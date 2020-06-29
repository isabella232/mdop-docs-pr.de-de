---
title: So führen Sie Crash Analyzer auf einem Endbenutzercomputer aus
description: So führen Sie Crash Analyzer auf einem Endbenutzercomputer aus
author: dansimp
ms.assetid: d36213e5-7719-44d7-be65-971c3ef7df2c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 028f1dd0a1651809ec54ae19094302586d864f99
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810513"
---
# <span data-ttu-id="81686-103">So führen Sie Crash Analyzer auf einem Endbenutzercomputer aus</span><span class="sxs-lookup"><span data-stu-id="81686-103">How to Run the Crash Analyzer on an End-user Computer</span></span>


<span data-ttu-id="81686-104">Zum Ausführen von **Crash Analyzer** aus dem Fenster " **Diagnose-und Wiederherstellungs-Toolset** " auf einem Endbenutzercomputer, auf dem Probleme auftreten, müssen die Microsoft-Debugging-Tools für Windows und die Symboldateien installiert sein.</span><span class="sxs-lookup"><span data-stu-id="81686-104">To run **Crash Analyzer** from the **Diagnostics and Recovery Toolset** window on an end-user computer that is experiencing problems, you must have the Microsoft Debugging Tools for Windows and the symbol files installed.</span></span> <span data-ttu-id="81686-105">Informationen zum Herunterladen der Windows-Debugging-Tools finden Sie unter [Debuggen von Tools für Windows](https://go.microsoft.com/fwlink/?LinkId=266248).</span><span class="sxs-lookup"><span data-stu-id="81686-105">To download the Windows Debugging Tools, see [Debugging Tools for Windows](https://go.microsoft.com/fwlink/?LinkId=266248).</span></span>

**<span data-ttu-id="81686-106">So führen Sie den Crash Analyzer auf einem Endbenutzercomputer aus</span><span class="sxs-lookup"><span data-stu-id="81686-106">To run the Crash Analyzer on an end-user computer</span></span>**

1.  <span data-ttu-id="81686-107">Klicken Sie im Fenster **Diagnose-und Wiederherstellungs-Toolset** auf einem Endbenutzercomputer auf **Crash Analyzer**.</span><span class="sxs-lookup"><span data-stu-id="81686-107">On the **Diagnostics and Recovery Toolset** window on an end-user computer, click **Crash Analyzer**.</span></span>

2.  <span data-ttu-id="81686-108">Geben Sie die erforderlichen Informationen für die Microsoft-Debugging-Tools für Windows ein.</span><span class="sxs-lookup"><span data-stu-id="81686-108">Provide the required information for the Microsoft Debugging Tools for Windows.</span></span>

3.  <span data-ttu-id="81686-109">Geben Sie die erforderlichen Informationen für die Symboldateien an.</span><span class="sxs-lookup"><span data-stu-id="81686-109">Provide the required information for the symbol files.</span></span> <span data-ttu-id="81686-110">Weitere Informationen zu Symboldateien finden Sie unter [So stellen Sie sicher, dass Crash Analyzer auf Symboldateien zugreifen kann](how-to-ensure-that-crash-analyzer-can-access-symbol-files.md).</span><span class="sxs-lookup"><span data-stu-id="81686-110">For more information about symbol files, see [How to Ensure that Crash Analyzer Can Access Symbol Files](how-to-ensure-that-crash-analyzer-can-access-symbol-files.md).</span></span>

4.  <span data-ttu-id="81686-111">Geben Sie die erforderlichen Informationen für eine Speicherabbilddatei an.</span><span class="sxs-lookup"><span data-stu-id="81686-111">Provide the required information for a memory dump file.</span></span> <span data-ttu-id="81686-112">So ermitteln Sie den Speicherort der Speicherabbilddatei:</span><span class="sxs-lookup"><span data-stu-id="81686-112">To determine the location of the memory dump file:</span></span>

    1.  <span data-ttu-id="81686-113">Öffnen Sie das Fenster **System Eigenschaften** .</span><span class="sxs-lookup"><span data-stu-id="81686-113">Open the **System Properties** window.</span></span>

    2.  <span data-ttu-id="81686-114">Klicken Sie auf **Start**, geben Sie **sysdm.cpl**ein, und drücken Sie dann die **Eingabe**Taste.</span><span class="sxs-lookup"><span data-stu-id="81686-114">Click **Start**, type **sysdm.cpl**, and then press **Enter**.</span></span>

    3.  <span data-ttu-id="81686-115">Klicken Sie auf die Registerkarte **Erweitert**.</span><span class="sxs-lookup"><span data-stu-id="81686-115">Click the **Advanced** tab.</span></span>

    4.  <span data-ttu-id="81686-116">Klicken Sie im Bereich **Start und Wiederherstellung** auf **Einstellungen**.</span><span class="sxs-lookup"><span data-stu-id="81686-116">In the **Startup and Recovery** area, click **Settings**.</span></span>

        <span data-ttu-id="81686-117">Wenn Sie nicht über Zugriff auf das Fenster **System Eigenschaften** verfügen, können Sie mithilfe des **Such** Tools in Microsoft Diagnostics and Recovery Toolset (Dart) 8,0 nach Dumpdateien auf dem Endbenutzercomputer suchen.</span><span class="sxs-lookup"><span data-stu-id="81686-117">If you do not have access to the **System Properties** window, you can search for dump files on the end-user computer by using the **Search** tool in Microsoft Diagnostics and Recovery Toolset (DaRT) 8.0.</span></span>

    <span data-ttu-id="81686-118">Der **Crash Analyzer** scannt die Speicherabbilddatei und meldet eine mögliche Ursache des Problems.</span><span class="sxs-lookup"><span data-stu-id="81686-118">The **Crash Analyzer** scans the memory dump file and reports a probable cause of the problem.</span></span> <span data-ttu-id="81686-119">Sie können weitere Informationen zu dem Fehler anzeigen, beispielsweise die spezifische Speicherabbild Nachricht und-Beschreibung, die Treiber, die zum Zeitpunkt des Fehlers geladen wurden, und die vollständige Ausgabe der Analyse.</span><span class="sxs-lookup"><span data-stu-id="81686-119">You can view more information about the failure, such as the specific memory dump message and description, the drivers loaded at the time of the failure, and the full output of the analysis.</span></span>

5.  <span data-ttu-id="81686-120">Ermitteln Sie die geeignete Strategie zur Behebung des Problems.</span><span class="sxs-lookup"><span data-stu-id="81686-120">Identify the appropriate strategy to resolve the problem.</span></span> <span data-ttu-id="81686-121">Bei der Strategie kann es erforderlich sein, den Gerätetreiber, der den Fehler verursacht hat, mithilfe des Knotens **Dienste und Treiber** des **Computerverwaltungs** -Tools in Dart 8,0 zu deaktivieren oder zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="81686-121">The strategy may require disabling or updating the device driver that caused the failure by using the **Services and Drivers** node of the **Computer Management** tool in DaRT 8.0.</span></span>

## <span data-ttu-id="81686-122">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="81686-122">Related topics</span></span>


[<span data-ttu-id="81686-123">Diagnostizieren von Systemfehlern mit Crash Analyzer</span><span class="sxs-lookup"><span data-stu-id="81686-123">Diagnosing System Failures with Crash Analyzer</span></span>](diagnosing-system-failures-with-crash-analyzer--dart-8.md)

[<span data-ttu-id="81686-124">Vorgänge für DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="81686-124">Operations for DaRT 8.0</span></span>](operations-for-dart-80-dart-8.md)

 

 





