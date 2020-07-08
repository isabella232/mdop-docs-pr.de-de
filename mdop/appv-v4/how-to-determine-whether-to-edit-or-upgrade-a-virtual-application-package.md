---
title: So ermitteln Sie, ob ein virtuelles Anwendungspaket bearbeitet oder aktualisiert werden soll
description: So ermitteln Sie, ob ein virtuelles Anwendungspaket bearbeitet oder aktualisiert werden soll
author: dansimp
ms.assetid: 33dd5332-6802-46e0-9748-43fcc8f80aa3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b256a4927231613b6f2e688b5951adf57c9cb89a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807132"
---
# So ermitteln Sie, ob ein virtuelles Anwendungspaket bearbeitet oder aktualisiert werden soll


Verwenden Sie die folgende Tabelle, um zu ermitteln, ob ein virtuelles Anwendungspaket zur Bearbeitung geöffnet werden kann, ob Sie eine neue Version des Pakets erstellen müssen oder ob eine der beiden Optionen mithilfe des App-V-Sequencers verfügbar ist.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Aktion</th>
<th align="left">Zum Bearbeiten öffnen</th>
<th align="left">Für Upgrade öffnen</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Anzeigen von Paketeigenschaften.</p></td>
<td align="left"><p>Ja</p></td>
<td align="left"><p>Ja</p></td>
</tr>
<tr class="even">
<td align="left"><p>Anzeigen des Paket Änderungsverlaufs</p></td>
<td align="left"><p>Ja</p></td>
<td align="left"><p>Ja</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Anzeigen zugehöriger Paketdateien</p></td>
<td align="left"><p>Ja</p></td>
<td align="left"><p>Ja</p></td>
</tr>
<tr class="even">
<td align="left"><p>Bearbeiten Sie die Registrierungseinstellungen.</p></td>
<td align="left"><p>Ja</p></td>
<td align="left"><p>Ja</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Überprüfen Sie die zusätzlichen Paketeinstellungen (mit Ausnahme der Dateieigenschaften des Betriebssystems).</p></td>
<td align="left"><p>Ja</p></td>
<td align="left"><p>Ja</p></td>
</tr>
<tr class="even">
<td align="left"><p>Erstellen Sie zugeordnete Windows Installer (MSI).</p></td>
<td align="left"><p>Ja</p></td>
<td align="left"><p>Ja</p></td>
</tr>
<tr class="odd">
<td align="left"><p>OSD-Datei ändern.</p></td>
<td align="left"><p>Ja</p></td>
<td align="left"><p>Ja</p></td>
</tr>
<tr class="even">
<td align="left"><p>Komprimieren und Dekomprimieren des Pakets.</p></td>
<td align="left"><p>Ja</p></td>
<td align="left"><p>Ja</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Dateitypzuordnungen hinzufügen.</p></td>
<td align="left"><p>Ja</p></td>
<td align="left"><p>Ja</p></td>
</tr>
<tr class="even">
<td align="left"><p>Umbenennen von Tastenkombinationen</p></td>
<td align="left"><p>Ja</p></td>
<td align="left"><p>Ja</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Legen Sie den virtualisierten Registrierungsschlüssel Status fest (override/Merge).</p></td>
<td align="left"><p>Ja</p></td>
<td align="left"><p>Ja</p></td>
</tr>
<tr class="even">
<td align="left"><p>Legen Sie den Status eines virtualisierten Ordners fest.</p></td>
<td align="left"><p>Ja</p></td>
<td align="left"><p>Ja</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Bearbeiten von virtuellen Dateisystem Zuordnungen</p></td>
<td align="left"><p>Ja</p></td>
<td align="left"><p>Ja</p></td>
</tr>
<tr class="even">
<td align="left"><p>Überprüfen Sie alle zugehörigen Betriebssystem-Dateieigenschaften für ein Paket.</p></td>
<td align="left"><p>Nein</p></td>
<td align="left"><p>Ja</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Weitere Dienste hinzufügen.</p></td>
<td align="left"><p>Nein</p></td>
<td align="left"><p>Ja</p></td>
</tr>
<tr class="even">
<td align="left"><p>Fügen Sie weitere Dateien hinzu.</p></td>
<td align="left"><p>Nein</p></td>
<td align="left"><p>Ja</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Sammeln und Konfigurieren von zugehörigen Sicherheitsbeschreibungen</p></td>
<td align="left"><p>Nein</p></td>
<td align="left"><p>Ja</p></td>
</tr>
<tr class="even">
<td align="left"><p>Wenden Sie Sicherheitsupdates an, oder aktualisieren Sie auf eine neue Version.</p></td>
<td align="left"><p>Nein</p></td>
<td align="left"><p>Ja</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Hinzufügen einer zusätzlichen Anwendung</p></td>
<td align="left"><p>Nein</p></td>
<td align="left"><p>Ja</p></td>
</tr>
<tr class="even">
<td align="left"><p>Wenden Sie Updates an, für die die Anwendung geöffnet werden muss.</p></td>
<td align="left"><p>Nein</p></td>
<td align="left"><p>Ja</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Wenden Sie Updates an, die erfordern, dass der Computer neu gestartet wird.</p></td>
<td align="left"><p>Nein</p></td>
<td align="left"><p>Ja</p></td>
</tr>
</tbody>
</table>

 

## Verwandte Themen


[So bearbeiten Sie eine vorhandene virtuelle Anwendung](how-to-edit-an-existing-virtual-application.md)

[So aktualisieren Sie eine vorhandene virtuelle Anwendung](how-to-upgrade-an-existing-virtual-application.md)

 

 





