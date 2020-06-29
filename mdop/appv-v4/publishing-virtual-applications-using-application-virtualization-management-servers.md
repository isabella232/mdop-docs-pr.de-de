---
title: Veröffentlichen von virtuellen Anwendungen mit Application Virtualization Management-Servern
description: Veröffentlichen von virtuellen Anwendungen mit Application Virtualization Management-Servern
author: dansimp
ms.assetid: f3d79284-3f82-4ca3-b741-1a80b61490da
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 01b85d73ed0a6a8bf723be381e947fbbc003bf6d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806439"
---
# <span data-ttu-id="cddcc-103">Veröffentlichen von virtuellen Anwendungen mit Application Virtualization Management-Servern</span><span class="sxs-lookup"><span data-stu-id="cddcc-103">Publishing Virtual Applications Using Application Virtualization Management Servers</span></span>


<span data-ttu-id="cddcc-104">In einer auf Application Virtualization Server basierenden Bereitstellung werden virtuelle Anwendungspakete, die sequenziert, getestet und bereitgestellt wurden, in die Hauptinhalts Freigabe kopiert, die vom Application Virtualization Management Server verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="cddcc-104">In an Application Virtualization Server-based deployment, virtual application packages that have been sequenced, tested, and found deployable are copied to the main CONTENT share to be used by the Application Virtualization Management Server.</span></span> <span data-ttu-id="cddcc-105">Nachdem die Pakete auf dem Application Virtualization-Verwaltungs Server importiert wurden, können Sie für die Endbenutzer veröffentlicht werden.</span><span class="sxs-lookup"><span data-stu-id="cddcc-105">After the packages are imported on the Application Virtualization Management Server, they can be published to the end users.</span></span>

<span data-ttu-id="cddcc-106">**Hinweis**  Die Inhaltsfreigabe sollte sich auf dem angeschlossenen Datenträgerspeicher des Servers befinden.</span><span class="sxs-lookup"><span data-stu-id="cddcc-106">**Note** The CONTENT share should be located on the server’s attached disk storage.</span></span> <span data-ttu-id="cddcc-107">Die Verwendung eines Netzwerkspeicher Geräts wie einem SAN oder einer DFS-Freigabe sollte aufgrund der Auswirkungen auf das Netzwerk sorgfältig berücksichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="cddcc-107">Using a network storage device such as a SAN or a DFS share should be considered carefully because of the network impact.</span></span>

 

<span data-ttu-id="cddcc-108">Anwendungen werden in Active Directory-Gruppen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="cddcc-108">Applications are provisioned to Active Directory groups.</span></span> <span data-ttu-id="cddcc-109">In der Regel erstellt der Application Virtualization-Administrator Active Directory-Gruppen für jede virtuelle Anwendung, die veröffentlicht werden soll, und fügt dann die entsprechenden Benutzer zu diesen Gruppen hinzu.</span><span class="sxs-lookup"><span data-stu-id="cddcc-109">Typically, the Application Virtualization administrator will create Active Directory groups for each virtual application to be published and then add the appropriate users to those groups.</span></span> <span data-ttu-id="cddcc-110">Wenn sich die Benutzer an ihren Arbeitsstationen anmelden, führt der Application Virtualization-Client standardmäßig eine Veröffentlichungsaktualisierung mithilfe der Anmeldeinformationen des angemeldeten Benutzers durch.</span><span class="sxs-lookup"><span data-stu-id="cddcc-110">When the users log on to their workstations, the Application Virtualization Client, by default, performs a publishing refresh using the credentials of the logged on user.</span></span> <span data-ttu-id="cddcc-111">Der Benutzer kann dann Anwendungen von überall aus starten, wo die Verknüpfungen gespeichert wurden.</span><span class="sxs-lookup"><span data-stu-id="cddcc-111">The user can then start applications from wherever the shortcuts have been placed.</span></span> <span data-ttu-id="cddcc-112">Der Application Virtualization-Administrator bestimmt, wo und wie viele Tastenkombinationen sich während der Sequenzierung der Anwendung auf dem Clientsystem befinden.</span><span class="sxs-lookup"><span data-stu-id="cddcc-112">The Application Virtualization administrator determines where and how many shortcuts are located on the client system during the sequencing of the application.</span></span>

<span data-ttu-id="cddcc-113">**Hinweis**  Bei einer *Veröffentlichungsaktualisierung* handelt es sich um einen Anruf an den Application Virtualization Server, der auf dem Application Virtualization-Client definiert ist, um zu ermitteln, welche virtuellen Anwendungsverknüpfungen für die Verwendung durch den Endbenutzer an den Client gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="cddcc-113">**Note** A *publishing refresh* is a call to the Application Virtualization Server that is defined on the Application Virtualization Client, to determine which virtual application shortcuts are sent to the client for use by the end user.</span></span>

 

## <span data-ttu-id="cddcc-114">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="cddcc-114">Related topics</span></span>


[<span data-ttu-id="cddcc-115">Application Virtualization Server-basiertes Szenario</span><span class="sxs-lookup"><span data-stu-id="cddcc-115">Application Virtualization Server-Based Scenario</span></span>](application-virtualization-server-based-scenario.md)

[<span data-ttu-id="cddcc-116">So veröffentlichen Sie eine virtuelle Anwendung auf dem Client</span><span class="sxs-lookup"><span data-stu-id="cddcc-116">How to Publish a Virtual Application on the Client</span></span>](how-to-publish-a-virtual-application-on-the-client.md)

[<span data-ttu-id="cddcc-117">Übersicht über die Application Virtualization-Systemkomponenten</span><span class="sxs-lookup"><span data-stu-id="cddcc-117">Overview of the Application Virtualization System Components</span></span>](overview-of-the-application-virtualization-system-components.md)

[<span data-ttu-id="cddcc-118">Planen Ihrer Streaming-Lösung in einer Anwendung Virtualisierung Server-basierten-Implementierung</span><span class="sxs-lookup"><span data-stu-id="cddcc-118">Planning Your Streaming Solution in an Application Virtualization Server-Based Implementation</span></span>](planning-your-streaming-solution-in-an-application-virtualization-server-based-implementation.md)

 

 





