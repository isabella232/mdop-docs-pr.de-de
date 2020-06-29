---
title: Vorbereiten der Umgebung für MBAM 1.0
description: Vorbereiten der Umgebung für MBAM 1.0
author: dansimp
ms.assetid: 915f7c3c-70ad-4a90-a434-73e7fba97ecb
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9a2de4e825d5c89aeabcf57d78dc856bacb03e11
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809808"
---
# <span data-ttu-id="92409-103">Vorbereiten der Umgebung für MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="92409-103">Preparing your Environment for MBAM 1.0</span></span>


<span data-ttu-id="92409-104">Bevor Sie mit dem Setup für die Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) beginnen, stellen Sie sicher, dass Sie die erforderlichen Voraussetzungen für die Installation des Produkts erfüllt haben.</span><span class="sxs-lookup"><span data-stu-id="92409-104">Before you begin the Microsoft BitLocker Administration and Monitoring (MBAM) Setup, make sure that you have met the necessary prerequisites to install the product.</span></span> <span data-ttu-id="92409-105">Wenn Sie die Voraussetzungen im Voraus kennen, können Sie das Produkt effizient bereitstellen und seine Features aktivieren, die die geschäftlichen Ziele Ihrer Organisation effektiver unterstützen können.</span><span class="sxs-lookup"><span data-stu-id="92409-105">If you know the prerequisites in advance, you can efficiently deploy the product and enable its features, which can support the business objectives of your organization more effectively.</span></span>

## <span data-ttu-id="92409-106">Überprüfen der MBAM 1,0-Bereitstellungsvoraussetzungen</span><span class="sxs-lookup"><span data-stu-id="92409-106">Review MBAM 1.0 deployment prerequisites</span></span>


<span data-ttu-id="92409-107">Der MBAM-Client und alle MBAM-Server Features verfügen über bestimmte Voraussetzungen, die erfüllt sein müssen, bevor Sie erfolgreich installiert werden können.</span><span class="sxs-lookup"><span data-stu-id="92409-107">The MBAM Client and each of the MBAM Server features have specific prerequisites that must be met before they can be successfully installed.</span></span>

<span data-ttu-id="92409-108">Um eine erfolgreiche Installation von MBAM-Clients und MBAM-Server Features zu gewährleisten, sollten Sie sicherstellen, dass Computer, die für die Installation von MBAM Client oder MBAM Server festgelegt wurden, ordnungsgemäß für MBAM Setup vorbereitet sind.</span><span class="sxs-lookup"><span data-stu-id="92409-108">To ensure successful installation of MBAM Clients and MBAM Server features, you should plan to ensure that computers specified for MBAM Client or MBAM Server feature installation are properly prepared for MBAM Setup.</span></span>

<span data-ttu-id="92409-109">**Hinweis**  MBAM-Setup überprüft, ob alle Voraussetzungen erfüllt sind, bevor die Installation gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="92409-109">**Note** MBAM Setup verifies if all prerequisites are met before installation starts.</span></span> <span data-ttu-id="92409-110">Wenn Sie nicht erfüllt sind, schlägt Setup fehl.</span><span class="sxs-lookup"><span data-stu-id="92409-110">If they are not met, Setup will fail.</span></span>

 

[<span data-ttu-id="92409-111">Bereitstellungsvoraussetzungen für MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="92409-111">MBAM 1.0 Deployment Prerequisites</span></span>](mbam-10-deployment-prerequisites.md)

## <span data-ttu-id="92409-112">Planen der MBAM 1,0-Gruppenrichtlinienanforderungen</span><span class="sxs-lookup"><span data-stu-id="92409-112">Plan for MBAM 1.0 Group Policy requirements</span></span>


<span data-ttu-id="92409-113">Bevor MBAM Clients im Unternehmen verwalten kann, müssen Sie die Gruppenrichtlinie für die Verschlüsselungsanforderungen Ihrer Umgebung definieren.</span><span class="sxs-lookup"><span data-stu-id="92409-113">Before MBAM can manage clients in the enterprise, you must define the Group Policy for the encryption requirements of your environment.</span></span>

<span data-ttu-id="92409-114">**Wichtig**  MBAM wird nicht mit Richtlinien für eigenständige BitLocker-Laufwerkverschlüsselung funktionieren.</span><span class="sxs-lookup"><span data-stu-id="92409-114">**Important** MBAM will not work with policies for stand-alone BitLocker drive encryption.</span></span> <span data-ttu-id="92409-115">Für MBAM muss eine Gruppenrichtlinie definiert werden. Andernfalls treten bei der BitLocker-Verschlüsselung und-Erzwingung Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="92409-115">Group Policy must be defined for MBAM; otherwise, the BitLocker encryption and enforcement will fail.</span></span>

 

[<span data-ttu-id="92409-116">Planen der Gruppenrichtlinienanforderungen für MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="92409-116">Planning for MBAM 1.0 Group Policy Requirements</span></span>](planning-for-mbam-10-group-policy-requirements.md)

## <span data-ttu-id="92409-117">Planen von MBAM 1,0-Administratorrollen</span><span class="sxs-lookup"><span data-stu-id="92409-117">Plan for MBAM 1.0 administrator roles</span></span>


<span data-ttu-id="92409-118">MBAM-Administratorrollen werden von lokalen Gruppen verwaltet, die von MBAM Setup erstellt werden, wenn Sie Folgendes installieren: BitLocker-Verwaltungs-und Überwachungs Server, das Feature Konformitäts-und Überwachungsberichte sowie die Datenbank für Konformitäts-und Überwachungs Status.</span><span class="sxs-lookup"><span data-stu-id="92409-118">MBAM administrator roles are managed by local groups that are created by MBAM Setup when you install the following: BitLocker Administration and Monitoring Server, the Compliance and Audit Reports feature, and the Compliance and Audit Status Database.</span></span>

<span data-ttu-id="92409-119">Die Mitgliedschaft in MBAM-Rollen kann effektiver verwaltet werden, wenn Sie in ActiveDirectoryDomainServices Sicherheitsgruppen erstellen, diesen Gruppen die entsprechenden Administratorkonten hinzufügen und diese Sicherheitsgruppen dann den lokalen MBAM-Gruppen hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="92409-119">The membership of MBAM roles can be managed more effectively if you create security groups in ActiveDirectoryDomainServices, add the appropriate administrator accounts to those groups, and then add those security groups to the MBAM local groups.</span></span> <span data-ttu-id="92409-120">Weitere Informationen finden Sie unter [Verwalten von MBAM-Administrator Rollen](how-to-manage-mbam-administrator-roles-mbam-1.md).</span><span class="sxs-lookup"><span data-stu-id="92409-120">For more information, see [How to Manage MBAM Administrator Roles](how-to-manage-mbam-administrator-roles-mbam-1.md).</span></span>

[<span data-ttu-id="92409-121">Planen der Administratorrollen für MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="92409-121">Planning for MBAM 1.0 Administrator Roles</span></span>](planning-for-mbam-10-administrator-roles.md)

## <span data-ttu-id="92409-122">Weitere Ressourcen für die Planung von MBAM</span><span class="sxs-lookup"><span data-stu-id="92409-122">Other resources for MBAM planning</span></span>


[<span data-ttu-id="92409-123">Planen von MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="92409-123">Planning for MBAM 1.0</span></span>](planning-for-mbam-10.md)

 

 





