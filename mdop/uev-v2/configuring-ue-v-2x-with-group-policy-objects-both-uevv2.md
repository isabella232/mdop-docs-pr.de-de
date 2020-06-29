---
title: Konfigurieren von UE-V 2. x mit Gruppenrichtlinienobjekten
description: Konfigurieren von UE-V 2. x mit Gruppenrichtlinienobjekten
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
ms.openlocfilehash: bdff63b948752b9bec83e77e275f1cb20a384463
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810546"
---
# <span data-ttu-id="2af0b-103">Konfigurieren von UE-V 2. x mit Gruppenrichtlinienobjekten</span><span class="sxs-lookup"><span data-stu-id="2af0b-103">Configuring UE-V 2.x with Group Policy Objects</span></span>


<span data-ttu-id="2af0b-104">Einige Gruppenrichtlinieneinstellungen für Microsoft User Experience Virtualization (UE-V) 2,0, 2,1 und 2,1 SP1 können für Computer definiert werden, und andere Gruppenrichtlinieneinstellungen können für benutzerdefiniert werden.</span><span class="sxs-lookup"><span data-stu-id="2af0b-104">Some Microsoft User Experience Virtualization (UE-V) 2.0, 2.1, and 2.1 SP1 Group Policy settings can be defined for computers, and other Group Policy settings can be defined for users.</span></span> <span data-ttu-id="2af0b-105">Informationen zum Installieren von ADMX-Dateien für UE-v-Gruppenrichtlinien finden Sie unter [Installieren der ADMX-Vorlagen für Gruppenrichtlinien für UE-v 2](https://technet.microsoft.com/library/dn458891.aspx#admx).</span><span class="sxs-lookup"><span data-stu-id="2af0b-105">For information about how to install UE-V Group Policy ADMX files, see [Installing the UE-V 2 Group Policy ADMX Templates](https://technet.microsoft.com/library/dn458891.aspx#admx).</span></span>

<span data-ttu-id="2af0b-106">Die folgenden Richtlinieneinstellungen können für UE-V konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="2af0b-106">The following policy settings can be configured for UE-V.</span></span>

**<span data-ttu-id="2af0b-107">Gruppenrichtlinieneinstellungen</span><span class="sxs-lookup"><span data-stu-id="2af0b-107">Group Policy settings</span></span>**

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="2af0b-108">Name der Gruppenrichtlinieneinstellung</span><span class="sxs-lookup"><span data-stu-id="2af0b-108">Group Policy setting name</span></span></th>
<th align="left"><span data-ttu-id="2af0b-109">Ziel</span><span class="sxs-lookup"><span data-stu-id="2af0b-109">Target</span></span></th>
<th align="left"><span data-ttu-id="2af0b-110">Beschreibung der Gruppenrichtlinieneinstellung</span><span class="sxs-lookup"><span data-stu-id="2af0b-110">Group Policy setting description</span></span></th>
<th align="left"><span data-ttu-id="2af0b-111">Konfigurationsoptionen</span><span class="sxs-lookup"><span data-stu-id="2af0b-111">Configuration options</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2af0b-112">Kontakt mit dem Link Text</span><span class="sxs-lookup"><span data-stu-id="2af0b-112">Contact IT Link Text</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af0b-113">Nur Computer</span><span class="sxs-lookup"><span data-stu-id="2af0b-113">Computers Only</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af0b-114">Diese Gruppenrichtlinieneinstellung gibt den Text des Links für die URL der Kontaktadresse im Unternehmenseinstellungen-Center an.</span><span class="sxs-lookup"><span data-stu-id="2af0b-114">This Group Policy setting specifies the text of the Contact IT URL hyperlink in the Company Settings Center.</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af0b-115">Wenn Sie diese Gruppenrichtlinieneinstellung aktivieren, wird im Unternehmens Einstellungs Center der angegebene Text im Link zur URL des Kontakts angezeigt.</span><span class="sxs-lookup"><span data-stu-id="2af0b-115">If you enable this Group Policy setting, the Company Settings Center displays the specified text in the link to the Contact IT URL.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2af0b-116">Kontakt-URL</span><span class="sxs-lookup"><span data-stu-id="2af0b-116">Contact IT URL</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af0b-117">Nur Computer</span><span class="sxs-lookup"><span data-stu-id="2af0b-117">Computers Only</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af0b-118">Diese Gruppenrichtlinieneinstellung gibt die URL für den Link "Kontakt" im Unternehmenseinstellungen-Center an.</span><span class="sxs-lookup"><span data-stu-id="2af0b-118">This Group Policy setting specifies the URL for the Contact IT link in the Company Settings Center.</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af0b-119">Wenn Sie diese Einstellung aktivieren, kontaktiert das Unternehmenseinstellungen-Center die Text-Links zur angegebenen URL.</span><span class="sxs-lookup"><span data-stu-id="2af0b-119">If you enable this setting, the Company Settings Center Contact IT text links to the specified URL.</span></span> <span data-ttu-id="2af0b-120">Der Link kann aus einem beliebigen Standardprotokoll wie http oder mailto sein.</span><span class="sxs-lookup"><span data-stu-id="2af0b-120">The link can be of any standard protocol, such as HTTP or mailto.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2af0b-121">Verwenden Sie nicht den Synchronisierungsanbieter.</span><span class="sxs-lookup"><span data-stu-id="2af0b-121">Do not use the sync provider</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af0b-122">Computer und Benutzer</span><span class="sxs-lookup"><span data-stu-id="2af0b-122">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af0b-123">Mithilfe dieser Gruppenrichtlinieneinstellung können Sie konfigurieren, ob UE-V das Feature "Synchronisierungsanbieter" verwendet.</span><span class="sxs-lookup"><span data-stu-id="2af0b-123">By using this Group Policy setting, you can configure whether UE-V uses the sync provider feature.</span></span> <span data-ttu-id="2af0b-124">Mit dieser Richtlinieneinstellung können Sie auch die Benachrichtigung aktivieren, die angezeigt wird, wenn der Import von Benutzereinstellungen verzögert wird.</span><span class="sxs-lookup"><span data-stu-id="2af0b-124">This policy setting also lets you enable notification to appear when the import of user settings is delayed.</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af0b-125">Aktivieren Sie diese Einstellung, um den UE-V-Agent so zu konfigurieren, dass der Synchronisierungsanbieter nicht verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="2af0b-125">Enable this setting to configure the UE-V Agent not to use the sync provider.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2af0b-126">Benachrichtigung zur ersten Verwendung</span><span class="sxs-lookup"><span data-stu-id="2af0b-126">First Use Notification</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af0b-127">Nur Computer</span><span class="sxs-lookup"><span data-stu-id="2af0b-127">Computers Only</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af0b-128">Diese Gruppenrichtlinieneinstellung aktiviert eine Benachrichtigung im Infobereich, die angezeigt wird, wenn die UE-V</span><span class="sxs-lookup"><span data-stu-id="2af0b-128">This Group Policy setting enables a notification in the notification area that appears when the UE-V</span></span></p>
<p><span data-ttu-id="2af0b-129">der Agent wird zum ersten Mal ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2af0b-129">agent runs for the first time.</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af0b-130">Der Standardwert ist aktiviert.</span><span class="sxs-lookup"><span data-stu-id="2af0b-130">The default is enabled.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2af0b-131">Roaming-Windows-Einstellungen</span><span class="sxs-lookup"><span data-stu-id="2af0b-131">Roam Windows settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af0b-132">Computer und Benutzer</span><span class="sxs-lookup"><span data-stu-id="2af0b-132">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af0b-133">Diese Gruppenrichtlinieneinstellung konfiguriert die Synchronisierung von Windows-Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="2af0b-133">This Group Policy setting configures the synchronization of Windows settings.</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af0b-134">Wählen Sie aus, welche Windows-Einstellungen zwischen Computern synchronisiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="2af0b-134">Select which Windows settings synchronize between computers.</span></span></p>
<p><span data-ttu-id="2af0b-135">Standardmäßig werden in Windows-Designs, Desktopeinstellungen und Einstellungen für den erleichterten Zugriff Einstellungen zwischen Computern der gleichen Betriebssystemversion synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="2af0b-135">By default, Windows themes, desktop settings, and Ease of Access settings synchronize settings between computers of the same operating system version.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2af0b-136">Warnungsschwellenwert für Einstellungen-Paketgröße</span><span class="sxs-lookup"><span data-stu-id="2af0b-136">Settings package size warning threshold</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af0b-137">Computer und Benutzer</span><span class="sxs-lookup"><span data-stu-id="2af0b-137">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af0b-138">Mit dieser Gruppenrichtlinieneinstellung können Sie den UE-V-Agent so konfigurieren, dass er meldet, wenn die Dateigröße eines Einstellungen-Pakets einen festgelegten Schwellenwert erreicht.</span><span class="sxs-lookup"><span data-stu-id="2af0b-138">This Group Policy setting lets you configure the UE-V Agent to report when a settings package file size reaches a defined threshold.</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af0b-139">Geben Sie den bevorzugten Schwellenwert für die Größe des Einstellungs Pakets in Kilobyte (KB) an.</span><span class="sxs-lookup"><span data-stu-id="2af0b-139">Specify the preferred threshold for settings package sizes in kilobytes (KB).</span></span></p>
<p><span data-ttu-id="2af0b-140">Standardmäßig hat der UE-V-Agent keinen Schwellenwert für die Paketdatei Größe.</span><span class="sxs-lookup"><span data-stu-id="2af0b-140">By default, the UE-V Agent does not have a package file size threshold.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2af0b-141">Speicherpfad für Einstellungen</span><span class="sxs-lookup"><span data-stu-id="2af0b-141">Settings storage path</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af0b-142">Computer und Benutzer</span><span class="sxs-lookup"><span data-stu-id="2af0b-142">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af0b-143">Diese Gruppenrichtlinieneinstellung konfiguriert, wo die Benutzereinstellungen gespeichert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="2af0b-143">This Group Policy setting configures where the user settings are to be stored.</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af0b-144">Geben Sie einen UNC-Pfad (Universal Naming Convention) und Variablen wie \Server\SettingsShare%username%.</span><span class="sxs-lookup"><span data-stu-id="2af0b-144">Enter a Universal Naming Convention (UNC) path and variables such as \Server\SettingsShare%username%.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2af0b-145">Katalogpfad für Einstellungs Vorlagen</span><span class="sxs-lookup"><span data-stu-id="2af0b-145">Settings template catalog path</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af0b-146">Nur Computer</span><span class="sxs-lookup"><span data-stu-id="2af0b-146">Computers Only</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af0b-147">Diese Gruppenrichtlinieneinstellung konfiguriert, wo die Speicherort Vorlagen für benutzerdefinierte Einstellungen gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="2af0b-147">This Group Policy setting configures where custom settings location templates are stored.</span></span> <span data-ttu-id="2af0b-148">Mit dieser Richtlinieneinstellung wird auch konfiguriert, ob der Katalog zum Ersetzen der Microsoft-Standardvorlagen verwendet werden soll, die mit dem UE-V-Agent installiert werden.</span><span class="sxs-lookup"><span data-stu-id="2af0b-148">This policy setting also configures whether the catalog is to be used to replace the default Microsoft templates that are installed with the UE-V Agent.</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af0b-149">Geben Sie einen UNC-Pfad (Universal Naming Convention) wie \Server\TemplateShare oder einen Ordnerspeicherort auf dem Computer ein.</span><span class="sxs-lookup"><span data-stu-id="2af0b-149">Enter a Universal Naming Convention (UNC) path such as \Server\TemplateShare or a folder location on the computer.</span></span></p>
<p><span data-ttu-id="2af0b-150">Aktivieren Sie das Kontrollkästchen, um die standardmäßigen Microsoft-Vorlagen zu ersetzen.</span><span class="sxs-lookup"><span data-stu-id="2af0b-150">Select the check box to replace the default Microsoft templates.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2af0b-151">Synchronisierungseinstellungen über getaktete Verbindungen</span><span class="sxs-lookup"><span data-stu-id="2af0b-151">Sync settings over metered connections</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af0b-152">Computer und Benutzer</span><span class="sxs-lookup"><span data-stu-id="2af0b-152">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af0b-153">Diese Gruppenrichtlinieneinstellung legt fest, ob UE-V Einstellungen über getaktete Verbindungen synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="2af0b-153">This Group Policy setting defines whether UE-V synchronizes settings over metered connections.</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af0b-154">Standardmäßig synchronisiert der UE-V-Agent die Einstellungen nicht über eine getaktete Verbindung.</span><span class="sxs-lookup"><span data-stu-id="2af0b-154">By default, the UE-V Agent does not synchronize settings over a metered connection.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2af0b-155">Synchronisierungseinstellungen über getaktete Verbindungen auch beim Roaming</span><span class="sxs-lookup"><span data-stu-id="2af0b-155">Sync settings over metered connections even when roaming</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af0b-156">Computer und Benutzer</span><span class="sxs-lookup"><span data-stu-id="2af0b-156">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af0b-157">Diese Gruppenrichtlinieneinstellung legt fest, ob UE-V Einstellungen über getaktete Verbindungen außerhalb des Home-Provider-Netzwerks synchronisiert, beispielsweise, wenn sich die Datenverbindung im roamingmodus befindet.</span><span class="sxs-lookup"><span data-stu-id="2af0b-157">This Group Policy setting defines whether UE-V synchronizes settings over metered connections outside of the home provider network, for example, when the data connection is in roaming mode.</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af0b-158">Standardmäßig synchronisiert UE-V die Einstellungen für eine getaktete Verbindung nicht, wenn sich der Roaming-Modus befindet.</span><span class="sxs-lookup"><span data-stu-id="2af0b-158">By default, UE-V does not synchronize settings over a metered connection when it is in roaming mode.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2af0b-159">Synchronisierungs Timeout</span><span class="sxs-lookup"><span data-stu-id="2af0b-159">Synchronization timeout</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af0b-160">Computer und Benutzer</span><span class="sxs-lookup"><span data-stu-id="2af0b-160">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af0b-161">Mit dieser Gruppenrichtlinieneinstellung wird die Anzahl der Millisekunden konfiguriert, die der Computer vor einem Timeout wartet, wenn er Benutzereinstellungen vom Speicherort der Remoteeinstellungen abruft.</span><span class="sxs-lookup"><span data-stu-id="2af0b-161">This Group Policy setting configures the number of milliseconds that the computer waits before a time-out when it retrieves user settings from the remote settings location.</span></span> <span data-ttu-id="2af0b-162">Wenn der Remotespeicher Standort nicht verfügbar ist und der Benutzer den Synchronisierungsanbieter nicht verwendet, wird der Anwendungsstart um diese Zahl von Millisekunden verzögert.</span><span class="sxs-lookup"><span data-stu-id="2af0b-162">If the remote storage location is unavailable, and the user does not use the sync provider, the application start is delayed by this many milliseconds.</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af0b-163">Geben Sie das bevorzugte Synchronisierungs Timeout in Millisekunden an.</span><span class="sxs-lookup"><span data-stu-id="2af0b-163">Specify the preferred synchronization time-out in milliseconds.</span></span> <span data-ttu-id="2af0b-164">Der Standardwert ist 2000 Millisekunden.</span><span class="sxs-lookup"><span data-stu-id="2af0b-164">The default value is 2000 milliseconds.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2af0b-165">Taskleistensymbol</span><span class="sxs-lookup"><span data-stu-id="2af0b-165">Tray Icon</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af0b-166">Nur Computer</span><span class="sxs-lookup"><span data-stu-id="2af0b-166">Computers Only</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af0b-167">Diese Gruppenrichtlinieneinstellung aktiviert das Taskleistensymbol für die Benutzeroberflächen-Virtualisierung (UE-V).</span><span class="sxs-lookup"><span data-stu-id="2af0b-167">This Group Policy setting enables the User Experience Virtualization (UE-V) tray icon.</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af0b-168">Der Standardwert ist aktiviert.</span><span class="sxs-lookup"><span data-stu-id="2af0b-168">The default is enabled.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2af0b-169">Verwenden der Benutzeroberflächen-Virtualisierung (UE-V)</span><span class="sxs-lookup"><span data-stu-id="2af0b-169">Use User Experience Virtualization (UE-V)</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af0b-170">Computer und Benutzer</span><span class="sxs-lookup"><span data-stu-id="2af0b-170">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af0b-171">Mit dieser Gruppenrichtlinieneinstellung können Sie die Virtualisierung der Benutzeroberfläche (UE-V) aktivieren oder deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="2af0b-171">This Group Policy setting lets you enable or disable User Experience Virtualization (UE-V).</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af0b-172">Aktivieren oder deaktivieren Sie diese Gruppenrichtlinieneinstellung.</span><span class="sxs-lookup"><span data-stu-id="2af0b-172">Enable or disable this Group Policy setting.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="2af0b-173">**Hinweis**  Darüber hinaus stehen Gruppenrichtlinieneinstellungen für viele Desktopanwendungen und Windows-Apps zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="2af0b-173">**Note** In addition, Group Policy settings are available for many desktop applications and Windows apps.</span></span> <span data-ttu-id="2af0b-174">Sie können diese Einstellungen verwenden, um die Synchronisierung von Einstellungen für bestimmte Anwendungen zu aktivieren oder zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="2af0b-174">You can use these settings to enable or disable settings synchronization for specific applications.</span></span>

 

**<span data-ttu-id="2af0b-175">Gruppenrichtlinieneinstellungen für Windows-apps</span><span class="sxs-lookup"><span data-stu-id="2af0b-175">Windows App Group Policy settings</span></span>**

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="2af0b-176">Name der Gruppenrichtlinieneinstellung</span><span class="sxs-lookup"><span data-stu-id="2af0b-176">Group Policy setting name</span></span></th>
<th align="left"><span data-ttu-id="2af0b-177">Ziel</span><span class="sxs-lookup"><span data-stu-id="2af0b-177">Target</span></span></th>
<th align="left"><span data-ttu-id="2af0b-178">Beschreibung der Gruppenrichtlinieneinstellung</span><span class="sxs-lookup"><span data-stu-id="2af0b-178">Group Policy setting description</span></span></th>
<th align="left"><span data-ttu-id="2af0b-179">Konfigurationsoptionen</span><span class="sxs-lookup"><span data-stu-id="2af0b-179">Configuration options</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2af0b-180">Windows-apps nicht synchronisieren</span><span class="sxs-lookup"><span data-stu-id="2af0b-180">Do not synchronize Windows Apps</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af0b-181">Computer und Benutzer</span><span class="sxs-lookup"><span data-stu-id="2af0b-181">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af0b-182">Diese Gruppenrichtlinieneinstellung legt fest, ob der UE-V-Agent die Einstellungen für Windows-apps synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="2af0b-182">This Group Policy setting defines whether the UE-V Agent synchronizes settings for Windows apps.</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af0b-183">Standardmäßig werden Windows-apps synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="2af0b-183">The default is to synchronize Windows apps.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2af0b-184">Windows-App-Liste</span><span class="sxs-lookup"><span data-stu-id="2af0b-184">Windows App List</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af0b-185">Computer und Benutzer</span><span class="sxs-lookup"><span data-stu-id="2af0b-185">Computer and User</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af0b-186">Mit dieser Einstellung werden die Familienpaket Namen der Windows-apps aufgelistet, und es wird ausdrücklich angegeben, ob UE-V die Einstellungen dieser APP synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="2af0b-186">This setting lists the family package names of the Windows apps and states expressly whether UE-V synchronizes that app’s settings.</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af0b-187">Mit dieser Einstellung können Sie festlegen, dass die Einstellungen einer APP nie von UE-V synchronisiert werden, selbst wenn die Einstellungen aller anderen Windows-apps synchronisiert sind.</span><span class="sxs-lookup"><span data-stu-id="2af0b-187">You can use this setting to specify that settings of an app are never synchronized by UE-V, even if the settings of all other Windows apps are synchronized.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2af0b-188">Synchronisieren nicht aufgelisteter Windows-apps</span><span class="sxs-lookup"><span data-stu-id="2af0b-188">Sync Unlisted Windows Apps</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af0b-189">Computer und Benutzer</span><span class="sxs-lookup"><span data-stu-id="2af0b-189">Computer and User</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af0b-190">Diese Gruppenrichtlinieneinstellung definiert das Standardeinstellungen-Synchronisierungsverhalten des UE-V-Agents für Windows-apps, die nicht explizit in der Windows-App-Liste aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="2af0b-190">This Group Policy setting defines the default settings sync behavior of the UE-V Agent for Windows apps that are not explicitly listed in the Windows app list.</span></span></p></td>
<td align="left"><p><span data-ttu-id="2af0b-191">Standardmäßig synchronisiert der UE-V-Agent nur die Einstellungen dieser Windows-apps, die in der Windows-App-Liste enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="2af0b-191">By default, the UE-V Agent only synchronizes settings of those Windows apps that are included in the Windows app list.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="2af0b-192">Weitere Informationen zum Synchronisieren von Windows-apps finden Sie unter [Windows-App-Liste](https://technet.microsoft.com/library/dn458925.aspx#win8applist).</span><span class="sxs-lookup"><span data-stu-id="2af0b-192">For more information about synchronizing Windows apps, see [Windows App List](https://technet.microsoft.com/library/dn458925.aspx#win8applist).</span></span>

**<span data-ttu-id="2af0b-193">So konfigurieren Sie computerbezogene Gruppenrichtlinieneinstellungen</span><span class="sxs-lookup"><span data-stu-id="2af0b-193">To configure computer-targeted Group Policy settings</span></span>**

1.  <span data-ttu-id="2af0b-194">Verwenden Sie die Gruppenrichtlinien-Verwaltungskonsole (Group Policy Management Console, GPMC) oder die erweiterte Gruppenrichtlinienverwaltung (Group Policy Management, AGPM) auf dem Computer, der als Domänencontroller fungiert, um Gruppenrichtlinieneinstellungen für UE-V-Computer zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="2af0b-194">Use the Group Policy Management Console (GPMC) or the Advanced Group Policy Management (AGPM) on the computer that acts as a domain controller to manage Group Policy settings for UE-V computers.</span></span> <span data-ttu-id="2af0b-195">Navigieren Sie zu **Computer Konfiguration**, wählen Sie **Richtlinien**aus, wählen Sie **Administrative Vorlagen**aus, klicken Sie auf **Windows-Komponenten**, und wählen Sie dann **Microsoft User Experience Virtualization**aus.</span><span class="sxs-lookup"><span data-stu-id="2af0b-195">Navigate to **Computer configuration**, select **Policies**, select **Administrative Templates**, click **Windows Components**, and then select **Microsoft User Experience Virtualization**.</span></span>

2.  <span data-ttu-id="2af0b-196">Wählen Sie die zu bearbeitende Gruppenrichtlinieneinstellung aus.</span><span class="sxs-lookup"><span data-stu-id="2af0b-196">Select the Group Policy setting to be edited.</span></span>

**<span data-ttu-id="2af0b-197">So konfigurieren Sie benutzerbezogene Gruppenrichtlinieneinstellungen</span><span class="sxs-lookup"><span data-stu-id="2af0b-197">To configure user-targeted Group Policy settings</span></span>**

1.  <span data-ttu-id="2af0b-198">Verwenden Sie die Gruppenrichtlinien-Verwaltungskonsole (Group Policy Management Console, GPMC) oder das erweiterte Tool für die Gruppenrichtlinienverwaltung (AGPM) im Microsoft Desktop Optimization Pack (MDOP) auf dem Domänencontrollercomputer, um die Gruppenrichtlinieneinstellungen für UE-V zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="2af0b-198">Use the Group Policy Management Console (GPMC) or the Advanced Group Policy Management (AGPM) tool in Microsoft Desktop Optimization Pack (MDOP) on the domain controller computer to manage Group Policy settings for UE-V.</span></span> <span data-ttu-id="2af0b-199">Navigieren Sie zu **Benutzerkonfiguration**, wählen Sie **Richtlinien**aus, wählen Sie **Administrative Vorlagen**aus, klicken Sie auf **Windows-Komponenten**, und wählen Sie dann **Microsoft User Experience Virtualization**aus.</span><span class="sxs-lookup"><span data-stu-id="2af0b-199">Navigate to **User configuration**, select **Policies**, select **Administrative Templates**, click **Windows Components**, and then select **Microsoft User Experience Virtualization**.</span></span>

2.  <span data-ttu-id="2af0b-200">Wählen Sie die bearbeitete Gruppenrichtlinieneinstellung aus.</span><span class="sxs-lookup"><span data-stu-id="2af0b-200">Select the edited Group Policy setting.</span></span>

<span data-ttu-id="2af0b-201">Der UE-V-Agent verwendet die folgende Rangfolge, um die Synchronisierung zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="2af0b-201">The UE-V Agent uses the following order of precedence to determine synchronization.</span></span>

**<span data-ttu-id="2af0b-202">Rangfolge der UE-V-Einstellungen</span><span class="sxs-lookup"><span data-stu-id="2af0b-202">Order of precedence for UE-V settings</span></span>**

1.  <span data-ttu-id="2af0b-203">Benutzerbezogene Einstellungen, die von Gruppenrichtlinieneinstellungen verwaltet werden – diese Konfigurationseinstellungen werden im Registrierungsschlüssel nach Gruppenrichtlinie unter gespeichert `HKEY_CURRENT_USER\Software\Policies\Microsoft\Uev\Agent\Configuration` .</span><span class="sxs-lookup"><span data-stu-id="2af0b-203">User-targeted settings that are managed by Group Policy settings - These configuration settings are stored in the registry key by Group Policy under `HKEY_CURRENT_USER\Software\Policies\Microsoft\Uev\Agent\Configuration`.</span></span>

2.  <span data-ttu-id="2af0b-204">Computer gesteuerte Einstellungen, die von Gruppenrichtlinieneinstellungen verwaltet werden – diese Konfigurationseinstellungen werden im Registrierungsschlüssel nach Gruppenrichtlinie unter gespeichert `HKEY_LOCAL_MACHINE\Software\Policies\Microsoft\Uev\Agent\Configuration` .</span><span class="sxs-lookup"><span data-stu-id="2af0b-204">Computer-targeted settings that are managed by Group Policy settings - These configuration settings are stored in the registry key by Group Policy under `HKEY_LOCAL_MACHINE\Software\Policies\Microsoft\Uev\Agent\Configuration`.</span></span>

3.  <span data-ttu-id="2af0b-205">Konfigurationseinstellungen, die vom aktuellen Benutzer mithilfe von Windows PowerShell oder Windows-Verwaltungsinstrumentation (WMI) definiert werden – diese Konfigurationseinstellungen werden vom UE-V-Agent unter diesem Registrierungsspeicherort gespeichert: `HKEY_CURRENT_USER\Software\Microsoft\Uev\Agent\Configuration` .</span><span class="sxs-lookup"><span data-stu-id="2af0b-205">Configuration settings that are defined by the current user by using Windows PowerShell or Windows management Instrumentation (WMI) - These configuration settings are stored by the UE-V Agent under this registry location: `HKEY_CURRENT_USER\Software\Microsoft\Uev\Agent\Configuration`.</span></span>

4.  <span data-ttu-id="2af0b-206">Konfigurationseinstellungen, die für den Computer mithilfe von Windows PowerShell oder WMI definiert sind.</span><span class="sxs-lookup"><span data-stu-id="2af0b-206">Configuration settings that are defined for the computer by using Windows PowerShell or WMI.</span></span> <span data-ttu-id="2af0b-207">Diese Konfigurationseinstellungen werden vom UE-V-Agent unter diesem Registrierungsspeicherort `HKEY_LOCAL_MACHINE\Software\Microsoft\Uev\Agent\Configuration` gespeichert:</span><span class="sxs-lookup"><span data-stu-id="2af0b-207">These configuration settings are stored by the UE-V Agent under this registry location: `HKEY_LOCAL_MACHINE\Software\Microsoft\Uev\Agent\Configuration`.</span></span>

    <span data-ttu-id="2af0b-208">Sie **haben einen Vorschlag für UE-V**?</span><span class="sxs-lookup"><span data-stu-id="2af0b-208">**Got a suggestion for UE-V**?</span></span> <span data-ttu-id="2af0b-209">[Hier](http://uev.uservoice.com/forums/280428-microsoft-user-experience-virtualization)können Sie Vorschläge hinzufügen oder abstimmen.</span><span class="sxs-lookup"><span data-stu-id="2af0b-209">Add or vote on suggestions [here](http://uev.uservoice.com/forums/280428-microsoft-user-experience-virtualization).</span></span> <span data-ttu-id="2af0b-210">**Haben Sie ein UE-V-Problem**?</span><span class="sxs-lookup"><span data-stu-id="2af0b-210">**Got a UE-V issue**?</span></span> <span data-ttu-id="2af0b-211">Verwenden Sie das [UE-V TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopuev).</span><span class="sxs-lookup"><span data-stu-id="2af0b-211">Use the [UE-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopuev).</span></span>

## <span data-ttu-id="2af0b-212">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="2af0b-212">Related topics</span></span>


[<span data-ttu-id="2af0b-213">Verwalten von UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="2af0b-213">Administering UE-V 2.x</span></span>](administering-ue-v-2x-new-uevv2.md)

[<span data-ttu-id="2af0b-214">Verwalten von Konfigurationen für UE-V 2.x</span><span class="sxs-lookup"><span data-stu-id="2af0b-214">Manage Configurations for UE-V 2.x</span></span>](manage-configurations-for-ue-v-2x-new-uevv2.md)

 

 





