---
title: So stellen Sie das DaRT-Wiederherstellungsabbild über ein USB-Flashlaufwerk bereit
description: So stellen Sie das DaRT-Wiederherstellungsabbild über ein USB-Flashlaufwerk bereit
author: dansimp
ms.assetid: 5b7aa843-731e-47e7-b5f9-48d08da732d6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 1228c9cb5f870162f285d726d48721dde1185107
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810093"
---
# <span data-ttu-id="ef279-103">So stellen Sie das DaRT-Wiederherstellungsabbild über ein USB-Flashlaufwerk bereit</span><span class="sxs-lookup"><span data-stu-id="ef279-103">How to Deploy the DaRT Recovery Image Using a USB Flash Drive</span></span>


<span data-ttu-id="ef279-104">Nachdem Sie den Bild-Assistenten für die **Dart-Wiederherstellung**ausgeführt haben, können Sie das Tool unter verwenden, um <https://go.microsoft.com/fwlink/?LinkId=218888> die ISO-Bilddatei auf ein USB-Flashlaufwerk (USB-Stick) zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="ef279-104">After you have finished running the **DaRT Recovery Image Wizard**, you can use the tool at <https://go.microsoft.com/fwlink/?LinkId=218888> to copy the ISO image file to a USB flash drive (UFD).</span></span>

<span data-ttu-id="ef279-105">Sie können die ISO-Abbilddatei auch manuell auf ein USB-Flashlaufwerk kopieren, indem Sie die Schritte in diesem Abschnitt ausführen.</span><span class="sxs-lookup"><span data-stu-id="ef279-105">You can also manually copy the ISO image file to a UFD by following the steps provided in this section.</span></span>

**<span data-ttu-id="ef279-106">So speichern Sie das DART-Wiederherstellungsabbild auf einem USB-Speicherstick</span><span class="sxs-lookup"><span data-stu-id="ef279-106">To save the DaRT recovery image to a USB flash drive</span></span>**

1.  <span data-ttu-id="ef279-107">Formatieren Sie den USB-Speicherstick.</span><span class="sxs-lookup"><span data-stu-id="ef279-107">Format the USB flash drive.</span></span>

    1.  <span data-ttu-id="ef279-108">Legen Sie in einer laufenden gültigen Betriebssystem-oder windowsPE-Sitzung Ihr USB-Flashlaufwerk ein.</span><span class="sxs-lookup"><span data-stu-id="ef279-108">From a running valid operating system or WindowsPE session, insert your UFD.</span></span>

    2.  <span data-ttu-id="ef279-109">Geben Sie an der Eingabeaufforderung mit Administratorberechtigungen **DiskPart** ein, und geben Sie dann **List Disk**ein.</span><span class="sxs-lookup"><span data-stu-id="ef279-109">At the command prompt with administrator permissions, type **DISKPART** and then type **LIST DISK**.</span></span>

        <span data-ttu-id="ef279-110">Das Eingabeaufforderungsfenster zeigt die Datenträgernummer Ihres USB-Flashlaufwerks an, beispielsweise **Datenträger 1**.</span><span class="sxs-lookup"><span data-stu-id="ef279-110">The Command Prompt window displays the disk number of your UFD, for example **DISK 1**.</span></span>

    3.  <span data-ttu-id="ef279-111">Geben Sie die folgenden Befehle einzeln an der Eingabeaufforderung ein.</span><span class="sxs-lookup"><span data-stu-id="ef279-111">Enter the following commands one at a time at the command prompt.</span></span>

        ``` syntax
        SELECT DISK 1
        CLEAN
        CREATE PARTITION PRIMARY
        SELECT PARTITION 1
        ACTIVE
        FORMAT FS=NTFS
        ASSIGN
        EXIT
        ```

        <span data-ttu-id="ef279-112">**Hinweis**  Im vorherigen Codebeispiel wird davon ausgegangen, dass Disk1 das USB-Laufwerk ist.</span><span class="sxs-lookup"><span data-stu-id="ef279-112">**Note** The previous code example assumes Disk1 is the UFD.</span></span> <span data-ttu-id="ef279-113">Wenn dies erforderlich ist, ersetzen Sie Datenträger 1 durch ihre Datenträgernummer.</span><span class="sxs-lookup"><span data-stu-id="ef279-113">If it is necessary, replace DISK 1 with your disk number.</span></span>

         

2.  <span data-ttu-id="ef279-114">Wenn Sie die bevorzugte Methode Ihres Unternehmens zum Montieren eines Bilds verwenden, montieren Sie die ISO-Bilddatei, die Sie im Dialogfeld **Startabbild erstellen** des **Dart-Assistenten**für die Bildwiederherstellung erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="ef279-114">By using your company’s preferred method of mounting an image, mount the ISO image file that you created in the **Create Startup Image** dialog box of the **DaRT Recovery Image Wizard**.</span></span> <span data-ttu-id="ef279-115">Dies erfordert, dass Sie eine Methode zum Bereitstelleneiner Bilddatei zur Verfügung haben.</span><span class="sxs-lookup"><span data-stu-id="ef279-115">This requires that you have a method available to mount an image file.</span></span>

3.  <span data-ttu-id="ef279-116">Öffnen Sie die bereitgestellte ISO-Abbilddatei, und kopieren Sie den gesamten Inhalt auf den formatierten USB-Stick.</span><span class="sxs-lookup"><span data-stu-id="ef279-116">Open the mounted ISO image file and copy all its contents to the formatted USB flash drive.</span></span>

    <span data-ttu-id="ef279-117">**Hinweis**  Wenn Sie eine CD oder DVD des Wiederherstellungsabbilds gebrannt haben, können Sie die Dateien auf der CD oder DVD öffnen und den Inhalt auf das USB-Flashlaufwerk kopieren.</span><span class="sxs-lookup"><span data-stu-id="ef279-117">**Note** If you burned a CD or DVD of the recovery image, you can open the files on the CD or DVD and copy the contents to the UFD.</span></span> <span data-ttu-id="ef279-118">Damit können Sie die Notwendigkeit überspringen, das Bild bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="ef279-118">This lets you skip the need to mount the image.</span></span>

     

## <span data-ttu-id="ef279-119">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="ef279-119">Related topics</span></span>


[<span data-ttu-id="ef279-120">Bereitstellen der Wiederherstellungsabbilder von DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="ef279-120">Deploying the DaRT 7.0 Recovery Image</span></span>](deploying-the-dart-70-recovery-image-dart-7.md)

 

 





