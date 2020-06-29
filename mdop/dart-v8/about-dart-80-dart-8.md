---
title: Informationen zu DaRT 8.0
description: Informationen zu DaRT 8.0
author: dansimp
ms.assetid: ce91efd6-7d78-44cb-bb8f-1f43f768ebaa
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: e70816425dc4775b11596b91d7b5c0045830c6ad
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808662"
---
# <span data-ttu-id="5cde1-103">Informationen zu DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="5cde1-103">About DaRT 8.0</span></span>


<span data-ttu-id="5cde1-104">Microsoft Diagnostics and Recovery Toolset (Dart) 8,0 unterstützt Sie bei der Problembehandlung und Reparatur von Windows-basierten Computern.</span><span class="sxs-lookup"><span data-stu-id="5cde1-104">Microsoft Diagnostics and Recovery Toolset (DaRT) 8.0 helps you troubleshoot and repair Windows-based computers.</span></span> <span data-ttu-id="5cde1-105">Dazu gehören die Computer, die nicht gestartet werden können.</span><span class="sxs-lookup"><span data-stu-id="5cde1-105">This includes those computers that cannot be started.</span></span> <span data-ttu-id="5cde1-106">Dart 8,0 ist ein leistungsfähiger Satz von Tools, die die Windows-Wiederherstellungsumgebung (WinRE) erweitern.</span><span class="sxs-lookup"><span data-stu-id="5cde1-106">DaRT 8.0 is a powerful set of tools that extend the Windows Recovery Environment (WinRE).</span></span> <span data-ttu-id="5cde1-107">Mithilfe von DART können Sie ein Problem analysieren, um dessen Ursache zu ermitteln, beispielsweise indem Sie das Ereignisprotokoll oder die Systemregistrierung des Computers überprüfen.</span><span class="sxs-lookup"><span data-stu-id="5cde1-107">By using DaRT, you can analyze an issue to determine its cause, for example, by inspecting the computer’s event log or system registry.</span></span> <span data-ttu-id="5cde1-108">DART unterstützt die Wiederherstellung von grundlegenden Festplatten, die Partitionen enthalten, beispielsweise primäre Partitionen und logische Laufwerke, und unterstützt die Wiederherstellung von Volumes.</span><span class="sxs-lookup"><span data-stu-id="5cde1-108">DaRT supports the recovery of basic hard disks that contain partitions, for example, primary partitions and logical drives, and supports the recovery of volumes.</span></span>

<span data-ttu-id="5cde1-109">**Hinweis**  DART unterstützt die Wiederherstellung von dynamischen Datenträgern nicht.</span><span class="sxs-lookup"><span data-stu-id="5cde1-109">**Note** DaRT does not support the recovery of dynamic disks.</span></span>

 

<span data-ttu-id="5cde1-110">DART bietet auch Tools, mit denen Sie ein Problem beheben können, sobald Sie die Ursache ermitteln.</span><span class="sxs-lookup"><span data-stu-id="5cde1-110">DaRT also provides tools to help you fix a problem as soon as you determine the cause.</span></span> <span data-ttu-id="5cde1-111">So können Sie beispielsweise die Tools in DART verwenden, um einen fehlerhaften Gerätetreiber zu deaktivieren, Hotfixes zu entfernen, gelöschte Dateien wiederherzustellen und den Computer auf Malware zu überprüfen, auch wenn Sie das installierte Windows-Betriebssystem nicht starten können oder sollten.</span><span class="sxs-lookup"><span data-stu-id="5cde1-111">For example, you can use the tools in DaRT to disable a faulty device driver, remove hotfixes, restore deleted files, and scan the computer for malware even when you cannot or should not start the installed Windows operating system.</span></span>

<span data-ttu-id="5cde1-112">Dart kann Ihnen dabei helfen, Computer mit einer 32-Bit-oder 64-Bit-Version von Windows 8 schnell wiederherzustellen, und zwar in der Regel in kürzerer Zeit, als wenn Sie den Computer umbilden würden.</span><span class="sxs-lookup"><span data-stu-id="5cde1-112">DaRT can help you quickly recover computers that are running either 32-bit or 64-bit versions of Windows 8, typically in less time than it would take to reimage the computer.</span></span>

<span data-ttu-id="5cde1-113">Mit der Funktion in DART können Sie ein Wiederherstellungsabbild erstellen.</span><span class="sxs-lookup"><span data-stu-id="5cde1-113">Functionality in DaRT lets you create a recovery image.</span></span> <span data-ttu-id="5cde1-114">Das Wiederherstellungsabbild startet die Windows-Wiederherstellungsumgebung (Windows RE), auf der Sie das Fenster **Diagnose-und Wiederherstellungs-Toolset** starten und auf die Dart-Tools zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="5cde1-114">The recovery image starts Windows Recovery Environment (Windows RE), from which you can start the **Diagnostics and Recovery Toolset** window and access the DaRT tools.</span></span>

<span data-ttu-id="5cde1-115">Verwenden Sie den **Dart-Wiederherstellungsbild-Assistenten** zum Erstellen des DART-Wiederherstellungs Bilds.</span><span class="sxs-lookup"><span data-stu-id="5cde1-115">Use the **DaRT Recovery Image Wizard** to create the DaRT recovery image.</span></span> <span data-ttu-id="5cde1-116">Standardmäßig erstellt der Assistent eine Image-Datei für die internationale Organisation für Standardisierung (ISO) und eine WIM-Datei (Windows Imaging Format) und ermöglicht das Brennen des Bilds auf eine CD, DVD oder USB.</span><span class="sxs-lookup"><span data-stu-id="5cde1-116">By default, the wizard creates an International Organization for Standardization (ISO) image file and a Windows Imaging Format (WIM) file and let you burn the image to a CD, DVD, or USB.</span></span> <span data-ttu-id="5cde1-117">Sie können das Bild lokal auf den Computern des Endbenutzers bereitstellen, oder Sie können es von einer Remotenetzwerk Partition oder einer Wiederherstellungspartition auf der lokalen Festplatte bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="5cde1-117">You can deploy the image locally at end user’s computers, or you can deploy it from a remote network partition or a recovery partition on the local hard drive.</span></span>

## <a href="" id="what-s-new-in-dart-8-0"></a><span data-ttu-id="5cde1-118">Neuerungen in Dart 8,0</span><span class="sxs-lookup"><span data-stu-id="5cde1-118">What’s new in DaRT 8.0</span></span>


<span data-ttu-id="5cde1-119">Dart 8,0 kann Ihnen dabei helfen, Computer mit einer 32-Bit-oder 64-Bit-Version von Windows 8 schnell wiederherzustellen, in der Regel in kürzerer Zeit, als es für die Neubildung des Computers dauern würde.</span><span class="sxs-lookup"><span data-stu-id="5cde1-119">DaRT 8.0 can help you quickly recover computers that are running either 32-bit or 64-bit versions of Windows 8, typically in less time than it would take to reimage the computer.</span></span> <span data-ttu-id="5cde1-120">Dart 8,0 verfügt über die folgenden neuen Features.</span><span class="sxs-lookup"><span data-stu-id="5cde1-120">DaRT 8.0 has the following new features.</span></span>

### <span data-ttu-id="5cde1-121">Erstellen von DART-Bildern mithilfe von Windows 8 oder Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5cde1-121">Create DaRT images by using Windows 8 or Windows Server 2012</span></span>

<span data-ttu-id="5cde1-122">Dart 8,0 ermöglicht Ihnen, Dart-Bilder mithilfe von Windows® 8 oder Windows Server® 2012 zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="5cde1-122">DaRT 8.0 enables you to create DaRT images using either Windows® 8 or Windows Server® 2012.</span></span> <span data-ttu-id="5cde1-123">Für Windows-Versionen, die älter als Windows 8 und Windows Server 2012 sind, sollten Kunden weiterhin frühere Versionen von DART verwenden.</span><span class="sxs-lookup"><span data-stu-id="5cde1-123">For versions of Windows earlier than Windows 8 and Windows Server 2012, customers should continue to use earlier versions of DaRT.</span></span>

### <span data-ttu-id="5cde1-124">Generieren von 32-und 64-Bit-Bildern auf einem Computer</span><span class="sxs-lookup"><span data-stu-id="5cde1-124">Generate both 32- and 64-bit images from one computer</span></span>

<span data-ttu-id="5cde1-125">Dart 8,0 ermöglicht Ihnen, sowohl 32-Bit-als auch 64-Bit-Bilder von einem einzelnen Computer zu generieren, auf dem Dart ausgeführt wird, unabhängig davon, ob es sich bei dem Computer um einen 32-Bit-oder 64-Bit-Computer handelt.</span><span class="sxs-lookup"><span data-stu-id="5cde1-125">DaRT 8.0 enables you to generate both 32-bit and 64-bit images from a single computer that is running DaRT, regardless of whether the computer is a 32-bit or 64-bit computer.</span></span> <span data-ttu-id="5cde1-126">In DaRT7 musste das erstellte Bild identisch sein, wie der Computer, auf dem Dart ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="5cde1-126">In DaRT7, the image that was created had to be the same, bit-wise, as the computer that was running DaRT.</span></span>

### <span data-ttu-id="5cde1-127">Erstellen eines Bilds, das Computer unterstützt, die über eine BIOS-oder UEFI-Schnittstelle verfügen</span><span class="sxs-lookup"><span data-stu-id="5cde1-127">Create one image that supports computers that have either a BIOS or UEFI interface</span></span>

<span data-ttu-id="5cde1-128">Die Unterstützung von Dart 8.0 für die Unified Extensible Firmware Interface (UEFI)-und BIOS-Schnittstellen ermöglicht es Ihnen, nur ein Bild zu erstellen, das mit Computern mit einer der beiden Schnittstellen funktioniert.</span><span class="sxs-lookup"><span data-stu-id="5cde1-128">DaRT 8.0’s support for both the Unified Extensible Firmware Interface (UEFI) and BIOS interfaces enables you to create just one image that works with computers that have either interface.</span></span>

### <span data-ttu-id="5cde1-129">Verwenden einer GUID-Partitionstabelle (GPT) für die Partitionierung</span><span class="sxs-lookup"><span data-stu-id="5cde1-129">Use a GUID partition table (GPT) for partitioning</span></span>

<span data-ttu-id="5cde1-130">Dart 8,0-Tools unterstützen jetzt Windows 8 GPT-Datenträger, die einen flexibleren Mechanismus für die Partitionierung von Datenträgern bereitstellen, als das MBR-Partitionierungsschema (Master Boot Record).</span><span class="sxs-lookup"><span data-stu-id="5cde1-130">DaRT 8.0 tools now support Windows 8 GPT disks, which provide a more flexible mechanism for partitioning disks than the older master boot record (MBR) partitioning scheme.</span></span> <span data-ttu-id="5cde1-131">Dart 8,0-Tools unterstützen weiterhin die MBR-Partitionierung.</span><span class="sxs-lookup"><span data-stu-id="5cde1-131">DaRT 8.0 tools continue to support MBR partitioning.</span></span>

### <span data-ttu-id="5cde1-132">Installieren von Windows 8 und Windows Server 2012 auf der lokalen Festplatte</span><span class="sxs-lookup"><span data-stu-id="5cde1-132">Install Windows 8 and Windows Server 2012 on the local hard disk</span></span>

<span data-ttu-id="5cde1-133">Dart 8,0-Tools können nur verwendet werden, wenn Windows 8 und Windows Server 2012 auf der lokalen Festplatte installiert sind.</span><span class="sxs-lookup"><span data-stu-id="5cde1-133">DaRT 8.0 tools can be used only when Windows 8 and Windows Server 2012 are installed on the local hard disk.</span></span> <span data-ttu-id="5cde1-134">Derzeit gibt es keine Unterstützung für Windows to go.</span><span class="sxs-lookup"><span data-stu-id="5cde1-134">Currently, there is no support for Windows To Go.</span></span>

### <a href="" id="-------------dart-8-0-release-notes"></a> <span data-ttu-id="5cde1-135">Dart 8,0-Versionshinweise</span><span class="sxs-lookup"><span data-stu-id="5cde1-135">DaRT 8.0 release notes</span></span>

<span data-ttu-id="5cde1-136">Weitere Informationen und aktuelle Nachrichten, die nicht in die Dokumentation eingehen, finden Sie in den Versionshinweisen [zu Dart 8,0](release-notes-for-dart-80--dart-8.md).</span><span class="sxs-lookup"><span data-stu-id="5cde1-136">For more information, and for late-breaking news that did not make it into the documentation, see the [Release Notes for DaRT 8.0](release-notes-for-dart-80--dart-8.md).</span></span>

## <span data-ttu-id="5cde1-137">So erhalten Sie Dart 8,0</span><span class="sxs-lookup"><span data-stu-id="5cde1-137">How to Get DaRT 8.0</span></span>


<span data-ttu-id="5cde1-138">Diese Technologie ist Teil des Microsoft Desktop Optimization Pack (MDOP).</span><span class="sxs-lookup"><span data-stu-id="5cde1-138">This technology is a part of the Microsoft Desktop Optimization Pack (MDOP).</span></span> <span data-ttu-id="5cde1-139">MDOP ist Teil von Microsoft Software Assurance.</span><span class="sxs-lookup"><span data-stu-id="5cde1-139">MDOP is part of Microsoft Software Assurance.</span></span> <span data-ttu-id="5cde1-140">Weitere Informationen zur Microsoft-Software Assurance und zum Erwerb von MDOP finden Sie unter [wie erhalte ich MDOP](https://go.microsoft.com/fwlink/?LinkId=322049) ( https://go.microsoft.com/fwlink/?LinkId=322049) .</span><span class="sxs-lookup"><span data-stu-id="5cde1-140">For more information about Microsoft Software Assurance and acquiring MDOP, see [How Do I Get MDOP](https://go.microsoft.com/fwlink/?LinkId=322049) (https://go.microsoft.com/fwlink/?LinkId=322049).</span></span>

## <span data-ttu-id="5cde1-141">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="5cde1-141">Related topics</span></span>


[<span data-ttu-id="5cde1-142">Erste Schritte mit DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="5cde1-142">Getting Started with DaRT 8.0</span></span>](getting-started-with-dart-80-dart-8.md)

[<span data-ttu-id="5cde1-143">Versionshinweise für DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="5cde1-143">Release Notes for DaRT 8.0</span></span>](release-notes-for-dart-80--dart-8.md)

 

 





