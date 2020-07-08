---
title: Bestimmen der Veröffentlichungsmethode
description: Bestimmen der Veröffentlichungsmethode
author: dansimp
ms.assetid: 1f2d0d39-5d65-457a-b826-4f45b00c8c85
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9a6b19b12c28ab67e3250909cb32ddb8419f399a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808899"
---
# Bestimmen der Veröffentlichungsmethode


Nachdem Sie eine Anwendung mithilfe von Application Virtualization Sequencer sequenziert haben, müssen Sie diese Anwendung für Ihre Benutzer *veröffentlichen* . Die Veröffentlichung der Anwendung besteht darin, die Symbole, Paketdefinitionsinformationen und den Speicherort der Inhaltsquelle auf jedem Computer bereitzustellen, auf dem der Application Virtualization-Client installiert wurde. In der folgenden Tabelle werden die Veröffentlichungsmethoden beschrieben, die bei der Bereitstellung von Application Virtualization mithilfe eines ESD-Systems (Electronic Software Distribution) unterstützt werden.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Methode</th>
<th align="left">Vorteile</th>
<th align="left">Nachteile</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Generieren Sie eine Windows Installer-Datei während der Sequenzierung als eigenständige Lösung.</p></td>
<td align="left"><ul>
<li><p>Sehr einfach zu verwenden.</p></li>
<li><p>Das Paket wurde lokal auf jedem Computer in den Cache geladen.</p></li>
<li><p>Symbole, die dem Benutzer angezeigt werden.</p></li>
<li><p>Ähnlich wie herkömmliche Softwarebereitstellung.</p></li>
<li><p>Keine Notwendigkeit für Streaming-Server.</p></li>
</ul></td>
<td align="left"><ul>
<li><p>Keine Flexibilität beim Speicherort von Paketinhalten auf Computern – derselbe Standort auf allen Computern.</p></li>
<li><p>Sie müssen nur Programme hinzufügen/entfernen oder msiexec verwenden, um Anwendungen zu entfernen.</p></li>
<li><p>Entfernen und ersetzen durch neue Version, die für die Paketaktualisierung erforderlich ist.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Generieren Sie während der Sequenzierung eine Windows Installer-Datei, die mit den Befehlszeileneigenschaften Mode, Load und OVERRIDEURL und dem Paketmanifest verwendet wird.</p></td>
<td align="left"><ul>
<li><p>Einfach zu verwenden, aber mit zusätzlicher Flexibilität.</p></li>
<li><p>Symbole, die dem Benutzer angezeigt werden.</p></li>
<li><p>SFT-Datei, die die Anwendungen enthält, kann an einem Streaming-Quellspeicherort abgelegt werden, wobei die Clients für die Verwendung dieses Speicherorts konfiguriert sind.</p></li>
</ul></td>
<td align="left"><ul>
<li><p>Begrenzte Flexibilität – nur der Speicherort des Paketinhalts kann zur Laufzeit gesteuert werden.</p></li>
<li><p>Sie müssen nur Programme hinzufügen/entfernen oder msiexec verwenden, um die Anwendung zu entfernen.</p></li>
<li><p>Entfernen und ersetzen mit der neuen Version, die für die Paketaktualisierung erforderlich ist, es sei denn, Sie verwenden Streaming Server.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>Führen Sie SFTMIME-Befehle aus.</p></td>
<td align="left"><ul>
<li><p>Vollständige Flexibilität – vollständige Kontrolle über alle Paketverwaltungsfunktionen.</p></li>
</ul></td>
<td align="left"><ul>
<li><p>Befehle müssen für die Verwendung mit dem ESD-System skriptiert werden.</p></li>
<li><p>Befehle müssen auf jedem Computer in der richtigen Reihenfolge ausgeführt werden.</p></li>
<li><p>Detailliertes Verständnis der Befehlssprache und sorgfältige Planung erforderlich.</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

Weitere Informationen zum Verwenden dieser Veröffentlichungsmethoden finden Sie unter [Veröffentlichen einer virtuellen Anwendung auf dem Client](how-to-publish-a-virtual-application-on-the-client.md).

## Verwandte Themen


[Bestimmen der Streaming-Methode](determine-your-streaming-method.md)

[Electronic Software Distribution-basiertes Szenario](electronic-software-distribution-based-scenario.md)

[Übersicht über Electronic Software Distribution-basierte Szenarien](electronic-software-distribution-based-scenario-overview.md)

[So veröffentlichen Sie eine virtuelle Anwendung auf dem Client](how-to-publish-a-virtual-application-on-the-client.md)

[SFTMIME-Befehlsreferenz](sftmime--command-reference.md)

 

 





