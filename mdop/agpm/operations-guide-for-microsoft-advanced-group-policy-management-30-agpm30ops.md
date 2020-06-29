---
title: Betriebshandbuch für Microsoft Advanced Group Policy Management 3.0
description: Betriebshandbuch für Microsoft Advanced Group Policy Management 3.0
author: dansimp
ms.assetid: aaefe6d1-a9e5-43eb-b4d8-85880798cb8b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4958609444a62560060a565fb8626bcc9680fd9e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809397"
---
# <span data-ttu-id="da4ba-103">Betriebshandbuch für Microsoft Advanced Group Policy Management 3.0</span><span class="sxs-lookup"><span data-stu-id="da4ba-103">Operations Guide for Microsoft Advanced Group Policy Management 3.0</span></span>


<span data-ttu-id="da4ba-104">Sie können Microsoft Advanced Group Policy Management (AGPM) verwenden, um die Funktionen der Gruppenrichtlinien-Verwaltungskonsole (Group Policy Management Console, GPMC) zu erweitern und umfassende Änderungssteuerung und Erweiterte Verwaltung für Gruppenrichtlinienobjekte (Group Policy Objects, GPOs) bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="da4ba-104">You can use Microsoft Advanced Group Policy Management (AGPM) to extend the capabilities of the Group Policy Management Console (GPMC), providing comprehensive change control and enhanced management for Group Policy Objects (GPOs).</span></span>

<span data-ttu-id="da4ba-105">Mit AGPM können Sie:</span><span class="sxs-lookup"><span data-stu-id="da4ba-105">With AGPM you can:</span></span>

-   <span data-ttu-id="da4ba-106">Führen Sie die Offlinebearbeitung von GPOs aus, damit Sie Sie vor der Bereitstellung in einer Produktionsumgebung erstellen und testen können.</span><span class="sxs-lookup"><span data-stu-id="da4ba-106">Perform offline editing of GPOs, so you can create and test them before deploying to a production environment.</span></span>

-   <span data-ttu-id="da4ba-107">Sie können mehrere Versionen eines Gruppenrichtlinienobjekts in einem zentralen Archiv speichern, sodass Sie einen Rollback durchführen können, wenn ein Problem auftritt.</span><span class="sxs-lookup"><span data-stu-id="da4ba-107">Retain multiple versions of a GPO in a central archive, so you can roll back if a problem occurs.</span></span>

-   <span data-ttu-id="da4ba-108">Teilen Sie die Verantwortung für die Bearbeitung, Genehmigung und Überprüfung von GPOs zwischen mehreren Personen mithilfe einer rollenbasierten Delegierung.</span><span class="sxs-lookup"><span data-stu-id="da4ba-108">Share the responsibility for editing, approving, and reviewing GPOs among multiple people using role-based delegation.</span></span>

-   <span data-ttu-id="da4ba-109">Eliminieren Sie die Gefahr, dass mehrere Gruppenrichtlinienadministratoren die Arbeit des anderen überschreiben, indem Sie die Funktion zum ein-und Auschecken für GPOs verwenden.</span><span class="sxs-lookup"><span data-stu-id="da4ba-109">Eliminate the danger of multiple Group Policy administrators overwriting each other's work by using a check-in/check-out capability for GPOs.</span></span>

-   <span data-ttu-id="da4ba-110">Analysieren Sie Änderungen an einem Gruppenrichtlinienobjekt, indem Sie es mit einem anderen Gruppenrichtlinienobjekt oder einer anderen Version desselben Gruppenrichtlinienobjekts mithilfe von Differenz Berichterstattung vergleichen.</span><span class="sxs-lookup"><span data-stu-id="da4ba-110">Analyze changes to a GPO, comparing it to another GPO or another version of the same GPO using difference reporting.</span></span>

-   <span data-ttu-id="da4ba-111">Vereinfachen Sie die Erstellung neuer GPOs mithilfe von GPO-Vorlagen, wobei Standardeinstellungen gespeichert werden, die als Ausgangspunkt für neue GPOs verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="da4ba-111">Simplify the creation of new GPOs by using GPO templates, storing standard settings to use as starting points for new GPOs.</span></span>

<span data-ttu-id="da4ba-112">AGPM fügt unter jeder Domäne, die in der GPMC angezeigt wird, einen Ordner " **Änderungssteuerung** " sowie eine Registerkarte " **Verlauf** " für jedes GPO und jeden in der GPMC angezeigten Gruppenrichtlinien Link hinzu.</span><span class="sxs-lookup"><span data-stu-id="da4ba-112">AGPM adds a **Change Control** folder under each domain displayed in the GPMC, as well as a **History** tab for each GPO and Group Policy link displayed in the GPMC.</span></span>

-   [<span data-ttu-id="da4ba-113">Übersicht über Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="da4ba-113">Overview of Advanced Group Policy Management</span></span>](overview-of-advanced-group-policy-management-agpm30ops.md)

-   [<span data-ttu-id="da4ba-114">Bewährte Methoden für die Versionskontrolle</span><span class="sxs-lookup"><span data-stu-id="da4ba-114">Best Practices for Version Control</span></span>](best-practices-for-version-control.md)

-   [<span data-ttu-id="da4ba-115">Prüfliste: Verwalten des AGPM-Servers und -Archivs</span><span class="sxs-lookup"><span data-stu-id="da4ba-115">Checklist: Administer the AGPM Server and Archive</span></span>](checklist-administer-the-agpm-server-and-archive.md)

-   [<span data-ttu-id="da4ba-116">Prüfliste: Erstellen, Bearbeiten und Bereitstellen eines Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="da4ba-116">Checklist: Create, Edit, and Deploy a GPO</span></span>](checklist-create-edit-and-deploy-a-gpo-agpm30ops.md)

-   [<span data-ttu-id="da4ba-117">Durchführen von AGPM-Administratoraufgaben</span><span class="sxs-lookup"><span data-stu-id="da4ba-117">Performing AGPM Administrator Tasks</span></span>](performing-agpm-administrator-tasks-agpm30ops.md)

-   [<span data-ttu-id="da4ba-118">Durchführen von Editor-Aufgaben</span><span class="sxs-lookup"><span data-stu-id="da4ba-118">Performing Editor Tasks</span></span>](performing-editor-tasks-agpm30ops.md)

-   [<span data-ttu-id="da4ba-119">Durchführen der Aufgaben von genehmigenden Personen</span><span class="sxs-lookup"><span data-stu-id="da4ba-119">Performing Approver Tasks</span></span>](performing-approver-tasks-agpm30ops.md)

-   [<span data-ttu-id="da4ba-120">Durchführen von Prüferaufgaben</span><span class="sxs-lookup"><span data-stu-id="da4ba-120">Performing Reviewer Tasks</span></span>](performing-reviewer-tasks-agpm30ops.md)

-   [<span data-ttu-id="da4ba-121">Problembehandlung bei Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="da4ba-121">Troubleshooting Advanced Group Policy Management</span></span>](troubleshooting-advanced-group-policy-management-agpm30ops.md)

-   [<span data-ttu-id="da4ba-122">Benutzeroberfläche: Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="da4ba-122">User Interface: Advanced Group Policy Management</span></span>](user-interface-advanced-group-policy-management-agpm30ops.md)

 

 





