---
title: Verwalten von UE-V 1.0-Speicherortvorlagen mithilfe von PowerShell und WMI
description: Verwalten von UE-V 1.0-Speicherortvorlagen mithilfe von PowerShell und WMI
author: dansimp
ms.assetid: 4b911c78-a5e9-4199-bfeb-72ab764d47c1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d8dab0997cdfaf7c96862fcce4bc012c3edfe0c0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804268"
---
# <span data-ttu-id="c75fb-103">Verwalten von UE-V 1.0-Speicherortvorlagen mithilfe von PowerShell und WMI</span><span class="sxs-lookup"><span data-stu-id="c75fb-103">Managing UE-V 1.0 Settings Location Templates Using PowerShell and WMI</span></span>


<span data-ttu-id="c75fb-104">Microsoft User Experience Virtualization (UE-V) verwendet Einstellungen-Standort Vorlagen (XML-Dateien), die die Einstellungen definieren, die von der Benutzeroberflächen-Virtualisierung erfasst und angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="c75fb-104">Microsoft User Experience Virtualization (UE-V) uses settings location templates (XML files) that define the settings captured and applied by User Experience Virtualization.</span></span> <span data-ttu-id="c75fb-105">UE-V enthält eine Reihe von Standardeinstellungen für Standort Vorlagen.</span><span class="sxs-lookup"><span data-stu-id="c75fb-105">UE-V includes a set of standard settings location templates.</span></span> <span data-ttu-id="c75fb-106">Es enthält auch das UE-V-Generator Tool, mit dem Sie benutzerdefinierte Speicherort Vorlagen für Einstellungen erstellen können.</span><span class="sxs-lookup"><span data-stu-id="c75fb-106">It also includes the UE-V Generator tool that enables you to create custom settings location templates.</span></span> <span data-ttu-id="c75fb-107">Nach dem Erstellen und Bereitstellen von Einstellungen für Speicherort Vorlagen können Sie diese Vorlagen mithilfe von PowerShell oder WMI verwalten.</span><span class="sxs-lookup"><span data-stu-id="c75fb-107">After you create and deploy settings location templates you can manage those templates using PowerShell or WMI.</span></span>

## <span data-ttu-id="c75fb-108">Verwalten von Speicherort Vorlagen für Einstellungen mit WMI und PowerShell</span><span class="sxs-lookup"><span data-stu-id="c75fb-108">Manage settings location templates with WMI and PowerShell</span></span>


<span data-ttu-id="c75fb-109">Zu den WMI-und PowerShell-Features von UE-V gehören die Möglichkeit zum Aktivieren, deaktivieren, registrieren, aktualisieren und Aufheben der Registrierung von Einstellungen für Standort Vorlagen.</span><span class="sxs-lookup"><span data-stu-id="c75fb-109">The WMI and PowerShell features of UE-V include the ability to enable, disable, register, update, and unregister settings location templates.</span></span> <span data-ttu-id="c75fb-110">Mithilfe dieser Features können Sie den Prozess der Registrierung, Aktualisierung oder Aufheben der Registrierung von Vorlagen mit dem UE-V-Agent automatisieren.</span><span class="sxs-lookup"><span data-stu-id="c75fb-110">By using these features, you can automate the process of registering, updating, or unregistering templates with the UE-V agent.</span></span> <span data-ttu-id="c75fb-111">Sie können Vorlagen auch manuell mithilfe von WMI-und PowerShell-Befehlen registrieren.</span><span class="sxs-lookup"><span data-stu-id="c75fb-111">You can also manually register templates using WMI and PowerShell commands.</span></span> <span data-ttu-id="c75fb-112">Wenn Sie diese Features in Verbindung mit einer Lösung für die elektronische Softwareverteilung, einer Gruppenrichtlinie oder einer anderen automatisierten Bereitstellungsmethode wie einem Skript verwenden, können Sie diesen Prozess weiter automatisieren.</span><span class="sxs-lookup"><span data-stu-id="c75fb-112">By using these features in conjunction with an electronic software distribution solution, Group Policy, or another automated deployment method such as a script, you can further automate that process.</span></span>

<span data-ttu-id="c75fb-113">Sie müssen über Administratorberechtigungen verfügen, um eine Einstellungs Speicherort Vorlage zu aktualisieren, zu registrieren oder die Registrierung aufzuheben.</span><span class="sxs-lookup"><span data-stu-id="c75fb-113">You must have administrator permissions to update, register, or unregister a settings location template.</span></span> <span data-ttu-id="c75fb-114">Zum Aktivieren oder Deaktivieren von Vorlagen sind keine Administrator Berechtigungen erforderlich.</span><span class="sxs-lookup"><span data-stu-id="c75fb-114">Administrator permissions are not required to enable or disable templates.</span></span>

**<span data-ttu-id="c75fb-115">So verwalten Sie Einstellungen für Standort Vorlagen mit PowerShell</span><span class="sxs-lookup"><span data-stu-id="c75fb-115">To manage settings location templates with PowerShell</span></span>**

1.  <span data-ttu-id="c75fb-116">Verwenden Sie ein Konto mit Administratorrechten, um ein Windows PowerShell-Fenster zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="c75fb-116">Use an account with administrator rights to open a Windows PowerShell window.</span></span> <span data-ttu-id="c75fb-117">Zum Importieren des **Microsoft UE-V PowerShell-** Moduls geben Sie an der PowerShell-Eingabeaufforderung den folgenden Befehl ein.</span><span class="sxs-lookup"><span data-stu-id="c75fb-117">To import the **Microsoft UE-V PowerShell** module, type the following command at the PowerShell command prompt.</span></span>

    ``` syntax
    Import-module UEV
    ```

2.  <span data-ttu-id="c75fb-118">Verwenden Sie die folgenden PowerShell-Cmdlets zum Registrieren und Verwalten der Standort Vorlagen für UE-V-Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="c75fb-118">Use the following PowerShell cmdlets to register and manage the UE-V settings location templates.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong><span data-ttu-id="c75fb-119">PowerShell-Befehl</span><span class="sxs-lookup"><span data-stu-id="c75fb-119">PowerShell command</span></span></strong></th>
    <th align="left"><strong><span data-ttu-id="c75fb-120">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c75fb-120">Description</span></span></strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="c75fb-121">Get-UevTemplate</span><span class="sxs-lookup"><span data-stu-id="c75fb-121">Get-UevTemplate</span></span></p></td>
    <td align="left"><p><span data-ttu-id="c75fb-122">Listet alle auf dem Computer registrierten Einstellungen für Standort Vorlagen auf.</span><span class="sxs-lookup"><span data-stu-id="c75fb-122">Lists all the settings location templates registered on the computer.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="c75fb-123">Registrieren-UevTemplate</span><span class="sxs-lookup"><span data-stu-id="c75fb-123">Register-UevTemplate</span></span></p></td>
    <td align="left"><p><span data-ttu-id="c75fb-124">Registriert eine Speicherort Vorlage für Einstellungen mit UE-V.</span><span class="sxs-lookup"><span data-stu-id="c75fb-124">Registers a settings location template with UE-V.</span></span> <span data-ttu-id="c75fb-125">Nachdem eine Vorlage registriert wurde, synchronisiert UE-V die in der Vorlage definierten Einstellungen zwischen Computern, auf denen die Vorlage registriert ist.</span><span class="sxs-lookup"><span data-stu-id="c75fb-125">Once a template is registered, UE-V will synchronize the settings that are defined in the template between computers that have the template registered.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="c75fb-126">Registrierung aufheben-UevTemplate</span><span class="sxs-lookup"><span data-stu-id="c75fb-126">Unregister-UevTemplate</span></span></p></td>
    <td align="left"><p><span data-ttu-id="c75fb-127">Hebt die Registrierung einer Einstellungs Speicherort Vorlage mit UE-V auf.</span><span class="sxs-lookup"><span data-stu-id="c75fb-127">Unregisters a settings location template with UE-V.</span></span> <span data-ttu-id="c75fb-128">Sobald eine Vorlage aufgehoben wurde, synchronisiert UE-V nicht mehr die Einstellungen, die in der Vorlage zwischen Computern definiert sind.</span><span class="sxs-lookup"><span data-stu-id="c75fb-128">As soon as a template is unregistered, UE-V will no longer synchronize the settings that are defined in the template between computers.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="c75fb-129">Update-UevTemplate</span><span class="sxs-lookup"><span data-stu-id="c75fb-129">Update-UevTemplate</span></span></p></td>
    <td align="left"><p><span data-ttu-id="c75fb-130">Aktualisiert eine Vorlage für Einstellungs Speicherort mit einer neueren Version der Vorlage.</span><span class="sxs-lookup"><span data-stu-id="c75fb-130">Updates a settings location template with a more recent version of the template.</span></span> <span data-ttu-id="c75fb-131">Die neue Vorlage sollte eine neuere Version als die vorhandene aufweisen.</span><span class="sxs-lookup"><span data-stu-id="c75fb-131">The new template should have a version that is later than the existing one.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="c75fb-132">Deaktivieren-UevTemplate</span><span class="sxs-lookup"><span data-stu-id="c75fb-132">Disable-UevTemplate</span></span></p></td>
    <td align="left"><p><span data-ttu-id="c75fb-133">Deaktiviert eine Vorlage für den Einstellungs Speicherort für den aktuellen Benutzer des Computers.</span><span class="sxs-lookup"><span data-stu-id="c75fb-133">Disables a settings location template for the current user of the computer.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="c75fb-134">Enable-UevTemplate</span><span class="sxs-lookup"><span data-stu-id="c75fb-134">Enable-UevTemplate</span></span></p></td>
    <td align="left"><p><span data-ttu-id="c75fb-135">Aktiviert eine Vorlage für Einstellungs Speicherort für den aktuellen Benutzer des Computers.</span><span class="sxs-lookup"><span data-stu-id="c75fb-135">Enables a settings location template for the current user of the computer.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="c75fb-136">Test-UevTemplate</span><span class="sxs-lookup"><span data-stu-id="c75fb-136">Test-UevTemplate</span></span></p></td>
    <td align="left"><p><span data-ttu-id="c75fb-137">Bestimmt, ob eine angegebene Speicherort Vorlage für Einstellungen dem XML-Schema entspricht.</span><span class="sxs-lookup"><span data-stu-id="c75fb-137">Determines whether a given settings location template complies with its XML schema.</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

<span data-ttu-id="c75fb-138">Mit den UE-V PowerShell-Features können Sie eine Gruppe von Einstellungs Vorlagen verwalten, die in Ihrem Unternehmen bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="c75fb-138">The UE-V PowerShell features allow you to manage a group of settings templates deployed in your enterprise.</span></span> <span data-ttu-id="c75fb-139">Gehen Sie wie folgt vor, um eine Gruppe von Vorlagen mithilfe von PowerShell zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="c75fb-139">To manage a group of templates using PowerShell, do the following.</span></span>

**<span data-ttu-id="c75fb-140">So verwalten Sie eine Gruppe von Einstellungen-Speicherort Vorlagen mit PowerShell</span><span class="sxs-lookup"><span data-stu-id="c75fb-140">To manage a group of settings location templates with PowerShell</span></span>**

1.  <span data-ttu-id="c75fb-141">Ändern oder aktualisieren Sie die Speicherort Vorlagen für die gewünschten Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="c75fb-141">Modify or update the desired settings location templates.</span></span>

2.  <span data-ttu-id="c75fb-142">Stellen Sie die Speicherort Vorlagen für die gewünschten Einstellungen in einem Ordner bereit, auf den der lokale Computer zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="c75fb-142">Deploy the desired settings location templates to a folder accessible to the local computer.</span></span>

3.  <span data-ttu-id="c75fb-143">Öffnen Sie auf dem lokalen Computer ein Windows PowerShell-Fenster mit Administratorrechten.</span><span class="sxs-lookup"><span data-stu-id="c75fb-143">On the local computer, open a Windows PowerShell window with administrator rights.</span></span>

4.  <span data-ttu-id="c75fb-144">Importieren Sie das Microsoft UE-V PowerShell-Modul, indem Sie den folgenden Befehl eingeben.</span><span class="sxs-lookup"><span data-stu-id="c75fb-144">Import the Microsoft UE-V PowerShell module, by typing the following command.</span></span>

    ``` syntax
    Import-module UEV
    ```

5.  <span data-ttu-id="c75fb-145">Heben Sie die Registrierung aller zuvor registrierten Versionen der Vorlagen auf, indem Sie den folgenden Befehl eingeben.</span><span class="sxs-lookup"><span data-stu-id="c75fb-145">Unregister all the previously registered versions of the templates by typing the following command.</span></span>

    ``` syntax
    Get-UevTemplate | Unregister-UevTemplate
    ```

    <span data-ttu-id="c75fb-146">Dadurch werden alle aktiven Vorlagen auf dem Computer aufgehoben.</span><span class="sxs-lookup"><span data-stu-id="c75fb-146">This will unregister all active templates on the computer.</span></span>

6.  <span data-ttu-id="c75fb-147">Registrieren Sie die aktualisierten Vorlagen, indem Sie den folgenden Befehl eingeben.</span><span class="sxs-lookup"><span data-stu-id="c75fb-147">Register the updated templates by typing the following command.</span></span>

    ``` syntax
    Register-UevTemplate <path to template folder>\*.xml
    ```

    <span data-ttu-id="c75fb-148">Damit werden alle Einstellungen für den Speicherort registriert, die sich im angegebenen Vorlagenordner befinden.</span><span class="sxs-lookup"><span data-stu-id="c75fb-148">This will register all of the settings location templates located in the specified template folder.</span></span>

<span data-ttu-id="c75fb-149">Die Virtualisierung der Benutzeroberfläche bietet die folgenden WMI-Befehle.</span><span class="sxs-lookup"><span data-stu-id="c75fb-149">User Experience Virtualization provides the following set of WMI commands.</span></span> <span data-ttu-id="c75fb-150">Administratoren können diese Schnittstellen zum Verwalten von Einstellungen für Standort Vorlagen aus Windows PowerShell und zum Automatisieren von administrativen Vorlagen Aufgaben verwenden.</span><span class="sxs-lookup"><span data-stu-id="c75fb-150">Administrators can use these interfaces to manage settings location templates from Windows PowerShell and automate template administrative tasks.</span></span>

**<span data-ttu-id="c75fb-151">So verwalten Sie Einstellungen für Standort Vorlagen mit WMI</span><span class="sxs-lookup"><span data-stu-id="c75fb-151">To manage settings location templates with WMI</span></span>**

1.  <span data-ttu-id="c75fb-152">Verwenden Sie ein Konto mit Administratorrechten, um ein Windows PowerShell-Fenster zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="c75fb-152">Use an account with administrator rights to open a Windows PowerShell window.</span></span>

2.  <span data-ttu-id="c75fb-153">Verwenden Sie die folgenden WMI-Befehle zum Registrieren und Verwalten der Standort Vorlagen für UE-V-Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="c75fb-153">Use the following WMI commands to register and manage the UE-V settings location templates.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p><strong><span data-ttu-id="c75fb-154">PowerShell-Befehl</span><span class="sxs-lookup"><span data-stu-id="c75fb-154">PowerShell command</span></span></strong></p></td>
    <td align="left"><p><strong><span data-ttu-id="c75fb-155">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c75fb-155">Description</span></span></strong></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="c75fb-156">Get-WMIObject-Namespace root\Microsoft\UEV SettingsLocationTemplate | SELECT-Objekt-Vorlagen-Nr, Vorlagenname, TemplateVersion, aktiviert | Format – Tabelle – AutoSize</span><span class="sxs-lookup"><span data-stu-id="c75fb-156">Get-WmiObject -Namespace root\Microsoft\UEV SettingsLocationTemplate | Select-Object TemplateId,TemplateName, TemplateVersion,Enabled | Format-Table -Autosize</span></span></p></td>
    <td align="left"><p><span data-ttu-id="c75fb-157">Listet alle Einstellungen für den Speicherort auf, die für den Computer registriert sind.</span><span class="sxs-lookup"><span data-stu-id="c75fb-157">Lists all the settings location templates registered for the computer.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="c75fb-158">Invoke-WmiMethod-Namespace root\Microsoft\UEV-Class SettingsLocationTemplate-Name Register-Argumentlisten- &lt; Vorlagenpfad&gt;</span><span class="sxs-lookup"><span data-stu-id="c75fb-158">Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name Register -ArgumentList &lt;template path &gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="c75fb-159">Registriert eine Speicherort Vorlage für Einstellungen mit UE-V.</span><span class="sxs-lookup"><span data-stu-id="c75fb-159">Registers a settings location template with UE-V.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="c75fb-160">Invoke-WmiMethod-Namespace root\Microsoft\UEV-Class SettingsLocationTemplate-Name UnregisterByTemplateId-argumentlist- &lt; Vorlagen-ID&gt;</span><span class="sxs-lookup"><span data-stu-id="c75fb-160">Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name UnregisterByTemplateId -ArgumentList &lt;template ID&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="c75fb-161">Hebt die Registrierung einer Einstellungs Speicherort Vorlage mit UE-V auf.</span><span class="sxs-lookup"><span data-stu-id="c75fb-161">Unregisters a settings location template with UE-V.</span></span> <span data-ttu-id="c75fb-162">Sobald eine Vorlage aufgehoben wurde, synchronisiert UE-V nicht mehr die Einstellungen, die in der Vorlage zwischen Computern definiert sind.</span><span class="sxs-lookup"><span data-stu-id="c75fb-162">As soon as a template is unregistered, UE-V will no longer synchronize the settings that are defined in the template between computers.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="c75fb-163">Invoke-WmiMethod-Namespace root\Microsoft\UEV-Class SettingsLocationTemplate-Name EnableByTemplateId-argumentlist- &lt; Vorlagen-ID&gt;</span><span class="sxs-lookup"><span data-stu-id="c75fb-163">Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name EnableByTemplateId -ArgumentList &lt;template ID&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="c75fb-164">Aktiviert eine Vorlage für eine Einstellungsposition mit UE-V</span><span class="sxs-lookup"><span data-stu-id="c75fb-164">Enables a settings location template with UE-V</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="c75fb-165">Invoke-WmiMethod-Namespace root\Microsoft\UEV-Class SettingsLocationTemplate-Name DisableByTemplateId-argumentlist- &lt; Vorlagen-ID&gt;</span><span class="sxs-lookup"><span data-stu-id="c75fb-165">Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name DisableByTemplateId -ArgumentList &lt;template ID&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="c75fb-166">Deaktiviert eine Speicherort Vorlage für Einstellungen mit UE-V</span><span class="sxs-lookup"><span data-stu-id="c75fb-166">Disables a settings location template with UE-V</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="c75fb-167">Invoke-WmiMethod-Namespace root\Microsoft\UEV-Class SettingsLocationTemplate-Name Update – argumentlist- &lt; Vorlagenpfad&gt;</span><span class="sxs-lookup"><span data-stu-id="c75fb-167">Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name Update -ArgumentList &lt;template path&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="c75fb-168">Aktualisiert eine Vorlage für Einstellungs Speicherort mit UE-V.</span><span class="sxs-lookup"><span data-stu-id="c75fb-168">Updates a settings location template with UE-V.</span></span> <span data-ttu-id="c75fb-169">Die neue Vorlage sollte eine höhere Version als die vorhandene aufweisen.</span><span class="sxs-lookup"><span data-stu-id="c75fb-169">The new template should have a version that is higher than the existing one.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="c75fb-170">Invoke-WmiMethod-Namespace root\Microsoft\UEV-Class SettingsLocationTemplate-Name Validate-argumentlist- &lt; Vorlagenpfad&gt;</span><span class="sxs-lookup"><span data-stu-id="c75fb-170">Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name Validate -ArgumentList &lt;template path&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="c75fb-171">Bestimmt, ob eine angegebene Speicherort Vorlage für Einstellungen dem XML-Schema entspricht.</span><span class="sxs-lookup"><span data-stu-id="c75fb-171">Determines whether a given settings location template complies with its XML schema.</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

**<span data-ttu-id="c75fb-172">Bereitstellen des UE-V-Agents mit PowerShell</span><span class="sxs-lookup"><span data-stu-id="c75fb-172">How to deploy the UE-V agent with PowerShell</span></span>**

1.  <span data-ttu-id="c75fb-173">Stufen Sie die UE-V-Installationsdatei in einer barrierefreien Netzwerkfreigabe ein.</span><span class="sxs-lookup"><span data-stu-id="c75fb-173">Stage the UE-V installer file in an accessible network share.</span></span>

    <span data-ttu-id="c75fb-174">**Hinweis**  Verwenden Sie AgentSetup.exe, um sowohl 32-Bit-als auch 64-Bit-Versionen des UE-V-Agents bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="c75fb-174">**Note** Use AgentSetup.exe to deploy both 32-bit and 64-bit versions of the UE-V Agent.</span></span> <span data-ttu-id="c75fb-175">Windows Installer-Dateien, AgentSetupx86.msi und AgentSetupx64.msi, stehen für jede Architektur zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="c75fb-175">Windows Installer Files versions, AgentSetupx86.msi and AgentSetupx64.msi, are available for each architecture.</span></span> <span data-ttu-id="c75fb-176">Wenn Sie den UE-V-Agent zu einem späteren Zeitpunkt mit der Installationsdatei deinstallieren möchten, müssen Sie denselben Dateityp verwenden.</span><span class="sxs-lookup"><span data-stu-id="c75fb-176">To uninstall the UE-V Agent at a later time using the installation file, you must use the same file type.</span></span>

     

2.  <span data-ttu-id="c75fb-177">Verwenden Sie einen der folgenden PowerShell-Befehle, um den Agenten zu installieren.</span><span class="sxs-lookup"><span data-stu-id="c75fb-177">Use one of the following PowerShell commands to install the agent.</span></span>

    `& AgentSetup.exe /quiet /norestart /log "%temp%\UE-VAgentInstaller.log" SettingsStoragePath=\\server\settingsshare\%username%`

    `& msiexec.exe /i "<path to msi file>" /quiet /norestart /l*v "%temp%\UE-VAgentInstaller.log" SettingsStoragePath=\\server\settingsshare\%username%`

## <span data-ttu-id="c75fb-178">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="c75fb-178">Related topics</span></span>


[<span data-ttu-id="c75fb-179">Verwalten des UE-V 1.0-Agents und von Paketen mit PowerShell und WMI</span><span class="sxs-lookup"><span data-stu-id="c75fb-179">Managing the UE-V 1.0 Agent and Packages with PowerShell and WMI</span></span>](managing-the-ue-v-10-agent-and-packages-with-powershell-and-wmi.md)

[<span data-ttu-id="c75fb-180">Verwalten von UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="c75fb-180">Administering UE-V 1.0</span></span>](administering-ue-v-10.md)

[<span data-ttu-id="c75fb-181">Vorgänge für UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="c75fb-181">Operations for UE-V 1.0</span></span>](operations-for-ue-v-10.md)

 

 





