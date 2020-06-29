---
title: Verwalten des UE-V 2. x-Agents und der Pakete mit Windows PowerShell und WMI
description: Verwalten des UE-V 2. x-Agents und der Pakete mit Windows PowerShell und WMI
author: dansimp
ms.assetid: 56e6780b-8b2c-4717-91c8-2af63062ab75
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 6a709d2c66266cf33b8e89ddd905aa0f21eb7dfe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811974"
---
# <span data-ttu-id="5f897-103">Verwalten des UE-V 2. x-Agents und der Pakete mit Windows PowerShell und WMI</span><span class="sxs-lookup"><span data-stu-id="5f897-103">Managing the UE-V 2.x Agent and Packages with Windows PowerShell and WMI</span></span>


<span data-ttu-id="5f897-104">Sie können Windows-Verwaltungsinstrumentation (WMI) und Windows PowerShell verwenden, um die Konfiguration und das Synchronisierungsverhalten von Microsoft User Experience Virtualization (UE-V) 2,0, 2,1 und 2,1 SP1 zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="5f897-104">You can use Windows Management Instrumentation (WMI) and Windows PowerShell to manage Microsoft User Experience Virtualization (UE-V) 2.0, 2.1, and 2.1 SP1 Agent configuration and synchronization behavior.</span></span> <span data-ttu-id="5f897-105">Eine vollständige Liste der UE-v PowerShell-Cmdlets finden Sie unter [UE-v 2-Cmdlet-Referenz](https://go.microsoft.com/fwlink/?LinkId=393495) ( https://go.microsoft.com/fwlink/?LinkId=393495) .</span><span class="sxs-lookup"><span data-stu-id="5f897-105">For a complete list of UE-V PowerShell cmdlets, see [UE-V 2 Cmdlet Reference](https://go.microsoft.com/fwlink/?LinkId=393495) (https://go.microsoft.com/fwlink/?LinkId=393495).</span></span>

**<span data-ttu-id="5f897-106">Bereitstellen des UE-V-Agents mithilfe von Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="5f897-106">To deploy the UE-V Agent by using Windows PowerShell</span></span>**

1.  <span data-ttu-id="5f897-107">Stufen Sie die UE-V-Installationsdatei in einer barrierefreien Netzwerkfreigabe ein.</span><span class="sxs-lookup"><span data-stu-id="5f897-107">Stage the UE-V installer file in an accessible network share.</span></span>

    **<span data-ttu-id="5f897-108">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="5f897-108">Note</span></span>**  
    <span data-ttu-id="5f897-109">Verwenden Sie AgentSetup.exe, um sowohl 32-Bit-als auch 64-Bit-Versionen des UE-V-Agents bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="5f897-109">Use AgentSetup.exe to deploy both 32-bit and 64-bit versions of the UE-V Agent.</span></span> <span data-ttu-id="5f897-110">Windows Installer-Pakete, AgentSetupx86.msi und AgentSetupx64.msi, stehen für jede Architektur zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="5f897-110">Windows Installer packages, AgentSetupx86.msi and AgentSetupx64.msi, are available for each architecture.</span></span> <span data-ttu-id="5f897-111">Wenn Sie den UE-V-Agent zu einem späteren Zeitpunkt mithilfe der Installationsdatei deinstallieren möchten, müssen Sie denselben Dateityp verwenden.</span><span class="sxs-lookup"><span data-stu-id="5f897-111">To uninstall the UE-V Agent at a later time by using the installation file, you must use the same file type.</span></span>



2.  <span data-ttu-id="5f897-112">Verwenden Sie einen der folgenden Windows PowerShell-Befehle, um den UE-V-Agent zu installieren.</span><span class="sxs-lookup"><span data-stu-id="5f897-112">Use one of the following Windows PowerShell commands to install the UE-V Agent.</span></span>

    -   `& AgentSetup.exe /quiet /norestart /log "%temp%\UE-VAgentInstaller.log" SettingsStoragePath=\\server\settingsshare\%username%`

    -   `& msiexec.exe /i "<path to msi file>" /quiet /norestart /l*v "%temp%\UE-VAgentInstaller.log" SettingsStoragePath=\\server\settingsshare\%username%`

**<span data-ttu-id="5f897-113">So konfigurieren Sie den UE-V-Agent mithilfe von Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="5f897-113">To configure the UE-V Agent by using Windows PowerShell</span></span>**

1. <span data-ttu-id="5f897-114">Öffnen Sie ein Windows PowerShell-Fenster.</span><span class="sxs-lookup"><span data-stu-id="5f897-114">Open a Windows PowerShell window.</span></span> <span data-ttu-id="5f897-115">Öffnen Sie das Fenster mit einem Konto, das über Administratorrechte verfügt, um Computereinstellungen zu verwalten, die sich auf alle Benutzer des Computers auswirken, indem Sie den Parameter *Computer* verwenden.</span><span class="sxs-lookup"><span data-stu-id="5f897-115">To manage computer settings that affect all users of the computer by using the *Computer* parameter, open the window with an account that has administrator rights.</span></span>

2. <span data-ttu-id="5f897-116">Verwenden Sie die folgenden Windows PowerShell-Befehle zum Konfigurieren des Agents.</span><span class="sxs-lookup"><span data-stu-id="5f897-116">Use the following Windows PowerShell commands to configure the agent.</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="5f897-117">Windows PowerShell-Befehl</span><span class="sxs-lookup"><span data-stu-id="5f897-117">Windows PowerShell command</span></span></th>
   <th align="left"><span data-ttu-id="5f897-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5f897-118">Description</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><code>Get-UevConfiguration</code></p>
   <p></p></td>
   <td align="left"><p><span data-ttu-id="5f897-119">Ruft die effektiven Einstellungen des UE-V-Agents ab.</span><span class="sxs-lookup"><span data-stu-id="5f897-119">Gets the effective UE-V Agent settings.</span></span> <span data-ttu-id="5f897-120">Benutzerspezifische Einstellungen haben Vorrang vor den Computereinstellungen.</span><span class="sxs-lookup"><span data-stu-id="5f897-120">User-specific settings have precedence over the computer settings.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Get-UevConfiguration - CurrentComputerUser</code></p>
   <p></p></td>
   <td align="left"><p><span data-ttu-id="5f897-121">Ruft die Einstellungen des UE-V-Agents nur für den aktuellen Benutzer ab.</span><span class="sxs-lookup"><span data-stu-id="5f897-121">Gets the UE-V Agent settings values for the current user only.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Get-UevConfiguration -Computer</code></p></td>
   <td align="left"><p><span data-ttu-id="5f897-122">Ruft die Werte für die Konfigurationseinstellungen des UE-V-Agents für alle Benutzer auf dem Computer ab.</span><span class="sxs-lookup"><span data-stu-id="5f897-122">Gets the UE-V Agent configuration settings values for all users on the computer.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Get-UevConfiguration -Details</code></p></td>
   <td align="left"><p><span data-ttu-id="5f897-123">Ruft die Details für jede Konfigurationseinstellung ab.</span><span class="sxs-lookup"><span data-stu-id="5f897-123">Gets the details for each configuration setting.</span></span> <span data-ttu-id="5f897-124">Zeigt an, wo die Einstellung konfiguriert ist oder ob Sie den Standardwert verwendet.</span><span class="sxs-lookup"><span data-stu-id="5f897-124">Displays where the setting is configured or if it uses the default value.</span></span> <span data-ttu-id="5f897-125">Wird angezeigt, wenn die aktuelle Einstellung gültig ist.</span><span class="sxs-lookup"><span data-stu-id="5f897-125">Is displayed if the current setting is valid.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -Computer –ContactITDescription &lt;IT description&gt;</code></p></td>
   <td align="left"><p><span data-ttu-id="5f897-126">Legt den Text fest, der im Unternehmenseinstellungen-Center für den Link "Hilfe" angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="5f897-126">Sets the text that is displayed in the Company Settings Center for the help link.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration -Computer -ContactITUrl &lt;string&gt;</code></p></td>
   <td align="left"><p><span data-ttu-id="5f897-127">Legt die URL des Links im Unternehmenseinstellungen-Center für den Link Hilfe fest.</span><span class="sxs-lookup"><span data-stu-id="5f897-127">Sets the URL of the link in the Company Settings Center for the help link.</span></span> <span data-ttu-id="5f897-128">Jedes URL-Protokoll kann verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5f897-128">Any URL protocol can be used.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -Computer –EnableDontSyncWindows8AppSettings</code></p></td>
   <td align="left"><p><span data-ttu-id="5f897-129">Konfiguriert den UE-V-Agent so, dass keine Windows-Apps für alle Benutzer auf dem Computer synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="5f897-129">Configures the UE-V Agent to not synchronize any Windows apps for all users on the computer.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration -CurrentComputerUser – EnableDontSyncWindows8AppSettings</code></p></td>
   <td align="left"><p><span data-ttu-id="5f897-130">Konfiguriert den UE-V-Agent so, dass keine Windows-Apps für den aktuellen Computer Benutzer synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="5f897-130">Configures the UE-V Agent to not synchronize any Windows apps for the current computer user.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -Computer –EnableFirstUseNotification</code></p></td>
   <td align="left"><p><span data-ttu-id="5f897-131">Konfiguriert den UE-V-Agent so, dass die Benachrichtigung angezeigt wird, wenn der Agent zum ersten Mal für alle Benutzer auf dem Computer ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5f897-131">Configures the UE-V Agent to display notification the first time the agent runs for all users on the computer.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration -Computer –DisableFirstUseNotification</code></p></td>
   <td align="left"><p><span data-ttu-id="5f897-132">Konfiguriert den UE-V-Agent so, dass keine Benachrichtigung angezeigt wird, wenn der Agent zum ersten Mal für alle Benutzer auf dem Computer ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5f897-132">Configures the UE-V Agent to not display notification the first time that the agent runs for all users on the computer.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -Computer –EnableSettingsImportNotify</code></p></td>
   <td align="left"><p><span data-ttu-id="5f897-133">Konfiguriert den UE-V-Agent so, dass alle Benutzer auf dem Computer benachrichtigt werden, wenn die Synchronisierung der Einstellungen verzögert wird.</span><span class="sxs-lookup"><span data-stu-id="5f897-133">Configures the UE-V Agent to notify all users on the computer when settings synchronization is delayed.</span></span></p>
   <p><span data-ttu-id="5f897-134">Verwenden Sie den <em> DisableSettingsImportNotify </em> -Parameter, um die Benachrichtigung zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="5f897-134">Use the <em>DisableSettingsImportNotify</em> parameter to disable notification.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration - CurrentComputerUser -EnableSettingsImportNotify</code></p></td>
   <td align="left"><p><span data-ttu-id="5f897-135">Konfiguriert den UE-V-Agent so, dass der aktuelle Benutzer benachrichtigt wird, wenn die Synchronisierung der Einstellungen verzögert wird.</span><span class="sxs-lookup"><span data-stu-id="5f897-135">Configures the UE-V Agent to notify the current user when settings synchronization is delayed.</span></span></p>
   <p><span data-ttu-id="5f897-136">Verwenden Sie den <em> DisableSettingsImportNotify </em> -Parameter, um die Benachrichtigung zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="5f897-136">Use the <em>DisableSettingsImportNotify</em> parameter to disable notification.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -Computer –EnableSyncUnlistedWindows8Apps</code></p></td>
   <td align="left"><p><span data-ttu-id="5f897-137">Konfiguriert den UE-V-Agent so, dass alle Windows-apps synchronisiert werden, die nicht explizit durch die Windows-App-Liste für alle Benutzer des Computers deaktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="5f897-137">Configures the UE-V Agent to synchronize all Windows apps that are not explicitly disabled by the Windows app list for all users of the computer.</span></span> <span data-ttu-id="5f897-138">Weitere Informationen finden Sie unter &quot; Get-UevAppxPackage &quot; in <a href="managing-ue-v-2x-settings-location-templates-using-windows-powershell-and-wmi-both-uevv2.md" data-raw-source="[Managing UE-V 2.x Settings Location Templates Using Windows PowerShell and WMI](managing-ue-v-2x-settings-location-templates-using-windows-powershell-and-wmi-both-uevv2.md)"> Verwalten von Standort Vorlagen für die Einstellungen für UE-V 2. x mit Windows PowerShell und WMI </a> .</span><span class="sxs-lookup"><span data-stu-id="5f897-138">For more information, see &quot;Get-UevAppxPackage&quot; in <a href="managing-ue-v-2x-settings-location-templates-using-windows-powershell-and-wmi-both-uevv2.md" data-raw-source="[Managing UE-V 2.x Settings Location Templates Using Windows PowerShell and WMI](managing-ue-v-2x-settings-location-templates-using-windows-powershell-and-wmi-both-uevv2.md)">Managing UE-V 2.x Settings Location Templates Using Windows PowerShell and WMI</a>.</span></span></p>
   <p><span data-ttu-id="5f897-139">Verwenden Sie den <em> DisableSyncUnlistedWindows8Apps </em> -Parameter, um den UE-V-Agent so zu konfigurieren, dass nur Windows-apps synchronisiert werden, die explizit von der Windows-App-Liste aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="5f897-139">Use the <em>DisableSyncUnlistedWindows8Apps</em> parameter to configure the UE-V Agent to synchronize only Windows apps that are explicitly enabled by the Windows App List.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration - CurrentComputerUser - EnableSyncUnlistedWindows8Apps</code></p></td>
   <td align="left"><p><span data-ttu-id="5f897-140">Konfiguriert den UE-V-Agent so, dass alle Windows-apps synchronisiert werden, die nicht explizit durch die Windows-App-Liste für den aktuellen Benutzer auf dem Computer deaktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="5f897-140">Configures the UE-V Agent to synchronize all Windows apps that are not explicitly disabled by the Windows app list for the current user on the computer.</span></span> <span data-ttu-id="5f897-141">Weitere Informationen finden Sie unter &quot; Get-UevAppxPackage &quot; in <a href="managing-ue-v-2x-settings-location-templates-using-windows-powershell-and-wmi-both-uevv2.md" data-raw-source="[Managing UE-V 2.x Settings Location Templates Using Windows PowerShell and WMI](managing-ue-v-2x-settings-location-templates-using-windows-powershell-and-wmi-both-uevv2.md)"> Verwalten von Standort Vorlagen für die Einstellungen für UE-V 2. x mit Windows PowerShell und WMI </a> .</span><span class="sxs-lookup"><span data-stu-id="5f897-141">For more information, see &quot;Get-UevAppxPackage&quot; in <a href="managing-ue-v-2x-settings-location-templates-using-windows-powershell-and-wmi-both-uevv2.md" data-raw-source="[Managing UE-V 2.x Settings Location Templates Using Windows PowerShell and WMI](managing-ue-v-2x-settings-location-templates-using-windows-powershell-and-wmi-both-uevv2.md)">Managing UE-V 2.x Settings Location Templates Using Windows PowerShell and WMI</a>.</span></span></p>
   <p><span data-ttu-id="5f897-142">Verwenden Sie den <em> DisableSyncUnlistedWindows8Apps </em> -Parameter, um den UE-V-Agent so zu konfigurieren, dass nur Windows-apps synchronisiert werden, die explizit von der Windows-App-Liste aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="5f897-142">Use the <em>DisableSyncUnlistedWindows8Apps</em> parameter to configure the UE-V Agent to synchronize only Windows apps that are explicitly enabled by the Windows App List.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration –Computer –DisableSync</code></p></td>
   <td align="left"><p><span data-ttu-id="5f897-143">Deaktiviert UE-V für alle Benutzer auf dem Computer.</span><span class="sxs-lookup"><span data-stu-id="5f897-143">Disables UE-V for all the users on the computer.</span></span></p>
   <p><span data-ttu-id="5f897-144">Verwenden Sie den <em> EnableSync </em> -Parameter zum Aktivieren oder erneuten Aktivieren.</span><span class="sxs-lookup"><span data-stu-id="5f897-144">Use the <em>EnableSync</em> parameter to enable or re-enable.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration –CurrentComputerUser -DisableSync</code></p></td>
   <td align="left"><p><span data-ttu-id="5f897-145">Deaktiviert UE-V für den aktuellen Benutzer auf dem Computer.</span><span class="sxs-lookup"><span data-stu-id="5f897-145">Disables UE-V for the current user on the computer.</span></span></p>
   <p><span data-ttu-id="5f897-146">Verwenden Sie den <em> EnableSync </em> -Parameter zum Aktivieren oder erneuten Aktivieren.</span><span class="sxs-lookup"><span data-stu-id="5f897-146">Use the <em>EnableSync</em> parameter to enable or re-enable.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -Computer –EnableTrayIcon</code></p></td>
   <td align="left"><p><span data-ttu-id="5f897-147">Aktiviert das UE-V-Symbol im Infobereich für alle Benutzer des Computers.</span><span class="sxs-lookup"><span data-stu-id="5f897-147">Enables the UE-V icon in the notification area for all users of the computer.</span></span></p>
   <p><span data-ttu-id="5f897-148">Verwenden Sie den <em> DisableTrayIcon </em> -Parameter, um das Symbol zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="5f897-148">Use the <em>DisableTrayIcon</em> parameter to disable the icon.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration -Computer -MaxPackageSizeInBytes &lt;size in bytes&gt;</code></p></td>
   <td align="left"><p><span data-ttu-id="5f897-149">Konfiguriert den UE-V-Agent so, dass er meldet, wenn die Dateigröße des Einstellungen-Pakets den festgelegten Schwellenwert für alle Benutzer auf dem Computer erreicht.</span><span class="sxs-lookup"><span data-stu-id="5f897-149">Configures the UE-V agent to report when a settings package file size reaches the defined threshold for all users on the computer.</span></span> <span data-ttu-id="5f897-150">Legt die Größe des Schwellenwert Pakets in Bytes fest.</span><span class="sxs-lookup"><span data-stu-id="5f897-150">Sets the threshold package size in bytes.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -CurrentComputerUser -MaxPackageSizeInBytes &lt;size in bytes&gt;</code></p></td>
   <td align="left"><p><span data-ttu-id="5f897-151">Konfiguriert den UE-V-Agent so, dass er meldet, wenn die Dateigröße des Einstellungen-Pakets den definierten Schwellenwert erreicht hat.</span><span class="sxs-lookup"><span data-stu-id="5f897-151">Configures the UE-V agent to report when a settings package file size reaches the defined threshold.</span></span> <span data-ttu-id="5f897-152">Legt den Schwellenwert für die Paketgrößen Warnung für den aktuellen Benutzer fest.</span><span class="sxs-lookup"><span data-stu-id="5f897-152">Sets the package size warning threshold for the current user.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration -Computer -SettingsImportNotifyDelayInSeconds</code></p></td>
   <td align="left"><p><span data-ttu-id="5f897-153">Gibt die Zeit in Sekunden an, bevor der Benutzer für alle Benutzer des Computers benachrichtigt wird.</span><span class="sxs-lookup"><span data-stu-id="5f897-153">Specifies the time in seconds before the user is notified for all users of the computer</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration - CurrentComputerUser -SettingsImportNotifyDelayInSeconds</code></p></td>
   <td align="left"><p><span data-ttu-id="5f897-154">Gibt die Zeitdauer in Sekunden an, bevor die Benachrichtigung für den aktuellen Benutzer gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="5f897-154">Specifies the time in seconds before notification for the current user is sent.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration -Computer -SettingsStoragePath &lt;path to _settings_storage_location&gt;</code></p></td>
   <td align="left"><p><span data-ttu-id="5f897-155">Definiert einen Speicherplatz für computerspezifische Einstellungen für alle Benutzer des Computers.</span><span class="sxs-lookup"><span data-stu-id="5f897-155">Defines a per-computer settings storage location for all users of the computer.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -CurrentComputerUser -SettingsStoragePath &lt;path to _settings_storage_location&gt;</code></p></td>
   <td align="left"><p><span data-ttu-id="5f897-156">Definiert einen Speicherort für benutzerspezifische Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="5f897-156">Defines a per-user settings storage location.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration –Computer –SettingsTemplateCatalogPath &lt;path to catalog&gt;</code></p></td>
   <td align="left"><p><span data-ttu-id="5f897-157">Legt den Katalogpfad der Einstellungs Vorlage für alle Benutzer des Computers fest.</span><span class="sxs-lookup"><span data-stu-id="5f897-157">Sets the settings template catalog path for all users of the computer.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -Computer -SyncMethod &lt;sync method&gt;</code></p></td>
   <td align="left"><p><span data-ttu-id="5f897-158">Legt die Synchronisierungsmethode für alle Benutzer des Computers fest: SyncProvider oder None.</span><span class="sxs-lookup"><span data-stu-id="5f897-158">Sets the synchronization method for all users of the computer: SyncProvider or None.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration -CurrentComputerUser  -SyncMethod &lt;sync method&gt;</code></p></td>
   <td align="left"><p><span data-ttu-id="5f897-159">Legt die Synchronisierungsmethode für den aktuellen Benutzer fest: SyncProvider oder None.</span><span class="sxs-lookup"><span data-stu-id="5f897-159">Sets the synchronization method for the current user: SyncProvider or None.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -Computer -SyncTimeoutInMilliseconds &lt;timeout in milliseconds&gt;</code></p></td>
   <td align="left"><p><span data-ttu-id="5f897-160">Legt das Synchronisierungs Timeout in Millisekunden für alle Benutzer des Computers fest.</span><span class="sxs-lookup"><span data-stu-id="5f897-160">Sets the synchronization time-out in milliseconds for all users of the computer</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set- UevConfiguration -CurrentComputerUser -SyncTimeoutInMilliseconds &lt;timeout in milliseconds&gt;</code></p></td>
   <td align="left"><p><span data-ttu-id="5f897-161">Das Synchronisierungs Timeout für den aktuellen Benutzer festzulegen.</span><span class="sxs-lookup"><span data-stu-id="5f897-161">Set the synchronization time-out for the current user.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Clear-UevConfiguration –Computer -&lt;setting name&gt;</code></p></td>
   <td align="left"><p><span data-ttu-id="5f897-162">Löscht die angegebene Einstellung für alle Benutzer auf dem Computer.</span><span class="sxs-lookup"><span data-stu-id="5f897-162">Clears the specified setting for all users on the computer.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Clear-UevConfiguration –CurrentComputerUser -&lt;setting name&gt;</code></p></td>
   <td align="left"><p><span data-ttu-id="5f897-163">Löscht die angegebene Einstellung nur für den aktuellen Benutzer.</span><span class="sxs-lookup"><span data-stu-id="5f897-163">Clears the specified setting for the current user only.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Export-UevConfiguration &lt;settings migration file&gt;</code></p></td>
   <td align="left"><p><span data-ttu-id="5f897-164">Exportiert die UE-V-Computerkonfiguration in eine Migrationsdatei für Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="5f897-164">Exports the UE-V computer configuration to a settings migration file.</span></span> <span data-ttu-id="5f897-165">Die Dateinamenerweiterung muss UEV sein.</span><span class="sxs-lookup"><span data-stu-id="5f897-165">The file name extension must be .uev.</span></span></p>
   <p><span data-ttu-id="5f897-166">Das <code>Export</code> Cmdlet exportiert alle UE-V-Agenteneinstellungen, die mit dem <em> Computer </em> Parameter konfigurierbar sind.</span><span class="sxs-lookup"><span data-stu-id="5f897-166">The <code>Export</code> cmdlet exports all UE-V Agent settings that are configurable with the <em>Computer</em> parameter.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Import-UevConfiguration &lt;settings migration file&gt;</code></p></td>
   <td align="left"><p><span data-ttu-id="5f897-167">Importiert die UE-V-Computerkonfiguration aus einer Migrationsdatei für Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="5f897-167">Imports the UE-V computer configuration from a settings migration file.</span></span> <span data-ttu-id="5f897-168">Die Dateinamenerweiterung muss UEV sein.</span><span class="sxs-lookup"><span data-stu-id="5f897-168">The file name extension must be .uev.</span></span></p></td>
   </tr>
   </tbody>
   </table>



**<span data-ttu-id="5f897-169">So exportieren Sie UE-v-Paketeinstellungen und reparieren UE-v-Vorlagen mithilfe von Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="5f897-169">To export UE-V package settings and repair UE-V templates by using Windows PowerShell</span></span>**

1.  <span data-ttu-id="5f897-170">Öffnen Sie ein Windows PowerShell-Fenster als Administrator.</span><span class="sxs-lookup"><span data-stu-id="5f897-170">Open a Windows PowerShell window as an administrator.</span></span>

2.  <span data-ttu-id="5f897-171">Verwenden Sie die folgenden Windows PowerShell-Befehle zum Konfigurieren des Agents.</span><span class="sxs-lookup"><span data-stu-id="5f897-171">Use the following Windows PowerShell commands to configure the agent.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p><strong><span data-ttu-id="5f897-172">Windows PowerShell-Befehl</span><span class="sxs-lookup"><span data-stu-id="5f897-172">Windows PowerShell command</span></span></strong></p></td>
    <td align="left"><p><strong><span data-ttu-id="5f897-173">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5f897-173">Description</span></span></strong></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="5f897-174">Export-UevPackage MicrosoftCalculator6. pkgx</span><span class="sxs-lookup"><span data-stu-id="5f897-174">Export-UevPackage MicrosoftCalculator6.pkgx</span></span></p></td>
    <td align="left"><p><span data-ttu-id="5f897-175">Extrahiert die Einstellungen aus einer Microsoft Calculator-Paketdatei und wandelt sie in ein menschlich lesbares Format in XML um.</span><span class="sxs-lookup"><span data-stu-id="5f897-175">Extracts the settings from a Microsoft Calculator package file and converts them into a human-readable format in XML.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="5f897-176">Reparieren-UevTemplateIndex</span><span class="sxs-lookup"><span data-stu-id="5f897-176">Repair-UevTemplateIndex</span></span></p></td>
    <td align="left"><p><span data-ttu-id="5f897-177">Repariert den Index der Standort Vorlagen für UE-V-Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="5f897-177">Repairs the index of the UE-V settings location templates.</span></span></p></td>
    </tr>
    </tbody>
    </table>



**<span data-ttu-id="5f897-178">So konfigurieren Sie den UE-V-Agent mithilfe von WMI</span><span class="sxs-lookup"><span data-stu-id="5f897-178">To configure the UE-V Agent by using WMI</span></span>**

1.  <span data-ttu-id="5f897-179">Die Virtualisierung der Benutzeroberfläche bietet die folgenden WMI-Befehle.</span><span class="sxs-lookup"><span data-stu-id="5f897-179">User Experience Virtualization provides the following set of WMI commands.</span></span> <span data-ttu-id="5f897-180">Administratoren können diese Schnittstelle verwenden, um den UE-V-Agent über die Befehlszeile zu konfigurieren und typische Konfigurationsaufgaben zu automatisieren.</span><span class="sxs-lookup"><span data-stu-id="5f897-180">Administrators can use this interface to configure the UE-V agent at the command line and automate typical configuration tasks.</span></span>

    <span data-ttu-id="5f897-181">Verwenden Sie ein Konto mit Administratorrechten, um ein Windows PowerShell-Fenster zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="5f897-181">Use an account with administrator rights to open a Windows PowerShell window.</span></span>

2.  <span data-ttu-id="5f897-182">Verwenden Sie die folgenden WMI-Befehle zum Konfigurieren des Agents.</span><span class="sxs-lookup"><span data-stu-id="5f897-182">Use the following WMI commands to configure the agent.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><code>Windows PowerShell command</code></th>
    <th align="left"><span data-ttu-id="5f897-183">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5f897-183">Description</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><code>Get-WmiObject -Namespace root\Microsoft\UEV Configuration</code></p>
    <p></p></td>
    <td align="left"><p><span data-ttu-id="5f897-184">Zeigt die aktiven UE-V-Agenteneinstellungen an.</span><span class="sxs-lookup"><span data-stu-id="5f897-184">Displays the active UE-V Agent settings.</span></span> <span data-ttu-id="5f897-185">Benutzerspezifische Einstellungen haben Vorrang vor den Computereinstellungen.</span><span class="sxs-lookup"><span data-stu-id="5f897-185">User-specific settings have precedence over the computer settings.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Get-WmiObject -Namespace root\Microsoft\UEV UserConfiguration</code></p></td>
    <td align="left"><p><span data-ttu-id="5f897-186">Zeigt die für einen benutzerdefinierte UE-V-Agent-Konfiguration an.</span><span class="sxs-lookup"><span data-stu-id="5f897-186">Displays the UE-V Agent configuration that is defined for a user.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</code></p></td>
    <td align="left"><p><span data-ttu-id="5f897-187">Zeigt die für einen Computer definierte UE-V-Agent-Konfiguration an.</span><span class="sxs-lookup"><span data-stu-id="5f897-187">Displays the UE-V Agent configuration that is defined for a computer.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Get-WmiObject –Namespace root\Microsoft\Uev ConfigurationItem</code></p></td>
    <td align="left"><p><span data-ttu-id="5f897-188">Zeigt die Details für jedes Konfigurationselement an.</span><span class="sxs-lookup"><span data-stu-id="5f897-188">Displays the details for each configuration item.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</code></p>
    <p><code>$config.SettingsStoragePath = &lt;path_to_settings_storage_location&gt;</code></p>
    <p><span data-ttu-id="5f897-189">$config. Put ()</span><span class="sxs-lookup"><span data-stu-id="5f897-189">$config.Put()</span></span></p></td>
    <td align="left"><p><span data-ttu-id="5f897-190">Definiert einen Speicherort für pro Computer-Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="5f897-190">Defines a per-computer settings storage location.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>$config = Get-WmiObject -Namespace root\Microsoft\UEV UserConfiguration</code></p>
    <p><code>$config.SettingsStoragePath = &lt;path_to_settings_storage_location&gt;</code></p>
    <p><code>$config.Put()</code></p></td>
    <td align="left"><p><span data-ttu-id="5f897-191">Definiert einen Speicherort für benutzerspezifische Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="5f897-191">Defines a per-user settings storage location.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</code></p>
    <p><code>$config.SyncTimeoutInMilliseconds = &lt;timeout_in_milliseconds&gt;</code></p>
    <p><code>$config.Put()</code></p></td>
    <td align="left"><p><span data-ttu-id="5f897-192">Legt das Synchronisierungs Timeout in Millisekunden für alle Benutzer des Computers fest.</span><span class="sxs-lookup"><span data-stu-id="5f897-192">Sets the synchronization time-out in milliseconds for all users of the computer.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</code></p>
    <p><code>$config.MaxPackageSizeInBytes = &lt;size_in_bytes&gt;</code></p>
    <p><code>$config.Put()</code></p></td>
    <td align="left"><p><span data-ttu-id="5f897-193">Konfiguriert den UE-V-Agent so, dass er meldet, wenn die Dateigröße eines Einstellungen-Pakets einen festgelegten Schwellenwert erreicht.</span><span class="sxs-lookup"><span data-stu-id="5f897-193">Configures the UE-V Agent to report when a settings package file size reaches a defined threshold.</span></span> <span data-ttu-id="5f897-194">Legen Sie die Schwellenwert-Paketdatei Größe in Bytes für alle Benutzer des Computers fest.</span><span class="sxs-lookup"><span data-stu-id="5f897-194">Set the threshold package file size in bytes for all users of the computer.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</code></p>
    <p><code>$config.SyncMethod = &lt;sync_method&gt;</code></p>
    <p><code>$config.Put()</code></p></td>
    <td align="left"><p><span data-ttu-id="5f897-195">Legt die Synchronisierungsmethode für alle Benutzer des Computers fest: SyncProvider oder None.</span><span class="sxs-lookup"><span data-stu-id="5f897-195">Sets the synchronization method for all users of the computer: SyncProvider or None.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</code></p>
    <p><code>$config.&lt;setting name&gt; = $true</code></p>
    <p><code>$config.Put()</code></p></td>
    <td align="left"><p><span data-ttu-id="5f897-196">Wenn Sie eine bestimmte Einstellung pro Computer aktivieren möchten, deaktivieren Sie die Einstellung, und verwenden Sie <em> $NULL </em> als Einstellungswert.</span><span class="sxs-lookup"><span data-stu-id="5f897-196">To enable a specific per-computer setting, clear the setting, and use <em>$null</em> as the setting value.</span></span> <span data-ttu-id="5f897-197">Verwenden Sie UserConfiguration für benutzerspezifische Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="5f897-197">Use UserConfiguration for per-user settings.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</code></p>
    <p><code>$config.&lt;setting name&gt; = $false</code></p>
    <p><code>$config.Put()</code></p></td>
    <td align="left"><p><span data-ttu-id="5f897-198">Wenn Sie eine bestimmte Einstellung pro Computer deaktivieren möchten, deaktivieren Sie die Einstellung, und verwenden Sie <em> $NULL </em> als Einstellungswert.</span><span class="sxs-lookup"><span data-stu-id="5f897-198">To disable a specific per-computer setting, clear the setting, and use <em>$null</em> as the setting value.</span></span> <span data-ttu-id="5f897-199">Verwenden Sie die Benutzerkonfiguration für benutzerspezifische Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="5f897-199">Use User Configuration for per-user settings.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</code></p>
    <p><code>$config.&lt;setting name&gt; = &lt;setting value&gt;</code></p>
    <p><code>$config.Put()</code></p></td>
    <td align="left"><p><span data-ttu-id="5f897-200">Aktualisiert eine bestimmte Einstellung pro Computer.</span><span class="sxs-lookup"><span data-stu-id="5f897-200">Updates a specific per-computer setting.</span></span> <span data-ttu-id="5f897-201">Verwenden Sie <em> $null als Einstellungswert, um die Einstellung zu löschen </em> .</span><span class="sxs-lookup"><span data-stu-id="5f897-201">To clear the setting, use <em>$null</em> as the setting value.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</code></p>
    <p><code></code><span data-ttu-id="5f897-202">$config. &lt; Einstellungs &gt;  =  &lt; Wert für Name&gt;</span><span class="sxs-lookup"><span data-stu-id="5f897-202">$config.&lt;setting name&gt; = &lt;setting value&gt;</span></span></p>
    <p><code>$config.Put()</code></p></td>
    <td align="left"><p><span data-ttu-id="5f897-203">Aktualisiert eine bestimmte pro-Benutzer-Einstellung für alle Benutzer des Computers.</span><span class="sxs-lookup"><span data-stu-id="5f897-203">Updates a specific per-user setting for all users of the computer.</span></span> <span data-ttu-id="5f897-204">Verwenden Sie <em> $null als Einstellungswert, um die Einstellung zu löschen </em> .</span><span class="sxs-lookup"><span data-stu-id="5f897-204">To clear the setting, use <em>$null</em> as the setting value.</span></span></p></td>
    </tr>
    </tbody>
    </table>



~~~
Upon configuration of the UE-V Agent with WMI and Windows PowerShell, the defined configuration is stored in the registry in the following locations.

`\HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\UEV\Agent\Configuration`

`\HKEY_CURRENT_USER\SOFTWARE\Microsoft\UEV\Agent\Configuration`
~~~

**<span data-ttu-id="5f897-205">So exportieren Sie UE-v-Paketeinstellungen und reparieren UE-v-Vorlagen mithilfe von WMI</span><span class="sxs-lookup"><span data-stu-id="5f897-205">To export UE-V package settings and repair UE-V templates by using WMI</span></span>**

1.  <span data-ttu-id="5f897-206">UE-V bietet den folgenden Satz von WMI-Befehlen.</span><span class="sxs-lookup"><span data-stu-id="5f897-206">UE-V provides the following set of WMI commands.</span></span> <span data-ttu-id="5f897-207">Administratoren können diese Schnittstelle verwenden, um ein Paket zu exportieren oder UE-V-Vorlagen zu reparieren.</span><span class="sxs-lookup"><span data-stu-id="5f897-207">Administrators can use this interface to export a package or repair UE-V templates.</span></span>

2.  <span data-ttu-id="5f897-208">Verwenden Sie die folgenden WMI-Befehle.</span><span class="sxs-lookup"><span data-stu-id="5f897-208">Use the following WMI commands.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="5f897-209">WMI-Befehl</span><span class="sxs-lookup"><span data-stu-id="5f897-209">WMI command</span></span></th>
    <th align="left"><span data-ttu-id="5f897-210">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5f897-210">Description</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class UserSettings -Name ExportPackage -ArgumentList &lt;package name&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="5f897-211">Extrahiert die Einstellungen aus einer Paketdatei und wandelt sie in ein menschlich lesbares Format in XML um.</span><span class="sxs-lookup"><span data-stu-id="5f897-211">Extracts the settings from a package file and converts them into a human-readable format in XML.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name RebuildIndex</code></p></td>
    <td align="left"><p><span data-ttu-id="5f897-212">Repariert den Index der Standort Vorlagen für UE-V-Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="5f897-212">Repairs the index of the UE-V settings location templates.</span></span> <span data-ttu-id="5f897-213">Muss als Administrator ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="5f897-213">Must be run as administrator.</span></span></p></td>
    </tr>
    </tbody>
    </table>



~~~
**Got a suggestion for UE-V**? Add or vote on suggestions [here](http://uev.uservoice.com/forums/280428-microsoft-user-experience-virtualization). **Got a UE-V issue**? Use the [UE-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopuev).
~~~

## <span data-ttu-id="5f897-214">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="5f897-214">Related topics</span></span>


[<span data-ttu-id="5f897-215">Verwalten von UE-V 2. x mit Windows PowerShell und WMI</span><span class="sxs-lookup"><span data-stu-id="5f897-215">Administering UE-V 2.x with Windows PowerShell and WMI</span></span>](administering-ue-v-2x-with-windows-powershell-and-wmi-both-uevv2.md)

[<span data-ttu-id="5f897-216">Verwalten von UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="5f897-216">Administering UE-V 2.x</span></span>](administering-ue-v-2x-new-uevv2.md)









