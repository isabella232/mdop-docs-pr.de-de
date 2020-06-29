---
title: So konfigurieren Sie einen Domänenbenutzer oder eine Gruppe
description: So konfigurieren Sie einen Domänenbenutzer oder eine Gruppe
author: dansimp
ms.assetid: 055aba81-a9c9-4b98-969d-775e603becf3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4c51da13808df657c1341572767c24860d9d5e8b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812211"
---
# <span data-ttu-id="3bb7c-103">So konfigurieren Sie einen Domänenbenutzer oder eine Gruppe</span><span class="sxs-lookup"><span data-stu-id="3bb7c-103">How to Configure a Domain User or Group</span></span>


<span data-ttu-id="3bb7c-104">Die Bereitstellungseinstellungen ermöglichen Ihnen, zu steuern, welche Benutzer oder Gruppen auf den Med-v-Arbeitsbereich zugreifen können, sowie, wie lange der Med-v-Arbeitsbereich genutzt werden kann und ob er offline verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="3bb7c-104">The deployment settings enable you to control which users or groups can access the MED-V workspace, as well as how long the MED-V workspace can be utilized and whether it can be used offline.</span></span> <span data-ttu-id="3bb7c-105">Sie können auch zusätzliche Regeln konfigurieren, um den Zugriff zwischen dem MED-V-Arbeitsbereich und dem Host zu steuern.</span><span class="sxs-lookup"><span data-stu-id="3bb7c-105">You can also configure additional rules to control access between the MED-V workspace and the host.</span></span>

<span data-ttu-id="3bb7c-106">Alle Berechtigungen des MED-V-Arbeitsbereichs sind im **Richtlinien** Modul auf der Registerkarte **Bereitstellung** konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="3bb7c-106">All MED-V workspace permissions are configured in the **Policy** module, on the **Deployment** tab.</span></span>

<span data-ttu-id="3bb7c-107">Damit Benutzer den Med-v-Arbeitsbereich verwenden können, müssen Sie zunächst Domänenbenutzer oder-Gruppen zu den Med-v Workspace-Berechtigungen hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="3bb7c-107">To allow users to utilize the MED-V workspace, you must first add domain users or groups to the MED-V workspace permissions.</span></span> <span data-ttu-id="3bb7c-108">Sie können dann Berechtigungen für jeden Benutzer oder jede Gruppe einstellen.</span><span class="sxs-lookup"><span data-stu-id="3bb7c-108">You can then set permissions for each user or group.</span></span>

## <span data-ttu-id="3bb7c-109">Hinzufügen eines Domänenbenutzers oder einer Gruppe</span><span class="sxs-lookup"><span data-stu-id="3bb7c-109">How to Add a Domain User or Group</span></span>


**<span data-ttu-id="3bb7c-110">So fügen Sie einen Domänenbenutzer oder eine Gruppe hinzu</span><span class="sxs-lookup"><span data-stu-id="3bb7c-110">To add a domain user or group</span></span>**

1.  <span data-ttu-id="3bb7c-111">Klicken Sie im Fenster **Benutzer/Gruppen** auf **hinzufügen.**</span><span class="sxs-lookup"><span data-stu-id="3bb7c-111">In the **Users / Groups** window, click **Add.**</span></span>

2.  <span data-ttu-id="3bb7c-112">Wählen Sie im Dialogfeld **Benutzer-oder Gruppennamen eingeben** eine der folgenden Aktionen aus:</span><span class="sxs-lookup"><span data-stu-id="3bb7c-112">In the **Enter User or Group names** dialog box, select domain users or groups by doing one of the following:</span></span>

    -   <span data-ttu-id="3bb7c-113">Geben Sie im Feld **Benutzer-oder Gruppennamen eingeben** einen Benutzer oder eine Gruppe ein, der in der Domäne oder als lokaler Benutzer oder eine Gruppe auf dem Computer vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="3bb7c-113">In the **Enter User or Group names** field, type a user or group that exists in the domain or as a local user or group on the computer.</span></span> <span data-ttu-id="3bb7c-114">Klicken Sie dann auf **Namen überprüfen** , um Sie in den vollständigen vorhandenen Namen aufzulösen.</span><span class="sxs-lookup"><span data-stu-id="3bb7c-114">Then click **Check Names** to resolve it to the full existent name.</span></span>

    -   <span data-ttu-id="3bb7c-115">Klicken Sie auf **Suchen** , um das Dialogfeld **Benutzer oder Gruppen Standard auswählen** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="3bb7c-115">Click **Find** to open the standard **Select Users or Groups** dialog box.</span></span> <span data-ttu-id="3bb7c-116">Wählen Sie dann Domänenbenutzer oder Gruppen aus.</span><span class="sxs-lookup"><span data-stu-id="3bb7c-116">Then select domain users or groups.</span></span>

3.  <span data-ttu-id="3bb7c-117">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="3bb7c-117">Click **OK**.</span></span>

    <span data-ttu-id="3bb7c-118">Die Domänenbenutzer oder-Gruppen werden hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3bb7c-118">The domain users or groups are added.</span></span>

    **<span data-ttu-id="3bb7c-119">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="3bb7c-119">Note</span></span>**  
    <span data-ttu-id="3bb7c-120">Benutzer aus vertrauenswürdigen Domänen sollten manuell hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="3bb7c-120">Users from trusted domains should be added manually.</span></span>



~~~
**Warning**  
Do not run the management application from a computer that is part of a domain that is not trusted by the domain the server is installed on.
~~~



## <span data-ttu-id="3bb7c-121">Entfernen eines Domänenbenutzers oder einer Gruppe</span><span class="sxs-lookup"><span data-stu-id="3bb7c-121">How to Remove a Domain User or Group</span></span>


**<span data-ttu-id="3bb7c-122">So entfernen Sie einen Domänenbenutzer oder eine Gruppe</span><span class="sxs-lookup"><span data-stu-id="3bb7c-122">To remove a domain user or group</span></span>**

1.  <span data-ttu-id="3bb7c-123">Wählen Sie im Fenster **Benutzer/Gruppen** einen Benutzer oder eine Gruppe aus.</span><span class="sxs-lookup"><span data-stu-id="3bb7c-123">In the **Users / Groups** window, select a user or group.</span></span>

2.  <span data-ttu-id="3bb7c-124">Klicken Sie auf **Entfernen**.</span><span class="sxs-lookup"><span data-stu-id="3bb7c-124">Click **Remove**.</span></span>

    <span data-ttu-id="3bb7c-125">Der Benutzer oder die Gruppe wird gelöscht.</span><span class="sxs-lookup"><span data-stu-id="3bb7c-125">The user or group is deleted.</span></span>

## <span data-ttu-id="3bb7c-126">Einrichten von Berechtigungen für einen Benutzer oder eine Gruppe</span><span class="sxs-lookup"><span data-stu-id="3bb7c-126">How to Set Permissions for a User or a Group</span></span>


**<span data-ttu-id="3bb7c-127">So setzen Sie Berechtigungen für einen Benutzer oder eine Gruppe</span><span class="sxs-lookup"><span data-stu-id="3bb7c-127">To set permissions for a user or a group</span></span>**

1.  <span data-ttu-id="3bb7c-128">Klicken Sie auf den Benutzer oder die Gruppe, für den Sie die Berechtigungen festlegen möchten.</span><span class="sxs-lookup"><span data-stu-id="3bb7c-128">Click the user or group for which you are setting the permissions.</span></span>

2.  <span data-ttu-id="3bb7c-129">Konfigurieren Sie die MED-V Workspace-Eigenschaften wie in der folgenden Tabelle beschrieben.</span><span class="sxs-lookup"><span data-stu-id="3bb7c-129">Configure the MED-V workspace properties as described in the following table.</span></span>

3.  <span data-ttu-id="3bb7c-130">Wählen Sie im Menü **Richtlinie** die Option **Commit**aus.</span><span class="sxs-lookup"><span data-stu-id="3bb7c-130">On the **Policy** menu, select **Commit**.</span></span>

**<span data-ttu-id="3bb7c-131">Arbeitsbereichs Bereitstellungseigenschaften</span><span class="sxs-lookup"><span data-stu-id="3bb7c-131">Workspace Deployment Properties</span></span>**

<span data-ttu-id="3bb7c-132">Eigenschaftsbeschreibung *Allgemein*</span><span class="sxs-lookup"><span data-stu-id="3bb7c-132">Property Description *General*</span></span>

<span data-ttu-id="3bb7c-133">Arbeitsbereich für &lt; Benutzer oder Gruppen aktivieren&gt;</span><span class="sxs-lookup"><span data-stu-id="3bb7c-133">Enable Workspace for &lt;user or group&gt;</span></span>

<span data-ttu-id="3bb7c-134">Aktivieren Sie dieses Kontrollkästchen, um den MED-V-Arbeitsbereich für diesen Benutzer oder diese Gruppe zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="3bb7c-134">Select this check box to enable the MED-V workspace for this user or group.</span></span>

<span data-ttu-id="3bb7c-135">Arbeitsbereich läuft an diesem Datum ab</span><span class="sxs-lookup"><span data-stu-id="3bb7c-135">Workspace expires on this date</span></span>

<span data-ttu-id="3bb7c-136">Aktivieren Sie dieses Kontrollkästchen, um dem Berechtigungssatz für diesen Benutzer oder diese Gruppe ein Ablaufdatum zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="3bb7c-136">Select this check box to assign an expiration date for the permissions set for this user or group.</span></span>

<span data-ttu-id="3bb7c-137">Wenn diese Option ausgewählt ist, ist das Datumsfeld aktiviert.</span><span class="sxs-lookup"><span data-stu-id="3bb7c-137">When selected, the date box is enabled.</span></span> <span data-ttu-id="3bb7c-138">Legen Sie das Datum fest, und die Berechtigungen werden am Ende des angegebenen Datums ablaufen.</span><span class="sxs-lookup"><span data-stu-id="3bb7c-138">Set the date, and permissions will expire at the end of the date specified.</span></span>

<span data-ttu-id="3bb7c-139">Offline Arbeit ist auf</span><span class="sxs-lookup"><span data-stu-id="3bb7c-139">Offline work is restricted to</span></span>

<span data-ttu-id="3bb7c-140">Aktivieren Sie dieses Kontrollkästchen, um einen Zeitraum zuzuweisen, in dem die Richtlinie für diesen Benutzer oder diese Gruppe aktualisiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="3bb7c-140">Select this check box to assign a time period in which the policy must be refreshed for this user or group.</span></span> <span data-ttu-id="3bb7c-141">Wenn diese Option ausgewählt ist, ist das Feld Zeitraum aktiviert.</span><span class="sxs-lookup"><span data-stu-id="3bb7c-141">When selected, the time period box is enabled.</span></span> <span data-ttu-id="3bb7c-142">Legen Sie die Anzahl der Tage oder Stunden fest, und am Ende des angegebenen Zeitraums kann der Benutzer oder die Gruppe keine Verbindung herstellen, wenn die Richtlinie nicht aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="3bb7c-142">Set the number of days or hours, and at the end of the specified time period, the user or group will not be able to connect if the policy is not refreshed.</span></span>

<span data-ttu-id="3bb7c-143">Arbeitsbereichs Löschoptionen</span><span class="sxs-lookup"><span data-stu-id="3bb7c-143">Workspace deletion options</span></span>

<span data-ttu-id="3bb7c-144">Klicken Sie, um die Löschoptionen für den MED-V-Arbeitsbereich zu definieren.</span><span class="sxs-lookup"><span data-stu-id="3bb7c-144">Click to set the MED-V workspace deletion options.</span></span> <span data-ttu-id="3bb7c-145">Weitere Informationen finden Sie unter [so wird es gemacht: Einrichten von Optionen für den Arbeitsbereichs Löschvorgang in MED-V](how-to-set-med-v-workspace-deletion-options.md).</span><span class="sxs-lookup"><span data-stu-id="3bb7c-145">For more information, see [How to Set MED-V Workspace Deletion Options](how-to-set-med-v-workspace-deletion-options.md).</span></span>

*<span data-ttu-id="3bb7c-146">Datenübertragung</span><span class="sxs-lookup"><span data-stu-id="3bb7c-146">Data Transfer</span></span>*

<span data-ttu-id="3bb7c-147">Unterstützen Zwischenablage zwischen Host und Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="3bb7c-147">Support clipboard between host and Workspace</span></span>

<span data-ttu-id="3bb7c-148">Aktivieren Sie dieses Kontrollkästchen, um das Kopieren und Einfügen zwischen dem Host und dem MED-V-Arbeitsbereich zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="3bb7c-148">Select this check box to enable copying and pasting between the host and the MED-V workspace.</span></span>

<span data-ttu-id="3bb7c-149">Unterstützung der Dateiübertragung zwischen dem Host und dem Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="3bb7c-149">Support file transfer between the host and Workspace</span></span>

<span data-ttu-id="3bb7c-150">Aktivieren Sie dieses Kontrollkästchen, um die Übertragung von Dateien zwischen dem Host und dem MED-V-Arbeitsbereich zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="3bb7c-150">Select this check box to enable transferring files between the host and MED-V workspace.</span></span> <span data-ttu-id="3bb7c-151">Wählen Sie im Feld " **Dateiübertragung** " eine der folgenden Optionen aus:</span><span class="sxs-lookup"><span data-stu-id="3bb7c-151">Select one of the following options from the **File Transfer** box:</span></span>

-   <span data-ttu-id="3bb7c-152">**Beides**: Aktivieren Sie die Übertragung von Dateien zwischen dem Host und dem MED-V-Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="3bb7c-152">**Both**—Enable transferring files between the host and the MED-V workspace.</span></span>

-   <span data-ttu-id="3bb7c-153">**Host to Workspace**– aktivieren Sie die Übertragung von Dateien vom Host in den MED-V-Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="3bb7c-153">**Host to Workspace**—Enable transferring files from the host to the MED-V workspace.</span></span>

-   <span data-ttu-id="3bb7c-154">**Arbeitsbereich für Host**: Aktivieren Sie die Übertragung von Dateien aus dem MED-V-Arbeitsbereich an den Host.</span><span class="sxs-lookup"><span data-stu-id="3bb7c-154">**Workspace to Host**—Enable transferring files from the MED-V workspace to the host.</span></span>

**<span data-ttu-id="3bb7c-155">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="3bb7c-155">Note</span></span>**  
<span data-ttu-id="3bb7c-156">Wenn ein Benutzer ohne Berechtigungen versucht, Dateien zu übertragen, wird ein Fenster eingeblendet, in dem er aufgefordert wird, die Anmeldeinformationen eines Benutzers einzugeben, der über die Berechtigung zum Durchführen der Dateiübertragung verfügt.</span><span class="sxs-lookup"><span data-stu-id="3bb7c-156">If a user without permissions attempts to transfer files, a window will appear prompting him to enter the credentials of a user with permissions to perform the file transfer.</span></span>



**<span data-ttu-id="3bb7c-157">Wichtig</span><span class="sxs-lookup"><span data-stu-id="3bb7c-157">Important</span></span>**  
<span data-ttu-id="3bb7c-158">Um die Dateiübertragung in Windows XP SP3 zu unterstützen, müssen Sie die Offlinedateisynchronisierung deaktivieren, indem Sie die Registrierung wie folgt bearbeiten:</span><span class="sxs-lookup"><span data-stu-id="3bb7c-158">To support file transfer in Windows XP SP3, you must disable offline file synchronization by editing the registry as follows:</span></span>

`REG ADD HKLM\software\microsoft\windows\currentversion\netcache /V Enabled /T REG_DWORD /F /D 0`



<span data-ttu-id="3bb7c-159">Erweitert</span><span class="sxs-lookup"><span data-stu-id="3bb7c-159">Advanced</span></span>

<span data-ttu-id="3bb7c-160">Klicken Sie, um die erweiterten Dateiübertragungsoptionen zu definieren.</span><span class="sxs-lookup"><span data-stu-id="3bb7c-160">Click to set the advanced file transfer options.</span></span> <span data-ttu-id="3bb7c-161">Weitere Informationen finden Sie unter [Vorgehensweise beim Einrichten erweiterter Dateiübertragungsoptionen](how-to-set-advanced-file-transfer-options.md).</span><span class="sxs-lookup"><span data-stu-id="3bb7c-161">For more information, see [How to Set Advanced File Transfer Options](how-to-set-advanced-file-transfer-options.md).</span></span>

*<span data-ttu-id="3bb7c-162">Gerätesteuerung</span><span class="sxs-lookup"><span data-stu-id="3bb7c-162">Device Control</span></span>*

<span data-ttu-id="3bb7c-163">Aktivieren des Druckvorgangs für Drucker, die mit dem Host verbunden sind</span><span class="sxs-lookup"><span data-stu-id="3bb7c-163">Enable printing to printers connected to the host</span></span>

<span data-ttu-id="3bb7c-164">Aktivieren Sie dieses Kontrollkästchen, um Benutzern das Drucken aus dem MED-V-Arbeitsbereich mithilfe des Host Druckers zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="3bb7c-164">Select this check box to enable users to print from the MED-V workspace using the host printer.</span></span>

**<span data-ttu-id="3bb7c-165">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="3bb7c-165">Note</span></span>**  
<span data-ttu-id="3bb7c-166">Der Druck wird von den auf dem Host definierten Druckern ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3bb7c-166">The printing is performed by the printers defined on the host.</span></span>



<span data-ttu-id="3bb7c-167">Aktivieren des Zugriffs auf CD/DVD</span><span class="sxs-lookup"><span data-stu-id="3bb7c-167">Enable access to CD / DVD</span></span>

<span data-ttu-id="3bb7c-168">Aktivieren Sie dieses Kontrollkästchen, um den Zugriff auf ein CD-oder DVD-Laufwerk über diesen MED-V-Arbeitsbereich zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="3bb7c-168">Select this check box to allow access to a CD or DVD drive from this MED-V workspace.</span></span>



**<span data-ttu-id="3bb7c-169">Mehrere Mitgliedschaften</span><span class="sxs-lookup"><span data-stu-id="3bb7c-169">Multiple Memberships</span></span>**

1.  <span data-ttu-id="3bb7c-170">Wenn der Benutzer Teil einer Gruppe ist und dem Benutzer sowie der Gruppe, der Sie angehören, Berechtigungen zugewiesen wurden, werden alle Berechtigungen angewendet.</span><span class="sxs-lookup"><span data-stu-id="3bb7c-170">If the user is part of a group and permissions are applied to the user as well as to the group they are part of, all permissions are applied.</span></span>

2.  <span data-ttu-id="3bb7c-171">Wenn der Benutzer ein Mitglied von zwei verschiedenen Gruppen ist, werden die am wenigsten restriktiven Berechtigungen angewendet.</span><span class="sxs-lookup"><span data-stu-id="3bb7c-171">If the user is a member of two different groups, the least restrictive permissions are applied.</span></span>

## <span data-ttu-id="3bb7c-172">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="3bb7c-172">Related topics</span></span>


[<span data-ttu-id="3bb7c-173">Über die Benutzeroberfläche der MED-V-Management-Konsole</span><span class="sxs-lookup"><span data-stu-id="3bb7c-173">Using the MED-V Management Console User Interface</span></span>](using-the-med-v-management-console-user-interface.md)

[<span data-ttu-id="3bb7c-174">Erstellen eines MED-V-Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="3bb7c-174">Creating a MED-V Workspace</span></span>](creating-a-med-v-workspacemedv-10-sp1.md)

[<span data-ttu-id="3bb7c-175">So legen Sie Optionen zum Löschen von MED-V-Arbeitsbereichen fest</span><span class="sxs-lookup"><span data-stu-id="3bb7c-175">How to Set MED-V Workspace Deletion Options</span></span>](how-to-set-med-v-workspace-deletion-options.md)

[<span data-ttu-id="3bb7c-176">So legen Sie erweiterte Optionen für die Dateiübertragung fest</span><span class="sxs-lookup"><span data-stu-id="3bb7c-176">How to Set Advanced File Transfer Options</span></span>](how-to-set-advanced-file-transfer-options.md)









