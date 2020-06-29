---
title: MED-V-Ereignisprotokollmeldungen
description: MED-V-Ereignisprotokollmeldungen
author: dansimp
ms.assetid: 7ba7344d-153b-4cc4-a00a-5d42aee9986b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b5d8dcf1cce48d6c1e29d46b4db7ac1550aa9477
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809739"
---
# <span data-ttu-id="a1f70-103">MED-V-Ereignisprotokollmeldungen</span><span class="sxs-lookup"><span data-stu-id="a1f70-103">MED-V Event Log Messages</span></span>


<span data-ttu-id="a1f70-104">Die Protokolldateien für Microsoft Enterprise Desktop Virtualization (Med-v) 2,0 bieten detaillierte Informationen dazu, wie Sie Med-v in Ihrem Unternehmen bereitstellen und verwalten, und helfen dabei, die Funktionalität zu überprüfen oder Probleme zu beheben.</span><span class="sxs-lookup"><span data-stu-id="a1f70-104">The log files for Microsoft Enterprise Desktop Virtualization (MED-V) 2.0 provide detailed information about how to deploy and manage MED-V in your enterprise and help verify functionality or help troubleshoot issues.</span></span>

## <span data-ttu-id="a1f70-105">Ereignis-IDs</span><span class="sxs-lookup"><span data-stu-id="a1f70-105">Event IDs</span></span>


<span data-ttu-id="a1f70-106">Im folgenden finden Sie eine Liste der Med-v-Ereignis-IDs, die Ihnen bei der Behandlung von Problemen helfen können, die beim Bereitstellen oder Verwalten von Med-v auftreten können.</span><span class="sxs-lookup"><span data-stu-id="a1f70-106">The following are a list of MED-V event IDs to help troubleshoot issues that you might encounter when you deploy or manage MED-V.</span></span>

### <span data-ttu-id="a1f70-107">FTS</span><span class="sxs-lookup"><span data-stu-id="a1f70-107">Fts</span></span>

<span data-ttu-id="a1f70-108">Zeigt die Ereignis-IDs für die erstmalige Einrichtung an.</span><span class="sxs-lookup"><span data-stu-id="a1f70-108">Shows the event IDs for first time setup.</span></span>

### <span data-ttu-id="a1f70-109">Ereignis-ID 3066</span><span class="sxs-lookup"><span data-stu-id="a1f70-109">Event ID 3066</span></span>

<span data-ttu-id="a1f70-110">Der Vorgang zum Starten des virtuellen Computers ist fehlgeschlagen.</span><span class="sxs-lookup"><span data-stu-id="a1f70-110">Start virtual machine operation failed.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="a1f70-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a1f70-111">Description</span></span>**  
<span data-ttu-id="a1f70-112">Bei der virtuellen Festplatte (VHD), die Sie zum Erstellen eines MED-V-Arbeitsbereichs verwenden, besteht ein potenzielles Problem.</span><span class="sxs-lookup"><span data-stu-id="a1f70-112">A potential problem exists with the virtual hard disk (VHD) that you are using to create a MED-V workspace.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="a1f70-113">Lösung</span><span class="sxs-lookup"><span data-stu-id="a1f70-113">Solution</span></span>**  
<span data-ttu-id="a1f70-114">Überprüfen Sie, ob Sie einen virtuellen Computer mit der VHD für MED-V erstellen können und ob er gestartet werden kann.</span><span class="sxs-lookup"><span data-stu-id="a1f70-114">Verify that you can create a virtual machine with the VHD for MED-V and that it can be started.</span></span>

### <span data-ttu-id="a1f70-115">Ereignis-ID 3071</span><span class="sxs-lookup"><span data-stu-id="a1f70-115">Event ID 3071</span></span>

<span data-ttu-id="a1f70-116">Fehler beim Vorbereiten der virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="a1f70-116">Virtual machine preparation failed.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="a1f70-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a1f70-117">Description</span></span>**  
<span data-ttu-id="a1f70-118">Bei der erstmaligen Einrichtung ist ein Problem aufgetreten, das möglicherweise von vielen unterschiedlichen Problemen verursacht wurde.</span><span class="sxs-lookup"><span data-stu-id="a1f70-118">A problem occurred with first time setup that might have been caused by many different issues.</span></span> <span data-ttu-id="a1f70-119">Dazu gehören Probleme mit der Netzwerkverbindung.</span><span class="sxs-lookup"><span data-stu-id="a1f70-119">These include problems with network connectivity.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="a1f70-120">Lösung</span><span class="sxs-lookup"><span data-stu-id="a1f70-120">Solution</span></span>**  
<span data-ttu-id="a1f70-121">Starten Sie den MED-V-Host-Agent neu, um die erstmalige Einrichtung erneut auszuführen.</span><span class="sxs-lookup"><span data-stu-id="a1f70-121">Restart the MED-V Host Agent to rerun first time setup.</span></span>

### <span data-ttu-id="a1f70-122">Ereignis-ID 3078</span><span class="sxs-lookup"><span data-stu-id="a1f70-122">Event ID 3078</span></span>

<span data-ttu-id="a1f70-123">Fehler beim Vorbereiten der virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="a1f70-123">Virtual machine preparation failed.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="a1f70-124">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a1f70-124">Description</span></span>**  
<span data-ttu-id="a1f70-125">Bei der VHD, die Sie zum Erstellen eines MED-V-Arbeitsbereichs verwenden, besteht ein potenzielles Problem.</span><span class="sxs-lookup"><span data-stu-id="a1f70-125">A potential problem exists with the VHD that you are using to create a MED-V workspace.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="a1f70-126">Lösung</span><span class="sxs-lookup"><span data-stu-id="a1f70-126">Solution</span></span>**  
<span data-ttu-id="a1f70-127">Überprüfen Sie, ob Sie einen virtuellen Computer mit der VHD für MED-V erstellen können und ob er gestartet werden kann.</span><span class="sxs-lookup"><span data-stu-id="a1f70-127">Verify that you can create a virtual machine with the VHD for MED-V and that it can be started.</span></span>

### <span data-ttu-id="a1f70-128">Ereignis-ID 3079</span><span class="sxs-lookup"><span data-stu-id="a1f70-128">Event ID 3079</span></span>

<span data-ttu-id="a1f70-129">Erneutes Testen der Vorbereitung virtueller Computer</span><span class="sxs-lookup"><span data-stu-id="a1f70-129">Retrying virtual machine preparation.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="a1f70-130">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a1f70-130">Description</span></span>**  
<span data-ttu-id="a1f70-131">MED-V versucht, den virtuellen Computer vorzubereiten.</span><span class="sxs-lookup"><span data-stu-id="a1f70-131">MED-V is trying to prepare the virtual machine.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="a1f70-132">Lösung</span><span class="sxs-lookup"><span data-stu-id="a1f70-132">Solution</span></span>**  
<span data-ttu-id="a1f70-133">Es ist keine Aktion erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a1f70-133">No action is required.</span></span> <span data-ttu-id="a1f70-134">Lassen Sie die erstmalige Einrichtung fertig.</span><span class="sxs-lookup"><span data-stu-id="a1f70-134">Let first time setup finish.</span></span>

### <span data-ttu-id="a1f70-135">Ereignis-ID 3080</span><span class="sxs-lookup"><span data-stu-id="a1f70-135">Event ID 3080</span></span>

<span data-ttu-id="a1f70-136">Der Client wurde beim Vorbereiten des virtuellen Computers angehalten.</span><span class="sxs-lookup"><span data-stu-id="a1f70-136">The client was stopped when preparing the virtual machine.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="a1f70-137">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a1f70-137">Description</span></span>**  
<span data-ttu-id="a1f70-138">MED-V wird bei dem Versuch, den virtuellen Computer vorzubereiten, unerwartet beendet.</span><span class="sxs-lookup"><span data-stu-id="a1f70-138">MED-V stops unexpectedly when it tries to prepare the virtual machine.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="a1f70-139">Lösung</span><span class="sxs-lookup"><span data-stu-id="a1f70-139">Solution</span></span>**  
<span data-ttu-id="a1f70-140">Starten Sie den MED-V-Host-Agent, und lassen Sie das erstmalige Setup abgeschlossen</span><span class="sxs-lookup"><span data-stu-id="a1f70-140">Start the MED-V Host Agent and let first time setup complete</span></span>

### <span data-ttu-id="a1f70-141">Ereignis-ID 3084</span><span class="sxs-lookup"><span data-stu-id="a1f70-141">Event ID 3084</span></span>

<span data-ttu-id="a1f70-142">Der virtuelle Computer ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="a1f70-142">Virtual machine is not valid.</span></span> <span data-ttu-id="a1f70-143">Das erstmalige Setup muss erneut ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="a1f70-143">First time setup needs to be re-run.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="a1f70-144">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a1f70-144">Description</span></span>**  
<span data-ttu-id="a1f70-145">Der MED-V-Host-Agent hat ein Problem mit dem virtuellen Computer festgestellt.</span><span class="sxs-lookup"><span data-stu-id="a1f70-145">The MED-V Host Agent detected a problem with the virtual machine.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="a1f70-146">Lösung</span><span class="sxs-lookup"><span data-stu-id="a1f70-146">Solution</span></span>**  
<span data-ttu-id="a1f70-147">Es ist keine Aktion erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a1f70-147">No action is required.</span></span> <span data-ttu-id="a1f70-148">Lassen Sie die erstmalige Einrichtung fertig.</span><span class="sxs-lookup"><span data-stu-id="a1f70-148">Let first time setup finish.</span></span>

### <span data-ttu-id="a1f70-149">Ereignis-ID 3099</span><span class="sxs-lookup"><span data-stu-id="a1f70-149">Event ID 3099</span></span>

<span data-ttu-id="a1f70-150">Fehler beim Aufrufen des virtuellen Computers für Start.</span><span class="sxs-lookup"><span data-stu-id="a1f70-150">Call to start virtual machine failed.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="a1f70-151">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a1f70-151">Description</span></span>**  
<span data-ttu-id="a1f70-152">Bei der VHD, die Sie zum Erstellen eines MED-V-Arbeitsbereichs verwenden, besteht ein potenzielles Problem.</span><span class="sxs-lookup"><span data-stu-id="a1f70-152">A potential problem exists with the VHD you are using to create a MED-V workspace.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="a1f70-153">Lösung</span><span class="sxs-lookup"><span data-stu-id="a1f70-153">Solution</span></span>**  
<span data-ttu-id="a1f70-154">Stellen Sie sicher, dass Sie einen virtuellen Computer mit der VHD für MED-V erstellen und öffnen können.</span><span class="sxs-lookup"><span data-stu-id="a1f70-154">Verify that you can create a virtual machine with the VHD for MED-V and that it can be opened.</span></span>

### <span data-ttu-id="a1f70-155">VM-Verwaltung</span><span class="sxs-lookup"><span data-stu-id="a1f70-155">VM Management</span></span>

### <span data-ttu-id="a1f70-156">Ereignis-ID 4022</span><span class="sxs-lookup"><span data-stu-id="a1f70-156">Event ID 4022</span></span>

<span data-ttu-id="a1f70-157">VMManagerException schwerwiegender Fehler beim Ausgeben des Befehls an VM.</span><span class="sxs-lookup"><span data-stu-id="a1f70-157">VMManagerException Fatal error while issuing command to VM.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="a1f70-158">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a1f70-158">Description</span></span>**  
<span data-ttu-id="a1f70-159">Der Endbenutzer hat versucht, Med-v durch abmelden oder durch Herunterfahren des Med-v-Hosts zu beenden, und die VMTaskTimeout-Konfigurationseinstellung wurde überschritten.</span><span class="sxs-lookup"><span data-stu-id="a1f70-159">The end user tried to exit MED-V by logging off or by shutting down the MED-V host, and the VMTaskTimeout configuration setting was exceeded.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="a1f70-160">Lösung</span><span class="sxs-lookup"><span data-stu-id="a1f70-160">Solution</span></span>**  
<span data-ttu-id="a1f70-161">Starten Sie MED-V neu.</span><span class="sxs-lookup"><span data-stu-id="a1f70-161">Restart MED-V.</span></span>

### <span data-ttu-id="a1f70-162">Ereignis-ID 4028</span><span class="sxs-lookup"><span data-stu-id="a1f70-162">Event ID 4028</span></span>

<span data-ttu-id="a1f70-163">Timeout des VM-Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="a1f70-163">VM Operation timed out.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="a1f70-164">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a1f70-164">Description</span></span>**  
<span data-ttu-id="a1f70-165">Der Endbenutzer hat versucht, MED-V durch abmelden oder durch Herunterfahren des Hosts zu beenden, und die VMTaskTimeout-Konfigurationseinstellung wurde überschritten.</span><span class="sxs-lookup"><span data-stu-id="a1f70-165">The end user tried to exit MED-V by logging off or by shutting down the host, and the VMTaskTimeout configuration setting was exceeded.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="a1f70-166">Lösung</span><span class="sxs-lookup"><span data-stu-id="a1f70-166">Solution</span></span>**  
<span data-ttu-id="a1f70-167">Starten Sie MED-V neu.</span><span class="sxs-lookup"><span data-stu-id="a1f70-167">Restart MED-V.</span></span>

### <span data-ttu-id="a1f70-168">Ereignis-ID 4038</span><span class="sxs-lookup"><span data-stu-id="a1f70-168">Event ID 4038</span></span>

<span data-ttu-id="a1f70-169">Vmsal hat eine Fehlermeldung an den Benutzer gesendet.</span><span class="sxs-lookup"><span data-stu-id="a1f70-169">Vmsal posted an error message to the user.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="a1f70-170">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a1f70-170">Description</span></span>**  
<span data-ttu-id="a1f70-171">Dem Endbenutzer wird eine Fehlermeldung angezeigt, die besagt, dass die virtuelle Anwendung von MED-V nicht gestartet werden konnte.</span><span class="sxs-lookup"><span data-stu-id="a1f70-171">An error message is displayed to the end user stating that MED-V could not start the virtual application.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="a1f70-172">Lösung</span><span class="sxs-lookup"><span data-stu-id="a1f70-172">Solution</span></span>**  
<span data-ttu-id="a1f70-173">Wenn der Fehler mindestens zwei Mal hintereinander protokolliert wird, beenden Sie MED-V, und stellen Sie eine Verbindung mit dem virtuellen Computer mithilfe der Windows Virtual PC-Konsole her, und versuchen Sie, die Anwendung im Vollbildmodus zu starten.</span><span class="sxs-lookup"><span data-stu-id="a1f70-173">If the error is logged two or more times in a row, stop MED-V and connect to the virtual machine by using Windows Virtual PC console and attempt to start the application in Full Screen.</span></span>

### <span data-ttu-id="a1f70-174">Ereignis-ID 4040</span><span class="sxs-lookup"><span data-stu-id="a1f70-174">Event ID 4040</span></span>

<span data-ttu-id="a1f70-175">Wiederverwendung von Ergänzungen, da Terminal Services im Gast nicht initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="a1f70-175">Recycling Additions because TerminalServices is not initialized in the guest.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="a1f70-176">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a1f70-176">Description</span></span>**  
<span data-ttu-id="a1f70-177">MED-V hat den virtuellen Computer neu gestartet, weil die Remote Desktop Dienste auf dem virtuellen Computer nicht initialisiert wurden.</span><span class="sxs-lookup"><span data-stu-id="a1f70-177">MED-V rebooted the virtual machine because Remote Desktop Services was not initialized on the virtual machine.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="a1f70-178">Lösung</span><span class="sxs-lookup"><span data-stu-id="a1f70-178">Solution</span></span>**  
<span data-ttu-id="a1f70-179">Wenn der Fehler mindestens zwei Mal hintereinander protokolliert wird, beenden Sie MED-V, und stellen Sie eine Verbindung mit dem virtuellen Computer mithilfe der Windows Virtual PC-Konsole her.</span><span class="sxs-lookup"><span data-stu-id="a1f70-179">If the error is logged two or more times in a row, stop MED-V and connect to the virtual machine by using Windows Virtual PC console.</span></span>

### <span data-ttu-id="a1f70-180">Ereignis-ID 4042</span><span class="sxs-lookup"><span data-stu-id="a1f70-180">Event ID 4042</span></span>

<span data-ttu-id="a1f70-181">Fehler beim wieder verwenden von Zusätzen im Gast.</span><span class="sxs-lookup"><span data-stu-id="a1f70-181">Failed to recycle additions in the guest.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="a1f70-182">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a1f70-182">Description</span></span>**  
<span data-ttu-id="a1f70-183">MED-V konnte keine virtuellen Computer Erweiterungen auf dem virtuellen Computer wieder verwenden.</span><span class="sxs-lookup"><span data-stu-id="a1f70-183">MED-V failed to recycle virtual machine additions on the virtual machine.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="a1f70-184">Lösung</span><span class="sxs-lookup"><span data-stu-id="a1f70-184">Solution</span></span>**  
<span data-ttu-id="a1f70-185">Wenn der Fehler mindestens zwei Mal hintereinander protokolliert wird, beenden Sie MED-V, und stellen Sie eine Verbindung mit dem virtuellen Computer mithilfe der Windows Virtual PC-Konsole her.</span><span class="sxs-lookup"><span data-stu-id="a1f70-185">If the error is logged two or more times in a row, stop MED-V and connect to the virtual machine by using Windows Virtual PC console.</span></span>

### <span data-ttu-id="a1f70-186">Ereignis-ID 4043</span><span class="sxs-lookup"><span data-stu-id="a1f70-186">Event ID 4043</span></span>

<span data-ttu-id="a1f70-187">Fehler beim Zurücksetzen des abgelaufenen Kennworts auf dem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="a1f70-187">Failed to reset expired password in the virtual machine.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="a1f70-188">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a1f70-188">Description</span></span>**  
<span data-ttu-id="a1f70-189">Der Endbenutzer hat das Kennwort auf dem virtuellen Computer nicht zurückgesetzt, bevor es abgelaufen ist.</span><span class="sxs-lookup"><span data-stu-id="a1f70-189">The end user did not reset the password in the virtual machine before it expired.</span></span> <span data-ttu-id="a1f70-190">Daher kann der Benutzer möglicherweise nicht auf Netzwerkressourcen zugreifen oder Arbeit speichern.</span><span class="sxs-lookup"><span data-stu-id="a1f70-190">As a result, the user might not be able to access network resources or save work.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="a1f70-191">Lösung</span><span class="sxs-lookup"><span data-stu-id="a1f70-191">Solution</span></span>**  
<span data-ttu-id="a1f70-192">Beenden Sie den MED-V-Gast, und starten Sie ihn erneut.</span><span class="sxs-lookup"><span data-stu-id="a1f70-192">Shut down the MED-V guest and restart it.</span></span>

### <span data-ttu-id="a1f70-193">URL-Umleitung</span><span class="sxs-lookup"><span data-stu-id="a1f70-193">URL Redirection</span></span>

### <span data-ttu-id="a1f70-194">Ereignis-ID 5005</span><span class="sxs-lookup"><span data-stu-id="a1f70-194">Event ID 5005</span></span>

<span data-ttu-id="a1f70-195">VM-Name konnte nicht aus der Konfiguration abgerufen werden. Gast Browser kann nicht gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="a1f70-195">Couldn’t get VM name from configuration; can’t launch guest browser.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="a1f70-196">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a1f70-196">Description</span></span>**  
<span data-ttu-id="a1f70-197">Die URL-Umleitung konnte den MED-V-Arbeitsbereichsnamen nicht aus der Konfiguration abrufen.</span><span class="sxs-lookup"><span data-stu-id="a1f70-197">URL Redirection could not obtain the MED-V workspace name from the configuration.</span></span> <span data-ttu-id="a1f70-198">Daher kann Windows Virtual PC nicht darüber informiert werden, dass die umgeleitete URL im MED-V Workspace-Browser geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="a1f70-198">As a result, it cannot inform Windows Virtual PC to open the redirected URL in the MED-V workspace browser.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="a1f70-199">Lösung</span><span class="sxs-lookup"><span data-stu-id="a1f70-199">Solution</span></span>**  
<span data-ttu-id="a1f70-200">Stellen Sie sicher, dass der Name des MED-V-Arbeitsbereichs festgesetzt ist und er dem Namen eines virtuellen Computers im C:\\Users\\- &lt; *Benutzer* &gt; \\Virtual Machines-Verzeichnis entspricht.</span><span class="sxs-lookup"><span data-stu-id="a1f70-200">Ensure that the MED-V workspace name is set and that it matches a virtual machine name in the C:\\Users\\&lt;*user*&gt;\\Virtual Machines directory.</span></span> <span data-ttu-id="a1f70-201">Der Name des MED-V-Arbeitsbereichs befindet sich unter HKLM\\SOFTWARE\\Microsoft\\Medv\\v2\\VM\\Name.</span><span class="sxs-lookup"><span data-stu-id="a1f70-201">The MED-V workspace name is located at HKLM\\SOFTWARE\\Microsoft\\Medv\\v2\\VM\\Name.</span></span>

<span data-ttu-id="a1f70-202">Wenn der Benutzer beispielsweise "Matt" ist und der Arbeitsbereichsname "mattsworkspace" lautet, sollte der Wert von HKLM\\SOFTWARE\\Microsoft\\Medv\\v2\\VM\\Name "mattsworkspace" sein, und es sollte eine Datei mit dem Namen C:\\Users\\Matt\\Virtual Machines\\mattsworkspace.vcmx.</span><span class="sxs-lookup"><span data-stu-id="a1f70-202">For example, if the user is "Matt" and the workspace name is "mattsworkspace", the value of HKLM\\SOFTWARE\\Microsoft\\Medv\\v2\\VM\\Name should be "mattsworkspace", and there should be a file that is named C:\\Users\\Matt\\Virtual Machines\\mattsworkspace.vcmx.</span></span>

### <span data-ttu-id="a1f70-203">Ereignis-ID 5006</span><span class="sxs-lookup"><span data-stu-id="a1f70-203">Event ID 5006</span></span>

<span data-ttu-id="a1f70-204">Fehler beim Erstellen des Pipes-Servers.</span><span class="sxs-lookup"><span data-stu-id="a1f70-204">Failed to create pipe server.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="a1f70-205">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a1f70-205">Description</span></span>**  
<span data-ttu-id="a1f70-206">Der URL-Umleitungsdienst konnte den Kanalserver für die Kommunikation mit Internet Explorer nicht erstellen.</span><span class="sxs-lookup"><span data-stu-id="a1f70-206">The URL Redirection service could not create the pipe server to communicate with Internet Explorer.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="a1f70-207">Lösung</span><span class="sxs-lookup"><span data-stu-id="a1f70-207">Solution</span></span>**  
<span data-ttu-id="a1f70-208">Überprüfen Sie die Systemereignisprotokolle auf Versuche, eine Datei oder Ressource zu erstellen, deren Pfad wie folgt beginnt: "\\\\.\\pipe\\MEDVUrlRedirectionPipe\_" und endet mit dem Benutzernamen und dem Domänennamen des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="a1f70-208">Check system event logs for attempts to create a file or resource whose path begins similar to the following: "\\\\.\\pipe\\MEDVUrlRedirectionPipe\_" and ends with the user’s user name and domain name.</span></span> <span data-ttu-id="a1f70-209">Wenn dies im Ereignisprotokoll nicht vorhanden ist, starten Sie den Computer neu.</span><span class="sxs-lookup"><span data-stu-id="a1f70-209">If this is not present in the event log, restart the computer.</span></span>

### <span data-ttu-id="a1f70-210">ConfigMgr (Gast)</span><span class="sxs-lookup"><span data-stu-id="a1f70-210">ConfigMgr (Guest)</span></span>

### <span data-ttu-id="a1f70-211">Ereignis-ID 7001</span><span class="sxs-lookup"><span data-stu-id="a1f70-211">Event ID 7001</span></span>

<span data-ttu-id="a1f70-212">Die Konfigurationsdaten des Host Netzwerks sind nicht ordnungsgemäß formatiert.</span><span class="sxs-lookup"><span data-stu-id="a1f70-212">The host network configuration data is not properly formatted.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="a1f70-213">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a1f70-213">Description</span></span>**  
<span data-ttu-id="a1f70-214">Entweder die vom Host empfangene Netzwerkkonfiguration ist eine falsch formatierte XML-Zeichenfolge, oder die vom Host zurückgegebenen Netzwerkinformationen können nicht in ein XML-Dokument geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="a1f70-214">Either the network configuration received from the host is an incorrectly formatted XML string, or the network information returned from the host cannot be written to an XML document.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="a1f70-215">Lösung</span><span class="sxs-lookup"><span data-stu-id="a1f70-215">Solution</span></span>**  
<span data-ttu-id="a1f70-216">Starten Sie den Hostcomputer und den virtuellen Computer neu.</span><span class="sxs-lookup"><span data-stu-id="a1f70-216">Restart the host computer and the virtual machine.</span></span>

### <span data-ttu-id="a1f70-217">Ereignis-ID 7005</span><span class="sxs-lookup"><span data-stu-id="a1f70-217">Event ID 7005</span></span>

<span data-ttu-id="a1f70-218">Eine Änderung der Host Netzwerkkonfiguration wurde erkannt, konnte aber nicht angewendet werden, da die Konfigurationsdaten des Host Netzwerks nicht ordnungsgemäß formatiert wurden.</span><span class="sxs-lookup"><span data-stu-id="a1f70-218">A change to the host network configuration was detected, but was not able to be applied because the host network configuration data was not properly formatted.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="a1f70-219">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a1f70-219">Description</span></span>**  
<span data-ttu-id="a1f70-220">Eine Änderung an der Host Netzwerkkonfiguration wurde dem virtuellen Computer mitgeteilt, konnte aber aufgrund eines Fehlers nicht auf dem virtuellen Computer verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="a1f70-220">A change to the host network configuration was communicated to the virtual machine, but could not be processed in the virtual machine because of an error.</span></span> <span data-ttu-id="a1f70-221">Dieser Fehler kann durch falsch formatierte Daten oder die Unfähigkeit verursacht werden, die Informationen in der WMI-CCMNetworkAdapter-Instanz (Windows Management Instrumentation) zu setzen.</span><span class="sxs-lookup"><span data-stu-id="a1f70-221">This error could be caused by incorrectly formatted data or the inability to set the information into the Windows Management Instrumentation (WMI) CCMNetworkAdapter instance.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="a1f70-222">Lösung</span><span class="sxs-lookup"><span data-stu-id="a1f70-222">Solution</span></span>**  
<span data-ttu-id="a1f70-223">Starten Sie den Host und den virtuellen Computer neu.</span><span class="sxs-lookup"><span data-stu-id="a1f70-223">Restart the host and virtual machine.</span></span>

### <span data-ttu-id="a1f70-224">ConfigMgr (Host)</span><span class="sxs-lookup"><span data-stu-id="a1f70-224">ConfigMgr (Host)</span></span>

### <span data-ttu-id="a1f70-225">Ereignis-ID 8006</span><span class="sxs-lookup"><span data-stu-id="a1f70-225">Event ID 8006</span></span>

<span data-ttu-id="a1f70-226">Der virtuelle Computer konnte nicht gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="a1f70-226">The virtual machine cannot be found.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="a1f70-227">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a1f70-227">Description</span></span>**  
<span data-ttu-id="a1f70-228">Windows Virtual PC 7 kann den virtuellen Computer nicht finden.</span><span class="sxs-lookup"><span data-stu-id="a1f70-228">Windows Virtual PC 7 cannot locate the virtual machine.</span></span> <span data-ttu-id="a1f70-229">Der virtuelle Computer wurde möglicherweise gelöscht, verschoben, entfernt oder der Zugriff wurde verweigert.</span><span class="sxs-lookup"><span data-stu-id="a1f70-229">The virtual machine might have been deleted, moved, removed, or access was denied.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="a1f70-230">Lösung</span><span class="sxs-lookup"><span data-stu-id="a1f70-230">Solution</span></span>**  
<span data-ttu-id="a1f70-231">Installieren Sie den virtuellen Computer erneut.</span><span class="sxs-lookup"><span data-stu-id="a1f70-231">Reinstall the virtual machine.</span></span>

### <span data-ttu-id="a1f70-232">Ereignis-ID 8008</span><span class="sxs-lookup"><span data-stu-id="a1f70-232">Event ID 8008</span></span>

<span data-ttu-id="a1f70-233">Die Netzwerkkonfigurationsinformationen der Arbeitsstation konnten nicht abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="a1f70-233">The workstation's network configuration information could not be retrieved.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="a1f70-234">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a1f70-234">Description</span></span>**  
<span data-ttu-id="a1f70-235">Netzwerkkonfigurationsinformationen konnten nicht vom MED-V-Host erfasst werden, wahrscheinlich wegen eines Systemanruf Fehlers in .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="a1f70-235">Network configuration information could not be collected from the MED-V host, most likely because of a system call failure in the .NET Framework.</span></span> <span data-ttu-id="a1f70-236">Dieser Fehler kann auch auftreten, wenn die vom MED-V-Host zurückgegebenen Netzwerkinformationen nicht in ein XML-Dokument geschrieben werden können.</span><span class="sxs-lookup"><span data-stu-id="a1f70-236">This failure can also occur if the network information returned from the MED-V host cannot be written to an XML document.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="a1f70-237">Lösung</span><span class="sxs-lookup"><span data-stu-id="a1f70-237">Solution</span></span>**  
<span data-ttu-id="a1f70-238">Starten Sie die Host Arbeitsstation neu.</span><span class="sxs-lookup"><span data-stu-id="a1f70-238">Restart the host workstation.</span></span>

### <span data-ttu-id="a1f70-239">Ereignis-ID 8010</span><span class="sxs-lookup"><span data-stu-id="a1f70-239">Event ID 8010</span></span>

<span data-ttu-id="a1f70-240">Die Netzwerkkonfigurationsdaten konnten auf dem virtuellen Computer nicht eingerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="a1f70-240">The network configuration data could not be set in the virtual machine.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="a1f70-241">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a1f70-241">Description</span></span>**  
<span data-ttu-id="a1f70-242">Die MED-V-hostnetwork-Adressübersetzung (NAT) konnte nicht an den virtuellen Computer übermittelt werden, wahrscheinlich, weil sich der virtuelle Computer in einem fehlerhaften Zustand befindet oder die Windows Virtual PC-Erweiterungen nicht installiert oder aktiviert wurden.</span><span class="sxs-lookup"><span data-stu-id="a1f70-242">The MED-V hostnetwork address translation (NAT) could not be communicated to the virtual machine, most likely because the virtual machine is in a bad state or the Windows Virtual PC Additions were not installed or enabled.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="a1f70-243">Lösung</span><span class="sxs-lookup"><span data-stu-id="a1f70-243">Solution</span></span>**  
<span data-ttu-id="a1f70-244">Beenden Sie den virtuellen Computer, und starten Sie ihn erneut.</span><span class="sxs-lookup"><span data-stu-id="a1f70-244">Shut down and restart the virtual machine.</span></span> <span data-ttu-id="a1f70-245">Darüber hinaus müssen Sie möglicherweise den virtuellen Computer erneut installieren.</span><span class="sxs-lookup"><span data-stu-id="a1f70-245">In addition, you might have to reinstall the virtual machine.</span></span>

### <span data-ttu-id="a1f70-246">Ereignis-ID 8011</span><span class="sxs-lookup"><span data-stu-id="a1f70-246">Event ID 8011</span></span>

<span data-ttu-id="a1f70-247">Die Netzwerkkonfigurationsdaten konnten auf dem virtuellen Computer nicht zurückgesetzt werden.</span><span class="sxs-lookup"><span data-stu-id="a1f70-247">The network configuration data could not be reset in the virtual machine.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="a1f70-248">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a1f70-248">Description</span></span>**  
<span data-ttu-id="a1f70-249">Die MED-V-hostnetwork-Konfiguration (Bridged) konnte nicht an den virtuellen Computer übermittelt werden, wahrscheinlich, weil sich der virtuelle Computer in einem fehlerhaften Zustand befindet oder die Windows Virtual PC-Erweiterungen nicht installiert oder aktiviert wurden.</span><span class="sxs-lookup"><span data-stu-id="a1f70-249">The MED-V hostnetwork configuration (BRIDGED) could not be communicated to the virtual machine, most likely because the virtual machine is in a bad state or the Windows Virtual PC Additions were not installed or enabled.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="a1f70-250">Lösung</span><span class="sxs-lookup"><span data-stu-id="a1f70-250">Solution</span></span>**  
<span data-ttu-id="a1f70-251">Beenden Sie den virtuellen Computer, und starten Sie ihn erneut.</span><span class="sxs-lookup"><span data-stu-id="a1f70-251">Shut down and restart the virtual machine.</span></span> <span data-ttu-id="a1f70-252">Darüber hinaus müssen Sie möglicherweise den virtuellen Computer erneut installieren.</span><span class="sxs-lookup"><span data-stu-id="a1f70-252">In addition, you might have to reinstall the virtual machine.</span></span>

### <span data-ttu-id="a1f70-253">Druckerumleitung</span><span class="sxs-lookup"><span data-stu-id="a1f70-253">Printer Redirection</span></span>

### <span data-ttu-id="a1f70-254">Ereignis-ID 9001</span><span class="sxs-lookup"><span data-stu-id="a1f70-254">Event ID 9001</span></span>

<span data-ttu-id="a1f70-255">Fehler bei der Datei Berechtigung.</span><span class="sxs-lookup"><span data-stu-id="a1f70-255">File Permission Error.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="a1f70-256">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a1f70-256">Description</span></span>**  
<span data-ttu-id="a1f70-257">Der Endbenutzer ist nicht berechtigt, auf den Ordner zuzugreifen, der zum Öffnen oder Erstellen der MED-V-Druckerdatei zum Lesen erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="a1f70-257">The end user is not authorized to access the folder required to open or create the MED-V printer file for reading.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="a1f70-258">Lösung</span><span class="sxs-lookup"><span data-stu-id="a1f70-258">Solution</span></span>**  
<span data-ttu-id="a1f70-259">Stellen Sie sicher, dass auf den User\\AppData\\-Pfad zugegriffen werden kann und dass der Benutzer die Berechtigung zum Lesen und schreiben hat.</span><span class="sxs-lookup"><span data-stu-id="a1f70-259">Verify that the User\\AppData\\ path can be accessed and that the user has permission to read and write to it.</span></span> <span data-ttu-id="a1f70-260">Wenn der Benutzer beispielsweise "Matt" ist, sollte der Pfad C:\\Users\\Matt\\AppData\\ und alle darin enthaltenen Dateien über Lese-und Schreibberechtigungen verfügen.</span><span class="sxs-lookup"><span data-stu-id="a1f70-260">For example, if the user is "Matt", the path C:\\Users\\Matt\\AppData\\, and all files therein should have Read and Write permissions.</span></span> <span data-ttu-id="a1f70-261">Und falls vorhanden, sollten der Pfad C:\\Users\\Matt\\AppData\\Local\\Microsoft\\MEDV\\v2\\ und alle darin enthaltenen Dateien über Lese-und Schreibberechtigungen verfügen.</span><span class="sxs-lookup"><span data-stu-id="a1f70-261">And if it exists, the path C:\\Users\\Matt\\AppData\\Local\\Microsoft\\MEDV\\v2\\ and all files therein should have Read and Write permissions.</span></span>

### <span data-ttu-id="a1f70-262">Ereignis-ID 9002</span><span class="sxs-lookup"><span data-stu-id="a1f70-262">Event ID 9002</span></span>

<span data-ttu-id="a1f70-263">Fehler bei der Datei Berechtigung.</span><span class="sxs-lookup"><span data-stu-id="a1f70-263">File Permission Error.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="a1f70-264">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a1f70-264">Description</span></span>**  
<span data-ttu-id="a1f70-265">Der Endbenutzer ist nicht berechtigt, auf den Ordner zuzugreifen, der zum Öffnen oder Erstellen der MED-V-Druckerdatei zum Schreiben erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="a1f70-265">The end user is not authorized to access the folder required to open or create the MED-V printer file for writing.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="a1f70-266">Lösung</span><span class="sxs-lookup"><span data-stu-id="a1f70-266">Solution</span></span>**  
<span data-ttu-id="a1f70-267">Stellen Sie sicher, dass auf den User\\AppData\\-Pfad zugegriffen werden kann und dass der Benutzer die Berechtigung zum Lesen und schreiben besitzt.</span><span class="sxs-lookup"><span data-stu-id="a1f70-267">Ensure that the User\\AppData\\ path can be accessed, and that the user has permission to read and write to it.</span></span> <span data-ttu-id="a1f70-268">Wenn der Benutzer beispielsweise "Matt" ist, sollte der Pfad C:\\Users\\Matt\\AppData\\ und alle darin enthaltenen Dateien über Lese-und Schreibberechtigungen verfügen.</span><span class="sxs-lookup"><span data-stu-id="a1f70-268">For example, if the user is "Matt", the path C:\\Users\\Matt\\AppData\\ and all files therein should have Read and Write permissions.</span></span> <span data-ttu-id="a1f70-269">Und falls vorhanden, sollten der Pfad C:\\Users\\Matt\\AppData\\Local\\Microsoft\\MEDV\\v2\\ und alle darin enthaltenen Dateien über Lese-und Schreibberechtigungen verfügen.</span><span class="sxs-lookup"><span data-stu-id="a1f70-269">And if it exists, the path C:\\Users\\Matt\\AppData\\Local\\Microsoft\\MEDV\\v2\\ and all files therein should have Read and Write permissions.</span></span>

### <span data-ttu-id="a1f70-270">Ereignis-ID 9004</span><span class="sxs-lookup"><span data-stu-id="a1f70-270">Event ID 9004</span></span>

<span data-ttu-id="a1f70-271">Der Pfad zum Speichern von MEDV-Drucker Dateien konnte nicht erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="a1f70-271">Could not create path for storing MEDV printer files.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="a1f70-272">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a1f70-272">Description</span></span>**  
<span data-ttu-id="a1f70-273">Der Drucker Umleitungsdienst konnte nicht auf Dateien zugreifen oder Verzeichnisse erstellen, die zum Speichern der Druckerinformationen erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="a1f70-273">The printer redirection service could not access files or create directories required for storing the printer information.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="a1f70-274">Lösung</span><span class="sxs-lookup"><span data-stu-id="a1f70-274">Solution</span></span>**  
<span data-ttu-id="a1f70-275">Stellen Sie sicher, dass auf den User\\AppData\\-Pfad zugegriffen werden kann und dass der Benutzer die Berechtigung zum Lesen und schreiben hat.</span><span class="sxs-lookup"><span data-stu-id="a1f70-275">Verify that the User\\AppData\\ path can be accessed and that the user has permission to read and write to it.</span></span> <span data-ttu-id="a1f70-276">Wenn der Benutzer beispielsweise "Matt" ist, sollte der Pfad C:\\Users\\Matt\\AppData\\ und alle darin enthaltenen Dateien über Lese-und Schreibberechtigungen verfügen.</span><span class="sxs-lookup"><span data-stu-id="a1f70-276">For example, if the user is "Matt", the path C:\\Users\\Matt\\AppData\\ and all files therein should have Read and Write permissions.</span></span> <span data-ttu-id="a1f70-277">Und falls vorhanden, sollten der Pfad C:\\Users\\Matt\\AppData\\Local\\Microsoft\\MEDV\\v2\\ und alle darin enthaltenen Dateien über Lese-und Schreibberechtigungen verfügen.</span><span class="sxs-lookup"><span data-stu-id="a1f70-277">And if it exists, the path C:\\Users\\Matt\\AppData\\Local\\Microsoft\\MEDV\\v2\\ and all files therein should have Read and Write permissions.</span></span>

### <span data-ttu-id="a1f70-278">Ereignis-ID 9005</span><span class="sxs-lookup"><span data-stu-id="a1f70-278">Event ID 9005</span></span>

<span data-ttu-id="a1f70-279">VM-Name konnte nicht aus der Konfiguration abgerufen werden. Gast-Installationsprogramm kann nicht gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="a1f70-279">Couldn’t get VM name from configuration; cannot launch guest installer.</span></span> <span data-ttu-id="a1f70-280">MED-V kann nicht aktualisiert werden – kein Host Netzwerk erkannt.</span><span class="sxs-lookup"><span data-stu-id="a1f70-280">Cannot update MED-V – No host network detected.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="a1f70-281">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a1f70-281">Description</span></span>**  
<span data-ttu-id="a1f70-282">Der Drucker Umleitungsdienst konnte den Med-v-Arbeitsbereichsnamen nicht aus der Med-v-Konfiguration abrufen und kann Windows Virtual PC nicht informieren, um das Installationsprogramm auf dem Med-v-Gast zu starten.</span><span class="sxs-lookup"><span data-stu-id="a1f70-282">The printer redirection service was not able to obtain the MED-V workspace name from the MED-V configuration and cannot inform Windows Virtual PC to start the installer on the MED-V guest.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="a1f70-283">Lösung</span><span class="sxs-lookup"><span data-stu-id="a1f70-283">Solution</span></span>**  
<span data-ttu-id="a1f70-284">Stellen Sie sicher, dass der Name des MED-V-Arbeitsbereichs festgesetzt ist und er dem Namen eines virtuellen Computers im C:\\Users\\- &lt; *Benutzer* &gt; \\Virtual Machines-Verzeichnis entspricht.</span><span class="sxs-lookup"><span data-stu-id="a1f70-284">Ensure that the MED-V workspace name is set and that it matches a virtual machine name in the C:\\Users\\&lt;*user*&gt;\\Virtual Machines directory.</span></span> <span data-ttu-id="a1f70-285">Der Name des MED-V-Arbeitsbereichs befindet sich unter HKLM\\SOFTWARE\\Microsoft\\Medv\\v2\\VM\\Name.</span><span class="sxs-lookup"><span data-stu-id="a1f70-285">The MED-V workspace name is located at HKLM\\SOFTWARE\\Microsoft\\Medv\\v2\\VM\\Name.</span></span>

<span data-ttu-id="a1f70-286">Wenn der Benutzer beispielsweise "Matt" ist und der Arbeitsbereichsname "mattsworkspace" lautet, sollte der Wert von HKLM\\SOFTWARE\\Microsoft\\Medv\\v2\\VM\\Name "mattsworkspace" sein, und es sollte eine Datei mit dem Namen C:\\Users\\Matt\\Virtual Machines\\mattsworkspace.vcmx.</span><span class="sxs-lookup"><span data-stu-id="a1f70-286">For example, if the user is "Matt" and the workspace name is "mattsworkspace", the value of HKLM\\SOFTWARE\\Microsoft\\Medv\\v2\\VM\\Name should be "mattsworkspace" and there should be a file that is named C:\\Users\\Matt\\Virtual Machines\\mattsworkspace.vcmx.</span></span>

### <span data-ttu-id="a1f70-287">Anwendungsveröffentlichung</span><span class="sxs-lookup"><span data-stu-id="a1f70-287">Application Publishing</span></span>

### <span data-ttu-id="a1f70-288">Ereignis-ID 10015</span><span class="sxs-lookup"><span data-stu-id="a1f70-288">Event ID 10015</span></span>

<span data-ttu-id="a1f70-289">Beim Abgleichvorgang ist ein Dateisystemfehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="a1f70-289">A file system error occurred during the reconcile process.</span></span> <span data-ttu-id="a1f70-290">Der Prozess "abstimmen" verarbeitet nicht den Datei &lt; *Namen* &gt; , sondern verarbeitet weiterhin alle anderen Änderungen.</span><span class="sxs-lookup"><span data-stu-id="a1f70-290">The reconcile process will not process the file &lt;*filename*&gt; but will continue to process any other changes.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="a1f70-291">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a1f70-291">Description</span></span>**  
<span data-ttu-id="a1f70-292">Beim Erstellen oder Löschen einer Verknüpfung ist ein nicht autorisierter Zugriffs-oder e/a-Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="a1f70-292">An unauthorized access or I/O error occurred when a shortcut was being created or deleted.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="a1f70-293">Lösung</span><span class="sxs-lookup"><span data-stu-id="a1f70-293">Solution</span></span>**  
<span data-ttu-id="a1f70-294">Stellen Sie sicher, dass auf den Dateipfad zugegriffen werden kann und der Benutzer über die Berechtigungen zum Erstellen oder Löschen der angegebenen Datei verfügt.</span><span class="sxs-lookup"><span data-stu-id="a1f70-294">Check that the file path can be accessed and that the user has permissions to create or delete the specified file.</span></span>

### <span data-ttu-id="a1f70-295">Ereignis-ID 10021</span><span class="sxs-lookup"><span data-stu-id="a1f70-295">Event ID 10021</span></span>

<span data-ttu-id="a1f70-296">Fehler &lt; *Fehler \ _information* &gt; für den Dateivorgangs &lt; *Vorgang \ _name* für &gt; den Datei &lt; *Namen* &gt; .</span><span class="sxs-lookup"><span data-stu-id="a1f70-296">Error &lt;*error\_information*&gt; for file operation &lt;*operation\_name*&gt; on file &lt;*filename*&gt;.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="a1f70-297">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a1f70-297">Description</span></span>**  
<span data-ttu-id="a1f70-298">Beim Erstellen oder Löschen einer Verknüpfung ist ein nicht autorisierter Zugriffs-oder e/a-Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="a1f70-298">An unauthorized access or I/O error occurred when a shortcut was being created or deleted.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="a1f70-299">Lösung</span><span class="sxs-lookup"><span data-stu-id="a1f70-299">Solution</span></span>**  
<span data-ttu-id="a1f70-300">Stellen Sie sicher, dass auf den Dateipfad zugegriffen werden kann und der Benutzer über die Berechtigungen zum Erstellen oder Löschen der angegebenen Datei verfügt.</span><span class="sxs-lookup"><span data-stu-id="a1f70-300">Check that the file path can be accessed and that the user has permissions to create or delete the specified file.</span></span>

### <span data-ttu-id="a1f70-301">Gast-Patches</span><span class="sxs-lookup"><span data-stu-id="a1f70-301">Guest Patching</span></span>

### <span data-ttu-id="a1f70-302">Ereignis-ID 11001</span><span class="sxs-lookup"><span data-stu-id="a1f70-302">Event ID 11001</span></span>

<span data-ttu-id="a1f70-303">Nachricht zur Verwendung der Weckfunktion für Gäste</span><span class="sxs-lookup"><span data-stu-id="a1f70-303">Guest wakeup task usage message.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="a1f70-304">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a1f70-304">Description</span></span>**  
<span data-ttu-id="a1f70-305">MedvHost.exe mit der Option "/GuestWakeup" falsch ausgeführt wurde oder der Befehl falsch formatiert ist.</span><span class="sxs-lookup"><span data-stu-id="a1f70-305">MedvHost.exe with the /GuestWakeup option was executed incorrectly, or the command is formatted incorrectly.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="a1f70-306">Lösung</span><span class="sxs-lookup"><span data-stu-id="a1f70-306">Solution</span></span>**  
<span data-ttu-id="a1f70-307">Stellen Sie sicher, dass der Befehl mit dem folgenden Format ausgeführt wird:</span><span class="sxs-lookup"><span data-stu-id="a1f70-307">Ensure that the command is executed with the following format:</span></span>

<span data-ttu-id="a1f70-308">Medvhost.exe/GuestWakeup/d: &lt; *Duration \ _in \ _minutes* &gt; /v: " &lt; *Arbeitsbereich \ _name* &gt; ", wobei</span><span class="sxs-lookup"><span data-stu-id="a1f70-308">Medvhost.exe /GuestWakeup /d:&lt; *duration\_in\_minutes*&gt; /v:”&lt; *workspace\_name*&gt;” where</span></span>

<span data-ttu-id="a1f70-309">&lt;*Dauer \ _in \ _minutes* &gt; Gibt an, wie viele Minuten die virtuelle Maschine wach bleiben soll (Standard ist 240) und</span><span class="sxs-lookup"><span data-stu-id="a1f70-309">&lt;*duration\_in\_minutes*&gt; is the number of minutes that the virtual machine should stay awake (default is 240) and</span></span>

<span data-ttu-id="a1f70-310">&lt;*Arbeitsbereich \ _name* &gt; der Name des virtuellen Computers, der geweckt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a1f70-310">&lt;*workspace\_name*&gt; is the name of the virtual machine that should be awakened.</span></span>

### <span data-ttu-id="a1f70-311">Ereignis-ID 11002</span><span class="sxs-lookup"><span data-stu-id="a1f70-311">Event ID 11002</span></span>

<span data-ttu-id="a1f70-312">MED-V kann nicht aktualisiert werden – kein Host Netzwerk erkannt.</span><span class="sxs-lookup"><span data-stu-id="a1f70-312">Cannot update MED-V – No host network detected.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="a1f70-313">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a1f70-313">Description</span></span>**  
<span data-ttu-id="a1f70-314">Gast-Patches konnten nicht abgeschlossen werden, da keine Host-Netzwerkverbindung gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="a1f70-314">Guest patching could not finish because no host network connection was detected.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="a1f70-315">Lösung</span><span class="sxs-lookup"><span data-stu-id="a1f70-315">Solution</span></span>**  
<span data-ttu-id="a1f70-316">Verbinden Sie den MED-V-Host mit einer aktiven Netzwerkverbindung, bevor Sie den Gast-Patch ausführen.</span><span class="sxs-lookup"><span data-stu-id="a1f70-316">Connect the MED-V host to an active network connection before you run guest patching.</span></span>

### <span data-ttu-id="a1f70-317">Ereignis-ID 11003</span><span class="sxs-lookup"><span data-stu-id="a1f70-317">Event ID 11003</span></span>

<span data-ttu-id="a1f70-318">Der MED-V-Host, der nicht auf einem/C-powerFailed ausgeführt wird, kann nicht aktualisiert werden, um einen Kanalserver zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="a1f70-318">Cannot update MED-V – Host not running on A/C powerFailed to create pipe server.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="a1f70-319">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a1f70-319">Description</span></span>**  
<span data-ttu-id="a1f70-320">Guest-Patches konnten nicht abgeschlossen werden, da der Host anscheinend auf Akkustrom und nicht auf einem Netzkabel läuft.</span><span class="sxs-lookup"><span data-stu-id="a1f70-320">Guest patching could not finish because the host appears to be running on battery power instead of from a power cord.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="a1f70-321">Lösung</span><span class="sxs-lookup"><span data-stu-id="a1f70-321">Solution</span></span>**  
<span data-ttu-id="a1f70-322">Verbinden Sie den Hostcomputer mit einem Netzkabel, bevor Sie den Gast Patchen ausführen.</span><span class="sxs-lookup"><span data-stu-id="a1f70-322">Connect the host computer to a power cord before you run guest patching.</span></span>

### <span data-ttu-id="a1f70-323">Client-UX</span><span class="sxs-lookup"><span data-stu-id="a1f70-323">Client UX</span></span>

### <span data-ttu-id="a1f70-324">Ereignis-ID 14003</span><span class="sxs-lookup"><span data-stu-id="a1f70-324">Event ID 14003</span></span>

<span data-ttu-id="a1f70-325">Die folgende Tray-Statusmeldung war zu lang und konnte nicht angezeigt werden: &lt; *Tray \ _status \ _message*&gt;</span><span class="sxs-lookup"><span data-stu-id="a1f70-325">The following tray status message was too long and could not be displayed: &lt;*tray\_status\_message*&gt;</span></span>

<a href="" id="description"></a>**<span data-ttu-id="a1f70-326">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a1f70-326">Description</span></span>**  
<span data-ttu-id="a1f70-327">MED-V hat eine unerwartete Zeichenfolge erstellt, die für die QuickInfo-oder Sprechblasenmeldung der Taskleiste zu lang war.</span><span class="sxs-lookup"><span data-stu-id="a1f70-327">MED-V created an unanticipated string that was too long for the tray tooltip or balloon message.</span></span> <span data-ttu-id="a1f70-328">Daher wurde die angezeigte Nachricht abgeschnitten.</span><span class="sxs-lookup"><span data-stu-id="a1f70-328">As a result, the displayed message was truncated.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="a1f70-329">Lösung</span><span class="sxs-lookup"><span data-stu-id="a1f70-329">Solution</span></span>**  
<span data-ttu-id="a1f70-330">Dies ist ein seltener Fehler, der auftreten kann, wenn MED-V den QuickInfo-Text nach dem Zufallsprinzip erstellt.</span><span class="sxs-lookup"><span data-stu-id="a1f70-330">This is a rare error that can occur when MED-V is randomly creating the tooltip text.</span></span> <span data-ttu-id="a1f70-331">Es gibt keine Lösung.</span><span class="sxs-lookup"><span data-stu-id="a1f70-331">There is no solution.</span></span>

### <span data-ttu-id="a1f70-332">Ereignis-ID 14004</span><span class="sxs-lookup"><span data-stu-id="a1f70-332">Event ID 14004</span></span>

<span data-ttu-id="a1f70-333">MED-V wurde aufgrund einer nicht behandelten Ausnahme angehalten.</span><span class="sxs-lookup"><span data-stu-id="a1f70-333">MED-V stopped due to an unhandled exception.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="a1f70-334">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a1f70-334">Description</span></span>**  
<span data-ttu-id="a1f70-335">Eine nicht behandelte Ausnahme hat dazu geführt, dass MED-V unerwartet beendet wird.</span><span class="sxs-lookup"><span data-stu-id="a1f70-335">An unhandled exception caused MED-V to stop unexpectedly.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="a1f70-336">Lösung</span><span class="sxs-lookup"><span data-stu-id="a1f70-336">Solution</span></span>**  
<span data-ttu-id="a1f70-337">Starten Sie MED-V neu.</span><span class="sxs-lookup"><span data-stu-id="a1f70-337">Restart MED-V.</span></span>

### <span data-ttu-id="a1f70-338">Ereignis-ID 14005</span><span class="sxs-lookup"><span data-stu-id="a1f70-338">Event ID 14005</span></span>

<span data-ttu-id="a1f70-339">Der Server hat versucht, Mutex zu erstellen, aber bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="a1f70-339">Server attempted to create mutex but it already existed.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="a1f70-340">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a1f70-340">Description</span></span>**  
<span data-ttu-id="a1f70-341">Eine zweite Instanz von MedvHost.exe bleibt im Arbeitsspeicher hängen.</span><span class="sxs-lookup"><span data-stu-id="a1f70-341">A second instance of MedvHost.exe is stuck in memory.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="a1f70-342">Lösung</span><span class="sxs-lookup"><span data-stu-id="a1f70-342">Solution</span></span>**  
<span data-ttu-id="a1f70-343">Öffnen Sie Task Manager, und beenden Sie alle MedvHost.exe Prozesse.</span><span class="sxs-lookup"><span data-stu-id="a1f70-343">Open TaskManager and end all MedvHost.exe processes.</span></span>

### <span data-ttu-id="a1f70-344">Ereignis-ID 14006</span><span class="sxs-lookup"><span data-stu-id="a1f70-344">Event ID 14006</span></span>

<span data-ttu-id="a1f70-345">Fehler beim Ändern oder Löschen der Registrierungswert &lt; *Registrierung \ _Value* &gt; .</span><span class="sxs-lookup"><span data-stu-id="a1f70-345">Error modifying or deleting registry value &lt;*registry\_value*&gt;.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="a1f70-346">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a1f70-346">Description</span></span>**  
<span data-ttu-id="a1f70-347">MED-V kann den angegebenen Eintrag in der Registrierung nicht ändern.</span><span class="sxs-lookup"><span data-stu-id="a1f70-347">MED-V is unable to modify the specified entry in the registry.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="a1f70-348">Lösung</span><span class="sxs-lookup"><span data-stu-id="a1f70-348">Solution</span></span>**  
<span data-ttu-id="a1f70-349">Stellen Sie sicher, dass Sie MED-V mit administrativen Anmeldeinformationen installieren oder deinstallieren.</span><span class="sxs-lookup"><span data-stu-id="a1f70-349">Ensure that you install or uninstall MED-V with administrative credentials.</span></span>

### <span data-ttu-id="a1f70-350">Ereignis-ID 14007</span><span class="sxs-lookup"><span data-stu-id="a1f70-350">Event ID 14007</span></span>

<span data-ttu-id="a1f70-351">Die angegebene Datei ( &lt; *filename* &gt; ) ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="a1f70-351">The file specified (&lt;*filename*&gt;) is not valid.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="a1f70-352">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a1f70-352">Description</span></span>**  
<span data-ttu-id="a1f70-353">Während der Installation oder Deinstallation wurde eine beschädigte temporäre Datei an den MED-V-Host übergeben.</span><span class="sxs-lookup"><span data-stu-id="a1f70-353">During install or uninstall, a corrupted temp file was passed to MED-V host.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="a1f70-354">Lösung</span><span class="sxs-lookup"><span data-stu-id="a1f70-354">Solution</span></span>**  
<span data-ttu-id="a1f70-355">Löschen Sie alle Dateien im Ordner Temp, und installieren oder deinstallieren Sie MED-V erneut.</span><span class="sxs-lookup"><span data-stu-id="a1f70-355">Delete all files in the Temp folder and reinstall or uninstall MED-V.</span></span>

### <span data-ttu-id="a1f70-356">Ereignis-ID 14008</span><span class="sxs-lookup"><span data-stu-id="a1f70-356">Event ID 14008</span></span>

<span data-ttu-id="a1f70-357">Datei nicht gefunden: &lt; *Dateiname* &gt; .</span><span class="sxs-lookup"><span data-stu-id="a1f70-357">File not found: &lt;*filename*&gt;.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="a1f70-358">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a1f70-358">Description</span></span>**  
<span data-ttu-id="a1f70-359">Während der Installation oder Deinstallation wurde ein Pfad einer erforderlichen temporären Datei nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="a1f70-359">During install or uninstall, a path of a required temp file was not found.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="a1f70-360">Lösung</span><span class="sxs-lookup"><span data-stu-id="a1f70-360">Solution</span></span>**  
<span data-ttu-id="a1f70-361">Löschen Sie alle Dateien im Ordner Temp, und installieren oder deinstallieren Sie MED-V erneut.</span><span class="sxs-lookup"><span data-stu-id="a1f70-361">Delete all files in the Temp folder and reinstall or uninstall MED-V.</span></span>

### <span data-ttu-id="a1f70-362">Ereignis-ID 14009</span><span class="sxs-lookup"><span data-stu-id="a1f70-362">Event ID 14009</span></span>

<span data-ttu-id="a1f70-363">Parameterdatei Dateiname kann nicht gelesen werden &lt; *filename* &gt; .</span><span class="sxs-lookup"><span data-stu-id="a1f70-363">Unable to read parameter file &lt;*filename*&gt;.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="a1f70-364">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a1f70-364">Description</span></span>**  
<span data-ttu-id="a1f70-365">Während des Installations-oder Deinstallationsvorgangs konnte MED-V keine temporäre Datei lesen.</span><span class="sxs-lookup"><span data-stu-id="a1f70-365">During the install or uninstall process, MED-V was unable to read a temp file.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="a1f70-366">Lösung</span><span class="sxs-lookup"><span data-stu-id="a1f70-366">Solution</span></span>**  
<span data-ttu-id="a1f70-367">Löschen Sie alle Dateien im Ordner Temp, und installieren oder deinstallieren Sie MED-V erneut.</span><span class="sxs-lookup"><span data-stu-id="a1f70-367">Delete all files in the Temp folder and reinstall or uninstall MED-V.</span></span> <span data-ttu-id="a1f70-368">Stellen Sie außerdem sicher, dass der Benutzer über die erforderlichen Rechte und Berechtigungen für den temporären Ordner verfügt.</span><span class="sxs-lookup"><span data-stu-id="a1f70-368">In addition, verify that the user has the necessary rights and permissions to the Temp folder.</span></span>

### <span data-ttu-id="a1f70-369">Ereignis-ID 14010</span><span class="sxs-lookup"><span data-stu-id="a1f70-369">Event ID 14010</span></span>

<span data-ttu-id="a1f70-370">Fehler beim Deserialisieren der Parameterdatei &lt; *Dateiname* &gt; .</span><span class="sxs-lookup"><span data-stu-id="a1f70-370">Error deserializing parameter file &lt;*filename*&gt;.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="a1f70-371">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a1f70-371">Description</span></span>**  
<span data-ttu-id="a1f70-372">Während des Installations-oder Deinstallationsprozesses hat MED-V eine beschädigte temporäre Datei gefunden.</span><span class="sxs-lookup"><span data-stu-id="a1f70-372">During the install or uninstall process, MED-V encountered a corrupted temp file.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="a1f70-373">Lösung</span><span class="sxs-lookup"><span data-stu-id="a1f70-373">Solution</span></span>**  
<span data-ttu-id="a1f70-374">Löschen Sie alle Dateien im Ordner Temp, und installieren oder deinstallieren Sie MED-V erneut.</span><span class="sxs-lookup"><span data-stu-id="a1f70-374">Delete all files in the Temp folder and reinstall or uninstall MED-V.</span></span> <span data-ttu-id="a1f70-375">Stellen Sie außerdem sicher, dass der Benutzer über die erforderlichen Rechte und Berechtigungen für den temporären Ordner verfügt.</span><span class="sxs-lookup"><span data-stu-id="a1f70-375">In addition, verify that the user has the necessary rights and permissions to the Temp folder.</span></span>

### <span data-ttu-id="a1f70-376">Ereignis-ID 14011</span><span class="sxs-lookup"><span data-stu-id="a1f70-376">Event ID 14011</span></span>

<span data-ttu-id="a1f70-377">Unerwarteter Fehler beim Deserialisieren der Parameterdatei &lt; *Dateiname* &gt; .</span><span class="sxs-lookup"><span data-stu-id="a1f70-377">Unexpected error deserializing parameter file &lt;*filename*&gt;.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="a1f70-378">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a1f70-378">Description</span></span>**  
<span data-ttu-id="a1f70-379">Während des Installations-oder Deinstallationsprozesses hat MED-V eine beschädigte temporäre Datei gefunden.</span><span class="sxs-lookup"><span data-stu-id="a1f70-379">During the install or uninstall process, MED-V encountered a corrupted temp file.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="a1f70-380">Lösung</span><span class="sxs-lookup"><span data-stu-id="a1f70-380">Solution</span></span>**  
<span data-ttu-id="a1f70-381">Löschen Sie alle Dateien im Ordner Temp, und installieren oder deinstallieren Sie MED-V erneut.</span><span class="sxs-lookup"><span data-stu-id="a1f70-381">Delete all files in the Temp folder and reinstall or uninstall MED-V.</span></span> <span data-ttu-id="a1f70-382">Stellen Sie außerdem sicher, dass der Benutzer über die erforderlichen Rechte und Berechtigungen für den temporären Ordner verfügt.</span><span class="sxs-lookup"><span data-stu-id="a1f70-382">In addition, verify that the user has the necessary rights and permissions to the Temp folder.</span></span>

### <span data-ttu-id="a1f70-383">Ereignis-ID 14012</span><span class="sxs-lookup"><span data-stu-id="a1f70-383">Event ID 14012</span></span>

<span data-ttu-id="a1f70-384">Unerwarteter Fehler, wenn Einstellungs Rechte für Ordner &lt; *Ordner \ _name* &gt; für Benutzer Benutzer &lt; *Name* &gt; .</span><span class="sxs-lookup"><span data-stu-id="a1f70-384">Unexpected error when settings rights on folder &lt;*folder\_name*&gt; for user &lt;*username*&gt;.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="a1f70-385">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a1f70-385">Description</span></span>**  
<span data-ttu-id="a1f70-386">Es tritt ein Fehler auf, wenn MED-V während der Installation nicht in der Lage ist, Rechte und Berechtigungen für bestimmte Ordner festzulegen.</span><span class="sxs-lookup"><span data-stu-id="a1f70-386">An error occurs when MED-V is unable to set rights and permissions on certain folders during installation.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="a1f70-387">Lösung</span><span class="sxs-lookup"><span data-stu-id="a1f70-387">Solution</span></span>**  
<span data-ttu-id="a1f70-388">Überprüfen Sie die Administratorrechte für die folgenden Ordner:</span><span class="sxs-lookup"><span data-stu-id="a1f70-388">Check the administrator rights to the following folders:</span></span>

<span data-ttu-id="a1f70-389">@"%ProgramData%\\Microsoft\\Medv\\AllUsers"</span><span class="sxs-lookup"><span data-stu-id="a1f70-389">@"%ProgramData%\\Microsoft\\Medv\\AllUsers"</span></span>

<span data-ttu-id="a1f70-390">@"%ProgramData%\\Microsoft\\Medv\\MedvLock"</span><span class="sxs-lookup"><span data-stu-id="a1f70-390">@"%ProgramData%\\Microsoft\\Medv\\MedvLock"</span></span>

<span data-ttu-id="a1f70-391">@"%ProgramData%\\Microsoft\\Medv\\Monitoring"</span><span class="sxs-lookup"><span data-stu-id="a1f70-391">@"%ProgramData%\\Microsoft\\Medv\\Monitoring"</span></span>

### <span data-ttu-id="a1f70-392">Ereignis-ID 14013</span><span class="sxs-lookup"><span data-stu-id="a1f70-392">Event ID 14013</span></span>

<span data-ttu-id="a1f70-393">Unerwarteter Fehler beim Erstellen einer Sperrdatei.</span><span class="sxs-lookup"><span data-stu-id="a1f70-393">Unexpected error when creating lock file.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="a1f70-394">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a1f70-394">Description</span></span>**  
<span data-ttu-id="a1f70-395">Es tritt ein Fehler auf, wenn MED-V während der Installation keine Datei im @ "%ProgramData%\\Microsoft\\Medv\\MedvLock"-Ordner erstellen kann.</span><span class="sxs-lookup"><span data-stu-id="a1f70-395">An error occurs when MED-V is unable to create a file in the @"%ProgramData%\\Microsoft\\Medv\\MedvLock" folder during installation.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="a1f70-396">Lösung</span><span class="sxs-lookup"><span data-stu-id="a1f70-396">Solution</span></span>**  
<span data-ttu-id="a1f70-397">Überprüfen Sie die Administratorrechte für den MedvLock-Ordner.</span><span class="sxs-lookup"><span data-stu-id="a1f70-397">Check the administrator rights to the MedvLock folder.</span></span>

## <span data-ttu-id="a1f70-398">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="a1f70-398">Related topics</span></span>


[<span data-ttu-id="a1f70-399">Problembehandlung für MED-V</span><span class="sxs-lookup"><span data-stu-id="a1f70-399">Troubleshooting MED-V</span></span>](troubleshooting-med-vmedv2.md)

 

 





