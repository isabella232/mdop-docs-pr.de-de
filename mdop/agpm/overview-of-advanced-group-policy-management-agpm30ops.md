---
title: Übersicht über Advanced Group Policy Management
description: Übersicht über Advanced Group Policy Management
author: dansimp
ms.assetid: 3a8d1e58-12b9-42bd-898f-6d57514dfbb9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: feb43972c78ed12501e372800c1f5ec19609477a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809388"
---
# <span data-ttu-id="8294e-103">Übersicht über Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="8294e-103">Overview of Advanced Group Policy Management</span></span>


<span data-ttu-id="8294e-104">Mithilfe der erweiterten Gruppenrichtlinienverwaltung (Group Policy Management, AGPM) können Sie die Funktionen der Gruppenrichtlinien-Verwaltungskonsole (Group Policy Management Console, GPMC) erweitern, um umfassende Änderungssteuerung und verbesserte Verwaltung für Gruppenrichtlinienobjekte (Group Policy Objects, GPOs) bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="8294e-104">You can use Advanced Group Policy Management (AGPM) to extend the capabilities of the Group Policy Management Console (GPMC) to provide comprehensive change control and improved management for Group Policy Objects (GPOs).</span></span>

## <span data-ttu-id="8294e-105">Entwicklung von Gruppenrichtlinienobjekten mit Änderungssteuerung</span><span class="sxs-lookup"><span data-stu-id="8294e-105">Group Policy object development with change control</span></span>


<span data-ttu-id="8294e-106">Mit AGPM können Sie eine Kopie der einzelnen Gruppenrichtlinienobjekte in einem zentralen Archiv speichern, damit Gruppenrichtlinienadministratoren Sie offline anzeigen und ändern können, ohne die bereitgestellte Version des Gruppenrichtlinienobjekts unmittelbar zu beeinflussen.</span><span class="sxs-lookup"><span data-stu-id="8294e-106">With AGPM, you can store a copy of each GPO in a central archive so that Group Policy administrators can view and change it offline without immediately affecting the deployed version of the GPO.</span></span> <span data-ttu-id="8294e-107">Darüber hinaus speichert AGPM eine Kopie jeder Version jedes gesteuerten Gruppenrichtlinienobjekts im Archiv, sodass Sie bei Bedarf auf eine frühere Version zurückgreifen können.</span><span class="sxs-lookup"><span data-stu-id="8294e-107">Additionally, AGPM stores a copy of each version of each controlled GPO in the archive so that you can roll back to an earlier version if necessary.</span></span>

<span data-ttu-id="8294e-108">Die Begriffe "Einchecken" und "Auschecken" werden ebenso wie in einer Bibliothek (oder in Anwendungen, die Änderungssteuerung, Versionskontrolle oder Quellcodeverwaltung für die Programmierungs Entwicklung bereitstellen) verwendet.</span><span class="sxs-lookup"><span data-stu-id="8294e-108">The terms "check in" and "check out" are used just as in a library (or in applications that provide change control, version control, or source control for programming development).</span></span> <span data-ttu-id="8294e-109">Wenn Sie ein Buch in einer Bibliothek verwenden möchten, können Sie es in der Bibliothek Auschecken.</span><span class="sxs-lookup"><span data-stu-id="8294e-109">To use a book that is in a library, you check it out from the library.</span></span> <span data-ttu-id="8294e-110">Niemand sonst kann es verwenden, wenn es ausgecheckt ist. Wenn Sie das Buch nicht mehr haben, können Sie es wieder in die Bibliothek einchecken, damit es von anderen verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="8294e-110">No one else can use it while you have it checked out. When you are finished with the book, you check it back into the library, so others can use it.</span></span>

<span data-ttu-id="8294e-111">Wenn Sie GPOs mithilfe von AGPM entwickeln:</span><span class="sxs-lookup"><span data-stu-id="8294e-111">When you develop GPOs by using AGPM:</span></span>

1.  <span data-ttu-id="8294e-112">Erstellen eines neuen kontrollierten Gruppenrichtlinienobjekts oder Steuern eines zuvor unkontrollierten Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="8294e-112">Create a new controlled GPO or control a previously uncontrolled GPO.</span></span>

2.  <span data-ttu-id="8294e-113">Überprüfen Sie das Gruppenrichtlinienobjekt, damit Sie und nur Sie es ändern können.</span><span class="sxs-lookup"><span data-stu-id="8294e-113">Check out the GPO, so that you and only you can change it.</span></span>

3.  <span data-ttu-id="8294e-114">Bearbeiten Sie das Gruppenrichtlinienobjekt.</span><span class="sxs-lookup"><span data-stu-id="8294e-114">Edit the GPO.</span></span>

4.  <span data-ttu-id="8294e-115">Überprüfen Sie das bearbeitete GPO, damit es von anderen geändert oder bereitgestellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="8294e-115">Check in the edited GPO, so that others can change it, or so that it can be deployed.</span></span>

5.  <span data-ttu-id="8294e-116">Überprüfen Sie die Änderungen.</span><span class="sxs-lookup"><span data-stu-id="8294e-116">Review the changes.</span></span>

6.  <span data-ttu-id="8294e-117">Stellen Sie das Gruppenrichtlinienobjekt in der Produktionsumgebung bereit.</span><span class="sxs-lookup"><span data-stu-id="8294e-117">Deploy the GPO to the production environment.</span></span>

## <span data-ttu-id="8294e-118">Rollenbasierte Delegierung</span><span class="sxs-lookup"><span data-stu-id="8294e-118">Role-based delegation</span></span>


<span data-ttu-id="8294e-119">AGPM bietet eine umfassende, einfach zu verwendende rollenbasierte Delegierung für die Verwaltung des Zugriffs auf GPOs im Archiv.</span><span class="sxs-lookup"><span data-stu-id="8294e-119">AGPM provides comprehensive, easy-to-use role-based delegation for managing access to GPOs in the archive.</span></span> <span data-ttu-id="8294e-120">Berechtigungen auf Domänenebene ermöglichen AGPM-Administratoren den Zugriff auf einzelne Domänen, ohne Zugriff auf andere Domänen zu gewähren.</span><span class="sxs-lookup"><span data-stu-id="8294e-120">Domain-level permissions enable AGPM Administrators to provide access to individual domains without providing access to other domains.</span></span> <span data-ttu-id="8294e-121">Die GPO-basierte Delegierung ermöglicht AGPM-Administratoren den Zugriff auf bestimmte GPOs, ohne domänenweiten Zugriff bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="8294e-121">GPO-based delegation enables AGPM Administrators to provide access to specific GPOs without providing domain-wide access.</span></span>

<span data-ttu-id="8294e-122">In AGPM gibt es speziell definierte Rollen: AGPM-Administrator (Vollzugriff), genehmigende Person, Editor und Bearbeiter.</span><span class="sxs-lookup"><span data-stu-id="8294e-122">Within AGPM, there are specifically defined roles: AGPM Administrator (Full Control), Approver, Editor, and Reviewer.</span></span> <span data-ttu-id="8294e-123">Die Rolle AGPM-Administrator umfasst die Berechtigungen für alle anderen Rollen.</span><span class="sxs-lookup"><span data-stu-id="8294e-123">The AGPM Administrator role includes the permissions for all other roles.</span></span> <span data-ttu-id="8294e-124">Standardmäßig haben nur genehmigende Personen die Möglichkeit, GPOs in der Produktionsumgebung bereitzustellen, um die Umgebung vor Fehlern durch die wenig erfahrenen Editoren zu schützen.</span><span class="sxs-lookup"><span data-stu-id="8294e-124">By default, only Approvers have the power to deploy GPOs to the production environment, protecting the environment from mistakes by less experienced Editors.</span></span> <span data-ttu-id="8294e-125">Standardmäßig umfassen alle Rollen auch die Rolle Prüfer und damit die Möglichkeit, die GPO-Einstellungen in Berichten anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="8294e-125">Also by default, all roles include the Reviewer role and therefore the ability to view GPO settings in reports.</span></span> <span data-ttu-id="8294e-126">AGPM bietet jedoch einem AGPM-Administrator die Flexibilität, den Zugriff auf Gruppenrichtlinienobjekte so anzupassen, dass Sie den Anforderungen Ihrer Organisation entsprechen.</span><span class="sxs-lookup"><span data-stu-id="8294e-126">However, AGPM provides an AGPM Administrator with the flexibility to customize GPO access to fit the needs of your organization.</span></span>

## <span data-ttu-id="8294e-127">Delegierung in einer mehr Gruppenrichtlinien-Administratorumgebung</span><span class="sxs-lookup"><span data-stu-id="8294e-127">Delegation in a multiple Group Policy administrator environment</span></span>


<span data-ttu-id="8294e-128">In einer Umgebung, in der mehrere Personen GPOs ändern, delegiert ein AGPM-Administrator die Berechtigung für Redakteure, Genehmiger und Prüfer, entweder als Gruppen oder als Einzelpersonen.</span><span class="sxs-lookup"><span data-stu-id="8294e-128">In an environment where multiple people change GPOs, an AGPM Administrator delegates permission to Editors, Approvers, and Reviewers, either as groups or as individuals.</span></span> <span data-ttu-id="8294e-129">Einen typischen Entwicklungsprozess für Gruppenrichtlinienobjekte für einen Editor und eine genehmigende Person finden Sie unter [Checkliste: erstellen, bearbeiten und Bereitstellen eines Gruppenrichtlinienobjekts](checklist-create-edit-and-deploy-a-gpo-agpm30ops.md).</span><span class="sxs-lookup"><span data-stu-id="8294e-129">For a typical GPO development process for an Editor and an Approver, see [Checklist: Create, Edit, and Deploy a GPO](checklist-create-edit-and-deploy-a-gpo-agpm30ops.md).</span></span>

### <span data-ttu-id="8294e-130">Weitere Verweise</span><span class="sxs-lookup"><span data-stu-id="8294e-130">Additional references</span></span>

-   [<span data-ttu-id="8294e-131">Betriebshandbuch für Microsoft Advanced Group Policy Management 3.0</span><span class="sxs-lookup"><span data-stu-id="8294e-131">Operations Guide for Microsoft Advanced Group Policy Management 3.0</span></span>](operations-guide-for-microsoft-advanced-group-policy-management-30-agpm30ops.md)

 

 





