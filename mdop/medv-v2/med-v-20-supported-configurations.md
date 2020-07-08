---
title: Von MED 2.0 unterstützte Konfigurationen
description: Von MED 2.0 unterstützte Konfigurationen
author: dansimp
ms.assetid: 88f1d232-aa01-45ab-8da7-d086269250b5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0fed090ec04cf67a32b13533f4003c01ae167493
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811023"
---
# Von MED 2.0 unterstützte Konfigurationen


Ihre Umgebung erfüllt möglicherweise bereits die Konfigurationsanforderungen, die hier bereitgestellt werden, damit Sie Microsoft Enterprise Desktop Virtualization (MED-V) 2,0 installieren und ausführen können. Wir haben Anforderungen wie Hostbetriebssystem, Festplattenspeicher und MED-V-Arbeitsbereichs Anforderungen berücksichtigt.

## Med-v 2.0-Host Computer Anforderungen


### MED-V 2,0 Host-Betriebs System Anforderungen

In der folgenden Tabelle sind die Betriebssysteme aufgeführt, die für die MED-V 2,0-Installation auf dem Hostcomputer unterstützt werden.

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
<td align="left"><p>Windows7</p></td>
<td align="left"><p>Professional, Enterprise oder Ultimate</p></td>
<td align="left"><p>Keine oder SP1</p></td>
<td align="left"><p>x86 oder x64</p></td>
</tr>
</tbody>
</table>

 

In der folgenden Tabelle ist der minimale Arbeitsspeicher für jedes Betriebssystem aufgeführt, das in MED-V 2,0 unterstützt wird.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Betriebssystem</th>
<th align="left">Minimaler erforderlicher Arbeitsspeicher</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows7 x86</p></td>
<td align="left"><p>2GB</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows7 x64</p></td>
<td align="left"><p>2GB</p></td>
</tr>
</tbody>
</table>

 

### Minimaler empfohlener Speicherplatz

Wir empfehlen eine Mindestkapazität von 10 GB verfügbarem Speicher. Der erforderliche Speicherplatz variiert jedoch stark und hängt von der Anzahl der im MED-V-Arbeitsbereich veröffentlichten Anwendungen ab.

### <a href="" id="med-v-2-0-host-configuration-"></a>Med-v 2.0-Host Konfiguration

**.NET Framework-Version**

Die .NET Framework 3.5 SP1-Version von Microsoft .NET Framework ist für MED-V 2,0 erforderlich. Sie können jedoch .NET Framework 4 oder höhere Versionen installieren, wenn .NET Framework 3,5 bereits installiert ist.

**Virtualisierungs-Engine**

Windows Virtual PCwith der im Microsoft Knowledge Base-Artikel 977206 beschriebene Hotfix wird für MED-V 2,0 unterstützt.

**Internet Browser**

Windows Internet Explorer8 und Windows Internet Explorer 9 werden für MED-V 2,0 unterstützt.

**Microsoft-Server Umgebungen**

Der Med-v-Host-Agent und der Med-v-Arbeitsbereichs-Packager werden in keiner Server Umgebung unterstützt.

## Med-v 2.0-Arbeitsbereichs Anforderungen


### Betriebs System Anforderungen für MED-V 2,0-Arbeitsbereiche

In der folgenden Tabelle sind die Betriebssysteme aufgeführt, die für MED-V 2,0-Arbeitsbereiche unterstützt werden.

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
<td align="left"><p>Professional Edition</p></td>
<td align="left"><p>SP3</p></td>
<td align="left"><p>x86</p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="med-v-2-0-workspace-configuration-"></a>Med-v 2.0 Workspace-Konfiguration

**.NET Framework-Version**

Nur die .NET Framework 3.5 SP1-Version von Microsoft .NET Framework wird für die MED-V 2,0 Workspace-Installation unterstützt.

**Internet Browser**

Windows Internet Explorer6, Windows Internet Explorer7, Windows Internet Explorer8 und Windows Internet Explorer9 werden für die MED-V 2,0 Workspace-Installation unterstützt.

### MED-V 2,0-Arbeitsbereichserstellung

Die virtuelle Festplatte, die zum Erstellen eines MED-V 2,0-Arbeitsbereichs Pakets verwendet wird, muss mithilfe von Windows Virtual PC erstellt werden.

## MED-V 2,0-Globalisierungsinformationen


### MED-V 2,0-Globalisierungsinformationen des Host-Agents

Die folgenden Sprachversionen des Windows-Betriebssystems werden für den MED-V 2,0-Host-Agent unterstützt:

-   Französisch

-   Italienisch

-   Deutsch

-   Spanisch

-   Koreanisch

-   Japanisch

-   Portugiesisch (Brasilien)

-   Russisch

-   Chinesisch (traditionell)

-   Chinesisch vereinfacht

-   Niederländisch

-   Schwedisch

-   Dänisch

-   Finnisch

-   Portugiesisch

-   Norwegisch

-   Polnisch

-   Türkisch

-   Ungarisch

-   Tschechisch

-   Griechisch

-   Slowakisch

-   Slowenisch

### Globalisierungsinformationen für MED-V 2,0-Arbeitsbereichs Pakete

Die folgenden Sprachversionen des Windows-Betriebssystems werden für das MED-V 2,0-Arbeitsbereichs Paket unterstützt:

-   Französisch

-   Italienisch

-   Deutsch

-   Spanisch

-   Koreanisch

-   Japanisch

-   Portugiesisch (Brasilien)

-   Russisch

-   Chinesisch (traditionell)

-   Chinesisch vereinfacht

## Verwandte Themen


[Bereitstellung von MED-V](deployment-of-med-v.md)

 

 





