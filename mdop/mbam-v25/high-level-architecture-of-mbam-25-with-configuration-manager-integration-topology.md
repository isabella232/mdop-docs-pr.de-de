---
title: High-Level-Architektur von MBAM 2.5 mit Configuration Manager-Integrationstopologie
description: High-Level-Architektur von MBAM 2.5 mit Configuration Manager-Integrationstopologie
author: dansimp
ms.assetid: 075bafa1-792b-4c24-9d8e-5d3153e2112c
ms.reviewer: ''
manager: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/23/2018
ms.author: dansimp
ms.openlocfilehash: 75af2e22981d76568916c36acadbbb25648b1f1d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811350"
---
# <span data-ttu-id="4707f-103">Allgemeine Architektur von MBAM 2,5 mit der Configuration Manager-Integrations Topologie</span><span class="sxs-lookup"><span data-stu-id="4707f-103">High-level architecture of MBAM 2.5 with Configuration Manager Integration topology</span></span>

<span data-ttu-id="4707f-104">In diesem Thema wird die empfohlene Architektur für die Bereitstellung von Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) mit der Configuration Manager-Integrations Topologie beschrieben.</span><span class="sxs-lookup"><span data-stu-id="4707f-104">This topic describes the recommended architecture for deploying Microsoft BitLocker Administration and Monitoring (MBAM) with the Configuration Manager Integration topology.</span></span> <span data-ttu-id="4707f-105">Diese Topologie integriert MBAM mit System Center Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="4707f-105">This topology integrates MBAM with System Center Configuration Manager.</span></span> <span data-ttu-id="4707f-106">Informationen zum Bereitstellen von MBAM mit der eigenständigen Topologie finden Sie unter [Architektur auf höherer Ebene von MBAM 2,5 mit eigenständiger Topologie](high-level-architecture-of-mbam-25-with-stand-alone-topology.md).</span><span class="sxs-lookup"><span data-stu-id="4707f-106">To deploy MBAM with the Stand-alone topology, see [High-Level Architecture of MBAM 2.5 with Stand-alone Topology](high-level-architecture-of-mbam-25-with-stand-alone-topology.md).</span></span>

<span data-ttu-id="4707f-107">Eine Liste der unterstützten Versionen der in diesem Thema erwähnten Software finden Sie unter [unterstützte MBAM 2,5-Konfigurationen](mbam-25-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="4707f-107">For a list of the supported versions of the software mentioned in this topic, see [MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md).</span></span>

<span data-ttu-id="4707f-108">**Wichtig**  Windows to go wird bei der Installation der Configuration Manager-Integrations Topologie nicht unterstützt, wenn Sie Configuration Manager 2007 verwenden.</span><span class="sxs-lookup"><span data-stu-id="4707f-108">**Important** Windows To Go is not supported for the Configuration Manager Integration topology installation when you are using Configuration Manager 2007.</span></span>

 

## <span data-ttu-id="4707f-109">Empfohlene Anzahl von Servern und unterstützte Anzahl von Clients</span><span class="sxs-lookup"><span data-stu-id="4707f-109">Recommended number of servers and supported number of clients</span></span>


<span data-ttu-id="4707f-110">Die empfohlene Anzahl von Servern und unterstützten Clients in einer Produktionsumgebung lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="4707f-110">The recommended number of servers and supported number of clients in a production environment is as follows:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="4707f-111">Empfohlene Architektur</span><span class="sxs-lookup"><span data-stu-id="4707f-111">Recommended architecture</span></span></th>
<th align="left"><span data-ttu-id="4707f-112">Details</span><span class="sxs-lookup"><span data-stu-id="4707f-112">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4707f-113">Anzahl der Server und anderer Computer</span><span class="sxs-lookup"><span data-stu-id="4707f-113">Number of servers and other computers</span></span></p></td>
<td align="left"><p><span data-ttu-id="4707f-114">Drei Server</span><span class="sxs-lookup"><span data-stu-id="4707f-114">Three servers</span></span></p>
<p><span data-ttu-id="4707f-115">Eine Workstation</span><span class="sxs-lookup"><span data-stu-id="4707f-115">One workstation</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4707f-116">Anzahl der unterstützten Clientcomputer</span><span class="sxs-lookup"><span data-stu-id="4707f-116">Number of client computers supported</span></span></p></td>
<td align="left"><p><span data-ttu-id="4707f-117">500.000</span><span class="sxs-lookup"><span data-stu-id="4707f-117">500,000</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="4707f-118">Unterschiede zwischen der Configuration Manager-Integration und eigenständigen Topologien</span><span class="sxs-lookup"><span data-stu-id="4707f-118">Differences between Configuration Manager Integration and stand-alone topologies</span></span>


<span data-ttu-id="4707f-119">Die wichtigsten Unterschiede zwischen den Topologien sind:</span><span class="sxs-lookup"><span data-stu-id="4707f-119">The main differences between the topologies are:</span></span>

-   <span data-ttu-id="4707f-120">Die Kompatibilitäts-und Berichterstattungsfeatures werden aus MBAM entfernt, und Sie können über den Configuration Manager darauf zugreifen.</span><span class="sxs-lookup"><span data-stu-id="4707f-120">The compliance and reporting features are removed from MBAM and are accessed from Configuration Manager.</span></span>

-   <span data-ttu-id="4707f-121">Berichte werden über die Configuration Manager-Verwaltungskonsole angezeigt, mit Ausnahme des Wiederherstellungs Überwachungsberichts, den Sie weiterhin über die MBAM-Website für Verwaltung und Überwachung anzeigen.</span><span class="sxs-lookup"><span data-stu-id="4707f-121">Reports are viewed from the Configuration Manager Management Console, with the exception of the Recovery Audit Report, which you continue to view from the MBAM Administration and Monitoring Website.</span></span>

## <span data-ttu-id="4707f-122">Empfohlene MBAM-Architektur auf höherer Ebene mit der Configuration Manager-Integrations Topologie</span><span class="sxs-lookup"><span data-stu-id="4707f-122">Recommended MBAM high-level architecture with the Configuration Manager Integration topology</span></span>


<span data-ttu-id="4707f-123">Das folgende Diagramm und die folgende Tabelle beschreiben die empfohlene allgemeine Architektur für MBAM mit der Configuration Manager-Integrations Topologie.</span><span class="sxs-lookup"><span data-stu-id="4707f-123">The following diagram and table describe the recommended high-level architecture for MBAM with the Configuration Manager Integration topology.</span></span> <span data-ttu-id="4707f-124">MBAM Multi-Forest-Bereitstellungen erfordern eine unidirektionale oder bidirektionale Vertrauensstellung.</span><span class="sxs-lookup"><span data-stu-id="4707f-124">MBAM multi-forest deployments require a one-way or two-way trust.</span></span> <span data-ttu-id="4707f-125">Unidirektionale Vertrauensstellungen setzen voraus, dass die Server Domäne der Clientdomäne vertraut.</span><span class="sxs-lookup"><span data-stu-id="4707f-125">One-way trusts require that the server domain trusts the client domain.</span></span>

![mbam2\-5](images/mbam2-5-cmserver.png)

### <span data-ttu-id="4707f-127">Datenbankserver</span><span class="sxs-lookup"><span data-stu-id="4707f-127">Database server</span></span>

#### <span data-ttu-id="4707f-128">Wiederherstellungsdatenbank</span><span class="sxs-lookup"><span data-stu-id="4707f-128">Recovery database</span></span>

<span data-ttu-id="4707f-129">Dieses Feature ist auf einem Computer mit Windows Server und unterstützten SQL Server-Instanzen konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="4707f-129">This feature is configured on a computer running Windows Server and supported SQL Server instance.</span></span>

<span data-ttu-id="4707f-130">Die **Wiederherstellungsdatenbank** speichert Wiederherstellungsdaten, die von MBAM-Client Computern erfasst werden.</span><span class="sxs-lookup"><span data-stu-id="4707f-130">The **Recovery Database** stores recovery data that is collected from MBAM Client computers.</span></span>

#### <span data-ttu-id="4707f-131">Überwachungsdatenbank</span><span class="sxs-lookup"><span data-stu-id="4707f-131">Audit database</span></span>

<span data-ttu-id="4707f-132">Dieses Feature ist auf einem Computer mit Windows Server und unterstützten SQL Server-Instanzen konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="4707f-132">This feature is configured on a computer running Windows Server and supported SQL Server instance.</span></span>

<span data-ttu-id="4707f-133">In der **Überwachungsdatenbank** werden Überwachungs Aktivitätsdaten gespeichert, die von Clientcomputern erfasst werden, die auf Wiederherstellungsdaten zugreifen.</span><span class="sxs-lookup"><span data-stu-id="4707f-133">The **Audit Database** stores audit activity data that is collected from client computers that have accessed recovery data.</span></span>

#### <span data-ttu-id="4707f-134">Berichte</span><span class="sxs-lookup"><span data-stu-id="4707f-134">Reports</span></span>

<span data-ttu-id="4707f-135">Dieses Feature ist auf einem Computer mit Windows Server und unterstützten SQL Server-Instanzen konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="4707f-135">This feature is configured on a computer running Windows Server and supported SQL Server instance.</span></span>

<span data-ttu-id="4707f-136">In den **Berichten** werden Wiederherstellungs Überwachungsdaten für die Clientcomputer in Ihrem Unternehmen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="4707f-136">The **Reports** provide recovery audit data for the client computers in your enterprise.</span></span> <span data-ttu-id="4707f-137">Sie können Berichte über die Configuration Manager-Konsole oder direkt in SQL Server Reporting Services anzeigen.</span><span class="sxs-lookup"><span data-stu-id="4707f-137">You can view reports from the Configuration Manager console or directly from SQL Server Reporting Services.</span></span>

### <span data-ttu-id="4707f-138">Primärer Configuration Manager-Standortserver</span><span class="sxs-lookup"><span data-stu-id="4707f-138">Configuration Manager primary site server</span></span>

<span data-ttu-id="4707f-139">System Center Configuration Manager-Integrations Feature</span><span class="sxs-lookup"><span data-stu-id="4707f-139">System Center Configuration Manager Integration feature</span></span>

-   <span data-ttu-id="4707f-140">Dieses Feature ist auf dem primären Configuration Manager-Standortserver konfiguriert, dem Server der obersten Ebene in Ihrer Configuration Manager-Infrastruktur.</span><span class="sxs-lookup"><span data-stu-id="4707f-140">This feature is configured on the Configuration Manager Primary Site Server, which is the top-tier server in your Configuration Manager infrastructure.</span></span>

-   <span data-ttu-id="4707f-141">Der **Configuration Manager-Server** sammelt die Hardwareinventurinformationen von Clientcomputern und wird verwendet, um die BitLocker-Kompatibilität von Clientcomputern zu melden.</span><span class="sxs-lookup"><span data-stu-id="4707f-141">The **Configuration Manager Server** collects the hardware inventory information from client computers and is used to report BitLocker compliance of client computers.</span></span>

-   <span data-ttu-id="4707f-142">Wenn Sie den Setup-Assistenten für die Microsoft BitLocker-Verwaltung und-Überwachung ausführen, um die Server Software zu installieren, werden die Auflistung der MBAM-unterstützten Computer, die Konfigurationsbasislinie und die Berichte auf dem primären Configuration Manager-Standortserver konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="4707f-142">When you run the Microsoft BitLocker Administration and Monitoring Setup wizard to install the server software, the MBAM Supported Computers collection, configuration baseline, and reports are configured on the Configuration Manager Primary Site Server.</span></span>

-   <span data-ttu-id="4707f-143">Die **Configuration Manager-Konsole** muss auf demselben Computer installiert sein, auf dem Sie die MBAM-Server Software installieren.</span><span class="sxs-lookup"><span data-stu-id="4707f-143">The **Configuration Manager console** must be installed on the same computer on which you install the MBAM Server software.</span></span>

### <span data-ttu-id="4707f-144">Verwaltungs-und Überwachungsserver</span><span class="sxs-lookup"><span data-stu-id="4707f-144">Administration and monitoring server</span></span>

#### <span data-ttu-id="4707f-145">Website "Verwaltung und Überwachung"</span><span class="sxs-lookup"><span data-stu-id="4707f-145">Administration and monitoring website</span></span>

<span data-ttu-id="4707f-146">Dieses Feature ist auf einem Computer mit Windows Server konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="4707f-146">This feature is configured on a computer running Windows Server.</span></span>

<span data-ttu-id="4707f-147">Die **Websiteverwaltung und Überwachung** wird verwendet, um Folgendes zu tun:</span><span class="sxs-lookup"><span data-stu-id="4707f-147">The **Administration and monitoring website** is used to:</span></span>

-   <span data-ttu-id="4707f-148">Helfen Sie den Endbenutzern beim wieder Zugriff auf Ihre Computer, wenn Sie gesperrt sind. (Dieser Bereich der Website wird im Allgemeinen als Help Desk bezeichnet.)</span><span class="sxs-lookup"><span data-stu-id="4707f-148">Help end users regain access to their computers when they are locked out. (This area of the Website is commonly called the Help Desk.)</span></span>

-   <span data-ttu-id="4707f-149">Anzeigen des Wiederherstellungs Überwachungsberichts, in dem Wiederherstellungsaktivitäten für Clientcomputer angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="4707f-149">View the Recovery Audit Report, which shows recovery activity for client computers.</span></span> <span data-ttu-id="4707f-150">Andere Berichte werden über die Configuration Manager-Konsole angezeigt.</span><span class="sxs-lookup"><span data-stu-id="4707f-150">Other reports are viewed from the Configuration Manager console.</span></span>

#### <span data-ttu-id="4707f-151">Self-Service-Portal</span><span class="sxs-lookup"><span data-stu-id="4707f-151">Self-service portal</span></span>

<span data-ttu-id="4707f-152">Dieses Feature ist auf einem Computer mit Windows Server konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="4707f-152">This feature is configured on a computer running Windows Server.</span></span>

<span data-ttu-id="4707f-153">Das **Self-Service-Portal** ist eine Website, auf der sich Endbenutzer auf Clientcomputern selbstständig an einer Website anmelden können, um einen Wiederherstellungsschlüssel abzurufen, wenn Sie Ihr BitLocker-Kennwort verlieren oder vergessen.</span><span class="sxs-lookup"><span data-stu-id="4707f-153">The **Self-Service Portal** is a website that enables end users on client computers to independently log on to a website to get a recovery key if they lose or forget their BitLocker password.</span></span>

#### <span data-ttu-id="4707f-154">Überwachen von Webdiensten für diese Website</span><span class="sxs-lookup"><span data-stu-id="4707f-154">Monitoring web services for this website</span></span>

<span data-ttu-id="4707f-155">Dieses Feature ist auf einem Computer mit Windows Server installiert.</span><span class="sxs-lookup"><span data-stu-id="4707f-155">This feature is installed on a computer running Windows Server.</span></span>

<span data-ttu-id="4707f-156">Die **Überwachungs-Webdienste** werden vom MBAM-Client und den Websites verwendet, um mit der Datenbank zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="4707f-156">The **monitoring web services** are used by the MBAM Client and the websites to communicate to the database.</span></span>

**<span data-ttu-id="4707f-157">Wichtig</span><span class="sxs-lookup"><span data-stu-id="4707f-157">Important</span></span>**<br><span data-ttu-id="4707f-158">Der Monitoring Web Service steht in der Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) 2,5 SP1 nicht mehr zur Verfügung, da die MBAM-Websites direkt mit der Wiederherstellungsdatenbank kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="4707f-158">The Monitoring Web Service is no longer available in Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 SP1 since the MBAM websites communicate directly with the Recovery Database.</span></span> 

 

### <span data-ttu-id="4707f-159">Verwaltungsarbeitsstation</span><span class="sxs-lookup"><span data-stu-id="4707f-159">Management workstation</span></span>

#### <span data-ttu-id="4707f-160">MBAM-Gruppenrichtlinienvorlagen</span><span class="sxs-lookup"><span data-stu-id="4707f-160">MBAM group policy templates</span></span>

-   <span data-ttu-id="4707f-161">Bei den **MBAM-Gruppenrichtlinienvorlagen** handelt es sich um Gruppenrichtlinieneinstellungen, die Implementierungs Einstellungen für MBAM definieren, mit denen Sie die BitLocker-Laufwerkverschlüsselung verwalten können.</span><span class="sxs-lookup"><span data-stu-id="4707f-161">The **MBAM Group Policy Templates** are Group Policy settings that define implementation settings for MBAM, which enable you to manage BitLocker drive encryption.</span></span>

-   <span data-ttu-id="4707f-162">Bevor Sie MBAM ausführen, müssen Sie die Gruppenrichtlinienvorlagen herunterladen, indem Sie [MDOP Gruppenrichtlinien (ADMX)-Vorlagen abrufen](https://go.microsoft.com/fwlink/p/?LinkId=393941) und auf einen Server oder eine Workstation kopieren, auf dem ein unterstütztes Windows-Server-oder Windows-Betriebssystem ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4707f-162">Before you run MBAM, you must download the Group Policy Templates from [How to Get MDOP Group Policy (.admx) Templates](https://go.microsoft.com/fwlink/p/?LinkId=393941) and copy them to a server or workstation that is running a supported Windows Server or Windows operating system.</span></span>

    **<span data-ttu-id="4707f-163">HINWEIS</span><span class="sxs-lookup"><span data-stu-id="4707f-163">NOTE</span></span>**<br><span data-ttu-id="4707f-164">Die Workstation muss kein dedizierter Computer sein.</span><span class="sxs-lookup"><span data-stu-id="4707f-164">The workstation does not have to be a dedicated computer.</span></span>

     

### <span data-ttu-id="4707f-165">MBAM-Client und Configuration Manager-Clientcomputer</span><span class="sxs-lookup"><span data-stu-id="4707f-165">MBAM Client and Configuration Manager Client computer</span></span>

#### <span data-ttu-id="4707f-166">MBAM-Client Software</span><span class="sxs-lookup"><span data-stu-id="4707f-166">MBAM Client software</span></span>

<span data-ttu-id="4707f-167">Der **MBAM-Client**:</span><span class="sxs-lookup"><span data-stu-id="4707f-167">The **MBAM Client**:</span></span>

-   <span data-ttu-id="4707f-168">Verwendet Gruppenrichtlinienobjekte, um die BitLocker-Laufwerkverschlüsselung auf Clientcomputern im Unternehmen durchzusetzen.</span><span class="sxs-lookup"><span data-stu-id="4707f-168">Uses Group Policy Objects to enforce BitLocker drive encryption on client computers in the enterprise.</span></span>

-   <span data-ttu-id="4707f-169">Sammelt den BitLocker-Wiederherstellungsschlüssel für drei Datenlaufwerk Typen: Betriebssystemlaufwerke, fest Netzlaufwerke und Wechseldatenträger (USB)-Datenlaufwerke.</span><span class="sxs-lookup"><span data-stu-id="4707f-169">Collects the BitLocker recovery key for three data drive types: operating system drives, fixed data drives, and removable (USB) data drives.</span></span>

-   <span data-ttu-id="4707f-170">Sammelt Wiederherstellungsinformationen und Computer Informationen zu den Clientcomputern.</span><span class="sxs-lookup"><span data-stu-id="4707f-170">Collects recovery information and computer information about the client computers.</span></span>

#### <span data-ttu-id="4707f-171">Konfigurations-Manager – Client</span><span class="sxs-lookup"><span data-stu-id="4707f-171">Configuration Manager Client</span></span>

<span data-ttu-id="4707f-172">Der **Configuration Manager-Client** ermöglicht es Configuration Manager, Hardware Kompatibilitätsdaten zu den Client Computern zu sammeln und Kompatibilitätsinformationen zu melden.</span><span class="sxs-lookup"><span data-stu-id="4707f-172">The **Configuration Manager Client** enables Configuration Manager to collect hardware compatibility data about the client computers and report compliance information.</span></span>

 

## <span data-ttu-id="4707f-173">Unterschiede in MBAM-Bereitstellung für unterstützte Configuration Manager-Versionen</span><span class="sxs-lookup"><span data-stu-id="4707f-173">Differences in MBAM deployment for supported Configuration Manager versions</span></span>


<span data-ttu-id="4707f-174">Wenn Sie MBAM mit der Configuration Manager-Integrations Topologie bereitstellen, können Sie MBAM auf einem primären Standortserver installieren.</span><span class="sxs-lookup"><span data-stu-id="4707f-174">When you deploy MBAM with the Configuration Manager Integration topology, you can install MBAM on a primary site server.</span></span> <span data-ttu-id="4707f-175">Die MBAM-Installation funktioniert jedoch anders für den System Center2012-Konfigurations-Manager und die Konfigurations Manager2007.</span><span class="sxs-lookup"><span data-stu-id="4707f-175">However, the MBAM installation works differently for System Center2012 Configuration Manager and Configuration Manager2007.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="4707f-176">Configuration Manager-Version</span><span class="sxs-lookup"><span data-stu-id="4707f-176">Configuration Manager version</span></span></th>
<th align="left"><span data-ttu-id="4707f-177">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4707f-177">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4707f-178">System Center2012 R2-Konfigurations-Manager</span><span class="sxs-lookup"><span data-stu-id="4707f-178">System Center2012 R2 Configuration Manager</span></span></p>
<p><span data-ttu-id="4707f-179">System Center2012-Konfigurations-Manager</span><span class="sxs-lookup"><span data-stu-id="4707f-179">System Center2012 Configuration Manager</span></span></p></td>
<td align="left"><p><span data-ttu-id="4707f-180">Wenn Sie MBAM auf einem primären Standortserver oder auf einem zentralen Administrationsserver installieren, führt MBAM alle Installationsaktionen auf diesem Website Server aus.</span><span class="sxs-lookup"><span data-stu-id="4707f-180">If you install MBAM on a primary site server or on a central administration server, MBAM performs all of the installation actions on that site server.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4707f-181">Konfigurations-Manager2007 R2</span><span class="sxs-lookup"><span data-stu-id="4707f-181">Configuration Manager2007 R2</span></span></p>
<p><span data-ttu-id="4707f-182">Konfigurations Manager2007</span><span class="sxs-lookup"><span data-stu-id="4707f-182">Configuration Manager2007</span></span></p></td>
<td align="left"><p><span data-ttu-id="4707f-183">Wenn Sie MBAM auf einem primären Standortserver installieren, der Teil einer größeren Configuration Manager-Hierarchie mit einem zentralen Standort übergeordneten Server ist, identifiziert MBAM den übergeordneten zentralen Standortserver und führt alle Installationsaktionen auf dem übergeordneten Server aus.</span><span class="sxs-lookup"><span data-stu-id="4707f-183">If you install MBAM on a primary site server that is part of a larger Configuration Manager hierarchy with a central site parent server, MBAM identifies the central site parent server and performs all of the installation actions on that parent server.</span></span> <span data-ttu-id="4707f-184">Die Installation umfasst das Überprüfen von Voraussetzungen und das Installieren der Configuration Manager-Objekte und-Berichte.</span><span class="sxs-lookup"><span data-stu-id="4707f-184">The installation includes checking prerequisites and installing the Configuration Manager objects and reports.</span></span></p>
<p><span data-ttu-id="4707f-185">Wenn Sie beispielsweise MBAM auf einem primären Standortserver installieren, der ein untergeordnetes Element eines übergeordneten zentralen Standortservers ist, installiert MBAM alle Configuration Manager-Objekte und-Berichte auf dem übergeordneten Server.</span><span class="sxs-lookup"><span data-stu-id="4707f-185">For example, if you install MBAM on a primary site server that is a child of a central site parent server, MBAM installs all of the Configuration Manager objects and reports on the parent server.</span></span> <span data-ttu-id="4707f-186">Wenn Sie MBAM auf dem übergeordneten Server installieren, führt MBAM alle Installationsaktionen auf dem übergeordneten Server aus.</span><span class="sxs-lookup"><span data-stu-id="4707f-186">If you install MBAM on the parent server, MBAM performs all of the installation actions on that parent server.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="4707f-187">Funktionsweise von MBAM mit Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="4707f-187">How MBAM works with Configuration Manager</span></span>


<span data-ttu-id="4707f-188">Die Integration von MBAM mit Configuration Manager basiert auf einem Konfigurationspaket, mit dem die in der folgenden Tabelle beschriebenen Elemente installiert werden.</span><span class="sxs-lookup"><span data-stu-id="4707f-188">The integration of MBAM with Configuration Manager is based on a configuration pack that installs the items described in the following table.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="4707f-189">Elemente, die in Configuration Manager installiert sind</span><span class="sxs-lookup"><span data-stu-id="4707f-189">Items installed into Configuration Manager</span></span></th>
<th align="left"><span data-ttu-id="4707f-190">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4707f-190">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4707f-191">Konfigurationsdaten</span><span class="sxs-lookup"><span data-stu-id="4707f-191">Configuration data</span></span></p></td>
<td align="left"><p><span data-ttu-id="4707f-192">Die Konfigurationsdaten installieren eine Konfigurationsbasislinie mit dem Namen "BitLocker-Schutz", die zwei Konfigurationselemente enthält:</span><span class="sxs-lookup"><span data-stu-id="4707f-192">The configuration data installs a configuration baseline, called “BitLocker Protection,” which contains two configuration items:</span></span></p>
<ul>
<li><p><span data-ttu-id="4707f-193">BitLocker-Betriebs System-Laufwerkschutz</span><span class="sxs-lookup"><span data-stu-id="4707f-193">BitLocker Operating System Drive Protection</span></span></p></li>
<li><p><span data-ttu-id="4707f-194">BitLocker-Datenlaufwerke mit fester Datensicherheit</span><span class="sxs-lookup"><span data-stu-id="4707f-194">BitLocker Fixed Data Drives Protection</span></span></p></li>
</ul>
<p><span data-ttu-id="4707f-195">Die Konfigurationsbasislinie wird in der MBAM-unterstützten Computersammlung bereitgestellt, die auch bei der Installation von MBAM erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="4707f-195">The configuration baseline is deployed to the MBAM Supported Computers collection, which is also created when MBAM is installed.</span></span></p>
<p><span data-ttu-id="4707f-196">Die beiden Konfigurationselemente stellen die Grundlage für die Auswertung des Kompatibilitätsstatus der Clientcomputer dar.</span><span class="sxs-lookup"><span data-stu-id="4707f-196">The two configuration items provide the basis for evaluating the compliance status of the client computers.</span></span> <span data-ttu-id="4707f-197">Diese Informationen werden in Configuration Manager erfasst, gespeichert und ausgewertet.</span><span class="sxs-lookup"><span data-stu-id="4707f-197">This information is captured, stored, and evaluated in Configuration Manager.</span></span></p>
<p><span data-ttu-id="4707f-198">Die Konfigurationselemente basieren auf den Compliance-Anforderungen für Betriebssystemlaufwerke und fest Netzlaufwerke.</span><span class="sxs-lookup"><span data-stu-id="4707f-198">The configuration items are based on the compliance requirements for operating system drives and fixed data drives.</span></span> <span data-ttu-id="4707f-199">Die erforderlichen Details für die bereitgestellten Computer werden erfasst, damit die Kompatibilität dieser Laufwerktypen ausgewertet werden kann.</span><span class="sxs-lookup"><span data-stu-id="4707f-199">The required details for the deployed computers are collected so that the compliance for those drive types can be evaluated.</span></span></p>
<p><span data-ttu-id="4707f-200">Standardmäßig wertet die Konfigurationsbasislinie den Kompatibilitätsstatus every12 Stunden aus und sendet die Kompatibilitätsdaten an Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="4707f-200">By default, the configuration baseline evaluates the compliance status every12 hours and sends the compliance data to Configuration Manager.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4707f-201">MBAM-unterstützte Computersammlung</span><span class="sxs-lookup"><span data-stu-id="4707f-201">MBAM Supported Computers collection</span></span></p></td>
<td align="left"><p><span data-ttu-id="4707f-202">MBAM erstellt eine Sammlung, die als MBAM unterstützte Computer bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="4707f-202">MBAM creates a collection that is called MBAM Supported Computers.</span></span> <span data-ttu-id="4707f-203">Die Konfigurationsbasislinie richtet sich an Clientcomputer, die in dieser Sammlung enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="4707f-203">The configuration baseline is targeted to client computers that are in this collection.</span></span></p>
<p><span data-ttu-id="4707f-204">Hierbei handelt es sich um eine dynamische Sammlung.</span><span class="sxs-lookup"><span data-stu-id="4707f-204">This is a dynamic collection.</span></span> <span data-ttu-id="4707f-205">Standardmäßig wird every12 Stunden ausgeführt, und die Mitgliedschaft wird anhand von drei Kriterien ausgewertet:</span><span class="sxs-lookup"><span data-stu-id="4707f-205">By default, it runs every12 hours and evaluates membership, based on three criteria:</span></span></p>
<ul>
<li><p><span data-ttu-id="4707f-206">Der Computer ist eine unterstützte Version des Windows-Betriebssystems.</span><span class="sxs-lookup"><span data-stu-id="4707f-206">The computer is a supported version of the Windows operating system.</span></span></p></li>
<li><p><span data-ttu-id="4707f-207">Der Computer ist ein physikalischer Computer.</span><span class="sxs-lookup"><span data-stu-id="4707f-207">The computer is a physical computer.</span></span> <span data-ttu-id="4707f-208">Virtuelle Computer werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4707f-208">Virtual machines are not supported.</span></span></p></li>
<li><p><span data-ttu-id="4707f-209">Der Computer verfügt über ein Trusted Platform Module (TPM), das verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="4707f-209">The computer has a Trusted Platform Module (TPM) that is available.</span></span> <span data-ttu-id="4707f-210">Eine kompatible Version von TPM 1.2 oder höher ist für Windows7 erforderlich.</span><span class="sxs-lookup"><span data-stu-id="4707f-210">A compatible version of TPM1.2 or later is required for Windows7.</span></span> <span data-ttu-id="4707f-211">Für Windows10, Windows 8.1, Windows8 und Windows to go ist kein TPM erforderlich.</span><span class="sxs-lookup"><span data-stu-id="4707f-211">Windows10, Windows8.1, Windows8, and Windows To Go do not require a TPM.</span></span></p></li>
</ul>
<p><span data-ttu-id="4707f-212">Die Sammlung wird für alle Computer ausgewertet, und es wird eine Teilmenge der kompatiblen Computer erstellt, die die Grundlage für die Kompatibilitäts Auswertung und-Berichterstellung für die MBAM-Integration bildet.</span><span class="sxs-lookup"><span data-stu-id="4707f-212">The collection is evaluated against all computers and a subset of compatible computers is created, which provides the basis for compliance evaluation and reporting for the MBAM integration.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4707f-213">Berichte</span><span class="sxs-lookup"><span data-stu-id="4707f-213">Reports</span></span></p></td>
<td align="left"><p><span data-ttu-id="4707f-214">Wenn Sie MBAM mit der Configuration Manager-Integrations Topologie konfigurieren, werden alle Berichte in Configuration Manager mit Ausnahme des Wiederherstellungs Überwachungsberichts angezeigt, von dem Sie auf der Website für die MBAM-Verwaltung und-Überwachung weiterhin angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="4707f-214">When you configure MBAM with the Configuration Manager Integration topology, you view all reports in Configuration Manager, except the Recovery Audit Report, the latter of which you continue to view in the MBAM Administration and Monitoring Website.</span></span> <span data-ttu-id="4707f-215">Die in Configuration Manager verfügbaren Berichte lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="4707f-215">The reports available in Configuration Manager are:</span></span></p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="4707f-216">Bericht</span><span class="sxs-lookup"><span data-stu-id="4707f-216">Report</span></span></th>
<th align="left"><span data-ttu-id="4707f-217">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4707f-217">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4707f-218">BitLocker Enterprise Compliance-Dashboard</span><span class="sxs-lookup"><span data-stu-id="4707f-218">BitLocker Enterprise Compliance Dashboard</span></span></p></td>
<td align="left"><p><span data-ttu-id="4707f-219">Bietet IT-Administratoren drei Ansichten von Informationen in einem einzigen Bericht: Kompatibilitätsstatus Verteilung, nicht kompatibel – Fehlerverteilung und Kompatibilitätsstatus Verteilung nach Laufwerks.</span><span class="sxs-lookup"><span data-stu-id="4707f-219">Gives IT administrators three views of information in a single report: Compliance Status Distribution, Non Compliant – Errors Distribution, and Compliance Status Distribution By Drive Type.</span></span> <span data-ttu-id="4707f-220">Mit den Drilldown-Optionen im Bericht können IT-Administratoren durch die Daten klicken und eine Liste der Computer anzeigen, die dem ausgewählten Zustand entsprechen.</span><span class="sxs-lookup"><span data-stu-id="4707f-220">Drill-down options on the report let IT administrators click through the data and view a list of computers that match the selected state.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4707f-221">Details zur BitLocker-Unternehmenskonformität</span><span class="sxs-lookup"><span data-stu-id="4707f-221">BitLocker Enterprise Compliance Details</span></span></p></td>
<td align="left"><p><span data-ttu-id="4707f-222">Ermöglicht IT-Administratoren die Anzeige von Informationen über den BitLocker-Verschlüsselungs Kompatibilitätsstatus des Unternehmens und umfasst den Kompatibilitätsstatus für jeden Computer.</span><span class="sxs-lookup"><span data-stu-id="4707f-222">Lets IT administrators view information about the BitLocker encryption compliance status of the enterprise and includes the compliance status for each computer.</span></span> <span data-ttu-id="4707f-223">Mit den Drilldown-Optionen im Bericht können IT-Administratoren durch die Daten klicken und eine Liste der Computer anzeigen, die dem ausgewählten Zustand entsprechen.</span><span class="sxs-lookup"><span data-stu-id="4707f-223">Drill-down options on the report let IT administrators click through the data and view a list of computers that match the selected state.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4707f-224">BitLocker-Computer Konformität</span><span class="sxs-lookup"><span data-stu-id="4707f-224">BitLocker Computer Compliance</span></span></p></td>
<td align="left"><p><span data-ttu-id="4707f-225">Ermöglicht es Administratoren, einen einzelnen Computer anzuzeigen und zu ermitteln, warum er mit dem Status "kompatibel" oder "nicht kompatibel" gemeldet wurde.</span><span class="sxs-lookup"><span data-stu-id="4707f-225">Lets IT administrators view an individual computer and determine why it was reported with a status of compliant or not compliant.</span></span> <span data-ttu-id="4707f-226">Der Bericht zeigt auch den Verschlüsselungsstatus der Betriebssystemlaufwerke und fest Netzlaufwerke an.</span><span class="sxs-lookup"><span data-stu-id="4707f-226">The report also displays the encryption state of the operating system drives and fixed data drives.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4707f-227">Zusammenfassung der BitLocker-Unternehmenskonformität</span><span class="sxs-lookup"><span data-stu-id="4707f-227">BitLocker Enterprise Compliance Summary</span></span></p></td>
<td align="left"><p><span data-ttu-id="4707f-228">Damit können IT-Administratoren den Status der MBAM-Richtlinienkonformität im Unternehmen anzeigen.</span><span class="sxs-lookup"><span data-stu-id="4707f-228">Lets IT administrators view the status of MBAM policy compliance in the enterprise.</span></span> <span data-ttu-id="4707f-229">Der Status jedes Computers wird ausgewertet, und der Bericht zeigt eine Zusammenfassung der Konformität aller Computer im Unternehmen mit der Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="4707f-229">Each computer’s state is evaluated, and the report shows a summary of the compliance of all computers in the enterprise against the policy.</span></span> <span data-ttu-id="4707f-230">Mit den Drilldown-Optionen im Bericht können IT-Administratoren durch die Daten klicken und eine Liste der Computer anzeigen, die dem ausgewählten Zustand entsprechen.</span><span class="sxs-lookup"><span data-stu-id="4707f-230">Drill-down options on the report let IT administrators click through the data and view a list of computers that match the selected state.</span></span></p></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
</tbody>
</table>

 


## <span data-ttu-id="4707f-231">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="4707f-231">Related topics</span></span>


[<span data-ttu-id="4707f-232">Erste Schritte mit MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="4707f-232">Getting Started with MBAM 2.5</span></span>](getting-started-with-mbam-25.md)

[<span data-ttu-id="4707f-233">High-Level-Architektur von MBAM 2.5 mit eigenständiger Topologie</span><span class="sxs-lookup"><span data-stu-id="4707f-233">High-Level Architecture of MBAM 2.5 with Stand-alone Topology</span></span>](high-level-architecture-of-mbam-25-with-stand-alone-topology.md)

[<span data-ttu-id="4707f-234">Beschreibung der Funktionen einer MBAM 2.5-Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="4707f-234">Illustrated Features of an MBAM 2.5 Deployment</span></span>](illustrated-features-of-an-mbam-25-deployment.md)

 

 
## <span data-ttu-id="4707f-235">Sie haben einen Vorschlag für MBAM?</span><span class="sxs-lookup"><span data-stu-id="4707f-235">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="4707f-236">[Hier](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)können Sie Vorschläge hinzufügen oder abstimmen.</span><span class="sxs-lookup"><span data-stu-id="4707f-236">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="4707f-237">Bei MBAM-Problemen verwenden Sie das [MBAM TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="4707f-237">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>




