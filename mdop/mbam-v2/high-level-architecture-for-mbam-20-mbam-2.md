---
title: High-Level-Architektur für MBAM2.0
description: High-Level-Architektur für MBAM2.0
author: dansimp
ms.assetid: 7f73dd3a-0b1f-4af6-a2f0-d0c5bc5d183a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ddc061a1aec5141548c2d2141be38f8501d2244d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810714"
---
# <span data-ttu-id="3faa7-103">High-Level-Architektur für MBAM2.0</span><span class="sxs-lookup"><span data-stu-id="3faa7-103">High-Level Architecture for MBAM 2.0</span></span>


<span data-ttu-id="3faa7-104">Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) ist eine Client/Server-Lösung, die Ihnen dabei helfen kann, die BitLocker-Bereitstellung und Bereitstellung zu vereinfachen, die Compliance und die Berichterstellung für BitLocker zu verbessern und die Supportkosten zu senken.</span><span class="sxs-lookup"><span data-stu-id="3faa7-104">Microsoft BitLocker Administration and Monitoring (MBAM) is a client/server solution that can help you simplify BitLocker provisioning and deployment, improve compliance and reporting on BitLocker, and reduce support costs.</span></span> <span data-ttu-id="3faa7-105">Die Microsoft BitLocker-Verwaltung und-Überwachung umfasst die Features, die in diesem Thema beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="3faa7-105">Microsoft BitLocker Administration and Monitoring includes the features that are described in this topic.</span></span>

<span data-ttu-id="3faa7-106">Die Microsoft BitLocker-Verwaltung und-Überwachung kann in der eigenständigen Topologie oder in einer Topologie bereitgestellt werden, die in Microsoft System Center Configuration Manager 2007 oder MicrosoftSystemCenter2012 ConfigurationManager integriert ist.</span><span class="sxs-lookup"><span data-stu-id="3faa7-106">Microsoft BitLocker Administration and Monitoring can be deployed in the Stand-alone topology, or in a topology that is integrated with Microsoft System Center Configuration Manager 2007 or MicrosoftSystemCenter2012 ConfigurationManager.</span></span> <span data-ttu-id="3faa7-107">In diesem Thema wird die Architektur für die eigenständige Topologie beschrieben.</span><span class="sxs-lookup"><span data-stu-id="3faa7-107">This topic describes the architecture for the Stand-alone topology.</span></span> <span data-ttu-id="3faa7-108">Informationen zum Bereitstellen in der integrierten Configuration Manager-Topologie finden Sie unter [Verwenden von MBAM mit Configuration Manager](using-mbam-with-configuration-manager.md).</span><span class="sxs-lookup"><span data-stu-id="3faa7-108">For information about deploying in the integrated Configuration Manager topology, see [Using MBAM with Configuration Manager](using-mbam-with-configuration-manager.md).</span></span>

<span data-ttu-id="3faa7-109">Das folgende Diagramm zeigt die empfohlene MBAM-Architektur für eine Produktionsumgebung, die aus zwei Servern und einer Verwaltungsarbeitsstation besteht.</span><span class="sxs-lookup"><span data-stu-id="3faa7-109">The following diagram shows the MBAM recommended architecture for a production environment, which consists of two servers and a management workstation.</span></span> <span data-ttu-id="3faa7-110">Diese Architektur unterstützt bis zu 200.000 MBAM-Clients.</span><span class="sxs-lookup"><span data-stu-id="3faa7-110">This architecture supports up to 200,000 MBAM clients.</span></span> <span data-ttu-id="3faa7-111">Die Server Features und-Datenbanken im Architektur Bild werden im folgenden Abschnitt beschrieben und unter dem Computer oder Server aufgelistet, auf dem wir die Installation empfehlen.</span><span class="sxs-lookup"><span data-stu-id="3faa7-111">The server features and databases in the architecture image are described in the following section and are listed under the computer or server where we recommend that you install them.</span></span>

<span data-ttu-id="3faa7-112">**Hinweis**  Eine Architektur mit einem Server sollte nur in Testumgebungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3faa7-112">**Note** A single-server architecture should be used only in test environments.</span></span>

 

![mbam 2 2-Server Bereitstellungstopologie](images/mbam2-3-servers.gif)

## <span data-ttu-id="3faa7-114">Verwaltungs-und Überwachungs Server</span><span class="sxs-lookup"><span data-stu-id="3faa7-114">Administration and Monitoring Server</span></span>


<span data-ttu-id="3faa7-115">Die folgenden Features sind auf diesem Server installiert:</span><span class="sxs-lookup"><span data-stu-id="3faa7-115">The following features are installed on this server:</span></span>

-   <span data-ttu-id="3faa7-116">**Verwaltungs-und Überwachungs Server**.</span><span class="sxs-lookup"><span data-stu-id="3faa7-116">**Administration and Monitoring Server**.</span></span> <span data-ttu-id="3faa7-117">Die Verwaltungs-und Überwachungs Server Funktion ist auf einem Windows-Server installiert und besteht aus der Websiteverwaltung und Überwachung, die die Berichte und das Helpdesk-Portal sowie die Überwachungs-Webdienste umfasst.</span><span class="sxs-lookup"><span data-stu-id="3faa7-117">The Administration and Monitoring Server feature is installed on a Windows server and consists of the Administration and Monitoring website, which includes the reports and the Help Desk Portal, and the monitoring web services.</span></span>

-   <span data-ttu-id="3faa7-118">**Self-Service-Portal**.</span><span class="sxs-lookup"><span data-stu-id="3faa7-118">**Self-Service Portal**.</span></span> <span data-ttu-id="3faa7-119">Das Self-Service-Portal ist auf einem Windows-Server installiert.</span><span class="sxs-lookup"><span data-stu-id="3faa7-119">The Self-Service Portal is installed on a Windows server.</span></span> <span data-ttu-id="3faa7-120">Das Self-Service-Portal ermöglicht Endbenutzern auf Clientcomputern die unabhängige Anmeldung bei einer Website, auf der Sie einen Wiederherstellungsschlüssel zum Wiederherstellen eines gesperrten BitLocker-Volumes abrufen können.</span><span class="sxs-lookup"><span data-stu-id="3faa7-120">The Self-Service Portal enables end users on client computers to independently log on to a website, where they can obtain a recovery key to recover a locked BitLocker volume.</span></span>

## <span data-ttu-id="3faa7-121">Daten Bank Server</span><span class="sxs-lookup"><span data-stu-id="3faa7-121">Database Server</span></span>


<span data-ttu-id="3faa7-122">Die folgenden Features sind auf diesem Server installiert:</span><span class="sxs-lookup"><span data-stu-id="3faa7-122">The following features are installed on this server:</span></span>

-   <span data-ttu-id="3faa7-123">**Wiederherstellungsdatenbank**.</span><span class="sxs-lookup"><span data-stu-id="3faa7-123">**Recovery Database**.</span></span> <span data-ttu-id="3faa7-124">Die Wiederherstellungsdatenbank ist auf einem Windows-Server und einer unterstützten Instanz von Microsoft SQLServer installiert.</span><span class="sxs-lookup"><span data-stu-id="3faa7-124">The Recovery Database is installed on a Windows server and a supported instance of Microsoft SQLServer.</span></span> <span data-ttu-id="3faa7-125">In dieser Datenbank werden Wiederherstellungsdaten gespeichert, die von MBAM-Clientcomputern erfasst werden.</span><span class="sxs-lookup"><span data-stu-id="3faa7-125">This database stores recovery data that is collected from MBAM client computers.</span></span>

-   <span data-ttu-id="3faa7-126">**Konformitäts-und Überwachungsdatenbank**.</span><span class="sxs-lookup"><span data-stu-id="3faa7-126">**Compliance and Audit Database**.</span></span> <span data-ttu-id="3faa7-127">Die Compliance-und Überwachungsdatenbank ist auf einem Windows-Server und einer unterstützten Instanz von SQLServer installiert.</span><span class="sxs-lookup"><span data-stu-id="3faa7-127">The Compliance and Audit Database is installed on a Windows server and a supported instance of SQLServer.</span></span> <span data-ttu-id="3faa7-128">In dieser Datenbank werden Kompatibilitätsdaten für MBAM-Clientcomputer gespeichert.</span><span class="sxs-lookup"><span data-stu-id="3faa7-128">This database stores compliance data for MBAM client computers.</span></span> <span data-ttu-id="3faa7-129">Diese Daten werden hauptsächlich für Berichte verwendet, die von SQL Server Reporting Services (SSRS) gehostet werden.</span><span class="sxs-lookup"><span data-stu-id="3faa7-129">This data is used primarily for reports that SQL Server Reporting Services (SSRS) hosts.</span></span>

-   <span data-ttu-id="3faa7-130">**Konformitäts-und Überwachungsberichte**.</span><span class="sxs-lookup"><span data-stu-id="3faa7-130">**Compliance and Audit Reports**.</span></span> <span data-ttu-id="3faa7-131">Die Kompatibilitäts-und Überwachungsberichte sind auf einem Windows-Server und einer unterstützten Instanz von SQLServer installiert, auf der das Feature SQL Server Reporting Services (SSRS) installiert ist.</span><span class="sxs-lookup"><span data-stu-id="3faa7-131">The Compliance and Audit Reports are installed on a Windows server and a supported instance of SQLServer that has the SQL Server Reporting Services (SSRS) feature installed.</span></span> <span data-ttu-id="3faa7-132">Diese Berichte enthalten MBAM-Berichte, auf die Sie über die Websiteverwaltung und Überwachung oder direkt vom SSRS-Server aus zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="3faa7-132">These reports provide MBAM reports that you can access from the Administration and Monitoring website or directly from the SSRS server.</span></span>

## <span data-ttu-id="3faa7-133">Verwaltungsarbeitsstation</span><span class="sxs-lookup"><span data-stu-id="3faa7-133">Management Workstation</span></span>


<span data-ttu-id="3faa7-134">Das folgende Feature ist auf der Verwaltungsarbeitsstation installiert, die ein Windows-Server oder ein Clientcomputer sein kann.</span><span class="sxs-lookup"><span data-stu-id="3faa7-134">The following feature is installed on the Management workstation, which can be a Windows server or a client computer.</span></span>

-   <span data-ttu-id="3faa7-135">**Richtlinienvorlage**aus.</span><span class="sxs-lookup"><span data-stu-id="3faa7-135">**Policy Template**.</span></span> <span data-ttu-id="3faa7-136">Die Richtlinienvorlage besteht aus Gruppenrichtlinieneinstellungen, die die MBAM-Implementierungs Einstellungen für die BitLocker-Laufwerkverschlüsselung definieren.</span><span class="sxs-lookup"><span data-stu-id="3faa7-136">The Policy Template consists of Group Policy settings that define MBAM implementation settings for BitLocker drive encryption.</span></span> <span data-ttu-id="3faa7-137">Sie können die Richtlinienvorlage auf einem beliebigen Server oder auf einer Arbeitsstation installieren, Sie wird jedoch häufig auf einer Verwaltungsarbeitsstation installiert, die ein unterstützter Windows-Server oder-Clientcomputer ist.</span><span class="sxs-lookup"><span data-stu-id="3faa7-137">You can install the Policy template on any server or workstation, but it is commonly installed on a management workstation, which is a supported Windows server or client computer.</span></span> <span data-ttu-id="3faa7-138">Die Workstation muss kein dedizierter Computer sein.</span><span class="sxs-lookup"><span data-stu-id="3faa7-138">The workstation does not have to be a dedicated computer.</span></span>

## <a href="" id="---------mbam-client"></a> <span data-ttu-id="3faa7-139">MBAM-Client</span><span class="sxs-lookup"><span data-stu-id="3faa7-139">MBAM Client</span></span>


<span data-ttu-id="3faa7-140">Der MBAM-Client ist auf einem Windows-Computer installiert und weist die folgenden Merkmale auf:</span><span class="sxs-lookup"><span data-stu-id="3faa7-140">The MBAM Client is installed on a Windows computer and has the following characteristics:</span></span>

-   <span data-ttu-id="3faa7-141">Verwendet Gruppenrichtlinien, um die BitLocker-Laufwerkverschlüsselung von Clientcomputern im Unternehmen zu erzwingen.</span><span class="sxs-lookup"><span data-stu-id="3faa7-141">Uses Group Policy to enforce the BitLocker drive encryption of client computers in the enterprise.</span></span>

-   <span data-ttu-id="3faa7-142">Sammelt den Wiederherstellungsschlüssel für die drei BitLocker-Datenlaufwerk Typen: Betriebssystemlaufwerke, fest Netzlaufwerke und austauschbare Datenlaufwerke (USB).</span><span class="sxs-lookup"><span data-stu-id="3faa7-142">Collects the recovery key for the three BitLocker data drive types: operating system drives, fixed data drives, and removable data (USB) drives.</span></span>

-   <span data-ttu-id="3faa7-143">Sammelt Kompatibilitätsdaten für den Computer und übergibt die Daten an das Berichterstattungssystem.</span><span class="sxs-lookup"><span data-stu-id="3faa7-143">Collects compliance data for the computer and passes the data to the reporting system.</span></span>

## <span data-ttu-id="3faa7-144">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="3faa7-144">Related topics</span></span>


[<span data-ttu-id="3faa7-145">Erste Schritte mit MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="3faa7-145">Getting Started with MBAM 2.0</span></span>](getting-started-with-mbam-20-mbam-2.md)

 

 





