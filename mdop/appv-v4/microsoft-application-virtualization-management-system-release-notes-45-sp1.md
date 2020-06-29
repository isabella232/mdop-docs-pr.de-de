---
title: Versionshinweise zu Microsoft Application Virtualization Management System 4,5 SP1
description: Versionshinweise zu Microsoft Application Virtualization Management System 4,5 SP1
author: dansimp
ms.assetid: 5d6b11ea-7b87-4084-9a7c-0d831f247aa3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 5c24d2e98ad09460ca22e4b29d75ae2b9c72d0bf
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806595"
---
# Versionshinweise zu Microsoft Application Virtualization Management System 4,5 SP1


Drücken Sie STRG + F, um diese Versionshinweise zu durchsuchen.

**Wichtig**  Lesen Sie diese Versionshinweise gründlich, bevor Sie das Application Virtualization Management System installieren. Diese Anmerkungen zu dieser Version enthalten Informationen, die Sie benötigen, um das Application Virtualization Management System erfolgreich zu installieren. Diese Anmerkungen zu dieser Version enthalten Informationen, die in der Produktdokumentation nicht zur Verfügung stehen. Wenn zwischen diesen Anmerkungen zur Version und anderen Application Virtualization Management System-Dokumentationen Diskrepanzen bestehen, sollte die neueste Änderung als autorisierend angesehen werden.

 

Aktualisierte Informationen zu bekannten Problemen finden Sie in der Microsoft TechNet-Bibliothek unter <https://go.microsoft.com/fwlink/?LinkId=122918> .

## Informationen zu Microsoft Application Virtualization 4,5 Service Pack 1


Diese Anmerkungen zur Version wurden aktualisiert, um die Änderungen zu berücksichtigen, die mit Microsoft Application Virtualization (App-V) 4.5 Service Pack1 (SP1) eingeführt wurden. Dieses Service Pack enthält die folgenden Änderungen:

-   Unterstützung für Windows 7 und Windows Server 2008 R2: App-V 4,5 SP1 bietet Unterstützung für Windows 7 und Windows Server 2008 R2, einschließlich Unterstützung für Windows 7-Features wie Taskleiste, AppLocker, BranchCache und BitLocker to go.Die Windows Server 2008 R2-Unterstützung ist nur für den Application Virtualization Server vorgesehen. Weitere Informationen zur AppLocker-Unterstützung in Windows 7 finden Sie unter <https://go.microsoft.com/fwlink/?LinkID=156732> .

-   Unterstützung für Kerberos-Realms von Drittanbietern: App-V 4,5 SP1 bietet Unterstützung für Umgebungen, die über eine Vertrauensstellung und zugeordnete Benutzerkonten zwischen einer Windows-Domäne und einem mit Kerberos-Realm verfügen, ein Szenario, das an vielen Universitäten üblich ist. Informationen dazu, wie Sie diesen Support aktivieren können, finden Sie in der Microsoft TechNet-Bibliothek unter <https://go.microsoft.com/fwlink/?LinkId=166004> .

-   Verbesserte Unterstützung für Anwendungsveröffentlichung und-Streaming über http/https: App-V 4,5 SP1 bietet Unterstützung für die Veröffentlichung und das Streaming von Anwendungen über die HTTP/HTTPS-Protokolle für Windows XP Home Edition, Windows Vista Home Basic und Windows 7 Home Basic.

-   Kunden Feedback und Hotfix-Rollup: App-v 4.5 SP1 umfasst auch ein Rollup von Korrekturen, um Probleme zu beheben, die seit der Microsoft Application Virtualization (App-V) 4.5 CU1-Version gefunden wurden. Die Updates sind ein Ergebnis einer Kombination aus bekannten Problemen und Kundenfeedback unserer internen Teams, Partner und Kunden, die APP-v 4.5 verwenden. Eine vollständige Liste der Updates finden Sie im Knowledge Base-Artikel unter <https://go.microsoft.com/fwlink/?LinkId=167121> .

## Informationen zur Produktdokumentation


Eine umfassende Dokumentation für Application Virtualization (app-v) finden Sie auf der Microsoft TechNet-Anwendung im Application Virtualization (app-v) TechCenter unter <https://go.microsoft.com/fwlink/?LinkId=122939> . Die TechNet-Dokumentation enthält die Online Hilfe für Application Virtualization Sequencer, den Application Virtualization-Client und den Application Virtualization Server. Darüber hinaus enthält es das Leitfaden zur Planung und Bereitstellung von Application Virtualization sowie das Application Virtualization Operations Guide.

## Schutz vor Sicherheitsrisiken und Viren


Wir empfehlen, dass Sie die neuesten verfügbaren Sicherheitsupdates für jede neue Software installieren, die installiert werden soll, um den Schutz vor Sicherheitsrisiken und Viren zu gewährleisten. Weitere Informationen finden Sie auf der Microsoft-Sicherheitswebsite unter <https://go.microsoft.com/fwlink/?LinkId=3482> .

## Bereitstellen von Feedback


Sie können über ein Community-Forum im Microsoft Application Virtualization TechCenter () Feedback bereitstellen, Vorschläge machen oder ein Problem mit dem Microsoft Application Virtualization (App-V)-Verwaltungs System melden <https://go.microsoft.com/fwlink/?LinkId=122917> .

Sie können auch Ihr Feedback zur Dokumentation direkt an das App-V-Dokumentationsteam weitergeben. Senden Sie Ihr Feedback zur Dokumentation an appvdocs@microsoft.com.

## Bekannte Probleme mit Application Virtualization 4.5 SP1


In diesem Abschnitt finden Sie die neuesten Informationen zu Problemen mit Microsoft Application Virtualization (App-V) 4.5 SP1. Diese Probleme werden in der Produktdokumentation nicht angezeigt und können in einigen Fällen der vorhandenen Produktdokumentation widersprechen. Wenn möglich, werden diese Probleme in späteren Versionen der Software behoben.

### Leitfaden zum Installieren der Server-Verwaltungskonsole

Wenn Sie Verwaltungssoftware auf anderen Systemen als dem primären Application Virtualization Publishing-und Streamingserver installieren müssen, unterstützt die Server Installation die Installation der Verwaltungskonsole und des Verwaltungs-Webdiensts auf separaten Servern vom primären App-V-Verwaltungsserver. Um die Verwaltungskomponenten auf mehreren Servern zu verteilen, muss die Kerberos-Delegierung auf dem Server aktiviert sein, auf dem der Webdienst installiert ist. Informationen dazu, wie Sie diesen Support aktivieren können, finden Sie in der Microsoft TechNet-Bibliothek unter <https://go.microsoft.com/fwlink/?LinkId=166682>

### Leitfaden zum Installieren oder Aktualisieren von Clients auf App-v 4.5 SP1 mithilfe von setup.msi

Wenn Sie Ihre APP-v-Clients auf App-v 4,5 SP1 mithilfe von setup.msi installieren oder aktualisieren, werden die Voraussetzungen nicht automatisch installiert.

WORKAROUNDYou müssen die Voraussetzungen manuell installieren, bevor Sie den App-v-Client toApp-v 4,5 SP1 installieren oder aktualisieren. Detaillierte Anweisungen zum Installieren der Voraussetzungen und des App-V-Clients finden Sie unter <https://go.microsoft.com/fwlink/?LinkId=144106> .

Wenn dies abgeschlossen ist, installieren Sie den App-V 4,5 SP1-Client unter Verwendung von setup.msi mit erhöhten Rechten. Diese Datei ist im Installers\\Client-Ordner auf dem App-V 4,5 SP1-Veröffentlichungsmedium verfügbar.

Verwenden Sie beim Installieren der Fehlerberichterstattung für Microsoft-Anwendungen den folgenden Befehl, wenn Sie auf den Desktop Client für App-V 4,5 SP1 installieren oder ein Upgrade durchführen:

    msiexec /i dw20shared.msi APPGUID={93468B43-C19D-44F9-8BCC-114076DB0443}  allusers=1 reboot=suppress REINSTALL=all REINSTALLMODE=vomus

Wenn Sie aber auf den App-V 4,5 SP1-Client für Remote Desktop Dienste (vormals Terminal Dienste) installieren oder ein Upgrade ausführen, verwenden Sie den folgenden Befehl:

    msiexec /i dw20shared.msi APPGUID={0042AD3C-99A4-4E58-B5F0-744D5AD96E1C} allusers=1 reboot=suppress REINSTALL=all REINSTALLMODE=vomus

**Hinweis**  Der APPGUID-Parameter verweist auf den Produktcode des App-V-Clients, den Sie installieren oder aktualisieren. Der Produktcode ist für jede setup.msi eindeutig. Sie können den Orca-Datenbankeditor oder ein ähnliches Tool verwenden, um Windows Installer-Dateien zu überprüfen und den Produktcode zu ermitteln. Dieser Schritt ist für alle Installationen oder Upgrades auf App-V 4,5 SP1 erforderlich.

 

### Verbessern der Leistung bei der Sequenzierung von .NET Framework

Bei der Sequenzierung von .NET Framework kann es zu einer reduzierten Systemleistung kommen, da der Microsoft .NET Framework-NGen-Dienst versucht, Assemblys als Hintergrundaufgabe vorkompilieren.

WORKAROUNDWhen-Sequenzierung .NET Framework deaktivieren Sie nach Abschluss der Überwachungsphase den Microsoft .NET Framework-NGen-Dienst (mscorsvw.exe). Sie müssen die Registerkarte **Virtuelle Dienste** im Sequencer verwenden und den Starttyp in deaktiviert ändern.

### Wenn Sie den Microsoft Application Virtualization-Client deinstallieren, werden die Benutzereinstellungen gelöscht, die dem Benutzer zugeordnet sind, der die Deinstallation ausführt.

Wenn Sie den App-V-Client deinstallieren, entfernt der Windows Installer die Anwendungsvirtualisierung-Einstellungen aus dem Profil des aktuellen Benutzers. Wenn Ihr Computer Server gespeicherte Profile verwendet, verwenden Sie Ihr privates Netzwerkkonto nicht, um den Client zu deinstallieren, da dadurch die Einstellungen für Ihre virtuellen Anwendungen auf allen ihren Computern entfernt werden.

WORKAROUNDYou sollte die App-V-Client-Deinstallation mit einem Administratorkonto durchführen, das nicht für die Ausführung virtueller Anwendungen verwendet wird.

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

### .Net-Kompatibilitätsänderungen

Microsoft Application Virtualization (App-V) kumulative Update1 oder höher unterstützt die Sequenzierung von .NET Framework unter WindowsXP (SP2 oder höher). Sequenz Routinen für .NET-Anwendungen, die für SoftGrid 4.2 geschrieben wurden, müssen möglicherweise aktualisiert werden, wenn Sie mit dem App-V 4,5-Sequenzer verwendet werden. Details und Problemumgehungen finden Sie im Knowledge Base-Artikel unter <https://go.microsoft.com/fwlink/?LinkId=123412> .

### <a href="" id="after-client-upgrade-from-app-v-4-2--some-applications-are-not-shown-"></a>Nach dem Client Upgrade von App-v 4.2 werden einige Anwendungen nicht angezeigt

Überprüfen Sie den folgenden Fehler im Protokoll: "der Application Virtualization-Client konnte die OSD-Datei nicht analysieren". Der App-V 4,5-Client filtert Anwendungen mit einer OSD-Datei, die eine leere OS-Kategorie ( &lt; OS &gt; &lt; /OS &gt; ) enthält.

WORKAROUNDDelete Sie das leere Betriebssystem-Tag aus der OSD-Datei.

### Der App-V-Server erfordert Ausnahmen in der Firewall für bestimmte Prozesse.

Damit der Serveranwendungen ordnungsgemäß streamen kann, müssen die Hauptprozesse des Servers, einschließlich des Verteilers, über die Firewall zugreifen.

Problemumgehung: Ausnahmen in der Server Firewall für die folgenden Prozesse: sghwsvr.exe und sghwdsptr.exe. Dies gilt für den App-v-Verwaltungsserver und den App-v-Streamingserver.

### Wenn das Server-Installationsprogramm im unbeaufsichtigten Modus ausgeführt wird, überprüft es nicht richtig auf MSXML6

Der App-V-Verwaltungs Server hängt von MSXML6 ab. Wenn Sie das Installationsprogramm allerdings im unbeaufsichtigten Modus ausführen, beispielsweise mithilfe des Befehls "msiexec-i setup.msi/qn" auf einem System, auf dem MSXML6 noch nicht installiert ist, erkennt das Installationsprogramm die fehlende Abhängigkeit nicht, und es wird ohnehin nicht installiert. Wenn Clients versuchen, Veröffentlichungsinformationen vom App-V-Verwaltungs Server zu aktualisieren, werden daher Fehler angezeigt.

WORKAROUNDVerify Sie, dass MSXML6 auf dem System installiert ist, bevor Sie eine unbeaufsichtigte Installation des App-V-Verwaltungsservers versuchen.

### Fehlercode 000C800 beim Versuch, eine Verbindung mit der Application Virtualization Management Console herzustellen

Ein Application Virtualization-Administrator, der kein lokaler Administrator auf dem App-v Management Web Service-Server ist, erhält beim Versuch, eine Verbindung mit der APP-v-Verwaltungskonsole herzustellen, eine Fehlermeldung (Fehlercode: 000C800), und der "SftMMC. Log-Eintrag gibt an, dass der Zugriff auf SftMgmt. udl verweigert wird. Damit Sie erfolgreich eine Verbindung mit der APP-v-Verwaltungskonsole herstellen können, muss ein Administrator, der nicht über lokale Administratorrechte auf dem App-v Management-Webdienstserver verfügt, mindestens über Lese-und Ausführungsberechtigungen für die SftMgmt. UDL-Datei verfügen.

Die Application Virtualization-Administratoren müssen Lese-und Ausführungsberechtigungen für die SftMgmt. UDL-Datei unter%systemdrive%\\Program c:\\Programme\\Microsoft System Center App virt Management Server\\App virt-Verwaltungsdienst erhalten.

### Befehlszeilenparameter des Client Installationsprogramms werden ignoriert, wenn Sie in Verbindung mit KEEPCURRENTSETTINGS = 1 verwendet werden.

Bei Verwendung in Verbindung mit KEEPCURRENTSETTINGS = 1 werden die folgenden Befehlszeilenparameter des Clientinstallationsprogramms ignoriert: SWICACHESIZE, MINFREESPACEMB, ALLOWINDEPENDENTFILESTREAMING, ApplicationSourceRoot, IconSourceRoot, OSDSourceRoot, SYSTEMEVENTLOGLEVEL, SWIGLOBALDATA, DOTIMEOUTMINUTES, SWIFSDRIVE, AUTOLOADTARGET, AUTOLOADTRIGGERS, SWIUSERDATA und REQUIRESECURECONNECTION.

WORKAROUNDIf Sie Einstellungen, die Sie beibehalten möchten, verwenden Sie KEEPCURRENTSETTINGS = 1, und setzen Sie die anderen Parameter nach der Bereitstellung. Die App-V ADM-Vorlage kann zum Festlegen der folgenden Clienteinstellungen verwendet werden: ApplicationSourceRoot, IconSourceRoot, OSDSourceRoot, AUTOLOADTARGET, AUTOLOADTRIGGERS, DOTIMEOUTMINUTES und ALLOWINDEPENDENTFILESTREAMING. Die ADM-Vorlage finden Sie unter <https://go.microsoft.com/fwlink/?LinkId=121835> .

## Anmerkungen zu dieser Version Copyright-Informationen


Informationen in diesem Dokument, einschließlich URLs und anderen Internet-Website verweisen, können ohne Vorankündigung geändert werden und dienen nur zu Informationszwecken. Das gesamte Risiko der Nutzung oder der Ergebnisse aus der Verwendung dieses Dokuments verbleibt beim Nutzer, und Microsoft Corporation übernimmt keine Garantien, weder ausdrücklich noch impliziert. Sofern nicht anders angegeben, sind die Unternehmen, Organisationen, Produkte, Domänennamen, e-Mail-Adressen, Logos, Personen, Orte und Ereignisse, die in Beispielen hierin dargestellt sind, fiktiv. Keine Assoziation mit einem wirklichen Unternehmen, einer Organisation, einem Produkt, einem Domänennamen, einer e-Mail-Adresse, einem Logo, einer Person, einem Ort oder einem Ereignis ist beabsichtigt oder sollte abgeleitet werden. Die Einhaltung aller anwendbaren Urheberrechtsgesetze obliegt dem Nutzer. Ohne die Rechte unter dem Urheberrecht zu begrenzen, darf kein Teil dieses Dokuments reproduziert, gespeichert oder in ein Retrievalsystem aufgenommen oder in irgendeiner Form oder auf andere Weise (elektronisch, mechanisch, Fotokopieren, aufzeichnen oder auf andere Weise) oder zu einem beliebigen Zweck ohne die ausdrückliche schriftliche Genehmigung der Microsoft Corporation übertragen werden.

Microsoft hat möglicherweise Patente, Patentanmeldungen, Marken, Urheberrechte oder andere Rechte an geistigem Eigentum, die Inhalte dieses Dokuments abdecken. Sofern nicht ausdrücklich in einem schriftlichen Lizenzvertrag von Microsoft vorgesehen, gibt Ihnen die Einrichtung dieses Dokuments keine Lizenz für diese Patente, Marken, Urheberrechte oder sonstiges geistiges Eigentum.



Microsoft, Active Directory, ActiveSync, MS-DOS, Windows, Windows Server und Windows Vista sind Marken der Microsoft-Unternehmensgruppe.

Alle anderen Marken sind Eigentum ihrer jeweiligen Eigentümer.

 

 





