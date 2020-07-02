---
title: Administrator Handbuch für Microsoft BitLocker-Verwaltung und-Überwachung 2
description: Administrator Handbuch für Microsoft BitLocker-Verwaltung und-Überwachung 2
author: dansimp
ms.assetid: fdb43f62-960a-4811-8802-50efdf04b4af
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 04/19/2017
ms.openlocfilehash: dd6deb6fb91c64ac8609b54114e0dd417497034a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10795750"
---
# <span data-ttu-id="54e32-103">Administrator Handbuch für Microsoft BitLocker-Verwaltung und-Überwachung 2</span><span class="sxs-lookup"><span data-stu-id="54e32-103">Microsoft BitLocker Administration and Monitoring 2 Administrator's Guide</span></span>

<span data-ttu-id="54e32-104">Microsoft BitLockerAdministration and Monitoring (MBAM) 2.0 bietet eine vereinfachte Verwaltungsoberfläche, die Sie zum Verwalten der BitLocker-Laufwerkverschlüsselung verwenden können.</span><span class="sxs-lookup"><span data-stu-id="54e32-104">Microsoft BitLockerAdministration and Monitoring(MBAM)2.0 provides a simplified administrative interface that you can use to manage BitLocker drive encryption.</span></span> <span data-ttu-id="54e32-105">In BitLockerAdministration und Monitoring 2.0 können Sie die BitLocker-Laufwerk Verschlüsselungsrichtlinien Optionen auswählen, die für Ihr Unternehmen geeignet sind, und diese dann zum Überwachen der Clientkompatibilität mit diesen Richtlinien verwenden.</span><span class="sxs-lookup"><span data-stu-id="54e32-105">In BitLockerAdministration and Monitoring2.0, you can select BitLocker drive encryption policy options that are appropriate for your enterprise, and then use them to monitor client compliance with those policies.</span></span> <span data-ttu-id="54e32-106">Sie können auch den Verschlüsselungsstatus eines einzelnen Computers und des Unternehmens als Ganzes melden.</span><span class="sxs-lookup"><span data-stu-id="54e32-106">You can also report on the encryption status of an individual computer and on the enterprise as a whole.</span></span> <span data-ttu-id="54e32-107">Darüber hinaus können Sie auf Wiederherstellungsschlüssel Informationen zugreifen, wenn Benutzer Ihre PIN oder Ihr Kennwort vergessen oder wenn sich der BIOS-oder Boot-Eintrag ändert.</span><span class="sxs-lookup"><span data-stu-id="54e32-107">In addition, you can access recovery key information when users forget their PIN or password or when their BIOS or boot record changes.</span></span>

## <span data-ttu-id="54e32-108">Gliederungs</span><span class="sxs-lookup"><span data-stu-id="54e32-108">Outline</span></span>

- [<span data-ttu-id="54e32-109">Erste Schritte mit MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="54e32-109">Getting Started with MBAM 2.0</span></span>](getting-started-with-mbam-20-mbam-2.md)
  - [<span data-ttu-id="54e32-110">Informationen zu MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="54e32-110">About MBAM 2.0</span></span>](about-mbam-20-mbam-2.md)
  - [<span data-ttu-id="54e32-111">Versionshinweise für MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="54e32-111">Release Notes for MBAM 2.0</span></span>](release-notes-for-mbam-20-mbam-2.md)
  - [<span data-ttu-id="54e32-112">Infos zu MBAM 2.0 SP1</span><span class="sxs-lookup"><span data-stu-id="54e32-112">About MBAM 2.0 SP1</span></span>](about-mbam-20-sp1.md)
  - [<span data-ttu-id="54e32-113">Versionshinweise für MBAM 2.0SP1</span><span class="sxs-lookup"><span data-stu-id="54e32-113">Release Notes for MBAM 2.0 SP1</span></span>](release-notes-for-mbam-20-sp1.md)
  - [<span data-ttu-id="54e32-114">Auswerten von MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="54e32-114">Evaluating MBAM 2.0</span></span>](evaluating-mbam-20-mbam-2.md)
  - [<span data-ttu-id="54e32-115">High-Level-Architektur für MBAM2.0</span><span class="sxs-lookup"><span data-stu-id="54e32-115">High-Level Architecture for MBAM 2.0</span></span>](high-level-architecture-for-mbam-20-mbam-2.md)
  - [<span data-ttu-id="54e32-116">Barrierefreiheit von MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="54e32-116">Accessibility for MBAM 2.0</span></span>](accessibility-for-mbam-20-mbam-2.md)
- [<span data-ttu-id="54e32-117">Planen von MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="54e32-117">Planning for MBAM 2.0</span></span>](planning-for-mbam-20-mbam-2.md)
  - [<span data-ttu-id="54e32-118">Vorbereiten der Umgebung für MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="54e32-118">Preparing your Environment for MBAM 2.0</span></span>](preparing-your-environment-for-mbam-20-mbam-2.md)
  - [<span data-ttu-id="54e32-119">Bereitstellungsvoraussetzungen für MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="54e32-119">MBAM 2.0 Deployment Prerequisites</span></span>](mbam-20-deployment-prerequisites-mbam-2.md)
  - [<span data-ttu-id="54e32-120">Planen der Bereitstellung von MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="54e32-120">Planning to Deploy MBAM 2.0</span></span>](planning-to-deploy-mbam-20-mbam-2.md)
  - [<span data-ttu-id="54e32-121">Von MBAM 2.0 unterstützte Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="54e32-121">MBAM 2.0 Supported Configurations</span></span>](mbam-20-supported-configurations-mbam-2.md)
  - [<span data-ttu-id="54e32-122">Prüfliste für die Planung von MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="54e32-122">MBAM 2.0 Planning Checklist</span></span>](mbam-20-planning-checklist-mbam-2.md)
- [<span data-ttu-id="54e32-123">Bereitstellen von MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="54e32-123">Deploying MBAM 2.0</span></span>](deploying-mbam-20-mbam-2.md)
  - [<span data-ttu-id="54e32-124">Bereitstellen der Serverinfrastruktur von MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="54e32-124">Deploying the MBAM 2.0 Server Infrastructure</span></span>](deploying-the-mbam-20-server-infrastructure-mbam-2.md)
  - [<span data-ttu-id="54e32-125">Bereitstellen von Gruppenrichtlinienobjekten für MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="54e32-125">Deploying MBAM 2.0 Group Policy Objects</span></span>](deploying-mbam-20-group-policy-objects-mbam-2.md)
  - [<span data-ttu-id="54e32-126">Bereitstellen des MBAM 2.0-Clients</span><span class="sxs-lookup"><span data-stu-id="54e32-126">Deploying the MBAM 2.0 Client</span></span>](deploying-the-mbam-20-client-mbam-2.md)
  - [<span data-ttu-id="54e32-127">Prüfliste für die Bereitstellung von MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="54e32-127">MBAM 2.0 Deployment Checklist</span></span>](mbam-20-deployment-checklist-mbam-2.md)
  - [<span data-ttu-id="54e32-128">Aktualisieren von früheren MBAM-Versionen</span><span class="sxs-lookup"><span data-stu-id="54e32-128">Upgrading from Previous Versions of MBAM</span></span>](upgrading-from-previous-versions-of-mbam.md)
- [<span data-ttu-id="54e32-129">Vorgänge für MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="54e32-129">Operations for MBAM 2.0</span></span>](operations-for-mbam-20-mbam-2.md)
  - [<span data-ttu-id="54e32-130">Verwenden von MBAM mit dem Konfigurations-Manager</span><span class="sxs-lookup"><span data-stu-id="54e32-130">Using MBAM with Configuration Manager</span></span>](using-mbam-with-configuration-manager.md)
  - [<span data-ttu-id="54e32-131">Verwalten von MBAM 2.0-Funktionen</span><span class="sxs-lookup"><span data-stu-id="54e32-131">Administering MBAM 2.0 Features</span></span>](administering-mbam-20-features-mbam-2.md)
  - [<span data-ttu-id="54e32-132">BitLocker-Kompatibilitätsüberwachung und -berichterstellung mit MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="54e32-132">Monitoring and Reporting BitLocker Compliance with MBAM 2.0</span></span>](monitoring-and-reporting-bitlocker-compliance-with-mbam-20-mbam-2.md)
  - [<span data-ttu-id="54e32-133">Verwalten von BitLocker mit MBAM</span><span class="sxs-lookup"><span data-stu-id="54e32-133">Performing BitLocker Management with MBAM</span></span>](performing-bitlocker-management-with-mbam-mbam-2.md)
  - [<span data-ttu-id="54e32-134">Verwalten von MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="54e32-134">Maintaining MBAM 2.0</span></span>](maintaining-mbam-20-mbam-2.md)
  - [<span data-ttu-id="54e32-135">Sicherheit und Datenschutz für MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="54e32-135">Security and Privacy for MBAM 2.0</span></span>](security-and-privacy-for-mbam-20-mbam-2.md)
  - [<span data-ttu-id="54e32-136">Verwalten von MBAM 2.0 mit PowerShell</span><span class="sxs-lookup"><span data-stu-id="54e32-136">Administering MBAM 2.0 Using PowerShell</span></span>](administering-mbam-20-using-powershell-mbam-2.md)
- [<span data-ttu-id="54e32-137">Problembehandlung bei MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="54e32-137">Troubleshooting MBAM 2.0</span></span>](troubleshooting-mbam-20-mbam-2.md)

## <span data-ttu-id="54e32-138">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="54e32-138">More Information</span></span>

- [<span data-ttu-id="54e32-139">MDOP-Informations Erfahrung</span><span class="sxs-lookup"><span data-stu-id="54e32-139">MDOP Information Experience</span></span>](index.md)

  <span data-ttu-id="54e32-140">Finden Sie Dokumentation, Videos und andere Ressourcen für MDOP-Technologien.</span><span class="sxs-lookup"><span data-stu-id="54e32-140">Find documentation, videos, and other resources for MDOP technologies.</span></span>

 

 





