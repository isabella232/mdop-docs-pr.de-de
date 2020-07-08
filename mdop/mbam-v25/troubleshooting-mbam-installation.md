---
title: Problembehandlung für MBAM 2.5-Installationsfehlern
description: Hier erfahren Sie, wie Sie MBAM 2,5-Installationsprobleme beheben.
author: Deland-Han
ms.reviewer: dcscontentpm
manager: dansimp
ms.author: delhan
ms.sitesec: library
ms.prod: w10
ms.date: 09/16/2019
ms.openlocfilehash: ed56a87496e09601c44028b7f948eda39143e8c0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804547"
---
# Problembehandlung für MBAM 2.5-Installationsfehlern

In diesem Artikel wird erläutert, wie Sie Probleme mit der 2,5-Installation von Microsoft BitLocker Administration and Monitoring (MBAM) in einer eigenständigen Konfiguration beheben.

## Verweisen auf MBAM-Protokolldateien zur Problembehandlung

MBAM umfasst die Protokollierung für die Server Installation, die Clientinstallation und die Ereignisse. Auf diese Protokollierung sollte zur Problembehandlung verwiesen werden. 
 
### MBAM-Server Installationsprotokolldateien

MBAMServerSetup.exe generiert die folgenden Protokolldateien im Ordner "% Temp%" des Benutzers während der MBAM-Installation:<br /> **Microsoft_BitLocker_Administration_and_Monitoring_<14 Nummern>. log**

MBAMServerSetup.exe protokolliert die Aktionen, die während der Installation des MBAM-Setups und der MBAM-Server Features ausgeführt wurden:<br /> **Microsoft_BitLocker_Administration_and_Monitoring_<14_numbers # C1_0_MBAMServer.msi. log**

MBAMServerSetup.exe protokolliert weitere Aktionen, die während der Installation ausgeführt wurden.

### MBAM-Client Installationsprotokolldatei

Die Clientinstallation wird in der folgenden Protokolldatei im Ordner "% Temp%" (oder an einem benutzerdefinierten Speicherort) aufgezeichnet, je nachdem, wie der Client installiert wurde. <br />**MSI \<five random characters\> . log**

Dieses Protokoll enthält die Aktionen, die während der MBAM-Clientinstallation ausgeführt werden.
 
### MBAM-Clientereignisprotokoll Kanal

MBAM verfügt über separate Ereignis Protokollierungs Kanäle. Die Administrator-, Analyse-und Betriebsprotokoll Dateien befinden sich in der Ereignisanzeige unter **Anwendungs-und Dienstprotokolle**  >  **Microsoft**  >  **Windows**-  >  **MBAM**.

Die folgende Tabelle enthält eine kurze Beschreibung der einzelnen Ereignisprotokolle.
 
|Ereignisprotokoll| Beschreibung|
|----------|-------|
|Microsoft-Windows-MBAM/Administrator|  Enthält Fehlermeldungen|
|Microsoft-Windows-MBAM/Analyse|   Enthält erweiterte Protokollierungsinformationen|
|Microsoft-Windows-MBAM/betriebsbereit|    Enthält Erfolgs Nachrichten|

### MBAM Server-Ereignisprotokollkanal

Die Protokolldateien befinden sich in der Ereignisanzeige unter **Anwendungs-und Dienstprotokolle**  >  **Microsoft**  >  **Windows**-  >  **MBAM**. Die folgende Tabelle enthält Serverereignisprotokolle, die in MBAM 2,5 eingeführt wurden:

|Ereignisprotokoll| Beschreibung|
|--------|-------------|
|Microsoft-Windows-MBAM/Administrator|  Enthält Fehlermeldungen|
|Microsoft-Windows-MBAM/Analyse|   Enthält erweiterte Protokollierungsinformationen|
|Microsoft-Windows-MBAM/betriebsbereit|    Enthält Erfolgs Nachrichten|

### MBAM-Webdienstprotokolle

Jedes MBAM-Webdienstprotokoll schreibt Protokollierungsinformationen in eine SVCLOG-Datei. Standardmäßig schreibt jeder Webdienst die Ablaufverfolgungsdatei unter einen Ordner, dessen Namen im C:\inetpub\Microsoft BitLocker-Verwaltungs Solution\Logs-Ordner verwendet wird.

Sie können das Tool Dienstablauf Verfolgungs Anzeige (Teil von Microsoft Visual Studio) verwenden, um die SVCLOG-Ablaufverfolgungen zu überprüfen.

## Problembehandlung bei Verschlüsselungs-und Berichterstattungsproblemen

Dieser Abschnitt enthält Informationen zur Problembehandlung für Serverfunktionen, Clientfunktionen, Konfigurationseinstellungen und bekannte Probleme:
 
### MBAM-Clientinstallation, Gruppenrichtlinieneinstellungen

Ermitteln Sie, ob der MBAM-Agent auf dem Clientcomputer installiert ist. Wenn MBAM installiert ist, wird ein Dienst mit dem Namen BitLocker-Verwaltungs Client Dienst erstellt. Dieser Dienst ist so konfiguriert, dass er automatisch gestartet wird. Ermitteln Sie, ob der Dienst ausgeführt wird.

Stellen Sie sicher, dass MBAM-Gruppenrichtlinieneinstellungen auf dem Clientcomputer angewendet werden. Der folgende Registrierungsunterschlüssel wird erstellt, wenn die Gruppenrichtlinieneinstellungen auf dem Clientcomputer angewendet wurden: **HKEY_LOCAL_MACHINE \software\policies\microsoft\fve\mdopbitlockermanagement**

Überprüfen Sie, ob dieser Schlüssel vorhanden ist und mit Werten pro Gruppenrichtlinieneinstellungen gefüllt wird.

### MBAM-Agent in der anfänglichen Verzögerungszeit

Der MBAM-Client startet den Vorgang nicht unmittelbar nach der Installation. Es gibt eine anfängliche zufällige Verzögerung von 1 bis 18 Minuten, bevor der MBAM-Agent seinen Vorgang startet. Zusätzlich zu der anfänglichen Verzögerung gibt es eine Verzögerung von mindestens 90 Minuten. (Die Verzögerung hängt von den Gruppenrichtlinieneinstellungen ab, die für die Häufigkeit der Überprüfung des Clientstatus konfiguriert sind.) Daher ist die Gesamtverzögerung, bevor ein Client den Vorgang *random startup delay*startet, die  +  *Häufigkeits Verzögerung für den Client zur Überprüfung der Häufigkeit*beim Start verzögert.

Wenn die Ereignisprotokolle für Betriebs-und Administratoren leer sind, hat der Client den Vorgang noch nicht begonnen und befindet sich in der zuvor erwähnten Verzögerungszeit. Wenn Sie die Verzögerung umgehen möchten, führen Sie die folgenden Schritte aus:
 
1. Beenden des BitLocker-Verwaltungs Client-Dienst Diensts

2. Erstellen Sie unter dem Registrierungsschlüssel **HKEY_LOCAL_MACHINE \software\microsoft\mbam** den Registrierungswert **NoStartupDelay** , legen Sie seinen Typ auf **REG_DWORD**, und legen Sie dann seinen Wert auf **1**.

3. Setzen Sie unter **HKEY_LOCAL_MACHINE \software\policies\microsoft\fve\mdopbitlockermanagement**die Werte für **ClientWakeupFrequency** und **StatusReportingFrequency** auf **1**. Diese Werte werden auf die ursprünglichen Einstellungen zurückgesetzt, nachdem die Gruppenrichtlinienupdates auf dem Computer installiert wurden.

4. Starten Sie den BitLocker-Verwaltungs Client-Dienst.

Wenn Sie sich nach dem Start des Diensts lokal auf dem Computer anmelden und keine Fehler auftreten, sollten Sie eine Anforderung erhalten, den Computer innerhalb einer Minute zu verschlüsseln. Wenn Sie keine Anforderung erhalten, sollten Sie die MBAM-Administrator Protokolle auf Fehlereinträge überprüfen.

### Der Computer verfügt nicht über ein TPM-Gerät, oder das TPM-Gerät ist im BIOS nicht aktiviert.

Überprüfen Sie das MBAM-Administrator Ereignisprotokoll. Im MBAM-Administrator Ereignisprotokoll sehen Sie einen Ereigniseintrag, der wie folgt aussieht:

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

Öffnen Sie die TPM-Verwaltung (TPM. msc), und überprüfen Sie, ob auf dem Computer ein TPM-Gerät installiert ist. Wenn TPM. msc kein Gerät anzeigt, öffnen Sie den Geräte-Manager (devmgmt. msc), und suchen Sie unter Sicherheitsgeräten nach einem vertrauenswürdigen Plattformmodul. Wenn kein Trusted Platform Module-Gerät angezeigt wird, kann dies aus einem der folgenden Gründe zutreffen:

* Ihr System verfügt nicht über ein Trusted Platform Module (TPM/Security)-Gerät.

* Das TPM-Gerät ist im BIOS deaktiviert.

* Das TPM-Gerät ist im BIOS aktiviert, die Verwaltung des TPM-Geräts aus der Betriebssystem Einstellung ist im BIOS jedoch deaktiviert.

* Sie verwenden keinen Microsoft-Treiber für das TPM-Gerät. Überprüfen Sie die Geräte, die im Geräte-Manager aufgeführt sind, um den Microsoft TPM-Gerätetreiber zu identifizieren.

Wenn das TPM-Gerät nicht den C:\Windows\System32\tpm.sys Treiber verwendet, sollten Sie den Treiber aktualisieren, indem Sie die C:\Windows\Inf\tpm.inf-Datei auswählen.

### Computer hat keine gültige System Partition

Überprüfen Sie das MBAM-Administrator Ereignisprotokoll. Im MBAM-Administrator Ereignisprotokoll sehen Sie einen Ereigniseintrag, der wie folgt aussieht:

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

Für BitLocker ist eine System Partition erforderlich, um die Verschlüsselung zu aktivieren ([BitLocker-Laufwerkverschlüsselung in Windows 7: häufig gestellte Fragen](https://docs.microsoft.com/previous-versions/windows/it-pro/windows-7/ee449438(v=ws.10)?redirectedfrom=MSDN#bkmk_partitions)).

MBAM erstellt die Systempartition nicht automatisch. Sie können das BitLocker Drive Preparation Utility (bdehdcfg.exe) verwenden, um die Systempartition zu erstellen und die erforderlichen Startdateien zu verschieben.

So können Sie beispielsweise den Befehl **% Windir% \system32\bdeHdCfg.exe-Target Standardgröße 300 – quiet** verwenden, um das Laufwerk im Hintergrund vorzubereiten, bevor Sie MBAM bereitstellen, um die Laufwerke zu verschlüsseln. Hierfür ist ein Neustart erforderlich. Sie können die Aktion auch erstellen, wenn dies erforderlich ist. Das folgende Dokument beschreibt das BitLocker-Laufwerk Vorbereitungs Tool:

[Beschreibung des BitLocker-Laufwerk Vorbereitungstools](https://support.microsoft.com/help/933246)

### Laufwerke sind nicht für ein kompatibles Dateisystem formatiert

Informationen zu den [Dateisystemanforderungen für BitLocker](https://docs.microsoft.com/previous-versions/windows/it-pro/windows-7/ee449438(v=ws.10)?redirectedfrom=MSDN#bkmk_hsrequirements)finden Sie im TechNet-Artikel.

### Gruppenrichtlinienkonflikt

Im MBAM-Administrator Ereignisprotokoll sehen Sie einen Ereigniseintrag, der wie folgt aussieht:

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

Überprüfen Sie Ihre Gruppenrichtlinieneinstellungen, um sicherzustellen, dass Sie keine widersprüchlichen Einstellungen zwischen den MBAM-Gruppenrichtlinieneinstellungen haben.

Sie sollten die Gruppenrichtlinie mithilfe der MDOP-MBAM-Vorlage und nicht mit der BitLocker-Laufwerk Verschlüsselungs Vorlage konfigurieren.

Beispiel:

Unter Verschlüsselungseinstellungen für das Betriebssystemlaufwerk haben Sie TPM als Protector ausgewählt, und Sie haben auch die Option **Erweiterte Pins für den Start zulassen**ausgewählt. Hierbei handelt es sich um in Konflikt stehende Einstellungen, da für den TPM-only-Schutz keine PIN erforderlich ist. Daher sollten Sie die Einstellung für erweiterte Pins deaktivieren.

### Der Benutzer hat möglicherweise eine Ausnahme beantragt.

Wenn Sie die Gruppenrichtlinieneinstellung "Computer Configuration\Administrative Vorlagen\Windows-Komponenten\Internet Components\MDOP MBAM (BitLocker-Verwaltung) \Client Management\Configure Benutzer Freistellungs Richtlinien aktiviert haben, wird Benutzern die Möglichkeit angeboten, eine Ausnahme zu beantragen.

Wenn der Benutzer eine Befreiung anfordert, ist die Ausnahme standardmäßig 7 Tage gültig, und der Benutzer erhält während dieses Zeitraums keine Aufforderungen zur Verschlüsselung. (Der Standardwert kann während der Richtlinienkonfiguration erhöht oder verringert werden.) Nachdem der frei stellungs Zeitraum beendet ist, wird der Benutzer aufgefordert, zu verschlüsseln.

Der folgende Eintrag wird im MBAM-Administrator Ereignisprotokoll angezeigt, wenn ein Computer unter einer Benutzer Befreiung steht:

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

Wenn Sie die Benutzer Befreiung für einen Computer manuell außer Kraft setzen möchten, führen Sie die folgenden Schritte aus:
 
1. Setzen Sie den AllowUserExemption-Wert unter dem folgenden Registrierungsunterschlüssel auf **0** : <br />
**HKEY_LOCAL_MACHINE \software\policies\microsoft\fve\mdopbitlockermanagement**

2. Löschen Sie alle Registrierungswerte unter dem folgenden Registrierungsunterschlüssel, mit Ausnahme von **Agentversion**, **EncodedComputerName**und **installiert**:<br />
**HKEY_LOCAL_MACHINE \software\microsoft\mbam**

    **Hinweis** Sie müssen den MBAM-Agent neu starten, damit die Änderungen wirksam werden.

Beachten Sie, dass diese Werte möglicherweise auf die ursprünglichen Einstellungen zurückgesetzt werden, nachdem Sie die Gruppenrichtlinie auf den Computer angewendet haben.

### WMI-Problem

MBAM verwendet Methoden der Win32_EncryptableVolume-Klasse zum Verwalten von BitLocker. Wenn dieses Modul nicht registriert oder beschädigt ist, funktioniert der MBAM-Client nicht ordnungsgemäß, und der folgende Ereigniseintrag wird im MBAM-Administrator Ereignisprotokoll angezeigt:

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

Darüber hinaus werden Sie möglicherweise feststellen, dass die Wiederherstellungs-und Hardware Richtlinien nicht mit Fehler Code 0x8007007e angewendet werden. Dies wird in "das angegebene Modul konnte nicht gefunden werden" übersetzt.

Um dieses Problem zu beheben, sollten Sie die **Win32_EncryptableVolume** Klasse mithilfe des folgenden Befehls erneut registrieren:

```cmd
mofcomp c:\Windows\System32\wbem\win32_encryptablevolume.mof
```

## Behandeln von Problemen mit der MBAM-Agent-Kommunikation

Dieser Abschnitt enthält Informationen zur Problembehandlung für die folgenden Probleme, die sich auf die Kommunikation zwischen MBAM-Agents beziehen:

### Falsche MBAM-Dienst-URL

Wenn der Wert des MBAM-Kompatibilitäts Status Diensts oder des Wiederherstellungs-und Hardware Diensts falsch ist, wird im MBAM-Administrator Ereignisprotokoll auf dem Clientcomputer ein Ereigniseintrag angezeigt, der wie folgt aussieht:

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
**HKEY_LOCAL_MACHINE \software\policies\microsoft\fve\mdopbitlockermanagement**

Standardmäßig weist die URL für KeyRecoveryServiceEndPoint (MBAM-Wiederherstellungs-und Hardware Dienstendpunkt) das folgende Format auf: <br />
**http:// \<servername\> : \<port\> /MBAMRecoveryAndHardwareService/CoreService.svc**

Standardmäßig weist die URL für StatusReportingServiceEndpoint (MBAM Status Reporting Service Endpoint) das folgende Format auf:<br />
**http:// \<servername\> : \<port\> /MBAMComplianceStatusService/StatusReportingService.svc**

> [!Note]
> Die URL darf keine Leerzeichen enthalten.

Wenn die Dienst-URL falsch ist, sollten Sie die Dienst-URL in der folgenden Gruppenrichtlinieneinstellung korrigieren:

**Computer Konfiguration**  >  **Richtlinien**  >  **Administrative Vorlagen**  >  **Windows-Komponenten**  >  **MDOP MBAM (BitLocker-Verwaltung)**  >  **Client Verwaltung**  >  **Konfigurieren von MBAM-Diensten**

### Verbindungsproblem mit Auswirkungen auf den MBAM-Verwaltungsserver

Der MBAM-Agent kann keine Aktualisierungen an der Datenbank Posten, wenn Verbindungsprobleme zwischen dem Client-Agent und dem MBAM-Verwaltungsserver bestehen. In diesem Fall werden Verbindungsfehler Einträge im MBAM-Administrator Ereignisprotokoll auf dem Clientcomputer festgestellt:

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

Grundlegende Überprüfungen:

* Überprüfen Sie die grundlegende Konnektivität, indem Sie den MBAM-Verwaltungsserver nach Name und IP-Adresse anpingen. Überprüfen Sie, ob Sie über Telnet oder PortQry eine Verbindung mit der MBAM-Verwaltungswebsite oder dem Dienst Port herstellen können.

* Überprüfen Sie, ob der IIS-Dienst auf dem MBAM-Verwaltungs-und-Überwachungsserver ausgeführt wird und dass der MBAM-Webdienst denselben Port überwacht, der auf dem MBAM-Clientcomputer konfiguriert ist ( `netstat –ano | find "portnumber"` ).

* Überprüfen Sie, ob die für die MBAM-Website konfigurierte Portnummer IIS-Manager (inetmgr) verwendet. Stellen Sie sicher, dass die Portnummer mit der Portnummer übereinstimmt, auf die der Client lauscht. Stellen Sie sicher, dass die Portnummer nicht von einer anderen Anwendung freigegeben wird. Beispielsweise sollte eine andere Anwendung auf dem Server nicht denselben Port verwenden.

* Wenn eine Firewall vorhanden ist, stellen Sie sicher, dass der Port in der Firewall oder dem Proxy Server geöffnet ist.

* Wenn die Kommunikation zwischen Client und Server sicher ist, stellen Sie sicher, dass Sie ein gültiges SSL-Zertifikat verwenden.

* Überprüfen Sie die Netzwerkkonnektivität zwischen dem Webserver und dem Datenbankserver, an den die Daten zum Einfügen gesendet werden. Sie können die Datenbankkonnektivität vom Webserver auf den Datenbankserver überprüfen, indem Sie den ODBC-Datenquellen Administrator verwenden. Detaillierte Informationen zur Problembehandlung der SQL Server-Verbindung finden Sie unter Problem [Behandlung beim Herstellen einer Verbindung mit dem SQL Server-Datenbankmodul](https://social.technet.microsoft.com/wiki/contents/articles/2102.how-to-troubleshoot-connecting-to-the-sql-server-database-engine.aspx).

#### Problembehandlung des Verbindungsproblems

Stellen Sie sicher, dass die auf dem Client konfigurierte Dienst-URL richtig ist. Kopieren Sie den Wert der URL für KeyRecoveryServiceEndPoint (**HKEY_LOCAL_MACHINE \software\policies\microsoft\fve\mdopbitlockermanagement**) aus der Registrierung, und öffnen Sie Sie in Internet Explorer.

Kopieren Sie ebenfalls den Wert der URL für StatusReportingServiceEndpoint (**HKEY_LOCAL_MACHINE \software\policies\microsoft\fve\mdopbitlockermanagement**), und öffnen Sie Sie in Internet Explorer.

> [!Note]
> Wenn Sie nicht von dem Clientcomputer zur URL navigieren können, sollten Sie die grundlegende Netzwerkkonnektivität vom Client zu dem Server testen, auf dem IIS ausgeführt wird. Siehe die Punkte 1, 2, 3 und 4 im vorherigen Abschnitt.

Überprüfen Sie darüber hinaus die Anwendungsprotokolle auf dem Administrations-und Überwachungsserver auf Fehler.

Sie können eine gleichzeitige Netzwerkablaufverfolgung zwischen dem Client und dem Server vornehmen und die Ablaufverfolgung überprüfen, um die Ursache für einen Verbindungsfehler zwischen dem Client-Agent und dem MBAM-Verwaltungsserver zu ermitteln.

> [!Note]
> Wenn Sie auf dem Clientcomputer zu den Dienst-URLs navigieren können und Verbindungsfehler Einträge in den MBAM-Administrator Ereignisprotokollen vorhanden sind, kann dies auf einen Verbindungsfehler zwischen dem Verwaltungsserver und dem Datenbankserver zurückzuführen sein.

Wenn Sie beide Dienst-URLs erfolgreich durchsuchen können und die Konnektivität zwischen dem Client und dem ausgeführten Server besteht, funktioniert IIS. Es gibt jedoch möglicherweise ein Problem bei der Kommunikation zwischen dem Server, auf dem IIS und dem Datenbankserver ausgeführt wird.

Möglicherweise können die MBAM-Dienste keine Verbindung mit dem Datenbankserver herstellen, weil ein Netzwerkproblem auftritt oder eine falsche Datenbankverbindungszeichenfolge festgelegt wurde. Überprüfen Sie die Anwendungsprotokolle auf dem Verwaltungs-und Überwachungsserver. Möglicherweise werden Fehlereinträge oder Warnungen aus Quell ASP.NET 2.0.50727.0 angezeigt, die dem folgenden Protokolleintrag ähneln:

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

#### Mögliche Ursachen

##### Ursache 1

Der Administrator hat während der Installation von Administrations-und Monitoring Server-Komponenten möglicherweise einen ungültigen Namen/Datenbanknamen für die Datenbankinstanz angegeben.

Sie können die Datenbankverbindungszeichenfolgen mithilfe der IIS-Verwaltungskonsole überprüfen und korrigieren. Öffnen Sie dazu den IIS-Manager, und navigieren Sie zu Microsoft BitLocker-Verwaltung und-Überwachung. Führen Sie für jeden Dienst, der auf der linken Seite aufgeführt ist, die folgenden Schritte aus, um die Datenbankverbindungszeichenfolgen zu ändern:

1. Doppelklicken Sie in der **Ansicht Features**auf **Verbindungszeichenfolgen**.

2. Wählen Sie auf der Seite **Verbindungszeichenfolgen** die Verbindungszeichenfolge aus, die Sie ändern möchten.

3. Wählen Sie im Bereich **Aktionen** die Option **Bearbeiten**aus.

4. Ändern Sie im Dialogfeld **Verbindungszeichenfolge bearbeiten** die Eigenschaften, die Sie ändern möchten, und wählen Sie dann **OK**aus.

##### Ursache 2

SQL Server-Port, der in der Firewall blockiert ist. Überprüfen Sie die Portnummer, für die SQL Server für die Überwachung konfiguriert ist, und stellen Sie sicher, dass der Port in der Firewall zwischen dem Verwaltungsserver und dem Datenbankserver geöffnet ist.

##### Ursache 3

Falsche SQL Server-TCP/IP-Bindungen. Überprüfen Sie die SQL-TCP/IP-Bindungen im SQL Server-Konfigurations-Manager auf dem Datenbankserver. MBAM erfordert, dass die Protokolle TCP/IP und Named Pipes für die Verbindung mit der Datenbank aktiviert sind.

##### Ursache 4

Das NT-AUTHORITY\NETWORK-Dienstkonto oder das Computerkonto des MBAM-Verwaltungsservers verfügen nicht über die erforderlichen Berechtigungen zum Herstellen einer Verbindung mit der SQL-Datenbank.

Während der Installation von Datenbankkomponenten auf dem Datenbankserver erstellt das Installationsprogramm zwei lokale Gruppen: MBAM Compliance Auditing DB Access und MBAM Recovery and Hardware DB Access.

Das NT-AUTHORITY\NETWORK-Dienstkonto, das Computerkonto des MBAM-Verwaltungsservers und der Benutzer, der die Datenbankkomponenten installiert, werden diesen Gruppen automatisch hinzugefügt.

Diesen Gruppen werden während der Installation die erforderlichen Berechtigungen für die Datenbank gewährt. Alle Benutzer, die Teil dieser Gruppe sind, erhalten automatisch die erforderlichen Berechtigungen für die Datenbank.

Der Webdienst kann aufgrund eines Berechtigungsproblems keine Verbindung mit dem Datenbankserver herstellen, wenn mindestens eine der folgenden Bedingungen zutrifft:

* Die zuvor erwähnten Gruppen werden aus den lokalen Gruppen auf dem Datenbankserver entfernt.

* Das NT-AUTHORITY\NETWORK-Dienstkonto und das Computerkonto des MBAM-Verwaltungsservers sind keine Mitglieder dieser Gruppen.

* Diese Gruppen verfügen nicht über die erforderlichen Berechtigungen für die Datenbank.

In den Anwendungsprotokollen auf dem MBAM-Verwaltungs-und-Überwachungsserver werden Sie auf berechtigungsbezogene Fehler hinweisen, wenn eine der vorherigen Bedingungen erfüllt ist. In diesem Fall sollten Sie das NT-AUTHORITY\NETWORK-Dienstkonto und das Computerkonto des MBAM-Verwaltungsservers manuell hinzufügen und ihm eine serverweite öffentliche Rolle auf dem SQL-Datenbankserver gewähren, der SQL Server Management Studio ( https://msdn.microsoft.com/library/aa337562.aspx) .

#### Überprüfen der Webdienstprotokolle

Wenn in den Anwendungsprotokollen auf dem MBAM-Verwaltungsserver keine Ereignisse protokolliert werden, sollten Sie die Webdienstprotokolle (. SVCLOG) des MBAM-Webdiensts überprüfen, der auf dem MBAM-Verwaltungs-und-Überwachungsserver gehostet wird. Sie müssen das Tool für die Dienstablauf Verfolgungs Anzeige (SvcTraceViewer.exe) verwenden https://msdn.microsoft.com/library/ms732023.aspx , um die Protokolldatei anzuzeigen.

Sie sollten in erster Linie die Dienstablauf Verfolgungsprotokolle von RecoveryandHardwareService und ComplianceStatusService untersuchen. Standardmäßig befinden sich Webdienstprotokolle im C:\inetpub\Microsoft BitLocker-Verwaltungs Solution\Logs-Ordner. Dort schreibt jeder Dienst seine SVCLOG-Datei unter seinen eigenen Ordner.

Überprüfen Sie die Aktivität im Dienstablauf Verfolgungsprotokoll auf Fehler-oder Warnungs Einträge. Fehlereinträge sind standardmäßig rot hervorgehoben. Wählen Sie im rechten Bereich des Ablaufverfolgungs-Viewers die Fehlerbeschreibung aus, um detaillierte Informationen zum Fehlereintrag anzuzeigen. Im folgenden wird ein Beispiel für einen Fehlereintrag aus dem Ablaufverfolgungsprotokoll angezeigt:

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

## Erneute Installation oder Neukonfiguration der MBAM-Infrastruktur

Um die MBAM-Infrastruktur erneut zu installieren oder neu zu konfigurieren, müssen Sie die folgenden Punkte kennen:

* Anwendungs Pool Konto

* MBAM-Gruppen (Helpdesk, erweitert, Gruppe "Berichtsbenutzer")

* MBAM-Berichts-URL

* SQL Server-Name und Datenbanknamen

* MBAM ReadWrite-und ReadOnly-Konten

### Anwendungs Pool Konto

Um das Anwendungs Pool Konto zu finden, melden Sie sich beim MBAM-Webserver an, öffnen Sie **Internet Informationsdienste (IIS)-Manager**, und wählen Sie dann **Anwendungs Pools**aus:

![Anwendungspools](images/troubleshooting-MBAM-installation-1.png)

Der Dienstprinzipal Name (SPN) muss in diesem Konto eingestellt sein. Diese Einstellung ist für die Funktionalität von MBAM sehr wichtig.

### MBAM-Gruppen (Helpdesk, erweitert, Gruppe "Berichtsbenutzer" und URL für Berichte)

![MBAM-Gruppen](images/troubleshooting-MBAM-installation-2.png)

Hier finden Sie Informationen wie die Helpdesk-Gruppe, die erweiterte Helpdesk-Gruppe, die Berichtsbenutzer Gruppe und die MBAM-Berichts-URL. Die URL des MBAM-Berichts muss im MBAM-Setup bereitgestellt werden und sollte wie folgt gelesen werden: http (s)://servername/reportserver.

### SQL Server-Namen und Daten Bank Namen (DB)

Um die SQL Server-Namen und-Instanzen zu finden, die das MBAM DBS hosten, melden Sie sich beim MBAM Web (IIS)-Server an, und navigieren Sie zum Registrierungsunterschlüssel Folowing:

**HKEY_LOCAL_MACHINE \software\microsoft\mbam Server\Web**

![Regedit](images/troubleshooting-MBAM-installation-3.png)

Die hervorgehobenen Abschnitte sind Verbindungszeichenfolgen. Diese sollten den SQL Server-Namen, Datenbanknamen und Instanzen (sofern benannt) aufweisen.

### MBAM ReadWrite-und ReadOnly-Konten

Diese Informationen befinden sich in der SQL Server-Datenbank, für die der Name bereits vom Webserver gefunden wurde.

#### ReadWrite-Konto

1. Melden Sie sich bei SQL Management Studio an.

2. Klicken Sie mit der rechten Maustaste auf **MBAM-Wiederherstellung und-Hardware**, wählen Sie **Eigenschaften**aus, und wählen Sie dann **Berechtigungen**aus.

Der Name des Lab-Kontos lautet beispielsweise **MBAMWrite**. Der Anwendungs Pool und die ReadWrite-Konten sind so eingestellt, dass Sie identisch sind.

![SQL DB](images/troubleshooting-MBAM-installation-4.png)

![DB-Eigenschaften](images/troubleshooting-MBAM-installation-5.png)

Navigieren Sie zu **Sicherheit** , und **melden** Sie sich dann in SQL Management Studio an. Navigieren Sie zu dem Konto, das im vorherigen Screenshot angezeigt wurde.

![SQL-Sicherheit](images/troubleshooting-MBAM-installation-6.png)

Klicken Sie mit der rechten Maustaste auf die Konten, wechseln Sie zu **Eigenschaften Benutzerzuordnung**, und suchen Sie nach der MBAM-Wiederherstellungs-und-Hardware Datenbank:

![Benutzerzuordnung](images/troubleshooting-MBAM-installation-7.png)

#### ReadOnly-Konto

Öffnen Sie den SQL Server Reporting Services-Konfigurations-Manager auf dem SSRS-Server. Wählen Sie **Berichts-Manager-URL**aus, und Durchsuchen Sie dann die **URLs**:

![Berichts-Manager](images/troubleshooting-MBAM-installation-8.png)

Wählen Sie **Microsoft BitLocker-Verwaltung und-Überwachung**aus:

![BitLocker-Verwaltung und-Überwachung](images/troubleshooting-MBAM-installation-9.png)

Wählen Sie **MaltaDatasource**:

![DBS](images/troubleshooting-MBAM-installation-10.png)

![MaltaDatasource](images/troubleshooting-MBAM-installation-11.png)

MaltaDataSource sollte über den Namen des ReadOnly-Kontos verfügen und in MBAM-Setup verwendet werden.

## Verweis

Weitere Informationen finden Sie in den folgenden Artikeln:

[Bereitstellen von MBAM 2,5 in einer eigenständigen Konfiguration](https://support.microsoft.com/help/3046555)

[Microsoft BitLocker Administration and Monitoring 2.5](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/)
