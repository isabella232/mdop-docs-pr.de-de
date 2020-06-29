---
title: Planen der Erstellung des DaRT 8.0-Wiederherstellungsabbilds
description: Planen der Erstellung des DaRT 8.0-Wiederherstellungsabbilds
author: dansimp
ms.assetid: cfd0e1e2-c379-4460-b545-3f7be9f33583
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 1d1dc7dc5b3776638523a282d9216b80d4ce9ce1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810777"
---
# Planen der Erstellung des DaRT 8.0-Wiederherstellungsabbilds


Verwenden Sie die Informationen in diesem Abschnitt, wenn Sie beabsichtigen, das Microsoft Diagnostics and Recovery Toolset (Dart) 8,0-Wiederherstellungsbild zu erstellen.

## Planen des Erstellens des Dart 8,0-Wiederherstellungs Bilds


Wenn Sie das DART-Wiederherstellungsbild erstellen, müssen Sie entscheiden, welche Tools in das Bild aufgenommen werden sollen. Um die Entscheidung zu treffen, sollten Endbenutzer möglicherweise auf diese Tools zugreifen. Wenn Supporttechniker die Wiederherstellungsbild Medien auf die Computer der Endbenutzer übertragen, um Probleme zu diagnostizieren, möchten Sie möglicherweise alle Tools auf dem Wiederherstellungsabbild installieren. Wenn Sie beabsichtigen, die Computer des Endbenutzers Remote zu diagnostizieren, möchten Sie möglicherweise einige der Tools wie Datenträger Zurücksetzung und Registrierungs-Editor deaktivieren und dann andere Tools, einschließlich Remote Verbindung, aktivieren.

Wenn Sie das DART-Wiederherstellungsabbild erstellen, geben Sie auch an, ob Sie weitere Treiber oder Dateien einbeziehen möchten. Ermitteln Sie die Speicherorte zusätzlicher Treiber oder Dateien, die Sie in das DART-Wiederherstellungsabbild einbeziehen möchten.

Weitere Informationen zu den Dart-Tools finden Sie unter [Übersicht über die Tools in Dart 8,0](overview-of-the-tools-in-dart-80-dart-8.md). Weitere Informationen dazu, wie Sie bei der Erstellung eines sicheren Wiederherstellungs Bilds helfen können, finden Sie unter [Sicherheitsüberlegungen für Dart 8,0](security-considerations-for-dart-80--dart-8.md).

## Voraussetzungen für das Wiederherstellungsabbild


Die folgenden Elemente sind für das Erstellen des DART-Wiederherstellungs Bilds erforderlich oder empfohlen:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Voraussetzung</strong></p></td>
<td align="left"><p><strong>Details</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows 8-Quelldateien</p></td>
<td align="left"><p>Erforderlich, um das DART-Wiederherstellungsbild zu erstellen. Geben Sie den Pfad einer Windows 8-DVD oder von Windows 8-Quelldateien an.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows-Debugging-Tools für Ihre Plattform</p></td>
<td align="left"><p>Erforderlich, wenn Sie den <strong> Absturzanalyse Programm ausführen </strong> , um die Ursache für einen Computer Fehler zu ermitteln. Wir empfehlen, dass Sie den Pfad der Windows-Debugging-Tools angeben, wenn Sie das DART-Wiederherstellungsabbild erstellen. Sie können die Windows-Debugging-Tools hier herunterladen: <a href="https://go.microsoft.com/fwlink/?LinkId=99934" data-raw-source="[Download and Install Debugging Tools for Windows](https://go.microsoft.com/fwlink/?LinkId=99934)"> herunterladen und Installieren von Debugging-Tools für Windows </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Optional: <strong> Defender- </strong> Definitionen</p></td>
<td align="left"><p>Die neuesten Definitionen für <strong> Defender </strong> sind erforderlich, wenn Sie <strong> Defender ausführen </strong> . Obwohl Sie die Definitionen beim Ausführen <strong> von Defender herunterladen können </strong> , empfehlen wir, dass Sie die neuesten Definitionen zum Zeitpunkt der Erstellung des DART-Wiederherstellungsabbilds herunterladen, damit Sie das Tool weiterhin mit den neuesten Definitionen ausführen können, auch wenn der Problem Computer nicht über Netzwerkkonnektivität verfügt.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Optional: Windows-Symbole-Dateien für die Verwendung mit <strong> Crash Analyzer</strong></p></td>
<td align="left"><p>In der Regel werden Debuginformationen in einer vom Programm getrennten Symboldatei gespeichert. Sie müssen Zugriff auf die Symbol Informationen haben, wenn Sie eine Anwendung debuggen, die nicht mehr reagiert, beispielsweise wenn Sie nicht mehr funktioniert. Weitere Informationen finden Sie unter <a href="diagnosing-system-failures-with-crash-analyzer--dart-8.md" data-raw-source="[Diagnosing System Failures with Crash Analyzer](diagnosing-system-failures-with-crash-analyzer--dart-8.md)"> Diagnostizieren von System Fehlern mit Crash Analyzer </a> .</p></td>
</tr>
</tbody>
</table>

 

## Verwandte Themen


[Planen der Bereitstellung von DaRT 8.0](planning-to-deploy-dart-80-dart-8.md)

 

 





