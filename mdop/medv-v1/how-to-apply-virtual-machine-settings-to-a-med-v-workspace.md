---
title: So wenden Sie die Einstellungen des virtuellen Computers auf einen MED-V-Arbeitsbereich an
description: So wenden Sie die Einstellungen des virtuellen Computers auf einen MED-V-Arbeitsbereich an
author: dansimp
ms.assetid: b50d0dfb-8d61-4543-9607-a29bbb1ed45f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9662bb8202285d51971eeea8beaef938b98ed6b0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811476"
---
# <span data-ttu-id="d0ca7-103">So wenden Sie die Einstellungen des virtuellen Computers auf einen MED-V-Arbeitsbereich an</span><span class="sxs-lookup"><span data-stu-id="d0ca7-103">How to Apply Virtual Machine Settings to a MED-V Workspace</span></span>


<span data-ttu-id="d0ca7-104">Jedem MED-V-Arbeitsbereich muss ein Microsoft Virtual PC-Abbild zugeordnet sein.</span><span class="sxs-lookup"><span data-stu-id="d0ca7-104">Every MED-V workspace must have a Microsoft Virtual PC image associated with it.</span></span> <span data-ttu-id="d0ca7-105">Mit den Einstellungen für den virtuellen Computer können Sie ein virtuelles PC-Abbild zuweisen und andere Eigenschaften des virtuellen Computers festlegen.</span><span class="sxs-lookup"><span data-stu-id="d0ca7-105">The virtual machine settings enable you to assign a Virtual PC image as well as set other virtual machine properties.</span></span>

<span data-ttu-id="d0ca7-106">Alle Einstellungen für den virtuellen Computer werden im **Richtlinien** Modul auf der Registerkarte **Einstellungen für virtuelle Computer** konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="d0ca7-106">All virtual machine settings are configured in the **Policy** module, on the **Virtual Machine Settings** tab.</span></span>

**<span data-ttu-id="d0ca7-107">So wenden Sie Einstellungen für virtuelle Computer auf einen MED-V-Arbeitsbereich an</span><span class="sxs-lookup"><span data-stu-id="d0ca7-107">To apply virtual machine settings to a MED-V workspace</span></span>**

1.  <span data-ttu-id="d0ca7-108">Klicken Sie auf den MED-V-Arbeitsbereich, den Sie konfigurieren möchten.</span><span class="sxs-lookup"><span data-stu-id="d0ca7-108">Click the MED-V workspace to configure.</span></span>

2.  <span data-ttu-id="d0ca7-109">Konfigurieren Sie die Eigenschaften des virtuellen Computers wie in der folgenden Tabelle beschrieben.</span><span class="sxs-lookup"><span data-stu-id="d0ca7-109">Configure the virtual machine properties as described in the following table.</span></span>

3.  <span data-ttu-id="d0ca7-110">Wählen Sie im Menü **Richtlinie** die Option **Commit**aus.</span><span class="sxs-lookup"><span data-stu-id="d0ca7-110">On the **Policy** menu, select **Commit**.</span></span>

**<span data-ttu-id="d0ca7-111">Eigenschaften von virtuellen Computern</span><span class="sxs-lookup"><span data-stu-id="d0ca7-111">Virtual Machine Properties</span></span>**

<span data-ttu-id="d0ca7-112">Eigenschaften Beschreibung *Einstellungen für den virtuellen Computer*</span><span class="sxs-lookup"><span data-stu-id="d0ca7-112">Property Description *Virtual Machine Settings*</span></span>

<span data-ttu-id="d0ca7-113">Zugewiesenes Bild</span><span class="sxs-lookup"><span data-stu-id="d0ca7-113">Assigned Image</span></span>

<span data-ttu-id="d0ca7-114">Das tatsächliche Microsoft Virtual PC-Abbild, das dem MED-V-Arbeitsbereich zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="d0ca7-114">The actual Microsoft Virtual PC image assigned to the MED-V workspace.</span></span> <span data-ttu-id="d0ca7-115">Das Menü enthält eine Liste aller verfügbaren Virtual PC-Bilder.</span><span class="sxs-lookup"><span data-stu-id="d0ca7-115">The menu provides a list of all available Virtual PC images.</span></span> <span data-ttu-id="d0ca7-116">Die folgenden Bildtypen befinden sich in der Liste der **aktiven** Bilder:</span><span class="sxs-lookup"><span data-stu-id="d0ca7-116">The following image types are in the **Active** image list:</span></span>

-   <span data-ttu-id="d0ca7-117">**Lokale Testbilder**– Bilder auf dem lokalen Computer, die noch nicht gepackt sind.</span><span class="sxs-lookup"><span data-stu-id="d0ca7-117">**Local test images**—Images on the local computer that are not yet packed.</span></span> <span data-ttu-id="d0ca7-118">Auf diese Bild Namen folgt das Wort "Test" in Klammern (Test) und dient nur zu Testzwecken.</span><span class="sxs-lookup"><span data-stu-id="d0ca7-118">These image names are followed by the word “test” in parentheses (test) and are for testing purposes only.</span></span>

-   <span data-ttu-id="d0ca7-119">**Lokal verpackte Bilder**– komprimierte Bilder auf dem lokalen Computer.</span><span class="sxs-lookup"><span data-stu-id="d0ca7-119">**Local packed images**—Packed images on the local computer.</span></span> <span data-ttu-id="d0ca7-120">Auf diese Bilder folgt das Wort "local" in Klammern (lokal) und kann nicht von Clients heruntergeladen werden, bis der Administrator Sie auf den Server hochgeladen hat.</span><span class="sxs-lookup"><span data-stu-id="d0ca7-120">These images are followed by the word “local” in parentheses (local) and cannot be downloaded by clients until the administrator uploads them to the server.</span></span>

    <span data-ttu-id="d0ca7-121">Ein lokales Bild kann ausgewählt werden, wenn Sie ein Paket erstellen, das über Wechselmedien (wie USB oder DVD) an den Client verteilt wird.</span><span class="sxs-lookup"><span data-stu-id="d0ca7-121">A local image can be selected if you are creating a package that will be distributed to the client via removable media (such as USB or DVD).</span></span>

-   <span data-ttu-id="d0ca7-122">**Komprimierte Bilder auf dem Server**– Bilder auf dem Server, die von Clients heruntergeladen werden können.</span><span class="sxs-lookup"><span data-stu-id="d0ca7-122">**Packed images on server**—Images that are on the server and are available for download by clients.</span></span> <span data-ttu-id="d0ca7-123">Klicken Sie auf aktualisieren, um die Liste Bilder zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="d0ca7-123">Click Refresh to refresh the images list.</span></span>

    <span data-ttu-id="d0ca7-124">**Hinweis**  Jedes MED-V Workspace-Bild kann nur von einem Windows-Benutzer verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d0ca7-124">**Note** Each MED-V workspace image can only be used by one Windows user.</span></span>

     

<span data-ttu-id="d0ca7-125">Arbeitsbereich ist persistent</span><span class="sxs-lookup"><span data-stu-id="d0ca7-125">Workspace is persistent</span></span>

<span data-ttu-id="d0ca7-126">Aktivieren Sie dieses Kontrollkästchen, um den MED-V-Arbeitsbereich als persistent zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="d0ca7-126">Select this check box to configure the MED-V workspace as persistent.</span></span> <span data-ttu-id="d0ca7-127">Wenn der Med-v-Arbeitsbereich in einem beständigen Med-v-Arbeitsbereich beendet wird, werden Änderungen und Ergänzungen des Med-v-Arbeitsbereichs im Med-v-Arbeitsbereich gespeichert.</span><span class="sxs-lookup"><span data-stu-id="d0ca7-127">In a persistent MED-V workspace, when the MED-V workspace is stopped, changes and additions to the MED-V workspace are saved in the MED-V workspace.</span></span>

<span data-ttu-id="d0ca7-128">Bei einem Domänen-MED-V-Arbeitsbereich muss diese Option ausgewählt sein.</span><span class="sxs-lookup"><span data-stu-id="d0ca7-128">For a Domain MED-V workspace, this option must be selected.</span></span>

<span data-ttu-id="d0ca7-129">**Hinweis**  Diese Einstellung sollte nicht geändert werden, nachdem ein MED-V-Arbeitsbereich für Benutzer bereitgestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="d0ca7-129">**Note** This setting should not be changed after a MED-V workspace is deployed to users.</span></span>

 

<span data-ttu-id="d0ca7-130">Beenden des virtuellen Computers beim Beenden des Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="d0ca7-130">Shut down the VM when stopping the Workspace</span></span>

<span data-ttu-id="d0ca7-131">Aktivieren Sie dieses Kontrollkästchen, um den virtuellen Computer zu beenden, wenn Sie den MED-V-Arbeitsbereich beenden.</span><span class="sxs-lookup"><span data-stu-id="d0ca7-131">Select this check box to shut down the virtual machine when stopping the MED-V workspace.</span></span> <span data-ttu-id="d0ca7-132">Wenn dieses Kontrollkästchen deaktiviert ist, wird nach Abschluss jeder Sitzung der virtuelle Computer nicht heruntergefahren, sondern stattdessen wird eine Momentaufnahme des virtuellen Computers erstellt.</span><span class="sxs-lookup"><span data-stu-id="d0ca7-132">If this check box is cleared, at the completion of each session, the virtual machine is not shut down but instead takes a snapshot of the virtual machine.</span></span> <span data-ttu-id="d0ca7-133">Nach dem Initiieren einer neuen Sitzung beginnt Windows mit dem Snapshot (das heißt, Windows wird nicht neu gestartet, und es ist keine Anmeldung erforderlich).</span><span class="sxs-lookup"><span data-stu-id="d0ca7-133">Upon the initiation of a new session, Windows starts from the snapshot (that is, Windows does not restart and no login is required).</span></span>

<span data-ttu-id="d0ca7-134">**Hinweis**  Diese Eigenschaft ist nur aktiviert, wenn " **Arbeitsbereich ist persistent** " ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="d0ca7-134">**Note** This property is enabled only if **Workspace is persistent** is selected.</span></span>

 

<span data-ttu-id="d0ca7-135">Anmelden bei Windows in VM mithilfe von MED-V-Anmeldeinformationen (SSO)</span><span class="sxs-lookup"><span data-stu-id="d0ca7-135">Logon to Windows in VM using MED-V credentials (SSO)</span></span>

<span data-ttu-id="d0ca7-136">Aktivieren Sie dieses Kontrollkästchen, um sich bei Windows auf dem virtuellen Computer mit den Med-v-Anmeldeinformationen anzumelden, die bei der Anmeldung bei Med-v-Client eingegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="d0ca7-136">Select this check box to log in to Windows on the virtual machine by using the MED-V credentials entered when logging in to MED-V client.</span></span>

<span data-ttu-id="d0ca7-137">**Hinweis**  Diese Eigenschaft ist nur aktiviert, wenn " **Arbeitsbereich ist persistent** " ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="d0ca7-137">**Note** This property is enabled only when **Workspace is persistent** is selected.</span></span>

 

<span data-ttu-id="d0ca7-138">Arbeitsbereich ist revertible</span><span class="sxs-lookup"><span data-stu-id="d0ca7-138">Workspace is revertible</span></span>

<span data-ttu-id="d0ca7-139">Aktivieren Sie dieses Kontrollkästchen, um den MED-V-Arbeitsbereich als revertible zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="d0ca7-139">Select this check box to configure the MED-V workspace as revertible.</span></span> <span data-ttu-id="d0ca7-140">In einem revertible Med-v-Arbeitsbereich wird nach Abschluss jeder Sitzung (d. h., wenn der Benutzer den Med-v-Arbeitsbereich beendet) der Med-v-Arbeitsbereich auf den ursprünglichen Zustand zurückgesetzt, in dem er sich während der Bereitstellung befand.</span><span class="sxs-lookup"><span data-stu-id="d0ca7-140">In a revertible MED-V workspace, at the completion of each session (that is, when the user stops the MED-V workspace), the MED-V workspace reverts to the original state it was in during deployment.</span></span> <span data-ttu-id="d0ca7-141">Keine Änderungen oder Ergänzungen, die der Benutzer vorgenommen hat, werden im MED-V-Arbeitsbereich zwischen Sitzungen gespeichert.</span><span class="sxs-lookup"><span data-stu-id="d0ca7-141">No changes or additions that the user made are saved on the MED-V workspace between sessions.</span></span>

<span data-ttu-id="d0ca7-142">**Hinweis**  Diese Einstellung sollte nicht geändert werden, nachdem ein MED-V-Arbeitsbereich für Benutzer bereitgestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="d0ca7-142">**Note** This setting should not be changed after a MED-V workspace is deployed to users.</span></span>

 

<span data-ttu-id="d0ca7-143">Synchronisieren der Arbeitsbereichs Zeitzone mit dem Host</span><span class="sxs-lookup"><span data-stu-id="d0ca7-143">Synchronize Workspace time zone with host</span></span>

<span data-ttu-id="d0ca7-144">Aktivieren Sie dieses Kontrollkästchen, um die Zeitzone im MED-V-Arbeitsbereich mit dem Host zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="d0ca7-144">Select this check box to synchronize the time zone in the MED-V workspace with the host.</span></span>

<span data-ttu-id="d0ca7-145">Die Synchronisierung funktioniert unterschiedlich, je nachdem, ob der MED-V-Arbeitsbereich persistent oder revertible ist, wie im folgenden beschrieben:</span><span class="sxs-lookup"><span data-stu-id="d0ca7-145">The synchronization works differently depending on whether the MED-V workspace is persistent or revertible, as follows:</span></span>

-   <span data-ttu-id="d0ca7-146">In einem beständigen MED-V-Arbeitsbereich versucht die Zeitzone zunächst, mit dem Server zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="d0ca7-146">In a persistent MED-V workspace, the time zone first tries to synchronize with the server.</span></span> <span data-ttu-id="d0ca7-147">Wenn das fehlschlägt, wird es mit dem Host synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="d0ca7-147">If that fails, it synchronizes with the host.</span></span>

-   <span data-ttu-id="d0ca7-148">In einem revertible MED-V-Arbeitsbereich wird die Zeitzone mit dem Host synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="d0ca7-148">In a revertible MED-V workspace, the time zone synchronizes with the host.</span></span>

*<span data-ttu-id="d0ca7-149">Einstellungen sperren</span><span class="sxs-lookup"><span data-stu-id="d0ca7-149">Lock Settings</span></span>*

<span data-ttu-id="d0ca7-150">Sperren des Arbeitsbereichs im Host-Standby/Hibernate-Ereignis</span><span class="sxs-lookup"><span data-stu-id="d0ca7-150">Lock the Workspace on host standby/hibernate event</span></span>

<span data-ttu-id="d0ca7-151">Aktivieren Sie dieses Kontrollkästchen, um den MED-V-Arbeitsbereich automatisch zu sperren, wenn der Hostcomputer in den Standbymodus oder Ruhezustand wechselt.</span><span class="sxs-lookup"><span data-stu-id="d0ca7-151">Select this check box to automatically lock the MED-V workspace when the host computer goes into standby or hibernate.</span></span>

<span data-ttu-id="d0ca7-152">Sperren des Arbeitsbereichs nach</span><span class="sxs-lookup"><span data-stu-id="d0ca7-152">Lock the Workspace after</span></span>

<span data-ttu-id="d0ca7-153">Aktivieren Sie dieses Kontrollkästchen, um den Med-v-Arbeitsbereich zu sperren, wenn sich der Med-v-Arbeitsbereich für einen bestimmten Zeitraum im Leerlauf befindet.</span><span class="sxs-lookup"><span data-stu-id="d0ca7-153">Select this check box to lock the MED-V workspace when the MED-V workspace is idle for a specified period of time.</span></span> <span data-ttu-id="d0ca7-154">Wenn diese Option ausgewählt ist, ist das Feld Zahl aktiviert.</span><span class="sxs-lookup"><span data-stu-id="d0ca7-154">When selected, the number box is enabled.</span></span> <span data-ttu-id="d0ca7-155">Geben Sie die Anzahl der Minuten der Leerlaufzeit ein, bevor Sie den MED-V-Arbeitsbereich sperren.</span><span class="sxs-lookup"><span data-stu-id="d0ca7-155">Enter the number of minutes of idle time before locking the MED-V workspace.</span></span>

<span data-ttu-id="d0ca7-156">**Hinweis**  Die Leerlaufzeit bezieht sich auf die MED-V Workspace-Anwendungen (nicht auf die Hostanwendungen).</span><span class="sxs-lookup"><span data-stu-id="d0ca7-156">**Note** The idle time refers to the MED-V workspace applications (not the host applications).</span></span>

 

*<span data-ttu-id="d0ca7-157">Bild Aktualisierungseinstellungen</span><span class="sxs-lookup"><span data-stu-id="d0ca7-157">Image Update Settings</span></span>*

<span data-ttu-id="d0ca7-158">Nur beibehalten</span><span class="sxs-lookup"><span data-stu-id="d0ca7-158">Keep only</span></span>

<span data-ttu-id="d0ca7-159">Aktivieren Sie dieses Kontrollkästchen, um die Anzahl der alten Bildversionen zu begrenzen, die beibehalten werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d0ca7-159">Select this check box to limit the number of old image versions to keep.</span></span>

<span data-ttu-id="d0ca7-160">Wenn diese Option ausgewählt ist, ist das Feld Zahl aktiviert.</span><span class="sxs-lookup"><span data-stu-id="d0ca7-160">When selected, the number box is enabled.</span></span> <span data-ttu-id="d0ca7-161">Geben Sie die Anzahl der alten Versionen ein, die Sie beibehalten möchten.</span><span class="sxs-lookup"><span data-stu-id="d0ca7-161">Enter the number of old versions to keep.</span></span>

<span data-ttu-id="d0ca7-162">Update vorschlagen, wenn eine neue Version verfügbar ist</span><span class="sxs-lookup"><span data-stu-id="d0ca7-162">Suggest update when a new version is available</span></span>

<span data-ttu-id="d0ca7-163">Aktivieren Sie dieses Kontrollkästchen, wenn Sie ein Update vorschlagen (aber nicht erzwingen) möchten, wenn eine neue Version des Bilds verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="d0ca7-163">Select this check box to suggest (but not force) an update when a new version of the image is available.</span></span>

<span data-ttu-id="d0ca7-164">Clients sollten Trim-Übertragung beim Herunterladen von Bildern für diesen Arbeitsbereich verwenden.</span><span class="sxs-lookup"><span data-stu-id="d0ca7-164">Clients should use Trim Transfer when downloading images for this Workspace</span></span>

<span data-ttu-id="d0ca7-165">Aktivieren Sie dieses Kontrollkästchen, um die Trimm Übertragung zu aktivieren (Weitere Informationen finden Sie unter [Med-v Trim Transfer Technology](med-v-trim-transfer-technology-medvv2.md)) beim Herunterladen von Bildern, die diesem Med-v-Arbeitsbereich zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="d0ca7-165">Select this check box to enable Trim Transfer (for more information, see [MED-V Trim Transfer Technology](med-v-trim-transfer-technology-medvv2.md)) when downloading images associated with this MED-V workspace.</span></span> <span data-ttu-id="d0ca7-166">Wenn dieses Kontrollkästchen deaktiviert ist, wird das vollständige Bild heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="d0ca7-166">If this check box is cleared, the full image will be downloaded.</span></span>

<span data-ttu-id="d0ca7-167">**Hinweis**  Bei der Trimm Übertragung muss die Festplatte indiziert werden, was viel Zeit in Anspruch nehmen kann.</span><span class="sxs-lookup"><span data-stu-id="d0ca7-167">**Note** Trim Transfer requires indexing the hard drive, which might take a considerable amount of time.</span></span> <span data-ttu-id="d0ca7-168">Es wird empfohlen, die Trim-Übertragung zu verwenden, wenn die Indizierung der Festplatte effizienter als das Herunterladen der neuen Bildversion ist, beispielsweise beim Herunterladen einer Bildversion, die mit der vorhandenen Version vergleichbar ist.</span><span class="sxs-lookup"><span data-stu-id="d0ca7-168">It is recommended to use Trim Transfer when indexing the hard drive is more efficient than downloading the new image version, such as when downloading an image version that is similar to the existing version.</span></span>

 

 

## <span data-ttu-id="d0ca7-169">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="d0ca7-169">Related topics</span></span>


[<span data-ttu-id="d0ca7-170">Erstellen eines MED-V-Images</span><span class="sxs-lookup"><span data-stu-id="d0ca7-170">Creating a MED-V Image</span></span>](creating-a-med-v-image.md)

[<span data-ttu-id="d0ca7-171">Über die Benutzeroberfläche der MED-V-Management-Konsole</span><span class="sxs-lookup"><span data-stu-id="d0ca7-171">Using the MED-V Management Console User Interface</span></span>](using-the-med-v-management-console-user-interface.md)

[<span data-ttu-id="d0ca7-172">Erstellen eines MED-V-Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="d0ca7-172">Creating a MED-V Workspace</span></span>](creating-a-med-v-workspacemedv-10-sp1.md)

 

 





