---
title: Mit dem Internet verbundene Szenarien für Umkreisnetzwerke
description: Mit dem Internet verbundene Szenarien für Umkreisnetzwerke
author: dansimp
ms.assetid: 8a4da6e6-82c7-49e5-b9b1-1666cba02f65
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: fcb04e651341fa107c358eaabbd7992d7ea155ec
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806644"
---
# <span data-ttu-id="01540-103">Mit dem Internet verbundene Szenarien für Umkreisnetzwerke</span><span class="sxs-lookup"><span data-stu-id="01540-103">Internet-Facing Server Scenarios for Perimeter Networks</span></span>


<span data-ttu-id="01540-104">App-v 4.5 unterstützt Server Szenarien mit Internet Verbindung, bei denen Benutzer, die nicht mit dem Unternehmensnetzwerk verbunden sind oder die Verbindung mit dem Netzwerk trennen, weiterhin App-v verwenden können.</span><span class="sxs-lookup"><span data-stu-id="01540-104">App-V4.5 supports Internet-facing server scenarios, in which users who are not connected to the corporate network or who disconnect from the network can still use App-V.</span></span> <span data-ttu-id="01540-105">Wie in der folgenden Abbildung zu sehen ist, wird nur die Verwendung von sicheren Protokollen im Internet (RTSPS und HTTPS) unterstützt.</span><span class="sxs-lookup"><span data-stu-id="01540-105">As shown in the following illustration, only the use of secure protocols on the Internet (RTSPS and HTTPS) is supported.</span></span>

![App-v-Firewall-Positionierungs Diagramm](images/appvfirewalls.gif)

<span data-ttu-id="01540-107">Sie können eine mit dem Internet verbundene Lösung mithilfe eines ISA-Servers einrichten, in dem sich die App-V-Infrastruktur wie folgt auf dem internen Netzwerk befindet:</span><span class="sxs-lookup"><span data-stu-id="01540-107">You can set up an Internet-facing solution, using an ISA Server, where the App-V infrastructure is on the internal network in the following ways:</span></span>

-   <span data-ttu-id="01540-108">Erstellen Sie eine Webveröffentlichungsregel für den IIS-Server, auf dem sich die ICO-und OSD-Dateien befinden – und optional die Pakete für Streaming –, die sich im internen Netzwerk befinden.</span><span class="sxs-lookup"><span data-stu-id="01540-108">Create a Web Publishing rule for the IIS server that is hosting the ICO and OSD files—and optionally, the packages for streaming—located on the internal network.</span></span> <span data-ttu-id="01540-109">Detaillierte Anweisungen finden Sie unter <https://go.microsoft.com/fwlink/?LinkId=151982> .</span><span class="sxs-lookup"><span data-stu-id="01540-109">Detailed steps are provided at <https://go.microsoft.com/fwlink/?LinkId=151982>.</span></span>

-   <span data-ttu-id="01540-110">Erstellen Sie eine Server Veröffentlichungsregel für den App-V Web Management Server (RTSPS).</span><span class="sxs-lookup"><span data-stu-id="01540-110">Create a Server Publishing rule for the App-V Web Management Server (RTSPS).</span></span> <span data-ttu-id="01540-111">Detaillierte Anweisungen finden Sie unter [https://go.microsoft.com/fwlink/?LinkId=151983&](https://go.microsoft.com/fwlink/?LinkId=151983) .</span><span class="sxs-lookup"><span data-stu-id="01540-111">Detailed steps are provided at [https://go.microsoft.com/fwlink/?LinkId=151983&](https://go.microsoft.com/fwlink/?LinkId=151983).</span></span>

<span data-ttu-id="01540-112">Wie in der folgenden Abbildung dargestellt: Wenn die Infrastruktur andere Firewalls zwischen dem Client und dem ISA-Server oder zwischen dem ISA-Server und dem internen Netzwerk implementiert hat, müssen sowohl RTSPS (TCP 322) als auch HTTPS-Firewallregeln (TCP 443) erstellt werden, um den Datenfluss zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="01540-112">As shown in the following illustration, if the infrastructure has implemented other firewalls between the client and the ISA Server or between the ISA Server and the internal network, both RTSPS (TCP 322) and HTTPS (TCP 443) firewall rules must be created to support the flow of traffic.</span></span> <span data-ttu-id="01540-113">Wenn Firewalls zwischen dem ISA-Server und dem internen Netzwerk implementiert wurden, muss der für Domänenmitglieder erforderliche Standarddaten Verkehr zum Tunneln durch die Firewall zugelassen werden (DNS, LDAP, Kerberos, SMB/CIFS).</span><span class="sxs-lookup"><span data-stu-id="01540-113">Also, if firewalls have been implemented between the ISA Server and the internal network, the default traffic required for domain members must be permitted to tunnel through the firewall (DNS, LDAP, Kerberos, SMB/CIFS).</span></span>

![App-v Umkreisnetzwerk-Firewall-Diagramm](images/appvperimeternetworkfirewall.gif)

<span data-ttu-id="01540-115">Da die Firewall-Lösungen von Umgebung zu Umgebung unterschiedlich sind, werden in diesem Thema die Anleitungen beschrieben, die erforderlich sind, um eine mit dem Internet verbundene App-V-Umgebung im Umkreisnetzwerk zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="01540-115">Because the firewall solutions vary from environment to environment, the guidance provided in this topic describes the traffic that would be required to configure an Internet-facing App-V environment in the perimeter network.</span></span> <span data-ttu-id="01540-116">Diese Informationen enthalten auch die empfohlenen internen Netzwerkserver.</span><span class="sxs-lookup"><span data-stu-id="01540-116">This information also includes the recommended internal network servers.</span></span>

<span data-ttu-id="01540-117">Platzieren Sie die folgenden Server im Umkreisnetzwerk:</span><span class="sxs-lookup"><span data-stu-id="01540-117">Place the following servers in the perimeter network:</span></span>

-   <span data-ttu-id="01540-118">App-V-Verwaltungs Server</span><span class="sxs-lookup"><span data-stu-id="01540-118">App-V Management Server</span></span>

-   <span data-ttu-id="01540-119">IIS-Server für Veröffentlichung und Streaming</span><span class="sxs-lookup"><span data-stu-id="01540-119">IIS server for publishing and streaming</span></span>

<span data-ttu-id="01540-120">**Hinweis**  Es wird empfohlen, den Verwaltungsserver und den IIS-Server auf separaten Computern zu platzieren.</span><span class="sxs-lookup"><span data-stu-id="01540-120">**Note** It is a best practice to place the Management Server and IIS server on separate computers.</span></span>

 

<span data-ttu-id="01540-121">Platzieren Sie die folgenden Server im internen Netzwerk:</span><span class="sxs-lookup"><span data-stu-id="01540-121">Place the following servers in the internal network:</span></span>

-   <span data-ttu-id="01540-122">Content Server</span><span class="sxs-lookup"><span data-stu-id="01540-122">Content server</span></span>

-   <span data-ttu-id="01540-123">Datenspeicher (SQL Server)</span><span class="sxs-lookup"><span data-stu-id="01540-123">Data store (SQL Server)</span></span>

-   <span data-ttu-id="01540-124">Active Directory-Domänen Controller</span><span class="sxs-lookup"><span data-stu-id="01540-124">Active Directory Domain Controller</span></span>

## <span data-ttu-id="01540-125">Verkehrsanforderungen</span><span class="sxs-lookup"><span data-stu-id="01540-125">Traffic Requirements</span></span>


<span data-ttu-id="01540-126">In den folgenden Tabellen sind die Datenverkehrsanforderungen für die Kommunikation aus dem Internet und dem Umkreisnetzwerk sowie vom Umkreisnetzwerk zum internen Netzwerk aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="01540-126">The following tables list the traffic requirements for communication from the Internet and the perimeter network and from the perimeter network to the internal network.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="01540-127">Datenverkehrsanforderungen vom Internet zu Umkreisnetzwerk</span><span class="sxs-lookup"><span data-stu-id="01540-127">Traffic Requirements from Internet to Perimeter Network</span></span></th>
<th align="left"><span data-ttu-id="01540-128">Details</span><span class="sxs-lookup"><span data-stu-id="01540-128">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="01540-129">RTSPS (Veröffentlichungs Aktualisierungs-und Streaming-Pakete)</span><span class="sxs-lookup"><span data-stu-id="01540-129">RTSPS (publishing refresh and streaming packages)</span></span></p></td>
<td align="left"><p><span data-ttu-id="01540-130">TCP 322 standardmäßig; Dies kann in App-V Management Server geändert werden.</span><span class="sxs-lookup"><span data-stu-id="01540-130">TCP 322 by default; this can be changed in App-V Management Server.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="01540-131">HTTPS (Veröffentlichungs-ICO-und OSD-Dateien und Streaming-Pakete)</span><span class="sxs-lookup"><span data-stu-id="01540-131">HTTPS (publishing ICO and OSD files and streaming packages)</span></span></p></td>
<td align="left"><p><span data-ttu-id="01540-132">TCP 443 standardmäßig; Dies kann in der IIS-Konfiguration geändert werden.</span><span class="sxs-lookup"><span data-stu-id="01540-132">TCP 443 by default; this can be changed in the IIS configuration.</span></span></p></td>
</tr>
</tbody>
</table>

 

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="01540-133">Datenverkehrsanforderungen vom Umkreisnetzwerk zum internen Netzwerk</span><span class="sxs-lookup"><span data-stu-id="01540-133">Traffic Requirements from Perimeter Network to Internal Network</span></span></th>
<th align="left"><span data-ttu-id="01540-134">Details</span><span class="sxs-lookup"><span data-stu-id="01540-134">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="01540-135">SQLServer</span><span class="sxs-lookup"><span data-stu-id="01540-135">SQL Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="01540-136">TCP 1433 ist der Standard, kann aber in SQL Server konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="01540-136">TCP 1433 is the default but can be configured in SQL Server.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="01540-137">SMB/CIFS</span><span class="sxs-lookup"><span data-stu-id="01540-137">SMB/CIFS</span></span></p></td>
<td align="left"><p><span data-ttu-id="01540-138">Wenn sich das Inhaltsverzeichnis Remote vom Verwaltungs Server oder IIS-Server befindet (empfohlen).</span><span class="sxs-lookup"><span data-stu-id="01540-138">If the content directory is located remotely from the Management Server(s) or IIS server (recommended).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="01540-139">Kerberos</span><span class="sxs-lookup"><span data-stu-id="01540-139">Kerberos</span></span></p></td>
<td align="left"><p><span data-ttu-id="01540-140">TCP und UDP 88</span><span class="sxs-lookup"><span data-stu-id="01540-140">TCP and UDP 88</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="01540-141">LDAP</span><span class="sxs-lookup"><span data-stu-id="01540-141">LDAP</span></span></p></td>
<td align="left"><p><span data-ttu-id="01540-142">TCP und UDP 389</span><span class="sxs-lookup"><span data-stu-id="01540-142">TCP and UDP 389</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="01540-143">DNS</span><span class="sxs-lookup"><span data-stu-id="01540-143">DNS</span></span></p></td>
<td align="left"><p><span data-ttu-id="01540-144">Für die Namensauflösung interner Ressourcen (kann mit der Verwendung der Host-Datei auf Umkreisnetzwerk Servern eliminiert werden)</span><span class="sxs-lookup"><span data-stu-id="01540-144">For name resolution of internal resources (can be eliminated with the use of host’s file on perimeter network servers)</span></span></p></td>
</tr>
</tbody>
</table>

 

 

 





