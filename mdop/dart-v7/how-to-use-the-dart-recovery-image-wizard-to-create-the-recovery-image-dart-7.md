---
title: So verwenden Sie den Assistent für DaRT-Wiederherstellungsabbilder zum Erstellen des Wiederherstellungsabbilds
description: So verwenden Sie den Assistent für DaRT-Wiederherstellungsabbilder zum Erstellen des Wiederherstellungsabbilds
author: dansimp
ms.assetid: 1b8ef983-fff9-4d75-a2f6-53120c5c00c9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 49253a8c0bf9c9073b57712acc773e4a57e31d72
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809646"
---
# <span data-ttu-id="acbd0-103">So verwenden Sie den Assistent für DaRT-Wiederherstellungsabbilder zum Erstellen des Wiederherstellungsabbilds</span><span class="sxs-lookup"><span data-stu-id="acbd0-103">How to Use the DaRT Recovery Image Wizard to Create the Recovery Image</span></span>


<span data-ttu-id="acbd0-104">Microsoft Diagnostics and Recovery Toolset (Dart) 7 umfasst den **Dart-Wiederherstellungs-Bild-Assistenten** , der in Windows zum Erstellen einer startbaren internationalen Organisation für Standardisierungs-Images (ISO) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="acbd0-104">Microsoft Diagnostics and Recovery Toolset (DaRT)7 includes the **DaRT Recovery Image Wizard** that is used in Windows to create a bootable International Organization for Standardization (ISO) image.</span></span> <span data-ttu-id="acbd0-105">Bei einem ISO-Bild handelt es sich um eine Datei, die den unformatierten Inhalt einer CD darstellt.</span><span class="sxs-lookup"><span data-stu-id="acbd0-105">An ISO image is a file that represents the raw contents of a CD.</span></span>

<span data-ttu-id="acbd0-106">Der **Dart-Wiederherstellungsbild-Assistent** benötigt die folgenden Informationen:</span><span class="sxs-lookup"><span data-stu-id="acbd0-106">The **DaRT Recovery Image Wizard** requires the following information:</span></span>

-   <span data-ttu-id="acbd0-107">**Startabbild**° ° Sie müssen den Pfad einer Windows 7-DVD oder Windows 7-Quelldateien angeben, die zum Erstellen des DART-Wiederherstellungs Bilds erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="acbd0-107">**Boot Image**˚˚You must provide the path of a Windows 7 DVD or Windows 7 source files that are required to create the DaRT recovery image.</span></span>

-   <span data-ttu-id="acbd0-108">**Werkzeug Auswahl**° ° Sie können die Tools auswählen, die in das DART-Wiederherstellungsbild aufgenommen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="acbd0-108">**Tool Selection**˚˚You can select the tools to include on the DaRT recovery image.</span></span>

-   <span data-ttu-id="acbd0-109">**Remoteverbindungen**° ° Sie können auswählen, ob das DART-Wiederherstellungsabbild die Möglichkeit zum Einrichten einer Remote Verbindung zwischen dem Helpdesk und dem Endbenutzercomputer aufweisen soll.</span><span class="sxs-lookup"><span data-stu-id="acbd0-109">**Remote Connections**˚˚You can select whether you want the DaRT recovery image to include the ability to establish a remote connection between the helpdesk and the end-user computer.</span></span>

-   <span data-ttu-id="acbd0-110">**Debugging-Tools für Windows**° ° Sie werden aufgefordert, den Speicherort der Debugging-Tools für Windows anzugeben.</span><span class="sxs-lookup"><span data-stu-id="acbd0-110">**Debugging Tools for Windows**˚˚You are asked to provide the location of the Debugging Tools for Windows.</span></span>

-   <span data-ttu-id="acbd0-111">**Definitionen für Standalone-System Sweeper**° ° Sie können entscheiden, ob Sie die neuesten Definitionen zu dem Zeitpunkt herunterladen möchten, zu dem Sie das Wiederherstellungsabbild erstellt haben, oder die Definitionen später herunterladen.</span><span class="sxs-lookup"><span data-stu-id="acbd0-111">**Definitions for Standalone System Sweeper**˚˚You can decide whether to download the latest definitions at the time that you create the recovery image or download the definitions later.</span></span>

-   <span data-ttu-id="acbd0-112">**Treiber**° ° Sie werden gefragt, ob Sie dem ISO-Abbild Treiber hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="acbd0-112">**Drivers**˚˚You are asked whether you want to add drivers to the ISO image.</span></span>

-   <span data-ttu-id="acbd0-113">**Weitere Dateien**° ° Sie können dem ISO-Abbilddateien hinzufügen, die möglicherweise beim Diagnostizieren von Problemen helfen.</span><span class="sxs-lookup"><span data-stu-id="acbd0-113">**Additional Files**˚˚You can add files to the ISO image that might help diagnose problems.</span></span>

-   <span data-ttu-id="acbd0-114">**ISO-Bildposition**° ° Sie werden aufgefordert anzugeben, wo sich das ISO-Abbild befinden soll.</span><span class="sxs-lookup"><span data-stu-id="acbd0-114">**ISO Image Location**˚˚You are asked to specify where the ISO image should be located.</span></span>

-   <span data-ttu-id="acbd0-115">**CD/DVD-Laufwerk**° ° Sie werden aufgefordert anzugeben, ob das CD-oder DVD-Laufwerk zum Brennen der CD oder DVD verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="acbd0-115">**CD/DVD Drive**˚˚You are asked to specify whether the CD or DVD drive should be used to burn the CD or DVD.</span></span>

<span data-ttu-id="acbd0-116">**Hinweis**  Die ISO-Bildgröße kann je nach den im **Dart-Wiederherstellungsbild-Assistenten**ausgewählten Tools variieren.</span><span class="sxs-lookup"><span data-stu-id="acbd0-116">**Note** The ISO image size can vary, depending on the tools that were selected in the **DaRT Recovery Image Wizard**.</span></span>

 

## <span data-ttu-id="acbd0-117">So erstellen Sie das Wiederherstellungsabbild mithilfe des DART-Wiederherstellungsbild-Assistenten</span><span class="sxs-lookup"><span data-stu-id="acbd0-117">To create the recovery image using the DaRT Recovery Image Wizard</span></span>


<span data-ttu-id="acbd0-118">Befolgen Sie diese Anweisungen, um das DART-Wiederherstellungsabbild mithilfe des **Dart-Wiederherstellungsbild-Assistenten** zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="acbd0-118">Follow these instructions to use the **DaRT Recovery Image Wizard** to create the DaRT recovery image.</span></span>

### <span data-ttu-id="acbd0-119">So wählen Sie die Tools aus, die Sie in das DART-Wiederherstellungsabbild einbeziehen möchten</span><span class="sxs-lookup"><span data-stu-id="acbd0-119">To select the tools to include on the DaRT recovery image</span></span>

<span data-ttu-id="acbd0-120">Der **Dart-Wiederherstellungsbild-Assistent** zeigt ein Dialogfeld für die **Tool Auswahl** an.</span><span class="sxs-lookup"><span data-stu-id="acbd0-120">The **DaRT Recovery Image Wizard** presents a **Tool Selection** dialog box.</span></span> <span data-ttu-id="acbd0-121">Sie können Tools aus der Liste der Tools auswählen oder entfernen, die im Dart-Wiederherstellungsbild enthalten sein sollen, indem Sie ein Tool markieren und dann auf die Schaltflächen **aktivieren** oder **Deaktivieren** klicken.</span><span class="sxs-lookup"><span data-stu-id="acbd0-121">You can select or remove tools from the list of tools to be included on the DaRT recovery image by highlighting a tool and then clicking the **Enable** or **Disable** buttons.</span></span>

<span data-ttu-id="acbd0-122">Nachdem Sie alle Tools ausgewählt haben, die Sie in das Wiederherstellungsabbild aufnehmen möchten, klicken Sie auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="acbd0-122">After you have selected all the tools that you want to include on the recovery image, click **Next**.</span></span>

### <span data-ttu-id="acbd0-123">So fügen Sie die Option zum Zulassen der Remotekonnektivität hinzu</span><span class="sxs-lookup"><span data-stu-id="acbd0-123">To add the option to allow remote connectivity</span></span>

<span data-ttu-id="acbd0-124">Sie können das Kontrollkästchen **Remoteverbindungen zulassen** aktivieren, um die Option im Fenster **Diagnose-und Wiederherstellungs-Toolset** bereitzustellen, um eine Remoteverbindung zwischen dem Helpdesk-Agenten und einem Endbenutzercomputer herzustellen.</span><span class="sxs-lookup"><span data-stu-id="acbd0-124">You can select the **Allow remote connections** check box to provide the option in the **Diagnostics and Recovery Toolset** window to establish a remote connection between the helpdesk agent and an end-user computer.</span></span> <span data-ttu-id="acbd0-125">Nachdem ein Helpdesk-Agent eine Remoteverbindung hergestellt hat, können Sie die Dart-Tools auf dem Endbenutzercomputer von einem Remotestandort aus ausführen.</span><span class="sxs-lookup"><span data-stu-id="acbd0-125">After a helpdesk agent establishes a remote connection, they can run the DaRT tools on the end-user computer from a remote location.</span></span>

<span data-ttu-id="acbd0-126">Sie können das Kontrollkästchen **Portnummer angeben** aktivieren, um eine bestimmte Portnummer einzugeben, die beim Einrichten einer Remoteverbindung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="acbd0-126">You can select the **Specify the port number** check box to enter a specific port number that will be used when establishing a remote connection.</span></span> <span data-ttu-id="acbd0-127">Sie können eine Portnummer zwischen 1 und 65535 angeben.</span><span class="sxs-lookup"><span data-stu-id="acbd0-127">You can specify a port number between 1 and 65535.</span></span> <span data-ttu-id="acbd0-128">Wir empfehlen, dass die Portnummer 1024 oder höher ist, um die Möglichkeit eines Konflikts zu minimieren.</span><span class="sxs-lookup"><span data-stu-id="acbd0-128">We recommend that the port number be 1024 or higher to minimize the possibility of a conflict.</span></span>

<span data-ttu-id="acbd0-129">Sie können auch eine angepasste Nachricht erstellen, die ein Endbenutzer erhält, wenn er eine Remoteverbindung herstellt.</span><span class="sxs-lookup"><span data-stu-id="acbd0-129">You can also create a customized message that an end user will receive when they establish a remote connection.</span></span> <span data-ttu-id="acbd0-130">Die Nachricht kann maximal 2048 Zeichen umfassen.</span><span class="sxs-lookup"><span data-stu-id="acbd0-130">The message can be a maximum of 2048 characters.</span></span>

<span data-ttu-id="acbd0-131">Weitere Informationen zum Remote Ausführen der Dart-Tools finden Sie unter [Wiederherstellen von Remotecomputern mithilfe des DART-Wiederherstellungs Bilds](how-to-recover-remote-computers-using-the-dart-recovery-image-dart-7.md).</span><span class="sxs-lookup"><span data-stu-id="acbd0-131">For more information about remotely running the DaRT tools, see [How to Recover Remote Computers Using the DaRT Recovery Image](how-to-recover-remote-computers-using-the-dart-recovery-image-dart-7.md).</span></span>

### <span data-ttu-id="acbd0-132">So fügen Sie dem Dart-Wiederherstellungsabbild die Debug-Tools für Windows hinzu</span><span class="sxs-lookup"><span data-stu-id="acbd0-132">To add the Debugging Tools for Windows to the DaRT recovery image</span></span>

<span data-ttu-id="acbd0-133">Im Dialogfeld **Absturzanalyse** des Bild- **Assistenten für Dart-Wiederherstellung**werden Sie aufgefordert, den Speicherort der Debugging-Tools für Windows anzugeben.</span><span class="sxs-lookup"><span data-stu-id="acbd0-133">In the **Crash Analyzer** dialog box of the **DaRT Recovery Image Wizard**, you are asked to specify the location of the Debugging Tools for Windows.</span></span> <span data-ttu-id="acbd0-134">Wenn Sie nicht über eine Kopie der Tools verfügen, können Sie Sie von Microsoft herunterladen.</span><span class="sxs-lookup"><span data-stu-id="acbd0-134">If you do not have a copy of the tools, you can download them from Microsoft.</span></span> <span data-ttu-id="acbd0-135">Der folgende Link zur Download-Seite wird im Assistenten bereitgestellt: [herunterladen und Installieren von Debugging-Tools für Windows](https://go.microsoft.com/fwlink/?LinkId=99934).</span><span class="sxs-lookup"><span data-stu-id="acbd0-135">The following link to the download page is provided in the wizard: [Download and Install Debugging Tools for Windows](https://go.microsoft.com/fwlink/?LinkId=99934).</span></span>

<span data-ttu-id="acbd0-136">Sie können entweder den Speicherort der Debug-Tools auf dem Computer angeben, auf dem Sie den **Dart-Wiederherstellungsbild-Assistenten**ausführen, oder Sie können die Tools verwenden, die sich auf dem Zielcomputer befinden.</span><span class="sxs-lookup"><span data-stu-id="acbd0-136">You can either specify the location of the debugging tools on the computer where you are running the **DaRT Recovery Image Wizard**, or you can decide to use the tools that are located on the destination computer.</span></span> <span data-ttu-id="acbd0-137">Wenn Sie sich entscheiden, eine Kopie auf einem anderen Computer zu verwenden, müssen Sie sicherstellen, dass die Tools auf jedem Computer installiert sind, auf dem Sie einen Absturz diagnostizieren.</span><span class="sxs-lookup"><span data-stu-id="acbd0-137">If you decide to use a copy on another computer, you must make sure that the tools are installed on each computer on which you are diagnosing a crash.</span></span>

<span data-ttu-id="acbd0-138">**Hinweis**  Wenn Sie **Crash Analyzer** in das ISO-Abbild einbeziehen, empfehlen wir, dass Sie auch die Debugging-Tools für Windows einbeziehen.</span><span class="sxs-lookup"><span data-stu-id="acbd0-138">**Note** If you include the **Crash Analyzer** in the ISO image, we recommend that you also include the Debugging Tools for Windows.</span></span>

 

<span data-ttu-id="acbd0-139">Führen Sie die folgenden Schritte aus, um die Debugging-Tools für Windows hinzuzufügen:</span><span class="sxs-lookup"><span data-stu-id="acbd0-139">Follow these steps to add the Debugging Tools for Windows:</span></span>

1.  <span data-ttu-id="acbd0-140">Optional Klicken Sie auf den Link, um die Debugging-Tools für Windows herunterzuladen.</span><span class="sxs-lookup"><span data-stu-id="acbd0-140">(Optional) Click the hyperlink to download the Debugging Tools for Windows.</span></span>

2.  <span data-ttu-id="acbd0-141">Wählen Sie eine der folgenden Optionen aus:</span><span class="sxs-lookup"><span data-stu-id="acbd0-141">Select one of the following options:</span></span>

    -   <span data-ttu-id="acbd0-142">**Verwenden Sie die Debugging-Tools für Windows an der folgenden Position**.</span><span class="sxs-lookup"><span data-stu-id="acbd0-142">**Use the Debugging Tools for Windows in the following location**.</span></span> <span data-ttu-id="acbd0-143">Wenn Sie diese Option auswählen, können Sie zum Speicherort der Tools navigieren.</span><span class="sxs-lookup"><span data-stu-id="acbd0-143">If you select this option, you can browse to the location of the tools.</span></span>

    -   <span data-ttu-id="acbd0-144">**Suchen Sie die Debugging-Tools für Windows auf dem System, das Sie reparieren möchten**.</span><span class="sxs-lookup"><span data-stu-id="acbd0-144">**Locate the Debugging Tools for Windows on the system that you are repairing**.</span></span> <span data-ttu-id="acbd0-145">Wenn Sie diese Option auswählen, funktioniert der **Absturzanalyse** Programm nicht, wenn die Debugging-Tools für Windows auf dem Problem Computer nicht gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="acbd0-145">If you select this option, the **Crash Analyzer** will not work if the Debugging Tools for Windows are not found on the problem computer.</span></span>

3.  <span data-ttu-id="acbd0-146">Klicken Sie abschließend auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="acbd0-146">After you have finished, click **Next**.</span></span>

### <span data-ttu-id="acbd0-147">So fügen Sie dem Dart-Wiederherstellungsabbild Definitionen für eigenständige System Sweeper hinzu</span><span class="sxs-lookup"><span data-stu-id="acbd0-147">To add definitions for Standalone System Sweeper to the DaRT recovery image</span></span>

<span data-ttu-id="acbd0-148">Definitionen sind ein Repository bekannter Schadsoftware und anderer potenziell unerwünschter Software.</span><span class="sxs-lookup"><span data-stu-id="acbd0-148">Definitions are a repository of known malware and other potentially unwanted software.</span></span> <span data-ttu-id="acbd0-149">Da Malware kontinuierlich entwickelt wird, setzt **Standalone-System Sweeper** auf aktuelle Definitionen, um festzustellen, ob Software, die versucht, die Einstellungen auf einem Computer zu installieren, auszuführen oder zu ändern, potenziell unerwünschte oder bösartige Software ist.</span><span class="sxs-lookup"><span data-stu-id="acbd0-149">Because malware is being continually developed, **Standalone System Sweeper** relies on current definitions to determine whether software that is trying to install, run, or change settings on a computer is potentially unwanted or malicious software.</span></span>

<span data-ttu-id="acbd0-150">Wenn Sie die neuesten Definitionen in das DART-Wiederherstellungsabbild einbeziehen möchten (empfohlen), klicken Sie auf **Ja, um die neuesten Definitionen herunterzuladen.**</span><span class="sxs-lookup"><span data-stu-id="acbd0-150">To include the latest definitions in the DaRT recovery image (recommended), click **Yes, download the latest definitions.**</span></span> <span data-ttu-id="acbd0-151">Das Definitionsupdate wird automatisch gestartet.</span><span class="sxs-lookup"><span data-stu-id="acbd0-151">The definition update starts automatically.</span></span> <span data-ttu-id="acbd0-152">Sie müssen mit dem Internet verbunden sein, um diesen Vorgang abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="acbd0-152">You must be connected to the Internet to complete this process.</span></span>

<span data-ttu-id="acbd0-153">Wenn Sie das Definitionsupdate überspringen möchten, klicken Sie auf **Nein, Definitionen später manuell herunterladen**.</span><span class="sxs-lookup"><span data-stu-id="acbd0-153">To skip the definition update, click **No, manually download definitions later**.</span></span> <span data-ttu-id="acbd0-154">Definitionen werden nicht in das DART-Wiederherstellungsbild aufgenommen.</span><span class="sxs-lookup"><span data-stu-id="acbd0-154">Definitions will not be included in the DaRT recovery image.</span></span>

<span data-ttu-id="acbd0-155">Wenn Sie sich entschließen, die neuesten Definitionen nicht in das Wiederherstellungsabbild aufzunehmen, oder wenn die im Wiederherstellungsabbild enthaltenen Definitionen nicht mehr aktuell sind, wenn Sie bereit sind, **eigenständiges System Sweeper**zu verwenden, besorgen Sie sich die neuesten Definitionen, bevor Sie mit dem Scannen beginnen, indem Sie die Anweisungen befolgen, die im **eigenständigen System Sweeper**bereitgestellt werden</span><span class="sxs-lookup"><span data-stu-id="acbd0-155">If you decide not to include the latest definitions on the recovery image, or if the definitions included on the recovery image are no longer current by the time that you are ready to use **Standalone System Sweeper**, obtain the latest definitions before you begin a scan by following the instructions that are provided in the **Standalone System Sweeper**.</span></span>

<span data-ttu-id="acbd0-156">**Wichtig**  Sie können nicht überprüfen, ob keine Definitionen vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="acbd0-156">**Important** You cannot scan if there are no definitions.</span></span>

 

<span data-ttu-id="acbd0-157">Klicken Sie abschließend auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="acbd0-157">After you have finished, click **Next**.</span></span>

### <span data-ttu-id="acbd0-158">So fügen Sie dem Dart-Wiederherstellungsabbild Treiber hinzu</span><span class="sxs-lookup"><span data-stu-id="acbd0-158">To add drivers to the DaRT recovery image</span></span>

<span data-ttu-id="acbd0-159">**Vorsicht**  Wenn Sie dem Dart-Wiederherstellungsabbild einen Treiber hinzufügen, werden standardmäßig alle weiteren Dateien und Unterordner, die sich in diesem Ordner befinden, dem Wiederherstellungsabbild hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="acbd0-159">**Caution** By default, when you add a driver to the DaRT recovery image, all additional files and subfolders that are located in that folder are added into the recovery image.</span></span> <span data-ttu-id="acbd0-160">Weitere Informationen finden Sie unter [Problembehandlung bei Dart 7,0](troubleshooting-dart-70-new-ia.md).</span><span class="sxs-lookup"><span data-stu-id="acbd0-160">For more information, see [Troubleshooting DaRT 7.0](troubleshooting-dart-70-new-ia.md).</span></span>

 

<span data-ttu-id="acbd0-161">Sie sollten zusätzliche Treiber für das Wiederherstellungsabbild für DaRT7 hinzufügen, die Sie möglicherweise benötigen, wenn Sie einen Computer reparieren.</span><span class="sxs-lookup"><span data-stu-id="acbd0-161">You should include additional drivers on the recovery image for DaRT7 that you may need when repairing a computer.</span></span> <span data-ttu-id="acbd0-162">Diese können in der Regelspeicher-oder Netzwerk Controller enthalten, die nicht auf der Windows-DVD enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="acbd0-162">These may typically include storage or network controllers that are not included on the Windows DVD.</span></span>

<span data-ttu-id="acbd0-163">**Wichtig**  Beachten Sie bei der Auswahl der zu berücksichtigenden Treiber, dass drahtlose Verbindungen (wie Bluetooth oder 802.11 a/b/g/n) in DART nicht unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="acbd0-163">**Important** When you select drivers to include, be aware that wireless connectivity (such as Bluetooth or 802.11a/b/g/n) is not supported in DaRT.</span></span>

 

**<span data-ttu-id="acbd0-164">So fügen Sie dem Wiederherstellungsabbild einen Speicher-oder Netzwerk Controller Treiber hinzu</span><span class="sxs-lookup"><span data-stu-id="acbd0-164">To add a storage or network controller driver to the recovery image</span></span>**

1.  <span data-ttu-id="acbd0-165">Klicken Sie im Dialogfeld **zusätzliche Treiber** des **Bild-Assistenten für Dart-Wiederherstellung**auf **Gerät hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="acbd0-165">In the **Additional Drivers** dialog box of the **DaRT Recovery Image Wizard**, click **Add Device**.</span></span>

2.  <span data-ttu-id="acbd0-166">Navigieren Sie zu der Datei, die für den Treiber hinzugefügt werden soll, und klicken Sie dann auf **Öffnen**.</span><span class="sxs-lookup"><span data-stu-id="acbd0-166">Browse to the file to be added for the driver, and then click **Open**.</span></span>

    <span data-ttu-id="acbd0-167">**Hinweis**  Die **Treiber** Datei wird vom Hersteller des Speichers oder des Netzwerkcontrollers bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="acbd0-167">**Note** The **driver** file is provided by the manufacturer of the storage or network controller.</span></span>

     

3.  <span data-ttu-id="acbd0-168">Wiederholen Sie die Schritte 1 und 2 für jeden Treiber, den Sie einbeziehen möchten.</span><span class="sxs-lookup"><span data-stu-id="acbd0-168">Repeat Steps 1 and 2 for every driver that you want to include.</span></span>

4.  <span data-ttu-id="acbd0-169">Klicken Sie abschließend auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="acbd0-169">After you have finished, click **Next**.</span></span>

### <span data-ttu-id="acbd0-170">So fügen Sie dem Dart-Wiederherstellungsabbild Dateien hinzu</span><span class="sxs-lookup"><span data-stu-id="acbd0-170">To add files to the DaRT recovery image</span></span>

<span data-ttu-id="acbd0-171">Führen Sie die folgenden Schritte aus, um dem Wiederherstellungsabbild Dateien hinzuzufügen, damit Sie diese zum Diagnostizieren von Computerproblemen verwenden können.</span><span class="sxs-lookup"><span data-stu-id="acbd0-171">Follow these steps to add files to the recovery image so that you can use them to diagnose computer problems.</span></span>

1.  <span data-ttu-id="acbd0-172">Klicken Sie im Dialogfeld **Weitere Dateien** des **Assistenten für Dart-Wiederherstellungs Bilder**auf **Dateien anzeigen**.</span><span class="sxs-lookup"><span data-stu-id="acbd0-172">In the **Additional Files** dialog box of the **DaRT Recovery Image Wizard**, click **Show Files**.</span></span> <span data-ttu-id="acbd0-173">Dadurch wird ein Explorer-Fenster geöffnet, in dem der Ordner angezeigt wird, in dem die freigegebenen Dateien gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="acbd0-173">This opens an Explorer window that displays the folder that holds the shared files.</span></span>

2.  <span data-ttu-id="acbd0-174">Erstellen Sie einen Unterordner in dem Ordner, der im Dialogfeld aufgeführt ist.</span><span class="sxs-lookup"><span data-stu-id="acbd0-174">Create a subfolder in the folder that is listed in the dialog box.</span></span>

3.  <span data-ttu-id="acbd0-175">Kopieren Sie die gewünschten Dateien in den neuen Unterordner.</span><span class="sxs-lookup"><span data-stu-id="acbd0-175">Copy the files that you want to the new subfolder.</span></span>

4.  <span data-ttu-id="acbd0-176">Klicken Sie abschließend auf **Weiter.**</span><span class="sxs-lookup"><span data-stu-id="acbd0-176">After you have finished, click **Next.**</span></span>

### <span data-ttu-id="acbd0-177">So wählen Sie einen Speicherort für die ISO-Datei aus, die das DART-Wiederherstellungsabbild enthält</span><span class="sxs-lookup"><span data-stu-id="acbd0-177">To select a location for the ISO that contains the DaRT recovery image</span></span>

<span data-ttu-id="acbd0-178">Führen Sie die folgenden Schritte aus, um den Speicherort für die Erstellung des ISO-Images anzugeben:</span><span class="sxs-lookup"><span data-stu-id="acbd0-178">Follow these steps to specify the location where the ISO image is created:</span></span>

1.  <span data-ttu-id="acbd0-179">Klicken Sie im Dialogfeld **Startabbild erstellen** des **Dart-Wiederherstellungsbild-Assistenten**auf **Durchsuchen**.</span><span class="sxs-lookup"><span data-stu-id="acbd0-179">In the **Create Startup Image** dialog box of the **DaRT Recovery Image Wizard**, click **Browse**.</span></span>

2.  <span data-ttu-id="acbd0-180">Navigieren Sie im Fenster **Speichern** unter zu dem bevorzugten Speicherort, und klicken Sie dann auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="acbd0-180">Browse to the preferred location in the **Save As** window, and then click **Save**.</span></span>

3.  <span data-ttu-id="acbd0-181">Klicken Sie abschließend auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="acbd0-181">After you have finished, click **Next**.</span></span>

<span data-ttu-id="acbd0-182">Die Größe des ISO-Bilds hängt von den ausgewählten Tools und den Dateien ab, die Sie im Assistenten hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="acbd0-182">The size of the ISO image will vary, depending on the tools that you select and the files that you add in the wizard.</span></span>

<span data-ttu-id="acbd0-183">Der Assistent erfordert eine ISO **-** Dateinamenerweiterung, da für die meisten Programme, die eine CD oder DVD brennen, diese Erweiterung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="acbd0-183">The wizard requires the ISO image to have an **.iso** file name extension because most programs that burn a CD or DVD require that extension.</span></span> <span data-ttu-id="acbd0-184">Wenn Sie keinen anderen Speicherort angeben, wird das ISO-Abbild auf dem Desktop mit dem Namen **DaRT70. ISO**erstellt.</span><span class="sxs-lookup"><span data-stu-id="acbd0-184">If you do not specify a different location, the ISO image is created on your desktop with the name **DaRT70.ISO**.</span></span>

### <span data-ttu-id="acbd0-185">So brennen Sie das Wiederherstellungsabbild auf eine CD oder DVD</span><span class="sxs-lookup"><span data-stu-id="acbd0-185">To burn the recovery image to a CD or DVD</span></span>

<span data-ttu-id="acbd0-186">Wenn der **Dart-Wiederherstellungs-Bild-Assistent** ein kompatibles CD-RW-Laufwerk auf dem Computer erkennt, bietet es an, das ISO-Image auf einen Datenträger zu brennen.</span><span class="sxs-lookup"><span data-stu-id="acbd0-186">If the **DaRT Recovery Image Wizard** detects a compatible CD-RW drive on your computer, it offers to burn the ISO image to a disc for you.</span></span> <span data-ttu-id="acbd0-187">Wenn Sie eine CD oder DVD brennen möchten und der Assistent Ihr Laufwerk nicht erkennt, müssen Sie ein anderes Programm verwenden, beispielsweise das Programm, das im Lieferumfang Ihres Laufwerks enthalten war.</span><span class="sxs-lookup"><span data-stu-id="acbd0-187">If you want to burn a CD or DVD and the wizard does not recognize your drive, you must use another program, such as the program that was included with your drive.</span></span> <span data-ttu-id="acbd0-188">Sie können einen Duplizierer, einen Duplizierungs Dienst oder eine CD-oder DVD-Brennsoftware verwenden, um zusätzliche Kopien zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="acbd0-188">You can use a duplicator, a duplicating service, or CD or DVD-burning software to make any additional copies.</span></span>

1.  <span data-ttu-id="acbd0-189">Wählen Sie im Dialogfeld " **auf eine beschreibbare CD/DVD brennen** " des **Assistenten für Dart-Wiederherstellungs Bilder**die Option **Image auf das folgende beschreibbare CD/DVD-Laufwerk brennen**aus.</span><span class="sxs-lookup"><span data-stu-id="acbd0-189">In the **Burn to a recordable CD/DVD** dialog box of the **DaRT Recovery Image Wizard**, select **Burn the image to the following recordable CD/DVD drive**.</span></span>

2.  <span data-ttu-id="acbd0-190">Wählen Sie das CD-oder DVD-Laufwerk aus.</span><span class="sxs-lookup"><span data-stu-id="acbd0-190">Select the CD or DVD drive.</span></span>

    <span data-ttu-id="acbd0-191">**Hinweis**  Wenn ein Laufwerk nicht erkannt wird und Sie ein neues Laufwerk installieren, können Sie auf **Laufwerkliste aktualisieren** klicken, um den Assistenten zu zwingen, die Liste der verfügbaren Laufwerke zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="acbd0-191">**Note** If a drive is not recognized and you install a new drive, you can click **Refresh Drive List** to force the wizard to update the list of available drives.</span></span>

     

3.  <span data-ttu-id="acbd0-192">Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="acbd0-192">Click **Next**.</span></span>

## <span data-ttu-id="acbd0-193">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="acbd0-193">Related topics</span></span>


[<span data-ttu-id="acbd0-194">Erstellen des DaRT 7.0-Wiederherstellungsabbilds</span><span class="sxs-lookup"><span data-stu-id="acbd0-194">Creating the DaRT 7.0 Recovery Image</span></span>](creating-the-dart-70-recovery-image-dart-7.md)

 

 





