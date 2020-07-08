---
title: ADD SERVER
description: ADD SERVER
author: dansimp
ms.assetid: 4be2ac2e-a410-4711-9f84-f305393c8fa7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e15a5943b40e14b2f9031bf8b3ddffa693e32dea
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808087"
---
# ADD SERVER


Fügt einen Veröffentlichungsserver hinzu.

`SFTMIME ADD SERVER:server-name /HOST hostname /TYPE {HTTP|RTSP}                 /PATH path [/PORT port] [/REFRESH {ON|OFF}] [/SECURE]                 [/LOG log-pathname | /CONSOLE | /GUI]`

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
<td align="left"><p>Server: &lt; Servername&gt;</p></td>
<td align="left"><p>Der Anzeigename für den Veröffentlichungsserver.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/Host &lt; Hostname&gt;</p></td>
<td align="left"><p>Der Hostname oder die IP-Adresse des Veröffentlichungsservers.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/Type {http | RTSP</p></td>
<td align="left"><p>Gibt an, ob es sich bei dem Veröffentlichungsserver um einen Webserver ( &quot; http &quot; ) oder einen Application Virtualization Server ( &quot; RTSP &quot; ) handelt.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/Port- &lt; Port&gt;</p></td>
<td align="left"><p>Der Port, auf dem der Veröffentlichungsserver lauscht. Standardmäßig wird 80 für normale HTTP-Server, 443 für http-Server mit erweiterter Sicherheit, 554 für normale Application Virtualization-Server und 322 für Server mit erweiterter Sicherheit verwendet.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/Path- &lt; Pfad&gt;</p></td>
<td align="left"><p>Der Pfadabschnitt der in einer Veröffentlichungsanforderung verwendeten URL. Wenn der Parameter Type auf RTSP eingestellt ist, ist der Pfad optional und standardmäßig auf &quot; / &quot; .</p></td>
</tr>
<tr class="even">
<td align="left"><p>/Refresh</p></td>
<td align="left"><p>Wenn die Einstellung auf ein gesetzt ist, werden Veröffentlichungsinformationen aktualisiert, wenn sich der Benutzer anmeldet. Standardmäßig auf ein.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/Secure</p></td>
<td align="left"><p>Gibt an, dass eine Verbindung mit erweiterter Sicherheit auf dem Veröffentlichungsserver eingerichtet werden sollte.</p></td>
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

 

 





