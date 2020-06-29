---
title: Bestimmen der Streaming-Methode
description: Bestimmen der Streaming-Methode
author: dansimp
ms.assetid: 50d5e0ec-7f48-4cea-8711-5882bd89153b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0acfd345ac55f11476cffe94b3a95b13c5d8f303
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808893"
---
# <span data-ttu-id="c1cca-103">Bestimmen der Streaming-Methode</span><span class="sxs-lookup"><span data-stu-id="c1cca-103">Determine Your Streaming Method</span></span>


<span data-ttu-id="c1cca-104">Wenn ein Benutzer zum ersten Mal auf das Symbol doppelklickt, das über den Veröffentlichungsprozess auf einem Computer gespeichert wurde, erhält der Application Virtualization-Client den Inhalt des virtuellen Anwendungspakets von einem Streaming Source-Speicherort.</span><span class="sxs-lookup"><span data-stu-id="c1cca-104">The first time that a user double-clicks the icon that has been placed on a computer through the publishing process, the Application Virtualization client will obtain the virtual application package content from a streaming source location.</span></span>

<span data-ttu-id="c1cca-105">**Hinweis** 
 *Streaming* ist der Ausdruck, der verwendet wird, um den Prozess zum Abrufen von Inhalten aus einem sequenzierten Anwendungspaket zu beschreiben, beginnend mit dem primären Feature-Block und anschließendes Abrufen zusätzlicher Blöcke nach Bedarf.</span><span class="sxs-lookup"><span data-stu-id="c1cca-105">**Note**
*Streaming* is the term used to describe the process of obtaining content from a sequenced application package, starting with the primary feature block and then obtaining additional blocks as needed.</span></span>

 

<span data-ttu-id="c1cca-106">Der Speicherort der Streaming-Quelle ist in der Regel ein Server, auf den der Computer des Benutzers zugreifen kann. einige elektronische Verteilungssysteme wie Microsoft Endpoint Configuration Manager können die SFT-Datei jedoch auf dem Computer des Benutzers verteilen und dann das virtuelle Anwendungspaket lokal aus dem Cache dieses Computers streamen.</span><span class="sxs-lookup"><span data-stu-id="c1cca-106">The streaming source location is usually a server that is accessible by the user’s computer; however, some electronic distribution systems, such as Microsoft Endpoint Configuration Manager, can distribute the SFT file to the user’s computer and then stream the virtual application package locally from that computer’s cache.</span></span>

<span data-ttu-id="c1cca-107">**Hinweis**  Ein Streaming-Quellspeicherort für virtuelle Pakete kann auf einem Computer eingerichtet werden, auf dem es sich nicht um einen Server handelt.</span><span class="sxs-lookup"><span data-stu-id="c1cca-107">**Note** A streaming source location for virtual packages can be set up on a computer that is not a server.</span></span> <span data-ttu-id="c1cca-108">Dies ist besonders hilfreich in einer kleinen Zweigstelle, die keinen Server hat.</span><span class="sxs-lookup"><span data-stu-id="c1cca-108">This is especially useful in a small branch office that has no server.</span></span>

 

<span data-ttu-id="c1cca-109">Die Streaming-Quellen, die zum Speichern sequenzierter Anwendungen verwendet werden können, werden in der folgenden Tabelle beschrieben.</span><span class="sxs-lookup"><span data-stu-id="c1cca-109">The streaming sources that can be used to store sequenced applications are described in the following table.</span></span>

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
<th align="left"><span data-ttu-id="c1cca-110">Servertyp</span><span class="sxs-lookup"><span data-stu-id="c1cca-110">Server Type</span></span></th>
<th align="left"><span data-ttu-id="c1cca-111">Protokoll</span><span class="sxs-lookup"><span data-stu-id="c1cca-111">Protocol</span></span></th>
<th align="left"><span data-ttu-id="c1cca-112">Vorteile</span><span class="sxs-lookup"><span data-stu-id="c1cca-112">Advantages</span></span></th>
<th align="left"><span data-ttu-id="c1cca-113">Nachteile</span><span class="sxs-lookup"><span data-stu-id="c1cca-113">Disadvantages</span></span></th>
<th align="left"><span data-ttu-id="c1cca-114">Links</span><span class="sxs-lookup"><span data-stu-id="c1cca-114">Links</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c1cca-115">Dateiserver</span><span class="sxs-lookup"><span data-stu-id="c1cca-115">File server</span></span></p></td>
<td align="left"><p><span data-ttu-id="c1cca-116">Datei</span><span class="sxs-lookup"><span data-stu-id="c1cca-116">File</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="c1cca-117">Einfache, kostengünstige Lösung zum Konfigurieren eines vorhandenen Dateiservers mit \Content-Freigabe</span><span class="sxs-lookup"><span data-stu-id="c1cca-117">Simple low-cost solution to configure existing file server with \CONTENT share</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="c1cca-118">Kein aktives Upgrade</span><span class="sxs-lookup"><span data-stu-id="c1cca-118">No active upgrade</span></span></p></li>
</ul></td>
<td align="left"><p><a href="how-to-configure-the-file-server.md" data-raw-source="[How to Configure the File Server](how-to-configure-the-file-server.md)"><span data-ttu-id="c1cca-119">So konfigurieren Sie den Dateiserver</span><span class="sxs-lookup"><span data-stu-id="c1cca-119">How to Configure the File Server</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c1cca-120">IIS-Server</span><span class="sxs-lookup"><span data-stu-id="c1cca-120">IIS server</span></span></p></td>
<td align="left"><p><span data-ttu-id="c1cca-121">HTTP/https</span><span class="sxs-lookup"><span data-stu-id="c1cca-121">HTTP/ HTTPS</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="c1cca-122">Unterstützt erhöhte Sicherheit mit HTTPS-Protokoll.</span><span class="sxs-lookup"><span data-stu-id="c1cca-122">Supports enhanced security using HTTPS protocol.</span></span></p></li>
<li><p><span data-ttu-id="c1cca-123">Unterstützt das Streaming an Remotecomputer über das Internet</span><span class="sxs-lookup"><span data-stu-id="c1cca-123">Supports streaming to remote computers across the Internet</span></span></p></li>
<li><p><span data-ttu-id="c1cca-124">Nur ein Port in der Firewall zu öffnen</span><span class="sxs-lookup"><span data-stu-id="c1cca-124">Only one port in firewall to open</span></span></p></li>
<li><p><span data-ttu-id="c1cca-125">Hochgradig skalierbar</span><span class="sxs-lookup"><span data-stu-id="c1cca-125">Highly scalable</span></span></p></li>
<li><p><span data-ttu-id="c1cca-126">Vertrautes Protokoll</span><span class="sxs-lookup"><span data-stu-id="c1cca-126">Familiar protocol</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="c1cca-127">IIS muss verwaltet werden</span><span class="sxs-lookup"><span data-stu-id="c1cca-127">Need to manage IIS</span></span></p></li>
<li><p><span data-ttu-id="c1cca-128">Kein aktives Upgrade</span><span class="sxs-lookup"><span data-stu-id="c1cca-128">No active upgrade</span></span></p></li>
</ul></td>
<td align="left"><p><a href="how-to-configure-the-server-for-iis.md" data-raw-source="[How to Configure the Server for IIS](how-to-configure-the-server-for-iis.md)"><span data-ttu-id="c1cca-129">So konfigurieren Sie den Server für IIS</span><span class="sxs-lookup"><span data-stu-id="c1cca-129">How to Configure the Server for IIS</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c1cca-130">Application Virtualization Streaming Server</span><span class="sxs-lookup"><span data-stu-id="c1cca-130">Application Virtualization Streaming Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="c1cca-131">RTSP/RTSPS</span><span class="sxs-lookup"><span data-stu-id="c1cca-131">RTSP/ RTSPS</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="c1cca-132">Aktives Upgrade</span><span class="sxs-lookup"><span data-stu-id="c1cca-132">Active upgrade</span></span></p></li>
<li><p><span data-ttu-id="c1cca-133">Unterstützt erweiterte Sicherheit mithilfe des RTSPS-Protokolls</span><span class="sxs-lookup"><span data-stu-id="c1cca-133">Supports enhanced security using RTSPS protocol</span></span></p></li>
<li><p><span data-ttu-id="c1cca-134">Nur ein Port in der Firewall zu öffnen (nur RTSPS)</span><span class="sxs-lookup"><span data-stu-id="c1cca-134">Only one port in firewall to open (RTSPS only)</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="c1cca-135">Duale Infrastruktur</span><span class="sxs-lookup"><span data-stu-id="c1cca-135">Dual infrastructure</span></span></p></li>
<li><p><span data-ttu-id="c1cca-136">Server Verwaltungsanforderung</span><span class="sxs-lookup"><span data-stu-id="c1cca-136">Server administration requirement</span></span></p></li>
</ul></td>
<td align="left"><p><a href="how-to-configure-the-application-virtualization-management-servers.md" data-raw-source="[How to Configure the Application Virtualization Management Servers](how-to-configure-the-application-virtualization-management-servers.md)"><span data-ttu-id="c1cca-137">So konfigurieren Sie Anwendung Virtualisierung Management Server</span><span class="sxs-lookup"><span data-stu-id="c1cca-137">How to Configure the Application Virtualization Management Servers</span></span></a></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="c1cca-138">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="c1cca-138">Related topics</span></span>


[<span data-ttu-id="c1cca-139">Electronic Software Distribution-basiertes Szenario</span><span class="sxs-lookup"><span data-stu-id="c1cca-139">Electronic Software Distribution-Based Scenario</span></span>](electronic-software-distribution-based-scenario.md)

[<span data-ttu-id="c1cca-140">Übersicht über Electronic Software Distribution-basierte Szenarien</span><span class="sxs-lookup"><span data-stu-id="c1cca-140">Electronic Software Distribution-Based Scenario Overview</span></span>](electronic-software-distribution-based-scenario-overview.md)

[<span data-ttu-id="c1cca-141">Bestimmen der Veröffentlichungsmethode</span><span class="sxs-lookup"><span data-stu-id="c1cca-141">Determine Your Publishing Method</span></span>](determine-your-publishing-method.md)

 

 





