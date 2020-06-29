---
title: Bereitstellen der Serverinfrastruktur von MBAM 2.0
description: Bereitstellen der Serverinfrastruktur von MBAM 2.0
author: dansimp
ms.assetid: 52e68d94-e2b4-4b06-ae55-f900ea6cc59f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 22a69fe8f6853c02a818bb026b36771cd09632f0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810747"
---
# <span data-ttu-id="abc1e-103">Bereitstellen der Serverinfrastruktur von MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="abc1e-103">Deploying the MBAM 2.0 Server Infrastructure</span></span>


<span data-ttu-id="abc1e-104">Die Microsoft BitLocker-MBAM-Server Features für die eigenständige Topologie können in verschiedenen Konfigurationen auf zwei oder mehr Servern in einer Produktionsumgebung installiert werden.</span><span class="sxs-lookup"><span data-stu-id="abc1e-104">Microsoft BitLocker Administration and Monitoring (MBAM) Server features for the Stand-alone topology can be installed in different configurations on two or more servers in a production environment.</span></span> <span data-ttu-id="abc1e-105">Die empfohlene Konfiguration sind zwei Server für eine Produktionsumgebung, je nach Ihren Skalierbarkeitsanforderungen.</span><span class="sxs-lookup"><span data-stu-id="abc1e-105">The recommended configuration is two servers for a production environment, depending on your scalability requirements.</span></span> <span data-ttu-id="abc1e-106">Verwenden Sie einen einzelnen Server für eine MBAM-Installation nur in Testumgebungen.</span><span class="sxs-lookup"><span data-stu-id="abc1e-106">Use a single server for an MBAM installation only in test environments.</span></span> <span data-ttu-id="abc1e-107">Weitere Informationen zum Planen der Bereitstellung von MBAM Server Features finden Sie unter [Planen der MBAM 2,0-Server Bereitstellung](planning-for-mbam-20-server-deployment-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="abc1e-107">For more information about planning for the MBAM Server feature deployment, see [Planning for MBAM 2.0 Server Deployment](planning-for-mbam-20-server-deployment-mbam-2.md).</span></span>

<span data-ttu-id="abc1e-108">Das folgende Diagramm zeigt ein Beispiel, wie Sie die empfohlene MBAM-Bereitstellung mit zwei Servern konfigurieren können.</span><span class="sxs-lookup"><span data-stu-id="abc1e-108">The following diagram shows an example of how you can configure the recommended two-server MBAM deployment.</span></span> <span data-ttu-id="abc1e-109">Mit dieser Konfiguration werden bis zu 200.000 MBAM-Clients in einer Produktionsumgebung unterstützt.</span><span class="sxs-lookup"><span data-stu-id="abc1e-109">This configuration supports up to 200,000 MBAM clients in a production environment.</span></span> <span data-ttu-id="abc1e-110">Die Server Features und-Datenbanken im Architektur Bild werden im folgenden Abschnitt beschrieben und unter dem Computer oder Server aufgelistet, auf dem wir die Installation empfehlen.</span><span class="sxs-lookup"><span data-stu-id="abc1e-110">The server features and databases in the architecture image are described in the following section and are listed under the computer or server where we recommend that you install them.</span></span>

![mbam 2 2-Server Bereitstellungstopologie](images/mbam2-3-servers.gif)

## <span data-ttu-id="abc1e-112">Verwaltungs-und Überwachungs Server</span><span class="sxs-lookup"><span data-stu-id="abc1e-112">Administration and Monitoring Server</span></span>


<span data-ttu-id="abc1e-113">Die folgenden Features sind auf diesem Server installiert:</span><span class="sxs-lookup"><span data-stu-id="abc1e-113">The following features are installed on this server:</span></span>

-   <span data-ttu-id="abc1e-114">**Verwaltungs-und Überwachungs Server**.</span><span class="sxs-lookup"><span data-stu-id="abc1e-114">**Administration and Monitoring Server**.</span></span> <span data-ttu-id="abc1e-115">Die Verwaltungs-und Überwachungs Server Funktion ist auf einem Windows-Server installiert und besteht aus der Helpdesk-Website und den Überwachungs-Webdiensten.</span><span class="sxs-lookup"><span data-stu-id="abc1e-115">The Administration and Monitoring Server feature is installed on a Windows server and consists of the Help Desk website and the monitoring web services.</span></span>

-   <span data-ttu-id="abc1e-116">**Self-Service-Portal**.</span><span class="sxs-lookup"><span data-stu-id="abc1e-116">**Self-Service Portal**.</span></span> <span data-ttu-id="abc1e-117">Das Self-Service-Portal ist auf einem Windows-Server installiert.</span><span class="sxs-lookup"><span data-stu-id="abc1e-117">The Self-Service Portal is installed on a Windows server.</span></span> <span data-ttu-id="abc1e-118">Das Self-Service-Portal ermöglicht Endbenutzern auf Clientcomputern die unabhängige Anmeldung bei einer Website, auf der Sie einen Wiederherstellungsschlüssel zum Wiederherstellen eines gesperrten BitLocker-Volumes abrufen können.</span><span class="sxs-lookup"><span data-stu-id="abc1e-118">The Self-Service Portal enables end users on client computers to independently log on to a website, where they can obtain a recovery key to recover a locked BitLocker volume.</span></span>

## <span data-ttu-id="abc1e-119">Daten Bank Server</span><span class="sxs-lookup"><span data-stu-id="abc1e-119">Database Server</span></span>


<span data-ttu-id="abc1e-120">Die folgenden Features sind auf diesem Server installiert:</span><span class="sxs-lookup"><span data-stu-id="abc1e-120">The following features are installed on this server:</span></span>

-   <span data-ttu-id="abc1e-121">**Wiederherstellungsdatenbank**.</span><span class="sxs-lookup"><span data-stu-id="abc1e-121">**Recovery Database**.</span></span> <span data-ttu-id="abc1e-122">Die Wiederherstellungsdatenbank ist auf einem Windows-Server und einer unterstützten Instanz von Microsoft SQLServer installiert.</span><span class="sxs-lookup"><span data-stu-id="abc1e-122">The Recovery Database is installed on a Windows server and a supported instance of Microsoft SQLServer.</span></span> <span data-ttu-id="abc1e-123">In dieser Datenbank werden Wiederherstellungsdaten gespeichert, die von MBAM-Clientcomputern erfasst werden.</span><span class="sxs-lookup"><span data-stu-id="abc1e-123">This database stores recovery data that is collected from MBAM client computers.</span></span>

-   <span data-ttu-id="abc1e-124">**Konformitäts-und Überwachungsdatenbank**.</span><span class="sxs-lookup"><span data-stu-id="abc1e-124">**Compliance and Audit Database**.</span></span> <span data-ttu-id="abc1e-125">Die Compliance-und Überwachungsdatenbank ist auf einem Windows-Server und einer unterstützten Instanz von SQLServer installiert.</span><span class="sxs-lookup"><span data-stu-id="abc1e-125">The Compliance and Audit Database is installed on a Windows server and a supported instance of SQLServer.</span></span> <span data-ttu-id="abc1e-126">In dieser Datenbank werden Kompatibilitätsdaten für MBAM-Clientcomputer gespeichert.</span><span class="sxs-lookup"><span data-stu-id="abc1e-126">This database stores compliance data for MBAM client computers.</span></span> <span data-ttu-id="abc1e-127">Diese Daten werden hauptsächlich für Berichte verwendet, die von SQL Server Reporting Services (SSRS) gehostet werden.</span><span class="sxs-lookup"><span data-stu-id="abc1e-127">This data is used primarily for reports that SQL Server Reporting Services (SSRS) hosts.</span></span>

-   <span data-ttu-id="abc1e-128">**Konformitäts-und Überwachungsberichte**.</span><span class="sxs-lookup"><span data-stu-id="abc1e-128">**Compliance and Audit Reports**.</span></span> <span data-ttu-id="abc1e-129">Die Kompatibilitäts-und Überwachungsberichte sind auf einem Windows-Server und einer unterstützten Instanz von SQLServer installiert, auf der das Feature SQL Server Reporting Services (SSRS) installiert ist.</span><span class="sxs-lookup"><span data-stu-id="abc1e-129">The Compliance and Audit Reports are installed on a Windows server and a supported instance of SQLServer that has the SQL Server Reporting Services (SSRS) feature installed.</span></span> <span data-ttu-id="abc1e-130">Diese Berichte enthalten MBAM-Berichte, auf die Sie über die Helpdesk-Website oder direkt vom SSRS-Server aus zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="abc1e-130">These reports provide MBAM reports that you can access from the Help Desk website or directly from the SSRS server.</span></span>

## <span data-ttu-id="abc1e-131">Verwaltungsarbeitsstation</span><span class="sxs-lookup"><span data-stu-id="abc1e-131">Management Workstation</span></span>


<span data-ttu-id="abc1e-132">Das folgende Feature ist auf der Verwaltungsarbeitsstation installiert, die ein Windows-Server oder ein Clientcomputer sein kann.</span><span class="sxs-lookup"><span data-stu-id="abc1e-132">The following feature is installed on the Management Workstation, which can be a Windows server or a client computer.</span></span>

-   <span data-ttu-id="abc1e-133">**Richtlinienvorlage**aus.</span><span class="sxs-lookup"><span data-stu-id="abc1e-133">**Policy Template**.</span></span> <span data-ttu-id="abc1e-134">Die Richtlinienvorlage besteht aus Gruppenrichtlinien, die MBAM-Implementierungs Einstellungen für die BitLocker-Laufwerkverschlüsselung definieren.</span><span class="sxs-lookup"><span data-stu-id="abc1e-134">The Policy Template consists of Group Policies that define MBAM implementation settings for BitLocker drive encryption.</span></span> <span data-ttu-id="abc1e-135">Sie können die Richtlinienvorlage auf einem beliebigen Server oder auf einer Arbeitsstation installieren, Sie wird jedoch häufig auf einer Verwaltungsarbeitsstation installiert, die ein unterstützter Windows-Server oder-Clientcomputer ist.</span><span class="sxs-lookup"><span data-stu-id="abc1e-135">You can install the Policy template on any server or workstation, but it is commonly installed on a management workstation, which is a supported Windows server or client computer.</span></span> <span data-ttu-id="abc1e-136">Die Workstation muss kein dedizierter Computer sein.</span><span class="sxs-lookup"><span data-stu-id="abc1e-136">The workstation does not have to be a dedicated computer.</span></span>

## <a href="" id="---------mbam-client"></a> <span data-ttu-id="abc1e-137">MBAM-Client</span><span class="sxs-lookup"><span data-stu-id="abc1e-137">MBAM Client</span></span>


<span data-ttu-id="abc1e-138">Der MBAM-Client ist auf einem Windows-Computer installiert und weist die folgenden Merkmale auf:</span><span class="sxs-lookup"><span data-stu-id="abc1e-138">The MBAM Client is installed on a Windows computer and has the following characteristics:</span></span>

-   <span data-ttu-id="abc1e-139">Verwendet Gruppenrichtlinien, um die BitLocker-Laufwerkverschlüsselung von Clientcomputern im Unternehmen zu erzwingen.</span><span class="sxs-lookup"><span data-stu-id="abc1e-139">Uses Group Policy to enforce the BitLocker drive encryption of client computers in the enterprise.</span></span>

-   <span data-ttu-id="abc1e-140">Sammelt den Wiederherstellungsschlüssel für die drei BitLocker-Datenlaufwerk Typen: Betriebssystemlaufwerke, fest Netzlaufwerke und austauschbare Datenlaufwerke (USB).</span><span class="sxs-lookup"><span data-stu-id="abc1e-140">Collects the recovery key for the three BitLocker data drive types: operating system drives, fixed data drives, and removable data (USB) drives.</span></span>

-   <span data-ttu-id="abc1e-141">Sammelt Kompatibilitätsdaten für den Computer und übergibt die Daten an das Berichterstattungssystem.</span><span class="sxs-lookup"><span data-stu-id="abc1e-141">Collects compliance data for the computer and passes the data to the reporting system.</span></span>

## <span data-ttu-id="abc1e-142">Weitere Ressourcen für die Bereitstellung von MBAM 2,0-Server Features</span><span class="sxs-lookup"><span data-stu-id="abc1e-142">Other Resources for Deploying MBAM 2.0 Server Features</span></span>


[<span data-ttu-id="abc1e-143">Bereitstellen von MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="abc1e-143">Deploying MBAM 2.0</span></span>](deploying-mbam-20-mbam-2.md)

 

 





