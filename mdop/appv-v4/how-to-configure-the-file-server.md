---
title: So konfigurieren Sie den Dateiserver
description: So konfigurieren Sie den Dateiserver
author: dansimp
ms.assetid: 0977554c-1741-411b-85e7-7e1cd017542f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8a8971ad5c9f83dec4d0c77a16f1093ef7026b5c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807244"
---
# <span data-ttu-id="e7ecc-103">So konfigurieren Sie den Dateiserver</span><span class="sxs-lookup"><span data-stu-id="e7ecc-103">How to Configure the File Server</span></span>


<span data-ttu-id="e7ecc-104">Mit dem folgenden Verfahren können Sie einen lokalen Computer konfigurieren, der als Dateifreigabe-und Datenstrom Anwendungen für den Application Virtualization-Desktop Client und den Client für Remote Desktop Dienste (vormals Terminal Dienste) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e7ecc-104">You can use the following procedure to configure a local computer that is used as a file share and streams applications to the Application Virtualization Desktop Client and the Client for Remote Desktop Services (formerly Terminal Services).</span></span> <span data-ttu-id="e7ecc-105">Dieses Szenario wird verwendet, wenn Sie Ihrer vorhandenen Hardwareumgebung keine zusätzliche Serverinfrastruktur hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="e7ecc-105">This scenario is used when you do not want to add an additional server infrastructure to your existing hardware environment.</span></span>

<span data-ttu-id="e7ecc-106">Wenn Sie einen Application Virtualization Management Server als Verteilungspunkt für die Dateifreigabe verwenden, die in lokalen Niederlassungen installiert ist, müssen Sie diesen Server konfigurieren, bevor virtuelle Anwendungen auf die Computer gestreamt werden können, die als Dateifreigaben verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e7ecc-106">If you are using an Application Virtualization Management Server as a distribution point to the file share installed in local offices, you must configure this server before virtual applications can be streamed to the computers that are used as file shares.</span></span> <span data-ttu-id="e7ecc-107">Wenn Sie die Server und die Dateifreigaben konfigurieren, müssen Sie das Inhaltsverzeichnis einrichten, in dem die SFT-Dateien geladen und gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="e7ecc-107">When you configure the servers and the file shares, you are setting up the content directory where the SFT files are loaded and stored.</span></span> <span data-ttu-id="e7ecc-108">Die SFT-Dateien enthalten die virtuelle Anwendung (oder Anwendungen).</span><span class="sxs-lookup"><span data-stu-id="e7ecc-108">The SFT files contain the virtual application (or applications).</span></span>

<span data-ttu-id="e7ecc-109">**Wichtig**  Damit Anwendungen ordnungsgemäß an den Application Virtualization-Desktop Client und den Client für Remote Desktop Dienste gestreamt werden können, strömt die SFT-Datei aus dem Inhaltsverzeichnis auf dem Server, auf dem Sie die virtuelle Anwendung speichern, aus. die ICO-Datei (Symbol) und die OSD-Datei (Open Software Descriptor) können so konfiguriert werden, dass Sie von einem anderen Server gestreamt wird.</span><span class="sxs-lookup"><span data-stu-id="e7ecc-109">**Important** For applications to stream properly to the Application Virtualization Desktop Client and the Client for Remote Desktop Services, the SFT file streams from the content directory on the server where you store the virtual application; the ICO (icon) file and the OSD (open software descriptor) file can be configured to stream from a different server.</span></span>

 

**<span data-ttu-id="e7ecc-110">So konfigurieren Sie den Application Virtualization-Dateiserver</span><span class="sxs-lookup"><span data-stu-id="e7ecc-110">To configure the Application Virtualization file server</span></span>**

1.  <span data-ttu-id="e7ecc-111">Führen Sie das folgende Installationsverfahren aus, um den als Verteilungspunkt verwendeten Server zu konfigurieren:</span><span class="sxs-lookup"><span data-stu-id="e7ecc-111">Complete the following installation procedure to configure the server that is used as the distribution point:</span></span>

    [<span data-ttu-id="e7ecc-112">So installieren Sie Application Virtualization Management Server</span><span class="sxs-lookup"><span data-stu-id="e7ecc-112">How to Install Application Virtualization Management Server</span></span>](how-to-install-application-virtualization-management-server.md)

    <span data-ttu-id="e7ecc-113">**Hinweis**  Während des Installationsvorgangs geben Sie den Speicherort des \\Content-Verzeichnisses auf dem Bildschirm " **Inhaltspfad** " an.</span><span class="sxs-lookup"><span data-stu-id="e7ecc-113">**Note** During the installation procedure, you specify the location of the \\Content directory on the **Content Path** screen.</span></span>

     

2.  <span data-ttu-id="e7ecc-114">Erstellen Sie auf jedem Computer, den Sie als Dateifreigabe verwenden, ein \\Content-Verzeichnis, das dem beim Installieren des Servers angegebenen Verzeichnis entspricht.</span><span class="sxs-lookup"><span data-stu-id="e7ecc-114">Create a \\Content directory, which corresponds to the directory you specified when you installed the server, on each computer that you are using as a file share.</span></span>

    <span data-ttu-id="e7ecc-115">**Wichtig**  Konfigurieren Sie die Application Virtualization-Desktop Clients so, dass Anwendungen von dem Computer, den Sie als Dateifreigabe verwenden, und nicht von einem Application Virtualization Server oder IIS-Server gestreamt werden.</span><span class="sxs-lookup"><span data-stu-id="e7ecc-115">**Important** Configure the Application Virtualization Desktop Clients to stream applications from the computer you are using as a file share rather than from an Application Virtualization Server or IIS server.</span></span>

     

3.  <span data-ttu-id="e7ecc-116">Wenn das \\Content-Verzeichnis erstellt wird, konfigurieren Sie dieses Verzeichnis als Standarddateifreigabe.</span><span class="sxs-lookup"><span data-stu-id="e7ecc-116">When the \\Content directory is created, configure this directory as a standard file share.</span></span>

## <span data-ttu-id="e7ecc-117">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="e7ecc-117">Related topics</span></span>


[<span data-ttu-id="e7ecc-118">Application Virtualization Server-basiertes Szenario</span><span class="sxs-lookup"><span data-stu-id="e7ecc-118">Application Virtualization Server-Based Scenario</span></span>](application-virtualization-server-based-scenario.md)

[<span data-ttu-id="e7ecc-119">Electronic Software Distribution-basiertes Szenario</span><span class="sxs-lookup"><span data-stu-id="e7ecc-119">Electronic Software Distribution-Based Scenario</span></span>](electronic-software-distribution-based-scenario.md)

[<span data-ttu-id="e7ecc-120">So konfigurieren Sie Anwendung Virtualisierung Management Server</span><span class="sxs-lookup"><span data-stu-id="e7ecc-120">How to Configure the Application Virtualization Management Servers</span></span>](how-to-configure-the-application-virtualization-management-servers.md)

[<span data-ttu-id="e7ecc-121">So konfigurieren Sie Application Virtualization Streaming Server</span><span class="sxs-lookup"><span data-stu-id="e7ecc-121">How to Configure the Application Virtualization Streaming Servers</span></span>](how-to-configure-the-application-virtualization-streaming-servers.md)

[<span data-ttu-id="e7ecc-122">So konfigurieren Sie den Server für IIS</span><span class="sxs-lookup"><span data-stu-id="e7ecc-122">How to Configure the Server for IIS</span></span>](how-to-configure-the-server-for-iis.md)

 

 





