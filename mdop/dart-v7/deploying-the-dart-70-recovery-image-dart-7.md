---
title: Bereitstellen der Wiederherstellungsabbilder von DaRT 7.0
description: Bereitstellen der Wiederherstellungsabbilder von DaRT 7.0
author: dansimp
ms.assetid: 6bba7bff-800f-44e4-bcfc-e143115607ca
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: cef626e50bf1049529c51afca5e536b03b3d915d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804391"
---
# <span data-ttu-id="b6671-103">Bereitstellen der Wiederherstellungsabbilder von DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="b6671-103">Deploying the DaRT 7.0 Recovery Image</span></span>


<span data-ttu-id="b6671-104">Nachdem Sie die Datei für die internationale Organisation für Standardisierung (ISO) erstellt haben, die das Wiederherstellungsabbild Microsoft Diagnostics and Recovery Toolset (Dart) 7 enthält, können Sie das DART-Wiederherstellungsabbild im gesamten Unternehmen bereitstellen, damit es für Endbenutzer und Helpdesk-Agents verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="b6671-104">After you have created the International Organization for Standardization (ISO) file that contains the Microsoft Diagnostics and Recovery Toolset (DaRT)7 recovery image, you can deploy the DaRT recovery image throughout your enterprise so that it is available to end users and helpdesk agents.</span></span> <span data-ttu-id="b6671-105">Es gibt vier unterstützte Methoden, mit denen Sie das DART-Wiederherstellungsbild bereitstellen können.</span><span class="sxs-lookup"><span data-stu-id="b6671-105">There are four supported methods that you can use to deploy the DaRT recovery image.</span></span>

-   <span data-ttu-id="b6671-106">Brennen der ISO-Abbilddatei auf eine CD oder DVD</span><span class="sxs-lookup"><span data-stu-id="b6671-106">Burn the ISO image file to a CD or DVD</span></span>

-   <span data-ttu-id="b6671-107">Speichern des Inhalts der ISO-Abbilddatei auf einem USB-Flash Laufwerk</span><span class="sxs-lookup"><span data-stu-id="b6671-107">Save the contents of the ISO image file to a USB Flash Drive (UFD)</span></span>

-   <span data-ttu-id="b6671-108">Extrahieren Sie die Datei "Boot. wim" aus dem ISO-Abbild, und stellen Sie Sie als Remotepartition bereit, die für Endbenutzercomputer verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="b6671-108">Extract the boot.wim file from the ISO image and deploy as a remote partition that is available to end-user computers</span></span>

-   <span data-ttu-id="b6671-109">Extrahieren der Datei "Boot. wim" aus dem ISO-Abbild und Bereitstellen in der Wiederherstellungspartition einer neuen Windows 7-Installation</span><span class="sxs-lookup"><span data-stu-id="b6671-109">Extract the boot.wim file from the ISO image and deploy in the recovery partition of a new Windows 7 installation</span></span>

<span data-ttu-id="b6671-110">**Wichtig**  Der **Dart-Wiederherstellungsbild-Assistent** bietet nur die Option zum Brennen einer CD oder DVD.</span><span class="sxs-lookup"><span data-stu-id="b6671-110">**Important** The **DaRT Recovery Image Wizard** only provides the option to burn a CD or DVD.</span></span> <span data-ttu-id="b6671-111">Alle anderen Methoden zum Speichern und Bereitstellen des Wiederherstellungsabbilds erfordern zusätzliche Schritte, die Tools beinhalten, die nicht in DART enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="b6671-111">All other methods of saving and deploying the recovery image require additional steps that involve tools that are not included in DaRT.</span></span> <span data-ttu-id="b6671-112">In diesem Abschnitt finden Sie einige Anleitungen und Links zu diesen anderen Methoden.</span><span class="sxs-lookup"><span data-stu-id="b6671-112">Some guidance and links for these other methods are provided in this section.</span></span>

 

## <span data-ttu-id="b6671-113">Bereitstellen des DART-Wiederherstellungs Bilds mithilfe eines USB-Flash Laufwerks</span><span class="sxs-lookup"><span data-stu-id="b6671-113">Deploy the DaRT Recovery Image Using a USB Flash Drive</span></span>


<span data-ttu-id="b6671-114">Nachdem Sie den Bild-Assistenten für die Dart-Wiederherstellung ausgeführt haben, können Sie das Tool unter verwenden, um <https://go.microsoft.com/fwlink/?LinkId=218888> die ISO-Bilddatei auf ein USB-Flashlaufwerk (USB-Stick) zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="b6671-114">After you have finished running the DaRT Recovery Image Wizard, you can use the tool at <https://go.microsoft.com/fwlink/?LinkId=218888> to copy the ISO image file to a USB flash drive (UFD).</span></span>

[<span data-ttu-id="b6671-115">So stellen Sie das DaRT-Wiederherstellungsabbild über ein USB-Flashlaufwerk bereit</span><span class="sxs-lookup"><span data-stu-id="b6671-115">How to Deploy the DaRT Recovery Image Using a USB Flash Drive</span></span>](how-to-deploy-the-dart-recovery-image-using-a-usb-flash-drive-dart-7.md)

## <span data-ttu-id="b6671-116">Bereitstellen des DART-Wiederherstellungs Bilds als Teil einer Wiederherstellungs Partition</span><span class="sxs-lookup"><span data-stu-id="b6671-116">Deploy the DaRT Recovery Image as Part of a Recovery Partition</span></span>


<span data-ttu-id="b6671-117">Nachdem Sie den Dart-Wiederherstellungsbild-Assistenten ausgeführt und das Wiederherstellungsabbild erstellt haben, können Sie die Datei "Boot. wim" aus der ISO-Abbilddatei extrahieren und als Wiederherstellungspartition in einem Windows 7-Abbild bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="b6671-117">After you have finished running the DaRT Recovery Image Wizard and created the recovery image, you can extract the boot.wim file from the ISO image file and deploy it as a recovery partition in a Windows 7 image.</span></span>

[<span data-ttu-id="b6671-118">So stellen Sie das DaRT-Wiederherstellungsabbild als Teil einer Wiederherstellungspartition bereit</span><span class="sxs-lookup"><span data-stu-id="b6671-118">How to Deploy the DaRT Recovery Image as Part of a Recovery Partition</span></span>](how-to-deploy-the-dart-recovery-image-as-part-of-a-recovery-partition-dart-7.md)

## <span data-ttu-id="b6671-119">Bereitstellen des DART-Wiederherstellungs Bilds als Remote Partition</span><span class="sxs-lookup"><span data-stu-id="b6671-119">Deploy the DaRT Recovery Image as a Remote Partition</span></span>


<span data-ttu-id="b6671-120">Nachdem Sie den Dart-Wiederherstellungsbild-Assistenten ausgeführt und das Wiederherstellungsabbild erstellt haben, können Sie die Datei "Boot. wim" aus der ISO-Abbilddatei extrahieren und als Remotepartition im Netzwerk bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="b6671-120">After you have finished running the DaRT Recovery Image Wizard and created the recovery image, you can extract the boot.wim file from the ISO image file and deploy it as a remote partition on the network.</span></span>

[<span data-ttu-id="b6671-121">Bereitstellen des DaRT-Wiederherstellungsabbilds in einer Remotepartition</span><span class="sxs-lookup"><span data-stu-id="b6671-121">How to Deploy the DaRT Recovery Image as a Remote Partition</span></span>](how-to-deploy-the-dart-recovery-image-as-a-remote-partition-dart-7.md)

## <span data-ttu-id="b6671-122">Weitere Ressourcen zum Verwalten der Bereitstellung des DART-Wiederherstellungs Bilds</span><span class="sxs-lookup"><span data-stu-id="b6671-122">Other resources for maintaining Deploying the DaRT Recovery Image</span></span>


-   [<span data-ttu-id="b6671-123">Bereitstellen von DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="b6671-123">Deploying DaRT 7.0</span></span>](deploying-dart-70-new-ia.md)

 

 





