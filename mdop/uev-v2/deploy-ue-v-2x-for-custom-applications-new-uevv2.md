---
title: Bereitstellen von UE-V 2. x für benutzerdefinierte Anwendungen
description: Bereitstellen von UE-V 2. x für benutzerdefinierte Anwendungen
author: dansimp
ms.assetid: f7cb089f-d764-4a93-82b6-926fe0385a23
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 07/19/2016
ms.openlocfilehash: 217f647d948df016c4a6b72736669c2b3305b705
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810534"
---
# <span data-ttu-id="b6f96-103">Bereitstellen von UE-V 2. x für benutzerdefinierte Anwendungen</span><span class="sxs-lookup"><span data-stu-id="b6f96-103">Deploy UE-V 2.x for Custom Applications</span></span>


<span data-ttu-id="b6f96-104">Microsoft User Experience Virtualization (UE-V) 2,0</span><span class="sxs-lookup"><span data-stu-id="b6f96-104">Microsoft User Experience Virtualization (UE-V) 2.0.</span></span> <span data-ttu-id="b6f96-105">2,1 und 2,1 SP1 verwenden XML-Dateien namens " **Einstellungen** ", um die Einstellungen für die Desktopanwendung und die Windows-Desktopeinstellungen zwischen den Benutzercomputern zu überwachen und zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="b6f96-105">2.1, and 2.1 SP1 use XML files called **settings location templates** to monitor and synchronize desktop application settings and Windows desktop settings between user computers.</span></span> <span data-ttu-id="b6f96-106">In UE-V sind standardmäßig einige Einstellungsortvorlagen enthalten.</span><span class="sxs-lookup"><span data-stu-id="b6f96-106">By default, some settings location templates are included in UE-V.</span></span> <span data-ttu-id="b6f96-107">Wenn Sie jedoch die Einstellungen für Desktopanwendungen, die nicht in den Standardvorlagen enthalten sind, synchronisieren möchten, können Sie mithilfe des UE-V-Generators ihre eigenen Speicherort Vorlagen für benutzerdefinierte Einstellungen erstellen.</span><span class="sxs-lookup"><span data-stu-id="b6f96-107">But if you want to synchronize settings for desktop applications other than those included in the default templates, you can create your own custom settings location templates by using the UE-V Generator.</span></span>

<span data-ttu-id="b6f96-108">Nachdem Sie das Planungs Material in [Vorbereiten einer UE-v 2. x-Bereitstellung](prepare-a-ue-v-2x-deployment-new-uevv2.md) gelesen haben und entschieden haben, dass Sie die Einstellungen für benutzerdefinierte Anwendungen (Drittanbieter, Branchen usw.) synchronisieren möchten, stellen Sie die Features von UE-v bereit, wie in diesem Thema beschrieben.</span><span class="sxs-lookup"><span data-stu-id="b6f96-108">Once you have read through the planning material in [Prepare a UE-V 2.x Deployment](prepare-a-ue-v-2x-deployment-new-uevv2.md) and have decided that you want to synchronize settings for custom applications (third-party, line-of-business, etc.), you will deploy the features of UE-V as described in this topic.</span></span> <span data-ttu-id="b6f96-109">Um zu beginnen, müssen Sie die wichtigsten Schritte zum Synchronisieren von Einstellungen für benutzerdefinierte Anwendungen ausführen:</span><span class="sxs-lookup"><span data-stu-id="b6f96-109">To start, here are the main steps required to synchronize settings for custom applications:</span></span>

-   [<span data-ttu-id="b6f96-110">Installieren des UEV-Generators</span><span class="sxs-lookup"><span data-stu-id="b6f96-110">Install the UEV Generator</span></span>](#uevgen)

    <span data-ttu-id="b6f96-111">Verwenden Sie den UEV-Generator, um benutzerdefinierte Speicherort Vorlagen für XML-Einstellungen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="b6f96-111">Use the UEV Generator to create custom XML settings location templates.</span></span>

-   [<span data-ttu-id="b6f96-112">Konfigurieren eines UE-V-Einstellungs Vorlagen Katalogs</span><span class="sxs-lookup"><span data-stu-id="b6f96-112">Configure a UE-V settings template catalog</span></span>](#deploycatalogue)

    <span data-ttu-id="b6f96-113">Sie können diesen Pfad definieren, in dem die Speicherort Vorlagen für benutzerdefinierte Einstellungen gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="b6f96-113">You can define this path where custom settings location templates are stored.</span></span>

-   [<span data-ttu-id="b6f96-114">Erstellen von Speicherort Vorlagen für benutzerdefinierte Einstellungen</span><span class="sxs-lookup"><span data-stu-id="b6f96-114">Create custom settings location templates</span></span>](#createcustomtemplates)

    <span data-ttu-id="b6f96-115">Mithilfe dieser benutzerdefinierten Vorlagen können Benutzer die Einstellungen für benutzerdefinierte Anwendungen synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="b6f96-115">These custom templates let users sync settings for custom applications.</span></span>

-   [<span data-ttu-id="b6f96-116">Bereitstellen der Speicherort Vorlagen für benutzerdefinierte Einstellungen</span><span class="sxs-lookup"><span data-stu-id="b6f96-116">Deploy the custom settings location templates</span></span>](#deploycustomtemplates)

    <span data-ttu-id="b6f96-117">Nachdem Sie die benutzerdefinierte Vorlage getestet haben, um sicherzustellen, dass die Einstellungen ordnungsgemäß synchronisiert werden, können Sie diese Vorlagen auf eine der folgenden Arten bereitstellen:</span><span class="sxs-lookup"><span data-stu-id="b6f96-117">After you test the custom template to ensure that settings are synced correctly, you can deploy these templates in one of these ways:</span></span>

    -   <span data-ttu-id="b6f96-118">Über Ihre vorhandene Bereitstellungsinfrastruktur wie Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="b6f96-118">Through your existing deployment infrastructure, such as Configuration Manager</span></span>

    -   <span data-ttu-id="b6f96-119">Verwenden von Gruppenrichtlinieneinstellungen</span><span class="sxs-lookup"><span data-stu-id="b6f96-119">By using Group Policy preferences</span></span>

    -   [<span data-ttu-id="b6f96-120">Bereitstellen eines UE-V-Einstellungs Vorlagen Katalogs</span><span class="sxs-lookup"><span data-stu-id="b6f96-120">Deploy a UE-V settings template catalog</span></span>](#deploycatalogue)

    <span data-ttu-id="b6f96-121">**Hinweis**  Vorlagen, die mithilfe von ESD-oder Gruppenrichtlinien bereitgestellt werden, müssen bei der UE-V-Windows-Verwaltungsinstrumentation (WMI) oder Windows PowerShell registriert sein.</span><span class="sxs-lookup"><span data-stu-id="b6f96-121">**Note** Templates that are deployed by using ESD or Group Policy must be registered with UE-V Windows Management Instrumentation (WMI) or Windows PowerShell.</span></span>

     

## <span data-ttu-id="b6f96-122">Vorbereiten der Bereitstellung von UE-V 2. x für benutzerdefinierte Anwendungen</span><span class="sxs-lookup"><span data-stu-id="b6f96-122">Prepare to Deploy UE-V 2.x for Custom Applications</span></span>


<span data-ttu-id="b6f96-123">Bevor Sie mit der Bereitstellung der UE-V-Features beginnen, die benutzerdefinierte Anwendungen behandeln, müssen Sie nur einige Punkte überprüfen.</span><span class="sxs-lookup"><span data-stu-id="b6f96-123">Before you start deploying the UE-V features that handle custom applications, there are just a couple things to review.</span></span>

### <span data-ttu-id="b6f96-124">Der UE-V-Generator</span><span class="sxs-lookup"><span data-stu-id="b6f96-124">The UE-V Generator</span></span>

<span data-ttu-id="b6f96-125">Der UE-V-Generator überwacht eine Anwendung, um die Speicherorte, an denen die Anwendung Ihre Einstellungen speichert, zu ermitteln und zu erfassen.</span><span class="sxs-lookup"><span data-stu-id="b6f96-125">The UE-V Generator monitors an application to discover and capture the locations where the application stores its settings.</span></span> <span data-ttu-id="b6f96-126">Die Anwendung, die überwacht wird, muss eine herkömmliche Anwendung sein.</span><span class="sxs-lookup"><span data-stu-id="b6f96-126">The application that is monitored must be a traditional application.</span></span> <span data-ttu-id="b6f96-127">Sie verwenden den UE-V-Generator zum Erstellen von Einstellungen für Speicherort Vorlagen, aber es kann keine Vorlage für eine Einstellungsposition aus diesen Anwendungstypen erstellen:</span><span class="sxs-lookup"><span data-stu-id="b6f96-127">You use the UE-V Generator to create settings location templates, but it cannot create a settings location template from these application types:</span></span>

-   <span data-ttu-id="b6f96-128">Virtualisierte Anwendungen</span><span class="sxs-lookup"><span data-stu-id="b6f96-128">Virtualized applications</span></span>

-   <span data-ttu-id="b6f96-129">Anwendungen, die über die Terminal Dienste angeboten werden</span><span class="sxs-lookup"><span data-stu-id="b6f96-129">Applications that are offered through Terminal Services</span></span>

-   <span data-ttu-id="b6f96-130">Java-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="b6f96-130">Java applications</span></span>

-   <span data-ttu-id="b6f96-131">Windows-Apps  </span><span class="sxs-lookup"><span data-stu-id="b6f96-131">Windows apps</span></span>

<span data-ttu-id="b6f96-132">**Hinweis**  Die Standort Vorlagen für die UE-V-Einstellungen können nicht aus virtualisierten Anwendungen oder Terminal Dienste-Anwendungen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="b6f96-132">**Note** UE-V settings location templates cannot be created from virtualized applications or Terminal Services applications.</span></span> <span data-ttu-id="b6f96-133">Einstellungen, die mithilfe der Vorlagen synchronisiert werden, können jedoch auf diese Anwendungen angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="b6f96-133">However, settings that are synchronized by using the templates can be applied to those applications.</span></span> <span data-ttu-id="b6f96-134">Öffnen Sie zum Erstellen von Vorlagen zur Unterstützung von VDI-Anwendungen (Virtual Desktop Infrastructure) und von Terminal Diensten eine Version des Windows Installer-Pakets (MSI) der Anwendung mithilfe des UE-V-Generators.</span><span class="sxs-lookup"><span data-stu-id="b6f96-134">To create templates that support Virtual Desktop Infrastructure (VDI) and Terminal Services applications, open a version of the Windows Installer (.msi) package of the application by using the UE-V Generator.</span></span> <span data-ttu-id="b6f96-135">Weitere Informationen zum Synchronisieren von Einstellungen für virtuelle Anwendungen finden Sie unter [Verwenden von UE-V 2. x mit Application Virtualization-Anwendungen](using-ue-v-2x-with-application-virtualization-applications-both-uevv2.md).</span><span class="sxs-lookup"><span data-stu-id="b6f96-135">For more information about synchronizing settings for virtual applications, see [Using UE-V 2.x with Application Virtualization Applications](using-ue-v-2x-with-application-virtualization-applications-both-uevv2.md).</span></span>

 

<span data-ttu-id="b6f96-136">**Ausgeschlossene Speicherorte:** Der Ermittlungsprozess schließt Speicherorte aus, die häufig Anwendungssoftware Dateien speichern, die die Einstellungen nicht gut zwischen Benutzercomputern oder Computerumgebungen synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="b6f96-136">**Excluded Locations:** The discovery process excludes locations that commonly store application software files that do not synchronize settings well between user computers or computing environments.</span></span> <span data-ttu-id="b6f96-137">Standardmäßig sind diese ausgeschlossen:</span><span class="sxs-lookup"><span data-stu-id="b6f96-137">By default, these are excluded:</span></span>

-   <span data-ttu-id="b6f96-138">HKEY \ _CURRENT \ _User Registrierungsschlüssel und Dateien, für die der angemeldete Benutzer keine Werte schreiben kann</span><span class="sxs-lookup"><span data-stu-id="b6f96-138">HKEY\_CURRENT\_USER registry keys and files to which the logged-on user cannot write values</span></span>

-   <span data-ttu-id="b6f96-139">HKEY \ _CURRENT \ _User Registrierungsschlüssel und Dateien, die der Kernfunktionalität des Windows-Betriebssystems zugeordnet sind</span><span class="sxs-lookup"><span data-stu-id="b6f96-139">HKEY\_CURRENT\_USER registry keys and files that are associated with the core functionality of the Windows operating system</span></span>

-   <span data-ttu-id="b6f96-140">Alle Registrierungsschlüssel, die sich im HKEY \ _LOCAL \ _MACHINE Hive befinden</span><span class="sxs-lookup"><span data-stu-id="b6f96-140">All registry keys that are located in the HKEY\_LOCAL\_MACHINE hive</span></span>

-   <span data-ttu-id="b6f96-141">Dateien, die sich in Verzeichnissen von Programmdateien befinden</span><span class="sxs-lookup"><span data-stu-id="b6f96-141">Files that are located in Program Files directories</span></span>

-   <span data-ttu-id="b6f96-142">Dateien, die sich in den Benutzern befinden \ \ \ [Benutzername \] \ \ APPDATA \ \ LocalLow</span><span class="sxs-lookup"><span data-stu-id="b6f96-142">Files that are located in Users \\ \[User name\] \\ AppData \\ LocalLow</span></span>

-   <span data-ttu-id="b6f96-143">Windows-Betriebssystemdateien, die sich in% SystemRoot% befinden</span><span class="sxs-lookup"><span data-stu-id="b6f96-143">Windows operating system files that are located in %Systemroot%</span></span>

<span data-ttu-id="b6f96-144">Wenn Registrierungsschlüssel und Dateien, die in ausgeschlossenen Speicherorten gespeichert sind, zum Synchronisieren von Anwendungseinstellungen erforderlich sind, können Sie die Speicherorte während des Erstellungsprozesses der Vorlage manuell zur Vorlage "Einstellungs Speicherort" hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="b6f96-144">If registry keys and files that are stored in excluded locations are required to synchronize application settings, you can manually add the locations to the settings location template during the template creation process.</span></span>
<span data-ttu-id="b6f96-145">Es werden jedoch nur Änderungen an der HKEY \ _CURRENT \ _User Hive synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="b6f96-145">However, only changes to the HKEY\_CURRENT\_USER hive will be sync-ed.</span></span>

### <span data-ttu-id="b6f96-146">Ersetzen der standardmäßigen Microsoft-Vorlagen</span><span class="sxs-lookup"><span data-stu-id="b6f96-146">Replace the default Microsoft templates</span></span>

<span data-ttu-id="b6f96-147">Der UE-V-Agent installiert eine Standardgruppe von Einstellungen-Standort Vorlagen für allgemeine Microsoft-Anwendungen und Windows-Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="b6f96-147">The UE-V Agent installs a default group of settings location templates for common Microsoft applications and Windows settings.</span></span> <span data-ttu-id="b6f96-148">Wenn Sie diese Vorlagen anpassen oder Einstellungen für Standort Vorlagen zum Synchronisieren von Einstellungen für benutzerdefinierte Anwendungen erstellen, kann der UE-V-Agent so konfiguriert werden, dass ein Einstellungs Vorlagenkatalog zum Speichern der Vorlagen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b6f96-148">If you customize these templates, or create settings location templates to synchronize settings for custom applications, the UE-V Agent can be configured to use a settings template catalog to store the templates.</span></span> <span data-ttu-id="b6f96-149">In diesem Fall müssen Sie die Standardvorlagen zusammen mit den benutzerdefinierten Vorlagen im Vorlagenkatalog für Einstellungen hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="b6f96-149">In this case, you will need to include the default templates along with the custom templates in the settings template catalog.</span></span>

<span data-ttu-id="b6f96-150">Wenn Sie [einen UE-V-Agent bereitstellen](https://technet.microsoft.com/library/dn458891.aspx#agent), können Sie den Befehlszeilenparameter verwenden, `RegisterMSTemplates` um die Registrierung der Microsoft-Standardvorlagen zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="b6f96-150">When you [Deploy a UE-V Agent](https://technet.microsoft.com/library/dn458891.aspx#agent), you can use the command-line parameter `RegisterMSTemplates` to disable the registration of the default Microsoft templates.</span></span>

<span data-ttu-id="b6f96-151">Wenn Sie Gruppenrichtlinien zum Konfigurieren des Katalog Pfads für Einstellungs Vorlagen verwenden, können Sie auswählen, dass die standardmäßigen Microsoft-Vorlagen ersetzt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b6f96-151">When you use Group Policy to configure the settings template catalog path, you can choose to replace the default Microsoft templates.</span></span> <span data-ttu-id="b6f96-152">Wenn Sie die Richtlinieneinstellungen so konfigurieren, dass die standardmäßigen Microsoft-Vorlagen ersetzt werden, werden alle Microsoft-Standardvorlagen, die vom UE-V-Agent installiert werden, gelöscht, und es werden nur die Vorlagen verwendet, die sich im Katalog der Einstellungs Vorlagen befinden.</span><span class="sxs-lookup"><span data-stu-id="b6f96-152">If you configure the policy settings to replace the default Microsoft templates, all of the default Microsoft templates that are installed by the UE-V Agent are deleted and only the templates that are located in the settings template catalog are used.</span></span> <span data-ttu-id="b6f96-153">Der Parameter für die Konfigurationseinstellung des UE-V-Agents `RegisterMSTemplates` muss auf " *true* " festgelegt werden, um die standardmäßige Microsoft-Vorlage zu überschreiben.</span><span class="sxs-lookup"><span data-stu-id="b6f96-153">The UE-V Agent configuration setting parameter `RegisterMSTemplates` must be set to *true* in order to override the default Microsoft template.</span></span>

<span data-ttu-id="b6f96-154">**Hinweis**  Wenn Sie diese Richtlinieneinstellung nach der Aktivierung deaktivieren, werden die standardmäßigen Microsoft-Vorlagen vom UE-V-Agent nicht wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="b6f96-154">**Note** If you disable this policy setting after it has been enabled, the UE-V Agent does not restore the default Microsoft templates.</span></span>

 

<span data-ttu-id="b6f96-155">Wenn im Einstellungs Vorlagenkatalog angepasste Vorlagen vorhanden sind, die die gleiche ID wie die standardmäßigen Microsoft-Vorlagen verwenden, und der UE-V-Agent nicht so konfiguriert ist, dass die standardmäßigen Microsoft-Vorlagen ersetzt werden, werden die Microsoft-Vorlagen ignoriert.</span><span class="sxs-lookup"><span data-stu-id="b6f96-155">If there are customized templates in the settings template catalog that use the same ID as the default Microsoft templates, and the UE-V Agent is not configured to replace the default Microsoft templates, the Microsoft templates are ignored.</span></span>

<span data-ttu-id="b6f96-156">Sie können die Standardvorlagen auch ersetzen, indem Sie die Windows PowerShell-Features von UE-V verwenden.</span><span class="sxs-lookup"><span data-stu-id="b6f96-156">You can also replace the default templates by using the UE-V Windows PowerShell features.</span></span> <span data-ttu-id="b6f96-157">Wenn Sie die standardmäßige Microsoft-Vorlage durch Windows PowerShell ersetzen möchten, heben Sie die Registrierung aller Microsoft-Standardvorlagen auf, und registrieren Sie dann die angepassten Vorlagen.</span><span class="sxs-lookup"><span data-stu-id="b6f96-157">To replace the default Microsoft template with Windows PowerShell, unregister all of the default Microsoft templates, and then register the customized templates.</span></span>

<span data-ttu-id="b6f96-158">**Hinweis**  Alte Einstellungs Pakete verbleiben im Einstellungs Speicherort, auch wenn Sie für eine Anwendung neue Speicherort Vorlagen für Einstellungen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="b6f96-158">**Note** Old settings packages remain in the settings storage location even if you deploy new settings location templates for an application.</span></span> <span data-ttu-id="b6f96-159">Diese Pakete werden nicht vom Agenten gelesen, aber auch nicht automatisch gelöscht.</span><span class="sxs-lookup"><span data-stu-id="b6f96-159">These packages are not read by the agent, but neither are they automatically deleted.</span></span>

 

## <a href="" id="uevgen"></a><span data-ttu-id="b6f96-160">Installieren des UEV 2. x-Generators</span><span class="sxs-lookup"><span data-stu-id="b6f96-160">Install the UEV 2.x Generator</span></span>


<span data-ttu-id="b6f96-161">Installieren Sie den Microsoft User Experience Virtualization (UE-V) 2,0-Generator auf einem Computer, den Sie dann zum Erstellen einer benutzerdefinierten Speicherort Vorlage für Einstellungen verwenden können.</span><span class="sxs-lookup"><span data-stu-id="b6f96-161">Install the Microsoft User Experience Virtualization (UE-V) 2.0 Generator on a computer that you can then use to create a custom settings location template.</span></span> <span data-ttu-id="b6f96-162">Auf diesem Computer sollten die Anwendungen installiert sein, für die benutzerdefinierte Einstellungen für Standort Vorlagen generiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b6f96-162">This computer should have the applications installed for which custom settings location templates are to be generated.</span></span>

**<span data-ttu-id="b6f96-163">So installieren Sie den UE-V-Generator</span><span class="sxs-lookup"><span data-stu-id="b6f96-163">To install the UE-V Generator</span></span>**

1.  <span data-ttu-id="b6f96-164">Suchen Sie als Benutzer mit lokalen Administratorrechten die Installationsdatei des UE-v-Generators, **ToolSetup.exe** die mit der UE-v-Software bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="b6f96-164">As a user with local administrator rights, locate the UE-V Generator installation file **ToolSetup.exe** provided with the UE-V software.</span></span> <span data-ttu-id="b6f96-165">Wenn Ihnen die Computerarchitektur bekannt ist, können Sie die entsprechende Windows Installer-Datei (MSI), **ToolsSetupx64.msi** oder **ToolsSetupx86.msi**ausführen.</span><span class="sxs-lookup"><span data-stu-id="b6f96-165">Or, if you know the computer architecture, you can run the appropriate Windows Installer (.msi) file, **ToolsSetupx64.msi** or **ToolsSetupx86.msi**.</span></span>

2.  <span data-ttu-id="b6f96-166">Doppelklicken Sie auf die Installationsdatei.</span><span class="sxs-lookup"><span data-stu-id="b6f96-166">Double-click the installation file.</span></span> <span data-ttu-id="b6f96-167">Der Setup-Assistent von User Experience Virtualization Generator wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="b6f96-167">The User Experience Virtualization Generator Setup wizard opens.</span></span> <span data-ttu-id="b6f96-168">Klicken Sie auf **Weiter**, um den Vorgang fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="b6f96-168">Click **Next** to continue.</span></span>

3.  <span data-ttu-id="b6f96-169">Akzeptieren Sie die Microsoft-Software-Lizenzbestimmungen, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="b6f96-169">Accept the Microsoft Software License Terms, and then click **Next**.</span></span>

4.  <span data-ttu-id="b6f96-170">Klicken Sie auf die Optionen für Microsoft Updates und das Programm zur Verbesserung der Benutzerfreundlichkeit.</span><span class="sxs-lookup"><span data-stu-id="b6f96-170">Click the options for Microsoft Updates and the Customer Experience Improvement Program.</span></span>

5.  <span data-ttu-id="b6f96-171">Wählen Sie den Zielordner aus, in dem der UE-V-Generator installiert werden soll, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="b6f96-171">Select the destination folder in which to install the UE-V Generator, and then click **Next**.</span></span>

6.  <span data-ttu-id="b6f96-172">Klicken Sie auf **Installieren** , um mit der Installation zu beginnen.</span><span class="sxs-lookup"><span data-stu-id="b6f96-172">Click **Install** to begin the installation.</span></span>

    <span data-ttu-id="b6f96-173">**Hinweis**  Vor der Installation der Anwendung wird eine Aufforderung zur **Benutzerkontensteuerung** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b6f96-173">**Note** A prompt for **User Account Control** appears before the application is installed.</span></span> <span data-ttu-id="b6f96-174">Zum Installieren des UE-V-Generators ist eine Berechtigung erforderlich.</span><span class="sxs-lookup"><span data-stu-id="b6f96-174">Permission is required to install the UE-V Generator.</span></span>

     

7.  <span data-ttu-id="b6f96-175">Klicken Sie auf **Fertig stellen** , um den Assistenten zu schließen, nachdem die Installation abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="b6f96-175">Click **Finish** to close the wizard after the installation is finished.</span></span> <span data-ttu-id="b6f96-176">Sie müssen den Computer neu starten, bevor Sie den UE-V-Generator ausführen können.</span><span class="sxs-lookup"><span data-stu-id="b6f96-176">You must restart your computer before you can run the UE-V Generator.</span></span>

    <span data-ttu-id="b6f96-177">Um zu überprüfen, ob die Installation erfolgreich war, klicken Sie auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Microsoft User Experience Virtualization**, und klicken Sie dann auf **Microsoft User Experience Virtualization Generator**.</span><span class="sxs-lookup"><span data-stu-id="b6f96-177">To verify that the installation was successful, click **Start**, click **All Programs**, click **Microsoft User Experience Virtualization**, and then click **Microsoft User Experience Virtualization Generator**.</span></span>

    <span data-ttu-id="b6f96-178">**Hinweis**  Der UE-v 2-Generator kann nur zum Erstellen von Vorlagen für UE-v 2-Agents verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b6f96-178">**Note** The UE-V 2 Generator can only be used to create templates for UE-V 2 Agents.</span></span> <span data-ttu-id="b6f96-179">Bei einer gemischten Bereitstellung von UE-v 1,0-Agents und UE-v 2-Agents sollten Sie den UE-v 1,0-Generator weiterhin verwenden, bis Sie alle UE-v-Agents aktualisiert haben.</span><span class="sxs-lookup"><span data-stu-id="b6f96-179">In a mixed deployment of UE-V 1.0 Agents and UE-V 2 Agents, you should continue to use the UE-V 1.0 Generator until you have upgraded all UE-V Agents.</span></span>

     

## <a href="" id="deploycatalogue"></a><span data-ttu-id="b6f96-180">Bereitstellen eines Einstellungs Vorlagen Katalogs</span><span class="sxs-lookup"><span data-stu-id="b6f96-180">Deploy a Settings Template Catalog</span></span>


<span data-ttu-id="b6f96-181">Der Katalog der Benutzeroberflächen-Virtualisierungs-Einstellungen ist ein Ordnerpfad auf UE-V-Computern oder eine SMB-Netzwerkfreigabe (Server Message Block), in der alle Speicherorte für benutzerdefinierte Einstellungen gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="b6f96-181">The User Experience Virtualization settings template catalog is a folder path on UE-V computers or a Server Message Block (SMB) network share that stores all the custom settings location templates.</span></span> <span data-ttu-id="b6f96-182">Ein geplanter Task im UE-V-Agent überprüft diesen Standort einmal täglich und aktualisiert sein Synchronisierungsverhalten basierend auf den Vorlagen in diesem Ordner.</span><span class="sxs-lookup"><span data-stu-id="b6f96-182">A scheduled task in the UE-V Agent checks this location one time each day and updates its synchronization behavior, based on the templates in this folder.</span></span>

<span data-ttu-id="b6f96-183">Der UE-V-Agent registriert Vorlagen, die in diesem Ordner nach dem letzten Überprüfen des Ordners hinzugefügt oder aktualisiert wurden, und hebt die Registrierung von Vorlagen auf, die entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="b6f96-183">The UE-V Agent registers templates that were added or updated in this folder after the last time that the folder was checked and unregisters templates that are removed.</span></span> <span data-ttu-id="b6f96-184">Standardmäßig werden Vorlagen um 3:30 Uhr einmal pro Tag registriert und nicht registriert.</span><span class="sxs-lookup"><span data-stu-id="b6f96-184">By default, templates are registered and unregistered one time per day at 3:30 A.M.</span></span> <span data-ttu-id="b6f96-185">Ortszeit durch den Aufgabenplaner und beim Systemstart.</span><span class="sxs-lookup"><span data-stu-id="b6f96-185">local time by the Task Scheduler and at system startup.</span></span> <span data-ttu-id="b6f96-186">Informationen zum Anpassen der Häufigkeit dieser geplanten Aufgabe finden Sie unter [Ändern der Häufigkeit von geplanten Aufgaben in UE-V 2. x](changing-the-frequency-of-ue-v-2x-scheduled-tasks-both-uevv2.md).</span><span class="sxs-lookup"><span data-stu-id="b6f96-186">To customize the frequency of this scheduled task, see [Changing the Frequency of UE-V 2.x Scheduled Tasks](changing-the-frequency-of-ue-v-2x-scheduled-tasks-both-uevv2.md).</span></span>

<span data-ttu-id="b6f96-187">Sie können den Katalogpfad der Einstellungs Vorlage mithilfe der Befehlszeilenoptionen für die Installation, Gruppenrichtlinie, WMI oder Windows PowerShell konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="b6f96-187">You can configure the settings template catalog path by using the installation command-line options, Group Policy, WMI, or Windows PowerShell.</span></span> <span data-ttu-id="b6f96-188">Vorlagen, die im Katalogpfad für Einstellungs Vorlagen gespeichert sind, werden automatisch von einem geplanten Vorgang registriert und nicht registriert.</span><span class="sxs-lookup"><span data-stu-id="b6f96-188">Templates that are stored at the settings template catalog path are automatically registered and unregistered by a scheduled task.</span></span>

**<span data-ttu-id="b6f96-189">So konfigurieren Sie den Vorlagenkatalog für die Einstellungen für UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="b6f96-189">To configure the settings template catalog for UE-V 2.x</span></span>**

1.  <span data-ttu-id="b6f96-190">Erstellen Sie einen neuen Ordner auf dem Computer, auf dem der Vorlagenkatalog für UE-V-Einstellungen gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="b6f96-190">Create a new folder on the computer that stores the UE-V settings template catalog.</span></span>

2.  <span data-ttu-id="b6f96-191">Legen Sie die folgenden SMB-Berechtigungen (Freigabeebene) für den Katalogordner "Einstellungs Vorlagen" ein.</span><span class="sxs-lookup"><span data-stu-id="b6f96-191">Set the following share-level (SMB) permissions for the settings template catalog folder.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong><span data-ttu-id="b6f96-192">Benutzerkonto</span><span class="sxs-lookup"><span data-stu-id="b6f96-192">User account</span></span></strong></th>
    <th align="left"><strong><span data-ttu-id="b6f96-193">Empfohlene Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="b6f96-193">Recommended permissions</span></span></strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="b6f96-194">Jeder</span><span class="sxs-lookup"><span data-stu-id="b6f96-194">Everyone</span></span></p></td>
    <td align="left"><p><span data-ttu-id="b6f96-195">Keine Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="b6f96-195">No Permissions</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="b6f96-196">Domänencomputer</span><span class="sxs-lookup"><span data-stu-id="b6f96-196">Domain Computers</span></span></p></td>
    <td align="left"><p><span data-ttu-id="b6f96-197">Lesen von Berechtigungsstufen</span><span class="sxs-lookup"><span data-stu-id="b6f96-197">Read Permission Levels</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="b6f96-198">Administratoren</span><span class="sxs-lookup"><span data-stu-id="b6f96-198">Administrators</span></span></p></td>
    <td align="left"><p><span data-ttu-id="b6f96-199">Berechtigungsstufen für Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b6f96-199">Read/Write Permission Levels</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

3.  <span data-ttu-id="b6f96-200">Legen Sie die folgenden NTFS-Dateisystemberechtigungen für den Ordner "Einstellungs Vorlagenkatalog" ein.</span><span class="sxs-lookup"><span data-stu-id="b6f96-200">Set the following NTFS file system permissions for the settings template catalog folder.</span></span>

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="b6f96-201">Benutzerkonto</span><span class="sxs-lookup"><span data-stu-id="b6f96-201">User account</span></span></th>
    <th align="left"><span data-ttu-id="b6f96-202">Empfohlene Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="b6f96-202">Recommended permissions</span></span></th>
    <th align="left"><span data-ttu-id="b6f96-203">Anwenden auf</span><span class="sxs-lookup"><span data-stu-id="b6f96-203">Apply to</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="b6f96-204">Ersteller/Besitzer</span><span class="sxs-lookup"><span data-stu-id="b6f96-204">Creator/Owner</span></span></p></td>
    <td align="left"><p><span data-ttu-id="b6f96-205">Vollzugriff</span><span class="sxs-lookup"><span data-stu-id="b6f96-205">Full Control</span></span></p></td>
    <td align="left"><p><span data-ttu-id="b6f96-206">Dieser Ordner, Unterordner und Dateien</span><span class="sxs-lookup"><span data-stu-id="b6f96-206">This Folder, Subfolders and Files</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="b6f96-207">Domänencomputer</span><span class="sxs-lookup"><span data-stu-id="b6f96-207">Domain Computers</span></span></p></td>
    <td align="left"><p><span data-ttu-id="b6f96-208">Ordnerinhalte auflisten und lesen</span><span class="sxs-lookup"><span data-stu-id="b6f96-208">List Folder Contents and Read</span></span></p></td>
    <td align="left"><p><span data-ttu-id="b6f96-209">Dieser Ordner, Unterordner und Dateien</span><span class="sxs-lookup"><span data-stu-id="b6f96-209">This Folder, Subfolders and Files</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="b6f96-210">Jeder</span><span class="sxs-lookup"><span data-stu-id="b6f96-210">Everyone</span></span></p></td>
    <td align="left"><p><span data-ttu-id="b6f96-211">Keine Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="b6f96-211">No Permissions</span></span></p></td>
    <td align="left"><p><span data-ttu-id="b6f96-212">Keine Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="b6f96-212">No Permissions</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="b6f96-213">Administratoren</span><span class="sxs-lookup"><span data-stu-id="b6f96-213">Administrators</span></span></p></td>
    <td align="left"><p><span data-ttu-id="b6f96-214">Vollzugriff</span><span class="sxs-lookup"><span data-stu-id="b6f96-214">Full Control</span></span></p></td>
    <td align="left"><p><span data-ttu-id="b6f96-215">Dieser Ordner, Unterordner und Dateien</span><span class="sxs-lookup"><span data-stu-id="b6f96-215">This Folder, Subfolders and Files</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

4.  <span data-ttu-id="b6f96-216">Klicken Sie auf **OK** , um die Dialogfelder zu schließen.</span><span class="sxs-lookup"><span data-stu-id="b6f96-216">Click **OK** to close the dialog boxes.</span></span>

<span data-ttu-id="b6f96-217">Die Netzwerkfreigabe muss mindestens die Berechtigungen für die Gruppe "Domänencomputer" erteilen.</span><span class="sxs-lookup"><span data-stu-id="b6f96-217">At a minimum, the network share must grant permissions for the Domain Computers group.</span></span> <span data-ttu-id="b6f96-218">Gewähren Sie darüber hinaus Zugriffsberechtigungen für den Netzwerkfreigabeordner für Administratoren, die die gespeicherten Vorlagen verwalten sollen.</span><span class="sxs-lookup"><span data-stu-id="b6f96-218">In addition, grant access permissions for the network share folder to administrators who are to manage the stored templates.</span></span>

## <a href="" id="createcustomtemplates"></a><span data-ttu-id="b6f96-219">Erstellen von Speicherort Vorlagen für benutzerdefinierte Einstellungen</span><span class="sxs-lookup"><span data-stu-id="b6f96-219">Create Custom Settings Location Templates</span></span>


<span data-ttu-id="b6f96-220">Verwenden Sie den UE-V-Generator zum Erstellen von Einstellungen-Speicherort Vorlagen für Branchenanwendungen oder andere benutzerdefinierte Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="b6f96-220">Use the UE-V Generator to create settings location templates for line-of-business applications or other custom applications.</span></span> <span data-ttu-id="b6f96-221">Nachdem die Vorlage für eine Anwendung erstellt wurde, können Sie Sie auf Computern bereitstellen, damit die Einstellungen für diese Anwendung synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="b6f96-221">After the template for an application is created, you can deploy it to computers so that settings are synchronized for that application.</span></span>

**<span data-ttu-id="b6f96-222">So erstellen Sie eine Standort Vorlage für UE-v-Einstellungen mit dem UE-v-Generator</span><span class="sxs-lookup"><span data-stu-id="b6f96-222">To create a UE-V settings location template with the UE-V Generator</span></span>**

1.  <span data-ttu-id="b6f96-223">Klicken Sie auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Microsoft User Experience Virtualization**, und klicken Sie dann auf **Microsoft User Experience Virtualization Generator**.</span><span class="sxs-lookup"><span data-stu-id="b6f96-223">Click **Start**, click **All Programs**, click **Microsoft User Experience Virtualization**, and then click **Microsoft User Experience Virtualization Generator**.</span></span>

2.  <span data-ttu-id="b6f96-224">Klicken Sie auf **Vorlage zum Erstellen einer Einstellungsposition**.</span><span class="sxs-lookup"><span data-stu-id="b6f96-224">Click **Create a settings location template**.</span></span>

3.  <span data-ttu-id="b6f96-225">Geben Sie die Anwendung an.</span><span class="sxs-lookup"><span data-stu-id="b6f96-225">Specify the application.</span></span> <span data-ttu-id="b6f96-226">Navigieren Sie zum Dateipfad der Anwendung (. exe) oder der Anwendungsverknüpfung (. lnk), für die Sie eine Vorlage für eine Einstellungsposition erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="b6f96-226">Browse to the file path of the application (.exe) or the application shortcut (.lnk) for which you want to create a settings location template.</span></span> <span data-ttu-id="b6f96-227">Geben Sie die Befehlszeilenargumente (sofern vorhanden) und das Arbeitsverzeichnis an, sofern vorhanden.</span><span class="sxs-lookup"><span data-stu-id="b6f96-227">Specify the command-line arguments, if any, and working directory, if any.</span></span> <span data-ttu-id="b6f96-228">Klicken Sie auf **Weiter**, um den Vorgang fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="b6f96-228">Click **Next** to continue.</span></span>

    <span data-ttu-id="b6f96-229">**Hinweis**  Bevor die Anwendung gestartet wird, zeigt das System eine Aufforderung zur **Steuerung des Benutzerkontos**an.</span><span class="sxs-lookup"><span data-stu-id="b6f96-229">**Note** Before the application is started, the system displays a prompt for **User Account Control**.</span></span> <span data-ttu-id="b6f96-230">Zum Überwachen der Registrierungs-und Dateispeicherorte, die die Anwendung zum Speichern von Einstellungen verwendet, ist eine Berechtigung erforderlich.</span><span class="sxs-lookup"><span data-stu-id="b6f96-230">Permission is required to monitor the registry and file locations that the application uses to store settings.</span></span>

     

4.  <span data-ttu-id="b6f96-231">Schließen Sie die Anwendung, nachdem die Anwendung gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="b6f96-231">After the application starts, close the application.</span></span> <span data-ttu-id="b6f96-232">Der UE-V-Generator zeichnet die Speicherorte auf, an denen die Anwendung die Einstellungen speichert.</span><span class="sxs-lookup"><span data-stu-id="b6f96-232">The UE-V Generator records the locations where the application stores its settings.</span></span>

5.  <span data-ttu-id="b6f96-233">Klicken Sie nach Abschluss des Prozesses auf **weiter** , um fortzufahren.</span><span class="sxs-lookup"><span data-stu-id="b6f96-233">After the process is completed, click **Next** to continue.</span></span>

6.  <span data-ttu-id="b6f96-234">Überprüfen und aktivieren Sie die Kontrollkästchen neben den entsprechenden Speicherorten für Registrierungseinstellungen und Einstellungen für die Dateispeicherorte, die für diese Anwendung synchronisiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b6f96-234">Review and select the check boxes that are next to the appropriate registry settings locations and settings file locations to synchronize for this application.</span></span> <span data-ttu-id="b6f96-235">Die Liste enthält die folgenden beiden Kategorien für die Einstellungen für die Speicherorte:</span><span class="sxs-lookup"><span data-stu-id="b6f96-235">The list includes the following two categories for settings locations:</span></span>

    -   <span data-ttu-id="b6f96-236">**Standard**: Anwendungseinstellungen, die in der Registrierung unter dem HKEY \ _CURRENT \ _User Schlüssel oder in den Dateiordnern unter \ \ **Users** \ \ \ [Benutzername \] \ \ **AppData**  \\  **Roaming**gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="b6f96-236">**Standard**: Application settings that are stored in the registry under the HKEY\_CURRENT\_USER keys or in the file folders under \\ **Users** \\ \[User name\] \\ **AppData** \\ **Roaming**.</span></span> <span data-ttu-id="b6f96-237">Der UE-V-Generator enthält standardmäßig diese Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="b6f96-237">The UE-V Generator includes these settings by default.</span></span>

    -   <span data-ttu-id="b6f96-238">Nicht **Standard**: Anwendungseinstellungen, die außerhalb der Speicherorte gespeichert sind, werden in den bewährten Methoden für Einstellungsdaten Speicher (optional) angegeben.</span><span class="sxs-lookup"><span data-stu-id="b6f96-238">**Nonstandard**: Application settings that are stored outside the locations are specified in the best practices for settings data storage (optional).</span></span> <span data-ttu-id="b6f96-239">Dazu gehören Dateien und Ordner unter **Benutzer** \ \ \ [Benutzername \] \ \ **AppData**  \\  **local**.</span><span class="sxs-lookup"><span data-stu-id="b6f96-239">These include files and folders under **Users** \\ \[User name\] \\ **AppData** \\ **Local**.</span></span> <span data-ttu-id="b6f96-240">Überprüfen Sie diese Speicherorte, um zu bestimmen, ob Sie Sie in die Vorlage für den Einstellungs Speicherort einbeziehen möchten.</span><span class="sxs-lookup"><span data-stu-id="b6f96-240">Review these locations to determine whether to include them in the settings location template.</span></span> <span data-ttu-id="b6f96-241">Aktivieren Sie die Kontrollkästchen Speicherorte, um Sie einzubeziehen.</span><span class="sxs-lookup"><span data-stu-id="b6f96-241">Select the locations check boxes to include them.</span></span>

    <span data-ttu-id="b6f96-242">Klicken Sie auf **Weiter**, um den Vorgang fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="b6f96-242">Click **Next** to continue.</span></span>

7.  <span data-ttu-id="b6f96-243">Überprüfen und bearbeiten Sie alle **Eigenschaften**, **Registrierungs** Speicherorte und **Datei** Speicherorte für die Vorlage Speicherort für Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="b6f96-243">Review and edit any **Properties**, **Registry** locations, and **Files** locations for the settings location template.</span></span>

    -   <span data-ttu-id="b6f96-244">Bearbeiten Sie die folgenden Eigenschaften auf der Registerkarte " **Eigenschaften** ":</span><span class="sxs-lookup"><span data-stu-id="b6f96-244">Edit the following properties on the **Properties** tab:</span></span>

        -   <span data-ttu-id="b6f96-245">**Anwendungsname**: der Name der Anwendung, der in der Beschreibung der Programmdatei Eigenschaften geschrieben ist.</span><span class="sxs-lookup"><span data-stu-id="b6f96-245">**Application Name**: The application name that is written in the description of the program files properties.</span></span>

        -   <span data-ttu-id="b6f96-246">**Programmname**: der Name des Programms, das aus den Programmdatei Eigenschaften übernommen wird.</span><span class="sxs-lookup"><span data-stu-id="b6f96-246">**Program name**: The name of the program that is taken from the program file properties.</span></span> <span data-ttu-id="b6f96-247">Dieser Name hat in der Regel die Dateinamenerweiterung exe.</span><span class="sxs-lookup"><span data-stu-id="b6f96-247">This name usually has the .exe file name extension.</span></span>

        -   <span data-ttu-id="b6f96-248">**Produktversion**: die Produktversionsnummer der exe-Datei der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="b6f96-248">**Product version**: The product version number of the .exe file of the application.</span></span> <span data-ttu-id="b6f96-249">Mit dieser Eigenschaft können Sie in Verbindung mit der **Dateiversion**ermitteln, welche Anwendungen von der Vorlage für die Einstellungsposition abzielen.</span><span class="sxs-lookup"><span data-stu-id="b6f96-249">This property, in conjunction with the **File version**, helps determine which applications are targeted by the settings location template.</span></span> <span data-ttu-id="b6f96-250">Diese Eigenschaft akzeptiert eine Hauptversionsnummer.</span><span class="sxs-lookup"><span data-stu-id="b6f96-250">This property accepts a major version number.</span></span> <span data-ttu-id="b6f96-251">Wenn diese Eigenschaft leer ist, gilt die Vorlage für die Einstellungsposition für alle Versionen des Produkts.</span><span class="sxs-lookup"><span data-stu-id="b6f96-251">If this property is empty, the settings location template applies to all versions of the product.</span></span>

        -   <span data-ttu-id="b6f96-252">**Dateiversion**: die Dateiversionsnummer der exe-Datei der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="b6f96-252">**File version**: The file version number of the .exe file of the application.</span></span> <span data-ttu-id="b6f96-253">Mit dieser Eigenschaft können Sie in Verbindung mit der **Produktversion**ermitteln, welche Anwendungen von der Vorlage für die Einstellungsposition abzielen.</span><span class="sxs-lookup"><span data-stu-id="b6f96-253">This property, in conjunction with the **Product version**, helps determine which applications are targeted by the settings location template.</span></span> <span data-ttu-id="b6f96-254">Diese Eigenschaft akzeptiert eine Hauptversionsnummer.</span><span class="sxs-lookup"><span data-stu-id="b6f96-254">This property accepts a major version number.</span></span> <span data-ttu-id="b6f96-255">Wenn diese Eigenschaft leer ist, gilt die Vorlage für die Einstellungsposition für alle Versionen des Programms.</span><span class="sxs-lookup"><span data-stu-id="b6f96-255">If this property is empty, the settings location template applies to all versions of the program.</span></span>

        -   <span data-ttu-id="b6f96-256">**Name der Vorlagen Autorin** (optional): der Name der Vorlage für den Speicherort der Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="b6f96-256">**Template author name** (optional): The name of the settings location template author.</span></span>

        -   <span data-ttu-id="b6f96-257">**E-Mail-Vorlage für Vorlagenautor** (optional): die e-Mail-Adresse der Vorlage "Speicherort für Einstellungen".</span><span class="sxs-lookup"><span data-stu-id="b6f96-257">**Template author email** (optional): The email address of the settings location template author.</span></span>

    -   <span data-ttu-id="b6f96-258">Auf der Registerkarte " **Registrierung** " sind der **Schlüssel** und der **Bereich** der Registrierungsspeicherorte aufgeführt, die in der Vorlage "einstellungensort" enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="b6f96-258">The **Registry** tab lists the **Key** and **Scope** of the registry locations that are included in the settings location template.</span></span> <span data-ttu-id="b6f96-259">Bearbeiten Sie die Registrierungsspeicherorte mithilfe des Dropdownmenüs **Aufgaben** .</span><span class="sxs-lookup"><span data-stu-id="b6f96-259">Edit the registry locations by using the **Tasks** drop-down menu.</span></span> <span data-ttu-id="b6f96-260">Mit Aufgaben können Sie neue Schlüssel hinzufügen, den Namen oder den Bereich vorhandener Schlüssel bearbeiten, Schlüssel löschen und die Registrierung durchsuchen, in der sich die Schlüssel befinden.</span><span class="sxs-lookup"><span data-stu-id="b6f96-260">Tasks enable you to add new keys, edit the name or scope of existing keys, delete keys, and browse the registry where the keys are located.</span></span> <span data-ttu-id="b6f96-261">Verwenden Sie den Bereich **alle Einstellungen** , um alle Registrierungseinstellungen unter dem angegebenen Schlüssel einzubeziehen.</span><span class="sxs-lookup"><span data-stu-id="b6f96-261">Use the **All Settings** scope to include all the registry settings under the specified key.</span></span> <span data-ttu-id="b6f96-262">Verwenden Sie **alle Einstellungen und Unterschlüssel** , um alle Registrierungseinstellungen unter den angegebenen Tasten, Unterschlüsseln und Unterschlüssel Einstellungen einzubeziehen.</span><span class="sxs-lookup"><span data-stu-id="b6f96-262">Use the **All Settings and Subkeys** to include all the registry settings under the specified key, subkeys, and subkey settings.</span></span>

    -   <span data-ttu-id="b6f96-263">Auf der Registerkarte " **Dateien** " werden der Dateipfad und die Dateimaske der Dateispeicherorte aufgeführt, die in der Vorlage für die Einstellungsposition enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="b6f96-263">The **Files** tab lists the file path and file mask of the file locations that are included in the settings location template.</span></span> <span data-ttu-id="b6f96-264">Bearbeiten Sie die Dateispeicherorte mithilfe des Dropdownmenüs **Aufgaben** .</span><span class="sxs-lookup"><span data-stu-id="b6f96-264">Edit the file locations by use of the **Tasks** drop-down menu.</span></span> <span data-ttu-id="b6f96-265">Mit Aufgaben für Dateispeicherorte können Sie neue Dateien oder Ordnerspeicherorte hinzufügen, den Bereich vorhandener Dateien oder Ordner bearbeiten, Dateien oder Ordner löschen und den ausgewählten Speicherort in Windows-Explorer öffnen.</span><span class="sxs-lookup"><span data-stu-id="b6f96-265">Tasks for file locations enable you to add new files or folder locations, edit the scope of existing files or folders, delete files or folders, and open the selected location in Windows Explorer.</span></span> <span data-ttu-id="b6f96-266">Lassen Sie die Dateimaske leer, um alle Dateien in den angegebenen Ordner einzubeziehen.</span><span class="sxs-lookup"><span data-stu-id="b6f96-266">Leave the file mask empty to include all files in the specified folder.</span></span>

8.  <span data-ttu-id="b6f96-267">Klicken Sie auf **Erstellen**und dann auf **Speichern** , um die Vorlage für die Einstellungsposition auf dem Computer zu speichern.</span><span class="sxs-lookup"><span data-stu-id="b6f96-267">Click **Create**, and then click **Save** to save the settings location template on the computer.</span></span>

9.  <span data-ttu-id="b6f96-268">Klicken Sie auf **Schließen** , um den Assistenten für Einstellungs Vorlagen zu schließen.</span><span class="sxs-lookup"><span data-stu-id="b6f96-268">Click **Close** to close the Settings Template Wizard.</span></span> <span data-ttu-id="b6f96-269">Beenden Sie die UE-V-Generator Anwendung.</span><span class="sxs-lookup"><span data-stu-id="b6f96-269">Exit the UE-V Generator application.</span></span>

    <span data-ttu-id="b6f96-270">Nachdem Sie die Vorlage für die Einstellungsposition für eine Anwendung erstellt haben, sollten Sie die Vorlage testen.</span><span class="sxs-lookup"><span data-stu-id="b6f96-270">After you have created the settings location template for an application, you should test the template.</span></span> <span data-ttu-id="b6f96-271">Stellen Sie die Vorlage in einer Lab-Umgebung bereit, bevor Sie Sie in der Produktion im Unternehmen einsetzen.</span><span class="sxs-lookup"><span data-stu-id="b6f96-271">Deploy the template in a lab environment before you put it into production in the enterprise.</span></span>

<span data-ttu-id="b6f96-272">[Anwendungsvorlagen Schema Referenz für UE-v](https://technet.microsoft.com/library/dn763947.aspx) beschreibt die XML-Struktur der Standort Vorlage für UE-v-Einstellungen und bietet Anleitungen für die Bearbeitung dieser Dateien.</span><span class="sxs-lookup"><span data-stu-id="b6f96-272">[Application Template Schema Reference for UE-V](https://technet.microsoft.com/library/dn763947.aspx) details the XML structure of the UE-V settings location template and provides guidance for editing these files.</span></span>

## <a href="" id="deploycustomtemplates"></a><span data-ttu-id="b6f96-273">Bereitstellen der Speicherort Vorlagen für benutzerdefinierte Einstellungen</span><span class="sxs-lookup"><span data-stu-id="b6f96-273">Deploy the Custom Settings Location Templates</span></span>


<span data-ttu-id="b6f96-274">Nachdem Sie eine Vorlage für die Einstellungsposition mit dem UE-V-Generator erstellt haben, sollten Sie Sie testen, um sicherzustellen, dass die Anwendungseinstellungen ordnungsgemäß synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="b6f96-274">After you create a settings location template with the UE-V Generator, you should test it to ensure that the application settings are synchronized correctly.</span></span> <span data-ttu-id="b6f96-275">Anschließend können Sie die Vorlage für die Einstellungsposition sicher auf Computern im Unternehmen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="b6f96-275">You can then safely deploy the settings location template to computers in the enterprise.</span></span>

<span data-ttu-id="b6f96-276">Einstellungen Speicherort Vorlagen können mithilfe einer der folgenden Methoden bereitgestellt werden:</span><span class="sxs-lookup"><span data-stu-id="b6f96-276">Settings location templates can be deployed by using one of these methods:</span></span>

-   <span data-ttu-id="b6f96-277">Ein ESD-System (Enterprise Software Distribution) wie System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="b6f96-277">An enterprise software distribution (ESD) system such as System Center Configuration Manager</span></span>

-   <span data-ttu-id="b6f96-278">Gruppenrichtlinienvoreinstellungen</span><span class="sxs-lookup"><span data-stu-id="b6f96-278">Group Policy preferences</span></span>

-   <span data-ttu-id="b6f96-279">Ein UE-V-Einstellungs Vorlagenkatalog</span><span class="sxs-lookup"><span data-stu-id="b6f96-279">A UE-V settings template catalog</span></span>

<span data-ttu-id="b6f96-280">Vorlagen, die mithilfe eines ESD-Systems oder von Gruppenrichtlinienobjekten bereitgestellt werden, müssen über die UE-V-Windows-Verwaltungsinstrumentation (WMI) oder Windows PowerShell registriert werden.</span><span class="sxs-lookup"><span data-stu-id="b6f96-280">Templates that are deployed by using an ESD system or Group Policy Objects must be registered through UE-V Windows Management Instrumentation (WMI) or Windows PowerShell.</span></span> <span data-ttu-id="b6f96-281">Vorlagen, die im Katalogspeicherort für Einstellungs Vorlagen gespeichert sind, werden vom UE-V-Agent automatisch registriert.</span><span class="sxs-lookup"><span data-stu-id="b6f96-281">Templates that are stored in the settings template catalog location are automatically registered by the UE-V Agent.</span></span>

**<span data-ttu-id="b6f96-282">So verwenden Sie den Katalogpfad der Einstellungs Vorlage zum Bereitstellen von UE-V-Einstellungen Speicherort Vorlagen</span><span class="sxs-lookup"><span data-stu-id="b6f96-282">To use the settings template catalog path to deploy UE-V settings location templates</span></span>**

1.  <span data-ttu-id="b6f96-283">Navigieren Sie zu dem Netzwerkfreigabeordner, der als Vorlagenkatalog für Einstellungen definiert ist.</span><span class="sxs-lookup"><span data-stu-id="b6f96-283">Browse to the network share folder that is defined as the settings template catalog.</span></span>

2.  <span data-ttu-id="b6f96-284">Hinzufügen, entfernen oder Aktualisieren von Einstellungen für Standort Vorlagen im Einstellungs Vorlagenkatalog, um die für UE-v-Computer gewünschte UE-v-Agent-Vorlagenkonfiguration wiederzugeben.</span><span class="sxs-lookup"><span data-stu-id="b6f96-284">Add, remove, or update settings location templates in the settings template catalog to reflect the UE-V Agent template configuration that you want for UE-V computers.</span></span>

    <span data-ttu-id="b6f96-285">**Hinweis**  Vorlagen auf Computern werden täglich aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="b6f96-285">**Note** Templates on computers are updated daily.</span></span> <span data-ttu-id="b6f96-286">Das Update basiert auf Änderungen am Vorlagenkatalog für Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="b6f96-286">The update is based on changes to the settings template catalog.</span></span>

     

3.  <span data-ttu-id="b6f96-287">Wenn Sie Vorlagen auf einem Computer, auf dem der UE-V-Agent ausgeführt wird, manuell aktualisieren möchten, öffnen Sie eine Eingabeaufforderung mit erhöhten Rechten, und navigieren Sie zu \*\*% Program Files%\\Microsoft User Experience Virtualization \ \ Agent \ \ &lt; x86 oder x64 &gt; \*\*, und führen Sie dann **ApplySettingsTemplateCatalog.exe**aus.</span><span class="sxs-lookup"><span data-stu-id="b6f96-287">To manually update templates on a computer that runs the UE-V Agent, open an elevated command prompt, and browse to **%Program Files%\\Microsoft User Experience Virtualization \\ Agent \\ &lt;x86 or x64 &gt;**, and then run **ApplySettingsTemplateCatalog.exe**.</span></span>

    <span data-ttu-id="b6f96-288">**Hinweis**  Dieses Programm wird automatisch während des Computerstarts und täglich bei 3:30 A. M ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b6f96-288">**Note** This program runs automatically during computer startup and daily at 3:30 A. M.</span></span> <span data-ttu-id="b6f96-289">, um alle neuen Vorlagen zu sammeln, die dem Katalog kürzlich hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="b6f96-289">to gather any new templates that were recently added to the catalog.</span></span>

     






## <span data-ttu-id="b6f96-290">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="b6f96-290">Related topics</span></span>


[<span data-ttu-id="b6f96-291">Vorbereiten einer UE-V 2. x-Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="b6f96-291">Prepare a UE-V 2.x Deployment</span></span>](prepare-a-ue-v-2x-deployment-new-uevv2.md)

[<span data-ttu-id="b6f96-292">Bereitstellen der erforderlichen Features für UE-V 2.x</span><span class="sxs-lookup"><span data-stu-id="b6f96-292">Deploy Required Features for UE-V 2.x</span></span>](deploy-required-features-for-ue-v-2x-new-uevv2.md)

 

 





