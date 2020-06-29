---
title: So verwalten Sie BitLocker-Verschlüsselungsausnahmen für Benutzer
description: So verwalten Sie BitLocker-Verschlüsselungsausnahmen für Benutzer
author: dansimp
ms.assetid: 1bfd9d66-6a9a-4d0e-b54a-e5a6627f5ada
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4d5530701fd208d42dc1f6774fac11ee9ca2036b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810936"
---
# So verwalten Sie BitLocker-Verschlüsselungsausnahmen für Benutzer


Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) kann zum Verwalten des BitLocker-Schutzes verwendet werden, indem Benutzer freigestellt werden, wenn Benutzer vorhanden sind, die Ihre Laufwerke nicht verschlüsseln müssen oder möchten.

Um Benutzer vom BitLocker-Schutz zu befreien, muss eine Organisation eine Infrastruktur zur Unterstützung von ausgenommenen Benutzern erstellen, beispielsweise indem Sie dem Benutzer eine Telefonnummer, eine Webseite oder eine Postanschrift zur Verfügung stellt, um eine Ausnahme zu beantragen. Darüber hinaus muss ein freigestellter Benutzer einer Sicherheitsgruppe für ein Gruppenrichtlinienobjekt hinzugefügt werden, das speziell für befreite Benutzer erstellt wurde. Wenn sich Mitglieder dieser Sicherheitsgruppe an einem Computer anmelden, zeigt die Gruppenrichtlinieneinstellung des Benutzers an, dass der Benutzer vom BitLocker-Schutz ausgenommen ist. Die Gruppenrichtlinieneinstellung des Benutzers überschreibt die Computerrichtlinie, und der Computer bleibt von der BitLocker-Verschlüsselung ausgenommen.

**Hinweis**  Wenn der Computer bereits mit BitLocker geschützt ist, hat die Richtlinie für die Benutzer Befreiung keine Auswirkungen.

 

In der folgenden Tabelle wird gezeigt, wie der BitLocker-Schutz angewendet wird, je nachdem, wie Ausnahmen eingestellt werden.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Benutzer Status</th>
<th align="left">Computer nicht freigestellt</th>
<th align="left">Computer ausgenommen</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Benutzer nicht freigestellt</strong></p></td>
<td align="left"><p>Der BitLocker-Schutz wird auf einem Computer erzwungen</p></td>
<td align="left"><p>Der BitLocker-Schutz wird auf dem Computer nicht erzwungen</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Benutzer freigestellt</strong></p></td>
<td align="left"><p>Der BitLocker-Schutz wird auf dem Computer nicht erzwungen</p></td>
<td align="left"><p>Der BitLocker-Schutz wird auf dem Computer nicht erzwungen</p></td>
</tr>
</tbody>
</table>

 

**So nehmen Sie einen Benutzer von der BitLocker-Verschlüsselung frei**

1.  Erstellen Sie eine ActiveDirectoryDomainServices-Sicherheitsgruppe, die verwendet wird, um Benutzer Ausnahmen von BitLocker-Verschlüsselungsanforderungen zu verwalten.

2.  Erstellen Sie eine Gruppenrichtlinienobjekteinstellung mithilfe der Gruppenrichtlinienvorlage Microsoft BitLocker-Verwaltung und-Überwachung, und ordnen Sie Sie der Active Directory-Gruppe zu, die Sie im vorherigen Schritt erstellt haben. Die Richtlinieneinstellungen zum Ausschließen von Benutzern finden Sie unter **UserConfiguration\\Administrative Templates\\Windows Components\\MDOP MBAM (BitLocker-Verwaltung)**.

3.  Nachdem Sie eine Sicherheitsgruppe für von BitLocker freigestellten Benutzern erstellt haben, fügen Sie dieser Gruppe die Namen der Benutzer hinzu, die eine Ausnahmegenehmigung anfordern. Wenn sich Benutzer an einem Computer anmelden, der von BitLocker gesteuert wird, überprüft der MBAM-Client die Einstellung für die Benutzer Freistellungs Richtlinie und unterbricht den Schutz, je nachdem, ob der Benutzer Teil der BitLocker-Ausnahme Sicherheitsgruppe ist.

    **Wichtig**  Szenarien mit freigegebenen Computern erfordern besondere Berücksichtigung bei der Verwendung von Ausnahmen für Benutzer. Wenn sich ein nicht ausgenommener Benutzer an einem Computer anmeldet, der für einen ausgenommenen Benutzer freigegeben wurde, kann der Computer verschlüsselt sein.

     

**So ermöglichen Sie Benutzern das Anfordern einer Ausnahme von der BitLocker-Verschlüsselung**

1.  Wenn Sie Benutzer Freistellungs Richtlinien mithilfe der MBAM-Richtlinienvorlage konfiguriert haben, kann ein Benutzer eine Ausnahme vom BitLocker-Schutz über den MBAM-Client anfordern.

2.  Wenn sich Benutzer an einem Computer anmelden, der verschlüsselt werden muss, erhalten Sie eine Benachrichtigung, dass Ihr Computer verschlüsselt wird. Sie können die **Anforderungs Befreiung** auswählen und die Verschlüsselung verschieben, indem Sie **später**auswählen, oder " **Start** " auswählen, um die BitLocker-Verschlüsselung zu übernehmen.

    **Hinweis**  Wenn Sie die **ausnahmeanforderung** auswählen, wird der BitLocker-Schutz so lange verschoben, bis die maximale Zeitdauer in der Benutzer Freistellungs Richtlinie festgesetzt ist.

     

3.  Wenn Benutzer die Option **Befreiung anfordern**auswählen, erhalten Sie eine Benachrichtigung, in der Sie aufgefordert werden, sich an die BitLocker-Verwaltungsgruppe Ihrer Organisation zu wenden. Je nachdem, wie die Richtlinie für die Benutzer Freistellung konfigurieren konfiguriert ist, werden Benutzern mindestens eine der folgenden Kontaktmethoden zur Verfügung gestellt:

    -   Telefonnummer

    -   URL der Webseite

    -   Postanschrift

    Nachdem die ausnahmeanforderung eingegangen ist, kann der MBAM-Administrator entscheiden, ob der Benutzer zur BitLocker-Ausnahme Active Directory-Gruppe hinzugefügt werden sollte.

    **Hinweis**  Sobald ein Benutzer eine ausnahmeanforderung übermittelt hat, meldet der MBAM-Agent den Benutzer als "vorübergehend ausgenommen" und wartet dann eine konfigurierbare Anzahl von Tagen, bevor er die Konformität des Computers erneut überprüft. Wenn der MBAM-Administrator die ausnahmeanforderung ablehnt, wird die Option "ausnahmeanforderung" deaktiviert, wodurch verhindert wird, dass der Benutzer die Ausnahme erneut anfordern kann.

     

## Verwandte Themen


[Verwalten von MBAM 2.0-Funktionen](administering-mbam-20-features-mbam-2.md)

 

 





