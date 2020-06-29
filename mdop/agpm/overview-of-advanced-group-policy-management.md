---
title: Übersicht über Advanced Group Policy Management
description: Übersicht über Advanced Group Policy Management
author: dansimp
ms.assetid: 028de9dd-848b-42bc-a982-65ba5c433772
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 38396de6bd8bdace72d3add1bba09769ae26de32
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809382"
---
# <span data-ttu-id="9bc4b-103">Übersicht über Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="9bc4b-103">Overview of Advanced Group Policy Management</span></span>


<span data-ttu-id="9bc4b-104">Sie können die erweiterte Gruppenrichtlinienverwaltung (Group Policy Management, AGPM) verwenden, um die Funktionen der Gruppenrichtlinien-Verwaltungskonsole (Group Policy Management Console, GPMC) zu erweitern und umfassende Änderungssteuerung und Erweiterte Verwaltung für Gruppenrichtlinienobjekte (Group Policy Objects, GPOs) bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="9bc4b-104">You can use Advanced Group Policy Management (AGPM) to extend the capabilities of the Group Policy Management Console (GPMC), providing comprehensive change control and enhanced management for Group Policy objects (GPOs).</span></span>

## <span data-ttu-id="9bc4b-105">Entwicklung von Gruppenrichtlinienobjekten mit Änderungssteuerung</span><span class="sxs-lookup"><span data-stu-id="9bc4b-105">Group Policy object development with change control</span></span>


<span data-ttu-id="9bc4b-106">Mit AGPM können Sie eine Kopie der einzelnen Gruppenrichtlinienobjekte in einem zentralen Archiv speichern, damit Gruppenrichtlinienadministratoren Sie offline anzeigen und ändern können, ohne die bereitgestellte Version des Gruppenrichtlinienobjekts unmittelbar zu beeinflussen.</span><span class="sxs-lookup"><span data-stu-id="9bc4b-106">With AGPM, you can store a copy of each GPO in a central archive, so Group Policy administrators can view and modify it offline without immediately impacting the deployed version of the GPO.</span></span> <span data-ttu-id="9bc4b-107">Darüber hinaus speichert AGPM eine Kopie jeder Version jedes gesteuerten Gruppenrichtlinienobjekts im Archiv, sodass Sie bei Bedarf eine frühere Version wiederherstellen können.</span><span class="sxs-lookup"><span data-stu-id="9bc4b-107">Additionally, AGPM stores a copy of each version of each controlled GPO in the archive so that you can roll back to an earlier version if needed.</span></span>

<span data-ttu-id="9bc4b-108">Die Begriffe "Einchecken" und "Auschecken" werden auf die gleiche Weise wie in einer Bibliothek (oder in Anwendungen, die Änderungssteuerung, Versionskontrolle oder Quellcodeverwaltung für die Programmierungs Entwicklung bereitstellen) verwendet.</span><span class="sxs-lookup"><span data-stu-id="9bc4b-108">The terms "check in" and "check out" are used in much the same way as in a library (or in applications that provide change control, version control, or source code control for programming development).</span></span> <span data-ttu-id="9bc4b-109">Wenn Sie ein Buch in einer Bibliothek verwenden möchten, können Sie es in der Bibliothek Auschecken.</span><span class="sxs-lookup"><span data-stu-id="9bc4b-109">To use a book that is in a library, you check it out from the library.</span></span> <span data-ttu-id="9bc4b-110">Niemand sonst kann es verwenden, wenn es ausgecheckt ist. Wenn Sie das Buch nicht mehr haben, können Sie es wieder in die Bibliothek einchecken, damit es von anderen verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="9bc4b-110">No one else can use it while you have it checked out. When you are finished with the book, you check it back into the library, so others can use it.</span></span>

<span data-ttu-id="9bc4b-111">Bei der Entwicklung von GPOs mithilfe von AGPM:</span><span class="sxs-lookup"><span data-stu-id="9bc4b-111">When developing GPOs using AGPM:</span></span>

1.  <span data-ttu-id="9bc4b-112">Erstellen eines neuen kontrollierten Gruppenrichtlinienobjekts oder Steuern eines zuvor unkontrollierten Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="9bc4b-112">Create a new controlled GPO or control a previously uncontrolled GPO.</span></span>

2.  <span data-ttu-id="9bc4b-113">Überprüfen Sie das Gruppenrichtlinienobjekt, damit Sie und nur Sie es ändern können.</span><span class="sxs-lookup"><span data-stu-id="9bc4b-113">Check out the GPO, so you and only you can modify it.</span></span>

3.  <span data-ttu-id="9bc4b-114">Bearbeiten Sie das Gruppenrichtlinienobjekt.</span><span class="sxs-lookup"><span data-stu-id="9bc4b-114">Edit the GPO.</span></span>

4.  <span data-ttu-id="9bc4b-115">Überprüfen Sie das bearbeitete GPO, damit es von anderen geändert oder bereitgestellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="9bc4b-115">Check in the edited GPO, so others can modify it, or so it can be deployed.</span></span>

5.  <span data-ttu-id="9bc4b-116">Überprüfen Sie die Änderungen.</span><span class="sxs-lookup"><span data-stu-id="9bc4b-116">Review the changes.</span></span>

6.  <span data-ttu-id="9bc4b-117">Stellen Sie das Gruppenrichtlinienobjekt in der Produktionsumgebung bereit.</span><span class="sxs-lookup"><span data-stu-id="9bc4b-117">Deploy the GPO to the production environment.</span></span>

## <span data-ttu-id="9bc4b-118">Rollenbasierte Delegierung</span><span class="sxs-lookup"><span data-stu-id="9bc4b-118">Role-based delegation</span></span>


<span data-ttu-id="9bc4b-119">AGPM bietet eine umfassende, einfach zu verwendende rollenbasierte Delegierung.</span><span class="sxs-lookup"><span data-stu-id="9bc4b-119">AGPM provides comprehensive, easy-to-use role-based delegation.</span></span> <span data-ttu-id="9bc4b-120">Berechtigungen auf Domänenebene ermöglichen AGPM-Administratoren den Zugriff auf einzelne Domänen, ohne Zugriff auf andere Domänen zu gewähren.</span><span class="sxs-lookup"><span data-stu-id="9bc4b-120">Domain-level permissions allow AGPM Administrators to provide access to individual domains without providing access to other domains.</span></span> <span data-ttu-id="9bc4b-121">Mithilfe der GPO-basierten Delegierung können AGPM-Administratoren nur Zugriff auf bestimmte GPOs zulassen.</span><span class="sxs-lookup"><span data-stu-id="9bc4b-121">GPO-based delegation enables AGPM Administrators to allow access only to specific GPOs.</span></span>

<span data-ttu-id="9bc4b-122">In AGPM gibt es speziell definierte Rollen: AGPM-Administrator (Vollzugriff), genehmigende Person, Editor und Bearbeiter.</span><span class="sxs-lookup"><span data-stu-id="9bc4b-122">Within AGPM, there are specifically defined roles: AGPM Administrator (Full Control), Approver, Editor, and Reviewer.</span></span> <span data-ttu-id="9bc4b-123">Die Rolle AGPM-Administrator umfasst die Berechtigungen für alle anderen Rollen.</span><span class="sxs-lookup"><span data-stu-id="9bc4b-123">The AGPM Administrator role includes the permissions for all other roles.</span></span> <span data-ttu-id="9bc4b-124">Standardmäßig haben nur genehmigende Personen die Möglichkeit, GPOs in der Produktionsumgebung bereitzustellen, um die Umgebung vor unbeabsichtigten Fehlern durch die wenig erfahrenen Editoren zu schützen.</span><span class="sxs-lookup"><span data-stu-id="9bc4b-124">By default, only Approvers have the power to deploy GPOs to the production environment, protecting the environment from inadvertent mistakes by less experienced Editors.</span></span> <span data-ttu-id="9bc4b-125">Standardmäßig umfassen alle Rollen auch die Rolle Prüfer und damit die Möglichkeit, die GPO-Einstellungen in Berichten anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="9bc4b-125">Also by default, all roles include the Reviewer role and therefore the ability to view GPO settings in reports.</span></span> <span data-ttu-id="9bc4b-126">AGPM bietet jedoch einem AGPM-Administrator die Flexibilität, den Zugriff auf Gruppenrichtlinienobjekte so anzupassen, dass Sie den Anforderungen Ihrer Organisation entsprechen.</span><span class="sxs-lookup"><span data-stu-id="9bc4b-126">However, AGPM provides an AGPM Administrator with the flexibility to customize GPO access to fit the needs of your organization.</span></span>

## <span data-ttu-id="9bc4b-127">Delegierung in einer mehr Gruppenrichtlinien-Administratorumgebung</span><span class="sxs-lookup"><span data-stu-id="9bc4b-127">Delegation in a multiple Group Policy administrator environment</span></span>


<span data-ttu-id="9bc4b-128">In einer Umgebung, in der mehrere Personen Änderungen an GPOs vornehmen, delegiert ein AGPM-Administrator die Berechtigung für Redakteure, Genehmiger und Prüfer, entweder als Gruppen oder als Einzelpersonen.</span><span class="sxs-lookup"><span data-stu-id="9bc4b-128">In an environment where multiple people make changes to GPOs, an AGPM Administrator delegates permission to Editors, Approvers, and Reviewers, either as groups or as individuals.</span></span> <span data-ttu-id="9bc4b-129">Einen typischen Entwicklungsprozess für Gruppenrichtlinienobjekte für einen Editor und eine genehmigende Person finden Sie unter [Checkliste: erstellen, bearbeiten und Bereitstellen eines Gruppenrichtlinienobjekts](checklist-create-edit-and-deploy-a-gpo.md).</span><span class="sxs-lookup"><span data-stu-id="9bc4b-129">For a typical GPO development process for an Editor and an Approver, see [Checklist: Create, Edit, and Deploy a GPO](checklist-create-edit-and-deploy-a-gpo.md).</span></span>

### <span data-ttu-id="9bc4b-130">Weitere Verweise</span><span class="sxs-lookup"><span data-stu-id="9bc4b-130">Additional references</span></span>

-   [<span data-ttu-id="9bc4b-131">Prüfliste: Erstellen, Bearbeiten und Zerstören eines Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="9bc4b-131">Checklist: Create, Edit, and Deploy a GPO</span></span>](checklist-create-edit-and-deploy-a-gpo.md)

-   [<span data-ttu-id="9bc4b-132">Durchführen von AGPM-Administratoraufgaben</span><span class="sxs-lookup"><span data-stu-id="9bc4b-132">Performing AGPM Administrator Tasks</span></span>](performing-agpm-administrator-tasks.md)

-   [<span data-ttu-id="9bc4b-133">Durchführen von Editor-Aufgaben</span><span class="sxs-lookup"><span data-stu-id="9bc4b-133">Performing Editor Tasks</span></span>](performing-editor-tasks.md)

-   [<span data-ttu-id="9bc4b-134">Durchführen der Aufgaben von genehmigenden Personen</span><span class="sxs-lookup"><span data-stu-id="9bc4b-134">Performing Approver Tasks</span></span>](performing-approver-tasks.md)

-   [<span data-ttu-id="9bc4b-135">Durchführen von Prüferaufgaben</span><span class="sxs-lookup"><span data-stu-id="9bc4b-135">Performing Reviewer Tasks</span></span>](performing-reviewer-tasks.md)

-   [<span data-ttu-id="9bc4b-136">Problembehandlung bei Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="9bc4b-136">Troubleshooting Advanced Group Policy Management</span></span>](troubleshooting-advanced-group-policy-management.md)

-   [<span data-ttu-id="9bc4b-137">Benutzeroberfläche: Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="9bc4b-137">User Interface: Advanced Group Policy Management</span></span>](user-interface-advanced-group-policy-management.md)

 

 





