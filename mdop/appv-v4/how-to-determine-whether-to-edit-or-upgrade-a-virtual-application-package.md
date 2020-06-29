---
title: So ermitteln Sie, ob ein virtuelles Anwendungspaket bearbeitet oder aktualisiert werden soll
description: So ermitteln Sie, ob ein virtuelles Anwendungspaket bearbeitet oder aktualisiert werden soll
author: dansimp
ms.assetid: 33dd5332-6802-46e0-9748-43fcc8f80aa3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b256a4927231613b6f2e688b5951adf57c9cb89a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807132"
---
# <span data-ttu-id="656d6-103">So ermitteln Sie, ob ein virtuelles Anwendungspaket bearbeitet oder aktualisiert werden soll</span><span class="sxs-lookup"><span data-stu-id="656d6-103">How to Determine Whether to Edit or Upgrade a Virtual Application Package</span></span>


<span data-ttu-id="656d6-104">Verwenden Sie die folgende Tabelle, um zu ermitteln, ob ein virtuelles Anwendungspaket zur Bearbeitung geöffnet werden kann, ob Sie eine neue Version des Pakets erstellen müssen oder ob eine der beiden Optionen mithilfe des App-V-Sequencers verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="656d6-104">Use the following table to help determine whether a virtual application package can be opened for edit, whether you need to create a new version of the package, or whether either option is available, using the App-V Sequencer.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="656d6-105">Aktion</span><span class="sxs-lookup"><span data-stu-id="656d6-105">Action</span></span></th>
<th align="left"><span data-ttu-id="656d6-106">Zum Bearbeiten öffnen</span><span class="sxs-lookup"><span data-stu-id="656d6-106">Open for edit</span></span></th>
<th align="left"><span data-ttu-id="656d6-107">Für Upgrade öffnen</span><span class="sxs-lookup"><span data-stu-id="656d6-107">Open for upgrade</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="656d6-108">Anzeigen von Paketeigenschaften.</span><span class="sxs-lookup"><span data-stu-id="656d6-108">View package properties.</span></span></p></td>
<td align="left"><p><span data-ttu-id="656d6-109">Ja</span><span class="sxs-lookup"><span data-stu-id="656d6-109">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="656d6-110">Ja</span><span class="sxs-lookup"><span data-stu-id="656d6-110">Yes</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="656d6-111">Anzeigen des Paket Änderungsverlaufs</span><span class="sxs-lookup"><span data-stu-id="656d6-111">View package change history.</span></span></p></td>
<td align="left"><p><span data-ttu-id="656d6-112">Ja</span><span class="sxs-lookup"><span data-stu-id="656d6-112">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="656d6-113">Ja</span><span class="sxs-lookup"><span data-stu-id="656d6-113">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="656d6-114">Anzeigen zugehöriger Paketdateien</span><span class="sxs-lookup"><span data-stu-id="656d6-114">View associated package files.</span></span></p></td>
<td align="left"><p><span data-ttu-id="656d6-115">Ja</span><span class="sxs-lookup"><span data-stu-id="656d6-115">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="656d6-116">Ja</span><span class="sxs-lookup"><span data-stu-id="656d6-116">Yes</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="656d6-117">Bearbeiten Sie die Registrierungseinstellungen.</span><span class="sxs-lookup"><span data-stu-id="656d6-117">Edit registry settings.</span></span></p></td>
<td align="left"><p><span data-ttu-id="656d6-118">Ja</span><span class="sxs-lookup"><span data-stu-id="656d6-118">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="656d6-119">Ja</span><span class="sxs-lookup"><span data-stu-id="656d6-119">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="656d6-120">Überprüfen Sie die zusätzlichen Paketeinstellungen (mit Ausnahme der Dateieigenschaften des Betriebssystems).</span><span class="sxs-lookup"><span data-stu-id="656d6-120">Review additional package settings (except operating system file properties).</span></span></p></td>
<td align="left"><p><span data-ttu-id="656d6-121">Ja</span><span class="sxs-lookup"><span data-stu-id="656d6-121">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="656d6-122">Ja</span><span class="sxs-lookup"><span data-stu-id="656d6-122">Yes</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="656d6-123">Erstellen Sie zugeordnete Windows Installer (MSI).</span><span class="sxs-lookup"><span data-stu-id="656d6-123">Create associated Windows Installer (MSI).</span></span></p></td>
<td align="left"><p><span data-ttu-id="656d6-124">Ja</span><span class="sxs-lookup"><span data-stu-id="656d6-124">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="656d6-125">Ja</span><span class="sxs-lookup"><span data-stu-id="656d6-125">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="656d6-126">OSD-Datei ändern.</span><span class="sxs-lookup"><span data-stu-id="656d6-126">Modify OSD file.</span></span></p></td>
<td align="left"><p><span data-ttu-id="656d6-127">Ja</span><span class="sxs-lookup"><span data-stu-id="656d6-127">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="656d6-128">Ja</span><span class="sxs-lookup"><span data-stu-id="656d6-128">Yes</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="656d6-129">Komprimieren und Dekomprimieren des Pakets.</span><span class="sxs-lookup"><span data-stu-id="656d6-129">Compress and uncompress package.</span></span></p></td>
<td align="left"><p><span data-ttu-id="656d6-130">Ja</span><span class="sxs-lookup"><span data-stu-id="656d6-130">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="656d6-131">Ja</span><span class="sxs-lookup"><span data-stu-id="656d6-131">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="656d6-132">Dateitypzuordnungen hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="656d6-132">Add file type associations.</span></span></p></td>
<td align="left"><p><span data-ttu-id="656d6-133">Ja</span><span class="sxs-lookup"><span data-stu-id="656d6-133">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="656d6-134">Ja</span><span class="sxs-lookup"><span data-stu-id="656d6-134">Yes</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="656d6-135">Umbenennen von Tastenkombinationen</span><span class="sxs-lookup"><span data-stu-id="656d6-135">Rename shortcuts.</span></span></p></td>
<td align="left"><p><span data-ttu-id="656d6-136">Ja</span><span class="sxs-lookup"><span data-stu-id="656d6-136">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="656d6-137">Ja</span><span class="sxs-lookup"><span data-stu-id="656d6-137">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="656d6-138">Legen Sie den virtualisierten Registrierungsschlüssel Status fest (override/Merge).</span><span class="sxs-lookup"><span data-stu-id="656d6-138">Set virtualized registry key state (override / merge).</span></span></p></td>
<td align="left"><p><span data-ttu-id="656d6-139">Ja</span><span class="sxs-lookup"><span data-stu-id="656d6-139">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="656d6-140">Ja</span><span class="sxs-lookup"><span data-stu-id="656d6-140">Yes</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="656d6-141">Legen Sie den Status eines virtualisierten Ordners fest.</span><span class="sxs-lookup"><span data-stu-id="656d6-141">Set virtualized folder state.</span></span></p></td>
<td align="left"><p><span data-ttu-id="656d6-142">Ja</span><span class="sxs-lookup"><span data-stu-id="656d6-142">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="656d6-143">Ja</span><span class="sxs-lookup"><span data-stu-id="656d6-143">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="656d6-144">Bearbeiten von virtuellen Dateisystem Zuordnungen</span><span class="sxs-lookup"><span data-stu-id="656d6-144">Edit virtual file system mappings.</span></span></p></td>
<td align="left"><p><span data-ttu-id="656d6-145">Ja</span><span class="sxs-lookup"><span data-stu-id="656d6-145">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="656d6-146">Ja</span><span class="sxs-lookup"><span data-stu-id="656d6-146">Yes</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="656d6-147">Überprüfen Sie alle zugehörigen Betriebssystem-Dateieigenschaften für ein Paket.</span><span class="sxs-lookup"><span data-stu-id="656d6-147">Review all associated operating system file properties for a package.</span></span></p></td>
<td align="left"><p><span data-ttu-id="656d6-148">Nein</span><span class="sxs-lookup"><span data-stu-id="656d6-148">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="656d6-149">Ja</span><span class="sxs-lookup"><span data-stu-id="656d6-149">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="656d6-150">Weitere Dienste hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="656d6-150">Add additional services.</span></span></p></td>
<td align="left"><p><span data-ttu-id="656d6-151">Nein</span><span class="sxs-lookup"><span data-stu-id="656d6-151">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="656d6-152">Ja</span><span class="sxs-lookup"><span data-stu-id="656d6-152">Yes</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="656d6-153">Fügen Sie weitere Dateien hinzu.</span><span class="sxs-lookup"><span data-stu-id="656d6-153">Add additional files.</span></span></p></td>
<td align="left"><p><span data-ttu-id="656d6-154">Nein</span><span class="sxs-lookup"><span data-stu-id="656d6-154">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="656d6-155">Ja</span><span class="sxs-lookup"><span data-stu-id="656d6-155">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="656d6-156">Sammeln und Konfigurieren von zugehörigen Sicherheitsbeschreibungen</span><span class="sxs-lookup"><span data-stu-id="656d6-156">Collect and configure associated security descriptors.</span></span></p></td>
<td align="left"><p><span data-ttu-id="656d6-157">Nein</span><span class="sxs-lookup"><span data-stu-id="656d6-157">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="656d6-158">Ja</span><span class="sxs-lookup"><span data-stu-id="656d6-158">Yes</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="656d6-159">Wenden Sie Sicherheitsupdates an, oder aktualisieren Sie auf eine neue Version.</span><span class="sxs-lookup"><span data-stu-id="656d6-159">Apply security updates or upgrade to a new version.</span></span></p></td>
<td align="left"><p><span data-ttu-id="656d6-160">Nein</span><span class="sxs-lookup"><span data-stu-id="656d6-160">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="656d6-161">Ja</span><span class="sxs-lookup"><span data-stu-id="656d6-161">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="656d6-162">Hinzufügen einer zusätzlichen Anwendung</span><span class="sxs-lookup"><span data-stu-id="656d6-162">Add an additional application.</span></span></p></td>
<td align="left"><p><span data-ttu-id="656d6-163">Nein</span><span class="sxs-lookup"><span data-stu-id="656d6-163">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="656d6-164">Ja</span><span class="sxs-lookup"><span data-stu-id="656d6-164">Yes</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="656d6-165">Wenden Sie Updates an, für die die Anwendung geöffnet werden muss.</span><span class="sxs-lookup"><span data-stu-id="656d6-165">Apply updates that require the application to open.</span></span></p></td>
<td align="left"><p><span data-ttu-id="656d6-166">Nein</span><span class="sxs-lookup"><span data-stu-id="656d6-166">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="656d6-167">Ja</span><span class="sxs-lookup"><span data-stu-id="656d6-167">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="656d6-168">Wenden Sie Updates an, die erfordern, dass der Computer neu gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="656d6-168">Apply updates that require the computer to restart.</span></span></p></td>
<td align="left"><p><span data-ttu-id="656d6-169">Nein</span><span class="sxs-lookup"><span data-stu-id="656d6-169">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="656d6-170">Ja</span><span class="sxs-lookup"><span data-stu-id="656d6-170">Yes</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="656d6-171">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="656d6-171">Related topics</span></span>


[<span data-ttu-id="656d6-172">So bearbeiten Sie eine vorhandene virtuelle Anwendung</span><span class="sxs-lookup"><span data-stu-id="656d6-172">How to Edit an Existing Virtual Application</span></span>](how-to-edit-an-existing-virtual-application.md)

[<span data-ttu-id="656d6-173">So aktualisieren Sie eine vorhandene virtuelle Anwendung</span><span class="sxs-lookup"><span data-stu-id="656d6-173">How to Upgrade an Existing Virtual Application</span></span>](how-to-upgrade-an-existing-virtual-application.md)

 

 





