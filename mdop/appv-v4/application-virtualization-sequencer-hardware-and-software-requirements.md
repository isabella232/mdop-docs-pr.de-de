---
title: Hardware- und Softwareanforderungen für Application Virtualization Sequencer
description: Hardware- und Softwareanforderungen für Application Virtualization Sequencer
author: dansimp
ms.assetid: c88a1b5b-23e1-4460-afa9-a5f37e32eb05
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d68afe4d4a3f6f301d38f2e86139d94319583467
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807980"
---
# Hardware- und Softwareanforderungen für Application Virtualization Sequencer


In diesem Thema werden die Mindestanforderungen für Hardware und Software für den Computer beschrieben, auf dem der Microsoft Application Virtualization (App-V)-Sequenzer ausgeführt wird.

**Wichtig**  Sie müssen den App-V-Sequencer (**SFTSequencer.exe**) mithilfe eines Kontos ausführen, das über Administratorberechtigungen verfügt, weil die Änderungen, die der Sequencer am lokalen System vornimmt, ausgeführt werden. Diese Änderungen können das Schreiben von Dateien in das **c:\\Programme-Datei** Verzeichnis, das vornehmen von Registrierungsänderungen, das Starten und Beenden von Diensten, das Aktualisieren von Sicherheitsbeschreibungen für Dateien und das Ändern von Berechtigungen umfassen.

 

Bevor Sie den Sequencer installieren und nachdem Sie die einzelnen Anwendungen sequenziert haben, müssen Sie ein sauberes Betriebssystemabbild auf dem Sequenzcomputer wiederherstellen. Mit einer der folgenden Methoden können Sie den Computer wiederherstellen, auf dem der Sequencer ausgeführt wird:

-   Formatieren Sie die Festplatte neu, und installieren Sie das Betriebssystem erneut.

-   Wiederherstellen der Festplatte auf dem Computer, auf dem das Sequenzer-Image ausgeführt wird, mithilfe einer anderen Datenträger-Imaging-Software.

-   Wiederherstellen eines virtuellen Betriebssystemabbilds wie einem Microsoft Virtual PC-Abbild Durch die Verwendung eines virtuellen Computers können saubere Sequenz Umgebungen problemlos wieder verwendet werden, wenn die Verwaltung minimal ist.

In der folgenden Liste werden die empfohlenen Hardwareanforderungen für die Ausführung des App-V-Sequencers erläutert.

Die Anforderungen werden zunächst für Microsoft Application Virtualization (app-v) 4.6 SP2 aufgeführt, gefolgt von den Anforderungen für Versionen, die APP-v 4.6 SP2 vorangestellt sind.

### <a href="" id="hardware-requirements-"></a>Hardwareanforderungen

-   Prozessor: Intel Pentium III, 1 GHz (32-Bit oder 64-Bit). Der Sequenzierungsprozess ist ein Single-Thread-Prozess und nutzt keine dualen Prozessoren.

-   Speicher – 1GB oder höher, 2GB empfohlen.

-   Festplatte – 40 Gigabyte (GB) Festplattenspeicher mit einem verfügbaren Festplattenspeicherplatz von 15 GB. Wir empfehlen, dass Sie mindestens dreimal so viel Festplattenspeicherplatz haben, wie es für die von Ihnen sequenzierte Anwendung erforderlich ist.

    **Hinweis**  Für die Sequenzierung ist eine starke Datenträgernutzung erforderlich. Eine schnelle Festplattengeschwindigkeit kann die Sequenzierungs Zeit verkleinern.

     

### Software Anforderungen für App-V 4,6 SP2

In der folgenden Liste werden die unterstützten Betriebssysteme für die Ausführung des App-V 4,6 SP2-Sequenzers erläutert.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Betriebssystem</th>
<th align="left">Edition</th>
<th align="left">Service Pack</th>
<th align="left">System Architektur</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>WindowsXP</p></td>
<td align="left"><p>Professional</p></td>
<td align="left"><p>SP3</p></td>
<td align="left"><p>x86</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Vista</p></td>
<td align="left"><p>Business, Enterprise oder Ultimate</p></td>
<td align="left"><p>SP2</p></td>
<td align="left"><p>x86</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows7</p></td>
<td align="left"><p>Professional, Enterprise oder Ultimate</p></td>
<td align="left"><p>Kein Service Pack oder SP1</p></td>
<td align="left"><p>x86 und x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows 8</p></td>
<td align="left"><p>Pro-oder Enterprise-Edition</p></td>
<td align="left"><p></p></td>
<td align="left"><p>x86 und x64</p></td>
</tr>
</tbody>
</table>

 

**Hinweis**  Der Application Virtualization (App-V) 4,6 SP2-Sequenzer unterstützt 32-Bit-und 64-Bit-Versionen dieser Betriebssysteme.

 

Sie sollten Computer, auf denen der Sequencer ausgeführt wird, mit denselben Anwendungen konfigurieren, die auf Zielcomputern installiert sind.

### Software Anforderungen für Versionen, die App-V 4,6 SP2 vorausgehen

In der folgenden Liste werden die unterstützten Betriebssysteme für die Ausführung des Sequencers für Versionen beschrieben, die App-V 4,6 SP2 vorangestellt sind.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Betriebssystem</th>
<th align="left">Edition</th>
<th align="left">Service Pack</th>
<th align="left">System Architektur</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>WindowsXP</p></td>
<td align="left"><p>Professional</p></td>
<td align="left"><p>SP2 oder SP3</p></td>
<td align="left"><p>x86</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Vista</p></td>
<td align="left"><p>Business, Enterprise oder Ultimate</p></td>
<td align="left"><p>Kein Service Pack, SP1 oder SP2</p></td>
<td align="left"><p>x86</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows7 ¹</p></td>
<td align="left"><p>Professional, Enterprise oder Ultimate</p></td>
<td align="left"><p></p></td>
<td align="left"><p>x86</p></td>
</tr>
</tbody>
</table>

 

¹ unterstützt für App-v 4,5 mit SP1 oder SP2 und nur App-v 4,6

**Hinweis**  Der Application Virtualization (App-V) 4,6-Sequenzer unterstützt 32-Bit-und 64-Bit-Versionen dieser Betriebssysteme.

 

Sie sollten Computer, auf denen der Sequencer ausgeführt wird, mit denselben Anwendungen konfigurieren, die auf Zielcomputern installiert sind.

### Software Anforderungen für Remote Desktop Dienste für App-V 4,6 SP2

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Betriebssystem</th>
<th align="left">Edition</th>
<th align="left">Service Pack</th>
<th align="left">System Architektur</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows Server2003 R2</p></td>
<td align="left"><p>Standard Edition, Enterprise Edition oder Datacenter Edition</p></td>
<td align="left"><p>SP2</p></td>
<td align="left"><p>x86</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008</p></td>
<td align="left"><p>Standard-, Enterprise-oder Datacenter-Edition</p></td>
<td align="left"><p>SP2</p></td>
<td align="left"><p>x86</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2008 R2</p></td>
<td align="left"><p>Standard-, Enterprise-oder Datacenter-Edition</p></td>
<td align="left"><p>Kein Service Pack oder SP1</p></td>
<td align="left"><p>x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2012</p></td>
<td align="left"><p>Standard-, Enterprise-oder Datacenter-Edition</p></td>
<td align="left"><p></p></td>
<td align="left"><p>x86 oder x64</p></td>
</tr>
</tbody>
</table>

 

**Hinweis**  Application Virtualization (App-V) 4,6 SP2 für Remote Desktop Dienste unterstützt 32-Bit-und 64-Bit-Versionen dieser Betriebssysteme.

 

### Software Anforderungen für Remote Desktop Dienste für Versionen, die App-V 4,6 SP2 vorausgehen

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Betriebssystem</th>
<th align="left">Edition</th>
<th align="left">Service Pack</th>
<th align="left">System Architektur</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows Server2003</p></td>
<td align="left"><p>Standard Edition, Enterprise Edition oder Datacenter Edition</p></td>
<td align="left"><p>SP1 oder SP2</p></td>
<td align="left"><p>x86</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2003 R2</p></td>
<td align="left"><p>Standard Edition, Enterprise Edition oder Datacenter Edition</p></td>
<td align="left"><p>Kein Service Pack oder SP2</p></td>
<td align="left"><p>x86</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2008</p></td>
<td align="left"><p>Standard-, Enterprise-oder Datacenter-Edition</p></td>
<td align="left"><p>SP1 oder SP2</p></td>
<td align="left"><p>x86</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008 R2</p></td>
<td align="left"><p>Standard-, Enterprise-oder Datacenter-Edition</p></td>
<td align="left"><p>Kein Service Pack oder SP1</p></td>
<td align="left"><p>x64</p></td>
</tr>
</tbody>
</table>

 

**Hinweis**  Application Virtualization (App-V) 4,6 SP2 für Remote Desktop Dienste unterstützt 32-Bit-und 64-Bit-Versionen dieser Betriebssysteme.

 

## Verwandte Themen


[Hardware- und Softwareanforderungen für Application Virtualization Client](application-virtualization-client-hardware-and-software-requirements.md)

[Systemanforderungen für Application Virtualization](application-virtualization-system-requirements.md)

[So installieren Sie Application Virtualization Sequencer](how-to-install-the-application-virtualization-sequencer.md)

[So aktualisieren Sie Application Virtualization Sequencer](how-to-upgrade-the-application-virtualization-sequencer.md)

 

 





