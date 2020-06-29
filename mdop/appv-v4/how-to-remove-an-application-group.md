---
title: So entfernen Sie eine Anwendungsgruppe
description: So entfernen Sie eine Anwendungsgruppe
author: dansimp
ms.assetid: 3016b373-f5a0-4c82-96e8-e5e7960f0cc4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b392fe84f4318cf7f355de0c07e4d6f1f5108ed7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806844"
---
# <span data-ttu-id="30541-103">So entfernen Sie eine Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="30541-103">How to Remove an Application Group</span></span>


<span data-ttu-id="30541-104">Mit den folgenden Verfahren können Sie eine Anwendungsgruppe in der Application Virtualization Server Management Console auf eine von zwei Arten entfernen:</span><span class="sxs-lookup"><span data-stu-id="30541-104">You can use the following procedures to remove an application group in the Application Virtualization Server Management Console in one of two ways:</span></span>

<span data-ttu-id="30541-105">**Vorsicht**  Durch das Löschen einer Gruppe mit Ihren Anwendungen werden diese Anwendungen vom Application Virtualization Management Server gelöscht.</span><span class="sxs-lookup"><span data-stu-id="30541-105">**Caution** Deleting a group with its applications deletes those applications from the Application Virtualization Management Server.</span></span> <span data-ttu-id="30541-106">Wenn Sie versuchen, dies zu tun, müssen Sie den Löschvorgang in einem Popupfenster bestätigen.</span><span class="sxs-lookup"><span data-stu-id="30541-106">When you try to do this, you must confirm the deletion in a pop-up window.</span></span>

 

**<span data-ttu-id="30541-107">So leeren Sie eine Anwendungsgruppe und löschen Sie dann</span><span class="sxs-lookup"><span data-stu-id="30541-107">To empty and then delete an application group</span></span>**

1.  <span data-ttu-id="30541-108">Erweitern Sie in der Application Virtualization Server-Verwaltungskonsole **Anwendungen** im linken Bereich, und wählen Sie die **Anwendungs** Gruppe aus, die Sie entfernen möchten.</span><span class="sxs-lookup"><span data-stu-id="30541-108">In the Application Virtualization Server Management Console, expand **Applications** in the left pane and select the **Application** group you want to remove.</span></span>

2.  <span data-ttu-id="30541-109">Wählen Sie im rechten Bereich die Anwendungen und Anwendungsgruppen aus, die Sie beibehalten möchten.</span><span class="sxs-lookup"><span data-stu-id="30541-109">In the right pane, select the applications and application groups you want to keep.</span></span> <span data-ttu-id="30541-110">Sie können die **STRG** -und die **UMSCHALT** Taste verwenden, um mehrere Anwendungen und Anwendungsgruppen auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="30541-110">You can use the **CTRL** and **Shift** keys to select multiple applications and application groups.</span></span>

3.  <span data-ttu-id="30541-111">Klicken Sie mit der rechten Maustaste auf die ausgewählten Anwendungen, und wählen Sie **verschieben**aus.</span><span class="sxs-lookup"><span data-stu-id="30541-111">Right-click the selected applications, and choose **Move**.</span></span>

4.  <span data-ttu-id="30541-112">Navigieren Sie im Fenster **Ziel auswählen** zum neuen Speicherort, und klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="30541-112">In the **Select Target** window, navigate to the new location and click **OK**.</span></span> <span data-ttu-id="30541-113">Wiederholen Sie diesen Schritt, wenn Sie unterschiedliche Anwendungen in mehr als eine Gruppe verschieben möchten.</span><span class="sxs-lookup"><span data-stu-id="30541-113">Repeat this step if you want to move different applications to more than one group.</span></span>

5.  <span data-ttu-id="30541-114">Wenn Sie mit dem Verschieben der Anwendungen fertig sind, die Sie beibehalten möchten, klicken Sie mit der rechten Maustaste auf die Anwendungsgruppe, und wählen Sie **Löschen**aus.</span><span class="sxs-lookup"><span data-stu-id="30541-114">When you finish moving the applications you want to keep, right-click the application group and choose **Delete**.</span></span>

6.  <span data-ttu-id="30541-115">Klicken Sie zum bestätigen auf **Ja** .</span><span class="sxs-lookup"><span data-stu-id="30541-115">Click **Yes** to confirm.</span></span>

**<span data-ttu-id="30541-116">So löschen Sie die Gruppe mit allen untergeordneten Gruppen und Ihren Anwendungen</span><span class="sxs-lookup"><span data-stu-id="30541-116">To delete the group, with all its child groups and its applications</span></span>**

1.  <span data-ttu-id="30541-117">Erweitern Sie in der Application Virtualization Server-Verwaltungskonsole im linken Bereich **Anwendungen** .</span><span class="sxs-lookup"><span data-stu-id="30541-117">In the Application Virtualization Server Management Console, expand **Applications** in the left pane.</span></span>

2.  <span data-ttu-id="30541-118">Klicken Sie mit der rechten Maustaste auf die Anwendungsgruppe, die Sie entfernen möchten, und wählen Sie **Löschen**aus.</span><span class="sxs-lookup"><span data-stu-id="30541-118">Right-click the application group you want to remove, and choose **Delete**.</span></span>

3.  <span data-ttu-id="30541-119">Klicken Sie zum bestätigen auf **Ja** .</span><span class="sxs-lookup"><span data-stu-id="30541-119">Click **Yes** to confirm.</span></span>

    <span data-ttu-id="30541-120">**Hinweis**  Sie können mehrere Anwendungsgruppen gleichzeitig auswählen und entfernen.</span><span class="sxs-lookup"><span data-stu-id="30541-120">**Note** You can select and remove multiple application groups simultaneously.</span></span> <span data-ttu-id="30541-121">Verwenden Sie im rechten Bereich die Tastenkombinationen mit der **STRG**-oder **UMSCHALT**Taste, um mehr als eine Gruppe auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="30541-121">In the right pane, use the **CTRL**-click or **Shift**-click key combinations to select more than one group.</span></span>

     

## <span data-ttu-id="30541-122">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="30541-122">Related topics</span></span>


[<span data-ttu-id="30541-123">So verwalten Sie Anwendungsgruppen in der Server Management Console</span><span class="sxs-lookup"><span data-stu-id="30541-123">How to Manage Application Groups in the Server Management Console</span></span>](how-to-manage-application-groups-in-the-server-management-console.md)

[<span data-ttu-id="30541-124">So verwalten Sie Anwendungen in der Server Management Console</span><span class="sxs-lookup"><span data-stu-id="30541-124">How to Manage Applications in the Server Management Console</span></span>](how-to-manage-applications-in-the-server-management-console.md)

 

 





