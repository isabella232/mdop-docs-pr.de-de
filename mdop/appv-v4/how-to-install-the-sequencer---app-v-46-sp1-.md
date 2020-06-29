---
title: Installieren des Sequencer (App-V 4,6 SP1)
description: Installieren des Sequencer (App-V 4,6 SP1)
author: dansimp
ms.assetid: fe8eb876-28fb-46ae-b592-da055107e639
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 611564e861d65dcd357c58732fb60dab21c05abe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807040"
---
# <span data-ttu-id="459b2-103">Installieren des Sequencer (App-V 4,6 SP1)</span><span class="sxs-lookup"><span data-stu-id="459b2-103">How to Install the Sequencer (App-V 4.6 SP1)</span></span>


<span data-ttu-id="459b2-104">Der Microsoft Application Virtualization (App-V)-Sequenzer überwacht und zeichnet den Installations-und Einrichtungsprozess für Anwendungen auf, damit die Anwendung als virtuelle Anwendung ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="459b2-104">The Microsoft Application Virtualization (App-V) Sequencer monitors and records the installation and setup process for applications so that the application can be run as a virtual application.</span></span> <span data-ttu-id="459b2-105">Installieren Sie den App-V-Sequencer auf einem Computer, auf dem nur das Betriebssystem installiert ist.</span><span class="sxs-lookup"><span data-stu-id="459b2-105">You should install the App-V Sequencer on a computer that has only the operating system installed.</span></span> <span data-ttu-id="459b2-106">Alternativ können Sie den Sequencer auf einem Computer installieren, der in einer virtuellen Umgebung ausgeführt wird, beispielsweise einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="459b2-106">Alternatively, you can install the Sequencer on a computer running in a virtual environment, for example, a virtual computer.</span></span> <span data-ttu-id="459b2-107">Diese Methode ist hilfreich, da es einfacher ist, eine saubere Sequenz Umgebung beizubehalten, die Sie mit minimaler zusätzlicher Konfiguration wieder verwenden können.</span><span class="sxs-lookup"><span data-stu-id="459b2-107">This method is useful because it is easier to maintain a clean sequencing environment that you can reuse with minimal additional configuration.</span></span>

<span data-ttu-id="459b2-108">Sie müssen über Administratorrechte auf dem Computer verfügen, den Sie zum Sequenzieren der Anwendung verwenden, und auf dem Computer darf keine Version von App-V Client ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="459b2-108">You must have administrative credentials on the computer you are using to sequence the application, and the computer must not be running any version of App-V client.</span></span> <span data-ttu-id="459b2-109">Das Erstellen einer virtuellen Anwendung mit dem App-V-Sequencer erfordert mehrere Vorgänge, daher ist es wichtig, dass Sie den Sequencer auf einem Computer installieren, der die [Hardware-und Software Anforderungen für Application Virtualization Sequencer](application-virtualization-sequencer-hardware-and-software-requirements.md)erfüllt oder überschreitet.</span><span class="sxs-lookup"><span data-stu-id="459b2-109">Creating a virtual application by using the App-V Sequencer requires multiple operations, so it is important that you install the Sequencer on a computer that meets or exceeds the [Application Virtualization Sequencer Hardware and Software Requirements](application-virtualization-sequencer-hardware-and-software-requirements.md).</span></span>

**<span data-ttu-id="459b2-110">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="459b2-110">Note</span></span>**  
<span data-ttu-id="459b2-111">Das Ausführen des App-V-Sequencers im abgesicherten Modus wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="459b2-111">Running the App-V sequencer in Safe Mode is not supported.</span></span>



**<span data-ttu-id="459b2-112">So installieren Sie den Microsoft Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="459b2-112">To install the Microsoft Application Virtualization Sequencer</span></span>**

1.  <span data-ttu-id="459b2-113">Kopieren Sie die Installationsdateien von Microsoft Application Virtualization Sequencer auf den Computer, auf dem Sie Sie installieren möchten.</span><span class="sxs-lookup"><span data-stu-id="459b2-113">Copy the Microsoft Application Virtualization Sequencer installation files to the computer on which you want to install it.</span></span>

2.  <span data-ttu-id="459b2-114">Doppelklicken Sie auf **Setup.exe**, um den Installations-Assistenten für Microsoft Application Virtualization Sequencer zu starten.</span><span class="sxs-lookup"><span data-stu-id="459b2-114">To start the Microsoft Application Virtualization Sequencer installation wizard, double-click **Setup.exe**.</span></span> <span data-ttu-id="459b2-115">Wenn das **Microsoft Visual C++ SP1 Redistributable Package (x86)** vor der Installation nicht erkannt wird, klicken Sie auf **Installieren** , um die erforderliche Voraussetzung zu installieren.</span><span class="sxs-lookup"><span data-stu-id="459b2-115">If the **Microsoft Visual C++ SP1 Redistributable Package (x86)** is not detected prior to installation, click **Install** to install the required prerequisite.</span></span>

3.  <span data-ttu-id="459b2-116">Klicken Sie auf der Seite **Willkommen** auf **weiter**, um die Installation fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="459b2-116">To continue the installation, on the **Welcome** page, click **Next**.</span></span>

4.  <span data-ttu-id="459b2-117">Klicken Sie auf der Seite **Lizenzvertrag** auf **Ich stimme den Bedingungen**des Lizenzvertrags zu, um die Bedingungen des Lizenzvertrags zu akzeptieren, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="459b2-117">On the **License Agreement** page, to accept the terms of the license agreement, click **I accept the terms in the license agreement**, and then click **Next**.</span></span>

5.  <span data-ttu-id="459b2-118">Klicken Sie auf der Seite **Zielordner** auf **weiter**, um den Standardinstallationsordner zu übernehmen.</span><span class="sxs-lookup"><span data-stu-id="459b2-118">On the **Destination Folder** page, to accept the default installation folder, click **Next**.</span></span> <span data-ttu-id="459b2-119">Wenn Sie einen anderen Zielordner angeben möchten, klicken Sie auf **ändern** , und geben Sie den Installationsordner an, der für die Installation verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="459b2-119">To specify a different destination folder, click **Change** and specify the installation folder that will be used for the installation.</span></span> <span data-ttu-id="459b2-120">Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="459b2-120">Click **Next**.</span></span>

6.  <span data-ttu-id="459b2-121">Klicken Sie auf der Seite **virtuelles Laufwerk** auf **weiter**, um das Standardlaufwerk **Q:\\** (Standard) für Application Virtualization als das Laufwerk zu konfigurieren, von dem alle sequenzierten Anwendungen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="459b2-121">On the **Virtual Drive** page, to configure the Application Virtualization default drive **Q:\\** (default) as the drive that all sequenced applications will run from, click **Next**.</span></span> <span data-ttu-id="459b2-122">Wenn Sie einen anderen Laufwerkbuchstaben angeben möchten, verwenden Sie die Liste, und wählen Sie den Laufwerkbuchstaben aus, den Sie verwenden möchten, indem Sie den entsprechenden Laufwerkbuchstaben auswählen, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="459b2-122">If you want to specify a different drive letter, use the list and select the drive letter that you want to use by selecting the appropriate drive letter, and then click **Next**.</span></span>

    **<span data-ttu-id="459b2-123">Wichtig</span><span class="sxs-lookup"><span data-stu-id="459b2-123">Important</span></span>**  
    <span data-ttu-id="459b2-124">Der mit diesem Schritt angegebene Application Virtualization-Laufwerkbuchstabe ist der Laufwerkbuchstabe, auf dem virtuelle Anwendungen auf Zielcomputern ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="459b2-124">The Application Virtualization drive letter specified with this step is the drive letter that virtual applications will be run from on target computers.</span></span> <span data-ttu-id="459b2-125">Der angegebene Laufwerkbuchstabe muss verfügbar sein und auf den Computern, auf denen der App-V-Client ausgeführt wird, derzeit nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="459b2-125">The drive letter specified must be available, and not currently in use on the computers running the App-V client.</span></span> <span data-ttu-id="459b2-126">Wenn das angegebene Laufwerk bereits verwendet wird, schlägt die virtuelle Anwendung auf dem Zielcomputer fehl.</span><span class="sxs-lookup"><span data-stu-id="459b2-126">If the specified drive is already in use, the virtual application fails on the target computer.</span></span>



7.  <span data-ttu-id="459b2-127">Klicken Sie auf der Seite **bereit zum Installieren des Programms** auf **Installieren**, um die Installation zu starten.</span><span class="sxs-lookup"><span data-stu-id="459b2-127">On the **Ready to Install the Program** page, to start the installation, click **Install**.</span></span>

8.  <span data-ttu-id="459b2-128">Klicken Sie auf der Seite **abgeschlossen des InstallShield-Assistenten** auf **Fertig stellen**, um den Installations-Assistenten zu schließen und den App-V-Sequenzer zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="459b2-128">On the **InstallShield Wizard Completed** page, to close the installation wizard and open the App-V Sequencer, click **Finish**.</span></span> <span data-ttu-id="459b2-129">Wenn Sie den Installations-Assistenten schließen möchten, ohne den Sequencer zu öffnen, deaktivieren Sie **das Programm starten**, und klicken Sie dann auf **Fertig stellen**.</span><span class="sxs-lookup"><span data-stu-id="459b2-129">To close the installation wizard without opening the Sequencer, clear **Launch the program**, and then click **Finish**.</span></span>

    **<span data-ttu-id="459b2-130">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="459b2-130">Note</span></span>**  
    <span data-ttu-id="459b2-131">Wenn Sie den App-V-Sequencer auf einem Computer mit einer virtuellen Umgebung, beispielsweise einem virtuellen Computer, installiert haben, müssen Sie jetzt einen Schnappschuss erstellen.</span><span class="sxs-lookup"><span data-stu-id="459b2-131">If you installed the App-V Sequencer on a computer running a virtual environment, for example a virtual machine, you must now take a snapshot.</span></span> <span data-ttu-id="459b2-132">Nachdem Sie eine Anwendung sequenziert haben, können Sie zu diesem Bild zurückkehren, sodass Sie die nächste Anwendung sequenzieren können.</span><span class="sxs-lookup"><span data-stu-id="459b2-132">After you sequence an application, you can revert to this image, so you can sequence the next application.</span></span>



~~~
When you uninstall the Sequencer, the following registry keys are not removed from the computer that the Sequencer was installed on. Additionally, you must restart the computer after you have uninstalled the Sequencer so that all associated drivers can be stopped and the operation can be completed.

-   **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid**

-   **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5**

-   **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\SystemGuard**

-   **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\SystemGuard\\SecKey**
~~~

## <span data-ttu-id="459b2-133">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="459b2-133">Related topics</span></span>


[<span data-ttu-id="459b2-134">Konfigurieren von Application Virtualization Sequencer (App-V 4.6 SP1)</span><span class="sxs-lookup"><span data-stu-id="459b2-134">Configuring the Application Virtualization Sequencer (App-V 4.6 SP1)</span></span>](configuring-the-application-virtualization-sequencer--app-v-46-sp1-.md)









