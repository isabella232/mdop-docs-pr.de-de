---
title: Kontrollierte GPO-Befehle
description: Kontrollierte GPO-Befehle
author: dansimp
ms.assetid: 370d3db9-4efc-4799-983d-e29ba5f32b07
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 65e9d06beb4c36762e845e452bab497a8d3da747
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808579"
---
# Kontrollierte GPO-Befehle


Die Registerkarte " **gesteuert** ":

-   Zeigt eine Liste der Gruppenrichtlinienobjekte (Group Policy Objects, GPOs) an, die von der erweiterten Gruppenrichtlinienverwaltung (AGPM) verwaltet werden.

-   Bietet ein Kontextmenü mit Befehlen zum Verwalten von GPOs und zum Anzeigen des Verlaufs und der Berichte für GPOs.

-   Zeigt eine Liste der Gruppen und Benutzer an, die über die Berechtigung zum Zugriff auf ein ausgewähltes Gruppenrichtlinienobjekt verfügen.

Wenn Sie mit der rechten Maustaste auf die Liste der **Gruppenrichtlinienobjekte** auf dieser Registerkarte klicken, wird ein Kontextmenü angezeigt. Dieses Menü enthält die jeweils folgenden Optionen.

## Steuerelement und Verlauf


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
<td align="left"><p>Erstellen Sie ein neues GPO, in dem die Änderungssteuerung über AGPM verwaltet und in der Produktionsumgebung der Domäne bereitgestellt wird. Wenn Sie nicht über die Berechtigung zum Erstellen eines Gruppenrichtlinienobjekts verfügen, werden Sie aufgefordert, eine Anforderung zu senden. (Diese Option wird angezeigt, wenn beim Klicken mit der rechten Maustaste auf die <strong> Liste der Gruppenrichtlinienobjekte </strong> .)</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Verlauf</strong></p></td>
<td align="left"><p>Öffnen Sie ein Fenster, in dem alle Versionen des ausgewählten Gruppenrichtlinienobjekts aufgelistet sind, die im Archiv gespeichert sind. Aus dem Protokoll können Sie einen Bericht über die Einstellungen in einem Gruppenrichtlinienobjekt abrufen, zwei Versionen eines GPO vergleichen, ein GPO mit einer Vorlage vergleichen oder auf eine frühere Version eines GPO zurückgreifen.</p></td>
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
<td align="left"><p>Generieren eines HTML-basierten oder XML-basierten Berichts, in dem die Einstellungen innerhalb des ausgewählten Gruppenrichtlinienobjekts angezeigt werden, oder Anzeigen von Links zu den ausgewählten Gruppenrichtlinienobjekten aus Organisationseinheiten ab dem Zeitpunkt, zu dem die Gruppenrichtlinienobjekte zuletzt gesteuert, importiert oder eingecheckt wurden.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Unterschiede</strong></p></td>
<td align="left"><p>Generieren eines HTML-basierten oder XML-basierten Berichts, der die Einstellungen in zwei ausgewählten GPOs oder innerhalb des ausgewählten GPO und einer Vorlage vergleicht.</p></td>
</tr>
</tbody>
</table>

 

## Bearbeitung


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
<td align="left"><p><strong>Bearbeiten</strong></p></td>
<td align="left"><p>Öffnen <strong> Sie das Fenster "Gruppenrichtlinien-Verwaltungs-Editor </strong> ", um das ausgewählte Gruppenrichtlinienobjekt zu ändern.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Abreise</strong></p></td>
<td align="left"><p>Besorgen Sie sich eine Kopie des ausgewählten GPO aus dem Archiv für die Offlinebearbeitung, und verbieten Sie anderen Personen, das Gruppenrichtlinienobjekt zu bearbeiten, bis es wieder in das Archiv eingecheckt wurde. Das Auschecken kann von einem AGPM-Administrator (Vollzugriff) überschrieben werden.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Ankunft</strong></p></td>
<td align="left"><p>Überprüfen Sie die bearbeitete Version des ausgewählten Gruppenrichtlinienobjekts in das Archiv, damit andere autorisierte Bearbeiter Änderungen vornehmen können, oder eine genehmigende Person das Gruppenrichtlinienobjekt in der Produktionsumgebung der Domäne bereitstellen kann.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Auschecken rückgängig machen</strong></p></td>
<td align="left"><p>Geben Sie ein ausgechecktes Gruppenrichtlinienobjekt ohne Änderungen in das Archiv zurück.</p></td>
</tr>
</tbody>
</table>

 

## Versionsverwaltung


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
<td align="left"><p><strong>Aus Produktion importieren</strong></p></td>
<td align="left"><p>Kopieren Sie für das ausgewählte Gruppenrichtlinienobjekt die Version in der Produktionsumgebung der Domäne in das Archiv.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Aus Datei importieren</strong></p></td>
<td align="left"><p>Ersetzen Sie die Richtlinieneinstellungen des ausgewählten, ausgecheckten Gruppenrichtlinienobjekts durch die von einer GPO-Sicherungsdatei.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Delete</strong></p></td>
<td align="left"><p>Verschieben Sie das ausgewählte Gruppenrichtlinienobjekt in den Papierkorb, und geben Sie an, ob Sie die bereitgestellte Version (sofern vorhanden) in Production belassen oder die bereitgestellte Version zusätzlich zur Version im Archiv löschen möchten. Wenn Sie nicht über die Berechtigung zum Löschen eines Gruppenrichtlinienobjekts verfügen, werden Sie aufgefordert, eine Anforderung zu senden.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Bereitstellen</strong></p></td>
<td align="left"><p>Verschieben Sie das ausgewählte Gruppenrichtlinienobjekt, das in das Archiv eingecheckt ist, in die Produktionsumgebung der Domäne. Mit dieser Aktion wird Sie im Netzwerk aktiviert und die zuvor aktive Version des Gruppenrichtlinienobjekts überschrieben, falls vorhanden. Wenn Sie nicht über die Berechtigung zum Bereitstellen eines GPO verfügen, werden Sie aufgefordert, eine Anforderung zu senden.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Exportieren nach</strong></p></td>
<td align="left"><p>Speichern Sie das ausgewählte Gruppenrichtlinienobjekt in einer Sicherungsdatei, damit Sie es in eine andere Domäne kopieren können.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Label</strong></p></td>
<td align="left"><p>Markieren Sie das ausgewählte Gruppenrichtlinienobjekt mit einer beschreibenden Bezeichnung (wie &quot; "bekannt gut &quot; ") und kommentieren Sie die Datensatzspeicherung. Beschriftungen werden in der <strong> </strong> Spalte Zustand und Kommentare in der <strong> </strong> Spalte Kommentar des <strong> verlaufsfensters angezeigt </strong> . Sie unterstützen Sie beim Ermitteln früherer Versionen eines Gruppenrichtlinienobjekts, sodass Sie einen Rollback durchführen können, wenn ein Problem auftritt.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Rename</strong></p></td>
<td align="left"><p>Ändern Sie den Namen des ausgewählten Gruppenrichtlinienobjekts. Wenn das Gruppenrichtlinienobjekt bereits bereitgestellt wurde, wird der Name in der Produktionsumgebung der Domäne aktualisiert, wenn das Gruppenrichtlinienobjekt erneut bereitgestellt wird.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Als Vorlage speichern</strong></p></td>
<td align="left"><p>Erstellen Sie eine neue Vorlage basierend auf den Einstellungen des ausgewählten Gruppenrichtlinienobjekts.</p></td>
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
<td align="left"><p>Aktualisieren Sie die Anzeige der Gruppenrichtlinien-Verwaltungskonsole (Group Policy Management Console, GPMC), um alle Änderungen einzubeziehen. Einige Änderungen werden erst angezeigt, wenn die Anzeige aktualisiert wird.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Hilfe</strong></p></td>
<td align="left"><p>Anzeigen der Hilfe zu AGPM</p></td>
</tr>
</tbody>
</table>

 

### Weitere Verweise

-   [Registerkarte "Inhalt"](contents-tab-agpm40.md)

-   [Durchführen von Editor-Aufgaben](performing-editor-tasks-agpm40.md)

-   [Durchführen der Aufgaben von genehmigenden Personen](performing-approver-tasks-agpm40.md)

-   [Durchführen von Prüferaufgaben](performing-reviewer-tasks-agpm40.md)

 

 





