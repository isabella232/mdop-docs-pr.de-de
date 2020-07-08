---
title: Registrierungswerte für App-V Client
description: Registrierungswerte für App-V Client
author: dansimp
ms.assetid: 46af5209-9762-47b9-afdb-9a2947e013f7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 05cd807ff9882bc478aca07abc4a28cdea83086a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808055"
---
# Registrierungswerte für App-V Client


Der Microsoft Application Virtualization (App-V)-Client speichert seine Konfiguration in der Registrierung. Sie können einige nützliche Informationen zu dem Client sammeln, wenn Sie das Format der Daten in der Registrierung verstehen. Sie können auch viele Clientaktionen konfigurieren, indem Sie Registrierungseinträge ändern. In diesem Thema werden alle Application Virtualization (App-V)-Client Registrierungsschlüssel aufgelistet und deren Verwendung erläutert.

**Wichtig**  
Auf einem Computer, auf dem ein 64-Bit-Betriebssystem ausgeführt wird, werden die in den folgenden Abschnitten beschriebenen Schlüssel und Werte unter HKEY \ _LOCAL \ _MACHINE \\software\\wow6432node\\microsoft\\softgrid\\4.5\\client.



## Konfigurationsschlüssel


Die folgende Tabelle enthält Informationen zu den Registrierungswerten, die mit dem HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\softgrid\\4.5\\client\\configuration-Schlüssel verknüpft sind.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Name</th>
<th align="left">Typ</th>
<th align="left">Daten (Beispiele)</th>
<th align="left">Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>ProductName</p></td>
<td align="left"><p>Zeichenfolge</p></td>
<td align="left"><p>Microsoft Application Virtualization-Desktop Client</p></td>
<td align="left"><p>Nicht ändern.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Version </p></td>
<td align="left"><p>Zeichenfolge </p></td>
<td align="left"><p>4.5.0.xxx </p></td>
<td align="left"><p>Nicht ändern. </p></td>
</tr>
<tr class="odd">
<td align="left"><p>Treiber </p></td>
<td align="left"><p>Zeichenfolge </p></td>
<td align="left"><p>Sftfs.sys </p></td>
<td align="left"><p>Wenn dieser Schlüsselwert vorhanden ist, enthält er den Namen des Treibers, der beim letzten Start des Kerns einen Abbruchfehler verursacht hat. Nachdem Sie den Abbruchfehler behoben haben, müssen Sie diesen Schlüsselwert löschen, damit sftlist beginnen kann.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Entspricht InstallPath </p></td>
<td align="left"><p>Zeichenfolge </p></td>
<td align="left"><p>Standard = c:\Programme\Microsoft Application Virtualization Client</p></td>
<td align="left"><p>Der Speicherort, an dem der Client installiert ist. Nicht ändern. </p></td>
</tr>
<tr class="odd">
<td align="left"><p>Protokolldateiname </p></td>
<td align="left"><p>Zeichenfolge </p></td>
<td align="left"><p>Standard = CSIDL_COMMON_APPDATA \microsoft\application Virtualization Client\sftlog.txt</p></td>
<td align="left"><p>Der Pfad und Name für die Clientprotokolldatei.</p>
<div class="alert">
<strong>Hinweis:</strong><br/><p>Wenn Sie eine frühere Version als App-V 4,6, SP1 und den Namen oder Speicherort der Protokolldatei ändern, müssen Sie den sftlist-Dienst neu starten, damit die Änderung wirksam wird.</p>
</div>
<div>

</div>
<p></p></td>
</tr>
<tr class="even">
<td align="left"><p>LogMinSeverity </p></td>
<td align="left"><p>DWORD </p></td>
<td align="left"><p>Standard = 4, Informations</p></td>
<td align="left"><p>Steuert, welche Nachrichten in das Protokoll geschrieben werden. Der Wert gibt einen Schwellenwert für das protokollierte an – alles, was kleiner oder gleich dem Wert ist, wird protokolliert. Ein Wert von 0x3 (Warnung) gibt beispielsweise an, dass Warnungen (0x3), Fehler (0x2) und kritische Fehler (0x1) protokolliert werden.</p>
<p>Wertbereich: 0x0 = keine, 0x1 = kritisch, 0x2 = Fehler, 0x3 = Warnung, 0x4 = Informationen (Standard), 0x5 = Verbose.</p>
<p>Die Protokollebene kann über die Application Virtualization (App-V)-Clientkonsole und über die Eingabeaufforderung konfiguriert werden. An einer Eingabeaufforderung wird mit dem Befehl sftlist.exe/Verboselog die Protokollebene auf Verbose erhöht. Weitere Informationen zu Befehlszeilen Details finden Sie unter</p>
<p><a href="https://go.microsoft.com/fwlink/?LinkId=141467https://go.microsoft.com/fwlink/?LinkId=141467" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=141467https://go.microsoft.com/fwlink/?LinkId=141467">https://go.microsoft.com/fwlink/?LinkId=141467https://go.microsoft.com/fwlink/?LinkId=141467</a></p>
<p>.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>LogRolloverCount</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Standard = 4</p></td>
<td align="left"><p>Definiert die Anzahl von Sicherungskopien der Protokolldatei, die beim Zurücksetzen beibehalten werden. Der gültige Bereich ist 0 – 9999. Der Standardwert ist 4. Der Wert 0 bedeutet, dass keine Kopien aufbewahrt werden.</p></td>
</tr>
<tr class="even">
<td align="left"><p>LogMaxSize</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Standard = 256</p></td>
<td align="left"><p>Definiert die maximale Größe in Megabytes (MB), die die Protokolldatei vergrößert werden kann, bevor Sie zurückgesetzt wird. Die Standardgröße ist 256 MB. Wenn diese Größe erreicht ist, wird beim nächsten Schreibversuch eine Protokoll Zurücksetzung erzwungen.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>SystemEventLogLevel</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Standard = 0x4 (App-V 4,5)</p>
<p>Standard = 0x3 (App-V 4,6)</p></td>
<td align="left"><p>Gibt den Protokolliergrad an, bei dem Protokollnachrichten in das NT-Ereignisprotokoll geschrieben werden. Der Wert gibt einen Schwellenwert für das protokollierte an, d. h., alles, was kleiner oder gleich dem Wert ist, wird protokolliert. Ein Wert von 0x3 (Warnung) gibt beispielsweise an, dass Warnungen (0x3), Fehler (0x2) und kritische Fehler (0x1) protokolliert werden.</p>
<p>Wertebereich</p>
<p>0x0 = keine</p>
<p>0x1 = kritisch</p>
<p>0x2 = Fehler</p>
<p>0x3 = Warnung</p>
<p>0x4 = Informationen (Standard)</p>
<p>0x5 = Verbose</p></td>
</tr>
<tr class="even">
<td align="left"><p>AllowIndependentFileStreaming</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Standard = 0</p></td>
<td align="left"><p>Gibt an, ob das Streaming aus einer Datei unabhängig davon aktiviert wird, wie der Client mit dem ApplicationSourceRoot-Parameter konfiguriert wurde. Ist dieser Wert auf "false" festgelegt, wird durch den Transport kein Streaming aus Dateien möglich, auch wenn der OSD-HREF-oder der ApplicationSourceRoot-Parameter einen Dateipfad enthält.</p>
<p>0x0 = false (Standard)</p>
<p>0x1 = wahr</p></td>
</tr>
<tr class="odd">
<td align="left"><p>ApplicationSourceRoot</p></td>
<td align="left"><p>Zeichenfolge</p></td>
<td align="left"><p>rtsps://mainserver:322/prodapps</p>
<p><a href="https://mainserver:443/prodapps" data-raw-source="https://mainserver:443/prodapps">https://mainserver:443/prodapps</a></p>
<p>Datei://\uncserver\share\prodapps</p>
<p>Datei://\uncserver\share</p></td>
<td align="left"><p>Ermöglicht einem Administrator oder einem ESD-System (Electronic Software Distribution), sicherzustellen, dass das Laden der Anwendung entsprechend dem Topologieverwaltung-Schema durchgeführt wird. Verwenden Sie diesen Schlüsselwert, um die OSD-CodeBase für das href-Element (beispielsweise den Quellspeicherort) für eine Anwendung zu überschreiben. Der Anwendungsquellen Stamm unterstützt URLs und UNC-Pfad Formate (Universal Naming Convention).</p>
<p>Das richtige Format für den URL-Pfad ist Protocol://Servername: [Port] [/path] [/], wobei Port und Path optional sind. Wenn kein Port angegeben wird, wird der Standardport für das Protokoll verwendet. Nur der Abschnitt Protocol://Server: Port der OSD-URL wird ersetzt. </p>
<p>Das richtige Format für den UNC-Pfad lautet \computername\sharefolder [Folder] [], wobei Folder optional ist. Der Computername kann ein vollständig qualifizierter Domänenname (Fully Qualified Domain Name, FQDN) oder eine IP-Adresse sein, und sharefolder kann ein Laufwerkbuchstabe sein. Es wird nur der \computername\sharefolder-oder Laufwerkbuchstaben Bereich des OSD-Pfads ersetzt. </p></td>
</tr>
<tr class="even">
<td align="left"><p>OSDSourceRoot</p></td>
<td align="left"><p>Zeichenfolge</p></td>
<td align="left"><p>\computername\sharefolder\resource</p>
<p>\computername\content</p>
<p>C:\foldername</p>
<p><a href="http://computername/productivity/" data-raw-source="http://computername/productivity/">http://computername/productivity/</a></p>
<p><a href="https://computername/productivity/" data-raw-source="https://computername/productivity/">https://computername/productivity/</a></p></td>
<td align="left"><p>Ermöglicht einem Administrator die Angabe eines Quellspeicherorts für den Abruf von OSD-Dateien für ein sequenziertes Anwendungspaket während der Veröffentlichung. Zulässige Formate für die OSDSourceRoot sind UNC-Pfade und URLs (http oder HTTPS).</p></td>
</tr>
<tr class="odd">
<td align="left"><p>IconSourceRoot</p></td>
<td align="left"><p>Zeichenfolge</p></td>
<td align="left"><p>\computername\sharefolder\resource</p>
<p>\computername\content</p>
<p>C:\foldername</p>
<p><a href="http://computername/productivity/" data-raw-source="http://computername/productivity/">http://computername/productivity/</a></p>
<p><a href="https://computername/productivity/" data-raw-source="https://computername/productivity/">https://computername/productivity/</a></p></td>
<td align="left"><p>Ermöglicht einem Administrator, einen Quellspeicherort für das Abrufen von Symboldateien für ein sequenziertes Anwendungspaket während der Veröffentlichung anzugeben. Zulässige Formate für die IconSourceRoot sind UNC-Pfade und URLs (http oder HTTPS).</p></td>
</tr>
<tr class="even">
<td align="left"><p>AutoLoadTriggers</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Standard = 5</p></td>
<td align="left"><p>Beim automatischen Lademodus handelt es sich um einen Client Laufzeitrichtlinien-Konfigurationsparameter, mit dem der sekundäre Funktionsbaustein einer virtualisierten Anwendung automatisch im Hintergrund an den Client gestreamt werden kann. Die Trigger für das automatische Laden sind Flags, die Ereignisse angeben, die das automatische Laden von Anwendungen initiieren. Beim Laden wird implizit Hintergrund Streaming verwendet, damit die Anwendung vollständig in den Cache geladen werden kann. Der primäre Feature-Block wird zuerst geladen, und die restlichen Funktionsbausteine werden in den Hintergrund geladen, damit Vordergrund Vorgänge wie Benutzerinteraktionen mit Anwendungen ausgeführt werden und eine optimale Leistung erzielt wird.</p>
<p>Bitmaskenwerte:</p>
<p>(0) Never: keine Bits sind gesetzt (Wert ist 0), es wird kein automatisches Laden durchgeführt, da keine Trigger gesetzt sind.</p>
<p>(1) onlaunch: das Laden beginnt, wenn ein Benutzer eine Anwendung startet.</p>
<p>(2) OnRefresh: das Laden beginnt, wenn die Anwendung veröffentlicht wird. Dies tritt auf, wenn der paketdatensatz hinzugefügt oder aktualisiert wird, beispielsweise, wenn eine Veröffentlichungsaktualisierung stattfindet.</p>
<p>(4) onlogin: das Laden beginnt, wenn sich ein Benutzer anmeldet.</p>
<p>(5) onlaunch und onlogin: Standard.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>AutoLoadTarget</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Standard = 1</p></td>
<td align="left"><p>Gibt an, was automatisch geladen wird, wenn ein bestimmter Trigger für das automatische Laden eintritt. Bitmaskenwerte:</p>
<p>(0) None: kein automatisches Laden, unabhängig davon, welche Trigger eingestellt werden können.</p>
<p>(1) PreviouslyUsed (Standard): Wenn ein automatischer Trigger aktiviert ist, laden Sie nur die Pakete, bei denen mindestens eine Anwendung im Paket zuvor verwendet wurde – also gestartet oder vorab gespeichert wurde.</p>
<p>(2) alle: Wenn ein automatischer Trigger aktiviert ist, werden alle Anwendungen im Paket (pro Paket) oder alle Pakete (für Client festgesetzt) automatisch geladen, unabhängig davon, ob Sie jemals gestartet wurden.</p></td>
</tr>
<tr class="even">
<td align="left"><p>RequireAuthorizationIfCached</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Standard = 1</p></td>
<td align="left"><p>Gibt an, dass immer eine Autorisierung erforderlich ist, unabhängig davon, ob sich eine Anwendung bereits im Cache befindet. Mögliche Werte:</p>
<p>0 = falsch: versuchen Sie immer, eine Verbindung mit dem Server herzustellen. Wenn keine Verbindung mit dem Server hergestellt werden kann, ermöglicht der Client dem Benutzer weiterhin, eine Anwendung zu starten, die zuvor in den Cache geladen wurde.</p>
<p>1 = wahr (Standard): die Anwendung muss beim Start immer autorisiert werden. Für RTSP-Streaming-Anwendungen wird das Benutzerautorisierungstoken zur Autorisierung an den Server gesendet. Bei dateibasierten Anwendungen steuern Datei-ACLs, ob ein Benutzer auf die Anwendung zugreifen kann.</p>
<p>Starten Sie den sftlist-Dienst neu, damit die Änderung wirksam wird.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>UserDataDirectory </p></td>
<td align="left"><p>Zeichenfolge </p></td>
<td align="left"><p>APPDATA</p></td>
<td align="left"><p>Der Speicherort, an dem der Symbolcache und die Benutzereinstellungen gespeichert werden.</p></td>
</tr>
<tr class="even">
<td align="left"><p>GlobalDataDirectory </p></td>
<td align="left"><p>Zeichenfolge </p></td>
<td align="left"><p>C:\Users\Public\Documents </p></td>
<td align="left"><p>Verzeichnis, das für globale App-V-Daten verwendet werden soll, einschließlich Caches für OSD-Dateien, Symboldateien, Verknüpfungsinformationen und SystemGuard-Ressourcen wie INI-Dateien.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>AllowCrashes </p></td>
<td align="left"><p>DWORD </p></td>
<td align="left"><p>0 oder 1 </p></td>
<td align="left"><p>Standard = 0: ein Wert von "0" bedeutet, dass der Client versucht, interne Programmausnahmen abzufangen, damit andere Benutzer Anwendungen wiederhergestellt und fortfahren können, wenn ein Absturz eintritt. Der Wert 1 bedeutet, dass der Client die internen Programmausnahmen eintreten lässt, damit Sie in einem Debugger erfasst werden können.</p></td>
</tr>
<tr class="even">
<td align="left"><p>CoreInternalTimeout </p></td>
<td align="left"><p>DWORD </p></td>
<td align="left"><p>60</p></td>
<td align="left"><p>Timeout in Sekunden für interne IPC-Anforderungen zwischen Core und Front-End. Nicht ändern. </p></td>
</tr>
<tr class="odd">
<td align="left"><p>DefaultSuiteCombineTime </p></td>
<td align="left"><p>DWORD </p></td>
<td align="left"><p>10</p></td>
<td align="left"><p>Dieser Wert wird verwendet, um anzugeben, wie schnell nach dem Start ein Programm beendet werden kann, und es werden keine Fehlermeldungen generiert, wenn eine andere Anwendung in derselben Suite ausgeführt wird. </p></td>
</tr>
<tr class="even">
<td align="left"><p>SerializedSuiteLaunchTimeout </p></td>
<td align="left"><p>DWORD </p></td>
<td align="left"><p>Standard = 60000</p></td>
<td align="left"><p>Definiert, wie lange der Client in Millisekunden warten wird, während er versucht, Programmstarts in der gleichen Suite zu serialisieren. Bei einem Timeout des Clients wird der Programmstart fortgesetzt, aber nicht serialisiert. </p></td>
</tr>
<tr class="odd">
<td align="left"><p>ScriptTimeout </p></td>
<td align="left"><p>DWORD </p></td>
<td align="left"><p>300</p></td>
<td align="left"><p>Standardtimeout in Sekunden für Skripts in der OSD-Datei, wenn Wait = true. Sie können pro-Skript-Timeouts mit Timeout anstelle von Wait angeben. Der Wert 0 bedeutet keine Wartezeit, und 0xFFFFFFFF bedeutet, dass Sie für immer warten. </p></td>
</tr>
<tr class="even">
<td align="left"><p>LaunchRecordLogPath </p></td>
<td align="left"><p>Zeichenfolge </p></td>
<td align="left"><p></p></td>
<td align="left"><p>Wenn dieser Wert unter HKLM oder HKCU einen gültigen Pfad zu einer Protokolldatei enthält, schreibt SFTTray in dieses Protokoll, wenn Programme gestartet, heruntergefahren, nicht gestartet werden und der getrennte Modus beendet oder beendet wird.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>LaunchRecordMask </p></td>
<td align="left"><p>DWORD </p></td>
<td align="left"><p>0x1A (26) log-Startfehler und die Eingabe-und Ausgangs Aktivität für den Offlinemodus.</p>
<p>0x1F (31) protokolliert alles.</p>
<p>0x0 (0) protokolliert nichts. </p></td>
<td align="left"><p>Gibt an, welches der fünf Ereignisse protokolliert wird (Bitmaskenwerte):</p>
<p>1 für Programmstarts</p>
<p>2 für Fehler beim Startfehler</p>
<p>4 für Shutdowns</p>
<p>8 für die Eingabe des getrennten Modus</p>
<p>16 für das Beenden des getrennten Modus, um die Verbindung zu einem Server wiederherzustellen</p>
<p>Fügen Sie eine beliebige Kombination dieser Nummern hinzu, um die jeweiligen Nachrichten zu aktivieren. Standardmäßig ist 0x1F, wenn nicht in der Registrierung. </p></td>
</tr>
<tr class="even">
<td align="left"><p>LaunchRecordWriteTimeout </p></td>
<td align="left"><p>DWORD </p></td>
<td align="left"><p>Standard = 3000</p></td>
<td align="left"><p>Gibt in Millisekunden an, wie lange das Tablett wartet, wenn es versucht, in das Startdatensatz Protokoll zu schreiben, wenn es von einem anderen Prozess verwendet wird.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>ImportSearchPath </p></td>
<td align="left"><p>Zeichenfolge </p></td>
<td align="left"><p>d:\files; C:\Dokumente und settings\user1\SFTs </p></td>
<td align="left"><p>Eine durch Semikolons getrennte Liste mit bis zu fünf Verzeichnissen für die Suche nach tragbaren SFT-Dateien, bevor der Benutzer aufgefordert wird, ein Verzeichnis auszuwählen. Der nachfolgende umgekehrte Schrägstrich in Paths ist optional. Dieser Wert ist standardmäßig nicht vorhanden und muss manuell eingestellt werden.</p></td>
</tr>
<tr class="even">
<td align="left"><p>UserImportPath</p></td>
<td align="left"><p>Zeichenfolge </p></td>
<td align="left"><p>D:\SFTs\ </p></td>
<td align="left"><p>Gültig nur unter HKCU. Der letzte Speicherort, zu dem der Benutzer beim Suchen einer SFT-Datei für den Paketimport gesucht hat. Wird automatisch festgesetzt, wenn SFT erfolgreich gefunden wurde. Diese wird für aufeinanderfolgende Importe verwendet, wenn Sie versuchen, SFT-Dateien automatisch zu finden.</p></td>
</tr>
</tbody>
</table>



## Freigegebener Schlüssel


Der HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\softgrid\\4.5\\shared-Schlüssel steuert Werte, die für App-V-Komponenten freigegeben werden. Die folgende Tabelle enthält Informationen zu den Registrierungswerten, die mit dem freigegebenen Schlüssel verknüpft sind.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Name </th>
<th align="left">Typ </th>
<th align="left">Daten (Beispiele) </th>
<th align="left">Beschreibung </th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>DumpPath </p></td>
<td align="left"><p>Zeichenfolge </p></td>
<td align="left"><p>Standard = c-c </p></td>
<td align="left"><p>Standardpfad zum Erstellen von Speicherabbilddateien beim Generieren eines Mini Abbilds für eine Ausnahme. Dieser Standardwert ist "c". Wenn nicht angegeben. Der Client Installer legt diesen Schlüssel auf das &lt; globale Datenverzeichnis der APP-Virtualisierung fest &gt; \Dumps. Der Sequencer-Installer legt diesen Schlüssel auf das Installationsverzeichnis fest. </p></td>
</tr>
<tr class="even">
<td align="left"><p>DumpPathSizeLimit </p></td>
<td align="left"><p>DWORD </p></td>
<td align="left"><p>1000</p></td>
<td align="left"><p>Gibt die maximale Gesamtmenge an Speicherplatz in Megabyte an, die zum Speichern von Mini Abbildern verwendet werden kann. Standard = 1000 MB.</p></td>
</tr>
</tbody>
</table>



## Netzwerkschlüssel


Der HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\softgrid\\4.5\\client\\network-Schlüssel steuert eine Vielzahl von netzwerkbezogenen Parametern. Dieser Schlüssel wird in erster Linie vom Netzwerktransport-Agent verwendet. Die folgende Tabelle enthält Informationen zu den Registrierungswerten, die dem Netzwerkschlüssel zugeordnet sind.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Name </th>
<th align="left">Typ </th>
<th align="left">Daten (Beispiele) </th>
<th align="left">Beschreibung </th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Online</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Standard = 1</p></td>
<td align="left"><p>Aktiviert oder deaktiviert den Offlinemodus. Wenn der Wert auf 0 gesetzt ist, kommuniziert der Client nicht mit App-V-Verwaltungsservern oder Veröffentlichungsservern. Bei getrennten Vorgängen kann der Client eine geladene Anwendung starten, auch wenn Sie nicht mit einem App-V-Verwaltungs Server verbunden ist. Im Offlinemodus versucht der Client nicht, eine Verbindung zu einem App-V-Verwaltungsserver oder Veröffentlichungsserver herzustellen. Sie müssen getrennte Vorgänge zulassen, um offline arbeiten zu können. Der Standardwert ist 1 aktiviert (Online) und 0 ist deaktiviert (offline).</p></td>
</tr>
<tr class="even">
<td align="left"><p>AllowDisconnectedOperation </p></td>
<td align="left"><p>DWORD </p></td>
<td align="left"><p>Standard = 1</p></td>
<td align="left"><p>Aktiviert oder deaktiviert den getrennten Betrieb. Der Standardwert ist 1 aktiviert, und 0 ist deaktiviert. Wenn getrennte Vorgänge aktiviert sind, kann der APP-v-Client eine geladene Anwendung starten, auch wenn Sie nicht mit einem App-v-Verwaltungs Server verbunden ist.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>FastConnectTimeout</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Standard = 1000</p></td>
<td align="left"><p>Dieser Wert gibt das Timeout für TCP-Verbindungen in Millisekunden an, um zu bestimmen, wann der Modus für den getrennten Betrieb wechselt. Dieser Wert kann verwendet werden, um den standardmäßigen ConnectTimeout von 20 Sekunden (App-V Connect-Timeout für Netzwerktransaktionen) oder das TCP-Timeout des Systems von ca. 25 Sekunden zu überschreiben. Dadurch wird der Client schnell in den getrennten Betriebsmodus versetzt. Auf die nächste Verbindung angewendet.</p></td>
</tr>
<tr class="even">
<td align="left"><p>LimitDisconnectedOperation</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Standard = 1 </p></td>
<td align="left"><p>Nur anwendbar, wenn AllowDisconnectedOperation 1 ist, aktiviert. Dieser Wert bestimmt, ob es ein Zeitlimit für die Dauer des Client-Betriebs in getrennten Vorgängen geben wird. 1 = limitiert. 0 = unbegrenzt.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>DOTimeoutMinutes</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Standard = 129600</p></td>
<td align="left"><p>Gibt an, wie viele Minuten eine Anwendung im getrennten Betriebsmodus verwendet werden kann.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>Die gültigen Werte sind 1 – 999999 in Tagen, ausgedrückt in Minuten (1 – 1439998560 Minuten). Der Standardwert ist 90 Tage oder 129.600 Minuten.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Protokoll</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Standard = 8</p></td>
<td align="left"><p>Standardprotokoll für die Verwendung (TCP vs SSL). Im Dialog Feld "Optionen" konfigurieren.</p></td>
</tr>
<tr class="even">
<td align="left"><p>ReadTimeout</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>20</p></td>
<td align="left"><p>Lesen des Timeouts für Netzwerktransaktionen in Sekunden. Nicht ändern.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>WriteTimeout</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>20</p></td>
<td align="left"><p>Schreiben Sie Timeout für Netzwerktransaktionen in Sekunden. Nicht ändern.</p></td>
</tr>
<tr class="even">
<td align="left"><p>ConnectTimeout</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>20</p></td>
<td align="left"><p>Verbinden Sie das Timeout für Netzwerktransaktionen in Sekunden. Nicht ändern.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>ReestablishmentRetries</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>3</p></td>
<td align="left"><p>Die Anzahl der Versuche, eine gelöschte Sitzung wiederherzustellen.</p></td>
</tr>
<tr class="even">
<td align="left"><p>ReestablishmentInterval</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>15</p></td>
<td align="left"><p>Die Anzahl der Sekunden, zwischen denen versucht wird, eine gelöschte Sitzung wiederherzustellen.</p></td>
</tr>
</tbody>
</table>



## Http-Taste


Der HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\softgrid\\4.5\\client\\network\\http-Schlüssel steuert die Parameter, die sich auf HTTP-Streaming beziehen. Dieser Schlüssel wird hauptsächlich vom Netzwerktransport-Agent verwendet. Die folgende Tabelle enthält Informationen zu den Registrierungswerten, die dem http-Schlüssel zugeordnet sind.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Name </th>
<th align="left">Typ </th>
<th align="left">Daten (Beispiele) </th>
<th align="left">Beschreibung </th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>LaunchIfNotFound</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Standard = 0</p></td>
<td align="left"><p>Steuert das Verhalten des HTTP-Streaming, wenn eine Verbindung mit dem HTTP-Server hergestellt werden kann und die Paketdatei auf dem HTTP-Server nicht mehr vorhanden ist. Wenn der Wert nicht vorhanden ist oder nicht auf 1 festgesetzt ist, können Sie mit dem App-V-Client keine Anwendung starten, die zuvor in den Cache geladen wurde.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>1</p></td>
<td align="left"><p>Wenn dieser Wert auf 1 festgesetzt ist, können Sie mit dem App-V-Client eine Anwendung starten, die zuvor in den Cache geladen wurde.</p></td>
</tr>
</tbody>
</table>



## Datei System Schlüssel


Die Werte, die unter dem HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\softgrid\\4.5\\client\\appfs-Schlüssel enthalten sind, steuern die Dateisystemparameter für App-V. Die folgende Tabelle enthält Informationen zu den Registrierungswerten, die mit dem AppFS-Schlüssel verknüpft sind.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Name </th>
<th align="left">Typ </th>
<th align="left">Daten (Beispiele) </th>
<th align="left">Beschreibung </th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>FileSize </p></td>
<td align="left"><p>DWORD </p></td>
<td align="left"><p>4096</p></td>
<td align="left"><p>Maximale Größe in Megabytes der Dateisystemcache-Datei. Wenn Sie diesen Wert in der Registrierung ändern, müssen Sie den Zustand auf 0 festlegen und einen Neustart durchführen. </p></td>
</tr>
<tr class="even">
<td align="left"><p>FileName </p></td>
<td align="left"><p>Zeichenfolge </p></td>
<td align="left"><p>C:\Users\Public\Documents\SoftGrid Client\sftfs.fsd </p></td>
<td align="left"><p>Speicherort der Dateisystem-Cache-Datei. Wenn Sie diesen Wert in der Registrierung ändern, müssen Sie entweder die Dateigröße beibehalten und den Neustart durchführen oder den Status auf 0 festlegen und neu starten. </p></td>
</tr>
<tr class="odd">
<td align="left"><p>DriveLetter </p></td>
<td align="left"><p>Zeichenfolge </p></td>
<td align="left"><p>F: </p></td>
<td align="left"><p>Laufwerk, auf dem das App-V-Dateisystem bereitgestellt wird, sofern verfügbar. Dieser Wert wird entweder vom Listener oder vom Installationsprogramm gesetzt und vom Dateisystem gelesen. </p></td>
</tr>
<tr class="even">
<td align="left"><p>Status </p></td>
<td align="left"><p>DWORD </p></td>
<td align="left"><p>0x100 </p></td>
<td align="left"><p>Status des Dateisystems. Legen Sie den Wert 0 fest, und starten Sie den Dateisystemcache vollständig. </p></td>
</tr>
<tr class="odd">
<td align="left"><p>FileSystemStorage </p></td>
<td align="left"><p>Zeichenfolge </p></td>
<td align="left"><p>C:\Profiles\Joe\SG </p></td>
<td align="left"><p>Pfad für Symlinks, die unter HKCU. Ändern Sie nicht (verwenden Sie das Datenverzeichnis unter Konfiguration, um es zu ändern). </p></td>
</tr>
<tr class="even">
<td align="left"><p>GlobalFileSystemStorage </p></td>
<td align="left"><p>Zeichenfolge </p></td>
<td align="left"><p>C:\Users\Public\Documents\SoftGrid Client\AppFS-Speicher </p></td>
<td align="left"><p>Pfad für globale Dateisystem Daten. Nicht ändern. </p></td>
</tr>
<tr class="odd">
<td align="left"><p>MaxPercentToLockInCache </p></td>
<td align="left"><p>DWORD </p></td>
<td align="left"><p>Standard = 90 </p></td>
<td align="left"><p>Gibt den maximalen Prozentsatz der Dateisystem-Cachedatei an, die gesperrt werden kann. Nicht ändern.</p></td>
</tr>
<tr class="even">
<td align="left"><p>UnloadLeastRecentlyUsed</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Standard = 1</p></td>
<td align="left"><p>Das Speicher Verwaltungsfeature "Dateisystem-Cache" verwendet einen am wenigsten zuletzt verwendeten Algorithmus (LRU) und ist standardmäßig aktiviert. Wenn der Platz, der für ein neues Paket erforderlich ist, den verfügbaren freien Speicherplatz im Cache überschreitet, verwendet der App-V-Client dieses Feature, um zu ermitteln, welche, falls vorhanden, vorhandene Pakete aus dem Cache löschen können, um Platz für das neue Paket zu schaffen. Der Client löscht das Paket mit dem ältesten Datum des letzten Zugriffs, wenn es älter als der im Registrierungswert MinPkgAge angegebene Wert ist. Werte sind 0 (deaktiviert) und 1 (Standard, aktiviert).</p></td>
</tr>
<tr class="odd">
<td align="left"><p>MinPackageAge</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>1</p></td>
<td align="left"><p>Wenn Sie feststellen möchten, wann das Paket für verwerfen ausgewählt werden kann, legen Sie diesen Registrierungswert auf die minimale Anzahl von Tagen fest, die Sie verstreichen möchten, nachdem das Paket zuletzt zugegriffen wurde. Pakete, die in letzter Zeit verwendet wurden, werden nicht verworfen.</p></td>
</tr>
</tbody>
</table>



## Berechtigungsschlüssel


Um zu verhindern, dass Benutzer Fehler machen, können Administratoren den HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\softgrid\\4.5\\client\\permissions-Schlüssel verwenden, um den Zugriff auf einige Aktionen für nicht administrative Benutzer zu steuern, beispielsweise um zu verhindern, dass Benutzer versehentlich Programme entladen. Benutzer mit Administratorrechten können sich eine dieser Berechtigungen erteilen. Achten Sie bei freigegebenen Systemen wie einem Host für Remotedesktopsitzungen-Server (ehemals Terminal Server) auf die Verwendung von zusätzlichen Berechtigungen für Benutzer, da einige dieser Berechtigungen es Benutzern ermöglichen, die Anwendungen zu steuern, die von allen Benutzern im System verwendet werden. Mögliche Werte für diese Einstellungen sind 1 (Allow) und 0 (Disallow).

Die Einstellungen für den Berechtigungsschlüssel Steuern alle Schnittstellen, die die benannten Aktionen ermöglichen. Dazu gehören das Dialog Feld Optionen, SFTTray und SFTMime. Diese Einstellungen wirken sich nicht auf Administratoren aus. Die folgende Tabelle enthält Informationen zu den Registrierungswerten, die mit dem Berechtigungsschlüssel verknüpft sind.

Name Type Data (Beispiele) Beschreibung ChangeFSDrive

DWORD

Standard = 0

Der Wert 1 ermöglicht es Benutzern, einen anderen Laufwerkbuchstaben auszuwählen, der als Dateisystemlaufwerk verwendet werden soll.

ChangeCacheSize

DWORD

Standard = 0

Der Wert 1 ermöglicht Benutzern, die Cachegröße zu ändern.

ChangeLogSettings

DWORD

Standard = 0

Der Wert 1 ermöglicht Benutzern, die Protokollebene zu ändern, deren Speicherort zu ändern und Sie über die Benutzeroberfläche zurückzusetzen.

AddApp

DWORD

Standard = 0

Mit dem Wert 1 können Benutzer Anwendungen explizit hinzufügen. Dies wirkt sich nicht auf Anwendungen aus, die über die Veröffentlichungsaktualisierung hinzugefügt werden, und es wird verhindert, dass Benutzer Anwendungen starten (und dadurch implizit hinzufügen), die noch nicht hinzugefügt wurden. Werte sind 0 oder 1.

LoadApp 

DWORD 

0

Ermöglicht es einem Benutzer nicht, eine Anwendung zu laden. Dies ist die Standardeinstellung für Host für Remotedesktopsitzungen. Wenn Sie ein mobiler Benutzer sind, möchten Sie möglicherweise Ihre Anwendungen im Cache vollständig laden, um Sie während des getrennten Betriebs oder Offlinemodus zu verwenden. Damit Anwendungen vom APP-v-Verwaltungsserver oder vom APP-v-Streamingserver gestreamt werden können, müssen Sie mit einem Server verbunden sein, um Anwendungen zu laden.

1

Ermöglicht einem Benutzer das Laden einer Anwendung. Dies ist die Standardeinstellung für Windows-Desktops. 

UnloadApp 

DWORD 

0

Ermöglicht es einem Benutzer nicht, eine Anwendung zu entladen. Beim Laden oder Entladen eines Pakets werden alle Anwendungen im Paket in den Cache geladen oder daraus entfernt.

1

Ermöglicht es einem Benutzer, eine Anwendung zu entladen. 

LockApp 

DWORD 

0

Der Benutzer kann keine Anwendung sperren und entsperren. Dies ist die Standardeinstellung für Host für Remotedesktopsitzungen. Eine gesperrte Anwendung kann nicht aus dem Cache entfernt werden, um Platz für neue Anwendungen zu schaffen. Wenn Sie eine gesperrte Anwendung vom App-V-Desktop oder-Client für Remote Desktop Dienste (ehemals Terminal Dienste)-Cache entfernen möchten, müssen Sie die Sperre aufheben.

1

Ermöglicht einem Benutzer das Sperren und Entsperren einer Anwendung. Dies ist die Standardeinstellung für Windows-Desktops. 

ManageTypes 

DWORD 

0

Ermöglicht es einem Benutzer nicht, nur Dateitypzuordnungen für diesen Benutzer hinzuzufügen, zu bearbeiten oder zu entfernen. Dies ist die Standardeinstellung für Host für Remotedesktopsitzungen. 

1

Ermöglicht einem Benutzer das Hinzufügen, bearbeiten und Entfernen von Dateitypzuordnungen für diesen Benutzer und nicht global. Dies ist die Standardeinstellung für Windows-Desktops. 

RefreshServer 

DWORD 

0

Ermöglicht es einem Benutzer nicht, eine Aktualisierung der MIME-Einstellungen auszulösen. Dies ist die Standardeinstellung für Host für Remotedesktopsitzungen. 

1

Ermöglicht einem Benutzer das Auslösen einer Aktualisierung der MIME-Einstellungen. Dies ist die Standardeinstellung für Windows-Desktops. 

UpdateOSDFile

DWORD

Standard = 0

Der Wert 1 ermöglicht einem Benutzer die Verwendung einer geänderten OSD-Datei.

ImportApp 

DWORD 

0

Der Benutzer kann Anwendungen nicht in den Cache importieren. Der Unterschied zwischen laden und importieren besteht darin, dass der Client beim Auslösen einer Last das Paket von dem aktuell konfigurierten Speicherort erhält, der in der OSD-, ASR-oder override-URL enthalten ist. Bei Verwendung von Import muss ein Speicherort angegeben werden, von dem das Paket abgerufen werden soll. 

1

Ermöglicht es einem Benutzer, Anwendungen in den Cache zu importieren. 

ChangeRefreshSettings

DWORD

Standard = 0

Der Wert 1 ermöglicht Benutzern, die Aktualisierungseinstellungen für Server zu ändern (Aktualisierung bei der Anmeldung und periodische Aktualisierung). Dies bedeutet nicht, dass der Benutzer andere Servereinstellungen (Pfad, Host usw.) ändern kann.

ManageServers

DWORD

Standard = 0

Der Wert 1 ermöglicht dem Benutzer das Hinzufügen, bearbeiten und Entfernen von Servern, mit Ausnahme der Bearbeitung der Aktualisierungseinstellungen, die durch die ChangeRefreshSettings-Berechtigung gesteuert werden.

PublishShortcut

DWORD

Standard = 0

Der Wert 1 ermöglicht Benutzern das Veröffentlichen von Verknüpfungen über die Benutzeroberfläche. Dies wirkt sich nicht auf Tastenkombinationen aus, die während einer Veröffentlichungsaktualisierung veröffentlicht werden.

ViewAllApplications

DWORD

Standard = 0

Der Wert 1 zeigt alle Anwendungen über die Benutzeroberfläche an; Andernfalls werden nur die Anwendungen des Benutzers angezeigt.

RepairApp

DWORD

Standard = 1

Der Wert 1 ermöglicht es dem Benutzer, die Reparaturaktion für Anwendungen in SFTMime oder der Client Verwaltungskonsole zu verwenden. Wenn Sie eine Anwendung reparieren, werden alle benutzerdefinierten Benutzereinstellungen entfernt und die Standardeinstellungen wiederhergestellt. Mit dieser Aktion werden keine Verknüpfungen oder Dateitypzuordnungen geändert oder gelöscht, und die Anwendung wird nicht aus dem Cache entfernt.

ClearApp

DWORD

Standard = 1

Der Wert 1 ermöglicht es dem Benutzer, die klare Aktion für Anwendungen in SFTMime oder der Client Verwaltungskonsole zu verwenden. Wenn Sie eine Anwendung von der Konsole löschen, können Sie diese Anwendung nicht mehr verwenden. Die Anwendung verbleibt jedoch im Cache und steht weiterhin anderen Benutzern im gleichen System zur Verfügung. Nach einer Veröffentlichungsaktualisierung werden die gelöschten Anwendungen wieder zur Verfügung gestellt.

DeleteApp

DWORD

Standard = 0

Der Wert 1 ermöglicht es dem Benutzer, die Löschaktion für Anwendungen in SFTMime oder der Client Verwaltungskonsole zu verwenden. Wenn Sie eine Anwendung löschen, steht die ausgewählte Anwendung nicht mehr für alle Benutzer dieses Clients zur Verfügung. Verknüpfungen und Dateitypzuordnungen werden gelöscht, und die Anwendung wird aus dem Cache gelöscht. Wenn sich eine andere Anwendung jedoch auf Daten im Dateisystem-Cache oder auf Einstellungsdaten für die ausgewählte Anwendung bezieht, werden diese Elemente nicht gelöscht.

Nach einer Veröffentlichungsaktualisierung werden die gelöschten Anwendungen wieder zur Verfügung gestellt.

ToggleOfflineMode

DWORD

Mit dem Wert 1 können die Benutzer auswählen, dass der Client im Offline Modus ausgeführt werden soll. Im Offline Modus kann der Application Virtualization-Client eine geladene Anwendung starten, auch wenn Sie nicht mit einem Application Virtualization Server verbunden ist.



## Benutzerdefinierte Einstellungen


Der HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\softgrid\\4.5\\client\\customsettings-Schlüssel enthält Werte, die für Front-End-Komponenten spezifisch sind. Alle benutzerdefinierten Einstellungen werden als Zeichenfolgen gespeichert. Die folgende Tabelle enthält Informationen zu den Registrierungswerten, die mit dem CustomSettings-Schlüssel verknüpft sind.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Name </th>
<th align="left">Typ </th>
<th align="left">Daten (Beispiele) </th>
<th align="left">Beschreibung </th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>TrayErrorDelay </p></td>
<td align="left"><p>DWORD </p></td>
<td align="left"><p>Standard = 30 </p></td>
<td align="left"><p>Zeit in Sekunden, in der der Application Virtualization-Benachrichtigungsbereich Fehlermeldungen wie "starten" nicht angezeigt wird &quot; &quot; . Minimaler Wert von 1. </p></td>
</tr>
<tr class="even">
<td align="left"><p>TraySuccessDelay </p></td>
<td align="left"><p>DWORD </p></td>
<td align="left"><p>Standard = 10 </p></td>
<td align="left"><p>Zeit in Sekunden, in der im appvmed-Benachrichtigungsbereich Erfolgsmeldungen wie &quot; Word gestartet &quot; oder &quot; Excel heruntergefahren angezeigt werden &quot; . Wenn 0, werden diese Nachrichten unterdrückt. </p></td>
</tr>
<tr class="odd">
<td align="left"><p>TrayVisibility</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Standard = 0</p></td>
<td align="left"><p>0 = Anzeige Fach, wenn virtualisierte Anwendungen verwendet werden.</p>
<p>1 = Anzeige Fach immer anzeigen.</p>
<p>2 = niemals Fach anzeigen.</p></td>
</tr>
<tr class="even">
<td align="left"><p>TrayShowRefresh</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p></p></td>
<td align="left"><p>Wenn präsentieren und auf einen Wert von 1 gesetzt ist, kann die Aktualisierung von Menüelement Anwendungen im Menü "Taskleiste" angezeigt werden, und der Benutzer kann darauf zugreifen.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>TrayShowLoad</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p></p></td>
<td align="left"><p>Wenn Present und auf einen Wert von 1 gesetzt ist, können Menüelement Lade Anwendungen im Menü "Taskleiste" angezeigt werden, und der Benutzer kann darauf zugreifen.</p></td>
</tr>
</tbody>
</table>



## Berichterstellungseinstellungen


Der HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\softgrid\\4.5\\client\\reporting-Schlüssel enthält Werte, die für die Berichterstellung an einen App-V-Verwaltungs Server spezifisch sind. Die folgende Tabelle enthält Informationen zu den Registrierungswerten, die dem Berichterstattungs Schlüssel zugeordnet sind.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Name </th>
<th align="left">Typ </th>
<th align="left">Daten (Beispiele) </th>
<th align="left">Beschreibung </th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>DataCacheLimit</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Standard = 20</p></td>
<td align="left"><p>Dieser Wert gibt die maximale Größe in Megabyte (MB) des XML-Caches zum Speichern von Berichtsinformationen an. Die Größe bezieht sich auf den Cache im Arbeitsspeicher. Wenn das Limit erreicht ist, wird die Protokolldatei überschrieben. Wenn ein neuer Eintrag hinzugefügt wird (unten in der Liste), werden mindestens einer der ältesten Datensätze (oben in der Liste) gelöscht, um Platz zu schaffen. Beim ersten auftreten wird eine Warnung in das Client Protokoll und das Ereignisprotokoll protokolliert, und es wird erst wieder protokolliert, nachdem der Cache bei der Übertragung erfolgreich gelöscht wurde und das Protokoll erneut gefüllt wurde.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Datablocking</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Standard = 65536</p></td>
<td align="left"><p>Dieser Wert gibt die maximale Größe in Bytes an, die bei der Veröffentlichungsaktualisierung an den Server gesendet werden soll, um permanente Übertragungsfehler zu vermeiden, wenn das Protokoll eine signifikante Größe erreicht hat. Der Standardwert ist 65536. Wenn Berichtsdaten an den Server übertragen werden, wird ein Block von Anwendungsdatensätzen, die kleiner oder gleich der Blockgröße in Bytes von XML-Daten sind, aus dem Cache entfernt und an den Server gesendet. Jedem Block werden die allgemeinen Client Daten und die globalen Paket Listendaten vorangestellt, und diese werden nicht in die Berechnung der Blockgröße einbezogen; Es besteht die Möglichkeit, dass eine extrem große Paketliste zu Übertragungsfehlern bei geringer Bandbreite oder unzuverlässigen Verbindungen führt.</p></td>
</tr>
</tbody>
</table>



## Verwandte Themen


[Application Virtualization Client-Referenz](application-virtualization-client-reference.md)









