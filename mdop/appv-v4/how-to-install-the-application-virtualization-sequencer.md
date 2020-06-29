---
title: So installieren Sie Application Virtualization Sequencer
description: So installieren Sie Application Virtualization Sequencer
author: dansimp
ms.assetid: 89cdf60d-18b0-4204-aa9f-b402610f8f0e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 56a6fe03f2149504b6c34c70b2b82ce2ba0b55ad
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807055"
---
# <span data-ttu-id="0a650-103">So installieren Sie Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="0a650-103">How to Install the Application Virtualization Sequencer</span></span>


<span data-ttu-id="0a650-104">Der Microsoft Application Virtualization Sequencer überwacht und zeichnet den Installations-und Einrichtungsprozess für Anwendungen auf, damit die Anwendung als virtuelle Anwendung ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="0a650-104">The Microsoft Application Virtualization Sequencer monitors and records the installation and setup process for applications so that the application can be run as a virtual application.</span></span> <span data-ttu-id="0a650-105">Installieren Sie den Sequencer auf einem Computer, auf dem nur das Betriebssystem installiert ist.</span><span class="sxs-lookup"><span data-stu-id="0a650-105">You should install the Sequencer on a computer that has only the operating system installed.</span></span> <span data-ttu-id="0a650-106">Alternativ können Sie den Sequencer auf einem Computer mit einer virtuellen Umgebung installieren – beispielsweise Microsoft Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="0a650-106">Alternatively, you can install the Sequencer on a computer running a virtual environment—for example, Microsoft Virtual PC.</span></span> <span data-ttu-id="0a650-107">Diese Methode ist hilfreich, da es einfacher ist, eine saubere Sequenz Umgebung beizubehalten, die mit minimaler zusätzlicher Konfiguration wieder verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="0a650-107">This method is useful because it is easier to maintain a clean sequencing environment that can be reused with minimal additional configuration.</span></span>

<span data-ttu-id="0a650-108">Sie müssen über Administratorrechte auf dem Computer verfügen, den Sie zum Sequenzieren der Anwendung verwenden, und auf dem Computer darf keine Version des Application Virtualization (App-V)-Clients ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="0a650-108">You must have administrative rights on the computer you are using to sequence the application and the computer must not be running any version of the Application Virtualization (App-V) client.</span></span> <span data-ttu-id="0a650-109">Das Erstellen einer virtuellen Anwendung mithilfe des Sequencers ist sehr ressourcenintensiv, daher ist es wichtig, dass Sie den Sequencer auf einem Computer installieren, der die empfohlenen Anforderungen erfüllt oder überschreitet.</span><span class="sxs-lookup"><span data-stu-id="0a650-109">Creating a virtual application by using the Sequencer is very resource intensive, so it is important that you install the Sequencer on a computer that meets or exceeds the recommended requirements.</span></span> <span data-ttu-id="0a650-110">Das Ausführen des App-V-Sequencers im abgesicherten Modus wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0a650-110">Running the App-V sequencer in Safe Mode is not supported.</span></span> <span data-ttu-id="0a650-111">Weitere Informationen zu den Systemanforderungen finden Sie unter [Application Virtualization System Requirements](application-virtualization-system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="0a650-111">For more information about the system requirements, see [Application Virtualization System Requirements](application-virtualization-system-requirements.md).</span></span>

<span data-ttu-id="0a650-112">**Wichtig**  Nachdem Sie eine Anwendung sequenziert haben, müssen Sie das Betriebssystem und den Sequencer auf dem Computer, den Sie für die Sequenz Anwendung verwenden, erneut installieren, bevor Sie eine neue Anwendung ordnungsgemäß ablaufen können.</span><span class="sxs-lookup"><span data-stu-id="0a650-112">**Important** After you have sequenced an application, before you can properly sequence a new application you must reinstall the operating system and the Sequencer on the computer you are using to sequence applications.</span></span>

 

**<span data-ttu-id="0a650-113">So installieren Sie den Microsoft Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="0a650-113">To install the Microsoft Application Virtualization Sequencer</span></span>**

1.  <span data-ttu-id="0a650-114">Kopieren Sie die Installationsdateien von Microsoft Application Virtualization Sequencer auf den Computer, auf dem Sie Sie installieren möchten.</span><span class="sxs-lookup"><span data-stu-id="0a650-114">Copy the Microsoft Application Virtualization Sequencer installation files to the computer that you want to install it on.</span></span>

2.  <span data-ttu-id="0a650-115">Wählen Sie **setup.exe**aus, um den Installations-Assistenten für Microsoft Application Virtualization Sequencer zu starten.</span><span class="sxs-lookup"><span data-stu-id="0a650-115">To start the Microsoft Application Virtualization Sequencer installation wizard, select **setup.exe**.</span></span> <span data-ttu-id="0a650-116">Wenn das **Microsoft Visual C++ SP1-verteilbare Paket (x86)** vor der Installation nicht erkannt wird, wird es von **setup.exe** installiert.</span><span class="sxs-lookup"><span data-stu-id="0a650-116">If the **Microsoft Visual C++ SP1 Redistributable Package (x86)** is not detected prior to installation, **setup.exe** will install it.</span></span>

3.  <span data-ttu-id="0a650-117">Klicken Sie auf der Seite **Willkommen** auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="0a650-117">On the **Welcome** page, click **Next**.</span></span>

4.  <span data-ttu-id="0a650-118">Wenn Sie auf der Seite " **Lizenzvertrag** " die Bedingungen des Lizenzvertrags akzeptieren möchten, wählen Sie **Ich akzeptiere die Bedingungen des Lizenzvertrags**.</span><span class="sxs-lookup"><span data-stu-id="0a650-118">On the **License Agreement** page, to accept the terms of the license agreement, select **I accept the terms in the license agreement**.</span></span> <span data-ttu-id="0a650-119">Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="0a650-119">Click **Next**.</span></span>

5.  <span data-ttu-id="0a650-120">Klicken Sie auf der Seite **Zielordner** auf **weiter**, um den Standardinstallationsordner zu übernehmen.</span><span class="sxs-lookup"><span data-stu-id="0a650-120">On the **Destination Folder** page, to accept the default installation folder, click **Next**.</span></span> <span data-ttu-id="0a650-121">Wenn Sie einen anderen Zielordner angeben möchten, klicken Sie auf **ändern** , und geben Sie den Installationsordner an, der für die Installation verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0a650-121">To specify a different destination folder, click **Change** and specify the installation folder that will be used for the installation.</span></span> <span data-ttu-id="0a650-122">Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="0a650-122">Click **Next**.</span></span>

6.  <span data-ttu-id="0a650-123">Klicken Sie auf der Seite **bereit zum Installieren des Programms** auf **Installieren**, um die Installation zu starten.</span><span class="sxs-lookup"><span data-stu-id="0a650-123">On the **Ready to Install the Program** page, to start the installation, click **Install**.</span></span>

7.  <span data-ttu-id="0a650-124">Klicken Sie auf der Seite **abgeschlossen des InstallShield-Assistenten** auf **Fertig stellen**, um den Installations-Assistenten zu schließen und den Sequencer zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="0a650-124">On the **InstallShield Wizard Completed** page, to close the installation wizard and open the Sequencer, click **Finish**.</span></span> <span data-ttu-id="0a650-125">Wenn Sie den Installations-Assistenten schließen möchten, ohne den Sequencer zu öffnen, deaktivieren Sie **Programm starten** , und klicken Sie auf **Fertig stellen**.</span><span class="sxs-lookup"><span data-stu-id="0a650-125">To close the installation wizard without opening the Sequencer, deselect **Launch the program** and click **Finish**.</span></span>

## <span data-ttu-id="0a650-126">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="0a650-126">Related topics</span></span>


[<span data-ttu-id="0a650-127">So aktualisieren Sie Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="0a650-127">How to Upgrade the Application Virtualization Sequencer</span></span>](how-to-upgrade-the-application-virtualization-sequencer.md)

[<span data-ttu-id="0a650-128">Bereitstellungsanforderungen für Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="0a650-128">Application Virtualization Deployment Requirements</span></span>](application-virtualization-deployment-requirements.md)

 

 





