---
title: Erstellen eines virtuellen PC-Images für MED-V
description: Erstellen eines virtuellen PC-Images für MED-V
author: dansimp
ms.assetid: 5e02ea07-25b9-41a5-a803-d70c55eef586
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 84e45f9ff7213abdd6288bcd750238436d3ab68c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810090"
---
# <span data-ttu-id="47ee1-103">Erstellen eines virtuellen PC-Images für MED-V</span><span class="sxs-lookup"><span data-stu-id="47ee1-103">Creating a Virtual PC Image for MED-V</span></span>


<span data-ttu-id="47ee1-104">Zum Erstellen eines virtuellen PC-Images (VPC) für MED-V müssen Sie die folgenden Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="47ee1-104">To create a Virtual PC (VPC) image for MED-V, you must perform the following:</span></span>

1.  <span data-ttu-id="47ee1-105">[Erstellen Sie ein VPC-Bild](#bkmk-creatingavirtualmachinebyusingmicrosoftvirtualpc).</span><span class="sxs-lookup"><span data-stu-id="47ee1-105">[Create a VPC image](#bkmk-creatingavirtualmachinebyusingmicrosoftvirtualpc).</span></span>

2.  <span data-ttu-id="47ee1-106">[Installieren Sie das MED-V Workspace. MSI-Paket auf dem VPC-Abbild](#bkmk-howtoinstallthemedvworkspacemsipackage).</span><span class="sxs-lookup"><span data-stu-id="47ee1-106">[Install the MED-V workspace .msi package onto the VPC image](#bkmk-howtoinstallthemedvworkspacemsipackage).</span></span>

3.  <span data-ttu-id="47ee1-107">[Führen Sie das Tool MED-V Virtual Machine Voraussetzungen für das VPC-Abbild aus](#bkmk-howtorunthevirtualmachineprerequisitestool).</span><span class="sxs-lookup"><span data-stu-id="47ee1-107">[Run the MED-V virtual machine prerequisites tool on the VPC image](#bkmk-howtorunthevirtualmachineprerequisitestool).</span></span>

4.  <span data-ttu-id="47ee1-108">[Manuelle Konfiguration von Voraussetzungen für virtuelle Maschinen auf dem VPC-Abbild](#bkmk-howtoconfiguremedvvirtualmachinemanualinstallationprerequisites)</span><span class="sxs-lookup"><span data-stu-id="47ee1-108">[Manually configure virtual machine prerequisites on the VPC image](#bkmk-howtoconfiguremedvvirtualmachinemanualinstallationprerequisites).</span></span>

5.  <span data-ttu-id="47ee1-109">[Konfigurieren von Sysprep für MED-V-Bilder](#bkmk-howtoconfiguresysprepformedvimages) (optional).</span><span class="sxs-lookup"><span data-stu-id="47ee1-109">[Configure Sysprep for MED-V images](#bkmk-howtoconfiguresysprepformedvimages) (optional).</span></span>

6.  <span data-ttu-id="47ee1-110">[Deaktivieren Sie Microsoft Virtual PC](#bkmk-turningoffmicrosoftvirtualpc).</span><span class="sxs-lookup"><span data-stu-id="47ee1-110">[Turn off Microsoft Virtual PC](#bkmk-turningoffmicrosoftvirtualpc).</span></span>

## <a href="" id="bkmk-creatingavirtualmachinebyusingmicrosoftvirtualpc"></a><span data-ttu-id="47ee1-111">Erstellen eines virtuellen PC-Images mithilfe von Microsoft Virtual PC</span><span class="sxs-lookup"><span data-stu-id="47ee1-111">Creating a Virtual PC Image by Using Microsoft Virtual PC</span></span>


<span data-ttu-id="47ee1-112">Informationen zum Erstellen eines virtuellen PC-Images mit Microsoft Virtual PC finden Sie in der Virtual PC-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="47ee1-112">To create a Virtual PC image using Microsoft Virtual PC, refer to the Virtual PC documentation.</span></span>

<span data-ttu-id="47ee1-113">Weitere Informationen finden Sie in den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="47ee1-113">For more information, see the following:</span></span>

-   [<span data-ttu-id="47ee1-114">Hilfe zu Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="47ee1-114">Windows Virtual PC Help</span></span>](https://go.microsoft.com/fwlink/?LinkId=182378)

-   [<span data-ttu-id="47ee1-115">Erstellen eines virtuellen Computers und Installieren eines Gastbetriebssystems</span><span class="sxs-lookup"><span data-stu-id="47ee1-115">Create a virtual machine and install a guest operating system</span></span>](https://go.microsoft.com/fwlink/?LinkId=182379)

## <a href="" id="bkmk-howtoinstallthemedvworkspacemsipackage"></a><span data-ttu-id="47ee1-116">Installieren des MED-V Workspace. msi-Pakets</span><span class="sxs-lookup"><span data-stu-id="47ee1-116">How to Install the MED-V Workspace .msi Package</span></span>


<span data-ttu-id="47ee1-117">Installieren Sie nach dem Erstellen des Virtual PC-Bilds das MED-V Workspace. MSI-Paket auf dem Bild.</span><span class="sxs-lookup"><span data-stu-id="47ee1-117">After the Virtual PC image is created, install the MED-V workspace .msi package onto the image.</span></span>

**<span data-ttu-id="47ee1-118">So installieren Sie das MED-V Workspace-Bild</span><span class="sxs-lookup"><span data-stu-id="47ee1-118">To install the MED-V workspace image</span></span>**

1.  <span data-ttu-id="47ee1-119">Starten Sie den virtuellen Computer, und kopieren Sie das MED-V Workspace. MSI-Paket nach innen.</span><span class="sxs-lookup"><span data-stu-id="47ee1-119">Start the virtual machine, and copy the MED-V workspace .msi package inside.</span></span>

    <span data-ttu-id="47ee1-120">Das MED-V Workspace. MSI-Paket heißt *MED-V\_workspace\_x.msi*, wobei *x* die Versionsnummer ist.</span><span class="sxs-lookup"><span data-stu-id="47ee1-120">The MED-V workspace .msi package is called *MED-V\_workspace\_x.msi*, where *x* is the version number.</span></span>

    <span data-ttu-id="47ee1-121">Beispiel: *MED-V\_workspace\_1.0.65.msi*.</span><span class="sxs-lookup"><span data-stu-id="47ee1-121">For example, *MED-V\_workspace\_1.0.65.msi*.</span></span>

2.  <span data-ttu-id="47ee1-122">Doppelklicken Sie auf das MED-V Workspace. MSI-Paket, und folgen Sie den Anweisungen des Installations-Assistenten.</span><span class="sxs-lookup"><span data-stu-id="47ee1-122">Double-click the MED-V workspace .msi package, and follow the installation wizard instructions.</span></span>

    **<span data-ttu-id="47ee1-123">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="47ee1-123">Note</span></span>**  
    <span data-ttu-id="47ee1-124">Wenn eine neue Med-v-Version veröffentlicht wird und ein vorhandenes Virtual PC-Abbild aktualisiert wird, deinstallieren Sie das vorhandene Med-v Workspace. MSI-Paket, starten Sie den Computer neu, und installieren Sie das neue Med-v Workspace. MSI-Paket.</span><span class="sxs-lookup"><span data-stu-id="47ee1-124">When a new MED-V version is released, and an existing Virtual PC image is updated, uninstall the existing MED-V workspace .msi package, reboot the computer, and install the new MED-V workspace .msi package.</span></span>



~~~
**Note**  
After the MED-V workspace .msi package is installed, other products that replace GINA cannot be installed.
~~~



## <a href="" id="bkmk-howtorunthevirtualmachineprerequisitestool"></a><span data-ttu-id="47ee1-125">Ausführen des Tools für Voraussetzungen für virtuelle Maschinen</span><span class="sxs-lookup"><span data-stu-id="47ee1-125">How to Run the Virtual Machine Prerequisites Tool</span></span>


<span data-ttu-id="47ee1-126">Das Tool für die Voraussetzungen für virtuelle Maschinen (VM) ist ein Assistent, der mehrere Voraussetzungen automatisiert.</span><span class="sxs-lookup"><span data-stu-id="47ee1-126">The virtual machine (VM) prerequisites tool is a wizard that automates several of the prerequisites.</span></span>

**<span data-ttu-id="47ee1-127">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="47ee1-127">Note</span></span>**  
<span data-ttu-id="47ee1-128">Obwohl im Assistenten viele Parameter konfigurierbar sind, können die für die ordnungsgemäße Funktion von MED-V erforderlichen Eigenschaften nicht konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="47ee1-128">Although many parameters are configurable in the wizard, the properties required for the proper functioning of MED-V are not configurable.</span></span>



**<span data-ttu-id="47ee1-129">So führen Sie das Tool für Voraussetzungen für virtuelle Maschinen aus</span><span class="sxs-lookup"><span data-stu-id="47ee1-129">To run the virtual machine prerequisites tool</span></span>**

1.  <span data-ttu-id="47ee1-130">Nachdem das Med-v Workspace. MSI-Paket installiert wurde, wählen Sie **Start** im Windows-Startmenü **Alle Programme &gt; Med-v &gt; VM-Voraussetzungen-Tool**aus.</span><span class="sxs-lookup"><span data-stu-id="47ee1-130">After the MED-V workspace .msi package is installed, on the Windows **Start** menu, select **All Programs &gt; MED-V &gt; VM Prerequisites Tool**.</span></span>

    **<span data-ttu-id="47ee1-131">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="47ee1-131">Note</span></span>**  
    <span data-ttu-id="47ee1-132">Der Benutzer, der das Tool für Voraussetzungen für virtuelle Maschinen ausführt, muss über lokale Administratorrechte verfügen und muss der einzige Benutzer sein, der angemeldet ist.</span><span class="sxs-lookup"><span data-stu-id="47ee1-132">The user running the virtual machine prerequisites tool must have local administrator rights and must be the only user logged in.</span></span>



~~~
The **MED-V VM Prerequisite Wizard Welcome** page appears.
~~~

2. <span data-ttu-id="47ee1-133">Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="47ee1-133">Click **Next**.</span></span>

3. <span data-ttu-id="47ee1-134">Wählen Sie auf der Seite **Windows-Einstellungen** in den folgenden konfigurierbaren Eigenschaften die zu konfigurierenden Eigenschaften aus:</span><span class="sxs-lookup"><span data-stu-id="47ee1-134">On the **Windows Settings** page, from the following configurable properties, select the ones to be configured:</span></span>

   -   **<span data-ttu-id="47ee1-135">Löschen der persönlichen Verlaufsinformationen der Benutzer</span><span class="sxs-lookup"><span data-stu-id="47ee1-135">Clear users’ personal history information</span></span>**

   -   **<span data-ttu-id="47ee1-136">Temporäres Verzeichnis für lokales Profil löschen</span><span class="sxs-lookup"><span data-stu-id="47ee1-136">Clear local profiles temp directory</span></span>**

   -   **<span data-ttu-id="47ee1-137">Deaktivieren von Sounds für folgende Windows-Ereignisse: Start, Anmeldung, Abmelden</span><span class="sxs-lookup"><span data-stu-id="47ee1-137">Disable sounds on following Windows events: start, logon, logoff</span></span>**

   **<span data-ttu-id="47ee1-138">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="47ee1-138">Note</span></span>**  
   <span data-ttu-id="47ee1-139">Aktivieren Sie den Windows-Seiten Speicher in einer Gruppenrichtlinie nicht.</span><span class="sxs-lookup"><span data-stu-id="47ee1-139">Do not enable Windows page saver in a group policy.</span></span>



4. <span data-ttu-id="47ee1-140">Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="47ee1-140">Click **Next**.</span></span>

5. <span data-ttu-id="47ee1-141">Wählen Sie auf der Seite **Internet Explorer-Einstellungen** in den folgenden konfigurierbaren Eigenschaften die zu konfigurierenden Eigenschaften aus:</span><span class="sxs-lookup"><span data-stu-id="47ee1-141">On the **Internet Explorer Settings** page, from the following configurable properties, select the ones to be configured:</span></span>

   -   **<span data-ttu-id="47ee1-142">Verwenden Sie keine AutoVervollständigen-Features</span><span class="sxs-lookup"><span data-stu-id="47ee1-142">Don't use auto complete features</span></span>**

   -   **<span data-ttu-id="47ee1-143">Deaktivieren der Wiederverwendung von Windows zum Starten von Tastenkombinationen</span><span class="sxs-lookup"><span data-stu-id="47ee1-143">Disable reuse of windows for launching shortcuts</span></span>**

   -   **<span data-ttu-id="47ee1-144">Browserverlauf löschen</span><span class="sxs-lookup"><span data-stu-id="47ee1-144">Clear browsing history</span></span>**

   -   **<span data-ttu-id="47ee1-145">Aktivieren von Tabbed-Browsing in Internet Explorer 7</span><span class="sxs-lookup"><span data-stu-id="47ee1-145">Enable tabbed browsing in Internet Explorer 7</span></span>**

6. <span data-ttu-id="47ee1-146">Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="47ee1-146">Click **Next**.</span></span>

7. <span data-ttu-id="47ee1-147">Wählen Sie auf der Seite **Windows-Dienste** in den folgenden konfigurierbaren Eigenschaften die zu konfigurierenden Eigenschaften aus:</span><span class="sxs-lookup"><span data-stu-id="47ee1-147">On the **Windows Services** page, from the following configurable properties, select the ones to be configured:</span></span>

   -   **<span data-ttu-id="47ee1-148">Security Center-Dienst</span><span class="sxs-lookup"><span data-stu-id="47ee1-148">Security center service</span></span>**

   -   **<span data-ttu-id="47ee1-149">Aufgabenplanungsdienst</span><span class="sxs-lookup"><span data-stu-id="47ee1-149">Task scheduler service</span></span>**

   -   **<span data-ttu-id="47ee1-150">Dienst für automatische Updates</span><span class="sxs-lookup"><span data-stu-id="47ee1-150">Automatic updates service</span></span>**

   -   **<span data-ttu-id="47ee1-151">System Wiederherstellungs Dienst</span><span class="sxs-lookup"><span data-stu-id="47ee1-151">System restore service</span></span>**

   -   **<span data-ttu-id="47ee1-152">Indizierungsdienst</span><span class="sxs-lookup"><span data-stu-id="47ee1-152">Indexing service</span></span>**

   -   **<span data-ttu-id="47ee1-153">Drahtlose Nullkonfiguration</span><span class="sxs-lookup"><span data-stu-id="47ee1-153">Wireless Zero Configuration</span></span>**

   -   **<span data-ttu-id="47ee1-154">Schnelle Benutzerwechsel Kompatibilität</span><span class="sxs-lookup"><span data-stu-id="47ee1-154">Fast User Switching Compatibility</span></span>**

8. <span data-ttu-id="47ee1-155">Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="47ee1-155">Click **Next**.</span></span>

9. <span data-ttu-id="47ee1-156">Gehen Sie auf der Windows-Seite für die **automatische Anmeldung** wie folgt vor:</span><span class="sxs-lookup"><span data-stu-id="47ee1-156">On the **Windows Auto Logon** page, do the following:</span></span>

   1.  <span data-ttu-id="47ee1-157">Aktivieren Sie das Kontrollkästchen **Automatische Windows-Anmeldung aktivieren** .</span><span class="sxs-lookup"><span data-stu-id="47ee1-157">Select the **Enable Windows Auto Logon** check box.</span></span>

   2.  <span data-ttu-id="47ee1-158">Weisen Sie einen **Benutzernamen** und ein **Kennwort**zu.</span><span class="sxs-lookup"><span data-stu-id="47ee1-158">Assign a **User name** and **Password**.</span></span>

10. <span data-ttu-id="47ee1-159">Klicken Sie auf über **nehmen**, und klicken Sie im daraufhin angezeigten Bestätigungsdialogfeld auf **Ja**.</span><span class="sxs-lookup"><span data-stu-id="47ee1-159">Click **Apply**, and in the confirmation box that appears, click **Yes**.</span></span>

11. <span data-ttu-id="47ee1-160">Klicken Sie auf der **Zusammenfassungs** Seite auf **Fertig stellen** , um den Assistenten zu beenden.</span><span class="sxs-lookup"><span data-stu-id="47ee1-160">On the **Summary** page, click **Finish** to quit the wizard</span></span>

**<span data-ttu-id="47ee1-161">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="47ee1-161">Note</span></span>**  
<span data-ttu-id="47ee1-162">Überprüfen Sie, ob die Gruppenrichtlinien die im Tool Voraussetzungen festgelegten obligatorischen Einstellungen nicht überschreiben.</span><span class="sxs-lookup"><span data-stu-id="47ee1-162">Verify that group policies do not overwrite the mandatory settings set in the prerequisites tool.</span></span>



## <a href="" id="bkmk-howtoconfiguremedvvirtualmachinemanualinstallationprerequisites"></a><span data-ttu-id="47ee1-163">So konfigurieren Sie die Voraussetzungen für die manuelle Installation von MED-V Virtual Machine</span><span class="sxs-lookup"><span data-stu-id="47ee1-163">How to Configure MED-V Virtual Machine Manual Installation Prerequisites</span></span>


<span data-ttu-id="47ee1-164">Einige Konfigurationen können nicht über das Voraussetzungen-Tool für virtuelle Maschinen konfiguriert werden und müssen manuell ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="47ee1-164">Several of the configurations cannot be configured through the virtual machine prerequisites tool and must be performed manually.</span></span>

-   <span data-ttu-id="47ee1-165">Einstellungen für den virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="47ee1-165">Virtual Machine Settings</span></span>

    <span data-ttu-id="47ee1-166">Es wird empfohlen, die folgenden Einstellungen für den virtuellen Computer in der Microsoft Virtual PC-Konsole zu konfigurieren:</span><span class="sxs-lookup"><span data-stu-id="47ee1-166">It is recommended to configure the following virtual machine settings in the Microsoft Virtual PC console:</span></span>

    -   <span data-ttu-id="47ee1-167">Deaktivieren von Diskettenlaufwerken</span><span class="sxs-lookup"><span data-stu-id="47ee1-167">Disable floppy disk drives.</span></span>

    -   <span data-ttu-id="47ee1-168">Deaktivieren Sie Undo-Disks (**Einstellungen &gt; Undo-Disks**).</span><span class="sxs-lookup"><span data-stu-id="47ee1-168">Disable undo-disks (**Settings &gt; undo-disks**).</span></span>

    -   <span data-ttu-id="47ee1-169">Stellen Sie sicher, dass das Bild nur einen virtuellen Prozessor aufweist.</span><span class="sxs-lookup"><span data-stu-id="47ee1-169">Ensure that the image has only one virtual CPU.</span></span>

    -   <span data-ttu-id="47ee1-170">Sie können die Interaktionen zwischen dem virtuellen Computer und dem Benutzer eliminieren, wenn diese nicht mit veröffentlichten Anwendungen verknüpft sind (beispielsweise Nachrichten, die Benutzereingaben erfordern).</span><span class="sxs-lookup"><span data-stu-id="47ee1-170">Eliminate interactions between the virtual machine and the user, where they are not related to published applications (such as, messages requiring user input).</span></span>

-   <span data-ttu-id="47ee1-171">Bildeinstellungen</span><span class="sxs-lookup"><span data-stu-id="47ee1-171">Image Settings</span></span>

    <span data-ttu-id="47ee1-172">Konfigurieren Sie die folgenden manuellen Einstellungen innerhalb des Bilds:</span><span class="sxs-lookup"><span data-stu-id="47ee1-172">Configure the following manual settings inside the image:</span></span>

    1.  <span data-ttu-id="47ee1-173">Deaktivieren Sie im Fenster **Eigenschaften von Energieoptionen** den Ruhezustand und den Ruhezustand.</span><span class="sxs-lookup"><span data-stu-id="47ee1-173">In the **Power Options Properties** window, disable hibernation and sleep.</span></span>

    2.  <span data-ttu-id="47ee1-174">Wenden Sie die neuesten Windows-Updates an.</span><span class="sxs-lookup"><span data-stu-id="47ee1-174">Apply the most recent Windows updates.</span></span>

    3.  <span data-ttu-id="47ee1-175">Deaktivieren Sie im Dialogfeld **Windows-Start und-Wiederherstellung** im Abschnitt **System Fehler** das Kontrollkästchen **automatisch neu starten** .</span><span class="sxs-lookup"><span data-stu-id="47ee1-175">In the **Windows Startup and Recovery** dialog box, in the **System Failure** section, clear the **Automatically restart** check box.</span></span>

    4.  <span data-ttu-id="47ee1-176">Stellen Sie sicher, dass das Bild einen VLK-Lizenzschlüssel verwendet.</span><span class="sxs-lookup"><span data-stu-id="47ee1-176">Ensure that the image uses a VLK license key.</span></span>

-   <span data-ttu-id="47ee1-177">Installieren von VPC-Ergänzungen</span><span class="sxs-lookup"><span data-stu-id="47ee1-177">Installing VPC Additions</span></span>

    <span data-ttu-id="47ee1-178">Klicken Sie im Menü **Aktion** auf **Virtual Machine Additions installieren oder aktualisieren**.</span><span class="sxs-lookup"><span data-stu-id="47ee1-178">On the **Action** menu, select **Install or Update Virtual Machine Additions**.</span></span>

-   <span data-ttu-id="47ee1-179">Konfigurieren des Drucks</span><span class="sxs-lookup"><span data-stu-id="47ee1-179">Configuring Printing</span></span>

    <span data-ttu-id="47ee1-180">Sie können den Druck aus dem MED-V-Arbeitsbereich auf eine der folgenden Arten konfigurieren:</span><span class="sxs-lookup"><span data-stu-id="47ee1-180">You can configure printing from the MED-V workspace in either of the following ways:</span></span>

    -   <span data-ttu-id="47ee1-181">Fügen Sie dem virtuellen Computer einen Drucker hinzu.</span><span class="sxs-lookup"><span data-stu-id="47ee1-181">Add a printer to the virtual machine.</span></span>

    -   <span data-ttu-id="47ee1-182">Drucken mit Druckern zulassen, die auf dem Hostcomputer konfiguriert sind.</span><span class="sxs-lookup"><span data-stu-id="47ee1-182">Allow printing with printers that are configured on the host computer.</span></span>

## <a href="" id="bkmk-howtoconfiguresysprepformedvimages"></a><span data-ttu-id="47ee1-183">Konfigurieren von Sysprep für MED-V-Bilder</span><span class="sxs-lookup"><span data-stu-id="47ee1-183">How to Configure Sysprep for MED-V Images</span></span>


<span data-ttu-id="47ee1-184">In einem Med-v-Arbeitsbereich kann Sysprep so konfiguriert werden, dass eine eindeutige Sicherheits-ID (SID) zugewiesen wird, insbesondere dann, wenn mehrere med-v-Arbeitsbereiche auf einem einzelnen Computer ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="47ee1-184">In a MED-V workspace, Sysprep can be configured in order to assign unique security ID (SID), particularly when multiple MED-V workspaces are run on a single computer.</span></span> <span data-ttu-id="47ee1-185">Es wird nicht empfohlen, Sysprep für die Teilnahme an einer Domäne zu verwenden. Verwenden Sie stattdessen die Aktion MED-V Join-Domänen Skript, wie unter [so wird es gemacht: Einrichten von Skriptaktionen](how-to-set-up-script-actions.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="47ee1-185">It is not recommended to use Sysprep to join a domain; instead, use the MED-V join domain script action as described in [How to Set Up Script Actions](how-to-set-up-script-actions.md).</span></span>

**<span data-ttu-id="47ee1-186">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="47ee1-186">Note</span></span>**  
<span data-ttu-id="47ee1-187">Sysprep ist das Microsoft-System Vorbereitungs Dienstprogramm für das Windows-Betriebssystem.</span><span class="sxs-lookup"><span data-stu-id="47ee1-187">Sysprep is Microsoft's system preparation utility for the Windows operating system.</span></span>



**<span data-ttu-id="47ee1-188">So konfigurieren Sie Sysprep in einem MED-V-Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="47ee1-188">To configure Sysprep in a MED-V workspace</span></span>**

1.  <span data-ttu-id="47ee1-189">Erstellen Sie ein Verzeichnis im Stammverzeichnis des Systemlaufwerks mit dem Namen *Sysprep*.</span><span class="sxs-lookup"><span data-stu-id="47ee1-189">Create a directory in the root of the system drive named *Sysprep*.</span></span>

2.  <span data-ttu-id="47ee1-190">Extrahieren Sie auf der Windows-Installations-CD *deploy.cab* auf das Stammverzeichnis des Systemlaufwerks, oder laden Sie das neueste Update zur Bereitstellungs Tools von der Microsoft-Website herunter.</span><span class="sxs-lookup"><span data-stu-id="47ee1-190">From the Windows installation CD, extract *deploy.cab* to the root of the system drive, or download the latest Deployment Tools update from the Microsoft Web site.</span></span>

    -   <span data-ttu-id="47ee1-191">Informationen zu Windows 2000 finden Sie unter [Bereitstellungs Tools-Update für Windows 2000](https://go.microsoft.com/fwlink/?LinkId=143001).</span><span class="sxs-lookup"><span data-stu-id="47ee1-191">For Windows 2000, see [Deployment Tools update for Windows 2000](https://go.microsoft.com/fwlink/?LinkId=143001).</span></span>

    -   <span data-ttu-id="47ee1-192">Unter Windows XP finden Sie unter [Bereitstellungs Tools-Update für Windows XP](https://go.microsoft.com/fwlink/?LinkId=143000).</span><span class="sxs-lookup"><span data-stu-id="47ee1-192">For Windows XP, see [Deployment Tools update for Windows XP](https://go.microsoft.com/fwlink/?LinkId=143000).</span></span>

3.  <span data-ttu-id="47ee1-193">Führen Sie den **Setup-Manager** (setupmgr.exe) aus.</span><span class="sxs-lookup"><span data-stu-id="47ee1-193">Run **Setup Manager** (setupmgr.exe).</span></span>

4.  <span data-ttu-id="47ee1-194">Folgen Sie dem Setup-Manager-Assistenten.</span><span class="sxs-lookup"><span data-stu-id="47ee1-194">Follow the Setup Manager wizard.</span></span>

<span data-ttu-id="47ee1-195">Nachdem Sysprep konfiguriert und der MED-V-Arbeitsbereich erstellt wurde, muss Sysprep ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="47ee1-195">After Sysprep is configured and the MED-V workspace is created, Sysprep must be executed.</span></span>

**<span data-ttu-id="47ee1-196">So führen Sie Sysprep aus</span><span class="sxs-lookup"><span data-stu-id="47ee1-196">To run Sysprep</span></span>**

1.  <span data-ttu-id="47ee1-197">Führen Sie aus dem Ordner "Sysprep", der sich im Stammverzeichnis des Systemlaufwerks befindet, das System Vorbereitungs Tool (Sysprep.exe) aus.</span><span class="sxs-lookup"><span data-stu-id="47ee1-197">From the Sysprep folder located in the root of the system drive, run the System Preparation Tool (Sysprep.exe).</span></span>

2.  <span data-ttu-id="47ee1-198">Klicken Sie im daraufhin angezeigten warnmeldungsfeld auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="47ee1-198">In the warning message box that appears, click **OK**.</span></span>

3.  <span data-ttu-id="47ee1-199">Aktivieren Sie im Dialogfeld **Sysprep-Eigenschaften** die Kontrollkästchen **Kulanzzeitraum nicht zurücksetzen für Aktivierung** und **Mini-Setup verwenden** .</span><span class="sxs-lookup"><span data-stu-id="47ee1-199">In the **Sysprep Properties** dialog box, select the **Don't reset grace period for activation** and **Use Mini-Setup** check boxes.</span></span>

4.  <span data-ttu-id="47ee1-200">Klicken Sie auf erneut **versiegeln**.</span><span class="sxs-lookup"><span data-stu-id="47ee1-200">Click **Reseal**.</span></span>

5.  <span data-ttu-id="47ee1-201">Wenn Sie mit den Informationen, die im angezeigten Bestätigungsdialogfeld aufgeführt sind, nicht zufrieden sind, klicken Sie auf **Abbrechen** , und ändern Sie die Auswahl.</span><span class="sxs-lookup"><span data-stu-id="47ee1-201">If you are not satisfied with the information listed in the confirmation message box that appears, click **Cancel** and change the selections.</span></span>

6.  <span data-ttu-id="47ee1-202">Klicken Sie auf **OK** , um den System Vorbereitungsvorgang abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="47ee1-202">Click **OK** to complete the system preparation process.</span></span>

## <a href="" id="bkmk-turningoffmicrosoftvirtualpc"></a><span data-ttu-id="47ee1-203">Deaktivieren von Microsoft Virtual PC</span><span class="sxs-lookup"><span data-stu-id="47ee1-203">Turning Off Microsoft Virtual PC</span></span>


<span data-ttu-id="47ee1-204">Nachdem alle Komponenten installiert und konfiguriert sind, schließen Sie Microsoft Virtual PC, und wählen Sie **Deaktivieren aus**.</span><span class="sxs-lookup"><span data-stu-id="47ee1-204">After all the components are installed and configured, close Microsoft Virtual PC and select **Turn Off**.</span></span>

## <span data-ttu-id="47ee1-205">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="47ee1-205">Related topics</span></span>


<span data-ttu-id="47ee1-206">Erstellen eines MED-V-Bilds [so wird es gemacht: Einrichten von Skriptaktionen](how-to-set-up-script-actions.md)</span><span class="sxs-lookup"><span data-stu-id="47ee1-206">Creating a MED-V Image [How to Set Up Script Actions](how-to-set-up-script-actions.md)</span></span>









