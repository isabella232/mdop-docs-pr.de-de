---
title: Verwalten von Standort Vorlagen für die UE-V 2. x-Einstellungen mithilfe von Windows PowerShell und WMI
description: Verwalten von Standort Vorlagen für die UE-V 2. x-Einstellungen mithilfe von Windows PowerShell und WMI
author: dansimp
ms.assetid: b5253050-acc3-4274-90d0-1fa4c480331d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 9788ff1a11f1c70e52b75dd2187a198f5472f77f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804559"
---
# <span data-ttu-id="17233-103">Verwalten von Standort Vorlagen für die UE-V 2. x-Einstellungen mithilfe von Windows PowerShell und WMI</span><span class="sxs-lookup"><span data-stu-id="17233-103">Managing UE-V 2.x Settings Location Templates Using Windows PowerShell and WMI</span></span>


<span data-ttu-id="17233-104">Microsoft User Experience Virtualization (UE-V) 2,0, 2,1 und 2,1 SP1 verwenden Sie Vorlagen für XML-Einstellungen, um die Einstellungen zu definieren, die von der Benutzer Experience Virtualization erfasst und angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="17233-104">Microsoft User Experience Virtualization (UE-V) 2.0, 2.1, and 2.1 SP1 use XML settings location templates to define the settings that User Experience Virtualization captures and applies.</span></span> <span data-ttu-id="17233-105">UE-V enthält eine Reihe von Standardeinstellungen für Standort Vorlagen.</span><span class="sxs-lookup"><span data-stu-id="17233-105">UE-V includes a set of standard settings location templates.</span></span> <span data-ttu-id="17233-106">Es enthält auch das UE-V-Generator Tool, mit dem Sie benutzerdefinierte Speicherort Vorlagen für Einstellungen erstellen können.</span><span class="sxs-lookup"><span data-stu-id="17233-106">It also includes the UE-V Generator tool that enables you to create custom settings location templates.</span></span> <span data-ttu-id="17233-107">Nachdem Sie die Vorlagen für Speicherort für Einstellungen erstellt und bereitgestellt haben, können Sie diese Vorlagen mithilfe von Windows PowerShell und der Windows-Verwaltungsinstrumentation (WMI) verwalten.</span><span class="sxs-lookup"><span data-stu-id="17233-107">After you create and deploy settings location templates, you can manage those templates by using Windows PowerShell and the Windows Management Instrumentation (WMI).</span></span> <span data-ttu-id="17233-108">Eine vollständige Liste der UE-v PowerShell-Cmdlets finden Sie unter [UE-v 2-Cmdlet-Referenz](https://go.microsoft.com/fwlink/p/?LinkId=393495) ( https://go.microsoft.com/fwlink/p/?LinkId=393495) .</span><span class="sxs-lookup"><span data-stu-id="17233-108">For a complete list of UE-V PowerShell cmdlets, see [UE-V 2 Cmdlet Reference](https://go.microsoft.com/fwlink/p/?LinkId=393495) (https://go.microsoft.com/fwlink/p/?LinkId=393495).</span></span>

## <span data-ttu-id="17233-109">Verwalten von Standort Vorlagen für die UE-V 2-Einstellungen mithilfe von Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="17233-109">Manage UE-V 2 settings location templates by using Windows PowerShell</span></span>


<span data-ttu-id="17233-110">Die WMI-und Windows PowerShell-Features von UE-V umfassen die Möglichkeit, Einstellungen für Standort Vorlagen zu aktivieren, zu deaktivieren, zu registrieren, zu aktualisieren und die Registrierung aufzuheben.</span><span class="sxs-lookup"><span data-stu-id="17233-110">The WMI and Windows PowerShell features of UE-V include the ability to enable, disable, register, update, and unregister settings location templates.</span></span> <span data-ttu-id="17233-111">Mithilfe dieser Features können Sie den Prozess der Registrierung, Aktualisierung oder Aufheben der Registrierung von Vorlagen mit dem UE-V-Agent automatisieren.</span><span class="sxs-lookup"><span data-stu-id="17233-111">By using these features, you can automate the process of registering, updating, or unregistering templates with the UE-V Agent.</span></span> <span data-ttu-id="17233-112">Sie können Vorlagen auch manuell mithilfe von WMI-und Windows PowerShell-Befehlen registrieren.</span><span class="sxs-lookup"><span data-stu-id="17233-112">You can also manually register templates by using WMI and Windows PowerShell commands.</span></span> <span data-ttu-id="17233-113">Wenn Sie diese Features in Verbindung mit einer Lösung für die elektronische Softwareverteilung, einer Gruppenrichtlinie oder einer anderen automatisierten Bereitstellungsmethode wie einem Skript verwenden, können Sie diesen Prozess weiter automatisieren.</span><span class="sxs-lookup"><span data-stu-id="17233-113">By using these features in conjunction with an electronic software distribution solution, Group Policy, or another automated deployment method such as a script, you can further automate that process.</span></span>

<span data-ttu-id="17233-114">Sie müssen über Administratorberechtigungen verfügen, um eine Einstellungs Speicherort Vorlage zu aktualisieren, zu registrieren oder die Registrierung aufzuheben.</span><span class="sxs-lookup"><span data-stu-id="17233-114">You must have administrator permissions to update, register, or unregister a settings location template.</span></span> <span data-ttu-id="17233-115">Zum Aktivieren, deaktivieren oder Auflisten von Vorlagen sind keine Administrator Berechtigungen erforderlich.</span><span class="sxs-lookup"><span data-stu-id="17233-115">Administrator permissions are not required to enable, disable, or list templates.</span></span>

***<em><span data-ttu-id="17233-116">So verwalten Sie Einstellungen für Standort Vorlagen mithilfe von Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="17233-116">To manage settings location templates by using Windows PowerShell</span></span>ell</em>***

1.  <span data-ttu-id="17233-117">Verwenden Sie ein Konto mit Administratorrechten, um eine Windows PowerShell-Eingabeaufforderung zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="17233-117">Use an account with administrator rights to open a Windows PowerShell command prompt.</span></span>

2.  <span data-ttu-id="17233-118">Verwenden Sie die folgenden Windows PowerShell-Cmdlets zum Registrieren und Verwalten der Standort Vorlagen für UE-V-Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="17233-118">Use the following Windows PowerShell cmdlets to register and manage the UE-V settings location templates.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="17233-119">Windows PowerShell-Befehl</span><span class="sxs-lookup"><span data-stu-id="17233-119">Windows PowerShell command</span></span></th>
    <th align="left"><span data-ttu-id="17233-120">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="17233-120">Description</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><code>Get-UevTemplate</code></p></td>
    <td align="left"><p><span data-ttu-id="17233-121">Listet alle Einstellungen-Speicherort Vorlagen auf, die auf dem Computer registriert sind.</span><span class="sxs-lookup"><span data-stu-id="17233-121">Lists all the settings location templates that are registered on the computer.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Get-UevTemplate –Application &lt;string&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="17233-122">Listet alle Einstellungen-Speicherort Vorlagen auf, die auf dem Computer registriert sind, auf dem der Anwendungsname oder der Vorlagenname eine &lt; Zeichenfolge enthält &gt; .</span><span class="sxs-lookup"><span data-stu-id="17233-122">Lists all the settings location templates that are registered on the computer where the application name or template name contains &lt;string&gt;.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Get-UevTemplate –TemplateID &lt;string&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="17233-123">Listet alle Einstellungen-Standort Vorlagen auf, die auf dem Computer registriert sind, auf dem die Vorlagen-ID eine &lt; Zeichenfolge enthält &gt; .</span><span class="sxs-lookup"><span data-stu-id="17233-123">Lists all the settings location templates that are registered on the computer where the template ID contains &lt;string&gt;.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Get-UevTemplate [-ApplicationOrTemplateID] &lt;string&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="17233-124">Listet alle Einstellungen-Speicherort Vorlagen auf, die auf dem Computer registriert sind, auf dem der Anwendungs-oder Vorlagenname oder die Vorlagen-ID eine &lt; Zeichenfolge enthält &gt; .</span><span class="sxs-lookup"><span data-stu-id="17233-124">Lists all the settings location templates that are registered on the computer where the application or template name, or template ID contains &lt;string&gt;.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Get-UevTemplateProgram [-ID] &lt;template ID&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="17233-125">Ruft den Namen des Programms und der Versionsinformationen ab, die von der Vorlagen-ID abhängen.</span><span class="sxs-lookup"><span data-stu-id="17233-125">Gets the name of the program and version information, which depend on the template ID.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Get-UevAppXPackage</code></p></td>
    <td align="left"><p><span data-ttu-id="17233-126">Ruft die effektive Liste der Windows-apps ab.</span><span class="sxs-lookup"><span data-stu-id="17233-126">Gets the effective list of Windows apps.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Get-UevAppXPackage -Computer</code></p></td>
    <td align="left"><p><span data-ttu-id="17233-127">Ruft die Liste der Windows-apps ab, die für den Computer konfiguriert sind.</span><span class="sxs-lookup"><span data-stu-id="17233-127">Gets the list of Windows apps that are configured for the computer.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Get-UevAppXPackage -CurrentComputerUser</code></p></td>
    <td align="left"><p><span data-ttu-id="17233-128">Ruft die Liste der Windows-apps ab, die für den aktuellen Benutzer konfiguriert sind.</span><span class="sxs-lookup"><span data-stu-id="17233-128">Gets the list of Windows apps that are configured for the current user.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Register-UevTemplate [-Path] &lt;template file path&gt;[,&lt;template file path&gt;]</code></p></td>
    <td align="left"><p><span data-ttu-id="17233-129">Registriert eine oder mehrere Einstellungen Speicherort Vorlage mit UE-V, indem relative Pfade und/oder Platzhalterzeichen in Dateipfaden verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="17233-129">Registers one or more settings location template with UE-V by using relative paths and/or wildcard characters in file paths.</span></span> <span data-ttu-id="17233-130">Nachdem eine Vorlage registriert wurde, synchronisiert UE-V die in der Vorlage definierten Einstellungen zwischen Computern, auf denen die Vorlage registriert ist.</span><span class="sxs-lookup"><span data-stu-id="17233-130">After a template is registered, UE-V synchronizes the settings that are defined in the template between computers that have the template registered.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Register-UevTemplate –LiteralPath &lt;template file path&gt;[,&lt;template file path&gt;]</code></p></td>
    <td align="left"><p><span data-ttu-id="17233-131">Registriert eine oder mehrere Einstellungen Speicherort Vorlage mit UE-V mithilfe von literalen Pfaden, in denen keine Zeichen als Platzhalterzeichen interpretiert werden können.</span><span class="sxs-lookup"><span data-stu-id="17233-131">Registers one or more settings location template with UE-V by using literal paths, where no characters can be interpreted as wildcard characters.</span></span> <span data-ttu-id="17233-132">Nachdem eine Vorlage registriert wurde, synchronisiert UE-V die in der Vorlage definierten Einstellungen zwischen Computern, auf denen die Vorlage registriert ist.</span><span class="sxs-lookup"><span data-stu-id="17233-132">After a template is registered, UE-V synchronizes the settings that are defined in the template between computers that have the template registered.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Unregister-UevTemplate [-ID] &lt;template ID&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="17233-133">Hebt die Registrierung einer Einstellungs Speicherort Vorlage mit UE-V auf.</span><span class="sxs-lookup"><span data-stu-id="17233-133">Unregisters a settings location template with UE-V.</span></span> <span data-ttu-id="17233-134">Wenn eine Vorlage nicht registriert ist, synchronisiert UE-V nicht mehr die Einstellungen, die in der Vorlage zwischen Computern definiert sind.</span><span class="sxs-lookup"><span data-stu-id="17233-134">When a template is unregistered, UE-V no longer synchronizes the settings that are defined in the template between computers.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Unregister-UevTemplate -All</code></p></td>
    <td align="left"><p><span data-ttu-id="17233-135">Hebt die Registrierung aller Einstellungen-Standort Vorlagen mit UE-V auf.</span><span class="sxs-lookup"><span data-stu-id="17233-135">Unregisters all settings location templates with UE-V.</span></span> <span data-ttu-id="17233-136">Wenn eine Vorlage nicht registriert ist, synchronisiert UE-V nicht mehr die Einstellungen, die in der Vorlage zwischen Computern definiert sind.</span><span class="sxs-lookup"><span data-stu-id="17233-136">When a template is unregistered, UE-V no longer synchronizes the settings that are defined in the template between computers.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Update-UevTemplate [-Path] &lt;template file path&gt;[,&lt;template file path&gt;]</code></p></td>
    <td align="left"><p><span data-ttu-id="17233-137">Aktualisiert eine oder mehrere Einstellungen-Speicherort Vorlagen mit einer neueren Version der Vorlage.</span><span class="sxs-lookup"><span data-stu-id="17233-137">Updates one or more settings location templates with a more recent version of the template.</span></span> <span data-ttu-id="17233-138">Verwenden Sie relative Pfade und/oder Platzhalterzeichen in den Dateipfaden.</span><span class="sxs-lookup"><span data-stu-id="17233-138">Use relative paths and/or wildcard characters in the file paths.</span></span> <span data-ttu-id="17233-139">Die neue Vorlage sollte eine neuere Version als die vorhandene Vorlage sein.</span><span class="sxs-lookup"><span data-stu-id="17233-139">The new template should be a newer version than the existing template.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Update-UevTemplate –LiteralPath &lt;template file path&gt;[,&lt;template file path&gt;]</code></p></td>
    <td align="left"><p><span data-ttu-id="17233-140">Aktualisiert eine oder mehrere Einstellungen-Speicherort Vorlagen mit einer neueren Version der Vorlage.</span><span class="sxs-lookup"><span data-stu-id="17233-140">Updates one or more settings location templates with a more recent version of the template.</span></span> <span data-ttu-id="17233-141">Verwenden Sie vollständige Pfade für Vorlagendateien, bei denen keine Zeichen als Platzhalterzeichen interpretiert werden können.</span><span class="sxs-lookup"><span data-stu-id="17233-141">Use full paths to template files, where no characters can be interpreted as wildcard characters.</span></span> <span data-ttu-id="17233-142">Die neue Vorlage sollte eine neuere Version als die vorhandene Vorlage sein.</span><span class="sxs-lookup"><span data-stu-id="17233-142">The new template should be a newer version than the existing template.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Clear-UevAppXPackage –Computer [-PackageFamilyName] &lt;package family name&gt;[,&lt;package family name&gt;]</code></p></td>
    <td align="left"><p><span data-ttu-id="17233-143">Entfernt eine oder mehrere Windows-Apps aus der Windows-App-Liste der Computer.</span><span class="sxs-lookup"><span data-stu-id="17233-143">Removes one or more Windows apps from the computer Windows app list.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Clear-UevAppXPackage -CurrentComputerUser</code></p></td>
    <td align="left"><p><span data-ttu-id="17233-144">Entfernt die Windows-App aus der Windows-App-Liste der aktuellen Benutzer.</span><span class="sxs-lookup"><span data-stu-id="17233-144">Removes Windows app from the current user Windows app list.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Clear-UevAppXPackage –Computer -All</code></p></td>
    <td align="left"><p><span data-ttu-id="17233-145">Entfernt alle Windows-Apps aus der Windows-App-Liste der Computer.</span><span class="sxs-lookup"><span data-stu-id="17233-145">Removes all Windows apps from the computer Windows app list.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Clear-UevAppXPackage [–CurrentComputerUser] [-PackageFamilyName] &lt;package family name&gt;[,&lt;package family name&gt;]</code></p></td>
    <td align="left"><p><span data-ttu-id="17233-146">Entfernt eine oder mehrere Windows-Apps aus der Windows-App-Liste der aktuellen Benutzer.</span><span class="sxs-lookup"><span data-stu-id="17233-146">Removes one or more Windows apps from the current user Windows app list.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Clear-UevAppXPackage [–CurrentComputerUser] -All</code></p></td>
    <td align="left"><p><span data-ttu-id="17233-147">Entfernt alle Windows-Apps aus der Windows-App-Liste der aktuellen Benutzer.</span><span class="sxs-lookup"><span data-stu-id="17233-147">Removes all Windows apps from the current user Windows app list.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Disable-UevTemplate [-ID] &lt;template ID&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="17233-148">Deaktiviert eine Vorlage für den Einstellungs Speicherort für den aktuellen Benutzer des Computers.</span><span class="sxs-lookup"><span data-stu-id="17233-148">Disables a settings location template for the current user of the computer.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Disable-UevAppXPackage –Computer [-PackageFamilyName] &lt;package family name&gt;[,&lt;package family name&gt;]</code></p></td>
    <td align="left"><p><span data-ttu-id="17233-149">Deaktiviert eine oder mehrere Windows-apps in der Windows-App-Liste der Computer.</span><span class="sxs-lookup"><span data-stu-id="17233-149">Disables one or more Windows apps in the computer Windows app list.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Disable-UevAppXPackage [–CurrentComputerUser] [-PackageFamilyName] &lt;package family name&gt;[,&lt;package family name&gt;]</code></p></td>
    <td align="left"><p><span data-ttu-id="17233-150">Deaktiviert eine oder mehrere Windows-apps in der Windows-App-Liste der aktuellen Benutzer.</span><span class="sxs-lookup"><span data-stu-id="17233-150">Disables one or more Windows apps in the current user Windows app list.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Enable-UevTemplate [-ID] &lt;template ID&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="17233-151">Aktiviert eine Vorlage für Einstellungs Speicherort für den aktuellen Benutzer des Computers.</span><span class="sxs-lookup"><span data-stu-id="17233-151">Enables a settings location template for the current user of the computer.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Enable-UevAppXPackage –Computer [-PackageFamilyName] &lt;package family name&gt;[,&lt;package family name&gt;]</code></p></td>
    <td align="left"><p><span data-ttu-id="17233-152">Aktiviert mindestens eine Windows-app in der Liste der Computer-Windows-apps.</span><span class="sxs-lookup"><span data-stu-id="17233-152">Enables one or more Windows apps in the computer Windows app list.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Enable-UevAppXPackage [–CurrentComputerUser] [-PackageFamilyName] &lt;package family name&gt;[,&lt;package family name&gt;]</code></p></td>
    <td align="left"><p><span data-ttu-id="17233-153">Aktiviert eine oder mehrere Windows-apps in der Windows-App-Liste der aktuellen Benutzer.</span><span class="sxs-lookup"><span data-stu-id="17233-153">Enables one or more Windows apps in the current user Windows app list.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Test-UevTemplate [-Path] &lt;template file path&gt;[,&lt;template file path&gt;]</code></p></td>
    <td align="left"><p><span data-ttu-id="17233-154">Bestimmt, ob eine oder mehrere Einstellungen-Speicherort Vorlagen dem XML-Schema entsprechen.</span><span class="sxs-lookup"><span data-stu-id="17233-154">Determines whether one or more settings location templates comply with its XML schema.</span></span> <span data-ttu-id="17233-155">Relative Pfade und Platzhalterzeichen können verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="17233-155">Can use relative paths and wildcard characters.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Test-UevTemplate –LiteralPath &lt;template file path&gt;[,&lt;template file path&gt;]</code></p></td>
    <td align="left"><p><span data-ttu-id="17233-156">Bestimmt, ob eine oder mehrere Einstellungen-Speicherort Vorlagen dem XML-Schema entsprechen.</span><span class="sxs-lookup"><span data-stu-id="17233-156">Determines whether one or more settings location templates comply with its XML schema.</span></span> <span data-ttu-id="17233-157">Der Pfad muss ein vollständiger Pfad zur Vorlagendatei sein, enthält jedoch keine Platzhalterzeichen.</span><span class="sxs-lookup"><span data-stu-id="17233-157">The path must be a full path to the template file, but does not include wildcard characters.</span></span></p></td>
    </tr>
    </tbody>
    </table>



<span data-ttu-id="17233-158">Mit den UE-V Windows PowerShell-Features können Sie eine Gruppe von Einstellungs Vorlagen verwalten, die in Ihrem Unternehmen bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="17233-158">The UE-V Windows PowerShell features enable you to manage a group of settings templates that are deployed in your enterprise.</span></span> <span data-ttu-id="17233-159">Gehen Sie wie folgt vor, um eine Gruppe von Vorlagen mithilfe von Windows PowerShell zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="17233-159">Use the following procedure to manage a group of templates by using Windows PowerShell.</span></span>

**<span data-ttu-id="17233-160">So verwalten Sie eine Gruppe von Einstellungen für Standort Vorlagen mithilfe von Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="17233-160">To manage a group of settings location templates by using Windows PowerShell</span></span>**

1.  <span data-ttu-id="17233-161">Ändern oder aktualisieren Sie die Speicherort Vorlagen für die gewünschten Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="17233-161">Modify or update the desired settings location templates.</span></span>

2.  <span data-ttu-id="17233-162">Wenn Sie die Einstellungen-Speicherort Vorlagen ändern oder aktualisieren möchten, stellen Sie die Speicherort Vorlagen für Einstellungen in einem Ordner bereit, auf den der lokale Computer zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="17233-162">If you want to modify or update the settings location templates, deploy those settings location templates to a folder that is accessible to the local computer.</span></span>

3.  <span data-ttu-id="17233-163">Öffnen Sie auf dem lokalen Computer ein Windows PowerShell-Fenster mit Administratorrechten.</span><span class="sxs-lookup"><span data-stu-id="17233-163">On the local computer, open a Windows PowerShell window with administrator rights.</span></span>

4.  <span data-ttu-id="17233-164">Heben Sie die Registrierung aller zuvor registrierten Versionen der Vorlagen auf, indem Sie den folgenden Befehl eingeben.</span><span class="sxs-lookup"><span data-stu-id="17233-164">Unregister all the previously registered versions of the templates by typing the following command.</span></span>

    ``` syntax
    Unregister-UevTemplate -All
    ```

    <span data-ttu-id="17233-165">Mit diesem Befehl werden alle aktiven Vorlagen auf dem Computer aufgehoben.</span><span class="sxs-lookup"><span data-stu-id="17233-165">This command unregisters all active templates on the computer.</span></span>

5.  <span data-ttu-id="17233-166">Registrieren Sie die aktualisierten Vorlagen, indem Sie den folgenden Befehl eingeben.</span><span class="sxs-lookup"><span data-stu-id="17233-166">Register the updated templates by typing the following command.</span></span>

    ``` syntax
    Register-UevTemplate <path to template folder>\*.xml
    ```

    <span data-ttu-id="17233-167">Dieser Befehl registriert alle Einstellungen-Standort Vorlagen, die sich im angegebenen Vorlagenordner befinden.</span><span class="sxs-lookup"><span data-stu-id="17233-167">This command registers all of the settings location templates that are located in the specified template folder.</span></span>

### <a href="" id="win8applist"></a><span data-ttu-id="17233-168">Windows-App-Liste</span><span class="sxs-lookup"><span data-stu-id="17233-168">Windows app list</span></span>

<span data-ttu-id="17233-169">Durch Auflisten einer Windows-app in der Windows-App-Liste geben Sie an, ob die APP für die Synchronisierung von Einstellungen aktiviert oder deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="17233-169">By listing a Windows app in the Windows app list, you specify whether that app is enabled or disabled for settings synchronization.</span></span> <span data-ttu-id="17233-170">Apps werden in der Liste nach dem Namen der paketfamilie identifiziert und festgelegt, ob die Synchronisierung der Einstellungen für diese APP aktiviert oder deaktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="17233-170">Apps are identified in the list by their Package Family name and whether settings synchronization should be enabled or disabled for that app.</span></span> <span data-ttu-id="17233-171">Wenn Sie diese Einstellungen zusammen mit der Einstellung für das Standard Synchronisierungsverhalten nicht aufgelistet verwenden, können Sie steuern, ob Windows-apps synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="17233-171">When you use these settings along with the Unlisted Default Sync Behavior setting, you can control whether Windows apps are synchronized.</span></span>

<span data-ttu-id="17233-172">Wenn Sie den Namen der paketfamilie von installierten Windows-apps anzeigen möchten, geben Sie an einer Windows PowerShell-Eingabeaufforderung Folgendes ein:</span><span class="sxs-lookup"><span data-stu-id="17233-172">To display the Package Family Name of installed Windows apps, at a Windows PowerShell command prompt, enter:</span></span>

``` syntax
Get-AppxPackage | Sort-Object PackageFamilyName | Format-Table PackageFamilyName
```

<span data-ttu-id="17233-173">Um eine Liste der Windows-apps anzuzeigen, die die Einstellungen auf einem Computer mit dem Namen der paketfamilie, dem aktivierten Status und der aktivierten Quelle synchronisieren können, geben Sie an einer Windows PowerShell-Eingabeaufforderung Folgendes ein:</span><span class="sxs-lookup"><span data-stu-id="17233-173">To display a list of Windows apps that can synchronize settings on a computer with their package family name, enabled status, and enabled source, at a Windows PowerShell command prompt, enter:</span></span> `Get-UevAppxPackage`

**<span data-ttu-id="17233-174">Definitionen von Get-UevAppxPackage-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="17233-174">Definitions of Get-UevAppxPackage properties</span></span>**

<a href="" id="displayname"></a>**<span data-ttu-id="17233-175">DisplayName</span><span class="sxs-lookup"><span data-stu-id="17233-175">DisplayName</span></span>**  
<span data-ttu-id="17233-176">Der Name, der dem Benutzer in der Anwendung "Unternehmenseinstellungen Center" angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="17233-176">The name that is displayed to the user in the Company Settings Center application.</span></span> <span data-ttu-id="17233-177">Die `DisplayName` Eigenschaft wird von der `PackageFamilyName` Eigenschaft abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="17233-177">The `DisplayName` property is derived from the `PackageFamilyName` property.</span></span>

<a href="" id="packagefamilyname"></a>**<span data-ttu-id="17233-178">PackageFamilyName</span><span class="sxs-lookup"><span data-stu-id="17233-178">PackageFamilyName</span></span>**  
<span data-ttu-id="17233-179">Der Name des Pakets, das für den aktuellen Benutzer installiert ist.</span><span class="sxs-lookup"><span data-stu-id="17233-179">The name of the package that is installed for the current user.</span></span>

<a href="" id="enabled"></a>**<span data-ttu-id="17233-180">Aktiviert</span><span class="sxs-lookup"><span data-stu-id="17233-180">Enabled</span></span>**  
<span data-ttu-id="17233-181">Definiert, ob die Einstellungen für die APP für die Synchronisierung konfiguriert sind.</span><span class="sxs-lookup"><span data-stu-id="17233-181">Defines whether the settings for the app are configured to synchronize.</span></span>

<a href="" id="enabledsource"></a>**<span data-ttu-id="17233-182">EnabledSource</span><span class="sxs-lookup"><span data-stu-id="17233-182">EnabledSource</span></span>**  
<span data-ttu-id="17233-183">Der Speicherort, an dem die Konfiguration, die die App aktiviert oder deaktiviert, festgesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="17233-183">The location where the configuration that enables or disables the app is set.</span></span> <span data-ttu-id="17233-184">Mögliche Werte sind: *NotSet*, *LocalMachine*, *LocalUser*, *PolicyMachine*und *PolicyUser*.</span><span class="sxs-lookup"><span data-stu-id="17233-184">Possible values are: *NotSet*, *LocalMachine*, *LocalUser*, *PolicyMachine*, and *PolicyUser*.</span></span>

<a href="" id="notset"></a>**<span data-ttu-id="17233-185">NotSet</span><span class="sxs-lookup"><span data-stu-id="17233-185">NotSet</span></span>**  
<span data-ttu-id="17233-186">Die Richtlinie ist nicht für die Synchronisierung dieser APP konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="17233-186">The policy is not configured to synchronize this app.</span></span>

<a href="" id="localmachine"></a>**<span data-ttu-id="17233-187">LocalMachine</span><span class="sxs-lookup"><span data-stu-id="17233-187">LocalMachine</span></span>**  
<span data-ttu-id="17233-188">Der Status "aktiviert" wird im Abschnitt "lokaler Computer" der Registrierung festgesetzt.</span><span class="sxs-lookup"><span data-stu-id="17233-188">The enabled state is set in the local computer section of the registry.</span></span>

<a href="" id="localuser"></a>**<span data-ttu-id="17233-189">LocalUser</span><span class="sxs-lookup"><span data-stu-id="17233-189">LocalUser</span></span>**  
<span data-ttu-id="17233-190">Der Status "aktiviert" wird im Abschnitt "aktueller Benutzer" der Registrierung festgesetzt.</span><span class="sxs-lookup"><span data-stu-id="17233-190">The enabled state is set in the current user section of the registry.</span></span>

<a href="" id="policymachine"></a>**<span data-ttu-id="17233-191">PolicyMachine</span><span class="sxs-lookup"><span data-stu-id="17233-191">PolicyMachine</span></span>**  
<span data-ttu-id="17233-192">Der Status "aktiviert" wird im Abschnitt "Richtlinie" des Abschnitts "lokaler Computer" der Registrierung festgesetzt.</span><span class="sxs-lookup"><span data-stu-id="17233-192">The enabled state is set in the policy section of the local computer section of the registry.</span></span>

<span data-ttu-id="17233-193">Um die Benutzer konfigurierte Liste der Windows-apps abzurufen, geben Sie an der Windows PowerShell-Eingabeaufforderung Folgendes ein:</span><span class="sxs-lookup"><span data-stu-id="17233-193">To get the user-configured list of Windows apps, at the Windows PowerShell command prompt, enter:</span></span> `Get-UevAppxPackage –CurrentComputerUser`

<span data-ttu-id="17233-194">Um die Computer konfigurierte Liste der Windows-apps abzurufen, geben Sie an der Windows PowerShell-Eingabeaufforderung Folgendes ein:</span><span class="sxs-lookup"><span data-stu-id="17233-194">To get the computer-configured list of Windows apps, at the Windows PowerShell command prompt, enter:</span></span> `Get-UevAppxPackage –Computer`

<span data-ttu-id="17233-195">Für Parameter, CurrentComputerUser oder Computer gibt das Cmdlet eine Liste der Windows-apps zurück, die auf dem Benutzer oder auf Computerebene konfiguriert sind.</span><span class="sxs-lookup"><span data-stu-id="17233-195">For either parameter, CurrentComputerUser or Computer, the cmdlet returns a list of the Windows apps that are configured at the user or at the computer level.</span></span>

**<span data-ttu-id="17233-196">Definitionen von Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="17233-196">Definitions of properties</span></span>**

<a href="" id="displayname"></a>**<span data-ttu-id="17233-197">DisplayName</span><span class="sxs-lookup"><span data-stu-id="17233-197">DisplayName</span></span>**  
<span data-ttu-id="17233-198">Der Name, der dem Benutzer in der Anwendung "Unternehmenseinstellungen Center" angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="17233-198">The name that is displayed to the user in the Company Settings Center application.</span></span> <span data-ttu-id="17233-199">Die `DisplayName` Eigenschaft wird von der `PackageFamilyName` Eigenschaft abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="17233-199">The `DisplayName` property is derived from the `PackageFamilyName` property.</span></span>

<a href="" id="packagefamilyname"></a>**<span data-ttu-id="17233-200">PackageFamilyName</span><span class="sxs-lookup"><span data-stu-id="17233-200">PackageFamilyName</span></span>**  
<span data-ttu-id="17233-201">Der Name des Pakets, das für den aktuellen Benutzer installiert ist.</span><span class="sxs-lookup"><span data-stu-id="17233-201">The name of the package that is installed for the current user.</span></span>

<a href="" id="enabled"></a>**<span data-ttu-id="17233-202">Aktiviert</span><span class="sxs-lookup"><span data-stu-id="17233-202">Enabled</span></span>**  
<span data-ttu-id="17233-203">Definiert, ob die Einstellungen für die APP für die Synchronisierung für den angegebenen Schalter ( **Benutzer** oder **Computer**) konfiguriert sind.</span><span class="sxs-lookup"><span data-stu-id="17233-203">Defines whether the settings for the app are configured to synchronize for the specified switch, that is, **user** or **computer**.</span></span>

<a href="" id="installed"></a>**<span data-ttu-id="17233-204">Installiert</span><span class="sxs-lookup"><span data-stu-id="17233-204">Installed</span></span>**  
<span data-ttu-id="17233-205">"True", wenn die APP, also die PackageFamilyName, für den aktuellen Benutzer installiert ist.</span><span class="sxs-lookup"><span data-stu-id="17233-205">True if the app, that is, the PackageFamilyName is installed for the current user.</span></span>

### <span data-ttu-id="17233-206">Verwalten von Standort Vorlagen für die UE-V 2-Einstellungen mithilfe von WMI</span><span class="sxs-lookup"><span data-stu-id="17233-206">Manage UE-V 2 settings location templates by using WMI</span></span>

<span data-ttu-id="17233-207">Die Virtualisierung der Benutzeroberfläche bietet die folgenden WMI-Befehle.</span><span class="sxs-lookup"><span data-stu-id="17233-207">User Experience Virtualization provides the following set of WMI commands.</span></span> <span data-ttu-id="17233-208">Administratoren können diese Schnittstellen zum Verwalten von Einstellungen für Standort Vorlagen aus Windows PowerShell und zum Automatisieren von administrativen Vorlagen Aufgaben verwenden.</span><span class="sxs-lookup"><span data-stu-id="17233-208">Administrators can use these interfaces to manage settings location templates from Windows PowerShell and automate template administrative tasks.</span></span>

**<span data-ttu-id="17233-209">So verwalten Sie Einstellungen für Standort Vorlagen mithilfe von WMI</span><span class="sxs-lookup"><span data-stu-id="17233-209">To manage settings location templates by using WMI</span></span>**

1.  <span data-ttu-id="17233-210">Verwenden Sie ein Konto mit Administratorrechten, um ein Windows PowerShell-Fenster zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="17233-210">Use an account with administrator rights to open a Windows PowerShell window.</span></span>

2.  <span data-ttu-id="17233-211">Verwenden Sie die folgenden WMI-Befehle zum Registrieren und Verwalten der Standort Vorlagen für UE-V-Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="17233-211">Use the following WMI commands to register and manage the UE-V settings location templates.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><code>                         Windows PowerShell command</code></th>
    <th align="left"><span data-ttu-id="17233-212">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="17233-212">Description</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><code>Get-WmiObject -Namespace root\Microsoft\UEV SettingsLocationTemplate | Select-Object TemplateId,TemplateName, TemplateVersion,Enabled | Format-Table -Autosize</code></p></td>
    <td align="left"><p><span data-ttu-id="17233-213">Listet alle Einstellungen-Speicherort Vorlagen auf, die für den Computer registriert sind.</span><span class="sxs-lookup"><span data-stu-id="17233-213">Lists all the settings location templates that are registered for the computer.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Invoke-WmiMethod –Namespace root\Microsoft\UEV –Class SettingsLocationTemplate –Name GetProcessInfoByTemplateId &lt;template Id&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="17233-214">Ruft den Namen des Programms und die Versionsinformationen ab, die vom Vorlagennamen abhängen.</span><span class="sxs-lookup"><span data-stu-id="17233-214">Gets the name of the program and version information, which depends on the template name.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Get-WmiObject -Namespace root\Microsoft\UEV EffectiveWindows8App</code></p></td>
    <td align="left"><p><span data-ttu-id="17233-215">Ruft die effektive Liste der Windows-apps ab.</span><span class="sxs-lookup"><span data-stu-id="17233-215">Gets the effective list of Windows apps.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="17233-216">Get-WMIObject-Namespace root\Microsoft\UEV MachineConfiguredWindows8App</span><span class="sxs-lookup"><span data-stu-id="17233-216">Get-WmiObject -Namespace root\Microsoft\UEV MachineConfiguredWindows8App</span></span></p></td>
    <td align="left"><p><span data-ttu-id="17233-217">Ruft die Liste der Windows-apps ab, die für den Computer konfiguriert sind.</span><span class="sxs-lookup"><span data-stu-id="17233-217">Gets the list of Windows apps that are configured for the computer.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Get-WmiObject -Namespace root\Microsoft\UEV UserConfiguredWindows8App</code></p></td>
    <td align="left"><p><span data-ttu-id="17233-218">Ruft die Liste der Windows-apps ab, die für den aktuellen Benutzer konfiguriert sind.</span><span class="sxs-lookup"><span data-stu-id="17233-218">Gets the list of Windows apps that are configured for the current user.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name Register -ArgumentList &lt;template path &gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="17233-219">Registriert eine Speicherort Vorlage für Einstellungen mit UE-V.</span><span class="sxs-lookup"><span data-stu-id="17233-219">Registers a settings location template with UE-V.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name UnregisterByTemplateId -ArgumentList &lt;template ID&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="17233-220">Hebt die Registrierung einer Einstellungs Speicherort Vorlage mit UE-V auf.</span><span class="sxs-lookup"><span data-stu-id="17233-220">Unregisters a settings location template with UE-V.</span></span> <span data-ttu-id="17233-221">Sobald eine Vorlage aufgehoben wurde, synchronisiert UE-V nicht mehr die Einstellungen, die in der Vorlage zwischen Computern definiert sind.</span><span class="sxs-lookup"><span data-stu-id="17233-221">As soon as a template is unregistered, UE-V no longer synchronizes the settings that are defined in the template between computers.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name Update -ArgumentList &lt;template path&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="17233-222">Aktualisiert eine Vorlage für Einstellungs Speicherort mit UE-V.</span><span class="sxs-lookup"><span data-stu-id="17233-222">Updates a settings location template with UE-V.</span></span> <span data-ttu-id="17233-223">Die neue Vorlage sollte eine neuere Version als die vorhandene sein.</span><span class="sxs-lookup"><span data-stu-id="17233-223">The new template should be a newer version than the existing one.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class MachineConfiguredWindows8App -Name RemoveApp -ArgumentList &lt;package family name | package family name&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="17233-224">Entfernt eine oder mehrere Windows-Apps aus der Windows-App-Liste der Computer.</span><span class="sxs-lookup"><span data-stu-id="17233-224">Removes one or more Windows apps from the computer Windows app list.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class UserConfiguredWindows8App -Name RemoveApp -ArgumentList &lt;package family name | package family name&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="17233-225">Entfernt eine oder mehrere Windows-Apps aus der Windows-App-Liste der aktuellen Benutzer.</span><span class="sxs-lookup"><span data-stu-id="17233-225">Removes one or more Windows apps from the current user Windows app list.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name DisableByTemplateId -ArgumentList &lt;template ID&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="17233-226">Deaktiviert eine oder mehrere Einstellungen-Standort Vorlagen mit UE-V.</span><span class="sxs-lookup"><span data-stu-id="17233-226">Disables one or more settings location templates with UE-V.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class MachineConfiguredWindows8App -Name DisableApp -ArgumentList &lt;package family name | package family name&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="17233-227">Deaktiviert eine oder mehrere Windows-apps in der Windows-App-Liste der Computer.</span><span class="sxs-lookup"><span data-stu-id="17233-227">Disables one or more Windows apps in the computer Windows app list.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class UserConfiguredWindows8App -Name DisableApp -ArgumentList &lt;package family name | package family name&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="17233-228">Deaktiviert eine oder mehrere Windows-apps in der Windows-App-Liste der aktuellen Benutzer.</span><span class="sxs-lookup"><span data-stu-id="17233-228">Disables one or more Windows apps in the current user Windows app list.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name EnableByTemplateId -ArgumentList &lt;template ID&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="17233-229">Aktiviert eine Einstellungs Speicherort Vorlage mit UE-V.</span><span class="sxs-lookup"><span data-stu-id="17233-229">Enables a settings location template with UE-V.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class MachineConfiguredWindows8App -Name EnableApp -ArgumentList &lt;package family name | package family name&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="17233-230">Aktiviert Windows-apps in der Windows-App-Liste der Computer.</span><span class="sxs-lookup"><span data-stu-id="17233-230">Enables Windows apps in the computer Windows app list.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class UserConfiguredWindows8App -Name EnableApp -ArgumentList &lt;package family name | package family name&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="17233-231">Aktiviert Windows-apps in der Windows-App-Liste der aktuellen Benutzer.</span><span class="sxs-lookup"><span data-stu-id="17233-231">Enables Windows apps in the current user Windows app list.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name Validate -ArgumentList &lt;template path&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="17233-232">Bestimmt, ob eine angegebene Speicherort Vorlage für Einstellungen dem XML-Schema entspricht.</span><span class="sxs-lookup"><span data-stu-id="17233-232">Determines whether a given settings location template complies with its XML schema.</span></span></p></td>
    </tr>
    </tbody>
    </table>



~~~
**Note**  
Where a list of Package Family Names is called by the WMI command, the list must be in quotes and separated by a pipe symbol, for example, `"<package family name | package family name>"`.
~~~



### <span data-ttu-id="17233-233">Bereitstellen des UE-V-Agents mithilfe von Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="17233-233">Deploying the UE-V Agent using Windows PowerShell</span></span>

**<span data-ttu-id="17233-234">Bereitstellen des UE-V-Agents mithilfe von Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="17233-234">How to deploy the UE-V Agent by using Windows PowerShell</span></span>**

1.  <span data-ttu-id="17233-235">Stufen Sie das Installationspaket des UE-V-Agents in einer barrierefreien Netzwerkfreigabe ein.</span><span class="sxs-lookup"><span data-stu-id="17233-235">Stage the UE-V Agent installation package in an accessible network share.</span></span>

    **<span data-ttu-id="17233-236">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="17233-236">Note</span></span>**  
    <span data-ttu-id="17233-237">Verwenden Sie AgentSetup.exe, um sowohl 32-Bit-als auch 64-Bit-Versionen des UE-V-Agents bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="17233-237">Use AgentSetup.exe to deploy both 32-bit and 64-bit versions of the UE-V Agent.</span></span> <span data-ttu-id="17233-238">Die Windows Installer-Pakete, AgentSetupx86.msi und AgentSetupx64.msi, stehen für jede Architektur zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="17233-238">The Windows Installer packages, AgentSetupx86.msi and AgentSetupx64.msi, are available for each architecture.</span></span> <span data-ttu-id="17233-239">Wenn Sie den UE-V-Agent zu einem späteren Zeitpunkt mithilfe der Installationsdatei deinstallieren möchten, müssen Sie denselben Dateityp verwenden.</span><span class="sxs-lookup"><span data-stu-id="17233-239">To uninstall the UE-V Agent at a later time by using the installation file, you must use the same file type.</span></span>



2.  <span data-ttu-id="17233-240">Verwenden Sie einen der folgenden Windows PowerShell-Befehle, um den UE-V-Agent zu installieren.</span><span class="sxs-lookup"><span data-stu-id="17233-240">Use one of the following Windows PowerShell commands to install the UE-V Agent.</span></span>

    -   `& AgentSetup.exe /quiet /norestart /log "%temp%\UE-VAgentInstaller.log" SettingsStoragePath=\\server\settingsshare\%username%`

    -   `& msiexec.exe /i "<path to msi file>" /quiet /norestart /l*v "%temp%\UE-VAgentInstaller.log" SettingsStoragePath=\\server\settingsshare\%username%`

<span data-ttu-id="17233-241">Sie **haben einen Vorschlag für UE-V**?</span><span class="sxs-lookup"><span data-stu-id="17233-241">**Got a suggestion for UE-V**?</span></span> <span data-ttu-id="17233-242">[Hier](http://uev.uservoice.com/forums/280428-microsoft-user-experience-virtualization)können Sie Vorschläge hinzufügen oder abstimmen.</span><span class="sxs-lookup"><span data-stu-id="17233-242">Add or vote on suggestions [here](http://uev.uservoice.com/forums/280428-microsoft-user-experience-virtualization).</span></span> <span data-ttu-id="17233-243">**Haben Sie ein UE-V-Problem**?</span><span class="sxs-lookup"><span data-stu-id="17233-243">**Got a UE-V issue**?</span></span> <span data-ttu-id="17233-244">Verwenden Sie das [UE-V TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopuev).</span><span class="sxs-lookup"><span data-stu-id="17233-244">Use the [UE-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopuev).</span></span>

## <span data-ttu-id="17233-245">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="17233-245">Related topics</span></span>


[<span data-ttu-id="17233-246">Verwalten von UE-V 2. x mit Windows PowerShell und WMI</span><span class="sxs-lookup"><span data-stu-id="17233-246">Administering UE-V 2.x with Windows PowerShell and WMI</span></span>](administering-ue-v-2x-with-windows-powershell-and-wmi-both-uevv2.md)

[<span data-ttu-id="17233-247">Verwalten von UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="17233-247">Administering UE-V 2.x</span></span>](administering-ue-v-2x-new-uevv2.md)









