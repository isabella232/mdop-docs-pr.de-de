---
title: Von MBAM 2.5 unterstützte Konfigurationen
description: Von MBAM 2.5 unterstützte Konfigurationen
author: dansimp
ms.assetid: ce689aff-9a55-4ae7-a968-23c7bda9b4d6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 10/24/2018
ms.openlocfilehash: 262cd8c259dc37b291cdaf02caf0e20b7515d38b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810228"
---
# <span data-ttu-id="8d647-103">Von MBAM 2.5 unterstützte Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="8d647-103">MBAM 2.5 Supported Configurations</span></span>


<span data-ttu-id="8d647-104">Sie können die Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) 2,5 in einer eigenständigen Topologie oder in einer Configuration Manager-Integrations Topologie ausführen, die MBAM in den System Center Configuration Manager integriert.</span><span class="sxs-lookup"><span data-stu-id="8d647-104">You can run Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 in a Stand-alone topology or in a Configuration Manager Integration topology that integrates MBAM with System Center Configuration Manager.</span></span> <span data-ttu-id="8d647-105">Wenn Sie die empfohlene Konfiguration für beide Topologien in einer Produktionsumgebung verwenden, unterstützt MBAM bis zu 500.000 MBAM-Clients.</span><span class="sxs-lookup"><span data-stu-id="8d647-105">If you use the recommended configuration for either topology in a production environment, MBAM supports up to 500,000 MBAM clients.</span></span> <span data-ttu-id="8d647-106">Informationen zu den empfohlenen Architekturen und Features, die auf den einzelnen Servern für die einzelnen Topologien konfiguriert sind, finden Sie unter [Architektur auf höherer Ebene für MBAM 2,5](high-level-architecture-for-mbam-25.md).</span><span class="sxs-lookup"><span data-stu-id="8d647-106">For information about the recommended architecture and features that are configured on each server for each topology, see [High-Level Architecture for MBAM 2.5](high-level-architecture-for-mbam-25.md).</span></span>

<span data-ttu-id="8d647-107">Weitere Konfigurationen, die speziell für die Configuration Manager-Integrations Topologie gelten, finden Sie unter [unterstützte Configuration Manager-Versionen von MBAM](#bkmk-cm-ramreqs).</span><span class="sxs-lookup"><span data-stu-id="8d647-107">For additional configurations that are specific to the Configuration Manager Integration topology, see [Versions of Configuration Manager that MBAM supports](#bkmk-cm-ramreqs).</span></span>

**<span data-ttu-id="8d647-108">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="8d647-108">Note</span></span>**  
<span data-ttu-id="8d647-109">Microsoft bietet Unterstützung für das aktuelle Service Pack und in einigen Fällen das unmittelbar vorhergehende Service Pack.</span><span class="sxs-lookup"><span data-stu-id="8d647-109">Microsoft provides support for the current service pack and, in some cases, the immediately preceding service pack.</span></span> <span data-ttu-id="8d647-110">Informationen zu den Support Zeitachsen für Ihr Produkt finden Sie unter [unterstützte Service Packs für Lebenszyklen](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span><span class="sxs-lookup"><span data-stu-id="8d647-110">To find the support timelines for your product, see the [Lifecycle Supported Service Packs](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span></span> <span data-ttu-id="8d647-111">Weitere Informationen zur Microsoft Support Lifecycle-Richtlinie finden Sie in den [FAQ zu Microsoft Support Lifecycle Support Policy](https://go.microsoft.com/fwlink/p/?LinkId=31976).</span><span class="sxs-lookup"><span data-stu-id="8d647-111">For additional information about Microsoft Support Lifecycle Policy, see [Microsoft Support Lifecycle Support Policy FAQ](https://go.microsoft.com/fwlink/p/?LinkId=31976).</span></span>



## <span data-ttu-id="8d647-112">MBAM unterstützte Sprachen</span><span class="sxs-lookup"><span data-stu-id="8d647-112">MBAM Supported Languages</span></span>


<span data-ttu-id="8d647-113">In den folgenden Tabellen werden die Sprachen aufgeführt, die für den MBAM-Client (einschließlich des Self-Service-Portals) und den MBAM-Server in MBAM 2,5 und MBAM 2,5 SP1 unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="8d647-113">The following tables show the languages that are supported for the MBAM Client (including the Self-Service Portal) and the MBAM Server in MBAM 2.5 and MBAM 2.5 SP1.</span></span>

**<span data-ttu-id="8d647-114">Unterstützte Sprachen in MBAM 2,5 SP1:</span><span class="sxs-lookup"><span data-stu-id="8d647-114">Supported Languages in MBAM 2.5 SP1:</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="8d647-115">Client Sprachen</span><span class="sxs-lookup"><span data-stu-id="8d647-115">Client Languages</span></span></th>
<th align="left"><span data-ttu-id="8d647-116">Server Sprachen</span><span class="sxs-lookup"><span data-stu-id="8d647-116">Server Languages</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8d647-117">Tschechische Republik (Tschechien) cs-cz</span><span class="sxs-lookup"><span data-stu-id="8d647-117">Czech (Czech Republic) cs-CZ</span></span></p>
<p><span data-ttu-id="8d647-118">Dänisch (Dänemark) da-DK</span><span class="sxs-lookup"><span data-stu-id="8d647-118">Danish (Denmark) da-DK</span></span></p>
<p><span data-ttu-id="8d647-119">Niederländisch (Niederlande) nl-nl</span><span class="sxs-lookup"><span data-stu-id="8d647-119">Dutch (Netherlands) nl-NL</span></span></p>
<p><span data-ttu-id="8d647-120">Englisch (USA) en-US</span><span class="sxs-lookup"><span data-stu-id="8d647-120">English (United States) en-US</span></span></p>
<p><span data-ttu-id="8d647-121">Finnisch (Finnland) fi-fi</span><span class="sxs-lookup"><span data-stu-id="8d647-121">Finnish (Finland) fi-FI</span></span></p>
<p><span data-ttu-id="8d647-122">Französisch (Frankreich) fr-FR</span><span class="sxs-lookup"><span data-stu-id="8d647-122">French (France) fr-FR</span></span></p>
<p><span data-ttu-id="8d647-123">Deutsch (Deutschland) de-de</span><span class="sxs-lookup"><span data-stu-id="8d647-123">German (Germany) de-DE</span></span></p>
<p><span data-ttu-id="8d647-124">Griechisch (Griechenland) el-gr</span><span class="sxs-lookup"><span data-stu-id="8d647-124">Greek (Greece) el-GR</span></span></p>
<p><span data-ttu-id="8d647-125">Ungarisch (Ungarn) hu-hu</span><span class="sxs-lookup"><span data-stu-id="8d647-125">Hungarian (Hungary) hu-HU</span></span></p>
<p><span data-ttu-id="8d647-126">Italienisch (Italien) IT-IT</span><span class="sxs-lookup"><span data-stu-id="8d647-126">Italian (Italy) it-IT</span></span></p>
<p><span data-ttu-id="8d647-127">Japanisch (Japan) ja-JP</span><span class="sxs-lookup"><span data-stu-id="8d647-127">Japanese (Japan) ja-JP</span></span></p>
<p><span data-ttu-id="8d647-128">Koreanisch (Korea) ko-kr</span><span class="sxs-lookup"><span data-stu-id="8d647-128">Korean (Korea) ko-KR</span></span></p>
<p><span data-ttu-id="8d647-129">Norwegisch, Nynorsk (Norwegen) NB-Nein</span><span class="sxs-lookup"><span data-stu-id="8d647-129">Norwegian, Bokmål (Norway) nb-NO</span></span></p>
<p><span data-ttu-id="8d647-130">Polnisch (Polen) pl-pl</span><span class="sxs-lookup"><span data-stu-id="8d647-130">Polish (Poland) pl-PL</span></span></p>
<p><span data-ttu-id="8d647-131">Portugiesisch (Brasilien) pt-br</span><span class="sxs-lookup"><span data-stu-id="8d647-131">Portuguese (Brazil) pt-BR</span></span></p>
<p><span data-ttu-id="8d647-132">Portugiesisch (Portugal) pt-pt</span><span class="sxs-lookup"><span data-stu-id="8d647-132">Portuguese (Portugal) pt-PT</span></span></p>
<p><span data-ttu-id="8d647-133">Russisch (Russland) ru-ru</span><span class="sxs-lookup"><span data-stu-id="8d647-133">Russian (Russia) ru-RU</span></span></p>
<p><span data-ttu-id="8d647-134">Slowakisch (Slowakei) sk-SK</span><span class="sxs-lookup"><span data-stu-id="8d647-134">Slovak (Slovakia) sk-SK</span></span></p>
<p><span data-ttu-id="8d647-135">Spanisch (Spanien) es-es</span><span class="sxs-lookup"><span data-stu-id="8d647-135">Spanish (Spain) es-ES</span></span></p>
<p><span data-ttu-id="8d647-136">SV-SE für Schwedisch (Schweden)</span><span class="sxs-lookup"><span data-stu-id="8d647-136">Swedish (Sweden) sv-SE</span></span></p>
<p><span data-ttu-id="8d647-137">Türkisch (Türkei) tr-TR</span><span class="sxs-lookup"><span data-stu-id="8d647-137">Turkish (Turkey) tr-TR</span></span></p>
<p><span data-ttu-id="8d647-138">Slowenisch (Slowenien) SL-SI</span><span class="sxs-lookup"><span data-stu-id="8d647-138">Slovenian (Slovenia) sl-SI</span></span></p>
<p><span data-ttu-id="8d647-139">Vereinfachtes Chinesisch (VR China) zh-cn</span><span class="sxs-lookup"><span data-stu-id="8d647-139">Simplified Chinese (PRC) zh-CN</span></span></p>
<p><span data-ttu-id="8d647-140">Traditionelles Chinesisch (Taiwan) zh-tw</span><span class="sxs-lookup"><span data-stu-id="8d647-140">Traditional Chinese (Taiwan) zh-TW</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="8d647-141">Englisch (USA) en-US</span><span class="sxs-lookup"><span data-stu-id="8d647-141">English (United States) en-US</span></span></p></li>
<li><p><span data-ttu-id="8d647-142">Französisch (Frankreich) fr-FR</span><span class="sxs-lookup"><span data-stu-id="8d647-142">French (France) fr-FR</span></span></p></li>
<li><p><span data-ttu-id="8d647-143">Deutsch (Deutschland) de-de</span><span class="sxs-lookup"><span data-stu-id="8d647-143">German (Germany) de-DE</span></span></p></li>
<li><p><span data-ttu-id="8d647-144">Italienisch (Italien) IT-IT</span><span class="sxs-lookup"><span data-stu-id="8d647-144">Italian (Italy) it-IT</span></span></p></li>
<li><p><span data-ttu-id="8d647-145">Japanisch (Japan) ja-JP</span><span class="sxs-lookup"><span data-stu-id="8d647-145">Japanese (Japan) ja-JP</span></span></p></li>
<li><p><span data-ttu-id="8d647-146">Koreanisch (Korea) ko-kr</span><span class="sxs-lookup"><span data-stu-id="8d647-146">Korean (Korea) ko-KR</span></span></p></li>
<li><p><span data-ttu-id="8d647-147">Portugiesisch (Brasilien) pt-br</span><span class="sxs-lookup"><span data-stu-id="8d647-147">Portuguese (Brazil) pt-BR</span></span></p></li>
<li><p><span data-ttu-id="8d647-148">Russisch (Russland) ru-ru</span><span class="sxs-lookup"><span data-stu-id="8d647-148">Russian (Russia) ru-RU</span></span></p></li>
<li><p><span data-ttu-id="8d647-149">Spanisch (Spanien) es-es</span><span class="sxs-lookup"><span data-stu-id="8d647-149">Spanish (Spain) es-ES</span></span></p></li>
<li><p><span data-ttu-id="8d647-150">Vereinfachtes Chinesisch (VR China) zh-cn</span><span class="sxs-lookup"><span data-stu-id="8d647-150">Simplified Chinese (PRC) zh-CN</span></span></p></li>
<li><p><span data-ttu-id="8d647-151">Traditionelles Chinesisch (Taiwan) zh-tw</span><span class="sxs-lookup"><span data-stu-id="8d647-151">Traditional Chinese (Taiwan) zh-TW</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="8d647-152">Unterstützte Sprachen in MBAM 2,5:</span><span class="sxs-lookup"><span data-stu-id="8d647-152">Supported Languages in MBAM 2.5:</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="8d647-153">Client Sprachen</span><span class="sxs-lookup"><span data-stu-id="8d647-153">Client Languages</span></span></th>
<th align="left"><span data-ttu-id="8d647-154">Server Sprachen</span><span class="sxs-lookup"><span data-stu-id="8d647-154">Server Languages</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><ul>
<li><p><span data-ttu-id="8d647-155">Englisch (USA) en-US</span><span class="sxs-lookup"><span data-stu-id="8d647-155">English (United States) en-US</span></span></p></li>
<li><p><span data-ttu-id="8d647-156">Französisch (Frankreich) fr-FR</span><span class="sxs-lookup"><span data-stu-id="8d647-156">French (France) fr-FR</span></span></p></li>
<li><p><span data-ttu-id="8d647-157">Deutsch (Deutschland) de-de</span><span class="sxs-lookup"><span data-stu-id="8d647-157">German (Germany) de-DE</span></span></p></li>
<li><p><span data-ttu-id="8d647-158">Italienisch (Italien) IT-IT</span><span class="sxs-lookup"><span data-stu-id="8d647-158">Italian (Italy) it-IT</span></span></p></li>
<li><p><span data-ttu-id="8d647-159">Japanisch (Japan) ja-JP</span><span class="sxs-lookup"><span data-stu-id="8d647-159">Japanese (Japan) ja-JP</span></span></p></li>
<li><p><span data-ttu-id="8d647-160">Koreanisch (Korea) ko-kr</span><span class="sxs-lookup"><span data-stu-id="8d647-160">Korean (Korea) ko-KR</span></span></p></li>
<li><p><span data-ttu-id="8d647-161">Portugiesisch (Brasilien) pt-br</span><span class="sxs-lookup"><span data-stu-id="8d647-161">Portuguese (Brazil) pt-BR</span></span></p></li>
<li><p><span data-ttu-id="8d647-162">Russisch (Russland) ru-ru</span><span class="sxs-lookup"><span data-stu-id="8d647-162">Russian (Russia) ru-RU</span></span></p></li>
<li><p><span data-ttu-id="8d647-163">Spanisch (Spanien) es-es</span><span class="sxs-lookup"><span data-stu-id="8d647-163">Spanish (Spain) es-ES</span></span></p></li>
<li><p><span data-ttu-id="8d647-164">Vereinfachtes Chinesisch (VR China) zh-cn</span><span class="sxs-lookup"><span data-stu-id="8d647-164">Simplified Chinese (PRC) zh-CN</span></span></p></li>
<li><p><span data-ttu-id="8d647-165">Traditionelles Chinesisch (Taiwan) zh-tw</span><span class="sxs-lookup"><span data-stu-id="8d647-165">Traditional Chinese (Taiwan) zh-TW</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="8d647-166">Englisch (USA) en-US</span><span class="sxs-lookup"><span data-stu-id="8d647-166">English (United States) en-US</span></span></p></li>
<li><p><span data-ttu-id="8d647-167">Französisch (Frankreich) fr-FR</span><span class="sxs-lookup"><span data-stu-id="8d647-167">French (France) fr-FR</span></span></p></li>
<li><p><span data-ttu-id="8d647-168">Deutsch (Deutschland) de-de</span><span class="sxs-lookup"><span data-stu-id="8d647-168">German (Germany) de-DE</span></span></p></li>
<li><p><span data-ttu-id="8d647-169">Italienisch (Italien) IT-IT</span><span class="sxs-lookup"><span data-stu-id="8d647-169">Italian (Italy) it-IT</span></span></p></li>
<li><p><span data-ttu-id="8d647-170">Japanisch (Japan) ja-JP</span><span class="sxs-lookup"><span data-stu-id="8d647-170">Japanese (Japan) ja-JP</span></span></p></li>
<li><p><span data-ttu-id="8d647-171">Koreanisch (Korea) ko-kr</span><span class="sxs-lookup"><span data-stu-id="8d647-171">Korean (Korea) ko-KR</span></span></p></li>
<li><p><span data-ttu-id="8d647-172">Portugiesisch (Brasilien) pt-br</span><span class="sxs-lookup"><span data-stu-id="8d647-172">Portuguese (Brazil) pt-BR</span></span></p></li>
<li><p><span data-ttu-id="8d647-173">Russisch (Russland) ru-ru</span><span class="sxs-lookup"><span data-stu-id="8d647-173">Russian (Russia) ru-RU</span></span></p></li>
<li><p><span data-ttu-id="8d647-174">Spanisch (Spanien) es-es</span><span class="sxs-lookup"><span data-stu-id="8d647-174">Spanish (Spain) es-ES</span></span></p></li>
<li><p><span data-ttu-id="8d647-175">Vereinfachtes Chinesisch (VR China) zh-cn</span><span class="sxs-lookup"><span data-stu-id="8d647-175">Simplified Chinese (PRC) zh-CN</span></span></p></li>
<li><p><span data-ttu-id="8d647-176">Traditionelles Chinesisch (Taiwan) zh-tw</span><span class="sxs-lookup"><span data-stu-id="8d647-176">Traditional Chinese (Taiwan) zh-TW</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>



## <a href="" id="---------mbam-server-system-requirements"></a> <span data-ttu-id="8d647-177">Systemanforderungen für MBAM-Server</span><span class="sxs-lookup"><span data-stu-id="8d647-177">MBAM Server system requirements</span></span>


### <span data-ttu-id="8d647-178">MBAM Server-Betriebssystemanforderungen</span><span class="sxs-lookup"><span data-stu-id="8d647-178">MBAM Server operating system requirements</span></span>

<span data-ttu-id="8d647-179">Wir empfehlen dringend, dass Sie den MBAM-Client und den MBAM-Server auf der gleichen Betriebssystem Zeile ausführen.</span><span class="sxs-lookup"><span data-stu-id="8d647-179">We strongly recommend that you run the MBAM Client and MBAM Server on the same line of operating systems.</span></span> <span data-ttu-id="8d647-180">Beispiel: Windows 10 mit Windows Server 2016, Windows 8,1 mit Windows Server 2012 R2 usw.</span><span class="sxs-lookup"><span data-stu-id="8d647-180">For example, Windows 10 with Windows Server 2016, Windows 8.1 with Windows Server 2012 R2, and so on.</span></span>

<span data-ttu-id="8d647-181">In der folgenden Tabelle sind die Betriebssysteme aufgeführt, die für die Installation des MBAM-Servers unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="8d647-181">The following table lists the operating systems that are supported for the MBAM Server installation.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="8d647-182">Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="8d647-182">Operating system</span></span></th>
<th align="left"><span data-ttu-id="8d647-183">Edition</span><span class="sxs-lookup"><span data-stu-id="8d647-183">Edition</span></span></th>
<th align="left"><span data-ttu-id="8d647-184">Service Pack</span><span class="sxs-lookup"><span data-stu-id="8d647-184">Service pack</span></span></th>
<th align="left"><span data-ttu-id="8d647-185">System Architektur</span><span class="sxs-lookup"><span data-stu-id="8d647-185">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8d647-186">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="8d647-186">Windows Server 2016</span></span></p></td>
<td align="left"><p><span data-ttu-id="8d647-187">Standard oder Rechenzentrum</span><span class="sxs-lookup"><span data-stu-id="8d647-187">Standard or Datacenter</span></span></p></td>
<td align="left"></td>
<td align="left"><p><span data-ttu-id="8d647-188">64Bit</span><span class="sxs-lookup"><span data-stu-id="8d647-188">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8d647-189">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="8d647-189">Windows Server 2012 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="8d647-190">Standard oder Rechenzentrum</span><span class="sxs-lookup"><span data-stu-id="8d647-190">Standard or Datacenter</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="8d647-191">64Bit</span><span class="sxs-lookup"><span data-stu-id="8d647-191">64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8d647-192">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8d647-192">Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="8d647-193">Standard oder Rechenzentrum</span><span class="sxs-lookup"><span data-stu-id="8d647-193">Standard or Datacenter</span></span></p></td>
<td align="left"></td>
<td align="left"><p><span data-ttu-id="8d647-194">64Bit</span><span class="sxs-lookup"><span data-stu-id="8d647-194">64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8d647-195">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8d647-195">Windows Server 2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="8d647-196">Standard, Enterprise oder Datacenter</span><span class="sxs-lookup"><span data-stu-id="8d647-196">Standard, Enterprise, or Datacenter</span></span></p></td>
<td align="left"><p><span data-ttu-id="8d647-197">SP1</span><span class="sxs-lookup"><span data-stu-id="8d647-197">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="8d647-198">64Bit</span><span class="sxs-lookup"><span data-stu-id="8d647-198">64-bit</span></span></p></td>
</tr>
</tbody>
</table>



<span data-ttu-id="8d647-199">Die Unternehmensdomäne muss mindestens einen Windows Server 2008-Domänencontroller (oder höher) enthalten.</span><span class="sxs-lookup"><span data-stu-id="8d647-199">The enterprise domain must contain at least one Windows Server 2008 (or later) domain controller.</span></span>

### <a href="" id="bkmk-stand-alone-ramreqs"></a><span data-ttu-id="8d647-200">MBAM-Server Prozessor, RAM und Speicherplatzanforderungen – eigenständige Topologie</span><span class="sxs-lookup"><span data-stu-id="8d647-200">MBAM Server processor, RAM, and disk space requirements – Stand-alone topology</span></span>

<span data-ttu-id="8d647-201">Diese Anforderungen gelten für die eigenständige MBAM-Topologie.</span><span class="sxs-lookup"><span data-stu-id="8d647-201">These requirements are for the MBAM Stand-alone topology.</span></span> <span data-ttu-id="8d647-202">Die Anforderungen für die Configuration Manager-Integrations Topologie finden Sie unter [MBAM-Server Prozessor, RAM und Speicherplatzanforderungen – Configuration Manager-Integrations Topologie](#bkmk-cm-ramreqs).</span><span class="sxs-lookup"><span data-stu-id="8d647-202">For the requirements for the Configuration Manager Integration topology, see [MBAM Server Processor, RAM, and Disk Space Requirements - Configuration Manager Integration Topology](#bkmk-cm-ramreqs).</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="8d647-203">Hardware Element</span><span class="sxs-lookup"><span data-stu-id="8d647-203">Hardware item</span></span></th>
<th align="left"><span data-ttu-id="8d647-204">Mindestanforderungen</span><span class="sxs-lookup"><span data-stu-id="8d647-204">Minimum requirement</span></span></th>
<th align="left"><span data-ttu-id="8d647-205">Empfohlene Anforderung</span><span class="sxs-lookup"><span data-stu-id="8d647-205">Recommended requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8d647-206">Prozessor</span><span class="sxs-lookup"><span data-stu-id="8d647-206">Processor</span></span></p></td>
<td align="left"><p><span data-ttu-id="8d647-207">2,33 GHz</span><span class="sxs-lookup"><span data-stu-id="8d647-207">2.33 GHz</span></span></p></td>
<td align="left"><p><span data-ttu-id="8d647-208">2,33 GHz oder höher</span><span class="sxs-lookup"><span data-stu-id="8d647-208">2.33 GHz or greater</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8d647-209">RAM</span><span class="sxs-lookup"><span data-stu-id="8d647-209">RAM</span></span></p></td>
<td align="left"><p><span data-ttu-id="8d647-210">8 GB</span><span class="sxs-lookup"><span data-stu-id="8d647-210">8 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="8d647-211">12 GB</span><span class="sxs-lookup"><span data-stu-id="8d647-211">12 GB</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8d647-212">Freier Speicherplatz</span><span class="sxs-lookup"><span data-stu-id="8d647-212">Free disk space</span></span></p></td>
<td align="left"><p><span data-ttu-id="8d647-213">1 GB</span><span class="sxs-lookup"><span data-stu-id="8d647-213">1 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="8d647-214">2 GB</span><span class="sxs-lookup"><span data-stu-id="8d647-214">2 GB</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-cm-ramreqs"></a><span data-ttu-id="8d647-215">MBAM-Server Prozessor, RAM und Speicherplatzanforderungen – Configuration Manager-Integrations Topologie</span><span class="sxs-lookup"><span data-stu-id="8d647-215">MBAM Server processor, RAM, and disk space requirements - Configuration Manager Integration topology</span></span>

<span data-ttu-id="8d647-216">In der folgenden Tabelle sind die Server Prozessor-, RAM-und Speicherplatzanforderungen für MBAM-Server aufgelistet, wenn Sie die Configuration Manager-Integrations Topologie verwenden.</span><span class="sxs-lookup"><span data-stu-id="8d647-216">The following table lists the server processor, RAM, and disk space requirements for MBAM servers when you are using the Configuration Manager Integration topology.</span></span> <span data-ttu-id="8d647-217">Die Anforderungen für die eigenständige Topologie finden Sie unter [MBAM-Server Prozessor, RAM und Speicherplatzanforderungen – eigenständige Topologie](#bkmk-stand-alone-ramreqs).</span><span class="sxs-lookup"><span data-stu-id="8d647-217">For the requirements for the Stand-alone topology, see [MBAM Server Processor, RAM, and Disk Space Requirements – Stand-alone Topology](#bkmk-stand-alone-ramreqs).</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="8d647-218">Hardware Element</span><span class="sxs-lookup"><span data-stu-id="8d647-218">Hardware item</span></span></th>
<th align="left"><span data-ttu-id="8d647-219">Mindestanforderungen</span><span class="sxs-lookup"><span data-stu-id="8d647-219">Minimum requirement</span></span></th>
<th align="left"><span data-ttu-id="8d647-220">Empfohlene Anforderung</span><span class="sxs-lookup"><span data-stu-id="8d647-220">Recommended requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8d647-221">Prozessor</span><span class="sxs-lookup"><span data-stu-id="8d647-221">Processor</span></span></p></td>
<td align="left"><p><span data-ttu-id="8d647-222">2,33 GHz</span><span class="sxs-lookup"><span data-stu-id="8d647-222">2.33 GHz</span></span></p></td>
<td align="left"><p><span data-ttu-id="8d647-223">2,33 GHz oder höher</span><span class="sxs-lookup"><span data-stu-id="8d647-223">2.33 GHz or greater</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8d647-224">RAM</span><span class="sxs-lookup"><span data-stu-id="8d647-224">RAM</span></span></p></td>
<td align="left"><p><span data-ttu-id="8d647-225">4 GB</span><span class="sxs-lookup"><span data-stu-id="8d647-225">4 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="8d647-226">8 GB</span><span class="sxs-lookup"><span data-stu-id="8d647-226">8 GB</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8d647-227">Freier Speicherplatz</span><span class="sxs-lookup"><span data-stu-id="8d647-227">Free disk space</span></span></p></td>
<td align="left"><p><span data-ttu-id="8d647-228">1 GB</span><span class="sxs-lookup"><span data-stu-id="8d647-228">1 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="8d647-229">2 GB</span><span class="sxs-lookup"><span data-stu-id="8d647-229">2 GB</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-cmversions"></a><span data-ttu-id="8d647-230">Von MBAM unterstützte Versionen von Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="8d647-230">Versions of Configuration Manager that MBAM supports</span></span>

<span data-ttu-id="8d647-231">MBAM unterstützt die folgenden Versionen von Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="8d647-231">MBAM supports the following versions of Configuration Manager.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="8d647-232">Unterstützte Version</span><span class="sxs-lookup"><span data-stu-id="8d647-232">Supported version</span></span></th>
<th align="left"><span data-ttu-id="8d647-233">Service Pack</span><span class="sxs-lookup"><span data-stu-id="8d647-233">Service pack</span></span></th>
<th align="left"><span data-ttu-id="8d647-234">System Architektur</span><span class="sxs-lookup"><span data-stu-id="8d647-234">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="even">
<td align="left"><p><span data-ttu-id="8d647-235">Microsoft System Center Configuration Manager (aktueller Zweig), Versionen bis zu 1902</span><span class="sxs-lookup"><span data-stu-id="8d647-235">Microsoft System Center Configuration Manager (Current Branch), versions up to 1902</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="8d647-236">64Bit</span><span class="sxs-lookup"><span data-stu-id="8d647-236">64-bit</span></span></p></td>
</tr>

<tr class="odd">
<td align="left"><p><span data-ttu-id="8d647-237">Microsoft System Center Configuration Manager 1806</span><span class="sxs-lookup"><span data-stu-id="8d647-237">Microsoft System Center Configuration Manager 1806</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="8d647-238">64Bit</span><span class="sxs-lookup"><span data-stu-id="8d647-238">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8d647-239">Microsoft System Center Configuration Manager (LTSB-Version 1606)</span><span class="sxs-lookup"><span data-stu-id="8d647-239">Microsoft System Center Configuration Manager (LTSB - version 1606)</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="8d647-240">64Bit</span><span class="sxs-lookup"><span data-stu-id="8d647-240">64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8d647-241">Microsoft System Center 2012-Konfigurations-Manager</span><span class="sxs-lookup"><span data-stu-id="8d647-241">Microsoft System Center 2012 Configuration Manager</span></span></p></td>
<td align="left"><p><span data-ttu-id="8d647-242">SP1</span><span class="sxs-lookup"><span data-stu-id="8d647-242">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="8d647-243">64Bit</span><span class="sxs-lookup"><span data-stu-id="8d647-243">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8d647-244">Microsoft System Center Configuration Manager 2007 R2 oder höher</span><span class="sxs-lookup"><span data-stu-id="8d647-244">Microsoft System Center Configuration Manager 2007 R2 or later</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="8d647-245">64Bit</span><span class="sxs-lookup"><span data-stu-id="8d647-245">64-bit</span></span></p>

<span data-ttu-id="8d647-246">&gt;<strong>Hinweis </strong> Obwohl Configuration Manager 2007 R2 32-Bit ist, müssen Sie es und SQL Server auf einem 64-Bit-Betriebssystem installieren, um der 64-Bit-MBAM-Software entsprechen zu können.</span><span class="sxs-lookup"><span data-stu-id="8d647-246">&gt;<strong>Note</strong> Although Configuration Manager 2007 R2 is 32 bit, you must install it and SQL Server on a 64-bit operating system in order to match the 64-bit MBAM software.</span></span>
</td>
</tr>
</tbody>
</table>



<span data-ttu-id="8d647-247">Eine Liste der unterstützten Konfigurationen für den Configuration Manager-Server finden Sie in der entsprechenden TechNet-Dokumentation für die Version von Configuration Manager, die Sie verwenden.</span><span class="sxs-lookup"><span data-stu-id="8d647-247">For a list of supported configurations for the Configuration Manager Server, see the appropriate TechNet documentation for the version of Configuration Manager that you are using.</span></span> <span data-ttu-id="8d647-248">MBAM hat keine zusätzlichen Systemanforderungen für den Configuration Manager-Server.</span><span class="sxs-lookup"><span data-stu-id="8d647-248">MBAM has no additional system requirements for the Configuration Manager Server.</span></span>

### <a href="" id="sql-server-database-requirements-"></a><span data-ttu-id="8d647-249">SQL Server-Datenbankanforderungen</span><span class="sxs-lookup"><span data-stu-id="8d647-249">SQL Server database requirements</span></span>

<span data-ttu-id="8d647-250">In der folgenden Tabelle sind die Microsoft SQL Server-Versionen aufgeführt, die für die MBAM-Server Features unterstützt werden, einschließlich der Datenbank für die Wiederherstellungsdatenbank, der Kompatibilitäts-und Überwachungsdatenbank sowie des Berichtsfeatures.</span><span class="sxs-lookup"><span data-stu-id="8d647-250">The following table lists the Microsoft SQL Server versions that are supported for the MBAM Server features, which include the Recovery Database, Compliance and Audit Database, and the Reports feature.</span></span> <span data-ttu-id="8d647-251">Die erforderlichen Versionen gelten für die eigenständige oder die Configuration Manager-Integrations Topologie.</span><span class="sxs-lookup"><span data-stu-id="8d647-251">The required versions apply to the Stand-alone or the Configuration Manager Integration topologies.</span></span>

<span data-ttu-id="8d647-252">Sie müssen SQL Server mit dem **SQL \ _Latin1 \ _General \ _CP1 \ _ci \ _AS** Sortierreihenfolge installieren.</span><span class="sxs-lookup"><span data-stu-id="8d647-252">You must install SQL Server with the **SQL\_Latin1\_General\_CP1\_CI\_AS** collation.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="8d647-253">SQL Server-Version</span><span class="sxs-lookup"><span data-stu-id="8d647-253">SQL Server version</span></span></th>
<th align="left"><span data-ttu-id="8d647-254">Edition</span><span class="sxs-lookup"><span data-stu-id="8d647-254">Edition</span></span></th>
<th align="left"><span data-ttu-id="8d647-255">Service Pack</span><span class="sxs-lookup"><span data-stu-id="8d647-255">Service pack</span></span></th>
<th align="left"><span data-ttu-id="8d647-256">System Architektur</span><span class="sxs-lookup"><span data-stu-id="8d647-256">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8d647-257">Microsoft SQL Server 2017</span><span class="sxs-lookup"><span data-stu-id="8d647-257">Microsoft SQL Server 2017</span></span></p></td>
<td align="left"><p><span data-ttu-id="8d647-258">Standard, Enterprise oder Datacenter</span><span class="sxs-lookup"><span data-stu-id="8d647-258">Standard, Enterprise, or Datacenter</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="8d647-259">64Bit</span><span class="sxs-lookup"><span data-stu-id="8d647-259">64-bit</span></span></p></td><br/><tr class="even">
<td align="left"><p><span data-ttu-id="8d647-260">Microsoft SQL Server 2016</span><span class="sxs-lookup"><span data-stu-id="8d647-260">Microsoft SQL Server 2016</span></span></p></td>
<td align="left"><p><span data-ttu-id="8d647-261">Standard, Enterprise oder Datacenter</span><span class="sxs-lookup"><span data-stu-id="8d647-261">Standard, Enterprise, or Datacenter</span></span></p></td>
<td align="left"><p><span data-ttu-id="8d647-262">SP1</span><span class="sxs-lookup"><span data-stu-id="8d647-262">SP1</span></span></p></td>
<a href="https://www.microsoft.com/download/details.aspx?id=54967" data-raw-source="https://www.microsoft.com/download/details.aspx?id=54967">https://www.microsoft.com/download/details.aspx?id=54967</a><td align="left"><p><span data-ttu-id="8d647-263">64Bit</span><span class="sxs-lookup"><span data-stu-id="8d647-263">64-bit</span></span></p></td>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8d647-264">Microsoft SQL Server 2014</span><span class="sxs-lookup"><span data-stu-id="8d647-264">Microsoft SQL Server 2014</span></span></p></td>
<td align="left"><p><span data-ttu-id="8d647-265">Standard, Enterprise oder Datacenter</span><span class="sxs-lookup"><span data-stu-id="8d647-265">Standard, Enterprise, or Datacenter</span></span></p></td>
<td align="left"><p><span data-ttu-id="8d647-266">SP1, SP2</span><span class="sxs-lookup"><span data-stu-id="8d647-266">SP1, SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="8d647-267">64Bit</span><span class="sxs-lookup"><span data-stu-id="8d647-267">64-bit</span></span></p></td>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8d647-268">Microsoft SQL Server 2012</span><span class="sxs-lookup"><span data-stu-id="8d647-268">Microsoft SQL Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="8d647-269">Standard, Enterprise oder Datacenter</span><span class="sxs-lookup"><span data-stu-id="8d647-269">Standard, Enterprise, or Datacenter</span></span></p></td>
<td align="left"><p><span data-ttu-id="8d647-270">SP3</span><span class="sxs-lookup"><span data-stu-id="8d647-270">SP3</span></span></p></td>
<td align="left"><p><span data-ttu-id="8d647-271">64Bit</span><span class="sxs-lookup"><span data-stu-id="8d647-271">64-bit</span></span></p></td>
<tr class="even">
<td align="left"><p><span data-ttu-id="8d647-272">Microsoft SQL Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8d647-272">Microsoft SQL Server 2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="8d647-273">Standard oder Enterprise</span><span class="sxs-lookup"><span data-stu-id="8d647-273">Standard or Enterprise</span></span></p></td>
<td align="left"><p><span data-ttu-id="8d647-274">SP3</span><span class="sxs-lookup"><span data-stu-id="8d647-274">SP3</span></span></p></td>
<td align="left"><p><span data-ttu-id="8d647-275">64Bit</span><span class="sxs-lookup"><span data-stu-id="8d647-275">64-bit</span></span></p></td>
</tr>
</tbody>
</table>

**<span data-ttu-id="8d647-276">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="8d647-276">Note</span></span>**  
<span data-ttu-id="8d647-277">Um SQL 2016 zu unterstützen, müssen Sie die Service Version für März 2017 für MDOP installieren https://www.microsoft.com/download/details.aspx?id=54967 und SQL 2017 unterstützen, wenn Sie die Version vom Juli 2018 für MDOP installieren müssen https://www.microsoft.com/download/details.aspx?id=57157 .</span><span class="sxs-lookup"><span data-stu-id="8d647-277">In order to support SQL 2016 you must install the March 2017 Servicing Release for MDOP https://www.microsoft.com/download/details.aspx?id=54967  and to support SQL 2017 you must install the July 2018 Servicing Release for MDOP https://www.microsoft.com/download/details.aspx?id=57157.</span></span> <span data-ttu-id="8d647-278">Im allgemeinen bleiben Sie stets auf dem laufenden, indem Sie immer das neueste Wartungsupdate verwenden, da es auch alle Bugfixes und neuen Features enthält.</span><span class="sxs-lookup"><span data-stu-id="8d647-278">In general stay current by always using the most recent servicing update as it also includes all bugfixes and new features.</span></span>


### <a href="" id="bkmk-sql-stand-alone-ramreqs"></a><span data-ttu-id="8d647-279">SQL Server-Prozessor, RAM und Speicherplatzanforderungen – eigenständige Topologie</span><span class="sxs-lookup"><span data-stu-id="8d647-279">SQL Server processor, RAM, and disk space requirements – Stand-alone topology</span></span>

<span data-ttu-id="8d647-280">In der folgenden Tabelle sind die empfohlenen Server Prozessor-, RAM-und Speicherplatzanforderungen für den SQL Server-Computer aufgeführt, wenn Sie die eigenständige Topologie verwenden.</span><span class="sxs-lookup"><span data-stu-id="8d647-280">The following table lists the recommended server processor, RAM, and disk space requirements for the SQL Server computer when you are using the Stand-alone topology.</span></span> <span data-ttu-id="8d647-281">Verwenden Sie diese Anforderungen als Leitfaden.</span><span class="sxs-lookup"><span data-stu-id="8d647-281">Use these requirements as a guide.</span></span> <span data-ttu-id="8d647-282">Ihre spezifischen Anforderungen unterscheiden sich je nach der Anzahl der Clientcomputer, die Sie in Ihrem Unternehmen unterstützen.</span><span class="sxs-lookup"><span data-stu-id="8d647-282">Your specific requirements will vary based on the number of client computers you are supporting in your enterprise.</span></span> <span data-ttu-id="8d647-283">Informationen zum Anzeigen der Anforderungen für die Configuration Manager-Integrations Topologie finden Sie unter [SQL Server-Prozessor, RAM und Speicherplatzanforderungen – Configuration Manager-Integrations Topologie](#bkmk-cm-sql-ramreqs).</span><span class="sxs-lookup"><span data-stu-id="8d647-283">To view the requirements for the Configuration Manager Integration topology, see [SQL Server Processor, RAM, and Disk Space Requirements - Configuration Manager Integration Topology](#bkmk-cm-sql-ramreqs).</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="8d647-284">Hardware Element</span><span class="sxs-lookup"><span data-stu-id="8d647-284">Hardware item</span></span></th>
<th align="left"><span data-ttu-id="8d647-285">Mindestanforderungen</span><span class="sxs-lookup"><span data-stu-id="8d647-285">Minimum requirement</span></span></th>
<th align="left"><span data-ttu-id="8d647-286">Empfohlene Anforderung</span><span class="sxs-lookup"><span data-stu-id="8d647-286">Recommended requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8d647-287">Prozessor</span><span class="sxs-lookup"><span data-stu-id="8d647-287">Processor</span></span></p></td>
<td align="left"><p><span data-ttu-id="8d647-288">2,33 GHz</span><span class="sxs-lookup"><span data-stu-id="8d647-288">2.33 GHz</span></span></p></td>
<td align="left"><p><span data-ttu-id="8d647-289">2,33 GHz oder höher</span><span class="sxs-lookup"><span data-stu-id="8d647-289">2.33 GHz or greater</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8d647-290">RAM</span><span class="sxs-lookup"><span data-stu-id="8d647-290">RAM</span></span></p></td>
<td align="left"><p><span data-ttu-id="8d647-291">8 GB</span><span class="sxs-lookup"><span data-stu-id="8d647-291">8 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="8d647-292">12 GB</span><span class="sxs-lookup"><span data-stu-id="8d647-292">12 GB</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8d647-293">Freier Speicherplatz</span><span class="sxs-lookup"><span data-stu-id="8d647-293">Free disk space</span></span></p></td>
<td align="left"><p><span data-ttu-id="8d647-294">5 GB</span><span class="sxs-lookup"><span data-stu-id="8d647-294">5 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="8d647-295">5 GB oder höher</span><span class="sxs-lookup"><span data-stu-id="8d647-295">5 GB or greater</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-cm-sql-ramreqs"></a><span data-ttu-id="8d647-296">SQL Server-Prozessor, RAM und Speicherplatzanforderungen – Configuration Manager-Integrations Topologie</span><span class="sxs-lookup"><span data-stu-id="8d647-296">SQL Server processor, RAM, and disk space requirements - Configuration Manager Integration topology</span></span>

<span data-ttu-id="8d647-297">In der folgenden Tabelle sind die Anforderungen für den Server Prozessor, den Arbeitsspeicher und den Speicherplatz für den Microsoft SQL Server-Computer aufgeführt, wenn Sie die Configuration Manager-Integrations Topologie verwenden, siehe [SQL Server-Prozessor, RAM und Speicherplatzanforderungen – eigenständige Topologie](#bkmk-sql-stand-alone-ramreqs).</span><span class="sxs-lookup"><span data-stu-id="8d647-297">The following table lists the server processor, RAM, and disk space requirements for the Microsoft SQL Server computer when you are using the Configuration Manager Integration topology, see [SQL Server Processor, RAM, and Disk Space Requirements – Stand-alone Topology](#bkmk-sql-stand-alone-ramreqs).</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="8d647-298">Hardware Element</span><span class="sxs-lookup"><span data-stu-id="8d647-298">Hardware item</span></span></th>
<th align="left"><span data-ttu-id="8d647-299">Mindestanforderungen</span><span class="sxs-lookup"><span data-stu-id="8d647-299">Minimum requirement</span></span></th>
<th align="left"><span data-ttu-id="8d647-300">Empfohlene Anforderung</span><span class="sxs-lookup"><span data-stu-id="8d647-300">Recommended requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8d647-301">Prozessor</span><span class="sxs-lookup"><span data-stu-id="8d647-301">Processor</span></span></p></td>
<td align="left"><p><span data-ttu-id="8d647-302">2,33 GHz</span><span class="sxs-lookup"><span data-stu-id="8d647-302">2.33 GHz</span></span></p></td>
<td align="left"><p><span data-ttu-id="8d647-303">2,33 GHz oder höher</span><span class="sxs-lookup"><span data-stu-id="8d647-303">2.33 GHz or greater</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8d647-304">RAM</span><span class="sxs-lookup"><span data-stu-id="8d647-304">RAM</span></span></p></td>
<td align="left"><p><span data-ttu-id="8d647-305">4 GB</span><span class="sxs-lookup"><span data-stu-id="8d647-305">4 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="8d647-306">8 GB</span><span class="sxs-lookup"><span data-stu-id="8d647-306">8 GB</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8d647-307">Freier Speicherplatz</span><span class="sxs-lookup"><span data-stu-id="8d647-307">Free disk space</span></span></p></td>
<td align="left"><p><span data-ttu-id="8d647-308">5 GB</span><span class="sxs-lookup"><span data-stu-id="8d647-308">5 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="8d647-309">5 GB</span><span class="sxs-lookup"><span data-stu-id="8d647-309">5 GB</span></span></p></td>
</tr>
</tbody>
</table>



## <a href="" id="---------mbam-client-system-requirements"></a> <span data-ttu-id="8d647-310">MBAM-Client Systemanforderungen</span><span class="sxs-lookup"><span data-stu-id="8d647-310">MBAM Client system requirements</span></span>


### <span data-ttu-id="8d647-311">Client-Betriebssystemanforderungen</span><span class="sxs-lookup"><span data-stu-id="8d647-311">Client operating system requirements</span></span>

<span data-ttu-id="8d647-312">Wir empfehlen dringend, dass Sie den MBAM-Client und den MBAM-Server auf der gleichen Betriebssystem Zeile ausführen.</span><span class="sxs-lookup"><span data-stu-id="8d647-312">We strongly recommend that you run the MBAM Client and MBAM Server on the same line of operating systems.</span></span> <span data-ttu-id="8d647-313">Beispiel: Windows 10 mit Windows Server 2016, Windows 8,1 mit Windows Server 2012 R2 usw.</span><span class="sxs-lookup"><span data-stu-id="8d647-313">For example, Windows 10 with Windows Server 2016, Windows 8.1 with Windows Server 2012 R2, and so on.</span></span>

<span data-ttu-id="8d647-314">In der folgenden Tabelle sind die Betriebssysteme aufgeführt, die für die MBAM-Client Installation unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="8d647-314">The following table lists the operating systems that are supported for MBAM Client installation.</span></span> <span data-ttu-id="8d647-315">Die gleichen Anforderungen gelten für die eigenständige und die Configuration Manager-Integrations Topologie.</span><span class="sxs-lookup"><span data-stu-id="8d647-315">The same requirements apply to the Stand-alone and the Configuration Manager Integration topologies.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="8d647-316">Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="8d647-316">Operating system</span></span></th>
<th align="left"><span data-ttu-id="8d647-317">Edition</span><span class="sxs-lookup"><span data-stu-id="8d647-317">Edition</span></span></th>
<th align="left"><span data-ttu-id="8d647-318">Service Pack</span><span class="sxs-lookup"><span data-stu-id="8d647-318">Service pack</span></span></th>
<th align="left"><span data-ttu-id="8d647-319">System Architektur</span><span class="sxs-lookup"><span data-stu-id="8d647-319">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="even">
    <td align="left"><p><span data-ttu-id="8d647-320">Windows 10-viel</span><span class="sxs-lookup"><span data-stu-id="8d647-320">Windows 10 IoT</span></span></p></td>
    <td align="left"><p><span data-ttu-id="8d647-321">Unternehmen</span><span class="sxs-lookup"><span data-stu-id="8d647-321">Enterprise</span></span></p></td>
    <td align="left"><p></p></td>
    <td align="left"><p><span data-ttu-id="8d647-322">32 Bit oder 64 Bit</span><span class="sxs-lookup"><span data-stu-id="8d647-322">32-bit or 64-bit</span></span></p></td>
</tr><br/><tr class="odd">
<td align="left"><p><span data-ttu-id="8d647-323">Windows 10</span><span class="sxs-lookup"><span data-stu-id="8d647-323">Windows 10</span></span></p></td>
<td align="left"><p><span data-ttu-id="8d647-324">Unternehmen</span><span class="sxs-lookup"><span data-stu-id="8d647-324">Enterprise</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="8d647-325">32 Bit oder 64 Bit</span><span class="sxs-lookup"><span data-stu-id="8d647-325">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8d647-326">Windows8.1</span><span class="sxs-lookup"><span data-stu-id="8d647-326">Windows 8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="8d647-327">Unternehmen</span><span class="sxs-lookup"><span data-stu-id="8d647-327">Enterprise</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="8d647-328">32 Bit oder 64 Bit</span><span class="sxs-lookup"><span data-stu-id="8d647-328">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8d647-329">Windows7</span><span class="sxs-lookup"><span data-stu-id="8d647-329">Windows 7</span></span></p></td>
<td align="left"><p><span data-ttu-id="8d647-330">Enterprise oder Ultimate</span><span class="sxs-lookup"><span data-stu-id="8d647-330">Enterprise or Ultimate</span></span></p></td>
<td align="left"><p><span data-ttu-id="8d647-331">SP1</span><span class="sxs-lookup"><span data-stu-id="8d647-331">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="8d647-332">32 Bit oder 64 Bit</span><span class="sxs-lookup"><span data-stu-id="8d647-332">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8d647-333">Windows To Go</span><span class="sxs-lookup"><span data-stu-id="8d647-333">Windows To Go</span></span></p></td>
<td align="left"><p><span data-ttu-id="8d647-334">Windows 8,1 und Windows 10 Enterprise</span><span class="sxs-lookup"><span data-stu-id="8d647-334">Windows 8.1 and Windows 10 Enterprise</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="8d647-335">32 Bit oder 64 Bit</span><span class="sxs-lookup"><span data-stu-id="8d647-335">32-bit or 64-bit</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="client-ram-requirements-"></a><span data-ttu-id="8d647-336">Client-RAM-Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8d647-336">Client RAM requirements</span></span>

<span data-ttu-id="8d647-337">Für die MBAM-Client Installation gibt es keine spezifischen RAM-Anforderungen.</span><span class="sxs-lookup"><span data-stu-id="8d647-337">There are no RAM requirements that are specific to the MBAM Client installation.</span></span>

## <a href="" id="---------mbam-group-policy-system-requirements"></a> <span data-ttu-id="8d647-338">Systemanforderungen für MBAM-Gruppenrichtlinien</span><span class="sxs-lookup"><span data-stu-id="8d647-338">MBAM Group Policy system requirements</span></span>


<span data-ttu-id="8d647-339">In der folgenden Tabelle sind die Betriebssysteme aufgeführt, die für die Installation von MBAM-Gruppenrichtlinienvorlagen unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="8d647-339">The following table lists the operating systems that are supported for MBAM Group Policy Templates installation.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="8d647-340">Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="8d647-340">Operating system</span></span></th>
<th align="left"><span data-ttu-id="8d647-341">Edition</span><span class="sxs-lookup"><span data-stu-id="8d647-341">Edition</span></span></th>
<th align="left"><span data-ttu-id="8d647-342">Service Pack</span><span class="sxs-lookup"><span data-stu-id="8d647-342">Service pack</span></span></th>
<th align="left"><span data-ttu-id="8d647-343">System Architektur</span><span class="sxs-lookup"><span data-stu-id="8d647-343">System architecture</span></span></th>
</tr>
</thead>
<tbody>
 <tr class="even">
      <td align="left"><p><span data-ttu-id="8d647-344">Windows 10-viel</span><span class="sxs-lookup"><span data-stu-id="8d647-344">Windows 10 IoT</span></span></p></td>
      <td align="left"><p><span data-ttu-id="8d647-345">Unternehmen</span><span class="sxs-lookup"><span data-stu-id="8d647-345">Enterprise</span></span></p></td>
      <td align="left"><p></p></td>
      <td align="left"><p><span data-ttu-id="8d647-346">32 Bit oder 64 Bit</span><span class="sxs-lookup"><span data-stu-id="8d647-346">32-bit or 64-bit</span></span></p></td>
 </tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8d647-347">Windows 10</span><span class="sxs-lookup"><span data-stu-id="8d647-347">Windows 10</span></span></p></td>
<td align="left"><p><span data-ttu-id="8d647-348">Unternehmen</span><span class="sxs-lookup"><span data-stu-id="8d647-348">Enterprise</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="8d647-349">32 Bit oder 64 Bit</span><span class="sxs-lookup"><span data-stu-id="8d647-349">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8d647-350">Windows8.1</span><span class="sxs-lookup"><span data-stu-id="8d647-350">Windows 8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="8d647-351">Unternehmen</span><span class="sxs-lookup"><span data-stu-id="8d647-351">Enterprise</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="8d647-352">32 Bit oder 64 Bit</span><span class="sxs-lookup"><span data-stu-id="8d647-352">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8d647-353">Windows7</span><span class="sxs-lookup"><span data-stu-id="8d647-353">Windows 7</span></span></p></td>
<td align="left"><p><span data-ttu-id="8d647-354">Enterprise oder Ultimate</span><span class="sxs-lookup"><span data-stu-id="8d647-354">Enterprise, or Ultimate</span></span></p></td>
<td align="left"><p><span data-ttu-id="8d647-355">SP1</span><span class="sxs-lookup"><span data-stu-id="8d647-355">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="8d647-356">32 Bit oder 64 Bit</span><span class="sxs-lookup"><span data-stu-id="8d647-356">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8d647-357">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="8d647-357">Windows Server 2012 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="8d647-358">Standard oder Rechenzentrum</span><span class="sxs-lookup"><span data-stu-id="8d647-358">Standard or Datacenter</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="8d647-359">64Bit</span><span class="sxs-lookup"><span data-stu-id="8d647-359">64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8d647-360">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8d647-360">Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="8d647-361">Standard oder Rechenzentrum</span><span class="sxs-lookup"><span data-stu-id="8d647-361">Standard or Datacenter</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="8d647-362">64Bit</span><span class="sxs-lookup"><span data-stu-id="8d647-362">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8d647-363">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8d647-363">Windows Server 2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="8d647-364">Standard, Enterprise oder Datacenter</span><span class="sxs-lookup"><span data-stu-id="8d647-364">Standard, Enterprise, or Datacenter</span></span></p></td>
<td align="left"><p><span data-ttu-id="8d647-365">SP1</span><span class="sxs-lookup"><span data-stu-id="8d647-365">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="8d647-366">64Bit</span><span class="sxs-lookup"><span data-stu-id="8d647-366">64-bit</span></span></p></td>
</tr>
</tbody>
</table>

## <span data-ttu-id="8d647-367">MBAM in Azure IaaS</span><span class="sxs-lookup"><span data-stu-id="8d647-367">MBAM In Azure IaaS</span></span>

<span data-ttu-id="8d647-368">Der MBAM-Server kann in Azure Infrastructure as a Service (IaaS) auf einer der oben aufgeführten unterstützten Betriebssystemversionen bereitgestellt werden, die eine Verbindung mit einem lokal gehosteten Active Directory oder einem Active Directory herstellt, das auch in Azure IaaS gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="8d647-368">The MBAM server can be deployed in Azure Infrastructure as a Service (IaaS) on any of the supported OS versions listed above, connecting to an Active Directory hosted on premises or an Active Directory also hosted in Azure IaaS.</span></span>  <span data-ttu-id="8d647-369">Die Dokumentation zum Einrichten und Konfigurieren von Active Directory auf Azure IaaS finden Sie [hier](https://msdn.microsoft.com/library/azure/jj156090.aspx).</span><span class="sxs-lookup"><span data-stu-id="8d647-369">Documentation for setting up and configuring Active Directory on Azure IaaS is [here](https://msdn.microsoft.com/library/azure/jj156090.aspx).</span></span>

<span data-ttu-id="8d647-370">Der MBAM-Client wird auf virtuellen Computern nicht unterstützt und auch auf Azure IaaS nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8d647-370">The MBAM client is not supported on virtual machines and is also not supported on Azure IaaS.</span></span>


## <span data-ttu-id="8d647-371">Dienstversionen</span><span class="sxs-lookup"><span data-stu-id="8d647-371">Service releases</span></span> 

- [<span data-ttu-id="8d647-372">Hotfix für April 2016</span><span class="sxs-lookup"><span data-stu-id="8d647-372">April 2016 hotfix</span></span>](https://support.microsoft.com/help/3144445/april-2016-hotfix-rollup-for-microsoft-desktop-optimization-pack)
- [<span data-ttu-id="8d647-373">September 2016</span><span class="sxs-lookup"><span data-stu-id="8d647-373">September 2016</span></span>](https://support.microsoft.com/ms-my/help/3168628/september-2016-servicing-release-for-microsoft-desktop-optimization-pa)
- [<span data-ttu-id="8d647-374">Dezember 2016</span><span class="sxs-lookup"><span data-stu-id="8d647-374">December 2016</span></span>](https://support.microsoft.com/help/3198158/december-2016-servicing-release-for-microsoft-desktop-optimization-pac)
- [<span data-ttu-id="8d647-375">März 2017</span><span class="sxs-lookup"><span data-stu-id="8d647-375">March 2017</span></span>](https://support.microsoft.com/en-ie/help/4014009/march-2017-servicing-release-for-microsoft-desktop-optimization-pack) 
- [<span data-ttu-id="8d647-376">Juni 2017</span><span class="sxs-lookup"><span data-stu-id="8d647-376">June 2017</span></span>](https://support.microsoft.com/af-za/help/4018510/june-2017-servicing-release-for-microsoft-desktop-optimization-pack)
- [<span data-ttu-id="8d647-377">September2017</span><span class="sxs-lookup"><span data-stu-id="8d647-377">September 2017</span></span>](https://support.microsoft.com/en-ie/help/4041137/september-2017-servicing-release-for-microsoft-desktop-optimization)
- [<span data-ttu-id="8d647-378">März 2018</span><span class="sxs-lookup"><span data-stu-id="8d647-378">March 2018</span></span>](https://support.microsoft.com/help/4074878/march-2018-servicing-release-for-microsoft-desktop-optimization-pack)
- [<span data-ttu-id="8d647-379">Juli 2018</span><span class="sxs-lookup"><span data-stu-id="8d647-379">July 2018</span></span>](https://support.microsoft.com/help/4340040/july-2018-servicing-release-for-microsoft-desktop-optimization-pack)
- [<span data-ttu-id="8d647-380">Mai 2019</span><span class="sxs-lookup"><span data-stu-id="8d647-380">May 2019</span></span>](https://support.microsoft.com/help/4505175/may-2019-servicing-release-for-microsoft-desktop-optimization-pack)

## <span data-ttu-id="8d647-381">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="8d647-381">Related topics</span></span>


[<span data-ttu-id="8d647-382">Planen der Bereitstellung von MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="8d647-382">Planning to Deploy MBAM 2.5</span></span>](planning-to-deploy-mbam-25.md)

[<span data-ttu-id="8d647-383">Vorbereiten der Umgebung für MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="8d647-383">Preparing your Environment for MBAM 2.5</span></span>](preparing-your-environment-for-mbam-25.md)




## <span data-ttu-id="8d647-384">Sie haben einen Vorschlag für MBAM?</span><span class="sxs-lookup"><span data-stu-id="8d647-384">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="8d647-385">[Hier](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)können Sie Vorschläge hinzufügen oder abstimmen.</span><span class="sxs-lookup"><span data-stu-id="8d647-385">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="8d647-386">Bei MBAM-Problemen verwenden Sie das [MBAM TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="8d647-386">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>




