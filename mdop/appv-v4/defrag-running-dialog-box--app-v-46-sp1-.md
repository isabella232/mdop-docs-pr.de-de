---
title: Dialogfeld „Disk Defragmenter ist aktiv“ (App-V 4.6 SP1)
description: Dialogfeld „Disk Defragmenter ist aktiv“ (App-V 4.6 SP1)
author: dansimp
ms.assetid: 0ceb0897-377e-4754-a7ab-3bc2b5af1452
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2ca56723dedb46ba87890ae62d476ca365b201c6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808929"
---
# <span data-ttu-id="b0d70-103">Dialogfeld „Disk Defragmenter ist aktiv“ (App-V 4.6 SP1)</span><span class="sxs-lookup"><span data-stu-id="b0d70-103">Defrag Running Dialog Box (App-V 4.6 SP1)</span></span>


<span data-ttu-id="b0d70-104">Der Dienst für die Datenträgerdefragmentierung wird ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b0d70-104">The Disk Defragmenter service is running.</span></span> <span data-ttu-id="b0d70-105">Der Dienst "Datenträgerdefragmentierung" verwendet Systemressourcen und kann die Leistung beeinträchtigen oder die zum Erstellen eines virtuellen Anwendungspakets benötigte Zeit verlängern.</span><span class="sxs-lookup"><span data-stu-id="b0d70-105">The Disk Defragmenter service uses system resources and can cause degradation in performance or increase the time it takes to create virtual application package.</span></span>

<span data-ttu-id="b0d70-106">Gehen Sie wie folgt vor, um zu verhindern, dass der Defragmentor-Dienst während der Sequenzierung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b0d70-106">Use the following procedure to stop the Disk Defragmenter service from running during sequencing.</span></span>

1.  <span data-ttu-id="b0d70-107">Klicken Sie auf dem Computer, auf dem der App-V-Sequenzer ausgeführt wird, auf **Start**, klicken Sie mit der rechten Maustaste auf **Computer**, und klicken Sie dann auf **Verwalten**.</span><span class="sxs-lookup"><span data-stu-id="b0d70-107">On the computer running the App-V Sequencer, click **Start**, right-click **Computer**, and then click **Manage**.</span></span>

2.  <span data-ttu-id="b0d70-108">Doppelklicken Sie in der **Computer Verwaltungs** Konsole auf **Dienste und Anwendungen**, und doppelklicken Sie dann auf **Dienste** , um **Dienste**zu erweitern.</span><span class="sxs-lookup"><span data-stu-id="b0d70-108">In the **Computer Management** console, double-click **Services and Applications**, and then double-click **Services** to expand **Services**,.</span></span>

3.  <span data-ttu-id="b0d70-109">Suchen Sie die Datei in der Liste.</span><span class="sxs-lookup"><span data-stu-id="b0d70-109">Locate it in the list.</span></span> <span data-ttu-id="b0d70-110">Klicken Sie mit der rechten Maustaste auf **Datenträgerdefragmentierung**, klicken Sie auf **Weitere Aktionen**, klicken Sie auf **Beenden** , um die Defragmentierung zu beenden, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="b0d70-110">Right-click **Disk Defragmenter**, click **More Actions**, click **Stop** to stop Disk Defragmenter, and then click **OK**.</span></span>

## <span data-ttu-id="b0d70-111">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="b0d70-111">Related topics</span></span>


[<span data-ttu-id="b0d70-112">Dialogfelder (AppV 4.6 SP1)</span><span class="sxs-lookup"><span data-stu-id="b0d70-112">Dialog Boxes (AppV 4.6 SP1)</span></span>](dialog-boxes--appv-46-sp1-.md)

 

 





