---
title: Diagnostizieren von Systemfehlern mit Crash Analyzer
description: Diagnostizieren von Systemfehlern mit Crash Analyzer
author: dansimp
ms.assetid: 170d40ef-4edb-4a32-a349-c285c0ea5e56
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3c5f8b7e189de024d7ceb84f8cfc151dc82d56ed
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809973"
---
# <span data-ttu-id="94e31-103">Diagnostizieren von Systemfehlern mit Crash Analyzer</span><span class="sxs-lookup"><span data-stu-id="94e31-103">Diagnosing System Failures with Crash Analyzer</span></span>


<span data-ttu-id="94e31-104">Mit dem Crash Analyzer in Microsoft Diagnostics and Recovery Toolset (Dart) 7 können Sie eine Absturzspeicherabbild Datei auf einem Windows-basierten Computer Debuggen und dann alle zugehörigen Computer Fehler diagnostizieren.</span><span class="sxs-lookup"><span data-stu-id="94e31-104">The Crash Analyzer in Microsoft Diagnostics and Recovery Toolset (DaRT)7 lets you debug a crash dump file on a Windows-based computer and then diagnose any related computer errors.</span></span> <span data-ttu-id="94e31-105">Der Crash-Analyzer verwendet die Microsoft-Debugging-Tools für Windows, um eine Absturzspeicherabbild Datei für den Treiber zu untersuchen, der den Computer fehlerhaft verursacht hat.</span><span class="sxs-lookup"><span data-stu-id="94e31-105">The Crash Analyzer uses the Microsoft Debugging Tools for Windows to examine a crash dump file for the driver that caused the computer to fail.</span></span>

## <span data-ttu-id="94e31-106">Ausführen von Crash Analyzer auf einem Endbenutzer Computer</span><span class="sxs-lookup"><span data-stu-id="94e31-106">Run the Crash Analyzer on an End-user Computer</span></span>


<span data-ttu-id="94e31-107">In der Regel führen Sie Crash Analyzer im Fenster Diagnose-und Wiederherstellungs-Toolset auf einem Endbenutzercomputer aus, auf dem Probleme auftreten.</span><span class="sxs-lookup"><span data-stu-id="94e31-107">Typically, you run Crash Analyzer from the Diagnostics and Recovery Toolset window on an end-user computer that has problems.</span></span> <span data-ttu-id="94e31-108">Der Absturzanalyse-Analyzer versucht, die Debugging-Tools für Windows auf dem Problem Computer zu finden.</span><span class="sxs-lookup"><span data-stu-id="94e31-108">The Crash Analyzer tries to locate the Debugging Tools for Windows on the problem computer.</span></span> <span data-ttu-id="94e31-109">Wenn das Dialogfeld Verzeichnispfad leer ist, müssen Sie den Speicherort eingeben oder den Speicherort der Debugging Tools für Windows Durchsuchen (Sie können die Dateien von Microsoft herunterladen).</span><span class="sxs-lookup"><span data-stu-id="94e31-109">If the directory path dialog box is empty, you must enter the location or browse to the location of the Debugging Tools for Windows (you can download the files from Microsoft).</span></span> <span data-ttu-id="94e31-110">Sie müssen auch einen Pfad angeben, in dem sich die Symboldateien befinden.</span><span class="sxs-lookup"><span data-stu-id="94e31-110">You must also provide a path to where the symbol files are located.</span></span>

<span data-ttu-id="94e31-111">Wenn Sie die Microsoft-Debugging-Tools für Windows und die Symboldateien beim Erstellen des DART-Wiederherstellungsabbilds einbezogen haben, sollten diese verfügbar sein, wenn Sie den Crash Analyzer auf dem Problem Computer ausführen.</span><span class="sxs-lookup"><span data-stu-id="94e31-111">If you included the Microsoft Debugging Tools for Windows and the symbol files when you created the DaRT recovery image, they should be available when you run the Crash Analyzer on the problem computer.</span></span>

[<span data-ttu-id="94e31-112">So führen Sie Crash Analyzer auf einem Endbenutzercomputer aus</span><span class="sxs-lookup"><span data-stu-id="94e31-112">How to Run the Crash Analyzer on an End-user Computer</span></span>](how-to-run-the-crash-analyzer-on-an-end-user-computer-dart-7.md)

## <span data-ttu-id="94e31-113">Ausführen von Crash Analyzer im eigenständigen Modus auf einem anderen Computer als einem Endbenutzercomputer</span><span class="sxs-lookup"><span data-stu-id="94e31-113">Run the Crash Analyzer in stand-alone mode on a computer other than an end-user computer</span></span>


<span data-ttu-id="94e31-114">Der Absturzanalyse-Analyzer versucht, die Debugging-Tools für Windows auf dem Problem Computer zu finden.</span><span class="sxs-lookup"><span data-stu-id="94e31-114">The Crash Analyzer tries to locate the Debugging Tools for Windows on the problem computer.</span></span> <span data-ttu-id="94e31-115">Wenn das Dialogfeld Verzeichnispfad leer ist, müssen Sie den Speicherort eingeben oder den Speicherort der Debugging Tools für Windows Durchsuchen (Sie können die Dateien von Microsoft herunterladen).</span><span class="sxs-lookup"><span data-stu-id="94e31-115">If the directory path dialog box is empty, you must enter the location or browse to the location of the Debugging Tools for Windows (you can download the files from Microsoft).</span></span> <span data-ttu-id="94e31-116">Sie müssen auch einen Pfad angeben, in dem sich die Symboldateien befinden.</span><span class="sxs-lookup"><span data-stu-id="94e31-116">You must also provide a path to where the symbol files are located.</span></span>

<span data-ttu-id="94e31-117">Wenn Sie die Microsoft-Debugging-Tools für Windows und die Symboldateien beim Erstellen des DART-Wiederherstellungsabbilds nicht einbezogen haben oder wenn die Datenträgergröße oder Netzwerkverbindungsprobleme Sie daran hindern, Sie zu erhalten, können Sie die Speicherabbilddatei vom Problem Computer kopieren und auf einem Computer analysieren, auf dem die eigenständige Version von Crash Analyzer installiert ist. , beispielsweise den Computer eines Helpdesk-Administrators.</span><span class="sxs-lookup"><span data-stu-id="94e31-117">If you did not include the Microsoft Debugging Tools for Windows and the symbol files when you created the DaRT recovery image, or if disk size or network connectivity problems are preventing you from obtaining them, then you can copy the dump file from the problem computer and analyze it on a computer that has the stand-alone version of Crash Analyzer installed, such as a helpdesk administrator’s computer.</span></span>

[<span data-ttu-id="94e31-118">So führen Sie Crash Analyzer im eigenständigen Modus auf einem anderen Computer als einem Endbenutzercomputer aus</span><span class="sxs-lookup"><span data-stu-id="94e31-118">How to Run the Crash Analyzer in Stand-alone Mode on a Computer Other than an End-user Computer</span></span>](how-to-run-the-crash-analyzer-in-stand-alone-mode-on-a-computer-other-than-an-end-user-computer-dart-7.md)

## <span data-ttu-id="94e31-119">Sicherstellen, dass Crash Analyzer auf Symboldateien zugreifen kann</span><span class="sxs-lookup"><span data-stu-id="94e31-119">Ensure that Crash Analyzer can access symbol files</span></span>


<span data-ttu-id="94e31-120">In der Regel werden Debuginformationen in einer Symboldatei gespeichert, die von der ausführbaren Datei getrennt ist.</span><span class="sxs-lookup"><span data-stu-id="94e31-120">Typically, debugging information is stored in a symbol file that is separate from the executable.</span></span> <span data-ttu-id="94e31-121">Sie müssen Zugriff auf die Symbol Informationen haben, wenn Sie eine Anwendung debuggen, die nicht mehr reagiert, beispielsweise wenn Sie abgestürzt ist.</span><span class="sxs-lookup"><span data-stu-id="94e31-121">You must have access to the symbol information when you debug an application that has stopped responding, for example if it crashed.</span></span>

<span data-ttu-id="94e31-122">Symbol Dateien werden beim Ausführen von Crash Analyzer automatisch heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="94e31-122">Symbol files are automatically downloaded when you run Crash Analyzer.</span></span> <span data-ttu-id="94e31-123">Wenn der Computer nicht über eine Internet Verbindung verfügt oder das Netzwerk den Computer für den Zugriff auf einen HTTP-Proxy Server benötigt, können die Symboldateien nicht heruntergeladen werden.</span><span class="sxs-lookup"><span data-stu-id="94e31-123">If the computer does not have an Internet connection or the network requires the computer to access an HTTP proxy server, the symbol files cannot be downloaded.</span></span>

[<span data-ttu-id="94e31-124">So stellen Sie sicher, dass Crash Analyzer auf Symboldateien zugreifen kann</span><span class="sxs-lookup"><span data-stu-id="94e31-124">How to Ensure that Crash Analyzer Can Access Symbol Files</span></span>](how-to-ensure-that-crash-analyzer-can-access-symbol-files-dart-7.md)

## <span data-ttu-id="94e31-125">Weitere Ressourcen zum Diagnostizieren von Systemfehlern mit Crash Analyzer</span><span class="sxs-lookup"><span data-stu-id="94e31-125">Other resources for diagnosing system failures with Crash Analyzer</span></span>


[<span data-ttu-id="94e31-126">Vorgänge für DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="94e31-126">Operations for DaRT 7.0</span></span>](operations-for-dart-70-new-ia.md)

 

 





