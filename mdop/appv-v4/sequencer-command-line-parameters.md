---
title: Sequencer Befehlszeilenparameter
description: Sequencer Befehlszeilenparameter
author: dansimp
ms.assetid: 28fb875a-c302-4d95-b2e0-8dc0c5dbb0f8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ecfa269de04cf3dcba30cbb4a40f9176f03f6571
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806352"
---
# <span data-ttu-id="fa0e9-103">Sequencer Befehlszeilenparameter</span><span class="sxs-lookup"><span data-stu-id="fa0e9-103">Sequencer Command-Line Parameters</span></span>


<span data-ttu-id="fa0e9-104">Sie können die folgenden Application Virtualization (App-V)-Sequenzer-Parameter verwenden, um eine Anwendung zu sequenzieren und eine vorhandene virtuelle Anwendung mithilfe einer Befehlszeile zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="fa0e9-104">You can use the following Application Virtualization (App-V) Sequencer parameters to sequence an application and to upgrade an existing virtual application by using a command line.</span></span> <span data-ttu-id="fa0e9-105">Weitere Informationen zum Sequenzieren einer Anwendung mithilfe einer Befehlszeile finden Sie unter so wird es [gemacht: Sequenzierung einer neuen Anwendung mithilfe der Befehlszeile](how-to-sequence-a-new-application-by-using-the-command-line.md).</span><span class="sxs-lookup"><span data-stu-id="fa0e9-105">For more information about sequencing an application by using a command line, see [How to Sequence a New Application by Using the Command Line](how-to-sequence-a-new-application-by-using-the-command-line.md).</span></span>

## <span data-ttu-id="fa0e9-106">Sequencer Befehlszeilenparameter</span><span class="sxs-lookup"><span data-stu-id="fa0e9-106">Sequencer Command-Line Parameters</span></span>


<a href="" id="-help-or---"></a>**<span data-ttu-id="fa0e9-107">/Help oder/?</span><span class="sxs-lookup"><span data-stu-id="fa0e9-107">/HELP or /?</span></span>**  
<span data-ttu-id="fa0e9-108">Zeigt Informationen zu Parametern an, die für die Verwendung einer Befehlszeile zur Sequenzierung von Anwendungen verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="fa0e9-108">Displays information about parameters that are available for using a command line to sequence applications.</span></span>

<a href="" id="-installpackage-or--i"></a>**<span data-ttu-id="fa0e9-109">/INSTALLPACKAGE oder/i</span><span class="sxs-lookup"><span data-stu-id="fa0e9-109">/INSTALLPACKAGE or /I</span></span>**  
<span data-ttu-id="fa0e9-110">Gibt den Windows Installer oder eine Batchdatei an, die zum Installieren einer Anwendung verwendet wird, damit Sie sequenziert werden kann.</span><span class="sxs-lookup"><span data-stu-id="fa0e9-110">Specifies the Windows Installer or a batch file that will be used to install an application so that it can be sequenced.</span></span>

<a href="" id="-installpath-or--p"></a>**<span data-ttu-id="fa0e9-111">/InstallPath oder/p</span><span class="sxs-lookup"><span data-stu-id="fa0e9-111">/INSTALLPATH or /P</span></span>**  
<span data-ttu-id="fa0e9-112">Gibt das Paketstammverzeichnis für eine Anwendung an.</span><span class="sxs-lookup"><span data-stu-id="fa0e9-112">Specifies the package root directory for an application.</span></span>

<a href="" id="-outputfile-or--o"></a>**<span data-ttu-id="fa0e9-113">/OutputFile oder/o</span><span class="sxs-lookup"><span data-stu-id="fa0e9-113">/OUTPUTFILE or /O</span></span>**  
<span data-ttu-id="fa0e9-114">Gibt den Pfad und den Dateinamen der SPRJ-Datei an, die generiert wird.</span><span class="sxs-lookup"><span data-stu-id="fa0e9-114">Specifies the path and file name of the SPRJ file that will be generated.</span></span>

<a href="" id="-fullload-or--f"></a>**<span data-ttu-id="fa0e9-115">/FULLLOAD oder/f</span><span class="sxs-lookup"><span data-stu-id="fa0e9-115">/FULLLOAD or /F</span></span>**  
<span data-ttu-id="fa0e9-116">Gibt an, ob alle Dateien im primären Feature-Block enthalten sein sollen.</span><span class="sxs-lookup"><span data-stu-id="fa0e9-116">Specifies whether all files will be contained in the primary feature block.</span></span> <span data-ttu-id="fa0e9-117">Wenn der Parameter **/FULLLOAD** in der Befehlszeile angegeben wird, werden alle zugeordneten Anwendungsdaten dem primären Feature-Block hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="fa0e9-117">If the **/FULLLOAD** parameter is specified on the command line, all of the associated application data is added to primary feature block.</span></span> <span data-ttu-id="fa0e9-118">Wenn der **/FULLLOAD** -Parameter nicht in der Befehlszeile angegeben ist, wird dem primären Feature-Block keine der zugeordneten Anwendungsdaten hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="fa0e9-118">If the **/FULLLOAD** parameter is not specified on the command line, then none of the associated application data is added to the primary feature block.</span></span>

<a href="" id="-packagename-or--k"></a>**<span data-ttu-id="fa0e9-119">/PackageName oder k</span><span class="sxs-lookup"><span data-stu-id="fa0e9-119">/PACKAGENAME or /K</span></span>**  
<span data-ttu-id="fa0e9-120">Gibt den Paketnamen an, der der sequenzierten Anwendung zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="fa0e9-120">Specifies the package name that will be assigned to the sequenced application.</span></span>

<a href="" id="-blocksize"></a>**<span data-ttu-id="fa0e9-121">/BLOCKSIZE</span><span class="sxs-lookup"><span data-stu-id="fa0e9-121">/BLOCKSIZE</span></span>**  
<span data-ttu-id="fa0e9-122">Gibt die SFT-Datei Blockgröße an, die zum Streamen des Pakets an Clientcomputer verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="fa0e9-122">Specifies the SFT file block size that will be used to stream the package to client computers.</span></span> <span data-ttu-id="fa0e9-123">Sie können einen der folgenden Werte auswählen:</span><span class="sxs-lookup"><span data-stu-id="fa0e9-123">You can select one of the following values:</span></span>

-   <span data-ttu-id="fa0e9-124">4 KB</span><span class="sxs-lookup"><span data-stu-id="fa0e9-124">4 KB</span></span>

-   <span data-ttu-id="fa0e9-125">16 KB</span><span class="sxs-lookup"><span data-stu-id="fa0e9-125">16 KB</span></span>

-   <span data-ttu-id="fa0e9-126">32 KB</span><span class="sxs-lookup"><span data-stu-id="fa0e9-126">32 KB</span></span>

-   <span data-ttu-id="fa0e9-127">64 KB</span><span class="sxs-lookup"><span data-stu-id="fa0e9-127">64 KB</span></span>

<span data-ttu-id="fa0e9-128">Sie sollten die Größe der SFT-Datei berücksichtigen, wenn Sie die Blockgröße angeben.</span><span class="sxs-lookup"><span data-stu-id="fa0e9-128">You should consider the size of the SFT file when you specify the block size.</span></span> <span data-ttu-id="fa0e9-129">Eine Datei mit einer kleineren Blockgröße dauert länger, um über das Netzwerk zu streamen, ist jedoch weniger bandbreitenintensiv.</span><span class="sxs-lookup"><span data-stu-id="fa0e9-129">A file with a smaller block size takes longer to stream over the network but is less bandwidth-intensive.</span></span> <span data-ttu-id="fa0e9-130">Dateien mit größeren Blockgrößen verwenden mehr Netzwerkbandbreite.</span><span class="sxs-lookup"><span data-stu-id="fa0e9-130">Files with larger block sizes use more network bandwidth.</span></span>

<a href="" id="-compression"></a>**<span data-ttu-id="fa0e9-131">/COMPRESSION</span><span class="sxs-lookup"><span data-stu-id="fa0e9-131">/COMPRESSION</span></span>**  
<span data-ttu-id="fa0e9-132">Gibt die Methode zum Komprimieren der SFT-Datei an, die an den Client gestreamt wird.</span><span class="sxs-lookup"><span data-stu-id="fa0e9-132">Specifies the method for compressing the SFT file that will be streamed to the client.</span></span>

<a href="" id="-msi-or--m"></a>**<span data-ttu-id="fa0e9-133">/MSI oder/m</span><span class="sxs-lookup"><span data-stu-id="fa0e9-133">/MSI or /M</span></span>**  
<span data-ttu-id="fa0e9-134">Gibt an, ob ein Windows Installer für die sequenzierte Anwendung erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="fa0e9-134">Specifies whether a Windows Installer for the sequenced application should be created.</span></span>

<a href="" id="-default"></a>**<span data-ttu-id="fa0e9-135">/DEFAULT</span><span class="sxs-lookup"><span data-stu-id="fa0e9-135">/DEFAULT</span></span>**  
<span data-ttu-id="fa0e9-136">Gibt die standardmäßige SPRJ-Datei an, die beim Erstellen eines virtuellen Anwendungspakets verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="fa0e9-136">Specifies the default SPRJ file that will be used when creating a virtual application package.</span></span> <span data-ttu-id="fa0e9-137">Diese Datei wird als SPRJ-Vorlage verwendet, wenn die Anwendung zum ersten Mal sequenziert wird.</span><span class="sxs-lookup"><span data-stu-id="fa0e9-137">This file is used as the .sprj template when the application is sequenced for the first time.</span></span>

<a href="" id="-upgrade"></a>**<span data-ttu-id="fa0e9-138">/Upgrade</span><span class="sxs-lookup"><span data-stu-id="fa0e9-138">/UPGRADE</span></span>**  
<span data-ttu-id="fa0e9-139">Gibt den Pfad und den Dateinamen der SPRJ-Datei an, die aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="fa0e9-139">Specifies the path and file name of the SPRJ file that will be upgraded.</span></span>

<a href="" id="-decodepath"></a>**<span data-ttu-id="fa0e9-140">/DECODEPATH</span><span class="sxs-lookup"><span data-stu-id="fa0e9-140">/DECODEPATH</span></span>**  
<span data-ttu-id="fa0e9-141">Gibt das Verzeichnis auf dem Sequenzcomputer an, auf dem die Dateien installiert sind, die dem sequenzierten Anwendungspaket zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="fa0e9-141">Specifies the directory on the sequencing computer where the files associated with the sequenced application package are installed.</span></span> <span data-ttu-id="fa0e9-142">Verwenden Sie bei der Angabe des Verzeichnisses eines der folgenden Formate:</span><span class="sxs-lookup"><span data-stu-id="fa0e9-142">Use one of the following formats when specifying the directory:</span></span>

-   <span data-ttu-id="fa0e9-143">/DECODEPATH: f:</span><span class="sxs-lookup"><span data-stu-id="fa0e9-143">/decodepath:Q:</span></span>

-   <span data-ttu-id="fa0e9-144">/DECODEPATH: q:</span><span class="sxs-lookup"><span data-stu-id="fa0e9-144">/decodepath:Q:.</span></span>

-   <span data-ttu-id="fa0e9-145">/DECODEPATH: "q:"</span><span class="sxs-lookup"><span data-stu-id="fa0e9-145">/decodepath:”Q:.”</span></span>

-   <span data-ttu-id="fa0e9-146">/DECODEPATH: "f:"</span><span class="sxs-lookup"><span data-stu-id="fa0e9-146">/decodepath:”Q:”</span></span>

## <span data-ttu-id="fa0e9-147">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="fa0e9-147">Related topics</span></span>


[<span data-ttu-id="fa0e9-148">Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="fa0e9-148">Application Virtualization Sequencer</span></span>](application-virtualization-sequencer.md)

[<span data-ttu-id="fa0e9-149">Sequencer-Befehlszeilenfehlercodes</span><span class="sxs-lookup"><span data-stu-id="fa0e9-149">Sequencer Command-Line Error Codes</span></span>](sequencer-command-line-error-codes.md)

 

 





