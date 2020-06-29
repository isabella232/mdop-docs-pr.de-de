---
title: Planen der Bereitstellung von DaRT 7.0
description: Planen der Bereitstellung von DaRT 7.0
author: dansimp
ms.assetid: 05e97cdb-a8c2-46e4-9c75-a7d12fe26fe8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 09725e994a95f4f93ae655402e7577e137e33f18
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808683"
---
# <span data-ttu-id="6b05f-103">Planen der Bereitstellung von DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="6b05f-103">Planning to Deploy DaRT 7.0</span></span>


<span data-ttu-id="6b05f-104">Es gibt eine Reihe unterschiedlicher Bereitstellungskonfigurationen und Voraussetzungen, die Sie berücksichtigen müssen, bevor Sie Ihren Bereitstellungsplan erstellen.</span><span class="sxs-lookup"><span data-stu-id="6b05f-104">There are a number of different deployment configurations and prerequisites that you must consider before you create your deployment plan.</span></span> <span data-ttu-id="6b05f-105">Dieser Abschnitt enthält Informationen, die Ihnen bei der Erfassung der Informationen helfen können, die Sie benötigen, um einen Bereitstellungsplan zu formulieren, der Ihren geschäftlichen Anforderungen am besten entspricht.</span><span class="sxs-lookup"><span data-stu-id="6b05f-105">This section includes information that can help you gather the information that you must have to formulate a deployment plan that best meets your business requirements.</span></span>

<span data-ttu-id="6b05f-106">Wenn Sie die Installation von Microsoft Diagnostics and Recovery Toolset (Dart) 7 planen, sollten Sie Folgendes bedenken:</span><span class="sxs-lookup"><span data-stu-id="6b05f-106">Consider the following when you plan your Microsoft Diagnostics and Recovery Toolset (DaRT)7 installation:</span></span>

-   <span data-ttu-id="6b05f-107">Wenn Sie Dart installieren, können Sie entweder alle Funktionen auf einem IT-Administratorcomputer installieren, auf dem Sie alle Aufgaben ausführen, die mit der Ausführung von DART verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="6b05f-107">When you install DaRT, you can either install all functionality on an IT administrator computer where you will perform all the tasks associated with running DaRT.</span></span> <span data-ttu-id="6b05f-108">Oder Sie können nur die Dart-Funktionalität installieren, die das Wiederherstellungsabbild auf dem IT-Administratorcomputer erstellt.</span><span class="sxs-lookup"><span data-stu-id="6b05f-108">Or you can install only the DaRT functionality that creates the recovery image on the IT administrator computer.</span></span> <span data-ttu-id="6b05f-109">Installieren Sie dann die zum Ausführen von DART verwendete Funktionalität wie **Dart Remote Connection Viewer** und **Crash Analyzer**auf einem Helpdesk-Agent-Computer.</span><span class="sxs-lookup"><span data-stu-id="6b05f-109">Then, install the functionality used to run DaRT, such as the **DaRT Remote Connection Viewer** and **Crash Analyzer**, on a helpdesk agent computer.</span></span>

-   <span data-ttu-id="6b05f-110">Damit Sie Dart Remote ausführen können, stellen Sie sicher, dass sich der Helpdesk-Agent-Computer und alle Computer, für die Sie möglicherweise eine Remote Behandlung durchführen, im gleichen Netzwerk befinden.</span><span class="sxs-lookup"><span data-stu-id="6b05f-110">To be able to run DaRT remotely, make sure that the helpdesk agent computer and all computers that you might be troubleshooting remotely are on the same network.</span></span>

-   <span data-ttu-id="6b05f-111">Bevor Sie Dart in die Produktion einführen, können Sie zunächst eine Lab-Umgebung für Tests erstellen.</span><span class="sxs-lookup"><span data-stu-id="6b05f-111">Before you roll out DaRT into production, you can first build a lab environment for testing.</span></span> <span data-ttu-id="6b05f-112">Ein Testlabor sollte mindestens zwei Computer umfassen, eines, das als IT-Administrator/Helpdesk-Agent-Computer fungiert, und eines, das als Endbenutzercomputer fungieren soll.</span><span class="sxs-lookup"><span data-stu-id="6b05f-112">A test lab should include a minimum of two computers, one to act as the IT administrator/helpdesk agent computer and one to act as an end-user computer.</span></span> <span data-ttu-id="6b05f-113">Sie können auch drei Computer in der Übungseinheit verwenden, wenn Sie die Zuständigkeiten des IT-Administrators von denen des Helpdesk-Agents trennen möchten.</span><span class="sxs-lookup"><span data-stu-id="6b05f-113">Or, you can use three computers in your lab if you want to separate the IT administrator responsibilities from those of the helpdesk agent.</span></span>

## <span data-ttu-id="6b05f-114">Überprüfen der unterstützten Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="6b05f-114">Review the supported configurations</span></span>


<span data-ttu-id="6b05f-115">Überprüfen Sie die unterstützten Konfigurationsinformationen des Microsoft Diagnostics and Recovery Toolset (Dart) 7, um zu bestätigen, dass die Computer, die Sie für die Client-oder Feature-Installation ausgewählt haben, die Mindestanforderungen für Hardware und Betriebssystem erfüllen.</span><span class="sxs-lookup"><span data-stu-id="6b05f-115">You should review the Microsoft Diagnostics and Recovery Toolset (DaRT)7 Supported Configurations information to confirm that the computers you have selected for client or feature installation meet the minimum hardware and operating system requirements.</span></span>

[<span data-ttu-id="6b05f-116">Von DaRT 7.0 unterstützte Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="6b05f-116">DaRT 7.0 Supported Configurations</span></span>](dart-70-supported-configurations-dart-7.md)

## <span data-ttu-id="6b05f-117">Planen des Erstellens des DART-Wiederherstellungs Bilds</span><span class="sxs-lookup"><span data-stu-id="6b05f-117">Plan for creating the DaRT recovery image</span></span>


<span data-ttu-id="6b05f-118">Wenn Sie das DART-Wiederherstellungsbild erstellen, müssen Sie entscheiden, welche Tools in das Bild aufgenommen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="6b05f-118">When you create the DaRT recovery image, you have to decide which tools to include on the image.</span></span> <span data-ttu-id="6b05f-119">Beachten Sie, dass die Endbenutzer möglicherweise gelegentlich Zugriff auf die verschiedenen Dart-Tools haben, wenn Sie diese Entscheidung treffen.</span><span class="sxs-lookup"><span data-stu-id="6b05f-119">When you make that decision, remember that end users might have access occasionally to the various DaRT tools.</span></span> <span data-ttu-id="6b05f-120">Wenn Sie das Wiederherstellungsabbild erstellen, geben Sie auch an, ob Sie weitere Treiber oder Dateien einbeziehen möchten.</span><span class="sxs-lookup"><span data-stu-id="6b05f-120">When you create the recovery image, you will also specify whether you want to include additional drivers or files.</span></span> <span data-ttu-id="6b05f-121">Ermitteln Sie die Speicherorte zusätzlicher Treiber oder Dateien, die Sie in das DART-Wiederherstellungsabbild einbeziehen möchten.</span><span class="sxs-lookup"><span data-stu-id="6b05f-121">Determine the locations of any additional drivers or files that you want to include on the DaRT recovery image.</span></span>

<span data-ttu-id="6b05f-122">Beachten Sie die Voraussetzungen und weitere zusätzliche Planungsempfehlungen für die Erstellung des DART-Wiederherstellungs Bilds.</span><span class="sxs-lookup"><span data-stu-id="6b05f-122">You should be aware of the prerequisites and other additional planning recommendations for creating the DaRT recovery image.</span></span>

[<span data-ttu-id="6b05f-123">Planen der Erstellung des DaRT 7.0-Wiederherstellungsabbilds</span><span class="sxs-lookup"><span data-stu-id="6b05f-123">Planning to Create the DaRT 7.0 Recovery Image</span></span>](planning-to-create-the-dart-70-recovery-image.md)

## <span data-ttu-id="6b05f-124">Planen des Speicherns und Bereitstellens des DART-Wiederherstellungs Bilds</span><span class="sxs-lookup"><span data-stu-id="6b05f-124">Plan for saving and deploying the DaRT recovery image</span></span>


<span data-ttu-id="6b05f-125">Zum Speichern und Bereitstellen des DART-Wiederherstellungs Bilds können verschiedene Methoden verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6b05f-125">Several methods can be used to save and deploy the DaRT recovery image.</span></span> <span data-ttu-id="6b05f-126">Berücksichtigen Sie die vor-und Nachteile der einzelnen Methoden, wenn Sie die Methode ermitteln, die Sie verwenden werden.</span><span class="sxs-lookup"><span data-stu-id="6b05f-126">When you are determining the method that you will use, consider the advantages and disadvantages of each.</span></span> <span data-ttu-id="6b05f-127">Denken Sie auch daran, wie Sie Dart in Ihrem Unternehmen verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="6b05f-127">Also, consider how you want to use DaRT in your enterprise.</span></span>

<span data-ttu-id="6b05f-128">**Hinweis**  Möglicherweise möchten Sie in Ihrer Organisation mehr als eine Methode verwenden.</span><span class="sxs-lookup"><span data-stu-id="6b05f-128">**Note** You might want to use more than one method in your organization.</span></span> <span data-ttu-id="6b05f-129">So können Sie beispielsweise für die meisten Situationen in DART von einer Remotepartition Booten und einen USB-Stick zur Verfügung stellen, falls der Endbenutzercomputer keine Verbindung mit dem Netzwerk herstellen kann.</span><span class="sxs-lookup"><span data-stu-id="6b05f-129">For example, you can boot into DaRT from a remote partition for most situations and have a USB flash drive available in case the end-user computer cannot connect to the network.</span></span>

 

[<span data-ttu-id="6b05f-130">Planen der Speicherung und Bereitstellung des DaRT 7.0-Wiederherstellungsabbilds</span><span class="sxs-lookup"><span data-stu-id="6b05f-130">Planning How to Save and Deploy the DaRT 7.0 Recovery Image</span></span>](planning-how-to-save-and-deploy-the-dart-70-recovery-image.md)

## <span data-ttu-id="6b05f-131">Weitere Ressourcen für die Planung der Bereitstellung von Dart</span><span class="sxs-lookup"><span data-stu-id="6b05f-131">Other resources for Planning to Deploy DaRT</span></span>


[<span data-ttu-id="6b05f-132">Planen von DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="6b05f-132">Planning for DaRT 7.0</span></span>](planning-for-dart-70-new-ia.md)

 

 





