---
title: Diagnostizieren von Systemfehlern mit Crash Analyzer
description: Diagnostizieren von Systemfehlern mit Crash Analyzer
author: dansimp
ms.assetid: ce3d3186-54fb-45b2-b5ce-9bb7841db28f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: abb9d1ec99236199e0866a3b23219dd412bc9da6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810618"
---
# <span data-ttu-id="4fb77-103">Diagnostizieren von Systemfehlern mit Crash Analyzer</span><span class="sxs-lookup"><span data-stu-id="4fb77-103">Diagnosing System Failures with Crash Analyzer</span></span>


<span data-ttu-id="4fb77-104">Mit dem **Crash Analyzer** in Microsoft Diagnostics and Recovery Toolset (Dart) 8,0 können Sie eine Speicherabbilddatei auf einem Windows-basierten Computer Debuggen und dann alle zugehörigen Computer Fehler diagnostizieren.</span><span class="sxs-lookup"><span data-stu-id="4fb77-104">The **Crash Analyzer** in Microsoft Diagnostics and Recovery Toolset (DaRT) 8.0 lets you debug a memory dump file on a Windows-based computer and then diagnose any related computer errors.</span></span> <span data-ttu-id="4fb77-105">Der **Crash-Analyzer** verwendet die Microsoft-Debugging-Tools für Windows, um eine Speicherabbilddatei für den Treiber zu untersuchen, der den Computer fehlerhaft verursacht hat.</span><span class="sxs-lookup"><span data-stu-id="4fb77-105">The **Crash Analyzer** uses the Microsoft Debugging Tools for Windows to examine a memory dump file for the driver that caused the computer to fail.</span></span> <span data-ttu-id="4fb77-106">Sie können Crash Analyzer auf einem Endbenutzercomputer oder im eigenständigen Modus auf einem anderen Computer als einem Endbenutzercomputer ausführen.</span><span class="sxs-lookup"><span data-stu-id="4fb77-106">You can run the Crash Analyzer on an end-user computer or in stand-alone mode on a computer other than an end-user computer.</span></span>

## <span data-ttu-id="4fb77-107">Ausführen von Crash Analyzer auf einem Endbenutzercomputer</span><span class="sxs-lookup"><span data-stu-id="4fb77-107">Run the Crash Analyzer on an end-user-computer</span></span>


<span data-ttu-id="4fb77-108">In der Regel führen Sie **Crash Analyzer** im Fenster **Diagnose-und Wiederherstellungs-Toolset** auf einem Endbenutzercomputer aus, auf dem das Problem auftritt.</span><span class="sxs-lookup"><span data-stu-id="4fb77-108">Typically, you run **Crash Analyzer** from the **Diagnostics and Recovery Toolset** window on an end-user computer that is experiencing the problem.</span></span> <span data-ttu-id="4fb77-109">Der **Absturzanalyse-Analyzer** versucht, die Debugging-Tools für Windows auf dem Problem Computer zu finden.</span><span class="sxs-lookup"><span data-stu-id="4fb77-109">The **Crash Analyzer** tries to locate the Debugging Tools for Windows on the problem computer.</span></span> <span data-ttu-id="4fb77-110">Wenn das Dialogfeld Verzeichnispfad leer ist, müssen Sie den Speicherort eingeben, oder navigieren Sie zum Speicherort der Debugging Tools für Windows (Sie können die Dateien von Microsoft herunterladen).</span><span class="sxs-lookup"><span data-stu-id="4fb77-110">If the directory path dialog box is empty, you must enter the location, or browse to the location of the Debugging Tools for Windows (you can download the files from Microsoft).</span></span> <span data-ttu-id="4fb77-111">Sie müssen auch einen Pfad angeben, in dem sich die Symboldateien befinden.</span><span class="sxs-lookup"><span data-stu-id="4fb77-111">You must also provide a path to where the symbol files are located.</span></span>

<span data-ttu-id="4fb77-112">Wenn Sie die Microsoft-Debugging-Tools für Windows und die Symboldateien beim Erstellen des Dart 8,0-Wiederherstellungsabbilds einbezogen haben, sollten die Tools und Symboldateien verfügbar sein, wenn Sie den **Crash Analyzer** auf dem Problem Computer ausführen.</span><span class="sxs-lookup"><span data-stu-id="4fb77-112">If you included the Microsoft Debugging Tools for Windows and the symbol files when you created the DaRT 8.0 recovery image, the Tools and symbol files should be available when you run the **Crash Analyzer** on the problem computer.</span></span> <span data-ttu-id="4fb77-113">Wenn Sie Sie nicht in das DART-Wiederherstellungsabbild aufgenommen haben, oder wenn die Datenträgergröße oder Netzwerkverbindungsprobleme Sie daran hindern, Sie zu erhalten, können Sie alternativ den Crash Analyzer im eigenständigen Modus auf einem anderen Computer als dem Computer des Endbenutzers ausführen, wie im folgenden Abschnitt beschrieben.</span><span class="sxs-lookup"><span data-stu-id="4fb77-113">If you did not include them in the DaRT recovery image, or if disk size or network connectivity problems are preventing you from obtaining them, you can alternatively run the Crash Analyzer in stand-alone mode on a computer other than the end user’s computer, as described in the following section.</span></span>

[<span data-ttu-id="4fb77-114">So führen Sie Crash Analyzer auf einem Endbenutzercomputer aus</span><span class="sxs-lookup"><span data-stu-id="4fb77-114">How to Run the Crash Analyzer on an End-user Computer</span></span>](how-to-run-the-crash-analyzer-on-an-end-user-computer-dart-8.md)

## <a href="" id="run-the-crash-analyzer-in-stand-alone-mode-on-a-computer-other-than-an-end-user-s-computer"></a><span data-ttu-id="4fb77-115">Ausführen von Crash Analyzer im eigenständigen Modus auf einem anderen Computer als dem Computer eines Endbenutzers</span><span class="sxs-lookup"><span data-stu-id="4fb77-115">Run the Crash Analyzer in stand-alone mode on a computer other than an end user’s computer</span></span>


<span data-ttu-id="4fb77-116">Obwohl Sie in der Regel **Crash Analyzer** auf dem Endbenutzercomputer ausführen, auf dem das Problem auftritt, können Sie den Crash Analyzer auch im eigenständigen Modus auf einem anderen Computer als einem Endbenutzercomputer ausführen.</span><span class="sxs-lookup"><span data-stu-id="4fb77-116">Although you typically run **Crash Analyzer** on the end-user computer that is experiencing the problem, you can also run the Crash Analyzer in stand-alone mode, on a computer other than an end-user computer.</span></span> <span data-ttu-id="4fb77-117">Sie können diese Option auswählen, wenn Sie die Windows-Debugging-Tools nicht in das DART-Wiederherstellungsabbild aufgenommen haben oder wenn die Datenträgergröße oder Netzwerkverbindungsprobleme verhindern, dass Sie die Debugging-Tools erhalten.</span><span class="sxs-lookup"><span data-stu-id="4fb77-117">You might choose this option if you did not include the Windows Debugging Tools in the DaRT recovery image, or if disk size or network connectivity problems are preventing you from obtaining the Debugging Tools.</span></span> <span data-ttu-id="4fb77-118">In diesem Fall können Sie die Speicherabbilddatei vom Problem Computer kopieren und auf einem Computer analysieren, auf dem die eigenständige Version von **Crash Analyzer** installiert ist, beispielsweise auf dem Computer eines Helpdesk-Agents.</span><span class="sxs-lookup"><span data-stu-id="4fb77-118">In this case, you can copy the dump file from the problem computer and analyze it on a computer that has the stand-alone version of **Crash Analyzer** installed, such as on a help desk agent’s computer.</span></span>

[<span data-ttu-id="4fb77-119">So führen Sie Crash Analyzer im eigenständigen Modus auf einem anderen Computer als einem Endbenutzercomputer aus</span><span class="sxs-lookup"><span data-stu-id="4fb77-119">How to Run the Crash Analyzer in Stand-alone Mode on a Computer Other than an End-user Computer</span></span>](how-to-run-the-crash-analyzer-in-stand-alone-mode-on-a-computer-other-than-an-end-user-computer-dart-8.md)

## <span data-ttu-id="4fb77-120">So stellen Sie sicher, dass Crash Analyzer auf Symboldateien zugreifen kann</span><span class="sxs-lookup"><span data-stu-id="4fb77-120">How to ensure that Crash Analyzer can access symbol files</span></span>


<span data-ttu-id="4fb77-121">Zum Debuggen von Anwendungen, die nicht mehr reagiert haben, benötigen Sie Zugriff auf die Symboldatei, die vom Programm getrennt ist.</span><span class="sxs-lookup"><span data-stu-id="4fb77-121">To debug applications that have stopped responding, you need access to the symbol file, which is separate from the program.</span></span> <span data-ttu-id="4fb77-122">Obwohl Symboldateien beim Ausführen von Crash Analyzer automatisch heruntergeladen werden, kann es vorkommen, dass der Problem Computer keinen Zugriff auf das Internet hat.</span><span class="sxs-lookup"><span data-stu-id="4fb77-122">Although symbol files are automatically downloaded when you run Crash Analyzer, there might be times when the problem computer does not have access to the Internet.</span></span> <span data-ttu-id="4fb77-123">Es gibt mehrere Möglichkeiten, um sicherzustellen, dass Ihnen der Zugriff auf Symboldateien garantiert ist.</span><span class="sxs-lookup"><span data-stu-id="4fb77-123">There are several ways to ensure that you have guaranteed access to symbol files.</span></span>

[<span data-ttu-id="4fb77-124">So stellen Sie sicher, dass Crash Analyzer auf Symboldateien zugreifen kann</span><span class="sxs-lookup"><span data-stu-id="4fb77-124">How to Ensure that Crash Analyzer Can Access Symbol Files</span></span>](how-to-ensure-that-crash-analyzer-can-access-symbol-files.md)

## <span data-ttu-id="4fb77-125">Weitere Ressourcen zum Diagnostizieren von Systemfehlern mit Crash Analyzer</span><span class="sxs-lookup"><span data-stu-id="4fb77-125">Other resources for diagnosing system failures with Crash Analyzer</span></span>


[<span data-ttu-id="4fb77-126">Vorgänge für DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="4fb77-126">Operations for DaRT 8.0</span></span>](operations-for-dart-80-dart-8.md)

 

 





