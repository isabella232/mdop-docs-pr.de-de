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
ms.openlocfilehash: 19da3df0976b51700e0d10c302a31421a88d17e4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804457"
---
# <span data-ttu-id="c3cfc-103">Aktualisieren von MBAM 2.5 auf MBAM 2.5 SP1</span><span class="sxs-lookup"><span data-stu-id="c3cfc-103">Upgrading to MBAM 2.5 SP1 from MBAM 2.5</span></span>
<span data-ttu-id="c3cfc-104">In diesem Thema wird beschrieben, wie Sie den Microsoft BitLocker-Verwaltungs-und-Überwachungs Server (MBAM) 2,5 und den MBAM-Client von 2,5 auf MBAM 2,5 SP1 aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="c3cfc-104">This topic describes the process for upgrading the Microsoft BitLocker Administration and Monitoring (MBAM) Server 2.5 and the MBAM Client from 2.5 to MBAM 2.5 SP1.</span></span>

### <span data-ttu-id="c3cfc-105">Vorbemerkungen</span><span class="sxs-lookup"><span data-stu-id="c3cfc-105">Before you begin</span></span>
#### <span data-ttu-id="c3cfc-106">Herunterladen der Service Version vom Mai 2019</span><span class="sxs-lookup"><span data-stu-id="c3cfc-106">Download the May 2019 servicing release</span></span>
[<span data-ttu-id="c3cfc-107">Desktop Optimierungspaket</span><span class="sxs-lookup"><span data-stu-id="c3cfc-107">Desktop Optimization Pack</span></span>](https://www.microsoft.com/download/details.aspx?id=58345)

#### <span data-ttu-id="c3cfc-108">Überprüfen der Installationsdokumentation</span><span class="sxs-lookup"><span data-stu-id="c3cfc-108">Verify the installation documentaion</span></span>
<span data-ttu-id="c3cfc-109">Stellen Sie sicher, dass Sie über eine aktuelle Dokumentation Ihrer MBAM-Umgebung verfügen, einschließlich aller Servernamen, Datenbanknamen, Dienstkonten und deren Kennwörter.</span><span class="sxs-lookup"><span data-stu-id="c3cfc-109">Verify you have a current documentation of your MBAM environment, including all server names, database names, service accounts and their passwords.</span></span>

### <span data-ttu-id="c3cfc-110">Upgrade-Schritte</span><span class="sxs-lookup"><span data-stu-id="c3cfc-110">Upgrade steps</span></span>
#### <span data-ttu-id="c3cfc-111">Schritte zum Upgrade der MBAM-Datenbank (SQL Server)</span><span class="sxs-lookup"><span data-stu-id="c3cfc-111">Steps to upgrade the MBAM Database (SQL Server)</span></span>
1. <span data-ttu-id="c3cfc-112">Verwenden des MBAM-Konfigurators; Entfernen Sie die Rolle "Berichte" aus dem SQL Server oder unabhängig davon, wo die SSRS-Datenbank gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="c3cfc-112">Using the MBAM Configurator; remove the Reports role from the SQL server, or wherever the SSRS database is hosted.</span></span> <span data-ttu-id="c3cfc-113">Je nach Umgebung kann es sich um denselben Server oder eine separate Person handeln.</span><span class="sxs-lookup"><span data-stu-id="c3cfc-113">Depending on your environment, this can be the same server or a separate one.</span></span>
  > [!NOTE]
  > <span data-ttu-id="c3cfc-114">Es wird keine Option zum Entfernen der Datenbanken angezeigt. Dies wird erwartet.</span><span class="sxs-lookup"><span data-stu-id="c3cfc-114">You will not see an option to remove the Databases; this is expected.</span></span>  
2. <span data-ttu-id="c3cfc-115">Installieren Sie 2,5 SP1 (mit dem MDOP-Microsoft-Desktop Optimierungspaket 2015 auf der Volumen Lizenzierungs-Service Center-Website:</span><span class="sxs-lookup"><span data-stu-id="c3cfc-115">Install 2.5 SP1(Located with MDOP - Microsoft Desktop Optimization Pack 2015 from the Volume Licensing Service Center site:</span></span>  <https://www.microsoft.com/Licensing/servicecenter/default.aspx>
3. <span data-ttu-id="c3cfc-116">Zu diesem Zeitpunkt keine Konfiguration vornehmen</span><span class="sxs-lookup"><span data-stu-id="c3cfc-116">Do not configure it at this time</span></span> 
4. <span data-ttu-id="c3cfc-117">Verwenden des MBAM-Konfigurators; erneutes Hinzufügen der Rolle "Berichte"</span><span class="sxs-lookup"><span data-stu-id="c3cfc-117">Using the MBAM Configurator; re-add the Reports role</span></span>
5. <span data-ttu-id="c3cfc-118">Verwenden des MBAM-Konfigurators; erneutes Hinzufügen der SQL-Datenbankrolle auf dem SQL Server</span><span class="sxs-lookup"><span data-stu-id="c3cfc-118">Using the MBAM Configurator; re-add the SQL Database role on the SQL Server</span></span>
6. <span data-ttu-id="c3cfc-119">Am Ende wird eine Warnung angezeigt, dass die DBS bereits vorhanden sind und nicht erstellt wurden, dies wird jedoch erwartet.</span><span class="sxs-lookup"><span data-stu-id="c3cfc-119">At the end, you will be warned that the DBs already exist and  weren’t created, but this is expected</span></span>
7. <span data-ttu-id="c3cfc-120">Durch diesen Vorgang werden die vorhandenen Datenbanken auf die aktuelle Version aktualisiert, die installiert wird.</span><span class="sxs-lookup"><span data-stu-id="c3cfc-120">This process updates the existing databases to the current version being installed.</span></span>              

#### <span data-ttu-id="c3cfc-121">Schritte zum Upgrade des MBAM-Servers (mit MBAM und IIS)</span><span class="sxs-lookup"><span data-stu-id="c3cfc-121">Steps to upgrade the MBAM Server (Running MBAM and IIS)</span></span>
1. <span data-ttu-id="c3cfc-122">Verwenden des MBAM-Konfigurators; Entfernen der Administrator-und Self-Service-Portale vom IIS-Server</span><span class="sxs-lookup"><span data-stu-id="c3cfc-122">Using the MBAM Configurator; remove the Admin and Self Service Portals from  the IIS server</span></span>
2. <span data-ttu-id="c3cfc-123">Installieren von MBAM 2,5 SP1</span><span class="sxs-lookup"><span data-stu-id="c3cfc-123">Install MBAM 2.5 SP1</span></span>
3. <span data-ttu-id="c3cfc-124">Zu diesem Zeitpunkt keine Konfiguration vornehmen</span><span class="sxs-lookup"><span data-stu-id="c3cfc-124">Do not configure it at this time</span></span>  
4. <span data-ttu-id="c3cfc-125">Verwenden des MBAM-Konfigurators; erneutes Hinzufügen der Administrator-und Self Service-Portale zum IIS-Server</span><span class="sxs-lookup"><span data-stu-id="c3cfc-125">Using the MBAM Configurator; re-add the Admin and Self Service Portals to the IIS server</span></span> 
5. <span data-ttu-id="c3cfc-126">Öffnen Sie eine Eingabeaufforderung mit erhöhten Rechten, geben Sie **iisreset**ein, und drücken Sie die EINGABETASTE.</span><span class="sxs-lookup"><span data-stu-id="c3cfc-126">Open an elevated command prompt, type **IISRESET**, and hit Enter.</span></span>
 
#### <span data-ttu-id="c3cfc-127">Schritte zum Upgrade der MBAM-Clients/-Endpunkte</span><span class="sxs-lookup"><span data-stu-id="c3cfc-127">Steps to upgrade the MBAM Clients/Endpoints</span></span>
1. <span data-ttu-id="c3cfc-128">Deinstallieren des 2,5-Agents aus Clientendpunkten</span><span class="sxs-lookup"><span data-stu-id="c3cfc-128">Uninstall the 2.5 Agent from client endpoints</span></span>
2. <span data-ttu-id="c3cfc-129">Installieren des 2,5 SP1-Agents auf den Clientendpunkten</span><span class="sxs-lookup"><span data-stu-id="c3cfc-129">Install the 2.5 SP1 Agent on the client endpoints</span></span>
3. <span data-ttu-id="c3cfc-130">Pushen des Client Updates für das 2019-Rollup für Mai auf Clients mit dem 2,5 SP1-Agent</span><span class="sxs-lookup"><span data-stu-id="c3cfc-130">Push out the May 2019 Rollup Client update to clients running the 2.5 SP1 Agent</span></span> 
4. <span data-ttu-id="c3cfc-131">Es ist nicht erforderlich, den vorhandenen Client vor der Installation des 2019-Rollups für Mai zu deinstallieren.</span><span class="sxs-lookup"><span data-stu-id="c3cfc-131">There is no need to uninstall the existing client prior to installing the May 2019 Rollup.</span></span>  
