---
title: Bereitstellen von MBAM 2.5
description: Bereitstellen von MBAM 2.5
author: dansimp
ms.assetid: 45403607-1f4d-42fe-8413-0d4da01808a6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0cfa0a190530186211cd96884b2e32e9c65881f1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811662"
---
# <span data-ttu-id="44909-103">Bereitstellen von MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="44909-103">Deploying MBAM 2.5</span></span>


<span data-ttu-id="44909-104">Verwenden Sie diese Informationen, um die Verfahren zum Bereitstellen und Konfigurieren von Microsoft BitLocker-Verwaltungs-und-Überwachungsfunktionen (MBAM) 2,5-Server Features für das Upgrade auf MBAM 2,5 aus früheren Versionen oder zum Entfernen von MBAM-Server Features zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="44909-104">Use this information to identify the procedures you can follow to deploy and configure Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 Server features to upgrade to MBAM 2.5 from previous versions, or to remove MBAM Server features.</span></span>

## <span data-ttu-id="44909-105">Bereitstellungsinformationen</span><span class="sxs-lookup"><span data-stu-id="44909-105">Deployment information</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="44909-106">Beschreibung des Themas</span><span class="sxs-lookup"><span data-stu-id="44909-106">Topic description</span></span></th>
<th align="left"><span data-ttu-id="44909-107">Links zu Themen</span><span class="sxs-lookup"><span data-stu-id="44909-107">Links to topics</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><ul>
<li><p><span data-ttu-id="44909-108">Optionen für die Bereitstellungstopologie</span><span class="sxs-lookup"><span data-stu-id="44909-108">Deployment topology options.</span></span></p></li>
<li><p><span data-ttu-id="44909-109">So installieren Sie die MBAM-Server Software</span><span class="sxs-lookup"><span data-stu-id="44909-109">How to install the MBAM Server software.</span></span></p></li>
<li><p><span data-ttu-id="44909-110">Konfigurieren der MBAM-Server Features</span><span class="sxs-lookup"><span data-stu-id="44909-110">How to configure the MBAM Server features.</span></span></p></li>
</ul></td>
<td align="left"><p><a href="deploying-the-mbam-25-server-infrastructure.md" data-raw-source="[Deploying the MBAM 2.5 Server Infrastructure](deploying-the-mbam-25-server-infrastructure.md)"><span data-ttu-id="44909-111">Bereitstellen der Serverinfrastruktur von MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="44909-111">Deploying the MBAM 2.5 Server Infrastructure</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="44909-112">Hier erfahren Sie, wie Sie die Vorlagen für MBAM-Gruppenrichtlinien herunterladen und bereitstellen, die für die Verwaltung von MBAM-Clients und BitLocker-Verschlüsselungsrichtlinien im Unternehmen erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="44909-112">How to download and deploy the MBAM Group Policy Templates, which are required to manage MBAM Clients and BitLocker encryption policies in the enterprise.</span></span></p></td>
<td align="left"><p><a href="deploying-mbam-25-group-policy-objects.md" data-raw-source="[Deploying MBAM 2.5 Group Policy Objects](deploying-mbam-25-group-policy-objects.md)"><span data-ttu-id="44909-113">Bereitstellen von Gruppenrichtlinienobjekten für MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="44909-113">Deploying MBAM 2.5 Group Policy Objects</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="44909-114">Verwenden der MBAM-Client-Windows Installer-Dateien zum Bereitstellen der MBAM-Client Software.</span><span class="sxs-lookup"><span data-stu-id="44909-114">How to use the MBAM Client Windows Installer files to deploy the MBAM Client software.</span></span></p></td>
<td align="left"><p><a href="deploying-the-mbam-25-client.md" data-raw-source="[Deploying the MBAM 2.5 Client](deploying-the-mbam-25-client.md)"><span data-ttu-id="44909-115">Bereitstellen des MBAM 2.5-Clients</span><span class="sxs-lookup"><span data-stu-id="44909-115">Deploying the MBAM 2.5 Client</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="44909-116">Checkliste, die Ihnen bei der Bereitstellung der MBAM-Server Features und des MBAM-Clients behilflich sein kann.</span><span class="sxs-lookup"><span data-stu-id="44909-116">Checklist that can assist you in deploying the MBAM Server features and MBAM Client.</span></span></p></td>
<td align="left"><p><a href="mbam-25-deployment-checklist.md" data-raw-source="[MBAM 2.5 Deployment Checklist](mbam-25-deployment-checklist.md)"><span data-ttu-id="44909-117">Prüfliste für die Bereitstellung von MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="44909-117">MBAM 2.5 Deployment Checklist</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="44909-118">Aktualisieren von MBAM aus früheren Versionen</span><span class="sxs-lookup"><span data-stu-id="44909-118">How to upgrade MBAM from previous versions.</span></span></p></td>
<td align="left"><p><a href="upgrading-to-mbam-25-or-mbam-25-sp1-from-previous-versions.md" data-raw-source="[Upgrading to MBAM 2.5 or MBAM 2.5 SP1 from Previous Versions](upgrading-to-mbam-25-or-mbam-25-sp1-from-previous-versions.md)"><span data-ttu-id="44909-119">Aktualisieren von MBAM 2.5 oder MBAM 2.5 SP1 von früheren Versionen</span><span class="sxs-lookup"><span data-stu-id="44909-119">Upgrading to MBAM 2.5 or MBAM 2.5 SP1 from Previous Versions</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="44909-120">Entfernen von MBAM-Server Features oder-Software.</span><span class="sxs-lookup"><span data-stu-id="44909-120">How to remove MBAM Server features or software.</span></span></p></td>
<td align="left"><p><a href="removing-mbam-server-features-or-software.md" data-raw-source="[Removing MBAM Server Features or Software](removing-mbam-server-features-or-software.md)"><span data-ttu-id="44909-121">Entfernen von MBAM-Serverfunktionen oder -software</span><span class="sxs-lookup"><span data-stu-id="44909-121">Removing MBAM Server Features or Software</span></span></a></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="44909-122">Weitere Ressourcen für die Bereitstellung von MBAM</span><span class="sxs-lookup"><span data-stu-id="44909-122">Other resources for deploying MBAM</span></span>


[<span data-ttu-id="44909-123">Microsoft BitLocker Administration and Monitoring 2.5</span><span class="sxs-lookup"><span data-stu-id="44909-123">Microsoft BitLocker Administration and Monitoring 2.5</span></span>](index.md)

[<span data-ttu-id="44909-124">Erste Schritte mit MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="44909-124">Getting Started with MBAM 2.5</span></span>](getting-started-with-mbam-25.md)

[<span data-ttu-id="44909-125">Planen von MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="44909-125">Planning for MBAM 2.5</span></span>](planning-for-mbam-25.md)

[<span data-ttu-id="44909-126">Vorgänge für MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="44909-126">Operations for MBAM 2.5</span></span>](operations-for-mbam-25.md)

[<span data-ttu-id="44909-127">Problembehandlung bei MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="44909-127">Troubleshooting MBAM 2.5</span></span>](troubleshooting-mbam-25.md)

[<span data-ttu-id="44909-128">Technische Referenz für MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="44909-128">Technical Reference for MBAM 2.5</span></span>](technical-reference-for-mbam-25.md)

[<span data-ttu-id="44909-129">Bereitstellen von MBAM 2,5 in einer eigenständigen Konfiguration</span><span class="sxs-lookup"><span data-stu-id="44909-129">Deploying MBAM 2.5 in a stand-alone configuration</span></span>](https://support.microsoft.com/kb/3046555)

## <span data-ttu-id="44909-130">Sie haben einen Vorschlag für MBAM?</span><span class="sxs-lookup"><span data-stu-id="44909-130">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="44909-131">[Hier](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)können Sie Vorschläge hinzufügen oder abstimmen.</span><span class="sxs-lookup"><span data-stu-id="44909-131">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="44909-132">Bei MBAM-Problemen verwenden Sie das [MBAM TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="44909-132">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>

 

 





