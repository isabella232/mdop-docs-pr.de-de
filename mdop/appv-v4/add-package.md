---
title: ADD PACKAGE
description: ADD PACKAGE
author: dansimp
ms.assetid: aa83928d-a234-4395-831e-2a7ef786ff53
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 925349ce5bdf041b6a8768b5413692966e1cfc1e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809331"
---
# ADD PACKAGE


Fügt einen Paket Eintrag hinzu. Wenn das Paket bereits vorhanden ist, wird mit diesem Befehl die Konfiguration des vorhandenen Pakets aktualisiert.

`SFTMIME ADD PACKAGE:package-name /MANIFEST manifest-path                 [/OVERRIDEURL url [/AUTOLOADONREFRESH] [/AUTOLOADONLOGIN]                 [/AUTOLOADONLAUNCH] [/AUTOLOADTARGET {NONE|ALL|PREVUSED}]                 [/GLOBAL] [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Parameter</th>
<th align="left">Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Paket: &lt; Package-Name&gt;</p></td>
<td align="left"><p>Benutzersicht barer und benutzerfreundlicher Name für das Paket.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/Manifest &lt; -Manifest-Pfad&gt;</p></td>
<td align="left"><p>Der Pfad der Manifestdatei, in der die im Paket enthaltenen Anwendungen sowie alle Veröffentlichungsinformationen aufgelistet sind.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/OVERRIDEURL- &lt; URL&gt;</p></td>
<td align="left"><p>Der Speicherort der SFT-Datei des Pakets.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/AUTOLOADONREFRESH</p></td>
<td align="left"><p>Das Laden des Hintergrunds wird nach einer Veröffentlichungsaktualisierung ausgeführt.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/AUTOLOADONLOGIN</p></td>
<td align="left"><p>Das Laden des Hintergrunds wird durchgeführt, wenn sich ein Benutzer anmeldet.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/AUTOLOADONLAUNCH</p></td>
<td align="left"><p>Das Laden des Hintergrunds wird ausgeführt, nachdem ein Benutzer eine Anwendung aus dem Paket gestartet hat.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/AUTOLOADTARGET-Ziel</p></td>
<td align="left"><p>Gibt an, welche Anwendungen aus dem Paket automatisch geladen werden.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Keine</p></td>
<td align="left"><p>Trotz des Vorhandenseins von/AUTOLOADONxxx-Flags wird kein Autoloading durchgeführt.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Alle</p></td>
<td align="left"><p>Wenn ein automatischer Trigger aktiviert ist, werden alle Anwendungen im Paket in den Cache geladen, unabhängig davon, ob Sie zuvor gestartet wurden.</p></td>
</tr>
<tr class="even">
<td align="left"><p>PREVUSED</p></td>
<td align="left"><p>Wenn ein automatischer Trigger aktiviert ist, wird das Paket geladen, wenn Anwendungen in diesem Paket zuvor von einem Benutzer gestartet wurden.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/Global</p></td>
<td align="left"><p>Falls vorhanden, ist das Paket für alle Benutzer auf diesem Computer verfügbar.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/Log</p></td>
<td align="left"><p>Wenn angegeben, wird die Ausgabe mit dem angegebenen Pfadnamen protokolliert.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/Console</p></td>
<td align="left"><p>Wenn angegeben, wird die Ausgabe im aktiven Konsolenfenster angezeigt (Standardeinstellung).</p></td>
</tr>
<tr class="even">
<td align="left"><p>/GUI</p></td>
<td align="left"><p>Wenn angegeben, wird die Ausgabe in einem Windows-Dialogfeld angezeigt.</p></td>
</tr>
</tbody>
</table>

 

Für Version 4.6 wurde die folgende Option hinzugefügt.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p>/LOGU</p></td>
<td align="left"><p>Wenn angegeben, wird die Ausgabe mit dem angegebenen Pfadname im Unicode-Format protokolliert.</p></td>
</tr>
</tbody>
</table>

 

## Verwandte Themen


[SFTMIME-Befehlsreferenz](sftmime--command-reference.md)

 

 





