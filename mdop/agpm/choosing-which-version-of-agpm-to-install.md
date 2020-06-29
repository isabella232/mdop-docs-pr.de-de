---
title: Welche Version von AGPM zur Installation auswählen
description: Welche Version von AGPM zur Installation auswählen
author: dansimp
ms.assetid: 31357d2a-bc23-4e15-93f4-0beda8ab7a7b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 04/05/2017
ms.openlocfilehash: b09ea8161b6801c62552f1c0d0ef8455dc111e2f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807771"
---
# <span data-ttu-id="ec522-103">Welche Version von AGPM zur Installation auswählen</span><span class="sxs-lookup"><span data-stu-id="ec522-103">Choosing Which Version of AGPM to Install</span></span>


<span data-ttu-id="ec522-104">Jede Version von MicrosoftAdvanced Group Policy Management (AGPM) unterstützt bestimmte Versionen des Windows-Betriebssystems.</span><span class="sxs-lookup"><span data-stu-id="ec522-104">Each release of MicrosoftAdvanced Group Policy Management (AGPM) supports specific versions of the Windows operating system.</span></span> <span data-ttu-id="ec522-105">Wir empfehlen dringend, dass Sie den AGPM-Client und AGPM-Server auf der gleichen Betriebssystem Zeile ausführen.</span><span class="sxs-lookup"><span data-stu-id="ec522-105">We strongly recommend that you run the AGPM Client and AGPM Server on the same line of operating systems.</span></span> <span data-ttu-id="ec522-106">Beispiel: Windows 10 mit Windows Server 2016, Windows 8.1 mit Windows Server2012 R2 usw.</span><span class="sxs-lookup"><span data-stu-id="ec522-106">For example, Windows 10 with Windows Server 2016, Windows8.1 with Windows Server2012 R2, and so on.</span></span>

<span data-ttu-id="ec522-107">Wir empfehlen, den AGPM-Server unter der neuesten Version des Betriebssystems in der Domäne zu installieren.</span><span class="sxs-lookup"><span data-stu-id="ec522-107">We recommend that you install the AGPM Server on the most recent version of the operating system in the domain.</span></span> <span data-ttu-id="ec522-108">AGPM verwendet die Gruppenrichtlinien-Verwaltungskonsole (Group Policy Management Console, GPMC) zum Sichern und Wiederherstellen von Gruppenrichtlinienobjekten (Group Policy Objects, GPOs).</span><span class="sxs-lookup"><span data-stu-id="ec522-108">AGPM uses the Group Policy Management Console (GPMC) to back up and restore Group Policy Objects (GPOs).</span></span> <span data-ttu-id="ec522-109">Da neuere Versionen der GPMC zusätzliche Richtlinieneinstellungen bereitstellen, die in früheren Versionen nicht verfügbar sind, können Sie weitere Richtlinieneinstellungen mithilfe der neuesten Version des Betriebssystems verwalten.</span><span class="sxs-lookup"><span data-stu-id="ec522-109">Because newer versions of the GPMC provide additional policy settings that are not available in earlier versions, you can manage more policy settings by using the most recent version of the operating system.</span></span>

<span data-ttu-id="ec522-110">In allen Versionen von AGPM können nur die Richtlinieneinstellungen verwaltet werden, die in der gleichen Version oder einer früheren Version des Betriebssystems, auf dem AGPM ausgeführt wird, eingeführt wurden.</span><span class="sxs-lookup"><span data-stu-id="ec522-110">All versions of AGPM can manage only the policy settings that were introduced in the same version or an earlier version of the operating system on which AGPM is running.</span></span> <span data-ttu-id="ec522-111">Wenn Sie beispielsweise AGPM 4.0 SP2 unter Windows Server 2012 installieren, können Sie Richtlinieneinstellungen verwalten, die in Windows Server 2012 oder früher eingeführt wurden, Sie können jedoch keine Richtlinieneinstellungen verwalten, die später in Windows 8.1 oder Windows Server2012 R2 eingeführt wurden.</span><span class="sxs-lookup"><span data-stu-id="ec522-111">For example, if you install AGPM4.0 SP2 on Windows Server 2012, you can manage policy settings that were introduced in Windows Server 2012 or earlier, but you cannot manage policy settings that were introduced later, in Windows8.1 or Windows Server2012 R2.</span></span>

<span data-ttu-id="ec522-112">Wenn die Version der GPMC auf dem AGPM-Server älter als die Version auf den Computern ist, die von Administratoren zum Verwalten von Gruppenrichtlinien verwendet werden, kann der AGPM-Server keine Richtlinieneinstellungen speichern, die in der älteren Version der GPMC nicht verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="ec522-112">If the version of the GPMC on your AGPM Server is older than the version on the computers that administrators use to manage Group Policy, the AGPM Server will be unable to store any policy settings that are not available in the older version of the GPMC.</span></span> <span data-ttu-id="ec522-113">Eine Tabelle mit den Gruppenrichtlinieneinstellungen in Windows finden Sie unter [Referenz zu Gruppenrichtlinieneinstellungen für Windows und Windows Server](https://go.microsoft.com/fwlink/p/?LinkId=613627).</span><span class="sxs-lookup"><span data-stu-id="ec522-113">For a spreadsheet of Group Policy settings included in Windows, see [Group Policy Settings Reference for Windows and Windows Server](https://go.microsoft.com/fwlink/p/?LinkId=613627).</span></span>

## <span data-ttu-id="ec522-114">AGPM 4.0 SP3</span><span class="sxs-lookup"><span data-stu-id="ec522-114">AGPM4.0 SP3</span></span>


<span data-ttu-id="ec522-115">Wenn Sie Computer, auf denen Windows 10 ausgeführt wird, zum Verwalten von GPOs verwenden, müssen Sie AGPM 4,0 SP3 verwenden.</span><span class="sxs-lookup"><span data-stu-id="ec522-115">If you are using computers that are running Windows 10 to manage GPOs, you must use AGPM 4.0 SP3.</span></span> <span data-ttu-id="ec522-116">Frühere Versionen von AGPM können auf Computern, auf denen das Betriebssystem Windows 10 ausgeführt wird, nicht installiert werden.</span><span class="sxs-lookup"><span data-stu-id="ec522-116">You cannot install earlier versions of AGPM on computers that are running the Windows 10 operating system.</span></span>

<span data-ttu-id="ec522-117">Tabelle 1 listet die Betriebssysteme auf, auf denen Sie AGPM 4.0 SP3 installieren können, sowie die Richtlinieneinstellungen, die Sie mithilfe von AGPM 4.0 SP3 verwalten können.</span><span class="sxs-lookup"><span data-stu-id="ec522-117">Table 1 lists the operating systems on which you can install AGPM4.0 SP3, and the policy settings that you can manage by using AGPM4.0 SP3.</span></span>

**<span data-ttu-id="ec522-118">Tabelle 1: AGPM 4,0 SP3 unterstützte Betriebssysteme und Richtlinieneinstellungen</span><span class="sxs-lookup"><span data-stu-id="ec522-118">Table 1: AGPM 4.0 SP3 supported operating systems and policy settings</span></span>**

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="ec522-119">Unterstützte Konfigurationen für den AGPM-Server</span><span class="sxs-lookup"><span data-stu-id="ec522-119">Supported configurations for the AGPM Server</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="ec522-120">Unterstützte Konfigurationen für den AGPM-Client</span><span class="sxs-lookup"><span data-stu-id="ec522-120">Supported configurations for the AGPM Client</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="ec522-121">AGPM-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="ec522-121">AGPM Support</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ec522-122">Windows Server 2016 oder Windows 10</span><span class="sxs-lookup"><span data-stu-id="ec522-122">Windows Server 2016 or Windows 10</span></span></p></td>
<td align="left"><p><span data-ttu-id="ec522-123">Windows Server 2016 oder Windows 10</span><span class="sxs-lookup"><span data-stu-id="ec522-123">Windows Server 2016 or Windows 10</span></span></p></td>
<td align="left"><p><span data-ttu-id="ec522-124">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="ec522-124">Supported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ec522-125">Windows Server2012 R2</span><span class="sxs-lookup"><span data-stu-id="ec522-125">Windows Server2012 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="ec522-126">Windows 10</span><span class="sxs-lookup"><span data-stu-id="ec522-126">Windows 10</span></span></p></td>
<td align="left"><p><span data-ttu-id="ec522-127">Unterstützt durch die in KB 4015786 beschriebenen Einschränkungen <a href="https://support.microsoft.com/help/4015786/known-issues-managing-a-windows-10-group-policy-client-in-windows-serv" data-raw-source="[KB 4015786](https://support.microsoft.com/help/4015786/known-issues-managing-a-windows-10-group-policy-client-in-windows-serv)"></span><span class="sxs-lookup"><span data-stu-id="ec522-127">Supported with the caveats outlined in <a href="https://support.microsoft.com/help/4015786/known-issues-managing-a-windows-10-group-policy-client-in-windows-serv" data-raw-source="[KB 4015786](https://support.microsoft.com/help/4015786/known-issues-managing-a-windows-10-group-policy-client-in-windows-serv)">KB 4015786</span></span></a>
</p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ec522-128">Windows Server2012 R2 oder Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="ec522-128">Windows Server2012 R2 or Windows8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="ec522-129">Windows Server2012 R2 oder Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="ec522-129">Windows Server2012 R2 or Windows8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="ec522-130">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="ec522-130">Supported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ec522-131">Windows Server2012 R2, Windows Server 2012 oder Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="ec522-131">Windows Server2012 R2, Windows Server 2012, or Windows8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="ec522-132">Windows Server 2012 oder Windows 8,1</span><span class="sxs-lookup"><span data-stu-id="ec522-132">Windows Server 2012 or Windows 8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="ec522-133">Unterstützt, aber Richtlinieneinstellungen oder Einstellungselemente, die nur in Windows 8.1 vorhanden sind, können nicht bearbeitet werden</span><span class="sxs-lookup"><span data-stu-id="ec522-133">Supported, but cannot edit policy settings or preference items that exist only in Windows8.1</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ec522-134">Windows Server2008R2 oder Windows7</span><span class="sxs-lookup"><span data-stu-id="ec522-134">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="ec522-135">Windows Server2008R2 oder Windows7</span><span class="sxs-lookup"><span data-stu-id="ec522-135">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="ec522-136">Unterstützt, aber Richtlinieneinstellungen oder Einstellungselemente, die nur in Windows 8.1 vorhanden sind, können nicht bearbeitet werden</span><span class="sxs-lookup"><span data-stu-id="ec522-136">Supported, but cannot edit policy settings or preference items that exist only in Windows8.1</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ec522-137">Windows Server 2012, Windows Server2008R2 oder Windows7</span><span class="sxs-lookup"><span data-stu-id="ec522-137">Windows Server 2012, Windows Server2008R2, or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="ec522-138">Windows Server2008 oder Windows Vista mit Service Pack 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="ec522-138">Windows Server2008 or WindowsVista with Service Pack 1 (SP1)</span></span></p></td>
<td align="left"><p><span data-ttu-id="ec522-139">Unterstützt, aber Richtlinieneinstellungen oder Einstellungselemente, die nur in Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows 8.1 oder Windows7 vorhanden sind, können nicht bearbeitet werden</span><span class="sxs-lookup"><span data-stu-id="ec522-139">Supported, but cannot edit policy settings or preference items that exist only in Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows8.1, or Windows7</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ec522-140">Windows Server2008 oder Windows Vista mit SP1</span><span class="sxs-lookup"><span data-stu-id="ec522-140">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="ec522-141">Windows Server 2012, Windows Server2008R2, Windows 8 oder Windows7</span><span class="sxs-lookup"><span data-stu-id="ec522-141">Windows Server 2012, Windows Server2008R2, Windows 8, or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="ec522-142">Nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ec522-142">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ec522-143">Windows Server2008 oder Windows Vista mit SP1</span><span class="sxs-lookup"><span data-stu-id="ec522-143">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="ec522-144">Windows Server2008 oder Windows Vista mit SP1</span><span class="sxs-lookup"><span data-stu-id="ec522-144">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="ec522-145">Unterstützt, jedoch können keine Richtlinieneinstellungen oder Einstellungselemente, die nur in Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows 8.1 oder Windows7 vorhanden sind, gemeldet oder bearbeitet werden</span><span class="sxs-lookup"><span data-stu-id="ec522-145">Supported, but cannot report or edit policy settings or preference items that exist only in Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows8.1, or Windows7</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="ec522-146">AGPM 4.0 SP2</span><span class="sxs-lookup"><span data-stu-id="ec522-146">AGPM4.0 SP2</span></span>


<span data-ttu-id="ec522-147">Wenn Sie Computer, auf denen Windows Server2012 R2 oder Windows 8.1 ausgeführt wird, zum Verwalten von GPOs verwenden, müssen Sie AGPM 4.0 SP2 verwenden.</span><span class="sxs-lookup"><span data-stu-id="ec522-147">If you are using computers that are running Windows Server2012 R2 or Windows8.1 to manage GPOs, you must use AGPM4.0 SP2.</span></span> <span data-ttu-id="ec522-148">Frühere Versionen von AGPM können auf Computern, auf denen diese Betriebssysteme ausgeführt werden, nicht installiert werden.</span><span class="sxs-lookup"><span data-stu-id="ec522-148">You cannot install earlier versions of AGPM on computers that are running those operating systems.</span></span>

<span data-ttu-id="ec522-149">Tabelle 1 listet die Betriebssysteme auf, auf denen Sie AGPM 4.0 SP2 installieren können, sowie die Richtlinieneinstellungen, die Sie mithilfe von AGPM 4.0 SP2 verwalten können.</span><span class="sxs-lookup"><span data-stu-id="ec522-149">Table 1 lists the operating systems on which you can install AGPM4.0 SP2, and the policy settings that you can manage by using AGPM4.0 SP2.</span></span>

**<span data-ttu-id="ec522-150">Tabelle 2: von AGPM 4.0 SP2 unterstützte Betriebssysteme und Richtlinieneinstellungen</span><span class="sxs-lookup"><span data-stu-id="ec522-150">Table 2: AGPM4.0 SP2 supported operating systems and policy settings</span></span>**

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="ec522-151">Unterstützte Konfigurationen für den AGPM-Server</span><span class="sxs-lookup"><span data-stu-id="ec522-151">Supported configurations for the AGPM Server</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="ec522-152">Unterstützte Konfigurationen für den AGPM-Client</span><span class="sxs-lookup"><span data-stu-id="ec522-152">Supported configurations for the AGPM Client</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="ec522-153">AGPM-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="ec522-153">AGPM Support</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ec522-154">Windows Server2012 R2 oder Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="ec522-154">Windows Server2012 R2 or Windows8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="ec522-155">Windows Server2012 R2 oder Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="ec522-155">Windows Server2012 R2 or Windows8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="ec522-156">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="ec522-156">Supported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ec522-157">Windows Server2012 R2, Windows Server 2012 oder Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="ec522-157">Windows Server2012 R2, Windows Server 2012, or Windows8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="ec522-158">Windows Server 2012 oder Windows 8,1</span><span class="sxs-lookup"><span data-stu-id="ec522-158">Windows Server 2012 or Windows 8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="ec522-159">Unterstützt, aber Richtlinieneinstellungen oder Einstellungselemente, die nur in Windows 8.1 vorhanden sind, können nicht bearbeitet werden</span><span class="sxs-lookup"><span data-stu-id="ec522-159">Supported, but cannot edit policy settings or preference items that exist only in Windows8.1</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ec522-160">Windows Server2008R2 oder Windows7</span><span class="sxs-lookup"><span data-stu-id="ec522-160">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="ec522-161">Windows Server2008R2 oder Windows7</span><span class="sxs-lookup"><span data-stu-id="ec522-161">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="ec522-162">Unterstützt, aber Richtlinieneinstellungen oder Einstellungselemente, die nur in Windows 8.1 vorhanden sind, können nicht bearbeitet werden</span><span class="sxs-lookup"><span data-stu-id="ec522-162">Supported, but cannot edit policy settings or preference items that exist only in Windows8.1</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ec522-163">Windows Server 2012, Windows Server2008R2 oder Windows7</span><span class="sxs-lookup"><span data-stu-id="ec522-163">Windows Server 2012, Windows Server2008R2, or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="ec522-164">Windows Server2008 oder Windows Vista mit Service Pack 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="ec522-164">Windows Server2008 or WindowsVista with Service Pack 1 (SP1)</span></span></p></td>
<td align="left"><p><span data-ttu-id="ec522-165">Unterstützt, aber Richtlinieneinstellungen oder Einstellungselemente, die nur in Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows 8.1 oder Windows7 vorhanden sind, können nicht bearbeitet werden</span><span class="sxs-lookup"><span data-stu-id="ec522-165">Supported, but cannot edit policy settings or preference items that exist only in Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows8.1, or Windows7</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ec522-166">Windows Server2008 oder Windows Vista mit SP1</span><span class="sxs-lookup"><span data-stu-id="ec522-166">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="ec522-167">Windows Server 2012, Windows Server2008R2 oder Windows7</span><span class="sxs-lookup"><span data-stu-id="ec522-167">Windows Server 2012, Windows Server2008R2, or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="ec522-168">Nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ec522-168">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ec522-169">Windows Server2008 oder Windows Vista mit SP1</span><span class="sxs-lookup"><span data-stu-id="ec522-169">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="ec522-170">Windows Server2008 oder Windows Vista mit SP1</span><span class="sxs-lookup"><span data-stu-id="ec522-170">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="ec522-171">Unterstützt, jedoch können keine Richtlinieneinstellungen oder Einstellungselemente, die nur in Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows 8.1 oder Windows7 vorhanden sind, gemeldet oder bearbeitet werden</span><span class="sxs-lookup"><span data-stu-id="ec522-171">Supported, but cannot report or edit policy settings or preference items that exist only in Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows8.1, or Windows7</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="ec522-172">AGPM 4.0 SP1</span><span class="sxs-lookup"><span data-stu-id="ec522-172">AGPM4.0 SP1</span></span>


<span data-ttu-id="ec522-173">In Tabelle 2 sind die Betriebssysteme aufgelistet, auf denen Sie AGPM 4,0 SP1 installieren können, sowie die Richtlinieneinstellungen, die Sie mithilfe von AGPM 4.0 SP1 verwalten können.</span><span class="sxs-lookup"><span data-stu-id="ec522-173">Table 2 lists the operating systems on which you can install AGPM 4.0 SP1, and the policy settings that you can manage by using AGPM4.0 SP1.</span></span>

**<span data-ttu-id="ec522-174">Tabelle 3: von AGPM 4.0 SP1 unterstützte Betriebssysteme und Richtlinieneinstellungen</span><span class="sxs-lookup"><span data-stu-id="ec522-174">Table 3: AGPM4.0 SP1 supported operating systems and policy settings</span></span>**

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="ec522-175">Unterstützte Konfigurationen für den AGPM-Server</span><span class="sxs-lookup"><span data-stu-id="ec522-175">Supported configurations for the AGPM Server</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="ec522-176">Unterstützte Konfigurationen für den AGPM-Client</span><span class="sxs-lookup"><span data-stu-id="ec522-176">Supported configurations for the AGPM Client</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="ec522-177">AGPM-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="ec522-177">AGPM Support</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ec522-178">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ec522-178">Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="ec522-179">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ec522-179">Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="ec522-180">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="ec522-180">Supported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ec522-181">Windows Server2008R2 oder Windows7</span><span class="sxs-lookup"><span data-stu-id="ec522-181">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="ec522-182">Windows Server2008R2 oder Windows7</span><span class="sxs-lookup"><span data-stu-id="ec522-182">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="ec522-183">Unterstützt, aber Richtlinieneinstellungen oder Einstellungselemente, die nur in Windows 8,1 vorhanden sind, können nicht bearbeitet werden</span><span class="sxs-lookup"><span data-stu-id="ec522-183">Supported, but cannot edit policy settings or preference items that exist only in Windows 8.1</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ec522-184">Windows Server 2012, Windows Server2008R2 oder Windows7</span><span class="sxs-lookup"><span data-stu-id="ec522-184">Windows Server 2012, Windows Server2008R2, or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="ec522-185">Windows Server2008 oder Windows Vista mit SP1</span><span class="sxs-lookup"><span data-stu-id="ec522-185">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="ec522-186">Unterstützt, aber Richtlinieneinstellungen oder Einstellungselemente, die nur in Windows Server2008R2 oder Windows7 vorhanden sind, können nicht bearbeitet werden</span><span class="sxs-lookup"><span data-stu-id="ec522-186">Supported, but cannot edit policy settings or preference items that exist only in Windows Server2008R2, or Windows7</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ec522-187">Windows Server2008 oder Windows Vista mit SP1</span><span class="sxs-lookup"><span data-stu-id="ec522-187">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="ec522-188">Windows Server 2012, Windows Server2008R2 oder Windows7</span><span class="sxs-lookup"><span data-stu-id="ec522-188">Windows Server 2012, Windows Server2008R2, or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="ec522-189">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="ec522-189">Supported</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ec522-190">Windows Server2008 oder Windows Vista mit SP1</span><span class="sxs-lookup"><span data-stu-id="ec522-190">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="ec522-191">Windows Server2008 oder Windows Vista mit SP1</span><span class="sxs-lookup"><span data-stu-id="ec522-191">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="ec522-192">Unterstützt, aber Richtlinieneinstellungen oder Einstellungselemente, die nur in Windows Server2008R2 oder Windows7 vorhanden sind, können nicht gemeldet oder bearbeitet werden</span><span class="sxs-lookup"><span data-stu-id="ec522-192">Supported, but cannot report or edit policy settings or preference items that exist only in Windows Server2008R2, or Windows7</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="ec522-193">AGPM 4.0</span><span class="sxs-lookup"><span data-stu-id="ec522-193">AGPM4.0</span></span>


<span data-ttu-id="ec522-194">In Tabelle 3 sind die Betriebssysteme aufgeführt, auf denen Sie AGPM 4,0 installieren können, sowie die Richtlinieneinstellungen, die Sie mithilfe von AGPM 4.0 verwalten können.</span><span class="sxs-lookup"><span data-stu-id="ec522-194">Table 3 lists the operating systems on which you can install AGPM 4.0, and the policy settings that you can manage by using AGPM4.0.</span></span>

**<span data-ttu-id="ec522-195">Tabelle 4: von AGPM 4.0 unterstützte Betriebssysteme und Richtlinieneinstellungen</span><span class="sxs-lookup"><span data-stu-id="ec522-195">Table 4: AGPM4.0 supported operating systems and policy settings</span></span>**

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ec522-196">Unterstützte Betriebssysteme für den AGPM-Server</span><span class="sxs-lookup"><span data-stu-id="ec522-196">Supported operating systems for the AGPM Server</span></span></th>
<th align="left"><span data-ttu-id="ec522-197">Unterstützte Betriebssysteme für den AGPM-Client</span><span class="sxs-lookup"><span data-stu-id="ec522-197">Supported operating systems for the AGPM Client</span></span></th>
<th align="left"><span data-ttu-id="ec522-198">AGPM-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="ec522-198">AGPM Support</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ec522-199">Windows Server2008R2 oder Windows7</span><span class="sxs-lookup"><span data-stu-id="ec522-199">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="ec522-200">Windows Server2008R2 oder Windows7</span><span class="sxs-lookup"><span data-stu-id="ec522-200">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="ec522-201">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="ec522-201">Supported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ec522-202">Windows Server2008R2 oder Windows7</span><span class="sxs-lookup"><span data-stu-id="ec522-202">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="ec522-203">Windows Server2008 oder Windows Vista mit SP1</span><span class="sxs-lookup"><span data-stu-id="ec522-203">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="ec522-204">Unterstützt, aber Richtlinieneinstellungen oder Einstellungselemente, die nur in Windows Server2008R2 oder Windows7 vorhanden sind, können nicht bearbeitet werden</span><span class="sxs-lookup"><span data-stu-id="ec522-204">Supported, but cannot edit policy settings or preference items that exist only in Windows Server2008R2 or Windows7</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ec522-205">Windows Server2008 oder Windows Vista mit SP1</span><span class="sxs-lookup"><span data-stu-id="ec522-205">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="ec522-206">Windows Server2008R2 oder Windows7</span><span class="sxs-lookup"><span data-stu-id="ec522-206">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="ec522-207">Nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ec522-207">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ec522-208">Windows Server2008 oder Windows Vista mit SP1</span><span class="sxs-lookup"><span data-stu-id="ec522-208">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="ec522-209">Windows Server2008 oder Windows Vista mit SP1</span><span class="sxs-lookup"><span data-stu-id="ec522-209">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="ec522-210">Unterstützt, aber Richtlinieneinstellungen oder Einstellungselemente, die nur in Windows Server2008R2 oder Windows7 vorhanden sind, können nicht gemeldet oder bearbeitet werden</span><span class="sxs-lookup"><span data-stu-id="ec522-210">Supported, but cannot report or edit policy settings or preference items that exist only in Windows Server2008R2 or Windows7</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="ec522-211">Versionen von AGPM, die einem AGPM 4.0 vorausgehen</span><span class="sxs-lookup"><span data-stu-id="ec522-211">Versions of AGPM that precede AGPM4.0</span></span>


<span data-ttu-id="ec522-212">Tabelle 4 listet die Betriebssysteme auf, auf denen Sie die Versionen von AGPM installieren können, die AGPM 4.0 vorangestellt sind.</span><span class="sxs-lookup"><span data-stu-id="ec522-212">Table 4 lists the operating systems on which you can install the versions of AGPM that precede AGPM4.0.</span></span> <span data-ttu-id="ec522-213">Wenn ein Betriebssystem nicht aufgeführt ist, können Sie AGPM auf diesem Betriebssystem nicht installieren.</span><span class="sxs-lookup"><span data-stu-id="ec522-213">If an operating system is not listed, you cannot install AGPM on that operating system.</span></span>

**<span data-ttu-id="ec522-214">Tabelle 5: Unterstützte Betriebssysteme für Versionen von AGPM, die AGPM 4.0 vorausgehen</span><span class="sxs-lookup"><span data-stu-id="ec522-214">Table 5: Supported operating systems for versions of AGPM that precede AGPM4.0</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ec522-215">Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="ec522-215">Operating system</span></span></th>
<th align="left"><span data-ttu-id="ec522-216">Version von AGPM, die installiert werden kann</span><span class="sxs-lookup"><span data-stu-id="ec522-216">Version of AGPM that can be installed</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ec522-217">Windows Server2008</span><span class="sxs-lookup"><span data-stu-id="ec522-217">Windows Server2008</span></span></p></td>
<td align="left"><p><span data-ttu-id="ec522-218">3.0</span><span class="sxs-lookup"><span data-stu-id="ec522-218">3.0</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ec522-219">Windows Vista mit SP1</span><span class="sxs-lookup"><span data-stu-id="ec522-219">Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="ec522-220">3.0</span><span class="sxs-lookup"><span data-stu-id="ec522-220">3.0</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ec522-221">Windows Vista ohne installiertes Service Pack (32-Bit)</span><span class="sxs-lookup"><span data-stu-id="ec522-221">WindowsVista with no service pack installed (32-bit)</span></span></p></td>
<td align="left"><p><span data-ttu-id="ec522-222">2,5</span><span class="sxs-lookup"><span data-stu-id="ec522-222">2.5</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ec522-223">Windows Server2003 (32-Bit)</span><span class="sxs-lookup"><span data-stu-id="ec522-223">Windows Server2003 (32-bit)</span></span></p></td>
<td align="left"><p><span data-ttu-id="ec522-224">2,5</span><span class="sxs-lookup"><span data-stu-id="ec522-224">2.5</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="ec522-225">So erhalten Sie MDOP-Technologien</span><span class="sxs-lookup"><span data-stu-id="ec522-225">How to Get MDOP Technologies</span></span>


<span data-ttu-id="ec522-226">AGPM 4,0 SP2 ist Teil des Microsoft Desktop Optimization Pack (MDOP).</span><span class="sxs-lookup"><span data-stu-id="ec522-226">AGPM 4.0 SP2 is a part of the Microsoft Desktop Optimization Pack (MDOP).</span></span> <span data-ttu-id="ec522-227">MDOP ist Teil von Microsoft Software Assurance.</span><span class="sxs-lookup"><span data-stu-id="ec522-227">MDOP is part of Microsoft Software Assurance.</span></span> <span data-ttu-id="ec522-228">Weitere Informationen zur Microsoft-Software Assurance und zum Erwerb von MDOP finden Sie unter [wie erhalte ich MDOP](https://go.microsoft.com/fwlink/?LinkId=322049) ( https://go.microsoft.com/fwlink/?LinkId=322049) .</span><span class="sxs-lookup"><span data-stu-id="ec522-228">For more information about Microsoft Software Assurance and acquiring MDOP, see [How Do I Get MDOP](https://go.microsoft.com/fwlink/?LinkId=322049) (https://go.microsoft.com/fwlink/?LinkId=322049).</span></span>

## <span data-ttu-id="ec522-229">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="ec522-229">Related topics</span></span>


[<span data-ttu-id="ec522-230">Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="ec522-230">Advanced Group Policy Management</span></span>](index.md)

 

 





