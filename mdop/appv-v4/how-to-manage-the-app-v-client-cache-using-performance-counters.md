---
title: So verwalten Sie den App-V-Client-Cache mithilfe von Leistungsindikatoren
description: So verwalten Sie den App-V-Client-Cache mithilfe von Leistungsindikatoren
author: dansimp
ms.assetid: 49d6c3f2-68b8-4c69-befa-7598a8737d05
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 396cceaf9a3bde661200be2771a85596a512732f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806984"
---
# <span data-ttu-id="47182-103">So verwalten Sie den App-V-Client-Cache mithilfe von Leistungsindikatoren</span><span class="sxs-lookup"><span data-stu-id="47182-103">How to Manage the App-V Client Cache Using Performance Counters</span></span>


<span data-ttu-id="47182-104">Mit dem folgenden Verfahren können Sie ermitteln, wie viel freier Speicherplatz im Application Virtualization (App-V)-Clientcache verfügbar ist, indem Sie die Informationen mithilfe des Systemmonitors grafisch darstellen.</span><span class="sxs-lookup"><span data-stu-id="47182-104">You can use the following procedure to determine how much free space is available in the Application Virtualization (App-V) client cache by using Performance Monitor to display the information graphically.</span></span> <span data-ttu-id="47182-105">Diese Informationen werden auf dem Clientcomputer von einem Leistungsindikator mit dem Namen "App virt-Client Cache" erfasst und enthalten die folgenden Leistungsindikatoren: "Cachegröße (MB)", "Zwischenspeicher Platz (MB)" und "% freier Speicherplatz".</span><span class="sxs-lookup"><span data-stu-id="47182-105">This information is captured on the client computer by a performance counter called “App Virt Client Cache,” and it includes the following counters: “Cache size (MB),” “Cache free space (MB),” and “% free space.”</span></span>

**<span data-ttu-id="47182-106">So ermitteln Sie die Verwendung des Clientcache Speichers</span><span class="sxs-lookup"><span data-stu-id="47182-106">To determine client cache space usage</span></span>**

1.  <span data-ttu-id="47182-107">Öffnen Sie eine Eingabeaufforderung als Administrator, oder klicken Sie auf **Start**, **Ausführen**, geben Sie **perfmon.exe**ein, und klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="47182-107">Open a command prompt as administrator, or click **Start**, **Run**, type **perfmon.exe**, and click **OK**.</span></span>

2.  <span data-ttu-id="47182-108">Klicken Sie je nach verwendetem Windows-Betriebssystem auf das Tool Leistungsmonitor oder Systemmonitor, nachdem das MMC-Fenster geöffnet wurde.</span><span class="sxs-lookup"><span data-stu-id="47182-108">Depending on the Windows operating system being used, click the Performance Monitor or System Monitor tool after the MMC window opens.</span></span>

3.  <span data-ttu-id="47182-109">Um Leistungsindikatoren hinzuzufügen, klicken Sie mit der rechten Maustaste auf den Diagrammbereich, und wählen Sie **Indikatoren hinzufügen**aus.</span><span class="sxs-lookup"><span data-stu-id="47182-109">To add counters, right-click the graph area and select **Add Counters**.</span></span>

4.  <span data-ttu-id="47182-110">Klicken Sie auf die Dropdownliste, um die Liste der verfügbaren Leistungsindikatoren anzuzeigen, Scrollen Sie, um den **App virt-Client Cache**zu finden, und fügen Sie dann die drei Leistungsindikatoren hinzu.</span><span class="sxs-lookup"><span data-stu-id="47182-110">Click the drop-down to display the list of available counters, scroll to find **App Virt Client Cache**, and then add the three counters.</span></span>

    <span data-ttu-id="47182-111">**Wichtig**  Da die App-V-Leistungsindikatoren in einer 32-Bit-DLL implementiert sind, müssen Sie den folgenden Befehl verwenden, um die 32-Bit-Version des Systemmonitors zu starten: **MMC/32 Perfmon. msc**.</span><span class="sxs-lookup"><span data-stu-id="47182-111">**Important** The App-V performance counters are implemented in a 32-bit DLL, so to see them, you must use the following command to start the 32-bit version of Performance Monitor: **mmc /32 perfmon.msc**.</span></span> <span data-ttu-id="47182-112">Dieser Befehl muss direkt auf dem Computer ausgeführt werden, der überwacht wird, und kann nicht zum Überwachen eines Remotecomputers, auf dem ein 64-Bit-Betriebssystem ausgeführt wird, verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="47182-112">This command must be run directly on the computer being monitored and cannot be used to monitor a remote computer running a 64-bit operating system.</span></span>

     

## <span data-ttu-id="47182-113">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="47182-113">Related topics</span></span>


[<span data-ttu-id="47182-114">So verwalten Sie virtuelle Anwendungen über die Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="47182-114">How to Manage Virtual Applications by Using the Command Line</span></span>](how-to-manage-virtual-applications-by-using-the-command-line.md)

 

 





