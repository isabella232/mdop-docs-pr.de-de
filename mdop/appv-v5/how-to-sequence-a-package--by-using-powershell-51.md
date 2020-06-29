---
title: Sequenzierung eines Pakets mithilfe von PowerShell
description: Sequenzierung eines Pakets mithilfe von PowerShell
author: dansimp
ms.assetid: 6134c6be-937d-4609-a516-92d49154b290
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e1bc2933fdb64080dab3b514784e7f68b0236df9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805168"
---
# <span data-ttu-id="a3f22-103">Sequenzierung eines Pakets mithilfe von PowerShell</span><span class="sxs-lookup"><span data-stu-id="a3f22-103">How to Sequence a Package by Using PowerShell</span></span>


<span data-ttu-id="a3f22-104">Gehen Sie wie folgt vor, um ein neues App-V 5,1-Paket mit PowerShell zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="a3f22-104">Use the following procedure to create a new App-V 5.1 package using PowerShell.</span></span>

<span data-ttu-id="a3f22-105">**Hinweis**  Bevor Sie dieses Verfahren verwenden, müssen Sie die zugehörigen Installationsdateien auf den Computer kopieren, auf dem der Sequencer ausgeführt wird, und Sie haben den Sequencer-Abschnitt der [Planung für den App-V 5,1-Sequenzer und die Client Bereitstellung](planning-for-the-app-v-51-sequencer-and-client-deployment.md)gelesen und verstanden.</span><span class="sxs-lookup"><span data-stu-id="a3f22-105">**Note** Before you use this procedure you must copy the associated installer files to the computer running the sequencer and you have read and understand the sequencer section of [Planning for the App-V 5.1 Sequencer and Client Deployment](planning-for-the-app-v-51-sequencer-and-client-deployment.md).</span></span>

 

**<span data-ttu-id="a3f22-106">So erstellen Sie eine neue virtuelle Anwendung mithilfe von PowerShell</span><span class="sxs-lookup"><span data-stu-id="a3f22-106">To create a new virtual application using PowerShell</span></span>**

1.  <span data-ttu-id="a3f22-107">Installieren Sie den App-V 5,1-Sequenzer.</span><span class="sxs-lookup"><span data-stu-id="a3f22-107">Install the App-V 5.1 sequencer.</span></span> <span data-ttu-id="a3f22-108">Weitere Informationen zum Installieren des Sequencers finden Sie unter [Installieren des Sequencers](how-to-install-the-sequencer-51beta-gb18030.md).</span><span class="sxs-lookup"><span data-stu-id="a3f22-108">For more information about installing the sequencer see [How to Install the Sequencer](how-to-install-the-sequencer-51beta-gb18030.md).</span></span>

2.  <span data-ttu-id="a3f22-109">Klicken Sie auf **Start** , und geben Sie **PowerShell**ein, um eine PowerShell-Konsole zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="a3f22-109">To open a PowerShell console click **Start** and type **PowerShell**.</span></span> <span data-ttu-id="a3f22-110">Klicken Sie mit der rechten Maustaste auf **Windows PowerShell**, und wählen Sie **Als Administrator ausführen** aus.</span><span class="sxs-lookup"><span data-stu-id="a3f22-110">Right-click **Windows PowerShell** and select **Run as Administrator**.</span></span>

3.  <span data-ttu-id="a3f22-111">Verwenden Sie die PowerShell-Konsole, und geben Sie Folgendes ein: **Import-Module appvsequencer**.</span><span class="sxs-lookup"><span data-stu-id="a3f22-111">Using the PowerShell console, type the following: **import-module appvsequencer**.</span></span>

4.  <span data-ttu-id="a3f22-112">Verwenden Sie zum Erstellen eines Pakets das Cmdlet **New-AppvSequencerPackage** .</span><span class="sxs-lookup"><span data-stu-id="a3f22-112">To create a package, use the **New-AppvSequencerPackage** cmdlet.</span></span> <span data-ttu-id="a3f22-113">Die folgenden Parameter sind erforderlich, um ein Paket zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="a3f22-113">The following parameters are required to create a package:</span></span>

    -   <span data-ttu-id="a3f22-114">**Name** – gibt den Namen des Pakets an.</span><span class="sxs-lookup"><span data-stu-id="a3f22-114">**Name** - specifies the name of the package.</span></span>

    -   <span data-ttu-id="a3f22-115">**PrimaryVirtualApplicationDirectory** – gibt den Pfad zu dem Verzeichnis an, das zum Installieren der Anwendung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a3f22-115">**PrimaryVirtualApplicationDirectory** - specifies the path to the directory that will be used to install the application.</span></span> <span data-ttu-id="a3f22-116">Dieser Pfad muss vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="a3f22-116">This path must exist.</span></span>

    -   <span data-ttu-id="a3f22-117">**Installer** – gibt den Pfad zum zugehörigen Anwendungs Installationsprogramm an.</span><span class="sxs-lookup"><span data-stu-id="a3f22-117">**Installer** - specifies the path to the associated application installer.</span></span>

    -   <span data-ttu-id="a3f22-118">**Path** – gibt das Ausgabeverzeichnis für das Paket an.</span><span class="sxs-lookup"><span data-stu-id="a3f22-118">**Path** - specifies the output directory for the package.</span></span>

    <span data-ttu-id="a3f22-119">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="a3f22-119">For example:</span></span>

    **<span data-ttu-id="a3f22-120">New-AppvSequencerPackage – Name Name &lt; des Package &gt; -PrimaryVirtualApplicationDirectory- &lt; Pfads zum Paket-root &gt; -Installer- &lt; Pfad zum ausführbaren Installer &gt; -OutputPath- &lt; Verzeichnis des Ausgabepfads&gt;</span><span class="sxs-lookup"><span data-stu-id="a3f22-120">New-AppvSequencerPackage –Name &lt;name of Package&gt; -PrimaryVirtualApplicationDirectory &lt;path to the package root&gt; -Installer &lt;path to the installer executable&gt; -OutputPath &lt;directory of the output path&gt;</span></span>**

    <span data-ttu-id="a3f22-121">Warten Sie, bis der Sequencer das Paket erstellt hat.</span><span class="sxs-lookup"><span data-stu-id="a3f22-121">Wait for the sequencer to create the package.</span></span> <span data-ttu-id="a3f22-122">Das Erstellen eines Pakets mit PowerShell kann Zeit in Anspruch nehmen.</span><span class="sxs-lookup"><span data-stu-id="a3f22-122">Creating a package using PowerShell can take time.</span></span> <span data-ttu-id="a3f22-123">Wenn das Paket nicht erfolgreich erstellt wurde, wird ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a3f22-123">If the package was not created successfully an error will be returned.</span></span>

    <span data-ttu-id="a3f22-124">In der folgenden Liste werden zusätzliche optionale Parameter angezeigt, die mit dem Cmdlet **New-AppvSequencerPackage** verwendet werden können:</span><span class="sxs-lookup"><span data-stu-id="a3f22-124">The following list displays additional optional parameters that can be used with **New-AppvSequencerPackage** cmdlet:</span></span>

    -   <span data-ttu-id="a3f22-125">AcceleratorFilePath – gibt den Pfad zur Beschleuniger. CAB-Datei an, um ein Paket zu generieren.</span><span class="sxs-lookup"><span data-stu-id="a3f22-125">AcceleratorFilePath – specifies the path to the accelerator .cab file to generate a package.</span></span>

    -   <span data-ttu-id="a3f22-126">InstalledFilesPath – gibt den Pfad an, in dem die lokal installierten Dateien der Anwendung gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="a3f22-126">InstalledFilesPath - specifies the path to where the local installed files of the application are saved.</span></span>

    -   <span data-ttu-id="a3f22-127">InstallMediaPath – gibt den Pfad an, in dem sich das Installationsmedium befindet</span><span class="sxs-lookup"><span data-stu-id="a3f22-127">InstallMediaPath - specifies the path to where the installation media is</span></span>

    -   <span data-ttu-id="a3f22-128">TemplateFilePath – gibt den Pfad zu einer Vorlagendatei an, wenn Sie den Sequenz Prozess anpassen möchten.</span><span class="sxs-lookup"><span data-stu-id="a3f22-128">TemplateFilePath - specifies the path to a template file if you want to customize the sequencing process.</span></span>

    -   <span data-ttu-id="a3f22-129">FullLoad – gibt an, dass das Paket vollständig auf den Computer heruntergeladen werden muss, auf dem die App-V 5,1 ausgeführt wird, bevor es geöffnet werden kann.</span><span class="sxs-lookup"><span data-stu-id="a3f22-129">FullLoad - specifies that the package must be fully downloaded to the computer running the App-V 5.1 before it can be opened.</span></span>

    <span data-ttu-id="a3f22-130">Sie **haben einen Vorschlag für App-V**?</span><span class="sxs-lookup"><span data-stu-id="a3f22-130">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="a3f22-131">[Hier](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)können Sie Vorschläge hinzufügen oder abstimmen.</span><span class="sxs-lookup"><span data-stu-id="a3f22-131">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="a3f22-132">Sie haben ein App-V-Problem?</span><span class="sxs-lookup"><span data-stu-id="a3f22-132">Got an App-V issue?</span></span>** <span data-ttu-id="a3f22-133">Verwenden Sie das [App-V TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="a3f22-133">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="a3f22-134">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="a3f22-134">Related topics</span></span>


[<span data-ttu-id="a3f22-135">Verwalten von App-V 5.1 mithilfe von PowerShell</span><span class="sxs-lookup"><span data-stu-id="a3f22-135">Administering App-V 5.1 by Using PowerShell</span></span>](administering-app-v-51-by-using-powershell.md)

 

 





