---
title: Anwendungsveröffentlichung und Clientinteraktion
description: Anwendungsveröffentlichung und Clientinteraktion
author: dansimp
ms.assetid: c69a724a-85d1-4e2d-94a2-7ffe0b47d971
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: b6080a501a8fdd2a39876ff979aa7a2982c76bbb
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805951"
---
# <span data-ttu-id="14981-103">Anwendungsveröffentlichung und Clientinteraktion</span><span class="sxs-lookup"><span data-stu-id="14981-103">Application Publishing and Client Interaction</span></span>


<span data-ttu-id="14981-104">Dieser Artikel enthält technische Informationen zu allgemeinen App-V-Clientvorgängen und deren Integration in das lokale Betriebssystem.</span><span class="sxs-lookup"><span data-stu-id="14981-104">This article provides technical information about common App-V client operations and their integration with the local operating system.</span></span>

-   [<span data-ttu-id="14981-105">App-V-Paketdateien, die vom Sequencer erstellt wurden</span><span class="sxs-lookup"><span data-stu-id="14981-105">App-V package files created by the Sequencer</span></span>](#bkmk-appv-pkg-files-list)

-   [<span data-ttu-id="14981-106">Was befindet sich in der AppV-Datei?</span><span class="sxs-lookup"><span data-stu-id="14981-106">What’s in the appv file?</span></span>](#bkmk-appv-file-contents)

-   [<span data-ttu-id="14981-107">App-V-Client Datenspeicherorte</span><span class="sxs-lookup"><span data-stu-id="14981-107">App-V client data storage locations</span></span>](#bkmk-files-data-storage)

-   [<span data-ttu-id="14981-108">Paket Registrierung</span><span class="sxs-lookup"><span data-stu-id="14981-108">Package registry</span></span>](#bkmk-pkg-registry)

-   [<span data-ttu-id="14981-109">App-V-Paketspeicher Verhalten</span><span class="sxs-lookup"><span data-stu-id="14981-109">App-V package store behavior</span></span>](#bkmk-pkg-store-behavior)

-   [<span data-ttu-id="14981-110">Roaming-Registrierung und Daten</span><span class="sxs-lookup"><span data-stu-id="14981-110">Roaming registry and data</span></span>](#bkmk-roaming-reg-data)

-   [<span data-ttu-id="14981-111">App-V Client Application Lifecycle Management</span><span class="sxs-lookup"><span data-stu-id="14981-111">App-V client application lifecycle management</span></span>](#bkmk-clt-app-lifecycle)

-   [<span data-ttu-id="14981-112">Integration von App-V-Paketen</span><span class="sxs-lookup"><span data-stu-id="14981-112">Integration of App-V packages</span></span>](#bkmk-integr-appv-pkgs)

-   [<span data-ttu-id="14981-113">Verarbeitung dynamischer Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="14981-113">Dynamic configuration processing</span></span>](#bkmk-dynamic-config)

-   [<span data-ttu-id="14981-114">Nebeneinander angeordnete Assemblys</span><span class="sxs-lookup"><span data-stu-id="14981-114">Side-by-side assemblies</span></span>](#bkmk-sidebyside-assemblies)

-   [<span data-ttu-id="14981-115">Client Protokollierung</span><span class="sxs-lookup"><span data-stu-id="14981-115">Client logging</span></span>](#bkmk-client-logging)

<span data-ttu-id="14981-116">Weitere Referenzinformationen finden Sie unter [Dokumentation der Microsoft Application Virtualization (App-V)-Download Seite](https://www.microsoft.com/download/details.aspx?id=27760).</span><span class="sxs-lookup"><span data-stu-id="14981-116">For additional reference information, see [Microsoft Application Virtualization (App-V) Documentation Resources Download Page](https://www.microsoft.com/download/details.aspx?id=27760).</span></span>

## <a href="" id="bkmk-appv-pkg-files-list"></a><span data-ttu-id="14981-117">App-V-Paketdateien, die vom Sequencer erstellt wurden</span><span class="sxs-lookup"><span data-stu-id="14981-117">App-V package files created by the Sequencer</span></span>


<span data-ttu-id="14981-118">Der Sequencer erstellt App-V-Pakete und erstellt eine virtualisierte Anwendung.</span><span class="sxs-lookup"><span data-stu-id="14981-118">The Sequencer creates App-V packages and produces a virtualized application.</span></span> <span data-ttu-id="14981-119">Der Sequenzierungsprozess erstellt die folgenden Dateien:</span><span class="sxs-lookup"><span data-stu-id="14981-119">The sequencing process creates the following files:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="14981-120">Datei</span><span class="sxs-lookup"><span data-stu-id="14981-120">File</span></span></th>
<th align="left"><span data-ttu-id="14981-121">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="14981-121">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="14981-122">. AppV</span><span class="sxs-lookup"><span data-stu-id="14981-122">.appv</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="14981-123">Die primäre Paketdatei, die die erfassten Ressourcen und Zustandsinformationen aus dem Sequenz Prozess enthält.</span><span class="sxs-lookup"><span data-stu-id="14981-123">The primary package file, which contains the captured assets and state information from the sequencing process.</span></span></p></li>
<li><p><span data-ttu-id="14981-124">Architektur der Paketdatei, Veröffentlichungsinformationen und Registrierung in einem Token-Formular, das bei der Zustellung erneut auf einen Computer und einen bestimmten Benutzer angewendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="14981-124">Architecture of the package file, publishing information, and registry in a tokenized form that can be reapplied to a machine and to a specific user upon delivery.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="14981-125">. MSI</span><span class="sxs-lookup"><span data-stu-id="14981-125">.MSI</span></span></p></td>
<td align="left"><p><span data-ttu-id="14981-126">Ausführbarer Bereitstellungs Wrapper, mit dem Sie AppV-Dateien manuell oder mithilfe einer Bereitstellungsplattform eines Drittanbieters bereitstellen können.</span><span class="sxs-lookup"><span data-stu-id="14981-126">Executable deployment wrapper that you can use to deploy .appv files manually or by using a third-party deployment platform.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="14981-127">_DeploymentConfig.XML</span><span class="sxs-lookup"><span data-stu-id="14981-127">_DeploymentConfig.XML</span></span></p></td>
<td align="left"><p><span data-ttu-id="14981-128">Datei, die verwendet wird, um die Standard Veröffentlichungs Parameter für alle Anwendungen in einem Paket anzupassen, das für alle Benutzer auf einem Computer, auf dem der App-V-Client ausgeführt wird, Global bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="14981-128">File used to customize the default publishing parameters for all applications in a package that is deployed globally to all users on a computer that is running the App-V client.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="14981-129">_UserConfig.XML</span><span class="sxs-lookup"><span data-stu-id="14981-129">_UserConfig.XML</span></span></p></td>
<td align="left"><p><span data-ttu-id="14981-130">Datei, die verwendet wird, um die Veröffentlichungs Parameter für alle Anwendungen in einem Paket anzupassen, das für einen bestimmten Benutzer auf einem Computer bereitgestellt wird, auf dem der App-V-Client ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="14981-130">File used to customize the publishing parameters for all applications in a package that is a deployed to a specific user on a computer that is running the App-V client.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="14981-131">Report.xml</span><span class="sxs-lookup"><span data-stu-id="14981-131">Report.xml</span></span></p></td>
<td align="left"><p><span data-ttu-id="14981-132">Zusammenfassung der Nachrichten, die sich aus dem Sequenz Prozess ergeben, einschließlich weggelassener Treiber, Dateien und Registrierungsspeicherorte.</span><span class="sxs-lookup"><span data-stu-id="14981-132">Summary of messages resulting from the sequencing process, including omitted drivers, files, and registry locations.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="14981-133">. CAB</span><span class="sxs-lookup"><span data-stu-id="14981-133">.CAB</span></span></p></td>
<td align="left"><p><em><span data-ttu-id="14981-134">Optional: </em> Paket Beschleunigerdatei, die zum automatischen Neuaufbau eines zuvor sequenzierten virtuellen Anwendungspakets verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="14981-134">Optional:</em> Package accelerator file used to automatically rebuild a previously sequenced virtual application package.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="14981-135">.appvt</span><span class="sxs-lookup"><span data-stu-id="14981-135">.appvt</span></span></p></td>
<td align="left"><p><em><span data-ttu-id="14981-136">Optional: </em> Sequencer-Vorlagendatei zur Beibehaltung häufig wieder verwendeter Sequenzer-Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="14981-136">Optional:</em> Sequencer template file used to retain commonly reused Sequencer settings.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="14981-137">Informationen zur Sequenzierung finden Sie unter [Application Virtualization 5,0-Sequenzierungs Handbuch](https://www.microsoft.com/download/details.aspx?id=27760).</span><span class="sxs-lookup"><span data-stu-id="14981-137">For information about sequencing, see [Application Virtualization 5.0 Sequencing Guide](https://www.microsoft.com/download/details.aspx?id=27760).</span></span>

## <a href="" id="bkmk-appv-file-contents"></a><span data-ttu-id="14981-138">Was befindet sich in der AppV-Datei?</span><span class="sxs-lookup"><span data-stu-id="14981-138">What’s in the appv file?</span></span>


<span data-ttu-id="14981-139">Bei der AppV-Datei handelt es sich um einen Container, in dem XML-und nicht-XML-Dateien zusammen in einer einzelnen Entität gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="14981-139">The appv file is a container that stores XML and non-XML files together in a single entity.</span></span> <span data-ttu-id="14981-140">Diese Datei wurde aus dem AppX-Format erstellt, das auf dem OPC-Standard (Open Packaging Conventions) basiert.</span><span class="sxs-lookup"><span data-stu-id="14981-140">This file is built from the AppX format, which is based on the Open Packaging Conventions (OPC) standard.</span></span>

<span data-ttu-id="14981-141">Wenn Sie den Inhalt der AppV-Datei anzeigen möchten, erstellen Sie eine Kopie des Pakets, und benennen Sie die kopierte Datei dann in eine ZIP-Erweiterung um.</span><span class="sxs-lookup"><span data-stu-id="14981-141">To view the appv file contents, make a copy of the package, and then rename the copied file to a ZIP extension.</span></span>

<span data-ttu-id="14981-142">Die AppV-Datei enthält die folgenden Ordner und Dateien, die beim Erstellen und Veröffentlichen einer virtuellen Anwendung verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="14981-142">The appv file contains the following folder and files, which are used when creating and publishing a virtual application:</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="14981-143">Name</span><span class="sxs-lookup"><span data-stu-id="14981-143">Name</span></span></th>
<th align="left"><span data-ttu-id="14981-144">Typ</span><span class="sxs-lookup"><span data-stu-id="14981-144">Type</span></span></th>
<th align="left"><span data-ttu-id="14981-145">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="14981-145">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="14981-146">Stamm</span><span class="sxs-lookup"><span data-stu-id="14981-146">Root</span></span></p></td>
<td align="left"><p><span data-ttu-id="14981-147">Dateiordner</span><span class="sxs-lookup"><span data-stu-id="14981-147">File folder</span></span></p></td>
<td align="left"><p><span data-ttu-id="14981-148">Verzeichnis, das das Dateisystem für die virtualisierte Anwendung enthält, das während der Sequenzierung erfasst wird.</span><span class="sxs-lookup"><span data-stu-id="14981-148">Directory that contains the file system for the virtualized application that is captured during sequencing.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="14981-149">[Content_Types]. XML</span><span class="sxs-lookup"><span data-stu-id="14981-149">[Content_Types].xml</span></span></p></td>
<td align="left"><p><span data-ttu-id="14981-150">XML-Datei</span><span class="sxs-lookup"><span data-stu-id="14981-150">XML File</span></span></p></td>
<td align="left"><p><span data-ttu-id="14981-151">Liste der Hauptinhalts Typen in der AppV-Datei (z. b. dll, exe, bin)</span><span class="sxs-lookup"><span data-stu-id="14981-151">List of the core content types in the appv file (e.g. DLL, EXE, BIN).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="14981-152">AppxBlockMap.xml</span><span class="sxs-lookup"><span data-stu-id="14981-152">AppxBlockMap.xml</span></span></p></td>
<td align="left"><p><span data-ttu-id="14981-153">XML-Datei</span><span class="sxs-lookup"><span data-stu-id="14981-153">XML File</span></span></p></td>
<td align="left"><p><span data-ttu-id="14981-154">Das Layout der AppV-Datei, in der Datei-, Block-und BlockMap-Elemente verwendet werden, die den Speicherort und die Überprüfung von Dateien im App-V-Paket ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="14981-154">Layout of the appv file, which uses File, Block, and BlockMap elements that enable location and validation of files in the App-V package.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="14981-155">AppxManifest.xml</span><span class="sxs-lookup"><span data-stu-id="14981-155">AppxManifest.xml</span></span></p></td>
<td align="left"><p><span data-ttu-id="14981-156">XML-Datei</span><span class="sxs-lookup"><span data-stu-id="14981-156">XML File</span></span></p></td>
<td align="left"><p><span data-ttu-id="14981-157">Metadaten für das Paket, das die erforderlichen Informationen zum Hinzufügen, veröffentlichen und Starten des Pakets enthält.</span><span class="sxs-lookup"><span data-stu-id="14981-157">Metadata for the package that contains the required information for adding, publishing, and launching the package.</span></span> <span data-ttu-id="14981-158">Enthält Erweiterungspunkte (Dateitypzuordnungen und Tastenkombinationen) sowie die Namen und GUIDs, die dem Paket zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="14981-158">Includes extension points (file type associations and shortcuts) and the names and GUIDs associated with the package.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="14981-159">FilesystemMetadata.xml</span><span class="sxs-lookup"><span data-stu-id="14981-159">FilesystemMetadata.xml</span></span></p></td>
<td align="left"><p><span data-ttu-id="14981-160">XML-Datei</span><span class="sxs-lookup"><span data-stu-id="14981-160">XML File</span></span></p></td>
<td align="left"><p><span data-ttu-id="14981-161">Liste der Dateien, die während der Sequenzierung erfasst werden, einschließlich Attribute (z. b. Verzeichnisse, Dateien, undurchsichtige Verzeichnisse, leere Verzeichnisse sowie lange und kurze Namen).</span><span class="sxs-lookup"><span data-stu-id="14981-161">List of the files captured during sequencing, including attributes (e.g., directories, files, opaque directories, empty directories,and long and short names).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="14981-162">PackageHistory.xml</span><span class="sxs-lookup"><span data-stu-id="14981-162">PackageHistory.xml</span></span></p></td>
<td align="left"><p><span data-ttu-id="14981-163">XML-Datei</span><span class="sxs-lookup"><span data-stu-id="14981-163">XML File</span></span></p></td>
<td align="left"><p><span data-ttu-id="14981-164">Informationen zum Sequenzcomputer (Betriebssystemversion, Internet Explorer-Version, .NET Framework-Version) und Prozess (Upgrade, Paketversion).</span><span class="sxs-lookup"><span data-stu-id="14981-164">Information about the sequencing computer (operating system version, Internet Explorer version, .Net Framework version) and process (upgrade, package version).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="14981-165">Registry. dat</span><span class="sxs-lookup"><span data-stu-id="14981-165">Registry.dat</span></span></p></td>
<td align="left"><p><span data-ttu-id="14981-166">DAT-Datei</span><span class="sxs-lookup"><span data-stu-id="14981-166">DAT File</span></span></p></td>
<td align="left"><p><span data-ttu-id="14981-167">Registrierungsschlüssel und Werte, die während des Sequenz Prozesses für das Paket erfasst wurden.</span><span class="sxs-lookup"><span data-stu-id="14981-167">Registry keys and values captured during the sequencing process for the package.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="14981-168">StreamMap.xml</span><span class="sxs-lookup"><span data-stu-id="14981-168">StreamMap.xml</span></span></p></td>
<td align="left"><p><span data-ttu-id="14981-169">XML-Datei</span><span class="sxs-lookup"><span data-stu-id="14981-169">XML File</span></span></p></td>
<td align="left"><p><span data-ttu-id="14981-170">Liste der Dateien für den Haupt-und Veröffentlichungs-Feature-Block.</span><span class="sxs-lookup"><span data-stu-id="14981-170">List of files for the primary and publishing feature block.</span></span> <span data-ttu-id="14981-171">Der Veröffentlichungsfeature-Block enthält die ICO-Dateien und die erforderlichen Teile von Dateien (exe und dll) für die Veröffentlichung des Pakets.</span><span class="sxs-lookup"><span data-stu-id="14981-171">The publishing feature block contains the ICO files and required portions of files (EXE and DLL) for publishing the package.</span></span> <span data-ttu-id="14981-172">Wenn vorhanden, enthält der primäre Feature-Block Dateien, die während des Sequenz Prozesses für Streaming optimiert wurden.</span><span class="sxs-lookup"><span data-stu-id="14981-172">When present, the primary feature block includes files that have been optimized for streaming during the sequencing process.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-files-data-storage"></a><span data-ttu-id="14981-173">App-V-Client Datenspeicherorte</span><span class="sxs-lookup"><span data-stu-id="14981-173">App-V client data storage locations</span></span>


<span data-ttu-id="14981-174">Der App-V-Client führt Aufgaben aus, um sicherzustellen, dass virtuelle Anwendungen ordnungsgemäß ausgeführt werden und wie lokal installierte Anwendungen funktionieren.</span><span class="sxs-lookup"><span data-stu-id="14981-174">The App-V client performs tasks to ensure that virtual applications run properly and work like locally installed applications.</span></span> <span data-ttu-id="14981-175">Der Vorgang zum Öffnen und Ausführen virtueller Anwendungen erfordert eine Zuordnung aus dem virtuellen Dateisystem und der Registrierung, um sicherzustellen, dass die Anwendung über die erforderlichen Komponenten einer herkömmlichen Anwendung verfügt, die von Benutzern erwartet wird.</span><span class="sxs-lookup"><span data-stu-id="14981-175">The process of opening and running virtual applications requires mapping from the virtual file system and registry to ensure the application has the required components of a traditional application expected by users.</span></span> <span data-ttu-id="14981-176">In diesem Abschnitt werden die Ressourcen beschrieben, die für die Ausführung virtueller Anwendungen erforderlich sind, und der Ort, an dem App-V die Ressourcen speichert.</span><span class="sxs-lookup"><span data-stu-id="14981-176">This section describes the assets that are required to run virtual applications and lists the location where App-V stores the assets.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="14981-177">Name</span><span class="sxs-lookup"><span data-stu-id="14981-177">Name</span></span></th>
<th align="left"><span data-ttu-id="14981-178">Pfad</span><span class="sxs-lookup"><span data-stu-id="14981-178">Location</span></span></th>
<th align="left"><span data-ttu-id="14981-179">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="14981-179">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="14981-180">Paketspeicher</span><span class="sxs-lookup"><span data-stu-id="14981-180">Package Store</span></span></p></td>
<td align="left"><p><span data-ttu-id="14981-181">%ProgramData%\App-V</span><span class="sxs-lookup"><span data-stu-id="14981-181">%ProgramData%\App-V</span></span></p></td>
<td align="left"><p><span data-ttu-id="14981-182">Standardspeicherort für nur-Lese-Paketdateien</span><span class="sxs-lookup"><span data-stu-id="14981-182">Default location for read only package files</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="14981-183">Computer Katalog</span><span class="sxs-lookup"><span data-stu-id="14981-183">Machine Catalog</span></span></p></td>
<td align="left"><p><span data-ttu-id="14981-184">%ProgramData%\Microsoft\AppV\Client\Catalog</span><span class="sxs-lookup"><span data-stu-id="14981-184">%ProgramData%\Microsoft\AppV\Client\Catalog</span></span></p></td>
<td align="left"><p><span data-ttu-id="14981-185">Enthält Konfigurationsdokumente pro Computer</span><span class="sxs-lookup"><span data-stu-id="14981-185">Contains per-machine configuration documents</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="14981-186">Benutzer Katalog</span><span class="sxs-lookup"><span data-stu-id="14981-186">User Catalog</span></span></p></td>
<td align="left"><p><span data-ttu-id="14981-187">%AppData%\Microsoft\AppV\Client\Catalog</span><span class="sxs-lookup"><span data-stu-id="14981-187">%AppData%\Microsoft\AppV\Client\Catalog</span></span></p></td>
<td align="left"><p><span data-ttu-id="14981-188">Enthält Konfigurationsdokumente pro Benutzer</span><span class="sxs-lookup"><span data-stu-id="14981-188">Contains per-user configuration documents</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="14981-189">Verknüpfungs Sicherungen</span><span class="sxs-lookup"><span data-stu-id="14981-189">Shortcut Backups</span></span></p></td>
<td align="left"><p><span data-ttu-id="14981-190">%AppData%\Microsoft\AppV\Client\Integration\ShortCutBackups</span><span class="sxs-lookup"><span data-stu-id="14981-190">%AppData%\Microsoft\AppV\Client\Integration\ShortCutBackups</span></span></p></td>
<td align="left"><p><span data-ttu-id="14981-191">Speichert vorherige Integrationspunkte, die die Wiederherstellung bei der Paket Veröffentlichung aktivieren</span><span class="sxs-lookup"><span data-stu-id="14981-191">Stores previous integration points that enable restore on package unpublish</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="14981-192">Roaming auf Write (Kuh) kopieren</span><span class="sxs-lookup"><span data-stu-id="14981-192">Copy on Write (COW) Roaming</span></span></p></td>
<td align="left"><p><span data-ttu-id="14981-193">%AppData%\Microsoft\AppV\Client\VFS</span><span class="sxs-lookup"><span data-stu-id="14981-193">%AppData%\Microsoft\AppV\Client\VFS</span></span></p></td>
<td align="left"><p><span data-ttu-id="14981-194">Beschreibbarer Roaming-Speicherort für Paketänderungen</span><span class="sxs-lookup"><span data-stu-id="14981-194">Writeable roaming location for package modification</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="14981-195">Auf Schreib (Kuh) lokal kopieren</span><span class="sxs-lookup"><span data-stu-id="14981-195">Copy on Write (COW) Local</span></span></p></td>
<td align="left"><p><span data-ttu-id="14981-196">%LocalAppData%\Microsoft\AppV\Client\VFS</span><span class="sxs-lookup"><span data-stu-id="14981-196">%LocalAppData%\Microsoft\AppV\Client\VFS</span></span></p></td>
<td align="left"><p><span data-ttu-id="14981-197">Beschreibbarer Speicherort für nicht-Roaming für Paketänderung</span><span class="sxs-lookup"><span data-stu-id="14981-197">Writeable non-roaming location for package modification</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="14981-198">Computerregistrierung</span><span class="sxs-lookup"><span data-stu-id="14981-198">Machine Registry</span></span></p></td>
<td align="left"><p><span data-ttu-id="14981-199">HKLM\Software\Microsoft\AppV</span><span class="sxs-lookup"><span data-stu-id="14981-199">HKLM\Software\Microsoft\AppV</span></span></p></td>
<td align="left"><p><span data-ttu-id="14981-200">Enthält Paket Zustandsinformationen, einschließlich VReg für Computer-oder Global veröffentlichte Pakete (Machine Hive)</span><span class="sxs-lookup"><span data-stu-id="14981-200">Contains package state information, including VReg for machine or globally published packages (Machine hive)</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="14981-201">Benutzerregistrierung</span><span class="sxs-lookup"><span data-stu-id="14981-201">User Registry</span></span></p></td>
<td align="left"><p><span data-ttu-id="14981-202">HKCU\Software\Microsoft\AppV</span><span class="sxs-lookup"><span data-stu-id="14981-202">HKCU\Software\Microsoft\AppV</span></span></p></td>
<td align="left"><p><span data-ttu-id="14981-203">Enthält Informationen zum Paket Zustand des Benutzers, einschließlich VReg</span><span class="sxs-lookup"><span data-stu-id="14981-203">Contains user package state information including VReg</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="14981-204">Benutzer Registrierungsklassen</span><span class="sxs-lookup"><span data-stu-id="14981-204">User Registry Classes</span></span></p></td>
<td align="left"><p><span data-ttu-id="14981-205">HKCU\Software\Classes\AppV</span><span class="sxs-lookup"><span data-stu-id="14981-205">HKCU\Software\Classes\AppV</span></span></p></td>
<td align="left"><p><span data-ttu-id="14981-206">Enthält zusätzliche Informationen zum Benutzerpaket Zustand</span><span class="sxs-lookup"><span data-stu-id="14981-206">Contains additional user package state information</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="14981-207">Weitere Details zur Tabelle finden Sie im Abschnitt unten und im gesamten Dokument.</span><span class="sxs-lookup"><span data-stu-id="14981-207">Additional details for the table are provided in the section below and throughout the document.</span></span>

### <span data-ttu-id="14981-208">Paketspeicher</span><span class="sxs-lookup"><span data-stu-id="14981-208">Package store</span></span>

<span data-ttu-id="14981-209">Der App-V-Client verwaltet die im Paketspeicher bereitgestellten Anwendungsressourcen.</span><span class="sxs-lookup"><span data-stu-id="14981-209">The App-V Client manages the applications assets mounted in the package store.</span></span> <span data-ttu-id="14981-210">Dieser Standardspeicherort ist `%ProgramData%\App-V` , Sie können ihn aber während oder nach dem Setup konfigurieren, indem Sie den `Set-AppVClientConfiguration` PowerShell-Befehl verwenden, der die lokale Registrierung ändert ( `PackageInstallationRoot` Wert unter dem `HKLM\Software\Microsoft\AppV\Client\Streaming` Schlüssel).</span><span class="sxs-lookup"><span data-stu-id="14981-210">This default storage location is `%ProgramData%\App-V`, but you can configure it during or after setup by using the `Set-AppVClientConfiguration` PowerShell command, which modifies the local registry (`PackageInstallationRoot` value under the `HKLM\Software\Microsoft\AppV\Client\Streaming` key).</span></span> <span data-ttu-id="14981-211">Der Paketspeicher muss sich im lokalen Pfad des Clientbetriebssystems befinden.</span><span class="sxs-lookup"><span data-stu-id="14981-211">The package store must be located at a local path on the client operating system.</span></span> <span data-ttu-id="14981-212">Die einzelnen Pakete werden im Paketspeicher in Unterverzeichnissen gespeichert, die für Paket-GUID und Versions-GUID benannt sind.</span><span class="sxs-lookup"><span data-stu-id="14981-212">The individual packages are stored in the package store in subdirectories named for the Package GUID and Version GUID.</span></span>

<span data-ttu-id="14981-213">Beispiel für einen Pfad zu einer bestimmten Anwendung:</span><span class="sxs-lookup"><span data-stu-id="14981-213">Example of a path to a specific application:</span></span>

``` syntax
C:\ProgramData\App-V\PackGUID\VersionGUID
```

<span data-ttu-id="14981-214">Informationen zum Ändern des Standardspeicherorts des Paketspeichers während der Installation finden Sie unter [Bereitstellen des App-V-Clients](how-to-deploy-the-app-v-client-gb18030.md).</span><span class="sxs-lookup"><span data-stu-id="14981-214">To change the default location of the package store during setup, see [How to Deploy the App-V Client](how-to-deploy-the-app-v-client-gb18030.md).</span></span>

### <span data-ttu-id="14981-215">Freigegebener Inhaltsspeicher</span><span class="sxs-lookup"><span data-stu-id="14981-215">Shared Content Store</span></span>

<span data-ttu-id="14981-216">Wenn der App-V-Client im freigegebenen Inhaltsspeicher Modus konfiguriert ist, werden keine Daten auf den Datenträger geschrieben, wenn ein Datenstromfehler auftritt, was bedeutet, dass für die Pakete nur minimaler lokaler Speicherplatz benötigt wird (Veröffentlichungsdaten).</span><span class="sxs-lookup"><span data-stu-id="14981-216">If the App-V Client is configured in Shared Content Store mode, no data is written to disk when a stream fault occurs, which means that the packages require minimal local disk space (publishing data).</span></span> <span data-ttu-id="14981-217">Die Verwendung von weniger Speicherplatz ist in VDI-Umgebungen, in denen der lokale Speicher limitiert werden kann, und das Streaming der Anwendungen von einem Hochleistungsnetzwerk Standort (wie einem SAN) vorzuziehen.</span><span class="sxs-lookup"><span data-stu-id="14981-217">The use of less disk space is highly desirable in VDI environments, where local storage can be limited, and streaming the applications from a high performance network location (such as a SAN) is preferable.</span></span> <span data-ttu-id="14981-218">Weitere Informationen zum Speichermodus für freigegebene Inhalte finden Sie unter <https://go.microsoft.com/fwlink/p/?LinkId=392750> .</span><span class="sxs-lookup"><span data-stu-id="14981-218">For more information on shared content store mode, see <https://go.microsoft.com/fwlink/p/?LinkId=392750>.</span></span>

<span data-ttu-id="14981-219">**Hinweis**  Der Computer und der Paketspeicher müssen sich auf einem lokalen Laufwerk befinden, auch wenn Sie für den App-V-Client freigegebene Inhaltsspeicher Konfigurationen verwenden.</span><span class="sxs-lookup"><span data-stu-id="14981-219">**Note** The machine and package store must be located on a local drive, even when you’re using Shared Content Store configurations for the App-V Client.</span></span>

 

### <span data-ttu-id="14981-220">Paket Kataloge</span><span class="sxs-lookup"><span data-stu-id="14981-220">Package catalogs</span></span>

<span data-ttu-id="14981-221">Der App-V-Client verwaltet die folgenden beiden dateibasierten Speicherorte:</span><span class="sxs-lookup"><span data-stu-id="14981-221">The App-V Client manages the following two file-based locations:</span></span>

-   **<span data-ttu-id="14981-222">Kataloge (Benutzer und Computer).</span><span class="sxs-lookup"><span data-stu-id="14981-222">Catalogs (user and machine).</span></span>**

-   <span data-ttu-id="14981-223">**Registrierungsspeicherorte** – hängt davon ab, wie das Paket für die Veröffentlichung vorgesehen ist.</span><span class="sxs-lookup"><span data-stu-id="14981-223">**Registry locations** - depends on how the package is targeted for publishing.</span></span> <span data-ttu-id="14981-224">Es gibt einen Katalog (Datenspeicher) für den Computer und einen Katalog für jeden einzelnen Benutzer.</span><span class="sxs-lookup"><span data-stu-id="14981-224">There is a Catalog (data store) for the computer, and a catalog for each individual user.</span></span> <span data-ttu-id="14981-225">Der Computer Katalog speichert globale Informationen, die für alle Benutzer oder einen beliebigen Benutzer gelten, und der Benutzer Katalog speichert Informationen, die für einen bestimmten Benutzer gelten.</span><span class="sxs-lookup"><span data-stu-id="14981-225">The Machine Catalog stores global information applicable to all users or any user, and the User Catalog stores information applicable to a specific user.</span></span> <span data-ttu-id="14981-226">Der Katalog ist eine Sammlung von dynamischen Konfigurationen und Manifestdateien; Es gibt diskrete Daten für Datei und Registrierung pro Paketversion.</span><span class="sxs-lookup"><span data-stu-id="14981-226">The Catalog is a collection of Dynamic Configurations and manifest files; there is discrete data for both file and registry per package version.</span></span> 

### <span data-ttu-id="14981-227">Computer Katalog</span><span class="sxs-lookup"><span data-stu-id="14981-227">Machine catalog</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="14981-228">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="14981-228">Description</span></span></p></td>
<td align="left"><p><span data-ttu-id="14981-229">Speichert Paket Dokumente, die für Benutzer auf dem Computer verfügbar sind, wenn Pakete hinzugefügt und veröffentlicht werden.</span><span class="sxs-lookup"><span data-stu-id="14981-229">Stores package documents that are available to users on the machine, when packages are added and published.</span></span> <span data-ttu-id="14981-230">Wenn ein Paket jedoch zum Zeitpunkt der Veröffentlichung "Global" ist, stehen die Integrationen allen Benutzern zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="14981-230">However, if a package is “global” at publishing time, the integrations are available to all users.</span></span></p>
<p><span data-ttu-id="14981-231">Wenn ein Paket nicht global ist, werden die Integrationen nur für bestimmte Benutzer veröffentlicht, es gibt jedoch weiterhin globale Ressourcen, die für jeden auf dem Clientcomputer geändert und sichtbar sind (beispielsweise befindet sich das Paketverzeichnis an einem freigegebenen Datenträgerspeicherort).</span><span class="sxs-lookup"><span data-stu-id="14981-231">If a package is non-global, the integrations are published only for specific users, but there are still global resources that are modified and visible to anyone on the client computer (e.g., the package directory is in a shared disk location).</span></span></p>
<p><span data-ttu-id="14981-232">Wenn ein Paket für einen Benutzer auf dem Computer (Global oder nicht global) zur Verfügung steht, wird das Manifest im Computer Katalog gespeichert.</span><span class="sxs-lookup"><span data-stu-id="14981-232">If a package is available to a user on the computer (global or non-global), the manifest is stored in the Machine Catalog.</span></span> <span data-ttu-id="14981-233">Wenn ein Paket Global veröffentlicht wird, gibt es eine dynamische Konfigurationsdatei, die im Computer Katalog gespeichert ist. Daher wird festgelegt, ob ein Paket Global ist, je nachdem, ob im Computer Katalog eine Richtliniendatei (UserDeploymentConfiguration-Datei) vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="14981-233">When a package is published globally, there is a Dynamic Configuration file, stored in the Machine Catalog; therefore, the determination of whether a package is global is defined according to whether there is a policy file (UserDeploymentConfiguration file) in the Machine Catalog.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="14981-234">Standardspeicherort</span><span class="sxs-lookup"><span data-stu-id="14981-234">Default storage location</span></span></p></td>
<td align="left"><p><code>%programdata%\Microsoft\AppV\Client\Catalog&lt;/code&gt;</p>
<p><span data-ttu-id="14981-235">Dieser Speicherort ist nicht mit dem Speicherort des Paketspeichers identisch.</span><span class="sxs-lookup"><span data-stu-id="14981-235">This location is not the same as the Package Store location.</span></span> <span data-ttu-id="14981-236">Der Paketspeicher ist die Goldene oder ursprüngliche Kopie der Paketdateien.</span><span class="sxs-lookup"><span data-stu-id="14981-236">The Package Store is the golden or pristine copy of the package files.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="14981-237">Dateien im Computer Katalog</span><span class="sxs-lookup"><span data-stu-id="14981-237">Files in the machine catalog</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="14981-238">Manifest.xml</span><span class="sxs-lookup"><span data-stu-id="14981-238">Manifest.xml</span></span></p></li>
<li><p><span data-ttu-id="14981-239">DeploymentConfiguration.xml</span><span class="sxs-lookup"><span data-stu-id="14981-239">DeploymentConfiguration.xml</span></span></p></li>
<li><p><span data-ttu-id="14981-240">UserManifest.xml (Global veröffentlichtes Paket)</span><span class="sxs-lookup"><span data-stu-id="14981-240">UserManifest.xml (Globally Published Package)</span></span></p></li>
<li><p><span data-ttu-id="14981-241">UserDeploymentConfiguration.xml (Global veröffentlichtes Paket)</span><span class="sxs-lookup"><span data-stu-id="14981-241">UserDeploymentConfiguration.xml (Globally Published Package)</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="14981-242">Zusätzlicher Standort des Computer Katalogs, der verwendet wird, wenn das Paket zu einer Verbindungsgruppe gehört</span><span class="sxs-lookup"><span data-stu-id="14981-242">Additional machine catalog location, used when the package is part of a connection group</span></span></p></td>
<td align="left"><p><span data-ttu-id="14981-243">Der folgende Standort ist zusätzlich zu dem oben genannten speziellen Paketspeicherort:</span><span class="sxs-lookup"><span data-stu-id="14981-243">The following location is in addition to the specific package location mentioned above:</span></span></p>
<p><code>%programdata%\Microsoft\AppV\Client\Catalog\PackageGroups\ConGroupGUID\ConGroupVerGUID</code></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="14981-244">Zusätzliche Dateien im Computer Katalog, wenn das Paket zu einer Verbindungsgruppe gehört</span><span class="sxs-lookup"><span data-stu-id="14981-244">Additional files in the machine catalog when the package is part of a connection group</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="14981-245">PackageGroupDescriptor.xml</span><span class="sxs-lookup"><span data-stu-id="14981-245">PackageGroupDescriptor.xml</span></span></p></li>
<li><p><span data-ttu-id="14981-246">UserPackageGroupDescriptor.xml (Globally published Connection Group)</span><span class="sxs-lookup"><span data-stu-id="14981-246">UserPackageGroupDescriptor.xml (globally published Connection Group)</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="14981-247">Benutzer Katalog</span><span class="sxs-lookup"><span data-stu-id="14981-247">User catalog</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="14981-248">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="14981-248">Description</span></span></p></td>
<td align="left"><p><span data-ttu-id="14981-249">Während des Veröffentlichungsprozesses erstellt.</span><span class="sxs-lookup"><span data-stu-id="14981-249">Created during the publishing process.</span></span> <span data-ttu-id="14981-250">Enthält Informationen, die für die Veröffentlichung des Pakets verwendet werden, und wird auch beim Start verwendet, um sicherzustellen, dass ein Paket für einen bestimmten Benutzer bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="14981-250">Contains information used for publishing the package, and also used at launch to ensure that a package is provisioned to a specific user.</span></span> <span data-ttu-id="14981-251">Wird in einem Roaming-Speicherort erstellt und enthält benutzerspezifische Veröffentlichungsinformationen.</span><span class="sxs-lookup"><span data-stu-id="14981-251">Created in a roaming location and includes user-specific publishing information.</span></span></p>
<p><span data-ttu-id="14981-252">Wenn ein Paket für einen Benutzer veröffentlicht wird, wird die Richtliniendatei im Benutzer Katalog gespeichert.</span><span class="sxs-lookup"><span data-stu-id="14981-252">When a package is published for a user, the policy file is stored in the User Catalog.</span></span> <span data-ttu-id="14981-253">Gleichzeitig wird eine Kopie des Manifests auch im Benutzer Katalog gespeichert.</span><span class="sxs-lookup"><span data-stu-id="14981-253">At the same time, a copy of the manifest is also stored in the User Catalog.</span></span> <span data-ttu-id="14981-254">Wenn ein Paket Anspruch für einen Benutzer entfernt wird, werden die entsprechenden Paketdateien aus dem Benutzer Katalog entfernt.</span><span class="sxs-lookup"><span data-stu-id="14981-254">When a package entitlement is removed for a user, the relevant package files are removed from the User Catalog.</span></span> <span data-ttu-id="14981-255">Wenn Sie sich den Benutzer Katalog ansehen, kann ein Administrator das vorhanden sein einer dynamischen Konfigurationsdatei anzeigen, die angibt, dass das Paket für diesen Benutzer berechtigt ist.</span><span class="sxs-lookup"><span data-stu-id="14981-255">Looking at the user catalog, an administrator can view the presence of a Dynamic Configuration file, which indicates that the package is entitled for that user.</span></span></p>
<p><span data-ttu-id="14981-256">Für Roaming-Benutzer muss sich der Benutzer Katalog an einem Roaming-oder freigegebenen Speicherort befinden, um das Legacy-App-V-Verhalten für die standardmäßige Ausrichtung von Benutzern beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="14981-256">For roaming users, the User Catalog needs to be in a roaming or shared location to preserve the legacy App-V behavior of targeting users by default.</span></span> <span data-ttu-id="14981-257">Der Anspruch und die Richtlinie sind an einen Benutzer und nicht an einen Computer gebunden, daher sollten Sie mit dem Benutzer Roaming durchlaufen, sobald er bereitgestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="14981-257">Entitlement and policy are tied to a user, not a computer, so they should roam with the user once they are provisioned.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="14981-258">Standardspeicherort</span><span class="sxs-lookup"><span data-stu-id="14981-258">Default storage location</span></span></p></td>
<td align="left"><p><code>appdata\roaming\Microsoft\AppV\Client\Catalog\Packages\PkgGUID\VerGUID</code></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="14981-259">Dateien im Benutzer Katalog</span><span class="sxs-lookup"><span data-stu-id="14981-259">Files in the user catalog</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="14981-260">UserManifest.xml</span><span class="sxs-lookup"><span data-stu-id="14981-260">UserManifest.xml</span></span></p></li>
<li><p><span data-ttu-id="14981-261">DynamicConfiguration.xml oder UserDeploymentConfiguration.xml</span><span class="sxs-lookup"><span data-stu-id="14981-261">DynamicConfiguration.xml or UserDeploymentConfiguration.xml</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="14981-262">Zusätzlicher Speicherort des Benutzer Katalogs, der verwendet wird, wenn das Paket zu einer Verbindungsgruppe gehört</span><span class="sxs-lookup"><span data-stu-id="14981-262">Additional user catalog location, used when the package is part of a connection group</span></span></p></td>
<td align="left"><p><span data-ttu-id="14981-263">Der folgende Standort ist zusätzlich zu dem oben genannten speziellen Paketspeicherort:</span><span class="sxs-lookup"><span data-stu-id="14981-263">The following location is in addition to the specific package location mentioned above:</span></span></p>
<p><code>appdata\roaming\Microsoft\AppV\Client\Catalog\PackageGroups\PkgGroupGUID\PkgGroupVerGUID</code></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="14981-264">Zusätzliche Datei im Computer Katalog, wenn das Paket zu einer Verbindungsgruppe gehört</span><span class="sxs-lookup"><span data-stu-id="14981-264">Additional file in the machine catalog when the package is part of a connection group</span></span></p></td>
<td align="left"><p><code>UserPackageGroupDescriptor.xml</code></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="14981-265">Verknüpfungs Sicherungen</span><span class="sxs-lookup"><span data-stu-id="14981-265">Shortcut backups</span></span>

<span data-ttu-id="14981-266">Während des Veröffentlichungsprozesses unterstützt der App-V-Client alle Verknüpfungen, und Integrationspunkte für `%AppData%\Microsoft\AppV\Client\Integration\ShortCutBackups.` diese Sicherung ermöglichen die Wiederherstellung dieser Integrationspunkte in den vorherigen Versionen, wenn das Paket nicht veröffentlicht wurde.</span><span class="sxs-lookup"><span data-stu-id="14981-266">During the publishing process, the App-V Client backs up any shortcuts and integration points to `%AppData%\Microsoft\AppV\Client\Integration\ShortCutBackups.` This backup enables the restoration of these integration points to the previous versions when the package is unpublished.</span></span>

### <span data-ttu-id="14981-267">Beim Schreiben von Dateien kopieren</span><span class="sxs-lookup"><span data-stu-id="14981-267">Copy on Write files</span></span>

<span data-ttu-id="14981-268">Der Paketspeicher enthält eine ursprüngliche Kopie der Paketdateien, die vom Veröffentlichungsserver gestreamt wurden.</span><span class="sxs-lookup"><span data-stu-id="14981-268">The Package Store contains a pristine copy of the package files that have been streamed from the publishing server.</span></span> <span data-ttu-id="14981-269">Während des normalen Betriebs einer App-V-Anwendung erfordert der Benutzer oder Dienst möglicherweise Änderungen an den Dateien.</span><span class="sxs-lookup"><span data-stu-id="14981-269">During normal operation of an App-V application, the user or service may require changes to the files.</span></span> <span data-ttu-id="14981-270">Diese Änderungen werden nicht im Paketspeicher vorgenommen, um die Möglichkeit zu erhalten, die Anwendung zu reparieren, wodurch diese Änderungen entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="14981-270">These changes are not made in the package store in order to preserve your ability to repair the application, which removes these changes.</span></span> <span data-ttu-id="14981-271">Diese Speicherorte, so genannte Copy on Write (Cow), unterstützen sowohl Roaming-als auch nicht-Roaming-Speicherorte.</span><span class="sxs-lookup"><span data-stu-id="14981-271">These locations, called Copy on Write (COW), support both roaming and non-roaming locations.</span></span> <span data-ttu-id="14981-272">Der Speicherort, an dem die Änderungen gespeichert werden, hängt davon ab, wo die Anwendung so programmiert wurde, dass Änderungen in einer systemeigenen Umgebung geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="14981-272">The location where the modifications are stored depends where the application has been programmed to write changes to in a native experience.</span></span>

### <span data-ttu-id="14981-273">Kuh-Roaming</span><span class="sxs-lookup"><span data-stu-id="14981-273">COW roaming</span></span>

<span data-ttu-id="14981-274">Der oben beschriebene Cow-Roaming-Standort speichert Änderungen an Dateien und Verzeichnissen, die auf den typischen Standort "% AppData%" oder "\\Users\\{username}\\AppData\\Roaming" ausgerichtet sind.</span><span class="sxs-lookup"><span data-stu-id="14981-274">The COW Roaming location described above stores changes to files and directories that are targeted to the typical %AppData% location or \\Users\\{username}\\AppData\\Roaming location.</span></span> <span data-ttu-id="14981-275">Diese Verzeichnisse und Dateien werden dann basierend auf den Einstellungen des Betriebssystems durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="14981-275">These directories and files are then roamed based on the operating system settings.</span></span>

### <span data-ttu-id="14981-276">Kuh lokal</span><span class="sxs-lookup"><span data-stu-id="14981-276">COW local</span></span>

<span data-ttu-id="14981-277">Der lokale Speicherort der Kuh ähnelt dem Roaming-Speicherort, aber die Verzeichnisse und Dateien werden nicht auf anderen Computern gespeichert, auch wenn Roaming-Unterstützung konfiguriert wurde.</span><span class="sxs-lookup"><span data-stu-id="14981-277">The COW Local location is similar to the roaming location, but the directories and files are not roamed to other computers, even if roaming support has been configured.</span></span> <span data-ttu-id="14981-278">Der oben beschriebene Cow-Standort speichert Änderungen, die für typische Fenster gelten, und nicht die Position% APPDATA%.</span><span class="sxs-lookup"><span data-stu-id="14981-278">The COW Local location described above stores changes applicable to typical windows and not the %AppData% location.</span></span> <span data-ttu-id="14981-279">Die aufgelisteten Verzeichnisse sind unterschiedlich, es gibt jedoch zwei Speicherorte für typische Windows-Speicherorte (beispielsweise Common APPDATA und Common AppDataS).</span><span class="sxs-lookup"><span data-stu-id="14981-279">The directories listed will vary but there will be two locations for any typical Windows locations (e.g. Common AppData and Common AppDataS).</span></span> <span data-ttu-id="14981-280">Das **S** gibt den eingeschränkten Speicherort an, wenn der virtuelle Dienst die Änderung als einen anderen erhöhten Benutzer von den angemeldeten Benutzern anfordert.</span><span class="sxs-lookup"><span data-stu-id="14981-280">The **S** signifies the restricted location when the virtual service requests the change as a different elevated user from the logged on users.</span></span> <span data-ttu-id="14981-281">Der nicht-**S** -Standort speichert benutzerbasierte Änderungen.</span><span class="sxs-lookup"><span data-stu-id="14981-281">The non-**S** location stores user based changes.</span></span>

## <a href="" id="bkmk-pkg-registry"></a><span data-ttu-id="14981-282">Paket Registrierung</span><span class="sxs-lookup"><span data-stu-id="14981-282">Package registry</span></span>


<span data-ttu-id="14981-283">Bevor eine Anwendung auf die Paket Registrierungsdaten zugreifen kann, muss der App-V-Client die Paket Registrierungsdaten für die Anwendungen verfügbar machen.</span><span class="sxs-lookup"><span data-stu-id="14981-283">Before an application can access the package registry data, the App-V Client must make the package registry data available to the applications.</span></span> <span data-ttu-id="14981-284">Der App-V-Client verwendet die echte Registrierung als Sicherungsspeicher für alle Registrierungsdaten.</span><span class="sxs-lookup"><span data-stu-id="14981-284">The App-V Client uses the real registry as a backing store for all registry data.</span></span>

<span data-ttu-id="14981-285">Wenn dem App-V-Client ein neues Paket hinzugefügt wird, eine Kopie der Registrierung. DAT-Datei aus dem Paket wird erstellt am `%ProgramData%\Microsoft\AppV\Client\VREG\{Version GUID}.dat` .</span><span class="sxs-lookup"><span data-stu-id="14981-285">When a new package is added to the App-V Client, a copy of the REGISTRY.DAT file from the package is created at `%ProgramData%\Microsoft\AppV\Client\VREG\{Version GUID}.dat`.</span></span> <span data-ttu-id="14981-286">Der Name der Datei ist die Versions-GUID mit dem. DAT-Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="14981-286">The name of the file is the version GUID with the .DAT extension.</span></span> <span data-ttu-id="14981-287">Der Grund für diese Kopie besteht darin, sicherzustellen, dass die eigentliche Hive-Datei im Paket nie verwendet wird, wodurch das Entfernen des Pakets zu einem späteren Zeitpunkt verhindert werden kann.</span><span class="sxs-lookup"><span data-stu-id="14981-287">The reason this copy is made is to ensure that the actual hive file in the package is never in use, which would prevent the removal of the package at a later time.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="14981-288">Registry. dat aus dem Paketspeicher</span><span class="sxs-lookup"><span data-stu-id="14981-288">Registry.dat from Package Store</span></span></strong></p></td>
<td align="left"><p><strong> &gt; </strong></p></td>
<td align="left"><p><strong><span data-ttu-id="14981-289">%ProgramData%\Microsoft\AppV\Client\Vreg {VersionGuid}. dat</span><span class="sxs-lookup"><span data-stu-id="14981-289">%ProgramData%\Microsoft\AppV\Client\Vreg{VersionGuid}.dat</span></span></strong></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="14981-290">Wenn die erste Anwendung aus dem Paket auf dem Client gestartet wird, wird der Client den Inhalt aus der hivedatei wiederherstellen oder kopieren, wodurch die Paket Registrierungsdaten an einem alternativen Speicherort neu erstellt werden `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\AppV\Client\Packages\PackageGuid\Versions\VersionGuid\REGISTRY` .</span><span class="sxs-lookup"><span data-stu-id="14981-290">When the first application from the package is launched on the client, the client stages or copies the contents out of the hive file, re-creating the package registry data in an alternate location `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\AppV\Client\Packages\PackageGuid\Versions\VersionGuid\REGISTRY`.</span></span> <span data-ttu-id="14981-291">Die bereitgestellten Registrierungsdaten weisen zwei unterschiedliche Typen von Computer Daten und Benutzerdaten auf.</span><span class="sxs-lookup"><span data-stu-id="14981-291">The staged registry data has two distinct types of machine data and user data.</span></span> <span data-ttu-id="14981-292">Computer Daten werden für alle Benutzer auf dem Computer freigegeben.</span><span class="sxs-lookup"><span data-stu-id="14981-292">Machine data is shared across all users on the machine.</span></span> <span data-ttu-id="14981-293">Benutzerdaten werden für jeden Benutzer an einem benutzerabhängige-Speicherort bereitgestellt `HKCU\Software\Microsoft\AppV\Client\Packages\PackageGuid\Registry\User` .</span><span class="sxs-lookup"><span data-stu-id="14981-293">User data is staged for each user to a userspecific location `HKCU\Software\Microsoft\AppV\Client\Packages\PackageGuid\Registry\User`.</span></span> <span data-ttu-id="14981-294">Die Computer Daten werden letztendlich beim Entfernen des Pakets entfernt, und die Benutzerdaten werden bei einem Veröffentlichungsvorgang des Benutzers entfernt.</span><span class="sxs-lookup"><span data-stu-id="14981-294">The machine data is ultimately removed at package removal time, and the user data is removed on a user unpublish operation.</span></span>

### <span data-ttu-id="14981-295">Staging von Paket Registrierungen vs. Verbindungsgruppen Registrierung</span><span class="sxs-lookup"><span data-stu-id="14981-295">Package registry staging vs. connection group registry staging</span></span>

<span data-ttu-id="14981-296">Wenn Verbindungsgruppen vorhanden sind, gilt der vorherige Prozess der Staging der Registrierung als wahr, doch anstatt eine Strukturdatei zu verarbeiten, gibt es mehr als eine.</span><span class="sxs-lookup"><span data-stu-id="14981-296">When connection groups are present, the previous process of staging the registry holds true, but instead of having one hive file to process, there are more than one.</span></span> <span data-ttu-id="14981-297">Die Dateien werden in der Reihenfolge verarbeitet, in der Sie in der Verbindungsgruppe XML angezeigt werden, wobei der erste Writer Konflikte gewinnt.</span><span class="sxs-lookup"><span data-stu-id="14981-297">The files are processed in the order in which they appear in the connection group XML, with the first writer winning any conflicts.</span></span>

<span data-ttu-id="14981-298">Die bereitgestellte Registrierung bleibt auf die gleiche Weise wie im einzelnen Paket Fall erhalten.</span><span class="sxs-lookup"><span data-stu-id="14981-298">The staged registry persists the same way as in the single package case.</span></span> <span data-ttu-id="14981-299">Die bereitgestellten Benutzerregistrierungsdaten verbleibt für die Verbindungsgruppe, bis Sie deaktiviert ist. die Registrierungsdaten für ein Stagingcomputer werden beim Entfernen der Verbindungsgruppe entfernt.</span><span class="sxs-lookup"><span data-stu-id="14981-299">Staged user registry data remains for the connection group until it is disabled; staged machine registry data is removed on connection group removal.</span></span>

### <span data-ttu-id="14981-300">Virtuelle Registrierung</span><span class="sxs-lookup"><span data-stu-id="14981-300">Virtual registry</span></span>

<span data-ttu-id="14981-301">Der Zweck der virtuellen Registrierung (VREG) besteht darin, eine einzelne zusammengeführte Ansicht der Paket Registrierung und der systemeigenen Registrierung für Anwendungen bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="14981-301">The purpose of the virtual registry (VREG) is to provide a single merged view of the package registry and the native registry to applications.</span></span> <span data-ttu-id="14981-302">Darüber hinaus bietet es die Funktion Copy-on-Write (Cow) – das heißt, dass alle Änderungen an der Registrierung aus dem Kontext eines virtuellen Prozesses an einem separaten Cow-Speicherort vorgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="14981-302">It also provides copy-on-write (COW) functionality – that is any changes made to the registry from the context of a virtual process are made to a separate COW location.</span></span> <span data-ttu-id="14981-303">Das bedeutet, dass der VREG bis zu drei getrennte Registrierungsspeicherorte in einer einzigen Ansicht basierend auf den aufgefüllten Speicherorten in der Registrierungs-Cow- &gt; Package-Native kombinieren muss &gt; .</span><span class="sxs-lookup"><span data-stu-id="14981-303">This means that the VREG must combine up to three separate registry locations into a single view based on the populated locations in the registry COW -&gt; package -&gt; native.</span></span> <span data-ttu-id="14981-304">Wenn eine Anforderung für Registrierungsdaten erfolgt, findet Sie in der Reihenfolge, bis Sie die angeforderten Daten gefunden hat.</span><span class="sxs-lookup"><span data-stu-id="14981-304">When a request is made for a registry data it will locate in order until it finds the data it was requesting.</span></span> <span data-ttu-id="14981-305">Bedeutet dies, dass ein Wert, der in einem Cow-Speicherort gespeichert ist, nicht an andere Speicherorte weitergeleitet wird, wenn sich am Speicherort der Kuh keine Daten befinden, wird das Paket und dann der systemeigene Speicherort weitergeleitet, bis die entsprechenden Daten gefunden wurden.</span><span class="sxs-lookup"><span data-stu-id="14981-305">Meaning if there is a value stored in a COW location it will not proceed to other locations, however, if there is no data in the COW location it will proceed to the Package and then Native location until it finds the appropriate data.</span></span>

### <span data-ttu-id="14981-306">Registrierungsspeicherorte</span><span class="sxs-lookup"><span data-stu-id="14981-306">Registry locations</span></span>

<span data-ttu-id="14981-307">Je nachdem, ob das Paket einzeln oder als Teil einer Verbindungsgruppe veröffentlicht wird, gibt es zwei Speicherorte für die Paket Registrierung und zwei Verbindungsgruppen Speicherorte, an denen der App-V-Client Registrierungsinformationen speichert.</span><span class="sxs-lookup"><span data-stu-id="14981-307">There are two package registry locations and two connection group locations where the App-V Client stores registry information, depending on whether the Package is published individually or as part of a connection group.</span></span> <span data-ttu-id="14981-308">Es gibt drei Cow-Speicherorte für Pakete und drei für Verbindungsgruppen, die von der VREG erstellt und verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="14981-308">There are three COW locations for packages and three for connection groups, which are created and managed by the VREG.</span></span> <span data-ttu-id="14981-309">Einstellungen für Pakete und Verbindungsgruppen werden nicht freigegeben:</span><span class="sxs-lookup"><span data-stu-id="14981-309">Settings for packages and connection groups are not shared:</span></span>

**<span data-ttu-id="14981-310">Einzelnes Paket VReg:</span><span class="sxs-lookup"><span data-stu-id="14981-310">Single Package VReg:</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="14981-311">Pfad</span><span class="sxs-lookup"><span data-stu-id="14981-311">Location</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="14981-312">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="14981-312">Description</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="14981-313">Kuhanzug</span><span class="sxs-lookup"><span data-stu-id="14981-313">COW</span></span></strong></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="14981-314">Machine Registry\Client\Packages\PkgGUID\REGISTRY (nur Elevate-Prozess kann schreiben)</span><span class="sxs-lookup"><span data-stu-id="14981-314">Machine Registry\Client\Packages\PkgGUID\REGISTRY (Only elevate process can write)</span></span></p></li>
<li><p><span data-ttu-id="14981-315">Benutzer Registry\Client\Packages\PkgGUID\REGISTRY (Benutzer-Roaming-alles, was unter HKCU außer Software\Classes geschrieben wurde</span><span class="sxs-lookup"><span data-stu-id="14981-315">User Registry\Client\Packages\PkgGUID\REGISTRY (User Roaming anything written under HKCU except Software\Classes</span></span></p></li>
<li><p><span data-ttu-id="14981-316">Benutzer Registrierungs Classes\Client\Packages\PkgGUID\REGISTRY (HKCU\Software\Classes-Schreibvorgänge und HKLM für nicht erhöhten Prozess)</span><span class="sxs-lookup"><span data-stu-id="14981-316">User Registry Classes\Client\Packages\PkgGUID\REGISTRY (HKCU\Software\Classes writes and HKLM for non elevated process)</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="14981-317">Paket</span><span class="sxs-lookup"><span data-stu-id="14981-317">Package</span></span></strong></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="14981-318">Machine Registry\Client\Packages\PkgGUID\Versions\VerGuid\Registry\Machine</span><span class="sxs-lookup"><span data-stu-id="14981-318">Machine Registry\Client\Packages\PkgGUID\Versions\VerGuid\Registry\Machine</span></span></p></li>
<li><p><span data-ttu-id="14981-319">Benutzer Registrierungs Classes\Client\Packages\PkgGUID\Versions\VerGUID\Registry</span><span class="sxs-lookup"><span data-stu-id="14981-319">User Registry Classes\Client\Packages\PkgGUID\Versions\VerGUID\Registry</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="14981-320">Systemeigene</span><span class="sxs-lookup"><span data-stu-id="14981-320">Native</span></span></strong></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="14981-321">Registrierungsspeicherort der systemeigenen Anwendung</span><span class="sxs-lookup"><span data-stu-id="14981-321">Native application registry location</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

 

**<span data-ttu-id="14981-322">Verbindungsgruppe VReg:</span><span class="sxs-lookup"><span data-stu-id="14981-322">Connection Group VReg:</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="14981-323">Pfad</span><span class="sxs-lookup"><span data-stu-id="14981-323">Location</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="14981-324">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="14981-324">Description</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="14981-325">Kuhanzug</span><span class="sxs-lookup"><span data-stu-id="14981-325">COW</span></span></strong></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="14981-326">Machine Registry\Client\PackageGroups\GrpGUID\REGISTRY (nur Elevate-Prozess kann schreiben)</span><span class="sxs-lookup"><span data-stu-id="14981-326">Machine Registry\Client\PackageGroups\GrpGUID\REGISTRY (only elevate process can write)</span></span></p></li>
<li><p><span data-ttu-id="14981-327">Benutzer Registry\Client\PackageGroups\GrpGUID\REGISTRY (alles, was in HKCU außer Software\Classes geschrieben wurde</span><span class="sxs-lookup"><span data-stu-id="14981-327">User Registry\Client\PackageGroups\GrpGUID\REGISTRY (Anything written to HKCU except Software\Classes</span></span></p></li>
<li><p><span data-ttu-id="14981-328">Benutzer Registrierungs Classes\Client\PackageGroups\GrpGUID\REGISTRY</span><span class="sxs-lookup"><span data-stu-id="14981-328">User Registry Classes\Client\PackageGroups\GrpGUID\REGISTRY</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="14981-329">Paket</span><span class="sxs-lookup"><span data-stu-id="14981-329">Package</span></span></strong></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="14981-330">Machine Registry\Client\PackageGroups\GrpGUID\Versions\VerGUID\REGISTRY</span><span class="sxs-lookup"><span data-stu-id="14981-330">Machine Registry\Client\PackageGroups\GrpGUID\Versions\VerGUID\REGISTRY</span></span></p></li>
<li><p><span data-ttu-id="14981-331">Benutzer Registrierungs Classes\Client\PackageGroups\GrpGUID\Versions\VerGUID\REGISTRY</span><span class="sxs-lookup"><span data-stu-id="14981-331">User Registry Classes\Client\PackageGroups\GrpGUID\Versions\VerGUID\REGISTRY</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="14981-332">Systemeigene</span><span class="sxs-lookup"><span data-stu-id="14981-332">Native</span></span></strong></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="14981-333">Registrierungsspeicherort der systemeigenen Anwendung</span><span class="sxs-lookup"><span data-stu-id="14981-333">Native application registry location</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

 

<span data-ttu-id="14981-334">Es gibt zwei Kuh-Standorte für HKLM; erhöhte und nicht erhöhte Prozesse.</span><span class="sxs-lookup"><span data-stu-id="14981-334">There are two COW locations for HKLM; elevated and non-elevated processes.</span></span> <span data-ttu-id="14981-335">Erhöhte Prozesse schreiben immer HKLM-Änderungen in die sichere Kuh unter HKLM.</span><span class="sxs-lookup"><span data-stu-id="14981-335">Elevated processes always write HKLM changes to the secure COW under HKLM.</span></span> <span data-ttu-id="14981-336">Nicht erhöhte Prozesse schreiben immer HKLM-Änderungen an der nicht sicheren Kuh unter HKCU\\Software\\Classes.</span><span class="sxs-lookup"><span data-stu-id="14981-336">Non-elevated processes always write HKLM changes to the non-secure COW under HKCU\\Software\\Classes.</span></span> <span data-ttu-id="14981-337">Wenn eine Anwendung Änderungen von HKLM liest, lesen erhöhte Prozesse Änderungen aus der sicheren Kuh unter HKLM.</span><span class="sxs-lookup"><span data-stu-id="14981-337">When an application reads changes from HKLM, elevated processes will read changes from the secure COW under HKLM.</span></span> <span data-ttu-id="14981-338">Nicht erhöhte Lesevorgänge von beiden, begünstigt die Änderungen, die in der unsicheren Kuh zuerst vorgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="14981-338">Non-elevated reads from both, favoring the changes made in the unsecure COW first.</span></span>

### <span data-ttu-id="14981-339">Pass-Through-Tasten</span><span class="sxs-lookup"><span data-stu-id="14981-339">Pass-through keys</span></span>

<span data-ttu-id="14981-340">Durch Pass-Through-Tasten können Administratoren bestimmte Schlüssel so konfigurieren, dass Sie nur aus der systemeigenen Registrierung gelesen werden können, wobei die Speicherorte für Pakete und Kühe umgangen werden.</span><span class="sxs-lookup"><span data-stu-id="14981-340">Pass-through keys enable an administrator to configure certain keys so they can only be read from the native registry, bypassing the Package and COW locations.</span></span> <span data-ttu-id="14981-341">Pass-Through-Speicherorte sind global auf dem Computer (nicht Paket spezifisch) und können konfiguriert werden, indem Sie den Pfad zum Schlüssel hinzufügen, der als Pass-Through für das **reg \ _MULTI \ _SZ** Wert **PassThroughPaths** des Schlüssels behandelt werden soll `HKLM\Software\Microsoft\AppV\Subsystem\VirtualRegistry` .</span><span class="sxs-lookup"><span data-stu-id="14981-341">Pass-through locations are global to the machine (not package specific) and can be configured by adding the path to the key, which should be treated as pass-through to the **REG\_MULTI\_SZ** value called **PassThroughPaths** of the key `HKLM\Software\Microsoft\AppV\Subsystem\VirtualRegistry`.</span></span> <span data-ttu-id="14981-342">Jede Taste, die unter diesem mehrteiligen Zeichenfolgenwert (und ihren untergeordneten Elementen) angezeigt wird, wird als Passthrough behandelt.</span><span class="sxs-lookup"><span data-stu-id="14981-342">Any key that appears under this multi-string value (and their children) will be treated as pass-through.</span></span>

<span data-ttu-id="14981-343">Die folgenden Speicherorte sind standardmäßig als Pass-Through-Speicherorte konfiguriert:</span><span class="sxs-lookup"><span data-stu-id="14981-343">The following locations are configured as pass-through locations by default:</span></span>

-   <span data-ttu-id="14981-344">HKEY \ _CURRENT \ _User \\software\\classes\\local Settings\\Software\\Microsoft\\Windows\\CurrentVersion\\AppModel</span><span class="sxs-lookup"><span data-stu-id="14981-344">HKEY\_CURRENT\_USER\\SOFTWARE\\Classes\\Local Settings\\Software\\Microsoft\\Windows\\CurrentVersion\\AppModel</span></span>

-   <span data-ttu-id="14981-345">HKEY \ _LOCAL \ _MACHINE \\software\\classes\\local Settings\\Software\\Microsoft\\Windows\\CurrentVersion\\AppModel</span><span class="sxs-lookup"><span data-stu-id="14981-345">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes\\Local Settings\\Software\\Microsoft\\Windows\\CurrentVersion\\AppModel</span></span>

-   <span data-ttu-id="14981-346">HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\windows\\currentversion\\winevt</span><span class="sxs-lookup"><span data-stu-id="14981-346">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows\\CurrentVersion\\WINEVT</span></span>

-   <span data-ttu-id="14981-347">HKEY \ _LOCAL \ _MACHINE \\system\\currentcontrolset\\services\\eventlog\\application</span><span class="sxs-lookup"><span data-stu-id="14981-347">HKEY\_LOCAL\_MACHINE\\SYSTEM\\CurrentControlSet\\services\\eventlog\\Application</span></span>

-   <span data-ttu-id="14981-348">HKEY \ _LOCAL \ _MACHINE \\system\\currentcontrolset\\control\\wmi\\autologger</span><span class="sxs-lookup"><span data-stu-id="14981-348">HKEY\_LOCAL\_MACHINE\\SYSTEM\\CurrentControlSet\\Control\\WMI\\Autologger</span></span>

-   <span data-ttu-id="14981-349">HKEY \ _CURRENT \ _User \\software\\microsoft\\windows\\currentversion\\internet-Einstellungen</span><span class="sxs-lookup"><span data-stu-id="14981-349">HKEY\_CURRENT\_USER\\SOFTWARE\\Microsoft\\Windows\\CurrentVersion\\Internet Settings</span></span>

-   <span data-ttu-id="14981-350">HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\windows NT\\CurrentVersion\\Perflib</span><span class="sxs-lookup"><span data-stu-id="14981-350">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\Perflib</span></span>

-   <span data-ttu-id="14981-351">HKEY \ _LOCAL \ _MACHINE \\software\\policies</span><span class="sxs-lookup"><span data-stu-id="14981-351">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Policies</span></span>

-   <span data-ttu-id="14981-352">HKEY \ _CURRENT \ _User \\software\\policies</span><span class="sxs-lookup"><span data-stu-id="14981-352">HKEY\_CURRENT\_USER\\SOFTWARE\\Policies</span></span>

<span data-ttu-id="14981-353">Der Zweck von Pass-Through-Schlüsseln besteht darin, sicherzustellen, dass eine virtuelle Anwendung keine Registrierungsdaten in die VReg schreibt, die für nicht virtuelle Anwendungen für den erfolgreichen Betrieb oder die Integration erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="14981-353">The purpose of Pass-through keys is to ensure that a virtual application does not write registry data in the VReg that is required for non-virtual applications for successful operation or integration.</span></span> <span data-ttu-id="14981-354">Mit dem Richtlinienschlüssel wird sichergestellt, dass die vom Administrator festgelegten gruppenrichtlinienbasierten Einstellungen verwendet werden und nicht pro Paketeinstellungen.</span><span class="sxs-lookup"><span data-stu-id="14981-354">The Policies key ensures that Group Policy based settings set by the administrator are utilized and not per package settings.</span></span> <span data-ttu-id="14981-355">Der AppModel-Schlüssel ist für die Integration in Windows moderne UI-basierte Anwendungen erforderlich.</span><span class="sxs-lookup"><span data-stu-id="14981-355">The AppModel key is required for integration with Windows Modern UI based applications.</span></span> <span data-ttu-id="14981-356">Es wird empfohlen, dass Verwaltungen keine der standardmäßigen Pass-Through-Schlüssel ändern, aber in einigen Fällen erfordert das Hinzufügen von zusätzlichen Pass-Through-Schlüsseln möglicherweise auf Grundlage des Anwendungsverhaltens.</span><span class="sxs-lookup"><span data-stu-id="14981-356">It is recommend that administers do not modify any of the default pass-through keys, but in some instances, based on application behavior may require adding additional pass-through keys.</span></span>

## <a href="" id="bkmk-pkg-store-behavior"></a><span data-ttu-id="14981-357">App-V-Paketspeicher Verhalten</span><span class="sxs-lookup"><span data-stu-id="14981-357">App-V package store behavior</span></span>


<span data-ttu-id="14981-358">App-V 5 verwaltet den Paketspeicher, also den Speicherort, an dem die erweiterten Objektdateien aus der AppV-Datei gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="14981-358">App-V 5 manages the Package Store, which is the location where the expanded asset files from the appv file are stored.</span></span> <span data-ttu-id="14981-359">Dieser Speicherort wird standardmäßig unter%ProgramData%\\App-V gespeichert und ist in Bezug auf Speicherfunktionen nur durch freien Speicherplatz limitiert.</span><span class="sxs-lookup"><span data-stu-id="14981-359">By default, this location is stored at %ProgramData%\\App-V, and is limited in terms of storage capabilities only by free disk space.</span></span> <span data-ttu-id="14981-360">Der Paketspeicher wird nach den GUIDs für das Paket und die Version organisiert, wie im vorherigen Abschnitt erwähnt.</span><span class="sxs-lookup"><span data-stu-id="14981-360">The package store is organized by the GUIDs for the package and version as mentioned in the previous section.</span></span>

### <span data-ttu-id="14981-361">Pakete hinzufügen</span><span class="sxs-lookup"><span data-stu-id="14981-361">Add packages</span></span>

<span data-ttu-id="14981-362">App-v-Pakete werden beim Hinzufügen des Computers mit dem App-v-Client bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="14981-362">App-V Packages are staged upon addition to the computer with the App-V Client.</span></span> <span data-ttu-id="14981-363">Der App-V-Client bietet Staging auf Abruf.</span><span class="sxs-lookup"><span data-stu-id="14981-363">The App-V Client provides on-demand staging.</span></span> <span data-ttu-id="14981-364">Während der Veröffentlichung oder einem manuellen Add-AppVClientPackage wird die Datenstruktur im Paketspeicher (c:\\programdata\\App-V\\{PkgGUID}\\{VerGUID}) erstellt.</span><span class="sxs-lookup"><span data-stu-id="14981-364">During publishing or a manual Add-AppVClientPackage, the data structure is built in the package store (c:\\programdata\\App-V\\{PkgGUID}\\{VerGUID}).</span></span> <span data-ttu-id="14981-365">Die im StreamMap.xml definierten Veröffentlichungs Blocks werden dem System und den Ordnern der obersten Ebene und untergeordneten Dateien hinzugefügt, um sicherzustellen, dass beim Start geeignete Anwendungsressourcen vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="14981-365">The package files identified in the publishing block defined in the StreamMap.xml are added to the system and the top level folders and child files staged to ensure proper application assets exist at launch.</span></span>

### <span data-ttu-id="14981-366">Befestigungs Pakete</span><span class="sxs-lookup"><span data-stu-id="14981-366">Mounting packages</span></span>

<span data-ttu-id="14981-367">Pakete können explizit mit der PowerShell oder mithilfe `Mount-AppVClientPackage` der **App-V-Client-Benutzeroberfläche** geladen werden, um ein Paket herunterzuladen.</span><span class="sxs-lookup"><span data-stu-id="14981-367">Packages can be explicitly loaded using the PowerShell `Mount-AppVClientPackage` or by using the **App-V Client UI** to download a package.</span></span> <span data-ttu-id="14981-368">Durch diesen Vorgang wird das gesamte Paket vollständig in den Paketspeicher geladen.</span><span class="sxs-lookup"><span data-stu-id="14981-368">This operation completely loads the entire package into the package store.</span></span>

### <span data-ttu-id="14981-369">Streaming-Pakete</span><span class="sxs-lookup"><span data-stu-id="14981-369">Streaming packages</span></span>

<span data-ttu-id="14981-370">Der App-V-Client kann so konfiguriert werden, dass das Standardverhalten von Streaming geändert wird.</span><span class="sxs-lookup"><span data-stu-id="14981-370">The App-V Client can be configured to change the default behavior of streaming.</span></span> <span data-ttu-id="14981-371">Alle Streaming-Richtlinien werden unter dem folgenden Registrierungsschlüssel gespeichert: `HKEY_LOCAL_MAcHINE\Software\Microsoft\AppV\Client\Streaming`</span><span class="sxs-lookup"><span data-stu-id="14981-371">All streaming policies are stored under the following registry key: `HKEY_LOCAL_MAcHINE\Software\Microsoft\AppV\Client\Streaming`.</span></span> <span data-ttu-id="14981-372">Richtlinien werden mit dem PowerShell-Cmdlet gesetzt `Set-AppvClientConfiguration` .</span><span class="sxs-lookup"><span data-stu-id="14981-372">Policies are set using the PowerShell cmdlet `Set-AppvClientConfiguration`.</span></span> <span data-ttu-id="14981-373">Die folgenden Richtlinien gelten für Streaming:</span><span class="sxs-lookup"><span data-stu-id="14981-373">The following policies apply to Streaming:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="14981-374">Richtlinie</span><span class="sxs-lookup"><span data-stu-id="14981-374">Policy</span></span></th>
<th align="left"><span data-ttu-id="14981-375">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="14981-375">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="14981-376">AllowHighCostLaunch</span><span class="sxs-lookup"><span data-stu-id="14981-376">AllowHighCostLaunch</span></span></p></td>
<td align="left"><p><span data-ttu-id="14981-377">Unter Windows 8 ist das Streaming über 3G-und Mobilfunknetze möglich.</span><span class="sxs-lookup"><span data-stu-id="14981-377">On Windows 8 it allows streaming over 3G and cellular networks</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="14981-378">AutoLoad</span><span class="sxs-lookup"><span data-stu-id="14981-378">AutoLoad</span></span></p></td>
<td align="left"><p><span data-ttu-id="14981-379">Gibt die Einstellung für den Hintergrund Ladevorgang an:</span><span class="sxs-lookup"><span data-stu-id="14981-379">Specifies the Background Load setting:</span></span></p>
<p><strong><span data-ttu-id="14981-380">0 </strong> - deaktiviert</span><span class="sxs-lookup"><span data-stu-id="14981-380">0</strong> - Disabled</span></span></p>
<p><strong><span data-ttu-id="14981-381">1 </strong> – nur zuvor verwendete Pakete</span><span class="sxs-lookup"><span data-stu-id="14981-381">1</strong> – Previously Used Packages only</span></span></p>
<p><strong><span data-ttu-id="14981-382">2 </strong> – alle Pakete</span><span class="sxs-lookup"><span data-stu-id="14981-382">2</strong> – All Packages</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="14981-383">PackageInstallationRoot</span><span class="sxs-lookup"><span data-stu-id="14981-383">PackageInstallationRoot</span></span></p></td>
<td align="left"><p><span data-ttu-id="14981-384">Der Stammordner für den Paketspeicher auf dem lokalen Computer</span><span class="sxs-lookup"><span data-stu-id="14981-384">The root folder for the package store in the local machine</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="14981-385">PackageSourceRoot</span><span class="sxs-lookup"><span data-stu-id="14981-385">PackageSourceRoot</span></span></p></td>
<td align="left"><p><span data-ttu-id="14981-386">Die Root-Überschreibung, von der Pakete gestreamt werden sollen</span><span class="sxs-lookup"><span data-stu-id="14981-386">The root override where packages should be streamed from</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="14981-387">SharedContentStoreMode</span><span class="sxs-lookup"><span data-stu-id="14981-387">SharedContentStoreMode</span></span></p></td>
<td align="left"><p><span data-ttu-id="14981-388">Ermöglicht die Verwendung des freigegebenen Inhaltsspeichers für VDI-Szenarien</span><span class="sxs-lookup"><span data-stu-id="14981-388">Enables the use of Shared Content Store for VDI scenarios</span></span></p></td>
</tr>
</tbody>
</table>

 

 

<span data-ttu-id="14981-389">Diese Einstellungen wirken sich auf das Verhalten von Streaming-App-V-Paketressourcen auf den Client aus.</span><span class="sxs-lookup"><span data-stu-id="14981-389">These settings affect the behavior of streaming App-V package assets to the client.</span></span> <span data-ttu-id="14981-390">Standardmäßig downloadet App-V nur die Ressourcen, die nach dem Herunterladen der ersten Veröffentlichungs-und primären Feature-Blöcke erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="14981-390">By default, App-V only downloads the assets required after downloading the initial publishing and primary feature blocks.</span></span> <span data-ttu-id="14981-391">Es gibt drei spezifische Verhaltensweisen rund um Streaming-Pakete, die erläutert werden müssen:</span><span class="sxs-lookup"><span data-stu-id="14981-391">There are three specific behaviors around streaming packages that must be explained:</span></span>

-   <span data-ttu-id="14981-392">Hintergrund Streaming</span><span class="sxs-lookup"><span data-stu-id="14981-392">Background Streaming</span></span>

-   <span data-ttu-id="14981-393">Optimiertes Streaming</span><span class="sxs-lookup"><span data-stu-id="14981-393">Optimized Streaming</span></span>

-   <span data-ttu-id="14981-394">Datenstromfehler</span><span class="sxs-lookup"><span data-stu-id="14981-394">Stream Faults</span></span>

### <span data-ttu-id="14981-395">Hintergrund Streaming</span><span class="sxs-lookup"><span data-stu-id="14981-395">Background streaming</span></span>

<span data-ttu-id="14981-396">Das PowerShell `Get-AppvClientConfiguration` -Cmdlet kann verwendet werden, um den aktuellen Modus für das Hintergrund Streaming mit der Einstellung "automatischer Lademodus" zu ermitteln und mit dem Cmdlet "AppvClientConfiguration" oder "Registry" (HKLM\\SOFTWARE\\Microsoft\\AppV\\ClientStreaming-Schlüssel) zu ändern.</span><span class="sxs-lookup"><span data-stu-id="14981-396">The PowerShell cmdlet `Get-AppvClientConfiguration` can be used to determine the current mode for background streaming with the AutoLoad setting and modified with the cmdlet Set-AppvClientConfiguration or from the registry (HKLM\\SOFTWARE\\Microsoft\\AppV\\ClientStreaming key).</span></span> <span data-ttu-id="14981-397">"Hintergrund Streaming" ist eine Standardeinstellung, bei der die Einstellung "automatisch laden" so eingestellt ist, dass zuvor verwendete Pakete heruntergeladen werden.</span><span class="sxs-lookup"><span data-stu-id="14981-397">Background streaming is a default setting where the Autoload setting is set to download previously used packages.</span></span> <span data-ttu-id="14981-398">Das Verhalten, das auf der Standardeinstellung (Wert = 1) basiert, downloadet App-V-Datenblöcke im Hintergrund, nachdem die Anwendung gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="14981-398">The behavior based on default setting (value=1) downloads App-V data blocks in the background after the application has been launched.</span></span> <span data-ttu-id="14981-399">Diese Einstellung kann alle zusammen (Wert = 0) oder aktiviert für alle Pakete (Wert = 2) deaktiviert werden, unabhängig davon, ob Sie gestartet wurden.</span><span class="sxs-lookup"><span data-stu-id="14981-399">This setting can be disabled all together (value=0) or enabled for all packages (value=2), whether they have been launched.</span></span>

### <span data-ttu-id="14981-400">Optimiertes Streaming</span><span class="sxs-lookup"><span data-stu-id="14981-400">Optimized streaming</span></span>

<span data-ttu-id="14981-401">App-V-Pakete können während der Sequenzierung mit einem primären Feature-Block konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="14981-401">App-V packages can be configured with a primary feature block during sequencing.</span></span> <span data-ttu-id="14981-402">Diese Einstellung ermöglicht es dem Sequenz Ingenieur, Startdateien für eine bestimmte Anwendung oder Anwendungen zu überwachen und die Datenblöcke im App-V-Paket für Streaming beim ersten Start einer beliebigen Anwendung im Paket zu kennzeichnen.</span><span class="sxs-lookup"><span data-stu-id="14981-402">This setting allows the sequencing engineer to monitor launch files for a specific application, or applications, and mark the blocks of data in the App-V package for streaming at first launch of any application in the package.</span></span>

### <span data-ttu-id="14981-403">Datenstromfehler</span><span class="sxs-lookup"><span data-stu-id="14981-403">Stream faults</span></span>

<span data-ttu-id="14981-404">Nach dem anfänglichen Datenstrom von Veröffentlichungsdaten und dem primären Feature-Block führen Anforderungen für zusätzliche Dateien Datenstromfehler aus.</span><span class="sxs-lookup"><span data-stu-id="14981-404">After the initial stream of any publishing data and the primary feature block, requests for additional files perform stream faults.</span></span> <span data-ttu-id="14981-405">Diese Datenblöcke werden nach Bedarf in den Paketspeicher heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="14981-405">These blocks of data are downloaded to the package store on an as-needed basis.</span></span> <span data-ttu-id="14981-406">Auf diese Weise kann ein Benutzer nur einen kleinen Teil des Pakets herunterladen, was in der Regel ausreicht, um das Paket zu starten und normale Aufgaben auszuführen.</span><span class="sxs-lookup"><span data-stu-id="14981-406">This allows a user to download only a small part of the package, typically enough to launch the package and run normal tasks.</span></span> <span data-ttu-id="14981-407">Alle anderen Blöcke werden heruntergeladen, wenn ein Benutzer einen Vorgang initiiert, der Daten erfordert, die derzeit nicht im Paketspeicher enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="14981-407">All other blocks are downloaded when a user initiates an operation that requires data not currently in the package store.</span></span>

<span data-ttu-id="14981-408">Weitere Informationen zum App-V-Paketstreaming finden Sie unter: <https://go.microsoft.com/fwlink/?LinkId=392770> .</span><span class="sxs-lookup"><span data-stu-id="14981-408">For more information on App-V Package streaming visit: <https://go.microsoft.com/fwlink/?LinkId=392770>.</span></span>

<span data-ttu-id="14981-409">Die Sequenzierung für die Streaming-Optimierung steht unter: <https://go.microsoft.com/fwlink/?LinkId=392771> .</span><span class="sxs-lookup"><span data-stu-id="14981-409">Sequencing for streaming optimization is available at: <https://go.microsoft.com/fwlink/?LinkId=392771>.</span></span>

### <span data-ttu-id="14981-410">Paketaktualisierungen</span><span class="sxs-lookup"><span data-stu-id="14981-410">Package upgrades</span></span>

<span data-ttu-id="14981-411">App-V-Pakete erfordern eine Aktualisierung während des gesamten Lebenszyklus der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="14981-411">App-V Packages require updating throughout the lifecycle of the application.</span></span> <span data-ttu-id="14981-412">App-V-Paketaktualisierungen ähneln dem Paket Veröffentlichungsvorgang, da jede Version in Ihrem eigenen PackageRoot-Speicherort erstellt wird: `%ProgramData%\App-V\{PkgGUID}\{newVerGUID}` .</span><span class="sxs-lookup"><span data-stu-id="14981-412">App-V Package upgrades are similar to the package publish operation, as each version will be created in its own PackageRoot location: `%ProgramData%\App-V\{PkgGUID}\{newVerGUID}`.</span></span> <span data-ttu-id="14981-413">Der Upgradevorgang wird durch das Erstellen von festen Links zu identischen und gestreamten Dateien aus anderen Versionen desselben Pakets optimiert.</span><span class="sxs-lookup"><span data-stu-id="14981-413">The upgrade operation is optimized by creating hard links to identical- and streamed-files from other versions of the same package.</span></span>

### <span data-ttu-id="14981-414">Paketentfernung</span><span class="sxs-lookup"><span data-stu-id="14981-414">Package removal</span></span>

<span data-ttu-id="14981-415">Das Verhalten des App-V-Clients, wenn Pakete entfernt werden, hängt von der zum Entfernen verwendeten Methode ab.</span><span class="sxs-lookup"><span data-stu-id="14981-415">The behavior of the App-V Client when packages are removed depends on the method used for removal.</span></span> <span data-ttu-id="14981-416">Wenn Sie eine vollständige App-V-Infrastruktur verwenden, um die Veröffentlichung der Anwendung aufzuheben, werden die Benutzer Katalogdateien (Computer Katalog für Global veröffentlichte Anwendungen) entfernt, aber der Speicherort des Paketspeichers und die Standorte für Kühe bleiben erhalten.</span><span class="sxs-lookup"><span data-stu-id="14981-416">Using an App-V full infrastructure to unpublish the application, the user catalog files (machine catalog for globally published applications) are removed, but retains the package store location and COW locations.</span></span> <span data-ttu-id="14981-417">Wenn das PowerShell `Remove-AppVClientPackge` -Cmdlet zum Entfernen eines App-V-Pakets verwendet wird, wird der Speicherort des Paketspeichers bereinigt.</span><span class="sxs-lookup"><span data-stu-id="14981-417">When the PowerShell cmdlet `Remove-AppVClientPackge` is used to remove an App-V Package, the package store location is cleaned.</span></span> <span data-ttu-id="14981-418">Beachten Sie, dass beim Aufheben der Veröffentlichung eines App-V-Pakets vom Verwaltungs Server keine Entfernungs Operation durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="14981-418">Remember that unpublishing an App-V Package from the Management Server does not perform a Remove operation.</span></span> <span data-ttu-id="14981-419">Bei keinem Vorgang werden die Paketspeicher Paketdateien entfernt.</span><span class="sxs-lookup"><span data-stu-id="14981-419">Neither operation will remove the Package Store package files.</span></span>

## <a href="" id="bkmk-roaming-reg-data"></a><span data-ttu-id="14981-420">Roaming-Registrierung und Daten</span><span class="sxs-lookup"><span data-stu-id="14981-420">Roaming registry and data</span></span>


<span data-ttu-id="14981-421">App-V 5 ist in der Lage, in Abhängigkeit davon, wie die verwendete Anwendung geschrieben wird, beim Roaming eine nahezu native Umgebung bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="14981-421">App-V 5 is able to provide a near-native experience when roaming, depending on how the application being used is written.</span></span> <span data-ttu-id="14981-422">Standardmäßig wird App-V auf der Grundlage der Roaming-Konfiguration des Betriebssystems APPDATA-Dateien durchlaufen, die am Roaming-Speicherort gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="14981-422">By default, App-V roams AppData that is stored in the roaming location, based on the roaming configuration of the operating system.</span></span> <span data-ttu-id="14981-423">Andere Speicherorte für die Speicherung dateibasierter Daten werden nicht von einem Computer zu einem Computer durchlaufen, da Sie sich an Speicherorten befinden, die nicht durchlaufen werden.</span><span class="sxs-lookup"><span data-stu-id="14981-423">Other locations for storage of file-based data do not roam from computer to computer, since they are in locations that are not roamed.</span></span>

### <a href="" id="bkmk-clt-inter-roam-reqs"></a><span data-ttu-id="14981-424">Roaming-Anforderungen und Datenspeicher für Benutzer Kataloge</span><span class="sxs-lookup"><span data-stu-id="14981-424">Roaming requirements and user catalog data storage</span></span>

<span data-ttu-id="14981-425">App-V speichert Daten, die den Zustand des Katalogs des Benutzers darstellen, in der folgenden Form:</span><span class="sxs-lookup"><span data-stu-id="14981-425">App-V stores data, which represents the state of the user’s catalog, in the form of:</span></span>

-   <span data-ttu-id="14981-426">Dateien unter%APPDATA%\\Microsoft\\AppV\\Client\\Catalog</span><span class="sxs-lookup"><span data-stu-id="14981-426">Files under %appdata%\\Microsoft\\AppV\\Client\\Catalog</span></span>

-   <span data-ttu-id="14981-427">Registrierungseinstellungen unter</span><span class="sxs-lookup"><span data-stu-id="14981-427">Registry settings under</span></span> `HKEY_CURRENT_USER\Software\Microsoft\AppV\Client\Packages`

<span data-ttu-id="14981-428">Zusammenstellen diese Dateien und Registrierungseinstellungen den Katalog des Benutzers dar, sodass entweder beide Roaming durchgeführt werden müssen, oder dass für einen bestimmten Benutzer kein Roaming durchgeführt werden muss.</span><span class="sxs-lookup"><span data-stu-id="14981-428">Together, these files and registry settings represent the user’s catalog, so either both must be roamed, or neither must be roamed for a given user.</span></span> <span data-ttu-id="14981-429">App-V unterstützt kein Roaming von% APPDATA%, aber nicht das Roaming des Benutzerprofils (Registrierung) oder umgekehrt.</span><span class="sxs-lookup"><span data-stu-id="14981-429">App-V does not support roaming %AppData%, but not roaming the user’s profile (registry), or vice versa.</span></span>

<span data-ttu-id="14981-430">**Hinweis**  Das Cmdlet **Repair-AppvClientPackage** repariert den Veröffentlichungsstatus von Paketen nicht, wobei der App-V-Zustand des Benutzers unter `HKEY_CURRENT_USER` fehlt oder mit den Daten in% APPDATA% nicht übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="14981-430">**Note** The **Repair-AppvClientPackage** cmdlet does not repair the publishing state of packages, where the user’s App-V state under `HKEY_CURRENT_USER` is missing or mismatched with the data in %appdata%.</span></span>

 

### <span data-ttu-id="14981-431">Registrierungsbasierte Daten</span><span class="sxs-lookup"><span data-stu-id="14981-431">Registry-based data</span></span>

<span data-ttu-id="14981-432">Das App-V-Registrierungs-Roaming fällt in zwei Szenarien, wie in der folgenden Tabelle dargestellt.</span><span class="sxs-lookup"><span data-stu-id="14981-432">App-V registry roaming falls into two scenarios, as shown in the following table.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="14981-433">Szenario</span><span class="sxs-lookup"><span data-stu-id="14981-433">Scenario</span></span></th>
<th align="left"><span data-ttu-id="14981-434">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="14981-434">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="14981-435">Anwendungen, die als Standardbenutzer ausgeführt werden</span><span class="sxs-lookup"><span data-stu-id="14981-435">Applications that are run as standard users</span></span></p></td>
<td align="left"><p><span data-ttu-id="14981-436">Wenn ein Standardbenutzer eine APP-v-Anwendung startet, werden sowohl HKLM-als auch HKCU für App-v-Anwendungen in der HKCU-Struktur auf dem Computer gespeichert.</span><span class="sxs-lookup"><span data-stu-id="14981-436">When a standard user launches an App-V application, both HKLM and HKCU for App-V applications are stored in the HKCU hive on the machine.</span></span> <span data-ttu-id="14981-437">Dies stellt zwei unterschiedliche Pfade dar:</span><span class="sxs-lookup"><span data-stu-id="14981-437">This presents as two distinct paths:</span></span></p>
<ul>
<li><p><span data-ttu-id="14981-438">HKLM: HKCU\SOFTWARE\Classes\AppV\Client\Packages {PkgGUID} \ REGISTRY\MACHINE\SOFTWARE</span><span class="sxs-lookup"><span data-stu-id="14981-438">HKLM: HKCU\SOFTWARE\Classes\AppV\Client\Packages{PkgGUID}\REGISTRY\MACHINE\SOFTWARE</span></span></p></li>
<li><p><span data-ttu-id="14981-439">HKCU: HKCU\SOFTWARE\Microsoft\AppV\Client\Packages {PkgGUID} \ REGISTRY\USER {Benutzer-Nr} \ Software</span><span class="sxs-lookup"><span data-stu-id="14981-439">HKCU: HKCU\SOFTWARE\Microsoft\AppV\Client\Packages{PkgGUID}\REGISTRY\USER{UserSID}\SOFTWARE</span></span></p></li>
</ul>
<p><span data-ttu-id="14981-440">Die Speicherorte sind für das Roaming auf der Grundlage der Betriebssystemeinstellungen aktiviert.</span><span class="sxs-lookup"><span data-stu-id="14981-440">The locations are enabled for roaming based on the operating system settings.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="14981-441">Anwendungen, die mit Elevation ausgeführt werden</span><span class="sxs-lookup"><span data-stu-id="14981-441">Applications that are run with elevation</span></span></p></td>
<td align="left"><p><span data-ttu-id="14981-442">Wenn eine Anwendung mit Elevation gestartet wird:</span><span class="sxs-lookup"><span data-stu-id="14981-442">When an application is launched with elevation:</span></span></p>
<ul>
<li><p><span data-ttu-id="14981-443">HKLM-Daten werden in der HKLM-Struktur auf dem lokalen Computer gespeichert.</span><span class="sxs-lookup"><span data-stu-id="14981-443">HKLM data is stored in the HKLM hive on the local computer</span></span></p></li>
<li><p><span data-ttu-id="14981-444">HKCU-Daten werden am Speicherort der Benutzerregistrierung gespeichert</span><span class="sxs-lookup"><span data-stu-id="14981-444">HKCU data is stored in the User Registry location</span></span></p></li>
</ul>
<p><span data-ttu-id="14981-445">In diesem Szenario werden diese Einstellungen nicht mit normalen Roaming-Konfigurationen des Betriebssystems durchlaufen, und die resultierenden Registrierungsschlüssel und-Werte werden an folgendem Speicherort gespeichert:</span><span class="sxs-lookup"><span data-stu-id="14981-445">In this scenario, these settings are not roamed with normal operating system roaming configurations, and the resulting registry keys and values are stored in the following location:</span></span></p>
<ul>
<li><p><span data-ttu-id="14981-446">HKLM\SOFTWARE\Microsoft\AppV\Client\Packages {PkgGUID} {Benutzer-Nr} \ REGISTRY\MACHINE\SOFTWARE</span><span class="sxs-lookup"><span data-stu-id="14981-446">HKLM\SOFTWARE\Microsoft\AppV\Client\Packages{PkgGUID}{UserSID}\REGISTRY\MACHINE\SOFTWARE</span></span></p></li>
<li><p><span data-ttu-id="14981-447">HKCU\SOFTWARE\Microsoft\AppV\Client\Packages {PkgGUID} \ Registry\User {Benutzer-Nr} \ Software</span><span class="sxs-lookup"><span data-stu-id="14981-447">HKCU\SOFTWARE\Microsoft\AppV\Client\Packages{PkgGUID}\Registry\User{UserSID}\SOFTWARE</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="14981-448">App-V und Ordnerumleitung</span><span class="sxs-lookup"><span data-stu-id="14981-448">App-V and folder redirection</span></span>

<span data-ttu-id="14981-449">App-V 5.0 SP2 unterstützt die Ordnerumleitung des Roaming-APPDATA-Ordners (% APPDATA%).</span><span class="sxs-lookup"><span data-stu-id="14981-449">App-V 5.0SP2 supports folder redirection of the roaming AppData folder (%AppData%).</span></span> <span data-ttu-id="14981-450">Wenn die virtuelle Umgebung gestartet wird, wird der Roaming-APPDATA-Zustand aus dem Roaming-AppData-Verzeichnis des Benutzers in den lokalen Cache kopiert.</span><span class="sxs-lookup"><span data-stu-id="14981-450">When the virtual environment is started, the roaming AppData state from the user’s roaming AppData directory is copied to the local cache.</span></span> <span data-ttu-id="14981-451">Umgekehrt wird beim Beenden der virtuellen Umgebung der lokale Cache, der dem Roaming-APPDATA eines bestimmten Benutzers zugeordnet ist, an den tatsächlichen Speicherort des Roaming-APPDATA-Verzeichnisses dieses Benutzers übertragen.</span><span class="sxs-lookup"><span data-stu-id="14981-451">Conversely, when the virtual environment is shut down, the local cache that is associated with a specific user’s roaming AppData is transferred to the actual location of that user’s roaming AppData directory.</span></span>

<span data-ttu-id="14981-452">Ein typisches Paket enthält mehrere Speicherorte, die im Sicherungsspeicher des Benutzers für Einstellungen in AppData\\Local und AppData\\Roaming. zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="14981-452">A typical package has several locations mapped in the user’s backing store for settings in both AppData\\Local and AppData\\Roaming.</span></span> <span data-ttu-id="14981-453">Bei diesen Speicherorten handelt es sich um die Kopie an Schreib Speicherorten, die pro Benutzer im Profil des Benutzers gespeichert werden und die zum Speichern von Änderungen an den Paket-VFS-Verzeichnissen und zum Schutz des Standardpakets VFS verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="14981-453">These locations are the Copy on Write locations that are stored per user in the user’s profile, and that are used to store changes made to the package VFS directories and to protect the default package VFS.</span></span>

<span data-ttu-id="14981-454">In der folgenden Tabelle sind lokale und Roaming-Speicherorte aufgeführt, wenn die Ordnerumleitung nicht implementiert wurde.</span><span class="sxs-lookup"><span data-stu-id="14981-454">The following table shows local and roaming locations, when folder redirection has not been implemented.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="14981-455">VFS-Verzeichnis im Paket</span><span class="sxs-lookup"><span data-stu-id="14981-455">VFS directory in package</span></span></th>
<th align="left"><span data-ttu-id="14981-456">Zugeordneter Speicherort des Sicherungsspeichers</span><span class="sxs-lookup"><span data-stu-id="14981-456">Mapped location of backing store</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="14981-457">ProgramFilesX86</span><span class="sxs-lookup"><span data-stu-id="14981-457">ProgramFilesX86</span></span></p></td>
<td align="left"><p><span data-ttu-id="14981-458">C:\users\jsmith\AppData &lt; Strong &gt; local </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID- &gt; \ProgramFilesX86</span><span class="sxs-lookup"><span data-stu-id="14981-458">C:\users\jsmith\AppData&lt;strong&gt;Local</strong>\Microsoft\AppV\Client\VFS&amp;lt;GUID&gt;\ProgramFilesX86</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="14981-459">SystemX86</span><span class="sxs-lookup"><span data-stu-id="14981-459">SystemX86</span></span></p></td>
<td align="left"><p><span data-ttu-id="14981-460">C:\users\jsmith\AppData &lt; Strong &gt; local </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID- &gt; \SystemX86</span><span class="sxs-lookup"><span data-stu-id="14981-460">C:\users\jsmith\AppData&lt;strong&gt;Local</strong>\Microsoft\AppV\Client\VFS&amp;lt;GUID&gt;\SystemX86</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="14981-461">Windows</span><span class="sxs-lookup"><span data-stu-id="14981-461">Windows</span></span></p></td>
<td align="left"><p><span data-ttu-id="14981-462">C:\users\jsmith\AppData &lt; Strong &gt; local </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt;</span><span class="sxs-lookup"><span data-stu-id="14981-462">C:\users\jsmith\AppData&lt;strong&gt;Local</strong>\Microsoft\AppV\Client\VFS&amp;lt;GUID&gt;\Windows</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="14981-463">appv_ROOT</span><span class="sxs-lookup"><span data-stu-id="14981-463">appv_ROOT</span></span></p></td>
<td align="left"><p><span data-ttu-id="14981-464">C:\users\jsmith\AppData &lt; Strong &gt; local </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \ appv_ROOT</span><span class="sxs-lookup"><span data-stu-id="14981-464">C:\users\jsmith\AppData&lt;strong&gt;Local</strong>\Microsoft\AppV\Client\VFS&amp;lt;GUID&gt;\appv_ROOT</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="14981-465">APPDATA</span><span class="sxs-lookup"><span data-stu-id="14981-465">AppData</span></span></p></td>
<td align="left"><p><span data-ttu-id="14981-466">C:\users\jsmith\AppData &lt; Strong &gt; Roaming </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID- &gt; \AppData</span><span class="sxs-lookup"><span data-stu-id="14981-466">C:\users\jsmith\AppData&lt;strong&gt;Roaming</strong>\Microsoft\AppV\Client\VFS&amp;lt;GUID&gt;\AppData</span></span></p></td>
</tr>
</tbody>
</table>

 

 

<span data-ttu-id="14981-467">In der folgenden Tabelle sind lokale und Roaming-Speicherorte aufgeführt, wenn die Ordnerumleitung für% APPDATA% implementiert wurde und der Standort umgeleitet wurde (in der Regel an einen Netzwerkspeicherort).</span><span class="sxs-lookup"><span data-stu-id="14981-467">The following table shows local and roaming locations, when folder redirection has been implemented for %AppData%, and the location has been redirected (typically to a network location).</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="14981-468">VFS-Verzeichnis im Paket</span><span class="sxs-lookup"><span data-stu-id="14981-468">VFS directory in package</span></span></th>
<th align="left"><span data-ttu-id="14981-469">Zugeordneter Speicherort des Sicherungsspeichers</span><span class="sxs-lookup"><span data-stu-id="14981-469">Mapped location of backing store</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="14981-470">ProgramFilesX86</span><span class="sxs-lookup"><span data-stu-id="14981-470">ProgramFilesX86</span></span></p></td>
<td align="left"><p><span data-ttu-id="14981-471">C:\users\jsmith\AppData &lt; Strong &gt; local </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID- &gt; \ProgramFilesX86</span><span class="sxs-lookup"><span data-stu-id="14981-471">C:\users\jsmith\AppData&lt;strong&gt;Local</strong>\Microsoft\AppV\Client\VFS&amp;lt;GUID&gt;\ProgramFilesX86</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="14981-472">SystemX86</span><span class="sxs-lookup"><span data-stu-id="14981-472">SystemX86</span></span></p></td>
<td align="left"><p><span data-ttu-id="14981-473">C:\users\jsmith\AppData &lt; Strong &gt; local </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID- &gt; \SystemX86</span><span class="sxs-lookup"><span data-stu-id="14981-473">C:\users\jsmith\AppData&lt;strong&gt;Local</strong>\Microsoft\AppV\Client\VFS&amp;lt;GUID&gt;\SystemX86</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="14981-474">Windows</span><span class="sxs-lookup"><span data-stu-id="14981-474">Windows</span></span></p></td>
<td align="left"><p><span data-ttu-id="14981-475">C:\users\jsmith\AppData &lt; Strong &gt; local </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt;</span><span class="sxs-lookup"><span data-stu-id="14981-475">C:\users\jsmith\AppData&lt;strong&gt;Local</strong>\Microsoft\AppV\Client\VFS&amp;lt;GUID&gt;\Windows</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="14981-476">appv_ROOT</span><span class="sxs-lookup"><span data-stu-id="14981-476">appv_ROOT</span></span></p></td>
<td align="left"><p><span data-ttu-id="14981-477">C:\users\jsmith\AppData &lt; Strong &gt; local </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \ appv_ROOT</span><span class="sxs-lookup"><span data-stu-id="14981-477">C:\users\jsmith\AppData&lt;strong&gt;Local</strong>\Microsoft\AppV\Client\VFS&amp;lt;GUID&gt;\appv_ROOT</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="14981-478">APPDATA</span><span class="sxs-lookup"><span data-stu-id="14981-478">AppData</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="14981-479">\Fileserver </strong> \users\jsmith\roaming\Microsoft\AppV\Client\VFS &amp; lt; GUID- &gt; \AppData</span><span class="sxs-lookup"><span data-stu-id="14981-479">\Fileserver</strong>\users\jsmith\roaming\Microsoft\AppV\Client\VFS&amp;lt;GUID&gt;\AppData</span></span></p></td>
</tr>
</tbody>
</table>

 

 

<span data-ttu-id="14981-480">Der aktuelle App-v-Client-VFS-Treiber kann nicht in Netzwerkspeicherorte schreiben, sodass der APP-v-Client das vorhanden sein einer Ordnerumleitung erkennt und die Daten auf dem lokalen Laufwerk während der Veröffentlichung und beim Starten der virtuellen Umgebung kopiert.</span><span class="sxs-lookup"><span data-stu-id="14981-480">The current App-V Client VFS driver cannot write to network locations, so the App-V Client detects the presence of folder redirection and copies the data on the local drive during publishing and when the virtual environment starts.</span></span> <span data-ttu-id="14981-481">Nachdem der Benutzer die APP-v-Anwendung geschlossen hat und der APP-v-Client die virtuelle Umgebung geschlossen hat, wird der lokale Speicher des VFS-APPDATA wieder in das Netzwerk kopiert, sodass Roaming auf weiteren Computern möglich ist, in denen der Vorgang wiederholt wird.</span><span class="sxs-lookup"><span data-stu-id="14981-481">After the user closes the App-V application and the App-V Client closes the virtual environment, the local storage of the VFS AppData is copied back to the network, enabling roaming to additional machines, where the process will be repeated.</span></span> <span data-ttu-id="14981-482">Die detaillierten Schritte der Prozesse sind:</span><span class="sxs-lookup"><span data-stu-id="14981-482">The detailed steps of the processes are:</span></span>

1.  <span data-ttu-id="14981-483">Während des Starts der Veröffentlichung oder virtuellen Umgebung erkennt der App-V-Client den Speicherort des APPDATA-Verzeichnisses.</span><span class="sxs-lookup"><span data-stu-id="14981-483">During publishing or virtual environment startup, the App-V Client detects the location of the AppData directory.</span></span>

2.  <span data-ttu-id="14981-484">Wenn der Roaming-APPDATA-Pfad lokal ist oder Ino AppData\\Roaming Standort zugeordnet ist, geschieht nichts.</span><span class="sxs-lookup"><span data-stu-id="14981-484">If the roaming AppData path is local or ino AppData\\Roaming location is mapped, nothing happens.</span></span>

3.  <span data-ttu-id="14981-485">Wenn der Roaming-APPDATA-Pfad nicht lokal ist, wird das VFS-AppData-Verzeichnis dem lokalen AppData-Verzeichnis zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="14981-485">If the roaming AppData path is not local, the VFS AppData directory is mapped to the local AppData directory.</span></span>

<span data-ttu-id="14981-486">Durch diesen Vorgang wird das Problem eines nicht lokalen% APPDATA% behoben, das vom App-V-Client-VFS-Treiber nicht unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="14981-486">This process solves the problem of a non-local %AppData% that is not supported by the App-V Client VFS driver.</span></span> <span data-ttu-id="14981-487">Die in diesem neuen Speicherort gespeicherten Daten werden jedoch nicht mit der Ordnerumleitung durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="14981-487">However, the data stored in this new location is not roamed with folder redirection.</span></span> <span data-ttu-id="14981-488">Alle Änderungen während der Ausführung der Anwendung erfolgen am lokalen APPDATA-Speicherort und müssen in den umgeleiteten Speicherort kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="14981-488">All changes during the running of the application happen to the local AppData location and must be copied to the redirected location.</span></span> <span data-ttu-id="14981-489">Die detaillierten Schritte dieses Prozesses sind:</span><span class="sxs-lookup"><span data-stu-id="14981-489">The detailed steps of this process are:</span></span>

1.  <span data-ttu-id="14981-490">App-V-Anwendung wird heruntergefahren, wodurch die virtuelle Umgebung beendet wird.</span><span class="sxs-lookup"><span data-stu-id="14981-490">App-V application is shut down, which shuts down the virtual environment.</span></span>

2.  <span data-ttu-id="14981-491">Der lokale Cache des Roaming-APPDATA-Speicherorts wird komprimiert und in einer ZIP-Datei gespeichert.</span><span class="sxs-lookup"><span data-stu-id="14981-491">The local cache of the roaming AppData location is compressed and stored in a ZIP file.</span></span>

3.  <span data-ttu-id="14981-492">Ein Zeitstempel am Ende des ZIP-Verpackungsprozesses wird verwendet, um die Datei zu benennen.</span><span class="sxs-lookup"><span data-stu-id="14981-492">A timestamp at the end of the ZIP packaging process is used to name the file.</span></span>

4.  <span data-ttu-id="14981-493">Der Zeitstempel wird in der Registrierung aufgezeichnet: HKEY \ _CURRENT \ _User \\software\\microsoft\\appv\\client\\packages\\ &lt; GUID &gt; \\AppDataTime als letzten bekannten APPDATA-Zeitstempel.</span><span class="sxs-lookup"><span data-stu-id="14981-493">The timestamp is recorded in the registry: HKEY\_CURRENT\_USER\\Software\\Microsoft\\AppV\\Client\\Packages\\&lt;GUID&gt;\\AppDataTime as the last known AppData timestamp.</span></span>

5.  <span data-ttu-id="14981-494">Der Ordner-Umleitungsprozess wird aufgerufen, um die ZIP-Datei auszuwerten und zu initiieren, die in das Roaming AppData-Verzeichnis hochgeladen wurde.</span><span class="sxs-lookup"><span data-stu-id="14981-494">The folder redirection process is called to evaluate and initiate the ZIP file uploaded to the roaming AppData directory.</span></span>

<span data-ttu-id="14981-495">Der timestamp wird verwendet, um ein Szenario des letzten Writer-WINS-Szenarios zu ermitteln, wenn ein Konflikt vorliegt, der zum Optimieren des Downloads der Daten verwendet wird, wenn die App-V-Anwendung veröffentlicht wird oder die virtuelle Umgebung gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="14981-495">The timestamp is used to determine a “last writer wins” scenario if there is a conflict and is used to optimize the download of the data when the App-V application is published or the virtual environment is started.</span></span> <span data-ttu-id="14981-496">Durch die Ordnerumleitung werden die Daten von allen anderen Clients zur Verfügung gestellt, die unter die unterstützende Richtlinie fallen, und der Vorgang zum Speichern der AppData\\Roaming-Daten am lokalen APPDATA-Speicherort auf dem Client wird initiiert.</span><span class="sxs-lookup"><span data-stu-id="14981-496">Folder redirection will make the data available from any other clients covered by the supporting policy and will initiate the process of storing the AppData\\Roaming data to the local AppData location on the client.</span></span> <span data-ttu-id="14981-497">Die detaillierten Prozesse sind:</span><span class="sxs-lookup"><span data-stu-id="14981-497">The detailed processes are:</span></span>

1.  <span data-ttu-id="14981-498">Der Benutzer startet die virtuelle Umgebung, indem er eine Anwendung startet.</span><span class="sxs-lookup"><span data-stu-id="14981-498">The user starts the virtual environment by starting an application.</span></span>

2.  <span data-ttu-id="14981-499">Die virtuelle Umgebung der Anwendung überprüft, falls vorhanden, die neueste ZIP-Datei mit Zeitstempel.</span><span class="sxs-lookup"><span data-stu-id="14981-499">The application’s virtual environment checks for the most recent time stamped ZIP file, if present.</span></span>

3.  <span data-ttu-id="14981-500">Sofern vorhanden, wird die Registrierung auf den letzten bekannt geladenen Timestamp überprüft.</span><span class="sxs-lookup"><span data-stu-id="14981-500">The registry is checked for the last known uploaded timestamp, if present.</span></span>

4.  <span data-ttu-id="14981-501">Die neueste ZIP-Datei wird heruntergeladen, es sei denn, der lokale letzte bekannte Upload-Zeitstempel ist größer als oder gleich dem Timestamp aus der ZIP-Datei.</span><span class="sxs-lookup"><span data-stu-id="14981-501">The most recent ZIP file is downloaded unless the local last known upload timestamp is greater than or equal to the timestamp from the ZIP file.</span></span>

5.  <span data-ttu-id="14981-502">Wenn der lokale letzte bekannte Upload-Zeitstempel vor der letzten ZIP-Datei im Roaming-APPDATA-Speicherort liegt, wird die ZIP-Datei in das lokale temporäre Verzeichnis im Profil des Benutzers extrahiert.</span><span class="sxs-lookup"><span data-stu-id="14981-502">If the local last known upload timestamp is earlier than that of the most recent ZIP file in the roaming AppData location, the ZIP file is extracted to the local temp directory in the user’s profile.</span></span>

6.  <span data-ttu-id="14981-503">Nachdem die ZIP-Datei erfolgreich extrahiert wurde, wird der lokale Cache des Roaming-APPDATA-Verzeichnisses umbenannt, und die neuen Daten werden in Position verschoben.</span><span class="sxs-lookup"><span data-stu-id="14981-503">After the ZIP file is successfully extracted, the local cache of the roaming AppData directory is renamed and the new data is moved into place.</span></span>

7.  <span data-ttu-id="14981-504">Das umbenannte Verzeichnis wird gelöscht, und die Anwendung wird mit den zuletzt gespeicherten Roaming-APPDATA-Daten geöffnet.</span><span class="sxs-lookup"><span data-stu-id="14981-504">The renamed directory is deleted and the application opens with the most recently saved roaming AppData data.</span></span>

<span data-ttu-id="14981-505">Dadurch wird das erfolgreiche Roaming von Anwendungseinstellungen abgeschlossen, die in AppData\\Roaming-Speicherorten vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="14981-505">This completes the successful roaming of application settings that are present in AppData\\Roaming locations.</span></span> <span data-ttu-id="14981-506">Die einzige andere Bedingung, die behoben werden muss, ist ein Paket Reparaturvorgang.</span><span class="sxs-lookup"><span data-stu-id="14981-506">The only other condition that must be addressed is a package repair operation.</span></span> <span data-ttu-id="14981-507">Die Details des Prozesses lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="14981-507">The details of the process are:</span></span>

1.  <span data-ttu-id="14981-508">Ermitteln Sie während der Reparatur, ob der Pfad zum Roaming-AppData-Verzeichnis des Benutzers nicht lokal ist.</span><span class="sxs-lookup"><span data-stu-id="14981-508">During repair, detect if the path to the user’s roaming AppData directory is not local.</span></span>

2.  <span data-ttu-id="14981-509">Karte die nicht lokalen Roaming-APPDATA-Pfad Ziele werden die erwarteten Roaming-und lokalen APPDATA-Speicherorte neu erstellt.</span><span class="sxs-lookup"><span data-stu-id="14981-509">Map the non-local roaming AppData path targets are recreated the expected roaming and local AppData locations.</span></span>

3.  <span data-ttu-id="14981-510">Löschen Sie den in der Registrierung gespeicherten Zeitstempel, falls vorhanden.</span><span class="sxs-lookup"><span data-stu-id="14981-510">Delete the timestamp stored in the registry, if present.</span></span>

<span data-ttu-id="14981-511">Durch diesen Vorgang werden sowohl die lokale als auch die Netzwerkspeicherorte für APPDATA neu erstellt, und der Registrierungseintrag des Zeitstempels wird entfernt.</span><span class="sxs-lookup"><span data-stu-id="14981-511">This process will re-create both the local and network locations for AppData and remove the registry record of the timestamp.</span></span>

## <a href="" id="bkmk-clt-app-lifecycle"></a><span data-ttu-id="14981-512">App-V Client Application Lifecycle Management</span><span class="sxs-lookup"><span data-stu-id="14981-512">App-V client application lifecycle management</span></span>


<span data-ttu-id="14981-513">In einer vollständigen APP-v-Infrastruktur werden nach der Sequenzierung von Anwendungen verwaltet und auf Benutzern oder Computern über die APP-v-Verwaltungs-und Veröffentlichungsserver veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="14981-513">In an App-V Full Infrastructure, after applications are sequenced they are managed and published to users or computers via the App-V Management and Publishing servers.</span></span> <span data-ttu-id="14981-514">In diesem Abschnitt werden die Vorgänge erläutert, die während der gemeinsamen App-v-Anwendungslebenszyklus Vorgänge (hinzufügen, veröffentlichen, starten, aktualisieren und entfernen) sowie der Datei-und Registrierungsspeicherorte auftreten, die aus der Perspektive des App-v-Clients geändert und geändert werden.</span><span class="sxs-lookup"><span data-stu-id="14981-514">This section details the operations that occur during the common App-V application lifecycle operations (Add, publishing, launch, upgrade, and removal) and the file and registry locations that are changed and modified from the App-V Client perspective.</span></span> <span data-ttu-id="14981-515">Die APP-v-Client Vorgänge werden als eine Reihe von PowerShell-Befehlen ausgeführt, die auf dem Computer mit dem App-v-Client initiiert wurden.</span><span class="sxs-lookup"><span data-stu-id="14981-515">The App-V Client operations are performed as a series of PowerShell commands initiated on the computer running the App-V Client.</span></span>

<span data-ttu-id="14981-516">Dieses Dokument befasst sich mit den vollständigen Infrastrukturlösungen von App V.</span><span class="sxs-lookup"><span data-stu-id="14981-516">This document focuses on App-V Full Infrastructure solutions.</span></span> <span data-ttu-id="14981-517">Spezifische Informationen zur App-V-Integration in Configuration Manager 2012 finden Sie unter: <https://go.microsoft.com/fwlink/?LinkId=392773> .</span><span class="sxs-lookup"><span data-stu-id="14981-517">For specific information on App-V Integration with Configuration Manager 2012 visit: <https://go.microsoft.com/fwlink/?LinkId=392773>.</span></span>

<span data-ttu-id="14981-518">Die Aufgaben des App-V-Anwendungslebenszyklus werden bei der Benutzeranmeldung (Standardeinstellung), beim Start des Computers oder als zeitgesteuerte Vorgänge im Hintergrund ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="14981-518">The App-V application lifecycle tasks are triggered at user login (default), machine startup, or as background timed operations.</span></span> <span data-ttu-id="14981-519">Die Einstellungen für die App-V-Client Vorgänge, einschließlich Veröffentlichungsserver, Aktualisierungsintervalle, Paket Skriptaktivierung und andere, werden während des Setups des Clients oder nach dem Setup mit PowerShell-Befehlen konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="14981-519">The settings for the App-V Client operations, including Publishing Servers, refresh intervals, package script enablement, and others, are configured during setup of the client or post-setup with PowerShell commands.</span></span> <span data-ttu-id="14981-520">Weitere Informationen finden Sie unter Vorgehensweise zum Bereitstellen des Clients auf der TechNet-Seite unter: [Bereitstellen des App-V-Clients](how-to-deploy-the-app-v-client-gb18030.md) oder verwenden der PowerShell:</span><span class="sxs-lookup"><span data-stu-id="14981-520">See the How to Deploy the Client section on TechNet at: [How to Deploy the App-V Client](how-to-deploy-the-app-v-client-gb18030.md) or utilize the PowerShell:</span></span>

```powershell
get-command *appv*
```

### <span data-ttu-id="14981-521">Veröffentlichungsaktualisierung</span><span class="sxs-lookup"><span data-stu-id="14981-521">Publishing refresh</span></span>

<span data-ttu-id="14981-522">Der Veröffentlichungs Aktualisierungsprozess umfasst mehrere kleinere Vorgänge, die auf dem App-V-Client ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="14981-522">The publishing refresh process is comprised of several smaller operations that are performed on the App-V Client.</span></span> <span data-ttu-id="14981-523">Da es sich bei App-V um eine Application Virtualization-Technologie und nicht um eine Vorgangs Planungstechnologie handelt, wird der Windows-Taskplaner verwendet, um den Prozess bei der Benutzeranmeldung, beim Starten des Computers und in geplanten Intervallen zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="14981-523">Since App-V is an application virtualization technology and not a task scheduling technology, the Windows Task Scheduler is utilized to enable the process at user logon, machine startup, and at scheduled intervals.</span></span> <span data-ttu-id="14981-524">Die Konfiguration des Clients während des oben aufgeführten Setups ist die bevorzugte Methode beim Verteilen des Clients an eine große Gruppe von Computern mit den richtigen Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="14981-524">The configuration of the client during setup listed above is the preferred method when distributing the client to a large group of computers with the correct settings.</span></span> <span data-ttu-id="14981-525">Diese Clienteinstellungen können mit den folgenden PowerShell-Cmdlets konfiguriert werden:</span><span class="sxs-lookup"><span data-stu-id="14981-525">These client settings can be configured with the following PowerShell cmdlets:</span></span>

-   <span data-ttu-id="14981-526">**Add-AppVPublishingServer:** Konfiguriert den Client mit einem App-v-Veröffentlichungs Server, der APP-v-Pakete bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="14981-526">**Add-AppVPublishingServer:** Configures the client with an App-V Publishing Server that provides App-V packages.</span></span>

-   <span data-ttu-id="14981-527">**Satz-AppVPublishingServer:** Ändert die aktuellen Einstellungen für den App-V-Veröffentlichungs Server.</span><span class="sxs-lookup"><span data-stu-id="14981-527">**Set-AppVPublishingServer:** Modifies the current settings for the App-V Publishing Server.</span></span>

-   <span data-ttu-id="14981-528">**Satz-AppVClientConfiguration:** Ändert die aktuelle Einstellungen für den App-V-Client.</span><span class="sxs-lookup"><span data-stu-id="14981-528">**Set-AppVClientConfiguration:** Modifies the currents settings for the App-V Client.</span></span>

-   <span data-ttu-id="14981-529">**Sync-AppVPublishingServer:** Initiiert einen Aktualisierungsvorgang für die App-V-Veröffentlichung manuell.</span><span class="sxs-lookup"><span data-stu-id="14981-529">**Sync-AppVPublishingServer:** Initiates an App-V Publishing Refresh process manually.</span></span> <span data-ttu-id="14981-530">Dies wird auch in den geplanten Aufgaben verwendet, die während der Konfiguration des Veröffentlichungsservers erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="14981-530">This is also utilized in the scheduled tasks created during configuration of the publishing server.</span></span>

<span data-ttu-id="14981-531">Im Fokus der folgenden Abschnitte finden Sie Informationen zu den Vorgängen, die in verschiedenen Phasen einer App-V-Veröffentlichungsaktualisierung ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="14981-531">The focus of the following sections is to detail the operations that occur during different phases of an App-V Publishing Refresh.</span></span> <span data-ttu-id="14981-532">Zu den Themen gehören:</span><span class="sxs-lookup"><span data-stu-id="14981-532">The topics include:</span></span>

-   <span data-ttu-id="14981-533">Hinzufügen eines App-V-Pakets</span><span class="sxs-lookup"><span data-stu-id="14981-533">Adding an App-V Package</span></span>

-   <span data-ttu-id="14981-534">Veröffentlichen eines App-V-Pakets</span><span class="sxs-lookup"><span data-stu-id="14981-534">Publishing an App-V Package</span></span>

### <span data-ttu-id="14981-535">Hinzufügen eines App-V-Pakets</span><span class="sxs-lookup"><span data-stu-id="14981-535">Adding an App-V package</span></span>

<span data-ttu-id="14981-536">Das Hinzufügen eines App-V-Pakets zum Client ist der erste Schritt des Veröffentlichungs Aktualisierungsprozesses.</span><span class="sxs-lookup"><span data-stu-id="14981-536">Adding an App-V package to the client is the first step of the publishing refresh process.</span></span> <span data-ttu-id="14981-537">Das Endergebnis ist mit dem `Add-AppVClientPackage` Cmdlet in PowerShell identisch, mit der Ausnahme, dass der konfigurierte Veröffentlichungsserver mit Ausnahme des Veröffentlichungs Aktualisierungs Add-Vorgangs kontaktiert wird und eine Liste der Anwendungen auf höherer Ebene zurück an den Client übergibt, um detailliertere Informationen und nicht einen einzelnen Paket-Add-Vorgang abzurufen.</span><span class="sxs-lookup"><span data-stu-id="14981-537">The end result is the same as the `Add-AppVClientPackage` cmdlet in PowerShell, except during the publishing refresh add process, the configured publishing server is contacted and passes a high-level list of applications back to the client to pull more detailed information and not a single package add operation.</span></span> <span data-ttu-id="14981-538">Der Prozess wird fortgesetzt, indem der Client für Paket-oder Verbindungsgruppen Erweiterungen oder-Updates konfiguriert und dann auf die AppV-Datei zugegriffen wird.</span><span class="sxs-lookup"><span data-stu-id="14981-538">The process continues by configuring the client for package or connection group additions or updates, then accesses the appv file.</span></span> <span data-ttu-id="14981-539">Als nächstes werden die Inhalte der AppV-Datei erweitert und auf dem lokalen Betriebssystem an den entsprechenden Speicherorten gespeichert.</span><span class="sxs-lookup"><span data-stu-id="14981-539">Next, the contents of the appv file are expanded and placed on the local operating system in the appropriate locations.</span></span> <span data-ttu-id="14981-540">Im folgenden finden Sie einen detaillierten Workflow des Prozesses, vorausgesetzt, das Paket ist für das Fehler Streaming konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="14981-540">The following is a detailed workflow of the process, assuming the package is configured for Fault Streaming.</span></span>

**<span data-ttu-id="14981-541">Hinzufügen eines App-V-Pakets</span><span class="sxs-lookup"><span data-stu-id="14981-541">How to add an App-V package</span></span>**

1.  <span data-ttu-id="14981-542">Manuelle Initiierung über PowerShell oder Task Sequenz Initiierung des Veröffentlichungs Aktualisierungsprozesses.</span><span class="sxs-lookup"><span data-stu-id="14981-542">Manual initiation via PowerShell or Task Sequence initiation of the Publishing Refresh process.</span></span>

    1.  <span data-ttu-id="14981-543">Der App-V-Client erstellt eine HTTP-Verbindung und fordert eine Liste der auf dem Ziel basierenden Anwendungen an.</span><span class="sxs-lookup"><span data-stu-id="14981-543">The App-V Client makes an HTTP connection and requests a list of applications based on the target.</span></span> <span data-ttu-id="14981-544">Der Veröffentlichungs Aktualisierungsprozess unterstützt die Zielgruppenadressierung von Computern oder Benutzern.</span><span class="sxs-lookup"><span data-stu-id="14981-544">The Publishing refresh process supports targeting machines or users.</span></span>

    2.  <span data-ttu-id="14981-545">Der App-V-Veröffentlichungs Server verwendet die Identität des initiierenden Ziels, Benutzers oder Computers und fragt die Datenbank nach einer Liste der berechtigten Anwendungen ab.</span><span class="sxs-lookup"><span data-stu-id="14981-545">The App-V Publishing Server uses the identity of the initiating target, user or machine, and queries the database for a list of entitled applications.</span></span> <span data-ttu-id="14981-546">Die Liste der Anwendungen wird als XML-Antwort bereitgestellt, die der Client zum Senden zusätzlicher Anforderungen an den Server verwendet, um weitere Informationen pro Paket zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="14981-546">The list of applications is provided as an XML response, which the client uses to send additional requests to the server for more information on a per package basis.</span></span>

2.  <span data-ttu-id="14981-547">Der Veröffentlichungs-Agent auf dem App-V-Client führt alle unter serialisierten Aktionen aus.</span><span class="sxs-lookup"><span data-stu-id="14981-547">The Publishing Agent on the App-V Client performs all actions below serialized.</span></span>

    <span data-ttu-id="14981-548">Bewerten Sie alle Verbindungsgruppen, die nicht veröffentlicht oder deaktiviert sind, da Paketversions Updates, die Teil der Verbindungsgruppe sind, nicht verarbeitet werden können.</span><span class="sxs-lookup"><span data-stu-id="14981-548">Evaluate any connection groups that are unpublished or disabled, since package version updates that are part of the connection group cannot be processed.</span></span>

3.  <span data-ttu-id="14981-549">Konfigurieren Sie die Pakete, indem Sie einen Add-oder Update-Vorgang identifizieren.</span><span class="sxs-lookup"><span data-stu-id="14981-549">Configure the packages by identifying an Add or Update operations.</span></span>

    1.  <span data-ttu-id="14981-550">Der App-V-Client verwendet die AppX-API von Windows und greift auf die AppV-Datei vom Veröffentlichungsserver zu.</span><span class="sxs-lookup"><span data-stu-id="14981-550">The App-V Client utilizes the AppX API from Windows and accesses the appv file from the publishing server.</span></span>

    2.  <span data-ttu-id="14981-551">Die Paketdatei wird geöffnet, und die AppXManifest.xml und StreamMap.xml werden in den Paketspeicher heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="14981-551">The package file is opened and the AppXManifest.xml and StreamMap.xml are downloaded to the Package Store.</span></span>

    3.  <span data-ttu-id="14981-552">Vollständiges Streamen von Veröffentlichungs Blockdaten, die im StreamMap.xml definiert sind.</span><span class="sxs-lookup"><span data-stu-id="14981-552">Completely stream publishing block data defined in the StreamMap.xml.</span></span> <span data-ttu-id="14981-553">Speichert die Veröffentlichungs Blockdaten im Paket Store\\PkgGUID\\VerGUID\\Root.</span><span class="sxs-lookup"><span data-stu-id="14981-553">Stores the publishing block data in the Package Store\\PkgGUID\\VerGUID\\Root.</span></span>

        -   <span data-ttu-id="14981-554">Symbole: Ziele von Erweiterungspunkten.</span><span class="sxs-lookup"><span data-stu-id="14981-554">Icons: Targets of extension points.</span></span>

        -   <span data-ttu-id="14981-555">Portable ausführbare Header (PE-Header): Ziele von Erweiterungspunkten, die die Basisinformationen zum Bild benötigen, auf einem Datenträger, auf den direkt zugegriffen wird, oder über Dateitypen.</span><span class="sxs-lookup"><span data-stu-id="14981-555">Portable Executable Headers (PE Headers): Targets of extension points that contain the base information about the image need on disk, directly accessed or via file types.</span></span>

        -   <span data-ttu-id="14981-556">Skripts: Download des Skripts-Verzeichnisses zur Verwendung im gesamten Veröffentlichungsprozess.</span><span class="sxs-lookup"><span data-stu-id="14981-556">Scripts: Download scripts directory for use throughout the publishing process.</span></span>

    4.  <span data-ttu-id="14981-557">Füllen Sie den Paketspeicher aus:</span><span class="sxs-lookup"><span data-stu-id="14981-557">Populate the Package store:</span></span>

        1.  <span data-ttu-id="14981-558">Erstellen Sie Dateien mit geringer Dichte auf einem Datenträger, die das extrahierte Paket für alle aufgelisteten Verzeichnisse darstellen.</span><span class="sxs-lookup"><span data-stu-id="14981-558">Create sparse files on disk that represent the extracted package for any directories listed.</span></span>

        2.  <span data-ttu-id="14981-559">Stufen Sie Dateien und Verzeichnisse der obersten Ebene unter root ein.</span><span class="sxs-lookup"><span data-stu-id="14981-559">Stage top level files and directories under root.</span></span>

        3.  <span data-ttu-id="14981-560">Alle anderen Dateien werden erstellt, wenn das Verzeichnis auf dem Datenträger als "spärlich" aufgeführt und bei Bedarf gestreamt wird.</span><span class="sxs-lookup"><span data-stu-id="14981-560">All other files are created when the directory is listed as sparse on disk and streamed on demand.</span></span>

    5.  <span data-ttu-id="14981-561">Erstellen Sie die Einträge des Computer Katalogs.</span><span class="sxs-lookup"><span data-stu-id="14981-561">Create the machine catalog entries.</span></span> <span data-ttu-id="14981-562">Erstellen Sie die Manifest.xml und DeploymentConfiguration.xml aus den Paketdateien (wenn keine DeploymentConfiguration.xml Datei im Paket ein Platzhalter erstellt wird).</span><span class="sxs-lookup"><span data-stu-id="14981-562">Create the Manifest.xml and DeploymentConfiguration.xml from the package files (if no DeploymentConfiguration.xml file in the package a placeholder is created).</span></span>

    6.  <span data-ttu-id="14981-563">Erstellen des Speicherorts des Paketspeichers in der Registrierungs-HKLM\\Software\\Microsoft\\AppV\\Client\\Packages\\PkgGUID\\Versions\\VerGUID\\Catalog</span><span class="sxs-lookup"><span data-stu-id="14981-563">Create location of the package store in the registry HKLM\\Software\\Microsoft\\AppV\\Client\\Packages\\PkgGUID\\Versions\\VerGUID\\Catalog</span></span>

    7.  <span data-ttu-id="14981-564">Erstellen Sie die Datei "Registry. dat" aus dem Paketspeicher auf%ProgramData%\\Microsoft\\AppV\\Client\\VReg\\ {VersionGUID}. dat</span><span class="sxs-lookup"><span data-stu-id="14981-564">Create the Registry.dat file from the package store to %ProgramData%\\Microsoft\\AppV\\Client\\VReg\\{VersionGUID}.dat</span></span>

    8.  <span data-ttu-id="14981-565">Registrieren des Pakets mit dem App-V-Kernel Modus-Treiber HKLM\\Microsoft\\Software\\AppV\\MAV</span><span class="sxs-lookup"><span data-stu-id="14981-565">Register the package with the App-V Kernel Mode Driver HKLM\\Microsoft\\Software\\AppV\\MAV</span></span>

    9.  <span data-ttu-id="14981-566">Rufen Sie Skripting aus der AppxManifest.xml oder DeploymentConfig.xml Datei auf, um die Anzeigedauer für das Paket hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="14981-566">Invoke scripting from the AppxManifest.xml or DeploymentConfig.xml file for Package Add timing.</span></span>

4.  <span data-ttu-id="14981-567">Konfigurieren Sie Verbindungsgruppen durch Hinzufügen und aktivieren oder deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="14981-567">Configure Connection Groups by adding and enabling or disabling.</span></span>

5.  <span data-ttu-id="14981-568">Entfernen Sie Objekte, die nicht auf dem Ziel veröffentlicht sind (Benutzer oder Computer).</span><span class="sxs-lookup"><span data-stu-id="14981-568">Remove objects that are not published to the target (user or machine).</span></span>

    <span data-ttu-id="14981-569">**Hinweis**  Dadurch wird keine Paketlöschung durchgeführt, sondern es werden vielmehr Integrationspunkte für das jeweilige Ziel (Benutzer oder Computer) entfernt und Benutzer Katalogdateien (Computer Katalogdateien für Global veröffentlicht) entfernt.</span><span class="sxs-lookup"><span data-stu-id="14981-569">**Note** This will not perform a package deletion but rather remove integration points for the specific target (user or machine) and remove user catalog files (machine catalog files for globally published).</span></span>

     

6.  <span data-ttu-id="14981-570">Aufrufen der Hintergrund Lade Montage auf der Grundlage der Clientkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="14981-570">Invoke background load mounting based on client configuration.</span></span>

7.  <span data-ttu-id="14981-571">Pakete, die bereits Veröffentlichungsinformationen für den Computer oder Benutzer aufweisen, werden sofort wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="14981-571">Packages that already have publishing information for the machine or user are immediately restored.</span></span>

    <span data-ttu-id="14981-572">**Hinweis**  Diese Bedingung tritt als ein Produkt der Entfernung auf, ohne die Veröffentlichung mit Hintergrund Addition des Pakets aufzuheben.</span><span class="sxs-lookup"><span data-stu-id="14981-572">**Note** This condition occurs as a product of removal without unpublishing with background addition of the package.</span></span>

     

<span data-ttu-id="14981-573">Damit ist ein App-V-Paket zum Veröffentlichen des Aktualisierungsprozesses abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="14981-573">This completes an App-V package add of the publishing refresh process.</span></span> <span data-ttu-id="14981-574">Im nächsten Schritt wird das Paket auf dem jeweiligen Ziel (Computer oder Benutzer) veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="14981-574">The next step is publishing the package to the specific target (machine or user).</span></span>

![Paket zum Hinzufügen von Datei-und Registrierungsdaten](images/packageaddfileandregistrydata.png)

### <span data-ttu-id="14981-576">Veröffentlichen eines App-V-Pakets</span><span class="sxs-lookup"><span data-stu-id="14981-576">Publishing an App-V package</span></span>

<span data-ttu-id="14981-577">Während des Veröffentlichungs Aktualisierungsvorgangs fügt der jeweilige Veröffentlichungsvorgang (Publish-AppVClientPackage) dem Benutzer Katalogeinträge hinzu, ordnet dem Benutzer den Berechtigungen zu, identifiziert den lokalen Speicher und beendet die einzelnen Integrationsschritte.</span><span class="sxs-lookup"><span data-stu-id="14981-577">During the Publishing Refresh operation, the specific publishing operation (Publish-AppVClientPackage) adds entries to the user catalog, maps entitlement to the user, identifies the local store, and finishes by completing any integration steps.</span></span> <span data-ttu-id="14981-578">Im folgenden finden Sie die detaillierten Schritte.</span><span class="sxs-lookup"><span data-stu-id="14981-578">The following are the detailed steps.</span></span>

**<span data-ttu-id="14981-579">Veröffentlichen und App-V-Paket</span><span class="sxs-lookup"><span data-stu-id="14981-579">How to publish and App-V package</span></span>**

1.  <span data-ttu-id="14981-580">Dem Benutzer Katalog werden Paket Einträge hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="14981-580">Package entries are added to the user catalog</span></span>

    1.  <span data-ttu-id="14981-581">Benutzerorientierte Pakete: die UserDeploymentConfiguration.xml und UserManifest.xml werden auf dem Computer im Benutzer Katalog gespeichert.</span><span class="sxs-lookup"><span data-stu-id="14981-581">User targeted packages: the UserDeploymentConfiguration.xml and UserManifest.xml are placed on the machine in the User Catalog</span></span>

    2.  <span data-ttu-id="14981-582">Maschinell ausgerichtete (globale) Pakete: die UserDeploymentConfiguration.xml wird im Computer Katalog gespeichert.</span><span class="sxs-lookup"><span data-stu-id="14981-582">Machine targeted (global) packages: the UserDeploymentConfiguration.xml is placed in the Machine Catalog</span></span>

2.  <span data-ttu-id="14981-583">Registrieren des Pakets mit dem Kernelmodus-Treiber für den Benutzer unter HKLM\\Software\\Microsoft\\AppV\\MAV</span><span class="sxs-lookup"><span data-stu-id="14981-583">Register the package with the kernel mode driver for the user at HKLM\\Software\\Microsoft\\AppV\\MAV</span></span>

3.  <span data-ttu-id="14981-584">Durchführen von Integrationsaufgaben</span><span class="sxs-lookup"><span data-stu-id="14981-584">Perform integration tasks.</span></span>

    1.  <span data-ttu-id="14981-585">Erstellen Sie Erweiterungspunkte.</span><span class="sxs-lookup"><span data-stu-id="14981-585">Create extension points.</span></span>

    2.  <span data-ttu-id="14981-586">Speichern von Sicherungsinformationen in der Registrierung und im Roaming-Profil des Benutzers (Verknüpfungs Sicherungen).</span><span class="sxs-lookup"><span data-stu-id="14981-586">Store backup information in the user’s registry and roaming profile (Shortcut Backups).</span></span>

        <span data-ttu-id="14981-587">**Hinweis**  Dies ermöglicht das Wiederherstellen von Erweiterungspunkten, wenn das Paket nicht veröffentlicht wurde.</span><span class="sxs-lookup"><span data-stu-id="14981-587">**Note** This enables restore extension points if the package is unpublished.</span></span>

         

    3.  <span data-ttu-id="14981-588">Führen Sie Skripts aus, die für die Veröffentlichungs Anzeige vorgesehen sind.</span><span class="sxs-lookup"><span data-stu-id="14981-588">Run scripts targeted for publishing timing.</span></span>

<span data-ttu-id="14981-589">Das Veröffentlichen eines App-V-Pakets, das Teil einer Verbindungsgruppe ist, ähnelt dem oben beschriebenen Verfahren.</span><span class="sxs-lookup"><span data-stu-id="14981-589">Publishing an App-V Package that is part of a Connection Group is very similar to the above process.</span></span> <span data-ttu-id="14981-590">Für Verbindungsgruppen enthält der Pfad, in dem die spezifischen Kataloginformationen gespeichert sind, PackageGroups als untergeordnetes Element des Katalog Verzeichnisses.</span><span class="sxs-lookup"><span data-stu-id="14981-590">For connection groups, the path that stores the specific catalog information includes PackageGroups as a child of the Catalog Directory.</span></span> <span data-ttu-id="14981-591">Weitere Informationen finden Sie in den Kataloginformationen zu Computer und Benutzern oben.</span><span class="sxs-lookup"><span data-stu-id="14981-591">Review the machine and users catalog information above for details.</span></span>

![Paketdatei-und Registrierungsdaten hinzufügen – Global](images/packageaddfileandregistrydata-global.png)

### <span data-ttu-id="14981-593">Anwendungsstart</span><span class="sxs-lookup"><span data-stu-id="14981-593">Application launch</span></span>

<span data-ttu-id="14981-594">Nach dem Veröffentlichungs Aktualisierungsvorgang startet der Benutzer eine App-V-Anwendung und startet Sie anschließend erneut.</span><span class="sxs-lookup"><span data-stu-id="14981-594">After the Publishing Refresh process, the user launches and subsequently re-launches an App-V application.</span></span> <span data-ttu-id="14981-595">Der Vorgang ist sehr einfach und für einen schnellen Start mit einem mindestnetzwerkverkehr optimiert.</span><span class="sxs-lookup"><span data-stu-id="14981-595">The process is very simple and optimized to launch quickly with a minimum of network traffic.</span></span> <span data-ttu-id="14981-596">Der App-V-Client überprüft den Pfad zu dem Benutzer Katalog für Dateien, die während der Veröffentlichung erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="14981-596">The App-V Client checks the path to the user catalog for files created during publishing.</span></span> <span data-ttu-id="14981-597">Nachdem die Rechte zum Starten des Pakets festgelegt wurden, erstellt der App-V-Client eine virtuelle Umgebung, beginnt mit dem Streaming aller erforderlichen Daten und wendet die entsprechenden Manifest-und Bereitstellungskonfigurationsdateien während der Erstellung der virtuellen Umgebung an.</span><span class="sxs-lookup"><span data-stu-id="14981-597">After rights to launch the package are established, the App-V Client creates a virtual environment, begins streaming any necessary data, and applies the appropriate manifest and deployment configuration files during virtual environment creation.</span></span> <span data-ttu-id="14981-598">Bei der Erstellung und Konfiguration der virtuellen Umgebung für das jeweilige Paket und die Anwendung wird die Anwendung gestartet.</span><span class="sxs-lookup"><span data-stu-id="14981-598">With the virtual environment created and configured for the specific package and application, the application starts.</span></span>

**<span data-ttu-id="14981-599">Starten von App-V-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="14981-599">How to launch App-V applications</span></span>**

1.  <span data-ttu-id="14981-600">Der Benutzer startet die Anwendung durch Klicken auf einen Verknüpfungs-oder Dateityp Aufruf.</span><span class="sxs-lookup"><span data-stu-id="14981-600">User launches the application by clicking on a shortcut or file type invocation.</span></span>

2.  <span data-ttu-id="14981-601">Der App-V-Client überprüft die Existenz im Benutzer Katalog für die folgenden Dateien:</span><span class="sxs-lookup"><span data-stu-id="14981-601">The App-V Client verifies existence in the User Catalog for the following files</span></span>

    -   <span data-ttu-id="14981-602">UserDeploymentConfiguration.xml</span><span class="sxs-lookup"><span data-stu-id="14981-602">UserDeploymentConfiguration.xml</span></span>

    -   <span data-ttu-id="14981-603">UserManifest.xml</span><span class="sxs-lookup"><span data-stu-id="14981-603">UserManifest.xml</span></span>

3.  <span data-ttu-id="14981-604">Wenn die Dateien vorhanden sind, ist die Anwendung für diesen bestimmten Benutzer berechtigt, und die Anwendung startet den Vorgang für den Start.</span><span class="sxs-lookup"><span data-stu-id="14981-604">If the files are present, the application is entitled for that specific user and the application will start the process for launch.</span></span> <span data-ttu-id="14981-605">An diesem Punkt ist kein Netzwerkdatenverkehr vorhanden.</span><span class="sxs-lookup"><span data-stu-id="14981-605">There is no network traffic at this point.</span></span>

4.  <span data-ttu-id="14981-606">Als nächstes überprüft der APP-v-Client, ob sich der Pfad für das für den App-v-Client Dienst registrierte Paket in der Registrierung befindet.</span><span class="sxs-lookup"><span data-stu-id="14981-606">Next, the App-V Client checks that the path for the package registered for the App-V Client service is found in the registry.</span></span>

5.  <span data-ttu-id="14981-607">Nachdem Sie den Pfad zum Paketspeicher gefunden haben, wird die virtuelle Umgebung erstellt.</span><span class="sxs-lookup"><span data-stu-id="14981-607">Upon finding the path to the package store, the virtual environment is created.</span></span> <span data-ttu-id="14981-608">Wenn es sich um den ersten Start handelt, blockiert das primäre Feature Downloads, falls vorhanden.</span><span class="sxs-lookup"><span data-stu-id="14981-608">If this is the first launch, the Primary Feature Block downloads if present.</span></span>

6.  <span data-ttu-id="14981-609">Nach dem Download verbraucht der APP-v-Client Dienst die Konfigurationsdateien für Manifest und Bereitstellung, um die virtuelle Umgebung zu konfigurieren, und alle App-v-Subsysteme werden geladen.</span><span class="sxs-lookup"><span data-stu-id="14981-609">After downloading, the App-V Client service consumes the manifest and deployment configuration files to configure the virtual environment and all App-V subsystems are loaded.</span></span>

7.  <span data-ttu-id="14981-610">Die Anwendung wird gestartet.</span><span class="sxs-lookup"><span data-stu-id="14981-610">The Application launches.</span></span> <span data-ttu-id="14981-611">Für alle fehlenden Dateien im Paketspeicher (Sparse-Dateien) streamt App-V Fehler Dateien nach Bedarf.</span><span class="sxs-lookup"><span data-stu-id="14981-611">For any missing files in the package store (sparse files), App-V will stream fault the files on an as needed basis.</span></span>

    ![Paket zum Hinzufügen von Datei-und Registrierungsdaten strömen](images/packageaddfileandregistrydata-stream.png)

### <span data-ttu-id="14981-613">Aktualisieren eines App-V-Pakets</span><span class="sxs-lookup"><span data-stu-id="14981-613">Upgrading an App-V package</span></span>

<span data-ttu-id="14981-614">Das Upgrade des App-v 5-Pakets unterscheidet sich von den älteren Versionen von App-v.</span><span class="sxs-lookup"><span data-stu-id="14981-614">The App-V 5 package upgrade process differs from the older versions of App-V.</span></span> <span data-ttu-id="14981-615">App-V unterstützt mehrere Versionen desselben Pakets auf einem Computer, der für verschiedene Benutzer berechtigt ist.</span><span class="sxs-lookup"><span data-stu-id="14981-615">App-V supports multiple versions of the same package on a machine entitled to different users.</span></span> <span data-ttu-id="14981-616">Paketversionen können jederzeit hinzugefügt werden, wenn der Paketspeicher und die Kataloge mit den neuen Ressourcen aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="14981-616">Package versions can be added at any time as the package store and catalogs are updated with the new resources.</span></span> <span data-ttu-id="14981-617">Der einzige für das Hinzufügen neuer Versionsressourcen spezifischer Prozess ist die Speicheroptimierung.</span><span class="sxs-lookup"><span data-stu-id="14981-617">The only process specific to the addition of new version resources is storage optimization.</span></span> <span data-ttu-id="14981-618">Während eines Upgrades werden nur die neuen Dateien zum neuen Versionsspeicher Standort hinzugefügt, und es werden harte Links für unveränderte Dateien erstellt.</span><span class="sxs-lookup"><span data-stu-id="14981-618">During an upgrade, only the new files are added to the new version store location and hard links are created for unchanged files.</span></span> <span data-ttu-id="14981-619">Dadurch wird der Gesamtspeicher reduziert, indem die Datei nur auf einem Datenträger gespeichert und dann in alle Ordner mit einem Dateispeicherort Eintrag auf dem Datenträger projiziert wird.</span><span class="sxs-lookup"><span data-stu-id="14981-619">This reduces the overall storage by only presenting the file on one disk location and then projecting it into all folders with a file location entry on the disk.</span></span> <span data-ttu-id="14981-620">Die speziellen Details zum Upgrade eines App-V-Pakets lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="14981-620">The specific details of upgrading an App-V Package are as follows:</span></span>

**<span data-ttu-id="14981-621">Aktualisieren eines App-V-Pakets</span><span class="sxs-lookup"><span data-stu-id="14981-621">How to upgrade an App-V package</span></span>**

1.  <span data-ttu-id="14981-622">Der APP-v-Client führt eine Veröffentlichungsaktualisierung durch und ermittelt eine neuere Version eines App-v-Pakets.</span><span class="sxs-lookup"><span data-stu-id="14981-622">The App-V Client performs a Publishing Refresh and discovers a newer version of an App-V Package.</span></span>

2.  <span data-ttu-id="14981-623">Paket Einträge werden dem entsprechenden Katalog für die neue Version hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="14981-623">Package entries are added to the appropriate catalog for the new version</span></span>

    1.  <span data-ttu-id="14981-624">Benutzerorientierte Pakete: die UserDeploymentConfiguration.xml und UserManifest.xml werden auf dem Computer im Benutzer Katalog unter appdata\\roaming\\Microsoft\\AppV\\Client\\Catalog\\Packages\\PkgGUID\\VerGUID</span><span class="sxs-lookup"><span data-stu-id="14981-624">User targeted packages: the UserDeploymentConfiguration.xml and UserManifest.xml are placed on the machine in the user catalog at appdata\\roaming\\Microsoft\\AppV\\Client\\Catalog\\Packages\\PkgGUID\\VerGUID</span></span>

    2.  <span data-ttu-id="14981-625">Maschinell ausgerichtete (globale) Pakete: die UserDeploymentConfiguration.xml wird im Computer Katalog unter%ProgramData%\\Microsoft\\AppV\\Client\\Catalog\\Packages\\PkgGUID\\VerGUID gespeichert.</span><span class="sxs-lookup"><span data-stu-id="14981-625">Machine targeted (global) packages: the UserDeploymentConfiguration.xml is placed in the machine catalog at %programdata%\\Microsoft\\AppV\\Client\\Catalog\\Packages\\PkgGUID\\VerGUID</span></span>

3.  <span data-ttu-id="14981-626">Registrieren des Pakets mit dem Kernelmodus-Treiber für den Benutzer unter HKLM\\Software\\Microsoft\\AppV\\MAV</span><span class="sxs-lookup"><span data-stu-id="14981-626">Register the package with the kernel mode driver for the user at HKLM\\Software\\Microsoft\\AppV\\MAV</span></span>

4.  <span data-ttu-id="14981-627">Durchführen von Integrationsaufgaben</span><span class="sxs-lookup"><span data-stu-id="14981-627">Perform integration tasks.</span></span>

    -   <span data-ttu-id="14981-628">Integrieren Sie Erweiterungspunkte (EP) aus den Manifesten und dynamischen Konfigurationsdateien.</span><span class="sxs-lookup"><span data-stu-id="14981-628">Integrate extensions points (EP) from the Manifest and Dynamic Configuration files.</span></span>

    1.  <span data-ttu-id="14981-629">Dateibasierte EP-Daten werden im AppData-Ordner unter Verwendung von Abzweigungspunkten aus dem Paketspeicher gespeichert.</span><span class="sxs-lookup"><span data-stu-id="14981-629">File based EP data is stored in the AppData folder utilizing Junction Points from the package store.</span></span>

    2.  <span data-ttu-id="14981-630">Version 1 EPS ist bereits vorhanden, wenn eine neue Version verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="14981-630">Version 1 EPs already exist when a new version becomes available.</span></span>

    3.  <span data-ttu-id="14981-631">Die Erweiterungspunkte werden in Maschinen-oder Benutzer Katalogen für neuere oder aktualisierte Erweiterungspunkte auf den Standort Version 2 umgeschaltet.</span><span class="sxs-lookup"><span data-stu-id="14981-631">The extension points are switched to the Version 2 location in machine or user catalogs for any newer or updated extension points.</span></span>

5.  <span data-ttu-id="14981-632">Führen Sie Skripts aus, die für die Veröffentlichungs Anzeige vorgesehen sind.</span><span class="sxs-lookup"><span data-stu-id="14981-632">Run scripts targeted for publishing timing.</span></span>

6.  <span data-ttu-id="14981-633">Installieren Sie nebeneinander angeordnete Assemblys nach Bedarf.</span><span class="sxs-lookup"><span data-stu-id="14981-633">Install Side by Side assemblies as required.</span></span>

### <span data-ttu-id="14981-634">Aktualisieren eines in-use-App-V-Pakets</span><span class="sxs-lookup"><span data-stu-id="14981-634">Upgrading an in-use App-V package</span></span>

<span data-ttu-id="14981-635">**Ab App-V 5 SP2**: Wenn Sie versuchen, ein Paket zu aktualisieren, das von einem Endbenutzer verwendet wird, wird die Aktualisierungsaufgabe in einem ausstehenden Zustand gespeichert.</span><span class="sxs-lookup"><span data-stu-id="14981-635">**Starting in App-V 5 SP2**: If you try to upgrade a package that is in use by an end user, the upgrade task is placed in a pending state.</span></span> <span data-ttu-id="14981-636">Das Upgrade wird später entsprechend den folgenden Regeln ausgeführt:</span><span class="sxs-lookup"><span data-stu-id="14981-636">The upgrade will run later, according to the following rules:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="14981-637">Art der Hintergrundaufgabe</span><span class="sxs-lookup"><span data-stu-id="14981-637">Task type</span></span></th>
<th align="left"><span data-ttu-id="14981-638">Anwendbare Regel</span><span class="sxs-lookup"><span data-stu-id="14981-638">Applicable rule</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="14981-639">Benutzerbasierte Aufgaben, beispielsweise die Veröffentlichung eines Pakets für einen Benutzer</span><span class="sxs-lookup"><span data-stu-id="14981-639">User-based task, e.g., publishing a package to a user</span></span></p></td>
<td align="left"><p><span data-ttu-id="14981-640">Die ausstehende Aufgabe wird ausgeführt, nachdem sich der Benutzer abgemeldet hat und sich dann wieder anmeldet.</span><span class="sxs-lookup"><span data-stu-id="14981-640">The pending task will be performed after the user logs off and then logs back on.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="14981-641">Global basierender Vorgang, beispielsweise Aktivieren einer Verbindungsgruppe Global</span><span class="sxs-lookup"><span data-stu-id="14981-641">Globally based task, e.g., enabling a connection group globally</span></span></p></td>
<td align="left"><p><span data-ttu-id="14981-642">Die ausstehende Aufgabe wird ausgeführt, wenn der Computer heruntergefahren und neu gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="14981-642">The pending task will be performed when the computer is shut down and then restarted.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="14981-643">Wenn eine Aufgabe in einem ausstehenden Zustand befindet, generiert der App-V-Client auch einen Registrierungsschlüssel für die ausstehende Aufgabe wie folgt:</span><span class="sxs-lookup"><span data-stu-id="14981-643">When a task is placed in a pending state, the App-V client also generates a registry key for the pending task, as follows:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="14981-644">Benutzerbasierter oder Global basierter Vorgang</span><span class="sxs-lookup"><span data-stu-id="14981-644">User-based or globally based task</span></span></th>
<th align="left"><span data-ttu-id="14981-645">Ort, an dem der Registrierungsschlüssel generiert wird</span><span class="sxs-lookup"><span data-stu-id="14981-645">Where the registry key is generated</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="14981-646">Benutzerbasierte Aufgaben</span><span class="sxs-lookup"><span data-stu-id="14981-646">User-based tasks</span></span></p></td>
<td align="left"><p><span data-ttu-id="14981-647">KEY_CURRENT_USER \software\microsoft\appv\client\pendingtasks</span><span class="sxs-lookup"><span data-stu-id="14981-647">KEY_CURRENT_USER\Software\Microsoft\AppV\Client\PendingTasks</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="14981-648">Global basierte Aufgaben</span><span class="sxs-lookup"><span data-stu-id="14981-648">Globally based tasks</span></span></p></td>
<td align="left"><p><span data-ttu-id="14981-649">HKEY_LOCAL_MACHINE \software\microsoft\appv\client\pendingtasks</span><span class="sxs-lookup"><span data-stu-id="14981-649">HKEY_LOCAL_MACHINE\Software\Microsoft\AppV\Client\PendingTasks</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="14981-650">Die folgenden Vorgänge müssen abgeschlossen sein, bevor Benutzer die neuere Version des Pakets verwenden können:</span><span class="sxs-lookup"><span data-stu-id="14981-650">The following operations must be completed before users can use the newer version of the package:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="14981-651">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="14981-651">Task</span></span></th>
<th align="left"><span data-ttu-id="14981-652">Details</span><span class="sxs-lookup"><span data-stu-id="14981-652">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="14981-653">Hinzufügen des Pakets zum Computer</span><span class="sxs-lookup"><span data-stu-id="14981-653">Add the package to the computer</span></span></p></td>
<td align="left"><p><span data-ttu-id="14981-654">Diese Aufgabe ist Computer spezifisch, und Sie können Sie jederzeit durchführen, indem Sie die Schritte im Abschnitt Paket hinzufügen oben ausführen.</span><span class="sxs-lookup"><span data-stu-id="14981-654">This task is computer specific and you can perform it at any time by completing the steps in the Package Add section above.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="14981-655">Veröffentlichen des Pakets</span><span class="sxs-lookup"><span data-stu-id="14981-655">Publish the package</span></span></p></td>
<td align="left"><p><span data-ttu-id="14981-656">Weitere Informationen finden Sie im Abschnitt Paket Veröffentlichung oben unter Schritte.</span><span class="sxs-lookup"><span data-stu-id="14981-656">See the Package Publishing section above for steps.</span></span> <span data-ttu-id="14981-657">Dieser Vorgang erfordert, dass Sie Erweiterungspunkte auf dem System aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="14981-657">This process requires that you update extension points on the system.</span></span> <span data-ttu-id="14981-658">Endbenutzer können die Anwendung nicht verwenden, wenn Sie diese Aufgabe ausführen.</span><span class="sxs-lookup"><span data-stu-id="14981-658">End users cannot be using the application when you complete this task.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="14981-659">Verwenden Sie die folgenden Beispielszenarien als Leitfaden zum Aktualisieren von Paketen.</span><span class="sxs-lookup"><span data-stu-id="14981-659">Use the following example scenarios as a guide for updating packages.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="14981-660">Szenario</span><span class="sxs-lookup"><span data-stu-id="14981-660">Scenario</span></span></th>
<th align="left"><span data-ttu-id="14981-661">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="14981-661">Requirements</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="14981-662">Das App-V-Paket wird nicht verwendet, wenn Sie versuchen, ein Upgrade durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="14981-662">App-V package is not in use when you try to upgrade</span></span></p></td>
<td align="left"><p><span data-ttu-id="14981-663">Keine der folgenden Komponenten des Pakets kann verwendet werden: virtuelle Anwendung, com-Server oder Shell-Erweiterungen.</span><span class="sxs-lookup"><span data-stu-id="14981-663">None of the following components of the package can be in use: virtual application, COM server, or shell extensions.</span></span></p>
<p><span data-ttu-id="14981-664">Der Administrator veröffentlicht eine neuere Version des Pakets, und das Upgrade funktioniert, wenn eine Komponente oder Anwendung innerhalb des Pakets das nächste Mal gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="14981-664">The administrator publishes a newer version of the package and the upgrade works the next time a component or application inside the package is launched.</span></span> <span data-ttu-id="14981-665">Die neue Version des Pakets wird gestreamt und ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="14981-665">The new version of the package is streamed and run.</span></span> <span data-ttu-id="14981-666">In diesem Szenario wurde in App-v 5 SP2 aus früheren Versionen von App-v 5 nichts geändert.</span><span class="sxs-lookup"><span data-stu-id="14981-666">Nothing has changed in this scenario in App-V 5 SP2 from previous releases of App-V 5.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="14981-667">Das App-V-Paket wird verwendet, wenn der Administrator eine neuere Version des Pakets veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="14981-667">App-V package is in use when the administrator publishes a newer version of the package</span></span></p></td>
<td align="left"><p><span data-ttu-id="14981-668">Der Aktualisierungsvorgang wird vom App-V-Client auf Ausstehend festgesetzt, was bedeutet, dass er in die Warteschlange gestellt und später ausgeführt wird, wenn das Paket nicht verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="14981-668">The upgrade operation is set to pending by the App-V Client, which means that it is queued and carried out later when the package is not in use.</span></span></p>
<p><span data-ttu-id="14981-669">Wenn die Paketanwendung verwendet wird, fährt der Benutzer die virtuelle Anwendung herunter, nach der das Upgrade ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="14981-669">If the package application is in use, the user shuts down the virtual application, after which the upgrade can occur.</span></span></p>
<p><span data-ttu-id="14981-670">Wenn das Paket über Shell-Erweiterungen (Office 2013) verfügt, die vom Windows-Explorer dauerhaft geladen werden, kann der Benutzer nicht angemeldet werden.</span><span class="sxs-lookup"><span data-stu-id="14981-670">If the package has shell extensions (Office 2013), which are permanently loaded by Windows Explorer, the user cannot be logged in.</span></span> <span data-ttu-id="14981-671">Benutzer müssen sich ab-und wieder anmelden, um das App-V-PaketUpgrade zu initiieren.</span><span class="sxs-lookup"><span data-stu-id="14981-671">Users must log off and the log back in to initiate the App-V package upgrade.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="14981-672">Global vs User Publishing</span><span class="sxs-lookup"><span data-stu-id="14981-672">Global vs user publishing</span></span>

<span data-ttu-id="14981-673">App-V-Pakete können auf eine von zwei Arten veröffentlicht werden. Benutzer, der ein App-v-Paket für einen bestimmten Benutzer oder eine Gruppe von Benutzern und Global anrechtet, das das App-v-Paket für alle Benutzer des Computers zum gesamten Computer berechtigt.</span><span class="sxs-lookup"><span data-stu-id="14981-673">App-V Packages can be published in one of two ways; User which entitles an App-V package to a specific user or group of users and Global which entitles the App-V package to the entire machine for all users of the machine.</span></span> <span data-ttu-id="14981-674">Nachdem ein PaketUpgrade vorangestellt wurde und das App-V-Paket nicht verwendet wird, sollten Sie die beiden Arten der Veröffentlichung in Frage stellen:</span><span class="sxs-lookup"><span data-stu-id="14981-674">Once a package upgrade has been pended and the App-V package is not in use, consider the two types of publishing:</span></span>

-   <span data-ttu-id="14981-675">**Global veröffentlicht**: die Anwendung wird auf einem Computer veröffentlicht. alle Benutzer auf diesem Computer können Sie verwenden.</span><span class="sxs-lookup"><span data-stu-id="14981-675">**Globally published**: the application is published to a machine; all users on that machine can use it.</span></span> <span data-ttu-id="14981-676">Das Upgrade wird durchgeführt, wenn der App-V-Client Dienst gestartet wird, was effektiv einen Neustart des Computers bedeutet.</span><span class="sxs-lookup"><span data-stu-id="14981-676">The upgrade will happen when the App-V Client Service starts, which effectively means a machine restart.</span></span>

-   <span data-ttu-id="14981-677">**Benutzer veröffentlicht**: die Anwendung wird für einen Benutzer veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="14981-677">**User published**: the application is published to a user.</span></span> <span data-ttu-id="14981-678">Wenn auf dem Computer mehrere Benutzer vorhanden sind, kann die Anwendung in einer Teilmenge der Benutzer veröffentlicht werden.</span><span class="sxs-lookup"><span data-stu-id="14981-678">If there are multiple users on the machine, the application can be published to a subset of the users.</span></span> <span data-ttu-id="14981-679">Das Upgrade erfolgt, wenn sich der Benutzer anmeldet oder wenn er erneut veröffentlicht wird (regelmäßige Aktualisierung und Auswertung der ConfigMgr-Richtlinie oder regelmäßige Veröffentlichung/Aktualisierung von App-V oder explizit über PowerShell-Befehle).</span><span class="sxs-lookup"><span data-stu-id="14981-679">The upgrade will happen when the user logs in or when it is published again (periodically, ConfigMgr Policy refresh and evaluation, or an App-V periodic publishing/refresh, or explicitly via PowerShell commands).</span></span>

### <span data-ttu-id="14981-680">Entfernen eines App-V-Pakets</span><span class="sxs-lookup"><span data-stu-id="14981-680">Removing an App-V package</span></span>

<span data-ttu-id="14981-681">Das Entfernen von App-V-Anwendungen in einer vollständigen Infrastruktur ist eine Veröffentlichungsoperation, bei der keine Paketentfernung durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="14981-681">Removing App-V applications in a Full Infrastructure is an unpublish operation, and does not perform a package removal.</span></span> <span data-ttu-id="14981-682">Der Prozess ist derselbe wie der obige Veröffentlichungsprozess, doch anstelle des Hinzufügens des Entfernungsprozesses werden die Änderungen, die für App-V-Pakete vorgenommen wurden, umgekehrt.</span><span class="sxs-lookup"><span data-stu-id="14981-682">The process is the same as the publish process above, but instead of adding the removal process reverses the changes that have been made for App-V Packages.</span></span>

### <span data-ttu-id="14981-683">Reparieren eines App-V-Pakets</span><span class="sxs-lookup"><span data-stu-id="14981-683">Repairing an App-V package</span></span>

<span data-ttu-id="14981-684">Der Reparaturvorgang ist sehr einfach, kann sich aber auf viele Speicherorte auf dem Computer auswirken.</span><span class="sxs-lookup"><span data-stu-id="14981-684">The repair operation is very simple but may affect many locations on the machine.</span></span> <span data-ttu-id="14981-685">Die zuvor erwähnten Exemplare auf Write (Cow)-Speicherorten werden entfernt, und Erweiterungspunkte werden deintegriert und dann wieder integriert.</span><span class="sxs-lookup"><span data-stu-id="14981-685">The previously mentioned Copy on Write (COW) locations are removed, and extension points are de-integrated and then re-integrated.</span></span> <span data-ttu-id="14981-686">Überprüfen Sie die Position der Cow-Daten Platzierungen, indem Sie überprüfen, wo Sie in der Registrierung registriert sind.</span><span class="sxs-lookup"><span data-stu-id="14981-686">Please review the COW data placement locations by reviewing where they are registered in the registry.</span></span> <span data-ttu-id="14981-687">Dieser Vorgang erfolgt automatisch, und es gibt keine andere administrative Steuerung als das Initiieren eines Reparaturvorgangs über die App-V-Client Konsole oder über PowerShell (Repair-AppVClientPackage).</span><span class="sxs-lookup"><span data-stu-id="14981-687">This operation is done automatically and there is no administrative control other than initiating a Repair operation from the App-V Client Console or via PowerShell (Repair-AppVClientPackage).</span></span>

## <a href="" id="bkmk-integr-appv-pkgs"></a><span data-ttu-id="14981-688">Integration von App-V-Paketen</span><span class="sxs-lookup"><span data-stu-id="14981-688">Integration of App-V packages</span></span>


<span data-ttu-id="14981-689">Die App-V-Client-und-Paketarchitektur bietet beim Hinzufügen und Veröffentlichen von Paketen eine spezifische Integration in das lokale Betriebssystem.</span><span class="sxs-lookup"><span data-stu-id="14981-689">The App-V Client and package architecture provides specific integration with the local operating system during the addition and publishing of packages.</span></span> <span data-ttu-id="14981-690">Drei Dateien definieren die Integrations-oder Erweiterungspunkte für ein App-V-Paket:</span><span class="sxs-lookup"><span data-stu-id="14981-690">Three files define the integration or extension points for an App-V Package:</span></span>

-   <span data-ttu-id="14981-691">AppXManifest.xml: innerhalb des Pakets mit Fall Back Kopien gespeichert, die im Paketspeicher und im Benutzerprofilgespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="14981-691">AppXManifest.xml: Stored inside of the package with fallback copies stored in the package store and the user profile.</span></span> <span data-ttu-id="14981-692">Enthält die während des Sequenz Prozesses erstellten Optionen.</span><span class="sxs-lookup"><span data-stu-id="14981-692">Contains the options created during the sequencing process.</span></span>

-   <span data-ttu-id="14981-693">DeploymentConfig.xml: enthält Konfigurationsinformationen zu Erweiterungspunkten für Computer-und benutzerbasierte Integrationen.</span><span class="sxs-lookup"><span data-stu-id="14981-693">DeploymentConfig.xml: Provides configuration information of computer and user based integration extension points.</span></span>

-   <span data-ttu-id="14981-694">UserConfig.xml: eine Teilmenge der Deploymentconfig.xml, die nur benutzerbasierte Konfigurationen bereitstellt und nur auf benutzerbasierte Erweiterungspunkte ausgerichtet ist.</span><span class="sxs-lookup"><span data-stu-id="14981-694">UserConfig.xml: A subset of the Deploymentconfig.xml that only provides user- based configurations and only targets user-based extension points.</span></span>

### <span data-ttu-id="14981-695">Regeln für die Integration</span><span class="sxs-lookup"><span data-stu-id="14981-695">Rules of integration</span></span>

<span data-ttu-id="14981-696">Wenn App-v-Anwendungen auf einem Computer mit dem App-v-Client veröffentlicht werden, finden einige spezifische Aktionen statt, wie in der folgenden Liste beschrieben:</span><span class="sxs-lookup"><span data-stu-id="14981-696">When App-V applications are published to a computer with the App-V Client, some specific actions take place as described in the list below:</span></span>

-   <span data-ttu-id="14981-697">Global Publishing: Verknüpfungen werden im Profilspeicherort alle Benutzer gespeichert, und andere Erweiterungspunkte werden in der Registrierung in der HKLM-Struktur gespeichert.</span><span class="sxs-lookup"><span data-stu-id="14981-697">Global Publishing: Shortcuts are stored in the All Users profile location and other extension points are stored in the registry in the HKLM hive.</span></span>

-   <span data-ttu-id="14981-698">Benutzer Veröffentlichung: Verknüpfungen werden im aktuellen Benutzerkontoprofil gespeichert, und andere Erweiterungspunkte werden in der Registrierung in der HKCU-Struktur gespeichert.</span><span class="sxs-lookup"><span data-stu-id="14981-698">User Publishing: Shortcuts are stored in the current user account profile and other extension points are stored in the registry in the HKCU hive.</span></span>

-   <span data-ttu-id="14981-699">Sicherung und Wiederherstellung: vorhandene systemeigene Anwendungsdaten und Registrierung (wie FTA-Registrierungen) werden während der Veröffentlichung gesichert.</span><span class="sxs-lookup"><span data-stu-id="14981-699">Backup and Restore: Existing native application data and registry (such as FTA registrations) are backed up during publishing.</span></span>

    1.  <span data-ttu-id="14981-700">App-v-Pakete erhalten den Besitz auf der Grundlage des letzten integrierten Pakets, in dem der Besitz an die neueste veröffentlichte App-v-Anwendung übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="14981-700">App-V packages are given ownership based on the last integrated package where the ownership is passed to the newest published App-V application.</span></span>

    2.  <span data-ttu-id="14981-701">Besitzer Übertragungen von einem App-v-Paket zu einem anderen, wenn das besitzende App-v-Paket nicht veröffentlicht wurde.</span><span class="sxs-lookup"><span data-stu-id="14981-701">Ownership transfers from one App-V package to another when the owning App-V package is unpublished.</span></span> <span data-ttu-id="14981-702">Dadurch wird keine Wiederherstellung der Daten oder der Registrierung initiiert.</span><span class="sxs-lookup"><span data-stu-id="14981-702">This will not initiate a restore of the data or registry.</span></span>

    3.  <span data-ttu-id="14981-703">Wiederherstellen der gesicherten Daten, wenn das letzte Paket unveröffentlicht oder auf einer Basis für die Erweiterung entfernt wurde.</span><span class="sxs-lookup"><span data-stu-id="14981-703">Restore the backed up data when the last package is unpublished or removed on a per extension point basis.</span></span>

### <span data-ttu-id="14981-704">Erweiterungspunkte</span><span class="sxs-lookup"><span data-stu-id="14981-704">Extension points</span></span>

<span data-ttu-id="14981-705">Die App-V-Veröffentlichungsdateien (Manifest und dynamische Konfiguration) bieten mehrere Erweiterungspunkte, mit denen die Anwendung in das lokale Betriebssystem integriert werden kann.</span><span class="sxs-lookup"><span data-stu-id="14981-705">The App-V publishing files (manifest and dynamic configuration) provide several extension points that enable the application to integrate with the local operating system.</span></span> <span data-ttu-id="14981-706">Diese Erweiterungspunkte führen typische Anwendungs Installationsaufgaben aus, beispielsweise das Platzieren von Verknüpfungen, das Erstellen von Dateitypzuordnungen und das Registrieren von Komponenten.</span><span class="sxs-lookup"><span data-stu-id="14981-706">These extension points perform typical application installation tasks, such as placing shortcuts, creating file type associations, and registering components.</span></span> <span data-ttu-id="14981-707">Da es sich um virtualisierte Anwendungen handelt, die nicht auf die gleiche Weise wie eine herkömmliche Anwendung installiert sind, gibt es einige Unterschiede.</span><span class="sxs-lookup"><span data-stu-id="14981-707">As these are virtualized applications that are not installed in the same manner a traditional application, there are some differences.</span></span> <span data-ttu-id="14981-708">Im folgenden finden Sie eine Liste der in diesem Abschnitt behandelten Erweiterungspunkte:</span><span class="sxs-lookup"><span data-stu-id="14981-708">The following is a list of extension points covered in this section:</span></span>

-   <span data-ttu-id="14981-709">Kombinationen</span><span class="sxs-lookup"><span data-stu-id="14981-709">Shortcuts</span></span>

-   <span data-ttu-id="14981-710">Dateitypzuordnungen</span><span class="sxs-lookup"><span data-stu-id="14981-710">File Type Associations</span></span>

-   <span data-ttu-id="14981-711">Shell-Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="14981-711">Shell Extensions</span></span>

-   <span data-ttu-id="14981-712">COM</span><span class="sxs-lookup"><span data-stu-id="14981-712">COM</span></span>

-   <span data-ttu-id="14981-713">Software-Clients</span><span class="sxs-lookup"><span data-stu-id="14981-713">Software Clients</span></span>

-   <span data-ttu-id="14981-714">Anwendungsfunktionen</span><span class="sxs-lookup"><span data-stu-id="14981-714">Application capabilities</span></span>

-   <span data-ttu-id="14981-715">URL-Protokoll Handler</span><span class="sxs-lookup"><span data-stu-id="14981-715">URL Protocol Handler</span></span>

-   <span data-ttu-id="14981-716">AppPath</span><span class="sxs-lookup"><span data-stu-id="14981-716">AppPath</span></span>

-   <span data-ttu-id="14981-717">Virtuelle Anwendung</span><span class="sxs-lookup"><span data-stu-id="14981-717">Virtual Application</span></span>

### <span data-ttu-id="14981-718">Kombinationen</span><span class="sxs-lookup"><span data-stu-id="14981-718">Shortcuts</span></span>

<span data-ttu-id="14981-719">Die Abkürzung ist eines der grundlegenden Elemente der Integration mit dem Betriebssystem und ist die Schnittstelle für die direkte Benutzereinführung einer App-V-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="14981-719">The short cut is one of the basic elements of integration with the OS and is the interface for direct user launch of an App-V application.</span></span> <span data-ttu-id="14981-720">Beim Veröffentlichen und Aufheben der Veröffentlichung von App-V-Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="14981-720">During the publishing and unpublishing of App-V applications.</span></span>

<span data-ttu-id="14981-721">In den XML-Dateien des paketmanifests und der Dynamic Configuration-XML-Datei befindet sich der Pfad zu einer bestimmten ausführbaren Anwendung in einem Abschnitt ähnlich der folgenden:</span><span class="sxs-lookup"><span data-stu-id="14981-721">From the package manifest and dynamic configuration XML files, the path to a specific application executable can be found in a section similar to the following:</span></span>

```xml
<Extension Category="AppV.Shortcut">
          <Shortcut>
            <File>[{Common Desktop}]\Adobe Reader 9.lnk</File>
            <Target>[{AppVPackageRoot}]\Reader\AcroRd32.exe</Target>
            <Icon>[{Windows}]\Installer\{AC76BA86-7AD7-1033-7B44-A94000000001}\SC_Reader.ico</Icon>
            <Arguments />
            <WorkingDirectory />
            <ShowCommand>1</ShowCommand>
            <ApplicationId>[{AppVPackageRoot}]\Reader\AcroRd32.exe</ApplicationId>
          </Shortcut>
        </Extension>
```

<span data-ttu-id="14981-722">Wie bereits erwähnt, werden die App-V-Tastenkombinationen standardmäßig im Profil des Benutzers basierend auf dem Aktualisierungsvorgang gespeichert.</span><span class="sxs-lookup"><span data-stu-id="14981-722">As mentioned previously, the App-V shortcuts are placed by default in the user’s profile based on the refresh operation.</span></span> <span data-ttu-id="14981-723">Im Profil "alle Benutzer" werden die Tastenkombinationen für globale Aktualisierung platziert, und die Benutzeraktualisierung speichert Sie im Profil des jeweiligen Benutzers.</span><span class="sxs-lookup"><span data-stu-id="14981-723">Global refresh places shortcuts in the All Users profile and user refresh stores them in the specific user’s profile.</span></span> <span data-ttu-id="14981-724">Die tatsächliche ausführbare Datei wird im Paketspeicher gespeichert.</span><span class="sxs-lookup"><span data-stu-id="14981-724">The actual executable is stored in the Package Store.</span></span> <span data-ttu-id="14981-725">Der Speicherort der ICO-Datei ist eine Token-Position im App-V-Paket.</span><span class="sxs-lookup"><span data-stu-id="14981-725">The location of the ICO file is a tokenized location in the App-V package.</span></span>

### <span data-ttu-id="14981-726">Dateitypzuordnungen</span><span class="sxs-lookup"><span data-stu-id="14981-726">File type associations</span></span>

<span data-ttu-id="14981-727">Der APP-v-Client verwaltet die lokalen Dateitypzuordnungen während der Veröffentlichung, wodurch Benutzern die Verwendung von Dateityp aufrufen oder das Öffnen einer Datei mit einer speziell registrierten Erweiterung (DOCX) ermöglicht wird, um eine App-V-Anwendung zu starten.</span><span class="sxs-lookup"><span data-stu-id="14981-727">The App-V Client manages the local operating system File Type Associations during publishing, which enables users to use file type invocations or to open a file with a specifically registered extension (.docx) to start an App-V application.</span></span> <span data-ttu-id="14981-728">Dateitypzuordnungen sind in den Manifest-und dynamischen Konfigurationsdateien vorhanden, wie im folgenden Beispiel dargestellt:</span><span class="sxs-lookup"><span data-stu-id="14981-728">File type associations are present in the manifest and dynamic configuration files as represented in the example below:</span></span>

```xml
<Extension Category="AppV.FileTypeAssociation">
          <FileTypeAssociation>
            <FileExtension MimeAssociation="true">
              <Name>.xdp</Name>
              <ProgId>AcroExch.XDPDoc</ProgId>
              <ContentType>application/vnd.adobe.xdp+xml</ContentType>
            </FileExtension>
            <ProgId>
              <Name>AcroExch.XDPDoc</Name>
              <Description>Adobe Acrobat XML Data Package File</Description>
              <EditFlags>65536</EditFlags>
              <DefaultIcon>[{Windows}]\Installer\{AC76BA86-7AD7-1033-7B44-A94000000001}\XDPFile_8.ico</DefaultIcon>
              <ShellCommands>
                <DefaultCommand>Read</DefaultCommand>
                <ShellCommand>
                  <ApplicationId>[{AppVPackageRoot}]\Reader\AcroRd32.exe</ApplicationId>
                  <Name>Open</Name>
                  <CommandLine>"[{AppVPackageRoot}]\Reader\AcroRd32.exe" "%1"</CommandLine>
                </ShellCommand>
                <ShellCommand>
                  <ApplicationId>[{AppVPackageRoot}]\Reader\AcroRd32.exe</ApplicationId>
                  <Name>Printto</Name>
                  <CommandLine>"[{AppVPackageRoot}]\Reader\AcroRd32.exe"  /t "%1" "%2" "%3" "%4"</CommandLine>
                </ShellCommand>
                <ShellCommand>
                  <ApplicationId>[{AppVPackageRoot}]\Reader\AcroRd32.exe</ApplicationId>
                  <Name>Read</Name>
                  <FriendlyName>Open with Adobe Reader 9</FriendlyName>
                  <CommandLine>"[{AppVPackageRoot}]\Reader\AcroRd32.exe" "%1"</CommandLine>
                </ShellCommand>
              </ShellCommands>
            </ProgId>
          </FileTypeAssociation>
        </Extension>
```

<span data-ttu-id="14981-729">**Hinweis**  In diesem Beispiel:</span><span class="sxs-lookup"><span data-stu-id="14981-729">**Note** In this example:</span></span>

-   `<Name>.xdp</Name>` <span data-ttu-id="14981-730">ist die Erweiterung</span><span class="sxs-lookup"><span data-stu-id="14981-730">is the extension</span></span>

-   `<Name>AcroExch.XDPDoc</Name>` <span data-ttu-id="14981-731">der ProgID-Wert (der auf die benachbarte ProgID zeigt)</span><span class="sxs-lookup"><span data-stu-id="14981-731">is the ProgId value (which points to the adjoining ProgId)</span></span>

-   `<CommandLine>"[{AppVPackageRoot}]\Reader\AcroRd32.exe" "%1"</CommandLine>` <span data-ttu-id="14981-732">ist die Befehlszeile, die auf die ausführbare Anwendung verweist.</span><span class="sxs-lookup"><span data-stu-id="14981-732">is the command line, which points to the application executable</span></span>

 

### <span data-ttu-id="14981-733">-Shell-Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="14981-733">Shell extensions</span></span>

<span data-ttu-id="14981-734">Shell-Erweiterungen werden während des Sequenz Prozesses automatisch in das Paket eingebettet.</span><span class="sxs-lookup"><span data-stu-id="14981-734">Shell extensions are embedded in the package automatically during the sequencing process.</span></span> <span data-ttu-id="14981-735">Wenn das Paket Global veröffentlicht wird, gibt die Shell-Erweiterung Benutzern dieselbe Funktionalität wie bei der lokalen Installation der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="14981-735">When the package is published globally, the shell extension gives users the same functionality as if the application were locally installed.</span></span> <span data-ttu-id="14981-736">Die Anwendung erfordert keine zusätzliche Einrichtung oder Konfiguration auf dem Client, um die Shell-Erweiterungsfunktion zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="14981-736">The application requires no additional setup or configuration on the client to enable the shell extension functionality.</span></span>

**<span data-ttu-id="14981-737">Voraussetzungen für die Verwendung von Shell-Erweiterungen:</span><span class="sxs-lookup"><span data-stu-id="14981-737">Requirements for using shell extensions:</span></span>**

-   <span data-ttu-id="14981-738">Pakete, die eingebettete Shell-Erweiterungen enthalten, müssen global veröffentlicht werden.</span><span class="sxs-lookup"><span data-stu-id="14981-738">Packages that contain embedded shell extensions must be published globally.</span></span>

-   <span data-ttu-id="14981-739">Die "Bitanzahl" der Anwendung, des Sequencers und des App-V-Clients müssen übereinstimmen, oder die Shell-Erweiterungen funktionieren nicht.</span><span class="sxs-lookup"><span data-stu-id="14981-739">The “bitness” of the application, Sequencer, and App-V client must match, or the shell extensions won’t work.</span></span> <span data-ttu-id="14981-740">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="14981-740">For example:</span></span>

    -   <span data-ttu-id="14981-741">Die Version der Anwendung ist 64-Bit.</span><span class="sxs-lookup"><span data-stu-id="14981-741">The version of the application is 64-bit.</span></span>

    -   <span data-ttu-id="14981-742">Der Sequencer wird auf einem 64-Bit-Computer ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="14981-742">The Sequencer is running on a 64-bit computer.</span></span>

    -   <span data-ttu-id="14981-743">Das Paket wird an einen 64-Bit-App-V-Clientcomputer übermittelt.</span><span class="sxs-lookup"><span data-stu-id="14981-743">The package is being delivered to a 64-bit App-V client computer.</span></span>

<span data-ttu-id="14981-744">In der folgenden Tabelle werden die unterstützten Shell-Erweiterungen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="14981-744">The following table displays the supported shell extensions.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="14981-745">Handler</span><span class="sxs-lookup"><span data-stu-id="14981-745">Handler</span></span></th>
<th align="left"><span data-ttu-id="14981-746">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="14981-746">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="14981-747">Kontextmenü Handler</span><span class="sxs-lookup"><span data-stu-id="14981-747">Context menu handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="14981-748">Fügt dem Kontextmenü Menüelemente hinzu.</span><span class="sxs-lookup"><span data-stu-id="14981-748">Adds menu items to the context menu.</span></span> <span data-ttu-id="14981-749">Sie wird aufgerufen, bevor das Kontextmenü angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="14981-749">It is called before the context menu is displayed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="14981-750">Drag & Drop-Handler</span><span class="sxs-lookup"><span data-stu-id="14981-750">Drag-and-drop handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="14981-751">Steuert die Aktion beim Klicken mit der rechten Maustaste auf Drag & Drop und ändert das angezeigte Kontextmenü.</span><span class="sxs-lookup"><span data-stu-id="14981-751">Controls the action upon right-click drag-and-drop and modifies the context menu that appears.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="14981-752">Ablegen eines Ziel Handlers</span><span class="sxs-lookup"><span data-stu-id="14981-752">Drop target handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="14981-753">Steuert die Aktion, nachdem ein Datenobjekt gezogen und über ein Ablageziel wie eine Datei abgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="14981-753">Controls the action after a data object is dragged-and-dropped over a drop target such as a file.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="14981-754">Datenobjekt-Handler</span><span class="sxs-lookup"><span data-stu-id="14981-754">Data object handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="14981-755">Steuert die Aktion, nachdem eine Datei in die Zwischenablage kopiert oder über ein Ablageziel gezogen und abgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="14981-755">Controls the action after a file is copied to the clipboard or dragged-and-dropped over a drop target.</span></span> <span data-ttu-id="14981-756">Sie kann dem Ablageziel zusätzliche Zwischenablageformate zur Verfügung stellen.</span><span class="sxs-lookup"><span data-stu-id="14981-756">It can provide additional clipboard formats to the drop target.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="14981-757">Eigenschaftentabellen-Handler</span><span class="sxs-lookup"><span data-stu-id="14981-757">Property sheet handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="14981-758">Ersetzt oder fügt Seiten in das DialogfeldEigenschaften Fenster eines Objekts ein.</span><span class="sxs-lookup"><span data-stu-id="14981-758">Replaces or adds pages to the property sheet dialog box of an object.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="14981-759">Infotipp-Handler</span><span class="sxs-lookup"><span data-stu-id="14981-759">Infotip handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="14981-760">Ermöglicht das Abrufen von Flags und Infotipp-Informationen für ein Element und das Anzeigen des Elements in einer Popup-QuickInfo beim Mauszeiger.</span><span class="sxs-lookup"><span data-stu-id="14981-760">Allows retrieving flags and infotip information for an item and displaying it inside a popup tooltip upon mouse- hover.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="14981-761">Spalten Handler</span><span class="sxs-lookup"><span data-stu-id="14981-761">Column handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="14981-762">Ermöglicht das Erstellen und Anzeigen benutzerdefinierter Spalten in der Windows-Explorer- <em> Detailansicht </em> .</span><span class="sxs-lookup"><span data-stu-id="14981-762">Allows creating and displaying custom columns in Windows Explorer <em>Details view</em>.</span></span> <span data-ttu-id="14981-763">Sie kann zum Erweitern von Sortierung und Gruppierung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="14981-763">It can be used to extend sorting and grouping.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="14981-764">Vorschauhandler</span><span class="sxs-lookup"><span data-stu-id="14981-764">Preview handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="14981-765">Ermöglicht das Anzeigen einer Vorschau einer Datei im Vorschaubereich von Windows-Explorer.</span><span class="sxs-lookup"><span data-stu-id="14981-765">Enables a preview of a file to be displayed in the Windows Explorer Preview Pane.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="14981-766">COM</span><span class="sxs-lookup"><span data-stu-id="14981-766">COM</span></span>

<span data-ttu-id="14981-767">Der App-V-Client unterstützt Veröffentlichungs Anwendungen mit Unterstützung für com-Integration und-Virtualisierung.</span><span class="sxs-lookup"><span data-stu-id="14981-767">The App-V Client supports publishing applications with support for COM integration and virtualization.</span></span> <span data-ttu-id="14981-768">Die com-Integration ermöglicht es dem App-V-Client, com-Objekte auf dem lokalen Betriebssystem und die Virtualisierung der Objekte zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="14981-768">COM integration allows the App-V Client to register COM objects on the local operating system and virtualization of the objects.</span></span> <span data-ttu-id="14981-769">Für die Zwecke dieses Dokuments erfordert die Integration von COM-Objekten zusätzliche Details.</span><span class="sxs-lookup"><span data-stu-id="14981-769">For the purposes of this document, the integration of COM objects requires additional detail.</span></span>

<span data-ttu-id="14981-770">App-V unterstützt das Registrieren von COM-Objekten aus dem Paket auf dem lokalen Betriebssystem mit zwei Prozesstypen: Out-of-Process-und in-Process-Prozesse.</span><span class="sxs-lookup"><span data-stu-id="14981-770">App-V supports registering COM objects from the package to the local operating system with two process types: Out-of-process and in-process.</span></span> <span data-ttu-id="14981-771">Das Registrieren von COM-Objekten erfolgt mit einer oder einer Kombination mehrerer Betriebsmodi für ein bestimmtes App-V-Paket, das aus, isoliert und integriert umfasst.</span><span class="sxs-lookup"><span data-stu-id="14981-771">Registering COM objects is accomplished with one or a combination of multiple modes of operation for a specific App-V package that includes off, Isolated, and Integrated.</span></span> <span data-ttu-id="14981-772">Der integrierte Modus ist entweder für den Out-of-Process-oder in-Process-Typ konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="14981-772">The integrated mode is configured for either the out-of-process or in-process type.</span></span> <span data-ttu-id="14981-773">Die Konfiguration von com-Modi und-Typen erfolgt mit dynamischen Konfigurationsdateien (deploymentconfig.xml oder userconfig.xml).</span><span class="sxs-lookup"><span data-stu-id="14981-773">Configuration of COM modes and types is accomplished with dynamic configuration files (deploymentconfig.xml or userconfig.xml).</span></span>

<span data-ttu-id="14981-774">Details zur App-V-Integration finden Sie unter: <https://go.microsoft.com/fwlink/?LinkId=392834> .</span><span class="sxs-lookup"><span data-stu-id="14981-774">Details on App-V integration are available at: <https://go.microsoft.com/fwlink/?LinkId=392834>.</span></span>

### <span data-ttu-id="14981-775">Software-Clients und Anwendungsfunktionen</span><span class="sxs-lookup"><span data-stu-id="14981-775">Software clients and application capabilities</span></span>

<span data-ttu-id="14981-776">App-V unterstützt bestimmte Software-Clients und Erweiterungspunkte für Anwendungsfunktionen, mit denen virtualisierte Anwendungen beim Software-Client des Betriebssystems registriert werden können.</span><span class="sxs-lookup"><span data-stu-id="14981-776">App-V supports specific software clients and application capabilities extension points that enable virtualized applications to be registered with the software client of the operating system.</span></span> <span data-ttu-id="14981-777">Dadurch können Benutzer Standard Programme für Vorgänge wie e-Mail, Chat und Media Player auswählen.</span><span class="sxs-lookup"><span data-stu-id="14981-777">This enables users to select default programs for operations like email, instant messaging, and media player.</span></span> <span data-ttu-id="14981-778">Dieser Vorgang wird in der Systemsteuerung mit dem festgelegten Programm Zugriffs-und Computer Standard durchgeführt und während der Sequenzierung in den Manifest-oder Dynamic Configuration-Dateien konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="14981-778">This operation is performed in the control panel with the Set Program Access and Computer Defaults, and configured during sequencing in the manifest or dynamic configuration files.</span></span> <span data-ttu-id="14981-779">Anwendungsfunktionen werden nur unterstützt, wenn die App-V-Anwendungen Global veröffentlicht werden.</span><span class="sxs-lookup"><span data-stu-id="14981-779">Application capabilities are only supported when the App-V applications are published globally.</span></span>

<span data-ttu-id="14981-780">Beispiel für die Software Clientregistrierung eines App-V-basierten e-Mail-Clients.</span><span class="sxs-lookup"><span data-stu-id="14981-780">Example of software client registration of an App-V based mail client.</span></span>

```xml
    <SoftwareClients Enabled="true">
      <ClientConfiguration EmailEnabled="true" />
      <Extensions>
        <Extension Category="AppV.SoftwareClient">
          <SoftwareClients>
            <EMail MakeDefault="true">
              <Name>Mozilla Thunderbird</Name>
              <Description>Mozilla Thunderbird</Description>
              <DefaultIcon>[{ProgramFilesX86}]\Mozilla Thunderbird\thunderbird.exe,0</DefaultIcon>
              <InstallationInformation>
                <RegistrationCommands>
                  <Reinstall>"[{ProgramFilesX86}]\Mozilla Thunderbird\uninstall\helper.exe" /SetAsDefaultAppGlobal</Reinstall>
                  <HideIcons>"[{ProgramFilesX86}]\Mozilla Thunderbird\uninstall\helper.exe" /HideShortcuts</HideIcons>
                  <ShowIcons>"[{ProgramFilesX86}]\Mozilla Thunderbird\uninstall\helper.exe" /ShowShortcuts</ShowIcons>
                </RegistrationCommands>
                <IconsVisible>1</IconsVisible>
                <OEMSettings />
              </InstallationInformation>
              <ShellCommands>
                <ApplicationId>[{ProgramFilesX86}]\Mozilla Thunderbird\thunderbird.exe</ApplicationId>
                <Open>"[{ProgramFilesX86}]\Mozilla Thunderbird\thunderbird.exe" -mail</Open>
              </ShellCommands>
              <MAPILibrary>[{ProgramFilesX86}]\Mozilla Thunderbird\mozMapi32_InUse.dll</MAPILibrary>
              <MailToProtocol>
                <Description>Thunderbird URL</Description>
                <EditFlags>2</EditFlags>
                <DefaultIcon>[{ProgramFilesX86}]\Mozilla Thunderbird\thunderbird.exe,0</DefaultIcon>
                <ShellCommands>
                  <ApplicationId>[{ProgramFilesX86}]\Mozilla Thunderbird\thunderbird.exe</ApplicationId>
                  <Open>"[{ProgramFilesX86}]\Mozilla Thunderbird\thunderbird.exe" -osint -compose "%1"</Open>
                </ShellCommands>
              </MailToProtocol>
            </EMail>
          </SoftwareClients>
        </Extension>
      </Extensions>
    </SoftwareClients>
```

<span data-ttu-id="14981-781">**Hinweis**  In diesem Beispiel:</span><span class="sxs-lookup"><span data-stu-id="14981-781">**Note** In this example:</span></span>

-   `<ClientConfiguration EmailEnabled="true" />` <span data-ttu-id="14981-782">ist die Gesamteinstellung für Software Clients zum Integrieren von e-Mail-Clients</span><span class="sxs-lookup"><span data-stu-id="14981-782">is the overall Software Clients setting to integrate Email clients</span></span>

-   `<EMail MakeDefault="true">` <span data-ttu-id="14981-783">ist die Kennzeichnung, um einen bestimmten e-Mail-Client als Standard-e-Mail-Client einzurichten</span><span class="sxs-lookup"><span data-stu-id="14981-783">is the flag to set a particular Email client as the default Email client</span></span>

-   `<MAPILibrary>[{ProgramFilesX86}]\Mozilla Thunderbird\mozMapi32_InUse.dll</MAPILibrary>` <span data-ttu-id="14981-784">ist die MAPI-DLL-Registrierung</span><span class="sxs-lookup"><span data-stu-id="14981-784">is the MAPI dll registration</span></span>

 

### <span data-ttu-id="14981-785">URL-Protokollhandler</span><span class="sxs-lookup"><span data-stu-id="14981-785">URL Protocol handler</span></span>

<span data-ttu-id="14981-786">Anwendungen werden nicht immer ausdrücklich als virtualisierte Anwendungen bezeichnet, die den Dateityp Aufruf verwenden.</span><span class="sxs-lookup"><span data-stu-id="14981-786">Applications do not always specifically called virtualized applications utilizing file type invocation.</span></span> <span data-ttu-id="14981-787">In einer Anwendung, die das Einbetten eines mailto:-Links in ein Dokument oder eine Webseite unterstützt, klickt der Benutzer beispielsweise auf einen mailto:-Link und erwartet, dass er seinen registrierten e-Mail-Client erhält.</span><span class="sxs-lookup"><span data-stu-id="14981-787">For, example, in an application that supports embedding a mailto: link inside a document or web page, the user clicks on a mailto: link and expects to get their registered mail client.</span></span> <span data-ttu-id="14981-788">App-V unterstützt URL-Protokollhandler, die pro Paket mit dem lokalen Betriebssystem registriert werden können.</span><span class="sxs-lookup"><span data-stu-id="14981-788">App-V supports URL Protocol handlers that can be registered on a per-package basis with the local operating system.</span></span> <span data-ttu-id="14981-789">Während der Sequenzierung werden die URL-Protokollhandler automatisch dem Paket hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="14981-789">During sequencing, the URL protocol handlers are automatically added to the package.</span></span>

<span data-ttu-id="14981-790">In Situationen, in denen es mehr als eine Anwendung gibt, die den spezifischen URL-Protokollhandler registrieren kann, können die dynamischen Konfigurationsdateien verwendet werden, um das Verhalten zu ändern und dieses Feature für eine Anwendung zu unterdrücken oder zu deaktivieren, die nicht die primäre Anwendung sein sollte, die gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="14981-790">For situations where there is more than one application that could register the specific URL Protocol handler, the dynamic configuration files can be utilized to modify the behavior and suppress or disable this feature for an application that should not be the primary application launched.</span></span>

### <span data-ttu-id="14981-791">AppPath</span><span class="sxs-lookup"><span data-stu-id="14981-791">AppPath</span></span>

<span data-ttu-id="14981-792">Der AppPath-Erweiterungspunkt unterstützt das direkte Aufrufen von App-V-Anwendungen aus dem Betriebssystem.</span><span class="sxs-lookup"><span data-stu-id="14981-792">The AppPath extension point supports calling App-V applications directly from the operating system.</span></span> <span data-ttu-id="14981-793">Dies erfolgt in der Regel über den Startbildschirm, je nach Betriebssystem, wodurch Administratoren den Zugriff auf App-V-Anwendungen über Betriebssystembefehle oder Skripts ermöglichen können, ohne den spezifischen Pfad zur ausführbaren Datei aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="14981-793">This is typically accomplished from the Run or Start Screen, depending on the operating system, which enables administrators to provide access to App-V applications from operating system commands or scripts without calling the specific path to the executable.</span></span> <span data-ttu-id="14981-794">Sie vermeidet daher die Änderung der Umgebungsvariablen "System Path" auf allen Systemen, wie Sie während der Veröffentlichung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="14981-794">It therefore avoids modifying the system path environment variable on all systems, as it is accomplished during publishing.</span></span>

<span data-ttu-id="14981-795">Der AppPath-Erweiterungspunkt wird entweder im Manifest oder in den dynamischen Konfigurationsdateien konfiguriert und während der Veröffentlichung für den Benutzer in der Registrierung auf dem lokalen Computer gespeichert.</span><span class="sxs-lookup"><span data-stu-id="14981-795">The AppPath extension point is configured either in the manifest or in the dynamic configuration files and is stored in the registry on the local machine during publishing for the user.</span></span> <span data-ttu-id="14981-796">Weitere Informationen zur AppPath-Überprüfung finden Sie unter: <https://go.microsoft.com/fwlink/?LinkId=392835> .</span><span class="sxs-lookup"><span data-stu-id="14981-796">For additional information on AppPath review: <https://go.microsoft.com/fwlink/?LinkId=392835>.</span></span>

### <span data-ttu-id="14981-797">Virtuelle Anwendung</span><span class="sxs-lookup"><span data-stu-id="14981-797">Virtual application</span></span>

<span data-ttu-id="14981-798">Dieses Subsystem stellt eine Liste der während der Sequenzierung erfassten Anwendungen bereit, die normalerweise von anderen App-V-Komponenten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="14981-798">This subsystem provides a list of applications captured during sequencing which is usually consumed by other App-V components.</span></span> <span data-ttu-id="14981-799">Die Integration von Erweiterungspunkten, die zu einer bestimmten Anwendung gehören, kann mit dynamischen Konfigurationsdateien deaktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="14981-799">Integration of extension points belonging to a particular application can be disabled using dynamic configuration files.</span></span> <span data-ttu-id="14981-800">Wenn ein Paket beispielsweise zwei Anwendungen enthält, ist es möglich, alle Erweiterungspunkte zu deaktivieren, die zu einer Anwendung gehören, damit nur Erweiterungspunkte anderer Anwendungen integriert werden können.</span><span class="sxs-lookup"><span data-stu-id="14981-800">For example, if a package contains two applications, it is possible to disable all extension points belonging to one application, in order to allow only integration of extension points of other application.</span></span>

### <span data-ttu-id="14981-801">Erweiterungspunkt Regeln</span><span class="sxs-lookup"><span data-stu-id="14981-801">Extension point rules</span></span>

<span data-ttu-id="14981-802">Die oben beschriebenen Erweiterungspunkte sind in das Betriebssystem integriert, je nachdem, wie die Pakete veröffentlicht wurden.</span><span class="sxs-lookup"><span data-stu-id="14981-802">The extension points described above are integrated into the operating system based on how the packages has been published.</span></span> <span data-ttu-id="14981-803">Bei der globalen Veröffentlichung werden Erweiterungspunkte an öffentlichen Speicherorten platziert, an denen die Benutzer Veröffentlichung Erweiterungspunkte an Benutzerspeicherorten platziert.</span><span class="sxs-lookup"><span data-stu-id="14981-803">Global publishing places extension points in public machine locations, where user publishing places extension points in user locations.</span></span> <span data-ttu-id="14981-804">Beispiel: eine auf dem Desktop erstellte und Global veröffentlichte Verknüpfung führt zu den Dateidaten für die Verknüpfung (%Public%\\Desktop) und den Registrierungsdaten (HKLM\\Software\\Classes).</span><span class="sxs-lookup"><span data-stu-id="14981-804">For example a shortcut that is created on the desktop and published globally will result in the file data for the shortcut (%Public%\\Desktop) and the registry data (HKLM\\Software\\Classes).</span></span> <span data-ttu-id="14981-805">Die gleiche Verknüpfung hätte Dateidaten (%USERPROFILE%\\Desktop) und Registrierungsdaten (HKCU\\Software\\Classes).</span><span class="sxs-lookup"><span data-stu-id="14981-805">The same shortcut would have file data (%UserProfile%\\Desktop) and registry data (HKCU\\Software\\Classes).</span></span>

<span data-ttu-id="14981-806">Erweiterungspunkte werden nicht alle auf die gleiche Weise veröffentlicht, wobei für einige Erweiterungspunkte eine globale Veröffentlichung erforderlich ist und andere eine Sequenzierung des jeweiligen Betriebssystems und der Architektur erfordern, in der Sie zugestellt werden.</span><span class="sxs-lookup"><span data-stu-id="14981-806">Extension points are not all published the same way, where some extension points will require global publishing and others require sequencing on the specific operating system and architecture where they are delivered.</span></span> <span data-ttu-id="14981-807">Nachfolgend finden Sie eine Tabelle, in der diese beiden Schlüssel Regeln beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="14981-807">Below is a table that describes these two key rules.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="14981-808">Virtuelle Erweiterung</span><span class="sxs-lookup"><span data-stu-id="14981-808">Virtual Extension</span></span></th>
<th align="left"><span data-ttu-id="14981-809">Erfordert eine Ziel-OS-Sequenzierung</span><span class="sxs-lookup"><span data-stu-id="14981-809">Requires target OS Sequencing</span></span></th>
<th align="left"><span data-ttu-id="14981-810">Erfordert globales publizieren</span><span class="sxs-lookup"><span data-stu-id="14981-810">Requires Global Publishing</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="14981-811">Tastenkombination</span><span class="sxs-lookup"><span data-stu-id="14981-811">Shortcut</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="14981-812">Dateitypzuordnung</span><span class="sxs-lookup"><span data-stu-id="14981-812">File Type Association</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="14981-813">URL-Protokolle</span><span class="sxs-lookup"><span data-stu-id="14981-813">URL Protocols</span></span></p></td>
<td align="left"><p><span data-ttu-id="14981-814">X</span><span class="sxs-lookup"><span data-stu-id="14981-814">X</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="14981-815">AppPaths</span><span class="sxs-lookup"><span data-stu-id="14981-815">AppPaths</span></span></p></td>
<td align="left"><p><span data-ttu-id="14981-816">X</span><span class="sxs-lookup"><span data-stu-id="14981-816">X</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="14981-817">COM-Modus</span><span class="sxs-lookup"><span data-stu-id="14981-817">COM Mode</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="14981-818">Software-Client</span><span class="sxs-lookup"><span data-stu-id="14981-818">Software Client</span></span></p></td>
<td align="left"><p><span data-ttu-id="14981-819">X</span><span class="sxs-lookup"><span data-stu-id="14981-819">X</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="14981-820">Anwendungsfunktionen</span><span class="sxs-lookup"><span data-stu-id="14981-820">Application Capabilities</span></span></p></td>
<td align="left"><p><span data-ttu-id="14981-821">X</span><span class="sxs-lookup"><span data-stu-id="14981-821">X</span></span></p></td>
<td align="left"><p><span data-ttu-id="14981-822">X</span><span class="sxs-lookup"><span data-stu-id="14981-822">X</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="14981-823">Kontextmenü Handler</span><span class="sxs-lookup"><span data-stu-id="14981-823">Context Menu Handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="14981-824">X</span><span class="sxs-lookup"><span data-stu-id="14981-824">X</span></span></p></td>
<td align="left"><p><span data-ttu-id="14981-825">X</span><span class="sxs-lookup"><span data-stu-id="14981-825">X</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="14981-826">Drag & Drop-Handler</span><span class="sxs-lookup"><span data-stu-id="14981-826">Drag-and-drop Handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="14981-827">X</span><span class="sxs-lookup"><span data-stu-id="14981-827">X</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="14981-828">Datenobjekt-Handler</span><span class="sxs-lookup"><span data-stu-id="14981-828">Data Object Handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="14981-829">X</span><span class="sxs-lookup"><span data-stu-id="14981-829">X</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="14981-830">Eigenschaftentabellen-Handler</span><span class="sxs-lookup"><span data-stu-id="14981-830">Property Sheet Handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="14981-831">X</span><span class="sxs-lookup"><span data-stu-id="14981-831">X</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="14981-832">Infotipp-Handler</span><span class="sxs-lookup"><span data-stu-id="14981-832">Infotip Handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="14981-833">X</span><span class="sxs-lookup"><span data-stu-id="14981-833">X</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="14981-834">Spalten Handler</span><span class="sxs-lookup"><span data-stu-id="14981-834">Column Handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="14981-835">X</span><span class="sxs-lookup"><span data-stu-id="14981-835">X</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="14981-836">Shell-Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="14981-836">Shell Extensions</span></span></p></td>
<td align="left"><p><span data-ttu-id="14981-837">X</span><span class="sxs-lookup"><span data-stu-id="14981-837">X</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="14981-838">Browser Helper-Objekt</span><span class="sxs-lookup"><span data-stu-id="14981-838">Browser Helper Object</span></span></p></td>
<td align="left"><p><span data-ttu-id="14981-839">X</span><span class="sxs-lookup"><span data-stu-id="14981-839">X</span></span></p></td>
<td align="left"><p><span data-ttu-id="14981-840">X</span><span class="sxs-lookup"><span data-stu-id="14981-840">X</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="14981-841">Active X-Objekt</span><span class="sxs-lookup"><span data-stu-id="14981-841">Active X Object</span></span></p></td>
<td align="left"><p><span data-ttu-id="14981-842">X</span><span class="sxs-lookup"><span data-stu-id="14981-842">X</span></span></p></td>
<td align="left"><p><span data-ttu-id="14981-843">X</span><span class="sxs-lookup"><span data-stu-id="14981-843">X</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-dynamic-config"></a><span data-ttu-id="14981-844">Verarbeitung dynamischer Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="14981-844">Dynamic configuration processing</span></span>


<span data-ttu-id="14981-845">Das Bereitstellen von App-V-Paketen auf einem Computer oder Benutzer ist sehr einfach.</span><span class="sxs-lookup"><span data-stu-id="14981-845">Deploying App-V packages to one machine or user is very simple.</span></span> <span data-ttu-id="14981-846">Da Organisationen AppV-Anwendungen jedoch über Unternehmensgrenzen hinweg sowie über geografische und politische Grenzen hinweg bereitstellen, ist die Möglichkeit, eine Anwendung einmal mit einem Satz von Einstellungen zu sequenzieren, unmöglich.</span><span class="sxs-lookup"><span data-stu-id="14981-846">However, as organizations deploy AppV applications across business lines and geographic and political boundaries, the ability to sequence an application one time with one set of settings becomes impossible.</span></span> <span data-ttu-id="14981-847">App-V wurde für dieses Szenario entwickelt, da es bestimmte Einstellungen und Konfigurationen während der Sequenzierung in der Manifestdatei erfasst, aber auch Änderungen mit dynamischen Konfigurationsdateien unterstützt.</span><span class="sxs-lookup"><span data-stu-id="14981-847">App-V was designed for this scenario, as it captures specific settings and configurations during sequencing in the Manifest file, but also supports modification with Dynamic Configuration files.</span></span>

<span data-ttu-id="14981-848">Mit der dynamischen App-V-Konfiguration können Sie eine Richtlinie für ein Paket entweder auf Computerebene oder auf Benutzerebene angeben.</span><span class="sxs-lookup"><span data-stu-id="14981-848">App-V dynamic configuration allows for specifying a policy for a package either at the machine level or at the user level.</span></span> <span data-ttu-id="14981-849">Mit den Dynamic Configuration-Dateien können Sequenzierungs Ingenieure die Konfiguration eines Pakets nach der Reihenfolge ändern, um die Anforderungen einzelner Benutzer-oder Computergruppen zu erfüllen.</span><span class="sxs-lookup"><span data-stu-id="14981-849">The Dynamic Configuration files enable sequencing engineers to modify the configuration of a package, post-sequencing, to address the needs of individual groups of users or machines.</span></span> <span data-ttu-id="14981-850">In einigen Fällen kann es notwendig sein, Änderungen an der Anwendung vorzunehmen, um die richtige Funktionalität innerhalb der App-V-Umgebung bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="14981-850">In some instances it may be necessary to make modifications to the application to provide proper functionality within the App-V environment.</span></span> <span data-ttu-id="14981-851">Beispielsweise kann es erforderlich sein, Änderungen an den \ _ \ \* config.xml-Dateien vorzunehmen, damit bestimmte Aktionen während der Ausführung der Anwendung zu einem bestimmten Zeitpunkt ausgeführt werden können, wie das Deaktivieren einer mailto-Erweiterung, um zu verhindern, dass eine virtualisierte Anwendung diese Erweiterung aus einer anderen Anwendung überschreibt.</span><span class="sxs-lookup"><span data-stu-id="14981-851">For example, it may be necessary to make modifications to the \_\*config.xml files to allow certain actions to be performed at a specified time during the execution of the application, like disabling a mailto extension to prevent a virtualized application from overwriting that extension from another application.</span></span>

<span data-ttu-id="14981-852">App-V-Pakete enthalten die Manifestdatei innerhalb der AppV-Paketdatei, die für Sequenz Vorgänge repräsentativ ist und die Richtlinie der Wahl ist, wenn einem bestimmten Paket keine dynamischen Konfigurationsdateien zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="14981-852">App-V Packages contain the Manifest file inside of the appv package file, which is representative of sequencing operations and is the policy of choice unless Dynamic Configuration files are assigned to a specific package.</span></span> <span data-ttu-id="14981-853">Nach der Sequenzierung können die dynamischen Konfigurationsdateien geändert werden, um die Veröffentlichung einer Anwendung für verschiedene Desktops oder Benutzer mit unterschiedlichen Erweiterungspunkten zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="14981-853">Post-sequencing, the Dynamic Configuration files can be modified to allow the publishing of an application to different desktops or users with different extension points.</span></span> <span data-ttu-id="14981-854">Die beiden dynamischen Konfigurationsdateien sind die Dynamic Deployment Configuration (DDC)-und Dynamic User Configuration (Duc)-Dateien.</span><span class="sxs-lookup"><span data-stu-id="14981-854">The two Dynamic Configuration Files are the Dynamic Deployment Configuration (DDC) and Dynamic User Configuration (DUC) files.</span></span> <span data-ttu-id="14981-855">In diesem Abschnitt wird die Kombination der Manifest-und Dynamic Configuration-Dateien behandelt.</span><span class="sxs-lookup"><span data-stu-id="14981-855">This section focuses on the combination of the manifest and dynamic configuration files.</span></span>

### <span data-ttu-id="14981-856">Beispiel für dynamische Konfigurationsdateien</span><span class="sxs-lookup"><span data-stu-id="14981-856">Example for dynamic configuration files</span></span>

<span data-ttu-id="14981-857">Das folgende Beispiel zeigt die Kombination aus Manifest, Bereitstellungskonfiguration und Benutzerkonfigurationsdateien nach der Veröffentlichung und im normalen Betrieb.</span><span class="sxs-lookup"><span data-stu-id="14981-857">The example below shows the combination of the Manifest, Deployment Configuration and User Configuration files after publishing and during normal operation.</span></span> <span data-ttu-id="14981-858">Diese Beispiele sind verkürzte Beispiele für die einzelnen Dateien.</span><span class="sxs-lookup"><span data-stu-id="14981-858">These examples are abbreviated examples of each of the files.</span></span> <span data-ttu-id="14981-859">Der Zweck besteht darin, die Kombination der Dateien nur anzuzeigen und keine vollständige Beschreibung der in den einzelnen Dateien verfügbaren spezifischen Kategorien zu sein.</span><span class="sxs-lookup"><span data-stu-id="14981-859">The purpose is show the combination of the files only and not to be a complete description of the specific categories available in each of the files.</span></span> <span data-ttu-id="14981-860">Weitere Informationen finden Sie im App-V 5-Sequenzierungs Handbuch unter:</span><span class="sxs-lookup"><span data-stu-id="14981-860">For more information review the App-V 5 Sequencing Guide at:</span></span> <https://go.microsoft.com/fwlink/?LinkID=269810>

**<span data-ttu-id="14981-861">Manifest</span><span class="sxs-lookup"><span data-stu-id="14981-861">Manifest</span></span>**

```xml
<appv:Extension Category="AppV.Shortcut">
     <appv:Shortcut>
          <appv:File>[{Common Programs}]\7-Zip\7-Zip File Manager.lnk</appv:File>
          <appv:Target>[{AppVPackageRoot}]\7zFM.exe</appv:Target>
          <appv:Icon>[{AppVPackageRoot}]\7zFM exe.O.ico</appv:Icon>
     </appv:Shortcut>
</appv:Extension>
```

**<span data-ttu-id="14981-862">Bereitstellungskonfiguration</span><span class="sxs-lookup"><span data-stu-id="14981-862">Deployment Configuration</span></span>**

```xml
<MachineConfiguration>
     <Subsystems>
          <Registry>
               <Include>
                    <Key Path= "\REGISTRY\Machine\Software\7zip">
                    <Value Type="REG_SZ" Name="Config" Data="1234"/>
                    </Key>
               </Include>
          </Registry>
     </Subsystems>
```

**<span data-ttu-id="14981-863">Benutzerkonfiguration</span><span class="sxs-lookup"><span data-stu-id="14981-863">User Configuration</span></span>**

```xml
<UserConfiguration>
     <Subsystems>
<appv:ExtensionCategory="AppV.Shortcut">
     <appv:Shortcut>
          <appv:File>[{Desktop}]\7-Zip\7-Zip File Manager.lnk</appv:File>
          <appv:Target>[{AppVPackageRoot}]\7zFM.exe</appv:Target>
          <appv:Icon>[{AppVPackageRoot}]\7zFM exe.O.ico</appv:Icon>
     </appv:Shortcut>
</appv:Extension>
     </Subsystems>
<UserConfiguration>
     <Subsystems>
<appv:Extension Category="AppV.Shortcut">
     <appv:Shortcut>
          <appv:Fìle>[{Desktop}]\7-Zip\7-Zip File Manager.lnk</appv:File>
          <appv:Target>[{AppVPackageRoot}]\7zFM.exe</appv:Target>
          <appv:Icon>[{AppVPackageRoot}]\7zFM.exe.O.ico</appv:Icon>
     </appv:Shortcut>
     <appv:Shortcut>
          <appv:File>[{Common Programs}]\7-Zip\7-Zip File Manager.Ink</appv:File>
          <appv:Target>[{AppVPackageRoot}]\7zFM.exe</appv:Target>
          <appv:Icon>[{AppVPackageRoot)]\7zFM.exe.O.ico</appv: Icon>
     </appv:Shortcut>
</appv:Extension>
     </Subsystems>
<MachineConfiguration>
     <Subsystems>
          <Registry>
               <Include>
                    <Key Path="\REGISTRY\Machine\Software\7zip">
                    <Value Type=”REG_SZ" Name="Config" Data="1234"/>
               </Include>
          </Registry>
     </Subsystems>
```

## <a href="" id="bkmk-sidebyside-assemblies"></a><span data-ttu-id="14981-864">Nebeneinander angeordnete Assemblys</span><span class="sxs-lookup"><span data-stu-id="14981-864">Side-by-side assemblies</span></span>


<span data-ttu-id="14981-865">App-V unterstützt das automatische Verpacken von nebeneinander angeordneten (SxS)-Assemblys während der Sequenzierung und Bereitstellung auf dem Client während der Veröffentlichung virtueller Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="14981-865">App-V supports the automatic packaging of side-by-side (SxS) assemblies during sequencing and deployment on the client during virtual application publishing.</span></span> <span data-ttu-id="14981-866">App-V 5 SP2 unterstützt das Aufzeichnen von SxS-Assemblys während der Sequenzierung für Assemblys, die auf dem Sequenzcomputer nicht vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="14981-866">App-V 5 SP2 supports capturing SxS assemblies during sequencing for assemblies not present on the sequencing machine.</span></span> <span data-ttu-id="14981-867">Und für Assemblys, bestehend aus Visual C++ (Version 8 und neuer) und/oder MSXML-Laufzeit, erkennt und erfasst der Sequencer diese Abhängigkeiten automatisch, selbst wenn Sie während der Überwachung nicht installiert wurden.</span><span class="sxs-lookup"><span data-stu-id="14981-867">And for assemblies consisting of Visual C++ (Version 8 and newer) and/or MSXML run-time, the Sequencer will automatically detect and capture these dependencies even if they were not installed during monitoring.</span></span> <span data-ttu-id="14981-868">Das Feature für nebeneinander angeordnete Assemblys entfernt die Einschränkungen früherer Versionen von App-v, wobei der APP-v-Sequenzer keine bereits auf der Sequenzierungs Arbeitsstation vorhandenen Assemblys erfasst und die Assemblys privatisiert hat, die auf eine Bit-Version pro Paket beschränkt sind.</span><span class="sxs-lookup"><span data-stu-id="14981-868">The Side by Side assemblies feature removes the limitations of previous versions of App-V, where the App-V Sequencer did not capture assemblies already present on the sequencing workstation, and privatizing the assemblies which limited to one bit version per package.</span></span> <span data-ttu-id="14981-869">Dieses Verhalten hat dazu geführt, dass App-V-Anwendungen für Clients fehlen, die die erforderlichen SxS-Assemblys aufweisen, wodurch Anwendungsstart Fehler verursacht wurden.</span><span class="sxs-lookup"><span data-stu-id="14981-869">This behavior resulted in deployed App-V applications to clients missing the required SxS assemblies, causing application launch failures.</span></span> <span data-ttu-id="14981-870">Dieser zwang den Verpackungsprozess, zu dokumentieren und sicherzustellen, dass alle für Pakete erforderlichen Assemblys lokal auf dem Clientbetriebssystem des Benutzers installiert wurden, um die Unterstützung für die virtuellen Anwendungen zu gewährleisten.</span><span class="sxs-lookup"><span data-stu-id="14981-870">This forced the packaging process to document and then ensure that all assemblies required for packages were locally installed on the user’s client operating system to ensure support for the virtual applications.</span></span> <span data-ttu-id="14981-871">Auf der Grundlage der Anzahl der Assemblys und der fehlenden Anwendungsdokumentation für die erforderlichen Abhängigkeiten war diese Aufgabe sowohl eine Herausforderung für die Verwaltung als auch die Implementierung.</span><span class="sxs-lookup"><span data-stu-id="14981-871">Based on the number of assemblies and the lack of application documentation for the required dependencies, this task was both a management and implementation challenge.</span></span>

<span data-ttu-id="14981-872">Die Unterstützung von nebeneinander angeordneten Assemblys in App-V bietet die folgenden Features.</span><span class="sxs-lookup"><span data-stu-id="14981-872">Side by Side Assembly support in App-V has the following features.</span></span>

-   <span data-ttu-id="14981-873">Automatische Erfassung von SxS-Assemblierungen während der Sequenzierung, unabhängig davon, ob die Assembly bereits auf der Sequenzierungs Arbeitsstation installiert war.</span><span class="sxs-lookup"><span data-stu-id="14981-873">Automatic captures of SxS assembly during Sequencing, regardless of whether the assembly was already installed on the sequencing workstation.</span></span>

-   <span data-ttu-id="14981-874">Der App-V-Client installiert erforderliche SxS-Assemblys automatisch zur Veröffentlichungszeit auf dem Clientcomputer, wenn diese nicht vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="14981-874">The App-V Client automatically installs required SxS assemblies to the client computer at publishing time when they are not present.</span></span>

-   <span data-ttu-id="14981-875">Der Sequencer meldet die VC-Laufzeitabhängigkeit in Sequencer-Berichterstattungsmechanismus.</span><span class="sxs-lookup"><span data-stu-id="14981-875">The Sequencer reports the VC run-time dependency in Sequencer reporting mechanism.</span></span>

-   <span data-ttu-id="14981-876">Der Sequencer ermöglicht die Entscheidung, die Assemblys, die bereits auf dem Sequencer installiert sind, nicht zu verpacken, wodurch Szenarien unterstützt werden, in denen die Assemblys zuvor auf den Zielcomputern installiert wurden.</span><span class="sxs-lookup"><span data-stu-id="14981-876">The Sequencer allows opting to not package the assemblies that are already installed on the Sequencer, supporting scenarios where the assemblies have previously been installed on the target computers.</span></span>

### <span data-ttu-id="14981-877">Automatisches Veröffentlichen von SxS-Assemblys</span><span class="sxs-lookup"><span data-stu-id="14981-877">Automatic publishing of SxS assemblies</span></span>

<span data-ttu-id="14981-878">Während der Veröffentlichung eines App-v-Pakets mit SxS-Assemblys überprüft der APP-v-Client, ob die Assembly auf dem Computer vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="14981-878">During publishing of an App-V package with SxS assemblies the App-V Client will check for the presence of the assembly on the machine.</span></span> <span data-ttu-id="14981-879">Wenn die Assembly nicht vorhanden ist, stellt der Client die Assembly auf dem Computer bereit.</span><span class="sxs-lookup"><span data-stu-id="14981-879">If the assembly does not exist, the client will deploy the assembly to the machine.</span></span> <span data-ttu-id="14981-880">Pakete, die Bestandteil von Verbindungsgruppen sind, basieren auf den nebeneinander angeordneten Baugruppen Installationen, die Bestandteil der Basispakete sind, da die Verbindungsgruppe keine Informationen zur Assemblierungs Installation enthält.</span><span class="sxs-lookup"><span data-stu-id="14981-880">Packages that are part of connection groups will rely on the Side by Side assembly installations that are part of the base packages, as the connection group does not contain any information about assembly installation.</span></span>

<span data-ttu-id="14981-881">**Hinweis**  Beim Aufheben der Veröffentlichung oder beim Entfernen eines Pakets mit einer Assembly werden die Assemblys für dieses Paket nicht entfernt.</span><span class="sxs-lookup"><span data-stu-id="14981-881">**Note** UnPublishing or removing a package with an assembly does not remove the assemblies for that package.</span></span>

 

## <a href="" id="bkmk-client-logging"></a><span data-ttu-id="14981-882">Client Protokollierung</span><span class="sxs-lookup"><span data-stu-id="14981-882">Client logging</span></span>


<span data-ttu-id="14981-883">Der App-V-Client protokolliert Informationen im Windows-Ereignisprotokoll im standardmäßigen etw-Format.</span><span class="sxs-lookup"><span data-stu-id="14981-883">The App-V client logs information to the Windows Event log in standard ETW format.</span></span> <span data-ttu-id="14981-884">Die spezifischen App-V-Ereignisse finden Sie in der Ereignisanzeige unter Anwendungen und Dienste Logs\\Microsoft\\AppV\\Client.</span><span class="sxs-lookup"><span data-stu-id="14981-884">The specific App-V events can be found in the event viewer, under Applications and Services Logs\\Microsoft\\AppV\\Client.</span></span>

<span data-ttu-id="14981-885">**Hinweis**  In App-V 5,0 SP3 wurden einige Protokolle konsolidiert und an den folgenden Speicherort verschoben:</span><span class="sxs-lookup"><span data-stu-id="14981-885">**Note** In App-V 5.0 SP3, some logs have been consolidated and moved to the following location:</span></span>

`Event logs/Applications and Services Logs/Microsoft/AppV/ServiceLog`

<span data-ttu-id="14981-886">Eine Liste der verschobenen Protokolle finden Sie unter [Informationen zu App-V 5,0 SP3](about-app-v-50-sp3.md#bkmk-event-logs-moved).</span><span class="sxs-lookup"><span data-stu-id="14981-886">For a list of the moved logs, see [About App-V 5.0 SP3](about-app-v-50-sp3.md#bkmk-event-logs-moved).</span></span>

 

<span data-ttu-id="14981-887">Nachfolgend werden drei spezifische Kategorien von Ereignissen aufgezeichnet.</span><span class="sxs-lookup"><span data-stu-id="14981-887">There are three specific categories of events recorded described below.</span></span>

<span data-ttu-id="14981-888">**Administrator**: protokolliert Ereignisse für Konfigurationen, die auf den App-V-Client angewendet werden, und enthält die primären Warnungen und Fehler.</span><span class="sxs-lookup"><span data-stu-id="14981-888">**Admin**: Logs events for configurations being applied to the App-V Client, and contains the primary warnings and errors.</span></span>

<span data-ttu-id="14981-889">**Betriebsbereit**: protokolliert die allgemeine App-v-Ausführung und-Verwendung einzelner Komponenten und erstellt ein Überwachungsprotokoll der APP-v-Vorgänge, die auf dem App-v-Client abgeschlossen wurden.</span><span class="sxs-lookup"><span data-stu-id="14981-889">**Operational**: Logs the general App-V execution and usage of individual components creating an audit log of the App-V operations that have been completed on the App-V Client.</span></span>

<span data-ttu-id="14981-890">**Virtuelle Anwendung**: protokolliert die Einführung virtueller Anwendungen und die Verwendung von Virtualisierungs-Subsysteme.</span><span class="sxs-lookup"><span data-stu-id="14981-890">**Virtual Application**: Logs virtual application launches and use of virtualization subsystems.</span></span>






 

 





