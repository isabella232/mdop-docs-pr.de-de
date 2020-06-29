---
title: So laden Sie Dateien und Pakete
description: So laden Sie Dateien und Pakete
author: dansimp
ms.assetid: f86f5bf1-99a4-44d7-ae2f-e6049c482f68
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9427fd8089ec9c22d7d379b15ae94bf421ca2d44
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807027"
---
# <span data-ttu-id="14dc4-103">So laden Sie Dateien und Pakete</span><span class="sxs-lookup"><span data-stu-id="14dc4-103">How to Load Files and Packages</span></span>


<span data-ttu-id="14dc4-104">Mit dem folgenden Verfahren können Sie Dateien und Pakete auf Application Virtualization-Servern laden.</span><span class="sxs-lookup"><span data-stu-id="14dc4-104">You can use the following procedure to load files and packages on Application Virtualization Servers.</span></span>

<span data-ttu-id="14dc4-105">**Hinweis**  Während des Installationsvorgangs haben Sie den Speicherort des \\Content-Verzeichnisses auf der Seite " **Inhaltspfad** " angegeben.</span><span class="sxs-lookup"><span data-stu-id="14dc4-105">**Note** During the installation process, you specified the location of the \\Content directory on the **Content Path** page.</span></span> <span data-ttu-id="14dc4-106">Dieses Verzeichnis sollte als Standarddateifreigabe erstellt und konfiguriert werden, bevor Sie auf den Speicherort verweisen.</span><span class="sxs-lookup"><span data-stu-id="14dc4-106">This directory should be created and configured as a standard file share before you point to its location.</span></span>

 

**<span data-ttu-id="14dc4-107">So laden Sie Dateien und Pakete</span><span class="sxs-lookup"><span data-stu-id="14dc4-107">To load files and packages</span></span>**

1.  <span data-ttu-id="14dc4-108">Navigieren Sie auf dem Computer, von dem aus Anwendungen gestreamt werden sollen, zu dem Speicherort, den Sie für das \\Content-Verzeichnis angegeben haben.</span><span class="sxs-lookup"><span data-stu-id="14dc4-108">On the computer from which you will stream applications, navigate to the location that you specified for the \\Content directory.</span></span> <span data-ttu-id="14dc4-109">Erstellen Sie bei Bedarf das Verzeichnis, und konfigurieren Sie es als Standarddateifreigabe.</span><span class="sxs-lookup"><span data-stu-id="14dc4-109">If necessary, create the directory and configure it as a standard file share.</span></span>

2.  <span data-ttu-id="14dc4-110">Verschieben Sie die SFT-Dateien für die virtuellen Anwendungen und Pakete in das \\Content-Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="14dc4-110">Move the SFT files for the virtual applications and packages to the \\Content directory.</span></span> <span data-ttu-id="14dc4-111">Um die SFT-Dateien zu organisieren und Verwirrung zu vermeiden, fügen Sie Anwendungen und Pakete in dedizierte Unterordner ein.</span><span class="sxs-lookup"><span data-stu-id="14dc4-111">To keep the SFT files organized and to avoid confusion, put applications and packages in dedicated subfolders.</span></span>

3.  <span data-ttu-id="14dc4-112">Laden Sie die Anwendungen und Pakete entsprechend den Anforderungen Ihres Szenarios und ihrer Konfiguration unter Berücksichtigung der folgenden Bedingungen:</span><span class="sxs-lookup"><span data-stu-id="14dc4-112">Load the applications and packages according to the requirements of your scenario and configuration, considering the following conditions:</span></span>

    -   <span data-ttu-id="14dc4-113">Wenn Ihre Anwendungen und Pakete auf einem Application Virtualization (App-V)-Verwaltungs Server gespeichert sind, laden Sie Sie über die Verwaltungskonsole.</span><span class="sxs-lookup"><span data-stu-id="14dc4-113">If your applications and packages are stored on an Application Virtualization (App-V) Management Server, load them through the Management Console.</span></span> <span data-ttu-id="14dc4-114">Weitere Informationen finden Sie unter [so wird es gemacht: Laden oder Entladen einer Anwendung](how-to-load-or-unload-an-application.md) oder [Laden virtueller Anwendungen aus dem Desktop Benachrichtigungsbereich](how-to-load-virtual-applications-from-the-desktop-notification-area.md).</span><span class="sxs-lookup"><span data-stu-id="14dc4-114">For more information, see [How to Load or Unload an Application](how-to-load-or-unload-an-application.md) or [How to Load Virtual Applications from the Desktop Notification Area](how-to-load-virtual-applications-from-the-desktop-notification-area.md).</span></span>

    -   <span data-ttu-id="14dc4-115">Wenn Ihre Anwendungen auf einem App-V-Streamingserver, einem Webserver oder einem Computer gespeichert sind, der als Datei Server konfiguriert ist, können die Anwendungen automatisch geladen werden.</span><span class="sxs-lookup"><span data-stu-id="14dc4-115">If your applications are stored on an App-V Streaming Server, a Web server, or a computer configured as a file server, the applications can be automatically loaded.</span></span>

        <span data-ttu-id="14dc4-116">**Hinweis**  Der App-V-Streamingserver Ruft das \\Content-Verzeichnis automatisch auf Anwendungen und Pakete ab und fügt diese Informationen in den Arbeitsspeicher für Dienst Anwendungsanforderungen ein.</span><span class="sxs-lookup"><span data-stu-id="14dc4-116">**Note** The App-V Streaming Server automatically polls the \\Content directory for applications and packages and puts this information in RAM to service application requests.</span></span>

        <span data-ttu-id="14dc4-117">Die App-V-Clients müssen ordnungsgemäß konfiguriert sein, damit Anwendungen und Pakete von Webservern und Dateiservern abgerufen werden können.</span><span class="sxs-lookup"><span data-stu-id="14dc4-117">The App-V Clients must be properly configured to retrieve applications and packages from Web servers and file servers.</span></span> <span data-ttu-id="14dc4-118">Weitere Informationen finden Sie unter [Konfigurieren des Clients für das Abrufen von Anwendungspaketen](how-to-configure-the-client-for-application-package-retrieval.md).</span><span class="sxs-lookup"><span data-stu-id="14dc4-118">For more information, see [How to Configure the Client for Application Package Retrieval](how-to-configure-the-client-for-application-package-retrieval.md).</span></span>

         

## <span data-ttu-id="14dc4-119">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="14dc4-119">Related topics</span></span>


[<span data-ttu-id="14dc4-120">Application Virtualization Server</span><span class="sxs-lookup"><span data-stu-id="14dc4-120">Application Virtualization Server</span></span>](application-virtualization-server.md)

 

 





