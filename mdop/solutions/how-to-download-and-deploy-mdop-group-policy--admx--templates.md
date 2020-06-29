---
title: Herunterladen und Bereitstellen von MDOP-Gruppenrichtlinienvorlagen (ADMX-Dateien)
description: Herunterladen und Bereitstellen von MDOP-Gruppenrichtlinienvorlagen (ADMX-Dateien)
author: dansimp
ms.assetid: fdb64505-6c66-4fdf-ad74-a6a161191e3f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/15/2018
ms.openlocfilehash: 5bc5f8d536c113ccbc0a1931e6c7e4ed3c7a9a37
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812043"
---
# <span data-ttu-id="e9992-103">Herunterladen und Bereitstellen von MDOP-Gruppenrichtlinienvorlagen (ADMX-Dateien)</span><span class="sxs-lookup"><span data-stu-id="e9992-103">How to Download and Deploy MDOP Group Policy (.admx) Templates</span></span>


<span data-ttu-id="e9992-104">Sie können die Funktionseinstellungen bestimmter Microsoft Desktop Optimization Pack (MDOP)-Technologien (beispielsweise App-v, UE-v oder MBAM) mithilfe von Gruppenrichtlinienvorlagen, den ADMX-und ADML-Dateien verwalten.</span><span class="sxs-lookup"><span data-stu-id="e9992-104">You can manage the feature settings of certain Microsoft Desktop Optimization Pack (MDOP) technologies (for example, App-V, UE-V, or MBAM) by using Group Policy templates, the .admx and .adml files.</span></span> <span data-ttu-id="e9992-105">MDOP-Gruppenrichtlinienvorlagen stehen in einer selbstextrahierenden, komprimierten Datei, gruppiert nach Technologie und Version, zum Download zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="e9992-105">MDOP Group Policy templates are available for download in a self-extracting, compressed file, grouped by technology and version.</span></span>

## <span data-ttu-id="e9992-106">MDOP-Gruppenrichtlinienvorlagen</span><span class="sxs-lookup"><span data-stu-id="e9992-106">MDOP Group Policy templates</span></span>

**<span data-ttu-id="e9992-107">Herunterladen und Bereitstellen der MDOP-Gruppenrichtlinienvorlagen</span><span class="sxs-lookup"><span data-stu-id="e9992-107">How to download and deploy the MDOP Group Policy templates</span></span>**

1. <span data-ttu-id="e9992-108">Herunterladen der neuesten [Vorlagen für MDOP-Gruppenrichtlinien](https://www.microsoft.com/download/details.aspx?id=55531)</span><span class="sxs-lookup"><span data-stu-id="e9992-108">Download the latest [MDOP Group Policy templates](https://www.microsoft.com/download/details.aspx?id=55531)</span></span> 

2. <span data-ttu-id="e9992-109">Erweitern Sie die heruntergeladene CAB-Datei, indem Sie</span><span class="sxs-lookup"><span data-stu-id="e9992-109">Expand the downloaded .cab file by running</span></span> `expand <download_folder>\MDOP_ADMX_Templates.cab -F:* <destination_folder>`

   **<span data-ttu-id="e9992-110">Warnung</span><span class="sxs-lookup"><span data-stu-id="e9992-110">Warning</span></span>**  
   <span data-ttu-id="e9992-111">Extrahieren Sie die Vorlagen nicht direkt in das Bereitstellungsverzeichnis für Gruppenrichtlinien.</span><span class="sxs-lookup"><span data-stu-id="e9992-111">Do not extract the templates directly to the Group Policy deployment directory.</span></span> <span data-ttu-id="e9992-112">In dieser Datei sind mehrere Technologien und Versionen gebündelt.</span><span class="sxs-lookup"><span data-stu-id="e9992-112">Multiple technologies and versions are bundled in this file.</span></span>

3. <span data-ttu-id="e9992-113">Suchen Sie im extrahierten Ordner nach der Datei "Technology-Version. ADMX".</span><span class="sxs-lookup"><span data-stu-id="e9992-113">In the extracted folder, locate the technology-version .admx file.</span></span> <span data-ttu-id="e9992-114">Bestimmte MDOP-Technologien verfügen über mehrere Gruppenrichtlinienobjekte (Group Policy Objects, GPOs).</span><span class="sxs-lookup"><span data-stu-id="e9992-114">Certain MDOP technologies have multiple sets of Group Policy Objects (GPOs).</span></span> <span data-ttu-id="e9992-115">MBAM enthält beispielsweise MBAM-Verwaltungseinstellungen und MBAM-Benutzereinstellungen.</span><span class="sxs-lookup"><span data-stu-id="e9992-115">For example, MBAM includes MBAM Management settings and MBAM User settings.</span></span>

4. <span data-ttu-id="e9992-116">Suchen Sie die entsprechende ADML-Datei nach Sprache-Kultur (d *-US* für Englisch-Vereinigte Staaten).</span><span class="sxs-lookup"><span data-stu-id="e9992-116">Locate the appropriate .adml file by language-culture (that is, *en-us* for English-United States).</span></span>

5. <span data-ttu-id="e9992-117">Kopieren Sie die ADMX-und ADML-Dateien in einen Richtlinien Definitions Ordner.</span><span class="sxs-lookup"><span data-stu-id="e9992-117">Copy the .admx and .adml files to a policy definition folder.</span></span> <span data-ttu-id="e9992-118">Je nachdem, wo Sie die Vorlagen speichern, können Sie die Gruppenrichtlinieneinstellungen auf dem lokalen Gerät oder auf einem beliebigen Computer in der Domäne konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="e9992-118">Depending on where you store the templates, you can configure Group Policy settings from the local device or from any computer on the domain.</span></span>

   - <span data-ttu-id="e9992-119">**Lokale Dateien:** Wenn Sie die Gruppenrichtlinieneinstellungen auf dem lokalen Gerät konfigurieren möchten, kopieren Sie die Vorlagendateien an die folgenden Speicherorte:</span><span class="sxs-lookup"><span data-stu-id="e9992-119">**Local files:** To configure Group Policy settings from the local device, copy template files to the following locations:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="e9992-120">Dateityp</span><span class="sxs-lookup"><span data-stu-id="e9992-120">File type</span></span></th>
   <th align="left"><span data-ttu-id="e9992-121">Dateispeicherort</span><span class="sxs-lookup"><span data-stu-id="e9992-121">File location</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="e9992-122">Gruppenrichtlinienvorlage (ADMX)</span><span class="sxs-lookup"><span data-stu-id="e9992-122">Group Policy template (.admx)</span></span></p></td>
   <td align="left"><p><code>%systemroot%</code><span data-ttu-id="e9992-123">&lt;starke &gt; PolicyDefinitions</span><span class="sxs-lookup"><span data-stu-id="e9992-123">&lt;strong&gt;policyDefinitions</span></span></strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="e9992-124">Gruppenrichtlinien-Sprachdatei (ADML)</span><span class="sxs-lookup"><span data-stu-id="e9992-124">Group Policy language file (.adml)</span></span></p></td>
   <td align="left"><p><code>%systemroot%</code><span data-ttu-id="e9992-125">&lt;starke &gt; PolicyDefinitions</span><span class="sxs-lookup"><span data-stu-id="e9992-125">&lt;strong&gt;policyDefinitions</span></span></strong><code>[MUIculture]</code></p></td>
   </tr>
   </tbody>
   </table>

   - <span data-ttu-id="e9992-126">**Zentraler Domänenspeicher:** Wenn Sie die Konfiguration der Gruppenrichtlinieneinstellungen durch einen Gruppenrichtlinienadministrator von einem beliebigen Computer in der Domäne aus aktivieren möchten, kopieren Sie Dateien an die folgenden Speicherorte auf dem Domänencontroller:</span><span class="sxs-lookup"><span data-stu-id="e9992-126">**Domain central store:** To enable Group Policy settings configuration by a Group Policy administrator from any computer on the domain, copy files to the following locations on the domain controller:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="e9992-127">Dateityp</span><span class="sxs-lookup"><span data-stu-id="e9992-127">File type</span></span></th>
   <th align="left"><span data-ttu-id="e9992-128">Dateispeicherort</span><span class="sxs-lookup"><span data-stu-id="e9992-128">File location</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="e9992-129">Gruppenrichtlinienvorlage (ADMX)</span><span class="sxs-lookup"><span data-stu-id="e9992-129">Group Policy template (.admx)</span></span></p></td>
   <td align="left"><p><code>%systemroot%</code><span data-ttu-id="e9992-130">&lt;starke &gt; sysvol\domain\policies\PolicyDefinitions</span><span class="sxs-lookup"><span data-stu-id="e9992-130">&lt;strong&gt;sysvol\domain\policies\PolicyDefinitions</span></span></strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="e9992-131">Gruppenrichtlinien-Sprachdatei (ADML)</span><span class="sxs-lookup"><span data-stu-id="e9992-131">Group Policy language file (.adml)</span></span></p></td>
   <td align="left"><p><code>%systemroot%</code><span data-ttu-id="e9992-132">&lt;starke &gt; sysvol\domain\policies\PolicyDefinitions [MUIculture]</span><span class="sxs-lookup"><span data-stu-id="e9992-132">&lt;strong&gt;sysvol\domain\policies\PolicyDefinitions[MUIculture]</span></span></strong><code>[MUIculture]</code></p>
   <p><span data-ttu-id="e9992-133">Beispielsweise wird die sprachspezifische ADML-Datei in US-Englisch in%SystemRoot%\sysvol\domain\policies\PolicyDefinitions\en-US. gespeichert.</span><span class="sxs-lookup"><span data-stu-id="e9992-133">For example, the U.S. English ADML language-specific file will be stored in %systemroot%\sysvol\domain\policies\PolicyDefinitions\en-us.</span></span></p></td>
   </tr>
   </tbody>
   </table>

6. <span data-ttu-id="e9992-134">Bearbeiten Sie die Gruppenrichtlinieneinstellungen mithilfe von Gruppenrichtlinien-Verwaltungskonsole (Group Policy Management Console, GPMC) oder erweiterte Gruppenrichtlinienverwaltung (Group Policy Management, AGPM), um Gruppenrichtlinieneinstellungen für die MDOP-Technologie zu konfigurieren</span><span class="sxs-lookup"><span data-stu-id="e9992-134">Edit the Group Policy settings using Group Policy Management Console (GPMC) or Advanced Group Policy Management (AGPM) to configure Group Policy settings for the MDOP technology.</span></span>

### <span data-ttu-id="e9992-135">MDOP-Gruppenrichtlinien nach Technologie</span><span class="sxs-lookup"><span data-stu-id="e9992-135">MDOP Group Policy by technology</span></span>

<span data-ttu-id="e9992-136">Weitere Informationen zu unterstützten MDOP-Gruppenrichtlinien finden Sie in der jeweiligen Dokumentation zur Technologie.</span><span class="sxs-lookup"><span data-stu-id="e9992-136">For more information about supported MDOP Group Policy, see the specific documentation for the technology.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="e9992-137">MDOP-Technologie</span><span class="sxs-lookup"><span data-stu-id="e9992-137">MDOP Technology</span></span></th>
<th align="left"><span data-ttu-id="e9992-138">Versions Pakete</span><span class="sxs-lookup"><span data-stu-id="e9992-138">Version bundles</span></span></th>
<th align="left"><span data-ttu-id="e9992-139">Anmerkungen</span><span class="sxs-lookup"><span data-stu-id="e9992-139">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="e9992-140">Application Virtualization (App-V)</span><span class="sxs-lookup"><span data-stu-id="e9992-140">Application Virtualization (App-V)</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="e9992-141">App-v 5,0 und App-v 5,0-Service Packs</span><span class="sxs-lookup"><span data-stu-id="e9992-141">App-V 5.0 and App-V 5.0 Service Packs</span></span></p></td>
<td align="left"><p><a href="../appv-v5/how-to-modify-app-v-50-client-configuration-using-the-admx-template-and-group-policy.md" data-raw-source="[How to Modify App-V 5.0 Client Configuration Using the ADMX Template and Group Policy](../appv-v5/how-to-modify-app-v-50-client-configuration-using-the-admx-template-and-group-policy.md)"><span data-ttu-id="e9992-142">So ändern Sie die App-V 5.0-Clientkonfiguration mithilfe der ADMX-Vorlage und -Gruppenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="e9992-142">How to Modify App-V 5.0 Client Configuration Using the ADMX Template and Group Policy</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="e9992-143">User Experience Virtualization (UE-V)</span><span class="sxs-lookup"><span data-stu-id="e9992-143">User Experience Virtualization (UE-V)</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="e9992-144">UE-v 2,0 und UE-v 2,1</span><span class="sxs-lookup"><span data-stu-id="e9992-144">UE-V 2.0 and UE-V 2.1</span></span></p></td>
<td align="left"><p><a href="../uev-v2/configuring-ue-v-2x-with-group-policy-objects-both-uevv2.md" data-raw-source="[Configuring UE-V 2.x with Group Policy Objects](../uev-v2/configuring-ue-v-2x-with-group-policy-objects-both-uevv2.md)"><span data-ttu-id="e9992-145">Konfigurieren von UE-V 2. x mit Gruppenrichtlinienobjekten</span><span class="sxs-lookup"><span data-stu-id="e9992-145">Configuring UE-V 2.x with Group Policy Objects</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="e9992-146">UE-V 1,0 einschließlich 1,0 SP1</span><span class="sxs-lookup"><span data-stu-id="e9992-146">UE-V 1.0 including 1.0 SP1</span></span></p></td>
<td align="left"><p><a href="../uev-v1/configuring-ue-v-with-group-policy-objects.md" data-raw-source="[Configuring UE-V with Group Policy Objects](../uev-v1/configuring-ue-v-with-group-policy-objects.md)"><span data-ttu-id="e9992-147">Konfigurieren von UE-V mit Gruppenrichtlinienobjekten</span><span class="sxs-lookup"><span data-stu-id="e9992-147">Configuring UE-V with Group Policy Objects</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="e9992-148">Microsoft BitLocker Administration and Monitoring (MBAM)</span><span class="sxs-lookup"><span data-stu-id="e9992-148">Microsoft BitLocker Administration and Monitoring (MBAM)</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="e9992-149">MBAM 2,5</span><span class="sxs-lookup"><span data-stu-id="e9992-149">MBAM 2.5</span></span></p></td>
<td align="left"><p><a href="../mbam-v25/planning-for-mbam-25-group-policy-requirements.md" data-raw-source="[Planning for MBAM 2.5 Group Policy Requirements](../mbam-v25/planning-for-mbam-25-group-policy-requirements.md)"><span data-ttu-id="e9992-150">Planen der Gruppenrichtlinienanforderungen für MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="e9992-150">Planning for MBAM 2.5 Group Policy Requirements</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="e9992-151">MBAM 2,0 einschließlich 2,0 SP1</span><span class="sxs-lookup"><span data-stu-id="e9992-151">MBAM 2.0 including 2.0 SP1</span></span></p></td>
<td align="left"><p><a href="../mbam-v2/planning-for-mbam-20-group-policy-requirements-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Group Policy Requirements](../mbam-v2/planning-for-mbam-20-group-policy-requirements-mbam-2.md)"><span data-ttu-id="e9992-152">Planen der Gruppenrichtlinienanforderungen für MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="e9992-152">Planning for MBAM 2.0 Group Policy Requirements</span></span></a></p>
<p><a href="../mbam-v2/deploying-mbam-20-group-policy-objects-mbam-2.md" data-raw-source="[Deploying MBAM 2.0 Group Policy Objects](../mbam-v2/deploying-mbam-20-group-policy-objects-mbam-2.md)"><span data-ttu-id="e9992-153">Bereitstellen von Gruppenrichtlinienobjekten für MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="e9992-153">Deploying MBAM 2.0 Group Policy Objects</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="e9992-154">MBAM 1,0</span><span class="sxs-lookup"><span data-stu-id="e9992-154">MBAM 1.0</span></span></p></td>
<td align="left"><p><a href="../mbam-v1/how-to-edit-mbam-10-gpo-settings.md" data-raw-source="[How to Edit MBAM 1.0 GPO Settings](../mbam-v1/how-to-edit-mbam-10-gpo-settings.md)"><span data-ttu-id="e9992-155">So bearbeiten Sie die GPO-Einstellungen für MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="e9992-155">How to Edit MBAM 1.0 GPO Settings</span></span></a></p></td>
</tr>
</tbody>
</table>

 

 

 





