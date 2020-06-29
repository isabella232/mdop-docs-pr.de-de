---
title: SFTTRAY-Befehlsreferenz
description: SFTTRAY-Befehlsreferenz
author: dansimp
ms.assetid: 6fa3a939-b047-4d6c-bd1d-dfb93e065eb2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 45a664b91ff7edd5f8536f035417cc3b0f52d7ca
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806272"
---
# SFTTRAY-Befehlsreferenz


Die Microsoft Application Virtualization (app-v)-Client Fachanwendung, sfttray.exe, ist das Hauptelement der Benutzeroberfläche des App-v-Clients, mit dem Benutzer während der normalen Verwendung interagieren können. Dieses Programm steuert das Streaming und den Start aller virtuellen Anwendungen und wird aufgerufen, indem Sie mit der rechten Maustaste auf das im Infobereich angezeigte Symbol klicken, um das Menü der Clientfunktionen anzuzeigen. Das Menü ermöglicht es dem Benutzer, Anwendungen zu laden, eine Veröffentlichungsaktualisierung zu starten, eine Anforderung abzubrechen oder den Client in den Offlinemodus zu ändern. Der Benutzer kann auch die Application Virtualization Client Tray-Anwendung und alle aktiven Anwendungen schließen, indem Sie auf **Beenden**klicken.

Standardmäßig wird das Symbol immer dann angezeigt, wenn eine virtuelle Anwendung gestartet wird, obwohl Sie dieses Verhalten mithilfe von SFTTRAY-Befehlen steuern können. Die Application Virtualization Client Tray-Anwendung zeigt auch eine Statusleiste für jede gestartete Anwendung sowie Statusmeldungen zu aktiven Anwendungen an. Durch Klicken auf die Statusleiste wird eine Meldung angezeigt, die es Ihnen ermöglicht, das Laden oder Starten einer Anwendung abzubrechen.

## SFTTRAY-Befehle


Die Liste der Befehle und Befehlszeilenoptionen kann angezeigt werden, indem Sie den folgenden Befehl in einem Befehlsfenster ausführen.

**Hinweis:**  
Es gibt nur eine Instanz der Application Virtualization-Client Taskleiste für jeden Benutzerkontext, wenn Sie also einen neuen SFTTRAY-Befehl starten, wird er an das Programm weitergeleitet, das bereits ausgeführt wird.



`Sfttray.exe /?`

### Befehlsverwendung

`Sfttray.exe [/HIDE | /SHOW]`

`Sfttray.exe [/HIDE | /SHOW] [/QUIET] [/EXE alternate-exe] /LAUNCH app [args]`

`Sfttray.exe [/HIDE | /SHOW] [/QUIET] /LOAD app [/SFTFILE sft]`

`Sfttray.exe [/HIDE | /SHOW] [/QUIET] /LOADALL`

`Sfttray.exe [/HIDE | /SHOW] [/QUIET] /REFRESHALL`

`Sfttray.exe [/HIDE | /SHOW] [/QUIET] /LAUNCHRESULT <UNIQUE ID>  /LAUNCH app [args]`

`Sfttray.exe /EXIT`

### Befehlszeilenoptionen

Die SFTTRAY-Befehlszeilenoptionen werden in der folgenden Tabelle beschrieben.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Schalter</th>
<th align="left">Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>/Hide</p></td>
<td align="left"><p>Blendet das SFTTRAY-Symbol im Windows-Benachrichtigungsbereich aus.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/Show</p></td>
<td align="left"><p>Zeigt das SFTTRAY-Symbol im Windows-Infobereich an.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/Quiet</p></td>
<td align="left"><p>Unterstützt die unbeaufsichtigte Verwendung, indem Fehler beim Anzeigen von Meldungsfeldern verhindert werden, die eine Benutzerbestätigung erfordern.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/EXE &lt; Alternate-exe&gt;</p></td>
<td align="left"><p>Wird mit/Launch verwendet, um anzugeben, dass ein ausführbares Programm in der virtuellen Umgebung gestartet werden soll, wenn anstelle der im OSD angegebenen Ziel Datei eine virtuelle Anwendung gestartet wird.</p>
<div class="alert">
<strong>Hinweis:</strong><br/><p>Verwenden Sie beispielsweise "SFTTRAY.EXE/exe REGEDIT.EXE/Launch- &lt; app", damit &gt; Sie die Registrierung der virtuellen Umgebung untersuchen können, in der die Anwendung ausgeführt wird.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p>/Launch- &lt; App &gt; [ &lt; args &gt; ]</p></td>
<td align="left"><p>Startet eine virtuelle Anwendung. Geben Sie den Namen und die Version einer Anwendung oder den Pfad zu einer OSD-Datei an. Optional können Befehlszeilenargumente an die virtuelle Anwendung übergeben werden.</p>
<div class="alert">
<strong>Hinweis:</strong><br/><p>Verwenden Sie den Befehl "SFTMIME.EXE/Query obj: App/Short", um eine Liste der Namen und Versionen der verfügbaren virtuellen Anwendungen zu erhalten.</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>/Load</p></td>
<td align="left"><p>Lädt oder importiert eine virtuelle Anwendung.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/LOADALL</p></td>
<td align="left"><p>Lädt alle Anwendungen in den Cache.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/REFRESHALL</p></td>
<td align="left"><p>Startet eine Veröffentlichungsaktualisierung für alle Anwendungen.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>&lt;eindeutige/LAUNCHRESULT-ID&gt;</p></td>
<td align="left"><p>Gibt den Startcode für den Start des Prozesses zurück, der sfttray.exe mithilfe eines globalen Ereignisses und einer Speicher zugeordneten Datei startet, die auf dem angegebenen Stammnamen für die eindeutige ID basieren. ¹</p></td>
</tr>
<tr class="even">
<td align="left"><p>/SFTFILE &lt; SFT&gt;</p></td>
<td align="left"><p>Optionaler Schalter, der mit/Load verwendet wird, um den Pfad zur SFT-Datei der Anwendung anzugeben. Wenn angegeben, wird die Anwendung importiert und nicht geladen.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/EXIT</p></td>
<td align="left"><p>Schließt das SFTTRAY-Programm und alle aktiven virtuellen Anwendungen und entfernt das Symbol aus dem Windows-Benachrichtigungsbereich.</p></td>
</tr>
</tbody>
</table>



**Hinweis:**  
¹ der */LAUNCHRESULT* -Befehlszeilenparameter bietet eine Möglichkeit für den Prozess, mit dem sfttray.exe gestartet wird, um den Stammnamen für ein globales Ereignis und eine Speicher zugeordnete Datei anzugeben, die verwendet wird, um den Start Ergebniscode an den Prozess zurückzugeben. Der Name des eindeutigen Bezeichners sollte mit "SFT-" beginnen, um zu verhindern, dass der Ereignisname virtualisiert wird, wenn der Startvorgang innerhalb einer virtuellen Umgebung aufgerufen wird. Der Speicher zugeordnete Bereich ist 64 Bits groß.

Um diesen Parameter zu verwenden, erstellt der Startvorgang ein Ereignis mit dem Namen " &lt; eindeutige ID &gt; -Ergebnis \ _Event", eine Speicher zugeordnete Datei mit dem Namen " &lt; eindeutige ID &gt; -Ergebnis \ _Value" und optional ein Ereignis mit dem Namen " &lt; Unique ID &gt; -Shutdown \ _Event", und der Startvorgang startet sfttray.exe und wartet darauf, dass das Ereignis signalisiert wird. Nachdem das Ereignis " &lt; eindeutige ID &gt; -Ergebnis \ _Event" signalisiert wurde, ruft der Startprozess den 64-Bit-Rückgabecode aus dem zugeordneten Speicherbereich ab.

Wenn das optionale Ereignis " &lt; eindeutige ID &gt; -Shutdown \ _Event" vorhanden ist, wenn die virtuelle Anwendung beendet wird, wird das Ereignis sfttray.exe geöffnet und signalisiert. Der Startprozess wartet auf dieses Shutdown-Ereignis, wenn es ermitteln muss, wann die virtuelle Anwendung beendet wird.











