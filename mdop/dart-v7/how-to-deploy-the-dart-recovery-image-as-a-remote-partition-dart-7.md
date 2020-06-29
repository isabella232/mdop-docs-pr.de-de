---
title: Bereitstellen des DaRT-Wiederherstellungsabbilds in einer Remotepartition
description: Bereitstellen des DaRT-Wiederherstellungsabbilds in einer Remotepartition
author: dansimp
ms.assetid: 757c9340-8eac-42e8-85de-4302e436713a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: a3acdbf72a2c6dac0238f868c7280f1c389b1311
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810033"
---
# <span data-ttu-id="1096b-103">Bereitstellen des DaRT-Wiederherstellungsabbilds in einer Remotepartition</span><span class="sxs-lookup"><span data-stu-id="1096b-103">How to Deploy the DaRT Recovery Image as a Remote Partition</span></span>


<span data-ttu-id="1096b-104">Nachdem Sie den Dart-Wiederherstellungsbild-Assistenten ausgeführt und das Wiederherstellungsabbild erstellt haben, können Sie die Datei "Boot. wim" aus der ISO-Abbilddatei extrahieren und als Remotepartition im Netzwerk bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="1096b-104">After you have finished running the DaRT Recovery Image Wizard and created the recovery image, you can extract the boot.wim file from the ISO image file and deploy it as a remote partition on the network.</span></span>

**<span data-ttu-id="1096b-105">So stellen Sie Dart als Remotepartition bereit</span><span class="sxs-lookup"><span data-stu-id="1096b-105">To deploy DaRT as a remote partition</span></span>**

1.  <span data-ttu-id="1096b-106">Extrahieren Sie die Datei "Boot. wim" aus der Dart-ISO-Abbilddatei.</span><span class="sxs-lookup"><span data-stu-id="1096b-106">Extract the boot.wim file from the DaRT ISO image file.</span></span>

    1.  <span data-ttu-id="1096b-107">Montieren Sie die ISO-Bilddatei, die Sie im Dialogfeld **Startabbild erstellen** erstellt haben, mithilfe der bevorzugten Methode des Unternehmens zum Einbinden eines Bilds.</span><span class="sxs-lookup"><span data-stu-id="1096b-107">Mount the ISO image file that you created in the **Create Startup Image** dialog box by using your company’s preferred method of mounting an image.</span></span>

    2.  <span data-ttu-id="1096b-108">Öffnen Sie die ISO-Abbilddatei, und kopieren Sie die Datei "Boot. wim" aus dem \\sources-Ordner im bereitgestellten Bild an einen Speicherort auf Ihrem Computer oder auf einem externen Laufwerk.</span><span class="sxs-lookup"><span data-stu-id="1096b-108">Open the ISO image file and copy the boot.wim file from the \\sources folder in the mounted image to a location on your computer or on an external drive.</span></span>

        <span data-ttu-id="1096b-109">**Hinweis**  Wenn Sie eine CD oder DVD des Wiederherstellungsabbilds gebrannt haben, können Sie die Dateien auf der CD oder DVD öffnen und die Datei "Boot. wim" aus dem \\sources-Ordner kopieren.</span><span class="sxs-lookup"><span data-stu-id="1096b-109">**Note** If you burned a CD or DVD of the recovery image, you can open the files on the CD or DVD and copy the boot.wim file from the \\sources folder.</span></span> <span data-ttu-id="1096b-110">Damit können Sie die Notwendigkeit überspringen, das Bild bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="1096b-110">This lets you skip the need to mount the image.</span></span>

         

2.  <span data-ttu-id="1096b-111">Stellen Sie die Datei "Boot. wim" auf einem WDS-Server bereit, auf den von Endbenutzercomputern in Ihrem Unternehmen aus zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="1096b-111">Deploy the boot.wim file to a WDS server that can be accessed from end-user computers in your enterprise.</span></span>

3.  <span data-ttu-id="1096b-112">Konfigurieren Sie den WDS-Server so, dass die Boot. WIM-Datei für Dart verwendet wird, indem Sie die Standard Bereitstellungsverfahren für WDS befolgen.</span><span class="sxs-lookup"><span data-stu-id="1096b-112">Configure the WDS server to use the boot.wim file for DaRT by following your standard WDS deployment procedures.</span></span>

<span data-ttu-id="1096b-113">Weitere Informationen zum Bereitstellen von Dart als Remotepartition finden Sie unter den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="1096b-113">For more information about how to deploy DaRT as a remote partition, see the following:</span></span>

-   [<span data-ttu-id="1096b-114">Exemplarische Vorgehensweise: Bereitstellen eines Bilds mithilfe von PXE</span><span class="sxs-lookup"><span data-stu-id="1096b-114">Walkthrough: Deploy an Image by Using PXE</span></span>](https://go.microsoft.com/fwlink/?LinkId=212108)

-   [<span data-ttu-id="1096b-115">Leitfaden für Windows-Bereitstellungsdienste – erste Schritte</span><span class="sxs-lookup"><span data-stu-id="1096b-115">Windows Deployment Services Getting Started Guide</span></span>](https://go.microsoft.com/fwlink/?LinkId=212106)

## <span data-ttu-id="1096b-116">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="1096b-116">Related topics</span></span>


[<span data-ttu-id="1096b-117">Bereitstellen der Wiederherstellungsabbilder von DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="1096b-117">Deploying the DaRT 7.0 Recovery Image</span></span>](deploying-the-dart-70-recovery-image-dart-7.md)

 

 





