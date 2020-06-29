---
title: So laden Sie die PowerShell-Cmdlets und rufen die Cmdlet-Hilfe auf
description: So laden Sie die PowerShell-Cmdlets und rufen die Cmdlet-Hilfe auf
author: dansimp
ms.assetid: 0624495b-943e-485b-9e54-b50e4ee6591c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/02/2016
ms.openlocfilehash: 7692d3e36aabc4f3142f664e94d9d71b2cfc1bd3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805366"
---
# <span data-ttu-id="6449c-103">So laden Sie die PowerShell-Cmdlets und rufen die Cmdlet-Hilfe auf</span><span class="sxs-lookup"><span data-stu-id="6449c-103">How to Load the PowerShell Cmdlets and Get Cmdlet Help</span></span>


<span data-ttu-id="6449c-104">Inhalt dieses Themas:</span><span class="sxs-lookup"><span data-stu-id="6449c-104">What this topic covers:</span></span>

-   [<span data-ttu-id="6449c-105">Voraussetzungen für die Verwendung von PowerShell-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="6449c-105">Requirements for using PowerShell cmdlets</span></span>](#bkmk-reqs-using-posh)

-   [<span data-ttu-id="6449c-106">Laden der PowerShell-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="6449c-106">Loading the PowerShell cmdlets</span></span>](#bkmk-load-cmdlets)

-   [<span data-ttu-id="6449c-107">Aufrufen von Hilfe zu den PowerShell-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="6449c-107">Getting help for the PowerShell cmdlets</span></span>](#bkmk-get-cmdlet-help)

-   [<span data-ttu-id="6449c-108">Anzeigen der Hilfe zu einem PowerShell-Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6449c-108">Displaying the help for a PowerShell cmdlet</span></span>](#bkmk-display-help-cmdlet)

## <a href="" id="bkmk-reqs-using-posh"></a><span data-ttu-id="6449c-109">Voraussetzungen für die Verwendung von PowerShell-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="6449c-109">Requirements for using PowerShell cmdlets</span></span>


<span data-ttu-id="6449c-110">Überprüfen Sie die folgenden Voraussetzungen für die Verwendung der App-V PowerShell-Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="6449c-110">Review the following requirements for using the App-V PowerShell cmdlets:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="6449c-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6449c-111">Requirement</span></span></th>
<th align="left"><span data-ttu-id="6449c-112">Details</span><span class="sxs-lookup"><span data-stu-id="6449c-112">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6449c-113">Benutzer können App-V Server-Cmdlets nur ausführen, wenn Sie Ihnen Zugriff gewähren, indem Sie eine der folgenden Methoden verwenden:</span><span class="sxs-lookup"><span data-stu-id="6449c-113">Users can run App-V Server cmdlets only if you grant them access by using one of the following methods:</span></span></p></td>
<td align="left"><ul>
<li><p><strong><span data-ttu-id="6449c-114">Wenn Sie den App-V-Server bereitstellen und konfigurieren </strong> :</span><span class="sxs-lookup"><span data-stu-id="6449c-114">When you are deploying and configuring the App-V Server</strong>:</span></span></p>
<p><span data-ttu-id="6449c-115">Geben Sie eine Active Directory-Gruppe oder einen einzelnen Benutzer an, der über die Berechtigungen zum Verwalten der App-V-Umgebung verfügt.</span><span class="sxs-lookup"><span data-stu-id="6449c-115">Specify an Active Directory group or individual user that has permissions to manage the App-V environment.</span></span> <span data-ttu-id="6449c-116">Hier erfahren Sie <a href="how-to-deploy-the-app-v-50-server-50sp3.md" data-raw-source="[How to Deploy the App-V 5.0 Server](how-to-deploy-the-app-v-50-server-50sp3.md)"> , wie der App-V 5,0-Server bereitgestellt wird </a> .</span><span class="sxs-lookup"><span data-stu-id="6449c-116">See <a href="how-to-deploy-the-app-v-50-server-50sp3.md" data-raw-source="[How to Deploy the App-V 5.0 Server](how-to-deploy-the-app-v-50-server-50sp3.md)">How to Deploy the App-V 5.0 Server</a>.</span></span></p></li>
<li><p><strong><span data-ttu-id="6449c-117">Nachdem Sie den App-V-Server bereitgestellt haben </strong> :</span><span class="sxs-lookup"><span data-stu-id="6449c-117">After you’ve deployed the App-V Server</strong>:</span></span></p>
<p><span data-ttu-id="6449c-118">Verwenden Sie die App-V-Verwaltungskonsole, um eine zusätzliche Active Directory-Gruppe oder einen weiteren Benutzer hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="6449c-118">Use the App-V Management console to add an additional Active Directory group or user.</span></span> <span data-ttu-id="6449c-119">Informationen dazu finden Sie unter <a href="how-to-add-or-remove-an-administrator-by-using-the-management-console.md" data-raw-source="[How to Add or Remove an Administrator by Using the Management Console](how-to-add-or-remove-an-administrator-by-using-the-management-console.md)"> Hinzufügen oder Entfernen eines Administrators mithilfe der Verwaltungskonsole </a> .</span><span class="sxs-lookup"><span data-stu-id="6449c-119">See <a href="how-to-add-or-remove-an-administrator-by-using-the-management-console.md" data-raw-source="[How to Add or Remove an Administrator by Using the Management Console](how-to-add-or-remove-an-administrator-by-using-the-management-console.md)">How to Add or Remove an Administrator by Using the Management Console</a>.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6449c-120">Cmdlets, die eine Eingabeaufforderung mit erhöhten Rechten erfordern</span><span class="sxs-lookup"><span data-stu-id="6449c-120">Cmdlets that require an elevated command prompt</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="6449c-121">Add-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="6449c-121">Add-AppvClientPackage</span></span></p></li>
<li><p><span data-ttu-id="6449c-122">Remove-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="6449c-122">Remove-AppvClientPackage</span></span></p></li>
<li><p><span data-ttu-id="6449c-123">Satz-AppvClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="6449c-123">Set-AppvClientConfiguration</span></span></p></li>
<li><p><span data-ttu-id="6449c-124">Add-AppvClientConnectionGroup</span><span class="sxs-lookup"><span data-stu-id="6449c-124">Add-AppvClientConnectionGroup</span></span></p></li>
<li><p><span data-ttu-id="6449c-125">Remove-AppvClientConnectionGroup</span><span class="sxs-lookup"><span data-stu-id="6449c-125">Remove-AppvClientConnectionGroup</span></span></p></li>
<li><p><span data-ttu-id="6449c-126">Add-AppvPublishingServer</span><span class="sxs-lookup"><span data-stu-id="6449c-126">Add-AppvPublishingServer</span></span></p></li>
<li><p><span data-ttu-id="6449c-127">Remove-AppvPublishingServer</span><span class="sxs-lookup"><span data-stu-id="6449c-127">Remove-AppvPublishingServer</span></span></p></li>
<li><p><span data-ttu-id="6449c-128">Senden-AppvClientReport</span><span class="sxs-lookup"><span data-stu-id="6449c-128">Send-AppvClientReport</span></span></p></li>
<li><p><span data-ttu-id="6449c-129">Satz-AppvClientMode</span><span class="sxs-lookup"><span data-stu-id="6449c-129">Set-AppvClientMode</span></span></p></li>
<li><p><span data-ttu-id="6449c-130">Satz-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="6449c-130">Set-AppvClientPackage</span></span></p></li>
<li><p><span data-ttu-id="6449c-131">Satz-AppvPublishingServer</span><span class="sxs-lookup"><span data-stu-id="6449c-131">Set-AppvPublishingServer</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6449c-132">Cmdlets, die Endbenutzer ausführen können, es sei denn, Sie konfigurieren Sie so, dass eine Eingabeaufforderung mit erhöhten Rechten erforderlich ist</span><span class="sxs-lookup"><span data-stu-id="6449c-132">Cmdlets that end users can run, unless you configure them to require an elevated command prompt</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="6449c-133">Publish-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="6449c-133">Publish-AppvClientPackage</span></span></p></li>
<li><p><span data-ttu-id="6449c-134">Veröffentlichung aufheben – AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="6449c-134">Unpublish-AppvClientPackage</span></span></p></li>
</ul>
<p><span data-ttu-id="6449c-135">Verwenden Sie eine der folgenden Methoden, um diese Cmdlets so zu konfigurieren, dass eine Eingabeaufforderung mit erhöhten Rechten erforderlich ist:</span><span class="sxs-lookup"><span data-stu-id="6449c-135">To configure these cmdlets to require an elevated command prompt, use one of the following methods:</span></span></p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="6449c-136">Methode</span><span class="sxs-lookup"><span data-stu-id="6449c-136">Method</span></span></th>
<th align="left"><span data-ttu-id="6449c-137">Weitere Ressourcen</span><span class="sxs-lookup"><span data-stu-id="6449c-137">More resources</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6449c-138">Führen Sie das <strong> Cmdlet "Satz-AppvClientConfiguration </strong> " mit dem <strong> -RequirePublishAsAdmin- </strong> Parameter aus.</span><span class="sxs-lookup"><span data-stu-id="6449c-138">Run the <strong>Set-AppvClientConfiguration</strong> cmdlet with the <strong>-RequirePublishAsAdmin</strong> parameter.</span></span></p></td>
<td align="left"><ul>
<li><p><a href="how-to-manage-connection-groups-on-a-stand-alone-computer-by-using-powershell.md#bkmk-admin-only-posh-topic-cg" data-raw-source="[How to Manage Connection Groups on a Stand-alone Computer by Using PowerShell](how-to-manage-connection-groups-on-a-stand-alone-computer-by-using-powershell.md#bkmk-admin-only-posh-topic-cg)"><span data-ttu-id="6449c-139">So verwalten Sie Verbindungsgruppen auf einem eigenständigen Computer mithilfe von PowerShell</span><span class="sxs-lookup"><span data-stu-id="6449c-139">How to Manage Connection Groups on a Stand-alone Computer by Using PowerShell</span></span></a></p></li>
<li><p><a href="how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md" data-raw-source="[How to Manage App-V 5.0 Packages Running on a Stand-Alone Computer by Using PowerShell](how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md)"><span data-ttu-id="6449c-140">So verwalten Sie App-V 5.0-Pakete auf einem eigenständigen Computer mithilfe von PowerShell</span><span class="sxs-lookup"><span data-stu-id="6449c-140">How to Manage App-V 5.0 Packages Running on a Stand-Alone Computer by Using PowerShell</span></span></a></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6449c-141">Aktivieren Sie die Gruppenrichtlinieneinstellung "als Administrator veröffentlichen" für App-V-Clients.</span><span class="sxs-lookup"><span data-stu-id="6449c-141">Enable the “Require publish as administrator” Group Policy setting for App-V Clients.</span></span></p></td>
<td align="left"><p><a href="how-to-publish-a-package-by-using-the-management-console-50.md" data-raw-source="[How to Publish a Package by Using the Management Console](how-to-publish-a-package-by-using-the-management-console-50.md)"><span data-ttu-id="6449c-142">So veröffentlichen Sie mithilfe der Verwaltungskonsole ein Paket</span><span class="sxs-lookup"><span data-stu-id="6449c-142">How to Publish a Package by Using the Management Console</span></span></a> </p></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-load-cmdlets"></a><span data-ttu-id="6449c-143">Laden der PowerShell-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="6449c-143">Loading the PowerShell cmdlets</span></span>
<span data-ttu-id="6449c-144">So laden Sie die PowerShell-Cmdlet-Module:</span><span class="sxs-lookup"><span data-stu-id="6449c-144">To load the PowerShell cmdlet modules:</span></span>

1.  <span data-ttu-id="6449c-145">Öffnen Sie Windows PowerShell oder Windows PowerShell Integrated Scripting Environment (ISE).</span><span class="sxs-lookup"><span data-stu-id="6449c-145">Open Windows PowerShell or Windows PowerShell Integrated Scripting Environment (ISE).</span></span>

2.  <span data-ttu-id="6449c-146">Geben Sie einen der folgenden Befehle ein, um die Cmdlets für das gewünschte Modul zu laden:</span><span class="sxs-lookup"><span data-stu-id="6449c-146">Type one of the following commands to load the cmdlets for the module you want:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="6449c-147">App-V-Komponente</span><span class="sxs-lookup"><span data-stu-id="6449c-147">App-V component</span></span></th>
<th align="left"><span data-ttu-id="6449c-148">Befehl zum eingeben</span><span class="sxs-lookup"><span data-stu-id="6449c-148">Command to type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6449c-149">App-V-Server</span><span class="sxs-lookup"><span data-stu-id="6449c-149">App-V Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="6449c-150">Import-Modul AppvServer</span><span class="sxs-lookup"><span data-stu-id="6449c-150">Import-Module AppvServer</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6449c-151">App-V-Sequenzer</span><span class="sxs-lookup"><span data-stu-id="6449c-151">App-V Sequencer</span></span></p></td>
<td align="left"><p><span data-ttu-id="6449c-152">Import-Modul AppvSequencer</span><span class="sxs-lookup"><span data-stu-id="6449c-152">Import-Module AppvSequencer</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6449c-153">App-V-Client</span><span class="sxs-lookup"><span data-stu-id="6449c-153">App-V Client</span></span></p></td>
<td align="left"><p><span data-ttu-id="6449c-154">Import-Modul AppvClient</span><span class="sxs-lookup"><span data-stu-id="6449c-154">Import-Module AppvClient</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-get-cmdlet-help"></a><span data-ttu-id="6449c-155">Aufrufen von Hilfe zu den PowerShell-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="6449c-155">Getting help for the PowerShell cmdlets</span></span>
<span data-ttu-id="6449c-156">Ab App-V 5,0 SP3 steht die Hilfe für das Cmdlet in zwei Formaten zur Verfügung:</span><span class="sxs-lookup"><span data-stu-id="6449c-156">Starting in App-V 5.0 SP3, cmdlet help is available in two formats:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="6449c-157">Format</span><span class="sxs-lookup"><span data-stu-id="6449c-157">Format</span></span></th>
<th align="left"><span data-ttu-id="6449c-158">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6449c-158">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6449c-159">Als herunterladbares Modul</span><span class="sxs-lookup"><span data-stu-id="6449c-159">As a downloadable module</span></span></p></td>
<td align="left"><p><span data-ttu-id="6449c-160">So laden Sie die neueste Hilfe herunter, nachdem Sie das Cmdlet-Modul heruntergeladen haben:</span><span class="sxs-lookup"><span data-stu-id="6449c-160">To download the latest help after downloading the cmdlet module:</span></span></p>
<ol>
<li><p><span data-ttu-id="6449c-161">Öffnen Sie Windows PowerShell oder Windows PowerShell Integrated Scripting Environment (ISE).</span><span class="sxs-lookup"><span data-stu-id="6449c-161">Open Windows PowerShell or Windows PowerShell Integrated Scripting Environment (ISE).</span></span></p></li>
<li><p><span data-ttu-id="6449c-162">Geben Sie einen der folgenden Befehle ein, um die Cmdlets für das gewünschte Modul zu laden:</span><span class="sxs-lookup"><span data-stu-id="6449c-162">Type one of the following commands to load the cmdlets for the module you want:</span></span></p></li>
</ol>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="6449c-163">App-V-Komponente</span><span class="sxs-lookup"><span data-stu-id="6449c-163">App-V component</span></span></th>
<th align="left"><span data-ttu-id="6449c-164">Befehl zum eingeben</span><span class="sxs-lookup"><span data-stu-id="6449c-164">Command to type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6449c-165">App-V-Server</span><span class="sxs-lookup"><span data-stu-id="6449c-165">App-V Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="6449c-166">Update-Hilfe-Modul AppvServer</span><span class="sxs-lookup"><span data-stu-id="6449c-166">Update-Help -Module AppvServer</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6449c-167">App-V-Sequenzer</span><span class="sxs-lookup"><span data-stu-id="6449c-167">App-V Sequencer</span></span></p></td>
<td align="left"><p><span data-ttu-id="6449c-168">Update-Hilfe-Modul AppvSequencer</span><span class="sxs-lookup"><span data-stu-id="6449c-168">Update-Help -Module AppvSequencer</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6449c-169">App-V-Client</span><span class="sxs-lookup"><span data-stu-id="6449c-169">App-V Client</span></span></p></td>
<td align="left"><p><span data-ttu-id="6449c-170">Update-Hilfe-Modul AppvClient</span><span class="sxs-lookup"><span data-stu-id="6449c-170">Update-Help -Module AppvClient</span></span></p></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6449c-171">Auf TechNet als Web-Seiten</span><span class="sxs-lookup"><span data-stu-id="6449c-171">On TechNet as web pages</span></span></p></td>
<td align="left"><p><span data-ttu-id="6449c-172">Weitere Informationen finden Sie unter App-V-Knoten unter <a href="https://technet.microsoft.com/library/dn520245.aspx" data-raw-source="[Microsoft Desktop Optimization Pack Automation with Windows PowerShell](https://technet.microsoft.com/library/dn520245.aspx)"> Microsoft Desktop Optimization Pack-Automatisierung mit Windows PowerShell </a> .</span><span class="sxs-lookup"><span data-stu-id="6449c-172">See the App-V node under <a href="https://technet.microsoft.com/library/dn520245.aspx" data-raw-source="[Microsoft Desktop Optimization Pack Automation with Windows PowerShell](https://technet.microsoft.com/library/dn520245.aspx)">Microsoft Desktop Optimization Pack Automation with Windows PowerShell</a>.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-display-help-cmdlet"></a><span data-ttu-id="6449c-173">Anzeigen der Hilfe zu einem PowerShell-Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6449c-173">Displaying the help for a PowerShell cmdlet</span></span>
<span data-ttu-id="6449c-174">So zeigen Sie Hilfe zu einem bestimmten PowerShell-Cmdlet an:</span><span class="sxs-lookup"><span data-stu-id="6449c-174">To display help for a specific PowerShell cmdlet:</span></span>

1.  <span data-ttu-id="6449c-175">Öffnen Sie Windows PowerShell oder Windows PowerShell Integrated Scripting Environment (ISE).</span><span class="sxs-lookup"><span data-stu-id="6449c-175">Open Windows PowerShell or Windows PowerShell Integrated Scripting Environment (ISE).</span></span>

2.  <span data-ttu-id="6449c-176">Geben **Sie Get-Help-** &lt; *Cmdlet*ein &gt; , beispielsweise **Get-Help Publish-AppvClientPackage**.</span><span class="sxs-lookup"><span data-stu-id="6449c-176">Type **Get-Help** &lt;*cmdlet*&gt;, for example, **Get-Help Publish-AppvClientPackage**.</span></span>

<span data-ttu-id="6449c-177">Sie **haben einen Vorschlag für App-V**?</span><span class="sxs-lookup"><span data-stu-id="6449c-177">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="6449c-178">[Hier](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)können Sie Vorschläge hinzufügen oder abstimmen.</span><span class="sxs-lookup"><span data-stu-id="6449c-178">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> <span data-ttu-id="6449c-179">Sie **haben ein App-V-Problem**?</span><span class="sxs-lookup"><span data-stu-id="6449c-179">**Got an App-V issue**?</span></span> <span data-ttu-id="6449c-180">Verwenden Sie das [App-V TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="6449c-180">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

 

 





