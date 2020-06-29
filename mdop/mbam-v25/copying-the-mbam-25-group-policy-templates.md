---
title: Kopieren die Gruppenrichtlinienvorlagen für MBAM 2.5
description: Kopieren die Gruppenrichtlinienvorlagen für MBAM 2.5
author: dansimp
ms.assetid: e526ecec-07ff-435e-bc90-3084b617b84b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/28/2017
ms.openlocfilehash: a3436552256b1632a11037dc94751207cde89d5c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811026"
---
# <span data-ttu-id="15603-103">Kopieren die Gruppenrichtlinienvorlagen für MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="15603-103">Copying the MBAM 2.5 Group Policy Templates</span></span>


<span data-ttu-id="15603-104">Bevor Sie die MBAM-Client Installation bereitstellen, müssen Sie die MBAM-Gruppenrichtlinienvorlagen, die Gruppenrichtlinieneinstellungen enthalten, die MBAM-Implementierungs Einstellungen für die BitLocker-Laufwerkverschlüsselung definieren, herunterladen.</span><span class="sxs-lookup"><span data-stu-id="15603-104">Before deploying the MBAM Client installation, you must download the MBAM Group Policy Templates, which contain Group Policy settings that define MBAM implementation settings for BitLocker Drive Encryption.</span></span> <span data-ttu-id="15603-105">Nachdem Sie die Vorlagen heruntergeladen haben, können Sie die Gruppenrichtlinieneinstellungen so festlegen, dass Sie im gesamten Unternehmen implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="15603-105">After downloading the templates, you then set the Group Policy settings to implement across your enterprise.</span></span>

## <span data-ttu-id="15603-106">Herunterladen und Bereitstellen der MDOP-Gruppenrichtlinienvorlagen</span><span class="sxs-lookup"><span data-stu-id="15603-106">Downloading and deploying the MDOP Group Policy templates</span></span>


<span data-ttu-id="15603-107">MDOP-Gruppenrichtlinienvorlagen stehen in einer selbstextrahierenden, komprimierten Datei, gruppiert nach Technologie und Version, zum Download zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="15603-107">MDOP Group Policy templates are available for download in a self-extracting, compressed file, grouped by technology and version.</span></span>

**<span data-ttu-id="15603-108">Herunterladen und Bereitstellen der MDOP-Gruppenrichtlinienvorlagen</span><span class="sxs-lookup"><span data-stu-id="15603-108">How to download and deploy the MDOP Group Policy templates</span></span>**

1. <span data-ttu-id="15603-109">Laden Sie die MDOP-Gruppenrichtlinienvorlagen aus den [Microsoft Desktop Optimization Pack-Gruppenrichtlinien-Verwaltungsvorlagen](https://www.microsoft.com/download/details.aspx?id=55531)herunter.</span><span class="sxs-lookup"><span data-stu-id="15603-109">Download the MDOP Group Policy templates from [Microsoft Desktop Optimization Pack Group Policy Administrative Templates](https://www.microsoft.com/download/details.aspx?id=55531).</span></span>

2. <span data-ttu-id="15603-110">Führen Sie die heruntergeladene Datei aus, um die Vorlagenordner zu extrahieren.</span><span class="sxs-lookup"><span data-stu-id="15603-110">Run the downloaded file to extract the template folders.</span></span>

   **<span data-ttu-id="15603-111">Warnung</span><span class="sxs-lookup"><span data-stu-id="15603-111">Warning</span></span>**  
   <span data-ttu-id="15603-112">Extrahieren Sie die Vorlagen nicht direkt in das Bereitstellungsverzeichnis für Gruppenrichtlinien.</span><span class="sxs-lookup"><span data-stu-id="15603-112">Do not extract the templates directly to the Group Policy deployment directory.</span></span> <span data-ttu-id="15603-113">In dieser Datei sind mehrere Technologien und Versionen gebündelt.</span><span class="sxs-lookup"><span data-stu-id="15603-113">Multiple technologies and versions are bundled in this file.</span></span>



3. <span data-ttu-id="15603-114">Suchen Sie im extrahierten Ordner nach der Datei "Technology-Version. ADMX".</span><span class="sxs-lookup"><span data-stu-id="15603-114">In the extracted folder, locate the technology-version .admx file.</span></span> <span data-ttu-id="15603-115">Bestimmte MDOP-Technologien verfügen über mehrere Gruppenrichtlinienobjekte (Group Policy Objects, GPOs).</span><span class="sxs-lookup"><span data-stu-id="15603-115">Certain MDOP technologies have multiple sets of Group Policy Objects (GPOs).</span></span> <span data-ttu-id="15603-116">MBAM enthält beispielsweise MBAM-Verwaltungseinstellungen und MBAM-Benutzereinstellungen.</span><span class="sxs-lookup"><span data-stu-id="15603-116">For example, MBAM includes MBAM Management settings and MBAM User settings.</span></span>

4. <span data-ttu-id="15603-117">Suchen Sie die entsprechende ADML-Datei nach sprach Kultur (d. *en* für Englisch – USA).</span><span class="sxs-lookup"><span data-stu-id="15603-117">Locate the appropriate .adml file by language-culture (that is, *en* for English-United States).</span></span>

5. <span data-ttu-id="15603-118">Kopieren Sie die ADMX-und ADML-Dateien in einen Richtlinien Definitions Ordner.</span><span class="sxs-lookup"><span data-stu-id="15603-118">Copy the .admx and .adml files to a policy definition folder.</span></span> <span data-ttu-id="15603-119">Je nachdem, wo Sie die Vorlagen speichern, können Sie die Gruppenrichtlinieneinstellungen auf dem lokalen Gerät oder auf einem beliebigen Computer in der Domäne konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="15603-119">Depending on where you store the templates, you can configure Group Policy settings from the local device or from any computer on the domain.</span></span>

   **<span data-ttu-id="15603-120">Lokale Dateien.</span><span class="sxs-lookup"><span data-stu-id="15603-120">Local files.</span></span>** <span data-ttu-id="15603-121">Wenn Sie die Gruppenrichtlinieneinstellungen auf dem lokalen Gerät konfigurieren möchten, kopieren Sie die Vorlagendateien an die folgenden Speicherorte:</span><span class="sxs-lookup"><span data-stu-id="15603-121">To configure Group Policy settings from the local device, copy template files to the following locations:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="15603-122">Dateityp</span><span class="sxs-lookup"><span data-stu-id="15603-122">File type</span></span></th>
   <th align="left"><span data-ttu-id="15603-123">Dateispeicherort</span><span class="sxs-lookup"><span data-stu-id="15603-123">File location</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="15603-124">Gruppenrichtlinienvorlage (ADMX)</span><span class="sxs-lookup"><span data-stu-id="15603-124">Group Policy template (.admx)</span></span></p></td>
   <td align="left"><p><code>%systemroot%</code><span data-ttu-id="15603-125">&lt;starke &gt; PolicyDefinitions</span><span class="sxs-lookup"><span data-stu-id="15603-125">&lt;strong&gt;policyDefinitions</span></span></strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="15603-126">Gruppenrichtlinien-Sprachdatei (ADML)</span><span class="sxs-lookup"><span data-stu-id="15603-126">Group Policy language file (.adml)</span></span></p></td>
   <td align="left"><p><code>%systemroot%</code><span data-ttu-id="15603-127">&lt;starke &gt; PolicyDefinitions</span><span class="sxs-lookup"><span data-stu-id="15603-127">&lt;strong&gt;policyDefinitions</span></span></strong><code>[MUIculture]</code></p></td>
   </tr>
   </tbody>
   </table>



~~~
**Domain central store.** To enable Group Policy settings configuration by a Group Policy administrator from any computer on the domain, copy files to the following locations on the domain controller:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">File type</th>
<th align="left">File location</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Group Policy template (.admx)</p></td>
<td align="left"><p><code>%systemroot%</code>\<strong>sysvol\domain\policies\PolicyDefinitions</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p>Group Policy language file (.adml)</p></td>
<td align="left"><p><code>%systemroot%</code>\<strong>sysvol\domain\policies\PolicyDefinitions\[MUIculture]</strong><code>\[MUIculture]</code></p>
<p>For example, the U.S. English ADML language-specific file will be stored in %systemroot%\sysvol\domain\policies\PolicyDefinitions\en-us.</p></td>
</tr>
</tbody>
</table>
~~~



6. <span data-ttu-id="15603-128">Bearbeiten Sie die Gruppenrichtlinieneinstellungen mithilfe von Gruppenrichtlinien-Verwaltungskonsole (Group Policy Management Console, GPMC) oder erweiterte Gruppenrichtlinienverwaltung (Group Policy Management, AGPM), um Gruppenrichtlinieneinstellungen für die MDOP-Technologie zu konfigurieren</span><span class="sxs-lookup"><span data-stu-id="15603-128">Edit the Group Policy settings using Group Policy Management Console (GPMC) or Advanced Group Policy Management (AGPM) to configure Group Policy settings for the MDOP technology.</span></span> <span data-ttu-id="15603-129">Weitere Informationen finden Sie unter [Bearbeiten der MBAM 2,5-Gruppenrichtlinieneinstellungen](editing-the-mbam-25-group-policy-settings.md) .</span><span class="sxs-lookup"><span data-stu-id="15603-129">See [Editing the MBAM 2.5 Group Policy Settings](editing-the-mbam-25-group-policy-settings.md) for more information.</span></span>

   <span data-ttu-id="15603-130">Beschreibungen der Gruppenrichtlinieneinstellungen finden Sie unter [Planen von MBAM 2,5-Gruppenrichtlinienanforderungen](planning-for-mbam-25-group-policy-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="15603-130">For descriptions of the Group Policy settings, see [Planning for MBAM 2.5 Group Policy Requirements](planning-for-mbam-25-group-policy-requirements.md).</span></span>


## <span data-ttu-id="15603-131">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="15603-131">Related topics</span></span>


[<span data-ttu-id="15603-132">Bereitstellen von Gruppenrichtlinienobjekten für MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="15603-132">Deploying MBAM 2.5 Group Policy Objects</span></span>](deploying-mbam-25-group-policy-objects.md)


## <span data-ttu-id="15603-133">Sie haben einen Vorschlag für MBAM?</span><span class="sxs-lookup"><span data-stu-id="15603-133">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="15603-134">[Hier](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)können Sie Vorschläge hinzufügen oder abstimmen.</span><span class="sxs-lookup"><span data-stu-id="15603-134">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="15603-135">Bei MBAM-Problemen verwenden Sie das [MBAM TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="15603-135">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>






