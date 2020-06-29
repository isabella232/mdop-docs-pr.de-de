---
title: Überwachen von Application Virtualization Servern
description: Überwachen von Application Virtualization Servern
author: dansimp
ms.assetid: d84355ae-4fe4-41d9-ac3a-3eaa32d9a61f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a53c0c37ca609c701727a7f4e18019a9f20110ed
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806588"
---
# <span data-ttu-id="a95a2-103">Überwachen von Application Virtualization Servern</span><span class="sxs-lookup"><span data-stu-id="a95a2-103">Monitoring Application Virtualization Servers</span></span>


<span data-ttu-id="a95a2-104">Zur Vereinfachung der Application Virtualization-Server Verwaltung (App-V) können Sie das System Center Operations Manager2007-Management Pack verwenden.</span><span class="sxs-lookup"><span data-stu-id="a95a2-104">To simplify Application Virtualization (App-V) Server management, you can use the System Center Operations Manager2007 Management Pack.</span></span> <span data-ttu-id="a95a2-105">Dieses Management Pack unterstützt nur Application Virtualization (App-V) 4,5-Server; frühere Server Versionen werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a95a2-105">This Management Pack supports only Application Virtualization (App-V) 4.5 servers; it does not support previous server versions.</span></span> <span data-ttu-id="a95a2-106">Das Management Pack maximiert die APP-v Server-Verfügbarkeit für die Behandlung von App-v-Client Anforderungen.</span><span class="sxs-lookup"><span data-stu-id="a95a2-106">The Management Pack maximizes App-V Server availability for handling App-V Client requests.</span></span>

## <span data-ttu-id="a95a2-107">Status anzeigen</span><span class="sxs-lookup"><span data-stu-id="a95a2-107">Status Indicators</span></span>


<span data-ttu-id="a95a2-108">Die Statusanzeige des App-V-Servers ist farblich gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="a95a2-108">The App-V Server health status indicators are color-coded.</span></span> <span data-ttu-id="a95a2-109">Die Farben stellen die folgenden Statuswerte dar:</span><span class="sxs-lookup"><span data-stu-id="a95a2-109">The colors represent the following status values:</span></span>

-   <span data-ttu-id="a95a2-110">Keine Farbe gibt an, dass der Server ohne nicht BEHEB Bare Fehler ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a95a2-110">No color indicates that the server is running without non-recoverable errors.</span></span>

-   <span data-ttu-id="a95a2-111">Gelb gibt an, dass eine der Komponenten nicht ordnungsgemäß funktioniert.</span><span class="sxs-lookup"><span data-stu-id="a95a2-111">Yellow indicates that one of the components is not functioning correctly.</span></span> <span data-ttu-id="a95a2-112">Die Gesamtfunktionalität des Servers wird beeinträchtigt, der Server steht jedoch weiterhin zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="a95a2-112">The overall functionality of the server is degraded, but the server is still available.</span></span>

-   <span data-ttu-id="a95a2-113">Rot gibt an, dass der Server nicht verfügbar ist und keine wichtigen Dienste bereitstellen oder mit externen Dienstabhängigkeiten kommunizieren kann.</span><span class="sxs-lookup"><span data-stu-id="a95a2-113">Red indicates that the server is not available and that it cannot provide key services or communicate with external service dependencies.</span></span>

## <span data-ttu-id="a95a2-114">Überwachungskriterien</span><span class="sxs-lookup"><span data-stu-id="a95a2-114">Monitoring Criteria</span></span>


<span data-ttu-id="a95a2-115">Das Management Pack überwacht die folgenden Aspekte des Serverzustands:</span><span class="sxs-lookup"><span data-stu-id="a95a2-115">The Management Pack monitors the following aspects of server health:</span></span>

-   <span data-ttu-id="a95a2-116">Server Status: überwacht Serverereignisse, um zu überprüfen, ob der Server die erwarteten Dienste bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="a95a2-116">Server Status—monitors server events to validate that the server is providing its expected services.</span></span>

-   <span data-ttu-id="a95a2-117">Zugriff auf Datenspeicher: verfolgt die Möglichkeit eines oder mehrerer App-v-Verwaltungsserver, auf den App-v-Datenspeicher zuzugreifen und mit ihm zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="a95a2-117">Data Store Access—tracks the ability of one or more of the App-V Management Servers to access and communicate with the App-V data store.</span></span>

-   <span data-ttu-id="a95a2-118">Zugriff auf Inhaltsdaten: überwacht den Zugriff auf das \\Content-Verzeichnis, das ein lokales Verzeichnis oder eine Netzwerkfreigabe sein kann, und die Möglichkeit, die angeforderten Dateien zu lesen.</span><span class="sxs-lookup"><span data-stu-id="a95a2-118">Content Data Access—monitors access to the \\Content directory, which might be a local directory or a network share, and the ability to read the requested files.</span></span>

-   <span data-ttu-id="a95a2-119">Sicherheit – meldet Fehler mit dem Zertifikat des App-V-Servers und der sicheren Kommunikation.</span><span class="sxs-lookup"><span data-stu-id="a95a2-119">Security—reports errors with the App-V Server’s certificate and secure communications.</span></span>

-   <span data-ttu-id="a95a2-120">Client Anforderungsbehandlung – überwacht die Fähigkeit eines oder mehrerer App-V-Server, Clientanforderungen zu verarbeiten und auf diese ordnungsgemäß zu reagieren.</span><span class="sxs-lookup"><span data-stu-id="a95a2-120">Client Request Handling—monitors the ability of one or more of the App-V Servers to handle and correctly respond to client requests.</span></span> <span data-ttu-id="a95a2-121">Diese Anforderungen umfassen das Veröffentlichen von Elementen wie Konfigurationsanforderungen, Paket Ladeanforderungen und außerhalb von Sequenz Anforderungen.</span><span class="sxs-lookup"><span data-stu-id="a95a2-121">These requests include publishing such items as configuration requests, package load requests, and out of sequence requests.</span></span>

-   <span data-ttu-id="a95a2-122">Serverkonfiguration: überprüft die Konfigurationseinstellungen des App-V-Servers.</span><span class="sxs-lookup"><span data-stu-id="a95a2-122">Server Configuration—checks the configuration settings of the App-V Server.</span></span> <span data-ttu-id="a95a2-123">Diese Konfigurationseinstellungen umfassen die Einstellungen in der Registrierung und im App-V-Datenspeicher.</span><span class="sxs-lookup"><span data-stu-id="a95a2-123">These configuration settings include the settings in the registry and in the App-V data store.</span></span>

## <span data-ttu-id="a95a2-124">Server Unterschiede</span><span class="sxs-lookup"><span data-stu-id="a95a2-124">Server Differences</span></span>


<span data-ttu-id="a95a2-125">Die wichtigsten Unterschiede zwischen dem App-v-Verwaltungsserver und dem App-v-Streamingserver lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="a95a2-125">The main differences between the App-V Management Server and the App-V Streaming Server are as follows:</span></span>

-   <span data-ttu-id="a95a2-126">App-V-Verwaltungsserver können Veröffentlichungs-, Streaming-, Verwaltungs-und Berichterstattungs Dienste bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="a95a2-126">App-V Management Servers can provide publishing, streaming, management, and reporting services.</span></span> <span data-ttu-id="a95a2-127">Daher kann das Management Pack mehr Aspekte des App-v-Verwaltungsservers verwalten, als auf dem App-v-Streamingserver verwaltet werden können, der nur Paketstreaming bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="a95a2-127">Therefore, the Management Pack can manage more aspects of the App-V Management Server than it can manage on the App-V Streaming Server, which provides only package streaming.</span></span>

-   <span data-ttu-id="a95a2-128">Der APP-v-Streamingserver hat keinen App-v-Datenspeicher, daher wird der Zugriff auf den Datenspeicher nicht überwacht.</span><span class="sxs-lookup"><span data-stu-id="a95a2-128">The App-V Streaming Server does not have an App-V data store, so data store access is not monitored.</span></span> <span data-ttu-id="a95a2-129">Die Konfigurationsinformationen für den App-V-Streamingserver werden in der Registrierung verwaltet.</span><span class="sxs-lookup"><span data-stu-id="a95a2-129">The configuration information for the App-V Streaming Server is managed in the registry.</span></span>

-   <span data-ttu-id="a95a2-130">Der APP-v-Streamingserver verwendet nicht die Schnittstelle der APP-v Server-Verwaltungskonsole. Verwenden Sie andere Tools, um die Konfiguration zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="a95a2-130">The App-V Streaming Server does not use the App-V Server Management Console interface; use other tools to manage the configuration.</span></span>

## <span data-ttu-id="a95a2-131">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="a95a2-131">Related topics</span></span>


[<span data-ttu-id="a95a2-132">Application Virtualization Server</span><span class="sxs-lookup"><span data-stu-id="a95a2-132">Application Virtualization Server</span></span>](application-virtualization-server.md)

 

 





