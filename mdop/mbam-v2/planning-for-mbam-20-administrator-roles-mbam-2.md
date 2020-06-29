---
title: Planen der Administratorrollen für MBAM 2.0
description: Planen der Administratorrollen für MBAM 2.0
author: dansimp
ms.assetid: 6f813297-6479-42d3-a21b-896d54466b5b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a89a04c0ef074407dc3cd081d351d44023e65e70
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810828"
---
# <span data-ttu-id="d2387-103">Planen der Administratorrollen für MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="d2387-103">Planning for MBAM 2.0 Administrator Roles</span></span>


<span data-ttu-id="d2387-104">In diesem Thema werden die verfügbaren Administratorrollen aufgelistet und beschrieben, die in Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) sowie die Serverspeicherorte, an denen die lokalen Gruppen erstellt werden, verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="d2387-104">This topic lists and describes the available administrator roles that are available in Microsoft BitLocker Administration and Monitoring (MBAM) as well as the server locations where the local groups are created.</span></span>

## <span data-ttu-id="d2387-105">MBAM-Administrator Rollen</span><span class="sxs-lookup"><span data-stu-id="d2387-105">MBAM Administrator Roles</span></span>


<a href="" id="---------------mbam-system-administrators"></a> **<span data-ttu-id="d2387-106">MBAM-System Administratoren</span><span class="sxs-lookup"><span data-stu-id="d2387-106">MBAM System Administrators</span></span>**  
<span data-ttu-id="d2387-107">Administratoren in dieser Rolle haben Zugriff auf alle Features der Microsoft BitLocker-Verwaltung und-Überwachung.</span><span class="sxs-lookup"><span data-stu-id="d2387-107">Administrators in this role have access to all Microsoft BitLocker Administration and Monitoring features.</span></span> <span data-ttu-id="d2387-108">Die lokale Gruppe für diese Rolle ist auf dem Verwaltungs-und Überwachungs Server installiert.</span><span class="sxs-lookup"><span data-stu-id="d2387-108">The local group for this role is installed on the Administration and Monitoring Server.</span></span>

<a href="" id="---------------mbam-helpdesk-users"></a> **<span data-ttu-id="d2387-109">MBAM Helpdesk-Benutzer</span><span class="sxs-lookup"><span data-stu-id="d2387-109">MBAM Helpdesk Users</span></span>**  
<span data-ttu-id="d2387-110">Administratoren in dieser Rolle haben Zugriff auf die Helpdesk-Features von MBAM.</span><span class="sxs-lookup"><span data-stu-id="d2387-110">Administrators in this role have access to the Help Desk features from MBAM.</span></span> <span data-ttu-id="d2387-111">Die lokale Gruppe für diese Rolle ist auf dem Verwaltungs-und Überwachungs Server installiert.</span><span class="sxs-lookup"><span data-stu-id="d2387-111">The local group for this role is installed on the Administration and Monitoring Server.</span></span>

<a href="" id="---------------mbam-report-users"></a> **<span data-ttu-id="d2387-112">MBAM-Berichtsbenutzer</span><span class="sxs-lookup"><span data-stu-id="d2387-112">MBAM Report Users</span></span>**  
<span data-ttu-id="d2387-113">Administratoren in dieser Rolle haben Zugriff auf die Konformitäts-und Überwachungsberichte von MBAM.</span><span class="sxs-lookup"><span data-stu-id="d2387-113">Administrators in this role have access to the Compliance and Audit Reports from MBAM.</span></span> <span data-ttu-id="d2387-114">Die lokale Gruppe für diese Rolle ist auf der Verwaltungs-und Überwachungsserver-, Konformitäts-und Überwachungsdatenbank sowie auf dem Server installiert, auf dem die Konformitäts-und Überwachungsberichte gehostet werden.</span><span class="sxs-lookup"><span data-stu-id="d2387-114">The local group for this role is installed on the Administration and Monitoring Server, Compliance and Audit Database, and on the server that hosts the Compliance and Audit Reports.</span></span>

<a href="" id="---------------mbam-advanced-helpdesk-users"></a> **<span data-ttu-id="d2387-115">MBAM Advanced Helpdesk-Benutzer</span><span class="sxs-lookup"><span data-stu-id="d2387-115">MBAM Advanced Helpdesk Users</span></span>**  
<span data-ttu-id="d2387-116">Administratoren in dieser Rolle haben erhöhten Zugriff auf die Helpdesk-Features von MBAM.</span><span class="sxs-lookup"><span data-stu-id="d2387-116">Administrators in this role have increased access to the Help Desk features from MBAM.</span></span> <span data-ttu-id="d2387-117">Die lokale Gruppe für diese Rolle ist auf dem Verwaltungs-und Überwachungs Server installiert.</span><span class="sxs-lookup"><span data-stu-id="d2387-117">The local group for this role is installed on the Administration and Monitoring Server.</span></span> <span data-ttu-id="d2387-118">Wenn ein Benutzer Mitglied sowohl von MBAM Helpdesk-Benutzern als auch von MBAM Advanced Helpdesk-Benutzern ist, überschreibt die MBAM Advanced Helpdesk-Benutzerberechtigungen die Benutzerberechtigungen des MBAM-Helpdesks.</span><span class="sxs-lookup"><span data-stu-id="d2387-118">If a user is a member of both MBAM Helpdesk Users and MBAM Advanced Helpdesk Users, the MBAM Advanced Helpdesk Users permissions will override the MBAM Helpdesk User permissions.</span></span>

<span data-ttu-id="d2387-119">**Wichtig**  Damit Berichte angezeigt werden können, muss ein Administrator ein Mitglied der Sicherheitsgruppe **MBAM-Berichtsbenutzer** in den Verwaltungs-und Überwachungsserver-, Konformitäts-und Überwachungsdatenbanken sowie auf dem Server sein, der das Feature Konformitäts-und Überwachungsberichte hostet.</span><span class="sxs-lookup"><span data-stu-id="d2387-119">**Important** To view reports, an administrative user must be a member of the **MBAM Report Users** security group on the Administration and Monitoring Server, Compliance and Audit Database, and on the server that hosts the Compliance and Audit Reports feature.</span></span> <span data-ttu-id="d2387-120">Als bewährte Methode können Sie eine Sicherheitsgruppe in Active Directory-Domänendiensten mit Rechten für die Sicherheitsgruppe **MBAM-Berichtsbenutzer** auf dem Verwaltungs-und Überwachungsserver und dem Server erstellen, auf dem die Konformitäts-und Überwachungsberichte gehostet werden.</span><span class="sxs-lookup"><span data-stu-id="d2387-120">As a best practice, create a security group in Active Directory Domain Services with rights on the local **MBAM Report Users** security group on both the Administration and Monitoring Server and the server that hosts the Compliance and Audit Reports.</span></span>

 

## <span data-ttu-id="d2387-121">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="d2387-121">Related topics</span></span>


[<span data-ttu-id="d2387-122">Vorbereiten der Umgebung für MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="d2387-122">Preparing your Environment for MBAM 2.0</span></span>](preparing-your-environment-for-mbam-20-mbam-2.md)

 

 





