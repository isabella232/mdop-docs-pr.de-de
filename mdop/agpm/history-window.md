---
title: Verlaufsfenster
description: Verlaufsfenster
author: dansimp
ms.assetid: f11f9ad9-bffe-4c56-8c46-fe9c0a8e55c1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 02b4336409f33d6c1f2868bceb22cb95120f2198
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808447"
---
# <span data-ttu-id="9f7e7-103">Verlaufsfenster</span><span class="sxs-lookup"><span data-stu-id="9f7e7-103">History Window</span></span>


<span data-ttu-id="9f7e7-104">Der Verlauf eines Gruppenrichtlinienobjekts (GPO) kann angezeigt werden, indem Sie auf ein GPO doppelklicken oder mit der rechten Maustaste auf ein GPO und dann auf **Verlauf**klicken.</span><span class="sxs-lookup"><span data-stu-id="9f7e7-104">The history of a Group Policy object (GPO) can be displayed by double-clicking a GPO or by right-clicking a GPO and then clicking **History**.</span></span> <span data-ttu-id="9f7e7-105">Darüber hinaus wird es in der **Gruppenrichtlinien-Verwaltungskonsole (Group Policy Management Console** , GPMC) als Registerkarte für jedes GPO angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9f7e7-105">It is also displayed in the **Group Policy Management Console** (GPMC) as a tab for each GPO.</span></span>

<span data-ttu-id="9f7e7-106">Das Protokoll enthält eine Liste aller Versionen des ausgewählten GPO, die im Archiv gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="9f7e7-106">The history provides a list of all versions of the selected GPO saved within the archive.</span></span> <span data-ttu-id="9f7e7-107">Im Fenster " **Verlauf** " können Sie einen Bericht über die Einstellungen in einem Gruppenrichtlinienobjekt abrufen, mehrere Versionen eines GPO vergleichen oder auf eine frühere Version eines GPO zurückgreifen.</span><span class="sxs-lookup"><span data-stu-id="9f7e7-107">From the **History** window, you can obtain a report of the settings within a GPO, compare multiple versions of a GPO, or roll back to a previous version of a GPO.</span></span>

## <span data-ttu-id="9f7e7-108">Filtern von Ereignissen im Verlaufsfenster</span><span class="sxs-lookup"><span data-stu-id="9f7e7-108">Filtering events in the History window</span></span>


<span data-ttu-id="9f7e7-109">Die Registerkarten im **Verlaufs** Fenster filtern die angezeigten Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="9f7e7-109">The tabs within the **History** window filter the events displayed.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="9f7e7-110">Tabs</span><span class="sxs-lookup"><span data-stu-id="9f7e7-110">Tabs</span></span></th>
<th align="left"><span data-ttu-id="9f7e7-111">Filterung</span><span class="sxs-lookup"><span data-stu-id="9f7e7-111">Filtering</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="9f7e7-112">Alle anzeigen</span><span class="sxs-lookup"><span data-stu-id="9f7e7-112">Show All</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="9f7e7-113">Anzeigen aller Versionen des Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="9f7e7-113">Display all versions of the GPO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="9f7e7-114">Eingecheckt</span><span class="sxs-lookup"><span data-stu-id="9f7e7-114">Checked In</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="9f7e7-115">Anzeigen nur eingecheckter Versionen des Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="9f7e7-115">Display only checked-in versions of the GPO.</span></span> <span data-ttu-id="9f7e7-116">Die bereitgestellte Version wird in dieser Liste ausgelassen.</span><span class="sxs-lookup"><span data-stu-id="9f7e7-116">The deployed version is omitted from this list.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="9f7e7-117">Nur Etiketten</span><span class="sxs-lookup"><span data-stu-id="9f7e7-117">Labels Only</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="9f7e7-118">Nur GPOs anzeigen, denen Beschriftungen zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="9f7e7-118">Display only GPOs that have labels associated with them.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="9f7e7-119">Ereignisinformationen</span><span class="sxs-lookup"><span data-stu-id="9f7e7-119">Event information</span></span>


<span data-ttu-id="9f7e7-120">Für jedes Ereignis im Verlauf des ausgewählten Gruppenrichtlinienobjekts werden Informationen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="9f7e7-120">Information is provided for each event in the history of the selected GPO.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="9f7e7-121">GPO-Merkmal</span><span class="sxs-lookup"><span data-stu-id="9f7e7-121">GPO Characteristic</span></span></th>
<th align="left"><span data-ttu-id="9f7e7-122">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9f7e7-122">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="9f7e7-123">Computer</span><span class="sxs-lookup"><span data-stu-id="9f7e7-123">Computer</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="9f7e7-124">Automatisch generierte Version des Computer Konfigurations Teils des Gruppenrichtlinienobjekts.</span><span class="sxs-lookup"><span data-stu-id="9f7e7-124">Automatically generated version of the Computer Configuration portion of the GPO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="9f7e7-125">Benutzer</span><span class="sxs-lookup"><span data-stu-id="9f7e7-125">User</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="9f7e7-126">Automatisch generierte Version des Benutzer Konfigurations Teils des Gruppenrichtlinienobjekts.</span><span class="sxs-lookup"><span data-stu-id="9f7e7-126">Automatically generated version of the User Configuration portion of the GPO.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="9f7e7-127">Zeit</span><span class="sxs-lookup"><span data-stu-id="9f7e7-127">Time</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="9f7e7-128">Timestamp der Version des Gruppenrichtlinienobjekts, wenn die Aktion im Feld Status durchgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="9f7e7-128">Timestamp of the version of the GPO when the action in the status field was performed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="9f7e7-129">Status</span><span class="sxs-lookup"><span data-stu-id="9f7e7-129">State</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="9f7e7-130">Der Status der ausgewählten Version des Gruppenrichtlinienobjekts:</span><span class="sxs-lookup"><span data-stu-id="9f7e7-130">The state of the selected version of the GPO:</span></span></p>
<p><img src="images/36f6b687-f5cc-40d1-805f-b191d1fb1ace.gif" alt="Deployed GPO icon" /> <strong><span data-ttu-id="9f7e7-131">Bereitgestellt </strong> : Diese Version des Gruppenrichtlinienobjekts befindet sich derzeit in der Produktionsumgebung.</span><span class="sxs-lookup"><span data-stu-id="9f7e7-131">Deployed</strong>: This version of the GPO is currently live in the production environment.</span></span></p>
<p><img src="images/57b610a5-1c71-4d26-9173-d04abd495fcc.gif" alt="Checked in GPO icon" /> <strong><span data-ttu-id="9f7e7-132">Eingecheckt </strong> : Diese Version des Gruppenrichtlinienobjekts steht autorisierten Editoren zum Auschecken zur Bearbeitung oder zum Bereitstellen eines Gruppenrichtlinienadministrators zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="9f7e7-132">Checked In</strong>: This version of the GPO is available for authorized Editors to check out for editing or for a Group Policy administrator to deploy.</span></span></p>
<p><img src="images/8e7a7c4e-809a-435a-8b29-30d797936210.gif" alt="Checked out GPO icon" /> <strong><span data-ttu-id="9f7e7-133">Ausgecheckt </strong> : Diese Version des Gruppenrichtlinienobjekts ist derzeit von einem Editor ausgecheckt und steht für andere Editoren nicht zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="9f7e7-133">Checked Out</strong>: This version of the GPO is currently checked out by an Editor and is unavailable for other Editors.</span></span> <span data-ttu-id="9f7e7-134">(Der Status "ausgecheckt" wird im <strong> Protokoll </strong> , außer um anzugeben, ob ein GPO zurzeit ausgecheckt ist.)</span><span class="sxs-lookup"><span data-stu-id="9f7e7-134">(The checked out state is not recorded in the <strong>History</strong> except to indicate if a GPO is currently checked out.)</span></span></p>
<p><img src="images/327623bd-0842-4372-be1f-bdc4b8c3481c.gif" alt="Created GPO icon" /> <strong><span data-ttu-id="9f7e7-135">Erstellt </strong> : gibt das Datum und die Uhrzeit der anfänglichen Erstellung des Gruppenrichtlinienobjekts an.</span><span class="sxs-lookup"><span data-stu-id="9f7e7-135">Created</strong>: Identifies the date and time of the initial creation of the GPO.</span></span></p>
<p><img src="images/8356fcdc-1279-425b-ab14-a23bcfe391da.gif" alt="Labeled GPO icon" /> <strong><span data-ttu-id="9f7e7-136">Gekennzeichnet </strong> : gibt eine beschriftete Version des Gruppenrichtlinienobjekts an.</span><span class="sxs-lookup"><span data-stu-id="9f7e7-136">Labeled</strong>: Identifies a labeled version of the GPO.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="9f7e7-137">GPO-Status</span><span class="sxs-lookup"><span data-stu-id="9f7e7-137">GPO Status</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="9f7e7-138">Die Computer Konfiguration und die Benutzerkonfiguration können separat verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="9f7e7-138">The Computer Configuration and the User Configuration can be managed separately from each other.</span></span> <span data-ttu-id="9f7e7-139">Dieser Status zeigt an, welche Teile des Gruppenrichtlinienobjekts aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="9f7e7-139">This status shows which portions of the GPO are enabled.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="9f7e7-140">Besitzer</span><span class="sxs-lookup"><span data-stu-id="9f7e7-140">Owner</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="9f7e7-141">Die Person, die das Gruppenrichtlinienobjekt eingecheckt oder bereitgestellt hat.</span><span class="sxs-lookup"><span data-stu-id="9f7e7-141">The person who checked in or deployed the GPO.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="9f7e7-142">Kommentar</span><span class="sxs-lookup"><span data-stu-id="9f7e7-142">Comment</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="9f7e7-143">Ein Kommentar, der vom Besitzer eines Gruppenrichtlinienobjekts zu dem Zeitpunkt eingegeben wurde, zu dem diese Version geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="9f7e7-143">A comment entered by the owner of a GPO at the time that this version was modified.</span></span> <span data-ttu-id="9f7e7-144">Nützlich, um die Besonderheiten der Version zu identifizieren, falls ein Rollback auf eine vorherige Version erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="9f7e7-144">Useful for identifying the specifics of the version in case of the need to roll back to a previous version.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="9f7e7-145">Berichte</span><span class="sxs-lookup"><span data-stu-id="9f7e7-145">Reports</span></span>


<span data-ttu-id="9f7e7-146">Je nachdem, ob eine einzelne GPO-Version oder mehrere GPO-Versionen ausgewählt sind, werden auf den Schaltflächen **Einstellungen** und **Unterschiede** Berichte zu den GPO-Einstellungen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9f7e7-146">Depending on whether a single GPO version or multiple GPO versions are selected, the **Settings** and **Differences** buttons display reports on GPO settings.</span></span> <span data-ttu-id="9f7e7-147">Mit der rechten Maustaste auf GPO-Versionen können auch XML-basierte Berichte angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="9f7e7-147">Right-clicking GPO versions provides the option to display XML-based reports as well.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="9f7e7-148">Button</span><span class="sxs-lookup"><span data-stu-id="9f7e7-148">Button</span></span></th>
<th align="left"><span data-ttu-id="9f7e7-149">Effekt</span><span class="sxs-lookup"><span data-stu-id="9f7e7-149">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="9f7e7-150">Einstellungen</span><span class="sxs-lookup"><span data-stu-id="9f7e7-150">Settings</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="9f7e7-151">Einen HTML-basierten Bericht generieren, in dem die Einstellungen in der ausgewählten Version des Gruppenrichtlinienobjekts angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="9f7e7-151">Generate an HTML-based report displaying the settings within the selected version of the GPO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="9f7e7-152">Unterschiede</span><span class="sxs-lookup"><span data-stu-id="9f7e7-152">Differences</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="9f7e7-153">Generieren eines HTML-basierten Berichts, der die Einstellungen in mehreren ausgewählten Versionen des Gruppenrichtlinienobjekts vergleicht.</span><span class="sxs-lookup"><span data-stu-id="9f7e7-153">Generate an HTML-based report comparing the settings within multiple selected versions of the GPO.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="9f7e7-154">Schlüssel für Unterschiedsberichte</span><span class="sxs-lookup"><span data-stu-id="9f7e7-154">Key to difference reports</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="9f7e7-155">Symbol</span><span class="sxs-lookup"><span data-stu-id="9f7e7-155">Symbol</span></span></th>
<th align="left"><span data-ttu-id="9f7e7-156">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="9f7e7-156">Meaning</span></span></th>
<th align="left"><span data-ttu-id="9f7e7-157">Farbe</span><span class="sxs-lookup"><span data-stu-id="9f7e7-157">Color</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9f7e7-158">Keine</span><span class="sxs-lookup"><span data-stu-id="9f7e7-158">None</span></span></p></td>
<td align="left"><p><span data-ttu-id="9f7e7-159">Element mit identischen Einstellungen in beiden GPOs vorhanden</span><span class="sxs-lookup"><span data-stu-id="9f7e7-159">Item exists with identical settings in both GPOs</span></span></p></td>
<td align="left"><p><span data-ttu-id="9f7e7-160">Variiert je nach Ebene</span><span class="sxs-lookup"><span data-stu-id="9f7e7-160">Varies with level</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="9f7e7-161">[#]</span><span class="sxs-lookup"><span data-stu-id="9f7e7-161">[#]</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="9f7e7-162">Element ist in beiden GPOs vorhanden, jedoch mit geänderten Einstellungen</span><span class="sxs-lookup"><span data-stu-id="9f7e7-162">Item exists in both GPOs, but with changed settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="9f7e7-163">Blaue</span><span class="sxs-lookup"><span data-stu-id="9f7e7-163">Blue</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="9f7e7-164">[-]</span><span class="sxs-lookup"><span data-stu-id="9f7e7-164">[-]</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="9f7e7-165">Element ist nur im ersten GPO vorhanden</span><span class="sxs-lookup"><span data-stu-id="9f7e7-165">Item exists only in the first GPO</span></span></p></td>
<td align="left"><p><span data-ttu-id="9f7e7-166">Rot</span><span class="sxs-lookup"><span data-stu-id="9f7e7-166">Red</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="9f7e7-167">[+]</span><span class="sxs-lookup"><span data-stu-id="9f7e7-167">[+]</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="9f7e7-168">Element ist nur im zweiten GPO vorhanden</span><span class="sxs-lookup"><span data-stu-id="9f7e7-168">Item exists only in the second GPO</span></span></p></td>
<td align="left"><p><span data-ttu-id="9f7e7-169">Grün</span><span class="sxs-lookup"><span data-stu-id="9f7e7-169">Green</span></span></p></td>
</tr>
</tbody>
</table>

 

-   <span data-ttu-id="9f7e7-170">Bei Elementen mit geänderten Einstellungen werden die geänderten Einstellungen identifiziert, wenn das Element erweitert wird.</span><span class="sxs-lookup"><span data-stu-id="9f7e7-170">For items with changed settings, the changed settings are identified when the item is expanded.</span></span> <span data-ttu-id="9f7e7-171">Der Wert für das Attribut in den einzelnen Gruppenrichtlinienobjekten wird in der Reihenfolge angezeigt, in der die GPOs im Bericht angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="9f7e7-171">The value for the attribute in each GPO is displayed in the same order that the GPOs are displayed in the report.</span></span>

-   <span data-ttu-id="9f7e7-172">Einige Änderungen an Einstellungen können dazu führen, dass ein Element als zwei unterschiedliche Elemente gemeldet wird (eines ist nur im ersten GPO vorhanden, das nur in der zweiten vorhanden ist), und nicht als ein Element, das sich geändert hat.</span><span class="sxs-lookup"><span data-stu-id="9f7e7-172">Some changes to settings may cause an item to be reported as two different items (one present only in the first GPO, one present only in the second), rather than as one item that has changed.</span></span>

### <span data-ttu-id="9f7e7-173">Weitere Verweise</span><span class="sxs-lookup"><span data-stu-id="9f7e7-173">Additional references</span></span>

-   [<span data-ttu-id="9f7e7-174">Registerkarte "Inhalt"</span><span class="sxs-lookup"><span data-stu-id="9f7e7-174">Contents Tab</span></span>](contents-tab.md)

 

 





