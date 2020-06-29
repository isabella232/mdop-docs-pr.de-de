---
title: Übersicht über Advanced Group Policy Management
description: Übersicht über Advanced Group Policy Management
author: dansimp
ms.assetid: 2c12f3b4-8472-4c5b-b7f8-1c98a80d6b47
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 94e47075ae865096f9fe7d327cc7b11cb54217d6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809385"
---
# <span data-ttu-id="6be42-103">Übersicht über Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="6be42-103">Overview of Advanced Group Policy Management</span></span>


<span data-ttu-id="6be42-104">Mithilfe der erweiterten Gruppenrichtlinienverwaltung (Group Policy Management, AGPM) können Sie die Funktionen der Gruppenrichtlinien-Verwaltungskonsole (Group Policy Management Console, GPMC) erweitern, um umfassende Änderungssteuerung und verbesserte Verwaltung für Gruppenrichtlinienobjekte (Group Policy Objects, GPOs) bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="6be42-104">You can use Advanced Group Policy Management (AGPM) to extend the capabilities of the Group Policy Management Console (GPMC) to provide comprehensive change control and improved management for Group Policy Objects (GPOs).</span></span>

## <span data-ttu-id="6be42-105">Entwicklung von Gruppenrichtlinienobjekten mit Änderungssteuerung</span><span class="sxs-lookup"><span data-stu-id="6be42-105">Group Policy object development with change control</span></span>


<span data-ttu-id="6be42-106">Mit AGPM können Sie eine Kopie der einzelnen Gruppenrichtlinienobjekte in einem zentralen Archiv speichern, damit Gruppenrichtlinienadministratoren Sie offline anzeigen und ändern können, ohne die bereitgestellte Version des Gruppenrichtlinienobjekts unmittelbar zu beeinflussen.</span><span class="sxs-lookup"><span data-stu-id="6be42-106">With AGPM, you can store a copy of each GPO in a central archive so that Group Policy administrators can view and change it offline without immediately affecting the deployed version of the GPO.</span></span> <span data-ttu-id="6be42-107">Darüber hinaus speichert AGPM eine Kopie jeder Version jedes gesteuerten Gruppenrichtlinienobjekts im Archiv, sodass Sie bei Bedarf auf eine frühere Version zurückgreifen können.</span><span class="sxs-lookup"><span data-stu-id="6be42-107">Additionally, AGPM stores a copy of each version of each controlled GPO in the archive so that you can roll back to an earlier version if necessary.</span></span>

<span data-ttu-id="6be42-108">Die Begriffe "Einchecken" und "Auschecken" werden ebenso wie in einer Bibliothek (oder in Anwendungen, die Änderungssteuerung, Versionskontrolle oder Quellcodeverwaltung für die Programmierungs Entwicklung bereitstellen) verwendet.</span><span class="sxs-lookup"><span data-stu-id="6be42-108">The terms "check in" and "check out" are used just as in a library (or in applications that provide change control, version control, or source control for programming development).</span></span> <span data-ttu-id="6be42-109">Wenn Sie ein Buch in einer Bibliothek verwenden möchten, können Sie es in der Bibliothek Auschecken.</span><span class="sxs-lookup"><span data-stu-id="6be42-109">To use a book that is in a library, you check it out from the library.</span></span> <span data-ttu-id="6be42-110">Niemand sonst kann es verwenden, wenn es ausgecheckt ist. Wenn Sie das Buch nicht mehr haben, können Sie es wieder in die Bibliothek einchecken, damit es von anderen verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="6be42-110">No one else can use it while you have it checked out. When you are finished with the book, you check it back into the library, so others can use it.</span></span>

<span data-ttu-id="6be42-111">Wenn Sie diese GPO-Steuerelementfeatures verwenden möchten, klicken Sie im Gruppenrichtlinien-Verwaltungs-Editor auf einen Knoten zum Ändern des Steuerelements.</span><span class="sxs-lookup"><span data-stu-id="6be42-111">To use these GPO control features, you will click a Change Control node in the Group Policy Management editor.</span></span> <span data-ttu-id="6be42-112">Der Knoten Change Control wird nur angezeigt, wenn Sie den AGPM-Client installiert haben.</span><span class="sxs-lookup"><span data-stu-id="6be42-112">The Change Control node appears only if you have installed the AGPM Client.</span></span>

<span data-ttu-id="6be42-113">Wenn Sie GPOs mithilfe von AGPM entwickeln:</span><span class="sxs-lookup"><span data-stu-id="6be42-113">When you develop GPOs by using AGPM:</span></span>

1.  <span data-ttu-id="6be42-114">Erstellen eines neuen kontrollierten Gruppenrichtlinienobjekts oder Steuern eines zuvor unkontrollierten Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="6be42-114">Create a new controlled GPO or control a previously uncontrolled GPO.</span></span>

2.  <span data-ttu-id="6be42-115">Überprüfen Sie das Gruppenrichtlinienobjekt, damit Sie und nur Sie es ändern können.</span><span class="sxs-lookup"><span data-stu-id="6be42-115">Check out the GPO, so that you and only you can change it.</span></span>

3.  <span data-ttu-id="6be42-116">Bearbeiten Sie das Gruppenrichtlinienobjekt.</span><span class="sxs-lookup"><span data-stu-id="6be42-116">Edit the GPO.</span></span>

4.  <span data-ttu-id="6be42-117">Überprüfen Sie das bearbeitete GPO, damit es von anderen geändert oder bereitgestellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="6be42-117">Check in the edited GPO, so that others can change it, or so that it can be deployed.</span></span>

5.  <span data-ttu-id="6be42-118">Überprüfen Sie die Änderungen.</span><span class="sxs-lookup"><span data-stu-id="6be42-118">Review the changes.</span></span>

6.  <span data-ttu-id="6be42-119">Stellen Sie das Gruppenrichtlinienobjekt in der Produktionsumgebung bereit.</span><span class="sxs-lookup"><span data-stu-id="6be42-119">Deploy the GPO to the production environment.</span></span>

## <span data-ttu-id="6be42-120">Rollenbasierte Delegierung</span><span class="sxs-lookup"><span data-stu-id="6be42-120">Role-based delegation</span></span>


<span data-ttu-id="6be42-121">AGPM bietet eine umfassende, einfach zu verwendende rollenbasierte Delegierung für die Verwaltung des Zugriffs auf GPOs im Archiv.</span><span class="sxs-lookup"><span data-stu-id="6be42-121">AGPM provides comprehensive, easy-to-use role-based delegation for managing access to GPOs in the archive.</span></span> <span data-ttu-id="6be42-122">Berechtigungen auf Domänenebene ermöglichen AGPM-Administratoren den Zugriff auf einzelne Domänen, ohne Zugriff auf andere Domänen zu gewähren.</span><span class="sxs-lookup"><span data-stu-id="6be42-122">Domain-level permissions enable AGPM Administrators to provide access to individual domains without providing access to other domains.</span></span> <span data-ttu-id="6be42-123">Die GPO-basierte Delegierung ermöglicht AGPM-Administratoren den Zugriff auf bestimmte GPOs, ohne domänenweiten Zugriff bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="6be42-123">GPO-based delegation enables AGPM Administrators to provide access to specific GPOs without providing domain-wide access.</span></span>

<span data-ttu-id="6be42-124">In AGPM gibt es speziell definierte Rollen: AGPM-Administrator (Vollzugriff), genehmigende Person, Editor und Bearbeiter.</span><span class="sxs-lookup"><span data-stu-id="6be42-124">Within AGPM, there are specifically defined roles: AGPM Administrator (Full Control), Approver, Editor, and Reviewer.</span></span> <span data-ttu-id="6be42-125">Die Rolle AGPM-Administrator umfasst die Berechtigungen für alle anderen Rollen.</span><span class="sxs-lookup"><span data-stu-id="6be42-125">The AGPM Administrator role includes the permissions for all other roles.</span></span> <span data-ttu-id="6be42-126">Standardmäßig haben nur genehmigende Personen die Möglichkeit, GPOs in der Produktionsumgebung einer Domäne bereitzustellen, um die Umgebung vor Fehlern durch die wenig erfahrenen Editoren zu schützen.</span><span class="sxs-lookup"><span data-stu-id="6be42-126">By default, only Approvers have the power to deploy GPOs to the production environment of a domain, protecting the environment from mistakes by less experienced Editors.</span></span> <span data-ttu-id="6be42-127">Standardmäßig umfassen alle Rollen auch die Rolle Prüfer und damit die Möglichkeit, die GPO-Einstellungen in Berichten anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="6be42-127">Also by default, all roles include the Reviewer role and therefore the ability to view GPO settings in reports.</span></span> <span data-ttu-id="6be42-128">AGPM bietet jedoch einem AGPM-Administrator die Flexibilität, den Zugriff auf Gruppenrichtlinienobjekte so anzupassen, dass Sie den Anforderungen Ihrer Organisation entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6be42-128">However, AGPM provides an AGPM Administrator with the flexibility to customize GPO access to fit the needs of your organization.</span></span>

## <span data-ttu-id="6be42-129">Delegierung in einer mehr Gruppenrichtlinien-Administratorumgebung</span><span class="sxs-lookup"><span data-stu-id="6be42-129">Delegation in a multiple Group Policy administrator environment</span></span>


<span data-ttu-id="6be42-130">In einer Umgebung, in der mehrere Personen GPOs ändern, delegiert ein AGPM-Administrator die Berechtigung für Redakteure, Genehmiger und Prüfer, entweder als Gruppen oder als Einzelpersonen.</span><span class="sxs-lookup"><span data-stu-id="6be42-130">In an environment where multiple people change GPOs, an AGPM Administrator delegates permission to Editors, Approvers, and Reviewers, either as groups or as individuals.</span></span> <span data-ttu-id="6be42-131">Einen typischen Entwicklungsprozess für Gruppenrichtlinienobjekte für einen Editor und eine genehmigende Person finden Sie unter [Checkliste: erstellen, bearbeiten und Bereitstellen eines Gruppenrichtlinienobjekts](checklist-create-edit-and-deploy-a-gpo-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="6be42-131">For a typical GPO development process for an Editor and an Approver, see [Checklist: Create, Edit, and Deploy a GPO](checklist-create-edit-and-deploy-a-gpo-agpm40.md).</span></span>

### <span data-ttu-id="6be42-132">Weitere Verweise</span><span class="sxs-lookup"><span data-stu-id="6be42-132">Additional references</span></span>

-   [<span data-ttu-id="6be42-133">Advanced Group Policy Management 4.0</span><span class="sxs-lookup"><span data-stu-id="6be42-133">Advanced Group Policy Management 4.0</span></span>](advanced-group-policy-management-40.md)

 

 





