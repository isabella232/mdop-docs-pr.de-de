---
title: High-Level-Architektur von MBAM 2.5 mit eigenständiger Topologie
description: High-Level-Architektur von MBAM 2.5 mit eigenständiger Topologie
author: dansimp
ms.assetid: 35f8c5f6-8be3-443d-baf0-56d68b08f3bc
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 75e878e24b4675f2f2f574791d0f06ecadd0196d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811827"
---
# <span data-ttu-id="532b6-103">High-Level-Architektur von MBAM 2.5 mit eigenständiger Topologie</span><span class="sxs-lookup"><span data-stu-id="532b6-103">High-Level Architecture of MBAM 2.5 with Stand-alone Topology</span></span>


<span data-ttu-id="532b6-104">In diesem Thema wird die empfohlene Architektur für die Bereitstellung von Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) mit der eigenständigen Configuration Manager-Topologie beschrieben.</span><span class="sxs-lookup"><span data-stu-id="532b6-104">This topic describes the recommended architecture for deploying Microsoft BitLocker Administration and Monitoring (MBAM) with the Configuration Manager Stand-alone topology.</span></span> <span data-ttu-id="532b6-105">In dieser Topologie wird MBAM als eigenständiges Produkt bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="532b6-105">In this topology, MBAM is deployed as a stand-alone product.</span></span> <span data-ttu-id="532b6-106">Sie können MBAM auch mit der Configuration Manager-Integrations Topologie bereitstellen, die MBAM mit Configuration Manager integriert.</span><span class="sxs-lookup"><span data-stu-id="532b6-106">You can alternatively deploy MBAM with the Configuration Manager Integration topology, which integrates MBAM with Configuration Manager.</span></span> <span data-ttu-id="532b6-107">Weitere Informationen finden Sie unter [Architektur auf höherer Ebene in MBAM 2,5 mit der Configuration Manager-Integrations Topologie](high-level-architecture-of-mbam-25-with-configuration-manager-integration-topology.md).</span><span class="sxs-lookup"><span data-stu-id="532b6-107">For more information, see [High-Level Architecture of MBAM 2.5 with Configuration Manager Integration Topology](high-level-architecture-of-mbam-25-with-configuration-manager-integration-topology.md).</span></span>

<span data-ttu-id="532b6-108">Eine Liste der unterstützten Versionen der in diesem Thema erwähnten Software finden Sie unter [unterstützte MBAM 2,5-Konfigurationen](mbam-25-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="532b6-108">For a list of the supported versions of the software mentioned in this topic, see [MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md).</span></span>

<span data-ttu-id="532b6-109">**Hinweis**  Wir empfehlen, nur in Testumgebungen eine Architektur mit einem Server zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="532b6-109">**Note** We recommend you use a single-server architecture in test environments only.</span></span>

 

## <span data-ttu-id="532b6-110">Empfohlene Anzahl von Servern und unterstützte Anzahl von Clients</span><span class="sxs-lookup"><span data-stu-id="532b6-110">Recommended number of servers and supported number of clients</span></span>


<span data-ttu-id="532b6-111">Die empfohlene Anzahl von Servern und unterstützten Clients in einer Produktionsumgebung lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="532b6-111">The recommended number of servers and supported number of clients in a production environment is as follows:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="532b6-112">Empfohlene Architektur in einer Produktionsumgebung</span><span class="sxs-lookup"><span data-stu-id="532b6-112">Recommended architecture in a production environment</span></span></th>
<th align="left"><span data-ttu-id="532b6-113">Details</span><span class="sxs-lookup"><span data-stu-id="532b6-113">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="532b6-114">Anzahl der Server und anderer Computer</span><span class="sxs-lookup"><span data-stu-id="532b6-114">Number of servers and other computers</span></span></p></td>
<td align="left"><p><span data-ttu-id="532b6-115">Zwei Server</span><span class="sxs-lookup"><span data-stu-id="532b6-115">Two servers</span></span></p>
<p><span data-ttu-id="532b6-116">Eine Workstation</span><span class="sxs-lookup"><span data-stu-id="532b6-116">One workstation</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="532b6-117">Anzahl der unterstützten Clientcomputer</span><span class="sxs-lookup"><span data-stu-id="532b6-117">Number of client computers supported</span></span></p></td>
<td align="left"><p><span data-ttu-id="532b6-118">500.000</span><span class="sxs-lookup"><span data-stu-id="532b6-118">500,000</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="532b6-119">Empfohlene MBAM-Architektur auf höherer Ebene mit der eigenständigen Topologie</span><span class="sxs-lookup"><span data-stu-id="532b6-119">Recommended MBAM high-level architecture with the Stand-alone topology</span></span>


<span data-ttu-id="532b6-120">Das folgende Diagramm und die folgende Tabelle beschreiben die empfohlene Architektur für zwei Server auf hoher Ebene für MBAM mit der eigenständigen Topologie.</span><span class="sxs-lookup"><span data-stu-id="532b6-120">The following diagram and table describe the recommended high-level, two-server architecture for MBAM with the Stand-alone topology.</span></span> <span data-ttu-id="532b6-121">MBAM Multi-Forest-Bereitstellungen erfordern eine unidirektionale oder bidirektionale Vertrauensstellung.</span><span class="sxs-lookup"><span data-stu-id="532b6-121">MBAM multi-forest deployments require a one-way or two-way trust.</span></span> <span data-ttu-id="532b6-122">Unidirektionale Vertrauensstellungen setzen voraus, dass die Server Domäne der Clientdomäne vertraut.</span><span class="sxs-lookup"><span data-stu-id="532b6-122">One-way trusts require that the server domain trusts the client domain.</span></span>

![mbam2](images/mbam2-5-2servers.png)

<span data-ttu-id="532b6-124">Server Features zum Konfigurieren auf diesem Server Beschreibungsdaten Bankserver</span><span class="sxs-lookup"><span data-stu-id="532b6-124">Server Features to configure on this server Description Database server</span></span>

<span data-ttu-id="532b6-125">Konformitäts-und Überwachungsdatenbank</span><span class="sxs-lookup"><span data-stu-id="532b6-125">Compliance and Audit Database</span></span>

<span data-ttu-id="532b6-126">Dieses Feature ist auf einem Server konfiguriert, auf dem Windows Server ausgeführt wird, und die SQL Server-Instanz unterstützt.</span><span class="sxs-lookup"><span data-stu-id="532b6-126">This feature is configured on a server running Windows Server and supported SQL Server instance.</span></span>

<span data-ttu-id="532b6-127">Die **Compliance-und Überwachungsdatenbank** speichert Kompatibilitätsdaten, die hauptsächlich für Berichte verwendet werden, die von SQL Server Reporting Services gehostet werden.</span><span class="sxs-lookup"><span data-stu-id="532b6-127">The **Compliance and Audit Database** stores compliance data, which is used primarily for reports that SQL Server Reporting Services hosts.</span></span>

<span data-ttu-id="532b6-128">Wiederherstellungsdatenbank</span><span class="sxs-lookup"><span data-stu-id="532b6-128">Recovery Database</span></span>

<span data-ttu-id="532b6-129">Dieses Feature ist auf einem Server konfiguriert, auf dem Windows Server ausgeführt wird, und die SQL Server-Instanz unterstützt.</span><span class="sxs-lookup"><span data-stu-id="532b6-129">This feature is configured on a server running Windows Server and supported SQL Server instance.</span></span>

<span data-ttu-id="532b6-130">Die **Wiederherstellungsdatenbank** speichert Wiederherstellungsdaten, die von MBAM-Clientcomputern erfasst werden.</span><span class="sxs-lookup"><span data-stu-id="532b6-130">The **Recovery Database** stores recovery data that is collected from MBAM client computers.</span></span>

<span data-ttu-id="532b6-131">Berichte</span><span class="sxs-lookup"><span data-stu-id="532b6-131">Reports</span></span>

<span data-ttu-id="532b6-132">Dieses Feature ist auf einem Server konfiguriert, auf dem Windows Server ausgeführt wird, und die SQL Server-Instanz unterstützt.</span><span class="sxs-lookup"><span data-stu-id="532b6-132">This feature is configured on a server running Windows Server and supported SQL Server instance.</span></span>

<span data-ttu-id="532b6-133">In den **Berichten** werden Wiederherstellungs Überwachungs-und Kompatibilitätsstatus Daten zu den Clientcomputern in Ihrem Unternehmen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="532b6-133">The **Reports** provide recovery audit and compliance status data about the client computers in your enterprise.</span></span> <span data-ttu-id="532b6-134">Sie können auf die Berichte über die Website Verwaltung und Überwachung oder direkt in SQL Server Reporting Services zugreifen.</span><span class="sxs-lookup"><span data-stu-id="532b6-134">You can access the reports from the Administration and Monitoring Website or directly from SQL Server Reporting Services.</span></span>

<span data-ttu-id="532b6-135">Verwaltungs-und Überwachungs Server</span><span class="sxs-lookup"><span data-stu-id="532b6-135">Administration and Monitoring Server</span></span>

<span data-ttu-id="532b6-136">Website "Verwaltung und Überwachung"</span><span class="sxs-lookup"><span data-stu-id="532b6-136">Administration and Monitoring Website</span></span>

<span data-ttu-id="532b6-137">Dieses Feature ist auf einem Computer mit Windows Server konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="532b6-137">This feature is configured on a computer running Windows Server.</span></span>

<span data-ttu-id="532b6-138">Die **Website Verwaltung und Überwachung** wird verwendet, um Folgendes zu tun:</span><span class="sxs-lookup"><span data-stu-id="532b6-138">The **Administration and Monitoring Website** is used to:</span></span>

-   <span data-ttu-id="532b6-139">Helfen Sie den Endbenutzern beim wieder Zugriff auf Ihre Computer, wenn Sie gesperrt sind. (Dieser Bereich der Website wird im Allgemeinen als Help Desk bezeichnet.)</span><span class="sxs-lookup"><span data-stu-id="532b6-139">Help end users regain access to their computers when they are locked out. (This area of the Website is commonly called the Help Desk.)</span></span>

-   <span data-ttu-id="532b6-140">Anzeigen von Berichten, die den Kompatibilitätsstatus und die Wiederherstellungs Aktivität für Clientcomputer anzeigen</span><span class="sxs-lookup"><span data-stu-id="532b6-140">View reports that show compliance status and recovery activity for client computers.</span></span>

<span data-ttu-id="532b6-141">Self-Service-Portal</span><span class="sxs-lookup"><span data-stu-id="532b6-141">Self-Service Portal</span></span>

<span data-ttu-id="532b6-142">Dieses Feature ist auf einem Computer mit Windows Server konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="532b6-142">This feature is configured on a computer running Windows Server.</span></span>

<span data-ttu-id="532b6-143">Das **Self-Service-Portal** ist eine Website, auf der sich Endbenutzer auf Clientcomputern selbstständig an einer Website anmelden können, um einen Wiederherstellungsschlüssel abzurufen, wenn Sie Ihr BitLocker-Kennwort verlieren oder vergessen.</span><span class="sxs-lookup"><span data-stu-id="532b6-143">The **Self-Service Portal** is a website that enables end users on client computers to independently log on to a website to get a recovery key if they lose or forget their BitLocker password.</span></span>

<span data-ttu-id="532b6-144">Überwachen von Webdiensten für diese Website</span><span class="sxs-lookup"><span data-stu-id="532b6-144">Monitoring web services for this website</span></span>

<span data-ttu-id="532b6-145">Dieses Feature ist auf einem Computer mit Windows Server konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="532b6-145">This feature is configured on a computer running Windows Server.</span></span>

<span data-ttu-id="532b6-146">Die **Überwachungs-Webdienste** werden vom MBAM-Client und den Websites verwendet, um mit der Datenbank zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="532b6-146">The **monitoring web services** are used by the MBAM Client and the websites to communicate to the database.</span></span>

<span data-ttu-id="532b6-147">**Wichtig**  Der Monitoring Web Service steht in der Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) 2,5 SP1 nicht mehr zur Verfügung, da die MBAM-Websites direkt mit der Wiederherstellungsdatenbank kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="532b6-147">**Important** The Monitoring Web Service is no longer available in Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 SP1 since the MBAM websites communicate directly with the Recovery Database.</span></span>

 

<span data-ttu-id="532b6-148">Verwaltungsarbeitsstation</span><span class="sxs-lookup"><span data-stu-id="532b6-148">Management workstation</span></span>

<span data-ttu-id="532b6-149">MBAM-Gruppenrichtlinienvorlagen</span><span class="sxs-lookup"><span data-stu-id="532b6-149">MBAM Group Policy Templates</span></span>

-   <span data-ttu-id="532b6-150">Bei den MBAM-Gruppenrichtlinienvorlagen handelt es sich um Gruppenrichtlinieneinstellungen, die Implementierungs Einstellungen für MBAM definieren, mit denen Sie die BitLocker-Laufwerkverschlüsselung verwalten können.</span><span class="sxs-lookup"><span data-stu-id="532b6-150">The MBAM Group Policy Templates are Group Policy settings that define implementation settings for MBAM, which enable you to manage BitLocker Drive Encryption.</span></span>

-   <span data-ttu-id="532b6-151">Bevor Sie MBAM ausführen, müssen Sie die Gruppenrichtlinienvorlagen herunterladen, indem Sie [MDOP Gruppenrichtlinien (ADMX)-Vorlagen abrufen](https://go.microsoft.com/fwlink/p/?LinkId=393941) und auf einen Server oder eine Workstation kopieren, auf dem ein unterstütztes Windows-Server-oder Windows-Betriebssystem ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="532b6-151">Before you run MBAM, you must download the Group Policy Templates from [How to Get MDOP Group Policy (.admx) Templates](https://go.microsoft.com/fwlink/p/?LinkId=393941) and copy them to a server or workstation that is running a supported Windows Server or Windows operating system.</span></span>

-   <span data-ttu-id="532b6-152">Die Workstation muss kein dedizierter Computer sein.</span><span class="sxs-lookup"><span data-stu-id="532b6-152">The workstation does not have to be a dedicated computer.</span></span>

<span data-ttu-id="532b6-153">MBAM-Client und Configuration Manager-Clientcomputer</span><span class="sxs-lookup"><span data-stu-id="532b6-153">MBAM Client and Configuration Manager client computer</span></span>

<span data-ttu-id="532b6-154">MBAM-Client Software</span><span class="sxs-lookup"><span data-stu-id="532b6-154">MBAM Client software</span></span>

<span data-ttu-id="532b6-155">Der MBAM-Client:</span><span class="sxs-lookup"><span data-stu-id="532b6-155">The MBAM Client:</span></span>

-   <span data-ttu-id="532b6-156">Verwendet Gruppenrichtlinienobjekte, um die BitLocker-Laufwerkverschlüsselung auf Clientcomputern im Unternehmen durchzusetzen.</span><span class="sxs-lookup"><span data-stu-id="532b6-156">Uses Group Policy Objects to enforce BitLocker Drive Encryption on client computers in the enterprise.</span></span>

-   <span data-ttu-id="532b6-157">Sammelt den BitLocker-Wiederherstellungsschlüssel für drei Datenlaufwerk Typen: Betriebssystemlaufwerke, fest Netzlaufwerke und Wechseldatenträger (USB)-Datenlaufwerke.</span><span class="sxs-lookup"><span data-stu-id="532b6-157">Collects the Bitlocker recovery key for three data drive types: operating system drives, fixed data drives, and removable (USB) data drives.</span></span>

-   <span data-ttu-id="532b6-158">Sammelt Wiederherstellungsinformationen und Computer Informationen zu den Clientcomputern.</span><span class="sxs-lookup"><span data-stu-id="532b6-158">Collects recovery information and computer information about the client computers.</span></span>



## <span data-ttu-id="532b6-159">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="532b6-159">Related topics</span></span>


[<span data-ttu-id="532b6-160">Erste Schritte mit MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="532b6-160">Getting Started with MBAM 2.5</span></span>](getting-started-with-mbam-25.md)

[<span data-ttu-id="532b6-161">High-Level-Architektur von MBAM 2.5 mit Configuration Manager-Integrationstopologie</span><span class="sxs-lookup"><span data-stu-id="532b6-161">High-Level Architecture of MBAM 2.5 with Configuration Manager Integration Topology</span></span>](high-level-architecture-of-mbam-25-with-configuration-manager-integration-topology.md)

[<span data-ttu-id="532b6-162">Beschreibung der Funktionen einer MBAM 2.5-Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="532b6-162">Illustrated Features of an MBAM 2.5 Deployment</span></span>](illustrated-features-of-an-mbam-25-deployment.md)

 

## <span data-ttu-id="532b6-163">Sie haben einen Vorschlag für MBAM?</span><span class="sxs-lookup"><span data-stu-id="532b6-163">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="532b6-164">[Hier](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)können Sie Vorschläge hinzufügen oder abstimmen.</span><span class="sxs-lookup"><span data-stu-id="532b6-164">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="532b6-165">Bei MBAM-Problemen verwenden Sie das [MBAM TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="532b6-165">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





