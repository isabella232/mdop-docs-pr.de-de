---
title: Informationen zu Application Virtualization-Anwendungen
description: Informationen zu Application Virtualization-Anwendungen
author: dansimp
ms.assetid: 3bf833b7-d172-4eef-a9e8-4b4f0c7eb15b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4eeea7a0ec4454aefcdde5196ae15ed029da45b5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808167"
---
# <span data-ttu-id="b277e-103">Informationen zu Application Virtualization-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="b277e-103">About Application Virtualization Applications</span></span>


<span data-ttu-id="b277e-104">In Application Virtualization ist eine *Anwendung* ein ausführbares Programm wie Microsoft Visio, das über einen Application Virtualization-Verwaltungs Server an den Application Virtualization-Desktop Client oder-Client für Remote Desktop Dienste (ehemals Terminal Dienste) gestreamt wird.</span><span class="sxs-lookup"><span data-stu-id="b277e-104">In Application Virtualization, an *application* is an executable program, such as Microsoft Visio, that is streamed to the Application Virtualization Desktop Client or Client for Remote Desktop Services (formerly Terminal Services) from an Application Virtualization Management Server.</span></span> <span data-ttu-id="b277e-105">Bevor eine Anwendung an einen Client gestreamt werden kann, muss die Anwendung für das Streaming vorbereitet werden, indem Sie Sie mit dem Application Virtualization Sequencer verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="b277e-105">Before an application can be streamed to a client, the application must be prepared for streaming by processing it with the Application Virtualization Sequencer.</span></span>

## <span data-ttu-id="b277e-106">Verwalten von Anwendungen</span><span class="sxs-lookup"><span data-stu-id="b277e-106">Managing Applications</span></span>


<span data-ttu-id="b277e-107">Sie müssen dem Systemanwendungen hinzufügen, bevor Sie die Anwendungen Benutzern zur Verfügung stellen können.</span><span class="sxs-lookup"><span data-stu-id="b277e-107">You must add applications to the system before you can make the applications available to users.</span></span> <span data-ttu-id="b277e-108">Die häufigste Methode zum Hinzufügen von Anwendungen zum System besteht darin, Sie zu importieren.</span><span class="sxs-lookup"><span data-stu-id="b277e-108">The most common method for adding applications to the system is to import them.</span></span> <span data-ttu-id="b277e-109">Um auf dieses Feature zuzugreifen, klicken Sie in der Application Virtualization Server-Verwaltungskonsole mit der rechten Maustaste auf den Knoten **Anwendungen** , und wählen Sie **Anwendungen importieren**aus.</span><span class="sxs-lookup"><span data-stu-id="b277e-109">To access this feature, right-click the **Applications** node in the Application Virtualization Server Management Console and choose **Import Applications**.</span></span>

<span data-ttu-id="b277e-110">Sie können mehr als eine OSD-Datei (Open Software Descriptor) gleichzeitig importieren, oder Sie können eine Sequenzer-Projektdatei (SPRJ) importieren, die mehrere OSD-Dateien enthalten kann.</span><span class="sxs-lookup"><span data-stu-id="b277e-110">You can import more than one Open Software Descriptor (OSD) file at the same time, or you can import a Sequencer Project file (SPRJ) that can contain multiple OSD files.</span></span> <span data-ttu-id="b277e-111">Mit dieser Funktion können Sie verwandte Anwendungen ähnlich konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="b277e-111">This functionality enables you to configure related applications similarly.</span></span>

<span data-ttu-id="b277e-112">Sie können auch die folgenden Features verwenden, um Ihnen bei der Verwaltung Ihrer Anwendungen zu helfen:</span><span class="sxs-lookup"><span data-stu-id="b277e-112">You can also use the following features to help you manage your applications:</span></span>

-   <span data-ttu-id="b277e-113">**Anwendungsgruppen**– ermöglicht Ihnen, logische Gruppen von Anwendungen für vereinfachte Verwaltung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="b277e-113">**Application Groups**—Enables you to create logical groups of applications for simplified management.</span></span> <span data-ttu-id="b277e-114">Wenn Änderungen an einer Gruppe vorgenommen wurden (beispielsweise Zugriffsberechtigungen), werden die Änderungen auf alle Anwendungen in der Gruppe angewendet.</span><span class="sxs-lookup"><span data-stu-id="b277e-114">When changes are made to a group (for example, access permissions), the changes are applied to all applications in the group.</span></span> <span data-ttu-id="b277e-115">Anwendungen in einer Gruppe können aus unterschiedlichen Paketen stammen.</span><span class="sxs-lookup"><span data-stu-id="b277e-115">Applications in a group can come from different packages.</span></span>

-   <span data-ttu-id="b277e-116">**Mehrfachauswahl**– Sie können mehrere Anwendungen gleichzeitig auswählen, indem Sie die STRG-Taste gedrückt halten, wenn Sie auf eine Anwendung klicken, um die Anwendungseigenschaften zu ändern.</span><span class="sxs-lookup"><span data-stu-id="b277e-116">**Multi Select**—Enables you to select multiple applications at once by holding the CTRL key when you click an application to modify the application properties.</span></span> <span data-ttu-id="b277e-117">Wenn Sie jedoch eine Beziehung zwischen den Anwendungen aufrecht erhalten möchten, sollten Sie eine Anwendungsgruppe erstellen, in der die Anwendungen enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="b277e-117">However, if you want to maintain a relationship between the applications, you should create an application group to hold the applications.</span></span>

-   <span data-ttu-id="b277e-118">**System übergreifende Kopie**– ermöglicht das Kopieren von Anwendungen aus einer Umgebung in eine andere Umgebung, in der dieselbe Version von App-V in einem Schritt ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b277e-118">**Cross System Copy**—Enables you to copy applications from one environment to another environment that is running the same version of App-V in one step.</span></span> <span data-ttu-id="b277e-119">Angenommen, Sie verfügen über eine Testumgebung für Benutzerakzeptanz, in der Sie zunächst Anwendungen bereitstellen und konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="b277e-119">For example, you might have a user acceptance test environment where you initially deploy and configure applications.</span></span> <span data-ttu-id="b277e-120">Nachdem Sie die Testphase abgeschlossen haben, möchten Sie möglicherweise denselben Satz von Anwendungen (einschließlich Berechtigungen) in die Produktionsumgebung replizieren.</span><span class="sxs-lookup"><span data-stu-id="b277e-120">After you finish your testing phase, you might want to replicate the same set of applications (including permissions) to the production environment.</span></span>

## <span data-ttu-id="b277e-121">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="b277e-121">Related topics</span></span>


[<span data-ttu-id="b277e-122">Informationen zu Application Virtualization-Paketen</span><span class="sxs-lookup"><span data-stu-id="b277e-122">About Application Virtualization Packages</span></span>](about-application-virtualization-packages.md)

[<span data-ttu-id="b277e-123">Informationen zur Application Virtualization Server Management Console</span><span class="sxs-lookup"><span data-stu-id="b277e-123">About the Application Virtualization Server Management Console</span></span>](about-the-application-virtualization-server-management-console.md)

[<span data-ttu-id="b277e-124">So verwalten Sie Anwendungsgruppen in der Server Management Console</span><span class="sxs-lookup"><span data-stu-id="b277e-124">How to Manage Application Groups in the Server Management Console</span></span>](how-to-manage-application-groups-in-the-server-management-console.md)

[<span data-ttu-id="b277e-125">So verwalten Sie Anwendungen in der Server Management Console</span><span class="sxs-lookup"><span data-stu-id="b277e-125">How to Manage Applications in the Server Management Console</span></span>](how-to-manage-applications-in-the-server-management-console.md)

 

 





