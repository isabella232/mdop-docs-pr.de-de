---
title: Benutzerzugriffsberechtigungen in Application Virtualization Client
description: Benutzerzugriffsberechtigungen in Application Virtualization Client
author: dansimp
ms.assetid: 7459374c-810c-45e3-b205-fdd1f8514f80
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1083faffb48aa58a0ee0c81b58fae307e53548b8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806179"
---
# Benutzerzugriffsberechtigungen in Application Virtualization Client


Auf der Registerkarte " **Berechtigungen** " im Dialogfeld " **Eigenschaften** ", das durch Klicken mit der rechten Maustaste auf den Knoten **Application Virtualization** in der Application Virtualization Client Management Console aufgerufen wird, können Administratoren Benutzern Berechtigungen zur Verwendung der verschiedenen Client Funktionen erteilen.

**Hinweis**  Bevor Sie die Benutzerberechtigungen ändern, stellen Sie sicher, dass alle Berechtigungsänderungen mit den Richtlinien der Organisation für die Gewährung von Benutzerberechtigungen konsistent sind.

 

In der folgenden Tabelle sind die Berechtigungen aufgeführt und beschrieben, die Benutzern gewährt werden können.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Berechtigungs Name</th>
<th align="left">Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Hinzufügen von Anwendungen</p></td>
<td align="left"><p>Registrieren Sie neue Anwendungen, indem Sie eine neue OSD-Datei an den Client übergeben, indem Sie sfttray.exe, sftmime.exe oder die MMC verwenden.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Ändern der Größe des Dateisystemcaches</p></td>
<td align="left"><p>Vergrößern des Dateisystemcaches</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Ändern des Dateisystemlaufwerks</p></td>
<td align="left"><p>Wählen Sie einen anderen bevorzugten Laufwerkbuchstaben für das Dateisystem aus.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Ändern von Protokolleinstellungen</p></td>
<td align="left"><p>Ändern Sie die Protokollebene oder den Protokollpfad für die Clientprotokolldatei.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Ändern von OSD-Dateien</p></td>
<td align="left"><p>Ändern Sie die OSD-Dateien für registrierte Anwendungen, und übergeben Sie diese an den Client. Dies hat keinen Einfluss auf die Veröffentlichungsaktualisierung.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Löschen von Anwendungseinstellungen</p></td>
<td align="left"><p>Löschen Sie Dateitypen, Verknüpfungen und alle Konfigurationen für den aktuellen Benutzer.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Löschen von Anwendungen</p></td>
<td align="left"><p>Entfernen Sie alle Verweise auf eine Anwendung aus dem Dateisystem und dem OSD-Cache für alle Benutzer auf dem Computer.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Importieren von Anwendungen in den Cache</p></td>
<td align="left"><p>Laden Sie Anwendungsdaten direkt aus einer angegebenen SFT-Datei in den Dateisystemcache. Dies wirkt sich auf alle Benutzer aus.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Laden von Anwendungen in den Cache</p></td>
<td align="left"><p>Starten Sie eine Auslastung der SFT-Datei für eine Anwendung aus der konfigurierten Quelle, beispielsweise einem App-V-Streamingserver. Dadurch wird die Anwendung für alle Benutzer auf dem Computer geladen.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Sperren und Entsperren von Anwendungen im Cache</p></td>
<td align="left"><p>Verhindern oder zulassen, dass Anwendungen aus dem Dateisystemcache entladen werden. Dies wirkt sich auf alle Benutzer auf dem Computer aus.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Verwalten von Dateitypzuordnungen</p></td>
<td align="left"><p>Sie können Dateitypzuordnungen nur für den aktuellen Benutzer hinzufügen, ändern oder löschen.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Verwalten von Veröffentlichungs Aktualisierungseinstellungen</p></td>
<td align="left"><p>Ändern Sie die Einstellungen, mit denen die Anzeigedauer für Veröffentlichungs Aktualisierungen für alle Benutzer auf dem Computer gesteuert wird.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Verwalten von Veröffentlichungsservern</p></td>
<td align="left"><p>Sie können Veröffentlichungsserver für alle Benutzer auf dem Computer hinzufügen, ändern oder löschen. Diese Berechtigung umfasst implizit die Berechtigung zum Verwalten von Veröffentlichungs Aktualisierungseinstellungen.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Veröffentlichen von Verknüpfungen</p></td>
<td align="left"><p>Erstellen neuer Verknüpfungen zu registrierten Anwendungen Der Benutzer muss auch über die Berechtigung zum Erstellen von Dateien im lokalen Dateisystem verfügen.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Reparieren von Anwendungen</p></td>
<td align="left"><p>Entfernen Sie anwendungsspezifische Konfigurationen für den aktuellen Benutzer, ohne Verknüpfungen oder Dateitypzuordnungen zu entfernen.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Starten einer Veröffentlichungsaktualisierung</p></td>
<td align="left"><p>Starten einer ungeplanten Veröffentlichungsaktualisierung für den aktuellen Benutzer</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Offlinemodus umschalten</p></td>
<td align="left"><p>Ändern Sie den gesamten Client von Online in den Offlinemodus für alle Benutzer.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Entladen von Anwendungen aus dem Cache</p></td>
<td align="left"><p>Löschen Sie Anwendungsdaten aus dem Dateisystemcache für alle Benutzer, ohne benutzerspezifische Einstellungen, Verknüpfungen oder Dateitypzuordnungen zu entfernen.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Alle Anwendungen anzeigen</p></td>
<td align="left"><p>Dem Benutzer gestatten, die virtuellen Anwendungen für alle auf dem Computer registrierten Benutzer anzuzeigen.</p></td>
</tr>
</tbody>
</table>

 

## Verwandte Themen


[So ändern Sie die Benutzerzugriffsberechtigungen](how-to-change-user-access-permissions.md)

 

 





