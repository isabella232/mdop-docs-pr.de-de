---
title: So verwalten Sie Anwendungslizenzen in der Server Management Console
description: So verwalten Sie Anwendungslizenzen in der Server Management Console
author: dansimp
ms.assetid: 48503b04-0de7-48de-98ee-4623a712a341
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ca9ab54c8b4cee06e0b17d8b5dee3d3ca7ce69c5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807020"
---
# <span data-ttu-id="a9a38-103">So verwalten Sie Anwendungslizenzen in der Server Management Console</span><span class="sxs-lookup"><span data-stu-id="a9a38-103">How to Manage Application Licenses in the Server Management Console</span></span>


<span data-ttu-id="a9a38-104">Bei der Application Virtualization Server-Verwaltungskonsole handelt es sich um die Schnittstelle, die Sie zum Verwalten der Application Virtualization-Plattform verwenden.</span><span class="sxs-lookup"><span data-stu-id="a9a38-104">The Application Virtualization Server Management Console is the interface you use to manage the Application Virtualization platform.</span></span> <span data-ttu-id="a9a38-105">In diesem Fall können Sie Anwendungslizenzgruppen hinzufügen, entfernen, konfigurieren und steuern.</span><span class="sxs-lookup"><span data-stu-id="a9a38-105">From it, you can add, remove, configure, and control application license groups.</span></span>

<span data-ttu-id="a9a38-106">**Wichtig**  Wenn die Einstellung App-V Client Application Source Root (ASR) so konfiguriert ist, dass Sie eine andere Art von Streaming-Quelle als den Verwaltungsserver verwendet, beispielsweise einen Streamingserver, einen IIS-Server oder einen Dateiserver, kann der Verwaltungsserver seine Lizenzierungsrichtlinie nicht erzwingen.</span><span class="sxs-lookup"><span data-stu-id="a9a38-106">**Important** If the App-V client Application Source Root (ASR) setting is configured to use any type of streaming source other than the Management Server, for example a Streaming Server, an IIS server, or a File server, then the Management Server is unable to enforce its licensing policy.</span></span>

 

## <span data-ttu-id="a9a38-107">Inhalt dieses Abschnitts</span><span class="sxs-lookup"><span data-stu-id="a9a38-107">In This Section</span></span>


<a href="" id="how-to-create-an-application-license-group"></a>[<span data-ttu-id="a9a38-108">So erstellen Sie eine Anwendungslizenzgruppe</span><span class="sxs-lookup"><span data-stu-id="a9a38-108">How to Create an Application License Group</span></span>](how-to-create-an-application-license-group.md)  
<span data-ttu-id="a9a38-109">Enthält eine Vorgehensweise zum Erstellen einer neuen Anwendung in einer Lizenzgruppe.</span><span class="sxs-lookup"><span data-stu-id="a9a38-109">Provides a procedure for creating a new application in a license group.</span></span>

<a href="" id="how-to-associate-an-application-with-a-license-group"></a>[<span data-ttu-id="a9a38-110">So ordnen Sie einer Lizenzgruppe eine Anwendung zu</span><span class="sxs-lookup"><span data-stu-id="a9a38-110">How to Associate an Application with a License Group</span></span>](how-to-associate-an-application-with-a-license-group.md)  
<span data-ttu-id="a9a38-111">Enthält ein Verfahren zum Hinzufügen einer Anwendung zu einer Lizenzgruppe.</span><span class="sxs-lookup"><span data-stu-id="a9a38-111">Provides a procedure for adding an application to a license group.</span></span>

<a href="" id="how-to-remove-an-application-from-a-license-group"></a>[<span data-ttu-id="a9a38-112">So entfernen Sie eine Anwendung aus einer Lizenzgruppe</span><span class="sxs-lookup"><span data-stu-id="a9a38-112">How to Remove an Application from a License Group</span></span>](how-to-remove-an-application-from-a-license-group.md)  
<span data-ttu-id="a9a38-113">Enthält eine Vorgehensweise zum Entfernen einer Anwendung aus einer Lizenzgruppe.</span><span class="sxs-lookup"><span data-stu-id="a9a38-113">Provides a procedure for removing an application from a license group.</span></span>

<a href="" id="how-to-remove-an-application-license-group"></a>[<span data-ttu-id="a9a38-114">So entfernen Sie eine Anwendungslizenzgruppe</span><span class="sxs-lookup"><span data-stu-id="a9a38-114">How to Remove an Application License Group</span></span>](how-to-remove-an-application-license-group.md)  
<span data-ttu-id="a9a38-115">Dieser Abschnitt enthält die erforderlichen Schritte zum Löschen einer Anwendungslizenzgruppe.</span><span class="sxs-lookup"><span data-stu-id="a9a38-115">This section includes the steps necessary to delete an application license group.</span></span>

<a href="" id="how-to-set-up-an-unlimited-license-group"></a>[<span data-ttu-id="a9a38-116">So richten Sie eine Gruppe für unbeschränkte Lizenzen ein</span><span class="sxs-lookup"><span data-stu-id="a9a38-116">How to Set Up an Unlimited License Group</span></span>](how-to-set-up-an-unlimited-license-group.md)  
<span data-ttu-id="a9a38-117">Bietet eine Vorgehensweise zum Erstellen einer neuen unbegrenzten Lizenzgruppe, die es einer unbegrenzten Anzahl von Benutzern ermöglicht, auf die Anwendungen in der Gruppe zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="a9a38-117">Provides a procedure for creating a new unlimited license group, allowing an unlimited number of users to access the applications in the group.</span></span>

<a href="" id="how-to-set-up-a-concurrent-license-group"></a>[<span data-ttu-id="a9a38-118">So richten Sie eine Gruppe für gleichzeitige Lizenzen ein</span><span class="sxs-lookup"><span data-stu-id="a9a38-118">How to Set Up a Concurrent License Group</span></span>](how-to-set-up-a-concurrent-license-group.md)  
<span data-ttu-id="a9a38-119">Bietet eine Vorgehensweise zum Erstellen einer neuen parallelen Lizenzgruppe, die es einer bestimmten Anzahl von gleichzeitigen Benutzern ermöglicht, auf die Anwendungen in der Gruppe zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="a9a38-119">Provides a procedure for creating a new concurrent license group, allowing a specific number of concurrent users to access the applications in the group.</span></span>

<a href="" id="how-to-set-up-a-named-license-group"></a>[<span data-ttu-id="a9a38-120">So richten Sie eine Gruppe für benannte Lizenzen ein</span><span class="sxs-lookup"><span data-stu-id="a9a38-120">How to Set Up a Named License Group</span></span>](how-to-set-up-a-named-license-group.md)  
<span data-ttu-id="a9a38-121">Bietet eine Vorgehensweise zum Erstellen einer neuen unbegrenzten Lizenzgruppe, die bestimmten Benutzern den Zugriff auf die Anwendungen in der Gruppe ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="a9a38-121">Provides a procedure for creating a new unlimited license group, allowing specific users to access the applications in the group.</span></span>

## <span data-ttu-id="a9a38-122">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="a9a38-122">Related topics</span></span>


[<span data-ttu-id="a9a38-123">So führen Sie Verwaltungsaufgaben in der Application Virtualization Server Management Console durch</span><span class="sxs-lookup"><span data-stu-id="a9a38-123">How to Perform Administrative Tasks in the Application Virtualization Server Management Console</span></span>](how-to-perform-administrative-tasks-in-the-application-virtualization-server-management-console.md)

 

 





