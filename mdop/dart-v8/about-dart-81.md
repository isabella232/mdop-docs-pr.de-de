---
title: Informationen zu DaRT 8.1
description: Informationen zu DaRT 8.1
author: dansimp
ms.assetid: dcaddc57-0111-4a9d-8be9-f5ada0eefa7d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 29c7522b4f5a5da3b451b23f2fd200db44bb9481
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808650"
---
# <span data-ttu-id="89ca9-103">Informationen zu DaRT 8.1</span><span class="sxs-lookup"><span data-stu-id="89ca9-103">About DaRT 8.1</span></span>


<span data-ttu-id="89ca9-104">Microsoft Diagnostics and Recovery Toolset (Dart) 8,1 bietet die folgenden Verbesserungen, die in diesem Thema beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="89ca9-104">Microsoft Diagnostics and Recovery Toolset (DaRT) 8.1 provides the following enhancements, which are described in this topic.</span></span>

## <a href="" id="what-s-new"></a><span data-ttu-id="89ca9-105">Neuigkeiten </span><span class="sxs-lookup"><span data-stu-id="89ca9-105">What’s new</span></span>


-   **<span data-ttu-id="89ca9-106">Unterstützung für WIMBoot</span><span class="sxs-lookup"><span data-stu-id="89ca9-106">Support for WIMBoot</span></span>**

    <span data-ttu-id="89ca9-107">Diagnose-und Wiederherstellungs-Toolset 8,1 unterstützt die Windows Image File Boot (WIMBoot)-Umgebung, wenn diese Bedingungen erfüllt sind:</span><span class="sxs-lookup"><span data-stu-id="89ca9-107">Diagnostics and Recovery Toolset 8.1 supports the Windows image file boot (WIMBoot) environment if these conditions are met:</span></span>

    -   <span data-ttu-id="89ca9-108">WIMBoot basiert auf Windows 8,1 Update 1 oder höher.</span><span class="sxs-lookup"><span data-stu-id="89ca9-108">WIMBoot is based on Windows 8.1 Update 1 or later.</span></span>

    -   <span data-ttu-id="89ca9-109">Das Dart 8,1-Bild ist auf Windows 8,1 Update 1 oder höher aufgebaut.</span><span class="sxs-lookup"><span data-stu-id="89ca9-109">The DaRT 8.1 image is built on Windows 8.1 Update 1 or later.</span></span>

    <span data-ttu-id="89ca9-110">Weitere Informationen zu WIMBoot finden Sie unter [Übersicht über den Windows-Image-Datei Start (WIMBoot)](https://go.microsoft.com/fwlink/?LinkId=517536).</span><span class="sxs-lookup"><span data-stu-id="89ca9-110">For more information about WIMBoot, see [Windows Image File Boot (WIMBoot) Overview](https://go.microsoft.com/fwlink/?LinkId=517536).</span></span>

-   **<span data-ttu-id="89ca9-111">Unterstützung für Windows Server 2012 R2 und Windows 8,1</span><span class="sxs-lookup"><span data-stu-id="89ca9-111">Support for Windows Server 2012 R2 and Windows 8.1</span></span>**

    <span data-ttu-id="89ca9-112">Sie können Dart-Bilder mithilfe von Windows Server 2012 R2 oder Windows 8,1 erstellen.</span><span class="sxs-lookup"><span data-stu-id="89ca9-112">You can create DaRT images by using Windows Server 2012 R2 or Windows 8.1.</span></span>

    **<span data-ttu-id="89ca9-113">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="89ca9-113">Note</span></span>**  
    <span data-ttu-id="89ca9-114">Verwenden Sie für frühere Versionen von Windows Server und Windows-Betriebssystemen die früheren Versionen von DART weiterhin.</span><span class="sxs-lookup"><span data-stu-id="89ca9-114">For earlier versions of the Windows Server and Windows operating systems, continue to use the earlier versions of DaRT.</span></span>



-   **<span data-ttu-id="89ca9-115">Kundenfeedback</span><span class="sxs-lookup"><span data-stu-id="89ca9-115">Customer feedback</span></span>**

    <span data-ttu-id="89ca9-116">Dart 8,1 enthält Updates zur Behebung von Problemen, die seit der Dart 8,0 SP1-Version gefunden wurden.</span><span class="sxs-lookup"><span data-stu-id="89ca9-116">DaRT 8.1 includes updates that address issues found since the DaRT 8.0 SP1 release.</span></span>

-   **<span data-ttu-id="89ca9-117">Windows Defender</span><span class="sxs-lookup"><span data-stu-id="89ca9-117">Windows Defender</span></span>**

    <span data-ttu-id="89ca9-118">Windows Defender in Windows 8,1 bietet verbesserten Schutz.</span><span class="sxs-lookup"><span data-stu-id="89ca9-118">Windows Defender in Windows 8.1 includes improved protection.</span></span> <span data-ttu-id="89ca9-119">Die Änderungen wirken sich nicht auf die Verwendung von Dart mit Windows Defender aus.</span><span class="sxs-lookup"><span data-stu-id="89ca9-119">The changes do not impact how you use DaRT with Windows Defender.</span></span>

## <span data-ttu-id="89ca9-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="89ca9-120">Requirements</span></span>


-   **<span data-ttu-id="89ca9-121">Windows Assessment und Development Kit 8,1</span><span class="sxs-lookup"><span data-stu-id="89ca9-121">Windows Assessment and Development Kit 8.1</span></span>**

    <span data-ttu-id="89ca9-122">Windows Assessment and Development Kit (ADK) 8,1 ist eine erforderliche Voraussetzung für den Dart-Wiederherstellungsbild-Assistenten.</span><span class="sxs-lookup"><span data-stu-id="89ca9-122">Windows Assessment and Development Kit (ADK) 8.1 is a required prerequisite for the DaRT Recovery Image Wizard.</span></span> <span data-ttu-id="89ca9-123">Windows ADK 8,1 enthält Bereitstellungstools, mit denen Windows-Bilder angepasst, bereitgestellt und gewartet werden können.</span><span class="sxs-lookup"><span data-stu-id="89ca9-123">Windows ADK 8.1 contains deployment tools that are used to customize, deploy, and service Windows images.</span></span> <span data-ttu-id="89ca9-124">Außerdem enthält Sie die Windows-Vorinstallationsumgebung (Windows PE).</span><span class="sxs-lookup"><span data-stu-id="89ca9-124">It also contains the Windows Preinstallation Environment (Windows PE).</span></span>

    **<span data-ttu-id="89ca9-125">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="89ca9-125">Note</span></span>**  
    <span data-ttu-id="89ca9-126">Windows ADK 8,1 ist nicht erforderlich, wenn Sie nur Remote Verbindungsanzeige oder Crash Analyzer installieren.</span><span class="sxs-lookup"><span data-stu-id="89ca9-126">Windows ADK 8.1 is not required if you are installing only Remote Connection Viewer or Crash Analyzer.</span></span>



~~~
To download Windows ADK 8.1, see [Windows Assessment and Deployment Kit (Windows ADK) for Windows 8.1](https://www.microsoft.com/download/details.aspx?id=39982) in the Microsoft Download Center.
~~~

-   **<span data-ttu-id="89ca9-127">Microsoft .NET Framework 4.5.1</span><span class="sxs-lookup"><span data-stu-id="89ca9-127">Microsoft .NET Framework 4.5.1</span></span>**

    <span data-ttu-id="89ca9-128">Für Dart 8,1 muss .NET Framework 4.5.1 installiert sein.</span><span class="sxs-lookup"><span data-stu-id="89ca9-128">DaRT 8.1 requires that .NET Framework 4.5.1 is installed.</span></span> <span data-ttu-id="89ca9-129">Informationen zum Herunterladen finden Sie unter [Microsoft.NET Framework 4.5.1](https://go.microsoft.com/fwlink/?LinkId=329038) im Microsoft Download Center.</span><span class="sxs-lookup"><span data-stu-id="89ca9-129">To download, see [Microsoft.NET Framework 4.5.1](https://go.microsoft.com/fwlink/?LinkId=329038) in the Microsoft Download Center.</span></span>

-   **<span data-ttu-id="89ca9-130">Windows 8,1-Debugging-Tools</span><span class="sxs-lookup"><span data-stu-id="89ca9-130">Windows 8.1 Debugging Tools</span></span>**

    <span data-ttu-id="89ca9-131">Wenn Sie das Crash Analyzer-Tool in Dart 8,1 verwenden möchten, benötigen Sie die erforderlichen Debugging-Tools, die im Software Development Kit für Windows 8,1 zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="89ca9-131">To use the Crash Analyzer tool in DaRT 8.1, you need the required debugging tools, which are available in the Software Development Kit for Windows 8.1.</span></span>

    <span data-ttu-id="89ca9-132">Informationen zum Herunterladen finden Sie unter [Windows Software Development Kit (SDK) für Windows 8,1](https://msdn.microsoft.com/library/windows/desktop/bg162891.aspx) im Microsoft Download Center.</span><span class="sxs-lookup"><span data-stu-id="89ca9-132">To download, see [Windows Software Development Kit (SDK) for Windows 8.1](https://msdn.microsoft.com/library/windows/desktop/bg162891.aspx) in the Microsoft Download Center.</span></span>

## <span data-ttu-id="89ca9-133">Verfügbarkeit von Sprachen</span><span class="sxs-lookup"><span data-stu-id="89ca9-133">Language availability</span></span>


<span data-ttu-id="89ca9-134">Dart 8,1 steht in den folgenden Sprachen zur Verfügung:</span><span class="sxs-lookup"><span data-stu-id="89ca9-134">DaRT 8.1 is available in the following languages:</span></span>

-   <span data-ttu-id="89ca9-135">Englisch (USA) en-US</span><span class="sxs-lookup"><span data-stu-id="89ca9-135">English (United States) en-US</span></span>

-   <span data-ttu-id="89ca9-136">Französisch (Frankreich) fr-FR</span><span class="sxs-lookup"><span data-stu-id="89ca9-136">French (France) fr-FR</span></span>

-   <span data-ttu-id="89ca9-137">Italienisch (Italien) IT-IT</span><span class="sxs-lookup"><span data-stu-id="89ca9-137">Italian (Italy) it-IT</span></span>

-   <span data-ttu-id="89ca9-138">Deutsch (Deutschland) de-de</span><span class="sxs-lookup"><span data-stu-id="89ca9-138">German (Germany) de-DE</span></span>

-   <span data-ttu-id="89ca9-139">Spanisch, internationale Sortierung (Spanien) es-es</span><span class="sxs-lookup"><span data-stu-id="89ca9-139">Spanish, International Sort (Spain) es-ES</span></span>

-   <span data-ttu-id="89ca9-140">Koreanisch (Korea) ko-kr</span><span class="sxs-lookup"><span data-stu-id="89ca9-140">Korean (Korea) ko-KR</span></span>

-   <span data-ttu-id="89ca9-141">Japanisch (Japan) ja-JP</span><span class="sxs-lookup"><span data-stu-id="89ca9-141">Japanese (Japan) ja-JP</span></span>

-   <span data-ttu-id="89ca9-142">Portugiesisch (Brasilien) pt-br</span><span class="sxs-lookup"><span data-stu-id="89ca9-142">Portuguese (Brazil) pt-BR</span></span>

-   <span data-ttu-id="89ca9-143">Russisch (Russland) ru-ru</span><span class="sxs-lookup"><span data-stu-id="89ca9-143">Russian (Russia) ru-RU</span></span>

-   <span data-ttu-id="89ca9-144">Chinesisch (traditionell) zh-tw</span><span class="sxs-lookup"><span data-stu-id="89ca9-144">Chinese Traditional zh-TW</span></span>

-   <span data-ttu-id="89ca9-145">Chinesisch (vereinfacht) zh-cn</span><span class="sxs-lookup"><span data-stu-id="89ca9-145">Chinese Simplified zh-CN</span></span>

## <span data-ttu-id="89ca9-146">So erhalten Sie MDOP-Technologien</span><span class="sxs-lookup"><span data-stu-id="89ca9-146">How to Get MDOP Technologies</span></span>


<span data-ttu-id="89ca9-147">Dart 8,1 ist Teil des Microsoft Desktop Optimization Pack (MDOP).</span><span class="sxs-lookup"><span data-stu-id="89ca9-147">DaRT 8.1 is a part of the Microsoft Desktop Optimization Pack (MDOP).</span></span> <span data-ttu-id="89ca9-148">MDOP ist Teil von Microsoft Software Assurance.</span><span class="sxs-lookup"><span data-stu-id="89ca9-148">MDOP is part of Microsoft Software Assurance.</span></span> <span data-ttu-id="89ca9-149">Weitere Informationen zur Microsoft-Software Assurance und zum Erwerb von MDOP finden Sie unter [wie erhalte ich MDOP](https://go.microsoft.com/fwlink/?LinkId=322049) ( https://go.microsoft.com/fwlink/?LinkId=322049) .</span><span class="sxs-lookup"><span data-stu-id="89ca9-149">For more information about Microsoft Software Assurance and acquiring MDOP, see [How Do I Get MDOP](https://go.microsoft.com/fwlink/?LinkId=322049) (https://go.microsoft.com/fwlink/?LinkId=322049).</span></span>

## <span data-ttu-id="89ca9-150">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="89ca9-150">Related topics</span></span>


[<span data-ttu-id="89ca9-151">Versionshinweise für DaRT 8.1</span><span class="sxs-lookup"><span data-stu-id="89ca9-151">Release Notes for DaRT 8.1</span></span>](release-notes-for-dart-81.md)









