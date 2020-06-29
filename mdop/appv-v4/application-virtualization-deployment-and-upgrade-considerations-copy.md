---
title: Bereitstellung von Application Virtualization und Upgrade Aspekte
description: Bereitstellung von Application Virtualization und Upgrade Aspekte
author: dansimp
ms.assetid: c3c38930-0da3-43e6-b240-945edfd00a01
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 09e6943c74c7f17b6a61bc7be4bcde925a54be56
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809256"
---
# <span data-ttu-id="1fa1b-103">Bereitstellung von Application Virtualization und Upgrade Aspekte</span><span class="sxs-lookup"><span data-stu-id="1fa1b-103">Application Virtualization Deployment and Upgrade Considerations</span></span>


<span data-ttu-id="1fa1b-104">Bevor Sie mit der Bereitstellung von Microsoft Application Virtualization (App-V) beginnen, müssen Sie möglicherweise Ihre Umgebungsanforderungen überprüfen, die die Hardware-und Softwareanforderungen für die Installation der verschiedenen Application Virtualization-Komponenten beinhalten.</span><span class="sxs-lookup"><span data-stu-id="1fa1b-104">Before you begin the deployment of Microsoft Application Virtualization (App-V), you might have to review your environment requirements that includes the hardware and software requirements for installing the various Application Virtualization components.</span></span> <span data-ttu-id="1fa1b-105">Wenn Sie ein Upgrade von einer früheren Version durchführen, finden Sie in den Themen in diesem Abschnitt Informationen dazu, wie Sie Ihre aktuellen Sequenzer-, Server-und Client Versionen aktualisieren können.</span><span class="sxs-lookup"><span data-stu-id="1fa1b-105">Also, if you are upgrading from an earlier version, the topics in this section provide information about how to upgrade your current Sequencer, Server, and Client versions.</span></span>

## <span data-ttu-id="1fa1b-106">Inhalt dieses Abschnitts</span><span class="sxs-lookup"><span data-stu-id="1fa1b-106">In This Section</span></span>


<a href="" id="application-virtualization-deployment-requirements"></a>[<span data-ttu-id="1fa1b-107">Bereitstellungsanforderungen für Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="1fa1b-107">Application Virtualization Deployment Requirements</span></span>](application-virtualization-deployment-requirements.md)  
<span data-ttu-id="1fa1b-108">Enthält allgemeine Informationen zu den Systemanforderungen und zu den Upgrade Überlegungen für Ihre Application Virtualization-Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="1fa1b-108">Provides general information about system requirements and upgrade considerations for your Application Virtualization deployment.</span></span>

<a href="" id="application-virtualization-deployment-and-upgrade-checklists"></a>[<span data-ttu-id="1fa1b-109">Bereitstellung und Upgrade von Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="1fa1b-109">Application Virtualization Deployment and Upgrade Checklists</span></span>](application-virtualization-deployment-and-upgrade-checklists.md)  
<span data-ttu-id="1fa1b-110">Enthält detaillierte Listen der Installations-und Aktualisierungsaufgaben mit Links zu den jeweiligen Verfahren.</span><span class="sxs-lookup"><span data-stu-id="1fa1b-110">Provides detailed lists of installation and upgrade tasks with links to the specific procedures.</span></span>

<a href="" id="how-to-install-the-servers-and-system-components"></a>[<span data-ttu-id="1fa1b-111">So installieren Sie die Server und Systemkomponenten</span><span class="sxs-lookup"><span data-stu-id="1fa1b-111">How to Install the Servers and System Components</span></span>](how-to-install-the-servers-and-system-components.md)  
<span data-ttu-id="1fa1b-112">Beschreibt, wie die für Ihre serverbasierte Bereitstellung erforderlichen Plattformkomponenten für Application Virtualization (App-V) installiert werden.</span><span class="sxs-lookup"><span data-stu-id="1fa1b-112">Describes how to install the Application Virtualization (App-V) platform components required for your server-based deployment.</span></span>

<a href="" id="how-to-manually-install-the-application-virtualization-client"></a>[<span data-ttu-id="1fa1b-113">So installieren Sie Application Virtualization Client manuell</span><span class="sxs-lookup"><span data-stu-id="1fa1b-113">How to Manually Install the Application Virtualization Client</span></span>](how-to-manually-install-the-application-virtualization-client.md)  
<span data-ttu-id="1fa1b-114">Beschreibt, wie die Application Virtualization-Client Software installiert wird.</span><span class="sxs-lookup"><span data-stu-id="1fa1b-114">Describes how to install the Application Virtualization Client software.</span></span>

<a href="" id="how-to-install-the-application-virtualization-sequencer"></a>[<span data-ttu-id="1fa1b-115">So installieren Sie Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="1fa1b-115">How to Install the Application Virtualization Sequencer</span></span>](how-to-install-the-application-virtualization-sequencer.md)  
<span data-ttu-id="1fa1b-116">Beschreibt, wie der Application Virtualization Sequencer installiert wird.</span><span class="sxs-lookup"><span data-stu-id="1fa1b-116">Describes how to install the Application Virtualization Sequencer.</span></span>

<a href="" id="how-to-upgrade-the-application-virtualization-client"></a>[<span data-ttu-id="1fa1b-117">So aktualisieren Sie Application Virtualization Client</span><span class="sxs-lookup"><span data-stu-id="1fa1b-117">How to Upgrade the Application Virtualization Client</span></span>](how-to-upgrade-the-application-virtualization-client.md)  
<span data-ttu-id="1fa1b-118">Beschreibt, wie der Application Virtualization-Desktop Client oder der Application Virtualization-Client für Remote Desktop Dienste (vormals Terminal Dienste) aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="1fa1b-118">Describes how to upgrade the Application Virtualization Desktop Client or the Application Virtualization Client for Remote Desktop Services (formerly Terminal Services).</span></span>

<a href="" id="how-to-upgrade-the-servers-and-system-components"></a>[<span data-ttu-id="1fa1b-119">So aktualisieren Sie die Server und Systemkomponenten</span><span class="sxs-lookup"><span data-stu-id="1fa1b-119">How to Upgrade the Servers and System Components</span></span>](how-to-upgrade-the-servers-and-system-components.md)  
<span data-ttu-id="1fa1b-120">Es wird beschrieben, wie Sie die auf allen Application Virtualization Management System-Computern installierten Softwarekomponenten aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="1fa1b-120">Describes how to upgrade the software components installed on all Application Virtualization Management System computers.</span></span>

<a href="" id="how-to-upgrade-the-application-virtualization-sequencer"></a>[<span data-ttu-id="1fa1b-121">So aktualisieren Sie Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="1fa1b-121">How to Upgrade the Application Virtualization Sequencer</span></span>](how-to-upgrade-the-application-virtualization-sequencer.md)  
<span data-ttu-id="1fa1b-122">Beschreibt, wie Sie den Sequencer auf Computern mit Windows Vista oder WindowsXP aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="1fa1b-122">Describes how to upgrade the Sequencer on computers that are running WindowsVista or WindowsXP.</span></span>

## <span data-ttu-id="1fa1b-123">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="1fa1b-123">Related topics</span></span>


[<span data-ttu-id="1fa1b-124">Application Virtualization-Referenz</span><span class="sxs-lookup"><span data-stu-id="1fa1b-124">Application Virtualization Reference</span></span>](application-virtualization-reference.md)

[<span data-ttu-id="1fa1b-125">Application Virtualization Server-basiertes Szenario</span><span class="sxs-lookup"><span data-stu-id="1fa1b-125">Application Virtualization Server-Based Scenario</span></span>](application-virtualization-server-based-scenario.md)

[<span data-ttu-id="1fa1b-126">Electronic Software Distribution-basiertes Szenario</span><span class="sxs-lookup"><span data-stu-id="1fa1b-126">Electronic Software Distribution-Based Scenario</span></span>](electronic-software-distribution-based-scenario.md)

[<span data-ttu-id="1fa1b-127">Szenario für die eigenständige Bereitstellung für Application Virtualization Clients</span><span class="sxs-lookup"><span data-stu-id="1fa1b-127">Stand-Alone Delivery Scenario for Application Virtualization Clients</span></span>](stand-alone-delivery-scenario-for-application-virtualization-clients.md)

 

 





