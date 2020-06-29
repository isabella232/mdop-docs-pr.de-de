---
title: So veröffentlichen Sie mithilfe der Verwaltungskonsole ein Paket
description: So veröffentlichen Sie mithilfe der Verwaltungskonsole ein Paket
author: dansimp
ms.assetid: e34d2bcf-15ac-4a75-9dc8-79380b36a25f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b0783a05f658da5e93603e26dc7e9581d26b81f9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805225"
---
# <span data-ttu-id="94b90-103">So veröffentlichen Sie mithilfe der Verwaltungskonsole ein Paket</span><span class="sxs-lookup"><span data-stu-id="94b90-103">How to Publish a Package by Using the Management Console</span></span>


<span data-ttu-id="94b90-104">Gehen Sie wie folgt vor, um ein App-V 5,1-Paket zu veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="94b90-104">Use the following procedure to publish an App-V 5.1 package.</span></span> <span data-ttu-id="94b90-105">Nachdem Sie ein Paket veröffentlicht haben, können Computer, auf denen der App-V 5,1-Client ausgeführt wird, auf die Anwendungen in diesem Paket zugreifen und diese ausführen.</span><span class="sxs-lookup"><span data-stu-id="94b90-105">Once you publish a package, computers that are running the App-V 5.1 client can access and run the applications in that package.</span></span>

<span data-ttu-id="94b90-106">**Hinweis**  Die Möglichkeit, nur Administratoren zum Veröffentlichen oder Aufheben der Veröffentlichung von Paketen (siehe unten) zu aktivieren, wird ab App-V 5,0 SP3 unterstützt.</span><span class="sxs-lookup"><span data-stu-id="94b90-106">**Note** The ability to enable only administrators to publish or unpublish packages (described below) is supported starting in App-V 5.0 SP3.</span></span>

 

**<span data-ttu-id="94b90-107">So veröffentlichen Sie ein App-V 5,1-Paket</span><span class="sxs-lookup"><span data-stu-id="94b90-107">To publish an App-V 5.1 package</span></span>**

1.  <span data-ttu-id="94b90-108">In der App-V 5,1-Verwaltungskonsole.</span><span class="sxs-lookup"><span data-stu-id="94b90-108">In the App-V 5.1 Management console.</span></span> <span data-ttu-id="94b90-109">Klicken oder klicken Sie mit der rechten Maustaste auf den Namen des zu veröffentlichenden Pakets.</span><span class="sxs-lookup"><span data-stu-id="94b90-109">Click or right-click the name of the package to be published.</span></span> <span data-ttu-id="94b90-110">Wählen Sie **veröffentlichen**aus.</span><span class="sxs-lookup"><span data-stu-id="94b90-110">Select **Publish**.</span></span>

2.  <span data-ttu-id="94b90-111">Überprüfen Sie die Spalte **Status** , um zu überprüfen, ob das Paket veröffentlicht wurde und nun verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="94b90-111">Review the **Status** column to verify that the package has been published and is now available.</span></span> <span data-ttu-id="94b90-112">Wenn das Paket verfügbar ist, wird der **veröffentlichte** Status angezeigt.</span><span class="sxs-lookup"><span data-stu-id="94b90-112">If the package is available, the status **published** is displayed.</span></span>

    <span data-ttu-id="94b90-113">Wenn das Paket nicht erfolgreich veröffentlicht wird, wird der Status **unveröffentlicht** zusammen mit dem Fehlertext angezeigt, in dem erläutert wird, warum das Paket nicht verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="94b90-113">If the package is not published successfully, the status **unpublished** is displayed, along with error text that explains why the package is not available.</span></span>

**<span data-ttu-id="94b90-114">So aktivieren Sie nur Administratoren zum Veröffentlichen oder Aufheben der Veröffentlichung von Paketen</span><span class="sxs-lookup"><span data-stu-id="94b90-114">To enable only administrators to publish or unpublish packages</span></span>**

1.  <span data-ttu-id="94b90-115">Navigieren Sie zum folgenden Gruppenrichtlinien-Objektknoten:</span><span class="sxs-lookup"><span data-stu-id="94b90-115">Navigate to the following Group Policy Object node:</span></span>

    <span data-ttu-id="94b90-116">**Computer Konfiguration &gt; Richtlinien &gt; Administrative Vorlagen &gt; System &gt; App-V &gt; Publishing**.</span><span class="sxs-lookup"><span data-stu-id="94b90-116">**Computer Configuration &gt; Policies &gt; Administrative Templates &gt; System &gt; App-V &gt; Publishing**.</span></span>

2.  <span data-ttu-id="94b90-117">Aktivieren Sie die Gruppenrichtlinieneinstellung **Veröffentlichung als Administrator anfordern** .</span><span class="sxs-lookup"><span data-stu-id="94b90-117">Enable the **Require publish as administrator** Group Policy setting.</span></span>

    <span data-ttu-id="94b90-118">Informationen zum Verwenden von PowerShell zum Einrichten dieses Elements finden Sie unter [Verwalten von App-V 5,1-Paketen, die mit PowerShell auf einem eigenständigen Computer ausgeführt](how-to-manage-app-v-51-packages-running-on-a-stand-alone-computer-by-using-powershell.md#bkmk-admins-pub-pkgs)werden.</span><span class="sxs-lookup"><span data-stu-id="94b90-118">To alternatively use PowerShell to set this item, see [How to Manage App-V 5.1 Packages Running on a Stand-Alone Computer by Using PowerShell](how-to-manage-app-v-51-packages-running-on-a-stand-alone-computer-by-using-powershell.md#bkmk-admins-pub-pkgs).</span></span>

    <span data-ttu-id="94b90-119">Sie **haben einen Vorschlag für App-V**?</span><span class="sxs-lookup"><span data-stu-id="94b90-119">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="94b90-120">[Hier](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)können Sie Vorschläge hinzufügen oder abstimmen.</span><span class="sxs-lookup"><span data-stu-id="94b90-120">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="94b90-121">Sie haben ein App-V-Problem?</span><span class="sxs-lookup"><span data-stu-id="94b90-121">Got an App-V issue?</span></span>** <span data-ttu-id="94b90-122">Verwenden Sie das [App-V TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="94b90-122">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="94b90-123">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="94b90-123">Related topics</span></span>


[<span data-ttu-id="94b90-124">Vorgänge für App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="94b90-124">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)

[<span data-ttu-id="94b90-125">So konfigurieren Sie mithilfe der Verwaltungskonsole den Zugriff auf Pakete</span><span class="sxs-lookup"><span data-stu-id="94b90-125">How to Configure Access to Packages by Using the Management Console</span></span>](how-to-configure-access-to-packages-by-using-the-management-console-51.md)

 

 





