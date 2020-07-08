---
title: Allgemeine sekundäre Registerkarten-Features
description: Allgemeine sekundäre Registerkarten-Features
author: dansimp
ms.assetid: 44a15c28-944c-49c1-8534-115ce1c362ed
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 546fd4c91e060a5595b6c848015290882de933b6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807767"
---
# Allgemeine sekundäre Registerkarten-Features


Jede sekundäre Registerkarte hat zwei Abschnitte:**Gruppenrichtlinienobjekte** und **Gruppen und Benutzer**.

## Abschnitt "Gruppenrichtlinienobjekte"


Im Abschnitt **Gruppenrichtlinienobjekte** wird eine gefilterte Liste der Gruppenrichtlinienobjekte (Group Policy Objects, GPOs) angezeigt, und es werden die folgenden Merkmale für jedes GPO identifiziert:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">GPO-Merkmal</th>
<th align="left">Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Name</strong></p></td>
<td align="left"><p>Der Name des Gruppenrichtlinienobjekts.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Computer (Comp.)</strong></p></td>
<td align="left"><p>Automatisch generierte Version des Computer Konfigurations Teils des Gruppenrichtlinienobjekts.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Benutzer</strong></p></td>
<td align="left"><p>Automatisch generierte Version des Benutzer Konfigurations Teils des Gruppenrichtlinienobjekts.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Status</strong></p></td>
<td align="left"><p>Der Status des ausgewählten Gruppenrichtlinienobjekts:</p>
<p><img src="images/36f6b687-f5cc-40d1-805f-b191d1fb1ace.gif" alt="Deployed GPO icon" /> <strong>Unkontrolliert: </strong> nicht von AGPM verwaltet.</p>
<p><img src="images/57b610a5-1c71-4d26-9173-d04abd495fcc.gif" alt="Checked in GPO icon" /> <strong>Eingecheckt: </strong> verfügbar für autorisierte Editoren zum Auschecken zur Bearbeitung oder zum Bereitstellen eines Gruppenrichtlinienadministrators.</p>
<p><img src="images/8e7a7c4e-809a-435a-8b29-30d797936210.gif" alt="Checked out GPO icon" /> <strong>Ausgecheckt: </strong> derzeit bearbeitet. Für andere Bearbeiter nicht verfügbar, bis der Herausgeber ausgecheckt hat oder ein AGPM-Administrator ihn überprüft hat.</p>
<p><img src="images/0840a6a3-54a6-4528-98a9-7b122243c1a5.gif" alt="Pending GPO icon" /> <strong>Ausstehend: </strong> wartet auf die Genehmigung eines Gruppenrichtlinienadministrators, bevor er erstellt, gesteuert, bereitgestellt oder gelöscht wird.</p>
<p><img src="images/57b610a5-1c71-4d26-9173-d04abd495fcc.gif" alt="Checked in GPO icon" /> <strong>Gelöscht: </strong> aus dem Archiv gelöscht, aber weiterhin in der Lage, wiederhergestellt zu werden.</p>
<p><img src="images/9b65829d-253c-4f30-9295-c816a6521ed2.gif" alt="Template icon" /> <strong>Vorlage: </strong> eine statische Version eines GPO zur Verwendung als Ausgangspunkt beim Erstellen neuer GPOs.</p>
<p><img src="images/cd349b8d-c4d8-45ff-b17f-7db882502c58.gif" alt="Default template icon" /> <strong>Vorlage (Standard): </strong> Diese Vorlage ist standardmäßig der Ausgangspunkt, der beim Erstellen eines neuen Gruppenrichtlinienobjekts verwendet wird.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>GPO-Status</strong></p></td>
<td align="left"><p>Die Computer Konfiguration und die Benutzerkonfiguration können separat verwaltet werden. Der Status des Gruppenrichtlinienobjekts gibt an, welche Teile des Gruppenrichtlinienobjekts aktiviert sind.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>WMI-Filter</strong></p></td>
<td align="left"><p>Zeigen Sie alle WMI-Filter an, die auf dieses Gruppenrichtlinienobjekt angewendet werden. WMI-Filter werden unter dem <strong> WMI </strong> -Filterknoten für die Domäne in der Konsolenstruktur der GPMC verwaltet.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Geändert</strong></p></td>
<td align="left"><p>Bei einem kontrollierten Gruppenrichtlinienobjekt das letzte Datum, an dem es eingecheckt wurde, nachdem es geändert oder ausgecheckt wurde. Bei einem nicht kontrollierten Gruppenrichtlinienobjekt das Datum, an dem es zuletzt geändert wurde.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Besitzer</strong></p></td>
<td align="left"><p>Der Herausgeber, der eingecheckt hat, oder die genehmigende Person, die das ausgewählte Gruppenrichtlinienobjekt bereitgestellt hat.</p></td>
</tr>
</tbody>
</table>

 

## Abschnitt "Gruppen und Benutzer"


Wenn ein GPO ausgewählt ist, wird im Abschnitt **Gruppen und Benutzer** eine Liste der Gruppen und Benutzer angezeigt, die Zugriff auf das Gruppenrichtlinienobjekt haben. Die zulässigen Berechtigungen und die Vererbung werden für jede Gruppe oder jeden Benutzer angezeigt. Ein AGPM-Administrator kann Berechtigungen entweder mithilfe von standardmäßigen AGPM-Rollen (Editor, genehmigende Person und Bearbeiter) oder einer benutzerdefinierten Kombination von Berechtigungen konfigurieren.

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

-   Informationen zu Rollen und Berechtigungen, die sich auf bestimmte Aufgaben beziehen, finden Sie unter Ausführen von Aufgaben im Rahmen von [AGPM-Administratoren](performing-agpm-administrator-tasks.md), Ausführen von [Editor Aufgaben](performing-editor-tasks.md), Ausführen von [genehmigenden Aufgaben](performing-approver-tasks.md)und [Ausführen von Aufgaben](performing-reviewer-tasks.md)für Bearbeiter.

### Weitere Verweise

-   [Registerkarte "Inhalt"](contents-tab.md)

 

 





