---
title: Hardware- und Softwareanforderungen für Sequencer
description: Hardware- und Softwareanforderungen für Sequencer
author: dansimp
ms.assetid: 36084e12-831d-452f-a4a4-45f07f9ce471
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0d4e12a5803a3c9033513424826b49bc0bca5885
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806344"
---
# Hardware- und Softwareanforderungen für Sequencer


In diesem Thema werden die Mindestanforderungen für Hardware und Software für den Computer beschrieben, auf dem der Microsoft Application Virtualization (App-V)-Sequenzer ausgeführt wird.

Bevor Sie den Sequencer installieren und nachdem Sie die einzelnen Anwendungen sequenziert haben, müssen Sie ein sauberes Betriebssystemabbild auf dem Sequenzcomputer wiederherstellen. Mit einer der folgenden Methoden können Sie den Computer wiederherstellen, auf dem der Sequencer ausgeführt wird:

-   Formatieren Sie die Festplatte neu, und installieren Sie das Betriebssystem erneut.

-   Wiederherstellen der Festplatte auf dem Computer, auf dem das Sequenzer-Image ausgeführt wird, mithilfe einer anderen Datenträger-Imaging-Software.

In der folgenden Liste werden die empfohlenen Hardwareanforderungen für die Ausführung des App-V-Sequencers erläutert.

### <a href="" id="hardware-requirements-"></a>Hardwareanforderungen

-   Prozessor: Intel Pentium III, 1 GHz (32-Bit oder 64-Bit). Der Sequenzierungsprozess ist ein Single-Thread-Prozess und nutzt keine dualen Prozessoren.

-   Arbeitsspeicher – 1GB oder höher, 2 GB empfohlen.

-   Festplatte – 40 Gigabyte (GB) Festplattenspeicher mit einem verfügbaren Festplattenspeicherplatz von 15 GB. Wir empfehlen, dass Sie mindestens dreimal so viel Festplattenspeicherplatz haben, wie es für die von Ihnen sequenzierte Anwendung erforderlich ist.

    **Hinweis**  Für die Sequenzierung ist eine starke Datenträgernutzung erforderlich. Eine schnelle Festplattengeschwindigkeit kann die Sequenzierungs Zeit verkleinern.

     

### Software Anforderungen

In der folgenden Liste werden die unterstützten Betriebssysteme für die Ausführung des Sequencers erläutert.

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

### Software Anforderungen für Remote Desktop Dienste

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
<td align="left"><p></p></td>
<td align="left"><p>x86</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2008</p></td>
<td align="left"><p>Standard, Enterprise oder Datacenter</p></td>
<td align="left"><p>SP1 oder SP2</p></td>
<td align="left"><p>x86</p></td>
</tr>
</tbody>
</table>

 

**Hinweis**  Application Virtualization (App-V) 4,6 für Remote Desktop Dienste unterstützt 32-Bit-und 64-Bit-Versionen dieser Betriebssysteme.

 

## Verwandte Themen


[Application Virtualization Sequencer – Übersicht](application-virtualization-sequencer-overview.md)

 

 





