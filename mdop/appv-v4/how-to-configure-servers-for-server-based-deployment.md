---
title: So konfigurieren Sie Server für die serverbasierte Bereitstellung
description: So konfigurieren Sie Server für die serverbasierte Bereitstellung
author: dansimp
ms.assetid: 6371c37a-46eb-44e8-ad6b-4430c866c8b4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4c60ae89bc42fddad8aeb6a4f6df0f2c0b4ee4f2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807299"
---
# <span data-ttu-id="68257-103">So konfigurieren Sie Server für die serverbasierte Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="68257-103">How to Configure Servers for Server-Based Deployment</span></span>


<span data-ttu-id="68257-104">Dieser Abschnitt enthält Verfahren, mit denen Sie die Microsoft System Center Application Virtualization (App-V)-Verwaltungsserver und Microsoft System Center Application Virtualization-Streamingserver sowie die Internet Informationsdienste (IIS) und Dateiserver entsprechend ihrer Application Virtualization Server-basierten Bereitstellungsstrategie konfigurieren können.</span><span class="sxs-lookup"><span data-stu-id="68257-104">This section provides procedures you can use to configure the Microsoft System Center Application Virtualization (App-V) Management Servers and Microsoft System Center Application Virtualization Streaming Servers, and the Internet Information Services (IIS) and file servers, as appropriate for your Application Virtualization Server-based deployment strategy.</span></span>

## <span data-ttu-id="68257-105">Inhalt dieses Abschnitts</span><span class="sxs-lookup"><span data-stu-id="68257-105">In This Section</span></span>


<a href="" id="how-to-configure-the-application-virtualization-management-servers"></a>[<span data-ttu-id="68257-106">So konfigurieren Sie Anwendung Virtualisierung Management Server</span><span class="sxs-lookup"><span data-stu-id="68257-106">How to Configure the Application Virtualization Management Servers</span></span>](how-to-configure-the-application-virtualization-management-servers.md)  
<span data-ttu-id="68257-107">Bietet eine schrittweise Anleitung zum Konfigurieren der Application Virtualization-Verwaltungsserver.</span><span class="sxs-lookup"><span data-stu-id="68257-107">Provides a step-by-step procedure for configuring the Application Virtualization Management Servers.</span></span>

<a href="" id="how-to-configure-the-application-virtualization-streaming-servers"></a>[<span data-ttu-id="68257-108">So konfigurieren Sie Application Virtualization Streaming Server</span><span class="sxs-lookup"><span data-stu-id="68257-108">How to Configure the Application Virtualization Streaming Servers</span></span>](how-to-configure-the-application-virtualization-streaming-servers.md)  
<span data-ttu-id="68257-109">Enthält ein schrittweises Verfahren zum Konfigurieren der Application Virtualization-Streamingserver.</span><span class="sxs-lookup"><span data-stu-id="68257-109">Provides a step-by-step procedure for configuring the Application Virtualization Streaming Servers.</span></span>

<a href="" id="how-to-configure-the-server-for-iis"></a>[<span data-ttu-id="68257-110">So konfigurieren Sie den Server für IIS</span><span class="sxs-lookup"><span data-stu-id="68257-110">How to Configure the Server for IIS</span></span>](how-to-configure-the-server-for-iis.md)  
<span data-ttu-id="68257-111">Enthält eine schrittweise Anleitung zum Konfigurieren des IIS-Servers für Ihre serverbasierte Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="68257-111">Provides a step-by-step procedure for configuring the IIS server for your server-based deployment.</span></span>

<a href="" id="how-to-configure-the-server-to-be-trusted-for-delegation"></a>[<span data-ttu-id="68257-112">So konfigurieren Sie den Server, damit ihm für Delegierungszwecke vertraut wird</span><span class="sxs-lookup"><span data-stu-id="68257-112">How to Configure the Server to be Trusted for Delegation</span></span>](how-to-configure-the-server-to-be-trusted-for-delegation.md)  
<span data-ttu-id="68257-113">Enthält detaillierte Anweisungen zum Konfigurieren des Servers, der für die Delegierung als vertrauenswürdig eingestuft wird.</span><span class="sxs-lookup"><span data-stu-id="68257-113">Provides detailed instructions about how to configure the server to be trusted for delegation.</span></span>

<a href="" id="configuring-the-firewall-for-the-app-v-servers"></a>[<span data-ttu-id="68257-114">Konfigurieren der Firewall für App-V Server</span><span class="sxs-lookup"><span data-stu-id="68257-114">Configuring the Firewall for the App-V Servers</span></span>](configuring-the-firewall-for-the-app-v-servers.md)  
<span data-ttu-id="68257-115">Beschreibt die Firewalleinstellungen, die für die App-V-Server erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="68257-115">Describes the firewall settings required for the App-V servers.</span></span>

<a href="" id="how-to-install-and-configure-the-default-application"></a>[<span data-ttu-id="68257-116">So installieren und konfigurieren Sie die Standardanwendung</span><span class="sxs-lookup"><span data-stu-id="68257-116">How to Install and Configure the Default Application</span></span>](how-to-install-and-configure-the-default-application.md)  
<span data-ttu-id="68257-117">Beschreibt, wie Sie die Standardanwendung zum Testen des App-V-Systems installieren und konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="68257-117">Describes how to install and configure the default application for testing the App-V system.</span></span>

## <span data-ttu-id="68257-118">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="68257-118">Related topics</span></span>


[<span data-ttu-id="68257-119">Übersicht über Application Virtualization Server-basierte Szenarien</span><span class="sxs-lookup"><span data-stu-id="68257-119">Application Virtualization Server-Based Scenario Overview</span></span>](application-virtualization-server-based-scenario-overview.md)

[<span data-ttu-id="68257-120">Electronic Software Distribution-basiertes Szenario</span><span class="sxs-lookup"><span data-stu-id="68257-120">Electronic Software Distribution-Based Scenario</span></span>](electronic-software-distribution-based-scenario.md)

[<span data-ttu-id="68257-121">So installieren Sie die Server und Systemkomponenten</span><span class="sxs-lookup"><span data-stu-id="68257-121">How to Install the Servers and System Components</span></span>](how-to-install-the-servers-and-system-components.md)

 

 





