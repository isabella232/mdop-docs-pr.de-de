---
title: Überwachen von Leistungszählern für Webdienstanforderungen
description: Überwachen von Leistungszählern für Webdienstanforderungen
author: dansimp
ms.assetid: bdb812a1-465a-4098-b4c0-cb99890d1b0d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 2db96e3375562b48d289ea5a21dc7e89b800d1ad
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810219"
---
# <span data-ttu-id="64ec8-103">Überwachen von Leistungszählern für Webdienstanforderungen</span><span class="sxs-lookup"><span data-stu-id="64ec8-103">Monitoring Web Service Request Performance Counters</span></span>


<span data-ttu-id="64ec8-104">Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) stellt Leistungsindikatoren bereit, die die Leistung von Anforderungen aufzeichnen, die an die folgenden Webdienste gesendet werden:</span><span class="sxs-lookup"><span data-stu-id="64ec8-104">Microsoft BitLocker Administration and Monitoring (MBAM) provides performance counters that record the performance of requests that are sent to the following web services:</span></span>

-   <span data-ttu-id="64ec8-105">**StatusReportingService. svc** – Dienst, der Anforderungen für den Konformitätsstatus erhält</span><span class="sxs-lookup"><span data-stu-id="64ec8-105">**StatusReportingService.svc** – service that receives requests for compliance status</span></span>

-   <span data-ttu-id="64ec8-106">**CoreService. svc** – Dienst, der Anforderungen für Schlüssel Wiederherstellungsversuche empfängt</span><span class="sxs-lookup"><span data-stu-id="64ec8-106">**CoreService.svc** – service that receives requests for key recovery attempts</span></span>

## <span data-ttu-id="64ec8-107">Von MBAM bereitgestellten Leistungsindikatoren</span><span class="sxs-lookup"><span data-stu-id="64ec8-107">Performance counters that MBAM provides</span></span>


<span data-ttu-id="64ec8-108">MBAM stellt die folgenden Leistungsindikatoren für jede der öffentlichen Methoden bereit, die von ihren StatusReportingService-und CoreService-Webdiensten implementiert werden:</span><span class="sxs-lookup"><span data-stu-id="64ec8-108">MBAM provides the following performance counters for each of the public methods that is implemented by its StatusReportingService and CoreService web services:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="64ec8-109">Typ des Leistungsindikators</span><span class="sxs-lookup"><span data-stu-id="64ec8-109">Type of performance counter</span></span></th>
<th align="left"><span data-ttu-id="64ec8-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="64ec8-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="64ec8-111">Gesamtzahl der Anforderungen</span><span class="sxs-lookup"><span data-stu-id="64ec8-111">Total number of requests</span></span></p></td>
<td align="left"><p><span data-ttu-id="64ec8-112">Stellt eine Inkrementierung bereit, die beim Starten oder Neustarten des Servers bei Null beginnt.</span><span class="sxs-lookup"><span data-stu-id="64ec8-112">Provides an incrementing count that starts from zero when the server is started or restarted.</span></span></p>
<p><span data-ttu-id="64ec8-113">Bietet eine Gesamtübersicht über die Systemaktivität.</span><span class="sxs-lookup"><span data-stu-id="64ec8-113">Provides an overall view of system activity.</span></span> <span data-ttu-id="64ec8-114">Kann mithilfe automatisierter Tools überwacht werden, um die Integrität des Servers zu gewährleisten und zu überprüfen, ob der Zähler kontinuierlich über einen bestimmten Zeitraum inkrementiert wird.</span><span class="sxs-lookup"><span data-stu-id="64ec8-114">Can be monitored by automated tools to ensure the health of the server and to validate that the counter continually increments over a specified period of time.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="64ec8-115">Anforderungen pro Sekunde</span><span class="sxs-lookup"><span data-stu-id="64ec8-115">Requests per second</span></span></p></td>
<td align="left"><p><span data-ttu-id="64ec8-116">Gibt den aktuellen Durchsatz des MBAM-Servers an, da er die MBAM-Clientbasis unterstützt.</span><span class="sxs-lookup"><span data-stu-id="64ec8-116">Indicates the current throughput of the MBAM Server as it supports the MBAM client base.</span></span></p>
<p><span data-ttu-id="64ec8-117">Ermöglicht Websiteadministratoren Folgendes:</span><span class="sxs-lookup"><span data-stu-id="64ec8-117">Enables site administrators to:</span></span></p>
<ul>
<li><p><span data-ttu-id="64ec8-118">Berechnen Sie die durchschnittliche Anzahl der Anforderungen pro Sekunde, basierend auf der Anzahl der MBAM-Clients und deren Häufigkeit der Berichterstellung.</span><span class="sxs-lookup"><span data-stu-id="64ec8-118">Calculate the average number of requests per second, based on the number of MBAM Clients and their reporting frequency.</span></span></p></li>
<li><p><span data-ttu-id="64ec8-119">Überprüfen Sie, ob die Anzahl der Anforderungen pro Sekunde in großem Umfang mit der berechneten durchschnittlichen Anzahl von Anforderungen pro Sekunde korreliert.</span><span class="sxs-lookup"><span data-stu-id="64ec8-119">Validate that the number of requests per second broadly correlates with the calculated average number of requests per second.</span></span> <span data-ttu-id="64ec8-120">Eine erhebliche Abweichung kann darauf hindeuten, dass der MBAM-Client nicht auf einem Prozentsatz der Clientbasis installiert ist oder dass ein MBAM-Gruppenrichtlinienobjekt nicht erfolgreich bereitgestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="64ec8-120">A significant variance can indicate that the MBAM Client isn't installed on a percentage of the client base or that an MBAM Group Policy Object hasn't been successfully deployed.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="64ec8-121">Anforderungsdauer</span><span class="sxs-lookup"><span data-stu-id="64ec8-121">Request duration</span></span></p></td>
<td align="left"><p><span data-ttu-id="64ec8-122">Zeichnet die Dauer von Anforderungen in Millisekunden auf.</span><span class="sxs-lookup"><span data-stu-id="64ec8-122">Records the duration of requests in milliseconds.</span></span></p>
<p><span data-ttu-id="64ec8-123">Obwohl dieser Leistungsindikator mit der Dauer jeder Anforderung aktualisiert wird, wird er von der Windows-Leistungsüberwachung nur in regelmäßigen Abständen (normalerweise in jeder Sekunde) angezeigt, sodass Sie möglicherweise eine gewisse Variabilität des Werts sehen.</span><span class="sxs-lookup"><span data-stu-id="64ec8-123">Although this counter is updated with the duration of each request, Windows Performance Monitor samples it only periodically (typically every second), so you might see some variability in the value.</span></span> <span data-ttu-id="64ec8-124">Aus diesem Grund sollten Sie die Verwendung des durch den System Monitor angezeigten Mittelwerts in Frage stellen.</span><span class="sxs-lookup"><span data-stu-id="64ec8-124">For this reason, consider using the average value displayed by Performance Monitor.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="64ec8-125">Ergebnisse und Empfehlungen zu Leistungsindikatoren</span><span class="sxs-lookup"><span data-stu-id="64ec8-125">Performance counter results and recommendations</span></span>


<span data-ttu-id="64ec8-126">Wenn Sie neue MBAM-Clients zu einem MBAM-Server mit Reservekapazität hinzufügen, erwarten Sie, dass die Anzahl der Anfragen pro Sekunde steigt.</span><span class="sxs-lookup"><span data-stu-id="64ec8-126">As you add new MBAM Clients to an MBAM Server with spare capacity, expect to see an increase in the number of requests per second.</span></span> <span data-ttu-id="64ec8-127">Dieser Anstieg ist proportional zur Anzahl der neuen Clientcomputer.</span><span class="sxs-lookup"><span data-stu-id="64ec8-127">This increase will be proportional to the number of new client computers.</span></span> <span data-ttu-id="64ec8-128">Die durchschnittliche Anforderungsdauer bleibt relativ statisch.</span><span class="sxs-lookup"><span data-stu-id="64ec8-128">The average request duration will remain relatively static.</span></span> <span data-ttu-id="64ec8-129">Wenn der Server seine maximale Kapazität erreicht, werden die Anforderungen pro Sekunde gestartet, um sich zu verkleinern, und die durchschnittliche Anforderungsdauer wird länger.</span><span class="sxs-lookup"><span data-stu-id="64ec8-129">As the server nears its maximum capacity, the requests per second start to level out, and the average request duration starts to get longer.</span></span>

<span data-ttu-id="64ec8-130">Wenn Sie Bedenken haben, ob Ihre MBAM-Server Ihre Clientbasis unterstützen können, sollten Sie die Bereitstellung von MBAM in Phasen in verschiedenen Sammlungen von Clientcomputern in Betracht gezogen.</span><span class="sxs-lookup"><span data-stu-id="64ec8-130">If you are concerned about whether your MBAM Servers can support your client base, consider deploying MBAM in phases across different collections of client computers.</span></span> <span data-ttu-id="64ec8-131">Wenn Sie MBAM für jede Sammlung von Clientcomputern bereitstellen, empfehlen wir, Snapshots der Leistungsindikatoren zu erstellen, um die relativen Auswirkungen der Bereitstellung auf jede neue Clientsammlung zu erkennen.</span><span class="sxs-lookup"><span data-stu-id="64ec8-131">As you deploy MBAM to each collection of client computers, we recommend that you take snapshots of the performance counters to see the relative impact of deploying to each new client collection.</span></span> <span data-ttu-id="64ec8-132">Wenn sich die Anzahl der Anforderungen pro Sekunde abhebt und die durchschnittliche Anforderungsdauer zunimmt, sollten Sie die MBAM-Server Infrastruktur erweitern, indem Sie eine der folgenden Aktionen ausführen:</span><span class="sxs-lookup"><span data-stu-id="64ec8-132">If the number of requests per second starts to level off and the average request duration increases, consider enhancing your MBAM Server infrastructure by doing one of the following:</span></span>

-   <span data-ttu-id="64ec8-133">Verschieben der MBAM-Datenbank auf einen dedizierten Microsoft SQL Server-oder SQL Server-Cluster</span><span class="sxs-lookup"><span data-stu-id="64ec8-133">Moving the MBAM database onto a dedicated Microsoft SQL Server or SQL Server cluster</span></span>

-   <span data-ttu-id="64ec8-134">Lastenausgleichs MBAM auf mehreren IIS-Webservern (Internet Informationsdienste)</span><span class="sxs-lookup"><span data-stu-id="64ec8-134">Load-balancing MBAM across multiple Internet Information Services (IIS) web servers</span></span>

-   <span data-ttu-id="64ec8-135">Bereitstellen von MBAM auf einer leistungsfähigeren Server Hardware</span><span class="sxs-lookup"><span data-stu-id="64ec8-135">Deploying MBAM on more powerful server hardware</span></span>

## <span data-ttu-id="64ec8-136">Anzeigen von Leistungsindikatoren</span><span class="sxs-lookup"><span data-stu-id="64ec8-136">Viewing performance counters</span></span>


<span data-ttu-id="64ec8-137">Das empfohlene Tool für die Anzeige von MBAM-Leistungsindikatoren ist der Windows-System Monitor, der im Lieferumfang von Windows enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="64ec8-137">The recommended tool for viewing MBAM performance counters is Windows Performance Monitor, which comes with Windows.</span></span> <span data-ttu-id="64ec8-138">Wenn Sie Windows PowerShell verwenden, müssen Sie die Leistungsindikatoren nicht aktivieren, bevor Sie Sie anzeigen können, da Sie automatisch vom Windows PowerShell **enable-WebApplication-** Cmdlet registriert werden.</span><span class="sxs-lookup"><span data-stu-id="64ec8-138">If you are using Windows PowerShell, you don’t need to enable the counters before viewing them, as they are automatically registered by the Windows PowerShell **Enable-webapplication** cmdlet.</span></span>

<span data-ttu-id="64ec8-139">Ausführliche Anweisungen zum Anzeigen von Leistungsindikatoren finden Sie unter [Anzeigen von MBAM-Leistungsindikatoren](https://go.microsoft.com/fwlink/?LinkId=393457).</span><span class="sxs-lookup"><span data-stu-id="64ec8-139">For detailed instructions on how to view performance counters, see [How to View MBAM Performance Counters](https://go.microsoft.com/fwlink/?LinkId=393457).</span></span>



## <span data-ttu-id="64ec8-140">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="64ec8-140">Related topics</span></span>


[<span data-ttu-id="64ec8-141">Verwalten von MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="64ec8-141">Maintaining MBAM 2.5</span></span>](maintaining-mbam-25.md)

 

 


## <span data-ttu-id="64ec8-142">Sie haben einen Vorschlag für MBAM?</span><span class="sxs-lookup"><span data-stu-id="64ec8-142">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="64ec8-143">[Hier](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)können Sie Vorschläge hinzufügen oder abstimmen.</span><span class="sxs-lookup"><span data-stu-id="64ec8-143">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="64ec8-144">Bei MBAM-Problemen verwenden Sie das [MBAM TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="64ec8-144">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>


