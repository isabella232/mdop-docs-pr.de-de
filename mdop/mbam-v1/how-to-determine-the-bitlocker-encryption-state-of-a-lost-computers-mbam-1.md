---
title: Wie Sie den BitLocker-Verschlüsselung Zustand von einer nicht mehr auffindbar Computern zu ermitteln
description: Wie Sie den BitLocker-Verschlüsselung Zustand von einer nicht mehr auffindbar Computern zu ermitteln
author: dansimp
ms.assetid: 9440890a-9c63-463b-9113-f46071446388
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d9b977b20ecf219830609c3b1f646a29e6678448
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810468"
---
# <span data-ttu-id="c475c-103">Wie Sie den BitLocker-Verschlüsselung Zustand von einer nicht mehr auffindbar Computern zu ermitteln</span><span class="sxs-lookup"><span data-stu-id="c475c-103">How to Determine the BitLocker Encryption State of a Lost Computers</span></span>


<span data-ttu-id="c475c-104">Mit Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) können Sie den letzten bekannten BitLocker-Verschlüsselungsstatus von verloren gegangenen oder gestohlenen Computern ermitteln.</span><span class="sxs-lookup"><span data-stu-id="c475c-104">Microsoft BitLocker Administration and Monitoring (MBAM) enables you to determine the last known BitLocker encryption status of computers that are lost or stolen.</span></span> <span data-ttu-id="c475c-105">Gehen Sie wie folgt vor, um festzustellen, ob die Volumes auf Computern verschlüsselt wurden, die sich nicht mehr in Ihrem Besitz befinden.</span><span class="sxs-lookup"><span data-stu-id="c475c-105">Use the following procedure to determine whether the volumes have been encrypted on computers that are no longer in your possession.</span></span>

**<span data-ttu-id="c475c-106">Ermitteln des letzten bekannten BitLocker-Verschlüsselungsstatus eines Computers</span><span class="sxs-lookup"><span data-stu-id="c475c-106">Determine a Computer's Last Known BitLocker Encryption state</span></span>**

1.  <span data-ttu-id="c475c-107">Öffnen Sie die MBAM-Website.</span><span class="sxs-lookup"><span data-stu-id="c475c-107">Open the MBAM website.</span></span>

    <span data-ttu-id="c475c-108">**Hinweis**  Die Standardadresse der MBAM-Website lautet http://\* &lt; Computername &gt; \*.</span><span class="sxs-lookup"><span data-stu-id="c475c-108">**Note** The default address for the MBAM website is http://*&lt;computername&gt;*.</span></span> <span data-ttu-id="c475c-109">Verwenden Sie den vollqualifizierten Servernamen, um die Ergebnisse schneller durchsuchen zu können.</span><span class="sxs-lookup"><span data-stu-id="c475c-109">Use the fully qualified server name for faster browsing results.</span></span>

     

2.  <span data-ttu-id="c475c-110">Wählen Sie im Navigationsbereich den Knoten **Bericht** aus, und wählen Sie dann den **Bericht Computer Compliance**aus.</span><span class="sxs-lookup"><span data-stu-id="c475c-110">Select the **Report** node from the navigation pane, and then select the **Computer Compliance Report**.</span></span>

3.  <span data-ttu-id="c475c-111">Verwenden Sie die Filterfelder im rechten Bereich, um die Suchergebnisse einzugrenzen, und klicken Sie dann auf **Suchen**.</span><span class="sxs-lookup"><span data-stu-id="c475c-111">Use the filter fields in the right-side pane to narrow the search results, and then click **Search**.</span></span> <span data-ttu-id="c475c-112">Die Ergebnisse werden unter Ihrer Suchanfrage angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c475c-112">Results will be shown below your search query.</span></span>

4.  <span data-ttu-id="c475c-113">Führen Sie die entsprechenden Schritte aus, die durch ihre Richtlinie für verloren gegangene Geräte festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="c475c-113">Take the appropriate action as determined by your policy for lost devices.</span></span>

    <span data-ttu-id="c475c-114">**Hinweis**  Die Gerätekompatibilität wird von den bereitgestellten BitLocker-Richtlinien bestimmt.</span><span class="sxs-lookup"><span data-stu-id="c475c-114">**Note** Device compliance is determined by the deployed BitLocker policies.</span></span> <span data-ttu-id="c475c-115">Sie sollten diese bereitgestellten Richtlinien überprüfen, wenn Sie versuchen, den BitLocker-Verschlüsselungsstatus eines Geräts zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="c475c-115">You should verify these deployed policies when you are trying to determine the BitLocker encryption state of a device.</span></span>

     

## <span data-ttu-id="c475c-116">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="c475c-116">Related topics</span></span>


[<span data-ttu-id="c475c-117">Verwalten von BitLocker mit MBAM</span><span class="sxs-lookup"><span data-stu-id="c475c-117">Performing BitLocker Management with MBAM</span></span>](performing-bitlocker-management-with-mbam.md)

 

 





