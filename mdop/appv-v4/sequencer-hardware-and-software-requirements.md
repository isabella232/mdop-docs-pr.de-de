---
title: Hardware- und Softwareanforderungen für Sequencer
description: Hardware- und Softwareanforderungen für Sequencer
author: dansimp
ms.assetid: 36084e12-831d-452f-a4a4-45f07f9ce471
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0d4e12a5803a3c9033513424826b49bc0bca5885
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806344"
---
# <span data-ttu-id="617b6-103">Hardware- und Softwareanforderungen für Sequencer</span><span class="sxs-lookup"><span data-stu-id="617b6-103">Sequencer Hardware and Software Requirements</span></span>


<span data-ttu-id="617b6-104">In diesem Thema werden die Mindestanforderungen für Hardware und Software für den Computer beschrieben, auf dem der Microsoft Application Virtualization (App-V)-Sequenzer ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="617b6-104">This topic describes the minimum recommended hardware and software requirements for the computer running the Microsoft Application Virtualization (App-V) Sequencer.</span></span>

<span data-ttu-id="617b6-105">Bevor Sie den Sequencer installieren und nachdem Sie die einzelnen Anwendungen sequenziert haben, müssen Sie ein sauberes Betriebssystemabbild auf dem Sequenzcomputer wiederherstellen.</span><span class="sxs-lookup"><span data-stu-id="617b6-105">Before you install the Sequencer and after you sequence each application, you must restore a clean operating system image to the sequencing computer.</span></span> <span data-ttu-id="617b6-106">Mit einer der folgenden Methoden können Sie den Computer wiederherstellen, auf dem der Sequencer ausgeführt wird:</span><span class="sxs-lookup"><span data-stu-id="617b6-106">You can use one of the following methods to restore the computer running the Sequencer:</span></span>

-   <span data-ttu-id="617b6-107">Formatieren Sie die Festplatte neu, und installieren Sie das Betriebssystem erneut.</span><span class="sxs-lookup"><span data-stu-id="617b6-107">Reformat the hard drive and reinstall the operating system.</span></span>

-   <span data-ttu-id="617b6-108">Wiederherstellen der Festplatte auf dem Computer, auf dem das Sequenzer-Image ausgeführt wird, mithilfe einer anderen Datenträger-Imaging-Software.</span><span class="sxs-lookup"><span data-stu-id="617b6-108">Restore the hard drive on the computer running the Sequencer image by using another disk-imaging software.</span></span>

<span data-ttu-id="617b6-109">In der folgenden Liste werden die empfohlenen Hardwareanforderungen für die Ausführung des App-V-Sequencers erläutert.</span><span class="sxs-lookup"><span data-stu-id="617b6-109">The following list outlines the recommended hardware requirements for running the App-V Sequencer.</span></span>

### <a href="" id="hardware-requirements-"></a><span data-ttu-id="617b6-110">Hardwareanforderungen</span><span class="sxs-lookup"><span data-stu-id="617b6-110">Hardware Requirements</span></span>

-   <span data-ttu-id="617b6-111">Prozessor: Intel Pentium III, 1 GHz (32-Bit oder 64-Bit).</span><span class="sxs-lookup"><span data-stu-id="617b6-111">Processor—Intel Pentium III, 1 GHz (32-bit or 64-bit).</span></span> <span data-ttu-id="617b6-112">Der Sequenzierungsprozess ist ein Single-Thread-Prozess und nutzt keine dualen Prozessoren.</span><span class="sxs-lookup"><span data-stu-id="617b6-112">The sequencing process is a single-threaded process and does not take advantage of dual processors.</span></span>

-   <span data-ttu-id="617b6-113">Arbeitsspeicher – 1GB oder höher, 2 GB empfohlen.</span><span class="sxs-lookup"><span data-stu-id="617b6-113">Memory—1GB or above, 2 GB recommended.</span></span>

-   <span data-ttu-id="617b6-114">Festplatte – 40 Gigabyte (GB) Festplattenspeicher mit einem verfügbaren Festplattenspeicherplatz von 15 GB.</span><span class="sxs-lookup"><span data-stu-id="617b6-114">Hard Disk—40 gigabyte (GB) hard disk space with a minimum of 15 GB available hard disk space.</span></span> <span data-ttu-id="617b6-115">Wir empfehlen, dass Sie mindestens dreimal so viel Festplattenspeicherplatz haben, wie es für die von Ihnen sequenzierte Anwendung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="617b6-115">We recommend that you have at least three times the hard disk space that the application you are sequencing requires.</span></span>

    <span data-ttu-id="617b6-116">**Hinweis**  Für die Sequenzierung ist eine starke Datenträgernutzung erforderlich.</span><span class="sxs-lookup"><span data-stu-id="617b6-116">**Note** Sequencing requires heavy disk usage.</span></span> <span data-ttu-id="617b6-117">Eine schnelle Festplattengeschwindigkeit kann die Sequenzierungs Zeit verkleinern.</span><span class="sxs-lookup"><span data-stu-id="617b6-117">A fast disk speed can decrease the sequencing time.</span></span>

     

### <span data-ttu-id="617b6-118">Software Anforderungen</span><span class="sxs-lookup"><span data-stu-id="617b6-118">Software Requirements</span></span>

<span data-ttu-id="617b6-119">In der folgenden Liste werden die unterstützten Betriebssysteme für die Ausführung des Sequencers erläutert.</span><span class="sxs-lookup"><span data-stu-id="617b6-119">The following list outlines the supported operating systems for running the Sequencer.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="617b6-120">Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="617b6-120">Operating System</span></span></th>
<th align="left"><span data-ttu-id="617b6-121">Edition</span><span class="sxs-lookup"><span data-stu-id="617b6-121">Edition</span></span></th>
<th align="left"><span data-ttu-id="617b6-122">Service Pack</span><span class="sxs-lookup"><span data-stu-id="617b6-122">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="617b6-123">System Architektur</span><span class="sxs-lookup"><span data-stu-id="617b6-123">System Architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="617b6-124">WindowsXP</span><span class="sxs-lookup"><span data-stu-id="617b6-124">WindowsXP</span></span></p></td>
<td align="left"><p><span data-ttu-id="617b6-125">Professional</span><span class="sxs-lookup"><span data-stu-id="617b6-125">Professional</span></span></p></td>
<td align="left"><p><span data-ttu-id="617b6-126">SP2 oder SP3</span><span class="sxs-lookup"><span data-stu-id="617b6-126">SP2 or SP3</span></span></p></td>
<td align="left"><p><span data-ttu-id="617b6-127">x86</span><span class="sxs-lookup"><span data-stu-id="617b6-127">x86</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="617b6-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="617b6-128">Windows Vista</span></span></p></td>
<td align="left"><p><span data-ttu-id="617b6-129">Business, Enterprise oder Ultimate</span><span class="sxs-lookup"><span data-stu-id="617b6-129">Business, Enterprise, or Ultimate</span></span></p></td>
<td align="left"><p><span data-ttu-id="617b6-130">Kein Service Pack, SP1 oder SP2</span><span class="sxs-lookup"><span data-stu-id="617b6-130">No service pack, SP1, or SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="617b6-131">x86</span><span class="sxs-lookup"><span data-stu-id="617b6-131">x86</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="617b6-132">Windows7 ¹</span><span class="sxs-lookup"><span data-stu-id="617b6-132">Windows7¹</span></span></p></td>
<td align="left"><p><span data-ttu-id="617b6-133">Professional, Enterprise oder Ultimate</span><span class="sxs-lookup"><span data-stu-id="617b6-133">Professional, Enterprise, or Ultimate</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="617b6-134">x86</span><span class="sxs-lookup"><span data-stu-id="617b6-134">x86</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="617b6-135">¹ unterstützt für App-v 4,5 mit SP1 oder SP2 und nur App-v 4,6</span><span class="sxs-lookup"><span data-stu-id="617b6-135">¹Supported for App-V 4.5 with SP1 or SP2, and App-V 4.6 only</span></span>

<span data-ttu-id="617b6-136">**Hinweis**  Der Application Virtualization (App-V) 4,6-Sequenzer unterstützt 32-Bit-und 64-Bit-Versionen dieser Betriebssysteme.</span><span class="sxs-lookup"><span data-stu-id="617b6-136">**Note** The Application Virtualization (App-V) 4.6 Sequencer supports 32-bit and 64-bit versions of these operating systems.</span></span>

 

<span data-ttu-id="617b6-137">Sie sollten Computer, auf denen der Sequencer ausgeführt wird, mit denselben Anwendungen konfigurieren, die auf Zielcomputern installiert sind.</span><span class="sxs-lookup"><span data-stu-id="617b6-137">You should configure computers running the Sequencer with the same applications that are installed on target computers.</span></span>

### <span data-ttu-id="617b6-138">Software Anforderungen für Remote Desktop Dienste</span><span class="sxs-lookup"><span data-stu-id="617b6-138">Software Requirements for Remote Desktop Services</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="617b6-139">Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="617b6-139">Operating System</span></span></th>
<th align="left"><span data-ttu-id="617b6-140">Edition</span><span class="sxs-lookup"><span data-stu-id="617b6-140">Edition</span></span></th>
<th align="left"><span data-ttu-id="617b6-141">Service Pack</span><span class="sxs-lookup"><span data-stu-id="617b6-141">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="617b6-142">System Architektur</span><span class="sxs-lookup"><span data-stu-id="617b6-142">System Architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="617b6-143">Windows Server2003</span><span class="sxs-lookup"><span data-stu-id="617b6-143">Windows Server2003</span></span></p></td>
<td align="left"><p><span data-ttu-id="617b6-144">Standard Edition, Enterprise Edition oder Datacenter Edition</span><span class="sxs-lookup"><span data-stu-id="617b6-144">Standard Edition, Enterprise Edition, or Datacenter Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="617b6-145">SP1 oder SP2</span><span class="sxs-lookup"><span data-stu-id="617b6-145">SP1 or SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="617b6-146">x86</span><span class="sxs-lookup"><span data-stu-id="617b6-146">x86</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="617b6-147">Windows Server2003 R2</span><span class="sxs-lookup"><span data-stu-id="617b6-147">Windows Server2003 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="617b6-148">Standard Edition, Enterprise Edition oder Datacenter Edition</span><span class="sxs-lookup"><span data-stu-id="617b6-148">Standard Edition, Enterprise Edition, or Datacenter Edition</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="617b6-149">x86</span><span class="sxs-lookup"><span data-stu-id="617b6-149">x86</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="617b6-150">Windows Server2008</span><span class="sxs-lookup"><span data-stu-id="617b6-150">Windows Server2008</span></span></p></td>
<td align="left"><p><span data-ttu-id="617b6-151">Standard, Enterprise oder Datacenter</span><span class="sxs-lookup"><span data-stu-id="617b6-151">Standard, Enterprise, or Datacenter</span></span></p></td>
<td align="left"><p><span data-ttu-id="617b6-152">SP1 oder SP2</span><span class="sxs-lookup"><span data-stu-id="617b6-152">SP1 or SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="617b6-153">x86</span><span class="sxs-lookup"><span data-stu-id="617b6-153">x86</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="617b6-154">**Hinweis**  Application Virtualization (App-V) 4,6 für Remote Desktop Dienste unterstützt 32-Bit-und 64-Bit-Versionen dieser Betriebssysteme.</span><span class="sxs-lookup"><span data-stu-id="617b6-154">**Note** Application Virtualization (App-V) 4.6 for Remote Desktop Services supports 32-bit and 64-bit versions of these operating systems.</span></span>

 

## <span data-ttu-id="617b6-155">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="617b6-155">Related topics</span></span>


[<span data-ttu-id="617b6-156">Application Virtualization Sequencer – Übersicht</span><span class="sxs-lookup"><span data-stu-id="617b6-156">Application Virtualization Sequencer Overview</span></span>](application-virtualization-sequencer-overview.md)

 

 





