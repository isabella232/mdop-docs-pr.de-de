---
title: Dialogfeld „Defender wird ausgeführt“ (App-V 4.6 SP1)
description: Dialogfeld „Defender wird ausgeführt“ (App-V 4.6 SP1)
author: dansimp
ms.assetid: 716ec7f9-ddad-45dd-a3c7-4a9d81cfcfd0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0e33d48c089d7bf903c65da804e6cf5aa1bd2065
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808956"
---
# <span data-ttu-id="96c4f-103">Dialogfeld „Defender wird ausgeführt“ (App-V 4.6 SP1)</span><span class="sxs-lookup"><span data-stu-id="96c4f-103">Defender Running Dialog Box (App-V 4.6 SP1)</span></span>


<span data-ttu-id="96c4f-104">Microsoft Windows Defender wird ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="96c4f-104">Microsoft Windows Defender is running.</span></span> <span data-ttu-id="96c4f-105">Sie sollten Windows Defender beenden, bevor Sie mit der Installation fortfahren.</span><span class="sxs-lookup"><span data-stu-id="96c4f-105">You should stop Windows Defender before continuing with the installation.</span></span> <span data-ttu-id="96c4f-106">Windows Defender kann die Erstellung eines Pakets stören, indem Sie auf Dateien zugreifen, die dem virtuellen Anwendungspaket hinzugefügt werden müssen, oder indem Sie dem virtuellen Anwendungspaket überflüssige Daten hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="96c4f-106">Windows Defender can interfere with creation of a package by accessing files that must be added to the virtual application package or by adding extraneous data to the virtual application package.</span></span>

<span data-ttu-id="96c4f-107">Gehen Sie wie folgt vor, um zu verhindern, dass Microsoft Windows Defender während der Sequenzierung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="96c4f-107">Use the following procedure to stop Microsoft Windows Defender from running during sequencing.</span></span>

1.  <span data-ttu-id="96c4f-108">Klicken Sie auf dem Computer, auf dem der App-V-Sequenzer ausgeführt wird, auf **Start**, klicken Sie mit der rechten Maustaste auf **Computer**, und klicken Sie dann auf **Verwalten**.</span><span class="sxs-lookup"><span data-stu-id="96c4f-108">On the computer running the App-V Sequencer, click **Start**, right-click **Computer**, and then click **Manage**.</span></span>

2.  <span data-ttu-id="96c4f-109">Doppelklicken Sie in der **Computer Verwaltungs** Konsole auf **Dienste und Anwendungen**, und doppelklicken Sie dann auf **Dienste** , um **Dienste**zu erweitern.</span><span class="sxs-lookup"><span data-stu-id="96c4f-109">In the **Computer Management** console, double click **Services and Applications**, and then double-click **Services** to expand **Services**.</span></span>

3.  <span data-ttu-id="96c4f-110">Suchen Sie die Datei in der Liste.</span><span class="sxs-lookup"><span data-stu-id="96c4f-110">Locate it in the list.</span></span> <span data-ttu-id="96c4f-111">Klicken Sie mit der rechten Maustaste auf Windows Defender, klicken Sie auf **Beenden** , um Microsoft Windows Defender zu beenden, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="96c4f-111">Right-click Windows Defender, click **Stop** to stop Microsoft Windows Defender, and then click **Ok**.</span></span>

## <span data-ttu-id="96c4f-112">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="96c4f-112">Related topics</span></span>


[<span data-ttu-id="96c4f-113">Dialogfelder (AppV 4.6 SP1)</span><span class="sxs-lookup"><span data-stu-id="96c4f-113">Dialog Boxes (AppV 4.6 SP1)</span></span>](dialog-boxes--appv-46-sp1-.md)

 

 





