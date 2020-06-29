---
title: Protokolldateien für Application Virtualization Sequencer
description: Protokolldateien für Application Virtualization Sequencer
author: dansimp
ms.assetid: 1a296544-eab4-46f9-82ce-3136f8b578af
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d8cdf9dbc78ccdd03df5903ef4d42990099a2c53
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806619"
---
# Protokolldateien für Application Virtualization Sequencer


Die Protokolldateien für den Application Virtualization (App-V)-Sequenzer liefern detaillierte Informationen zu Sequenz Anwendungen und können hilfreich sein, wenn Sie die Funktionalität überprüfen oder Probleme behandeln.

Die folgende Tabelle enthält Informationen zu den Protokolldateien und ihren Standardspeicherorten, die bei Verwendung des Sequencers erstellt werden.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Name der Protokolldatei</th>
<th align="left">Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>sft-seq-log.txt</strong></p></td>
<td align="left"><p>Enthält allgemeine Informationen zur Sequenzierung einer Anwendung. Verwenden Sie dieses Protokoll als Ausgangspunkt für die Problembehandlung von Sequencer-Fehlern.</p>
<p>Speicherort der Protokolldatei: <em> %windir%\Microsoft Application Virtualization Sequencer\Logs</em></p>
<p>[Vorlage-Tokenwert] App-v 4.6-Protokolldateispeicherort: <em> %windir%\Programme\Gemeinsame Dateien\Microsoft Application Virtualization Sequencer\Logs </em> [Vorlagen Tokenwert]</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>sftbt.txt</strong></p></td>
<td align="left"><p>Enthält Informationen zu Computerneustart Aufgaben, die während des simulierten Neustarts des Sequencers auftreten.</p>
<p>Speicherort der Protokolldatei: <em> %windir%\Microsoft Application Virtualization Sequencer\Logs</em></p>
<p>[Vorlage-Tokenwert] App-v 4.6-Protokolldateispeicherort: <em> %windir%\Programme\Gemeinsame Dateien\Microsoft Application Virtualization Sequencer\Logs </em> [Vorlagen Tokenwert]</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>SftCallBack.txt</strong></p></td>
<td align="left"><p>Bietet allgemeine Informationen zu Prozessen, die während der Sequenzierung verwendet werden.</p>
<p>Speicherort der Protokolldatei: <em> %windir%\Microsoft Application Virtualization Sequencer\Logs</em></p>
<p>[Vorlage-Tokenwert] App-v 4.6-Protokolldateispeicherort: <em> %windir%\Programme\Gemeinsame Dateien\Microsoft Application Virtualization Sequencer\Logs </em> [Vorlagen Tokenwert]</p></td>
</tr>
</tbody>
</table>

 

## Verwandte Themen


[Referenz zu Application Virtualization Sequencer](application-virtualization-sequencer-reference.md)

 

 





