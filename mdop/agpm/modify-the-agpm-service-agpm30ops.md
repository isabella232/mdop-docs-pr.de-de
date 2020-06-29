---
title: Ändern des AGPM-Diensts
description: Ändern des AGPM-Diensts
author: dansimp
ms.assetid: 3485f85f-59d1-48dc-8748-36826214dcb1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3f6111a2713fcbe59ffb4336fc84bfa4697ffdeb
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808332"
---
# <span data-ttu-id="6f86c-103">Ändern des AGPM-Diensts</span><span class="sxs-lookup"><span data-stu-id="6f86c-103">Modify the AGPM Service</span></span>


<span data-ttu-id="6f86c-104">Der AGPM-Dienst ist ein Windows-Dienst, der als Sicherheitsproxy fungiert und den Clientzugriff auf Gruppenrichtlinienobjekte (Group Policy Objects, GPOs) in der Archivierungs-und Produktionsumgebung verwaltet.</span><span class="sxs-lookup"><span data-stu-id="6f86c-104">The AGPM Service is a Windows service that acts as a security proxy, managing client access to Group Policy Objects (GPOs) in the archive and production environment.</span></span> <span data-ttu-id="6f86c-105">Wenn dieser Dienst beendet oder deaktiviert ist, können AGPM-Clients keine Vorgänge über den Server ausführen.</span><span class="sxs-lookup"><span data-stu-id="6f86c-105">If this service is stopped or disabled, AGPM Clients cannot perform operations through the server.</span></span> <span data-ttu-id="6f86c-106">Sie können den Archivierungspfad, das AGPM-Dienstkonto und den Port ändern, auf den der AGPM-Dienst lauscht.</span><span class="sxs-lookup"><span data-stu-id="6f86c-106">You can modify the archive path, the AGPM Service Account, and the port on which the AGPM Service listens.</span></span>

<span data-ttu-id="6f86c-107">**Vorsicht**  Ändern Sie die Einstellungen für den AGPM-Dienst nicht über **Administrative Tools** und **Dienste** im Betriebssystem.</span><span class="sxs-lookup"><span data-stu-id="6f86c-107">**Caution** Do not modify settings for the AGPM Service through **Administrative Tools** and **Services** in the operating system.</span></span> <span data-ttu-id="6f86c-108">Dadurch kann der Start des AGPM-Diensts verhindert werden.</span><span class="sxs-lookup"><span data-stu-id="6f86c-108">Doing so can prevent the AGPM Service from starting.</span></span>

 

<span data-ttu-id="6f86c-109">Ein Benutzerkonto, das ein Mitglied der Gruppe der Domänenadministratoren ist und Zugriff auf den AGPM-Server hat (der Computer, auf dem Microsoft Advanced Group Policy Management-Server installiert ist), ist erforderlich, um dieses Verfahren ausführen zu können.</span><span class="sxs-lookup"><span data-stu-id="6f86c-109">A user account that is a member of the Domain Admins group and has access to the AGPM Server (the computer on which Microsoft Advanced Group Policy Management - Server is installed) is required to complete this procedure.</span></span> <span data-ttu-id="6f86c-110">Darüber hinaus müssen Sie die Anmeldeinformationen für das AGPM-Dienstkonto angeben, um dieses Verfahren ausführen zu können.</span><span class="sxs-lookup"><span data-stu-id="6f86c-110">Additionally, you must provide credentials for the AGPM Service Account to complete this procedure.</span></span>

**<span data-ttu-id="6f86c-111">So ändern Sie den AGPM-Dienst</span><span class="sxs-lookup"><span data-stu-id="6f86c-111">To modify the AGPM Service</span></span>**

1.  <span data-ttu-id="6f86c-112">Auf dem Computer, auf dem Microsoft Advanced Group Policy Management-Server installiert ist:</span><span class="sxs-lookup"><span data-stu-id="6f86c-112">On the computer on which Microsoft Advanced Group Policy Management - Server is installed:</span></span>

    -   <span data-ttu-id="6f86c-113">Klicken Sie in WindowsServer2008 auf **Start**, **Systemsteuerung**und **Programme und Funktionen**.</span><span class="sxs-lookup"><span data-stu-id="6f86c-113">For WindowsServer2008, click **Start**, **Control Panel**, and **Programs and Features**.</span></span>

    -   <span data-ttu-id="6f86c-114">Klicken Sie in Windows Vista auf **Start**, **Systemsteuerung**, **Programme**und **Programme und Funktionen**.</span><span class="sxs-lookup"><span data-stu-id="6f86c-114">For WindowsVista, click **Start**, **Control Panel**, **Programs**, and **Programs and Features**.</span></span>

2.  <span data-ttu-id="6f86c-115">Klicken Sie mit der rechten Maustaste auf **Microsoft Advanced Group Policy Management-Server**, und klicken Sie dann auf **ändern**.</span><span class="sxs-lookup"><span data-stu-id="6f86c-115">Right-click **Microsoft Advanced Group Policy Management - Server**, and then click **Change**.</span></span>

3.  <span data-ttu-id="6f86c-116">Klicken Sie auf **weiter**, und klicken Sie dann auf **ändern**.</span><span class="sxs-lookup"><span data-stu-id="6f86c-116">Click **Next**, and then click **Modify**.</span></span>

4.  <span data-ttu-id="6f86c-117">Befolgen Sie die Anweisungen zum Konfigurieren des AGPM-Diensts:</span><span class="sxs-lookup"><span data-stu-id="6f86c-117">Follow the instructions to configure the AGPM Service:</span></span>

    1.  <span data-ttu-id="6f86c-118">Geben Sie im Dialogfeld **Archivpfad** einen neuen Speicherort für das Archiv relativ zum AGPM-Server ein, oder bestätigen Sie den aktuellen Archivierungspfad, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="6f86c-118">In the **Archive Path** dialog box, enter a new location for the archive relative to the AGPM Server, or confirm the current archive path, and then click **Next**.</span></span>

        <span data-ttu-id="6f86c-119">**Wichtig**  Der Archivierungspfad kann auf einen Ordner auf dem AGPM-Server oder an anderer Stelle verweisen, aber der Speicherort sollte über genügend Speicherplatz zum Speichern aller GPOs und Verlaufsdaten verfügen, die von diesem AGPM-Server verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="6f86c-119">**Important** The archive path can point to a folder on the AGPM Server or elsewhere, but the location should have sufficient space to store all GPOs and history data managed by this AGPM Server.</span></span>

         

    2.  <span data-ttu-id="6f86c-120">Geben Sie im Dialogfeld **AGPM-Dienstkonto** die Anmeldeinformationen für ein Dienstkonto ein, unter dem der AGPM-Dienst ausgeführt werden soll, und klicken Sie auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="6f86c-120">In the **AGPM Service Account** dialog box, enter credentials for a service account under which the AGPM Service will run, and click **Next**.</span></span>

        <span data-ttu-id="6f86c-121">**Wichtig**  Durch Ändern der Installation werden die Anmeldeinformationen für das AGPM-Dienstkonto gelöscht.</span><span class="sxs-lookup"><span data-stu-id="6f86c-121">**Important** Modifying the installation clears the credentials for the AGPM Service Account.</span></span> <span data-ttu-id="6f86c-122">Sie müssen die Anmeldeinformationen erneut eingeben, sind aber nicht für die Übereinstimmung mit den Anmeldeinformationen erforderlich, die während der ursprünglichen Installation verwendet wurden.</span><span class="sxs-lookup"><span data-stu-id="6f86c-122">You must re-enter credentials, but they are not required to match the credentials used during the original installation.</span></span>

        <span data-ttu-id="6f86c-123">Das AGPM-Dienstkonto muss Vollzugriff auf die GPOs haben, die es verwalten soll, und es wird die Berechtigung **Anmelden als Dienst** gewährt.</span><span class="sxs-lookup"><span data-stu-id="6f86c-123">The AGPM Service Account must have full access to the GPOs that it will manage and will be granted **Log On As A Service** permission.</span></span> <span data-ttu-id="6f86c-124">Wenn Sie GPOs in einer einzelnen Domäne verwalten, können Sie das Konto Lokales System für den primären Domänencontroller als AGPM-Dienstkonto festlegen.</span><span class="sxs-lookup"><span data-stu-id="6f86c-124">If you will be managing GPOs on a single domain, you can make the Local System account for the primary domain controller the AGPM Service Account.</span></span>

        <span data-ttu-id="6f86c-125">Wenn Sie GPOs in mehreren Domänen verwalten oder wenn es sich bei einem Mitgliedsserver um den AGPM-Server handelt, sollten Sie ein anderes Konto als AGPM-Dienstkonto konfigurieren, da das lokale System Konto für einen Domänencontroller nicht auf GPOs in anderen Domänen zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="6f86c-125">If you will be managing GPOs on multiple domains or if a member server will be the AGPM Server, you should configure a different account as the AGPM Service Account because the Local System account for one domain controller cannot access GPOs on other domains.</span></span>

         

    3.  <span data-ttu-id="6f86c-126">Geben Sie im Dialogfeld **Besitzer des Archivs** den Benutzernamen eines AGPM-Administrators (Vollzugriff) oder einer Gruppe von AGPM-Administratoren ein, und klicken Sie auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="6f86c-126">In the **Archive Owner** dialog box, enter the user name of an AGPM Administrator (Full Control) or group of AGPM Administrators, and click **Next**.</span></span>

        <span data-ttu-id="6f86c-127">**Hinweis**  Durch Ändern der Installation werden die Anmeldeinformationen für den Besitzer des Archivs gelöscht.</span><span class="sxs-lookup"><span data-stu-id="6f86c-127">**Note** Modifying the installation clears the credentials for the Archive Owner.</span></span> <span data-ttu-id="6f86c-128">Sie müssen die Anmeldeinformationen erneut eingeben, sind aber nicht für die Übereinstimmung mit den Anmeldeinformationen erforderlich, die während der ursprünglichen Installation verwendet wurden.</span><span class="sxs-lookup"><span data-stu-id="6f86c-128">You must re-enter credentials, but they are not required to match the credentials used during the original installation.</span></span>

         

    4.  <span data-ttu-id="6f86c-129">Geben Sie im Dialogfeld **Port Konfiguration** einen neuen Port ein, an dem der AGPM-Dienst den aktuell ausgewählten Port überwachen oder bestätigen soll, und klicken Sie auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="6f86c-129">In the **Port Configuration** dialog box, type a new port on which the AGPM Service should listen or confirm the port currently selected, and click **Next**.</span></span>

        <span data-ttu-id="6f86c-130">**Hinweis**  Standardmäßig überwacht der AGPM-Dienst Port 4600.</span><span class="sxs-lookup"><span data-stu-id="6f86c-130">**Note** By default, the AGPM Service listens on port 4600.</span></span>

        <span data-ttu-id="6f86c-131">Wenn Sie Portausnahmen manuell konfigurieren oder Regeln zum Konfigurieren von Portausnahmen haben, können Sie das Kontrollkästchen **Portausnahme zu Firewall hinzufügen** deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="6f86c-131">If you manually configure port exceptions or have rules configuring port exceptions, you can clear the **Add port exception to firewall** check box.</span></span>

         

5.  <span data-ttu-id="6f86c-132">Klicken Sie auf **ändern**, und klicken Sie nach Abschluss der Installation auf **Fertig stellen**.</span><span class="sxs-lookup"><span data-stu-id="6f86c-132">Click **Change**, and when the installation is complete click **Finish**.</span></span>

6.  <span data-ttu-id="6f86c-133">Wenn Sie den Port geändert haben, auf dem der AGPM-Dienst lauscht, ändern Sie den Port in der AGPM-Server Verbindung für jeden Gruppenrichtlinienadministrator.</span><span class="sxs-lookup"><span data-stu-id="6f86c-133">If you have changed the port on which the AGPM Service listens, modify the port in the AGPM Server connection for each Group Policy administrator.</span></span> <span data-ttu-id="6f86c-134">(Weitere Informationen finden Sie unter [Konfigurieren von AGPM-Server Verbindungen](configure-agpm-server-connections-agpm30ops.md).)</span><span class="sxs-lookup"><span data-stu-id="6f86c-134">(For more information, see [Configure AGPM Server Connections](configure-agpm-server-connections-agpm30ops.md).)</span></span>

7.  <span data-ttu-id="6f86c-135">Wiederholen Sie diesen Vorgang für jeden AGPM-Server, auf den die Konfigurationsänderungen angewendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="6f86c-135">Repeat for each AGPM Server to which the configuration changes should be applied.</span></span>

### <span data-ttu-id="6f86c-136">Weitere Verweise</span><span class="sxs-lookup"><span data-stu-id="6f86c-136">Additional references</span></span>

-   [<span data-ttu-id="6f86c-137">Verwalten des AGPM-Dienstes</span><span class="sxs-lookup"><span data-stu-id="6f86c-137">Managing the AGPM Service</span></span>](managing-the-agpm-service-agpm30ops.md)

 

 





