---
title: Application Virtualization Server-basiertes Szenario
description: Application Virtualization Server-basiertes Szenario
author: dansimp
ms.assetid: 10ed0b18-087d-470f-951b-5083f4cb076f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d6699bdc734258f67e4938e33266a2f061531939
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807943"
---
# <span data-ttu-id="eeecf-103">Application Virtualization Server-basiertes Szenario</span><span class="sxs-lookup"><span data-stu-id="eeecf-103">Application Virtualization Server-Based Scenario</span></span>


<span data-ttu-id="eeecf-104">Wenn Sie ein serverbasiertes Bereitstellungsszenario für Ihre Microsoft Application Virtualization (App-V)-Umgebung verwenden möchten, sollten Sie die Unterschiede zwischen dem Application Virtualization Management-Server und dem Application Virtualization Streaming Server verstehen.</span><span class="sxs-lookup"><span data-stu-id="eeecf-104">If you plan to use a server-based deployment scenario for your Microsoft Application Virtualization (App-V) environment, you should understand the differences between the Application Virtualization Management Server and the Application Virtualization Streaming Server.</span></span> <span data-ttu-id="eeecf-105">In den Themen in diesem Abschnitt werden diese Unterschiede beschrieben und außerdem Informationen zu Paketübermittlungsmethoden, Übertragungsprotokollen und externen Komponenten bereitgestellt, die Sie beim Fortsetzen der Bereitstellung Bedenken müssen.</span><span class="sxs-lookup"><span data-stu-id="eeecf-105">The topics in this section describe those differences and also provide information about package delivery methods, transmission protocols, and external components that you have to consider as you continue with your deployment.</span></span> <span data-ttu-id="eeecf-106">Dieser Abschnitt enthält auch Schritt-für-Schritt-Verfahren zum Installieren und Konfigurieren des App-V-Verwaltungsservers und von Application Virtualization-Streaming Servern.</span><span class="sxs-lookup"><span data-stu-id="eeecf-106">This section also provides step-by-step procedures for installing and configuring the App-V Management Server and the Application Virtualization Streaming Servers.</span></span>

## <span data-ttu-id="eeecf-107">Inhalt dieses Abschnitts</span><span class="sxs-lookup"><span data-stu-id="eeecf-107">In This Section</span></span>


<a href="" id="application-virtualization-server-based-scenario-overview"></a>[<span data-ttu-id="eeecf-108">Übersicht über Application Virtualization Server-basierte Szenarien</span><span class="sxs-lookup"><span data-stu-id="eeecf-108">Application Virtualization Server-Based Scenario Overview</span></span>](application-virtualization-server-based-scenario-overview.md)  
<span data-ttu-id="eeecf-109">Enthält wichtige Bereitstellungsinformationen zu Application Virtualization Management Server, dem Application Virtualization Streaming Server und den Paketübermittlungsmethoden,-Protokollen und externen Komponenten, die für Ihren Server basierten Bereitstellungsplan relevant sind.</span><span class="sxs-lookup"><span data-stu-id="eeecf-109">Provides important deployment information about the Application Virtualization Management Server, the Application Virtualization Streaming Server, and the package delivery methods, protocols, and external components relevant to your server-based deployment plan.</span></span>

<a href="" id="how-to-install-the-servers-and-system-components"></a>[<span data-ttu-id="eeecf-110">So installieren Sie die Server und Systemkomponenten</span><span class="sxs-lookup"><span data-stu-id="eeecf-110">How to Install the Servers and System Components</span></span>](how-to-install-the-servers-and-system-components.md)  
<span data-ttu-id="eeecf-111">Beschreibt, wie die Microsoft Application Virtualization Platform-Komponenten installiert werden, die für Ihre serverbasierte Bereitstellung erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="eeecf-111">Describes how to install the Microsoft Application Virtualization platform components required for your server-based deployment.</span></span>

<a href="" id="how-to-configure-servers-for-server-based-deployment"></a>[<span data-ttu-id="eeecf-112">So konfigurieren Sie Server für die serverbasierte Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="eeecf-112">How to Configure Servers for Server-Based Deployment</span></span>](how-to-configure-servers-for-server-based-deployment.md)  
<span data-ttu-id="eeecf-113">Beschreibt, wie Sie den Application Virtualization-Verwaltungsserver, den Application Virtualization Streaming Server, den IIS-Server (Internet Information Integration) und den Dateiserver konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="eeecf-113">Describes how to configure the Application Virtualization Management Server, the Application Virtualization Streaming Server, the Internet Information Integration (IIS) server, and the file server.</span></span>

<a href="" id="how-to-configure-a-read-only-cache-on-the-app-v-client--vdi-"></a>[<span data-ttu-id="eeecf-114">So konfigurieren Sie einen schreibgeschützten Cache für App-V Client (VDI)</span><span class="sxs-lookup"><span data-stu-id="eeecf-114">How to Configure a Read-only Cache on the App-V Client (VDI)</span></span>](how-to-configure-a-read-only-cache-on-the-app-v-client--vdi-.md)  
<span data-ttu-id="eeecf-115">Beschreibt, wie der App-V-Client für die Verwendung des schreibgeschützten Caches konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="eeecf-115">Describes how to configure the App-V client to use read-only cache.</span></span>

<a href="" id="how-to-configure-a-read-only-cache-on-the-app-v-client--rds-"></a>[<span data-ttu-id="eeecf-116">So konfigurieren Sie einen schreibgeschützten Cache für App-V Client (RDS)</span><span class="sxs-lookup"><span data-stu-id="eeecf-116">How to Configure a Read-only Cache on the App-V Client (RDS)</span></span>](how-to-configure-a-read-only-cache-on-the-app-v-client--rds--sp1.md)  
<span data-ttu-id="eeecf-117">Beschreibt, wie der App-V-Client für die Verwendung des schreibgeschützten Caches konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="eeecf-117">Describes how to configure the App-V client to use read-only cache.</span></span>

<a href="" id="how-to-configure-microsoft-sql-server-mirroring-support-for-app-v"></a>[<span data-ttu-id="eeecf-118">So konfigurieren Sie die Unterstützung von Microsoft SQL Server-Spiegelungen für App-V</span><span class="sxs-lookup"><span data-stu-id="eeecf-118">How to Configure Microsoft SQL Server Mirroring Support for App-V</span></span>](how-to-configure-microsoft-sql-server-mirroring-support-for-app-v.md)  
<span data-ttu-id="eeecf-119">Beschreibt, wie Sie die Datenbankspiegelung mithilfe von Microsoft SQL Server für Ihr App-V-System konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="eeecf-119">Describes how to configure database mirroring by using Microsoft SQL Server for your App-V system.</span></span>

## <span data-ttu-id="eeecf-120">Verweis</span><span class="sxs-lookup"><span data-stu-id="eeecf-120">Reference</span></span>


[<span data-ttu-id="eeecf-121">Befehlszeilenparameter von Application Virtualization Client Installer</span><span class="sxs-lookup"><span data-stu-id="eeecf-121">Application Virtualization Client Installer Command-Line Parameters</span></span>](application-virtualization-client-installer-command-line-parameters.md)

## <span data-ttu-id="eeecf-122">Verwandte Abschnitte</span><span class="sxs-lookup"><span data-stu-id="eeecf-122">Related Sections</span></span>


[<span data-ttu-id="eeecf-123">Electronic Software Distribution-basiertes Szenario</span><span class="sxs-lookup"><span data-stu-id="eeecf-123">Electronic Software Distribution-Based Scenario</span></span>](electronic-software-distribution-based-scenario.md)

## <span data-ttu-id="eeecf-124">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="eeecf-124">Related topics</span></span>


[<span data-ttu-id="eeecf-125">Bereitstellung von Application Virtualization und Upgrade Aspekte</span><span class="sxs-lookup"><span data-stu-id="eeecf-125">Application Virtualization Deployment and Upgrade Considerations</span></span>](application-virtualization-deployment-and-upgrade-considerations.md)

[<span data-ttu-id="eeecf-126">Szenario für die eigenständige Bereitstellung für Application Virtualization Clients</span><span class="sxs-lookup"><span data-stu-id="eeecf-126">Stand-Alone Delivery Scenario for Application Virtualization Clients</span></span>](stand-alone-delivery-scenario-for-application-virtualization-clients.md)

 

 





