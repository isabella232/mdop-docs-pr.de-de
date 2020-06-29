---
title: Sequencer-Befehlszeilenfehlercodes
description: Sequencer-Befehlszeilenfehlercodes
author: dansimp
ms.assetid: 3d491314-4923-45fd-9839-c541c5e620bd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 74f5bd0c1b66656ac6891dcc1c019254fa36fdac
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806355"
---
# <span data-ttu-id="78921-103">Sequencer-Befehlszeilenfehlercodes</span><span class="sxs-lookup"><span data-stu-id="78921-103">Sequencer Command-Line Error Codes</span></span>


<span data-ttu-id="78921-104">Verwenden Sie die folgende Liste, um Fehler zu identifizieren, die sich auf die Sequenzierung von Anwendungen beziehen, indem Sie die Befehlszeile verwenden.</span><span class="sxs-lookup"><span data-stu-id="78921-104">Use the following list to help identify errors that are related to sequencing applications by using the command line.</span></span> <span data-ttu-id="78921-105">Sie können diese Informationen auch anzeigen, indem Sie die zugehörige App-V Sequencer-Protokolldatei anzeigen.</span><span class="sxs-lookup"><span data-stu-id="78921-105">You can also see this information by viewing the associated App-V Sequencer log file.</span></span>

<span data-ttu-id="78921-106">**Hinweis**  Während der Sequenzierung können mehrere Fehler auftreten, und wenn dies der Fall ist, kann der angezeigte Fehlercode die Summe von zwei Fehlercodes sein.</span><span class="sxs-lookup"><span data-stu-id="78921-106">**Note** Multiple errors can occur during sequencing, and if this happens, the error code that is displayed might be the sum of two error codes.</span></span> <span data-ttu-id="78921-107">Wenn beispielsweise die */InstallPath* -und */OutputFile* -Parameter fehlen, gibt der App-V-Sequenzer **96**zurück – die Summe der beiden Fehlercodes.</span><span class="sxs-lookup"><span data-stu-id="78921-107">For example, if the */InstallPath* and */OutputFile* parameters are missing, the App-V Sequencer will return **96**—the sum of the two error codes.</span></span>

 

<a href="" id="01"></a><span data-ttu-id="78921-108">01</span><span class="sxs-lookup"><span data-stu-id="78921-108">01</span></span>  
<span data-ttu-id="78921-109">Es ist ein nicht spezifizierter Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="78921-109">There is an unspecified error.</span></span>

<a href="" id="02"></a><span data-ttu-id="78921-110">02</span><span class="sxs-lookup"><span data-stu-id="78921-110">02</span></span>  
<span data-ttu-id="78921-111">Das angegebene Installationsverzeichnis (/INSTALLPACKAGE) ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="78921-111">The specified installation directory (/INSTALLPACKAGE) is not valid.</span></span>

<a href="" id="04"></a><span data-ttu-id="78921-112">04</span><span class="sxs-lookup"><span data-stu-id="78921-112">04</span></span>  
<span data-ttu-id="78921-113">Das angegebene Paketstammverzeichnis (/INSTALLPATH) ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="78921-113">The specified package root directory (/INSTALLPATH) is not valid.</span></span>

<a href="" id="08"></a><span data-ttu-id="78921-114">08</span><span class="sxs-lookup"><span data-stu-id="78921-114">08</span></span>  
<span data-ttu-id="78921-115">Der angegebene */OutputFile* -Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="78921-115">The specified */OutputFile* parameter is not valid.</span></span>

<a href="" id="16"></a><span data-ttu-id="78921-116">16</span><span class="sxs-lookup"><span data-stu-id="78921-116">16</span></span>  
<span data-ttu-id="78921-117">Das Installationsverzeichnis (/INSTALLPACKAGE) ist nicht angegeben.</span><span class="sxs-lookup"><span data-stu-id="78921-117">The installation directory (/INSTALLPACKAGE) is not specified.</span></span>

<a href="" id="32"></a><span data-ttu-id="78921-118">32</span><span class="sxs-lookup"><span data-stu-id="78921-118">32</span></span>  
<span data-ttu-id="78921-119">Das Paketstammverzeichnis (/INSTALLPATH) ist nicht angegeben.</span><span class="sxs-lookup"><span data-stu-id="78921-119">The package root directory (/INSTALLPATH) is not specified.</span></span>

<a href="" id="64"></a><span data-ttu-id="78921-120">64</span><span class="sxs-lookup"><span data-stu-id="78921-120">64</span></span>  
<span data-ttu-id="78921-121">Der */OutputFile* -Parameter ist nicht angegeben.</span><span class="sxs-lookup"><span data-stu-id="78921-121">The */OutputFile* parameter is not specified.</span></span>

<a href="" id="128"></a><span data-ttu-id="78921-122">128</span><span class="sxs-lookup"><span data-stu-id="78921-122">128</span></span>  
<span data-ttu-id="78921-123">Das angegebene Application Virtualization-Laufwerk ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="78921-123">The specified application virtualization drive is not valid.</span></span>

<a href="" id="256"></a><span data-ttu-id="78921-124">256</span><span class="sxs-lookup"><span data-stu-id="78921-124">256</span></span>  
<span data-ttu-id="78921-125">Fehler beim Installationsprogramm.</span><span class="sxs-lookup"><span data-stu-id="78921-125">The installer failed.</span></span>

<a href="" id="512"></a><span data-ttu-id="78921-126">512</span><span class="sxs-lookup"><span data-stu-id="78921-126">512</span></span>  
<span data-ttu-id="78921-127">Fehler beim Sequenzieren der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="78921-127">Sequencing the application failed.</span></span>

<a href="" id="1024"></a><span data-ttu-id="78921-128">1024</span><span class="sxs-lookup"><span data-stu-id="78921-128">1024</span></span>  
<span data-ttu-id="78921-129">Fehler beim Auswerten installierter Verknüpfungen.</span><span class="sxs-lookup"><span data-stu-id="78921-129">Evaluating installed shortcuts failed.</span></span>

<a href="" id="2048"></a><span data-ttu-id="78921-130">2048</span><span class="sxs-lookup"><span data-stu-id="78921-130">2048</span></span>  
<span data-ttu-id="78921-131">Das sequenzierte Anwendungspaket kann nicht gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="78921-131">The sequenced application package cannot be saved.</span></span>

<a href="" id="4096"></a><span data-ttu-id="78921-132">4096</span><span class="sxs-lookup"><span data-stu-id="78921-132">4096</span></span>  
<span data-ttu-id="78921-133">Der angegebene Paket Name (/PACKAGENAME) ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="78921-133">The specified package name (/PACKAGENAME) is not valid.</span></span>

<a href="" id="8192"></a><span data-ttu-id="78921-134">8192</span><span class="sxs-lookup"><span data-stu-id="78921-134">8192</span></span>  
<span data-ttu-id="78921-135">Die angegebene Blockgröße (/Blocksize) ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="78921-135">The specified block size (/BLOCKSIZE) is not valid.</span></span>

<a href="" id="16384"></a><span data-ttu-id="78921-136">16384</span><span class="sxs-lookup"><span data-stu-id="78921-136">16384</span></span>  
<span data-ttu-id="78921-137">Der angegebene Komprimierungstyp (/Compression) ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="78921-137">The specified compression type (/COMPRESSION) is not valid.</span></span>

<a href="" id="32768"></a><span data-ttu-id="78921-138">32768</span><span class="sxs-lookup"><span data-stu-id="78921-138">32768</span></span>  
<span data-ttu-id="78921-139">Der angegebene Projektpfad ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="78921-139">The specified project path is not valid.</span></span>

<a href="" id="65536"></a><span data-ttu-id="78921-140">65536</span><span class="sxs-lookup"><span data-stu-id="78921-140">65536</span></span>  
<span data-ttu-id="78921-141">Der angegebene Aktualisierungsparameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="78921-141">The specified upgrade parameter is not valid.</span></span>

<a href="" id="131072"></a><span data-ttu-id="78921-142">131072</span><span class="sxs-lookup"><span data-stu-id="78921-142">131072</span></span>  
<span data-ttu-id="78921-143">Der angegebene Aktualisierungsprojekt Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="78921-143">The specified upgrade project parameter is not valid.</span></span>

<a href="" id="262144"></a><span data-ttu-id="78921-144">262144</span><span class="sxs-lookup"><span data-stu-id="78921-144">262144</span></span>  
<span data-ttu-id="78921-145">Der angegebene Decode path-Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="78921-145">The specified decode path parameter is not valid.</span></span>

<a href="" id="525288"></a><span data-ttu-id="78921-146">525288</span><span class="sxs-lookup"><span data-stu-id="78921-146">525288</span></span>  
<span data-ttu-id="78921-147">Der Paket Name ist nicht angegeben.</span><span class="sxs-lookup"><span data-stu-id="78921-147">The package name is not specified.</span></span>

## <span data-ttu-id="78921-148">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="78921-148">Related topics</span></span>


[<span data-ttu-id="78921-149">Referenz zu Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="78921-149">Application Virtualization Sequencer Reference</span></span>](application-virtualization-sequencer-reference.md)

[<span data-ttu-id="78921-150">Sequencer Befehlszeilenparameter</span><span class="sxs-lookup"><span data-stu-id="78921-150">Sequencer Command-Line Parameters</span></span>](sequencer-command-line-parameters.md)

 

 





