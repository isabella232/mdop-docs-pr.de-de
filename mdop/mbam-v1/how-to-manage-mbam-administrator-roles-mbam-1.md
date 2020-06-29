---
title: So verwalten Sie MBAM-Administratorrollen
description: So verwalten Sie MBAM-Administratorrollen
author: dansimp
ms.assetid: c0f25a42-dbff-418d-a776-4fe23ee07d16
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9d00b8ebf66d2b066afae33e67298691285ce9fa
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804625"
---
# <span data-ttu-id="75a6c-103">So verwalten Sie MBAM-Administratorrollen</span><span class="sxs-lookup"><span data-stu-id="75a6c-103">How to Manage MBAM Administrator Roles</span></span>


<span data-ttu-id="75a6c-104">Nachdem das Setup für Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) für alle Server Features abgeschlossen ist, müssen Administrator Benutzern Zugriff auf diese Server Features gewährt werden.</span><span class="sxs-lookup"><span data-stu-id="75a6c-104">After Microsoft BitLocker Administration and Monitoring (MBAM) Setup is complete for all server features, administrative users must be granted access to these server features.</span></span> <span data-ttu-id="75a6c-105">Als bewährte Methode sollten Administratoren, die die MBAM-Server Features verwalten oder verwenden, Active Directory-Sicherheitsgruppen zugewiesen werden, und diese Gruppen sollten der entsprechenden administrativen lokalen Gruppe MBAM hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="75a6c-105">As a best practice, administrators who will manage or use MBAM server features, should be assigned to Active Directory security groups and then those groups should be added to the appropriate MBAM administrative local group.</span></span>

**<span data-ttu-id="75a6c-106">So verwalten Sie MBAM-Administrator Rollenmitgliedschaften</span><span class="sxs-lookup"><span data-stu-id="75a6c-106">To manage MBAM Administrator Role memberships</span></span>**

1.  <span data-ttu-id="75a6c-107">Zuweisen von administrativen Benutzern zu Sicherheitsgruppen in ActiveDirectoryDomain-Diensten.</span><span class="sxs-lookup"><span data-stu-id="75a6c-107">Assign administrative users to security groups in ActiveDirectoryDomain Services.</span></span>

2.  <span data-ttu-id="75a6c-108">Fügen Sie den Rollen für MBAM administrative lokale Gruppen auf dem Microsoft BitLocker-Verwaltungs-und-Überwachungsserver für die jeweiligen Features ActiveDirectoryDomain-Dienst Sicherheitsgruppen hinzu.</span><span class="sxs-lookup"><span data-stu-id="75a6c-108">Add ActiveDirectoryDomain Services security groups to the roles for MBAM administrative local groups on the Microsoft BitLocker Administration and Monitoring server for the respective features.</span></span> <span data-ttu-id="75a6c-109">Die Benutzerrollen lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="75a6c-109">The user roles are as follows:</span></span>

    -   <span data-ttu-id="75a6c-110">**MBAM-System Administratoren** haben Zugriff auf alle Microsoft BitLocker-Verwaltungs-und-Überwachungsfeatures auf der MBAM-Verwaltungswebsite.</span><span class="sxs-lookup"><span data-stu-id="75a6c-110">**MBAM System Administrators** have access to all Microsoft BitLocker Administration and Monitoring features in the MBAM administration website.</span></span>

    -   <span data-ttu-id="75a6c-111">**MBAM-Hardware Benutzer** können auf die Hardware Kompatibilitätsfeatures auf der MBAM-Verwaltungswebsite zugreifen.</span><span class="sxs-lookup"><span data-stu-id="75a6c-111">**MBAM Hardware Users** have access to the Hardware Compatibility features in the MBAM administration website.</span></span>

    -   <span data-ttu-id="75a6c-112">**MBAM Helpdesk-Benutzer** haben Zugriff auf die Optionen "TPM verwalten" und "Drive Recovery" auf der MBAM-Verwaltungswebsite, müssen aber alle Felder ausfüllen, wenn Sie eine der beiden Optionen verwenden.</span><span class="sxs-lookup"><span data-stu-id="75a6c-112">**MBAM Helpdesk Users** have access to the Manage TPM and Drive Recovery options in the MBAM administration website, but must fill in all fields when they use either option.</span></span>

    -   <span data-ttu-id="75a6c-113">**MBAM-Berichtsbenutzer** haben Zugriff auf die Konformitäts-und Überwachungsberichte auf der MBAM-Verwaltungswebsite.</span><span class="sxs-lookup"><span data-stu-id="75a6c-113">**MBAM Report Users** have access to the Compliance and Audit reports in the MBAM administration website.</span></span>

    -   <span data-ttu-id="75a6c-114">**MBAM Advanced Helpdesk verwendet** Zugriff auf die Optionen "TPM verwalten" und "Drive Recovery" auf der MBAM-Verwaltungswebsite.</span><span class="sxs-lookup"><span data-stu-id="75a6c-114">**MBAM Advanced Helpdesk Uses** have access to the Manage TPM and Drive Recovery options in the MBAM administration website.</span></span> <span data-ttu-id="75a6c-115">Diese Benutzer müssen nicht alle Felder ausfüllen, wenn Sie eine der beiden Optionen verwenden.</span><span class="sxs-lookup"><span data-stu-id="75a6c-115">These users are not required to fill in all fields when they use either option.</span></span>

    <span data-ttu-id="75a6c-116">Weitere Informationen zu Rollen für die Microsoft BitLocker-Verwaltung und-Überwachung finden Sie unter [Planen von MBAM 1,0-Administrator Rollen](planning-for-mbam-10-administrator-roles.md).</span><span class="sxs-lookup"><span data-stu-id="75a6c-116">For more information about roles for Microsoft BitLocker Administration and Monitoring, see [Planning for MBAM 1.0 Administrator Roles](planning-for-mbam-10-administrator-roles.md).</span></span>

## <span data-ttu-id="75a6c-117">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="75a6c-117">Related topics</span></span>


[<span data-ttu-id="75a6c-118">Verwalten von MBAM 1.0-Funktionen</span><span class="sxs-lookup"><span data-stu-id="75a6c-118">Administering MBAM 1.0 Features</span></span>](administering-mbam-10-features.md)

 

 





