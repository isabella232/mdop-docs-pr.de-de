---
title: Planen der Serverbereitstellung für MBAM 2.5
description: Planen der Serverbereitstellung für MBAM 2.5
author: dansimp
ms.assetid: 88774c89-31c8-4eb8-a845-a00bbec8c870
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d2ecb510fab821118ce210577f9ffb83c39be050
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811620"
---
# <span data-ttu-id="b1af0-103">Planen der Serverbereitstellung für MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="b1af0-103">Planning for MBAM 2.5 Server Deployment</span></span>


<span data-ttu-id="b1af0-104">In diesem Thema sind die Features aufgeführt, die Sie für die eigenständige und Configuration Manager-Topologie von MBAM bereitstellen, und es wird die Reihenfolge aufgeführt, in der Sie bereitgestellt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="b1af0-104">This topic lists the features that you deploy for the MBAM Stand-alone and Configuration Manager topologies and lists the order in which you need to deploy them.</span></span> <span data-ttu-id="b1af0-105">Es gibt eine empfohlene Konfiguration für jede Topologie.</span><span class="sxs-lookup"><span data-stu-id="b1af0-105">There is a recommended configuration for each topology.</span></span> <span data-ttu-id="b1af0-106">Sie können jedoch MBAM-Server Datenbanken und-Features je nach Ihren Skalierbarkeitsanforderungen in unterschiedlichen Konfigurationen und auf mehreren Servern konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="b1af0-106">However, you can configure MBAM server databases and features in different configurations and across multiple servers, depending on your scalability requirements.</span></span>

## <span data-ttu-id="b1af0-107">Wichtige Planungsüberlegungen für Topologien</span><span class="sxs-lookup"><span data-stu-id="b1af0-107">Important planning considerations for both topologies</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="b1af0-108">Erwägungen</span><span class="sxs-lookup"><span data-stu-id="b1af0-108">Considerations</span></span></th>
<th align="left"><span data-ttu-id="b1af0-109">Details oder Zweck</span><span class="sxs-lookup"><span data-stu-id="b1af0-109">Details or purpose</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b1af0-110">Überprüfen Sie die folgenden Punkte, bevor Sie die Bereitstellung starten:</span><span class="sxs-lookup"><span data-stu-id="b1af0-110">Review the following before you start the deployment:</span></span></p>
<ul>
<li><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)"><span data-ttu-id="b1af0-111">MBAM 2.5-Servervoraussetzungen für eigenständige und Configuration Manager-Integrationstopologien</span><span class="sxs-lookup"><span data-stu-id="b1af0-111">MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies</span></span></a></p></li>
<li><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)"><span data-ttu-id="b1af0-112">Von MBAM 2.5 unterstützte Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="b1af0-112">MBAM 2.5 Supported Configurations</span></span></a></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="b1af0-113">Jedes MBAM-Feature hat bestimmte Voraussetzungen, die erfüllt sein müssen, bevor Sie die MBAM-Installation starten.</span><span class="sxs-lookup"><span data-stu-id="b1af0-113">Each MBAM feature has specific prerequisites that must be met before you start the MBAM installation.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b1af0-114">BitLocker-Wiederherstellungsschlüssel in MBAM verfallen nach einer einmaligen Verwendung.</span><span class="sxs-lookup"><span data-stu-id="b1af0-114">BitLocker recovery keys in MBAM expire after a single use.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b1af0-115">Eine einmalige Verwendung bedeutet, dass der Wiederherstellungsschlüssel über die Website "Verwaltung und Überwachung" (auch als "Helpdesk" bezeichnet), Self-Service-Portal oder mithilfe des <strong> Windows PowerShell-Cmdlets Get-MbamBitLockerRecoveryKey abgerufen wurde </strong> .</span><span class="sxs-lookup"><span data-stu-id="b1af0-115">A single use means that the recovery key has been retrieved through the Administration and Monitoring Website (also known as Help Desk), Self-Service Portal, or by using the Get-<strong>MbamBitLockerRecoveryKey</strong> Windows PowerShell cmdlet.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b1af0-116">Verfolgen Sie die Namen der Computer, auf denen Sie die einzelnen Features konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="b1af0-116">Keep track of the names of the computers on which you configure each feature.</span></span> <span data-ttu-id="b1af0-117">Diese Informationen werden während des gesamten Konfigurationsprozesses verwendet.</span><span class="sxs-lookup"><span data-stu-id="b1af0-117">You will use this information throughout the configuration process.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b1af0-118">Möglicherweise möchten Sie die <a href="mbam-25-deployment-checklist.md" data-raw-source="[MBAM 2.5 Deployment Checklist](mbam-25-deployment-checklist.md)"> MBAM 2,5-Bereitstellungscheckliste </a> für diesen Zweck verwenden.</span><span class="sxs-lookup"><span data-stu-id="b1af0-118">You may want to use the <a href="mbam-25-deployment-checklist.md" data-raw-source="[MBAM 2.5 Deployment Checklist](mbam-25-deployment-checklist.md)">MBAM 2.5 Deployment Checklist</a> for this purpose.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b1af0-119">Konfigurieren Sie nur die Gruppenrichtlinieneinstellungen im MDOP-MBAM (BitLocker-Verwaltungsknoten).</span><span class="sxs-lookup"><span data-stu-id="b1af0-119">Configure only the Group Policy settings in the MDOP MBAM (BitLocker Management) node.</span></span> <span data-ttu-id="b1af0-120">Ändern Sie nicht die Gruppenrichtlinieneinstellungen im BitLocker Drive Encryption-Knoten.</span><span class="sxs-lookup"><span data-stu-id="b1af0-120">Do not change the Group Policy settings in the BitLocker Drive Encryption node.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b1af0-121">Wenn Sie die Gruppenrichtlinieneinstellungen im Knoten BitLocker Drive Encryption ändern, funktioniert MBAM nicht.</span><span class="sxs-lookup"><span data-stu-id="b1af0-121">If you change the Group Policy settings in the BitLocker Drive Encryption node, MBAM will not work.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="planning-for-mbam-server-deployment---stand-alone-topology"></a><span data-ttu-id="b1af0-122">Planen der MBAM Server-Bereitstellung – eigenständige Topologie</span><span class="sxs-lookup"><span data-stu-id="b1af0-122">Planning for MBAM Server deployment – Stand-alone topology</span></span>


<span data-ttu-id="b1af0-123">Für die eigenständige Topologie wird eine Konfiguration mit zwei Servern für Produktionsumgebungen empfohlen, obwohl Konfigurationen von drei bis vier Servern verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="b1af0-123">For the Stand-alone topology, a two-server configuration is recommended for production environments, although configurations of three to four servers can be used.</span></span>

<span data-ttu-id="b1af0-124">Die Server Infrastruktur für die eigenständige MBAM-Topologie umfasst die folgenden Features, die in der angegebenen Reihenfolge konfiguriert werden müssen:</span><span class="sxs-lookup"><span data-stu-id="b1af0-124">The Server infrastructure for the MBAM Stand-alone topology contains the following features, which must be configured in the order listed:</span></span>

1.  <span data-ttu-id="b1af0-125">Datenbanken (Compliance-und Audit-Datenbank und Wiederherstellungsdatenbank)</span><span class="sxs-lookup"><span data-stu-id="b1af0-125">Databases (Compliance and Audit Database and Recovery Database)</span></span>

2.  <span data-ttu-id="b1af0-126">Berichte</span><span class="sxs-lookup"><span data-stu-id="b1af0-126">Reports</span></span>

3.  <span data-ttu-id="b1af0-127">Web Applications (und die entsprechenden Webdienste)</span><span class="sxs-lookup"><span data-stu-id="b1af0-127">Web applications (and their corresponding web services)</span></span>

    -   <span data-ttu-id="b1af0-128">Website "Verwaltung und Überwachung"</span><span class="sxs-lookup"><span data-stu-id="b1af0-128">Administration and Monitoring Website</span></span>

    -   <span data-ttu-id="b1af0-129">Self-Service-Portal</span><span class="sxs-lookup"><span data-stu-id="b1af0-129">Self-Service Portal</span></span>

<span data-ttu-id="b1af0-130">Eine Beschreibung dieser Features finden Sie unter [Architektur auf höherer Ebene von MBAM 2,5 mit eigenständiger Topologie](high-level-architecture-of-mbam-25-with-stand-alone-topology.md).</span><span class="sxs-lookup"><span data-stu-id="b1af0-130">For a description of these features, see [High-Level Architecture of MBAM 2.5 with Stand-alone Topology](high-level-architecture-of-mbam-25-with-stand-alone-topology.md).</span></span>

## <a href="" id="planning-for-mbam-server-deployment---configuration-manager-topology"></a><span data-ttu-id="b1af0-131">Planen der MBAM Server Bereitstellung – Configuration Manager-Topologie</span><span class="sxs-lookup"><span data-stu-id="b1af0-131">Planning for MBAM Server deployment – Configuration Manager topology</span></span>


<span data-ttu-id="b1af0-132">Für die Configuration Manager-Integrations Topologie wird eine Konfiguration mit drei Servern für Produktionsumgebungen empfohlen, auch wenn Konfigurationen von zusätzlichen Servern verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="b1af0-132">For the Configuration Manager Integration topology, a three-server configuration is recommended for production environments, although configurations of additional servers can be used.</span></span>

<span data-ttu-id="b1af0-133">Die Server Infrastruktur für die MBAM Configuration Manager-Topologie enthält die folgenden Features, die in der angegebenen Reihenfolge konfiguriert oder ausgeführt werden müssen:</span><span class="sxs-lookup"><span data-stu-id="b1af0-133">The Server infrastructure for the MBAM Configuration Manager topology contains the following features, which must be configured or performed in the order listed:</span></span>

1.  <span data-ttu-id="b1af0-134">Datenbanken (Compliance-und Audit-Datenbank und Wiederherstellungsdatenbank)</span><span class="sxs-lookup"><span data-stu-id="b1af0-134">Databases (Compliance and Audit Database and Recovery Database)</span></span>

2.  <span data-ttu-id="b1af0-135">Berichte</span><span class="sxs-lookup"><span data-stu-id="b1af0-135">Reports</span></span>

3.  <span data-ttu-id="b1af0-136">Web Applications (und die entsprechenden Webdienste)</span><span class="sxs-lookup"><span data-stu-id="b1af0-136">Web applications (and their corresponding web services)</span></span>

    -   <span data-ttu-id="b1af0-137">Website "Verwaltung und Überwachung"</span><span class="sxs-lookup"><span data-stu-id="b1af0-137">Administration and Monitoring Website</span></span>

    -   <span data-ttu-id="b1af0-138">Self-Service-Portal</span><span class="sxs-lookup"><span data-stu-id="b1af0-138">Self-Service Portal</span></span>

4.  <span data-ttu-id="b1af0-139">Integration von System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="b1af0-139">System Center Configuration Manager Integration</span></span>

<span data-ttu-id="b1af0-140">Eine Beschreibung dieser Features finden Sie unter [Architektur auf höherer Ebene in MBAM 2,5 mit der Configuration Manager-Integrations Topologie](high-level-architecture-of-mbam-25-with-configuration-manager-integration-topology.md).</span><span class="sxs-lookup"><span data-stu-id="b1af0-140">For a description of these features, see [High-Level Architecture of MBAM 2.5 with Configuration Manager Integration Topology](high-level-architecture-of-mbam-25-with-configuration-manager-integration-topology.md).</span></span>



## <span data-ttu-id="b1af0-141">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="b1af0-141">Related topics</span></span>


[<span data-ttu-id="b1af0-142">Planen der Bereitstellung von MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="b1af0-142">Planning to Deploy MBAM 2.5</span></span>](planning-to-deploy-mbam-25.md)

[<span data-ttu-id="b1af0-143">Bereitstellen der Serverinfrastruktur von MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="b1af0-143">Deploying the MBAM 2.5 Server Infrastructure</span></span>](deploying-the-mbam-25-server-infrastructure.md)

 

## <span data-ttu-id="b1af0-144">Sie haben einen Vorschlag für MBAM?</span><span class="sxs-lookup"><span data-stu-id="b1af0-144">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="b1af0-145">[Hier](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)können Sie Vorschläge hinzufügen oder abstimmen.</span><span class="sxs-lookup"><span data-stu-id="b1af0-145">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="b1af0-146">Bei MBAM-Problemen verwenden Sie das [MBAM TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="b1af0-146">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





