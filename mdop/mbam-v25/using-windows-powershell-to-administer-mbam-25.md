---
title: Verwenden von Windows PowerShell zum Verwalten von MBAM 2.5
description: Verwenden von Windows PowerShell zum Verwalten von MBAM 2.5
author: dansimp
ms.assetid: 64668e76-2cba-433d-8d2d-50df0a4b2997
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 11/02/2016
ms.openlocfilehash: 8db305bfbdf79723da2b186dd5cc00406a4089cc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804451"
---
# Verwenden von Windows PowerShell zum Verwalten von MBAM 2.5


In diesem Thema werden die Windows PowerShell-Cmdlets für die Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) beschrieben, die sich auf das Wiederherstellen von Computern oder Laufwerken beziehen, wenn Benutzer gesperrt werden.

Informationen zu Cmdlets, die Sie zum Konfigurieren der MBAM-Server Features verwenden, finden Sie unter [Konfigurieren von MBAM 2,5-Server Features mithilfe von Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md).

## <a href="" id="cmdlets-for-recovering-computers-or-drives-that-are-managed-by-mbam-"></a>Cmdlets zum Herstellen von Computern oder Laufwerken, die von MBAM verwaltet werden


Verwenden Sie die folgenden Windows PowerShell-Cmdlets zum Wiederherstellen von Computern oder Laufwerken, die von MBAM verwaltet werden.

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
<td align="left"><p>Get-MbamBitLockerRecoveryKey</p></td>
<td align="left"><p>Fordert einen MBAM-Wiederherstellungsschlüssel an, der Benutzern das Entsperren eines Computers oder eines verschlüsselten Laufwerks ermöglicht.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Get-MbamTPMOwnerPassword</p></td>
<td align="left"><p>Bietet Benutzern ein TPM-Besitzerkennwort, das Sie zum Entsperren eines Trusted Platform Module (TPM) verwenden können, wenn das TPM Sie gesperrt hat und Ihre PIN nicht mehr akzeptiert.</p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="---------mbam-cmdlet-help"></a> Hilfe zu MBAM-Cmdlets


Die Windows PowerShell-Hilfe für MBAM-Cmdlets steht in den folgenden Formaten zur Verfügung:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Windows PowerShell-Hilfeformat</th>
<th align="left">Weitere Informationen</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Geben Sie an einer Windows PowerShell-Eingabeaufforderung <strong> Get-Help- </strong> &lt; <em> Cmdlet ein.</em>&gt;</p></td>
<td align="left"><p>Wenn Sie die neuesten Windows PowerShell-Cmdlets hochladen möchten, befolgen Sie die Anweisungen unter <a href="configuring-mbam-25-server-features-by-using-windows-powershell.md" data-raw-source="[Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)"> Konfigurieren von MBAM 2,5-Server Features mithilfe von Windows PowerShell.</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Auf TechNet als Webseiten</p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=393498" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=393498">https://go.microsoft.com/fwlink/?LinkId=393498</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Im Download Center als Word. docx-Datei</p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=393497" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=393497">https://go.microsoft.com/fwlink/?LinkId=393497</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Im Download Center als PDF-Datei</p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=393499" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=393499">https://go.microsoft.com/fwlink/?LinkId=393499</a></p></td>
</tr>
</tbody>
</table>

 



## Verwandte Themen


[Verwalten von MBAM 2.5-Funktionen](administering-mbam-25-features.md)

[Konfigurieren von MBAM 2.5 Serverfunktionen mithilfe von Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)

 

## Sie haben einen Vorschlag für MBAM?
- [Hier](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)können Sie Vorschläge hinzufügen oder abstimmen. 
- Bei MBAM-Problemen verwenden Sie das [MBAM TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





