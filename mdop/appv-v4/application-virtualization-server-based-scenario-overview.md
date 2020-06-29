---
title: Übersicht über Application Virtualization Server-basierte Szenarien
description: Übersicht über Application Virtualization Server-basierte Szenarien
author: dansimp
ms.assetid: 2d91392b-5085-4a5d-94f2-15eed1ed2928
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7b3ac3f10a5b7c7705e6d72c122d52be801a6d50
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809148"
---
# <span data-ttu-id="006c0-103">Übersicht über Application Virtualization Server-basierte Szenarien</span><span class="sxs-lookup"><span data-stu-id="006c0-103">Application Virtualization Server-Based Scenario Overview</span></span>


<span data-ttu-id="006c0-104">Wenn Sie ein serverbasiertes Bereitstellungsszenario für Ihre Microsoft Application Virtualization-Umgebung verwenden möchten, ist es wichtig, die Unterschiede zwischen *Application Virtualization Management Server* und *Application Virtualization Streaming Server*zu verstehen.</span><span class="sxs-lookup"><span data-stu-id="006c0-104">If you plan to use a server-based deployment scenario for your Microsoft Application Virtualization environment, it is important to understand the differences between the *Application Virtualization Management Server* and the *Application Virtualization Streaming Server*.</span></span> <span data-ttu-id="006c0-105">In diesem Thema werden diese Unterschiede beschrieben und außerdem Informationen zu Paketübermittlungsmethoden, Übertragungsprotokollen und externen Komponenten bereitgestellt, die Sie beim Fortsetzen der Bereitstellung in Frage stellen müssen.</span><span class="sxs-lookup"><span data-stu-id="006c0-105">This topic describes those differences and also provides information about package delivery methods, transmission protocols, and external components that you will need to consider as you proceed with your deployment.</span></span>

## <span data-ttu-id="006c0-106">Application Virtualization-Verwaltungs Server</span><span class="sxs-lookup"><span data-stu-id="006c0-106">Application Virtualization Management Server</span></span>


<span data-ttu-id="006c0-107">Der Application Virtualization Management-Server führt sowohl die Veröffentlichungsfunktion als auch die Streamingfunktion aus.</span><span class="sxs-lookup"><span data-stu-id="006c0-107">The Application Virtualization Management Server performs both the publishing function and the streaming function.</span></span> <span data-ttu-id="006c0-108">Der Server veröffentlicht Anwendungssymbole, Verknüpfungen und Dateitypzuordnungen für die App-V-Clients für autorisierte Benutzer.</span><span class="sxs-lookup"><span data-stu-id="006c0-108">The server publishes application icons, shortcuts, and file type associations to the App-V clients for authorized users.</span></span> <span data-ttu-id="006c0-109">Wenn Benutzeranforderungen für Anwendungen empfangen werden, strömt der Server diese Daten bei Bedarf an autorisierte Benutzer mithilfe von RTSP-oder RTSPS-Protokollen aus.</span><span class="sxs-lookup"><span data-stu-id="006c0-109">When user requests for applications are received the server streams that data on-demand to authorized users using RTSP or RTSPS protocols.</span></span> <span data-ttu-id="006c0-110">In den meisten Konfigurationen, die diesen Server verwenden, geben mindestens ein Verwaltungsserver einen gemeinsamen Datenspeicher für Konfigurations-und Paketinformationen frei.</span><span class="sxs-lookup"><span data-stu-id="006c0-110">In most configurations using this server, one or more Management Servers share a common data store for configuration and package information.</span></span>

<span data-ttu-id="006c0-111">Die Application Virtualization Management-Server verwenden Active Directory-Gruppen, um die Benutzerautorisierung zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="006c0-111">The Application Virtualization Management Servers use Active Directory groups to manage user authorization.</span></span> <span data-ttu-id="006c0-112">Neben den Active Directory-Domänendiensten sind auf diesen Servern SQL Server installiert, um die Datenbank und den Datenspeicher zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="006c0-112">In addition to Active Directory Domain Services, these servers have SQL Server installed to manage the database and data store.</span></span> <span data-ttu-id="006c0-113">Der Verwaltungs Server wird über die Application Virtualization Management Console, ein Snap-in für die Microsoft Management Console, gesteuert.</span><span class="sxs-lookup"><span data-stu-id="006c0-113">The Management Server is controlled through the Application Virtualization Management Console, a snap-in to the Microsoft Management Console.</span></span>

<span data-ttu-id="006c0-114">Da die Application Virtualization-Verwaltungsserver Anwendungen bei Bedarf an Endbenutzer streamen, eignen sich diese Server ideal für Systemkonfigurationen mit zuverlässigen LANs mit hoher Bandbreite.</span><span class="sxs-lookup"><span data-stu-id="006c0-114">Because the Application Virtualization Management Servers stream applications to end-users on demand, these servers are ideally suited for system configurations that have reliable, high-bandwidth LANs.</span></span>

## <span data-ttu-id="006c0-115">Application Virtualization Streaming Server</span><span class="sxs-lookup"><span data-stu-id="006c0-115">Application Virtualization Streaming Server</span></span>


<span data-ttu-id="006c0-116">Der Application Virtualization Streaming Server bietet die gleichen Streaming-und Paket Aktualisierungsfunktionen, die vom Verwaltungs Server bereitgestellt werden, jedoch ohne die Active Directory-oder SQL Server-Anforderungen.</span><span class="sxs-lookup"><span data-stu-id="006c0-116">The Application Virtualization Streaming Server delivers the same streaming and package upgrade capabilities provided by the Management Server, but without its Active Directory or SQL Server requirements.</span></span> <span data-ttu-id="006c0-117">Der Streamingserver verfügt jedoch weder über einen Veröffentlichungsdienst noch über Lizenzierungs-oder Dosier Funktionen.</span><span class="sxs-lookup"><span data-stu-id="006c0-117">However, the Streaming Server does not have a publishing service, nor does it have licensing or metering capabilities.</span></span> <span data-ttu-id="006c0-118">Der Veröffentlichungsdienst eines separaten App-v-Verwaltungsservers wird in Verbindung mit dem App-v-Streamingserver verwendet.</span><span class="sxs-lookup"><span data-stu-id="006c0-118">The publishing service of a separate App-V Management Server is used in conjunction with the App-V Streaming Server.</span></span> <span data-ttu-id="006c0-119">Der APP-v-Streamingserver richtet sich an die Anforderungen von Unternehmen, die Application Virtualization an mehreren Speicherorten mit den Streamingfunktionen der klassischen Server Konfiguration verwenden möchten, aber möglicherweise nicht über die Infrastruktur zur Unterstützung von App-V-Verwaltungsservern an jedem Standort verfügen.</span><span class="sxs-lookup"><span data-stu-id="006c0-119">The App-V Streaming Server addresses the needs of businesses that want to use Application Virtualization in multiple locations with the streaming capabilities of the classic server configuration but might not have the infrastructure to support App-V Management Servers in every location.</span></span>

<span data-ttu-id="006c0-120">Der Application Virtualization Streaming Server kann auch in Umgebungen mit einem vorhandenen elektronischen Softwareverteilungssystem (ESD) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="006c0-120">The Application Virtualization Streaming Server can also be used in environments with an existing electronic software distribution system (ESD).</span></span> <span data-ttu-id="006c0-121">Sie verwenden das ESD-Programm zum Verwalten von Streaming-Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="006c0-121">You use the ESD to manage streaming applications.</span></span> <span data-ttu-id="006c0-122">Im Gegensatz zum Application Virtualization Management-Server verwendet der Streamingserver keine SQL-oder Verwaltungskonsole.</span><span class="sxs-lookup"><span data-stu-id="006c0-122">Unlike the Application Virtualization Management Server, the Streaming Server does not use SQL or a management console.</span></span> <span data-ttu-id="006c0-123">Diese Server verwenden Zugriffssteuerungslisten (ACLs), um die Benutzerautorisierung zu erteilen.</span><span class="sxs-lookup"><span data-stu-id="006c0-123">These servers use access control lists (ACLs) to grant user authorization.</span></span>

## <span data-ttu-id="006c0-124">Paketübermittlungsmethoden</span><span class="sxs-lookup"><span data-stu-id="006c0-124">Package Delivery Methods</span></span>


<span data-ttu-id="006c0-125">Wenn Sie beabsichtigen, einen Application Virtualization Server als Veröffentlichungs Bereitstellungsmethode zu verwenden, müssen Sie ermitteln, welche der folgenden Paketübermittlungsmethoden Ihr Szenario verwendet:</span><span class="sxs-lookup"><span data-stu-id="006c0-125">If you plan to use an Application Virtualization Server as the publishing delivery method, you need to determine which of the following package delivery methods your scenario employs:</span></span>

-   *<span data-ttu-id="006c0-126">Dynamische Paketzustellung</span><span class="sxs-lookup"><span data-stu-id="006c0-126">Dynamic package delivery</span></span>*

-   *<span data-ttu-id="006c0-127">Laden aus Dateipaket Zustellung</span><span class="sxs-lookup"><span data-stu-id="006c0-127">Load from file package delivery</span></span>*

### <span data-ttu-id="006c0-128">Dynamische Paketzustellung</span><span class="sxs-lookup"><span data-stu-id="006c0-128">Dynamic Package Delivery</span></span>

<span data-ttu-id="006c0-129">Während der dynamischen Paketzustellung übermittelt der Server (Application Virtualization Management Server, Application Virtualization Streaming Server oder IIS-Server) die virtualisierten Anwendungen über die bedarfsgesteuerte Bereitstellung an die Endbenutzer.</span><span class="sxs-lookup"><span data-stu-id="006c0-129">During dynamic package delivery, the server (Application Virtualization Management Server, Application Virtualization Streaming Server, or IIS server) delivers the virtualized applications to the end users through on-demand deployment.</span></span> <span data-ttu-id="006c0-130">Der Server übermittelt die virtualisierten Anwendungen und Pakete nur dann an einen Clientcomputer, wenn ein Benutzer zuerst versucht, eine Anwendung (bei Bedarf) zu starten.</span><span class="sxs-lookup"><span data-stu-id="006c0-130">The server delivers the virtualized applications and packages to a client computer only when a user first attempts to launch an application (on demand).</span></span> <span data-ttu-id="006c0-131">Der Server streamt nur die Blöcke, die zum Starten der Anwendung erforderlich sind (primärer Feature-Block).</span><span class="sxs-lookup"><span data-stu-id="006c0-131">The server streams only the blocks needed to start the application (primary feature block).</span></span> <span data-ttu-id="006c0-132">Nachdem der primäre Feature-Block an den Client übermittelt wurde, wird die Anwendung ausgeführt; der Client erhält nicht die vollständige Anwendung (inkrementelle Bereitstellung), es sei denn, der Client benötigt Zugriff auf einen Teil der Anwendung, der nicht im primären Feature-Block enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="006c0-132">After the primary feature block is delivered to the client, the application runs; the client does not receive the complete application (incremental deployment) unless the client needs access to a part of the application that is not included in the primary feature block.</span></span> <span data-ttu-id="006c0-133">In diesem Fall führt der Client eine Out-of-Sequence-Anforderung aus, und der sekundäre Feature-Block wird an den Client gestreamt.</span><span class="sxs-lookup"><span data-stu-id="006c0-133">When this occurs, the client performs an out-of-sequence request and the secondary feature block is streamed to the client.</span></span> <span data-ttu-id="006c0-134">Die dynamische Paketzustellung ermöglicht den schnellen Anwendungsstart.</span><span class="sxs-lookup"><span data-stu-id="006c0-134">Dynamic package delivery allows for rapid application launch.</span></span>

### <span data-ttu-id="006c0-135">Laden aus Dateipaket Zustellung</span><span class="sxs-lookup"><span data-stu-id="006c0-135">Load from File Package Delivery</span></span>

<span data-ttu-id="006c0-136">Für das Laden aus der Dateipaket Zustellung übergibt der Server das gesamte virtualisierte Anwendungspaket an einen Clientcomputer, bevor der Benutzer die Anwendung startet.</span><span class="sxs-lookup"><span data-stu-id="006c0-136">For load from file package delivery, the server delivers the entire virtualized application package to a client computer before the user launches the application.</span></span> <span data-ttu-id="006c0-137">In diesem Szenario werden virtualisierte Anwendungen als vollständige Pakete bereitgestellt und nicht über die dynamische, inkrementelle Methode, die vom dynamischen Übermittlungs Modell verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="006c0-137">In this scenario, virtualized applications are delivered as a full package, rather than through the dynamic, incremental method used by the dynamic delivery model.</span></span>

<span data-ttu-id="006c0-138">**Hinweis**  Für jede Zustellungsmethode sind der anfängliche Bereitstellungsprozess für die virtuelle Anwendung und der Aktualisierungsvorgang der virtuellen Anwendung identisch. das aktualisierte virtuelle Anwendungspaket ersetzt das ursprüngliche Anwendungspaket.</span><span class="sxs-lookup"><span data-stu-id="006c0-138">**Note** For each delivery method, the initial virtual application delivery process and the virtual application update process are the same; the updated virtual application package replaces the original application package.</span></span>

 

<span data-ttu-id="006c0-139">In der folgenden Tabelle werden die vor-und Nachteile der einzelnen Paketübermittlungsmethoden verglichen.</span><span class="sxs-lookup"><span data-stu-id="006c0-139">The following table compares the advantages and disadvantages of each package delivery method.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="006c0-140">Methode</span><span class="sxs-lookup"><span data-stu-id="006c0-140">Method</span></span></th>
<th align="left"><span data-ttu-id="006c0-141">Vorteile</span><span class="sxs-lookup"><span data-stu-id="006c0-141">Advantages</span></span></th>
<th align="left"><span data-ttu-id="006c0-142">Nachteile</span><span class="sxs-lookup"><span data-stu-id="006c0-142">Disadvantages</span></span></th>
<th align="left"><span data-ttu-id="006c0-143">Anmerkungen</span><span class="sxs-lookup"><span data-stu-id="006c0-143">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="006c0-144">Dynamische Paketzustellung</span><span class="sxs-lookup"><span data-stu-id="006c0-144">Dynamic package delivery</span></span></p></td>
<td align="left"><p><span data-ttu-id="006c0-145">Anwendungen werden nach Bedarf bereitgestellt und aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="006c0-145">Applications are delivered and updated on demand.</span></span></p>
<p><span data-ttu-id="006c0-146">Anwendungen werden bereitgestellt und inkrementell aktualisiert, um die Startzeit zu optimieren.</span><span class="sxs-lookup"><span data-stu-id="006c0-146">Applications are delivered and updated incrementally to optimize launch time.</span></span></p>
<p><span data-ttu-id="006c0-147">Updates werden automatisch an den Clientdesktop übermittelt.</span><span class="sxs-lookup"><span data-stu-id="006c0-147">Updates are delivered automatically to the client desktop.</span></span></p></td>
<td align="left"><p><span data-ttu-id="006c0-148">Größerer Speicherbedarf in der Unternehmenstopologie aufgrund von Server Anforderungen</span><span class="sxs-lookup"><span data-stu-id="006c0-148">Larger footprint in enterprise topology because of server requirements.</span></span></p>
<p><span data-ttu-id="006c0-149">Das Anwendungsstreaming sollte über ein LAN erfolgen. Bereitstellungsszenarien über ein WAN oder die Verwendung einer unzuverlässigen oder zeitweiligen Verbindung zwischen dem Server und dem Client sind möglicherweise unbrauchbar.</span><span class="sxs-lookup"><span data-stu-id="006c0-149">Application streaming should be over a LAN; deployment scenarios over a WAN or that use an unreliable or intermittent connection between the server and client might be unusable.</span></span></p></td>
<td align="left"><p><span data-ttu-id="006c0-150">Erfordert eine Streaming-Infrastruktur.</span><span class="sxs-lookup"><span data-stu-id="006c0-150">Requires a streaming infrastructure.</span></span></p>
<p><span data-ttu-id="006c0-151">Windows Installer, der zum Bereitstellen von Application Virtualization-Desktop Client Software für Endbenutzercomputer verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="006c0-151">Windows Installer used to deploy Application Virtualization Desktop Client software to end-user computers.</span></span></p>
<p><span data-ttu-id="006c0-152">Große Unternehmen sollten Application Virtualization Streaming Server als Verteilungspunkte verwenden.</span><span class="sxs-lookup"><span data-stu-id="006c0-152">Large enterprises should use Application Virtualization Streaming Servers as distribution points.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="006c0-153">Laden aus Dateipaket Zustellung</span><span class="sxs-lookup"><span data-stu-id="006c0-153">Load from file package delivery</span></span></p></td>
<td align="left"><p><span data-ttu-id="006c0-154">Konsistent mit typischen Unternehmensverwaltungsmethoden.</span><span class="sxs-lookup"><span data-stu-id="006c0-154">Consistent with typical enterprise management practices.</span></span></p>
<p><span data-ttu-id="006c0-155">Unterstützt eigenständige Konfigurationsszenarien.</span><span class="sxs-lookup"><span data-stu-id="006c0-155">Supports stand-alone configuration scenario.</span></span></p>
<p><span data-ttu-id="006c0-156">Bietet eine Lösung für das Problem von Micro-Branch Office.</span><span class="sxs-lookup"><span data-stu-id="006c0-156">Provides solution to micro–branch office problem.</span></span></p></td>
<td align="left"><p><span data-ttu-id="006c0-157">Die Anwendungs Zustellung und-Aktualisierung ist bei Bedarf nicht möglich.</span><span class="sxs-lookup"><span data-stu-id="006c0-157">Application delivery and update is not possible on-demand.</span></span></p>
<p><span data-ttu-id="006c0-158">Die Anwendungs Zustellung und-Aktualisierung ist nicht inkrementell; Sie erhöht den Ressourcenverbrauch relativ zur dynamischen Zustellung.</span><span class="sxs-lookup"><span data-stu-id="006c0-158">Application delivery and update is not incremental; it increases resource consumption relative to dynamic delivery.</span></span></p></td>
<td align="left"><p><span data-ttu-id="006c0-159">Die IT-Organisation ist häufig für die Verwaltung von Anwendungslizenzen, Benutzerautorisierung und Authentifizierung verantwortlich.</span><span class="sxs-lookup"><span data-stu-id="006c0-159">The IT organization is often responsible for managing application licenses, user authorization, and authentication.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="006c0-160">Server bezogene Protokolle und externe Komponenten</span><span class="sxs-lookup"><span data-stu-id="006c0-160">Server-Related Protocols and External Components</span></span>


<span data-ttu-id="006c0-161">In der folgenden Tabelle sind die Servertypen aufgeführt, die in einer Application Virtualization Server-basierten Szenarien verwendet werden können, zusammen mit den entsprechenden Übertragungsprotokollen und den externen Komponenten, die zur Unterstützung der spezifischen Serverkonfiguration erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="006c0-161">The following table lists the server types that can be used in an Application Virtualization Server-based scenarios, along with their corresponding transmission protocols and the external components needed to support the specific server configuration.</span></span> <span data-ttu-id="006c0-162">Die Tabelle enthält auch den Berichterstellungsmechanismus und den aktiven Aktualisierungsmechanismus für die einzelnen Servertypen.</span><span class="sxs-lookup"><span data-stu-id="006c0-162">The table also includes the reporting mechanism and the active upgrade mechanism for each server type.</span></span> <span data-ttu-id="006c0-163">Da diese Szenarien alle den Application Virtualization-Verwaltungs Server verwenden, können Sie die internen Berichterstellungsfunktionen verwenden, die in das System integriert sind.</span><span class="sxs-lookup"><span data-stu-id="006c0-163">Because these scenarios all use the Application Virtualization Management Server, you can use the internal reporting functionality that is built into the system.</span></span> <span data-ttu-id="006c0-164">Wenn Sie ein Application Virtualization Management oder einen Application Virtualization Streaming Server verwenden, um Pakete an den Client zu übermitteln, werden Pakete auf dem Server automatisch aktualisiert, wenn sich ein Benutzer beim Client anmeldet. Wenn Sie IIS-Server oder eine Datei verwenden, um die Pakete an den Client zu übermitteln, müssen die Pakete auf dem Client manuell aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="006c0-164">If you use an Application Virtualization Management or an Application Virtualization Streaming Server to deliver packages to the client, packages on the server are automatically upgraded when a user logs into the client; if you use IIS servers or a file to deliver the packages to the client, the packages on the client must be upgraded manually.</span></span>

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
<th align="left"><span data-ttu-id="006c0-165">Servertyp</span><span class="sxs-lookup"><span data-stu-id="006c0-165">Server Type</span></span></th>
<th align="left"><span data-ttu-id="006c0-166">Protokolle</span><span class="sxs-lookup"><span data-stu-id="006c0-166">Protocols</span></span></th>
<th align="left"><span data-ttu-id="006c0-167">Externe Komponenten erforderlich</span><span class="sxs-lookup"><span data-stu-id="006c0-167">External Components Needed</span></span></th>
<th align="left"><span data-ttu-id="006c0-168">Berichterstellung</span><span class="sxs-lookup"><span data-stu-id="006c0-168">Reporting</span></span></th>
<th align="left"><span data-ttu-id="006c0-169">Aktives Upgrade</span><span class="sxs-lookup"><span data-stu-id="006c0-169">Active Upgrade</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="006c0-170">Application Virtualization-Verwaltungs Server</span><span class="sxs-lookup"><span data-stu-id="006c0-170">Application Virtualization Management Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="006c0-171">RTSP</span><span class="sxs-lookup"><span data-stu-id="006c0-171">RTSP</span></span></p>
<p><span data-ttu-id="006c0-172">RTSPS</span><span class="sxs-lookup"><span data-stu-id="006c0-172">RTSPS</span></span></p></td>
<td align="left"><p><span data-ttu-id="006c0-173">Verwenden Sie bei Verwendung von HTTPS einen IIS-Server zum Herunterladen von ICO-und OSD-Dateien sowie eine Firewall, um den Server vor einer Gefährdung durch das Internet zu schützen.</span><span class="sxs-lookup"><span data-stu-id="006c0-173">When using HTTPS, use an IIS server to download ICO and OSD files and a firewall to protect the server from exposure to the Internet.</span></span></p></td>
<td align="left"><p><span data-ttu-id="006c0-174">Intern</span><span class="sxs-lookup"><span data-stu-id="006c0-174">Internal</span></span></p></td>
<td align="left"><p><span data-ttu-id="006c0-175">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="006c0-175">Supported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="006c0-176">Application Virtualization Streaming Server</span><span class="sxs-lookup"><span data-stu-id="006c0-176">Application Virtualization Streaming Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="006c0-177">RTSP</span><span class="sxs-lookup"><span data-stu-id="006c0-177">RTSP</span></span></p>
<p><span data-ttu-id="006c0-178">RTSPS</span><span class="sxs-lookup"><span data-stu-id="006c0-178">RTSPS</span></span></p></td>
<td align="left"><p><span data-ttu-id="006c0-179">Verwenden Sie einen Mechanismus, um den Inhalt zwischen dem Verwaltungsserver und dem Streamingserver zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="006c0-179">Use a mechanism to synchronize the content between the Management Server and the Streaming Server.</span></span> <span data-ttu-id="006c0-180">Verwenden Sie bei Verwendung von HTTPS einen IIS-Server zum Herunterladen von ICO-und OSD-Dateien, und verwenden Sie eine Firewall, um den Server vor der Gefährdung durch das Internet zu schützen.</span><span class="sxs-lookup"><span data-stu-id="006c0-180">When using HTTPS, use an IIS server to download ICO and OSD files and use a firewall to protect the server from exposure to the Internet.</span></span></p></td>
<td align="left"><p><span data-ttu-id="006c0-181">Intern</span><span class="sxs-lookup"><span data-stu-id="006c0-181">Internal</span></span></p></td>
<td align="left"><p><span data-ttu-id="006c0-182">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="006c0-182">Supported</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="006c0-183">IIS-Server</span><span class="sxs-lookup"><span data-stu-id="006c0-183">IIS server</span></span></p></td>
<td align="left"><p><span data-ttu-id="006c0-184">HTTP</span><span class="sxs-lookup"><span data-stu-id="006c0-184">HTTP</span></span></p>
<p><span data-ttu-id="006c0-185">HTTPS</span><span class="sxs-lookup"><span data-stu-id="006c0-185">HTTPS</span></span></p></td>
<td align="left"><p><span data-ttu-id="006c0-186">Verwenden Sie einen Mechanismus, um den Inhalt zwischen dem Verwaltungsserver und dem Streamingserver zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="006c0-186">Use a mechanism to synchronize the content between the Management Server and the Streaming Server.</span></span> <span data-ttu-id="006c0-187">Verwenden Sie bei Verwendung von http oder HTTPS einen IIS-Server zum Herunterladen von ICO-und OSD-Dateien sowie eine Firewall, um den Server vor der Gefährdung durch das Internet zu schützen.</span><span class="sxs-lookup"><span data-stu-id="006c0-187">When using HTTP or HTTPS, use an IIS server to download ICO and OSD files and a firewall to protect the server from exposure to the Internet.</span></span></p></td>
<td align="left"><p><span data-ttu-id="006c0-188">Intern</span><span class="sxs-lookup"><span data-stu-id="006c0-188">Internal</span></span></p></td>
<td align="left"><p><span data-ttu-id="006c0-189">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="006c0-189">Not Supported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="006c0-190">Datei</span><span class="sxs-lookup"><span data-stu-id="006c0-190">File</span></span></p></td>
<td align="left"><p><span data-ttu-id="006c0-191">SMB</span><span class="sxs-lookup"><span data-stu-id="006c0-191">SMB</span></span></p></td>
<td align="left"><p><span data-ttu-id="006c0-192">Sie benötigen eine Möglichkeit, den Inhalt zwischen dem Verwaltungsserver und dem Streamingserver zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="006c0-192">You need a way to synchronize the content between the Management Server and the Streaming Server.</span></span> <span data-ttu-id="006c0-193">Sie benötigen einen Clientcomputer mit Dateifreigabe-oder Streaming-Funktion.</span><span class="sxs-lookup"><span data-stu-id="006c0-193">You need a client computer with file sharing or streaming capability.</span></span></p></td>
<td align="left"><p><span data-ttu-id="006c0-194">Intern</span><span class="sxs-lookup"><span data-stu-id="006c0-194">Internal</span></span></p></td>
<td align="left"><p><span data-ttu-id="006c0-195">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="006c0-195">Not Supported</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="006c0-196">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="006c0-196">Related topics</span></span>


[<span data-ttu-id="006c0-197">Electronic Software Distribution-basiertes Szenario</span><span class="sxs-lookup"><span data-stu-id="006c0-197">Electronic Software Distribution-Based Scenario</span></span>](electronic-software-distribution-based-scenario.md)

[<span data-ttu-id="006c0-198">So konfigurieren Sie Server für die serverbasierte Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="006c0-198">How to Configure Servers for Server-Based Deployment</span></span>](how-to-configure-servers-for-server-based-deployment.md)

[<span data-ttu-id="006c0-199">So installieren Sie die Server und Systemkomponenten</span><span class="sxs-lookup"><span data-stu-id="006c0-199">How to Install the Servers and System Components</span></span>](how-to-install-the-servers-and-system-components.md)

 

 





