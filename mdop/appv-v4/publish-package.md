---
title: PUBLISH PACKAGE
description: PUBLISH PACKAGE
author: dansimp
ms.assetid: a33e72dd-194f-4283-8e99-4584ab13de53
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 00b63389986f495d9405939245a50575bae453f9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806456"
---
# PUBLISH PACKAGE


Veröffentlicht den Inhalt eines gesamten Pakets.

`SFTMIME PUBLISH PACKAGE:package-name /MANIFEST manifest-path [/GLOBAL]                 [/LOG log-pathname | /CONSOLE | /GUI]`

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
<td align="left"><p>Der Pfad oder die URL der Manifestdatei, in der die im Paket enthaltenen Anwendungen sowie alle Veröffentlichungsinformationen aufgelistet sind.</p></td>
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

 

**Wichtig**  Das Paket muss dem Application Virtualization-Client bereits hinzugefügt worden sein, und die Manifestdatei ist erforderlich.

Um den Parameter **Global** verwenden zu können, muss der Befehl Paket veröffentlichen als lokaler Administrator ausgeführt werden. Andernfalls werden nur **ManageTypes** -und **PublishShortcut** -Berechtigungen benötigt.

Durch die Veröffentlichung ohne den **globalen** Parameter wird dem Benutzer der Zugriff auf die Anwendungen im Paket gewährt, und die im Manifest aufgelisteten Dateitypen und Verknüpfungen werden im Profil des Benutzers veröffentlicht.

Durch die Veröffentlichung mit dem Parameter **Global** werden die im Manifest aufgelisteten Dateitypen und Tastenkombinationen dem Profil "alle Benutzer" hinzugefügt.

Wenn das Paket nicht global ist, bevor der Anruf und der **globale** Parameter verwendet werden, wird das Paket Global und allen Benutzern zur Verfügung gestellt.

 

## Verwandte Themen


[SFTMIME-Befehlsreferenz](sftmime--command-reference.md)

 

 





