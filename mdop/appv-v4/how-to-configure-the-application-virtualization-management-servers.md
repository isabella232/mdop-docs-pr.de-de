---
title: So konfigurieren Sie Anwendung Virtualisierung Management Server
description: So konfigurieren Sie Anwendung Virtualisierung Management Server
author: dansimp
ms.assetid: a9f96148-bf2d-486f-98c2-23409bfb0935
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d6d54dd213efb8d5cbff5d0e730e6dc08c8d19b1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807268"
---
# <span data-ttu-id="74ccd-103">So konfigurieren Sie Anwendung Virtualisierung Management Server</span><span class="sxs-lookup"><span data-stu-id="74ccd-103">How to Configure the Application Virtualization Management Servers</span></span>


<span data-ttu-id="74ccd-104">Bevor virtualisierte Anwendungen an den Application Virtualization-Desktop Client oder den Client für Remote Desktop Dienste (vormals Terminal Dienste) gestreamt werden können, muss der Application Virtualization-Verwaltungs Server konfiguriert sein.</span><span class="sxs-lookup"><span data-stu-id="74ccd-104">Before virtualized applications can be streamed to the Application Virtualization Desktop Client or the Client for Remote Desktop Services (formerly Terminal Services), the Application Virtualization Management Server must be configured.</span></span> <span data-ttu-id="74ccd-105">Wenn Sie den Server konfigurieren, richten Sie das *Inhaltsverzeichnis* ein, in dem die SFT-Dateien geladen und gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="74ccd-105">When you configure the server, you are setting up the *content directory* where the SFT files are loaded and stored.</span></span> <span data-ttu-id="74ccd-106">Die SFT-Dateien enthalten die virtualisierte Anwendung (oder Anwendungen).</span><span class="sxs-lookup"><span data-stu-id="74ccd-106">The SFT files contain the virtualized application (or applications).</span></span>

<span data-ttu-id="74ccd-107">**Wichtig**  Application Virtualization-Server streamen SFT-Dateien mit nur RTSP-oder RTSPS-Protokollen an den Desktop Client und den Client für Remote Desktop Dienste.</span><span class="sxs-lookup"><span data-stu-id="74ccd-107">**Important** Application Virtualization Servers stream SFT files to the Desktop Client and the Client for Remote Desktop Services using only RTSP or RTSPS protocols.</span></span> <span data-ttu-id="74ccd-108">Die ICO-Datei (Symbol) und die OSD-Datei (Open Software Descriptor) können so konfiguriert werden, dass Sie von einer anderen Datei oder einem anderen HTTP-Server gestreamt wird.</span><span class="sxs-lookup"><span data-stu-id="74ccd-108">The ICO (icon) file and the OSD (open software descriptor) file can be configured to stream from a different file or HTTP server.</span></span>

 

**<span data-ttu-id="74ccd-109">So konfigurieren Sie den Application Virtualization-Verwaltungs Server</span><span class="sxs-lookup"><span data-stu-id="74ccd-109">To configure the Application Virtualization Management Server</span></span>**

1.  <span data-ttu-id="74ccd-110">Führen Sie die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="74ccd-110">Complete the following procedure:</span></span>

    [<span data-ttu-id="74ccd-111">So installieren Sie Application Virtualization Management Server</span><span class="sxs-lookup"><span data-stu-id="74ccd-111">How to Install Application Virtualization Management Server</span></span>](how-to-install-application-virtualization-management-server.md)

    <span data-ttu-id="74ccd-112">**Hinweis**  Während des Installationsvorgangs geben Sie den Speicherort des \\Content-Verzeichnisses auf dem Bildschirm " **Inhaltspfad** " an.</span><span class="sxs-lookup"><span data-stu-id="74ccd-112">**Note** During the installation procedure, you specify the location of the \\Content directory on the **Content Path** screen.</span></span>

     

2.  <span data-ttu-id="74ccd-113">Navigieren Sie zu dem Speicherort, den Sie für das \\Content-Verzeichnis angegeben haben, und erstellen Sie bei Bedarf das Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="74ccd-113">Navigate to the location that you specified for the \\Content directory, and if necessary, create the directory.</span></span>

3.  <span data-ttu-id="74ccd-114">Wenn das Inhaltsverzeichnis erstellt wird, konfigurieren Sie dieses Verzeichnis als Standarddateifreigabe.</span><span class="sxs-lookup"><span data-stu-id="74ccd-114">When the content directory is created, configure this directory as a standard file share.</span></span>

## <span data-ttu-id="74ccd-115">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="74ccd-115">Related topics</span></span>


[<span data-ttu-id="74ccd-116">Application Virtualization Server-basiertes Szenario</span><span class="sxs-lookup"><span data-stu-id="74ccd-116">Application Virtualization Server-Based Scenario</span></span>](application-virtualization-server-based-scenario.md)

[<span data-ttu-id="74ccd-117">Systemanforderungen für Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="74ccd-117">Application Virtualization System Requirements</span></span>](application-virtualization-system-requirements.md)

[<span data-ttu-id="74ccd-118">Electronic Software Distribution-basiertes Szenario</span><span class="sxs-lookup"><span data-stu-id="74ccd-118">Electronic Software Distribution-Based Scenario</span></span>](electronic-software-distribution-based-scenario.md)

[<span data-ttu-id="74ccd-119">So konfigurieren Sie Server für die serverbasierte Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="74ccd-119">How to Configure Servers for Server-Based Deployment</span></span>](how-to-configure-servers-for-server-based-deployment.md)

 

 





