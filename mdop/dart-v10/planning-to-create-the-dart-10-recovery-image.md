---
title: Planen der Erstellung des DaRT 10-Wiederherstellungsabbilds
description: Planen der Erstellung des DaRT 10-Wiederherstellungsabbilds
author: dansimp
ms.assetid: a0087d93-b88f-454b-81b2-3c7ce3718023
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 44cf052eaffd19645885618da9104e5b0a50cfd5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809679"
---
# <span data-ttu-id="e4b3c-103">Planen der Erstellung des DaRT 10-Wiederherstellungsabbilds</span><span class="sxs-lookup"><span data-stu-id="e4b3c-103">Planning to Create the DaRT 10 Recovery Image</span></span>


<span data-ttu-id="e4b3c-104">Verwenden Sie die Informationen in diesem Abschnitt, wenn Sie beabsichtigen, das Microsoft Diagnostics and Recovery Toolset (Dart) 10-Wiederherstellungsbild zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="e4b3c-104">Use the information in this section when you are planning to create the Microsoft Diagnostics and Recovery Toolset (DaRT) 10 recovery image.</span></span>

## <span data-ttu-id="e4b3c-105">Planen des Erstellens des DART 10-Wiederherstellungs Bilds</span><span class="sxs-lookup"><span data-stu-id="e4b3c-105">Planning to create the DaRT 10 recovery image</span></span>


<span data-ttu-id="e4b3c-106">Wenn Sie das DART-Wiederherstellungsbild erstellen, müssen Sie entscheiden, welche Tools in das Bild aufgenommen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="e4b3c-106">When you create the DaRT recovery image, you have to decide which tools to include on the image.</span></span> <span data-ttu-id="e4b3c-107">Um die Entscheidung zu treffen, sollten Endbenutzer möglicherweise auf diese Tools zugreifen.</span><span class="sxs-lookup"><span data-stu-id="e4b3c-107">To make the decision, consider that end users may have access to those tools.</span></span> <span data-ttu-id="e4b3c-108">Wenn Supporttechniker die Wiederherstellungsbild Medien auf die Computer der Endbenutzer übertragen, um Probleme zu diagnostizieren, möchten Sie möglicherweise alle Tools auf dem Wiederherstellungsabbild installieren.</span><span class="sxs-lookup"><span data-stu-id="e4b3c-108">If support engineers will take the recovery image media to end users’ computers to diagnose issues, you may want to install all of the tools on the recovery image.</span></span> <span data-ttu-id="e4b3c-109">Wenn Sie beabsichtigen, die Computer des Endbenutzers Remote zu diagnostizieren, möchten Sie möglicherweise einige der Tools wie Datenträger Zurücksetzung und Registrierungs-Editor deaktivieren und dann andere Tools, einschließlich Remote Verbindung, aktivieren.</span><span class="sxs-lookup"><span data-stu-id="e4b3c-109">If you plan to diagnose end user’s computers remotely, you may want to disable some of the tools, such as Disk Wipe and Registry Editor, and then enable other tools, including Remote Connection.</span></span>

<span data-ttu-id="e4b3c-110">Wenn Sie das DART-Wiederherstellungsabbild erstellen, geben Sie auch an, ob Sie weitere Treiber oder Dateien einbeziehen möchten.</span><span class="sxs-lookup"><span data-stu-id="e4b3c-110">When you create the DaRT recovery image, you will also specify whether you want to include additional drivers or files.</span></span> <span data-ttu-id="e4b3c-111">Ermitteln Sie die Speicherorte zusätzlicher Treiber oder Dateien, die Sie in das DART-Wiederherstellungsabbild einbeziehen möchten.</span><span class="sxs-lookup"><span data-stu-id="e4b3c-111">Determine the locations of any additional drivers or files that you want to include on the DaRT recovery image.</span></span>

<span data-ttu-id="e4b3c-112">Weitere Informationen zu den Dart-Tools finden Sie unter [Übersicht über die Tools in DART 10](overview-of-the-tools-in-dart-10.md).</span><span class="sxs-lookup"><span data-stu-id="e4b3c-112">For more information about the DaRT tools, see [Overview of the Tools in DaRT 10](overview-of-the-tools-in-dart-10.md).</span></span> <span data-ttu-id="e4b3c-113">Weitere Informationen dazu, wie Sie bei der Erstellung eines sicheren Wiederherstellungs Bilds helfen können, finden Sie unter [Sicherheitsüberlegungen für Dart 10](security-considerations-for-dart-10.md).</span><span class="sxs-lookup"><span data-stu-id="e4b3c-113">For more information about how to help create a secure recovery image, see [Security Considerations for DaRT 10](security-considerations-for-dart-10.md).</span></span>

## <span data-ttu-id="e4b3c-114">Voraussetzungen für das Wiederherstellungsabbild</span><span class="sxs-lookup"><span data-stu-id="e4b3c-114">Prerequisites for the recovery image</span></span>


<span data-ttu-id="e4b3c-115">Die folgenden Elemente sind für das Erstellen des DART-Wiederherstellungs Bilds erforderlich oder empfohlen:</span><span class="sxs-lookup"><span data-stu-id="e4b3c-115">The following items are required or recommended for creating the DaRT recovery image:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="e4b3c-116">Voraussetzung</span><span class="sxs-lookup"><span data-stu-id="e4b3c-116">Prerequisite</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="e4b3c-117">Details</span><span class="sxs-lookup"><span data-stu-id="e4b3c-117">Details</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e4b3c-118">Windows 10-Quelldateien</span><span class="sxs-lookup"><span data-stu-id="e4b3c-118">Windows 10 source files</span></span></p></td>
<td align="left"><p><span data-ttu-id="e4b3c-119">Erforderlich, um das DART-Wiederherstellungsbild zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="e4b3c-119">Required to create the DaRT recovery image.</span></span> <span data-ttu-id="e4b3c-120">Geben Sie den Pfad einer Windows 10-DVD oder von Windows 10-Quelldateien an.</span><span class="sxs-lookup"><span data-stu-id="e4b3c-120">Provide the path of a Windows 10 DVD or of Windows 10 source files.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e4b3c-121">Windows-Debugging-Tools für Ihre Plattform</span><span class="sxs-lookup"><span data-stu-id="e4b3c-121">Windows Debugging Tools for your platform</span></span></p></td>
<td align="left"><p><span data-ttu-id="e4b3c-122">Erforderlich, wenn Sie den <strong> Absturzanalyse Programm ausführen </strong> , um die Ursache für einen Computer Fehler zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="e4b3c-122">Required when you run the <strong>Crash Analyzer</strong> to determine the cause of a computer failure.</span></span> <span data-ttu-id="e4b3c-123">Wir empfehlen, dass Sie den Pfad der Windows-Debugging-Tools angeben, wenn Sie das DART-Wiederherstellungsabbild erstellen.</span><span class="sxs-lookup"><span data-stu-id="e4b3c-123">We recommend that you specify the path of the Windows Debugging Tools at the time that you create the DaRT recovery image.</span></span> <span data-ttu-id="e4b3c-124">Sie können die Windows-Debugging-Tools hier herunterladen: <a href="https://docs.microsoft.com/windows-hardware/drivers/debugger/" data-raw-source="[Download and Install Debugging Tools for Windows](https://docs.microsoft.com/windows-hardware/drivers/debugger/)"> herunterladen und Installieren von Debugging-Tools für Windows </a> .</span><span class="sxs-lookup"><span data-stu-id="e4b3c-124">You can download the Windows Debugging Tools here: <a href="https://docs.microsoft.com/windows-hardware/drivers/debugger/" data-raw-source="[Download and Install Debugging Tools for Windows](https://docs.microsoft.com/windows-hardware/drivers/debugger/)">Download and Install Debugging Tools for Windows</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e4b3c-125">Optional: Windows-Symbole-Dateien für die Verwendung mit <strong> Crash Analyzer</span><span class="sxs-lookup"><span data-stu-id="e4b3c-125">Optional: Windows symbols files for use with <strong>Crash Analyzer</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="e4b3c-126">In der Regel werden Debuginformationen in einer vom Programm getrennten Symboldatei gespeichert.</span><span class="sxs-lookup"><span data-stu-id="e4b3c-126">Typically, debugging information is stored in a symbol file that is separate from the program.</span></span> <span data-ttu-id="e4b3c-127">Sie müssen Zugriff auf die Symbol Informationen haben, wenn Sie eine Anwendung debuggen, die nicht mehr reagiert, beispielsweise wenn Sie nicht mehr funktioniert.</span><span class="sxs-lookup"><span data-stu-id="e4b3c-127">You must have access to the symbol information when you debug an application that has stopped responding, for example, if it stopped working.</span></span> <span data-ttu-id="e4b3c-128">Weitere Informationen finden Sie unter <a href="diagnosing-system-failures-with-crash-analyzer-dart-10.md" data-raw-source="[Diagnosing System Failures with Crash Analyzer](diagnosing-system-failures-with-crash-analyzer-dart-10.md)"> Diagnostizieren von System Fehlern mit Crash Analyzer </a> .</span><span class="sxs-lookup"><span data-stu-id="e4b3c-128">For more information, see <a href="diagnosing-system-failures-with-crash-analyzer-dart-10.md" data-raw-source="[Diagnosing System Failures with Crash Analyzer](diagnosing-system-failures-with-crash-analyzer-dart-10.md)">Diagnosing System Failures with Crash Analyzer</a>.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="e4b3c-129">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="e4b3c-129">Related topics</span></span>

[<span data-ttu-id="e4b3c-130">Planen der Bereitstellung von DaRT 10</span><span class="sxs-lookup"><span data-stu-id="e4b3c-130">Planning to Deploy DaRT 10</span></span>](planning-to-deploy-dart-10.md)

 

 




