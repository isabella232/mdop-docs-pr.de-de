---
title: Unterstützte App-V 5.0-Konfigurationen
description: Unterstützte App-V 5.0-Konfigurationen
author: dansimp
ms.assetid: 3787ff63-7ce7-45a8-8f01-81b4b6dced34
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 60236743d2a6b418ca7f4705168a7bf064b82156
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805990"
---
# <span data-ttu-id="8057d-103">Unterstützte App-V 5.0-Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="8057d-103">App-V 5.0 Supported Configurations</span></span>


<span data-ttu-id="8057d-104">In diesem Thema werden die Anforderungen beschrieben, die erforderlich sind, um Microsoft Application Virtualization (App-V) 5,0 in Ihrer Umgebung zu installieren und auszuführen.</span><span class="sxs-lookup"><span data-stu-id="8057d-104">This topic specifies the requirements that are necessary to install and run Microsoft Application Virtualization (App-V) 5.0 in your environment.</span></span>

**<span data-ttu-id="8057d-105">Wichtig</span><span class="sxs-lookup"><span data-stu-id="8057d-105">Important</span></span>**  
<span data-ttu-id="8057d-106">**Die unterstützten Konfigurationen in diesem Artikel gelten nur für App-V 5,0**.</span><span class="sxs-lookup"><span data-stu-id="8057d-106">**The supported configurations in this article apply only to App-V 5.0**.</span></span> <span data-ttu-id="8057d-107">Informationen zu unterstützten Konfigurationen, die für App-V 5,0-Service Packs gelten, finden Sie auf den folgenden Webseiten:</span><span class="sxs-lookup"><span data-stu-id="8057d-107">For supported configurations that apply to App-V 5.0 Service Packs, see the following web pages:</span></span>

-   [<span data-ttu-id="8057d-108">Neuigkeiten in App-V 5.0 SP1</span><span class="sxs-lookup"><span data-stu-id="8057d-108">What's new in App-V 5.0 SP1</span></span>](whats-new-in-app-v-50-sp1.md)

-   [<span data-ttu-id="8057d-109">Informationen zu App-V 5.0 SP2</span><span class="sxs-lookup"><span data-stu-id="8057d-109">About App-V 5.0 SP2</span></span>](about-app-v-50-sp2.md)

-   [<span data-ttu-id="8057d-110">Unterstützte App-V 5.0 SP3-Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="8057d-110">App-V 5.0 SP3 Supported Configurations</span></span>](app-v-50-sp3-supported-configurations.md)



## <a href="" id="---------app-v-5-0-server-system-requirements"></a> <span data-ttu-id="8057d-111">Systemanforderungen für App-V 5,0 Server</span><span class="sxs-lookup"><span data-stu-id="8057d-111">App-V 5.0 server system requirements</span></span>


**<span data-ttu-id="8057d-112">Wichtig</span><span class="sxs-lookup"><span data-stu-id="8057d-112">Important</span></span>**  
<span data-ttu-id="8057d-113">Der App-V 5,0-Server unterstützt die folgenden Szenarien nicht:</span><span class="sxs-lookup"><span data-stu-id="8057d-113">The App-V 5.0 server does not support the following scenarios:</span></span>



-   <span data-ttu-id="8057d-114">Bereitstellung auf einem Computer, auf dem Microsoft Windows Server Core ausgeführt wird</span><span class="sxs-lookup"><span data-stu-id="8057d-114">Deployment to a computer that runs Microsoft Windows Server Core.</span></span>

-   <span data-ttu-id="8057d-115">Bereitstellung auf einem Computer, auf dem eine frühere Version der App-V 5,0-Server Komponenten ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8057d-115">Deployment to a computer that runs a previous version of App-V 5.0 server components.</span></span>

    **<span data-ttu-id="8057d-116">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="8057d-116">Note</span></span>**  
    <span data-ttu-id="8057d-117">Sie können APP-v 5,0 nebeneinander mit dem App-v 4,5 Lightweight Streaming Server (LWS)-Server installieren.</span><span class="sxs-lookup"><span data-stu-id="8057d-117">You can install App-V 5.0 side-by-side with the App-V 4.5 Lightweight Streaming Server (LWS) server only.</span></span> <span data-ttu-id="8057d-118">Die Bereitstellung von App-v 5,0 nebeneinander mit dem App-v 4,5 Application Virtualization Management Service (HWS)-Server wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8057d-118">Deployment of App-V 5.0 side-by-side with the App-V 4.5 Application Virtualization Management Service (HWS) server is not supported.</span></span>



-   <span data-ttu-id="8057d-119">Bereitstellung auf einem Computer, auf dem Microsoft SQL Server Express Edition ausgeführt wird</span><span class="sxs-lookup"><span data-stu-id="8057d-119">Deployment to a computer that runs Microsoft SQL Server Express edition.</span></span>

-   <span data-ttu-id="8057d-120">Remote Bereitstellung der Verwaltungsserver-Datenbank oder der Berichtsdatenbank</span><span class="sxs-lookup"><span data-stu-id="8057d-120">Remote deployment of the management server database or the reporting database.</span></span> <span data-ttu-id="8057d-121">Das Installationsprogramm muss direkt auf dem Computer ausgeführt werden, auf dem Microsoft SQL ausgeführt wird, damit die Datenbankinstallation erfolgreich durchgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="8057d-121">The installer must be run directly on the computer running Microsoft SQL for the database installation to succeed.</span></span>

-   <span data-ttu-id="8057d-122">Bereitstellung auf einem Domänencontroller.</span><span class="sxs-lookup"><span data-stu-id="8057d-122">Deployment to a domain controller.</span></span>

-   <span data-ttu-id="8057d-123">Kurze Pfade werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8057d-123">Short paths are not supported.</span></span> <span data-ttu-id="8057d-124">Wenn Sie einen kurzen Pfad verwenden möchten, müssen Sie einen neuen Datenträger erstellen.</span><span class="sxs-lookup"><span data-stu-id="8057d-124">If you plan to use a short path you must create a new volume.</span></span>

### <span data-ttu-id="8057d-125">Betriebssystemanforderungen für Management Server</span><span class="sxs-lookup"><span data-stu-id="8057d-125">Management Server operating system requirements</span></span>

<span data-ttu-id="8057d-126">In der folgenden Tabelle sind die Betriebssysteme aufgeführt, die für die Installation des App-V 5,0-Verwaltungsservers unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="8057d-126">The following table lists the operating systems that are supported for the App-V 5.0 management server installation.</span></span>

**<span data-ttu-id="8057d-127">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="8057d-127">Note</span></span>**  
<span data-ttu-id="8057d-128">Microsoft bietet Unterstützung für das aktuelle Service Pack und in einigen Fällen das unmittelbar vorhergehende Service Pack.</span><span class="sxs-lookup"><span data-stu-id="8057d-128">Microsoft provides support for the current service pack and, in some cases, the immediately preceding service pack.</span></span> <span data-ttu-id="8057d-129">Informationen zu den Support Zeitachsen für Ihr Produkt finden Sie unter [unterstützte Service Packs für Lebenszyklen](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span><span class="sxs-lookup"><span data-stu-id="8057d-129">To find the support timelines for your product, see the [Lifecycle Supported Service Packs](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span></span> <span data-ttu-id="8057d-130">Weitere Informationen zur Microsoft Support Lifecycle-Richtlinie finden Sie in den [FAQ zu Microsoft Support Lifecycle Support Policy](https://go.microsoft.com/fwlink/p/?LinkId=31976).</span><span class="sxs-lookup"><span data-stu-id="8057d-130">For additional information about Microsoft Support Lifecycle Policy, see [Microsoft Support Lifecycle Support Policy FAQ](https://go.microsoft.com/fwlink/p/?LinkId=31976).</span></span>



<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="8057d-131">Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="8057d-131">Operating system</span></span></th>
<th align="left"><span data-ttu-id="8057d-132">Edition</span><span class="sxs-lookup"><span data-stu-id="8057d-132">Edition</span></span></th>
<th align="left"><span data-ttu-id="8057d-133">Service Pack</span><span class="sxs-lookup"><span data-stu-id="8057d-133">Service pack</span></span></th>
<th align="left"><span data-ttu-id="8057d-134">System Architektur</span><span class="sxs-lookup"><span data-stu-id="8057d-134">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8057d-135">Microsoft Windows Server 2008 (Standard, Enterprise, Datacenter oder Web Server)</span><span class="sxs-lookup"><span data-stu-id="8057d-135">Microsoft Windows Server 2008 (Standard, Enterprise, Datacenter, or Web Server)</span></span></p></td>
<td align="left"><p><span data-ttu-id="8057d-136">R2</span><span class="sxs-lookup"><span data-stu-id="8057d-136">R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="8057d-137">SP1 und höher</span><span class="sxs-lookup"><span data-stu-id="8057d-137">SP1 and higher</span></span></p></td>
<td align="left"><p><span data-ttu-id="8057d-138">64Bit</span><span class="sxs-lookup"><span data-stu-id="8057d-138">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8057d-139">Microsoft Windows Server 2012 (Standard, Datacenter)</span><span class="sxs-lookup"><span data-stu-id="8057d-139">Microsoft Windows Server 2012 (Standard, Datacenter)</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"></td>
<td align="left"><p><span data-ttu-id="8057d-140">64Bit</span><span class="sxs-lookup"><span data-stu-id="8057d-140">64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8057d-141">Microsoft Windows Server 2012 (Standard, Datacenter)</span><span class="sxs-lookup"><span data-stu-id="8057d-141">Microsoft Windows Server 2012 (Standard, Datacenter)</span></span></p></td>
<td align="left"><p><span data-ttu-id="8057d-142">R2</span><span class="sxs-lookup"><span data-stu-id="8057d-142">R2</span></span></p></td>
<td align="left"></td>
<td align="left"><p><span data-ttu-id="8057d-143">64Bit</span><span class="sxs-lookup"><span data-stu-id="8057d-143">64-bit</span></span></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="8057d-144">Wichtig</span><span class="sxs-lookup"><span data-stu-id="8057d-144">Important</span></span>**  
<span data-ttu-id="8057d-145">Die Bereitstellung der Verwaltungsserverrolle auf einem Computer mit aktivierter Remote Desktop Freigabe (RDS) wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8057d-145">Deployment of the management server role to a computer with Remote Desktop Sharing (RDS) enabled is not supported.</span></span>



### <a href="" id="management-server-hardware-requirements-"></a><span data-ttu-id="8057d-146">Hardwareanforderungen für den Verwaltungs Server</span><span class="sxs-lookup"><span data-stu-id="8057d-146">Management Server hardware requirements</span></span>

-   <span data-ttu-id="8057d-147">Prozessor – 1,4 GHz oder schneller, 64-Bit (x64)-Prozessor</span><span class="sxs-lookup"><span data-stu-id="8057d-147">Processor—1.4 GHz or faster, 64-bit (x64) processor</span></span>

-   <span data-ttu-id="8057d-148">RAM – 1 GB RAM (64-Bit)</span><span class="sxs-lookup"><span data-stu-id="8057d-148">RAM— 1 GB RAM (64-bit)</span></span>

-   <span data-ttu-id="8057d-149">Speicherplatz – 200 MB verfügbarer Festplattenspeicherplatz, nicht einschließlich des Inhaltsverzeichnisses.</span><span class="sxs-lookup"><span data-stu-id="8057d-149">Disk space—200 MB available hard disk space, not including the content directory.</span></span>

### <span data-ttu-id="8057d-150">Betriebssystemanforderungen für Veröffentlichungs Server</span><span class="sxs-lookup"><span data-stu-id="8057d-150">Publishing Server operating system requirements</span></span>

<span data-ttu-id="8057d-151">In der folgenden Tabelle sind die Betriebssysteme aufgeführt, die für die Installation des App-V 5,0-Publishing Servers unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="8057d-151">The following table lists the operating systems that are supported for the App-V 5.0 publishing server installation.</span></span>

**<span data-ttu-id="8057d-152">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="8057d-152">Note</span></span>**  
<span data-ttu-id="8057d-153">Microsoft bietet Unterstützung für das aktuelle Service Pack und in einigen Fällen das unmittelbar vorhergehende Service Pack.</span><span class="sxs-lookup"><span data-stu-id="8057d-153">Microsoft provides support for the current service pack and, in some cases, the immediately preceding service pack.</span></span> <span data-ttu-id="8057d-154">Informationen zu den Support Zeitachsen für Ihr Produkt finden Sie unter [unterstützte Service Packs für Lebenszyklen](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span><span class="sxs-lookup"><span data-stu-id="8057d-154">To find the support timelines for your product, see the [Lifecycle Supported Service Packs](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span></span> <span data-ttu-id="8057d-155">Weitere Informationen zur Microsoft Support Lifecycle-Richtlinie finden Sie in den [FAQ zu Microsoft Support Lifecycle Support Policy](https://go.microsoft.com/fwlink/p/?LinkId=31976).</span><span class="sxs-lookup"><span data-stu-id="8057d-155">For additional information about Microsoft Support Lifecycle Policy, see [Microsoft Support Lifecycle Support Policy FAQ](https://go.microsoft.com/fwlink/p/?LinkId=31976).</span></span>



<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="8057d-156">Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="8057d-156">Operating system</span></span></th>
<th align="left"><span data-ttu-id="8057d-157">Edition</span><span class="sxs-lookup"><span data-stu-id="8057d-157">Edition</span></span></th>
<th align="left"><span data-ttu-id="8057d-158">Service Pack</span><span class="sxs-lookup"><span data-stu-id="8057d-158">Service pack</span></span></th>
<th align="left"><span data-ttu-id="8057d-159">System Architektur</span><span class="sxs-lookup"><span data-stu-id="8057d-159">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8057d-160">Microsoft Windows Server 2008 (Standard, Enterprise, Datacenter oder Web Server)</span><span class="sxs-lookup"><span data-stu-id="8057d-160">Microsoft Windows Server 2008 (Standard, Enterprise, Datacenter, or Web Server)</span></span></p></td>
<td align="left"><p><span data-ttu-id="8057d-161">R2</span><span class="sxs-lookup"><span data-stu-id="8057d-161">R2</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="8057d-162">64Bit</span><span class="sxs-lookup"><span data-stu-id="8057d-162">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8057d-163">Microsoft Windows Server 2012 (Standard, Datacenter)</span><span class="sxs-lookup"><span data-stu-id="8057d-163">Microsoft Windows Server 2012 (Standard, Datacenter)</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"></td>
<td align="left"><p><span data-ttu-id="8057d-164">64Bit</span><span class="sxs-lookup"><span data-stu-id="8057d-164">64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8057d-165">Microsoft Windows Server 2012 (Standard, Datacenter)</span><span class="sxs-lookup"><span data-stu-id="8057d-165">Microsoft Windows Server 2012 (Standard, Datacenter)</span></span></p></td>
<td align="left"><p><span data-ttu-id="8057d-166">R2</span><span class="sxs-lookup"><span data-stu-id="8057d-166">R2</span></span></p></td>
<td align="left"></td>
<td align="left"><p><span data-ttu-id="8057d-167">64Bit</span><span class="sxs-lookup"><span data-stu-id="8057d-167">64-bit</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="publishing-server-hardware-requirements-"></a><span data-ttu-id="8057d-168">Hardwareanforderungen für Veröffentlichungs Server</span><span class="sxs-lookup"><span data-stu-id="8057d-168">Publishing Server hardware requirements</span></span>

-   <span data-ttu-id="8057d-169">Prozessor – 1,4 GHz oder schneller.</span><span class="sxs-lookup"><span data-stu-id="8057d-169">Processor—1.4 GHz or faster.</span></span> <span data-ttu-id="8057d-170">64-Bit (x64)-Prozessor</span><span class="sxs-lookup"><span data-stu-id="8057d-170">64-bit (x64) processor</span></span>

-   <span data-ttu-id="8057d-171">RAM – 2 GB RAM (64-Bit)</span><span class="sxs-lookup"><span data-stu-id="8057d-171">RAM— 2 GB RAM (64-bit)</span></span>

-   <span data-ttu-id="8057d-172">Speicherplatz – 200 MB verfügbarer Speicherplatz auf der Festplatte.</span><span class="sxs-lookup"><span data-stu-id="8057d-172">Disk space—200 MB available hard disk space.</span></span> <span data-ttu-id="8057d-173">nicht einschließlich Inhaltsverzeichnis</span><span class="sxs-lookup"><span data-stu-id="8057d-173">not including content directory</span></span>

### <span data-ttu-id="8057d-174">Anforderungen des Reporting Server-Betriebssystems</span><span class="sxs-lookup"><span data-stu-id="8057d-174">Reporting Server operating system requirements</span></span>

<span data-ttu-id="8057d-175">In der folgenden Tabelle sind die Betriebssysteme aufgeführt, die für die App-V 5,0 Reporting Server-Installation unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="8057d-175">The following table lists the operating systems that are supported for the App-V 5.0 reporting server installation.</span></span>

**<span data-ttu-id="8057d-176">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="8057d-176">Note</span></span>**  
<span data-ttu-id="8057d-177">Microsoft bietet Unterstützung für das aktuelle Service Pack und in einigen Fällen das unmittelbar vorhergehende Service Pack.</span><span class="sxs-lookup"><span data-stu-id="8057d-177">Microsoft provides support for the current service pack and, in some cases, the immediately preceding service pack.</span></span> <span data-ttu-id="8057d-178">Informationen zu den Support Zeitachsen für Ihr Produkt finden Sie unter [unterstützte Service Packs für Lebenszyklen](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span><span class="sxs-lookup"><span data-stu-id="8057d-178">To find the support timelines for your product, see the [Lifecycle Supported Service Packs](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span></span> <span data-ttu-id="8057d-179">Weitere Informationen zur Microsoft Support Lifecycle-Richtlinie finden Sie in den [FAQ zu Microsoft Support Lifecycle Support Policy](https://go.microsoft.com/fwlink/p/?LinkId=31976).</span><span class="sxs-lookup"><span data-stu-id="8057d-179">For additional information about Microsoft Support Lifecycle Policy, see [Microsoft Support Lifecycle Support Policy FAQ](https://go.microsoft.com/fwlink/p/?LinkId=31976).</span></span>



<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="8057d-180">Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="8057d-180">Operating system</span></span></th>
<th align="left"><span data-ttu-id="8057d-181">Edition</span><span class="sxs-lookup"><span data-stu-id="8057d-181">Edition</span></span></th>
<th align="left"><span data-ttu-id="8057d-182">Service Pack</span><span class="sxs-lookup"><span data-stu-id="8057d-182">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="8057d-183">System Architektur</span><span class="sxs-lookup"><span data-stu-id="8057d-183">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8057d-184">Microsoft Windows Server 2008 (Standard, Enterprise, Datacenter oder Web Server)</span><span class="sxs-lookup"><span data-stu-id="8057d-184">Microsoft Windows Server 2008 (Standard, Enterprise, Datacenter, or Web Server)</span></span></p></td>
<td align="left"><p><span data-ttu-id="8057d-185">R2</span><span class="sxs-lookup"><span data-stu-id="8057d-185">R2</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="8057d-186">64Bit</span><span class="sxs-lookup"><span data-stu-id="8057d-186">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8057d-187">Microsoft Windows Server 2012 (Standard, Datacenter)</span><span class="sxs-lookup"><span data-stu-id="8057d-187">Microsoft Windows Server 2012 (Standard, Datacenter)</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"></td>
<td align="left"><p><span data-ttu-id="8057d-188">64Bit</span><span class="sxs-lookup"><span data-stu-id="8057d-188">64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8057d-189">Microsoft Windows Server 2012 (Standard, Datacenter)</span><span class="sxs-lookup"><span data-stu-id="8057d-189">Microsoft Windows Server 2012 (Standard, Datacenter)</span></span></p></td>
<td align="left"><p><span data-ttu-id="8057d-190">R2</span><span class="sxs-lookup"><span data-stu-id="8057d-190">R2</span></span></p></td>
<td align="left"></td>
<td align="left"><p><span data-ttu-id="8057d-191">64Bit</span><span class="sxs-lookup"><span data-stu-id="8057d-191">64-bit</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="reporting-server-hardware-requirements-"></a><span data-ttu-id="8057d-192">Hardwareanforderungen für den Berichts Server</span><span class="sxs-lookup"><span data-stu-id="8057d-192">Reporting Server hardware requirements</span></span>

-   <span data-ttu-id="8057d-193">Prozessor – 1,4 GHz oder schneller.</span><span class="sxs-lookup"><span data-stu-id="8057d-193">Processor—1.4 GHz or faster.</span></span> <span data-ttu-id="8057d-194">64-Bit (x64)-Prozessor</span><span class="sxs-lookup"><span data-stu-id="8057d-194">64-bit (x64) processor</span></span>

-   <span data-ttu-id="8057d-195">RAM – 2 GB RAM (64-Bit)</span><span class="sxs-lookup"><span data-stu-id="8057d-195">RAM—2 GB RAM (64-bit)</span></span>

-   <span data-ttu-id="8057d-196">Speicherplatz – 200 MB verfügbarer Festplattenspeicherplatz</span><span class="sxs-lookup"><span data-stu-id="8057d-196">Disk space—200 MB available hard disk space</span></span>

### <a href="" id="sql-server-database-requirements-"></a><span data-ttu-id="8057d-197">SQL Server-Datenbankanforderungen</span><span class="sxs-lookup"><span data-stu-id="8057d-197">SQL Server database requirements</span></span>

<span data-ttu-id="8057d-198">In der folgenden Tabelle sind die SQL Server-Versionen aufgeführt, die für die App-V 5,0-Datenbank und die Server Installation unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="8057d-198">The following table lists the SQL Server versions that are supported for the App-V 5.0 database and server installation.</span></span>

<table>
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="8057d-199">App-V 5,0-Servertyp</span><span class="sxs-lookup"><span data-stu-id="8057d-199">App-V 5.0 server type</span></span></th>
<th align="left"><span data-ttu-id="8057d-200">SQL Server-Version</span><span class="sxs-lookup"><span data-stu-id="8057d-200">SQL Server version</span></span></th>
<th align="left"><span data-ttu-id="8057d-201">Edition</span><span class="sxs-lookup"><span data-stu-id="8057d-201">Edition</span></span></th>
<th align="left"><span data-ttu-id="8057d-202">Service Pack</span><span class="sxs-lookup"><span data-stu-id="8057d-202">Service pack</span></span></th>
<th align="left"><span data-ttu-id="8057d-203">System Architektur</span><span class="sxs-lookup"><span data-stu-id="8057d-203">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8057d-204">Verwaltung/Berichterstattung</span><span class="sxs-lookup"><span data-stu-id="8057d-204">Management / Reporting</span></span></p></td>
<td align="left"><p><span data-ttu-id="8057d-205">Microsoft SQL Server 2008</span><span class="sxs-lookup"><span data-stu-id="8057d-205">Microsoft SQL Server 2008</span></span></p>
<p><span data-ttu-id="8057d-206">(Standard, Enterprise, Datacenter oder Developer Edition mit folgendem Feature: <strong> Datenbankmodul </strong> -Dienste.)</span><span class="sxs-lookup"><span data-stu-id="8057d-206">(Standard, Enterprise, Datacenter, or the Developer Edition with the following feature: <strong>Database Engine Services</strong>.)</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="8057d-207">32 Bit oder 64 Bit</span><span class="sxs-lookup"><span data-stu-id="8057d-207">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8057d-208">Verwaltung/Berichterstattung</span><span class="sxs-lookup"><span data-stu-id="8057d-208">Management / Reporting</span></span></p></td>
<td align="left"><p><span data-ttu-id="8057d-209">Microsoft SQL Server 2008</span><span class="sxs-lookup"><span data-stu-id="8057d-209">Microsoft SQL Server 2008</span></span> </p>
<p><span data-ttu-id="8057d-210">(Standard, Enterprise, Datacenter oder Developer Edition mit folgendem Feature: <strong> Datenbankmodul </strong> -Dienste.)</span><span class="sxs-lookup"><span data-stu-id="8057d-210">(Standard, Enterprise, Datacenter, or the Developer Edition with the following feature: <strong>Database Engine Services</strong>.)</span></span></p></td>
<td align="left"><p><span data-ttu-id="8057d-211">R2</span><span class="sxs-lookup"><span data-stu-id="8057d-211">R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="8057d-212">SP2</span><span class="sxs-lookup"><span data-stu-id="8057d-212">SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="8057d-213">32 Bit oder 64 Bit</span><span class="sxs-lookup"><span data-stu-id="8057d-213">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8057d-214">Verwaltung/Berichterstattung</span><span class="sxs-lookup"><span data-stu-id="8057d-214">Management / Reporting</span></span></p></td>
<td align="left"><p><span data-ttu-id="8057d-215">Microsoft SQL Server 2012</span><span class="sxs-lookup"><span data-stu-id="8057d-215">Microsoft SQL Server 2012</span></span></p>
<p><span data-ttu-id="8057d-216">(Standard, Enterprise, Datacenter oder Developer Edition mit folgendem Feature: <strong> Datenbankmodul </strong> -Dienste.)</span><span class="sxs-lookup"><span data-stu-id="8057d-216">(Standard, Enterprise, Datacenter, or the Developer Edition with the following feature: <strong>Database Engine Services</strong>.)</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="8057d-217">32 Bit oder 64 Bit</span><span class="sxs-lookup"><span data-stu-id="8057d-217">32-bit or 64-bit</span></span></p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-client-supp-cfgs"></a> <span data-ttu-id="8057d-218">App-V 5,0-Clientsystemanforderungen</span><span class="sxs-lookup"><span data-stu-id="8057d-218">App-V 5.0 client system requirements</span></span>


<span data-ttu-id="8057d-219">In der folgenden Tabelle sind die Betriebssysteme aufgeführt, die für die App-V 5,0-Clientinstallation unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="8057d-219">The following table lists the operating systems that are supported for the App-V 5.0 client installation.</span></span>

**<span data-ttu-id="8057d-220">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="8057d-220">Note</span></span>**  
<span data-ttu-id="8057d-221">Microsoft bietet Unterstützung für das aktuelle Service Pack und in einigen Fällen das unmittelbar vorhergehende Service Pack.</span><span class="sxs-lookup"><span data-stu-id="8057d-221">Microsoft provides support for the current service pack and, in some cases, the immediately preceding service pack.</span></span> <span data-ttu-id="8057d-222">Informationen zu den Support Zeitachsen für Ihr Produkt finden Sie unter [unterstützte Service Packs für Lebenszyklen](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span><span class="sxs-lookup"><span data-stu-id="8057d-222">To find the support timelines for your product, see the [Lifecycle Supported Service Packs](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span></span> <span data-ttu-id="8057d-223">Weitere Informationen zur Microsoft Support Lifecycle-Richtlinie finden Sie in den [FAQ zu Microsoft Support Lifecycle Support Policy](https://go.microsoft.com/fwlink/p/?LinkId=31976).</span><span class="sxs-lookup"><span data-stu-id="8057d-223">For additional information about Microsoft Support Lifecycle Policy, see [Microsoft Support Lifecycle Support Policy FAQ](https://go.microsoft.com/fwlink/p/?LinkId=31976).</span></span>



<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="8057d-224">Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="8057d-224">Operating system</span></span></th>
<th align="left"><span data-ttu-id="8057d-225">Service Pack</span><span class="sxs-lookup"><span data-stu-id="8057d-225">Service pack</span></span></th>
<th align="left"><span data-ttu-id="8057d-226">System Architektur</span><span class="sxs-lookup"><span data-stu-id="8057d-226">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8057d-227">Microsoft Windows 7</span><span class="sxs-lookup"><span data-stu-id="8057d-227">Microsoft Windows 7</span></span></p></td>
<td align="left"><p><span data-ttu-id="8057d-228">SP1</span><span class="sxs-lookup"><span data-stu-id="8057d-228">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="8057d-229">32 Bit oder 64 Bit</span><span class="sxs-lookup"><span data-stu-id="8057d-229">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8057d-230">Microsoft Windows 8</span><span class="sxs-lookup"><span data-stu-id="8057d-230">Microsoft Windows 8</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="8057d-231">32 Bit oder 64 Bit</span><span class="sxs-lookup"><span data-stu-id="8057d-231">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><div class="alert">
<strong><span data-ttu-id="8057d-232">Wichtig</span><span class="sxs-lookup"><span data-stu-id="8057d-232">Important</span></span></strong><br/><p><span data-ttu-id="8057d-233">Windows 8,1 wird nur von App-V 5,0 SP2 unterstützt</span><span class="sxs-lookup"><span data-stu-id="8057d-233">Windows 8.1 is only supported by App-V 5.0 SP2</span></span></p>
</div>
<div>

</div>
<p><span data-ttu-id="8057d-234">Windows8.1</span><span class="sxs-lookup"><span data-stu-id="8057d-234">Windows 8.1</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="8057d-235">32 Bit oder 64 Bit</span><span class="sxs-lookup"><span data-stu-id="8057d-235">32-bit or 64-bit</span></span></p></td>
</tr>
</tbody>
</table>



<span data-ttu-id="8057d-236">Die folgenden App-V-Client Installationsszenarien werden nicht unterstützt, es sei denn, es wird angegeben:</span><span class="sxs-lookup"><span data-stu-id="8057d-236">The following App-V client installation scenarios are not supported, except as noted:</span></span>

-   <span data-ttu-id="8057d-237">Computer, auf denen Windows Server ausgeführt wird</span><span class="sxs-lookup"><span data-stu-id="8057d-237">Computers that run Windows Server</span></span>

-   <span data-ttu-id="8057d-238">Computer, auf denen App-V 4,6 SP1 oder frühere Versionen ausgeführt werden</span><span class="sxs-lookup"><span data-stu-id="8057d-238">Computers that run App-V 4.6 SP1 or earlier versions</span></span>

-   <span data-ttu-id="8057d-239">Der App-V 5,0-Client für Remote Desktop Dienste wird nur für RDS-fähige Server unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8057d-239">The App-V 5.0 Remote Desktop services client is supported only for RDS-enabled servers</span></span>

### <a href="" id="client-hardware-requirements-"></a><span data-ttu-id="8057d-240">Client Hardwareanforderungen</span><span class="sxs-lookup"><span data-stu-id="8057d-240">Client hardware requirements</span></span>

<span data-ttu-id="8057d-241">In der folgenden Liste wird die unterstützte Hardwarekonfiguration für die App-V 5,0-Clientinstallation angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8057d-241">The following list displays the supported hardware configuration for the App-V 5.0 client installation.</span></span>

-   <span data-ttu-id="8057d-242">Prozessor – 1,4 GHz oder schneller 32-Bit (x86) oder 64-Bit (x64)-Prozessor</span><span class="sxs-lookup"><span data-stu-id="8057d-242">Processor— 1.4 GHz or faster 32-bit (x86) or 64-bit (x64) processor</span></span>

-   <span data-ttu-id="8057d-243">RAM – 1 GB (32-Bit) oder 2 GB (64-Bit)</span><span class="sxs-lookup"><span data-stu-id="8057d-243">RAM— 1 GB (32-bit) or 2 GB (64-bit)</span></span>

-   <span data-ttu-id="8057d-244">Datenträger – 100 MB für die Installation, nicht einschließlich des von virtualisierten Anwendungen verwendeten Speicherplatzes.</span><span class="sxs-lookup"><span data-stu-id="8057d-244">Disk— 100 MB for installation, not including the disk space that is used by virtualized applications.</span></span>

## <a href="" id="---------app-v-5-0-remote-desktop-client-system-requirements"></a> <span data-ttu-id="8057d-245">App-V 5,0-Systemanforderungen für Remote Desktop Client</span><span class="sxs-lookup"><span data-stu-id="8057d-245">App-V 5.0 Remote Desktop client system requirements</span></span>


<span data-ttu-id="8057d-246">In der folgenden Tabelle sind die Betriebssysteme aufgeführt, die für die App-V 5,0-Remote Desktop Client-Installation unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="8057d-246">The following table lists the operating systems that are supported for App-V 5.0 Remote Desktop client installation.</span></span>

**<span data-ttu-id="8057d-247">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="8057d-247">Note</span></span>**  
<span data-ttu-id="8057d-248">Microsoft bietet Unterstützung für das aktuelle Service Pack und in einigen Fällen das unmittelbar vorhergehende Service Pack.</span><span class="sxs-lookup"><span data-stu-id="8057d-248">Microsoft provides support for the current service pack and, in some cases, the immediately preceding service pack.</span></span> <span data-ttu-id="8057d-249">Informationen zu den Support Zeitachsen für Ihr Produkt finden Sie unter [unterstützte Service Packs für Lebenszyklen](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span><span class="sxs-lookup"><span data-stu-id="8057d-249">To find the support timelines for your product, see the [Lifecycle Supported Service Packs](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span></span> <span data-ttu-id="8057d-250">Weitere Informationen zur Microsoft Support Lifecycle-Richtlinie finden Sie in den [FAQ zu Microsoft Support Lifecycle Support Policy](https://go.microsoft.com/fwlink/p/?LinkId=31976).</span><span class="sxs-lookup"><span data-stu-id="8057d-250">For additional information about Microsoft Support Lifecycle Policy, see [Microsoft Support Lifecycle Support Policy FAQ](https://go.microsoft.com/fwlink/p/?LinkId=31976).</span></span>



<span data-ttu-id="8057d-251">Betriebssystem Edition-Service Pack Microsoft Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8057d-251">Operating system Edition Service pack Microsoft Windows Server 2008</span></span>

<span data-ttu-id="8057d-252">R2</span><span class="sxs-lookup"><span data-stu-id="8057d-252">R2</span></span>

<span data-ttu-id="8057d-253">SP1</span><span class="sxs-lookup"><span data-stu-id="8057d-253">SP1</span></span>

<span data-ttu-id="8057d-254">Microsoft Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8057d-254">Microsoft Windows Server 2012</span></span>

**<span data-ttu-id="8057d-255">Wichtig</span><span class="sxs-lookup"><span data-stu-id="8057d-255">Important</span></span>**  
<span data-ttu-id="8057d-256">Windows Server 2012 R2 wird nur von App-V 5,0 SP2 unterstützt</span><span class="sxs-lookup"><span data-stu-id="8057d-256">Windows Server 2012 R2 is only supported by App-V 5.0 SP2</span></span>



<span data-ttu-id="8057d-257">Microsoft Windows Server 2012 (Standard, Datacenter)</span><span class="sxs-lookup"><span data-stu-id="8057d-257">Microsoft Windows Server 2012 (Standard, Datacenter)</span></span>

<span data-ttu-id="8057d-258">R2</span><span class="sxs-lookup"><span data-stu-id="8057d-258">R2</span></span>

<span data-ttu-id="8057d-259">64Bit</span><span class="sxs-lookup"><span data-stu-id="8057d-259">64-bit</span></span>



### <a href="" id="remote-desktop-client-hardware-requirements-"></a><span data-ttu-id="8057d-260">Hardwareanforderungen für Remote Desktop Client</span><span class="sxs-lookup"><span data-stu-id="8057d-260">Remote Desktop client hardware requirements</span></span>

<span data-ttu-id="8057d-261">In der folgenden Liste wird die unterstützte Hardwarekonfiguration für die App-V 5,0-Clientinstallation angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8057d-261">The following list displays the supported hardware configuration for the App-V 5.0 client installation.</span></span>

-   <span data-ttu-id="8057d-262">Prozessor – 1,4 GHz oder schneller 32-Bit (x86) oder 64-Bit (x64)-Prozessor</span><span class="sxs-lookup"><span data-stu-id="8057d-262">Processor— 1.4 GHz or faster 32-bit (x86) or 64-bit (x64) processor</span></span>

-   <span data-ttu-id="8057d-263">RAM – 1 GB (32-Bit) oder 2 GB (64-Bit)</span><span class="sxs-lookup"><span data-stu-id="8057d-263">RAM— 1 GB (32-bit) or 2 GB (64-bit)</span></span>

-   <span data-ttu-id="8057d-264">Datenträger – 100 MB für die Installation, nicht einschließlich des von virtualisierten Anwendungen verwendeten Speicherplatzes.</span><span class="sxs-lookup"><span data-stu-id="8057d-264">Disk— 100 MB for installation, not including the disk space that is used by virtualized applications.</span></span>

## <a href="" id="---------app-v-5-0-sequencer-system-requirements"></a> <span data-ttu-id="8057d-265">Systemanforderungen für App-V 5,0-Sequenzer</span><span class="sxs-lookup"><span data-stu-id="8057d-265">App-V 5.0 Sequencer system requirements</span></span>


<span data-ttu-id="8057d-266">In der folgenden Tabelle sind die Betriebssysteme aufgeführt, die für die Installation von App-V 5,0 Sequencer unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="8057d-266">The following table lists the operating systems that are supported for App-V 5.0 Sequencer installation.</span></span>

**<span data-ttu-id="8057d-267">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="8057d-267">Note</span></span>**  
<span data-ttu-id="8057d-268">Microsoft bietet Unterstützung für das aktuelle Service Pack und in einigen Fällen das unmittelbar vorhergehende Service Pack.</span><span class="sxs-lookup"><span data-stu-id="8057d-268">Microsoft provides support for the current service pack and, in some cases, the immediately preceding service pack.</span></span> <span data-ttu-id="8057d-269">Informationen zu den Support Zeitachsen für Ihr Produkt finden Sie unter [unterstützte Service Packs für Lebenszyklen](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span><span class="sxs-lookup"><span data-stu-id="8057d-269">To find the support timelines for your product, see the [Lifecycle Supported Service Packs](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span></span> <span data-ttu-id="8057d-270">Weitere Informationen zur Microsoft Support Lifecycle-Richtlinie finden Sie in den [FAQ zu Microsoft Support Lifecycle Support Policy](https://go.microsoft.com/fwlink/p/?LinkId=31976).</span><span class="sxs-lookup"><span data-stu-id="8057d-270">For additional information about Microsoft Support Lifecycle Policy, see [Microsoft Support Lifecycle Support Policy FAQ](https://go.microsoft.com/fwlink/p/?LinkId=31976).</span></span>



<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="8057d-271">Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="8057d-271">Operating system</span></span></th>
<th align="left"><span data-ttu-id="8057d-272">Edition</span><span class="sxs-lookup"><span data-stu-id="8057d-272">Edition</span></span></th>
<th align="left"><span data-ttu-id="8057d-273">Service Pack</span><span class="sxs-lookup"><span data-stu-id="8057d-273">Service pack</span></span></th>
<th align="left"><span data-ttu-id="8057d-274">System Architektur</span><span class="sxs-lookup"><span data-stu-id="8057d-274">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8057d-275">Microsoft Windows 7</span><span class="sxs-lookup"><span data-stu-id="8057d-275">Microsoft Windows 7</span></span></p></td>
<td align="left"></td>
<td align="left"><p><span data-ttu-id="8057d-276">SP1</span><span class="sxs-lookup"><span data-stu-id="8057d-276">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="8057d-277">32Bit und 64Bit</span><span class="sxs-lookup"><span data-stu-id="8057d-277">32-bit and 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8057d-278">Microsoft Windows 8</span><span class="sxs-lookup"><span data-stu-id="8057d-278">Microsoft Windows 8</span></span></p></td>
<td align="left"></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="8057d-279">32Bit und 64Bit</span><span class="sxs-lookup"><span data-stu-id="8057d-279">32-bit and 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><div class="alert">
<strong><span data-ttu-id="8057d-280">Wichtig</span><span class="sxs-lookup"><span data-stu-id="8057d-280">Important</span></span></strong><br/><p><span data-ttu-id="8057d-281">Windows 8,1 wird nur von App-V 5,0 SP2 unterstützt</span><span class="sxs-lookup"><span data-stu-id="8057d-281">Windows 8.1 is only supported by App-V 5.0 SP2</span></span></p>
</div>
<div>

</div>
<p><span data-ttu-id="8057d-282">Windows8.1</span><span class="sxs-lookup"><span data-stu-id="8057d-282">Windows 8.1</span></span></p></td>
<td align="left"></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="8057d-283">32 Bit oder 64 Bit</span><span class="sxs-lookup"><span data-stu-id="8057d-283">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8057d-284">Microsoft Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8057d-284">Microsoft Windows Server 2008</span></span></p></td>
<td align="left"><p><span data-ttu-id="8057d-285">R2</span><span class="sxs-lookup"><span data-stu-id="8057d-285">R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="8057d-286">SP1</span><span class="sxs-lookup"><span data-stu-id="8057d-286">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="8057d-287">32Bit und 64Bit</span><span class="sxs-lookup"><span data-stu-id="8057d-287">32-bit and 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8057d-288">Microsoft Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8057d-288">Microsoft Windows Server 2012</span></span></p></td>
<td align="left"></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="8057d-289">32Bit und 64Bit</span><span class="sxs-lookup"><span data-stu-id="8057d-289">32-bit and 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><div class="alert">
<strong><span data-ttu-id="8057d-290">Wichtig</span><span class="sxs-lookup"><span data-stu-id="8057d-290">Important</span></span></strong><br/><p><span data-ttu-id="8057d-291">Windows Server 2012 R2 wird nur von App-V 5,0 SP2 unterstützt</span><span class="sxs-lookup"><span data-stu-id="8057d-291">Windows Server 2012 R2 is only supported by App-V 5.0 SP2</span></span></p>
</div>
<div>

</div>
<p><span data-ttu-id="8057d-292">Microsoft Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8057d-292">Microsoft Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="8057d-293">R2</span><span class="sxs-lookup"><span data-stu-id="8057d-293">R2</span></span></p></td>
<td align="left"></td>
<td align="left"><p><span data-ttu-id="8057d-294">64Bit</span><span class="sxs-lookup"><span data-stu-id="8057d-294">64-bit</span></span></p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-supp-ver-sccm"></a><span data-ttu-id="8057d-295">Unterstützte Versionen von System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="8057d-295">Supported versions of System Center Configuration Manager</span></span>


<span data-ttu-id="8057d-296">Sie können den Microsoft System Center 2012-Konfigurations-Manager oder den System Center 2012 R2-Konfigurations-Manager verwenden, um virtuelle App-V-Anwendungen, Berichterstellung und andere Funktionen zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="8057d-296">You can use Microsoft System Center 2012 Configuration Manager or System Center 2012 R2 Configuration Manager to manage App-V virtual applications, reporting, and other functions.</span></span> <span data-ttu-id="8057d-297">In der folgenden Tabelle sind die unterstützten Versionen von Configuration Manager für jede anwendbare Version von App-V aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="8057d-297">The following table lists the supported versions of Configuration Manager for each applicable version of App-V.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="8057d-298">Unterstützte Configuration Manager-Version</span><span class="sxs-lookup"><span data-stu-id="8057d-298">Supported Configuration Manager version</span></span></th>
<th align="left"><span data-ttu-id="8057d-299">App-V-Version</span><span class="sxs-lookup"><span data-stu-id="8057d-299">App-V version</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8057d-300">Microsoft System Center 2012-Konfigurations-Manager</span><span class="sxs-lookup"><span data-stu-id="8057d-300">Microsoft System Center 2012 Configuration Manager</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="8057d-301">App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="8057d-301">App-V 5.0</span></span></p></li>
<li><p><span data-ttu-id="8057d-302">App-V 5,0 SP1</span><span class="sxs-lookup"><span data-stu-id="8057d-302">App-V 5.0 SP1</span></span></p></li>
<li><p><span data-ttu-id="8057d-303">App-V 5,0 SP2</span><span class="sxs-lookup"><span data-stu-id="8057d-303">App-V 5.0 SP2</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8057d-304">System Center 2012 R2 Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="8057d-304">System Center 2012 R2 Configuration Manager</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="8057d-305">App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="8057d-305">App-V 5.0</span></span></p></li>
<li><p><span data-ttu-id="8057d-306">App-V 5,0 SP1</span><span class="sxs-lookup"><span data-stu-id="8057d-306">App-V 5.0 SP1</span></span></p></li>
<li><p><span data-ttu-id="8057d-307">App-V 5,0 SP2</span><span class="sxs-lookup"><span data-stu-id="8057d-307">App-V 5.0 SP2</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>



<span data-ttu-id="8057d-308">Weitere Informationen zur Integration von Configuration Manager in App-v finden Sie unter [Planen der APP-v-Integration in Configuration Manager](https://technet.microsoft.com/library/jj822982.aspx).</span><span class="sxs-lookup"><span data-stu-id="8057d-308">For more information about how Configuration Manager integrates with App-V, see [Planning for App-V Integration with Configuration Manager](https://technet.microsoft.com/library/jj822982.aspx).</span></span>






## <span data-ttu-id="8057d-309">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="8057d-309">Related topics</span></span>


[<span data-ttu-id="8057d-310">Planen der Bereitstellung von App-V</span><span class="sxs-lookup"><span data-stu-id="8057d-310">Planning to Deploy App-V</span></span>](planning-to-deploy-app-v.md)

[<span data-ttu-id="8057d-311">Voraussetzungen für App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="8057d-311">App-V 5.0 Prerequisites</span></span>](app-v-50-prerequisites.md)









