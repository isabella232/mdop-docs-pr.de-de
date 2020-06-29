---
title: So verwalten Sie Anwendungsgruppen in der Server Management Console
description: So verwalten Sie Anwendungsgruppen in der Server Management Console
author: dansimp
ms.assetid: 46997971-bdc8-4565-aefd-f47e90d6d7a6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 59a357d93ea63cc728f59a0633b7a5b9953aad14
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807012"
---
# <span data-ttu-id="b763b-103">So verwalten Sie Anwendungsgruppen in der Server Management Console</span><span class="sxs-lookup"><span data-stu-id="b763b-103">How to Manage Application Groups in the Server Management Console</span></span>


<span data-ttu-id="b763b-104">Sie können eine oder mehrere Anwendungen in Anwendungsgruppen in der Application Virtualization Server-Verwaltungskonsole anzeigen und verwalten.</span><span class="sxs-lookup"><span data-stu-id="b763b-104">You can display and manage one or more applications in application groups in the Application Virtualization Server Management Console.</span></span> <span data-ttu-id="b763b-105">Dies kann hilfreich sein, wenn Sie die folgenden Aktionen ausführen möchten:</span><span class="sxs-lookup"><span data-stu-id="b763b-105">This can be useful when you want to do the following:</span></span>

-   <span data-ttu-id="b763b-106">Organisieren Sie viele Anwendungen in mehr verwaltbaren Untergruppen.</span><span class="sxs-lookup"><span data-stu-id="b763b-106">Organize many applications into more manageable subgroups.</span></span>

-   <span data-ttu-id="b763b-107">Erstellen Sie Gruppen von Anwendungen, die für eine Abteilung oder eine andere Unternehmenssparte spezifisch sind.</span><span class="sxs-lookup"><span data-stu-id="b763b-107">Create groups of applications specific to a department or other company division.</span></span>

-   <span data-ttu-id="b763b-108">Gruppieren Sie ähnliche Anwendungstypen wie Finanzsoftware.</span><span class="sxs-lookup"><span data-stu-id="b763b-108">Group similar types of applications, such as financial software.</span></span>

-   <span data-ttu-id="b763b-109">Vereinfachen Sie die Zugriffsberechtigungen oder die Lizenzverwaltung nach Gruppen.</span><span class="sxs-lookup"><span data-stu-id="b763b-109">Simplify access permissions or license management by group.</span></span>

-   <span data-ttu-id="b763b-110">Sie können die Eigenschaften von Anwendungen und Anwendungsgruppen in einer Gruppe gleichzeitig ändern.</span><span class="sxs-lookup"><span data-stu-id="b763b-110">Change the properties of applications and application groups within a group simultaneously.</span></span>

<span data-ttu-id="b763b-111">Sie können eine Gruppe erstellen, Sie an der gewünschten Stelle in der **Anwendungs** Struktur der Konsole platzieren und Anwendungen in die Gruppe importieren.</span><span class="sxs-lookup"><span data-stu-id="b763b-111">You can create a group, place it where you would like in the console's **Applications** tree, and import applications to the group.</span></span> <span data-ttu-id="b763b-112">Anschließend können Sie die Eigenschaften der Gruppe konfigurieren und verwalten, um alle Anwendungen zu beeinflussen.</span><span class="sxs-lookup"><span data-stu-id="b763b-112">Then you can configure and manage the group's properties to affect all of its applications.</span></span> <span data-ttu-id="b763b-113">Sie können auch Anwendungen zwischen Gruppen verschieben.</span><span class="sxs-lookup"><span data-stu-id="b763b-113">You can also move applications among groups.</span></span>

<span data-ttu-id="b763b-114">**Hinweis**  Das Verschieben von Anwendungen in Gruppen hat keinen Einfluss auf die Speicherorte Ihrer Dateien (SFT, OSD oder SPRJ) im Dateisystem des Servers.</span><span class="sxs-lookup"><span data-stu-id="b763b-114">**Note** Moving applications into groups does not affect the locations of their files (SFT, OSD, or SPRJ) on the server's file system.</span></span>

 

## <span data-ttu-id="b763b-115">Inhalt dieses Abschnitts</span><span class="sxs-lookup"><span data-stu-id="b763b-115">In This Section</span></span>


<a href="" id="how-to-create-an-application-group"></a>[<span data-ttu-id="b763b-116">So erstellen Sie eine Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="b763b-116">How to Create an Application Group</span></span>](how-to-create-an-application-group.md)  
<span data-ttu-id="b763b-117">Enthält Schritt-für-Schritt-Anleitungen zum Erstellen einer Anwendungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="b763b-117">Provides step-by-step instructions for creating an application group.</span></span>

<a href="" id="how-to-move-an-application-group"></a>[<span data-ttu-id="b763b-118">So verschieben Sie eine Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="b763b-118">How to Move an Application Group</span></span>](how-to-move-an-application-group.md)  
<span data-ttu-id="b763b-119">Enthält Schritt-für-Schritt-Anweisungen zum Verschieben einer Anwendungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="b763b-119">Provides step-by-step instructions for moving an application group.</span></span>

<a href="" id="how-to-rename-an-application-group"></a>[<span data-ttu-id="b763b-120">So benennen Sie eine Anwendungsgruppe um</span><span class="sxs-lookup"><span data-stu-id="b763b-120">How to Rename an Application Group</span></span>](how-to-rename-an-application-group.md)  
<span data-ttu-id="b763b-121">Enthält Schritt-für-Schritt-Anleitungen zum Umbenennen einer Anwendungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="b763b-121">Provides step-by-step instructions for renaming an application group.</span></span>

<a href="" id="how-to-remove-an-application-group"></a>[<span data-ttu-id="b763b-122">So entfernen Sie eine Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="b763b-122">How to Remove an Application Group</span></span>](how-to-remove-an-application-group.md)  
<span data-ttu-id="b763b-123">Enthält Schritt-für-Schritt-Anweisungen zum Entfernen oder Löschen einer Anwendungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="b763b-123">Provides step-by-step instructions for removing or deleting an application group.</span></span>

## <span data-ttu-id="b763b-124">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="b763b-124">Related topics</span></span>


[<span data-ttu-id="b763b-125">So verwalten Sie Anwendungen in der Server Management Console</span><span class="sxs-lookup"><span data-stu-id="b763b-125">How to Manage Applications in the Server Management Console</span></span>](how-to-manage-applications-in-the-server-management-console.md)

[<span data-ttu-id="b763b-126">So führen Sie Verwaltungsaufgaben in der Application Virtualization Server Management Console durch</span><span class="sxs-lookup"><span data-stu-id="b763b-126">How to Perform Administrative Tasks in the Application Virtualization Server Management Console</span></span>](how-to-perform-administrative-tasks-in-the-application-virtualization-server-management-console.md)

 

 





