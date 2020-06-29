---
title: So verwalten Sie Berichte in der Server Management Console
description: So verwalten Sie Berichte in der Server Management Console
author: dansimp
ms.assetid: 28d99620-6339-43f6-9288-4aa958607c59
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 3d70734be04df380e6ce3f4ee8de126503e482e2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806988"
---
# <span data-ttu-id="1fba1-103">So verwalten Sie Berichte in der Server Management Console</span><span class="sxs-lookup"><span data-stu-id="1fba1-103">How to Manage Reports in the Server Management Console</span></span>


<span data-ttu-id="1fba1-104">Um das Application Virtualization-System effektiv zu verwalten, können Sie mithilfe der Application Virtualization Server-Verwaltungskonsole eine Vielzahl von Berichten generieren, die Informationen zum System bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="1fba1-104">To effectively manage the Application Virtualization System, you can use the Application Virtualization Server Management Console to generate a variety of reports that provide information about the system.</span></span> <span data-ttu-id="1fba1-105">Diese Informationen umfassen tägliche Nutzungsinformationen für eine bestimmte Anwendung oder alle Anwendungen sowie die Systemfehler Verfolgung.</span><span class="sxs-lookup"><span data-stu-id="1fba1-105">This information includes daily usage information for a specific application or all applications, and system error tracking.</span></span>

**<span data-ttu-id="1fba1-106">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="1fba1-106">Note</span></span>**  
-   <span data-ttu-id="1fba1-107">Während der Installation installiert das Installationsskript nur die englische Sprachversion der Berichtsanzeige.</span><span class="sxs-lookup"><span data-stu-id="1fba1-107">During installation, the installation script installs only the English language version of report viewer.</span></span> <span data-ttu-id="1fba1-108">Damit die Berichtsanzeige die richtigen Informationen in anderen Sprachen anzeigt, muss ein Sprachpaket vom folgenden Speicherort installiert <https://go.microsoft.com/fwlink/?LinkId=131645> werden:</span><span class="sxs-lookup"><span data-stu-id="1fba1-108">For the report viewer to display the correct information in other languages, it is necessary to install a language pack from the following location: <https://go.microsoft.com/fwlink/?LinkId=131645>.</span></span>

-   <span data-ttu-id="1fba1-109">Wenn Sie in der Server Verwaltungskonsole eine Anwendung hinzufügen oder bearbeiten, müssen Sie sicherstellen, dass die Anwendungsnamen und-Versionen exakt mit denen in den OSD-Dateien übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="1fba1-109">When you add or edit an application in the Server Management Console, you must make sure that the application names and versions exactly match those in the OSD files.</span></span> <span data-ttu-id="1fba1-110">Das berichterstellungsfeature verwendet die Datenfelder Anwendungsnamen und Versionen, wenn es Anwendungs Nutzungsdaten identifiziert, für die ein Bericht erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="1fba1-110">The reporting feature uses the application names and versions data fields when it identifies application usage data on which to report.</span></span> <span data-ttu-id="1fba1-111">Wenn die Datenfelder nicht übereinstimmen, werden die Verwendungsdaten Sätze übersprungen.</span><span class="sxs-lookup"><span data-stu-id="1fba1-111">If the data fields do not match, the usage records will be skipped.</span></span>

 

## <span data-ttu-id="1fba1-112">Inhalt dieses Abschnitts</span><span class="sxs-lookup"><span data-stu-id="1fba1-112">In This Section</span></span>


<a href="" id="application-virtualization-report-types"></a>[<span data-ttu-id="1fba1-113">Berichtstypen der Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="1fba1-113">Application Virtualization Report Types</span></span>](application-virtualization-report-types.md)  
<span data-ttu-id="1fba1-114">Enthält Informationen zu den verfügbaren Berichtstypen.</span><span class="sxs-lookup"><span data-stu-id="1fba1-114">Contains information about the available report types.</span></span>

<a href="" id="how-to-create-a-report"></a>[<span data-ttu-id="1fba1-115">So erstellen Sie einen Bericht</span><span class="sxs-lookup"><span data-stu-id="1fba1-115">How to Create a Report</span></span>](how-to-create-a-reportserver.md)  
<span data-ttu-id="1fba1-116">Bietet eine schrittweise Anleitung zum Erstellen eines Berichts.</span><span class="sxs-lookup"><span data-stu-id="1fba1-116">Provides a step-by-step process for creating a report.</span></span>

<a href="" id="how-to-run-a-report"></a>[<span data-ttu-id="1fba1-117">So führen Sie einen Bericht aus</span><span class="sxs-lookup"><span data-stu-id="1fba1-117">How to Run a Report</span></span>](how-to-run-a-reportserver.md)  
<span data-ttu-id="1fba1-118">Bietet eine schrittweise Anleitung zum Ausführen eines Berichts.</span><span class="sxs-lookup"><span data-stu-id="1fba1-118">Provides a step-by-step process for running a report.</span></span>

<a href="" id="how-to-print-a-report"></a>[<span data-ttu-id="1fba1-119">So drucken Sie einen Bericht</span><span class="sxs-lookup"><span data-stu-id="1fba1-119">How to Print a Report</span></span>](how-to-print-a-reportserver.md)  
<span data-ttu-id="1fba1-120">Bietet eine schrittweise Anleitung zum Drucken eines Berichts.</span><span class="sxs-lookup"><span data-stu-id="1fba1-120">Provides a step-by-step process for printing a report.</span></span>

<a href="" id="how-to-export-a-report"></a>[<span data-ttu-id="1fba1-121">So exportieren Sie einen Bericht</span><span class="sxs-lookup"><span data-stu-id="1fba1-121">How to Export a Report</span></span>](how-to-export-a-reportserver.md)  
<span data-ttu-id="1fba1-122">Bietet eine schrittweise Anleitung zum Exportieren eines Berichts.</span><span class="sxs-lookup"><span data-stu-id="1fba1-122">Provides a step-by-step process for exporting a report.</span></span>

<a href="" id="how-to-delete-a-report"></a>[<span data-ttu-id="1fba1-123">So löschen Sie einen Bericht</span><span class="sxs-lookup"><span data-stu-id="1fba1-123">How to Delete a Report</span></span>](how-to-delete-a-reportserver.md)  
<span data-ttu-id="1fba1-124">Bietet eine schrittweise Anleitung zum Löschen eines Berichts.</span><span class="sxs-lookup"><span data-stu-id="1fba1-124">Provides a step-by-step process for deleting a report.</span></span>

## <span data-ttu-id="1fba1-125">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="1fba1-125">Related topics</span></span>


[<span data-ttu-id="1fba1-126">Bericht zur Anwendungsverwendung</span><span class="sxs-lookup"><span data-stu-id="1fba1-126">Application Utilization Report</span></span>](application-utilization-reportserver.md)

[<span data-ttu-id="1fba1-127">So führen Sie Verwaltungsaufgaben in der Application Virtualization Server Management Console durch</span><span class="sxs-lookup"><span data-stu-id="1fba1-127">How to Perform Administrative Tasks in the Application Virtualization Server Management Console</span></span>](how-to-perform-administrative-tasks-in-the-application-virtualization-server-management-console.md)

[<span data-ttu-id="1fba1-128">Bericht zur Softwareüberwachung</span><span class="sxs-lookup"><span data-stu-id="1fba1-128">Software Audit Report</span></span>](software-audit-reportserver.md)

[<span data-ttu-id="1fba1-129">Bericht zu Systemfehlern</span><span class="sxs-lookup"><span data-stu-id="1fba1-129">System Error Report</span></span>](system-error-reportserver.md)

[<span data-ttu-id="1fba1-130">Bericht zur Systemverwendung</span><span class="sxs-lookup"><span data-stu-id="1fba1-130">System Utilization Report</span></span>](system-utilization-reportserver.md)

 

 





