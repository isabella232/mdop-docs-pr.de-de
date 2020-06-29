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
# <span data-ttu-id="840b6-103">Prüfliste: Erstellen, Bearbeiten und Zerstören eines Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="840b6-103">Checklist: Create, Edit, and Deploy a GPO</span></span>


<span data-ttu-id="840b6-104">In einer Umgebung, in der mehrere Personengruppen Richtlinienobjekte (Group Policy Objects, GPOs) mithilfe der erweiterten Gruppenrichtlinienverwaltung (Group Policy Management, AGPM) ändern, delegiert ein AGPM-Administrator (Vollzugriff) die Berechtigung für Redakteure, Genehmiger und Prüfer entweder als Gruppen oder als Einzelpersonen.</span><span class="sxs-lookup"><span data-stu-id="840b6-104">In an environment where multiple people change Group Policy Objects (GPOs) by using Advanced Group Policy Management (AGPM), an AGPM Administrator (Full Control) delegates permission to Editors, Approvers, and Reviewers either as groups or as individuals.</span></span> <span data-ttu-id="840b6-105">Im folgenden wird ein typischer GPO-Entwicklungsprozess für einen Editor und eine genehmigende Person beschrieben.</span><span class="sxs-lookup"><span data-stu-id="840b6-105">The following is a typical GPO development process for an Editor and an Approver.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="840b6-106">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="840b6-106">Task</span></span></th>
<th align="left"><span data-ttu-id="840b6-107">Verweis</span><span class="sxs-lookup"><span data-stu-id="840b6-107">Reference</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="840b6-108">Der Editor fordert, dass ein neues Gruppenrichtlinienobjekt erstellt wird oder eine genehmigende Person ein neues Gruppenrichtlinienobjekt erstellt.</span><span class="sxs-lookup"><span data-stu-id="840b6-108">Editor requests that a new GPO be created or an Approver creates a new GPO.</span></span></p></td>
<td align="left"><p><a href="request-the-creation-of-a-new-controlled-gpo-agpm40.md" data-raw-source="[Request the Creation of a New Controlled GPO](request-the-creation-of-a-new-controlled-gpo-agpm40.md)"><span data-ttu-id="840b6-109">Anfordern der Erstellung eines neuen gesteuerten Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="840b6-109">Request the Creation of a New Controlled GPO</span></span></a></p>
<p><a href="create-a-new-controlled-gpo-agpm40.md" data-raw-source="[Create a New Controlled GPO](create-a-new-controlled-gpo-agpm40.md)"><span data-ttu-id="840b6-110">Erstellen eines neuen gesteuerten Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="840b6-110">Create a New Controlled GPO</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="840b6-111">Genehmiger genehmigt die Erstellung des Gruppenrichtlinienobjekts, wenn es von einem Editor angefordert wurde.</span><span class="sxs-lookup"><span data-stu-id="840b6-111">Approver approves the creation of the GPO if it was requested by an Editor.</span></span></p></td>
<td align="left"><p><a href="approve-or-reject-a-pending-action-agpm40.md" data-raw-source="[Approve or Reject a Pending Action](approve-or-reject-a-pending-action-agpm40.md)"><span data-ttu-id="840b6-112">Genehmigen oder Ablehnen einer ausstehenden Aktion</span><span class="sxs-lookup"><span data-stu-id="840b6-112">Approve or Reject a Pending Action</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="840b6-113">Der Editor checkt eine Kopie des Gruppenrichtlinienobjekts aus dem Archiv aus, damit niemand anderes das Gruppenrichtlinienobjekt ändern kann.</span><span class="sxs-lookup"><span data-stu-id="840b6-113">Editor checks out a copy of the GPO from the archive so that no one else can modify the GPO.</span></span> <span data-ttu-id="840b6-114">Der Editor nimmt Änderungen am GPO vor und überprüft dann das geänderte Gruppenrichtlinienobjekt in das Archiv.</span><span class="sxs-lookup"><span data-stu-id="840b6-114">Editor makes changes to the GPO, and then checks the modified GPO into the archive.</span></span></p></td>
<td align="left"><p><a href="edit-a-gpo-offline-agpm40.md" data-raw-source="[Edit a GPO Offline](edit-a-gpo-offline-agpm40.md)"><span data-ttu-id="840b6-115">Offline-Bearbeitung eines Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="840b6-115">Edit a GPO Offline</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="840b6-116">Bei der Entwicklung in einer Testgesamtstruktur exportiert der Editor das Gruppenrichtlinienobjekt in eine Datei, überträgt die Datei in die Produktionsgesamtstruktur und importiert die Datei.</span><span class="sxs-lookup"><span data-stu-id="840b6-116">If developing in a test forest, Editor exports the GPO to a file, transfers the file to the production forest, and imports the file.</span></span> <span data-ttu-id="840b6-117">Darüber hinaus kann ein Editor das Gruppenrichtlinienobjekt mit einer Organisationseinheit verknüpfen, die Testcomputer und-Benutzer enthält.</span><span class="sxs-lookup"><span data-stu-id="840b6-117">Additionally, an Editor can link the GPO to an organizational unit that contains test computers and users.</span></span></p></td>
<td align="left"><p><a href="using-a-test-environment.md" data-raw-source="[Using a Test Environment](using-a-test-environment.md)"><span data-ttu-id="840b6-118">Verwenden einer Testumgebung</span><span class="sxs-lookup"><span data-stu-id="840b6-118">Using a Test Environment</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="840b6-119">Der Editor fordert die Bereitstellung des Gruppenrichtlinienobjekts in der Produktionsumgebung der Domäne an.</span><span class="sxs-lookup"><span data-stu-id="840b6-119">Editor requests deployment of the GPO to the production environment of the domain.</span></span></p></td>
<td align="left"><p><a href="request-deployment-of-a-gpo-agpm40.md" data-raw-source="[Request Deployment of a GPO](request-deployment-of-a-gpo-agpm40.md)"><span data-ttu-id="840b6-120">Anfordern der Bereitstellung eines Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="840b6-120">Request Deployment of a GPO</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="840b6-121">Überprüfer wie Genehmiger oder Bearbeiter analysieren das Gruppenrichtlinienobjekt.</span><span class="sxs-lookup"><span data-stu-id="840b6-121">Reviewers, such as Approvers or Editors, analyze the GPO.</span></span></p></td>
<td align="left"><p><a href="performing-reviewer-tasks-agpm40.md" data-raw-source="[Performing Reviewer Tasks](performing-reviewer-tasks-agpm40.md)"><span data-ttu-id="840b6-122">Durchführen von Prüferaufgaben</span><span class="sxs-lookup"><span data-stu-id="840b6-122">Performing Reviewer Tasks</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="840b6-123">Der Genehmiger genehmigt und stellt das Gruppenrichtlinienobjekt in der Produktionsumgebung der Domäne bereit oder lehnt das Gruppenrichtlinienobjekt ab.</span><span class="sxs-lookup"><span data-stu-id="840b6-123">Approver approves and deploys the GPO to the production environment of the domain or rejects the GPO.</span></span></p></td>
<td align="left"><p><a href="approve-or-reject-a-pending-action-agpm40.md" data-raw-source="[Approve or Reject a Pending Action](approve-or-reject-a-pending-action-agpm40.md)"><span data-ttu-id="840b6-124">Genehmigen oder Ablehnen einer ausstehenden Aktion</span><span class="sxs-lookup"><span data-stu-id="840b6-124">Approve or Reject a Pending Action</span></span></a></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="840b6-125">Weitere Verweise</span><span class="sxs-lookup"><span data-stu-id="840b6-125">Additional references</span></span>

[<span data-ttu-id="840b6-126">Advanced Group Policy Management 4.0</span><span class="sxs-lookup"><span data-stu-id="840b6-126">Advanced Group Policy Management 4.0</span></span>](advanced-group-policy-management-40.md)

 

 





