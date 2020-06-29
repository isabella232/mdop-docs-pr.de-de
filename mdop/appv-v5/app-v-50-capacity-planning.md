---
title: Planen der Kapazität für App-V 5.0
description: Planen der Kapazität für App-V 5.0
author: dansimp
ms.assetid: 56f48b00-cd91-4280-9481-5372a0e2e792
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9e828457a286f6f686c227a935828679514d87ad
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806038"
---
# <span data-ttu-id="329f2-103">Planen der Kapazität für App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="329f2-103">App-V 5.0 Capacity Planning</span></span>


<span data-ttu-id="329f2-104">Die folgenden Empfehlungen können als Basis für die Ermittlung der Kapazitäts Planungsinformationen verwendet werden, die für die App-V 5,0-Infrastruktur Ihrer Organisation geeignet sind.</span><span class="sxs-lookup"><span data-stu-id="329f2-104">The following recommendations can be used as a baseline to help determine capacity planning information that is appropriate to your organization’s App-V 5.0 infrastructure.</span></span>

<span data-ttu-id="329f2-105">**Wichtig**  Verwenden Sie die Informationen in diesem Abschnitt nur als Allgemeinen Leitfaden für die Planung Ihrer App-V 5,0-Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="329f2-105">**Important** Use the information in this section only as a general guide for planning your App-V 5.0 deployment.</span></span> <span data-ttu-id="329f2-106">Die Anforderungen an die Systemkapazität hängen von den spezifischen Details Ihrer Hardware-und Anwendungsumgebung ab.</span><span class="sxs-lookup"><span data-stu-id="329f2-106">Your system capacity requirements will depend on the specific details of your hardware and application environment.</span></span> <span data-ttu-id="329f2-107">Darüber hinaus sind die in diesem Dokument angezeigten Leistungsnummern Beispiele, und ihre Ergebnisse können variieren.</span><span class="sxs-lookup"><span data-stu-id="329f2-107">Additionally, the performance numbers displayed in this document are examples and your results may vary.</span></span>

 

## <span data-ttu-id="329f2-108">Ermitteln des Projektumfangs</span><span class="sxs-lookup"><span data-stu-id="329f2-108">Determine the Project Scope</span></span>


<span data-ttu-id="329f2-109">Bevor Sie die App-V 5,0-Infrastruktur entwerfen, müssen Sie den Projektbereich ermitteln.</span><span class="sxs-lookup"><span data-stu-id="329f2-109">Before you design the App-V 5.0 infrastructure, you must determine the project’s scope.</span></span> <span data-ttu-id="329f2-110">Der Bereich besteht darin, zu ermitteln, welche Anwendungen virtuell verfügbar sind, und um auch die Zielbenutzer und deren Speicherorte zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="329f2-110">The scope consists of determining which applications will be available virtually and to also identify the target users, and their locations.</span></span> <span data-ttu-id="329f2-111">Mithilfe dieser Informationen können Sie ermitteln, welche Art von App-V 5,0-Infrastruktur implementiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="329f2-111">This information will help determine what type of App-V 5.0 infrastructure should be implemented.</span></span> <span data-ttu-id="329f2-112">Entscheidungen bezüglich des Projektumfangs müssen auf den spezifischen Anforderungen Ihrer Organisation basieren.</span><span class="sxs-lookup"><span data-stu-id="329f2-112">Decisions about the scope of the project must be based on the specific needs of your organization.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="329f2-113">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="329f2-113">Task</span></span></th>
<th align="left"><span data-ttu-id="329f2-114">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="329f2-114">More Information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="329f2-115">Ermitteln des Anwendungsbereichs</span><span class="sxs-lookup"><span data-stu-id="329f2-115">Determine Application Scope</span></span></p></td>
<td align="left"><p><span data-ttu-id="329f2-116">Je nachdem, welche Anwendungen virtualisiert werden sollen, kann die App-V 5,0-Infrastruktur auf unterschiedliche Weise eingerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="329f2-116">Depending on the applications to be virtualized, the App-V 5.0 infrastructure can be set up in different ways.</span></span> <span data-ttu-id="329f2-117">Die erste Aufgabe besteht darin, zu definieren, welche Anwendungen virtualisiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="329f2-117">The first task is to define what applications you want to virtualize.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="329f2-118">Bestimmen des Positions Bereichs</span><span class="sxs-lookup"><span data-stu-id="329f2-118">Determine Location Scope</span></span></p></td>
<td align="left"><p><span data-ttu-id="329f2-119">Der Speicherort Bereich bezieht sich auf die physischen Standorte (beispielsweise unternehmensweit oder einen bestimmten geografischen Standort), in denen Sie die virtualisierten Anwendungen ausführen möchten.</span><span class="sxs-lookup"><span data-stu-id="329f2-119">Location scope refers to the physical locations (for example, enterprise-wide or a specific geographic location) where you plan to run the virtualized applications.</span></span> <span data-ttu-id="329f2-120">Sie kann sich auch auf die Benutzerpopulation beziehen (beispielsweise auf eine einzelne Abteilung), die die virtuellen Anwendungen ausführt.</span><span class="sxs-lookup"><span data-stu-id="329f2-120">It can also refer to the user population (for example, a single department) who will run the virtual applications.</span></span> <span data-ttu-id="329f2-121">Sie sollten eine Netzwerkübersicht erhalten, die die Verbindungspfade sowie die verfügbare Bandbreite für jeden Standort sowie die Anzahl der Benutzer, die virtualisierte Anwendungen verwenden, und die WAN-Verbindungsgeschwindigkeit umfasst.</span><span class="sxs-lookup"><span data-stu-id="329f2-121">You should obtain a network map that includes the connection paths as well as available bandwidth to each location and the number of users using virtualized applications and the WAN link speed.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="329f2-122">Ermitteln, welche App-V 5,0-Infrastruktur erforderlich ist</span><span class="sxs-lookup"><span data-stu-id="329f2-122">Determine Which App-V 5.0 Infrastructure is Required</span></span>


<span data-ttu-id="329f2-123">**Wichtig**  Bei den beiden folgenden Modellen muss der App-V 5,0-Client auf dem Computer installiert sein, auf dem Sie virtuelle Anwendungen ausführen möchten.</span><span class="sxs-lookup"><span data-stu-id="329f2-123">**Important** Both of the following models require the App-V 5.0 client to be installed on the computer where you plan to run virtual applications.</span></span>

<span data-ttu-id="329f2-124">Sie können Ihre App-V 5,0-Umgebung auch mithilfe einer ESD-Lösung (Electronic Software Distribution) wie Microsoft Systems Center Configuration Manager verwalten.</span><span class="sxs-lookup"><span data-stu-id="329f2-124">You can also manage your App-V 5.0 environment using an Electronic Software Distribution (ESD) solution such as Microsoft Systems Center Configuration Manager.</span></span> <span data-ttu-id="329f2-125">Weitere Informationen finden Sie unter [Bereitstellen von App-V 5,0-Paketen mithilfe von ESD (Electronic Software Distribution)](deploying-app-v-50-packages-by-using-electronic-software-distribution--esd-.md).</span><span class="sxs-lookup"><span data-stu-id="329f2-125">For more information see [Deploying App-V 5.0 Packages by Using Electronic Software Distribution (ESD)](deploying-app-v-50-packages-by-using-electronic-software-distribution--esd-.md).</span></span>

 

-   <span data-ttu-id="329f2-126">**Eigenständiges Modell** : das eigenständige Modell ermöglicht es virtuellen Anwendungen, Windows Installer für die Verteilung ohne Streaming zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="329f2-126">**Standalone Model** - The standalone model allows virtual applications to be Windows Installer-enabled for distribution without streaming.</span></span> <span data-ttu-id="329f2-127">App-V 5,0 im Standalone-Modus besteht aus Sequencer und Client; Es sind keine zusätzlichen Komponenten erforderlich.</span><span class="sxs-lookup"><span data-stu-id="329f2-127">App-V 5.0 in Standalone Mode consists of the sequencer and the client; no additional components are required.</span></span> <span data-ttu-id="329f2-128">Anwendungen werden mithilfe eines Prozesses, der als Sequenzierung bezeichnet wird, für die Virtualisierung vorbereitet.</span><span class="sxs-lookup"><span data-stu-id="329f2-128">Applications are prepared for virtualization using a process called sequencing.</span></span> <span data-ttu-id="329f2-129">Weitere Informationen finden Sie unter [Planen der App-V 5,0-Sequenzer und Client Bereitstellung](planning-for-the-app-v-50-sequencer-and-client-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="329f2-129">For more information see, [Planning for the App-V 5.0 Sequencer and Client Deployment](planning-for-the-app-v-50-sequencer-and-client-deployment.md).</span></span> <span data-ttu-id="329f2-130">Das eigenständige Modell wird für die folgenden Szenarien empfohlen:</span><span class="sxs-lookup"><span data-stu-id="329f2-130">The stand-alone model is recommended for the following scenarios:</span></span>

    -   <span data-ttu-id="329f2-131">Mit getrennten Remotebenutzern, die keine Verbindung mit der App-V 5,0-Infrastruktur herstellen können.</span><span class="sxs-lookup"><span data-stu-id="329f2-131">With disconnected remote users who cannot connect to the App-V 5.0 infrastructure.</span></span>

    -   <span data-ttu-id="329f2-132">Wenn Sie ein Softwareverwaltungssystem wie Configuration Manager 2012 ausführen.</span><span class="sxs-lookup"><span data-stu-id="329f2-132">When you are running a software management system, such as Configuration Manager 2012.</span></span>

    -   <span data-ttu-id="329f2-133">Wenn Netzwerkbandbreite-Einschränkungen die elektronische Softwareverteilung hemmen.</span><span class="sxs-lookup"><span data-stu-id="329f2-133">When network bandwidth limitations inhibit electronic software distribution.</span></span>

-   <span data-ttu-id="329f2-134">**Vollständiges Infrastrukturmodell** – das vollständige Infrastrukturmodell bietet Software Verteilungs-, Verwaltungs-und Berichterstattungsfunktionen. Darüber hinaus wird das Streaming von Anwendungen im gesamten Netzwerk berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="329f2-134">**Full Infrastructure Model** - The full infrastructure model provides for software distribution, management, and reporting capabilities; it also includes the streaming of applications across the network.</span></span> <span data-ttu-id="329f2-135">Das vollständige Infrastrukturmodell der APP-v 5,0 besteht aus einem oder mehreren App-v 5,0-Verwaltungsservern.</span><span class="sxs-lookup"><span data-stu-id="329f2-135">The App-V 5.0 Full Infrastructure Model consists of one or more App-V 5.0 management servers.</span></span> <span data-ttu-id="329f2-136">Der Verwaltungs Server kann zum Veröffentlichen von Anwendungen für alle Clients verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="329f2-136">The Management Server can be used to publish applications to all clients.</span></span> <span data-ttu-id="329f2-137">Beim Veröffentlichungsprozess werden die virtuellen Anwendungssymbole und-Verknüpfungen auf dem Zielcomputer platziert.</span><span class="sxs-lookup"><span data-stu-id="329f2-137">The publishing process places the virtual application icons and shortcuts on the target computer.</span></span> <span data-ttu-id="329f2-138">Sie kann Anwendungen auch an lokale Benutzer streamen.</span><span class="sxs-lookup"><span data-stu-id="329f2-138">It can also stream applications to local users.</span></span> <span data-ttu-id="329f2-139">Weitere Informationen zum Installieren des Verwaltungsservers finden Sie unter [Planen der App-V 5,0-Server Bereitstellung](planning-for-the-app-v-50-server-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="329f2-139">For more information about installing the management server see, [Planning for the App-V 5.0 Server Deployment](planning-for-the-app-v-50-server-deployment.md).</span></span> <span data-ttu-id="329f2-140">Das vollständige Infrastrukturmodell wird für die folgenden Szenarien empfohlen:</span><span class="sxs-lookup"><span data-stu-id="329f2-140">The full infrastructure model is recommended for the following scenarios:</span></span>

    <span data-ttu-id="329f2-141">**Wichtig**  Das vollständige Infrastrukturmodell der App-V 5,0 erfordert, dass Microsoft SQL Server Konfigurationsdaten speichert.</span><span class="sxs-lookup"><span data-stu-id="329f2-141">**Important** The App-V 5.0 full infrastructure model requires Microsoft SQL Server to store configuration data.</span></span> <span data-ttu-id="329f2-142">Weitere Informationen finden Sie unter [unterstützte Konfigurationen für App-V 5,0](app-v-50-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="329f2-142">For more information see [App-V 5.0 Supported Configurations](app-v-50-supported-configurations.md).</span></span>

     

    -   <span data-ttu-id="329f2-143">Wenn Sie den Verwaltungs Server verwenden möchten, um die Anwendung auf Zielcomputern zu veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="329f2-143">When you want to use the Management Server to publish the application to target computers.</span></span>

    -   <span data-ttu-id="329f2-144">Schnelle Bereitstellung von Anwendungen für die Zielcomputer.</span><span class="sxs-lookup"><span data-stu-id="329f2-144">For rapid provisioning of applications to target computers.</span></span>

    -   <span data-ttu-id="329f2-145">Wenn Sie die App-V 5,0-Berichterstellung verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="329f2-145">When you want to use App-V 5.0 reporting.</span></span>

## <span data-ttu-id="329f2-146">Richtlinien für die End-to-End-Server Größe</span><span class="sxs-lookup"><span data-stu-id="329f2-146">End-to-end Server Sizing Guidance</span></span>


<span data-ttu-id="329f2-147">Der folgende Abschnitt enthält Informationen zur End-to-End-App-V 5,0-Größenanpassung und-Planung.</span><span class="sxs-lookup"><span data-stu-id="329f2-147">The following section provides information about end-to-end App-V 5.0 sizing and planning.</span></span> <span data-ttu-id="329f2-148">Weitere spezifische Informationen finden Sie in den folgenden Abschnitten.</span><span class="sxs-lookup"><span data-stu-id="329f2-148">For more specific information, refer to the subsequent sections.</span></span>

<span data-ttu-id="329f2-149">**Hinweis**  Die Antwortzeit für Roundtrips auf dem Client ist die Zeit, die der Computer mit dem App-V 5,0-Client erhält, um eine erfolgreiche Benachrichtigung vom Veröffentlichungsserver zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="329f2-149">**Note** Round trip response time on the client is the time taken by the computer running the App-V 5.0 client to receive a successful notification from the publishing server.</span></span> <span data-ttu-id="329f2-150">Die Antwortzeit für Roundtrips auf dem Veröffentlichungsserver ist die Zeit, die der Computer, auf dem der Veröffentlichungsserver ausgeführt wird, zum Empfangen einer erfolgreichen Paketmetadaten-Aktualisierung vom Verwaltungsserver einnimmt.</span><span class="sxs-lookup"><span data-stu-id="329f2-150">Round trip response time on the publishing server is the time taken by the computer running the publishing server to receive a successful package metadata update from the management server.</span></span>

 

-   <span data-ttu-id="329f2-151">20.000-Clients können auf einen einzelnen Veröffentlichungsserver Zielen, um die Paketaktualisierungen in einer akzeptablen Roundtrip-Zeit zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="329f2-151">20,000 clients can target a single publishing server to obtain the package refreshes in an acceptable round trip time.</span></span> <span data-ttu-id="329f2-152">( &lt; 3 Sekunden)</span><span class="sxs-lookup"><span data-stu-id="329f2-152">(&lt;3 seconds)</span></span>

-   <span data-ttu-id="329f2-153">Ein einzelner Verwaltungsserver kann bis zu 50-Publishing Server für die Aktualisierung von Paketmetadaten in einer akzeptablen Roundtrip-Zeit unterstützen.</span><span class="sxs-lookup"><span data-stu-id="329f2-153">A single management server can support up to 50 publishing servers for package metadata refreshes in an acceptable round trip time.</span></span> <span data-ttu-id="329f2-154">( &lt; 5 Sekunden)</span><span class="sxs-lookup"><span data-stu-id="329f2-154">(&lt;5 seconds)</span></span>

## <a href="" id="---------app-v-5-0-management-server-capacity-planning-recommendations"></a> <span data-ttu-id="329f2-155">Empfehlungen für die Kapazitätsplanung für App-V 5,0-Verwaltungs Server</span><span class="sxs-lookup"><span data-stu-id="329f2-155">App-V 5.0 Management Server Capacity Planning Recommendations</span></span>


<span data-ttu-id="329f2-156">Für die App-V 5,0-Veröffentlichungsserver ist der Verwaltungsserver für Paket Aktualisierungsanforderungen und Paket Aktualisierungs Antworten erforderlich.</span><span class="sxs-lookup"><span data-stu-id="329f2-156">The App-V 5.0 publishing servers require the management server for package refresh requests and package refresh responses.</span></span> <span data-ttu-id="329f2-157">Der Verwaltungsserver sendet dann die Informationen an die Verwaltungsdatenbank, um Informationen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="329f2-157">The management server then sends the information to the management database to retrieve information.</span></span> <span data-ttu-id="329f2-158">Weitere Informationen zu den unterstützten Konfigurationen des App-v 5,0-Verwaltungsservers finden Sie unter [unterstützte Konfigurationen für App-v 5,0](app-v-50-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="329f2-158">For more information about App-V 5.0 management server supported configurations see [App-V 5.0 Supported Configurations](app-v-50-supported-configurations.md).</span></span>

<span data-ttu-id="329f2-159">**Hinweis**  Die standardmäßige Aktualisierungszeit auf dem App-V 5,0-Veröffentlichungsserver beträgt zehn Minuten.</span><span class="sxs-lookup"><span data-stu-id="329f2-159">**Note** The default refresh time on the App-V 5.0 publishing server is ten minutes.</span></span>

 

<span data-ttu-id="329f2-160">Wenn mehrere gleichzeitige Veröffentlichungsserver einen einzelnen Verwaltungsserver für die Aktualisierung von Paketmetadaten kontaktieren, beeinflussen die folgenden drei Faktoren die Antwortzeit für Roundtrips auf dem Veröffentlichungsserver:</span><span class="sxs-lookup"><span data-stu-id="329f2-160">When multiple simultaneous publishing servers contact a single management server for package metadata refreshes, the following three factors influence the round trip response time on the publishing server:</span></span>

1.  <span data-ttu-id="329f2-161">Die Anzahl von Veröffentlichungsservern, die gleichzeitige Anforderungen stellen.</span><span class="sxs-lookup"><span data-stu-id="329f2-161">Number of publishing servers making simultaneous requests.</span></span>

2.  <span data-ttu-id="329f2-162">Die Anzahl der auf dem Verwaltungsserver konfigurierten Verbindungsgruppen.</span><span class="sxs-lookup"><span data-stu-id="329f2-162">Number of connection groups configured on the management server.</span></span>

3.  <span data-ttu-id="329f2-163">Die Anzahl der auf dem Verwaltungsserver konfigurierten Zugriffsgruppen.</span><span class="sxs-lookup"><span data-stu-id="329f2-163">Number of access groups configured on the management server.</span></span>

<span data-ttu-id="329f2-164">In der folgenden Tabelle werden weitere Informationen zu jedem Faktor angezeigt, der sich auf die Roundtrip-Zeit auswirkt.</span><span class="sxs-lookup"><span data-stu-id="329f2-164">The following table displays more information about each factor that impacts round trip time.</span></span>

<span data-ttu-id="329f2-165">**Hinweis**  "Roundtrip-Antwortzeit" ist die Zeit, die der Computer ausführt, auf dem der App-V 5,0-Publishing Server ausgeführt wird, um ein erfolgreiches Paketmetadaten-Update vom Verwaltungsserver zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="329f2-165">**Note** Round trip response time is the time taken by the computer running the App-V 5.0 publishing server to receive a successful package metadata update from the management server.</span></span>

 

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="329f2-166">Faktoren, die sich auf die Reaktionszeit von Roundtrips auswirken</span><span class="sxs-lookup"><span data-stu-id="329f2-166">Factors impacting round trip response time</span></span></th>
<th align="left"><span data-ttu-id="329f2-167">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="329f2-167">More Information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="329f2-168">Die Anzahl der Veröffentlichungsserver, die Paketmetadaten gleichzeitig anfordern, wird aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="329f2-168">The number of publishing servers simultaneously requesting package metadata refreshes.</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="329f2-169">Ein einzelner Verwaltungsserver kann auf bis zu 320-Publishing Servern Antworten, die gleichzeitig Veröffentlichungsmetadaten anfordern.</span><span class="sxs-lookup"><span data-stu-id="329f2-169">A single management server can respond to up to 320 publishing servers requesting publishing metadata simultaneously.</span></span></p></li>
<li><p><span data-ttu-id="329f2-170">Die Antwortzeit für Roundtrips für 320-pub-Server beträgt ~ 40 Sekunden.</span><span class="sxs-lookup"><span data-stu-id="329f2-170">Round trip response time for 320 pub servers is ~40 seconds.</span></span></p></li>
<li><p><span data-ttu-id="329f2-171">Bei &lt; 50-Publishing Servern, die Metadaten gleichzeitig anfordern, beträgt die Antwortzeit für Roundtrips &lt; 5 Sekunden.</span><span class="sxs-lookup"><span data-stu-id="329f2-171">For &lt;50 publishing servers requesting metadata simultaneously, the round trip response time is &lt;5 seconds.</span></span></p></li>
<li><p><span data-ttu-id="329f2-172">Von 50 zu 320-Publishing Servern vergrößert sich die Antwortzeit linear (ca. 2x).</span><span class="sxs-lookup"><span data-stu-id="329f2-172">From 50 to 320 publishing servers, the response time increases linearly (approximately 2x).</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="329f2-173">Die Anzahl der auf dem Verwaltungsserver konfigurierten Verbindungsgruppen.</span><span class="sxs-lookup"><span data-stu-id="329f2-173">The number of connection groups configured on the management server.</span></span></p>
<p></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="329f2-174">Für bis zu 100-Verbindungsgruppen gibt es keine signifikante Änderung der Roundtrip-Antwortzeit auf dem Veröffentlichungsserver.</span><span class="sxs-lookup"><span data-stu-id="329f2-174">For up to 100 connection groups, there is no significant change in the round trip response time on the publishing server.</span></span></p></li>
<li><p><span data-ttu-id="329f2-175">Bei 100-400-Verbindungsgruppen gibt es eine geringfügige lineare Erhöhung der Antwortzeit für Roundtrips.</span><span class="sxs-lookup"><span data-stu-id="329f2-175">For 100 - 400 connection groups, there is a minor linear increase in the round trip response time.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="329f2-176">Die Anzahl der Zugriffsgruppen, die auf dem Verwaltungsserver konfiguriert sind.</span><span class="sxs-lookup"><span data-stu-id="329f2-176">The number of access groups configured on the management server.</span></span></p>
<p></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="329f2-177">Für bis zu 40-Zugriffsgruppen gibt es eine lineare (ungefähr 3X) höhere Vergrößerung der Roundtrip-Antwortzeit auf dem Veröffentlichungsserver.</span><span class="sxs-lookup"><span data-stu-id="329f2-177">For up to 40 access groups, there is a linear (approximately 3x) increase in the round trip response time on the publishing server.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="329f2-178">In der folgenden Tabelle werden die Beispielwerte für die einzelnen vorherigen Faktoren angezeigt.</span><span class="sxs-lookup"><span data-stu-id="329f2-178">The following table displays sample values for each of the previous factors.</span></span> <span data-ttu-id="329f2-179">In jeder Variation werden 120-Pakete vom App-V 5.0-Verwaltungsserver aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="329f2-179">In each variation, 120 packages are refreshed from the App-V 5.0management server.</span></span>

<table>
<colgroup>
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="329f2-180">Szenario</span><span class="sxs-lookup"><span data-stu-id="329f2-180">Scenario</span></span></th>
<th align="left"><span data-ttu-id="329f2-181">Variante</span><span class="sxs-lookup"><span data-stu-id="329f2-181">Variation</span></span></th>
<th align="left"><span data-ttu-id="329f2-182">Anzahl der Verbindungsgruppen</span><span class="sxs-lookup"><span data-stu-id="329f2-182">Number of connection groups</span></span></th>
<th align="left"><span data-ttu-id="329f2-183">Anzahl der Zugriffsgruppen</span><span class="sxs-lookup"><span data-stu-id="329f2-183">Number of access groups</span></span></th>
<th align="left"><span data-ttu-id="329f2-184">Anzahl der Veröffentlichungsserver</span><span class="sxs-lookup"><span data-stu-id="329f2-184">Number of publishing servers</span></span></th>
<th align="left"><span data-ttu-id="329f2-185">Netzwerkverbindungstyp, Veröffentlichungsserver/Verwaltungsserver</span><span class="sxs-lookup"><span data-stu-id="329f2-185">Network connection type publishing server / management server</span></span></th>
<th align="left"><span data-ttu-id="329f2-186">Roundtrip-Antwortzeit auf dem Veröffentlichungsserver (in Sekunden)</span><span class="sxs-lookup"><span data-stu-id="329f2-186">Round trip response time on the publishing server (in seconds)</span></span></th>
<th align="left"><span data-ttu-id="329f2-187">CPU-Auslastung auf dem Verwaltungsserver</span><span class="sxs-lookup"><span data-stu-id="329f2-187">CPU utilization on management server</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="329f2-188">Publishing Server wenden sich gleichzeitig an den Verwaltungsserver, um Metadaten zu veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="329f2-188">Publishing servers simultaneously contacting management server for publishing metadata.</span></span></p></td>
<td align="left"><p><span data-ttu-id="329f2-189">Anzahl der Veröffentlichungsserver</span><span class="sxs-lookup"><span data-stu-id="329f2-189">Number of publishing servers</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="329f2-190">0</span><span class="sxs-lookup"><span data-stu-id="329f2-190">0</span></span></p></li>
<li><p><span data-ttu-id="329f2-191">0</span><span class="sxs-lookup"><span data-stu-id="329f2-191">0</span></span></p></li>
<li><p><span data-ttu-id="329f2-192">0</span><span class="sxs-lookup"><span data-stu-id="329f2-192">0</span></span></p></li>
<li><p><span data-ttu-id="329f2-193">0</span><span class="sxs-lookup"><span data-stu-id="329f2-193">0</span></span></p></li>
<li><p><span data-ttu-id="329f2-194">0</span><span class="sxs-lookup"><span data-stu-id="329f2-194">0</span></span></p></li>
<li><p><span data-ttu-id="329f2-195">0</span><span class="sxs-lookup"><span data-stu-id="329f2-195">0</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="329f2-196">1</span><span class="sxs-lookup"><span data-stu-id="329f2-196">1</span></span></p></li>
<li><p><span data-ttu-id="329f2-197">1</span><span class="sxs-lookup"><span data-stu-id="329f2-197">1</span></span></p></li>
<li><p><span data-ttu-id="329f2-198">1</span><span class="sxs-lookup"><span data-stu-id="329f2-198">1</span></span></p></li>
<li><p><span data-ttu-id="329f2-199">1</span><span class="sxs-lookup"><span data-stu-id="329f2-199">1</span></span></p></li>
<li><p><span data-ttu-id="329f2-200">1</span><span class="sxs-lookup"><span data-stu-id="329f2-200">1</span></span></p></li>
<li><p><span data-ttu-id="329f2-201">1</span><span class="sxs-lookup"><span data-stu-id="329f2-201">1</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="329f2-202">50</span><span class="sxs-lookup"><span data-stu-id="329f2-202">50</span></span></p></li>
<li><p><span data-ttu-id="329f2-203">100</span><span class="sxs-lookup"><span data-stu-id="329f2-203">100</span></span></p></li>
<li><p><span data-ttu-id="329f2-204">200</span><span class="sxs-lookup"><span data-stu-id="329f2-204">200</span></span></p></li>
<li><p><span data-ttu-id="329f2-205">300</span><span class="sxs-lookup"><span data-stu-id="329f2-205">300</span></span></p></li>
<li><p><span data-ttu-id="329f2-206">315</span><span class="sxs-lookup"><span data-stu-id="329f2-206">315</span></span></p></li>
<li><p><span data-ttu-id="329f2-207">320</span><span class="sxs-lookup"><span data-stu-id="329f2-207">320</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="329f2-208">LAN</span><span class="sxs-lookup"><span data-stu-id="329f2-208">LAN</span></span></p></li>
<li><p><span data-ttu-id="329f2-209">LAN</span><span class="sxs-lookup"><span data-stu-id="329f2-209">LAN</span></span></p></li>
<li><p><span data-ttu-id="329f2-210">LAN</span><span class="sxs-lookup"><span data-stu-id="329f2-210">LAN</span></span></p></li>
<li><p><span data-ttu-id="329f2-211">LAN</span><span class="sxs-lookup"><span data-stu-id="329f2-211">LAN</span></span></p></li>
<li><p><span data-ttu-id="329f2-212">LAN</span><span class="sxs-lookup"><span data-stu-id="329f2-212">LAN</span></span></p></li>
<li><p><span data-ttu-id="329f2-213">LAN</span><span class="sxs-lookup"><span data-stu-id="329f2-213">LAN</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="329f2-214">5</span><span class="sxs-lookup"><span data-stu-id="329f2-214">5</span></span></p></li>
<li><p><span data-ttu-id="329f2-215">10</span><span class="sxs-lookup"><span data-stu-id="329f2-215">10</span></span></p></li>
<li><p><span data-ttu-id="329f2-216">19</span><span class="sxs-lookup"><span data-stu-id="329f2-216">19</span></span></p></li>
<li><p><span data-ttu-id="329f2-217">32</span><span class="sxs-lookup"><span data-stu-id="329f2-217">32</span></span></p></li>
<li><p><span data-ttu-id="329f2-218">30</span><span class="sxs-lookup"><span data-stu-id="329f2-218">30</span></span></p></li>
<li><p><span data-ttu-id="329f2-219">37</span><span class="sxs-lookup"><span data-stu-id="329f2-219">37</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="329f2-220">17</span><span class="sxs-lookup"><span data-stu-id="329f2-220">17</span></span></p></li>
<li><p><span data-ttu-id="329f2-221">17</span><span class="sxs-lookup"><span data-stu-id="329f2-221">17</span></span></p></li>
<li><p><span data-ttu-id="329f2-222">17</span><span class="sxs-lookup"><span data-stu-id="329f2-222">17</span></span></p></li>
<li><p><span data-ttu-id="329f2-223">15</span><span class="sxs-lookup"><span data-stu-id="329f2-223">15</span></span></p></li>
<li><p><span data-ttu-id="329f2-224">17</span><span class="sxs-lookup"><span data-stu-id="329f2-224">17</span></span></p></li>
<li><p><span data-ttu-id="329f2-225">15</span><span class="sxs-lookup"><span data-stu-id="329f2-225">15</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="329f2-226">Veröffentlichungsmetadaten enthält Verbindungsgruppen</span><span class="sxs-lookup"><span data-stu-id="329f2-226">Publishing metadata contains connection groups</span></span></p></td>
<td align="left"><p><span data-ttu-id="329f2-227">Anzahl der Verbindungsgruppen</span><span class="sxs-lookup"><span data-stu-id="329f2-227">Number of connection groups</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="329f2-228">10</span><span class="sxs-lookup"><span data-stu-id="329f2-228">10</span></span></p></li>
<li><p><span data-ttu-id="329f2-229">50</span><span class="sxs-lookup"><span data-stu-id="329f2-229">50</span></span></p></li>
<li><p><span data-ttu-id="329f2-230">100</span><span class="sxs-lookup"><span data-stu-id="329f2-230">100</span></span></p></li>
<li><p><span data-ttu-id="329f2-231">150</span><span class="sxs-lookup"><span data-stu-id="329f2-231">150</span></span></p></li>
<li><p><span data-ttu-id="329f2-232">300</span><span class="sxs-lookup"><span data-stu-id="329f2-232">300</span></span></p></li>
<li><p><span data-ttu-id="329f2-233">400</span><span class="sxs-lookup"><span data-stu-id="329f2-233">400</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="329f2-234">1</span><span class="sxs-lookup"><span data-stu-id="329f2-234">1</span></span></p></li>
<li><p><span data-ttu-id="329f2-235">1</span><span class="sxs-lookup"><span data-stu-id="329f2-235">1</span></span></p></li>
<li><p><span data-ttu-id="329f2-236">1</span><span class="sxs-lookup"><span data-stu-id="329f2-236">1</span></span></p></li>
<li><p><span data-ttu-id="329f2-237">1</span><span class="sxs-lookup"><span data-stu-id="329f2-237">1</span></span></p></li>
<li><p><span data-ttu-id="329f2-238">1</span><span class="sxs-lookup"><span data-stu-id="329f2-238">1</span></span></p></li>
<li><p><span data-ttu-id="329f2-239">1</span><span class="sxs-lookup"><span data-stu-id="329f2-239">1</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="329f2-240">100</span><span class="sxs-lookup"><span data-stu-id="329f2-240">100</span></span></p></li>
<li><p><span data-ttu-id="329f2-241">100</span><span class="sxs-lookup"><span data-stu-id="329f2-241">100</span></span></p></li>
<li><p><span data-ttu-id="329f2-242">100</span><span class="sxs-lookup"><span data-stu-id="329f2-242">100</span></span></p></li>
<li><p><span data-ttu-id="329f2-243">100</span><span class="sxs-lookup"><span data-stu-id="329f2-243">100</span></span></p></li>
<li><p><span data-ttu-id="329f2-244">100</span><span class="sxs-lookup"><span data-stu-id="329f2-244">100</span></span></p></li>
<li><p><span data-ttu-id="329f2-245">100</span><span class="sxs-lookup"><span data-stu-id="329f2-245">100</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="329f2-246">LAN</span><span class="sxs-lookup"><span data-stu-id="329f2-246">LAN</span></span></p></li>
<li><p><span data-ttu-id="329f2-247">LAN</span><span class="sxs-lookup"><span data-stu-id="329f2-247">LAN</span></span></p></li>
<li><p><span data-ttu-id="329f2-248">LAN</span><span class="sxs-lookup"><span data-stu-id="329f2-248">LAN</span></span></p></li>
<li><p><span data-ttu-id="329f2-249">LAN</span><span class="sxs-lookup"><span data-stu-id="329f2-249">LAN</span></span></p></li>
<li><p><span data-ttu-id="329f2-250">LAN</span><span class="sxs-lookup"><span data-stu-id="329f2-250">LAN</span></span></p></li>
<li><p><span data-ttu-id="329f2-251">LAN</span><span class="sxs-lookup"><span data-stu-id="329f2-251">LAN</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="329f2-252">10</span><span class="sxs-lookup"><span data-stu-id="329f2-252">10</span></span></p></li>
<li><p><span data-ttu-id="329f2-253">11</span><span class="sxs-lookup"><span data-stu-id="329f2-253">11</span></span></p></li>
<li><p><span data-ttu-id="329f2-254">11</span><span class="sxs-lookup"><span data-stu-id="329f2-254">11</span></span></p></li>
<li><p><span data-ttu-id="329f2-255">16</span><span class="sxs-lookup"><span data-stu-id="329f2-255">16</span></span></p></li>
<li><p><span data-ttu-id="329f2-256">22</span><span class="sxs-lookup"><span data-stu-id="329f2-256">22</span></span></p></li>
<li><p><span data-ttu-id="329f2-257">25</span><span class="sxs-lookup"><span data-stu-id="329f2-257">25</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="329f2-258">17</span><span class="sxs-lookup"><span data-stu-id="329f2-258">17</span></span></p></li>
<li><p><span data-ttu-id="329f2-259">19</span><span class="sxs-lookup"><span data-stu-id="329f2-259">19</span></span></p></li>
<li><p><span data-ttu-id="329f2-260">22</span><span class="sxs-lookup"><span data-stu-id="329f2-260">22</span></span></p></li>
<li><p><span data-ttu-id="329f2-261">19</span><span class="sxs-lookup"><span data-stu-id="329f2-261">19</span></span></p></li>
<li><p><span data-ttu-id="329f2-262">20</span><span class="sxs-lookup"><span data-stu-id="329f2-262">20</span></span></p></li>
<li><p><span data-ttu-id="329f2-263">20</span><span class="sxs-lookup"><span data-stu-id="329f2-263">20</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="329f2-264">Veröffentlichungsmetadaten enthalten Zugriffsgruppen</span><span class="sxs-lookup"><span data-stu-id="329f2-264">Publishing metadata contains access groups</span></span></p></td>
<td align="left"><p><span data-ttu-id="329f2-265">Anzahl der Zugriffsgruppen</span><span class="sxs-lookup"><span data-stu-id="329f2-265">Number of access groups</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="329f2-266">0</span><span class="sxs-lookup"><span data-stu-id="329f2-266">0</span></span></p></li>
<li><p><span data-ttu-id="329f2-267">0</span><span class="sxs-lookup"><span data-stu-id="329f2-267">0</span></span></p></li>
<li><p><span data-ttu-id="329f2-268">0</span><span class="sxs-lookup"><span data-stu-id="329f2-268">0</span></span></p></li>
<li><p><span data-ttu-id="329f2-269">0</span><span class="sxs-lookup"><span data-stu-id="329f2-269">0</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="329f2-270">1</span><span class="sxs-lookup"><span data-stu-id="329f2-270">1</span></span></p></li>
<li><p><span data-ttu-id="329f2-271">10</span><span class="sxs-lookup"><span data-stu-id="329f2-271">10</span></span></p></li>
<li><p><span data-ttu-id="329f2-272">20</span><span class="sxs-lookup"><span data-stu-id="329f2-272">20</span></span></p></li>
<li><p><span data-ttu-id="329f2-273">40</span><span class="sxs-lookup"><span data-stu-id="329f2-273">40</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="329f2-274">100</span><span class="sxs-lookup"><span data-stu-id="329f2-274">100</span></span></p></li>
<li><p><span data-ttu-id="329f2-275">100</span><span class="sxs-lookup"><span data-stu-id="329f2-275">100</span></span></p></li>
<li><p><span data-ttu-id="329f2-276">100</span><span class="sxs-lookup"><span data-stu-id="329f2-276">100</span></span></p></li>
<li><p><span data-ttu-id="329f2-277">100</span><span class="sxs-lookup"><span data-stu-id="329f2-277">100</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="329f2-278">LAN</span><span class="sxs-lookup"><span data-stu-id="329f2-278">LAN</span></span></p></li>
<li><p><span data-ttu-id="329f2-279">LAN</span><span class="sxs-lookup"><span data-stu-id="329f2-279">LAN</span></span></p></li>
<li><p><span data-ttu-id="329f2-280">LAN</span><span class="sxs-lookup"><span data-stu-id="329f2-280">LAN</span></span></p></li>
<li><p><span data-ttu-id="329f2-281">LAN</span><span class="sxs-lookup"><span data-stu-id="329f2-281">LAN</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="329f2-282">10</span><span class="sxs-lookup"><span data-stu-id="329f2-282">10</span></span></p></li>
<li><p><span data-ttu-id="329f2-283">43</span><span class="sxs-lookup"><span data-stu-id="329f2-283">43</span></span></p></li>
<li><p><span data-ttu-id="329f2-284">153</span><span class="sxs-lookup"><span data-stu-id="329f2-284">153</span></span></p></li>
<li><p><span data-ttu-id="329f2-285">535</span><span class="sxs-lookup"><span data-stu-id="329f2-285">535</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="329f2-286">17</span><span class="sxs-lookup"><span data-stu-id="329f2-286">17</span></span></p></li>
<li><p><span data-ttu-id="329f2-287">26</span><span class="sxs-lookup"><span data-stu-id="329f2-287">26</span></span></p></li>
<li><p><span data-ttu-id="329f2-288">24</span><span class="sxs-lookup"><span data-stu-id="329f2-288">24</span></span></p></li>
<li><p><span data-ttu-id="329f2-289">24</span><span class="sxs-lookup"><span data-stu-id="329f2-289">24</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="329f2-290">Die CPU-Auslastung des Computers, auf dem der Verwaltungsserver ausgeführt wird, beträgt rund 25%, unabhängig davon, wie viele Veröffentlichungsserver darauf ausgerichtet sind.</span><span class="sxs-lookup"><span data-stu-id="329f2-290">The CPU utilization of the computer running the management server is around 25% irrespective of the number of publishing servers targeting it.</span></span> <span data-ttu-id="329f2-291">Die Microsoft SQL Server-Datenbank Transaktionen/Sek., Batchanforderungen/Sek. und Benutzer Verbindungen sind unabhängig von der Anzahl der Veröffentlichungsserver identisch.</span><span class="sxs-lookup"><span data-stu-id="329f2-291">The Microsoft SQL Server database transactions/sec, batch requests/sec and user connections are identical irrespective of the number of publishing servers.</span></span> <span data-ttu-id="329f2-292">Beispiel: Transaktionen/Sek ist ~ 30, Batchanforderungen ~ 200, und der Benutzer verbindet ~ 6.</span><span class="sxs-lookup"><span data-stu-id="329f2-292">For example: Transactions/sec is ~30, batch requests ~200, and user connects ~6.</span></span>

<span data-ttu-id="329f2-293">Bei Verwendung einer geografisch verteilten Bereitstellung, bei der der Verwaltungsserver & Veröffentlichungsserver ein langsames Verbindungsnetzwerk zwischen Ihnen verwenden, liegt die Antwortzeit für Roundtrips auf den Veröffentlichungsservern innerhalb akzeptabler Zeiträume ( &lt; 5 Sekunden), auch bei gleichzeitigen 100-Anforderungen auf einem einzigen Verwaltungsserver.</span><span class="sxs-lookup"><span data-stu-id="329f2-293">Using a geographically distributed deployment, where the management server & publishing servers utilize a slow link network between them, the round trip response time on the publishing servers is within acceptable time limits (&lt;5 seconds), even for 100 simultaneous requests on a single management server.</span></span>

<table>
<colgroup>
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="329f2-294">Szenario</span><span class="sxs-lookup"><span data-stu-id="329f2-294">Scenario</span></span></th>
<th align="left"><span data-ttu-id="329f2-295">Variante</span><span class="sxs-lookup"><span data-stu-id="329f2-295">Variation</span></span></th>
<th align="left"><span data-ttu-id="329f2-296">Anzahl der Verbindungsgruppen</span><span class="sxs-lookup"><span data-stu-id="329f2-296">Number of connection groups</span></span></th>
<th align="left"><span data-ttu-id="329f2-297">Anzahl der Zugriffsgruppen</span><span class="sxs-lookup"><span data-stu-id="329f2-297">Number of access groups</span></span></th>
<th align="left"><span data-ttu-id="329f2-298">Anzahl der Veröffentlichungsserver</span><span class="sxs-lookup"><span data-stu-id="329f2-298">Number of publishing servers</span></span></th>
<th align="left"><span data-ttu-id="329f2-299">Netzwerkverbindungstyp, Veröffentlichungsserver/Verwaltungsserver</span><span class="sxs-lookup"><span data-stu-id="329f2-299">Network connection type publishing server / management server</span></span></th>
<th align="left"><span data-ttu-id="329f2-300">Roundtrip-Antwortzeit auf dem Veröffentlichungsserver (in Sekunden)</span><span class="sxs-lookup"><span data-stu-id="329f2-300">Round trip response time on the publishing server (in seconds)</span></span></th>
<th align="left"><span data-ttu-id="329f2-301">CPU-Auslastung auf dem Verwaltungsserver</span><span class="sxs-lookup"><span data-stu-id="329f2-301">CPU utilization on management server</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="329f2-302">Netzwerkverbindung zwischen dem Veröffentlichungsserver und dem Verwaltungsserver</span><span class="sxs-lookup"><span data-stu-id="329f2-302">Network connection between the publishing server and management server</span></span></p></td>
<td align="left"><p><span data-ttu-id="329f2-303">1,5 Mbps Slow Link-Netzwerk</span><span class="sxs-lookup"><span data-stu-id="329f2-303">1.5 Mbps Slow link Network</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="329f2-304">0</span><span class="sxs-lookup"><span data-stu-id="329f2-304">0</span></span></p></li>
<li><p><span data-ttu-id="329f2-305">0</span><span class="sxs-lookup"><span data-stu-id="329f2-305">0</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="329f2-306">1</span><span class="sxs-lookup"><span data-stu-id="329f2-306">1</span></span></p></li>
<li><p><span data-ttu-id="329f2-307">1</span><span class="sxs-lookup"><span data-stu-id="329f2-307">1</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="329f2-308">50</span><span class="sxs-lookup"><span data-stu-id="329f2-308">50</span></span></p></li>
<li><p><span data-ttu-id="329f2-309">100</span><span class="sxs-lookup"><span data-stu-id="329f2-309">100</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="329f2-310">1,5 MBit/s Kabel-DSL</span><span class="sxs-lookup"><span data-stu-id="329f2-310">1.5Mbps Cable DSL</span></span></p></li>
<li><p><span data-ttu-id="329f2-311">1,5 MBit/s Kabel-DSL</span><span class="sxs-lookup"><span data-stu-id="329f2-311">1.5Mbps Cable DSL</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="329f2-312">4</span><span class="sxs-lookup"><span data-stu-id="329f2-312">4</span></span></p></li>
<li><p><span data-ttu-id="329f2-313">5</span><span class="sxs-lookup"><span data-stu-id="329f2-313">5</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="329f2-314">1</span><span class="sxs-lookup"><span data-stu-id="329f2-314">1</span></span></p></li>
<li><p><span data-ttu-id="329f2-315">2</span><span class="sxs-lookup"><span data-stu-id="329f2-315">2</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="329f2-316">Netzwerkverbindung zwischen dem Veröffentlichungsserver und dem Verwaltungsserver</span><span class="sxs-lookup"><span data-stu-id="329f2-316">Network connection between the publishing server and management server</span></span></p></td>
<td align="left"><p><span data-ttu-id="329f2-317">LAN/WLAN-Netzwerk</span><span class="sxs-lookup"><span data-stu-id="329f2-317">LAN / WIFI Network</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="329f2-318">0</span><span class="sxs-lookup"><span data-stu-id="329f2-318">0</span></span></p></li>
<li><p><span data-ttu-id="329f2-319">0</span><span class="sxs-lookup"><span data-stu-id="329f2-319">0</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="329f2-320">1</span><span class="sxs-lookup"><span data-stu-id="329f2-320">1</span></span></p></li>
<li><p><span data-ttu-id="329f2-321">1</span><span class="sxs-lookup"><span data-stu-id="329f2-321">1</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="329f2-322">100</span><span class="sxs-lookup"><span data-stu-id="329f2-322">100</span></span></p></li>
<li><p><span data-ttu-id="329f2-323">200</span><span class="sxs-lookup"><span data-stu-id="329f2-323">200</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="329f2-324">WLAN</span><span class="sxs-lookup"><span data-stu-id="329f2-324">Wifi</span></span></p></li>
<li><p><span data-ttu-id="329f2-325">WLAN</span><span class="sxs-lookup"><span data-stu-id="329f2-325">Wifi</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="329f2-326">11</span><span class="sxs-lookup"><span data-stu-id="329f2-326">11</span></span></p></li>
<li><p><span data-ttu-id="329f2-327">20</span><span class="sxs-lookup"><span data-stu-id="329f2-327">20</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="329f2-328">15</span><span class="sxs-lookup"><span data-stu-id="329f2-328">15</span></span></p></li>
<li><p><span data-ttu-id="329f2-329">17</span><span class="sxs-lookup"><span data-stu-id="329f2-329">17</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="329f2-330">Unabhängig davon, ob der Verwaltungsserver und die Veröffentlichungsserver über ein langsames Verbindungsnetzwerk oder ein Hochgeschwindigkeits-Netzwerk verbunden sind, kann der Verwaltungsserver ca. 15.000-Paket Aktualisierungsanforderungen in 30 Minuten verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="329f2-330">Whether the management server and publishing servers are connected over a slow link network, or a high speed network, the management server can handle approximately 15,000 package refresh requests in 30 minutes.</span></span>

## <a href="" id="---------app-v-5-0-reporting-server-capacity-planning-recommendations"></a> <span data-ttu-id="329f2-331">App-V 5,0 Reporting Server-Kapazitäts Planungsempfehlungen</span><span class="sxs-lookup"><span data-stu-id="329f2-331">App-V 5.0 Reporting Server Capacity Planning Recommendations</span></span>


<span data-ttu-id="329f2-332">App-V 5,0-Clients senden Berichtsdaten an den Berichtsserver.</span><span class="sxs-lookup"><span data-stu-id="329f2-332">App-V 5.0 clients send reporting data to the reporting server.</span></span> <span data-ttu-id="329f2-333">Der Berichtsserver zeichnet dann die Informationen in der Microsoft SQL Server-Datenbank auf und gibt eine erfolgreiche Benachrichtigung zurück an den Computer mit dem App-V 5,0-Client.</span><span class="sxs-lookup"><span data-stu-id="329f2-333">The reporting server then records the information in the Microsoft SQL Server database and returns a successful notification back to the computer running App-V 5.0 client.</span></span> <span data-ttu-id="329f2-334">Weitere Informationen zu den unterstützten Konfigurationen von App-v 5,0-Berichtsservern finden Sie unter [unterstützte Konfigurationen für App-v 5,0](app-v-50-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="329f2-334">For more information about App-V 5.0 Reporting Server supported configurations see [App-V 5.0 Supported Configurations](app-v-50-supported-configurations.md).</span></span>

<span data-ttu-id="329f2-335">**Hinweis**  "Roundtrip-Antwortzeit" ist die Zeit, die der Computer ausführt, auf dem der App-V 5,0-Client ausgeführt wird, um die Bericht Erstellungsinformationen an den Berichtsserver zu senden und eine erfolgreiche Benachrichtigung vom Berichtsserver zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="329f2-335">**Note** Round trip response time is the time taken by the computer running the App-V 5.0 client to send the reporting information to the reporting server and receive a successful notification from the reporting server.</span></span>

 

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="329f2-336">Szenario</span><span class="sxs-lookup"><span data-stu-id="329f2-336">Scenario</span></span></th>
<th align="left"><span data-ttu-id="329f2-337">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="329f2-337">Summary</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="329f2-338">Mehrere App-V 5,0-Clients senden Bericht Erstellungsinformationen gleichzeitig an den Berichtsserver.</span><span class="sxs-lookup"><span data-stu-id="329f2-338">Multiple App-V 5.0 clients send reporting information to the reporting server simultaneously.</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="329f2-339">Die Antwortzeit für Roundtrips vom Berichtsserver beträgt 2,6 Sekunden für 500-Clients.</span><span class="sxs-lookup"><span data-stu-id="329f2-339">Round trip response time from the reporting server is 2.6 seconds for 500 clients.</span></span></p></li>
<li><p><span data-ttu-id="329f2-340">Die Antwortzeit für Roundtrips vom Berichtsserver beträgt 5,65 Sekunden für 1000-Clients.</span><span class="sxs-lookup"><span data-stu-id="329f2-340">Round trip response time from the reporting server is 5.65 seconds for 1000 clients.</span></span></p></li>
<li><p><span data-ttu-id="329f2-341">Die Antwortzeit für Roundtrips erhöht sich linear abhängig von der Anzahl der Clients.</span><span class="sxs-lookup"><span data-stu-id="329f2-341">Round trip response time increases linearly depending on number of clients.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="329f2-342">Vom Berichtsserver verarbeitete Anforderungen pro Sekunde.</span><span class="sxs-lookup"><span data-stu-id="329f2-342">Requests per second processed by the reporting server.</span></span></p>
<p></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="329f2-343">Mit einem einzelnen Berichtsserver und einer einzelnen Datenbank können maximal 139-Anforderungen pro Sekunde verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="329f2-343">A single reporting server and a single database, can process a maximum of 139 requests per second.</span></span> <span data-ttu-id="329f2-344">Der Mittelwert ist 121-Anforderungen/Sekunde.</span><span class="sxs-lookup"><span data-stu-id="329f2-344">The average is 121 requests/second.</span></span></p></li>
<li><p><span data-ttu-id="329f2-345">Bei Verwendung von zwei Berichtsservern, die an dieselbe Microsoft SQL Server-Datenbank Bericht erstatten, ähnelt die durchschnittliche Anforderung/Sekunde einem einzelnen Berichtsserver = ~ 127 mit einem max. 278-Anforderungen/Sekunde.</span><span class="sxs-lookup"><span data-stu-id="329f2-345">Using two reporting servers reporting to the same Microsoft SQL Server database, the average requests/second is similar to a single reporting server = ~127, with a max of 278 requests/second.</span></span></p></li>
<li><p><span data-ttu-id="329f2-346">Ein einzelner Berichtsserver kann 500 Concurrent/Active Connections verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="329f2-346">A single reporting server can process 500 concurrent/active connections.</span></span></p></li>
<li><p><span data-ttu-id="329f2-347">Ein einzelner Berichtsserver kann maximal 1500 gleichzeitige Verbindungen verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="329f2-347">A single reporting server can process a maximum 1500 concurrent connections.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="329f2-348">Berichtsdatenbank.</span><span class="sxs-lookup"><span data-stu-id="329f2-348">Reporting Database.</span></span></p>
<p></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="329f2-349">Das Sperren von Konflikten auf dem Computer, auf dem Microsoft SQL Server ausgeführt wird, ist der limitierende Faktor für Anforderungen/Sekunde.</span><span class="sxs-lookup"><span data-stu-id="329f2-349">Lock contention on the computer running Microsoft SQL Server is the limiting factor for requests/second.</span></span></p></li>
<li><p><span data-ttu-id="329f2-350">Durchsatz und Antwortzeit sind unabhängig von der Datenbankgröße.</span><span class="sxs-lookup"><span data-stu-id="329f2-350">Throughput and response time are independent of database size.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="329f2-351">**Berechnen der Zufalls Verzögerung**:</span><span class="sxs-lookup"><span data-stu-id="329f2-351">**Calculating random delay**:</span></span>

<span data-ttu-id="329f2-352">Die zufällige Verzögerung gibt die maximale Verzögerung (in Minuten) für Daten an, die an den Berichtsserver gesendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="329f2-352">The random delay specifies the maximum delay (in minutes) for data to be sent to the reporting server.</span></span> <span data-ttu-id="329f2-353">Wenn der geplante Task gestartet wird, generiert der Client eine zufällige Verzögerung zwischen **0** und **ReportingRandomDelay** und wartet die angegebene Dauer vor dem Senden von Daten.</span><span class="sxs-lookup"><span data-stu-id="329f2-353">When the scheduled task is started, the client generates a random delay between **0** and **ReportingRandomDelay** and will wait the specified duration before sending data.</span></span>

<span data-ttu-id="329f2-354">Zufällige Verzögerung = 4 \ \* Anzahl der Clients/durchschnittliche Anforderungen pro Sekunde.</span><span class="sxs-lookup"><span data-stu-id="329f2-354">Random delay = 4 \* number of clients / average requests per second.</span></span>

<span data-ttu-id="329f2-355">Beispiel: bei 500-Clients mit 120-Anforderungen pro Sekunde beträgt die zufällige Verzögerung 4 \ \* 500/120 = ~ 17 Minuten.</span><span class="sxs-lookup"><span data-stu-id="329f2-355">Example: For 500 clients, with 120 requests per second, the Random delay is, 4 \* 500 / 120 = ~17 minutes.</span></span>

## <a href="" id="---------app-v-5-0-publishing-server-capacity-planning-recommendations"></a> <span data-ttu-id="329f2-356">Empfehlungen für die Kapazitätsplanung von App-V 5,0 Publishing Server</span><span class="sxs-lookup"><span data-stu-id="329f2-356">App-V 5.0 Publishing Server Capacity Planning Recommendations</span></span>


<span data-ttu-id="329f2-357">Computer, auf denen der APP-v 5,0-Client ausgeführt wird, stellen eine Verbindung mit dem App-v 5,0-Veröffentlichungsserver her, um eine Veröffentlichungs Aktualisierungsanforderung zu senden und eine Antwort zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="329f2-357">Computers running the App-V 5.0 client connect to the App-V 5.0 publishing server to send a publishing refresh request and to receive a response.</span></span> <span data-ttu-id="329f2-358">Die Antwortzeit für Roundtrips wird auf dem Computer gemessen, auf dem der App-V 5,0-Client ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="329f2-358">Round trip response time is measured on the computer running the App-V 5.0 client.</span></span> <span data-ttu-id="329f2-359">Die Prozessorzeit wird auf dem Veröffentlichungsserver gemessen.</span><span class="sxs-lookup"><span data-stu-id="329f2-359">Processor time is measured on the publishing server.</span></span> <span data-ttu-id="329f2-360">Weitere Informationen zu den unterstützten Konfigurationen des App-v 5,0-Publishing Servers finden Sie unter [unterstützte Konfigurationen für App-v 5,0](app-v-50-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="329f2-360">For more information about App-V 5.0 Publishing Server supported configurations see [App-V 5.0 Supported Configurations](app-v-50-supported-configurations.md).</span></span>

<span data-ttu-id="329f2-361">**Wichtig**  In der folgenden Liste sind die Hauptfaktoren aufgeführt, die beim Einrichten des App-V 5,0-Publishing Servers zu berücksichtigen sind:</span><span class="sxs-lookup"><span data-stu-id="329f2-361">**Important** The following list displays the main factors to consider when setting up the App-V 5.0 publishing server:</span></span>

-   <span data-ttu-id="329f2-362">Die Anzahl der Clients, die gleichzeitig mit einem einzelnen Veröffentlichungsserver verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="329f2-362">The number of clients connecting simultaneously to a single publishing server.</span></span>

-   <span data-ttu-id="329f2-363">Die Anzahl der Pakete in jeder Aktualisierung.</span><span class="sxs-lookup"><span data-stu-id="329f2-363">The number of packages in each refresh.</span></span>

-   <span data-ttu-id="329f2-364">Die verfügbare Netzwerkbandbreite in Ihrer Umgebung zwischen dem Client und dem App-V 5,0-Veröffentlichungsserver.</span><span class="sxs-lookup"><span data-stu-id="329f2-364">The available network bandwidth in your environment between the client and the App-V 5.0 publishing server.</span></span>

 

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="329f2-365">Szenario</span><span class="sxs-lookup"><span data-stu-id="329f2-365">Scenario</span></span></th>
<th align="left"><span data-ttu-id="329f2-366">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="329f2-366">Summary</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="329f2-367">Mehrere App-V 5,0-Clients stellen gleichzeitig eine Verbindung mit einem einzelnen Veröffentlichungsserver her.</span><span class="sxs-lookup"><span data-stu-id="329f2-367">Multiple App-V 5.0 clients connect to a single publishing server simultaneously.</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="329f2-368">Ein Publishing Server, auf dem Dual-Core-Prozessoren ausgeführt werden, kann auf höchstens 5000-Clients antworten, die eine Aktualisierung gleichzeitig anfordern.</span><span class="sxs-lookup"><span data-stu-id="329f2-368">A publishing server running dual core processors can respond to at most 5000 clients requesting a refresh simultaneously.</span></span></p></li>
<li><p><span data-ttu-id="329f2-369">Für 5000-10000-Clients erfordert der Veröffentlichungsserver mindestens einen Quad-Core.</span><span class="sxs-lookup"><span data-stu-id="329f2-369">For 5000-10000 clients, the publishing server requires a minimum quad core.</span></span></p></li>
<li><p><span data-ttu-id="329f2-370">Für 10000-20000-Clients sollte der Veröffentlichungsserver über zwei Quad-Cores verfügen, um die Antwortzeiten effizienter zu gestalten.</span><span class="sxs-lookup"><span data-stu-id="329f2-370">For 10000-20000 clients, the publishing server should have dual quad cores for more efficient response times.</span></span></p></li>
<li><p><span data-ttu-id="329f2-371">Ein Veröffentlichungsserver mit einem Quad-Core kann innerhalb von 3 Sekunden bis zu 10000-Pakete aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="329f2-371">A publishing server with a quad core can refresh up to 10000 packages within 3 seconds.</span></span> <span data-ttu-id="329f2-372">(Unterstützung von 10000-Clients gleichzeitig)</span><span class="sxs-lookup"><span data-stu-id="329f2-372">(Supporting 10000 simultaneous clients)</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="329f2-373">Die Anzahl der Pakete in jeder Aktualisierung.</span><span class="sxs-lookup"><span data-stu-id="329f2-373">Number of packages in each refresh.</span></span></p>
<p></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="329f2-374">Steigende Anzahl von Paketen erhöht die Antwortzeit um ~ 40% (bis zu 1000-Pakete).</span><span class="sxs-lookup"><span data-stu-id="329f2-374">Increasing number of packages will increase response time by ~40% (up to 1000 packages).</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="329f2-375">Netzwerk zwischen dem App-V 5,0-Client und dem Veröffentlichungsserver.</span><span class="sxs-lookup"><span data-stu-id="329f2-375">Network between the App-V 5.0 client and the publishing server.</span></span></p>
<p></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="329f2-376">In einem langsamen Netzwerk (1,5 Mbps-Bandbreite) gibt es eine Steigerung der Antwortzeit von 97% im Vergleich zu LAN (bis zu 1000 Benutzern).</span><span class="sxs-lookup"><span data-stu-id="329f2-376">Across a slow network (1.5 Mbps bandwidth), there is a 97% increase in response time compared to LAN (up to 1000 users).</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="329f2-377">**Hinweis**  Die CPU-Auslastung des Veröffentlichungsservers ist im Zeitintervall immer sehr groß, wenn Sie gleichzeitige Anforderungen verarbeiten muss ( &gt; in den meisten Fällen 90%).</span><span class="sxs-lookup"><span data-stu-id="329f2-377">**Note** The publishing server CPU usage is always high during the time interval when it has to process simultaneous requests (&gt;90% in most cases).</span></span> <span data-ttu-id="329f2-378">Der Veröffentlichungsserver kann in einer Sekunde 1500-Clientanforderungen verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="329f2-378">The publishing server can handle ~1500 client requests in 1 second.</span></span>

 

<table>
<colgroup>
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="329f2-379">Szenario</span><span class="sxs-lookup"><span data-stu-id="329f2-379">Scenario</span></span></th>
<th align="left"><span data-ttu-id="329f2-380">Variante</span><span class="sxs-lookup"><span data-stu-id="329f2-380">Variation</span></span></th>
<th align="left"><span data-ttu-id="329f2-381">Anzahl der App-V 5,0-Clients</span><span class="sxs-lookup"><span data-stu-id="329f2-381">Number of App-V 5.0 clients</span></span></th>
<th align="left"><span data-ttu-id="329f2-382">Anzahl der Pakete</span><span class="sxs-lookup"><span data-stu-id="329f2-382">Number of packages</span></span></th>
<th align="left"><span data-ttu-id="329f2-383">Prozessorkonfiguration auf dem Veröffentlichungsserver</span><span class="sxs-lookup"><span data-stu-id="329f2-383">Processor configuration on the publishing server</span></span></th>
<th align="left"><span data-ttu-id="329f2-384">Netzwerkverbindungstyp, Veröffentlichungsserver/App-V 5,0-Client</span><span class="sxs-lookup"><span data-stu-id="329f2-384">Network connection type publishing server / App-V 5.0 client</span></span></th>
<th align="left"><span data-ttu-id="329f2-385">Roundtrip-Zeit auf dem App-V 5,0-Client (in Sekunden)</span><span class="sxs-lookup"><span data-stu-id="329f2-385">Round trip time on the App-V 5.0 client (in seconds)</span></span></th>
<th align="left"><span data-ttu-id="329f2-386">CPU-Auslastung auf dem Veröffentlichungsserver (in%)</span><span class="sxs-lookup"><span data-stu-id="329f2-386">CPU utilization on publishing server (in %)</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="329f2-387">App-V 5,0-Client sendet Antwort auf Veröffentlichungs Aktualisierungsanforderung &amp; , jede Anforderung, die 120-Pakete enthält</span><span class="sxs-lookup"><span data-stu-id="329f2-387">App-V 5.0 client sends publishing refresh request &amp; receives response, each request containing 120 packages</span></span></p></td>
<td align="left"><p><span data-ttu-id="329f2-388">Anzahl der Clients</span><span class="sxs-lookup"><span data-stu-id="329f2-388">Number of clients</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="329f2-389">100</span><span class="sxs-lookup"><span data-stu-id="329f2-389">100</span></span></p></li>
<li><p><span data-ttu-id="329f2-390">1000</span><span class="sxs-lookup"><span data-stu-id="329f2-390">1000</span></span></p></li>
<li><p><span data-ttu-id="329f2-391">5000</span><span class="sxs-lookup"><span data-stu-id="329f2-391">5000</span></span></p></li>
<li><p><span data-ttu-id="329f2-392">10000</span><span class="sxs-lookup"><span data-stu-id="329f2-392">10000</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="329f2-393">120</span><span class="sxs-lookup"><span data-stu-id="329f2-393">120</span></span></p></li>
<li><p><span data-ttu-id="329f2-394">120</span><span class="sxs-lookup"><span data-stu-id="329f2-394">120</span></span></p></li>
<li><p><span data-ttu-id="329f2-395">120</span><span class="sxs-lookup"><span data-stu-id="329f2-395">120</span></span></p></li>
<li><p><span data-ttu-id="329f2-396">120</span><span class="sxs-lookup"><span data-stu-id="329f2-396">120</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="329f2-397">Dual-Core</span><span class="sxs-lookup"><span data-stu-id="329f2-397">Dual Core</span></span></p></li>
<li><p><span data-ttu-id="329f2-398">Dual-Core</span><span class="sxs-lookup"><span data-stu-id="329f2-398">Dual Core</span></span></p></li>
<li><p><span data-ttu-id="329f2-399">Quad-Core</span><span class="sxs-lookup"><span data-stu-id="329f2-399">Quad Core</span></span></p></li>
<li><p><span data-ttu-id="329f2-400">Quad-Core</span><span class="sxs-lookup"><span data-stu-id="329f2-400">Quad Core</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="329f2-401">LAN</span><span class="sxs-lookup"><span data-stu-id="329f2-401">LAN</span></span></p></li>
<li><p><span data-ttu-id="329f2-402">LAN</span><span class="sxs-lookup"><span data-stu-id="329f2-402">LAN</span></span></p></li>
<li><p><span data-ttu-id="329f2-403">LAN</span><span class="sxs-lookup"><span data-stu-id="329f2-403">LAN</span></span></p></li>
<li><p><span data-ttu-id="329f2-404">LAN</span><span class="sxs-lookup"><span data-stu-id="329f2-404">LAN</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="329f2-405">1</span><span class="sxs-lookup"><span data-stu-id="329f2-405">1</span></span></p></li>
<li><p><span data-ttu-id="329f2-406">2</span><span class="sxs-lookup"><span data-stu-id="329f2-406">2</span></span></p></li>
<li><p><span data-ttu-id="329f2-407">2</span><span class="sxs-lookup"><span data-stu-id="329f2-407">2</span></span></p></li>
<li><p><span data-ttu-id="329f2-408">3</span><span class="sxs-lookup"><span data-stu-id="329f2-408">3</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="329f2-409">100</span><span class="sxs-lookup"><span data-stu-id="329f2-409">100</span></span></p></li>
<li><p><span data-ttu-id="329f2-410">99</span><span class="sxs-lookup"><span data-stu-id="329f2-410">99</span></span></p></li>
<li><p><span data-ttu-id="329f2-411">89</span><span class="sxs-lookup"><span data-stu-id="329f2-411">89</span></span></p></li>
<li><p><span data-ttu-id="329f2-412">77</span><span class="sxs-lookup"><span data-stu-id="329f2-412">77</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="329f2-413">Mehrere Pakete in jeder Aktualisierung</span><span class="sxs-lookup"><span data-stu-id="329f2-413">Multiple packages in each refresh</span></span></p></td>
<td align="left"><p><span data-ttu-id="329f2-414">Anzahl der Pakete</span><span class="sxs-lookup"><span data-stu-id="329f2-414">Number of packages</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="329f2-415">1000</span><span class="sxs-lookup"><span data-stu-id="329f2-415">1000</span></span></p></li>
<li><p><span data-ttu-id="329f2-416">1000</span><span class="sxs-lookup"><span data-stu-id="329f2-416">1000</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="329f2-417">500</span><span class="sxs-lookup"><span data-stu-id="329f2-417">500</span></span></p></li>
<li><p><span data-ttu-id="329f2-418">1000</span><span class="sxs-lookup"><span data-stu-id="329f2-418">1000</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="329f2-419">Quad-Core</span><span class="sxs-lookup"><span data-stu-id="329f2-419">Quad Core</span></span></p></li>
<li><p><span data-ttu-id="329f2-420">Quad-Core</span><span class="sxs-lookup"><span data-stu-id="329f2-420">Quad Core</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="329f2-421">LAN</span><span class="sxs-lookup"><span data-stu-id="329f2-421">LAN</span></span></p></li>
<li><p><span data-ttu-id="329f2-422">LAN</span><span class="sxs-lookup"><span data-stu-id="329f2-422">LAN</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="329f2-423">2</span><span class="sxs-lookup"><span data-stu-id="329f2-423">2</span></span></p></li>
<li><p><span data-ttu-id="329f2-424">3</span><span class="sxs-lookup"><span data-stu-id="329f2-424">3</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="329f2-425">92</span><span class="sxs-lookup"><span data-stu-id="329f2-425">92</span></span></p></li>
<li><p><span data-ttu-id="329f2-426">91</span><span class="sxs-lookup"><span data-stu-id="329f2-426">91</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="329f2-427">Netzwerk zwischen Client und Veröffentlichungsserver</span><span class="sxs-lookup"><span data-stu-id="329f2-427">Network between client and publishing server</span></span></p></td>
<td align="left"><p><span data-ttu-id="329f2-428">1,5 Mbps Slow Link-Netzwerk</span><span class="sxs-lookup"><span data-stu-id="329f2-428">1.5 Mbps Slow link network</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="329f2-429">100</span><span class="sxs-lookup"><span data-stu-id="329f2-429">100</span></span></p></li>
<li><p><span data-ttu-id="329f2-430">500</span><span class="sxs-lookup"><span data-stu-id="329f2-430">500</span></span></p></li>
<li><p><span data-ttu-id="329f2-431">1000</span><span class="sxs-lookup"><span data-stu-id="329f2-431">1000</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="329f2-432">120</span><span class="sxs-lookup"><span data-stu-id="329f2-432">120</span></span></p></li>
<li><p><span data-ttu-id="329f2-433">120</span><span class="sxs-lookup"><span data-stu-id="329f2-433">120</span></span></p></li>
<li><p><span data-ttu-id="329f2-434">120</span><span class="sxs-lookup"><span data-stu-id="329f2-434">120</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="329f2-435">Quad-Core</span><span class="sxs-lookup"><span data-stu-id="329f2-435">Quad Core</span></span></p></li>
<li><p><span data-ttu-id="329f2-436">Quad-Core</span><span class="sxs-lookup"><span data-stu-id="329f2-436">Quad Core</span></span></p></li>
<li><p><span data-ttu-id="329f2-437">Quad-Core</span><span class="sxs-lookup"><span data-stu-id="329f2-437">Quad Core</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="329f2-438">1,5 Mbps Intra-Continental-Netzwerk</span><span class="sxs-lookup"><span data-stu-id="329f2-438">1.5 Mbps Intra-Continental Network</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="329f2-439">3</span><span class="sxs-lookup"><span data-stu-id="329f2-439">3</span></span></p></li>
<li><p><span data-ttu-id="329f2-440">10 (mit 0,2% Ausfallrate)</span><span class="sxs-lookup"><span data-stu-id="329f2-440">10 (with 0.2% failure rate)</span></span></p></li>
<li><p><span data-ttu-id="329f2-441">17 (mit einer Ausfallrate von 1%)</span><span class="sxs-lookup"><span data-stu-id="329f2-441">17 (with 1% failure rate)</span></span></p></li>
</ul></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="---------app-v-5-0-streaming-capacity-planning-recommendations"></a> <span data-ttu-id="329f2-442">Empfehlungen für App-V 5,0-Streaming-Kapazitätsplanung</span><span class="sxs-lookup"><span data-stu-id="329f2-442">App-V 5.0 Streaming Capacity Planning Recommendations</span></span>


<span data-ttu-id="329f2-443">Auf Computern, auf denen der App-V 5,0-Client ausgeführt wird, wird das virtuelle Anwendungspaket vom Streamingserver gestreamt.</span><span class="sxs-lookup"><span data-stu-id="329f2-443">Computers running the App-V 5.0 client stream the virtual application package from the streaming server.</span></span> <span data-ttu-id="329f2-444">Die Antwortzeit für Roundtrips wird auf dem Computer gemessen, auf dem der App-V 5,0-Client ausgeführt wird, und es wird die Zeit zum Streamen des gesamten Pakets übernommen.</span><span class="sxs-lookup"><span data-stu-id="329f2-444">Round trip response time is measured on the computer running the App-V 5.0 client, and is the time taken to stream the entire package.</span></span>

<span data-ttu-id="329f2-445">**Wichtig**  In der folgenden Liste sind die Hauptfaktoren aufgeführt, die beim Einrichten des App-V 5,0-Streaming Servers zu berücksichtigen sind:</span><span class="sxs-lookup"><span data-stu-id="329f2-445">**Important** The following list identifies the main factors to consider when setting up the App-V 5.0 streaming server:</span></span>

-   <span data-ttu-id="329f2-446">Die Anzahl der Clients, die Anwendungspakete gleichzeitig von einem einzelnen Streamingserver streamen.</span><span class="sxs-lookup"><span data-stu-id="329f2-446">The number of clients streaming application packages simultaneously from a single streaming server.</span></span>

-   <span data-ttu-id="329f2-447">Die Größe des zu streamenden Pakets.</span><span class="sxs-lookup"><span data-stu-id="329f2-447">The size of the package being streamed.</span></span>

-   <span data-ttu-id="329f2-448">Die verfügbare Netzwerkbandbreite in Ihrer Umgebung zwischen dem Client und dem Streamingserver.</span><span class="sxs-lookup"><span data-stu-id="329f2-448">The available network bandwidth in your environment between the client and the streaming server.</span></span>

 

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="329f2-449">Szenario</span><span class="sxs-lookup"><span data-stu-id="329f2-449">Scenario</span></span></th>
<th align="left"><span data-ttu-id="329f2-450">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="329f2-450">Summary</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="329f2-451">Mehrere App-V 5,0-Clients streamen Anwendungen gleichzeitig von einem einzelnen Streamingserver.</span><span class="sxs-lookup"><span data-stu-id="329f2-451">Multiple App-V 5.0 clients stream applications from a single streaming server simultaneously.</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="329f2-452">Wenn die Anzahl der Clients, die gleichzeitig vom gleichen Server gestreamt werden, zunimmt, gibt es eine lineare Beziehung mit der Download/Streaming-Zeit des Pakets.</span><span class="sxs-lookup"><span data-stu-id="329f2-452">If the number of clients simultaneously streaming from the same server increases, there is a linear relationship with the package download/streaming time.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="329f2-453">Die Größe des zu streamenden Pakets.</span><span class="sxs-lookup"><span data-stu-id="329f2-453">Size of the package being streamed.</span></span></p>
<p></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="329f2-454">Die Größe des Pakets hat erhebliche Auswirkungen auf die Streaming/Download-Zeit nur für größere Pakete mit einer Größe von ~ 1GB.</span><span class="sxs-lookup"><span data-stu-id="329f2-454">The package size has a significant impact on the streaming/download time only for larger packages with a size ~ 1GB.</span></span> <span data-ttu-id="329f2-455">Bei Paketgrößen von 3 MB bis 100 MB beträgt die streamingzeit zwischen 20 Sekunden und 100 Sekunden, mit 100 gleichzeitigen Clients.</span><span class="sxs-lookup"><span data-stu-id="329f2-455">For package sizes ranging from 3 MB to 100 MB, the streaming time ranges from 20 seconds to 100 seconds, with 100 simultaneous clients.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="329f2-456">Netzwerk zwischen dem App-V 5,0-Client und dem Streaming-Server.</span><span class="sxs-lookup"><span data-stu-id="329f2-456">Network between the App-V 5.0 client and the streaming server.</span></span></p>
<p></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="329f2-457">In einem langsamen Netzwerk (1,5 Mbps-Bandbreite) gibt es eine Steigerung der Antwortzeit von 70-80% im Vergleich zu LAN (bis zu 100 Benutzern).</span><span class="sxs-lookup"><span data-stu-id="329f2-457">Across a slow network (1.5 Mbps bandwidth), there is a 70-80% increase in response time compared to LAN (up to 100 users).</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="329f2-458">In der folgenden Tabelle werden die Beispielwerte für die einzelnen Faktoren in der vorherigen Liste angezeigt:</span><span class="sxs-lookup"><span data-stu-id="329f2-458">The following table displays sample values for each of the factors in the previous list:</span></span>

<table style="width:100%;">
<colgroup>
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="329f2-459">Szenario</span><span class="sxs-lookup"><span data-stu-id="329f2-459">Scenario</span></span></th>
<th align="left"><span data-ttu-id="329f2-460">Variante</span><span class="sxs-lookup"><span data-stu-id="329f2-460">Variation</span></span></th>
<th align="left"><span data-ttu-id="329f2-461">Anzahl der App-V 5,0-Clients</span><span class="sxs-lookup"><span data-stu-id="329f2-461">Number of App-V 5.0 clients</span></span></th>
<th align="left"><span data-ttu-id="329f2-462">Größe der einzelnen Pakete</span><span class="sxs-lookup"><span data-stu-id="329f2-462">Size of each package</span></span></th>
<th align="left"><span data-ttu-id="329f2-463">Netzwerkverbindungstyp Streaming Server/App-V 5,0 Client</span><span class="sxs-lookup"><span data-stu-id="329f2-463">Network connection type streaming server / App-V 5.0 client</span></span></th>
<th align="left"><span data-ttu-id="329f2-464">Roundtrip-Zeit auf dem App-V 5,0-Client (in Sekunden)</span><span class="sxs-lookup"><span data-stu-id="329f2-464">Round trip time on the App-V 5.0 client (in seconds)</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="329f2-465">Mehrere App-V 5,0-Clients, die virtuelle Anwendungspakete von einem Streamingserver streamen.</span><span class="sxs-lookup"><span data-stu-id="329f2-465">Multiple App-V 5.0 clients streaming virtual application packages from a streaming server.</span></span></p></td>
<td align="left"><p><span data-ttu-id="329f2-466">Die Anzahl der Clients.</span><span class="sxs-lookup"><span data-stu-id="329f2-466">Number of clients.</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="329f2-467">100</span><span class="sxs-lookup"><span data-stu-id="329f2-467">100</span></span></p></li>
<li><p><span data-ttu-id="329f2-468">200</span><span class="sxs-lookup"><span data-stu-id="329f2-468">200</span></span></p></li>
<li><p><span data-ttu-id="329f2-469">1000</span><span class="sxs-lookup"><span data-stu-id="329f2-469">1000</span></span></p></li>
<li><p></p></li>
<li><p><span data-ttu-id="329f2-470">100</span><span class="sxs-lookup"><span data-stu-id="329f2-470">100</span></span></p></li>
<li><p><span data-ttu-id="329f2-471">200</span><span class="sxs-lookup"><span data-stu-id="329f2-471">200</span></span></p></li>
<li><p><span data-ttu-id="329f2-472">1000</span><span class="sxs-lookup"><span data-stu-id="329f2-472">1000</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="329f2-473">3,5 MB</span><span class="sxs-lookup"><span data-stu-id="329f2-473">3.5 MB</span></span></p></li>
<li><p><span data-ttu-id="329f2-474">3,5 MB</span><span class="sxs-lookup"><span data-stu-id="329f2-474">3.5 MB</span></span></p></li>
<li><p><span data-ttu-id="329f2-475">3,5 MB</span><span class="sxs-lookup"><span data-stu-id="329f2-475">3.5 MB</span></span></p></li>
<li><p></p></li>
<li><p><span data-ttu-id="329f2-476">5 MB</span><span class="sxs-lookup"><span data-stu-id="329f2-476">5 MB</span></span></p></li>
<li><p><span data-ttu-id="329f2-477">5 MB</span><span class="sxs-lookup"><span data-stu-id="329f2-477">5 MB</span></span></p></li>
<li><p><span data-ttu-id="329f2-478">5 MB</span><span class="sxs-lookup"><span data-stu-id="329f2-478">5 MB</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="329f2-479">LAN</span><span class="sxs-lookup"><span data-stu-id="329f2-479">LAN</span></span></p></li>
<li><p><span data-ttu-id="329f2-480">LAN</span><span class="sxs-lookup"><span data-stu-id="329f2-480">LAN</span></span></p></li>
<li><p><span data-ttu-id="329f2-481">LAN</span><span class="sxs-lookup"><span data-stu-id="329f2-481">LAN</span></span></p></li>
<li><p></p></li>
<li><p><span data-ttu-id="329f2-482">LAN</span><span class="sxs-lookup"><span data-stu-id="329f2-482">LAN</span></span></p></li>
<li><p><span data-ttu-id="329f2-483">LAN</span><span class="sxs-lookup"><span data-stu-id="329f2-483">LAN</span></span></p></li>
<li><p><span data-ttu-id="329f2-484">LAN</span><span class="sxs-lookup"><span data-stu-id="329f2-484">LAN</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="329f2-485">29</span><span class="sxs-lookup"><span data-stu-id="329f2-485">29</span></span></p></li>
<li><p><span data-ttu-id="329f2-486">39</span><span class="sxs-lookup"><span data-stu-id="329f2-486">39</span></span></p></li>
<li><p><span data-ttu-id="329f2-487">391</span><span class="sxs-lookup"><span data-stu-id="329f2-487">391</span></span></p></li>
<li><p></p></li>
<li><p><span data-ttu-id="329f2-488">35</span><span class="sxs-lookup"><span data-stu-id="329f2-488">35</span></span></p></li>
<li><p><span data-ttu-id="329f2-489">68</span><span class="sxs-lookup"><span data-stu-id="329f2-489">68</span></span></p></li>
<li><p><span data-ttu-id="329f2-490">461</span><span class="sxs-lookup"><span data-stu-id="329f2-490">461</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="329f2-491">Die Größe der einzelnen Pakete, die gestreamt werden.</span><span class="sxs-lookup"><span data-stu-id="329f2-491">Size of each package being streamed.</span></span></p></td>
<td align="left"><p><span data-ttu-id="329f2-492">Die Größe jedes Pakets.</span><span class="sxs-lookup"><span data-stu-id="329f2-492">Size of each package.</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="329f2-493">100</span><span class="sxs-lookup"><span data-stu-id="329f2-493">100</span></span></p></li>
<li><p><span data-ttu-id="329f2-494">200</span><span class="sxs-lookup"><span data-stu-id="329f2-494">200</span></span></p></li>
<li><p></p></li>
<li><p><span data-ttu-id="329f2-495">100</span><span class="sxs-lookup"><span data-stu-id="329f2-495">100</span></span></p></li>
<li><p><span data-ttu-id="329f2-496">200</span><span class="sxs-lookup"><span data-stu-id="329f2-496">200</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="329f2-497">21 MB</span><span class="sxs-lookup"><span data-stu-id="329f2-497">21 MB</span></span></p></li>
<li><p><span data-ttu-id="329f2-498">21 MB</span><span class="sxs-lookup"><span data-stu-id="329f2-498">21 MB</span></span></p></li>
<li><p></p></li>
<li><p><span data-ttu-id="329f2-499">109</span><span class="sxs-lookup"><span data-stu-id="329f2-499">109</span></span></p></li>
<li><p><span data-ttu-id="329f2-500">109</span><span class="sxs-lookup"><span data-stu-id="329f2-500">109</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="329f2-501">LAN</span><span class="sxs-lookup"><span data-stu-id="329f2-501">LAN</span></span></p></li>
<li><p><span data-ttu-id="329f2-502">LAN</span><span class="sxs-lookup"><span data-stu-id="329f2-502">LAN</span></span></p></li>
<li><p></p></li>
<li><p><span data-ttu-id="329f2-503">LAN</span><span class="sxs-lookup"><span data-stu-id="329f2-503">LAN</span></span></p></li>
<li><p><span data-ttu-id="329f2-504">LAN</span><span class="sxs-lookup"><span data-stu-id="329f2-504">LAN</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<p><span data-ttu-id="329f2-505">33</span><span class="sxs-lookup"><span data-stu-id="329f2-505">33</span></span></p>
<p><span data-ttu-id="329f2-506">83</span><span class="sxs-lookup"><span data-stu-id="329f2-506">83</span></span></p>
<p></p>
<p><span data-ttu-id="329f2-507">100</span><span class="sxs-lookup"><span data-stu-id="329f2-507">100</span></span></p>
<p><span data-ttu-id="329f2-508">160</span><span class="sxs-lookup"><span data-stu-id="329f2-508">160</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="329f2-509">Netzwerkverbindung zwischen Client und App-V 5,0 Streaming Server.</span><span class="sxs-lookup"><span data-stu-id="329f2-509">Network connection between client and App-V 5.0 streaming server.</span></span></p></td>
<td align="left"><p><span data-ttu-id="329f2-510">1,5 Mbps Slow Link-Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="329f2-510">1.5 Mbps Slow link network.</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="329f2-511">100</span><span class="sxs-lookup"><span data-stu-id="329f2-511">100</span></span></p></li>
<li><p></p></li>
<li><p><span data-ttu-id="329f2-512">100</span><span class="sxs-lookup"><span data-stu-id="329f2-512">100</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="329f2-513">3,5 MB</span><span class="sxs-lookup"><span data-stu-id="329f2-513">3.5 MB</span></span></p></li>
<li><p></p></li>
<li><p><span data-ttu-id="329f2-514">5 MB</span><span class="sxs-lookup"><span data-stu-id="329f2-514">5 MB</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="329f2-515">1,5 Mbps Intra-Continental-Netzwerk</span><span class="sxs-lookup"><span data-stu-id="329f2-515">1.5 Mbps Intra-Continental Network</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<p><span data-ttu-id="329f2-516">102</span><span class="sxs-lookup"><span data-stu-id="329f2-516">102</span></span></p>
<p></p>
<p><span data-ttu-id="329f2-517">121</span><span class="sxs-lookup"><span data-stu-id="329f2-517">121</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="329f2-518">Jeder App-V 5,0-Streamingserver sollte in der Lage sein, ein minimales 200-Client-Streaming mit virtualisierten Anwendungen gleichzeitig zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="329f2-518">Each App-V 5.0 streaming server should be able to handle a minimum of 200 clients concurrently streaming virtualized applications.</span></span>

<span data-ttu-id="329f2-519">**Hinweis**  Die tatsächliche Zeit für den Datenstrom wird in erster Linie durch die Anzahl der gleichzeitigen Streaming-Clients, die Anzahl der Pakete, die Paketgröße, die Netzwerkaktivität des Servers und die Netzwerkbedingungen bestimmt.</span><span class="sxs-lookup"><span data-stu-id="329f2-519">**Note** The actual time to it will take to stream is determined primarily by the number of clients streaming simultaneously, number of packages, package size, the server’s network activity, and network conditions.</span></span>

 

<span data-ttu-id="329f2-520">Beispielsweise kann ein durchschnittlicher Benutzer ein 100-MB-Paket in weniger als zwei Minuten streamen, wenn 100 gleichzeitige Clients vom Server gestreamt werden.</span><span class="sxs-lookup"><span data-stu-id="329f2-520">For example, an average user can stream a 100 MB package in less than 2 minutes, when 100 simultaneous clients are streaming from the server.</span></span> <span data-ttu-id="329f2-521">Ein Paket mit einer Größe von 1 GB kann jedoch bis zu 30 Minuten dauern.</span><span class="sxs-lookup"><span data-stu-id="329f2-521">However, a package of size 1 GB could take up to 30 minutes.</span></span> <span data-ttu-id="329f2-522">In den meisten realen Umgebungen, in denen die Streaming-Nachfrage nicht gleichmäßig verteilt ist, müssen Sie die ungefähren Peak-Streaming-Anforderungen verstehen, die in Ihrer Umgebung vorhanden sind, um die Anzahl der erforderlichen Streamingserver richtig zu ändern.</span><span class="sxs-lookup"><span data-stu-id="329f2-522">In most real world environments streaming demand is not uniformly distributed, you will need to understand the approximate peak streaming requirements present in your environment in order to properly size the number of required streaming servers.</span></span>

<span data-ttu-id="329f2-523">Die Anzahl der Clients, die ein Streamingserver unterstützenkann, kann erheblich erhöht werden, und die Spitzen-Streaming-Anforderungen werden verringert, wenn Sie Ihre Anwendungen Vorabzwischenspeichern.</span><span class="sxs-lookup"><span data-stu-id="329f2-523">The number of clients a streaming server can support can be significantly increased and the peak streaming requirements reduced if you pre-cache your applications.</span></span> <span data-ttu-id="329f2-524">Sie können auch die Anzahl der Clients erhöhen, die ein Streamingserver unterstützt, indem Sie on-Demand-Streaming-Übermittlung und Datenstrom optimierte Pakete verwenden.</span><span class="sxs-lookup"><span data-stu-id="329f2-524">You can also increase the number of clients a streaming server can support by using on-demand streaming delivery and stream optimized packages.</span></span>

## <span data-ttu-id="329f2-525">Kombinieren von App-V 5,0-Server Rollen</span><span class="sxs-lookup"><span data-stu-id="329f2-525">Combining App-V 5.0 Server Roles</span></span>


<span data-ttu-id="329f2-526">Diskontierung von Skalierungs-und Fehlertoleranzanforderungen: die Mindestanzahl von Servern, die für einen Standort mit Active Directory-Konnektivität benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="329f2-526">Discounting scaling and fault-tolerance requirements, the minimum number of servers needed for a location with connectivity to Active Directory is one.</span></span> <span data-ttu-id="329f2-527">Dieser Server hostet den Verwaltungsserver, den Verwaltungsserverdienst und die Microsoft SQL Server-Rollen.</span><span class="sxs-lookup"><span data-stu-id="329f2-527">This server will host the management server, management server service, and Microsoft SQL Server roles.</span></span> <span data-ttu-id="329f2-528">Server Rollen können daher in jeder gewünschten Kombination angeordnet werden, da Sie nicht miteinander in Konflikt stehen.</span><span class="sxs-lookup"><span data-stu-id="329f2-528">Server roles, therefore, can be arranged in any desired combination since they do not conflict with one another.</span></span>

<span data-ttu-id="329f2-529">Wenn Sie die Skalierungsanforderungen ignorieren, beträgt die Mindestanzahl von Servern, die für die Bereitstellung einer fehlertoleranten Implementierung erforderlich sind, vier.</span><span class="sxs-lookup"><span data-stu-id="329f2-529">Ignoring scaling requirements, the minimum number of servers necessary to provide a fault-tolerant implementation is four.</span></span> <span data-ttu-id="329f2-530">Der Verwaltungsserver und die Microsoft SQL Server-Rollen unterstützen die Platzierung in fehlertoleranten Konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="329f2-530">The management server, and Microsoft SQL Server roles support being placed in fault-tolerant configurations.</span></span> <span data-ttu-id="329f2-531">Der Verwaltungsserverdienst kann mit jeder der Rollen kombiniert werden, bleibt aber ein einzelner Fehlerpunkt.</span><span class="sxs-lookup"><span data-stu-id="329f2-531">The management server service can be combined with any of the roles, but remains a single point of failure.</span></span>

<span data-ttu-id="329f2-532">Obwohl eine Reihe von Strategien und Technologien zur Fehlertoleranz verfügbar sind, gelten nicht alle für einen bestimmten Dienst.</span><span class="sxs-lookup"><span data-stu-id="329f2-532">Although there are a number of fault-tolerance strategies and technologies available, not all are applicable to a given service.</span></span> <span data-ttu-id="329f2-533">Wenn App-V 5,0-Rollen kombiniert werden, gelten möglicherweise bestimmte Fehlertoleranzoptionen aufgrund von Inkompatibilitäten nicht mehr.</span><span class="sxs-lookup"><span data-stu-id="329f2-533">Additionally, if App-V 5.0 roles are combined, certain fault-tolerance options may no longer apply due to incompatibilities.</span></span>






## <span data-ttu-id="329f2-534">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="329f2-534">Related topics</span></span>


[<span data-ttu-id="329f2-535">Unterstützte App-V 5.0-Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="329f2-535">App-V 5.0 Supported Configurations</span></span>](app-v-50-supported-configurations.md)

[<span data-ttu-id="329f2-536">Planen für hohe Verfügbarkeit mit App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="329f2-536">Planning for High Availability with App-V 5.0</span></span>](planning-for-high-availability-with-app-v-50.md)

[<span data-ttu-id="329f2-537">Planen der Bereitstellung von App-V</span><span class="sxs-lookup"><span data-stu-id="329f2-537">Planning to Deploy App-V</span></span>](planning-to-deploy-app-v.md)

 

 





