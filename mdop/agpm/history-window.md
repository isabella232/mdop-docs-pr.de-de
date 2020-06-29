---
title: Verlaufsfenster
description: Verlaufsfenster
author: dansimp
ms.assetid: f11f9ad9-bffe-4c56-8c46-fe9c0a8e55c1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 02b4336409f33d6c1f2868bceb22cb95120f2198
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808447"
---
# Verlaufsfenster


Der Verlauf eines Gruppenrichtlinienobjekts (GPO) kann angezeigt werden, indem Sie auf ein GPO doppelklicken oder mit der rechten Maustaste auf ein GPO und dann auf **Verlauf**klicken. Darüber hinaus wird es in der **Gruppenrichtlinien-Verwaltungskonsole (Group Policy Management Console** , GPMC) als Registerkarte für jedes GPO angezeigt.

Das Protokoll enthält eine Liste aller Versionen des ausgewählten GPO, die im Archiv gespeichert sind. Im Fenster " **Verlauf** " können Sie einen Bericht über die Einstellungen in einem Gruppenrichtlinienobjekt abrufen, mehrere Versionen eines GPO vergleichen oder auf eine frühere Version eines GPO zurückgreifen.

## Filtern von Ereignissen im Verlaufsfenster


Die Registerkarten im **Verlaufs** Fenster filtern die angezeigten Ereignisse.

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
<td align="left"><p><strong>Alle anzeigen</strong></p></td>
<td align="left"><p>Anzeigen aller Versionen des Gruppenrichtlinienobjekts</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Eingecheckt</strong></p></td>
<td align="left"><p>Anzeigen nur eingecheckter Versionen des Gruppenrichtlinienobjekts Die bereitgestellte Version wird in dieser Liste ausgelassen.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Nur Etiketten</strong></p></td>
<td align="left"><p>Nur GPOs anzeigen, denen Beschriftungen zugeordnet sind.</p></td>
</tr>
</tbody>
</table>

 

## Ereignisinformationen


Für jedes Ereignis im Verlauf des ausgewählten Gruppenrichtlinienobjekts werden Informationen bereitgestellt.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">GPO-Merkmal</th>
<th align="left">Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Computer</strong></p></td>
<td align="left"><p>Automatisch generierte Version des Computer Konfigurations Teils des Gruppenrichtlinienobjekts.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Benutzer</strong></p></td>
<td align="left"><p>Automatisch generierte Version des Benutzer Konfigurations Teils des Gruppenrichtlinienobjekts.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Zeit</strong></p></td>
<td align="left"><p>Timestamp der Version des Gruppenrichtlinienobjekts, wenn die Aktion im Feld Status durchgeführt wurde.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Status</strong></p></td>
<td align="left"><p>Der Status der ausgewählten Version des Gruppenrichtlinienobjekts:</p>
<p><img src="images/36f6b687-f5cc-40d1-805f-b191d1fb1ace.gif" alt="Deployed GPO icon" /> <strong>Bereitgestellt </strong> : Diese Version des Gruppenrichtlinienobjekts befindet sich derzeit in der Produktionsumgebung.</p>
<p><img src="images/57b610a5-1c71-4d26-9173-d04abd495fcc.gif" alt="Checked in GPO icon" /> <strong>Eingecheckt </strong> : Diese Version des Gruppenrichtlinienobjekts steht autorisierten Editoren zum Auschecken zur Bearbeitung oder zum Bereitstellen eines Gruppenrichtlinienadministrators zur Verfügung.</p>
<p><img src="images/8e7a7c4e-809a-435a-8b29-30d797936210.gif" alt="Checked out GPO icon" /> <strong>Ausgecheckt </strong> : Diese Version des Gruppenrichtlinienobjekts ist derzeit von einem Editor ausgecheckt und steht für andere Editoren nicht zur Verfügung. (Der Status "ausgecheckt" wird im <strong> Protokoll </strong> , außer um anzugeben, ob ein GPO zurzeit ausgecheckt ist.)</p>
<p><img src="images/327623bd-0842-4372-be1f-bdc4b8c3481c.gif" alt="Created GPO icon" /> <strong>Erstellt </strong> : gibt das Datum und die Uhrzeit der anfänglichen Erstellung des Gruppenrichtlinienobjekts an.</p>
<p><img src="images/8356fcdc-1279-425b-ab14-a23bcfe391da.gif" alt="Labeled GPO icon" /> <strong>Gekennzeichnet </strong> : gibt eine beschriftete Version des Gruppenrichtlinienobjekts an.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>GPO-Status</strong></p></td>
<td align="left"><p>Die Computer Konfiguration und die Benutzerkonfiguration können separat verwaltet werden. Dieser Status zeigt an, welche Teile des Gruppenrichtlinienobjekts aktiviert sind.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Besitzer</strong></p></td>
<td align="left"><p>Die Person, die das Gruppenrichtlinienobjekt eingecheckt oder bereitgestellt hat.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Kommentar</strong></p></td>
<td align="left"><p>Ein Kommentar, der vom Besitzer eines Gruppenrichtlinienobjekts zu dem Zeitpunkt eingegeben wurde, zu dem diese Version geändert wurde. Nützlich, um die Besonderheiten der Version zu identifizieren, falls ein Rollback auf eine vorherige Version erforderlich ist.</p></td>
</tr>
</tbody>
</table>

 

## Berichte


Je nachdem, ob eine einzelne GPO-Version oder mehrere GPO-Versionen ausgewählt sind, werden auf den Schaltflächen **Einstellungen** und **Unterschiede** Berichte zu den GPO-Einstellungen angezeigt. Mit der rechten Maustaste auf GPO-Versionen können auch XML-basierte Berichte angezeigt werden.

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

-   [Registerkarte "Inhalt"](contents-tab.md)

 

 





