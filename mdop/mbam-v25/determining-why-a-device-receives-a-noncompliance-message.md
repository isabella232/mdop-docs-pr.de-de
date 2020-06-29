---
title: Ermitteln, warum ein Gerät eine Benachrichtigung zur Nichtkompatibilität empfängt
description: Ermitteln, warum ein Gerät eine Benachrichtigung zur Nichtkompatibilität empfängt
author: dansimp
ms.assetid: 793df330-a0ee-4759-b53a-95618ac74428
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/22/2017
ms.openlocfilehash: ce1d344676ebf4328506228f1bfa87c76e8036f9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810636"
---
# <span data-ttu-id="43045-103">Ermitteln, warum ein Gerät eine Benachrichtigung zur Nichtkompatibilität empfängt</span><span class="sxs-lookup"><span data-stu-id="43045-103">Determining why a Device Receives a Noncompliance Message</span></span>


<span data-ttu-id="43045-104">Die folgenden nicht Konformitäts Codes werden von WMI bereitgestellt und beschreiben die Gründe, warum ein bestimmtes Gerät von MBAM als nicht kompatibel gemeldet wird.</span><span class="sxs-lookup"><span data-stu-id="43045-104">The following noncompliance codes are provided by WMI and describe the reasons why a particular device is reported by MBAM as noncompliant.</span></span>

<span data-ttu-id="43045-105">Sie können Ihre bevorzugte Methode verwenden, um WMI anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="43045-105">You can use your preferred method to view WMI.</span></span> <span data-ttu-id="43045-106">Wenn Sie PowerShell verwenden, führen Sie `gwmi -class mbam_volume -Namespace root\microsoft\mbam` eine PowerShell-Eingabeaufforderung aus, und suchen Sie nach ReasonsForNoncompliance.</span><span class="sxs-lookup"><span data-stu-id="43045-106">If you use PowerShell, run `gwmi -class mbam_volume -Namespace root\microsoft\mbam` from a PowerShell prompt and search for ReasonsForNoncompliance.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="43045-107">Nicht Kompatibilitäts Code</span><span class="sxs-lookup"><span data-stu-id="43045-107">Non-Compliance Code</span></span></th>
<th align="left"><span data-ttu-id="43045-108">Grund für die Nichtkonformität</span><span class="sxs-lookup"><span data-stu-id="43045-108">Reason for Non-Compliance</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="43045-109">0</span><span class="sxs-lookup"><span data-stu-id="43045-109">0</span></span></p></td>
<td align="left"><p><span data-ttu-id="43045-110">Verschlüsselungsstärke nicht AES 256.</span><span class="sxs-lookup"><span data-stu-id="43045-110">Cipher strength not AES 256.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="43045-111">1</span><span class="sxs-lookup"><span data-stu-id="43045-111">1</span></span></p></td>
<td align="left"><p><span data-ttu-id="43045-112">Für die MBAM-Richtlinie muss dieser Datenträger verschlüsselt sein, aber nicht.</span><span class="sxs-lookup"><span data-stu-id="43045-112">MBAM Policy requires this volume to be encrypted but it is not.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="43045-113">2</span><span class="sxs-lookup"><span data-stu-id="43045-113">2</span></span></p></td>
<td align="left"><p><span data-ttu-id="43045-114">Für die MBAM-Richtlinie muss dieser Datenträger nicht verschlüsselt werden, aber es ist.</span><span class="sxs-lookup"><span data-stu-id="43045-114">MBAM Policy requires this volume to NOT be encrypted, but it is.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="43045-115">3</span><span class="sxs-lookup"><span data-stu-id="43045-115">3</span></span></p></td>
<td align="left"><p><span data-ttu-id="43045-116">Die MBAM-Richtlinie setzt voraus, dass dieser Datenträger einen TPM-Schutz verwendet.</span><span class="sxs-lookup"><span data-stu-id="43045-116">MBAM Policy requires this volume use a TPM protector, but it does not.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="43045-117">4</span><span class="sxs-lookup"><span data-stu-id="43045-117">4</span></span></p></td>
<td align="left"><p><span data-ttu-id="43045-118">Für die MBAM-Richtlinie muss dieser Datenträger ein TPM + PIN-Schutz verwenden, aber nicht.</span><span class="sxs-lookup"><span data-stu-id="43045-118">MBAM Policy requires this volume use a TPM+PIN protector, but it does not.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="43045-119">5</span><span class="sxs-lookup"><span data-stu-id="43045-119">5</span></span></p></td>
<td align="left"><p><span data-ttu-id="43045-120">Die MBAM-Richtlinie lässt nicht zu, dass nicht-TPM-Computer als kompatibel gemeldet werden.</span><span class="sxs-lookup"><span data-stu-id="43045-120">MBAM Policy does not allow non TPM machines to report as compliant.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="43045-121">6</span><span class="sxs-lookup"><span data-stu-id="43045-121">6</span></span></p></td>
<td align="left"><p><span data-ttu-id="43045-122">Das Volume hat eine TPM-Beschützer, das TPM ist aber nicht sichtbar (gebootet mit dem Wiederherstellungsschlüssel nach dem Deaktivieren von TPM im BIOS?).</span><span class="sxs-lookup"><span data-stu-id="43045-122">Volume has a TPM protector but the TPM is not visible (booted with recover key after disabling TPM in BIOS?).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="43045-123">7</span><span class="sxs-lookup"><span data-stu-id="43045-123">7</span></span></p></td>
<td align="left"><p><span data-ttu-id="43045-124">Die MBAM-Richtlinie setzt voraus, dass dieser Datenträger einen Kennwortschutz verwendet.</span><span class="sxs-lookup"><span data-stu-id="43045-124">MBAM Policy requires this volume use a password protector, but it does not have one.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="43045-125">8</span><span class="sxs-lookup"><span data-stu-id="43045-125">8</span></span></p></td>
<td align="left"><p><span data-ttu-id="43045-126">Die MBAM-Richtlinie setzt voraus, dass dieser Datenträger keine Kenn Wort Schutzmittel verwendet, aber eine hat.</span><span class="sxs-lookup"><span data-stu-id="43045-126">MBAM Policy requires this volume NOT use a password protector, but it has one.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="43045-127">9</span><span class="sxs-lookup"><span data-stu-id="43045-127">9</span></span></p></td>
<td align="left"><p><span data-ttu-id="43045-128">Die MBAM-Richtlinie setzt voraus, dass dieser Datenträger einen automatischen Unlock-Schutz verwendet, aber nicht über einen.</span><span class="sxs-lookup"><span data-stu-id="43045-128">MBAM Policy requires this volume use an auto-unlock protector, but it does not have one.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="43045-129">10</span><span class="sxs-lookup"><span data-stu-id="43045-129">10</span></span></p></td>
<td align="left"><p><span data-ttu-id="43045-130">Die MBAM-Richtlinie setzt voraus, dass dieser Datenträger keinen automatischen entsperren-Schutz verwendet, aber einen hat.</span><span class="sxs-lookup"><span data-stu-id="43045-130">MBAM Policy requires this volume NOT use an auto-unlock protector, but it has one.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="43045-131">11</span><span class="sxs-lookup"><span data-stu-id="43045-131">11</span></span></p></td>
<td align="left"><p><span data-ttu-id="43045-132">Es wurde ein Richtlinienkonflikt festgestellt, der verhindert, dass MBAM dieses Volume als kompatibel meldet.</span><span class="sxs-lookup"><span data-stu-id="43045-132">Policy conflict detected preventing MBAM from reporting this volume as compliant.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="43045-133">12</span><span class="sxs-lookup"><span data-stu-id="43045-133">12</span></span></p></td>
<td align="left"><p><span data-ttu-id="43045-134">Zum Verschlüsseln des BS-Volumes ist eine Systemlautstärke erforderlich, die jedoch nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="43045-134">A system volume is needed to encrypt the OS volume but it is not present.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="43045-135">13</span><span class="sxs-lookup"><span data-stu-id="43045-135">13</span></span></p></td>
<td align="left"><p><span data-ttu-id="43045-136">Der Schutz wird für die Lautstärke angehalten.</span><span class="sxs-lookup"><span data-stu-id="43045-136">Protection is suspended for the volume.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="43045-137">14</span><span class="sxs-lookup"><span data-stu-id="43045-137">14</span></span></p></td>
<td align="left"><p><span data-ttu-id="43045-138">Deaktivieren Sie das Kontrollkästchen für unsichere Vorgänge, es sei denn, die Betriebssystem Lautstärke</span><span class="sxs-lookup"><span data-stu-id="43045-138">AutoUnlock unsafe unless the OS volume is encrypted.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="43045-139">15</span><span class="sxs-lookup"><span data-stu-id="43045-139">15</span></span></p></td>
<td align="left"><p><span data-ttu-id="43045-140">Richtlinie erfordert eine minimale Cypher-Stärke ist XTS-AES-128-Bit, die tatsächliche Verschlüsselungsstärke ist schwächer als die.</span><span class="sxs-lookup"><span data-stu-id="43045-140">Policy requires minimum cypher strength is XTS-AES-128 bit, actual cypher strength is weaker than that.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="43045-141">16</span><span class="sxs-lookup"><span data-stu-id="43045-141">16</span></span></p></td>
<td align="left"><p><span data-ttu-id="43045-142">Richtlinie erfordert eine minimale Cypher-Stärke ist XTS-AES-256-Bit, die tatsächliche Verschlüsselungsstärke ist schwächer als die.</span><span class="sxs-lookup"><span data-stu-id="43045-142">Policy requires minimum cypher strength is XTS-AES-256 bit, actual cypher strength is weaker than that.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="43045-143">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="43045-143">Related topics</span></span>


[<span data-ttu-id="43045-144">Technische Referenz für MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="43045-144">Technical Reference for MBAM 2.5</span></span>](technical-reference-for-mbam-25.md)

[<span data-ttu-id="43045-145">Konfigurieren von MBAM 2.5 Serverfunktionen mithilfe von Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="43045-145">Configuring MBAM 2.5 Server Features by Using Windows PowerShell</span></span>](configuring-mbam-25-server-features-by-using-windows-powershell.md)

 
## <span data-ttu-id="43045-146">Sie haben einen Vorschlag für MBAM?</span><span class="sxs-lookup"><span data-stu-id="43045-146">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="43045-147">[Hier](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)können Sie Vorschläge hinzufügen oder abstimmen.</span><span class="sxs-lookup"><span data-stu-id="43045-147">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="43045-148">Bei MBAM-Problemen verwenden Sie das [MBAM TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="43045-148">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>
 





