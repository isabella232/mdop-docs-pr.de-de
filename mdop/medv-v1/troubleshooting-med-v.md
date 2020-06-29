---
title: Problembehandlung für MED-V
description: Problembehandlung für MED-V
author: dansimp
ms.assetid: f43dae36-6485-4e06-9c66-0a646e27079d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 38d13be699a92368ff258026acd8e0d5f0e28cd6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811410"
---
# <span data-ttu-id="0b6f1-103">Problembehandlung für MED-V</span><span class="sxs-lookup"><span data-stu-id="0b6f1-103">Troubleshooting MED-V</span></span>


<span data-ttu-id="0b6f1-104">Dieser Abschnitt enthält Informationen zur Problembehandlung bei allgemeinen Problemen mit Microsoft Enterprise Desktop Virtualization (MED-V).</span><span class="sxs-lookup"><span data-stu-id="0b6f1-104">This section provides information to help troubleshoot general issues with Microsoft Enterprise Desktop Virtualization (MED-V).</span></span>

## <span data-ttu-id="0b6f1-105">Wenn Sie die Hostauflösung ändern und dann den MED-V-Arbeitsbereich maximieren, wird der Desktop schwarz angezeigt.</span><span class="sxs-lookup"><span data-stu-id="0b6f1-105">Changing the host resolution and then maximizing the MED-V workspace causes the desktop to appear black</span></span>


<span data-ttu-id="0b6f1-106">Wenn Sie im vollständigen Desktopmodus arbeiten und die Hostauflösung ändern und dann das Med-v Workspace-Fenster maximieren, wird der Desktop schwarz angezeigt, und der Med-v-Arbeitsbereich reagiert möglicherweise nicht.</span><span class="sxs-lookup"><span data-stu-id="0b6f1-106">When working in full desktop mode, if you change the host resolution and then maximize the MED-V workspace window, the desktop appears black and the MED-V workspace might not respond.</span></span>

### <span data-ttu-id="0b6f1-107">Lösung</span><span class="sxs-lookup"><span data-stu-id="0b6f1-107">Solution</span></span>

<span data-ttu-id="0b6f1-108">Beenden Sie den MED-V-Arbeitsbereich, und starten Sie ihn dann.</span><span class="sxs-lookup"><span data-stu-id="0b6f1-108">Stop and then start the MED-V workspace.</span></span>

## <span data-ttu-id="0b6f1-109">Das Starten eines MED-V-Arbeitsbereichs mit deaktiviertem Netzwerkadapter und späterer Aktivierung des Adapters stellt keine Netzwerkkonnektivität wieder her</span><span class="sxs-lookup"><span data-stu-id="0b6f1-109">Starting a MED-V workspace with a network adapter disabled and then later enabling the adapter does not restore network connectivity</span></span>


<span data-ttu-id="0b6f1-110">Wenn Sie einen Med-v-Arbeitsbereich im Brückenmodus konfigurieren und dann den Med-v-Arbeitsbereich starten, während ein Netzwerkadapter deaktiviert ist, wird die Netzwerkverbindung über diesen Adapter nicht wiederhergestellt, wenn der Adapter später aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="0b6f1-110">If you configure a MED-V workspace in bridge mode and then start the MED-V workspace while a network adapter is disabled, if the adapter is later enabled, the network connectivity through that adapter is not restored.</span></span>

### <span data-ttu-id="0b6f1-111">Lösung</span><span class="sxs-lookup"><span data-stu-id="0b6f1-111">Solution</span></span>

<span data-ttu-id="0b6f1-112">Beenden Sie den MED-V-Arbeitsbereich, und starten Sie ihn dann.</span><span class="sxs-lookup"><span data-stu-id="0b6f1-112">Stop and then start the MED-V workspace.</span></span>

## <span data-ttu-id="0b6f1-113">Ein Bild kann nur von einem Windows-Benutzer pro Computer verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0b6f1-113">An image can be used by only one Windows user per computer</span></span>


<span data-ttu-id="0b6f1-114">Ein MED-V Workspace-Bild kann nur von Windows-Benutzern verwendet werden, die das Bild heruntergeladen oder importiert haben.</span><span class="sxs-lookup"><span data-stu-id="0b6f1-114">A MED-V workspace image can be used only by the Windows user who downloaded or imported the image.</span></span> <span data-ttu-id="0b6f1-115">Dieser Benutzer ist der einzige Benutzer neben Administratoren, die über die Berechtigungen für den Ordner verfügen, in dem sich die heruntergeladenen Bilder befinden.</span><span class="sxs-lookup"><span data-stu-id="0b6f1-115">This user is the only user aside from administrators who have permissions to the folder where the downloaded images are located.</span></span>

### <span data-ttu-id="0b6f1-116">Lösung</span><span class="sxs-lookup"><span data-stu-id="0b6f1-116">Solution</span></span>

<span data-ttu-id="0b6f1-117">Manuelles Ändern der Zugriffssteuerungsliste (ACL) im Bildspeicher</span><span class="sxs-lookup"><span data-stu-id="0b6f1-117">Manually change the access control list (ACL) on the image store.</span></span>

## <span data-ttu-id="0b6f1-118">Bei der Installation von MED-V mithilfe von Configuration Manager mit aktivierten Benutzerrechten schlägt die Deinstallation fehl</span><span class="sxs-lookup"><span data-stu-id="0b6f1-118">When installing MED-V by using Configuration Manager with users rights enabled, uninstall fails</span></span>


<span data-ttu-id="0b6f1-119">Wenn MED-V mit Microsoft System Center Configuration Manager installiert ist und der Ausführungsmodus des Pakets auf Benutzerrechte festgesetzt ist, schlägt die Deinstallation mit einer Fehlermeldung fehl, die besagt, dass nur administrative Benutzer MED-V deinstallieren können.</span><span class="sxs-lookup"><span data-stu-id="0b6f1-119">If MED-V is installed by using Microsoft System Center Configuration Manager and the run mode of the package is set to users rights, uninstall fails with an error message that says that only administrative users can uninstall MED-V.</span></span>

### <span data-ttu-id="0b6f1-120">Lösung</span><span class="sxs-lookup"><span data-stu-id="0b6f1-120">Solution</span></span>

<span data-ttu-id="0b6f1-121">Legen Sie beim Erstellen eines Configuration Manager-Pakets für MED-V den Ausführungsmodus auf Administratorrechte.</span><span class="sxs-lookup"><span data-stu-id="0b6f1-121">When creating a Configuration Manager package for MED-V, set the run mode to administrative rights.</span></span>

## <span data-ttu-id="0b6f1-122">Wenn Sie MED-V mithilfe eines Unternehmens Bereitstellungssystems installieren, in dem die Installation so konfiguriert ist, dass der Client nach der Installation ausgeführt wird, können Sie den Client nicht ausführen.</span><span class="sxs-lookup"><span data-stu-id="0b6f1-122">When installing MED-V by using a corporate deployment system, where the installation is configured to run the client following installation, you cannot run the client</span></span>


<span data-ttu-id="0b6f1-123">Wenn Med-v mit einem Unternehmens Bereitstellungssystem installiert ist und das Installationspaket so konfiguriert ist, dass der Med-v-Client nach der Installation ausgeführt wird, können Sie nach dem Ausführen des Clients unter dem Systemkonto nicht sehen, dass der Client ausgeführt wird (außer im Infobereich), und Sie können nicht mit ihm interagieren.</span><span class="sxs-lookup"><span data-stu-id="0b6f1-123">If MED-V is installed by using a corporate deployment system and the installation package is configured to run MED-V client following the installation, after the client is running under the system account, you cannot see that the client is running (except in the notification area), and you cannot interact with it.</span></span>

### <span data-ttu-id="0b6f1-124">Lösung</span><span class="sxs-lookup"><span data-stu-id="0b6f1-124">Solution</span></span>

<span data-ttu-id="0b6f1-125">Wenn Sie MED-V mithilfe eines Unternehmens Bereitstellungssystems installieren, verwenden Sie den Parameter *Start \ _MEDV = 0* . msi.</span><span class="sxs-lookup"><span data-stu-id="0b6f1-125">When installing MED-V by using a corporate deployment system, use the *START\_MEDV=0* .msi parameter.</span></span>

## <span data-ttu-id="0b6f1-126">MED-V-Testbild kann nicht gestartet werden</span><span class="sxs-lookup"><span data-stu-id="0b6f1-126">MED-V test image fails to start</span></span>


<span data-ttu-id="0b6f1-127">Wenn ein MED-V-Testbild nicht gestartet werden kann, wird es nie wiederhergestellt, und alle zukünftigen Starts werden mit der Fehlermeldung "Gina-Fehler beim Laden" fehlschlagen.</span><span class="sxs-lookup"><span data-stu-id="0b6f1-127">If a MED-V test image fails to start, it will never recover and all future startups will fail with a “GINA fail to load” error message.</span></span>

### <span data-ttu-id="0b6f1-128">Lösung</span><span class="sxs-lookup"><span data-stu-id="0b6f1-128">Solution</span></span>

<span data-ttu-id="0b6f1-129">Löschen Sie das vorhandene Test Abbild, und erstellen Sie es dann erneut.</span><span class="sxs-lookup"><span data-stu-id="0b6f1-129">Delete the existing test image and then re-create it.</span></span>

## <span data-ttu-id="0b6f1-130">Nach dem Versuch, einer Domäne mit den falschen Anmeldeinformationen beizutreten, gelingt es dem Bild nie, der Domäne beizutreten.</span><span class="sxs-lookup"><span data-stu-id="0b6f1-130">After attempting to join a domain with the wrong credentials, the image never succeeds in joining the domain</span></span>


<span data-ttu-id="0b6f1-131">Wenn ein Konfigurationsfehler im Building Block der Join-Domäne vorhanden ist, der zum erstmaligen Setup-Skript der virtuellen Maschine gehört, bewirkt dies, dass der MED-V-Arbeitsbereich beim Versuch, einer Domäne beizutreten, fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="0b6f1-131">If there is a configuration error in the join domain building block, which is part of the virtual machine first-time setup script, it causes the MED-V workspace to fail when attempting to join a domain.</span></span> <span data-ttu-id="0b6f1-132">Nachdem der Konfigurationsfehler behoben wurde, kann das im MED-V-Arbeitsbereich enthaltene Bild nicht zur Domäne hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="0b6f1-132">After the configuration error is repaired, the image included in the MED-V workspace cannot join the domain.</span></span>

### <span data-ttu-id="0b6f1-133">Lösung</span><span class="sxs-lookup"><span data-stu-id="0b6f1-133">Solution</span></span>

<span data-ttu-id="0b6f1-134">Wenn das Bild bereitgestellt wurde, verteilen Sie es erneut.</span><span class="sxs-lookup"><span data-stu-id="0b6f1-134">If the image was deployed, redistribute the image.</span></span> <span data-ttu-id="0b6f1-135">Wenn es sich bei dem Bild um ein Testbild handelt, erstellen Sie das Bild erneut.</span><span class="sxs-lookup"><span data-stu-id="0b6f1-135">If the image was a test image, re-create the image.</span></span>

## <span data-ttu-id="0b6f1-136">MED-V unterstützt nicht mehrere Monitore</span><span class="sxs-lookup"><span data-stu-id="0b6f1-136">MED-V does not support multiple monitors</span></span>


<span data-ttu-id="0b6f1-137">MED-V unterstützt die Anzeige von veröffentlichten Anwendungen auf mehreren Monitoren nicht.</span><span class="sxs-lookup"><span data-stu-id="0b6f1-137">MED-V does not support displaying published applications across multiple monitors.</span></span> <span data-ttu-id="0b6f1-138">Veröffentlichte Anwendungen und andere Clientfenster werden möglicherweise auf dem falschen Bildschirm angezeigt, und manchmal, nachdem ein Bildschirm getrennt wurde, versucht MED-V, den Bildschirm an den Monitor zu senden, damit der angeschlossene Monitor leer angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="0b6f1-138">Published applications and other client windows may be displayed in the wrong screen, and sometimes after a screen is disconnected, MED-V attempts to send the screen to the monitor so that the connected monitor appears blank.</span></span>

### <span data-ttu-id="0b6f1-139">Lösung</span><span class="sxs-lookup"><span data-stu-id="0b6f1-139">Solution</span></span>

<span data-ttu-id="0b6f1-140">Trennen Sie den zusätzlichen Bildschirm, und starten Sie den Client neu.</span><span class="sxs-lookup"><span data-stu-id="0b6f1-140">Disconnect the additional screen, and restart the client.</span></span>

## <span data-ttu-id="0b6f1-141">Der Med-v-Arbeitsbereich kann nicht gestartet werden, wenn der Host während des Starts des Med-v-Arbeitsbereichs abstürzt</span><span class="sxs-lookup"><span data-stu-id="0b6f1-141">MED-V workspace might fail to start if the host crashes during MED-V workspace startup</span></span>


<span data-ttu-id="0b6f1-142">Wenn der Host während des Startvorgangs des Med-v-Arbeitsbereichs abstürzt und eine Fehlermeldung mit dem Hinweis "Stammelement fehlt" angezeigt wird, kann der Med-v-Arbeitsbereich Daten zu einer leeren VMC-Datei (Virtual Machine Configuration) hinzufügen, wodurch der Startvorgang fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="0b6f1-142">If the host crashes during the MED-V workspace startup process and an error message appears that says “Root element is missing,” the MED-V workspace might add data to an empty virtual machine configuration (VMC) file, which will cause the startup process to fail.</span></span>

### <span data-ttu-id="0b6f1-143">Lösung</span><span class="sxs-lookup"><span data-stu-id="0b6f1-143">Solution</span></span>

<span data-ttu-id="0b6f1-144">Ersetzen Sie die leere VMC-Datei durch eine VMC-Datei aus dem Basis Bild.</span><span class="sxs-lookup"><span data-stu-id="0b6f1-144">Replace the empty VMC file with a VMC file from the base image.</span></span>

## <span data-ttu-id="0b6f1-145">Die Tastatur reagiert in veröffentlichten Anwendungsfenstern nicht</span><span class="sxs-lookup"><span data-stu-id="0b6f1-145">The keyboard does not respond in published application windows</span></span>


<span data-ttu-id="0b6f1-146">Wenn Sie in einem MED-V-Arbeitsbereich die Windows-Logo-Taste drücken, während sich eine veröffentlichte Anwendung im Fokus befindet, reagiert die Tastatur nicht mehr in veröffentlichten Anwendungsfenstern.</span><span class="sxs-lookup"><span data-stu-id="0b6f1-146">In a MED-V workspace, if you press the Windows logo key when a published application is in focus, the keyboard no longer responds in published application windows.</span></span>

### <span data-ttu-id="0b6f1-147">Lösung</span><span class="sxs-lookup"><span data-stu-id="0b6f1-147">Solution</span></span>

<span data-ttu-id="0b6f1-148">Drücken Sie die Windows-Logo-Taste, während eine veröffentlichte Anwendung den Fokus hat.</span><span class="sxs-lookup"><span data-stu-id="0b6f1-148">Press the Windows logo key while a published application is in focus.</span></span>

## <span data-ttu-id="0b6f1-149">Ein Domänen-MED-V-Arbeitsbereich aktualisiert keine Domänenanmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="0b6f1-149">A domain MED-V workspace does not update domain credentials</span></span>


<span data-ttu-id="0b6f1-150">Wenn Sie einen beständigen Med-v-Arbeitsbereich in einer Domänenumgebung verwenden und Ihr Domänenkennwort ändern, aktualisiert der Med-v-Client die Anmeldeinformationen für die Med-v Workspace-Domäne nicht.</span><span class="sxs-lookup"><span data-stu-id="0b6f1-150">When using a persistent MED-V workspace in a domain environment, if you change your domain password, the MED-V client does not update the MED-V workspace domain credentials.</span></span> <span data-ttu-id="0b6f1-151">Wenn eine veröffentlichte Anwendung versucht, auf eine Netzwerkressource zuzugreifen, erhalten Sie eine Fehlermeldung, in der Sie darüber informiert werden, dass Ihre Anmeldeinformationen abgelaufen sind.</span><span class="sxs-lookup"><span data-stu-id="0b6f1-151">When a published application attempts to access a network resource, you will receive an error message notifying you that your credentials expired.</span></span>

### <span data-ttu-id="0b6f1-152">Lösung</span><span class="sxs-lookup"><span data-stu-id="0b6f1-152">Solution</span></span>

<span data-ttu-id="0b6f1-153">Starten Sie das Betriebssystem MED-V Workspace neu.</span><span class="sxs-lookup"><span data-stu-id="0b6f1-153">Restart the MED-V workspace operating system.</span></span>

## <span data-ttu-id="0b6f1-154">Maximierte veröffentlichte Anwendungsfenster decken die Host-Taskleiste ab</span><span class="sxs-lookup"><span data-stu-id="0b6f1-154">Maximized published application windows cover the host taskbar</span></span>


<span data-ttu-id="0b6f1-155">Wenn Sie ein veröffentlichtes Anwendungsfenster auf Vollbild maximieren, kann es die Host-Taskleiste abdecken.</span><span class="sxs-lookup"><span data-stu-id="0b6f1-155">If you maximize a published application window to full screen, it might cover the host taskbar.</span></span>

### <span data-ttu-id="0b6f1-156">Lösung</span><span class="sxs-lookup"><span data-stu-id="0b6f1-156">Solution</span></span>

<span data-ttu-id="0b6f1-157">Führen Sie eine der folgenden Aktionen aus:</span><span class="sxs-lookup"><span data-stu-id="0b6f1-157">Do one of the following:</span></span>

<span data-ttu-id="0b6f1-158">Minimieren Sie das Fenster "veröffentlichte Anwendung", um Zugriff auf den Infobereich zu erhalten, und starten Sie den MED-V-Arbeitsbereich neu.</span><span class="sxs-lookup"><span data-stu-id="0b6f1-158">Minimize the published application window to gain access to the notification area, and restart the MED-V workspace.</span></span>

<span data-ttu-id="0b6f1-159">Minimieren Sie das Fenster der veröffentlichten Anwendung, und stellen Sie das Fenster dann auf seinen maximierten Zustand zurück.</span><span class="sxs-lookup"><span data-stu-id="0b6f1-159">Minimize the published application window, and then restore the window to its maximized state.</span></span>

## <span data-ttu-id="0b6f1-160">Das Hinzufügen von Benutzern oder Gruppen im MED-V Server-Konfigurations-Manager funktioniert nicht</span><span class="sxs-lookup"><span data-stu-id="0b6f1-160">Adding users or groups in the MED-V Server Configuration Manager does not work</span></span>


<span data-ttu-id="0b6f1-161">Beim Hinzufügen von Benutzern oder Gruppen im Dialogfeld **Benutzer oder Gruppen auswählen** werden die ausgewählten Benutzer oder Gruppen nicht zur Zugriffssteuerungsliste im MED-V Server-Konfigurations-Manager hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="0b6f1-161">When adding users or groups in the **Select Users or Groups** dialog box, the selected users or groups are not added to the access control list in the MED-V Server Configuration Manager.</span></span>

### <span data-ttu-id="0b6f1-162">Lösung</span><span class="sxs-lookup"><span data-stu-id="0b6f1-162">Solution</span></span>

<span data-ttu-id="0b6f1-163">Hinzufügen von Benutzern oder Gruppen mithilfe des Dialogfelds **Benutzer-oder Gruppennamen eingeben** .</span><span class="sxs-lookup"><span data-stu-id="0b6f1-163">Add users or groups using the **Enter User or Group names** dialog box.</span></span> <span data-ttu-id="0b6f1-164">Ausführliche Informationen finden Sie unter [so wird es gemacht: Installieren und Konfigurieren der MED-V-Server Komponente](how-to-install-and-configure-the-med-v-server-component.md#bkmk-configuringpermissions).</span><span class="sxs-lookup"><span data-stu-id="0b6f1-164">For detailed information, see [How to Install and Configure the MED-V Server Component](how-to-install-and-configure-the-med-v-server-component.md#bkmk-configuringpermissions).</span></span>

## <span data-ttu-id="0b6f1-165">MED-V funktioniert nicht auf Computern, auf denen Windows Virtual PC für Windows 7 installiert ist</span><span class="sxs-lookup"><span data-stu-id="0b6f1-165">MED-V does not work on computers with Windows Virtual PC for Windows 7 installed</span></span>


<span data-ttu-id="0b6f1-166">Für MED-V ist Windows Virtual PC2007 erforderlich.</span><span class="sxs-lookup"><span data-stu-id="0b6f1-166">MED-V requires Windows Virtual PC2007.</span></span> <span data-ttu-id="0b6f1-167">Windows Virtual PC für Windows7 und Virtual PC2007 SP1 können nicht auf demselben Computer installiert werden.</span><span class="sxs-lookup"><span data-stu-id="0b6f1-167">Windows Virtual PC for Windows7 and Virtual PC2007 SP1 cannot be installed on the same computer.</span></span>

### <span data-ttu-id="0b6f1-168">Lösung</span><span class="sxs-lookup"><span data-stu-id="0b6f1-168">Solution</span></span>

<span data-ttu-id="0b6f1-169">Deinstallieren Sie Virtual PC für Windows7, bevor Sie Virtual PC2007 SP1 und MED-V installieren.</span><span class="sxs-lookup"><span data-stu-id="0b6f1-169">Uninstall Virtual PC for Windows7 before installing Virtual PC2007 SP1 and MED-V.</span></span>

## <a href="" id="med-v-does-not-support-virtual-pc-and-windows-xp-mode-images-"></a><span data-ttu-id="0b6f1-170">MED-V unterstützt keine Images für Virtual PC und WindowsXP-Modus</span><span class="sxs-lookup"><span data-stu-id="0b6f1-170">MED-V does not support Virtual PC and WindowsXP Mode images</span></span>


<span data-ttu-id="0b6f1-171">Med-v 1.0 SP1 unterstützt keine Bilder, die von Windows Virtual PC für Windows7 erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="0b6f1-171">MED-V1.0 SP1 does not support images created by Windows Virtual PC for Windows7.</span></span> <span data-ttu-id="0b6f1-172">Wenn ein virtueller PC für Windows7-Bild verwendet wird, schlägt der Client während des Starts fehl.</span><span class="sxs-lookup"><span data-stu-id="0b6f1-172">If a Virtual PC for Windows7 image is used, the client will fail during startup.</span></span>

### <span data-ttu-id="0b6f1-173">Lösung</span><span class="sxs-lookup"><span data-stu-id="0b6f1-173">Solution</span></span>

<span data-ttu-id="0b6f1-174">Erstellen Sie MED-V-Bilder mithilfe von Virtual PC2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="0b6f1-174">Create MED-V images by using Virtual PC2007 SP1.</span></span>

## <span data-ttu-id="0b6f1-175">Die Windows-Firewall blockiert die virtuelle PC2007 SP1-Netzwerkaktivität</span><span class="sxs-lookup"><span data-stu-id="0b6f1-175">Windows firewall blocks Virtual PC2007 SP1 network activity</span></span>


<span data-ttu-id="0b6f1-176">Standardmäßig blockiert die Windows-Firewall virtuelle PC2007 SP1-Netzwerkaktivitäten, und wenn Virtual PC2007 SP1 auf dem Clientcomputer initiiert wird, gibt es eine Firewall-Nachricht, die die Startsequenz und den gesamten Netzwerkzugriff blockiert.</span><span class="sxs-lookup"><span data-stu-id="0b6f1-176">By default, Windows firewall blocks Virtual PC2007 SP1 network activity, and when Virtual PC2007 SP1 initiates on the client computer, there is a firewall message that blocks its startup sequence and all network access.</span></span>

### <span data-ttu-id="0b6f1-177">Lösung</span><span class="sxs-lookup"><span data-stu-id="0b6f1-177">Solution</span></span>

<span data-ttu-id="0b6f1-178">Aktualisieren Sie die Firewall-Ausnahme mithilfe von Gruppenrichtlinien, bevor MED-V vom Endbenutzer verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0b6f1-178">Update the firewall exception by using Group Policy before MED-V is used by the end user.</span></span>

## <span data-ttu-id="0b6f1-179">Beim Aktualisieren des Clients wird eine Fehlermeldung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="0b6f1-179">When upgrading the client an error message appears</span></span>


<span data-ttu-id="0b6f1-180">Wenn Sie den Client von Med-v 1.0 auf Med-v 1.0 SP1 aktualisieren, wird möglicherweise eine Meldung angezeigt, in der Sie darüber informiert werden, dass kein Med-v-Arbeitsbereich definiert ist.</span><span class="sxs-lookup"><span data-stu-id="0b6f1-180">When upgrading the client from MED-V1.0 to MED-V1.0 SP1, a message may appear notifying you that no MED-V workspace is defined.</span></span>

### <span data-ttu-id="0b6f1-181">Lösung</span><span class="sxs-lookup"><span data-stu-id="0b6f1-181">Solution</span></span>

<span data-ttu-id="0b6f1-182">Schließen Sie den Client, und starten Sie ihn erneut.</span><span class="sxs-lookup"><span data-stu-id="0b6f1-182">Close the client and restart it.</span></span>

## <span data-ttu-id="0b6f1-183">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="0b6f1-183">Related topics</span></span>


[<span data-ttu-id="0b6f1-184">Versionshinweise für MED-V 1.0</span><span class="sxs-lookup"><span data-stu-id="0b6f1-184">MED-V 1.0 Release Notes</span></span>](med-v-10-release-notesmedv-10.md)

[<span data-ttu-id="0b6f1-185">MED-V 1.0 SP1 und SP2-Versionshinweise</span><span class="sxs-lookup"><span data-stu-id="0b6f1-185">MED-V 1.0 SP1 and SP2 Release Notes</span></span>](med-v-10-sp1-and-sp2-release-notesmedv-10-sp1.md)

 

 





