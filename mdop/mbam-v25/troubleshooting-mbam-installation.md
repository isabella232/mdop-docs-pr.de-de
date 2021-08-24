---
title: Problembehandlung für MBAM 2.5-Installationsfehlern
description: Einführung in die Behandlung von MBAM 2.5-Installationsproblemen.
author: Deland-Han
ms.reviewer: dcscontentpm
manager: dansimp
ms.author: delhan
ms.sitesec: library
ms.prod: w10
ms.date: 09/16/2019
ms.openlocfilehash: 6ea152792801c630fa365f37d1668d1a4d84b3a5
ms.sourcegitcommit: 3e0500abde44d6a09c7ac8e3caf5e25929b490a4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2021
ms.locfileid: "11910630"
---
# <a name="troubleshooting-mbam-25-installation-problems"></a>Problembehandlung für MBAM 2.5-Installationsfehlern

In diesem Artikel wird erläutert, wie Sie Probleme mit der Installation von Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 in einer eigenständigen Konfiguration behandeln.

## <a name="referring-mbam-log-files-for-troubleshooting"></a>Verweisen auf MBAM-Protokolldateien zur Problembehandlung

MBAM umfasst die Protokollierung für Serverinstallation, Clientinstallation und Ereignisse. Auf diese Protokollierung sollte zur Problembehandlung verwiesen werden. 
 
### <a name="mbam-server-installation-log-files"></a>MBAM-Serverinstallationsprotokolldateien

MBAMServerSetup.exe generiert während der MBAM-Installation die folgenden Protokolldateien im Ordner %temp% des Benutzers:<br /> **Microsoft_BitLocker_Administration_and_Monitoring_<14 Nummern>.log**

MBAMServerSetup.exe protokolliert die Aktionen, die während der Installation von MBAM-Setup- und MBAM-Serverfeatures ausgeführt wurden:<br /> **Microsoft_BitLocker_Administration_and_Monitoring_<14_numbers>_0_MBAMServer.msi.log**

MBAMServerSetup.exe protokolliert zusätzliche Aktionen, die während der Installation ausgeführt wurden.

### <a name="mbam-client-installation-log-file"></a>MBAM-Clientinstallationsprotokolldatei

Die Clientinstallation wird in der folgenden Protokolldatei im Ordner %temp% aufgezeichnet (oder an einem benutzerdefinierten Speicherort, je nachdem, wie der Client installiert wurde): <br />**\<five random characters\>MSI.log**

Dieses Protokoll enthält die Aktionen, die während der MBAM-Clientinstallation ausgeführt werden.
 
### <a name="mbam-client-event-logging-channel"></a>MBAM-Clientereignisprotokollierungskanal

MBAM verfügt über separate Kanäle für die Ereignisprotokollierung. Die Protokolldateien "Admin", "Analytical" und "Operational" befinden sich in der Ereignisanzeige unter **"Anwendungs- und Dienstprotokolle**  >  **Microsoft**  >  **Windows**  >  **MBAM".**

Die folgende Tabelle enthält eine kurze Beschreibung der einzelnen Ereignisprotokolle.
 
|Ereignisprotokoll| Beschreibung|
|----------|-------|
|Microsoft-Windows-MBAM/Admin|  Enthält Fehlermeldungen|
|Microsoft-Windows-MBAM/Analytics|   Enthält erweiterte Protokollierungsinformationen|
|Microsoft-Windows-MBAM/Operational|    Enthält Erfolgsmeldungen|

### <a name="mbam-server-event-logging-channel"></a>MBAM-Serverereignisprotokollierungskanal

Die Protokolldateien befinden sich in der Ereignisanzeige unter **Anwendungs- und Dienstprotokolle**  >  **Microsoft**  >  **Windows**  >  **MBAM.** Die folgende Tabelle enthält Serverereignisprotokolle, die in MBAM 2.5 eingeführt wurden:

|Ereignisprotokoll| Beschreibung|
|--------|-------------|
|Microsoft-Windows-MBAM/Admin|  Enthält Fehlermeldungen|
|Microsoft-Windows-MBAM/Analytics|   Enthält erweiterte Protokollierungsinformationen|
|Microsoft-Windows-MBAM/Operational|    Enthält Erfolgsmeldungen|

### <a name="mbam-web-service-logs"></a>MBAM-Webdienstprotokolle

Jedes MBAM-Webdienstprotokoll schreibt Protokollierungsinformationen in eine SVCLOG-Datei. Standardmäßig schreibt jeder Webdienst die Ablaufverfolgungsdatei in einen Ordner, der seinen Namen im Ordner "C:\inetpub\Microsoft BitLocker-Verwaltungslösung\Protokolle" verwendet.

Sie können das Tool für die Dienstablaufverfolgungsanzeige (Teil von Microsoft Visual Studio) verwenden, um die Svclog-Ablaufverfolgungen zu überprüfen.

## <a name="troubleshooting-encryption-and-reporting-issues"></a>Behandeln von Verschlüsselungs- und Berichterstellungsproblemen

Dieser Abschnitt enthält Informationen zur Problembehandlung für Serverfunktionen, Clientfunktionen, Konfigurationseinstellungen und bekannte Probleme:
 
### <a name="mbam-client-installation-group-policy-settings"></a>MBAM-Clientinstallation, Gruppenrichtlinieneinstellungen

Ermitteln Sie, ob der MBAM-Agent auf dem Clientcomputer installiert ist. Wenn MBAM installiert ist, wird ein Dienst mit dem Namen BitLocker-Verwaltungsclientdienst erstellt. Dieser Dienst ist so konfiguriert, dass er automatisch gestartet wird. Bestimmen Sie, ob der Dienst ausgeführt wird.

Stellen Sie sicher, dass mbam-Gruppenrichtlinieneinstellungen auf dem Clientcomputer angewendet werden. Der folgende Registrierungsunterschlüssel wird erstellt, wenn die Gruppenrichtlinieneinstellungen auf dem Clientcomputer angewendet wurden: **HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement**

Stellen Sie sicher, dass dieser Schlüssel vorhanden ist und mithilfe von Werten pro Gruppenrichtlinieneinstellungen aufgefüllt wird.

### <a name="mbam-agent-in-the-initial-delay-period"></a>MBAM-Agent im anfänglichen Verzögerungszeitraum

Der MBAM-Client startet den Vorgang nicht unmittelbar nach der Installation. Es gibt eine anfängliche zufällige Verzögerung von 1 bis 18 Minuten, bevor der MBAM-Agent den Vorgang startet. Zusätzlich zur anfänglichen Verzögerung gibt es eine Verzögerung von mindestens 90 Minuten. (Die Verzögerung hängt von den Gruppenrichtlinieneinstellungen ab, die für die Häufigkeit der Überprüfung des Clientstatus konfiguriert sind.) Daher ist die gesamte Verzögerung vor dem Starten eines Clients *eine zufällige Startverzögerung,*  +  *bei der der Client die Häufigkeitsverzögerung überprüft.*

Wenn die Betriebs- und Administrator-Ereignisprotokolle leer sind, hat der Client den Vorgang noch nicht gestartet und befindet sich im Verzögerungszeitraum, der zuvor erwähnt wurde. Wenn Sie die Verzögerung umgehen möchten, führen Sie die folgenden Schritte aus:
 
1. Beenden Sie den BitLocker-Verwaltungsclientdienst.

2. Erstellen Sie unter dem ** RegistrierungsunterschlüsselHKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MBAM** den Registrierungswert **NoStartupDelay,** legen Sie seinen Typ auf **REG_DWORD**fest, und legen Sie dann den Wert auf **1**fest.

3. Legen ** Sie **unterHKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagementdie Werte **"ClientWakeupFrequency"** und **"StatusReportingFrequency"** auf **1**fest. Diese Werte werden auf ihre ursprünglichen Einstellungen zurückgesetzt, nachdem sich Gruppenrichtlinienupdates auf dem Computer befinden.

4. Starten Sie den BitLocker-Verwaltungsclientdienst.

Wenn Sie sich nach dem Start des Diensts lokal auf dem Computer anmelden und keine Fehler auftreten, sollten Sie innerhalb einer Minute eine Anforderung zum Verschlüsseln des Computers erhalten. Wenn Sie keine Anforderung erhalten, sollten Sie die MBAM-Administratorprotokolle auf Fehlereinträge überprüfen.

### <a name="computer-does-not-have-a-tpm-device-or-the-tpm-device-is-not-enabled-in-the-bios"></a>Der Computer verfügt nicht über ein TPM-Gerät, oder das TPM-Gerät ist im BIOS nicht aktiviert.

Überprüfen Sie das MBAM-Administratorereignisprotokoll. Im MBAM Admin-Ereignisprotokoll wird ein Ereigniseintrag angezeigt, der dem folgenden ähnelt:

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          8/3/2013 12:31:10 PM
    Event ID:      9
    Task Category: None
    Level:         Error
    Keywords:      
    User:          SYSTEM
    Computer:      Mbamclient.contoso.com
    Description:
    The TPM hardware is missing.
    TPM is needed to encrypt the operating system drive with any TPM protector.

Öffnen Sie die TPM-Verwaltung (tpm.msc), und überprüfen Sie, ob der Computer über ein TPM-Gerät verfügt. Wenn tpm.msc kein Gerät anzeigt, öffnen Sie den Geräte-Manager (devmgmt.msc), und suchen Sie unter "Sicherheitsgeräte" nach einem vertrauenswürdigen Plattformmodul. Wenn ein Gerät des vertrauenswürdigen Plattformmoduls nicht angezeigt wird, kann dies aus einem der folgenden Gründe zutreffen:

* Ihr System verfügt nicht über ein TRUSTED Platform Module (TPM/Security)-Gerät.

* Das TPM-Gerät ist im BIOS deaktiviert.

* TPM-Gerät ist im BIOS aktiviert, aber die Verwaltung des TPM-Geräts über die Betriebssystemeinstellung ist im BIOS deaktiviert.

* Sie verwenden keinen Microsoft-Treiber für das TPM-Gerät. Überprüfen Sie die im Geräte-Manager aufgeführten Geräte, um den Microsoft TPM-Gerätetreiber zu identifizieren.

Wenn das TPM-Gerät den C:\Windows\System32\tpm.sys Treiber nicht verwendet, sollten Sie den Treiber aktualisieren, indem Sie die Datei "C:\Windows\Inf\tpm.inf" auswählen.

### <a name="computer-does-not-have-a-valid-system-partition"></a>Computer verfügt nicht über eine gültige SYSTEM-Partition

Überprüfen Sie das MBAM-Administratorereignisprotokoll. Im MBAM Admin-Ereignisprotokoll wird ein Ereigniseintrag angezeigt, der dem folgenden ähnelt:

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          8/3/2013 4:13:37 AM
    Event ID:      8
    Task Category: None
    Level:         Error
    Keywords:      
    User:          SYSTEM
    Computer:      BITTESTVM.xtremelabs.com
    Description:
    The system volume is missing.
    SystemVolume is needed to encrypt the operating system drive.

BitLocker erfordert eine SYSTEM-Partition, um die Verschlüsselung zu aktivieren ([BitLocker-Laufwerkverschlüsselung in Windows 7: Häufig gestellte Fragen](https://docs.microsoft.com/previous-versions/windows/it-pro/windows-7/ee449438(v=ws.10)?redirectedfrom=MSDN#bkmk_partitions)).

MBAM erstellt die Systempartition nicht automatisch. Sie können das BitLocker-Laufwerkvorbereitungsprogramm (bdehdcfg.exe) verwenden, um die Systempartition zu erstellen und die erforderlichen Startdateien zu verschieben.

Sie können beispielsweise den Befehl **%windir%\system32\bdeHdCfg.exe -target default -size 300 –quiet** verwenden, um das Laufwerk im Hintergrund vorzubereiten, bevor Sie MBAM zum Verschlüsseln der Laufwerke bereitstellen. Dies erfordert einen Neustart. Sie können die Aktion auch skripten, wenn dies erforderlich ist. Im folgenden Dokument wird das BitLocker-Laufwerkvorbereitungstool beschrieben:

[Beschreibung des BitLocker-Laufwerkvorbereitungstools](https://support.microsoft.com/help/933246)

### <a name="drives-are-not-formatted-to-have-a-compatible-file-system"></a>Laufwerke sind nicht so formatiert, dass sie über ein kompatibles Dateisystem verfügen

Informationen zu Dateisystemanforderungen für BitLocker finden Sie im [TechNet-Artikel.](https://docs.microsoft.com/previous-versions/windows/it-pro/windows-7/ee449438(v=ws.10)?redirectedfrom=MSDN#bkmk_hsrequirements)

### <a name="group-policy-conflict"></a>Gruppenrichtlinienkonflikt

Im MBAM Admin-Ereignisprotokoll wird ein Ereigniseintrag angezeigt, der dem folgenden ähnelt:

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          7/25/2013 9:27:58 PM
    Event ID:      22
    Task Category: None
    Level:         Error
    Keywords:      
    User:          SYSTEM
    Computer:      Mbamclient.contoso.com
    Description:
    Detected Fixed Data Drive volume encryption policies conflict.
    Check BitLocker and MBAM policies related to FDD drive protectors.

Überprüfen Sie ihre Gruppenrichtlinieneinstellungen, um sicherzustellen, dass zwischen den MBAM-Gruppenrichtlinieneinstellungen keine widersprüchliche Einstellung vorhanden ist.

Sie sollten Die Gruppenrichtlinie mithilfe der MDOP MBAM-Vorlage und nicht der BitLocker-Laufwerkverschlüsselungsvorlage konfigurieren.

Zum Beispiel:

Unter den Verschlüsselungseinstellungen für das Betriebssystemlaufwerk haben Sie TPM als Schutzvorrichtung ausgewählt, und Sie haben auch **"Erweiterte PINs für den Start zulassen"** ausgewählt. Dies sind widersprüchliche Einstellungen, da für den reinen TPM-Schutz keine PIN erforderlich ist. Daher sollten Sie die erweiterte PINs-Einstellung deaktivieren.

### <a name="user-may-have-requested-an-exemption"></a>Der Benutzer hat möglicherweise eine Ausnahme angefordert.

Wenn Sie die Gruppenrichtlinieneinstellung "Computerkonfiguration\Administrative Vorlagen\Windows Komponenten\MDOP MBAM (BitLocker-Verwaltung)\Clientverwaltung\Gruppenrichtlinien für Benutzerausnahmerichtlinien konfigurieren" aktiviert haben, wird Benutzern die Möglichkeit angeboten, eine Ausnahme anzufordern.

Wenn der Benutzer eine Ausnahme anfordert, ist die Ausnahme standardmäßig 7 Tage gültig, und der Benutzer erhält während dieses Zeitraums keine Aufforderungen zur Verschlüsselung. (Der Standardwert kann während der Richtlinienkonfiguration erhöht oder verringert werden.) Nachdem der Freistellungszeitraum abgelaufen ist, wird der Benutzer aufgefordert, zu verschlüsseln.

Sie sehen den folgenden Eintrag im MBAM-Administratorereignisprotokoll, wenn ein Computer von der Benutzerbefreiung ausgenommen ist:

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          8/3/2013 3:06:40 PM
    Event ID:      13
    Task Category: None
    Level:         Warning
    Keywords:      
    User:          SYSTEM
    Computer:      MBAMCLIENT.contoso.com
    Description:
    The user is exempt from encryption.

Wenn Sie die Benutzerfreistellung für einen Computer manuell außer Kraft setzen möchten, führen Sie die folgenden Schritte aus:
 
1. Legen Sie den AllowUserExemption-Wert unter dem folgenden Registrierungsunterschlüssel auf **0** fest: <br />
**HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement**

2. Löschen Sie alle Registrierungswerte unter dem folgenden Registrierungsunterschlüssel mit Ausnahme von **AgentVersion,** **EncodedComputerName**und **Installed:**<br />
**HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MBAM**

    **Hinweis** Sie müssen den MBAM-Agent neu starten, damit die Änderungen wirksam werden.

Beachten Sie, dass nach dem Anwenden von Gruppenrichtlinien auf den Computer diese Werte möglicherweise auf ihre ursprünglichen Einstellungen zurückgesetzt werden.

### <a name="wmi-issue"></a>WMI-Problem

MBAM verwendet Methoden der win32_encryptablevolume-Klasse zum Verwalten von BitLocker. Wenn dieses Modul nicht registriert oder beschädigt ist, wird der MBAM-Client nicht ordnungsgemäß ausgeführt, und der folgende Ereigniseintrag wird im MBAM Admin-Ereignisprotokoll angezeigt:

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          7/27/2013 11:18:51 PM
    Event ID:      4
    Task Category: None
    Level:         Error
    Keywords:      
    User:          SYSTEM
    Computer:      BITTEST.xtremelabs.com
    Description:
    An error occurred while sending encryption status data.
    Error code:
    0x80041016 
    Details:
    NULL

Darüber hinaus können Sie feststellen, dass die Wiederherstellungs- und Hardwarerichtlinien nicht mit fehlercode 0x8007007e gelten. Dies bedeutet: "Das angegebene Modul konnte nicht gefunden werden."

Um dieses Problem zu beheben, sollten Sie die **win32_encryptablevolume** Klasse mithilfe des folgenden Befehls erneut registrieren:

```cmd
mofcomp c:\Windows\System32\wbem\win32_encryptablevolume.mof
```

## <a name="troubleshooting-mbam-agent-communication-issues"></a>Behandeln von Problemen mit der MBAM-Agent-Kommunikation

Dieser Abschnitt enthält Informationen zur Problembehandlung für die folgenden Probleme im Zusammenhang mit der MBAM-Agent-Kommunikation:

### <a name="incorrect-mbam-service-url"></a>Falsche MBAM-Dienst-URL

Wenn der Wert des MBAM-Konformitätsstatusdiensts oder des Wiederherstellungs- und Hardwarediensts falsch ist, wird im MBAM-Administratorereignisprotokoll auf dem Clientcomputer ein Ereigniseintrag angezeigt, der dem folgenden ähnelt:

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          8/3/2013 4:13:36 PM
    Event ID:      4
    Task Category: None
    Level:         Error
    Keywords:     
    User:          SYSTEM
    Computer:      Mbamclient.contoso.com
    Description:
    An error occurred while sending encryption status data.
    Error code:
    0x803d0010
    Details:
    The remote endpoint was not reachable.

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          8/3/2013 4:13:33 PM
    Event ID:      18
    Task Category: None
    Level:         Error
    Keywords:     
    User:          SYSTEM
    Computer:      Mbamclient.contoso.com
    Description:
    Unable to connect to the MBAM Recovery and Hardware service.
    Error code:
    0x803d0010
    Details:
    The remote endpoint was not reachable.

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          8/3/2013 4:20:32 PM
    Event ID:      4
    Task Category: None
    Level:         Error
    Keywords:     
    User:          SYSTEM
    Computer:      Mbamclient.contoso.com
    Description:
    An error occurred while sending encryption status data.
    Error code:
    0x803d0020
    Details:
    The endpoint address URL is invalid.

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          8/3/2013 4:20:32 PM
    Event ID:      18
    Task Category: None
    Level:         Error
    Keywords:     
    User:          SYSTEM
    Computer:      Mbamclient.contoso.com
    Description:
    Unable to connect to the MBAM Recovery and Hardware service.
    Error code:
    0x803d0020
    Details:
    The endpoint address URL is invalid.

Überprüfen Sie die Werte von **KeyRecoveryServiceEndPoint** und **StatusReportingServiceEndpoint** unter dem folgenden Registrierungsunterschlüssel auf dem Clientcomputer: <br />
**HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement**

Standardmäßig hat die URL für KeyRecoveryServiceEndPoint (MBAM Recovery and Hardware service endpoint) das folgende Format: <br />
**http:// : \<servername\> \<port\> /MBAMRecoveryAndHardwareService/CoreService.svc**

Standardmäßig hat die URL für StatusReportingServiceEndpoint (MBAM Status Reporting Service Endpoint) das folgende Format:<br />
**http:// : \<servername\> \<port\> /MBAMComplianceStatusService/StatusReportingService.svc**

> [!Note]
> Die URL sollte keine Leerzeichen enthalten.

Wenn die Dienst-URL falsch ist, sollten Sie die Dienst-URL in der folgenden Gruppenrichtlinieneinstellung korrigieren:

**Computerkonfiguration**  >  **Richtlinien**  >  **Administrative Vorlagen**  >  **Windows-Komponenten**  >  **MDOP MBAM (BitLocker-Verwaltung)**  >  **Clientverwaltung**  >  **Konfigurieren von MBAM-Diensten**

### <a name="connectivity-issue-that-affects-the-mbam-administration-server"></a>Verbindungsproblem, das sich auf den MBAM-Verwaltungsserver auswirkt

Der MBAM-Agent kann keine Updates für die Datenbank bereitstellen, wenn Konnektivitätsprobleme zwischen dem Client-Agent und dem MBAM-Verwaltungsserver vorhanden sind. In diesem Fall werden Sie Verbindungsfehlereinträge im MBAM-Administratorereignisprotokoll auf dem Clientcomputer feststellen:

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          29-04-2014 18:21:22
    Event ID:      2
    Task Category: None
    Level:         Error
    Keywords:     
    User:          SYSTEM
    Computer:      TESTLABS.CONTOSO.COM
    Description:
    An error occurred while applying MBAM policies.
    Volume ID:\\?\Volume{871c5858-2467-4d0b-8c83-d68af8ce10e5}\ 
    Error code:
    0x803D0010 
    Details:
    The remote endpoint was not reachable.
 
    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          29-04-2014 23:06:48
    Event ID:      2
    Task Category: None
    Level:         Error
    Keywords:     
    User:          SYSTEM
    Computer:      TESTLABS.CONTOSO.COM
    Description:
    An error occurred while applying MBAM policies.
    Volume ID:\\?\Volume{871c5858-2467-4d0b-8c83-d68af8ce10e5}\ 
    Error code:
    0x803D0006 
    Details:
    The operation did not complete within the time allotted.

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          02-09-2013 02:02:04
    Event ID:      18
    Task Category: None
    Level:         Error
    Keywords:     
    User:          SYSTEM
    Computer:      TESTLABS.CONTOSO.COM
    Description:
    Unable to connect to the MBAM Recovery and Hardware service.
    Error code:
    0x803D0010 
    Details:
    The remote endpoint was not reachable.

Grundlegende Prüfungen:

* Überprüfen Sie die grundlegende Konnektivität durch Pingen des MBAM-Verwaltungsservers nach Name und IP. Überprüfen Sie, ob Sie mit telnet oder portqry eine Verbindung mit der MBAM-Verwaltungswebsite oder dem Dienstport herstellen können.

* Stellen Sie sicher, dass der IIS-Dienst auf dem MBAM-Verwaltungs- und -Überwachungsserver ausgeführt wird und dass der MBAM-Webdienst auf demselben Port lauscht, der auf dem MBAM-Clientcomputer konfiguriert ist ( `netstat –ano | find "portnumber"` ).

* Stellen Sie sicher, dass die für die MBAM-Website konfigurierte Portnummer IIS-Manager (inetmgr) verwendet. Stellen Sie sicher, dass die Portnummer mit der Portnummer übereinstimmt, auf der der Client lauscht. Stellen Sie sicher, dass die Portnummer nicht von einer anderen Anwendung gemeinsam verwendet wird. Eine andere Anwendung auf dem Server sollte beispielsweise nicht denselben Port verwenden.

* Wenn eine Firewall vorhanden ist, stellen Sie sicher, dass der Port in der Firewall oder dem Proxyserver geöffnet ist.

* Wenn die Kommunikation zwischen Client und Server sicher ist, stellen Sie sicher, dass Sie ein gültiges SSL-Zertifikat verwenden.

* Überprüfen Sie die Netzwerkkonnektivität zwischen dem Webserver und dem Datenbankserver, an den die Daten zum Einfügen gesendet werden. Sie können die Datenbankkonnektivität vom Webserver zum Datenbankserver mithilfe des ODBC-Datenquellenadministrators überprüfen. Ausführliche SQL Server Informationen zur Verbindungsproblembehandlung finden Sie unter [Problembehandlung beim Herstellen einer Verbindung mit dem SQL Server Datenbank-Engine.](https://social.technet.microsoft.com/wiki/contents/articles/2102.how-to-troubleshoot-connecting-to-the-sql-server-database-engine.aspx)

#### <a name="troubleshooting-the-connectivity-issue"></a>Problembehandlung des Verbindungsproblems

Stellen Sie sicher, dass die Dienst-URL, die auf dem Client konfiguriert ist, korrekt ist. Kopieren Sie den Wert der URL für KeyRecoveryServiceEndPoint (**HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement**) aus der Registrierung, und öffnen Sie ihn in Internet Explorer.

Kopieren Sie auf ähnliche Weise den Wert der URL für StatusReportingServiceEndpoint (HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement), und öffnen** Sie **ihn in Internet Explorer.

> [!Note]
> Wenn Sie vom Clientcomputer nicht zur URL navigieren können, sollten Sie die grundlegende Netzwerkkonnektivität vom Client mit dem Server testen, auf dem IIS ausgeführt wird. Siehe Die Punkte 1, 2, 3 und 4 im vorherigen Abschnitt.

Überprüfen Sie außerdem die Anwendungsprotokolle auf dem Verwaltungs- und Überwachungsserver auf Fehler.

Sie können eine gleichzeitige Netzwerkablaufverfolgung zwischen dem Client und dem Server erstellen und die Ablaufverfolgung überprüfen, um die Ursache des Verbindungsfehlers zwischen dem Client-Agent und dem MBAM-Verwaltungsserver zu ermitteln.

> [!Note]
> Wenn Sie vom Clientcomputer zu den Dienst-URLs navigieren können und verbindungsfehlereinträge in den MBAM-Administratorereignisprotokollen vorhanden sind, kann dies auf einen Verbindungsfehler zwischen dem Verwaltungsserver und dem Datenbankserver zurückzuführen sein.

Wenn Sie erfolgreich zu beiden Dienst-URLs navigieren können und eine Verbindung zwischen dem Client und dem server besteht, der ausgeführt wird, funktioniert IIS. Es kann jedoch ein Problem bei der Kommunikation zwischen dem Server, auf dem IIS ausgeführt wird, und dem Datenbankserver auftreten.

Die MBAM-Dienste können aufgrund eines Netzwerkproblems oder einer falschen Einstellung der Datenbankverbindungszeichenfolge möglicherweise keine Verbindung mit dem Datenbankserver herstellen. Überprüfen Sie die Anwendungsprotokolle auf dem Verwaltungs- und Überwachungsserver. Möglicherweise werden Fehlereinträge oder Warnungen aus der Quelle ASP.NET 2.0.50727.0 angezeigt, die dem folgenden Protokolleintrag ähneln:

    Log Name:      Application
    Source:        ASP.NET 2.0.50727.0
    Date:          7/11/2013 6:16:34 PM
    Event ID:      1310
    Task Category: Web Event
    Level:         Warning
    Keywords:      Classic
    User:          N/A
    Computer:      MBAM2-Admin.contoso.com
    Description:
    Event code: 100001
    Event message: SQL error occurred
    Event time: 7/11/2013 6:16:34 PM
    Event time (UTC): 7/11/2013 12:46:34 PM
    Event ID: 6615fb8eb9d54e778b933d5bb7ca91ed
    Event sequence: 2
    Event occurrence: 1
    Event detail code: 0 
    Application information:
        Application domain: /LM/W3SVC/2/ROOT/MBAMAdministrationService-1-130180202570338699
        Trust level: Full
        Application Virtual Path: /MBAMAdministrationService
        Application Path: C:\inetpub\Microsoft BitLocker Management Solution\Administration Service\
        Machine name: MBAM2-ADMIN 
    
    Process information:
        Process ID: 1940
        Process name: w3wp.exe
        Account name: NT AUTHORITY\NETWORK SERVICE 
    
    Exception information:
        Exception type: SqlException
        Exception message: A network-related or instance-specific error occurred while establishing a connection to SQL Server. The server was not found or was not accessible. Verify that the instance name is correct and that SQL Server is configured to allow remote connections. (provider: Named Pipes Provider, error: 40 - Could not open a connection to SQL Server) 
    
    Request information:
        Request URL: 
        Request path: 
        User host address: 
        User: 
        Is authenticated: False
        Authentication Type: 
        Thread account name: NT AUTHORITY\NETWORK SERVICE 
    
    Thread information:
        Thread ID: 7
        Thread account name: NT AUTHORITY\NETWORK SERVICE
        Is impersonating: False
        Stack trace:    at System.Data.SqlClient.SqlInternalConnection.OnError(SqlException exception, Boolean breakConnection)
       at System.Data.SqlClient.TdsParser.ThrowExceptionAndWarning(TdsParserStateObject stateObj)
       at System.Data.SqlClient.TdsParser.Connect(ServerInfo serverInfo, SqlInternalConnectionTds connHandler, Boolean ignoreSniOpenTimeout, Int64 timerExpire, Boolean encrypt, Boolean trustServerCert, Boolean integratedSecurity, SqlConnection owningObject)
       at System.Data.SqlClient.SqlInternalConnectionTds.AttemptOneLogin(ServerInfo serverInfo, String newPassword, Boolean ignoreSniOpenTimeout, Int64 timerExpire, SqlConnection owningObject)
       at System.Data.SqlClient.SqlInternalConnectionTds.LoginNoFailover(String host, String newPassword, Boolean redirectedUserInstance, SqlConnection owningObject, SqlConnectionString connectionOptions, Int64 timerStart)
       at System.Data.SqlClient.SqlInternalConnectionTds.OpenLoginEnlist(SqlConnection owningObject, SqlConnectionString connectionOptions, String newPassword, Boolean redirectedUserInstance)
       at System.Data.SqlClient.SqlInternalConnectionTds..ctor(DbConnectionPoolIdentity identity, SqlConnectionString connectionOptions, Object providerInfo, String newPassword, SqlConnection owningObject, Boolean redirectedUserInstance)
       at System.Data.SqlClient.SqlConnectionFactory.CreateConnection(DbConnectionOptions options, Object poolGroupProviderInfo, DbConnectionPool pool, DbConnection owningConnection)
       at System.Data.ProviderBase.DbConnectionFactory.CreatePooledConnection(DbConnection owningConnection, DbConnectionPool pool, DbConnectionOptions options)
       at System.Data.ProviderBase.DbConnectionPool.CreateObject(DbConnection owningObject)
       at System.Data.ProviderBase.DbConnectionPool.UserCreateRequest(DbConnection owningObject)
       at System.Data.ProviderBase.DbConnectionPool.GetConnection(DbConnection owningObject)
       at System.Data.ProviderBase.DbConnectionFactory.GetConnection(DbConnection owningConnection)
       at System.Data.ProviderBase.DbConnectionClosed.OpenConnection(DbConnection outerConnection, DbConnectionFactory connectionFactory)
       at System.Data.SqlClient.SqlConnection.Open()
       at System.Data.Linq.SqlClient.SqlConnectionManager.UseConnection(IConnectionUser user)
       at System.Data.Linq.SqlClient.SqlProvider.get_IsSqlCe()
       at System.Data.Linq.SqlClient.SqlProvider.InitializeProviderMode()
       at System.Data.Linq.SqlClient.SqlProvider.System.Data.Linq.Provider.IProvider.Execute(Expression query)
       at System.Data.Linq.DataContext.ExecuteMethodCall(Object instance, MethodInfo methodInfo, Object[] parameters)
       at Microsoft.Mbam.Server.ServiceCommon.KeyRecoveryModelDataContext.GetRecoveryKeyIds(String partialRecoveryKeyId, String reason)
       at Microsoft.Mbam.ApplicationSupportService.AdministrationService.GetRecoveryKeyIds(String partialRecoveryKeyId, String reasonCode)
    
    Custom event details:
        Application: MBAMAdministrationService
        Sql Server:
        Database: MBAM Recovery and Hardware
        Database: MBAM Compliance Status
        Sql ErrorCode: 5
        Error Message: A network-related or instance-specific error occurred while establishing a connection to SQL Server. The server was not found or was not accessible. Verify that the instance name is correct and that SQL Server is configured to allow remote connections. (provider: Named Pipes Provider, error: 40 - Could not open a connection to SQL Server)

#### <a name="possible-causes"></a>Mögliche Ursachen

##### <a name="cause-1"></a>Ursache 1

Der Administrator hat möglicherweise während der Installation von Verwaltungs- und Überwachungsserverkomponenten einen ungültigen Datenbankinstanznamen/Datenbanknamen angegeben.

Sie können die Datenbankverbindungszeichenfolgen mithilfe der IIS-Verwaltungskonsole überprüfen und korrigieren. Öffnen Sie dazu den IIS-Manager, und navigieren Sie zu Microsoft BitLocker Administration and Monitoring. Führen Sie für jeden Dienst, der auf der linken Seite aufgeführt ist, die folgenden Schritte aus, um die Datenbankverbindungszeichenfolgen zu ändern:

1. Wählen Sie in **der Featuresansicht** **Verbindungszeichenfolgen**aus.

2. Wählen Sie auf der Seite **"Verbindungszeichenfolgen"** die Verbindungszeichenfolge aus, die Sie ändern möchten.

3. Wählen Sie im Bereich **"Aktionen"** die Option **"Bearbeiten"** aus.

4. Ändern Sie im Dialogfeld **Verbindungszeichenfolge bearbeiten** die Eigenschaften, die Sie ändern möchten, und wählen Sie dann **OK**aus.

##### <a name="cause-2"></a>Ursache 2

SQL Server port blocked in firewall. Überprüfen Sie die Portnummer, auf die SQL Server für das Überwachen konfiguriert ist, und stellen Sie sicher, dass der Port in der Firewall zwischen dem Verwaltungsserver und dem Datenbankserver geöffnet ist.

##### <a name="cause-3"></a>Ursache 3

Falsche SQL Tcp/IP-Serverbindungen. Überprüfen Sie SQL TCP/IP-Bindungen in SQL Server-Konfigurations-Manager auf dem Datenbankserver. MBAM erfordert, dass die Protokolle TCP/IP und Named Pipe für die Verbindung mit der Datenbank aktiviert sind.

##### <a name="cause-4"></a>Ursache 4

Das NT Authority\Network Service-Konto oder das Computerkonto des MBAM-Verwaltungsservers verfügt nicht über die erforderlichen Berechtigungen, um eine Verbindung mit der SQL Datenbank herzustellen.

Während der Installation von Datenbankkomponenten auf dem Datenbankserver erstellt das Installationsprogramm zwei lokale Gruppen: MBAM Compliance Auditing DB Access und MBAM Recovery and Hardware DB Access.

Das NT Authority\Network Service-Konto, das Computerkonto des MBAM-Verwaltungsservers und der Benutzer, der die Datenbankkomponenten installiert, werden diesen Gruppen automatisch hinzugefügt.

Diesen Gruppen werden während der Installation die erforderlichen Berechtigungen für die Datenbank gewährt. Alle Benutzer, die Teil dieser Gruppe sind, erhalten automatisch die erforderlichen Berechtigungen für die Datenbank.

Der Webdienst stellt aufgrund eines Berechtigungsproblems möglicherweise keine Verbindung mit dem Datenbankserver her, wenn eine oder mehrere der folgenden Bedingungen erfüllt sind:

* Die zuvor erwähnten Gruppen werden aus den lokalen Gruppen auf dem Datenbankserver entfernt.

* Das NT Authority\Network Service-Konto und das Computerkonto des MBAM-Verwaltungsservers sind keine Mitglieder dieser Gruppen.

* Diese Gruppen verfügen nicht über die erforderlichen Berechtigungen für die Datenbank.

Sie werden in den Anwendungsprotokollen auf dem MBAM-Verwaltungs- und Überwachungsserver Fehler im Zusammenhang mit Berechtigungen feststellen, wenn eine der vorherigen Bedingungen zutrifft. In diesem Fall sollten Sie das NT Authority\Network Service-Konto und das Computerkonto des MBAM-Verwaltungsservers manuell hinzufügen und ihm eine serverweite öffentliche Rolle auf dem SQL Datenbankserver gewähren, der SQL Server Management Studio ( https://msdn.microsoft.com/library/aa337562.aspx) verwendet.

#### <a name="review-the-web-service-logs"></a>Überprüfen der Webdienstprotokolle

Wenn in den Anwendungsprotokollen auf dem MBAM-Verwaltungsserver keine Ereignisse protokolliert werden, ist es an der Zeit, die Webdienstprotokolle (SVCLOG) des MBAM-Webdiensts zu überprüfen, der auf dem MBAM-Verwaltungs- und Überwachungsserver gehostet wird. Sie müssen das Dienstablaufverfolgungs-Viewer-Tool (SvcTraceViewer.exe) https://msdn.microsoft.com/library/ms732023.aspx verwenden, um die Protokolldatei anzuzeigen.

Sie sollten in erster Linie die Dienstablaufverfolgungsprotokolle von RecoveryandHardwareService und ComplianceStatusService untersuchen. Standardmäßig befinden sich Webdienstprotokolle im Ordner "C:\inetpub\Microsoft BitLocker-Verwaltungslösung\Protokolle". Dort schreibt jeder Dienst seine SVCLOG-Datei in einen eigenen Ordner.

Überprüfen Sie die Aktivität im Dienstablaufverfolgungsprotokoll auf Fehler- oder Warnungseinträge. Standardmäßig werden Fehlereinträge rot hervorgehoben. Wählen Sie die Fehlerbeschreibung im rechten Bereich der Ablaufverfolgungsanzeige aus, um detaillierte Informationen zum Fehlereintrag anzuzeigen. Es folgt ein Beispielfehlereintrag aus dem Ablaufverfolgungsprotokoll:

    <E2ETraceEvent xmlns="http://schemas.microsoft.com/2004/06/E2ETraceEvent">
    <System xmlns="http://schemas.microsoft.com/2004/06/windows/eventlog/system">
    <EventID>15183</EventID>
    <Type>3</Type>
    <SubType Name="Error">0</SubType>
    <Level>2</Level>
    <TimeCreated SystemTime="2013-07-05T14:48:06.2821550Z" />
    <Source Name="Microsoft.Mbam.CoreService" />
    <Correlation ActivityID="{00000000-0000-0000-0000-000000000000}" />
    <Execution ProcessName="w3wp" ProcessID="4332" ThreadID="11" />
    <Channel />
    <Computer>XXXXXXXXXXX</Computer>
    </System>
    <ApplicationData>AddUpdateVolume: While executing sql transaction for add volume to store exception occurred Key Recovery Data Store processing error: Violation of UNIQUE KEY constraint 'UniqueRecoveryKeyId'. Cannot insert duplicate key in object 'RecoveryAndHardwareCore.Keys'. The duplicate key value is (8637036e-b379-4798-bd9e-5a0b36296de3).
    </ApplicationData>
    </E2ETraceEvent>

## <a name="re-installation-or-reconfiguration-of-mbam-infrastructure"></a>Erneute Installation oder Neukonfiguration der MBAM-Infrastruktur

Um die MBAM-Infrastruktur neu zu installieren oder neu zu konfigurieren, müssen Sie die folgenden Dinge kennen:

* Anwendungspoolkonto

* MBAM-Gruppen (Helpdesk, Erweitert, Berichtbenutzergruppe)

* URL für MBAM-Berichte

* SQL Server- und Datenbanknamen

* MBAM ReadWrite- und ReadOnly-Konten

### <a name="application-pool-account"></a>Anwendungspoolkonto

Um das Anwendungspoolkonto zu finden, melden Sie sich beim MBAM-Webserver an, öffnen **Sie Internetinformationsdienste (IIS)-Manager,** und wählen Sie dann **Anwendungspools aus:**

![Anwendungspools.](images/troubleshooting-MBAM-installation-1.png)

Der Dienstprinzipalname (SERVICE Principal Name, SPN) muss in diesem Konto festgelegt werden. Diese Einstellung ist sehr wichtig für die Funktionalität von MBAM.

### <a name="mbam-groups-helpdesk-advanced-report-users-group-and-reports-url"></a>MBAM-Gruppen (Helpdesk, Erweitert, Berichtsbenutzergruppe und Berichts-URL)

![MBAM-Gruppen.](images/troubleshooting-MBAM-installation-2.png)

Dies enthält Informationen wie Helpdesk-Gruppe, Erweiterte Helpdesk-Gruppe, Gruppe "Berichtsbenutzer" und MBAM-Berichts-URL. Die URL für MBAM-Berichte muss im MBAM-Setup angegeben werden und sollte wie folgt lauten: http(s)://servername/ReportServer.

### <a name="sql-server-name-and-database-db-names"></a>SQL Server Namen und Datenbanknamen (DB)

Um die SQL Server Namen und Instanzen zu finden, die die MBAM-DBs hosten, melden Sie sich beim MBAM Web (IIS)-Server an, und navigieren Sie zum untergeordneten Registrierungsunterschlüssel:

**HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MBAM Server\Web**

![Regedit.](images/troubleshooting-MBAM-installation-3.png)

Die hervorgehobenen Teile sind Verbindungszeichenfolgen. Diese sollten den SQL Server Namen, Datenbanknamen und Instanzen (sofern benannt) aufweisen.

### <a name="mbam-readwrite-and-readonly-accounts"></a>MBAM ReadWrite- und ReadOnly-Konten

Diese Informationen befinden sich in der SQL Server Datenbank, für die der Name bereits vom Webserver gefunden wurde.

#### <a name="readwrite-account"></a>ReadWrite-Konto

1. Melden Sie sich beim SQL Management Studio an.

2. Klicken Sie mit der rechten Maustaste auf **MBAM-Wiederherstellung und Hardware,** wählen Sie **"Eigenschaften"** und dann **"Berechtigungen" aus.**

Der Name des Lab-Kontos lautet beispielsweise **MBAMWrite.** Die Konten "Anwendungspool" und "ReadWrite" sind auf "identisch" festgelegt.

![SQL DB.](images/troubleshooting-MBAM-installation-4.png)

![DB-Eigenschaften.](images/troubleshooting-MBAM-installation-5.png)

Navigieren Sie zu **"Sicherheit",** und **melden Sie sich** dann in SQL Management Studio an. Navigieren Sie zu dem Konto, das im vorherigen Screenshot angezeigt wurde.

![SQL Sicherheit.](images/troubleshooting-MBAM-installation-6.png)

Klicken Sie mit der rechten Maustaste auf die Konten, wechseln Sie zu **Eigenschaftenbenutzerzuordnung,** und suchen Sie die MBAM-Wiederherstellungs- und Hardwaredatenbank:

![Benutzerzuordnung.](images/troubleshooting-MBAM-installation-7.png)

#### <a name="readonly-account"></a>ReadOnly-Konto

Öffnen Sie SQL Server Reporting Services Configuration Manager auf dem SSRS-Server. Wählen Sie **die Berichts-Manager-URL**aus, und navigieren Sie dann zu den **URLs:**

![Berichts-Manager.](images/troubleshooting-MBAM-installation-8.png)

Wählen Sie **Microsoft Bitlocker Administration and Monitoring**aus:

![Bitlocker-Verwaltung und -Überwachung.](images/troubleshooting-MBAM-installation-9.png)

Wählen Sie **"MaltaDatasource" aus:**

![Dbs.](images/troubleshooting-MBAM-installation-10.png)

![MaltaDatasource.](images/troubleshooting-MBAM-installation-11.png)

"MaltaDataSource" sollte den Namen des ReadOnly-Kontos haben und beim MBAM-Setup verwendet werden.

## <a name="reference"></a>Verweis

Weitere Informationen finden Sie in den folgenden Artikeln:

[Bereitstellen von MBAM 2.5 in einer eigenständigen Konfiguration](https://support.microsoft.com/help/3046555)

[Microsoft BitLocker Administration and Monitoring 2.5](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/)
