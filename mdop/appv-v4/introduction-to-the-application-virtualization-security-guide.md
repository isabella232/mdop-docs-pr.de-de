---
title: Einführung in das Application Virtualization Security Guide
description: Einführung in das Application Virtualization Security Guide
author: dansimp
ms.assetid: 50e1d220-7a95-45b8-933b-3dadddebe26f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 4b41c65c5ad753aa606d47d2eafe4a28e035cc4e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806639"
---
# <span data-ttu-id="d714c-103">Einführung in das Application Virtualization Security Guide</span><span class="sxs-lookup"><span data-stu-id="d714c-103">Introduction to the Application Virtualization Security Guide</span></span>


<span data-ttu-id="d714c-104">Dieser Microsoft Application Virtualization (app-v)-Sicherheitsleitfaden enthält Anweisungen für Administratoren, die für die Konfiguration der Sicherheitsfeatures verantwortlich sind, die für die APP-v-Bereitstellung ausgewählt wurden.</span><span class="sxs-lookup"><span data-stu-id="d714c-104">This Microsoft Application Virtualization (App-V) security guide provides instructions for administrators who are responsible for configuring the security features that were selected for the App-V deployment.</span></span>

<span data-ttu-id="d714c-105">**Hinweis**  Diese Dokumentation bietet keine Anleitungen für die Auswahl der spezifischen Sicherheitsoptionen.</span><span class="sxs-lookup"><span data-stu-id="d714c-105">**Note** This documentation does not provide guidance for choosing the specific security options.</span></span> <span data-ttu-id="d714c-106">Diese Informationen finden Sie im Whitepaper zu App-V Security Best Practices, das unter verfügbar ist <https://go.microsoft.com/fwlink/?LinkId=127120> .</span><span class="sxs-lookup"><span data-stu-id="d714c-106">That information is provided in the App-V Security Best Practices white paper available at <https://go.microsoft.com/fwlink/?LinkId=127120>.</span></span>

 

<span data-ttu-id="d714c-107">Als App-V-Administrator mit diesem Leitfaden sollten Sie mit den folgenden sicherheitsrelevanten Technologien vertraut sein:</span><span class="sxs-lookup"><span data-stu-id="d714c-107">As an App-V administrator using this guide, you should be familiar with the following security-related technologies:</span></span>

-   <span data-ttu-id="d714c-108">Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="d714c-108">Active Directory Domain Services</span></span>

-   <span data-ttu-id="d714c-109">Infrastruktur öffentlicher Schlüssel (PKI)</span><span class="sxs-lookup"><span data-stu-id="d714c-109">Public key infrastructure (PKI)</span></span>

-   <span data-ttu-id="d714c-110">IPSec (Internet Protocol Security)</span><span class="sxs-lookup"><span data-stu-id="d714c-110">Internet Protocol Security (IPsec)</span></span>

-   <span data-ttu-id="d714c-111">Gruppenrichtlinien</span><span class="sxs-lookup"><span data-stu-id="d714c-111">Group Policies</span></span>

-   <span data-ttu-id="d714c-112">Internet Informationsdienste (IIS)</span><span class="sxs-lookup"><span data-stu-id="d714c-112">Internet Information Services (IIS)</span></span>

## <span data-ttu-id="d714c-113">App-V-Infrastrukturkomponenten</span><span class="sxs-lookup"><span data-stu-id="d714c-113">APP-V Infrastructure Components</span></span>


<span data-ttu-id="d714c-114">Wenn Sie eine erweiterte Sicherheits-App-V-Umgebung planen, können Sie verschiedene Infrastrukturmodelle in Frage stellen.</span><span class="sxs-lookup"><span data-stu-id="d714c-114">When planning an enhanced security App-V environment, you can consider several different infrastructure models.</span></span>

<span data-ttu-id="d714c-115">**Hinweis**  Weitere Informationen zu App-V-Infrastrukturmodellen finden Sie in der folgenden Dokumentation:</span><span class="sxs-lookup"><span data-stu-id="d714c-115">**Note** For more information about App-V infrastructure models, see the following documentation:</span></span>

-   [<span data-ttu-id="d714c-116">Leitfaden zur Planung und Bereitstellung von App-V</span><span class="sxs-lookup"><span data-stu-id="d714c-116">App-V Planning and Deployment Guide</span></span>](https://go.microsoft.com/fwlink/?LinkId=122063)

-   [<span data-ttu-id="d714c-117">Leitfaden für Infrastrukturplanung und-Entwurf</span><span class="sxs-lookup"><span data-stu-id="d714c-117">Infrastructure Planning and Design Guide Series</span></span>](https://go.microsoft.com/fwlink/?LinkId=151986)

 

<span data-ttu-id="d714c-118">Diese Modelle verwenden einige, aber möglicherweise nicht alle App-V-Komponenten, die in der folgenden Abbildung dargestellt sind.</span><span class="sxs-lookup"><span data-stu-id="d714c-118">These models utilize some but possibly not all of the App-V components depicted in the following illustration.</span></span>

![App-v Branch Office-Diagramm](images/appvbranchoffices.gif)

<a href="" id="application-virtualization--app-v--management-server"></a><span data-ttu-id="d714c-120">Application Virtualization (App-V)-Verwaltungs Server</span><span class="sxs-lookup"><span data-stu-id="d714c-120">Application Virtualization (App-V) Management Server</span></span>  
<span data-ttu-id="d714c-121">Der APP-v-Verwaltungs Server strömt den Paketinhalt aus und veröffentlicht die Verknüpfungen und Dateitypen Zuordnungen für den App-v-Client.</span><span class="sxs-lookup"><span data-stu-id="d714c-121">The App-V Management Server streams the package content and publishes the shortcuts and file-type associations to the App-V Client.</span></span> <span data-ttu-id="d714c-122">Der App-V-Verwaltungs Server unterstützt auch das aktive Upgrade, die Lizenzverwaltung und eine Datenbank, die für die Berichterstellung verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="d714c-122">The App-V Management Server also supports active upgrade, license management, and a database that can be used for reporting.</span></span>

<a href="" id="application-virtualization--app-v--streaming-server"></a><span data-ttu-id="d714c-123">Application Virtualization (App-V)-Streamingserver</span><span class="sxs-lookup"><span data-stu-id="d714c-123">Application Virtualization (App-V) Streaming Server</span></span>  
<span data-ttu-id="d714c-124">Der APP-v-Streamingserver hostet die Pakete für das Streaming an App-v-Clients in Umgebungen wie Zweigstellen, bei denen die Bandbreite der Verbindung zum App-v-Verwaltungsserver nicht ausreicht, um Paketinhalte an Clients zu streamen.</span><span class="sxs-lookup"><span data-stu-id="d714c-124">The App-V Streaming Server hosts the packages for streaming to App-V Clients in environments such as branch offices, where the bandwidth of the connection to the App-V Management Server is insufficient for streaming package content to clients.</span></span> <span data-ttu-id="d714c-125">Der Streamingserver enthält nur Streamingfunktionen und stellt Ihnen keine app-v-Verwaltungskonsole oder den App-v-Verwaltungs-Webdienst zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="d714c-125">The Streaming Server contains only streaming functionality and does not provide you with the App-V Management Console or the App-V Management Web Service.</span></span>

<a href="" id="application-virtualization--app-v--data-store"></a><span data-ttu-id="d714c-126">Application Virtualization (App-V)-Datenspeicher</span><span class="sxs-lookup"><span data-stu-id="d714c-126">Application Virtualization (App-V) Data Store</span></span>  
<span data-ttu-id="d714c-127">Der APP-v-Datenspeicher in der SQL-Datenbank speichert Informationen zur APP-v-Infrastruktur.</span><span class="sxs-lookup"><span data-stu-id="d714c-127">The App-V data store, in the SQL database, retains information related to the App-V infrastructure.</span></span> <span data-ttu-id="d714c-128">Die Informationen im App-V-Datenspeicher umfassen alle Anwendungsdatensätze, Anwendungszuordnungen und die Gruppen, die die Application Virtualization-Umgebung verwalten.</span><span class="sxs-lookup"><span data-stu-id="d714c-128">The information in the App-V data store includes all application records, application assignments, and which groups manage the Application Virtualization environment.</span></span>

<a href="" id="application-virtualization--app-v--management-service"></a><span data-ttu-id="d714c-129">Application Virtualization (App-V)-Verwaltungsdienst</span><span class="sxs-lookup"><span data-stu-id="d714c-129">Application Virtualization (App-V) Management Service</span></span>  
<span data-ttu-id="d714c-130">Der App-V-Verwaltungsdienst kommuniziert Lese-und Schreibanforderungen an den Application Virtualization-Datenspeicher.</span><span class="sxs-lookup"><span data-stu-id="d714c-130">The App-V Management Service communicates read/write requests to the Application Virtualization data store.</span></span> <span data-ttu-id="d714c-131">Diese Komponente kann auf demselben Computer wie der App-V-Verwaltungs Server oder auf einem anderen Computer installiert sein, auf dem IIS installiert ist.</span><span class="sxs-lookup"><span data-stu-id="d714c-131">This component can be installed on the same computer as the App-V Management Server or on a separate computer with IIS installed.</span></span>

<a href="" id="application-virtualization--app-v--management-console"></a><span data-ttu-id="d714c-132">Application Virtualization (App-V)-Verwaltungskonsole</span><span class="sxs-lookup"><span data-stu-id="d714c-132">Application Virtualization (App-V) Management Console</span></span>  
<span data-ttu-id="d714c-133">Die APP-v-Verwaltungskonsole ist ein Snap-in-Verwaltungsdienstprogramm für die APP-v Server-Verwaltung.</span><span class="sxs-lookup"><span data-stu-id="d714c-133">The App-V Management Console is a snap-in management utility for App-V Server administration.</span></span> <span data-ttu-id="d714c-134">Diese Komponente kann auf demselben Computer wie der App-V-Server oder auf einer separaten Workstation mit MMC 3.0 und installiert werden. NET 2.0 installiert ist.</span><span class="sxs-lookup"><span data-stu-id="d714c-134">This component can be installed on the same computer as the App-V Server or on a separate workstation that has MMC3.0 and .NET2.0 installed.</span></span>

<a href="" id="application-virtualization--app-v--sequencer"></a><span data-ttu-id="d714c-135">Application Virtualization (App-V)-Sequenzer</span><span class="sxs-lookup"><span data-stu-id="d714c-135">Application Virtualization (App-V) Sequencer</span></span>  
<span data-ttu-id="d714c-136">Der App-V-Sequencer überwacht und erfasst die Installation von Anwendungen und erstellt virtuelle Anwendungspakete.</span><span class="sxs-lookup"><span data-stu-id="d714c-136">The App-V Sequencer monitors and captures the installation of applications and creates virtual application packages.</span></span> <span data-ttu-id="d714c-137">Die Ausgabe des Sequencers besteht aus dem Anwendungssymbol, der OSD-Datei mit Anwendungs Definitionsinformationen, einer Paket Manifestdatei und einer SFT-Datei mit den Inhaltsdateien der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="d714c-137">The output of the Sequencer consists of the application icon, the OSD file containing application definition information, a package manifest file, and an SFT file containing the application’s content files.</span></span> <span data-ttu-id="d714c-138">Optional kann eine Windows Installer-Datei für die Installation des Pakets erstellt werden, ohne die App-V-Infrastruktur zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="d714c-138">Optionally, a Windows Installer file can be created for installing the package without using the App-V infrastructure.</span></span>

<a href="" id="application-virtualization--app-v--client"></a><span data-ttu-id="d714c-139">Application Virtualization (App-V)-Client</span><span class="sxs-lookup"><span data-stu-id="d714c-139">Application Virtualization (App-V) Client</span></span>  
<span data-ttu-id="d714c-140">Der APP-v-Client ist auf dem App-v-Desktop Clientcomputer oder auf dem App-v-Terminaldiensteclient installiert.</span><span class="sxs-lookup"><span data-stu-id="d714c-140">The App-V Client is installed on the App-V Desktop Client computer or on the App-V Terminal Services Client computer.</span></span> <span data-ttu-id="d714c-141">Sie stellt die virtuelle Umgebung für die virtuellen Anwendungspakete bereit.</span><span class="sxs-lookup"><span data-stu-id="d714c-141">It provides the virtual environment for the virtual application packages.</span></span> <span data-ttu-id="d714c-142">Der App-V-Client verwaltet das Streaming des Pakets in den Cache, die Aktualisierung der virtuellen Anwendungsveröffentlichung und die Interaktion mit den Application Virtualization-Servern.</span><span class="sxs-lookup"><span data-stu-id="d714c-142">The App-V Client manages the package streaming to the cache, virtual application publishing refresh, and interaction with the Application Virtualization Servers.</span></span>

 

 





