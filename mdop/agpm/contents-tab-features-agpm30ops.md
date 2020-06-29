---
title: Features der Registerkarte „Inhalt“
description: Features der Registerkarte „Inhalt“
author: dansimp
ms.assetid: 725f025a-c30a-4d07-add1-4e0ed9a1a5fd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f64aad16a3335d78641812121692f6d5f6436ee1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807695"
---
# <span data-ttu-id="c6839-103">Features der Registerkarte „Inhalt“</span><span class="sxs-lookup"><span data-stu-id="c6839-103">Contents Tab Features</span></span>


<span data-ttu-id="c6839-104">Jede sekundäre Registerkarte auf der Registerkarte **Inhalt** enthält zwei Abschnitte:**Gruppenrichtlinienobjekte** und **Gruppen und Benutzer**.</span><span class="sxs-lookup"><span data-stu-id="c6839-104">Each secondary tab within the **Contents** tab has two sections—**Group Policy objects** and **Groups and Users**.</span></span>

## <span data-ttu-id="c6839-105">Abschnitt "Gruppenrichtlinienobjekte"</span><span class="sxs-lookup"><span data-stu-id="c6839-105">Group Policy objects section</span></span>


<span data-ttu-id="c6839-106">Im Abschnitt **Gruppenrichtlinienobjekte** wird eine gefilterte Liste der Gruppenrichtlinienobjekte (Group Policy Objects, GPOs) angezeigt, und es werden die folgenden Attribute für jedes GPO identifiziert:</span><span class="sxs-lookup"><span data-stu-id="c6839-106">The **Group Policy objects** section displays a filtered list of Group Policy Objects (GPOs) and identifies the following attributes for each GPO:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c6839-107">GPO-Attribut</span><span class="sxs-lookup"><span data-stu-id="c6839-107">GPO attribute</span></span></th>
<th align="left"><span data-ttu-id="c6839-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c6839-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="c6839-109">Name</span><span class="sxs-lookup"><span data-stu-id="c6839-109">Name</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="c6839-110">Der Name des Gruppenrichtlinienobjekts.</span><span class="sxs-lookup"><span data-stu-id="c6839-110">Name of the GPO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="c6839-111">Status</span><span class="sxs-lookup"><span data-stu-id="c6839-111">State</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="c6839-112">Der Status des ausgewählten Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="c6839-112">The state of the selected GPO</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="c6839-113">Geändert von</span><span class="sxs-lookup"><span data-stu-id="c6839-113">Changed By</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="c6839-114">Der Herausgeber, der eingecheckt hat, oder die genehmigende Person, die das ausgewählte Gruppenrichtlinienobjekt bereitgestellt hat.</span><span class="sxs-lookup"><span data-stu-id="c6839-114">The Editor who checked in or the Approver who deployed the selected GPO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="c6839-115">Datum ändern</span><span class="sxs-lookup"><span data-stu-id="c6839-115">Change Date</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="c6839-116">Bei einem kontrollierten GPO das letzte Datum, an dem es eingecheckt wurde, nachdem es geändert oder ausgecheckt wurde, um geändert zu werden.</span><span class="sxs-lookup"><span data-stu-id="c6839-116">For a controlled GPO, the most recent date it was checked in after being modified or checked out to be modified.</span></span> <span data-ttu-id="c6839-117">Bei einem nicht kontrollierten Gruppenrichtlinienobjekt das Datum, an dem es zuletzt geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="c6839-117">For an uncontrolled GPO, the date when it was last modified.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="c6839-118">Kommentar</span><span class="sxs-lookup"><span data-stu-id="c6839-118">Comment</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="c6839-119">Ein Kommentar, der von der Person eingegeben wurde, die zu dem Zeitpunkt, zu dem Sie geändert wurde, ein GPO eingecheckt oder bereitgestellt hat.</span><span class="sxs-lookup"><span data-stu-id="c6839-119">A comment entered by the person who checked in or deployed a GPO at the time that it was modified.</span></span> <span data-ttu-id="c6839-120">Nützlich, um die Besonderheiten der Version zu identifizieren, falls ein Rollback auf eine vorherige Version erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="c6839-120">Useful for identifying the specifics of the version in case of the need to roll back to a previous version.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="c6839-121">Computer Version</span><span class="sxs-lookup"><span data-stu-id="c6839-121">Computer Version</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="c6839-122">Automatisch generierte Version des Computer Konfigurations Teils des Gruppenrichtlinienobjekts.</span><span class="sxs-lookup"><span data-stu-id="c6839-122">Automatically generated version of the Computer Configuration portion of the GPO.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="c6839-123">Benutzer Version</span><span class="sxs-lookup"><span data-stu-id="c6839-123">User Version</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="c6839-124">Automatisch generierte Version des Benutzer Konfigurations Teils des Gruppenrichtlinienobjekts.</span><span class="sxs-lookup"><span data-stu-id="c6839-124">Automatically generated version of the User Configuration portion of the GPO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="c6839-125">GPO-Status</span><span class="sxs-lookup"><span data-stu-id="c6839-125">GPO Status</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="c6839-126">Die Computer Konfiguration und die Benutzerkonfiguration können separat verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="c6839-126">The Computer Configuration and the User Configuration can be managed separately.</span></span> <span data-ttu-id="c6839-127">Der Status des Gruppenrichtlinienobjekts gibt an, welche Teile des Gruppenrichtlinienobjekts aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="c6839-127">The GPO Status indicates which portions of the GPO are enabled.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="c6839-128">WMI-Filter</span><span class="sxs-lookup"><span data-stu-id="c6839-128">WMI Filter</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="c6839-129">Zeigen Sie alle WMI-Filter an, die auf dieses Gruppenrichtlinienobjekt angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="c6839-129">Display any WMI filters that are applied to this GPO.</span></span> <span data-ttu-id="c6839-130">WMI-Filter werden in der <strong> </strong> Konsolenstruktur der GPMC unter dem Ordner WMI-Filter für die Domäne verwaltet.</span><span class="sxs-lookup"><span data-stu-id="c6839-130">WMI filters are managed under the <strong>WMI Filters</strong> folder for the domain in the console tree of the GPMC.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="c6839-131">Abschnitt "Gruppen und Benutzer"</span><span class="sxs-lookup"><span data-stu-id="c6839-131">Groups and Users section</span></span>


<span data-ttu-id="c6839-132">Wenn ein GPO ausgewählt ist, wird im Abschnitt **Gruppen und Benutzer** eine Liste der Gruppen und Benutzer angezeigt, die Zugriff auf das Gruppenrichtlinienobjekt haben.</span><span class="sxs-lookup"><span data-stu-id="c6839-132">When a GPO is selected, the **Groups and Users** section displays a list of the groups and users with access to that GPO.</span></span> <span data-ttu-id="c6839-133">Die zulässigen Berechtigungen und die Vererbung werden für jede Gruppe oder jeden Benutzer angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c6839-133">The allowed permissions and inheritance are displayed for each group or user.</span></span> <span data-ttu-id="c6839-134">Ein AGPM-Administrator kann Berechtigungen entweder mithilfe von standardmäßigen AGPM-Rollen (Editor, genehmigende Person, Bearbeiter und AGPM-Administrator) oder einer benutzerdefinierten Kombination von Berechtigungen konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="c6839-134">An AGPM Administrator can configure permissions using either standard AGPM roles (Editor, Approver, Reviewer, and AGPM Administrator) or a customized combination of permissions.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c6839-135">Button</span><span class="sxs-lookup"><span data-stu-id="c6839-135">Button</span></span></th>
<th align="left"><span data-ttu-id="c6839-136">Effekt</span><span class="sxs-lookup"><span data-stu-id="c6839-136">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="c6839-137">Add</span><span class="sxs-lookup"><span data-stu-id="c6839-137">Add</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="c6839-138">Fügen Sie der Sicherheitsbeschreibung einen neuen Eintrag hinzu.</span><span class="sxs-lookup"><span data-stu-id="c6839-138">Add a new entry to the security descriptor.</span></span> <span data-ttu-id="c6839-139">Alle Benutzer oder Gruppen in Active Directory können hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="c6839-139">Any user or group in Active Directory can be added.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="c6839-140">Entfernen</span><span class="sxs-lookup"><span data-stu-id="c6839-140">Remove</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="c6839-141">Entfernen des ausgewählten Eintrags aus der Zugriffssteuerungsliste</span><span class="sxs-lookup"><span data-stu-id="c6839-141">Remove the selected entry from the Access Control List.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="c6839-142">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c6839-142">Properties</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="c6839-143">Anzeigen der Eigenschaften für das ausgewählte Objekt</span><span class="sxs-lookup"><span data-stu-id="c6839-143">Display the properties for the selected object.</span></span> <span data-ttu-id="c6839-144">Die Seite "Eigenschaften" wird für ein Objekt in <strong> Active Directory-Benutzer und-Computer angezeigt </strong> .</span><span class="sxs-lookup"><span data-stu-id="c6839-144">The properties page is the same one displayed for an object in <strong>Active Directory Users and Computers</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="c6839-145">Erweitert</span><span class="sxs-lookup"><span data-stu-id="c6839-145">Advanced</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="c6839-146">Öffnen Sie den Editor für die <strong> Zugriffssteuerungsliste </strong> .</span><span class="sxs-lookup"><span data-stu-id="c6839-146">Open the <strong>Access Control List Editor</strong>.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="c6839-147">Weitere Überlegungen</span><span class="sxs-lookup"><span data-stu-id="c6839-147">Additional considerations</span></span>

-   <span data-ttu-id="c6839-148">Informationen zu Rollen und Berechtigungen, die sich auf bestimmte Aufgaben beziehen, finden Sie unter Ausführen von Aufgaben im Rahmen von [AGPM-Administratoren](performing-agpm-administrator-tasks-agpm30ops.md), Ausführen von [Editor Aufgaben](performing-editor-tasks-agpm30ops.md), Ausführen von [genehmigenden Aufgaben](performing-approver-tasks-agpm30ops.md)und [Ausführen von Aufgaben](performing-reviewer-tasks-agpm30ops.md)für Bearbeiter.</span><span class="sxs-lookup"><span data-stu-id="c6839-148">For information about roles and permissions related to specific tasks, see the tasks under [Performing AGPM Administrator Tasks](performing-agpm-administrator-tasks-agpm30ops.md), [Performing Editor Tasks](performing-editor-tasks-agpm30ops.md), [Performing Approver Tasks](performing-approver-tasks-agpm30ops.md), and [Performing Reviewer Tasks](performing-reviewer-tasks-agpm30ops.md).</span></span>

### <span data-ttu-id="c6839-149">Weitere Verweise</span><span class="sxs-lookup"><span data-stu-id="c6839-149">Additional references</span></span>

-   [<span data-ttu-id="c6839-150">Registerkarte "Inhalt"</span><span class="sxs-lookup"><span data-stu-id="c6839-150">Contents Tab</span></span>](contents-tab-agpm30ops.md)

 

 





