---
title: So verzweigen Sie ein Paket
description: So verzweigen Sie ein Paket
author: dansimp
ms.assetid: bfe46a8a-f0ee-4a71-9e9c-64ac08aac9c1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2de36fae1a09aeae4d1b7b21ebe00f683e3b3693
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807383"
---
# <span data-ttu-id="879f5-103">So verzweigen Sie ein Paket</span><span class="sxs-lookup"><span data-stu-id="879f5-103">How to Branch a Package</span></span>


<span data-ttu-id="879f5-104">Gehen Sie wie folgt vor, um ein vorhandenes sequenziertes Anwendungspaket so zu ändern, dass es parallel zum ursprünglichen sequenzierten Anwendungspaket ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="879f5-104">Use this procedure to modify an existing sequenced application package so you can run it side-by-side with the original sequenced application package.</span></span> <span data-ttu-id="879f5-105">Dieser Vorgang wird als Verzweigung bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="879f5-105">This process is called branching.</span></span> <span data-ttu-id="879f5-106">Wenn Sie ein virtuelles Anwendungspaket verzweigen, können Sie zwei Versionen desselben Pakets ausführen.</span><span class="sxs-lookup"><span data-stu-id="879f5-106">When you branch a virtual application package you are able to run two versions of the same package.</span></span> <span data-ttu-id="879f5-107">So können Sie beispielsweise ein Service Pack auf ein vorhandenes Paket anwenden und es nebeneinander mit dem ursprünglichen sequenzierten virtuellen Anwendungspaket ausführen.</span><span class="sxs-lookup"><span data-stu-id="879f5-107">For example, you can apply a service pack to an existing package, and run it side-by-side with the original sequenced virtual application package.</span></span>

<span data-ttu-id="879f5-108">Gehen Sie wie folgt vor, um ein sequenziertes virtuelles Anwendungspaket zu verzweigen.</span><span class="sxs-lookup"><span data-stu-id="879f5-108">Use the following procedure to branch a sequenced virtual application package.</span></span>

**<span data-ttu-id="879f5-109">So verzweigen Sie ein sequenziertes virtuelles Anwendungspaket</span><span class="sxs-lookup"><span data-stu-id="879f5-109">To branch a sequenced virtual application package</span></span>**

1.  <span data-ttu-id="879f5-110">Öffnen Sie den Microsoft Application Virtualization (App-V)-Sequenzer.</span><span class="sxs-lookup"><span data-stu-id="879f5-110">Open the Microsoft Application Virtualization (App-V) Sequencer.</span></span> <span data-ttu-id="879f5-111">Um das Zielverzeichnis anzugeben, in dem sich das Paket (SPRJ) befindet, das Sie verzweigen möchten, wählen Sie **Datei**aus, **Öffnen**.</span><span class="sxs-lookup"><span data-stu-id="879f5-111">To specify the destination directory that contains the package (.sprj) you want to branch select **File**, **Open**.</span></span>

2.  <span data-ttu-id="879f5-112">Navigieren Sie zu dem Verzeichnis, das die sequenzierte Anwendung enthält, die Sie verzweigen möchten, und klicken Sie auf **Öffnen**.</span><span class="sxs-lookup"><span data-stu-id="879f5-112">Navigate to the directory that contains the sequenced application you plan to branch and click **Open**.</span></span>

3.  <span data-ttu-id="879f5-113">Wenn Sie eine Kopie des Pakets speichern möchten, wählen Sie im App-V-Sequenzer **Datei**, **Speichern**unter aus.</span><span class="sxs-lookup"><span data-stu-id="879f5-113">To save a copy of the package, in the App-V Sequencer, select **File**, **Save As**.</span></span> <span data-ttu-id="879f5-114">Geben Sie einen neuen eindeutigen Namen an, und geben Sie ein neues eindeutiges Paketstammverzeichnis für die Kopie des Pakets an.</span><span class="sxs-lookup"><span data-stu-id="879f5-114">Specify a new, unique name, and specify a new unique package root directory for the copy of the package.</span></span> <span data-ttu-id="879f5-115">Klicken Sie auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="879f5-115">Click **Save**.</span></span>

    **<span data-ttu-id="879f5-116">Wichtig</span><span class="sxs-lookup"><span data-stu-id="879f5-116">Important</span></span>**  
    <span data-ttu-id="879f5-117">Sie müssen einen neuen Paketnamen angeben, oder die vorhandene Version des Pakets wird überschrieben.</span><span class="sxs-lookup"><span data-stu-id="879f5-117">You must specify a new package name or you will overwrite the existing version of the package.</span></span>



~~~
The sequencer will automatically generate new GUID files for the new package. The version number associated with the package will also be automatically appended to the OSD file name.
~~~

4. <span data-ttu-id="879f5-118">Nachdem Sie die neue Version gespeichert haben, können Sie die erforderlichen Konfigurationsänderungen übernehmen und die zugehörigen ICO-, OSD-, SFT-und SPRJ-Dateien auf dem Application Virtualization (App-V)-Server speichern.</span><span class="sxs-lookup"><span data-stu-id="879f5-118">After you save the new version you can apply the required configuration changes and save the associated ICO, OSD, SFT, and SPRJ files to correct location on the Application Virtualization (App-V) server.</span></span>

## <span data-ttu-id="879f5-119">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="879f5-119">Related topics</span></span>


[<span data-ttu-id="879f5-120">Aufgaben für den Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="879f5-120">Tasks for the Application Virtualization Sequencer</span></span>](tasks-for-the-application-virtualization-sequencer.md)









