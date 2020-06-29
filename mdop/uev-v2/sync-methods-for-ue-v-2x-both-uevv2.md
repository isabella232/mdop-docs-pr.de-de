---
title: Synchronisieren von Methoden für UE-V 2.x
description: Synchronisieren von Methoden für UE-V 2.x
author: dansimp
ms.assetid: af0ae894-dfdc-41d2-927b-c2ab1b355ffe
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a163442e2ab3dbd777aca133b13b0086cdb8ae1a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810039"
---
# <span data-ttu-id="bf93a-103">Synchronisieren von Methoden für UE-V 2.x</span><span class="sxs-lookup"><span data-stu-id="bf93a-103">Sync Methods for UE-V 2.x</span></span>


<span data-ttu-id="bf93a-104">Mit dem Microsoft User Experience Virtualization (UE-V) 2,0, 2,1 und 2,1 SP1-Agent können Sie die Anwendungs-und Windows-Einstellungen der Benutzer mit dem Speicherort der Einstellungen synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="bf93a-104">The Microsoft User Experience Virtualization (UE-V) 2.0, 2.1, and 2.1 SP1 Agent lets you synchronize users’ application and Windows settings with the settings storage location.</span></span> <span data-ttu-id="bf93a-105">Die Konfiguration der *Synchronisierungsmethode* definiert, wie der UE-V-Agent diese Einstellungen in den Speicherort der Einstellungen hochladen und herunterlädt.</span><span class="sxs-lookup"><span data-stu-id="bf93a-105">The *Sync Method* configuration defines how the UE-V Agent uploads and downloads those settings to the settings storage location.</span></span> <span data-ttu-id="bf93a-106">UE-V 2. x führt eine neue SyncMethod namens *SyncProvider*ein.</span><span class="sxs-lookup"><span data-stu-id="bf93a-106">UE-V 2.x introduces a new SyncMethod called the *SyncProvider*.</span></span> <span data-ttu-id="bf93a-107">Weitere Informationen zu Trigger-Ereignissen, mit denen die Synchronisierung von Anwendungs-und Windows-Einstellungen gestartet wird, finden Sie unter [Synchronisieren von Trigger-Ereignissen für UE-V 2. x](sync-trigger-events-for-ue-v-2x-both-uevv2.md).</span><span class="sxs-lookup"><span data-stu-id="bf93a-107">For more information about trigger events that start the synchronization of application and Windows settings, see [Sync Trigger Events for UE-V 2.x](sync-trigger-events-for-ue-v-2x-both-uevv2.md).</span></span>

## <span data-ttu-id="bf93a-108">SyncMethod-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="bf93a-108">SyncMethod Configuration</span></span>


<span data-ttu-id="bf93a-109">In dieser Tabelle werden die Änderungen an SyncMethod von UE-v v 1.0 zu v 2.0 zu v 2.1 sowie die Einstellungen für jede Konfiguration erläutert:</span><span class="sxs-lookup"><span data-stu-id="bf93a-109">This table explains the changes to SyncMethod from UE-V v1.0 to v2.0 to v2.1, as well as the settings for each configuration:</span></span>

<table>
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="bf93a-110">SyncMethod-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="bf93a-110">SyncMethod Configuration</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="bf93a-111">V 1.0</span><span class="sxs-lookup"><span data-stu-id="bf93a-111">V1.0</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="bf93a-112">V 2.0</span><span class="sxs-lookup"><span data-stu-id="bf93a-112">V2.0</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="bf93a-113">V 2.1 und v 2.1 SP1</span><span class="sxs-lookup"><span data-stu-id="bf93a-113">V2.1 and V2.1 SP1</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="bf93a-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bf93a-114">Description</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="bf93a-115">SyncProvider</span><span class="sxs-lookup"><span data-stu-id="bf93a-115">SyncProvider</span></span></p></td>
<td align="left"><p><span data-ttu-id="bf93a-116">n.a.</span><span class="sxs-lookup"><span data-stu-id="bf93a-116">n/a</span></span></p></td>
<td align="left"><p><span data-ttu-id="bf93a-117">Standard</span><span class="sxs-lookup"><span data-stu-id="bf93a-117">Default</span></span></p></td>
<td align="left"><p><span data-ttu-id="bf93a-118">Standard</span><span class="sxs-lookup"><span data-stu-id="bf93a-118">Default</span></span></p></td>
<td align="left"><p><span data-ttu-id="bf93a-119">Änderungen an Einstellungen für eine bestimmte Anwendung oder für globale Windows-Desktopeinstellungen werden lokal in einem Cacheordner gespeichert.</span><span class="sxs-lookup"><span data-stu-id="bf93a-119">Settings changes for a specific application or for global Windows desktop settings are saved locally to a cache folder.</span></span> <span data-ttu-id="bf93a-120">Diese Änderungen werden dann mit dem Speicherort der Einstellungen synchronisiert, wenn ein Synchronisierungstrigger-Ereignis stattfindet.</span><span class="sxs-lookup"><span data-stu-id="bf93a-120">These changes are then synchronized with the settings storage location when a synchronization trigger event takes place.</span></span> <span data-ttu-id="bf93a-121">Durch das Verschieben von Änderungen werden die lokalen Änderungen im Speicherpfad für Einstellungen gespeichert.</span><span class="sxs-lookup"><span data-stu-id="bf93a-121">Pushing out changes will save the local changes to the settings storage path.</span></span></p>
<p><span data-ttu-id="bf93a-122">Diese Standardeinstellung ist der Gold Standard für Computer.</span><span class="sxs-lookup"><span data-stu-id="bf93a-122">This default setting is the gold standard for computers.</span></span> <span data-ttu-id="bf93a-123">Mit dieser Option wird versucht, die Einstellung und die Timeouts nach einer kurzen Verzögerung zu synchronisieren, um sicherzustellen, dass die Anwendung oder der Betriebssystem Start für einen längeren Zeitraum nicht verzögert wird.</span><span class="sxs-lookup"><span data-stu-id="bf93a-123">This option attempts to synchronize the setting and times out after a short delay to ensure that the application or operating system startup isn’t delayed for a long period of time.</span></span></p>
<p><span data-ttu-id="bf93a-124">Diese Funktionalität ist auch an die geplante Aufgabe – Synchronisierungs-Controller-Anwendung gebunden.</span><span class="sxs-lookup"><span data-stu-id="bf93a-124">This functionality is also tied to the Scheduled task – Sync Controller Application.</span></span> <span data-ttu-id="bf93a-125">Der Administrator steuert die Häufigkeit des geplanten Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="bf93a-125">The administrator controls the frequency of the Scheduled task.</span></span> <span data-ttu-id="bf93a-126">Standardmäßig werden die Einstellungen von Computern alle 30 Minuten nach der Anmeldung synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="bf93a-126">By default, computers synchronize their settings every 30 min after logging on.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bf93a-127">Offlinedateien</span><span class="sxs-lookup"><span data-stu-id="bf93a-127">OfflineFiles</span></span></p></td>
<td align="left"><p><span data-ttu-id="bf93a-128">Standard</span><span class="sxs-lookup"><span data-stu-id="bf93a-128">Default</span></span></p></td>
<td align="left"><p><span data-ttu-id="bf93a-129">Veraltet</span><span class="sxs-lookup"><span data-stu-id="bf93a-129">Deprecated</span></span></p></td>
<td align="left"><p><span data-ttu-id="bf93a-130">Veraltet</span><span class="sxs-lookup"><span data-stu-id="bf93a-130">Deprecated</span></span></p></td>
<td align="left"><p><span data-ttu-id="bf93a-131">Verhält sich wie SyncProvider in v 2.0.</span><span class="sxs-lookup"><span data-stu-id="bf93a-131">Behaves the same as SyncProvider in V2.0.</span></span></p>
<p><span data-ttu-id="bf93a-132">Wenn Offline Dateien aktiviert sind und der Ordner angeheftet ist, wird UE-V diesen Ordner unpin und direkt mit dem zentralen SMB-Verzeichnis synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="bf93a-132">If Offline files are enabled and the folder is pinned then UE-V will unpin this folder and sync directly to the central SMB directory.</span></span></p>
<p><strong><span data-ttu-id="bf93a-133">Hinweis: </strong> in V 1.0, wenn Sie UE-V auf eine Corpnet getrennte Weise verwenden möchten (auch wenn Sie mit einem Laptop unterwegs sind), sollten Sie Offline Dateien verwenden, um sicherzustellen, dass Ihre Einstellungen durchstreift werden.</span><span class="sxs-lookup"><span data-stu-id="bf93a-133">NOTE:</strong> In V1.0 if you wanted to use UE-V in a CorpNet disconnected manner (aka traveling with a Laptop), then the guidance is to use Offline Files to ensure that your settings roamed.</span></span><span data-ttu-id="bf93a-134">Wir haben genügend Kundenfeedback erhalten, dass das Aktivieren von Offline Dateien ein nicht trivialer Enterprise-Blocker ist.</span><span class="sxs-lookup"><span data-stu-id="bf93a-134"> We received sufficient customer feedback that turning on Offline files is a non-trivial enterprise blocker.</span></span> <span data-ttu-id="bf93a-135">In UE-V 2 haben wir also ein eng gekoppeltes Synchronisierungsmodul erstellt, um Ihre Daten lokal zwischenzuspeichern und die Einstellungen mit dem zentralen Server zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="bf93a-135">So in UE-V 2, we created a tightly coupled synchronization engine to cache your data locally and synchronize the settings to the central server.</span></span> <span data-ttu-id="bf93a-136">Dieser Funktionsbereich ersetzt nicht die Offline Dateien oder die Ordnerumleitung.</span><span class="sxs-lookup"><span data-stu-id="bf93a-136">This feature area does not replace Offline Files or Folder Redirection.</span></span></p>
<p><span data-ttu-id="bf93a-137">UE-V 2 funktioniert nicht gut mit Offline Ordnern, daher ist es nicht so, den Speicherpfad für Einstellungen auf einen angehefteten offline-oder CSC-Ordner festzulegen.</span><span class="sxs-lookup"><span data-stu-id="bf93a-137">UE-V 2 does not work well with Offline folders so the guidance is not to set the settings storage path to a pinned Offline or CSC folder.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="bf93a-138">Extern</span><span class="sxs-lookup"><span data-stu-id="bf93a-138">External</span></span></p></td>
<td align="left"><p><span data-ttu-id="bf93a-139">n.a.</span><span class="sxs-lookup"><span data-stu-id="bf93a-139">n/a</span></span></p></td>
<td align="left"><p><span data-ttu-id="bf93a-140">n.a.</span><span class="sxs-lookup"><span data-stu-id="bf93a-140">n/a</span></span></p></td>
<td align="left"><p><span data-ttu-id="bf93a-141">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="bf93a-141">Supported</span></span></p></td>
<td align="left"><p><span data-ttu-id="bf93a-142">Neu in UE-v 2,1 gibt diese Konfigurationsmethode an, dass, wenn UE-v-Einstellungen in einen lokalen Ordner auf dem Benutzer Computer geschrieben werden, ein externes Synchronisierungsmodul (wie OneDrive for Business, Arbeitsordner, SharePoint oder Dropbox) verwendet werden kann, um diese Einstellungen auf die verschiedenen Computer anzuwenden, auf die Benutzer zugreifen.</span><span class="sxs-lookup"><span data-stu-id="bf93a-142">New in UE-V 2.1, this configuration method specifies that if UE-V settings are written to a local folder on the user computer, then any external sync engine (such as OneDrive for Business, Work Folders, Sharepoint, or Dropbox) can be used to apply these settings to the different computers that users access.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bf93a-143">Keine</span><span class="sxs-lookup"><span data-stu-id="bf93a-143">None</span></span></p></td>
<td align="left"><p><span data-ttu-id="bf93a-144">Ja</span><span class="sxs-lookup"><span data-stu-id="bf93a-144">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="bf93a-145">Ja</span><span class="sxs-lookup"><span data-stu-id="bf93a-145">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="bf93a-146">Ja</span><span class="sxs-lookup"><span data-stu-id="bf93a-146">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="bf93a-147">Diese Konfigurationseinstellung ist für die Virtual Desktop Infrastructure (VDI) und die Übertragung von Anwendungserfahrung in erster Linie vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="bf93a-147">This configuration setting is designed for the Virtual Desktop Infrastructure (VDI) and Streamed Application experience primarily.</span></span> <span data-ttu-id="bf93a-148">Diese Einstellung sollte in Windows Server-Feldern verwendet werden, die in einem Rechenzentrum verwendet werden, wobei die Verbindung immer verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="bf93a-148">This setting should be used on Windows Server boxes used in a datacenter, where the connection will always be available.</span></span></p>
<p><span data-ttu-id="bf93a-149">Alle Einstellungsänderungen werden direkt auf dem Server gespeichert.</span><span class="sxs-lookup"><span data-stu-id="bf93a-149">Any settings changes are saved directly to the server.</span></span> <span data-ttu-id="bf93a-150">Wenn die Netzwerkverbindung mit dem Einstellungsspeicher Pfad nicht verfügbar ist, werden die Einstellungen Änderungen auf dem Gerät zwischengespeichert und beim nächsten Ausführen des Synchronisierungsanbieters synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="bf93a-150">If the network connection to the settings storage path is not available, then the settings changes are cached on the device and are synchronized the next time that the Sync Provider runs.</span></span> <span data-ttu-id="bf93a-151">Wenn der Speicherpfad für Einstellungen nicht gefunden wird und das Benutzerprofil bei der Abmeldung aus einer gepoolten VDI-Umgebung entfernt wird, gehen diese Einstellungsänderungen verloren, und der Benutzer muss die Änderung erneut anwenden, wenn der Computer erneut den Speicherpfad für Einstellungen erreichen kann.</span><span class="sxs-lookup"><span data-stu-id="bf93a-151">If the settings storage path is not found and the user profile is removed from a pooled VDI environment on logoff, then these settings changes are lost, and the user must reapply the change when the computer can again reach the settings storage path.</span></span></p>
<p><span data-ttu-id="bf93a-152">Apps und Betriebssystem warten auf unbestimmte Zeit, bis der Standort vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="bf93a-152">Apps and OS will wait indefinitely for the location to be present.</span></span> <span data-ttu-id="bf93a-153">Dies kann dazu führen, dass die APP-Lade-oder Betriebssystem-Anmeldezeit drastisch zunimmt, wenn der Standort nicht gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="bf93a-153">This could cause App load or OS logon time to dramatically increase if the location is not found.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="bf93a-154">Sie können die Synchronisierungsmethode wie folgt konfigurieren:</span><span class="sxs-lookup"><span data-stu-id="bf93a-154">You can configure the sync method in these ways:</span></span>

-   <span data-ttu-id="bf93a-155">Wenn Sie [den UE-V-Agent](https://technet.microsoft.com/library/dn458891.aspx#agent) über einen Befehlszeilenparameter oder in einem Batchskript bereitstellen</span><span class="sxs-lookup"><span data-stu-id="bf93a-155">When you [Deploy the UE-V Agent](https://technet.microsoft.com/library/dn458891.aspx#agent) through a command-line parameter or in a batch script</span></span>

-   <span data-ttu-id="bf93a-156">Über [Gruppenrichtlinien](https://technet.microsoft.com/library/dn458893.aspx) Einstellungen</span><span class="sxs-lookup"><span data-stu-id="bf93a-156">Through [Group Policy](https://technet.microsoft.com/library/dn458893.aspx) settings</span></span>

-   <span data-ttu-id="bf93a-157">Mit dem [System Center-Konfigurationspaket](https://technet.microsoft.com/library/dn458917.aspx) für UE-V</span><span class="sxs-lookup"><span data-stu-id="bf93a-157">With the [System Center Configuration Pack](https://technet.microsoft.com/library/dn458917.aspx) for UE-V</span></span>

-   <span data-ttu-id="bf93a-158">Nach der Installation des UE-V-Agents mithilfe von [Windows PowerShell oder Windows-Verwaltungsinstrumentation (WMI)](https://technet.microsoft.com/library/dn458937.aspx)</span><span class="sxs-lookup"><span data-stu-id="bf93a-158">After installation of the UE-V Agent, by using [Windows PowerShell or Windows Management Instrumentation (WMI)](https://technet.microsoft.com/library/dn458937.aspx)</span></span>






## <span data-ttu-id="bf93a-159">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="bf93a-159">Related topics</span></span>


[<span data-ttu-id="bf93a-160">Bereitstellen der erforderlichen Features für UE-V 2.x</span><span class="sxs-lookup"><span data-stu-id="bf93a-160">Deploy Required Features for UE-V 2.x</span></span>](deploy-required-features-for-ue-v-2x-new-uevv2.md#ssl)

[<span data-ttu-id="bf93a-161">Bereitstellen der erforderlichen Features für UE-V 2.x</span><span class="sxs-lookup"><span data-stu-id="bf93a-161">Deploy Required Features for UE-V 2.x</span></span>](deploy-required-features-for-ue-v-2x-new-uevv2.md#config)

[<span data-ttu-id="bf93a-162">Technische Referenz für UE-V 2.x</span><span class="sxs-lookup"><span data-stu-id="bf93a-162">Technical Reference for UE-V 2.x</span></span>](technical-reference-for-ue-v-2x-both-uevv2.md)

 

 





