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
ms.openlocfilehash: f8a69fb323d9f47c5b906ac3abc6ec59376ee6f7
ms.sourcegitcommit: 0a7dee11289780336d9c24ebbf27c5c1ffee441c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/04/2020
ms.locfileid: "10905602"
---
# <span data-ttu-id="5212d-103">Welche Version von AGPM zur Installation auswählen</span><span class="sxs-lookup"><span data-stu-id="5212d-103">Choosing Which Version of AGPM to Install</span></span>


<span data-ttu-id="5212d-104">Jede Version von MicrosoftAdvanced Group Policy Management (AGPM) unterstützt bestimmte Versionen des Windows-Betriebssystems.</span><span class="sxs-lookup"><span data-stu-id="5212d-104">Each release of MicrosoftAdvanced Group Policy Management (AGPM) supports specific versions of the Windows operating system.</span></span> <span data-ttu-id="5212d-105">Wir empfehlen dringend, dass Sie den AGPM-Client und AGPM-Server auf der gleichen Betriebssystem Zeile ausführen.</span><span class="sxs-lookup"><span data-stu-id="5212d-105">We strongly recommend that you run the AGPM Client and AGPM Server on the same line of operating systems.</span></span> <span data-ttu-id="5212d-106">Beispiel: Windows 10 mit Windows Server 2016, Windows 8.1 mit Windows Server2012 R2 usw.</span><span class="sxs-lookup"><span data-stu-id="5212d-106">For example, Windows 10 with Windows Server 2016, Windows8.1 with Windows Server2012 R2, and so on.</span></span>

<span data-ttu-id="5212d-107">Wir empfehlen, den AGPM-Server unter der neuesten Version des Betriebssystems in der Domäne zu installieren.</span><span class="sxs-lookup"><span data-stu-id="5212d-107">We recommend that you install the AGPM Server on the most recent version of the operating system in the domain.</span></span> <span data-ttu-id="5212d-108">AGPM verwendet die Gruppenrichtlinien-Verwaltungskonsole (Group Policy Management Console, GPMC) zum Sichern und Wiederherstellen von Gruppenrichtlinienobjekten (Group Policy Objects, GPOs).</span><span class="sxs-lookup"><span data-stu-id="5212d-108">AGPM uses the Group Policy Management Console (GPMC) to back up and restore Group Policy Objects (GPOs).</span></span> <span data-ttu-id="5212d-109">Da neuere Versionen der GPMC zusätzliche Richtlinieneinstellungen bereitstellen, die in früheren Versionen nicht verfügbar sind, können Sie weitere Richtlinieneinstellungen mithilfe der neuesten Version des Betriebssystems verwalten.</span><span class="sxs-lookup"><span data-stu-id="5212d-109">Because newer versions of the GPMC provide additional policy settings that are not available in earlier versions, you can manage more policy settings by using the most recent version of the operating system.</span></span>

<span data-ttu-id="5212d-110">In allen Versionen von AGPM können nur die Richtlinieneinstellungen verwaltet werden, die in der gleichen Version oder einer früheren Version des Betriebssystems, auf dem AGPM ausgeführt wird, eingeführt wurden.</span><span class="sxs-lookup"><span data-stu-id="5212d-110">All versions of AGPM can manage only the policy settings that were introduced in the same version or an earlier version of the operating system on which AGPM is running.</span></span> <span data-ttu-id="5212d-111">Wenn Sie beispielsweise AGPM 4.0 SP2 unter Windows Server 2012 installieren, können Sie Richtlinieneinstellungen verwalten, die in Windows Server 2012 oder früher eingeführt wurden, Sie können jedoch keine Richtlinieneinstellungen verwalten, die später in Windows 8.1 oder Windows Server2012 R2 eingeführt wurden.</span><span class="sxs-lookup"><span data-stu-id="5212d-111">For example, if you install AGPM4.0 SP2 on Windows Server 2012, you can manage policy settings that were introduced in Windows Server 2012 or earlier, but you cannot manage policy settings that were introduced later, in Windows8.1 or Windows Server2012 R2.</span></span>

<span data-ttu-id="5212d-112">Wenn die Version der GPMC auf dem AGPM-Server älter als die Version auf den Computern ist, die von Administratoren zum Verwalten von Gruppenrichtlinien verwendet werden, kann der AGPM-Server keine Richtlinieneinstellungen speichern, die in der älteren Version der GPMC nicht verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="5212d-112">If the version of the GPMC on your AGPM Server is older than the version on the computers that administrators use to manage Group Policy, the AGPM Server will be unable to store any policy settings that are not available in the older version of the GPMC.</span></span> <span data-ttu-id="5212d-113">Eine Tabelle mit den Gruppenrichtlinieneinstellungen in Windows finden Sie unter [Referenz zu Gruppenrichtlinieneinstellungen für Windows und Windows Server](https://go.microsoft.com/fwlink/p/?LinkId=613627).</span><span class="sxs-lookup"><span data-stu-id="5212d-113">For a spreadsheet of Group Policy settings included in Windows, see [Group Policy Settings Reference for Windows and Windows Server](https://go.microsoft.com/fwlink/p/?LinkId=613627).</span></span>

## <span data-ttu-id="5212d-114">AGPM 4.0 SP3</span><span class="sxs-lookup"><span data-stu-id="5212d-114">AGPM4.0 SP3</span></span>


<span data-ttu-id="5212d-115">Wenn Sie Computer, auf denen Windows 10 ausgeführt wird, zum Verwalten von GPOs verwenden, müssen Sie AGPM 4,0 SP3 verwenden.</span><span class="sxs-lookup"><span data-stu-id="5212d-115">If you are using computers that are running Windows 10 to manage GPOs, you must use AGPM 4.0 SP3.</span></span> <span data-ttu-id="5212d-116">Frühere Versionen von AGPM können auf Computern, auf denen das Betriebssystem Windows 10 ausgeführt wird, nicht installiert werden.</span><span class="sxs-lookup"><span data-stu-id="5212d-116">You cannot install earlier versions of AGPM on computers that are running the Windows 10 operating system.</span></span>

<span data-ttu-id="5212d-117">Tabelle 1 listet die Betriebssysteme auf, auf denen Sie AGPM 4.0 SP3 installieren können, sowie die Richtlinieneinstellungen, die Sie mithilfe von AGPM 4.0 SP3 verwalten können.</span><span class="sxs-lookup"><span data-stu-id="5212d-117">Table 1 lists the operating systems on which you can install AGPM4.0 SP3, and the policy settings that you can manage by using AGPM4.0 SP3.</span></span>

**<span data-ttu-id="5212d-118">Tabelle 1: AGPM 4,0 SP3 unterstützte Betriebssysteme und Richtlinieneinstellungen</span><span class="sxs-lookup"><span data-stu-id="5212d-118">Table 1: AGPM 4.0 SP3 supported operating systems and policy settings</span></span>**

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="5212d-119">Unterstützte Konfigurationen für den AGPM-Server</span><span class="sxs-lookup"><span data-stu-id="5212d-119">Supported configurations for the AGPM Server</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="5212d-120">Unterstützte Konfigurationen für den AGPM-Client</span><span class="sxs-lookup"><span data-stu-id="5212d-120">Supported configurations for the AGPM Client</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="5212d-121">AGPM-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="5212d-121">AGPM Support</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5212d-122">Windows Server 2019 oder Windows 10</span><span class="sxs-lookup"><span data-stu-id="5212d-122">Windows Server 2019 or Windows 10</span></span></p></td>
<td align="left"><p><span data-ttu-id="5212d-123">Windows Server 2019 oder Windows 10</span><span class="sxs-lookup"><span data-stu-id="5212d-123">Windows Server 2019 or Windows 10</span></span></p></td>
<td align="left"><p><span data-ttu-id="5212d-124">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="5212d-124">Supported</span></span></p></td>
</tr>
 <tr class="even">
<td align="left"><p><span data-ttu-id="5212d-125">Windows Server 2019 oder Windows 10</span><span class="sxs-lookup"><span data-stu-id="5212d-125">Windows Server 2019 or Windows 10</span></span></p></td>
<td align="left"><p><span data-ttu-id="5212d-126">Windows Server 2019 oder Windows 10</span><span class="sxs-lookup"><span data-stu-id="5212d-126">Windows Server 2019 or Windows 10</span></span></p></td>
<td align="left"><p><span data-ttu-id="5212d-127">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="5212d-127">Supported</span></span></p></td>
</tr>
<tr class="edd">
<td align="left"><p><span data-ttu-id="5212d-128">Windows Server2012 R2</span><span class="sxs-lookup"><span data-stu-id="5212d-128">Windows Server2012 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="5212d-129">Windows 10</span><span class="sxs-lookup"><span data-stu-id="5212d-129">Windows 10</span></span></p></td>
<td align="left"><p><span data-ttu-id="5212d-130">Unterstützt durch die in KB 4015786 beschriebenen Einschränkungen <a href="https://support.microsoft.com/help/4015786/known-issues-managing-a-windows-10-group-policy-client-in-windows-serv" data-raw-source="[KB 4015786](https://support.microsoft.com/help/4015786/known-issues-managing-a-windows-10-group-policy-client-in-windows-serv)"></span><span class="sxs-lookup"><span data-stu-id="5212d-130">Supported with the caveats outlined in <a href="https://support.microsoft.com/help/4015786/known-issues-managing-a-windows-10-group-policy-client-in-windows-serv" data-raw-source="[KB 4015786](https://support.microsoft.com/help/4015786/known-issues-managing-a-windows-10-group-policy-client-in-windows-serv)">KB 4015786</span></span></a>
</p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5212d-131">Windows Server2012 R2 oder Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="5212d-131">Windows Server2012 R2 or Windows8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="5212d-132">Windows Server2012 R2 oder Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="5212d-132">Windows Server2012 R2 or Windows8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="5212d-133">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="5212d-133">Supported</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5212d-134">Windows Server2012 R2, Windows Server 2012 oder Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="5212d-134">Windows Server2012 R2, Windows Server 2012, or Windows8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="5212d-135">Windows Server 2012 oder Windows 8,1</span><span class="sxs-lookup"><span data-stu-id="5212d-135">Windows Server 2012 or Windows 8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="5212d-136">Unterstützt, aber Richtlinieneinstellungen oder Einstellungselemente, die nur in Windows 8.1 vorhanden sind, können nicht bearbeitet werden</span><span class="sxs-lookup"><span data-stu-id="5212d-136">Supported, but cannot edit policy settings or preference items that exist only in Windows8.1</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5212d-137">Windows Server2008R2 oder Windows7</span><span class="sxs-lookup"><span data-stu-id="5212d-137">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="5212d-138">Windows Server2008R2 oder Windows7</span><span class="sxs-lookup"><span data-stu-id="5212d-138">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="5212d-139">Unterstützt, aber Richtlinieneinstellungen oder Einstellungselemente, die nur in Windows 8.1 vorhanden sind, können nicht bearbeitet werden</span><span class="sxs-lookup"><span data-stu-id="5212d-139">Supported, but cannot edit policy settings or preference items that exist only in Windows8.1</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5212d-140">Windows Server 2012, Windows Server2008R2 oder Windows7</span><span class="sxs-lookup"><span data-stu-id="5212d-140">Windows Server 2012, Windows Server2008R2, or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="5212d-141">Windows Server2008 oder Windows Vista mit Service Pack 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="5212d-141">Windows Server2008 or WindowsVista with Service Pack 1 (SP1)</span></span></p></td>
<td align="left"><p><span data-ttu-id="5212d-142">Unterstützt, aber Richtlinieneinstellungen oder Einstellungselemente, die nur in Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows 8.1 oder Windows7 vorhanden sind, können nicht bearbeitet werden</span><span class="sxs-lookup"><span data-stu-id="5212d-142">Supported, but cannot edit policy settings or preference items that exist only in Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows8.1, or Windows7</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5212d-143">Windows Server2008 oder Windows Vista mit SP1</span><span class="sxs-lookup"><span data-stu-id="5212d-143">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="5212d-144">Windows Server 2012, Windows Server2008R2, Windows 8 oder Windows7</span><span class="sxs-lookup"><span data-stu-id="5212d-144">Windows Server 2012, Windows Server2008R2, Windows 8, or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="5212d-145">Nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="5212d-145">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5212d-146">Windows Server2008 oder Windows Vista mit SP1</span><span class="sxs-lookup"><span data-stu-id="5212d-146">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="5212d-147">Windows Server2008 oder Windows Vista mit SP1</span><span class="sxs-lookup"><span data-stu-id="5212d-147">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="5212d-148">Unterstützt, jedoch können keine Richtlinieneinstellungen oder Einstellungselemente, die nur in Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows 8.1 oder Windows7 vorhanden sind, gemeldet oder bearbeitet werden</span><span class="sxs-lookup"><span data-stu-id="5212d-148">Supported, but cannot report or edit policy settings or preference items that exist only in Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows8.1, or Windows7</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="5212d-149">AGPM 4.0 SP2</span><span class="sxs-lookup"><span data-stu-id="5212d-149">AGPM4.0 SP2</span></span>


<span data-ttu-id="5212d-150">Wenn Sie Computer, auf denen Windows Server2012 R2 oder Windows 8.1 ausgeführt wird, zum Verwalten von GPOs verwenden, müssen Sie AGPM 4.0 SP2 verwenden.</span><span class="sxs-lookup"><span data-stu-id="5212d-150">If you are using computers that are running Windows Server2012 R2 or Windows8.1 to manage GPOs, you must use AGPM4.0 SP2.</span></span> <span data-ttu-id="5212d-151">Frühere Versionen von AGPM können auf Computern, auf denen diese Betriebssysteme ausgeführt werden, nicht installiert werden.</span><span class="sxs-lookup"><span data-stu-id="5212d-151">You cannot install earlier versions of AGPM on computers that are running those operating systems.</span></span>

<span data-ttu-id="5212d-152">Tabelle 1 listet die Betriebssysteme auf, auf denen Sie AGPM 4.0 SP2 installieren können, sowie die Richtlinieneinstellungen, die Sie mithilfe von AGPM 4.0 SP2 verwalten können.</span><span class="sxs-lookup"><span data-stu-id="5212d-152">Table 1 lists the operating systems on which you can install AGPM4.0 SP2, and the policy settings that you can manage by using AGPM4.0 SP2.</span></span>

**<span data-ttu-id="5212d-153">Tabelle 2: von AGPM 4.0 SP2 unterstützte Betriebssysteme und Richtlinieneinstellungen</span><span class="sxs-lookup"><span data-stu-id="5212d-153">Table 2: AGPM4.0 SP2 supported operating systems and policy settings</span></span>**

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="5212d-154">Unterstützte Konfigurationen für den AGPM-Server</span><span class="sxs-lookup"><span data-stu-id="5212d-154">Supported configurations for the AGPM Server</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="5212d-155">Unterstützte Konfigurationen für den AGPM-Client</span><span class="sxs-lookup"><span data-stu-id="5212d-155">Supported configurations for the AGPM Client</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="5212d-156">AGPM-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="5212d-156">AGPM Support</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5212d-157">Windows Server2012 R2 oder Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="5212d-157">Windows Server2012 R2 or Windows8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="5212d-158">Windows Server2012 R2 oder Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="5212d-158">Windows Server2012 R2 or Windows8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="5212d-159">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="5212d-159">Supported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5212d-160">Windows Server2012 R2, Windows Server 2012 oder Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="5212d-160">Windows Server2012 R2, Windows Server 2012, or Windows8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="5212d-161">Windows Server 2012 oder Windows 8,1</span><span class="sxs-lookup"><span data-stu-id="5212d-161">Windows Server 2012 or Windows 8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="5212d-162">Unterstützt, aber Richtlinieneinstellungen oder Einstellungselemente, die nur in Windows 8.1 vorhanden sind, können nicht bearbeitet werden</span><span class="sxs-lookup"><span data-stu-id="5212d-162">Supported, but cannot edit policy settings or preference items that exist only in Windows8.1</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5212d-163">Windows Server2008R2 oder Windows7</span><span class="sxs-lookup"><span data-stu-id="5212d-163">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="5212d-164">Windows Server2008R2 oder Windows7</span><span class="sxs-lookup"><span data-stu-id="5212d-164">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="5212d-165">Unterstützt, aber Richtlinieneinstellungen oder Einstellungselemente, die nur in Windows 8.1 vorhanden sind, können nicht bearbeitet werden</span><span class="sxs-lookup"><span data-stu-id="5212d-165">Supported, but cannot edit policy settings or preference items that exist only in Windows8.1</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5212d-166">Windows Server 2012, Windows Server2008R2 oder Windows7</span><span class="sxs-lookup"><span data-stu-id="5212d-166">Windows Server 2012, Windows Server2008R2, or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="5212d-167">Windows Server2008 oder Windows Vista mit Service Pack 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="5212d-167">Windows Server2008 or WindowsVista with Service Pack 1 (SP1)</span></span></p></td>
<td align="left"><p><span data-ttu-id="5212d-168">Unterstützt, aber Richtlinieneinstellungen oder Einstellungselemente, die nur in Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows 8.1 oder Windows7 vorhanden sind, können nicht bearbeitet werden</span><span class="sxs-lookup"><span data-stu-id="5212d-168">Supported, but cannot edit policy settings or preference items that exist only in Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows8.1, or Windows7</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5212d-169">Windows Server2008 oder Windows Vista mit SP1</span><span class="sxs-lookup"><span data-stu-id="5212d-169">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="5212d-170">Windows Server 2012, Windows Server2008R2 oder Windows7</span><span class="sxs-lookup"><span data-stu-id="5212d-170">Windows Server 2012, Windows Server2008R2, or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="5212d-171">Nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="5212d-171">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5212d-172">Windows Server2008 oder Windows Vista mit SP1</span><span class="sxs-lookup"><span data-stu-id="5212d-172">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="5212d-173">Windows Server2008 oder Windows Vista mit SP1</span><span class="sxs-lookup"><span data-stu-id="5212d-173">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="5212d-174">Unterstützt, jedoch können keine Richtlinieneinstellungen oder Einstellungselemente, die nur in Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows 8.1 oder Windows7 vorhanden sind, gemeldet oder bearbeitet werden</span><span class="sxs-lookup"><span data-stu-id="5212d-174">Supported, but cannot report or edit policy settings or preference items that exist only in Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows8.1, or Windows7</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="5212d-175">AGPM 4.0 SP1</span><span class="sxs-lookup"><span data-stu-id="5212d-175">AGPM4.0 SP1</span></span>


<span data-ttu-id="5212d-176">In Tabelle 2 sind die Betriebssysteme aufgelistet, auf denen Sie AGPM 4,0 SP1 installieren können, sowie die Richtlinieneinstellungen, die Sie mithilfe von AGPM 4.0 SP1 verwalten können.</span><span class="sxs-lookup"><span data-stu-id="5212d-176">Table 2 lists the operating systems on which you can install AGPM 4.0 SP1, and the policy settings that you can manage by using AGPM4.0 SP1.</span></span>

**<span data-ttu-id="5212d-177">Tabelle 3: von AGPM 4.0 SP1 unterstützte Betriebssysteme und Richtlinieneinstellungen</span><span class="sxs-lookup"><span data-stu-id="5212d-177">Table 3: AGPM4.0 SP1 supported operating systems and policy settings</span></span>**

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="5212d-178">Unterstützte Konfigurationen für den AGPM-Server</span><span class="sxs-lookup"><span data-stu-id="5212d-178">Supported configurations for the AGPM Server</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="5212d-179">Unterstützte Konfigurationen für den AGPM-Client</span><span class="sxs-lookup"><span data-stu-id="5212d-179">Supported configurations for the AGPM Client</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="5212d-180">AGPM-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="5212d-180">AGPM Support</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5212d-181">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5212d-181">Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="5212d-182">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5212d-182">Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="5212d-183">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="5212d-183">Supported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5212d-184">Windows Server2008R2 oder Windows7</span><span class="sxs-lookup"><span data-stu-id="5212d-184">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="5212d-185">Windows Server2008R2 oder Windows7</span><span class="sxs-lookup"><span data-stu-id="5212d-185">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="5212d-186">Unterstützt, aber Richtlinieneinstellungen oder Einstellungselemente, die nur in Windows 8,1 vorhanden sind, können nicht bearbeitet werden</span><span class="sxs-lookup"><span data-stu-id="5212d-186">Supported, but cannot edit policy settings or preference items that exist only in Windows 8.1</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5212d-187">Windows Server 2012, Windows Server2008R2 oder Windows7</span><span class="sxs-lookup"><span data-stu-id="5212d-187">Windows Server 2012, Windows Server2008R2, or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="5212d-188">Windows Server2008 oder Windows Vista mit SP1</span><span class="sxs-lookup"><span data-stu-id="5212d-188">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="5212d-189">Unterstützt, aber Richtlinieneinstellungen oder Einstellungselemente, die nur in Windows Server2008R2 oder Windows7 vorhanden sind, können nicht bearbeitet werden</span><span class="sxs-lookup"><span data-stu-id="5212d-189">Supported, but cannot edit policy settings or preference items that exist only in Windows Server2008R2, or Windows7</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5212d-190">Windows Server2008 oder Windows Vista mit SP1</span><span class="sxs-lookup"><span data-stu-id="5212d-190">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="5212d-191">Windows Server 2012, Windows Server2008R2 oder Windows7</span><span class="sxs-lookup"><span data-stu-id="5212d-191">Windows Server 2012, Windows Server2008R2, or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="5212d-192">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="5212d-192">Supported</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5212d-193">Windows Server2008 oder Windows Vista mit SP1</span><span class="sxs-lookup"><span data-stu-id="5212d-193">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="5212d-194">Windows Server2008 oder Windows Vista mit SP1</span><span class="sxs-lookup"><span data-stu-id="5212d-194">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="5212d-195">Unterstützt, aber Richtlinieneinstellungen oder Einstellungselemente, die nur in Windows Server2008R2 oder Windows7 vorhanden sind, können nicht gemeldet oder bearbeitet werden</span><span class="sxs-lookup"><span data-stu-id="5212d-195">Supported, but cannot report or edit policy settings or preference items that exist only in Windows Server2008R2, or Windows7</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="5212d-196">AGPM 4.0</span><span class="sxs-lookup"><span data-stu-id="5212d-196">AGPM4.0</span></span>


<span data-ttu-id="5212d-197">In Tabelle 3 sind die Betriebssysteme aufgeführt, auf denen Sie AGPM 4,0 installieren können, sowie die Richtlinieneinstellungen, die Sie mithilfe von AGPM 4.0 verwalten können.</span><span class="sxs-lookup"><span data-stu-id="5212d-197">Table 3 lists the operating systems on which you can install AGPM 4.0, and the policy settings that you can manage by using AGPM4.0.</span></span>

**<span data-ttu-id="5212d-198">Tabelle 4: von AGPM 4.0 unterstützte Betriebssysteme und Richtlinieneinstellungen</span><span class="sxs-lookup"><span data-stu-id="5212d-198">Table 4: AGPM4.0 supported operating systems and policy settings</span></span>**

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="5212d-199">Unterstützte Betriebssysteme für den AGPM-Server</span><span class="sxs-lookup"><span data-stu-id="5212d-199">Supported operating systems for the AGPM Server</span></span></th>
<th align="left"><span data-ttu-id="5212d-200">Unterstützte Betriebssysteme für den AGPM-Client</span><span class="sxs-lookup"><span data-stu-id="5212d-200">Supported operating systems for the AGPM Client</span></span></th>
<th align="left"><span data-ttu-id="5212d-201">AGPM-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="5212d-201">AGPM Support</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5212d-202">Windows Server2008R2 oder Windows7</span><span class="sxs-lookup"><span data-stu-id="5212d-202">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="5212d-203">Windows Server2008R2 oder Windows7</span><span class="sxs-lookup"><span data-stu-id="5212d-203">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="5212d-204">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="5212d-204">Supported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5212d-205">Windows Server2008R2 oder Windows7</span><span class="sxs-lookup"><span data-stu-id="5212d-205">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="5212d-206">Windows Server2008 oder Windows Vista mit SP1</span><span class="sxs-lookup"><span data-stu-id="5212d-206">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="5212d-207">Unterstützt, aber Richtlinieneinstellungen oder Einstellungselemente, die nur in Windows Server2008R2 oder Windows7 vorhanden sind, können nicht bearbeitet werden</span><span class="sxs-lookup"><span data-stu-id="5212d-207">Supported, but cannot edit policy settings or preference items that exist only in Windows Server2008R2 or Windows7</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5212d-208">Windows Server2008 oder Windows Vista mit SP1</span><span class="sxs-lookup"><span data-stu-id="5212d-208">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="5212d-209">Windows Server2008R2 oder Windows7</span><span class="sxs-lookup"><span data-stu-id="5212d-209">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="5212d-210">Nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="5212d-210">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5212d-211">Windows Server2008 oder Windows Vista mit SP1</span><span class="sxs-lookup"><span data-stu-id="5212d-211">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="5212d-212">Windows Server2008 oder Windows Vista mit SP1</span><span class="sxs-lookup"><span data-stu-id="5212d-212">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="5212d-213">Unterstützt, aber Richtlinieneinstellungen oder Einstellungselemente, die nur in Windows Server2008R2 oder Windows7 vorhanden sind, können nicht gemeldet oder bearbeitet werden</span><span class="sxs-lookup"><span data-stu-id="5212d-213">Supported, but cannot report or edit policy settings or preference items that exist only in Windows Server2008R2 or Windows7</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="5212d-214">Versionen von AGPM, die einem AGPM 4.0 vorausgehen</span><span class="sxs-lookup"><span data-stu-id="5212d-214">Versions of AGPM that precede AGPM4.0</span></span>


<span data-ttu-id="5212d-215">Tabelle 4 listet die Betriebssysteme auf, auf denen Sie die Versionen von AGPM installieren können, die AGPM 4.0 vorangestellt sind.</span><span class="sxs-lookup"><span data-stu-id="5212d-215">Table 4 lists the operating systems on which you can install the versions of AGPM that precede AGPM4.0.</span></span> <span data-ttu-id="5212d-216">Wenn ein Betriebssystem nicht aufgeführt ist, können Sie AGPM auf diesem Betriebssystem nicht installieren.</span><span class="sxs-lookup"><span data-stu-id="5212d-216">If an operating system is not listed, you cannot install AGPM on that operating system.</span></span>

**<span data-ttu-id="5212d-217">Tabelle 5: Unterstützte Betriebssysteme für Versionen von AGPM, die AGPM 4.0 vorausgehen</span><span class="sxs-lookup"><span data-stu-id="5212d-217">Table 5: Supported operating systems for versions of AGPM that precede AGPM4.0</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="5212d-218">Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="5212d-218">Operating system</span></span></th>
<th align="left"><span data-ttu-id="5212d-219">Version von AGPM, die installiert werden kann</span><span class="sxs-lookup"><span data-stu-id="5212d-219">Version of AGPM that can be installed</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5212d-220">Windows Server2008</span><span class="sxs-lookup"><span data-stu-id="5212d-220">Windows Server2008</span></span></p></td>
<td align="left"><p><span data-ttu-id="5212d-221">3.0</span><span class="sxs-lookup"><span data-stu-id="5212d-221">3.0</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5212d-222">Windows Vista mit SP1</span><span class="sxs-lookup"><span data-stu-id="5212d-222">Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="5212d-223">3.0</span><span class="sxs-lookup"><span data-stu-id="5212d-223">3.0</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5212d-224">Windows Vista ohne installiertes Service Pack (32-Bit)</span><span class="sxs-lookup"><span data-stu-id="5212d-224">WindowsVista with no service pack installed (32-bit)</span></span></p></td>
<td align="left"><p><span data-ttu-id="5212d-225">2,5</span><span class="sxs-lookup"><span data-stu-id="5212d-225">2.5</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5212d-226">Windows Server2003 (32-Bit)</span><span class="sxs-lookup"><span data-stu-id="5212d-226">Windows Server2003 (32-bit)</span></span></p></td>
<td align="left"><p><span data-ttu-id="5212d-227">2,5</span><span class="sxs-lookup"><span data-stu-id="5212d-227">2.5</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="5212d-228">So erhalten Sie MDOP-Technologien</span><span class="sxs-lookup"><span data-stu-id="5212d-228">How to Get MDOP Technologies</span></span>


<span data-ttu-id="5212d-229">AGPM 4,0 SP2 ist Teil des Microsoft Desktop Optimization Pack (MDOP).</span><span class="sxs-lookup"><span data-stu-id="5212d-229">AGPM 4.0 SP2 is a part of the Microsoft Desktop Optimization Pack (MDOP).</span></span> <span data-ttu-id="5212d-230">MDOP ist Teil von Microsoft Software Assurance.</span><span class="sxs-lookup"><span data-stu-id="5212d-230">MDOP is part of Microsoft Software Assurance.</span></span> <span data-ttu-id="5212d-231">Weitere Informationen zur Microsoft-Software Assurance und zum Erwerb von MDOP finden Sie unter [wie erhalte ich MDOP](https://go.microsoft.com/fwlink/?LinkId=322049) ( https://go.microsoft.com/fwlink/?LinkId=322049) .</span><span class="sxs-lookup"><span data-stu-id="5212d-231">For more information about Microsoft Software Assurance and acquiring MDOP, see [How Do I Get MDOP](https://go.microsoft.com/fwlink/?LinkId=322049) (https://go.microsoft.com/fwlink/?LinkId=322049).</span></span>

## <span data-ttu-id="5212d-232">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="5212d-232">Related topics</span></span>


[<span data-ttu-id="5212d-233">Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="5212d-233">Advanced Group Policy Management</span></span>](index.md)

 

 





