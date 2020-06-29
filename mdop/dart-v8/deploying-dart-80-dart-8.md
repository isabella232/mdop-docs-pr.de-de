---
title: Bereitstellen von DaRT 8.0
description: Bereitstellen von DaRT 8.0
author: dansimp
ms.assetid: 5a976d4e-3372-4ef6-9095-1b48e99af21b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 7cc847836587abb0eaa22c009c8fd18d0ba0899b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810390"
---
# <span data-ttu-id="22fb6-103">Bereitstellen von DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="22fb6-103">Deploying DaRT 8.0</span></span>


<span data-ttu-id="22fb6-104">Microsoft Diagnostics and Recovery Toolset (Dart) 8,0 unterstützt eine Reihe unterschiedlicher Bereitstellungskonfigurationen.</span><span class="sxs-lookup"><span data-stu-id="22fb6-104">Microsoft Diagnostics and Recovery Toolset (DaRT) 8.0 supports a number of different deployment configurations.</span></span> <span data-ttu-id="22fb6-105">Dieser Abschnitt enthält Informationen, die Sie über die Bereitstellung von Dart 8,0 und Schritt-für-Schritt-Verfahren berücksichtigen sollten, damit Sie die Aufgaben, die Sie in verschiedenen Phasen Ihrer Bereitstellung ausführen müssen, erfolgreich durchführen können.</span><span class="sxs-lookup"><span data-stu-id="22fb6-105">This section includes information you should consider about the deployment of DaRT 8.0 and step-by-step procedures to help you successfully perform the tasks that you must complete at different stages of your deployment.</span></span>

## <span data-ttu-id="22fb6-106">Bereitstellungsinformationen</span><span class="sxs-lookup"><span data-stu-id="22fb6-106">Deployment Information</span></span>


-   [<span data-ttu-id="22fb6-107">Bereitstellen von DaRT 8.0 für Administratorcomputer</span><span class="sxs-lookup"><span data-stu-id="22fb6-107">Deploying DaRT 8.0 to Administrator Computers</span></span>](deploying-dart-80-to-administrator-computers-dart-8.md)

    <span data-ttu-id="22fb6-108">In diesem Abschnitt werden die verschiedenen Dart-Bereitstellungsoptionen für Ihre Anforderungen beschrieben und erläutert, wie Sie bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="22fb6-108">This section describes the different DaRT deployment options for your requirements and explains how to deploy them.</span></span>

-   [<span data-ttu-id="22fb6-109">Erstellen des DaRT 8.0-Wiederherstellungsabbilds</span><span class="sxs-lookup"><span data-stu-id="22fb6-109">Creating the DaRT 8.0 Recovery Image</span></span>](creating-the-dart-80-recovery-image-dart-8.md)

    <span data-ttu-id="22fb6-110">In diesem Abschnitt werden die Methoden beschrieben, mit denen Sie das DART-Wiederherstellungsabbild erstellen können, und es werden Anweisungen zum Erstellen des Wiederherstellungs Bilds mithilfe des DART-Wiederherstellungsbild-Assistenten bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="22fb6-110">This section describes the methods you can use to create the DaRT recovery image and provides instructions to create the recovery image by using the DaRT Recovery Image wizard.</span></span>

-   [<span data-ttu-id="22fb6-111">Bereitstellen der DaRT-Recovery-Images</span><span class="sxs-lookup"><span data-stu-id="22fb6-111">Deploying the DaRT Recovery Image</span></span>](deploying-the-dart-recovery-image-dart-8.md)

    <span data-ttu-id="22fb6-112">Dieser Abschnitt enthält Informationen, die Ihnen bei der Entscheidung für die beste Dart-Wiederherstellungs-Image-Bereitstellungsoption für Ihre Anforderungen helfen, und enthält Anweisungen zum Bereitstellen des Wiederherstellungsabbilds.</span><span class="sxs-lookup"><span data-stu-id="22fb6-112">This section provides information to help you decide on the best DaRT recovery image deployment option for your requirements and provides instructions on how to deploy the recovery image.</span></span>

-   [<span data-ttu-id="22fb6-113">Prüfliste für die Bereitstellung von DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="22fb6-113">DaRT 8.0 Deployment Checklist</span></span>](dart-80-deployment-checklist-dart-8.md)

    <span data-ttu-id="22fb6-114">Dieser Abschnitt enthält eine Checkliste für die Bereitstellung, die Ihnen bei der Bereitstellung von DART helfen kann.</span><span class="sxs-lookup"><span data-stu-id="22fb6-114">This section contains a deployment checklist that can help you to deploy DaRT.</span></span>

### <span data-ttu-id="22fb6-115">So erhalten Sie Dart</span><span class="sxs-lookup"><span data-stu-id="22fb6-115">How to get DaRT</span></span>

<span data-ttu-id="22fb6-116">Diese Technologie ist Teil des Microsoft Desktop Optimization Pack (MDOP).</span><span class="sxs-lookup"><span data-stu-id="22fb6-116">This technology is a part of the Microsoft Desktop Optimization Pack (MDOP).</span></span> <span data-ttu-id="22fb6-117">Unternehmenskunden können MDOP mit Microsoft Software Assurance erhalten.</span><span class="sxs-lookup"><span data-stu-id="22fb6-117">Enterprise customers can get MDOP with Microsoft Software Assurance.</span></span> <span data-ttu-id="22fb6-118">Weitere Informationen zur Microsoft-Software Assurance und zum Erwerb von MDOP finden Sie unter [wie erhalte ich MDOP](https://go.microsoft.com/fwlink/p/?LinkId=322049) ( https://go.microsoft.com/fwlink/p/?LinkId=322049) .</span><span class="sxs-lookup"><span data-stu-id="22fb6-118">For more information about Microsoft Software Assurance and acquiring MDOP, see [How Do I Get MDOP](https://go.microsoft.com/fwlink/p/?LinkId=322049) (https://go.microsoft.com/fwlink/p/?LinkId=322049).</span></span>

## <span data-ttu-id="22fb6-119">Weitere Ressourcen für die Bereitstellung von Dart</span><span class="sxs-lookup"><span data-stu-id="22fb6-119">Other Resources for deploying DaRT</span></span>


[<span data-ttu-id="22fb6-120">Diagnose-und Wiederherstellungs-Toolset 8 – Administrator Handbuch</span><span class="sxs-lookup"><span data-stu-id="22fb6-120">Diagnostics and Recovery Toolset 8 Administrator's Guide</span></span>](index.md)

[<span data-ttu-id="22fb6-121">Erste Schritte mit DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="22fb6-121">Getting Started with DaRT 8.0</span></span>](getting-started-with-dart-80-dart-8.md)

[<span data-ttu-id="22fb6-122">Planen von DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="22fb6-122">Planning for DaRT 8.0</span></span>](planning-for-dart-80-dart-8.md)

[<span data-ttu-id="22fb6-123">Vorgänge für DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="22fb6-123">Operations for DaRT 8.0</span></span>](operations-for-dart-80-dart-8.md)

[<span data-ttu-id="22fb6-124">Problembehandlung für DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="22fb6-124">Troubleshooting DaRT 8.0</span></span>](troubleshooting-dart-80-dart-8.md)

 

 





