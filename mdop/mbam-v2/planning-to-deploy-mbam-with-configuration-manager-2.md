---
title: Planen der Bereitstellung von MBAM mit dem Konfigurations-Manager
description: Planen der Bereitstellung von MBAM mit dem Konfigurations-Manager
author: dansimp
ms.assetid: fb768306-48c2-40b4-ac4e-c279db987391
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: e8588ce03c86a8a5138d591327e5f95503dce5ad
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811269"
---
# <span data-ttu-id="7a679-103">Planen der Bereitstellung von MBAM mit dem Konfigurations-Manager</span><span class="sxs-lookup"><span data-stu-id="7a679-103">Planning to Deploy MBAM with Configuration Manager</span></span>


<span data-ttu-id="7a679-104">Zur Bereitstellung von MBAM mit der Configuration Manager-Topologie wird eine Architektur mit drei Servern empfohlen, die 200.000-Clients unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7a679-104">To deploy MBAM with the Configuration Manager topology, a three-server architecture, which supports 200,000 clients, is recommended.</span></span> <span data-ttu-id="7a679-105">Verwenden Sie einen separaten Server zum Ausführen von Configuration Manager, und installieren Sie die grundlegenden Verwaltungs-und Überwachungsfeatures auf zwei Servern, wie im Architektur Bild unter [Erste Schritte – verwenden von MBAM mit Configuration Manager](getting-started---using-mbam-with-configuration-manager.md)dargestellt.</span><span class="sxs-lookup"><span data-stu-id="7a679-105">Use a separate server to run Configuration Manager, and install the basic Administration and Monitoring features on two servers, as shown in the architecture image in [Getting Started - Using MBAM with Configuration Manager](getting-started---using-mbam-with-configuration-manager.md).</span></span>

**<span data-ttu-id="7a679-106">Wichtig</span><span class="sxs-lookup"><span data-stu-id="7a679-106">Important</span></span>**  
<span data-ttu-id="7a679-107">Windows to go wird nicht unterstützt, wenn Sie die integrierte Topologie von MBAM mit Configuration Manager 2007 installieren.</span><span class="sxs-lookup"><span data-stu-id="7a679-107">Windows To Go is not supported when you install the integrated topology of MBAM with Configuration Manager 2007.</span></span>



## <span data-ttu-id="7a679-108">Voraussetzungen für die Bereitstellung für die Installation von MBAM mit Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="7a679-108">Deployment Prerequisites for Installing MBAM with Configuration Manager</span></span>


<span data-ttu-id="7a679-109">Stellen Sie sicher, dass Sie die folgenden Voraussetzungen erfüllt haben, bevor Sie MBAM mit Configuration Manager installieren:</span><span class="sxs-lookup"><span data-stu-id="7a679-109">Ensure that you have met the following prerequisites before you install MBAM with Configuration Manager:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="7a679-110">Voraussetzung</span><span class="sxs-lookup"><span data-stu-id="7a679-110">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="7a679-111">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="7a679-111">Additional Information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7a679-112">Stellen Sie sicher, dass der Configuration Manager-Server ein primärer Standort im Configuration Manager-System ist.</span><span class="sxs-lookup"><span data-stu-id="7a679-112">Ensure that the Configuration Manager Server is a primary site in the Configuration Manager system.</span></span></p></td>
<td align="left"><p><span data-ttu-id="7a679-113">n.v.</span><span class="sxs-lookup"><span data-stu-id="7a679-113">N/A</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7a679-114">Aktivieren Sie den Hardware Inventur Client-Agent auf dem Configuration Manager-Server.</span><span class="sxs-lookup"><span data-stu-id="7a679-114">Enable the Hardware Inventory Client Agent on the Configuration Manager Server.</span></span></p></td>
<td align="left"><p><span data-ttu-id="7a679-115">Informationen zu Configuration Manager 2007 finden Sie unter <a href="https://go.microsoft.com/fwlink/?LinkId=301656" data-raw-source="[How to Configure Hardware Inventory for a Site](https://go.microsoft.com/fwlink/?LinkId=301656)"> Konfigurieren der Hardware Inventur für eine Website </a> .</span><span class="sxs-lookup"><span data-stu-id="7a679-115">For Configuration Manager 2007, see <a href="https://go.microsoft.com/fwlink/?LinkId=301656" data-raw-source="[How to Configure Hardware Inventory for a Site](https://go.microsoft.com/fwlink/?LinkId=301656)">How to Configure Hardware Inventory for a Site</a>.</span></span></p>
<p><span data-ttu-id="7a679-116">Informationen zu System Center 2012-Konfigurations-Manager finden Sie unter <a href="https://go.microsoft.com/fwlink/?LinkId=301685" data-raw-source="[How to Configure Hardware Inventory in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=301685)"> Konfigurieren der Hardware Inventur in Configuration Manager </a> .</span><span class="sxs-lookup"><span data-stu-id="7a679-116">For System Center 2012 Configuration Manager, see <a href="https://go.microsoft.com/fwlink/?LinkId=301685" data-raw-source="[How to Configure Hardware Inventory in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=301685)">How to Configure Hardware Inventory in Configuration Manager</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7a679-117">Aktivieren Sie den DCM-Agent (Desired Configuration Management) oder die Kompatibilitätseinstellungen, abhängig von der Version von Configuration Manager, die Sie verwenden.</span><span class="sxs-lookup"><span data-stu-id="7a679-117">Enable the Desired Configuration Management (DCM) agent or the compliance settings, depending on the version of Configuration Manager that you are using.</span></span></p></td>
<td align="left"><p><span data-ttu-id="7a679-118">Aktivieren Sie für Configuration Manager 2007 die Eigenschaften des Client-Agents für die <a href="https://go.microsoft.com/fwlink/?LinkId=301686" data-raw-source="[Desired Configuration Management Client Agent Properties](https://go.microsoft.com/fwlink/?LinkId=301686)"> Verwaltung der gewünschten Konfiguration </a> .</span><span class="sxs-lookup"><span data-stu-id="7a679-118">For Configuration Manager 2007, enable the see <a href="https://go.microsoft.com/fwlink/?LinkId=301686" data-raw-source="[Desired Configuration Management Client Agent Properties](https://go.microsoft.com/fwlink/?LinkId=301686)">Desired Configuration Management Client Agent Properties</a>.</span></span></p>
<p><span data-ttu-id="7a679-119">Informationen zu System Center 2012-Konfigurations-Manager finden Sie unter <a href="https://go.microsoft.com/fwlink/?LinkId=301687" data-raw-source="[Configuring Compliance Settings in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=301687)"> Konfigurieren von Kompatibilitätseinstellungen in Configuration Manager </a> .</span><span class="sxs-lookup"><span data-stu-id="7a679-119">For System Center 2012 Configuration Manager, see <a href="https://go.microsoft.com/fwlink/?LinkId=301687" data-raw-source="[Configuring Compliance Settings in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=301687)">Configuring Compliance Settings in Configuration Manager</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7a679-120">Definieren Sie einen Reporting Services-Punkt in Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="7a679-120">Define a reporting services point in Configuration Manager.</span></span> <span data-ttu-id="7a679-121">Für SQL Reporting Services erforderlich.</span><span class="sxs-lookup"><span data-stu-id="7a679-121">Required for SQL Reporting Services.</span></span></p></td>
<td align="left"><p><span data-ttu-id="7a679-122">Informationen zu Configuration Manager 2007 finden Sie unter <a href="https://go.microsoft.com/fwlink/?LinkId=301688" data-raw-source="[How to Create a Reporting Services Point for SQL Reporting Services](https://go.microsoft.com/fwlink/?LinkId=301688)"> Erstellen eines Reporting Services-Punkts für SQL Reporting Services </a> .</span><span class="sxs-lookup"><span data-stu-id="7a679-122">For Configuration Manager 2007, see <a href="https://go.microsoft.com/fwlink/?LinkId=301688" data-raw-source="[How to Create a Reporting Services Point for SQL Reporting Services](https://go.microsoft.com/fwlink/?LinkId=301688)">How to Create a Reporting Services Point for SQL Reporting Services</a>.</span></span></p>
<p><span data-ttu-id="7a679-123">Informationen zu System Center 2012-Konfigurations-Manager finden Sie unter <a href="https://go.microsoft.com/fwlink/?LinkId=301689" data-raw-source="[Prerequisites for Reporting in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=301689)"> Voraussetzungen für die Berichterstellung in Configuration Manager </a> .</span><span class="sxs-lookup"><span data-stu-id="7a679-123">For System Center 2012 Configuration Manager, see <a href="https://go.microsoft.com/fwlink/?LinkId=301689" data-raw-source="[Prerequisites for Reporting in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=301689)">Prerequisites for Reporting in Configuration Manager</a>.</span></span></p></td>
</tr>
</tbody>
</table>



## <a href="" id="---------configuration-manager-supported-versions"></a> <span data-ttu-id="7a679-124">Von Configuration Manager unterstützte Versionen</span><span class="sxs-lookup"><span data-stu-id="7a679-124">Configuration Manager Supported Versions</span></span>


<span data-ttu-id="7a679-125">MBAM unterstützt die folgenden Versionen von Configuration Manager:</span><span class="sxs-lookup"><span data-stu-id="7a679-125">MBAM supports the following versions of Configuration Manager:</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="7a679-126">Unterstützte Version</span><span class="sxs-lookup"><span data-stu-id="7a679-126">Supported version</span></span></th>
<th align="left"><span data-ttu-id="7a679-127">Service Pack</span><span class="sxs-lookup"><span data-stu-id="7a679-127">Service pack</span></span></th>
<th align="left"><span data-ttu-id="7a679-128">System Architektur</span><span class="sxs-lookup"><span data-stu-id="7a679-128">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7a679-129">Microsoft System Center Configuration Manager 2007 R2</span><span class="sxs-lookup"><span data-stu-id="7a679-129">Microsoft System Center Configuration Manager 2007 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="7a679-130">SP1 oder höher</span><span class="sxs-lookup"><span data-stu-id="7a679-130">SP1 or later</span></span></p></td>
<td align="left"><p><span data-ttu-id="7a679-131">64Bit</span><span class="sxs-lookup"><span data-stu-id="7a679-131">64-bit</span></span></p>
<div class="alert">
<strong><span data-ttu-id="7a679-132">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="7a679-132">Note</span></span></strong><br/><p><span data-ttu-id="7a679-133">Obwohl der Configuration Manager 2007 32-Bit ist, müssen Sie ihn und SQL Server auf einem 64-Bit-Betriebssystem installieren, um der 64-Bit-MBAM-Software entsprechen zu können.</span><span class="sxs-lookup"><span data-stu-id="7a679-133">Although Configuration Manager 2007 is 32 bit, you must install it and SQL Server on a 64-bit operating system in order to match the 64-bit MBAM software.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7a679-134">Microsoft System Center 2012-Konfigurations-Manager</span><span class="sxs-lookup"><span data-stu-id="7a679-134">Microsoft System Center 2012 Configuration Manager</span></span></p></td>
<td align="left"><p><span data-ttu-id="7a679-135">SP1</span><span class="sxs-lookup"><span data-stu-id="7a679-135">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="7a679-136">64Bit</span><span class="sxs-lookup"><span data-stu-id="7a679-136">64-bit</span></span></p></td>
</tr>
</tbody>
</table>



<span data-ttu-id="7a679-137">Eine Liste der unterstützten Konfigurationen für den Configuration Manager-Server finden Sie auf der entsprechenden Webseite für die Version von Configuration Manager, die Sie verwenden.</span><span class="sxs-lookup"><span data-stu-id="7a679-137">For a list of supported configurations for the Configuration Manager Server, see the appropriate webpage for the version of Configuration Manager that you are using.</span></span> <span data-ttu-id="7a679-138">MBAM hat keine zusätzlichen Systemanforderungen für den Configuration Manager-Server.</span><span class="sxs-lookup"><span data-stu-id="7a679-138">MBAM has no additional system requirements for the Configuration Manager Server.</span></span>

## <a href="" id="---------mbam-and-sql-server-system-requirements"></a> <span data-ttu-id="7a679-139">MBAM-und SQL Server-System Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7a679-139">MBAM and SQL Server System Requirements</span></span>


<span data-ttu-id="7a679-140">Die unterstützten Konfigurationen und Systemanforderungen für die MBAM-Server und SQL Server für die Configuration Manager-Topologie sind dieselben wie für die eigenständige Topologie.</span><span class="sxs-lookup"><span data-stu-id="7a679-140">The supported configurations and system requirements for the MBAM servers and SQL Server for the Configuration Manager topology are the same as those for the Stand-alone topology.</span></span> <span data-ttu-id="7a679-141">Die eigenständigen Systemanforderungen finden Sie unter [unterstützte MBAM 2,0-Konfigurationen](mbam-20-supported-configurations-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="7a679-141">For the Stand-alone system requirements, see [MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md).</span></span> <span data-ttu-id="7a679-142">Informationen zu den Anforderungen des MBAM-Servers und des SQL Server-Prozessors, des Arbeitsspeichers und des Speicherplatzes für die Configuration Manager-Topologie finden Sie in den folgenden Abschnitten.</span><span class="sxs-lookup"><span data-stu-id="7a679-142">For the MBAM Server and SQL Server processor, RAM, and disk space requirements for the Configuration Manager topology, see the following sections.</span></span>

## <span data-ttu-id="7a679-143">MBAM-Server Prozessor, RAM und Speicherplatzanforderungen für MBAM</span><span class="sxs-lookup"><span data-stu-id="7a679-143">MBAM Server Processor, RAM, and Disk Space Requirements for MBAM</span></span>


<span data-ttu-id="7a679-144">In der folgenden Tabelle sind die Server Prozessor-, RAM-und Speicherplatzanforderungen für MBAM-Server aufgelistet, wenn Sie die Configuration Manager-Integrations Topologie verwenden.</span><span class="sxs-lookup"><span data-stu-id="7a679-144">The following table lists the server processor, RAM, and disk space requirements for MBAM servers when you are using the Configuration Manager Integration topology.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="7a679-145">Hardware Komponente</span><span class="sxs-lookup"><span data-stu-id="7a679-145">Hardware Component</span></span></th>
<th align="left"><span data-ttu-id="7a679-146">Mindestanforderungen</span><span class="sxs-lookup"><span data-stu-id="7a679-146">Minimum Requirement</span></span></th>
<th align="left"><span data-ttu-id="7a679-147">Empfohlene Anforderung</span><span class="sxs-lookup"><span data-stu-id="7a679-147">Recommended Requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7a679-148">Prozessor</span><span class="sxs-lookup"><span data-stu-id="7a679-148">Processor</span></span></p></td>
<td align="left"><p><span data-ttu-id="7a679-149">2,33 GHz</span><span class="sxs-lookup"><span data-stu-id="7a679-149">2.33 GHz</span></span></p></td>
<td align="left"><p><span data-ttu-id="7a679-150">2,33 GHz oder höher</span><span class="sxs-lookup"><span data-stu-id="7a679-150">2.33 GHz or greater</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7a679-151">RAM</span><span class="sxs-lookup"><span data-stu-id="7a679-151">RAM</span></span></p></td>
<td align="left"><p><span data-ttu-id="7a679-152">4 GB</span><span class="sxs-lookup"><span data-stu-id="7a679-152">4 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="7a679-153">8 GB</span><span class="sxs-lookup"><span data-stu-id="7a679-153">8 GB</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7a679-154">Freier Speicherplatz</span><span class="sxs-lookup"><span data-stu-id="7a679-154">Free disk space</span></span></p></td>
<td align="left"><p><span data-ttu-id="7a679-155">1 GB</span><span class="sxs-lookup"><span data-stu-id="7a679-155">1 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="7a679-156">2 GB</span><span class="sxs-lookup"><span data-stu-id="7a679-156">2 GB</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="7a679-157">SQL Server-Prozessor, Arbeitsspeicher und Speicherplatzanforderungen</span><span class="sxs-lookup"><span data-stu-id="7a679-157">SQL Server Processor, RAM, and Disk Space Requirements</span></span>


<span data-ttu-id="7a679-158">In der folgenden Tabelle sind die Anforderungen für den Server Prozessor, den Arbeitsspeicher und den Speicherplatz für den SQL Server-Computer aufgeführt, wenn Sie die Configuration Manager-Integrations Topologie verwenden.</span><span class="sxs-lookup"><span data-stu-id="7a679-158">The following table lists the server processor, RAM, and disk space requirements for the SQL Server computer when you are using the Configuration Manager Integration topology.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="7a679-159">Hardware Komponente</span><span class="sxs-lookup"><span data-stu-id="7a679-159">Hardware Component</span></span></th>
<th align="left"><span data-ttu-id="7a679-160">Mindestanforderungen</span><span class="sxs-lookup"><span data-stu-id="7a679-160">Minimum Requirement</span></span></th>
<th align="left"><span data-ttu-id="7a679-161">Empfohlene Anforderung</span><span class="sxs-lookup"><span data-stu-id="7a679-161">Recommended Requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7a679-162">Prozessor</span><span class="sxs-lookup"><span data-stu-id="7a679-162">Processor</span></span></p></td>
<td align="left"><p><span data-ttu-id="7a679-163">2,33 GHz</span><span class="sxs-lookup"><span data-stu-id="7a679-163">2.33 GHz</span></span></p></td>
<td align="left"><p><span data-ttu-id="7a679-164">2,33 GHz oder höher</span><span class="sxs-lookup"><span data-stu-id="7a679-164">2.33 GHz or greater</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7a679-165">RAM</span><span class="sxs-lookup"><span data-stu-id="7a679-165">RAM</span></span></p></td>
<td align="left"><p><span data-ttu-id="7a679-166">4 GB</span><span class="sxs-lookup"><span data-stu-id="7a679-166">4 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="7a679-167">8 GB</span><span class="sxs-lookup"><span data-stu-id="7a679-167">8 GB</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7a679-168">Freier Speicherplatz</span><span class="sxs-lookup"><span data-stu-id="7a679-168">Free disk space</span></span></p></td>
<td align="left"><p><span data-ttu-id="7a679-169">5 GB</span><span class="sxs-lookup"><span data-stu-id="7a679-169">5 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="7a679-170">5 GB oder höher</span><span class="sxs-lookup"><span data-stu-id="7a679-170">5 GB or greater</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="7a679-171">Erforderliche Berechtigungen zum Installieren des MBAM-Servers</span><span class="sxs-lookup"><span data-stu-id="7a679-171">Required permissions to install the MBAM Server</span></span>


<span data-ttu-id="7a679-172">Zum Installieren von MBAM mit Configuration Manager müssen Sie über einen Administrator Benutzer in Configuration Manager verfügen, der über eine Sicherheitsrolle mit den in der folgenden Tabelle aufgeführten Mindestberechtigungen verfügt.</span><span class="sxs-lookup"><span data-stu-id="7a679-172">To install MBAM with Configuration Manager, you must have an administrative user in Configuration Manager who has a security role with the minimum permissions listed in the following table.</span></span> <span data-ttu-id="7a679-173">Die Tabelle enthält auch die Rechte, die Sie über die grundlegenden Computeradministrator Rechte hinaus benötigen, um den MBAM-Server zu installieren.</span><span class="sxs-lookup"><span data-stu-id="7a679-173">The table also shows the rights that you must have, beyond basic computer administrator rights, to install the MBAM Server.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="7a679-174">Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="7a679-174">Permissions</span></span></th>
<th align="left"><span data-ttu-id="7a679-175">MBAM-Server Feature</span><span class="sxs-lookup"><span data-stu-id="7a679-175">MBAM Server Feature</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7a679-176">SQL instance-Anmelde Server Rollen:-dbcreator-processadmin</span><span class="sxs-lookup"><span data-stu-id="7a679-176">SQL instance Login Server Roles: - dbcreator- processadmin</span></span></p></td>
<td align="left"><p>- <span data-ttu-id="7a679-177">Wiederherstellungsdatenbank – Überwachungsdatenbank</span><span class="sxs-lookup"><span data-stu-id="7a679-177">Recovery Database- Audit Database</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7a679-178">SQL Server Reporting Services-Instanzen Rechte:-Erstellen von Ordnern-veröffentlichen von Berichten</span><span class="sxs-lookup"><span data-stu-id="7a679-178">SQL Server Reporting Services instance rights: - Create Folders- Publish Reports</span></span></p></td>
<td align="left"><p>- <span data-ttu-id="7a679-179">Integration von System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="7a679-179">System Center Configuration Manager Integration</span></span></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="7a679-180">System Center 2012 Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="7a679-180">System Center 2012 Configuration Manager</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="7a679-181">Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="7a679-181">Permissions</span></span></th>
<th align="left"><span data-ttu-id="7a679-182">Configuration Manager-Server Feature</span><span class="sxs-lookup"><span data-stu-id="7a679-182">Configuration Manager Server Feature</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7a679-183">Configuration Manager-Website Rechte:-Lesen</span><span class="sxs-lookup"><span data-stu-id="7a679-183">Configuration Manager site rights:- Read</span></span></p></td>
<td align="left"><p><span data-ttu-id="7a679-184">Integration von System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="7a679-184">System Center Configuration Manager integration</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7a679-185">Configuration Manager-Sammlungs Rechte:-Erstellen-Löschen-lesen-ändern – Bereitstellen von Konfigurationselementen</span><span class="sxs-lookup"><span data-stu-id="7a679-185">Configuration Manager collection rights: - Create- Delete- Read- Modify- Deploy Configuration Items</span></span></p></td>
<td align="left"><p><span data-ttu-id="7a679-186">Integration von System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="7a679-186">System Center Configuration Manager integration</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7a679-187">Configuration Manager-Konfigurationselement Rechte:-Create-DELETE-Read</span><span class="sxs-lookup"><span data-stu-id="7a679-187">Configuration Manager configuration item rights: - Create- Delete- Read</span></span></p></td>
<td align="left"><p><span data-ttu-id="7a679-188">Integration von System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="7a679-188">System Center Configuration Manager integration</span></span></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="7a679-189">Configuration Manager 2007</span><span class="sxs-lookup"><span data-stu-id="7a679-189">Configuration Manager 2007</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="7a679-190">Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="7a679-190">Permissions</span></span></th>
<th align="left"><span data-ttu-id="7a679-191">Configuration Manager-Server Feature</span><span class="sxs-lookup"><span data-stu-id="7a679-191">Configuration Manager Server Feature</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7a679-192">Configuration Manager-Website Rechte:-Lesen</span><span class="sxs-lookup"><span data-stu-id="7a679-192">Configuration Manager site rights:- Read</span></span></p></td>
<td align="left"><p><span data-ttu-id="7a679-193">Integration von System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="7a679-193">System Center Configuration Manager integration</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7a679-194">Configuration Manager-Sammlungs Rechte:-Create-DELETE-Read-ReadResource</span><span class="sxs-lookup"><span data-stu-id="7a679-194">Configuration Manager collection rights: - Create- Delete- Read- ReadResource</span></span></p></td>
<td align="left"><p><span data-ttu-id="7a679-195">Integration von System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="7a679-195">System Center Configuration Manager integration</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7a679-196">Configuration Manager-Konfigurationselement Rechte:-Create-DELETE-Read-Distribute</span><span class="sxs-lookup"><span data-stu-id="7a679-196">Configuration Manager configuration item rights: - Create- Delete- Read- Distribute</span></span></p></td>
<td align="left"><p><span data-ttu-id="7a679-197">Integration von System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="7a679-197">System Center Configuration Manager integration</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="7a679-198">Reihenfolge der Bereitstellung von MBAM-Features für die Configuration Manager-Topologie</span><span class="sxs-lookup"><span data-stu-id="7a679-198">Order of Deployment of MBAM Features for the Configuration Manager Topology</span></span>


<span data-ttu-id="7a679-199">Wenn Sie MBAM auf dem Configuration Manager-Server bereitstellen, müssen Sie die Bereitstellungsaufgaben in der folgenden Reihenfolge ausführen:</span><span class="sxs-lookup"><span data-stu-id="7a679-199">When deploying MBAM on the Configuration Manager Server, you must complete the deployment tasks in the following order:</span></span>

1.  <span data-ttu-id="7a679-200">Bearbeiten Sie die Datei "Configuration. mof" auf dem Configuration Manager-Server.</span><span class="sxs-lookup"><span data-stu-id="7a679-200">Edit the configuration.mof file on the Configuration Manager Server.</span></span>

2.  <span data-ttu-id="7a679-201">Erstellen oder bearbeiten Sie den SMS-_def. MOF-Datei-Konfigurations-Manager-Server.</span><span class="sxs-lookup"><span data-stu-id="7a679-201">Create or edit the sms\_def.mof file Configuration Manager Server.</span></span>

3.  <span data-ttu-id="7a679-202">Installieren Sie MBAM auf dem Configuration Manager-Server.</span><span class="sxs-lookup"><span data-stu-id="7a679-202">Install MBAM on the Configuration Manager Server.</span></span>

4.  <span data-ttu-id="7a679-203">Installieren Sie die Wiederherstellungsdatenbank und die Überwachungsdatenbank auf dem Datenbankserver.</span><span class="sxs-lookup"><span data-stu-id="7a679-203">Install the Recovery Database and the Audit Database on the Database server.</span></span>

5.  <span data-ttu-id="7a679-204">Installieren Sie die MBAM-Features auf dem Verwaltungs-und Überwachungs Server.</span><span class="sxs-lookup"><span data-stu-id="7a679-204">Install the MBAM features on the Administration and Monitoring Server.</span></span>

## <span data-ttu-id="7a679-205">Prüfliste für die Planung für die Installation von MBAM mit Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="7a679-205">Planning Checklist for Installing MBAM with Configuration Manager</span></span>


<span data-ttu-id="7a679-206">In dieser Checkliste werden die empfohlenen Schritte und eine Liste der Elemente auf höherer Ebene erläutert, die bei der Planung einer Microsoft BitLocker-Verwaltungs-und-Überwachungs Bereitstellung mit Configuration Manager berücksichtigt werden sollten.</span><span class="sxs-lookup"><span data-stu-id="7a679-206">This checklist outlines the recommended steps and a high-level list of items to consider when planning for an Microsoft BitLocker Administration and Monitoring deployment with Configuration Manager.</span></span> <span data-ttu-id="7a679-207">Es wird empfohlen, dass Sie diese Checkliste in ein Kalkulationstabellenprogramm kopieren und für ihre Verwendung anpassen.</span><span class="sxs-lookup"><span data-stu-id="7a679-207">It is recommended that you copy this checklist into a spreadsheet program and customize it for your use.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left"><span data-ttu-id="7a679-208">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="7a679-208">Task</span></span></th>
<th align="left"><span data-ttu-id="7a679-209">Verweise</span><span class="sxs-lookup"><span data-stu-id="7a679-209">References</span></span></th>
<th align="left"><span data-ttu-id="7a679-210">Anmerkungen</span><span class="sxs-lookup"><span data-stu-id="7a679-210">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="7a679-211">Lesen Sie die Informationen zu den ersten Schritten, in denen beschrieben wird, wie der Configuration Manager mit MBAM funktioniert, und zeigt die empfohlene Architektur auf hoher Ebene an.</span><span class="sxs-lookup"><span data-stu-id="7a679-211">Review the getting started information, which describes how Configuration Manager works with MBAM and shows the recommended high-level architecture.</span></span></p></td>
<td align="left"><p><a href="getting-started---using-mbam-with-configuration-manager.md" data-raw-source="[Getting Started - Using MBAM with Configuration Manager](getting-started---using-mbam-with-configuration-manager.md)"><span data-ttu-id="7a679-212">Erste Schritte – Verwenden von MBAM mit dem Konfigurations-Manager</span><span class="sxs-lookup"><span data-stu-id="7a679-212">Getting Started - Using MBAM with Configuration Manager</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="7a679-213">Überprüfen Sie die Planungsinformationen, in denen die Voraussetzungen für die Bereitstellung, unterstützte Konfigurationen, erforderliche Berechtigungen und Bereitstellungsreihenfolge für die einzelnen Features beschrieben sind.</span><span class="sxs-lookup"><span data-stu-id="7a679-213">Review the planning information, which describes the deployment prerequisites, supported configurations, required permissions, and deployment order for each feature.</span></span></p></td>
<td align="left"><p><span data-ttu-id="7a679-214">Planen der Bereitstellung von MBAM mit dem Konfigurations-Manager</span><span class="sxs-lookup"><span data-stu-id="7a679-214">Planning to Deploy MBAM with Configuration Manager</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="7a679-215">Planen und Konfigurieren von MBAM-Gruppenrichtlinienanforderungen</span><span class="sxs-lookup"><span data-stu-id="7a679-215">Plan for and configure MBAM Group Policy requirements.</span></span></p></td>
<td align="left"><p><a href="planning-for-mbam-20-group-policy-requirements-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Group Policy Requirements](planning-for-mbam-20-group-policy-requirements-mbam-2.md)"><span data-ttu-id="7a679-216">Planen der Gruppenrichtlinienanforderungen für MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="7a679-216">Planning for MBAM 2.0 Group Policy Requirements</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="7a679-217">Planen und erstellen Sie die erforderlichen Active Directory-Domänendienste-Sicherheitsgruppen, und planen Sie die Mitgliedschaftsanforderungen für MBAM Local Security Group.</span><span class="sxs-lookup"><span data-stu-id="7a679-217">Plan for and create necessary Active Directory Domain Services security groups and plan for MBAM local security group membership requirements.</span></span></p></td>
<td align="left"><p><a href="planning-for-mbam-20-administrator-roles-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Administrator Roles](planning-for-mbam-20-administrator-roles-mbam-2.md)"><span data-ttu-id="7a679-218">Planen der Administratorrollen für MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="7a679-218">Planning for MBAM 2.0 Administrator Roles</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="7a679-219">Planen der Bereitstellung der MBAM-Client Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="7a679-219">Plan for deploying MBAM Client deployment.</span></span></p></td>
<td align="left"><p><a href="planning-for-mbam-20-client-deployment-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Client Deployment](planning-for-mbam-20-client-deployment-mbam-2.md)"><span data-ttu-id="7a679-220">Planen der Clientbereitstellung für MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="7a679-220">Planning for MBAM 2.0 Client Deployment</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="7a679-221">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="7a679-221">Related topics</span></span>


[<span data-ttu-id="7a679-222">Verwenden von MBAM mit dem Konfigurations-Manager</span><span class="sxs-lookup"><span data-stu-id="7a679-222">Using MBAM with Configuration Manager</span></span>](using-mbam-with-configuration-manager.md)









