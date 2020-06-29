---
title: So erstellen Sie einen Package Accelerator mithilfe von PowerShell
description: So erstellen Sie einen Package Accelerator mithilfe von PowerShell
author: dansimp
ms.assetid: 8e527363-d961-4153-826a-446a4ad8d980
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4270db9a5f0603cff1f33e6244a5abb517572d97
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805621"
---
# <span data-ttu-id="d7f04-103">So erstellen Sie einen Package Accelerator mithilfe von PowerShell</span><span class="sxs-lookup"><span data-stu-id="d7f04-103">How to Create a Package Accelerator by Using PowerShell</span></span>


<span data-ttu-id="d7f04-104">App-V 5,0-Paket Beschleuniger Sequenzieren automatisch große, komplexe Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="d7f04-104">App-V 5.0 package accelerators automatically sequence large, complex applications.</span></span> <span data-ttu-id="d7f04-105">Darüber hinaus müssen Sie beim Anwenden eines App-V 5,0-Paket Beschleunigers nicht immer eine Anwendung manuell installieren, um das virtualisierte Paket zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="d7f04-105">Additionally, when you apply an App-V 5.0 package accelerator, you are not always required to manually install an application to create the virtualized package.</span></span>

**<span data-ttu-id="d7f04-106">So erstellen Sie einen Paket Beschleuniger</span><span class="sxs-lookup"><span data-stu-id="d7f04-106">To create a package accelerator</span></span>**

1.  <span data-ttu-id="d7f04-107">Installieren Sie den App-V 5,0-Sequenzer.</span><span class="sxs-lookup"><span data-stu-id="d7f04-107">Install the App-V 5.0 sequencer.</span></span> <span data-ttu-id="d7f04-108">Weitere Informationen zum Installieren des Sequencers finden Sie unter [Installieren des Sequencers](how-to-install-the-sequencer-beta-gb18030.md).</span><span class="sxs-lookup"><span data-stu-id="d7f04-108">For more information about installing the sequencer see [How to Install the Sequencer](how-to-install-the-sequencer-beta-gb18030.md).</span></span>

2.  <span data-ttu-id="d7f04-109">Klicken Sie auf **Start** , und geben Sie **PowerShell**ein, um eine PowerShell-Konsole zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="d7f04-109">To open a PowerShell console click **Start** and type **PowerShell**.</span></span> <span data-ttu-id="d7f04-110">Klicken Sie mit der rechten Maustaste auf **Windows PowerShell**, und wählen Sie **Als Administrator ausführen** aus.</span><span class="sxs-lookup"><span data-stu-id="d7f04-110">Right-click **Windows PowerShell** and select **Run as Administrator**.</span></span> <span data-ttu-id="d7f04-111">Verwenden Sie das Cmdlet **New-AppvPackageAccelerator** .</span><span class="sxs-lookup"><span data-stu-id="d7f04-111">Use the **New-AppvPackageAccelerator** cmdlet.</span></span>

3.  <span data-ttu-id="d7f04-112">Wenn Sie einen Paket Beschleuniger erstellen möchten, stellen Sie sicher, dass Sie über das AppV-Paket verfügen, um eine Zugriffstaste von den Installationsmedien oder Installationsdateien sowie optional eine Read Me-Datei für die Benutzer des Beschleunigers zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="d7f04-112">To create a package accelerator, make sure that you have the .appv package to create an accelerator from, the installation media or installation files, and optionally a read me file for consumers of the accelerator to use.</span></span> <span data-ttu-id="d7f04-113">Die folgenden Parameter sind erforderlich, um das Paket Beschleuniger-Cmdlet zu verwenden:</span><span class="sxs-lookup"><span data-stu-id="d7f04-113">The following parameters are required to use the package accelerator cmdlet:</span></span>

    -   <span data-ttu-id="d7f04-114">**InstalledFilesPath** – gibt den Anwendungs Installationspfad an.</span><span class="sxs-lookup"><span data-stu-id="d7f04-114">**InstalledFilesPath** - specifies the application installation path.</span></span>

    -   <span data-ttu-id="d7f04-115">**Installer** – gibt den Pfad zu den Anwendungs Installationsmedien an.</span><span class="sxs-lookup"><span data-stu-id="d7f04-115">**Installer** – specifies the path to the application installer media</span></span>

    -   <span data-ttu-id="d7f04-116">**InputPackagePath** – gibt den Pfad zum AppV-Paket an.</span><span class="sxs-lookup"><span data-stu-id="d7f04-116">**InputPackagePath** – specifies the path to the .appv package</span></span>

    -   <span data-ttu-id="d7f04-117">**Path** – gibt das Ausgabeverzeichnis für das Paket an.</span><span class="sxs-lookup"><span data-stu-id="d7f04-117">**Path** – specifies the output directory for the package.</span></span>

    <span data-ttu-id="d7f04-118">Im folgenden Beispiel wird gezeigt, wie Sie einen Paket Beschleuniger mit einem AppV-Paket und den Installationsmedien erstellen können:</span><span class="sxs-lookup"><span data-stu-id="d7f04-118">The following example displays how you can create a package accelerator with an .appv package and the installation media:</span></span>

    **<span data-ttu-id="d7f04-119">New-AppvPackageAccelerator-InputPackagePath &lt; path to the. AppV Datei &gt; -Installer- &lt; Pfad zur ausführbaren Installationsprogramm &gt; -Pfad &lt; Verzeichnis des Ausgabepfads&gt;</span><span class="sxs-lookup"><span data-stu-id="d7f04-119">New-AppvPackageAccelerator -InputPackagePath &lt;path to the .appv file&gt; -Installer &lt;path to the installer executable&gt; -Path &lt;directory of the output path&gt;</span></span>**

    <span data-ttu-id="d7f04-120">Zusätzliche optionale Parameter, die mit dem Cmdlet **New-AppvPackageAccelerator** verwendet werden können, werden in der folgenden Liste angezeigt:</span><span class="sxs-lookup"><span data-stu-id="d7f04-120">Additional optional parameters that can be used with the **New-AppvPackageAccelerator** cmdlet are displayed in the following list:</span></span>

    -   <span data-ttu-id="d7f04-121">**AcceleratorDescriptionFile** – gibt den Pfad zu den vom Benutzer erstellten Paket Beschleuniger Anweisungen an.</span><span class="sxs-lookup"><span data-stu-id="d7f04-121">**AcceleratorDescriptionFile** - specifies the path to user created package accelerator instructions.</span></span> <span data-ttu-id="d7f04-122">Die Anweisungen für den Paket Beschleuniger sind **txt-** oder **RTF** -Beschreibungsdateien, die mit dem mit dem Paket Beschleuniger erstellten Paket verpackt werden.</span><span class="sxs-lookup"><span data-stu-id="d7f04-122">The package accelerator instructions are **.txt** or **.rtf** description files that will be packaged with the package created using the package accelerator.</span></span>

    <span data-ttu-id="d7f04-123">Sie **haben einen Vorschlag für App-V**?</span><span class="sxs-lookup"><span data-stu-id="d7f04-123">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="d7f04-124">[Hier](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)können Sie Vorschläge hinzufügen oder abstimmen.</span><span class="sxs-lookup"><span data-stu-id="d7f04-124">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="d7f04-125">Sie haben ein App-V-Problem?</span><span class="sxs-lookup"><span data-stu-id="d7f04-125">Got an App-V issue?</span></span>** <span data-ttu-id="d7f04-126">Verwenden Sie das [App-V TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="d7f04-126">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="d7f04-127">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="d7f04-127">Related topics</span></span>


[<span data-ttu-id="d7f04-128">Verwalten von App-V mithilfe von PowerShell</span><span class="sxs-lookup"><span data-stu-id="d7f04-128">Administering App-V by Using PowerShell</span></span>](administering-app-v-by-using-powershell.md)

 

 





