---
title: Planen der Erstellung des DaRT 7.0-Wiederherstellungsabbilds
description: Planen der Erstellung des DaRT 7.0-Wiederherstellungsabbilds
author: dansimp
ms.assetid: e5d49bee-ae4e-467b-9976-c1203f6355f9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: c370d2a69ec8ccea217696045e64e9a0ae724815
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808692"
---
# <span data-ttu-id="9b985-103">Planen der Erstellung des DaRT 7.0-Wiederherstellungsabbilds</span><span class="sxs-lookup"><span data-stu-id="9b985-103">Planning to Create the DaRT 7.0 Recovery Image</span></span>


<span data-ttu-id="9b985-104">Verwenden Sie die Informationen in diesem Abschnitt, wenn Sie die Erstellung des Microsoft Diagnostics and Recovery Toolset (Dart) 7-Wiederherstellungs Bilds planen.</span><span class="sxs-lookup"><span data-stu-id="9b985-104">Use the information in this section when you plan for creating the Microsoft Diagnostics and Recovery Toolset (DaRT)7 recovery image.</span></span>

## <span data-ttu-id="9b985-105">Planen des Erstellens des DART 7-Wiederherstellungs Bilds</span><span class="sxs-lookup"><span data-stu-id="9b985-105">Planning to Create the DaRT 7 Recovery Image</span></span>


<span data-ttu-id="9b985-106">Wenn Sie das DART-Wiederherstellungsbild erstellen, müssen Sie entscheiden, welche Tools in das Bild aufgenommen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="9b985-106">When you create the DaRT recovery image, you have to decide which tools to include on the image.</span></span> <span data-ttu-id="9b985-107">Beachten Sie, dass die Endbenutzer möglicherweise gelegentlich Zugriff auf die verschiedenen Dart-Tools haben, wenn Sie diese Entscheidung treffen.</span><span class="sxs-lookup"><span data-stu-id="9b985-107">When you make that decision, remember that end users might have access occasionally to the various DaRT tools.</span></span> <span data-ttu-id="9b985-108">Weitere Informationen zu den Dart-Tools finden Sie unter [Übersicht über die Tools in DART 7,0](overview-of-the-tools-in-dart-70-new-ia.md).</span><span class="sxs-lookup"><span data-stu-id="9b985-108">For more information about the DaRT tools, see [Overview of the Tools in DaRT 7.0](overview-of-the-tools-in-dart-70-new-ia.md).</span></span> <span data-ttu-id="9b985-109">Weitere Informationen dazu, wie Sie bei der Erstellung eines sicheren Wiederherstellungs Bilds helfen können, finden Sie unter [Sicherheitsüberlegungen für Dart 7,0](security-considerations-for-dart-70-dart-7.md).</span><span class="sxs-lookup"><span data-stu-id="9b985-109">For more information about how to help create a secure recovery image, see [Security Considerations for DaRT 7.0](security-considerations-for-dart-70-dart-7.md).</span></span>

<span data-ttu-id="9b985-110">Wenn Sie das DART-Wiederherstellungsabbild erstellen, geben Sie auch an, ob Sie weitere Treiber oder Dateien einbeziehen möchten.</span><span class="sxs-lookup"><span data-stu-id="9b985-110">When you create the DaRT recovery image, you will also specify whether you want to include additional drivers or files.</span></span> <span data-ttu-id="9b985-111">Ermitteln Sie die Speicherorte zusätzlicher Treiber oder Dateien, die Sie in das DART-Wiederherstellungsabbild einbeziehen möchten.</span><span class="sxs-lookup"><span data-stu-id="9b985-111">Determine the locations of any additional drivers or files that you want to include on the DaRT recovery image.</span></span>

## <span data-ttu-id="9b985-112">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="9b985-112">Prerequisites</span></span>


<span data-ttu-id="9b985-113">Die folgenden Elemente sind für das Erstellen des DART-Wiederherstellungs Bilds erforderlich oder empfohlen:</span><span class="sxs-lookup"><span data-stu-id="9b985-113">The following items are required or recommended for creating the DaRT recovery image:</span></span>

-   <span data-ttu-id="9b985-114">Windows 7-Quelldateien</span><span class="sxs-lookup"><span data-stu-id="9b985-114">Windows 7 source files</span></span>

    <span data-ttu-id="9b985-115">Sie müssen den Pfad einer Windows 7-DVD oder von Windows 7-Quelldateien angeben.</span><span class="sxs-lookup"><span data-stu-id="9b985-115">You must provide the path of a Windows 7 DVD or of Windows 7 source files.</span></span> <span data-ttu-id="9b985-116">Zum Erstellen des DART-Wiederherstellungs Bilds sind Windows 7-Quelldateien erforderlich.</span><span class="sxs-lookup"><span data-stu-id="9b985-116">Windows 7 source files are required to create the DaRT recovery image.</span></span>

-   <span data-ttu-id="9b985-117">Windows-Debugging-Tools für Ihre Plattform</span><span class="sxs-lookup"><span data-stu-id="9b985-117">Windows Debugging Tools for your platform</span></span>

    <span data-ttu-id="9b985-118">Windows-Debugging-Tools sind erforderlich, wenn Sie **Crash Analyzer** ausführen, um die Ursache für einen Computerabsturz zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="9b985-118">Windows Debugging Tools are required when you run **Crash Analyzer** to determine the cause of a computer crash.</span></span> <span data-ttu-id="9b985-119">Wir empfehlen, dass Sie den Pfad der Windows-Debugging-Tools angeben, wenn Sie das DART-Wiederherstellungsabbild erstellen.</span><span class="sxs-lookup"><span data-stu-id="9b985-119">We recommend that you specify the path of the Windows Debugging Tools at the time that you create the DaRT recovery image.</span></span> <span data-ttu-id="9b985-120">Wenn dies erforderlich ist, können Sie die Windows-Debugging-Tools hier herunterladen: [herunterladen und Installieren von Debugging-Tools für Windows](https://go.microsoft.com/fwlink/?LinkId=99934).</span><span class="sxs-lookup"><span data-stu-id="9b985-120">If it is necessary, you can download the Windows Debugging Tools here: [Download and Install Debugging Tools for Windows](https://go.microsoft.com/fwlink/?LinkId=99934).</span></span>

-   <span data-ttu-id="9b985-121">Optional: **eigenständige System Sweeper** -Definitionen</span><span class="sxs-lookup"><span data-stu-id="9b985-121">Optional: **Standalone System Sweeper** definitions</span></span>

    <span data-ttu-id="9b985-122">Wenn Sie dieses Tool ausführen, sind die neuesten Definitionen für das **Standalone-System Sweeper** erforderlich.</span><span class="sxs-lookup"><span data-stu-id="9b985-122">The latest definitions for the **Standalone System Sweeper** are required when you run this tool.</span></span> <span data-ttu-id="9b985-123">Obwohl Sie die Definitionen herunterladen können, wenn Sie **Standalone-System Sweeper**ausführen, empfehlen wir, dass Sie die neuesten Definitionen zum Zeitpunkt der Erstellung des DART-Wiederherstellungsabbilds herunterladen.</span><span class="sxs-lookup"><span data-stu-id="9b985-123">Although you can download the definitions when you run **Standalone System Sweeper**, we recommend that you download the latest definitions at the time you create the DaRT recovery image.</span></span> <span data-ttu-id="9b985-124">Auf diese Weise können Sie das Tool weiterhin mit den neuesten Definitionen ausführen, auch wenn der Problem Computer nicht über Netzwerkkonnektivität verfügt.</span><span class="sxs-lookup"><span data-stu-id="9b985-124">In this manner, you can still run the tool with the latest definitions even if the problem computer does not have network connectivity.</span></span>

-   <span data-ttu-id="9b985-125">Optional: Windows-Symbole-Dateien für die Verwendung mit **Crash Analyzer**</span><span class="sxs-lookup"><span data-stu-id="9b985-125">Optional: Windows symbols files for use with **Crash Analyzer**</span></span>

    <span data-ttu-id="9b985-126">In der Regel werden Debuginformationen in einer Symboldatei gespeichert, die von der ausführbaren Datei getrennt ist.</span><span class="sxs-lookup"><span data-stu-id="9b985-126">Typically, debugging information is stored in a symbol file that is separate from the executable.</span></span> <span data-ttu-id="9b985-127">Sie müssen Zugriff auf die Symbol Informationen haben, wenn Sie eine Anwendung debuggen, die nicht mehr reagiert, beispielsweise wenn Sie abgestürzt ist.</span><span class="sxs-lookup"><span data-stu-id="9b985-127">You must have access to the symbol information when you debug an application that has stopped responding, for example if it crashed.</span></span> <span data-ttu-id="9b985-128">Weitere Informationen finden Sie unter [Diagnostizieren von System Fehlern mit Crash Analyzer](diagnosing-system-failures-with-crash-analyzer--dart-7.md).</span><span class="sxs-lookup"><span data-stu-id="9b985-128">For more information, see [Diagnosing System Failures with Crash Analyzer](diagnosing-system-failures-with-crash-analyzer--dart-7.md).</span></span>

## <span data-ttu-id="9b985-129">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="9b985-129">Related topics</span></span>


[<span data-ttu-id="9b985-130">Planen der Bereitstellung von DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="9b985-130">Planning to Deploy DaRT 7.0</span></span>](planning-to-deploy-dart-70.md)

 

 





