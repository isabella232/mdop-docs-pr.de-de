---
title: Prüfliste für das Auswerten von branchspezifischen Anwendungen für UE-V 1.0
description: Prüfliste für das Auswerten von branchspezifischen Anwendungen für UE-V 1.0
author: dansimp
ms.assetid: 3bfaab30-59f7-4099-abb1-d248ce0086b8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 133bc5d195763b7281fd8d152e153231ac4c4d47
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811767"
---
# Prüfliste für das Auswerten von branchspezifischen Anwendungen für UE-V 1.0


Wenn Sie auswerten möchten, welche Branchenanwendungen in Ihre UE-V-Bereitstellung einbezogen werden sollen, sollten Sie Folgendes berücksichtigen:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left">Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Enthält diese Anwendung Einstellungen, die vom Benutzer angepasst werden können?</p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Ist es wichtig, dass der Benutzer diese Einstellungen durchstreift?</p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Werden diese Benutzereinstellungen bereits von einer Anwendungs Verwaltungs-oder Einstellungsrichtlinien Lösung verwaltet? UE-V wendet Anwendungseinstellungen beim Start von Anwendungen und Windows-Einstellungen bei Anmeldung, entsperren oder Remote Verbindungsereignissen an. Wenn Sie UE-V mit anderen Einstellungen-Richtlinien Lösungen verwenden, kann es vorkommen, dass Benutzer in Roaming-Einstellungen inkonsistent sind.</p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Sind die Anwendungseinstellungen für den Computer spezifisch? Anwendungseinstellungen und Anpassungen, die Hardware oder bestimmten Computerkonfigurationen zugeordnet sind, werden nicht konsistent in Sitzungen durchlaufen und können zu einer unzureichenden Anwendungsumgebung führen.</p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Speichert die Anwendung die Einstellungen im Verzeichnis "Programme" oder im Dateiverzeichnis, das sich im <strong> </strong> Verzeichnis Benutzer \ [Benutzername] \ <strong> AppData LocalLow befindet </strong>  \  <strong> </strong> ? Anwendungsdaten, die an einem dieser Speicherorte gespeichert sind, sollten normalerweise nicht mit dem Benutzer Roaming durchlaufen, da diese Daten für den Computer spezifisch sind oder weil die Daten für die Roaming-Datei zu groß sind.</p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Speichert die Anwendung alle Einstellungen in einer Datei, die andere Anwendungsdaten enthält, die nicht durchlaufen werden sollen? UE-V synchronisiert Dateien als einzelne Einheit. Wenn Einstellungen in Dateien gespeichert werden, die Anwendungsdaten außer Einstellungen enthalten, kann das Synchronisieren dieser zusätzlichen Daten zu einer unzureichenden Anwendungsumgebung führen.</p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Wie groß sind die Dateien, die die Einstellungen enthalten? Die Leistung der Synchronisierung von Einstellungen kann von umfangreichen Dateien beeinflusst werden. Das einbeziehen großer Dateien kann sich auf die Leistung der Synchronisierung von Einstellungen auswirken.</p></td>
</tr>
</tbody>
</table>

 

## Verwandte Themen


[Planen für UE-V-Konfigurationsmethoden](planning-for-ue-v-configuration-methods.md)

[Planen für UE-V 1.0](planning-for-ue-v-10.md)

 

 





