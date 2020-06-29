---
title: Verwalten von MBAM 1.0 mithilfe von PowerShell
description: Verwalten von MBAM 1.0 mithilfe von PowerShell
author: dansimp
ms.assetid: 3bf2eca5-4ab7-4e84-9e80-c0c7d709647b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3547bee9b2efc58252bb6f0a1cb0aa4c484e4e80
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810975"
---
# Verwalten von MBAM 1.0 mithilfe von PowerShell


Die Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) enthält die folgenden aufgelisteten Satz von Windows PowerShell-Cmdlets. Administratoren können mithilfe dieser PowerShell-Cmdlets verschiedene MBAM-Serveraufgaben über die Eingabeaufforderung statt über die MBAM-Verwaltungswebsite ausführen.

## Verwalten von MBAM mithilfe von PowerShell


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
<td align="left"><p>Add-MbamHardwareType</p></td>
<td align="left"><p>Fügt ein neues Hardwaremodell zur MBAM-Hardwareinventur hinzu. Dieses Cmdlet kann auch angeben, ob die Hardware für die BitLocker-Laufwerkverschlüsselung unterstützt oder nicht unterstützt wird.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Get-MbamBitLockerRecoveryKey</p></td>
<td align="left"><p>Fordert einen MBAM-Wiederherstellungsschlüssel an, mit dem ein Benutzer einen Computer oder ein verschlüsseltes Laufwerk entsperren kann.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Get-MbamHardwareType</p></td>
<td align="left"><p>Ruft eine Master-Hardwareinventur ab, die Daten enthält, die angeben, ob Hardware Modelle kompatibel oder mit der BitLocker-Laufwerkverschlüsselung nicht kompatibel sind.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Get-MbamTPMOwnerPassword</p></td>
<td align="left"><p>Stellt ein TPM-Besitzerkennwort für einen Benutzer zum Verwalten des TPM-Zugriffs (Trusted Platform Module) bereit. Hilft Benutzern, wenn TPM Sie gesperrt hat und Ihre PIN nicht mehr akzeptiert.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Installieren-mbam</p></td>
<td align="left"><p>Installiert MBAM-Features, die erweiterte Gruppenrichtlinien-, Verschlüsselungs-, Schlüssel Wiederherstellungs-und Kompatibilitäts Berichterstattungstools bereitstellen.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Remove-MbamHardwareType</p></td>
<td align="left"><p>Entfernt die Hardware Modelle aus der Hardwareinventur.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Satz-MbamHardwareType</p></td>
<td align="left"><p>Ermöglicht die Verwaltung einer Master-Hardwareinventur, um festzulegen, ob Hardware Modelle für die BitLocker-Verschlüsselung geeignet oder nicht geeignet sind.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Deinstallieren-mbam</p></td>
<td align="left"><p>Entfernt zuvor installierte MBAM-Features, die Erweiterte Richtlinien-, Verschlüsselungs-, Schlüssel Wiederherstellungs-und Kompatibilitäts Berichterstattungstools bieten.</p></td>
</tr>
</tbody>
</table>

 

## Verwandte Themen


[Vorgänge für MBAM 1.0](operations-for-mbam-10.md)

 

 





