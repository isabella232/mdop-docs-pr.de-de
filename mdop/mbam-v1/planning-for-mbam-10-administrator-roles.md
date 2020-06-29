---
title: Planen der Administratorrollen für MBAM 1.0
description: Planen der Administratorrollen für MBAM 1.0
author: dansimp
ms.assetid: 95be0eb4-25e9-43ca-a8e7-27373d35544d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 104d650824330ea990881c520a7811511f496dd1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811425"
---
# <span data-ttu-id="dd4ec-103">Planen der Administratorrollen für MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="dd4ec-103">Planning for MBAM 1.0 Administrator Roles</span></span>


<span data-ttu-id="dd4ec-104">Dieses Thema enthält und beschreibt die Administratorrollen, die in Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) verfügbar sind, sowie die Serverspeicherorte, an denen die lokalen Gruppen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="dd4ec-104">This topic includes and describes the administrator roles that are available in Microsoft BitLocker Administration and Monitoring (MBAM), as well as the server locations where the local groups are created.</span></span>

## <span data-ttu-id="dd4ec-105">MBAM-Administrator Rollen</span><span class="sxs-lookup"><span data-stu-id="dd4ec-105">MBAM Administrator roles</span></span>


<a href="" id="---------------mbam-system-administrators"></a> **<span data-ttu-id="dd4ec-106">MBAM-System Administratoren</span><span class="sxs-lookup"><span data-stu-id="dd4ec-106">MBAM System Administrators</span></span>**  
<span data-ttu-id="dd4ec-107">Administratoren in dieser Rolle haben Zugriff auf alle MBAM-Features.</span><span class="sxs-lookup"><span data-stu-id="dd4ec-107">Administrators in this role have access to all MBAM features.</span></span> <span data-ttu-id="dd4ec-108">Die lokale Gruppe für diese Rolle ist auf dem Verwaltungs-und Überwachungs Server installiert.</span><span class="sxs-lookup"><span data-stu-id="dd4ec-108">The local group for this role is installed on the Administration and Monitoring Server.</span></span>

<a href="" id="---------------mbam-hardware-users"></a> **<span data-ttu-id="dd4ec-109">MBAM-Hardware Benutzer</span><span class="sxs-lookup"><span data-stu-id="dd4ec-109">MBAM Hardware Users</span></span>**  
<span data-ttu-id="dd4ec-110">Administratoren in dieser Rolle haben Zugriff auf die Features der Hardware Funktion von MBAM.</span><span class="sxs-lookup"><span data-stu-id="dd4ec-110">Administrators in this role have access to the Hardware Capability features from MBAM.</span></span> <span data-ttu-id="dd4ec-111">Die lokale Gruppe für diese Rolle ist auf dem Verwaltungs-und Überwachungs Server installiert.</span><span class="sxs-lookup"><span data-stu-id="dd4ec-111">The local group for this role is installed on the Administration and Monitoring Server.</span></span>

<a href="" id="---------------mbam-helpdesk-users"></a> **<span data-ttu-id="dd4ec-112">MBAM Helpdesk-Benutzer</span><span class="sxs-lookup"><span data-stu-id="dd4ec-112">MBAM Helpdesk Users</span></span>**  
<span data-ttu-id="dd4ec-113">Administratoren in dieser Rolle haben Zugriff auf die Helpdesk-Features von MBAM.</span><span class="sxs-lookup"><span data-stu-id="dd4ec-113">Administrators in this role have access to the Helpdesk features from MBAM.</span></span> <span data-ttu-id="dd4ec-114">Die lokale Gruppe für diese Rolle ist auf dem Verwaltungs-und Überwachungs Server installiert.</span><span class="sxs-lookup"><span data-stu-id="dd4ec-114">The local group for this role is installed on the Administration and Monitoring Server.</span></span>

<a href="" id="---------------mbam--report-users"></a> **<span data-ttu-id="dd4ec-115">MBAM-Berichtsbenutzer</span><span class="sxs-lookup"><span data-stu-id="dd4ec-115">MBAM Report Users</span></span>**  
<span data-ttu-id="dd4ec-116">Administratoren in dieser Rolle haben Zugriff auf das Feature Konformitäts-und Überwachungsberichte von MBAM.</span><span class="sxs-lookup"><span data-stu-id="dd4ec-116">Administrators in this role have access to the Compliance and Audit Reports feature from MBAM.</span></span> <span data-ttu-id="dd4ec-117">Die lokale Gruppe für diese Rolle ist auf der Verwaltungs-und Überwachungsserver-, Konformitäts-und Überwachungsdatenbank sowie auf dem Server installiert, auf dem die Konformitäts-und Überwachungsberichte gehostet werden.</span><span class="sxs-lookup"><span data-stu-id="dd4ec-117">The local group for this role is installed on the Administration and Monitoring Server, Compliance and Audit Database, and on the server that hosts the Compliance and Audit Reports.</span></span>

<a href="" id="---------------mbam--advanced-helpdesk-users"></a> **<span data-ttu-id="dd4ec-118">MBAM Advanced Helpdesk-Benutzer</span><span class="sxs-lookup"><span data-stu-id="dd4ec-118">MBAM Advanced Helpdesk Users</span></span>**  
<span data-ttu-id="dd4ec-119">Administratoren in dieser Rolle haben erhöhten Zugriff auf die Helpdesk-Features von MBAM.</span><span class="sxs-lookup"><span data-stu-id="dd4ec-119">Administrators in this role have increased access to the Helpdesk features from MBAM.</span></span> <span data-ttu-id="dd4ec-120">Die lokale Gruppe für diese Rolle ist auf dem Verwaltungs-und Überwachungs Server installiert.</span><span class="sxs-lookup"><span data-stu-id="dd4ec-120">The local group for this role is installed on the Administration and Monitoring Server.</span></span> <span data-ttu-id="dd4ec-121">Wenn ein Benutzer Mitglied sowohl von MBAM Helpdesk-Benutzern als auch von MBAM Advanced Helpdesk-Benutzern ist, überschreibt die Berechtigung MBAM Advanced Helpdesk-Benutzer die Berechtigungen des MBAM-Helpdesk-Benutzers.</span><span class="sxs-lookup"><span data-stu-id="dd4ec-121">If a user is a member of both MBAM Helpdesk Users and MBAM Advanced Helpdesk Users, the MBAM Advanced Helpdesk Users permissions will overwrite the MBAM Helpdesk User permissions.</span></span>

<span data-ttu-id="dd4ec-122">**Wichtig**  Damit die Berichte angezeigt werden können, muss ein Administrator ein Mitglied der Sicherheitsgruppe **MBAM-Berichtsbenutzer** in den Verwaltungs-und Überwachungs Servern, der Kompatibilitäts-und Überwachungsdatenbank sowie auf dem Server sein, der das Feature Compliance und Berichte hostet.</span><span class="sxs-lookup"><span data-stu-id="dd4ec-122">**Important** To view the reports, an administrative user must be a member of the **MBAM Report Users** security group on the Administration and Monitoring Server, Compliance and Audit Database, and on the server that hosts the Compliance and Reports feature.</span></span> <span data-ttu-id="dd4ec-123">Als bewährte Methode können Sie eine Sicherheitsgruppe in Active Directory mit Rechten für die lokale **MBAM-Berichtsbenutzer** -Sicherheitsgruppe sowohl auf dem Verwaltungs-und Überwachungsserver als auch auf dem Server erstellen, auf dem die Konformität und die Berichte gehostet werden.</span><span class="sxs-lookup"><span data-stu-id="dd4ec-123">As a best practice, create a security group in Active Directory with rights on the local **MBAM Report Users** security group on both the Administration and Monitoring Server and on the server that hosts the Compliance and Reports.</span></span>

 

## <span data-ttu-id="dd4ec-124">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="dd4ec-124">Related topics</span></span>


[<span data-ttu-id="dd4ec-125">Vorbereiten der Umgebung für MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="dd4ec-125">Preparing your Environment for MBAM 1.0</span></span>](preparing-your-environment-for-mbam-10.md)

 

 





