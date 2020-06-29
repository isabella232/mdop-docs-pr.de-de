---
title: Befehlszeilenparameter
description: Befehlszeilenparameter
author: dansimp
ms.assetid: d90a0591-f1ce-4cb8-b244-85cc70461922
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 31d6ca1215648e2519e9818817ab5cc779a746d0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807892"
---
# <span data-ttu-id="52474-103">Befehlszeilenparameter</span><span class="sxs-lookup"><span data-stu-id="52474-103">Command-Line Parameters</span></span>


<span data-ttu-id="52474-104">Verwenden Sie die folgenden Application Virtualization Sequencer-Parameter, um eine Anwendung zu sequenzieren und ein sequenziertes Anwendungspaket an der Eingabeaufforderung zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="52474-104">Use the following Application Virtualization Sequencer parameters to sequence an application and to upgrade a sequenced application package at the command prompt.</span></span> <span data-ttu-id="52474-105">Im Microsoft Application Virtualization Sequencer-Verzeichnis geben Sie **SFTSequencer**und dann den entsprechenden Parameter ein.</span><span class="sxs-lookup"><span data-stu-id="52474-105">In the Microsoft Application Virtualization Sequencer directory, you would enter **SFTSequencer**, followed by the appropriate parameter.</span></span>

<a href="" id="-help-or---"></a><span data-ttu-id="52474-106">*/Help* oder */?*</span><span class="sxs-lookup"><span data-stu-id="52474-106">*/HELP* or */?*</span></span>  
<span data-ttu-id="52474-107">Verwenden Sie diese Funktion, um die Liste der für die Befehlszeilen Sequenz verfügbaren Parameter anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="52474-107">Use to display the list of parameters available for command-line sequencing.</span></span>

<a href="" id="-installpackage-or--i"></a><span data-ttu-id="52474-108">*/INSTALLPACKAGE* oder */i*</span><span class="sxs-lookup"><span data-stu-id="52474-108">*/INSTALLPACKAGE* or */I*</span></span>  
<span data-ttu-id="52474-109">Hiermit können Sie das Installationsprogramm oder eine Batchdatei angeben, in der die Anwendung sequenziert werden soll.</span><span class="sxs-lookup"><span data-stu-id="52474-109">Use to specify the installer or a batch file for the application to be sequenced.</span></span>

<a href="" id="-installpath-or--p"></a><span data-ttu-id="52474-110">*/InstallPath* oder */p*</span><span class="sxs-lookup"><span data-stu-id="52474-110">*/INSTALLPATH* or */P*</span></span>  
<span data-ttu-id="52474-111">Hiermit geben Sie das Paketstammverzeichnis an.</span><span class="sxs-lookup"><span data-stu-id="52474-111">Use to specify the package root directory.</span></span>

<a href="" id="-outputfile-or--o"></a><span data-ttu-id="52474-112">*/OutputFile* oder */o*</span><span class="sxs-lookup"><span data-stu-id="52474-112">*/OUTPUTFILE* or */O*</span></span>  
<span data-ttu-id="52474-113">Hiermit geben Sie den Pfad und den Dateinamen der SPRJ-Datei an, die generiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="52474-113">Use to specify the path and file name of the SPRJ file that will be generated.</span></span>

<span data-ttu-id="52474-114">**Wichtig**  Der */OutputFile* -Parameter steht beim Öffnen eines Pakets, das Sie nicht aktualisieren möchten, nicht zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="52474-114">**Important** The */OUTPUTFILE* parameter is not available when opening a package that you do not intend to upgrade.</span></span>

 

<a href="" id="-fullload-or--f"></a><span data-ttu-id="52474-115">*/FULLLOAD* oder */f*</span><span class="sxs-lookup"><span data-stu-id="52474-115">*/FULLLOAD* or */F*</span></span>  
<span data-ttu-id="52474-116">Verwenden Sie diese Option, um anzugeben, ob alles im primären Feature-Block platziert werden soll.</span><span class="sxs-lookup"><span data-stu-id="52474-116">Use to specify whether to put everything in the primary feature block.</span></span>

<a href="" id="-packagename-or--k"></a><span data-ttu-id="52474-117">*/PackageName* oder *k*</span><span class="sxs-lookup"><span data-stu-id="52474-117">*/PACKAGENAME* or */K*</span></span>  
<span data-ttu-id="52474-118">Hiermit geben Sie den Paketnamen der sequenzierten Anwendung an.</span><span class="sxs-lookup"><span data-stu-id="52474-118">Use to specify the package name of the sequenced application.</span></span>

<a href="" id="-blocksize"></a>*<span data-ttu-id="52474-119">/BLOCKSIZE</span><span class="sxs-lookup"><span data-stu-id="52474-119">/BLOCKSIZE</span></span>*  
<span data-ttu-id="52474-120">Gibt die SFT-Datei Blockgröße an, die zum Streamen des Pakets an Clientcomputer verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="52474-120">Specifies the SFT file block size that will be used to stream the package to client computers.</span></span> <span data-ttu-id="52474-121">Sie können einen der folgenden Werte auswählen:</span><span class="sxs-lookup"><span data-stu-id="52474-121">You can select one of the following values:</span></span>

-   <span data-ttu-id="52474-122">4 KB</span><span class="sxs-lookup"><span data-stu-id="52474-122">4 KB</span></span>

-   <span data-ttu-id="52474-123">16 KB</span><span class="sxs-lookup"><span data-stu-id="52474-123">16 KB</span></span>

-   <span data-ttu-id="52474-124">32 KB</span><span class="sxs-lookup"><span data-stu-id="52474-124">32 KB</span></span>

-   <span data-ttu-id="52474-125">64 KB</span><span class="sxs-lookup"><span data-stu-id="52474-125">64 KB</span></span>

<span data-ttu-id="52474-126">Sie sollten die Größe der SFT-Datei berücksichtigen, wenn Sie die Blockgröße angeben.</span><span class="sxs-lookup"><span data-stu-id="52474-126">You should consider the size of the SFT file when you specify the block size.</span></span> <span data-ttu-id="52474-127">Eine Datei mit einer kleineren Blockgröße dauert länger, um über das Netzwerk zu streamen, ist jedoch weniger bandbreitenintensiv.</span><span class="sxs-lookup"><span data-stu-id="52474-127">A file with a smaller block size takes longer to stream over the network but is less bandwidth-intensive.</span></span> <span data-ttu-id="52474-128">Dateien mit größeren Blockgrößen verwenden mehr Netzwerkbandbreite.</span><span class="sxs-lookup"><span data-stu-id="52474-128">Files with larger block sizes use more network bandwidth.</span></span>

<a href="" id="-compression"></a>*<span data-ttu-id="52474-129">/COMPRESSION</span><span class="sxs-lookup"><span data-stu-id="52474-129">/COMPRESSION</span></span>*  
<span data-ttu-id="52474-130">Verwenden Sie diese Methode, um die Methode zum Komprimieren der SFT-Datei beim Streamen an den Client anzugeben.</span><span class="sxs-lookup"><span data-stu-id="52474-130">Use to specify the method for compressing the SFT file as it is streamed to the client.</span></span>

<a href="" id="-msi-or--m"></a><span data-ttu-id="52474-131">*/MSI* oder */m*</span><span class="sxs-lookup"><span data-stu-id="52474-131">*/MSI* or */M*</span></span>  
<span data-ttu-id="52474-132">Hiermit geben Sie an, wie ein Microsoft Windows Installer-Paket für die sequenzierte Anwendung generiert wird.</span><span class="sxs-lookup"><span data-stu-id="52474-132">Use to specify generating a Microsoft Windows Installer package for the sequenced application.</span></span>

<a href="" id="-default"></a>*<span data-ttu-id="52474-133">/DEFAULT</span><span class="sxs-lookup"><span data-stu-id="52474-133">/DEFAULT</span></span>*  
<span data-ttu-id="52474-134">Gibt die standardmäßige SPRJ-Datei an, die beim Erstellen eines virtuellen Anwendungspakets verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="52474-134">Specifies the default SPRJ file that will be used when creating a virtual application package.</span></span> <span data-ttu-id="52474-135">Diese Datei wird als SPRJ-Vorlage verwendet, wenn die Anwendung zum ersten Mal sequenziert wird.</span><span class="sxs-lookup"><span data-stu-id="52474-135">This file is used as the .sprj template when the application is sequenced for the first time.</span></span>

<a href="" id="-upgrade"></a>*<span data-ttu-id="52474-136">/Upgrade</span><span class="sxs-lookup"><span data-stu-id="52474-136">/UPGRADE</span></span>*  
<span data-ttu-id="52474-137">Gibt den Pfad und den Dateinamen der SPRJ-Datei an, die aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="52474-137">Specifies the path and file name of the SPRJ file that will be upgraded.</span></span>

<a href="" id="-decodepath"></a>*<span data-ttu-id="52474-138">/DECODEPATH</span><span class="sxs-lookup"><span data-stu-id="52474-138">/DECODEPATH</span></span>*  
<span data-ttu-id="52474-139">Gibt das Verzeichnis auf dem Sequenzcomputer an, auf dem die Dateien installiert sind, die dem sequenzierten Anwendungspaket zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="52474-139">Specifies the directory on the sequencing computer where the files associated with the sequenced application package are installed.</span></span> <span data-ttu-id="52474-140">Verwenden Sie bei der Angabe des Verzeichnisses eines der folgenden Formate:</span><span class="sxs-lookup"><span data-stu-id="52474-140">Use one of the following formats when specifying the directory:</span></span>

-   <span data-ttu-id="52474-141">/DECODEPATH: f:</span><span class="sxs-lookup"><span data-stu-id="52474-141">/decodepath:Q:</span></span>

-   <span data-ttu-id="52474-142">/DECODEPATH: q:</span><span class="sxs-lookup"><span data-stu-id="52474-142">/decodepath:Q:.</span></span>

-   <span data-ttu-id="52474-143">/DECODEPATH: "q:"</span><span class="sxs-lookup"><span data-stu-id="52474-143">/decodepath:”Q:.”</span></span>

-   <span data-ttu-id="52474-144">/DECODEPATH: "f:"</span><span class="sxs-lookup"><span data-stu-id="52474-144">/decodepath:”Q:”</span></span>

## <span data-ttu-id="52474-145">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="52474-145">Related topics</span></span>


[<span data-ttu-id="52474-146">Informationen zum Verwenden der Sequencer-Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="52474-146">About Using the Sequencer Command Line</span></span>](about-using-the-sequencer-command-line.md)

[<span data-ttu-id="52474-147">So öffnen Sie eine sequenzierte Anwendung über die Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="52474-147">How to Open a Sequenced Application Using the Command Line</span></span>](how-to-open-a-sequenced-application-using-the-command-line.md)

[<span data-ttu-id="52474-148">So aktualisieren Sie ein Paket mit dem Befehl „Paket öffnen“</span><span class="sxs-lookup"><span data-stu-id="52474-148">How to Upgrade a Package Using the Open Package Command</span></span>](how-to-upgrade-a-package-using-the-open-package-command.md)

 

 





