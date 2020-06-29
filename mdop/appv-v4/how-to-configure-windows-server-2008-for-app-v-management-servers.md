---
title: Konfigurieren von Windows Server 2008 für App-V Management Server
description: Konfigurieren von Windows Server 2008 für App-V Management Server
author: dansimp
ms.assetid: 38b4016f-de82-4209-9159-387d20ddee25
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2d1cd7e84ffc0036c98e70a9a0ee1fd3a4ade790
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807220"
---
# <span data-ttu-id="795ec-103">Konfigurieren von Windows Server 2008 für App-V Management Server</span><span class="sxs-lookup"><span data-stu-id="795ec-103">How to Configure Windows Server 2008 for App-V Management Servers</span></span>


<span data-ttu-id="795ec-104">Auf dem Windows Server 2008-Server, auf dem Sie den Microsoft Application Virtualization (App-V)-Verwaltungs-Webdienst installieren, müssen Internet Informationsdienste (IIS) als Rolle auf dem Server installiert sein.</span><span class="sxs-lookup"><span data-stu-id="795ec-104">The Windows Server 2008 server on which you install the Microsoft Application Virtualization (App-V) Management Web Service requires Internet Information Services (IIS) to be installed as a role on the server.</span></span> <span data-ttu-id="795ec-105">Gehen Sie wie folgt vor, um Windows Server 2008 so zu konfigurieren, dass die APP-vserver-Installation unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="795ec-105">Use the following procedure to configure Windows Server 2008 to support App-Vserver installation.</span></span>

**<span data-ttu-id="795ec-106">So installieren Sie IIS auf einem Windows Server2008-Computer</span><span class="sxs-lookup"><span data-stu-id="795ec-106">To install IIS on a Windows Server2008 computer</span></span>**

1.  <span data-ttu-id="795ec-107">Klicken Sie auf dem Windows Server2008-Computer auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Verwaltung**, und klicken Sie dann auf **Server-Manager** , um den Server-Manager zu starten.</span><span class="sxs-lookup"><span data-stu-id="795ec-107">On the Windows Server2008 computer, click **Start**, click **All Programs**, click **Administrative Tools**, and then click **Server Manager** to start Server Manager.</span></span> <span data-ttu-id="795ec-108">Klicken Sie im Server-Manager mit der rechten Maustaste auf den Knoten **Rollen** , und klicken Sie auf **Rollen hinzufügen** , um den **Assistenten zum Hinzufügen von Rollen**zu starten.</span><span class="sxs-lookup"><span data-stu-id="795ec-108">In Server Manager, right-click the **Roles** node, and click **Add Roles** to start the **Add Roles Wizard**.</span></span>

2.  <span data-ttu-id="795ec-109">Wählen Sie im **Assistenten zum Hinzufügen von Rollen**auf der Seite **Server Rollen auswählen** die Option **Webserver (IIS)** aus.</span><span class="sxs-lookup"><span data-stu-id="795ec-109">In the **Add Roles Wizard**, on the **Select Server Roles** page, select **Web Server (IIS)**.</span></span> <span data-ttu-id="795ec-110">Wenn Sie dazu aufgefordert werden, klicken Sie auf **erforderliche Features hinzufügen** , um die abhängigen Features hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="795ec-110">When prompted, click **Add Required Features** to add the dependent features.</span></span>

3.  <span data-ttu-id="795ec-111">Klicken Sie auf der Seite **Server Rollen auswählen** auf **weiter**, und klicken Sie dann erneut auf **weiter** .</span><span class="sxs-lookup"><span data-stu-id="795ec-111">On the **Select Server Roles** page, Click **Next**, and then click **Next** again.</span></span>

4.  <span data-ttu-id="795ec-112">Klicken Sie im **Assistenten zum Hinzufügen von Rollen**auf der Seite **Rollendienste auswählen** auf:</span><span class="sxs-lookup"><span data-stu-id="795ec-112">In the **Add Roles Wizard**, on the **Select Role Services** page:</span></span>

    1.  <span data-ttu-id="795ec-113">Wählen Sie unter **Anwendungsentwicklung**die Option **ASP.net** aus, und klicken Sie bei der entsprechenden Aufforderung auf **Erforderliche Rollendienste hinzufügen** , um die Dienste und Features der abhängigen Rollen hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="795ec-113">Under **Application Development**, select **ASP.NET** and, when prompted, click **Add Required Role Services** to add the dependent roles services and features.</span></span>

    2.  <span data-ttu-id="795ec-114">Wählen Sie unter **Sicherheit**die Option **Windows-Authentifizierung**aus.</span><span class="sxs-lookup"><span data-stu-id="795ec-114">Under **Security**, select **Windows Authentication**.</span></span>

    3.  <span data-ttu-id="795ec-115">Wählen Sie im Knoten **Verwaltungstools** die Option **IIS-Verwaltungsskripts und-Tools**aus.</span><span class="sxs-lookup"><span data-stu-id="795ec-115">In the **Management Tools** node, select **IIS Management Scripts and Tools**.</span></span> <span data-ttu-id="795ec-116">Stellen Sie unter **IIS6-Verwaltungskompatibilität**sicher, dass sowohl die **IIS6-Metabase-Kompatibilität** als auch die IIS6-WMI- **Kompatibilität** ausgewählt sind, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="795ec-116">Under **IIS6 Management Compatibility**, ensure that both **IIS6 Metabase Compatibility** and **IIS6 WMI Compatibility** are selected, and then click **Next**.</span></span>

5.  <span data-ttu-id="795ec-117">Klicken Sie auf der Seite **Installationsauswahl bestätigen** auf **Installieren**, und führen Sie dann den restlichen Assistenten aus.</span><span class="sxs-lookup"><span data-stu-id="795ec-117">On the **Confirm Installation Selections** page, click **Install**, and then complete the rest of the wizard.</span></span>

6.  <span data-ttu-id="795ec-118">Klicken Sie auf **Schließen** , um den **Assistenten zum Hinzufügen von Rollen**zu beenden, und schließen Sie dann Server-Manager.</span><span class="sxs-lookup"><span data-stu-id="795ec-118">Click **Close** to exit the **Add Roles Wizard**, and then close Server Manager.</span></span>

## <span data-ttu-id="795ec-119">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="795ec-119">Related topics</span></span>


[<span data-ttu-id="795ec-120">Bereitstellungsanforderungen für Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="795ec-120">Application Virtualization Deployment Requirements</span></span>](application-virtualization-deployment-requirements.md)

[<span data-ttu-id="795ec-121">Bereitstellung und Upgrade von Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="795ec-121">Application Virtualization Deployment and Upgrade Checklists</span></span>](application-virtualization-deployment-and-upgrade-checklists.md)

 

 





