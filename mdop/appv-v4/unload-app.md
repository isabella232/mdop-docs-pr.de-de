---
title: UNLOAD APP
description: UNLOAD APP
author: dansimp
ms.assetid: f0d729ae-8772-498b-be11-1a4b35499c53
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f1ae30f5b8c788f8763c2c2b9d1c1956182750d3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806192"
---
# UNLOAD APP


Entlädt die Anwendung und alle anderen Anwendungen im Paket aus dem Dateisystemcache.

`SFTMIME UNLOAD APP:application [/LOG log-pathname | /CONSOLE | /GUI]`

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
<td align="left"><p>App: &lt; Anwendung&gt;</p></td>
<td align="left"><p>Der Name und die Version (optional) der zu entladenden Anwendung.</p></td>
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

 

 





