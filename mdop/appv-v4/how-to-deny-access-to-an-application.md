---
title: So verweigern Sie den Zugriff auf eine Anwendung
description: So verweigern Sie den Zugriff auf eine Anwendung
author: dansimp
ms.assetid: 14f5e201-7265-462c-b738-57938dc3fc30
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 56a89669ea8c6323023b585d6d58620cd203fc00
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807139"
---
# <span data-ttu-id="197e1-103">So verweigern Sie den Zugriff auf eine Anwendung</span><span class="sxs-lookup"><span data-stu-id="197e1-103">How to Deny Access to an Application</span></span>


<span data-ttu-id="197e1-104">Benutzer müssen in der Liste der **Zugriffsberechtigungen** einer Anwendung sein, um die Anwendung laden und verwenden zu können.</span><span class="sxs-lookup"><span data-stu-id="197e1-104">Users must be in an application's **Access Permissions** list to load and use the application.</span></span> <span data-ttu-id="197e1-105">Die Application Virtualization Server-Verwaltungskonsole unterstützt zwar nicht die explizite Verweigerung des Zugriffs einer Benutzergruppe auf eine Anwendung, aber Sie können die Benutzergruppen aus den Eigenschaften einer Anwendung entfernen, um dies zu erreichen.</span><span class="sxs-lookup"><span data-stu-id="197e1-105">Although the Application Virtualization Server Management Console does not support explicitly denying a user group access to an application, you can remove the user groups from an application’s properties to achieve this.</span></span>

**<span data-ttu-id="197e1-106">So verweigern Sie den Zugriff auf eine Anwendung</span><span class="sxs-lookup"><span data-stu-id="197e1-106">To deny access to an application</span></span>**

1.  <span data-ttu-id="197e1-107">Klicken Sie für eine vorhandene Anwendung im linken Bereich auf den Knoten **Anwendungen** .</span><span class="sxs-lookup"><span data-stu-id="197e1-107">For an existing application, click the **Applications** node in the left pane.</span></span>

2.  <span data-ttu-id="197e1-108">Klicken Sie im rechten Bereich mit der rechten Maustaste auf eine Anwendung, und wählen Sie **Eigenschaften**aus.</span><span class="sxs-lookup"><span data-stu-id="197e1-108">Right-click an application in the right pane, and choose **Properties**.</span></span> <span data-ttu-id="197e1-109">Wählen Sie dann die Registerkarte **Zugriffsberechtigungen** aus.</span><span class="sxs-lookup"><span data-stu-id="197e1-109">Then select the **Access Permissions** tab.</span></span>

3.  <span data-ttu-id="197e1-110">Wenn Sie den Zugriff für eine Benutzergruppe entfernen möchten, markieren Sie die Benutzergruppe, und klicken Sie auf **Entfernen**.</span><span class="sxs-lookup"><span data-stu-id="197e1-110">To remove access for a user group, highlight the user group and click **Remove**.</span></span>

4.  <span data-ttu-id="197e1-111">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="197e1-111">Click **OK**.</span></span>

    <span data-ttu-id="197e1-112">**Hinweis**  Um den Zugriff auf Anwendungen zu steuern, können Sie auch die Anwendungslizenzen einschränken.</span><span class="sxs-lookup"><span data-stu-id="197e1-112">**Note** To control access to applications, you can also limit the application licenses.</span></span> <span data-ttu-id="197e1-113">Das Einrichten der richtigen Benutzergruppen in den Active Directory-Domänendiensten bietet die einfachste Möglichkeit zum gewähren und Verweigern des Zugriffs auf bestimmte Gruppen von Benutzern.</span><span class="sxs-lookup"><span data-stu-id="197e1-113">Setting up the proper user groups in Active Directory Domain Services provides the easiest way to grant and deny access to specific sets of users.</span></span>

     

## <span data-ttu-id="197e1-114">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="197e1-114">Related topics</span></span>


[<span data-ttu-id="197e1-115">So gewähren Sie Zugriff auf eine Anwendung</span><span class="sxs-lookup"><span data-stu-id="197e1-115">How to Grant Access to an Application</span></span>](how-to-grant-access-to-an-application.md)

[<span data-ttu-id="197e1-116">So verwalten Sie Anwendungslizenzen in der Server Management Console</span><span class="sxs-lookup"><span data-stu-id="197e1-116">How to Manage Application Licenses in the Server Management Console</span></span>](how-to-manage-application-licenses-in-the-server-management-console.md)

[<span data-ttu-id="197e1-117">So verwalten Sie Anwendungen in der Server Management Console</span><span class="sxs-lookup"><span data-stu-id="197e1-117">How to Manage Applications in the Server Management Console</span></span>](how-to-manage-applications-in-the-server-management-console.md)

 

 





