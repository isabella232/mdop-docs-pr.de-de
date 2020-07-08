---
title: Seite ' Erweiterte Optionen ' für Application Virtualization Sequencer-Assistent
description: Seite ' Erweiterte Optionen ' für Application Virtualization Sequencer-Assistent
author: dansimp
ms.assetid: 2c4c5d95-d55e-463d-a851-8486f6a724f2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 716fa27852f1cadfebec31a267ce1b9b581b8ff7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807971"
---
# Seite ' Erweiterte Optionen ' für Application Virtualization Sequencer-Assistent


Verwenden Sie die Seite **Erweiterte Optionen** des Sequence-Assistenten für Application Virtualization (App-V), um erweiterte Optionen für die Installation der Anwendung anzugeben. Die Seite enthält die in der folgenden Tabelle beschriebenen Elemente.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Name</th>
<th align="left">Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Block Größe</strong></p></td>
<td align="left"><p>Hiermit können Sie die Größe von Blöcken angeben, in die die SFT-Datei aufgeteilt wird, wenn Sie über ein Netzwerk gestreamt wird. Alle Blöcke entsprechen der angegebenen Größe; Allerdings kann der letzte Block kleiner als angegeben sein. Wählen Sie einen der folgenden Werte aus:</p>
<ul>
<li><p><strong>4 KB</strong></p></li>
<li><p><strong>16 KB</strong></p></li>
<li><p><strong>32 KB</strong></p></li>
<li><p><strong>64 KB</strong></p></li>
</ul>
<div class="alert">
<strong>Hinweis:</strong><br/><p>Wenn Sie eine Blockgröße auswählen, sollten Sie die Größe der SFT-Datei und die Netzwerkbandbreite in Frage stellen. Eine Datei mit einer kleineren Blockgröße dauert länger, um über das Netzwerk zu streamen, ist jedoch weniger bandbreitenintensiv. Dateien mit größeren Blockgrößen können schneller gestreamt werden, verwenden aber mehr Netzwerkbandbreite. Durch experimentieren können Sie die optimale Blockgröße für Streaming-Anwendungen in Ihrem Netzwerk ermitteln.</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Aktivieren von Microsoft Update während der Überwachung</strong></p></td>
<td align="left"><p>Aktiviert die Installation von Microsoft Updates während des Sequenz-Assistenten&#39;s-Überwachungsphase.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>REBASE-DLLs</strong></p></td>
<td align="left"><p>Ermöglicht die Neuzuordnung unterstützter Dynamic-Link-Bibliotheken zu einem zusammenhängenden Speicherplatz im Arbeitsspeicher, wodurch der Arbeitsspeicher gespart und die Leistung verbessert wird.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Zurück</strong></p></td>
<td align="left"><p>Greift auf den Sequenz-Assistenten&#39;s vorherige Seite zu.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Nächste</strong></p></td>
<td align="left"><p>Greift auf den Sequenz-Assistenten zu&#39;nächste Seite.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Abbrechen</strong></p></td>
<td align="left"><p>Beendet den Vorgang des Sequenz-Assistenten.</p></td>
</tr>
</tbody>
</table>



\ [Vorlage-Tokenwert \]

Verwenden Sie die Seite " **Erweiterte Optionen** " des App-V-Sequenz-Assistenten, um erweiterte Optionen für die Anwendung anzugeben, die Sie sequenzieren. Diese Seite enthält die in der folgenden Tabelle beschriebenen Elemente.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Name</th>
<th align="left">Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Microsoft Update während der Überwachung ausführen lassen</strong></p></td>
<td align="left"><p>Gibt an, ob Softwareupdates während der Überwachungsphase der Anwendungs Sequenz auf die Anwendung angewendet werden. Diese Option ist hilfreich, wenn Updates erforderlich sind, um die Anwendungsinstallation erfolgreich abzuschließen. Diese Option ist standardmäßig nicht aktiviert.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>REBASE-DLLs</strong></p></td>
<td align="left"><p>Ermöglicht die Neuzuordnung unterstützter Dynamic-Link-Bibliotheken zu einem zusammenhängenden Speicherplatz im Arbeitsspeicher. Wenn Sie diese Option auswählen, können Sie den Arbeitsspeicher verwalten und die Anwendungsleistung verbessern. Diese Option ist standardmäßig nicht aktiviert.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Zurück</strong></p></td>
<td align="left"><p>Wechselt zur vorherigen Seite des Assistenten.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Nächste</strong></p></td>
<td align="left"><p>Wechselt zur nächsten Seite des Assistenten.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Abbrechen</strong></p></td>
<td align="left"><p>Verwirft die Einstellungen und beendet den Assistenten.</p></td>
</tr>
</tbody>
</table>



\ [Vorlage-Tokenwert \]

## Verwandte Themen


[Sequenz-Assistent](sequencing-wizard.md)









