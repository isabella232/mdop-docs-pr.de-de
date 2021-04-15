---
title: Konfigurieren von UE-V 2.x mit Gruppenrichtlinienobjekten
description: Konfigurieren von UE-V 2.x mit Gruppenrichtlinienobjekten
author: dansimp
ms.assetid: 2bb55834-26ee-4f19-9860-dfdf3c797143
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b6c9636df36a53cbf65bf1904965f2809484b99c
ms.sourcegitcommit: bdc377477a8cc9e973fbcdd67c2f07b882c5d61e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2021
ms.locfileid: "11494060"
---
# <a name="configuring-ue-v-2x-with-group-policy-objects"></a><span data-ttu-id="7aaa8-103">Konfigurieren von UE-V 2.x mit Gruppenrichtlinienobjekten</span><span class="sxs-lookup"><span data-stu-id="7aaa8-103">Configuring UE-V 2.x with Group Policy Objects</span></span>


<span data-ttu-id="7aaa8-104">Einige Gruppenrichtlinieneinstellungen für Microsoft User Experience Virtualization (UE-V) 2.0, 2.1 und 2.1 SP1 können für Computer definiert werden, und andere Gruppenrichtlinieneinstellungen können für Benutzer definiert werden.</span><span class="sxs-lookup"><span data-stu-id="7aaa8-104">Some Microsoft User Experience Virtualization (UE-V) 2.0, 2.1, and 2.1 SP1 Group Policy settings can be defined for computers, and other Group Policy settings can be defined for users.</span></span> <span data-ttu-id="7aaa8-105">Informationen zum Installieren von UE-V-Gruppenrichtlinien-ADMX-Dateien finden Sie unter [Installing the UE-V 2 Group Policy ADMX Templates](https://technet.microsoft.com/library/dn458891.aspx#admx).</span><span class="sxs-lookup"><span data-stu-id="7aaa8-105">For information about how to install UE-V Group Policy ADMX files, see [Installing the UE-V 2 Group Policy ADMX Templates](https://technet.microsoft.com/library/dn458891.aspx#admx).</span></span>

<span data-ttu-id="7aaa8-106">Die folgenden Richtlinieneinstellungen können für UE-V konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="7aaa8-106">The following policy settings can be configured for UE-V.</span></span>

**<span data-ttu-id="7aaa8-107">Gruppenrichtlinieneinstellungen</span><span class="sxs-lookup"><span data-stu-id="7aaa8-107">Group Policy settings</span></span>**

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="7aaa8-108">Gruppenrichtlinieneinstellungsname</span><span class="sxs-lookup"><span data-stu-id="7aaa8-108">Group Policy setting name</span></span></th>
<th align="left"><span data-ttu-id="7aaa8-109">Ziel</span><span class="sxs-lookup"><span data-stu-id="7aaa8-109">Target</span></span></th>
<th align="left"><span data-ttu-id="7aaa8-110">Beschreibung der Gruppenrichtlinieneinstellung</span><span class="sxs-lookup"><span data-stu-id="7aaa8-110">Group Policy setting description</span></span></th>
<th align="left"><span data-ttu-id="7aaa8-111">Konfigurationsoptionen</span><span class="sxs-lookup"><span data-stu-id="7aaa8-111">Configuration options</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7aaa8-112">Konfigurieren der Synchronisierungsmethode</span><span class="sxs-lookup"><span data-stu-id="7aaa8-112">Configure Sync Method</span></span></p></td>
<td align="left"><p><span data-ttu-id="7aaa8-113">Computer und Benutzer</span><span class="sxs-lookup"><span data-stu-id="7aaa8-113">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="7aaa8-114">Mithilfe dieser Gruppenrichtlinieneinstellung können Sie konfigurieren, ob die User Experience Virtualization (UE-V) das Synchronisierungsanbieterfeature verwendet.</span><span class="sxs-lookup"><span data-stu-id="7aaa8-114">By using this Group Policy setting, you can configure whether User Experience Virtualization (UE-V) uses the sync provider feature.</span></span> <span data-ttu-id="7aaa8-115">Mit dieser Richtlinieneinstellung können Sie auch aktivieren, dass eine Benachrichtigung angezeigt wird, wenn der Import von Benutzereinstellungen verzögert wird.</span><span class="sxs-lookup"><span data-stu-id="7aaa8-115">This policy setting also lets you enable a notification to appear when the import of user settings is delayed.</span></span></p></td>
<td align="left"><p><span data-ttu-id="7aaa8-116">Aktivieren Sie diese Einstellung, um den UE-V-Agent so zu konfigurieren, dass er weder den Synchronisierungsanbieter noch das externe Synchronisierungsmodul verwendet.</span><span class="sxs-lookup"><span data-stu-id="7aaa8-116">Enable this setting to configure the UE-V agent not to use the sync provider, or to use the external synchronization engine.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7aaa8-117">Kontakt IT Link Text</span><span class="sxs-lookup"><span data-stu-id="7aaa8-117">Contact IT Link Text</span></span></p></td>
<td align="left"><p><span data-ttu-id="7aaa8-118">Nur Computer</span><span class="sxs-lookup"><span data-stu-id="7aaa8-118">Computers Only</span></span></p></td>
<td align="left"><p><span data-ttu-id="7aaa8-119">Diese Gruppenrichtlinieneinstellung gibt den Text des Hyperlinks für die Kontakt-IT-URL im Unternehmenseinstellungscenter an.</span><span class="sxs-lookup"><span data-stu-id="7aaa8-119">This Group Policy setting specifies the text of the Contact IT URL hyperlink in the Company Settings Center.</span></span></p></td>
<td align="left"><p><span data-ttu-id="7aaa8-120">Wenn Sie diese Gruppenrichtlinieneinstellung aktivieren, zeigt das Unternehmenseinstellungscenter den angegebenen Text im Link zur KONTAKT-IT-URL an.</span><span class="sxs-lookup"><span data-stu-id="7aaa8-120">If you enable this Group Policy setting, the Company Settings Center displays the specified text in the link to the Contact IT URL.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7aaa8-121">Kontaktieren der IT-URL</span><span class="sxs-lookup"><span data-stu-id="7aaa8-121">Contact IT URL</span></span></p></td>
<td align="left"><p><span data-ttu-id="7aaa8-122">Nur Computer</span><span class="sxs-lookup"><span data-stu-id="7aaa8-122">Computers Only</span></span></p></td>
<td align="left"><p><span data-ttu-id="7aaa8-123">Diese Gruppenrichtlinieneinstellung gibt die URL für den Link Kontakt-IT im Unternehmenseinstellungscenter an.</span><span class="sxs-lookup"><span data-stu-id="7aaa8-123">This Group Policy setting specifies the URL for the Contact IT link in the Company Settings Center.</span></span></p></td>
<td align="left"><p><span data-ttu-id="7aaa8-124">Wenn Sie diese Einstellung aktivieren, wird im Unternehmenseinstellungscenter It-Text kontaktieren mit der angegebenen URL verknüpft.</span><span class="sxs-lookup"><span data-stu-id="7aaa8-124">If you enable this setting, the Company Settings Center Contact IT text links to the specified URL.</span></span> <span data-ttu-id="7aaa8-125">Der Link kann eines beliebigen Standardprotokolls sein, z. B. HTTP oder mailto.</span><span class="sxs-lookup"><span data-stu-id="7aaa8-125">The link can be of any standard protocol, such as HTTP or mailto.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7aaa8-126">First Use Notification</span><span class="sxs-lookup"><span data-stu-id="7aaa8-126">First Use Notification</span></span></p></td>
<td align="left"><p><span data-ttu-id="7aaa8-127">Nur Computer</span><span class="sxs-lookup"><span data-stu-id="7aaa8-127">Computers Only</span></span></p></td>
<td align="left"><p><span data-ttu-id="7aaa8-128">Diese Gruppenrichtlinieneinstellung aktiviert eine Benachrichtigung im Benachrichtigungsbereich, die angezeigt wird, wenn UE-V</span><span class="sxs-lookup"><span data-stu-id="7aaa8-128">This Group Policy setting enables a notification in the notification area that appears when the UE-V</span></span></p>
<p><span data-ttu-id="7aaa8-129">Agent wird zum ersten Mal ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7aaa8-129">agent runs for the first time.</span></span></p></td>
<td align="left"><p><span data-ttu-id="7aaa8-130">Die Standardeinstellung ist aktiviert.</span><span class="sxs-lookup"><span data-stu-id="7aaa8-130">The default is enabled.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7aaa8-131">Pingen des Speicherorts der Einstellungen vor der Synchronisierung</span><span class="sxs-lookup"><span data-stu-id="7aaa8-131">Ping the settings storage location before sync</span></span></p></td>
<td align="left"><p><span data-ttu-id="7aaa8-132">Computer und Benutzer</span><span class="sxs-lookup"><span data-stu-id="7aaa8-132">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="7aaa8-133">Diese Richtlinieneinstellung ermöglicht der Konfiguration des UE-V-Synchronisierungsanbieters das Pingen des Speicherpfads für Einstellungen, bevor Versucht wird, Einstellungen zu synchronisieren, um die Verbindung zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="7aaa8-133">This policy setting allows configuration of the UE-V sync provider to ping the settings storage path before attempting to sync settings in order to verify the connection.</span></span></p></td>
<td align="left"><p><span data-ttu-id="7aaa8-134">Aktivieren oder Deaktivieren dieser Gruppenrichtlinieneinstellung.</span><span class="sxs-lookup"><span data-stu-id="7aaa8-134">Enable or disable this Group Policy setting.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7aaa8-135">Warnungsschwellenwert für Die Größe des Einstellungspakets</span><span class="sxs-lookup"><span data-stu-id="7aaa8-135">Settings package size warning threshold</span></span></p></td>
<td align="left"><p><span data-ttu-id="7aaa8-136">Computer und Benutzer</span><span class="sxs-lookup"><span data-stu-id="7aaa8-136">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="7aaa8-137">Mit dieser Gruppenrichtlinieneinstellung können Sie den UE-V-Agent so konfigurieren, dass er berichtet, wenn die Größe einer Einstellungspaketdatei einen definierten Schwellenwert erreicht.</span><span class="sxs-lookup"><span data-stu-id="7aaa8-137">This Group Policy setting lets you configure the UE-V Agent to report when a settings package file size reaches a defined threshold.</span></span></p></td>
<td align="left"><p><span data-ttu-id="7aaa8-138">Geben Sie den bevorzugten Schwellenwert für Einstellungspaketgrößen in Kilobyte (KB) an.</span><span class="sxs-lookup"><span data-stu-id="7aaa8-138">Specify the preferred threshold for settings package sizes in kilobytes (KB).</span></span></p>
<p><span data-ttu-id="7aaa8-139">Standardmäßig verfügt der UE-V-Agent nicht über einen Schwellenwert für die Paketdateigröße.</span><span class="sxs-lookup"><span data-stu-id="7aaa8-139">By default, the UE-V Agent does not have a package file size threshold.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7aaa8-140">Speicherpfad für Einstellungen</span><span class="sxs-lookup"><span data-stu-id="7aaa8-140">Settings storage path</span></span></p></td>
<td align="left"><p><span data-ttu-id="7aaa8-141">Computer und Benutzer</span><span class="sxs-lookup"><span data-stu-id="7aaa8-141">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="7aaa8-142">Diese Gruppenrichtlinieneinstellung konfiguriert, wo die Benutzereinstellungen gespeichert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="7aaa8-142">This Group Policy setting configures where the user settings are to be stored.</span></span></p></td>
<td align="left"><p><span data-ttu-id="7aaa8-143">Geben Sie einen UNC-Pfad (Universal Naming Convention) und Variablen wie \Server\SettingsShare%username%ein.</span><span class="sxs-lookup"><span data-stu-id="7aaa8-143">Enter a Universal Naming Convention (UNC) path and variables such as \Server\SettingsShare%username%.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7aaa8-144">Pfad des Einstellungsvorlagenkatalogs</span><span class="sxs-lookup"><span data-stu-id="7aaa8-144">Settings template catalog path</span></span></p></td>
<td align="left"><p><span data-ttu-id="7aaa8-145">Nur Computer</span><span class="sxs-lookup"><span data-stu-id="7aaa8-145">Computers Only</span></span></p></td>
<td align="left"><p><span data-ttu-id="7aaa8-146">Mit dieser Gruppenrichtlinieneinstellung wird konfiguriert, wo benutzerdefinierte Einstellungsspeicherortvorlagen gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="7aaa8-146">This Group Policy setting configures where custom settings location templates are stored.</span></span> <span data-ttu-id="7aaa8-147">Mit dieser Richtlinieneinstellung wird außerdem konfiguriert, ob der Katalog zum Ersetzen der standardmäßigen Microsoft-Vorlagen verwendet werden soll, die durch den UE-V-Agent installiert sind.</span><span class="sxs-lookup"><span data-stu-id="7aaa8-147">This policy setting also configures whether the catalog is to be used to replace the default Microsoft templates that are installed with the UE-V Agent.</span></span></p></td>
<td align="left"><p><span data-ttu-id="7aaa8-148">Geben Sie einen UNC-Pfad (Universal Naming Convention) ein, z. B. \Server\TemplateShare oder einen Ordnerspeicherort auf dem Computer.</span><span class="sxs-lookup"><span data-stu-id="7aaa8-148">Enter a Universal Naming Convention (UNC) path such as \Server\TemplateShare or a folder location on the computer.</span></span></p>
<p><span data-ttu-id="7aaa8-149">Aktivieren Sie das Kontrollkästchen, um die Standardmäßigen Microsoft-Vorlagen zu ersetzen.</span><span class="sxs-lookup"><span data-stu-id="7aaa8-149">Select the check box to replace the default Microsoft templates.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7aaa8-150">Synchronisieren von Einstellungen über gemessene Verbindungen</span><span class="sxs-lookup"><span data-stu-id="7aaa8-150">Sync settings over metered connections</span></span></p></td>
<td align="left"><p><span data-ttu-id="7aaa8-151">Computer und Benutzer</span><span class="sxs-lookup"><span data-stu-id="7aaa8-151">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="7aaa8-152">Diese Gruppenrichtlinieneinstellung definiert, ob UE-V Einstellungen über gemessene Verbindungen synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="7aaa8-152">This Group Policy setting defines whether UE-V synchronizes settings over metered connections.</span></span></p></td>
<td align="left"><p><span data-ttu-id="7aaa8-153">Standardmäßig synchronisiert der UE-V-Agent die Einstellungen nicht über eine gemessene Verbindung.</span><span class="sxs-lookup"><span data-stu-id="7aaa8-153">By default, the UE-V Agent does not synchronize settings over a metered connection.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7aaa8-154">Synchronisieren von Einstellungen über gemessene Verbindungen auch beim Roaming</span><span class="sxs-lookup"><span data-stu-id="7aaa8-154">Sync settings over metered connections even when roaming</span></span></p></td>
<td align="left"><p><span data-ttu-id="7aaa8-155">Computer und Benutzer</span><span class="sxs-lookup"><span data-stu-id="7aaa8-155">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="7aaa8-156">Diese Gruppenrichtlinieneinstellung definiert, ob UE-V Einstellungen über gemessene Verbindungen außerhalb des Heimanbieternetzwerks synchronisiert, z. B. wenn sich die Datenverbindung im Roamingmodus befindet.</span><span class="sxs-lookup"><span data-stu-id="7aaa8-156">This Group Policy setting defines whether UE-V synchronizes settings over metered connections outside of the home provider network, for example, when the data connection is in roaming mode.</span></span></p></td>
<td align="left"><p><span data-ttu-id="7aaa8-157">Standardmäßig synchronisiert UE-V die Einstellungen nicht über eine gemessene Verbindung, wenn sie sich im Roamingmodus befindet.</span><span class="sxs-lookup"><span data-stu-id="7aaa8-157">By default, UE-V does not synchronize settings over a metered connection when it is in roaming mode.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7aaa8-158">Synchronisierungstimeout</span><span class="sxs-lookup"><span data-stu-id="7aaa8-158">Synchronization timeout</span></span></p></td>
<td align="left"><p><span data-ttu-id="7aaa8-159">Computer und Benutzer</span><span class="sxs-lookup"><span data-stu-id="7aaa8-159">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="7aaa8-160">Mit dieser Gruppenrichtlinieneinstellung wird die Anzahl von Millisekunden konfiguriert, die der Computer vor einem Zeit-Out wartet, wenn Benutzereinstellungen vom Remoteeinstellungsspeicherort abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="7aaa8-160">This Group Policy setting configures the number of milliseconds that the computer waits before a time-out when it retrieves user settings from the remote settings location.</span></span> <span data-ttu-id="7aaa8-161">Wenn der Remotespeicherort nicht verfügbar ist und der Benutzer den Synchronisierungsanbieter nicht verwendet, verzögert sich der Anwendungsstart um so viele Millisekunden.</span><span class="sxs-lookup"><span data-stu-id="7aaa8-161">If the remote storage location is unavailable, and the user does not use the sync provider, the application start is delayed by this many milliseconds.</span></span></p></td>
<td align="left"><p><span data-ttu-id="7aaa8-162">Geben Sie das bevorzugte Synchronisierungs-Time-Out in Millisekunden an.</span><span class="sxs-lookup"><span data-stu-id="7aaa8-162">Specify the preferred synchronization time-out in milliseconds.</span></span> <span data-ttu-id="7aaa8-163">Der Standardwert ist 2000 Millisekunden.</span><span class="sxs-lookup"><span data-stu-id="7aaa8-163">The default value is 2000 milliseconds.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7aaa8-164">Synchronisieren von Windows-Einstellungen</span><span class="sxs-lookup"><span data-stu-id="7aaa8-164">Synchronize Windows settings</span></span> </p></td>
<td align="left"><p><span data-ttu-id="7aaa8-165">Computer und Benutzer</span><span class="sxs-lookup"><span data-stu-id="7aaa8-165">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="7aaa8-166">Diese Gruppenrichtlinieneinstellung konfiguriert die Synchronisierung von Windows-Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="7aaa8-166">This Group Policy setting configures the synchronization of Windows settings.</span></span></p></td>
<td align="left"><p><span data-ttu-id="7aaa8-167">Wählen Sie aus, welche Windows-Einstellungen zwischen Computern synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="7aaa8-167">Select which Windows settings synchronize between computers.</span></span></p>
<p><span data-ttu-id="7aaa8-168">Standardmäßig synchronisieren Windows-Designs, Desktopeinstellungen und Einstellungen für die Benutzerfreundlichkeit Einstellungen zwischen Computern derselben Betriebssystemversion.</span><span class="sxs-lookup"><span data-stu-id="7aaa8-168">By default, Windows themes, desktop settings, and Ease of Access settings synchronize settings between computers of the same operating system version.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7aaa8-169">Tablettsymbol</span><span class="sxs-lookup"><span data-stu-id="7aaa8-169">Tray Icon</span></span></p></td>
<td align="left"><p><span data-ttu-id="7aaa8-170">Nur Computer</span><span class="sxs-lookup"><span data-stu-id="7aaa8-170">Computers Only</span></span></p></td>
<td align="left"><p><span data-ttu-id="7aaa8-171">Diese Gruppenrichtlinieneinstellung aktiviert das UE-V-Traysymbol.</span><span class="sxs-lookup"><span data-stu-id="7aaa8-171">This Group Policy setting enables the UE-V tray icon.</span></span></p></td>
<td align="left"><p><span data-ttu-id="7aaa8-172">Die Standardeinstellung ist aktiviert.</span><span class="sxs-lookup"><span data-stu-id="7aaa8-172">The default is enabled.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7aaa8-173">Verwenden der Benutzeroberflächenvirtualisierung (UE-V)</span><span class="sxs-lookup"><span data-stu-id="7aaa8-173">Use User Experience Virtualization (UE-V)</span></span></p></td>
<td align="left"><p><span data-ttu-id="7aaa8-174">Computer und Benutzer</span><span class="sxs-lookup"><span data-stu-id="7aaa8-174">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="7aaa8-175">Mit dieser Gruppenrichtlinieneinstellung können Sie UE-V aktivieren oder deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="7aaa8-175">This Group Policy setting lets you enable or disable UE-V.</span></span></p></td>
<td align="left"><p><span data-ttu-id="7aaa8-176">Aktivieren oder Deaktivieren dieser Gruppenrichtlinieneinstellung.</span><span class="sxs-lookup"><span data-stu-id="7aaa8-176">Enable or disable this Group Policy setting.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7aaa8-177">VDI-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="7aaa8-177">VDI Configuration</span></span></p></td>
<td align="left"><p><span data-ttu-id="7aaa8-178">Computer und Benutzer</span><span class="sxs-lookup"><span data-stu-id="7aaa8-178">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="7aaa8-179">Mit dieser Richtlinieneinstellung wird die Synchronisierung von UE-V-Rollbackinformationen für Computer konfiguriert, die in einer gepoolten VDI-Umgebung ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="7aaa8-179">This policy setting configures the synchronization of UE-V rollback information for computers running in a pooled VDI environment.</span></span> <span data-ttu-id="7aaa8-180">Wenn diese Richtlinie aktiviert ist, wird der UE-V-Rollbackstatus in den Speicherort der Einstellungen bei der Anmeldung kopiert und bei der Anmeldung wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="7aaa8-180">If this policy is enabled, the UE-V rollback state is copied to the settings storage location on logout and restored on login.</span></span></p></td>
<td align="left"><p><span data-ttu-id="7aaa8-181">Aktivieren oder Deaktivieren dieser Gruppenrichtlinieneinstellung.</span><span class="sxs-lookup"><span data-stu-id="7aaa8-181">Enable or disable this Group Policy setting.</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="7aaa8-182">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="7aaa8-182">Note</span></span>**  
<span data-ttu-id="7aaa8-183">Darüber hinaus sind Gruppenrichtlinieneinstellungen für viele Desktopanwendungen und Windows-Apps verfügbar.</span><span class="sxs-lookup"><span data-stu-id="7aaa8-183">In addition, Group Policy settings are available for many desktop applications and Windows apps.</span></span> <span data-ttu-id="7aaa8-184">Sie können diese Einstellungen verwenden, um die Einstellungssynchronisierung für bestimmte Anwendungen zu aktivieren oder zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="7aaa8-184">You can use these settings to enable or disable settings synchronization for specific applications.</span></span>

 

**<span data-ttu-id="7aaa8-185">Windows App-Gruppenrichtlinieneinstellungen</span><span class="sxs-lookup"><span data-stu-id="7aaa8-185">Windows App Group Policy settings</span></span>**

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="7aaa8-186">Gruppenrichtlinieneinstellungsname</span><span class="sxs-lookup"><span data-stu-id="7aaa8-186">Group Policy setting name</span></span></th>
<th align="left"><span data-ttu-id="7aaa8-187">Ziel</span><span class="sxs-lookup"><span data-stu-id="7aaa8-187">Target</span></span></th>
<th align="left"><span data-ttu-id="7aaa8-188">Beschreibung der Gruppenrichtlinieneinstellung</span><span class="sxs-lookup"><span data-stu-id="7aaa8-188">Group Policy setting description</span></span></th>
<th align="left"><span data-ttu-id="7aaa8-189">Konfigurationsoptionen</span><span class="sxs-lookup"><span data-stu-id="7aaa8-189">Configuration options</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7aaa8-190">Keine Synchronisierung von Windows Apps</span><span class="sxs-lookup"><span data-stu-id="7aaa8-190">Do not synchronize Windows Apps</span></span></p></td>
<td align="left"><p><span data-ttu-id="7aaa8-191">Computer und Benutzer</span><span class="sxs-lookup"><span data-stu-id="7aaa8-191">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="7aaa8-192">Diese Gruppenrichtlinieneinstellung definiert, ob der UE-V-Agent Einstellungen für Windows-Apps synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="7aaa8-192">This Group Policy setting defines whether the UE-V Agent synchronizes settings for Windows apps.</span></span></p></td>
<td align="left"><p><span data-ttu-id="7aaa8-193">Die Standardeinstellung ist die Synchronisierung von Windows-Apps.</span><span class="sxs-lookup"><span data-stu-id="7aaa8-193">The default is to synchronize Windows apps.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7aaa8-194">Windows-App-Liste</span><span class="sxs-lookup"><span data-stu-id="7aaa8-194">Windows App List</span></span></p></td>
<td align="left"><p><span data-ttu-id="7aaa8-195">Computer und Benutzer</span><span class="sxs-lookup"><span data-stu-id="7aaa8-195">Computer and User</span></span></p></td>
<td align="left"><p><span data-ttu-id="7aaa8-196">Diese Einstellung listet die Familienpaketnamen der Windows-Apps auf und gibt ausdrücklich an, ob UE-V die Einstellungen dieser App synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="7aaa8-196">This setting lists the family package names of the Windows apps and states expressly whether UE-V synchronizes that app’s settings.</span></span></p></td>
<td align="left"><p><span data-ttu-id="7aaa8-197">Sie können diese Einstellung verwenden, um anzugeben, dass die Einstellungen einer App niemals von UE-V synchronisiert werden, auch wenn die Einstellungen aller anderen Windows-Apps synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="7aaa8-197">You can use this setting to specify that settings of an app are never synchronized by UE-V, even if the settings of all other Windows apps are synchronized.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7aaa8-198">Synchronisieren nicht aufgelisteter Windows Apps</span><span class="sxs-lookup"><span data-stu-id="7aaa8-198">Sync Unlisted Windows Apps</span></span></p></td>
<td align="left"><p><span data-ttu-id="7aaa8-199">Computer und Benutzer</span><span class="sxs-lookup"><span data-stu-id="7aaa8-199">Computer and User</span></span></p></td>
<td align="left"><p><span data-ttu-id="7aaa8-200">Diese Gruppenrichtlinieneinstellung definiert das Synchronisierungsverhalten der Standardeinstellungen des UE-V-Agents für Windows-Apps, die nicht explizit in der Windows-App-Liste aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="7aaa8-200">This Group Policy setting defines the default settings sync behavior of the UE-V Agent for Windows apps that are not explicitly listed in the Windows app list.</span></span></p></td>
<td align="left"><p><span data-ttu-id="7aaa8-201">Standardmäßig synchronisiert der UE-V-Agent nur die Einstellungen der Windows-Apps, die in der Windows-App-Liste enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="7aaa8-201">By default, the UE-V Agent only synchronizes settings of those Windows apps that are included in the Windows app list.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="7aaa8-202">Weitere Informationen zum Synchronisieren von Windows-Apps finden Sie unter [Windows App List](https://technet.microsoft.com/library/dn458925.aspx#win8applist).</span><span class="sxs-lookup"><span data-stu-id="7aaa8-202">For more information about synchronizing Windows apps, see [Windows App List](https://technet.microsoft.com/library/dn458925.aspx#win8applist).</span></span>

**<span data-ttu-id="7aaa8-203">So konfigurieren Sie computerorientierte Gruppenrichtlinieneinstellungen</span><span class="sxs-lookup"><span data-stu-id="7aaa8-203">To configure computer-targeted Group Policy settings</span></span>**

1.  <span data-ttu-id="7aaa8-204">Verwenden Sie die Gruppenrichtlinienverwaltungskonsole (Group Policy Management Console, GPMC) oder die erweiterte Gruppenrichtlinienverwaltung (Advanced Group Policy Management, AGPM) auf dem Computer, der als Domänencontroller fungiert, um Gruppenrichtlinieneinstellungen für UE-V-Computer zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="7aaa8-204">Use the Group Policy Management Console (GPMC) or the Advanced Group Policy Management (AGPM) on the computer that acts as a domain controller to manage Group Policy settings for UE-V computers.</span></span> <span data-ttu-id="7aaa8-205">Navigieren Sie **zu Computerkonfiguration,** wählen **Sie Richtlinien**aus, wählen Sie Administrative **Vorlagen aus,** klicken Sie auf **Windows-Komponenten,** und wählen Sie dann Microsoft User Experience Virtualization **aus.**</span><span class="sxs-lookup"><span data-stu-id="7aaa8-205">Navigate to **Computer configuration**, select **Policies**, select **Administrative Templates**, click **Windows Components**, and then select **Microsoft User Experience Virtualization**.</span></span>

2.  <span data-ttu-id="7aaa8-206">Wählen Sie die Zu bearbeitende Gruppenrichtlinieneinstellung aus.</span><span class="sxs-lookup"><span data-stu-id="7aaa8-206">Select the Group Policy setting to be edited.</span></span>

**<span data-ttu-id="7aaa8-207">So konfigurieren Sie benutzerorientierte Gruppenrichtlinieneinstellungen</span><span class="sxs-lookup"><span data-stu-id="7aaa8-207">To configure user-targeted Group Policy settings</span></span>**

1.  <span data-ttu-id="7aaa8-208">Verwenden Sie die Gruppenrichtlinienverwaltungskonsole (Group Policy Management Console, GPMC) oder das Tool für die erweiterte Gruppenrichtlinienverwaltung (Advanced Group Policy Management, AGPM) in Microsoft Desktop Optimization Pack (MDOP) auf dem Domänencontrollercomputer, um Gruppenrichtlinieneinstellungen für UE-V zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="7aaa8-208">Use the Group Policy Management Console (GPMC) or the Advanced Group Policy Management (AGPM) tool in Microsoft Desktop Optimization Pack (MDOP) on the domain controller computer to manage Group Policy settings for UE-V.</span></span> <span data-ttu-id="7aaa8-209">Navigieren Sie **zu Benutzerkonfiguration,** wählen **Sie Richtlinien**aus, wählen Sie Administrative **Vorlagen aus,** klicken Sie auf Windows-Komponenten, und wählen Sie **dann Microsoft User Experience Virtualization aus.** \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="7aaa8-209">Navigate to **User configuration**, select **Policies**, select **Administrative Templates**, click **Windows Components**, and then select **Microsoft User Experience Virtualization**.</span></span>

2.  <span data-ttu-id="7aaa8-210">Wählen Sie die bearbeitete Gruppenrichtlinieneinstellung aus.</span><span class="sxs-lookup"><span data-stu-id="7aaa8-210">Select the edited Group Policy setting.</span></span>

<span data-ttu-id="7aaa8-211">Der UE-V-Agent verwendet die folgende Rangfolge, um die Synchronisierung zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="7aaa8-211">The UE-V Agent uses the following order of precedence to determine synchronization.</span></span>

**<span data-ttu-id="7aaa8-212">Rangfolge für UE-V-Einstellungen</span><span class="sxs-lookup"><span data-stu-id="7aaa8-212">Order of precedence for UE-V settings</span></span>**

1.  <span data-ttu-id="7aaa8-213">Benutzerorientierte Einstellungen, die von Gruppenrichtlinieneinstellungen verwaltet werden – Diese Konfigurationseinstellungen werden im Registrierungsschlüssel von der Gruppenrichtlinie unter `HKEY_CURRENT_USER\Software\Policies\Microsoft\Uev\Agent\Configuration` gespeichert.</span><span class="sxs-lookup"><span data-stu-id="7aaa8-213">User-targeted settings that are managed by Group Policy settings - These configuration settings are stored in the registry key by Group Policy under `HKEY_CURRENT_USER\Software\Policies\Microsoft\Uev\Agent\Configuration`.</span></span>

2.  <span data-ttu-id="7aaa8-214">Computerorientierte Einstellungen, die von Gruppenrichtlinieneinstellungen verwaltet werden – Diese Konfigurationseinstellungen werden im Registrierungsschlüssel von der Gruppenrichtlinie unter `HKEY_LOCAL_MACHINE\Software\Policies\Microsoft\Uev\Agent\Configuration` gespeichert.</span><span class="sxs-lookup"><span data-stu-id="7aaa8-214">Computer-targeted settings that are managed by Group Policy settings - These configuration settings are stored in the registry key by Group Policy under `HKEY_LOCAL_MACHINE\Software\Policies\Microsoft\Uev\Agent\Configuration`.</span></span>

3.  <span data-ttu-id="7aaa8-215">Konfigurationseinstellungen, die vom aktuellen Benutzer mithilfe von Windows PowerShell oder Windows Management Instrumentation (WMI) definiert werden – Diese Konfigurationseinstellungen werden vom UE-V-Agent unter diesem Registrierungsspeicherort gespeichert: `HKEY_CURRENT_USER\Software\Microsoft\Uev\Agent\Configuration` .</span><span class="sxs-lookup"><span data-stu-id="7aaa8-215">Configuration settings that are defined by the current user by using Windows PowerShell or Windows management Instrumentation (WMI) - These configuration settings are stored by the UE-V Agent under this registry location: `HKEY_CURRENT_USER\Software\Microsoft\Uev\Agent\Configuration`.</span></span>

4.  <span data-ttu-id="7aaa8-216">Konfigurationseinstellungen, die für den Computer mithilfe von Windows PowerShell oder WMI definiert werden.</span><span class="sxs-lookup"><span data-stu-id="7aaa8-216">Configuration settings that are defined for the computer by using Windows PowerShell or WMI.</span></span> <span data-ttu-id="7aaa8-217">Diese Konfigurationseinstellungen werden vom UE-V-Agent unter diesem Registrierungsspeicherort gespeichert: `HKEY_LOCAL_MACHINE\Software\Microsoft\Uev\Agent\Configuration` .</span><span class="sxs-lookup"><span data-stu-id="7aaa8-217">These configuration settings are stored by the UE-V Agent under this registry location: `HKEY_LOCAL_MACHINE\Software\Microsoft\Uev\Agent\Configuration`.</span></span>

    <span data-ttu-id="7aaa8-218">**Haben Sie einen Vorschlag für UE-V ?**</span><span class="sxs-lookup"><span data-stu-id="7aaa8-218">**Got a suggestion for UE-V**?</span></span> <span data-ttu-id="7aaa8-219">Fügen Sie hier Vorschläge hinzu, oder stimmen Sie [über diese ab.](http://uev.uservoice.com/forums/280428-microsoft-user-experience-virtualization)</span><span class="sxs-lookup"><span data-stu-id="7aaa8-219">Add or vote on suggestions [here](http://uev.uservoice.com/forums/280428-microsoft-user-experience-virtualization).</span></span> <span data-ttu-id="7aaa8-220">**Haben Sie ein UE-V-Problem?**</span><span class="sxs-lookup"><span data-stu-id="7aaa8-220">**Got a UE-V issue**?</span></span> <span data-ttu-id="7aaa8-221">Verwenden Sie [das UE-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopuev).</span><span class="sxs-lookup"><span data-stu-id="7aaa8-221">Use the [UE-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopuev).</span></span>

## <a name="related-topics"></a><span data-ttu-id="7aaa8-222">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="7aaa8-222">Related topics</span></span>


[<span data-ttu-id="7aaa8-223">Verwalten von UE-V 2.x</span><span class="sxs-lookup"><span data-stu-id="7aaa8-223">Administering UE-V 2.x</span></span>](administering-ue-v-2x-new-uevv2.md)

[<span data-ttu-id="7aaa8-224">Verwalten von Konfigurationen für UE-V 2.x</span><span class="sxs-lookup"><span data-stu-id="7aaa8-224">Manage Configurations for UE-V 2.x</span></span>](manage-configurations-for-ue-v-2x-new-uevv2.md)

 

 
