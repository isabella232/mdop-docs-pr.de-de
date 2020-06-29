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
# Ermitteln, warum ein Gerät eine Benachrichtigung zur Nichtkompatibilität empfängt


Die folgenden nicht Konformitäts Codes werden von WMI bereitgestellt und beschreiben die Gründe, warum ein bestimmtes Gerät von MBAM als nicht kompatibel gemeldet wird.

Sie können Ihre bevorzugte Methode verwenden, um WMI anzuzeigen. Wenn Sie PowerShell verwenden, führen Sie `gwmi -class mbam_volume -Namespace root\microsoft\mbam` eine PowerShell-Eingabeaufforderung aus, und suchen Sie nach ReasonsForNoncompliance.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nicht Kompatibilitäts Code</th>
<th align="left">Grund für die Nichtkonformität</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>0</p></td>
<td align="left"><p>Verschlüsselungsstärke nicht AES 256.</p></td>
</tr>
<tr class="even">
<td align="left"><p>1</p></td>
<td align="left"><p>Für die MBAM-Richtlinie muss dieser Datenträger verschlüsselt sein, aber nicht.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>2</p></td>
<td align="left"><p>Für die MBAM-Richtlinie muss dieser Datenträger nicht verschlüsselt werden, aber es ist.</p></td>
</tr>
<tr class="even">
<td align="left"><p>3</p></td>
<td align="left"><p>Die MBAM-Richtlinie setzt voraus, dass dieser Datenträger einen TPM-Schutz verwendet.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>4</p></td>
<td align="left"><p>Für die MBAM-Richtlinie muss dieser Datenträger ein TPM + PIN-Schutz verwenden, aber nicht.</p></td>
</tr>
<tr class="even">
<td align="left"><p>5</p></td>
<td align="left"><p>Die MBAM-Richtlinie lässt nicht zu, dass nicht-TPM-Computer als kompatibel gemeldet werden.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>6</p></td>
<td align="left"><p>Das Volume hat eine TPM-Beschützer, das TPM ist aber nicht sichtbar (gebootet mit dem Wiederherstellungsschlüssel nach dem Deaktivieren von TPM im BIOS?).</p></td>
</tr>
<tr class="even">
<td align="left"><p>7</p></td>
<td align="left"><p>Die MBAM-Richtlinie setzt voraus, dass dieser Datenträger einen Kennwortschutz verwendet.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>8</p></td>
<td align="left"><p>Die MBAM-Richtlinie setzt voraus, dass dieser Datenträger keine Kenn Wort Schutzmittel verwendet, aber eine hat.</p></td>
</tr>
<tr class="even">
<td align="left"><p>9</p></td>
<td align="left"><p>Die MBAM-Richtlinie setzt voraus, dass dieser Datenträger einen automatischen Unlock-Schutz verwendet, aber nicht über einen.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>10</p></td>
<td align="left"><p>Die MBAM-Richtlinie setzt voraus, dass dieser Datenträger keinen automatischen entsperren-Schutz verwendet, aber einen hat.</p></td>
</tr>
<tr class="even">
<td align="left"><p>11</p></td>
<td align="left"><p>Es wurde ein Richtlinienkonflikt festgestellt, der verhindert, dass MBAM dieses Volume als kompatibel meldet.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>12</p></td>
<td align="left"><p>Zum Verschlüsseln des BS-Volumes ist eine Systemlautstärke erforderlich, die jedoch nicht vorhanden ist.</p></td>
</tr>
<tr class="even">
<td align="left"><p>13</p></td>
<td align="left"><p>Der Schutz wird für die Lautstärke angehalten.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>14</p></td>
<td align="left"><p>Deaktivieren Sie das Kontrollkästchen für unsichere Vorgänge, es sei denn, die Betriebssystem Lautstärke</p></td>
</tr>
<tr class="even">
<td align="left"><p>15</p></td>
<td align="left"><p>Richtlinie erfordert eine minimale Cypher-Stärke ist XTS-AES-128-Bit, die tatsächliche Verschlüsselungsstärke ist schwächer als die.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>16</p></td>
<td align="left"><p>Richtlinie erfordert eine minimale Cypher-Stärke ist XTS-AES-256-Bit, die tatsächliche Verschlüsselungsstärke ist schwächer als die.</p></td>
</tr>
</tbody>
</table>

 

## Verwandte Themen


[Technische Referenz für MBAM2.5](technical-reference-for-mbam-25.md)

[Konfigurieren von MBAM 2.5 Serverfunktionen mithilfe von Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)

 
## Sie haben einen Vorschlag für MBAM?
- [Hier](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)können Sie Vorschläge hinzufügen oder abstimmen. 
- Bei MBAM-Problemen verwenden Sie das [MBAM TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).
 





