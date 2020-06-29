---
title: Bereitstellen von MBAM 2.0
description: Bereitstellen von MBAM 2.0
author: dansimp
ms.assetid: 4b0eaf10-81b4-427e-9d43-eb833de935a3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ba4423de5306e1ca204ef3b9fd31424bb8f2630f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809976"
---
# <span data-ttu-id="965ae-103">Bereitstellen von MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="965ae-103">Deploying MBAM 2.0</span></span>


<span data-ttu-id="965ae-104">Die Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) unterstützt eine Reihe unterschiedlicher Bereitstellungskonfigurationen.</span><span class="sxs-lookup"><span data-stu-id="965ae-104">Microsoft BitLocker Administration and Monitoring (MBAM) supports a number of different deployment configurations.</span></span> <span data-ttu-id="965ae-105">Dieser Abschnitt enthält Informationen, die Sie über die Bereitstellung von MBAM und Schritt-für-Schritt-Verfahren berücksichtigen sollten, damit Sie die Aufgaben, die Sie in verschiedenen Phasen der Bereitstellung ausführen müssen, erfolgreich durchführen können.</span><span class="sxs-lookup"><span data-stu-id="965ae-105">This section includes information that you should consider about the deployment of MBAM and step-by-step procedures to help you successfully perform the tasks that you must complete at different stages of your deployment.</span></span>

<span data-ttu-id="965ae-106">Sie können MBAM entweder in einer eigenständigen Topologie oder mit einer Topologie bereitstellen, die MBAM mit Microsoft System Center Configuration Manager 2007 oder MicrosoftSystemCenter2012 ConfigurationManager integriert.</span><span class="sxs-lookup"><span data-stu-id="965ae-106">You can deploy MBAM either in a Stand-alone topology, or with a topology that integrates MBAM with Microsoft System Center Configuration Manager 2007 or MicrosoftSystemCenter2012 ConfigurationManager.</span></span> <span data-ttu-id="965ae-107">Informationen zum Installieren von MBAM mit der integrierten Configuration Manager-Topologie finden Sie unter [Verwenden von MBAM mit Configuration Manager](using-mbam-with-configuration-manager.md).</span><span class="sxs-lookup"><span data-stu-id="965ae-107">For information about installing MBAM with the Configuration Manager integrated topology, see [Using MBAM with Configuration Manager](using-mbam-with-configuration-manager.md).</span></span>

## <span data-ttu-id="965ae-108">Bereitstellungsinformationen</span><span class="sxs-lookup"><span data-stu-id="965ae-108">Deployment Information</span></span>


-   [<span data-ttu-id="965ae-109">Bereitstellen der Serverinfrastruktur von MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="965ae-109">Deploying the MBAM 2.0 Server Infrastructure</span></span>](deploying-the-mbam-20-server-infrastructure-mbam-2.md)

    <span data-ttu-id="965ae-110">In diesem Abschnitt werden die verschiedenen Optionen der MBAM-Bereitstellungstopologie sowie die Verwendung des MBAM-Setups zum Bereitstellen von MBAM-Server Features beschrieben.</span><span class="sxs-lookup"><span data-stu-id="965ae-110">This section describes the different MBAM deployment topology options and how to use MBAM Setup to deploy MBAM Server features.</span></span>

-   [<span data-ttu-id="965ae-111">Bereitstellen von Gruppenrichtlinienobjekten für MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="965ae-111">Deploying MBAM 2.0 Group Policy Objects</span></span>](deploying-mbam-20-group-policy-objects-mbam-2.md)

    <span data-ttu-id="965ae-112">In diesem Abschnitt wird beschrieben, wie Sie MBAM-Gruppenrichtlinienobjekte erstellen und bereitstellen, die für die Verwaltung von MBAM-Clients und BitLocker-Verschlüsselungsrichtlinien im gesamten Unternehmen erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="965ae-112">This section describes how to create and deploy MBAM Group Policy Objects that are required for managing MBAM Clients and BitLocker encryption policies throughout the enterprise.</span></span>

-   [<span data-ttu-id="965ae-113">Bereitstellen des MBAM 2.0-Clients</span><span class="sxs-lookup"><span data-stu-id="965ae-113">Deploying the MBAM 2.0 Client</span></span>](deploying-the-mbam-20-client-mbam-2.md)

    <span data-ttu-id="965ae-114">In diesem Abschnitt wird beschrieben, wie Sie die MBAM-Clientinstallationsdateien verwenden, um die MBAM-Client Software bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="965ae-114">This section describes how to use the MBAM Client Installer files to deploy the MBAM Client software.</span></span>

-   [<span data-ttu-id="965ae-115">Prüfliste für die Bereitstellung von MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="965ae-115">MBAM 2.0 Deployment Checklist</span></span>](mbam-20-deployment-checklist-mbam-2.md)

    <span data-ttu-id="965ae-116">Dieser Abschnitt enthält eine Checkliste für die Bereitstellung, die zur Unterstützung der MBAM-Server Funktion und der MBAM-Client Bereitstellung verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="965ae-116">This section provides a deployment checklist that can be used to assist in MBAM Server feature and MBAM Client deployment.</span></span>

-   [<span data-ttu-id="965ae-117">Aktualisieren von früheren MBAM-Versionen</span><span class="sxs-lookup"><span data-stu-id="965ae-117">Upgrading from Previous Versions of MBAM</span></span>](upgrading-from-previous-versions-of-mbam.md)

    <span data-ttu-id="965ae-118">Dieser Abschnitt enthält Anweisungen zum Upgrade von MBAM aus früheren Versionen.</span><span class="sxs-lookup"><span data-stu-id="965ae-118">This section provides instructions for upgrading MBAM from previous versions.</span></span>

## <span data-ttu-id="965ae-119">Weitere Ressourcen für die Bereitstellung von MBAM</span><span class="sxs-lookup"><span data-stu-id="965ae-119">Other Resources for Deploying MBAM</span></span>


[<span data-ttu-id="965ae-120">Administrator Handbuch für Microsoft BitLocker-Verwaltung und-Überwachung 2</span><span class="sxs-lookup"><span data-stu-id="965ae-120">Microsoft BitLocker Administration and Monitoring 2 Administrator's Guide</span></span>](index.md)

[<span data-ttu-id="965ae-121">Erste Schritte mit MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="965ae-121">Getting Started with MBAM 2.0</span></span>](getting-started-with-mbam-20-mbam-2.md)

[<span data-ttu-id="965ae-122">Planen von MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="965ae-122">Planning for MBAM 2.0</span></span>](planning-for-mbam-20-mbam-2.md)

[<span data-ttu-id="965ae-123">Vorgänge für MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="965ae-123">Operations for MBAM 2.0</span></span>](operations-for-mbam-20-mbam-2.md)

[<span data-ttu-id="965ae-124">Problembehandlung bei MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="965ae-124">Troubleshooting MBAM 2.0</span></span>](troubleshooting-mbam-20-mbam-2.md)

 

 





