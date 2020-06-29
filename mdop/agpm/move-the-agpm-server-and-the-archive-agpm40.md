---
title: Verschieben des AGPM-Servers und -Archivs
description: Verschieben des AGPM-Servers und -Archivs
author: dansimp
ms.assetid: 9ec48d3a-c293-45f0-8939-32ccdc062303
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 61ad2eb6e0ea46eef89379894a99469254e0fd5e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809412"
---
# <span data-ttu-id="ba40c-103">Verschieben des AGPM-Servers und -Archivs</span><span class="sxs-lookup"><span data-stu-id="ba40c-103">Move the AGPM Server and the Archive</span></span>


<span data-ttu-id="ba40c-104">Wenn Sie den AGPM-Server und den Server ersetzen, auf dem das Archiv gehostet wird, müssen Sie den AGPM-Dienst und das Archiv verschieben.</span><span class="sxs-lookup"><span data-stu-id="ba40c-104">If you are replacing the AGPM Server and the server on which the archive is hosted, you must move the AGPM Service and the archive.</span></span> <span data-ttu-id="ba40c-105">Wenn Sie möchten, können Sie den AGPM-Dienst und das Archiv separat verschieben.</span><span class="sxs-lookup"><span data-stu-id="ba40c-105">If you prefer, you can move the AGPM Service and the archive separately.</span></span>

**<span data-ttu-id="ba40c-106">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="ba40c-106">Note</span></span>**  
-   <span data-ttu-id="ba40c-107">Der AGPM-Server ist der Computer, auf dem der AGPM-Dienst gehostet wird, und der Computer, auf dem Microsoft Advanced Group Policy Management – Server installiert ist.</span><span class="sxs-lookup"><span data-stu-id="ba40c-107">The AGPM Server is the computer that hosts the AGPM Service and the computer on which Microsoft Advanced Group Policy Management – Server is installed.</span></span>

-   <span data-ttu-id="ba40c-108">Standardmäßig wird das Archiv auf dem AGPM-Server gehostet, doch Sie können stattdessen einen Archivierungspfad angeben, um ihn auf einem anderen Server zu hosten.</span><span class="sxs-lookup"><span data-stu-id="ba40c-108">By default, the archive is hosted on the AGPM Server, but you can specify an archive path to host it on another server instead.</span></span>

 

<span data-ttu-id="ba40c-109">Ein Benutzerkonto, das Mitglied der Gruppe der Domänenadministratoren ist und Zugriff auf die vorherigen und neuen AGPM-Server hat, ist erforderlich, um dieses Verfahren ausführen zu können.</span><span class="sxs-lookup"><span data-stu-id="ba40c-109">A user account that is a member of the Domain Admins group and has access to the previous and new AGPM Servers is required to complete this procedure.</span></span> <span data-ttu-id="ba40c-110">Darüber hinaus müssen Sie die Anmeldeinformationen für das AGPM-Dienstkonto angeben, das vom neuen AGPM-Server verwendet werden soll, um dieses Verfahren ausführen zu können.</span><span class="sxs-lookup"><span data-stu-id="ba40c-110">Additionally, you must provide credentials for the AGPM Service Account to be used by the new AGPM Server to complete this procedure.</span></span>

**<span data-ttu-id="ba40c-111">So verschieben Sie den AGPM-Dienst und das Archiv auf einen anderen Server oder auf einen anderen Server</span><span class="sxs-lookup"><span data-stu-id="ba40c-111">To move the AGPM Service and the archive to a different server or servers</span></span>**

1.  <span data-ttu-id="ba40c-112">Sichern Sie das Archiv.</span><span class="sxs-lookup"><span data-stu-id="ba40c-112">Back up the archive.</span></span> <span data-ttu-id="ba40c-113">Weitere Informationen finden Sie unter [Sichern des Archivs](back-up-the-archive-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="ba40c-113">For more information, see [Back Up the Archive](back-up-the-archive-agpm40.md).</span></span>

2.  <span data-ttu-id="ba40c-114">Verschieben Sie den AGPM-Dienst:</span><span class="sxs-lookup"><span data-stu-id="ba40c-114">Move the AGPM Service:</span></span>

    1.  <span data-ttu-id="ba40c-115">Beenden Sie den AGPM-Dienst.</span><span class="sxs-lookup"><span data-stu-id="ba40c-115">Stop the AGPM Service.</span></span> <span data-ttu-id="ba40c-116">Weitere Informationen finden Sie unter [starten und Beenden des AGPM-Diensts](start-and-stop-the-agpm-service-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="ba40c-116">For more information, see [Start and Stop the AGPM Service](start-and-stop-the-agpm-service-agpm40.md).</span></span>

    2.  <span data-ttu-id="ba40c-117">Installieren Sie Microsoft Advanced Group Policy Management-Server auf dem neuen Server, der den AGPM-Dienst hosten soll.</span><span class="sxs-lookup"><span data-stu-id="ba40c-117">Install Microsoft Advanced Group Policy Management - Server on the new server that will host the AGPM Service.</span></span> <span data-ttu-id="ba40c-118">Während dieses Vorgangs geben Sie den neuen Archivierungspfad, den Speicherort für das Archiv, in Bezug auf den AGPM-Server an.</span><span class="sxs-lookup"><span data-stu-id="ba40c-118">During this process, you specify the new archive path, the location for the archive in relation to the AGPM Server.</span></span> <span data-ttu-id="ba40c-119">Weitere Informationen finden Sie unter [Schritt-für-Schritt-Anleitung für Microsoft Advanced Group Policy Management 4,0](https://go.microsoft.com/fwlink/?LinkId=153505) ( https://go.microsoft.com/fwlink/?LinkId=153505) und [Planungshandbuch für Microsoft Advanced Group Policy Management](https://go.microsoft.com/fwlink/?LinkId=156883) ( https://go.microsoft.com/fwlink/?LinkId=156883) .</span><span class="sxs-lookup"><span data-stu-id="ba40c-119">For more information, see [Step-by-Step Guide for Microsoft Advanced Group Policy Management 4.0](https://go.microsoft.com/fwlink/?LinkId=153505) (https://go.microsoft.com/fwlink/?LinkId=153505) and [Planning Guide for Microsoft Advanced Group Policy Management](https://go.microsoft.com/fwlink/?LinkId=156883) (https://go.microsoft.com/fwlink/?LinkId=156883).</span></span>

    3.  <span data-ttu-id="ba40c-120">Entweder ein AGPM-Administrator (Vollzugriff) muss die AGPM-Serververbindung für alle Gruppenrichtlinienadministratoren konfigurieren, die den neuen AGPM-Server verwenden und die Verbindung für den alten AGPM-Server entfernen, da sonst jeder Gruppenrichtlinienadministrator die neue AGPM-Serververbindung manuell konfigurieren und die alte AGPM-Serververbindung für das AGPM-Snap-in auf dem Computer entfernen muss.</span><span class="sxs-lookup"><span data-stu-id="ba40c-120">Either an AGPM Administrator (Full Control) must configure the AGPM Server connection for all Group Policy administrators who will use the new AGPM Server and remove the connection for the old AGPM Server, or else each Group Policy administrator must manually configure the new AGPM Server connection and remove the old AGPM Server connection for the AGPM snap-in on their computer.</span></span> <span data-ttu-id="ba40c-121">Weitere Informationen finden Sie unter [Konfigurieren von AGPM-Server Verbindungen](configure-agpm-server-connections-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="ba40c-121">For more information, see [Configure AGPM Server Connections](configure-agpm-server-connections-agpm40.md).</span></span>

        <span data-ttu-id="ba40c-122">**Hinweis**  Als bewährte Methode sollten Sie Microsoft Advanced Group Policy Management – Server vom vorherigen AGPM-Server deinstallieren.</span><span class="sxs-lookup"><span data-stu-id="ba40c-122">**Note** As a best practice, you should uninstall Microsoft Advanced Group Policy Management – Server from the previous AGPM Server.</span></span> <span data-ttu-id="ba40c-123">Dadurch wird sichergestellt, dass der AGPM-Dienst nicht versehentlich auf diesem Server neu gestartet werden kann und möglicherweise Verwirrung verursacht, wenn keine AGPM-Serververbindungen mehr vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="ba40c-123">This will ensure that the AGPM Service cannot be unintentionally restarted on that server and potentially cause confusion if any AGPM Server connections to it remain.</span></span>

         

3.  <span data-ttu-id="ba40c-124">Kopieren Sie das Archiv von der Sicherung auf den neuen Server, der das Archiv hosten soll.</span><span class="sxs-lookup"><span data-stu-id="ba40c-124">Copy the archive from the backup to the new server that will host the archive.</span></span> <span data-ttu-id="ba40c-125">Weitere Informationen finden Sie unter [Wiederherstellen des Archivs aus einer Sicherung](restore-the-archive-from-a-backup-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="ba40c-125">For more information, see [Restore the Archive from a Backup](restore-the-archive-from-a-backup-agpm40.md).</span></span>

    <span data-ttu-id="ba40c-126">**Wichtig**  Wenn Sie das Archiv verschoben haben, ohne den AGPM-Dienst zur gleichen Zeit zu verschieben:</span><span class="sxs-lookup"><span data-stu-id="ba40c-126">**Important** If you moved the archive without moving the AGPM Service at the same time:</span></span>

    1.  <span data-ttu-id="ba40c-127">Sie müssen den Archivierungspfad so ändern, dass er auf den neuen Speicherort für das Archiv in Bezug auf den AGPM-Server verweist.</span><span class="sxs-lookup"><span data-stu-id="ba40c-127">You must change the archive path to point to the new location for the archive in relation to the AGPM Server.</span></span> <span data-ttu-id="ba40c-128">Weitere Informationen finden Sie unter [Ändern des AGPM-Diensts](modify-the-agpm-service-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="ba40c-128">For more information, see [Modify the AGPM Service](modify-the-agpm-service-agpm40.md).</span></span>

    2.  <span data-ttu-id="ba40c-129">Sie müssen das Kennwort erneut eingeben und auf der Registerkarte **Domänendelegierung** bestätigen. Weitere Informationen finden Sie unter [Konfigurieren von e-Mail-Benachrichtigungen](configure-e-mail-notification-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="ba40c-129">You must re-enter and confirm the password on the **Domain Delegation** tab. For more information, see [Configure E-Mail Notification](configure-e-mail-notification-agpm40.md).</span></span>

     

### <span data-ttu-id="ba40c-130">Weitere Verweise</span><span class="sxs-lookup"><span data-stu-id="ba40c-130">Additional references</span></span>

-   [<span data-ttu-id="ba40c-131">Sichern des Archivs</span><span class="sxs-lookup"><span data-stu-id="ba40c-131">Back Up the Archive</span></span>](back-up-the-archive-agpm40.md)

-   [<span data-ttu-id="ba40c-132">Wiederherstellen des Archivs aus einer Sicherung</span><span class="sxs-lookup"><span data-stu-id="ba40c-132">Restore the Archive from a Backup</span></span>](restore-the-archive-from-a-backup-agpm40.md)

-   [<span data-ttu-id="ba40c-133">Konfigurieren von AGPM-Server-Verbindungen</span><span class="sxs-lookup"><span data-stu-id="ba40c-133">Configure AGPM Server Connections</span></span>](configure-agpm-server-connections-agpm40.md)

-   [<span data-ttu-id="ba40c-134">Ändern des AGPM-Diensts</span><span class="sxs-lookup"><span data-stu-id="ba40c-134">Modify the AGPM Service</span></span>](modify-the-agpm-service-agpm40.md)

-   <span data-ttu-id="ba40c-135">[Schritt-für-Schritt-Anleitung für Microsoft Advanced Group Policy Management 4,0](https://go.microsoft.com/fwlink/?LinkId=153505) (https://go.microsoft.com/fwlink/?LinkId=153505)</span><span class="sxs-lookup"><span data-stu-id="ba40c-135">[Step-by-Step Guide for Microsoft Advanced Group Policy Management 4.0](https://go.microsoft.com/fwlink/?LinkId=153505) (https://go.microsoft.com/fwlink/?LinkId=153505)</span></span>

-   <span data-ttu-id="ba40c-136">[Planungshandbuch für Microsoft Advanced Group Policy Management](https://go.microsoft.com/fwlink/?LinkId=156883) (https://go.microsoft.com/fwlink/?LinkId=156883)</span><span class="sxs-lookup"><span data-stu-id="ba40c-136">[Planning Guide for Microsoft Advanced Group Policy Management](https://go.microsoft.com/fwlink/?LinkId=156883) (https://go.microsoft.com/fwlink/?LinkId=156883)</span></span>

-   [<span data-ttu-id="ba40c-137">Durchführen von AGPM-Administratoraufgaben</span><span class="sxs-lookup"><span data-stu-id="ba40c-137">Performing AGPM Administrator Tasks</span></span>](performing-agpm-administrator-tasks-agpm40.md)

 

 





