---
title: Bereitstellung von Application Virtualization und Upgrade Aspekte
description: Bereitstellung von Application Virtualization und Upgrade Aspekte
author: dansimp
ms.assetid: adc562ee-7276-4b14-b10a-da17f05e1682
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: dd9e6c1a624b9da18bba75c5f3816a8e9c5391a8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809238"
---
# <span data-ttu-id="785a6-103">Bereitstellung von Application Virtualization und Upgrade Aspekte</span><span class="sxs-lookup"><span data-stu-id="785a6-103">Application Virtualization Deployment and Upgrade Considerations</span></span>


<span data-ttu-id="785a6-104">Bevor Sie mit der Bereitstellung von Microsoft Application Virtualization beginnen, müssen Sie möglicherweise Ihre Umgebungsanforderungen überprüfen, einschließlich der Hardware-und Softwareanforderungen für die Installation der verschiedenen Application Virtualization-Komponenten.</span><span class="sxs-lookup"><span data-stu-id="785a6-104">Before you begin the deployment of Microsoft Application Virtualization, you might need to review your environment requirements, including the hardware and software requirements for installing the various Application Virtualization components.</span></span> <span data-ttu-id="785a6-105">Wenn Sie ein Upgrade von einer früheren Version durchführen, finden Sie in den Themen dieses Abschnittsinformationen zum Aktualisieren Ihrer aktuellen Sequenzer-, Server-und Clientversionen.</span><span class="sxs-lookup"><span data-stu-id="785a6-105">Also, if you are upgrading from a previous version, the topics in this section provide information about upgrading your current Sequencer, server, and client versions.</span></span>

## <span data-ttu-id="785a6-106">Inhalt dieses Abschnitts</span><span class="sxs-lookup"><span data-stu-id="785a6-106">In This Section</span></span>


<a href="" id="application-virtualization-deployment-requirements"></a>[<span data-ttu-id="785a6-107">Bereitstellungsanforderungen für Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="785a6-107">Application Virtualization Deployment Requirements</span></span>](application-virtualization-deployment-requirements.md)  
<span data-ttu-id="785a6-108">Enthält allgemeine Informationen zu den Systemanforderungen und zu den Upgrade Überlegungen für Ihre Application Virtualization-Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="785a6-108">Provides general information about system requirements and upgrade considerations for your Application Virtualization deployment.</span></span>

<a href="" id="how-to-upgrade-the-application-virtualization-client"></a>[<span data-ttu-id="785a6-109">So aktualisieren Sie Application Virtualization Client</span><span class="sxs-lookup"><span data-stu-id="785a6-109">How to Upgrade the Application Virtualization Client</span></span>](how-to-upgrade-the-application-virtualization-client.md)  
<span data-ttu-id="785a6-110">Bietet Schritt-für-Schritt-Verfahren für das Upgrade des Application Virtualization-Desktop Clients oder des Application Virtualization-Clients für Remote Desktop Dienste (vormals Terminal Dienste).</span><span class="sxs-lookup"><span data-stu-id="785a6-110">Provides step-by-step procedures for upgrading the Application Virtualization Desktop Client or the Application Virtualization Client for Remote Desktop Services (formerly Terminal Services).</span></span>

<a href="" id="how-to-upgrade-the-servers-and-system-components"></a>[<span data-ttu-id="785a6-111">So aktualisieren Sie die Server und Systemkomponenten</span><span class="sxs-lookup"><span data-stu-id="785a6-111">How to Upgrade the Servers and System Components</span></span>](how-to-upgrade-the-servers-and-system-components.md)  
<span data-ttu-id="785a6-112">Bietet ein schrittweises Verfahren, mit dem Sie die Softwarekomponenten aktualisieren können, die auf allen Application Virtualization System-Computern installiert sind.</span><span class="sxs-lookup"><span data-stu-id="785a6-112">Provides a step-by-step procedure you can use to upgrade the software components installed on all Application Virtualization System computers.</span></span>

<a href="" id="how-to-upgrade-the-application-virtualization-sequencer"></a>[<span data-ttu-id="785a6-113">So aktualisieren Sie Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="785a6-113">How to Upgrade the Application Virtualization Sequencer</span></span>](how-to-upgrade-the-application-virtualization-sequencer.md)  
<span data-ttu-id="785a6-114">Bietet Schritt-für-Schritt-Verfahren zum Aktualisieren des Sequencers auf Computern unter Windows Vista oder WindowsXP.</span><span class="sxs-lookup"><span data-stu-id="785a6-114">Provides step-by-step procedures for upgrading the Sequencer on computers running Windows Vista or WindowsXP.</span></span>

<a href="" id="how-to-install-the-application-virtualization-sequencer"></a>[<span data-ttu-id="785a6-115">So installieren Sie Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="785a6-115">How to Install the Application Virtualization Sequencer</span></span>](how-to-install-the-application-virtualization-sequencer.md)  
<span data-ttu-id="785a6-116">Bietet eine schrittweise Anleitung zum Installieren des Sequencers.</span><span class="sxs-lookup"><span data-stu-id="785a6-116">Provides a step-by-step procedure for installing the Sequencer.</span></span>

## <span data-ttu-id="785a6-117">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="785a6-117">Related topics</span></span>


[<span data-ttu-id="785a6-118">Application Virtualization-Referenz</span><span class="sxs-lookup"><span data-stu-id="785a6-118">Application Virtualization Reference</span></span>](application-virtualization-reference.md)

[<span data-ttu-id="785a6-119">Application Virtualization Server-basiertes Szenario</span><span class="sxs-lookup"><span data-stu-id="785a6-119">Application Virtualization Server-Based Scenario</span></span>](application-virtualization-server-based-scenario.md)

[<span data-ttu-id="785a6-120">Electronic Software Distribution-basiertes Szenario</span><span class="sxs-lookup"><span data-stu-id="785a6-120">Electronic Software Distribution-Based Scenario</span></span>](electronic-software-distribution-based-scenario.md)

[<span data-ttu-id="785a6-121">Szenario für die eigenständige Bereitstellung für Application Virtualization Clients</span><span class="sxs-lookup"><span data-stu-id="785a6-121">Stand-Alone Delivery Scenario for Application Virtualization Clients</span></span>](stand-alone-delivery-scenario-for-application-virtualization-clients.md)

 

 





