---
title: Leitfaden zur Planung und Bereitstellung für das Application Virtualization System
description: Leitfaden zur Planung und Bereitstellung für das Application Virtualization System
author: dansimp
ms.assetid: 6c012e33-9ac6-4cd8-84ff-54f40973833f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 10bcac26fddae2f0e5826dbd7335adda06d3987e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806515"
---
# <span data-ttu-id="9360e-103">Leitfaden zur Planung und Bereitstellung für das Application Virtualization System</span><span class="sxs-lookup"><span data-stu-id="9360e-103">Planning and Deployment Guide for the Application Virtualization System</span></span>


<span data-ttu-id="9360e-104">Microsoft Application Virtualization Management bietet die Möglichkeit, Anwendungen für Endbenutzercomputer verfügbar zu machen, ohne die Anwendungen direkt auf diesen Computern installieren zu müssen.</span><span class="sxs-lookup"><span data-stu-id="9360e-104">Microsoft Application Virtualization Management provides the capability to make applications available to end user computers without having to install the applications directly on those computers.</span></span> <span data-ttu-id="9360e-105">Dies wird durch einen Prozess ermöglicht, der als *Sequenzierung der Anwendung*bezeichnet wird, wodurch jede Anwendung in ihrer eigenen, eigenständigen virtuellen Umgebung auf dem Clientcomputer ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="9360e-105">This is made possible through a process known as *sequencing the application*, which enables each application to run in its own self-contained virtual environment on the client computer.</span></span> <span data-ttu-id="9360e-106">Die sequenzierten Anwendungen werden voneinander isoliert, wodurch Anwendungskonflikte eliminiert werden, Sie können jedoch weiterhin mit dem Clientcomputer interagieren.</span><span class="sxs-lookup"><span data-stu-id="9360e-106">The sequenced applications are isolated from one another, eliminating application conflicts, yet can still interact with the client computer.</span></span>

<span data-ttu-id="9360e-107">Application Virtualization Client ist die Komponente Application Virtualization System, die es dem Endbenutzer ermöglicht, mit den Anwendungen zu interagieren, nachdem Sie auf dem Computer veröffentlicht wurden.</span><span class="sxs-lookup"><span data-stu-id="9360e-107">The Application Virtualization Client is the Application Virtualization system component that enables the end user to interact with the applications after they have been published to the computer.</span></span> <span data-ttu-id="9360e-108">Der Client verwaltet die virtuelle Umgebung, in der die virtualisierten Anwendungen auf jedem Computer ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="9360e-108">The client manages the virtual environment in which the virtualized applications run on each computer.</span></span> <span data-ttu-id="9360e-109">Nachdem der Client auf einem Computer installiert wurde, müssen die Anwendungen dem Computer über einen als " *Publishing*" bezeichneten Prozess zur Verfügung gestellt werden, mit dem der Endbenutzer die virtuellen Anwendungen ausführen kann.</span><span class="sxs-lookup"><span data-stu-id="9360e-109">After the client has been installed on a computer, the applications must be made available to the computer through a process known as *publishing*, which enables the end user to run the virtual applications.</span></span> <span data-ttu-id="9360e-110">Der Veröffentlichungsprozess platziert die Symbole und Tastenkombinationen für die virtuelle Anwendung auf dem Computer – normalerweise auf dem Windows-Desktop oder im **Startmenü** – und platziert auch die Zuordnungsinformationen für die Paketdefinition und die Dateitypzuordnung auf dem Computer.</span><span class="sxs-lookup"><span data-stu-id="9360e-110">The publishing process places the virtual application icons and shortcuts on the computer—typically on the Windows desktop or on the **Start** menu—and also places the package definition and file type association information on the computer.</span></span> <span data-ttu-id="9360e-111">Durch die Veröffentlichung wird der Inhalt des Anwendungspakets auch dem Computer des Endbenutzers zur Verfügung gestellt.</span><span class="sxs-lookup"><span data-stu-id="9360e-111">Publishing also makes the application package content available to the end user’s computer.</span></span>

<span data-ttu-id="9360e-112">Der Inhalt des virtuellen Anwendungspakets kann auf einem oder mehreren Application Virtualization-Servern gespeichert werden, damit er bei Bedarf auf die Clients gestreamt und lokal zwischengespeichert werden kann.</span><span class="sxs-lookup"><span data-stu-id="9360e-112">The virtual application package content can be placed on one or more Application Virtualization servers so that it can be streamed down to the clients on demand and cached locally.</span></span> <span data-ttu-id="9360e-113">Dateiserver und Webserver können auch als Streamingserver verwendet werden, oder die Inhalte können direkt auf dem Computer des Endbenutzers abgelegt werden, beispielsweise wenn Sie ein elektronisches Softwareverteilungssystem wie Microsoft Endpoint Configuration Manager verwenden.</span><span class="sxs-lookup"><span data-stu-id="9360e-113">File servers and Web servers can also be used as streaming servers, or the content can be placed directly on the end user’s computer—for example, if you are using an electronic software distribution system, such as Microsoft Endpoint Configuration Manager.</span></span> <span data-ttu-id="9360e-114">Bei einer Multi-Server-Implementierung erfordert die Beibehaltung des Paketinhalts und die Aktualität auf allen Streaming-Servern eine umfassende Paketverwaltungslösung.</span><span class="sxs-lookup"><span data-stu-id="9360e-114">In a multi-server implementation, maintaining the package content and keeping it up to date on all the streaming servers requires a comprehensive package management solution.</span></span> <span data-ttu-id="9360e-115">Je nach Größe Ihrer Organisation müssen Sie möglicherweise viele virtuelle Anwendungen für Endbenutzer zugänglich machen, die sich auf der ganzen Welt befinden.</span><span class="sxs-lookup"><span data-stu-id="9360e-115">Depending on the size of your organization, you might need to have many virtual applications accessible to end users located all over the world.</span></span> <span data-ttu-id="9360e-116">Die Verwaltung der Pakete, um sicherzustellen, dass die richtigen Anwendungen allen Benutzern zur Verfügung stehen, wenn Sie Zugriff darauf benötigen, ist daher eine Grundvoraussetzung.</span><span class="sxs-lookup"><span data-stu-id="9360e-116">Managing the packages to ensure that the right applications are available to all users where and when they need access to them is therefore an essential requirement.</span></span>

<span data-ttu-id="9360e-117">Der Leitfaden zur Planung und Bereitstellung von Application Virtualization bietet Informationen, die Ihnen helfen, die Microsoft Application Virtualization-Anwendung und ihre Komponenten besser zu verstehen und bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="9360e-117">The Application Virtualization Planning and Deployment Guide provides information to help you better understand and deploy the Microsoft Application Virtualization application and its components.</span></span> <span data-ttu-id="9360e-118">Darüber hinaus finden Sie schrittweise Anleitungen zum Implementieren der wichtigsten Bereitstellungsszenarien.</span><span class="sxs-lookup"><span data-stu-id="9360e-118">It also provides step-by-step procedures for implementing the key deployment scenarios.</span></span>

## <span data-ttu-id="9360e-119">Inhalt dieses Abschnitts</span><span class="sxs-lookup"><span data-stu-id="9360e-119">In This Section</span></span>


<a href="" id="planning-for-application-virtualization-system-deployment"></a>[<span data-ttu-id="9360e-120">Planen der Bereitstellung von Application Virtualization System</span><span class="sxs-lookup"><span data-stu-id="9360e-120">Planning for Application Virtualization System Deployment</span></span>](planning-for-application-virtualization-system-deployment.md)  
<span data-ttu-id="9360e-121">Bietet die erforderlichen Anleitungen für die Planung der Implementierung und Bereitstellung Ihres Application Virtualization-Systems.</span><span class="sxs-lookup"><span data-stu-id="9360e-121">Provides the guidance necessary to plan the implementation and deployment of your Application Virtualization system.</span></span>

<a href="" id="application-virtualization-deployment-and-upgrade-considerations"></a>[<span data-ttu-id="9360e-122">Bereitstellung von Application Virtualization und Upgrade Aspekte</span><span class="sxs-lookup"><span data-stu-id="9360e-122">Application Virtualization Deployment and Upgrade Considerations</span></span>](application-virtualization-deployment-and-upgrade-considerations.md)  
<span data-ttu-id="9360e-123">Enthält Informationen zu den Hardware-und Softwareanforderungen für die Installation der verschiedenen Application Virtualization-Komponenten sowie Informationen zum Upgrade.</span><span class="sxs-lookup"><span data-stu-id="9360e-123">Provides information about hardware and software requirements for installing the various Application Virtualization components, as well as upgrade information.</span></span>

<a href="" id="electronic-software-distribution-based-scenario"></a>[<span data-ttu-id="9360e-124">Electronic Software Distribution-basiertes Szenario</span><span class="sxs-lookup"><span data-stu-id="9360e-124">Electronic Software Distribution-Based Scenario</span></span>](electronic-software-distribution-based-scenario.md)  
<span data-ttu-id="9360e-125">Enthält Informationen zum Bereitstellen von Application Virtualization mithilfe eines ESD-Systems (Electronic Software Distribution).</span><span class="sxs-lookup"><span data-stu-id="9360e-125">Provides information about deploying Application Virtualization using an electronic software distribution (ESD) system.</span></span>

<a href="" id="application-virtualization-server-based-scenario"></a>[<span data-ttu-id="9360e-126">Application Virtualization Server-basiertes Szenario</span><span class="sxs-lookup"><span data-stu-id="9360e-126">Application Virtualization Server-Based Scenario</span></span>](application-virtualization-server-based-scenario.md)  
<span data-ttu-id="9360e-127">Enthält Informationen zum Bereitstellen von Application Virtualization mithilfe des Application Virtualization Management-Servers.</span><span class="sxs-lookup"><span data-stu-id="9360e-127">Provides information about deploying Application Virtualization using the Application Virtualization Management Server.</span></span>

<a href="" id="stand-alone-delivery-scenario-for-application-virtualization-clients"></a>[<span data-ttu-id="9360e-128">Szenario für die eigenständige Bereitstellung für Application Virtualization Clients</span><span class="sxs-lookup"><span data-stu-id="9360e-128">Stand-Alone Delivery Scenario for Application Virtualization Clients</span></span>](stand-alone-delivery-scenario-for-application-virtualization-clients.md)  
<span data-ttu-id="9360e-129">Beschreibt, wie Application Virtualization in einem eigenständigen Modus ohne Verwendung von ESD-oder Server basierten Ressourcen bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="9360e-129">Describes how to deploy Application Virtualization in a stand-alone mode, without the use of ESD or server-based resources.</span></span>

<a href="" id="application-virtualization-reference"></a>[<span data-ttu-id="9360e-130">Application Virtualization-Referenz</span><span class="sxs-lookup"><span data-stu-id="9360e-130">Application Virtualization Reference</span></span>](application-virtualization-reference.md)  
<span data-ttu-id="9360e-131">Enthält detailliertes technisches Referenzmaterial zum Installieren und Verwalten von Systemkomponenten.</span><span class="sxs-lookup"><span data-stu-id="9360e-131">Contains detailed technical reference material related to installing and managing system components.</span></span>

 

 




