---
title: So fügen Sie mithilfe der Verwaltungskonsole einen Administrator hinzu oder entfernen einen Administrator
description: So fügen Sie mithilfe der Verwaltungskonsole einen Administrator hinzu oder entfernen einen Administrator
author: dansimp
ms.assetid: 7ff8c436-9d2e-446a-9ea2-bbab7e25bf21
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8fbc1a532a39c8688b99c28a2e23b713b348967c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805768"
---
# <span data-ttu-id="a3d0c-103">So fügen Sie mithilfe der Verwaltungskonsole einen Administrator hinzu oder entfernen einen Administrator</span><span class="sxs-lookup"><span data-stu-id="a3d0c-103">How to Add or Remove an Administrator by Using the Management Console</span></span>


<span data-ttu-id="a3d0c-104">Führen Sie die folgenden Verfahren aus, um einen Administrator auf dem Microsoft Application Virtualization (App-V) 5,1-Server hinzuzufügen oder zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="a3d0c-104">Use the following procedures to add or remove an administrator on the Microsoft Application Virtualization (App-V) 5.1 server.</span></span>

**<span data-ttu-id="a3d0c-105">So fügen Sie einen Administrator mithilfe der Verwaltungskonsole hinzu</span><span class="sxs-lookup"><span data-stu-id="a3d0c-105">To add an administrator using the Management Console</span></span>**

1.  <span data-ttu-id="a3d0c-106">Öffnen Sie die 5,1-Verwaltungskonsole von Microsoft Application Virtualization (App-V), und klicken Sie im Navigationsbereich auf **Administratoren** .</span><span class="sxs-lookup"><span data-stu-id="a3d0c-106">Open the Microsoft Application Virtualization (App-V) 5.1 Management Console and click **Administrators** in the navigation pane.</span></span> <span data-ttu-id="a3d0c-107">Der Navigationsbereich zeigt eine Liste von Benutzer und Gruppen für das Access-Verzeichnis (AD) an, die derzeit über Administratorzugriff auf den Microsoft Application Virtualization (App-V) 5,1-Server verfügen.</span><span class="sxs-lookup"><span data-stu-id="a3d0c-107">The navigation pane displays a list of Access Directory (AD) users and groups that currently have administrative access to the Microsoft Application Virtualization (App-V) 5.1 server.</span></span>

2.  <span data-ttu-id="a3d0c-108">Klicken Sie zum Hinzufügen eines neuen Administrators auf **Add Administrator** geben Sie den Namen des Administrators, den Sie hinzufügen möchten, in das Feld **Active Directory-Name** ein.</span><span class="sxs-lookup"><span data-stu-id="a3d0c-108">To add a new administrator, click **Add Administrator** Type the name of the administrator that you want to add in the **Active Directory Name** field.</span></span> <span data-ttu-id="a3d0c-109">Stellen Sie sicher, dass Sie den Domänennamen des zugehörigen Benutzerkontos angeben.</span><span class="sxs-lookup"><span data-stu-id="a3d0c-109">Ensure you provide the associated user account domain name.</span></span> <span data-ttu-id="a3d0c-110">Beispiel: **Domänen**  \\  **Name**.</span><span class="sxs-lookup"><span data-stu-id="a3d0c-110">For example, **Domain** \\ **UserName**.</span></span>

3.  <span data-ttu-id="a3d0c-111">Wählen Sie das Konto aus, das Sie hinzufügen möchten, und klicken Sie auf **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="a3d0c-111">Select the account that you want to add and click **Add**.</span></span> <span data-ttu-id="a3d0c-112">Das neue Konto wird in der Liste der Serveradministratoren angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a3d0c-112">The new account is displayed in the list of server administrators.</span></span>

**<span data-ttu-id="a3d0c-113">So entfernen Sie einen Administrator mithilfe der Verwaltungskonsole</span><span class="sxs-lookup"><span data-stu-id="a3d0c-113">To remove an administrator using the Management Console</span></span>**

1.  <span data-ttu-id="a3d0c-114">Öffnen Sie die 5,1-Verwaltungskonsole von Microsoft Application Virtualization (App-V), und klicken Sie im Navigationsbereich auf **Administratoren** .</span><span class="sxs-lookup"><span data-stu-id="a3d0c-114">Open the Microsoft Application Virtualization (App-V) 5.1 Management Console and click **Administrators** in the navigation pane.</span></span> <span data-ttu-id="a3d0c-115">Der Navigationsbereich zeigt eine Liste der AD-Benutzer und-Gruppen an, die derzeit über Administratorzugriff auf den Microsoft Application Virtualization (App-V) 5,1-Server verfügen.</span><span class="sxs-lookup"><span data-stu-id="a3d0c-115">The navigation pane displays a list of AD users and groups that currently have administrative access to the Microsoft Application Virtualization (App-V) 5.1 server.</span></span>

2.  <span data-ttu-id="a3d0c-116">Klicken Sie mit der rechten Maustaste auf das Konto, das aus der Liste der Administratoren entfernt werden soll, und wählen Sie **Entfernen**aus.</span><span class="sxs-lookup"><span data-stu-id="a3d0c-116">Right-click the account to be removed from the list of administrators and select **Remove**.</span></span>

    <span data-ttu-id="a3d0c-117">Sie **haben einen Vorschlag für App-V**?</span><span class="sxs-lookup"><span data-stu-id="a3d0c-117">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="a3d0c-118">[Hier](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)können Sie Vorschläge hinzufügen oder abstimmen.</span><span class="sxs-lookup"><span data-stu-id="a3d0c-118">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="a3d0c-119">Sie haben ein App-V-Problem?</span><span class="sxs-lookup"><span data-stu-id="a3d0c-119">Got an App-V issue?</span></span>** <span data-ttu-id="a3d0c-120">Verwenden Sie das [App-V TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="a3d0c-120">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="a3d0c-121">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="a3d0c-121">Related topics</span></span>


[<span data-ttu-id="a3d0c-122">Vorgänge für App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="a3d0c-122">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)

 

 





