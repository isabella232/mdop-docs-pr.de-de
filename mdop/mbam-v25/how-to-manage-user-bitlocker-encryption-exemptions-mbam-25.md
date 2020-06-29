---
title: So verwalten Sie BitLocker-Verschlüsselungsausnahmen für Benutzer
description: So verwalten Sie BitLocker-Verschlüsselungsausnahmen für Benutzer
author: dansimp
ms.assetid: f582ab82-5bb5-4cd3-ad7c-483240533cf9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c4224a0fb6d905c2362659efe7cf05e16756f7c0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811968"
---
# So verwalten Sie BitLocker-Verschlüsselungsausnahmen für Benutzer


Mit Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) können Sie Benutzer von den BitLocker-Laufwerk Verschlüsselungsanforderungen ausschließen.

Um Benutzer vom BitLocker-Schutz zu befreien, müssen Sie Folgendes tun:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Aufgabe</th>
<th align="left">Details</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Erstellen einer Infrastruktur zur Unterstützung von befreiten Benutzern</p></td>
<td align="left"><p>Beispiele für diese Infrastruktur sind die Bereitstellung von Benutzern mit einer Kontakt Telefonnummer, einer Webseite oder einer Postanschrift, die Sie verwenden können, um eine Ausnahme zu beantragen.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Hinzufügen des befreiten Benutzers zu einer Sicherheitsgruppe für ein Gruppenrichtlinienobjekt, das speziell für befreite Benutzer konfiguriert ist.</p></td>
<td align="left"><p>Wenn sich Mitglieder dieser Sicherheitsgruppe bei einem Computer anmelden, wird der Benutzer durch die Gruppenrichtlinieneinstellung des Benutzers vom BitLocker-Schutz ausgenommen. Die Gruppenrichtlinieneinstellung des Benutzers überschreibt die Computerrichtlinie, und der Computer bleibt von der BitLocker-Verschlüsselung ausgenommen.</p>
<div class="alert">
<strong>Hinweis:</strong><br/><p>MBAM erlässt die Verschlüsselungsrichtlinie nicht, wenn der Computer bereits BitLocker-geschützt ist und der Benutzer freigestellt ist. Wenn ein anderer Benutzer, der nicht von der Verschlüsselungsrichtlinie ausgenommen ist, sich auf dem Computer anmeldet, wird jedoch die Verschlüsselung durchgeführt.</p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



In den folgenden Schritten wird beschrieben, was geschieht, wenn Endbenutzer eine Ausnahme vom BitLocker-Laufwerk-Verschlüsselungs Befreiungsprozess über den MBAM-Client oder über den von Ihrer Organisation verwendeten Prozess anfordern. Sie müssen die MBAM-Gruppenrichtlinieneinstellungen so konfigurieren, dass Endbenutzer eine Ausnahme von der BitLocker-Laufwerkverschlüsselung anfordern können.

1.  Wenn sich Endbenutzer bei einem Computer anmelden, der verschlüsselt werden muss, erhalten Sie eine Benachrichtigung, dass Ihr Computer verschlüsselt wird. Sie können die **Anforderungs Befreiung** auswählen und die Verschlüsselung verschieben, indem Sie **verschieben**auswählen, oder Sie können **Verschlüsselung starten** auswählen, um die BitLocker-Verschlüsselung zu akzeptieren.

    **Hinweis:**  
    Wenn Sie die **ausnahmeanforderung** auswählen, wird der BitLocker-Schutz so lange verschoben, bis die maximale Zeitdauer in der Benutzer Freistellungs Richtlinie festgesetzt ist.



2.  Wenn Endbenutzer die Option **Befreiung anfordern**auswählen, erhalten Sie eine Benachrichtigung, in der Sie aufgefordert werden, sich an die BitLocker-Verwaltungsgruppe der Organisation zu wenden. Je nachdem, wie die **Richtlinie für die Benutzer Freistellung konfigurieren** konfiguriert ist, werden Benutzern mindestens eine der folgenden Kontaktmethoden zur Verfügung gestellt:

    -   Telefonnummer

    -   URL der Webseite

    -   Postanschrift

3.  Nachdem die ausnahmeanforderung eingegangen ist, entscheidet der MBAM-Administrator, ob der Benutzer der BitLocker-Ausnahmegruppe Active Directory-Domänendienste (AD DS) hinzugefügt werden soll.

4.  Nachdem ein Endbenutzer eine ausnahmeanforderung eingereicht hat, meldet der MBAM-Client den Benutzer als "vorübergehend ausgenommen". Der Client wartet dann eine festgelegte Anzahl von Tagen, die von den IT-Administratoren konfiguriert werden, bevor er die Konformität des Computers erneut überprüft. Wenn der MBAM-Administrator die ausnahmeanforderung ablehnt, wird die Option "ausnahmeanforderung" deaktiviert, wodurch verhindert wird, dass der Benutzer die Befreiung erneut anfordert.

Mit Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) können Sie Benutzer von den BitLocker-Laufwerk Verschlüsselungsanforderungen ausschließen.

Um Benutzer vom BitLocker-Schutz zu befreien, müssen Sie Folgendes tun:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Aufgabe</th>
<th align="left">Details</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Erstellen einer Infrastruktur zur Unterstützung von befreiten Benutzern</p></td>
<td align="left"><p>Beispiele für diese Infrastruktur sind die Bereitstellung von Benutzern mit einer Kontakt Telefonnummer, einer Webseite oder einer Postanschrift, die Sie verwenden können, um eine Ausnahme zu beantragen.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Hinzufügen des befreiten Benutzers zu einer Sicherheitsgruppe für ein Gruppenrichtlinienobjekt, das speziell für befreite Benutzer konfiguriert ist.</p></td>
<td align="left"><p>Wenn sich Mitglieder dieser Sicherheitsgruppe bei einem Computer anmelden, wird der Benutzer durch die Gruppenrichtlinieneinstellung des Benutzers vom BitLocker-Schutz ausgenommen. Die Gruppenrichtlinieneinstellung des Benutzers überschreibt die Computerrichtlinie, und der Computer bleibt von der BitLocker-Verschlüsselung ausgenommen.</p>
<div class="alert">
<strong>Hinweis:</strong><br/><p>Wenn der Computer bereits mit BitLocker geschützt ist, hat die Richtlinie für die Benutzer Befreiung keine Auswirkungen. Darüber hinaus erfolgt die Verschlüsselung, wenn sich ein anderer Benutzer an einem Computer anmeldet, der nicht von der Verschlüsselungsrichtlinie ausgenommen ist.</p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



In den folgenden Schritten wird beschrieben, was geschieht, wenn Endbenutzer eine Ausnahme vom BitLocker-Laufwerk-Verschlüsselungs Befreiungsprozess über den MBAM-Client oder über den von Ihrer Organisation verwendeten Prozess anfordern. Sie müssen die MBAM-Gruppenrichtlinieneinstellungen so konfigurieren, dass Endbenutzer eine Ausnahme von der BitLocker-Laufwerkverschlüsselung anfordern können.

1.  Wenn sich Endbenutzer bei einem Computer anmelden, der verschlüsselt werden muss, erhalten Sie eine Benachrichtigung, dass Ihr Computer verschlüsselt wird. Sie können die **Anforderungs Befreiung** auswählen und die Verschlüsselung verschieben, indem Sie **verschieben**auswählen, oder Sie können **Verschlüsselung starten** auswählen, um die BitLocker-Verschlüsselung zu akzeptieren.

    **Hinweis:**  
    Wenn Sie die **ausnahmeanforderung** auswählen, wird der BitLocker-Schutz so lange verschoben, bis die maximale Zeitdauer in der Benutzer Freistellungs Richtlinie festgesetzt ist.



2.  Wenn Endbenutzer die Option **Befreiung anfordern**auswählen, erhalten Sie eine Benachrichtigung, in der Sie aufgefordert werden, sich an die BitLocker-Verwaltungsgruppe der Organisation zu wenden. Je nachdem, wie die **Richtlinie für die Benutzer Freistellung konfigurieren** konfiguriert ist, werden Benutzern mindestens eine der folgenden Kontaktmethoden zur Verfügung gestellt:

    -   Telefonnummer

    -   URL der Webseite

    -   Postanschrift

3.  Nachdem die ausnahmeanforderung eingegangen ist, entscheidet der MBAM-Administrator, ob der Benutzer der BitLocker-Ausnahmegruppe Active Directory-Domänendienste (AD DS) hinzugefügt werden soll.

4.  Nachdem ein Endbenutzer eine ausnahmeanforderung eingereicht hat, meldet der MBAM-Client den Benutzer als "vorübergehend ausgenommen". Der Client wartet dann eine festgelegte Anzahl von Tagen, die von den IT-Administratoren konfiguriert werden, bevor er die Konformität des Computers erneut überprüft. Wenn der MBAM-Administrator die ausnahmeanforderung ablehnt, wird die Option "ausnahmeanforderung" deaktiviert, wodurch verhindert wird, dass der Benutzer die Befreiung erneut anfordert.

**So nehmen Sie einen Benutzer von der BitLocker-Laufwerkverschlüsselung frei**

1.  Erstellen Sie eine AD DS-Sicherheitsgruppe, die verwendet wird, um Benutzer Ausnahmen von BitLocker-Verschlüsselungsanforderungen zu verwalten.

2.  Erstellen Sie ein Gruppenrichtlinienobjekt mithilfe der Gruppenrichtlinienvorlagen für Microsoft BitLocker-Verwaltung und-Überwachung.

3.  Ordnen Sie das Gruppenrichtlinienobjekt der AD DS-Gruppe zu, die Sie im vorherigen Schritt erstellt haben. Die Richtlinieneinstellungen, um Benutzer zu befreien, finden Sie unter: **UserConfiguration** &gt; **Administrative Templates** &gt; **Windows Components** &gt; **MDOP MBAM (BitLocker-Verwaltung)**.

4.  Fügen Sie der Sicherheitsgruppe, die Sie für BitLocker-Ausgeschlossene Benutzer erstellt haben, die Namen der Benutzer hinzu, die eine Befreiung anfordern.

    Wenn sich ein Benutzer bei einem von BitLocker kontrollierten Computer anmeldet, überprüft der MBAM-Client die Einstellung für die Benutzer Freistellungs Richtlinie. Wenn der Computer bereits verschlüsselt ist, wird der BitLocker-Schutz nicht angehalten. Wenn der Computer nicht verschlüsselt ist, fordert MBAM den Benutzer nicht auf zu verschlüsseln.

    **Wichtig**  
    Szenarien mit freigegebenen Computern erfordern besondere Berücksichtigung, wenn Sie BitLocker-Benutzer Ausnahmen verwenden. Wenn sich ein nicht ausgenommener Benutzer an einem Computer anmeldet, der für einen ausgenommenen Benutzer freigegeben wurde, kann der Computer verschlüsselt sein.




## Verwandte Themen


[Verwalten von MBAM 2.5-Funktionen](administering-mbam-25-features.md)

[Planen der Gruppenrichtlinienanforderungen für MBAM 2.5](planning-for-mbam-25-group-policy-requirements.md)




## Sie haben einen Vorschlag für MBAM?
- [Hier](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)können Sie Vorschläge hinzufügen oder abstimmen. 
- Bei MBAM-Problemen verwenden Sie das [MBAM TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).




