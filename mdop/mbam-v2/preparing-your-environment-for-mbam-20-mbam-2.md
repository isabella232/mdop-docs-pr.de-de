---
title: Vorbereiten der Umgebung für MBAM 2.0
description: Vorbereiten der Umgebung für MBAM 2.0
author: dansimp
ms.assetid: 5fb01da9-620e-4992-9e54-2ed3fb69e6af
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f1be989112d456064db302952d50159d00b5597a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811257"
---
# <span data-ttu-id="86e4b-103">Vorbereiten der Umgebung für MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="86e4b-103">Preparing your Environment for MBAM 2.0</span></span>


<span data-ttu-id="86e4b-104">Bevor Sie mit der Einrichtung von Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) beginnen, sollten Sie sicherstellen, dass Sie die Voraussetzungen für die Installation des Produkts erfüllt haben.</span><span class="sxs-lookup"><span data-stu-id="86e4b-104">Before beginning Microsoft BitLocker Administration and Monitoring (MBAM) Setup, you should make sure that you have met the prerequisites to install the product.</span></span> <span data-ttu-id="86e4b-105">Wenn Sie wissen, welche Voraussetzungen Voraussetzungen sind, können Sie das Produkt effizient bereitstellen und seine Features aktivieren, damit es die geschäftlichen Ziele Ihrer Organisation am effektivsten unterstützt.</span><span class="sxs-lookup"><span data-stu-id="86e4b-105">When you know what the prerequisites are ahead of time, you can efficiently deploy the product and enable its features so that it most effectively supports your organization’s business objectives.</span></span>

<span data-ttu-id="86e4b-106">Wenn Sie die Microsoft BitLocker-Verwaltung und-Überwachung mit Microsoft System Center Configuration Manager 2007 oder MicrosoftSystemCenter2012 ConfigurationManager bereitstellen, lesen Sie [Planen der Bereitstellung von MBAM mit Configuration Manager](planning-to-deploy-mbam-with-configuration-manager-2.md).</span><span class="sxs-lookup"><span data-stu-id="86e4b-106">If you are deploying Microsoft BitLocker Administration and Monitoring with Microsoft System Center Configuration Manager 2007 or MicrosoftSystemCenter2012 ConfigurationManager, see [Planning to Deploy MBAM with Configuration Manager](planning-to-deploy-mbam-with-configuration-manager-2.md).</span></span>

## <span data-ttu-id="86e4b-107">Überprüfen der MBAM 2,0-Bereitstellungsvoraussetzungen</span><span class="sxs-lookup"><span data-stu-id="86e4b-107">Review MBAM 2.0 Deployment Prerequisites</span></span>


<span data-ttu-id="86e4b-108">Der MBAM-Client und alle MBAM-Server Features verfügen über bestimmte Voraussetzungen, die erfüllt sein müssen, bevor Sie erfolgreich installiert werden können.</span><span class="sxs-lookup"><span data-stu-id="86e4b-108">The MBAM Client and each of the MBAM Server features have specific prerequisites that must be met before they can be successfully installed.</span></span>

<span data-ttu-id="86e4b-109">Um eine erfolgreiche Installation von MBAM-Clients und MBAM-Server Features sicherzustellen, müssen Sie sicherstellen, dass die für die Installation von MBAM Client-oder MBAM-Servern angegebenen Computer ordnungsgemäß für die MBAM Einrichtung vorbereitet sind</span><span class="sxs-lookup"><span data-stu-id="86e4b-109">To ensure successful installation of MBAM Clients and MBAM Server features, ensure that computers specified for MBAM Client or MBAM Server feature installation are properly prepared for MBAM Setup.</span></span>

<span data-ttu-id="86e4b-110">**Hinweis**  MBAM-Setup überprüft, ob alle Voraussetzungen erfüllt sind, bevor die Installation gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="86e4b-110">**Note** MBAM Setup checks that all prerequisites are met before installation starts.</span></span> <span data-ttu-id="86e4b-111">Wenn alle Voraussetzungen nicht erfüllt sind, schlägt Setup fehl.</span><span class="sxs-lookup"><span data-stu-id="86e4b-111">If all prerequisites are not met, Setup will fail.</span></span>

 

[<span data-ttu-id="86e4b-112">Bereitstellungsvoraussetzungen für MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="86e4b-112">MBAM 2.0 Deployment Prerequisites</span></span>](mbam-20-deployment-prerequisites-mbam-2.md)

## <span data-ttu-id="86e4b-113">Planen der MBAM 2,0-Gruppenrichtlinienanforderungen</span><span class="sxs-lookup"><span data-stu-id="86e4b-113">Plan for MBAM 2.0 Group Policy Requirements</span></span>


<span data-ttu-id="86e4b-114">Bevor MBAM Clients im Unternehmen verwalten kann, müssen Sie Gruppenrichtlinien für die Verschlüsselungsanforderungen Ihrer Umgebung definieren.</span><span class="sxs-lookup"><span data-stu-id="86e4b-114">Before MBAM can manage clients in the enterprise, you must define Group Policy for the encryption requirements of your environment.</span></span>

<span data-ttu-id="86e4b-115">**Wichtig**  MBAM wird nicht mit Richtlinien für eigenständige BitLocker-Laufwerkverschlüsselung funktionieren.</span><span class="sxs-lookup"><span data-stu-id="86e4b-115">**Important** MBAM will not work with policies for stand-alone BitLocker drive encryption.</span></span> <span data-ttu-id="86e4b-116">Für MBAM müssen Gruppenrichtlinieneinstellungen definiert sein, oder die BitLocker-Verschlüsselung und-Erzwingung schlägt fehl.</span><span class="sxs-lookup"><span data-stu-id="86e4b-116">Group Policy settings must be defined for MBAM, or BitLocker encryption and enforcement will fail.</span></span>

 

[<span data-ttu-id="86e4b-117">Planen der Gruppenrichtlinienanforderungen für MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="86e4b-117">Planning for MBAM 2.0 Group Policy Requirements</span></span>](planning-for-mbam-20-group-policy-requirements-mbam-2.md)

## <span data-ttu-id="86e4b-118">Planen von MBAM 2,0-Administrator Rollen</span><span class="sxs-lookup"><span data-stu-id="86e4b-118">Plan for MBAM 2.0 Administrator Roles</span></span>


<span data-ttu-id="86e4b-119">MBAM-Administratorrollen werden von lokalen Gruppen verwaltet, die von MBAM Setup beim Installieren des BitLocker-Verwaltungs-und Überwachungsservers, des Features Konformitäts-und Überwachungsberichte sowie der Kompatibilitäts-und Überwachungs Status Datenbank erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="86e4b-119">MBAM administrator roles are managed by local groups that are created by MBAM Setup when you install the BitLocker Administration and Monitoring Server, the Compliance and Audit Reports feature, and the Compliance and Audit Status Database.</span></span>

<span data-ttu-id="86e4b-120">Die Mitgliedschaft in den Microsoft BitLocker-Verwaltungs-und Überwachungs Rollen kann am besten durch Erstellen von Sicherheitsgruppen in ActiveDirectoryDomainServices, Hinzufügen der entsprechenden Administratorkonten zu diesen Gruppen und anschließendes Hinzufügen dieser Sicherheitsgruppen zur BitLocker-Verwaltung und zum Überwachen lokaler Gruppen verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="86e4b-120">The membership of Microsoft BitLocker Administration and Monitoring roles can best be managed by creating security groups in ActiveDirectoryDomainServices, adding the appropriate administrator accounts to those groups, and then adding those security groups to the BitLocker Administration and Monitoring local groups.</span></span> <span data-ttu-id="86e4b-121">Weitere Informationen finden Sie unter [Verwalten von MBAM-Administrator Rollen](how-to-manage-mbam-administrator-roles-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="86e4b-121">For more information, see [How to Manage MBAM Administrator Roles](how-to-manage-mbam-administrator-roles-mbam-2.md).</span></span>

## <span data-ttu-id="86e4b-122">Weitere Ressourcen für die Planung von MBAM</span><span class="sxs-lookup"><span data-stu-id="86e4b-122">Other Resources for MBAM Planning</span></span>


[<span data-ttu-id="86e4b-123">Planen von MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="86e4b-123">Planning for MBAM 2.0</span></span>](planning-for-mbam-20-mbam-2.md)

[<span data-ttu-id="86e4b-124">Von MBAM 2.0 unterstützte Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="86e4b-124">MBAM 2.0 Supported Configurations</span></span>](mbam-20-supported-configurations-mbam-2.md)

 

 





