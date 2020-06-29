---
title: QUERY OBJ
description: QUERY OBJ
author: dansimp
ms.assetid: 55abf0d1-c779-4172-8357-552ab010933b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 328e9feb96c70080531cbbc666d8ff1b86045ba5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806427"
---
# QUERY OBJ


Gibt eine durch Tabstopps getrennte Liste der aktuellen Anwendungen, Pakete, Dateitypzuordnungen oder Veröffentlichungsserver zurück.

`SFTMIME QUERY OBJ:{APP|PACKAGE|TYPE|SERVER} [/SHORT] [/GLOBAL]                 [/LOG log-pathname | /CONSOLE ]`

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
<td align="left"><p>App</p></td>
<td align="left"><p>Gibt eine Liste der Anwendungen zurück.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Paket</p></td>
<td align="left"><p>Gibt eine Liste der Pakete zurück.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>TYPE</p></td>
<td align="left"><p>Gibt eine Liste der Dateitypzuordnungen zurück.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Server</p></td>
<td align="left"><p>Gibt eine Liste der Veröffentlichungsserver zurück.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/SHORT</p></td>
<td align="left"><p>Gibt eine Liste der Anwendungsnamen, Pakete, Assoziationen oder Servernamen zurück, ohne die vollständigen Eigenschaften der einzelnen anzeigen anzuzeigen.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/Global</p></td>
<td align="left"><p>Gibt für Anwendungen alle bekannten Anwendungen zurück, nicht nur diejenigen, auf die der aktuelle Benutzer zugreifen kann. Gibt für Pakete alle bekannten Pakete anstatt nur diejenigen zurück, auf die der aktuelle Benutzer zugreifen kann. Gibt für Zuordnungen nur Zuordnungen zurück, die für alle Benutzer gelten, nicht für benutzerspezifische. Nicht gültig für Server.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/Log</p></td>
<td align="left"><p>Wenn angegeben, wird die Ausgabe mit dem angegebenen Pfadnamen protokolliert.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/Console</p></td>
<td align="left"><p>Wenn angegeben, wird die Ausgabe im aktiven Konsolenfenster angezeigt (Standardeinstellung).</p></td>
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

 

**Hinweis**  In Version 4,6 wurde der Ausgabe von SFTMIME Query obj: App \ [/GLOBAL\] eine neue Spalte hinzugefügt. Die letzte Spalte der Ausgabe ist ein numerischer Wert, der angibt, ob eine Anwendung veröffentlicht wird oder nicht.

Veröffentlicht = 1 bedeutet, dass die Anwendung durch eine Veröffentlichungs Server Aktualisierung veröffentlicht wurde, indem Sie die Anwendung mithilfe einer Windows Installer-Datei (. MSI) oder durch Ausführen eines SFTMIME-Pakets zum Hinzufügen, Konfigurieren des Pakets oder Veröffentlichen eines Pakets mithilfe eines paketmanifests.

Published = 0 bedeutet, dass die Anwendung nicht veröffentlicht wurde oder dass Sie nicht mehr als Ergebnis der Durchführung eines Clear-Vorgangs oder durch Ausführen eines SFTMIME-Befehls "UNPUBLISH" veröffentlicht wurde.

Wenn Sie den/Global-Parameter verwenden, ist der veröffentlichte Zustand 1 für Anwendungen, die Global veröffentlicht wurden, und 0 für die Anwendungen, die unter Benutzerkontexten veröffentlicht wurden. Ohne den/Global-Parameter wird ein veröffentlichter Zustand von 1 für Anwendungen zurückgegeben, die im Kontext des Benutzers veröffentlicht werden, der den Befehl ausführt, und für die Global veröffentlichten Anwendungen wird ein Zustand von 0 zurückgegeben.

 

Mithilfe des SFTMIME-Abfrage-obj-Befehls können Sie Informationen zu allen oben gezeigten Objekten Abfragen – Anwendungen, Pakete, Dateitypzuordnungen und Server.Im folgenden Beispiel wird gezeigt, wie Sie den SFTMIME-Abfrage-obj-Befehl in ihren normalen Vorgangs Aufgaben verwenden können, indem Sie den Prozess, dem Sie folgen, wenn Sie den OVERRIDEURL-Parameterwert für ein bestimmtes Paket festlegen möchten, um einen neuen Pfad für den Paketinhalt anzugeben. 

1.  Führen Sie den folgenden Befehl aus, um das Paket zu finden, das Sie konfigurieren möchten:

    `SFTMIME QUERY OBJ:PACKAGE`

    Dieser Befehl gibt jeden gefundenen Paketnamen als GUID in der ersten Ausgabespalte zurück, beispielsweise {AF78ABE1-57D4-4297-89DE-C308684AEDD6}.

2.  Zum Festlegen des OVERRIDEURL-Parameterwerts verwenden Sie den Befehl SFTMIME- [Paket konfigurieren](configure-package.md) . Wenn Sie beispielsweise den OVERRIDEURL-Wert für dieses Paket auf einen Wert von *\\\\server\\share\\mypackage.SFT*festlegen möchten, verwenden Sie den Befehl SFTMIME-Paket konfigurieren, und geben Sie ihm die ausgewählte Paket-GUID aus der Ausgabe des Befehls SFTMIME Query obj in Schritt 1, gefolgt vom OVERRIDEURL-Parameter und dem neuen Wert, wie folgt:

    `SFTMIME CONFIGURE PACKAGE:"{AF78ABE1-57D4-4297-89DE-C308684AEDD6}" /OVERRIDEURL "\\\\server\\share\\mypackage.sft "`

Für Version 4.6 SP2 wurde die folgende Option hinzugefügt.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p>/NO-UPDATE-FTA-SHORTCUT</p></td>
<td align="left"><p>Gibt den aktuellen Zustand des/no-Update-FTA-Shortcut-Flags an.</p></td>
</tr>
</tbody>
</table>

 

## Verwandte Themen


[SFTMIME-Befehlsreferenz](sftmime--command-reference.md)

 

 





