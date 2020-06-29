---
title: So ermitteln Sie den BitLocker-Verschlüsselungsstatus verloren gegangener Computer
description: So ermitteln Sie den BitLocker-Verschlüsselungsstatus verloren gegangener Computer
author: dansimp
ms.assetid: 4f4bec1b-df3e-40ee-b431-291440268d64
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 95fb843b230804417e375946814a585d1d681634
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810576"
---
# <span data-ttu-id="a72fd-103">So ermitteln Sie den BitLocker-Verschlüsselungsstatus verloren gegangener Computer</span><span class="sxs-lookup"><span data-stu-id="a72fd-103">How to Determine BitLocker Encryption State of Lost Computers</span></span>


<span data-ttu-id="a72fd-104">Gehen Sie wie folgt vor, um die Website Verwaltung und Überwachung zu ermitteln:</span><span class="sxs-lookup"><span data-stu-id="a72fd-104">Use this procedure with the Administration and Monitoring Website to determine the following:</span></span>

-   <span data-ttu-id="a72fd-105">Der letzte bekannte BitLocker-Verschlüsselungsstatus von verlorenen oder gestohlenen Computern</span><span class="sxs-lookup"><span data-stu-id="a72fd-105">The last known BitLocker encryption status of lost or stolen computers</span></span>

-   <span data-ttu-id="a72fd-106">Ob die Volumes auf einem verloren gegangenen oder gestohlenen Computer verschlüsselt wurden</span><span class="sxs-lookup"><span data-stu-id="a72fd-106">Whether the volumes on a lost or stolen computer were encrypted</span></span>

<span data-ttu-id="a72fd-107">Zum Ausführen dieser Aufgabe benötigen Sie Zugriff auf den Bereich **Berichte** der Website Verwaltung und Überwachung.</span><span class="sxs-lookup"><span data-stu-id="a72fd-107">To complete this task, you need access to the **Reports** area of the Administration and Monitoring Website.</span></span> <span data-ttu-id="a72fd-108">Um Zugriff auf diesen Bereich zu erhalten, müssen Sie der Rolle MBAM-Berichtsbenutzer zugewiesen sein.</span><span class="sxs-lookup"><span data-stu-id="a72fd-108">To get access to this area, you must be assigned the MBAM Report Users role.</span></span> <span data-ttu-id="a72fd-109">Sie haben diesen Rollen möglicherweise unterschiedliche Namen gegeben, als Sie Sie erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="a72fd-109">You may have given these roles different names when you created them.</span></span> <span data-ttu-id="a72fd-110">Weitere Informationen finden Sie unter [Planen von MBAM 2,5-Gruppen und-Konten](planning-for-mbam-25-groups-and-accounts.md#bkmk-helpdesk-roles).</span><span class="sxs-lookup"><span data-stu-id="a72fd-110">For more information, see [Planning for MBAM 2.5 Groups and Accounts](planning-for-mbam-25-groups-and-accounts.md#bkmk-helpdesk-roles).</span></span>

<span data-ttu-id="a72fd-111">**Hinweis**  Die Gerätekompatibilität hängt von den BitLocker-Richtlinien ab, die Ihr Unternehmen bereitgestellt hat.</span><span class="sxs-lookup"><span data-stu-id="a72fd-111">**Note** Device compliance is determined by the BitLocker policies that your enterprise has deployed.</span></span> <span data-ttu-id="a72fd-112">Möglicherweise möchten Sie die bereitgestellten Richtlinien überprüfen, bevor Sie versuchen, den BitLocker-Verschlüsselungsstatus eines Geräts zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="a72fd-112">You may want to verify your deployed policies before you try to determine the BitLocker encryption state of a device.</span></span>

 

**<span data-ttu-id="a72fd-113">So ermitteln Sie den letzten bekannten BitLocker-Verschlüsselungsstatus von verlorenen Computern</span><span class="sxs-lookup"><span data-stu-id="a72fd-113">To determine the last known BitLocker encryption state of lost computers</span></span>**

1.  <span data-ttu-id="a72fd-114">Öffnen Sie einen Webbrowser, und navigieren Sie zur **Website Verwaltung und Überwachung**.</span><span class="sxs-lookup"><span data-stu-id="a72fd-114">Open a web browser and navigate to the **Administration and Monitoring Website**.</span></span>

2.  <span data-ttu-id="a72fd-115">Wählen Sie im linken Bereich **Berichte** aus, um die Seite Berichte zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="a72fd-115">In the left pane, select **Reports** to open the Reports page.</span></span>

3.  <span data-ttu-id="a72fd-116">Wählen Sie den **Bericht zur Computer Konformität**aus.</span><span class="sxs-lookup"><span data-stu-id="a72fd-116">Select the **Computer Compliance Report**.</span></span>

4.  <span data-ttu-id="a72fd-117">Verwenden Sie die Filterfelder im rechten Bereich, um die Suchergebnisse einzugrenzen, und klicken Sie dann auf **Suchen**.</span><span class="sxs-lookup"><span data-stu-id="a72fd-117">Use the filter fields in the right pane to narrow the search results, and then click **Search**.</span></span> <span data-ttu-id="a72fd-118">Ergebnisse werden unter Ihrer Suchabfrage angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a72fd-118">Results are shown under your search query.</span></span>

5.  <span data-ttu-id="a72fd-119">Führen Sie die entsprechenden Schritte aus, wie es in Ihrer Richtlinie für verloren gegangene Geräte festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="a72fd-119">Take the appropriate action, as determined by your policy for lost devices.</span></span>



## <span data-ttu-id="a72fd-120">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="a72fd-120">Related topics</span></span>


[<span data-ttu-id="a72fd-121">Durchführen der BitLocker-Verwaltung mit MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="a72fd-121">Performing BitLocker Management with MBAM 2.5</span></span>](performing-bitlocker-management-with-mbam-25.md)

 
## <span data-ttu-id="a72fd-122">Sie haben einen Vorschlag für MBAM?</span><span class="sxs-lookup"><span data-stu-id="a72fd-122">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="a72fd-123">[Hier](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)können Sie Vorschläge hinzufügen oder abstimmen.</span><span class="sxs-lookup"><span data-stu-id="a72fd-123">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="a72fd-124">Bei MBAM-Problemen verwenden Sie das [MBAM TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="a72fd-124">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>
 





