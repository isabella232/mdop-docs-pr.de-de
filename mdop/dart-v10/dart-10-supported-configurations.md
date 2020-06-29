---
title: Von DaRT 10 unterstützte Konfigurationen
description: Von DaRT 10 unterstützte Konfigurationen
author: dansimp
ms.assetid: a07d6562-1fa9-499f-829c-9cc487ede0b7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 414b9d5cb7bf78dcfeda3fafc1c476e367709446
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804751"
---
# <span data-ttu-id="a84be-103">Von DaRT 10 unterstützte Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="a84be-103">DaRT 10 Supported Configurations</span></span>


<span data-ttu-id="a84be-104">In diesem Thema werden die Voraussetzungen für Software und unterstützte Konfigurationen angegeben, die zum Installieren und Ausführen von Microsoft Diagnostics and Recovery Toolset (Dart) 10 in Ihrer Umgebung erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="a84be-104">This topic specifies the prerequisite software and supported configurations requirements that are necessary to install and run Microsoft Diagnostics and Recovery Toolset (DaRT) 10 in your environment.</span></span> <span data-ttu-id="a84be-105">Die Betriebssystemanforderungen und die Systemanforderungen, die für die Ausführung von DART 10 erforderlich sind, werden angegeben.</span><span class="sxs-lookup"><span data-stu-id="a84be-105">Both the operating system requirements and the system requirements that are required to run DaRT 10 are specified.</span></span> <span data-ttu-id="a84be-106">Informationen zu den Voraussetzungen, die Sie beim Erstellen des DART-Wiederherstellungs Bilds beachten müssen, finden Sie unter [Planen der Erstellung des DART 10-Wiederherstellungs Bilds](planning-to-create-the-dart-10-recovery-image.md).</span><span class="sxs-lookup"><span data-stu-id="a84be-106">For information about prerequisites that you need to consider to create the DaRT recovery image, see [Planning to Create the DaRT 10 Recovery Image](planning-to-create-the-dart-10-recovery-image.md).</span></span>

<span data-ttu-id="a84be-107">Informationen zu unterstützten Konfigurationen, die für spätere Versionen gelten, finden Sie in der Dokumentation zur jeweiligen Version.</span><span class="sxs-lookup"><span data-stu-id="a84be-107">For supported configurations that apply to later releases, see the documentation for the applicable release.</span></span>

<span data-ttu-id="a84be-108">Sie können Dart auf eine von zwei Arten installieren.</span><span class="sxs-lookup"><span data-stu-id="a84be-108">You can install DaRT in one of two ways.</span></span> <span data-ttu-id="a84be-109">Sie können alle Funktionen auf einem IT-Administratorcomputer installieren, in dem Sie alle Aufgaben ausführen, die mit der Ausführung von DART verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="a84be-109">You can install all functionality on an IT administrator computer, where you will perform all the tasks associated with running DaRT.</span></span> <span data-ttu-id="a84be-110">Alternativ können Sie auf dem Administratorcomputer nur die Dart-Funktionalität installieren, die das Wiederherstellungsabbild erstellt, und dann die Funktionalität installieren, die zum Ausführen von DART (also der Dart-Remote Verbindungsanzeige) auf einem Helpdesk-Computer verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a84be-110">Alternatively, you can install, on the administrator computer, only the DaRT functionality that creates the recovery image, and then install the functionality used to run DaRT (that is, the DaRT Remote Connection Viewer) on a help desk computer.</span></span>

## <span data-ttu-id="a84be-111">Dart 10-Voraussetzungs Software</span><span class="sxs-lookup"><span data-stu-id="a84be-111">DaRT 10 prerequisite software</span></span>


<span data-ttu-id="a84be-112">Stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind, bevor Sie Dart installieren.</span><span class="sxs-lookup"><span data-stu-id="a84be-112">Make sure that the following prerequisites are met before you install DaRT.</span></span>

### <span data-ttu-id="a84be-113">Voraussetzungen für Administrator Computer</span><span class="sxs-lookup"><span data-stu-id="a84be-113">Administrator computer prerequisites</span></span>

<span data-ttu-id="a84be-114">In der folgenden Tabelle sind die Installationsvoraussetzungen für den Administratorcomputer aufgeführt, wenn Sie Dart 10 und alle Dart-Tools installieren.</span><span class="sxs-lookup"><span data-stu-id="a84be-114">The following table lists the installation prerequisites for the administrator computer when you are installing DaRT 10 and all of the DaRT tools.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="a84be-115">Voraussetzung</span><span class="sxs-lookup"><span data-stu-id="a84be-115">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="a84be-116">Details</span><span class="sxs-lookup"><span data-stu-id="a84be-116">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="a84be-117">Windows Assessment and Development Kit (ADK)</span><span class="sxs-lookup"><span data-stu-id="a84be-117">Windows Assessment and Development Kit (ADK)</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="a84be-118">Erforderlich für den Dart-Wiederherstellungsbild-Assistenten.</span><span class="sxs-lookup"><span data-stu-id="a84be-118">Required for the DaRT Recovery Image wizard.</span></span> <span data-ttu-id="a84be-119">Enthält die Bereitstellungs Tools, die verwendet werden, um Windows-Abbilder anzupassen, bereitzustellen und zu verwenden, und enthält die Windows-Vorinstallationsumgebung (Windows PE).</span><span class="sxs-lookup"><span data-stu-id="a84be-119">Contains the Deployment Tools, which are used to customize, deploy, and service Windows images, and contains the Windows Preinstallation Environment (Windows PE).</span></span> <span data-ttu-id="a84be-120">Das ADK ist nicht erforderlich, wenn Sie nur den Remote Connection Viewer und/oder Crash Analyzer installieren.</span><span class="sxs-lookup"><span data-stu-id="a84be-120">The ADK is not required if you are installing only the Remote Connection Viewer and/or Crash Analyzer.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="a84be-121">Windows Development Kit oder Software Development Kit (optional)</span><span class="sxs-lookup"><span data-stu-id="a84be-121">Windows Development Kit OR Software Development Kit (optional)</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="a84be-122">Für Crash Analyzer sind die Windows 10-Debugging-Tools aus dem Windows Driver Kit zum Analysieren von Speicherabbilddateien erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a84be-122">Crash Analyzer requires the Windows 10 Debugging Tools from the Windows Driver Kit to analyze memory dump files.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="a84be-123">Windows 10 64-Bit-oder 32-Bit-ISO-Abbild</span><span class="sxs-lookup"><span data-stu-id="a84be-123">Windows 10 64-bit or 32-bit ISO image</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="a84be-124">Für Dart ist die Windows-Wiederherstellungsumgebung (Windows RE)-Abbild von Windows 10 Media erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a84be-124">DaRT requires the Windows Recovery Environment (Windows RE) image from the Windows 10 media.</span></span> <span data-ttu-id="a84be-125">Laden Sie die 32-Bit-oder 64-Bit-Version von Windows 10 herunter, je nach dem Typ des DART-Wiederherstellungs Bilds, das Sie erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="a84be-125">Download the 32-bit or 64-bit version of Windows 10, depending on the type of DaRT recovery image you want to create.</span></span> <span data-ttu-id="a84be-126">Wenn Sie beide Systemtypen in Ihrer Umgebung unterstützen, laden Sie beide Versionen von Windows 10 herunter.</span><span class="sxs-lookup"><span data-stu-id="a84be-126">If you support both system types in your environment, download both versions of Windows 10.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="a84be-127">Voraussetzungen für Helpdesk-Computer</span><span class="sxs-lookup"><span data-stu-id="a84be-127">Help desk computer prerequisites</span></span>

<span data-ttu-id="a84be-128">In der folgenden Tabelle sind die Voraussetzungen für die Installation des Helpdesk-Computers aufgeführt, wenn Sie den Dart 10 Remote Connection Viewer ausführen.</span><span class="sxs-lookup"><span data-stu-id="a84be-128">The following table lists the installation prerequisites for the help desk computer when you are running the DaRT 10 Remote Connection Viewer.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="a84be-129">Voraussetzung</span><span class="sxs-lookup"><span data-stu-id="a84be-129">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="a84be-130">Details</span><span class="sxs-lookup"><span data-stu-id="a84be-130">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="a84be-131">Dart 10-Remote Verbindungsanzeige</span><span class="sxs-lookup"><span data-stu-id="a84be-131">DaRT 10 Remote Connection Viewer</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="a84be-132">Muss unter einem Windows 10-Betriebssystem installiert sein.</span><span class="sxs-lookup"><span data-stu-id="a84be-132">Must be installed on a Windows 10 operating system.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="a84be-133">Debugging-Tools für Windows</span><span class="sxs-lookup"><span data-stu-id="a84be-133">Debugging Tools for Windows</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="a84be-134">Nur erforderlich, wenn Sie das Crash Analyzer-Tool installieren</span><span class="sxs-lookup"><span data-stu-id="a84be-134">Required only if you are installing the Crash Analyzer tool</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="a84be-135">Voraussetzungen für Endbenutzercomputer</span><span class="sxs-lookup"><span data-stu-id="a84be-135">End-user computer prerequisites</span></span>

<span data-ttu-id="a84be-136">Es gibt keine erforderliche Software, die auf Endbenutzercomputern installiert werden muss, außer dem Betriebssystem Windows 10.</span><span class="sxs-lookup"><span data-stu-id="a84be-136">There is no prerequisite software that must be installed on end-user computers, other than the Windows 10 operating system.</span></span>

## <a href="" id="---------dart-10-operating-system-requirements"></a> <span data-ttu-id="a84be-137">Dart 10-Betriebssystemanforderungen</span><span class="sxs-lookup"><span data-stu-id="a84be-137">DaRT 10 operating system requirements</span></span>


### <span data-ttu-id="a84be-138">Systemanforderungen für Administrator Computer</span><span class="sxs-lookup"><span data-stu-id="a84be-138">Administrator computer system requirements</span></span>

<span data-ttu-id="a84be-139">In der folgenden Tabelle sind die Betriebssysteme aufgeführt, die für die Installation von DART 10-Administrator Computern unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="a84be-139">The following table lists the operating systems that are supported for the DaRT 10 administrator computer installation.</span></span>

<span data-ttu-id="a84be-140">**Hinweis**  Stellen Sie sicher, dass Sie genügend Speicherplatz für alle zusätzlichen Tools zuweisen, die Sie auf dem Administratorcomputer installieren möchten.</span><span class="sxs-lookup"><span data-stu-id="a84be-140">**Note** Make sure that you allocate enough space for any additional tools that you want to install on the administrator computer.</span></span>

 

<span data-ttu-id="a84be-141">**Hinweis**  Microsoft bietet Unterstützung für das aktuelle Service Pack und in einigen Fällen das unmittelbar vorhergehende Service Pack.</span><span class="sxs-lookup"><span data-stu-id="a84be-141">**Note** Microsoft provides support for the current service pack and, in some cases, the immediately preceding service pack.</span></span> <span data-ttu-id="a84be-142">Informationen zu den Support Zeitachsen für Ihr Produkt finden Sie unter [unterstützte Service Packs für Lebenszyklen](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span><span class="sxs-lookup"><span data-stu-id="a84be-142">To find the support timelines for your product, see the [Lifecycle Supported Service Packs](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span></span> <span data-ttu-id="a84be-143">Weitere Informationen zur Microsoft Support Lifecycle-Richtlinie finden Sie in den [FAQ zu Microsoft Support Lifecycle Support Policy](https://go.microsoft.com/fwlink/p/?LinkId=31976).</span><span class="sxs-lookup"><span data-stu-id="a84be-143">For additional information about Microsoft Support Lifecycle Policy, see [Microsoft Support Lifecycle Support Policy FAQ](https://go.microsoft.com/fwlink/p/?LinkId=31976).</span></span>

 

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
<th align="left"><span data-ttu-id="a84be-144">Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="a84be-144">Operating System</span></span></th>
<th align="left"><span data-ttu-id="a84be-145">Edition</span><span class="sxs-lookup"><span data-stu-id="a84be-145">Edition</span></span></th>
<th align="left"><span data-ttu-id="a84be-146">Service Pack</span><span class="sxs-lookup"><span data-stu-id="a84be-146">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="a84be-147">System Architektur</span><span class="sxs-lookup"><span data-stu-id="a84be-147">System Architecture</span></span></th>
<th align="left"><span data-ttu-id="a84be-148">Betriebssystemanforderungen</span><span class="sxs-lookup"><span data-stu-id="a84be-148">Operating System Requirements</span></span></th>
<th align="left"><span data-ttu-id="a84be-149">RAM-Anforderung für die Ausführung von Dart</span><span class="sxs-lookup"><span data-stu-id="a84be-149">RAM Requirement for Running DaRT</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a84be-150">Windows 10</span><span class="sxs-lookup"><span data-stu-id="a84be-150">Windows10</span></span></p></td>
<td align="left"><p><span data-ttu-id="a84be-151">Alle Editionen</span><span class="sxs-lookup"><span data-stu-id="a84be-151">All editions</span></span></p></td>
<td align="left"><p><span data-ttu-id="a84be-152">n.v.</span><span class="sxs-lookup"><span data-stu-id="a84be-152">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="a84be-153">64Bit</span><span class="sxs-lookup"><span data-stu-id="a84be-153">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="a84be-154">2 GB</span><span class="sxs-lookup"><span data-stu-id="a84be-154">2 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="a84be-155">2,5 GB</span><span class="sxs-lookup"><span data-stu-id="a84be-155">2.5 GB</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a84be-156">Windows 10</span><span class="sxs-lookup"><span data-stu-id="a84be-156">Windows10</span></span></p></td>
<td align="left"><p><span data-ttu-id="a84be-157">Alle Editionen</span><span class="sxs-lookup"><span data-stu-id="a84be-157">All editions</span></span></p></td>
<td align="left"><p><span data-ttu-id="a84be-158">n.v.</span><span class="sxs-lookup"><span data-stu-id="a84be-158">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="a84be-159">32 Bit</span><span class="sxs-lookup"><span data-stu-id="a84be-159">32-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="a84be-160">1 GB</span><span class="sxs-lookup"><span data-stu-id="a84be-160">1 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="a84be-161">1,5 GB</span><span class="sxs-lookup"><span data-stu-id="a84be-161">1.5 GB</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="-------------dart-help-desk-computer-system-requirements"></a> <span data-ttu-id="a84be-162">Systemanforderungen für Dart-Helpdesk-Computer</span><span class="sxs-lookup"><span data-stu-id="a84be-162">DaRT help desk computer system requirements</span></span>

<span data-ttu-id="a84be-163">Wenn Sie einem Helpdesk die Remote Behandlung von Computern gestatten, muss die Remote Verbindungsanzeige auf dem Helpdesk-Computer installiert sein.</span><span class="sxs-lookup"><span data-stu-id="a84be-163">If you allow a help desk to remotely troubleshoot computers, you must have the Remote Connection Viewer installed on the help desk computer.</span></span> <span data-ttu-id="a84be-164">Sie können das Crash Analyzer-Tool optional auf dem Helpdesk-Computer installieren.</span><span class="sxs-lookup"><span data-stu-id="a84be-164">You can optionally install the Crash Analyzer tool on the help desk computer.</span></span>

<span data-ttu-id="a84be-165">Dart 10 ermöglicht einem Helpdesk-Mitarbeiter, mithilfe des DART 7,0, Dart 8,0, Dart 8,1 oder Dart 10 Remote Connection Viewer eine Verbindung mit einem Dart 10-Computer herzustellen.</span><span class="sxs-lookup"><span data-stu-id="a84be-165">DaRT 10 enables a help desk worker to connect to a DaRT 10 computer by using either the DaRT 7.0, DaRT 8.0, DaRt 8.1, or DaRT 10 Remote Connection Viewer.</span></span> <span data-ttu-id="a84be-166">Die Dart 7,0, Dart 8,0 und Dart 8,1, Remote Verbindungs-Viewer erfordern Windows 7-, Windows 8-oder Windows 8,1-Betriebssysteme, während die Dart 10-Remote Verbindungsanzeige Windows 10 erfordert.</span><span class="sxs-lookup"><span data-stu-id="a84be-166">The DaRT 7.0, DaRT 8.0 and DaRt 8.1, Remote Connection Viewers require Windows 7, Windows 8, or Windows 8.1 operating systems respectively, while the DaRT 10 Remote Connection Viewer requires Windows 10.</span></span> <span data-ttu-id="a84be-167">Die Dart 10-Remote Verbindungsanzeige und alle anderen Tools von DART 10 können nur auf einem Computer mit Windows 10 installiert werden.</span><span class="sxs-lookup"><span data-stu-id="a84be-167">The DaRT 10 Remote Connection Viewer and all other DaRT 10 tools can be installed only on a computer running Windows 10.</span></span>

<span data-ttu-id="a84be-168">In der folgenden Tabelle sind die Betriebssysteme aufgeführt, die für die Installation des DART-Helpdesk-Computers unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="a84be-168">The following table lists the operating systems that are supported for the DaRT help desk computer installation.</span></span>

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
<th align="left"><span data-ttu-id="a84be-169">Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="a84be-169">Operating System</span></span></th>
<th align="left"><span data-ttu-id="a84be-170">Edition</span><span class="sxs-lookup"><span data-stu-id="a84be-170">Edition</span></span></th>
<th align="left"><span data-ttu-id="a84be-171">Service Pack</span><span class="sxs-lookup"><span data-stu-id="a84be-171">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="a84be-172">System Architektur</span><span class="sxs-lookup"><span data-stu-id="a84be-172">System Architecture</span></span></th>
<th align="left"><span data-ttu-id="a84be-173">Betriebssystemanforderungen</span><span class="sxs-lookup"><span data-stu-id="a84be-173">Operating System Requirements</span></span></th>
<th align="left"><span data-ttu-id="a84be-174">RAM-Anforderungen für die Ausführung von Dart</span><span class="sxs-lookup"><span data-stu-id="a84be-174">RAM Requirements for Running DaRT</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a84be-175">Windows 10</span><span class="sxs-lookup"><span data-stu-id="a84be-175">Windows10</span></span></p></td>
<td align="left"><p><span data-ttu-id="a84be-176">Alle Editionen</span><span class="sxs-lookup"><span data-stu-id="a84be-176">All editions</span></span></p></td>
<td align="left"><p><span data-ttu-id="a84be-177">n.v.</span><span class="sxs-lookup"><span data-stu-id="a84be-177">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="a84be-178">64Bit</span><span class="sxs-lookup"><span data-stu-id="a84be-178">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="a84be-179">2 GB</span><span class="sxs-lookup"><span data-stu-id="a84be-179">2 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="a84be-180">2,5 GB</span><span class="sxs-lookup"><span data-stu-id="a84be-180">2.5 GB</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a84be-181">Windows10 (nur mit Remote Connection Viewer 10,0)</span><span class="sxs-lookup"><span data-stu-id="a84be-181">Windows10 (with Remote Connection Viewer 10.0 only)</span></span></p></td>
<td align="left"><p><span data-ttu-id="a84be-182">Alle Editionen</span><span class="sxs-lookup"><span data-stu-id="a84be-182">All editions</span></span></p></td>
<td align="left"><p><span data-ttu-id="a84be-183">n.v.</span><span class="sxs-lookup"><span data-stu-id="a84be-183">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="a84be-184">32 Bit</span><span class="sxs-lookup"><span data-stu-id="a84be-184">32-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="a84be-185">1 GB</span><span class="sxs-lookup"><span data-stu-id="a84be-185">1 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="a84be-186">1,5 GB</span><span class="sxs-lookup"><span data-stu-id="a84be-186">1.5 GB</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a84be-187">Windows8</span><span class="sxs-lookup"><span data-stu-id="a84be-187">Windows8</span></span></p></td>
<td align="left"><p><span data-ttu-id="a84be-188">Alle Editionen</span><span class="sxs-lookup"><span data-stu-id="a84be-188">All editions</span></span></p></td>
<td align="left"><p><span data-ttu-id="a84be-189">n.v.</span><span class="sxs-lookup"><span data-stu-id="a84be-189">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="a84be-190">64Bit</span><span class="sxs-lookup"><span data-stu-id="a84be-190">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="a84be-191">2 GB</span><span class="sxs-lookup"><span data-stu-id="a84be-191">2 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="a84be-192">2,5 GB</span><span class="sxs-lookup"><span data-stu-id="a84be-192">2.5 GB</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a84be-193">Windows8 (nur mit Remote Connection Viewer 8,0)</span><span class="sxs-lookup"><span data-stu-id="a84be-193">Windows8 (with Remote Connection Viewer 8.0 only)</span></span></p></td>
<td align="left"><p><span data-ttu-id="a84be-194">Alle Editionen</span><span class="sxs-lookup"><span data-stu-id="a84be-194">All editions</span></span></p></td>
<td align="left"><p><span data-ttu-id="a84be-195">n.v.</span><span class="sxs-lookup"><span data-stu-id="a84be-195">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="a84be-196">32 Bit</span><span class="sxs-lookup"><span data-stu-id="a84be-196">32-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="a84be-197">1 GB</span><span class="sxs-lookup"><span data-stu-id="a84be-197">1 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="a84be-198">1,5 GB</span><span class="sxs-lookup"><span data-stu-id="a84be-198">1.5 GB</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a84be-199">Windows 7 (nur mit Remote Connection Viewer 7,0)</span><span class="sxs-lookup"><span data-stu-id="a84be-199">Windows 7 (with Remote Connection Viewer 7.0 only)</span></span></p></td>
<td align="left"><p><span data-ttu-id="a84be-200">Alle Editionen</span><span class="sxs-lookup"><span data-stu-id="a84be-200">All editions</span></span></p></td>
<td align="left"><p><span data-ttu-id="a84be-201">SP1, SP2</span><span class="sxs-lookup"><span data-stu-id="a84be-201">SP1, SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="a84be-202">64-Bit oder 32-Bit</span><span class="sxs-lookup"><span data-stu-id="a84be-202">64-bit or 32-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="a84be-203">1 GB</span><span class="sxs-lookup"><span data-stu-id="a84be-203">1 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="a84be-204">n.v.</span><span class="sxs-lookup"><span data-stu-id="a84be-204">N/A</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a84be-205">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a84be-205">Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="a84be-206">Standard, Enterprise, Rechenzentrum</span><span class="sxs-lookup"><span data-stu-id="a84be-206">Standard, Enterprise, Data Center</span></span></p></td>
<td align="left"><p><span data-ttu-id="a84be-207">n.v.</span><span class="sxs-lookup"><span data-stu-id="a84be-207">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="a84be-208">64Bit</span><span class="sxs-lookup"><span data-stu-id="a84be-208">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="a84be-209">2 GB</span><span class="sxs-lookup"><span data-stu-id="a84be-209">2 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="a84be-210">1,0 GB</span><span class="sxs-lookup"><span data-stu-id="a84be-210">1.0 GB</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a84be-211">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="a84be-211">Windows Server 2012 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="a84be-212">Standard, Enterprise, Rechenzentrum</span><span class="sxs-lookup"><span data-stu-id="a84be-212">Standard, Enterprise, Data Center</span></span></p></td>
<td align="left"><p><span data-ttu-id="a84be-213">n.v.</span><span class="sxs-lookup"><span data-stu-id="a84be-213">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="a84be-214">64Bit</span><span class="sxs-lookup"><span data-stu-id="a84be-214">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="a84be-215">2 GB</span><span class="sxs-lookup"><span data-stu-id="a84be-215">2 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="a84be-216">1,0 GB</span><span class="sxs-lookup"><span data-stu-id="a84be-216">1.0 GB</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="a84be-217">DART verfügt auch über die folgenden Mindestanforderungen an die Hardware für den Endbenutzercomputer:</span><span class="sxs-lookup"><span data-stu-id="a84be-217">DaRT also has the following minimum hardware requirements for the end-user computer:</span></span>

<span data-ttu-id="a84be-218">Ein CD-oder DVD-Laufwerk oder ein USB-Anschluss – nur erforderlich, wenn Sie Dart in Ihrem Unternehmen mit einer CD, DVD oder einem USB-Gerät bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="a84be-218">A CD or DVD drive or a USB port - required only if you are deploying DaRT in your enterprise by using a CD, DVD, or USB.</span></span>

<span data-ttu-id="a84be-219">BIOS-Unterstützung für das Starten des Computers von einer CD oder DVD, einem USB-Flashlaufwerk oder von einer Remote-oder Wiederherstellungspartition.</span><span class="sxs-lookup"><span data-stu-id="a84be-219">BIOS support for starting the computer from a CD or DVD, a USB flash drive, or from a remote or recovery partition.</span></span>

### <a href="" id="-------------dart-10-end-user-computer-system-requirements"></a> <span data-ttu-id="a84be-220">Dart 10 – Systemanforderungen für Endbenutzercomputer</span><span class="sxs-lookup"><span data-stu-id="a84be-220">DaRT 10 end-user computer system requirements</span></span>

<span data-ttu-id="a84be-221">Das Fenster Diagnose-und Wiederherstellungs-Toolset in DART 10 setzt voraus, dass der Endbenutzercomputer eines der folgenden Betriebssysteme zusammen mit dem angegebenen verfügbaren Speicherplatz für Dart verwendet:</span><span class="sxs-lookup"><span data-stu-id="a84be-221">The Diagnostics and Recovery Toolset window in DaRT 10 requires that the end-user computer use one of the following operating systems together with the specified amount of system memory available for DaRT:</span></span>

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
<th align="left"><span data-ttu-id="a84be-222">Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="a84be-222">Operating System</span></span></th>
<th align="left"><span data-ttu-id="a84be-223">Edition</span><span class="sxs-lookup"><span data-stu-id="a84be-223">Edition</span></span></th>
<th align="left"><span data-ttu-id="a84be-224">Service Pack</span><span class="sxs-lookup"><span data-stu-id="a84be-224">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="a84be-225">System Architektur</span><span class="sxs-lookup"><span data-stu-id="a84be-225">System Architecture</span></span></th>
<th align="left"><span data-ttu-id="a84be-226">Betriebssystemanforderungen</span><span class="sxs-lookup"><span data-stu-id="a84be-226">Operating System Requirements</span></span></th>
<th align="left"><span data-ttu-id="a84be-227">RAM-Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a84be-227">RAM Requirements</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a84be-228">Windows 10</span><span class="sxs-lookup"><span data-stu-id="a84be-228">Windows10</span></span></p></td>
<td align="left"><p><span data-ttu-id="a84be-229">Alle Editionen</span><span class="sxs-lookup"><span data-stu-id="a84be-229">All editions</span></span></p></td>
<td align="left"><p><span data-ttu-id="a84be-230">n.v.</span><span class="sxs-lookup"><span data-stu-id="a84be-230">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="a84be-231">64Bit</span><span class="sxs-lookup"><span data-stu-id="a84be-231">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="a84be-232">2 GB</span><span class="sxs-lookup"><span data-stu-id="a84be-232">2 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="a84be-233">2,5 GB</span><span class="sxs-lookup"><span data-stu-id="a84be-233">2.5 GB</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a84be-234">Windows 10</span><span class="sxs-lookup"><span data-stu-id="a84be-234">Windows10</span></span></p></td>
<td align="left"><p><span data-ttu-id="a84be-235">Alle Editionen</span><span class="sxs-lookup"><span data-stu-id="a84be-235">All editions</span></span></p></td>
<td align="left"><p><span data-ttu-id="a84be-236">n.v.</span><span class="sxs-lookup"><span data-stu-id="a84be-236">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="a84be-237">32 Bit</span><span class="sxs-lookup"><span data-stu-id="a84be-237">32-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="a84be-238">1 GB</span><span class="sxs-lookup"><span data-stu-id="a84be-238">1 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="a84be-239">1,5 GB</span><span class="sxs-lookup"><span data-stu-id="a84be-239">1.5 GB</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="a84be-240">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="a84be-240">Related topics</span></span>


[<span data-ttu-id="a84be-241">Planen der Bereitstellung von DaRT 10</span><span class="sxs-lookup"><span data-stu-id="a84be-241">Planning to Deploy DaRT 10</span></span>](planning-to-deploy-dart-10.md)

 

 





