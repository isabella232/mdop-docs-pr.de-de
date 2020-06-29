---
title: Verwenden von Application Virtualization-Servern als Paketverwaltungslösung
description: Verwenden von Application Virtualization-Servern als Paketverwaltungslösung
author: dansimp
ms.assetid: 41597355-e7bb-45e2-b300-7b1724419975
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2b81ed3ab6fa3a70fe4780904059091f22579d9e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806180"
---
# <span data-ttu-id="cb89b-103">Verwenden von Application Virtualization-Servern als Paketverwaltungslösung</span><span class="sxs-lookup"><span data-stu-id="cb89b-103">Using Application Virtualization Servers as a Package Management Solution</span></span>


<span data-ttu-id="cb89b-104">Wenn Sie nicht über ein vorhandenes ESD-System zum Bereitstellen Ihrer Application Virtualization-Lösung verfügen oder keines verwenden möchten, müssen Sie einen oder mehrere Application Virtualization Management-Server als Kern ihrer Systemarchitektur installieren.</span><span class="sxs-lookup"><span data-stu-id="cb89b-104">If you do not have an existing ESD system to deploy your Application Virtualization solution or do not wish to use one, you will need to install one or more Application Virtualization Management Servers as the core of your system architecture.</span></span> <span data-ttu-id="cb89b-105">Der Application Virtualization Management-Server erfordert einen dedizierten Server Computer und benötigt eine Microsoft SQL Server-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="cb89b-105">The Application Virtualization Management Server requires a dedicated server computer and needs a Microsoft SQL Server database.</span></span> <span data-ttu-id="cb89b-106">Die Datenbank kann sich auf demselben Server befinden oder auf einem Unternehmensdatenbankserver konfiguriert werden, auf den der Application Virtualization Management-Server über eine Hochgeschwindigkeits-LAN-Verbindung zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="cb89b-106">The database can be on the same server, or it can be configured on a corporate database server that is accessible to the Application Virtualization Management Server over a high-speed LAN connection.</span></span> <span data-ttu-id="cb89b-107">Darüber hinaus müssen Sie die Microsoft Application Virtualization Management Console entweder auf dem Application Virtualization-Verwaltungsserver oder auf einer bestimmten Verwaltungsarbeitsstation installieren, und Sie müssen den Microsoft Application Virtualization Management Web Service installieren, der auch auf dem Application Virtualization Management Server oder auf einem separaten IIS-Server installiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="cb89b-107">In addition, you will need to install the Microsoft Application Virtualization Management Console, on either the Application Virtualization Management Server or on a designated management workstation, and you will need to install the Microsoft Application Virtualization Management Web Service, which can also be installed on the Application Virtualization Management Server or on a separate IIS server.</span></span> <span data-ttu-id="cb89b-108">Die Application Virtualization-Verwaltungskonsole wird zum Herstellen einer Verbindung mit dem Application Virtualization Management Web Service verwendet, sodass der System Administrator mit dem Application Virtualization Management Server interagieren kann.</span><span class="sxs-lookup"><span data-stu-id="cb89b-108">The Application Virtualization Management Console is used to connect to the Application Virtualization Management Web Service, enabling the system administrator to interact with the Application Virtualization Management Server.</span></span>

<span data-ttu-id="cb89b-109">**Hinweis**  Der Zugriff auf die Anwendungen wird mithilfe von Sicherheitsgruppen in den Active Directory-Domänendiensten gesteuert, sodass Sie einen Prozess planen müssen, um eine Sicherheitsgruppe für jede virtualisierte Anwendung einzurichten und zu verwalten, welche Benutzer zu jeder Gruppe hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="cb89b-109">**Note** Access to the applications is controlled by means of Security Groups in Active Directory Domain Services, so you will need to plan a process to set up a security group for each virtualized application and for managing which users are added to each group.</span></span> <span data-ttu-id="cb89b-110">Der Application Virtualization Management Server-Administrator konfiguriert den Server für die Verwendung dieser Active Directory-Gruppen, und der Server steuert dann automatisch den Zugriff auf die Pakete basierend auf der Active Directory-Gruppenmitgliedschaft.</span><span class="sxs-lookup"><span data-stu-id="cb89b-110">The Application Virtualization Management Server administrator configures the server to use these Active Directory groups, and the server then automatically controls access to the packages based on Active Directory group membership.</span></span>

 

## <span data-ttu-id="cb89b-111">Inhalt dieses Abschnitts</span><span class="sxs-lookup"><span data-stu-id="cb89b-111">In This Section</span></span>


<a href="" id="overview-of-the-application-virtualization-system-components"></a>[<span data-ttu-id="cb89b-112">Übersicht über die Application Virtualization-Systemkomponenten</span><span class="sxs-lookup"><span data-stu-id="cb89b-112">Overview of the Application Virtualization System Components</span></span>](overview-of-the-application-virtualization-system-components.md)  
<span data-ttu-id="cb89b-113">Listet die primären Komponenten des Microsoft Application Virtualization-Verwaltungssystems auf und beschreibt sie.</span><span class="sxs-lookup"><span data-stu-id="cb89b-113">Lists and describes the primary components of the Microsoft Application Virtualization Management System.</span></span>

<a href="" id="publishing-virtual-applications-using-application-virtualization-management-servers"></a>[<span data-ttu-id="cb89b-114">Veröffentlichen von virtuellen Anwendungen mit Application Virtualization Management-Servern</span><span class="sxs-lookup"><span data-stu-id="cb89b-114">Publishing Virtual Applications Using Application Virtualization Management Servers</span></span>](publishing-virtual-applications-using-application-virtualization-management-servers.md)  
<span data-ttu-id="cb89b-115">Bietet einen kurzen Überblick darüber, wie virtuelle Anwendungen in einem Server basierten Bereitstellungsszenario für Application Virtualization veröffentlicht werden.</span><span class="sxs-lookup"><span data-stu-id="cb89b-115">Provides a brief overview of how virtual applications are published in an Application Virtualization Server-based deployment scenario.</span></span>

<a href="" id="planning-your-streaming-solution-in-an-application-virtualization-server-based-implementation"></a>[<span data-ttu-id="cb89b-116">Planen Ihrer Streaming-Lösung in einer Anwendung Virtualisierung Server-basierten-Implementierung</span><span class="sxs-lookup"><span data-stu-id="cb89b-116">Planning Your Streaming Solution in an Application Virtualization Server-Based Implementation</span></span>](planning-your-streaming-solution-in-an-application-virtualization-server-based-implementation.md)  
<span data-ttu-id="cb89b-117">Beschreibt die verfügbaren Optionen für die Verwendung von Application Virtualization Streaming Servern in Verbindung mit ihrer auf Application Virtualization Management Server basierenden Implementierung.</span><span class="sxs-lookup"><span data-stu-id="cb89b-117">Describes available options for using Application Virtualization Streaming Servers in conjunction with your Application Virtualization Management Server-based implementation.</span></span>

## <span data-ttu-id="cb89b-118">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="cb89b-118">Related topics</span></span>


[<span data-ttu-id="cb89b-119">Application Virtualization Server-basiertes Szenario</span><span class="sxs-lookup"><span data-stu-id="cb89b-119">Application Virtualization Server-Based Scenario</span></span>](application-virtualization-server-based-scenario.md)

[<span data-ttu-id="cb89b-120">Planen der Bereitstellung von Application Virtualization System</span><span class="sxs-lookup"><span data-stu-id="cb89b-120">Planning for Application Virtualization System Deployment</span></span>](planning-for-application-virtualization-system-deployment.md)

 

 





