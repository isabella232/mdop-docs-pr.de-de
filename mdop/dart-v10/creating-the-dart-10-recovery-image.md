---
title: Erstellen des DaRT 10-Wiederherstellungsabbilds
description: Erstellen des DaRT 10-Wiederherstellungsabbilds
author: dansimp
ms.assetid: 173556de-2f20-4ea6-9e29-fc5ccc71ebd7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: ebb48ee140a6e3f70e05acd3f6affc6e3b71ff37
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804805"
---
# <span data-ttu-id="4f91a-103">Erstellen des DaRT 10-Wiederherstellungsabbilds</span><span class="sxs-lookup"><span data-stu-id="4f91a-103">Creating the DaRT 10 Recovery Image</span></span>


<span data-ttu-id="4f91a-104">Nachdem Sie Microsoft Diagnostics and Recovery Toolset (Dart) 10 installiert haben, erstellen Sie ein DART 10-Wiederherstellungsabbild.</span><span class="sxs-lookup"><span data-stu-id="4f91a-104">After installing Microsoft Diagnostics and Recovery Toolset (DaRT) 10, you create a DaRT 10 recovery image.</span></span> <span data-ttu-id="4f91a-105">Das Wiederherstellungsabbild startet Windows RE, aus dem Sie dann die Dart-Tools starten können.</span><span class="sxs-lookup"><span data-stu-id="4f91a-105">The recovery image starts Windows RE, from which you can then start the DaRT tools.</span></span> <span data-ttu-id="4f91a-106">Sie können internationale Organisation für Standardisierungs Dateien (ISO) und Wim-Bilder (Windows Imaging Format) erstellen.</span><span class="sxs-lookup"><span data-stu-id="4f91a-106">You can generate International Organization for Standardization (ISO) files and Windows Imaging Format (WIM) images.</span></span> <span data-ttu-id="4f91a-107">Darüber hinaus können Sie mithilfe von PowerShell Skripts generieren, die die Einstellungen verwenden, die Sie im Dart-Wiederherstellungsbild-Assistenten ausgewählt haben.</span><span class="sxs-lookup"><span data-stu-id="4f91a-107">In addition, you can use PowerShell to generate scripts that use the settings you select in the DaRT Recovery Image wizard.</span></span> <span data-ttu-id="4f91a-108">Sie können das Skript später verwenden, um Wiederherstellungs Bilder mithilfe der gleichen Einstellungen wiederherzustellen.</span><span class="sxs-lookup"><span data-stu-id="4f91a-108">You can use the script later to rebuild recovery images by using the same settings.</span></span> <span data-ttu-id="4f91a-109">Das Wiederherstellungsabbild bietet eine Reihe von Wiederherstellungstools.</span><span class="sxs-lookup"><span data-stu-id="4f91a-109">The recovery image provides a variety of recovery tools.</span></span> <span data-ttu-id="4f91a-110">Eine Beschreibung der Tools finden Sie unter [Übersicht über die Tools in DART 10](overview-of-the-tools-in-dart-10.md).</span><span class="sxs-lookup"><span data-stu-id="4f91a-110">For a description of the tools, see [Overview of the Tools in DaRT 10](overview-of-the-tools-in-dart-10.md).</span></span>

<span data-ttu-id="4f91a-111">Nachdem Sie den Computer in DART gestartet haben, können Sie die verschiedenen Dart-Tools ausführen, um zu versuchen, den Computer zu diagnostizieren und zu reparieren.</span><span class="sxs-lookup"><span data-stu-id="4f91a-111">After you boot the computer into DaRT, you can run the different DaRT tools to try to diagnose and repair the computer.</span></span> <span data-ttu-id="4f91a-112">In diesem Abschnitt werden Sie durch den Vorgang zum Erstellen des DART-Wiederherstellungs Bilds geführt, in dem Sie die Tools und Features auswählen können, die Sie als Teil des Bilds einfügen möchten.</span><span class="sxs-lookup"><span data-stu-id="4f91a-112">This section walks you through the process of creating the DaRT recovery image and lets you select the tools and features that you want to include as part of the image.</span></span>

<span data-ttu-id="4f91a-113">Sie können das DART-Wiederherstellungsabbild mithilfe einer der beiden folgenden Methoden erstellen:</span><span class="sxs-lookup"><span data-stu-id="4f91a-113">You can create the DaRT recovery image by using either of two methods:</span></span>

-   <span data-ttu-id="4f91a-114">Verwenden Sie den Dart-Wiederherstellungsbild-Assistenten, der in einer Windows-Umgebung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4f91a-114">Use the DaRT Recovery Image wizard, which runs in a Windows environment.</span></span>

-   <span data-ttu-id="4f91a-115">Ändern Sie ein Beispiel-PowerShell-Skript mit den gewünschten Werten.</span><span class="sxs-lookup"><span data-stu-id="4f91a-115">Modify an example PowerShell script with the values you want.</span></span> <span data-ttu-id="4f91a-116">Weitere Informationen finden Sie unter [so wird es gemacht: Verwenden eines PowerShell-Skripts zum Erstellen des Wiederherstellungsabbilds](how-to-use-a-powershell-script-to-create-the-recovery-image-dart-10.md).</span><span class="sxs-lookup"><span data-stu-id="4f91a-116">For more information, see [How to Use a PowerShell Script to Create the Recovery Image](how-to-use-a-powershell-script-to-create-the-recovery-image-dart-10.md).</span></span>

<span data-ttu-id="4f91a-117">Sie können die ISO auf eine beschreibbare CD oder DVD schreiben, Sie auf einem USB-Stick speichern oder in einem Format speichern, das Sie zum Booten von DART von einer Remotepartition oder einer Wiederherstellungspartition verwenden können.</span><span class="sxs-lookup"><span data-stu-id="4f91a-117">You can write the ISO to a recordable CD or DVD, save it to a USB flash drive, or save it in a format that you can use to boot into DaRT from a remote partition or from a recovery partition.</span></span>

<span data-ttu-id="4f91a-118">Nachdem Sie das ISO-Abbild erstellt haben, können Sie es auf eine leere CD oder DVD brennen (wenn Ihr Computer über ein CD-oder DVD-Laufwerk verfügt).</span><span class="sxs-lookup"><span data-stu-id="4f91a-118">Once you have created the ISO image, you can burn it onto a blank CD or DVD (if your computer has a CD or DVD drive).</span></span> <span data-ttu-id="4f91a-119">Wenn Ihr Computer nicht über ein Laufwerk für diesen Zweck verfügt, können Sie die meisten generischen Programme verwenden, mit denen CDs oder DVDs gebrannt werden.</span><span class="sxs-lookup"><span data-stu-id="4f91a-119">If your computer does not have a drive for this purpose, you can use most generic programs that are used to burn CDs or DVDs.</span></span>

## <span data-ttu-id="4f91a-120">Auswählen der Bildarchitektur und angeben des Pfads</span><span class="sxs-lookup"><span data-stu-id="4f91a-120">Select the image architecture and specify the path</span></span>


<span data-ttu-id="4f91a-121">Auf der Windows 10-Medienseite wählen Sie aus, ob Sie ein 32-Bit-oder 64-Bit-Dart-Wiederherstellungsbild erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="4f91a-121">On the Windows 10 Media page, you select whether to create a 32-bit or 64-bit DaRT recovery image.</span></span> <span data-ttu-id="4f91a-122">Verwenden Sie das 32-Bit-Fenster zum Erstellen von 32-Bit-Dart-Wiederherstellungs Bildern und 64-Bit-Windows zum Erstellen von 64-Bit-Dart-Wiederherstellungs Bildern.</span><span class="sxs-lookup"><span data-stu-id="4f91a-122">Use the 32-bit Windows to build 32-bit DaRT recovery images, and 64-bit Windows to build 64-bit DaRT recovery images.</span></span> <span data-ttu-id="4f91a-123">Sie können einen einzelnen Computer verwenden, um Wiederherstellungs Bilder für beide Architekturtypen zu erstellen, Sie können jedoch kein einzelnes Bild erstellen, das sowohl auf 32-Bit-als auch auf 64-Bit-Architekturen funktioniert.</span><span class="sxs-lookup"><span data-stu-id="4f91a-123">You can use a single computer to create recovery images for both architecture types, but you cannot create one image that works on both 32-bit and 64-bit architectures.</span></span> <span data-ttu-id="4f91a-124">Außerdem geben Sie den Pfad der Windows 10-Installationsmedien an.</span><span class="sxs-lookup"><span data-stu-id="4f91a-124">You also indicate the path of the Windows 10 installation media.</span></span> <span data-ttu-id="4f91a-125">Wählen Sie die Architektur aus, die dem von Ihnen erstellten Wiederherstellungsbild entspricht.</span><span class="sxs-lookup"><span data-stu-id="4f91a-125">Choose the architecture that matches the one of the recovery image that you are creating.</span></span>

**<span data-ttu-id="4f91a-126">So wählen Sie die Bildarchitektur aus und geben den Pfad an</span><span class="sxs-lookup"><span data-stu-id="4f91a-126">To select the image architecture and specify the path</span></span>**

1.  <span data-ttu-id="4f91a-127">Wählen Sie auf der **Windows 10-Medien** Seite eine der folgenden Optionen aus:</span><span class="sxs-lookup"><span data-stu-id="4f91a-127">On the **Windows 10 Media** page, select one of the following:</span></span>

    -   <span data-ttu-id="4f91a-128">Wenn Sie ein Wiederherstellungsabbild für 64-Bit-Computer erstellen, wählen Sie **x64-(64-Bit-) Dart-Bild erstellen**aus.</span><span class="sxs-lookup"><span data-stu-id="4f91a-128">If you are creating a recovery image for 64-bit computers, select **Create x64 (64-bit) DaRT image**.</span></span>

    -   <span data-ttu-id="4f91a-129">Wenn Sie ein Wiederherstellungsabbild für 32-Bit-Computer erstellen, wählen Sie **x86 (32-Bit) Dart-Bild erstellen**aus.</span><span class="sxs-lookup"><span data-stu-id="4f91a-129">If you are creating a recovery image for 32-bit computers, select **Create x86 (32-bit) DaRT image**.</span></span>

2.  <span data-ttu-id="4f91a-130">Geben Sie im Feld **Geben Sie den Stammpfad des Windows 10 &lt; -64-Bit-oder 32-Bit- &gt; Installationsmediums** an den Pfad der Windows 10-Installationsdateien ein.</span><span class="sxs-lookup"><span data-stu-id="4f91a-130">In the **Specify the root path of the Windows 10 &lt;64-bit or 32-bit&gt; install media** box, type the path of the Windows 10 installation files.</span></span> <span data-ttu-id="4f91a-131">Verwenden Sie einen Pfad, der der Architektur des Wiederherstellungs Bilds entspricht, das Sie erstellen.</span><span class="sxs-lookup"><span data-stu-id="4f91a-131">Use a path that matches the architecture of the recovery image that you are creating.</span></span>

3.  <span data-ttu-id="4f91a-132">Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="4f91a-132">Click **Next**.</span></span>

## <span data-ttu-id="4f91a-133">Auswählen der Tools, die in das Wiederherstellungsabbild aufgenommen werden sollen</span><span class="sxs-lookup"><span data-stu-id="4f91a-133">Select the tools to include on the recovery image</span></span>


<span data-ttu-id="4f91a-134">Auf der Seite Extras können Sie zahlreiche Tools auswählen, die in das Wiederherstellungsabbild aufgenommen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="4f91a-134">On the Tools page, you can select numerous tools to include on the recovery image.</span></span> <span data-ttu-id="4f91a-135">Diese Tools stehen Endbenutzern zur Verfügung, wenn Sie in das DART-Bild Booten.</span><span class="sxs-lookup"><span data-stu-id="4f91a-135">These tools will be available to end users when they boot into the DaRT image.</span></span> <span data-ttu-id="4f91a-136">Wenn Sie jedoch beim Erstellen des DART-Bilds die Remotekonnektivität aktivieren, stehen alle Tools zur Verfügung, wenn ein Mitarbeiter des Helpdesks eine Verbindung mit dem Computer des Endbenutzers herstellt, unabhängig davon, welche Tools Sie in das Bild aufgenommen haben.</span><span class="sxs-lookup"><span data-stu-id="4f91a-136">However, if you enable remote connectivity when creating the DaRT image, all of the tools will be available when a help desk worker connects to the end user’s computer, regardless of which tools you chose to include on the image.</span></span>

<span data-ttu-id="4f91a-137">Wenn Sie den Endbenutzer Zugriff auf diese Tools einschränken, aber weiterhin den vollständigen Zugriff auf die Tools über die Remote Verbindungsanzeige behalten möchten, wählen Sie diese Tools auf der Seite Tools nicht aus.</span><span class="sxs-lookup"><span data-stu-id="4f91a-137">To restrict end-user access to these tools, but still retain full access to the tools through the Remote Connection Viewer, do not select those tools on the Tools page.</span></span> <span data-ttu-id="4f91a-138">Endbenutzer können nur die Remote Verbindung verwenden und können alle Tools, die Sie aus dem Wiederherstellungsabbild ausschließen, sehen, aber nicht darauf zugreifen.</span><span class="sxs-lookup"><span data-stu-id="4f91a-138">End users will be able to use only Remote Connection and will be able to see, but not access, any tools that you exclude from the recovery image.</span></span>

**<span data-ttu-id="4f91a-139">So wählen Sie die Tools aus, die Sie in das Wiederherstellungsabbild einbeziehen möchten</span><span class="sxs-lookup"><span data-stu-id="4f91a-139">To select the tools to include on the recovery image</span></span>**

1.  <span data-ttu-id="4f91a-140">Aktivieren Sie auf der Seite **Extras** das Kontrollkästchen neben jedem Tool, das Sie in das Bild einbeziehen möchten.</span><span class="sxs-lookup"><span data-stu-id="4f91a-140">On the **Tools** page, select the check box beside each tool that you want to include on the image.</span></span>

2.  <span data-ttu-id="4f91a-141">Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="4f91a-141">Click **Next**.</span></span>

## <span data-ttu-id="4f91a-142">Auswählen, ob die Remotekonnektivität von einem Helpdesk zugelassen werden soll</span><span class="sxs-lookup"><span data-stu-id="4f91a-142">Choose whether to allow remote connectivity by a help desk</span></span>


<span data-ttu-id="4f91a-143">Auf der Seite Remote Verbindung können Sie festlegen, dass ein Helpdesk-Mitarbeiter eine Remoteverbindung herstellen und die Dart-Tools auf dem Computer eines Endbenutzers ausführen soll.</span><span class="sxs-lookup"><span data-stu-id="4f91a-143">On the Remote Connection page, you can choose to enable a help desk worker to remotely connect to and run the DaRT tools on an end user’s computer.</span></span> <span data-ttu-id="4f91a-144">Die Option Remotekonnektivität wird dann im Fenster Diagnose-und Wiederherstellungs-Toolset als verfügbare Option angezeigt.</span><span class="sxs-lookup"><span data-stu-id="4f91a-144">The remote connectivity option is then shown as an available option in the Diagnostics and Recovery Toolset window.</span></span> <span data-ttu-id="4f91a-145">Nachdem die Helpdesk-Mitarbeiter eine Remoteverbindung hergestellt haben, können Sie die Dart-Tools auf dem Endbenutzercomputer von einem Remotestandort aus ausführen.</span><span class="sxs-lookup"><span data-stu-id="4f91a-145">After help desk workers establish a remote connection, they can run the DaRT tools on the end-user computer from a remote location.</span></span>

**<span data-ttu-id="4f91a-146">So wählen Sie aus, ob die Remotekonnektivität von Helpdesk-Mitarbeitern zugelassen werden soll</span><span class="sxs-lookup"><span data-stu-id="4f91a-146">To choose whether to allow remote connectivity by help desk workers</span></span>**

1.  <span data-ttu-id="4f91a-147">Aktivieren Sie auf der Seite **Remoteverbindung** das Kontrollkästchen **Remoteverbindungen zulassen** , um Remoteverbindungen zuzulassen, oder deaktivieren Sie das Kontrollkästchen, um Remoteverbindungen zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="4f91a-147">On the **Remote Connection** page, select the **Allow remote connections** check box to allow remote connections, or clear the check box to prevent remote connections.</span></span>

2.  <span data-ttu-id="4f91a-148">Wenn Sie das Kontrollkästchen **Remoteverbindungen zulassen** deaktiviert haben, klicken Sie auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="4f91a-148">If you cleared the **Allow remote connections** check box, click **Next**.</span></span> <span data-ttu-id="4f91a-149">Fahren Sie andernfalls mit dem nächsten Schritt fort, um die Konfiguration der Remotekonnektivität fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="4f91a-149">Otherwise, go to the next step to continue configuring remote connectivity.</span></span>

3.  <span data-ttu-id="4f91a-150">Wählen Sie eine der folgenden Optionen:</span><span class="sxs-lookup"><span data-stu-id="4f91a-150">Select one of the following:</span></span>

    -   <span data-ttu-id="4f91a-151">Lassen Sie Windows eine offene Portnummer auswählen.</span><span class="sxs-lookup"><span data-stu-id="4f91a-151">Let Windows choose an open port number.</span></span>

    -   <span data-ttu-id="4f91a-152">Geben Sie die Portnummer an.</span><span class="sxs-lookup"><span data-stu-id="4f91a-152">Specify the port number.</span></span> <span data-ttu-id="4f91a-153">Wenn Sie diese Option auswählen, geben Sie eine Portnummer zwischen 1 und 65535 in das Feld unterhalb der Option ein.</span><span class="sxs-lookup"><span data-stu-id="4f91a-153">If you select this option, enter a port number between 1 and 65535 in the field beneath the option.</span></span> <span data-ttu-id="4f91a-154">Diese Portnummer wird beim Einrichten einer Remoteverbindung verwendet.</span><span class="sxs-lookup"><span data-stu-id="4f91a-154">This port number will be used when establishing a remote connection.</span></span> <span data-ttu-id="4f91a-155">Wir empfehlen, dass die Portnummer 1024 oder höher ist, um die Möglichkeit eines Konflikts zu minimieren.</span><span class="sxs-lookup"><span data-stu-id="4f91a-155">We recommend that the port number be 1024 or higher to minimize the possibility of a conflict.</span></span>

4.  <span data-ttu-id="4f91a-156">(Optional) erstellen Sie im Dialogfeld "Willkommensnachricht für **Remoteverbindung** " eine benutzerdefinierte Nachricht, die Endbenutzer erhalten, wenn Sie eine Remoteverbindung herstellen.</span><span class="sxs-lookup"><span data-stu-id="4f91a-156">(Optional) in the **Remote connection welcome** message box, create a customized message that end users receive when they establish a remote connection.</span></span> <span data-ttu-id="4f91a-157">Die Nachricht kann maximal 2048 Zeichen umfassen.</span><span class="sxs-lookup"><span data-stu-id="4f91a-157">The message can be a maximum of 2048 characters.</span></span>

5.  <span data-ttu-id="4f91a-158">Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="4f91a-158">Click **Next**.</span></span>

    <span data-ttu-id="4f91a-159">Weitere Informationen dazu, wie Sie die Dart-Tools Remote ausführen können, finden Sie unter [Wiederherstellen von Remotecomputern mithilfe des DART-Wiederherstellungs Bilds](how-to-recover-remote-computers-by-using-the-dart-recovery-image-dart-10.md).</span><span class="sxs-lookup"><span data-stu-id="4f91a-159">For more information about running the DaRT tools remotely, see [How to Recover Remote Computers by Using the DaRT Recovery Image](how-to-recover-remote-computers-by-using-the-dart-recovery-image-dart-10.md).</span></span>

## <span data-ttu-id="4f91a-160">Hinzufügen von Treibern zum Wiederherstellungsabbild</span><span class="sxs-lookup"><span data-stu-id="4f91a-160">Add drivers to the recovery image</span></span>


<span data-ttu-id="4f91a-161">Auf der Registerkarte "Treiber" auf der Seite "Erweiterte Optionen" können Sie zusätzliche Gerätetreiber hinzufügen, die Sie möglicherweise benötigen, wenn Sie einen Computer reparieren.</span><span class="sxs-lookup"><span data-stu-id="4f91a-161">On the Drivers tab of the Advanced Options page, you can add additional device drivers that you may need when repairing a computer.</span></span> <span data-ttu-id="4f91a-162">Diese können in der Regelspeicher-oder Netzwerk Controller enthalten, die von Windows 10 nicht bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="4f91a-162">These may typically include storage or network controllers that Windows 10 does not provide.</span></span> <span data-ttu-id="4f91a-163">Treiber werden installiert, wenn das Bild erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="4f91a-163">Drivers are installed when the image is created.</span></span>

<span data-ttu-id="4f91a-164">**Wichtig**  Beachten Sie bei der Auswahl der zu berücksichtigenden Treiber, dass drahtlose Verbindungen (wie Bluetooth oder 802.11 a/b/g/n) in DART nicht unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="4f91a-164">**Important** When you select drivers to include, be aware that wireless connectivity (such as Bluetooth or 802.11a/b/g/n) is not supported in DaRT.</span></span>

 

**<span data-ttu-id="4f91a-165">So fügen Sie dem Wiederherstellungsabbild Treiber hinzu</span><span class="sxs-lookup"><span data-stu-id="4f91a-165">To add drivers to the recovery image</span></span>**

1.  <span data-ttu-id="4f91a-166">Klicken Sie auf der Seite **Erweiterte Optionen** auf die Registerkarte **Treiber** .</span><span class="sxs-lookup"><span data-stu-id="4f91a-166">On the **Advanced Options** page, click the **Drivers** tab.</span></span>

2.  <span data-ttu-id="4f91a-167">Klicken Sie auf **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="4f91a-167">Click **Add**.</span></span>

3.  <span data-ttu-id="4f91a-168">Navigieren Sie zu der Datei, die für den Treiber hinzugefügt werden soll, und klicken Sie dann auf **Öffnen**.</span><span class="sxs-lookup"><span data-stu-id="4f91a-168">Browse to the file to be added for the driver, and then click **Open**.</span></span>

    <span data-ttu-id="4f91a-169">**Hinweis**  Die Treiberdatei wird vom Hersteller des Speichers oder des Netzwerkcontrollers bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="4f91a-169">**Note** The driver file is provided by the manufacturer of the storage or network controller.</span></span>

     

4.  <span data-ttu-id="4f91a-170">Wiederholen Sie die Schritte 2 und 3 für jeden Treiber, den Sie einbeziehen möchten.</span><span class="sxs-lookup"><span data-stu-id="4f91a-170">Repeat Steps 2 and 3 for every driver that you want to include.</span></span>

5.  <span data-ttu-id="4f91a-171">Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="4f91a-171">Click **Next**.</span></span>

## <span data-ttu-id="4f91a-172">Hinzufügen von optionalen WinPE-Paketen zum Wiederherstellungsabbild</span><span class="sxs-lookup"><span data-stu-id="4f91a-172">Add WinPE optional packages to the recovery image</span></span>


<span data-ttu-id="4f91a-173">Auf der Registerkarte "WinPE" auf der Seite "Erweiterte Optionen" können Sie dem Dart-Bild optionale WinPE-Pakete hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="4f91a-173">On the WinPE tab of the Advanced Options page, you can add WinPE optional packages to the DaRT image.</span></span> <span data-ttu-id="4f91a-174">Diese Pakete sind Teil des Windows ADK, das eine Installationsvoraussetzung für den Dart-Wiederherstellungsbild-Assistenten ist.</span><span class="sxs-lookup"><span data-stu-id="4f91a-174">These packages are part of the Windows ADK, which is an installation prerequisite for the DaRT Recovery Image wizard.</span></span> <span data-ttu-id="4f91a-175">Die Tools, die Sie auswählen können, sind alle optional.</span><span class="sxs-lookup"><span data-stu-id="4f91a-175">The tools that you can select are all optional.</span></span> <span data-ttu-id="4f91a-176">Alle erforderlichen Pakete werden automatisch basierend auf den Tools hinzugefügt, die Sie auf der Seite "Tools" ausgewählt haben.</span><span class="sxs-lookup"><span data-stu-id="4f91a-176">Any required packages are added automatically, based on the tools you selected on the Tools page.</span></span>

<span data-ttu-id="4f91a-177">Sie können auch die Größe des Scratch-Space angeben.</span><span class="sxs-lookup"><span data-stu-id="4f91a-177">You can also specify the size of the scratch space.</span></span> <span data-ttu-id="4f91a-178">Scratch-Speicherplatz ist die Größe des RAM-Speicherplatzes, der für die Ausführung von DART reserviert ist.</span><span class="sxs-lookup"><span data-stu-id="4f91a-178">Scratch space is the amount of RAM disk space that is set aside for DaRT to run.</span></span> <span data-ttu-id="4f91a-179">Der Scratch-Bereich ist nützlich, wenn die Festplatte des Endbenutzers nicht verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="4f91a-179">The scratch space is useful in case the end user’s hard disk is not available.</span></span> <span data-ttu-id="4f91a-180">Wenn Sie zusätzliche Tools und Treiber ausführen, möchten Sie möglicherweise den Scratch-Platz erhöhen.</span><span class="sxs-lookup"><span data-stu-id="4f91a-180">If you are running additional tools and drivers, you may want to increase the scratch space.</span></span>

**<span data-ttu-id="4f91a-181">So fügen Sie dem Wiederherstellungsabbild optionale WinPE-Pakete hinzu</span><span class="sxs-lookup"><span data-stu-id="4f91a-181">To add WinPE optional packages to the recovery image</span></span>**

1.  <span data-ttu-id="4f91a-182">Klicken Sie auf der Seite **Erweiterte Optionen** auf die Registerkarte **WinPE** .</span><span class="sxs-lookup"><span data-stu-id="4f91a-182">On the **Advanced Options** page, click the **WinPE** tab.</span></span>

2.  <span data-ttu-id="4f91a-183">Aktivieren Sie das Kontrollkästchen neben jedem Paket, das Sie in das Bild einbeziehen möchten, oder klicken Sie auf das Kontrollkästchen **Name** , um alle Pakete auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="4f91a-183">Select the check box beside each package that you want to include on the image, or click the **Name** check box to select all of the packages.</span></span>

3.  <span data-ttu-id="4f91a-184">Wählen Sie im Feld **Scratch Space** den RAM-Speicherplatz aus, der für die Ausführung von DART reserviert werden soll, falls die Festplatte des Endbenutzers nicht verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="4f91a-184">In the **Scratch Space** field, select the amount of RAM disk space to allocate for running DaRT in case the end user’s hard disk is not available.</span></span>

4.  <span data-ttu-id="4f91a-185">Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="4f91a-185">Click **Next**.</span></span>

## <span data-ttu-id="4f91a-186">Hinzufügen der Debugging-Tools für Crash Analyzer</span><span class="sxs-lookup"><span data-stu-id="4f91a-186">Add the debugging tools for Crash Analyzer</span></span>


<span data-ttu-id="4f91a-187">Wenn Sie das Tool Absturzanalyse in das ISO-Abbild einbeziehen, müssen Sie auch die Debugging-Tools für Windows einbeziehen.</span><span class="sxs-lookup"><span data-stu-id="4f91a-187">If you include the Crash Analyzer tool in the ISO image, you must also include the Debugging Tools for Windows.</span></span> <span data-ttu-id="4f91a-188">Auf der Seite "Erweiterte Optionen" auf der Registerkarte Crash Analyzer geben Sie den Pfad der Windows 10-Debugging-Tools ein, die von Crash Analyzer zum Analysieren von Speicherabbilddateien verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4f91a-188">On the Crash Analyzer tab of the Advanced Options page, you enter the path of the Windows 10 Debugging Tools, which Crash Analyzer uses to analyze memory dump files.</span></span> <span data-ttu-id="4f91a-189">Sie können die Tools verwenden, die sich auf dem Computer befinden, auf dem Sie den Dart-Wiederherstellungsbild-Assistenten ausführen, oder Sie können die Tools verwenden, die sich auf dem Computer des Endbenutzers befinden.</span><span class="sxs-lookup"><span data-stu-id="4f91a-189">You can use the tools that are on the computer where you are running the DaRT Recovery Image wizard, or you can use the tools that are on the end-user computer.</span></span> <span data-ttu-id="4f91a-190">Wenn Sie die Tools auf dem Endbenutzercomputer verwenden möchten, denken Sie daran, dass auf jedem Computer, den Sie diagnostizieren, die Debug-Tools installiert sein müssen.</span><span class="sxs-lookup"><span data-stu-id="4f91a-190">If you decide to use the tools on the end-user computer, remember that every computer that you diagnose must have the Debugging Tools installed.</span></span>

<span data-ttu-id="4f91a-191">Wenn Sie das Microsoft Windows Software Development Kit (SDK) oder das Microsoft Windows Development Kit (WDK) installiert haben, werden die Windows 10-Debugging-Tools standardmäßig zum Wiederherstellungsbild hinzugefügt, und der Pfad zu den Debugging-Tools wird automatisch ausgefüllt.</span><span class="sxs-lookup"><span data-stu-id="4f91a-191">If you installed the Microsoft Windows Software Development Kit (SDK) or the Microsoft Windows Development Kit (WDK), the Windows 10 Debugging Tools are added to the recovery image by default, and the path to the Debugging Tools is automatically filled in.</span></span> <span data-ttu-id="4f91a-192">Sie können den Pfad der Windows 10-Debugging-Tools ändern, wenn sich die Dateien an einem anderen Ort als dem durch den Standard Dateipfad angegebenen Speicherort befinden.</span><span class="sxs-lookup"><span data-stu-id="4f91a-192">You can change the path of the Windows 10 Debugging Tools if the files are located somewhere other than the location indicated by the default file path.</span></span> <span data-ttu-id="4f91a-193">Mit einem Link im Assistenten können Sie Debugging-Tools für Windows herunterladen und installieren, wenn diese noch nicht installiert sind.</span><span class="sxs-lookup"><span data-stu-id="4f91a-193">A link in the wizard lets you download and install debugging tools for Windows if they are not already installed.</span></span>

<span data-ttu-id="4f91a-194">Informationen zum Herunterladen der Windows-Debugging-Tools finden Sie unter [Debuggen von Tools für Windows](https://go.microsoft.com/fwlink/?LinkId=266248).</span><span class="sxs-lookup"><span data-stu-id="4f91a-194">To download the Windows Debugging Tools, see [Debugging Tools for Windows](https://go.microsoft.com/fwlink/?LinkId=266248).</span></span> <span data-ttu-id="4f91a-195">Installieren Sie die Debug-Tools am Standardspeicherort.</span><span class="sxs-lookup"><span data-stu-id="4f91a-195">Install the Debugging Tools to the default location.</span></span>

<span data-ttu-id="4f91a-196">**Hinweis**  Der Dart-Assistent überprüft die Tools im `HKLM\Software\Microsoft\Windows Kits\Installed Roots\WindowsDebuggersRoot` Registrierungsschlüssel.</span><span class="sxs-lookup"><span data-stu-id="4f91a-196">**Note** The DaRT wizard checks for the tools in the `HKLM\Software\Microsoft\Windows Kits\Installed Roots\WindowsDebuggersRoot` registry key.</span></span> <span data-ttu-id="4f91a-197">Wenn der Registrierungswert nicht vorhanden ist, sucht der Assistent je nach ihrer Systemarchitektur an einem der folgenden Speicherorte:</span><span class="sxs-lookup"><span data-stu-id="4f91a-197">If the registry value is not there, the wizard looks in one of the following locations, depending on your system architecture:</span></span>

`%ProgramFilesX86%\Windows Kits\10.0\Debuggers\x64`

`%ProgramFilesX86%\Windows Kits\10.0\Debuggers\x86`

 

**<span data-ttu-id="4f91a-198">So fügen Sie die Debugging-Tools für Crash Analyzer hinzu</span><span class="sxs-lookup"><span data-stu-id="4f91a-198">To add the debugging tools for Crash Analyzer</span></span>**

1.  <span data-ttu-id="4f91a-199">Klicken Sie auf der Seite **Erweiterte Optionen** auf die Registerkarte **Crash Analyzer** .</span><span class="sxs-lookup"><span data-stu-id="4f91a-199">On the **Advanced Options** page, click the **Crash Analyzer** tab.</span></span>

2.  <span data-ttu-id="4f91a-200">Optional Klicken Sie auf **Debug-Tools herunterladen** , um die Debugging-Tools für Windows herunterzuladen.</span><span class="sxs-lookup"><span data-stu-id="4f91a-200">(Optional) Click **Download the Debugging Tools** to download the Debugging Tools for Windows.</span></span>

3.  <span data-ttu-id="4f91a-201">Wählen Sie eine der folgenden Optionen aus:</span><span class="sxs-lookup"><span data-stu-id="4f91a-201">Select one of the following options:</span></span>

    -   <span data-ttu-id="4f91a-202">**Schließen Sie die Windows 10- &lt; &gt; Debug-Tools 64-Bit oder 32 ein**.</span><span class="sxs-lookup"><span data-stu-id="4f91a-202">**Include the Windows 10 &lt;64-bit or 32-bit&gt; Debugging Tools**.</span></span> <span data-ttu-id="4f91a-203">Wenn Sie diese Option auswählen, navigieren Sie zu dem Speicherort der Tools, und wählen Sie ihn aus, wenn der Pfad noch nicht angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="4f91a-203">If you select this option, browse to and select the location of the tools if the path is not already displaying.</span></span>

    -   <span data-ttu-id="4f91a-204">**Verwenden Sie die Debugging-Tools des Systems, das gedebuggt wird**.</span><span class="sxs-lookup"><span data-stu-id="4f91a-204">**Use the Debugging Tools from the system that is being debugged**.</span></span> <span data-ttu-id="4f91a-205">Wenn Sie diese Option auswählen, funktioniert der Absturzanalyse Programm nicht, wenn die Debugging-Tools für Windows auf dem Problem Computer nicht gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="4f91a-205">If you select this option, the Crash Analyzer will not work if the Debugging Tools for Windows are not found on the problem computer.</span></span>

4.  <span data-ttu-id="4f91a-206">Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="4f91a-206">Click **Next**.</span></span>

## <span data-ttu-id="4f91a-207">Auswählen der zu erstellende Typen von Wiederherstellungsbild Dateien</span><span class="sxs-lookup"><span data-stu-id="4f91a-207">Select the types of recovery image files to create</span></span>


<span data-ttu-id="4f91a-208">Wählen Sie auf der Seite "Bild erstellen" einen Ausgabeordner für das Wiederherstellungsabbild aus, geben Sie einen Bildnamen ein, und wählen Sie die Typen von DART-Wiederherstellungsbild Dateien aus, die Sie erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="4f91a-208">On the Create Image page, you choose an output folder for the recovery image, enter an image name, and select the types of DaRT recovery image files to create.</span></span> <span data-ttu-id="4f91a-209">Während der Erstellung des Wiederherstellungsprozesses werden die Windows-Quelldateien entpackt, Dart-Dateien werden kopiert, und das Bild wird dann in die Dateiformate, die Sie auf dieser Seite ausgewählt haben, "neu verpackt".</span><span class="sxs-lookup"><span data-stu-id="4f91a-209">During the recovery image creation process, Windows source files are unpacked, DaRT files are copied to it, and the image is then “re-packed” into the file formats that you select on this page.</span></span>

<span data-ttu-id="4f91a-210">Die verfügbaren Bilddateitypen sind:</span><span class="sxs-lookup"><span data-stu-id="4f91a-210">The available image file types are:</span></span>

-   <span data-ttu-id="4f91a-211">**Windows Imaging-Datei (WIM)** – wird zum Bereitstellen von Dart in einer PXE-Umgebung (Preboot Execution Environment) oder einer lokalen Partition verwendet.</span><span class="sxs-lookup"><span data-stu-id="4f91a-211">**Windows Imaging File (WIM)** - used to deploy DaRT to a preboot execution environment (PXE) or local partition).</span></span>

-   <span data-ttu-id="4f91a-212">**International Standards Organization (ISO)** – wird für die Bereitstellung auf einer CD oder DVD oder für die Verwendung in virtuellen Maschinen (VM) s) verwendet.</span><span class="sxs-lookup"><span data-stu-id="4f91a-212">**International Standards Organization (ISO)** – used to deploy to CD or DVD, or for use in virtual machines (VM)s).</span></span> <span data-ttu-id="4f91a-213">Der Assistent setzt voraus, dass das ISO-Abbild eine ISO-Dateinamenerweiterung aufweist, da für die meisten Programme, die eine CD oder DVD brennen, diese Erweiterung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="4f91a-213">The wizard requires that the ISO image have an .iso file name extension because most programs that burn a CD or DVD require that extension.</span></span> <span data-ttu-id="4f91a-214">Wenn Sie keinen anderen Speicherort angeben, wird das ISO-Abbild auf dem Desktop mit dem Namen DaRT10. ISO erstellt.</span><span class="sxs-lookup"><span data-stu-id="4f91a-214">If you do not specify a different location, the ISO image is created on your desktop with the name DaRT10.ISO.</span></span>

-   <span data-ttu-id="4f91a-215">**PowerShell-Skript** – erstellt ein DART-Wiederherstellungsbild mit Befehlen, die im wesentlichen dieselben Optionen bieten, die Sie mithilfe des DART-Wiederherstellungsbild-Assistenten auswählen können.</span><span class="sxs-lookup"><span data-stu-id="4f91a-215">**PowerShell script** – creates a DaRT recovery image with commands that provide essentially the same options that you can select by using the DaRT Recovery Image wizard.</span></span> <span data-ttu-id="4f91a-216">Mit dem Skript können Sie auch Dateien im Dart-Wiederherstellungsbild hinzufügen oder ändern.</span><span class="sxs-lookup"><span data-stu-id="4f91a-216">The script also enables you to add or changes files in the DaRT recovery image.</span></span>

<span data-ttu-id="4f91a-217">Wenn Sie auf dieser Seite das Kontrollkästchen Bild bearbeiten aktivieren, können Sie das Wiederherstellungsbild während des Bild Erstellungsvorgangs anpassen.</span><span class="sxs-lookup"><span data-stu-id="4f91a-217">If you select the Edit Image check box on this page, you can customize the recovery image during the image creation process.</span></span> <span data-ttu-id="4f91a-218">So können Sie beispielsweise die Datei "winpeshl.ini" ändern, um eine benutzerdefinierte Startreihenfolge zu erstellen oder Tools von Drittanbietern hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="4f91a-218">For example, you can change the “winpeshl.ini” file to create a custom startup order or to add third-party tools.</span></span>

**<span data-ttu-id="4f91a-219">So wählen Sie die Typen von Wiederherstellungsbild Dateien aus, die erstellt werden sollen</span><span class="sxs-lookup"><span data-stu-id="4f91a-219">To select the types of recovery image files to create</span></span>**

1.  <span data-ttu-id="4f91a-220">Klicken Sie auf der Seite **Bild erstellen** auf **Durchsuchen** , um den Ausgabeordner für die Bilddatei auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="4f91a-220">On the **Create Image** page, click **Browse** to choose the output folder for the image file.</span></span>

    <span data-ttu-id="4f91a-221">**Hinweis**  Die Größe des Bilds hängt von den ausgewählten Tools und den Dateien ab, die Sie im Assistenten hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="4f91a-221">**Note** The size of the image will vary, depending on the tools that you select and the files that you add in the wizard.</span></span>

     

2.  <span data-ttu-id="4f91a-222">Geben Sie im Feld **Bildname** einen Namen für das DART-Wiederherstellungsbild ein, oder übernehmen Sie den Standardnamen DaRT10.</span><span class="sxs-lookup"><span data-stu-id="4f91a-222">In the **Image name** box, enter a name for the DaRT recovery image, or accept the default name, which is DaRT10.</span></span>

    <span data-ttu-id="4f91a-223">Der Assistent erstellt einen Unterordner im Ausgabepfad mit diesem Namen.</span><span class="sxs-lookup"><span data-stu-id="4f91a-223">The wizard creates a subfolder in the output path by this name.</span></span>

3.  <span data-ttu-id="4f91a-224">Wählen Sie die Typen von Bilddateien aus, die Sie erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="4f91a-224">Select the types of image files that you want to create.</span></span>

4.  <span data-ttu-id="4f91a-225">Wählen Sie eine der folgenden Optionen aus:</span><span class="sxs-lookup"><span data-stu-id="4f91a-225">Choose one of the following:</span></span>

    -   <span data-ttu-id="4f91a-226">Wenn Sie die Dateien im Wiederherstellungsabbild ändern möchten, bevor Sie die Bilddateien erstellen, aktivieren Sie das Kontrollkästchen **Bild bearbeiten** , und klicken Sie dann auf **vorbereiten**.</span><span class="sxs-lookup"><span data-stu-id="4f91a-226">To change the files in the recovery image before you create the image files, select the **Edit Image** check box, and then click **Prepare**.</span></span>

    -   <span data-ttu-id="4f91a-227">Wenn Sie das Wiederherstellungsabbild erstellen möchten, ohne die Dateien zu ändern, klicken Sie auf **Erstellen**.</span><span class="sxs-lookup"><span data-stu-id="4f91a-227">To create the recovery image without changing the files, click **Create**.</span></span>

5.  

    <span data-ttu-id="4f91a-228">Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="4f91a-228">Click **Next**.</span></span>

## <span data-ttu-id="4f91a-229">Bearbeiten der Wiederherstellungsbild Dateien</span><span class="sxs-lookup"><span data-stu-id="4f91a-229">Edit the recovery image files</span></span>


<span data-ttu-id="4f91a-230">Sie können das Wiederherstellungsbild nur bearbeiten, wenn Sie auf der Seite Bild erstellen das Kontrollkästchen Bild bearbeiten aktiviert haben.</span><span class="sxs-lookup"><span data-stu-id="4f91a-230">You can edit the recovery image only if you selected the Edit Image check box on the Create Image page.</span></span> <span data-ttu-id="4f91a-231">Nachdem das Wiederherstellungsabbild für die Bearbeitung vorbereitet wurde, können Sie die Wiederherstellungsabbild Dateien hinzufügen und ändern, bevor Sie das startfähige Medium erstellen.</span><span class="sxs-lookup"><span data-stu-id="4f91a-231">After the recovery image has been prepared for editing, you can add and modify the recovery image files before creating the bootable media.</span></span> <span data-ttu-id="4f91a-232">So können Sie beispielsweise eine benutzerdefinierte Reihenfolge für den Start erstellen, verschiedene Tools von Drittanbietern hinzufügen usw.</span><span class="sxs-lookup"><span data-stu-id="4f91a-232">For example, you can create a custom order for startup, add various third-party tools, and so on.</span></span>

**<span data-ttu-id="4f91a-233">So bearbeiten Sie die Wiederherstellungsbild Dateien</span><span class="sxs-lookup"><span data-stu-id="4f91a-233">To edit the recovery image files</span></span>**

1.  <span data-ttu-id="4f91a-234">Klicken Sie auf der Seite **Bild bearbeiten** auf in Windows-Explorer **Öffnen** .</span><span class="sxs-lookup"><span data-stu-id="4f91a-234">On the **Edit Image** page, click **Open** in Windows Explorer.</span></span>

2.  <span data-ttu-id="4f91a-235">Erstellen Sie einen Unterordner in dem Ordner, der im Dialogfeld aufgeführt ist.</span><span class="sxs-lookup"><span data-stu-id="4f91a-235">Create a subfolder in the folder that is listed in the dialog box.</span></span>

3.  <span data-ttu-id="4f91a-236">Kopieren Sie die gewünschten Dateien in den neuen Unterordner, oder entfernen Sie die Dateien, die Sie nicht benötigen.</span><span class="sxs-lookup"><span data-stu-id="4f91a-236">Copy the files that you want to the new subfolder, or remove files that you don’t want.</span></span>

4.  <span data-ttu-id="4f91a-237">Klicken Sie auf **Erstellen** , um die Erstellung des Wiederherstellungs Bilds zu starten.</span><span class="sxs-lookup"><span data-stu-id="4f91a-237">Click **Create** to start creating the recovery image.</span></span>

## <span data-ttu-id="4f91a-238">Generieren der Wiederherstellungsbild Dateien</span><span class="sxs-lookup"><span data-stu-id="4f91a-238">Generate the recovery image files</span></span>


<span data-ttu-id="4f91a-239">Auf der Seite "Dateien generieren" wird das DART-Wiederherstellungsbild für die Dateitypen generiert, die Sie auf der Seite "Bild erstellen" ausgewählt haben.</span><span class="sxs-lookup"><span data-stu-id="4f91a-239">On the Generate Files page, the DaRT recovery image is generated for the file types that you selected on the Create Image page.</span></span>

**<span data-ttu-id="4f91a-240">So generieren Sie die Wiederherstellungsbild Dateien</span><span class="sxs-lookup"><span data-stu-id="4f91a-240">To generate the recovery image files</span></span>**

-   <span data-ttu-id="4f91a-241">Klicken Sie auf der Seite **Dateien generieren** auf **weiter** , um die Wiederherstellungsabbild Dateien zu generieren.</span><span class="sxs-lookup"><span data-stu-id="4f91a-241">On the **Generate Files** page, click **Next** to generate the recovery image files.</span></span>

## <span data-ttu-id="4f91a-242">Kopieren des Wiederherstellungs Bilds auf eine CD, DVD oder USB</span><span class="sxs-lookup"><span data-stu-id="4f91a-242">Copy the recovery image to a CD, DVD, or USB</span></span>


<span data-ttu-id="4f91a-243">Auf der Seite startbare Medien erstellen können Sie die Bilddatei optional auf eine CD, DVD oder ein USB-Flashlaufwerk (USB-Stick) kopieren.</span><span class="sxs-lookup"><span data-stu-id="4f91a-243">On the Create Bootable Media page, you can optionally copy the image file to a CD, DVD, or USB flash drive (UFD).</span></span> <span data-ttu-id="4f91a-244">Sie können auf dieser Seite auch weitere startbare Medien erstellen, indem Sie den Assistenten erneut starten.</span><span class="sxs-lookup"><span data-stu-id="4f91a-244">You can also create additional bootable media from this page by restarting the wizard.</span></span>

<span data-ttu-id="4f91a-245">**Hinweis**  Die PXE-Installation (Preboot Execution Environment) und die Bereitstellung lokaler Bilder werden von diesem Tool nicht nativ unterstützt, da Sie zusätzliche Enterprise-Tools wie System Center Configuration Manager-Server und Microsoft Development Toolkit erfordern.</span><span class="sxs-lookup"><span data-stu-id="4f91a-245">**Note** The Preboot execution environment (PXE) and local image deployment are not supported natively by this tool since they require additional enterprise tools, such as System Center Configuration Manager server and Microsoft Development Toolkit.</span></span>

 

**<span data-ttu-id="4f91a-246">So kopieren Sie das Wiederherstellungsabbild auf eine CD, DVD oder USB</span><span class="sxs-lookup"><span data-stu-id="4f91a-246">To copy the recovery image to a CD, DVD, or USB</span></span>**

1.  <span data-ttu-id="4f91a-247">Wählen Sie auf der Seite startbare **Medien erstellen** die ISO-Datei aus, die Sie kopieren möchten.</span><span class="sxs-lookup"><span data-stu-id="4f91a-247">On the **Create Bootable Media** page, select the iso file that you want to copy.</span></span>

2.  <span data-ttu-id="4f91a-248">Legen Sie eine CD, DVD oder USB ein, und wählen Sie dann das Laufwerk aus.</span><span class="sxs-lookup"><span data-stu-id="4f91a-248">Insert a CD, DVD, or USB, and then select the drive.</span></span>

    <span data-ttu-id="4f91a-249">**Hinweis**  Wenn ein Laufwerk nicht erkannt wird und Sie ein neues Laufwerk installieren, können Sie auf **Aktualisieren** klicken, um den Assistenten zu zwingen, die Liste der verfügbaren Laufwerke zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="4f91a-249">**Note** If a drive is not recognized and you install a new drive, you can click **Refresh** to force the wizard to update the list of available drives.</span></span>

     

3.  <span data-ttu-id="4f91a-250">Klicken Sie auf die Schaltfläche **startfähige Medien erstellen** .</span><span class="sxs-lookup"><span data-stu-id="4f91a-250">Click the **Create Bootable Media** button.</span></span>

4.  <span data-ttu-id="4f91a-251">Wenn Sie ein weiteres Wiederherstellungsabbild erstellen möchten, klicken Sie auf neu starten, oder klicken Sie auf **Schließen** , wenn Sie mit dem Erstellen aller gewünschten Medien fertig sind.</span><span class="sxs-lookup"><span data-stu-id="4f91a-251">To create another recovery image, click Restart, or click **Close** if you have finished creating all of the media that you want.</span></span>

## <span data-ttu-id="4f91a-252">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="4f91a-252">Related topics</span></span>


[<span data-ttu-id="4f91a-253">Übersicht über die Tools in DaRT 10</span><span class="sxs-lookup"><span data-stu-id="4f91a-253">Overview of the Tools in DaRT 10</span></span>](overview-of-the-tools-in-dart-10.md)

[<span data-ttu-id="4f91a-254">Bereitstellen von DaRT 10</span><span class="sxs-lookup"><span data-stu-id="4f91a-254">Deploying DaRT 10</span></span>](deploying-dart-10.md)

 

 





