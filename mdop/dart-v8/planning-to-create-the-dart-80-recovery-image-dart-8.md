---
title: Planen der Erstellung des DaRT 8.0-Wiederherstellungsabbilds
description: Planen der Erstellung des DaRT 8.0-Wiederherstellungsabbilds
author: dansimp
ms.assetid: cfd0e1e2-c379-4460-b545-3f7be9f33583
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 1d1dc7dc5b3776638523a282d9216b80d4ce9ce1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810777"
---
# <span data-ttu-id="eb2ff-103">Planen der Erstellung des DaRT 8.0-Wiederherstellungsabbilds</span><span class="sxs-lookup"><span data-stu-id="eb2ff-103">Planning to Create the DaRT 8.0 Recovery Image</span></span>


<span data-ttu-id="eb2ff-104">Verwenden Sie die Informationen in diesem Abschnitt, wenn Sie beabsichtigen, das Microsoft Diagnostics and Recovery Toolset (Dart) 8,0-Wiederherstellungsbild zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="eb2ff-104">Use the information in this section when you are planning to create the Microsoft Diagnostics and Recovery Toolset (DaRT) 8.0 recovery image.</span></span>

## <span data-ttu-id="eb2ff-105">Planen des Erstellens des Dart 8,0-Wiederherstellungs Bilds</span><span class="sxs-lookup"><span data-stu-id="eb2ff-105">Planning to create the DaRT 8.0 recovery image</span></span>


<span data-ttu-id="eb2ff-106">Wenn Sie das DART-Wiederherstellungsbild erstellen, müssen Sie entscheiden, welche Tools in das Bild aufgenommen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="eb2ff-106">When you create the DaRT recovery image, you have to decide which tools to include on the image.</span></span> <span data-ttu-id="eb2ff-107">Um die Entscheidung zu treffen, sollten Endbenutzer möglicherweise auf diese Tools zugreifen.</span><span class="sxs-lookup"><span data-stu-id="eb2ff-107">To make the decision, consider that end users may have access to those tools.</span></span> <span data-ttu-id="eb2ff-108">Wenn Supporttechniker die Wiederherstellungsbild Medien auf die Computer der Endbenutzer übertragen, um Probleme zu diagnostizieren, möchten Sie möglicherweise alle Tools auf dem Wiederherstellungsabbild installieren.</span><span class="sxs-lookup"><span data-stu-id="eb2ff-108">If support engineers will take the recovery image media to end users’ computers to diagnose issues, you may want to install all of the tools on the recovery image.</span></span> <span data-ttu-id="eb2ff-109">Wenn Sie beabsichtigen, die Computer des Endbenutzers Remote zu diagnostizieren, möchten Sie möglicherweise einige der Tools wie Datenträger Zurücksetzung und Registrierungs-Editor deaktivieren und dann andere Tools, einschließlich Remote Verbindung, aktivieren.</span><span class="sxs-lookup"><span data-stu-id="eb2ff-109">If you plan to diagnose end user’s computers remotely, you may want to disable some of the tools, such as Disk Wipe and Registry Editor, and then enable other tools, including Remote Connection.</span></span>

<span data-ttu-id="eb2ff-110">Wenn Sie das DART-Wiederherstellungsabbild erstellen, geben Sie auch an, ob Sie weitere Treiber oder Dateien einbeziehen möchten.</span><span class="sxs-lookup"><span data-stu-id="eb2ff-110">When you create the DaRT recovery image, you will also specify whether you want to include additional drivers or files.</span></span> <span data-ttu-id="eb2ff-111">Ermitteln Sie die Speicherorte zusätzlicher Treiber oder Dateien, die Sie in das DART-Wiederherstellungsabbild einbeziehen möchten.</span><span class="sxs-lookup"><span data-stu-id="eb2ff-111">Determine the locations of any additional drivers or files that you want to include on the DaRT recovery image.</span></span>

<span data-ttu-id="eb2ff-112">Weitere Informationen zu den Dart-Tools finden Sie unter [Übersicht über die Tools in Dart 8,0](overview-of-the-tools-in-dart-80-dart-8.md).</span><span class="sxs-lookup"><span data-stu-id="eb2ff-112">For more information about the DaRT tools, see [Overview of the Tools in DaRT 8.0](overview-of-the-tools-in-dart-80-dart-8.md).</span></span> <span data-ttu-id="eb2ff-113">Weitere Informationen dazu, wie Sie bei der Erstellung eines sicheren Wiederherstellungs Bilds helfen können, finden Sie unter [Sicherheitsüberlegungen für Dart 8,0](security-considerations-for-dart-80--dart-8.md).</span><span class="sxs-lookup"><span data-stu-id="eb2ff-113">For more information about how to help create a secure recovery image, see [Security Considerations for DaRT 8.0](security-considerations-for-dart-80--dart-8.md).</span></span>

## <span data-ttu-id="eb2ff-114">Voraussetzungen für das Wiederherstellungsabbild</span><span class="sxs-lookup"><span data-stu-id="eb2ff-114">Prerequisites for the recovery image</span></span>


<span data-ttu-id="eb2ff-115">Die folgenden Elemente sind für das Erstellen des DART-Wiederherstellungs Bilds erforderlich oder empfohlen:</span><span class="sxs-lookup"><span data-stu-id="eb2ff-115">The following items are required or recommended for creating the DaRT recovery image:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="eb2ff-116">Voraussetzung</span><span class="sxs-lookup"><span data-stu-id="eb2ff-116">Prerequisite</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="eb2ff-117">Details</span><span class="sxs-lookup"><span data-stu-id="eb2ff-117">Details</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="eb2ff-118">Windows 8-Quelldateien</span><span class="sxs-lookup"><span data-stu-id="eb2ff-118">Windows 8 source files</span></span></p></td>
<td align="left"><p><span data-ttu-id="eb2ff-119">Erforderlich, um das DART-Wiederherstellungsbild zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="eb2ff-119">Required to create the DaRT recovery image.</span></span> <span data-ttu-id="eb2ff-120">Geben Sie den Pfad einer Windows 8-DVD oder von Windows 8-Quelldateien an.</span><span class="sxs-lookup"><span data-stu-id="eb2ff-120">Provide the path of a Windows 8 DVD or of Windows 8 source files.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="eb2ff-121">Windows-Debugging-Tools für Ihre Plattform</span><span class="sxs-lookup"><span data-stu-id="eb2ff-121">Windows Debugging Tools for your platform</span></span></p></td>
<td align="left"><p><span data-ttu-id="eb2ff-122">Erforderlich, wenn Sie den <strong> Absturzanalyse Programm ausführen </strong> , um die Ursache für einen Computer Fehler zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="eb2ff-122">Required when you run the <strong>Crash Analyzer</strong> to determine the cause of a computer failure.</span></span> <span data-ttu-id="eb2ff-123">Wir empfehlen, dass Sie den Pfad der Windows-Debugging-Tools angeben, wenn Sie das DART-Wiederherstellungsabbild erstellen.</span><span class="sxs-lookup"><span data-stu-id="eb2ff-123">We recommend that you specify the path of the Windows Debugging Tools at the time that you create the DaRT recovery image.</span></span> <span data-ttu-id="eb2ff-124">Sie können die Windows-Debugging-Tools hier herunterladen: <a href="https://go.microsoft.com/fwlink/?LinkId=99934" data-raw-source="[Download and Install Debugging Tools for Windows](https://go.microsoft.com/fwlink/?LinkId=99934)"> herunterladen und Installieren von Debugging-Tools für Windows </a> .</span><span class="sxs-lookup"><span data-stu-id="eb2ff-124">You can download the Windows Debugging Tools here: <a href="https://go.microsoft.com/fwlink/?LinkId=99934" data-raw-source="[Download and Install Debugging Tools for Windows](https://go.microsoft.com/fwlink/?LinkId=99934)">Download and Install Debugging Tools for Windows</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="eb2ff-125">Optional: <strong> Defender- </strong> Definitionen</span><span class="sxs-lookup"><span data-stu-id="eb2ff-125">Optional: <strong>Defender</strong> definitions</span></span></p></td>
<td align="left"><p><span data-ttu-id="eb2ff-126">Die neuesten Definitionen für <strong> Defender </strong> sind erforderlich, wenn Sie <strong> Defender ausführen </strong> .</span><span class="sxs-lookup"><span data-stu-id="eb2ff-126">The latest definitions for <strong>Defender</strong> are required when you run <strong>Defender</strong>.</span></span> <span data-ttu-id="eb2ff-127">Obwohl Sie die Definitionen beim Ausführen <strong> von Defender herunterladen können </strong> , empfehlen wir, dass Sie die neuesten Definitionen zum Zeitpunkt der Erstellung des DART-Wiederherstellungsabbilds herunterladen, damit Sie das Tool weiterhin mit den neuesten Definitionen ausführen können, auch wenn der Problem Computer nicht über Netzwerkkonnektivität verfügt.</span><span class="sxs-lookup"><span data-stu-id="eb2ff-127">Although you can download the definitions when you run <strong>Defender</strong>, we recommend that you download the latest definitions at the time you create the DaRT recovery image so that you can still run the tool with the latest definitions even if the problem computer does not have network connectivity.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="eb2ff-128">Optional: Windows-Symbole-Dateien für die Verwendung mit <strong> Crash Analyzer</span><span class="sxs-lookup"><span data-stu-id="eb2ff-128">Optional: Windows symbols files for use with <strong>Crash Analyzer</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="eb2ff-129">In der Regel werden Debuginformationen in einer vom Programm getrennten Symboldatei gespeichert.</span><span class="sxs-lookup"><span data-stu-id="eb2ff-129">Typically, debugging information is stored in a symbol file that is separate from the program.</span></span> <span data-ttu-id="eb2ff-130">Sie müssen Zugriff auf die Symbol Informationen haben, wenn Sie eine Anwendung debuggen, die nicht mehr reagiert, beispielsweise wenn Sie nicht mehr funktioniert.</span><span class="sxs-lookup"><span data-stu-id="eb2ff-130">You must have access to the symbol information when you debug an application that has stopped responding, for example, if it stopped working.</span></span> <span data-ttu-id="eb2ff-131">Weitere Informationen finden Sie unter <a href="diagnosing-system-failures-with-crash-analyzer--dart-8.md" data-raw-source="[Diagnosing System Failures with Crash Analyzer](diagnosing-system-failures-with-crash-analyzer--dart-8.md)"> Diagnostizieren von System Fehlern mit Crash Analyzer </a> .</span><span class="sxs-lookup"><span data-stu-id="eb2ff-131">For more information, see <a href="diagnosing-system-failures-with-crash-analyzer--dart-8.md" data-raw-source="[Diagnosing System Failures with Crash Analyzer](diagnosing-system-failures-with-crash-analyzer--dart-8.md)">Diagnosing System Failures with Crash Analyzer</a>.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="eb2ff-132">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="eb2ff-132">Related topics</span></span>


[<span data-ttu-id="eb2ff-133">Planen der Bereitstellung von DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="eb2ff-133">Planning to Deploy DaRT 8.0</span></span>](planning-to-deploy-dart-80-dart-8.md)

 

 





