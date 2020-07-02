---
title: Microsoft BitLocker Administration and Monitoring 2.5
description: Microsoft BitLocker Administration and Monitoring 2.5
author: dansimp
ms.assetid: fd81d7de-b166-47e8-b6c7-d984830762b6
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 04/19/2017
ms.openlocfilehash: 2e5243131853207f0ed3cbb6d0cd8fb8e3d56108
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10795694"
---
# <span data-ttu-id="d4245-103">Microsoft BitLocker Administration and Monitoring 2.5</span><span class="sxs-lookup"><span data-stu-id="d4245-103">Microsoft BitLocker Administration and Monitoring 2.5</span></span>

<span data-ttu-id="d4245-104">Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) 2,5 bietet eine vereinfachte Verwaltungsoberfläche, die Sie zum Verwalten der BitLocker-Laufwerkverschlüsselung verwenden können.</span><span class="sxs-lookup"><span data-stu-id="d4245-104">Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 provides a simplified administrative interface that you can use to manage BitLocker Drive Encryption.</span></span> <span data-ttu-id="d4245-105">Sie konfigurieren MBAM-Gruppenrichtlinienvorlagen, mit denen Sie die für Ihr Unternehmen geeigneten BitLocker-Laufwerk Verschlüsselungsrichtlinien Optionen festlegen und dann verwenden können, um die Clientkompatibilität mit diesen Richtlinien zu überwachen.</span><span class="sxs-lookup"><span data-stu-id="d4245-105">You configure MBAM Group Policy Templates that enable you to set BitLocker Drive Encryption policy options that are appropriate for your enterprise, and then use them to monitor client compliance with those policies.</span></span> <span data-ttu-id="d4245-106">Sie können auch den Verschlüsselungsstatus eines einzelnen Computers und des Unternehmens als Ganzes melden.</span><span class="sxs-lookup"><span data-stu-id="d4245-106">You can also report on the encryption status of an individual computer and on the enterprise as a whole.</span></span> <span data-ttu-id="d4245-107">Darüber hinaus können Sie auf Wiederherstellungsschlüssel Informationen zugreifen, wenn Benutzer Ihre PIN oder Ihr Kennwort vergessen oder wenn sich der BIOS-oder Boot-Eintrag ändert.</span><span class="sxs-lookup"><span data-stu-id="d4245-107">In addition, you can access recovery key information when users forget their PIN or password or when their BIOS or boot record changes.</span></span> <span data-ttu-id="d4245-108">Eine detailliertere Beschreibung von MBAM finden Sie unter [Informationen zu MBAM 2,5](about-mbam-25.md).</span><span class="sxs-lookup"><span data-stu-id="d4245-108">For a more detailed description of MBAM, see [About MBAM 2.5](about-mbam-25.md).</span></span>

<span data-ttu-id="d4245-109">Informationen zum Abrufen von MBAM finden Sie unter [wie erhalte ich MDOP](https://docs.microsoft.com/microsoft-desktop-optimization-pack/index#how-to-get-mdop).</span><span class="sxs-lookup"><span data-stu-id="d4245-109">To obtain MBAM, see [How Do I Get MDOP](https://docs.microsoft.com/microsoft-desktop-optimization-pack/index#how-to-get-mdop).</span></span>

## <span data-ttu-id="d4245-110">Gliederungs</span><span class="sxs-lookup"><span data-stu-id="d4245-110">Outline</span></span>

- <a href="" id="getting-started-with-mbam-2-5"></a>[<span data-ttu-id="d4245-111">Erste Schritte mit MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="d4245-111">Getting Started with MBAM 2.5</span></span>](getting-started-with-mbam-25.md)
  - [<span data-ttu-id="d4245-112">Informationen zu MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="d4245-112">About MBAM 2.5</span></span>](about-mbam-25.md)
  - [<span data-ttu-id="d4245-113">Versionshinweise für MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="d4245-113">Release Notes for MBAM 2.5</span></span>](release-notes-for-mbam-25.md)
  - [<span data-ttu-id="d4245-114">Infos zu MBAM 2.5 SP1</span><span class="sxs-lookup"><span data-stu-id="d4245-114">About MBAM 2.5 SP1</span></span>](about-mbam-25-sp1.md)
  - [<span data-ttu-id="d4245-115">Versionshinweise für MBAM 2.5SP1</span><span class="sxs-lookup"><span data-stu-id="d4245-115">Release Notes for MBAM 2.5 SP1</span></span>](release-notes-for-mbam-25-sp1.md)
  - [<span data-ttu-id="d4245-116">Auswerten von MBAM 2.5 in einer Testumgebung</span><span class="sxs-lookup"><span data-stu-id="d4245-116">Evaluating MBAM 2.5 in a Test Environment</span></span>](evaluating-mbam-25-in-a-test-environment.md)
  - [<span data-ttu-id="d4245-117">High-Level-Architektur für MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="d4245-117">High-Level Architecture for MBAM 2.5</span></span>](high-level-architecture-for-mbam-25.md)
  - [<span data-ttu-id="d4245-118">Barrierefreiheit von MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="d4245-118">Accessibility for MBAM 2.5</span></span>](accessibility-for-mbam-25.md)
- <a href="" id="planning-for-mbam-2-5"></a>[<span data-ttu-id="d4245-119">Planen von MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="d4245-119">Planning for MBAM 2.5</span></span>](planning-for-mbam-25.md)
  - [<span data-ttu-id="d4245-120">Vorbereiten der Umgebung für MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="d4245-120">Preparing your Environment for MBAM 2.5</span></span>](preparing-your-environment-for-mbam-25.md)
  - [<span data-ttu-id="d4245-121">Bereitstellungsvoraussetzungen für MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="d4245-121">MBAM 2.5 Deployment Prerequisites</span></span>](mbam-25-deployment-prerequisites.md)
  - [<span data-ttu-id="d4245-122">Planen der Gruppenrichtlinienanforderungen für MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="d4245-122">Planning for MBAM 2.5 Group Policy Requirements</span></span>](planning-for-mbam-25-group-policy-requirements.md)
  - [<span data-ttu-id="d4245-123">Planen der Gruppen und Konten für MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="d4245-123">Planning for MBAM 2.5 Groups and Accounts</span></span>](planning-for-mbam-25-groups-and-accounts.md)
  - [<span data-ttu-id="d4245-124">Planen der Sicherung von MBAM-Websites</span><span class="sxs-lookup"><span data-stu-id="d4245-124">Planning How to Secure the MBAM Websites</span></span>](planning-how-to-secure-the-mbam-websites.md)
  - [<span data-ttu-id="d4245-125">Planen der Bereitstellung von MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="d4245-125">Planning to Deploy MBAM 2.5</span></span>](planning-to-deploy-mbam-25.md)
  - [<span data-ttu-id="d4245-126">Von MBAM 2.5 unterstützte Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="d4245-126">MBAM 2.5 Supported Configurations</span></span>](mbam-25-supported-configurations.md)
  - [<span data-ttu-id="d4245-127">Planen der hohen Verfügbarkeit von MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="d4245-127">Planning for MBAM 2.5 High Availability</span></span>](planning-for-mbam-25-high-availability.md)
  - [<span data-ttu-id="d4245-128">Sicherheitsüberlegungen zu MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="d4245-128">MBAM 2.5 Security Considerations</span></span>](mbam-25-security-considerations.md)
  - [<span data-ttu-id="d4245-129">Prüfliste für die Planung von MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="d4245-129">MBAM 2.5 Planning Checklist</span></span>](mbam-25-planning-checklist.md)
- <a href="" id="deploying-mbam-2-5"></a>[<span data-ttu-id="d4245-130">Bereitstellen von MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="d4245-130">Deploying MBAM 2.5</span></span>](deploying-mbam-25.md)
  - [<span data-ttu-id="d4245-131">Bereitstellen der Serverinfrastruktur von MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="d4245-131">Deploying the MBAM 2.5 Server Infrastructure</span></span>](deploying-the-mbam-25-server-infrastructure.md)
  - [<span data-ttu-id="d4245-132">Bereitstellen von Gruppenrichtlinienobjekten für MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="d4245-132">Deploying MBAM 2.5 Group Policy Objects</span></span>](deploying-mbam-25-group-policy-objects.md)
  - [<span data-ttu-id="d4245-133">Bereitstellen des MBAM 2.5-Clients</span><span class="sxs-lookup"><span data-stu-id="d4245-133">Deploying the MBAM 2.5 Client</span></span>](deploying-the-mbam-25-client.md)
  - [<span data-ttu-id="d4245-134">Prüfliste für die Bereitstellung von MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="d4245-134">MBAM 2.5 Deployment Checklist</span></span>](mbam-25-deployment-checklist.md)
  - [<span data-ttu-id="d4245-135">Aktualisieren von MBAM 2.5 oder MBAM 2.5 SP1 von früheren Versionen</span><span class="sxs-lookup"><span data-stu-id="d4245-135">Upgrading to MBAM 2.5 or MBAM 2.5 SP1 from Previous Versions</span></span>](upgrading-to-mbam-25-or-mbam-25-sp1-from-previous-versions.md)
  - [<span data-ttu-id="d4245-136">Entfernen von MBAM-Serverfunktionen oder -software</span><span class="sxs-lookup"><span data-stu-id="d4245-136">Removing MBAM Server Features or Software</span></span>](removing-mbam-server-features-or-software.md)
- <a href="" id="operations-for-mbam-2-5"></a>[<span data-ttu-id="d4245-137">Vorgänge für MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="d4245-137">Operations for MBAM 2.5</span></span>](operations-for-mbam-25.md)
  - [<span data-ttu-id="d4245-138">Verwalten von MBAM 2.5-Funktionen</span><span class="sxs-lookup"><span data-stu-id="d4245-138">Administering MBAM 2.5 Features</span></span>](administering-mbam-25-features.md)
  - [<span data-ttu-id="d4245-139">BitLocker-Kompatibilitätsüberwachung und -berichterstellung mit MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="d4245-139">Monitoring and Reporting BitLocker Compliance with MBAM 2.5</span></span>](monitoring-and-reporting-bitlocker-compliance-with-mbam-25.md)
  - [<span data-ttu-id="d4245-140">Durchführen der BitLocker-Verwaltung mit MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="d4245-140">Performing BitLocker Management with MBAM 2.5</span></span>](performing-bitlocker-management-with-mbam-25.md)
  - [<span data-ttu-id="d4245-141">Verwalten von MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="d4245-141">Maintaining MBAM 2.5</span></span>](maintaining-mbam-25.md)
  - [<span data-ttu-id="d4245-142">Verwenden von Windows PowerShell zum Verwalten von MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="d4245-142">Using Windows PowerShell to Administer MBAM 2.5</span></span>](using-windows-powershell-to-administer-mbam-25.md)
- <a href="" id="troubleshooting-mbam-2-5"></a>[<span data-ttu-id="d4245-143">Problembehandlung bei MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="d4245-143">Troubleshooting MBAM 2.5</span></span>](troubleshooting-mbam-25.md)
- <a href="" id="technical-reference-for-mbam-2-5"></a>[<span data-ttu-id="d4245-144">Technische Referenz für MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="d4245-144">Technical Reference for MBAM 2.5</span></span>](technical-reference-for-mbam-25.md)
  - [<span data-ttu-id="d4245-145">Client-Ereignisprotokolle</span><span class="sxs-lookup"><span data-stu-id="d4245-145">Client Event Logs</span></span>](client-event-logs.md)
  - [<span data-ttu-id="d4245-146">Serverereignisprotokolle</span><span class="sxs-lookup"><span data-stu-id="d4245-146">Server Event Logs</span></span>](server-event-logs.md)

## <span data-ttu-id="d4245-147">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="d4245-147">More Information</span></span>

- [<span data-ttu-id="d4245-148">MDOP-Informations Erfahrung</span><span class="sxs-lookup"><span data-stu-id="d4245-148">MDOP Information Experience</span></span>](index.md)

  <span data-ttu-id="d4245-149">Finden Sie Dokumentation, Videos und andere Ressourcen für MDOP-Technologien.</span><span class="sxs-lookup"><span data-stu-id="d4245-149">Find documentation, videos, and other resources for MDOP technologies.</span></span>

- [<span data-ttu-id="d4245-150">MBAM-Bereitstellungshandbuch</span><span class="sxs-lookup"><span data-stu-id="d4245-150">MBAM Deployment Guide</span></span>](https://www.microsoft.com/download/details.aspx?id=38398)

  <span data-ttu-id="d4245-151">Erhalten Sie Hilfe bei der Auswahl einer Bereitstellungsmethode für MBAM, einschließlich Schritt-für-Schritt-Anleitungen für die einzelnen Methoden.</span><span class="sxs-lookup"><span data-stu-id="d4245-151">Get help in choosing a deployment method for MBAM, including step-by-step instructions for each method.</span></span>
    
- [<span data-ttu-id="d4245-152">Anwenden von Hotfixes auf MBAM 2,5 SP1-Server</span><span class="sxs-lookup"><span data-stu-id="d4245-152">Apply Hotfixes on MBAM 2.5 SP1 Server</span></span>](apply-hotfix-for-mbam-25-sp1.md)

  <span data-ttu-id="d4245-153">Leitfaden zum Anwenden von MBAM 2,5 SP1-Server-Hotfixes</span><span class="sxs-lookup"><span data-stu-id="d4245-153">Guide of how to apply MBAM 2.5 SP1 Server hotfixes</span></span>
