---
title: Bereitstellen des DaRT-Wiederherstellungsabbilds in einer Remotepartition
description: Bereitstellen des DaRT-Wiederherstellungsabbilds in einer Remotepartition
author: dansimp
ms.assetid: 06a5e250-b992-4f6a-ad74-e7715f9e96e7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 3cdb1313a64bacd652a5253c09f36fa792d0fa3c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804697"
---
# <span data-ttu-id="632b5-103">Bereitstellen des DaRT-Wiederherstellungsabbilds in einer Remotepartition</span><span class="sxs-lookup"><span data-stu-id="632b5-103">How to Deploy the DaRT Recovery Image as a Remote Partition</span></span>


<span data-ttu-id="632b5-104">Nachdem Sie den Microsoft Diagnostics and Recovery Toolset (Dart) 10-Wiederherstellungsbild-Assistenten ausgeführt und das Wiederherstellungsabbild erstellt haben, können Sie die Datei "Boot. wim" aus der ISO-Abbilddatei extrahieren und als Remotepartition im Netzwerk bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="632b5-104">After you have finished running the Microsoft Diagnostics and Recovery Toolset (DaRT) 10 Recovery Image wizard and created the recovery image, you can extract the boot.wim file from the ISO image file and deploy it as a remote partition on the network.</span></span>

**<span data-ttu-id="632b5-105">So stellen Sie Dart 10 als Remotepartition bereit</span><span class="sxs-lookup"><span data-stu-id="632b5-105">To deploy DaRT 10 as a remote partition</span></span>**

1.  <span data-ttu-id="632b5-106">Extrahieren Sie die Datei "Boot. wim" aus der Dart-ISO-Abbilddatei.</span><span class="sxs-lookup"><span data-stu-id="632b5-106">Extract the boot.wim file from the DaRT ISO image file.</span></span>

    1.  <span data-ttu-id="632b5-107">Montieren Sie die ISO-Bilddatei, die Sie im Dialogfeld **Startabbild erstellen** erstellt haben, mithilfe der bevorzugten Methode des Unternehmens zum Einbinden eines Bilds.</span><span class="sxs-lookup"><span data-stu-id="632b5-107">Mount the ISO image file that you created in the **Create Startup Image** dialog box by using your company’s preferred method of mounting an image.</span></span>

    2.  <span data-ttu-id="632b5-108">Öffnen Sie die ISO-Abbilddatei, und kopieren Sie die Datei "Boot. wim" aus dem \\sources-Ordner im bereitgestellten Bild an einen Speicherort auf Ihrem Computer oder auf einem externen Laufwerk.</span><span class="sxs-lookup"><span data-stu-id="632b5-108">Open the ISO image file and copy the boot.wim file from the \\sources folder in the mounted image to a location on your computer or on an external drive.</span></span>

        <span data-ttu-id="632b5-109">**Hinweis**  Wenn Sie eine CD oder DVD des Wiederherstellungsabbilds gebrannt haben, können Sie die Dateien auf der CD oder DVD öffnen und die Datei "Boot. wim" aus dem \\sources-Ordner kopieren.</span><span class="sxs-lookup"><span data-stu-id="632b5-109">**Note** If you burned a CD or DVD of the recovery image, you can open the files on the CD or DVD and copy the boot.wim file from the \\sources folder.</span></span> <span data-ttu-id="632b5-110">Damit können Sie die Notwendigkeit überspringen, das Bild bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="632b5-110">This lets you skip the need to mount the image.</span></span>

         

2.  <span data-ttu-id="632b5-111">Stellen Sie die Datei "Boot. wim" auf einem WDS-Server bereit, auf den von Endbenutzercomputern in Ihrem Unternehmen aus zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="632b5-111">Deploy the boot.wim file to a WDS server that can be accessed from end-user computers in your enterprise.</span></span>

3.  <span data-ttu-id="632b5-112">Konfigurieren Sie den WDS-Server so, dass die Boot. WIM-Datei für Dart verwendet wird, indem Sie die Standard Bereitstellungsverfahren für WDS befolgen.</span><span class="sxs-lookup"><span data-stu-id="632b5-112">Configure the WDS server to use the boot.wim file for DaRT by following your standard WDS deployment procedures.</span></span>

<span data-ttu-id="632b5-113">Weitere Informationen zum Bereitstellen von Dart als Remotepartition finden Sie unter [Exemplarische Vorgehensweise: Bereitstellen eines Bilds mithilfe der PXE](https://go.microsoft.com/fwlink/?LinkId=212108) -und [Windows-Bereitstellungsdienste – Leitfaden für erste Schritte](https://go.microsoft.com/fwlink/?LinkId=212106).</span><span class="sxs-lookup"><span data-stu-id="632b5-113">For more information about how to deploy DaRT as a remote partition, see [Walkthrough: Deploy an Image by Using PXE](https://go.microsoft.com/fwlink/?LinkId=212108) and [Windows Deployment Services Getting Started Guide](https://go.microsoft.com/fwlink/?LinkId=212106).</span></span>

## <span data-ttu-id="632b5-114">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="632b5-114">Related topics</span></span>


[<span data-ttu-id="632b5-115">Erstellen des DaRT 10-Wiederherstellungsabbilds</span><span class="sxs-lookup"><span data-stu-id="632b5-115">Creating the DaRT 10 Recovery Image</span></span>](creating-the-dart-10-recovery-image.md)

[<span data-ttu-id="632b5-116">Bereitstellen des DaRT-Wiederherstellungsabbilds</span><span class="sxs-lookup"><span data-stu-id="632b5-116">Deploying the DaRT Recovery Image</span></span>](deploying-the-dart-recovery-image-dart-10.md)

[<span data-ttu-id="632b5-117">Planen von DaRT 10</span><span class="sxs-lookup"><span data-stu-id="632b5-117">Planning for DaRT 10</span></span>](planning-for-dart-10.md)

 

 





