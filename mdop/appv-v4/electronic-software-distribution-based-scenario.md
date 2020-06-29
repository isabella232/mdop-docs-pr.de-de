---
title: Electronic Software Distribution-basiertes Szenario
description: Electronic Software Distribution-basiertes Szenario
author: dansimp
ms.assetid: 18be0f8d-60ee-449b-aa83-93c86d1a908e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 52b9a30f2b1d403ec41090252f331a984225fd19
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808848"
---
# <span data-ttu-id="4b9ef-103">Electronic Software Distribution-basiertes Szenario</span><span class="sxs-lookup"><span data-stu-id="4b9ef-103">Electronic Software Distribution-Based Scenario</span></span>


<span data-ttu-id="4b9ef-104">Wenn Sie ein ESD-Bereitstellungsszenario (Electronic Software Distribution) für Ihre Microsoft Application Virtualization-Umgebung verwenden möchten, ist es wichtig, die Faktoren zu verstehen, die in diese Entscheidung eingehen und davon betroffen sind.</span><span class="sxs-lookup"><span data-stu-id="4b9ef-104">If you plan to use an electronic software distribution (ESD) deployment scenario for your Microsoft Application Virtualization environment, it is important to understand the factors that go into and are affected by that decision.</span></span> <span data-ttu-id="4b9ef-105">In den Themen in diesem Abschnitt wird das ESD-Szenario beschrieben, und es werden Informationen zu Paketübermittlungsmethoden, Übertragungsprotokollen und externen Komponenten bereitgestellt, die Sie in ihrer Bereitstellungsstrategie in Frage stellen müssen.</span><span class="sxs-lookup"><span data-stu-id="4b9ef-105">The topics in this section describe the ESD scenario and provide information about package delivery methods, transmission protocols, and external components that you will need to consider in your deployment strategy.</span></span> <span data-ttu-id="4b9ef-106">Sie können auch die in diesem Abschnitt beschriebenen Verfahren verwenden, um Ihre Bereitstellung von der Server Konfigurationsphase bis zur Bereitstellungs Überprüfungsphase abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="4b9ef-106">You can also use the procedures in this section to complete your deployment, from the server configuration phase through the deployment verification phase.</span></span>

## <span data-ttu-id="4b9ef-107">Inhalt dieses Abschnitts</span><span class="sxs-lookup"><span data-stu-id="4b9ef-107">In This Section</span></span>


<a href="" id="electronic-software-distribution-based-scenario-overview"></a>[<span data-ttu-id="4b9ef-108">Übersicht über Electronic Software Distribution-basierte Szenarien</span><span class="sxs-lookup"><span data-stu-id="4b9ef-108">Electronic Software Distribution-Based Scenario Overview</span></span>](electronic-software-distribution-based-scenario-overview.md)  
<span data-ttu-id="4b9ef-109">Enthält wichtige Informationen zu den Veröffentlichungs-und Streaming-Methoden, die Sie für eine ESD-basierte Bereitstellung verwenden können.</span><span class="sxs-lookup"><span data-stu-id="4b9ef-109">Provides important information about the publishing and streaming methods you can use for an ESD-based deployment.</span></span>

<a href="" id="how-to-configure-servers-for-esd-based-deployment"></a>[<span data-ttu-id="4b9ef-110">So konfigurieren Sie Servern für die ESD-basierte Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="4b9ef-110">How to Configure Servers for ESD-Based Deployment</span></span>](how-to-configure-servers-for-esd-based-deployment.md)  
<span data-ttu-id="4b9ef-111">Dieser Abschnitt enthält Verfahren, mit denen Sie die Application Virtualization-Streamingserver, den IIS-Server und den Dateiserver für Ihre Software Verteilungs basierte Bereitstellungsstrategie konfigurieren können.</span><span class="sxs-lookup"><span data-stu-id="4b9ef-111">This section provides procedures you can use to configure the Application Virtualization Streaming Servers, the IIS server, and the file server for your electronic software distribution–based deployment strategy.</span></span>

<a href="" id="how-to-install-the-client-by-using-the-command-line"></a>[<span data-ttu-id="4b9ef-112">So installieren Sie den Client über die Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="4b9ef-112">How to Install the Client by Using the Command Line</span></span>](how-to-install-the-client-by-using-the-command-line-new.md)  
<span data-ttu-id="4b9ef-113">Enthält Befehlszeilenverfahren zum Installieren des Application Virtualization-Clients mithilfe der setup.exe-oder setup.msi-Datei.</span><span class="sxs-lookup"><span data-stu-id="4b9ef-113">Provides command-line procedures for installing the Application Virtualization Client, using either the setup.exe or the setup.msi file.</span></span>

<a href="" id="how-to-uninstall-the-app-v-client"></a>[<span data-ttu-id="4b9ef-114">So deinstallieren Sie App-V Client</span><span class="sxs-lookup"><span data-stu-id="4b9ef-114">How to Uninstall the App-V Client</span></span>](how-to-uninstall-the-app-v-client.md)  
<span data-ttu-id="4b9ef-115">Bietet ein schrittweises Verfahren, mit dem Sie überprüfen können, ob der Application Virtualization-Client installiert wurde und ordnungsgemäß funktioniert.</span><span class="sxs-lookup"><span data-stu-id="4b9ef-115">Provides a step-by-step procedure you can use to confirm that the Application Virtualization Client has been installed and is functioning correctly.</span></span>

<a href="" id="how-to-publish-a-virtual-application-on-the-client"></a>[<span data-ttu-id="4b9ef-116">So veröffentlichen Sie eine virtuelle Anwendung auf dem Client</span><span class="sxs-lookup"><span data-stu-id="4b9ef-116">How to Publish a Virtual Application on the Client</span></span>](how-to-publish-a-virtual-application-on-the-client.md)  
<span data-ttu-id="4b9ef-117">Bietet Befehlszeilenverfahren für die Veröffentlichung eines Anwendungspakets mit Windows Installer oder SFTMIME.</span><span class="sxs-lookup"><span data-stu-id="4b9ef-117">Provides command-line procedures for publishing an application package, using either Windows Installer or SFTMIME.</span></span>

## <span data-ttu-id="4b9ef-118">Verweis</span><span class="sxs-lookup"><span data-stu-id="4b9ef-118">Reference</span></span>


[<span data-ttu-id="4b9ef-119">Befehlszeilenparameter von Application Virtualization Client Installer</span><span class="sxs-lookup"><span data-stu-id="4b9ef-119">Application Virtualization Client Installer Command-Line Parameters</span></span>](application-virtualization-client-installer-command-line-parameters.md)

## <span data-ttu-id="4b9ef-120">Verwandte Abschnitte</span><span class="sxs-lookup"><span data-stu-id="4b9ef-120">Related Sections</span></span>


[<span data-ttu-id="4b9ef-121">Application Virtualization Server-basiertes Szenario</span><span class="sxs-lookup"><span data-stu-id="4b9ef-121">Application Virtualization Server-Based Scenario</span></span>](application-virtualization-server-based-scenario.md)

## <span data-ttu-id="4b9ef-122">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="4b9ef-122">Related topics</span></span>


[<span data-ttu-id="4b9ef-123">Bereitstellung von Application Virtualization und Upgrade Aspekte</span><span class="sxs-lookup"><span data-stu-id="4b9ef-123">Application Virtualization Deployment and Upgrade Considerations</span></span>](application-virtualization-deployment-and-upgrade-considerations.md)

[<span data-ttu-id="4b9ef-124">Szenario für die eigenständige Bereitstellung für Application Virtualization Clients</span><span class="sxs-lookup"><span data-stu-id="4b9ef-124">Stand-Alone Delivery Scenario for Application Virtualization Clients</span></span>](stand-alone-delivery-scenario-for-application-virtualization-clients.md)

 

 





