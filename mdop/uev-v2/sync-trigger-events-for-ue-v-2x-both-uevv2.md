---
title: Synchronisieren von Triggerereignissen für UE-V 2.x
description: Synchronisieren von Triggerereignissen für UE-V 2.x
author: dansimp
ms.assetid: 4ed71a13-6a4f-4376-996f-74b126536bbc
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f3e89a0370790e7f462b2f469792128dba033460
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811971"
---
# <span data-ttu-id="776e9-103">Synchronisieren von Triggerereignissen für UE-V 2.x</span><span class="sxs-lookup"><span data-stu-id="776e9-103">Sync Trigger Events for UE-V 2.x</span></span>


<span data-ttu-id="776e9-104">Mit Microsoft User Experience Virtualization (UE-V) 2,0, 2,1 und 2,1 SP1 können Sie Ihre Anwendungs-und Windows-Einstellungen auf allen Ihren Domänen verbundenen Geräten synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="776e9-104">Microsoft User Experience Virtualization (UE-V) 2.0, 2.1, and 2.1 SP1 lets you synchronize your application and Windows settings across all your domain-joined devices.</span></span> <span data-ttu-id="776e9-105">*Synchronisierungstrigger-Ereignisse* definieren, wann der UE-V-Agent diese Einstellungen mit dem Speicherort der Einstellungen synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="776e9-105">*Sync trigger events* define when the UE-V Agent synchronizes those settings with the settings storage location.</span></span> <span data-ttu-id="776e9-106">UE-V 2 führt eine neue *Synchronisierungsmethode* mit dem Namen " *SyncProvider*" ein.</span><span class="sxs-lookup"><span data-stu-id="776e9-106">UE-V 2 introduces a new *Sync Method* called the *SyncProvider*.</span></span> <span data-ttu-id="776e9-107">Weitere Informationen zur Konfiguration der Synchronisierungsmethoden finden Sie unter [Synchronisierungsmethoden für UE-V 2. x](sync-methods-for-ue-v-2x-both-uevv2.md).</span><span class="sxs-lookup"><span data-stu-id="776e9-107">For more information about Sync Method configuration, see [Sync Methods for UE-V 2.x](sync-methods-for-ue-v-2x-both-uevv2.md).</span></span>

## <span data-ttu-id="776e9-108">UE-V 2-Synchronisierungs Trigger-Ereignisse</span><span class="sxs-lookup"><span data-stu-id="776e9-108">UE-V 2 Sync Trigger Events</span></span>


<span data-ttu-id="776e9-109">In der folgenden Tabelle werden die Trigger-Ereignisse für klassische Anwendungen und Windows-Einstellungen erläutert.</span><span class="sxs-lookup"><span data-stu-id="776e9-109">The following table explains the trigger events for classic applications and Windows settings.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="776e9-110">UE-V 2-Trigger-Ereignis</span><span class="sxs-lookup"><span data-stu-id="776e9-110">UE-V 2 Trigger Event</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="776e9-111">SyncMethod = SyncProvider</span><span class="sxs-lookup"><span data-stu-id="776e9-111">SyncMethod=SyncProvider</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="776e9-112">SyncMethod = keine</span><span class="sxs-lookup"><span data-stu-id="776e9-112">SyncMethod=None</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="776e9-113">Windows-Anmeldung</span><span class="sxs-lookup"><span data-stu-id="776e9-113">Windows Logon</span></span></strong></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="776e9-114">Anwendungs-und Windows-Einstellungen werden aus dem Speicherort für Einstellungen in den lokalen Cache importiert.</span><span class="sxs-lookup"><span data-stu-id="776e9-114">Application and Windows settings are imported to the local cache from the settings storage location.</span></span></p></li>
<li><p><a href="https://technet.microsoft.com/library/dn458932.aspx#autosyncsettings2" data-raw-source="[Asynchronous Windows settings](https://technet.microsoft.com/library/dn458932.aspx#autosyncsettings2)"><span data-ttu-id="776e9-115">Asynchrone Windows </a> -Einstellungen werden angewendet.</span><span class="sxs-lookup"><span data-stu-id="776e9-115">Asynchronous Windows settings</a> are applied.</span></span></p></li>
<li><p><span data-ttu-id="776e9-116">Synchrone Windows-Einstellungen werden während der nächsten Windows-Anmeldung übernommen.</span><span class="sxs-lookup"><span data-stu-id="776e9-116">Synchronous Windows settings will be applied during the next Windows logon.</span></span></p></li>
<li><p><span data-ttu-id="776e9-117">Anwendungseinstellungen werden angewendet, wenn die Anwendung gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="776e9-117">Application settings will be applied when the application starts.</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="776e9-118">Anwendungs-und Windows-Einstellungen werden direkt vom Speicherort der Einstellungen gelesen.</span><span class="sxs-lookup"><span data-stu-id="776e9-118">Application and Windows settings are read directly from the settings storage location.</span></span></p></li>
<li><p><span data-ttu-id="776e9-119">Asynchrone und synchrone Windows-Einstellungen werden angewendet.</span><span class="sxs-lookup"><span data-stu-id="776e9-119">Asynchronous and synchronous Windows settings are applied.</span></span></p></li>
<li><p><span data-ttu-id="776e9-120">Anwendungseinstellungen werden angewendet, wenn die Anwendung gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="776e9-120">Application settings will be applied when the application starts.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="776e9-121">Windows-Abmeldung</span><span class="sxs-lookup"><span data-stu-id="776e9-121">Windows Logoff</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="776e9-122">Lokale Änderungen lokal speichern und asynchrone und synchrone Windows-Einstellungen auf den Einstellungen-Speicherort Server kopieren, falls verfügbar</span><span class="sxs-lookup"><span data-stu-id="776e9-122">Store changes locally and cache and copy asynchronous and synchronous Windows settings to the settings storage location server, if available</span></span></p></td>
<td align="left"><p><span data-ttu-id="776e9-123">Speichern von Änderungen an einem asynchronen und synchronen Windows-Einstellungs Speicherort</span><span class="sxs-lookup"><span data-stu-id="776e9-123">Store changes to asynchronous and synchronous Windows settings storage location</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="776e9-124">Windows Connect (RDP)/entsperren</span><span class="sxs-lookup"><span data-stu-id="776e9-124">Windows Connect (RDP) / Unlock</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="776e9-125">Synchronisieren Sie alle asynchronen Windows-Einstellungen vom Speicherort der Einstellungen zum lokalen Cache, sofern verfügbar.</span><span class="sxs-lookup"><span data-stu-id="776e9-125">Synchronize any asynchronous Windows settings from settings storage location to local cache, if available.</span></span></p>
<p><span data-ttu-id="776e9-126">Anwenden von zwischengespeicherten Windows-Einstellungen</span><span class="sxs-lookup"><span data-stu-id="776e9-126">Apply cached Windows settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="776e9-127">Herunterladen und Anwenden von asynchronen Windows-Einstellungen vom Speicherort des Einstellungs Speichers</span><span class="sxs-lookup"><span data-stu-id="776e9-127">Download and apply asynchronous windows settings from settings storage location</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="776e9-128">Windows-Trennung (RDP)/Sperre</span><span class="sxs-lookup"><span data-stu-id="776e9-128">Windows Disconnect (RDP) / Lock</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="776e9-129">Speichern Sie die Änderungen an den asynchronen Windows-Einstellungen im lokalen Cache.</span><span class="sxs-lookup"><span data-stu-id="776e9-129">Store asynchronous Windows settings changes to the local cache.</span></span></p>
<p><span data-ttu-id="776e9-130">Synchronisieren Sie alle asynchronen Windows-Einstellungen aus dem lokalen Cache mit dem Speicherort der Einstellungen, falls verfügbar</span><span class="sxs-lookup"><span data-stu-id="776e9-130">Synchronize any asynchronous Windows settings from the local cache to settings storage location, if available</span></span></p></td>
<td align="left"><p><span data-ttu-id="776e9-131">Speichern von Änderungen an den asynchronen Windows-Einstellungen am Speicherort der Einstellungen</span><span class="sxs-lookup"><span data-stu-id="776e9-131">Store asynchronous Windows settings changes to the settings storage location</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="776e9-132">Anwendungsstart</span><span class="sxs-lookup"><span data-stu-id="776e9-132">Application start</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="776e9-133">Anwenden von Anwendungseinstellungen aus dem lokalen Cache beim Starten der Anwendung</span><span class="sxs-lookup"><span data-stu-id="776e9-133">Apply application settings from local cache as the application starts</span></span></p></td>
<td align="left"><p><span data-ttu-id="776e9-134">Anwenden von Anwendungseinstellungen vom Speicherort der Einstellungen beim Starten der Anwendung</span><span class="sxs-lookup"><span data-stu-id="776e9-134">Apply application settings from settings storage location as the application starts</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="776e9-135">Anwendung wird geschlossen</span><span class="sxs-lookup"><span data-stu-id="776e9-135">Application closes</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="776e9-136">Speichern von Änderungen an den Anwendungseinstellungen im lokalen Cache und Kopieren von Einstellungen in den Speicherort der Einstellungen, sofern verfügbar</span><span class="sxs-lookup"><span data-stu-id="776e9-136">Store any application settings changes to the local cache and copy settings to settings storage location, if available</span></span></p></td>
<td align="left"><p><span data-ttu-id="776e9-137">Speichern der Änderungen an den Einstellungen des Einstellungsspeicher Orts</span><span class="sxs-lookup"><span data-stu-id="776e9-137">Store any application settings changes to settings storage location</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="776e9-138">Der geplante Synchronisierungs Controller-Task oder "Jetzt synchronisieren" wird über das Unternehmenseinstellungen-Center ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="776e9-138">Sync Controller Scheduled Task or “Sync Now” is run from the Company Settings Center</span></span></strong></p>
<p></p></td>
<td align="left"><p><span data-ttu-id="776e9-139">Anwendungs-und Windows-Einstellungen werden zwischen dem Speicherort der Einstellungen und dem lokalen Cache synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="776e9-139">Application and Windows settings are synchronized between the settings storage location and the local cache.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="776e9-140">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="776e9-140">Note</span></span></strong><br/><p><span data-ttu-id="776e9-141">Änderungen an Einstellungen werden erst lokal zwischengespeichert, nachdem eine Anwendung geschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="776e9-141">Settings changes are not cached locally until an application closes.</span></span> <span data-ttu-id="776e9-142">Dieser Trigger exportiert keine Änderungen, die an einer aktuell ausgeführten Anwendung vorgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="776e9-142">This trigger will not export changes made to a currently running application.</span></span></p>
<p><span data-ttu-id="776e9-143">Für Windows-Einstellungen bedeutet dies, dass alle Änderungen nicht lokal zwischengespeichert und bis zur nächsten Sperre (asynchron) oder Abmeldung (asynchron und synchron) exportiert werden.</span><span class="sxs-lookup"><span data-stu-id="776e9-143">For Windows settings, this means that any changes will not be cached locally and exported until the next Lock (Asynchronous) or Logoff (Asynchronous and Synchronous).</span></span></p>
</div>
<div>

</div>
<p><span data-ttu-id="776e9-144">In diesen Fällen werden Einstellungen angewendet:</span><span class="sxs-lookup"><span data-stu-id="776e9-144">Settings are applied in these cases:</span></span></p>
<ul>
<li><p><span data-ttu-id="776e9-145">Asynchrone Windows-Einstellungen werden direkt angewendet.</span><span class="sxs-lookup"><span data-stu-id="776e9-145">Asynchronous Windows settings are applied directly.</span></span></p></li>
<li><p><span data-ttu-id="776e9-146">Anwendungseinstellungen werden angewendet, wenn die Anwendung gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="776e9-146">Application settings are applied when the application starts.</span></span></p></li>
<li><p><span data-ttu-id="776e9-147">Während der nächsten Windows-Anmeldung werden sowohl asynchrone als auch synchrone Windows-Einstellungen angewendet.</span><span class="sxs-lookup"><span data-stu-id="776e9-147">Both asynchronous and synchronous Windows settings are applied during the next Windows logon.</span></span></p></li>
<li><p><span data-ttu-id="776e9-148">Bei der nächsten Aktualisierung werden die Windows-App-Einstellungen (AppX) angewendet.</span><span class="sxs-lookup"><span data-stu-id="776e9-148">Windows app (AppX) settings are applied during the next refresh.</span></span> <span data-ttu-id="776e9-149">Weitere Informationen finden Sie unter <a href="https://technet.microsoft.com/library/dn458944.aspx" data-raw-source="[Monitor Application Settings](https://technet.microsoft.com/library/dn458944.aspx)"> Überwachen von Anwendungseinstellungen </a> .</span><span class="sxs-lookup"><span data-stu-id="776e9-149">See <a href="https://technet.microsoft.com/library/dn458944.aspx" data-raw-source="[Monitor Application Settings](https://technet.microsoft.com/library/dn458944.aspx)">Monitor Application Settings</a> for more information.</span></span></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="776e9-150">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="776e9-150">NA</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="776e9-151">Asynchrone Einstellungen, die im Remotespeicher aktualisiert wurden \*</span><span class="sxs-lookup"><span data-stu-id="776e9-151">Asynchronous Settings updated on remote store\*</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="776e9-152">Laden und Anwenden neuer asynchroner Einstellungen aus dem Cache.</span><span class="sxs-lookup"><span data-stu-id="776e9-152">Load and apply new asynchronous settings from the cache.</span></span></p></td>
<td align="left"><p><span data-ttu-id="776e9-153">Laden und Anwenden von Einstellungen vom zentralen Server</span><span class="sxs-lookup"><span data-stu-id="776e9-153">Load and apply settings from central server</span></span></p></td>
</tr>
</tbody>
</table>








## <span data-ttu-id="776e9-154">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="776e9-154">Related topics</span></span>


[<span data-ttu-id="776e9-155">Technische Referenz für UE-V 2.x</span><span class="sxs-lookup"><span data-stu-id="776e9-155">Technical Reference for UE-V 2.x</span></span>](technical-reference-for-ue-v-2x-both-uevv2.md)

[<span data-ttu-id="776e9-156">Ändern der Häufigkeit von geplanten Aufgaben in UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="776e9-156">Changing the Frequency of UE-V 2.x Scheduled Tasks</span></span>](changing-the-frequency-of-ue-v-2x-scheduled-tasks-both-uevv2.md)

[<span data-ttu-id="776e9-157">Wählen Sie die Konfigurationsmethode für UE-V 2. x aus.</span><span class="sxs-lookup"><span data-stu-id="776e9-157">Choose the Configuration Method for UE-V 2.x</span></span>](https://technet.microsoft.com/library/dn458891.aspx#config)









