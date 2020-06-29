---
title: Aktualisieren von MBAM 2,5 auf MBAM 2,5 SP1-Update zur Wartungsversion
author: dansimp
ms.author: ksharma
manager: miaposto
audience: ITPro
ms.topic: article
ms.prod: w10
ms.localizationpriority: Normal
ms.openlocfilehash: 372822e1ec049871c62af9f429290b88bbfac949
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804475"
---
# <span data-ttu-id="0eb55-102">Upgrade von MBAM 2,5 auf MBAM 2,5 SP1-Update zur Wartungsversion</span><span class="sxs-lookup"><span data-stu-id="0eb55-102">Upgrade from MBAM 2.5 to MBAM 2.5 SP1 Servicing Release Update</span></span>

<span data-ttu-id="0eb55-103">In diesem Artikel finden Sie Schritt-für-Schritt-Anleitungen zum Upgrade von Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) 2,5 auf MBAM 2,5 Service Pack 1 (SP1) zusammen mit dem [Microsoft Desktop Optimization Pack (MDOP)-Update](https://support.microsoft.com/help/4505175/may-2019-servicing-release-for-microsoft-desktop-optimization-pack) für die Wartung von 2019 in einer eigenständigen Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="0eb55-103">This article provides step-by-step instructions to upgrade Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 to MBAM 2.5 Service Pack 1 (SP1) together with the [Microsoft Desktop Optimization Pack (MDOP) May 2019 servicing update](https://support.microsoft.com/help/4505175/may-2019-servicing-release-for-microsoft-desktop-optimization-pack) in a standalone configuration.</span></span>

<span data-ttu-id="0eb55-104">In diesem Leitfaden wird eine Konfiguration mit zwei Servern verwendet.</span><span class="sxs-lookup"><span data-stu-id="0eb55-104">In this guide, we will use a two-server configuration.</span></span> <span data-ttu-id="0eb55-105">Bei einem Server handelt es sich um einen Datenbankserver, auf dem Microsoft SQL Server 2016 ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0eb55-105">One server will be a database server that's running Microsoft SQL Server 2016.</span></span> <span data-ttu-id="0eb55-106">Dieser Server hostet die MBAM-Datenbanken und-Berichte.</span><span class="sxs-lookup"><span data-stu-id="0eb55-106">This server will host the MBAM databases and reports.</span></span> <span data-ttu-id="0eb55-107">Der andere Server ist ein Windows Server 2012 R2-Webserver.</span><span class="sxs-lookup"><span data-stu-id="0eb55-107">The other server will be a Windows Server 2012 R2 web server.</span></span> <span data-ttu-id="0eb55-108">Auf diesem Server werden "Verwaltung und Überwachung" und "Self-Service-Portal" gehostet.</span><span class="sxs-lookup"><span data-stu-id="0eb55-108">This server will host "Administration and Monitoring" and "Self-Service Portal."</span></span>

## <span data-ttu-id="0eb55-109">Vorbereiten des Upgrades von MBAM 2,5 SP1</span><span class="sxs-lookup"><span data-stu-id="0eb55-109">Prepare to upgrade MBAM 2.5 SP1</span></span>

### <span data-ttu-id="0eb55-110">Kennen Sie die MBAM-Server in Ihrer Umgebung</span><span class="sxs-lookup"><span data-stu-id="0eb55-110">Know the MBAM servers in your environment</span></span>

1. <span data-ttu-id="0eb55-111">SQL Server-Datenbankmodul: Server, der die MBAM-Datenbanken hostet.</span><span class="sxs-lookup"><span data-stu-id="0eb55-111">SQL Server Database Engine: Server that hosts the MBAM databases.</span></span>
2. <span data-ttu-id="0eb55-112">SQL Server Reporting Services: Server, der die MBAM-Berichte hostet.</span><span class="sxs-lookup"><span data-stu-id="0eb55-112">SQL Server Reporting Services: Server that hosts the MBAM reports.</span></span>
3. <span data-ttu-id="0eb55-113">Internetinformationsdienste (IIS)-Webservern: Server, auf dem MBAM-Webanwendungen und MBAM-Dienste gehostet werden.</span><span class="sxs-lookup"><span data-stu-id="0eb55-113">Internet Information Services (IIS) web servers: Server that hosts MBAM Web Applications and MBAM services.</span></span>
4. <span data-ttu-id="0eb55-114">Optional Microsoft System Center Configuration Manager-Primärer Standortserver: die MBAM-Konfigurationsanwendung wird auf diesem Server ausgeführt, um MBAM-Berichte mit Configuration Manager zu integrieren.</span><span class="sxs-lookup"><span data-stu-id="0eb55-114">(Optional) Microsoft System Center Configuration Manager primary site server: The MBAM configuration application is run on this server to integrate MBAM reports with Configuration Manager.</span></span> <span data-ttu-id="0eb55-115">Diese Berichte werden dann mit vorhandenen Configuration Manager-Berichten in der Configuration Manager-Instanz von SQL Server Reporting Services (SSRS) zusammengeführt.</span><span class="sxs-lookup"><span data-stu-id="0eb55-115">These reports are then merged with existing Configuration Manager reports on the Configuration Manager SQL Server Reporting Services (SSRS) instance.</span></span>

### <span data-ttu-id="0eb55-116">Identifizieren von Dienstkonten, Gruppen, Servername und Berichts-URL</span><span class="sxs-lookup"><span data-stu-id="0eb55-116">Identify service accounts, groups, server name, and reports URL</span></span>

1. <span data-ttu-id="0eb55-117">Identifizieren Sie das MBAM-Anwendungspooldienst Konto, das von IIS-Webservern zum Lesen und Schreiben von Daten in MBAM-Datenbanken verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0eb55-117">Identify the MBAM application pool service account that's used by IIS web servers to read and write data to MBAM databases.</span></span>
2. <span data-ttu-id="0eb55-118">Identifizieren Sie die Gruppen, die während der Konfiguration von MBAM Web Features verwendet werden, und die URL des Berichtsweb Diensts.</span><span class="sxs-lookup"><span data-stu-id="0eb55-118">Identify the groups that are used during the MBAM web features configuration and the reports web service URL.</span></span>
3. <span data-ttu-id="0eb55-119">Ermitteln Sie den Namen und den Instanznamen von SQL Server.</span><span class="sxs-lookup"><span data-stu-id="0eb55-119">Identify the SQL Server name and instance name.</span></span> <span data-ttu-id="0eb55-120">Schauen Sie sich dieses Video an, um weitere Informationen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="0eb55-120">Watch this video to learn more.</span></span>

    > [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE3ANP1]

4. <span data-ttu-id="0eb55-121">Identifizieren Sie das SQL Server Reporting Services-Konto, das zum Lesen von Kompatibilitätsdaten aus der Compliance-und Überwachungsdatenbank verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0eb55-121">Identify the SQL Server Reporting Services Account that's used for reading compliance data from the Compliance and Audit database.</span></span> <span data-ttu-id="0eb55-122">Schauen Sie sich dieses Video an, um weitere Informationen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="0eb55-122">Watch this video to learn more.</span></span>

    > [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE3ALdZ]

## <span data-ttu-id="0eb55-123">Upgrade der MBAM-Infrastruktur auf die neueste verfügbare Version</span><span class="sxs-lookup"><span data-stu-id="0eb55-123">Upgrade the MBAM infrastructure to the latest version available</span></span>

<span data-ttu-id="0eb55-124">Die Installation oder das Upgrade der MBAM-Server Infrastruktur erfolgt immer in der nachstehend aufgeführten Reihenfolge:</span><span class="sxs-lookup"><span data-stu-id="0eb55-124">MBAM Server infrastructure installation or upgrade is always performed in the order listed below:</span></span>

- <span data-ttu-id="0eb55-125">SQL Server-Datenbankmodul: Datenbanken</span><span class="sxs-lookup"><span data-stu-id="0eb55-125">SQL Server Database Engine: Databases</span></span>
- <span data-ttu-id="0eb55-126">SQL Server Reporting Services: Berichte</span><span class="sxs-lookup"><span data-stu-id="0eb55-126">SQL Server Reporting Services: Reports</span></span>
- <span data-ttu-id="0eb55-127">Webserver: Webanwendungen</span><span class="sxs-lookup"><span data-stu-id="0eb55-127">Web Server: Web Applications</span></span>
- <span data-ttu-id="0eb55-128">SCCM-Server: in SCCM integrierte Berichte (falls zutreffend)</span><span class="sxs-lookup"><span data-stu-id="0eb55-128">SCCM Server: SCCM Integrated Reports if applicable</span></span>
- <span data-ttu-id="0eb55-129">Clients: MBAM-Agent oder Client Update</span><span class="sxs-lookup"><span data-stu-id="0eb55-129">Clients: MBAM Agent or Client Update</span></span>
- <span data-ttu-id="0eb55-130">Vorlagen für Gruppenrichtlinien: Aktualisieren Sie die vorhandene Gruppenrichtlinie mit neuen Vorlagen, und aktivieren Sie neue Einstellungen für vorhandene MBAM-Gruppenrichtlinien.</span><span class="sxs-lookup"><span data-stu-id="0eb55-130">Group Policy Templates: Update the existing Group Policy with new templates and enable new settings on existing MBAM Group Policy</span></span>

> [!NOTE]
> <span data-ttu-id="0eb55-131">Wir empfehlen, dass Sie vor dem Ausführen der Upgrades eine vollständige Datenbanksicherung der MBAM-Datenbankenerstellen.</span><span class="sxs-lookup"><span data-stu-id="0eb55-131">We recommend that you create a full database backup of the MBAM databases before you run the upgrades.</span></span>

### <span data-ttu-id="0eb55-132">Aktualisieren des MBAM SQL Server</span><span class="sxs-lookup"><span data-stu-id="0eb55-132">Upgrade the MBAM SQL Server</span></span>

<span data-ttu-id="0eb55-133">Schauen Sie sich dieses Video an, um zu erfahren, wie Sie den MBAM SQL Server aktualisieren:</span><span class="sxs-lookup"><span data-stu-id="0eb55-133">Watch this video to learn how to upgrade the MBAM SQL Server:</span></span>

   > [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE3ALew]

### <span data-ttu-id="0eb55-134">Aktualisieren des MBAM-Webservers</span><span class="sxs-lookup"><span data-stu-id="0eb55-134">Upgrade the MBAM Web Server</span></span>

<span data-ttu-id="0eb55-135">Schauen Sie sich dieses Video an, um zu erfahren, wie Sie den MBAM-Webserver aktualisieren:</span><span class="sxs-lookup"><span data-stu-id="0eb55-135">Watch this video to learn how to upgrade the MBAM Web Server:</span></span>

   > [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE3ALex]

## <span data-ttu-id="0eb55-136">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="0eb55-136">More information</span></span>

<span data-ttu-id="0eb55-137">Weitere Informationen zu bekannten Problemen in MBAM 2,5 SP1 finden Sie unter [Anmerkungen zu dieser Version von MBAM 2,5 SP1](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/release-notes-for-mbam-25-sp1).</span><span class="sxs-lookup"><span data-stu-id="0eb55-137">For more information about known issues in MBAM 2.5 SP1, see [Release Notes for MBAM 2.5 SP1](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/release-notes-for-mbam-25-sp1).</span></span>
