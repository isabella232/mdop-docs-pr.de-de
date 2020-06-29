---
title: So verwalten Sie MBAM-Administratorrollen
description: So verwalten Sie MBAM-Administratorrollen
author: dansimp
ms.assetid: 813ac0c4-3cf9-47af-b4cb-9395fd915e5c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 14e9128904b448b20e0596a2630627b7ca8e711d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810963"
---
# <span data-ttu-id="9a602-103">So verwalten Sie MBAM-Administratorrollen</span><span class="sxs-lookup"><span data-stu-id="9a602-103">How to Manage MBAM Administrator Roles</span></span>


<span data-ttu-id="9a602-104">Nachdem die Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) für alle Server Features abgeschlossen ist, müssen Administrator Benutzern Zugriff auf Sie gewährt werden.</span><span class="sxs-lookup"><span data-stu-id="9a602-104">After Microsoft BitLocker Administration and Monitoring (MBAM) Setup is complete for all server features, administrative users will have to be granted access to them.</span></span> <span data-ttu-id="9a602-105">Als bewährte Methode sollten Administratoren, die die Microsoft BitLocker-Verwaltungs-und-Überwachungs Server Features verwalten oder verwenden, den Sicherheitsgruppen für Domänendienste zugewiesen werden, und diese Gruppen sollten dann der entsprechenden administrativen lokalen Gruppe MBAM hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="9a602-105">As a best practice, administrators who will manage or use Microsoft BitLocker Administration and Monitoring Server features should be assigned to Domain Services security groups, and then those groups should be added to the appropriate MBAM administrative local group.</span></span>

**<span data-ttu-id="9a602-106">So verwalten Sie MBAM-Administrator Rollenmitgliedschaften</span><span class="sxs-lookup"><span data-stu-id="9a602-106">To manage MBAM Administrator Role memberships</span></span>**

1.  <span data-ttu-id="9a602-107">Zuweisen von administrativen Benutzern zu Sicherheitsgruppen in den Active Directory-Domänendiensten</span><span class="sxs-lookup"><span data-stu-id="9a602-107">Assign administrative users to security groups in ActiveDirectory Domain Services.</span></span>

2.  <span data-ttu-id="9a602-108">Fügen Sie den Rollen für MBAM administrative lokale Gruppen auf dem MBAM-Server für die jeweiligen Features Active Directory-Sicherheitsgruppen hinzu.</span><span class="sxs-lookup"><span data-stu-id="9a602-108">Add ActiveDirectory security groups to the roles for MBAM administrative local groups on the MBAM server for the respective features.</span></span>

    -   <span data-ttu-id="9a602-109">**MBAM-System Administratoren** haben Zugriff auf alle MBAM-Features auf der MBAM-Verwaltungs-und-Überwachungs Website.</span><span class="sxs-lookup"><span data-stu-id="9a602-109">**MBAM System Administrators** have access to all MBAM features in the MBAM Administration and Monitoring website.</span></span>

    -   <span data-ttu-id="9a602-110">**MBAM Helpdesk-Benutzer** haben Zugriff auf die Optionen "TPM verwalten" und "Drive Recovery" auf der MBAM-Website, müssen aber alle Felder ausfüllen, wenn Sie eine der beiden Optionen verwenden.</span><span class="sxs-lookup"><span data-stu-id="9a602-110">**MBAM Helpdesk Users** have access to the Manage TPM and Drive Recovery options in the MBAM Administration and Monitoring website, but must fill in all fields when they use either option.</span></span>

    -   <span data-ttu-id="9a602-111">**MBAM-Berichtsbenutzer** haben Zugriff auf die Konformitäts-und Überwachungsberichte auf der MBAM-Website.</span><span class="sxs-lookup"><span data-stu-id="9a602-111">**MBAM Report Users** have access to the Compliance and Audit reports in the MBAM Administration and Monitoring website.</span></span>

    -   <span data-ttu-id="9a602-112">**MBAM Advanced Helpdesk-Benutzer** haben Zugriff auf die Optionen "TPM verwalten" und "Drive Recovery" auf der MBAM-Website für Verwaltung und Überwachung, sind aber nicht verpflichtet, alle Felder auszufüllen, wenn Sie eine der beiden Optionen verwenden.</span><span class="sxs-lookup"><span data-stu-id="9a602-112">**MBAM Advanced Helpdesk Users** have access to the Manage TPM and Drive Recovery options in the MBAM Administration and Monitoring website, but are not required to fill in all fields when they use either option.</span></span>

    <span data-ttu-id="9a602-113">Weitere Informationen zu Rollen für die Microsoft BitLocker-Verwaltung und-Überwachung finden Sie unter [Planen von MBAM 2,0-Administrator Rollen](planning-for-mbam-20-administrator-roles-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="9a602-113">For more information about roles for Microsoft BitLocker Administration and Monitoring, see [Planning for MBAM 2.0 Administrator Roles](planning-for-mbam-20-administrator-roles-mbam-2.md).</span></span>

## <span data-ttu-id="9a602-114">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="9a602-114">Related topics</span></span>


[<span data-ttu-id="9a602-115">Verwalten von MBAM 2.0-Funktionen</span><span class="sxs-lookup"><span data-stu-id="9a602-115">Administering MBAM 2.0 Features</span></span>](administering-mbam-20-features-mbam-2.md)

 

 





