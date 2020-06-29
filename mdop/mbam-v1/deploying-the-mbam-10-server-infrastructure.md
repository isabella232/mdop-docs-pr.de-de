---
title: Bereitstellen der Serverinfrastruktur von MBAM 1.0
description: Bereitstellen der Serverinfrastruktur von MBAM 1.0
author: dansimp
ms.assetid: 90529379-b70e-4c92-b188-3d7aaf1844af
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: de136db557233a097d95f47ef0a1bba5996798c5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810999"
---
# <span data-ttu-id="1b390-103">Bereitstellen der Serverinfrastruktur von MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="1b390-103">Deploying the MBAM 1.0 Server Infrastructure</span></span>


<span data-ttu-id="1b390-104">Sie können die Microsoft BitLocker-Verwaltungs-und-Überwachungs Server Features (MBAM) in verschiedenen Konfigurationen mithilfe von einem bis fünf Servern installieren.</span><span class="sxs-lookup"><span data-stu-id="1b390-104">You can install Microsoft BitLocker Administration and Monitoring (MBAM) Server features in different configurations by using one to five servers.</span></span> <span data-ttu-id="1b390-105">Im Allgemeinen sollten Sie je nach Ihren Skalierbarkeitsanforderungen eine Konfiguration mit drei bis fünf Servern für Produktionsumgebungen verwenden.</span><span class="sxs-lookup"><span data-stu-id="1b390-105">Generally, you should use a configuration of three to five servers for production environments, depending on your scalability needs.</span></span> <span data-ttu-id="1b390-106">Weitere Informationen zur Leistungsskalierbarkeit von MBAM und empfohlenen Bereitstellungs Topologien finden Sie unter [Whitepaper zur Skalierbarkeit von MBAM und Leitfaden für die höchst Verfügbarkeit](https://go.microsoft.com/fwlink/p/?LinkId=258314).</span><span class="sxs-lookup"><span data-stu-id="1b390-106">For more information about performance scalability of MBAM and recommended deployment topologies, see the [MBAM Scalability and High-Availability Guide White Paper](https://go.microsoft.com/fwlink/p/?LinkId=258314).</span></span>

## <span data-ttu-id="1b390-107">Bereitstellen aller MBAM 1,0 auf einem einzelnen Server</span><span class="sxs-lookup"><span data-stu-id="1b390-107">Deploy all MBAM 1.0 on a single server</span></span>


<span data-ttu-id="1b390-108">In dieser Konfiguration sind alle MBAM-Features auf einem einzelnen Server installiert.</span><span class="sxs-lookup"><span data-stu-id="1b390-108">In this configuration, all MBAM features are installed on a single server.</span></span> <span data-ttu-id="1b390-109">Diese Bereitstellungstopologie für die MBAM-Serverinfrastruktur unterstützt bis zu 21.000-MBAM-Clientcomputer.</span><span class="sxs-lookup"><span data-stu-id="1b390-109">This deployment topology for MBAM server infrastructure will support up to 21,000 MBAM client computers.</span></span>

<span data-ttu-id="1b390-110">**Wichtig**  Diese Konfiguration wird unterstützt, aber wir empfehlen Sie nur zum Testen.</span><span class="sxs-lookup"><span data-stu-id="1b390-110">**Important** This configuration is supported, but we recommend it for testing only.</span></span>

 

<span data-ttu-id="1b390-111">Die Verfahren in diesem Abschnitt beschreiben die vollständige Installation der MBAM-Features auf einem einzelnen Server.</span><span class="sxs-lookup"><span data-stu-id="1b390-111">The procedures in this section describe the full installation of the MBAM features on a single server.</span></span>

[<span data-ttu-id="1b390-112">So installieren und Konfigurieren von MBAM auf einem Server</span><span class="sxs-lookup"><span data-stu-id="1b390-112">How to Install and Configure MBAM on a Single Server</span></span>](how-to-install-and-configure-mbam-on-a-single-server-mbam-1.md)

## <span data-ttu-id="1b390-113">Bereitstellen von MBAM 1,0 auf verteilten Servern</span><span class="sxs-lookup"><span data-stu-id="1b390-113">Deploy MBAM 1.0 on distributed servers</span></span>


<span data-ttu-id="1b390-114">MBAM-Features können je nach Ihren Skalierbarkeitsanforderungen in verschiedenen Konfigurationen installiert werden.</span><span class="sxs-lookup"><span data-stu-id="1b390-114">MBAM features can be installed in different configurations, depending on your scalability needs.</span></span> <span data-ttu-id="1b390-115">Weitere Informationen zum Planen der Bereitstellung von MBAM Server Features finden Sie unter [Planen der MBAM 1,0-Server Bereitstellung](planning-for-mbam-10-server-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="1b390-115">For more information about how to plan for MBAM server feature deployment, see [Planning for MBAM 1.0 Server Deployment](planning-for-mbam-10-server-deployment.md).</span></span>

<span data-ttu-id="1b390-116">Die Verfahren in diesem Abschnitt beschreiben die vollständige Installation der MBAM-Features auf verteilten Servern.</span><span class="sxs-lookup"><span data-stu-id="1b390-116">The procedures in this section describe the full installation of the MBAM features on distributed servers.</span></span>

### <span data-ttu-id="1b390-117">Konfiguration mit drei Computern</span><span class="sxs-lookup"><span data-stu-id="1b390-117">Three-computer configuration</span></span>

<span data-ttu-id="1b390-118">Das folgende Diagramm zeigt die Bereitstellungstopologie mit drei Computern für MBAM.</span><span class="sxs-lookup"><span data-stu-id="1b390-118">The following diagram displays the three-computer deployment topology for MBAM.</span></span> <span data-ttu-id="1b390-119">Wir empfehlen diese Topologie für Produktionsumgebungen, die bis zu 55.000 MBAM-Clients unterstützen.</span><span class="sxs-lookup"><span data-stu-id="1b390-119">We recommend this topology for production environments that support up to 55,000 MBAM Clients.</span></span>

![mbam drei Computer Bereitstellungstopologie](images/mbam-3-server.jpg)

<span data-ttu-id="1b390-121">In dieser Konfiguration werden die MBAM-Features in der folgenden Konfiguration installiert:</span><span class="sxs-lookup"><span data-stu-id="1b390-121">In this configuration, MBAM features are installed in the following configuration:</span></span>

1.  <span data-ttu-id="1b390-122">Wiederherstellungs-und Hardware Datenbank, Konformitäts-und Überwachungsdatenbank sowie Compliance-und Überwachungsberichte sind auf einem Server installiert.</span><span class="sxs-lookup"><span data-stu-id="1b390-122">Recovery and Hardware Database, Compliance and Audit Database, and Compliance and Audit Reports are installed on a server.</span></span>

2.  <span data-ttu-id="1b390-123">Die Verwaltungs-und Überwachungsserver Funktion ist auf einem Server installiert.</span><span class="sxs-lookup"><span data-stu-id="1b390-123">Administration and Monitoring Server feature is installed on a server.</span></span>

3.  <span data-ttu-id="1b390-124">Die MBAM-Gruppenrichtlinienvorlage ist auf einem Computer installiert, auf dem Gruppenrichtlinienobjekte (GPO) geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="1b390-124">MBAM Group Policy template is installed on a computer that is capable of modifying Group Policy Objects (GPO).</span></span>

### <span data-ttu-id="1b390-125">Konfiguration mit vier Computern</span><span class="sxs-lookup"><span data-stu-id="1b390-125">Four-computer configuration</span></span>

<span data-ttu-id="1b390-126">Das folgende Diagramm zeigt die Bereitstellungstopologie mit vier Computern für MBAM.</span><span class="sxs-lookup"><span data-stu-id="1b390-126">The following diagram displays the four-computer deployment topology for MBAM.</span></span> <span data-ttu-id="1b390-127">Wir empfehlen diese Topologie für Produktionsumgebungen, die bis zu 110.000 MBAM-Clients unterstützen.</span><span class="sxs-lookup"><span data-stu-id="1b390-127">We recommended this topology for production environments that support up to 110,000 MBAM Clients.</span></span>

![mbam vier Computer Bereitstellungstopologie.](images/mbam-4-computer.jpg)

<span data-ttu-id="1b390-129">In dieser Konfiguration werden die MBAM-Features in der folgenden Konfiguration installiert:</span><span class="sxs-lookup"><span data-stu-id="1b390-129">In this configuration, MBAM features are installed in the following configuration:</span></span>

1.  <span data-ttu-id="1b390-130">Wiederherstellungs-und Hardware Datenbank, Konformitäts-und Überwachungsdatenbank sowie Compliance-und Überwachungsberichte sind auf einem Server installiert.</span><span class="sxs-lookup"><span data-stu-id="1b390-130">Recovery and Hardware Database, Compliance and Audit Database, and Compliance and Audit Reports are installed on a server.</span></span>

2.  <span data-ttu-id="1b390-131">Die Verwaltungs-und Überwachungsserver Funktion ist auf einem Server installiert, der in einem NLB-Server Cluster (Network Load Balancing) konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="1b390-131">Administration and Monitoring Server feature is installed on a server that is configured in a Network Load Balancing (NLB) Server Cluster.</span></span>

3.  <span data-ttu-id="1b390-132">Die MBAM-Gruppenrichtlinienvorlage ist auf einem Computer installiert, auf dem die Gruppenrichtlinienobjekte geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="1b390-132">MBAM Group Policy template is installed on a computer that is capable of modifying the Group Policy Objects.</span></span>

### <span data-ttu-id="1b390-133">Konfiguration mit fünf Computern</span><span class="sxs-lookup"><span data-stu-id="1b390-133">Five-computer configuration</span></span>

<span data-ttu-id="1b390-134">Das folgende Diagramm zeigt die fünf Computer Bereitstellungstopologie für MBAM.</span><span class="sxs-lookup"><span data-stu-id="1b390-134">The following diagram displays the five-computer deployment topology for MBAM.</span></span> <span data-ttu-id="1b390-135">Wir empfehlen diese Topologie für Produktionsumgebungen, die bis zu 135.000 MBAM-Clients unterstützen.</span><span class="sxs-lookup"><span data-stu-id="1b390-135">We recommend this topology for production environments that support up to 135,000 MBAM Clients.</span></span>

![mbam fünf Computer Bereitstellungstopologie.](images/mbam-5-computer.jpg)

<span data-ttu-id="1b390-137">In dieser Konfiguration werden die MBAM-Features in der folgenden Konfiguration installiert:</span><span class="sxs-lookup"><span data-stu-id="1b390-137">In this configuration, MBAM features are installed in the following configuration:</span></span>

1.  <span data-ttu-id="1b390-138">Die Wiederherstellungs-und Hardware Datenbank ist auf einem Server installiert.</span><span class="sxs-lookup"><span data-stu-id="1b390-138">Recovery and Hardware Database is installed on a server.</span></span>

2.  <span data-ttu-id="1b390-139">Die Compliance-und Audit-Datenbank sowie Compliance-und Überwachungsberichte sind auf einem Server installiert.</span><span class="sxs-lookup"><span data-stu-id="1b390-139">The Compliance and Audit Database and Compliance and Audit Reports are installed on a server.</span></span>

3.  <span data-ttu-id="1b390-140">Die Verwaltungs-und Überwachungsserver Funktion ist auf einem Server installiert, der in einem NLB-Server Cluster (Network Load Balancing) konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="1b390-140">Administration and Monitoring Server feature is installed on a server that is configured in a Network Load Balancing (NLB) Server Cluster.</span></span>

4.  <span data-ttu-id="1b390-141">Die MBAM-Gruppenrichtlinienvorlage ist auf einem Computer installiert, auf dem Gruppenrichtlinienobjekte geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="1b390-141">MBAM Group Policy template is installed on a computer that is capable of modifying Group Policy Objects.</span></span>

[<span data-ttu-id="1b390-142">Installieren und Konfigurieren von MBAM auf verteilten Servern</span><span class="sxs-lookup"><span data-stu-id="1b390-142">How to Install and Configure MBAM on Distributed Servers</span></span>](how-to-install-and-configure-mbam-on-distributed-servers-mbam-1.md)

[<span data-ttu-id="1b390-143">So konfigurieren Sie den Netzwerklastenausgleich für MBAM</span><span class="sxs-lookup"><span data-stu-id="1b390-143">How to Configure Network Load Balancing for MBAM</span></span>](how-to-configure-network-load-balancing-for-mbam.md)

## <span data-ttu-id="1b390-144">Weitere Ressourcen für die Bereitstellung von MBAM 1,0 Server Features</span><span class="sxs-lookup"><span data-stu-id="1b390-144">Other resources for MBAM 1.0 Server features deployment</span></span>


[<span data-ttu-id="1b390-145">Bereitstellen von MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="1b390-145">Deploying MBAM 1.0</span></span>](deploying-mbam-10.md)

 

 





