---
title: So veröffentlichen Sie mithilfe der Verwaltungskonsole ein Paket
description: So veröffentlichen Sie mithilfe der Verwaltungskonsole ein Paket
author: dansimp
ms.assetid: 7c6930fc-5c89-4519-a901-512dae155fd2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 832dd95edbb0f4cd6b6ae242a81859141ebcb279
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805237"
---
# <span data-ttu-id="b20cb-103">So veröffentlichen Sie mithilfe der Verwaltungskonsole ein Paket</span><span class="sxs-lookup"><span data-stu-id="b20cb-103">How to Publish a Package by Using the Management Console</span></span>


<span data-ttu-id="b20cb-104">Gehen Sie wie folgt vor, um ein App-V 5,0-Paket zu veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="b20cb-104">Use the following procedure to publish an App-V 5.0 package.</span></span> <span data-ttu-id="b20cb-105">Nachdem Sie ein Paket veröffentlicht haben, können Computer, auf denen der App-V 5,0-Client ausgeführt wird, auf die Anwendungen in diesem Paket zugreifen und diese ausführen.</span><span class="sxs-lookup"><span data-stu-id="b20cb-105">Once you publish a package, computers that are running the App-V 5.0 client can access and run the applications in that package.</span></span>

<span data-ttu-id="b20cb-106">**Hinweis**  Die Möglichkeit, nur Administratoren zum Veröffentlichen oder Aufheben der Veröffentlichung von Paketen (siehe unten) zu aktivieren, wird ab App-V 5,0 SP3 unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b20cb-106">**Note** The ability to enable only administrators to publish or unpublish packages (described below) is supported starting in App-V 5.0 SP3.</span></span>

 

**<span data-ttu-id="b20cb-107">So veröffentlichen Sie ein App-V 5,0-Paket</span><span class="sxs-lookup"><span data-stu-id="b20cb-107">To publish an App-V 5.0 package</span></span>**

1.  <span data-ttu-id="b20cb-108">In der App-V 5,0-Verwaltungskonsole.</span><span class="sxs-lookup"><span data-stu-id="b20cb-108">In the App-V 5.0 Management console.</span></span> <span data-ttu-id="b20cb-109">Klicken Sie mit der rechten Maustaste auf den Namen des zu veröffentlichenden Pakets, und wählen Sie **veröffentlichen**aus.</span><span class="sxs-lookup"><span data-stu-id="b20cb-109">right-click the name of the package to be published, and select **Publish**.</span></span>

2.  <span data-ttu-id="b20cb-110">Überprüfen Sie die Spalte **Status** , um zu überprüfen, ob das Paket veröffentlicht wurde und nun verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="b20cb-110">Review the **Status** column to verify that the package has been published and is now available.</span></span> <span data-ttu-id="b20cb-111">Wenn das Paket verfügbar ist, wird der **veröffentlichte** Status angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b20cb-111">If the package is available, the status **published** is displayed.</span></span>

    <span data-ttu-id="b20cb-112">Wenn das Paket nicht erfolgreich veröffentlicht wird, wird der Status **unveröffentlicht** zusammen mit dem Fehlertext angezeigt, in dem erläutert wird, warum das Paket nicht verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="b20cb-112">If the package is not published successfully, the status **unpublished** is displayed, along with error text that explains why the package is not available.</span></span>

**<span data-ttu-id="b20cb-113">So aktivieren Sie nur Administratoren zum Veröffentlichen oder Aufheben der Veröffentlichung von Paketen</span><span class="sxs-lookup"><span data-stu-id="b20cb-113">To enable only administrators to publish or unpublish packages</span></span>**

1.  <span data-ttu-id="b20cb-114">Navigieren Sie zum folgenden Gruppenrichtlinien-Objektknoten:</span><span class="sxs-lookup"><span data-stu-id="b20cb-114">Navigate to the following Group Policy Object node:</span></span>

    <span data-ttu-id="b20cb-115">**Computer Konfiguration &gt; Richtlinien &gt; Administrative Vorlagen &gt; System &gt; App-V &gt; Publishing**.</span><span class="sxs-lookup"><span data-stu-id="b20cb-115">**Computer Configuration &gt; Policies &gt; Administrative Templates &gt; System &gt; App-V &gt; Publishing**.</span></span>

2.  <span data-ttu-id="b20cb-116">Aktivieren Sie die Gruppenrichtlinieneinstellung **Veröffentlichung als Administrator anfordern** .</span><span class="sxs-lookup"><span data-stu-id="b20cb-116">Enable the **Require publish as administrator** Group Policy setting.</span></span>

    <span data-ttu-id="b20cb-117">Informationen zum Verwenden von PowerShell zum Einrichten dieses Elements finden Sie unter [Verwalten von App-V 5,0-Paketen, die mit PowerShell auf einem eigenständigen Computer ausgeführt](how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md#bkmk-admins-pub-pkgs)werden.</span><span class="sxs-lookup"><span data-stu-id="b20cb-117">To alternatively use PowerShell to set this item, see [How to Manage App-V 5.0 Packages Running on a Stand-Alone Computer by Using PowerShell](how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md#bkmk-admins-pub-pkgs).</span></span>

    <span data-ttu-id="b20cb-118">Sie **haben einen Vorschlag für App-V**?</span><span class="sxs-lookup"><span data-stu-id="b20cb-118">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="b20cb-119">[Hier](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)können Sie Vorschläge hinzufügen oder abstimmen.</span><span class="sxs-lookup"><span data-stu-id="b20cb-119">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="b20cb-120">Sie haben ein App-V-Problem?</span><span class="sxs-lookup"><span data-stu-id="b20cb-120">Got an App-V issue?</span></span>** <span data-ttu-id="b20cb-121">Verwenden Sie das [App-V TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="b20cb-121">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="b20cb-122">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="b20cb-122">Related topics</span></span>


[<span data-ttu-id="b20cb-123">Vorgänge für App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="b20cb-123">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

[<span data-ttu-id="b20cb-124">So konfigurieren Sie mithilfe der Verwaltungskonsole den Zugriff auf Pakete</span><span class="sxs-lookup"><span data-stu-id="b20cb-124">How to Configure Access to Packages by Using the Management Console</span></span>](how-to-configure-access-to-packages-by-using-the-management-console-50.md)

 

 





