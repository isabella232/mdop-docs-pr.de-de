---
title: Ändern des Archivpfads
description: Ändern des Archivpfads
author: dansimp
ms.assetid: 6d90daf9-58db-4166-b5b3-e84bb261164a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1fc6ba2bf415d3d1bc67144d0dec1030c6173026
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808328"
---
# <span data-ttu-id="dba23-103">Ändern des Archivpfads</span><span class="sxs-lookup"><span data-stu-id="dba23-103">Modify the Archive Path</span></span>


<span data-ttu-id="dba23-104">Der Archivpfad ist der Speicherort des Archivs relativ zum AGPM-Server.</span><span class="sxs-lookup"><span data-stu-id="dba23-104">The archive path is the location of the archive relative to the AGPM Server.</span></span> <span data-ttu-id="dba23-105">Der Archivpfad kann auf einen Ordner auf dem AGPM-Server oder auf einem anderen Server in derselben Gesamtstruktur verweisen.</span><span class="sxs-lookup"><span data-stu-id="dba23-105">The archive path can point to a folder on the AGPM Server or on another server in the same forest.</span></span>

<span data-ttu-id="dba23-106">Der Archivierungspfad und das AGPM-Dienstkonto werden während der Installation von AGPM Server konfiguriert und können anschließend über die **Option Software** auf dem AGPM-Server geändert werden.</span><span class="sxs-lookup"><span data-stu-id="dba23-106">The archive path and AGPM Service Account are configured during the installation of AGPM Server and can be changed afterward through **Add or Remove Programs** on the AGPM Server.</span></span>

<span data-ttu-id="dba23-107">Ein Benutzerkonto, das ein Mitglied der Gruppe der Domänenadministratoren ist und Zugriff auf den AGPM-Server hat (der Computer, auf dem Microsoft Advanced Group Policy Management-Server installiert ist), ist erforderlich, um dieses Verfahren ausführen zu können.</span><span class="sxs-lookup"><span data-stu-id="dba23-107">A user account that is a member of the Domain Admins group and has access to the AGPM Server (the computer on which Microsoft Advanced Group Policy Management - Server is installed) is required to complete this procedure.</span></span>

**<span data-ttu-id="dba23-108">So ändern Sie den Archivpfad</span><span class="sxs-lookup"><span data-stu-id="dba23-108">To modify the archive path</span></span>**

1.  <span data-ttu-id="dba23-109">Klicken Sie auf dem Computer, auf dem Microsoft Advanced Group Policy Management-Server installiert ist, auf **Start**, klicken Sie auf **System**Steuerung, klicken Sie auf **Programme hinzufügen oder entfernen**.</span><span class="sxs-lookup"><span data-stu-id="dba23-109">On the computer on which Microsoft Advanced Group Policy Management - Server is installed, click **Start**, click **Control Panel**, click **Add or Remove Programs**.</span></span>

2.  <span data-ttu-id="dba23-110">Klicken Sie auf **Microsoft Advanced Group Policy Management-Server**, und klicken Sie dann auf **ändern**.</span><span class="sxs-lookup"><span data-stu-id="dba23-110">Click **Microsoft Advanced Group Policy Management - Server**, and then click **Change**.</span></span>

3.  <span data-ttu-id="dba23-111">Klicken Sie auf **weiter**, und klicken Sie dann auf **ändern**.</span><span class="sxs-lookup"><span data-stu-id="dba23-111">Click **Next**, and then click **Modify**.</span></span>

4.  <span data-ttu-id="dba23-112">Folgen Sie den Anweisungen auf dem Bildschirm, um die Einstellungen für den AGPM-Dienst zu konfigurieren:</span><span class="sxs-lookup"><span data-stu-id="dba23-112">Follow the instructions on screen to configure settings for the AGPM Service:</span></span>

    1.  <span data-ttu-id="dba23-113">Geben Sie für den Archivpfad einen neuen Speicherort für das Archiv relativ zum AGPM-Server ein.</span><span class="sxs-lookup"><span data-stu-id="dba23-113">For the archive path, enter a new location for the archive relative to the AGPM Server.</span></span> <span data-ttu-id="dba23-114">Der Archivierungspfad kann auf einen Ordner auf dem AGPM-Server oder an anderer Stelle verweisen, aber der Speicherort sollte über genügend Speicherplatz zum Speichern aller GPOs und Verlaufsdaten verfügen, die von diesem AGPM-Server verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="dba23-114">The archive path can point to a folder on the AGPM Server or elsewhere, but the location should have sufficient space to store all GPOs and history data managed by this AGPM Server.</span></span>

    2.  <span data-ttu-id="dba23-115">Geben Sie die Anmeldeinformationen für das AGPM-Dienstkonto ein.</span><span class="sxs-lookup"><span data-stu-id="dba23-115">Enter credentials for the AGPM Service Account.</span></span>

        <span data-ttu-id="dba23-116">**Wichtig**  Durch Ändern der Installation werden die Anmeldeinformationen für das AGPM-Dienstkonto gelöscht.</span><span class="sxs-lookup"><span data-stu-id="dba23-116">**Important** Modifying the installation clears the credentials for the AGPM Service Account.</span></span> <span data-ttu-id="dba23-117">Sie müssen die Anmeldeinformationen erneut eingeben, sind aber nicht für die Übereinstimmung mit den Anmeldeinformationen erforderlich, die während der ursprünglichen Installation verwendet wurden.</span><span class="sxs-lookup"><span data-stu-id="dba23-117">You must re-enter credentials, but they are not required to match the credentials used during the original installation.</span></span>

        <span data-ttu-id="dba23-118">Das AGPM-Dienstkonto muss Vollzugriff auf die GPOs haben, die es verwalten soll.</span><span class="sxs-lookup"><span data-stu-id="dba23-118">The AGPM Service Account must have full access to the GPOs that it will manage.</span></span> <span data-ttu-id="dba23-119">Wenn Sie GPOs in einer einzelnen Domäne verwalten, können Sie das Konto Lokales System für den primären Domänencontroller als AGPM-Dienstkonto festlegen.</span><span class="sxs-lookup"><span data-stu-id="dba23-119">If you will be managing GPOs on a single domain, you can make the Local System account for the primary domain controller the AGPM Service Account.</span></span>

        <span data-ttu-id="dba23-120">Wenn Sie GPOs in mehreren Domänen verwalten oder wenn es sich bei einem Mitgliedsserver um den AGPM-Server handelt, sollten Sie ein anderes Konto als AGPM-Dienstkonto konfigurieren, da das lokale System Konto für einen Domänencontroller nicht auf GPOs in anderen Domänen zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="dba23-120">If you will be managing GPOs on multiple domains or if a member server will be the AGPM Server, you should configure a different account as the AGPM Service Account because the Local System account for one domain controller cannot access GPOs on other domains.</span></span>

         

    3.  <span data-ttu-id="dba23-121">Geben Sie für den Archiv Besitzer die Anmeldeinformationen eines AGPM-Administrators (Vollzugriff) ein.</span><span class="sxs-lookup"><span data-stu-id="dba23-121">For the archive owner, enter the credentials of an AGPM Administrator (Full Control).</span></span>

5.  <span data-ttu-id="dba23-122">Klicken Sie auf **ändern**, und klicken Sie nach Abschluss der Installation auf **Fertig stellen**.</span><span class="sxs-lookup"><span data-stu-id="dba23-122">Click **Change**, and when the installation is complete click **Finish**.</span></span>

### <span data-ttu-id="dba23-123">Weitere Verweise</span><span class="sxs-lookup"><span data-stu-id="dba23-123">Additional references</span></span>

-   [<span data-ttu-id="dba23-124">Verwalten des AGPM-Dienstes</span><span class="sxs-lookup"><span data-stu-id="dba23-124">Managing the AGPM Service</span></span>](managing-the-agpm-service.md)

 

 





