---
title: Hardware- und Softwareanforderungen für Application Virtualization Sequencer
description: Hardware- und Softwareanforderungen für Application Virtualization Sequencer
author: dansimp
ms.assetid: c88a1b5b-23e1-4460-afa9-a5f37e32eb05
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d68afe4d4a3f6f301d38f2e86139d94319583467
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807980"
---
# <span data-ttu-id="6a6c2-103">Hardware- und Softwareanforderungen für Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="6a6c2-103">Application Virtualization Sequencer Hardware and Software Requirements</span></span>


<span data-ttu-id="6a6c2-104">In diesem Thema werden die Mindestanforderungen für Hardware und Software für den Computer beschrieben, auf dem der Microsoft Application Virtualization (App-V)-Sequenzer ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6a6c2-104">This topic describes the minimum recommended hardware and software requirements for the computer running the Microsoft Application Virtualization (App-V) Sequencer.</span></span>

<span data-ttu-id="6a6c2-105">**Wichtig**  Sie müssen den App-V-Sequencer (**SFTSequencer.exe**) mithilfe eines Kontos ausführen, das über Administratorberechtigungen verfügt, weil die Änderungen, die der Sequencer am lokalen System vornimmt, ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="6a6c2-105">**Important** You must run the App-V sequencer (**SFTSequencer.exe**) using an account that has administrator privileges because of the changes the sequencer makes to the local system.</span></span> <span data-ttu-id="6a6c2-106">Diese Änderungen können das Schreiben von Dateien in das **c:\\Programme-Datei** Verzeichnis, das vornehmen von Registrierungsänderungen, das Starten und Beenden von Diensten, das Aktualisieren von Sicherheitsbeschreibungen für Dateien und das Ändern von Berechtigungen umfassen.</span><span class="sxs-lookup"><span data-stu-id="6a6c2-106">These changes can include writing files to the **C:\\Program Files** directory, making registry changes, starting and stopping services, updating security descriptors for files, and changing permissions.</span></span>

 

<span data-ttu-id="6a6c2-107">Bevor Sie den Sequencer installieren und nachdem Sie die einzelnen Anwendungen sequenziert haben, müssen Sie ein sauberes Betriebssystemabbild auf dem Sequenzcomputer wiederherstellen.</span><span class="sxs-lookup"><span data-stu-id="6a6c2-107">Before you install the Sequencer and after you sequence each application, you must restore a clean operating system image to the sequencing computer.</span></span> <span data-ttu-id="6a6c2-108">Mit einer der folgenden Methoden können Sie den Computer wiederherstellen, auf dem der Sequencer ausgeführt wird:</span><span class="sxs-lookup"><span data-stu-id="6a6c2-108">You can use one of the following methods to restore the computer running the Sequencer:</span></span>

-   <span data-ttu-id="6a6c2-109">Formatieren Sie die Festplatte neu, und installieren Sie das Betriebssystem erneut.</span><span class="sxs-lookup"><span data-stu-id="6a6c2-109">Reformat the hard drive and reinstall the operating system.</span></span>

-   <span data-ttu-id="6a6c2-110">Wiederherstellen der Festplatte auf dem Computer, auf dem das Sequenzer-Image ausgeführt wird, mithilfe einer anderen Datenträger-Imaging-Software.</span><span class="sxs-lookup"><span data-stu-id="6a6c2-110">Restore the hard drive on the computer running the Sequencer image by using another disk-imaging software.</span></span>

-   <span data-ttu-id="6a6c2-111">Wiederherstellen eines virtuellen Betriebssystemabbilds wie einem Microsoft Virtual PC-Abbild</span><span class="sxs-lookup"><span data-stu-id="6a6c2-111">Revert a virtual operating system image such as a Microsoft Virtual PC image.</span></span> <span data-ttu-id="6a6c2-112">Durch die Verwendung eines virtuellen Computers können saubere Sequenz Umgebungen problemlos wieder verwendet werden, wenn die Verwaltung minimal ist.</span><span class="sxs-lookup"><span data-stu-id="6a6c2-112">Using a virtual machine allows for clean sequencing environments to be easily reused with minimal administration.</span></span>

<span data-ttu-id="6a6c2-113">In der folgenden Liste werden die empfohlenen Hardwareanforderungen für die Ausführung des App-V-Sequencers erläutert.</span><span class="sxs-lookup"><span data-stu-id="6a6c2-113">The following list outlines the recommended hardware requirements for running the App-V Sequencer.</span></span>

<span data-ttu-id="6a6c2-114">Die Anforderungen werden zunächst für Microsoft Application Virtualization (app-v) 4.6 SP2 aufgeführt, gefolgt von den Anforderungen für Versionen, die APP-v 4.6 SP2 vorangestellt sind.</span><span class="sxs-lookup"><span data-stu-id="6a6c2-114">The requirements are listed first for Microsoft Application Virtualization (App-V)4.6 SP2, followed by the requirements for versions that preceded App-V4.6SP2.</span></span>

### <a href="" id="hardware-requirements-"></a><span data-ttu-id="6a6c2-115">Hardwareanforderungen</span><span class="sxs-lookup"><span data-stu-id="6a6c2-115">Hardware Requirements</span></span>

-   <span data-ttu-id="6a6c2-116">Prozessor: Intel Pentium III, 1 GHz (32-Bit oder 64-Bit).</span><span class="sxs-lookup"><span data-stu-id="6a6c2-116">Processor—Intel Pentium III, 1 GHz (32-bit or 64-bit).</span></span> <span data-ttu-id="6a6c2-117">Der Sequenzierungsprozess ist ein Single-Thread-Prozess und nutzt keine dualen Prozessoren.</span><span class="sxs-lookup"><span data-stu-id="6a6c2-117">The sequencing process is a single-threaded process and does not take advantage of dual processors.</span></span>

-   <span data-ttu-id="6a6c2-118">Speicher – 1GB oder höher, 2GB empfohlen.</span><span class="sxs-lookup"><span data-stu-id="6a6c2-118">Memory—1GB or above, 2GB recommended.</span></span>

-   <span data-ttu-id="6a6c2-119">Festplatte – 40 Gigabyte (GB) Festplattenspeicher mit einem verfügbaren Festplattenspeicherplatz von 15 GB.</span><span class="sxs-lookup"><span data-stu-id="6a6c2-119">Hard disk—40 gigabyte (GB) hard disk space with a minimum of 15 GB available hard disk space.</span></span> <span data-ttu-id="6a6c2-120">Wir empfehlen, dass Sie mindestens dreimal so viel Festplattenspeicherplatz haben, wie es für die von Ihnen sequenzierte Anwendung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="6a6c2-120">We recommend that you have at least three times the hard disk space that the application you are sequencing requires.</span></span>

    <span data-ttu-id="6a6c2-121">**Hinweis**  Für die Sequenzierung ist eine starke Datenträgernutzung erforderlich.</span><span class="sxs-lookup"><span data-stu-id="6a6c2-121">**Note** Sequencing requires heavy disk usage.</span></span> <span data-ttu-id="6a6c2-122">Eine schnelle Festplattengeschwindigkeit kann die Sequenzierungs Zeit verkleinern.</span><span class="sxs-lookup"><span data-stu-id="6a6c2-122">A fast disk speed can decrease the sequencing time.</span></span>

     

### <span data-ttu-id="6a6c2-123">Software Anforderungen für App-V 4,6 SP2</span><span class="sxs-lookup"><span data-stu-id="6a6c2-123">Software Requirements for App-V 4.6 SP2</span></span>

<span data-ttu-id="6a6c2-124">In der folgenden Liste werden die unterstützten Betriebssysteme für die Ausführung des App-V 4,6 SP2-Sequenzers erläutert.</span><span class="sxs-lookup"><span data-stu-id="6a6c2-124">The following list outlines the supported operating systems for running the App-V 4.6 SP2 Sequencer.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="6a6c2-125">Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="6a6c2-125">Operating System</span></span></th>
<th align="left"><span data-ttu-id="6a6c2-126">Edition</span><span class="sxs-lookup"><span data-stu-id="6a6c2-126">Edition</span></span></th>
<th align="left"><span data-ttu-id="6a6c2-127">Service Pack</span><span class="sxs-lookup"><span data-stu-id="6a6c2-127">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="6a6c2-128">System Architektur</span><span class="sxs-lookup"><span data-stu-id="6a6c2-128">System Architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6a6c2-129">WindowsXP</span><span class="sxs-lookup"><span data-stu-id="6a6c2-129">WindowsXP</span></span></p></td>
<td align="left"><p><span data-ttu-id="6a6c2-130">Professional</span><span class="sxs-lookup"><span data-stu-id="6a6c2-130">Professional</span></span></p></td>
<td align="left"><p><span data-ttu-id="6a6c2-131">SP3</span><span class="sxs-lookup"><span data-stu-id="6a6c2-131">SP3</span></span></p></td>
<td align="left"><p><span data-ttu-id="6a6c2-132">x86</span><span class="sxs-lookup"><span data-stu-id="6a6c2-132">x86</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6a6c2-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6a6c2-133">Windows Vista</span></span></p></td>
<td align="left"><p><span data-ttu-id="6a6c2-134">Business, Enterprise oder Ultimate</span><span class="sxs-lookup"><span data-stu-id="6a6c2-134">Business, Enterprise, or Ultimate</span></span></p></td>
<td align="left"><p><span data-ttu-id="6a6c2-135">SP2</span><span class="sxs-lookup"><span data-stu-id="6a6c2-135">SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="6a6c2-136">x86</span><span class="sxs-lookup"><span data-stu-id="6a6c2-136">x86</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6a6c2-137">Windows7</span><span class="sxs-lookup"><span data-stu-id="6a6c2-137">Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="6a6c2-138">Professional, Enterprise oder Ultimate</span><span class="sxs-lookup"><span data-stu-id="6a6c2-138">Professional, Enterprise, or Ultimate</span></span></p></td>
<td align="left"><p><span data-ttu-id="6a6c2-139">Kein Service Pack oder SP1</span><span class="sxs-lookup"><span data-stu-id="6a6c2-139">No service pack or SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="6a6c2-140">x86 und x64</span><span class="sxs-lookup"><span data-stu-id="6a6c2-140">x86 and x64</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6a6c2-141">Windows 8</span><span class="sxs-lookup"><span data-stu-id="6a6c2-141">Windows 8</span></span></p></td>
<td align="left"><p><span data-ttu-id="6a6c2-142">Pro-oder Enterprise-Edition</span><span class="sxs-lookup"><span data-stu-id="6a6c2-142">Pro or Enterprise Edition</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="6a6c2-143">x86 und x64</span><span class="sxs-lookup"><span data-stu-id="6a6c2-143">x86 and x64</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="6a6c2-144">**Hinweis**  Der Application Virtualization (App-V) 4,6 SP2-Sequenzer unterstützt 32-Bit-und 64-Bit-Versionen dieser Betriebssysteme.</span><span class="sxs-lookup"><span data-stu-id="6a6c2-144">**Note** The Application Virtualization (App-V) 4.6 SP2 Sequencer supports 32-bit and 64-bit versions of these operating systems.</span></span>

 

<span data-ttu-id="6a6c2-145">Sie sollten Computer, auf denen der Sequencer ausgeführt wird, mit denselben Anwendungen konfigurieren, die auf Zielcomputern installiert sind.</span><span class="sxs-lookup"><span data-stu-id="6a6c2-145">You should configure computers running the Sequencer with the same applications that are installed on targeted computers.</span></span>

### <span data-ttu-id="6a6c2-146">Software Anforderungen für Versionen, die App-V 4,6 SP2 vorausgehen</span><span class="sxs-lookup"><span data-stu-id="6a6c2-146">Software Requirements for Versions that Precede App-V 4.6 SP2</span></span>

<span data-ttu-id="6a6c2-147">In der folgenden Liste werden die unterstützten Betriebssysteme für die Ausführung des Sequencers für Versionen beschrieben, die App-V 4,6 SP2 vorangestellt sind.</span><span class="sxs-lookup"><span data-stu-id="6a6c2-147">The following list outlines the supported operating systems for running the Sequencer for versions that precede App-V 4.6 SP2.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="6a6c2-148">Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="6a6c2-148">Operating System</span></span></th>
<th align="left"><span data-ttu-id="6a6c2-149">Edition</span><span class="sxs-lookup"><span data-stu-id="6a6c2-149">Edition</span></span></th>
<th align="left"><span data-ttu-id="6a6c2-150">Service Pack</span><span class="sxs-lookup"><span data-stu-id="6a6c2-150">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="6a6c2-151">System Architektur</span><span class="sxs-lookup"><span data-stu-id="6a6c2-151">System Architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6a6c2-152">WindowsXP</span><span class="sxs-lookup"><span data-stu-id="6a6c2-152">WindowsXP</span></span></p></td>
<td align="left"><p><span data-ttu-id="6a6c2-153">Professional</span><span class="sxs-lookup"><span data-stu-id="6a6c2-153">Professional</span></span></p></td>
<td align="left"><p><span data-ttu-id="6a6c2-154">SP2 oder SP3</span><span class="sxs-lookup"><span data-stu-id="6a6c2-154">SP2 or SP3</span></span></p></td>
<td align="left"><p><span data-ttu-id="6a6c2-155">x86</span><span class="sxs-lookup"><span data-stu-id="6a6c2-155">x86</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6a6c2-156">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6a6c2-156">Windows Vista</span></span></p></td>
<td align="left"><p><span data-ttu-id="6a6c2-157">Business, Enterprise oder Ultimate</span><span class="sxs-lookup"><span data-stu-id="6a6c2-157">Business, Enterprise, or Ultimate</span></span></p></td>
<td align="left"><p><span data-ttu-id="6a6c2-158">Kein Service Pack, SP1 oder SP2</span><span class="sxs-lookup"><span data-stu-id="6a6c2-158">No service pack, SP1, or SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="6a6c2-159">x86</span><span class="sxs-lookup"><span data-stu-id="6a6c2-159">x86</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6a6c2-160">Windows7 ¹</span><span class="sxs-lookup"><span data-stu-id="6a6c2-160">Windows7¹</span></span></p></td>
<td align="left"><p><span data-ttu-id="6a6c2-161">Professional, Enterprise oder Ultimate</span><span class="sxs-lookup"><span data-stu-id="6a6c2-161">Professional, Enterprise, or Ultimate</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="6a6c2-162">x86</span><span class="sxs-lookup"><span data-stu-id="6a6c2-162">x86</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="6a6c2-163">¹ unterstützt für App-v 4,5 mit SP1 oder SP2 und nur App-v 4,6</span><span class="sxs-lookup"><span data-stu-id="6a6c2-163">¹Supported for App-V 4.5 with SP1 or SP2, and App-V 4.6 only</span></span>

<span data-ttu-id="6a6c2-164">**Hinweis**  Der Application Virtualization (App-V) 4,6-Sequenzer unterstützt 32-Bit-und 64-Bit-Versionen dieser Betriebssysteme.</span><span class="sxs-lookup"><span data-stu-id="6a6c2-164">**Note** The Application Virtualization (App-V) 4.6 Sequencer supports 32-bit and 64-bit versions of these operating systems.</span></span>

 

<span data-ttu-id="6a6c2-165">Sie sollten Computer, auf denen der Sequencer ausgeführt wird, mit denselben Anwendungen konfigurieren, die auf Zielcomputern installiert sind.</span><span class="sxs-lookup"><span data-stu-id="6a6c2-165">You should configure computers running the Sequencer with the same applications that are installed on targeted computers.</span></span>

### <span data-ttu-id="6a6c2-166">Software Anforderungen für Remote Desktop Dienste für App-V 4,6 SP2</span><span class="sxs-lookup"><span data-stu-id="6a6c2-166">Software Requirements for Remote Desktop Services for App-V 4.6 SP2</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="6a6c2-167">Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="6a6c2-167">Operating System</span></span></th>
<th align="left"><span data-ttu-id="6a6c2-168">Edition</span><span class="sxs-lookup"><span data-stu-id="6a6c2-168">Edition</span></span></th>
<th align="left"><span data-ttu-id="6a6c2-169">Service Pack</span><span class="sxs-lookup"><span data-stu-id="6a6c2-169">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="6a6c2-170">System Architektur</span><span class="sxs-lookup"><span data-stu-id="6a6c2-170">System Architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6a6c2-171">Windows Server2003 R2</span><span class="sxs-lookup"><span data-stu-id="6a6c2-171">Windows Server2003 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="6a6c2-172">Standard Edition, Enterprise Edition oder Datacenter Edition</span><span class="sxs-lookup"><span data-stu-id="6a6c2-172">Standard Edition, Enterprise Edition, or Datacenter Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="6a6c2-173">SP2</span><span class="sxs-lookup"><span data-stu-id="6a6c2-173">SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="6a6c2-174">x86</span><span class="sxs-lookup"><span data-stu-id="6a6c2-174">x86</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6a6c2-175">Windows Server2008</span><span class="sxs-lookup"><span data-stu-id="6a6c2-175">Windows Server2008</span></span></p></td>
<td align="left"><p><span data-ttu-id="6a6c2-176">Standard-, Enterprise-oder Datacenter-Edition</span><span class="sxs-lookup"><span data-stu-id="6a6c2-176">Standard, Enterprise, or Datacenter Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="6a6c2-177">SP2</span><span class="sxs-lookup"><span data-stu-id="6a6c2-177">SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="6a6c2-178">x86</span><span class="sxs-lookup"><span data-stu-id="6a6c2-178">x86</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6a6c2-179">Windows Server2008 R2</span><span class="sxs-lookup"><span data-stu-id="6a6c2-179">Windows Server2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="6a6c2-180">Standard-, Enterprise-oder Datacenter-Edition</span><span class="sxs-lookup"><span data-stu-id="6a6c2-180">Standard, Enterprise, or Datacenter Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="6a6c2-181">Kein Service Pack oder SP1</span><span class="sxs-lookup"><span data-stu-id="6a6c2-181">No service pack or SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="6a6c2-182">x64</span><span class="sxs-lookup"><span data-stu-id="6a6c2-182">x64</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6a6c2-183">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6a6c2-183">Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="6a6c2-184">Standard-, Enterprise-oder Datacenter-Edition</span><span class="sxs-lookup"><span data-stu-id="6a6c2-184">Standard, Enterprise, or Datacenter Edition</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="6a6c2-185">x86 oder x64</span><span class="sxs-lookup"><span data-stu-id="6a6c2-185">x86 or x64</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="6a6c2-186">**Hinweis**  Application Virtualization (App-V) 4,6 SP2 für Remote Desktop Dienste unterstützt 32-Bit-und 64-Bit-Versionen dieser Betriebssysteme.</span><span class="sxs-lookup"><span data-stu-id="6a6c2-186">**Note** Application Virtualization (App-V) 4.6 SP2 for Remote Desktop Services supports 32-bit and 64-bit versions of these operating systems.</span></span>

 

### <span data-ttu-id="6a6c2-187">Software Anforderungen für Remote Desktop Dienste für Versionen, die App-V 4,6 SP2 vorausgehen</span><span class="sxs-lookup"><span data-stu-id="6a6c2-187">Software Requirements for Remote Desktop Services for Versions that Precede App-V 4.6 SP2</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="6a6c2-188">Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="6a6c2-188">Operating System</span></span></th>
<th align="left"><span data-ttu-id="6a6c2-189">Edition</span><span class="sxs-lookup"><span data-stu-id="6a6c2-189">Edition</span></span></th>
<th align="left"><span data-ttu-id="6a6c2-190">Service Pack</span><span class="sxs-lookup"><span data-stu-id="6a6c2-190">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="6a6c2-191">System Architektur</span><span class="sxs-lookup"><span data-stu-id="6a6c2-191">System Architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6a6c2-192">Windows Server2003</span><span class="sxs-lookup"><span data-stu-id="6a6c2-192">Windows Server2003</span></span></p></td>
<td align="left"><p><span data-ttu-id="6a6c2-193">Standard Edition, Enterprise Edition oder Datacenter Edition</span><span class="sxs-lookup"><span data-stu-id="6a6c2-193">Standard Edition, Enterprise Edition, or Datacenter Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="6a6c2-194">SP1 oder SP2</span><span class="sxs-lookup"><span data-stu-id="6a6c2-194">SP1 or SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="6a6c2-195">x86</span><span class="sxs-lookup"><span data-stu-id="6a6c2-195">x86</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6a6c2-196">Windows Server2003 R2</span><span class="sxs-lookup"><span data-stu-id="6a6c2-196">Windows Server2003 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="6a6c2-197">Standard Edition, Enterprise Edition oder Datacenter Edition</span><span class="sxs-lookup"><span data-stu-id="6a6c2-197">Standard Edition, Enterprise Edition, or Datacenter Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="6a6c2-198">Kein Service Pack oder SP2</span><span class="sxs-lookup"><span data-stu-id="6a6c2-198">No service pack or SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="6a6c2-199">x86</span><span class="sxs-lookup"><span data-stu-id="6a6c2-199">x86</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6a6c2-200">Windows Server2008</span><span class="sxs-lookup"><span data-stu-id="6a6c2-200">Windows Server2008</span></span></p></td>
<td align="left"><p><span data-ttu-id="6a6c2-201">Standard-, Enterprise-oder Datacenter-Edition</span><span class="sxs-lookup"><span data-stu-id="6a6c2-201">Standard, Enterprise, or Datacenter Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="6a6c2-202">SP1 oder SP2</span><span class="sxs-lookup"><span data-stu-id="6a6c2-202">SP1 or SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="6a6c2-203">x86</span><span class="sxs-lookup"><span data-stu-id="6a6c2-203">x86</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6a6c2-204">Windows Server2008 R2</span><span class="sxs-lookup"><span data-stu-id="6a6c2-204">Windows Server2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="6a6c2-205">Standard-, Enterprise-oder Datacenter-Edition</span><span class="sxs-lookup"><span data-stu-id="6a6c2-205">Standard, Enterprise, or Datacenter Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="6a6c2-206">Kein Service Pack oder SP1</span><span class="sxs-lookup"><span data-stu-id="6a6c2-206">No service pack or SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="6a6c2-207">x64</span><span class="sxs-lookup"><span data-stu-id="6a6c2-207">x64</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="6a6c2-208">**Hinweis**  Application Virtualization (App-V) 4,6 SP2 für Remote Desktop Dienste unterstützt 32-Bit-und 64-Bit-Versionen dieser Betriebssysteme.</span><span class="sxs-lookup"><span data-stu-id="6a6c2-208">**Note** Application Virtualization (App-V) 4.6 SP2 for Remote Desktop Services supports 32-bit and 64-bit versions of these operating systems.</span></span>

 

## <span data-ttu-id="6a6c2-209">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="6a6c2-209">Related topics</span></span>


[<span data-ttu-id="6a6c2-210">Hardware- und Softwareanforderungen für Application Virtualization Client</span><span class="sxs-lookup"><span data-stu-id="6a6c2-210">Application Virtualization Client Hardware and Software Requirements</span></span>](application-virtualization-client-hardware-and-software-requirements.md)

[<span data-ttu-id="6a6c2-211">Systemanforderungen für Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="6a6c2-211">Application Virtualization System Requirements</span></span>](application-virtualization-system-requirements.md)

[<span data-ttu-id="6a6c2-212">So installieren Sie Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="6a6c2-212">How to Install the Application Virtualization Sequencer</span></span>](how-to-install-the-application-virtualization-sequencer.md)

[<span data-ttu-id="6a6c2-213">So aktualisieren Sie Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="6a6c2-213">How to Upgrade the Application Virtualization Sequencer</span></span>](how-to-upgrade-the-application-virtualization-sequencer.md)

 

 





