---
title: Starten und Beenden des AGPM-Diensts
description: Starten und Beenden des AGPM-Diensts
author: dansimp
ms.assetid: b9d26920-c439-4992-9a78-73e4fba8309d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2be1c2386bedd5888c0ed032479bf1237ce8289c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808219"
---
# <span data-ttu-id="71ff7-103">Starten und Beenden des AGPM-Diensts</span><span class="sxs-lookup"><span data-stu-id="71ff7-103">Start and Stop the AGPM Service</span></span>


<span data-ttu-id="71ff7-104">Der AGPM-Dienst ist ein Windows-Dienst, der als Sicherheitsproxy fungiert und den Clientzugriff auf Gruppenrichtlinienobjekte (Group Policy Objects, GPOs) in der Archivierungs-und Produktionsumgebung verwaltet.</span><span class="sxs-lookup"><span data-stu-id="71ff7-104">The AGPM Service is a Windows service that acts as a security proxy, managing client access to Group Policy Objects (GPOs) in the archive and production environment.</span></span>

<span data-ttu-id="71ff7-105">**Wichtig**  Durch das Beenden oder Deaktivieren des AGPM-Diensts können AGPM-Clients keine Vorgänge (wie das Auflisten oder Bearbeiten von GPOs) über den Server ausführen.</span><span class="sxs-lookup"><span data-stu-id="71ff7-105">**Important** Stopping or disabling the AGPM Service will prevent AGPM Clients from performing any operations (such as listing or editing GPOs) through the server.</span></span>

 

<span data-ttu-id="71ff7-106">Ein Benutzerkonto mit Zugriff auf den AGPM-Server (der Computer, auf dem der AGPM-Dienst installiert ist) ist erforderlich, um dieses Verfahren ausführen zu können.</span><span class="sxs-lookup"><span data-stu-id="71ff7-106">A user account with access to the AGPM Server (the computer on which the AGPM Service is installed) is required to complete this procedure.</span></span>

**<span data-ttu-id="71ff7-107">So starten oder beenden Sie den AGPM-Dienst</span><span class="sxs-lookup"><span data-stu-id="71ff7-107">To start or stop the AGPM Service</span></span>**

1.  <span data-ttu-id="71ff7-108">Klicken Sie auf dem Computer, auf dem Microsoft Advanced Group Policy Management-Server (und daher der AGPM-Dienst) installiert ist, auf **Start**, klicken Sie auf **System**Steuerung, klicken Sie auf **Verwaltung**, und klicken Sie dann auf **Dienste**.</span><span class="sxs-lookup"><span data-stu-id="71ff7-108">On the computer on which Microsoft Advanced Group Policy Management - Server (and therefore the AGPM Service) is installed, click **Start**, click **Control Panel**, click **Administrative Tools**, and then click **Services**.</span></span>

2.  <span data-ttu-id="71ff7-109">Klicken Sie in der Liste der Dienste mit der rechten Maustaste auf **AGPM-Dienst** , und wählen Sie **starten**, **neu starten**oder **Beenden**aus.</span><span class="sxs-lookup"><span data-stu-id="71ff7-109">In the list of services, right-click **AGPM Service** and select **Start**, **Restart**, or **Stop**.</span></span>

    <span data-ttu-id="71ff7-110">**Vorsicht**  Ändern Sie die Einstellungen für den AGPM-Dienst nicht über **Administrative Tools** und **Dienste** im Betriebssystem.</span><span class="sxs-lookup"><span data-stu-id="71ff7-110">**Caution** Do not modify settings for the AGPM Service through **Administrative Tools** and **Services** in the operating system.</span></span> <span data-ttu-id="71ff7-111">Dadurch kann der Start des AGPM-Diensts verhindert werden.</span><span class="sxs-lookup"><span data-stu-id="71ff7-111">Doing so can prevent the AGPM Service from starting.</span></span>

     

### <span data-ttu-id="71ff7-112">Weitere Verweise</span><span class="sxs-lookup"><span data-stu-id="71ff7-112">Additional references</span></span>

-   [<span data-ttu-id="71ff7-113">Verwalten des AGPM-Dienstes</span><span class="sxs-lookup"><span data-stu-id="71ff7-113">Managing the AGPM Service</span></span>](managing-the-agpm-service-agpm30ops.md)

 

 





