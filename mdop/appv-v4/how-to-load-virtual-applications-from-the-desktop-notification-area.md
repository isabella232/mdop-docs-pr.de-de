---
title: So laden Sie virtuelle Anwendungen aus dem Desktop-Infobereich
description: So laden Sie virtuelle Anwendungen aus dem Desktop-Infobereich
author: dansimp
ms.assetid: f52758eb-8b81-4b3c-9bc3-adcf7c00c238
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d7004f9e0031dfeeedc8b6a916e2f3488f1d31e1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807019"
---
# <span data-ttu-id="71d33-103">So laden Sie virtuelle Anwendungen aus dem Desktop-Infobereich</span><span class="sxs-lookup"><span data-stu-id="71d33-103">How to Load Virtual Applications from the Desktop Notification Area</span></span>


<span data-ttu-id="71d33-104">Wenn Sie ein mobiler Benutzer sind, möchten Sie möglicherweise Ihre Anwendungen im Cache vollständig laden, um Sie während des getrennten Betriebs oder Offlinemodus zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="71d33-104">If you are a mobile user, you might want to fully load your applications in the cache to use them during disconnected operation or offline mode.</span></span> <span data-ttu-id="71d33-105">Damit Anwendungen von Application Virtualization (app-v) oder Application Virtualization (app-v) Streaming Server gestreamt werden können, müssen Sie mit einem Server verbunden sein, um Anwendungen zu laden.</span><span class="sxs-lookup"><span data-stu-id="71d33-105">To stream applications from the Application Virtualization (App-V) Server or the Application Virtualization (App-V) Streaming Server, you must be connected to a server to load applications.</span></span> <span data-ttu-id="71d33-106">Wenn Sie nicht mit dem Server verbunden sind, wenn Sie versuchen, Anwendungen zu laden, generiert Ihr System eine entsprechende Fehlermeldung.</span><span class="sxs-lookup"><span data-stu-id="71d33-106">If you are not connected to the server when you attempt to load applications, your system will generate an appropriate error message.</span></span> <span data-ttu-id="71d33-107">Sie können Anwendungen auch aus einer Datei oder einem Datenträger an den Client streamen.</span><span class="sxs-lookup"><span data-stu-id="71d33-107">You can also stream applications to the client from a file or disk.</span></span>

<span data-ttu-id="71d33-108">Die Anwendungen werden jeweils eine Anwendung geladen.</span><span class="sxs-lookup"><span data-stu-id="71d33-108">The applications are loaded one application at a time.</span></span> <span data-ttu-id="71d33-109">Die Statusleiste zeigt den Anwendungsnamen, den Prozentsatz der geladenen Anwendung und die Anzahl der Anwendungen an, die bereits im Vergleich zur Gesamtzahl der in der Warteschlange befindlichen Anwendungen verarbeitet wurden.</span><span class="sxs-lookup"><span data-stu-id="71d33-109">The progress bar shows you the application name, the percentage of application loaded, and the number of applications already processed compared to the total number of the applications queued.</span></span> <span data-ttu-id="71d33-110">Sie können alle laufenden Anwendungen überspringen, bevor Sie 100% geladen werden.</span><span class="sxs-lookup"><span data-stu-id="71d33-110">You can skip any application in progress before it is 100% loaded.</span></span> <span data-ttu-id="71d33-111">Sie können auch das Laden aller verbleibenden Anwendungen überspringen.</span><span class="sxs-lookup"><span data-stu-id="71d33-111">You can skip the loading of all remaining applications as well.</span></span>

<span data-ttu-id="71d33-112">**Hinweis**  Wenn Ihr System beim Laden einer Anwendung einen Fehler findet, wird Ihnen der Fehler gemeldet.</span><span class="sxs-lookup"><span data-stu-id="71d33-112">**Note** If your system encounters an error while loading an application, it reports the error to you.</span></span> <span data-ttu-id="71d33-113">Sie müssen das Fehlerdialogfeld schließen, bevor die nächste Anwendung geladen wird.</span><span class="sxs-lookup"><span data-stu-id="71d33-113">You must dismiss the error dialog before it will load the next application.</span></span>

 

**<span data-ttu-id="71d33-114">So laden Sie alle Anwendungen</span><span class="sxs-lookup"><span data-stu-id="71d33-114">To load all applications</span></span>**

1.  <span data-ttu-id="71d33-115">Klicken Sie mit der rechten Maustaste im Infobereich auf das Symbol Application Virtualization System.</span><span class="sxs-lookup"><span data-stu-id="71d33-115">Right-click the Application Virtualization System icon in the notification area.</span></span>

2.  <span data-ttu-id="71d33-116">Wählen Sie im Popupmenü **Anwendungen laden** aus.</span><span class="sxs-lookup"><span data-stu-id="71d33-116">Select **Load Applications** from the pop-up menu.</span></span>

**<span data-ttu-id="71d33-117">So überspringen Sie Anwendungen</span><span class="sxs-lookup"><span data-stu-id="71d33-117">To skip applications</span></span>**

1.  <span data-ttu-id="71d33-118">Klicken Sie auf die Statusleiste, um das Dialogfeld anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="71d33-118">Click the progress bar to display the dialog box.</span></span>

2.  <span data-ttu-id="71d33-119">Wählen Sie eine der folgenden Schaltflächen aus, um die gewünschten Ergebnisse zu erzielen:</span><span class="sxs-lookup"><span data-stu-id="71d33-119">Select one of the following buttons to achieve the desired results:</span></span>

    1.  <span data-ttu-id="71d33-120">**Skip**– zum Überspringen der aktuell ladenden Anwendung.</span><span class="sxs-lookup"><span data-stu-id="71d33-120">**Skip**—To skip the currently loading application.</span></span>

    2.  <span data-ttu-id="71d33-121">**Alle überspringen**– um alle verbleibenden Anwendungen zu überspringen.</span><span class="sxs-lookup"><span data-stu-id="71d33-121">**Skip All**—To skip all remaining applications.</span></span>

    3.  <span data-ttu-id="71d33-122">**Weiter**– zum Abbrechen des Dialogfelds und zum Fortsetzen des Ladens von Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="71d33-122">**Continue**—To cancel the dialog box and continue loading applications.</span></span>

## <span data-ttu-id="71d33-123">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="71d33-123">Related topics</span></span>


[<span data-ttu-id="71d33-124">So verwenden Sie den Desktop-Infobereich für Application Virtualization Client Management</span><span class="sxs-lookup"><span data-stu-id="71d33-124">How to Use the Desktop Notification Area for Application Virtualization Client Management</span></span>](how-to-use-the-desktop-notification-area-for-application-virtualization-client-management.md)

 

 





