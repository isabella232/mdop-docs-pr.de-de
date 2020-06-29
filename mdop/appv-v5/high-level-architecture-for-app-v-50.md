---
title: High-Level-Architektur für App-V 5.0
description: High-Level-Architektur für App-V 5.0
author: dansimp
ms.assetid: fdf8b841-918f-4672-b352-0f2b9519581b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0ec105ffcc3213e488615603484b2de6bafce4d3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805816"
---
# <span data-ttu-id="ffad8-103">High-Level-Architektur für App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="ffad8-103">High Level Architecture for App-V 5.0</span></span>


<span data-ttu-id="ffad8-104">Verwenden Sie die folgenden Informationen, um Ihnen zu helfen, die Microsoft Application Virtualization (App-V) 5,0-Bereitstellung zu vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="ffad8-104">Use the following information to help you simplify you Microsoft Application Virtualization (App-V) 5.0 deployment.</span></span>

## <span data-ttu-id="ffad8-105">Übersicht über die Architektur</span><span class="sxs-lookup"><span data-stu-id="ffad8-105">Architecture Overview</span></span>


<span data-ttu-id="ffad8-106">Eine typische App-V 5,0-Implementierung besteht aus den folgenden Elementen.</span><span class="sxs-lookup"><span data-stu-id="ffad8-106">A typical App-V 5.0 implementation consists of the following elements.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ffad8-107">Element</span><span class="sxs-lookup"><span data-stu-id="ffad8-107">Element</span></span></th>
<th align="left"><span data-ttu-id="ffad8-108">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="ffad8-108">More information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ffad8-109">App-V 5,0-Verwaltungs Server</span><span class="sxs-lookup"><span data-stu-id="ffad8-109">App-V 5.0 Management Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="ffad8-110">Der APP-v 5,0-Verwaltungsserver bietet allgemeine Verwaltungsfunktionen für die APP-v 5,0-Infrastruktur.</span><span class="sxs-lookup"><span data-stu-id="ffad8-110">The App-V 5.0 Management server provides overall management functionality for the App-V 5.0 infrastructure.</span></span> <span data-ttu-id="ffad8-111">Darüber hinaus können Sie mehr als eine Instanz des Verwaltungsservers in Ihrer Umgebung installieren, die die folgenden Vorteile bietet:</span><span class="sxs-lookup"><span data-stu-id="ffad8-111">Additionally, you can install more than one instance of the management server in your environment which provides the following benefits:</span></span></p>
<ul>
<li><p><span data-ttu-id="ffad8-112">Fehlertoleranz und höhere Verfügbarkeit – die Installation und Konfiguration des App-V 5,0-Verwaltungsservers auf zwei separaten Computern kann in Situationen helfen, in denen einer der Server nicht verfügbar oder offline ist.</span><span class="sxs-lookup"><span data-stu-id="ffad8-112">Fault Tolerance and High Availability – Installing and configuring the App-V 5.0 Management server on two separate computers can help in situations when one of the servers is unavailable or offline.</span></span></p>
<p><span data-ttu-id="ffad8-113">Sie können auch die Verfügbarkeit von App-V 5,0 erhöhen, indem Sie den Verwaltungsserver auf mehreren Computern installieren.</span><span class="sxs-lookup"><span data-stu-id="ffad8-113">You can also help increase App-V 5.0 availability by installing the Management server on multiple computers.</span></span> <span data-ttu-id="ffad8-114">In diesem Szenario sollte auch ein Netzwerklastenausgleich berücksichtigt werden, damit Server Anforderungen ausgeglichen sind.</span><span class="sxs-lookup"><span data-stu-id="ffad8-114">In this scenario, a network load balancer should also be considered so that server requests are balanced.</span></span></p></li>
<li><p><span data-ttu-id="ffad8-115">Skalierbarkeit – Sie können bei Bedarf zusätzliche Verwaltungsserver hinzufügen, um eine hohe Auslastung zu unterstützen, beispielsweise können Sie mehrere Server hinter einem Load Balancer installieren.</span><span class="sxs-lookup"><span data-stu-id="ffad8-115">Scalability – You can add additional management servers as necessary to support a high load, for example you can install multiple servers behind a load balancer.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ffad8-116">App-V 5,0-Veröffentlichungs Server</span><span class="sxs-lookup"><span data-stu-id="ffad8-116">App-V 5.0 Publishing Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="ffad8-117">Der App-V 5,0-Publishing Server bietet Funktionen für das Hosten und Streaming virtueller Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="ffad8-117">The App-V 5.0 publishing server provides functionality for virtual application hosting and streaming.</span></span> <span data-ttu-id="ffad8-118">Der Veröffentlichungsserver erfordert keine Datenbankverbindung und unterstützt die folgenden Protokolle:</span><span class="sxs-lookup"><span data-stu-id="ffad8-118">The publishing server does not require a database connection and supports the following protocols:</span></span></p>
<ul>
<li><p><span data-ttu-id="ffad8-119">HTTP und HTTPS</span><span class="sxs-lookup"><span data-stu-id="ffad8-119">HTTP, and HTTPS</span></span></p></li>
</ul>
<p><span data-ttu-id="ffad8-120">Sie können auch die Verfügbarkeit von App-V 5,0 verbessern, indem Sie den Veröffentlichungsserver auf mehreren Computern installieren.</span><span class="sxs-lookup"><span data-stu-id="ffad8-120">You can also help increase App-V 5.0 availability by installing the Publishing server on multiple computers.</span></span> <span data-ttu-id="ffad8-121">Darüber hinaus sollte ein Netzwerklastenausgleich berücksichtigt werden, damit Server Anforderungen ausgeglichen sind.</span><span class="sxs-lookup"><span data-stu-id="ffad8-121">A network load balancer should also be considered so that server requests are balanced.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ffad8-122">App-V 5,0-Berichts Server</span><span class="sxs-lookup"><span data-stu-id="ffad8-122">App-V 5.0 Reporting Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="ffad8-123">Der APP-v 5,0-Berichtsserver ermöglicht autorisierten Benutzern, vorhandene App-v 5,0-Berichte und Ad-hoc-Berichte auszuführen und anzuzeigen, die Ihnen beim Verwalten der APP-v 5,0-Infrastruktur behilflich sein können.</span><span class="sxs-lookup"><span data-stu-id="ffad8-123">The App-V 5.0 Reporting server enables authorized users to run and view existing App-V 5.0 reports and ad hoc reports that can help them manage the App-V 5.0 infrastructure.</span></span> <span data-ttu-id="ffad8-124">Der Berichtsserver erfordert eine Verbindung mit der App-V 5,0-Berichtsdatenbank.</span><span class="sxs-lookup"><span data-stu-id="ffad8-124">The Reporting server requires a connection to the App-V 5.0 reporting database.</span></span> <span data-ttu-id="ffad8-125">Sie können auch die Verfügbarkeit von App-V 5,0 verbessern, indem Sie den Berichtsserver auf mehreren Computern installieren.</span><span class="sxs-lookup"><span data-stu-id="ffad8-125">You can also help increase App-V 5.0 availability by installing the Reporting server on multiple computers.</span></span> <span data-ttu-id="ffad8-126">Darüber hinaus sollte ein Netzwerklastenausgleich berücksichtigt werden, damit Server Anforderungen ausgeglichen sind.</span><span class="sxs-lookup"><span data-stu-id="ffad8-126">A network load balancer should also be considered so that server requests are balanced.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ffad8-127">App-V 5,0-Client</span><span class="sxs-lookup"><span data-stu-id="ffad8-127">App-V 5.0 Client</span></span></p></td>
<td align="left"><p><span data-ttu-id="ffad8-128">Mit dem App-v 5,0-Client können Pakete, die mit App-v 5,0 erstellt wurden, auf Zielcomputern ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="ffad8-128">The App-V 5.0 client enables packages created using App-V 5.0 to run on target computers.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="ffad8-129">**Hinweis**  Wenn Sie App-v 5,0 mit ESD (Electronic Software Distribution) verwenden, müssen Sie den App-v 5,0-Verwaltungsserver nicht verwenden, Sie können jedoch weiterhin die Bericht Erstellungs-und Streamingfunktionen von App-v 5,0 nutzen.</span><span class="sxs-lookup"><span data-stu-id="ffad8-129">**Note** If you are using App-V 5.0 with Electronic Software Distribution (ESD) you are not required to use the App-V 5.0 Management server, however you can still utilize the reporting and streaming functionality of App-V 5.0.</span></span>

 






## <span data-ttu-id="ffad8-130">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="ffad8-130">Related topics</span></span>


[<span data-ttu-id="ffad8-131">Erste Schritte mit App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="ffad8-131">Getting Started with App-V 5.0</span></span>](getting-started-with-app-v-50--rtm.md)

 

 





