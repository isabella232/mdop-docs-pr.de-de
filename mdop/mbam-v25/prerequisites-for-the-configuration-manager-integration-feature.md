---
title: Voraussetzungen für das Configuration Manager-Integrationsfeature
description: Voraussetzungen für das Configuration Manager-Integrationsfeature
author: dansimp
ms.assetid: b318cbd3-b009-44b8-991b-f7364c1cae88
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: af7abd50f6218810dd6718f091512b48fee32652
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810900"
---
# <span data-ttu-id="213bf-103">Voraussetzungen für das Configuration Manager-Integrationsfeature</span><span class="sxs-lookup"><span data-stu-id="213bf-103">Prerequisites for the Configuration Manager Integration Feature</span></span>


<span data-ttu-id="213bf-104">Wenn Sie MBAM mit der System Center Configuration Manager-Integrations Topologie bereitstellen, empfehlen wir eine Architektur mit drei Servern, wie in [der allgemeinen Architektur von MBAM 2,5 mit der Configuration Manager-Integrations Topologie](high-level-architecture-of-mbam-25-with-configuration-manager-integration-topology.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="213bf-104">If you deploy MBAM with the System Center Configuration Manager Integration topology, we recommend a three-server architecture, as described in [High-Level Architecture of MBAM 2.5 with Configuration Manager Integration Topology](high-level-architecture-of-mbam-25-with-configuration-manager-integration-topology.md).</span></span> <span data-ttu-id="213bf-105">Diese Architektur kann 500.000-Clientcomputer unterstützen.</span><span class="sxs-lookup"><span data-stu-id="213bf-105">This architecture can support 500,000 client computers.</span></span>

**<span data-ttu-id="213bf-106">Wichtig</span><span class="sxs-lookup"><span data-stu-id="213bf-106">Important</span></span>**  
<span data-ttu-id="213bf-107">Windows to go wird bei der Installation der Configuration Manager-Integrations Topologie nicht unterstützt, wenn Sie Configuration Manager 2007 verwenden.</span><span class="sxs-lookup"><span data-stu-id="213bf-107">Windows To Go is not supported for the Configuration Manager Integration topology installation when you are using Configuration Manager 2007.</span></span>



## <span data-ttu-id="213bf-108">Allgemeine Voraussetzungen für das Configuration Manager-Integrations Feature</span><span class="sxs-lookup"><span data-stu-id="213bf-108">General prerequisites for the Configuration Manager Integration feature</span></span>


<span data-ttu-id="213bf-109">Wenn Sie MBAM mit Configuration Manager installieren, sind zusätzlich zu den Voraussetzungen für die eigenständige Topologie die folgenden zusätzlichen Voraussetzungen erforderlich.</span><span class="sxs-lookup"><span data-stu-id="213bf-109">When you install MBAM with Configuration Manager, the following additional prerequisites are required in addition to the prerequisites for the Stand-alone topology.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="213bf-110">Voraussetzung</span><span class="sxs-lookup"><span data-stu-id="213bf-110">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="213bf-111">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="213bf-111">Additional information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="213bf-112">Der Configuration Manager-Server ist ein primärer Standort im Configuration Manager-System.</span><span class="sxs-lookup"><span data-stu-id="213bf-112">The Configuration Manager Server is a primary site in the Configuration Manager system.</span></span></p></td>
<td align="left"><p><span data-ttu-id="213bf-113">n.v.</span><span class="sxs-lookup"><span data-stu-id="213bf-113">N/A</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="213bf-114">Der Hardware Inventur Client-Agent befindet sich auf dem Configuration Manager-Server.</span><span class="sxs-lookup"><span data-stu-id="213bf-114">The Hardware Inventory Client Agent is on the Configuration Manager Server.</span></span></p></td>
<td align="left"><p><span data-ttu-id="213bf-115">Informationen zu System Center 2012-Konfigurations-Manager finden Sie unter <a href="https://go.microsoft.com/fwlink/?LinkId=301685" data-raw-source="[How to Configure Hardware Inventory in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=301685)"> Konfigurieren der Hardware Inventur in Configuration Manager </a> .</span><span class="sxs-lookup"><span data-stu-id="213bf-115">For System Center 2012 Configuration Manager, see <a href="https://go.microsoft.com/fwlink/?LinkId=301685" data-raw-source="[How to Configure Hardware Inventory in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=301685)">How to Configure Hardware Inventory in Configuration Manager</a>.</span></span></p>
<p><span data-ttu-id="213bf-116">Informationen zu Configuration Manager 2007 finden Sie unter <a href="https://go.microsoft.com/fwlink/?LinkId=301656" data-raw-source="[How to Configure Hardware Inventory for a Site](https://go.microsoft.com/fwlink/?LinkId=301656)"> Konfigurieren der Hardware Inventur für eine Website </a> .</span><span class="sxs-lookup"><span data-stu-id="213bf-116">For Configuration Manager 2007, see <a href="https://go.microsoft.com/fwlink/?LinkId=301656" data-raw-source="[How to Configure Hardware Inventory for a Site](https://go.microsoft.com/fwlink/?LinkId=301656)">How to Configure Hardware Inventory for a Site</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="213bf-117">Je nach der von Ihnen verwendeten Version von Configuration Manager ist eine der folgenden Optionen aktiviert:</span><span class="sxs-lookup"><span data-stu-id="213bf-117">One of the following is enabled, depending on the version of Configuration Manager that you are using:</span></span></p>
<ul>
<li><p><span data-ttu-id="213bf-118">Kompatibilitätseinstellungen – (System Center 2012-Konfigurations-Manager)</span><span class="sxs-lookup"><span data-stu-id="213bf-118">Compliance Settings - (System Center 2012 Configuration Manager)</span></span></p></li>
<li><p><span data-ttu-id="213bf-119">DCM-Client-Agent (Desired Configuration Management) – (Configuration Manager 2007)</span><span class="sxs-lookup"><span data-stu-id="213bf-119">Desired Configuration Management (DCM) Client Agent – (Configuration Manager 2007)</span></span></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="213bf-120">Informationen zu System Center 2012-Konfigurations-Manager finden Sie unter <a href="https://go.microsoft.com/fwlink/?LinkId=301687" data-raw-source="[Configuring Compliance Settings in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=301687)"> Konfigurieren von Kompatibilitätseinstellungen in Configuration Manager </a> .</span><span class="sxs-lookup"><span data-stu-id="213bf-120">For System Center 2012 Configuration Manager, see <a href="https://go.microsoft.com/fwlink/?LinkId=301687" data-raw-source="[Configuring Compliance Settings in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=301687)">Configuring Compliance Settings in Configuration Manager</a>.</span></span></p>
<p><span data-ttu-id="213bf-121">Informationen zu Configuration Manager 2007 finden Sie unter <a href="https://go.microsoft.com/fwlink/?LinkId=301686" data-raw-source="[Desired Configuration Management Client Agent Properties](https://go.microsoft.com/fwlink/?LinkId=301686)"> Client-Agent-Eigenschaften der gewünschten Configuration-Verwaltung </a> .</span><span class="sxs-lookup"><span data-stu-id="213bf-121">For Configuration Manager 2007, see <a href="https://go.microsoft.com/fwlink/?LinkId=301686" data-raw-source="[Desired Configuration Management Client Agent Properties](https://go.microsoft.com/fwlink/?LinkId=301686)">Desired Configuration Management Client Agent Properties</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="213bf-122">Ein Reporting Services-Punkt ist in Configuration Manager definiert.</span><span class="sxs-lookup"><span data-stu-id="213bf-122">A reporting services point is defined in Configuration Manager.</span></span> <span data-ttu-id="213bf-123">Erforderlich für SQL Server Reporting Services (SSRS).</span><span class="sxs-lookup"><span data-stu-id="213bf-123">Required for SQL Server Reporting Services (SSRS).</span></span></p></td>
<td align="left"><p><span data-ttu-id="213bf-124">Informationen zu System Center 2012-Konfigurations-Manager finden Sie unter <a href="https://go.microsoft.com/fwlink/?LinkId=301689" data-raw-source="[Prerequisites for Reporting in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=301689)"> Voraussetzungen für die Berichterstellung in Configuration Manager </a> .</span><span class="sxs-lookup"><span data-stu-id="213bf-124">For System Center 2012 Configuration Manager, see <a href="https://go.microsoft.com/fwlink/?LinkId=301689" data-raw-source="[Prerequisites for Reporting in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=301689)">Prerequisites for Reporting in Configuration Manager</a>.</span></span></p>
<p><span data-ttu-id="213bf-125">Informationen zu Configuration Manager 2007 finden Sie unter <a href="https://go.microsoft.com/fwlink/?LinkId=301688" data-raw-source="[How to Create a Reporting Services Point for SQL Reporting Services](https://go.microsoft.com/fwlink/?LinkId=301688)"> Erstellen eines Reporting Services-Punkts für SQL Reporting Services </a> .</span><span class="sxs-lookup"><span data-stu-id="213bf-125">For Configuration Manager 2007, see <a href="https://go.microsoft.com/fwlink/?LinkId=301688" data-raw-source="[How to Create a Reporting Services Point for SQL Reporting Services](https://go.microsoft.com/fwlink/?LinkId=301688)">How to Create a Reporting Services Point for SQL Reporting Services</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="213bf-126">Configuration Manager 2007 erfordert Microsoft .NET Framework 2,0</span><span class="sxs-lookup"><span data-stu-id="213bf-126">Configuration Manager 2007 requires Microsoft .NET Framework 2.0</span></span></p></td>
<td align="left"><p><span data-ttu-id="213bf-127">Der DCM-Client-Agent (Desired Configuration Management) in Configuration Manager 2007 erfordert .NET Framework 2,0, um die Kompatibilität zu melden.</span><span class="sxs-lookup"><span data-stu-id="213bf-127">The Desired Configuration Management (DCM) Client Agent in Configuration Manager 2007 requires .NET Framework 2.0 to report compliance.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="213bf-128">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="213bf-128">Note</span></span></strong><br/><p><span data-ttu-id="213bf-129">Beim Installieren von .NET Framework 3,5 wird .NET Framework 2,0 automatisch installiert.</span><span class="sxs-lookup"><span data-stu-id="213bf-129">Installing .NET Framework 3.5 automatically installs .NET Framework 2.0.</span></span></p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="213bf-130">Erforderliche Berechtigungen zum Installieren von MBAM mit Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="213bf-130">Required permissions to install MBAM with Configuration Manager</span></span>


<span data-ttu-id="213bf-131">Zum Installieren von MBAM mit Configuration Manager müssen Sie über einen Administrator Benutzer in Configuration Manager verfügen, der über eine Sicherheitsrolle mit den in der folgenden Tabelle aufgeführten Mindestberechtigungen verfügt.</span><span class="sxs-lookup"><span data-stu-id="213bf-131">To install MBAM with Configuration Manager, you must have an administrative user in Configuration Manager who has a security role with the minimum permissions listed in the following table.</span></span> <span data-ttu-id="213bf-132">Die Tabelle enthält auch die Rechte, die Sie über die grundlegenden Computeradministrator Rechte hinaus benötigen, um den MBAM-Server zu installieren.</span><span class="sxs-lookup"><span data-stu-id="213bf-132">The table also shows the rights that you must have, beyond basic computer administrator rights, to install the MBAM Server.</span></span>

**<span data-ttu-id="213bf-133">Die Berechtigungen in der folgenden Tabelle gelten für beide Versionen von Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="213bf-133">The permissions in the following table apply to both versions of Configuration Manager.</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="213bf-134">Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="213bf-134">Permissions</span></span></th>
<th align="left"><span data-ttu-id="213bf-135">MBAM-Server Feature</span><span class="sxs-lookup"><span data-stu-id="213bf-135">MBAM Server feature</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="213bf-136">SQL Server-Instanz-Anmelde Server Rollen:-dbcreator-processadmin</span><span class="sxs-lookup"><span data-stu-id="213bf-136">SQL Server instance login server roles: - dbcreator- processadmin</span></span></p></td>
<td align="left"><p>- <span data-ttu-id="213bf-137">Wiederherstellungsdatenbank – Überwachungsdatenbank</span><span class="sxs-lookup"><span data-stu-id="213bf-137">Recovery Database- Audit Database</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="213bf-138">Rechte von SSRS-Instanzen:-Erstellen von Ordnern-veröffentlichen von Berichten</span><span class="sxs-lookup"><span data-stu-id="213bf-138">SSRS instance rights: - Create Folders- Publish Reports</span></span></p></td>
<td align="left"><p>- <span data-ttu-id="213bf-139">Integration von System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="213bf-139">System Center Configuration Manager Integration</span></span></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="213bf-140">System Center 2012 Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="213bf-140">System Center 2012 Configuration Manager</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="213bf-141">Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="213bf-141">Permissions</span></span></th>
<th align="left"><span data-ttu-id="213bf-142">Configuration Manager-Server Feature</span><span class="sxs-lookup"><span data-stu-id="213bf-142">Configuration Manager Server feature</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="213bf-143">Configuration Manager-Website Rechte:-Lesen</span><span class="sxs-lookup"><span data-stu-id="213bf-143">Configuration Manager site rights:- Read</span></span></p></td>
<td align="left"><p><span data-ttu-id="213bf-144">Integration von System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="213bf-144">System Center Configuration Manager Integration</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="213bf-145">Configuration Manager-Sammlungs Rechte:-Erstellen-Löschen-lesen-ändern – Bereitstellen von Konfigurationselementen</span><span class="sxs-lookup"><span data-stu-id="213bf-145">Configuration Manager collection rights: - Create- Delete- Read- Modify- Deploy Configuration Items</span></span></p></td>
<td align="left"><p><span data-ttu-id="213bf-146">Integration von System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="213bf-146">System Center Configuration Manager Integration</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="213bf-147">Configuration Manager-Konfigurationselement Rechte:-Create-DELETE-Read</span><span class="sxs-lookup"><span data-stu-id="213bf-147">Configuration Manager configuration item rights: - Create- Delete- Read</span></span></p></td>
<td align="left"><p><span data-ttu-id="213bf-148">Integration von System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="213bf-148">System Center Configuration Manager Integration</span></span></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="213bf-149">Configuration Manager 2007</span><span class="sxs-lookup"><span data-stu-id="213bf-149">Configuration Manager 2007</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="213bf-150">Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="213bf-150">Permissions</span></span></th>
<th align="left"><span data-ttu-id="213bf-151">Configuration Manager-Server Feature</span><span class="sxs-lookup"><span data-stu-id="213bf-151">Configuration Manager Server feature</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="213bf-152">Configuration Manager-Website Rechte:-Lesen</span><span class="sxs-lookup"><span data-stu-id="213bf-152">Configuration Manager site rights:- Read</span></span></p></td>
<td align="left"><p><span data-ttu-id="213bf-153">Integration von System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="213bf-153">System Center Configuration Manager Integration</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="213bf-154">Configuration Manager-Sammlungs Rechte:-Create-DELETE-Read-ReadResource</span><span class="sxs-lookup"><span data-stu-id="213bf-154">Configuration Manager collection rights: - Create- Delete- Read- ReadResource</span></span></p></td>
<td align="left"><p><span data-ttu-id="213bf-155">Integration von System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="213bf-155">System Center Configuration Manager Integration</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="213bf-156">Configuration Manager-Konfigurationselement Rechte:-Create-DELETE-Read-Distribute</span><span class="sxs-lookup"><span data-stu-id="213bf-156">Configuration Manager configuration item rights: - Create- Delete- Read- Distribute</span></span></p></td>
<td align="left"><p><span data-ttu-id="213bf-157">Integration von System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="213bf-157">System Center Configuration Manager Integration</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="213bf-158">Erforderliche Änderungen für die MOF-Dateien</span><span class="sxs-lookup"><span data-stu-id="213bf-158">Required changes for the .mof files</span></span>


<span data-ttu-id="213bf-159">Damit die Clientcomputer BitLocker-Kompatibilitätsdetails über die MBAM-Konfigurations-Manager-Berichte melden können, müssen Sie die Datei "Configuration. mof" und die SMS \ _def. MOF-Datei für System Center 2012 Configuration Manager und Microsoft System Center Configuration Manager 2007 bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="213bf-159">To enable the client computers to report BitLocker compliance details through the MBAM Configuration Manager reports, you have to edit the Configuration.mof file and Sms\_def.mof file for System Center 2012 Configuration Manager and Microsoft System Center Configuration Manager 2007.</span></span> <span data-ttu-id="213bf-160">Anweisungen hierzu finden Sie unter [Voraussetzungen für MBAM 2,5-Server, die nur für die Configuration Manager-Integrations Topologie gelten](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md).</span><span class="sxs-lookup"><span data-stu-id="213bf-160">For instructions, see [MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md).</span></span>



## <span data-ttu-id="213bf-161">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="213bf-161">Related topics</span></span>


[<span data-ttu-id="213bf-162">MBAM 2.5-Servervoraussetzungen für eigenständige und Configuration Manager-Integrationstopologien</span><span class="sxs-lookup"><span data-stu-id="213bf-162">MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies</span></span>](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)

[<span data-ttu-id="213bf-163">MBAM 2.5-Servervoraussetzungen, die nur für die Configuration Manager-Integrationstopologie gelten</span><span class="sxs-lookup"><span data-stu-id="213bf-163">MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology</span></span>](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md)



## <span data-ttu-id="213bf-164">Sie haben einen Vorschlag für MBAM?</span><span class="sxs-lookup"><span data-stu-id="213bf-164">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="213bf-165">[Hier](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)können Sie Vorschläge hinzufügen oder abstimmen.</span><span class="sxs-lookup"><span data-stu-id="213bf-165">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="213bf-166">Bei MBAM-Problemen verwenden Sie das [MBAM TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="213bf-166">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





