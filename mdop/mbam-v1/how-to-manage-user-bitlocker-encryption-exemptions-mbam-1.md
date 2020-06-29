---
title: So verwalten Sie BitLocker-Verschlüsselungsausnahmen für Benutzer
description: So verwalten Sie BitLocker-Verschlüsselungsausnahmen für Benutzer
author: dansimp
ms.assetid: 48d69721-504f-4524-8a04-b9ce213ac9b4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8c3d70558a65c3288174413d6c36cc9c77bc9eaa
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804622"
---
# So verwalten Sie BitLocker-Verschlüsselungsausnahmen für Benutzer


Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) kann zum Verwalten des BitLocker-Schutzes verwendet werden, indem Benutzer freigestellt werden, die Ihre Laufwerke nicht verschlüsseln müssen oder möchten.

Um Benutzer vom BitLocker-Schutz zu befreien, muss eine Organisation zunächst eine Infrastruktur zur Unterstützung derartiger Ausnahmen erstellen. Die unterstützende Infrastruktur kann eine Kontakt Telefonnummer, eine Webseite oder eine Postanschrift enthalten, um eine Befreiung zu beantragen. Darüber hinaus muss jeder befreite Benutzer einer Sicherheitsgruppe für Gruppenrichtlinien hinzugefügt werden, die speziell für befreite Benutzer erstellt wurden. Wenn sich Mitglieder dieser Sicherheitsgruppe an einem Computer anmelden, zeigt die Benutzergruppenrichtlinie an, dass der Benutzer vom BitLocker-Schutz ausgenommen ist. Die Benutzerrichtlinie überschreibt die Computerrichtlinie, und der Computer bleibt von der BitLocker-Verschlüsselung ausgenommen.

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
<td align="left"><p>Der BitLocker-Schutz wird auf dem Computer erzwungen.</p></td>
<td align="left"><p>Der BitLocker-Schutz wird auf dem Computer nicht erzwungen.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Benutzer freigestellt</strong></p></td>
<td align="left"><p>Der BitLocker-Schutz wird auf dem Computer nicht erzwungen.</p></td>
<td align="left"><p>Der BitLocker-Schutz wird auf dem Computer nicht erzwungen.</p></td>
</tr>
</tbody>
</table>

 

**So nehmen Sie einen Benutzer von der BitLocker-Verschlüsselung frei**

1.  Erstellen Sie eine ActiveDirectoryDomainServices-Sicherheitsgruppe, die verwendet wird, um Benutzer Ausnahmen von der BitLocker-Verschlüsselung zu verwalten.

2.  Erstellen Sie eine Gruppenrichtlinienobjekteinstellung mithilfe der MBAM-Gruppenrichtlinienvorlage. Ordnen Sie das Gruppenrichtlinienobjekt der Active Directory-Gruppe zu, die Sie im vorherigen Schritt erstellt haben. Weitere Informationen zu den erforderlichen Richtlinieneinstellungen, mit denen Benutzer die Befreiung von der BitLocker-Verschlüsselung anfordern können, finden Sie im Abschnitt Konfigurieren von Benutzer Freistellungs Richtlinien unter [Planen der MBAM 1,0-Gruppenrichtlinienanforderungen](planning-for-mbam-10-group-policy-requirements.md).

3.  Nachdem Sie eine Sicherheitsgruppe für von BitLocker freigestellten Benutzern erstellt haben, fügen Sie dieser Gruppe die Namen der Benutzer hinzu, die eine Befreiung anfordern. Wenn sich ein Benutzer bei einem von BitLocker gesteuerten Computer anmeldet, überprüft der MBAM-Client die Richtlinieneinstellung für die Benutzer Befreiung und unterbricht den Schutz, je nachdem, ob der Benutzer Teil der BitLocker-Ausnahme Sicherheitsgruppe ist.

    **Hinweis**  Szenarien für gemeinsam genutzte Computer erfordern besondere Rücksicht auf die Benutzer Befreiung. Wenn sich ein nicht ausgenommener Benutzer an einem Computer anmeldet, der für einen ausgenommenen Benutzer freigegeben wurde, kann der Computer verschlüsselt sein.

     

**So ermöglichen Sie Benutzern das Anfordern einer Ausnahme von der BitLocker-Verschlüsselung**

1.  Nachdem Sie die Richtlinien für die Benutzer Befreiung durch usingwith der MBAM-Richtlinienvorlage konfiguriert haben, kann ein Benutzer eine Befreiung vom BitLocker-Schutz über den MBAM-Client anfordern.

2.  Wenn sich ein Benutzer an einem Computer anmeldet, der in der MBAM-Hardware Kompatibilitätsliste als **kompatibel** gekennzeichnet ist, zeigt das System dem Benutzer eine Benachrichtigung an, dass der Computer verschlüsselt werden soll. Der Benutzer kann **Anforderungs Befreiung** auswählen und die Verschlüsselung verschieben, indem er **später**auswählt, oder wählen Sie **Start** aus, um die BitLocker-Verschlüsselung zu übernehmen.

    **Hinweis**  Wenn Sie die Option **Befreiung anfordern** auswählen, wird der BitLocker-Schutz so lange verschoben, bis die maximale Zeit in der Benutzer Freistellungs Richtlinie gesetzt ist.

     

3.  Wenn ein Benutzer die **Anforderungs Befreiung**auswählt, wird der Benutzer benachrichtigt, wenn er sich an die BitLocker-Verwaltungsgruppe der Organisation wenden möchte. Je nachdem, wie die Richtlinie für die Benutzer Freistellung konfigurieren konfiguriert ist, werden Benutzern mindestens eine der folgenden Kontaktmethoden zur Verfügung gestellt:

    -   Telefonnummer

    -   URL der Webseite

    -   Postanschrift

    Nach der Übermittlung der Anforderung kann der MBAM-Administrator entscheiden, ob der Benutzer zur BitLocker-Ausnahmegruppe Active Directory hinzugefügt werden soll.

    **Hinweis**  Nachdem die Beschränkungs Frist für die Benutzer Freistellungs Richtlinie abgelaufen ist, wird den Benutzern die Option zum Anfordern einer Ausnahme von der Verschlüsselungsrichtlinie nicht angezeigt. An diesem Punkt müssen Benutzer sich direkt mit dem MBAM-Administrator in Verbindung setzen, um eine Ausnahme vom BitLocker-Schutz zu erhalten.

     

## Verwandte Themen


[Verwalten von MBAM 1.0-Funktionen](administering-mbam-10-features.md)

 

 





