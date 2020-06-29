---
title: Übersicht über die Application Virtualization-Systemkomponenten
description: Übersicht über die Application Virtualization-Systemkomponenten
author: dansimp
ms.assetid: 75d88ef7-44d8-4fa7-b7f5-9153f37e570d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: cab0065b9966094da687cce2f5e94069922189fc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806552"
---
# <span data-ttu-id="ed8ac-103">Übersicht über die Application Virtualization-Systemkomponenten</span><span class="sxs-lookup"><span data-stu-id="ed8ac-103">Overview of the Application Virtualization System Components</span></span>


<span data-ttu-id="ed8ac-104">In der folgenden Tabelle werden die primären Komponenten des Microsoft Application Virtualization-Verwaltungssystems beschrieben.</span><span class="sxs-lookup"><span data-stu-id="ed8ac-104">The following table describes the primary components of the Microsoft Application Virtualization Management System.</span></span> <span data-ttu-id="ed8ac-105">Weitere Informationen zum Bereitstellen dieser Systemkomponenten finden Sie unter [Server basiertes Application Virtualization-Szenario](application-virtualization-server-based-scenario.md).</span><span class="sxs-lookup"><span data-stu-id="ed8ac-105">For more information about deploying these system components, see [Application Virtualization Server-Based Scenario](application-virtualization-server-based-scenario.md).</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ed8ac-106">Komponente</span><span class="sxs-lookup"><span data-stu-id="ed8ac-106">Component</span></span></th>
<th align="left"><span data-ttu-id="ed8ac-107">Funktion</span><span class="sxs-lookup"><span data-stu-id="ed8ac-107">Function</span></span></th>
<th align="left"><span data-ttu-id="ed8ac-108">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="ed8ac-108">Additional Information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ed8ac-109">Microsoft Application Virtualization-Verwaltungs Server</span><span class="sxs-lookup"><span data-stu-id="ed8ac-109">Microsoft Application Virtualization Management Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="ed8ac-110">Die Komponente, die für das Streaming des Paketinhalts und die Veröffentlichung der Verknüpfungen und Dateitypzuordnungen zum Application Virtualization Client verantwortlich ist.</span><span class="sxs-lookup"><span data-stu-id="ed8ac-110">The component responsible for streaming the package content and publishing the shortcuts and file type associations to the Application Virtualization Client.</span></span></p></td>
<td align="left"><p><span data-ttu-id="ed8ac-111">Der Application Virtualization-Verwaltungs Server unterstützt das aktive Upgrade, die Lizenzverwaltung und eine Datenbank, die für die Berichterstellung verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="ed8ac-111">The Application Virtualization Management Server supports active upgrade, License Management, and a database that can be used for reporting.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="ed8ac-112">Inhalts </strong> Ordner</span><span class="sxs-lookup"><span data-stu-id="ed8ac-112">Content</strong> folder</span></span></p></td>
<td align="left"><p><span data-ttu-id="ed8ac-113">Der Speicherort der Application Virtualization-Pakete für Streaming.</span><span class="sxs-lookup"><span data-stu-id="ed8ac-113">The location of the Application Virtualization packages for streaming.</span></span></p></td>
<td align="left"><p><span data-ttu-id="ed8ac-114">Dieser Ordner kann sich auf einer Freigabe auf dem Application Virtualization-Verwaltungs Server befinden.</span><span class="sxs-lookup"><span data-stu-id="ed8ac-114">This folder can be located on a share on or off the Application Virtualization Management Server.</span></span> <span data-ttu-id="ed8ac-115">Der Ordner kann sich auch in einem SAN (Storage Area Network) befinden.</span><span class="sxs-lookup"><span data-stu-id="ed8ac-115">The folder can also be located on a Storage Area Network (SAN).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ed8ac-116">Microsoft Application Virtualization-Verwaltungskonsole</span><span class="sxs-lookup"><span data-stu-id="ed8ac-116">Microsoft Application Virtualization Management Console</span></span></p></td>
<td align="left"><p><span data-ttu-id="ed8ac-117">Ein MMC 3,0-Snap-in-Verwaltungsdienstprogramm für die Microsoft Application Virtualization Server-Verwaltung.</span><span class="sxs-lookup"><span data-stu-id="ed8ac-117">An MMC 3.0 snap-in management utility for Microsoft Application Virtualization Server administration.</span></span></p></td>
<td align="left"><p><span data-ttu-id="ed8ac-118">Diese Komponente kann auf dem Microsoft Application Virtualization Server oder auf einer separaten Workstation mit MMC 3.0 und installiert werden. NET 2.0 installiert ist.</span><span class="sxs-lookup"><span data-stu-id="ed8ac-118">This component can be installed on the Microsoft Application Virtualization server or located on a separate workstation that has MMC3.0 and .NET2.0 installed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ed8ac-119">Microsoft Application Virtualization Management Web Service</span><span class="sxs-lookup"><span data-stu-id="ed8ac-119">Microsoft Application Virtualization Management Web Service</span></span></p></td>
<td align="left"><p><span data-ttu-id="ed8ac-120">Die Komponente, die für die Kommunikation von Lese-und Schreibanforderungen an den Application Virtualization-Datenspeicher verantwortlich ist.</span><span class="sxs-lookup"><span data-stu-id="ed8ac-120">The component responsible for communicating any read/write requests to the Application Virtualization data store.</span></span></p></td>
<td align="left"><p><span data-ttu-id="ed8ac-121">Diese Komponente kann auf dem Microsoft Application Virtualization Server oder auf einem anderen Computer installiert sein, auf dem IIS installiert ist.</span><span class="sxs-lookup"><span data-stu-id="ed8ac-121">This component can installed on the Microsoft Application Virtualization Server or on a separate computer with IIS installed.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ed8ac-122">Microsoft Application Virtualization-Datenspeicher</span><span class="sxs-lookup"><span data-stu-id="ed8ac-122">Microsoft Application Virtualization Data Store</span></span></p></td>
<td align="left"><p><span data-ttu-id="ed8ac-123">Die in der SQL-Datenbank gespeicherte Komponente, die für die Speicherung aller Informationen im Zusammenhang mit der Application Virtualization-Infrastruktur verantwortlich ist.</span><span class="sxs-lookup"><span data-stu-id="ed8ac-123">The component stored in the SQL database and responsible for storing all information related to the Application Virtualization infrastructure.</span></span></p></td>
<td align="left"><p><span data-ttu-id="ed8ac-124">Diese Informationen umfassen alle Anwendungsdatensätze, Anwendungszuordnungen und welche Gruppen für die Verwaltung der Application Virtualization-Umgebung verantwortlich sind.</span><span class="sxs-lookup"><span data-stu-id="ed8ac-124">This information includes all application records, application assignments, and which groups have responsibility for managing the Application Virtualization environment.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ed8ac-125">Microsoft Application Virtualization Streaming Server</span><span class="sxs-lookup"><span data-stu-id="ed8ac-125">Microsoft Application Virtualization Streaming Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="ed8ac-126">Die Komponente, die für das Hosten der Application Virtualization-Pakete für das Streaming an Clients in einer Zweigstelle verantwortlich ist, in der der Link zurück zum Application Virtualization Management-Server als WAN angesehen wird.</span><span class="sxs-lookup"><span data-stu-id="ed8ac-126">The component responsible for hosting the Application Virtualization packages for streaming to clients in a branch office, where the link back to the Application Virtualization Management Server is considered a WAN.</span></span></p></td>
<td align="left"><p><span data-ttu-id="ed8ac-127">Dieser Server enthält nur Streamingfunktionen und stellt weder die Application Virtualization Management Console noch den Application Virtualization Management Web Service bereit.</span><span class="sxs-lookup"><span data-stu-id="ed8ac-127">This server contains streaming functionality only and provides neither the Application Virtualization Management Console nor the Application Virtualization Management Web Service.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ed8ac-128">Microsoft Application Virtualization-Sequenzer</span><span class="sxs-lookup"><span data-stu-id="ed8ac-128">Microsoft Application Virtualization Sequencer</span></span></p></td>
<td align="left"><p><span data-ttu-id="ed8ac-129">Die Komponente, die zum Überwachen und Aufzeichnen der Installation von Anwendungen zum Erstellen von virtuellen Anwendungspaketen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ed8ac-129">The component used to monitor and capture the installation of applications to create virtual application packages.</span></span></p></td>
<td align="left"><p><span data-ttu-id="ed8ac-130">Die Ausgabe besteht aus den Symbolen der Anwendung, einer OSD-Datei mit Paketdefinitionsinformationen, einer Paket Manifestdatei und der SFT-Datei mit den Inhaltsdateien des Anwendungsprogramms.</span><span class="sxs-lookup"><span data-stu-id="ed8ac-130">Output consists of the application’s icons, an OSD file containing package definition information, a package manifest file, and the SFT file containing the application program’s content files.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ed8ac-131">Microsoft Application Virtualization-Client</span><span class="sxs-lookup"><span data-stu-id="ed8ac-131">Microsoft Application Virtualization Client</span></span></p></td>
<td align="left"><p><span data-ttu-id="ed8ac-132">Die Komponente, die auf dem Application Virtualization-Desktop Client oder auf dem Application Virtualization-Client für Remote Desktop Dienste (vormals Terminal Dienste) installiert ist und die virtuelle Umgebung für virtualisierte Anwendungen bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="ed8ac-132">The component installed on the Application Virtualization Desktop Client or on the Application Virtualization Client for Remote Desktop Services (formerly Terminal Services) and that provides the virtual environment for the virtualized applications.</span></span></p></td>
<td align="left"><p><span data-ttu-id="ed8ac-133">Der Microsoft Application Virtualization-Client verwaltet das Paketstreaming in den Zwischenspeicher, Veröffentlichungsaktualisierung, Transport und alle Interaktionen mit den Application Virtualization-Servern.</span><span class="sxs-lookup"><span data-stu-id="ed8ac-133">The Microsoft Application Virtualization Client manages the package streaming into cache, publishing refresh, transport, and all interaction with the Application Virtualization Servers.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="ed8ac-134">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="ed8ac-134">Related topics</span></span>


[<span data-ttu-id="ed8ac-135">Application Virtualization Server-basiertes Szenario</span><span class="sxs-lookup"><span data-stu-id="ed8ac-135">Application Virtualization Server-Based Scenario</span></span>](application-virtualization-server-based-scenario.md)

[<span data-ttu-id="ed8ac-136">Planen Ihrer Streaming-Lösung in einer Anwendung Virtualisierung Server-basierten-Implementierung</span><span class="sxs-lookup"><span data-stu-id="ed8ac-136">Planning Your Streaming Solution in an Application Virtualization Server-Based Implementation</span></span>](planning-your-streaming-solution-in-an-application-virtualization-server-based-implementation.md)

[<span data-ttu-id="ed8ac-137">Veröffentlichen von virtuellen Anwendungen mit Application Virtualization Management-Servern</span><span class="sxs-lookup"><span data-stu-id="ed8ac-137">Publishing Virtual Applications Using Application Virtualization Management Servers</span></span>](publishing-virtual-applications-using-application-virtualization-management-servers.md)

 

 





