---
title: App-V 4.5 SP2 – Versionshinweise
description: App-V 4.5 SP2 – Versionshinweise
author: dansimp
ms.assetid: 1b3a8a83-4523-4634-9f75-29bc22ca5815
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 35cff3b2a2c110a4d8beba883a4cf9332381ea60
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808072"
---
# App-V 4.5 SP2 – Versionshinweise


Drücken Sie STRG + F, um diese Versionshinweise zu durchsuchen.

**Wichtig**  Lesen Sie diese Versionshinweise gründlich, bevor Sie das Microsoft Application Virtualization Management System installieren. Diese Anmerkungen zu dieser Version enthalten Informationen, die Sie benötigen, um das Application Virtualization Management System erfolgreich zu installieren. Diese Anmerkungen zu dieser Version enthalten Informationen, die in der Produktdokumentation nicht zur Verfügung stehen. Wenn zwischen diesen Anmerkungen zur Version und anderen Application Virtualization Management System-Dokumentationen Diskrepanzen bestehen, sollte die neueste Änderung als autorisierend angesehen werden.

 

Aktualisierte Informationen zu bekannten Problemen finden Sie in der Microsoft TechNet-Bibliothek unter [App-V 4,5 SP2 – Versionshinweise](https://go.microsoft.com/fwlink/?LinkId=184640) ( https://go.microsoft.com/fwlink/?LinkId=184640) .

## Informationen zu Microsoft Application Virtualization 4,5 Service Pack 2


Diese Anmerkungen zur Version wurden aktualisiert, um die Änderungen zu berücksichtigen, die mit Microsoft Application Virtualization (App-V) 4.5 Service Pack2 (SP2) eingeführt wurden. Dieses Service Pack enthält die folgenden Änderungen:

-   Unterstützung für Office 2010: App-v 4.5 SP2 unterstützt jetzt die Virtualisierung von Microsoft Office 2010. Ausführliche Anleitungen für die Sequenzierung von Microsoft Office 2010 mit App-v 4,5 SP2 finden Sie unter [normative Anleitungen für die Sequenzierung von Office 2010 in Microsoft App-v 4,6](https://go.microsoft.com/fwlink/?LinkId=191539) ( https://go.microsoft.com/fwlink/?LinkId=191539) .

-   Unterstützung für die Datenbankspiegelung: App-v 4.5 SP2 unterstützt jetzt die Microsoft SQL Server-Datenbankspiegelung. Weitere Informationen zum Konfigurieren der Datenbankspiegelung in Ihrer APP-v-Umgebung finden Sie unter [Konfigurieren der Microsoft SQL Server-Spiegelungs Unterstützung für App-v](https://go.microsoft.com/fwlink/?LinkId=190880) ( https://go.microsoft.com/fwlink/?LinkId=190880) .

-   Kunden Feedback und Hotfix-Rollup: App-v 4.5 SP2 enthält auch ein Rollup mit Korrekturen zur Behebung von Problemen, die nach der APP-v 4.5 SP1-Version gefunden wurden. Die Updates befassen sich mit einer Kombination aus bekannten Problemen und Kundenfeedback von internen Microsoft-Teams,-Partnern und-Kunden, die APP-v 4.5 verwenden. Eine vollständige Liste der Updates finden Sie im Artikel 980847 in der Microsoft Knowledge Base (KB) unter [Beschreibung von Microsoft Application Virtualization 4,5 Service Pack 2](https://go.microsoft.com/fwlink/?LinkId=191540) ( https://go.microsoft.com/fwlink/?LinkId=191540) .

## Informationen zur Produktdokumentation


Eine umfassende Dokumentation für Application Virtualization (App-V) finden Sie auf der Microsoft TechNet-Website in der [Application Virtualization TechCenter-Bibliothek](https://go.microsoft.com/fwlink/?LinkId=122939) ( https://go.microsoft.com/fwlink/?LinkId=122939) . Die TechNet-Dokumentation umfasst die Online Hilfe für Application Virtualization Sequencer, die Application Virtualization-Clients und den Application Virtualization Server. Darüber hinaus enthält es das Leitfaden zur Planung und Bereitstellung von Application Virtualization sowie das Application Virtualization Operations Guide.

## Schutz vor Sicherheitsrisiken und Viren


Wir empfehlen, dass Sie die neuesten verfügbaren Sicherheitsupdates für jede neue Software installieren, die installiert werden soll, um den Schutz vor Sicherheitsrisiken und Viren zu gewährleisten. Weitere Informationen finden Sie unter [Microsoft-Sicherheit](https://go.microsoft.com/fwlink/?LinkId=3482) ( https://go.microsoft.com/fwlink/?LinkId=3482) .

## Feedback geben


Sie können mit dem Microsoft Application Virtualization (app-v)-Verwaltungs System über das Community-Forum im Application Virtualization TechCenter [App-v Documentation Forum](https://go.microsoft.com/fwlink/?LinkId=122917) ( https://go.microsoft.com/fwlink/?LinkId=122917) .

Sie können Ihr Dokumentations Feedback auch direkt an das App-V-Dokumentationsteam unter senden <appvdocs@microsoft.com> .

## Bekannte Probleme mit Application Virtualization 4.5 SP2


In diesem Abschnitt finden Sie die neuesten Informationen zu Problemen mit Microsoft Application Virtualization (App-V) 4.5 SP2. Diese Probleme werden in der Produktdokumentation nicht angezeigt und können in einigen Fällen der vorhandenen Produktdokumentation widersprechen. Wenn möglich, werden diese Probleme in späteren Versionen der Software behoben.

### Leitfaden zum Installieren der Server-Verwaltungskonsole

Wenn Sie Verwaltungssoftware auf anderen Systemen als dem primären Application Virtualization Publishing and Streaming Server installieren müssen, unterstützt die Server Installation die Installation der Application Virtualization Management Console und des Application Virtualization Management Web Service auf separaten Servern vom primären App-V-Verwaltungsserver. Um die Verwaltungskomponenten auf mehreren Servern zu verteilen, muss die Kerberos-Delegierung auf dem Server aktiviert sein, auf dem der Application Virtualization Web Service installiert ist. Informationen dazu, wie Sie diese Unterstützung aktivieren, finden Sie unter so wird es [gemacht: Konfigurieren des Servers für die Delegierung als vertrauenswürdig](https://go.microsoft.com/fwlink/?LinkId=166682) ( https://go.microsoft.com/fwlink/?LinkId=166682) .

### Leitfaden zum Installieren oder Aktualisieren von Clients auf App-v 4.5 SP2 mithilfe von Setup.msi

Beim Installieren oder Aktualisieren Ihrer APP-v-Clients auf App-v 4,5 SP2 mithilfe von Setup.msi werden die Voraussetzungen nicht automatisch installiert.

WORKAROUNDYou müssen die Voraussetzungen manuell installieren, bevor Sie die APP-v-Clients auf App-v 4.5 SP2 installieren oder aktualisieren. Detaillierte Anweisungen zum Installieren der Voraussetzungen und des App-V-Clients finden Sie unter so wird es [gemacht: Installieren des Clients mithilfe der Befehlszeile](https://go.microsoft.com/fwlink/?LinkId=144106) ( https://go.microsoft.com/fwlink/?LinkId=144106) .

Wenn dies abgeschlossen ist, installieren Sie die App-V 4,5 SP2-Clients, indem Sie Setup.msi mit administrativen Anmeldeinformationen verwenden. Diese Datei ist im Installers\\Client-Ordner auf dem App-V 4,5 SP2-Veröffentlichungsmedium verfügbar.

Verwenden Sie bei der Installation der Fehlerberichterstattung für Microsoft-Anwendungen den folgenden Befehl, wenn Sie auf den App-V 4,5 SP2-Desktop Client installieren oder darauf aktualisieren:

**msiexec/i dw20shared.msi APPGUID = {C6FC75B9-7D86-4C44-8BDB-EAFE1F0E200D} ALLUSERS = 1 Reboot = unterdrücken Sie erneut installieren = alle REINSTALLMODE = vomus**

Wenn Sie aber auf den App-V 4,5 SP2-Client für Remote Desktop Dienste (vormals Terminal Dienste) installieren oder ein Upgrade ausführen, verwenden Sie den folgenden Befehl:

**msiexec/i dw20shared.msi APPGUID = {ECF80BBA-CA07-4A74-9ED6-E064F38AF1F5} ALLUSERS = 1 Reboot = unterdrücken Sie erneut installieren = alle REINSTALLMODE = vomus**

**Hinweis:**  
-   Der APPGUID-Parameter verweist auf den Produktcode der App-V-Clients, die Sie installieren oder aktualisieren. Der Produktcode ist für jede Setup.msi eindeutig. Sie können den Orca-Daten Bank Editor oder ein ähnliches Tool verwenden, um Windows Installer-Dateien zu überprüfen und den Produktcode zu ermitteln. Dieser Schritt ist für alle Installationen oder Upgrades auf App-V 4,5 SP2 erforderlich.

-   Dieser Schritt ist nicht erforderlich, wenn Sie ein Upgrade durchlaufen und Dw20shared.msi bereits installiert haben.

 

### Verbessern der Leistung bei der Sequenzierung von .NET Framework

Bei der Sequenzierung von Microsoft .NET Framework kann es zu einer reduzierten Systemleistung kommen, da der .NET Framework-NGen-Dienst versucht, Assemblys als Hintergrundaufgabe vorkompilieren.

WORKAROUNDWhen-Sequenzierung .NET Framework deaktivieren Sie nach Abschluss der Überwachungsphase den .NET Framework-NGen-Dienst (Mscorsvw.exe). Sie müssen die Registerkarte **Virtuelle Dienste** im App-V-Sequenzer verwenden und den Starttyp in **deaktiviert**ändern.

### Wenn Sie den Microsoft Application Virtualization-Client deinstallieren, werden die Benutzereinstellungen gelöscht, die dem Benutzer zugeordnet sind, der die Deinstallation ausführt.

Wenn Sie den App-V-Client deinstallieren, entfernt der Windows Installer Application Virtualization-Einstellungen aus dem Profil des aktuellen Benutzers. Wenn Ihr Computer Server gespeicherte Profile verwendet, verwenden Sie Ihr privates Netzwerkkonto nicht, um den Client zu deinstallieren, da dadurch die Einstellungen für Ihre virtuellen Anwendungen auf allen ihren Computern entfernt werden.

WORKAROUNDYou muss den App-V-Client mit einem Administratorkonto deinstallieren, das nicht für die Ausführung virtueller Anwendungen verwendet wird.

### Bearbeitungen, die auf dem virtuellen Dateisystem und den Registerkarten der virtuellen Registrierung vorgenommen wurden, müssen beim Ausführen des Sequenz-Assistenten gespeichert werden.

Wenn Sie ein Paket öffnen, um ein Upgrade durchzuführen, oder wenn Sie den Sequenz-Assistenten bereits mit einem neuen Paket ausgeführt haben und Änderungen am Paket auf den Registerkarten virtuelles Dateisystem oder virtuelle Registrierung vornehmen, werden diese Änderungen nicht automatisch gespeichert.

WORKAROUNDSave Sie die Änderungen, bevor Sie den Assistenten erneut ausführen, um sicherzustellen, dass Sie in der virtuellen Umgebung des Assistenten wiedergegeben werden.

### Befehlszeilen-Sequencer muss über eine Eingabeaufforderung mit erhöhten Rechten ausgeführt werden

Wenn Sie den Befehlszeilen-Sequenzer verwenden, wird keine Eingabeaufforderung zur Erhöhung angezeigt.

WORKAROUNDRun Sie den Befehlszeilen-Sequencer mithilfe einer Eingabeaufforderung mit erhöhten Rechten.

### Kurze Pfadvariablennamen in OSD-Dateien können zu Fehlern führen

Wenn Sie Fehler 450478-1F702339-0000010B "der Verzeichnisname ist ungültig" beim Starten einer virtuellen Anwendung auf dem Client erhalten, ist es möglich, dass die Variable im OSD-Menü falsch eingestellt ist. Dies kann geschehen, wenn das Installationsprogramm der Anwendung einen kurzen Pfadnamen während der Sequenzierung festlegt.

WORKAROUNDRemove Sie die nachfolgende Tilde aus einer beliebigen CSIDL-Variablen, die in der OSD-Datei vorhanden ist.

### <a href="" id="correct-syntax-for-decodepath-parameter-for-command-line-sequencer-"></a>Korrekte Syntax für den DECODEPATH-Parameter für Befehlszeilen-Sequenzer

Wenn Sie im Befehlszeilen-Sequencer ein Paket für das Upgrade öffnen und es in das Stammverzeichnis von Laufwerk Q decodieren, sollte die Syntax für den *DECODEPATH* -Parameter keinen nachfolgenden Schrägstrich beinhalten.

WORKAROUNDYou kann **f:** anstelle von **Q:\\** verwenden (wobei das nachfolgende "\ \"-Zeichen ausgelassen wird).

### <a href="" id="when-upgrading-app-v-4-2-packages--you-encounter-problems-caused-by-windows-installer-files-in-the-virtual-file-system-"></a>Wenn upgradingAPP-V 4,2-Pakete auftreten, treten Probleme auf, die von Windows Installer-Dateien im virtuellen Datei System verursacht werden.

Beim Aktualisieren eines Pakets von App-v 4.2 können Probleme im Zusammenhang mit einer Nichtübereinstimmung von Windows Installer-Systemdateien auftreten, die standardmäßig in App-v 4.2 enthalten sind, und die Windows Installer-Bibliotheken, die lokal auf der Sequenzierungs Arbeitsstation installiert sind. Die folgenden Dateien befinden sich in CSIDL \ _SYSTEM \ \:

Cabinet.dll

Msi.dll

Msiexec.exe

Msihnd.dll

Msimsg.dlll

WORKAROUNDDelete Sie alle vorhergehenden Dateien aus dem Paket. Löschen Sie die Zuordnungen auf der Registerkarte **VFS** und die eigentlichen Dateien im CSIDL \ _SYSTEM-Ordner in Ihrem Decode-Pfad.

### <a href="" id="on-windows-xp--by-default--client-installation-logging-is-not-enabled-"></a>Unter WindowsXP ist die Client Installationsprotokollierung standardmäßig nicht aktiviert.

Wenn Sie den Client installieren, um sicherzustellen, dass Installationsfehler für die Problembehandlung erfasst werden, müssen Sie die Protokollierung über die Befehlszeile aktivieren.

WORKAROUNDAdd Sie den Parameter */l\ * VX! log.txt* an die Befehlszeile, wie im folgenden Beispiel gezeigt:

**setup.exe/s/v "/qn/l\ * VX! log.txt "**

**msiexec.exe/i setup.msi/Qn/l\ * VX! log.txt**

Alternativ können Sie den Registrierungsschlüssel auf den folgenden Wert setzen:

**\ [HKEY \ _LOCAL \ _MACHINE \\software\\policies\\microsoft\\windows\\installer\] "Logging" = "voicewarmupx!"**

### Damit die Kerberos-Authentifizierung funktioniert, müssen Dienstprinzipalnamen (Service Principal Names, SPNs) für IIS registriert sein.

Wenn Sie Internet Informationsdienste (IIS) 6.0 oriis 7.0 für Symbol-oder OSD-Dateiabruf und-Streaming von Paketen verwenden, müssen die SPNs wie folgt registriert werden, um die Kerberos-Authentifizierung zu aktivieren:

-   Führen Sie auf dem IIS-Server die folgenden Befehle mit dem SETSPN.EXE Resource Kit-Tool aus. Der vollqualifizierte Domänenname (Fully Qualified Domain Name, FQDN) des Servers muss verwendet werden.

    **Setspn-r SOFTGRID/ &lt; Server-FQDN&gt;**

    **Setspn-r http/ &lt; Server-FQDN&gt;**

Weitere Informationen finden Sie unter [integrierte Windows-Authentifizierung (IIS 6,0)](https://go.microsoft.com/fwlink/?LinkId=131407) ( https://go.microsoft.com/fwlink/?LinkId=131407) .

### .Net-Kompatibilitätsänderungen

Microsoft Application Virtualization (App-V) kumulative Update1 oder höher unterstützt die Sequenzierung von .NET Framework unter WindowsXP SP2 oder höher. Sequenz Routinen für .NET-Anwendungen, die für SoftGrid 4.2 geschrieben wurden, müssen möglicherweise aktualisiert werden, wenn Sie mit dem App-V 4,5-Sequenzer verwendet werden. Details und Problemumgehungen finden Sie im Application Virtualization TechCenter-Artikel unter [Support für .net in Microsoft Application Virtualization 4,5](https://go.microsoft.com/fwlink/?LinkId=123412) ( https://go.microsoft.com/fwlink/?LinkId=123412) .

### <a href="" id="after-client-upgrade-from-app-v-4-2--some-applications-are-not-shown-"></a>Nach dem Client Upgrade von App-v 4.2 werden einige Anwendungen nicht angezeigt

Überprüfen Sie den folgenden Fehler im Protokoll: "der Application Virtualization-Client konnte die OSD-Datei nicht analysieren". Der App-V 4,5-Client filtert Anwendungen mit einer OSD-Datei, die eine leere OS-Tag ( &lt; OS &gt; &lt; /OS &gt; ) enthält.

WORKAROUNDDelete Sie das leere Betriebssystem-Tag aus der OSD-Datei.

### Der App-V-Server erfordert Ausnahmen in der Firewall für bestimmte Prozesse.

Damit der Serveranwendungen ordnungsgemäß streamen kann, erfordern die Kernprozesse des Servers, einschließlich des Verteilers, den Zugriff über die Firewall.

Problemumgehung: Ausnahmen in der Server Firewall für die folgenden Prozesse: Sghwsvr.exe und Sghwdsptr.exe. Dies gilt für den App-v-Verwaltungsserver und den App-v-Streamingserver.

### Wenn das Server-Installationsprogramm im unbeaufsichtigten Modus ausgeführt wird, überprüft es nicht richtig auf MSXML6

Der App-V-Verwaltungs Server hängt von MSXML6 ab. Wenn Sie das Installationsprogramm allerdings im unbeaufsichtigten Modus ausführen, beispielsweise mithilfe des Befehls **msiexec-i setup.msi/Qn** auf einem System, auf dem MSXML6 noch nicht installiert ist, erkennt das Installationsprogramm die fehlende Abhängigkeit nicht, und es wird ohnehin nicht installiert. Wenn Clients versuchen, Veröffentlichungsinformationen vom App-V-Verwaltungs Server zu aktualisieren, werden daher Fehler angezeigt.

WORKAROUNDVerify Sie, dass MSXML6 auf dem System installiert ist, bevor Sie eine unbeaufsichtigte Installation des App-V-Verwaltungsservers versuchen.

### Fehlercode 000C800 beim Versuch, eine Verbindung mit der Application Virtualization Management Console herzustellen

Ein Application Virtualization-Administrator, der kein lokaler Administrator auf dem App-v Management Web Service-Server ist, erhält einen Fehler (Fehlercode: 000C800) beim Versuch, eine Verbindung mit der APP-v-Verwaltungskonsole herzustellen, und der "SftMMC. Log-Eintrag gibt an, dass der Zugriff auf SftMgmt. udl verweigert wird. Damit Sie erfolgreich eine Verbindung mit der APP-v-Verwaltungskonsole herstellen können, muss ein Administrator, der nicht über lokale Administratorrechte auf dem App-v Management-Webdienstserver verfügt, mindestens über Lese-und Ausführungsberechtigungen für die SftMgmt. UDL-Datei verfügen.

Application Virtualization-Administratoren müssen über Lese-und Ausführungsberechtigungen für die SftMgmt. UDL-Datei im Ordner%SystemDrive%\\Program c:\\Programme\\Microsoft System Center App virt Management Server\\App virt-Verwaltungsdienst verfügen.

### Befehlszeilenparameter des Client Installationsprogramms werden ignoriert, wenn Sie in Verbindung mit KEEPCURRENTSETTINGS = 1 verwendet werden.

Bei Verwendung in Verbindung mit KEEPCURRENTSETTINGS = 1 werden die folgenden Befehlszeilenparameter des Clientinstallationsprogramms ignoriert: SWICACHESIZE, MINFREESPACEMB, ALLOWINDEPENDENTFILESTREAMING, ApplicationSourceRoot, IconSourceRoot, OSDSourceRoot, SYSTEMEVENTLOGLEVEL, SWIGLOBALDATA, DOTIMEOUTMINUTES, SWIFSDRIVE, AUTOLOADTARGET, AUTOLOADTRIGGERS, SWIUSERDATA und REQUIRESECURECONNECTION.

WORKAROUNDIf Sie über Einstellungen verfügen, die Sie beibehalten möchten, verwenden Sie KEEPCURRENTSETTINGS = 1, und setzen Sie die anderen Parameter nach der Bereitstellung. Die App-V ADM-Vorlage kann zum Festlegen der folgenden Clienteinstellungen verwendet werden: ApplicationSourceRoot, IconSourceRoot, OSDSourceRoot, AUTOLOADTARGET, AUTOLOADTRIGGERS, DOTIMEOUTMINUTES und ALLOWINDEPENDENTFILESTREAMING. Sie können die ADM-Vorlage aus dem Microsoft Download Center unter [Microsoft Application Virtualization administrative Template (ADM-Vorlage)](https://go.microsoft.com/fwlink/?LinkId=121835) herunterladen ( https://go.microsoft.com/fwlink/?LinkId=121835) .

### Anmerkungen zu dieser Version Copyright-Informationen

Dieses Dokument wird ohne Gewähr zur Verfügung gestellt. Die in diesem Dokument enthaltenen Informationen und Ansichten, einschließlich URLs und andere Verweise auf Internetwebsites, können ohne vorherige Ankündigung geändert werden. Das Risiko der Nutzung dieser Informationen liegt beim Benutzer.

Einige hier dargestellte Beispiele werden nur zur Illustration bereitgestellt und sind fiktiv.Es ist keine wirkliche Zuordnung oder Verbindung vorgesehen oder sollte abgeleitet werden.

Dieses Dokument stellt Ihnen keinerlei Rechte am geistigen Eigentum eines beliebigen Microsoft-Produkts zur Verfügung. Dieses Dokument darf für interne Referenzzwecke kopiert und verwendet werden. Sie können dieses Dokument für Ihre internen, Referenzzwecke ändern.



Microsoft, Active Directory, ActiveSync, MS-DOS, Windows, Windows Server und Windows Vista sind Marken der Microsoft-Unternehmensgruppe.

Alle anderen Marken sind Eigentum ihrer jeweiligen Eigentümer.

 

 





