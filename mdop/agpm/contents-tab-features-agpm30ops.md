---
title: Features der Registerkarte „Inhalt“
description: Features der Registerkarte „Inhalt“
author: dansimp
ms.assetid: 725f025a-c30a-4d07-add1-4e0ed9a1a5fd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f64aad16a3335d78641812121692f6d5f6436ee1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807695"
---
# Features der Registerkarte „Inhalt“


Jede sekundäre Registerkarte auf der Registerkarte **Inhalt** enthält zwei Abschnitte:**Gruppenrichtlinienobjekte** und **Gruppen und Benutzer**.

## Abschnitt "Gruppenrichtlinienobjekte"


Im Abschnitt **Gruppenrichtlinienobjekte** wird eine gefilterte Liste der Gruppenrichtlinienobjekte (Group Policy Objects, GPOs) angezeigt, und es werden die folgenden Attribute für jedes GPO identifiziert:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">GPO-Attribut</th>
<th align="left">Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Name</strong></p></td>
<td align="left"><p>Der Name des Gruppenrichtlinienobjekts.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Status</strong></p></td>
<td align="left"><p>Der Status des ausgewählten Gruppenrichtlinienobjekts</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Geändert von</strong></p></td>
<td align="left"><p>Der Herausgeber, der eingecheckt hat, oder die genehmigende Person, die das ausgewählte Gruppenrichtlinienobjekt bereitgestellt hat.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Datum ändern</strong></p></td>
<td align="left"><p>Bei einem kontrollierten GPO das letzte Datum, an dem es eingecheckt wurde, nachdem es geändert oder ausgecheckt wurde, um geändert zu werden. Bei einem nicht kontrollierten Gruppenrichtlinienobjekt das Datum, an dem es zuletzt geändert wurde.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Kommentar</strong></p></td>
<td align="left"><p>Ein Kommentar, der von der Person eingegeben wurde, die zu dem Zeitpunkt, zu dem Sie geändert wurde, ein GPO eingecheckt oder bereitgestellt hat. Nützlich, um die Besonderheiten der Version zu identifizieren, falls ein Rollback auf eine vorherige Version erforderlich ist.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Computer Version</strong></p></td>
<td align="left"><p>Automatisch generierte Version des Computer Konfigurations Teils des Gruppenrichtlinienobjekts.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Benutzer Version</strong></p></td>
<td align="left"><p>Automatisch generierte Version des Benutzer Konfigurations Teils des Gruppenrichtlinienobjekts.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>GPO-Status</strong></p></td>
<td align="left"><p>Die Computer Konfiguration und die Benutzerkonfiguration können separat verwaltet werden. Der Status des Gruppenrichtlinienobjekts gibt an, welche Teile des Gruppenrichtlinienobjekts aktiviert sind.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>WMI-Filter</strong></p></td>
<td align="left"><p>Zeigen Sie alle WMI-Filter an, die auf dieses Gruppenrichtlinienobjekt angewendet werden. WMI-Filter werden in der <strong> </strong> Konsolenstruktur der GPMC unter dem Ordner WMI-Filter für die Domäne verwaltet.</p></td>
</tr>
</tbody>
</table>

 

## Abschnitt "Gruppen und Benutzer"


Wenn ein GPO ausgewählt ist, wird im Abschnitt **Gruppen und Benutzer** eine Liste der Gruppen und Benutzer angezeigt, die Zugriff auf das Gruppenrichtlinienobjekt haben. Die zulässigen Berechtigungen und die Vererbung werden für jede Gruppe oder jeden Benutzer angezeigt. Ein AGPM-Administrator kann Berechtigungen entweder mithilfe von standardmäßigen AGPM-Rollen (Editor, genehmigende Person, Bearbeiter und AGPM-Administrator) oder einer benutzerdefinierten Kombination von Berechtigungen konfigurieren.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Button</th>
<th align="left">Effekt</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Add</strong></p></td>
<td align="left"><p>Fügen Sie der Sicherheitsbeschreibung einen neuen Eintrag hinzu. Alle Benutzer oder Gruppen in Active Directory können hinzugefügt werden.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Entfernen</strong></p></td>
<td align="left"><p>Entfernen des ausgewählten Eintrags aus der Zugriffssteuerungsliste</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Eigenschaften</strong></p></td>
<td align="left"><p>Anzeigen der Eigenschaften für das ausgewählte Objekt Die Seite "Eigenschaften" wird für ein Objekt in <strong> Active Directory-Benutzer und-Computer angezeigt </strong> .</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Erweitert</strong></p></td>
<td align="left"><p>Öffnen Sie den Editor für die <strong> Zugriffssteuerungsliste </strong> .</p></td>
</tr>
</tbody>
</table>

 

### Weitere Überlegungen

-   Informationen zu Rollen und Berechtigungen, die sich auf bestimmte Aufgaben beziehen, finden Sie unter Ausführen von Aufgaben im Rahmen von [AGPM-Administratoren](performing-agpm-administrator-tasks-agpm30ops.md), Ausführen von [Editor Aufgaben](performing-editor-tasks-agpm30ops.md), Ausführen von [genehmigenden Aufgaben](performing-approver-tasks-agpm30ops.md)und [Ausführen von Aufgaben](performing-reviewer-tasks-agpm30ops.md)für Bearbeiter.

### Weitere Verweise

-   [Registerkarte "Inhalt"](contents-tab-agpm30ops.md)

 

 





