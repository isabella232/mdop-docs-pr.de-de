---
title: Vorlagenbefehle
description: Vorlagenbefehle
author: dansimp
ms.assetid: 243a9b18-bf3f-44fa-94d7-5c793f7322da
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2c540bf87462f501a4db5596faca43ef66ee8558
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807447"
---
# <span data-ttu-id="731eb-103">Vorlagenbefehle</span><span class="sxs-lookup"><span data-stu-id="731eb-103">Template Commands</span></span>


<span data-ttu-id="731eb-104">Registerkarte " **Vorlagen** ":</span><span class="sxs-lookup"><span data-stu-id="731eb-104">The **Templates** tab:</span></span>

-   <span data-ttu-id="731eb-105">Zeigt eine Liste der verfügbaren Vorlagen an, die Sie zum Erstellen neuer Gruppenrichtlinienobjekte (Group Policy Objects, GPOs) verwenden können.</span><span class="sxs-lookup"><span data-stu-id="731eb-105">Displays a list of available templates that you can use to create new Group Policy Objects (GPOs).</span></span>

-   <span data-ttu-id="731eb-106">Bietet ein Kontextmenü mit Befehlen zum Erstellen eines Gruppenrichtlinienobjekts auf der Grundlage einer ausgewählten Vorlage, zum Verwalten von Vorlagen und zum Anzeigen von Berichten für Vorlagen.</span><span class="sxs-lookup"><span data-stu-id="731eb-106">Provides a shortcut menu with commands for creating a GPO based on a selected template, managing templates, and displaying reports for templates.</span></span>

-   <span data-ttu-id="731eb-107">Zeigt eine Liste der Gruppen und Benutzer an, die über die Berechtigung zum Zugriff auf eine ausgewählte Vorlage verfügen.</span><span class="sxs-lookup"><span data-stu-id="731eb-107">Displays a list of the groups and users who have permission to access a selected template.</span></span>

<span data-ttu-id="731eb-108">Da eine Vorlage nicht geändert werden kann, haben Vorlagen keinen Verlauf.</span><span class="sxs-lookup"><span data-stu-id="731eb-108">Because a template cannot be altered, templates have no history.</span></span> <span data-ttu-id="731eb-109">Wie bei allen GPO-Versionen können die Einstellungen einer Vorlage jedoch mit einem Einstellungsbericht angezeigt oder mit einem anderen Gruppenrichtlinienobjekt mit einem Differenz Bericht verglichen werden.</span><span class="sxs-lookup"><span data-stu-id="731eb-109">However, like any GPO version, the settings of a template can be displayed with a settings report or compared to another GPO with a difference report.</span></span>

<span data-ttu-id="731eb-110">**Hinweis**  Eine Vorlage ist eine nicht bearbeitbare, statische Version eines GPO, die als Ausgangspunkt zum Erstellen neuer, bearbeitbarer GPOs verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="731eb-110">**Note** A template is an uneditable, static version of a GPO for use as a starting point for creating new, editable GPOs.</span></span>

 

<span data-ttu-id="731eb-111">Wenn Sie mit der rechten Maustaste auf die Liste der **Gruppenrichtlinienobjekte** auf dieser Registerkarte klicken, wird ein Kontextmenü angezeigt, einschließlich der jeweils folgenden Optionen.</span><span class="sxs-lookup"><span data-stu-id="731eb-111">Right-clicking the **Group Policy Objects** list on this tab displays a shortcut menu, including whichever of the following options are applicable.</span></span>

## <span data-ttu-id="731eb-112">Steuerelement</span><span class="sxs-lookup"><span data-stu-id="731eb-112">Control</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="731eb-113">Befehl</span><span class="sxs-lookup"><span data-stu-id="731eb-113">Command</span></span></th>
<th align="left"><span data-ttu-id="731eb-114">Effekt</span><span class="sxs-lookup"><span data-stu-id="731eb-114">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="731eb-115">Neues gesteuertes Gruppenrichtlinienobjekt</span><span class="sxs-lookup"><span data-stu-id="731eb-115">New Controlled GPO</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="731eb-116">Erstellen eines neuen Gruppenrichtlinienobjekts auf der Grundlage der ausgewählten Vorlage</span><span class="sxs-lookup"><span data-stu-id="731eb-116">Create a new GPO based on the selected template.</span></span> <span data-ttu-id="731eb-117">Die Option zum Bereitstellen des neuen Gruppenrichtlinienobjekts in der Produktionsumgebung der Domäne wird bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="731eb-117">The option to deploy the new GPO to the production environment of the domain is provided.</span></span> <span data-ttu-id="731eb-118">Wenn Sie nicht über die Berechtigung zum Erstellen eines Gruppenrichtlinienobjekts verfügen, werden Sie aufgefordert, eine Anforderung zu senden.</span><span class="sxs-lookup"><span data-stu-id="731eb-118">If you do not have permission to create a GPO, you will be prompted to submit a request.</span></span> <span data-ttu-id="731eb-119">(Diese Option wird angezeigt, wenn beim Klicken mit der rechten Maustaste auf die <strong> Liste der Gruppenrichtlinienobjekte </strong> .)</span><span class="sxs-lookup"><span data-stu-id="731eb-119">(This option is displayed if no GPO is selected when right-clicking in the <strong>Group Policy Objects</strong> list.)</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="731eb-120">Berichte</span><span class="sxs-lookup"><span data-stu-id="731eb-120">Reports</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="731eb-121">Befehl</span><span class="sxs-lookup"><span data-stu-id="731eb-121">Command</span></span></th>
<th align="left"><span data-ttu-id="731eb-122">Effekt</span><span class="sxs-lookup"><span data-stu-id="731eb-122">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="731eb-123">Einstellungen</span><span class="sxs-lookup"><span data-stu-id="731eb-123">Settings</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="731eb-124">Generieren eines HTML-basierten oder XML-basierten Berichts, in dem die Einstellungen des ausgewählten Gruppenrichtlinienobjekts angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="731eb-124">Generate an HTML-based or XML-based report displaying the settings within the selected GPO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="731eb-125">Unterschiede</span><span class="sxs-lookup"><span data-stu-id="731eb-125">Differences</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="731eb-126">Generieren eines HTML-basierten oder XML-basierten Berichts, der die Einstellungen in zwei ausgewählten GPO-Vorlagen vergleicht</span><span class="sxs-lookup"><span data-stu-id="731eb-126">Generate an HTML-based or XML-based report comparing the settings within two selected GPO templates.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="731eb-127">Vorlagenverwaltung</span><span class="sxs-lookup"><span data-stu-id="731eb-127">Template management</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="731eb-128">Befehl</span><span class="sxs-lookup"><span data-stu-id="731eb-128">Command</span></span></th>
<th align="left"><span data-ttu-id="731eb-129">Effekt</span><span class="sxs-lookup"><span data-stu-id="731eb-129">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="731eb-130">Als Standard festlegen</span><span class="sxs-lookup"><span data-stu-id="731eb-130">Set as Default</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="731eb-131">Die ausgewählte Vorlage als Standard festlegen, der beim Erstellen eines neuen Gruppenrichtlinienobjekts automatisch verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="731eb-131">Set the selected template as the default to be used automatically when creating a new GPO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="731eb-132">Delete</span><span class="sxs-lookup"><span data-stu-id="731eb-132">Delete</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="731eb-133">Verschieben der ausgewählten Vorlage in den <strong> Papierkorb </strong></span><span class="sxs-lookup"><span data-stu-id="731eb-133">Move the selected template to the <strong>Recycle Bin</strong>.</span></span> <span data-ttu-id="731eb-134">Wenn Sie nicht über die Berechtigung zum Löschen eines Gruppenrichtlinienobjekts verfügen, werden Sie aufgefordert, eine Anforderung zu senden.</span><span class="sxs-lookup"><span data-stu-id="731eb-134">If you do not have permission to delete a GPO, you will be prompted to submit a request.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="731eb-135">Rename</span><span class="sxs-lookup"><span data-stu-id="731eb-135">Rename</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="731eb-136">Ändern des Namens der ausgewählten Vorlage</span><span class="sxs-lookup"><span data-stu-id="731eb-136">Change the name of the selected template.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="731eb-137">Verschiedenes</span><span class="sxs-lookup"><span data-stu-id="731eb-137">Miscellaneous</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="731eb-138">Befehl</span><span class="sxs-lookup"><span data-stu-id="731eb-138">Command</span></span></th>
<th align="left"><span data-ttu-id="731eb-139">Effekt</span><span class="sxs-lookup"><span data-stu-id="731eb-139">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="731eb-140">Aktualisieren</span><span class="sxs-lookup"><span data-stu-id="731eb-140">Refresh</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="731eb-141">Aktualisieren Sie die Anzeige der Gruppenrichtlinien-Verwaltungskonsole, um alle Änderungen einzubeziehen.</span><span class="sxs-lookup"><span data-stu-id="731eb-141">Update the display of the Group Policy Management Console to incorporate any changes.</span></span> <span data-ttu-id="731eb-142">Einige Änderungen werden erst angezeigt, wenn die Anzeige aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="731eb-142">Some changes are not visible until the display is refreshed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="731eb-143">Hilfe</span><span class="sxs-lookup"><span data-stu-id="731eb-143">Help</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="731eb-144">Anzeigen der Hilfe für erweiterte Gruppenrichtlinienverwaltung (AGPM)</span><span class="sxs-lookup"><span data-stu-id="731eb-144">Display help for Advanced Group Policy Management (AGPM).</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="731eb-145">Weitere Verweise</span><span class="sxs-lookup"><span data-stu-id="731eb-145">Additional references</span></span>

-   [<span data-ttu-id="731eb-146">Registerkarte "Inhalt"</span><span class="sxs-lookup"><span data-stu-id="731eb-146">Contents Tab</span></span>](contents-tab-agpm40.md)

-   [<span data-ttu-id="731eb-147">Durchführen von Editor-Aufgaben</span><span class="sxs-lookup"><span data-stu-id="731eb-147">Performing Editor Tasks</span></span>](performing-editor-tasks-agpm40.md)

-   [<span data-ttu-id="731eb-148">Durchführen von Prüferaufgaben</span><span class="sxs-lookup"><span data-stu-id="731eb-148">Performing Reviewer Tasks</span></span>](performing-reviewer-tasks-agpm40.md)

 

 





