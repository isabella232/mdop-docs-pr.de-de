---
title: UNPUBLISH PACKAGE
description: UNPUBLISH PACKAGE
author: dansimp
ms.assetid: 1651427c-72a5-4701-bb57-71e14a7a3803
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7704fb3ed03be4864a837767d9e890d28b63f175
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806184"
---
# UNPUBLISH PACKAGE


Ermöglicht Ihnen, die Verknüpfungen und Dateitypen für ein gesamtes Paket zu entfernen.

`SFTMIME UNPUBLISH PACKAGE:package-name [/CLEAR] [/GLOBAL]                 [/LOG log-pathname | /CONSOLE | /GUI]`

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
<td align="left"><p>Der Name des Pakets.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/Clear</p></td>
<td align="left"><p>Falls vorhanden, werden die Benutzereinstellungen ebenfalls entfernt. (Weitere Informationen finden Sie weiter unten in diesem Thema unter wichtige Hinweise.)</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/Global</p></td>
<td align="left"><p>Falls vorhanden, wird das Paket für alle Benutzer auf diesem Computer unveröffentlicht.</p></td>
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

 

**Wichtig**  Bevor Sie den Befehl " **Paket veröffentlichen** " ausführen können, muss das Paket bereits dem Application Virtualization-Client hinzugefügt worden sein.

Zur Verwendung von " **Global**" muss " **veröffentlichungspaket** aufheben" als lokaler Administrator ausgeführt werden. Andernfalls ist nur **ClearApp** -Berechtigung erforderlich.

Bei Verwendung von "nicht **veröffentlichen** " mit " **Global** " werden alle globalen Dateitypen und Tastenkombinationen für das Paket entfernt. **Clear** ist nicht anwendbar.

Bei Verwendung von " **UNPUBLISH-Paket** ohne **Global** " werden die Benutzer Verknüpfungen und Dateitypen für das Paket entfernt, und wenn **Clear** festgesetzt ist, werden auch Benutzereinstellungen entfernt und Hintergrund Lasten unter dem Kontext des Benutzers angehalten.

Das **Paket "Veröffentlichung** aufheben" funktioniert in Anwendungen mit dem gleichen Paketnamen oder der gleichen GUID, die als Quell-ID für das **Add**-, **Edit**-und **Publish-Paket**verwendet wurden.

Das **Paket "Veröffentlichung** aufheben" löscht immer alle Benutzereinstellungen, Verknüpfungen und Dateitypen, unabhängig von der Verwendung des/Clear-Schalters.

 

## Verwandte Themen


[SFTMIME-Befehlsreferenz](sftmime--command-reference.md)

 

 





