---
title: CONFIGURE PACKAGE
description: CONFIGURE PACKAGE
author: dansimp
ms.assetid: acc7eaa8-6ada-47b9-a655-2ca2537605b9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: dc8b315b68349cc9834316786b0bf15d4ac3c5cd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807871"
---
# CONFIGURE PACKAGE


Ermöglicht dem Benutzer das Ändern einer Paket Manifestdatei, einer Paketquelle, eines Load Trigger-Typs oder eines Lade Ziels für ein Paket.

`SFTMIME CONFIGURE PACKAGE:package-name [/MANIFEST manifest-path]                 [/OVERRIDEURL url] [/AUTOLOADNEVER] [/AUTOLOADONREFRESH]                 [/AUTOLOADONLOGIN] [/AUTOLOADONLAUNCH]                 [/AUTOLOADTARGET {NONE|ALL|PREVUSED}]                 [/LOG log-pathname | /CONSOLE | /GUI]                 [/NO-UPDATE-FTA-SHORTCUT {TRUE|FALSE} {/GLOBAL}]`

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
<td align="left"><p>/OVERRIDEURL- &lt; URL&gt;</p></td>
<td align="left"><p>Der Speicherort der SFT-Datei des Pakets.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/AUTOLOADNEVER</p></td>
<td align="left"><p>Das Laden des Hintergrunds ist für das Paket deaktiviert.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/AUTOLOADONREFRESH</p></td>
<td align="left"><p>Das Laden des Hintergrunds wird nach einer Veröffentlichungsaktualisierung ausgeführt.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/AUTOLOADONLOGIN</p></td>
<td align="left"><p>Das Laden des Hintergrunds wird durchgeführt, wenn sich ein Benutzer anmeldet.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/AUTOLOADONLAUNCH</p></td>
<td align="left"><p>Das Laden des Hintergrunds wird ausgeführt, nachdem ein Benutzer eine Anwendung aus dem Paket gestartet hat.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/AUTOLOADTARGET- &lt; Ziel&gt;</p></td>
<td align="left"><p>Gibt an, welche Anwendungen aus dem Paket automatisch geladen werden.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Keine</p></td>
<td align="left"><p>Trotz vorhanden sein von/AUTOLOADONxxx-Flags wird kein Autoloading durchgeführt.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Alle</p></td>
<td align="left"><p>Wenn ein automatischer Trigger aktiviert ist, werden alle Anwendungen im Paket in den Cache geladen, unabhängig davon, ob Sie jemals gestartet wurden.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>PREVUSED</p></td>
<td align="left"><p>Wenn ein automatischer Trigger aktiviert ist, wird das Paket geladen, wenn Anwendungen in diesem Paket zuvor von einem Benutzer gestartet wurden.</p></td>
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

 

Für Version 4.6 SP2 wurde die folgende Option hinzugefügt.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p>[/no-Update-FTA-Shortcut {true | FALSE} {/Global}]</p></td>
<td align="left"><p>Wenn der Wert auf true festgelegt ist, wird für das Paket entweder pro Benutzer oder Global ein Registrierungswert erstellt, wenn das/Global-Flag angegeben ist.</p>
<p>Wenn Sie auf false festgelegt ist, wird der Registrierungswert entfernt, und die Dateitypen Zuordnungen (FTA) für das Paket werden neu installiert.</p>
<p>Wenn keine Angabe erfolgt, tritt normales FTA-und Verknüpfungs Veröffentlichungsverhalten auf. Wenn Sie spätere Veröffentlichungs Aktualisierungsvorgänge auf dem App-V 4,6 SP2-Client ausführen, werden die Verknüpfungen und FTA für Pakete, deren Registrierungswert festgesetzt ist, nicht geändert, und die Verknüpfungen und Freihandelsabkommen werden beim Systemstart oder bei der Benutzeranmeldung nicht registriert, es sei denn, Sie setzen das Flag zurück.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/Global</p></td>
<td align="left"><p>Funktioniert in Verbindung mit dem/No-Update-FTA-Shortcut-Flag. Wenn das/Global-Flag vorhanden ist, gibt es an, dass ein Registrierungswert für dieses Paket für alle Benutzer erstellt wird. Standardmäßig wird der Registrierungswert nur für diesen Benutzer erstellt.</p></td>
</tr>
</tbody>
</table>

 

## Verwandte Themen


[SFTMIME-Befehlsreferenz](sftmime--command-reference.md)

 

 





