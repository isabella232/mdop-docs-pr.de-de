---
title: Allgemeine sekundäre Registerkarten-Features
description: Allgemeine sekundäre Registerkarten-Features
author: dansimp
ms.assetid: 44a15c28-944c-49c1-8534-115ce1c362ed
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 546fd4c91e060a5595b6c848015290882de933b6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807767"
---
# <span data-ttu-id="ef110-103">Allgemeine sekundäre Registerkarten-Features</span><span class="sxs-lookup"><span data-stu-id="ef110-103">Common Secondary Tab Features</span></span>


<span data-ttu-id="ef110-104">Jede sekundäre Registerkarte hat zwei Abschnitte:**Gruppenrichtlinienobjekte** und **Gruppen und Benutzer**.</span><span class="sxs-lookup"><span data-stu-id="ef110-104">Each secondary tab has two sections—**Group Policy objects** and **Groups and Users**.</span></span>

## <span data-ttu-id="ef110-105">Abschnitt "Gruppenrichtlinienobjekte"</span><span class="sxs-lookup"><span data-stu-id="ef110-105">Group Policy objects section</span></span>


<span data-ttu-id="ef110-106">Im Abschnitt **Gruppenrichtlinienobjekte** wird eine gefilterte Liste der Gruppenrichtlinienobjekte (Group Policy Objects, GPOs) angezeigt, und es werden die folgenden Merkmale für jedes GPO identifiziert:</span><span class="sxs-lookup"><span data-stu-id="ef110-106">The **Group Policy objects** section displays a filtered list of Group Policy objects (GPOs) and identifies the following characteristics for each GPO:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ef110-107">GPO-Merkmal</span><span class="sxs-lookup"><span data-stu-id="ef110-107">GPO Characteristic</span></span></th>
<th align="left"><span data-ttu-id="ef110-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ef110-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="ef110-109">Name</span><span class="sxs-lookup"><span data-stu-id="ef110-109">Name</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="ef110-110">Der Name des Gruppenrichtlinienobjekts.</span><span class="sxs-lookup"><span data-stu-id="ef110-110">Name of the Group Policy object.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="ef110-111">Computer (Comp.)</span><span class="sxs-lookup"><span data-stu-id="ef110-111">Computer (Comp.)</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="ef110-112">Automatisch generierte Version des Computer Konfigurations Teils des Gruppenrichtlinienobjekts.</span><span class="sxs-lookup"><span data-stu-id="ef110-112">Automatically generated version of the Computer Configuration portion of the GPO.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="ef110-113">Benutzer</span><span class="sxs-lookup"><span data-stu-id="ef110-113">User</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="ef110-114">Automatisch generierte Version des Benutzer Konfigurations Teils des Gruppenrichtlinienobjekts.</span><span class="sxs-lookup"><span data-stu-id="ef110-114">Automatically generated version of the User Configuration portion of the GPO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="ef110-115">Status</span><span class="sxs-lookup"><span data-stu-id="ef110-115">State</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="ef110-116">Der Status des ausgewählten Gruppenrichtlinienobjekts:</span><span class="sxs-lookup"><span data-stu-id="ef110-116">The state of the selected GPO:</span></span></p>
<p><img src="images/36f6b687-f5cc-40d1-805f-b191d1fb1ace.gif" alt="Deployed GPO icon" /> <strong><span data-ttu-id="ef110-117">Unkontrolliert: </strong> nicht von AGPM verwaltet.</span><span class="sxs-lookup"><span data-stu-id="ef110-117">Uncontrolled:</strong> Not managed by AGPM.</span></span></p>
<p><img src="images/57b610a5-1c71-4d26-9173-d04abd495fcc.gif" alt="Checked in GPO icon" /> <strong><span data-ttu-id="ef110-118">Eingecheckt: </strong> verfügbar für autorisierte Editoren zum Auschecken zur Bearbeitung oder zum Bereitstellen eines Gruppenrichtlinienadministrators.</span><span class="sxs-lookup"><span data-stu-id="ef110-118">Checked In:</strong> Available for authorized Editors to check out for editing or for a Group Policy administrator to deploy.</span></span></p>
<p><img src="images/8e7a7c4e-809a-435a-8b29-30d797936210.gif" alt="Checked out GPO icon" /> <strong><span data-ttu-id="ef110-119">Ausgecheckt: </strong> derzeit bearbeitet.</span><span class="sxs-lookup"><span data-stu-id="ef110-119">Checked Out:</strong> Currently being edited.</span></span> <span data-ttu-id="ef110-120">Für andere Bearbeiter nicht verfügbar, bis der Herausgeber ausgecheckt hat oder ein AGPM-Administrator ihn überprüft hat.</span><span class="sxs-lookup"><span data-stu-id="ef110-120">Unavailable for other Editors to check out until the Editor who checked it out or an AGPM Administrator checks it in.</span></span></p>
<p><img src="images/0840a6a3-54a6-4528-98a9-7b122243c1a5.gif" alt="Pending GPO icon" /> <strong><span data-ttu-id="ef110-121">Ausstehend: </strong> wartet auf die Genehmigung eines Gruppenrichtlinienadministrators, bevor er erstellt, gesteuert, bereitgestellt oder gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="ef110-121">Pending:</strong> Awaiting approval from a Group Policy administrator before being created, controlled, deployed, or deleted.</span></span></p>
<p><img src="images/57b610a5-1c71-4d26-9173-d04abd495fcc.gif" alt="Checked in GPO icon" /> <strong><span data-ttu-id="ef110-122">Gelöscht: </strong> aus dem Archiv gelöscht, aber weiterhin in der Lage, wiederhergestellt zu werden.</span><span class="sxs-lookup"><span data-stu-id="ef110-122">Deleted:</strong> Deleted from the archive, but still able to be restored.</span></span></p>
<p><img src="images/9b65829d-253c-4f30-9295-c816a6521ed2.gif" alt="Template icon" /> <strong><span data-ttu-id="ef110-123">Vorlage: </strong> eine statische Version eines GPO zur Verwendung als Ausgangspunkt beim Erstellen neuer GPOs.</span><span class="sxs-lookup"><span data-stu-id="ef110-123">Template:</strong> A static version of a GPO for use as a starting point when creating new GPOs.</span></span></p>
<p><img src="images/cd349b8d-c4d8-45ff-b17f-7db882502c58.gif" alt="Default template icon" /> <strong><span data-ttu-id="ef110-124">Vorlage (Standard): </strong> Diese Vorlage ist standardmäßig der Ausgangspunkt, der beim Erstellen eines neuen Gruppenrichtlinienobjekts verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ef110-124">Template (default):</strong> By default, this template is the starting point used when creating a new GPO.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="ef110-125">GPO-Status</span><span class="sxs-lookup"><span data-stu-id="ef110-125">GPO Status</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="ef110-126">Die Computer Konfiguration und die Benutzerkonfiguration können separat verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="ef110-126">The Computer Configuration and the User Configuration can be managed separately.</span></span> <span data-ttu-id="ef110-127">Der Status des Gruppenrichtlinienobjekts gibt an, welche Teile des Gruppenrichtlinienobjekts aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="ef110-127">The GPO Status indicates which portions of the GPO are enabled.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="ef110-128">WMI-Filter</span><span class="sxs-lookup"><span data-stu-id="ef110-128">WMI Filter</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="ef110-129">Zeigen Sie alle WMI-Filter an, die auf dieses Gruppenrichtlinienobjekt angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="ef110-129">Display any WMI filters that are applied to this GPO.</span></span> <span data-ttu-id="ef110-130">WMI-Filter werden unter dem <strong> WMI </strong> -Filterknoten für die Domäne in der Konsolenstruktur der GPMC verwaltet.</span><span class="sxs-lookup"><span data-stu-id="ef110-130">WMI filters are managed under the <strong>WMI Filters</strong> node for the domain in the console tree of the GPMC.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="ef110-131">Geändert</span><span class="sxs-lookup"><span data-stu-id="ef110-131">Modified</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="ef110-132">Bei einem kontrollierten Gruppenrichtlinienobjekt das letzte Datum, an dem es eingecheckt wurde, nachdem es geändert oder ausgecheckt wurde.</span><span class="sxs-lookup"><span data-stu-id="ef110-132">For a controlled GPO, the most recent date when it was checked in after being modified or checked out to be modified.</span></span> <span data-ttu-id="ef110-133">Bei einem nicht kontrollierten Gruppenrichtlinienobjekt das Datum, an dem es zuletzt geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="ef110-133">For an uncontrolled GPO, the date when it was last modified.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="ef110-134">Besitzer</span><span class="sxs-lookup"><span data-stu-id="ef110-134">Owner</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="ef110-135">Der Herausgeber, der eingecheckt hat, oder die genehmigende Person, die das ausgewählte Gruppenrichtlinienobjekt bereitgestellt hat.</span><span class="sxs-lookup"><span data-stu-id="ef110-135">The Editor who checked in or the Approver who deployed the selected GPO.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="ef110-136">Abschnitt "Gruppen und Benutzer"</span><span class="sxs-lookup"><span data-stu-id="ef110-136">Groups and Users section</span></span>


<span data-ttu-id="ef110-137">Wenn ein GPO ausgewählt ist, wird im Abschnitt **Gruppen und Benutzer** eine Liste der Gruppen und Benutzer angezeigt, die Zugriff auf das Gruppenrichtlinienobjekt haben.</span><span class="sxs-lookup"><span data-stu-id="ef110-137">When a GPO is selected, the **Groups and Users** section displays a list of the groups and users with access to that GPO.</span></span> <span data-ttu-id="ef110-138">Die zulässigen Berechtigungen und die Vererbung werden für jede Gruppe oder jeden Benutzer angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ef110-138">The allowed permissions and inheritance are displayed for each group or user.</span></span> <span data-ttu-id="ef110-139">Ein AGPM-Administrator kann Berechtigungen entweder mithilfe von standardmäßigen AGPM-Rollen (Editor, genehmigende Person und Bearbeiter) oder einer benutzerdefinierten Kombination von Berechtigungen konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="ef110-139">An AGPM Administrator can configure permissions using either standard AGPM roles (Editor, Approver, and Reviewer) or a customized combination of permissions.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ef110-140">Button</span><span class="sxs-lookup"><span data-stu-id="ef110-140">Button</span></span></th>
<th align="left"><span data-ttu-id="ef110-141">Effekt</span><span class="sxs-lookup"><span data-stu-id="ef110-141">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="ef110-142">Add</span><span class="sxs-lookup"><span data-stu-id="ef110-142">Add</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="ef110-143">Fügen Sie der Sicherheitsbeschreibung einen neuen Eintrag hinzu.</span><span class="sxs-lookup"><span data-stu-id="ef110-143">Add a new entry to the security descriptor.</span></span> <span data-ttu-id="ef110-144">Alle Benutzer oder Gruppen in Active Directory können hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="ef110-144">Any user or group in Active Directory can be added.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="ef110-145">Entfernen</span><span class="sxs-lookup"><span data-stu-id="ef110-145">Remove</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="ef110-146">Entfernen des ausgewählten Eintrags aus der Zugriffssteuerungsliste</span><span class="sxs-lookup"><span data-stu-id="ef110-146">Remove the selected entry from the Access Control List.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="ef110-147">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ef110-147">Properties</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="ef110-148">Anzeigen der Eigenschaften für das ausgewählte Objekt</span><span class="sxs-lookup"><span data-stu-id="ef110-148">Display the properties for the selected object.</span></span> <span data-ttu-id="ef110-149">Die Seite "Eigenschaften" wird für ein Objekt in <strong> Active Directory-Benutzer und-Computer angezeigt </strong> .</span><span class="sxs-lookup"><span data-stu-id="ef110-149">The properties page is the same one displayed for an object in <strong>Active Directory Users and Computers</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="ef110-150">Erweitert</span><span class="sxs-lookup"><span data-stu-id="ef110-150">Advanced</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="ef110-151">Öffnen Sie den Editor für die <strong> Zugriffssteuerungsliste </strong> .</span><span class="sxs-lookup"><span data-stu-id="ef110-151">Open the <strong>Access Control List Editor</strong>.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="ef110-152">Weitere Überlegungen</span><span class="sxs-lookup"><span data-stu-id="ef110-152">Additional considerations</span></span>

-   <span data-ttu-id="ef110-153">Informationen zu Rollen und Berechtigungen, die sich auf bestimmte Aufgaben beziehen, finden Sie unter Ausführen von Aufgaben im Rahmen von [AGPM-Administratoren](performing-agpm-administrator-tasks.md), Ausführen von [Editor Aufgaben](performing-editor-tasks.md), Ausführen von [genehmigenden Aufgaben](performing-approver-tasks.md)und [Ausführen von Aufgaben](performing-reviewer-tasks.md)für Bearbeiter.</span><span class="sxs-lookup"><span data-stu-id="ef110-153">For information about roles and permissions related to specific tasks, see the tasks under [Performing AGPM Administrator Tasks](performing-agpm-administrator-tasks.md), [Performing Editor Tasks](performing-editor-tasks.md), [Performing Approver Tasks](performing-approver-tasks.md), and [Performing Reviewer Tasks](performing-reviewer-tasks.md).</span></span>

### <span data-ttu-id="ef110-154">Weitere Verweise</span><span class="sxs-lookup"><span data-stu-id="ef110-154">Additional references</span></span>

-   [<span data-ttu-id="ef110-155">Registerkarte "Inhalt"</span><span class="sxs-lookup"><span data-stu-id="ef110-155">Contents Tab</span></span>](contents-tab.md)

 

 





