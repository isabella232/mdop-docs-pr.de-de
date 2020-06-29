---
title: Planen einer Streaminglösung in einer ESD-Implementierung (Electronic Software Distribution)
description: Planen einer Streaminglösung in einer ESD-Implementierung (Electronic Software Distribution)
author: dansimp
ms.assetid: bc18772a-f169-486f-adb1-7af1a31845aa
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c49d6fc0b5f8f5dee347ead3bb899ce9b0387024
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806475"
---
# <span data-ttu-id="22705-103">Planen einer Streaminglösung in einer ESD-Implementierung (Electronic Software Distribution)</span><span class="sxs-lookup"><span data-stu-id="22705-103">Planning Your Streaming Solution in an Electronic Software Distribution Implementation</span></span>


<span data-ttu-id="22705-104">Wenn Sie sich entschließen, Streamingserver in Verbindung mit Ihrem ESD-System zu verwenden, um Anwendungsinhalte auf Ihren Endbenutzercomputern zur Verfügung zu stellen, können Sie aus verschiedenen alternativen auswählen und dabei die Infrastruktur nutzen, die bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="22705-104">If you decide to use streaming servers in conjunction with your ESD system to make application content available to your end user computers, you can choose from several alternatives, taking advantage of whatever infrastructure is already in place.</span></span> <span data-ttu-id="22705-105">Wenn Ihr ESD-System beispielsweise über Softwareverteilungsfreigaben auf Servern in ihren Außendienst Niederlassungen verfügt, können Sie die Application Virtualization \\CONTENT-Freigabe auf diesen Servern platzieren und dann die Clients so konfigurieren, dass Sie diese Inhaltsfreigabe als Anwendungsinhalts Quelle verwenden.</span><span class="sxs-lookup"><span data-stu-id="22705-105">For example, if your ESD system has software distribution shares on servers in your field branch offices, you can place the Application Virtualization \\CONTENT share on those servers and then configure the clients to use that content share as their application content source.</span></span> <span data-ttu-id="22705-106">Zu den unterstützten Optionen gehört die Verwendung eines Dateiservers oder eines IIS-Servers.</span><span class="sxs-lookup"><span data-stu-id="22705-106">The supported options include using a file server or an IIS server.</span></span> <span data-ttu-id="22705-107">Sie können den Application Virtualization Streaming Server auch auf einem vorhandenen Dateiserver oder IIS-Server installieren.</span><span class="sxs-lookup"><span data-stu-id="22705-107">You could also install the Application Virtualization Streaming Server on an existing file server or IIS server.</span></span>

<span data-ttu-id="22705-108">Der Application Virtualization Streaming Server bietet Unterstützung für das aktive Upgrade-Feature in Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="22705-108">The Application Virtualization Streaming Server provides support for the active upgrade feature in Application Virtualization.</span></span> <span data-ttu-id="22705-109">Das Feature "Aktives Upgrade" ermöglicht das Hinzufügen einer neuen Version einer Anwendung zu einem App-V-Verwaltungsserver oder Streamingserver, ohne dass dies Auswirkungen auf die Benutzer hat, die die Anwendung zurzeit ausführen.</span><span class="sxs-lookup"><span data-stu-id="22705-109">The active upgrade feature enables a new version of an application to be added to an App-V Management Server or Streaming Server without affecting users currently running the application.</span></span> <span data-ttu-id="22705-110">Die APP-v-Clients erhalten automatisch die neueste Version der Anwendung vom APP-v-Verwaltungsserver oder Streamingserver, wenn der Benutzer die Anwendung das nächste Mal startet.</span><span class="sxs-lookup"><span data-stu-id="22705-110">The App-V clients will automatically receive the latest version of the application from the App-V Management Server or Streaming Server the next time the user starts the application.</span></span> <span data-ttu-id="22705-111">Für dieses Feature ist die Verwendung des RTSP (S)-Protokolls erforderlich.</span><span class="sxs-lookup"><span data-stu-id="22705-111">Use of the RTSP(S) protocol is required for this feature.</span></span> <span data-ttu-id="22705-112">Wenn Sie den Application Virtualization Streaming Server nicht verwenden möchten, müssen Sie Anwendungspaket-Upgrades explizit mithilfe des ESD-Systems verwalten.</span><span class="sxs-lookup"><span data-stu-id="22705-112">If you choose not to use the Application Virtualization Streaming Server, you will need to explicitly manage application package upgrades by using the ESD system.</span></span>

<span data-ttu-id="22705-113">**Hinweis**  Der Zugriff auf die Anwendungen wird mithilfe von Sicherheitsgruppen in den Active Directory-Domänendiensten gesteuert, daher müssen Sie einen Prozess für das Einrichten einer Sicherheitsgruppe für jede virtuelle Anwendung und für die Verwaltung der Benutzer planen, die jeder Gruppe hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="22705-113">**Note** Access to the applications is controlled by means of Security Groups in Active Directory Domain Services, so you will need to plan a process for setting up a security group for each virtual application and for managing which users are added to each group.</span></span> <span data-ttu-id="22705-114">Der Application Virtualization System-Administrator konfiguriert jeden Streamingserver so, dass diese Active Directory-Gruppen verwendet werden, indem ACLs auf die Anwendungsverzeichnisse unter der Inhaltsfreigabe angewendet werden, die den Zugriff auf die Pakete auf Grundlage der Active Directory-Gruppenmitgliedschaft steuert.</span><span class="sxs-lookup"><span data-stu-id="22705-114">The Application Virtualization system administrator configures each streaming server to use these Active Directory groups by applying ACLs to the application directories under the CONTENT share, which controls access to the packages based on Active Directory group membership.</span></span>

 

<span data-ttu-id="22705-115">Die Merkmale der verfügbaren Streaming-Optionen sind in der folgenden Tabelle zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="22705-115">The characteristics of the available streaming options are summarized in the following table.</span></span>

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
<th align="left"><span data-ttu-id="22705-116">Servertyp</span><span class="sxs-lookup"><span data-stu-id="22705-116">Server Type</span></span></th>
<th align="left"><span data-ttu-id="22705-117">Protokoll</span><span class="sxs-lookup"><span data-stu-id="22705-117">Protocol</span></span></th>
<th align="left"><span data-ttu-id="22705-118">Vorteile</span><span class="sxs-lookup"><span data-stu-id="22705-118">Advantages</span></span></th>
<th align="left"><span data-ttu-id="22705-119">Nachteile</span><span class="sxs-lookup"><span data-stu-id="22705-119">Disadvantages</span></span></th>
<th align="left"><span data-ttu-id="22705-120">Links</span><span class="sxs-lookup"><span data-stu-id="22705-120">Links</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="22705-121">Dateiserver</span><span class="sxs-lookup"><span data-stu-id="22705-121">File server</span></span></p></td>
<td align="left"><p><span data-ttu-id="22705-122">SMB</span><span class="sxs-lookup"><span data-stu-id="22705-122">SMB</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="22705-123">Einfache, kostengünstige Lösung zum Konfigurieren eines vorhandenen Dateiservers mit \Content-Freigabe</span><span class="sxs-lookup"><span data-stu-id="22705-123">Simple low-cost solution to configure existing file server with \CONTENT share</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="22705-124">Kein aktives Upgrade</span><span class="sxs-lookup"><span data-stu-id="22705-124">No active upgrade</span></span></p></li>
</ul></td>
<td align="left"><p><a href="how-to-configure-the-file-server.md" data-raw-source="[How to Configure the File Server](how-to-configure-the-file-server.md)"><span data-ttu-id="22705-125">So konfigurieren Sie den Dateiserver</span><span class="sxs-lookup"><span data-stu-id="22705-125">How to Configure the File Server</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="22705-126">IIS-Server</span><span class="sxs-lookup"><span data-stu-id="22705-126">IIS server</span></span></p></td>
<td align="left"><p><span data-ttu-id="22705-127">HTTP/https</span><span class="sxs-lookup"><span data-stu-id="22705-127">HTTP/ HTTPS</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="22705-128">Unterstützt erweiterte Sicherheit mithilfe des HTTPS-Protokolls</span><span class="sxs-lookup"><span data-stu-id="22705-128">Supports enhanced security using HTTPS protocol</span></span></p></li>
<li><p><span data-ttu-id="22705-129">Unterstützt das Streaming an Remotecomputer über das Internet</span><span class="sxs-lookup"><span data-stu-id="22705-129">Supports streaming to remote computers across the Internet</span></span></p></li>
<li><p><span data-ttu-id="22705-130">Nur ein Port in der Firewall zu öffnen</span><span class="sxs-lookup"><span data-stu-id="22705-130">Only one port in firewall to open</span></span></p></li>
<li><p><span data-ttu-id="22705-131">Skalierbare</span><span class="sxs-lookup"><span data-stu-id="22705-131">Scalable</span></span></p></li>
<li><p><span data-ttu-id="22705-132">Vertrautes Protokoll</span><span class="sxs-lookup"><span data-stu-id="22705-132">Familiar protocol</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="22705-133">IIS muss verwaltet werden</span><span class="sxs-lookup"><span data-stu-id="22705-133">Need to manage IIS</span></span></p></li>
<li><p><span data-ttu-id="22705-134">Kein aktives Upgrade</span><span class="sxs-lookup"><span data-stu-id="22705-134">No active upgrade</span></span></p></li>
</ul></td>
<td align="left"><p><a href="how-to-configure-the-server-for-iis.md" data-raw-source="[How to Configure the Server for IIS](how-to-configure-the-server-for-iis.md)"><span data-ttu-id="22705-135">So konfigurieren Sie den Server für IIS</span><span class="sxs-lookup"><span data-stu-id="22705-135">How to Configure the Server for IIS</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="22705-136">Application Virtualization Streaming Server</span><span class="sxs-lookup"><span data-stu-id="22705-136">Application Virtualization Streaming Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="22705-137">RTSP/RTSPS</span><span class="sxs-lookup"><span data-stu-id="22705-137">RTSP/ RTSPS</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="22705-138">Aktives Upgrade</span><span class="sxs-lookup"><span data-stu-id="22705-138">Active upgrade</span></span></p></li>
<li><p><span data-ttu-id="22705-139">Unterstützt erweiterte Sicherheit mithilfe des RTSPS-Protokolls</span><span class="sxs-lookup"><span data-stu-id="22705-139">Supports enhanced security using RTSPS protocol</span></span></p></li>
<li><p><span data-ttu-id="22705-140">Nur ein Port in der Firewall zu öffnen</span><span class="sxs-lookup"><span data-stu-id="22705-140">Only one port in firewall to open</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="22705-141">Duale Infrastruktur</span><span class="sxs-lookup"><span data-stu-id="22705-141">Dual infrastructure</span></span></p></li>
<li><p><span data-ttu-id="22705-142">Server Verwaltungsanforderung</span><span class="sxs-lookup"><span data-stu-id="22705-142">Server administration requirement</span></span></p></li>
</ul></td>
<td align="left"><p><a href="how-to-configure-the-application-virtualization-management-servers.md" data-raw-source="[How to Configure the Application Virtualization Management Servers](how-to-configure-the-application-virtualization-management-servers.md)"><span data-ttu-id="22705-143">So konfigurieren Sie Anwendung Virtualisierung Management Server</span><span class="sxs-lookup"><span data-stu-id="22705-143">How to Configure the Application Virtualization Management Servers</span></span></a></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="22705-144">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="22705-144">Related topics</span></span>


[<span data-ttu-id="22705-145">So konfigurieren Sie Servern für die ESD-basierte Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="22705-145">How to Configure Servers for ESD-Based Deployment</span></span>](how-to-configure-servers-for-esd-based-deployment.md)

[<span data-ttu-id="22705-146">Übersicht über Sicherheit und Schutz</span><span class="sxs-lookup"><span data-stu-id="22705-146">Security and Protection Overview</span></span>](security-and-protection-overview.md)

[<span data-ttu-id="22705-147">Veröffentlichen von virtuellen Anwendungen mit Electronic Software Distribution</span><span class="sxs-lookup"><span data-stu-id="22705-147">Publishing Virtual Applications Using Electronic Software Distribution</span></span>](publishing-virtual-applications-using-electronic-software-distribution.md)

 

 





