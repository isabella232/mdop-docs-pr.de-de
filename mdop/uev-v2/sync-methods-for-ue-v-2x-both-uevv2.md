---
title: Synchronisieren von Methoden für UE-V 2.x
description: Synchronisieren von Methoden für UE-V 2.x
author: dansimp
ms.assetid: af0ae894-dfdc-41d2-927b-c2ab1b355ffe
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a163442e2ab3dbd777aca133b13b0086cdb8ae1a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810039"
---
# Synchronisieren von Methoden für UE-V 2.x


Mit dem Microsoft User Experience Virtualization (UE-V) 2,0, 2,1 und 2,1 SP1-Agent können Sie die Anwendungs-und Windows-Einstellungen der Benutzer mit dem Speicherort der Einstellungen synchronisieren. Die Konfiguration der *Synchronisierungsmethode* definiert, wie der UE-V-Agent diese Einstellungen in den Speicherort der Einstellungen hochladen und herunterlädt. UE-V 2. x führt eine neue SyncMethod namens *SyncProvider*ein. Weitere Informationen zu Trigger-Ereignissen, mit denen die Synchronisierung von Anwendungs-und Windows-Einstellungen gestartet wird, finden Sie unter [Synchronisieren von Trigger-Ereignissen für UE-V 2. x](sync-trigger-events-for-ue-v-2x-both-uevv2.md).

## SyncMethod-Konfiguration


In dieser Tabelle werden die Änderungen an SyncMethod von UE-v v 1.0 zu v 2.0 zu v 2.1 sowie die Einstellungen für jede Konfiguration erläutert:

<table>
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>SyncMethod-Konfiguration</strong></p></td>
<td align="left"><p><strong>V 1.0</strong></p></td>
<td align="left"><p><strong>V 2.0</strong></p></td>
<td align="left"><p><strong>V 2.1 und v 2.1 SP1</strong></p></td>
<td align="left"><p><strong>Beschreibung</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p>SyncProvider</p></td>
<td align="left"><p>n.a.</p></td>
<td align="left"><p>Standard</p></td>
<td align="left"><p>Standard</p></td>
<td align="left"><p>Änderungen an Einstellungen für eine bestimmte Anwendung oder für globale Windows-Desktopeinstellungen werden lokal in einem Cacheordner gespeichert. Diese Änderungen werden dann mit dem Speicherort der Einstellungen synchronisiert, wenn ein Synchronisierungstrigger-Ereignis stattfindet. Durch das Verschieben von Änderungen werden die lokalen Änderungen im Speicherpfad für Einstellungen gespeichert.</p>
<p>Diese Standardeinstellung ist der Gold Standard für Computer. Mit dieser Option wird versucht, die Einstellung und die Timeouts nach einer kurzen Verzögerung zu synchronisieren, um sicherzustellen, dass die Anwendung oder der Betriebssystem Start für einen längeren Zeitraum nicht verzögert wird.</p>
<p>Diese Funktionalität ist auch an die geplante Aufgabe – Synchronisierungs-Controller-Anwendung gebunden. Der Administrator steuert die Häufigkeit des geplanten Vorgangs. Standardmäßig werden die Einstellungen von Computern alle 30 Minuten nach der Anmeldung synchronisiert.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Offlinedateien</p></td>
<td align="left"><p>Standard</p></td>
<td align="left"><p>Veraltet</p></td>
<td align="left"><p>Veraltet</p></td>
<td align="left"><p>Verhält sich wie SyncProvider in v 2.0.</p>
<p>Wenn Offline Dateien aktiviert sind und der Ordner angeheftet ist, wird UE-V diesen Ordner unpin und direkt mit dem zentralen SMB-Verzeichnis synchronisiert.</p>
<p><strong>Hinweis: </strong> in V 1.0, wenn Sie UE-V auf eine Corpnet getrennte Weise verwenden möchten (auch wenn Sie mit einem Laptop unterwegs sind), sollten Sie Offline Dateien verwenden, um sicherzustellen, dass Ihre Einstellungen durchstreift werden.Wir haben genügend Kundenfeedback erhalten, dass das Aktivieren von Offline Dateien ein nicht trivialer Enterprise-Blocker ist. In UE-V 2 haben wir also ein eng gekoppeltes Synchronisierungsmodul erstellt, um Ihre Daten lokal zwischenzuspeichern und die Einstellungen mit dem zentralen Server zu synchronisieren. Dieser Funktionsbereich ersetzt nicht die Offline Dateien oder die Ordnerumleitung.</p>
<p>UE-V 2 funktioniert nicht gut mit Offline Ordnern, daher ist es nicht so, den Speicherpfad für Einstellungen auf einen angehefteten offline-oder CSC-Ordner festzulegen.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Extern</p></td>
<td align="left"><p>n.a.</p></td>
<td align="left"><p>n.a.</p></td>
<td align="left"><p>Unterstützt</p></td>
<td align="left"><p>Neu in UE-v 2,1 gibt diese Konfigurationsmethode an, dass, wenn UE-v-Einstellungen in einen lokalen Ordner auf dem Benutzer Computer geschrieben werden, ein externes Synchronisierungsmodul (wie OneDrive for Business, Arbeitsordner, SharePoint oder Dropbox) verwendet werden kann, um diese Einstellungen auf die verschiedenen Computer anzuwenden, auf die Benutzer zugreifen.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Keine</p></td>
<td align="left"><p>Ja</p></td>
<td align="left"><p>Ja</p></td>
<td align="left"><p>Ja</p></td>
<td align="left"><p>Diese Konfigurationseinstellung ist für die Virtual Desktop Infrastructure (VDI) und die Übertragung von Anwendungserfahrung in erster Linie vorgesehen. Diese Einstellung sollte in Windows Server-Feldern verwendet werden, die in einem Rechenzentrum verwendet werden, wobei die Verbindung immer verfügbar ist.</p>
<p>Alle Einstellungsänderungen werden direkt auf dem Server gespeichert. Wenn die Netzwerkverbindung mit dem Einstellungsspeicher Pfad nicht verfügbar ist, werden die Einstellungen Änderungen auf dem Gerät zwischengespeichert und beim nächsten Ausführen des Synchronisierungsanbieters synchronisiert. Wenn der Speicherpfad für Einstellungen nicht gefunden wird und das Benutzerprofil bei der Abmeldung aus einer gepoolten VDI-Umgebung entfernt wird, gehen diese Einstellungsänderungen verloren, und der Benutzer muss die Änderung erneut anwenden, wenn der Computer erneut den Speicherpfad für Einstellungen erreichen kann.</p>
<p>Apps und Betriebssystem warten auf unbestimmte Zeit, bis der Standort vorhanden ist. Dies kann dazu führen, dass die APP-Lade-oder Betriebssystem-Anmeldezeit drastisch zunimmt, wenn der Standort nicht gefunden wird.</p></td>
</tr>
</tbody>
</table>

 

Sie können die Synchronisierungsmethode wie folgt konfigurieren:

-   Wenn Sie [den UE-V-Agent](https://technet.microsoft.com/library/dn458891.aspx#agent) über einen Befehlszeilenparameter oder in einem Batchskript bereitstellen

-   Über [Gruppenrichtlinien](https://technet.microsoft.com/library/dn458893.aspx) Einstellungen

-   Mit dem [System Center-Konfigurationspaket](https://technet.microsoft.com/library/dn458917.aspx) für UE-V

-   Nach der Installation des UE-V-Agents mithilfe von [Windows PowerShell oder Windows-Verwaltungsinstrumentation (WMI)](https://technet.microsoft.com/library/dn458937.aspx)






## Verwandte Themen


[Bereitstellen der erforderlichen Features für UE-V 2.x](deploy-required-features-for-ue-v-2x-new-uevv2.md#ssl)

[Bereitstellen der erforderlichen Features für UE-V 2.x](deploy-required-features-for-ue-v-2x-new-uevv2.md#config)

[Technische Referenz für UE-V 2.x](technical-reference-for-ue-v-2x-both-uevv2.md)

 

 





