---
title: Von DaRT 8.0 unterstützte Konfigurationen
description: Von DaRT 8.0 unterstützte Konfigurationen
author: dansimp
ms.assetid: 95d68e5c-d202-4f4a-adef-d2098328172e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 02c891555992652bf2a9b2b674ab8377536ef9d6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810249"
---
# <span data-ttu-id="453f0-103">Von DaRT 8.0 unterstützte Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="453f0-103">DaRT 8.0 Supported Configurations</span></span>


<span data-ttu-id="453f0-104">In diesem Thema werden die Voraussetzungen für Software und unterstützte Konfigurationen angegeben, die erforderlich sind, um Microsoft Diagnostics and Recovery Toolset (Dart) 8,0 in Ihrer Umgebung zu installieren und auszuführen.</span><span class="sxs-lookup"><span data-stu-id="453f0-104">This topic specifies the prerequisite software and supported configurations requirements that are necessary to install and run Microsoft Diagnostics and Recovery Toolset (DaRT) 8.0 in your environment.</span></span> <span data-ttu-id="453f0-105">Die Betriebssystemanforderungen und die Systemanforderungen, die für die Ausführung von Dart 8,0 erforderlich sind, werden angegeben.</span><span class="sxs-lookup"><span data-stu-id="453f0-105">Both the operating system requirements and the system requirements that are required to run DaRT 8.0 are specified.</span></span> <span data-ttu-id="453f0-106">Informationen zu den Voraussetzungen, die Sie beim Erstellen des DART-Wiederherstellungs Bilds beachten müssen, finden Sie unter [Planen der Erstellung des Dart 8,0-Wiederherstellungs Bilds](planning-to-create-the-dart-80-recovery-image-dart-8.md).</span><span class="sxs-lookup"><span data-stu-id="453f0-106">For information about prerequisites that you need to consider to create the DaRT recovery image, see [Planning to Create the DaRT 8.0 Recovery Image](planning-to-create-the-dart-80-recovery-image-dart-8.md).</span></span>

<span data-ttu-id="453f0-107">Informationen zu unterstützten Konfigurationen, die für spätere Versionen gelten, finden Sie in der Dokumentation zur jeweiligen Version.</span><span class="sxs-lookup"><span data-stu-id="453f0-107">For supported configurations that apply to later releases, see the documentation for the applicable release.</span></span>

<span data-ttu-id="453f0-108">Sie können Dart auf eine von zwei Arten installieren.</span><span class="sxs-lookup"><span data-stu-id="453f0-108">You can install DaRT in one of two ways.</span></span> <span data-ttu-id="453f0-109">Sie können alle Funktionen auf einem IT-Administratorcomputer installieren, in dem Sie alle Aufgaben ausführen, die mit der Ausführung von DART verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="453f0-109">You can install all functionality on an IT administrator computer, where you will perform all the tasks associated with running DaRT.</span></span> <span data-ttu-id="453f0-110">Alternativ können Sie auf dem Administratorcomputer nur die Dart-Funktionalität installieren, die das Wiederherstellungsabbild erstellt, und dann die Funktionalität installieren, die zum Ausführen von DART (also der Dart-Remote Verbindungsanzeige) auf einem Helpdesk-Computer verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="453f0-110">Alternatively, you can install, on the administrator computer, only the DaRT functionality that creates the recovery image, and then install the functionality used to run DaRT (that is, the DaRT Remote Connection Viewer) on a help desk computer.</span></span>

## <a href="" id="---------dart-8-0-prerequisite-software"></a> <span data-ttu-id="453f0-111">Dart 8,0-Voraussetzungs Software</span><span class="sxs-lookup"><span data-stu-id="453f0-111">DaRT 8.0 prerequisite software</span></span>


<span data-ttu-id="453f0-112">Stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind, bevor Sie Dart installieren.</span><span class="sxs-lookup"><span data-stu-id="453f0-112">Make sure that the following prerequisites are met before you install DaRT.</span></span>

### <span data-ttu-id="453f0-113">Voraussetzungen für Administrator Computer</span><span class="sxs-lookup"><span data-stu-id="453f0-113">Administrator computer prerequisites</span></span>

<span data-ttu-id="453f0-114">In der folgenden Tabelle sind die Installationsvoraussetzungen für den Administratorcomputer aufgeführt, wenn Sie Dart 8,0 und alle Dart-Tools installieren.</span><span class="sxs-lookup"><span data-stu-id="453f0-114">The following table lists the installation prerequisites for the administrator computer when you are installing DaRT 8.0 and all of the DaRT tools.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="453f0-115">Voraussetzung</span><span class="sxs-lookup"><span data-stu-id="453f0-115">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="453f0-116">Details</span><span class="sxs-lookup"><span data-stu-id="453f0-116">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="453f0-117">Windows Assessment and Development Kit (ADK)</span><span class="sxs-lookup"><span data-stu-id="453f0-117">Windows Assessment and Development Kit (ADK)</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="453f0-118">Erforderlich für den Dart-Wiederherstellungsbild-Assistenten.</span><span class="sxs-lookup"><span data-stu-id="453f0-118">Required for the DaRT Recovery Image wizard.</span></span> <span data-ttu-id="453f0-119">Enthält die Bereitstellungs Tools, die verwendet werden, um Windows-Abbilder anzupassen, bereitzustellen und zu verwenden, und enthält die Windows-Vorinstallationsumgebung (Windows PE).</span><span class="sxs-lookup"><span data-stu-id="453f0-119">Contains the Deployment Tools, which are used to customize, deploy, and service Windows images, and contains the Windows Preinstallation Environment (Windows PE).</span></span> <span data-ttu-id="453f0-120">Das ADK ist nicht erforderlich, wenn Sie nur den Remote Connection Viewer und/oder Crash Analyzer installieren.</span><span class="sxs-lookup"><span data-stu-id="453f0-120">The ADK is not required if you are installing only the Remote Connection Viewer and/or Crash Analyzer.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="453f0-121">.NET Framework 4,5</span><span class="sxs-lookup"><span data-stu-id="453f0-121">.NET Framework 4.5</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="453f0-122">Erforderlich für den Dart-Wiederherstellungsbild-Assistenten.</span><span class="sxs-lookup"><span data-stu-id="453f0-122">Required by the DaRT Recovery Image wizard.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="453f0-123">Windows Development Kit oder Software Development Kit (optional)</span><span class="sxs-lookup"><span data-stu-id="453f0-123">Windows Development Kit OR Software Development Kit (optional)</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="453f0-124">Für Crash Analyzer sind die Windows 8-Debugging-Tools aus dem Windows Driver Kit zum Analysieren von Speicherabbilddateien erforderlich.</span><span class="sxs-lookup"><span data-stu-id="453f0-124">Crash Analyzer requires the Windows 8 Debugging Tools from the Windows Driver Kit to analyze memory dump files.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="453f0-125">Windows 8 64-Bit ISO-Abbild</span><span class="sxs-lookup"><span data-stu-id="453f0-125">Windows 8 64-bit ISO image</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="453f0-126">Für Dart ist die Windows-Wiederherstellungsumgebung (Windows RE)-Abbild von Windows 8 Media erforderlich.</span><span class="sxs-lookup"><span data-stu-id="453f0-126">DaRT requires the Windows Recovery Environment (Windows RE) image from the Windows 8 media.</span></span> <span data-ttu-id="453f0-127">Laden Sie die 32-Bit-oder 64-Bit-Version von Windows 8 herunter, je nach dem Typ des DART-Wiederherstellungs Bilds, das Sie erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="453f0-127">Download the 32-bit or 64-bit version of Windows 8, depending on the type of DaRT recovery image you want to create.</span></span> <span data-ttu-id="453f0-128">Wenn Sie beide Systemtypen in Ihrer Umgebung unterstützen, laden Sie beide Versionen von Windows 8 herunter.</span><span class="sxs-lookup"><span data-stu-id="453f0-128">If you support both system types in your environment, download both versions of Windows 8.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="453f0-129">Voraussetzungen für Helpdesk-Computer</span><span class="sxs-lookup"><span data-stu-id="453f0-129">Help desk computer prerequisites</span></span>

<span data-ttu-id="453f0-130">In der folgenden Tabelle sind die Installationsvoraussetzungen für den Helpdesk-Computer aufgeführt, wenn Sie die Dart 8,0-Remote Verbindungsanzeige ausführen.</span><span class="sxs-lookup"><span data-stu-id="453f0-130">The following table lists the installation prerequisites for the help desk computer when you are running the DaRT 8.0 Remote Connection Viewer.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="453f0-131">Voraussetzung</span><span class="sxs-lookup"><span data-stu-id="453f0-131">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="453f0-132">Details</span><span class="sxs-lookup"><span data-stu-id="453f0-132">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="453f0-133">Dart 8,0-Remote Verbindungsanzeige</span><span class="sxs-lookup"><span data-stu-id="453f0-133">DaRT 8.0 Remote Connection Viewer</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="453f0-134">Muss unter einem Windows 8-Betriebssystem installiert sein.</span><span class="sxs-lookup"><span data-stu-id="453f0-134">Must be installed on a Windows 8 operating system.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="453f0-135">NET Framework 4,5</span><span class="sxs-lookup"><span data-stu-id="453f0-135">NET Framework 4.5</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="453f0-136">Erforderlich für den Dart-Wiederherstellungsbild-Assistenten</span><span class="sxs-lookup"><span data-stu-id="453f0-136">Required by the DaRT Recovery Image wizard</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="453f0-137">Debugging-Tools für Windows</span><span class="sxs-lookup"><span data-stu-id="453f0-137">Debugging Tools for Windows</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="453f0-138">Nur erforderlich, wenn Sie das Crash Analyzer-Tool installieren</span><span class="sxs-lookup"><span data-stu-id="453f0-138">Required only if you are installing the Crash Analyzer tool</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="453f0-139">Voraussetzungen für Endbenutzercomputer</span><span class="sxs-lookup"><span data-stu-id="453f0-139">End-user computer prerequisites</span></span>

<span data-ttu-id="453f0-140">Es gibt keine erforderliche Software, die auf Endbenutzercomputern installiert werden muss, mit Ausnahme des Betriebssystems Windows 8.</span><span class="sxs-lookup"><span data-stu-id="453f0-140">There is no prerequisite software that must be installed on end-user computers, other than the Windows 8 operating system.</span></span>

## <a href="" id="---------dart-operating-system-requirements"></a> <span data-ttu-id="453f0-141">Dart-Betriebssystemanforderungen</span><span class="sxs-lookup"><span data-stu-id="453f0-141">DaRT operating system requirements</span></span>


### <span data-ttu-id="453f0-142">Systemanforderungen für Administrator Computer</span><span class="sxs-lookup"><span data-stu-id="453f0-142">Administrator computer system requirements</span></span>

<span data-ttu-id="453f0-143">In der folgenden Tabelle sind die Betriebssysteme aufgeführt, die für die Installation des DART-Administratorcomputers unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="453f0-143">The following table lists the operating systems that are supported for the DaRT administrator computer installation.</span></span>

<span data-ttu-id="453f0-144">**Hinweis**  Stellen Sie sicher, dass Sie genügend Speicherplatz für alle zusätzlichen Tools zuweisen, die Sie auf dem Administratorcomputer installieren möchten.</span><span class="sxs-lookup"><span data-stu-id="453f0-144">**Note** Make sure that you allocate enough space for any additional tools that you want to install on the administrator computer.</span></span>

 

<span data-ttu-id="453f0-145">**Hinweis**  Microsoft bietet Unterstützung für das aktuelle Service Pack und in einigen Fällen das unmittelbar vorhergehende Service Pack.</span><span class="sxs-lookup"><span data-stu-id="453f0-145">**Note** Microsoft provides support for the current service pack and, in some cases, the immediately preceding service pack.</span></span> <span data-ttu-id="453f0-146">Informationen zu den Support Zeitachsen für Ihr Produkt finden Sie unter [unterstützte Service Packs für Lebenszyklen](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span><span class="sxs-lookup"><span data-stu-id="453f0-146">To find the support timelines for your product, see the [Lifecycle Supported Service Packs](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span></span> <span data-ttu-id="453f0-147">Weitere Informationen zur Microsoft Support Lifecycle-Richtlinie finden Sie in den [FAQ zu Microsoft Support Lifecycle Support Policy](https://go.microsoft.com/fwlink/p/?LinkId=31976).</span><span class="sxs-lookup"><span data-stu-id="453f0-147">For additional information about Microsoft Support Lifecycle Policy, see [Microsoft Support Lifecycle Support Policy FAQ](https://go.microsoft.com/fwlink/p/?LinkId=31976).</span></span>

 

<table style="width:100%;">
<colgroup>
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="453f0-148">Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="453f0-148">Operating System</span></span></th>
<th align="left"><span data-ttu-id="453f0-149">Edition</span><span class="sxs-lookup"><span data-stu-id="453f0-149">Edition</span></span></th>
<th align="left"><span data-ttu-id="453f0-150">Service Pack</span><span class="sxs-lookup"><span data-stu-id="453f0-150">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="453f0-151">System Architektur</span><span class="sxs-lookup"><span data-stu-id="453f0-151">System Architecture</span></span></th>
<th align="left"><span data-ttu-id="453f0-152">Betriebssystemanforderungen</span><span class="sxs-lookup"><span data-stu-id="453f0-152">Operating System Requirements</span></span></th>
<th align="left"><span data-ttu-id="453f0-153">RAM-Anforderung für die Ausführung von Dart</span><span class="sxs-lookup"><span data-stu-id="453f0-153">RAM Requirement for Running DaRT</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="453f0-154">Windows8</span><span class="sxs-lookup"><span data-stu-id="453f0-154">Windows8</span></span></p></td>
<td align="left"><p><span data-ttu-id="453f0-155">Alle Editionen</span><span class="sxs-lookup"><span data-stu-id="453f0-155">All editions</span></span></p></td>
<td align="left"><p><span data-ttu-id="453f0-156">n.v.</span><span class="sxs-lookup"><span data-stu-id="453f0-156">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="453f0-157">64Bit</span><span class="sxs-lookup"><span data-stu-id="453f0-157">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="453f0-158">2 GB</span><span class="sxs-lookup"><span data-stu-id="453f0-158">2 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="453f0-159">2,5 GB</span><span class="sxs-lookup"><span data-stu-id="453f0-159">2.5 GB</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="453f0-160">Windows8</span><span class="sxs-lookup"><span data-stu-id="453f0-160">Windows8</span></span></p></td>
<td align="left"><p><span data-ttu-id="453f0-161">Alle Editionen</span><span class="sxs-lookup"><span data-stu-id="453f0-161">All editions</span></span></p></td>
<td align="left"><p><span data-ttu-id="453f0-162">n.v.</span><span class="sxs-lookup"><span data-stu-id="453f0-162">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="453f0-163">32 Bit</span><span class="sxs-lookup"><span data-stu-id="453f0-163">32-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="453f0-164">1 GB</span><span class="sxs-lookup"><span data-stu-id="453f0-164">1 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="453f0-165">1,5 GB</span><span class="sxs-lookup"><span data-stu-id="453f0-165">1.5 GB</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="453f0-166">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="453f0-166">Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="453f0-167">Standard, Enterprise, Rechenzentrum</span><span class="sxs-lookup"><span data-stu-id="453f0-167">Standard, Enterprise, Data Center</span></span></p></td>
<td align="left"><p><span data-ttu-id="453f0-168">n.v.</span><span class="sxs-lookup"><span data-stu-id="453f0-168">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="453f0-169">64Bit</span><span class="sxs-lookup"><span data-stu-id="453f0-169">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="453f0-170">512MB</span><span class="sxs-lookup"><span data-stu-id="453f0-170">512 MB</span></span></p></td>
<td align="left"><p><span data-ttu-id="453f0-171">1.0 GB</span><span class="sxs-lookup"><span data-stu-id="453f0-171">1 .0 GB</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="-------------dart-help-desk-computer-system-requirements"></a> <span data-ttu-id="453f0-172">Systemanforderungen für Dart-Helpdesk-Computer</span><span class="sxs-lookup"><span data-stu-id="453f0-172">DaRT help desk computer system requirements</span></span>

<span data-ttu-id="453f0-173">Wenn Sie einem Helpdesk die Remote Behandlung von Computern gestatten, muss die Remote Verbindungsanzeige auf dem Helpdesk-Computer installiert sein.</span><span class="sxs-lookup"><span data-stu-id="453f0-173">If you allow a help desk to remotely troubleshoot computers, you must have the Remote Connection Viewer installed on the help desk computer.</span></span> <span data-ttu-id="453f0-174">Sie können das Crash Analyzer-Tool optional auf dem Helpdesk-Computer installieren.</span><span class="sxs-lookup"><span data-stu-id="453f0-174">You can optionally install the Crash Analyzer tool on the help desk computer.</span></span>

<span data-ttu-id="453f0-175">Dart 8,0 ermöglicht einem Helpdesk-Mitarbeiter, mithilfe des DART 7,0-oder Dart 8,0-Remote Verbindungs-Viewers eine Verbindung mit einem Dart 8,0-Computer herzustellen.</span><span class="sxs-lookup"><span data-stu-id="453f0-175">DaRT 8.0 enables a help desk worker to connect to a DaRT 8.0 computer by using either the DaRT 7.0 or DaRT 8.0 Remote Connection Viewer.</span></span> <span data-ttu-id="453f0-176">Die Dart 7,0-Remote Verbindungsanzeige erfordert ein Windows 7-Betriebssystem, während die Dart 8,0-Remote Verbindungsanzeige Windows 8 erfordert.</span><span class="sxs-lookup"><span data-stu-id="453f0-176">The DaRT 7.0 Remote Connection Viewer requires a Windows 7 operating system, while the DaRT 8.0 Remote Connection Viewer requires Windows 8.</span></span> <span data-ttu-id="453f0-177">Die Dart 8,0-Remote Verbindungsanzeige und alle anderen Dart 8,0-Tools können nur auf einem Computer mit Windows 8 installiert werden.</span><span class="sxs-lookup"><span data-stu-id="453f0-177">The DaRT 8.0 Remote Connection Viewer and all other DaRT 8.0 tools can be installed only on a computer running Windows 8.</span></span>

<span data-ttu-id="453f0-178">In der folgenden Tabelle sind die Betriebssysteme aufgeführt, die für die Installation des DART-Helpdesk-Computers unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="453f0-178">The following table lists the operating systems that are supported for the DaRT help desk computer installation.</span></span>

<table style="width:100%;">
<colgroup>
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="453f0-179">Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="453f0-179">Operating System</span></span></th>
<th align="left"><span data-ttu-id="453f0-180">Edition</span><span class="sxs-lookup"><span data-stu-id="453f0-180">Edition</span></span></th>
<th align="left"><span data-ttu-id="453f0-181">Service Pack</span><span class="sxs-lookup"><span data-stu-id="453f0-181">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="453f0-182">System Architektur</span><span class="sxs-lookup"><span data-stu-id="453f0-182">System Architecture</span></span></th>
<th align="left"><span data-ttu-id="453f0-183">Betriebssystemanforderungen</span><span class="sxs-lookup"><span data-stu-id="453f0-183">Operating System Requirements</span></span></th>
<th align="left"><span data-ttu-id="453f0-184">RAM-Anforderungen für die Ausführung von Dart</span><span class="sxs-lookup"><span data-stu-id="453f0-184">RAM Requirements for Running DaRT</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="453f0-185">Windows8</span><span class="sxs-lookup"><span data-stu-id="453f0-185">Windows8</span></span></p></td>
<td align="left"><p><span data-ttu-id="453f0-186">Alle Editionen</span><span class="sxs-lookup"><span data-stu-id="453f0-186">All editions</span></span></p></td>
<td align="left"><p><span data-ttu-id="453f0-187">n.v.</span><span class="sxs-lookup"><span data-stu-id="453f0-187">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="453f0-188">64Bit</span><span class="sxs-lookup"><span data-stu-id="453f0-188">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="453f0-189">2 GB</span><span class="sxs-lookup"><span data-stu-id="453f0-189">2 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="453f0-190">2,5 GB</span><span class="sxs-lookup"><span data-stu-id="453f0-190">2.5 GB</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="453f0-191">Windows8 (nur mit Remote Connection Viewer 8,0)</span><span class="sxs-lookup"><span data-stu-id="453f0-191">Windows8 (with Remote Connection Viewer 8.0 only)</span></span></p></td>
<td align="left"><p><span data-ttu-id="453f0-192">Alle Editionen</span><span class="sxs-lookup"><span data-stu-id="453f0-192">All editions</span></span></p></td>
<td align="left"><p><span data-ttu-id="453f0-193">n.v.</span><span class="sxs-lookup"><span data-stu-id="453f0-193">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="453f0-194">32 Bit</span><span class="sxs-lookup"><span data-stu-id="453f0-194">32-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="453f0-195">1 GB</span><span class="sxs-lookup"><span data-stu-id="453f0-195">1 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="453f0-196">1,5 GB</span><span class="sxs-lookup"><span data-stu-id="453f0-196">1.5 GB</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="453f0-197">Windows 7 (nur mit Remote Connection Viewer 7,0)</span><span class="sxs-lookup"><span data-stu-id="453f0-197">Windows 7 (with Remote Connection Viewer 7.0 only)</span></span></p></td>
<td align="left"><p><span data-ttu-id="453f0-198">Alle Editionen</span><span class="sxs-lookup"><span data-stu-id="453f0-198">All editions</span></span></p></td>
<td align="left"><p><span data-ttu-id="453f0-199">SP1, SP2</span><span class="sxs-lookup"><span data-stu-id="453f0-199">SP1, SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="453f0-200">64-Bit oder 32-Bit</span><span class="sxs-lookup"><span data-stu-id="453f0-200">64-bit or 32-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="453f0-201">1 GB</span><span class="sxs-lookup"><span data-stu-id="453f0-201">1 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="453f0-202">n.v.</span><span class="sxs-lookup"><span data-stu-id="453f0-202">N/A</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="453f0-203">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="453f0-203">Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="453f0-204">Standard, Enterprise, Rechenzentrum</span><span class="sxs-lookup"><span data-stu-id="453f0-204">Standard, Enterprise, Data Center</span></span></p></td>
<td align="left"><p><span data-ttu-id="453f0-205">n.v.</span><span class="sxs-lookup"><span data-stu-id="453f0-205">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="453f0-206">64Bit</span><span class="sxs-lookup"><span data-stu-id="453f0-206">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="453f0-207">51</span><span class="sxs-lookup"><span data-stu-id="453f0-207">51</span></span></p></td>
<td align="left"><p><span data-ttu-id="453f0-208">1,0 GB</span><span class="sxs-lookup"><span data-stu-id="453f0-208">1.0 GB</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="453f0-209">DART verfügt auch über die folgenden Mindestanforderungen an die Hardware für den Endbenutzercomputer:</span><span class="sxs-lookup"><span data-stu-id="453f0-209">DaRT also has the following minimum hardware requirements for the end-user computer:</span></span>

<span data-ttu-id="453f0-210">Ein CD-oder DVD-Laufwerk oder ein USB-Anschluss – nur erforderlich, wenn Sie Dart in Ihrem Unternehmen mit einer CD, DVD oder einem USB-Gerät bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="453f0-210">A CD or DVD drive or a USB port - required only if you are deploying DaRT in your enterprise by using a CD, DVD, or USB.</span></span>

<span data-ttu-id="453f0-211">BIOS-Unterstützung für das Starten des Computers von einer CD oder DVD, einem USB-Flashlaufwerk oder von einer Remote-oder Wiederherstellungspartition.</span><span class="sxs-lookup"><span data-stu-id="453f0-211">BIOS support for starting the computer from a CD or DVD, a USB flash drive, or from a remote or recovery partition.</span></span>

### <a href="" id="-------------dart-end-user-computer-system-requirements"></a> <span data-ttu-id="453f0-212">Systemanforderungen für Dart-Endbenutzercomputer</span><span class="sxs-lookup"><span data-stu-id="453f0-212">DaRT end-user computer system requirements</span></span>

<span data-ttu-id="453f0-213">Das Fenster Diagnose-und Wiederherstellungs-Toolset in DART setzt voraus, dass der Endbenutzercomputer eines der folgenden Betriebssysteme zusammen mit dem angegebenen verfügbaren Speicherplatz für Dart verwendet:</span><span class="sxs-lookup"><span data-stu-id="453f0-213">The Diagnostics and Recovery Toolset window in DaRT requires that the end-user computer use one of the following operating systems together with the specified amount of system memory available for DaRT:</span></span>

<table style="width:100%;">
<colgroup>
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="453f0-214">Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="453f0-214">Operating System</span></span></th>
<th align="left"><span data-ttu-id="453f0-215">Edition</span><span class="sxs-lookup"><span data-stu-id="453f0-215">Edition</span></span></th>
<th align="left"><span data-ttu-id="453f0-216">Service Pack</span><span class="sxs-lookup"><span data-stu-id="453f0-216">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="453f0-217">System Architektur</span><span class="sxs-lookup"><span data-stu-id="453f0-217">System Architecture</span></span></th>
<th align="left"><span data-ttu-id="453f0-218">Betriebssystemanforderungen</span><span class="sxs-lookup"><span data-stu-id="453f0-218">Operating System Requirements</span></span></th>
<th align="left"><span data-ttu-id="453f0-219">RAM-Anforderungen</span><span class="sxs-lookup"><span data-stu-id="453f0-219">RAM Requirements</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="453f0-220">Windows8</span><span class="sxs-lookup"><span data-stu-id="453f0-220">Windows8</span></span></p></td>
<td align="left"><p><span data-ttu-id="453f0-221">Alle Editionen</span><span class="sxs-lookup"><span data-stu-id="453f0-221">All editions</span></span></p></td>
<td align="left"><p><span data-ttu-id="453f0-222">n.v.</span><span class="sxs-lookup"><span data-stu-id="453f0-222">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="453f0-223">64Bit</span><span class="sxs-lookup"><span data-stu-id="453f0-223">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="453f0-224">2 GB</span><span class="sxs-lookup"><span data-stu-id="453f0-224">2 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="453f0-225">2,5 GB</span><span class="sxs-lookup"><span data-stu-id="453f0-225">2.5 GB</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="453f0-226">Windows8</span><span class="sxs-lookup"><span data-stu-id="453f0-226">Windows8</span></span></p></td>
<td align="left"><p><span data-ttu-id="453f0-227">Alle Editionen</span><span class="sxs-lookup"><span data-stu-id="453f0-227">All editions</span></span></p></td>
<td align="left"><p><span data-ttu-id="453f0-228">n.v.</span><span class="sxs-lookup"><span data-stu-id="453f0-228">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="453f0-229">32 Bit</span><span class="sxs-lookup"><span data-stu-id="453f0-229">32-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="453f0-230">1 GB</span><span class="sxs-lookup"><span data-stu-id="453f0-230">1 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="453f0-231">1,5 GB</span><span class="sxs-lookup"><span data-stu-id="453f0-231">1.5 GB</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="453f0-232">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="453f0-232">Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="453f0-233">Standard, Enterprise, Rechenzentrum</span><span class="sxs-lookup"><span data-stu-id="453f0-233">Standard, Enterprise, Data Center</span></span></p></td>
<td align="left"><p><span data-ttu-id="453f0-234">n.v.</span><span class="sxs-lookup"><span data-stu-id="453f0-234">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="453f0-235">64Bit</span><span class="sxs-lookup"><span data-stu-id="453f0-235">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="453f0-236">512MB</span><span class="sxs-lookup"><span data-stu-id="453f0-236">512 MB</span></span></p></td>
<td align="left"><p><span data-ttu-id="453f0-237">1,0 GB</span><span class="sxs-lookup"><span data-stu-id="453f0-237">1.0 GB</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="453f0-238">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="453f0-238">Related topics</span></span>


[<span data-ttu-id="453f0-239">Planen der Bereitstellung von DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="453f0-239">Planning to Deploy DaRT 8.0</span></span>](planning-to-deploy-dart-80-dart-8.md)

 

 





