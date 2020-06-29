---
title: Verlaufsfenster
description: Verlaufsfenster
author: dansimp
ms.assetid: 5bea62e7-d267-40b2-a66d-fb1be7373a1c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 81f19e3834e945a45238856e23f6ee4a86407c4a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808448"
---
# <span data-ttu-id="442c0-103">Verlaufsfenster</span><span class="sxs-lookup"><span data-stu-id="442c0-103">History Window</span></span>


<span data-ttu-id="442c0-104">Der Verlauf eines Gruppenrichtlinienobjekts (GPO) kann angezeigt werden, indem Sie auf ein GPO doppelklicken oder mit der rechten Maustaste auf ein GPO und dann auf **Verlauf**klicken.</span><span class="sxs-lookup"><span data-stu-id="442c0-104">The history of a Group Policy Object (GPO) can be displayed by double-clicking a GPO or by right-clicking a GPO and then clicking **History**.</span></span> <span data-ttu-id="442c0-105">Darüber hinaus wird es in der Gruppenrichtlinien-Verwaltungskonsole (Group Policy Management Console, GPMC) als Registerkarte für jedes GPO angezeigt.</span><span class="sxs-lookup"><span data-stu-id="442c0-105">It is also displayed in the Group Policy Management Console (GPMC) as a tab for each GPO.</span></span>

<span data-ttu-id="442c0-106">Das Protokoll enthält eine Aufzeichnung der Ereignisse in der Lebensdauer des ausgewählten Gruppenrichtlinienobjekts.</span><span class="sxs-lookup"><span data-stu-id="442c0-106">The history provides a record of events in the lifetime of the selected GPO.</span></span> <span data-ttu-id="442c0-107">Im Fenster " **Verlauf** " können Sie einen Bericht über die Einstellungen in einer Version des Gruppenrichtlinienobjekts abrufen, mehrere Versionen eines GPO vergleichen oder auf eine frühere Version eines GPO zurückgreifen.</span><span class="sxs-lookup"><span data-stu-id="442c0-107">From the **History** window, you can obtain a report of the settings in a version of the GPO, compare multiple versions of a GPO, or roll back to an earlier version of a GPO.</span></span>

## <span data-ttu-id="442c0-108">Filtern von Ereignissen im Verlaufsfenster</span><span class="sxs-lookup"><span data-stu-id="442c0-108">Filtering events in the History window</span></span>


<span data-ttu-id="442c0-109">Die Registerkarten im **Verlaufs** Fenster filtern die Zustände im Verlauf des Gruppenrichtlinienobjekts.</span><span class="sxs-lookup"><span data-stu-id="442c0-109">The tabs within the **History** window filter the states in the history of the GPO.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="442c0-110">Tabs</span><span class="sxs-lookup"><span data-stu-id="442c0-110">Tabs</span></span></th>
<th align="left"><span data-ttu-id="442c0-111">Filterung</span><span class="sxs-lookup"><span data-stu-id="442c0-111">Filtering</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="442c0-112">Alle Zustände</span><span class="sxs-lookup"><span data-stu-id="442c0-112">All States</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="442c0-113">Zeigt alle Zustände im Verlauf des Gruppenrichtlinienobjekts an.</span><span class="sxs-lookup"><span data-stu-id="442c0-113">Display all states in the history of the GPO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="442c0-114">Eindeutige Versionen</span><span class="sxs-lookup"><span data-stu-id="442c0-114">Unique Versions</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="442c0-115">Zeigt nur eindeutige Versionen des in das Archiv eingecheckten Gruppenrichtlinienobjekts an.</span><span class="sxs-lookup"><span data-stu-id="442c0-115">Display only unique versions of the GPO checked into the archive.</span></span> <span data-ttu-id="442c0-116">Die Version, die in der Produktionsumgebung bereitgestellt wird, Verknüpfungen zu eindeutigen Versionen und Informationsstatus werden in dieser Liste ausgelassen.</span><span class="sxs-lookup"><span data-stu-id="442c0-116">The version deployed to the production environment, shortcuts to unique versions, and informational states are omitted from this list.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="442c0-117">Ereignisinformationen</span><span class="sxs-lookup"><span data-stu-id="442c0-117">Event information</span></span>


<span data-ttu-id="442c0-118">Informationen werden für jeden Zustand im Verlauf des Gruppenrichtlinienobjekts bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="442c0-118">Information is provided for each state in the history of the GPO.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="442c0-119">GPO-Attribut</span><span class="sxs-lookup"><span data-stu-id="442c0-119">GPO attribute</span></span></th>
<th align="left"><span data-ttu-id="442c0-120">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="442c0-120">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="442c0-121">Datum ändern</span><span class="sxs-lookup"><span data-stu-id="442c0-121">Change Date</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="442c0-122">Der Zeitstempel des Vorgangs, in dem die Aktion in der <strong> Spalte "Zustand" </strong> ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="442c0-122">Time stamp of when the action in the <strong>State</strong> column was performed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="442c0-123">Status</span><span class="sxs-lookup"><span data-stu-id="442c0-123">State</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="442c0-124">Ein Zustand im Verlauf des Gruppenrichtlinienobjekts.</span><span class="sxs-lookup"><span data-stu-id="442c0-124">A state in the history of the GPO.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="442c0-125">Geändert von</span><span class="sxs-lookup"><span data-stu-id="442c0-125">Changed By</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="442c0-126">Die Person, die das Gruppenrichtlinienobjekt eingecheckt oder bereitgestellt hat.</span><span class="sxs-lookup"><span data-stu-id="442c0-126">The person who checked in or deployed the GPO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="442c0-127">Kommentar</span><span class="sxs-lookup"><span data-stu-id="442c0-127">Comment</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="442c0-128">Ein Kommentar, der von der Person eingegeben wurde, die zu dem Zeitpunkt, zu dem diese Version geändert wurde, ein GPO eingecheckt oder bereitgestellt hat, um die Besonderheiten der Version zu identifizieren, wenn ein Rollback auf eine frühere Version erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="442c0-128">A comment entered by the person who checked in or deployed a GPO at the time that this version was changed, useful for identifying the specifics of the version in case of the need to roll back to an earlier version.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="442c0-129">Löschbar</span><span class="sxs-lookup"><span data-stu-id="442c0-129">Deletable</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="442c0-130">Ob diese Version des Gruppenrichtlinienobjekts gelöscht werden kann, wenn die Anzahl der eindeutigen Versionen jedes im Archiv aufbewahrten Gruppenrichtlinienobjekts limitiert ist.</span><span class="sxs-lookup"><span data-stu-id="442c0-130">Whether this version of the GPO can be deleted if the number of unique versions of each GPO retained in the archive is limited.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="442c0-131">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="442c0-131">Note</span></span></strong><br/><p><span data-ttu-id="442c0-132">Sie können ändern, ob eine Version eines GPO gelöscht werden kann, indem Sie mit der rechten Maustaste auf das Gruppenrichtlinienobjekt klicken und dann auf " <strong> Löschen" </strong> oder "Löschen zulassen" klicken <strong> </strong> .</span><span class="sxs-lookup"><span data-stu-id="442c0-132">You can change whether a version of a GPO can be deleted by right-clicking the GPO and then clicking <strong>Do Not Allow Deletion</strong> or <strong>Allow Deletion</strong>.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="442c0-133">Computer Version</span><span class="sxs-lookup"><span data-stu-id="442c0-133">Computer Version</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="442c0-134">Automatisch generierte Version des Computer Konfigurations Teils des Gruppenrichtlinienobjekts.</span><span class="sxs-lookup"><span data-stu-id="442c0-134">Automatically generated version of the Computer Configuration part of the GPO.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="442c0-135">Benutzer Version</span><span class="sxs-lookup"><span data-stu-id="442c0-135">User Version</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="442c0-136">Automatisch generierte Version des Benutzer Konfigurations Teils des Gruppenrichtlinienobjekts.</span><span class="sxs-lookup"><span data-stu-id="442c0-136">Automatically generated version of the User Configuration part of the GPO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="442c0-137">GPO-Status</span><span class="sxs-lookup"><span data-stu-id="442c0-137">GPO Status</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="442c0-138">Die Computer Konfiguration und die Benutzerkonfiguration können separat verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="442c0-138">The Computer Configuration and the User Configuration can be managed separately from each other.</span></span> <span data-ttu-id="442c0-139">Dieser Status zeigt an, welche Teile des Gruppenrichtlinienobjekts aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="442c0-139">This status shows which portions of the GPO are enabled.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="442c0-140">Quell-GPO-Informationen</span><span class="sxs-lookup"><span data-stu-id="442c0-140">Source GPO Information</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="442c0-141">Für ein Gruppenrichtlinienobjekt, das aus einer anderen Gesamtstruktur importiert wurde, den ursprünglichen Namen, die Domäne sowie den Benutzer und das Datum, die der letzten Änderung zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="442c0-141">For a GPO that has been imported from another forest, the original GPO name, domain, and user and date associated with the last change.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="442c0-142">Berichte</span><span class="sxs-lookup"><span data-stu-id="442c0-142">Reports</span></span>


<span data-ttu-id="442c0-143">Auf den Schaltflächen **Einstellungen** und **Unterschiede** werden Berichte zu den GPO-Einstellungen für die ausgewählte GPO-Version oder Versionen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="442c0-143">The **Settings** and **Differences** buttons display reports about GPO settings for the GPO version or versions selected.</span></span> <span data-ttu-id="442c0-144">Darüber hinaus bietet das Klicken mit der rechten Maustaste auf eine GPO-Version oder-Version die Möglichkeit, XML-basierte Berichte anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="442c0-144">Also, right-clicking a GPO version or versions provides the option to display XML-based reports.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="442c0-145">Button</span><span class="sxs-lookup"><span data-stu-id="442c0-145">Button</span></span></th>
<th align="left"><span data-ttu-id="442c0-146">Effekt</span><span class="sxs-lookup"><span data-stu-id="442c0-146">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="442c0-147">Einstellungen</span><span class="sxs-lookup"><span data-stu-id="442c0-147">Settings</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="442c0-148">Einen HTML-basierten Bericht generieren, in dem die Einstellungen in der ausgewählten Version des Gruppenrichtlinienobjekts angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="442c0-148">Generate an HTML-based report displaying the settings within the selected version of the GPO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="442c0-149">Unterschiede</span><span class="sxs-lookup"><span data-stu-id="442c0-149">Differences</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="442c0-150">Generieren eines HTML-basierten Berichts, der die Einstellungen in mehreren ausgewählten Versionen des Gruppenrichtlinienobjekts vergleicht.</span><span class="sxs-lookup"><span data-stu-id="442c0-150">Generate an HTML-based report comparing the settings within multiple selected versions of the GPO.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="442c0-151">Schlüssel für Unterschiedsberichte</span><span class="sxs-lookup"><span data-stu-id="442c0-151">Key to difference reports</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="442c0-152">Symbol</span><span class="sxs-lookup"><span data-stu-id="442c0-152">Symbol</span></span></th>
<th align="left"><span data-ttu-id="442c0-153">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="442c0-153">Meaning</span></span></th>
<th align="left"><span data-ttu-id="442c0-154">Farbe</span><span class="sxs-lookup"><span data-stu-id="442c0-154">Color</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="442c0-155">Keine</span><span class="sxs-lookup"><span data-stu-id="442c0-155">None</span></span></p></td>
<td align="left"><p><span data-ttu-id="442c0-156">Element mit identischen Einstellungen in beiden GPOs vorhanden</span><span class="sxs-lookup"><span data-stu-id="442c0-156">Item exists with identical settings in both GPOs</span></span></p></td>
<td align="left"><p><span data-ttu-id="442c0-157">Variiert je nach Ebene</span><span class="sxs-lookup"><span data-stu-id="442c0-157">Varies with level</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="442c0-158">[#]</span><span class="sxs-lookup"><span data-stu-id="442c0-158">[#]</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="442c0-159">Element ist in beiden GPOs vorhanden, jedoch mit geänderten Einstellungen</span><span class="sxs-lookup"><span data-stu-id="442c0-159">Item exists in both GPOs, but with changed settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="442c0-160">Blaue</span><span class="sxs-lookup"><span data-stu-id="442c0-160">Blue</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="442c0-161">[-]</span><span class="sxs-lookup"><span data-stu-id="442c0-161">[-]</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="442c0-162">Element ist nur im ersten GPO vorhanden</span><span class="sxs-lookup"><span data-stu-id="442c0-162">Item exists only in the first GPO</span></span></p></td>
<td align="left"><p><span data-ttu-id="442c0-163">Rot</span><span class="sxs-lookup"><span data-stu-id="442c0-163">Red</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="442c0-164">[+]</span><span class="sxs-lookup"><span data-stu-id="442c0-164">[+]</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="442c0-165">Element ist nur im zweiten GPO vorhanden</span><span class="sxs-lookup"><span data-stu-id="442c0-165">Item exists only in the second GPO</span></span></p></td>
<td align="left"><p><span data-ttu-id="442c0-166">Grün</span><span class="sxs-lookup"><span data-stu-id="442c0-166">Green</span></span></p></td>
</tr>
</tbody>
</table>



-   <span data-ttu-id="442c0-167">Bei Elementen mit geänderten Einstellungen werden die geänderten Einstellungen identifiziert, wenn das Element erweitert wird.</span><span class="sxs-lookup"><span data-stu-id="442c0-167">For items with changed settings, the changed settings are identified when the item is expanded.</span></span> <span data-ttu-id="442c0-168">Der Wert für das Attribut in den einzelnen Gruppenrichtlinienobjekten wird in der Reihenfolge angezeigt, in der die GPOs im Bericht angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="442c0-168">The value for the attribute in each GPO is displayed in the same order that the GPOs are displayed in the report.</span></span>

-   <span data-ttu-id="442c0-169">Einige Änderungen an Einstellungen können dazu führen, dass ein Element als zwei Elemente gemeldet wird (eines ist nur im ersten GPO vorhanden, das nur in der zweiten vorhanden ist), anstatt eines Elements, das sich geändert hat.</span><span class="sxs-lookup"><span data-stu-id="442c0-169">Some changes to settings may cause an item to be reported as two items (one present only in the first GPO, one present only in the second), instead of one item that has changed.</span></span>

### <span data-ttu-id="442c0-170">Weitere Verweise</span><span class="sxs-lookup"><span data-stu-id="442c0-170">Additional references</span></span>

-   [<span data-ttu-id="442c0-171">Registerkarte "Inhalt"</span><span class="sxs-lookup"><span data-stu-id="442c0-171">Contents Tab</span></span>](contents-tab-agpm40.md)









