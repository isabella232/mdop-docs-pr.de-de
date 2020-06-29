---
title: Voraussetzungen für MBAM 2.5-Clients
description: Voraussetzungen für MBAM 2.5-Clients
author: dansimp
ms.assetid: fc230679-9c84-4b99-a77c-bae7e7bf8145
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 04/23/2017
ms.openlocfilehash: ac5e211e5ea038f47db3d5e68155eb5af38aa231
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812073"
---
# Voraussetzungen für MBAM 2.5-Clients


Bevor Sie die MBAM-Client Software auf den Computern der Endbenutzer installieren, stellen Sie sicher, dass Ihre Umgebung und die Clientcomputer die folgenden Voraussetzungen erfüllen.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Voraussetzung</th>
<th align="left">Details</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Die Unternehmensdomäne muss mindestens einen Windows Server 2008-Domänencontroller (oder höher) enthalten.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Der Clientcomputer muss beim Unternehmensintranet angemeldet sein.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Nur für Clientcomputer unter Windows 7: jeder Client muss über eine TPM-Funktion (Trusted Platform Module) verfügen (TPM 1,2 oder höher).</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Für Windows 8,1, Windows 10 RTM oder Windows 10, Version 1511, nur Clientcomputer: Wenn MBAM in der Lage sein soll, die TPM-Wiederherstellungsschlüssel zu speichern und zu verwalten, muss die TPM-automatische Bereitstellung deaktiviert sein, und MBAM muss als Besitzer des TPM eingestellt sein, bevor Sie MBAM bereitstellen.</p>
<p>In MBAM 2,5 SP1 müssen Sie die TPM-automatische Bereitstellung nicht mehr deaktivieren, aber Sie müssen sicherstellen, dass die TPM-Gruppenrichtlinienobjekte auf nicht Escrow-TPM-OwnerAuth zu Active Directory festzulegen sind.</p></td>
<td align="left"><p><a href="mbam-25-security-considerations.md#bkmk-tpm" data-raw-source="[MBAM 2.5 Security Considerations](mbam-25-security-considerations.md#bkmk-tpm)">Sicherheitsüberlegungen zu MBAM2.5</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Für Windows 10, Version 1607 oder höher, kann nur Windows den Besitz des TPM übernehmen. In addiiton wird Windows das TPM-Besitzerkennwort beim Bereitstellen des TPMs nicht beibehalten.</p>
<p>In MBAM 2,5 SP1 müssen Sie die automatische Bereitstellung aktivieren.</p>
</p></td>
<td align="left"><p>Weitere Informationen finden Sie unter <a href="https://technet.microsoft.com/itpro/windows/keep-secure/change-the-tpm-owner-password" data-raw-source="[TPM owner password](https://technet.microsoft.com/itpro/windows/keep-secure/change-the-tpm-owner-password)"> TPM-Besitzerkennwort </a> .
</p></td>
</tr>
<tr class="even">
<td align="left"><p>Der TPM-Chip muss im BIOS aktiviert sein und vom Betriebssystem Rückstellen.</p></td>
<td align="left"><p>Weitere Informationen finden Sie in der BIOS-Dokumentation.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Die Festplatte des Computers muss mindestens zwei Partitionen enthalten und muss mit dem NTFS-Dateisystem formatiert sein.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Die Festplatte des Computers muss ein BIOS aufweisen, das mit TPM kompatibel ist und USB-Geräte während des Computerstarts unterstützt.</p></td>
<td align="left"><div class="alert">
<strong>Hinweis:</strong><br/><p>Stellen Sie sicher, dass die Tastatur, das Video oder die Maus direkt verbunden sind und nicht über einen KVM-Schalter (Keyboard, Video oder Maus) verwaltet werden. Ein KVM-Switch kann die Fähigkeit des Computers stören, die physische Anwesenheit von Hardware zu erkennen.</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>Wenn Sie einen Proxy verwenden, muss er im Systemkontext sichtbar sein. MBAM wird im Systemkontext und nicht im Benutzerkontext ausgeführt.</p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



**Wichtig**  
Wenn BitLocker ohne MBAM verwendet wurde, kann MBAM installiert werden und die vorhandenen TPM-Informationen verwenden.




## Verwandte Themen


[Von MBAM 2.5 unterstützte Konfigurationen](mbam-25-supported-configurations.md)

[Planen der Bereitstellung von MBAM 2.5](planning-to-deploy-mbam-25.md)


## Sie haben einen Vorschlag für MBAM?
- [Hier](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)können Sie Vorschläge hinzufügen oder abstimmen.
- Bei MBAM-Problemen verwenden Sie das [MBAM TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).






