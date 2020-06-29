---
title: Verwalten des UE-V 1.0-Agents und von Paketen mit PowerShell und WMI
description: Verwalten des UE-V 1.0-Agents und von Paketen mit PowerShell und WMI
author: dansimp
ms.assetid: c8989b01-1769-4e69-82b1-4aadb261d2d5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 79268e3384aaaf08bdd4e9b92d74b039ce96596a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807851"
---
# <span data-ttu-id="7d115-103">Verwalten des UE-V 1.0-Agents und von Paketen mit PowerShell und WMI</span><span class="sxs-lookup"><span data-stu-id="7d115-103">Managing the UE-V 1.0 Agent and Packages with PowerShell and WMI</span></span>


<span data-ttu-id="7d115-104">Sie können WMI und PowerShell verwenden, um die Konfiguration und das Synchronisierungsverhalten der Microsoft User Experience Virtualization (UE-V)-Agents zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="7d115-104">You can use WMI and PowerShell to manage Microsoft User Experience Virtualization (UE-V) Agent configuration and synchronization behavior.</span></span>

**<span data-ttu-id="7d115-105">Bereitstellen des UE-V-Agents mit PowerShell</span><span class="sxs-lookup"><span data-stu-id="7d115-105">How to deploy the UE-V agent with PowerShell</span></span>**

1.  <span data-ttu-id="7d115-106">Stufen Sie die UE-V-Installationsdatei in einer barrierefreien Netzwerkfreigabe ein.</span><span class="sxs-lookup"><span data-stu-id="7d115-106">Stage the UE-V installer file in an accessible network share.</span></span>

    **<span data-ttu-id="7d115-107">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="7d115-107">Note</span></span>**  
    <span data-ttu-id="7d115-108">Verwenden Sie AgentSetup.exe, um sowohl 32-Bit-als auch 64-Bit-Versionen des UE-V-Agents bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="7d115-108">Use AgentSetup.exe to deploy both 32-bit and 64-bit versions of the UE-V Agent.</span></span> <span data-ttu-id="7d115-109">Windows Installer-Dateien, AgentSetupx86.msi und AgentSetupx64.msi, stehen für jede Architektur zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="7d115-109">Windows Installer Files versions, AgentSetupx86.msi and AgentSetupx64.msi, are available for each architecture.</span></span> <span data-ttu-id="7d115-110">Wenn Sie den UE-V-Agent zu einem späteren Zeitpunkt mit der Installationsdatei deinstallieren möchten, müssen Sie denselben Dateityp verwenden.</span><span class="sxs-lookup"><span data-stu-id="7d115-110">To uninstall the UE-V Agent at a later time using the installation file, you must use the same file type.</span></span>



2.  <span data-ttu-id="7d115-111">Verwenden Sie einen der folgenden PowerShell-Befehle, um den Agenten zu installieren.</span><span class="sxs-lookup"><span data-stu-id="7d115-111">Use one of the following PowerShell commands to install the agent.</span></span>

    `& AgentSetup.exe /quiet /norestart /log "%temp%\UE-VAgentInstaller.log" SettingsStoragePath=\\server\settingsshare\%username%`

    `& msiexec.exe /i "<path to msi file>" /quiet /norestart /l*v "%temp%\UE-VAgentInstaller.log" SettingsStoragePath=\\server\settingsshare\%username%`

**<span data-ttu-id="7d115-112">Konfigurieren des UE-V-Agents mit PowerShell</span><span class="sxs-lookup"><span data-stu-id="7d115-112">How to configure the UE-V Agent with PowerShell</span></span>**

1.  <span data-ttu-id="7d115-113">Verwenden Sie ein Konto mit Administratorrechten, um ein PowerShell-Fenster zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="7d115-113">Use an account with administrator rights to open a PowerShell window.</span></span> <span data-ttu-id="7d115-114">Importieren Sie das UE-V PowerShell-Modul mithilfe des folgenden Befehls.</span><span class="sxs-lookup"><span data-stu-id="7d115-114">Import the UE-V PowerShell module by using the following command.</span></span>

    ``` syntax
    Import-module UEV
    ```

2.  <span data-ttu-id="7d115-115">Verwenden Sie die folgenden PowerShell-Befehle zum Konfigurieren des Agents.</span><span class="sxs-lookup"><span data-stu-id="7d115-115">Use the following PowerShell commands to configure the agent.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p><strong><span data-ttu-id="7d115-116">PowerShell-Befehl</span><span class="sxs-lookup"><span data-stu-id="7d115-116">PowerShell command</span></span></strong></p></td>
    <td align="left"><p><strong><span data-ttu-id="7d115-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7d115-117">Description</span></span></strong></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="7d115-118">Get-UevConfiguration</span><span class="sxs-lookup"><span data-stu-id="7d115-118">Get-UevConfiguration</span></span></p>
    <p></p></td>
    <td align="left"><p><span data-ttu-id="7d115-119">Zeigen Sie die effektiven Einstellungen des UE-V-Agents an.</span><span class="sxs-lookup"><span data-stu-id="7d115-119">View the effective UE-V agent settings.</span></span> <span data-ttu-id="7d115-120">Benutzerspezifische Einstellungen haben Vorrang vor den Computereinstellungen.</span><span class="sxs-lookup"><span data-stu-id="7d115-120">User-specific settings have precedence over the computer settings.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="7d115-121">Get-UevConfiguration-CurrentComputerUser</span><span class="sxs-lookup"><span data-stu-id="7d115-121">Get-UevConfiguration - CurrentComputerUser</span></span></p>
    <p></p></td>
    <td align="left"><p><span data-ttu-id="7d115-122">Anzeigen der Einstellungen des UE-V-Agents nur für den aktuellen Benutzer.</span><span class="sxs-lookup"><span data-stu-id="7d115-122">View the UE-V agent settings values for the current user only.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="7d115-123">Get-UevConfiguration-Computer</span><span class="sxs-lookup"><span data-stu-id="7d115-123">Get-UevConfiguration -Computer</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7d115-124">Zeigen Sie die Werte für die Konfigurationseinstellungen des UE-V-Agents für alle Benutzer auf dem Computer an.</span><span class="sxs-lookup"><span data-stu-id="7d115-124">View the UE-V agent configuration settings values for all users on the computer.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="7d115-125">Satz-UevConfiguration-Computer-SettingsStoragePath &lt; Pfad zu _settings_storage_location&gt;</span><span class="sxs-lookup"><span data-stu-id="7d115-125">Set-UevConfiguration -Computer -SettingsStoragePath &lt;path to _settings_storage_location&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7d115-126">Definieren Sie einen Speicherort für pro Computer-Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="7d115-126">Define a per-computer settings storage location.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="7d115-127">Satz-UevConfiguration-CurrentComputerUser-SettingsStoragePath- &lt; Pfad zu _settings_storage_location&gt;</span><span class="sxs-lookup"><span data-stu-id="7d115-127">Set-UevConfiguration -CurrentComputerUser -SettingsStoragePath &lt;path to _settings_storage_location&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7d115-128">Definieren Sie einen Speicherort für benutzerspezifische Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="7d115-128">Define a per-user settings storage location.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="7d115-129">UevConfiguration-Computer-SyncTimeoutInMilliseconds &lt; Timeout in Millisekunden&gt;</span><span class="sxs-lookup"><span data-stu-id="7d115-129">Set-UevConfiguration -Computer -SyncTimeoutInMilliseconds &lt;timeout in milliseconds&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7d115-130">Einstellen des Synchronisierungs Timeouts in Millisekunden</span><span class="sxs-lookup"><span data-stu-id="7d115-130">Set the synchronization timeout in milliseconds</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="7d115-131">UevConfiguration-CurrentComputerUser-SyncTimeoutInMilliseconds- &lt; Timeout in Millisekunden&gt;</span><span class="sxs-lookup"><span data-stu-id="7d115-131">Set-UevConfiguration -CurrentComputerUser -SyncTimeoutInMilliseconds &lt;timeout in milliseconds&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7d115-132">Setzen Sie das Synchronisierungs Timeout für den aktuellen Benutzer.</span><span class="sxs-lookup"><span data-stu-id="7d115-132">Set the synchronization timeout for the current user.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="7d115-133">Satz-UevConfiguration-Computer-MaxPackageSizeInBytes &lt; Größe in Bytes&gt;</span><span class="sxs-lookup"><span data-stu-id="7d115-133">Set-UevConfiguration -Computer -MaxPackageSizeInBytes &lt;size in bytes&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7d115-134">Konfigurieren Sie den UE-V-Agent so, dass er meldet, wenn die Dateigröße eines Einstellungen-Pakets einen definierten Schwellenwert erreicht.</span><span class="sxs-lookup"><span data-stu-id="7d115-134">Configure the UE-V agent to report when a settings package file size reaches a defined threshold.</span></span> <span data-ttu-id="7d115-135">Festlegen der Größe des Schwellenwert Pakets in Bytes</span><span class="sxs-lookup"><span data-stu-id="7d115-135">Set the threshold package size in bytes.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="7d115-136">Satz-UevConfiguration-CurrentComputerUser-MaxPackageSizeInBytes &lt; Größe in Bytes&gt;</span><span class="sxs-lookup"><span data-stu-id="7d115-136">Set-UevConfiguration -CurrentComputerUser -MaxPackageSizeInBytes &lt;size in bytes&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7d115-137">Festlegen des warnungsschwellenwerts für die Paketgröße für den aktuellen Benutzer</span><span class="sxs-lookup"><span data-stu-id="7d115-137">Set the package size warning threshold for the current user.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="7d115-138">Satz-UevConfiguration – Computer – SettingsTemplateCatalogPath &lt; Pfad zum Katalog&gt;</span><span class="sxs-lookup"><span data-stu-id="7d115-138">Set-UevConfiguration –Computer –SettingsTemplateCatalogPath &lt;path to catalog&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7d115-139">Festlegen des Katalog Pfads für die Einstellungs Vorlage</span><span class="sxs-lookup"><span data-stu-id="7d115-139">Set the settings template catalog path.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="7d115-140">Satz-UevConfiguration-Computer-SyncMethod- &lt; Synchronisierungsmethode&gt;</span><span class="sxs-lookup"><span data-stu-id="7d115-140">Set-UevConfiguration -Computer -SyncMethod &lt;sync method&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7d115-141">Setzen Sie die Synchronisierungsmethode: Offlinedateien oder None.</span><span class="sxs-lookup"><span data-stu-id="7d115-141">Set the synchronization method: OfflineFiles or None.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="7d115-142">Satz-UevConfiguration-CurrentComputerUser-SyncMethod- &lt; Synchronisierungsmethode&gt;</span><span class="sxs-lookup"><span data-stu-id="7d115-142">Set-UevConfiguration -CurrentComputerUser -SyncMethod &lt;sync method&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7d115-143">Stellen Sie die Synchronisierungsmethode für den aktuellen Benutzer ein: Offlinedateien oder None.</span><span class="sxs-lookup"><span data-stu-id="7d115-143">Set the synchronization method for the current user: OfflineFiles or None.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="7d115-144">Satz-UEVConfiguration-Computer – EnableSettingsImportNotify</span><span class="sxs-lookup"><span data-stu-id="7d115-144">Set-UEVConfiguration -Computer –EnableSettingsImportNotify</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7d115-145">Benachrichtigung kann auftreten, wenn der Import von Benutzereinstellungen verzögert wird.</span><span class="sxs-lookup"><span data-stu-id="7d115-145">Enable notification to occur when the import of user settings is delayed.</span></span></p>
    <p><span data-ttu-id="7d115-146">Verwenden Sie – DisableSettingsImportNotify, um die Benachrichtigung zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="7d115-146">Use –DisableSettingsImportNotify to disable notification.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="7d115-147">Satz-UEVConfiguration-CurrentComputerUser-EnableSettingsImportNotify</span><span class="sxs-lookup"><span data-stu-id="7d115-147">Set-UEVConfiguration - CurrentComputerUser -EnableSettingsImportNotify</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7d115-148">Benachrichtigung für den aktuellen Benutzer aktivieren, wenn der Import von Benutzereinstellungen verzögert wird.</span><span class="sxs-lookup"><span data-stu-id="7d115-148">Enable notification for the current user when the import of user settings is delayed.</span></span></p>
    <p><span data-ttu-id="7d115-149">Verwenden Sie – DisableSettingsImportNotify, um die Benachrichtigung zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="7d115-149">Use –DisableSettingsImportNotify to disable notification.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="7d115-150">Satz-UEVConfiguration-Computer-SettingsImportNotifyDelayInSeconds</span><span class="sxs-lookup"><span data-stu-id="7d115-150">Set-UEVConfiguration -Computer -SettingsImportNotifyDelayInSeconds</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7d115-151">Angeben der Uhrzeit in Sekunden, bevor der Benutzer benachrichtigt wird</span><span class="sxs-lookup"><span data-stu-id="7d115-151">Specify the time in seconds before the user is notified</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="7d115-152">Satz-UEVConfiguration-CurrentComputerUser-SettingsImportNotifyDelayInSeconds</span><span class="sxs-lookup"><span data-stu-id="7d115-152">Set-UEVConfiguration - CurrentComputerUser -SettingsImportNotifyDelayInSeconds</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7d115-153">Geben Sie die Zeitdauer in Sekunden vor der Benachrichtigung für den aktuellen Benutzer an.</span><span class="sxs-lookup"><span data-stu-id="7d115-153">Specify the time in seconds before notification for the current user.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="7d115-154">Satz-UevConfiguration – Computer – DisableSync</span><span class="sxs-lookup"><span data-stu-id="7d115-154">Set-UevConfiguration –Computer –DisableSync</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7d115-155">Deaktivieren Sie UE-V für alle Benutzer auf dem Computer.</span><span class="sxs-lookup"><span data-stu-id="7d115-155">Disable UE-V for all the users on the computer.</span></span></p>
    <p><span data-ttu-id="7d115-156">Verwenden Sie – EnableSync zum Aktivieren oder erneuten Aktivieren.</span><span class="sxs-lookup"><span data-stu-id="7d115-156">Use –EnableSync to enable or re-enable.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="7d115-157">Satz-UevConfiguration – CurrentComputerUser-DisableSync</span><span class="sxs-lookup"><span data-stu-id="7d115-157">Set-UevConfiguration –CurrentComputerUser -DisableSync</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7d115-158">Deaktivieren Sie UE-V für den aktuellen Benutzer auf dem Computer.</span><span class="sxs-lookup"><span data-stu-id="7d115-158">Disable UE-V for the current user on the computer.</span></span></p>
    <p><span data-ttu-id="7d115-159">Verwenden Sie – EnableSync zum Aktivieren oder erneuten Aktivieren.</span><span class="sxs-lookup"><span data-stu-id="7d115-159">Use –EnableSync to enable or re-enable.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="7d115-160">Clear-UevConfiguration – Name der Computer &lt; Einstellung&gt;</span><span class="sxs-lookup"><span data-stu-id="7d115-160">Clear-UevConfiguration –Computer -&lt;setting name&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7d115-161">Deaktivieren Sie eine bestimmte Einstellung für alle Benutzer auf dem Computer.</span><span class="sxs-lookup"><span data-stu-id="7d115-161">Clear a specific setting for all users on the computer.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="7d115-162">Clear-UevConfiguration – CurrentComputerUser- &lt; Einstellungsname&gt;</span><span class="sxs-lookup"><span data-stu-id="7d115-162">Clear-UevConfiguration –CurrentComputerUser -&lt;setting name&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7d115-163">Deaktivieren Sie eine bestimmte Einstellung nur für den aktuellen Benutzer.</span><span class="sxs-lookup"><span data-stu-id="7d115-163">Clear a specific setting for the current user only.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="7d115-164">Migrationsdatei für Export-UevConfiguration- &lt; Einstellungen&gt;</span><span class="sxs-lookup"><span data-stu-id="7d115-164">Export-UevConfiguration &lt;settings migration file&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7d115-165">Exportieren Sie die UE-V-Computerkonfiguration in eine Migrationsdatei für Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="7d115-165">Export the UE-V computer configuration to a settings migration file.</span></span> <span data-ttu-id="7d115-166">Die Dateierweiterung muss ". UEV" sein.</span><span class="sxs-lookup"><span data-stu-id="7d115-166">The extension of the file must be “.uev”.</span></span></p>
    <p><span data-ttu-id="7d115-167">Mit dem Export-Cmdlet werden alle UE-V-Agent-Einstellungen exportiert, die mit dem-Computer-Parameter konfigurierbar sind.</span><span class="sxs-lookup"><span data-stu-id="7d115-167">The export cmdlet exports all UE-V agent settings that are configurable with the -computer parameter.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="7d115-168">Migrationsdatei für Import-UevConfiguration- &lt; Einstellungen&gt;</span><span class="sxs-lookup"><span data-stu-id="7d115-168">Import-UevConfiguration &lt;settings migration file&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7d115-169">Importieren Sie die UE-V-Computerkonfiguration aus einer Einstellungs Migrationsdatei (UEV-Datei).</span><span class="sxs-lookup"><span data-stu-id="7d115-169">Import the UE-V computer configuration from a settings migration file (.uev file).</span></span></p></td>
    </tr>
    </tbody>
    </table>



**<span data-ttu-id="7d115-170">Exportieren von UE-v-Paketeinstellungen und Reparieren von UE-v-Vorlagen mit PowerShell</span><span class="sxs-lookup"><span data-stu-id="7d115-170">How to export UE-V package settings and repair UE-V templates with PowerShell</span></span>**

1.  <span data-ttu-id="7d115-171">Öffnen Sie ein PowerShell-Fenster als Administrator.</span><span class="sxs-lookup"><span data-stu-id="7d115-171">Open a PowerShell window as an Administrator.</span></span> <span data-ttu-id="7d115-172">Importieren Sie das UE-V PowerShell-Modul mit dem folgenden Befehl.</span><span class="sxs-lookup"><span data-stu-id="7d115-172">Import the UE-V PowerShell module with the following command.</span></span>

    ``` syntax
    Import-module UEV
    ```

2.  <span data-ttu-id="7d115-173">Verwenden Sie die folgenden PowerShell-Befehle zum Konfigurieren des Agents.</span><span class="sxs-lookup"><span data-stu-id="7d115-173">Use the following PowerShell commands to configure the agent.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p><strong><span data-ttu-id="7d115-174">PowerShell-Befehl</span><span class="sxs-lookup"><span data-stu-id="7d115-174">PowerShell command</span></span></strong></p></td>
    <td align="left"><p><strong><span data-ttu-id="7d115-175">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7d115-175">Description</span></span></strong></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="7d115-176">Export-UevPackage MicrosoftCalculator6. pkgx</span><span class="sxs-lookup"><span data-stu-id="7d115-176">Export-UevPackage MicrosoftCalculator6.pkgx</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7d115-177">Extrahiert die Einstellungen aus einer Microsoft Calculator-Paketdatei und wandelt sie in ein menschlich lesbares Format in XML um.</span><span class="sxs-lookup"><span data-stu-id="7d115-177">Extracts the settings from a Microsoft Calculator package file and converts them into a human-readable format in XML.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="7d115-178">Reparieren-UevTemplateIndex</span><span class="sxs-lookup"><span data-stu-id="7d115-178">Repair-UevTemplateIndex</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7d115-179">Repariert den Index der Standort Vorlagen für UE-V-Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="7d115-179">Repairs the index of the UE-V settings location templates.</span></span></p></td>
    </tr>
    </tbody>
    </table>



**<span data-ttu-id="7d115-180">Konfigurieren des UE-V-Agents mit WMI</span><span class="sxs-lookup"><span data-stu-id="7d115-180">How to configure the UE-V Agent with WMI</span></span>**

1.  <span data-ttu-id="7d115-181">Die Virtualisierung der Benutzeroberfläche bietet die folgenden WMI-Befehle.</span><span class="sxs-lookup"><span data-stu-id="7d115-181">User Experience Virtualization provides the following set of WMI commands.</span></span> <span data-ttu-id="7d115-182">Administratoren können diese Schnittstelle verwenden, um den UE-V-Agent über die Befehlszeile zu konfigurieren und typische Konfigurationsaufgaben zu automatisieren.</span><span class="sxs-lookup"><span data-stu-id="7d115-182">Administrators can use this interface to configure the UE-V agent from the command line and automate typical configuration tasks.</span></span>

    <span data-ttu-id="7d115-183">Verwenden Sie ein Konto mit Administratorrechten, um ein PowerShell-Fenster zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="7d115-183">Use an account with administrator rights to open a PowerShell window.</span></span>

2.  <span data-ttu-id="7d115-184">Verwenden Sie die folgenden WMI-Befehle zum Konfigurieren des Agents.</span><span class="sxs-lookup"><span data-stu-id="7d115-184">Use the following WMI commands to configure the agent.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="7d115-185">PowerShell-Befehl</span><span class="sxs-lookup"><span data-stu-id="7d115-185">PowerShell command</span></span></th>
    <th align="left"><span data-ttu-id="7d115-186">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7d115-186">Description</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="7d115-187">Get-WMIObject-Namespace-root\Microsoft\UEV-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="7d115-187">Get-WmiObject -Namespace root\Microsoft\UEV Configuration</span></span></p>
    <p></p></td>
    <td align="left"><p><span data-ttu-id="7d115-188">Anzeigen der aktiven UE-V-Agenteneinstellungen</span><span class="sxs-lookup"><span data-stu-id="7d115-188">View the active UE-V agent settings.</span></span> <span data-ttu-id="7d115-189">Benutzerspezifische Einstellungen haben Vorrang vor den Computereinstellungen.</span><span class="sxs-lookup"><span data-stu-id="7d115-189">User-specific settings have precedence over the computer settings.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="7d115-190">Get-WMIObject-Namespace root\Microsoft\UEV UserConfiguration</span><span class="sxs-lookup"><span data-stu-id="7d115-190">Get-WmiObject -Namespace root\Microsoft\UEV UserConfiguration</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7d115-191">Anzeigen der für den benutzerdefinierten UE-V-Agent-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="7d115-191">View the UE-V agent configuration that is defined for user.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="7d115-192">Get-WMIObject-Namespace root\Microsoft\UEV ComputerConfiguration</span><span class="sxs-lookup"><span data-stu-id="7d115-192">Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7d115-193">Anzeigen der für den Computer definierten UE-V-Agent-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="7d115-193">View the UE-V agent configuration that is defined for computer.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="7d115-194">$config = Get-WMIObject-Namespace root\Microsoft\UEV ComputerConfiguration</span><span class="sxs-lookup"><span data-stu-id="7d115-194">$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</span></span></p>
    <p><span data-ttu-id="7d115-195">$config. SettingsStoragePath = &lt; path_to_settings_storage_location&gt;</span><span class="sxs-lookup"><span data-stu-id="7d115-195">$config.SettingsStoragePath = &lt;path_to_settings_storage_location&gt;</span></span></p>
    <p><span data-ttu-id="7d115-196">$config. Put ()</span><span class="sxs-lookup"><span data-stu-id="7d115-196">$config.Put()</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7d115-197">Definieren Sie einen Speicherort für pro Computer-Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="7d115-197">Define a per-computer settings storage location.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="7d115-198">$config = Get-WMIObject-Namespace root\Microsoft\UEV UserConfiguration</span><span class="sxs-lookup"><span data-stu-id="7d115-198">$config = Get-WmiObject -Namespace root\Microsoft\UEV UserConfiguration</span></span></p>
    <p><span data-ttu-id="7d115-199">$config. SettingsStoragePath = &lt; path_to_settings_storage_location&gt;</span><span class="sxs-lookup"><span data-stu-id="7d115-199">$config.SettingsStoragePath = &lt;path_to_settings_storage_location&gt;</span></span></p>
    <p><span data-ttu-id="7d115-200">$config. Put ()</span><span class="sxs-lookup"><span data-stu-id="7d115-200">$config.Put()</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7d115-201">Definieren Sie einen Speicherort für benutzerspezifische Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="7d115-201">Define a per-user settings storage location.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="7d115-202">$config = Get-WMIObject-Namespace root\Microsoft\UEV ComputerConfiguration</span><span class="sxs-lookup"><span data-stu-id="7d115-202">$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</span></span></p>
    <p><span data-ttu-id="7d115-203">$config. SyncTimeoutInMilliseconds = &lt; timeout_in_milliseconds&gt;</span><span class="sxs-lookup"><span data-stu-id="7d115-203">$config.SyncTimeoutInMilliseconds = &lt;timeout_in_milliseconds&gt;</span></span></p>
    <p><span data-ttu-id="7d115-204">$config. Put ()</span><span class="sxs-lookup"><span data-stu-id="7d115-204">$config.Put()</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7d115-205">Setzen Sie das Synchronisierungs Timeout in Millisekunden.</span><span class="sxs-lookup"><span data-stu-id="7d115-205">Set the synchronization timeout in milliseconds.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="7d115-206">$config = Get-WMIObject-Namespace root\Microsoft\UEV ComputerConfiguration</span><span class="sxs-lookup"><span data-stu-id="7d115-206">$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</span></span></p>
    <p><span data-ttu-id="7d115-207">$config. MaxPackageSizeInBytes = &lt; size_in_bytes&gt;</span><span class="sxs-lookup"><span data-stu-id="7d115-207">$config.MaxPackageSizeInBytes = &lt;size_in_bytes&gt;</span></span></p>
    <p><span data-ttu-id="7d115-208">$config. Put ()</span><span class="sxs-lookup"><span data-stu-id="7d115-208">$config.Put()</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7d115-209">Konfigurieren Sie den UE-V-Agent so, dass er meldet, wenn die Dateigröße eines Einstellungen-Pakets einen definierten Schwellenwert erreicht.</span><span class="sxs-lookup"><span data-stu-id="7d115-209">Configure the UE-V agent to report when a settings package file size reaches a defined threshold.</span></span> <span data-ttu-id="7d115-210">Legen Sie die Schwellenwert-Paketdatei Größe in Bytes fest.</span><span class="sxs-lookup"><span data-stu-id="7d115-210">Set the threshold package file size in bytes.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="7d115-211">$config = Get-WMIObject-Namespace root\Microsoft\UEV ComputerConfiguration</span><span class="sxs-lookup"><span data-stu-id="7d115-211">$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</span></span></p>
    <p><span data-ttu-id="7d115-212">$config. SyncMethod = &lt; sync_method&gt;</span><span class="sxs-lookup"><span data-stu-id="7d115-212">$config.SyncMethod = &lt;sync_method&gt;</span></span></p>
    <p><span data-ttu-id="7d115-213">$config. Put ()</span><span class="sxs-lookup"><span data-stu-id="7d115-213">$config.Put()</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7d115-214">Setzen Sie die Synchronisierungsmethode: Offlinedateien oder None.</span><span class="sxs-lookup"><span data-stu-id="7d115-214">Set the synchronization method: OfflineFiles or None.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="7d115-215">$config = Get-WMIObject-Namespace root\Microsoft\UEV ComputerConfiguration</span><span class="sxs-lookup"><span data-stu-id="7d115-215">$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</span></span></p>
    <p><span data-ttu-id="7d115-216">$config. &lt; Einstellungs &gt;  =  &lt; Wert für Name&gt;</span><span class="sxs-lookup"><span data-stu-id="7d115-216">$config.&lt;setting name&gt; = &lt;setting value&gt;</span></span></p>
    <p><span data-ttu-id="7d115-217">$config. Put ()</span><span class="sxs-lookup"><span data-stu-id="7d115-217">$config.Put()</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7d115-218">Aktualisieren Sie eine bestimmte Einstellung pro Computer.</span><span class="sxs-lookup"><span data-stu-id="7d115-218">Update a specific per-computer setting.</span></span> <span data-ttu-id="7d115-219">Verwenden Sie $NULL als Einstellungswert, um die Einstellung zu löschen.</span><span class="sxs-lookup"><span data-stu-id="7d115-219">To clear the setting, use $null as the setting value.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="7d115-220">$config = Get-WMIObject-Namespace root\Microsoft\UEV ComputerConfiguration</span><span class="sxs-lookup"><span data-stu-id="7d115-220">$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</span></span></p>
    <p><span data-ttu-id="7d115-221">$config. &lt; Einstellungs &gt;  =  &lt; Wert für Name&gt;</span><span class="sxs-lookup"><span data-stu-id="7d115-221">$config.&lt;setting name&gt; = &lt;setting value&gt;</span></span></p>
    <p><span data-ttu-id="7d115-222">$config. Put ()</span><span class="sxs-lookup"><span data-stu-id="7d115-222">$config.Put()</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7d115-223">Aktualisieren einer bestimmten Einstellung für jeden Benutzer</span><span class="sxs-lookup"><span data-stu-id="7d115-223">Update a specific per-user setting.</span></span> <span data-ttu-id="7d115-224">Verwenden Sie $NULL als Einstellungswert, um die Einstellung zu löschen.</span><span class="sxs-lookup"><span data-stu-id="7d115-224">To clear the setting, use $null as the setting value.</span></span></p></td>
    </tr>
    </tbody>
    </table>



~~~
Upon configuration of the UE-V Agent with WMI and PowerShell, the defined configuration is stored in the registry in the following locations:

`\HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\UEV\Agent\Configuration`

`\HKEY_CURRENT_USER\SOFTWARE\Microsoft\UEV\Agent\Configuration`
~~~

## <span data-ttu-id="7d115-225">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="7d115-225">Related topics</span></span>


[<span data-ttu-id="7d115-226">Verwalten von UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="7d115-226">Administering UE-V 1.0</span></span>](administering-ue-v-10.md)

[<span data-ttu-id="7d115-227">Vorgänge für UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="7d115-227">Operations for UE-V 1.0</span></span>](operations-for-ue-v-10.md)









