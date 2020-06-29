---
title: Bereitstellen des Sprachrelease-Updates für MBAM 1.0
description: Bereitstellen des Sprachrelease-Updates für MBAM 1.0
author: dansimp
ms.assetid: 9dbd85c3-e470-4752-a90f-25754dd46dab
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a819be81594efd9349e3f6c0f6559c2b810bdc9d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804517"
---
# <span data-ttu-id="95405-103">Bereitstellen des Sprachrelease-Updates für MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="95405-103">Deploying the MBAM 1.0 Language Release Update</span></span>


<span data-ttu-id="95405-104">Die Microsoft BitLocker-Verwaltungs-und-Überwachungs Version (MBAM) 1.0 ist ein Update für MBAM und umfasst die Unterstützung neuer Sprachen.</span><span class="sxs-lookup"><span data-stu-id="95405-104">Microsoft BitLocker Administration and Monitoring (MBAM)1.0 Language Release is an update to MBAM and includes the support of new languages.</span></span> <span data-ttu-id="95405-105">Die neuen Sprachen sind:</span><span class="sxs-lookup"><span data-stu-id="95405-105">The new languages are:</span></span>

-   <span data-ttu-id="95405-106">Englisch (en-US)</span><span class="sxs-lookup"><span data-stu-id="95405-106">English (en-us)</span></span>

-   <span data-ttu-id="95405-107">Französisch (FR)</span><span class="sxs-lookup"><span data-stu-id="95405-107">French (fr)</span></span>

-   <span data-ttu-id="95405-108">Italienisch (IT)</span><span class="sxs-lookup"><span data-stu-id="95405-108">Italian (it)</span></span>

-   <span data-ttu-id="95405-109">Deutsch (de)</span><span class="sxs-lookup"><span data-stu-id="95405-109">German (de)</span></span>

-   <span data-ttu-id="95405-110">Spanisch (es)</span><span class="sxs-lookup"><span data-stu-id="95405-110">Spanish (es)</span></span>

-   <span data-ttu-id="95405-111">Koreanisch (Ko)</span><span class="sxs-lookup"><span data-stu-id="95405-111">Korean (ko)</span></span>

-   <span data-ttu-id="95405-112">Japanisch (ja)</span><span class="sxs-lookup"><span data-stu-id="95405-112">Japanese (ja)</span></span>

-   <span data-ttu-id="95405-113">Brasilianisches Portugiesisch (PT-BR)</span><span class="sxs-lookup"><span data-stu-id="95405-113">Brazilian Portuguese (pt-br)</span></span>

-   <span data-ttu-id="95405-114">Russisch (ru)</span><span class="sxs-lookup"><span data-stu-id="95405-114">Russian (ru)</span></span>

-   <span data-ttu-id="95405-115">Chinesisch (traditionell) (ZH-TW)</span><span class="sxs-lookup"><span data-stu-id="95405-115">Chinese Traditional (zh-tw)</span></span>

-   <span data-ttu-id="95405-116">Chinesisch (vereinfacht) (ZH-CN)</span><span class="sxs-lookup"><span data-stu-id="95405-116">Chinese Simplified (zh-cn)</span></span>

<span data-ttu-id="95405-117">Mit dem MBAM 1.0-sprach Update wird die Versionsnummer von MBAM 1.0.1237.1 in MBAM 1.0.2001 geändert.</span><span class="sxs-lookup"><span data-stu-id="95405-117">The MBAM1.0 language update will change the version number from MBAM 1.0.1237.1 to MBAM 1.0.2001.</span></span>

<span data-ttu-id="95405-118">Sie müssen nicht alle MBAM-Features erneut installieren, um diese zusätzlichen Sprachen hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="95405-118">You do not need to reinstall all of the MBAM features in order to add these additional languages.</span></span> <span data-ttu-id="95405-119">In diesem Thema werden die erforderlichen Schritte zum Hinzufügen der neu unterstützten Sprachen definiert.</span><span class="sxs-lookup"><span data-stu-id="95405-119">This topic defines the steps required to add the newly supported languages.</span></span>

## <span data-ttu-id="95405-120">Bereitstellen der MBAM International-Version für MBAM-Server Features</span><span class="sxs-lookup"><span data-stu-id="95405-120">Deploy the MBAM international release to MBAM Server features</span></span>


<span data-ttu-id="95405-121">Zunächst müssen Sie die folgenden MBAM-Server Features aktualisieren:</span><span class="sxs-lookup"><span data-stu-id="95405-121">To begin, you must update the following MBAM server features:</span></span>

-   <span data-ttu-id="95405-122">Konformitäts-und Überwachungsbericht</span><span class="sxs-lookup"><span data-stu-id="95405-122">Compliance and Audit Report</span></span>

-   <span data-ttu-id="95405-123">Verwaltungs-und Überwachungs Server</span><span class="sxs-lookup"><span data-stu-id="95405-123">Administration and Monitoring Server</span></span>

-   <span data-ttu-id="95405-124">Richtlinienvorlagen</span><span class="sxs-lookup"><span data-stu-id="95405-124">Policy Templates</span></span>

<span data-ttu-id="95405-125">Anschließend müssen Sie **MbamSetup.exe** ausführen, um die MBAM-Features zu aktualisieren, die gleichzeitig auf dem gleichen Server ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="95405-125">Then, you must run **MbamSetup.exe** to upgrade the MBAM features that run on the same server at the same time.</span></span>

[<span data-ttu-id="95405-126">So installieren Sie das MBAM-Sprachupdate auf einem einzelnen Server</span><span class="sxs-lookup"><span data-stu-id="95405-126">How to Install the MBAM Language Update on a Single Server</span></span>](how-to-install-the-mbam-language-update-on-a-single-server-mbam-1.md)

[<span data-ttu-id="95405-127">So installieren Sie das MBAM-Sprachupdate auf verteilten Servern</span><span class="sxs-lookup"><span data-stu-id="95405-127">How to Install the MBAM Language Update on Distributed Servers</span></span>](how-to-install-the-mbam-language-update-on-distributed-servers-mbam-1.md)

## <span data-ttu-id="95405-128">Installieren des MBAM-sprach Updates für Gruppenrichtlinien</span><span class="sxs-lookup"><span data-stu-id="95405-128">Install the MBAM language update for Group Policies</span></span>


<span data-ttu-id="95405-129">Die MBAM-Gruppenrichtlinienvorlagen können auf jeder Verwaltungsarbeitsstation installiert werden, oder Sie können in den zentralen Gruppenrichtlinien-Informationsspeicher kopiert werden, um die Vorlagen für alle Gruppenrichtlinienadministratoren verfügbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="95405-129">The MBAM Group Policy templates can be installed on each management workstation or they can be copied to the Group Policy central store, in order to make the templates available to all Group Policy administrators.</span></span> <span data-ttu-id="95405-130">Die Richtlinienvorlagen können nicht direkt auf einem Domänencontroller installiert werden.</span><span class="sxs-lookup"><span data-stu-id="95405-130">The policy templates cannot be directly installed on a domain controller.</span></span> <span data-ttu-id="95405-131">Wenn Sie keinen zentralen Gruppenrichtlinien Speicher verwenden, müssen Sie die Richtlinien manuell auf jeden Domänencontroller kopieren, der MBAM-Gruppenrichtlinien verwaltet.</span><span class="sxs-lookup"><span data-stu-id="95405-131">If you do not use a Group Policy central store, then you must copy the policies manually to each domain controller that manages MBAM Group Policy.</span></span>

<span data-ttu-id="95405-132">Wenn Sie die Vorlagen für MBAM-Sprachrichtlinien hinzufügen möchten, kopieren Sie die Gruppenrichtlinien-Sprachdateien von%systemroot%\\PolicyDefinitions auf dem Computer, auf dem die Rolle "Richtlinienvorlagen" an demselben Speicherort auf dem Arbeitsstationscomputer installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="95405-132">To add the MBAM language policies templates, copy the Group Policy language files from %SystemRoot%\\PolicyDefinitions on the computer where the “Policy Templates” role was installed to the same location on the workstation computer.</span></span> <span data-ttu-id="95405-133">Im folgenden finden Sie einige Beispiele für Gruppenrichtliniendateien:</span><span class="sxs-lookup"><span data-stu-id="95405-133">Here are some examples of Group Policy files:</span></span>

-   <span data-ttu-id="95405-134">BitLockerManagement. ADMX</span><span class="sxs-lookup"><span data-stu-id="95405-134">BitLockerManagement.admx</span></span>

-   <span data-ttu-id="95405-135">BitLockerUserManagement. ADMX</span><span class="sxs-lookup"><span data-stu-id="95405-135">BitLockerUserManagement.admx</span></span>

-   <span data-ttu-id="95405-136">en-us\\BitLockerManagement.adml</span><span class="sxs-lookup"><span data-stu-id="95405-136">en-us\\BitLockerManagement.adml</span></span>

-   <span data-ttu-id="95405-137">en-us\\BitLockerUserManagement.adml</span><span class="sxs-lookup"><span data-stu-id="95405-137">en-us\\BitLockerUserManagement.adml</span></span>

-   <span data-ttu-id="95405-138">Fr-fr\\ BitLockerManagement. ADML</span><span class="sxs-lookup"><span data-stu-id="95405-138">fr-fr\\ BitLockerManagement.adml</span></span>

-   <span data-ttu-id="95405-139">Fr-fr\\ BitLockerUserManagement. ADML</span><span class="sxs-lookup"><span data-stu-id="95405-139">fr-fr\\ BitLockerUserManagement.adml</span></span>

-   <span data-ttu-id="95405-140">(und ebenso für jede unterstützte Sprache)</span><span class="sxs-lookup"><span data-stu-id="95405-140">(and similarly for each supported language)</span></span>

## <span data-ttu-id="95405-141">Bekannte Probleme in der MBAM International-Version</span><span class="sxs-lookup"><span data-stu-id="95405-141">Known issues in the MBAM international release</span></span>


<span data-ttu-id="95405-142">Dieses Thema enthält bekannte Probleme bei der Microsoft BitLocker-Verwaltung und-Überwachung in der internationalen Version.</span><span class="sxs-lookup"><span data-stu-id="95405-142">This topic contains known issues for Microsoft BitLocker Administration and Monitoring International Release.</span></span>

[<span data-ttu-id="95405-143">Bekannte Probleme beim internationalen Release für MBAM</span><span class="sxs-lookup"><span data-stu-id="95405-143">Known Issues in the MBAM International Release</span></span>](known-issues-in-the-mbam-international-release-mbam-1.md)

## <span data-ttu-id="95405-144">Weitere Ressourcen für die Bereitstellung des MBAM 1,0-Sprach Updates</span><span class="sxs-lookup"><span data-stu-id="95405-144">Other resources for deploying the MBAM 1.0 Language Update</span></span>


[<span data-ttu-id="95405-145">Bereitstellen von MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="95405-145">Deploying MBAM 1.0</span></span>](deploying-mbam-10.md)

 

 





