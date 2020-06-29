---
title: Verwalten von MBAM 2.0 mit PowerShell
description: Verwalten von MBAM 2.0 mit PowerShell
author: dansimp
ms.assetid: d785a8df-0a8c-4d70-abd2-93a762b4f3de
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 736943e707b5d033b8ba6c26641393f02f0cdaf8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809994"
---
# Verwalten von MBAM 2.0 mit PowerShell


Die Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) enthält die folgenden aufgelisteten Satz von Windows PowerShell-Cmdlets. Administratoren können diese PowerShell-Cmdlets verwenden, um verschiedene Microsoft BitLocker-Verwaltungs-und-Überwachungsserver Aufgaben über die Befehlszeile statt über die MBAM-Verwaltungswebsite durchzuführen.

## Verwalten von MBAM mit PowerShell


Verwenden Sie die hier beschriebenen PowerShell-Cmdlets, um MBAM zu verwalten.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Name</th>
<th align="left">Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Installieren-mbam</p></td>
<td align="left"><p>Installiert die MBAM-Features, die Erweiterte Richtlinien-, Verschlüsselungs-, Schlüssel Wiederherstellungs-und Konformitätsberichte bieten.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Deinstallieren-mbam</p></td>
<td align="left"><p>Entfernt die MBAM-Features, die Erweiterte Richtlinien-, Verschlüsselungs-, Schlüssel Wiederherstellungs-und Compliance-Berichterstattungstools bieten.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Get-MbamBitLockerRecoveryKey</p></td>
<td align="left"><p>Fordert einen MBAM-Wiederherstellungsschlüssel an, der Benutzern die Sperrung eines Computers oder eines verschlüsselten Laufwerks ermöglicht.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Get-MbamTPMOwnerPassword</p></td>
<td align="left"><p>Bietet Benutzern ein TPM-Besitzerkennwort, das Sie zum Entsperren eines Trusted Platform Module (TPM) verwenden können, wenn das TPM Sie gesperrt hat und Ihre PIN nicht mehr akzeptiert.</p></td>
</tr>
</tbody>
</table>

 

## Verwandte Themen


[Vorgänge für MBAM 2.0](operations-for-mbam-20-mbam-2.md)

 

 





