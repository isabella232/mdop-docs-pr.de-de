---
title: Synchronisieren von Office 2013 mit UE-V 2,0
description: Synchronisieren von Office 2013 mit UE-V 2,0
author: dansimp
ms.assetid: c46feb6d-28a8-4799-888d-053531dc5842
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: c9b079d3f21e6ced689fa2101f5321fa9b1406c8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812025"
---
# <span data-ttu-id="9becb-103">Synchronisieren von Office 2013 mit UE-V 2,0</span><span class="sxs-lookup"><span data-stu-id="9becb-103">Synchronizing Office 2013 with UE-V 2.0</span></span>


<span data-ttu-id="9becb-104">Microsoft User Experience Virtualization (UE-v) 2,0 unterstützt die Synchronisierung der Microsoft Office 2013-Anwendungseinstellung mithilfe einer Vorlage aus dem UE-v-Vorlagenkatalog.</span><span class="sxs-lookup"><span data-stu-id="9becb-104">Microsoft User Experience Virtualization (UE-V) 2.0 supports the synchronization of Microsoft Office 2013 application setting using a template available from the UE-V template gallery.</span></span> <span data-ttu-id="9becb-105">Die Kombination aus UE-v 2 und App-v 5,0 SP2 Unterstützung von Office 2013 Professional Plus ermöglicht die gleiche Erfahrung auf virtualisierten Instanzen von Office 2013 von jedem UE-v-fähigen Gerät oder virtualisierten Desktop.</span><span class="sxs-lookup"><span data-stu-id="9becb-105">The combination of UE-V 2 and App-V 5.0 SP2 support of Office 2013 Professional Plus enables the same experience on virtualized instance of Office 2013 from any UE-V-enabled device or virtualized desktop.</span></span>

<span data-ttu-id="9becb-106">Um die Unterstützung von UE-v-Anwendungseinstellungen von Office 2013 zu aktivieren, können Sie die offiziellen UE-v Office 2013-Vorlagen aus dem [Vorlagenkatalog Microsoft User Experience Virtualization (UE-v) 2](https://go.microsoft.com/fwlink/p/?LinkId=246589)herunterladen.</span><span class="sxs-lookup"><span data-stu-id="9becb-106">To activate UE-V application settings support of Office 2013, you can download official UE-V Office 2013 templates from the [Microsoft User Experience Virtualization (UE-V) 2 Template Gallery](https://go.microsoft.com/fwlink/p/?LinkId=246589).</span></span> <span data-ttu-id="9becb-107">Diese Ressource bietet von Microsoft verfasste UE-V-Einstellungen für Standort Vorlagen sowie von der Community entwickelte Einstellungen für Standort Vorlagen.</span><span class="sxs-lookup"><span data-stu-id="9becb-107">This resource provides Microsoft-authored UE-V settings location templates as well as community-developed settings location templates.</span></span>

## <span data-ttu-id="9becb-108">Microsoft Office-Support in UE-V</span><span class="sxs-lookup"><span data-stu-id="9becb-108">Microsoft Office support in UE-V</span></span>


<span data-ttu-id="9becb-109">UE-v 1,0 und UE-v 2 umfassen Einstellungen-Speicherort Vorlagen für Microsoft Office 2010.</span><span class="sxs-lookup"><span data-stu-id="9becb-109">UE-V 1.0 and UE-V 2 include settings location templates for Microsoft Office 2010.</span></span> <span data-ttu-id="9becb-110">Diese Vorlagen werden als Teil des UE-V-Agenten Installationsprozesses verteilt und registriert.</span><span class="sxs-lookup"><span data-stu-id="9becb-110">These templates are distributed and registered as part of the UE-V Agent installation process.</span></span> <span data-ttu-id="9becb-111">Mithilfe dieser Vorlagen können Sie die Office-Benutzererfahrung zwischen Geräten synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="9becb-111">These templates help synchronize users’ Office experience between devices.</span></span> <span data-ttu-id="9becb-112">Die UE-V-Vorlagen für Office 2013 bieten eine sehr ähnliche Einstellungs Oberfläche für die Vorlagen für Office 2010.</span><span class="sxs-lookup"><span data-stu-id="9becb-112">The UE-V templates for Office 2013 provide a very similar settings experience to the templates for Office 2010.</span></span> <span data-ttu-id="9becb-113">Microsoft Office 2013-Einstellungen, die durch die Office 365-Umgebung durchlaufen wurden, sind in diesen Einstellungen nicht enthalten.</span><span class="sxs-lookup"><span data-stu-id="9becb-113">Microsoft Office 2013 settings roamed by Office 365 experience are not included in these settings.</span></span> <span data-ttu-id="9becb-114">Eine Liste der Office 365-spezifischen Einstellungen finden Sie unter [Übersicht über die Einstellungen für Benutzer und Roaming für Office 2013](https://go.microsoft.com/fwlink/p/?LinkId=391220).</span><span class="sxs-lookup"><span data-stu-id="9becb-114">For a list of Office 365-specific settings, see [Overview of user and roaming settings for Office 2013](https://go.microsoft.com/fwlink/p/?LinkId=391220).</span></span>

## <span data-ttu-id="9becb-115">Synchronisierte Office 2013-Einstellungen</span><span class="sxs-lookup"><span data-stu-id="9becb-115">Synchronized Office 2013 Settings</span></span>


<span data-ttu-id="9becb-116">Die folgenden Tabellen enthalten die Details für die Office 2013-Unterstützung in UE-V:</span><span class="sxs-lookup"><span data-stu-id="9becb-116">The following tables contain the details for Office 2013 support in UE-V:</span></span>

### <span data-ttu-id="9becb-117">Unterstützte UE-V-Vorlagen für Microsoft Office</span><span class="sxs-lookup"><span data-stu-id="9becb-117">Supported UE-V templates for Microsoft Office</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="9becb-118">Office 2013-Vorlagen (UE-v 2,0, verfügbar auf dem UE-v-Katalog):</span><span class="sxs-lookup"><span data-stu-id="9becb-118">Office 2013 templates (UE-V 2.0, available on UE-V gallery):</span></span></th>
<th align="left"><span data-ttu-id="9becb-119">Office 2010-Vorlagen (UE-V 1,0 &amp; 1,0 SP1):</span><span class="sxs-lookup"><span data-stu-id="9becb-119">Office 2010 templates (UE-V 1.0 &amp; 1.0 SP1):</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9becb-120">MicrosoftOffice2013Win32.xml</span><span class="sxs-lookup"><span data-stu-id="9becb-120">MicrosoftOffice2013Win32.xml</span></span></p>
<p><span data-ttu-id="9becb-121">MicrosoftOffice2013Win64.xml</span><span class="sxs-lookup"><span data-stu-id="9becb-121">MicrosoftOffice2013Win64.xml</span></span></p>
<p><span data-ttu-id="9becb-122">MicrosoftLync2013Win32.xml</span><span class="sxs-lookup"><span data-stu-id="9becb-122">MicrosoftLync2013Win32.xml</span></span></p>
<p><span data-ttu-id="9becb-123">MicrosoftLync2013Win64.xml</span><span class="sxs-lookup"><span data-stu-id="9becb-123">MicrosoftLync2013Win64.xml</span></span></p></td>
<td align="left"><p><span data-ttu-id="9becb-124">MicrosoftOffice2010Win32.xml</span><span class="sxs-lookup"><span data-stu-id="9becb-124">MicrosoftOffice2010Win32.xml</span></span></p>
<p><span data-ttu-id="9becb-125">MicrosoftOffice2010Win64.xml</span><span class="sxs-lookup"><span data-stu-id="9becb-125">MicrosoftOffice2010Win64.xml</span></span></p>
<p><span data-ttu-id="9becb-126">MicrosoftLync2010.xml</span><span class="sxs-lookup"><span data-stu-id="9becb-126">MicrosoftLync2010.xml</span></span></p>
<p></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="9becb-127">Von den UE-V-Vorlagen unterstützte Microsoft Office-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="9becb-127">Microsoft Office Applications supported by the UE-V templates</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9becb-128">Microsoft Access 2013</span><span class="sxs-lookup"><span data-stu-id="9becb-128">Microsoft Access 2013</span></span></p>
<p><span data-ttu-id="9becb-129">Microsoft lync 2013</span><span class="sxs-lookup"><span data-stu-id="9becb-129">Microsoft Lync 2013</span></span></p>
<p><span data-ttu-id="9becb-130">Microsoft Excel 2013</span><span class="sxs-lookup"><span data-stu-id="9becb-130">Microsoft Excel 2013</span></span></p>
<p><span data-ttu-id="9becb-131">Microsoft InfoPath 2013</span><span class="sxs-lookup"><span data-stu-id="9becb-131">Microsoft InfoPath 2013</span></span></p>
<p><span data-ttu-id="9becb-132">Microsoft OneNote 2013</span><span class="sxs-lookup"><span data-stu-id="9becb-132">Microsoft OneNote 2013</span></span></p>
<p><span data-ttu-id="9becb-133">Microsoft Outlook 2013</span><span class="sxs-lookup"><span data-stu-id="9becb-133">Microsoft Outlook 2013</span></span></p>
<p><span data-ttu-id="9becb-134">Microsoft PowerPoint 2013</span><span class="sxs-lookup"><span data-stu-id="9becb-134">Microsoft PowerPoint 2013</span></span></p>
<p><span data-ttu-id="9becb-135">Microsoft Project 2013</span><span class="sxs-lookup"><span data-stu-id="9becb-135">Microsoft Project 2013</span></span></p>
<p><span data-ttu-id="9becb-136">Microsoft Publisher 2013</span><span class="sxs-lookup"><span data-stu-id="9becb-136">Microsoft Publisher 2013</span></span></p>
<p><span data-ttu-id="9becb-137">Microsoft SharePoint Designer 2013</span><span class="sxs-lookup"><span data-stu-id="9becb-137">Microsoft SharePoint Designer 2013</span></span></p>
<p><span data-ttu-id="9becb-138">Microsoft Visio 2013</span><span class="sxs-lookup"><span data-stu-id="9becb-138">Microsoft Visio 2013</span></span></p>
<p><span data-ttu-id="9becb-139">Microsoft Word 2013</span><span class="sxs-lookup"><span data-stu-id="9becb-139">Microsoft Word 2013</span></span></p>
<p><span data-ttu-id="9becb-140">Microsoft Office Upload-Manager</span><span class="sxs-lookup"><span data-stu-id="9becb-140">Microsoft Office Upload Manager</span></span></p></td>
<td align="left"><p><span data-ttu-id="9becb-141">Microsoft Access 2010</span><span class="sxs-lookup"><span data-stu-id="9becb-141">Microsoft Access 2010</span></span></p>
<p><span data-ttu-id="9becb-142">Microsoft lync 2010</span><span class="sxs-lookup"><span data-stu-id="9becb-142">Microsoft Lync 2010</span></span></p>
<p><span data-ttu-id="9becb-143">Microsoft Excel 2010</span><span class="sxs-lookup"><span data-stu-id="9becb-143">Microsoft Excel 2010</span></span></p>
<p><span data-ttu-id="9becb-144">Microsoft InfoPath 2010</span><span class="sxs-lookup"><span data-stu-id="9becb-144">Microsoft InfoPath 2010</span></span></p>
<p><span data-ttu-id="9becb-145">Microsoft OneNote 2010</span><span class="sxs-lookup"><span data-stu-id="9becb-145">Microsoft OneNote 2010</span></span></p>
<p><span data-ttu-id="9becb-146">Microsoft Outlook 2010</span><span class="sxs-lookup"><span data-stu-id="9becb-146">Microsoft Outlook 2010</span></span></p>
<p><span data-ttu-id="9becb-147">Microsoft PowerPoint 2010</span><span class="sxs-lookup"><span data-stu-id="9becb-147">Microsoft PowerPoint 2010</span></span></p>
<p><span data-ttu-id="9becb-148">Microsoft Project 2010</span><span class="sxs-lookup"><span data-stu-id="9becb-148">Microsoft Project 2010</span></span></p>
<p><span data-ttu-id="9becb-149">Microsoft Publisher 2010</span><span class="sxs-lookup"><span data-stu-id="9becb-149">Microsoft Publisher 2010</span></span></p>
<p><span data-ttu-id="9becb-150">Microsoft SharePoint Designer 2010</span><span class="sxs-lookup"><span data-stu-id="9becb-150">Microsoft SharePoint Designer 2010</span></span></p>
<p><span data-ttu-id="9becb-151">Microsoft Visio 2010</span><span class="sxs-lookup"><span data-stu-id="9becb-151">Microsoft Visio 2010</span></span></p>
<p><span data-ttu-id="9becb-152">Microsoft Word 2010</span><span class="sxs-lookup"><span data-stu-id="9becb-152">Microsoft Word 2010</span></span></p>
<p></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="9becb-153">Bereitstellen der Office 2013-Vorlagen</span><span class="sxs-lookup"><span data-stu-id="9becb-153">Deploying the Office 2013 templates</span></span>


<span data-ttu-id="9becb-154">Sie können die Standort Vorlage für UE-V-Einstellungen mit den folgenden Methoden bereitstellen:</span><span class="sxs-lookup"><span data-stu-id="9becb-154">You can deploy UE-V settings location template with the following methods:</span></span>

-   <span data-ttu-id="9becb-155">**Registrieren einer Vorlage über PowerShell**</span><span class="sxs-lookup"><span data-stu-id="9becb-155">**Registering template via PowerShell**.</span></span> <span data-ttu-id="9becb-156">Wenn Sie Windows PowerShell zum Verwalten von Computern verwenden, führen Sie den folgenden Windows PowerShell-Befehl als Administrator öffnen aus, um die Speicherort Vorlage für diese Einstellungen zu registrieren:</span><span class="sxs-lookup"><span data-stu-id="9becb-156">If you use Windows PowerShell to manage computers, run the following Windows PowerShell command open as an administrator to register this settings location template:</span></span>

    ``` syntax
    Register-UevTemplate -Path <Path_to_Template>
    ```

    <span data-ttu-id="9becb-157">Weitere Informationen zur Verwendung von UE-v und Windows PowerShell finden Sie unter [Verwalten von Standort Vorlagen für die UE-v 2. x-Einstellungen mithilfe von Windows PowerShell und WMI](managing-ue-v-2x-settings-location-templates-using-windows-powershell-and-wmi-both-uevv2.md).</span><span class="sxs-lookup"><span data-stu-id="9becb-157">For more information using UE-V and Windows PowerShell, see [Managing UE-V 2.x Settings Location Templates Using Windows PowerShell and WMI](managing-ue-v-2x-settings-location-templates-using-windows-powershell-and-wmi-both-uevv2.md).</span></span>

-   <span data-ttu-id="9becb-158">**Registrieren einer Vorlage über den Vorlagenkatalog Pfad**</span><span class="sxs-lookup"><span data-stu-id="9becb-158">**Registering template via Template Catalog Path**.</span></span> <span data-ttu-id="9becb-159">Wenn Sie den Katalogpfad der Einstellungs Vorlage zum Verwalten von Vorlagen auf den Computern der Benutzer verwenden, kopieren Sie die Office 2013-Vorlage in den Ordner, der im UE-V-Agent definiert ist.</span><span class="sxs-lookup"><span data-stu-id="9becb-159">If you use the Settings Template Catalog Path to manage templates on users’ computers, copy the Office 2013 template into the folder defined in the UE-V Agent.</span></span> <span data-ttu-id="9becb-160">Wenn der geplante Task "Vorlage automatisch aktualisieren (ApplySettingsCatalog.exe)" das nächste Mal ausgeführt wird, wird die Vorlage "Settings Location" auf dem Gerät registriert.</span><span class="sxs-lookup"><span data-stu-id="9becb-160">The next time the Template Auto Update (ApplySettingsCatalog.exe) scheduled task runs, the settings location template will be registered on the device.</span></span> <span data-ttu-id="9becb-161">Weitere Informationen finden Sie unter [Bereitstellen des Einstellungs Vorlagen Katalogs für UE-V 2](https://technet.microsoft.com/library/dn458942.aspx#deploycatalogue).</span><span class="sxs-lookup"><span data-stu-id="9becb-161">For more information, see [Deploying the Settings Template Catalog for UE-V 2](https://technet.microsoft.com/library/dn458942.aspx#deploycatalogue).</span></span>

-   <span data-ttu-id="9becb-162">**Registrieren einer Vorlage über Configuration Manager**</span><span class="sxs-lookup"><span data-stu-id="9becb-162">**Registering template via Configuration Manager**.</span></span> <span data-ttu-id="9becb-163">Wenn Sie Configuration Manager zum Verwalten Ihrer Speicher Vorlagen für UE-V-Einstellungen verwenden, erstellen Sie die Vorlage-Baseline-CAB neu, importieren Sie Sie in Configuration Manager, und stellen Sie dann den Basisplan für Ihre Clients bereit.</span><span class="sxs-lookup"><span data-stu-id="9becb-163">If you use Configuration Manager to manage your UE-V settings storage templates, then recreate the Template Baseline CAB, import it into Configuration Manager, and then deploy the baseline to your clients.</span></span> <span data-ttu-id="9becb-164">Weitere Informationen finden Sie in den Anleitungen in der Dokumentation zum [System Center 2012-Konfigurationspaket für Microsoft User Experience Virtualization 2](https://go.microsoft.com/fwlink/?LinkId=317263).</span><span class="sxs-lookup"><span data-stu-id="9becb-164">For more information, see the guidance provided in the documentation for the [System Center 2012 Configuration Pack for Microsoft User Experience Virtualization 2](https://go.microsoft.com/fwlink/?LinkId=317263).</span></span>






 

 





