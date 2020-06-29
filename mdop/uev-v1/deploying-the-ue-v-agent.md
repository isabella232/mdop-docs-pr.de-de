---
title: Bereitstellen von UE-V-Agent
description: Bereitstellen von UE-V-Agent
author: dansimp
ms.assetid: ec1c16c4-4be0-41ff-93bc-3e2b1afb5832
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 19f3b798ad7d3a43b0a274a25dd97b651435de51
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812202"
---
# <span data-ttu-id="2cbb8-103">Bereitstellen von UE-V-Agent</span><span class="sxs-lookup"><span data-stu-id="2cbb8-103">Deploying the UE-V Agent</span></span>


<span data-ttu-id="2cbb8-104">Der Microsoft User Experience Virtualization (UE-v)-Agent muss auf jedem Computer ausgeführt werden, auf dem UE-v verwendet wird, um die Anwendungs-und Windows-Einstellungen zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="2cbb8-104">The Microsoft User Experience Virtualization (UE-V) agent must run on each computer that uses UE-V to roam application and Windows settings.</span></span> <span data-ttu-id="2cbb8-105">Eine einzelne Installationsdatei, AgentSetup.exe, installiert den UE-V-Agent sowohl auf 32-als auch 64-Bit-Betriebssystemen.</span><span class="sxs-lookup"><span data-stu-id="2cbb8-105">A single installer file, AgentSetup.exe, installs the UE-V agent on both 32-bit and 64-bit operating systems.</span></span> <span data-ttu-id="2cbb8-106">Die Befehlszeilenparameter des UE-V-Agents lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="2cbb8-106">The command-line parameters of the UE-V Agent are the following:</span></span>

**<span data-ttu-id="2cbb8-107">AgentSetup.exe Befehlszeilenparameter</span><span class="sxs-lookup"><span data-stu-id="2cbb8-107">AgentSetup.exe command-line parameters</span></span>**

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="2cbb8-108">Befehlszeilenparameter</span><span class="sxs-lookup"><span data-stu-id="2cbb8-108">Command-line parameter</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="2cbb8-109">Definition</span><span class="sxs-lookup"><span data-stu-id="2cbb8-109">Definition</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="2cbb8-110">Anmerkungen</span><span class="sxs-lookup"><span data-stu-id="2cbb8-110">Notes</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2cbb8-111">/Help oder/h oder/?</span><span class="sxs-lookup"><span data-stu-id="2cbb8-111">/help or /h or /?</span></span></p></td>
<td align="left"><p><span data-ttu-id="2cbb8-112">Zeigt das Dialogfeld "AgentSetup.exe Verwendung" an.</span><span class="sxs-lookup"><span data-stu-id="2cbb8-112">Displays the AgentSetup.exe usage dialog.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2cbb8-113">SettingsStoragePath</span><span class="sxs-lookup"><span data-stu-id="2cbb8-113">SettingsStoragePath</span></span></p></td>
<td align="left"><p><span data-ttu-id="2cbb8-114">Gibt den UNC-Pfad (Universal Naming Convention) an, der definiert, wo die Einstellungen gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="2cbb8-114">Indicates the Universal Naming Convention (UNC) path that defines where settings are stored.</span></span></p></td>
<td align="left"><p><span data-ttu-id="2cbb8-115">% Username% oder% Computername% Umgebungsvariablen werden akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="2cbb8-115">%username% or %computername% environment variables are accepted.</span></span> <span data-ttu-id="2cbb8-116">Für Skripts sind möglicherweise Escape-Variablen erforderlich.</span><span class="sxs-lookup"><span data-stu-id="2cbb8-116">Scripting may require escaped variables.</span></span></p>
<p><strong><span data-ttu-id="2cbb8-117">Standard </strong> : &lt; None &gt; (Active Directory-Benutzer Start)</span><span class="sxs-lookup"><span data-stu-id="2cbb8-117">Default</strong>: &lt;none&gt; (Active Directory user home)</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2cbb8-118">SettingsTemplateCatalogPath</span><span class="sxs-lookup"><span data-stu-id="2cbb8-118">SettingsTemplateCatalogPath</span></span></p></td>
<td align="left"><p><span data-ttu-id="2cbb8-119">Gibt den UNC-Pfad (Universal Naming Convention) an, der den Speicherort definiert, der auf neue Einstellungen für Standort Vorlagen überprüft wurde.</span><span class="sxs-lookup"><span data-stu-id="2cbb8-119">Indicates the Universal Naming Convention (UNC) path that defines the location that was checked for new settings location templates.</span></span></p></td>
<td align="left"><p><span data-ttu-id="2cbb8-120">Nur für benutzerdefinierte Einstellungen für Standort Vorlagen erforderlich</span><span class="sxs-lookup"><span data-stu-id="2cbb8-120">Only required for custom settings location templates</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2cbb8-121">RegisterMSTemplates</span><span class="sxs-lookup"><span data-stu-id="2cbb8-121">RegisterMSTemplates</span></span></p></td>
<td align="left"><p><span data-ttu-id="2cbb8-122">Gibt an, ob die Microsoft-Standardvorlagen während der Installation registriert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="2cbb8-122">Specifies whether the default Microsoft templates should be registered during installation.</span></span></p></td>
<td align="left"><p><span data-ttu-id="2cbb8-123">True | False</span><span class="sxs-lookup"><span data-stu-id="2cbb8-123">True | False</span></span></p>
<p><strong><span data-ttu-id="2cbb8-124">Standard </strong> : true</span><span class="sxs-lookup"><span data-stu-id="2cbb8-124">Default</strong>: True</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2cbb8-125">SyncMethod</span><span class="sxs-lookup"><span data-stu-id="2cbb8-125">SyncMethod</span></span></p></td>
<td align="left"><p><span data-ttu-id="2cbb8-126">Gibt an, welche Synchronisierungsmethode verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="2cbb8-126">Specifies which synchronization method should be used.</span></span></p></td>
<td align="left"><p><span data-ttu-id="2cbb8-127">Offlinedateien | Keine</span><span class="sxs-lookup"><span data-stu-id="2cbb8-127">OfflineFiles | None</span></span></p>
<p><strong><span data-ttu-id="2cbb8-128">Standard </strong> : Offlinedateien</span><span class="sxs-lookup"><span data-stu-id="2cbb8-128">Default</strong>: OfflineFiles</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2cbb8-129">SyncTimeoutInMilliseconds</span><span class="sxs-lookup"><span data-stu-id="2cbb8-129">SyncTimeoutInMilliseconds</span></span></p></td>
<td align="left"><p><span data-ttu-id="2cbb8-130">Gibt die Anzahl der Millisekunden an, die der Computer vor dem Timeout wartet, wenn er Benutzereinstellungen vom Speicherort für Einstellungen abruft.</span><span class="sxs-lookup"><span data-stu-id="2cbb8-130">Specifies the number of milliseconds that the computer waits before timeout when it retrieves user settings from the settings storage location.</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="2cbb8-131">Standard </strong> : 2000 Millisekunden</span><span class="sxs-lookup"><span data-stu-id="2cbb8-131">Default</strong>: 2000 milliseconds</span></span></p>
<p><span data-ttu-id="2cbb8-132">(bis zu 2 Sekunden warten)</span><span class="sxs-lookup"><span data-stu-id="2cbb8-132">(wait up to 2 seconds)</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2cbb8-133">SyncEnabled</span><span class="sxs-lookup"><span data-stu-id="2cbb8-133">SyncEnabled</span></span></p></td>
<td align="left"><p><span data-ttu-id="2cbb8-134">Gibt an, ob die UE-V-Synchronisierung aktiviert oder deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="2cbb8-134">Specifies whether UE-V synchronization is enabled or disabled.</span></span></p></td>
<td align="left"><p><span data-ttu-id="2cbb8-135">True | False</span><span class="sxs-lookup"><span data-stu-id="2cbb8-135">True | False</span></span></p>
<p><strong><span data-ttu-id="2cbb8-136">Standard </strong> : true</span><span class="sxs-lookup"><span data-stu-id="2cbb8-136">Default</strong>: True</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2cbb8-137">MaxPackageSizeInBytes</span><span class="sxs-lookup"><span data-stu-id="2cbb8-137">MaxPackageSizeInBytes</span></span></p></td>
<td align="left"><p><span data-ttu-id="2cbb8-138">Gibt eine Dateigröße des Einstellungen-Pakets in Byte an, wenn der UE-V-Agent meldet, dass Dateien den Schwellenwert überschreiten.</span><span class="sxs-lookup"><span data-stu-id="2cbb8-138">Specifies a settings package file size in bytes when the UE-V agent reports that files exceed the threshold.</span></span></p></td>
<td align="left"><p><span data-ttu-id="2cbb8-139">&lt;Größe&gt;</span><span class="sxs-lookup"><span data-stu-id="2cbb8-139">&lt;size&gt;</span></span></p>
<p><strong><span data-ttu-id="2cbb8-140">Standard </strong> : None (kein Warnungsschwellenwert)</span><span class="sxs-lookup"><span data-stu-id="2cbb8-140">Default</strong>: none (no warning threshold)</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2cbb8-141">CEIPEnabled</span><span class="sxs-lookup"><span data-stu-id="2cbb8-141">CEIPEnabled</span></span></p></td>
<td align="left"><p><span data-ttu-id="2cbb8-142">Gibt die Einstellung für die Teilnahme am Programm zur Verbesserung der Benutzerfreundlichkeit an.</span><span class="sxs-lookup"><span data-stu-id="2cbb8-142">Specifies the setting for participation in the Customer Experience Improvement program.</span></span> <span data-ttu-id="2cbb8-143">Wenn die Einstellung auf "true" festgelegt ist, werden die Installationsinformationen auf die Microsoft-Website zur Verbesserung der Benutzerfreundlichkeit hochgeladen.</span><span class="sxs-lookup"><span data-stu-id="2cbb8-143">If set to true, then installer information is uploaded to the Microsoft Customer Experience Improvement Program site.</span></span> <span data-ttu-id="2cbb8-144">Wenn Sie auf "false" festgelegt ist, werden keine Informationen hochgeladen.</span><span class="sxs-lookup"><span data-stu-id="2cbb8-144">If set to false, then no information is uploaded.</span></span></p></td>
<td align="left"><p><span data-ttu-id="2cbb8-145">True | False</span><span class="sxs-lookup"><span data-stu-id="2cbb8-145">True | False</span></span></p>
<p><strong><span data-ttu-id="2cbb8-146">Standard </strong> : falsch</span><span class="sxs-lookup"><span data-stu-id="2cbb8-146">Default</strong>: False</span></span></p>
<p><strong><span data-ttu-id="2cbb8-147">Unter Windows 7 </strong> : true</span><span class="sxs-lookup"><span data-stu-id="2cbb8-147">On Windows 7</strong>: True</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="2cbb8-148">Während der Installation gibt der SettingsStoragePath-Befehlszeilenparameter den Speicherort für Einstellungen für die Einstellungswerte an.</span><span class="sxs-lookup"><span data-stu-id="2cbb8-148">During installation, the SettingsStoragePath command-line parameter specifies the settings storage location for the settings values.</span></span> <span data-ttu-id="2cbb8-149">Vor der Bereitstellung des UE-V-Agents kann ein Einstellungs Speicherort definiert werden.</span><span class="sxs-lookup"><span data-stu-id="2cbb8-149">A settings storage location can be defined before deploying the UE-V Agent.</span></span> <span data-ttu-id="2cbb8-150">Wenn kein Speicherort für Einstellungen festgelegt ist, verwendet UE-V das Active Directory-Benutzerstammverzeichnis als Speicherort für Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="2cbb8-150">If no settings storage location is defined, then UE-V uses the Active Directory user Home Directory as the settings storage location.</span></span> <span data-ttu-id="2cbb8-151">Wenn Sie während des Setups die SettingsStoragePath-Konfiguration angeben und den% username% als Teil des Werts verwenden, wird dadurch dieselbe Benutzereinstellungen-Oberfläche auf allen Computern oder Sitzungen durchlaufen, bei denen sich ein Benutzer anmeldet.</span><span class="sxs-lookup"><span data-stu-id="2cbb8-151">When you specify the SettingsStoragePath configuration during setup and use the %username% as part of the value, this will roam the same user settings experience on all computers or sessions that a user logs into.</span></span> <span data-ttu-id="2cbb8-152">Wenn Sie die%username%\\%Computername%-Variablen als Teil des SettingsStoragePath-Werts angeben, bleibt die Einstellungs Oberfläche für jeden Computer erhalten.</span><span class="sxs-lookup"><span data-stu-id="2cbb8-152">If you specify the %username%\\%computername% variables as part of the SettingsStoragePath value, this will preserve the settings experience for each computer.</span></span>

<span data-ttu-id="2cbb8-153">Architekturspezifische Windows Installer-Dateien (MSI) werden für die UE-V-Agent-Installation zusätzlich zum kombinierten 32-Bit-und 64-Bit-Installationsprogramm bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="2cbb8-153">Architecture-specific Windows Installer (.msi) files are provided for the UE-V agent installation in addition to the combined 32-bit and 64-bit installer.</span></span> <span data-ttu-id="2cbb8-154">Die AgentSetupx86.msi-oder AgentSetupx64.msi Installationsdateien sind kleiner als die AgentSetup.exe Datei und können die Agenten Bereitstellungen rationalisieren.</span><span class="sxs-lookup"><span data-stu-id="2cbb8-154">The AgentSetupx86.msi or AgentSetupx64.msi install files are smaller than the AgentSetup.exe file and might streamline the agent deployments.</span></span> <span data-ttu-id="2cbb8-155">Die Befehlszeilenparameter für das AgentSetup.exe-Installationsprogramm werden für die Windows Installer-Installation (MSI) unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2cbb8-155">The command-line parameters for the AgentSetup.exe installer are supported for the Windows Installer (.msi) installation.</span></span>

<span data-ttu-id="2cbb8-156">**Hinweis**  Bei der Installation oder Deinstallation des UE-V-Agents können Sie entweder die AgentSetup.exe-Datei oder die Sie AgentSetup &lt; arch &gt; . msi-Datei verwenden, aber nicht beide.</span><span class="sxs-lookup"><span data-stu-id="2cbb8-156">**Note** During UE-V agent installation or uninstallation you can either use the AgentSetup.exe file or the AgentSetup&lt;arch&gt;.msi file, but not both.</span></span> <span data-ttu-id="2cbb8-157">Die gleiche Datei muss verwendet werden, um den UE-v-Agent zu deinstallieren, wie er zum Installieren des UE-v-Agents verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="2cbb8-157">The same file must be used to uninstall the UE-V Agent as it was used to install the UE-V Agent.</span></span>

 

<span data-ttu-id="2cbb8-158">Achten Sie beim Installieren des UE-V-Agents darauf, das richtige Variablen Format zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="2cbb8-158">Be sure to use the correct variable format when you install the UE-V agent.</span></span> <span data-ttu-id="2cbb8-159">Die folgende Tabelle enthält Beispiele für Bereitstellungsoptionen für die Verwendung der AgentSetup.exe-oder Windows Installer-Installationsdateien (MSI).</span><span class="sxs-lookup"><span data-stu-id="2cbb8-159">The following table provides examples of deployment options for using the AgentSetup.exe or the Windows Installer (.msi) installation files.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="2cbb8-160">Bereitstellungstyp</span><span class="sxs-lookup"><span data-stu-id="2cbb8-160">Deployment type</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="2cbb8-161">Bereitstellungs Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2cbb8-161">Deployment description</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="2cbb8-162">Beispiel</span><span class="sxs-lookup"><span data-stu-id="2cbb8-162">Example</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2cbb8-163">Eingabeaufforderung</span><span class="sxs-lookup"><span data-stu-id="2cbb8-163">Command prompt</span></span></p></td>
<td align="left"><p><span data-ttu-id="2cbb8-164">Wenn Sie den UE-V-Agent über eine Eingabeaufforderung installieren, verwenden Sie das Variable Format% ^ username%.</span><span class="sxs-lookup"><span data-stu-id="2cbb8-164">When you install the UE-V agent from a command prompt, use the %^username% variable format.</span></span> <span data-ttu-id="2cbb8-165">Wenn Anführungszeichen aufgrund von Leerzeichen im Einstellungsspeicher Pfad erforderlich sind, verwenden Sie eine Batchskriptdatei für die Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="2cbb8-165">If quotation marks are needed because of spaces in the settings storage path, use a batch script file for deployment.</span></span></p>
<p></p></td>
<td align="left"><p><code>AgentSetup.exe /quiet /norestart /log &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare%^username%</code></p>
<p></p>
<p><code>msiexec.exe /i &quot;&lt;path to msi file&gt;&quot; /quiet /norestart /l<em>v &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare%^username%</code></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2cbb8-166">Batch Skript</span><span class="sxs-lookup"><span data-stu-id="2cbb8-166">Batch script</span></span></p></td>
<td align="left"><p><span data-ttu-id="2cbb8-167">Wenn Sie den UE-V-Agent aus einer Batchskriptdatei installieren, verwenden Sie das Variable Format%% username%%.</span><span class="sxs-lookup"><span data-stu-id="2cbb8-167">When you install the UE-V Agent from a batch script file, use the %%username%% variable format.</span></span> <span data-ttu-id="2cbb8-168">Wenn Sie diese Installationsmethode verwenden, müssen Sie der Variablen mit den%% Zeichen entkommen.</span><span class="sxs-lookup"><span data-stu-id="2cbb8-168">If you use this install method, you must escape the variable with the %% characters.</span></span> <span data-ttu-id="2cbb8-169">Ohne dieses Zeichen erweitert das Skript die Benutzername-Variable zum Zeitpunkt der Installation, anstatt zur Laufzeit, wodurch UE-V einen einzelnen Einstellungen-Speicherort für alle Benutzer verwendet.</span><span class="sxs-lookup"><span data-stu-id="2cbb8-169">Without this character, the script expands the username variable at install time, rather than at run time, causing UE-V to use a single settings storage location for all users.</span></span></p></td>
<td align="left"><p><code>AgentSetup.exe /quiet /norestart /log &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=&quot;\server\settingsshare%%username%%&quot;</code></p>
<p></p>
<p><code>msiexec.exe /i &quot;&lt;path to msi file&gt;&quot; /quiet /norestart /l</em>v &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=&quot;\server\settingsshare%%username%%&quot;</code></p>
<p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2cbb8-170">PowerShell</span><span class="sxs-lookup"><span data-stu-id="2cbb8-170">PowerShell</span></span></p></td>
<td align="left"><p><span data-ttu-id="2cbb8-171">Wenn Sie den UE-V-Agent über eine PowerShell-Eingabeaufforderung oder ein PowerShell-Skript installieren, verwenden Sie das Variable Format% username%.</span><span class="sxs-lookup"><span data-stu-id="2cbb8-171">When you install the UE-V agent from a PowerShell prompt or PowerShell script, use the %username% variable format.</span></span></p></td>
<td align="left"><p><code>&amp; AgentSetup.exe /quiet /norestart /log &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare%username%</code></p>
<p></p>
<p><code>&amp; msiexec.exe /i &quot;&lt;path to msi file&gt;&quot; /quiet /norestart /l<em>v &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare%username%</code></p>
<p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2cbb8-172">Elektronische Softwareverteilung, wie etwa die Bereitstellung der Configuration Manager-Softwarebereitstellung)</span><span class="sxs-lookup"><span data-stu-id="2cbb8-172">Electronic software distribution, such as deployment of Configuration Manager Software Deployment)</span></span></p></td>
<td align="left"><p><span data-ttu-id="2cbb8-173">Verwenden Sie beim Installieren des UE-V-Agents mit Configuration Manager das Variablen Format ^% username ^%.</span><span class="sxs-lookup"><span data-stu-id="2cbb8-173">When you install the UE-V Agent with Configuration Manager, use the ^%username^% variable format.</span></span></p></td>
<td align="left"><p><code>AgentSetup.exe /quiet /norestart /log &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare^%username^%</code></p>
<p></p>
<p><code>msiexec.exe /i &quot;&lt;path to msi file&gt;&quot; /quiet /norestart /l</em>v &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare^%username^%</code></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="2cbb8-174">**Hinweis**  Für die Installation des U-EV-Agents sind Administrator Rechte erforderlich, und der Computer erfordert einen Neustart, bevor der UE-V-Agent ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="2cbb8-174">**Note** The installation of the U-EV Agent requires Administrator rights and the computer will require a restart before the UE-V agent can run.</span></span>

 

## <span data-ttu-id="2cbb8-175">Bereitstellungsmethoden für UE-V-Agents von einer Netzwerkfreigabe</span><span class="sxs-lookup"><span data-stu-id="2cbb8-175">UE-V Agent deployment methods from a network share</span></span>


<span data-ttu-id="2cbb8-176">Sie können die folgenden Methoden zum Bereitstellen des UE-V-Agents verwenden:</span><span class="sxs-lookup"><span data-stu-id="2cbb8-176">You can use the following methods to deploy the UE-V agent:</span></span>

-   <span data-ttu-id="2cbb8-177">Eine ESD-Lösung (Electronic Software Distribution), die eine Windows Installer-Datei (MSI) installieren kann.</span><span class="sxs-lookup"><span data-stu-id="2cbb8-177">An electronic software distribution (ESD) solution that can install a Windows Installer (.msi) file.</span></span>

-   <span data-ttu-id="2cbb8-178">Ein Installationsskript, das auf die Windows Installer-Datei (MSI) verweist, die zentral auf einer Freigabe gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="2cbb8-178">An installation script that references the Windows Installer (.msi) file that is stored centrally on a share.</span></span>

-   <span data-ttu-id="2cbb8-179">Manuelles Ausführen des Installationsprogramms auf dem Computer.</span><span class="sxs-lookup"><span data-stu-id="2cbb8-179">Manually running the installation program on the computer.</span></span>

<span data-ttu-id="2cbb8-180">Führen Sie die folgenden Schritte aus, um den UE-V-Agent über eine Netzwerkfreigabe bereitzustellen:</span><span class="sxs-lookup"><span data-stu-id="2cbb8-180">To deploy the UE-V agent from a network share, use the following steps:</span></span>

**<span data-ttu-id="2cbb8-181">So installieren und konfigurieren Sie den UE-V-Agent über eine Netzwerkfreigabe</span><span class="sxs-lookup"><span data-stu-id="2cbb8-181">To install and configure the UE-V Agent from a network share</span></span>**

1.  <span data-ttu-id="2cbb8-182">Stufen Sie die Installationsdatei des UE-V-Agents (AgentSetup.exe) auf einer Netzwerkfreigabe ein, auf die Benutzer die Berechtigung "lesen" haben.</span><span class="sxs-lookup"><span data-stu-id="2cbb8-182">Stage the UE-V agent installation file (AgentSetup.exe) on a network share to which users have “read” permission.</span></span>

2.  <span data-ttu-id="2cbb8-183">Stellen Sie ein Skript auf Benutzercomputern bereit, die den UE-V-Agent installieren.</span><span class="sxs-lookup"><span data-stu-id="2cbb8-183">Deploy a script to user computers that installs the UE-V agent.</span></span> <span data-ttu-id="2cbb8-184">Das Skript sollte den Speicherort für Einstellungen angeben.</span><span class="sxs-lookup"><span data-stu-id="2cbb8-184">The script should specify the settings storage location.</span></span>

**<span data-ttu-id="2cbb8-185">Aktualisieren des UE-V-Agents</span><span class="sxs-lookup"><span data-stu-id="2cbb8-185">Update the UE-V Agent</span></span>**

<span data-ttu-id="2cbb8-186">Updates für die UE-V-Agent-Software werden über Microsoft Update bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="2cbb8-186">Updates for the UE-V agent software will be provided through Microsoft Update.</span></span> <span data-ttu-id="2cbb8-187">Bei einem UE-V-Agent-Upgrade kann die Standardgruppe der Einstellungen für den Speicherort für allgemeine Microsoft-Anwendungen und Windows-Einstellungen aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="2cbb8-187">During a UE-V agent upgrade, the default group of settings location templates for common Microsoft applications and Windows settings may be updated.</span></span> <span data-ttu-id="2cbb8-188">Updates für UE-V-Agents können mithilfe von ESD-Infrastruktur (Enterprise Software Distribution) bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="2cbb8-188">UE-V agent updates can be deployed by using Enterprise Software Distribution (ESD) infrastructure.</span></span>

## <span data-ttu-id="2cbb8-189">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="2cbb8-189">Related topics</span></span>


[<span data-ttu-id="2cbb8-190">Bereitstellen von UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="2cbb8-190">Deploying UE-V 1.0</span></span>](deploying-ue-v-10.md)

[<span data-ttu-id="2cbb8-191">Unterstützte Konfigurationen für UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="2cbb8-191">Supported Configurations for UE-V 1.0</span></span>](supported-configurations-for-ue-v-10.md)

[<span data-ttu-id="2cbb8-192">Bereitstellen des Speicherorts für die Einstellungen für UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="2cbb8-192">Deploying the Settings Storage Location for UE-V 1.0</span></span>](deploying-the-settings-storage-location-for-ue-v-10.md)

[<span data-ttu-id="2cbb8-193">Installieren von UE-V-Generator</span><span class="sxs-lookup"><span data-stu-id="2cbb8-193">Installing the UE-V Generator</span></span>](installing-the-ue-v-generator.md)

<span data-ttu-id="2cbb8-194">Bereitstellen des Benutzeroberflächen-Virtualisierungs-Agents</span><span class="sxs-lookup"><span data-stu-id="2cbb8-194">Deploy the User Experience Virtualization Agent</span></span>
 

 





