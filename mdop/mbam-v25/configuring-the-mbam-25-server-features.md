---
title: Konfigurieren der MBAM 2.5-Serverfunktionen
description: Konfigurieren der MBAM 2.5-Serverfunktionen
author: dansimp
ms.assetid: 894d1080-5f13-48f7-8fde-82f8d440a4ed
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e6ba2fc49086acf698f61b9997505c8fa884c0eb
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809727"
---
# <span data-ttu-id="1429b-103">Konfigurieren der MBAM 2.5-Serverfunktionen</span><span class="sxs-lookup"><span data-stu-id="1429b-103">Configuring the MBAM 2.5 Server Features</span></span>


<span data-ttu-id="1429b-104">Verwenden Sie diese Informationen als Ausgangspunkt für die Konfiguration der Microsoft BitLocker-MBAM-2,5-Server Features nach [der Installation der MBAM 2,5-Server Software](installing-the-mbam-25-server-software.md).</span><span class="sxs-lookup"><span data-stu-id="1429b-104">Use this information as a starting place for configuring Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 Server features after [Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md).</span></span> <span data-ttu-id="1429b-105">Es gibt zwei Methoden, mit denen Sie MBAM konfigurieren können:</span><span class="sxs-lookup"><span data-stu-id="1429b-105">There are two methods you can use to configure MBAM:</span></span>

-   <span data-ttu-id="1429b-106">MBAM-Serverkonfigurations-Assistent</span><span class="sxs-lookup"><span data-stu-id="1429b-106">MBAM Server Configuration wizard</span></span>

-   <span data-ttu-id="1429b-107">Windows PowerShell-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="1429b-107">Windows PowerShell cmdlets</span></span>

## <span data-ttu-id="1429b-108">Bevor Sie mit dem Konfigurieren der MBAM-Server Features beginnen</span><span class="sxs-lookup"><span data-stu-id="1429b-108">Before you start configuring MBAM Server features</span></span>


<span data-ttu-id="1429b-109">Überprüfen und führen Sie die folgenden Schritte aus, bevor Sie mit dem Konfigurieren der MBAM-Server Features beginnen:</span><span class="sxs-lookup"><span data-stu-id="1429b-109">Review and complete the following steps before you start configuring the MBAM Server features:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="1429b-110">Schritt</span><span class="sxs-lookup"><span data-stu-id="1429b-110">Step</span></span></th>
<th align="left"><span data-ttu-id="1429b-111">Wo erhalte ich Anweisungen?</span><span class="sxs-lookup"><span data-stu-id="1429b-111">Where to get instructions</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1429b-112">Überprüfen Sie die empfohlene Architektur für MBAM.</span><span class="sxs-lookup"><span data-stu-id="1429b-112">Review the recommended architecture for MBAM.</span></span></p></td>
<td align="left"><p><a href="high-level-architecture-for-mbam-25.md" data-raw-source="[High-Level Architecture for MBAM 2.5](high-level-architecture-for-mbam-25.md)"><span data-ttu-id="1429b-113">High-Level-Architektur für MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="1429b-113">High-Level Architecture for MBAM 2.5</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1429b-114">Überprüfen Sie die unterstützten Konfigurationen für MBAM.</span><span class="sxs-lookup"><span data-stu-id="1429b-114">Review the supported configurations for MBAM.</span></span></p></td>
<td align="left"><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)"><span data-ttu-id="1429b-115">Von MBAM 2.5 unterstützte Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="1429b-115">MBAM 2.5 Supported Configurations</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1429b-116">Führen Sie die erforderlichen Voraussetzungen für jeden Server aus.</span><span class="sxs-lookup"><span data-stu-id="1429b-116">Complete the required prerequisites on each server.</span></span></p></td>
<td align="left"><ul>
<li><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)"><span data-ttu-id="1429b-117">MBAM 2.5-Servervoraussetzungen für eigenständige und Configuration Manager-Integrationstopologien</span><span class="sxs-lookup"><span data-stu-id="1429b-117">MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies</span></span></a></p></li>
<li><p><a href="mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md" data-raw-source="[MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md)"><span data-ttu-id="1429b-118">MBAM 2.5-Servervoraussetzungen, die nur für die Configuration Manager-Integrationstopologie gelten</span><span class="sxs-lookup"><span data-stu-id="1429b-118">MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology</span></span></a></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1429b-119">Installieren Sie die MBAM-Server Software auf jedem Server, auf dem Sie ein MBAM-Server Feature konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="1429b-119">Install the MBAM Server software on each server where you will configure an MBAM Server feature.</span></span></p></td>
<td align="left"><p><a href="installing-the-mbam-25-server-software.md" data-raw-source="[Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md)"><span data-ttu-id="1429b-120">Installieren der MBAM 2.5-Serversoftware</span><span class="sxs-lookup"><span data-stu-id="1429b-120">Installing the MBAM 2.5 Server Software</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1429b-121">Überprüfen Sie die Voraussetzungen für die Verwendung von Windows PowerShell zum Konfigurieren von MBAM-Server Features (wenn Sie diese Methode zum Konfigurieren von MBAM-Server Features verwenden).</span><span class="sxs-lookup"><span data-stu-id="1429b-121">Review the prerequisites for using Windows PowerShell to configure MBAM Server features (if you are using this method to configure MBAM Server features).</span></span></p></td>
<td align="left"><p><a href="configuring-mbam-25-server-features-by-using-windows-powershell.md" data-raw-source="[Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)"><span data-ttu-id="1429b-122">Konfigurieren von MBAM 2.5 Serverfunktionen mithilfe von Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="1429b-122">Configuring MBAM 2.5 Server Features by Using Windows PowerShell</span></span></a></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="1429b-123">Schritte zum Konfigurieren der MBAM-Server Features</span><span class="sxs-lookup"><span data-stu-id="1429b-123">Steps for configuring MBAM Server features</span></span>


<span data-ttu-id="1429b-124">In jeder Zeile in der folgenden Tabelle werden die Features beschrieben, die Sie auf einem separaten Server konfigurieren, entsprechend der empfohlenen [allgemeinen Architektur für MBAM 2,5](high-level-architecture-for-mbam-25.md).</span><span class="sxs-lookup"><span data-stu-id="1429b-124">Each row in the following table describes the features that you will configure on a separate server, according to the recommended [High-Level Architecture for MBAM 2.5](high-level-architecture-for-mbam-25.md).</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="1429b-125">Zu installierende Features</span><span class="sxs-lookup"><span data-stu-id="1429b-125">Features to install</span></span></th>
<th align="left"><span data-ttu-id="1429b-126">Wo erhalte ich Anweisungen?</span><span class="sxs-lookup"><span data-stu-id="1429b-126">Where to get instructions</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1429b-127">Konfigurieren Sie die Datenbanken.</span><span class="sxs-lookup"><span data-stu-id="1429b-127">Configure the databases.</span></span></p></td>
<td align="left"><p><a href="how-to-configure-the-mbam-25-databases.md" data-raw-source="[How to Configure the MBAM 2.5 Databases](how-to-configure-the-mbam-25-databases.md)"><span data-ttu-id="1429b-128">So konfigurieren Sie die MBAM 2.5-Datenbanken</span><span class="sxs-lookup"><span data-stu-id="1429b-128">How to Configure the MBAM 2.5 Databases</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1429b-129">Konfigurieren Sie die Berichte.</span><span class="sxs-lookup"><span data-stu-id="1429b-129">Configure the reports.</span></span></p></td>
<td align="left"><p><a href="how-to-configure-the-mbam-25-reports.md" data-raw-source="[How to Configure the MBAM 2.5 Reports](how-to-configure-the-mbam-25-reports.md)"><span data-ttu-id="1429b-130">So konfigurieren Sie die MBAM 2.5-Berichte</span><span class="sxs-lookup"><span data-stu-id="1429b-130">How to Configure the MBAM 2.5 Reports</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1429b-131">Konfigurieren Sie die Webanwendungen.</span><span class="sxs-lookup"><span data-stu-id="1429b-131">Configure the web applications.</span></span></p></td>
<td align="left"><p><a href="how-to-configure-the-mbam-25-web-applications.md" data-raw-source="[How to Configure the MBAM 2.5 Web Applications](how-to-configure-the-mbam-25-web-applications.md)"><span data-ttu-id="1429b-132">So konfigurieren Sie die MBAM 2.5-Webanwendungen</span><span class="sxs-lookup"><span data-stu-id="1429b-132">How to Configure the MBAM 2.5 Web Applications</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1429b-133">Konfigurieren Sie die System Center Configuration Manager-Integration (falls zutreffend).</span><span class="sxs-lookup"><span data-stu-id="1429b-133">Configure the System Center Configuration Manager Integration (if applicable).</span></span></p></td>
<td align="left"><p><a href="how-to-configure-the-mbam-25-system-center-configuration-manager-integration.md" data-raw-source="[How to Configure the MBAM 2.5 System Center Configuration Manager Integration](how-to-configure-the-mbam-25-system-center-configuration-manager-integration.md)"><span data-ttu-id="1429b-134">So konfigurieren Sie die Integration von MBAM 2.5 in System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="1429b-134">How to Configure the MBAM 2.5 System Center Configuration Manager Integration</span></span></a></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="1429b-135">Eine Liste der Ereignisse zur Konfiguration von MBAM Server-Features finden Sie unter [Serverereignisprotokolle](server-event-logs.md).</span><span class="sxs-lookup"><span data-stu-id="1429b-135">For a list of events about MBAM Server feature configuration, see [Server Event Logs](server-event-logs.md).</span></span>



## <span data-ttu-id="1429b-136">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="1429b-136">Related topics</span></span>


<span data-ttu-id="1429b-137">Konfigurieren der MBAM 2.5-Serverfunktionen</span><span class="sxs-lookup"><span data-stu-id="1429b-137">Configuring the MBAM 2.5 Server Features</span></span>
 

 
## <span data-ttu-id="1429b-138">Sie haben einen Vorschlag für MBAM?</span><span class="sxs-lookup"><span data-stu-id="1429b-138">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="1429b-139">[Hier](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)können Sie Vorschläge hinzufügen oder abstimmen.</span><span class="sxs-lookup"><span data-stu-id="1429b-139">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="1429b-140">Bei MBAM-Problemen verwenden Sie das [MBAM TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="1429b-140">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>




