---
title: Planen der Serverbereitstellung für MBAM 1.0
description: Planen der Serverbereitstellung für MBAM 1.0
author: dansimp
ms.assetid: 3cbef284-3092-4c42-9234-2826b18ddef1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 76ff9c444ce3f9c39161341610fb0cd9a763dc6d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804220"
---
# <span data-ttu-id="16929-103">Planen der Serverbereitstellung für MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="16929-103">Planning for MBAM 1.0 Server Deployment</span></span>


<span data-ttu-id="16929-104">Die Microsoft BitLocker-Serverinfrastruktur für die Verwaltungs-und Überwachungsdienste (MBAM) hängt von einer Reihe von Server Features ab, die basierend auf den Anforderungen Ihres Unternehmens auf einem oder mehreren Server Computern installiert werden können.</span><span class="sxs-lookup"><span data-stu-id="16929-104">The Microsoft BitLocker Administration and Monitoring (MBAM) server infrastructure depends on a set of server features that can be installed on one or more server computers, based on the requirements of your enterprise.</span></span>

## <span data-ttu-id="16929-105">Planen der Bereitstellung von MBAM Server</span><span class="sxs-lookup"><span data-stu-id="16929-105">Planning for MBAM Server deployment</span></span>


<span data-ttu-id="16929-106">Die folgenden MBAM-Features stellen die Serverinfrastruktur für eine MBAM-Server Bereitstellung dar:</span><span class="sxs-lookup"><span data-stu-id="16929-106">The following MBAM features represent the server infrastructure for an MBAM server deployment:</span></span>

-   <span data-ttu-id="16929-107">Wiederherstellungs-und Hardware Datenbank</span><span class="sxs-lookup"><span data-stu-id="16929-107">Recovery and Hardware Database</span></span>

-   <span data-ttu-id="16929-108">Konformitäts-und Überwachungsdatenbank</span><span class="sxs-lookup"><span data-stu-id="16929-108">Compliance and Audit Database</span></span>

-   <span data-ttu-id="16929-109">Konformitäts-und Überwachungsberichte</span><span class="sxs-lookup"><span data-stu-id="16929-109">Compliance and Audit Reports</span></span>

-   <span data-ttu-id="16929-110">Verwaltungs-und Überwachungs Server</span><span class="sxs-lookup"><span data-stu-id="16929-110">Administration and Monitoring Server</span></span>

<span data-ttu-id="16929-111">MBAM Server-Datenbanken und-Features können je nach Ihren Skalierbarkeitsanforderungen in unterschiedlichen Konfigurationen installiert werden.</span><span class="sxs-lookup"><span data-stu-id="16929-111">MBAM server databases and features can be installed in different configurations, depending on your scalability needs.</span></span> <span data-ttu-id="16929-112">Alle MBAM-Server Features können auf einem einzelnen Server installiert oder auf mehrere Server verteilt werden.</span><span class="sxs-lookup"><span data-stu-id="16929-112">All MBAM Server features can be installed on a single server or distributed across multiple servers.</span></span> <span data-ttu-id="16929-113">Im Allgemeinen empfiehlt es sich, eine Konfiguration mit drei Servern oder fünf Servern für Produktionsumgebungen zu verwenden, auch wenn Konfigurationen von zwei oder vier Servern je nach Ihren Computeranforderungen ebenfalls verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="16929-113">Generally, we recommend that you use a three-server or five-server configuration for production environments, although configurations of two or four servers can also be used, depending on your computing needs.</span></span>

<span data-ttu-id="16929-114">**Hinweis**  Weitere Informationen zur Leistungsskalierbarkeit von MBAM und empfohlenen Bereitstellungs Topologien finden Sie unter Whitepaper zur Skalierbarkeit von MBAM und Leitfaden für die höchst Verfügbarkeit <https://go.microsoft.com/fwlink/p/?LinkId=258314> .</span><span class="sxs-lookup"><span data-stu-id="16929-114">**Note** For more information about performance scalability of MBAM and recommended deployment topologies, see the MBAM Scalability and High-Availability Guide white paper at <https://go.microsoft.com/fwlink/p/?LinkId=258314>.</span></span>

 

<span data-ttu-id="16929-115">Jedes MBAM-Feature hat bestimmte Voraussetzungen.</span><span class="sxs-lookup"><span data-stu-id="16929-115">Each MBAM feature has specific prerequisites.</span></span> <span data-ttu-id="16929-116">Eine vollständige Liste der Voraussetzungen und Hardware-und Softwareanforderungen für Server Features finden Sie unter [MBAM 1,0-Bereitstellungsvoraussetzungen](mbam-10-deployment-prerequisites.md) und [unterstützte MBAM 1,0-Konfigurationen](mbam-10-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="16929-116">For a full list of server feature prerequisites and hardware and software requirements, see [MBAM 1.0 Deployment Prerequisites](mbam-10-deployment-prerequisites.md) and [MBAM 1.0 Supported Configurations](mbam-10-supported-configurations.md).</span></span>

<span data-ttu-id="16929-117">Zusätzlich zu den serverbezogenen MBAM-Features umfasst die Server-Setup Anwendung eine MBAM-Gruppenrichtlinienvorlage.</span><span class="sxs-lookup"><span data-stu-id="16929-117">In addition to the server-related MBAM features, the server Setup application includes an MBAM Group Policy template.</span></span> <span data-ttu-id="16929-118">Diese Vorlage kann auf jedem Computer installiert werden, auf dem die Gruppenrichtlinien-Verwaltungskonsole (Group Policy Management Console, GPMC) oder die erweiterte Gruppenrichtlinienverwaltung (Group Policy Management, AGPM) ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="16929-118">This template can be installed on any computer that is able to run the Group Policy Management Console (GPMC) or Advanced Group Policy Management (AGPM).</span></span>

## <span data-ttu-id="16929-119">Reihenfolge der Bereitstellung von MBAM-Server Features</span><span class="sxs-lookup"><span data-stu-id="16929-119">Order of deployment of MBAM Server Features</span></span>


<span data-ttu-id="16929-120">Wenn Sie die MBAM-Server Features bereitstellen, installieren Sie die Features in der folgenden Reihenfolge:</span><span class="sxs-lookup"><span data-stu-id="16929-120">When you deploy the MBAM Server features, install the features in the following order:</span></span>

1.  <span data-ttu-id="16929-121">Wiederherstellungs-und Hardware Datenbank</span><span class="sxs-lookup"><span data-stu-id="16929-121">Recovery and Hardware Database</span></span>

2.  <span data-ttu-id="16929-122">Konformitäts-und Überwachungsdatenbank</span><span class="sxs-lookup"><span data-stu-id="16929-122">Compliance and Audit Database</span></span>

3.  <span data-ttu-id="16929-123">Konformitätsprüfung und Berichte</span><span class="sxs-lookup"><span data-stu-id="16929-123">Compliance Audit and Reports</span></span>

4.  <span data-ttu-id="16929-124">Verwaltungs-und Überwachungs Server</span><span class="sxs-lookup"><span data-stu-id="16929-124">Administration and Monitoring Server</span></span>

5.  <span data-ttu-id="16929-125">Richtlinienvorlage</span><span class="sxs-lookup"><span data-stu-id="16929-125">Policy Template</span></span>

<span data-ttu-id="16929-126">**Hinweis**  Verfolgen Sie die Namen der Computer, auf denen Sie die einzelnen Features installieren.</span><span class="sxs-lookup"><span data-stu-id="16929-126">**Note** Keep track of the names of the computers on which you install each feature.</span></span> <span data-ttu-id="16929-127">Sie werden diese Informationen während des Installationsvorgangs verwenden.</span><span class="sxs-lookup"><span data-stu-id="16929-127">You will use this information throughout the installation process.</span></span> <span data-ttu-id="16929-128">Sie können eine Bereitstellungscheckliste drucken und verwenden, um Sie beim Installationsvorgang zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="16929-128">You can print and use a deployment checklist to assist you in the installation process.</span></span> <span data-ttu-id="16929-129">Weitere Informationen zur MBAM-Bereitstellungscheckliste finden Sie unter [MBAM 1,0 Deployment Checkliste](mbam-10-deployment-checklist.md).</span><span class="sxs-lookup"><span data-stu-id="16929-129">For more information about the MBAM deployment checklist, see [MBAM 1.0 Deployment Checklist](mbam-10-deployment-checklist.md).</span></span>

 

## <span data-ttu-id="16929-130">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="16929-130">Related topics</span></span>


[<span data-ttu-id="16929-131">Planen der Bereitstellung von MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="16929-131">Planning to Deploy MBAM 1.0</span></span>](planning-to-deploy-mbam-10.md)

[<span data-ttu-id="16929-132">Bereitstellen der Serverinfrastruktur von MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="16929-132">Deploying the MBAM 1.0 Server Infrastructure</span></span>](deploying-the-mbam-10-server-infrastructure.md)

 

 





