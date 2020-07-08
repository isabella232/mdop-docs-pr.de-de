---
title: Vorlagenbefehle
description: Vorlagenbefehle
author: dansimp
ms.assetid: 243a9b18-bf3f-44fa-94d7-5c793f7322da
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2c540bf87462f501a4db5596faca43ef66ee8558
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807447"
---
# Vorlagenbefehle


Registerkarte " **Vorlagen** ":

-   Zeigt eine Liste der verfügbaren Vorlagen an, die Sie zum Erstellen neuer Gruppenrichtlinienobjekte (Group Policy Objects, GPOs) verwenden können.

-   Bietet ein Kontextmenü mit Befehlen zum Erstellen eines Gruppenrichtlinienobjekts auf der Grundlage einer ausgewählten Vorlage, zum Verwalten von Vorlagen und zum Anzeigen von Berichten für Vorlagen.

-   Zeigt eine Liste der Gruppen und Benutzer an, die über die Berechtigung zum Zugriff auf eine ausgewählte Vorlage verfügen.

Da eine Vorlage nicht geändert werden kann, haben Vorlagen keinen Verlauf. Wie bei allen GPO-Versionen können die Einstellungen einer Vorlage jedoch mit einem Einstellungsbericht angezeigt oder mit einem anderen Gruppenrichtlinienobjekt mit einem Differenz Bericht verglichen werden.

**Hinweis**  Eine Vorlage ist eine nicht bearbeitbare, statische Version eines GPO, die als Ausgangspunkt zum Erstellen neuer, bearbeitbarer GPOs verwendet werden kann.

 

Wenn Sie mit der rechten Maustaste auf die Liste der **Gruppenrichtlinienobjekte** auf dieser Registerkarte klicken, wird ein Kontextmenü angezeigt, einschließlich der jeweils folgenden Optionen.

## Steuerelement


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Befehl</th>
<th align="left">Effekt</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Neues gesteuertes Gruppenrichtlinienobjekt</strong></p></td>
<td align="left"><p>Erstellen eines neuen Gruppenrichtlinienobjekts auf der Grundlage der ausgewählten Vorlage Die Option zum Bereitstellen des neuen Gruppenrichtlinienobjekts in der Produktionsumgebung der Domäne wird bereitgestellt. Wenn Sie nicht über die Berechtigung zum Erstellen eines Gruppenrichtlinienobjekts verfügen, werden Sie aufgefordert, eine Anforderung zu senden. (Diese Option wird angezeigt, wenn beim Klicken mit der rechten Maustaste auf die <strong> Liste der Gruppenrichtlinienobjekte </strong> .)</p></td>
</tr>
</tbody>
</table>

 

## Berichte


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Befehl</th>
<th align="left">Effekt</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Einstellungen</strong></p></td>
<td align="left"><p>Generieren eines HTML-basierten oder XML-basierten Berichts, in dem die Einstellungen des ausgewählten Gruppenrichtlinienobjekts angezeigt werden.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Unterschiede</strong></p></td>
<td align="left"><p>Generieren eines HTML-basierten oder XML-basierten Berichts, der die Einstellungen in zwei ausgewählten GPO-Vorlagen vergleicht</p></td>
</tr>
</tbody>
</table>

 

## Vorlagenverwaltung


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Befehl</th>
<th align="left">Effekt</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Als Standard festlegen</strong></p></td>
<td align="left"><p>Die ausgewählte Vorlage als Standard festlegen, der beim Erstellen eines neuen Gruppenrichtlinienobjekts automatisch verwendet werden soll.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Delete</strong></p></td>
<td align="left"><p>Verschieben der ausgewählten Vorlage in den <strong> Papierkorb </strong> Wenn Sie nicht über die Berechtigung zum Löschen eines Gruppenrichtlinienobjekts verfügen, werden Sie aufgefordert, eine Anforderung zu senden.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Rename</strong></p></td>
<td align="left"><p>Ändern des Namens der ausgewählten Vorlage</p></td>
</tr>
</tbody>
</table>

 

## Verschiedenes


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Befehl</th>
<th align="left">Effekt</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Aktualisieren</strong></p></td>
<td align="left"><p>Aktualisieren Sie die Anzeige der Gruppenrichtlinien-Verwaltungskonsole, um alle Änderungen einzubeziehen. Einige Änderungen werden erst angezeigt, wenn die Anzeige aktualisiert wird.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Hilfe</strong></p></td>
<td align="left"><p>Anzeigen der Hilfe für erweiterte Gruppenrichtlinienverwaltung (AGPM)</p></td>
</tr>
</tbody>
</table>

 

### Weitere Verweise

-   [Registerkarte "Inhalt"](contents-tab-agpm40.md)

-   [Durchführen von Editor-Aufgaben](performing-editor-tasks-agpm40.md)

-   [Durchführen von Prüferaufgaben](performing-reviewer-tasks-agpm40.md)

 

 





