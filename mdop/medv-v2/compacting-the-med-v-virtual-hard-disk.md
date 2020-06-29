---
title: Komprimieren der virtuellen MED-V-Festplatte
description: Komprimieren der virtuellen MED-V-Festplatte
author: dansimp
ms.assetid: 5e6122d1-9847-4b33-adab-594919eec3c5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f71aefb1e4e901078b4d0a421065b7bd5acdf0ee
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809859"
---
# <span data-ttu-id="02b32-103">Komprimieren der virtuellen MED-V-Festplatte</span><span class="sxs-lookup"><span data-stu-id="02b32-103">Compacting the MED-V Virtual Hard Disk</span></span>


<span data-ttu-id="02b32-104">Obwohl es optional ist, können Sie die virtuelle Festplatte (VHD) komprimieren, um leeren Speicherplatz freizugeben und die Größe der VHD zu verringern, bevor Sie das Windows Virtual PC-Abbild konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="02b32-104">Although it is optional, you can compact the virtual hard disk (VHD) to reclaim empty disk space and reduce the size of the VHD before you configure the Windows Virtual PC image.</span></span>

<span data-ttu-id="02b32-105">**Wichtig**  Bevor Sie fortfahren, erstellen Sie eine Sicherungskopie Ihres Windows XP-Abbilds.</span><span class="sxs-lookup"><span data-stu-id="02b32-105">**Important** Before you proceed, create a backup copy of your Windows XP image.</span></span>

 

**<span data-ttu-id="02b32-106">Vorbereiten der virtuellen Festplatte</span><span class="sxs-lookup"><span data-stu-id="02b32-106">Preparing the Virtual Hard Disk</span></span>**

1.  <span data-ttu-id="02b32-107">Öffnen Sie Ihr Windows XP-Abbild.</span><span class="sxs-lookup"><span data-stu-id="02b32-107">Open your Windows XP image.</span></span>

    <span data-ttu-id="02b32-108">Klicken Sie auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Windows Virtual PC**, klicken Sie auf **Windows Virtual PC**, und doppelklicken Sie dann auf Ihr Windows XP-Abbild.</span><span class="sxs-lookup"><span data-stu-id="02b32-108">Click **Start**, click **All Programs**, click **Windows Virtual PC**, click **Windows Virtual PC**, then double-click your Windows XP image.</span></span>

2.  <span data-ttu-id="02b32-109">Löschen Sie den dll-Cache.</span><span class="sxs-lookup"><span data-stu-id="02b32-109">Clear the DLL cache.</span></span>

    1.  <span data-ttu-id="02b32-110">Geben Sie an einer Eingabeaufforderung auf dem virtuellen Computer **sfc/CacheSize = 1**ein.</span><span class="sxs-lookup"><span data-stu-id="02b32-110">At a command prompt in the virtual machine, type **sfc /cachesize=1**.</span></span>

    2.  <span data-ttu-id="02b32-111">Starten Sie den virtuellen Computer neu.</span><span class="sxs-lookup"><span data-stu-id="02b32-111">Restart the virtual machine.</span></span>

    3.  <span data-ttu-id="02b32-112">Geben Sie an einer Eingabeaufforderung auf dem virtuellen Computer **sfc/PURGECACHE**.</span><span class="sxs-lookup"><span data-stu-id="02b32-112">At a command prompt in the virtual machine, type **sfc /purgecache**.</span></span>

3.  <span data-ttu-id="02b32-113">Löschen Sie nicht benötigte Dateien wie Deinstallationsprogramme, temporäre Dateien, Protokolldateien, Seiten Dateien, freigegebene Ordner usw.</span><span class="sxs-lookup"><span data-stu-id="02b32-113">Delete unnecessary files, such as uninstallers, temp files, log files, page files, shared folders, and so on.</span></span>

4.  <span data-ttu-id="02b32-114">Deaktivieren Sie die System Wiederherstellung.</span><span class="sxs-lookup"><span data-stu-id="02b32-114">Turn off System Restore.</span></span> <span data-ttu-id="02b32-115">Sie können diesen Schritt auch in der Datei "Sysprep. inf" angeben.</span><span class="sxs-lookup"><span data-stu-id="02b32-115">You can also specify this step in your Sysprep.inf file.</span></span>

    1.  <span data-ttu-id="02b32-116">Doppelklicken **Sie in der Systemsteuerung auf** **System**, und wählen Sie dann die Registerkarte **Systemwiederherstellung** aus.</span><span class="sxs-lookup"><span data-stu-id="02b32-116">In **Control Panel**, double-click **System**, and then select the **System Restore** tab.</span></span>

    2.  <span data-ttu-id="02b32-117">Wählen Sie **System Wiederherstellung deaktivieren**aus, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="02b32-117">Select **Turn off System Restore**, and then click **OK**.</span></span>

5.  <span data-ttu-id="02b32-118">Setzen Sie die maximale Größe des Ereignisprotokolls, und löschen Sie alle Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="02b32-118">Set maximum event log sizes and clear all events.</span></span>

    1.  <span data-ttu-id="02b32-119">Öffnen Sie die Ereignisanzeige.</span><span class="sxs-lookup"><span data-stu-id="02b32-119">Open the event viewer.</span></span>

        <span data-ttu-id="02b32-120">Klicken Sie auf **Start**, klicken Sie auf **System**Steuerung, doppelklicken Sie auf **Verwaltung**, und doppelklicken Sie dann auf **Ereignisanzeige**.</span><span class="sxs-lookup"><span data-stu-id="02b32-120">Click **Start**, click **Control Panel**, double-click **Administrative Tools**, then double-click **Event Viewer**.</span></span>

    2.  <span data-ttu-id="02b32-121">Klicken Sie mit der rechten Maustaste auf **Anwendung**, und klicken Sie auf **Eigenschaften**.</span><span class="sxs-lookup"><span data-stu-id="02b32-121">Right-click **Application**, and click **Properties**.</span></span>

    3.  <span data-ttu-id="02b32-122">Legen Sie im Bereich **Log Size** die **Maximale Protokollgröße** auf 512 KB und wählen Sie dann **Ereignisse nach Bedarf überschreiben**aus.</span><span class="sxs-lookup"><span data-stu-id="02b32-122">In the **Log Size** area, set **Maximum Log Size** to 512KB and then select **Overwrite events as needed**.</span></span>

    4.  <span data-ttu-id="02b32-123">Klicken Sie auf **Protokoll löschen**.</span><span class="sxs-lookup"><span data-stu-id="02b32-123">Click **Clear Log**.</span></span> <span data-ttu-id="02b32-124">Klicken Sie im daraufhin angezeigten Dialogfeld **Ereignisanzeige** auf **Nein**.</span><span class="sxs-lookup"><span data-stu-id="02b32-124">In the **Event Viewer** dialog box that appears, click **No**.</span></span>

    5.  <span data-ttu-id="02b32-125">Klicken Sie im **Eigenschaften** Fenster auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="02b32-125">In the **Properties** window, click **OK**.</span></span>

    6.  <span data-ttu-id="02b32-126">Wiederholen Sie die Schritte a bis e für die **Sicherheits** -und **System** Protokolle.</span><span class="sxs-lookup"><span data-stu-id="02b32-126">Repeat steps a through e for the **Security** and **System** logs.</span></span>

6.  <span data-ttu-id="02b32-127">Führen Sie das Tool Datenträgerbereinigung aus.</span><span class="sxs-lookup"><span data-stu-id="02b32-127">Run the Disk Cleanup Tool.</span></span>

    <span data-ttu-id="02b32-128">Klicken Sie auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Zubehör**, klicken Sie auf **System Tools**, und klicken Sie dann auf **Datenträgerbereinigung**.</span><span class="sxs-lookup"><span data-stu-id="02b32-128">Click **Start**, click **All Programs**, click **Accessories**, click **System Tools**, and then click **Disk Cleanup**.</span></span>

7.  <span data-ttu-id="02b32-129">Konfigurieren Sie Ihre Seitendatei nach Bedarf für Ihre Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="02b32-129">Configure your page file as needed for your applications.</span></span>

    1.  <span data-ttu-id="02b32-130">Doppelklicken **Sie in der Systemsteuerung auf** **System**, und wählen Sie dann die Registerkarte **erweitert** aus.</span><span class="sxs-lookup"><span data-stu-id="02b32-130">In **Control Panel**, double-click **System**, and then select the **Advanced** tab.</span></span>

    2.  <span data-ttu-id="02b32-131">Klicken Sie im Bereich " **Leistung** " auf " **Einstellungen**".</span><span class="sxs-lookup"><span data-stu-id="02b32-131">In the **Performance** area, click **Settings**.</span></span>

    3.  <span data-ttu-id="02b32-132">Klicken Sie im Bereich **virtueller Speicher** auf **ändern**.</span><span class="sxs-lookup"><span data-stu-id="02b32-132">In the **Virtual Memory** area, click **Change**.</span></span>

    4.  <span data-ttu-id="02b32-133">Konfigurieren Sie Ihre Seitendatei Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="02b32-133">Configure your page file settings.</span></span>

8.  <span data-ttu-id="02b32-134">Fahren Sie das Windows XP-Abbild herunter.</span><span class="sxs-lookup"><span data-stu-id="02b32-134">Shut down the Windows XP image.</span></span>

**<span data-ttu-id="02b32-135">Defragmentieren und vorkomprimieren der virtuellen Festplatte</span><span class="sxs-lookup"><span data-stu-id="02b32-135">Defragmenting and Pre-compacting the Virtual Hard Disk</span></span>**

1.  <span data-ttu-id="02b32-136">Klicken Sie in der **System** Steuerung auf dem Hostcomputer unter Windows 7 auf **Verwaltungs Tools**, doppelklicken Sie auf **Computerverwaltung**, und klicken Sie dann auf **Datenträgerverwaltung**.</span><span class="sxs-lookup"><span data-stu-id="02b32-136">In **Control Panel** on the host computer that is running Windows 7, click **Administrative Tools**, double-click **Computer Management**, then click **Disk Management**.</span></span>

2.  <span data-ttu-id="02b32-137">Wenn Sie die Datenträger-Verwaltungskonsole verwenden, fügen Sie die virtuelle Festplatte an (mounten), und Defragmentieren Sie die Festplatte.</span><span class="sxs-lookup"><span data-stu-id="02b32-137">By using the Disk Management Console, attach (mount) the virtual hard disk and then defragment the disk.</span></span>

3.  <span data-ttu-id="02b32-138">Extrahieren Sie mithilfe eines ISO-Extraktionstools die Datei "precompact. ISO", die sich im Ordner \\Program Files\\Windows Virtual PC\\Integration Components befindet.</span><span class="sxs-lookup"><span data-stu-id="02b32-138">By using an ISO extraction tool, extract the precompact.iso located in the \\Program Files\\Windows Virtual PC\\Integration Components folder.</span></span>

4.  <span data-ttu-id="02b32-139">Verwenden Sie das precompact.exe-Programm, um die virtuelle Windows XP-Festplatte zu komprimieren.</span><span class="sxs-lookup"><span data-stu-id="02b32-139">Use the precompact.exe program to compress the Windows XP virtual hard disk.</span></span>

5.  <span data-ttu-id="02b32-140">Trennen Sie die virtuelle Festplatte mithilfe der Datenträgerverwaltungskonsole.</span><span class="sxs-lookup"><span data-stu-id="02b32-140">By using the Disk Management Console, detach the virtual hard disk.</span></span>

**<span data-ttu-id="02b32-141">Komprimieren der virtuellen Festplatte</span><span class="sxs-lookup"><span data-stu-id="02b32-141">Compacting the Virtual Hard Disk</span></span>**

1.  <span data-ttu-id="02b32-142">Öffnen Sie Windows Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="02b32-142">Open Windows Virtual PC.</span></span>

    <span data-ttu-id="02b32-143">Klicken Sie auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Windows Virtual PC**, und klicken Sie dann auf **Windows Virtual PC**.</span><span class="sxs-lookup"><span data-stu-id="02b32-143">Click **Start**, click **All Programs**, click **Windows Virtual PC**, then click **Windows Virtual PC**.</span></span>

2.  <span data-ttu-id="02b32-144">Klicken Sie mit der rechten Maustaste auf Ihr Windows XP-Bild, und wählen Sie **Einstellungen**aus.</span><span class="sxs-lookup"><span data-stu-id="02b32-144">Right-click your Windows XP image and select **Settings**.</span></span>

3.  <span data-ttu-id="02b32-145">Klicken Sie auf die **Festplatte** für diejenige, die Ihrem Windows XP-Abbild entspricht, und klicken Sie dann auf **ändern**.</span><span class="sxs-lookup"><span data-stu-id="02b32-145">Click **Hard Disk** for the one that corresponds to your Windows XP image, and then click **Modify**.</span></span>

4.  <span data-ttu-id="02b32-146">Klicken Sie auf **virtuelle Festplatte komprimieren**.</span><span class="sxs-lookup"><span data-stu-id="02b32-146">Click **Compact virtual hard disk**.</span></span>

5.  <span data-ttu-id="02b32-147">Klicken Sie auf **komprimieren** , und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="02b32-147">Click **Compact** and then click **OK**.</span></span>

<span data-ttu-id="02b32-148">Erstellen Sie eine Sicherungskopie Ihrer komprimierten virtuellen Festplatte.</span><span class="sxs-lookup"><span data-stu-id="02b32-148">Create a backup copy of your compacted virtual hard disk.</span></span>

## <span data-ttu-id="02b32-149">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="02b32-149">Related topics</span></span>


[<span data-ttu-id="02b32-150">Konfigurieren eines virtuellen Windows-PC-Images für MED-V</span><span class="sxs-lookup"><span data-stu-id="02b32-150">Configuring a Windows Virtual PC Image for MED-V</span></span>](configuring-a-windows-virtual-pc-image-for-med-v.md)

[<span data-ttu-id="02b32-151">Technische Referenz für MED-V</span><span class="sxs-lookup"><span data-stu-id="02b32-151">Technical Reference for MED-V</span></span>](technical-reference-for-med-v.md)

 

 





