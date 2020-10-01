---
title: Aktualisieren von MBAM 2.5 auf MBAM 2.5 SP1
description: Aktualisieren von MBAM 2.5 auf MBAM 2.5 SP1
author: dansimp
ms.assetid: ''
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 2/16/2018
ms.openlocfilehash: 330ded822dd9da96a1c33eabcb31d744044dc28e
ms.sourcegitcommit: ae34c5cb5e7979b472b257a4691142e493d5d6fe
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/30/2020
ms.locfileid: "11091620"
---
# <span data-ttu-id="93ba8-103">Aktualisieren von MBAM 2.5 auf MBAM 2.5 SP1</span><span class="sxs-lookup"><span data-stu-id="93ba8-103">Upgrading to MBAM 2.5 SP1 from MBAM 2.5</span></span>
<span data-ttu-id="93ba8-104">In diesem Thema wird beschrieben, wie Sie den Microsoft BitLocker-Verwaltungs-und-Überwachungs Server (MBAM) 2,5 und den MBAM-Client von 2,5 auf MBAM 2,5 SP1 aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="93ba8-104">This topic describes the process for upgrading the Microsoft BitLocker Administration and Monitoring (MBAM) Server 2.5 and the MBAM Client from 2.5 to MBAM 2.5 SP1.</span></span>

### <span data-ttu-id="93ba8-105">Vorbemerkungen</span><span class="sxs-lookup"><span data-stu-id="93ba8-105">Before you begin</span></span>
#### <span data-ttu-id="93ba8-106">Herunterladen der Service Version vom Mai 2019</span><span class="sxs-lookup"><span data-stu-id="93ba8-106">Download the May 2019 servicing release</span></span>
[<span data-ttu-id="93ba8-107">Desktop Optimierungspaket</span><span class="sxs-lookup"><span data-stu-id="93ba8-107">Desktop Optimization Pack</span></span>](https://www.microsoft.com/download/details.aspx?id=58345)

#### <span data-ttu-id="93ba8-108">Herunterladen der Service Version vom Juli 2018</span><span class="sxs-lookup"><span data-stu-id="93ba8-108">Download the July 2018 servicing release</span></span>
[<span data-ttu-id="93ba8-109">Desktop Optimierungspaket</span><span class="sxs-lookup"><span data-stu-id="93ba8-109">Desktop Optimization Pack</span></span>](https://www.microsoft.com/download/details.aspx?id=57157)


#### <span data-ttu-id="93ba8-110">Überprüfen der Installationsdokumentation</span><span class="sxs-lookup"><span data-stu-id="93ba8-110">Verify the installation documentaion</span></span>
<span data-ttu-id="93ba8-111">Stellen Sie sicher, dass Sie über eine aktuelle Dokumentation Ihrer MBAM-Umgebung verfügen, einschließlich aller Servernamen, Datenbanknamen, Dienstkonten und deren Kennwörter.</span><span class="sxs-lookup"><span data-stu-id="93ba8-111">Verify you have a current documentation of your MBAM environment, including all server names, database names, service accounts and their passwords.</span></span>

### <span data-ttu-id="93ba8-112">Upgrade-Schritte</span><span class="sxs-lookup"><span data-stu-id="93ba8-112">Upgrade steps</span></span>
#### <span data-ttu-id="93ba8-113">Schritte zum Upgrade der MBAM-Datenbank (SQL Server)</span><span class="sxs-lookup"><span data-stu-id="93ba8-113">Steps to upgrade the MBAM Database (SQL Server)</span></span>
1. <span data-ttu-id="93ba8-114">Verwenden des MBAM-Konfigurators; Entfernen Sie die Rolle "Berichte" aus dem SQL Server oder unabhängig davon, wo die SSRS-Datenbank gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="93ba8-114">Using the MBAM Configurator; remove the Reports role from the SQL server, or wherever the SSRS database is hosted.</span></span> <span data-ttu-id="93ba8-115">Je nach Umgebung kann es sich um denselben Server oder eine separate Person handeln.</span><span class="sxs-lookup"><span data-stu-id="93ba8-115">Depending on your environment, this can be the same server or a separate one.</span></span>
  > [!NOTE]
  > <span data-ttu-id="93ba8-116">Es wird keine Option zum Entfernen der Datenbanken angezeigt. Dies wird erwartet.</span><span class="sxs-lookup"><span data-stu-id="93ba8-116">You will not see an option to remove the Databases; this is expected.</span></span>  
2. <span data-ttu-id="93ba8-117">Installieren Sie 2,5 SP1 (mit dem MDOP-Microsoft-Desktop Optimierungspaket 2015 auf der Volumen Lizenzierungs-Service Center-Website:</span><span class="sxs-lookup"><span data-stu-id="93ba8-117">Install 2.5 SP1(Located with MDOP - Microsoft Desktop Optimization Pack 2015 from the Volume Licensing Service Center site:</span></span>  <https://www.microsoft.com/Licensing/servicecenter/default.aspx>
3. <span data-ttu-id="93ba8-118">Zu diesem Zeitpunkt keine Konfiguration vornehmen</span><span class="sxs-lookup"><span data-stu-id="93ba8-118">Do not configure it at this time</span></span> 
4. <span data-ttu-id="93ba8-119">Verwenden des MBAM-Konfigurators; erneutes Hinzufügen der Rolle "Berichte"</span><span class="sxs-lookup"><span data-stu-id="93ba8-119">Using the MBAM Configurator; re-add the Reports role</span></span>
5. <span data-ttu-id="93ba8-120">Verwenden des MBAM-Konfigurators; erneutes Hinzufügen der SQL-Datenbankrolle auf dem SQL Server</span><span class="sxs-lookup"><span data-stu-id="93ba8-120">Using the MBAM Configurator; re-add the SQL Database role on the SQL Server</span></span>
6. <span data-ttu-id="93ba8-121">Am Ende wird eine Warnung angezeigt, dass die DBS bereits vorhanden sind und nicht erstellt wurden, dies wird jedoch erwartet.</span><span class="sxs-lookup"><span data-stu-id="93ba8-121">At the end, you will be warned that the DBs already exist and  weren’t created, but this is expected</span></span>
7. <span data-ttu-id="93ba8-122">Durch diesen Vorgang werden die vorhandenen Datenbanken auf die aktuelle Version aktualisiert, die installiert wird.</span><span class="sxs-lookup"><span data-stu-id="93ba8-122">This process updates the existing databases to the current version being installed.</span></span>              

#### <span data-ttu-id="93ba8-123">Schritte zum Upgrade des MBAM-Servers (mit MBAM und IIS)</span><span class="sxs-lookup"><span data-stu-id="93ba8-123">Steps to upgrade the MBAM Server (Running MBAM and IIS)</span></span>
1. <span data-ttu-id="93ba8-124">Verwenden des MBAM-Konfigurators; Entfernen der Administrator-und Self-Service-Portale vom IIS-Server</span><span class="sxs-lookup"><span data-stu-id="93ba8-124">Using the MBAM Configurator; remove the Admin and Self Service Portals from  the IIS server</span></span>
2. <span data-ttu-id="93ba8-125">Installieren von MBAM 2,5 SP1</span><span class="sxs-lookup"><span data-stu-id="93ba8-125">Install MBAM 2.5 SP1</span></span>
3. <span data-ttu-id="93ba8-126">Zu diesem Zeitpunkt keine Konfiguration vornehmen</span><span class="sxs-lookup"><span data-stu-id="93ba8-126">Do not configure it at this time</span></span>  
4. <span data-ttu-id="93ba8-127">Verwenden des MBAM-Konfigurators; erneutes Hinzufügen der Administrator-und Self Service-Portale zum IIS-Server</span><span class="sxs-lookup"><span data-stu-id="93ba8-127">Using the MBAM Configurator; re-add the Admin and Self Service Portals to the IIS server</span></span> 
5. <span data-ttu-id="93ba8-128">Öffnen Sie eine Eingabeaufforderung mit erhöhten Rechten, geben Sie **iisreset**ein, und drücken Sie die EINGABETASTE.</span><span class="sxs-lookup"><span data-stu-id="93ba8-128">Open an elevated command prompt, type **IISRESET**, and hit Enter.</span></span>
 
#### <span data-ttu-id="93ba8-129">Schritte zum Upgrade der MBAM-Clients/-Endpunkte</span><span class="sxs-lookup"><span data-stu-id="93ba8-129">Steps to upgrade the MBAM Clients/Endpoints</span></span>
1. <span data-ttu-id="93ba8-130">Deinstallieren des 2,5-Agents aus Clientendpunkten</span><span class="sxs-lookup"><span data-stu-id="93ba8-130">Uninstall the 2.5 Agent from client endpoints</span></span>
2. <span data-ttu-id="93ba8-131">Installieren des 2,5 SP1-Agents auf den Clientendpunkten</span><span class="sxs-lookup"><span data-stu-id="93ba8-131">Install the 2.5 SP1 Agent on the client endpoints</span></span>
3. <span data-ttu-id="93ba8-132">Pushen des Client Updates für das 2019-Rollup für Mai auf Clients mit dem 2,5 SP1-Agent</span><span class="sxs-lookup"><span data-stu-id="93ba8-132">Push out the May 2019 Rollup Client update to clients running the 2.5 SP1 Agent</span></span> 
4. <span data-ttu-id="93ba8-133">Es ist nicht erforderlich, den vorhandenen Client vor der Installation des 2019-Rollups für Mai zu deinstallieren.</span><span class="sxs-lookup"><span data-stu-id="93ba8-133">There is no need to uninstall the existing client prior to installing the May 2019 Rollup.</span></span>  
