---
title: Sichern des Archivs
description: Sichern des Archivs
author: dansimp
ms.assetid: 538d85eb-3596-4c1d-bbd7-26bc28857c28
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8c6888d61e126d603aefa4e818f1070c5a493ea6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807816"
---
# <span data-ttu-id="91f4c-103">Sichern des Archivs</span><span class="sxs-lookup"><span data-stu-id="91f4c-103">Back Up the Archive</span></span>


<span data-ttu-id="91f4c-104">Um bei der Wiederherstellung des Archivs für erweiterte Gruppenrichtlinienverwaltung (AGPM) bei einem Notfall zu helfen, sollte ein AGPM-Administrator (Vollzugriff) das Archiv häufig sichern.</span><span class="sxs-lookup"><span data-stu-id="91f4c-104">To help in the recovery of the archive for Advanced Group Policy Management (AGPM) if there is a disaster, an AGPM Administrator (Full Control) should back up the archive frequently.</span></span> <span data-ttu-id="91f4c-105">Standardmäßig wird das Archiv in%ProgramData%\\Microsoft\\AGPM. erstellt.</span><span class="sxs-lookup"><span data-stu-id="91f4c-105">By default, the archive is created in %ProgramData%\\Microsoft\\AGPM.</span></span> <span data-ttu-id="91f4c-106">Sie können jedoch während der Einrichtung des Microsoft Advanced Group Policy Management-Servers einen anderen Pfad angeben.</span><span class="sxs-lookup"><span data-stu-id="91f4c-106">However, you can specify a different path during the setup of Microsoft Advanced Group Policy Management - Server.</span></span>

<span data-ttu-id="91f4c-107">Ein Benutzerkonto, das Zugriff auf den AGPM-Server hat – den Computer, auf dem der AGPM-Dienst installiert ist – und auf den Ordner, der das Archiv enthält, ist erforderlich, um dieses Verfahren auszuführen.</span><span class="sxs-lookup"><span data-stu-id="91f4c-107">A user account that has access to both the AGPM Server—the computer on which the AGPM Service is installed—and to the folder that contains the archive is required to complete this procedure.</span></span>

**<span data-ttu-id="91f4c-108">So sichern Sie das Archiv</span><span class="sxs-lookup"><span data-stu-id="91f4c-108">To back up the archive</span></span>**

1.  <span data-ttu-id="91f4c-109">Beenden Sie den AGPM-Dienst.</span><span class="sxs-lookup"><span data-stu-id="91f4c-109">Stop the AGPM Service.</span></span> <span data-ttu-id="91f4c-110">Weitere Informationen finden Sie unter [starten und Beenden des AGPM-Diensts](start-and-stop-the-agpm-service-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="91f4c-110">For more information, see [Start and Stop the AGPM Service](start-and-stop-the-agpm-service-agpm40.md).</span></span>

2.  <span data-ttu-id="91f4c-111">Sichern Sie den Archivordner mithilfe von Windows-Explorer, xcopy, Windows Server®-Sicherung oder einem anderen Sicherungstool.</span><span class="sxs-lookup"><span data-stu-id="91f4c-111">Back up the archive folder by using Windows Explorer, Xcopy, Windows Server® Backup, or another backup tool.</span></span> <span data-ttu-id="91f4c-112">Stellen Sie sicher, dass Sie versteckte, System-und schreibgeschützte Dateien sichern.</span><span class="sxs-lookup"><span data-stu-id="91f4c-112">Make sure that you back up hidden, system, and read-only files.</span></span>

3.  <span data-ttu-id="91f4c-113">Speichern Sie die Archivsicherung an einem sicheren Ort.</span><span class="sxs-lookup"><span data-stu-id="91f4c-113">Store the archive backup in a secure location.</span></span>

4.  <span data-ttu-id="91f4c-114">Starten Sie den AGPM-Dienst erneut.</span><span class="sxs-lookup"><span data-stu-id="91f4c-114">Restart the AGPM Service.</span></span> <span data-ttu-id="91f4c-115">Weitere Informationen finden Sie unter [starten und Beenden des AGPM-Diensts](start-and-stop-the-agpm-service-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="91f4c-115">For more information, see [Start and Stop the AGPM Service](start-and-stop-the-agpm-service-agpm40.md).</span></span>

<span data-ttu-id="91f4c-116">**Hinweis**  Wenn ein AGPM-Administrator das Archiv selten zurückgibt, sind die Gruppenrichtlinienobjekte (Group Policy Objects, GPOs) in der Archivsicherung nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="91f4c-116">**Note** If an AGPM Administrator backs up the archive infrequently, the Group Policy Objects (GPOs) in the archive backup will not be current.</span></span> <span data-ttu-id="91f4c-117">Um sicherzustellen, dass die Archivsicherung aktuell ist, sichern Sie das Archiv im Rahmen der täglichen Backup-Strategie Ihrer Organisation.</span><span class="sxs-lookup"><span data-stu-id="91f4c-117">To better ensure that the archive backup is current, back up the archive as part of your organization’s daily backup strategy.</span></span>

 

### <span data-ttu-id="91f4c-118">Weitere Verweise</span><span class="sxs-lookup"><span data-stu-id="91f4c-118">Additional references</span></span>

-   [<span data-ttu-id="91f4c-119">Wiederherstellen des Archivs aus einer Sicherung</span><span class="sxs-lookup"><span data-stu-id="91f4c-119">Restore the Archive from a Backup</span></span>](restore-the-archive-from-a-backup-agpm40.md)

-   [<span data-ttu-id="91f4c-120">Verschieben des AGPM-Servers und -Archivs</span><span class="sxs-lookup"><span data-stu-id="91f4c-120">Move the AGPM Server and the Archive</span></span>](move-the-agpm-server-and-the-archive-agpm40.md)

-   [<span data-ttu-id="91f4c-121">Verwalten des Archivs</span><span class="sxs-lookup"><span data-stu-id="91f4c-121">Managing the Archive</span></span>](managing-the-archive-agpm40.md)

 

 





