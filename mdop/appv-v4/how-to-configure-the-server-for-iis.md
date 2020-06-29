---
title: So konfigurieren Sie den Server für IIS
description: So konfigurieren Sie den Server für IIS
author: dansimp
ms.assetid: 1fcfc583-322f-4a38-90d0-e64bfa9ee3d8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9fe3367698b6f387d4467afdad1b3e17211134d6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807228"
---
# <span data-ttu-id="8a7f9-103">So konfigurieren Sie den Server für IIS</span><span class="sxs-lookup"><span data-stu-id="8a7f9-103">How to Configure the Server for IIS</span></span>


<span data-ttu-id="8a7f9-104">Bevor virtuelle Anwendungen an den Application Virtualization-Desktop Client und den Client für Remote Desktop Dienste (vormals Terminal Dienste) gestreamt werden können, müssen die IIS-Server konfiguriert sein.</span><span class="sxs-lookup"><span data-stu-id="8a7f9-104">Before virtual applications can be streamed to the Application Virtualization Desktop Client and the Client for Remote Desktop Services (formerly Terminal Services), the IIS servers must be configured.</span></span> <span data-ttu-id="8a7f9-105">Wenn Sie die Server konfigurieren, richten Sie das Inhaltsverzeichnis ein, in dem die SFT-Dateien geladen und gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="8a7f9-105">When you configure the servers, you are setting up the content directory where the SFT files are loaded and stored.</span></span> <span data-ttu-id="8a7f9-106">Die SFT-Dateien enthalten die virtuelle Anwendung (oder Anwendungen).</span><span class="sxs-lookup"><span data-stu-id="8a7f9-106">The SFT files contain the virtual application (or applications).</span></span>

**<span data-ttu-id="8a7f9-107">So konfigurieren Sie das Inhaltsverzeichnis auf dem IIS-Server</span><span class="sxs-lookup"><span data-stu-id="8a7f9-107">To configure the content directory on the IIS server</span></span>**

1.  <span data-ttu-id="8a7f9-108">Suchen Sie auf dem Server, auf dem IIS ausgeführt wird, nach dem Verzeichnis, das Sie als Inhaltsverzeichnis verwenden möchten, oder erstellen Sie das Verzeichnis, falls es nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="8a7f9-108">On the server that is running IIS, locate the directory that you want to use as the content directory, or create the directory if it does not exist.</span></span> <span data-ttu-id="8a7f9-109">Konfigurieren Sie dieses Verzeichnis als Standarddateifreigabe.</span><span class="sxs-lookup"><span data-stu-id="8a7f9-109">Configure this directory as a standard file share.</span></span>

2.  <span data-ttu-id="8a7f9-110">Öffnen Sie auf dem Server, auf dem IIS ausgeführt wird, **IIS-Manager**, und erstellen Sie unter der Standardwebsite ein virtuelles Verzeichnis, das dem Inhaltsverzeichnis entspricht, das Sie auf dem Server erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="8a7f9-110">On the server that is running IIS, open **IIS Manager**, and under the default website, create a virtual directory that corresponds to the content directory that you created on the server.</span></span> <span data-ttu-id="8a7f9-111">Vergewissern Sie sich, dass " **Lesen** " aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="8a7f9-111">Make sure that **Read** is checked.</span></span>

3.  <span data-ttu-id="8a7f9-112">Geben Sie dem neu erstellten virtuellen Verzeichnis den Alias **Inhalt**.</span><span class="sxs-lookup"><span data-stu-id="8a7f9-112">Give the newly created virtual directory the alias **Content**.</span></span>

4.  <span data-ttu-id="8a7f9-113">Akzeptieren Sie alle anderen Standardeinstellungen für dieses virtuelle Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="8a7f9-113">Accept all other default settings for this virtual directory.</span></span>

5.  <span data-ttu-id="8a7f9-114">Konfigurieren Sie die NTFS-Dateisystemberechtigungen für das Inhaltsverzeichnis und die Paketordner unter dem Inhaltsverzeichnis, indem Sie die Sicherheitsgruppen in den Active Directory-Domänendiensten verwenden, die Sie zuvor definiert haben.</span><span class="sxs-lookup"><span data-stu-id="8a7f9-114">Configure the NTFS file system permissions to the content directory and the package folders under the content directory by using the Security Groups in Active Directory Domain Services that you defined earlier.</span></span>

<span data-ttu-id="8a7f9-115">**Hinweis**  Wenn Sie IIS zum Veröffentlichen der ICO-und OSD-Dateien verwenden, müssen Sie einen MIME-Typ für OSD = txt konfigurieren. Andernfalls dient IIS nicht für die ICO-und OSD-Dateien für Clients.</span><span class="sxs-lookup"><span data-stu-id="8a7f9-115">**Note** If you are using IIS to publish the ICO and OSD files, you must configure a MIME type for OSD=TXT; otherwise, IIS will not serve the ICO and OSD files to clients.</span></span> <span data-ttu-id="8a7f9-116">Wenn Sie IIS zum Veröffentlichen von Paketen (SFT-Dateien) verwenden, müssen Sie einen MIME-Typ für SFT = Binary konfigurieren. Andernfalls dient IIS nicht für die SFT-Dateien für Clients.</span><span class="sxs-lookup"><span data-stu-id="8a7f9-116">If you are using IIS to publish packages (SFT files), you must configure a MIME type for SFT=Binary; otherwise, IIS will not serve the SFT files to clients.</span></span>

 

## <span data-ttu-id="8a7f9-117">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="8a7f9-117">Related topics</span></span>


[<span data-ttu-id="8a7f9-118">Application Virtualization Server-basiertes Szenario</span><span class="sxs-lookup"><span data-stu-id="8a7f9-118">Application Virtualization Server-Based Scenario</span></span>](application-virtualization-server-based-scenario.md)

[<span data-ttu-id="8a7f9-119">Electronic Software Distribution-basiertes Szenario</span><span class="sxs-lookup"><span data-stu-id="8a7f9-119">Electronic Software Distribution-Based Scenario</span></span>](electronic-software-distribution-based-scenario.md)

[<span data-ttu-id="8a7f9-120">So konfigurieren Sie Anwendung Virtualisierung Management Server</span><span class="sxs-lookup"><span data-stu-id="8a7f9-120">How to Configure the Application Virtualization Management Servers</span></span>](how-to-configure-the-application-virtualization-management-servers.md)

[<span data-ttu-id="8a7f9-121">So konfigurieren Sie Application Virtualization Streaming Server</span><span class="sxs-lookup"><span data-stu-id="8a7f9-121">How to Configure the Application Virtualization Streaming Servers</span></span>](how-to-configure-the-application-virtualization-streaming-servers.md)

[<span data-ttu-id="8a7f9-122">So konfigurieren Sie den Dateiserver</span><span class="sxs-lookup"><span data-stu-id="8a7f9-122">How to Configure the File Server</span></span>](how-to-configure-the-file-server.md)

 

 





