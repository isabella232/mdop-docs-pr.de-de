---
title: So aktualisieren Sie ein Paket mit dem Befehl „Paket öffnen“
description: So aktualisieren Sie ein Paket mit dem Befehl „Paket öffnen“
author: dansimp
ms.assetid: 67c10440-de8a-4547-a34b-f83206d0cc3b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: cca438fe90373e8f934d1d790246544cdf46fa18
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806739"
---
# <span data-ttu-id="1a672-103">So aktualisieren Sie ein Paket mit dem Befehl „Paket öffnen“</span><span class="sxs-lookup"><span data-stu-id="1a672-103">How to Upgrade a Package Using the Open Package Command</span></span>


<span data-ttu-id="1a672-104">Verwenden Sie den Befehl "Paket öffnen", um ein Update auf ein sequenziertes Anwendungspaket zu aktualisieren oder anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="1a672-104">Use the Open Package command to upgrade or apply an update to a sequenced application package.</span></span> <span data-ttu-id="1a672-105">Wenn Sie ein vorhandenes virtuelles Anwendungspaket über die Befehlszeile aktualisieren, wird die ursprüngliche Version der SFT-Datei gelöscht.</span><span class="sxs-lookup"><span data-stu-id="1a672-105">When you upgrade an existing virtual application package using the command line, the original version of the .sft file is deleted.</span></span> <span data-ttu-id="1a672-106">Sie sollten die zugehörige SFT-Datei sichern, bevor Sie das Paket über die Befehlszeile aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="1a672-106">You should backup the associated .sft file before upgrading the package using the command line.</span></span>

**<span data-ttu-id="1a672-107">So aktualisieren Sie ein Paket mit dem Befehl "Paket öffnen"</span><span class="sxs-lookup"><span data-stu-id="1a672-107">To upgrade a package using the Open Package command</span></span>**

1.  <span data-ttu-id="1a672-108">Zum Öffnen des Pakets, das aktualisiert werden soll, wählen Sie in der Application Virtualization (App-V)-Konsole **Datei**aus, öffnen Sie das **Paket für das Upgrade**.</span><span class="sxs-lookup"><span data-stu-id="1a672-108">To open the package that will be upgraded, in the Application Virtualization (App-V) console select **File**, **Open Package for Upgrade**.</span></span> <span data-ttu-id="1a672-109">Wählen Sie im Dialogfeld **Öffnen** das Paket aus, das aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="1a672-109">In the **Open** dialog box, select the package that will be upgraded.</span></span>

2.  <span data-ttu-id="1a672-110">Zum Starten des **Sequenz** -Assistenten wählen Sie **Tools**, **Sequenz-Assistent**aus.</span><span class="sxs-lookup"><span data-stu-id="1a672-110">To start the **Sequencing** wizard, select **Tools**, **Sequencing Wizard**.</span></span> <span data-ttu-id="1a672-111">Führen Sie den Assistenten aus, indem Sie die Konfigurationsänderungen anwenden, um die neue sequenzierte Anwendung zu speichern, wählen Sie **Datei**und dann **Speichern**aus.</span><span class="sxs-lookup"><span data-stu-id="1a672-111">Complete the wizard applying the configuration changes, to save the new sequenced application, select **File**, **Save**.</span></span>

3.  <span data-ttu-id="1a672-112">Wenn Sie die Versionsnummer an den Paketnamen anfügen möchten, wählen Sie in der Sequencer-Konsole **Extras**, **Optionen**aus.</span><span class="sxs-lookup"><span data-stu-id="1a672-112">To append the version number to the package name, in the Sequencer console, select **Tools**, **Options**.</span></span> <span data-ttu-id="1a672-113">Wählen Sie **Paket Version an filename anfügen**aus.</span><span class="sxs-lookup"><span data-stu-id="1a672-113">Select **Append Package Version to Filename**.</span></span> <span data-ttu-id="1a672-114">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="1a672-114">Click **OK**.</span></span>

    <span data-ttu-id="1a672-115">**Wichtig**  Das Aktualisieren des Datei namens mit der Paketversion ist wichtig, um das Upgrade erfolgreich abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="1a672-115">**Important** Updating the file name with the package version is essential to successfully completing the upgrade.</span></span>

     

## <span data-ttu-id="1a672-116">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="1a672-116">Related topics</span></span>


[<span data-ttu-id="1a672-117">So verwalten Sie virtuellen Anwendungen über die Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="1a672-117">How to Manage Virtual Applications Using the Command Line</span></span>](how-to-manage-virtual-applications-using-the-command-line.md)

 

 





