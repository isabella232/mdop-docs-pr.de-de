---
title: Bereitstellen der DaRT-Recovery-Images
description: Bereitstellen der DaRT-Recovery-Images
author: dansimp
ms.assetid: 2b859da6-e31a-4240-8868-93a754328cf2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7de3ed9c01a1808364158124c4f2dcab835823a7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804736"
---
# <span data-ttu-id="85b7a-103">Bereitstellen der DaRT-Recovery-Images</span><span class="sxs-lookup"><span data-stu-id="85b7a-103">Deploying the DaRT Recovery Image</span></span>


<span data-ttu-id="85b7a-104">Nachdem Sie die Datei für die internationale Organisation für Standardisierung (ISO) erstellt haben, die das Wiederherstellungsabbild Microsoft Diagnostics and Recovery Toolset (Dart) 10 enthält, können Sie das DART 10-Wiederherstellungsabbild im gesamten Unternehmen bereitstellen, damit es für Endbenutzer und Helpdesk-Mitarbeiter zur Verfügung steht.</span><span class="sxs-lookup"><span data-stu-id="85b7a-104">After you have created the International Organization for Standardization (ISO) file that contains the Microsoft Diagnostics and Recovery Toolset (DaRT) 10 recovery image, you can deploy the DaRT 10 recovery image throughout your enterprise so that it is available to end users and help desk workers.</span></span> <span data-ttu-id="85b7a-105">Es gibt vier unterstützte Methoden, mit denen Sie das DART-Wiederherstellungsbild bereitstellen können.</span><span class="sxs-lookup"><span data-stu-id="85b7a-105">There are four supported methods that you can use to deploy the DaRT recovery image.</span></span> <span data-ttu-id="85b7a-106">Informationen zum Überprüfen der vor-und Nachteile der einzelnen Methoden finden Sie unter [Planen des Speicherns und Bereitstellen des Wiederherstellungs Bilds von DART 10](planning-how-to-save-and-deploy-the-dart-10-recovery-image.md).</span><span class="sxs-lookup"><span data-stu-id="85b7a-106">To review the advantages and disadvantages of each method, see [Planning How to Save and Deploy the DaRT 10 Recovery Image](planning-how-to-save-and-deploy-the-dart-10-recovery-image.md).</span></span>

<span data-ttu-id="85b7a-107">Brennen der ISO-Abbilddatei auf eine CD oder DVD mithilfe des DART-Wiederherstellungs-Bild-Assistenten</span><span class="sxs-lookup"><span data-stu-id="85b7a-107">Burn the ISO image file to a CD or DVD by using the DaRT Recovery Image wizard</span></span>

<span data-ttu-id="85b7a-108">Speichern des Inhalts der ISO-Abbilddatei auf einem USB-Flash Laufwerk (USB-Stick) mithilfe des DART-Wiederherstellungs-Bild-Assistenten</span><span class="sxs-lookup"><span data-stu-id="85b7a-108">Save the contents of the ISO image file to a USB Flash Drive (UFD) by using the DaRT Recovery Image wizard</span></span>

<span data-ttu-id="85b7a-109">Extrahieren Sie die Datei "Boot. wim" aus dem ISO-Abbild, und stellen Sie Sie als Remotepartition bereit, die für Endbenutzercomputer verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="85b7a-109">Extract the boot.wim file from the ISO image and deploy as a remote partition that is available to end-user computers</span></span>

<span data-ttu-id="85b7a-110">Extrahieren der Datei "Boot. wim" aus dem ISO-Abbild und Bereitstellen in der Wiederherstellungspartition einer neuen Windows 10-Installation</span><span class="sxs-lookup"><span data-stu-id="85b7a-110">Extract the boot.wim file from the ISO image and deploy in the recovery partition of a new Windows 10 installation</span></span>

<span data-ttu-id="85b7a-111">**Wichtig**  Der **Dart-Wiederherstellungs-Bild-Assistent** bietet die Möglichkeit, das Bild auf eine CD, DVD oder ein USB-Laufwerk zu brennen, aber die anderen Methoden zum Speichern und Bereitstellen des Wiederherstellungsabbilds erfordern zusätzliche Schritte, die Tools beinhalten, die nicht in DART enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="85b7a-111">**Important** The **DaRT Recovery Image Wizard** provides the option to burn the image to a CD, DVD or UFD, but the other methods of saving and deploying the recovery image require additional steps that involve tools that are not included in DaRT.</span></span> <span data-ttu-id="85b7a-112">In diesem Abschnitt finden Sie einige Anleitungen und Links zu diesen anderen Methoden.</span><span class="sxs-lookup"><span data-stu-id="85b7a-112">Some guidance and links for these other methods are provided in this section.</span></span>

 

## <span data-ttu-id="85b7a-113">Bereitstellen des DART-Wiederherstellungs Bilds als Teil einer Wiederherstellungspartition</span><span class="sxs-lookup"><span data-stu-id="85b7a-113">Deploy the DaRT recovery image as part of a recovery partition</span></span>


<span data-ttu-id="85b7a-114">Nachdem Sie den Dart-Wiederherstellungsbild-Assistenten ausgeführt und das Wiederherstellungsabbild erstellt haben, können Sie die Datei "Boot. wim" aus der ISO-Abbilddatei extrahieren und als Wiederherstellungspartition in einem Windows 10-Abbild bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="85b7a-114">After you have finished running the DaRT Recovery Image wizard and created the recovery image, you can extract the boot.wim file from the ISO image file and deploy it as a recovery partition in a Windows 10 image.</span></span>

[<span data-ttu-id="85b7a-115">So stellen Sie das DaRT-Wiederherstellungsabbild als Teil einer Wiederherstellungspartition bereit</span><span class="sxs-lookup"><span data-stu-id="85b7a-115">How to Deploy the DaRT Recovery Image as Part of a Recovery Partition</span></span>](how-to-deploy-the-dart-recovery-image-as-part-of-a-recovery-partition-dart-10.md)

## <span data-ttu-id="85b7a-116">Bereitstellen des DART-Wiederherstellungs Bilds als Remotepartition</span><span class="sxs-lookup"><span data-stu-id="85b7a-116">Deploy the DaRT recovery image as a remote partition</span></span>


<span data-ttu-id="85b7a-117">Sie können das Wiederherstellungsabbild auf einem zentralen Netzwerk-Start Server wie Windows-Bereitstellungsdienste hosten und Benutzern oder Supportmitarbeitern die Möglichkeit geben, das Bild bei Bedarf auf Computer zu streamen.</span><span class="sxs-lookup"><span data-stu-id="85b7a-117">You can host the recovery image on a central network boot server, such as Windows Deployment Services, and allow users or support staff to stream the image to computers on demand.</span></span>

[<span data-ttu-id="85b7a-118">Bereitstellen des DaRT-Wiederherstellungsabbilds in einer Remotepartition</span><span class="sxs-lookup"><span data-stu-id="85b7a-118">How to Deploy the DaRT Recovery Image as a Remote Partition</span></span>](how-to-deploy-the-dart-recovery-image-as-a-remote-partition-dart-10.md)

## <span data-ttu-id="85b7a-119">Weitere Ressourcen für die Bereitstellung des DART-Wiederherstellungs Bilds</span><span class="sxs-lookup"><span data-stu-id="85b7a-119">Other resources for deploying the DaRT recovery image</span></span>


[<span data-ttu-id="85b7a-120">Bereitstellen von DaRT 10</span><span class="sxs-lookup"><span data-stu-id="85b7a-120">Deploying DaRT 10</span></span>](deploying-dart-10.md)

 

 





