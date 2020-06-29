---
title: Von MBAM 2.0 unterstützte Konfigurationen
description: Von MBAM 2.0 unterstützte Konfigurationen
author: dansimp
ms.assetid: dca63391-39fe-4273-a570-76d0a2f8a0fd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 8f314adcf818c1bdb17b0b239a7469f97fa849e4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810237"
---
# <span data-ttu-id="3da45-103">Von MBAM 2.0 unterstützte Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="3da45-103">MBAM 2.0 Supported Configurations</span></span>


<span data-ttu-id="3da45-104">In diesem Thema werden die Anforderungen zum Installieren und Ausführen von Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) 2,0 in Ihrer Umgebung mithilfe der eigenständigen Topologie angegeben.</span><span class="sxs-lookup"><span data-stu-id="3da45-104">This topic specifies the requirements to install and run Microsoft BitLocker Administration and Monitoring (MBAM) 2.0 in your environment by using the Stand-alone topology.</span></span> <span data-ttu-id="3da45-105">Informationen zu unterstützten Konfigurationen, die für spätere Versionen gelten, finden Sie in der Dokumentation zur jeweiligen Version.</span><span class="sxs-lookup"><span data-stu-id="3da45-105">For supported configurations that apply to later releases, see the documentation for the applicable release.</span></span>

<span data-ttu-id="3da45-106">Wenn Sie beabsichtigen, MBAM 2,0 mithilfe der Configuration Manager-Topologie zu installieren, und eine Liste der Systemanforderungen überprüfen möchten, lesen Sie [Planen der Bereitstellung von MBAM mit Configuration Manager](planning-to-deploy-mbam-with-configuration-manager-2.md).</span><span class="sxs-lookup"><span data-stu-id="3da45-106">If you plan to install MBAM 2.0 by using the Configuration Manager topology and want to review a list of the system requirements, see [Planning to Deploy MBAM with Configuration Manager](planning-to-deploy-mbam-with-configuration-manager-2.md).</span></span>

<span data-ttu-id="3da45-107">Die empfohlene Konfiguration für die Ausführung von MBAM in einer Produktionsumgebung besteht je nach Ihren Skalierbarkeitsanforderungen aus zwei Servern.</span><span class="sxs-lookup"><span data-stu-id="3da45-107">The recommended configuration for running MBAM in a production environment is with two servers, depending on your scalability requirements.</span></span> <span data-ttu-id="3da45-108">Diese Konfiguration unterstützt bis zu 200.000 MBAM-Clients.</span><span class="sxs-lookup"><span data-stu-id="3da45-108">This configuration supports up to 200,000 MBAM clients.</span></span> <span data-ttu-id="3da45-109">Ein Bild und Beschreibungen der eigenständigen MBAM-Serverinfrastruktur finden Sie unter [Architektur auf höherer Ebene für MBAM 2,0](high-level-architecture-for-mbam-20-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="3da45-109">For an image and descriptions of the Stand-alone MBAM server infrastructure, see [High-Level Architecture for MBAM 2.0](high-level-architecture-for-mbam-20-mbam-2.md).</span></span>

<span data-ttu-id="3da45-110">**Hinweis**  Microsoft bietet Unterstützung für das aktuelle Service Pack und in einigen Fällen das unmittelbar vorhergehende Service Pack.</span><span class="sxs-lookup"><span data-stu-id="3da45-110">**Note** Microsoft provides support for the current service pack and, in some cases, the immediately preceding service pack.</span></span> <span data-ttu-id="3da45-111">Informationen zu den Support Zeitachsen für Ihr Produkt finden Sie unter [unterstützte Service Packs für Lebenszyklen](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span><span class="sxs-lookup"><span data-stu-id="3da45-111">To find the support timelines for your product, see the [Lifecycle Supported Service Packs](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span></span> <span data-ttu-id="3da45-112">Weitere Informationen zur Microsoft Support Lifecycle-Richtlinie finden Sie in den [FAQ zu Microsoft Support Lifecycle Support Policy](https://go.microsoft.com/fwlink/p/?LinkId=31976).</span><span class="sxs-lookup"><span data-stu-id="3da45-112">For additional information about Microsoft Support Lifecycle Policy, see [Microsoft Support Lifecycle Support Policy FAQ](https://go.microsoft.com/fwlink/p/?LinkId=31976).</span></span>

 

## <a href="" id="---------mbam-server-system-requirements"></a> <span data-ttu-id="3da45-113">System Anforderungen für MBAM-Server</span><span class="sxs-lookup"><span data-stu-id="3da45-113">MBAM Server System Requirements</span></span>


### <span data-ttu-id="3da45-114">Server Betriebssystem-Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3da45-114">Server Operating System Requirements</span></span>

<span data-ttu-id="3da45-115">In der folgenden Tabelle sind die Betriebssysteme aufgeführt, die für die Installation von Microsoft BitLocker-Administration und-Monitoring Server unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="3da45-115">The following table lists the operating systems that are supported for the Microsoft BitLocker Administration and Monitoring Server installation.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="3da45-116">Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="3da45-116">Operating system</span></span></th>
<th align="left"><span data-ttu-id="3da45-117">Edition</span><span class="sxs-lookup"><span data-stu-id="3da45-117">Edition</span></span></th>
<th align="left"><span data-ttu-id="3da45-118">Service Pack</span><span class="sxs-lookup"><span data-stu-id="3da45-118">Service pack</span></span></th>
<th align="left"><span data-ttu-id="3da45-119">System Architektur</span><span class="sxs-lookup"><span data-stu-id="3da45-119">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3da45-120">WindowsServer2008 R2</span><span class="sxs-lookup"><span data-stu-id="3da45-120">WindowsServer2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="3da45-121">Standard-, Enterprise-oder Datacenter-Edition</span><span class="sxs-lookup"><span data-stu-id="3da45-121">Standard, Enterprise, or Datacenter Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="3da45-122">SP1</span><span class="sxs-lookup"><span data-stu-id="3da45-122">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="3da45-123">64Bit</span><span class="sxs-lookup"><span data-stu-id="3da45-123">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3da45-124">WindowsServer2012</span><span class="sxs-lookup"><span data-stu-id="3da45-124">WindowsServer2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="3da45-125">Standard-oder Datacenter Edition</span><span class="sxs-lookup"><span data-stu-id="3da45-125">Standard or Datacenter Edition</span></span></p></td>
<td align="left"></td>
<td align="left"><p><span data-ttu-id="3da45-126">64Bit</span><span class="sxs-lookup"><span data-stu-id="3da45-126">64-bit</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="3da45-127">**Hinweis**  Es gibt keine Unterstützung für die Installation von MBAM-Diensten,-Berichten oder-Datenbanken auf einem Domänencontrollercomputer.</span><span class="sxs-lookup"><span data-stu-id="3da45-127">**Note** There is no support for installing MBAM services, reports, or databases on a domain controller computer.</span></span>

 

### <a href="" id="server-processor--ram--and-disk-space-requirements-"></a><span data-ttu-id="3da45-128">Server Prozessor, Arbeitsspeicher und Speicherplatzanforderungen</span><span class="sxs-lookup"><span data-stu-id="3da45-128">Server Processor, RAM, and Disk Space Requirements</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="3da45-129">Hardware Komponente</span><span class="sxs-lookup"><span data-stu-id="3da45-129">Hardware component</span></span></th>
<th align="left"><span data-ttu-id="3da45-130">Mindestanforderungen</span><span class="sxs-lookup"><span data-stu-id="3da45-130">Minimum requirement</span></span></th>
<th align="left"><span data-ttu-id="3da45-131">Empfohlene Anforderung</span><span class="sxs-lookup"><span data-stu-id="3da45-131">Recommended requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3da45-132">Prozessor</span><span class="sxs-lookup"><span data-stu-id="3da45-132">Processor</span></span></p></td>
<td align="left"><p><span data-ttu-id="3da45-133">2,33 GHz</span><span class="sxs-lookup"><span data-stu-id="3da45-133">2.33 GHz</span></span></p></td>
<td align="left"><p><span data-ttu-id="3da45-134">2,33 GHz oder höher</span><span class="sxs-lookup"><span data-stu-id="3da45-134">2.33 GHz or greater</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3da45-135">RAM</span><span class="sxs-lookup"><span data-stu-id="3da45-135">RAM</span></span></p></td>
<td align="left"><p><span data-ttu-id="3da45-136">8 GB</span><span class="sxs-lookup"><span data-stu-id="3da45-136">8 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="3da45-137">12 GB</span><span class="sxs-lookup"><span data-stu-id="3da45-137">12 GB</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3da45-138">Freier Speicherplatz</span><span class="sxs-lookup"><span data-stu-id="3da45-138">Free disk space</span></span></p></td>
<td align="left"><p><span data-ttu-id="3da45-139">1 GB</span><span class="sxs-lookup"><span data-stu-id="3da45-139">1 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="3da45-140">2 GB</span><span class="sxs-lookup"><span data-stu-id="3da45-140">2 GB</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="sql-server-database-requirements-"></a><span data-ttu-id="3da45-141">SQLServer-Datenbankanforderungen</span><span class="sxs-lookup"><span data-stu-id="3da45-141">SQLServer Database Requirements</span></span>

<span data-ttu-id="3da45-142">In der folgenden Tabelle sind die SQLServer-Versionen aufgeführt, die für die Installation von Verwaltungs-und Überwachungs Server Features unterstützt werden, einschließlich der Datenbank für die Wiederherstellung, der Konformitäts-und Überwachungsdatenbank sowie der Konformitäts-und Überwachungsberichte.</span><span class="sxs-lookup"><span data-stu-id="3da45-142">The following table lists the SQLServer versions that are supported for the Administration and Monitoring Server feature installation, which includes the Recovery Database, Compliance and Audit Database, and Compliance and Audit Reports.</span></span> <span data-ttu-id="3da45-143">Die Datenbanken erfordern zusätzlich die Installation der SQL Server-Verwaltungs Tools.</span><span class="sxs-lookup"><span data-stu-id="3da45-143">The databases additionally require the installation of SQL Server Management Tools.</span></span>

<span data-ttu-id="3da45-144">**Hinweis**  MBAM unterstützt keine systemeigenen SQL-Clustering-, Spiegelungs-oder Verfügbarkeitsgruppen.</span><span class="sxs-lookup"><span data-stu-id="3da45-144">**Note** MBAM does not natively support SQL clustering, mirroring, or Availability Groups.</span></span> <span data-ttu-id="3da45-145">Wenn Sie die Datenbanken installieren möchten, müssen Sie die MBAM-Server Installation auf einem eigenständigen SQL Server ausführen.</span><span class="sxs-lookup"><span data-stu-id="3da45-145">To install the databases, you must run the MBAM Server installation on a stand-alone SQL server.</span></span>

 

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="3da45-146">SQL Server-Version</span><span class="sxs-lookup"><span data-stu-id="3da45-146">SQL Server version</span></span></th>
<th align="left"><span data-ttu-id="3da45-147">Edition</span><span class="sxs-lookup"><span data-stu-id="3da45-147">Edition</span></span></th>
<th align="left"><span data-ttu-id="3da45-148">Service Pack</span><span class="sxs-lookup"><span data-stu-id="3da45-148">Service pack</span></span></th>
<th align="left"><span data-ttu-id="3da45-149">System Architektur</span><span class="sxs-lookup"><span data-stu-id="3da45-149">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3da45-150">MicrosoftSQLServer2008 R2</span><span class="sxs-lookup"><span data-stu-id="3da45-150">MicrosoftSQLServer2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="3da45-151">Standard-, Enterprise-oder Datacenter-Edition</span><span class="sxs-lookup"><span data-stu-id="3da45-151">Standard, Enterprise, or Datacenter Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="3da45-152">SP1</span><span class="sxs-lookup"><span data-stu-id="3da45-152">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="3da45-153">64Bit</span><span class="sxs-lookup"><span data-stu-id="3da45-153">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3da45-154">MicrosoftSQLServer2012</span><span class="sxs-lookup"><span data-stu-id="3da45-154">MicrosoftSQLServer2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="3da45-155">Standard-, Enterprise-oder Datacenter-Edition</span><span class="sxs-lookup"><span data-stu-id="3da45-155">Standard, Enterprise, or Datacenter Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="3da45-156">SP1</span><span class="sxs-lookup"><span data-stu-id="3da45-156">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="3da45-157">64Bit</span><span class="sxs-lookup"><span data-stu-id="3da45-157">64-bit</span></span></p></td>
</tr>
</tbody>
</table>

 

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="3da45-158">Hardware Komponente</span><span class="sxs-lookup"><span data-stu-id="3da45-158">Hardware component</span></span></th>
<th align="left"><span data-ttu-id="3da45-159">Mindestanforderungen</span><span class="sxs-lookup"><span data-stu-id="3da45-159">Minimum requirement</span></span></th>
<th align="left"><span data-ttu-id="3da45-160">Empfohlene Anforderung</span><span class="sxs-lookup"><span data-stu-id="3da45-160">Recommended requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3da45-161">Prozessor</span><span class="sxs-lookup"><span data-stu-id="3da45-161">Processor</span></span></p></td>
<td align="left"><p><span data-ttu-id="3da45-162">2,33 GHz</span><span class="sxs-lookup"><span data-stu-id="3da45-162">2.33 GHz</span></span></p></td>
<td align="left"><p><span data-ttu-id="3da45-163">2,33 GHz oder höher</span><span class="sxs-lookup"><span data-stu-id="3da45-163">2.33 GHz or greater</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3da45-164">RAM</span><span class="sxs-lookup"><span data-stu-id="3da45-164">RAM</span></span></p></td>
<td align="left"><p><span data-ttu-id="3da45-165">8 GB</span><span class="sxs-lookup"><span data-stu-id="3da45-165">8 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="3da45-166">12 GB</span><span class="sxs-lookup"><span data-stu-id="3da45-166">12 GB</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3da45-167">Freier Speicherplatz</span><span class="sxs-lookup"><span data-stu-id="3da45-167">Free disk space</span></span></p></td>
<td align="left"><p><span data-ttu-id="3da45-168">5 GB</span><span class="sxs-lookup"><span data-stu-id="3da45-168">5 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="3da45-169">5 GB oder höher</span><span class="sxs-lookup"><span data-stu-id="3da45-169">5 GB or greater</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="---------mbam-client-system-requirements"></a> <span data-ttu-id="3da45-170">MBAM-Client System Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3da45-170">MBAM Client System Requirements</span></span>


### <span data-ttu-id="3da45-171">Client-Betriebs System Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3da45-171">Client Operating System Requirements</span></span>

<span data-ttu-id="3da45-172">In der folgenden Tabelle sind die Betriebssysteme aufgeführt, die für die Microsoft BitLocker-Verwaltung und-Überwachung der Client Installation unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="3da45-172">The following table lists the operating systems that are supported for Microsoft BitLocker Administration and Monitoring Client installation.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="3da45-173">Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="3da45-173">Operating system</span></span></th>
<th align="left"><span data-ttu-id="3da45-174">Edition</span><span class="sxs-lookup"><span data-stu-id="3da45-174">Edition</span></span></th>
<th align="left"><span data-ttu-id="3da45-175">Service Pack</span><span class="sxs-lookup"><span data-stu-id="3da45-175">Service pack</span></span></th>
<th align="left"><span data-ttu-id="3da45-176">System Architektur</span><span class="sxs-lookup"><span data-stu-id="3da45-176">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3da45-177">Windows7</span><span class="sxs-lookup"><span data-stu-id="3da45-177">Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="3da45-178">Enterprise-oder Ultimate-Edition</span><span class="sxs-lookup"><span data-stu-id="3da45-178">Enterprise or Ultimate Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="3da45-179">SP1</span><span class="sxs-lookup"><span data-stu-id="3da45-179">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="3da45-180">32 Bit oder 64 Bit</span><span class="sxs-lookup"><span data-stu-id="3da45-180">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3da45-181">Windows 8</span><span class="sxs-lookup"><span data-stu-id="3da45-181">Windows 8</span></span></p></td>
<td align="left"><p><span data-ttu-id="3da45-182">Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="3da45-182">Enterprise Edition</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="3da45-183">32 Bit oder 64 Bit</span><span class="sxs-lookup"><span data-stu-id="3da45-183">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3da45-184">Windows To Go</span><span class="sxs-lookup"><span data-stu-id="3da45-184">Windows To Go</span></span></p></td>
<td align="left"><p><span data-ttu-id="3da45-185">Windows 8 Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="3da45-185">Windows 8 Enterprise Edition</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="3da45-186">32 Bit oder 64 Bit</span><span class="sxs-lookup"><span data-stu-id="3da45-186">32-bit or 64-bit</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="client-ram-requirements-"></a><span data-ttu-id="3da45-187">Client-RAM-Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3da45-187">Client RAM Requirements</span></span>

<span data-ttu-id="3da45-188">Es gibt keine RAM-Anforderungen, die für die Microsoft BitLocker-Administrator-und-Überwachungs Client Installation spezifisch sind.</span><span class="sxs-lookup"><span data-stu-id="3da45-188">There are no RAM requirements that are specific to the Microsoft BitLocker Administration and Monitoring Client installation.</span></span>

## <a href="" id="---------mbam-group-policy-system-requirements"></a> <span data-ttu-id="3da45-189">System Anforderungen für MBAM-Gruppenrichtlinien</span><span class="sxs-lookup"><span data-stu-id="3da45-189">MBAM Group Policy System Requirements</span></span>


<span data-ttu-id="3da45-190">In der folgenden Tabelle sind die Betriebssysteme aufgeführt, die für die Microsoft BitLocker-Verwaltung und-Überwachung der Gruppenrichtlinien-Vorlageninstallation unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="3da45-190">The following table lists the operating systems that are supported for Microsoft BitLocker Administration and Monitoring Group Policy template installation.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="3da45-191">Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="3da45-191">Operating system</span></span></th>
<th align="left"><span data-ttu-id="3da45-192">Edition</span><span class="sxs-lookup"><span data-stu-id="3da45-192">Edition</span></span></th>
<th align="left"><span data-ttu-id="3da45-193">Service Pack</span><span class="sxs-lookup"><span data-stu-id="3da45-193">Service pack</span></span></th>
<th align="left"><span data-ttu-id="3da45-194">System Architektur</span><span class="sxs-lookup"><span data-stu-id="3da45-194">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3da45-195">Windows7</span><span class="sxs-lookup"><span data-stu-id="3da45-195">Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="3da45-196">Enterprise-oder Ultimate-Edition</span><span class="sxs-lookup"><span data-stu-id="3da45-196">Enterprise, or Ultimate Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="3da45-197">SP1</span><span class="sxs-lookup"><span data-stu-id="3da45-197">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="3da45-198">32 Bit oder 64 Bit</span><span class="sxs-lookup"><span data-stu-id="3da45-198">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3da45-199">Windows 8</span><span class="sxs-lookup"><span data-stu-id="3da45-199">Windows 8</span></span></p></td>
<td align="left"><p><span data-ttu-id="3da45-200">Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="3da45-200">Enterprise Edition</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="3da45-201">32 Bit oder 64 Bit</span><span class="sxs-lookup"><span data-stu-id="3da45-201">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3da45-202">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="3da45-202">Windows Server 2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="3da45-203">Standard-, Enterprise-oder Datacenter-Edition</span><span class="sxs-lookup"><span data-stu-id="3da45-203">Standard, Enterprise, or Datacenter Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="3da45-204">SP1</span><span class="sxs-lookup"><span data-stu-id="3da45-204">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="3da45-205">64Bit</span><span class="sxs-lookup"><span data-stu-id="3da45-205">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3da45-206">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3da45-206">Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="3da45-207">Standard-oder Datacenter Edition</span><span class="sxs-lookup"><span data-stu-id="3da45-207">Standard or Datacenter Edition</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="3da45-208">64Bit</span><span class="sxs-lookup"><span data-stu-id="3da45-208">64-bit</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="3da45-209">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="3da45-209">Related topics</span></span>


[<span data-ttu-id="3da45-210">Planen der Bereitstellung von MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="3da45-210">Planning to Deploy MBAM 2.0</span></span>](planning-to-deploy-mbam-20-mbam-2.md)

[<span data-ttu-id="3da45-211">Bereitstellungsvoraussetzungen für MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="3da45-211">MBAM 2.0 Deployment Prerequisites</span></span>](mbam-20-deployment-prerequisites-mbam-2.md)

 

 





