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
ms.openlocfilehash: 8ed7915e33c5e4735a7c58674ed5f7d6da8e9a06
ms.sourcegitcommit: 9087f0a1b5bd3f81a9b790d5e39fdf39c18a2411
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/23/2020
ms.locfileid: "11182927"
---
# <span data-ttu-id="2efd5-103">Von MBAM 2.5 unterstützte Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="2efd5-103">MBAM 2.5 Supported Configurations</span></span>


<span data-ttu-id="2efd5-104">Sie können die Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) 2,5 in einer eigenständigen Topologie oder in einer Configuration Manager-Integrations Topologie ausführen, die MBAM in den System Center Configuration Manager integriert.</span><span class="sxs-lookup"><span data-stu-id="2efd5-104">You can run Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 in a Stand-alone topology or in a Configuration Manager Integration topology that integrates MBAM with System Center Configuration Manager.</span></span> <span data-ttu-id="2efd5-105">Wenn Sie die empfohlene Konfiguration für beide Topologien in einer Produktionsumgebung verwenden, unterstützt MBAM bis zu 500.000 MBAM-Clients.</span><span class="sxs-lookup"><span data-stu-id="2efd5-105">If you use the recommended configuration for either topology in a production environment, MBAM supports up to 500,000 MBAM clients.</span></span> <span data-ttu-id="2efd5-106">Informationen zu den empfohlenen Architekturen und Features, die auf den einzelnen Servern für die einzelnen Topologien konfiguriert sind, finden Sie unter [Architektur auf höherer Ebene für MBAM 2,5](high-level-architecture-for-mbam-25.md).</span><span class="sxs-lookup"><span data-stu-id="2efd5-106">For information about the recommended architecture and features that are configured on each server for each topology, see [High-Level Architecture for MBAM 2.5](high-level-architecture-for-mbam-25.md).</span></span>

<span data-ttu-id="2efd5-107">Weitere Konfigurationen, die speziell für die Configuration Manager-Integrations Topologie gelten, finden Sie unter [unterstützte Configuration Manager-Versionen von MBAM](#bkmk-cm-ramreqs).</span><span class="sxs-lookup"><span data-stu-id="2efd5-107">For additional configurations that are specific to the Configuration Manager Integration topology, see [Versions of Configuration Manager that MBAM supports](#bkmk-cm-ramreqs).</span></span>

**<span data-ttu-id="2efd5-108">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="2efd5-108">Note</span></span>**  
<span data-ttu-id="2efd5-109">Microsoft bietet Unterstützung für das aktuelle Service Pack und in einigen Fällen das unmittelbar vorhergehende Service Pack.</span><span class="sxs-lookup"><span data-stu-id="2efd5-109">Microsoft provides support for the current service pack and, in some cases, the immediately preceding service pack.</span></span> <span data-ttu-id="2efd5-110">Informationen zu den Support Zeitachsen für Ihr Produkt finden Sie unter [unterstützte Service Packs für Lebenszyklen](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span><span class="sxs-lookup"><span data-stu-id="2efd5-110">To find the support timelines for your product, see the [Lifecycle Supported Service Packs](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span></span> <span data-ttu-id="2efd5-111">Weitere Informationen zur Microsoft Support Lifecycle-Richtlinie finden Sie in den [FAQ zu Microsoft Support Lifecycle Support Policy](https://go.microsoft.com/fwlink/p/?LinkId=31976).</span><span class="sxs-lookup"><span data-stu-id="2efd5-111">For additional information about Microsoft Support Lifecycle Policy, see [Microsoft Support Lifecycle Support Policy FAQ](https://go.microsoft.com/fwlink/p/?LinkId=31976).</span></span>



## <span data-ttu-id="2efd5-112">MBAM unterstützte Sprachen</span><span class="sxs-lookup"><span data-stu-id="2efd5-112">MBAM Supported Languages</span></span>


<span data-ttu-id="2efd5-113">In den folgenden Tabellen werden die Sprachen aufgeführt, die für den MBAM-Client (einschließlich des Self-Service-Portals) und den MBAM-Server in MBAM 2,5 und MBAM 2,5 SP1 unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="2efd5-113">The following tables show the languages that are supported for the MBAM Client (including the Self-Service Portal) and the MBAM Server in MBAM 2.5 and MBAM 2.5 SP1.</span></span>

**<span data-ttu-id="2efd5-114">Unterstützte Sprachen in MBAM 2,5 SP1:</span><span class="sxs-lookup"><span data-stu-id="2efd5-114">Supported Languages in MBAM 2.5 SP1:</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="2efd5-115">Client Sprachen</span><span class="sxs-lookup"><span data-stu-id="2efd5-115">Client Languages</span></span></th>
<th align="left"><span data-ttu-id="2efd5-116">Server Sprachen</span><span class="sxs-lookup"><span data-stu-id="2efd5-116">Server Languages</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2efd5-117">Tschechische Republik (Tschechien) cs-cz</span><span class="sxs-lookup"><span data-stu-id="2efd5-117">Czech (Czech Republic) cs-CZ</span></span></p>
<p><span data-ttu-id="2efd5-118">Dänisch (Dänemark) da-DK</span><span class="sxs-lookup"><span data-stu-id="2efd5-118">Danish (Denmark) da-DK</span></span></p>
<p><span data-ttu-id="2efd5-119">Niederländisch (Niederlande) nl-nl</span><span class="sxs-lookup"><span data-stu-id="2efd5-119">Dutch (Netherlands) nl-NL</span></span></p>
<p><span data-ttu-id="2efd5-120">Englisch (USA) en-US</span><span class="sxs-lookup"><span data-stu-id="2efd5-120">English (United States) en-US</span></span></p>
<p><span data-ttu-id="2efd5-121">Finnisch (Finnland) fi-fi</span><span class="sxs-lookup"><span data-stu-id="2efd5-121">Finnish (Finland) fi-FI</span></span></p>
<p><span data-ttu-id="2efd5-122">Französisch (Frankreich) fr-FR</span><span class="sxs-lookup"><span data-stu-id="2efd5-122">French (France) fr-FR</span></span></p>
<p><span data-ttu-id="2efd5-123">Deutsch (Deutschland) de-de</span><span class="sxs-lookup"><span data-stu-id="2efd5-123">German (Germany) de-DE</span></span></p>
<p><span data-ttu-id="2efd5-124">Griechisch (Griechenland) el-gr</span><span class="sxs-lookup"><span data-stu-id="2efd5-124">Greek (Greece) el-GR</span></span></p>
<p><span data-ttu-id="2efd5-125">Ungarisch (Ungarn) hu-hu</span><span class="sxs-lookup"><span data-stu-id="2efd5-125">Hungarian (Hungary) hu-HU</span></span></p>
<p><span data-ttu-id="2efd5-126">Italienisch (Italien) IT-IT</span><span class="sxs-lookup"><span data-stu-id="2efd5-126">Italian (Italy) it-IT</span></span></p>
<p><span data-ttu-id="2efd5-127">Japanisch (Japan) ja-JP</span><span class="sxs-lookup"><span data-stu-id="2efd5-127">Japanese (Japan) ja-JP</span></span></p>
<p><span data-ttu-id="2efd5-128">Koreanisch (Korea) ko-kr</span><span class="sxs-lookup"><span data-stu-id="2efd5-128">Korean (Korea) ko-KR</span></span></p>
<p><span data-ttu-id="2efd5-129">Norwegisch, Nynorsk (Norwegen) NB-Nein</span><span class="sxs-lookup"><span data-stu-id="2efd5-129">Norwegian, Bokmål (Norway) nb-NO</span></span></p>
<p><span data-ttu-id="2efd5-130">Polnisch (Polen) pl-pl</span><span class="sxs-lookup"><span data-stu-id="2efd5-130">Polish (Poland) pl-PL</span></span></p>
<p><span data-ttu-id="2efd5-131">Portugiesisch (Brasilien) pt-br</span><span class="sxs-lookup"><span data-stu-id="2efd5-131">Portuguese (Brazil) pt-BR</span></span></p>
<p><span data-ttu-id="2efd5-132">Portugiesisch (Portugal) pt-pt</span><span class="sxs-lookup"><span data-stu-id="2efd5-132">Portuguese (Portugal) pt-PT</span></span></p>
<p><span data-ttu-id="2efd5-133">Russisch (Russland) ru-ru</span><span class="sxs-lookup"><span data-stu-id="2efd5-133">Russian (Russia) ru-RU</span></span></p>
<p><span data-ttu-id="2efd5-134">Slowakisch (Slowakei) sk-SK</span><span class="sxs-lookup"><span data-stu-id="2efd5-134">Slovak (Slovakia) sk-SK</span></span></p>
<p><span data-ttu-id="2efd5-135">Spanisch (Spanien) es-es</span><span class="sxs-lookup"><span data-stu-id="2efd5-135">Spanish (Spain) es-ES</span></span></p>
<p><span data-ttu-id="2efd5-136">SV-SE für Schwedisch (Schweden)</span><span class="sxs-lookup"><span data-stu-id="2efd5-136">Swedish (Sweden) sv-SE</span></span></p>
<p><span data-ttu-id="2efd5-137">Türkisch (Türkei) tr-TR</span><span class="sxs-lookup"><span data-stu-id="2efd5-137">Turkish (Turkey) tr-TR</span></span></p>
<p><span data-ttu-id="2efd5-138">Slowenisch (Slowenien) SL-SI</span><span class="sxs-lookup"><span data-stu-id="2efd5-138">Slovenian (Slovenia) sl-SI</span></span></p>
<p><span data-ttu-id="2efd5-139">Vereinfachtes Chinesisch (VR China) zh-cn</span><span class="sxs-lookup"><span data-stu-id="2efd5-139">Simplified Chinese (PRC) zh-CN</span></span></p>
<p><span data-ttu-id="2efd5-140">Traditionelles Chinesisch (Taiwan) zh-tw</span><span class="sxs-lookup"><span data-stu-id="2efd5-140">Traditional Chinese (Taiwan) zh-TW</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="2efd5-141">Englisch (USA) en-US</span><span class="sxs-lookup"><span data-stu-id="2efd5-141">English (United States) en-US</span></span></p></li>
<li><p><span data-ttu-id="2efd5-142">Französisch (Frankreich) fr-FR</span><span class="sxs-lookup"><span data-stu-id="2efd5-142">French (France) fr-FR</span></span></p></li>
<li><p><span data-ttu-id="2efd5-143">Deutsch (Deutschland) de-de</span><span class="sxs-lookup"><span data-stu-id="2efd5-143">German (Germany) de-DE</span></span></p></li>
<li><p><span data-ttu-id="2efd5-144">Italienisch (Italien) IT-IT</span><span class="sxs-lookup"><span data-stu-id="2efd5-144">Italian (Italy) it-IT</span></span></p></li>
<li><p><span data-ttu-id="2efd5-145">Japanisch (Japan) ja-JP</span><span class="sxs-lookup"><span data-stu-id="2efd5-145">Japanese (Japan) ja-JP</span></span></p></li>
<li><p><span data-ttu-id="2efd5-146">Koreanisch (Korea) ko-kr</span><span class="sxs-lookup"><span data-stu-id="2efd5-146">Korean (Korea) ko-KR</span></span></p></li>
<li><p><span data-ttu-id="2efd5-147">Portugiesisch (Brasilien) pt-br</span><span class="sxs-lookup"><span data-stu-id="2efd5-147">Portuguese (Brazil) pt-BR</span></span></p></li>
<li><p><span data-ttu-id="2efd5-148">Russisch (Russland) ru-ru</span><span class="sxs-lookup"><span data-stu-id="2efd5-148">Russian (Russia) ru-RU</span></span></p></li>
<li><p><span data-ttu-id="2efd5-149">Spanisch (Spanien) es-es</span><span class="sxs-lookup"><span data-stu-id="2efd5-149">Spanish (Spain) es-ES</span></span></p></li>
<li><p><span data-ttu-id="2efd5-150">Vereinfachtes Chinesisch (VR China) zh-cn</span><span class="sxs-lookup"><span data-stu-id="2efd5-150">Simplified Chinese (PRC) zh-CN</span></span></p></li>
<li><p><span data-ttu-id="2efd5-151">Traditionelles Chinesisch (Taiwan) zh-tw</span><span class="sxs-lookup"><span data-stu-id="2efd5-151">Traditional Chinese (Taiwan) zh-TW</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="2efd5-152">Unterstützte Sprachen in MBAM 2,5:</span><span class="sxs-lookup"><span data-stu-id="2efd5-152">Supported Languages in MBAM 2.5:</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="2efd5-153">Client Sprachen</span><span class="sxs-lookup"><span data-stu-id="2efd5-153">Client Languages</span></span></th>
<th align="left"><span data-ttu-id="2efd5-154">Server Sprachen</span><span class="sxs-lookup"><span data-stu-id="2efd5-154">Server Languages</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><ul>
<li><p><span data-ttu-id="2efd5-155">Englisch (USA) en-US</span><span class="sxs-lookup"><span data-stu-id="2efd5-155">English (United States) en-US</span></span></p></li>
<li><p><span data-ttu-id="2efd5-156">Französisch (Frankreich) fr-FR</span><span class="sxs-lookup"><span data-stu-id="2efd5-156">French (France) fr-FR</span></span></p></li>
<li><p><span data-ttu-id="2efd5-157">Deutsch (Deutschland) de-de</span><span class="sxs-lookup"><span data-stu-id="2efd5-157">German (Germany) de-DE</span></span></p></li>
<li><p><span data-ttu-id="2efd5-158">Italienisch (Italien) IT-IT</span><span class="sxs-lookup"><span data-stu-id="2efd5-158">Italian (Italy) it-IT</span></span></p></li>
<li><p><span data-ttu-id="2efd5-159">Japanisch (Japan) ja-JP</span><span class="sxs-lookup"><span data-stu-id="2efd5-159">Japanese (Japan) ja-JP</span></span></p></li>
<li><p><span data-ttu-id="2efd5-160">Koreanisch (Korea) ko-kr</span><span class="sxs-lookup"><span data-stu-id="2efd5-160">Korean (Korea) ko-KR</span></span></p></li>
<li><p><span data-ttu-id="2efd5-161">Portugiesisch (Brasilien) pt-br</span><span class="sxs-lookup"><span data-stu-id="2efd5-161">Portuguese (Brazil) pt-BR</span></span></p></li>
<li><p><span data-ttu-id="2efd5-162">Russisch (Russland) ru-ru</span><span class="sxs-lookup"><span data-stu-id="2efd5-162">Russian (Russia) ru-RU</span></span></p></li>
<li><p><span data-ttu-id="2efd5-163">Spanisch (Spanien) es-es</span><span class="sxs-lookup"><span data-stu-id="2efd5-163">Spanish (Spain) es-ES</span></span></p></li>
<li><p><span data-ttu-id="2efd5-164">Vereinfachtes Chinesisch (VR China) zh-cn</span><span class="sxs-lookup"><span data-stu-id="2efd5-164">Simplified Chinese (PRC) zh-CN</span></span></p></li>
<li><p><span data-ttu-id="2efd5-165">Traditionelles Chinesisch (Taiwan) zh-tw</span><span class="sxs-lookup"><span data-stu-id="2efd5-165">Traditional Chinese (Taiwan) zh-TW</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="2efd5-166">Englisch (USA) en-US</span><span class="sxs-lookup"><span data-stu-id="2efd5-166">English (United States) en-US</span></span></p></li>
<li><p><span data-ttu-id="2efd5-167">Französisch (Frankreich) fr-FR</span><span class="sxs-lookup"><span data-stu-id="2efd5-167">French (France) fr-FR</span></span></p></li>
<li><p><span data-ttu-id="2efd5-168">Deutsch (Deutschland) de-de</span><span class="sxs-lookup"><span data-stu-id="2efd5-168">German (Germany) de-DE</span></span></p></li>
<li><p><span data-ttu-id="2efd5-169">Italienisch (Italien) IT-IT</span><span class="sxs-lookup"><span data-stu-id="2efd5-169">Italian (Italy) it-IT</span></span></p></li>
<li><p><span data-ttu-id="2efd5-170">Japanisch (Japan) ja-JP</span><span class="sxs-lookup"><span data-stu-id="2efd5-170">Japanese (Japan) ja-JP</span></span></p></li>
<li><p><span data-ttu-id="2efd5-171">Koreanisch (Korea) ko-kr</span><span class="sxs-lookup"><span data-stu-id="2efd5-171">Korean (Korea) ko-KR</span></span></p></li>
<li><p><span data-ttu-id="2efd5-172">Portugiesisch (Brasilien) pt-br</span><span class="sxs-lookup"><span data-stu-id="2efd5-172">Portuguese (Brazil) pt-BR</span></span></p></li>
<li><p><span data-ttu-id="2efd5-173">Russisch (Russland) ru-ru</span><span class="sxs-lookup"><span data-stu-id="2efd5-173">Russian (Russia) ru-RU</span></span></p></li>
<li><p><span data-ttu-id="2efd5-174">Spanisch (Spanien) es-es</span><span class="sxs-lookup"><span data-stu-id="2efd5-174">Spanish (Spain) es-ES</span></span></p></li>
<li><p><span data-ttu-id="2efd5-175">Vereinfachtes Chinesisch (VR China) zh-cn</span><span class="sxs-lookup"><span data-stu-id="2efd5-175">Simplified Chinese (PRC) zh-CN</span></span></p></li>
<li><p><span data-ttu-id="2efd5-176">Traditionelles Chinesisch (Taiwan) zh-tw</span><span class="sxs-lookup"><span data-stu-id="2efd5-176">Traditional Chinese (Taiwan) zh-TW</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>



## <a href="" id="---------mbam-server-system-requirements"></a> <span data-ttu-id="2efd5-177">Systemanforderungen für MBAM-Server</span><span class="sxs-lookup"><span data-stu-id="2efd5-177">MBAM Server system requirements</span></span>


### <span data-ttu-id="2efd5-178">MBAM Server-Betriebssystemanforderungen</span><span class="sxs-lookup"><span data-stu-id="2efd5-178">MBAM Server operating system requirements</span></span>

<span data-ttu-id="2efd5-179">Wir empfehlen dringend, dass Sie den MBAM-Client und den MBAM-Server auf der gleichen Betriebssystem Zeile ausführen.</span><span class="sxs-lookup"><span data-stu-id="2efd5-179">We strongly recommend that you run the MBAM Client and MBAM Server on the same line of operating systems.</span></span> <span data-ttu-id="2efd5-180">Beispiel: Windows 10 mit Windows Server 2016, Windows 8,1 mit Windows Server 2012 R2 usw.</span><span class="sxs-lookup"><span data-stu-id="2efd5-180">For example, Windows 10 with Windows Server 2016, Windows 8.1 with Windows Server 2012 R2, and so on.</span></span>

<span data-ttu-id="2efd5-181">In der folgenden Tabelle sind die Betriebssysteme aufgeführt, die für die Installation des MBAM-Servers unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="2efd5-181">The following table lists the operating systems that are supported for the MBAM Server installation.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="2efd5-182">Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="2efd5-182">Operating system</span></span></th>
<th align="left"><span data-ttu-id="2efd5-183">Edition</span><span class="sxs-lookup"><span data-stu-id="2efd5-183">Edition</span></span></th>
<th align="left"><span data-ttu-id="2efd5-184">Service Pack</span><span class="sxs-lookup"><span data-stu-id="2efd5-184">Service pack</span></span></th>
<th align="left"><span data-ttu-id="2efd5-185">System Architektur</span><span class="sxs-lookup"><span data-stu-id="2efd5-185">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2efd5-186">Windows Server 2019</span><span class="sxs-lookup"><span data-stu-id="2efd5-186">Windows Server 2019</span></span></p></td>
<td align="left"><p><span data-ttu-id="2efd5-187">Standard oder Rechenzentrum</span><span class="sxs-lookup"><span data-stu-id="2efd5-187">Standard or Datacenter</span></span></p></td>
<td align="left"></td>
<td align="left"><p><span data-ttu-id="2efd5-188">64Bit</span><span class="sxs-lookup"><span data-stu-id="2efd5-188">64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2efd5-189">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="2efd5-189">Windows Server 2016</span></span></p></td>
<td align="left"><p><span data-ttu-id="2efd5-190">Standard oder Rechenzentrum</span><span class="sxs-lookup"><span data-stu-id="2efd5-190">Standard or Datacenter</span></span></p></td>
<td align="left"></td>
<td align="left"><p><span data-ttu-id="2efd5-191">64Bit</span><span class="sxs-lookup"><span data-stu-id="2efd5-191">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2efd5-192">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="2efd5-192">Windows Server 2012 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="2efd5-193">Standard oder Rechenzentrum</span><span class="sxs-lookup"><span data-stu-id="2efd5-193">Standard or Datacenter</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="2efd5-194">64Bit</span><span class="sxs-lookup"><span data-stu-id="2efd5-194">64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2efd5-195">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2efd5-195">Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="2efd5-196">Standard oder Rechenzentrum</span><span class="sxs-lookup"><span data-stu-id="2efd5-196">Standard or Datacenter</span></span></p></td>
<td align="left"></td>
<td align="left"><p><span data-ttu-id="2efd5-197">64Bit</span><span class="sxs-lookup"><span data-stu-id="2efd5-197">64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2efd5-198">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="2efd5-198">Windows Server 2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="2efd5-199">Standard, Enterprise oder Datacenter</span><span class="sxs-lookup"><span data-stu-id="2efd5-199">Standard, Enterprise, or Datacenter</span></span></p></td>
<td align="left"><p><span data-ttu-id="2efd5-200">SP1</span><span class="sxs-lookup"><span data-stu-id="2efd5-200">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="2efd5-201">64Bit</span><span class="sxs-lookup"><span data-stu-id="2efd5-201">64-bit</span></span></p></td>
</tr>
</tbody>
</table>



<span data-ttu-id="2efd5-202">Die Unternehmensdomäne muss mindestens einen Windows Server 2008-Domänencontroller (oder höher) enthalten.</span><span class="sxs-lookup"><span data-stu-id="2efd5-202">The enterprise domain must contain at least one Windows Server 2008 (or later) domain controller.</span></span>

### <a href="" id="bkmk-stand-alone-ramreqs"></a><span data-ttu-id="2efd5-203">MBAM-Server Prozessor, RAM und Speicherplatzanforderungen – eigenständige Topologie</span><span class="sxs-lookup"><span data-stu-id="2efd5-203">MBAM Server processor, RAM, and disk space requirements – Stand-alone topology</span></span>

<span data-ttu-id="2efd5-204">Diese Anforderungen gelten für die eigenständige MBAM-Topologie.</span><span class="sxs-lookup"><span data-stu-id="2efd5-204">These requirements are for the MBAM Stand-alone topology.</span></span> <span data-ttu-id="2efd5-205">Die Anforderungen für die Configuration Manager-Integrations Topologie finden Sie unter [MBAM-Server Prozessor, RAM und Speicherplatzanforderungen – Configuration Manager-Integrations Topologie](#bkmk-cm-ramreqs).</span><span class="sxs-lookup"><span data-stu-id="2efd5-205">For the requirements for the Configuration Manager Integration topology, see [MBAM Server Processor, RAM, and Disk Space Requirements - Configuration Manager Integration Topology](#bkmk-cm-ramreqs).</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="2efd5-206">Hardware Element</span><span class="sxs-lookup"><span data-stu-id="2efd5-206">Hardware item</span></span></th>
<th align="left"><span data-ttu-id="2efd5-207">Mindestanforderungen</span><span class="sxs-lookup"><span data-stu-id="2efd5-207">Minimum requirement</span></span></th>
<th align="left"><span data-ttu-id="2efd5-208">Empfohlene Anforderung</span><span class="sxs-lookup"><span data-stu-id="2efd5-208">Recommended requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2efd5-209">Prozessor</span><span class="sxs-lookup"><span data-stu-id="2efd5-209">Processor</span></span></p></td>
<td align="left"><p><span data-ttu-id="2efd5-210">2,33 GHz</span><span class="sxs-lookup"><span data-stu-id="2efd5-210">2.33 GHz</span></span></p></td>
<td align="left"><p><span data-ttu-id="2efd5-211">2,33 GHz oder höher</span><span class="sxs-lookup"><span data-stu-id="2efd5-211">2.33 GHz or greater</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2efd5-212">RAM</span><span class="sxs-lookup"><span data-stu-id="2efd5-212">RAM</span></span></p></td>
<td align="left"><p><span data-ttu-id="2efd5-213">8 GB</span><span class="sxs-lookup"><span data-stu-id="2efd5-213">8 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="2efd5-214">12 GB</span><span class="sxs-lookup"><span data-stu-id="2efd5-214">12 GB</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2efd5-215">Freier Speicherplatz</span><span class="sxs-lookup"><span data-stu-id="2efd5-215">Free disk space</span></span></p></td>
<td align="left"><p><span data-ttu-id="2efd5-216">1 GB</span><span class="sxs-lookup"><span data-stu-id="2efd5-216">1 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="2efd5-217">2 GB</span><span class="sxs-lookup"><span data-stu-id="2efd5-217">2 GB</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-cm-ramreqs"></a><span data-ttu-id="2efd5-218">MBAM-Server Prozessor, RAM und Speicherplatzanforderungen – Configuration Manager-Integrations Topologie</span><span class="sxs-lookup"><span data-stu-id="2efd5-218">MBAM Server processor, RAM, and disk space requirements - Configuration Manager Integration topology</span></span>

<span data-ttu-id="2efd5-219">In der folgenden Tabelle sind die Server Prozessor-, RAM-und Speicherplatzanforderungen für MBAM-Server aufgelistet, wenn Sie die Configuration Manager-Integrations Topologie verwenden.</span><span class="sxs-lookup"><span data-stu-id="2efd5-219">The following table lists the server processor, RAM, and disk space requirements for MBAM servers when you are using the Configuration Manager Integration topology.</span></span> <span data-ttu-id="2efd5-220">Die Anforderungen für die eigenständige Topologie finden Sie unter [MBAM-Server Prozessor, RAM und Speicherplatzanforderungen – eigenständige Topologie](#bkmk-stand-alone-ramreqs).</span><span class="sxs-lookup"><span data-stu-id="2efd5-220">For the requirements for the Stand-alone topology, see [MBAM Server Processor, RAM, and Disk Space Requirements – Stand-alone Topology](#bkmk-stand-alone-ramreqs).</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="2efd5-221">Hardware Element</span><span class="sxs-lookup"><span data-stu-id="2efd5-221">Hardware item</span></span></th>
<th align="left"><span data-ttu-id="2efd5-222">Mindestanforderungen</span><span class="sxs-lookup"><span data-stu-id="2efd5-222">Minimum requirement</span></span></th>
<th align="left"><span data-ttu-id="2efd5-223">Empfohlene Anforderung</span><span class="sxs-lookup"><span data-stu-id="2efd5-223">Recommended requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2efd5-224">Prozessor</span><span class="sxs-lookup"><span data-stu-id="2efd5-224">Processor</span></span></p></td>
<td align="left"><p><span data-ttu-id="2efd5-225">2,33 GHz</span><span class="sxs-lookup"><span data-stu-id="2efd5-225">2.33 GHz</span></span></p></td>
<td align="left"><p><span data-ttu-id="2efd5-226">2,33 GHz oder höher</span><span class="sxs-lookup"><span data-stu-id="2efd5-226">2.33 GHz or greater</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2efd5-227">RAM</span><span class="sxs-lookup"><span data-stu-id="2efd5-227">RAM</span></span></p></td>
<td align="left"><p><span data-ttu-id="2efd5-228">4 GB</span><span class="sxs-lookup"><span data-stu-id="2efd5-228">4 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="2efd5-229">8 GB</span><span class="sxs-lookup"><span data-stu-id="2efd5-229">8 GB</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2efd5-230">Freier Speicherplatz</span><span class="sxs-lookup"><span data-stu-id="2efd5-230">Free disk space</span></span></p></td>
<td align="left"><p><span data-ttu-id="2efd5-231">1 GB</span><span class="sxs-lookup"><span data-stu-id="2efd5-231">1 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="2efd5-232">2 GB</span><span class="sxs-lookup"><span data-stu-id="2efd5-232">2 GB</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-cmversions"></a><span data-ttu-id="2efd5-233">Von MBAM unterstützte Versionen von Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="2efd5-233">Versions of Configuration Manager that MBAM supports</span></span>

<span data-ttu-id="2efd5-234">MBAM unterstützt die folgenden Versionen von Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="2efd5-234">MBAM supports the following versions of Configuration Manager.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="2efd5-235">Unterstützte Version</span><span class="sxs-lookup"><span data-stu-id="2efd5-235">Supported version</span></span></th>
<th align="left"><span data-ttu-id="2efd5-236">Service Pack</span><span class="sxs-lookup"><span data-stu-id="2efd5-236">Service pack</span></span></th>
<th align="left"><span data-ttu-id="2efd5-237">System Architektur</span><span class="sxs-lookup"><span data-stu-id="2efd5-237">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="even">
<td align="left"><p><span data-ttu-id="2efd5-238">Microsoft System Center Configuration Manager (aktueller Zweig), Versionen bis zu 1902</span><span class="sxs-lookup"><span data-stu-id="2efd5-238">Microsoft System Center Configuration Manager (Current Branch), versions up to 1902</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="2efd5-239">64Bit</span><span class="sxs-lookup"><span data-stu-id="2efd5-239">64-bit</span></span></p></td>
</tr>

<tr class="odd">
<td align="left"><p><span data-ttu-id="2efd5-240">Microsoft System Center Configuration Manager 1806</span><span class="sxs-lookup"><span data-stu-id="2efd5-240">Microsoft System Center Configuration Manager 1806</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="2efd5-241">64Bit</span><span class="sxs-lookup"><span data-stu-id="2efd5-241">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2efd5-242">Microsoft System Center Configuration Manager (LTSB-Version 1606)</span><span class="sxs-lookup"><span data-stu-id="2efd5-242">Microsoft System Center Configuration Manager (LTSB - version 1606)</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="2efd5-243">64Bit</span><span class="sxs-lookup"><span data-stu-id="2efd5-243">64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2efd5-244">Microsoft System Center 2012-Konfigurations-Manager</span><span class="sxs-lookup"><span data-stu-id="2efd5-244">Microsoft System Center 2012 Configuration Manager</span></span></p></td>
<td align="left"><p><span data-ttu-id="2efd5-245">SP1</span><span class="sxs-lookup"><span data-stu-id="2efd5-245">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="2efd5-246">64Bit</span><span class="sxs-lookup"><span data-stu-id="2efd5-246">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2efd5-247">Microsoft System Center Configuration Manager 2007 R2 oder höher</span><span class="sxs-lookup"><span data-stu-id="2efd5-247">Microsoft System Center Configuration Manager 2007 R2 or later</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="2efd5-248">64Bit</span><span class="sxs-lookup"><span data-stu-id="2efd5-248">64-bit</span></span></p>

<span data-ttu-id="2efd5-249">&gt;<strong>Hinweis </strong> Obwohl Configuration Manager 2007 R2 32-Bit ist, müssen Sie es und SQL Server auf einem 64-Bit-Betriebssystem installieren, um der 64-Bit-MBAM-Software entsprechen zu können.</span><span class="sxs-lookup"><span data-stu-id="2efd5-249">&gt;<strong>Note</strong> Although Configuration Manager 2007 R2 is 32 bit, you must install it and SQL Server on a 64-bit operating system in order to match the 64-bit MBAM software.</span></span>
</td>
</tr>
</tbody>
</table>



<span data-ttu-id="2efd5-250">Eine Liste der unterstützten Konfigurationen für den Configuration Manager-Server finden Sie in der entsprechenden TechNet-Dokumentation für die Version von Configuration Manager, die Sie verwenden.</span><span class="sxs-lookup"><span data-stu-id="2efd5-250">For a list of supported configurations for the Configuration Manager Server, see the appropriate TechNet documentation for the version of Configuration Manager that you are using.</span></span> <span data-ttu-id="2efd5-251">MBAM hat keine zusätzlichen Systemanforderungen für den Configuration Manager-Server.</span><span class="sxs-lookup"><span data-stu-id="2efd5-251">MBAM has no additional system requirements for the Configuration Manager Server.</span></span>

### <a href="" id="sql-server-database-requirements-"></a><span data-ttu-id="2efd5-252">SQL Server-Datenbankanforderungen</span><span class="sxs-lookup"><span data-stu-id="2efd5-252">SQL Server database requirements</span></span>

<span data-ttu-id="2efd5-253">In der folgenden Tabelle sind die Microsoft SQL Server-Versionen aufgeführt, die für die MBAM-Server Features unterstützt werden, einschließlich der Datenbank für die Wiederherstellungsdatenbank, der Kompatibilitäts-und Überwachungsdatenbank sowie des Berichtsfeatures.</span><span class="sxs-lookup"><span data-stu-id="2efd5-253">The following table lists the Microsoft SQL Server versions that are supported for the MBAM Server features, which include the Recovery Database, Compliance and Audit Database, and the Reports feature.</span></span> <span data-ttu-id="2efd5-254">Die erforderlichen Versionen gelten für die eigenständige oder die Configuration Manager-Integrations Topologie.</span><span class="sxs-lookup"><span data-stu-id="2efd5-254">The required versions apply to the Stand-alone or the Configuration Manager Integration topologies.</span></span>

<span data-ttu-id="2efd5-255">Sie müssen SQL Server mit dem **SQL \ _Latin1 \ _General \ _CP1 \ _ci \ _AS** Sortierreihenfolge installieren.</span><span class="sxs-lookup"><span data-stu-id="2efd5-255">You must install SQL Server with the **SQL\_Latin1\_General\_CP1\_CI\_AS** collation.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="2efd5-256">SQL Server-Version</span><span class="sxs-lookup"><span data-stu-id="2efd5-256">SQL Server version</span></span></th>
<th align="left"><span data-ttu-id="2efd5-257">Edition</span><span class="sxs-lookup"><span data-stu-id="2efd5-257">Edition</span></span></th>
<th align="left"><span data-ttu-id="2efd5-258">Service Pack</span><span class="sxs-lookup"><span data-stu-id="2efd5-258">Service pack</span></span></th>
<th align="left"><span data-ttu-id="2efd5-259">System Architektur</span><span class="sxs-lookup"><span data-stu-id="2efd5-259">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2efd5-260">Microsoft SQL Server 2019</span><span class="sxs-lookup"><span data-stu-id="2efd5-260">Microsoft SQL Server 2019</span></span></p></td>
<td align="left"><p><span data-ttu-id="2efd5-261">Standard, Enterprise oder Datacenter</span><span class="sxs-lookup"><span data-stu-id="2efd5-261">Standard, Enterprise, or Datacenter</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="2efd5-262">64Bit</span><span class="sxs-lookup"><span data-stu-id="2efd5-262">64-bit</span></span></p></td><br/><tr class="even">
<td align="left"><p><span data-ttu-id="2efd5-263">Microsoft SQL Server 2017</span><span class="sxs-lookup"><span data-stu-id="2efd5-263">Microsoft SQL Server 2017</span></span></p></td>
<td align="left"><p><span data-ttu-id="2efd5-264">Standard, Enterprise oder Datacenter</span><span class="sxs-lookup"><span data-stu-id="2efd5-264">Standard, Enterprise, or Datacenter</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="2efd5-265">64Bit</span><span class="sxs-lookup"><span data-stu-id="2efd5-265">64-bit</span></span></p></td><br/><tr class="even">
<td align="left"><p><span data-ttu-id="2efd5-266">Microsoft SQL Server 2016</span><span class="sxs-lookup"><span data-stu-id="2efd5-266">Microsoft SQL Server 2016</span></span></p></td>
<td align="left"><p><span data-ttu-id="2efd5-267">Standard, Enterprise oder Datacenter</span><span class="sxs-lookup"><span data-stu-id="2efd5-267">Standard, Enterprise, or Datacenter</span></span></p></td>
<td align="left"><p><span data-ttu-id="2efd5-268">SP1</span><span class="sxs-lookup"><span data-stu-id="2efd5-268">SP1</span></span></p></td>
<a href="https://www.microsoft.com/download/details.aspx?id=54967" data-raw-source="https://www.microsoft.com/download/details.aspx?id=54967">https://www.microsoft.com/download/details.aspx?id=54967</a><td align="left"><p><span data-ttu-id="2efd5-269">64Bit</span><span class="sxs-lookup"><span data-stu-id="2efd5-269">64-bit</span></span></p></td>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2efd5-270">Microsoft SQL Server 2014</span><span class="sxs-lookup"><span data-stu-id="2efd5-270">Microsoft SQL Server 2014</span></span></p></td>
<td align="left"><p><span data-ttu-id="2efd5-271">Standard, Enterprise oder Datacenter</span><span class="sxs-lookup"><span data-stu-id="2efd5-271">Standard, Enterprise, or Datacenter</span></span></p></td>
<td align="left"><p><span data-ttu-id="2efd5-272">SP1, SP2</span><span class="sxs-lookup"><span data-stu-id="2efd5-272">SP1, SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="2efd5-273">64Bit</span><span class="sxs-lookup"><span data-stu-id="2efd5-273">64-bit</span></span></p></td>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2efd5-274">Microsoft SQL Server 2012</span><span class="sxs-lookup"><span data-stu-id="2efd5-274">Microsoft SQL Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="2efd5-275">Standard, Enterprise oder Datacenter</span><span class="sxs-lookup"><span data-stu-id="2efd5-275">Standard, Enterprise, or Datacenter</span></span></p></td>
<td align="left"><p><span data-ttu-id="2efd5-276">SP3</span><span class="sxs-lookup"><span data-stu-id="2efd5-276">SP3</span></span></p></td>
<td align="left"><p><span data-ttu-id="2efd5-277">64Bit</span><span class="sxs-lookup"><span data-stu-id="2efd5-277">64-bit</span></span></p></td>
<tr class="even">
<td align="left"><p><span data-ttu-id="2efd5-278">Microsoft SQL Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="2efd5-278">Microsoft SQL Server 2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="2efd5-279">Standard oder Enterprise</span><span class="sxs-lookup"><span data-stu-id="2efd5-279">Standard or Enterprise</span></span></p></td>
<td align="left"><p><span data-ttu-id="2efd5-280">SP3</span><span class="sxs-lookup"><span data-stu-id="2efd5-280">SP3</span></span></p></td>
<td align="left"><p><span data-ttu-id="2efd5-281">64Bit</span><span class="sxs-lookup"><span data-stu-id="2efd5-281">64-bit</span></span></p></td>
</tr>
</tbody>
</table>

**<span data-ttu-id="2efd5-282">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="2efd5-282">Note</span></span>**  
<span data-ttu-id="2efd5-283">MBAM hat einen maximal unterstützten Kompatibilitätsgrad von 140.</span><span class="sxs-lookup"><span data-stu-id="2efd5-283">MBAM has a maximum supported compatibility level of 140.</span></span> <span data-ttu-id="2efd5-284">Der Standardkompatibilitätsgrad für neue Datenbanken, die auf SQL Server 2019 erstellt wurden, ist 150, die nach der Erstellung der Datenbank mit dem Befehl ALTER DATABASE nach 140 oder niedriger geändert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="2efd5-284">The default compatibility level for new databases created on SQL Server 2019 is 150 which will need to be altered to 140 or lower, using the ALTER DATABASE command, after the database has been created.</span></span> <span data-ttu-id="2efd5-285">Vorhandene Datenbanken, die von SQL Server 2017 oder darunter migriert wurden, verbleiben auf dem vorherigen Kompatibilitätsgrad und müssen nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="2efd5-285">Existing databases migrated from SQL server 2017 or below will remain at their previous compatibility level and do not need to be altered.</span></span>

<span data-ttu-id="2efd5-286">Um SQL 2016 zu unterstützen, müssen Sie die Service Version für März 2017 für MDOP installieren https://www.microsoft.com/download/details.aspx?id=54967  und SQL 2017 unterstützen, wenn Sie die Version vom Juli 2018 für MDOP installieren müssen https://www.microsoft.com/download/details.aspx?id=57157 .</span><span class="sxs-lookup"><span data-stu-id="2efd5-286">In order to support SQL 2016 you must install the March 2017 Servicing Release for MDOP https://www.microsoft.com/download/details.aspx?id=54967  and to support SQL 2017 you must install the July 2018 Servicing Release for MDOP https://www.microsoft.com/download/details.aspx?id=57157.</span></span> <span data-ttu-id="2efd5-287">Im allgemeinen bleiben Sie stets auf dem laufenden, indem Sie immer das neueste Wartungsupdate verwenden, da es auch alle Bugfixes und neuen Features enthält.</span><span class="sxs-lookup"><span data-stu-id="2efd5-287">In general stay current by always using the most recent servicing update as it also includes all bugfixes and new features.</span></span>


### <a href="" id="bkmk-sql-stand-alone-ramreqs"></a><span data-ttu-id="2efd5-288">SQL Server-Prozessor, RAM und Speicherplatzanforderungen – eigenständige Topologie</span><span class="sxs-lookup"><span data-stu-id="2efd5-288">SQL Server processor, RAM, and disk space requirements – Stand-alone topology</span></span>

<span data-ttu-id="2efd5-289">In der folgenden Tabelle sind die empfohlenen Server Prozessor-, RAM-und Speicherplatzanforderungen für den SQL Server-Computer aufgeführt, wenn Sie die eigenständige Topologie verwenden.</span><span class="sxs-lookup"><span data-stu-id="2efd5-289">The following table lists the recommended server processor, RAM, and disk space requirements for the SQL Server computer when you are using the Stand-alone topology.</span></span> <span data-ttu-id="2efd5-290">Verwenden Sie diese Anforderungen als Leitfaden.</span><span class="sxs-lookup"><span data-stu-id="2efd5-290">Use these requirements as a guide.</span></span> <span data-ttu-id="2efd5-291">Ihre spezifischen Anforderungen unterscheiden sich je nach der Anzahl der Clientcomputer, die Sie in Ihrem Unternehmen unterstützen.</span><span class="sxs-lookup"><span data-stu-id="2efd5-291">Your specific requirements will vary based on the number of client computers you are supporting in your enterprise.</span></span> <span data-ttu-id="2efd5-292">Informationen zum Anzeigen der Anforderungen für die Configuration Manager-Integrations Topologie finden Sie unter [SQL Server-Prozessor, RAM und Speicherplatzanforderungen – Configuration Manager-Integrations Topologie](#bkmk-cm-sql-ramreqs).</span><span class="sxs-lookup"><span data-stu-id="2efd5-292">To view the requirements for the Configuration Manager Integration topology, see [SQL Server Processor, RAM, and Disk Space Requirements - Configuration Manager Integration Topology](#bkmk-cm-sql-ramreqs).</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="2efd5-293">Hardware Element</span><span class="sxs-lookup"><span data-stu-id="2efd5-293">Hardware item</span></span></th>
<th align="left"><span data-ttu-id="2efd5-294">Mindestanforderungen</span><span class="sxs-lookup"><span data-stu-id="2efd5-294">Minimum requirement</span></span></th>
<th align="left"><span data-ttu-id="2efd5-295">Empfohlene Anforderung</span><span class="sxs-lookup"><span data-stu-id="2efd5-295">Recommended requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2efd5-296">Prozessor</span><span class="sxs-lookup"><span data-stu-id="2efd5-296">Processor</span></span></p></td>
<td align="left"><p><span data-ttu-id="2efd5-297">2,33 GHz</span><span class="sxs-lookup"><span data-stu-id="2efd5-297">2.33 GHz</span></span></p></td>
<td align="left"><p><span data-ttu-id="2efd5-298">2,33 GHz oder höher</span><span class="sxs-lookup"><span data-stu-id="2efd5-298">2.33 GHz or greater</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2efd5-299">RAM</span><span class="sxs-lookup"><span data-stu-id="2efd5-299">RAM</span></span></p></td>
<td align="left"><p><span data-ttu-id="2efd5-300">8 GB</span><span class="sxs-lookup"><span data-stu-id="2efd5-300">8 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="2efd5-301">12 GB</span><span class="sxs-lookup"><span data-stu-id="2efd5-301">12 GB</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2efd5-302">Freier Speicherplatz</span><span class="sxs-lookup"><span data-stu-id="2efd5-302">Free disk space</span></span></p></td>
<td align="left"><p><span data-ttu-id="2efd5-303">5 GB</span><span class="sxs-lookup"><span data-stu-id="2efd5-303">5 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="2efd5-304">5 GB oder höher</span><span class="sxs-lookup"><span data-stu-id="2efd5-304">5 GB or greater</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-cm-sql-ramreqs"></a><span data-ttu-id="2efd5-305">SQL Server-Prozessor, RAM und Speicherplatzanforderungen – Configuration Manager-Integrations Topologie</span><span class="sxs-lookup"><span data-stu-id="2efd5-305">SQL Server processor, RAM, and disk space requirements - Configuration Manager Integration topology</span></span>

<span data-ttu-id="2efd5-306">In der folgenden Tabelle sind die Anforderungen für den Server Prozessor, den Arbeitsspeicher und den Speicherplatz für den Microsoft SQL Server-Computer aufgeführt, wenn Sie die Configuration Manager-Integrations Topologie verwenden, siehe [SQL Server-Prozessor, RAM und Speicherplatzanforderungen – eigenständige Topologie](#bkmk-sql-stand-alone-ramreqs).</span><span class="sxs-lookup"><span data-stu-id="2efd5-306">The following table lists the server processor, RAM, and disk space requirements for the Microsoft SQL Server computer when you are using the Configuration Manager Integration topology, see [SQL Server Processor, RAM, and Disk Space Requirements – Stand-alone Topology](#bkmk-sql-stand-alone-ramreqs).</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="2efd5-307">Hardware Element</span><span class="sxs-lookup"><span data-stu-id="2efd5-307">Hardware item</span></span></th>
<th align="left"><span data-ttu-id="2efd5-308">Mindestanforderungen</span><span class="sxs-lookup"><span data-stu-id="2efd5-308">Minimum requirement</span></span></th>
<th align="left"><span data-ttu-id="2efd5-309">Empfohlene Anforderung</span><span class="sxs-lookup"><span data-stu-id="2efd5-309">Recommended requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2efd5-310">Prozessor</span><span class="sxs-lookup"><span data-stu-id="2efd5-310">Processor</span></span></p></td>
<td align="left"><p><span data-ttu-id="2efd5-311">2,33 GHz</span><span class="sxs-lookup"><span data-stu-id="2efd5-311">2.33 GHz</span></span></p></td>
<td align="left"><p><span data-ttu-id="2efd5-312">2,33 GHz oder höher</span><span class="sxs-lookup"><span data-stu-id="2efd5-312">2.33 GHz or greater</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2efd5-313">RAM</span><span class="sxs-lookup"><span data-stu-id="2efd5-313">RAM</span></span></p></td>
<td align="left"><p><span data-ttu-id="2efd5-314">4 GB</span><span class="sxs-lookup"><span data-stu-id="2efd5-314">4 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="2efd5-315">8 GB</span><span class="sxs-lookup"><span data-stu-id="2efd5-315">8 GB</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2efd5-316">Freier Speicherplatz</span><span class="sxs-lookup"><span data-stu-id="2efd5-316">Free disk space</span></span></p></td>
<td align="left"><p><span data-ttu-id="2efd5-317">5 GB</span><span class="sxs-lookup"><span data-stu-id="2efd5-317">5 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="2efd5-318">5 GB</span><span class="sxs-lookup"><span data-stu-id="2efd5-318">5 GB</span></span></p></td>
</tr>
</tbody>
</table>



## <a href="" id="---------mbam-client-system-requirements"></a> <span data-ttu-id="2efd5-319">MBAM-Client Systemanforderungen</span><span class="sxs-lookup"><span data-stu-id="2efd5-319">MBAM Client system requirements</span></span>


### <span data-ttu-id="2efd5-320">Client-Betriebssystemanforderungen</span><span class="sxs-lookup"><span data-stu-id="2efd5-320">Client operating system requirements</span></span>

<span data-ttu-id="2efd5-321">Wir empfehlen dringend, dass Sie den MBAM-Client und den MBAM-Server auf der gleichen Betriebssystem Zeile ausführen.</span><span class="sxs-lookup"><span data-stu-id="2efd5-321">We strongly recommend that you run the MBAM Client and MBAM Server on the same line of operating systems.</span></span> <span data-ttu-id="2efd5-322">Beispiel: Windows 10 mit Windows Server 2016, Windows 8,1 mit Windows Server 2012 R2 usw.</span><span class="sxs-lookup"><span data-stu-id="2efd5-322">For example, Windows 10 with Windows Server 2016, Windows 8.1 with Windows Server 2012 R2, and so on.</span></span>

<span data-ttu-id="2efd5-323">In der folgenden Tabelle sind die Betriebssysteme aufgeführt, die für die MBAM-Client Installation unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="2efd5-323">The following table lists the operating systems that are supported for MBAM Client installation.</span></span> <span data-ttu-id="2efd5-324">Die gleichen Anforderungen gelten für die eigenständige und die Configuration Manager-Integrations Topologie.</span><span class="sxs-lookup"><span data-stu-id="2efd5-324">The same requirements apply to the Stand-alone and the Configuration Manager Integration topologies.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="2efd5-325">Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="2efd5-325">Operating system</span></span></th>
<th align="left"><span data-ttu-id="2efd5-326">Edition</span><span class="sxs-lookup"><span data-stu-id="2efd5-326">Edition</span></span></th>
<th align="left"><span data-ttu-id="2efd5-327">Service Pack</span><span class="sxs-lookup"><span data-stu-id="2efd5-327">Service pack</span></span></th>
<th align="left"><span data-ttu-id="2efd5-328">System Architektur</span><span class="sxs-lookup"><span data-stu-id="2efd5-328">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="even">
    <td align="left"><p><span data-ttu-id="2efd5-329">Windows 10-viel</span><span class="sxs-lookup"><span data-stu-id="2efd5-329">Windows 10 IoT</span></span></p></td>
    <td align="left"><p><span data-ttu-id="2efd5-330">Unternehmen</span><span class="sxs-lookup"><span data-stu-id="2efd5-330">Enterprise</span></span></p></td>
    <td align="left"><p></p></td>
    <td align="left"><p><span data-ttu-id="2efd5-331">32 Bit oder 64 Bit</span><span class="sxs-lookup"><span data-stu-id="2efd5-331">32-bit or 64-bit</span></span></p></td>
</tr><br/><tr class="odd">
<td align="left"><p><span data-ttu-id="2efd5-332">Windows 10</span><span class="sxs-lookup"><span data-stu-id="2efd5-332">Windows 10</span></span></p></td>
<td align="left"><p><span data-ttu-id="2efd5-333">Unternehmen</span><span class="sxs-lookup"><span data-stu-id="2efd5-333">Enterprise</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="2efd5-334">32 Bit oder 64 Bit</span><span class="sxs-lookup"><span data-stu-id="2efd5-334">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2efd5-335">Windows8.1</span><span class="sxs-lookup"><span data-stu-id="2efd5-335">Windows 8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="2efd5-336">Unternehmen</span><span class="sxs-lookup"><span data-stu-id="2efd5-336">Enterprise</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="2efd5-337">32 Bit oder 64 Bit</span><span class="sxs-lookup"><span data-stu-id="2efd5-337">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2efd5-338">Windows7</span><span class="sxs-lookup"><span data-stu-id="2efd5-338">Windows 7</span></span></p></td>
<td align="left"><p><span data-ttu-id="2efd5-339">Enterprise oder Ultimate</span><span class="sxs-lookup"><span data-stu-id="2efd5-339">Enterprise or Ultimate</span></span></p></td>
<td align="left"><p><span data-ttu-id="2efd5-340">SP1</span><span class="sxs-lookup"><span data-stu-id="2efd5-340">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="2efd5-341">32 Bit oder 64 Bit</span><span class="sxs-lookup"><span data-stu-id="2efd5-341">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2efd5-342">Windows To Go</span><span class="sxs-lookup"><span data-stu-id="2efd5-342">Windows To Go</span></span></p></td>
<td align="left"><p><span data-ttu-id="2efd5-343">Windows 8,1 und Windows 10 Enterprise</span><span class="sxs-lookup"><span data-stu-id="2efd5-343">Windows 8.1 and Windows 10 Enterprise</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="2efd5-344">32 Bit oder 64 Bit</span><span class="sxs-lookup"><span data-stu-id="2efd5-344">32-bit or 64-bit</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="client-ram-requirements-"></a><span data-ttu-id="2efd5-345">Client-RAM-Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2efd5-345">Client RAM requirements</span></span>

<span data-ttu-id="2efd5-346">Für die MBAM-Client Installation gibt es keine spezifischen RAM-Anforderungen.</span><span class="sxs-lookup"><span data-stu-id="2efd5-346">There are no RAM requirements that are specific to the MBAM Client installation.</span></span>

## <a href="" id="---------mbam-group-policy-system-requirements"></a> <span data-ttu-id="2efd5-347">Systemanforderungen für MBAM-Gruppenrichtlinien</span><span class="sxs-lookup"><span data-stu-id="2efd5-347">MBAM Group Policy system requirements</span></span>


<span data-ttu-id="2efd5-348">In der folgenden Tabelle sind die Betriebssysteme aufgeführt, die für die Installation von MBAM-Gruppenrichtlinienvorlagen unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="2efd5-348">The following table lists the operating systems that are supported for MBAM Group Policy Templates installation.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="2efd5-349">Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="2efd5-349">Operating system</span></span></th>
<th align="left"><span data-ttu-id="2efd5-350">Edition</span><span class="sxs-lookup"><span data-stu-id="2efd5-350">Edition</span></span></th>
<th align="left"><span data-ttu-id="2efd5-351">Service Pack</span><span class="sxs-lookup"><span data-stu-id="2efd5-351">Service pack</span></span></th>
<th align="left"><span data-ttu-id="2efd5-352">System Architektur</span><span class="sxs-lookup"><span data-stu-id="2efd5-352">System architecture</span></span></th>
</tr>
</thead>
<tbody>
 <tr class="even">
      <td align="left"><p><span data-ttu-id="2efd5-353">Windows 10-viel</span><span class="sxs-lookup"><span data-stu-id="2efd5-353">Windows 10 IoT</span></span></p></td>
      <td align="left"><p><span data-ttu-id="2efd5-354">Unternehmen</span><span class="sxs-lookup"><span data-stu-id="2efd5-354">Enterprise</span></span></p></td>
      <td align="left"><p></p></td>
      <td align="left"><p><span data-ttu-id="2efd5-355">32 Bit oder 64 Bit</span><span class="sxs-lookup"><span data-stu-id="2efd5-355">32-bit or 64-bit</span></span></p></td>
 </tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2efd5-356">Windows 10</span><span class="sxs-lookup"><span data-stu-id="2efd5-356">Windows 10</span></span></p></td>
<td align="left"><p><span data-ttu-id="2efd5-357">Unternehmen</span><span class="sxs-lookup"><span data-stu-id="2efd5-357">Enterprise</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="2efd5-358">32 Bit oder 64 Bit</span><span class="sxs-lookup"><span data-stu-id="2efd5-358">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2efd5-359">Windows8.1</span><span class="sxs-lookup"><span data-stu-id="2efd5-359">Windows 8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="2efd5-360">Unternehmen</span><span class="sxs-lookup"><span data-stu-id="2efd5-360">Enterprise</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="2efd5-361">32 Bit oder 64 Bit</span><span class="sxs-lookup"><span data-stu-id="2efd5-361">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2efd5-362">Windows7</span><span class="sxs-lookup"><span data-stu-id="2efd5-362">Windows 7</span></span></p></td>
<td align="left"><p><span data-ttu-id="2efd5-363">Enterprise oder Ultimate</span><span class="sxs-lookup"><span data-stu-id="2efd5-363">Enterprise, or Ultimate</span></span></p></td>
<td align="left"><p><span data-ttu-id="2efd5-364">SP1</span><span class="sxs-lookup"><span data-stu-id="2efd5-364">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="2efd5-365">32 Bit oder 64 Bit</span><span class="sxs-lookup"><span data-stu-id="2efd5-365">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2efd5-366">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="2efd5-366">Windows Server 2012 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="2efd5-367">Standard oder Rechenzentrum</span><span class="sxs-lookup"><span data-stu-id="2efd5-367">Standard or Datacenter</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="2efd5-368">64Bit</span><span class="sxs-lookup"><span data-stu-id="2efd5-368">64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2efd5-369">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2efd5-369">Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="2efd5-370">Standard oder Rechenzentrum</span><span class="sxs-lookup"><span data-stu-id="2efd5-370">Standard or Datacenter</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="2efd5-371">64Bit</span><span class="sxs-lookup"><span data-stu-id="2efd5-371">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2efd5-372">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="2efd5-372">Windows Server 2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="2efd5-373">Standard, Enterprise oder Datacenter</span><span class="sxs-lookup"><span data-stu-id="2efd5-373">Standard, Enterprise, or Datacenter</span></span></p></td>
<td align="left"><p><span data-ttu-id="2efd5-374">SP1</span><span class="sxs-lookup"><span data-stu-id="2efd5-374">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="2efd5-375">64Bit</span><span class="sxs-lookup"><span data-stu-id="2efd5-375">64-bit</span></span></p></td>
</tr>
</tbody>
</table>

## <span data-ttu-id="2efd5-376">MBAM in Azure IaaS</span><span class="sxs-lookup"><span data-stu-id="2efd5-376">MBAM In Azure IaaS</span></span>

<span data-ttu-id="2efd5-377">Der MBAM-Server kann in Azure Infrastructure as a Service (IaaS) auf einer der oben aufgeführten unterstützten Betriebssystemversionen bereitgestellt werden, die eine Verbindung mit einem lokal gehosteten Active Directory oder einem Active Directory herstellt, das auch in Azure IaaS gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="2efd5-377">The MBAM server can be deployed in Azure Infrastructure as a Service (IaaS) on any of the supported OS versions listed above, connecting to an Active Directory hosted on premises or an Active Directory also hosted in Azure IaaS.</span></span>  <span data-ttu-id="2efd5-378">Die Dokumentation zum Einrichten und Konfigurieren von Active Directory auf Azure IaaS finden Sie [hier](https://msdn.microsoft.com/library/azure/jj156090.aspx).</span><span class="sxs-lookup"><span data-stu-id="2efd5-378">Documentation for setting up and configuring Active Directory on Azure IaaS is [here](https://msdn.microsoft.com/library/azure/jj156090.aspx).</span></span>

<span data-ttu-id="2efd5-379">Der MBAM-Client wird auf virtuellen Computern nicht unterstützt und auch auf Azure IaaS nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2efd5-379">The MBAM client is not supported on virtual machines and is also not supported on Azure IaaS.</span></span>


## <span data-ttu-id="2efd5-380">Dienstversionen</span><span class="sxs-lookup"><span data-stu-id="2efd5-380">Service releases</span></span> 

- [<span data-ttu-id="2efd5-381">Hotfix für April 2016</span><span class="sxs-lookup"><span data-stu-id="2efd5-381">April 2016 hotfix</span></span>](https://support.microsoft.com/help/3144445/april-2016-hotfix-rollup-for-microsoft-desktop-optimization-pack)
- [<span data-ttu-id="2efd5-382">September 2016</span><span class="sxs-lookup"><span data-stu-id="2efd5-382">September 2016</span></span>](https://support.microsoft.com/ms-my/help/3168628/september-2016-servicing-release-for-microsoft-desktop-optimization-pa)
- [<span data-ttu-id="2efd5-383">Dezember 2016</span><span class="sxs-lookup"><span data-stu-id="2efd5-383">December 2016</span></span>](https://support.microsoft.com/help/3198158/december-2016-servicing-release-for-microsoft-desktop-optimization-pac)
- [<span data-ttu-id="2efd5-384">März 2017</span><span class="sxs-lookup"><span data-stu-id="2efd5-384">March 2017</span></span>](https://support.microsoft.com/en-ie/help/4014009/march-2017-servicing-release-for-microsoft-desktop-optimization-pack) 
- [<span data-ttu-id="2efd5-385">Juni 2017</span><span class="sxs-lookup"><span data-stu-id="2efd5-385">June 2017</span></span>](https://support.microsoft.com/af-za/help/4018510/june-2017-servicing-release-for-microsoft-desktop-optimization-pack)
- [<span data-ttu-id="2efd5-386">September2017</span><span class="sxs-lookup"><span data-stu-id="2efd5-386">September 2017</span></span>](https://support.microsoft.com/en-ie/help/4041137/september-2017-servicing-release-for-microsoft-desktop-optimization)
- [<span data-ttu-id="2efd5-387">März 2018</span><span class="sxs-lookup"><span data-stu-id="2efd5-387">March 2018</span></span>](https://support.microsoft.com/help/4074878/march-2018-servicing-release-for-microsoft-desktop-optimization-pack)
- [<span data-ttu-id="2efd5-388">Juli 2018</span><span class="sxs-lookup"><span data-stu-id="2efd5-388">July 2018</span></span>](https://support.microsoft.com/help/4340040/july-2018-servicing-release-for-microsoft-desktop-optimization-pack)
- [<span data-ttu-id="2efd5-389">Mai 2019</span><span class="sxs-lookup"><span data-stu-id="2efd5-389">May 2019</span></span>](https://support.microsoft.com/help/4505175/may-2019-servicing-release-for-microsoft-desktop-optimization-pack)

## <span data-ttu-id="2efd5-390">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="2efd5-390">Related topics</span></span>


[<span data-ttu-id="2efd5-391">Planen der Bereitstellung von MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="2efd5-391">Planning to Deploy MBAM 2.5</span></span>](planning-to-deploy-mbam-25.md)

[<span data-ttu-id="2efd5-392">Vorbereiten der Umgebung für MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="2efd5-392">Preparing your Environment for MBAM 2.5</span></span>](preparing-your-environment-for-mbam-25.md)




## <span data-ttu-id="2efd5-393">Sie haben einen Vorschlag für MBAM?</span><span class="sxs-lookup"><span data-stu-id="2efd5-393">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="2efd5-394">[Hier](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)können Sie Vorschläge hinzufügen oder abstimmen.</span><span class="sxs-lookup"><span data-stu-id="2efd5-394">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="2efd5-395">Bei MBAM-Problemen verwenden Sie das [MBAM TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="2efd5-395">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>




