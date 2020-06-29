---
title: So führen Sie Crash Analyzer auf einem Endbenutzercomputer aus
description: So führen Sie Crash Analyzer auf einem Endbenutzercomputer aus
author: dansimp
ms.assetid: 40af4ead-6588-4a81-8eaa-3dc00c397e1d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 943e3956609ae7e24deaca4313036445802a8f7f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810195"
---
# <span data-ttu-id="d99f4-103">So führen Sie Crash Analyzer auf einem Endbenutzercomputer aus</span><span class="sxs-lookup"><span data-stu-id="d99f4-103">How to Run the Crash Analyzer on an End-user Computer</span></span>


<span data-ttu-id="d99f4-104">In der Regel führen Sie den Microsoft Diagnostics and Recovery Toolset (Dart) 7 Crash Analyzer aus dem Fenster Diagnose-und Wiederherstellungs-Toolset auf einem Endbenutzercomputer mit Problemen aus.</span><span class="sxs-lookup"><span data-stu-id="d99f4-104">Typically, you run Microsoft Diagnostics and Recovery Toolset (DaRT)7 Crash Analyzer from the Diagnostics and Recovery Toolset window on an end-user computer that has problems.</span></span> <span data-ttu-id="d99f4-105">Der Absturzanalyse-Analyzer versucht, die Debugging-Tools für Windows auf dem Problem Computer zu finden.</span><span class="sxs-lookup"><span data-stu-id="d99f4-105">The Crash Analyzer tries to locate the Debugging Tools for Windows on the problem computer.</span></span> <span data-ttu-id="d99f4-106">Wenn das Dialogfeld Verzeichnispfad leer ist, müssen Sie den Speicherort eingeben oder den Speicherort der Debugging Tools für Windows Durchsuchen (Sie können die Dateien von Microsoft herunterladen).</span><span class="sxs-lookup"><span data-stu-id="d99f4-106">If the directory path dialog box is empty, you must enter the location or browse to the location of the Debugging Tools for Windows (you can download the files from Microsoft).</span></span> <span data-ttu-id="d99f4-107">Sie müssen auch einen Pfad angeben, in dem sich die Symboldateien befinden.</span><span class="sxs-lookup"><span data-stu-id="d99f4-107">You must also provide a path to where the symbol files are located.</span></span>

**<span data-ttu-id="d99f4-108">So öffnen und führen Sie den Crash Analyzer auf einem Endbenutzercomputer</span><span class="sxs-lookup"><span data-stu-id="d99f4-108">To open and run the Crash Analyzer on an end-user computer</span></span>**

1.  <span data-ttu-id="d99f4-109">Klicken Sie im Fenster **Diagnose-und Wiederherstellungs-Toolset** auf einem Endbenutzercomputer auf **Crash Analyzer**.</span><span class="sxs-lookup"><span data-stu-id="d99f4-109">On the **Diagnostics and Recovery Toolset** window on an end-user computer, click **Crash Analyzer**.</span></span>

2.  <span data-ttu-id="d99f4-110">Geben Sie die erforderlichen Informationen für Folgendes an:</span><span class="sxs-lookup"><span data-stu-id="d99f4-110">Provide the required information for the following:</span></span>

    -   <span data-ttu-id="d99f4-111">Microsoft-Debugging-Tools für Windows</span><span class="sxs-lookup"><span data-stu-id="d99f4-111">Microsoft Debugging Tools for Windows</span></span>

    -   <span data-ttu-id="d99f4-112">Symbol Dateien</span><span class="sxs-lookup"><span data-stu-id="d99f4-112">Symbol files</span></span>

        <span data-ttu-id="d99f4-113">Weitere Informationen zu Symboldateien finden Sie unter [So stellen Sie sicher, dass Crash Analyzer auf Symboldateien zugreifen kann](how-to-ensure-that-crash-analyzer-can-access-symbol-files-dart-7.md).</span><span class="sxs-lookup"><span data-stu-id="d99f4-113">For more information about symbol files, see, [How to Ensure that Crash Analyzer Can Access Symbol Files](how-to-ensure-that-crash-analyzer-can-access-symbol-files-dart-7.md).</span></span>

    -   <span data-ttu-id="d99f4-114">Eine Absturzspeicherabbild Datei</span><span class="sxs-lookup"><span data-stu-id="d99f4-114">A crash dump file</span></span>

        <span data-ttu-id="d99f4-115">Führen Sie die folgenden Schritte aus, um den Speicherort der Absturzspeicherabbild Datei zu ermitteln:</span><span class="sxs-lookup"><span data-stu-id="d99f4-115">Follow these steps to determine the location of the crash dump file:</span></span>

        1.  <span data-ttu-id="d99f4-116">Öffnen Sie das Fenster **System Eigenschaften** .</span><span class="sxs-lookup"><span data-stu-id="d99f4-116">Open the **System Properties** window.</span></span>

            <span data-ttu-id="d99f4-117">Klicken Sie auf **Start**, geben Sie sysdm.cpl ein, und drücken Sie dann die EINGABETASTE.</span><span class="sxs-lookup"><span data-stu-id="d99f4-117">Click **Start**, type sysdm.cpl, and then press Enter.</span></span>

        2.  <span data-ttu-id="d99f4-118">Klicken Sie auf die Registerkarte **Erweitert**.</span><span class="sxs-lookup"><span data-stu-id="d99f4-118">Click the **Advanced** tab.</span></span>

        3.  <span data-ttu-id="d99f4-119">Klicken Sie im Bereich **Start und Wiederherstellung** auf **Einstellungen**.</span><span class="sxs-lookup"><span data-stu-id="d99f4-119">In the **Startup and Recovery** area, click **Settings**.</span></span>

        <span data-ttu-id="d99f4-120">**Hinweis**  Wenn Sie keinen Zugriff auf das Fenster " **System Eigenschaften** " haben, können Sie mithilfe des **Such** Tools in DART nach Dumpdateien auf dem Endbenutzercomputer suchen.</span><span class="sxs-lookup"><span data-stu-id="d99f4-120">**Note** If you do not have access to the **System Properties** window, you can search for dump files on the end-user computer by using the **Search** tool in DaRT.</span></span>

         

3.  <span data-ttu-id="d99f4-121">**Crash Analyzer** scannt die Absturzspeicherabbild Datei und meldet eine mögliche Ursache für den Absturz.</span><span class="sxs-lookup"><span data-stu-id="d99f4-121">The **Crash Analyzer** scans the crash dump file and reports a probable cause of the crash.</span></span> <span data-ttu-id="d99f4-122">Sie können weitere Informationen zum Absturz anzeigen, beispielsweise die spezifische Absturzmeldung und Beschreibung, die zum Zeitpunkt des Absturzes geladenen Treiber und die vollständige Ausgabe der Analyse.</span><span class="sxs-lookup"><span data-stu-id="d99f4-122">You can view more information about the crash, such as the specific crash message and description, the drivers loaded at the time of the crash, and the full output of the analysis.</span></span>

4.  <span data-ttu-id="d99f4-123">Entscheiden Sie sich für eine geeignete Strategie zur Lösung des Problems.</span><span class="sxs-lookup"><span data-stu-id="d99f4-123">Decide upon an appropriate strategy to resolve the problem.</span></span> <span data-ttu-id="d99f4-124">Möglicherweise müssen Sie den Gerätetreiber, der den Absturz verursacht hat, mithilfe des Knotens **Dienste und Treiber** des **Computer Verwaltungs** Tools in DART deaktivieren oder aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="d99f4-124">This may require disabling or updating the device driver that caused the crash by using the **Services and Drivers** node of the **Computer Management** tool in DaRT.</span></span>

## <span data-ttu-id="d99f4-125">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="d99f4-125">Related topics</span></span>


[<span data-ttu-id="d99f4-126">Diagnostizieren von Systemfehlern mit Crash Analyzer</span><span class="sxs-lookup"><span data-stu-id="d99f4-126">Diagnosing System Failures with Crash Analyzer</span></span>](diagnosing-system-failures-with-crash-analyzer--dart-7.md)

 

 





