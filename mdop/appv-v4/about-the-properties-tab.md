---
title: Informationen zur Registerkarte „Eigenschaften“
description: Informationen zur Registerkarte „Eigenschaften“
author: dansimp
ms.assetid: a6cf6f51-3778-4c8d-9632-3af4005775d2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4b2d6c3e01dde48fdd6701984f66610ea0333b74
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808100"
---
# <span data-ttu-id="c434c-103">Informationen zur Registerkarte „Eigenschaften“</span><span class="sxs-lookup"><span data-stu-id="c434c-103">About the Properties Tab</span></span>


<span data-ttu-id="c434c-104">Verwenden Sie die Registerkarte **Eigenschaften** , um grundlegende statistische Informationen zu einem sequenzierten Anwendungspaket anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="c434c-104">Use the **Properties** tab to view basic statistical information about a sequenced application package.</span></span> <span data-ttu-id="c434c-105">Sofern nicht anders angegeben, werden die Informationen automatisch generiert.</span><span class="sxs-lookup"><span data-stu-id="c434c-105">The information is automatically generated unless otherwise noted.</span></span> <span data-ttu-id="c434c-106">Diese Registerkarte enthält die folgenden Elemente.</span><span class="sxs-lookup"><span data-stu-id="c434c-106">This tab contains the following elements.</span></span>

## <span data-ttu-id="c434c-107">Paketinformationen</span><span class="sxs-lookup"><span data-stu-id="c434c-107">Package Information</span></span>


<a href="" id="package-name"></a>**<span data-ttu-id="c434c-108">Paket Name</span><span class="sxs-lookup"><span data-stu-id="c434c-108">Package Name</span></span>**  
<span data-ttu-id="c434c-109">Der einzelne Name für ein sequenziertes Anwendungspaket, das möglicherweise eine oder mehrere Anwendungen enthält – beispielsweise kann Microsoft Office verwendet werden, um ein sequenziertes Anwendungspaket zu beschriften, das Microsoft Word-und Microsoft Excel-Anwendungen enthält, die in derselben virtuellen Umgebung ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="c434c-109">The single name used for a sequenced application package that might contain one or more applications—for example, Microsoft Office could be used to label a sequenced application package that contains Microsoft Word and Microsoft Excel applications that run in the same virtual environment.</span></span>

<a href="" id="comments"></a>**<span data-ttu-id="c434c-110">Anmerkungen</span><span class="sxs-lookup"><span data-stu-id="c434c-110">Comments</span></span>**  
<span data-ttu-id="c434c-111">Zeigt eine kurze Beschreibung des Softwarepakets an, das im abstrakten Element "Open Software Descriptor (OSD)-Datei" angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="c434c-111">Displays a short description of the software package that will appear in the Open Software Descriptor (OSD) file ABSTRACT element.</span></span> <span data-ttu-id="c434c-112">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="c434c-112">This item is optional.</span></span>

<a href="" id="package-version"></a>**<span data-ttu-id="c434c-113">Paket Version</span><span class="sxs-lookup"><span data-stu-id="c434c-113">Package Version</span></span>**  
<span data-ttu-id="c434c-114">Die Version des sequenzierten Anwendungspakets.</span><span class="sxs-lookup"><span data-stu-id="c434c-114">The sequenced application package version.</span></span>

<a href="" id="package-guid"></a>**<span data-ttu-id="c434c-115">Paket-GUID</span><span class="sxs-lookup"><span data-stu-id="c434c-115">Package GUID</span></span>**  
<span data-ttu-id="c434c-116">Die GUID (Globally Unique Identifier), die dem sequenzierten Anwendungspaket automatisch zugewiesen wird, um Sie von anderen sequenzierten Anwendungspaketen zu unterscheiden, die möglicherweise auf dem Computer ausgeführt werden, auf dem ein sequenziertes Anwendungspaket gestreamt wird.</span><span class="sxs-lookup"><span data-stu-id="c434c-116">The globally unique identifier (GUID) automatically assigned to the sequenced application package to distinguish it from other sequenced application packages that might be running on the computer to which a sequenced application package is streamed.</span></span>

<a href="" id="package-version-guid"></a>**<span data-ttu-id="c434c-117">Paketversions-GUID</span><span class="sxs-lookup"><span data-stu-id="c434c-117">Package Version GUID</span></span>**  
<span data-ttu-id="c434c-118">Die Versions-GUID des sequenzierten Anwendungspakets.</span><span class="sxs-lookup"><span data-stu-id="c434c-118">The sequenced application package version GUID.</span></span>

<a href="" id="root-directory"></a>**<span data-ttu-id="c434c-119">Stammverzeichnis</span><span class="sxs-lookup"><span data-stu-id="c434c-119">Root Directory</span></span>**  
<span data-ttu-id="c434c-120">Das Verzeichnis auf dem Sequenzcomputer, in dem Dateien für das sequenzierte Anwendungspaket installiert sind.</span><span class="sxs-lookup"><span data-stu-id="c434c-120">The directory on the sequencing computer in which files for the sequenced application package are installed.</span></span> <span data-ttu-id="c434c-121">Dieses Verzeichnis wird auch auf dem Computer erstellt, auf dem ein sequenziertes Anwendungspaket gestreamt wird.</span><span class="sxs-lookup"><span data-stu-id="c434c-121">This directory is also created on the computer to which a sequenced application package will be streamed.</span></span> <span data-ttu-id="c434c-122">Es wird empfohlen, für die Abwärtskompatibilität zu sorgen, dass es sich um einen 8,3-Format Verzeichnisnamen am Stamm des Q-Laufwerks handelt, beispielsweise Q:\\MyApp.1\\.</span><span class="sxs-lookup"><span data-stu-id="c434c-122">It is recommended for backwards compatibility that this be an 8.3 format directory name at the root of the Q drive, such as Q:\\MyApp.1\\.</span></span>

<a href="" id="created"></a>**<span data-ttu-id="c434c-123">Erstellt</span><span class="sxs-lookup"><span data-stu-id="c434c-123">Created</span></span>**  
<span data-ttu-id="c434c-124">Das Datum und die Uhrzeit der Erstellung des sequenzierten Anwendungspakets.</span><span class="sxs-lookup"><span data-stu-id="c434c-124">The date and time the sequenced application package was created.</span></span>

<a href="" id="modified"></a>**<span data-ttu-id="c434c-125">Geändert</span><span class="sxs-lookup"><span data-stu-id="c434c-125">Modified</span></span>**  
<span data-ttu-id="c434c-126">Das Datum und die Uhrzeit, zu der das sequenzierte Anwendungspaket zuletzt geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="c434c-126">The date and time the sequenced application package was last modified.</span></span>

<a href="" id="package-size"></a>**<span data-ttu-id="c434c-127">Paketgröße</span><span class="sxs-lookup"><span data-stu-id="c434c-127">Package Size</span></span>**  
<span data-ttu-id="c434c-128">Die Größe des Pakets in Megabytes.</span><span class="sxs-lookup"><span data-stu-id="c434c-128">The size of the package in megabytes.</span></span>

<a href="" id="launch-size"></a>**<span data-ttu-id="c434c-129">Startgröße</span><span class="sxs-lookup"><span data-stu-id="c434c-129">Launch Size</span></span>**  
<span data-ttu-id="c434c-130">Die Größe in Megabyte des Teils der SFT-Datei, die zum Starten der Anwendung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="c434c-130">The size in megabytes of the portion of the SFT file that is required to start the application.</span></span>

## <span data-ttu-id="c434c-131">Sequenz Parameter</span><span class="sxs-lookup"><span data-stu-id="c434c-131">Sequencing Parameters</span></span>


<a href="" id="block-size"></a>**<span data-ttu-id="c434c-132">Block Größe</span><span class="sxs-lookup"><span data-stu-id="c434c-132">Block Size</span></span>**  
<span data-ttu-id="c434c-133">Gibt die Größe des primären und des sekundären Funktionsblocks an, in die die SFT-Datei für das Streaming in einem Netzwerk aufgeteilt wird.</span><span class="sxs-lookup"><span data-stu-id="c434c-133">Specifies the size of the primary and secondary feature blocks into which the SFT file is divided for streaming across a network.</span></span> <span data-ttu-id="c434c-134">Alle Blöcke entsprechen der angegebenen Größe; Allerdings kann der letzte Block kleiner als angegeben sein.</span><span class="sxs-lookup"><span data-stu-id="c434c-134">All blocks equal the specified size; however, the last block might be smaller than specified.</span></span> <span data-ttu-id="c434c-135">Es wird einer der folgenden Werte angezeigt:</span><span class="sxs-lookup"><span data-stu-id="c434c-135">You will see one of the following values:</span></span>

-   <span data-ttu-id="c434c-136">4 KB</span><span class="sxs-lookup"><span data-stu-id="c434c-136">4 KB</span></span>

-   <span data-ttu-id="c434c-137">16 KB</span><span class="sxs-lookup"><span data-stu-id="c434c-137">16 KB</span></span>

-   <span data-ttu-id="c434c-138">32 KB</span><span class="sxs-lookup"><span data-stu-id="c434c-138">32 KB</span></span>

-   <span data-ttu-id="c434c-139">64 KB</span><span class="sxs-lookup"><span data-stu-id="c434c-139">64 KB</span></span>

<span data-ttu-id="c434c-140">**Hinweis**  Nachdem das ursprüngliche Paket erstellt wurde, kann der Block Size-Wert nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="c434c-140">**Note** After the initial package has been created, the block size value is not changeable.</span></span>

 

## <span data-ttu-id="c434c-141">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="c434c-141">Related topics</span></span>


[<span data-ttu-id="c434c-142">So ändern Sie die Paketeigenschaften</span><span class="sxs-lookup"><span data-stu-id="c434c-142">How to Change Package Properties</span></span>](how-to-change-package-properties.md)

[<span data-ttu-id="c434c-143">Sequencer Console</span><span class="sxs-lookup"><span data-stu-id="c434c-143">Sequencer Console</span></span>](sequencer-console.md)

 

 





