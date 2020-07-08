---
title: So verwenden Sie die Administration and Monitoring-Website
description: So verwenden Sie die Administration and Monitoring-Website
author: dansimp
ms.assetid: bb96a4e8-d4f4-4e6f-b7db-82d96998bfa6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9b9597e29a5a7a6236cb351d8d6d1f682edce3cf
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804682"
---
# So verwenden Sie die Administration and Monitoring-Website


Die Verwaltungs-und Überwachungs Website, auch als "Helpdesk" bezeichnet, ist eine Verwaltungsschnittstelle für die BitLocker-Laufwerkverschlüsselung. Verwenden Sie die Website, um Berichte zu überprüfen, die Laufwerke der Endbenutzer wiederherzustellen und das TPMs der Endbenutzer zu verwalten, wie in den folgenden Abschnitten beschrieben.

**Hinweis**  Wenn Sie MBAM in der eigenständigen Topologie verwenden, werden alle Berichte auf der Website Verwaltung und Überwachung angezeigt. Wenn Sie die Configuration Manager-Integrations Topologie verwenden, werden alle Berichte in Configuration Manager mit Ausnahme des Wiederherstellungs Überwachungsberichts angezeigt, den Sie auf der Website Verwaltung und Überwachung weiter anzeigen. Weitere Informationen zu Berichten finden Sie unter über [wachen und melden von BitLocker-Konformität mit MBAM 2,5](monitoring-and-reporting-bitlocker-compliance-with-mbam-25.md).

 

## Erforderliche Rollen für die Verwendung der Website "Verwaltung und Überwachung"


Wenn Sie auf bestimmte Bereiche der Verwaltungs-und Überwachungs Website zugreifen möchten, müssen Sie über eine der folgenden Rollen verfügen, bei denen es sich um Gruppen handelt, die Sie in Active Directory erstellen. Sie können einen beliebigen Namen für diese Gruppen verwenden.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Account</th>
<th align="left">Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>MBAM Advanced Helpdesk-Benutzer</p></td>
<td align="left"><p>Bietet Zugriff auf alle Bereiche der Verwaltungs-und Überwachungs Website. Benutzer, die über diese Rolle verfügen, geben nur den Wiederherstellungsschlüssel und nicht die Domäne und den Benutzernamen des Endbenutzers ein, wenn Sie den Endbenutzern helfen, Ihre Laufwerke wiederherzustellen. Wenn ein Benutzer ein Mitglied der Gruppe MBAM Helpdesk-Benutzer und der Gruppe der erweiterten Helpdesk-Benutzer von MBAM ist, überschreiben die Berechtigungen des erweiterten Helpdesk-Benutzers von MBAM die Berechtigungen für die MBAM Helpdesk-Benutzergruppe.</p>
<p></p></td>
</tr>
<tr class="even">
<td align="left"><p>MBAM Helpdesk-Benutzer</p></td>
<td align="left"><p>Bietet Zugriff auf die Bereiche Manage TPM und Drive Recovery der Verwaltungs-und Überwachungs Website. Personen, die über diese Rolle verfügen, müssen alle Felder ausfüllen, einschließlich der Domäne und des Kontonamens des Endbenutzers, wenn beide Bereiche verwendet werden.</p>
<p>Wenn ein Benutzer ein Mitglied der Gruppe MBAM Helpdesk-Benutzer und der Gruppe der erweiterten Helpdesk-Benutzer von MBAM ist, überschreiben die Berechtigungen des erweiterten Helpdesk-Benutzers von MBAM die Berechtigungen für die MBAM Helpdesk-Benutzergruppe.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>MBAM-Berichtsbenutzer</p></td>
<td align="left"><p>Bietet Zugriff auf die Berichte im Bereich "Berichte" auf <strong> </strong> der Website Verwaltung und Überwachung.</p></td>
</tr>
</tbody>
</table>

 

## Aufgaben, die auf der Website "Verwaltung und Überwachung" ausgeführt werden können


In der folgenden Tabelle sind die Aufgaben aufgeführt, die Sie auf der Website Verwaltung und Überwachung ausführen können, und es werden Links zu weiteren Informationen zu den einzelnen Aufgaben bereitgestellt.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Aufgabe</th>
<th align="left">Bereich der Website, auf den Sie auf die Aufgabe zugreifen</th>
<th align="left">Beschreibung</th>
<th align="left">Weitere Informationen</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Anzeigen von Berichten</p></td>
<td align="left"><p>Berichte</p></td>
<td align="left"><p>Ermöglicht Ihnen das Ausführen von Berichten zum Überwachen der BitLocker-Nutzung,-Compliance und-Wiederherstellungs Aktivität. Berichte liefern Daten zur Unternehmenskonformität, zu einzelnen Computern und zur Anforderung von Wiederherstellungsschlüsseln oder zum TPM-OwnerAuth-Paket für einen bestimmten Computer.</p></td>
<td align="left"><p><a href="viewing-mbam-25-reports-for-the-stand-alone-topology.md" data-raw-source="[Viewing MBAM 2.5 Reports for the Stand-alone Topology](viewing-mbam-25-reports-for-the-stand-alone-topology.md)">Anzeigen von MBAM 2.5-Berichten für die eigenständige Topologie</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Ermitteln des BitLocker-Verschlüsselungsstatus von verlorenen oder gestohlenen Computern</p></td>
<td align="left"><p>Berichte</p></td>
<td align="left"><p>Ermitteln Sie, ob ein Volume verschlüsselt wurde, wenn der Computer verloren geht oder gestohlen wurde.</p></td>
<td align="left"><p><a href="how-to-determine-bitlocker-encryption-state-of-lost-computers-mbam-25.md" data-raw-source="[How to Determine BitLocker Encryption State of Lost Computers](how-to-determine-bitlocker-encryption-state-of-lost-computers-mbam-25.md)">So ermitteln Sie den BitLocker-Verschlüsselungsstatus verloren gegangener Computer</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Wiederherstellen verlorener Laufwerke</p></td>
<td align="left"><p>Laufwerk Wiederherstellung</p></td>
<td align="left"><p>Wiederherstellen von Laufwerken, die:</p>
<ul>
<li><p>Im Wiederherstellungsmodus</p></li>
<li><p>Wurden verschoben</p></li>
<li><p>Sind beschädigt</p></li>
</ul></td>
<td align="left"><ul>
<li><p><a href="how-to-recover-a-drive-in-recovery-mode-mbam-25.md" data-raw-source="[How to Recover a Drive in Recovery Mode](how-to-recover-a-drive-in-recovery-mode-mbam-25.md)">So stellen Sie ein Laufwerk im Wiederherstellungsmodus wieder her</a></p></li>
<li><p><a href="how-to-recover-a-moved-drive-mbam-25.md" data-raw-source="[How to Recover a Moved Drive](how-to-recover-a-moved-drive-mbam-25.md)">So stellen Sie ein verschobenes Laufwerk wieder her</a></p></li>
<li><p><a href="how-to-recover-a-corrupted-drive-mbam-25.md" data-raw-source="[How to Recover a Corrupted Drive](how-to-recover-a-corrupted-drive-mbam-25.md)">So stellen Sie ein beschädigtes Laufwerk wieder her</a></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Zurücksetzen einer TPM-Sperrung</p></td>
<td align="left"><p>TPM verwalten</p></td>
<td align="left"><p>Bietet Zugriff auf TPM-Daten, die vom MBAM-Client erfasst wurden. Verwenden Sie in einer TPM-Sperrung die Website Verwaltung und überwachen, um die erforderliche Kennwortdatei zum Entsperren des TPMs abzurufen.</p></td>
<td align="left"><p><a href="how-to-reset-a-tpm-lockout-mbam-25.md" data-raw-source="[How to Reset a TPM Lockout](how-to-reset-a-tpm-lockout-mbam-25.md)">So setzen Sie eine TPM-Sperre zurück</a></p></td>
</tr>
</tbody>
</table>

 


## Verwandte Themen


[Durchführen der BitLocker-Verwaltung mit MBAM 2.5](performing-bitlocker-management-with-mbam-25.md)

 

## Sie haben einen Vorschlag für MBAM?
- [Hier](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)können Sie Vorschläge hinzufügen oder abstimmen. 
- Bei MBAM-Problemen verwenden Sie das [MBAM TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





