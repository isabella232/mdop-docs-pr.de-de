---
title: HELP
description: HELP
author: dansimp
ms.assetid: 0ddb5f18-0c0a-45ea-b7c7-2d4749e3d35d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 395e6199529ccbe708aa7d1ac6673ea6f9494ae4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808770"
---
# <span data-ttu-id="328ff-103">HELP</span><span class="sxs-lookup"><span data-stu-id="328ff-103">HELP</span></span>


<span data-ttu-id="328ff-104">Zeigt Informationen zu den verschiedenen SFTMIME-Befehlen an, die in Application Virtualization (App-V) verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="328ff-104">Displays information about the various SFTMIME commands that can be used in Application Virtualization (App-V).</span></span>

## <span data-ttu-id="328ff-105">HELP</span><span class="sxs-lookup"><span data-stu-id="328ff-105">HELP</span></span>


`SFTMIME [/? | /HELP [VERB:<verb>]]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="328ff-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="328ff-106">Parameter</span></span></th>
<th align="left"><span data-ttu-id="328ff-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="328ff-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="328ff-108">/?,/Help</span><span class="sxs-lookup"><span data-stu-id="328ff-108">/?, /HELP</span></span></p></td>
<td align="left"><p><span data-ttu-id="328ff-109">Zeigt Nutzungsinformationen an.</span><span class="sxs-lookup"><span data-stu-id="328ff-109">Displays usage information.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="328ff-110">Verb</span><span class="sxs-lookup"><span data-stu-id="328ff-110">verb</span></span></p></td>
<td align="left"><p><span data-ttu-id="328ff-111">Der auszuführende Befehl, beispielsweise "hinzufügen", "Aktualisieren", "Hilfe" oder "entfernen".</span><span class="sxs-lookup"><span data-stu-id="328ff-111">The command to run, such as ADD, REFRESH, HELP or REMOVE.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="328ff-112">Objekt</span><span class="sxs-lookup"><span data-stu-id="328ff-112">object</span></span></p></td>
<td align="left"><p><span data-ttu-id="328ff-113">Wofür der Befehl gilt, beispielsweise App: &quot; Standardanwendung.&quot;</span><span class="sxs-lookup"><span data-stu-id="328ff-113">What the command applies to, such as APP:&quot;Default Application.&quot;</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="328ff-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="328ff-114">parameters</span></span></p></td>
<td align="left"><p><span data-ttu-id="328ff-115">Optionale Parameter für das angegebene Verb und Objekt.</span><span class="sxs-lookup"><span data-stu-id="328ff-115">Optional parameters for the specified verb and object.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="328ff-116">/Log</span><span class="sxs-lookup"><span data-stu-id="328ff-116">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="328ff-117">Protokollausgabe in den angegebenen Pfadname.</span><span class="sxs-lookup"><span data-stu-id="328ff-117">Log output to the specified path name.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="328ff-118">/Console</span><span class="sxs-lookup"><span data-stu-id="328ff-118">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="328ff-119">Zeigt die Ausgabe im aktiven Konsolenfenster an (Standardeinstellung).</span><span class="sxs-lookup"><span data-stu-id="328ff-119">Displays output in the active console window (default).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="328ff-120">/GUI</span><span class="sxs-lookup"><span data-stu-id="328ff-120">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="328ff-121">Zeigt Fehler in einem Dialogfeld an (gilt nicht für Abfragen).</span><span class="sxs-lookup"><span data-stu-id="328ff-121">Displays errors in a dialog box (not valid for queries).</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="328ff-122">Für Version 4.6 wurde die folgende Option hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="328ff-122">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="328ff-123">/LOGU</span><span class="sxs-lookup"><span data-stu-id="328ff-123">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="328ff-124">Wenn angegeben, wird die Ausgabe mit dem angegebenen Pfadname im Unicode-Format protokolliert.</span><span class="sxs-lookup"><span data-stu-id="328ff-124">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="328ff-125">Die in der folgenden Tabelle beschriebenen Verben werden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="328ff-125">The verbs described in the following table are supported.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="328ff-126">HINZUFÜGEN</span><span class="sxs-lookup"><span data-stu-id="328ff-126">ADD</span></span></p></td>
<td align="left"><p><span data-ttu-id="328ff-127">Fügt dem App-V-Client eine neue Anwendung, ein Paket, eine Dateitypzuordnung oder einen Veröffentlichungsserver hinzu.</span><span class="sxs-lookup"><span data-stu-id="328ff-127">Adds a new application, package, file type association, or publishing server to the App-V Client.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="328ff-128">Konfigurieren</span><span class="sxs-lookup"><span data-stu-id="328ff-128">CONFIGURE</span></span></p></td>
<td align="left"><p><span data-ttu-id="328ff-129">Ändert die Konfiguration einer Anwendung, eines Pakets, einer Dateitypzuordnung oder eines Veröffentlichungsservers.</span><span class="sxs-lookup"><span data-stu-id="328ff-129">Changes the configuration of an application, a package, a file type association, or a publishing server.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="328ff-130">DELETE</span><span class="sxs-lookup"><span data-stu-id="328ff-130">DELETE</span></span></p></td>
<td align="left"><p><span data-ttu-id="328ff-131">Entfernt Anwendungen, Pakete, Dateitypzuordnungen oder Server.</span><span class="sxs-lookup"><span data-stu-id="328ff-131">Removes applications, packages, file type associations, or servers.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="328ff-132">Laden</span><span class="sxs-lookup"><span data-stu-id="328ff-132">LOAD</span></span></p></td>
<td align="left"><p><span data-ttu-id="328ff-133">Lädt ein Paket in den Dateisystemcache.</span><span class="sxs-lookup"><span data-stu-id="328ff-133">Loads a package into the file system cache.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="328ff-134">Reparatur</span><span class="sxs-lookup"><span data-stu-id="328ff-134">REPAIR</span></span></p></td>
<td align="left"><p><span data-ttu-id="328ff-135">Setzt Ihre persönlichen Einstellungen für eine Anwendung zurück.</span><span class="sxs-lookup"><span data-stu-id="328ff-135">Resets your personal settings for an application.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="328ff-136">Aktualisieren</span><span class="sxs-lookup"><span data-stu-id="328ff-136">REFRESH</span></span></p></td>
<td align="left"><p><span data-ttu-id="328ff-137">Löst eine Aktualisierung des Veröffentlichungsservers aus.</span><span class="sxs-lookup"><span data-stu-id="328ff-137">Triggers a publishing server refresh.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="328ff-138">Veröffentlichen</span><span class="sxs-lookup"><span data-stu-id="328ff-138">PUBLISH</span></span></p></td>
<td align="left"><p><span data-ttu-id="328ff-139">Veröffentlicht eine Anwendungsverknüpfung für das Startmenü, den Desktop oder einen anderen angegebenen Speicherort des Benutzers oder kann verwendet werden, um den Inhalt eines gesamten Pakets zu veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="328ff-139">Publishes an application shortcut to the user's Start menu, desktop, or other specified location, or can be used to publish the contents of an entire package.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="328ff-140">Veröffentlichung</span><span class="sxs-lookup"><span data-stu-id="328ff-140">UNPUBLISH</span></span></p></td>
<td align="left"><p><span data-ttu-id="328ff-141">Entfernt die Verknüpfungen und Dateitypen für ein gesamtes Paket.</span><span class="sxs-lookup"><span data-stu-id="328ff-141">Removes the shortcuts and file types for an entire package.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="328ff-142">Abfrage</span><span class="sxs-lookup"><span data-stu-id="328ff-142">QUERY</span></span></p></td>
<td align="left"><p><span data-ttu-id="328ff-143">Ruft eine aktuelle Liste von Anwendungen, Paketen, Dateitypzuordnungen oder Veröffentlichungsservern ab.</span><span class="sxs-lookup"><span data-stu-id="328ff-143">Gets a current list of applications, packages, file type associations, or publishing servers.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="328ff-144">Deaktivieren</span><span class="sxs-lookup"><span data-stu-id="328ff-144">CLEAR</span></span></p></td>
<td align="left"><p><span data-ttu-id="328ff-145">Entfernt ihre persönlichen Einstellungen und Desktopkonfigurationen für eine oder mehrere Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="328ff-145">Removes your personal settings and desktop configurations for one or more applications.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="328ff-146">Entladen</span><span class="sxs-lookup"><span data-stu-id="328ff-146">UNLOAD</span></span></p></td>
<td align="left"><p><span data-ttu-id="328ff-147">Entladen eines Pakets aus dem Dateisystemcache</span><span class="sxs-lookup"><span data-stu-id="328ff-147">Unloads a package from the file system cache.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="328ff-148">Sperren</span><span class="sxs-lookup"><span data-stu-id="328ff-148">LOCK</span></span></p></td>
<td align="left"><p><span data-ttu-id="328ff-149">Sperrt die im Dateisystemcache angegebene Anwendung.</span><span class="sxs-lookup"><span data-stu-id="328ff-149">Locks the application specified in the file system cache.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="328ff-150">Entsperren</span><span class="sxs-lookup"><span data-stu-id="328ff-150">UNLOCK</span></span></p></td>
<td align="left"><p><span data-ttu-id="328ff-151">Entsperrt die im Dateisystemcache angegebene Anwendung.</span><span class="sxs-lookup"><span data-stu-id="328ff-151">Unlocks the application specified in the file system cache.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="328ff-152">Verwenden Sie den folgenden Befehl, um weitere Informationen zu den vorhergehenden Aktionen zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="328ff-152">For more information about the preceding actions, use the following command:</span></span>

`SFTMIME /HELP VERB:verb`

<span data-ttu-id="328ff-153">Mit dem folgenden Befehl werden beispielsweise Informationen für das Add-Verb angezeigt:</span><span class="sxs-lookup"><span data-stu-id="328ff-153">For example, the following command will display information for the ADD verb:</span></span>

`SFTMIME /HELP VERB:ADD`

## <span data-ttu-id="328ff-154">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="328ff-154">Related topics</span></span>


[<span data-ttu-id="328ff-155">SFTMIME-Befehlsreferenz</span><span class="sxs-lookup"><span data-stu-id="328ff-155">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





