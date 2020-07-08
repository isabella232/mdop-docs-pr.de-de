---
title: ADD TYPE
description: ADD TYPE
author: dansimp
ms.assetid: 8f1d3978-9977-4851-9f46-fee6aefa3535
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4d2dcfb24a32dc733aa91b5534e0011090ef12b9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809322"
---
# ADD TYPE


Fügt die angegebene Dateitypzuordnung hinzu.

`SFTMIME ADD TYPE:file-extension /APP application [/ICON icon-pathname]                 [/DESCRIPTION type-desc] [/CONTENT-TYPE content-type] [/GLOBAL]                 [/PERCEIVED-TYPE perceived-type] [/PROGID progid]                 [/CONFIRMOPEN {YES|NO}] [/SHOWEXT {YES|NO}]                 [/NEWMENU {YES|NO}]  [/LOG log-pathname | /CONSOLE | /GUI]`

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
<td align="left"><p>Typ: &lt; Dateierweiterung&gt;</p></td>
<td align="left"><p>Die Dateinamenerweiterung, die der angegebenen Anwendung zugeordnet wird.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/APP- &lt; Anwendung&gt;</p></td>
<td align="left"><p>Der Name und die Version (optional) der Anwendung.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/Icon &lt; -Symbolpfadname&gt;</p></td>
<td align="left"><p>Der Pfad oder die URL für die Symboldatei.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/Description &lt; -Typ-DESC&gt;</p></td>
<td align="left"><p>Der benutzerfreundliche Name für den Dateityp. Standardmäßig wird die &quot; Erweiterungsdatei verwendet.&quot;</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/Content-Type &lt; -Inhaltstyp&gt;</p></td>
<td align="left"><p>Der Inhaltstyp der Datei. Standardmäßig wird &quot; Application/Softricity-Extension verwendet.&quot;</p></td>
</tr>
<tr class="even">
<td align="left"><p>/Global</p></td>
<td align="left"><p>Falls vorhanden, ist das Paket für alle Benutzer auf diesem Computer verfügbar.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/Perceived-Type &lt; wahrgenommen-Typ&gt;</p></td>
<td align="left"><p>Der wahrgenommene Typ der Datei. Der Standardwert ist Nothing.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/ProgID- &lt; ProgID&gt;</p></td>
<td align="left"><p>Der programmgesteuerte Bezeichner für den Dateityp. Standardmäßig wird die APP virt. Extension. File verwendet.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/CONFIRMOPEN</p></td>
<td align="left"><p>Gibt an, ob Benutzer, die eine Datei dieses Typs herunterladen, aufgefordert werden, die Datei zu öffnen oder zu speichern. Standardwert ist "Ja".</p></td>
</tr>
<tr class="even">
<td align="left"><p>/SHOWEXT</p></td>
<td align="left"><p>Gibt an, ob die Dateierweiterung immer angezeigt werden soll, auch wenn der Benutzer angefordert hat, dass alle Erweiterungen ausgeblendet werden. Standardmäßig auf Nein.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/NEWMENU</p></td>
<td align="left"><p>Gibt an, ob dem neuen Menü der Shell ein Eintrag hinzugefügt werden soll <strong> </strong> . Standardmäßig auf Nein.</p></td>
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

 

 





