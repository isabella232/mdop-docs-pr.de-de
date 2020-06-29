---
title: So stellen Sie das DaRT-Wiederherstellungsabbild als Teil einer Wiederherstellungspartition bereit
description: So stellen Sie das DaRT-Wiederherstellungsabbild als Teil einer Wiederherstellungspartition bereit
author: dansimp
ms.assetid: 07c5d539-51d9-4759-adc7-72b40d5d7bb3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: e3647d684f64a0635e2875314498bde841204369
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810522"
---
# <span data-ttu-id="c191a-103">So stellen Sie das DaRT-Wiederherstellungsabbild als Teil einer Wiederherstellungspartition bereit</span><span class="sxs-lookup"><span data-stu-id="c191a-103">How to Deploy the DaRT Recovery Image as Part of a Recovery Partition</span></span>


<span data-ttu-id="c191a-104">Nachdem Sie den Microsoft Diagnostics and Recovery Toolset (Dart) 8,0-Wiederherstellungsbild-Assistenten ausgeführt und das Wiederherstellungsabbild erstellt haben, können Sie die Datei "Boot. wim" aus der ISO-Abbilddatei extrahieren und als Wiederherstellungspartition in einem Windows 8-Abbild bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="c191a-104">After you have finished running the Microsoft Diagnostics and Recovery Toolset (DaRT) 8.0 Recovery Image wizard and created the recovery image, you can extract the boot.wim file from the ISO image file and deploy it as a recovery partition in a Windows 8 image.</span></span> <span data-ttu-id="c191a-105">Eine Partition wird empfohlen, da alle Beschädigungsprobleme, die das Starten des Windows-Betriebssystems verhindern, auch das Starten des Wiederherstellungs Bilds verhindern.</span><span class="sxs-lookup"><span data-stu-id="c191a-105">A partition is recommended, because any corruption issues that prevent the Windows operating system from starting would also prevent the recovery image from starting.</span></span> <span data-ttu-id="c191a-106">Eine separate Partition verhindert auch, dass der BitLocker-Wiederherstellungsschlüssel zweimal bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="c191a-106">A separate partition also eliminates the need to provide the BitLocker recovery key twice.</span></span> <span data-ttu-id="c191a-107">Sie sollten die Partition ausblenden, um zu verhindern, dass Benutzer Dateien darin speichern.</span><span class="sxs-lookup"><span data-stu-id="c191a-107">Consider hiding the partition to prevent users from storing files on it.</span></span>

**<span data-ttu-id="c191a-108">So stellen Sie Dart auf der Wiederherstellungspartition eines Windows 8-Bilds bereit</span><span class="sxs-lookup"><span data-stu-id="c191a-108">To deploy DaRT in the recovery partition of a Windows 8 image</span></span>**

1.  <span data-ttu-id="c191a-109">Erstellen Sie eine Zielpartition in Ihrem Windows 8-Abbild, die größer oder gleich der Größe der ISO-Abbilddatei ist, die Sie mit dem **Dart 8,0-Wiederherstellungsbild-Assistenten**erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="c191a-109">Create a target partition in your Windows 8 image that is equal to or greater than the size of the ISO image file that you created by using the **DaRT 8.0 Recovery Image wizard**.</span></span>

    <span data-ttu-id="c191a-110">Die für eine Dart-Partition erforderliche Mindestgröße beträgt 500 MB, um die Remote Verbindungsfunktion in DART zu berücksichtigen.</span><span class="sxs-lookup"><span data-stu-id="c191a-110">The minimum size required for a DaRT partition is 500MB to accommodate the remote connection functionality in DaRT.</span></span>

2.  <span data-ttu-id="c191a-111">Extrahieren Sie die Datei "Boot. wim" aus der Dart-ISO-Abbilddatei.</span><span class="sxs-lookup"><span data-stu-id="c191a-111">Extract the boot.wim file from the DaRT ISO image file.</span></span>

    1.  <span data-ttu-id="c191a-112">Montieren Sie die ISO-Bilddatei, die Sie auf der Seite **Startabbild erstellen** erstellt haben, mithilfe der bevorzugten Methode Ihres Unternehmens.</span><span class="sxs-lookup"><span data-stu-id="c191a-112">Using your company’s preferred method, mount the ISO image file that you created on the **Create Startup Image** page.</span></span>

    2.  <span data-ttu-id="c191a-113">Öffnen Sie die ISO-Abbilddatei, und kopieren Sie die Datei "Boot. wim" aus dem \\sources-Ordner im bereitgestellten Bild an einen Speicherort auf Ihrem Computer oder auf einem externen Laufwerk.</span><span class="sxs-lookup"><span data-stu-id="c191a-113">Open the ISO image file and copy the boot.wim file from the \\sources folder in the mounted image to a location on your computer or on an external drive.</span></span>

        <span data-ttu-id="c191a-114">**Hinweis**  Wenn Sie eine CD, DVD oder einen USB-Anschluss des Wiederherstellungs Bilds gebrannt haben, können Sie die Dateien auf dem Wechselmedium öffnen und die Datei "Boot. wim" aus dem \\sources-Ordner kopieren.</span><span class="sxs-lookup"><span data-stu-id="c191a-114">**Note** If you burned a CD, DVD, or USB of the recovery image, you can open the files on the removable media and copy the boot.wim file from the \\sources folder.</span></span> <span data-ttu-id="c191a-115">Wenn Sie die Datei "Boot. wim" kopieren, müssen Sie das Bild nicht bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="c191a-115">If you copy boot.wim file, you don’t need to mount the image.</span></span>

         

3.  <span data-ttu-id="c191a-116">Verwenden Sie die Datei "Boot. wim" zum Erstellen einer startbaren Wiederherstellungspartition mithilfe der Standardmethode Ihres Unternehmens zum Erstellen eines benutzerdefinierten Windows RE-Abbilds.</span><span class="sxs-lookup"><span data-stu-id="c191a-116">Use the boot.wim file to create a bootable recovery partition by using your company’s standard method for creating a custom Windows RE image.</span></span>

    <span data-ttu-id="c191a-117">Weitere Informationen zum Erstellen oder Anpassen einer Wiederherstellungspartition finden Sie unter [Anpassen der Windows RE-Benutzeroberfläche](https://go.microsoft.com/fwlink/?LinkId=214222).</span><span class="sxs-lookup"><span data-stu-id="c191a-117">For more information about how to create or customize a recovery partition, see [Customizing the Windows RE Experience](https://go.microsoft.com/fwlink/?LinkId=214222).</span></span>

4.  <span data-ttu-id="c191a-118">Ersetzen Sie die Zielpartition in Ihrem Windows 8-Abbild durch die Wiederherstellungspartition.</span><span class="sxs-lookup"><span data-stu-id="c191a-118">Replace the target partition in your Windows 8 image with the recovery partition.</span></span>

    <span data-ttu-id="c191a-119">Weitere Informationen dazu, wie Sie eine Wiederherstellungslösung bereitstellen, um das Factory-Abbild bei einem Systemfehler erneut zu installieren, finden Sie unter [Bereitstellen eines System Wiederherstellungsabbilds](https://go.microsoft.com/fwlink/?LinkId=214221).</span><span class="sxs-lookup"><span data-stu-id="c191a-119">For more information about how to deploy a recovery solution to reinstall the factory image in the event of a system failure, see [Deploy a System Recovery Image](https://go.microsoft.com/fwlink/?LinkId=214221).</span></span>

## <span data-ttu-id="c191a-120">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="c191a-120">Related topics</span></span>


[<span data-ttu-id="c191a-121">Erstellen des DaRT 8.0-Wiederherstellungsabbilds</span><span class="sxs-lookup"><span data-stu-id="c191a-121">Creating the DaRT 8.0 Recovery Image</span></span>](creating-the-dart-80-recovery-image-dart-8.md)

[<span data-ttu-id="c191a-122">Bereitstellen der DaRT-Recovery-Images</span><span class="sxs-lookup"><span data-stu-id="c191a-122">Deploying the DaRT Recovery Image</span></span>](deploying-the-dart-recovery-image-dart-8.md)

[<span data-ttu-id="c191a-123">Planen von DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="c191a-123">Planning for DaRT 8.0</span></span>](planning-for-dart-80-dart-8.md)

 

 





