---
title: Erstellen des DaRT 8.0-Wiederherstellungsabbilds
description: Erstellen des DaRT 8.0-Wiederherstellungsabbilds
author: dansimp
ms.assetid: 39001b8e-86c0-45ef-8f34-2d6199f9922d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/21/2017
ms.openlocfilehash: 79ce5859e7d0eacf95124c2a7409ff6c21890d65
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804313"
---
# <span data-ttu-id="215e5-103">Erstellen des DaRT 8.0-Wiederherstellungsabbilds</span><span class="sxs-lookup"><span data-stu-id="215e5-103">Creating the DaRT 8.0 Recovery Image</span></span>


<span data-ttu-id="215e5-104">Nachdem Sie Microsoft Diagnostics and Recovery Toolset (Dart) 8,0 installiert haben, erstellen Sie ein Dart 8,0-Wiederherstellungsabbild.</span><span class="sxs-lookup"><span data-stu-id="215e5-104">After installing Microsoft Diagnostics and Recovery Toolset (DaRT) 8.0, you create a DaRT 8.0 recovery image.</span></span> <span data-ttu-id="215e5-105">Das Wiederherstellungsabbild startet Windows RE, aus dem Sie dann die Dart-Tools starten können.</span><span class="sxs-lookup"><span data-stu-id="215e5-105">The recovery image starts Windows RE, from which you can then start the DaRT tools.</span></span> <span data-ttu-id="215e5-106">Sie können internationale Organisation für Standardisierungs Dateien (ISO) und Wim-Bilder (Windows Imaging Format) erstellen.</span><span class="sxs-lookup"><span data-stu-id="215e5-106">You can generate International Organization for Standardization (ISO) files and Windows Imaging Format (WIM) images.</span></span> <span data-ttu-id="215e5-107">Darüber hinaus können Sie mithilfe von PowerShell Skripts generieren, die die Einstellungen verwenden, die Sie im Dart-Wiederherstellungsbild-Assistenten ausgewählt haben.</span><span class="sxs-lookup"><span data-stu-id="215e5-107">In addition, you can use PowerShell to generate scripts that use the settings you select in the DaRT Recovery Image wizard.</span></span> <span data-ttu-id="215e5-108">Sie können das Skript später verwenden, um Wiederherstellungs Bilder mithilfe der gleichen Einstellungen wiederherzustellen.</span><span class="sxs-lookup"><span data-stu-id="215e5-108">You can use the script later to rebuild recovery images by using the same settings.</span></span> <span data-ttu-id="215e5-109">Das Wiederherstellungsabbild bietet eine Reihe von Wiederherstellungstools.</span><span class="sxs-lookup"><span data-stu-id="215e5-109">The recovery image provides a variety of recovery tools.</span></span> <span data-ttu-id="215e5-110">Eine Beschreibung der Tools finden Sie unter [Übersicht über die Tools in Dart 8,0](overview-of-the-tools-in-dart-80-dart-8.md).</span><span class="sxs-lookup"><span data-stu-id="215e5-110">For a description of the tools, see [Overview of the Tools in DaRT 8.0](overview-of-the-tools-in-dart-80-dart-8.md).</span></span>

<span data-ttu-id="215e5-111">Nachdem Sie den Computer in DART gestartet haben, können Sie die verschiedenen Dart-Tools ausführen, um zu versuchen, den Computer zu diagnostizieren und zu reparieren.</span><span class="sxs-lookup"><span data-stu-id="215e5-111">After you boot the computer into DaRT, you can run the different DaRT tools to try to diagnose and repair the computer.</span></span> <span data-ttu-id="215e5-112">In diesem Abschnitt werden Sie durch den Vorgang zum Erstellen des DART-Wiederherstellungs Bilds geführt, in dem Sie die Tools und Features auswählen können, die Sie als Teil des Bilds einfügen möchten.</span><span class="sxs-lookup"><span data-stu-id="215e5-112">This section walks you through the process of creating the DaRT recovery image and lets you select the tools and features that you want to include as part of the image.</span></span>

<span data-ttu-id="215e5-113">Sie können das DART-Wiederherstellungsabbild mithilfe einer der beiden folgenden Methoden erstellen:</span><span class="sxs-lookup"><span data-stu-id="215e5-113">You can create the DaRT recovery image by using either of two methods:</span></span>

-   <span data-ttu-id="215e5-114">Verwenden Sie den Dart-Wiederherstellungsbild-Assistenten, der in einer Windows-Umgebung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="215e5-114">Use the DaRT Recovery Image wizard, which runs in a Windows environment.</span></span>

-   <span data-ttu-id="215e5-115">Ändern Sie ein Beispiel-PowerShell-Skript mit den gewünschten Werten.</span><span class="sxs-lookup"><span data-stu-id="215e5-115">Modify an example PowerShell script with the values you want.</span></span> <span data-ttu-id="215e5-116">Weitere Informationen finden Sie unter [so wird es gemacht: Verwenden eines PowerShell-Skripts zum Erstellen des Wiederherstellungsabbilds](how-to-use-a-powershell-script-to-create-the-recovery-image-dart-8.md).</span><span class="sxs-lookup"><span data-stu-id="215e5-116">For more information, see [How to Use a PowerShell Script to Create the Recovery Image](how-to-use-a-powershell-script-to-create-the-recovery-image-dart-8.md).</span></span>

<span data-ttu-id="215e5-117">Sie können die ISO auf eine beschreibbare CD oder DVD schreiben, Sie auf einem USB-Stick speichern oder in einem Format speichern, das Sie zum Booten von DART von einer Remotepartition oder einer Wiederherstellungspartition verwenden können.</span><span class="sxs-lookup"><span data-stu-id="215e5-117">You can write the ISO to a recordable CD or DVD, save it to a USB flash drive, or save it in a format that you can use to boot into DaRT from a remote partition or from a recovery partition.</span></span>

<span data-ttu-id="215e5-118">Nachdem Sie das ISO-Abbild erstellt haben, können Sie es auf eine leere CD oder DVD brennen (wenn Ihr Computer über ein CD-oder DVD-Laufwerk verfügt).</span><span class="sxs-lookup"><span data-stu-id="215e5-118">Once you have created the ISO image, you can burn it onto a blank CD or DVD (if your computer has a CD or DVD drive).</span></span> <span data-ttu-id="215e5-119">Wenn Ihr Computer nicht über ein Laufwerk für diesen Zweck verfügt, können Sie die meisten generischen Programme verwenden, mit denen CDs oder DVDs gebrannt werden.</span><span class="sxs-lookup"><span data-stu-id="215e5-119">If your computer does not have a drive for this purpose, you can use most generic programs that are used to burn CDs or DVDs.</span></span>

## <span data-ttu-id="215e5-120">Auswählen der Bildarchitektur und angeben des Pfads</span><span class="sxs-lookup"><span data-stu-id="215e5-120">Select the image architecture and specify the path</span></span>


<span data-ttu-id="215e5-121">Auf der Windows 8 Media-Seite Wählen Sie aus, ob Sie ein 32-Bit-oder 64-Bit-Dart-Wiederherstellungsbild erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="215e5-121">On the Windows 8 Media page, you select whether to create a 32-bit or 64-bit DaRT recovery image.</span></span> <span data-ttu-id="215e5-122">Verwenden Sie das 32-Bit-Fenster zum Erstellen von 32-Bit-Dart-Wiederherstellungs Bildern und 64-Bit-Windows zum Erstellen von 64-Bit-Dart-Wiederherstellungs Bildern.</span><span class="sxs-lookup"><span data-stu-id="215e5-122">Use the 32-bit Windows to build 32-bit DaRT recovery images, and 64-bit Windows to build 64-bit DaRT recovery images.</span></span> <span data-ttu-id="215e5-123">Sie können einen einzelnen Computer verwenden, um Wiederherstellungs Bilder für beide Architekturtypen zu erstellen, Sie können jedoch kein einzelnes Bild erstellen, das sowohl auf 32-Bit-als auch auf 64-Bit-Architekturen funktioniert.</span><span class="sxs-lookup"><span data-stu-id="215e5-123">You can use a single computer to create recovery images for both architecture types, but you cannot create one image that works on both 32-bit and 64-bit architectures.</span></span> <span data-ttu-id="215e5-124">Außerdem geben Sie den Pfad der Windows 8-Installationsmedien an.</span><span class="sxs-lookup"><span data-stu-id="215e5-124">You also indicate the path of the Windows 8 installation media.</span></span> <span data-ttu-id="215e5-125">Wählen Sie die Architektur aus, die dem von Ihnen erstellten Wiederherstellungsbild entspricht.</span><span class="sxs-lookup"><span data-stu-id="215e5-125">Choose the architecture that matches the one of the recovery image that you are creating.</span></span>

**<span data-ttu-id="215e5-126">So wählen Sie die Bildarchitektur aus und geben den Pfad an</span><span class="sxs-lookup"><span data-stu-id="215e5-126">To select the image architecture and specify the path</span></span>**

1.  <span data-ttu-id="215e5-127">Wählen Sie auf der Seite **Windows 8 Media** eine der folgenden Optionen aus:</span><span class="sxs-lookup"><span data-stu-id="215e5-127">On the **Windows 8 Media** page, select one of the following:</span></span>

    -   <span data-ttu-id="215e5-128">Wenn Sie ein Wiederherstellungsabbild für 64-Bit-Computer erstellen, wählen Sie **x64-(64-Bit-) Dart-Bild erstellen**aus.</span><span class="sxs-lookup"><span data-stu-id="215e5-128">If you are creating a recovery image for 64-bit computers, select **Create x64 (64-bit) DaRT image**.</span></span>

    -   <span data-ttu-id="215e5-129">Wenn Sie ein Wiederherstellungsabbild für 32-Bit-Computer erstellen, wählen Sie **x86 (32-Bit) Dart-Bild erstellen**aus.</span><span class="sxs-lookup"><span data-stu-id="215e5-129">If you are creating a recovery image for 32-bit computers, select **Create x86 (32-bit) DaRT image**.</span></span>

2.  <span data-ttu-id="215e5-130">Geben Sie im Feld **Geben Sie den Stammpfad des Windows 8 &lt; 64-Bit-oder 32-Bit- &gt; Installationsmediums** an den Pfad der Windows 8-Installationsdateien ein.</span><span class="sxs-lookup"><span data-stu-id="215e5-130">In the **Specify the root path of the Windows 8 &lt;64-bit or 32-bit&gt; install media** box, type the path of the Windows 8 installation files.</span></span> <span data-ttu-id="215e5-131">Verwenden Sie einen Pfad, der der Architektur des Wiederherstellungs Bilds entspricht, das Sie erstellen.</span><span class="sxs-lookup"><span data-stu-id="215e5-131">Use a path that matches the architecture of the recovery image that you are creating.</span></span>

3.  <span data-ttu-id="215e5-132">Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="215e5-132">Click **Next**.</span></span>

## <span data-ttu-id="215e5-133">Auswählen der Tools, die in das Wiederherstellungsabbild aufgenommen werden sollen</span><span class="sxs-lookup"><span data-stu-id="215e5-133">Select the tools to include on the recovery image</span></span>


<span data-ttu-id="215e5-134">Auf der Seite Extras können Sie zahlreiche Tools auswählen, die in das Wiederherstellungsabbild aufgenommen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="215e5-134">On the Tools page, you can select numerous tools to include on the recovery image.</span></span> <span data-ttu-id="215e5-135">Diese Tools stehen Endbenutzern zur Verfügung, wenn Sie in das DART-Bild Booten.</span><span class="sxs-lookup"><span data-stu-id="215e5-135">These tools will be available to end users when they boot into the DaRT image.</span></span> <span data-ttu-id="215e5-136">Wenn Sie jedoch beim Erstellen des DART-Bilds die Remotekonnektivität aktivieren, stehen alle Tools zur Verfügung, wenn ein Mitarbeiter des Helpdesks eine Verbindung mit dem Computer des Endbenutzers herstellt, unabhängig davon, welche Tools Sie in das Bild aufgenommen haben.</span><span class="sxs-lookup"><span data-stu-id="215e5-136">However, if you enable remote connectivity when creating the DaRT image, all of the tools will be available when a help desk worker connects to the end user’s computer, regardless of which tools you chose to include on the image.</span></span>

<span data-ttu-id="215e5-137">Wenn Sie den Endbenutzer Zugriff auf diese Tools einschränken, aber weiterhin den vollständigen Zugriff auf die Tools über die Remote Verbindungsanzeige behalten möchten, wählen Sie diese Tools auf der Seite Tools nicht aus.</span><span class="sxs-lookup"><span data-stu-id="215e5-137">To restrict end-user access to these tools, but still retain full access to the tools through the Remote Connection Viewer, do not select those tools on the Tools page.</span></span> <span data-ttu-id="215e5-138">Endbenutzer können nur die Remote Verbindung verwenden und können alle Tools, die Sie aus dem Wiederherstellungsabbild ausschließen, sehen, aber nicht darauf zugreifen.</span><span class="sxs-lookup"><span data-stu-id="215e5-138">End users will be able to use only Remote Connection and will be able to see, but not access, any tools that you exclude from the recovery image.</span></span>

**<span data-ttu-id="215e5-139">So wählen Sie die Tools aus, die Sie in das Wiederherstellungsabbild einbeziehen möchten</span><span class="sxs-lookup"><span data-stu-id="215e5-139">To select the tools to include on the recovery image</span></span>**

1.  <span data-ttu-id="215e5-140">Aktivieren Sie auf der Seite **Extras** das Kontrollkästchen neben jedem Tool, das Sie in das Bild einbeziehen möchten.</span><span class="sxs-lookup"><span data-stu-id="215e5-140">On the **Tools** page, select the check box beside each tool that you want to include on the image.</span></span>

2.  <span data-ttu-id="215e5-141">Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="215e5-141">Click **Next**.</span></span>

## <span data-ttu-id="215e5-142">Auswählen, ob die Remotekonnektivität von einem Helpdesk zugelassen werden soll</span><span class="sxs-lookup"><span data-stu-id="215e5-142">Choose whether to allow remote connectivity by a help desk</span></span>


<span data-ttu-id="215e5-143">Auf der Seite Remote Verbindung können Sie festlegen, dass ein Helpdesk-Mitarbeiter eine Remoteverbindung herstellen und die Dart-Tools auf dem Computer eines Endbenutzers ausführen soll.</span><span class="sxs-lookup"><span data-stu-id="215e5-143">On the Remote Connection page, you can choose to enable a help desk worker to remotely connect to and run the DaRT tools on an end user’s computer.</span></span> <span data-ttu-id="215e5-144">Die Option Remotekonnektivität wird dann im Fenster Diagnose-und Wiederherstellungs-Toolset als verfügbare Option angezeigt.</span><span class="sxs-lookup"><span data-stu-id="215e5-144">The remote connectivity option is then shown as an available option in the Diagnostics and Recovery Toolset window.</span></span> <span data-ttu-id="215e5-145">Nachdem die Helpdesk-Mitarbeiter eine Remoteverbindung hergestellt haben, können Sie die Dart-Tools auf dem Endbenutzercomputer von einem Remotestandort aus ausführen.</span><span class="sxs-lookup"><span data-stu-id="215e5-145">After help desk workers establish a remote connection, they can run the DaRT tools on the end-user computer from a remote location.</span></span>

**<span data-ttu-id="215e5-146">So wählen Sie aus, ob die Remotekonnektivität von Helpdesk-Mitarbeitern zugelassen werden soll</span><span class="sxs-lookup"><span data-stu-id="215e5-146">To choose whether to allow remote connectivity by help desk workers</span></span>**

1.  <span data-ttu-id="215e5-147">Aktivieren Sie auf der Seite **Remoteverbindung** das Kontrollkästchen **Remoteverbindungen zulassen** , um Remoteverbindungen zuzulassen, oder deaktivieren Sie das Kontrollkästchen, um Remoteverbindungen zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="215e5-147">On the **Remote Connection** page, select the **Allow remote connections** check box to allow remote connections, or clear the check box to prevent remote connections.</span></span>

2.  <span data-ttu-id="215e5-148">Wenn Sie das Kontrollkästchen **Remoteverbindungen zulassen** deaktiviert haben, klicken Sie auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="215e5-148">If you cleared the **Allow remote connections** check box, click **Next**.</span></span> <span data-ttu-id="215e5-149">Fahren Sie andernfalls mit dem nächsten Schritt fort, um die Konfiguration der Remotekonnektivität fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="215e5-149">Otherwise, go to the next step to continue configuring remote connectivity.</span></span>

3.  <span data-ttu-id="215e5-150">Wählen Sie eine der folgenden Optionen:</span><span class="sxs-lookup"><span data-stu-id="215e5-150">Select one of the following:</span></span>

    -   <span data-ttu-id="215e5-151">Lassen Sie Windows eine offene Portnummer auswählen.</span><span class="sxs-lookup"><span data-stu-id="215e5-151">Let Windows choose an open port number.</span></span>

    -   <span data-ttu-id="215e5-152">Geben Sie die Portnummer an.</span><span class="sxs-lookup"><span data-stu-id="215e5-152">Specify the port number.</span></span> <span data-ttu-id="215e5-153">Wenn Sie diese Option auswählen, geben Sie eine Portnummer zwischen 1 und 65535 in das Feld unterhalb der Option ein.</span><span class="sxs-lookup"><span data-stu-id="215e5-153">If you select this option, enter a port number between 1 and 65535 in the field beneath the option.</span></span> <span data-ttu-id="215e5-154">Diese Portnummer wird beim Einrichten einer Remoteverbindung verwendet.</span><span class="sxs-lookup"><span data-stu-id="215e5-154">This port number will be used when establishing a remote connection.</span></span> <span data-ttu-id="215e5-155">Wir empfehlen, dass die Portnummer 1024 oder höher ist, um die Möglichkeit eines Konflikts zu minimieren.</span><span class="sxs-lookup"><span data-stu-id="215e5-155">We recommend that the port number be 1024 or higher to minimize the possibility of a conflict.</span></span>

4.  <span data-ttu-id="215e5-156">(Optional) erstellen Sie im Dialogfeld "Willkommensnachricht für **Remoteverbindung** " eine benutzerdefinierte Nachricht, die Endbenutzer erhalten, wenn Sie eine Remoteverbindung herstellen.</span><span class="sxs-lookup"><span data-stu-id="215e5-156">(Optional) in the **Remote connection welcome** message box, create a customized message that end users receive when they establish a remote connection.</span></span> <span data-ttu-id="215e5-157">Die Nachricht kann maximal 2048 Zeichen umfassen.</span><span class="sxs-lookup"><span data-stu-id="215e5-157">The message can be a maximum of 2048 characters.</span></span>

5.  <span data-ttu-id="215e5-158">Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="215e5-158">Click **Next**.</span></span>

    <span data-ttu-id="215e5-159">Weitere Informationen dazu, wie Sie die Dart-Tools Remote ausführen können, finden Sie unter [Wiederherstellen von Remotecomputern mithilfe des DART-Wiederherstellungs Bilds](how-to-recover-remote-computers-by-using-the-dart-recovery-image-dart-8.md).</span><span class="sxs-lookup"><span data-stu-id="215e5-159">For more information about running the DaRT tools remotely, see [How to Recover Remote Computers by Using the DaRT Recovery Image](how-to-recover-remote-computers-by-using-the-dart-recovery-image-dart-8.md).</span></span>

## <span data-ttu-id="215e5-160">Hinzufügen von Treibern zum Wiederherstellungsabbild</span><span class="sxs-lookup"><span data-stu-id="215e5-160">Add drivers to the recovery image</span></span>


<span data-ttu-id="215e5-161">Auf der Registerkarte "Treiber" auf der Seite "Erweiterte Optionen" können Sie zusätzliche Gerätetreiber hinzufügen, die Sie möglicherweise benötigen, wenn Sie einen Computer reparieren.</span><span class="sxs-lookup"><span data-stu-id="215e5-161">On the Drivers tab of the Advanced Options page, you can add additional device drivers that you may need when repairing a computer.</span></span> <span data-ttu-id="215e5-162">Diese können in der Regelspeicher-oder Netzwerk Controller enthalten, die von Windows 8 nicht bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="215e5-162">These may typically include storage or network controllers that Windows 8 does not provide.</span></span> <span data-ttu-id="215e5-163">Treiber werden installiert, wenn das Bild erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="215e5-163">Drivers are installed when the image is created.</span></span>

<span data-ttu-id="215e5-164">**Wichtig**  Beachten Sie bei der Auswahl der zu berücksichtigenden Treiber, dass drahtlose Verbindungen (wie Bluetooth oder 802.11 a/b/g/n) in DART nicht unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="215e5-164">**Important** When you select drivers to include, be aware that wireless connectivity (such as Bluetooth or 802.11a/b/g/n) is not supported in DaRT.</span></span>

 

**<span data-ttu-id="215e5-165">So fügen Sie dem Wiederherstellungsabbild Treiber hinzu</span><span class="sxs-lookup"><span data-stu-id="215e5-165">To add drivers to the recovery image</span></span>**

1.  <span data-ttu-id="215e5-166">Klicken Sie auf der Seite **Erweiterte Optionen** auf die Registerkarte **Treiber** .</span><span class="sxs-lookup"><span data-stu-id="215e5-166">On the **Advanced Options** page, click the **Drivers** tab.</span></span>

2.  <span data-ttu-id="215e5-167">Klicken Sie auf **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="215e5-167">Click **Add**.</span></span>

3.  <span data-ttu-id="215e5-168">Navigieren Sie zu der Datei, die für den Treiber hinzugefügt werden soll, und klicken Sie dann auf **Öffnen**.</span><span class="sxs-lookup"><span data-stu-id="215e5-168">Browse to the file to be added for the driver, and then click **Open**.</span></span>

    <span data-ttu-id="215e5-169">**Hinweis**  Die Treiberdatei wird vom Hersteller des Speichers oder des Netzwerkcontrollers bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="215e5-169">**Note** The driver file is provided by the manufacturer of the storage or network controller.</span></span>

     

4.  <span data-ttu-id="215e5-170">Wiederholen Sie die Schritte 2 und 3 für jeden Treiber, den Sie einbeziehen möchten.</span><span class="sxs-lookup"><span data-stu-id="215e5-170">Repeat Steps 2 and 3 for every driver that you want to include.</span></span>

5.  <span data-ttu-id="215e5-171">Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="215e5-171">Click **Next**.</span></span>

## <span data-ttu-id="215e5-172">Hinzufügen von optionalen WinPE-Paketen zum Wiederherstellungsabbild</span><span class="sxs-lookup"><span data-stu-id="215e5-172">Add WinPE optional packages to the recovery image</span></span>


<span data-ttu-id="215e5-173">Auf der Registerkarte "WinPE" auf der Seite "Erweiterte Optionen" können Sie dem Dart-Bild optionale WinPE-Pakete hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="215e5-173">On the WinPE tab of the Advanced Options page, you can add WinPE optional packages to the DaRT image.</span></span> <span data-ttu-id="215e5-174">Diese Pakete sind Teil des Windows ADK, das eine Installationsvoraussetzung für den Dart-Wiederherstellungsbild-Assistenten ist.</span><span class="sxs-lookup"><span data-stu-id="215e5-174">These packages are part of the Windows ADK, which is an installation prerequisite for the DaRT Recovery Image wizard.</span></span> <span data-ttu-id="215e5-175">Die Tools, die Sie auswählen können, sind alle optional.</span><span class="sxs-lookup"><span data-stu-id="215e5-175">The tools that you can select are all optional.</span></span> <span data-ttu-id="215e5-176">Alle erforderlichen Pakete werden automatisch basierend auf den Tools hinzugefügt, die Sie auf der Seite "Tools" ausgewählt haben.</span><span class="sxs-lookup"><span data-stu-id="215e5-176">Any required packages are added automatically, based on the tools you selected on the Tools page.</span></span>

<span data-ttu-id="215e5-177">Sie können auch die Größe des Scratch-Space angeben.</span><span class="sxs-lookup"><span data-stu-id="215e5-177">You can also specify the size of the scratch space.</span></span> <span data-ttu-id="215e5-178">Scratch-Speicherplatz ist die Größe des RAM-Speicherplatzes, der für die Ausführung von DART reserviert ist.</span><span class="sxs-lookup"><span data-stu-id="215e5-178">Scratch space is the amount of RAM disk space that is set aside for DaRT to run.</span></span> <span data-ttu-id="215e5-179">Der Scratch-Bereich ist nützlich, wenn die Festplatte des Endbenutzers nicht verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="215e5-179">The scratch space is useful in case the end user’s hard disk is not available.</span></span> <span data-ttu-id="215e5-180">Wenn Sie zusätzliche Tools und Treiber ausführen, möchten Sie möglicherweise den Scratch-Platz erhöhen.</span><span class="sxs-lookup"><span data-stu-id="215e5-180">If you are running additional tools and drivers, you may want to increase the scratch space.</span></span>

**<span data-ttu-id="215e5-181">So fügen Sie dem Wiederherstellungsabbild optionale WinPE-Pakete hinzu</span><span class="sxs-lookup"><span data-stu-id="215e5-181">To add WinPE optional packages to the recovery image</span></span>**

1.  <span data-ttu-id="215e5-182">Klicken Sie auf der Seite **Erweiterte Optionen** auf die Registerkarte **WinPE** .</span><span class="sxs-lookup"><span data-stu-id="215e5-182">On the **Advanced Options** page, click the **WinPE** tab.</span></span>

2.  <span data-ttu-id="215e5-183">Aktivieren Sie das Kontrollkästchen neben jedem Paket, das Sie in das Bild einbeziehen möchten, oder klicken Sie auf das Kontrollkästchen **Name** , um alle Pakete auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="215e5-183">Select the check box beside each package that you want to include on the image, or click the **Name** check box to select all of the packages.</span></span>

3.  <span data-ttu-id="215e5-184">Wählen Sie im Feld **Scratch Space** den RAM-Speicherplatz aus, der für die Ausführung von DART reserviert werden soll, falls die Festplatte des Endbenutzers nicht verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="215e5-184">In the **Scratch Space** field, select the amount of RAM disk space to allocate for running DaRT in case the end user’s hard disk is not available.</span></span>

4.  <span data-ttu-id="215e5-185">Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="215e5-185">Click **Next**.</span></span>

## <span data-ttu-id="215e5-186">Hinzufügen der Debugging-Tools für Crash Analyzer</span><span class="sxs-lookup"><span data-stu-id="215e5-186">Add the debugging tools for Crash Analyzer</span></span>


<span data-ttu-id="215e5-187">Wenn Sie das Tool Absturzanalyse in das ISO-Abbild einbeziehen, müssen Sie auch die Debugging-Tools für Windows einbeziehen.</span><span class="sxs-lookup"><span data-stu-id="215e5-187">If you include the Crash Analyzer tool in the ISO image, you must also include the Debugging Tools for Windows.</span></span> <span data-ttu-id="215e5-188">Auf der Seite "Erweiterte Optionen" auf der Registerkarte Crash Analyzer geben Sie den Pfad der Windows 8-Debugging-Tools ein, die von Crash Analyzer zum Analysieren von Speicherabbilddateien verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="215e5-188">On the Crash Analyzer tab of the Advanced Options page, you enter the path of the Windows 8 Debugging Tools, which Crash Analyzer uses to analyze memory dump files.</span></span> <span data-ttu-id="215e5-189">Sie können die Tools verwenden, die sich auf dem Computer befinden, auf dem Sie den Dart-Wiederherstellungsbild-Assistenten ausführen, oder Sie können die Tools verwenden, die sich auf dem Computer des Endbenutzers befinden.</span><span class="sxs-lookup"><span data-stu-id="215e5-189">You can use the tools that are on the computer where you are running the DaRT Recovery Image wizard, or you can use the tools that are on the end-user computer.</span></span> <span data-ttu-id="215e5-190">Wenn Sie die Tools auf dem Endbenutzercomputer verwenden möchten, denken Sie daran, dass auf jedem Computer, den Sie diagnostizieren, die Debug-Tools installiert sein müssen.</span><span class="sxs-lookup"><span data-stu-id="215e5-190">If you decide to use the tools on the end-user computer, remember that every computer that you diagnose must have the Debugging Tools installed.</span></span>

<span data-ttu-id="215e5-191">Wenn Sie das Microsoft Windows Software Development Kit (SDK) oder das Microsoft Windows Development Kit (WDK) installiert haben, werden die Windows 8-Debugging-Tools standardmäßig zum Wiederherstellungsbild hinzugefügt, und der Pfad zu den Debugging-Tools wird automatisch ausgefüllt.</span><span class="sxs-lookup"><span data-stu-id="215e5-191">If you installed the Microsoft Windows Software Development Kit (SDK) or the Microsoft Windows Development Kit (WDK), the Windows 8 Debugging Tools are added to the recovery image by default, and the path to the Debugging Tools is automatically filled in.</span></span> <span data-ttu-id="215e5-192">Sie können den Pfad der Windows 8-Debugging-Tools ändern, wenn sich die Dateien an einem anderen Ort als dem durch den Standard Dateipfad angegebenen Speicherort befinden.</span><span class="sxs-lookup"><span data-stu-id="215e5-192">You can change the path of the Windows 8 Debugging Tools if the files are located somewhere other than the location indicated by the default file path.</span></span> <span data-ttu-id="215e5-193">Mit einem Link im Assistenten können Sie Debugging-Tools für Windows herunterladen und installieren, wenn diese noch nicht installiert sind.</span><span class="sxs-lookup"><span data-stu-id="215e5-193">A link in the wizard lets you download and install debugging tools for Windows if they are not already installed.</span></span>

<span data-ttu-id="215e5-194">Informationen zum Herunterladen der Windows-Debugging-Tools finden Sie unter [Debuggen von Tools für Windows](https://go.microsoft.com/fwlink/?LinkId=266248).</span><span class="sxs-lookup"><span data-stu-id="215e5-194">To download the Windows Debugging Tools, see [Debugging Tools for Windows](https://go.microsoft.com/fwlink/?LinkId=266248).</span></span> <span data-ttu-id="215e5-195">Installieren Sie die Debug-Tools am Standardspeicherort.</span><span class="sxs-lookup"><span data-stu-id="215e5-195">Install the Debugging Tools to the default location.</span></span>

<span data-ttu-id="215e5-196">**Hinweis**  Der Dart-Assistent überprüft die Tools im `HKLM\Software\Microsoft\Windows Kits\Installed Roots\WindowsDebuggersRoot` Registrierungsschlüssel.</span><span class="sxs-lookup"><span data-stu-id="215e5-196">**Note** The DaRT wizard checks for the tools in the `HKLM\Software\Microsoft\Windows Kits\Installed Roots\WindowsDebuggersRoot` registry key.</span></span> <span data-ttu-id="215e5-197">Wenn der Registrierungswert nicht vorhanden ist, sucht der Assistent je nach ihrer Systemarchitektur an einem der folgenden Speicherorte:</span><span class="sxs-lookup"><span data-stu-id="215e5-197">If the registry value is not there, the wizard looks in one of the following locations, depending on your system architecture:</span></span>

`%ProgramFilesX86%\Windows Kits\8.0\Debuggers\x64`

`%ProgramFilesX86%\Windows Kits\8.0\Debuggers\x86`

 

**<span data-ttu-id="215e5-198">So fügen Sie die Debugging-Tools für Crash Analyzer hinzu</span><span class="sxs-lookup"><span data-stu-id="215e5-198">To add the debugging tools for Crash Analyzer</span></span>**

1.  <span data-ttu-id="215e5-199">Klicken Sie auf der Seite **Erweiterte Optionen** auf die Registerkarte **Crash Analyzer** .</span><span class="sxs-lookup"><span data-stu-id="215e5-199">On the **Advanced Options** page, click the **Crash Analyzer** tab.</span></span>

2.  <span data-ttu-id="215e5-200">Optional Klicken Sie auf **Debug-Tools herunterladen** , um die Debugging-Tools für Windows herunterzuladen.</span><span class="sxs-lookup"><span data-stu-id="215e5-200">(Optional) Click **Download the Debugging Tools** to download the Debugging Tools for Windows.</span></span>

3.  <span data-ttu-id="215e5-201">Wählen Sie eine der folgenden Optionen aus:</span><span class="sxs-lookup"><span data-stu-id="215e5-201">Select one of the following options:</span></span>

    -   <span data-ttu-id="215e5-202">**Schließen Sie die Windows 8 &lt; 64-Bit-oder 32-Bit- &gt; Debugging-Tools ein**.</span><span class="sxs-lookup"><span data-stu-id="215e5-202">**Include the Windows 8 &lt;64-bit or 32-bit&gt; Debugging Tools**.</span></span> <span data-ttu-id="215e5-203">Wenn Sie diese Option auswählen, navigieren Sie zu dem Speicherort der Tools, und wählen Sie ihn aus, wenn der Pfad noch nicht angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="215e5-203">If you select this option, browse to and select the location of the tools if the path is not already displaying.</span></span>

    -   <span data-ttu-id="215e5-204">**Verwenden Sie die Debugging-Tools des Systems, das gedebuggt wird**.</span><span class="sxs-lookup"><span data-stu-id="215e5-204">**Use the Debugging Tools from the system that is being debugged**.</span></span> <span data-ttu-id="215e5-205">Wenn Sie diese Option auswählen, funktioniert der Absturzanalyse Programm nicht, wenn die Debugging-Tools für Windows auf dem Problem Computer nicht gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="215e5-205">If you select this option, the Crash Analyzer will not work if the Debugging Tools for Windows are not found on the problem computer.</span></span>

4.  <span data-ttu-id="215e5-206">Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="215e5-206">Click **Next**.</span></span>

## <span data-ttu-id="215e5-207">Hinzufügen von Definitionen für das Defender-Tool</span><span class="sxs-lookup"><span data-stu-id="215e5-207">Add definitions for the Defender tool</span></span>


<span data-ttu-id="215e5-208">Auf der Registerkarte Defender der Seite Erweiterte Optionen fügen Sie Definitionen hinzu, die vom Defender-Tool verwendet werden, um zu ermitteln, ob Software, die versucht, die Einstellungen auf einem Computer zu installieren, auszuführen oder zu ändern, unerwünschte oder bösartige Software ist.</span><span class="sxs-lookup"><span data-stu-id="215e5-208">On the Defender tab of the Advanced Options page, you add definitions, which are used by the Defender tool to determine whether software that is trying to install, run, or change settings on a computer is unwanted or malicious software.</span></span>

**<span data-ttu-id="215e5-209">So fügen Sie Definitionen für das Defender-Tool hinzu</span><span class="sxs-lookup"><span data-stu-id="215e5-209">To add definitions for the Defender tool</span></span>**

1.  <span data-ttu-id="215e5-210">Klicken Sie auf der Seite **Erweiterte Optionen** auf die Registerkarte **Defender** .</span><span class="sxs-lookup"><span data-stu-id="215e5-210">On the **Advanced Options** page, click the **Defender** tab.</span></span>

2.  <span data-ttu-id="215e5-211">Wählen Sie eine der folgenden Optionen aus:</span><span class="sxs-lookup"><span data-stu-id="215e5-211">Select one of the following options:</span></span>

    -   <span data-ttu-id="215e5-212">**Laden Sie die neuesten Definitionen herunter (empfohlen)** – das Definitionsupdate wird automatisch gestartet, und die Definitionen werden dem Dart-Wiederherstellungsbild hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="215e5-212">**Download the latest definitions (Recommended)** – The definition update starts automatically, and the definitions are added to the DaRT recovery image.</span></span> <span data-ttu-id="215e5-213">Diese Option wird empfohlen, damit Sie Fälle vermeiden können, in denen die Definitionen möglicherweise nicht verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="215e5-213">This option is recommended to help you avoid cases where the definitions might not be available.</span></span> <span data-ttu-id="215e5-214">Sie müssen mit dem Internet verbunden sein, um die Definitionen herunterladen zu können.</span><span class="sxs-lookup"><span data-stu-id="215e5-214">You must be connected to the Internet to download the definitions.</span></span>

    -   <span data-ttu-id="215e5-215">**Herunterladen der Definitionen später** – Definitionen werden nicht im Dart-Wiederherstellungsbild enthalten sein, und Sie müssen die Definitionen von dem Computer herunterladen, auf dem Dart ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="215e5-215">**Download the definitions later** – Definitions will not be included in the DaRT recovery image, and you will need to download the definitions from the computer that is running DaRT.</span></span>

        <span data-ttu-id="215e5-216">Wenn Sie sich entschließen, die neuesten Definitionen nicht in das Wiederherstellungsabbild aufzunehmen, oder wenn die Definitionen, die in dem Wiederherstellungsabbild enthalten sind, nicht mehr aktuell sind, wenn Sie Defender verwenden möchten, besorgen Sie sich die neuesten Definitionen, bevor Sie mit dem Scannen beginnen, indem Sie die Anweisungen befolgen, die in Defender bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="215e5-216">If you decide not to include the latest definitions on the recovery image, or if the definitions included on the recovery image are no longer current by the time that you are ready to use Defender, obtain the latest definitions before you begin a scan by following the instructions that are provided in Defender.</span></span>

        <span data-ttu-id="215e5-217">**Wichtig**  Sie können nicht überprüfen, ob keine Definitionen vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="215e5-217">**Important** You cannot scan if there are no definitions.</span></span>

         

3.  <span data-ttu-id="215e5-218">Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="215e5-218">Click **Next**.</span></span>

## <span data-ttu-id="215e5-219">Auswählen der zu erstellende Typen von Wiederherstellungsbild Dateien</span><span class="sxs-lookup"><span data-stu-id="215e5-219">Select the types of recovery image files to create</span></span>


<span data-ttu-id="215e5-220">Wählen Sie auf der Seite "Bild erstellen" einen Ausgabeordner für das Wiederherstellungsabbild aus, geben Sie einen Bildnamen ein, und wählen Sie die Typen von DART-Wiederherstellungsbild Dateien aus, die Sie erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="215e5-220">On the Create Image page, you choose an output folder for the recovery image, enter an image name, and select the types of DaRT recovery image files to create.</span></span> <span data-ttu-id="215e5-221">Während der Erstellung des Wiederherstellungsprozesses werden die Windows-Quelldateien entpackt, Dart-Dateien werden kopiert, und das Bild wird dann in die Dateiformate, die Sie auf dieser Seite ausgewählt haben, "neu verpackt".</span><span class="sxs-lookup"><span data-stu-id="215e5-221">During the recovery image creation process, Windows source files are unpacked, DaRT files are copied to it, and the image is then “re-packed” into the file formats that you select on this page.</span></span>

<span data-ttu-id="215e5-222">Die verfügbaren Bilddateitypen sind:</span><span class="sxs-lookup"><span data-stu-id="215e5-222">The available image file types are:</span></span>

-   <span data-ttu-id="215e5-223">**Windows Imaging-Datei (WIM)** – wird zum Bereitstellen von Dart in einer PXE-Umgebung (Preboot Execution Environment) oder einer lokalen Partition verwendet.</span><span class="sxs-lookup"><span data-stu-id="215e5-223">**Windows Imaging File (WIM)** - used to deploy DaRT to a preboot execution environment (PXE) or local partition).</span></span>

-   <span data-ttu-id="215e5-224">**ISO-Abbilddatei** – wird für die Bereitstellung auf CD oder DVD oder für die Verwendung in virtuellen Maschinen (VM) s) verwendet.</span><span class="sxs-lookup"><span data-stu-id="215e5-224">**ISO image file** – used to deploy to CD or DVD, or for use in virtual machines (VM)s).</span></span> <span data-ttu-id="215e5-225">Der Assistent setzt voraus, dass das ISO-Abbild eine ISO-Dateinamenerweiterung aufweist, da für die meisten Programme, die eine CD oder DVD brennen, diese Erweiterung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="215e5-225">The wizard requires that the ISO image have an .iso file name extension because most programs that burn a CD or DVD require that extension.</span></span> <span data-ttu-id="215e5-226">Wenn Sie keinen anderen Speicherort angeben, wird das ISO-Abbild auf dem Desktop mit dem Namen DaRT8. ISO erstellt.</span><span class="sxs-lookup"><span data-stu-id="215e5-226">If you do not specify a different location, the ISO image is created on your desktop with the name DaRT8.ISO.</span></span>

-   <span data-ttu-id="215e5-227">**PowerShell-Skript** – erstellt ein DART-Wiederherstellungsbild mit Befehlen, die im wesentlichen dieselben Optionen bieten, die Sie mithilfe des DART-Wiederherstellungsbild-Assistenten auswählen können.</span><span class="sxs-lookup"><span data-stu-id="215e5-227">**PowerShell script** – creates a DaRT recovery image with commands that provide essentially the same options that you can select by using the DaRT Recovery Image wizard.</span></span> <span data-ttu-id="215e5-228">Mit dem Skript können Sie auch Dateien im Dart-Wiederherstellungsbild hinzufügen oder ändern.</span><span class="sxs-lookup"><span data-stu-id="215e5-228">The script also enables you to add or changes files in the DaRT recovery image.</span></span>

<span data-ttu-id="215e5-229">Wenn Sie auf dieser Seite das Kontrollkästchen Bild bearbeiten aktivieren, können Sie das Wiederherstellungsbild während des Bild Erstellungsvorgangs anpassen.</span><span class="sxs-lookup"><span data-stu-id="215e5-229">If you select the Edit Image check box on this page, you can customize the recovery image during the image creation process.</span></span> <span data-ttu-id="215e5-230">So können Sie beispielsweise die Datei "winpeshl.ini" ändern, um eine benutzerdefinierte Startreihenfolge zu erstellen oder Tools von Drittanbietern hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="215e5-230">For example, you can change the “winpeshl.ini” file to create a custom startup order or to add third-party tools.</span></span>

**<span data-ttu-id="215e5-231">So wählen Sie die Typen von Wiederherstellungsbild Dateien aus, die erstellt werden sollen</span><span class="sxs-lookup"><span data-stu-id="215e5-231">To select the types of recovery image files to create</span></span>**

1.  <span data-ttu-id="215e5-232">Klicken Sie auf der Seite **Bild erstellen** auf **Durchsuchen** , um den Ausgabeordner für die Bilddatei auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="215e5-232">On the **Create Image** page, click **Browse** to choose the output folder for the image file.</span></span>

    <span data-ttu-id="215e5-233">**Hinweis**  Die Größe des Bilds hängt von den ausgewählten Tools und den Dateien ab, die Sie im Assistenten hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="215e5-233">**Note** The size of the image will vary, depending on the tools that you select and the files that you add in the wizard.</span></span>

     

2.  <span data-ttu-id="215e5-234">Geben Sie im Feld **Bildname** einen Namen für das DART-Wiederherstellungsbild ein, oder übernehmen Sie den Standardnamen DaRT8.</span><span class="sxs-lookup"><span data-stu-id="215e5-234">In the **Image name** box, enter a name for the DaRT recovery image, or accept the default name, which is DaRT8.</span></span>

    <span data-ttu-id="215e5-235">Der Assistent erstellt einen Unterordner im Ausgabepfad mit diesem Namen.</span><span class="sxs-lookup"><span data-stu-id="215e5-235">The wizard creates a subfolder in the output path by this name.</span></span>

3.  <span data-ttu-id="215e5-236">Wählen Sie die Typen von Bilddateien aus, die Sie erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="215e5-236">Select the types of image files that you want to create.</span></span>

4.  <span data-ttu-id="215e5-237">Wählen Sie eine der folgenden Optionen aus:</span><span class="sxs-lookup"><span data-stu-id="215e5-237">Choose one of the following:</span></span>

    -   <span data-ttu-id="215e5-238">Wenn Sie die Dateien im Wiederherstellungsabbild ändern möchten, bevor Sie die Bilddateien erstellen, aktivieren Sie das Kontrollkästchen **Bild bearbeiten** , und klicken Sie dann auf **vorbereiten**.</span><span class="sxs-lookup"><span data-stu-id="215e5-238">To change the files in the recovery image before you create the image files, select the **Edit Image** check box, and then click **Prepare**.</span></span>

    -   <span data-ttu-id="215e5-239">Wenn Sie das Wiederherstellungsabbild erstellen möchten, ohne die Dateien zu ändern, klicken Sie auf **Erstellen**.</span><span class="sxs-lookup"><span data-stu-id="215e5-239">To create the recovery image without changing the files, click **Create**.</span></span>

5.  

    <span data-ttu-id="215e5-240">Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="215e5-240">Click **Next**.</span></span>

## <span data-ttu-id="215e5-241">Bearbeiten der Wiederherstellungsbild Dateien</span><span class="sxs-lookup"><span data-stu-id="215e5-241">Edit the recovery image files</span></span>


<span data-ttu-id="215e5-242">Sie können das Wiederherstellungsbild nur bearbeiten, wenn Sie auf der Seite Bild erstellen das Kontrollkästchen Bild bearbeiten aktiviert haben.</span><span class="sxs-lookup"><span data-stu-id="215e5-242">You can edit the recovery image only if you selected the Edit Image check box on the Create Image page.</span></span> <span data-ttu-id="215e5-243">Nachdem das Wiederherstellungsabbild für die Bearbeitung vorbereitet wurde, können Sie die Wiederherstellungsabbild Dateien hinzufügen und ändern, bevor Sie das startfähige Medium erstellen.</span><span class="sxs-lookup"><span data-stu-id="215e5-243">After the recovery image has been prepared for editing, you can add and modify the recovery image files before creating the bootable media.</span></span> <span data-ttu-id="215e5-244">So können Sie beispielsweise eine benutzerdefinierte Reihenfolge für den Start erstellen, verschiedene Tools von Drittanbietern hinzufügen usw.</span><span class="sxs-lookup"><span data-stu-id="215e5-244">For example, you can create a custom order for startup, add various third-party tools, and so on.</span></span>

**<span data-ttu-id="215e5-245">So bearbeiten Sie die Wiederherstellungsbild Dateien</span><span class="sxs-lookup"><span data-stu-id="215e5-245">To edit the recovery image files</span></span>**

1.  <span data-ttu-id="215e5-246">Klicken Sie auf der Seite **Bild bearbeiten** auf in Windows-Explorer **Öffnen** .</span><span class="sxs-lookup"><span data-stu-id="215e5-246">On the **Edit Image** page, click **Open** in Windows Explorer.</span></span>

2.  <span data-ttu-id="215e5-247">Erstellen Sie einen Unterordner in dem Ordner, der im Dialogfeld aufgeführt ist.</span><span class="sxs-lookup"><span data-stu-id="215e5-247">Create a subfolder in the folder that is listed in the dialog box.</span></span>

3.  <span data-ttu-id="215e5-248">Kopieren Sie die gewünschten Dateien in den neuen Unterordner, oder entfernen Sie die Dateien, die Sie nicht benötigen.</span><span class="sxs-lookup"><span data-stu-id="215e5-248">Copy the files that you want to the new subfolder, or remove files that you don’t want.</span></span>

4.  <span data-ttu-id="215e5-249">Klicken Sie auf **Erstellen** , um die Erstellung des Wiederherstellungs Bilds zu starten.</span><span class="sxs-lookup"><span data-stu-id="215e5-249">Click **Create** to start creating the recovery image.</span></span>

## <span data-ttu-id="215e5-250">Generieren der Wiederherstellungsbild Dateien</span><span class="sxs-lookup"><span data-stu-id="215e5-250">Generate the recovery image files</span></span>


<span data-ttu-id="215e5-251">Auf der Seite "Dateien generieren" wird das DART-Wiederherstellungsbild für die Dateitypen generiert, die Sie auf der Seite "Bild erstellen" ausgewählt haben.</span><span class="sxs-lookup"><span data-stu-id="215e5-251">On the Generate Files page, the DaRT recovery image is generated for the file types that you selected on the Create Image page.</span></span>

**<span data-ttu-id="215e5-252">So generieren Sie die Wiederherstellungsbild Dateien</span><span class="sxs-lookup"><span data-stu-id="215e5-252">To generate the recovery image files</span></span>**

-   <span data-ttu-id="215e5-253">Klicken Sie auf der Seite **Dateien generieren** auf **weiter** , um die Wiederherstellungsabbild Dateien zu generieren.</span><span class="sxs-lookup"><span data-stu-id="215e5-253">On the **Generate Files** page, click **Next** to generate the recovery image files.</span></span>

## <span data-ttu-id="215e5-254">Kopieren des Wiederherstellungs Bilds auf eine CD, DVD oder USB</span><span class="sxs-lookup"><span data-stu-id="215e5-254">Copy the recovery image to a CD, DVD, or USB</span></span>


<span data-ttu-id="215e5-255">Auf der Seite startbare Medien erstellen können Sie die Bilddatei optional auf eine CD, DVD oder ein USB-Flashlaufwerk (USB-Stick) kopieren.</span><span class="sxs-lookup"><span data-stu-id="215e5-255">On the Create Bootable Media page, you can optionally copy the image file to a CD, DVD, or USB flash drive (UFD).</span></span> <span data-ttu-id="215e5-256">Sie können auf dieser Seite auch weitere startbare Medien erstellen, indem Sie den Assistenten erneut starten.</span><span class="sxs-lookup"><span data-stu-id="215e5-256">You can also create additional bootable media from this page by restarting the wizard.</span></span>

<span data-ttu-id="215e5-257">**Hinweis**  Die PXE-Installation (Preboot Execution Environment) und die Bereitstellung lokaler Bilder werden von diesem Tool nicht nativ unterstützt, da Sie zusätzliche Enterprise-Tools wie System Center Configuration Manager-Server und Microsoft Development Toolkit erfordern.</span><span class="sxs-lookup"><span data-stu-id="215e5-257">**Note** The Preboot execution environment (PXE) and local image deployment are not supported natively by this tool since they require additional enterprise tools, such as System Center Configuration Manager server and Microsoft Development Toolkit.</span></span>

 

**<span data-ttu-id="215e5-258">So kopieren Sie das Wiederherstellungsabbild auf eine CD, DVD oder USB</span><span class="sxs-lookup"><span data-stu-id="215e5-258">To copy the recovery image to a CD, DVD, or USB</span></span>**

1.  <span data-ttu-id="215e5-259">Wählen Sie auf der Seite startbare **Medien erstellen** die ISO-Datei aus, die Sie kopieren möchten.</span><span class="sxs-lookup"><span data-stu-id="215e5-259">On the **Create Bootable Media** page, select the iso file that you want to copy.</span></span>

2.  <span data-ttu-id="215e5-260">Legen Sie eine CD, DVD oder USB ein, und wählen Sie dann das Laufwerk aus.</span><span class="sxs-lookup"><span data-stu-id="215e5-260">Insert a CD, DVD, or USB, and then select the drive.</span></span>

    <span data-ttu-id="215e5-261">**Hinweis**  Wenn ein Laufwerk nicht erkannt wird und Sie ein neues Laufwerk installieren, können Sie auf **Aktualisieren** klicken, um den Assistenten zu zwingen, die Liste der verfügbaren Laufwerke zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="215e5-261">**Note** If a drive is not recognized and you install a new drive, you can click **Refresh** to force the wizard to update the list of available drives.</span></span>

     

3.  <span data-ttu-id="215e5-262">Klicken Sie auf die Schaltfläche **startfähige Medien erstellen** .</span><span class="sxs-lookup"><span data-stu-id="215e5-262">Click the **Create Bootable Media** button.</span></span>

4.  <span data-ttu-id="215e5-263">Wenn Sie ein weiteres Wiederherstellungsabbild erstellen möchten, klicken Sie auf neu starten, oder klicken Sie auf **Schließen** , wenn Sie mit dem Erstellen aller gewünschten Medien fertig sind.</span><span class="sxs-lookup"><span data-stu-id="215e5-263">To create another recovery image, click Restart, or click **Close** if you have finished creating all of the media that you want.</span></span>

## <span data-ttu-id="215e5-264">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="215e5-264">Related topics</span></span>


[<span data-ttu-id="215e5-265">Übersicht über die Tools in DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="215e5-265">Overview of the Tools in DaRT 8.0</span></span>](overview-of-the-tools-in-dart-80-dart-8.md)

[<span data-ttu-id="215e5-266">Bereitstellen von DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="215e5-266">Deploying DaRT 8.0</span></span>](deploying-dart-80-dart-8.md)

 

 





