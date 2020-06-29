---
title: Planen Ihrer Streaming-Lösung in einer Anwendung Virtualisierung Server-basierten-Implementierung
description: Planen Ihrer Streaming-Lösung in einer Anwendung Virtualisierung Server-basierten-Implementierung
author: dansimp
ms.assetid: 3a57306e-5c54-4fde-8593-fe3b788f18d3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0d315f554eb99fc5c05c231630eaa41d4f505535
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806479"
---
# <span data-ttu-id="10d5b-103">Planen Ihrer Streaming-Lösung in einer Anwendung Virtualisierung Server-basierten-Implementierung</span><span class="sxs-lookup"><span data-stu-id="10d5b-103">Planning Your Streaming Solution in an Application Virtualization Server-Based Implementation</span></span>


<span data-ttu-id="10d5b-104">Wenn Sie Application Virtualization-Streamingserver in Verbindung mit ihrer auf Application Virtualization Management Server basierenden Implementierung verwenden möchten, können Sie aus verschiedenen alternativen auswählen und dabei die Infrastruktur nutzen, die bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="10d5b-104">If you want to use Application Virtualization Streaming Servers in conjunction with your Application Virtualization Management Server-based implementation, you can choose from several alternatives, taking advantage of whatever infrastructure is already in place.</span></span> <span data-ttu-id="10d5b-105">Wenn Sie beispielsweise bereits über Server in ihren Außendienst Niederlassungen verfügen, können Sie die Application Virtualization \\CONTENT-Freigabe auf diesen Servern platzieren und dann die Clients so konfigurieren, dass Sie diese Inhaltsfreigabe als Anwendungsinhalts Quelle verwenden.</span><span class="sxs-lookup"><span data-stu-id="10d5b-105">For example, if you already have servers in your field branch offices, you can place the Application Virtualization \\CONTENT share on those servers and then configure the clients to use that content share as their application content source.</span></span> <span data-ttu-id="10d5b-106">Wenn Sie sich für die Verwendung von Application Virtualization-Verwaltungsservern entscheiden, beispielsweise weil Sie nur über ein einzelnes Office verfügen, können die Clients Inhalte von diesem Server streamen.</span><span class="sxs-lookup"><span data-stu-id="10d5b-106">If you choose to use only Application Virtualization Management Servers—for example, because you have only a single office—the clients can stream content from that server.</span></span>

<span data-ttu-id="10d5b-107">Zu den unterstützten Optionen zählen die Verwendung eines Dateiservers, eines IIS-Servers oder eines Application Virtualization Streaming-Servers.</span><span class="sxs-lookup"><span data-stu-id="10d5b-107">The supported options include using a file server, an IIS server, or an Application Virtualization Streaming Server.</span></span> <span data-ttu-id="10d5b-108">Sie können den Application Virtualization Streaming Server auch auf einem vorhandenen Dateiserver oder IIS-Server installieren.</span><span class="sxs-lookup"><span data-stu-id="10d5b-108">You could also install the Application Virtualization Streaming Server on an existing file server or IIS server.</span></span> <span data-ttu-id="10d5b-109">Die Merkmale dieser verschiedenen Optionen sind in der folgenden Tabelle zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="10d5b-109">The characteristics of these different options are summarized in the following table.</span></span>

<span data-ttu-id="10d5b-110">**Hinweis**  Das Feature "Aktives Upgrade" ermöglicht das Hinzufügen einer neuen Version einer Anwendung zu einem App-V-Verwaltungsserver oder Streamingserver, ohne dass dies Auswirkungen auf die Benutzer hat, die die Anwendung zurzeit ausführen.</span><span class="sxs-lookup"><span data-stu-id="10d5b-110">**Note** The active upgrade feature enables a new version of an application to be added to an App-V Management Server or Streaming Server without affecting users currently running the application.</span></span> <span data-ttu-id="10d5b-111">Die APP-v-Clients erhalten automatisch die neueste Version der Anwendung vom APP-v-Verwaltungsserver oder Streamingserver, wenn der Benutzer die Anwendung das nächste Mal startet.</span><span class="sxs-lookup"><span data-stu-id="10d5b-111">The App-V clients will automatically receive the latest version of the application from the App-V Management Server or Streaming Server the next time the user starts the application.</span></span> <span data-ttu-id="10d5b-112">Für dieses Feature ist die Verwendung des RTSP (S)-Protokolls erforderlich.</span><span class="sxs-lookup"><span data-stu-id="10d5b-112">Use of the RTSP(S) protocol is required for this feature.</span></span>

 

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
<th align="left"><span data-ttu-id="10d5b-113">Servertyp</span><span class="sxs-lookup"><span data-stu-id="10d5b-113">Server Type</span></span></th>
<th align="left"><span data-ttu-id="10d5b-114">Protokoll</span><span class="sxs-lookup"><span data-stu-id="10d5b-114">Protocol</span></span></th>
<th align="left"><span data-ttu-id="10d5b-115">Vorteile</span><span class="sxs-lookup"><span data-stu-id="10d5b-115">Advantages</span></span></th>
<th align="left"><span data-ttu-id="10d5b-116">Nachteile</span><span class="sxs-lookup"><span data-stu-id="10d5b-116">Disadvantages</span></span></th>
<th align="left"><span data-ttu-id="10d5b-117">Links</span><span class="sxs-lookup"><span data-stu-id="10d5b-117">Links</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="10d5b-118">Dateiserver</span><span class="sxs-lookup"><span data-stu-id="10d5b-118">File server</span></span></p></td>
<td align="left"><p><span data-ttu-id="10d5b-119">SMB</span><span class="sxs-lookup"><span data-stu-id="10d5b-119">SMB</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="10d5b-120">Einfache, kostengünstige Lösung zum Konfigurieren eines vorhandenen Dateiservers mit \Content-Freigabe</span><span class="sxs-lookup"><span data-stu-id="10d5b-120">Simple low-cost solution to configure existing file server with \CONTENT share</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="10d5b-121">Kein aktives Upgrade</span><span class="sxs-lookup"><span data-stu-id="10d5b-121">No active upgrade</span></span></p></li>
</ul></td>
<td align="left"><p><a href="how-to-configure-the-file-server.md" data-raw-source="[How to Configure the File Server](how-to-configure-the-file-server.md)"><span data-ttu-id="10d5b-122">So konfigurieren Sie den Dateiserver</span><span class="sxs-lookup"><span data-stu-id="10d5b-122">How to Configure the File Server</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="10d5b-123">IIS-Server</span><span class="sxs-lookup"><span data-stu-id="10d5b-123">IIS server</span></span></p></td>
<td align="left"><p><span data-ttu-id="10d5b-124">HTTP/https</span><span class="sxs-lookup"><span data-stu-id="10d5b-124">HTTP/ HTTPS</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="10d5b-125">Unterstützt erweiterte Sicherheit mithilfe des HTTPS-Protokolls</span><span class="sxs-lookup"><span data-stu-id="10d5b-125">Supports enhanced security using HTTPS protocol</span></span></p></li>
<li><p><span data-ttu-id="10d5b-126">Unterstützt das Streaming an Remotecomputer über das Internet</span><span class="sxs-lookup"><span data-stu-id="10d5b-126">Supports streaming to remote computers across the Internet</span></span></p></li>
<li><p><span data-ttu-id="10d5b-127">Nur ein Port in der Firewall zu öffnen</span><span class="sxs-lookup"><span data-stu-id="10d5b-127">Only one port in firewall to open</span></span></p></li>
<li><p><span data-ttu-id="10d5b-128">Skalierbare</span><span class="sxs-lookup"><span data-stu-id="10d5b-128">Scalable</span></span></p></li>
<li><p><span data-ttu-id="10d5b-129">Vertrautes Protokoll</span><span class="sxs-lookup"><span data-stu-id="10d5b-129">Familiar protocol</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="10d5b-130">IIS muss verwaltet werden</span><span class="sxs-lookup"><span data-stu-id="10d5b-130">Need to manage IIS</span></span></p></li>
<li><p><span data-ttu-id="10d5b-131">Kein aktives Upgrade</span><span class="sxs-lookup"><span data-stu-id="10d5b-131">No active upgrade</span></span></p></li>
</ul></td>
<td align="left"><p><a href="how-to-configure-the-server-for-iis.md" data-raw-source="[How to Configure the Server for IIS](how-to-configure-the-server-for-iis.md)"><span data-ttu-id="10d5b-132">So konfigurieren Sie den Server für IIS</span><span class="sxs-lookup"><span data-stu-id="10d5b-132">How to Configure the Server for IIS</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="10d5b-133">Application Virtualization Streaming Server</span><span class="sxs-lookup"><span data-stu-id="10d5b-133">Application Virtualization Streaming Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="10d5b-134">RTSP/RTSPS</span><span class="sxs-lookup"><span data-stu-id="10d5b-134">RTSP/ RTSPS</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="10d5b-135">Aktives Upgrade</span><span class="sxs-lookup"><span data-stu-id="10d5b-135">Active upgrade</span></span></p></li>
<li><p><span data-ttu-id="10d5b-136">Unterstützt erweiterte Sicherheit mithilfe des RTSPS-Protokolls</span><span class="sxs-lookup"><span data-stu-id="10d5b-136">Supports enhanced security using RTSPS protocol</span></span></p></li>
<li><p><span data-ttu-id="10d5b-137">Nur ein Port in der Firewall zu öffnen</span><span class="sxs-lookup"><span data-stu-id="10d5b-137">Only one port in firewall to open</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="10d5b-138">Duale Infrastruktur</span><span class="sxs-lookup"><span data-stu-id="10d5b-138">Dual infrastructure</span></span></p></li>
<li><p><span data-ttu-id="10d5b-139">Server Verwaltungsanforderung</span><span class="sxs-lookup"><span data-stu-id="10d5b-139">Server administration requirement</span></span></p></li>
</ul></td>
<td align="left"><p><a href="how-to-configure-the-application-virtualization-streaming-servers.md" data-raw-source="[How to Configure the Application Virtualization Streaming Servers](how-to-configure-the-application-virtualization-streaming-servers.md)"><span data-ttu-id="10d5b-140">So konfigurieren Sie Application Virtualization Streaming Server</span><span class="sxs-lookup"><span data-stu-id="10d5b-140">How to Configure the Application Virtualization Streaming Servers</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="10d5b-141">Application Virtualization-Verwaltungs Server</span><span class="sxs-lookup"><span data-stu-id="10d5b-141">Application Virtualization Management Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="10d5b-142">RTSP/RTSPS</span><span class="sxs-lookup"><span data-stu-id="10d5b-142">RTSP/ RTSPS</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="10d5b-143">Aktives Upgrade</span><span class="sxs-lookup"><span data-stu-id="10d5b-143">Active upgrade</span></span></p></li>
<li><p><span data-ttu-id="10d5b-144">Unterstützt erweiterte Sicherheit mithilfe des RTSPS-Protokolls</span><span class="sxs-lookup"><span data-stu-id="10d5b-144">Supports enhanced security using RTSPS protocol</span></span></p></li>
<li><p><span data-ttu-id="10d5b-145">Nur ein Port in der Firewall zu öffnen</span><span class="sxs-lookup"><span data-stu-id="10d5b-145">Only one port in firewall to open</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="10d5b-146">Duale Infrastruktur</span><span class="sxs-lookup"><span data-stu-id="10d5b-146">Dual infrastructure</span></span></p></li>
<li><p><span data-ttu-id="10d5b-147">Server Verwaltungsanforderung</span><span class="sxs-lookup"><span data-stu-id="10d5b-147">Server administration requirement</span></span></p></li>
</ul></td>
<td align="left"><p><a href="how-to-configure-the-application-virtualization-management-servers.md" data-raw-source="[How to Configure the Application Virtualization Management Servers](how-to-configure-the-application-virtualization-management-servers.md)"><span data-ttu-id="10d5b-148">So konfigurieren Sie Anwendung Virtualisierung Management Server</span><span class="sxs-lookup"><span data-stu-id="10d5b-148">How to Configure the Application Virtualization Management Servers</span></span></a></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="10d5b-149">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="10d5b-149">Related topics</span></span>


[<span data-ttu-id="10d5b-150">Application Virtualization Server-basiertes Szenario</span><span class="sxs-lookup"><span data-stu-id="10d5b-150">Application Virtualization Server-Based Scenario</span></span>](application-virtualization-server-based-scenario.md)

[<span data-ttu-id="10d5b-151">Übersicht über die Application Virtualization-Systemkomponenten</span><span class="sxs-lookup"><span data-stu-id="10d5b-151">Overview of the Application Virtualization System Components</span></span>](overview-of-the-application-virtualization-system-components.md)

[<span data-ttu-id="10d5b-152">Veröffentlichen von virtuellen Anwendungen mit Application Virtualization Management-Servern</span><span class="sxs-lookup"><span data-stu-id="10d5b-152">Publishing Virtual Applications Using Application Virtualization Management Servers</span></span>](publishing-virtual-applications-using-application-virtualization-management-servers.md)

 

 





