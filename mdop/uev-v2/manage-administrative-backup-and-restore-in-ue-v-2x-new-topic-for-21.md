---
title: Verwalten der administrativen Sicherung und Wiederherstellung in UE-V 2. x
description: Verwalten der administrativen Sicherung und Wiederherstellung in UE-V 2. x
author: dansimp
ms.assetid: 2eb5ae75-65e5-4afc-adb6-4e83cf4364ae
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 11c168b54b71731c51417b2b7c4737c85f42035a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812325"
---
# <span data-ttu-id="017a7-103">Verwalten der administrativen Sicherung und Wiederherstellung in UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="017a7-103">Manage Administrative Backup and Restore in UE-V 2.x</span></span>


<span data-ttu-id="017a7-104">Als Administrator von Microsoft User Experience Virtualization (UE-V) 2,0, 2,1 oder 2,1 SP1 können Sie die Anwendungs-und Windows-Einstellungen in Ihrem ursprünglichen Zustand wiederherstellen.</span><span class="sxs-lookup"><span data-stu-id="017a7-104">As an administrator of Microsoft User Experience Virtualization (UE-V) 2.0, 2.1, or 2.1 SP1, you can restore application and Windows settings to their original state.</span></span> <span data-ttu-id="017a7-105">Und neu in UE-V 2,1 können Sie auch zusätzliche Einstellungen wiederherstellen, wenn ein Benutzer ein neues Gerät annimmt.</span><span class="sxs-lookup"><span data-stu-id="017a7-105">And new in UE-V 2.1, you can also restore additional settings when a user adopts a new device.</span></span>

## <span data-ttu-id="017a7-106">Wiederherstellen von Einstellungen in UE-v 2,1 oder UE-v 2,1 SP1, wenn ein Benutzer ein neues Gerät annimmt</span><span class="sxs-lookup"><span data-stu-id="017a7-106">Restore Settings in UE-V 2.1 or UE-V 2.1 SP1 when a User Adopts a New Device</span></span>


<span data-ttu-id="017a7-107">Wenn Sie die Einstellungen wiederherstellen möchten, wenn ein Benutzer ein neues Gerät annimmt, können Sie eine Vorlage für die Einstellungen-Position im **Backup** -oder Roam-Profil **(Standard)** mit dem PowerShell-Cmdlet "UevTemplateProfile" setzen.</span><span class="sxs-lookup"><span data-stu-id="017a7-107">To restore settings when a user adopts a new device, you can put a settings location template in **backup** or **roam (default)** profile using the Set-UevTemplateProfile PowerShell cmdlet.</span></span> <span data-ttu-id="017a7-108">Auf diese Weise können Computereinstellungen zusätzlich zu den Benutzereinstellungen mit dem neuen Computer synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="017a7-108">This lets computer settings sync to the new computer, in addition to user settings.</span></span> <span data-ttu-id="017a7-109">Vorlagen, die dem Sicherungsprofil zugewiesen sind, werden für dieses Gerät gesichert und auf Gerätebasis konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="017a7-109">Templates assigned to the backup profile are backed up for that device and configured on a per-device basis.</span></span> <span data-ttu-id="017a7-110">Verwenden Sie zum Sichern von Einstellungen für eine Vorlage das folgende Cmdlet in Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="017a7-110">To backup settings for a template, use the following cmdlet in Windows PowerShell:</span></span>

``` syntax
Set-UevTemplateProfile -ID <TemplateID> -Profile <backup>
```

-   <span data-ttu-id="017a7-111">&lt;Vorlagen &gt; -ID ist die UE-V-Vorlagen-ID</span><span class="sxs-lookup"><span data-stu-id="017a7-111">&lt;TemplateID&gt; is the UE-V Template ID</span></span>

-   <span data-ttu-id="017a7-112">&lt;Backup &gt; kann entweder ein Backup oder ein Roaming sein</span><span class="sxs-lookup"><span data-stu-id="017a7-112">&lt;backup&gt; can either be Backup or Roaming</span></span>

<span data-ttu-id="017a7-113">Beim Ersetzen des Geräts eines Benutzers werden die Einstellungen von UE-V automatisch wiederhergestellt, wenn die Domäne, der Benutzername und der Gerätename des Benutzers übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="017a7-113">When replacing a user’s device UE-V automatically restores settings if the user’s domain, username, and device name all match.</span></span> <span data-ttu-id="017a7-114">Alle synchronisierten und alle Sicherungsdaten werden auf dem Gerät automatisch wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="017a7-114">All synchronized and any backup data is restored on the device automatically.</span></span>

<span data-ttu-id="017a7-115">Sie können auch das neue PowerShell-Cmdlet Restore-UevBackup verwenden, um die Einstellungen von einem anderen Gerät wiederherzustellen.</span><span class="sxs-lookup"><span data-stu-id="017a7-115">You can also use the new PowerShell cmdlet, Restore-UevBackup, to restore settings from a different device.</span></span> <span data-ttu-id="017a7-116">Wenn Sie die Einstellungs Pakete für das neue Gerät Klonen möchten, verwenden Sie das folgende Cmdlet in Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="017a7-116">To clone the settings packages for the new device, use the following cmdlet in Windows PowerShell:</span></span>

``` syntax
Restore-UevBackup –Machine <MachineName>
```

<span data-ttu-id="017a7-117">dabei &lt; &gt; ist MachineName der Computername des Geräts.</span><span class="sxs-lookup"><span data-stu-id="017a7-117">where &lt;MachineName&gt; is the computer name of the device.</span></span>

<span data-ttu-id="017a7-118">Vorlagen wie die Office 2013-Vorlage, die viele Anwendungen beinhalten, können entweder alle in das Roaming (Standard) oder ein gesichertes Profil aufgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="017a7-118">Templates such as the Office 2013 template that include many applications can either all be included in the roamed (default) or backed up profile.</span></span> <span data-ttu-id="017a7-119">Einzelne apps in einer vorlagensuite Folgen der Gruppe.</span><span class="sxs-lookup"><span data-stu-id="017a7-119">Individual apps in a template suite follow the group.</span></span> <span data-ttu-id="017a7-120">Office 2013 in-Box-Vorlagen beinhalten sowohl Roaming-als auch nur-Backup-Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="017a7-120">Office 2013 in-box templates include both roaming and backup-only settings.</span></span> <span data-ttu-id="017a7-121">Backup-Only-Einstellungen können nicht in ein Roaming-Profil aufgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="017a7-121">Backup-only settings cannot be included in a roaming profile.</span></span>

<span data-ttu-id="017a7-122">Im Rahmen des Sicherungs-und Wiederherstellungsfeatures hat UE-V die Optionen für das Rollback zu den Einstellungen als **Letztes bekanntes gut (LKG)** hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="017a7-122">As part of the Backup/Restore feature, UE-V added **last known good (LKG)** to the options for rolling back to settings.</span></span> <span data-ttu-id="017a7-123">In dieser Version können Sie die ursprünglichen Einstellungen oder LKG-Einstellungen wiederherstellen.</span><span class="sxs-lookup"><span data-stu-id="017a7-123">In this release, you can roll back to either the original settings or LKG settings.</span></span> <span data-ttu-id="017a7-124">Mit den LKG-Einstellungen können Benutzer einen zwischen-und einen stabilen Punkt vor dem Zustand Pre-UE-V der Einstellungen wiederherstellen.</span><span class="sxs-lookup"><span data-stu-id="017a7-124">The LKG settings let users roll back to an intermediate and stable point ahead of the pre-UE-V state of the settings.</span></span>

### <span data-ttu-id="017a7-125">So wird es gemacht: Sichern/Wiederherstellen von Vorlagen mit UE-V</span><span class="sxs-lookup"><span data-stu-id="017a7-125">How to Backup/Restore Templates with UE-V</span></span>

<span data-ttu-id="017a7-126">Hierbei handelt es sich um die wichtigsten Sicherungs-und Wiederherstellungskomponenten von UE-V:</span><span class="sxs-lookup"><span data-stu-id="017a7-126">These are the key backup and restore components of UE-V:</span></span>

-   <span data-ttu-id="017a7-127">Vorlagen profile</span><span class="sxs-lookup"><span data-stu-id="017a7-127">Template profiles</span></span>

-   <span data-ttu-id="017a7-128">Speicherort der Einstellungs Pakete in der Vorlage "Einstellungen-Speicherort"</span><span class="sxs-lookup"><span data-stu-id="017a7-128">Settings packages location within the Settings Storage Location template</span></span>

-   <span data-ttu-id="017a7-129">Sicherungs Trigger</span><span class="sxs-lookup"><span data-stu-id="017a7-129">Backup trigger</span></span>

-   <span data-ttu-id="017a7-130">Wiederherstellen von Einstellungen</span><span class="sxs-lookup"><span data-stu-id="017a7-130">How settings are restored</span></span>

**<span data-ttu-id="017a7-131">Vorlagen profile</span><span class="sxs-lookup"><span data-stu-id="017a7-131">Template Profiles</span></span>**

<span data-ttu-id="017a7-132">Ein UE-V-Vorlagenprofil wird definiert, wenn die Vorlage auf dem Gerät registriert oder über das PowerShell/WMI-Konfigurationsdienstprogramm nach der Registrierung bereit steht.</span><span class="sxs-lookup"><span data-stu-id="017a7-132">A UE-V template profile is defined when the template is registered on the device or post registration through the PowerShell/WMI configuration utility.</span></span> <span data-ttu-id="017a7-133">Zu den Profiltypen gehören:</span><span class="sxs-lookup"><span data-stu-id="017a7-133">The profile types include:</span></span>

-   <span data-ttu-id="017a7-134">Roaming (Standard)</span><span class="sxs-lookup"><span data-stu-id="017a7-134">Roaming (default)</span></span>

-   <span data-ttu-id="017a7-135">Sicherung</span><span class="sxs-lookup"><span data-stu-id="017a7-135">Backup</span></span>

-   <span data-ttu-id="017a7-136">Nach unten</span><span class="sxs-lookup"><span data-stu-id="017a7-136">BackupOnly</span></span>

<span data-ttu-id="017a7-137">Wenn Sie registriert sind, werden alle Vorlagen in das Roaming-Profil aufgenommen, sofern nicht anders angegeben.</span><span class="sxs-lookup"><span data-stu-id="017a7-137">All templates are included in the roaming profile when registered unless otherwise specified.</span></span> <span data-ttu-id="017a7-138">Mit diesen Vorlagen werden die Einstellungen für alle UE-V-aktivierten Geräte synchronisiert, wobei die entsprechende Vorlage aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="017a7-138">These templates synchronize settings to all UE-V enabled devices with the corresponding template enabled.</span></span>

<span data-ttu-id="017a7-139">Vorlagen können mithilfe des Cmdlets "Satz-UevTemplateProfile" zum Sicherungsprofil mit PowerShell oder WMI hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="017a7-139">Templates can be added to the Backup Profile with PowerShell or WMI using the Set-UevTemplateProfile cmdlet.</span></span> <span data-ttu-id="017a7-140">Vorlagen im Sicherungsprofil sichern Sie diese Einstellungen auf den Speicherort für Einstellungen in einem speziellen Verzeichnis für Gerätenamen.</span><span class="sxs-lookup"><span data-stu-id="017a7-140">Templates in the Backup Profile back up these settings to the Settings Storage Location in a special Device name directory.</span></span> <span data-ttu-id="017a7-141">Die angegebenen Einstellungen werden an diesem Speicherort gesichert.</span><span class="sxs-lookup"><span data-stu-id="017a7-141">Specified settings are backed up to this location.</span></span>

<span data-ttu-id="017a7-142">Vorlagen, die für das betreffende Gerät zu einem bestimmten Zeitpunkt vorgesehen sind, sollten nur dann synchronisiert werden, wenn Sie explizit wiederhergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="017a7-142">Templates designated BackupOnly include settings specific to that device that should not be synchronized unless explicitly restored.</span></span> <span data-ttu-id="017a7-143">Diese Einstellungen werden im gleichen gerätespezifischen Einstellungen-Paketspeicherort auf dem Speicherstandort "Einstellungen" als gesicherten-Einstellungen gespeichert.</span><span class="sxs-lookup"><span data-stu-id="017a7-143">These settings are stored in the same device-specific settings package location on the settings storage location as the Backedup Settings.</span></span> <span data-ttu-id="017a7-144">Für diese Vorlagen ist in der Vorlage ein spezieller Bezeichner eingebettet, der angibt, dass Sie Teil dieses Profils sein sollen.</span><span class="sxs-lookup"><span data-stu-id="017a7-144">These templates have a special identifier embedded in the template that specifies they should be part of this profile.</span></span>

**<span data-ttu-id="017a7-145">Speicherort der Einstellungs Pakete in der Vorlage "Einstellungen-Speicherort"</span><span class="sxs-lookup"><span data-stu-id="017a7-145">Settings packages location within the Settings Storage Location template</span></span>**

<span data-ttu-id="017a7-146">Einstellungen für das Roaming-Profil werden am Speicherort der Einstellungen gespeichert.</span><span class="sxs-lookup"><span data-stu-id="017a7-146">Roaming Profile settings are stored on the settings storage location.</span></span> <span data-ttu-id="017a7-147">Vorlagen, die der Sicherung oder dem backuponly-Profil zugewiesen sind, speichern Ihre Einstellungen am Speicherort für Einstellungen in einem speziellen Verzeichnis für Gerätenamen.</span><span class="sxs-lookup"><span data-stu-id="017a7-147">Templates assigned to the Backup or the BackupOnly profile store their settings to the Settings Storage Location in a special Device name directory.</span></span> <span data-ttu-id="017a7-148">Jedes Gerät mit Vorlagen in diesen Profilen verfügt über einen eigenen Gerätenamen.</span><span class="sxs-lookup"><span data-stu-id="017a7-148">Each device with templates in these profiles has its own device name.</span></span> <span data-ttu-id="017a7-149">UE-V bereinigt diese Verzeichnisse nicht.</span><span class="sxs-lookup"><span data-stu-id="017a7-149">UE-V does not clean up these directories.</span></span>

**<span data-ttu-id="017a7-150">Sicherungs Trigger</span><span class="sxs-lookup"><span data-stu-id="017a7-150">Backup trigger</span></span>**

<span data-ttu-id="017a7-151">Die Sicherung wird von denselben Ereignissen ausgelöst, die eine UE-V-Synchronisierung auslösen.</span><span class="sxs-lookup"><span data-stu-id="017a7-151">Backup is triggered by the same events that trigger a UE-V synchronization.</span></span>

**<span data-ttu-id="017a7-152">Wiederherstellen von Einstellungen</span><span class="sxs-lookup"><span data-stu-id="017a7-152">How settings are restored</span></span>**

<span data-ttu-id="017a7-153">Durch das Wiederherstellen des Geräts eines Benutzers werden die Einstellungen der aktuell registrierten Vorlage aus dem Sicherungsordner eines anderen Geräts und alle synchronisierten Einstellungen auf dem aktuellen Computer wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="017a7-153">Restoring a user’s device restores the currently registered Template’s settings from another device’s backup folder and all synchronized settings to the current machine.</span></span> <span data-ttu-id="017a7-154">Die Einstellungen werden auf diese zwei Arten wiederhergestellt:</span><span class="sxs-lookup"><span data-stu-id="017a7-154">Settings are restored in these two ways:</span></span>

-   **<span data-ttu-id="017a7-155">Automatische Wiederherstellung</span><span class="sxs-lookup"><span data-stu-id="017a7-155">Automatic restore</span></span>**

    <span data-ttu-id="017a7-156">Wenn die Einstellungen für den Speicherpfad, die Domäne und den Computer Namen des Benutzers mit dem aktuellen Benutzer übereinstimmen, werden alle Einstellungen für diesen Benutzer synchronisiert, wobei nur die neuesten Einstellungen angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="017a7-156">If the user’s UE-V settings storage path, domain, and Computer name match the current user then all of the settings for that user are synchronized, with only the latest settings applied.</span></span> <span data-ttu-id="017a7-157">Wenn sich ein Benutzer zum ersten Mal bei einem neuen Gerät anmeldet und diese Kriterien erfüllt sind, werden die Einstellungsdaten auf dieses Gerät angewendet.</span><span class="sxs-lookup"><span data-stu-id="017a7-157">If a user logs on to a new device for the first time and these criteria are met, the settings data is applied to that device.</span></span>

    **<span data-ttu-id="017a7-158">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="017a7-158">Note</span></span>**  
    <span data-ttu-id="017a7-159">Die Einstellungen für Barrierefreiheit und Windows-Desktop erfordern, dass der Benutzer sich erneut bei Windows anmeldet, um angewendet zu werden.</span><span class="sxs-lookup"><span data-stu-id="017a7-159">Accessibility and Windows Desktop settings require the user to re-logon to Windows to be applied.</span></span>



-   **<span data-ttu-id="017a7-160">Manuelle Wiederherstellung</span><span class="sxs-lookup"><span data-stu-id="017a7-160">Manual Restore</span></span>**

    <span data-ttu-id="017a7-161">Wenn Sie Benutzer beim Wiederherstellen eines Geräts während einer Aktualisierung unterstützen möchten, können Sie das Cmdlet Restore-UevBackup verwenden.</span><span class="sxs-lookup"><span data-stu-id="017a7-161">If you want to assist users by restoring a device during a refresh, you can choose to use the Restore-UevBackup cmdlet.</span></span> <span data-ttu-id="017a7-162">Dieser Befehl bewirkt, dass die Einstellungen des Benutzers vom Speicherort für Einstellungen heruntergeladen werden.</span><span class="sxs-lookup"><span data-stu-id="017a7-162">This command causes the user’s settings to be downloaded from the Settings Storage Location.</span></span>

## <span data-ttu-id="017a7-163">Wiederherstellen von Anwendungs-und Windows-Einstellungen auf den ursprünglichen Zustand</span><span class="sxs-lookup"><span data-stu-id="017a7-163">Restore Application and Windows Settings to Original State</span></span>


<span data-ttu-id="017a7-164">Mit WMI-und Windows PowerShell-Befehlen können Sie die Anwendungs-und Windows-Einstellungen auf die Einstellungswerte zurücksetzen, die sich auf dem Computer befanden, als die Anwendung zum ersten Mal gestartet wurde, nachdem der UE-V-Agent installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="017a7-164">WMI and Windows PowerShell commands let you restore application and Windows settings to the settings values that were on the computer the first time that the application started after the UE-V Agent was installed.</span></span> <span data-ttu-id="017a7-165">Diese Wiederherstellungsaktion wird für einzelne Anwendungs-oder Windows-Einstellungen ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="017a7-165">This restoring action is performed on a per-application or Windows settings basis.</span></span> <span data-ttu-id="017a7-166">Die Einstellungen werden beim nächsten Ausführen der Anwendung wiederhergestellt, oder die Einstellungen werden wiederhergestellt, wenn sich der Benutzer beim Betriebssystem anmeldet.</span><span class="sxs-lookup"><span data-stu-id="017a7-166">The settings are restored the next time that the application runs, or the settings are restored when the user logs on to the operating system.</span></span>

**<span data-ttu-id="017a7-167">So stellen Sie Anwendungseinstellungen und Windows-Einstellungen mit Windows PowerShell für UE-V 2. x wieder her</span><span class="sxs-lookup"><span data-stu-id="017a7-167">To restore application settings and Windows settings with Windows PowerShell for UE-V 2.x</span></span>**

1.  <span data-ttu-id="017a7-168">Öffnen Sie das Windows PowerShell-Fenster.</span><span class="sxs-lookup"><span data-stu-id="017a7-168">Open the Windows PowerShell window.</span></span>

2.  <span data-ttu-id="017a7-169">Geben Sie das folgende Windows PowerShell-Cmdlet ein, um die Anwendungseinstellungen und Windows-Einstellungen wiederherzustellen.</span><span class="sxs-lookup"><span data-stu-id="017a7-169">Enter the following Windows PowerShell cmdlet to restore the application settings and Windows settings.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong><span data-ttu-id="017a7-170">Windows PowerShell-Cmdlet</span><span class="sxs-lookup"><span data-stu-id="017a7-170">Windows PowerShell cmdlet</span></span></strong></th>
    <th align="left"><strong><span data-ttu-id="017a7-171">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="017a7-171">Description</span></span></strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><code>Restore-UevUserSetting -&lt;TemplateID&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="017a7-172">Wiederherstellen der Benutzereinstellungen für eine Anwendung oder Wiederherstellen einer Gruppe von Windows-Einstellungen</span><span class="sxs-lookup"><span data-stu-id="017a7-172">Restores the user settings for an application or restores a group of Windows settings.</span></span></p></td>
    </tr>
    </tbody>
    </table>



**<span data-ttu-id="017a7-173">So stellen Sie Anwendungseinstellungen und Windows-Einstellungen mit WMI wieder her</span><span class="sxs-lookup"><span data-stu-id="017a7-173">To restore application settings and Windows settings with WMI</span></span>**

1.  <span data-ttu-id="017a7-174">Öffnen Sie ein Windows PowerShell-Fenster.</span><span class="sxs-lookup"><span data-stu-id="017a7-174">Open a Windows PowerShell window.</span></span>

2.  <span data-ttu-id="017a7-175">Geben Sie den folgenden WMI-Befehl ein, um Anwendungseinstellungen und Windows-Einstellungen wiederherzustellen.</span><span class="sxs-lookup"><span data-stu-id="017a7-175">Enter the following WMI command to restore application settings and Windows settings.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong><span data-ttu-id="017a7-176">WMI-Befehl</span><span class="sxs-lookup"><span data-stu-id="017a7-176">WMI command</span></span></strong></th>
    <th align="left"><strong><span data-ttu-id="017a7-177">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="017a7-177">Description</span></span></strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class UserSettings -Name RestoreByTemplateId -ArgumentList &lt;template_ID&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="017a7-178">Wiederherstellen der Benutzereinstellungen für eine Anwendung oder Wiederherstellen einer Gruppe von Windows-Einstellungen</span><span class="sxs-lookup"><span data-stu-id="017a7-178">Restores the user settings for an application or restores a group of Windows settings.</span></span></p></td>
    </tr>
    </tbody>
    </table>



~~~
**Note**  
UE-V does not provide a settings rollback for Windows apps.
~~~








## <span data-ttu-id="017a7-179">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="017a7-179">Related topics</span></span>


[<span data-ttu-id="017a7-180">Verwalten von UE-V 2. x mit Windows PowerShell und WMI</span><span class="sxs-lookup"><span data-stu-id="017a7-180">Administering UE-V 2.x with Windows PowerShell and WMI</span></span>](administering-ue-v-2x-with-windows-powershell-and-wmi-both-uevv2.md)

[<span data-ttu-id="017a7-181">Verwalten von UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="017a7-181">Administering UE-V 2.x</span></span>](administering-ue-v-2x-new-uevv2.md)









