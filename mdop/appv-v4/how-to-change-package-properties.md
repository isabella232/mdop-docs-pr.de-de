---
title: So ändern Sie die Paketeigenschaften
description: So ändern Sie die Paketeigenschaften
author: dansimp
ms.assetid: 6050916a-d4fe-4dac-8f2a-47308dbbf481
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d2427a2651f3941f967c171ae7854facc62b4aa9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807348"
---
# <span data-ttu-id="bf74f-103">So ändern Sie die Paketeigenschaften</span><span class="sxs-lookup"><span data-stu-id="bf74f-103">How to Change Package Properties</span></span>


<span data-ttu-id="bf74f-104">Mit den folgenden Verfahren können Sie den Namen eines Application Virtualization-Pakets und die zugehörigen Kommentare ändern.</span><span class="sxs-lookup"><span data-stu-id="bf74f-104">You can use the following procedures to modify an Application Virtualization package name and its associated comments.</span></span>

<span data-ttu-id="bf74f-105">Wenn dies das erste Mal ist, dass das Paket erstellt wurde, können Sie auch die Blockgröße des Sequenz-Parameters ändern, die bestimmt, wie ein sequenziertes Anwendungspaket von einem Application Virtualization Server an einen Application Virtualization-Desktop Client gestreamt wird.</span><span class="sxs-lookup"><span data-stu-id="bf74f-105">If this is the first time the package has been created, you can also change the sequencing parameter block size, which determines how a sequenced application package is streamed from an Application Virtualization Server to an Application Virtualization Desktop Client.</span></span>

<span data-ttu-id="bf74f-106">**Hinweis**  Wenn Sie eine Blockgröße auswählen, sollten Sie die Größe der SFT-Datei und die Netzwerkbandbreite in Frage stellen.</span><span class="sxs-lookup"><span data-stu-id="bf74f-106">**Note** When selecting a block size, consider the size of the SFT file and your network bandwidth.</span></span> <span data-ttu-id="bf74f-107">Eine Datei mit einer kleineren Blockgröße dauert länger, um über das Netzwerk zu streamen, es ist jedoch weniger bandbreitenintensiv.</span><span class="sxs-lookup"><span data-stu-id="bf74f-107">A file with a smaller block size takes longer to stream over the network, but it is less bandwidth intensive.</span></span> <span data-ttu-id="bf74f-108">Dateien mit größeren Blockgrößen können schneller gestreamt werden, verwenden aber mehr Netzwerkbandbreite.</span><span class="sxs-lookup"><span data-stu-id="bf74f-108">Files with larger block sizes might stream faster, but they use more network bandwidth.</span></span> <span data-ttu-id="bf74f-109">Durch experimentieren können Sie die optimale Blockgröße für Streaming-Anwendungen in Ihrem Netzwerk ermitteln.</span><span class="sxs-lookup"><span data-stu-id="bf74f-109">Through experimentation, you can discover the optimum block size for streaming applications on your network.</span></span>

 

<span data-ttu-id="bf74f-110">Die restlichen Paketeigenschaften auf der Registerkarte **Eigenschaften** werden automatisch generiert und können auf dieser Registerkarte nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="bf74f-110">The remainder of the package properties on the **Properties** tab is automatically generated and cannot be modified on this tab.</span></span>

**<span data-ttu-id="bf74f-111">So ändern Sie den Paketnamen oder die Kommentare</span><span class="sxs-lookup"><span data-stu-id="bf74f-111">To change the package name or comments</span></span>**

1.  <span data-ttu-id="bf74f-112">Klicken Sie auf die Registerkarte **Eigenschaften** .</span><span class="sxs-lookup"><span data-stu-id="bf74f-112">Click the **Properties** tab.</span></span>

2.  <span data-ttu-id="bf74f-113">Geben Sie im Textfeld **Paketname** den einzelnen für das Paket verwendeten Namen ein, der mehrere Anwendungen enthalten kann.</span><span class="sxs-lookup"><span data-stu-id="bf74f-113">In the **Package Name** text box, enter or edit the single name used for the package, which can contain multiple applications.</span></span>

3.  <span data-ttu-id="bf74f-114">Geben Sie im Textfeld **Kommentare** optional Kommentare ein, oder bearbeiten Sie Sie.</span><span class="sxs-lookup"><span data-stu-id="bf74f-114">In the **Comments** text box, optionally enter or edit any comments.</span></span> <span data-ttu-id="bf74f-115">Die empfohlene bewährte Vorgehensweise besteht darin, Detailinformationen zum Paket und zur Sequenzierung bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="bf74f-115">The suggested best practice is to provide detail information about the package and sequencing.</span></span>

4.  <span data-ttu-id="bf74f-116">Wählen Sie im Menü **Datei** die Option **Speichern**aus.</span><span class="sxs-lookup"><span data-stu-id="bf74f-116">From the **File** menu, select **Save**.</span></span>

**<span data-ttu-id="bf74f-117">So ändern Sie die Blockgröße</span><span class="sxs-lookup"><span data-stu-id="bf74f-117">To change the block size</span></span>**

1.  <span data-ttu-id="bf74f-118">Klicken Sie auf die Registerkarte **Eigenschaften** .</span><span class="sxs-lookup"><span data-stu-id="bf74f-118">Click the **Properties** tab.</span></span>

2.  <span data-ttu-id="bf74f-119">Wählen Sie in der Dropdownliste **Block Größe** die Option **4 KB**, **16 KB**, **32 KB**oder **64 KB**aus.</span><span class="sxs-lookup"><span data-stu-id="bf74f-119">On the **Block Size** drop-down list, select **4 KB**, **16 KB**, **32 KB**, or **64 KB**.</span></span>

3.  <span data-ttu-id="bf74f-120">Wählen Sie im Menü **Datei** die Option **Speichern**aus.</span><span class="sxs-lookup"><span data-stu-id="bf74f-120">From the **File** menu, select **Save**.</span></span>

## <span data-ttu-id="bf74f-121">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="bf74f-121">Related topics</span></span>


[<span data-ttu-id="bf74f-122">Informationen zur Registerkarte „Eigenschaften“</span><span class="sxs-lookup"><span data-stu-id="bf74f-122">About the Properties Tab</span></span>](about-the-properties-tab.md)

[<span data-ttu-id="bf74f-123">Sequencer Console</span><span class="sxs-lookup"><span data-stu-id="bf74f-123">Sequencer Console</span></span>](sequencer-console.md)

 

 





