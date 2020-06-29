---
title: 'Checkliste: erstellen, bearbeiten und Bereitstellen eines Gruppenrichtlinienobjekts'
description: 'Checkliste: erstellen, bearbeiten und Bereitstellen eines Gruppenrichtlinienobjekts'
author: dansimp
ms.assetid: 614e2d9a-c18b-4f62-99fd-e17a2ac8559d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c79fefaa65c138372ebee00b769ccc5243142e22
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807776"
---
# <span data-ttu-id="1d7d1-103">Prüfliste: Erstellen, Bearbeiten und Zerstören eines Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="1d7d1-103">Checklist: Create, Edit, and Deploy a GPO</span></span>


<span data-ttu-id="1d7d1-104">In einer Umgebung, in der mehrere Personen Änderungen an Gruppenrichtlinienobjekten (Group Policy Objects, GPOs) vornehmen, delegiert ein AGPM-Administrator (Vollzugriff) die Berechtigung für Redakteure, Genehmiger und Prüfer, entweder als Gruppen oder als Einzelpersonen.</span><span class="sxs-lookup"><span data-stu-id="1d7d1-104">In an environment where multiple people make changes to Group Policy objects (GPOs), an AGPM Administrator (Full Control) delegates permission to Editors, Approvers, and Reviewers, either as groups or as individuals.</span></span> <span data-ttu-id="1d7d1-105">Im folgenden wird ein typischer GPO-Entwicklungsprozess für einen Editor und eine genehmigende Person beschrieben.</span><span class="sxs-lookup"><span data-stu-id="1d7d1-105">The following is a typical GPO development process for an Editor and an Approver.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="1d7d1-106">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="1d7d1-106">Task</span></span></th>
<th align="left"><span data-ttu-id="1d7d1-107">Verweis</span><span class="sxs-lookup"><span data-stu-id="1d7d1-107">Reference</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1d7d1-108">Der Editor fordert die Erstellung eines neuen Gruppenrichtlinienobjekts an, oder eine genehmigende Person erstellt ein neues Gruppenrichtlinienobjekt.</span><span class="sxs-lookup"><span data-stu-id="1d7d1-108">Editor requests the creation of a new GPO or an Approver creates a new GPO.</span></span></p></td>
<td align="left"><p><a href="request-the-creation-of-a-new-controlled-gpo.md" data-raw-source="[Request the Creation of a New Controlled GPO](request-the-creation-of-a-new-controlled-gpo.md)"><span data-ttu-id="1d7d1-109">Anfordern der Erstellung eines neuen gesteuerten Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="1d7d1-109">Request the Creation of a New Controlled GPO</span></span></a></p>
<p><a href="create-a-new-controlled-gpo.md" data-raw-source="[Create a New Controlled GPO](create-a-new-controlled-gpo.md)"><span data-ttu-id="1d7d1-110">Erstellen eines neuen gesteuerten Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="1d7d1-110">Create a New Controlled GPO</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1d7d1-111">Genehmiger genehmigt die Erstellung des Gruppenrichtlinienobjekts, wenn es von einem Editor angefordert wurde.</span><span class="sxs-lookup"><span data-stu-id="1d7d1-111">Approver approves the creation of the GPO if it was requested by an Editor.</span></span></p></td>
<td align="left"><p><a href="approve-or-reject-a-pending-action.md" data-raw-source="[Approve or Reject a Pending Action](approve-or-reject-a-pending-action.md)"><span data-ttu-id="1d7d1-112">Genehmigen oder Ablehnen einer ausstehenden Aktion</span><span class="sxs-lookup"><span data-stu-id="1d7d1-112">Approve or Reject a Pending Action</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1d7d1-113">Der Editor checkt eine Kopie des Gruppenrichtlinienobjekts aus dem Archiv aus, sodass niemand anderes das Gruppenrichtlinienobjekt ändern kann.</span><span class="sxs-lookup"><span data-stu-id="1d7d1-113">Editor checks out a copy of the GPO from the archive, so no one else can modify the GPO.</span></span> <span data-ttu-id="1d7d1-114">Der Editor nimmt Änderungen am GPO vor und überprüft dann das geänderte Gruppenrichtlinienobjekt in das Archiv.</span><span class="sxs-lookup"><span data-stu-id="1d7d1-114">Editor makes changes to the GPO, and then checks the modified GPO into the archive.</span></span></p></td>
<td align="left"><p><a href="edit-a-gpo-offline.md" data-raw-source="[Edit a GPO Offline](edit-a-gpo-offline.md)"><span data-ttu-id="1d7d1-115">Offline-Bearbeitung eines Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="1d7d1-115">Edit a GPO Offline</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1d7d1-116">Der Editor fordert die Bereitstellung des Gruppenrichtlinienobjekts in der Produktionsumgebung an.</span><span class="sxs-lookup"><span data-stu-id="1d7d1-116">Editor requests deployment of the GPO to the production environment.</span></span></p></td>
<td align="left"><p><a href="request-deployment-of-a-gpo.md" data-raw-source="[Request Deployment of a GPO](request-deployment-of-a-gpo.md)"><span data-ttu-id="1d7d1-117">Anfordern der Bereitstellung eines Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="1d7d1-117">Request Deployment of a GPO</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1d7d1-118">Überprüfer wie Genehmiger oder Bearbeiter analysieren das Gruppenrichtlinienobjekt.</span><span class="sxs-lookup"><span data-stu-id="1d7d1-118">Reviewers, such as Approvers or Editors, analyze the GPO.</span></span></p></td>
<td align="left"><p><a href="performing-reviewer-tasks.md" data-raw-source="[Performing Reviewer Tasks](performing-reviewer-tasks.md)"><span data-ttu-id="1d7d1-119">Durchführen von Prüferaufgaben</span><span class="sxs-lookup"><span data-stu-id="1d7d1-119">Performing Reviewer Tasks</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1d7d1-120">Der Genehmiger genehmigt und stellt das Gruppenrichtlinienobjekt in der Produktionsumgebung bereit oder lehnt das Gruppenrichtlinienobjekt ab.</span><span class="sxs-lookup"><span data-stu-id="1d7d1-120">Approver approves and deploys the GPO to the production environment or rejects the GPO.</span></span></p></td>
<td align="left"><p><a href="approve-or-reject-a-pending-action.md" data-raw-source="[Approve or Reject a Pending Action](approve-or-reject-a-pending-action.md)"><span data-ttu-id="1d7d1-121">Genehmigen oder Ablehnen einer ausstehenden Aktion</span><span class="sxs-lookup"><span data-stu-id="1d7d1-121">Approve or Reject a Pending Action</span></span></a></p></td>
</tr>
</tbody>
</table>

 

 

 





