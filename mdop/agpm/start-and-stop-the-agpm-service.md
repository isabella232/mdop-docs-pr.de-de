---
title: Starten und Beenden des AGPM-Diensts
description: Starten und Beenden des AGPM-Diensts
author: dansimp
ms.assetid: 769aa0ce-224a-446f-9958-9518af4ad159
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 33e797182d49157da0fe8f36dce17b4b35cdd623
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807460"
---
# <span data-ttu-id="7431b-103">Starten und Beenden des AGPM-Diensts</span><span class="sxs-lookup"><span data-stu-id="7431b-103">Start and Stop the AGPM Service</span></span>


<span data-ttu-id="7431b-104">Der AGPM-Dienst ist ein Windows-Dienst, der als Sicherheitsproxy fungiert und den Clientzugriff auf Gruppenrichtlinienobjekte (Group Policy Objects, GPOs) in der Archivierungs-und Produktionsumgebung verwaltet.</span><span class="sxs-lookup"><span data-stu-id="7431b-104">The AGPM Service is a Windows service that acts as a security proxy, managing client access to Group Policy objects (GPOs) in the archive and production environment.</span></span>

<span data-ttu-id="7431b-105">**Wichtig**  Durch das Beenden oder Deaktivieren des AGPM-Diensts können AGPM-Clients keine Vorgänge (wie das Auflisten oder Bearbeiten von GPOs) über den Server ausführen.</span><span class="sxs-lookup"><span data-stu-id="7431b-105">**Important** Stopping or disabling the AGPM Service will prevent AGPM clients from performing any operations (such as listing or editing GPOs) through the server.</span></span>

 

<span data-ttu-id="7431b-106">Ein Benutzerkonto mit Zugriff auf den AGPM-Server (der Computer, auf dem der AGPM-Dienst installiert ist) ist erforderlich, um dieses Verfahren ausführen zu können.</span><span class="sxs-lookup"><span data-stu-id="7431b-106">A user account with access to the AGPM Server (the computer on which the AGPM Service is installed) is required to complete this procedure.</span></span>

**<span data-ttu-id="7431b-107">So starten oder beenden Sie den AGPM-Dienst</span><span class="sxs-lookup"><span data-stu-id="7431b-107">To start or stop the AGPM Service</span></span>**

1.  <span data-ttu-id="7431b-108">Klicken Sie auf dem Computer, auf dem Microsoft Advanced Group Policy Management-Server (und daher der AGPM-Dienst) installiert ist, auf **Start**, klicken Sie auf **System**Steuerung, klicken Sie auf **Verwaltung**, und klicken Sie dann auf **Dienste**.</span><span class="sxs-lookup"><span data-stu-id="7431b-108">On the computer on which Microsoft Advanced Group Policy Management - Server (and therefore the AGPM Service) is installed, click **Start**, click **Control Panel**, click **Administrative Tools**, and then click **Services**.</span></span>

2.  <span data-ttu-id="7431b-109">Klicken Sie in der Liste der Dienste mit der rechten Maustaste auf **AGPM-Dienst** , und wählen Sie **starten**, **neu starten**oder **Beenden**aus.</span><span class="sxs-lookup"><span data-stu-id="7431b-109">In the list of services, right-click **AGPM Service** and select **Start**, **Restart**, or **Stop**.</span></span>

    <span data-ttu-id="7431b-110">**Vorsicht**  Ändern Sie die Einstellungen für den AGPM-Dienst nicht über **Administrative Tools** und **Dienste** im Betriebssystem.</span><span class="sxs-lookup"><span data-stu-id="7431b-110">**Caution** Do not modify settings for the AGPM Service through **Administrative Tools** and **Services** in the operating system.</span></span> <span data-ttu-id="7431b-111">Dadurch kann der Start des AGPM-Diensts verhindert werden.</span><span class="sxs-lookup"><span data-stu-id="7431b-111">Doing so can prevent the AGPM Service from starting.</span></span> <span data-ttu-id="7431b-112">Informationen zum Ändern der Einstellungen für den Dienst finden Sie unter [Verwalten des AGPM-Diensts](managing-the-agpm-service.md).</span><span class="sxs-lookup"><span data-stu-id="7431b-112">To modify settings for the service, see [Managing the AGPM Service](managing-the-agpm-service.md).</span></span>

     

### <span data-ttu-id="7431b-113">Weitere Verweise</span><span class="sxs-lookup"><span data-stu-id="7431b-113">Additional references</span></span>

-   [<span data-ttu-id="7431b-114">Verwalten des AGPM-Dienstes</span><span class="sxs-lookup"><span data-stu-id="7431b-114">Managing the AGPM Service</span></span>](managing-the-agpm-service.md)

 

 





