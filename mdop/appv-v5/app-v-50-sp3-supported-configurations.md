---
title: Unterstützte App-V 5.0 SP3-Konfigurationen
description: Unterstützte App-V 5.0 SP3-Konfigurationen
author: dansimp
ms.assetid: 08ced79a-0ed3-43c3-82e7-de01c1f33e81
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: b5a8858c703add3dc84c7eed4f62aa97e60ec9b0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805993"
---
# <span data-ttu-id="7dc0b-103">Unterstützte App-V 5.0 SP3-Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="7dc0b-103">App-V 5.0 SP3 Supported Configurations</span></span>


<span data-ttu-id="7dc0b-104">In diesem Thema werden die Anforderungen zum Installieren und Ausführen von Microsoft Application Virtualization (App-V) 5,0 SP3 in Ihrer Umgebung angegeben.</span><span class="sxs-lookup"><span data-stu-id="7dc0b-104">This topic specifies the requirements to install and run Microsoft Application Virtualization (App-V) 5.0 SP3 in your environment.</span></span>

## <span data-ttu-id="7dc0b-105">Systemanforderungen für App-V Server</span><span class="sxs-lookup"><span data-stu-id="7dc0b-105">App-V Server system requirements</span></span>


<span data-ttu-id="7dc0b-106">In diesem Abschnitt werden die Betriebssystem-und Hardwareanforderungen für alle App-V-Server Komponenten aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="7dc0b-106">This section lists the operating system and hardware requirements for all of the App-V Server components.</span></span>

### <span data-ttu-id="7dc0b-107">Nicht unterstützte App-V 5,0 SP3-Server Szenarien</span><span class="sxs-lookup"><span data-stu-id="7dc0b-107">Unsupported App-V 5.0 SP3 Server scenarios</span></span>

<span data-ttu-id="7dc0b-108">Der App-V 5,0 SP3-Server unterstützt die folgenden Szenarien nicht:</span><span class="sxs-lookup"><span data-stu-id="7dc0b-108">The App-V 5.0 SP3 Server does not support the following scenarios:</span></span>

-   <span data-ttu-id="7dc0b-109">Bereitstellung auf einem Computer, auf dem Microsoft Windows Server Core ausgeführt wird</span><span class="sxs-lookup"><span data-stu-id="7dc0b-109">Deployment to a computer that runs Microsoft Windows Server Core.</span></span>

-   <span data-ttu-id="7dc0b-110">Bereitstellung auf einem Computer, auf dem eine frühere Version der App-V 5,0 SP3-Server Komponenten ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7dc0b-110">Deployment to a computer that runs a previous version of App-V 5.0 SP3 Server components.</span></span> <span data-ttu-id="7dc0b-111">Sie können APP-v 5,0 SP3 nebeneinander mit dem App-v 4.5 Lightweight Streaming Server (LWS)-Server installieren.</span><span class="sxs-lookup"><span data-stu-id="7dc0b-111">You can install App-V 5.0 SP3 side by side with the App-V4.5 Lightweight Streaming Server (LWS) server only.</span></span> <span data-ttu-id="7dc0b-112">Die Bereitstellung von App-v nebeneinander mit dem App-v 4,5 Application Virtualization Management Service (HWS)-Server wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7dc0b-112">Deployment of App-V side by side with the App-V 4.5 Application Virtualization Management Service (HWS) server is not supported.</span></span>

-   <span data-ttu-id="7dc0b-113">Bereitstellung auf einem Computer, auf dem Microsoft SQL Server Express Edition ausgeführt wird</span><span class="sxs-lookup"><span data-stu-id="7dc0b-113">Deployment to a computer that runs Microsoft SQL Server Express edition.</span></span>

-   <span data-ttu-id="7dc0b-114">Remote Bereitstellung der Verwaltungsserver-Datenbank oder der Berichtsdatenbank</span><span class="sxs-lookup"><span data-stu-id="7dc0b-114">Remote deployment of the management server database or the reporting database.</span></span> <span data-ttu-id="7dc0b-115">Sie müssen das Installationsprogramm direkt auf dem Computer ausführen, auf dem Microsoft SQL Server ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7dc0b-115">You must run the installer directly on the computer that is running Microsoft SQL Server.</span></span>

-   <span data-ttu-id="7dc0b-116">Bereitstellung auf einem Domänencontroller.</span><span class="sxs-lookup"><span data-stu-id="7dc0b-116">Deployment to a domain controller.</span></span>

-   <span data-ttu-id="7dc0b-117">Kurze Pfade.</span><span class="sxs-lookup"><span data-stu-id="7dc0b-117">Short paths.</span></span> <span data-ttu-id="7dc0b-118">Wenn Sie einen kurzen Pfad verwenden möchten, müssen Sie einen neuen Datenträger erstellen.</span><span class="sxs-lookup"><span data-stu-id="7dc0b-118">If you plan to use a short path, you must create a new volume.</span></span>

### <span data-ttu-id="7dc0b-119">Betriebssystemanforderungen für Management Server</span><span class="sxs-lookup"><span data-stu-id="7dc0b-119">Management server operating system requirements</span></span>

<span data-ttu-id="7dc0b-120">In der folgenden Tabelle sind die Betriebssysteme aufgeführt, die für die Installation des App-V 5,0 SP3-Verwaltungsservers unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="7dc0b-120">The following table lists the operating systems that are supported for the App-V 5.0 SP3 Management server installation.</span></span>

<span data-ttu-id="7dc0b-121">**Hinweis**  Microsoft bietet Unterstützung für das aktuelle Service Pack und in einigen Fällen das unmittelbar vorhergehende Service Pack.</span><span class="sxs-lookup"><span data-stu-id="7dc0b-121">**Note** Microsoft provides support for the current service pack and, in some cases, the immediately preceding service pack.</span></span> <span data-ttu-id="7dc0b-122">Informationen zu den Support Zeitachsen für Ihr Produkt finden Sie unter [unterstützte Service Packs für Lebenszyklen](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span><span class="sxs-lookup"><span data-stu-id="7dc0b-122">To find the support timelines for your product, see the [Lifecycle Supported Service Packs](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span></span> <span data-ttu-id="7dc0b-123">Weitere Informationen finden Sie unter [Supportrichtlinien für Microsoft Support-Lebenszyklus](https://go.microsoft.com/fwlink/p/?LinkId=31976) .</span><span class="sxs-lookup"><span data-stu-id="7dc0b-123">See [Microsoft Support Lifecycle Support Policy FAQ](https://go.microsoft.com/fwlink/p/?LinkId=31976) for more information.</span></span>

 

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="7dc0b-124">Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="7dc0b-124">Operating system</span></span></th>
<th align="left"><span data-ttu-id="7dc0b-125">Service Pack</span><span class="sxs-lookup"><span data-stu-id="7dc0b-125">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="7dc0b-126">System Architektur</span><span class="sxs-lookup"><span data-stu-id="7dc0b-126">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7dc0b-127">Microsoft Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="7dc0b-127">Microsoft Windows Server 2012 R2</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="7dc0b-128">64Bit</span><span class="sxs-lookup"><span data-stu-id="7dc0b-128">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7dc0b-129">Microsoft Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7dc0b-129">Microsoft Windows Server 2012</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="7dc0b-130">64Bit</span><span class="sxs-lookup"><span data-stu-id="7dc0b-130">64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7dc0b-131">Microsoft Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7dc0b-131">Microsoft Windows Server 2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="7dc0b-132">SP1</span><span class="sxs-lookup"><span data-stu-id="7dc0b-132">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="7dc0b-133">64Bit</span><span class="sxs-lookup"><span data-stu-id="7dc0b-133">64-bit</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="7dc0b-134">**Wichtig**  Die Bereitstellung der Verwaltungsserverrolle auf einem Computer mit aktivierter Remote Desktop Freigabe (RDS) wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7dc0b-134">**Important** Deployment of the Management server role to a computer with Remote Desktop Sharing (RDS) enabled is not supported.</span></span>

 

### <a href="" id="management-server-hardware-requirements-"></a><span data-ttu-id="7dc0b-135">Hardwareanforderungen für den Verwaltungsserver</span><span class="sxs-lookup"><span data-stu-id="7dc0b-135">Management server hardware requirements</span></span>

-   <span data-ttu-id="7dc0b-136">Prozessor – 1,4 GHz oder schneller, 64-Bit (x64)-Prozessor</span><span class="sxs-lookup"><span data-stu-id="7dc0b-136">Processor—1.4 GHz or faster, 64-bit (x64) processor</span></span>

-   <span data-ttu-id="7dc0b-137">RAM – 1 GB RAM (64-Bit)</span><span class="sxs-lookup"><span data-stu-id="7dc0b-137">RAM—1 GB RAM (64-bit)</span></span>

-   <span data-ttu-id="7dc0b-138">Speicherplatz – 200 MB verfügbarer Festplattenspeicherplatz, nicht einschließlich des Inhaltsverzeichnisses</span><span class="sxs-lookup"><span data-stu-id="7dc0b-138">Disk space—200 MB available hard disk space, not including the content directory</span></span>

### <span data-ttu-id="7dc0b-139">Verwaltungsserver-Datenbankanforderungen</span><span class="sxs-lookup"><span data-stu-id="7dc0b-139">Management server database requirements</span></span>

<span data-ttu-id="7dc0b-140">In der folgenden Tabelle sind die SQL Server-Versionen aufgeführt, die für die Installation der App-V 5,0 SP3-Verwaltungsdatenbank unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="7dc0b-140">The following table lists the SQL Server versions that are supported for the App-V 5.0 SP3 Management database installation.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="7dc0b-141">SQL Server-Version</span><span class="sxs-lookup"><span data-stu-id="7dc0b-141">SQL Server version</span></span></th>
<th align="left"><span data-ttu-id="7dc0b-142">Service Pack</span><span class="sxs-lookup"><span data-stu-id="7dc0b-142">Service pack</span></span></th>
<th align="left"><span data-ttu-id="7dc0b-143">System Architektur</span><span class="sxs-lookup"><span data-stu-id="7dc0b-143">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7dc0b-144">Microsoft SQL Server 2014</span><span class="sxs-lookup"><span data-stu-id="7dc0b-144">Microsoft SQL Server 2014</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="7dc0b-145">32 Bit oder 64 Bit</span><span class="sxs-lookup"><span data-stu-id="7dc0b-145">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7dc0b-146">Microsoft SQL Server 2012</span><span class="sxs-lookup"><span data-stu-id="7dc0b-146">Microsoft SQL Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="7dc0b-147">SP2</span><span class="sxs-lookup"><span data-stu-id="7dc0b-147">SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="7dc0b-148">32 Bit oder 64 Bit</span><span class="sxs-lookup"><span data-stu-id="7dc0b-148">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7dc0b-149">Microsoft SQL Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7dc0b-149">Microsoft SQL Server 2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="7dc0b-150">SP3</span><span class="sxs-lookup"><span data-stu-id="7dc0b-150">SP3</span></span></p></td>
<td align="left"><p><span data-ttu-id="7dc0b-151">32 Bit oder 64 Bit</span><span class="sxs-lookup"><span data-stu-id="7dc0b-151">32-bit or 64-bit</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="7dc0b-152">Betriebssystemanforderungen für Veröffentlichungsserver</span><span class="sxs-lookup"><span data-stu-id="7dc0b-152">Publishing server operating system requirements</span></span>

<span data-ttu-id="7dc0b-153">In der folgenden Tabelle sind die Betriebssysteme aufgeführt, die für die Installation von App-V 5,0 SP3-Publishing Server unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="7dc0b-153">The following table lists the operating systems that are supported for the App-V 5.0 SP3 Publishing server installation.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="7dc0b-154">Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="7dc0b-154">Operating system</span></span></th>
<th align="left"><span data-ttu-id="7dc0b-155">Service Pack</span><span class="sxs-lookup"><span data-stu-id="7dc0b-155">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="7dc0b-156">System Architektur</span><span class="sxs-lookup"><span data-stu-id="7dc0b-156">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7dc0b-157">Microsoft Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="7dc0b-157">Microsoft Windows Server 2012 R2</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="7dc0b-158">64Bit</span><span class="sxs-lookup"><span data-stu-id="7dc0b-158">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7dc0b-159">Microsoft Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7dc0b-159">Microsoft Windows Server 2012</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="7dc0b-160">64Bit</span><span class="sxs-lookup"><span data-stu-id="7dc0b-160">64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7dc0b-161">Microsoft Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7dc0b-161">Microsoft Windows Server 2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="7dc0b-162">SP1</span><span class="sxs-lookup"><span data-stu-id="7dc0b-162">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="7dc0b-163">64Bit</span><span class="sxs-lookup"><span data-stu-id="7dc0b-163">64-bit</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="publishing-server-hardware-requirements-"></a><span data-ttu-id="7dc0b-164">Hardwareanforderungen für Veröffentlichungsserver</span><span class="sxs-lookup"><span data-stu-id="7dc0b-164">Publishing server hardware requirements</span></span>

<span data-ttu-id="7dc0b-165">App-V bietet keine zusätzlichen Anforderungen, die über die von Windows Server hinausgehen.</span><span class="sxs-lookup"><span data-stu-id="7dc0b-165">App-V adds no additional requirements beyond those of Windows Server.</span></span>

-   <span data-ttu-id="7dc0b-166">Prozessor – 1,4 GHz oder schneller, 64-Bit (x64)-Prozessor</span><span class="sxs-lookup"><span data-stu-id="7dc0b-166">Processor—1.4 GHz or faster, 64-bit (x64) processor</span></span>

-   <span data-ttu-id="7dc0b-167">RAM – 2 GB RAM (64-Bit)</span><span class="sxs-lookup"><span data-stu-id="7dc0b-167">RAM—2 GB RAM (64-bit)</span></span>

-   <span data-ttu-id="7dc0b-168">Speicherplatz – 200 MB verfügbarer Festplattenspeicherplatz, nicht einschließlich des Inhaltsverzeichnisses</span><span class="sxs-lookup"><span data-stu-id="7dc0b-168">Disk space—200 MB available hard disk space, not including the content directory</span></span>

### <span data-ttu-id="7dc0b-169">Anforderungen des Reporting Server-Betriebssystems</span><span class="sxs-lookup"><span data-stu-id="7dc0b-169">Reporting server operating system requirements</span></span>

<span data-ttu-id="7dc0b-170">In der folgenden Tabelle sind die Betriebssysteme aufgeführt, die für die App-V 5,0 SP3 Reporting Server-Installation unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="7dc0b-170">The following table lists the operating systems that are supported for the App-V 5.0 SP3 Reporting server installation.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="7dc0b-171">Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="7dc0b-171">Operating system</span></span></th>
<th align="left"><span data-ttu-id="7dc0b-172">Service Pack</span><span class="sxs-lookup"><span data-stu-id="7dc0b-172">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="7dc0b-173">System Architektur</span><span class="sxs-lookup"><span data-stu-id="7dc0b-173">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7dc0b-174">Microsoft Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="7dc0b-174">Microsoft Windows Server 2012 R2</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="7dc0b-175">64Bit</span><span class="sxs-lookup"><span data-stu-id="7dc0b-175">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7dc0b-176">Microsoft Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7dc0b-176">Microsoft Windows Server 2012</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="7dc0b-177">64Bit</span><span class="sxs-lookup"><span data-stu-id="7dc0b-177">64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7dc0b-178">Microsoft Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7dc0b-178">Microsoft Windows Server 2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="7dc0b-179">SP1</span><span class="sxs-lookup"><span data-stu-id="7dc0b-179">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="7dc0b-180">64Bit</span><span class="sxs-lookup"><span data-stu-id="7dc0b-180">64-bit</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="reporting-server-hardware-requirements-"></a><span data-ttu-id="7dc0b-181">Hardwareanforderungen für den Berichtsserver</span><span class="sxs-lookup"><span data-stu-id="7dc0b-181">Reporting server hardware requirements</span></span>

<span data-ttu-id="7dc0b-182">App-V bietet keine zusätzlichen Anforderungen, die über die von Windows Server hinausgehen.</span><span class="sxs-lookup"><span data-stu-id="7dc0b-182">App-V adds no additional requirements beyond those of Windows Server.</span></span>

-   <span data-ttu-id="7dc0b-183">Prozessor – 1,4 GHz oder schneller, 64-Bit (x64)-Prozessor</span><span class="sxs-lookup"><span data-stu-id="7dc0b-183">Processor—1.4 GHz or faster, 64-bit (x64) processor</span></span>

-   <span data-ttu-id="7dc0b-184">RAM – 2 GB RAM (64-Bit)</span><span class="sxs-lookup"><span data-stu-id="7dc0b-184">RAM—2 GB RAM (64-bit)</span></span>

-   <span data-ttu-id="7dc0b-185">Speicherplatz – 200 MB verfügbarer Festplattenspeicherplatz</span><span class="sxs-lookup"><span data-stu-id="7dc0b-185">Disk space—200 MB available hard disk space</span></span>

### <span data-ttu-id="7dc0b-186">Anforderungen für die Berichtsserver-Datenbank</span><span class="sxs-lookup"><span data-stu-id="7dc0b-186">Reporting server database requirements</span></span>

<span data-ttu-id="7dc0b-187">In der folgenden Tabelle sind die SQL Server-Versionen aufgeführt, die für die App-V 5,0 SP3-Berichtsdatenbank-Installation unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="7dc0b-187">The following table lists the SQL Server versions that are supported for the App-V 5.0 SP3 Reporting database installation.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="7dc0b-188">SQL Server-Version</span><span class="sxs-lookup"><span data-stu-id="7dc0b-188">SQL Server version</span></span></th>
<th align="left"><span data-ttu-id="7dc0b-189">Service Pack</span><span class="sxs-lookup"><span data-stu-id="7dc0b-189">Service pack</span></span></th>
<th align="left"><span data-ttu-id="7dc0b-190">System Architektur</span><span class="sxs-lookup"><span data-stu-id="7dc0b-190">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7dc0b-191">Microsoft SQL Server 2014</span><span class="sxs-lookup"><span data-stu-id="7dc0b-191">Microsoft SQL Server 2014</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="7dc0b-192">32 Bit oder 64 Bit</span><span class="sxs-lookup"><span data-stu-id="7dc0b-192">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7dc0b-193">Microsoft SQL Server 2012</span><span class="sxs-lookup"><span data-stu-id="7dc0b-193">Microsoft SQL Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="7dc0b-194">SP2</span><span class="sxs-lookup"><span data-stu-id="7dc0b-194">SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="7dc0b-195">32 Bit oder 64 Bit</span><span class="sxs-lookup"><span data-stu-id="7dc0b-195">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7dc0b-196">Microsoft SQL Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7dc0b-196">Microsoft SQL Server 2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="7dc0b-197">SP3</span><span class="sxs-lookup"><span data-stu-id="7dc0b-197">SP3</span></span></p></td>
<td align="left"><p><span data-ttu-id="7dc0b-198">32 Bit oder 64 Bit</span><span class="sxs-lookup"><span data-stu-id="7dc0b-198">32-bit or 64-bit</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-client-supp-cfgs"></a><span data-ttu-id="7dc0b-199">App-V-Clientsystemanforderungen</span><span class="sxs-lookup"><span data-stu-id="7dc0b-199">App-V client system requirements</span></span>


<span data-ttu-id="7dc0b-200">In der folgenden Tabelle sind die Betriebssysteme aufgeführt, die für die App-V 5,0 SP3-Clientinstallation unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="7dc0b-200">The following table lists the operating systems that are supported for the App-V 5.0 SP3 client installation.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="7dc0b-201">Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="7dc0b-201">Operating system</span></span></th>
<th align="left"><span data-ttu-id="7dc0b-202">Service Pack</span><span class="sxs-lookup"><span data-stu-id="7dc0b-202">Service pack</span></span></th>
<th align="left"><span data-ttu-id="7dc0b-203">System Architektur</span><span class="sxs-lookup"><span data-stu-id="7dc0b-203">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7dc0b-204">Microsoft Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="7dc0b-204">Microsoft Windows8.1</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="7dc0b-205">32 Bit oder 64 Bit</span><span class="sxs-lookup"><span data-stu-id="7dc0b-205">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7dc0b-206">Microsoft Windows8</span><span class="sxs-lookup"><span data-stu-id="7dc0b-206">Microsoft Windows8</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="7dc0b-207">32 Bit oder 64 Bit</span><span class="sxs-lookup"><span data-stu-id="7dc0b-207">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7dc0b-208">Windows7</span><span class="sxs-lookup"><span data-stu-id="7dc0b-208">Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="7dc0b-209">SP1</span><span class="sxs-lookup"><span data-stu-id="7dc0b-209">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="7dc0b-210">32 Bit oder 64 Bit</span><span class="sxs-lookup"><span data-stu-id="7dc0b-210">32-bit or 64-bit</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="7dc0b-211">Die folgenden App-V-Client Installationsszenarien werden nicht unterstützt, es sei denn, es wird angegeben:</span><span class="sxs-lookup"><span data-stu-id="7dc0b-211">The following App-V client installation scenarios are not supported, except as noted:</span></span>

-   <span data-ttu-id="7dc0b-212">Computer, auf denen Windows Server ausgeführt wird</span><span class="sxs-lookup"><span data-stu-id="7dc0b-212">Computers that run Windows Server</span></span>

-   <span data-ttu-id="7dc0b-213">Computer, auf denen App-v 4.6 SP1 oder frühere Versionen ausgeführt werden</span><span class="sxs-lookup"><span data-stu-id="7dc0b-213">Computers that run App-V4.6SP1 or earlier versions</span></span>

-   <span data-ttu-id="7dc0b-214">Der App-V 5,0 SP3-Remote Desktop Dienste-Client wird nur für RDS-fähige Server unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7dc0b-214">The App-V 5.0 SP3 Remote Desktop services client is supported only for RDS-enabled servers</span></span>

### <a href="" id="app-v-client-hardware-requirements-"></a><span data-ttu-id="7dc0b-215">Hardwareanforderungen für App-V-Clients</span><span class="sxs-lookup"><span data-stu-id="7dc0b-215">App-V client hardware requirements</span></span>

<span data-ttu-id="7dc0b-216">In der folgenden Liste wird die unterstützte Hardwarekonfiguration für die App-V 5,0 SP3-Clientinstallation angezeigt.</span><span class="sxs-lookup"><span data-stu-id="7dc0b-216">The following list displays the supported hardware configuration for the App-V 5.0 SP3 client installation.</span></span>

-   <span data-ttu-id="7dc0b-217">Prozessor – 1,4 GHz oder schneller 32-Bit (x86) oder 64-Bit (x64)-Prozessor</span><span class="sxs-lookup"><span data-stu-id="7dc0b-217">Processor— 1.4 GHz or faster 32-bit (x86) or 64-bit (x64) processor</span></span>

-   <span data-ttu-id="7dc0b-218">RAM – 1 GB (32-Bit) oder 2 GB (64-Bit)</span><span class="sxs-lookup"><span data-stu-id="7dc0b-218">RAM— 1 GB (32-bit) or 2 GB (64-bit)</span></span>

-   <span data-ttu-id="7dc0b-219">Datenträger – 100 MB für die Installation, nicht einschließlich des von virtualisierten Anwendungen verwendeten Speicherplatzes.</span><span class="sxs-lookup"><span data-stu-id="7dc0b-219">Disk— 100 MB for installation, not including the disk space that is used by virtualized applications.</span></span>

## <span data-ttu-id="7dc0b-220">Clientsystemanforderungen für Remote Desktop Dienste</span><span class="sxs-lookup"><span data-stu-id="7dc0b-220">Remote Desktop Services client system requirements</span></span>


<span data-ttu-id="7dc0b-221">In der folgenden Tabelle sind die Betriebssysteme aufgeführt, die für die App-V 5,0 SP3-Clientinstallation für Remote Desktop Dienste (RDS) unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="7dc0b-221">The following table lists the operating systems that are supported for App-V 5.0 SP3 Remote Desktop Services (RDS) client installation.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="7dc0b-222">Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="7dc0b-222">Operating system</span></span></th>
<th align="left"><span data-ttu-id="7dc0b-223">Service Pack</span><span class="sxs-lookup"><span data-stu-id="7dc0b-223">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="7dc0b-224">System Architektur</span><span class="sxs-lookup"><span data-stu-id="7dc0b-224">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7dc0b-225">Microsoft Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="7dc0b-225">Microsoft Windows Server 2012 R2</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="7dc0b-226">64Bit</span><span class="sxs-lookup"><span data-stu-id="7dc0b-226">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7dc0b-227">Microsoft Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7dc0b-227">Microsoft Windows Server 2012</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="7dc0b-228">64Bit</span><span class="sxs-lookup"><span data-stu-id="7dc0b-228">64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7dc0b-229">Microsoft Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7dc0b-229">Microsoft Windows Server 2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="7dc0b-230">SP1</span><span class="sxs-lookup"><span data-stu-id="7dc0b-230">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="7dc0b-231">64Bit</span><span class="sxs-lookup"><span data-stu-id="7dc0b-231">64-bit</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="7dc0b-232">Hardwareanforderungen für Remote Desktop Dienste-Clients</span><span class="sxs-lookup"><span data-stu-id="7dc0b-232">Remote Desktop Services client hardware requirements</span></span>

<span data-ttu-id="7dc0b-233">App-V bietet keine zusätzlichen Anforderungen, die über die von Windows Server hinausgehen.</span><span class="sxs-lookup"><span data-stu-id="7dc0b-233">App-V adds no additional requirements beyond those of Windows Server.</span></span>

-   <span data-ttu-id="7dc0b-234">Prozessor – 1,4 GHz oder schneller, 64-Bit (x64)-Prozessor</span><span class="sxs-lookup"><span data-stu-id="7dc0b-234">Processor—1.4 GHz or faster, 64-bit (x64) processor</span></span>

-   <span data-ttu-id="7dc0b-235">RAM – 2 GB RAM (64-Bit)</span><span class="sxs-lookup"><span data-stu-id="7dc0b-235">RAM—2 GB RAM (64-bit)</span></span>

-   <span data-ttu-id="7dc0b-236">Speicherplatz – 200 MB verfügbarer Festplattenspeicherplatz</span><span class="sxs-lookup"><span data-stu-id="7dc0b-236">Disk space—200 MB available hard disk space</span></span>

## <span data-ttu-id="7dc0b-237">Systemanforderungen für Sequencer</span><span class="sxs-lookup"><span data-stu-id="7dc0b-237">Sequencer system requirements</span></span>


<span data-ttu-id="7dc0b-238">In der folgenden Tabelle sind die Betriebssysteme aufgeführt, die für die App-V 5,0 SP3-Sequencer-Installation unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="7dc0b-238">The following table lists the operating systems that are supported for the App-V 5.0 SP3 Sequencer installation.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="7dc0b-239">Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="7dc0b-239">Operating system</span></span></th>
<th align="left"><span data-ttu-id="7dc0b-240">Service Pack</span><span class="sxs-lookup"><span data-stu-id="7dc0b-240">Service pack</span></span></th>
<th align="left"><span data-ttu-id="7dc0b-241">System Architektur</span><span class="sxs-lookup"><span data-stu-id="7dc0b-241">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7dc0b-242">Microsoft Windows Server2012 R2</span><span class="sxs-lookup"><span data-stu-id="7dc0b-242">Microsoft Windows Server2012 R2</span></span></p></td>
<td align="left"></td>
<td align="left"><p><span data-ttu-id="7dc0b-243">64Bit</span><span class="sxs-lookup"><span data-stu-id="7dc0b-243">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7dc0b-244">Microsoft Windows Server2012</span><span class="sxs-lookup"><span data-stu-id="7dc0b-244">Microsoft Windows Server2012</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="7dc0b-245">64Bit</span><span class="sxs-lookup"><span data-stu-id="7dc0b-245">64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7dc0b-246">Microsoft Windows Server2008 R2</span><span class="sxs-lookup"><span data-stu-id="7dc0b-246">Microsoft Windows Server2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="7dc0b-247">SP1</span><span class="sxs-lookup"><span data-stu-id="7dc0b-247">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="7dc0b-248">64Bit</span><span class="sxs-lookup"><span data-stu-id="7dc0b-248">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7dc0b-249">Microsoft Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="7dc0b-249">Microsoft Windows8.1</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="7dc0b-250">32Bit und 64Bit</span><span class="sxs-lookup"><span data-stu-id="7dc0b-250">32-bit and 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7dc0b-251">Microsoft Windows8</span><span class="sxs-lookup"><span data-stu-id="7dc0b-251">Microsoft Windows8</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="7dc0b-252">32Bit und 64Bit</span><span class="sxs-lookup"><span data-stu-id="7dc0b-252">32-bit and 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7dc0b-253">Microsoft Windows7</span><span class="sxs-lookup"><span data-stu-id="7dc0b-253">Microsoft Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="7dc0b-254">SP1</span><span class="sxs-lookup"><span data-stu-id="7dc0b-254">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="7dc0b-255">32Bit und 64Bit</span><span class="sxs-lookup"><span data-stu-id="7dc0b-255">32-bit and 64-bit</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="7dc0b-256">Hardwareanforderungen für Sequenzer</span><span class="sxs-lookup"><span data-stu-id="7dc0b-256">Sequencer hardware requirements</span></span>

<span data-ttu-id="7dc0b-257">Die Hardwareanforderungen finden Sie in der Windows-oder Windows Server-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="7dc0b-257">See the Windows or Windows Server documentation for the hardware requirements.</span></span> <span data-ttu-id="7dc0b-258">App-V fügt keine zusätzlichen Hardwareanforderungen hinzu.</span><span class="sxs-lookup"><span data-stu-id="7dc0b-258">App-V adds no additional hardware requirements.</span></span>

## <a href="" id="bkmk-supp-ver-sccm"></a><span data-ttu-id="7dc0b-259">Unterstützte Versionen von System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="7dc0b-259">Supported versions of System Center Configuration Manager</span></span>


<span data-ttu-id="7dc0b-260">Der App-V-Client unterstützt die folgenden Versionen von System Center Configuration Manager:</span><span class="sxs-lookup"><span data-stu-id="7dc0b-260">The App-V client supports the following versions of System Center Configuration Manager:</span></span>

-   <span data-ttu-id="7dc0b-261">MicrosoftSystemCenter2012 ConfigurationManager</span><span class="sxs-lookup"><span data-stu-id="7dc0b-261">MicrosoftSystemCenter2012 ConfigurationManager</span></span>

-   <span data-ttu-id="7dc0b-262">System Center 2012 R2 Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="7dc0b-262">System Center 2012 R2 Configuration Manager</span></span>

-   <span data-ttu-id="7dc0b-263">System Center 2012 R2 Configuration Manager SP1</span><span class="sxs-lookup"><span data-stu-id="7dc0b-263">System Center 2012 R2 Configuration Manager SP1</span></span>

<span data-ttu-id="7dc0b-264">Weitere Informationen zur Integration von Configuration Manager in App-v finden Sie unter [Planen der APP-v-Integration in Configuration Manager](https://technet.microsoft.com/library/jj822982.aspx).</span><span class="sxs-lookup"><span data-stu-id="7dc0b-264">For more information about how Configuration Manager integrates with App-V, see [Planning for App-V Integration with Configuration Manager](https://technet.microsoft.com/library/jj822982.aspx).</span></span>






## <span data-ttu-id="7dc0b-265">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="7dc0b-265">Related topics</span></span>


[<span data-ttu-id="7dc0b-266">Planen der Bereitstellung von App-V</span><span class="sxs-lookup"><span data-stu-id="7dc0b-266">Planning to Deploy App-V</span></span>](planning-to-deploy-app-v.md)

[<span data-ttu-id="7dc0b-267">Voraussetzungen für App-V 5.0 SP3</span><span class="sxs-lookup"><span data-stu-id="7dc0b-267">App-V 5.0 SP3 Prerequisites</span></span>](app-v-50-sp3-prerequisites.md)

 

 





