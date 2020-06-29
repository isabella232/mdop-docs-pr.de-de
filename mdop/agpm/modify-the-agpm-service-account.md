---
title: Ändern des AGPM-Dienstkontos
description: Ändern des AGPM-Dienstkontos
author: dansimp
ms.assetid: 0d8d8c7b-f299-4fee-8414-406492156942
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0672ceed2fba17060e17d2ffcfa264da458b9897
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808340"
---
# <span data-ttu-id="12bf2-103">Ändern des AGPM-Dienstkontos</span><span class="sxs-lookup"><span data-stu-id="12bf2-103">Modify the AGPM Service Account</span></span>


<span data-ttu-id="12bf2-104">Der AGPM-Dienst ist ein Windows-Dienst, der als Sicherheitsproxy fungiert und den Clientzugriff auf Gruppenrichtlinienobjekte (Group Policy Objects, GPOs) in der Archivierungs-und Produktionsumgebung verwaltet.</span><span class="sxs-lookup"><span data-stu-id="12bf2-104">The AGPM Service is a Windows service that acts as a security proxy, managing client access to Group Policy objects (GPOs) in the archive and production environment.</span></span> <span data-ttu-id="12bf2-105">Wenn dieser Dienst beendet oder deaktiviert ist, können AGPM-Clients keine Vorgänge über den Server ausführen.</span><span class="sxs-lookup"><span data-stu-id="12bf2-105">If this service is stopped or disabled, AGPM clients cannot perform operations through the server.</span></span>

<span data-ttu-id="12bf2-106">Der Archivierungspfad und das AGPM-Dienstkonto werden während der Installation von AGPM Server konfiguriert und können anschließend über die **Option Software** auf dem AGPM-Server geändert werden.</span><span class="sxs-lookup"><span data-stu-id="12bf2-106">The archive path and AGPM Service Account are configured during the installation of AGPM Server and can be changed afterward through **Add or Remove Programs** on the AGPM Server.</span></span>

<span data-ttu-id="12bf2-107">**Vorsicht**  Ändern Sie die Einstellungen für den AGPM-Dienst nicht über **Administrative Tools** und **Dienste** im Betriebssystem.</span><span class="sxs-lookup"><span data-stu-id="12bf2-107">**Caution** Do not modify settings for the AGPM Service through **Administrative Tools** and **Services** in the operating system.</span></span> <span data-ttu-id="12bf2-108">Dadurch kann der Start des AGPM-Diensts verhindert werden.</span><span class="sxs-lookup"><span data-stu-id="12bf2-108">Doing so can prevent the AGPM Service from starting.</span></span>

 

<span data-ttu-id="12bf2-109">Ein Benutzerkonto, das ein Mitglied der Gruppe der Domänenadministratoren ist und Zugriff auf den AGPM-Server hat (der Computer, auf dem Microsoft Advanced Group Policy Management-Server installiert ist), ist erforderlich, um dieses Verfahren ausführen zu können.</span><span class="sxs-lookup"><span data-stu-id="12bf2-109">A user account that is a member of the Domain Admins group and has access to the AGPM Server (the computer on which Microsoft Advanced Group Policy Management - Server is installed) is required to complete this procedure.</span></span>

<span data-ttu-id="12bf2-110">**Wichtig**  Das AGPM-Dienstkonto muss Vollzugriff auf die GPOs haben, die es verwalten soll, und es wird die Berechtigung **Anmelden als Dienst** gewährt.</span><span class="sxs-lookup"><span data-stu-id="12bf2-110">**Important** The AGPM Service Account must have full access to the GPOs that it will manage and will be granted **Log On As A Service** permission.</span></span> <span data-ttu-id="12bf2-111">Wenn Sie GPOs in einer einzelnen Domäne verwalten, können Sie das Konto Lokales System für den primären Domänencontroller als AGPM-Dienstkonto festlegen.</span><span class="sxs-lookup"><span data-stu-id="12bf2-111">If you will be managing GPOs on a single domain, you can make the Local System account for the primary domain controller the AGPM Service Account.</span></span>

<span data-ttu-id="12bf2-112">Wenn Sie GPOs in mehreren Domänen verwalten oder wenn es sich bei einem Mitgliedsserver um den AGPM-Server handelt, sollten Sie ein anderes Konto als AGPM-Dienstkonto konfigurieren, da das lokale System Konto für einen Domänencontroller nicht auf GPOs in anderen Domänen zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="12bf2-112">If you will be managing GPOs on multiple domains or if a member server will be the AGPM Server, you should configure a different account as the AGPM Service Account because the Local System account for one domain controller cannot access GPOs on other domains.</span></span>

 

**<span data-ttu-id="12bf2-113">So ändern Sie das AGPM-Dienstkonto</span><span class="sxs-lookup"><span data-stu-id="12bf2-113">To modify the AGPM Service Account</span></span>**

1.  <span data-ttu-id="12bf2-114">Klicken Sie auf dem Computer, auf dem Microsoft Advanced Group Policy Management-Server installiert ist, auf **Start**, klicken Sie auf **System**Steuerung, klicken Sie auf **Programme hinzufügen oder entfernen**.</span><span class="sxs-lookup"><span data-stu-id="12bf2-114">On the computer on which Microsoft Advanced Group Policy Management - Server is installed, click **Start**, click **Control Panel**, click **Add or Remove Programs**.</span></span>

2.  <span data-ttu-id="12bf2-115">Klicken Sie auf **Microsoft Advanced Group Policy Management-Server**, und klicken Sie dann auf **ändern**.</span><span class="sxs-lookup"><span data-stu-id="12bf2-115">Click **Microsoft Advanced Group Policy Management - Server**, and then click **Change**.</span></span>

3.  <span data-ttu-id="12bf2-116">Klicken Sie auf **weiter**, und klicken Sie dann auf **ändern**.</span><span class="sxs-lookup"><span data-stu-id="12bf2-116">Click **Next**, and then click **Modify**.</span></span>

4.  <span data-ttu-id="12bf2-117">Folgen Sie den Anweisungen auf dem Bildschirm, um die Einstellungen für den AGPM-Dienst zu konfigurieren:</span><span class="sxs-lookup"><span data-stu-id="12bf2-117">Follow the instructions on screen to configure settings for the AGPM Service:</span></span>

    1.  <span data-ttu-id="12bf2-118">Für den Archivierungspfad bestätigen oder ändern Sie den Speicherort für das Archiv relativ zum AGPM-Server.</span><span class="sxs-lookup"><span data-stu-id="12bf2-118">For the archive path, confirm or change the location for the archive relative to the AGPM Server.</span></span> <span data-ttu-id="12bf2-119">Der Archivierungspfad kann auf einen Ordner auf dem AGPM-Server oder an anderer Stelle verweisen, aber der Speicherort sollte über genügend Speicherplatz zum Speichern aller GPOs und Verlaufsdaten verfügen, die von diesem AGPM-Server verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="12bf2-119">The archive path can point to a folder on the AGPM Server or elsewhere, but the location should have sufficient space to store all GPOs and history data managed by this AGPM Server.</span></span>

    2.  <span data-ttu-id="12bf2-120">Geben Sie neue Anmeldeinformationen für das AGPM-Dienstkonto ein.</span><span class="sxs-lookup"><span data-stu-id="12bf2-120">Enter new credentials for the AGPM Service Account.</span></span>

    3.  <span data-ttu-id="12bf2-121">Geben Sie für den Archiv Besitzer die Anmeldeinformationen eines AGPM-Administrators (Vollzugriff) ein.</span><span class="sxs-lookup"><span data-stu-id="12bf2-121">For the archive owner, enter the credentials of an AGPM Administrator (Full Control).</span></span>

5.  <span data-ttu-id="12bf2-122">Klicken Sie auf **ändern**, und klicken Sie nach Abschluss der Installation auf **Fertig stellen**.</span><span class="sxs-lookup"><span data-stu-id="12bf2-122">Click **Change**, and when the installation is complete click **Finish**.</span></span>

### <span data-ttu-id="12bf2-123">Weitere Verweise</span><span class="sxs-lookup"><span data-stu-id="12bf2-123">Additional references</span></span>

-   [<span data-ttu-id="12bf2-124">Verwalten des AGPM-Dienstes</span><span class="sxs-lookup"><span data-stu-id="12bf2-124">Managing the AGPM Service</span></span>](managing-the-agpm-service.md)

 

 





