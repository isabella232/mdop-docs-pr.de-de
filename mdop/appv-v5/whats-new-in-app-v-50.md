---
title: Neuigkeiten in App-V 5.0
description: Neuigkeiten in App-V 5.0
author: dansimp
ms.assetid: 79ff6e02-e926-4803-87d8-248a6b28099d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: dabe264f033bd5c9897f07d931f799a42e6b72e9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804814"
---
# <span data-ttu-id="ad168-103">Neuigkeiten in App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="ad168-103">What's New in App-V 5.0</span></span>


<span data-ttu-id="ad168-104">Dieser Abschnitt richtet sich an Benutzer, die bereits mit App-v vertraut sind und wissen möchten, was sich in App-v 5,0 geändert hat, wenn Sie noch nicht mit App-v vertraut sind, sollten Sie zunächst die [Planung für App-v 5,0](planning-for-app-v-50-rc.md)lesen.</span><span class="sxs-lookup"><span data-stu-id="ad168-104">This section is for users who are already familiar with App-V and want to know what has changed in App-V 5.0 If you are not already familiar with App-V, you should start by reading [Planning for App-V 5.0](planning-for-app-v-50-rc.md).</span></span>

## <span data-ttu-id="ad168-105">Änderungen der Standard Funktionalität</span><span class="sxs-lookup"><span data-stu-id="ad168-105">Changes in Standard Functionality</span></span>


<span data-ttu-id="ad168-106">Die folgenden Abschnitte enthalten Informationen zu den Änderungen in den Standardfunktionen für App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="ad168-106">The following sections contain information about the changes in standard functionality for App-V 5.0.</span></span>

### <span data-ttu-id="ad168-107">Änderungen an unterstützten Betriebssystemen</span><span class="sxs-lookup"><span data-stu-id="ad168-107">Changes to Supported Operating Systems</span></span>

<span data-ttu-id="ad168-108">Weitere Informationen finden Sie unter [unterstützte App-V 5,0-Konfigurationen](app-v-50-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="ad168-108">For more information, see [App-V 5.0 Supported Configurations](app-v-50-supported-configurations.md).</span></span>

## <span data-ttu-id="ad168-109">Änderungen am Sequencer</span><span class="sxs-lookup"><span data-stu-id="ad168-109">Changes to the sequencer</span></span>


<span data-ttu-id="ad168-110">Die folgenden Abschnitte enthalten Informationen zu den Änderungen im App-V 5,0-Sequenzer.</span><span class="sxs-lookup"><span data-stu-id="ad168-110">The following sections contain information about the changes in the App-V 5.0 sequencer.</span></span>

### <span data-ttu-id="ad168-111">Spezifische Änderung des Sequencers</span><span class="sxs-lookup"><span data-stu-id="ad168-111">Specific change to the sequencer</span></span>

<span data-ttu-id="ad168-112">In der folgenden Tabelle werden Informationen zu den Änderungen mit dem App-V 5,0-Sequenzer angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ad168-112">The following table displays information about what has changed with the App-V 5.0 sequencer</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ad168-113">Sequencer-Feature</span><span class="sxs-lookup"><span data-stu-id="ad168-113">Sequencer Feature</span></span></th>
<th align="left"><span data-ttu-id="ad168-114">App-V 5,0-Sequenzer-Funktionalität</span><span class="sxs-lookup"><span data-stu-id="ad168-114">App-V 5.0 Sequencer Functionality</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ad168-115">Neustart-Verarbeitung</span><span class="sxs-lookup"><span data-stu-id="ad168-115">Reboot processing</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad168-116">Wenn eine Anwendung nach einem Neustart auffordert, sollten Sie der Anwendung den Neustart des Computers mit dem Sequencer gestatten.</span><span class="sxs-lookup"><span data-stu-id="ad168-116">When an application prompts for a restart, you should allow the application to restart the computer running the sequencer.</span></span> <span data-ttu-id="ad168-117">Der Computer, auf dem der Sequencer ausgeführt wird, wird neu gestartet, und der Sequencer wird im Überwachungsmodus fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="ad168-117">The computer running the sequencer will restart and the sequencer will resume in monitoring mode.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ad168-118">Angeben des virtuellen Anwendungsverzeichnisses</span><span class="sxs-lookup"><span data-stu-id="ad168-118">Specifying the virtual application directory</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad168-119">Das virtuelle Anwendungsverzeichnis ist ein obligatorischer Parameter.</span><span class="sxs-lookup"><span data-stu-id="ad168-119">Virtual Application Directory is a mandatory parameter.</span></span> <span data-ttu-id="ad168-120">Die besten Ergebnisse erzielen Sie, wenn Sie dem Installationsverzeichnis des Anwendungs Installationsprogramms entsprechen.</span><span class="sxs-lookup"><span data-stu-id="ad168-120">For best results, it should match the installation directory of the application installer.</span></span> <span data-ttu-id="ad168-121">Dies führt zu einer optimierten Leistung und Anwendungskompatibilität.</span><span class="sxs-lookup"><span data-stu-id="ad168-121">This results in more optimal performance and application compatibility.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ad168-122">Bearbeiten von Verknüpfungen/Freihandelsabkommen</span><span class="sxs-lookup"><span data-stu-id="ad168-122">Editing shortcuts/FTAs</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad168-123">Die Seite "Verknüpfungen/FTA" befindet sich auf der Seite " <strong> Erweiterte </strong> Bearbeitung" nach Abschluss des Sequenz-Assistenten.</span><span class="sxs-lookup"><span data-stu-id="ad168-123">The Shortcuts/FTA page is on the <strong>Advanced</strong> editing page after the sequencing wizard has completed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ad168-124">Registerkarte „Verlauf ändern“</span><span class="sxs-lookup"><span data-stu-id="ad168-124">Change History Tab</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad168-125">Die Registerkarte Änderungsverlauf wurde für App-V 5,0 entfernt.</span><span class="sxs-lookup"><span data-stu-id="ad168-125">The Change History tab has been removed for App-V 5.0.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ad168-126">Registerkarte „OSD“</span><span class="sxs-lookup"><span data-stu-id="ad168-126">OSD Tab</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad168-127">Die Registerkarte "OSD" wurde für App-V 5,0 entfernt.</span><span class="sxs-lookup"><span data-stu-id="ad168-127">The OSD tab has been removed for App-V 5.0.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ad168-128">Registerkarte „Virtuelle Dienste“</span><span class="sxs-lookup"><span data-stu-id="ad168-128">Virtual Services Tab</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad168-129">Die Registerkarte Virtuelle Dienste wurde für App-V 5,0 entfernt.</span><span class="sxs-lookup"><span data-stu-id="ad168-129">The virtual services tab has been removed for App-V 5.0.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ad168-130">Registerkarte "Dateien/virtuelles Datei System"</span><span class="sxs-lookup"><span data-stu-id="ad168-130">Files/Virtual File System Tab</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad168-131">Diese Registerkarten werden kombiniert, und Sie können Paketdateien ändern.</span><span class="sxs-lookup"><span data-stu-id="ad168-131">These tabs are combined and allow you to modify package files.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ad168-132">Registerkarte „Bereitstellung“</span><span class="sxs-lookup"><span data-stu-id="ad168-132">Deployment Tab</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad168-133">Es gibt keine weiteren Optionen zum Konfigurieren der Server-URL in den Paketen.</span><span class="sxs-lookup"><span data-stu-id="ad168-133">There are no longer options to configure the server URL in the packages.</span></span> <span data-ttu-id="ad168-134">Sie sollten dies jetzt mithilfe der Bereitstellungskonfiguration oder des Verwaltungsservers konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="ad168-134">You should configure this now using deployment configuration, or the management server.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ad168-135">Paket Konverter-Tool</span><span class="sxs-lookup"><span data-stu-id="ad168-135">Package Converter Tool</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad168-136">Sie können jetzt mithilfe von PowerShell Pakete konvertieren, die in früheren Versionen erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="ad168-136">You can now use PowerShell to convert packages created in previous versions.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ad168-137">Add-on/Middleware</span><span class="sxs-lookup"><span data-stu-id="ad168-137">Add-on/Middleware</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad168-138">Sie können übergeordnete Pakete erweitern, wenn Sie eine Add-on-oder Middleware-Anwendung sequenzieren.</span><span class="sxs-lookup"><span data-stu-id="ad168-138">You can expand parent packages when you are sequencing an Add-On or Middleware application.</span></span> <span data-ttu-id="ad168-139">Add-ons und Middleware-Pakete müssen über Verbindungsgruppen in App-V 5,0 verbunden sein.</span><span class="sxs-lookup"><span data-stu-id="ad168-139">Add-ons and Middleware packages must be connected using connection groups in App-V 5.0.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ad168-140">Ausgabe von Dateien</span><span class="sxs-lookup"><span data-stu-id="ad168-140">Files output</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad168-141">Die folgenden Dateien werden mit App-V 5,0, Windows Installer (MSI), AppV, Bereitstellungskonfiguration, Benutzerkonfiguration und dem Report.XML erstellt.</span><span class="sxs-lookup"><span data-stu-id="ad168-141">The following files are created with App-V 5.0, Windows Installer (.msi), .appv, deployment configuration, user configuration, and the Report.XML.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ad168-142">Komprimierungs-/Sicherheitsbeschreibungen/MSI-Pakete</span><span class="sxs-lookup"><span data-stu-id="ad168-142">Compression/Security descriptors/MSI packages</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad168-143">Die Komprimierung und das Erstellen einer Windows Installer-Datei (MSI) sind für alle Pakete automatisch, und Sie können Sicherheitsbeschreibungen nicht mehr außer Kraft setzen.</span><span class="sxs-lookup"><span data-stu-id="ad168-143">Compression and the creation of a Windows Installer (.msi) file are automatic for all packages and you can no longer override security descriptors.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ad168-144">Extras/Optionen</span><span class="sxs-lookup"><span data-stu-id="ad168-144">Tools / Options</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad168-145">Das Diagnosefenster wurde entfernt sowie verschiedene andere Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="ad168-145">The Diagnostics window has been removed as well as several other settings.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ad168-146">Installationslaufwerk</span><span class="sxs-lookup"><span data-stu-id="ad168-146">Installation Drive</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad168-147">Wenn Sie eine Anwendung installieren, ist kein Installationslaufwerk mehr erforderlich.</span><span class="sxs-lookup"><span data-stu-id="ad168-147">An installation drive is no longer required when you install an application.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ad168-148">OOS-Streaming</span><span class="sxs-lookup"><span data-stu-id="ad168-148">OOS Streaming</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad168-149">Wenn keine Datenstromoptimierung durchgeführt wird, sind Pakete Datenstromfehler Haft, wenn Sie von Computern angefordert werden, auf denen der App-V 5,0-Client ausgeführt wird, bis Sie gestartet werden können.</span><span class="sxs-lookup"><span data-stu-id="ad168-149">If no stream optimization is performed, packages are stream faulted when they are requested by computers running the App-V 5.0 client until they can launch.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ad168-150">F: &lt; /p&gt;</span><span class="sxs-lookup"><span data-stu-id="ad168-150">Q:&lt;/p&gt;</span></span></td>
<td align="left"><p><span data-ttu-id="ad168-151">App-V 5,0 verwendet das systemeigene Dateisystem und erfordert keine q: mehr</span><span class="sxs-lookup"><span data-stu-id="ad168-151">App-V 5.0 uses the native file system and no longer requires a Q:.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="ad168-152">Fehlererkennung bei der Sequenzierung</span><span class="sxs-lookup"><span data-stu-id="ad168-152">Sequencing error detection</span></span>


<span data-ttu-id="ad168-153">Der App-V 5,0-Sequenzer kann häufige Sequenzierungs Probleme während der Sequenzierung erkennen.</span><span class="sxs-lookup"><span data-stu-id="ad168-153">The App-V 5.0 sequencer can detect common sequencing issues during sequencing.</span></span> <span data-ttu-id="ad168-154">Auf der Seite " **Installationsbericht** " am Ende des Sequenz-Assistenten werden in Abhängigkeit vom Schweregrad des Problems diagnostische Nachrichten angezeigt, die in **Fehler**, **Warnungen**und **Informationen** kategorisiert sind.</span><span class="sxs-lookup"><span data-stu-id="ad168-154">The **Installation Report** page at the end of the sequencing wizard displays diagnostic messages categorized into **Errors**, **Warnings**, and **Info** depending on the severity of the issue.</span></span>

<span data-ttu-id="ad168-155">Wenn Sie ausführlichere Informationen zu einem Ereignis anzeigen möchten, doppelklicken Sie auf das Element, das Sie im Bericht überprüfen möchten.</span><span class="sxs-lookup"><span data-stu-id="ad168-155">To display more detailed information about an event, double-click the item you want to review in the report.</span></span> <span data-ttu-id="ad168-156">Die Sequenzierungs Probleme sowie Vorschläge zur Behebung der Probleme werden angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ad168-156">The sequencing issues, as well as suggestions about how to resolve the issues are displayed.</span></span> <span data-ttu-id="ad168-157">Wenn Sie mit dem Erstellen eines Pakets fertig sind, werden die Informationen aus dem Bericht zur Systemvorbereitung und dem Installationsbericht zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="ad168-157">Information from the system preparation report and the installation report are summarized when you have finished creating a package.</span></span> <span data-ttu-id="ad168-158">In der folgenden Liste werden die im Bericht verfügbaren Problemtypen angezeigt:</span><span class="sxs-lookup"><span data-stu-id="ad168-158">The following list displays the types of issues available in the report:</span></span>

-   <span data-ttu-id="ad168-159">Ausgeschlossene Dateien.</span><span class="sxs-lookup"><span data-stu-id="ad168-159">Excluded files.</span></span>

-   <span data-ttu-id="ad168-160">Treiberinformationen.</span><span class="sxs-lookup"><span data-stu-id="ad168-160">Driver information.</span></span>

-   <span data-ttu-id="ad168-161">Unterschiede bei com+-Systemen.</span><span class="sxs-lookup"><span data-stu-id="ad168-161">COM+ system differences.</span></span>

-   <span data-ttu-id="ad168-162">Nebeneinander (SxS)-Konflikte.</span><span class="sxs-lookup"><span data-stu-id="ad168-162">Side-by-side (SxS) conflicts.</span></span>

-   <span data-ttu-id="ad168-163">Shell-Erweiterungen.</span><span class="sxs-lookup"><span data-stu-id="ad168-163">Shell Extensions.</span></span>

-   <span data-ttu-id="ad168-164">Informationen zu nicht unterstützten Diensten.</span><span class="sxs-lookup"><span data-stu-id="ad168-164">Information about unsupported services.</span></span>

-   <span data-ttu-id="ad168-165">DCOM.</span><span class="sxs-lookup"><span data-stu-id="ad168-165">DCOM.</span></span>

## <span data-ttu-id="ad168-166">Verbindungsgruppen</span><span class="sxs-lookup"><span data-stu-id="ad168-166">Connection Groups</span></span>


<span data-ttu-id="ad168-167">Das App-v-Feature, das früher als " **Dynamic Suite Composition** " bezeichnet wird, wird nun in App-V 5,0 als **Verbindungsgruppen** bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="ad168-167">The App-V feature formerly known as **Dynamic Suite Composition** is now referred to as **Connection Groups** in App-V 5.0.</span></span> <span data-ttu-id="ad168-168">Weitere Informationen zum Verwenden von Verbindungsgruppen finden Sie unter [Verwalten von Verbindungsgruppen](managing-connection-groups.md).</span><span class="sxs-lookup"><span data-stu-id="ad168-168">For more information about using Connection Groups see [Managing Connection Groups](managing-connection-groups.md).</span></span>

## <span data-ttu-id="ad168-169">Lizenzierungs-und Dosierungs Funktionen</span><span class="sxs-lookup"><span data-stu-id="ad168-169">Licensing and Metering Functionality</span></span>


<span data-ttu-id="ad168-170">Die Anwendungs-und Lizenzierungs Funktionalität wurde in App-V 5,0 entfernt.</span><span class="sxs-lookup"><span data-stu-id="ad168-170">The application and licensing functionality has been removed in App-V 5.0.</span></span> <span data-ttu-id="ad168-171">Die tatsächlichen Lizenz Positionen in Ihrer Umgebung hängen von den spezifischen Softwaretitel Lizenzen und Nutzungsrechten ab, die durch die zugehörigen Lizenzbedingungen gewährt werden.</span><span class="sxs-lookup"><span data-stu-id="ad168-171">The actual license positions in your environment depend on the specific software title license and usage rights granted by the associated license terms.</span></span>

## <span data-ttu-id="ad168-172">Datei-und Anwendungs Cache</span><span class="sxs-lookup"><span data-stu-id="ad168-172">File and Application Cache</span></span>


<span data-ttu-id="ad168-173">In App-V 5,0 steht kein Datei-oder Anwendungscache zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="ad168-173">There is no file or application cache available with App-V 5.0.</span></span>






## <span data-ttu-id="ad168-174">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="ad168-174">Related topics</span></span>


[<span data-ttu-id="ad168-175">Informationen zu App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="ad168-175">About App-V 5.0</span></span>](about-app-v-50.md)

 

 





