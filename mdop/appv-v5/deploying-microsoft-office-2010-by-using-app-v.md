---
title: Bereitstellen von Microsoft Office2010 mit App-V
description: Bereitstellen von Microsoft Office2010 mit App-V
author: dansimp
ms.assetid: 0a9e496e-82a1-4dc0-a496-7b21eaa00f53
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 303a44d921e40a411a4c4ea4622f06a76b8ed9c6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805876"
---
# <span data-ttu-id="1ee7d-103">Bereitstellen von Microsoft Office2010 mit App-V</span><span class="sxs-lookup"><span data-stu-id="1ee7d-103">Deploying Microsoft Office 2010 by Using App-V</span></span>


<span data-ttu-id="1ee7d-104">Sie können Office 2010-Pakete für Application Virtualization 5,0 mithilfe einer der folgenden Methoden erstellen:</span><span class="sxs-lookup"><span data-stu-id="1ee7d-104">You can create Office 2010 packages for Application Virtualization 5.0 using one of the following methods:</span></span>

-   <span data-ttu-id="1ee7d-105">Application Virtualization (App-V)-Sequenzer</span><span class="sxs-lookup"><span data-stu-id="1ee7d-105">Application Virtualization (App-V) Sequencer</span></span>

-   <span data-ttu-id="1ee7d-106">Application Virtualization (App-V)-Paket Beschleuniger</span><span class="sxs-lookup"><span data-stu-id="1ee7d-106">Application Virtualization (App-V) Package Accelerator</span></span>

## <span data-ttu-id="1ee7d-107">App-V-Unterstützung für Office 2010</span><span class="sxs-lookup"><span data-stu-id="1ee7d-107">App-V support for Office 2010</span></span>


<span data-ttu-id="1ee7d-108">In der folgenden Tabelle sind die App-V-Versionen, Methoden der Office-Paketerstellung, unterstützte Lizenzierung und unterstützte Bereitstellungen für Office 2010 zu finden.</span><span class="sxs-lookup"><span data-stu-id="1ee7d-108">The following table shows the App-V versions, methods of Office package creation, supported licensing, and supported deployments for Office 2010.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="1ee7d-109">Unterstütztes Element</span><span class="sxs-lookup"><span data-stu-id="1ee7d-109">Supported item</span></span></th>
<th align="left"><span data-ttu-id="1ee7d-110">Supportstufe</span><span class="sxs-lookup"><span data-stu-id="1ee7d-110">Level of support</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1ee7d-111">Unterstützte App-V-Versionen</span><span class="sxs-lookup"><span data-stu-id="1ee7d-111">Supported App-V versions</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="1ee7d-112">4,6</span><span class="sxs-lookup"><span data-stu-id="1ee7d-112">4.6</span></span></p></li>
<li><p><span data-ttu-id="1ee7d-113">5.0</span><span class="sxs-lookup"><span data-stu-id="1ee7d-113">5.0</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1ee7d-114">Paketerstellung</span><span class="sxs-lookup"><span data-stu-id="1ee7d-114">Package creation</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="1ee7d-115">Sequenzierung</span><span class="sxs-lookup"><span data-stu-id="1ee7d-115">Sequencing</span></span></p></li>
<li><p><span data-ttu-id="1ee7d-116">Paket Beschleuniger</span><span class="sxs-lookup"><span data-stu-id="1ee7d-116">Package Accelerator</span></span></p></li>
<li><p><span data-ttu-id="1ee7d-117">Office Deployment Kit</span><span class="sxs-lookup"><span data-stu-id="1ee7d-117">Office Deployment Kit</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1ee7d-118">Unterstützte Lizenzierung</span><span class="sxs-lookup"><span data-stu-id="1ee7d-118">Supported licensing</span></span></p></td>
<td align="left"><p><span data-ttu-id="1ee7d-119">Volumenlizenzierung</span><span class="sxs-lookup"><span data-stu-id="1ee7d-119">Volume Licensing</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1ee7d-120">Unterstützte Bereitstellungen</span><span class="sxs-lookup"><span data-stu-id="1ee7d-120">Supported deployments</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="1ee7d-121">Desktop</span><span class="sxs-lookup"><span data-stu-id="1ee7d-121">Desktop</span></span></p></li>
<li><p><span data-ttu-id="1ee7d-122">Persönlicher VDI</span><span class="sxs-lookup"><span data-stu-id="1ee7d-122">Personal VDI</span></span></p></li>
<li><p><span data-ttu-id="1ee7d-123">RDS</span><span class="sxs-lookup"><span data-stu-id="1ee7d-123">RDS</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="1ee7d-124">Erstellen von Office 2010 App-V 5,0 mithilfe des Sequencers</span><span class="sxs-lookup"><span data-stu-id="1ee7d-124">Creating Office 2010 App-V 5.0 using the sequencer</span></span>


<span data-ttu-id="1ee7d-125">Die Sequenzierung von Office 2010 ist eine der Hauptmethoden zum Erstellen eines Office 2010-Pakets unter App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="1ee7d-125">Sequencing Office 2010 is one of the main methods for creating an Office 2010 package on App-V 5.0.</span></span> <span data-ttu-id="1ee7d-126">Microsoft hat in einem Knowledge Base-Artikel eine detaillierte Anleitung bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="1ee7d-126">Microsoft has provided a detailed recipe through a Knowledge Base article.</span></span> <span data-ttu-id="1ee7d-127">Informationen zum Erstellen eines Office 2010-Pakets unter App-V 5,0 finden Sie unter dem folgenden Link für detaillierte Anweisungen:</span><span class="sxs-lookup"><span data-stu-id="1ee7d-127">To create an Office 2010 package on App-V 5.0, refer to the following link for detailed instructions:</span></span>

[<span data-ttu-id="1ee7d-128">Sequenzierung von Microsoft Office 2010 in Microsoft Application Virtualization 5,0</span><span class="sxs-lookup"><span data-stu-id="1ee7d-128">How To Sequence Microsoft Office 2010 in Microsoft Application Virtualization 5.0</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330676)

## <span data-ttu-id="1ee7d-129">Erstellen von Office 2010-App-V 5,0-Paketen mithilfe von Paket Beschleunigern</span><span class="sxs-lookup"><span data-stu-id="1ee7d-129">Creating Office 2010 App-V 5.0 packages using package accelerators</span></span>


<span data-ttu-id="1ee7d-130">Office 2010 App-V 5,0-Pakete können über Paket Beschleuniger erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="1ee7d-130">Office 2010 App-V 5.0 packages can be created through package accelerators.</span></span> <span data-ttu-id="1ee7d-131">Microsoft hat Paket Beschleuniger für die Erstellung von Office 2010 unter Windows 8 und Windows 7 bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="1ee7d-131">Microsoft has provided package accelerators for creating Office 2010 on Windows 8 and Windows 7.</span></span> <span data-ttu-id="1ee7d-132">Informationen zum Erstellen von Office 2010-Paketen für App-V mithilfe von Paket Beschleunigern finden Sie auf den folgenden Seiten, um auf den entsprechenden Paket Beschleuniger zuzugreifen:</span><span class="sxs-lookup"><span data-stu-id="1ee7d-132">To create Office 2010 packages on App-V using Package accelerators, refer to the following pages to access the appropriate package accelerator:</span></span>

-   [<span data-ttu-id="1ee7d-133">App-V 5,0-Paket Beschleuniger für Office Professional Plus 2010 – Windows 8</span><span class="sxs-lookup"><span data-stu-id="1ee7d-133">App-V 5.0 Package Accelerator for Office Professional Plus 2010 – Windows 8</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330677)

-   [<span data-ttu-id="1ee7d-134">App-V 5,0-Paket Beschleuniger für Office Professional Plus 2010 – Windows 7</span><span class="sxs-lookup"><span data-stu-id="1ee7d-134">App-V 5.0 Package Accelerator for Office Professional Plus 2010 – Windows 7</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330678)

<span data-ttu-id="1ee7d-135">Ausführliche Anweisungen zum Erstellen von virtuellen Anwendungspaketen mithilfe von App-v-Paket Beschleunigern finden Sie unter [Erstellen eines virtuellen Anwendungspakets mithilfe eines App-v-Paket Beschleunigers](how-to-create-a-virtual-application-package-using-an-app-v-package-accelerator.md).</span><span class="sxs-lookup"><span data-stu-id="1ee7d-135">For detailed instructions on how to create virtual application packages using App-V package accelerators, see [How to Create a Virtual Application Package Using an App-V Package Accelerator](how-to-create-a-virtual-application-package-using-an-app-v-package-accelerator.md).</span></span>

## <span data-ttu-id="1ee7d-136">Bereitstellen des Microsoft Office-Pakets für App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="1ee7d-136">Deploying the Microsoft Office package for App-V 5.0</span></span>


<span data-ttu-id="1ee7d-137">Sie können Office 2010-Pakete mithilfe einer der folgenden Bereitstellungsmethoden für App-V bereitstellen:</span><span class="sxs-lookup"><span data-stu-id="1ee7d-137">You can deploy Office 2010 packages by using any of the following App-V deployment methods:</span></span>

-   <span data-ttu-id="1ee7d-138">System Center Konfigurations-Manager</span><span class="sxs-lookup"><span data-stu-id="1ee7d-138">System Center Configuration Manager</span></span>

-   <span data-ttu-id="1ee7d-139">App-V-Server</span><span class="sxs-lookup"><span data-stu-id="1ee7d-139">App-V server</span></span>

-   <span data-ttu-id="1ee7d-140">Eigenständige über PowerShell-Befehle</span><span class="sxs-lookup"><span data-stu-id="1ee7d-140">Stand-alone through PowerShell commands</span></span>

## <span data-ttu-id="1ee7d-141">Office-App-V-Paketverwaltung und-Anpassung</span><span class="sxs-lookup"><span data-stu-id="1ee7d-141">Office App-V package management and customization</span></span>


<span data-ttu-id="1ee7d-142">Office 2010-Pakete können wie alle anderen App-V 5,0-Pakete über bekannte Paket Verwaltungsmechanismen verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="1ee7d-142">Office 2010 packages can be managed like any other App-V 5.0 packages through known package management mechanisms.</span></span> <span data-ttu-id="1ee7d-143">Es sind keine speziellen Anweisungen erforderlich, beispielsweise zum Hinzufügen, veröffentlichen, Aufheben der Veröffentlichung oder Entfernen von Office-Paketen.</span><span class="sxs-lookup"><span data-stu-id="1ee7d-143">No special instructions are needed, for example, to add, publish, unpublish, or remove Office packages.</span></span>

## <span data-ttu-id="1ee7d-144">Integration von Microsoft Office in Windows</span><span class="sxs-lookup"><span data-stu-id="1ee7d-144">Microsoft Office integration with Windows</span></span>


<span data-ttu-id="1ee7d-145">Die folgende Tabelle enthält eine vollständige Liste der unterstützten Integrationspunkte für Office 2010.</span><span class="sxs-lookup"><span data-stu-id="1ee7d-145">The following table provides a full list of supported integration points for Office 2010.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="1ee7d-146">Erweiterungspunkt</span><span class="sxs-lookup"><span data-stu-id="1ee7d-146">Extension Point</span></span></th>
<th align="left"><span data-ttu-id="1ee7d-147">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1ee7d-147">Description</span></span></th>
<th align="left"><span data-ttu-id="1ee7d-148">Office 2010</span><span class="sxs-lookup"><span data-stu-id="1ee7d-148">Office 2010</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1ee7d-149">Lync-Besprechungsteilnahme-Plug-in für Firefox und Chrome</span><span class="sxs-lookup"><span data-stu-id="1ee7d-149">Lync meeting Join Plug-in for Firefox and Chrome</span></span></p></td>
<td align="left"><p><span data-ttu-id="1ee7d-150">Benutzer können über Firefox und Chrome an lync-Besprechungen teilnehmen</span><span class="sxs-lookup"><span data-stu-id="1ee7d-150">User can join Lync meetings from Firefox and Chrome</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1ee7d-151">An den OneNote-Druckertreiber gesendet</span><span class="sxs-lookup"><span data-stu-id="1ee7d-151">Sent to OneNote Print Driver</span></span></p></td>
<td align="left"><p><span data-ttu-id="1ee7d-152">Benutzer kann in OneNote drucken</span><span class="sxs-lookup"><span data-stu-id="1ee7d-152">User can print to OneNote</span></span></p></td>
<td align="left"><p><span data-ttu-id="1ee7d-153">Ja</span><span class="sxs-lookup"><span data-stu-id="1ee7d-153">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1ee7d-154">Verknüpfte OneNote-Notizen</span><span class="sxs-lookup"><span data-stu-id="1ee7d-154">OneNote Linked Notes</span></span></p></td>
<td align="left"><p><span data-ttu-id="1ee7d-155">Verknüpfte OneNote-Notizen</span><span class="sxs-lookup"><span data-stu-id="1ee7d-155">OneNote Linked Notes</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1ee7d-156">An OneNote Internet Explorer-Add-in senden</span><span class="sxs-lookup"><span data-stu-id="1ee7d-156">Send to OneNote Internet Explorer Add-In</span></span></p></td>
<td align="left"><p><span data-ttu-id="1ee7d-157">Benutzer kann von IE an OneNote senden</span><span class="sxs-lookup"><span data-stu-id="1ee7d-157">User can send to OneNote from IE</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1ee7d-158">Firewall-Ausnahme für lync und Outlook</span><span class="sxs-lookup"><span data-stu-id="1ee7d-158">Firewall Exception for Lync and Outlook</span></span></p></td>
<td align="left"><p><span data-ttu-id="1ee7d-159">Firewall-Ausnahme für lync und Outlook</span><span class="sxs-lookup"><span data-stu-id="1ee7d-159">Firewall Exception for Lync and Outlook</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1ee7d-160">MAPI-Client</span><span class="sxs-lookup"><span data-stu-id="1ee7d-160">MAPI Client</span></span></p></td>
<td align="left"><p><span data-ttu-id="1ee7d-161">Systemeigene apps und Add-Ins können mit Virtual Outlook über MAPI interagieren</span><span class="sxs-lookup"><span data-stu-id="1ee7d-161">Native apps and add-ins can interact with virtual Outlook through MAPI</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1ee7d-162">SharePoint-Plug-in für Firefox</span><span class="sxs-lookup"><span data-stu-id="1ee7d-162">SharePoint Plugin for Firefox</span></span></p></td>
<td align="left"><p><span data-ttu-id="1ee7d-163">Benutzer kann SharePoint-Features in Firefox verwenden</span><span class="sxs-lookup"><span data-stu-id="1ee7d-163">User can use SharePoint features in Firefox</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1ee7d-164">Applet für Mail-Systemsteuerung</span><span class="sxs-lookup"><span data-stu-id="1ee7d-164">Mail Control Panel Applet</span></span></p></td>
<td align="left"><p><span data-ttu-id="1ee7d-165">Der Benutzer erhält das Applet für die Mail-Systemsteuerung in Outlook</span><span class="sxs-lookup"><span data-stu-id="1ee7d-165">User gets the mail control panel applet in Outlook</span></span></p></td>
<td align="left"><p><span data-ttu-id="1ee7d-166">Ja</span><span class="sxs-lookup"><span data-stu-id="1ee7d-166">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1ee7d-167">Primäre Interop-Assemblys</span><span class="sxs-lookup"><span data-stu-id="1ee7d-167">Primary Interop Assemblies</span></span></p></td>
<td align="left"><p><span data-ttu-id="1ee7d-168">Unterstützung verwalteter Add-ins</span><span class="sxs-lookup"><span data-stu-id="1ee7d-168">Support managed add-ins</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1ee7d-169">Cache Handler für Office-Dokumente</span><span class="sxs-lookup"><span data-stu-id="1ee7d-169">Office Document Cache Handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="1ee7d-170">Ermöglicht den Dokumenten Cache für Office-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="1ee7d-170">Allows Document Cache for Office applications</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1ee7d-171">Outlook-Protokoll such Handler</span><span class="sxs-lookup"><span data-stu-id="1ee7d-171">Outlook Protocol Search handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="1ee7d-172">Benutzer kann in Outlook suchen</span><span class="sxs-lookup"><span data-stu-id="1ee7d-172">User can search in outlook</span></span></p></td>
<td align="left"><p><span data-ttu-id="1ee7d-173">Ja</span><span class="sxs-lookup"><span data-stu-id="1ee7d-173">Yes</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1ee7d-174">ActiveX-Steuerelemente:</span><span class="sxs-lookup"><span data-stu-id="1ee7d-174">Active X Controls:</span></span></p></td>
<td align="left"><p><span data-ttu-id="1ee7d-175">Weitere Informationen zu ActiveX-Steuerelementen finden Sie unter <a href="https://go.microsoft.com/fwlink/p/?LinkId=331361" data-raw-source="[ActiveX Control API Reference](https://go.microsoft.com/fwlink/p/?LinkId=331361)"> API-Referenz für ActiveX-Steuerelemente </a> .</span><span class="sxs-lookup"><span data-stu-id="1ee7d-175">For more information on ActiveX controls, refer to <a href="https://go.microsoft.com/fwlink/p/?LinkId=331361" data-raw-source="[ActiveX Control API Reference](https://go.microsoft.com/fwlink/p/?LinkId=331361)">ActiveX Control API Reference</a>.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="1ee7d-176">Groove. SiteClient</span><span class="sxs-lookup"><span data-stu-id="1ee7d-176">Groove.SiteClient</span></span></p></td>
<td align="left"><p><span data-ttu-id="1ee7d-177">Active X-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="1ee7d-177">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="1ee7d-178">PortalConnect.PersonalSite</span><span class="sxs-lookup"><span data-stu-id="1ee7d-178">PortalConnect.PersonalSite</span></span></p></td>
<td align="left"><p><span data-ttu-id="1ee7d-179">Active X-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="1ee7d-179">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="1ee7d-180">SharePoint. OpenDocuments</span><span class="sxs-lookup"><span data-stu-id="1ee7d-180">SharePoint.openDocuments</span></span></p></td>
<td align="left"><p><span data-ttu-id="1ee7d-181">Active X-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="1ee7d-181">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="1ee7d-182">SharePoint. ExportDatabase</span><span class="sxs-lookup"><span data-stu-id="1ee7d-182">SharePoint.ExportDatabase</span></span></p></td>
<td align="left"><p><span data-ttu-id="1ee7d-183">Active X-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="1ee7d-183">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="1ee7d-184">SharePoint. SpreadSheetLauncher</span><span class="sxs-lookup"><span data-stu-id="1ee7d-184">SharePoint.SpreadSheetLauncher</span></span></p></td>
<td align="left"><p><span data-ttu-id="1ee7d-185">Active X-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="1ee7d-185">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="1ee7d-186">SharePoint. StssyncHander</span><span class="sxs-lookup"><span data-stu-id="1ee7d-186">SharePoint.StssyncHander</span></span></p></td>
<td align="left"><p><span data-ttu-id="1ee7d-187">Active X-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="1ee7d-187">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="1ee7d-188">SharePoint. DragUploadCtl</span><span class="sxs-lookup"><span data-stu-id="1ee7d-188">SharePoint.DragUploadCtl</span></span></p></td>
<td align="left"><p><span data-ttu-id="1ee7d-189">Active X-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="1ee7d-189">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="1ee7d-190">SharePoint. DragDownloadCtl</span><span class="sxs-lookup"><span data-stu-id="1ee7d-190">SharePoint.DragDownloadCtl</span></span></p></td>
<td align="left"><p><span data-ttu-id="1ee7d-191">Active X-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="1ee7d-191">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="1ee7d-192">Sharpoint. XMLDocuments</span><span class="sxs-lookup"><span data-stu-id="1ee7d-192">Sharpoint.OpenXMLDocuments</span></span></p></td>
<td align="left"><p><span data-ttu-id="1ee7d-193">Active X-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="1ee7d-193">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="1ee7d-194">SharePoint. ClipboardCtl</span><span class="sxs-lookup"><span data-stu-id="1ee7d-194">Sharepoint.ClipboardCtl</span></span></p></td>
<td align="left"><p><span data-ttu-id="1ee7d-195">Active X-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="1ee7d-195">Active X control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="1ee7d-196">Winproj. Activator</span><span class="sxs-lookup"><span data-stu-id="1ee7d-196">WinProj.Activator</span></span></p></td>
<td align="left"><p><span data-ttu-id="1ee7d-197">Active X-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="1ee7d-197">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="1ee7d-198">Name. NameCtrl</span><span class="sxs-lookup"><span data-stu-id="1ee7d-198">Name.NameCtrl</span></span></p></td>
<td align="left"><p><span data-ttu-id="1ee7d-199">Active X-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="1ee7d-199">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="1ee7d-200">STSUPld. CopyCtl</span><span class="sxs-lookup"><span data-stu-id="1ee7d-200">STSUPld.CopyCtl</span></span></p></td>
<td align="left"><p><span data-ttu-id="1ee7d-201">Active X-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="1ee7d-201">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="1ee7d-202">CommunicatorMeetingJoinAx. joinmanager</span><span class="sxs-lookup"><span data-stu-id="1ee7d-202">CommunicatorMeetingJoinAx.JoinManager</span></span></p></td>
<td align="left"><p><span data-ttu-id="1ee7d-203">Active X-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="1ee7d-203">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="1ee7d-204">LISTNET. Listnet</span><span class="sxs-lookup"><span data-stu-id="1ee7d-204">LISTNET.Listnet</span></span></p></td>
<td align="left"><p><span data-ttu-id="1ee7d-205">Active X-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="1ee7d-205">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="1ee7d-206">OneDrive pro-Browser-Helfer</span><span class="sxs-lookup"><span data-stu-id="1ee7d-206">OneDrive Pro Browser Helper</span></span></p></td>
<td align="left"><p><span data-ttu-id="1ee7d-207">Active X-Steuerelement]</span><span class="sxs-lookup"><span data-stu-id="1ee7d-207">Active X Control]</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1ee7d-208">OneDrive pro-symbolüberlagerungen</span><span class="sxs-lookup"><span data-stu-id="1ee7d-208">OneDrive Pro Icon Overlays</span></span></p></td>
<td align="left"><p><span data-ttu-id="1ee7d-209">Windows Explorer-Shell-Symbol Overlays, wenn Benutzerordner OneDrive pro-Ordner anzeigen</span><span class="sxs-lookup"><span data-stu-id="1ee7d-209">Windows explorer shell icon overlays when users look at folders OneDrive Pro folders</span></span></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="1ee7d-210">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="1ee7d-210">Additional resources</span></span>


**<span data-ttu-id="1ee7d-211">Office 2013-App-V 5,0-Pakete 5,0 weitere Ressourcen</span><span class="sxs-lookup"><span data-stu-id="1ee7d-211">Office 2013 App-V 5.0 Packages 5.0 Additional Resources</span></span>**

[<span data-ttu-id="1ee7d-212">Unterstützte Szenarien für die Bereitstellung von Microsoft Office als sequenziertes App-V-Paket</span><span class="sxs-lookup"><span data-stu-id="1ee7d-212">Supported scenarios for deploying Microsoft Office as a sequenced App-V Package</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330680)

**<span data-ttu-id="1ee7d-213">Office 2010-App-V 5,0-Pakete</span><span class="sxs-lookup"><span data-stu-id="1ee7d-213">Office 2010 App-V 5.0 Packages</span></span>**

[<span data-ttu-id="1ee7d-214">Microsoft Office 2010-Sequenzierung-Kit für Microsoft Application Virtualization 5,0</span><span class="sxs-lookup"><span data-stu-id="1ee7d-214">Microsoft Office 2010 Sequencing Kit for Microsoft Application Virtualization 5.0</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330681)

[<span data-ttu-id="1ee7d-215">Bekannte Probleme beim Erstellen oder Verwenden eines App-V 5,0 Office 2010-Pakets</span><span class="sxs-lookup"><span data-stu-id="1ee7d-215">Known issues when you create or use an App-V 5.0 Office 2010 package</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330682)

[<span data-ttu-id="1ee7d-216">Sequenzierung von Microsoft Office 2010 in Microsoft Application Virtualization 5,0</span><span class="sxs-lookup"><span data-stu-id="1ee7d-216">How to sequence Microsoft Office 2010 in Microsoft Application Virtualization 5.0</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330676)

**<span data-ttu-id="1ee7d-217">Verbindungsgruppen</span><span class="sxs-lookup"><span data-stu-id="1ee7d-217">Connection Groups</span></span>**

[<span data-ttu-id="1ee7d-218">Bereitstellen von Verbindungsgruppen in Microsoft App-V V5</span><span class="sxs-lookup"><span data-stu-id="1ee7d-218">Deploying Connection Groups in Microsoft App-V v5</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330683)

[<span data-ttu-id="1ee7d-219">Verwalten von Verbindungsgruppen</span><span class="sxs-lookup"><span data-stu-id="1ee7d-219">Managing Connection Groups</span></span>](managing-connection-groups.md)

**<span data-ttu-id="1ee7d-220">Dynamische Konfiguration</span><span class="sxs-lookup"><span data-stu-id="1ee7d-220">Dynamic Configuration</span></span>**

[<span data-ttu-id="1ee7d-221">Informationen zur dynamischen Konfiguration in App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="1ee7d-221">About App-V 5.0 Dynamic Configuration</span></span>](about-app-v-50-dynamic-configuration.md)






 

 





