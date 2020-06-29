---
title: High-Level-Architektur für MBAM 1.0
description: High-Level-Architektur für MBAM 1.0
author: dansimp
ms.assetid: b1349196-88ed-4d6c-8a1d-998f18127b6b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: de3529fdb565859fcc212d1a9a614ac4ef4b183e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811035"
---
# <span data-ttu-id="52d68-103">High-Level-Architektur für MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="52d68-103">High Level Architecture for MBAM 1.0</span></span>


<span data-ttu-id="52d68-104">Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) ist eine Client/Server-Daten Verschlüsselungslösung, die Ihnen dabei helfen kann, die BitLocker-Bereitstellung und Bereitstellung zu vereinfachen, die BitLocker-Compliance und-Berichterstellung zu verbessern und die Supportkosten zu reduzieren</span><span class="sxs-lookup"><span data-stu-id="52d68-104">Microsoft BitLocker Administration and Monitoring (MBAM) is a client/server data encryption solution that can help you simplify BitLocker provisioning and deployment, improve BitLocker compliance and reporting, and reduce support costs.</span></span> <span data-ttu-id="52d68-105">MBAM enthält die Features, die in diesem Thema beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="52d68-105">MBAM includes the features that are described in this topic.</span></span>

<span data-ttu-id="52d68-106">Darüber hinaus gibt es ein Video, das eine Übersicht über die MBAM-Architektur und das MBAM-Setup bietet.</span><span class="sxs-lookup"><span data-stu-id="52d68-106">Additionally, there is a video that provides an overview of the MBAM architecture and MBAM Setup.</span></span> <span data-ttu-id="52d68-107">Weitere Informationen finden Sie unter [Übersicht über die Bereitstellung und Architektur von MBAM](https://go.microsoft.com/fwlink/p/?LinkId=258392).</span><span class="sxs-lookup"><span data-stu-id="52d68-107">For more information, see [MBAM Deployment and Architecture Overview](https://go.microsoft.com/fwlink/p/?LinkId=258392).</span></span>

## <span data-ttu-id="52d68-108">Übersicht über die Architektur</span><span class="sxs-lookup"><span data-stu-id="52d68-108">Architecture Overview</span></span>


<span data-ttu-id="52d68-109">Das folgende Diagramm zeigt die MBAM-Architektur an.</span><span class="sxs-lookup"><span data-stu-id="52d68-109">The following diagram displays the MBAM architecture.</span></span> <span data-ttu-id="52d68-110">Die MBAM-Bereitstellungstopologie mit einem Server wird angezeigt, um die MBAM-Features einzuführen.</span><span class="sxs-lookup"><span data-stu-id="52d68-110">The single-server MBAM deployment topology is shown to introduce the MBAM features.</span></span> <span data-ttu-id="52d68-111">Diese MBAM-Bereitstellungstopologie wird jedoch nur für Lab-Umgebungen empfohlen.</span><span class="sxs-lookup"><span data-stu-id="52d68-111">However, this MBAM deployment topology is recommended only for lab environments.</span></span>

<span data-ttu-id="52d68-112">**Hinweis**  Für eine Produktionsbereitstellung wird mindestens eine MBAM-Bereitstellungstopologie mit drei Computern empfohlen.</span><span class="sxs-lookup"><span data-stu-id="52d68-112">**Note** At least a three-computer MBAM deployment topology is recommended for a production deployment.</span></span> <span data-ttu-id="52d68-113">Weitere Informationen zu MBAM-Bereitstellungs Topologien finden Sie unter [Bereitstellen der MBAM 1,0-Server Infrastruktur](deploying-the-mbam-10-server-infrastructure.md).</span><span class="sxs-lookup"><span data-stu-id="52d68-113">For more information about MBAM deployment topologies, see [Deploying the MBAM 1.0 Server Infrastructure](deploying-the-mbam-10-server-infrastructure.md).</span></span>

 

![mbam Single Server-Bereitstellungstopologie](images/mbam-1-server.jpg)

1.  <span data-ttu-id="52d68-115">**Verwaltungs-und Überwachungs Server**.</span><span class="sxs-lookup"><span data-stu-id="52d68-115">**Administration and Monitoring Server**.</span></span> <span data-ttu-id="52d68-116">Der MBAM-Verwaltungs-und-Überwachungsserver ist auf einem Windows-Server installiert und fungiert als Host für die MBAM-Verwaltungs-und-Verwaltungswebsite sowie für die Überwachungs-Webdienste.</span><span class="sxs-lookup"><span data-stu-id="52d68-116">The MBAM Administration and Monitoring Server is installed on a Windows server and hosts the MBAM Administration and Management website and the monitoring web services.</span></span> <span data-ttu-id="52d68-117">Die MBAM-Verwaltungs-und-Verwaltungswebsite wird verwendet, um den Status der Unternehmenskonformität zu ermitteln, die Aktivität zu überwachen, die Hardware Funktion zu verwalten und auf Wiederherstellungsdaten wie die BitLocker-Wiederherstellungsschlüssel zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="52d68-117">The MBAM Administration and Management website is used to determine enterprise compliance status, to audit activity, to manage hardware capability, and to access recovery data, such as the BitLocker recovery keys.</span></span> <span data-ttu-id="52d68-118">Der Administrations-und Überwachungs Server stellt eine Verbindung mit den folgenden Datenbanken und Diensten her:</span><span class="sxs-lookup"><span data-stu-id="52d68-118">The Administration and Monitoring Server connects to the following databases and services:</span></span>

    -   <span data-ttu-id="52d68-119">Wiederherstellungs-und Hardware Datenbank.</span><span class="sxs-lookup"><span data-stu-id="52d68-119">Recovery and Hardware Database.</span></span> <span data-ttu-id="52d68-120">Die Wiederherstellungs-und Hardware Datenbank ist auf einem Windows-basierten Server und unterstützten SQLServer-Instanzen installiert.</span><span class="sxs-lookup"><span data-stu-id="52d68-120">The Recovery and Hardware database is installed on a Windows-based server and supported SQLServer instance.</span></span> <span data-ttu-id="52d68-121">In dieser Datenbank werden Wiederherstellungsdaten und Hardwareinformationen gespeichert, die von MBAM-Clientcomputern erfasst werden.</span><span class="sxs-lookup"><span data-stu-id="52d68-121">This database stores recovery data and hardware information that is collected from MBAM client computers.</span></span>

    -   <span data-ttu-id="52d68-122">Konformitäts-und Überwachungsdatenbank.</span><span class="sxs-lookup"><span data-stu-id="52d68-122">Compliance and Audit Database.</span></span> <span data-ttu-id="52d68-123">Die Datenbank "Konformitäts-und Überwachungsdatenbank" wird auf einer Windows Server-und unterstützten SQLServer-Instanz installiert.</span><span class="sxs-lookup"><span data-stu-id="52d68-123">The Compliance and Audit Database is installed on a Windows server and supported SQLServer instance.</span></span> <span data-ttu-id="52d68-124">In dieser Datenbank werden Kompatibilitätsdaten für MBAM-Clientcomputer gespeichert.</span><span class="sxs-lookup"><span data-stu-id="52d68-124">This database stores compliance data for MBAM client computers.</span></span> <span data-ttu-id="52d68-125">Diese Daten werden hauptsächlich für Berichte verwendet, die von SQL Server Reporting Services (SSRS) gehostet werden.</span><span class="sxs-lookup"><span data-stu-id="52d68-125">This data is used primarily for reports that are hosted by SQL Server Reporting Services (SSRS).</span></span>

    -   <span data-ttu-id="52d68-126">Konformitäts-und Überwachungsberichte.</span><span class="sxs-lookup"><span data-stu-id="52d68-126">Compliance and Audit Reports.</span></span> <span data-ttu-id="52d68-127">Die Konformitäts-und Überwachungsberichte werden auf einem auf Windows basierenden Server und unterstützten SQLServer-Instanzen installiert, auf denen das SSRS-Feature installiert ist.</span><span class="sxs-lookup"><span data-stu-id="52d68-127">The Compliance and Audit Reports are installed on a Windows-based server and supported SQLServer instance that has the SSRS feature installed.</span></span> <span data-ttu-id="52d68-128">Diese Berichte enthalten Berichte zur Microsoft BitLocker-Verwaltung und-Überwachung.</span><span class="sxs-lookup"><span data-stu-id="52d68-128">These reports provide Microsoft BitLocker Administration and Monitoring reports.</span></span> <span data-ttu-id="52d68-129">Auf diese Berichte kann über die MBAM-Verwaltungs-und-Verwaltungswebsite oder direkt vom SSRS-Server aus zugegriffen werden.</span><span class="sxs-lookup"><span data-stu-id="52d68-129">These reports can be accessed from the MBAM Administration and Management website or directly from the SSRS Server.</span></span>

2.  <span data-ttu-id="52d68-130">**MBAM-Client**.</span><span class="sxs-lookup"><span data-stu-id="52d68-130">**MBAM Client**.</span></span> <span data-ttu-id="52d68-131">Der Client für die Microsoft BitLocker-Verwaltung und-Überwachung führt die folgenden Aufgaben aus:</span><span class="sxs-lookup"><span data-stu-id="52d68-131">The Microsoft BitLocker Administration and Monitoring Client performs the following tasks:</span></span>

    -   <span data-ttu-id="52d68-132">Verwendet Gruppenrichtlinien, um die BitLocker-Verschlüsselung von Clientcomputern im Unternehmen durchzusetzen.</span><span class="sxs-lookup"><span data-stu-id="52d68-132">Uses Group Policy to enforce the BitLocker encryption of client computers in the enterprise.</span></span>

    -   <span data-ttu-id="52d68-133">Sammelt den Wiederherstellungsschlüssel für die drei BitLocker-Datenlaufwerk Typen: Betriebssystemlaufwerke, fest Netzlaufwerke und austauschbare Datenlaufwerke (USB).</span><span class="sxs-lookup"><span data-stu-id="52d68-133">Collects the recovery key for the three BitLocker data drive types: operating system drives, fixed data drives, and removable data (USB) drives.</span></span>

    -   <span data-ttu-id="52d68-134">Sammelt Wiederherstellungsinformationen und Hardwareinformationen zu den Clientcomputern.</span><span class="sxs-lookup"><span data-stu-id="52d68-134">Collects recovery information and hardware information about the client computers.</span></span>

    -   <span data-ttu-id="52d68-135">Sammelt Kompatibilitätsdaten für den Computer und übergibt die Daten an das Berichterstattungssystem.</span><span class="sxs-lookup"><span data-stu-id="52d68-135">Collects compliance data for the computer and passes the data to the reporting system.</span></span>

3.  <span data-ttu-id="52d68-136">**Richtlinienvorlage**aus.</span><span class="sxs-lookup"><span data-stu-id="52d68-136">**Policy Template**.</span></span> <span data-ttu-id="52d68-137">Die MBAM-Gruppenrichtlinienvorlage ist auf einem unterstützten Windows-basierten Server oder Clientcomputer installiert.</span><span class="sxs-lookup"><span data-stu-id="52d68-137">The MBAM Group Policy template is installed on a supported Windows-based server or client computer.</span></span> <span data-ttu-id="52d68-138">Diese Vorlage wird verwendet, um die MBAM-Implementierungs Einstellungen für die BitLocker-Laufwerkverschlüsselung festzulegen.</span><span class="sxs-lookup"><span data-stu-id="52d68-138">This template is used to specify the MBAM implementation settings for BitLocker drive encryption.</span></span>

## <span data-ttu-id="52d68-139">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="52d68-139">Related topics</span></span>


[<span data-ttu-id="52d68-140">Erste Schritte mit MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="52d68-140">Getting Started with MBAM 1.0</span></span>](getting-started-with-mbam-10.md)

 

 





