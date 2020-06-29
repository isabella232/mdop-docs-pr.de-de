---
title: HELP
description: HELP
author: dansimp
ms.assetid: 0ddb5f18-0c0a-45ea-b7c7-2d4749e3d35d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 395e6199529ccbe708aa7d1ac6673ea6f9494ae4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808770"
---
# HELP


Zeigt Informationen zu den verschiedenen SFTMIME-Befehlen an, die in Application Virtualization (App-V) verwendet werden können.

## HELP


`SFTMIME [/? | /HELP [VERB:<verb>]]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Parameter</th>
<th align="left">Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>/?,/Help</p></td>
<td align="left"><p>Zeigt Nutzungsinformationen an.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Verb</p></td>
<td align="left"><p>Der auszuführende Befehl, beispielsweise "hinzufügen", "Aktualisieren", "Hilfe" oder "entfernen".</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Objekt</p></td>
<td align="left"><p>Wofür der Befehl gilt, beispielsweise App: &quot; Standardanwendung.&quot;</p></td>
</tr>
<tr class="even">
<td align="left"><p>Parameter</p></td>
<td align="left"><p>Optionale Parameter für das angegebene Verb und Objekt.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/Log</p></td>
<td align="left"><p>Protokollausgabe in den angegebenen Pfadname.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/Console</p></td>
<td align="left"><p>Zeigt die Ausgabe im aktiven Konsolenfenster an (Standardeinstellung).</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/GUI</p></td>
<td align="left"><p>Zeigt Fehler in einem Dialogfeld an (gilt nicht für Abfragen).</p></td>
</tr>
</tbody>
</table>

 

Für Version 4.6 wurde die folgende Option hinzugefügt.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p>/LOGU</p></td>
<td align="left"><p>Wenn angegeben, wird die Ausgabe mit dem angegebenen Pfadname im Unicode-Format protokolliert.</p></td>
</tr>
</tbody>
</table>

 

Die in der folgenden Tabelle beschriebenen Verben werden unterstützt.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p>HINZUFÜGEN</p></td>
<td align="left"><p>Fügt dem App-V-Client eine neue Anwendung, ein Paket, eine Dateitypzuordnung oder einen Veröffentlichungsserver hinzu.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Konfigurieren</p></td>
<td align="left"><p>Ändert die Konfiguration einer Anwendung, eines Pakets, einer Dateitypzuordnung oder eines Veröffentlichungsservers.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>DELETE</p></td>
<td align="left"><p>Entfernt Anwendungen, Pakete, Dateitypzuordnungen oder Server.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Laden</p></td>
<td align="left"><p>Lädt ein Paket in den Dateisystemcache.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Reparatur</p></td>
<td align="left"><p>Setzt Ihre persönlichen Einstellungen für eine Anwendung zurück.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Aktualisieren</p></td>
<td align="left"><p>Löst eine Aktualisierung des Veröffentlichungsservers aus.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Veröffentlichen</p></td>
<td align="left"><p>Veröffentlicht eine Anwendungsverknüpfung für das Startmenü, den Desktop oder einen anderen angegebenen Speicherort des Benutzers oder kann verwendet werden, um den Inhalt eines gesamten Pakets zu veröffentlichen.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Veröffentlichung</p></td>
<td align="left"><p>Entfernt die Verknüpfungen und Dateitypen für ein gesamtes Paket.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Abfrage</p></td>
<td align="left"><p>Ruft eine aktuelle Liste von Anwendungen, Paketen, Dateitypzuordnungen oder Veröffentlichungsservern ab.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Deaktivieren</p></td>
<td align="left"><p>Entfernt ihre persönlichen Einstellungen und Desktopkonfigurationen für eine oder mehrere Anwendungen.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Entladen</p></td>
<td align="left"><p>Entladen eines Pakets aus dem Dateisystemcache</p></td>
</tr>
<tr class="even">
<td align="left"><p>Sperren</p></td>
<td align="left"><p>Sperrt die im Dateisystemcache angegebene Anwendung.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Entsperren</p></td>
<td align="left"><p>Entsperrt die im Dateisystemcache angegebene Anwendung.</p></td>
</tr>
</tbody>
</table>

 

Verwenden Sie den folgenden Befehl, um weitere Informationen zu den vorhergehenden Aktionen zu erhalten:

`SFTMIME /HELP VERB:verb`

Mit dem folgenden Befehl werden beispielsweise Informationen für das Add-Verb angezeigt:

`SFTMIME /HELP VERB:ADD`

## Verwandte Themen


[SFTMIME-Befehlsreferenz](sftmime--command-reference.md)

 

 





