---
title: Installieren von Anwendungen auf einem virtuellen Windows-PC-Image
description: Installieren von Anwendungen auf einem virtuellen Windows-PC-Image
author: dansimp
ms.assetid: 32651eff-e3c6-4ef4-947d-2beddc695eac
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 9bf73fec0b33b37c2553dfe6f923917aa926b8e8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811992"
---
# <span data-ttu-id="1b7b2-103">Installieren von Anwendungen auf einem virtuellen Windows-PC-Image</span><span class="sxs-lookup"><span data-stu-id="1b7b2-103">Installing Applications on a Windows Virtual PC Image</span></span>


<span data-ttu-id="1b7b2-104">Nachdem Sie ein Windows Virtual PC-Abbild für die Verwendung mit Microsoft Enterprise Desktop Virtualization (Med-v) 2,0 erstellt haben, können Sie andere Komponenten installieren, die bei der Ausführung von Med-v hilfreich sind, beispielsweise ein ESD-System (Electronic Software Distribution) und eine Antivirus-Software.</span><span class="sxs-lookup"><span data-stu-id="1b7b2-104">After you have created a Windows Virtual PC image for use with Microsoft Enterprise Desktop Virtualization (MED-V) 2.0, you can install other components that are helpful when running MED-V, such as an electronic software distribution (ESD) system and antivirus software.</span></span>

<span data-ttu-id="1b7b2-105">Der folgende Abschnitt enthält Informationen, die Sie bei der Installation von Software auf dem MED-V-Abbild unterstützen.</span><span class="sxs-lookup"><span data-stu-id="1b7b2-105">The following section provides information to help you install software on the MED-V image.</span></span>

<span data-ttu-id="1b7b2-106">**Vorsicht**  Um die Verwaltung von Med-v Workspace nach der Bereitstellung zu vereinfachen, empfehlen wir, die Anzahl der Komponenten, die Sie auf dem Med-v-Abbild installieren, auf die Komponenten zu begrenzen, die erforderlich sind oder die bei Verwendung von Med-v hilfreich sind.</span><span class="sxs-lookup"><span data-stu-id="1b7b2-106">**Caution** For ease of MED-V workspace management after deployment, we recommend that you limit the number of components that you install on the MED-V image to those components that are required or that are helpful when using MED-V.</span></span> <span data-ttu-id="1b7b2-107">Wenn Sie beispielsweise nicht für med-v erforderlich sind, können Sie ein ESD-System installieren, um es später für die Installation von Anwendungen in einem Med-v-Arbeitsbereich und einer Antivirensoftware zur Sicherheit des Bilds zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="1b7b2-107">For example, although they are not required to run MED-V, you can install an ESD system to use later for installing applications to a MED-V workspace and antivirus software for security on the image.</span></span>

 

**<span data-ttu-id="1b7b2-108">Installieren von Software auf einem MED-V-Abbild</span><span class="sxs-lookup"><span data-stu-id="1b7b2-108">Installing Software on a MED-V Image</span></span>**

1.  <span data-ttu-id="1b7b2-109">Wenn es derzeit nicht ausgeführt wird, öffnen Sie den virtuellen MED-V-Computer.</span><span class="sxs-lookup"><span data-stu-id="1b7b2-109">If it is not currently running, open your MED-V virtual machine.</span></span>

    1.  <span data-ttu-id="1b7b2-110">Klicken Sie auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Windows Virtual PC** , und klicken Sie dann auf **Windows Virtual PC**.</span><span class="sxs-lookup"><span data-stu-id="1b7b2-110">Click **Start**, click **All Programs**, click **Windows Virtual PC** and then click **Windows Virtual PC**.</span></span>

    2.  <span data-ttu-id="1b7b2-111">Doppelklicken Sie auf den virtuellen MED-V-Computer.</span><span class="sxs-lookup"><span data-stu-id="1b7b2-111">Double-click your MED-V virtual machine.</span></span>

2.  <span data-ttu-id="1b7b2-112">Suchen Sie im Betriebssystem des virtuellen Computers die Installationsdateien für die Software, die Sie installieren möchten.</span><span class="sxs-lookup"><span data-stu-id="1b7b2-112">From inside the virtual machine operating system, locate the installation files for the software that you want to install.</span></span>

3.  <span data-ttu-id="1b7b2-113">Befolgen Sie die Installationsanweisungen, die vom Softwarehersteller bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="1b7b2-113">Follow the installation instructions that are provided by the software vendor.</span></span>

    <span data-ttu-id="1b7b2-114">**Hinweis**  Nachdem die Installation abgeschlossen ist, müssen Sie möglicherweise den virtuellen Computer schließen und neu starten.</span><span class="sxs-lookup"><span data-stu-id="1b7b2-114">**Note** After installation is complete, you might have to close and then restart the virtual machine.</span></span>

     

<span data-ttu-id="1b7b2-115">Wiederholen Sie diese Schritte für jede Software oder Anwendung, die Sie auf dem MED-V-Abbild installieren möchten.</span><span class="sxs-lookup"><span data-stu-id="1b7b2-115">Repeat these steps for any software or application that you want to install on the MED-V image.</span></span> <span data-ttu-id="1b7b2-116">Wir empfehlen, dass Sie die Anzahl der Anwendungen begrenzen, die Sie auf dem Bild vorinstallieren.</span><span class="sxs-lookup"><span data-stu-id="1b7b2-116">We recommend that you limit the number of applications that you preinstall on the image.</span></span> <span data-ttu-id="1b7b2-117">Die empfohlene Vorgehensweise zum Installieren von Anwendungen und anderer Software auf dem Bild besteht darin, jetzt ein ESD-System vorinstallieren und es später zum Bereitstellen von Software auf dem Bild zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="1b7b2-117">The recommended process for installing applications and other software on the image is to preinstall an ESD system now and to use it later to deploy software to the image.</span></span> <span data-ttu-id="1b7b2-118">Alternativ können Sie auch Gruppenrichtlinien oder App-v verwenden, um Anwendungen in einem Med-v-Arbeitsbereich hinzuzufügen oder zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="1b7b2-118">Alternately, you can also use Group Policy or App-V to add or remove applications on a MED-V workspace.</span></span> <span data-ttu-id="1b7b2-119">Weitere Informationen finden Sie unter [Verwalten von Anwendungen, die in MED-V-Arbeitsbereichen bereitgestellt werden](managing-applications-deployed-to-med-v-workspaces.md).</span><span class="sxs-lookup"><span data-stu-id="1b7b2-119">For more information, see [Managing Applications Deployed to MED-V Workspaces](managing-applications-deployed-to-med-v-workspaces.md).</span></span>

<span data-ttu-id="1b7b2-120">Weitere Informationen dazu, wie Sie Software auf einem virtuellen Bild installieren, finden Sie in den folgenden Artikeln:</span><span class="sxs-lookup"><span data-stu-id="1b7b2-120">For more information about how to install software on a virtual image, see the following articles:</span></span>

-   <span data-ttu-id="1b7b2-121">[Veröffentlichen und Verwenden von virtuellen Anwendungen](https://go.microsoft.com/fwlink/?LinkId=195926) ( https://go.microsoft.com/fwlink/?LinkId=195926) .</span><span class="sxs-lookup"><span data-stu-id="1b7b2-121">[Publish and Use Virtual Applications](https://go.microsoft.com/fwlink/?LinkId=195926) (https://go.microsoft.com/fwlink/?LinkId=195926).</span></span>

-   <span data-ttu-id="1b7b2-122">[Hilfe zu Windows Virtual PC](https://go.microsoft.com/fwlink/?LinkId=182378) ( https://go.microsoft.com/fwlink/?LinkId=182378) .</span><span class="sxs-lookup"><span data-stu-id="1b7b2-122">[Windows Virtual PC Help](https://go.microsoft.com/fwlink/?LinkId=182378) (https://go.microsoft.com/fwlink/?LinkId=182378).</span></span>

<span data-ttu-id="1b7b2-123">Nachdem Sie alle gewünschten Software auf dem MED-V-Bild installiert haben, kann Ihr Bild verpackt werden.</span><span class="sxs-lookup"><span data-stu-id="1b7b2-123">After you have installed all of the software that you want on the MED-V image, your image is ready to be packaged.</span></span>

## <span data-ttu-id="1b7b2-124">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="1b7b2-124">Related topics</span></span>


[<span data-ttu-id="1b7b2-125">Konfigurieren eines virtuellen Windows-PC-Images für MED-V</span><span class="sxs-lookup"><span data-stu-id="1b7b2-125">Configuring a Windows Virtual PC Image for MED-V</span></span>](configuring-a-windows-virtual-pc-image-for-med-v.md)

[<span data-ttu-id="1b7b2-126">Vorbereiten eines MED-V-Images</span><span class="sxs-lookup"><span data-stu-id="1b7b2-126">Prepare a MED-V Image</span></span>](prepare-a-med-v-image.md)

 

 





