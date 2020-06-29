---
title: Planen der Bereitstellung des App-V 5.1-Servers
description: Planen der Bereitstellung des App-V 5.1-Servers
author: dansimp
ms.assetid: eedd97c9-bee0-4749-9d1e-ab9528fba398
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 31e3a116eb511356b061e6ccb18c7e25c060a66e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804976"
---
# <span data-ttu-id="1b5bc-103">Planen der Bereitstellung des App-V 5.1-Servers</span><span class="sxs-lookup"><span data-stu-id="1b5bc-103">Planning for the App-V 5.1 Server Deployment</span></span>


<span data-ttu-id="1b5bc-104">Die Microsoft Application Virtualization (App-V) 5,1 Server-Infrastruktur besteht aus einer Reihe spezieller Features, die basierend auf den Anforderungen des Unternehmens auf einem oder mehreren Server Computern installiert werden können.</span><span class="sxs-lookup"><span data-stu-id="1b5bc-104">The Microsoft Application Virtualization (App-V) 5.1 server infrastructure consists of a set of specialized features that can be installed on one or more server computers, based on the requirements of the enterprise.</span></span>

## <span data-ttu-id="1b5bc-105">Planen der App-V 5,1-Server Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="1b5bc-105">Planning for App-V 5.1 Server Deployment</span></span>


<span data-ttu-id="1b5bc-106">Der App-V 5,1-Server besteht aus den folgenden Features:</span><span class="sxs-lookup"><span data-stu-id="1b5bc-106">The App-V 5.1 server consists of the following features:</span></span>

-   <span data-ttu-id="1b5bc-107">Verwaltungs Server – bietet allgemeine Verwaltungsfunktionen für die App-V 5,1-Infrastruktur.</span><span class="sxs-lookup"><span data-stu-id="1b5bc-107">Management Server – provides overall management functionality for the App-V 5.1 infrastructure.</span></span>

-   <span data-ttu-id="1b5bc-108">Verwaltungsdatenbank – ermöglicht die Bereitstellung von Datenbankbereitstellungen für die App-V 5,1-Verwaltung.</span><span class="sxs-lookup"><span data-stu-id="1b5bc-108">Management Database – facilitates database predeployments for App-V 5.1 management.</span></span>

-   <span data-ttu-id="1b5bc-109">Publishing Server – bietet Hosting-und Streamingfunktionen für virtuelle Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="1b5bc-109">Publishing Server – provides hosting and streaming functionality for virtual applications.</span></span>

-   <span data-ttu-id="1b5bc-110">Reporting Server – bietet App-V 5,1 Reporting Services.</span><span class="sxs-lookup"><span data-stu-id="1b5bc-110">Reporting Server – provides App-V 5.1 reporting services.</span></span>

-   <span data-ttu-id="1b5bc-111">Berichtsdatenbank – ermöglicht die Bereitstellung von Datenbanken für App-V 5,1-Berichterstellung.</span><span class="sxs-lookup"><span data-stu-id="1b5bc-111">Reporting Database – facilitates database predeployments for App-V 5.1 reporting.</span></span>

<span data-ttu-id="1b5bc-112">In der folgenden Liste werden die empfohlenen Methoden zum Installieren der App-V 5,1-Serverinfrastruktur angezeigt:</span><span class="sxs-lookup"><span data-stu-id="1b5bc-112">The following list displays the recommended methods for installing the App-V 5.1 server infrastructure:</span></span>

-   <span data-ttu-id="1b5bc-113">Installieren Sie den App-V 5,1-Server.</span><span class="sxs-lookup"><span data-stu-id="1b5bc-113">Install the App-V 5.1 server.</span></span> <span data-ttu-id="1b5bc-114">Weitere Informationen finden Sie unter [Bereitstellen des App-V 5,1-Servers](how-to-deploy-the-app-v-51-server.md).</span><span class="sxs-lookup"><span data-stu-id="1b5bc-114">For more information, see [How to Deploy the App-V 5.1 Server](how-to-deploy-the-app-v-51-server.md).</span></span>

-   <span data-ttu-id="1b5bc-115">Installieren Sie die Datenbank-, Berichterstattungs-und Verwaltungsfeatures auf separaten Computern.</span><span class="sxs-lookup"><span data-stu-id="1b5bc-115">Install the database, reporting, and management features on separate computers.</span></span> <span data-ttu-id="1b5bc-116">Weitere Informationen finden Sie unter [so wird es gemacht: Installieren der Verwaltungs-und Berichtsdatenbanken auf separaten Computern über die Verwaltungs-und Reporting Services](how-to-install-the-management-and-reporting-databases-on-separate-computers-from-the-management-and-reporting-services51.md).</span><span class="sxs-lookup"><span data-stu-id="1b5bc-116">For more information, see [How to Install the Management and Reporting Databases on Separate Computers from the Management and Reporting Services](how-to-install-the-management-and-reporting-databases-on-separate-computers-from-the-management-and-reporting-services51.md).</span></span>

-   <span data-ttu-id="1b5bc-117">Verwenden Sie Electronic Software Distribution (ESD).</span><span class="sxs-lookup"><span data-stu-id="1b5bc-117">Use Electronic Software Distribution (ESD).</span></span> <span data-ttu-id="1b5bc-118">Weitere Informationen finden Sie unter [Bereitstellen von App-V 5,1-Paketen mithilfe der elektronischen Software Verteilung](how-to-deploy-app-v-51-packages-using-electronic-software-distribution.md).</span><span class="sxs-lookup"><span data-stu-id="1b5bc-118">For more information, see [How to deploy App-V 5.1 Packages Using Electronic Software Distribution](how-to-deploy-app-v-51-packages-using-electronic-software-distribution.md).</span></span>

-   <span data-ttu-id="1b5bc-119">Installieren Sie alle Server Features auf einem einzelnen Computer.</span><span class="sxs-lookup"><span data-stu-id="1b5bc-119">Install all server features on a single computer.</span></span>

## <a href="" id="---------app-v-5-1-server-interaction"></a> <span data-ttu-id="1b5bc-120">App-V 5,1-Server Interaktion</span><span class="sxs-lookup"><span data-stu-id="1b5bc-120">App-V 5.1 Server Interaction</span></span>


<span data-ttu-id="1b5bc-121">Dieser Abschnitt enthält Informationen dazu, wie die verschiedenen App-V 5,1-Serverrollen miteinander interagieren.</span><span class="sxs-lookup"><span data-stu-id="1b5bc-121">This section contains information about how the various App-V 5.1 server roles interact with each other.</span></span>

<span data-ttu-id="1b5bc-122">Der App-V 5,1-Verwaltungs Server enthält das Repository der Pakete und deren zugewiesene Konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="1b5bc-122">The App-V 5.1 Management Server contains the repository of packages and their assigned configurations.</span></span> <span data-ttu-id="1b5bc-123">Bei Veröffentlichungsservern, die beim Verwaltungs Server registriert sind, werden die zugehörigen Metadaten den Veröffentlichungsservern zur Verwendung bereitgestellt, wenn Veröffentlichungs Aktualisierungsanforderungen von Computern mit dem App-V 5,1-Client empfangen werden.</span><span class="sxs-lookup"><span data-stu-id="1b5bc-123">For Publishing Servers that are registered with the Management Server, the associated metadata is provided to the Publishing servers for use when publishing refresh requests are received from computers running the App-V 5.1 Client.</span></span> <span data-ttu-id="1b5bc-124">App-V 5,1-Publishing Server, die von einem einzelnen Verwaltungsserver verwaltet werden, können verschiedene Clients bedienen und unterschiedliche Websitenamen und Portbindungen aufweisen.</span><span class="sxs-lookup"><span data-stu-id="1b5bc-124">App-V 5.1 publishing servers managed by a single management server can be serving different clients and can have different website names and port bindings.</span></span> <span data-ttu-id="1b5bc-125">Darüber hinaus sind alle Veröffentlichungsserver, die vom gleichen Verwaltungs Server verwaltet werden, Replikate voneinander.</span><span class="sxs-lookup"><span data-stu-id="1b5bc-125">Additionally, all Publishing Servers managed by the same Management Server are replicas of each other.</span></span>

<span data-ttu-id="1b5bc-126">**Hinweis**  Der Verwaltungs Server führt keinen Lastenausgleich aus.</span><span class="sxs-lookup"><span data-stu-id="1b5bc-126">**Note** The Management Server does not perform any load balancing.</span></span> <span data-ttu-id="1b5bc-127">Die zugehörigen Metadaten werden einfach an den Veröffentlichungsserver übergeben, um Sie für die Verarbeitung von Clientanforderungen zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="1b5bc-127">The associated metadata is simply passed to the publishing server for use when processing client requests.</span></span>

 

## <span data-ttu-id="1b5bc-128">Server bezogene Protokolle und externe Features</span><span class="sxs-lookup"><span data-stu-id="1b5bc-128">Server-Related Protocols and External Features</span></span>


<span data-ttu-id="1b5bc-129">Im folgenden werden Informationen zu serverbezogenen Protokollen angezeigt, die von den App-V 5,1-Servern verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1b5bc-129">The following displays information about server-related protocols used by the App-V 5.1 servers.</span></span> <span data-ttu-id="1b5bc-130">Die Tabelle enthält auch den Berichterstellungsmechanismus für die einzelnen Servertypen.</span><span class="sxs-lookup"><span data-stu-id="1b5bc-130">The table also includes the reporting mechanism for each server type.</span></span>

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
<th align="left"><span data-ttu-id="1b5bc-131">Servertyp</span><span class="sxs-lookup"><span data-stu-id="1b5bc-131">Server Type</span></span></th>
<th align="left"><span data-ttu-id="1b5bc-132">Protokolle</span><span class="sxs-lookup"><span data-stu-id="1b5bc-132">Protocols</span></span></th>
<th align="left"><span data-ttu-id="1b5bc-133">Erforderliche externe Features</span><span class="sxs-lookup"><span data-stu-id="1b5bc-133">External Features Needed</span></span></th>
<th align="left"><span data-ttu-id="1b5bc-134">Berichterstellung</span><span class="sxs-lookup"><span data-stu-id="1b5bc-134">Reporting</span></span></th>
<th align="left"></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1b5bc-135">IIS-Server</span><span class="sxs-lookup"><span data-stu-id="1b5bc-135">IIS server</span></span></p></td>
<td align="left"><p><span data-ttu-id="1b5bc-136">HTTP</span><span class="sxs-lookup"><span data-stu-id="1b5bc-136">HTTP</span></span></p>
<p><span data-ttu-id="1b5bc-137">HTTPS</span><span class="sxs-lookup"><span data-stu-id="1b5bc-137">HTTPS</span></span></p></td>
<td align="left"><p><span data-ttu-id="1b5bc-138">Diese Server-Protokoll-Kombination erfordert einen Mechanismus zum Synchronisieren des Inhalts zwischen dem Management-Server und dem Streaming-Server.</span><span class="sxs-lookup"><span data-stu-id="1b5bc-138">This server-protocol combination requires a mechanism to synchronize the content between the Management Server and the Streaming Server.</span></span> <span data-ttu-id="1b5bc-139">Verwenden Sie bei Verwendung von http oder HTTPS einen IIS-Server und eine Firewall, um den Server vor der Gefährdung durch das Internet zu schützen.</span><span class="sxs-lookup"><span data-stu-id="1b5bc-139">When using HTTP or HTTPS, use an IIS server and a firewall to protect the server from exposure to the Internet.</span></span></p></td>
<td align="left"><p><span data-ttu-id="1b5bc-140">Intern</span><span class="sxs-lookup"><span data-stu-id="1b5bc-140">Internal</span></span></p></td>
<td align="left"></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1b5bc-141">Datei</span><span class="sxs-lookup"><span data-stu-id="1b5bc-141">File</span></span></p></td>
<td align="left"><p><span data-ttu-id="1b5bc-142">SMB</span><span class="sxs-lookup"><span data-stu-id="1b5bc-142">SMB</span></span></p></td>
<td align="left"><p><span data-ttu-id="1b5bc-143">Diese Server-Protokoll-Kombination erfordert Unterstützung, um den Inhalt zwischen dem Verwaltungsserver und dem Streamingserver zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="1b5bc-143">This server-protocol combination requires support to synchronize the content between the Management Server and the Streaming Server.</span></span> <span data-ttu-id="1b5bc-144">Verwenden Sie einen Clientcomputer mit Dateifreigabe-oder Streaming-Funktion.</span><span class="sxs-lookup"><span data-stu-id="1b5bc-144">Use a client computer with file sharing or streaming capability.</span></span></p></td>
<td align="left"><p><span data-ttu-id="1b5bc-145">Intern</span><span class="sxs-lookup"><span data-stu-id="1b5bc-145">Internal</span></span></p></td>
<td align="left"></td>
</tr>
</tbody>
</table>

 






## <span data-ttu-id="1b5bc-146">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="1b5bc-146">Related topics</span></span>


[<span data-ttu-id="1b5bc-147">Planen der Bereitstellung von App-V</span><span class="sxs-lookup"><span data-stu-id="1b5bc-147">Planning to Deploy App-V</span></span>](planning-to-deploy-app-v51.md)

[<span data-ttu-id="1b5bc-148">Bereitstellen des App-V 5.1-Servers</span><span class="sxs-lookup"><span data-stu-id="1b5bc-148">Deploying the App-V 5.1 Server</span></span>](deploying-the-app-v-51-server.md)

 

 





