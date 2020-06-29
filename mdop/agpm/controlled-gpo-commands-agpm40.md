---
title: Kontrollierte GPO-Befehle
description: Kontrollierte GPO-Befehle
author: dansimp
ms.assetid: 370d3db9-4efc-4799-983d-e29ba5f32b07
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 65e9d06beb4c36762e845e452bab497a8d3da747
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808579"
---
# <span data-ttu-id="056c8-103">Kontrollierte GPO-Befehle</span><span class="sxs-lookup"><span data-stu-id="056c8-103">Controlled GPO Commands</span></span>


<span data-ttu-id="056c8-104">Die Registerkarte " **gesteuert** ":</span><span class="sxs-lookup"><span data-stu-id="056c8-104">The **Controlled** tab:</span></span>

-   <span data-ttu-id="056c8-105">Zeigt eine Liste der Gruppenrichtlinienobjekte (Group Policy Objects, GPOs) an, die von der erweiterten Gruppenrichtlinienverwaltung (AGPM) verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="056c8-105">Displays a list of Group Policy Objects (GPOs) managed by Advanced Group Policy Management (AGPM).</span></span>

-   <span data-ttu-id="056c8-106">Bietet ein Kontextmenü mit Befehlen zum Verwalten von GPOs und zum Anzeigen des Verlaufs und der Berichte für GPOs.</span><span class="sxs-lookup"><span data-stu-id="056c8-106">Provides a shortcut menu with commands for managing GPOs and for displaying the history and reports for GPOs.</span></span>

-   <span data-ttu-id="056c8-107">Zeigt eine Liste der Gruppen und Benutzer an, die über die Berechtigung zum Zugriff auf ein ausgewähltes Gruppenrichtlinienobjekt verfügen.</span><span class="sxs-lookup"><span data-stu-id="056c8-107">Displays a list of the groups and users who have permission to access a selected GPO.</span></span>

<span data-ttu-id="056c8-108">Wenn Sie mit der rechten Maustaste auf die Liste der **Gruppenrichtlinienobjekte** auf dieser Registerkarte klicken, wird ein Kontextmenü angezeigt.</span><span class="sxs-lookup"><span data-stu-id="056c8-108">Right-clicking the **Group Policy Objects** list on this tab displays a shortcut menu.</span></span> <span data-ttu-id="056c8-109">Dieses Menü enthält die jeweils folgenden Optionen.</span><span class="sxs-lookup"><span data-stu-id="056c8-109">This menu includes whichever of the following options are applicable.</span></span>

## <span data-ttu-id="056c8-110">Steuerelement und Verlauf</span><span class="sxs-lookup"><span data-stu-id="056c8-110">Control and history</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="056c8-111">Befehl</span><span class="sxs-lookup"><span data-stu-id="056c8-111">Command</span></span></th>
<th align="left"><span data-ttu-id="056c8-112">Effekt</span><span class="sxs-lookup"><span data-stu-id="056c8-112">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="056c8-113">Neues gesteuertes Gruppenrichtlinienobjekt</span><span class="sxs-lookup"><span data-stu-id="056c8-113">New Controlled GPO</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="056c8-114">Erstellen Sie ein neues GPO, in dem die Änderungssteuerung über AGPM verwaltet und in der Produktionsumgebung der Domäne bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="056c8-114">Create a new GPO with change control managed through AGPM and deploy it to the production environment of the domain.</span></span> <span data-ttu-id="056c8-115">Wenn Sie nicht über die Berechtigung zum Erstellen eines Gruppenrichtlinienobjekts verfügen, werden Sie aufgefordert, eine Anforderung zu senden.</span><span class="sxs-lookup"><span data-stu-id="056c8-115">If you do not have permission to create a GPO, you are prompted to submit a request.</span></span> <span data-ttu-id="056c8-116">(Diese Option wird angezeigt, wenn beim Klicken mit der rechten Maustaste auf die <strong> Liste der Gruppenrichtlinienobjekte </strong> .)</span><span class="sxs-lookup"><span data-stu-id="056c8-116">(This option is displayed if no GPO is selected when right-clicking in the <strong>Group Policy Objects</strong> list.)</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="056c8-117">Verlauf</span><span class="sxs-lookup"><span data-stu-id="056c8-117">History</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="056c8-118">Öffnen Sie ein Fenster, in dem alle Versionen des ausgewählten Gruppenrichtlinienobjekts aufgelistet sind, die im Archiv gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="056c8-118">Open a window listing all versions of the selected GPO saved within the archive.</span></span> <span data-ttu-id="056c8-119">Aus dem Protokoll können Sie einen Bericht über die Einstellungen in einem Gruppenrichtlinienobjekt abrufen, zwei Versionen eines GPO vergleichen, ein GPO mit einer Vorlage vergleichen oder auf eine frühere Version eines GPO zurückgreifen.</span><span class="sxs-lookup"><span data-stu-id="056c8-119">From the history, you can obtain a report of the settings within a GPO, compare two versions of a GPO, compare a GPO to a template, or roll back to an earlier version of a GPO.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="056c8-120">Berichte</span><span class="sxs-lookup"><span data-stu-id="056c8-120">Reports</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="056c8-121">Befehl</span><span class="sxs-lookup"><span data-stu-id="056c8-121">Command</span></span></th>
<th align="left"><span data-ttu-id="056c8-122">Effekt</span><span class="sxs-lookup"><span data-stu-id="056c8-122">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="056c8-123">Einstellungen</span><span class="sxs-lookup"><span data-stu-id="056c8-123">Settings</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="056c8-124">Generieren eines HTML-basierten oder XML-basierten Berichts, in dem die Einstellungen innerhalb des ausgewählten Gruppenrichtlinienobjekts angezeigt werden, oder Anzeigen von Links zu den ausgewählten Gruppenrichtlinienobjekten aus Organisationseinheiten ab dem Zeitpunkt, zu dem die Gruppenrichtlinienobjekte zuletzt gesteuert, importiert oder eingecheckt wurden.</span><span class="sxs-lookup"><span data-stu-id="056c8-124">Generate an HTML-based or XML-based report displaying the settings within the selected GPO or display links to the selected GPO(s) from organizational units as of when the GPO(s) was most recently controlled, imported, or checked in.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="056c8-125">Unterschiede</span><span class="sxs-lookup"><span data-stu-id="056c8-125">Differences</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="056c8-126">Generieren eines HTML-basierten oder XML-basierten Berichts, der die Einstellungen in zwei ausgewählten GPOs oder innerhalb des ausgewählten GPO und einer Vorlage vergleicht.</span><span class="sxs-lookup"><span data-stu-id="056c8-126">Generate an HTML-based or XML-based report comparing the settings within two selected GPOs or within the selected GPO and a template.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="056c8-127">Bearbeitung</span><span class="sxs-lookup"><span data-stu-id="056c8-127">Editing</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="056c8-128">Befehl</span><span class="sxs-lookup"><span data-stu-id="056c8-128">Command</span></span></th>
<th align="left"><span data-ttu-id="056c8-129">Effekt</span><span class="sxs-lookup"><span data-stu-id="056c8-129">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="056c8-130">Bearbeiten</span><span class="sxs-lookup"><span data-stu-id="056c8-130">Edit</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="056c8-131">Öffnen <strong> Sie das Fenster "Gruppenrichtlinien-Verwaltungs-Editor </strong> ", um das ausgewählte Gruppenrichtlinienobjekt zu ändern.</span><span class="sxs-lookup"><span data-stu-id="056c8-131">Open the <strong>Group Policy Management Editor</strong> window to change the selected GPO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="056c8-132">Abreise</span><span class="sxs-lookup"><span data-stu-id="056c8-132">Check Out</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="056c8-133">Besorgen Sie sich eine Kopie des ausgewählten GPO aus dem Archiv für die Offlinebearbeitung, und verbieten Sie anderen Personen, das Gruppenrichtlinienobjekt zu bearbeiten, bis es wieder in das Archiv eingecheckt wurde.</span><span class="sxs-lookup"><span data-stu-id="056c8-133">Obtain a copy of the selected GPO from the archive for offline editing and prohibit anyone else from editing the GPO until it is checked back into the archive.</span></span> <span data-ttu-id="056c8-134">Das Auschecken kann von einem AGPM-Administrator (Vollzugriff) überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="056c8-134">Check Out can be overridden by an AGPM Administrator (Full Control).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="056c8-135">Ankunft</span><span class="sxs-lookup"><span data-stu-id="056c8-135">Check In</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="056c8-136">Überprüfen Sie die bearbeitete Version des ausgewählten Gruppenrichtlinienobjekts in das Archiv, damit andere autorisierte Bearbeiter Änderungen vornehmen können, oder eine genehmigende Person das Gruppenrichtlinienobjekt in der Produktionsumgebung der Domäne bereitstellen kann.</span><span class="sxs-lookup"><span data-stu-id="056c8-136">Check the edited version of the selected GPO into the archive, so other authorized Editors can make changes or an Approver can deploy the GPO to the production environment of the domain.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="056c8-137">Auschecken rückgängig machen</span><span class="sxs-lookup"><span data-stu-id="056c8-137">Undo Check Out</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="056c8-138">Geben Sie ein ausgechecktes Gruppenrichtlinienobjekt ohne Änderungen in das Archiv zurück.</span><span class="sxs-lookup"><span data-stu-id="056c8-138">Return a checked out GPO to the archive without any changes.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="056c8-139">Versionsverwaltung</span><span class="sxs-lookup"><span data-stu-id="056c8-139">Version management</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="056c8-140">Befehl</span><span class="sxs-lookup"><span data-stu-id="056c8-140">Command</span></span></th>
<th align="left"><span data-ttu-id="056c8-141">Effekt</span><span class="sxs-lookup"><span data-stu-id="056c8-141">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="056c8-142">Aus Produktion importieren</span><span class="sxs-lookup"><span data-stu-id="056c8-142">Import from Production</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="056c8-143">Kopieren Sie für das ausgewählte Gruppenrichtlinienobjekt die Version in der Produktionsumgebung der Domäne in das Archiv.</span><span class="sxs-lookup"><span data-stu-id="056c8-143">For the selected GPO, copy the version in the production environment of the domain to the archive.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="056c8-144">Aus Datei importieren</span><span class="sxs-lookup"><span data-stu-id="056c8-144">Import from File</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="056c8-145">Ersetzen Sie die Richtlinieneinstellungen des ausgewählten, ausgecheckten Gruppenrichtlinienobjekts durch die von einer GPO-Sicherungsdatei.</span><span class="sxs-lookup"><span data-stu-id="056c8-145">Replace the policy settings of the selected, checked-out GPO with those from a GPO backup file.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="056c8-146">Delete</span><span class="sxs-lookup"><span data-stu-id="056c8-146">Delete</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="056c8-147">Verschieben Sie das ausgewählte Gruppenrichtlinienobjekt in den Papierkorb, und geben Sie an, ob Sie die bereitgestellte Version (sofern vorhanden) in Production belassen oder die bereitgestellte Version zusätzlich zur Version im Archiv löschen möchten.</span><span class="sxs-lookup"><span data-stu-id="056c8-147">Move the selected GPO to the Recycle Bin and indicate whether to leave the deployed version (if one exists) in production or to delete the deployed version in addition to the version in the archive.</span></span> <span data-ttu-id="056c8-148">Wenn Sie nicht über die Berechtigung zum Löschen eines Gruppenrichtlinienobjekts verfügen, werden Sie aufgefordert, eine Anforderung zu senden.</span><span class="sxs-lookup"><span data-stu-id="056c8-148">If you do not have permission to delete a GPO, you are prompted to submit a request.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="056c8-149">Bereitstellen</span><span class="sxs-lookup"><span data-stu-id="056c8-149">Deploy</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="056c8-150">Verschieben Sie das ausgewählte Gruppenrichtlinienobjekt, das in das Archiv eingecheckt ist, in die Produktionsumgebung der Domäne.</span><span class="sxs-lookup"><span data-stu-id="056c8-150">Move the selected GPO that is checked into the archive to the production environment of the domain.</span></span> <span data-ttu-id="056c8-151">Mit dieser Aktion wird Sie im Netzwerk aktiviert und die zuvor aktive Version des Gruppenrichtlinienobjekts überschrieben, falls vorhanden.</span><span class="sxs-lookup"><span data-stu-id="056c8-151">This action makes it active on the network and overwrites the previously active version of the GPO if one existed.</span></span> <span data-ttu-id="056c8-152">Wenn Sie nicht über die Berechtigung zum Bereitstellen eines GPO verfügen, werden Sie aufgefordert, eine Anforderung zu senden.</span><span class="sxs-lookup"><span data-stu-id="056c8-152">If you do not have permission to deploy a GPO, you will be prompted to submit a request.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="056c8-153">Exportieren nach</span><span class="sxs-lookup"><span data-stu-id="056c8-153">Export to</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="056c8-154">Speichern Sie das ausgewählte Gruppenrichtlinienobjekt in einer Sicherungsdatei, damit Sie es in eine andere Domäne kopieren können.</span><span class="sxs-lookup"><span data-stu-id="056c8-154">Save the selected GPO to a backup file so that you can copy it to another domain.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="056c8-155">Label</span><span class="sxs-lookup"><span data-stu-id="056c8-155">Label</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="056c8-156">Markieren Sie das ausgewählte Gruppenrichtlinienobjekt mit einer beschreibenden Bezeichnung (wie &quot; "bekannt gut &quot; ") und kommentieren Sie die Datensatzspeicherung.</span><span class="sxs-lookup"><span data-stu-id="056c8-156">Mark the selected GPO with a descriptive label (such as &quot;Known good&quot;) and comment for record keeping.</span></span> <span data-ttu-id="056c8-157">Beschriftungen werden in der <strong> </strong> Spalte Zustand und Kommentare in der <strong> </strong> Spalte Kommentar des <strong> verlaufsfensters angezeigt </strong> .</span><span class="sxs-lookup"><span data-stu-id="056c8-157">Labels appear in the <strong>State</strong> column and comments in the <strong>Comment</strong> column of the <strong>History</strong> window.</span></span> <span data-ttu-id="056c8-158">Sie unterstützen Sie beim Ermitteln früherer Versionen eines Gruppenrichtlinienobjekts, sodass Sie einen Rollback durchführen können, wenn ein Problem auftritt.</span><span class="sxs-lookup"><span data-stu-id="056c8-158">They help you identify earlier versions of a GPO so that you can roll back if a problem occurs.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="056c8-159">Rename</span><span class="sxs-lookup"><span data-stu-id="056c8-159">Rename</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="056c8-160">Ändern Sie den Namen des ausgewählten Gruppenrichtlinienobjekts.</span><span class="sxs-lookup"><span data-stu-id="056c8-160">Change the name of the selected GPO.</span></span> <span data-ttu-id="056c8-161">Wenn das Gruppenrichtlinienobjekt bereits bereitgestellt wurde, wird der Name in der Produktionsumgebung der Domäne aktualisiert, wenn das Gruppenrichtlinienobjekt erneut bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="056c8-161">If the GPO has already been deployed, the name will be updated in the production environment of the domain when the GPO is redeployed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="056c8-162">Als Vorlage speichern</span><span class="sxs-lookup"><span data-stu-id="056c8-162">Save as Template</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="056c8-163">Erstellen Sie eine neue Vorlage basierend auf den Einstellungen des ausgewählten Gruppenrichtlinienobjekts.</span><span class="sxs-lookup"><span data-stu-id="056c8-163">Create a new template based on the settings of the selected GPO.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="056c8-164">Verschiedenes</span><span class="sxs-lookup"><span data-stu-id="056c8-164">Miscellaneous</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="056c8-165">Befehl</span><span class="sxs-lookup"><span data-stu-id="056c8-165">Command</span></span></th>
<th align="left"><span data-ttu-id="056c8-166">Effekt</span><span class="sxs-lookup"><span data-stu-id="056c8-166">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="056c8-167">Aktualisieren</span><span class="sxs-lookup"><span data-stu-id="056c8-167">Refresh</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="056c8-168">Aktualisieren Sie die Anzeige der Gruppenrichtlinien-Verwaltungskonsole (Group Policy Management Console, GPMC), um alle Änderungen einzubeziehen.</span><span class="sxs-lookup"><span data-stu-id="056c8-168">Update the display of the Group Policy Management Console (GPMC) to incorporate any changes.</span></span> <span data-ttu-id="056c8-169">Einige Änderungen werden erst angezeigt, wenn die Anzeige aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="056c8-169">Some changes are not visible until the display is refreshed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="056c8-170">Hilfe</span><span class="sxs-lookup"><span data-stu-id="056c8-170">Help</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="056c8-171">Anzeigen der Hilfe zu AGPM</span><span class="sxs-lookup"><span data-stu-id="056c8-171">Display help for AGPM.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="056c8-172">Weitere Verweise</span><span class="sxs-lookup"><span data-stu-id="056c8-172">Additional references</span></span>

-   [<span data-ttu-id="056c8-173">Registerkarte "Inhalt"</span><span class="sxs-lookup"><span data-stu-id="056c8-173">Contents Tab</span></span>](contents-tab-agpm40.md)

-   [<span data-ttu-id="056c8-174">Durchführen von Editor-Aufgaben</span><span class="sxs-lookup"><span data-stu-id="056c8-174">Performing Editor Tasks</span></span>](performing-editor-tasks-agpm40.md)

-   [<span data-ttu-id="056c8-175">Durchführen der Aufgaben von genehmigenden Personen</span><span class="sxs-lookup"><span data-stu-id="056c8-175">Performing Approver Tasks</span></span>](performing-approver-tasks-agpm40.md)

-   [<span data-ttu-id="056c8-176">Durchführen von Prüferaufgaben</span><span class="sxs-lookup"><span data-stu-id="056c8-176">Performing Reviewer Tasks</span></span>](performing-reviewer-tasks-agpm40.md)

 

 





