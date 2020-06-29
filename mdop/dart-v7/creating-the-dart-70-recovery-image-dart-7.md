---
title: Erstellen des DaRT 7.0-Wiederherstellungsabbilds
description: Erstellen des DaRT 7.0-Wiederherstellungsabbilds
author: dansimp
ms.assetid: ebb2ec58-0349-469d-a23f-3f944fe4c1fa
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f19ff144cac61ca7ea5a8498f67caf8a99229d77
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809862"
---
# <span data-ttu-id="6e930-103">Erstellen des DaRT 7.0-Wiederherstellungsabbilds</span><span class="sxs-lookup"><span data-stu-id="6e930-103">Creating the DaRT 7.0 Recovery Image</span></span>


<span data-ttu-id="6e930-104">Microsoft Diagnostics and Recovery Toolset (Dart) 7 umfasst den **Dart-Wiederherstellungs-Bild-Assistenten** , der in Windows zum Erstellen einer startbaren internationalen Organisation für Standardisierungs-Images (ISO) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6e930-104">Microsoft Diagnostics and Recovery Toolset (DaRT)7 includes the **DaRT Recovery Image Wizard** that is used in Windows to create a bootable International Organization for Standardization (ISO) image.</span></span> <span data-ttu-id="6e930-105">Bei einem ISO-Bild handelt es sich um eine Datei, die den unformatierten Inhalt einer CD darstellt.</span><span class="sxs-lookup"><span data-stu-id="6e930-105">An ISO image is a file that represents the raw contents of a CD.</span></span>

## <span data-ttu-id="6e930-106">Verwenden des DART-Wiederherstellungsbild-Assistenten zum Erstellen des Wiederherstellungs Bilds</span><span class="sxs-lookup"><span data-stu-id="6e930-106">Use the DaRT Recovery Image Wizard to Create the Recovery Image</span></span>


<span data-ttu-id="6e930-107">Die vom Dart-Wiederherstellungsbild-Assistenten erstellte ISO-Datei enthält das DART-Wiederherstellungsbild, mit dem Sie auf einen Problem Computer booten können, auch wenn es sonst nicht gestartet werden kann.</span><span class="sxs-lookup"><span data-stu-id="6e930-107">The ISO created by the DaRT Recovery Image Wizard contains the DaRT recovery image that lets you boot into a problem computer, even if it might otherwise not start.</span></span> <span data-ttu-id="6e930-108">Nachdem Sie den Computer in DART gestartet haben, können Sie die verschiedenen Dart-Tools ausführen, um zu versuchen, den Computer zu diagnostizieren und zu reparieren.</span><span class="sxs-lookup"><span data-stu-id="6e930-108">After you boot the computer into DaRT, you can run the different DaRT tools to try to diagnose and repair the computer.</span></span>

<span data-ttu-id="6e930-109">Sie können die ISO auf eine beschreibbare CD oder DVD schreiben, Sie auf einem USB-Stick speichern oder in einem Format speichern, das Sie zum Booten von DART von einer Remotepartition oder einer Wiederherstellungspartition verwenden können.</span><span class="sxs-lookup"><span data-stu-id="6e930-109">You can write the ISO to a recordable CD or DVD, save it to a USB flash drive, or save it in a format that you can use to boot into DaRT from a remote partition or from a recovery partition.</span></span> <span data-ttu-id="6e930-110">Weitere Informationen finden Sie unter [Bereitstellen des DART 7,0-Wiederherstellungsabbilds](deploying-the-dart-70-recovery-image-dart-7.md).</span><span class="sxs-lookup"><span data-stu-id="6e930-110">For more information, see [Deploying the DaRT 7.0 Recovery Image](deploying-the-dart-70-recovery-image-dart-7.md).</span></span>

<span data-ttu-id="6e930-111">**Hinweis**  Wenn Ihr Computer ein CD-RW-Laufwerk enthält, bietet der Assistent an, das ISO-Abbild auf eine leere CD oder DVD zu brennen.</span><span class="sxs-lookup"><span data-stu-id="6e930-111">**Note** If your computer includes a CD-RW drive, the wizard offers to burn the ISO image to a blank CD or DVD.</span></span> <span data-ttu-id="6e930-112">Wenn auf Ihrem Computer kein vom Assistenten unterstütztes Laufwerk enthalten ist, können Sie das ISO-Abbild auf eine CD oder DVD brennen, indem Sie die meisten Programme verwenden, die eine CD oder DVD brennen können.</span><span class="sxs-lookup"><span data-stu-id="6e930-112">If your computer does not include a drive that is supported by the wizard, you can burn the ISO image onto a CD or DVD by using most programs that can burn a CD or DVD.</span></span>

 

<span data-ttu-id="6e930-113">Zum Erstellen einer startbaren CD oder DVD aus dem ISO-Abbild benötigen Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="6e930-113">To create a bootable CD or DVD from the ISO image, you must have:</span></span>

-   <span data-ttu-id="6e930-114">Ein CD-RW-Laufwerk.</span><span class="sxs-lookup"><span data-stu-id="6e930-114">A CD-RW drive.</span></span>

-   <span data-ttu-id="6e930-115">Eine beschreibbare CD oder DVD (in einem vom beschreibbaren Laufwerk unterstützten Format).</span><span class="sxs-lookup"><span data-stu-id="6e930-115">A recordable CD or DVD (in a format supported by the recordable drive).</span></span>

-   <span data-ttu-id="6e930-116">Software, die das beschreibbare Laufwerk unterstützt und das Brennen eines ISO-Images direkt auf CD oder DVD unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6e930-116">Software that supports the recordable drive and supports burning an ISO image directly to CD or DVD.</span></span>

    <span data-ttu-id="6e930-117">**Wichtig**  Testen Sie die CD oder DVD, die Sie erstellen, auf allen verschiedenen Arten von Computern, die Sie unterstützen möchten, weil einige Computer nicht von allen Arten von beschreibbaren Medien gestartet werden können.</span><span class="sxs-lookup"><span data-stu-id="6e930-117">**Important** Test the CD or DVD that you create on all the different kinds of computers that you intend to support because some computers cannot start from all kinds of recordable media.</span></span>

     

<span data-ttu-id="6e930-118">Um das ISO-Abbild auf einem USB-Flashlaufwerk (USB-Stick) zu speichern, müssen Sie Folgendes haben:</span><span class="sxs-lookup"><span data-stu-id="6e930-118">To save the ISO image to a USB flash drive (UFD), you must have:</span></span>

-   <span data-ttu-id="6e930-119">Ein korrekt formatiertes USB-Laufwerk.</span><span class="sxs-lookup"><span data-stu-id="6e930-119">A correctly formatted UFD.</span></span>

-   <span data-ttu-id="6e930-120">Ein Programm, das Sie zum Bereitstellen des ISO-Images verwenden können.</span><span class="sxs-lookup"><span data-stu-id="6e930-120">A program that you can use to mount the ISO image.</span></span>

[<span data-ttu-id="6e930-121">So verwenden Sie den Assistent für DaRT-Wiederherstellungsabbilder zum Erstellen des Wiederherstellungsabbilds</span><span class="sxs-lookup"><span data-stu-id="6e930-121">How to Use the DaRT Recovery Image Wizard to Create the Recovery Image</span></span>](how-to-use-the-dart-recovery-image-wizard-to-create-the-recovery-image-dart-7.md)

## <span data-ttu-id="6e930-122">Erstellen eines zeitlimitierten Wiederherstellungs Bilds</span><span class="sxs-lookup"><span data-stu-id="6e930-122">Create a Time Limited Recovery Image</span></span>


<span data-ttu-id="6e930-123">Sie können ein DART-Wiederherstellungsbild erstellen, das nur für eine bestimmte Anzahl von Tagen nach der Generierung verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="6e930-123">You can create a DaRT recovery image that can only be used for a certain number of days after it is generated.</span></span> <span data-ttu-id="6e930-124">Dazu müssen Sie den **Dart-Wiederherstellungsbild-Assistenten** an einer Eingabeaufforderung ausführen und die Anzahl der Tage angeben.</span><span class="sxs-lookup"><span data-stu-id="6e930-124">To do this, you must run the **DaRT Recovery Image Wizard** at a command prompt and specify the number of days.</span></span>

[<span data-ttu-id="6e930-125">So erstellen Sie ein zeitlich begrenztes Wiederherstellungsabbild</span><span class="sxs-lookup"><span data-stu-id="6e930-125">How to Create a Time Limited Recovery Image</span></span>](how-to-create-a-time-limited-recovery-image-dart-7.md)

## <span data-ttu-id="6e930-126">Weitere Ressourcen zum Erstellen des DaRT7-Wiederherstellungs Bilds</span><span class="sxs-lookup"><span data-stu-id="6e930-126">Other resources for creating the DaRT7 recovery image</span></span>


-   [<span data-ttu-id="6e930-127">Bereitstellen von DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="6e930-127">Deploying DaRT 7.0</span></span>](deploying-dart-70-new-ia.md)

 

 





