---
title: Von MED 1.0 unterstützte Konfigurationen
description: Von MED 1.0 unterstützte Konfigurationen
author: dansimp
ms.assetid: 74643de6-549e-4177-a559-6407e156ed3a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3b8ffdfb6e34fe7888ea5ace0ff7264bd978a548
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804355"
---
# <span data-ttu-id="ecb55-103">Von MED 1.0 unterstützte Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="ecb55-103">MED-V 1.0 Supported Configurations</span></span>


<span data-ttu-id="ecb55-104">In diesem Thema werden die Anforderungen beschrieben, die erforderlich sind, um Microsoft Enterprise Desktop Virtualization (MED-V) 1,0 in Ihrer Umgebung zu installieren und auszuführen.</span><span class="sxs-lookup"><span data-stu-id="ecb55-104">This topic specifies the requirements necessary to install and run Microsoft Enterprise Desktop Virtualization (MED-V) 1.0 in your environment.</span></span>

## <span data-ttu-id="ecb55-105">MED-V 1,0-Client System Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ecb55-105">MED-V 1.0 Client System Requirements</span></span>


### <span data-ttu-id="ecb55-106">Anforderungen des MED-V-Client-Betriebssystems</span><span class="sxs-lookup"><span data-stu-id="ecb55-106">MED-V Client Operating System Requirements</span></span>

<span data-ttu-id="ecb55-107">In der folgenden Tabelle sind die Betriebssysteme aufgeführt, die für die MED-V 1,0-Clientinstallation unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="ecb55-107">The following table lists the operating systems that are supported for MED-V 1.0 client installation.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ecb55-108">Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="ecb55-108">Operating System</span></span></th>
<th align="left"><span data-ttu-id="ecb55-109">Edition</span><span class="sxs-lookup"><span data-stu-id="ecb55-109">Edition</span></span></th>
<th align="left"><span data-ttu-id="ecb55-110">Service Pack</span><span class="sxs-lookup"><span data-stu-id="ecb55-110">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="ecb55-111">System Architektur</span><span class="sxs-lookup"><span data-stu-id="ecb55-111">System Architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ecb55-112">WindowsXP</span><span class="sxs-lookup"><span data-stu-id="ecb55-112">Windows XP</span></span></p></td>
<td align="left"><p><span data-ttu-id="ecb55-113">Professional Edition</span><span class="sxs-lookup"><span data-stu-id="ecb55-113">Professional Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="ecb55-114">SP2 oder SP3</span><span class="sxs-lookup"><span data-stu-id="ecb55-114">SP2 or SP3</span></span></p></td>
<td align="left"><p><span data-ttu-id="ecb55-115">x86</span><span class="sxs-lookup"><span data-stu-id="ecb55-115">x86</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ecb55-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ecb55-116">Windows Vista</span></span></p></td>
<td align="left"><p><span data-ttu-id="ecb55-117">Business-, Enterprise-oder Ultimate-Edition</span><span class="sxs-lookup"><span data-stu-id="ecb55-117">Business, Enterprise, or Ultimate Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="ecb55-118">SP1 oder SP2</span><span class="sxs-lookup"><span data-stu-id="ecb55-118">SP1 or SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="ecb55-119">x86</span><span class="sxs-lookup"><span data-stu-id="ecb55-119">x86</span></span></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="ecb55-120">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="ecb55-120">Note</span></span>**  
<span data-ttu-id="ecb55-121">Der MED-V-Client wird im systemeigenen x64-Modus nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ecb55-121">MED-V client does not run in native x64 mode.</span></span> <span data-ttu-id="ecb55-122">Stattdessen wird MED-V im Windows-64-Bit-Modus (WOW64) auf 64-Bit-Computern ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ecb55-122">Instead, MED-V runs in Windows on Windows 64-bit (WOW64) mode on 64-bit computers.</span></span>



### <a href="" id="med-v-1-0-client-configuration-"></a><span data-ttu-id="ecb55-123">MED-V 1,0-Client Konfiguration</span><span class="sxs-lookup"><span data-stu-id="ecb55-123">MED-V 1.0 Client Configuration</span></span>

**<span data-ttu-id="ecb55-124">.NET Framework-Version</span><span class="sxs-lookup"><span data-stu-id="ecb55-124">.NET Framework Version</span></span>**

<span data-ttu-id="ecb55-125">Die folgenden Versionen von Microsoft .NET Framework werden für die MED-V 1,0-Clientinstallation unterstützt:</span><span class="sxs-lookup"><span data-stu-id="ecb55-125">The following versions of the Microsoft .NET Framework are supported for MED-V 1.0 client installation:</span></span>

-   <span data-ttu-id="ecb55-126">.NET Framework 2,0 oder .NET Framework 2,0 SP1</span><span class="sxs-lookup"><span data-stu-id="ecb55-126">.NET Framework 2.0 or .NET Framework 2.0 SP1</span></span>

-   <span data-ttu-id="ecb55-127">.NET Framework 3,0 oder .NET Framework 3,0 SP1</span><span class="sxs-lookup"><span data-stu-id="ecb55-127">.NET Framework 3.0 or .NET Framework 3.0 SP1</span></span>

-   <span data-ttu-id="ecb55-128">.NET Framework 3,5 oder .NET Framework 3,5 SP1</span><span class="sxs-lookup"><span data-stu-id="ecb55-128">.NET Framework 3.5 or .NET Framework 3.5 SP1</span></span>

**<span data-ttu-id="ecb55-129">Virtualisierungs-Engine</span><span class="sxs-lookup"><span data-stu-id="ecb55-129">Virtualization Engine</span></span>**

<span data-ttu-id="ecb55-130">Microsoft Virtual PC 2007 SP1 mit dem Hotfix, der im Microsoft Knowledge Base-Artikel 974918 beschrieben wird, wird für die MED-V 1,0-Clientinstallation in den folgenden Konfigurationen unterstützt:</span><span class="sxs-lookup"><span data-stu-id="ecb55-130">Microsoft Virtual PC 2007 SP1 with the hotfix that is described in Microsoft Knowledge Base article 974918 is supported for MED-V 1.0 client installation in the following configurations:</span></span>

-   <span data-ttu-id="ecb55-131">Statische virtuelle Festplatte (VHD)-Datei</span><span class="sxs-lookup"><span data-stu-id="ecb55-131">Static Virtual Hard Disk (VHD) file</span></span>

-   <span data-ttu-id="ecb55-132">Mehrere VHD-Dateien, die sich im gleichen Verzeichnis befinden</span><span class="sxs-lookup"><span data-stu-id="ecb55-132">Multiple VHD files located within the same directory</span></span>

-   <span data-ttu-id="ecb55-133">Dynamische VHD-Datei</span><span class="sxs-lookup"><span data-stu-id="ecb55-133">Dynamic VHD file</span></span>

**<span data-ttu-id="ecb55-134">Internet Browser</span><span class="sxs-lookup"><span data-stu-id="ecb55-134">Internet Browser</span></span>**

<span data-ttu-id="ecb55-135">Windows Internet Explorer 7 und Windows Internet Explorer 8 werden für die MED-V 1,0-Clientinstallation unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ecb55-135">Windows Internet Explorer 7 and Windows Internet Explorer 8 are supported for MED-V 1.0 client installation.</span></span>

**<span data-ttu-id="ecb55-136">Microsoft Hyper-V Server</span><span class="sxs-lookup"><span data-stu-id="ecb55-136">Microsoft Hyper-V Server</span></span>**

<span data-ttu-id="ecb55-137">Der Med-v-Client wird in einer Microsoft Hyper-v-Server Umgebung nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ecb55-137">The MED-V client is not supported in a Microsoft Hyper-V server environment.</span></span>

## <span data-ttu-id="ecb55-138">System Anforderungen für MED-V 1,0-Arbeitsbereiche</span><span class="sxs-lookup"><span data-stu-id="ecb55-138">MED-V 1.0 Workspace System Requirements</span></span>


### <span data-ttu-id="ecb55-139">Betriebs System Anforderungen für den MED-V-Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="ecb55-139">MED-V Workspace Operating System Requirements</span></span>

<span data-ttu-id="ecb55-140">In der folgenden Tabelle sind die Betriebssysteme aufgeführt, die für MED-V 1,0-Arbeitsbereiche unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="ecb55-140">The following table lists the operating systems supported for MED-V 1.0 workspaces.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ecb55-141">Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="ecb55-141">Operating System</span></span></th>
<th align="left"><span data-ttu-id="ecb55-142">Edition</span><span class="sxs-lookup"><span data-stu-id="ecb55-142">Edition</span></span></th>
<th align="left"><span data-ttu-id="ecb55-143">Service Pack</span><span class="sxs-lookup"><span data-stu-id="ecb55-143">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="ecb55-144">System Architektur</span><span class="sxs-lookup"><span data-stu-id="ecb55-144">System Architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ecb55-145">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="ecb55-145">Windows 2000</span></span></p></td>
<td align="left"><p><span data-ttu-id="ecb55-146">Professional</span><span class="sxs-lookup"><span data-stu-id="ecb55-146">Professional</span></span></p></td>
<td align="left"><p><span data-ttu-id="ecb55-147">SP4</span><span class="sxs-lookup"><span data-stu-id="ecb55-147">SP4</span></span></p></td>
<td align="left"><p><span data-ttu-id="ecb55-148">X86</span><span class="sxs-lookup"><span data-stu-id="ecb55-148">X86</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ecb55-149">WindowsXP</span><span class="sxs-lookup"><span data-stu-id="ecb55-149">Windows XP</span></span></p></td>
<td align="left"><p><span data-ttu-id="ecb55-150">Professional Edition</span><span class="sxs-lookup"><span data-stu-id="ecb55-150">Professional Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="ecb55-151">SP2 oder SP3</span><span class="sxs-lookup"><span data-stu-id="ecb55-151">SP2 or SP3</span></span></p>
<div class="alert">
<strong><span data-ttu-id="ecb55-152">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="ecb55-152">Note</span></span></strong><br/><p><span data-ttu-id="ecb55-153">SP3 wird empfohlen, um sicherzustellen, dass der Med-v-Arbeitsbereich mit zukünftigen Versionen von Med-v kompatibel ist.</span><span class="sxs-lookup"><span data-stu-id="ecb55-153">SP3 is recommended to ensure that the MED-V workspace will be compatible with future versions of MED-V.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="ecb55-154">x86</span><span class="sxs-lookup"><span data-stu-id="ecb55-154">x86</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="med-v-1-0-workspace-configuration-"></a><span data-ttu-id="ecb55-155">MED-V 1,0 Workspace-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="ecb55-155">MED-V 1.0 Workspace Configuration</span></span>

**<span data-ttu-id="ecb55-156">.NET Framework-Version</span><span class="sxs-lookup"><span data-stu-id="ecb55-156">.NET Framework Version</span></span>**

<span data-ttu-id="ecb55-157">Für med-v ist eine der folgenden unterstützten Versionen der Microsoft .NET Framework für med-v 1,0 Workspace-Installation erforderlich:</span><span class="sxs-lookup"><span data-stu-id="ecb55-157">MED-V requires one of the following supported versions of the Microsoft .NET Framework for MED-V 1.0 workspace installation:</span></span>

-   <span data-ttu-id="ecb55-158">.NET Framework 2,0 SP1</span><span class="sxs-lookup"><span data-stu-id="ecb55-158">.NET Framework 2.0 SP1</span></span>

-   <span data-ttu-id="ecb55-159">.NET Framework 3,0 SP1</span><span class="sxs-lookup"><span data-stu-id="ecb55-159">.NET Framework 3.0 SP1</span></span>

-   <span data-ttu-id="ecb55-160">.NET Framework 3,5 oder .NET Framework 3,5 SP1</span><span class="sxs-lookup"><span data-stu-id="ecb55-160">.NET Framework 3.5 or .NET Framework 3.5 SP1</span></span>

**<span data-ttu-id="ecb55-161">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="ecb55-161">Note</span></span>**  
<span data-ttu-id="ecb55-162">.NET Framework 3,5 SP1 wird empfohlen, um sicherzustellen, dass der Med-v-Arbeitsbereich mit zukünftigen Versionen von Med-v kompatibel ist.</span><span class="sxs-lookup"><span data-stu-id="ecb55-162">.NET Framework 3.5 SP1 is recommended to ensure that the MED-V workspace will be compatible with future versions of MED-V.</span></span>



**<span data-ttu-id="ecb55-163">Internet Browser</span><span class="sxs-lookup"><span data-stu-id="ecb55-163">Internet Browser</span></span>**

<span data-ttu-id="ecb55-164">Windows Internet Explorer 6 SP2 und Windows Internet Explorer 7 werden für die MED-V 1,0 Workspace-Installation unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ecb55-164">Windows Internet Explorer 6 SP2 and Windows Internet Explorer 7 are supported for the MED-V 1.0 workspace installation.</span></span>

### <a href="" id="med-v-workspace-images-"></a><span data-ttu-id="ecb55-165">MED-V-Arbeitsbereichs Bilder</span><span class="sxs-lookup"><span data-stu-id="ecb55-165">MED-V Workspace Images</span></span>

<span data-ttu-id="ecb55-166">MED-V-Arbeitsbereichs Bilder müssen mithilfe von Virtual PC 2007 SP1 erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="ecb55-166">MED-V workspace images must be created by using Virtual PC 2007 SP1.</span></span>

## <span data-ttu-id="ecb55-167">MED-V 1,0-Server System Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ecb55-167">MED-V 1.0 Server System Requirements</span></span>


### <span data-ttu-id="ecb55-168">Anforderungen des MED-V 1,0 Server-Betriebssystems</span><span class="sxs-lookup"><span data-stu-id="ecb55-168">MED-V 1.0 Server Operating System Requirements</span></span>

<span data-ttu-id="ecb55-169">In der folgenden Tabelle sind die Betriebssysteme aufgeführt, die für MED-V 1,0-Server Installationen unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="ecb55-169">The following table lists the operating systems supported for MED-V 1.0 server installations.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ecb55-170">Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="ecb55-170">Operating System</span></span></th>
<th align="left"><span data-ttu-id="ecb55-171">Edition</span><span class="sxs-lookup"><span data-stu-id="ecb55-171">Edition</span></span></th>
<th align="left"><span data-ttu-id="ecb55-172">Service Pack</span><span class="sxs-lookup"><span data-stu-id="ecb55-172">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="ecb55-173">System Architektur</span><span class="sxs-lookup"><span data-stu-id="ecb55-173">System Architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ecb55-174">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ecb55-174">Windows Server 2008</span></span></p></td>
<td align="left"><p><span data-ttu-id="ecb55-175">Standard oder Enterprise</span><span class="sxs-lookup"><span data-stu-id="ecb55-175">Standard or Enterprise</span></span></p></td>
<td align="left"><p><span data-ttu-id="ecb55-176">Keine</span><span class="sxs-lookup"><span data-stu-id="ecb55-176">None</span></span></p></td>
<td align="left"><p><span data-ttu-id="ecb55-177">X86 oder x64</span><span class="sxs-lookup"><span data-stu-id="ecb55-177">X86 or x64</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="med-v-1-0-server-configuration-"></a><span data-ttu-id="ecb55-178">MED-V 1,0-Server Konfiguration</span><span class="sxs-lookup"><span data-stu-id="ecb55-178">MED-V 1.0 Server Configuration</span></span>

**<span data-ttu-id="ecb55-179">.NET Framework-Version</span><span class="sxs-lookup"><span data-stu-id="ecb55-179">.NET Framework Version</span></span>**

<span data-ttu-id="ecb55-180">Für med-v ist eine der folgenden unterstützten Versionen der Microsoft .NET Framework für med-v 1,0 Workspace-Installation erforderlich:</span><span class="sxs-lookup"><span data-stu-id="ecb55-180">MED-V requires one of the following supported versions of the Microsoft .NET Framework for MED-V 1.0 workspace installation:</span></span>

-   <span data-ttu-id="ecb55-181">.NET Framework 2,0 oder .NET Framework 2,0 SP1</span><span class="sxs-lookup"><span data-stu-id="ecb55-181">.NET Framework 2.0 or .NET Framework 2.0 SP1</span></span>

-   <span data-ttu-id="ecb55-182">.NET Framework 3,0 oder .NET Framework 3,0 SP1</span><span class="sxs-lookup"><span data-stu-id="ecb55-182">.NET Framework 3.0 or .NET Framework 3.0 SP1</span></span>

-   <span data-ttu-id="ecb55-183">.NET Framework 3,5 oder .NET Framework 3,5 SP1</span><span class="sxs-lookup"><span data-stu-id="ecb55-183">.NET Framework 3.5 or .NET Framework 3.5 SP1</span></span>

**<span data-ttu-id="ecb55-184">Microsoft SQL Server-Version</span><span class="sxs-lookup"><span data-stu-id="ecb55-184">Microsoft SQL Server Version</span></span>**

<span data-ttu-id="ecb55-185">Die folgenden Versionen von Microsoft SQL Server werden für med-v 1,0 unterstützt, wenn SQL Server lokal oder Remote vom Med-v 1,0-Server installiert wird:</span><span class="sxs-lookup"><span data-stu-id="ecb55-185">The following versions of Microsoft SQL Server are supported for MED-V 1.0 when SQL Server is installed locally or remotely from the MED-V 1.0 Server:</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ecb55-186">SQL Server-Version</span><span class="sxs-lookup"><span data-stu-id="ecb55-186">SQL Server Version</span></span></th>
<th align="left"><span data-ttu-id="ecb55-187">Edition</span><span class="sxs-lookup"><span data-stu-id="ecb55-187">Edition</span></span></th>
<th align="left"><span data-ttu-id="ecb55-188">Service Pack</span><span class="sxs-lookup"><span data-stu-id="ecb55-188">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="ecb55-189">System Architektur</span><span class="sxs-lookup"><span data-stu-id="ecb55-189">System Architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ecb55-190">SQL Server 2005</span><span class="sxs-lookup"><span data-stu-id="ecb55-190">SQL Server 2005</span></span></p></td>
<td align="left"><p><span data-ttu-id="ecb55-191">Express-, Standard-oder Enterprise-Edition</span><span class="sxs-lookup"><span data-stu-id="ecb55-191">Express, Standard, or Enterprise Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="ecb55-192">SP2</span><span class="sxs-lookup"><span data-stu-id="ecb55-192">SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="ecb55-193">X86 oder x64</span><span class="sxs-lookup"><span data-stu-id="ecb55-193">X86 or x64</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ecb55-194">SQL Server 2008</span><span class="sxs-lookup"><span data-stu-id="ecb55-194">SQL Server 2008</span></span></p></td>
<td align="left"><p><span data-ttu-id="ecb55-195">Express, Standard oder Enterprise</span><span class="sxs-lookup"><span data-stu-id="ecb55-195">Express, Standard, or Enterprise</span></span></p></td>
<td align="left"><p><span data-ttu-id="ecb55-196">Keine</span><span class="sxs-lookup"><span data-stu-id="ecb55-196">None</span></span></p></td>
<td align="left"><p><span data-ttu-id="ecb55-197">X86 oder x64</span><span class="sxs-lookup"><span data-stu-id="ecb55-197">X86 or x64</span></span></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="ecb55-198">Microsoft Hyper-V Server</span><span class="sxs-lookup"><span data-stu-id="ecb55-198">Microsoft Hyper-V Server</span></span>**

<span data-ttu-id="ecb55-199">Der Med-v-Server wird in einer Microsoft Hyper-v-Server Umgebung unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ecb55-199">The MED-V server is supported in a Microsoft Hyper-V server environment.</span></span>

## <span data-ttu-id="ecb55-200">MED-V 1,0-Globalisierungsinformationen</span><span class="sxs-lookup"><span data-stu-id="ecb55-200">MED-V 1.0 Globalization Information</span></span>


<span data-ttu-id="ecb55-201">Obwohl Med-v nicht in anderen Sprachen als Englisch verfügbar ist, werden die folgenden Sprachversionen des Windows-Betriebssystems für die Med-v 1,0-Client-, Workspace-und Server Installationen unterstützt:</span><span class="sxs-lookup"><span data-stu-id="ecb55-201">Although MED-V is not released in languages other than English, the following Windows operating system language versions are supported for the MED-V 1.0 client, workspace, and server installations:</span></span>

-   <span data-ttu-id="ecb55-202">Englisch</span><span class="sxs-lookup"><span data-stu-id="ecb55-202">English</span></span>

-   <span data-ttu-id="ecb55-203">Französisch</span><span class="sxs-lookup"><span data-stu-id="ecb55-203">French</span></span>

-   <span data-ttu-id="ecb55-204">Deutsch</span><span class="sxs-lookup"><span data-stu-id="ecb55-204">German</span></span>

-   <span data-ttu-id="ecb55-205">Italienisch</span><span class="sxs-lookup"><span data-stu-id="ecb55-205">Italian</span></span>

-   <span data-ttu-id="ecb55-206">Spanisch</span><span class="sxs-lookup"><span data-stu-id="ecb55-206">Spanish</span></span>

-   <span data-ttu-id="ecb55-207">Portugiesisch (Brasilien)</span><span class="sxs-lookup"><span data-stu-id="ecb55-207">Portuguese (Brazil)</span></span>









