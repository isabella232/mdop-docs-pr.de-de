---
title: Verlaufsfenster
description: Verlaufsfenster
author: dansimp
ms.assetid: 114f50a4-508d-4589-b006-6cd05cffe6b7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 81911b5103c76e267d806fb7cd8acf55811440c9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808451"
---
# <span data-ttu-id="e59d4-103">Verlaufsfenster</span><span class="sxs-lookup"><span data-stu-id="e59d4-103">History Window</span></span>


<span data-ttu-id="e59d4-104">Der Verlauf eines Gruppenrichtlinienobjekts (GPO) kann angezeigt werden, indem Sie auf ein GPO doppelklicken oder mit der rechten Maustaste auf ein GPO und dann auf **Verlauf**klicken.</span><span class="sxs-lookup"><span data-stu-id="e59d4-104">The history of a Group Policy Object (GPO) can be displayed by double-clicking a GPO or by right-clicking a GPO and then clicking **History**.</span></span> <span data-ttu-id="e59d4-105">Darüber hinaus wird es in der **Gruppenrichtlinien-Verwaltungskonsole (Group Policy Management Console** , GPMC) als Registerkarte für jedes GPO angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e59d4-105">It is also displayed in the **Group Policy Management Console** (GPMC) as a tab for each GPO.</span></span>

<span data-ttu-id="e59d4-106">Das Protokoll enthält eine Aufzeichnung der Ereignisse in der Lebensdauer des ausgewählten Gruppenrichtlinienobjekts.</span><span class="sxs-lookup"><span data-stu-id="e59d4-106">The history provides a record of events in the lifetime of the selected GPO.</span></span> <span data-ttu-id="e59d4-107">Im Fenster " **Verlauf** " können Sie einen Bericht über die Einstellungen in einer Version des Gruppenrichtlinienobjekts abrufen, mehrere Versionen eines GPO vergleichen oder auf eine frühere Version eines GPO zurückgreifen.</span><span class="sxs-lookup"><span data-stu-id="e59d4-107">From the **History** window, you can obtain a report of the settings within a version of the GPO, compare multiple versions of a GPO, or roll back to a previous version of a GPO.</span></span>

## <span data-ttu-id="e59d4-108">Filtern von Ereignissen im Verlaufsfenster</span><span class="sxs-lookup"><span data-stu-id="e59d4-108">Filtering events in the History window</span></span>


<span data-ttu-id="e59d4-109">Die Registerkarten im **Verlaufs** Fenster filtern die Zustände im Verlauf des Gruppenrichtlinienobjekts.</span><span class="sxs-lookup"><span data-stu-id="e59d4-109">The tabs within the **History** window filter the states in the history of the GPO.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="e59d4-110">Tabs</span><span class="sxs-lookup"><span data-stu-id="e59d4-110">Tabs</span></span></th>
<th align="left"><span data-ttu-id="e59d4-111">Filterung</span><span class="sxs-lookup"><span data-stu-id="e59d4-111">Filtering</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="e59d4-112">Alle Zustände</span><span class="sxs-lookup"><span data-stu-id="e59d4-112">All States</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="e59d4-113">Zeigt alle Zustände im Verlauf des Gruppenrichtlinienobjekts an.</span><span class="sxs-lookup"><span data-stu-id="e59d4-113">Display all states in the history of the GPO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="e59d4-114">Eindeutige Versionen</span><span class="sxs-lookup"><span data-stu-id="e59d4-114">Unique Versions</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="e59d4-115">Zeigt nur eindeutige Versionen des in das Archiv eingecheckten Gruppenrichtlinienobjekts an.</span><span class="sxs-lookup"><span data-stu-id="e59d4-115">Display only unique versions of the GPO checked into the archive.</span></span> <span data-ttu-id="e59d4-116">Die Version, die in der Produktionsumgebung bereitgestellt wird, Verknüpfungen zu eindeutigen Versionen und Informationsstatus werden in dieser Liste ausgelassen.</span><span class="sxs-lookup"><span data-stu-id="e59d4-116">The version deployed to the production environment, shortcuts to unique versions, and informational states are omitted from this list.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="e59d4-117">Ereignisinformationen</span><span class="sxs-lookup"><span data-stu-id="e59d4-117">Event information</span></span>


<span data-ttu-id="e59d4-118">Informationen werden für jeden Zustand im Verlauf des Gruppenrichtlinienobjekts bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="e59d4-118">Information is provided for each state in the history of the GPO.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="e59d4-119">GPO-Attribut</span><span class="sxs-lookup"><span data-stu-id="e59d4-119">GPO attribute</span></span></th>
<th align="left"><span data-ttu-id="e59d4-120">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e59d4-120">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="e59d4-121">Datum ändern</span><span class="sxs-lookup"><span data-stu-id="e59d4-121">Change Date</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="e59d4-122">Der Zeitstempel des Vorgangs, in dem die Aktion in der <strong> Spalte "Zustand" </strong> ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="e59d4-122">Time stamp of when the action in the <strong>State</strong> column was performed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="e59d4-123">Status</span><span class="sxs-lookup"><span data-stu-id="e59d4-123">State</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="e59d4-124">Ein Zustand im Verlauf des Gruppenrichtlinienobjekts.</span><span class="sxs-lookup"><span data-stu-id="e59d4-124">A state in the history of the GPO.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="e59d4-125">Geändert von</span><span class="sxs-lookup"><span data-stu-id="e59d4-125">Changed By</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="e59d4-126">Die Person, die das Gruppenrichtlinienobjekt eingecheckt oder bereitgestellt hat.</span><span class="sxs-lookup"><span data-stu-id="e59d4-126">The person who checked in or deployed the GPO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="e59d4-127">Kommentar</span><span class="sxs-lookup"><span data-stu-id="e59d4-127">Comment</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="e59d4-128">Ein Kommentar, der von der Person eingegeben wurde, die zum Zeitpunkt der Änderung dieser Version ein GPO eingecheckt oder bereitgestellt hat.</span><span class="sxs-lookup"><span data-stu-id="e59d4-128">A comment entered by the person who checked in or deployed a GPO at the time that this version was modified.</span></span> <span data-ttu-id="e59d4-129">Nützlich, um die Besonderheiten der Version zu identifizieren, falls ein Rollback auf eine vorherige Version erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="e59d4-129">Useful for identifying the specifics of the version in case of the need to roll back to a previous version.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="e59d4-130">Löschbar</span><span class="sxs-lookup"><span data-stu-id="e59d4-130">Deletable</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="e59d4-131">Ob diese Version des Gruppenrichtlinienobjekts gelöscht werden kann, wenn die Anzahl der eindeutigen Versionen jedes im Archiv aufbewahrten Gruppenrichtlinienobjekts limitiert ist.</span><span class="sxs-lookup"><span data-stu-id="e59d4-131">Whether this version of the GPO can be deleted if the number of unique versions of each GPO retained in the archive is limited.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="e59d4-132">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="e59d4-132">Note</span></span></strong><br/><p><span data-ttu-id="e59d4-133">Sie können ändern, ob eine Version eines Gruppenrichtlinienobjekts löschbar ist, indem Sie mit der rechten Maustaste darauf klicken und dann auf " <strong> Löschen" </strong> oder "Löschen zulassen" klicken <strong> </strong> .</span><span class="sxs-lookup"><span data-stu-id="e59d4-133">You can modify whether a version of a GPO is deletable by right-clicking it and then clicking <strong>Do Not Allow Deletion</strong> or <strong>Allow Deletion</strong>.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="e59d4-134">Computer Version</span><span class="sxs-lookup"><span data-stu-id="e59d4-134">Computer Version</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="e59d4-135">Automatisch generierte Version des Computer Konfigurations Teils des Gruppenrichtlinienobjekts.</span><span class="sxs-lookup"><span data-stu-id="e59d4-135">Automatically generated version of the Computer Configuration portion of the GPO.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="e59d4-136">Benutzer Version</span><span class="sxs-lookup"><span data-stu-id="e59d4-136">User Version</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="e59d4-137">Automatisch generierte Version des Benutzer Konfigurations Teils des Gruppenrichtlinienobjekts.</span><span class="sxs-lookup"><span data-stu-id="e59d4-137">Automatically generated version of the User Configuration portion of the GPO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="e59d4-138">GPO-Status</span><span class="sxs-lookup"><span data-stu-id="e59d4-138">GPO Status</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="e59d4-139">Die Computer Konfiguration und die Benutzerkonfiguration können separat verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="e59d4-139">The Computer Configuration and the User Configuration can be managed separately from each other.</span></span> <span data-ttu-id="e59d4-140">Dieser Status zeigt an, welche Teile des Gruppenrichtlinienobjekts aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="e59d4-140">This status shows which portions of the GPO are enabled.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="e59d4-141">WMI-Filter</span><span class="sxs-lookup"><span data-stu-id="e59d4-141">WMI Filter</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="e59d4-142">Zeigen Sie alle WMI-Filter an, die auf dieses Gruppenrichtlinienobjekt angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="e59d4-142">Display any WMI filters that are applied to this GPO.</span></span> <span data-ttu-id="e59d4-143">WMI-Filter werden in der <strong> </strong> Konsolenstruktur der GPMC unter dem Ordner WMI-Filter für die Domäne verwaltet.</span><span class="sxs-lookup"><span data-stu-id="e59d4-143">WMI filters are managed under the <strong>WMI Filters</strong> folder for the domain in the console tree of the GPMC.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="e59d4-144">Berichte</span><span class="sxs-lookup"><span data-stu-id="e59d4-144">Reports</span></span>


<span data-ttu-id="e59d4-145">Auf den Schaltflächen **Einstellungen** und **Unterschiede** werden Berichte zu den GPO-Einstellungen für die ausgewählte GPO-Version oder Versionen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e59d4-145">The **Settings** and **Differences** buttons display reports about GPO settings for the GPO version or versions selected.</span></span> <span data-ttu-id="e59d4-146">Mit der rechten Maustaste auf GPO-Versionen können auch XML-basierte Berichte angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="e59d4-146">Right-clicking GPO versions provides the option to display XML-based reports as well.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="e59d4-147">Button</span><span class="sxs-lookup"><span data-stu-id="e59d4-147">Button</span></span></th>
<th align="left"><span data-ttu-id="e59d4-148">Effekt</span><span class="sxs-lookup"><span data-stu-id="e59d4-148">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="e59d4-149">Einstellungen</span><span class="sxs-lookup"><span data-stu-id="e59d4-149">Settings</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="e59d4-150">Einen HTML-basierten Bericht generieren, in dem die Einstellungen in der ausgewählten Version des Gruppenrichtlinienobjekts angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="e59d4-150">Generate an HTML-based report displaying the settings within the selected version of the GPO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="e59d4-151">Unterschiede</span><span class="sxs-lookup"><span data-stu-id="e59d4-151">Differences</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="e59d4-152">Generieren eines HTML-basierten Berichts, der die Einstellungen in mehreren ausgewählten Versionen des Gruppenrichtlinienobjekts vergleicht.</span><span class="sxs-lookup"><span data-stu-id="e59d4-152">Generate an HTML-based report comparing the settings within multiple selected versions of the GPO.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="e59d4-153">Schlüssel für Unterschiedsberichte</span><span class="sxs-lookup"><span data-stu-id="e59d4-153">Key to difference reports</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="e59d4-154">Symbol</span><span class="sxs-lookup"><span data-stu-id="e59d4-154">Symbol</span></span></th>
<th align="left"><span data-ttu-id="e59d4-155">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="e59d4-155">Meaning</span></span></th>
<th align="left"><span data-ttu-id="e59d4-156">Farbe</span><span class="sxs-lookup"><span data-stu-id="e59d4-156">Color</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e59d4-157">Keine</span><span class="sxs-lookup"><span data-stu-id="e59d4-157">None</span></span></p></td>
<td align="left"><p><span data-ttu-id="e59d4-158">Element mit identischen Einstellungen in beiden GPOs vorhanden</span><span class="sxs-lookup"><span data-stu-id="e59d4-158">Item exists with identical settings in both GPOs</span></span></p></td>
<td align="left"><p><span data-ttu-id="e59d4-159">Variiert je nach Ebene</span><span class="sxs-lookup"><span data-stu-id="e59d4-159">Varies with level</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="e59d4-160">[#]</span><span class="sxs-lookup"><span data-stu-id="e59d4-160">[#]</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="e59d4-161">Element ist in beiden GPOs vorhanden, jedoch mit geänderten Einstellungen</span><span class="sxs-lookup"><span data-stu-id="e59d4-161">Item exists in both GPOs, but with changed settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="e59d4-162">Blaue</span><span class="sxs-lookup"><span data-stu-id="e59d4-162">Blue</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="e59d4-163">[-]</span><span class="sxs-lookup"><span data-stu-id="e59d4-163">[-]</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="e59d4-164">Element ist nur im ersten GPO vorhanden</span><span class="sxs-lookup"><span data-stu-id="e59d4-164">Item exists only in the first GPO</span></span></p></td>
<td align="left"><p><span data-ttu-id="e59d4-165">Rot</span><span class="sxs-lookup"><span data-stu-id="e59d4-165">Red</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="e59d4-166">[+]</span><span class="sxs-lookup"><span data-stu-id="e59d4-166">[+]</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="e59d4-167">Element ist nur im zweiten GPO vorhanden</span><span class="sxs-lookup"><span data-stu-id="e59d4-167">Item exists only in the second GPO</span></span></p></td>
<td align="left"><p><span data-ttu-id="e59d4-168">Grün</span><span class="sxs-lookup"><span data-stu-id="e59d4-168">Green</span></span></p></td>
</tr>
</tbody>
</table>



-   <span data-ttu-id="e59d4-169">Bei Elementen mit geänderten Einstellungen werden die geänderten Einstellungen identifiziert, wenn das Element erweitert wird.</span><span class="sxs-lookup"><span data-stu-id="e59d4-169">For items with changed settings, the changed settings are identified when the item is expanded.</span></span> <span data-ttu-id="e59d4-170">Der Wert für das Attribut in den einzelnen Gruppenrichtlinienobjekten wird in der Reihenfolge angezeigt, in der die GPOs im Bericht angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="e59d4-170">The value for the attribute in each GPO is displayed in the same order that the GPOs are displayed in the report.</span></span>

-   <span data-ttu-id="e59d4-171">Einige Änderungen an Einstellungen können dazu führen, dass ein Element als zwei unterschiedliche Elemente gemeldet wird (eines ist nur im ersten GPO vorhanden, das nur in der zweiten vorhanden ist), und nicht als ein Element, das sich geändert hat.</span><span class="sxs-lookup"><span data-stu-id="e59d4-171">Some changes to settings may cause an item to be reported as two different items (one present only in the first GPO, one present only in the second), rather than as one item that has changed.</span></span>

### <span data-ttu-id="e59d4-172">Weitere Verweise</span><span class="sxs-lookup"><span data-stu-id="e59d4-172">Additional references</span></span>

-   [<span data-ttu-id="e59d4-173">Registerkarte "Inhalt"</span><span class="sxs-lookup"><span data-stu-id="e59d4-173">Contents Tab</span></span>](contents-tab-agpm30ops.md)









