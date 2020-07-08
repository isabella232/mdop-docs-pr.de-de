---
title: Versionshinweise zu Microsoft Application Virtualization Management System
description: Versionshinweise zu Microsoft Application Virtualization Management System
author: dansimp
ms.assetid: e1a4d5ee-53c7-4b48-814c-a34ce0e698dc
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: c34abab9a49bd69f760a9b531d0950cc581253c1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806596"
---
# Versionshinweise zu Microsoft Application Virtualization Management System


Drücken Sie STRG + F, um diese Versionshinweise zu durchsuchen.

**Wichtig**  Lesen Sie diese Versionshinweise gründlich, bevor Sie das Application Virtualization Management System installieren. Diese Anmerkungen zu dieser Version enthalten Informationen, die Sie benötigen, um das Application Virtualization Management System erfolgreich zu installieren. Dieses Dokument enthält Informationen, die in der Produktdokumentation nicht zur Verfügung stehen. Wenn zwischen diesen Anmerkungen zur Version und anderen Application Virtualization Management System-Dokumentationen Diskrepanzen bestehen, sollte die neueste Änderung als autorisierend angesehen werden. Diese Versionshinweise ersetzen die Inhalte, die in diesem Produkt enthalten sind.

 

Aktualisierte Informationen zu bekannten Problemen finden Sie in der Microsoft TechNet-Bibliothek unter <https://go.microsoft.com/fwlink/?LinkId=122918> .

## Informationen zu Microsoft Application Virtualization 4,5 Kumulatives Update 1


Diese Anmerkungen zur Version wurden aktualisiert, um die mit Microsoft Application Virtualization 4.5 kumulierten Update1 (app-v 4.5 CU1) eingeführten Änderungen zu berücksichtigen, die die neuesten Updates für Application Virtualization (app-v) 4.5 bereitstellen. Dieses kumulative Update enthält die folgenden Änderungen:

-   Unterstützung für Windows7 Beta und Windows Server2008R2 Beta: App-v 4.5 CU1 behebt Kompatibilitätsprobleme mit Windows7 Beta und Windows Server2008R2 Beta. Unterstützung wird für das Blockieren von Problemen bereitgestellt, die verhindern, dass APP-v 4.5-CU1 in einer Testumgebung auf Pre-RTM-Versionen von Windows7 ausgeführt werden. Dadurch wird sichergestellt, dass Ihre virtuellen Anwendungen in einer Testumgebung erfolgreich ausgeführt werden können, wenn Kompatibilität zwischen App-v 4.5-Client und Windows7 Beta erforderlich ist.

    **Wichtig**  Das Ausführen von App-v 4.5-CU1 unter einer beliebigen Version von Windows7 oder Windows Server2008R2 in einer aktiven Betriebsumgebung wird nicht unterstützt.

     

-   Verbesserte Unterstützung für die Sequenzierung von .NET Framework: App-v 4.5 CU1 behebt frühere Probleme mit der Sequenzierung von .NET Framework 3.5 und früher unter WindowsXP (SP2 oder höher). Weitere Informationen zu den neuen Funktionen finden Sie im TechNet-Artikel unter <https://go.microsoft.com/fwlink/?LinkId=123412> .

-   Kunden Feedback und Hotfix-Rollup: App-v 4.5 CU1 enthält auch ein Rollup von Korrekturen, um Probleme zu beheben, die seit der Version App-v 4.5 RTM gefunden wurden. Dies umfasst eine Kombination aus bekannten Problemen und Kundenfeedback unserer internen Teams, Partner und Kunden, die APP-v 4.5 verwenden. Eine vollständige Liste der enthaltenen Updates finden Sie im KB-Artikel unter <https://go.microsoft.com/fwlink/?LinkId=141258> .

## Informationen zur Produktdokumentation


Eine umfassende Dokumentation für Application Virtualization (app-v) finden Sie auf der Microsoft TechNet-Anwendung im Application Virtualization (app-v) TechCenter unter <https://go.microsoft.com/fwlink/?LinkId=122939> . Die TechNet-Dokumentation enthält die Online Hilfe für Application Virtualization Sequencer, den Application Virtualization-Client und den Application Virtualization Server. Darüber hinaus enthält es das Leitfaden zur Planung und Bereitstellung von Application Virtualization sowie das Application Virtualization Operations Guide.

## Schutz vor Sicherheitsrisiken und Viren


Zum Schutz vor Sicherheitsrisiken und Viren ist es wichtig, die neuesten verfügbaren Sicherheitsupdates für jede neue Software zu installieren, die installiert wird. Weitere Informationen finden Sie auf der Microsoft-Sicherheitswebsite unter <https://go.microsoft.com/fwlink/?LinkId=3482> .

## Bereitstellen von Feedback


Sie können über ein Community-Forum im Microsoft Application Virtualization TechCenter () Feedback bereitstellen, Vorschläge machen oder ein Problem mit dem Microsoft Application Virtualization (App-V)-Verwaltungs System melden <https://go.microsoft.com/fwlink/?LinkId=122917> .

Sie können auch Ihr Feedback zur Dokumentation direkt an das App-V-Dokumentationsteam weitergeben. Senden Sie Ihr Feedback zur Dokumentation an appvdocs@microsoft.com.

## Bekannte Probleme mit Application Virtualization 4.5 CU1


Dieser Abschnitt enthält die aktuellsten Informationen zu Problemen mit Microsoft Application Virtualization (App-V) 4.5 CU1. Diese Probleme werden in der Produktdokumentation nicht angezeigt und können in einigen Fällen der vorhandenen Produktdokumentation widersprechen. Wenn möglich, werden diese Probleme in späteren Versionen behoben.

### Leitfaden zum Installieren oder Aktualisieren von Clients auf App-v 4.5-CU1 mithilfe von setup.msi

Wenn Sie Ihre APP-v-Clients mithilfe von setup.msi auf App-v 4.5-CU1 installieren oder aktualisieren, werden die Voraussetzungen nicht automatisch installiert.

WORKAROUNDYou müssen die Voraussetzungen manuell installieren, bevor Sie den App-V-Client auf 4.5 CU1 installieren oder aktualisieren. Detaillierte Anweisungen zum Installieren der Voraussetzungen und des App-V-Clients finden Sie unter <https://go.microsoft.com/fwlink/?LinkId=144106> .

Wenn dies abgeschlossen ist, installieren Sie den App-v 4.5-CU1-Client mithilfe von setup.msi mit erhöhten Rechten. Diese Datei ist auf dem App-v 4.5 CU1-Veröffentlichungsmedium im Ordner "Installers\\Client" verfügbar.

Verwenden Sie beim Installieren der Fehlerberichterstattung für Microsoft-Anwendungen den folgenden Befehl, wenn Sie auf den App-v 4.5 CU1-Desktop Client installieren oder darauf aktualisieren:

    msiexec /i dw20shared.msi APPGUID={FE495DBC-6D42-4698-B61F-86E655E0796D}  allusers=1 reboot=suppress REINSTALL=all REINSTALLMODE=vomus

Wenn Sie aber auf den App-V 4,5 CU1-Terminaldiensteclient installieren oder ein Upgrade ausführen, verwenden Sie den folgenden Befehl:

    msiexec /i dw20shared.msi APPGUID={8A97C241-D92A-47DC-B360-E716C1AAA929} allusers=1 reboot=suppress REINSTALL=all REINSTALLMODE=vomus

**Hinweis**  Der APPGUID-Parameter verweist auf den Produktcode des App-V-Clients, auf den Sie installieren oder aktualisieren. Der Produktcode ist für jede setup.msi eindeutig. Sie können den Orca-Datenbankeditor oder ein ähnliches Tool verwenden, um Windows Installer-Dateien zu überprüfen und den Produktcode zu ermitteln. Dieser Schritt ist für alle Installationen oder Upgrades auf App-v 4.5 CU1 erforderlich.

 

### <a href="" id="some-applications-might-fail-to-install-during-the-monitoring-phase-when-sequencing-on-windows-7-beta--"></a>Einige Anwendungen können während der Überwachungsphase bei der Sequenzierung auf Windows7 Beta nicht installiert werden

Bei der Sequenzierung auf Windows7 Beta oder auf einem Computer mit Windows Installer 5.0 kann es vorkommen, dass einige Anwendungen während der Überwachungsphase nicht installiert werden.

WORKAROUNDYou muss der Gruppe "jeder" die Berechtigung "Vollzugriff" für den folgenden Registrierungsschlüssel manuell erteilen:

    HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\SystemGuard

**Wichtig**  Sie müssen die Schaltfläche " **erweitert** " verwenden, um die Option "vererbbare Berechtigungen des übergeordneten Objekts einbeziehen" einzurichten.

 

### Pakete können bei der Sequenzierung auf Windows7 Beta nicht gespeichert werden

Bei der Sequenzierung auf Windows7 Beta können Sie das sequenzierte Paket möglicherweise aufgrund einer Zugriffsverletzung nicht speichern.

Problemumgehungen, die im Abschnitt bewährte Methoden des Microsoft Application Virtualization 4.5-Sequenzierungs Leitfadens angegeben <https://go.microsoft.com/fwlink/?LinkId=144108> sind (siehe), müssen Sie die folgenden Softwareprogramme Herunterfahren und deaktivieren, bevor Sie mit der Sequenzierung beginnen:

-   Windows Defender

-   Antivirensoftware

-   Software für die Datenträgerdefragmentierung

-   Windows Search

-   Eine beliebige geöffnete Windows-Explorer-Sitzung

Wenn Sie Microsoft Update auf der Sequenzierungs Station zum Aufzeichnen von Updates während des Paket Aktualisierungsprozesses installiert haben, müssen Sie außerdem "C:\\Windows\\SoftwareDistribution" als VFS-Ausschluss hinzufügen, bevor Sie mit der Sequenzierung beginnen.

### Verbessern der Leistung bei der Sequenzierung von .NET Framework

Bei der Sequenzierung von .NET Framework kann es zu einer reduzierten Systemleistung kommen, da der Microsoft .NET Framework-NGen-Dienst versucht, Assemblys als Hintergrundaufgabe vorkompilieren.

WORKAROUNDWhen-Sequenzierung .NET Framework deaktivieren Sie nach Abschluss der Überwachungsphase den Microsoft .NET Framework-NGen-Dienst (mscorsvw.exe). Sie müssen die Registerkarte **Virtuelle Dienste** im Sequencer verwenden und den Starttyp in deaktiviert ändern.

### Interoperabilitätsprobleme mit der Windows7-Taskleiste

Wenn Sie den Application Virtualization-Client auf Windows7 ausführen, reduziert die Windows7-Taskleiste nicht mehrere Instanzen einer virtuellen Anwendung in einer einzigen Taskleistenschaltfläche. Darüber hinaus werden Sprunglisten nicht angezeigt, wenn Sie mit der rechten Maustaste auf eine Taskleistenschaltfläche einer virtuellen Anwendung klicken, es sei denn, die Anwendung wurde an die Windows7-Taskleiste angeheftet.

### Wenn Sie den Microsoft Application Virtualization-Client deinstallieren, werden die Benutzereinstellungen gelöscht, die dem Benutzer zugeordnet sind, der die Deinstallation ausführt.

Wenn Sie den Microsoft Application Virtualization-Client deinstallieren, entfernt der Windows Installer die Einstellungen für Application Virtualization aus dem Profil des aktuellen Benutzers. Wenn Ihr Computer Server gespeicherte Profile verwendet, verwenden Sie Ihr privates Netzwerkkonto nicht, um den Client zu deinstallieren, da dadurch die Einstellungen für Ihre virtuellen Anwendungen auf allen ihren Computern entfernt werden.

WORKAROUNDYou sollte die App-V-Client-Deinstallation mit einem Administratorkonto durchführen, das nicht für die Ausführung virtueller Anwendungen verwendet wird.

### Bearbeitungen, die auf dem virtuellen Dateisystem und den Registerkarten der virtuellen Registrierung vorgenommen wurden, müssen beim Ausführen des Sequenz-Assistenten gespeichert werden.

Wenn Sie ein Paket öffnen, um ein Upgrade durchzuführen oder den Sequenz-Assistenten bereits mit einem neuen Paket auszuführen, und Sie Änderungen am Paket auf den Registerkarten virtuelles Dateisystem oder virtuelle Registrierung vornehmen, werden diese Änderungen nicht automatisch gespeichert.

WORKAROUNDSave Sie die Änderungen, bevor Sie den Assistenten erneut ausführen, um sicherzustellen, dass Sie in der virtuellen Umgebung des Assistenten wiedergegeben werden.

### Befehlszeilen-Sequencer muss über eine Eingabeaufforderung mit erhöhten Rechten ausgeführt werden

Wenn Sie den Befehlszeilen-Sequenzer verwenden, wird keine Eingabeaufforderung zur Erhöhung angezeigt.

WORKAROUNDRun Sie den Befehlszeilen-Sequencer mithilfe einer Eingabeaufforderung mit erhöhten Rechten.

### Konfiguration der Server Verwaltungskonsole in verteilten Umgebungen

Wenn Sie Verwaltungskomponenten auf anderen Systemen als dem primären Application Virtualization Publishing-und Streamingserver installieren müssen, unterstützt die Server Installation die Installation unserer Verwaltungskonsole und des Webdiensts auf separaten Servern vom primären Application Virtualization-Server, wenn Sie ordnungsgemäß konfiguriert sind.

Um die Verwaltungskomponenten auf mehreren Servern zu verteilen, muss die Kerberos-Delegierung auf dem Server aktiviert sein, auf dem der Webdienst installiert ist.

### Kurze Pfadvariablennamen in OSD-Dateien können zu Fehlern führen

Wenn Sie Fehler 450478-1F702339-0000010B "der Verzeichnisname ist ungültig" beim Starten einer virtuellen Anwendung auf dem Client erhalten, ist es möglich, dass die Variable im OSD-Menü falsch eingestellt ist. Dies kann geschehen, wenn das Installationsprogramm der Anwendung einen kurzen Pfadnamen während der Sequenzierung festlegt.

WORKAROUNDRemove Sie die nachfolgende Tilde aus einer beliebigen CSIDL-Variablen, die in der OSD-Datei vorhanden ist.

### <a href="" id="correct-syntax-for-decodepath-parameter-for-command-line-sequencer-"></a>Korrekte Syntax für den DECODEPATH-Parameter für Befehlszeilen-Sequenzer

Wenn Sie im Befehlszeilen-Sequencer ein Paket für das Upgrade öffnen und es in den Stamm des Q-Laufwerks decodieren, sollte die Syntax für den *DECODEPATH* -Parameter keinen nachfolgenden Schrägstrich aufweisen.

WORKAROUNDYou kann **f:** anstelle von **Q:\\** verwenden (wobei das nachfolgende "\ \"-Zeichen ausgelassen wird).

### <a href="" id="when-upgrading-4-2-packages--you-encounter-problems-caused-by-windows-installer-files-in-the-virtual-file-system-"></a>Wenn Sie 4.2-Pakete aktualisieren, treten Probleme auf, die von Windows Installer-Dateien im virtuellen Datei System verursacht werden.

Beim Upgrade eines Pakets von 4.2 können Probleme im Zusammenhang mit einer Nichtübereinstimmung von Windows Installer-Systemdateien auftreten, die standardmäßig in 4.2 enthalten sind, und die Windows Installer-Bibliotheken, die lokal auf der Sequenzierungs Arbeitsstation installiert sind. Die folgenden Dateien befinden sich in CSIDL \ _SYSTEM \ \:

cabinet.dll

msi.dll

msiexec.exe

msihnd.dll

msimsg.dlll

WORKAROUNDDelete Sie alle vorhergehenden Dateien aus dem Paket. Löschen Sie die Zuordnungen auf der Registerkarte **VFS** sowie die eigentlichen Dateien im CSIDL \ _SYSTEM-Ordner in Ihrem Decode-Pfad.

### <a href="" id="on-windows-xp--client-install-logging-is-not-enabled-by-default-"></a>Unter WindowsXP ist die Client Installationsprotokollierung standardmäßig nicht aktiviert.

Wenn Sie den Client installieren, um sicherzustellen, dass etwaige Installationsfehler zu Problembehandlungszwecken erfasst werden, sollten Sie die Protokollierung über die Befehlszeile aktivieren.

WORKAROUNDAdd Sie den Parameter */l\ * VX! log.txt* an die Befehlszeile, wie im folgenden Beispiel gezeigt:

setup.exe/s/v "/qn/l\ * VX! log.txt "

msiexec.exe/i setup.msi/Qn/l\ * VX! log.txt

Alternativ können Sie den Registrierungsschlüssel auf den folgenden Wert setzen:

\ [HKEY \ _LOCAL \ _MACHINE \\software\\policies\\microsoft\\windows\\installer\] "Logging" = "voicewarmupx!"

### Damit die Kerberos-Authentifizierung funktioniert, müssen Dienstprinzipalnamen (Service Principal Names, SPNs) für IIS registriert sein.

Wenn Sie IIS 6.0 oder 7.0 für Symbol-oder OSD-Dateiabruf und-Streaming von Paketen verwenden und die Kerberos-Authentifizierung aktiviert werden soll, müssen die SPNs wie folgt registriert sein:

-   Führen Sie auf dem IIS-Server die folgenden Befehle mit dem SETSPN.EXE Resource Kit-Tool aus. Der vollqualifizierte Domänenname (Fully Qualified Domain Name, FQDN) des Servers muss verwendet werden.

    Setspn-r SOFTGRID/ &lt; Server-FQDN&gt;

    Setspn-r http/ &lt; Server-FQDN&gt;

Weitere Informationen finden Sie unter <https://go.microsoft.com/fwlink/?LinkId=131407>.

### Bei einem Upgrade von RC können die Standardberechtigungen für Clientprotokolle nicht für Benutzer ohne Administratorrechte für den Zugriff auf die Protokolle zur Fehlerbehebung und Unterstützung zugelassen werden.

Die Standardberechtigungen für Clientprotokolle für den Anwendungs-VirtualizationRC-Client haben keinen Zugriff auf Protokolldateien durch nicht-Administratoren ermöglicht, und manuelle Änderungen an diesen Protokoll Berechtigungen wurden wiederhergestellt, wenn Clients neu gestartet wurden. Dies wurde in der RTM-Version für neue Clientinstallationen korrigiert, doch beim Upgrade von RC werden die benutzerdefinierten Berechtigungen für vorhandene Protokolldateien nicht zurückgesetzt. Wenn jedoch neue Protokolle erstellt oder nach einem Protokoll zurückgesetzt werden, verfügen die Dateien über die neuen Standardberechtigungen.

WORKAROUNDAfter Sie das Upgrade, setzen Sie vorhandene Clientprotokolle zurück, oder ändern Sie Ihre Berechtigungen manuell.

### .Net-Kompatibilitätsänderungen

Microsoft Application Virtualization kumulativer Update1 unterstützt die Sequenzierung von .NET Framework unter WindowsXP (SP2 oder höher). Sequenz Routinen für .NET-Anwendungen, die für SoftGrid 4.2 geschrieben wurden, müssen möglicherweise aktualisiert werden, wenn Sie mit dem App-v 4.5-Sequenzer verwendet werden. Details und Problemumgehungen finden Sie im Knowledge Base-Artikel unter <https://go.microsoft.com/fwlink/?LinkId=123412> .

### <a href="" id="after-client-upgrade-from-app-v-4-2--some-applications-are-not-shown-"></a>Nach dem Client Upgrade von App-v 4.2 werden einige Anwendungen nicht angezeigt

Überprüfen Sie den folgenden Fehler im Protokoll: "der Application Virtualization-Client konnte die OSD-Datei nicht analysieren". Der Microsoft Application Virtualization 4.5-Client filtert Anwendungen mit einer OSD-Datei, die eine leere OS &lt; -Kategorie (OS &gt; &lt; /OS &gt; ) enthält.

WORKAROUNDDelete Sie das leere Betriebssystem-Tag aus der OSD-Datei.

### Der App-V-Server erfordert Ausnahmen in der Firewall für bestimmte Prozesse.

Damit der Serveranwendungen ordnungsgemäß streamen kann, müssen die Hauptprozesse des Servers, einschließlich des Verteilers, über die Firewall zugreifen.

Problemumgehung: Ausnahmen in der Server Firewall für die folgenden Prozesse: sghwsvr.exe und sghwdsptr.exe. Dies gilt für den App-v-Verwaltungsserver und den App-v-Streamingserver.

### Sequenzierung von Paketen, die neue Visual Basic-Runtimes erfordern, schlägt möglicherweise fehl

Wenn Sie ein Paket sequenzieren, das eine neuere Version einer Visual Basic-Runtime (VB) auf einem System verwendet, auf dem eine ältere Version von VBruntime installiert ist, wird möglicherweise ein Absturz oder ein anderes unerwartetes Verhalten angezeigt, wenn Sie versuchen, Ihr Paket zu verwenden. Wenn Sie beispielsweise versuchen, Microsoft Money2007 zu sequenzieren, das die Version 6.00.9782 des VBruntime verwendet, auf einem WindowsXP-System mit der Version 6.00.9690 des VBruntime wird möglicherweise ein Absturz im Rechnungs-Designer angezeigt, wenn Sie versuchen, es auf einem anderen WindowsXP-System mit diesem älteren VBruntime auszuführen.

WORKAROUNDAfter Wenn Sie die Anwendung auf dem Sequenzcomputer installieren, während Sie weiterhin überwacht wird, kopieren Sie die richtige (neuere) VBruntime in das Verzeichnis im Paket, aus dem die ausführbare Datei gestartet wird. Dadurch kann die sequenzierte Anwendung die erwartete Version des VBruntime beim Starten ermitteln.

**Wichtig**  Dieses Problem wurde in Microsoft Application Virtualization 4.5 kumulativer Update1 behoben.

 

### Wenn das Server-Installationsprogramm im unbeaufsichtigten Modus ausgeführt wird, überprüft es nicht richtig auf MSXML6

Der App-V-Verwaltungs Server hängt von MSXML6 ab. Wenn Sie das Installationsprogramm allerdings im unbeaufsichtigten Modus ausführen, beispielsweise mit dem Befehl "msiexec-i setup.msi/qn" auf einem System, auf dem MSXML6 noch nicht installiert ist, werden die fehlenden Abhängigkeiten nicht bemerkt und trotzdem nicht installiert. Das häufigste Ergebnis: Wenn Clients versuchen, Veröffentlichungsinformationen vom App-V-Verwaltungs Server zu aktualisieren, werden Fehler angezeigt.

WORKAROUNDVerify Sie, dass MSXML6 auf dem System installiert ist, bevor Sie eine unbeaufsichtigte Installation des App-V-Verwaltungsservers versuchen.

### Fehlercode 000C800 beim Versuch, eine Verbindung mit der Application Virtualization Management Console herzustellen

Ein Application Virtualization-Administrator, der kein lokaler Administrator auf dem Application Virtualization Management Service-Server ist, erhält beim Versuch, eine Verbindung mit der Application Virtualization Management Console herzustellen, eine Fehlermeldung (Fehlercode: 000C800), und der "SftMMC. Log-Eintrag gibt an, dass der Zugriff auf SftMgmt. udl verweigert wird. Um erfolgreich eine Verbindung mit der Application Virtualization Management Console herzustellen, muss ein Application Virtualization-Administrator, der kein lokaler Administrator auf dem Application Virtualization Management Service-Server ist, mindestens über Lese-und Ausführungszugriff auf die SftMgmt. UDL-Datei verfügen.

Die Application Virtualization-Administratoren müssen Lese-und Ausführungsberechtigungen für die SftMgmt. UDL-Datei unter%systemdrive%\\Program c:\\Programme\\Microsoft System Center App virt Management Server\\App virt-Verwaltungsdienst erhalten.

### Befehlszeilenparameter des Client Installationsprogramms werden ignoriert, wenn Sie in Verbindung mit KEEPCURRENTSETTINGS = 1 verwendet werden.

Bei Verwendung in Verbindung mit KEEPCURRENTSETTINGS = 1 werden die folgenden Befehlszeilenparameter des Clientinstallationsprogramms ignoriert: SWICACHESIZE, MINFREESPACEMB, ALLOWINDEPENDENTFILESTREAMING, ApplicationSourceRoot, IconSourceRoot, OSDSourceRoot, SYSTEMEVENTLOGLEVEL, SWIGLOBALDATA, DOTIMEOUTMINUTES, SWIFSDRIVE, AUTOLOADTARGET, AUTOLOADTRIGGERS, SWIUSERDATA und REQUIRESECURECONNECTION.

WORKAROUNDIf Sie Einstellungen, die Sie beibehalten möchten, verwenden Sie KEEPCURRENTSETTINGS = 1, und setzen Sie die anderen Parameter nach der Bereitstellung. Die App-V ADM-Vorlage kann zum Festlegen der folgenden Clienteinstellungen verwendet werden: ApplicationSourceRoot, IconSourceRoot, OSDSourceRoot, AUTOLOADTARGET, AUTOLOADTRIGGERS, DOTIMEOUTMINUTES und ALLOWINDEPENDENTFILESTREAMING. Die ADM-Vorlage finden Sie unter <https://go.microsoft.com/fwlink/?LinkId=121835> .

### Fehler beim Initialisieren virtueller Anwendungen mit Symantec Endpoint Protection

Bei Verwendung von Symantec Endpoint Protection mit aktiviertem Feature für die Anwendungs-und Gerätesteuerung können virtuelle Anwendungen möglicherweise nicht gestartet werden, mit dem Fehler "die Anwendung konnte nicht ordnungsgemäß initialisiert werden (0xc000007b)". Details und Problemumgehungen finden Sie im Knowledge Base-Artikel unter <https://go.microsoft.com/fwlink/?LinkId=125851> .

**Wichtig**  Dieses Problem wurde in Microsoft Application Virtualization 4.5 kumulativer Update1 behoben.

 

## Anmerkungen zu dieser Version Copyright-Informationen


Informationen in diesem Dokument, einschließlich URLs und anderen Internet-Website verweisen, können ohne Vorankündigung geändert werden und dienen nur zu Informationszwecken. Das gesamte Risiko der Nutzung oder der Ergebnisse der Verwendung dieses Dokuments verbleibt beim Nutzer, und Microsoft Corporation übernimmt keine Garantien, weder ausdrücklich noch impliziert. Die hier gezeigten Beispiele für Unternehmen, Organisationen, Produkte, Personen und Ereignisse sind fiktiv. Keine Assoziation mit einem wirklichen Unternehmen, einer Organisation, einem Produkt, einer Person oder einem Ereignis ist beabsichtigt oder sollte abgeleitet werden. Die Einhaltung aller anwendbaren Urheberrechtsgesetze obliegt dem Nutzer. Ohne die Rechte unter dem Urheberrecht zu begrenzen, darf kein Teil dieses Dokuments reproduziert, gespeichert oder in ein Retrievalsystem aufgenommen oder in irgendeiner Form oder auf andere Weise (elektronisch, mechanisch, Fotokopieren, aufzeichnen oder auf andere Weise) oder zu einem beliebigen Zweck ohne die ausdrückliche schriftliche Genehmigung der Microsoft Corporation übertragen werden.

Microsoft hat möglicherweise Patente, Patentanmeldungen, Marken, Urheberrechte oder andere Rechte an geistigem Eigentum, die Inhalte dieses Dokuments abdecken. Sofern nicht ausdrücklich in einem schriftlichen Lizenzvertrag von Microsoft vorgesehen, gibt Ihnen die Einrichtung dieses Dokuments keine Lizenz für diese Patente, Marken, Urheberrechte oder sonstiges geistiges Eigentum.



Microsoft, MS-DOS, Windows, Windows Server, Windows Vista, Active Directory und ActiveSync sind entweder eingetragene Marken oder Marken von MicrosoftCorporation in den USA und/oder anderen Ländern.

Die Namen der Unternehmen und Produkte, die hierin erwähnt werden, können Marken der jeweiligen Besitzer sein.

 

 





