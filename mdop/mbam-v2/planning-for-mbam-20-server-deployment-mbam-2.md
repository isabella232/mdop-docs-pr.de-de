---
title: Planen der Serverbereitstellung für MBAM 2.0
description: Planen der Serverbereitstellung für MBAM 2.0
author: dansimp
ms.assetid: b57f1a42-134f-4997-8697-7fbed08e2fc4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 57e6510556522dce029c958172bd89a361e06b83
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804358"
---
# <span data-ttu-id="2d8e7-103">Planen der Serverbereitstellung für MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="2d8e7-103">Planning for MBAM 2.0 Server Deployment</span></span>


<span data-ttu-id="2d8e7-104">Die Microsoft BitLocker-Serverinfrastruktur für die Verwaltungs-und Überwachungsdienste (MBAM) hängt von einer Reihe von Server Features ab, die basierend auf den Anforderungen des Unternehmens auf einem oder mehreren Server Computern installiert werden können.</span><span class="sxs-lookup"><span data-stu-id="2d8e7-104">The Microsoft BitLocker Administration and Monitoring (MBAM) server infrastructure depends on a set of server features that can be installed on one or more server computers, based on the requirements of the enterprise.</span></span> <span data-ttu-id="2d8e7-105">Wenn Sie die Microsoft BitLocker-Verwaltung und-Überwachung mit der Configuration Manager-Topologie installieren, lesen Sie [Planen der Bereitstellung von MBAM mit Configuration Manager](planning-to-deploy-mbam-with-configuration-manager-2.md).</span><span class="sxs-lookup"><span data-stu-id="2d8e7-105">If you are installing Microsoft BitLocker Administration and Monitoring with the Configuration Manager topology, see [Planning to Deploy MBAM with Configuration Manager](planning-to-deploy-mbam-with-configuration-manager-2.md).</span></span>

<span data-ttu-id="2d8e7-106">**Hinweis**  Installationen der Microsoft BitLocker-Verwaltung und-Überwachung auf einem einzelnen Server werden nur für Testumgebungen empfohlen.</span><span class="sxs-lookup"><span data-stu-id="2d8e7-106">**Note** Installations of Microsoft BitLocker Administration and Monitoring on a single server are recommended only for test environments.</span></span>

 

## <span data-ttu-id="2d8e7-107">Planen der Bereitstellung von MBAM Server</span><span class="sxs-lookup"><span data-stu-id="2d8e7-107">Planning for MBAM Server Deployment</span></span>


<span data-ttu-id="2d8e7-108">Die Infrastruktur für eine MBAM-Server Bereitstellung umfasst die folgenden Features:</span><span class="sxs-lookup"><span data-stu-id="2d8e7-108">The infrastructure for an MBAM Server deployment includes the following features:</span></span>

-   <span data-ttu-id="2d8e7-109">Wiederherstellungsdatenbank</span><span class="sxs-lookup"><span data-stu-id="2d8e7-109">Recovery Database</span></span>

-   <span data-ttu-id="2d8e7-110">Konformitäts-und Überwachungsdatenbank</span><span class="sxs-lookup"><span data-stu-id="2d8e7-110">Compliance and Audit Database</span></span>

-   <span data-ttu-id="2d8e7-111">Konformitäts-und Überwachungsberichte</span><span class="sxs-lookup"><span data-stu-id="2d8e7-111">Compliance and Audit Reports</span></span>

-   <span data-ttu-id="2d8e7-112">Self-Service-Portal</span><span class="sxs-lookup"><span data-stu-id="2d8e7-112">Self-Service Portal</span></span>

-   <span data-ttu-id="2d8e7-113">Verwaltungs-und Überwachungs Server</span><span class="sxs-lookup"><span data-stu-id="2d8e7-113">Administration and Monitoring Server</span></span>

-   <span data-ttu-id="2d8e7-114">MBAM-Gruppenrichtlinienvorlage</span><span class="sxs-lookup"><span data-stu-id="2d8e7-114">MBAM Group Policy Template</span></span>

<span data-ttu-id="2d8e7-115">MBAM Server-Datenbanken und-Features können je nach Ihren Skalierbarkeitsanforderungen in unterschiedlichen Konfigurationen installiert werden.</span><span class="sxs-lookup"><span data-stu-id="2d8e7-115">MBAM Server databases and features can be installed in different configurations, depending on your scalability requirements.</span></span> <span data-ttu-id="2d8e7-116">Alle MBAM-Server Features können auf einem einzelnen Server installiert oder auf mehrere Server verteilt werden.</span><span class="sxs-lookup"><span data-stu-id="2d8e7-116">All MBAM Server features can be installed on a single server or distributed across multiple servers.</span></span> <span data-ttu-id="2d8e7-117">Es wird empfohlen, eine Konfiguration mit zwei Servern für Produktionsumgebungen zu verwenden, wobei je nach Ihren Computeranforderungen auch Konfigurationen von zwei bis vier Servern verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="2d8e7-117">We recommend that you use a two-server configuration for production environments, although configurations of two to four servers can also be used, depending on your computing requirements.</span></span>

<span data-ttu-id="2d8e7-118">Jedes MBAM-Feature hat bestimmte Voraussetzungen.</span><span class="sxs-lookup"><span data-stu-id="2d8e7-118">Each MBAM feature has specific prerequisites.</span></span> <span data-ttu-id="2d8e7-119">Eine vollständige Liste der Voraussetzungen und Hardware-und Softwareanforderungen für Server Features finden Sie unter [MBAM 2,0-Bereitstellungsvoraussetzungen](mbam-20-deployment-prerequisites-mbam-2.md) und [unterstützte MBAM 2,0-Konfigurationen](mbam-20-supported-configurations-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="2d8e7-119">For a full list of server feature prerequisites and hardware and software requirements, see [MBAM 2.0 Deployment Prerequisites](mbam-20-deployment-prerequisites-mbam-2.md) and [MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md).</span></span>

<span data-ttu-id="2d8e7-120">Zusätzlich zu den serverbezogenen MBAM-Features umfasst die Server-Setup Anwendung eine MBAM-Gruppenrichtlinienvorlage.</span><span class="sxs-lookup"><span data-stu-id="2d8e7-120">In addition to the server-related MBAM features, the Server Setup application includes an MBAM Group Policy template.</span></span> <span data-ttu-id="2d8e7-121">Die Vorlage enthält Gruppenrichtlinienobjekt-Einstellungen, die Sie konfigurieren, um die BitLocker-Laufwerkverschlüsselung im Unternehmen zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="2d8e7-121">The template contains Group Policy Object (GPO) settings that you configure to manage BitLocker Drive Encryption in the enterprise.</span></span> <span data-ttu-id="2d8e7-122">Sie können diese Vorlage auf jedem Computer installieren, auf dem die Gruppenrichtlinien-Verwaltungskonsole (Group Policy Management Console, GPMC) oder die erweiterte Gruppenrichtlinienverwaltung (Group Policy Management, AGPM) ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="2d8e7-122">You can install this template on any computer that can run the Group Policy Management Console (GPMC) or Advanced Group Policy Management (AGPM).</span></span>

<span data-ttu-id="2d8e7-123">Wenn Sie die MBAM-Server Bereitstellung planen, sollten Sie Bedenken, dass die BitLocker-Wiederherstellungsschlüssel in MBAM nur zur einmaligen Verwendung vorgesehen sind, nachdem die Wiederherstellungsschlüssel ablaufen.</span><span class="sxs-lookup"><span data-stu-id="2d8e7-123">As you plan the MBAM Server deployment, consider that BitLocker recovery keys in MBAM are intended for single use only, after which recovery keys expire.</span></span> <span data-ttu-id="2d8e7-124">Damit die Schlüssel nach der Verwendung ablaufen, müssen Sie über das Helpdesk-Portal oder das Self-Service-Portal abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="2d8e7-124">In order for the keys to expire after use, they must be retrieved through the Help Desk Portal or the Self-Service Portal.</span></span>

## <span data-ttu-id="2d8e7-125">Reihenfolge der Bereitstellung von MBAM-Server Features</span><span class="sxs-lookup"><span data-stu-id="2d8e7-125">Order of Deployment of MBAM Server Features</span></span>


<span data-ttu-id="2d8e7-126">Zum Bereitstellen von MBAM-Features auf mehreren Servern müssen Sie die Features in der folgenden Reihenfolge installieren:</span><span class="sxs-lookup"><span data-stu-id="2d8e7-126">To deploy MBAM features on multiple servers, you have to install the features in the following order:</span></span>

1.  <span data-ttu-id="2d8e7-127">Wiederherstellungsdatenbank</span><span class="sxs-lookup"><span data-stu-id="2d8e7-127">Recovery Database</span></span>

2.  <span data-ttu-id="2d8e7-128">Konformitäts-und Überwachungsdatenbank</span><span class="sxs-lookup"><span data-stu-id="2d8e7-128">Compliance and Audit Database</span></span>

3.  <span data-ttu-id="2d8e7-129">Konformitätsprüfung und Berichte</span><span class="sxs-lookup"><span data-stu-id="2d8e7-129">Compliance Audit and Reports</span></span>

4.  <span data-ttu-id="2d8e7-130">Self-Service-Portal</span><span class="sxs-lookup"><span data-stu-id="2d8e7-130">Self-Service Portal</span></span>

5.  <span data-ttu-id="2d8e7-131">Verwaltungs-und Überwachungs Server</span><span class="sxs-lookup"><span data-stu-id="2d8e7-131">Administration and Monitoring Server</span></span>

6.  <span data-ttu-id="2d8e7-132">MBAM-Gruppenrichtlinienvorlage</span><span class="sxs-lookup"><span data-stu-id="2d8e7-132">MBAM Group Policy Template</span></span>

<span data-ttu-id="2d8e7-133">**Hinweis**  Verfolgen Sie die Namen der Computer, auf denen Sie die einzelnen Features installieren.</span><span class="sxs-lookup"><span data-stu-id="2d8e7-133">**Note** Keep track of the names of the computers on which you install each feature.</span></span> <span data-ttu-id="2d8e7-134">Sie müssen diese Informationen während des Installationsvorgangs verwenden.</span><span class="sxs-lookup"><span data-stu-id="2d8e7-134">You have to use this information throughout the installation process.</span></span> <span data-ttu-id="2d8e7-135">Sie können eine Bereitstellungscheckliste drucken und verwenden, um diesen Aufwand zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="2d8e7-135">You can print and use a deployment checklist to assist in this effort.</span></span> <span data-ttu-id="2d8e7-136">Weitere Informationen zur MBAM-Bereitstellungscheckliste finden Sie unter [MBAM 2,0 Deployment Checkliste](mbam-20-deployment-checklist-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="2d8e7-136">For more information about the MBAM Deployment Checklist, see [MBAM 2.0 Deployment Checklist](mbam-20-deployment-checklist-mbam-2.md).</span></span>

 

## <span data-ttu-id="2d8e7-137">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="2d8e7-137">Related topics</span></span>


[<span data-ttu-id="2d8e7-138">Planen der Bereitstellung von MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="2d8e7-138">Planning to Deploy MBAM 2.0</span></span>](planning-to-deploy-mbam-20-mbam-2.md)

[<span data-ttu-id="2d8e7-139">Bereitstellen der Serverinfrastruktur von MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="2d8e7-139">Deploying the MBAM 2.0 Server Infrastructure</span></span>](deploying-the-mbam-20-server-infrastructure-mbam-2.md)

 

 





