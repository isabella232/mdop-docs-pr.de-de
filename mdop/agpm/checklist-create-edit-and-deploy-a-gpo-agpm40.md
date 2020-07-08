---
title: 'Checkliste: erstellen, bearbeiten und Bereitstellen eines Gruppenrichtlinienobjekts'
description: 'Checkliste: erstellen, bearbeiten und Bereitstellen eines Gruppenrichtlinienobjekts'
author: dansimp
ms.assetid: 44631bed-16d2-4b5a-af70-17a73fb5f6af
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7d8bea9109040aa81a20df62356ef1d307d5eac0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807772"
---
# Prüfliste: Erstellen, Bearbeiten und Zerstören eines Gruppenrichtlinienobjekts


In einer Umgebung, in der mehrere Personengruppen Richtlinienobjekte (Group Policy Objects, GPOs) mithilfe der erweiterten Gruppenrichtlinienverwaltung (Group Policy Management, AGPM) ändern, delegiert ein AGPM-Administrator (Vollzugriff) die Berechtigung für Redakteure, Genehmiger und Prüfer entweder als Gruppen oder als Einzelpersonen. Im folgenden wird ein typischer GPO-Entwicklungsprozess für einen Editor und eine genehmigende Person beschrieben.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Aufgabe</th>
<th align="left">Verweis</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Der Editor fordert, dass ein neues Gruppenrichtlinienobjekt erstellt wird oder eine genehmigende Person ein neues Gruppenrichtlinienobjekt erstellt.</p></td>
<td align="left"><p><a href="request-the-creation-of-a-new-controlled-gpo-agpm40.md" data-raw-source="[Request the Creation of a New Controlled GPO](request-the-creation-of-a-new-controlled-gpo-agpm40.md)">Anfordern der Erstellung eines neuen gesteuerten Gruppenrichtlinienobjekts</a></p>
<p><a href="create-a-new-controlled-gpo-agpm40.md" data-raw-source="[Create a New Controlled GPO](create-a-new-controlled-gpo-agpm40.md)">Erstellen eines neuen gesteuerten Gruppenrichtlinienobjekts</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Genehmiger genehmigt die Erstellung des Gruppenrichtlinienobjekts, wenn es von einem Editor angefordert wurde.</p></td>
<td align="left"><p><a href="approve-or-reject-a-pending-action-agpm40.md" data-raw-source="[Approve or Reject a Pending Action](approve-or-reject-a-pending-action-agpm40.md)">Genehmigen oder Ablehnen einer ausstehenden Aktion</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Der Editor checkt eine Kopie des Gruppenrichtlinienobjekts aus dem Archiv aus, damit niemand anderes das Gruppenrichtlinienobjekt ändern kann. Der Editor nimmt Änderungen am GPO vor und überprüft dann das geänderte Gruppenrichtlinienobjekt in das Archiv.</p></td>
<td align="left"><p><a href="edit-a-gpo-offline-agpm40.md" data-raw-source="[Edit a GPO Offline](edit-a-gpo-offline-agpm40.md)">Offline-Bearbeitung eines Gruppenrichtlinienobjekts</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Bei der Entwicklung in einer Testgesamtstruktur exportiert der Editor das Gruppenrichtlinienobjekt in eine Datei, überträgt die Datei in die Produktionsgesamtstruktur und importiert die Datei. Darüber hinaus kann ein Editor das Gruppenrichtlinienobjekt mit einer Organisationseinheit verknüpfen, die Testcomputer und-Benutzer enthält.</p></td>
<td align="left"><p><a href="using-a-test-environment.md" data-raw-source="[Using a Test Environment](using-a-test-environment.md)">Verwenden einer Testumgebung</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Der Editor fordert die Bereitstellung des Gruppenrichtlinienobjekts in der Produktionsumgebung der Domäne an.</p></td>
<td align="left"><p><a href="request-deployment-of-a-gpo-agpm40.md" data-raw-source="[Request Deployment of a GPO](request-deployment-of-a-gpo-agpm40.md)">Anfordern der Bereitstellung eines Gruppenrichtlinienobjekts</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Überprüfer wie Genehmiger oder Bearbeiter analysieren das Gruppenrichtlinienobjekt.</p></td>
<td align="left"><p><a href="performing-reviewer-tasks-agpm40.md" data-raw-source="[Performing Reviewer Tasks](performing-reviewer-tasks-agpm40.md)">Durchführen von Prüferaufgaben</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Der Genehmiger genehmigt und stellt das Gruppenrichtlinienobjekt in der Produktionsumgebung der Domäne bereit oder lehnt das Gruppenrichtlinienobjekt ab.</p></td>
<td align="left"><p><a href="approve-or-reject-a-pending-action-agpm40.md" data-raw-source="[Approve or Reject a Pending Action](approve-or-reject-a-pending-action-agpm40.md)">Genehmigen oder Ablehnen einer ausstehenden Aktion</a></p></td>
</tr>
</tbody>
</table>

 

### Weitere Verweise

[Advanced Group Policy Management 4.0](advanced-group-policy-management-40.md)

 

 





