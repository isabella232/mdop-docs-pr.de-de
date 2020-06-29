---
title: So installieren Sie den Sequencer
description: So installieren Sie den Sequencer
author: dansimp
ms.assetid: 2cd16427-a0ba-4870-82d1-3e3c79e1959b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 75a0f987fcc76d1ed92631085a4364ae6e06c9ce
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807039"
---
# <span data-ttu-id="46ef5-103">So installieren Sie den Sequencer</span><span class="sxs-lookup"><span data-stu-id="46ef5-103">How to Install the Sequencer</span></span>


<span data-ttu-id="46ef5-104">Der Microsoft Application Virtualization (App-V)-Sequenzer überwacht und zeichnet den Installations-und Einrichtungsprozess für Anwendungen auf, damit die Anwendung als virtuelle Anwendung ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="46ef5-104">The Microsoft Application Virtualization (App-V) Sequencer monitors and records the installation and setup process for applications so that the application can be run as a virtual application.</span></span> <span data-ttu-id="46ef5-105">Installieren Sie den Sequencer auf einem Computer, auf dem nur das Betriebssystem installiert ist.</span><span class="sxs-lookup"><span data-stu-id="46ef5-105">You should install the Sequencer on a computer that has only the operating system installed.</span></span> <span data-ttu-id="46ef5-106">Alternativ können Sie den Sequencer auf einem Computer mit einer virtuellen Umgebung installieren – beispielsweise Microsoft Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="46ef5-106">Alternatively, you can install the Sequencer on a computer running a virtual environment—for example, Microsoft Virtual PC.</span></span> <span data-ttu-id="46ef5-107">Diese Methode ist hilfreich, da es einfacher ist, eine saubere Sequenz Umgebung beizubehalten, die mit minimaler zusätzlicher Konfiguration wieder verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="46ef5-107">This method is useful because it is easier to maintain a clean sequencing environment that can be reused with minimal additional configuration.</span></span>

<span data-ttu-id="46ef5-108">Sie müssen über Administratorrechte auf dem Computer verfügen, den Sie verwenden, um die Anwendung zu sequenzieren, und der Computer muss mit dem Netzwerk verbunden sein.</span><span class="sxs-lookup"><span data-stu-id="46ef5-108">You must have administrative rights on the computer you are using to sequence the application and the computer must be connected to the network.</span></span> <span data-ttu-id="46ef5-109">Auf dem Computer darf keine Version des Application Virtualization (App-V)-Clients ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="46ef5-109">The computer must not be running any version of the Application Virtualization (App-V) client.</span></span> <span data-ttu-id="46ef5-110">Das Erstellen einer virtuellen Anwendung mithilfe des Sequencers ist sehr ressourcenintensiv, daher ist es wichtig, dass Sie den Sequencer auf einem Computer installieren, der die empfohlenen Anforderungen erfüllt oder überschreitet.</span><span class="sxs-lookup"><span data-stu-id="46ef5-110">Creating a virtual application using the Sequencer is very resource intensive, so it is important that you install the Sequencer on a computer that meets or exceeds the recommended requirements.</span></span> <span data-ttu-id="46ef5-111">Weitere Informationen zu den Systemanforderungen finden Sie unter [Hardware-und Software Anforderungen für Sequencer](sequencer-hardware-and-software-requirements.md)..</span><span class="sxs-lookup"><span data-stu-id="46ef5-111">For more information about the system requirements, see [Sequencer Hardware and Software Requirements](sequencer-hardware-and-software-requirements.md)..</span></span>

**<span data-ttu-id="46ef5-112">So installieren Sie den Microsoft Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="46ef5-112">To install the Microsoft Application Virtualization Sequencer</span></span>**

1.  <span data-ttu-id="46ef5-113">Kopieren Sie die Installationsdateien von Microsoft Application Virtualization Sequencer auf den Computer, auf dem Sie Sie installieren möchten.</span><span class="sxs-lookup"><span data-stu-id="46ef5-113">Copy the Microsoft Application Virtualization Sequencer installation files to the computer that you want to install it on.</span></span>

2.  <span data-ttu-id="46ef5-114">Wählen Sie **setup.exe**aus, um den Installations-Assistenten für Microsoft Application Virtualization Sequencer zu starten.</span><span class="sxs-lookup"><span data-stu-id="46ef5-114">To start the Microsoft Application Virtualization Sequencer installation wizard, select **setup.exe**.</span></span> <span data-ttu-id="46ef5-115">Wenn das **Microsoft Visual C++ SP1-verteilbare Paket (x86)** vor der Installation nicht erkannt wird, wird es von **setup.exe** installiert.</span><span class="sxs-lookup"><span data-stu-id="46ef5-115">If the **Microsoft Visual C++ SP1 Redistributable Package (x86)** is not detected prior to installation, **setup.exe** will install it.</span></span>

3.  <span data-ttu-id="46ef5-116">Klicken Sie auf der Seite **Willkommen** auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="46ef5-116">On the **Welcome** page, click **Next**.</span></span>

4.  <span data-ttu-id="46ef5-117">Wenn Sie auf der Seite " **Lizenzvertrag** " die Bedingungen des Lizenzvertrags akzeptieren möchten, wählen Sie **Ich akzeptiere die Bedingungen des Lizenzvertrags**.</span><span class="sxs-lookup"><span data-stu-id="46ef5-117">On the **License Agreement** page, to accept the terms of the license agreement, select **I accept the terms in the license agreement**.</span></span> <span data-ttu-id="46ef5-118">Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="46ef5-118">Click **Next**.</span></span>

5.  <span data-ttu-id="46ef5-119">Klicken Sie auf der Seite **Zielordner** auf **weiter**, um den Standardinstallationsordner zu übernehmen.</span><span class="sxs-lookup"><span data-stu-id="46ef5-119">On the **Destination Folder** page, to accept the default installation folder, click **Next**.</span></span> <span data-ttu-id="46ef5-120">Wenn Sie einen anderen Zielordner angeben möchten, klicken Sie auf **ändern** , und geben Sie den Installationsordner an, der für die Installation verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="46ef5-120">To specify a different destination folder, click **Change** and specify the installation folder that will be used for the installation.</span></span> <span data-ttu-id="46ef5-121">Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="46ef5-121">Click **Next**.</span></span>

6.  <span data-ttu-id="46ef5-122">Klicken Sie auf der Seite **bereit zum Installieren des Programms** auf **Installieren**, um die Installation zu starten.</span><span class="sxs-lookup"><span data-stu-id="46ef5-122">On the **Ready to Install the Program** page, to start the installation, click **Install**.</span></span>

7.  <span data-ttu-id="46ef5-123">Klicken Sie auf der Seite **abgeschlossen des InstallShield-Assistenten** auf **Fertig stellen**, um den Installations-Assistenten zu schließen und den Sequencer zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="46ef5-123">On the **InstallShield Wizard Completed** page, to close the installation wizard and open the Sequencer, click **Finish**.</span></span> <span data-ttu-id="46ef5-124">Wenn Sie den Installations-Assistenten schließen möchten, ohne den Sequencer zu öffnen, deaktivieren Sie **Programm starten** , und klicken Sie auf **Fertig stellen**.</span><span class="sxs-lookup"><span data-stu-id="46ef5-124">To close the installation wizard without opening the Sequencer, deselect **Launch the program** and click **Finish**.</span></span>

## <span data-ttu-id="46ef5-125">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="46ef5-125">Related topics</span></span>


[<span data-ttu-id="46ef5-126">Konfigurieren von Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="46ef5-126">Configuring the Application Virtualization Sequencer</span></span>](configuring-the-application-virtualization-sequencer.md)

 

 





