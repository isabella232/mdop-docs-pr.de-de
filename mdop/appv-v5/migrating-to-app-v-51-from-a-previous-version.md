---
title: Migrieren zu App-V 5.1 von einer früheren Version
description: Migrieren zu App-V 5.1 von einer früheren Version
author: dansimp
ms.assetid: e7ee0edc-7544-4c0a-aaca-d922a33bc1bb
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 7fb6ddbfed4f6fd1ae9613d2ee86361a51918a65
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805063"
---
# <span data-ttu-id="2e55b-103">Migrieren zu App-V 5.1 von einer früheren Version</span><span class="sxs-lookup"><span data-stu-id="2e55b-103">Migrating to App-V 5.1 from a Previous Version</span></span>


<span data-ttu-id="2e55b-104">Mit Microsoft Application Virtualization (app-v) 5,1 können Sie Ihre vorhandene App-v 4,6-oder App-v 5,0-Infrastruktur auf die flexiblere, integrierte und einfacher zu verwaltende App-v 5,1-Infrastruktur migrieren.</span><span class="sxs-lookup"><span data-stu-id="2e55b-104">With Microsoft Application Virtualization (App-V) 5.1, you can migrate your existing App-V 4.6 or App-V 5.0 infrastructure to the more flexible, integrated, and easier to manage App-V 5.1 infrastructure.</span></span>
<span data-ttu-id="2e55b-105">Sie können jedoch nicht direkt von App-v 4. x zu app-v 5,1 migrieren, sondern müssen zuerst zu app-v 5,0 migrieren.</span><span class="sxs-lookup"><span data-stu-id="2e55b-105">However, you cannot migrate directly from App-V 4.x to App-V 5.1, you must migrate to App-V 5.0 first.</span></span> <span data-ttu-id="2e55b-106">Weitere Informationen zum Migrieren von App-v 4. x zu app-v 5,0 finden Sie unter [Migrieren von einer früheren Version](migrating-from-a-previous-version-app-v-50.md) .</span><span class="sxs-lookup"><span data-stu-id="2e55b-106">For more information on migrating from App-V 4.x to App-V 5.0, see [Migrating from a Previous Version](migrating-from-a-previous-version-app-v-50.md)</span></span>  

<span data-ttu-id="2e55b-107">**Hinweis**  App-v 5,1-Pakete sind genauso wie App-v 5,0-Pakete.</span><span class="sxs-lookup"><span data-stu-id="2e55b-107">**Note** App-V 5.1 packages are exactly the same as App-V 5.0 packages.</span></span> <span data-ttu-id="2e55b-108">Es wurde keine Änderung des Paketformats zwischen den Versionen vorgenommen, und daher ist es nicht erforderlich, App-v 5,0-Pakete in App-v 5,1-Pakete zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="2e55b-108">There has been no change in the package format between the versions and therefore, there is no need to convert App-V 5.0 packages to App-V 5.1 packages.</span></span>

<span data-ttu-id="2e55b-109">Weitere Informationen zu den Unterschieden zwischen App-v 4,6 und App-v 5,1 finden Sie unter **Unterschiede zwischen App-v 4,6 und App-v 5,0 im Abschnitt** [über APP-v 5,0](about-app-v-50.md).</span><span class="sxs-lookup"><span data-stu-id="2e55b-109">For more information about the differences between App-V 4.6 and App-V 5.1, see the **Differences between App-V 4.6 and App-V 5.0 section** of [About App-V 5.0](about-app-v-50.md).</span></span>

 

## <a href="" id="bkmk-pkgconvimprove"></a><span data-ttu-id="2e55b-110">Verbesserungen des App-V 5,1-Paket Konverters</span><span class="sxs-lookup"><span data-stu-id="2e55b-110">Improvements to the App-V 5.1 Package Converter</span></span>


<span data-ttu-id="2e55b-111">Sie können jetzt den Paket Konverter verwenden, um App-V 4,6-Pakete zu konvertieren, die Skripts enthalten, und Registrierungsinformationen und Skripts aus den Dateien des Quell-OSD sind jetzt in der Ausgabe des Paket Konverters enthalten.</span><span class="sxs-lookup"><span data-stu-id="2e55b-111">You can now use the package converter to convert App-V 4.6 packages that contain scripts, and registry information and scripts from source .osd files are now included in package converter output.</span></span>

<span data-ttu-id="2e55b-112">Sie können auch den `–OSDsToIncludeInPackage` Parameter mit dem `ConvertFrom-AppvLegacyPackage` Cmdlet verwenden, um anzugeben, welche OSD-Dateiinformationen konvertiert und in das neue Paket gestellt werden.</span><span class="sxs-lookup"><span data-stu-id="2e55b-112">You can also use the `–OSDsToIncludeInPackage` parameter with the `ConvertFrom-AppvLegacyPackage` cmdlet to specify which .osd files’ information is converted and placed within the new package.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="2e55b-113">Neu in App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="2e55b-113">New in App-V 5.1</span></span></th>
<th align="left"><span data-ttu-id="2e55b-114">Vor App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="2e55b-114">Prior to App-V 5.1</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2e55b-115">Neue XML-Dateien werden entsprechend den OSD-Dateien erstellt, die einem Paket zugeordnet sind. Diese Dateien umfassen die folgenden Informationen:</span><span class="sxs-lookup"><span data-stu-id="2e55b-115">New .xml files are created corresponding to the .osd files associated with a package; these files include the following information:</span></span></p>
<ul>
<li><p><span data-ttu-id="2e55b-116">Umgebungsvariablen</span><span class="sxs-lookup"><span data-stu-id="2e55b-116">environment variables</span></span></p></li>
<li><p><span data-ttu-id="2e55b-117">Kombinationen</span><span class="sxs-lookup"><span data-stu-id="2e55b-117">shortcuts</span></span></p></li>
<li><p><span data-ttu-id="2e55b-118">Dateitypzuordnungen</span><span class="sxs-lookup"><span data-stu-id="2e55b-118">file type associations</span></span></p></li>
<li><p><span data-ttu-id="2e55b-119">Registrierungsinformationen</span><span class="sxs-lookup"><span data-stu-id="2e55b-119">registry information</span></span></p></li>
<li><p><span data-ttu-id="2e55b-120">Skripts</span><span class="sxs-lookup"><span data-stu-id="2e55b-120">scripts</span></span></p></li>
</ul>
<p><span data-ttu-id="2e55b-121">Sie können jetzt mithilfe des Parameters auswählen, dass Informationen aus einer Teilmenge der OSD-Dateien im Quellverzeichnis zum Paket hinzugefügt werden sollen <code>-OSDsToIncludeInPackage</code> .</span><span class="sxs-lookup"><span data-stu-id="2e55b-121">You can now choose to add information from a subset of the .osd files in the source directory to the package using the <code>-OSDsToIncludeInPackage</code> parameter.</span></span></p></td>
<td align="left"><p><span data-ttu-id="2e55b-122">Registrierungsinformationen und Skripts, die in OSD-Dateien enthalten sind, die einem Paket zugeordnet sind, wurden in der Paket Konverter-Ausgabe nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="2e55b-122">Registry information and scripts included in .osd files associated with a package were not included in package converter output.</span></span></p>
<p><span data-ttu-id="2e55b-123">Der Paket Konverter füllt das neue Paket mit Informationen aus allen OSD-Dateien im Quellverzeichnis auf.</span><span class="sxs-lookup"><span data-stu-id="2e55b-123">The package converter would populate the new package with information from all of the .osd files in the source directory.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="2e55b-124">Beispiel für eine Konvertierungsanweisung</span><span class="sxs-lookup"><span data-stu-id="2e55b-124">Example conversion statement</span></span>

<span data-ttu-id="2e55b-125">Wenn Sie den neuen Prozess verstehen möchten, lesen Sie die folgende Beispiel `ConvertFrom-AppvLegacyPackage` Paket Konverter-Anweisung.</span><span class="sxs-lookup"><span data-stu-id="2e55b-125">To understand the new process, review the following example `ConvertFrom-AppvLegacyPackage` package converter statement.</span></span>

**<span data-ttu-id="2e55b-126">Wenn das Quellverzeichnis (\\\\OldPkgStore\\ContosoApp) Folgendes enthält:</span><span class="sxs-lookup"><span data-stu-id="2e55b-126">If the source directory (\\\\OldPkgStore\\ContosoApp) includes the following:</span></span>**

-   <span data-ttu-id="2e55b-127">ContosoApp. SFT</span><span class="sxs-lookup"><span data-stu-id="2e55b-127">ContosoApp.sft</span></span>

-   <span data-ttu-id="2e55b-128">ContosoApp.msi</span><span class="sxs-lookup"><span data-stu-id="2e55b-128">ContosoApp.msi</span></span>

-   <span data-ttu-id="2e55b-129">ContosoApp. SPRJ</span><span class="sxs-lookup"><span data-stu-id="2e55b-129">ContosoApp.sprj</span></span>

-   <span data-ttu-id="2e55b-130">ContosoApp\_manifest.xml</span><span class="sxs-lookup"><span data-stu-id="2e55b-130">ContosoApp\_manifest.xml</span></span>

-   <span data-ttu-id="2e55b-131">X. OSD</span><span class="sxs-lookup"><span data-stu-id="2e55b-131">X.osd</span></span>

-   <span data-ttu-id="2e55b-132">Y. OSD</span><span class="sxs-lookup"><span data-stu-id="2e55b-132">Y.osd</span></span>

-   <span data-ttu-id="2e55b-133">Z. OSD</span><span class="sxs-lookup"><span data-stu-id="2e55b-133">Z.osd</span></span>

**<span data-ttu-id="2e55b-134">Und führen Sie diesen Befehl aus:</span><span class="sxs-lookup"><span data-stu-id="2e55b-134">And you run this command:</span></span>**

``` syntax
ConvertFrom-AppvLegacyPackage –SourcePath \\OldPkgStore\ContosoApp\ 
-DestinationPath \\NewPkgStore\ContosoApp\
-OSDsToIncludeInPackage X.osd,Y.osd
```

**<span data-ttu-id="2e55b-135">Im Zielverzeichnis (\\\\NewPkgStore\\ContosoApp) wird Folgendes erstellt:</span><span class="sxs-lookup"><span data-stu-id="2e55b-135">The following is created in the destination directory (\\\\NewPkgStore\\ContosoApp):</span></span>**

-   <span data-ttu-id="2e55b-136">ContosoApp. AppV</span><span class="sxs-lookup"><span data-stu-id="2e55b-136">ContosoApp.appv</span></span>

-   <span data-ttu-id="2e55b-137">ContosoApp.msi</span><span class="sxs-lookup"><span data-stu-id="2e55b-137">ContosoApp.msi</span></span>

-   <span data-ttu-id="2e55b-138">ContosoApp\_DeploymentConfig.xml</span><span class="sxs-lookup"><span data-stu-id="2e55b-138">ContosoApp\_DeploymentConfig.xml</span></span>

-   <span data-ttu-id="2e55b-139">ContosoApp\_UserConfig.xml</span><span class="sxs-lookup"><span data-stu-id="2e55b-139">ContosoApp\_UserConfig.xml</span></span>

-   <span data-ttu-id="2e55b-140">X\_Config.xml</span><span class="sxs-lookup"><span data-stu-id="2e55b-140">X\_Config.xml</span></span>

-   <span data-ttu-id="2e55b-141">Y\_Config.xml</span><span class="sxs-lookup"><span data-stu-id="2e55b-141">Y\_Config.xml</span></span>

-   <span data-ttu-id="2e55b-142">Z\_Config.xml</span><span class="sxs-lookup"><span data-stu-id="2e55b-142">Z\_Config.xml</span></span>

**<span data-ttu-id="2e55b-143">Im obigen Beispiel:</span><span class="sxs-lookup"><span data-stu-id="2e55b-143">In the above example:</span></span>**

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="2e55b-144">Diese Quellverzeichnis Dateien...</span><span class="sxs-lookup"><span data-stu-id="2e55b-144">These Source directory files…</span></span></th>
<th align="left"><span data-ttu-id="2e55b-145">... werden in diese Zielverzeichnis Dateien konvertiert...</span><span class="sxs-lookup"><span data-stu-id="2e55b-145">…are converted to these Destination directory files…</span></span></th>
<th align="left"><span data-ttu-id="2e55b-146">... und enthält die folgenden Elemente</span><span class="sxs-lookup"><span data-stu-id="2e55b-146">…and will contain these items</span></span></th>
<th align="left"><span data-ttu-id="2e55b-147">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2e55b-147">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><ul>
<li><p><span data-ttu-id="2e55b-148">X. OSD</span><span class="sxs-lookup"><span data-stu-id="2e55b-148">X.osd</span></span></p></li>
<li><p><span data-ttu-id="2e55b-149">Y. OSD</span><span class="sxs-lookup"><span data-stu-id="2e55b-149">Y.osd</span></span></p></li>
<li><p><span data-ttu-id="2e55b-150">Z. OSD</span><span class="sxs-lookup"><span data-stu-id="2e55b-150">Z.osd</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="2e55b-151">X_Config.xml</span><span class="sxs-lookup"><span data-stu-id="2e55b-151">X_Config.xml</span></span></p></li>
<li><p><span data-ttu-id="2e55b-152">Y_Config.xml</span><span class="sxs-lookup"><span data-stu-id="2e55b-152">Y_Config.xml</span></span></p></li>
<li><p><span data-ttu-id="2e55b-153">Z_Config.xml</span><span class="sxs-lookup"><span data-stu-id="2e55b-153">Z_Config.xml</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="2e55b-154">Umgebungsvariablen</span><span class="sxs-lookup"><span data-stu-id="2e55b-154">Environment variables</span></span></p></li>
<li><p><span data-ttu-id="2e55b-155">Kombinationen</span><span class="sxs-lookup"><span data-stu-id="2e55b-155">Shortcuts</span></span></p></li>
<li><p><span data-ttu-id="2e55b-156">Dateitypzuordnungen</span><span class="sxs-lookup"><span data-stu-id="2e55b-156">File type associations</span></span></p></li>
<li><p><span data-ttu-id="2e55b-157">Registrierungsinformationen</span><span class="sxs-lookup"><span data-stu-id="2e55b-157">Registry information</span></span></p></li>
<li><p><span data-ttu-id="2e55b-158">Skripts</span><span class="sxs-lookup"><span data-stu-id="2e55b-158">Scripts</span></span></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="2e55b-159">Jede OSD-Datei wird in eine separate, entsprechende XML-Datei konvertiert, die die Elemente enthält, die hier im App-V 5,1-Bereitstellungs Konfigurationsformat aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="2e55b-159">Each .osd file is converted to a separate, corresponding .xml file that contains the items listed here in App-V 5.1 deployment configuration format.</span></span> <span data-ttu-id="2e55b-160">Diese Elemente können dann aus diesen XML-Dateien kopiert und wie gewünscht in die Bereitstellungskonfiguration oder die Benutzerkonfigurationsdateien eingefügt werden.</span><span class="sxs-lookup"><span data-stu-id="2e55b-160">These items can then be copied from these .xml files and placed in the deployment configuration or user configuration files as desired.</span></span></p>
<p><span data-ttu-id="2e55b-161">In diesem Beispiel gibt es drei XML-Dateien, die den drei OSD-Dateien im Quellverzeichnis entsprechen.</span><span class="sxs-lookup"><span data-stu-id="2e55b-161">In this example, there are three .xml files, corresponding with the three .osd files in the source directory.</span></span> <span data-ttu-id="2e55b-162">Jede XML-Datei enthält die Umgebungsvariablen, Verknüpfungen, Dateitypen Zuordnungen, Registrierungsinformationen und Skripts in der entsprechenden OSD-Datei.</span><span class="sxs-lookup"><span data-stu-id="2e55b-162">Each .xml file contains the environment variables, shortcuts, file type associations, registry information, and scripts in its corresponding .osd file.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><ul>
<li><p><span data-ttu-id="2e55b-163">X. OSD</span><span class="sxs-lookup"><span data-stu-id="2e55b-163">X.osd</span></span></p></li>
<li><p><span data-ttu-id="2e55b-164">Y. OSD</span><span class="sxs-lookup"><span data-stu-id="2e55b-164">Y.osd</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="2e55b-165">ContosoApp. AppV</span><span class="sxs-lookup"><span data-stu-id="2e55b-165">ContosoApp.appv</span></span></p></li>
<li><p><span data-ttu-id="2e55b-166">ContosoApp_DeploymentConfig.xml</span><span class="sxs-lookup"><span data-stu-id="2e55b-166">ContosoApp_DeploymentConfig.xml</span></span></p></li>
<li><p><span data-ttu-id="2e55b-167">ContosoApp_UserConfig.xml</span><span class="sxs-lookup"><span data-stu-id="2e55b-167">ContosoApp_UserConfig.xml</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="2e55b-168">Umgebungsvariablen</span><span class="sxs-lookup"><span data-stu-id="2e55b-168">Environment variables</span></span></p></li>
<li><p><span data-ttu-id="2e55b-169">Kombinationen</span><span class="sxs-lookup"><span data-stu-id="2e55b-169">Shortcuts</span></span></p></li>
<li><p><span data-ttu-id="2e55b-170">Dateitypzuordnungen</span><span class="sxs-lookup"><span data-stu-id="2e55b-170">File type associations</span></span></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="2e55b-171">Die Informationen aus den im Parameter angegebenen OSD-Dateien <code>-OSDsToIncludeInPackage</code> werden konvertiert und innerhalb des Pakets gespeichert.</span><span class="sxs-lookup"><span data-stu-id="2e55b-171">The information from the .osd files specified in the <code>-OSDsToIncludeInPackage</code> parameter are converted and placed inside the package.</span></span> <span data-ttu-id="2e55b-172">Der Konverter füllt dann die Konfigurationsdatei für die Bereitstellung und die Benutzerkonfigurationsdatei mit dem Inhalt des Pakets auf, ebenso wie App-V Sequencer beim Sequenzieren eines neuen Pakets.</span><span class="sxs-lookup"><span data-stu-id="2e55b-172">The converter then populates the deployment configuration file and the user configuration file with the contents of the package, just as App-V Sequencer does when sequencing a new package.</span></span></p>
<p><span data-ttu-id="2e55b-173">In diesem Beispiel wurden Umgebungsvariablen, Verknüpfungen und Dateitypzuordnungen, die in X. OSD und Y. OSD enthalten sind, konvertiert und in das App-V-Paket eingefügt, und einige dieser Informationen wurden auch in die Bereitstellungskonfiguration und die Konfigurationsdateien der Benutzer aufgenommen.</span><span class="sxs-lookup"><span data-stu-id="2e55b-173">In this example, environment variables, shortcuts, and file type associations included in X.osd and Y.osd were converted and placed in the App-V package, and some of this information was also included in the deployment configuration and user configuration files.</span></span> <span data-ttu-id="2e55b-174">X. OSD und Y. OSD wurden verwendet, weil Sie als Argumente für den Parameter hinzugefügt wurden <code>-OSDsToIncludeInPackage</code> .</span><span class="sxs-lookup"><span data-stu-id="2e55b-174">X.osd and Y.osd were used because they were included as arguments to the <code>-OSDsToIncludeInPackage</code> parameter.</span></span> <span data-ttu-id="2e55b-175">Im Paket sind keine Informationen von Z. OSD enthalten, da es nicht als eines dieser Argumente enthalten war.</span><span class="sxs-lookup"><span data-stu-id="2e55b-175">No information from Z.osd was included in the package, because it was not included as one of these arguments.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="2e55b-176">Konvertieren von Paketen, die mit einer früheren Version von App-V erstellt wurden</span><span class="sxs-lookup"><span data-stu-id="2e55b-176">Converting packages created using a prior version of App-V</span></span>


<span data-ttu-id="2e55b-177">Verwenden Sie das Paket Konverter-Dienstprogramm, um virtuelle Anwendungspakete zu aktualisieren, die mit den Versionen von App-v vor App-v 5,0 erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="2e55b-177">Use the package converter utility to upgrade virtual application packages created using versions of App-V prior to App-V 5.0.</span></span> <span data-ttu-id="2e55b-178">Der Paket Konverter verwendet PowerShell zum Konvertieren von Paketen und kann die Automatisierung des Prozesses unterstützen, wenn viele Pakete vorhanden sind, für die eine Konvertierung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="2e55b-178">The package converter uses PowerShell to convert packages and can help automate the process if you have many packages that require conversion.</span></span>

<span data-ttu-id="2e55b-179">**Wichtig**  Nachdem Sie ein vorhandenes Paket konvertiert haben, sollten Sie das Paket vor der Bereitstellung des Pakets testen, um sicherzustellen, dass der Konvertierungsvorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="2e55b-179">**Important** After you convert an existing package you should test the package prior to deploying the package to ensure the conversion process was successful.</span></span>

 

**<span data-ttu-id="2e55b-180">Was Sie wissen müssen, bevor Sie vorhandene Pakete konvertieren</span><span class="sxs-lookup"><span data-stu-id="2e55b-180">What to know before you convert existing packages</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="2e55b-181">Problem</span><span class="sxs-lookup"><span data-stu-id="2e55b-181">Issue</span></span></th>
<th align="left"><span data-ttu-id="2e55b-182">Problemumgehung</span><span class="sxs-lookup"><span data-stu-id="2e55b-182">Workaround</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2e55b-183">Virtuelle Pakete, die DSC verwenden, werden nach der Konvertierung nicht verknüpft.</span><span class="sxs-lookup"><span data-stu-id="2e55b-183">Virtual packages using DSC are not linked after conversion.</span></span></p></td>
<td align="left"><p><span data-ttu-id="2e55b-184">Verknüpfen Sie die Pakete mithilfe von Verbindungsgruppen.</span><span class="sxs-lookup"><span data-stu-id="2e55b-184">Link the packages using connection groups.</span></span> <span data-ttu-id="2e55b-185">Siehe <a href="managing-connection-groups51.md" data-raw-source="[Managing Connection Groups](managing-connection-groups51.md)"> Verwalten von Verbindungsgruppen </a> .</span><span class="sxs-lookup"><span data-stu-id="2e55b-185">See <a href="managing-connection-groups51.md" data-raw-source="[Managing Connection Groups](managing-connection-groups51.md)">Managing Connection Groups</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2e55b-186">Während der Konvertierung werden Umgebungsvariablen Konflikte erkannt.</span><span class="sxs-lookup"><span data-stu-id="2e55b-186">Environment variable conflicts are detected during conversion.</span></span></p></td>
<td align="left"><p><span data-ttu-id="2e55b-187">Beheben Sie alle Konflikte in der zugehörigen <strong> OSD- </strong> Datei.</span><span class="sxs-lookup"><span data-stu-id="2e55b-187">Resolve any conflicts in the associated <strong>.osd</strong> file.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2e55b-188">Während der Konvertierung werden hart codierte Pfade erkannt.</span><span class="sxs-lookup"><span data-stu-id="2e55b-188">Hard-coded paths are detected during conversion.</span></span></p></td>
<td align="left"><p><span data-ttu-id="2e55b-189">Hart codierte Pfade sind schwierig, richtig zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="2e55b-189">Hard-coded paths are difficult to convert correctly.</span></span> <span data-ttu-id="2e55b-190">Der Paket Konverter erkennt Pakete mit Dateien, die hart codierte Pfade enthalten, und gibt diese zurück.</span><span class="sxs-lookup"><span data-stu-id="2e55b-190">The package converter will detect and return packages with files that contain hard-coded paths.</span></span> <span data-ttu-id="2e55b-191">Zeigen Sie die Datei mit dem hartcodierten Pfad an, und ermitteln Sie, ob das Paket die Datei erfordert.</span><span class="sxs-lookup"><span data-stu-id="2e55b-191">View the file with the hard-coded path, and determine whether the package requires the file.</span></span> <span data-ttu-id="2e55b-192">Wenn dies der Fall ist, empfiehlt es sich, das Paket neu zu sequenzieren.</span><span class="sxs-lookup"><span data-stu-id="2e55b-192">If so, it is recommended to re-sequence the package.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="2e55b-193">Beim Konvertieren einer Paketprüfung auf fehlerhafte Dateien oder Verknüpfungen.</span><span class="sxs-lookup"><span data-stu-id="2e55b-193">When converting a package check for failing files or shortcuts.</span></span> <span data-ttu-id="2e55b-194">Suchen Sie das Element in App-V 4,6-Paket.</span><span class="sxs-lookup"><span data-stu-id="2e55b-194">Locate the item in App-V 4.6 package.</span></span> <span data-ttu-id="2e55b-195">Möglicherweise handelt es sich um einen hartcodierten Pfad.</span><span class="sxs-lookup"><span data-stu-id="2e55b-195">It could possibly be a hard-coded path.</span></span> <span data-ttu-id="2e55b-196">Konvertieren Sie den Pfad.</span><span class="sxs-lookup"><span data-stu-id="2e55b-196">Convert the path.</span></span>

<span data-ttu-id="2e55b-197">**Hinweis**  Es wird empfohlen, den App-V 5,1-Sequenzer zum Konvertieren kritischer Anwendungen oder Anwendungen zu verwenden, die Features nutzen müssen.</span><span class="sxs-lookup"><span data-stu-id="2e55b-197">**Note** It is recommended that you use the App-V 5.1 sequencer for converting critical applications or applications that need to take advantage of features.</span></span> <span data-ttu-id="2e55b-198">Lesen Sie, [wie Sie eine neue Anwendung mit App-V 5,1 Sequenzieren](how-to-sequence-a-new-application-with-app-v-51-beta-gb18030.md).</span><span class="sxs-lookup"><span data-stu-id="2e55b-198">See, [How to Sequence a New Application with App-V 5.1](how-to-sequence-a-new-application-with-app-v-51-beta-gb18030.md).</span></span>

<span data-ttu-id="2e55b-199">Wenn ein konvertiertes Paket nicht geöffnet wird, nachdem Sie es konvertiert haben, empfiehlt es sich auch, die Anwendung mithilfe des App-V 5,1-Sequencers neu zu sequenzieren.</span><span class="sxs-lookup"><span data-stu-id="2e55b-199">If a converted package does not open after you convert it, it is also recommended that you re-sequence the application using the App-V 5.1 sequencer.</span></span>

 

[<span data-ttu-id="2e55b-200">So konvertieren Sie ein Paket, das in einer früheren Version von App-V erstellt wurde</span><span class="sxs-lookup"><span data-stu-id="2e55b-200">How to Convert a Package Created in a Previous Version of App-V</span></span>](how-to-convert-a-package-created-in-a-previous-version-of-app-v51.md)

## <span data-ttu-id="2e55b-201">Migrieren von Clients</span><span class="sxs-lookup"><span data-stu-id="2e55b-201">Migrating Clients</span></span>


<span data-ttu-id="2e55b-202">In der folgenden Tabelle wird die empfohlene Methode zum Aktualisieren von Clients angezeigt.</span><span class="sxs-lookup"><span data-stu-id="2e55b-202">The following table displays the recommended method for upgrading clients.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="2e55b-203">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="2e55b-203">Task</span></span></th>
<th align="left"><span data-ttu-id="2e55b-204">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="2e55b-204">More Information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2e55b-205">Aktualisieren Ihrer Umgebung auf die neueste Version von App-v 4.6</span><span class="sxs-lookup"><span data-stu-id="2e55b-205">Upgrade your environment to the latest version of App-V4.6</span></span></p></td>
<td align="left"><p><a href="../appv-v4/application-virtualization-deployment-and-upgrade-considerations-copy.md" data-raw-source="[Application Virtualization Deployment and Upgrade Considerations](../appv-v4/application-virtualization-deployment-and-upgrade-considerations-copy.md)"><span data-ttu-id="2e55b-206">Überlegungen zur Implementierung und zum Upgrade von Application Virtualization </a></span><span class="sxs-lookup"><span data-stu-id="2e55b-206">Application Virtualization Deployment and Upgrade Considerations</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2e55b-207">Installieren Sie den App-V 5,1-Client mit aktivierter Koexistenz.</span><span class="sxs-lookup"><span data-stu-id="2e55b-207">Install the App-V 5.1 client with co-existence enabled.</span></span></p></td>
<td align="left"><p><a href="how-to-deploy-the-app-v-46-and-the-app-v--51-client-on-the-same-computer.md" data-raw-source="[How to Deploy the App-V 4.6 and the App-V 5.1 Client on the Same Computer](how-to-deploy-the-app-v-46-and-the-app-v--51-client-on-the-same-computer.md)"><span data-ttu-id="2e55b-208">Bereitstellen der APP-v 4,6 und des App-v 5,1-Clients auf </a> demselben Computer</span><span class="sxs-lookup"><span data-stu-id="2e55b-208">How to Deploy the App-V 4.6 and the App-V 5.1 Client on the Same Computer</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2e55b-209">Sequenzieren und Rollout von App-V 5,1-Paketen.</span><span class="sxs-lookup"><span data-stu-id="2e55b-209">Sequence and roll out App-V 5.1 packages.</span></span> <span data-ttu-id="2e55b-210">Bei Bedarf können Sie die Veröffentlichung von App-V 4,6-Paketen aufheben.</span><span class="sxs-lookup"><span data-stu-id="2e55b-210">As needed, unpublish App-V 4.6 packages.</span></span></p></td>
<td align="left"><p><a href="how-to-sequence-a-new-application-with-app-v-51-beta-gb18030.md" data-raw-source="[How to Sequence a New Application with App-V 5.1](how-to-sequence-a-new-application-with-app-v-51-beta-gb18030.md)"><span data-ttu-id="2e55b-211">So wird es gemacht: Sequenzierung einer neuen Anwendung mit APP- </a> V 5,1</span><span class="sxs-lookup"><span data-stu-id="2e55b-211">How to Sequence a New Application with App-V 5.1</a>.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="2e55b-212">**Wichtig**  Sie müssen die neueste Version von App-v 4.6 ausführen, um den Koexistenzmodus verwenden zu können.</span><span class="sxs-lookup"><span data-stu-id="2e55b-212">**Important** You must be running the latest version of App-V4.6 to use coexistence mode.</span></span> <span data-ttu-id="2e55b-213">Wenn Sie ein Paket sequenzieren, müssen Sie außerdem die Einstellung für die Verwaltungsautorität konfigurieren, die sich in der **Benutzerkonfiguration** befindet, die sich im Abschnitt **Benutzerkonfiguration** befindet.</span><span class="sxs-lookup"><span data-stu-id="2e55b-213">Additionally, when you sequence a package, you must configure the Managing Authority setting, which is in the **User Configuration** is located in the **User Configuration** section.</span></span>

 

## <span data-ttu-id="2e55b-214">Migrieren der vollständigen Infrastruktur des App-V 5,1-Servers</span><span class="sxs-lookup"><span data-stu-id="2e55b-214">Migrating the App-V 5.1 Server Full Infrastructure</span></span>


<span data-ttu-id="2e55b-215">Es gibt keine direkte Methode zum Upgrade auf eine vollständige App-V 5,1-Infrastruktur.</span><span class="sxs-lookup"><span data-stu-id="2e55b-215">There is no direct method to upgrade to a full App-V 5.1 infrastructure.</span></span> <span data-ttu-id="2e55b-216">Verwenden Sie die Informationen im folgenden Abschnitt, um Informationen zum Upgrade des App-V-Servers zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="2e55b-216">Use the information in the following section for information about upgrading the App-V server.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="2e55b-217">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="2e55b-217">Task</span></span></th>
<th align="left"><span data-ttu-id="2e55b-218">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="2e55b-218">More Information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2e55b-219">Aktualisieren Sie Ihre Umgebung auf die neueste Version von App-v 4.6.</span><span class="sxs-lookup"><span data-stu-id="2e55b-219">Upgrade your environment to the latest version of App-V4.6.</span></span></p></td>
<td align="left"><p><a href="../appv-v4/application-virtualization-deployment-and-upgrade-considerations-copy.md" data-raw-source="[Application Virtualization Deployment and Upgrade Considerations](../appv-v4/application-virtualization-deployment-and-upgrade-considerations-copy.md)"><span data-ttu-id="2e55b-220">Überlegungen zur Implementierung und zum Upgrade von Application Virtualization </a></span><span class="sxs-lookup"><span data-stu-id="2e55b-220">Application Virtualization Deployment and Upgrade Considerations</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2e55b-221">Bereitstellen der App-V 5,1-Version des Clients</span><span class="sxs-lookup"><span data-stu-id="2e55b-221">Deploy App-V 5.1 version of the client.</span></span></p></td>
<td align="left"><p><a href="how-to-deploy-the-app-v-client-51gb18030.md" data-raw-source="[How to Deploy the App-V Client](how-to-deploy-the-app-v-client-51gb18030.md)"><span data-ttu-id="2e55b-222">Bereitstellen des App-V </a> -Clients</span><span class="sxs-lookup"><span data-stu-id="2e55b-222">How to Deploy the App-V Client</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2e55b-223">Installieren Sie den App-V 5,1-Server.</span><span class="sxs-lookup"><span data-stu-id="2e55b-223">Install App-V 5.1 server.</span></span></p></td>
<td align="left"><p><a href="how-to-deploy-the-app-v-51-server.md" data-raw-source="[How to Deploy the App-V 5.1 Server](how-to-deploy-the-app-v-51-server.md)"><span data-ttu-id="2e55b-224">Bereitstellen des App-V 5,1 </a> -Servers</span><span class="sxs-lookup"><span data-stu-id="2e55b-224">How to Deploy the App-V 5.1 Server</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2e55b-225">Migrieren vorhandener Pakete</span><span class="sxs-lookup"><span data-stu-id="2e55b-225">Migrate existing packages.</span></span></p></td>
<td align="left"><p><span data-ttu-id="2e55b-226">Weitere Informationen finden Sie unter <strong> Konvertieren von Paketen, die mit einer früheren Version von App-V </strong> in diesem Artikel erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="2e55b-226">See the <strong>Converting packages created using a prior version of App-V</strong> section of this article.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="2e55b-227">Zusätzliche Migrationsaufgaben</span><span class="sxs-lookup"><span data-stu-id="2e55b-227">Additional Migration tasks</span></span>


<span data-ttu-id="2e55b-228">Sie können auch zusätzliche Migrationsaufgaben wie die Neukonfiguration von Endpunkten und das Öffnen eines Pakets ausführen, das mit einer früheren Version auf einem Computer mit dem App-V 5,1-Client erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="2e55b-228">You can also perform additional migration tasks such as reconfiguring end points as well as opening a package created using a prior version on a computer running the App-V 5.1 client.</span></span> <span data-ttu-id="2e55b-229">Die folgenden Links enthalten weitere Informationen zum Ausführen dieser Aufgaben.</span><span class="sxs-lookup"><span data-stu-id="2e55b-229">The following links provide more information about performing these tasks.</span></span>

[<span data-ttu-id="2e55b-230">So migrieren Sie Erweiterungspunkte von einem App-V 4.6-Paket zu einem konvertierten App-V 5.1-Paket für alle Benutzer eines bestimmten Computers</span><span class="sxs-lookup"><span data-stu-id="2e55b-230">How to Migrate Extension Points From an App-V 4.6 Package to a Converted App-V 5.1 Package for All Users on a Specific Computer</span></span>](how-to-migrate-extension-points-from-an-app-v-46-package-to-a-converted-app-v-51-package-for-all-users-on-a-specific-computer.md)

[<span data-ttu-id="2e55b-231">So migrieren Sie Erweiterungspunkte von einem App-V 4.6-Paket zu App-V 5.1 für einen bestimmten Benutzer</span><span class="sxs-lookup"><span data-stu-id="2e55b-231">How to Migrate Extension Points From an App-V 4.6 Package to App-V 5.1 for a Specific User</span></span>](how-to-migrate-extension-points-from-an-app-v-46-package-to-app-v-51-for-a-specific-user.md)

[<span data-ttu-id="2e55b-232">So setzen Sie Erweiterungspunkte von einem App-V 5.1-Paket auf ein App-V 4.6-Paket für alle Benutzer eines bestimmten Computers zurück</span><span class="sxs-lookup"><span data-stu-id="2e55b-232">How to Revert Extension Points from an App-V 5.1 Package to an App-V 4.6 Package For All Users on a Specific Computer</span></span>](how-to-revert-extension-points-from-an-app-v-51-package-to-an-app-v-46-package-for-all-users-on-a-specific-computer.md)

[<span data-ttu-id="2e55b-233">So setzen Sie Erweiterungspunkte von einem App-V 5.1-Paket auf ein App-V 4.6-Paket für einen bestimmten Benutzer zurück</span><span class="sxs-lookup"><span data-stu-id="2e55b-233">How to Revert Extension Points From an App-V 5.1 Package to an App-V 4.6 Package for a Specific User</span></span>](how-to-revert-extension-points-from-an-app-v-51-package-to-an-app-v-46-package-for-a-specific-user.md)







## <span data-ttu-id="2e55b-234">Weitere Ressourcen für die Ausführung von App-V-Migrationsaufgaben</span><span class="sxs-lookup"><span data-stu-id="2e55b-234">Other resources for performing App-V migration tasks</span></span>


[<span data-ttu-id="2e55b-235">Vorgänge für App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="2e55b-235">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)

[<span data-ttu-id="2e55b-236">Ein vereinfachtes Upgrade-Verfahren für Microsoft App-V 5,1-Verwaltungs Server</span><span class="sxs-lookup"><span data-stu-id="2e55b-236">A simplified Microsoft App-V 5.1 Management Server upgrade procedure</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=786330)

 

 





