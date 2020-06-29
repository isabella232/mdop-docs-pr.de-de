---
title: Betriebshandbuch für Microsoft Advanced Group Policy Management 2.5
description: Betriebshandbuch für Microsoft Advanced Group Policy Management 2.5
author: dansimp
ms.assetid: 005f0bb5-789f-42a9-bcaf-7e8c31a8df66
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c0ae04e0e8dcf62d3ea840de28a9248827ec62e4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809400"
---
# <span data-ttu-id="526fe-103">Betriebshandbuch für Microsoft Advanced Group Policy Management 2.5</span><span class="sxs-lookup"><span data-stu-id="526fe-103">Operations Guide for Microsoft Advanced Group Policy Management 2.5</span></span>


<span data-ttu-id="526fe-104">Sie können Microsoft Advanced Group Policy Management (AGPM) verwenden, um die Funktionen der Gruppenrichtlinien-Verwaltungskonsole (Group Policy Management Console, GPMC) zu erweitern und umfassende Änderungssteuerung und Erweiterte Verwaltung für Gruppenrichtlinienobjekte (Group Policy Objects, GPOs) bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="526fe-104">You can use Microsoft Advanced Group Policy Management (AGPM) to extend the capabilities of the Group Policy Management Console (GPMC), providing comprehensive change control and enhanced management for Group Policy objects (GPOs).</span></span>

<span data-ttu-id="526fe-105">Mit AGPM können Sie:</span><span class="sxs-lookup"><span data-stu-id="526fe-105">With AGPM you can:</span></span>

-   <span data-ttu-id="526fe-106">Führen Sie die Offlinebearbeitung von GPOs aus, damit Sie Sie vor der Bereitstellung in einer Produktionsumgebung erstellen und testen können.</span><span class="sxs-lookup"><span data-stu-id="526fe-106">Perform offline editing of GPOs, so you can create and test them before deploying to a production environment.</span></span>

-   <span data-ttu-id="526fe-107">Sie können mehrere Versionen eines Gruppenrichtlinienobjekts in einem zentralen Archiv speichern, sodass Sie einen Rollback durchführen können, wenn ein Problem auftritt.</span><span class="sxs-lookup"><span data-stu-id="526fe-107">Retain multiple versions of a GPO in a central archive, so you can roll back if a problem occurs.</span></span>

-   <span data-ttu-id="526fe-108">Teilen Sie die Verantwortung für die Bearbeitung, Genehmigung und Überprüfung von GPOs zwischen mehreren Personen mithilfe einer rollenbasierten Delegierung.</span><span class="sxs-lookup"><span data-stu-id="526fe-108">Share the responsibility for editing, approving, and reviewing GPOs among multiple people using role-based delegation.</span></span>

-   <span data-ttu-id="526fe-109">Eliminieren Sie die Gefahr, dass mehrere Gruppenrichtlinienadministratoren die Arbeit des anderen überschreiben, indem Sie die Funktion zum ein-und Auschecken für GPOs verwenden.</span><span class="sxs-lookup"><span data-stu-id="526fe-109">Eliminate the danger of multiple Group Policy administrators overwriting each other's work by using a check-in/check-out capability for GPOs.</span></span>

-   <span data-ttu-id="526fe-110">Analysieren Sie Änderungen an einem Gruppenrichtlinienobjekt, indem Sie es mit einem anderen Gruppenrichtlinienobjekt oder einer anderen Version desselben Gruppenrichtlinienobjekts mithilfe von Differenz Berichterstattung vergleichen.</span><span class="sxs-lookup"><span data-stu-id="526fe-110">Analyze changes to a GPO, comparing it to another GPO or another version of the same GPO using difference reporting.</span></span>

-   <span data-ttu-id="526fe-111">Vereinfachen Sie die Erstellung neuer GPOs mithilfe von GPO-Vorlagen, wobei Standardeinstellungen gespeichert werden, die als Ausgangspunkt für neue GPOs verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="526fe-111">Simplify the creation of new GPOs by using GPO templates, storing standard settings to use as starting points for new GPOs.</span></span>

<span data-ttu-id="526fe-112">AGPM fügt unter jeder Domäne, die in der GPMC angezeigt wird, sowie den Registerkarten **Protokoll** und **Erweiterungen** für jedes GPO und jeden Gruppenrichtlinien Link, der in der GPMC angezeigt wird, einen Knoten für die **Änderungssteuerung** hinzu.</span><span class="sxs-lookup"><span data-stu-id="526fe-112">AGPM adds a **Change Control** node under each domain displayed in the GPMC, as well as **History** and **Extensions** tabs for each GPO and Group Policy link displayed in the GPMC.</span></span>

-   [<span data-ttu-id="526fe-113">Übersicht über Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="526fe-113">Overview of Advanced Group Policy Management</span></span>](overview-of-advanced-group-policy-management.md)

-   [<span data-ttu-id="526fe-114">Prüfliste: Erstellen, Bearbeiten und Zerstören eines Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="526fe-114">Checklist: Create, Edit, and Deploy a GPO</span></span>](checklist-create-edit-and-deploy-a-gpo.md)

-   [<span data-ttu-id="526fe-115">Durchführen von AGPM-Administratoraufgaben</span><span class="sxs-lookup"><span data-stu-id="526fe-115">Performing AGPM Administrator Tasks</span></span>](performing-agpm-administrator-tasks.md)

-   [<span data-ttu-id="526fe-116">Durchführen von Editor-Aufgaben</span><span class="sxs-lookup"><span data-stu-id="526fe-116">Performing Editor Tasks</span></span>](performing-editor-tasks.md)

-   [<span data-ttu-id="526fe-117">Durchführen der Aufgaben von genehmigenden Personen</span><span class="sxs-lookup"><span data-stu-id="526fe-117">Performing Approver Tasks</span></span>](performing-approver-tasks.md)

-   [<span data-ttu-id="526fe-118">Durchführen von Prüferaufgaben</span><span class="sxs-lookup"><span data-stu-id="526fe-118">Performing Reviewer Tasks</span></span>](performing-reviewer-tasks.md)

-   [<span data-ttu-id="526fe-119">Problembehandlung bei Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="526fe-119">Troubleshooting Advanced Group Policy Management</span></span>](troubleshooting-advanced-group-policy-management.md)

-   [<span data-ttu-id="526fe-120">Benutzeroberfläche: Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="526fe-120">User Interface: Advanced Group Policy Management</span></span>](user-interface-advanced-group-policy-management.md)

 

 





