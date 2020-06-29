---
title: Befehlszeilenfehler
description: Befehlszeilenfehler
author: dansimp
ms.assetid: eea62568-4e90-4877-9cc7-e27ef5c05068
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ab29a77dc15a8c7bd3590b918a7ca8c1ca6e8c0d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807895"
---
# <span data-ttu-id="65ed0-103">Befehlszeilenfehler</span><span class="sxs-lookup"><span data-stu-id="65ed0-103">Command-Line Errors</span></span>


<span data-ttu-id="65ed0-104">Ermitteln Sie anhand der folgenden Fehlerliste die Gründe, warum die Befehlszeilen-Sequenzierung nicht ordnungsgemäß funktioniert.</span><span class="sxs-lookup"><span data-stu-id="65ed0-104">Use the following list of errors to identify the reasons why command-line sequencing is not working properly.</span></span> <span data-ttu-id="65ed0-105">Sie können diese Fehler auch sehen, indem Sie die Sequencer-Protokolldatei anzeigen.</span><span class="sxs-lookup"><span data-stu-id="65ed0-105">You can also see these errors by viewing the sequencer log file.</span></span>

<span data-ttu-id="65ed0-106">**Hinweis**  Bei der Sequenzierung wird möglicherweise mehr als ein Fehler angezeigt.</span><span class="sxs-lookup"><span data-stu-id="65ed0-106">**Note** More than one error might be displayed when sequencing.</span></span> <span data-ttu-id="65ed0-107">Darüber hinaus kann der angezeigte Fehlercode die Summe von zwei Fehlercodes sein.</span><span class="sxs-lookup"><span data-stu-id="65ed0-107">Furthermore, the error code displayed might be the sum of two error codes.</span></span> <span data-ttu-id="65ed0-108">Wenn beispielsweise die */InstallPath* -und */OutputFile* -Parameter fehlen, gibt Microsoft System Center Application Virtualization Sequencer 96 zurück – die Summe der beiden Fehlercodes.</span><span class="sxs-lookup"><span data-stu-id="65ed0-108">For example, if the */InstallPath* and */OutputFile* parameters are missing, the Microsoft System Center Application Virtualization Sequencer will return 96—the sum of the two error codes.</span></span>

 

<a href="" id="01"></a><span data-ttu-id="65ed0-109">01</span><span class="sxs-lookup"><span data-stu-id="65ed0-109">01</span></span>  
<span data-ttu-id="65ed0-110">Es ist ein nicht spezifizierter Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="65ed0-110">There is an unspecified error.</span></span>

<a href="" id="02"></a><span data-ttu-id="65ed0-111">02</span><span class="sxs-lookup"><span data-stu-id="65ed0-111">02</span></span>  
<span data-ttu-id="65ed0-112">Das angegebene Installationsverzeichnis (/INSTALLPACKAGE) ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="65ed0-112">The specified installation directory (/INSTALLPACKAGE) specified is not valid.</span></span>

<a href="" id="04"></a><span data-ttu-id="65ed0-113">04</span><span class="sxs-lookup"><span data-stu-id="65ed0-113">04</span></span>  
<span data-ttu-id="65ed0-114">Das angegebene Paketstammverzeichnis (/INSTALLPATH) ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="65ed0-114">The specified package root directory (/INSTALLPATH) is not valid.</span></span>

<a href="" id="08"></a><span data-ttu-id="65ed0-115">08</span><span class="sxs-lookup"><span data-stu-id="65ed0-115">08</span></span>  
<span data-ttu-id="65ed0-116">Der angegebene */OutputFile* -Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="65ed0-116">The */OutputFile* parameter that was specified is not valid.</span></span>

<a href="" id="16"></a><span data-ttu-id="65ed0-117">16</span><span class="sxs-lookup"><span data-stu-id="65ed0-117">16</span></span>  
<span data-ttu-id="65ed0-118">Das Installationsverzeichnis (/INSTALLPACKAGE) wurde nicht angegeben.</span><span class="sxs-lookup"><span data-stu-id="65ed0-118">The installation directory (/INSTALLPACKAGE) was not specified.</span></span>

<a href="" id="32"></a><span data-ttu-id="65ed0-119">32</span><span class="sxs-lookup"><span data-stu-id="65ed0-119">32</span></span>  
<span data-ttu-id="65ed0-120">Das Paketstammverzeichnis (/INSTALLPATH) wurde nicht angegeben.</span><span class="sxs-lookup"><span data-stu-id="65ed0-120">The package root directory (/INSTALLPATH) was not specified.</span></span>

<a href="" id="64"></a><span data-ttu-id="65ed0-121">64</span><span class="sxs-lookup"><span data-stu-id="65ed0-121">64</span></span>  
<span data-ttu-id="65ed0-122">Der */OutputFile* -Parameter wurde nicht angegeben.</span><span class="sxs-lookup"><span data-stu-id="65ed0-122">The */OutputFile* parameter was not specified.</span></span>

<a href="" id="128"></a><span data-ttu-id="65ed0-123">128</span><span class="sxs-lookup"><span data-stu-id="65ed0-123">128</span></span>  
<span data-ttu-id="65ed0-124">Das angegebene Application Virtualization-Laufwerk ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="65ed0-124">The specified application virtualization drive is not valid.</span></span>

<a href="" id="256"></a><span data-ttu-id="65ed0-125">256</span><span class="sxs-lookup"><span data-stu-id="65ed0-125">256</span></span>  
<span data-ttu-id="65ed0-126">Fehler beim Installationsprogramm.</span><span class="sxs-lookup"><span data-stu-id="65ed0-126">The installer failed.</span></span>

<a href="" id="512"></a><span data-ttu-id="65ed0-127">512</span><span class="sxs-lookup"><span data-stu-id="65ed0-127">512</span></span>  
<span data-ttu-id="65ed0-128">Fehler beim Sequenzieren der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="65ed0-128">Sequencing the application failed.</span></span>

<a href="" id="1024"></a><span data-ttu-id="65ed0-129">1024</span><span class="sxs-lookup"><span data-stu-id="65ed0-129">1024</span></span>  
<span data-ttu-id="65ed0-130">Fehler beim Auswerten installierter Verknüpfungen.</span><span class="sxs-lookup"><span data-stu-id="65ed0-130">Evaluating installed shortcuts failed.</span></span>

<a href="" id="2048"></a><span data-ttu-id="65ed0-131">2048</span><span class="sxs-lookup"><span data-stu-id="65ed0-131">2048</span></span>  
<span data-ttu-id="65ed0-132">Das sequenzierte Anwendungspaket kann nicht gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="65ed0-132">The sequenced application package cannot be saved.</span></span>

<a href="" id="4096"></a><span data-ttu-id="65ed0-133">4096</span><span class="sxs-lookup"><span data-stu-id="65ed0-133">4096</span></span>  
<span data-ttu-id="65ed0-134">Der angegebene Paket Name (/PACKAGENAME) ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="65ed0-134">The specified package name (/PACKAGENAME) is not valid.</span></span>

<a href="" id="8192"></a><span data-ttu-id="65ed0-135">8192</span><span class="sxs-lookup"><span data-stu-id="65ed0-135">8192</span></span>  
<span data-ttu-id="65ed0-136">Die angegebene Blockgröße (/Blocksize <em> ) </em> ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="65ed0-136">The specified block size (/BLOCKSIZE<em>)</em> is not valid.</span></span>

<a href="" id="16384"></a><span data-ttu-id="65ed0-137">16384</span><span class="sxs-lookup"><span data-stu-id="65ed0-137">16384</span></span>  
<span data-ttu-id="65ed0-138">Der angegebene Komprimierungstyp (/Compression) ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="65ed0-138">The specified compression type (/COMPRESSION) is not valid.</span></span>

<a href="" id="32768"></a><span data-ttu-id="65ed0-139">32768</span><span class="sxs-lookup"><span data-stu-id="65ed0-139">32768</span></span>  
<span data-ttu-id="65ed0-140">Der angegebene Projektpfad ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="65ed0-140">The specified project path is not valid.</span></span>

<a href="" id="65536"></a><span data-ttu-id="65ed0-141">65536</span><span class="sxs-lookup"><span data-stu-id="65ed0-141">65536</span></span>  
<span data-ttu-id="65ed0-142">Der angegebene Aktualisierungsparameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="65ed0-142">The specified upgrade parameter is not valid.</span></span>

<a href="" id="131072"></a><span data-ttu-id="65ed0-143">131072</span><span class="sxs-lookup"><span data-stu-id="65ed0-143">131072</span></span>  
<span data-ttu-id="65ed0-144">Der angegebene Aktualisierungsprojekt Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="65ed0-144">The specified upgrade project parameter is not valid.</span></span>

<a href="" id="262144"></a><span data-ttu-id="65ed0-145">262144</span><span class="sxs-lookup"><span data-stu-id="65ed0-145">262144</span></span>  
<span data-ttu-id="65ed0-146">Der angegebene Decode path-Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="65ed0-146">The specified decode path parameter is not valid.</span></span>

<a href="" id="525288"></a><span data-ttu-id="65ed0-147">525288</span><span class="sxs-lookup"><span data-stu-id="65ed0-147">525288</span></span>  
<span data-ttu-id="65ed0-148">Der Paketname wurde nicht angegeben.</span><span class="sxs-lookup"><span data-stu-id="65ed0-148">The package name was not specified.</span></span>

## <span data-ttu-id="65ed0-149">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="65ed0-149">Related topics</span></span>


[<span data-ttu-id="65ed0-150">Informationen zum Verwenden der Sequencer-Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="65ed0-150">About Using the Sequencer Command Line</span></span>](about-using-the-sequencer-command-line.md)

[<span data-ttu-id="65ed0-151">Befehlszeilenparameter</span><span class="sxs-lookup"><span data-stu-id="65ed0-151">Command-Line Parameters</span></span>](command-line-parameters.md)

 

 





