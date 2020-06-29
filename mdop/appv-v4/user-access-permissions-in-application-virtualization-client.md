---
title: Benutzerzugriffsberechtigungen in Application Virtualization Client
description: Benutzerzugriffsberechtigungen in Application Virtualization Client
author: dansimp
ms.assetid: 7459374c-810c-45e3-b205-fdd1f8514f80
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1083faffb48aa58a0ee0c81b58fae307e53548b8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806179"
---
# <span data-ttu-id="45b96-103">Benutzerzugriffsberechtigungen in Application Virtualization Client</span><span class="sxs-lookup"><span data-stu-id="45b96-103">User Access Permissions in Application Virtualization Client</span></span>


<span data-ttu-id="45b96-104">Auf der Registerkarte " **Berechtigungen** " im Dialogfeld " **Eigenschaften** ", das durch Klicken mit der rechten Maustaste auf den Knoten **Application Virtualization** in der Application Virtualization Client Management Console aufgerufen wird, können Administratoren Benutzern Berechtigungen zur Verwendung der verschiedenen Client Funktionen erteilen.</span><span class="sxs-lookup"><span data-stu-id="45b96-104">On the **Permissions** tab on the **Properties** dialog box, accessible by right-clicking the **Application Virtualization** node in the Application Virtualization Client Management Console, administrators can grant users permissions to use the various client functions.</span></span>

<span data-ttu-id="45b96-105">**Hinweis**  Bevor Sie die Benutzerberechtigungen ändern, stellen Sie sicher, dass alle Berechtigungsänderungen mit den Richtlinien der Organisation für die Gewährung von Benutzerberechtigungen konsistent sind.</span><span class="sxs-lookup"><span data-stu-id="45b96-105">**Note** Before changing users permissions, ensure that any permissions changes are consistent with the organization's guidelines for granting user permissions.</span></span>

 

<span data-ttu-id="45b96-106">In der folgenden Tabelle sind die Berechtigungen aufgeführt und beschrieben, die Benutzern gewährt werden können.</span><span class="sxs-lookup"><span data-stu-id="45b96-106">The following table lists and describes the permissions that can be granted to users.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="45b96-107">Berechtigungs Name</span><span class="sxs-lookup"><span data-stu-id="45b96-107">Permission Name</span></span></th>
<th align="left"><span data-ttu-id="45b96-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="45b96-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="45b96-109">Hinzufügen von Anwendungen</span><span class="sxs-lookup"><span data-stu-id="45b96-109">Add applications</span></span></p></td>
<td align="left"><p><span data-ttu-id="45b96-110">Registrieren Sie neue Anwendungen, indem Sie eine neue OSD-Datei an den Client übergeben, indem Sie sfttray.exe, sftmime.exe oder die MMC verwenden.</span><span class="sxs-lookup"><span data-stu-id="45b96-110">Register new applications by passing a new OSD file to the client by using sfttray.exe, sftmime.exe or the MMC.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="45b96-111">Ändern der Größe des Dateisystemcaches</span><span class="sxs-lookup"><span data-stu-id="45b96-111">Change file system cache size</span></span></p></td>
<td align="left"><p><span data-ttu-id="45b96-112">Vergrößern des Dateisystemcaches</span><span class="sxs-lookup"><span data-stu-id="45b96-112">Increase the size of the file system cache.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="45b96-113">Ändern des Dateisystemlaufwerks</span><span class="sxs-lookup"><span data-stu-id="45b96-113">Change file system drive</span></span></p></td>
<td align="left"><p><span data-ttu-id="45b96-114">Wählen Sie einen anderen bevorzugten Laufwerkbuchstaben für das Dateisystem aus.</span><span class="sxs-lookup"><span data-stu-id="45b96-114">Select a different preferred drive letter for the file system.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="45b96-115">Ändern von Protokolleinstellungen</span><span class="sxs-lookup"><span data-stu-id="45b96-115">Change log settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="45b96-116">Ändern Sie die Protokollebene oder den Protokollpfad für die Clientprotokolldatei.</span><span class="sxs-lookup"><span data-stu-id="45b96-116">Change the log level or the log path for the client log file.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="45b96-117">Ändern von OSD-Dateien</span><span class="sxs-lookup"><span data-stu-id="45b96-117">Change OSD files</span></span></p></td>
<td align="left"><p><span data-ttu-id="45b96-118">Ändern Sie die OSD-Dateien für registrierte Anwendungen, und übergeben Sie diese an den Client.</span><span class="sxs-lookup"><span data-stu-id="45b96-118">Modify OSD files for registered applications and pass them into the client.</span></span> <span data-ttu-id="45b96-119">Dies hat keinen Einfluss auf die Veröffentlichungsaktualisierung.</span><span class="sxs-lookup"><span data-stu-id="45b96-119">This does not affect publishing refresh.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="45b96-120">Löschen von Anwendungseinstellungen</span><span class="sxs-lookup"><span data-stu-id="45b96-120">Clear application settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="45b96-121">Löschen Sie Dateitypen, Verknüpfungen und alle Konfigurationen für den aktuellen Benutzer.</span><span class="sxs-lookup"><span data-stu-id="45b96-121">Delete file types, shortcuts and any configurations for the current user.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="45b96-122">Löschen von Anwendungen</span><span class="sxs-lookup"><span data-stu-id="45b96-122">Delete applications</span></span></p></td>
<td align="left"><p><span data-ttu-id="45b96-123">Entfernen Sie alle Verweise auf eine Anwendung aus dem Dateisystem und dem OSD-Cache für alle Benutzer auf dem Computer.</span><span class="sxs-lookup"><span data-stu-id="45b96-123">Remove all references to an application from the file system and OSD cache for all users on the computer.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="45b96-124">Importieren von Anwendungen in den Cache</span><span class="sxs-lookup"><span data-stu-id="45b96-124">Import applications into the cache</span></span></p></td>
<td align="left"><p><span data-ttu-id="45b96-125">Laden Sie Anwendungsdaten direkt aus einer angegebenen SFT-Datei in den Dateisystemcache.</span><span class="sxs-lookup"><span data-stu-id="45b96-125">Load application data directly from a specified SFT file into the file system cache.</span></span> <span data-ttu-id="45b96-126">Dies wirkt sich auf alle Benutzer aus.</span><span class="sxs-lookup"><span data-stu-id="45b96-126">This affects all users.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="45b96-127">Laden von Anwendungen in den Cache</span><span class="sxs-lookup"><span data-stu-id="45b96-127">Load applications into the cache</span></span></p></td>
<td align="left"><p><span data-ttu-id="45b96-128">Starten Sie eine Auslastung der SFT-Datei für eine Anwendung aus der konfigurierten Quelle, beispielsweise einem App-V-Streamingserver.</span><span class="sxs-lookup"><span data-stu-id="45b96-128">Start a load of the SFT file for an application from the configured source, such as an App-V Streaming Server.</span></span> <span data-ttu-id="45b96-129">Dadurch wird die Anwendung für alle Benutzer auf dem Computer geladen.</span><span class="sxs-lookup"><span data-stu-id="45b96-129">This loads the application for all users on the computer.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="45b96-130">Sperren und Entsperren von Anwendungen im Cache</span><span class="sxs-lookup"><span data-stu-id="45b96-130">Lock and unlock applications in the cache</span></span></p></td>
<td align="left"><p><span data-ttu-id="45b96-131">Verhindern oder zulassen, dass Anwendungen aus dem Dateisystemcache entladen werden.</span><span class="sxs-lookup"><span data-stu-id="45b96-131">Prevent or allow applications from being unloaded from the file system cache.</span></span> <span data-ttu-id="45b96-132">Dies wirkt sich auf alle Benutzer auf dem Computer aus.</span><span class="sxs-lookup"><span data-stu-id="45b96-132">This affects all users on the computer.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="45b96-133">Verwalten von Dateitypzuordnungen</span><span class="sxs-lookup"><span data-stu-id="45b96-133">Manage file type associations</span></span></p></td>
<td align="left"><p><span data-ttu-id="45b96-134">Sie können Dateitypzuordnungen nur für den aktuellen Benutzer hinzufügen, ändern oder löschen.</span><span class="sxs-lookup"><span data-stu-id="45b96-134">Add, modify, or delete file type associations for the current user only.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="45b96-135">Verwalten von Veröffentlichungs Aktualisierungseinstellungen</span><span class="sxs-lookup"><span data-stu-id="45b96-135">Manage publishing refresh settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="45b96-136">Ändern Sie die Einstellungen, mit denen die Anzeigedauer für Veröffentlichungs Aktualisierungen für alle Benutzer auf dem Computer gesteuert wird.</span><span class="sxs-lookup"><span data-stu-id="45b96-136">Change settings that control the timing of publishing refreshes for all users on the computer.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="45b96-137">Verwalten von Veröffentlichungsservern</span><span class="sxs-lookup"><span data-stu-id="45b96-137">Manage publishing servers</span></span></p></td>
<td align="left"><p><span data-ttu-id="45b96-138">Sie können Veröffentlichungsserver für alle Benutzer auf dem Computer hinzufügen, ändern oder löschen.</span><span class="sxs-lookup"><span data-stu-id="45b96-138">Add, modify, or delete publishing servers for all users on the computer.</span></span> <span data-ttu-id="45b96-139">Diese Berechtigung umfasst implizit die Berechtigung zum Verwalten von Veröffentlichungs Aktualisierungseinstellungen.</span><span class="sxs-lookup"><span data-stu-id="45b96-139">This permission implicitly includes permission to manage publishing refresh settings.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="45b96-140">Veröffentlichen von Verknüpfungen</span><span class="sxs-lookup"><span data-stu-id="45b96-140">Publish shortcuts</span></span></p></td>
<td align="left"><p><span data-ttu-id="45b96-141">Erstellen neuer Verknüpfungen zu registrierten Anwendungen</span><span class="sxs-lookup"><span data-stu-id="45b96-141">Create new shortcuts to registered applications.</span></span> <span data-ttu-id="45b96-142">Der Benutzer muss auch über die Berechtigung zum Erstellen von Dateien im lokalen Dateisystem verfügen.</span><span class="sxs-lookup"><span data-stu-id="45b96-142">The user must also have permission to create files in the local file system.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="45b96-143">Reparieren von Anwendungen</span><span class="sxs-lookup"><span data-stu-id="45b96-143">Repair applications</span></span></p></td>
<td align="left"><p><span data-ttu-id="45b96-144">Entfernen Sie anwendungsspezifische Konfigurationen für den aktuellen Benutzer, ohne Verknüpfungen oder Dateitypzuordnungen zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="45b96-144">Remove application specific configurations for the current user without removing shortcuts or file type associations.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="45b96-145">Starten einer Veröffentlichungsaktualisierung</span><span class="sxs-lookup"><span data-stu-id="45b96-145">Start a publishing refresh</span></span></p></td>
<td align="left"><p><span data-ttu-id="45b96-146">Starten einer ungeplanten Veröffentlichungsaktualisierung für den aktuellen Benutzer</span><span class="sxs-lookup"><span data-stu-id="45b96-146">Start an unscheduled publishing refresh for the current user.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="45b96-147">Offlinemodus umschalten</span><span class="sxs-lookup"><span data-stu-id="45b96-147">Toggle offline mode</span></span></p></td>
<td align="left"><p><span data-ttu-id="45b96-148">Ändern Sie den gesamten Client von Online in den Offlinemodus für alle Benutzer.</span><span class="sxs-lookup"><span data-stu-id="45b96-148">Change the entire client from online to offline mode for all users.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="45b96-149">Entladen von Anwendungen aus dem Cache</span><span class="sxs-lookup"><span data-stu-id="45b96-149">Unload applications from the cache</span></span></p></td>
<td align="left"><p><span data-ttu-id="45b96-150">Löschen Sie Anwendungsdaten aus dem Dateisystemcache für alle Benutzer, ohne benutzerspezifische Einstellungen, Verknüpfungen oder Dateitypzuordnungen zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="45b96-150">Clear application data from the file system cache for all users without removing user-specific settings, shortcuts, or file type associations.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="45b96-151">Alle Anwendungen anzeigen</span><span class="sxs-lookup"><span data-stu-id="45b96-151">View all applications</span></span></p></td>
<td align="left"><p><span data-ttu-id="45b96-152">Dem Benutzer gestatten, die virtuellen Anwendungen für alle auf dem Computer registrierten Benutzer anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="45b96-152">Allow the user to see the virtual applications for all users registered on the computer.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="45b96-153">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="45b96-153">Related topics</span></span>


[<span data-ttu-id="45b96-154">So ändern Sie die Benutzerzugriffsberechtigungen</span><span class="sxs-lookup"><span data-stu-id="45b96-154">How to Change User Access Permissions</span></span>](how-to-change-user-access-permissions.md)

 

 





