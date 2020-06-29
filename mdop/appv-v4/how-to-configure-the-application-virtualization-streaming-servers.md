---
title: So konfigurieren Sie Application Virtualization Streaming Server
description: So konfigurieren Sie Application Virtualization Streaming Server
author: dansimp
ms.assetid: 3e2dde35-9d72-40ba-9fdf-d0338bd4d561
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a0ec5497b010d18bcba60e81e96cbe6334c27fb8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807260"
---
# <span data-ttu-id="32bfc-103">So konfigurieren Sie Application Virtualization Streaming Server</span><span class="sxs-lookup"><span data-stu-id="32bfc-103">How to Configure the Application Virtualization Streaming Servers</span></span>


<span data-ttu-id="32bfc-104">Bevor virtuelle Anwendungen an den Application Virtualization-Desktop Client oder den Client für Remote Desktop Dienste (vormals Terminal Dienste) gestreamt werden können, müssen die Application Virtualization Streaming-Server konfiguriert sein.</span><span class="sxs-lookup"><span data-stu-id="32bfc-104">Before virtual applications can be streamed to the Application Virtualization Desktop Client or the Client for Remote Desktop Services (formerly Terminal Services), the Application Virtualization Streaming Servers must be configured.</span></span> <span data-ttu-id="32bfc-105">Wenn Sie die Server konfigurieren, richten Sie das *Inhaltsverzeichnis* ein, in dem die SFT-Dateien geladen und gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="32bfc-105">When you configure the servers, you are setting up the *content directory* where the SFT files are loaded and stored.</span></span> <span data-ttu-id="32bfc-106">Die SFT-Dateien enthalten die virtuelle Anwendung (oder Anwendungen).</span><span class="sxs-lookup"><span data-stu-id="32bfc-106">The SFT files contain the virtual application (or applications).</span></span>

<span data-ttu-id="32bfc-107">**Wichtig**  Application Virtualization-Server streamen SFT-Dateien mit nur RTSP-oder RTSPS-Protokollen an den Desktop Client und den Client für Remote Desktop Dienste.</span><span class="sxs-lookup"><span data-stu-id="32bfc-107">**Important** Application Virtualization Servers stream SFT files to the Desktop Client and the Client for Remote Desktop Services using only RTSP or RTSPS protocols.</span></span> <span data-ttu-id="32bfc-108">Die ICO-Datei (Symbol) und die OSD-Datei (Open Software Descriptor) können so konfiguriert werden, dass Sie von einer anderen Datei oder einem anderen HTTP-Server gestreamt wird.</span><span class="sxs-lookup"><span data-stu-id="32bfc-108">The ICO (icon) file and the OSD (open software descriptor) file can be configured to stream from a different file or HTTP server.</span></span>

 

**<span data-ttu-id="32bfc-109">So konfigurieren Sie die Application Virtualization Streaming Server</span><span class="sxs-lookup"><span data-stu-id="32bfc-109">To configure the Application Virtualization Streaming Servers</span></span>**

1.  <span data-ttu-id="32bfc-110">Führen Sie das Installationsverfahren für den Application Virtualization Streaming Server aus.</span><span class="sxs-lookup"><span data-stu-id="32bfc-110">Complete the installation procedure for the Application Virtualization Streaming Server.</span></span> <span data-ttu-id="32bfc-111">Während des Installationsvorgangs geben Sie den Speicherort des \\Content-Verzeichnisses auf dem Bildschirm " **Inhaltspfad** " an.</span><span class="sxs-lookup"><span data-stu-id="32bfc-111">During the installation procedure, you specify the location of the \\Content directory on the **Content Path** screen.</span></span>

2.  <span data-ttu-id="32bfc-112">Navigieren Sie zu dem Speicherort, den Sie für das \\Content-Verzeichnis angegeben haben, und erstellen Sie bei Bedarf das Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="32bfc-112">Navigate to the location that you specified for the \\Content directory, and if you have to, create the directory.</span></span>

3.  <span data-ttu-id="32bfc-113">Wenn das Inhaltsverzeichnis erstellt wird, konfigurieren Sie dieses Verzeichnis als Standarddateifreigabe.</span><span class="sxs-lookup"><span data-stu-id="32bfc-113">When the Content directory is created, configure this directory as a standard file share.</span></span>

4.  <span data-ttu-id="32bfc-114">Konfigurieren Sie die NTFS-Dateisystemberechtigungen für das Inhaltsverzeichnis und die Paketordner unter dem Inhaltsverzeichnis.</span><span class="sxs-lookup"><span data-stu-id="32bfc-114">Configure the NTFS file system permissions to the Content directory and the package folders under the Content directory.</span></span> <span data-ttu-id="32bfc-115">Sie sollten Sicherheitsgruppen in Active Directory-Domänendiensten verwenden, die definieren, welche Benutzer auf jede Anwendung zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="32bfc-115">You should use Security Groups in Active Directory Domain Services that define which users can access each application.</span></span>

## <span data-ttu-id="32bfc-116">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="32bfc-116">Related topics</span></span>


[<span data-ttu-id="32bfc-117">Application Virtualization Server-basiertes Szenario</span><span class="sxs-lookup"><span data-stu-id="32bfc-117">Application Virtualization Server-Based Scenario</span></span>](application-virtualization-server-based-scenario.md)

[<span data-ttu-id="32bfc-118">Electronic Software Distribution-basiertes Szenario</span><span class="sxs-lookup"><span data-stu-id="32bfc-118">Electronic Software Distribution-Based Scenario</span></span>](electronic-software-distribution-based-scenario.md)

[<span data-ttu-id="32bfc-119">So konfigurieren Sie Anwendung Virtualisierung Management Server</span><span class="sxs-lookup"><span data-stu-id="32bfc-119">How to Configure the Application Virtualization Management Servers</span></span>](how-to-configure-the-application-virtualization-management-servers.md)

[<span data-ttu-id="32bfc-120">So konfigurieren Sie den Dateiserver</span><span class="sxs-lookup"><span data-stu-id="32bfc-120">How to Configure the File Server</span></span>](how-to-configure-the-file-server.md)

[<span data-ttu-id="32bfc-121">So konfigurieren Sie den Server für IIS</span><span class="sxs-lookup"><span data-stu-id="32bfc-121">How to Configure the Server for IIS</span></span>](how-to-configure-the-server-for-iis.md)

 

 





