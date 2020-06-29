---
title: So stellen Sie das DaRT-Wiederherstellungsabbild als Teil einer Wiederherstellungspartition bereit
description: So stellen Sie das DaRT-Wiederherstellungsabbild als Teil einer Wiederherstellungspartition bereit
author: dansimp
ms.assetid: 462f2d08-f03b-4a07-b2d3-c69205dc6f70
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: e75c3f9e58d784c13003feb84001f89c4607115d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810027"
---
# <span data-ttu-id="d54e5-103">So stellen Sie das DaRT-Wiederherstellungsabbild als Teil einer Wiederherstellungspartition bereit</span><span class="sxs-lookup"><span data-stu-id="d54e5-103">How to Deploy the DaRT Recovery Image as Part of a Recovery Partition</span></span>


<span data-ttu-id="d54e5-104">Nachdem Sie den Dart-Wiederherstellungsbild-Assistenten ausgeführt und das Wiederherstellungsabbild erstellt haben, können Sie die Datei "Boot. wim" aus der ISO-Abbilddatei extrahieren und als Wiederherstellungspartition in einem Windows 7-Abbild bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="d54e5-104">After you have finished running the DaRT Recovery Image Wizard and created the recovery image, you can extract the boot.wim file from the ISO image file and deploy it as a recovery partition in a Windows 7 image.</span></span>

**<span data-ttu-id="d54e5-105">So stellen Sie Dart auf der Wiederherstellungspartition eines Windows 7-Bilds bereit</span><span class="sxs-lookup"><span data-stu-id="d54e5-105">To deploy DaRT in the recovery partition of a Windows 7 image</span></span>**

1.  <span data-ttu-id="d54e5-106">Erstellen Sie eine Zielpartition in Ihrem Windows 7-Abbild, die größer oder gleich der Größe der ISO-Abbilddatei ist, die Sie mit dem **Dart-Bild-Assistenten**erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="d54e5-106">Create a target partition in your Windows 7 image that is equal to or greater than the size of the ISO image file that you created by using the **DaRT Recovery Image Wizard**.</span></span>

    <span data-ttu-id="d54e5-107">Die für eine Dart-Partition erforderliche Mindestgröße beträgt etwa 300MB.</span><span class="sxs-lookup"><span data-stu-id="d54e5-107">The minimum size required for a DaRT partition is approximately 300MB.</span></span> <span data-ttu-id="d54e5-108">Es wird jedoch empfohlen, 450mb gelangte für die Remote Verbindungsfunktion in DART zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="d54e5-108">However, we recommend 450MB to accommodate for the remote connection functionality in DaRT.</span></span>

2.  <span data-ttu-id="d54e5-109">Extrahieren Sie die Datei "Boot. wim" aus der Dart-ISO-Abbilddatei.</span><span class="sxs-lookup"><span data-stu-id="d54e5-109">Extract the boot.wim file from the DaRT ISO image file.</span></span>

    1.  <span data-ttu-id="d54e5-110">Montieren Sie die ISO-Bilddatei, die Sie im Dialogfeld **Startabbild erstellen** erstellt haben, mithilfe der bevorzugten Methode des Unternehmens zum Einbinden eines Bilds.</span><span class="sxs-lookup"><span data-stu-id="d54e5-110">Mount the ISO image file that you created in the **Create Startup Image** dialog box by using your company’s preferred method of mounting an image.</span></span>

    2.  <span data-ttu-id="d54e5-111">Öffnen Sie die ISO-Abbilddatei, und kopieren Sie die Datei "Boot. wim" aus dem \\sources-Ordner im bereitgestellten Bild an einen Speicherort auf Ihrem Computer oder auf einem externen Laufwerk.</span><span class="sxs-lookup"><span data-stu-id="d54e5-111">Open the ISO image file and copy the boot.wim file from the \\sources folder in the mounted image to a location on your computer or on an external drive.</span></span>

        <span data-ttu-id="d54e5-112">**Hinweis**  Wenn Sie eine CD oder DVD des Wiederherstellungsabbilds gebrannt haben, können Sie die Dateien auf der CD oder DVD öffnen und die Datei "Boot. wim" aus dem \\sources-Ordner kopieren.</span><span class="sxs-lookup"><span data-stu-id="d54e5-112">**Note** If you burned a CD or DVD of the recovery image, you can open the files on the CD or DVD and copy the boot.wim file from the \\sources folder.</span></span> <span data-ttu-id="d54e5-113">Damit können Sie die Notwendigkeit überspringen, das Bild bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="d54e5-113">This lets you skip the need to mount the image.</span></span>

         

3.  <span data-ttu-id="d54e5-114">Verwenden Sie die Datei "Boot. wim" zum Erstellen einer startbaren Wiederherstellungspartition mithilfe der Standardmethode Ihres Unternehmens zum Erstellen eines benutzerdefinierten Windows RE-Abbilds.</span><span class="sxs-lookup"><span data-stu-id="d54e5-114">Use the boot.wim file to create a bootable recovery partition by using your company’s standard method for creating a custom Windows RE image.</span></span>

    <span data-ttu-id="d54e5-115">Weitere Informationen zum Erstellen oder Anpassen einer Wiederherstellungspartition finden Sie unter [Anpassen der Windows RE-Benutzeroberfläche](https://go.microsoft.com/fwlink/?LinkId=214222).</span><span class="sxs-lookup"><span data-stu-id="d54e5-115">For more information about how to create or customize a recovery partition, see [Customizing the Windows RE Experience](https://go.microsoft.com/fwlink/?LinkId=214222).</span></span>

4.  <span data-ttu-id="d54e5-116">Ersetzen Sie die Zielpartition in Ihrem Windows 7-Abbild durch die Wiederherstellungspartition.</span><span class="sxs-lookup"><span data-stu-id="d54e5-116">Replace the target partition in your Windows 7 image with the recovery partition.</span></span>

<span data-ttu-id="d54e5-117">Nachdem Sie Ihr Windows 7-Abbild bereitgestellt haben, können Sie es mithilfe des standardmäßigen Bereitstellungsprozesses Ihres Unternehmens an Computer in Ihrem Unternehmen verteilen.</span><span class="sxs-lookup"><span data-stu-id="d54e5-117">After your Windows 7 image is ready, distribute the image to computers in your enterprise by using your company’s standard image deployment process.</span></span> <span data-ttu-id="d54e5-118">Weitere Informationen zum Erstellen eines Windows 7-Bilds finden Sie unter Erstellen [eines Standard Abbilds von Windows 7: schrittweise Anleitung](https://go.microsoft.com/fwlink/?LinkId=212103).</span><span class="sxs-lookup"><span data-stu-id="d54e5-118">For more information about how to create a Windows 7 image, see [Building a Standard Image of Windows 7: Step-by-Step Guide](https://go.microsoft.com/fwlink/?LinkId=212103).</span></span>

<span data-ttu-id="d54e5-119">Weitere Informationen dazu, wie Sie eine Wiederherstellungslösung bereitstellen, um das Factory-Abbild bei einem Systemfehler erneut zu installieren, finden Sie unter [Bereitstellen eines System Wiederherstellungsabbilds](https://go.microsoft.com/fwlink/?LinkId=214221).</span><span class="sxs-lookup"><span data-stu-id="d54e5-119">For more information about how to deploy a recovery solution to reinstall the factory image in the event of a system failure, see [Deploy a System Recovery Image](https://go.microsoft.com/fwlink/?LinkId=214221).</span></span>

## <span data-ttu-id="d54e5-120">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="d54e5-120">Related topics</span></span>


[<span data-ttu-id="d54e5-121">Bereitstellen der Wiederherstellungsabbilder von DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="d54e5-121">Deploying the DaRT 7.0 Recovery Image</span></span>](deploying-the-dart-70-recovery-image-dart-7.md)

 

 





