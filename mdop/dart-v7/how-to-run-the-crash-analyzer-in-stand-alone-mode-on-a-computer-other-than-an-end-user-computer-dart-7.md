---
title: So führen Sie Crash Analyzer im eigenständigen Modus auf einem anderen Computer als einem Endbenutzercomputer aus
description: So führen Sie Crash Analyzer im eigenständigen Modus auf einem anderen Computer als einem Endbenutzercomputer aus
author: dansimp
ms.assetid: 881d573f-2f18-4c5f-838e-2f5320179f94
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6f398c56b7c631145388541b71229d69c16bf6f3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809565"
---
# <span data-ttu-id="6ac20-103">So führen Sie Crash Analyzer im eigenständigen Modus auf einem anderen Computer als einem Endbenutzercomputer aus</span><span class="sxs-lookup"><span data-stu-id="6ac20-103">How to Run the Crash Analyzer in Stand-alone Mode on a Computer Other than an End-user Computer</span></span>


<span data-ttu-id="6ac20-104">Wenn Sie nicht auf die Microsoft Debugging Tools für Windows oder die Symboldateien auf dem Endbenutzercomputer zugreifen können, können Sie die Speicherabbilddatei vom Problem Computer kopieren und auf einem Computer analysieren, auf dem die eigenständige Version von Crash Analyzer installiert ist, beispielsweise den Computer eines Helpdesk-Administrators.</span><span class="sxs-lookup"><span data-stu-id="6ac20-104">If you cannot access the Microsoft Debugging Tools for Windows or the symbol files on the end-user computer, you can copy the dump file from the problem computer and analyze it on a computer that has the stand-alone version of Crash Analyzer installed, such as a helpdesk administrator’s computer.</span></span>

**<span data-ttu-id="6ac20-105">So führen Sie den Crash Analyzer im eigenständigen Modus aus</span><span class="sxs-lookup"><span data-stu-id="6ac20-105">To run the Crash Analyzer in stand-alone mode</span></span>**

1.  <span data-ttu-id="6ac20-106">Klicken Sie auf einem Computer, auf dem **Start**DaRT7 installiert ist, auf  /  **Alle Programme**starten  /  **Microsoft Dart 7**.</span><span class="sxs-lookup"><span data-stu-id="6ac20-106">On a computer with DaRT7 installed, click **Start** / **All Programs** / **Microsoft DaRT 7**.</span></span>

2.  <span data-ttu-id="6ac20-107">Geben Sie die erforderlichen Informationen für Folgendes an:</span><span class="sxs-lookup"><span data-stu-id="6ac20-107">Provide the required information for the following:</span></span>

    -   <span data-ttu-id="6ac20-108">Microsoft-Debugging-Tools für Windows</span><span class="sxs-lookup"><span data-stu-id="6ac20-108">Microsoft Debugging Tools for Windows</span></span>

    -   <span data-ttu-id="6ac20-109">Symbol Dateien</span><span class="sxs-lookup"><span data-stu-id="6ac20-109">Symbol files</span></span>

        <span data-ttu-id="6ac20-110">Weitere Informationen zu Symboldateien finden Sie unter [So stellen Sie sicher, dass Crash Analyzer auf Symboldateien zugreifen kann](how-to-ensure-that-crash-analyzer-can-access-symbol-files-dart-7.md).</span><span class="sxs-lookup"><span data-stu-id="6ac20-110">For more information about symbol files, see, [How to Ensure that Crash Analyzer Can Access Symbol Files](how-to-ensure-that-crash-analyzer-can-access-symbol-files-dart-7.md).</span></span>

    -   <span data-ttu-id="6ac20-111">Eine Absturzspeicherabbild Datei</span><span class="sxs-lookup"><span data-stu-id="6ac20-111">A crash dump file</span></span>

        <span data-ttu-id="6ac20-112">**Hinweis**  Verwenden Sie das Such Tool in DaRT7, um die kopierte Absturzspeicherabbild Datei zu finden.</span><span class="sxs-lookup"><span data-stu-id="6ac20-112">**Note** Use the Search tool in DaRT7 to locate the copied crash dump file.</span></span>

         

3.  <span data-ttu-id="6ac20-113">**Crash Analyzer** scannt die Absturzspeicherabbild Datei und meldet eine mögliche Ursache für den Absturz.</span><span class="sxs-lookup"><span data-stu-id="6ac20-113">The **Crash Analyzer** scans the crash dump file and reports a probable cause of the crash.</span></span> <span data-ttu-id="6ac20-114">Sie können weitere Informationen zum Absturz anzeigen, beispielsweise die spezifische Absturzmeldung und Beschreibung, die zum Zeitpunkt des Absturzes geladenen Treiber und die vollständige Ausgabe der Analyse.</span><span class="sxs-lookup"><span data-stu-id="6ac20-114">You can view more information about the crash, such as the specific crash message and description, the drivers loaded at the time of the crash, and the full output of the analysis.</span></span>

4.  <span data-ttu-id="6ac20-115">Entscheiden Sie sich für eine geeignete Strategie zur Lösung des Problems.</span><span class="sxs-lookup"><span data-stu-id="6ac20-115">Decide upon an appropriate strategy to resolve the problem.</span></span> <span data-ttu-id="6ac20-116">Möglicherweise müssen Sie den Gerätetreiber, der den Absturz verursacht hat, mithilfe des Knotens **Dienste und Treiber** des **Computer Verwaltungs** Tools in DART deaktivieren oder aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="6ac20-116">This may require disabling or updating the device driver that caused the crash by using the **Services and Drivers** node of the **Computer Management** tool in DaRT.</span></span>

## <span data-ttu-id="6ac20-117">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="6ac20-117">Related topics</span></span>


[<span data-ttu-id="6ac20-118">Diagnostizieren von Systemfehlern mit Crash Analyzer</span><span class="sxs-lookup"><span data-stu-id="6ac20-118">Diagnosing System Failures with Crash Analyzer</span></span>](diagnosing-system-failures-with-crash-analyzer--dart-7.md)

 

 





