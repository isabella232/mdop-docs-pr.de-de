---
title: Übersicht über Electronic Software Distribution-basierte Szenarien
description: Übersicht über Electronic Software Distribution-basierte Szenarien
author: dansimp
ms.assetid: e9e94b8a-6cba-4de8-9b57-73897796b6a0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: cfbdf40f5ac0f61721c05d0da5cd49e910b16154
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808851"
---
# <span data-ttu-id="48b5f-103">Übersicht über Electronic Software Distribution-basierte Szenarien</span><span class="sxs-lookup"><span data-stu-id="48b5f-103">Electronic Software Distribution-Based Scenario Overview</span></span>


<span data-ttu-id="48b5f-104">Wenn Sie beabsichtigen, eine ESD-Lösung (Electronic Software Distribution) für die Bereitstellung virtueller Anwendungen zu verwenden, ist es wichtig, die Faktoren zu verstehen, die in diese Entscheidung eingehen und davon betroffen sind.</span><span class="sxs-lookup"><span data-stu-id="48b5f-104">If you plan to use an electronic software distribution (ESD) solution to deploy virtual applications, it is important to understand the factors that go into and are affected by that decision.</span></span> <span data-ttu-id="48b5f-105">In diesem Thema werden die Vorteile der Verwendung eines ESD-basierten Szenarios beschrieben, und es werden Informationen zu den Veröffentlichungs-und Paketstreaming-Methoden bereitgestellt, die Sie beim Fortsetzen der Bereitstellung in Frage stellen müssen.</span><span class="sxs-lookup"><span data-stu-id="48b5f-105">This topic describes the benefits of using an ESD-based scenario and provides information about the publishing and package streaming methods that you will need to consider as you proceed with your deployment.</span></span>

<span data-ttu-id="48b5f-106">**Wichtig**  Je nachdem, welche ESD-Lösung Sie verwenden, müssen Sie mit den Anforderungen ihrer jeweiligen Lösung vertraut sein.</span><span class="sxs-lookup"><span data-stu-id="48b5f-106">**Important** Whichever ESD solution you use, you must be familiar with the requirements of your particular solution.</span></span> <span data-ttu-id="48b5f-107">Wenn Sie den Microsoft Endpoint Configuration Manager verwenden, lesen Sie die Configuration Manager-Dokumentation unter <https://go.microsoft.com/fwlink/?LinkId=66999> .</span><span class="sxs-lookup"><span data-stu-id="48b5f-107">If you are using Microsoft Endpoint Configuration Manager, see the Configuration Manager documentation at <https://go.microsoft.com/fwlink/?LinkId=66999>.</span></span>

 

<span data-ttu-id="48b5f-108">Die Verwendung eines vorhandenen ESD-Systems bietet Ihnen folgende Vorteile:</span><span class="sxs-lookup"><span data-stu-id="48b5f-108">Using an existing ESD system provides you with the following benefits:</span></span>

-   <span data-ttu-id="48b5f-109">Beseitigt duale Verwaltungsinfrastrukturen</span><span class="sxs-lookup"><span data-stu-id="48b5f-109">Eliminates dual management infrastructures</span></span>

-   <span data-ttu-id="48b5f-110">Senkt die Kosten zusätzlicher Hardware</span><span class="sxs-lookup"><span data-stu-id="48b5f-110">Reduces the cost of additional hardware</span></span>

-   <span data-ttu-id="48b5f-111">Geringere Kosten für zusätzliche Betriebssystem-und Datenbanklizenzen</span><span class="sxs-lookup"><span data-stu-id="48b5f-111">Reduces the cost of additional operating system and database licenses</span></span>

## <span data-ttu-id="48b5f-112">Veröffentlichungsmethoden</span><span class="sxs-lookup"><span data-stu-id="48b5f-112">Publishing Methods</span></span>


<span data-ttu-id="48b5f-113">Bei Verwendung eines ESD-basierten Szenarios haben Sie die folgenden Möglichkeiten, die Anwendung auf den Clients zu veröffentlichen:</span><span class="sxs-lookup"><span data-stu-id="48b5f-113">When using an ESD-based scenario, you have the following choices for publishing the application to the clients:</span></span>

-   **<span data-ttu-id="48b5f-114">Eigenständiger Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="48b5f-114">Stand-alone Windows Installer.</span></span>** <span data-ttu-id="48b5f-115">Die Windows Installer-Datei enthält das Manifest und die OSD-und ICO-Dateien, die die Clients verwenden, um ein Paket zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="48b5f-115">The Windows Installer file contains the manifest and the OSD and ICO files the clients use to configure a package.</span></span> <span data-ttu-id="48b5f-116">Die Windows Installer-Datei kopiert auch die SFT-Datei auf den Client, da dieses Szenario keinen Server verwendet.</span><span class="sxs-lookup"><span data-stu-id="48b5f-116">The Windows Installer file also copies the SFT file to the client because this scenario does not use a server.</span></span>

-   **<span data-ttu-id="48b5f-117">Windows Installer mit dem Paketmanifest.</span><span class="sxs-lookup"><span data-stu-id="48b5f-117">Windows Installer with the package manifest.</span></span>** <span data-ttu-id="48b5f-118">Die Windows Installer-Datei enthält das Manifest und die OSD-und ICO-Dateien, die die Clients verwenden, um ein Paket zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="48b5f-118">The Windows Installer file contains the manifest and the OSD and ICO files the clients use to configure a package.</span></span> <span data-ttu-id="48b5f-119">Die SFT-Datei wird auf einem Server gespeichert.</span><span class="sxs-lookup"><span data-stu-id="48b5f-119">The SFT file is stored on a server.</span></span> <span data-ttu-id="48b5f-120">Ein Befehlszeilenparameter leitet den Client an den Speicherort der SFT-Datei weiter.</span><span class="sxs-lookup"><span data-stu-id="48b5f-120">A command-line parameter directs the client to the location of the SFT file.</span></span>

-   **<span data-ttu-id="48b5f-121">SFTMIME-Befehle.</span><span class="sxs-lookup"><span data-stu-id="48b5f-121">SFTMIME commands.</span></span>** <span data-ttu-id="48b5f-122">SFTMIME-Befehle werden mit den Manifest-, OSD-, ICO-und SFT-Dateien verwendet, um dem Clientpakete hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="48b5f-122">SFTMIME commands are used with the manifest, OSD, ICO, and SFT files to add packages to the client.</span></span> <span data-ttu-id="48b5f-123">Die Manifestdatei muss sich auf dem Clientcomputer befinden, oder es muss über einen UNC-Pfad zugegriffen werden können.</span><span class="sxs-lookup"><span data-stu-id="48b5f-123">The manifest file must be on the client computer, or it must be accessible through a UNC path.</span></span> <span data-ttu-id="48b5f-124">Je nach Clientkonfiguration und Befehlszeilenoptionen können sich die OSD-, ICO-und SFT-Dateien auf dem Clientcomputer oder auf einem Server befinden.</span><span class="sxs-lookup"><span data-stu-id="48b5f-124">Depending on the client configuration and the command-line options, the OSD, ICO, and SFT files can be on the client computer or on a server.</span></span>

<span data-ttu-id="48b5f-125">Ausführlichere Informationen zu den vorangehenden Veröffentlichungsmethoden finden Sie unter [Ermitteln der Veröffentlichungsmethode](determine-your-publishing-method.md).</span><span class="sxs-lookup"><span data-stu-id="48b5f-125">For more detailed information about the preceding publishing methods, see [Determine Your Publishing Method](determine-your-publishing-method.md).</span></span>

## <span data-ttu-id="48b5f-126">Streaming-Methoden für Pakete</span><span class="sxs-lookup"><span data-stu-id="48b5f-126">Package Streaming Methods</span></span>


<span data-ttu-id="48b5f-127">Sie müssen die Methode ermitteln, die Ihr Application Virtualization System zum Streamen der virtuellen Anwendungspakete oder SFT-Dateien vom Server an die Clients verwenden wird.</span><span class="sxs-lookup"><span data-stu-id="48b5f-127">You will need to determine the method your Application Virtualization System will use to stream the virtual application packages, or SFT files, from the server to the clients.</span></span> <span data-ttu-id="48b5f-128">Die folgenden Streaming-Optionen stehen zur Verfügung:</span><span class="sxs-lookup"><span data-stu-id="48b5f-128">The following streaming options are available:</span></span>

-   **<span data-ttu-id="48b5f-129">Application Virtualization Streaming Server.</span><span class="sxs-lookup"><span data-stu-id="48b5f-129">Application Virtualization Streaming Server.</span></span>** <span data-ttu-id="48b5f-130">Wenn Sie in Ihrer Konfiguration einen Application Virtualization Streaming Server verwenden, werden die SFT-Dateien über RTSP-oder RTSPS-Protokolle an die Clients von diesem Server gestreamt.</span><span class="sxs-lookup"><span data-stu-id="48b5f-130">If you use an Application Virtualization Streaming Server in your configuration, the SFT files are streamed to the clients from that server using RTSP or RTSPS protocols.</span></span> <span data-ttu-id="48b5f-131">Sie müssen die Server Software auf einem Computer installieren, und Sie müssen Sie über die Registrierung konfigurieren, aber diese Konfiguration ist nicht von Diensten wie SQL-oder Active Directory-Domänendiensten abhängig.</span><span class="sxs-lookup"><span data-stu-id="48b5f-131">You must install the server software on a computer and you must configure it through the registry, but this configuration does not depend on services such as SQL or Active Directory Domain Services.</span></span> <span data-ttu-id="48b5f-132">Die SFT-Dateien werden auf dem Server an einem Speicherort gespeichert, auf den die Clients zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="48b5f-132">The SFT files are stored on the server at a location accessible by the clients.</span></span> <span data-ttu-id="48b5f-133">Veröffentlichungsinformationen können über einen beliebigen Verteilungsmechanismus an die Clients verteilt werden.</span><span class="sxs-lookup"><span data-stu-id="48b5f-133">Publishing information can be distributed to the clients through any distribution mechanism.</span></span> <span data-ttu-id="48b5f-134">Bei der Konfiguration erhält der Client jedoch automatisch Paketaktualisierungen, und das aktive Upgrade wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="48b5f-134">However, when configured, the client receives package upgrades automatically and active upgrade is supported.</span></span>

-   **<span data-ttu-id="48b5f-135">Application Virtualization-Verwaltungs Server.</span><span class="sxs-lookup"><span data-stu-id="48b5f-135">Application Virtualization Management Server.</span></span>** <span data-ttu-id="48b5f-136">Wenn Sie in Ihrer Konfiguration einen Application Virtualization Management Server verwenden, werden die SFT-Dateien über RTSP-oder RTSPS-Protokolle an die Clients von diesem Server gestreamt.</span><span class="sxs-lookup"><span data-stu-id="48b5f-136">If you use an Application Virtualization Management Server in your configuration, the SFT files are streamed to the clients from that server using RTSP or RTSPS protocols.</span></span> <span data-ttu-id="48b5f-137">Sie können diesen Server über die Application Virtualization Management Console verwalten.</span><span class="sxs-lookup"><span data-stu-id="48b5f-137">You manage this server through the Application Virtualization Management Console.</span></span> <span data-ttu-id="48b5f-138">Diese Konfiguration verwendet eine SQL-Datenbank und Active Directory-Dienste.</span><span class="sxs-lookup"><span data-stu-id="48b5f-138">This configuration uses a SQL database and Active Directory services.</span></span> <span data-ttu-id="48b5f-139">Der Server kann Veröffentlichungsinformationen an die Clients verteilen, sodass keine zusätzlichen Veröffentlichungsmechanismen erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="48b5f-139">The server can distribute publishing information to the clients, so additional publishing mechanisms are not needed.</span></span>

-   **<span data-ttu-id="48b5f-140">Dateiserver.</span><span class="sxs-lookup"><span data-stu-id="48b5f-140">File server.</span></span>** <span data-ttu-id="48b5f-141">Wenn Sie einen Dateiserver in Ihrer Konfiguration verwenden, werden die SFT-Dateien mithilfe von SMB-Protokollen an die anderen Clientcomputer gestreamt.</span><span class="sxs-lookup"><span data-stu-id="48b5f-141">If you use a file server in your configuration, the SFT files are streamed to the other client computers by using SMB protocols.</span></span> <span data-ttu-id="48b5f-142">Die in dieser Konfiguration verwendeten Dateiserver werden verwaltet, indem Zugriffssteuerungslisten für die Dateifreigaben und SFT-Dateien erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="48b5f-142">File servers used in this configuration are managed by creating access control lists (ACLs) on the file shares and SFT files.</span></span> <span data-ttu-id="48b5f-143">Es muss darauf geachtet werden, dass die Clients an die richtigen Dateien auf dem Dateiserver weitergeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="48b5f-143">Care must be taken to direct the clients to the correct files on the file server.</span></span>

-   **<span data-ttu-id="48b5f-144">IIS-Server.</span><span class="sxs-lookup"><span data-stu-id="48b5f-144">IIS server.</span></span>** <span data-ttu-id="48b5f-145">Wenn Sie einen IIS-Server in Ihrer Konfiguration verwenden, werden die SFT-Dateien über HTTP-oder HTTPS-Protokolle an die Clients von diesem Server gestreamt.</span><span class="sxs-lookup"><span data-stu-id="48b5f-145">If you use an IIS server in your configuration, the SFT files are streamed to the clients from that server using HTTP or HTTPS protocols.</span></span> <span data-ttu-id="48b5f-146">Der IIS-Server kann einfach konfiguriert und verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="48b5f-146">The IIS server is easy to configure and manage.</span></span> <span data-ttu-id="48b5f-147">Es muss darauf geachtet werden, dass die Clients an die richtigen Dateien auf dem IIS-Server weitergeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="48b5f-147">Care must be taken to direct the clients to the correct files on the IIS server.</span></span>

<span data-ttu-id="48b5f-148">Ausführlichere Informationen zu den vorhergehenden Streaming-Methoden finden Sie unter [Ermitteln der Streaming-Methode](determine-your-streaming-method.md).</span><span class="sxs-lookup"><span data-stu-id="48b5f-148">For more detailed information about the preceding streaming methods, see [Determine Your Streaming Method](determine-your-streaming-method.md).</span></span>

## <span data-ttu-id="48b5f-149">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="48b5f-149">Related topics</span></span>


[<span data-ttu-id="48b5f-150">Befehlszeilenparameter von Application Virtualization Client Installer</span><span class="sxs-lookup"><span data-stu-id="48b5f-150">Application Virtualization Client Installer Command-Line Parameters</span></span>](application-virtualization-client-installer-command-line-parameters.md)

[<span data-ttu-id="48b5f-151">Application Virtualization Server-basiertes Szenario</span><span class="sxs-lookup"><span data-stu-id="48b5f-151">Application Virtualization Server-Based Scenario</span></span>](application-virtualization-server-based-scenario.md)

[<span data-ttu-id="48b5f-152">Bestimmen der Veröffentlichungsmethode</span><span class="sxs-lookup"><span data-stu-id="48b5f-152">Determine Your Publishing Method</span></span>](determine-your-publishing-method.md)

[<span data-ttu-id="48b5f-153">Bestimmen der Streaming-Methode</span><span class="sxs-lookup"><span data-stu-id="48b5f-153">Determine Your Streaming Method</span></span>](determine-your-streaming-method.md)

[<span data-ttu-id="48b5f-154">Electronic Software Distribution-basiertes Szenario</span><span class="sxs-lookup"><span data-stu-id="48b5f-154">Electronic Software Distribution-Based Scenario</span></span>](electronic-software-distribution-based-scenario.md)

[<span data-ttu-id="48b5f-155">SFTMIME-Befehlsreferenz</span><span class="sxs-lookup"><span data-stu-id="48b5f-155">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





