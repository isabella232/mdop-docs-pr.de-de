---
title: App-V 5.1 – Unterstützte Konfigurationen
description: App-V 5.1 – Unterstützte Konfigurationen
author: dansimp
ms.assetid: 8b8db63b-f71c-4ae9-80e7-a6752334e1f6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 04/02/2020
ms.openlocfilehash: fbda364de66b1f7b8730dca38f864a84f7848e58
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805942"
---
# <span data-ttu-id="84d7e-103">App-V 5.1 – Unterstützte Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="84d7e-103">App-V 5.1 Supported Configurations</span></span>

><span data-ttu-id="84d7e-104">Gilt für: Windows 10, Version 1607; Window Server 2019; Windows Server 2016; Windows Server 2012 R2; Windows Server 2012; Windows Server 2008 R2 (erweitertes Sicherheits Update)</span><span class="sxs-lookup"><span data-stu-id="84d7e-104">Applies to: Windows 10, version 1607; Window Server 2019; Windows Server 2016; Windows Server 2012 R2; Windows Server 2012; Windows Server 2008 R2 (Extended Security Update)</span></span>

<span data-ttu-id="84d7e-105">In diesem Thema werden die Anforderungen zum Installieren und Ausführen von Microsoft Application Virtualization (App-V) 5,1 in Ihrer Umgebung angegeben.</span><span class="sxs-lookup"><span data-stu-id="84d7e-105">This topic specifies the requirements to install and run Microsoft Application Virtualization (App-V) 5.1 in your environment.</span></span>

## <span data-ttu-id="84d7e-106">Systemanforderungen für App-V Server</span><span class="sxs-lookup"><span data-stu-id="84d7e-106">App-V Server system requirements</span></span>

<span data-ttu-id="84d7e-107">In diesem Abschnitt werden die Betriebssystem-und Hardwareanforderungen für alle App-V-Server Komponenten aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="84d7e-107">This section lists the operating system and hardware requirements for all of the App-V Server components.</span></span>

### <span data-ttu-id="84d7e-108">Nicht unterstützte App-V 5,1-Server Szenarien</span><span class="sxs-lookup"><span data-stu-id="84d7e-108">Unsupported App-V 5.1 Server scenarios</span></span>

<span data-ttu-id="84d7e-109">Der App-V 5,1-Server unterstützt die folgenden Szenarien nicht:</span><span class="sxs-lookup"><span data-stu-id="84d7e-109">The App-V 5.1 Server does not support the following scenarios:</span></span>

-   <span data-ttu-id="84d7e-110">Bereitstellung auf einem Computer, auf dem Microsoft Windows Server Core ausgeführt wird</span><span class="sxs-lookup"><span data-stu-id="84d7e-110">Deployment to a computer that runs Microsoft Windows Server Core.</span></span>

-   <span data-ttu-id="84d7e-111">Bereitstellung auf einem Computer, auf dem eine frühere Version der App-V 5,1-Server Komponenten ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="84d7e-111">Deployment to a computer that runs a previous version of App-V 5.1 Server components.</span></span> <span data-ttu-id="84d7e-112">Sie können APP-v 5,1 nebeneinander mit dem App-v 4.5 Lightweight Streaming Server (LWS)-Server installieren.</span><span class="sxs-lookup"><span data-stu-id="84d7e-112">You can install App-V 5.1 side by side with the App-V4.5 Lightweight Streaming Server (LWS) server only.</span></span> <span data-ttu-id="84d7e-113">Die Bereitstellung von App-v nebeneinander mit dem App-v 4,5 Application Virtualization Management Service (HWS)-Server wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="84d7e-113">Deployment of App-V side by side with the App-V 4.5 Application Virtualization Management Service (HWS) server is not supported.</span></span>

-   <span data-ttu-id="84d7e-114">Bereitstellung auf einem Computer, auf dem Microsoft SQL Server Express Edition ausgeführt wird</span><span class="sxs-lookup"><span data-stu-id="84d7e-114">Deployment to a computer that runs Microsoft SQL Server Express edition.</span></span>

-   <span data-ttu-id="84d7e-115">Bereitstellung auf einem Domänencontroller.</span><span class="sxs-lookup"><span data-stu-id="84d7e-115">Deployment to a domain controller.</span></span>

-   <span data-ttu-id="84d7e-116">Kurze Pfade.</span><span class="sxs-lookup"><span data-stu-id="84d7e-116">Short paths.</span></span> <span data-ttu-id="84d7e-117">Wenn Sie einen kurzen Pfad verwenden möchten, müssen Sie einen neuen Datenträger erstellen.</span><span class="sxs-lookup"><span data-stu-id="84d7e-117">If you plan to use a short path, you must create a new volume.</span></span>

### <span data-ttu-id="84d7e-118">Betriebssystemanforderungen für Management Server</span><span class="sxs-lookup"><span data-stu-id="84d7e-118">Management server operating system requirements</span></span>

<span data-ttu-id="84d7e-119">In der folgenden Tabelle sind die Betriebssysteme aufgeführt, die für die Installation des App-V 5,1-Verwaltungsservers unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="84d7e-119">The following table lists the operating systems that are supported for the App-V 5.1 Management server installation.</span></span>

> [!NOTE]
> <span data-ttu-id="84d7e-120">Microsoft bietet Unterstützung für das aktuelle Service Pack und in einigen Fällen das unmittelbar vorhergehende Service Pack.</span><span class="sxs-lookup"><span data-stu-id="84d7e-120">Microsoft provides support for the current service pack and, in some cases, the immediately preceding service pack.</span></span> <span data-ttu-id="84d7e-121">Informationen zu den Support Zeitachsen für Ihr Produkt finden Sie unter [unterstützte Service Packs für Lebenszyklen](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span><span class="sxs-lookup"><span data-stu-id="84d7e-121">To find the support timelines for your product, see the [Lifecycle Supported Service Packs](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span></span> <span data-ttu-id="84d7e-122">Weitere Informationen finden Sie unter [Supportrichtlinien für Microsoft Support-Lebenszyklus](https://go.microsoft.com/fwlink/p/?LinkId=31976) .</span><span class="sxs-lookup"><span data-stu-id="84d7e-122">See [Microsoft Support Lifecycle Support Policy FAQ](https://go.microsoft.com/fwlink/p/?LinkId=31976) for more information.</span></span>

 | <span data-ttu-id="84d7e-123">Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="84d7e-123">Operating System</span></span>                 | <span data-ttu-id="84d7e-124">Service Pack</span><span class="sxs-lookup"><span data-stu-id="84d7e-124">Service Pack</span></span> | <span data-ttu-id="84d7e-125">System Architektur</span><span class="sxs-lookup"><span data-stu-id="84d7e-125">System Architecture</span></span> |
|----------------------------------|--------------|---------------------|
| <span data-ttu-id="84d7e-126">Microsoft Windows Server 2019</span><span class="sxs-lookup"><span data-stu-id="84d7e-126">Microsoft Windows Server 2019</span></span>    |              |        <span data-ttu-id="84d7e-127">64Bit</span><span class="sxs-lookup"><span data-stu-id="84d7e-127">64-bit</span></span>       |
| <span data-ttu-id="84d7e-128">Microsoft Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="84d7e-128">Microsoft Windows Server 2016</span></span>    |              |        <span data-ttu-id="84d7e-129">64Bit</span><span class="sxs-lookup"><span data-stu-id="84d7e-129">64-bit</span></span>       |
| <span data-ttu-id="84d7e-130">Microsoft Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="84d7e-130">Microsoft Windows Server 2012 R2</span></span> |              |        <span data-ttu-id="84d7e-131">64Bit</span><span class="sxs-lookup"><span data-stu-id="84d7e-131">64-bit</span></span>       |
| <span data-ttu-id="84d7e-132">Microsoft Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="84d7e-132">Microsoft Windows Server 2012</span></span>    |              |        <span data-ttu-id="84d7e-133">64Bit</span><span class="sxs-lookup"><span data-stu-id="84d7e-133">64-bit</span></span>       |
| <span data-ttu-id="84d7e-134">[Erweitertes Sicherheits Update](https://www.microsoft.com/windows-server/extended-security-updates) für Microsoft Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="84d7e-134">Microsoft Windows Server 2008 R2 [Extended Security Update](https://www.microsoft.com/windows-server/extended-security-updates)</span></span>|      <span data-ttu-id="84d7e-135">SP1</span><span class="sxs-lookup"><span data-stu-id="84d7e-135">SP1</span></span>     |        <span data-ttu-id="84d7e-136">64Bit</span><span class="sxs-lookup"><span data-stu-id="84d7e-136">64-bit</span></span>       |
 

<span data-ttu-id="84d7e-137">**Wichtig**  Die Bereitstellung der Verwaltungsserverrolle auf einem Computer mit aktivierter Remote Desktop Freigabe (RDS) wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="84d7e-137">**Important** Deployment of the Management server role to a computer with Remote Desktop Sharing (RDS) enabled is not supported.</span></span>

 

### <a href="" id="management-server-hardware-requirements-"></a><span data-ttu-id="84d7e-138">Hardwareanforderungen für den Verwaltungsserver</span><span class="sxs-lookup"><span data-stu-id="84d7e-138">Management server hardware requirements</span></span>

-   <span data-ttu-id="84d7e-139">Prozessor – 1,4 GHz oder schneller, 64-Bit (x64)-Prozessor</span><span class="sxs-lookup"><span data-stu-id="84d7e-139">Processor—1.4 GHz or faster, 64-bit (x64) processor</span></span>

-   <span data-ttu-id="84d7e-140">RAM – 1 GB RAM (64-Bit)</span><span class="sxs-lookup"><span data-stu-id="84d7e-140">RAM—1 GB RAM (64-bit)</span></span>

-   <span data-ttu-id="84d7e-141">Speicherplatz – 200 MB verfügbarer Festplattenspeicherplatz, nicht einschließlich des Inhaltsverzeichnisses</span><span class="sxs-lookup"><span data-stu-id="84d7e-141">Disk space—200 MB available hard disk space, not including the content directory</span></span>

### <span data-ttu-id="84d7e-142">Verwaltungsserver-Datenbankanforderungen</span><span class="sxs-lookup"><span data-stu-id="84d7e-142">Management server database requirements</span></span>

<span data-ttu-id="84d7e-143">In der folgenden Tabelle sind die SQL Server-Versionen aufgeführt, die für die Installation der App-V 5,1-Verwaltungsdatenbank unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="84d7e-143">The following table lists the SQL Server versions that are supported for the App-V 5.1 Management database installation.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="84d7e-144">SQL Server-Version</span><span class="sxs-lookup"><span data-stu-id="84d7e-144">SQL Server version</span></span></th>
<th align="left"><span data-ttu-id="84d7e-145">Service Pack</span><span class="sxs-lookup"><span data-stu-id="84d7e-145">Service pack</span></span></th>
<th align="left"><span data-ttu-id="84d7e-146">System Architektur</span><span class="sxs-lookup"><span data-stu-id="84d7e-146">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="even">
<td align="left"><p><span data-ttu-id="84d7e-147">Microsoft SQL Server 2019</span><span class="sxs-lookup"><span data-stu-id="84d7e-147">Microsoft SQL Server 2019</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="84d7e-148">32 Bit oder 64 Bit</span><span class="sxs-lookup"><span data-stu-id="84d7e-148">32-bit or 64-bit</span></span></p></td>
</tr>

<tr class="odd">
<td align="left"><p><span data-ttu-id="84d7e-149">Microsoft SQL Server 2017</span><span class="sxs-lookup"><span data-stu-id="84d7e-149">Microsoft SQL Server 2017</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="84d7e-150">32 Bit oder 64 Bit</span><span class="sxs-lookup"><span data-stu-id="84d7e-150">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="84d7e-151">Microsoft SQL Server 2016</span><span class="sxs-lookup"><span data-stu-id="84d7e-151">Microsoft SQL Server 2016</span></span></p></td>
<td align="left"><p><span data-ttu-id="84d7e-152">SP2</span><span class="sxs-lookup"><span data-stu-id="84d7e-152">SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="84d7e-153">32 Bit oder 64 Bit</span><span class="sxs-lookup"><span data-stu-id="84d7e-153">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="84d7e-154">Microsoft SQL Server 2014</span><span class="sxs-lookup"><span data-stu-id="84d7e-154">Microsoft SQL Server 2014</span></span></p></td>
<td align="left"><p><span data-ttu-id="84d7e-155">SP2</span><span class="sxs-lookup"><span data-stu-id="84d7e-155">SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="84d7e-156">32 Bit oder 64 Bit</span><span class="sxs-lookup"><span data-stu-id="84d7e-156">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="84d7e-157">Microsoft SQL Server 2012</span><span class="sxs-lookup"><span data-stu-id="84d7e-157">Microsoft SQL Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="84d7e-158">SP2</span><span class="sxs-lookup"><span data-stu-id="84d7e-158">SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="84d7e-159">32 Bit oder 64 Bit</span><span class="sxs-lookup"><span data-stu-id="84d7e-159">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="84d7e-160">Microsoft SQL Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="84d7e-160">Microsoft SQL Server 2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="84d7e-161">SP3</span><span class="sxs-lookup"><span data-stu-id="84d7e-161">SP3</span></span></p></td>
<td align="left"><p><span data-ttu-id="84d7e-162">32 Bit oder 64 Bit</span><span class="sxs-lookup"><span data-stu-id="84d7e-162">32-bit or 64-bit</span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="84d7e-163">Weitere Informationen zu Benutzer Konfigurationsdateien mit SQL Server 2016 oder höher finden Sie im [Support Artikel](https://support.microsoft.com/help/4548751/app-v-server-publishing-might-fail-when-you-apply-user-configuration-f).</span><span class="sxs-lookup"><span data-stu-id="84d7e-163">For more information on user configuration files with SQL server 2016 or later, see the [support article](https://support.microsoft.com/help/4548751/app-v-server-publishing-might-fail-when-you-apply-user-configuration-f).</span></span>

### <span data-ttu-id="84d7e-164">Betriebssystemanforderungen für Veröffentlichungsserver</span><span class="sxs-lookup"><span data-stu-id="84d7e-164">Publishing server operating system requirements</span></span>

<span data-ttu-id="84d7e-165">In der folgenden Tabelle sind die Betriebssysteme aufgeführt, die für die Installation des App-V 5,1-Publishing Servers unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="84d7e-165">The following table lists the operating systems that are supported for the App-V 5.1 Publishing server installation.</span></span>

| <span data-ttu-id="84d7e-166">Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="84d7e-166">Operating System</span></span>                 | <span data-ttu-id="84d7e-167">Service Pack</span><span class="sxs-lookup"><span data-stu-id="84d7e-167">Service Pack</span></span> | <span data-ttu-id="84d7e-168">System Architektur</span><span class="sxs-lookup"><span data-stu-id="84d7e-168">System Architecture</span></span> |
|----------------------------------|--------------|---------------------|
| <span data-ttu-id="84d7e-169">Microsoft Windows Server 2019</span><span class="sxs-lookup"><span data-stu-id="84d7e-169">Microsoft Windows Server 2019</span></span>    |              |        <span data-ttu-id="84d7e-170">64Bit</span><span class="sxs-lookup"><span data-stu-id="84d7e-170">64-bit</span></span>       |
| <span data-ttu-id="84d7e-171">Microsoft Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="84d7e-171">Microsoft Windows Server 2016</span></span>    |              |        <span data-ttu-id="84d7e-172">64Bit</span><span class="sxs-lookup"><span data-stu-id="84d7e-172">64-bit</span></span>       |
| <span data-ttu-id="84d7e-173">Microsoft Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="84d7e-173">Microsoft Windows Server 2012 R2</span></span> |              |        <span data-ttu-id="84d7e-174">64Bit</span><span class="sxs-lookup"><span data-stu-id="84d7e-174">64-bit</span></span>       |
| <span data-ttu-id="84d7e-175">Microsoft Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="84d7e-175">Microsoft Windows Server 2012</span></span>    |              |        <span data-ttu-id="84d7e-176">64Bit</span><span class="sxs-lookup"><span data-stu-id="84d7e-176">64-bit</span></span>       |
| <span data-ttu-id="84d7e-177">[Erweitertes Sicherheits Update](https://www.microsoft.com/windows-server/extended-security-updates) für Microsoft Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="84d7e-177">Microsoft Windows Server 2008 R2 [Extended Security Update](https://www.microsoft.com/windows-server/extended-security-updates)</span></span> |      <span data-ttu-id="84d7e-178">SP1</span><span class="sxs-lookup"><span data-stu-id="84d7e-178">SP1</span></span>     |        <span data-ttu-id="84d7e-179">64Bit</span><span class="sxs-lookup"><span data-stu-id="84d7e-179">64-bit</span></span>       |

### <a href="" id="publishing-server-hardware-requirements-"></a><span data-ttu-id="84d7e-180">Hardwareanforderungen für Veröffentlichungsserver</span><span class="sxs-lookup"><span data-stu-id="84d7e-180">Publishing server hardware requirements</span></span>

<span data-ttu-id="84d7e-181">App-V bietet keine zusätzlichen Anforderungen, die über die von Windows Server hinausgehen.</span><span class="sxs-lookup"><span data-stu-id="84d7e-181">App-V adds no additional requirements beyond those of Windows Server.</span></span>

-   <span data-ttu-id="84d7e-182">Prozessor – 1,4 GHz oder schneller, 64-Bit (x64)-Prozessor</span><span class="sxs-lookup"><span data-stu-id="84d7e-182">Processor—1.4 GHz or faster, 64-bit (x64) processor</span></span>

-   <span data-ttu-id="84d7e-183">RAM – 2 GB RAM (64-Bit)</span><span class="sxs-lookup"><span data-stu-id="84d7e-183">RAM—2 GB RAM (64-bit)</span></span>

-   <span data-ttu-id="84d7e-184">Speicherplatz – 200 MB verfügbarer Festplattenspeicherplatz, nicht einschließlich des Inhaltsverzeichnisses</span><span class="sxs-lookup"><span data-stu-id="84d7e-184">Disk space—200 MB available hard disk space, not including the content directory</span></span>

### <span data-ttu-id="84d7e-185">Anforderungen des Reporting Server-Betriebssystems</span><span class="sxs-lookup"><span data-stu-id="84d7e-185">Reporting server operating system requirements</span></span>

<span data-ttu-id="84d7e-186">In der folgenden Tabelle sind die Betriebssysteme aufgeführt, die für die App-V 5,1 Reporting Server-Installation unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="84d7e-186">The following table lists the operating systems that are supported for the App-V 5.1 Reporting server installation.</span></span>

| <span data-ttu-id="84d7e-187">Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="84d7e-187">Operating System</span></span>                 | <span data-ttu-id="84d7e-188">Service Pack</span><span class="sxs-lookup"><span data-stu-id="84d7e-188">Service Pack</span></span> | <span data-ttu-id="84d7e-189">System Architektur</span><span class="sxs-lookup"><span data-stu-id="84d7e-189">System Architecture</span></span> |
|----------------------------------|--------------|---------------------|
| <span data-ttu-id="84d7e-190">Microsoft Windows Server 2019</span><span class="sxs-lookup"><span data-stu-id="84d7e-190">Microsoft Windows Server 2019</span></span>    |              |        <span data-ttu-id="84d7e-191">64Bit</span><span class="sxs-lookup"><span data-stu-id="84d7e-191">64-bit</span></span>       |
| <span data-ttu-id="84d7e-192">Microsoft Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="84d7e-192">Microsoft Windows Server 2016</span></span>    |              |        <span data-ttu-id="84d7e-193">64Bit</span><span class="sxs-lookup"><span data-stu-id="84d7e-193">64-bit</span></span>       |
| <span data-ttu-id="84d7e-194">Microsoft Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="84d7e-194">Microsoft Windows Server 2012 R2</span></span> |              |        <span data-ttu-id="84d7e-195">64Bit</span><span class="sxs-lookup"><span data-stu-id="84d7e-195">64-bit</span></span>       |
| <span data-ttu-id="84d7e-196">Microsoft Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="84d7e-196">Microsoft Windows Server 2012</span></span>    |              |        <span data-ttu-id="84d7e-197">64Bit</span><span class="sxs-lookup"><span data-stu-id="84d7e-197">64-bit</span></span>       |
| <span data-ttu-id="84d7e-198">[Erweitertes Sicherheits Update](https://www.microsoft.com/windows-server/extended-security-updates) für Microsoft Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="84d7e-198">Microsoft Windows Server 2008 R2 [Extended Security Update](https://www.microsoft.com/windows-server/extended-security-updates)</span></span> |      <span data-ttu-id="84d7e-199">SP1</span><span class="sxs-lookup"><span data-stu-id="84d7e-199">SP1</span></span>     |        <span data-ttu-id="84d7e-200">64Bit</span><span class="sxs-lookup"><span data-stu-id="84d7e-200">64-bit</span></span>       |

### <a href="" id="reporting-server-hardware-requirements-"></a><span data-ttu-id="84d7e-201">Hardwareanforderungen für den Berichtsserver</span><span class="sxs-lookup"><span data-stu-id="84d7e-201">Reporting server hardware requirements</span></span>

<span data-ttu-id="84d7e-202">App-V bietet keine zusätzlichen Anforderungen, die über die von Windows Server hinausgehen.</span><span class="sxs-lookup"><span data-stu-id="84d7e-202">App-V adds no additional requirements beyond those of Windows Server.</span></span>

-   <span data-ttu-id="84d7e-203">Prozessor – 1,4 GHz oder schneller, 64-Bit (x64)-Prozessor</span><span class="sxs-lookup"><span data-stu-id="84d7e-203">Processor—1.4 GHz or faster, 64-bit (x64) processor</span></span>

-   <span data-ttu-id="84d7e-204">RAM – 2 GB RAM (64-Bit)</span><span class="sxs-lookup"><span data-stu-id="84d7e-204">RAM—2 GB RAM (64-bit)</span></span>

-   <span data-ttu-id="84d7e-205">Speicherplatz – 200 MB verfügbarer Festplattenspeicherplatz</span><span class="sxs-lookup"><span data-stu-id="84d7e-205">Disk space—200 MB available hard disk space</span></span>

### <span data-ttu-id="84d7e-206">Anforderungen für die Berichtsserver-Datenbank</span><span class="sxs-lookup"><span data-stu-id="84d7e-206">Reporting server database requirements</span></span>

<span data-ttu-id="84d7e-207">In der folgenden Tabelle sind die SQL Server-Versionen aufgeführt, die für die Installation der App-V 5,1-Berichtsdatenbank unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="84d7e-207">The following table lists the SQL Server versions that are supported for the App-V 5.1 Reporting database installation.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="84d7e-208">SQL Server-Version</span><span class="sxs-lookup"><span data-stu-id="84d7e-208">SQL Server version</span></span></th>
<th align="left"><span data-ttu-id="84d7e-209">Service Pack</span><span class="sxs-lookup"><span data-stu-id="84d7e-209">Service pack</span></span></th>
<th align="left"><span data-ttu-id="84d7e-210">System Architektur</span><span class="sxs-lookup"><span data-stu-id="84d7e-210">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="84d7e-211">Microsoft SQL Server 2017</span><span class="sxs-lookup"><span data-stu-id="84d7e-211">Microsoft SQL Server 2017</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="84d7e-212">32 Bit oder 64 Bit</span><span class="sxs-lookup"><span data-stu-id="84d7e-212">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="84d7e-213">Microsoft SQL Server 2016</span><span class="sxs-lookup"><span data-stu-id="84d7e-213">Microsoft SQL Server 2016</span></span></p></td>
<td align="left"><p><span data-ttu-id="84d7e-214">SP2</span><span class="sxs-lookup"><span data-stu-id="84d7e-214">SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="84d7e-215">32 Bit oder 64 Bit</span><span class="sxs-lookup"><span data-stu-id="84d7e-215">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="84d7e-216">Microsoft SQL Server 2014</span><span class="sxs-lookup"><span data-stu-id="84d7e-216">Microsoft SQL Server 2014</span></span></p></td>
<td align="left"><p><span data-ttu-id="84d7e-217">SP2</span><span class="sxs-lookup"><span data-stu-id="84d7e-217">SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="84d7e-218">32 Bit oder 64 Bit</span><span class="sxs-lookup"><span data-stu-id="84d7e-218">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="84d7e-219">Microsoft SQL Server 2012</span><span class="sxs-lookup"><span data-stu-id="84d7e-219">Microsoft SQL Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="84d7e-220">SP2</span><span class="sxs-lookup"><span data-stu-id="84d7e-220">SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="84d7e-221">32 Bit oder 64 Bit</span><span class="sxs-lookup"><span data-stu-id="84d7e-221">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="84d7e-222">Microsoft SQL Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="84d7e-222">Microsoft SQL Server 2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="84d7e-223">SP3</span><span class="sxs-lookup"><span data-stu-id="84d7e-223">SP3</span></span></p></td>
<td align="left"><p><span data-ttu-id="84d7e-224">32 Bit oder 64 Bit</span><span class="sxs-lookup"><span data-stu-id="84d7e-224">32-bit or 64-bit</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-client-supp-cfgs"></a><span data-ttu-id="84d7e-225">App-V-Clientsystemanforderungen</span><span class="sxs-lookup"><span data-stu-id="84d7e-225">App-V client system requirements</span></span>

<span data-ttu-id="84d7e-226">In der folgenden Tabelle sind die Betriebssysteme aufgeführt, die für die App-V 5,1-Clientinstallation unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="84d7e-226">The following table lists the operating systems that are supported for the App-V 5.1 client installation.</span></span>

> [!NOTE]
> <span data-ttu-id="84d7e-227">Mit der Windows 10-Anniversary-Version (aka 1607-Version) ist der APP-v-Client in-Box und blockiert die Installation einer früheren Version des App-v-Clients.</span><span class="sxs-lookup"><span data-stu-id="84d7e-227">With the Windows 10 Anniversary release (aka 1607 version), the App-V client is in-box and will block installation of any previous version of the App-V client</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="84d7e-228">Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="84d7e-228">Operating system</span></span></th>
<th align="left"><span data-ttu-id="84d7e-229">Service Pack</span><span class="sxs-lookup"><span data-stu-id="84d7e-229">Service pack</span></span></th>
<th align="left"><span data-ttu-id="84d7e-230">System Architektur</span><span class="sxs-lookup"><span data-stu-id="84d7e-230">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="84d7e-231">Microsoft Windows10 (Pre-1607-Version)</span><span class="sxs-lookup"><span data-stu-id="84d7e-231">Microsoft Windows10 (pre-1607 version)</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="84d7e-232">32 Bit oder 64 Bit</span><span class="sxs-lookup"><span data-stu-id="84d7e-232">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="84d7e-233">Microsoft Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="84d7e-233">Microsoft Windows8.1</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="84d7e-234">32 Bit oder 64 Bit</span><span class="sxs-lookup"><span data-stu-id="84d7e-234">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="84d7e-235">Windows7</span><span class="sxs-lookup"><span data-stu-id="84d7e-235">Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="84d7e-236">SP1</span><span class="sxs-lookup"><span data-stu-id="84d7e-236">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="84d7e-237">32 Bit oder 64 Bit</span><span class="sxs-lookup"><span data-stu-id="84d7e-237">32-bit or 64-bit</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="84d7e-238">Die folgenden App-V-Client Installationsszenarien werden nicht unterstützt, es sei denn, es wird angegeben:</span><span class="sxs-lookup"><span data-stu-id="84d7e-238">The following App-V client installation scenarios are not supported, except as noted:</span></span>

-   <span data-ttu-id="84d7e-239">Computer, auf denen Windows Server ausgeführt wird</span><span class="sxs-lookup"><span data-stu-id="84d7e-239">Computers that run Windows Server</span></span>

-   <span data-ttu-id="84d7e-240">Computer, auf denen App-v 4.6 SP1 oder frühere Versionen ausgeführt werden</span><span class="sxs-lookup"><span data-stu-id="84d7e-240">Computers that run App-V4.6SP1 or earlier versions</span></span>

-   <span data-ttu-id="84d7e-241">Der App-V 5,1-Client für Remote Desktop Dienste wird nur für RDS-fähige Server unterstützt.</span><span class="sxs-lookup"><span data-stu-id="84d7e-241">The App-V 5.1 Remote Desktop services client is supported only for RDS-enabled servers</span></span>

### <a href="" id="app-v-client-hardware-requirements-"></a><span data-ttu-id="84d7e-242">Hardwareanforderungen für App-V-Clients</span><span class="sxs-lookup"><span data-stu-id="84d7e-242">App-V client hardware requirements</span></span>

<span data-ttu-id="84d7e-243">In der folgenden Liste wird die unterstützte Hardwarekonfiguration für die App-V 5,1-Clientinstallation angezeigt.</span><span class="sxs-lookup"><span data-stu-id="84d7e-243">The following list displays the supported hardware configuration for the App-V 5.1 client installation.</span></span>

-   <span data-ttu-id="84d7e-244">Prozessor – 1,4 GHz oder schneller 32-Bit (x86) oder 64-Bit (x64)-Prozessor</span><span class="sxs-lookup"><span data-stu-id="84d7e-244">Processor— 1.4 GHz or faster 32-bit (x86) or 64-bit (x64) processor</span></span>

-   <span data-ttu-id="84d7e-245">RAM – 1 GB (32-Bit) oder 2 GB (64-Bit)</span><span class="sxs-lookup"><span data-stu-id="84d7e-245">RAM— 1 GB (32-bit) or 2 GB (64-bit)</span></span>

-   <span data-ttu-id="84d7e-246">Datenträger – 100 MB für die Installation, nicht einschließlich des von virtualisierten Anwendungen verwendeten Speicherplatzes.</span><span class="sxs-lookup"><span data-stu-id="84d7e-246">Disk— 100 MB for installation, not including the disk space that is used by virtualized applications.</span></span>

## <span data-ttu-id="84d7e-247">Clientsystemanforderungen für Remote Desktop Dienste</span><span class="sxs-lookup"><span data-stu-id="84d7e-247">Remote Desktop Services client system requirements</span></span>


<span data-ttu-id="84d7e-248">In der folgenden Tabelle sind die Betriebssysteme aufgeführt, die für die App-V 5,1-Clientinstallation für Remote Desktop Dienste (RDS) unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="84d7e-248">The following table lists the operating systems that are supported for App-V 5.1 Remote Desktop Services (RDS) client installation.</span></span>

| <span data-ttu-id="84d7e-249">Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="84d7e-249">Operating System</span></span>                 | <span data-ttu-id="84d7e-250">Service Pack</span><span class="sxs-lookup"><span data-stu-id="84d7e-250">Service Pack</span></span> | <span data-ttu-id="84d7e-251">System Architektur</span><span class="sxs-lookup"><span data-stu-id="84d7e-251">System Architecture</span></span> |
|----------------------------------|--------------|---------------------|
| <span data-ttu-id="84d7e-252">Microsoft Windows Server 2019</span><span class="sxs-lookup"><span data-stu-id="84d7e-252">Microsoft Windows Server 2019</span></span>    |              |        <span data-ttu-id="84d7e-253">64Bit</span><span class="sxs-lookup"><span data-stu-id="84d7e-253">64-bit</span></span>       |
| <span data-ttu-id="84d7e-254">Microsoft Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="84d7e-254">Microsoft Windows Server 2016</span></span>    |              |        <span data-ttu-id="84d7e-255">64Bit</span><span class="sxs-lookup"><span data-stu-id="84d7e-255">64-bit</span></span>       |
| <span data-ttu-id="84d7e-256">Microsoft Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="84d7e-256">Microsoft Windows Server 2012 R2</span></span> |              |        <span data-ttu-id="84d7e-257">64Bit</span><span class="sxs-lookup"><span data-stu-id="84d7e-257">64-bit</span></span>       |
| <span data-ttu-id="84d7e-258">Microsoft Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="84d7e-258">Microsoft Windows Server 2012</span></span>    |              |        <span data-ttu-id="84d7e-259">64Bit</span><span class="sxs-lookup"><span data-stu-id="84d7e-259">64-bit</span></span>       |
| <span data-ttu-id="84d7e-260">[Erweitertes Sicherheits Update](https://www.microsoft.com/windows-server/extended-security-updates) für Microsoft Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="84d7e-260">Microsoft Windows Server 2008 R2 [Extended Security Update](https://www.microsoft.com/windows-server/extended-security-updates)</span></span> |      <span data-ttu-id="84d7e-261">SP1</span><span class="sxs-lookup"><span data-stu-id="84d7e-261">SP1</span></span>     |        <span data-ttu-id="84d7e-262">64Bit</span><span class="sxs-lookup"><span data-stu-id="84d7e-262">64-bit</span></span>       |

### <span data-ttu-id="84d7e-263">Hardwareanforderungen für Remote Desktop Dienste-Clients</span><span class="sxs-lookup"><span data-stu-id="84d7e-263">Remote Desktop Services client hardware requirements</span></span>

<span data-ttu-id="84d7e-264">App-V bietet keine zusätzlichen Anforderungen, die über die von Windows Server hinausgehen.</span><span class="sxs-lookup"><span data-stu-id="84d7e-264">App-V adds no additional requirements beyond those of Windows Server.</span></span>

-   <span data-ttu-id="84d7e-265">Prozessor – 1,4 GHz oder schneller, 64-Bit (x64)-Prozessor</span><span class="sxs-lookup"><span data-stu-id="84d7e-265">Processor—1.4 GHz or faster, 64-bit (x64) processor</span></span>

-   <span data-ttu-id="84d7e-266">RAM – 2 GB RAM (64-Bit)</span><span class="sxs-lookup"><span data-stu-id="84d7e-266">RAM—2 GB RAM (64-bit)</span></span>

-   <span data-ttu-id="84d7e-267">Speicherplatz – 200 MB verfügbarer Festplattenspeicherplatz</span><span class="sxs-lookup"><span data-stu-id="84d7e-267">Disk space—200 MB available hard disk space</span></span>

## <span data-ttu-id="84d7e-268">Systemanforderungen für Sequencer</span><span class="sxs-lookup"><span data-stu-id="84d7e-268">Sequencer system requirements</span></span>

<span data-ttu-id="84d7e-269">In der folgenden Tabelle sind die Betriebssysteme aufgeführt, die für die App-V 5,1 Sequencer-Installation unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="84d7e-269">The following table lists the operating systems that are supported for the App-V 5.1 Sequencer installation.</span></span>

| <span data-ttu-id="84d7e-270">Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="84d7e-270">Operating System</span></span>                 | <span data-ttu-id="84d7e-271">Service Pack</span><span class="sxs-lookup"><span data-stu-id="84d7e-271">Service Pack</span></span> | <span data-ttu-id="84d7e-272">System Architektur</span><span class="sxs-lookup"><span data-stu-id="84d7e-272">System Architecture</span></span> |
|----------------------------------|--------------|---------------------|
| <span data-ttu-id="84d7e-273">Microsoft Windows Server 2019</span><span class="sxs-lookup"><span data-stu-id="84d7e-273">Microsoft Windows Server 2019</span></span>    |              |        <span data-ttu-id="84d7e-274">64Bit</span><span class="sxs-lookup"><span data-stu-id="84d7e-274">64-bit</span></span>       |
| <span data-ttu-id="84d7e-275">Microsoft Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="84d7e-275">Microsoft Windows Server 2016</span></span>    |              |        <span data-ttu-id="84d7e-276">64Bit</span><span class="sxs-lookup"><span data-stu-id="84d7e-276">64-bit</span></span>       |
| <span data-ttu-id="84d7e-277">Microsoft Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="84d7e-277">Microsoft Windows Server 2012 R2</span></span> |              |        <span data-ttu-id="84d7e-278">64Bit</span><span class="sxs-lookup"><span data-stu-id="84d7e-278">64-bit</span></span>       |
| <span data-ttu-id="84d7e-279">Microsoft Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="84d7e-279">Microsoft Windows Server 2012</span></span>    |              |        <span data-ttu-id="84d7e-280">64Bit</span><span class="sxs-lookup"><span data-stu-id="84d7e-280">64-bit</span></span>       |
| <span data-ttu-id="84d7e-281">[Erweitertes Sicherheits Update](https://www.microsoft.com/windows-server/extended-security-updates) für Microsoft Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="84d7e-281">Microsoft Windows Server 2008 R2 [Extended Security Update](https://www.microsoft.com/windows-server/extended-security-updates)</span></span> |      <span data-ttu-id="84d7e-282">SP1</span><span class="sxs-lookup"><span data-stu-id="84d7e-282">SP1</span></span>     |        <span data-ttu-id="84d7e-283">64Bit</span><span class="sxs-lookup"><span data-stu-id="84d7e-283">64-bit</span></span>       |
| <span data-ttu-id="84d7e-284">Microsoft Windows 10</span><span class="sxs-lookup"><span data-stu-id="84d7e-284">Microsoft Windows 10</span></span>             |              | <span data-ttu-id="84d7e-285">32Bit und 64Bit</span><span class="sxs-lookup"><span data-stu-id="84d7e-285">32-bit and 64-bit</span></span>   |
| <span data-ttu-id="84d7e-286">Microsoft Windows 8,1</span><span class="sxs-lookup"><span data-stu-id="84d7e-286">Microsoft Windows 8.1</span></span>            |              | <span data-ttu-id="84d7e-287">32Bit und 64Bit</span><span class="sxs-lookup"><span data-stu-id="84d7e-287">32-bit and 64-bit</span></span>   |
| <span data-ttu-id="84d7e-288">Microsoft Windows 7</span><span class="sxs-lookup"><span data-stu-id="84d7e-288">Microsoft Windows 7</span></span>              |      <span data-ttu-id="84d7e-289">SP1</span><span class="sxs-lookup"><span data-stu-id="84d7e-289">SP1</span></span>     | <span data-ttu-id="84d7e-290">32Bit und 64Bit</span><span class="sxs-lookup"><span data-stu-id="84d7e-290">32-bit and 64-bit</span></span>   |

### <span data-ttu-id="84d7e-291">Hardwareanforderungen für Sequenzer</span><span class="sxs-lookup"><span data-stu-id="84d7e-291">Sequencer hardware requirements</span></span>

<span data-ttu-id="84d7e-292">Die Hardwareanforderungen finden Sie in der Windows-oder Windows Server-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="84d7e-292">See the Windows or Windows Server documentation for the hardware requirements.</span></span> <span data-ttu-id="84d7e-293">App-V fügt keine zusätzlichen Hardwareanforderungen hinzu.</span><span class="sxs-lookup"><span data-stu-id="84d7e-293">App-V adds no additional hardware requirements.</span></span>

## <a href="" id="bkmk-supp-ver-sccm"></a><span data-ttu-id="84d7e-294">Unterstützte Versionen von System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="84d7e-294">Supported versions of System Center Configuration Manager</span></span>

<span data-ttu-id="84d7e-295">Der App-V-Client unterstützt die folgenden Versionen von System Center Configuration Manager:</span><span class="sxs-lookup"><span data-stu-id="84d7e-295">The App-V client supports the following versions of System Center Configuration Manager:</span></span>

-   <span data-ttu-id="84d7e-296">MicrosoftSystemCenter2012 ConfigurationManager</span><span class="sxs-lookup"><span data-stu-id="84d7e-296">MicrosoftSystemCenter2012 ConfigurationManager</span></span>

-   <span data-ttu-id="84d7e-297">System Center 2012 R2 Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="84d7e-297">System Center 2012 R2 Configuration Manager</span></span>

-   <span data-ttu-id="84d7e-298">System Center 2012 R2 Configuration Manager SP1</span><span class="sxs-lookup"><span data-stu-id="84d7e-298">System Center 2012 R2 Configuration Manager SP1</span></span>

<span data-ttu-id="84d7e-299">Die folgende APP-v-und System Center Configuration Manager-Versionsmatrix zeigt alle offiziell unterstützten Kombinationen von App-v und Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="84d7e-299">The following App-V and System Center Configuration Manager version matrix shows all officially supported combinations of App-V and Configuration Manager.</span></span>

> [!NOTE]
> <span data-ttu-id="84d7e-300">Sowohl App-V 4,5 als auch 4,6 haben die Mainstream-Unterstützung beendet.</span><span class="sxs-lookup"><span data-stu-id="84d7e-300">Both App-V 4.5 and 4.6 have exited Mainstream support.</span></span>

<table>
<colgroup>
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="84d7e-301">App-V-Version</span><span class="sxs-lookup"><span data-stu-id="84d7e-301">App-V Version</span></span></th>
<th align="left"><span data-ttu-id="84d7e-302">System Center Configuration Manager 2007</span><span class="sxs-lookup"><span data-stu-id="84d7e-302">System Center Configuration Manager 2007</span></span></th>
<th align="left"><span data-ttu-id="84d7e-303">System Center 2012 Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="84d7e-303">System Center 2012 Configuration Manager</span></span></th>
<th align="left"><span data-ttu-id="84d7e-304">System Center 2012 Configuration Manager SP1</span><span class="sxs-lookup"><span data-stu-id="84d7e-304">System Center 2012 Configuration Manager SP1</span></span></th>
<th align="left"><span data-ttu-id="84d7e-305">System Center 2012 R2 Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="84d7e-305">System Center 2012 R2 Configuration Manager</span></span></th>
<th align="left"><span data-ttu-id="84d7e-306">System Center 2012 R2 Configuration Manager SP1</span><span class="sxs-lookup"><span data-stu-id="84d7e-306">System Center 2012 R2 Configuration Manager SP1</span></span></th>
<th align="left"><span data-ttu-id="84d7e-307">System Center 2012 Configuration Manager SP2</span><span class="sxs-lookup"><span data-stu-id="84d7e-307">System Center 2012 Configuration Manager SP2</span></span></th>
<th align="left"><span data-ttu-id="84d7e-308">System Center Configuration Manager, Version 1511</span><span class="sxs-lookup"><span data-stu-id="84d7e-308">System Center Configuration Manager Version 1511</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="84d7e-309">App-V 5,0 SP3</span><span class="sxs-lookup"><span data-stu-id="84d7e-309">App-V 5.0 SP3</span></span></p></td>
<td align="left"><p><span data-ttu-id="84d7e-310">Nur MSI-Wrapper</span><span class="sxs-lookup"><span data-stu-id="84d7e-310">MSI-Wrapper Only</span></span></p></td>
<td align="left"><p><span data-ttu-id="84d7e-311">Nein</span><span class="sxs-lookup"><span data-stu-id="84d7e-311">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="84d7e-312">2012 SP1 CU4</span><span class="sxs-lookup"><span data-stu-id="84d7e-312">2012 SP1 CU4</span></span></p></td>
<td align="left"><p><span data-ttu-id="84d7e-313">2012 R2 CU1</span><span class="sxs-lookup"><span data-stu-id="84d7e-313">2012 R2 CU1</span></span></p></td>
<td align="left"><p><span data-ttu-id="84d7e-314">Ja</span><span class="sxs-lookup"><span data-stu-id="84d7e-314">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="84d7e-315">Ja</span><span class="sxs-lookup"><span data-stu-id="84d7e-315">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="84d7e-316">Ja</span><span class="sxs-lookup"><span data-stu-id="84d7e-316">Yes</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="84d7e-317">App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="84d7e-317">App-V 5.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="84d7e-318">Nur MSI-Wrapper</span><span class="sxs-lookup"><span data-stu-id="84d7e-318">MSI-Wrapper Only</span></span></p></td>
<td align="left"><p><span data-ttu-id="84d7e-319">Nein</span><span class="sxs-lookup"><span data-stu-id="84d7e-319">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="84d7e-320">2012 SP1 CU4</span><span class="sxs-lookup"><span data-stu-id="84d7e-320">2012 SP1 CU4</span></span></p></td>
<td align="left"><p><span data-ttu-id="84d7e-321">2012 R2 CU1</span><span class="sxs-lookup"><span data-stu-id="84d7e-321">2012 R2 CU1</span></span></p></td>
<td align="left"><p><span data-ttu-id="84d7e-322">Ja</span><span class="sxs-lookup"><span data-stu-id="84d7e-322">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="84d7e-323">Ja</span><span class="sxs-lookup"><span data-stu-id="84d7e-323">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="84d7e-324">Ja</span><span class="sxs-lookup"><span data-stu-id="84d7e-324">Yes</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="84d7e-325">Weitere Informationen zur Integration von Configuration Manager in App-v finden Sie unter [Planen der APP-v-Integration in Configuration Manager](https://technet.microsoft.com/library/jj822982.aspx).</span><span class="sxs-lookup"><span data-stu-id="84d7e-325">For more information about how Configuration Manager integrates with App-V, see [Planning for App-V Integration with Configuration Manager](https://technet.microsoft.com/library/jj822982.aspx).</span></span>

## <span data-ttu-id="84d7e-326">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="84d7e-326">Related topics</span></span>

[<span data-ttu-id="84d7e-327">Planen der Bereitstellung von App-V</span><span class="sxs-lookup"><span data-stu-id="84d7e-327">Planning to Deploy App-V</span></span>](planning-to-deploy-app-v51.md)

[<span data-ttu-id="84d7e-328">Voraussetzungen für App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="84d7e-328">App-V 5.1 Prerequisites</span></span>](app-v-51-prerequisites.md)
