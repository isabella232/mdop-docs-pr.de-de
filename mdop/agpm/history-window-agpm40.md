---
title: Verlaufsfenster
description: Verlaufsfenster
author: dansimp
ms.assetid: 5bea62e7-d267-40b2-a66d-fb1be7373a1c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 81f19e3834e945a45238856e23f6ee4a86407c4a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808448"
---
# Verlaufsfenster


Der Verlauf eines Gruppenrichtlinienobjekts (GPO) kann angezeigt werden, indem Sie auf ein GPO doppelklicken oder mit der rechten Maustaste auf ein GPO und dann auf **Verlauf**klicken. Darüber hinaus wird es in der Gruppenrichtlinien-Verwaltungskonsole (Group Policy Management Console, GPMC) als Registerkarte für jedes GPO angezeigt.

Das Protokoll enthält eine Aufzeichnung der Ereignisse in der Lebensdauer des ausgewählten Gruppenrichtlinienobjekts. Im Fenster " **Verlauf** " können Sie einen Bericht über die Einstellungen in einer Version des Gruppenrichtlinienobjekts abrufen, mehrere Versionen eines GPO vergleichen oder auf eine frühere Version eines GPO zurückgreifen.

## Filtern von Ereignissen im Verlaufsfenster


Die Registerkarten im **Verlaufs** Fenster filtern die Zustände im Verlauf des Gruppenrichtlinienobjekts.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Tabs</th>
<th align="left">Filterung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Alle Zustände</strong></p></td>
<td align="left"><p>Zeigt alle Zustände im Verlauf des Gruppenrichtlinienobjekts an.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Eindeutige Versionen</strong></p></td>
<td align="left"><p>Zeigt nur eindeutige Versionen des in das Archiv eingecheckten Gruppenrichtlinienobjekts an. Die Version, die in der Produktionsumgebung bereitgestellt wird, Verknüpfungen zu eindeutigen Versionen und Informationsstatus werden in dieser Liste ausgelassen.</p></td>
</tr>
</tbody>
</table>



## Ereignisinformationen


Informationen werden für jeden Zustand im Verlauf des Gruppenrichtlinienobjekts bereitgestellt.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">GPO-Attribut</th>
<th align="left">Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Datum ändern</strong></p></td>
<td align="left"><p>Der Zeitstempel des Vorgangs, in dem die Aktion in der <strong> Spalte "Zustand" </strong> ausgeführt wurde.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Status</strong></p></td>
<td align="left"><p>Ein Zustand im Verlauf des Gruppenrichtlinienobjekts.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Geändert von</strong></p></td>
<td align="left"><p>Die Person, die das Gruppenrichtlinienobjekt eingecheckt oder bereitgestellt hat.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Kommentar</strong></p></td>
<td align="left"><p>Ein Kommentar, der von der Person eingegeben wurde, die zu dem Zeitpunkt, zu dem diese Version geändert wurde, ein GPO eingecheckt oder bereitgestellt hat, um die Besonderheiten der Version zu identifizieren, wenn ein Rollback auf eine frühere Version erforderlich ist.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Löschbar</strong></p></td>
<td align="left"><p>Ob diese Version des Gruppenrichtlinienobjekts gelöscht werden kann, wenn die Anzahl der eindeutigen Versionen jedes im Archiv aufbewahrten Gruppenrichtlinienobjekts limitiert ist.</p>
<div class="alert">
<strong>Hinweis:</strong><br/><p>Sie können ändern, ob eine Version eines GPO gelöscht werden kann, indem Sie mit der rechten Maustaste auf das Gruppenrichtlinienobjekt klicken und dann auf " <strong> Löschen" </strong> oder "Löschen zulassen" klicken <strong> </strong> .</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Computer Version</strong></p></td>
<td align="left"><p>Automatisch generierte Version des Computer Konfigurations Teils des Gruppenrichtlinienobjekts.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Benutzer Version</strong></p></td>
<td align="left"><p>Automatisch generierte Version des Benutzer Konfigurations Teils des Gruppenrichtlinienobjekts.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>GPO-Status</strong></p></td>
<td align="left"><p>Die Computer Konfiguration und die Benutzerkonfiguration können separat verwaltet werden. Dieser Status zeigt an, welche Teile des Gruppenrichtlinienobjekts aktiviert sind.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Quell-GPO-Informationen</strong></p></td>
<td align="left"><p>Für ein Gruppenrichtlinienobjekt, das aus einer anderen Gesamtstruktur importiert wurde, den ursprünglichen Namen, die Domäne sowie den Benutzer und das Datum, die der letzten Änderung zugeordnet sind.</p></td>
</tr>
</tbody>
</table>



## Berichte


Auf den Schaltflächen **Einstellungen** und **Unterschiede** werden Berichte zu den GPO-Einstellungen für die ausgewählte GPO-Version oder Versionen angezeigt. Darüber hinaus bietet das Klicken mit der rechten Maustaste auf eine GPO-Version oder-Version die Möglichkeit, XML-basierte Berichte anzuzeigen.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Button</th>
<th align="left">Effekt</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Einstellungen</strong></p></td>
<td align="left"><p>Einen HTML-basierten Bericht generieren, in dem die Einstellungen in der ausgewählten Version des Gruppenrichtlinienobjekts angezeigt werden.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Unterschiede</strong></p></td>
<td align="left"><p>Generieren eines HTML-basierten Berichts, der die Einstellungen in mehreren ausgewählten Versionen des Gruppenrichtlinienobjekts vergleicht.</p></td>
</tr>
</tbody>
</table>



### Schlüssel für Unterschiedsberichte

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Symbol</th>
<th align="left">Bedeutung</th>
<th align="left">Farbe</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Keine</p></td>
<td align="left"><p>Element mit identischen Einstellungen in beiden GPOs vorhanden</p></td>
<td align="left"><p>Variiert je nach Ebene</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>[#]</strong></p></td>
<td align="left"><p>Element ist in beiden GPOs vorhanden, jedoch mit geänderten Einstellungen</p></td>
<td align="left"><p>Blaue</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>[-]</strong></p></td>
<td align="left"><p>Element ist nur im ersten GPO vorhanden</p></td>
<td align="left"><p>Rot</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>[+]</strong></p></td>
<td align="left"><p>Element ist nur im zweiten GPO vorhanden</p></td>
<td align="left"><p>Grün</p></td>
</tr>
</tbody>
</table>



-   Bei Elementen mit geänderten Einstellungen werden die geänderten Einstellungen identifiziert, wenn das Element erweitert wird. Der Wert für das Attribut in den einzelnen Gruppenrichtlinienobjekten wird in der Reihenfolge angezeigt, in der die GPOs im Bericht angezeigt werden.

-   Einige Änderungen an Einstellungen können dazu führen, dass ein Element als zwei Elemente gemeldet wird (eines ist nur im ersten GPO vorhanden, das nur in der zweiten vorhanden ist), anstatt eines Elements, das sich geändert hat.

### Weitere Verweise

-   [Registerkarte "Inhalt"](contents-tab-agpm40.md)









