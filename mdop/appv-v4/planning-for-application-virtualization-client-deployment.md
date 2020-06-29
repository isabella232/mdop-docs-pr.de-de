---
title: Planen der Bereitstellung von Application Virtualization Client
description: Planen der Bereitstellung von Application Virtualization Client
author: dansimp
ms.assetid: a352f80f-f0f9-4fbf-ac10-24c510b2d6be
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6c9fc4f29020af83a8606827015947e78761f4d7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806512"
---
# <span data-ttu-id="311ff-103">Planen der Bereitstellung von Application Virtualization Client</span><span class="sxs-lookup"><span data-stu-id="311ff-103">Planning for Application Virtualization Client Deployment</span></span>


<span data-ttu-id="311ff-104">Nachdem Sie entschieden haben, wie Sie virtuelle Anwendungspakete auf Ihren Endbenutzercomputern veröffentlichen und bereitstellen, sollten Sie die Bereitstellung der Application Virtualization-Client Software planen.</span><span class="sxs-lookup"><span data-stu-id="311ff-104">After you have decided how you will publish and deploy virtual application packages to your end user computers, you should plan the deployment of the Application Virtualization Client software.</span></span>

<span data-ttu-id="311ff-105">Application Virtualization Client ist die Komponente, in der die virtuellen Anwendungen tatsächlich ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="311ff-105">The Application Virtualization Client is the component that actually runs the virtual applications.</span></span> <span data-ttu-id="311ff-106">Der Application Virtualization-Client ermöglicht Benutzern die Interaktion mit Symbolen und das Doppelklicken auf Dateitypen, um eine virtuelle Anwendung zu starten.</span><span class="sxs-lookup"><span data-stu-id="311ff-106">The Application Virtualization Client enables users to interact with icons and to double-click file types to start a virtual application.</span></span> <span data-ttu-id="311ff-107">Darüber hinaus wird das Streaming der Anwendungsinhalte von einem Streamingserver verarbeitet und zwischengespeichert, bevor die Anwendung gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="311ff-107">It also handles streaming of the application content from a streaming server and caches it before starting the application.</span></span> <span data-ttu-id="311ff-108">Der Anwendungsinhalt ist so strukturiert, dass der gesamte Inhalt, der zum Starten der Anwendung und zur Behandlung der anfänglichen Benutzerinteraktion benötigt wird, zuerst an den Endbenutzercomputer gestreamt wird.</span><span class="sxs-lookup"><span data-stu-id="311ff-108">The application content is structured such that all the content needed to start the application and handle initial user interaction is streamed to the end user computer first.</span></span> <span data-ttu-id="311ff-109">Es gibt zwei verschiedene Arten von Application Virtualization-Client Software: den Application Virtualization Client für Remotedesktopdienste (ehemals Terminal Dienste), der auf Server Systemen für den Remote Desktop-Sitzungshost (RDSession-Host) und dem Application Virtualization-Desktop Client verwendet wird, der für alle anderen Computer verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="311ff-109">There are two different types of Application Virtualization Client software: the Application Virtualization Client for Remote Desktop Services (formerly Terminal Services), which is used on Remote Desktop Session Host (RDSession Host) server systems, and the Application Virtualization Desktop Client, which is used for all other computers.</span></span>

<span data-ttu-id="311ff-110">Der Application Virtualization-Client sollte zur Installationszeit entweder in der Application Virtualization-Verwaltungskonsole oder über die Befehlszeile des Installationsprogramms mit einer Reihe wichtiger Einstellungen konfiguriert werden, einschließlich der folgenden:</span><span class="sxs-lookup"><span data-stu-id="311ff-110">The Application Virtualization Client should be configured at installation time, either in the Application Virtualization Management Console or via the installer command line, with a number of important settings, including the following:</span></span>

-   <span data-ttu-id="311ff-111">Speicherorte der Symbole für alle Anwendungen</span><span class="sxs-lookup"><span data-stu-id="311ff-111">Locations of the icons for all the applications.</span></span>

-   <span data-ttu-id="311ff-112">Der Speicherort der OSD-Datei, die die Paketdefinitionsinformationen enthält.</span><span class="sxs-lookup"><span data-stu-id="311ff-112">The location of the OSD file that contains the package definition information.</span></span>

-   <span data-ttu-id="311ff-113">Die Inhaltsquelle der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="311ff-113">The application content source.</span></span>

-   <span data-ttu-id="311ff-114">Das Kommunikationsprotokoll, das beim Abrufen der vorhergehenden Elemente verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="311ff-114">The communications protocol to be used when retrieving the preceding items.</span></span>

-   <span data-ttu-id="311ff-115">Die zu verwendende Cachegröße und-Verwaltungsmethode.</span><span class="sxs-lookup"><span data-stu-id="311ff-115">The cache size and cache size management method to be used.</span></span>

<span data-ttu-id="311ff-116">Um die Bereitstellung der Application Virtualization-Client Software zu beschleunigen, wenn Sie eine ESD-Lösung (Electronic Software Distribution) verwenden, müssen die vorhergehenden Einstellungen im Voraus sorgfältig definiert werden.</span><span class="sxs-lookup"><span data-stu-id="311ff-116">To expedite the deployment of the Application Virtualization Client software when using an electronic software distribution (ESD) solution, the preceding settings must be defined carefully in advance.</span></span> <span data-ttu-id="311ff-117">Dies ist besonders wichtig, wenn Sie Computer in verschiedenen Niederlassungen haben, deren Clients für die Verwendung unterschiedlicher Quellspeicherorte konfiguriert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="311ff-117">This is especially important when you have computers in different offices, where their clients would need to be configured to use different source locations.</span></span>

**<span data-ttu-id="311ff-118">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="311ff-118">Note</span></span>**  
-   <span data-ttu-id="311ff-119">Die Werte für Symbolposition und OSD-Datei sind ein wichtiger Faktor, der bei der Auswahl der Veröffentlichungsmethode berücksichtigt werden muss, egal, ob Sie Windows Installer oder SFTMIME verwenden.</span><span class="sxs-lookup"><span data-stu-id="311ff-119">The icon location and OSD file values are an important factor to consider when choosing your publishing method, whether using Windows Installer or SFTMIME.</span></span> <span data-ttu-id="311ff-120">Die Einstellung für die Inhaltsquelle der Anwendung wird durch Ihre Wahl der Streaming-Methode definiert.</span><span class="sxs-lookup"><span data-stu-id="311ff-120">The setting for the application content source is defined by your choice of streaming method.</span></span>

-   <span data-ttu-id="311ff-121">Wenn Sie sicherstellen möchten, dass der Cache über genügend Speicherplatz für alle Pakete verfügt, die möglicherweise bereitgestellt werden, verwenden Sie die Einstellung Speicher **Platz für freien Speicherplatz verwenden** , wenn Sie den Client so konfigurieren, dass der Cache nach Bedarf erweitert werden kann.</span><span class="sxs-lookup"><span data-stu-id="311ff-121">To ensure that the cache has sufficient space allocated for all packages that might be deployed, use the **Use free disk space threshold** setting when you configure the client so that the cache can grow as needed.</span></span> <span data-ttu-id="311ff-122">Sie können aber auch im voraus ermitteln, wie viel Speicherplatz für den App-V-Cache benötigt wird, und die Cachegröße zur Installationszeit entsprechend festlegen.</span><span class="sxs-lookup"><span data-stu-id="311ff-122">Alternatively, determine in advance how much disk space will be needed for the App-V cache, and at installation time, set the cache size accordingly.</span></span> <span data-ttu-id="311ff-123">Weitere Informationen zum Cache Space Management-Feature finden Sie unter **Verwenden des Cache-Speicherplatz Verwaltungsfeatures** im Microsoft Application Virtualization (App-V)-Betriebsleitfaden.</span><span class="sxs-lookup"><span data-stu-id="311ff-123">For more information about the cache space management feature, see **How to Use the Cache Space Management Feature** in the Microsoft Application Virtualization (App-V) Operations Guide.</span></span>

-   <span data-ttu-id="311ff-124">Während der Veröffentlichungs-und http (S)-Streaming-Vorgänge verwenden App-V 4,5 SP1-Clients die Proxyservereinstellungen, die in Internet Explorer auf dem Computer des Benutzers konfiguriert sind.</span><span class="sxs-lookup"><span data-stu-id="311ff-124">During both the publishing and HTTP(S) streaming operations,App-V 4.5 SP1 clients use the proxy server settings that are configured in Internet Explorer on the user’s computer.</span></span>

<span data-ttu-id="311ff-125">Weitere Informationen zum Konfigurieren der Client Installationsparameter finden Sie unter [Befehlszeilenparameter für Application Virtualization Client Installer](application-virtualization-client-installer-command-line-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="311ff-125">For more information about configuring the client installation parameters, see [Application Virtualization Client Installer Command-Line Parameters](application-virtualization-client-installer-command-line-parameters.md).</span></span>

 

<span data-ttu-id="311ff-126">Schließlich müssen Sie ermitteln, wie die Application Virtualization-Desktop Client Software für die Desktop Clients bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="311ff-126">Finally, you need to determine how to deploy the Application Virtualization Desktop Client software for the desktop clients.</span></span> <span data-ttu-id="311ff-127">Obwohl es möglich ist, den Application Virtualization Desktop Client manuell auf jedem Computer bereitzustellen, müssten die meisten Organisationen dies über einen automatisierten Prozess durchführen.</span><span class="sxs-lookup"><span data-stu-id="311ff-127">Although it is possible to deploy the Application Virtualization Desktop Client manually on each computer, most organizations would need to do this through some automated process.</span></span> <span data-ttu-id="311ff-128">Bei einer mittleren oder großen Organisation ist möglicherweise ein ESD-System in Betrieb, was eine ideale Möglichkeit zum Bereitstellen des Clients darstellt.</span><span class="sxs-lookup"><span data-stu-id="311ff-128">A medium or large organization might have an ESD system in operation, and that would be an ideal way to deploy the client.</span></span> <span data-ttu-id="311ff-129">Wenn kein ESD-System vorhanden ist, können Sie die Standardmethode zur Installation von Software in Ihrer Organisation verwenden.</span><span class="sxs-lookup"><span data-stu-id="311ff-129">If no ESD system exists, you can use your standard method of installing software in your organization.</span></span> <span data-ttu-id="311ff-130">Zu den Auswahlmöglichkeiten gehören Gruppenrichtlinien oder verschiedene Skripttechniken.</span><span class="sxs-lookup"><span data-stu-id="311ff-130">Choices include Group Policy or various scripting techniques.</span></span> <span data-ttu-id="311ff-131">Je nach Anzahl und Größe der Offices, die Sie haben, kann dieser Bereitstellungsprozess komplex sein, und es ist wichtig, dass Sie einen strukturierten Ansatz Unternehmen, um sicherzustellen, dass alle Computer einen Client mit der richtigen Konfiguration installieren.</span><span class="sxs-lookup"><span data-stu-id="311ff-131">Depending on the number and size of the offices you have, this deployment process can be complex, and it is essential that you take a structured approach to ensure all computers get a client installed with the correct configuration.</span></span>

## <span data-ttu-id="311ff-132">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="311ff-132">Related topics</span></span>


[<span data-ttu-id="311ff-133">Planen der Bereitstellung von Application Virtualization System</span><span class="sxs-lookup"><span data-stu-id="311ff-133">Planning for Application Virtualization System Deployment</span></span>](planning-for-application-virtualization-system-deployment.md)

[<span data-ttu-id="311ff-134">So installieren Sie den Client über die Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="311ff-134">How to Install the Client by Using the Command Line</span></span>](how-to-install-the-client-by-using-the-command-line-new.md)

[<span data-ttu-id="311ff-135">So veröffentlichen Sie eine virtuelle Anwendung auf dem Client</span><span class="sxs-lookup"><span data-stu-id="311ff-135">How to Publish a Virtual Application on the Client</span></span>](how-to-publish-a-virtual-application-on-the-client.md)

[<span data-ttu-id="311ff-136">So aktualisieren Sie Application Virtualization Client</span><span class="sxs-lookup"><span data-stu-id="311ff-136">How to Upgrade the Application Virtualization Client</span></span>](how-to-upgrade-the-application-virtualization-client.md)

[<span data-ttu-id="311ff-137">So deinstallieren Sie App-V Client</span><span class="sxs-lookup"><span data-stu-id="311ff-137">How to Uninstall the App-V Client</span></span>](how-to-uninstall-the-app-v-client.md)

 

 





