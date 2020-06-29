---
title: Verlaufsfenster
description: Verlaufsfenster
author: dansimp
ms.assetid: 114f50a4-508d-4589-b006-6cd05cffe6b7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 81911b5103c76e267d806fb7cd8acf55811440c9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808451"
---
# Verlaufsfenster


Der Verlauf eines Gruppenrichtlinienobjekts (GPO) kann angezeigt werden, indem Sie auf ein GPO doppelklicken oder mit der rechten Maustaste auf ein GPO und dann auf **Verlauf**klicken. Darüber hinaus wird es in der **Gruppenrichtlinien-Verwaltungskonsole (Group Policy Management Console** , GPMC) als Registerkarte für jedes GPO angezeigt.

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
<td align="left"><p>Ein Kommentar, der von der Person eingegeben wurde, die zum Zeitpunkt der Änderung dieser Version ein GPO eingecheckt oder bereitgestellt hat. Nützlich, um die Besonderheiten der Version zu identifizieren, falls ein Rollback auf eine vorherige Version erforderlich ist.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Löschbar</strong></p></td>
<td align="left"><p>Ob diese Version des Gruppenrichtlinienobjekts gelöscht werden kann, wenn die Anzahl der eindeutigen Versionen jedes im Archiv aufbewahrten Gruppenrichtlinienobjekts limitiert ist.</p>
<div class="alert">
<strong>Hinweis:</strong><br/><p>Sie können ändern, ob eine Version eines Gruppenrichtlinienobjekts löschbar ist, indem Sie mit der rechten Maustaste darauf klicken und dann auf " <strong> Löschen" </strong> oder "Löschen zulassen" klicken <strong> </strong> .</p>
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
<td align="left"><p><strong>WMI-Filter</strong></p></td>
<td align="left"><p>Zeigen Sie alle WMI-Filter an, die auf dieses Gruppenrichtlinienobjekt angewendet werden. WMI-Filter werden in der <strong> </strong> Konsolenstruktur der GPMC unter dem Ordner WMI-Filter für die Domäne verwaltet.</p></td>
</tr>
</tbody>
</table>



## Berichte


Auf den Schaltflächen **Einstellungen** und **Unterschiede** werden Berichte zu den GPO-Einstellungen für die ausgewählte GPO-Version oder Versionen angezeigt. Mit der rechten Maustaste auf GPO-Versionen können auch XML-basierte Berichte angezeigt werden.

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

-   Einige Änderungen an Einstellungen können dazu führen, dass ein Element als zwei unterschiedliche Elemente gemeldet wird (eines ist nur im ersten GPO vorhanden, das nur in der zweiten vorhanden ist), und nicht als ein Element, das sich geändert hat.

### Weitere Verweise

-   [Registerkarte "Inhalt"](contents-tab-agpm30ops.md)









