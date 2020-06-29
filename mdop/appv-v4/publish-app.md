---
title: PUBLISH APP
description: PUBLISH APP
author: dansimp
ms.assetid: f25f06a8-ca23-435b-a0c2-16a5f39b6b97
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b2ccb19255786ee47a8356feef14be1c4d9b4fb2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806459"
---
# PUBLISH APP


Veröffentlicht eine Anwendungsverknüpfung im Startmenü, auf dem Desktop oder an einem anderen angegebenen Speicherort des Benutzers.

`SFTMIME PUBLISH APP:application                 {/DESKTOP | /START | /TARGET target-path} [/ICON icon-pathname]                 [/DISPLAY display-name] [/ARGS command-args...]                 [/LOG log-pathname | /CONSOLE | /GUI]`

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
<td align="left"><p>Anwendung: &lt; Anwendung&gt;</p></td>
<td align="left"><p>Der Name und die Version (optional) der Anwendung.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/Desktop</p></td>
<td align="left"><p>Veröffentlicht eine Verknüpfung auf dem Desktop des Benutzers.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/Start</p></td>
<td align="left"><p>Veröffentlicht eine Verknüpfung im Ordner "Application Virtualization Applications" im Ordner "Programme" des Menüs "Start".</p></td>
</tr>
<tr class="even">
<td align="left"><p>/Target &lt; -Zielpfad&gt;</p></td>
<td align="left"><p>Der absolute Pfad, in dem die Verknüpfung veröffentlicht werden soll.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/Icon &lt; -Symbolpfadname&gt;</p></td>
<td align="left"><p>Der Pfad oder die URL für die Symboldatei.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Names &lt; -Anzeigename&gt;</p></td>
<td align="left"><p>Der Anzeigename für die Verknüpfung.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/ARGS &lt; Command-args&gt;</p></td>
<td align="left"><p>Parameter, die an die Anwendung übergeben werden sollen.</p></td>
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

 

 





