---
title: Betriebshandbuch für Microsoft Advanced Group Policy Management 4.0
description: Betriebshandbuch für Microsoft Advanced Group Policy Management 4.0
author: dansimp
ms.assetid: 0bafeba3-20a9-4360-be5d-03f786df11ee
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b51956c319f1b0a77e4a4bdf71090be4f322236e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808324"
---
# <span data-ttu-id="9b377-103">Betriebshandbuch für Microsoft Advanced Group Policy Management 4.0</span><span class="sxs-lookup"><span data-stu-id="9b377-103">Operations Guide for Microsoft Advanced Group Policy Management 4.0</span></span>


<span data-ttu-id="9b377-104">Sie können Microsoft Advanced Group Policy Management (AGPM) verwenden, um die Funktionen der Gruppenrichtlinien-Verwaltungskonsole (Group Policy Management Console, GPMC) zu erweitern.</span><span class="sxs-lookup"><span data-stu-id="9b377-104">You can use Microsoft Advanced Group Policy Management (AGPM) to extend the capabilities of the Group Policy Management Console (GPMC).</span></span> <span data-ttu-id="9b377-105">AGPM bietet umfassende Änderungssteuerung und verbesserte Verwaltung von Gruppenrichtlinienobjekten (Group Policy Objects, GPOs).</span><span class="sxs-lookup"><span data-stu-id="9b377-105">AGPM provides comprehensive change control and improved management of Group Policy Objects (GPOs).</span></span>

<span data-ttu-id="9b377-106">Mit AGPM können Sie die folgenden Aufgaben ausführen:</span><span class="sxs-lookup"><span data-stu-id="9b377-106">Using AGPM, you can do these tasks:</span></span>

-   <span data-ttu-id="9b377-107">Führen Sie die Offlinebearbeitung von GPOs aus, damit Sie Sie erstellen und testen können, bevor Sie Sie in einer Produktionsumgebung bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="9b377-107">Perform offline editing of GPOs so that you can create and test them before you deploy them to a production environment.</span></span>

-   <span data-ttu-id="9b377-108">Verwalten Sie mehrere Versionen eines GPO in einem zentralen Archiv, damit Sie einen Rollback ausführen können, wenn ein Problem auftritt.</span><span class="sxs-lookup"><span data-stu-id="9b377-108">Maintain multiple versions of a GPO in a central archive so that you can roll back if a problem occurs.</span></span>

-   <span data-ttu-id="9b377-109">Teilen Sie die Verantwortung für die Bearbeitung, Genehmigung und Überprüfung von GPOs zwischen mehreren Personen mithilfe einer rollenbasierten Delegierung.</span><span class="sxs-lookup"><span data-stu-id="9b377-109">Share the responsibility for editing, approving, and reviewing GPOs among multiple people by using role-based delegation.</span></span>

-   <span data-ttu-id="9b377-110">Eliminieren Sie die Gefahr, dass mehrere Gruppenrichtlinienadministratoren die Arbeit eines anderen überschreiben, indem Sie die Funktion zum ein-und Auschecken für GPOs verwenden.</span><span class="sxs-lookup"><span data-stu-id="9b377-110">Eliminate the danger of multiple Group Policy administrators overwriting one another's work by using the check-in and check-out capability for GPOs.</span></span>

-   <span data-ttu-id="9b377-111">Analysieren Sie Änderungen an einem GPO, und vergleichen Sie es mit einem anderen Gruppenrichtlinienobjekt oder einer anderen Version desselben Gruppenrichtlinienobjekts mithilfe von Differenz Berichterstattung.</span><span class="sxs-lookup"><span data-stu-id="9b377-111">Analyze changes to a GPO, comparing it to another GPO or another version of the same GPO by using difference reporting.</span></span>

-   <span data-ttu-id="9b377-112">Vereinfachen Sie das Erstellen neuer GPOs mithilfe von GPO-Vorlagen, speichern Sie allgemeine Richtlinieneinstellungen und Einstellungen, um Sie als Ausgangspunkt für neue GPOs zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="9b377-112">Simplify creating new GPOs by using GPO templates, storing common policy settings and preference settings to use as starting points for new GPOs.</span></span>

-   <span data-ttu-id="9b377-113">Delegieren des Zugriffs auf die Produktionsumgebung</span><span class="sxs-lookup"><span data-stu-id="9b377-113">Delegate access to the production environment.</span></span>

-   <span data-ttu-id="9b377-114">Suchen Sie nach GPOs mit bestimmten Attributen, und Filtern Sie die Liste der angezeigten GPOs.</span><span class="sxs-lookup"><span data-stu-id="9b377-114">Search for GPOs with specific attributes and filter the list of GPOs displayed.</span></span>

-   <span data-ttu-id="9b377-115">Exportieren Sie ein GPO in eine Datei, damit Sie es aus einer Domäne in einer Testgesamtstruktur in eine Domäne in einer Produktionsgesamtstruktur kopieren können.</span><span class="sxs-lookup"><span data-stu-id="9b377-115">Export a GPO to a file so that you can copy it from a domain in a test forest to a domain in a production forest.</span></span>

<span data-ttu-id="9b377-116">AGPM fügt unter jeder Domäne, die in der GPMC angezeigt wird, zusätzlich zu einer Registerkarte " **Verlauf** " für jedes GPO und jeden in der GPMC angezeigten Gruppenrichtlinien Link einen Ordner für die **Änderungssteuerung** hinzu.</span><span class="sxs-lookup"><span data-stu-id="9b377-116">AGPM adds a **Change Control** folder under each domain displayed in the GPMC, in addition to a **History** tab for each GPO and Group Policy link displayed in the GPMC.</span></span>

-   [<span data-ttu-id="9b377-117">Übersicht über Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="9b377-117">Overview of Advanced Group Policy Management</span></span>](overview-of-advanced-group-policy-management-agpm40.md)

-   [<span data-ttu-id="9b377-118">Bewährte Methoden für die Versionskontrolle</span><span class="sxs-lookup"><span data-stu-id="9b377-118">Best Practices for Version Control</span></span>](best-practices-for-version-control-agpm40.md)

-   [<span data-ttu-id="9b377-119">Prüfliste: Verwalten des AGPM-Servers und -Archivs</span><span class="sxs-lookup"><span data-stu-id="9b377-119">Checklist: Administer the AGPM Server and Archive</span></span>](checklist-administer-the-agpm-server-and-archive-agpm40.md)

-   [<span data-ttu-id="9b377-120">Prüfliste: Erstellen, Bearbeiten und Bereitstellen eines Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="9b377-120">Checklist: Create, Edit, and Deploy a GPO</span></span>](checklist-create-edit-and-deploy-a-gpo-agpm40.md)

-   [<span data-ttu-id="9b377-121">Suchen und Filtern der GPO-Liste</span><span class="sxs-lookup"><span data-stu-id="9b377-121">Search and Filter the List of GPOs</span></span>](search-and-filter-the-list-of-gpos.md)

-   [<span data-ttu-id="9b377-122">Durchführen von AGPM-Administratoraufgaben</span><span class="sxs-lookup"><span data-stu-id="9b377-122">Performing AGPM Administrator Tasks</span></span>](performing-agpm-administrator-tasks-agpm40.md)

-   [<span data-ttu-id="9b377-123">Durchführen von Editor-Aufgaben</span><span class="sxs-lookup"><span data-stu-id="9b377-123">Performing Editor Tasks</span></span>](performing-editor-tasks-agpm40.md)

-   [<span data-ttu-id="9b377-124">Durchführen der Aufgaben von genehmigenden Personen</span><span class="sxs-lookup"><span data-stu-id="9b377-124">Performing Approver Tasks</span></span>](performing-approver-tasks-agpm40.md)

-   [<span data-ttu-id="9b377-125">Durchführen von Prüferaufgaben</span><span class="sxs-lookup"><span data-stu-id="9b377-125">Performing Reviewer Tasks</span></span>](performing-reviewer-tasks-agpm40.md)

-   [<span data-ttu-id="9b377-126">Problembehandlung für AGPM</span><span class="sxs-lookup"><span data-stu-id="9b377-126">Troubleshooting AGPM</span></span>](troubleshooting-agpm-agpm40.md)

-   [<span data-ttu-id="9b377-127">Benutzeroberfläche: Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="9b377-127">User Interface: Advanced Group Policy Management</span></span>](user-interface-advanced-group-policy-management-agpm40.md)

 

 





