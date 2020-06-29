---
title: Bereitstellen von Microsoft Office2010 mit App-V
description: Bereitstellen von Microsoft Office2010 mit App-V
author: dansimp
ms.assetid: ae0b0459-c0d6-4946-b62d-ff153f52d1fb
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 90454373e9a1c894eba8cbf1b8642656b986bc94
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805867"
---
# <span data-ttu-id="79dab-103">Bereitstellen von Microsoft Office2010 mit App-V</span><span class="sxs-lookup"><span data-stu-id="79dab-103">Deploying Microsoft Office 2010 by Using App-V</span></span>


<span data-ttu-id="79dab-104">Sie können Office 2010-Pakete für Microsoft Application Virtualization (App-V) 5,1 mithilfe einer der folgenden Methoden erstellen:</span><span class="sxs-lookup"><span data-stu-id="79dab-104">You can create Office 2010 packages for Microsoft Application Virtualization (App-V) 5.1 using one of the following methods:</span></span>

-   <span data-ttu-id="79dab-105">Application Virtualization (App-V)-Sequenzer</span><span class="sxs-lookup"><span data-stu-id="79dab-105">Application Virtualization (App-V) Sequencer</span></span>

-   <span data-ttu-id="79dab-106">Application Virtualization (App-V)-Paket Beschleuniger</span><span class="sxs-lookup"><span data-stu-id="79dab-106">Application Virtualization (App-V) Package Accelerator</span></span>

## <span data-ttu-id="79dab-107">App-V-Unterstützung für Office 2010</span><span class="sxs-lookup"><span data-stu-id="79dab-107">App-V support for Office 2010</span></span>


<span data-ttu-id="79dab-108">In der folgenden Tabelle sind die App-V-Versionen, Methoden der Office-Paketerstellung, unterstützte Lizenzierung und unterstützte Bereitstellungen für Office 2010 zu finden.</span><span class="sxs-lookup"><span data-stu-id="79dab-108">The following table shows the App-V versions, methods of Office package creation, supported licensing, and supported deployments for Office 2010.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="79dab-109">Unterstütztes Element</span><span class="sxs-lookup"><span data-stu-id="79dab-109">Supported item</span></span></th>
<th align="left"><span data-ttu-id="79dab-110">Supportstufe</span><span class="sxs-lookup"><span data-stu-id="79dab-110">Level of support</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="79dab-111">Unterstützte App-V-Versionen</span><span class="sxs-lookup"><span data-stu-id="79dab-111">Supported App-V versions</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="79dab-112">4,6</span><span class="sxs-lookup"><span data-stu-id="79dab-112">4.6</span></span></p></li>
<li><p><span data-ttu-id="79dab-113">5.0</span><span class="sxs-lookup"><span data-stu-id="79dab-113">5.0</span></span></p></li>
<li><p><span data-ttu-id="79dab-114">5,1</span><span class="sxs-lookup"><span data-stu-id="79dab-114">5.1</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="79dab-115">Paketerstellung</span><span class="sxs-lookup"><span data-stu-id="79dab-115">Package creation</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="79dab-116">Sequenzierung</span><span class="sxs-lookup"><span data-stu-id="79dab-116">Sequencing</span></span></p></li>
<li><p><span data-ttu-id="79dab-117">Paket Beschleuniger</span><span class="sxs-lookup"><span data-stu-id="79dab-117">Package Accelerator</span></span></p></li>
<li><p><span data-ttu-id="79dab-118">Office Deployment Kit</span><span class="sxs-lookup"><span data-stu-id="79dab-118">Office Deployment Kit</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="79dab-119">Unterstützte Lizenzierung</span><span class="sxs-lookup"><span data-stu-id="79dab-119">Supported licensing</span></span></p></td>
<td align="left"><p><span data-ttu-id="79dab-120">Volumenlizenzierung</span><span class="sxs-lookup"><span data-stu-id="79dab-120">Volume Licensing</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="79dab-121">Unterstützte Bereitstellungen</span><span class="sxs-lookup"><span data-stu-id="79dab-121">Supported deployments</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="79dab-122">Desktop</span><span class="sxs-lookup"><span data-stu-id="79dab-122">Desktop</span></span></p></li>
<li><p><span data-ttu-id="79dab-123">Persönlicher VDI</span><span class="sxs-lookup"><span data-stu-id="79dab-123">Personal VDI</span></span></p></li>
<li><p><span data-ttu-id="79dab-124">RDS</span><span class="sxs-lookup"><span data-stu-id="79dab-124">RDS</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="79dab-125">Erstellen von Office 2010 App-V 5,1 mithilfe des Sequencers</span><span class="sxs-lookup"><span data-stu-id="79dab-125">Creating Office 2010 App-V 5.1 using the sequencer</span></span>


<span data-ttu-id="79dab-126">Die Sequenzierung von Office 2010 ist eine der Hauptmethoden zum Erstellen eines Office 2010-Pakets unter App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="79dab-126">Sequencing Office 2010 is one of the main methods for creating an Office 2010 package on App-V 5.1.</span></span> <span data-ttu-id="79dab-127">Microsoft hat in einem Knowledge Base-Artikel eine detaillierte Anleitung bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="79dab-127">Microsoft has provided a detailed recipe through a Knowledge Base article.</span></span> <span data-ttu-id="79dab-128">Informationen zum Erstellen eines Office 2010-Pakets unter App-V 5,1 finden Sie unter dem folgenden Link für detaillierte Anweisungen:</span><span class="sxs-lookup"><span data-stu-id="79dab-128">To create an Office 2010 package on App-V 5.1, refer to the following link for detailed instructions:</span></span>

[<span data-ttu-id="79dab-129">Sequenzierung von Microsoft Office 2010 in Microsoft Application Virtualization 5,0</span><span class="sxs-lookup"><span data-stu-id="79dab-129">How To Sequence Microsoft Office 2010 in Microsoft Application Virtualization 5.0</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330676)

## <span data-ttu-id="79dab-130">Erstellen von Office 2010-App-V 5,1-Paketen mithilfe von Paket Beschleunigern</span><span class="sxs-lookup"><span data-stu-id="79dab-130">Creating Office 2010 App-V 5.1 packages using package accelerators</span></span>


<span data-ttu-id="79dab-131">Office 2010 App-V 5,1-Pakete können über Paket Beschleuniger erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="79dab-131">Office 2010 App-V 5.1 packages can be created through package accelerators.</span></span> <span data-ttu-id="79dab-132">Microsoft hat Paket Beschleuniger für die Erstellung von Office 2010 unter Windows 10, Windows 8 und Windows 7 bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="79dab-132">Microsoft has provided package accelerators for creating Office 2010 on Windows 10, Windows 8 and Windows 7.</span></span> <span data-ttu-id="79dab-133">Informationen zum Erstellen von Office 2010-Paketen für App-V mithilfe von Paket Beschleunigern finden Sie auf den folgenden Seiten, um auf den entsprechenden Paket Beschleuniger zuzugreifen:</span><span class="sxs-lookup"><span data-stu-id="79dab-133">To create Office 2010 packages on App-V using Package accelerators, refer to the following pages to access the appropriate package accelerator:</span></span>

-   [<span data-ttu-id="79dab-134">App-V 5,0-Paket Beschleuniger für Office Professional Plus 2010 – Windows 8</span><span class="sxs-lookup"><span data-stu-id="79dab-134">App-V 5.0 Package Accelerator for Office Professional Plus 2010 – Windows 8</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330677)

-   [<span data-ttu-id="79dab-135">App-V 5,0-Paket Beschleuniger für Office Professional Plus 2010 – Windows 7</span><span class="sxs-lookup"><span data-stu-id="79dab-135">App-V 5.0 Package Accelerator for Office Professional Plus 2010 – Windows 7</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330678)

<span data-ttu-id="79dab-136">Ausführliche Anweisungen zum Erstellen von virtuellen Anwendungspaketen mithilfe von App-v-Paket Beschleunigern finden Sie unter [Erstellen eines virtuellen Anwendungspakets mithilfe eines App-v-Paket Beschleunigers](how-to-create-a-virtual-application-package-using-an-app-v-package-accelerator51.md).</span><span class="sxs-lookup"><span data-stu-id="79dab-136">For detailed instructions on how to create virtual application packages using App-V package accelerators, see [How to Create a Virtual Application Package Using an App-V Package Accelerator](how-to-create-a-virtual-application-package-using-an-app-v-package-accelerator51.md).</span></span>

## <span data-ttu-id="79dab-137">Bereitstellen des Microsoft Office-Pakets für App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="79dab-137">Deploying the Microsoft Office package for App-V 5.1</span></span>


<span data-ttu-id="79dab-138">Sie können Office 2010-Pakete mithilfe einer der folgenden Bereitstellungsmethoden für App-V bereitstellen:</span><span class="sxs-lookup"><span data-stu-id="79dab-138">You can deploy Office 2010 packages by using any of the following App-V deployment methods:</span></span>

-   <span data-ttu-id="79dab-139">System Center Konfigurations-Manager</span><span class="sxs-lookup"><span data-stu-id="79dab-139">System Center Configuration Manager</span></span>

-   <span data-ttu-id="79dab-140">App-V-Server</span><span class="sxs-lookup"><span data-stu-id="79dab-140">App-V server</span></span>

-   <span data-ttu-id="79dab-141">Eigenständige über PowerShell-Befehle</span><span class="sxs-lookup"><span data-stu-id="79dab-141">Stand-alone through PowerShell commands</span></span>

## <span data-ttu-id="79dab-142">Office-App-V-Paketverwaltung und-Anpassung</span><span class="sxs-lookup"><span data-stu-id="79dab-142">Office App-V package management and customization</span></span>


<span data-ttu-id="79dab-143">Office 2010-Pakete können wie alle anderen App-V 5,1-Pakete über bekannte Paket Verwaltungsmechanismen verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="79dab-143">Office 2010 packages can be managed like any other App-V 5.1 packages through known package management mechanisms.</span></span> <span data-ttu-id="79dab-144">Es sind keine speziellen Anweisungen erforderlich, beispielsweise zum Hinzufügen, veröffentlichen, Aufheben der Veröffentlichung oder Entfernen von Office-Paketen.</span><span class="sxs-lookup"><span data-stu-id="79dab-144">No special instructions are needed, for example, to add, publish, unpublish, or remove Office packages.</span></span>

## <span data-ttu-id="79dab-145">Integration von Microsoft Office in Windows</span><span class="sxs-lookup"><span data-stu-id="79dab-145">Microsoft Office integration with Windows</span></span>


<span data-ttu-id="79dab-146">Die folgende Tabelle enthält eine vollständige Liste der unterstützten Integrationspunkte für Office 2010.</span><span class="sxs-lookup"><span data-stu-id="79dab-146">The following table provides a full list of supported integration points for Office 2010.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="79dab-147">Erweiterungspunkt</span><span class="sxs-lookup"><span data-stu-id="79dab-147">Extension Point</span></span></th>
<th align="left"><span data-ttu-id="79dab-148">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="79dab-148">Description</span></span></th>
<th align="left"><span data-ttu-id="79dab-149">Office 2010</span><span class="sxs-lookup"><span data-stu-id="79dab-149">Office 2010</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="79dab-150">Lync-Besprechungsteilnahme-Plug-in für Firefox und Chrome</span><span class="sxs-lookup"><span data-stu-id="79dab-150">Lync meeting Join Plug-in for Firefox and Chrome</span></span></p></td>
<td align="left"><p><span data-ttu-id="79dab-151">Benutzer können über Firefox und Chrome an lync-Besprechungen teilnehmen</span><span class="sxs-lookup"><span data-stu-id="79dab-151">User can join Lync meetings from Firefox and Chrome</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="79dab-152">An den OneNote-Druckertreiber gesendet</span><span class="sxs-lookup"><span data-stu-id="79dab-152">Sent to OneNote Print Driver</span></span></p></td>
<td align="left"><p><span data-ttu-id="79dab-153">Benutzer kann in OneNote drucken</span><span class="sxs-lookup"><span data-stu-id="79dab-153">User can print to OneNote</span></span></p></td>
<td align="left"><p><span data-ttu-id="79dab-154">Ja</span><span class="sxs-lookup"><span data-stu-id="79dab-154">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="79dab-155">Verknüpfte OneNote-Notizen</span><span class="sxs-lookup"><span data-stu-id="79dab-155">OneNote Linked Notes</span></span></p></td>
<td align="left"><p><span data-ttu-id="79dab-156">Verknüpfte OneNote-Notizen</span><span class="sxs-lookup"><span data-stu-id="79dab-156">OneNote Linked Notes</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="79dab-157">An OneNote Internet Explorer-Add-in senden</span><span class="sxs-lookup"><span data-stu-id="79dab-157">Send to OneNote Internet Explorer Add-In</span></span></p></td>
<td align="left"><p><span data-ttu-id="79dab-158">Benutzer kann von IE an OneNote senden</span><span class="sxs-lookup"><span data-stu-id="79dab-158">User can send to OneNote from IE</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="79dab-159">Firewall-Ausnahme für lync und Outlook</span><span class="sxs-lookup"><span data-stu-id="79dab-159">Firewall Exception for Lync and Outlook</span></span></p></td>
<td align="left"><p><span data-ttu-id="79dab-160">Firewall-Ausnahme für lync und Outlook</span><span class="sxs-lookup"><span data-stu-id="79dab-160">Firewall Exception for Lync and Outlook</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="79dab-161">MAPI-Client</span><span class="sxs-lookup"><span data-stu-id="79dab-161">MAPI Client</span></span></p></td>
<td align="left"><p><span data-ttu-id="79dab-162">Systemeigene apps und Add-Ins können mit Virtual Outlook über MAPI interagieren</span><span class="sxs-lookup"><span data-stu-id="79dab-162">Native apps and add-ins can interact with virtual Outlook through MAPI</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="79dab-163">SharePoint-Plug-in für Firefox</span><span class="sxs-lookup"><span data-stu-id="79dab-163">SharePoint Plugin for Firefox</span></span></p></td>
<td align="left"><p><span data-ttu-id="79dab-164">Benutzer kann SharePoint-Features in Firefox verwenden</span><span class="sxs-lookup"><span data-stu-id="79dab-164">User can use SharePoint features in Firefox</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="79dab-165">Applet für Mail-Systemsteuerung</span><span class="sxs-lookup"><span data-stu-id="79dab-165">Mail Control Panel Applet</span></span></p></td>
<td align="left"><p><span data-ttu-id="79dab-166">Der Benutzer erhält das Applet für die Mail-Systemsteuerung in Outlook</span><span class="sxs-lookup"><span data-stu-id="79dab-166">User gets the mail control panel applet in Outlook</span></span></p></td>
<td align="left"><p><span data-ttu-id="79dab-167">Ja</span><span class="sxs-lookup"><span data-stu-id="79dab-167">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="79dab-168">Primäre Interop-Assemblys</span><span class="sxs-lookup"><span data-stu-id="79dab-168">Primary Interop Assemblies</span></span></p></td>
<td align="left"><p><span data-ttu-id="79dab-169">Unterstützung verwalteter Add-ins</span><span class="sxs-lookup"><span data-stu-id="79dab-169">Support managed add-ins</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="79dab-170">Cache Handler für Office-Dokumente</span><span class="sxs-lookup"><span data-stu-id="79dab-170">Office Document Cache Handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="79dab-171">Ermöglicht den Dokumenten Cache für Office-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="79dab-171">Allows Document Cache for Office applications</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="79dab-172">Outlook-Protokoll such Handler</span><span class="sxs-lookup"><span data-stu-id="79dab-172">Outlook Protocol Search handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="79dab-173">Benutzer kann in Outlook suchen</span><span class="sxs-lookup"><span data-stu-id="79dab-173">User can search in outlook</span></span></p></td>
<td align="left"><p><span data-ttu-id="79dab-174">Ja</span><span class="sxs-lookup"><span data-stu-id="79dab-174">Yes</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="79dab-175">ActiveX-Steuerelemente:</span><span class="sxs-lookup"><span data-stu-id="79dab-175">Active X Controls:</span></span></p></td>
<td align="left"><p><span data-ttu-id="79dab-176">Weitere Informationen zu ActiveX-Steuerelementen finden Sie unter <a href="https://go.microsoft.com/fwlink/p/?LinkId=331361" data-raw-source="[ActiveX Control API Reference](https://go.microsoft.com/fwlink/p/?LinkId=331361)"> API-Referenz für ActiveX-Steuerelemente </a> .</span><span class="sxs-lookup"><span data-stu-id="79dab-176">For more information on ActiveX controls, refer to <a href="https://go.microsoft.com/fwlink/p/?LinkId=331361" data-raw-source="[ActiveX Control API Reference](https://go.microsoft.com/fwlink/p/?LinkId=331361)">ActiveX Control API Reference</a>.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="79dab-177">Groove. SiteClient</span><span class="sxs-lookup"><span data-stu-id="79dab-177">Groove.SiteClient</span></span></p></td>
<td align="left"><p><span data-ttu-id="79dab-178">Active X-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="79dab-178">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="79dab-179">PortalConnect.PersonalSite</span><span class="sxs-lookup"><span data-stu-id="79dab-179">PortalConnect.PersonalSite</span></span></p></td>
<td align="left"><p><span data-ttu-id="79dab-180">Active X-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="79dab-180">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="79dab-181">SharePoint. OpenDocuments</span><span class="sxs-lookup"><span data-stu-id="79dab-181">SharePoint.openDocuments</span></span></p></td>
<td align="left"><p><span data-ttu-id="79dab-182">Active X-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="79dab-182">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="79dab-183">SharePoint. ExportDatabase</span><span class="sxs-lookup"><span data-stu-id="79dab-183">SharePoint.ExportDatabase</span></span></p></td>
<td align="left"><p><span data-ttu-id="79dab-184">Active X-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="79dab-184">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="79dab-185">SharePoint. SpreadSheetLauncher</span><span class="sxs-lookup"><span data-stu-id="79dab-185">SharePoint.SpreadSheetLauncher</span></span></p></td>
<td align="left"><p><span data-ttu-id="79dab-186">Active X-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="79dab-186">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="79dab-187">SharePoint. StssyncHander</span><span class="sxs-lookup"><span data-stu-id="79dab-187">SharePoint.StssyncHander</span></span></p></td>
<td align="left"><p><span data-ttu-id="79dab-188">Active X-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="79dab-188">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="79dab-189">SharePoint. DragUploadCtl</span><span class="sxs-lookup"><span data-stu-id="79dab-189">SharePoint.DragUploadCtl</span></span></p></td>
<td align="left"><p><span data-ttu-id="79dab-190">Active X-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="79dab-190">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="79dab-191">SharePoint. DragDownloadCtl</span><span class="sxs-lookup"><span data-stu-id="79dab-191">SharePoint.DragDownloadCtl</span></span></p></td>
<td align="left"><p><span data-ttu-id="79dab-192">Active X-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="79dab-192">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="79dab-193">Sharpoint. XMLDocuments</span><span class="sxs-lookup"><span data-stu-id="79dab-193">Sharpoint.OpenXMLDocuments</span></span></p></td>
<td align="left"><p><span data-ttu-id="79dab-194">Active X-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="79dab-194">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="79dab-195">SharePoint. ClipboardCtl</span><span class="sxs-lookup"><span data-stu-id="79dab-195">Sharepoint.ClipboardCtl</span></span></p></td>
<td align="left"><p><span data-ttu-id="79dab-196">Active X-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="79dab-196">Active X control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="79dab-197">Winproj. Activator</span><span class="sxs-lookup"><span data-stu-id="79dab-197">WinProj.Activator</span></span></p></td>
<td align="left"><p><span data-ttu-id="79dab-198">Active X-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="79dab-198">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="79dab-199">Name. NameCtrl</span><span class="sxs-lookup"><span data-stu-id="79dab-199">Name.NameCtrl</span></span></p></td>
<td align="left"><p><span data-ttu-id="79dab-200">Active X-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="79dab-200">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="79dab-201">STSUPld. CopyCtl</span><span class="sxs-lookup"><span data-stu-id="79dab-201">STSUPld.CopyCtl</span></span></p></td>
<td align="left"><p><span data-ttu-id="79dab-202">Active X-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="79dab-202">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="79dab-203">CommunicatorMeetingJoinAx. joinmanager</span><span class="sxs-lookup"><span data-stu-id="79dab-203">CommunicatorMeetingJoinAx.JoinManager</span></span></p></td>
<td align="left"><p><span data-ttu-id="79dab-204">Active X-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="79dab-204">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="79dab-205">LISTNET. Listnet</span><span class="sxs-lookup"><span data-stu-id="79dab-205">LISTNET.Listnet</span></span></p></td>
<td align="left"><p><span data-ttu-id="79dab-206">Active X-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="79dab-206">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="79dab-207">OneDrive pro-Browser-Helfer</span><span class="sxs-lookup"><span data-stu-id="79dab-207">OneDrive Pro Browser Helper</span></span></p></td>
<td align="left"><p><span data-ttu-id="79dab-208">Active X-Steuerelement]</span><span class="sxs-lookup"><span data-stu-id="79dab-208">Active X Control]</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="79dab-209">OneDrive pro-symbolüberlagerungen</span><span class="sxs-lookup"><span data-stu-id="79dab-209">OneDrive Pro Icon Overlays</span></span></p></td>
<td align="left"><p><span data-ttu-id="79dab-210">Windows Explorer-Shell-Symbol Overlays, wenn Benutzerordner OneDrive pro-Ordner anzeigen</span><span class="sxs-lookup"><span data-stu-id="79dab-210">Windows explorer shell icon overlays when users look at folders OneDrive Pro folders</span></span></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="79dab-211">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="79dab-211">Additional resources</span></span>


**<span data-ttu-id="79dab-212">Office 2013-App-V-Pakete – zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="79dab-212">Office 2013 App-V Packages Additional Resources</span></span>**

[<span data-ttu-id="79dab-213">Unterstützte Szenarien für die Bereitstellung von Microsoft Office als sequenziertes App-V-Paket</span><span class="sxs-lookup"><span data-stu-id="79dab-213">Supported scenarios for deploying Microsoft Office as a sequenced App-V Package</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330680)

**<span data-ttu-id="79dab-214">Office 2010-App-V-Pakete</span><span class="sxs-lookup"><span data-stu-id="79dab-214">Office 2010 App-V Packages</span></span>**

[<span data-ttu-id="79dab-215">Microsoft Office 2010-Sequenzierung-Kit für Microsoft Application Virtualization 5,0</span><span class="sxs-lookup"><span data-stu-id="79dab-215">Microsoft Office 2010 Sequencing Kit for Microsoft Application Virtualization 5.0</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330681)

[<span data-ttu-id="79dab-216">Bekannte Probleme beim Erstellen oder Verwenden eines App-V 5,0 Office 2010-Pakets</span><span class="sxs-lookup"><span data-stu-id="79dab-216">Known issues when you create or use an App-V 5.0 Office 2010 package</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330682)

[<span data-ttu-id="79dab-217">Sequenzierung von Microsoft Office 2010 in Microsoft Application Virtualization 5,0</span><span class="sxs-lookup"><span data-stu-id="79dab-217">How to sequence Microsoft Office 2010 in Microsoft Application Virtualization 5.0</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330676)

**<span data-ttu-id="79dab-218">Verbindungsgruppen</span><span class="sxs-lookup"><span data-stu-id="79dab-218">Connection Groups</span></span>**

[<span data-ttu-id="79dab-219">Bereitstellen von Verbindungsgruppen in Microsoft App-V V5</span><span class="sxs-lookup"><span data-stu-id="79dab-219">Deploying Connection Groups in Microsoft App-V v5</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330683)

[<span data-ttu-id="79dab-220">Verwalten von Verbindungsgruppen</span><span class="sxs-lookup"><span data-stu-id="79dab-220">Managing Connection Groups</span></span>](managing-connection-groups51.md)

**<span data-ttu-id="79dab-221">Dynamische Konfiguration</span><span class="sxs-lookup"><span data-stu-id="79dab-221">Dynamic Configuration</span></span>**

[<span data-ttu-id="79dab-222">Informationen zur dynamischen Konfiguration in App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="79dab-222">About App-V 5.1 Dynamic Configuration</span></span>](about-app-v-51-dynamic-configuration.md)






 

 





