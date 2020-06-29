---
title: Ändern der Häufigkeit von geplanten Aufgaben in UE-V 2. x
description: Ändern der Häufigkeit von geplanten Aufgaben in UE-V 2. x
author: dansimp
ms.assetid: ee486570-c6cf-4fd9-ba48-0059ba877c10
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 09/29/2016
ms.openlocfilehash: 1c1e3c091431dc56068dcd1fe0e849b0df1f6aa0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810549"
---
# <span data-ttu-id="3e858-103">Ändern der Häufigkeit von geplanten Aufgaben in UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="3e858-103">Changing the Frequency of UE-V 2.x Scheduled Tasks</span></span>


<span data-ttu-id="3e858-104">Das Microsoft User Experience Virtualization (UE-v) 2,0, 2,1 oder 2,1 SP1-Agent-Installationsprogramm, AgentSetup.exe, erstellt die folgenden geplanten Aufgaben während der Installation des UE-v-Agents:</span><span class="sxs-lookup"><span data-stu-id="3e858-104">The Microsoft User Experience Virtualization (UE-V) 2.0, 2.1, or 2.1 SP1 Agent installer, AgentSetup.exe, creates the following scheduled tasks during the UE-V Agent installation:</span></span>

-   **<span data-ttu-id="3e858-105">Überwachen von Anwendungseinstellungen</span><span class="sxs-lookup"><span data-stu-id="3e858-105">Monitor Application Settings</span></span>**

-   **<span data-ttu-id="3e858-106">Synchronisierungs-Controller-Anwendung</span><span class="sxs-lookup"><span data-stu-id="3e858-106">Sync Controller Application</span></span>**

-   **<span data-ttu-id="3e858-107">Synchronisieren von Einstellungen beim Abmelden</span><span class="sxs-lookup"><span data-stu-id="3e858-107">Synchronize Settings at Logoff</span></span>**

-   **<span data-ttu-id="3e858-108">Automatische Aktualisierung der Vorlage</span><span class="sxs-lookup"><span data-stu-id="3e858-108">Template Auto Update</span></span>**

-   **<span data-ttu-id="3e858-109">Sammeln von CEIP-Daten</span><span class="sxs-lookup"><span data-stu-id="3e858-109">Collect CEIP data</span></span>**

-   **<span data-ttu-id="3e858-110">Hochladen von CEIP-Daten</span><span class="sxs-lookup"><span data-stu-id="3e858-110">Upload CEIP Data</span></span>**

<span data-ttu-id="3e858-111">**Hinweis**  Mit Ausnahme von CEIP-Daten sammeln müssen diese Aufgaben aktiviert bleiben, da UE-V nicht ohne Sie funktionieren kann.</span><span class="sxs-lookup"><span data-stu-id="3e858-111">**Note** With the exception of Collect CEIP Data, these tasks must remain enabled as UE-V cannot function without them.</span></span>

 

<span data-ttu-id="3e858-112">Diese geplanten Aufgaben können mit den UE-V-Tools nicht konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="3e858-112">These scheduled tasks are not configurable with the UE-V tools.</span></span> <span data-ttu-id="3e858-113">Administratoren, die die geplante Aufgabe für diese Elemente ändern möchten, können ein Skript erstellen, das die Schtasks.exe Befehlszeilenoptionen verwendet.</span><span class="sxs-lookup"><span data-stu-id="3e858-113">Administrators who want to change the scheduled task for these items can create a script that uses the Schtasks.exe command-line options.</span></span>

<span data-ttu-id="3e858-114">Weitere Informationen zu Schtasks.exe finden Sie unter [so wird es gemacht: Verwenden von schtasks, exe zum Planen von Aufgaben in Windows Server 2003](https://go.microsoft.com/fwlink/?LinkID=264854).</span><span class="sxs-lookup"><span data-stu-id="3e858-114">For more information about Schtasks.exe, see [How to use Schtasks,exe to Schedule Tasks in Windows Server 2003](https://go.microsoft.com/fwlink/?LinkID=264854).</span></span>

<span data-ttu-id="3e858-115">Weitere Informationen zu</span><span class="sxs-lookup"><span data-stu-id="3e858-115">For more information about</span></span>

## <span data-ttu-id="3e858-116">Geplante Aufgaben in UE-V</span><span class="sxs-lookup"><span data-stu-id="3e858-116">UE-V Scheduled Tasks</span></span>


<span data-ttu-id="3e858-117">Die folgenden geplanten Aufgaben sind in UE-V 2 mit Konfigurationsbefehlen für geplante Aufgaben enthalten.</span><span class="sxs-lookup"><span data-stu-id="3e858-117">The following scheduled tasks are included in UE-V 2 with sample scheduled task configuration commands.</span></span>

### <span data-ttu-id="3e858-118">Sammeln von CEIP-Daten</span><span class="sxs-lookup"><span data-stu-id="3e858-118">Collect CEIP Data</span></span>

<span data-ttu-id="3e858-119">Wenn sich der Benutzer oder Administrator bei der Installation für die Teilnahme am Programm zur Verbesserung der Benutzerfreundlichkeit (CEIP) entschieden hat, sammelt UE-V Daten, um das Produkt in zukünftigen Versionen zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="3e858-119">If upon installation the user or administrator choses to participate in the Customer Experience Improvement Program (CEIP), UE-V collects data to help improve the product in future releases.</span></span> <span data-ttu-id="3e858-120">Dieser geplante Task wird nur bei der Anmeldung ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3e858-120">This scheduled task only runs at logon.</span></span> <span data-ttu-id="3e858-121">Der Task " **CEIP-Daten sammeln** " führt die UevSqmSession.exe aus, die sich im Installationsverzeichnis des UE-V-Agents befindet.</span><span class="sxs-lookup"><span data-stu-id="3e858-121">The **Collect CEIP Data** task runs the UevSqmSession.exe, which is located in the UE-V Agent installation directory.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="3e858-122">Aufgabenname</span><span class="sxs-lookup"><span data-stu-id="3e858-122">Task name</span></span></th>
<th align="left"><span data-ttu-id="3e858-123">Standardereignis</span><span class="sxs-lookup"><span data-stu-id="3e858-123">Default event</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3e858-124">\Microsoft\UE-V\Collect-CEIP-Daten</span><span class="sxs-lookup"><span data-stu-id="3e858-124">\Microsoft\UE-V\Collect CEIP data</span></span></p></td>
<td align="left"><p><span data-ttu-id="3e858-125">Anmelde</span><span class="sxs-lookup"><span data-stu-id="3e858-125">Logon</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="3e858-126">Überwachen von Anwendungseinstellungen</span><span class="sxs-lookup"><span data-stu-id="3e858-126">Monitor Application Settings</span></span>

<span data-ttu-id="3e858-127">Mit der Aufgabe " **Monitor-Anwendungseinstellungen** " werden die Einstellungen für Windows-apps synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="3e858-127">The **Monitor Application Settings** task is used to synchronize settings for Windows apps.</span></span> <span data-ttu-id="3e858-128">Sie wird bei der Anmeldung ausgeführt, wird aber um 30 Sekunden verzögert, um die Anmeldung nicht schädlich zu beeinflussen.</span><span class="sxs-lookup"><span data-stu-id="3e858-128">It is run at logon but is delayed by 30 seconds to not affect the logon detrimentally.</span></span> <span data-ttu-id="3e858-129">Die Aufgabe "Monitor Application Status" führt die UevAppMonitor.exe-Datei aus, die sich im Installationsverzeichnis des UE-V-Agents befindet.</span><span class="sxs-lookup"><span data-stu-id="3e858-129">The Monitor Application Status task runs the UevAppMonitor.exe file, which is located in the UE-V Agent installation directory.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="3e858-130">Aufgabenname</span><span class="sxs-lookup"><span data-stu-id="3e858-130">Task name</span></span></th>
<th align="left"><span data-ttu-id="3e858-131">Standardereignis</span><span class="sxs-lookup"><span data-stu-id="3e858-131">Default event</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3e858-132">\Microsoft\UE-V\Monitor-Anwendungs Status</span><span class="sxs-lookup"><span data-stu-id="3e858-132">\Microsoft\UE-V\Monitor Application Status</span></span></p></td>
<td align="left"><p><span data-ttu-id="3e858-133">Anmelde</span><span class="sxs-lookup"><span data-stu-id="3e858-133">Logon</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="3e858-134">Synchronisierungs-Controller-Anwendung</span><span class="sxs-lookup"><span data-stu-id="3e858-134">Sync Controller Application</span></span>

<span data-ttu-id="3e858-135">Der Synchronisierungs **Controller-Anwendungs** Task wird verwendet, um den Synchronisierungs Controller zu starten, um die Einstellungen vom Computer zum Speicherort der Einstellungen zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="3e858-135">The **Sync Controller Application** task is used to start the Sync Controller to synchronize settings from the computer to the settings storage location.</span></span> <span data-ttu-id="3e858-136">Standardmäßig wird die Aufgabe alle 30 Minuten ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3e858-136">By default, the task runs every 30 minutes.</span></span> <span data-ttu-id="3e858-137">Zu diesem Zeitpunkt werden lokale Einstellungen mit dem Speicherort der Einstellungen synchronisiert, und die aktualisierten Einstellungen für den Speicherort der Einstellungen werden mit dem Computer synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="3e858-137">At that time, local settings are synchronized to the settings storage location, and updated settings on the settings storage location are synchronized to the computer.</span></span> <span data-ttu-id="3e858-138">Die Synchronisierungs Controller Anwendung führt die Microsoft.Uev.SyncController.exe aus, die sich im Installationsverzeichnis des UE-V-Agents befindet.</span><span class="sxs-lookup"><span data-stu-id="3e858-138">The Sync Controller application runs the Microsoft.Uev.SyncController.exe, which is located in the UE-V Agent installation directory.</span></span>
<span data-ttu-id="3e858-139">**Hinweis:** Gemäß der Aufgabe " **Anwendungseinstellungen überwachen** " wird diese Aufgabe bei der Anmeldung ausgeführt, Sie wird jedoch um 30 Sekunden verzögert, um die Anmeldung nicht schädlich zu beeinflussen.</span><span class="sxs-lookup"><span data-stu-id="3e858-139">**Note:** As per the **Monitor Application Settings** task, this task is run at logon but is delayed by 30 seconds to not affect the logon detrimentally.</span></span>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="3e858-140">Aufgabenname</span><span class="sxs-lookup"><span data-stu-id="3e858-140">Task name</span></span></th>
<th align="left"><span data-ttu-id="3e858-141">Standardereignis</span><span class="sxs-lookup"><span data-stu-id="3e858-141">Default event</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3e858-142">\Microsoft\UE-V\Sync-Controller Anwendung</span><span class="sxs-lookup"><span data-stu-id="3e858-142">\Microsoft\UE-V\Sync Controller Application</span></span></p></td>
<td align="left"><p><span data-ttu-id="3e858-143">Anmeldung und anschließend alle 30 Minuten</span><span class="sxs-lookup"><span data-stu-id="3e858-143">Logon, and every 30 minutes thereafter</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="3e858-144">Mit dem folgenden Befehl wird beispielsweise der Agent so konfiguriert, dass die Einstellungen alle 15 Minuten anstelle des standardmäßigen 30-minütigen synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="3e858-144">For example, the following command configures the agent to synchronize settings every 15 minutes instead of the default 30 minutes.</span></span>

``` syntax
Schtasks /change /tn “Microsoft\UE-V\Sync Controller Application” /ri 15
```

### <span data-ttu-id="3e858-145">Synchronisieren von Einstellungen beim Abmelden</span><span class="sxs-lookup"><span data-stu-id="3e858-145">Synchronize Settings at Logoff</span></span>

<span data-ttu-id="3e858-146">Mit der Aufgabe **Synchronisierungseinstellungen beim Abmelden** wird eine Anwendung bei der Anmeldung gestartet, die die Synchronisierung von Anwendungen bei der Abmeldung für UE-V steuert.</span><span class="sxs-lookup"><span data-stu-id="3e858-146">The **Synchronize Settings at Logoff** task is used to start an application at logon that controls the synchronization of applications at logoff for UE-V.</span></span> <span data-ttu-id="3e858-147">Der Task "Einstellungen beim Abmelden synchronisieren" führt die Microsoft.Uev.SyncController.exe-Datei aus, die sich im Installationsverzeichnis des UE-V-Agents befindet.</span><span class="sxs-lookup"><span data-stu-id="3e858-147">The Synchronize Settings at Logoff task runs the Microsoft.Uev.SyncController.exe file, which is located in the UE-V Agent installation directory.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="3e858-148">Aufgabenname</span><span class="sxs-lookup"><span data-stu-id="3e858-148">Task name</span></span></th>
<th align="left"><span data-ttu-id="3e858-149">Standardereignis</span><span class="sxs-lookup"><span data-stu-id="3e858-149">Default event</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3e858-150">\Microsoft\UE-V\Synchronize-Einstellungen beim Abmelden</span><span class="sxs-lookup"><span data-stu-id="3e858-150">\Microsoft\UE-V\Synchronize Settings at Logoff</span></span></p></td>
<td align="left"><p><span data-ttu-id="3e858-151">Anmelde</span><span class="sxs-lookup"><span data-stu-id="3e858-151">Logon</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="3e858-152">Automatische Aktualisierung der Vorlage</span><span class="sxs-lookup"><span data-stu-id="3e858-152">Template Auto Update</span></span>

<span data-ttu-id="3e858-153">Mit dem **automatischen Aktualisierungs** Vorgang der Vorlage wird der Einstellungs Vorlagenkatalog auf neue, aktualisierte oder entfernte Vorlagen überprüft.</span><span class="sxs-lookup"><span data-stu-id="3e858-153">The **Template Auto Update** task checks the settings template catalog for new, updated, or removed templates.</span></span> <span data-ttu-id="3e858-154">Diese Aufgabe wird nur ausgeführt, wenn die SettingsTemplateCatalog konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="3e858-154">This task only runs if the SettingsTemplateCatalog is configured.</span></span> <span data-ttu-id="3e858-155">Der Task " **Automatische Aktualisierung der Vorlage** " führt die ApplySettingsCatalog.exe-Datei aus, die sich im Installationsverzeichnis des UE-V-Agents befindet.</span><span class="sxs-lookup"><span data-stu-id="3e858-155">The **Template Auto Update** task runs the ApplySettingsCatalog.exe file, which is located in the UE-V Agent installation directory.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="3e858-156">Aufgabenname</span><span class="sxs-lookup"><span data-stu-id="3e858-156">Task name</span></span></th>
<th align="left"><span data-ttu-id="3e858-157">Standardereignis</span><span class="sxs-lookup"><span data-stu-id="3e858-157">Default event</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3e858-158">\Microsoft\UE-V\Template Auto Update</span><span class="sxs-lookup"><span data-stu-id="3e858-158">\Microsoft\UE-V\Template Auto Update</span></span></p></td>
<td align="left"><p><span data-ttu-id="3e858-159">System Start und um 3:30 Uhr täglich, zu einem beliebigen Zeitpunkt innerhalb eines 1-Stunden-Fensters</span><span class="sxs-lookup"><span data-stu-id="3e858-159">System startup and at 3:30 AM every day, at a random time within a 1-hour window</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="3e858-160">**Beispiel:** Mit dem folgenden Befehl wird der UE-V-Agent so konfiguriert, dass der Katalog Speicher für Einstellungs Vorlagen stündlich überprüft wird.</span><span class="sxs-lookup"><span data-stu-id="3e858-160">**Example:** The following command configures the UE-V Agent to check the settings template catalog store every hour.</span></span>

``` syntax
schtasks /change /tn "Microsoft\UE-V\Template Auto Update" /ri 60
```

### <span data-ttu-id="3e858-161">Hochladen von CEIP-Daten</span><span class="sxs-lookup"><span data-stu-id="3e858-161">Upload CEIP Data</span></span>

<span data-ttu-id="3e858-162">Der Task " **CEIP-Daten hochladen** " wird während der Installation ausgeführt, wenn der Benutzer oder der Administrator sich für die Teilnahme am Programm zur Verbesserung der Benutzerfreundlichkeit (CEIP) entschieden hat.</span><span class="sxs-lookup"><span data-stu-id="3e858-162">The **Upload CEIP Data** task runs during the installation if the user or the administrator chose to participate in the Customer Experience Improvement Program (CEIP).</span></span> <span data-ttu-id="3e858-163">Mit dieser Aufgabe werden die Daten auf die CEIP-Server hochgeladen, auf denen die Daten zur Verbesserung des Produkts für zukünftige Versionen von UE-V verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3e858-163">This task uploads the data to the CEIP servers where the data is used to help improve the product for future releases of UE-V.</span></span> <span data-ttu-id="3e858-164">Diese geplante Aufgabe wird bei der Anmeldung und anschließend alle 4 Stunden ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3e858-164">This scheduled task runs at logon and every 4 hours afterwards.</span></span> <span data-ttu-id="3e858-165">Der Task " **CEIP-Daten hochladen** " führt die UevSqmUploader.exe-Datei aus, die sich im Installationsverzeichnis des UE-V-Agents befindet.</span><span class="sxs-lookup"><span data-stu-id="3e858-165">The **Upload CEIP data** task runs the UevSqmUploader.exe file, which is located in the UE-V Agent installation directory.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="3e858-166">Aufgabenname</span><span class="sxs-lookup"><span data-stu-id="3e858-166">Task name</span></span></th>
<th align="left"><span data-ttu-id="3e858-167">Standardereignis</span><span class="sxs-lookup"><span data-stu-id="3e858-167">Default event</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3e858-168">\Microsoft\UE-V\Upload-CEIP-Daten</span><span class="sxs-lookup"><span data-stu-id="3e858-168">\Microsoft\UE-V\Upload CEIP data</span></span></p></td>
<td align="left"><p><span data-ttu-id="3e858-169">Bei der Anmeldung und alle 4 Stunden</span><span class="sxs-lookup"><span data-stu-id="3e858-169">At logon and every 4 hours</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="3e858-170">Informationen zu geplanten Aufgaben in UE-V 2</span><span class="sxs-lookup"><span data-stu-id="3e858-170">UE-V 2 Scheduled Task Details</span></span>


<span data-ttu-id="3e858-171">Das folgende Diagramm enthält zusätzliche Informationen zu geplanten Aufgaben für UE-V 2:</span><span class="sxs-lookup"><span data-stu-id="3e858-171">The following chart provides additional information about scheduled tasks for UE-V 2:</span></span>

<table style="width:100%;">
<colgroup>
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="3e858-172">Vorgangsname </strong> (Dateiname)</span><span class="sxs-lookup"><span data-stu-id="3e858-172">Task Name</strong> (file name)</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="3e858-173">Standardhäufigkeit</span><span class="sxs-lookup"><span data-stu-id="3e858-173">Default Frequency</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="3e858-174">Power-Umschaltfläche</span><span class="sxs-lookup"><span data-stu-id="3e858-174">Power Toggle</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="3e858-175">Nur im Leerlauf</span><span class="sxs-lookup"><span data-stu-id="3e858-175">Idle Only</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="3e858-176">Netzwerkverbindung</span><span class="sxs-lookup"><span data-stu-id="3e858-176">Network Connection</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="3e858-177">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3e858-177">Description</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="3e858-178">Überwachen von Anwendungseinstellungen </strong> (UevAppMonitor.exe)</span><span class="sxs-lookup"><span data-stu-id="3e858-178">Monitor Application Settings</strong> (UevAppMonitor.exe)</span></span></p></td>
<td align="left"><p><span data-ttu-id="3e858-179">Startet 30 Sekunden nach der Anmeldung und wird bis zur Abmeldung fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="3e858-179">Starts 30 seconds after logon and continues until logoff.</span></span></p></td>
<td align="left"><p><span data-ttu-id="3e858-180">Nein.</span><span class="sxs-lookup"><span data-stu-id="3e858-180">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="3e858-181">Ja</span><span class="sxs-lookup"><span data-stu-id="3e858-181">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="3e858-182">–</span><span class="sxs-lookup"><span data-stu-id="3e858-182">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="3e858-183">Synchronisiert Einstellungen für Windows-Apps (AppX).</span><span class="sxs-lookup"><span data-stu-id="3e858-183">Synchronizes settings for Windows (AppX) apps.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="3e858-184">Synchronisierungs Controller Anwendung </strong> (Microsoft.Uev.SyncController.exe)</span><span class="sxs-lookup"><span data-stu-id="3e858-184">Sync Controller Application</strong> (Microsoft.Uev.SyncController.exe)</span></span></p></td>
<td align="left"><p><span data-ttu-id="3e858-185">Bei der Anmeldung und danach alle 30 Minuten.</span><span class="sxs-lookup"><span data-stu-id="3e858-185">At logon and every 30 min thereafter.</span></span></p></td>
<td align="left"><p><span data-ttu-id="3e858-186">Ja</span><span class="sxs-lookup"><span data-stu-id="3e858-186">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="3e858-187">Ja</span><span class="sxs-lookup"><span data-stu-id="3e858-187">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="3e858-188">Nur, wenn das Netzwerk verbunden ist</span><span class="sxs-lookup"><span data-stu-id="3e858-188">Only if Network is connected</span></span></p></td>
<td align="left"><p><span data-ttu-id="3e858-189">Startet den Synchronisierungs Controller, der lokale Einstellungen mit dem Speicherort für Einstellungen synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="3e858-189">Starts the Sync Controller which synchronizes local settings with the settings storage location.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="3e858-190">Synchronisieren von Einstellungen beim Abmelden </strong> (Microsoft.Uev.SyncController.exe)</span><span class="sxs-lookup"><span data-stu-id="3e858-190">Synchronize Settings at Logoff</strong> (Microsoft.Uev.SyncController.exe)</span></span></p></td>
<td align="left"><p><span data-ttu-id="3e858-191">Wird bei der Anmeldung ausgeführt und wartet auf Abmelden, um die Einstellungen zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="3e858-191">Runs at logon and then waits for Logoff to Synchronize settings.</span></span></p></td>
<td align="left"><p><span data-ttu-id="3e858-192">Nein.</span><span class="sxs-lookup"><span data-stu-id="3e858-192">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="3e858-193">Ja</span><span class="sxs-lookup"><span data-stu-id="3e858-193">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="3e858-194">–</span><span class="sxs-lookup"><span data-stu-id="3e858-194">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="3e858-195">Starten Sie bei der Anmeldung eine Anwendung, die die Synchronisierung von Anwendungen bei der Abmeldung steuert.</span><span class="sxs-lookup"><span data-stu-id="3e858-195">Start an application at logon that controls the synchronization of applications at logoff.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="3e858-196">Automatische Aktualisierung der Vorlage </strong> (ApplySettingsCatalog.exe)</span><span class="sxs-lookup"><span data-stu-id="3e858-196">Template Auto Update</strong> (ApplySettingsCatalog.exe)</span></span></p></td>
<td align="left"><p><span data-ttu-id="3e858-197">Wird bei der Erstanmeldung und bei 3:30 am Tag danach ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3e858-197">Runs at initial logon and at 3:30 AM every day thereafter.</span></span></p></td>
<td align="left"><p><span data-ttu-id="3e858-198">Ja</span><span class="sxs-lookup"><span data-stu-id="3e858-198">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="3e858-199">Nein</span><span class="sxs-lookup"><span data-stu-id="3e858-199">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="3e858-200">n.a.</span><span class="sxs-lookup"><span data-stu-id="3e858-200">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="3e858-201">Überprüft den Vorlagenkatalog der Einstellungen auf neue, aktualisierte oder entfernte Vorlagen.</span><span class="sxs-lookup"><span data-stu-id="3e858-201">Checks the settings template catalog for new, updated, or removed templates.</span></span> <span data-ttu-id="3e858-202">Diese Aufgabe wird nur ausgeführt, wenn SettingsTemplateCatalog konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="3e858-202">This task only runs if SettingsTemplateCatalog is configured.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="3e858-203">Sammeln von CEIP </strong> -Daten (UevSqmSession.exe)</span><span class="sxs-lookup"><span data-stu-id="3e858-203">Collect CEIP data</strong> (UevSqmSession.exe)</span></span></p></td>
<td align="left"><p><span data-ttu-id="3e858-204">Bei der Anmeldung wird der Dienst gestartet.</span><span class="sxs-lookup"><span data-stu-id="3e858-204">At logon launches service</span></span></p></td>
<td align="left"><p><span data-ttu-id="3e858-205">Nein</span><span class="sxs-lookup"><span data-stu-id="3e858-205">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="3e858-206">Ja</span><span class="sxs-lookup"><span data-stu-id="3e858-206">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="3e858-207">n.a.</span><span class="sxs-lookup"><span data-stu-id="3e858-207">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="3e858-208">Wenn sich der Benutzer oder Administrator für das Programm zur Verbesserung der Benutzerfreundlichkeit einsetzt, sammelt diese Aufgabe Daten, die zur Verbesserung der zukünftigen Versionen von UE-V beitragen.</span><span class="sxs-lookup"><span data-stu-id="3e858-208">If the user or administrator opts in to the Customer Experience Improvement Program (CEIP), this task collects data that helps improve UE-V future releases.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="3e858-209">Hochladen von CEIP </strong> -Daten (UevSqmUploader.exe)</span><span class="sxs-lookup"><span data-stu-id="3e858-209">Upload CEIP Data</strong> (UevSqmUploader.exe)</span></span></p></td>
<td align="left"><p><span data-ttu-id="3e858-210">Wird bei der Anmeldung und bei 4:00 am Tag danach ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3e858-210">Runs at logon and at 4:00 AM every day thereafter.</span></span></p></td>
<td align="left"><p><span data-ttu-id="3e858-211">Nein</span><span class="sxs-lookup"><span data-stu-id="3e858-211">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="3e858-212">Ja</span><span class="sxs-lookup"><span data-stu-id="3e858-212">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="3e858-213">Nur, wenn das Netzwerk verbunden ist</span><span class="sxs-lookup"><span data-stu-id="3e858-213">Only if Network is connected</span></span></p></td>
<td align="left"><p><span data-ttu-id="3e858-214">Wenn der Benutzer oder Administrator sich für das Programm zur Verbesserung der Benutzerfreundlichkeit einsetzt, werden die Daten von dieser Aufgabe auf die CEIP-Server hochgeladen.</span><span class="sxs-lookup"><span data-stu-id="3e858-214">If the user or administrator opts in to the Customer Experience Improvement Program (CEIP), this task uploads the data to the CEIP servers.</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="3e858-215">Legende</span><span class="sxs-lookup"><span data-stu-id="3e858-215">Legend</span></span>**

-   <span data-ttu-id="3e858-216">**Power Toggle** – der Aufgabenplaner optimiert den Energieverbrauch, wenn er nicht mit dem Stromnetz verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="3e858-216">**Power Toggle** – Task Scheduler will optimize power consumption when not connected to AC power.</span></span> <span data-ttu-id="3e858-217">Die Aufgabe kann nicht mehr ausgeführt werden, wenn der Computer in den Batteriebetrieb wechselt.</span><span class="sxs-lookup"><span data-stu-id="3e858-217">The task might stop running if the computer switches to battery power.</span></span>

-   <span data-ttu-id="3e858-218">**Nur im Leerlauf** – die Aufgabe wird nicht mehr ausgeführt, wenn der Computer nicht mehr im Leerlauf ist.</span><span class="sxs-lookup"><span data-stu-id="3e858-218">**Idle Only** – The task will stop running if the computer ceases to be idle.</span></span> <span data-ttu-id="3e858-219">Standardmäßig wird die Aufgabe nicht neu gestartet, wenn sich der Computer wieder im Leerlauf befindet.</span><span class="sxs-lookup"><span data-stu-id="3e858-219">By default the task will not restart when the computer is idle again.</span></span> <span data-ttu-id="3e858-220">Stattdessen wird die Aufgabe beim nächsten Aufgaben Auslöser erneut gestartet.</span><span class="sxs-lookup"><span data-stu-id="3e858-220">Instead the task will begin again on the next task trigger.</span></span>

-   <span data-ttu-id="3e858-221">**Netzwerkverbindung** – Aufgaben, die mit "Ja" gekennzeichnet sind, werden nur ausgeführt, wenn auf dem Computer eine Netzwerkverbindung verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="3e858-221">**Network Connection** – Tasks marked “Yes” only run if the computer has a network connection available.</span></span> <span data-ttu-id="3e858-222">Aufgaben, die mit "N/A" gekennzeichnet sind, werden unabhängig von der Netzwerkkonnektivität ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3e858-222">Tasks marked “N/A” run regardless of network connectivity.</span></span>

### <span data-ttu-id="3e858-223">Verwalten von geplanten Aufgaben</span><span class="sxs-lookup"><span data-stu-id="3e858-223">How to Manage Scheduled Tasks</span></span>

<span data-ttu-id="3e858-224">Führen Sie die folgenden Schritte aus, um geplante Aufgaben zu finden:</span><span class="sxs-lookup"><span data-stu-id="3e858-224">To find Scheduled Tasks, perform the following:</span></span>

1.  <span data-ttu-id="3e858-225">Öffnen Sie "Aufgaben planen" auf dem Computer des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="3e858-225">Open “Schedule Tasks” on the user computer.</span></span>

2.  <span data-ttu-id="3e858-226">Navigieren Sie zu: Aufgabenplanung- &gt; Taskplaner-Bibliothek- &gt; Microsoft- &gt; UE-V</span><span class="sxs-lookup"><span data-stu-id="3e858-226">Navigate to: Task Scheduler -&gt; Task Scheduler Library -&gt; Microsoft -&gt; UE-V</span></span>

3.  <span data-ttu-id="3e858-227">Wählen Sie im Detailbereich die geplante Aufgabe aus, die Sie verwalten und konfigurieren möchten.</span><span class="sxs-lookup"><span data-stu-id="3e858-227">Select the scheduled task you wish to manage and configure in the details pane.</span></span>

### <span data-ttu-id="3e858-228">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="3e858-228">Additional information</span></span>

<span data-ttu-id="3e858-229">Die folgenden zusätzlichen Informationen gelten für geplante UE-V-Aufgaben:</span><span class="sxs-lookup"><span data-stu-id="3e858-229">The following additional information applies to UE-V scheduled tasks:</span></span>

-   <span data-ttu-id="3e858-230">ll-Tasksequenz Programme befinden sich standardmäßig im Installationsordner des UE-V-Agents `%programFiles%\Microsoft User Experience Virtualization\Agent\[architecture]\` .</span><span class="sxs-lookup"><span data-stu-id="3e858-230">ll task sequence programs are located in the UE-V Agent installation folder, `%programFiles%\Microsoft User Experience Virtualization\Agent\[architecture]\`, by default.</span></span>

-   <span data-ttu-id="3e858-231">Die geplante Aufgabe der Synchronisierungs Controller Anwendung ist die entscheidende Komponente, wenn die UE-v-SyncMethod auf "SyncProvider" (UE-v 2-Standardkonfiguration) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="3e858-231">The Sync Controller Application Scheduled task is the crucial component when the UE-V SyncMethod is set to “SyncProvider” (UE-V 2 default configuration).</span></span> <span data-ttu-id="3e858-232">Mit dieser geplanten Aufgabe bleibt der SettingsSToragePath mit den lokal zwischengespeicherten Versionen der Einstellungspaket Dateien synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="3e858-232">This scheduled task keeps the SettingsSToragePath synchronized with the locally cached versions of the settings package files.</span></span> <span data-ttu-id="3e858-233">Wenn Benutzer sich beschweren, dass die Einstellungen nicht oft genug synchronisiert werden, können Sie die Einstellung für den geplanten Vorgang auf nur 1 Minute reduzieren.</span><span class="sxs-lookup"><span data-stu-id="3e858-233">If users complain that settings do not synchronize often enough, then you can reduce the scheduled task setting to as little as 1 minute.</span></span><span data-ttu-id="3e858-234">Sie können bei Bedarf auch den Standardwert von 30 Minuten auf einen höheren Betrag erhöhen.</span><span class="sxs-lookup"><span data-stu-id="3e858-234"> You can also increase the 30 min default to a higher amount if necessary.</span></span> <span data-ttu-id="3e858-235">Wenn Benutzer sich beschweren, dass die Einstellungen bei der Anmeldung nicht schnell genug synchronisiert werden, können Sie die Verzögerungseinstellung für den geplanten Vorgang entfernen.</span><span class="sxs-lookup"><span data-stu-id="3e858-235">If users complain that settings do not synchronize fast enough on logon, then you can remove the delay setting for the scheduled task.</span></span> <span data-ttu-id="3e858-236">(Sie können die Einstellung Verzögerung im Dialogfeld **Trigger bearbeiten** finden)</span><span class="sxs-lookup"><span data-stu-id="3e858-236">(You can find the delay setting in the **Edit Trigger** dialogue box)</span></span>

-   <span data-ttu-id="3e858-237">Sie müssen den geplanten Aufgabenplan automatisch aktualisieren nicht deaktivieren, wenn Sie eine andere Methode verwenden, um die Vorlagen der Clients synchron zu halten (also Gruppenrichtlinien-oder Configuration Manager-Basispläne).</span><span class="sxs-lookup"><span data-stu-id="3e858-237">You do not need to disable the Template Auto Update scheduled task if you use another method to keep the clients’ templates in sync (i.e. Group Policy or Configuration Manager Baselines).</span></span> <span data-ttu-id="3e858-238">Wenn der Wert der SettingsTemplateCatalog-Eigenschaft leer bleibt, verhindert UE-V, dass der Einstellungs Katalog für benutzerdefinierte Vorlagen überprüft wird.</span><span class="sxs-lookup"><span data-stu-id="3e858-238">Leaving the SettingsTemplateCatalog property value blank prevents UE-V from checking the settings catalog for custom templates.</span></span> <span data-ttu-id="3e858-239">Dieser geplante Task wird ApplySettingsCatalog.exe ausgeführt und wird im wesentlichen sofort zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="3e858-239">This scheduled task runs ApplySettingsCatalog.exe and will essentially return immediately.</span></span>

-   <span data-ttu-id="3e858-240">Der geplante Task "Anwendungseinstellungen überwachen" aktualisiert die Windows-App-Einstellungen (AppX) in Echtzeit basierend auf den Windows-app-Programm Einstellungs Triggern, die in jede APP integriert sind.</span><span class="sxs-lookup"><span data-stu-id="3e858-240">The Monitor Application Settings scheduled task will update Windows app (AppX) settings in real time, based on Windows app program setting triggers built into each app.</span></span>






## <span data-ttu-id="3e858-241">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="3e858-241">Related topics</span></span>


[<span data-ttu-id="3e858-242">Verwalten von UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="3e858-242">Administering UE-V 2.x</span></span>](administering-ue-v-2x-new-uevv2.md)

[<span data-ttu-id="3e858-243">Bereitstellen von UE-V 2. x für benutzerdefinierte Anwendungen</span><span class="sxs-lookup"><span data-stu-id="3e858-243">Deploy UE-V 2.x for Custom Applications</span></span>](deploy-ue-v-2x-for-custom-applications-new-uevv2.md#deploycatalogue)

 

 





