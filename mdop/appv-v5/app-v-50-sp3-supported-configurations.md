---
title: Unterstützte App-V 5.0 SP3-Konfigurationen
description: Unterstützte App-V 5.0 SP3-Konfigurationen
author: dansimp
ms.assetid: 08ced79a-0ed3-43c3-82e7-de01c1f33e81
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: b5a8858c703add3dc84c7eed4f62aa97e60ec9b0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805993"
---
# Unterstützte App-V 5.0 SP3-Konfigurationen


In diesem Thema werden die Anforderungen zum Installieren und Ausführen von Microsoft Application Virtualization (App-V) 5,0 SP3 in Ihrer Umgebung angegeben.

## Systemanforderungen für App-V Server


In diesem Abschnitt werden die Betriebssystem-und Hardwareanforderungen für alle App-V-Server Komponenten aufgelistet.

### Nicht unterstützte App-V 5,0 SP3-Server Szenarien

Der App-V 5,0 SP3-Server unterstützt die folgenden Szenarien nicht:

-   Bereitstellung auf einem Computer, auf dem Microsoft Windows Server Core ausgeführt wird

-   Bereitstellung auf einem Computer, auf dem eine frühere Version der App-V 5,0 SP3-Server Komponenten ausgeführt wird. Sie können APP-v 5,0 SP3 nebeneinander mit dem App-v 4.5 Lightweight Streaming Server (LWS)-Server installieren. Die Bereitstellung von App-v nebeneinander mit dem App-v 4,5 Application Virtualization Management Service (HWS)-Server wird nicht unterstützt.

-   Bereitstellung auf einem Computer, auf dem Microsoft SQL Server Express Edition ausgeführt wird

-   Remote Bereitstellung der Verwaltungsserver-Datenbank oder der Berichtsdatenbank Sie müssen das Installationsprogramm direkt auf dem Computer ausführen, auf dem Microsoft SQL Server ausgeführt wird.

-   Bereitstellung auf einem Domänencontroller.

-   Kurze Pfade. Wenn Sie einen kurzen Pfad verwenden möchten, müssen Sie einen neuen Datenträger erstellen.

### Betriebssystemanforderungen für Management Server

In der folgenden Tabelle sind die Betriebssysteme aufgeführt, die für die Installation des App-V 5,0 SP3-Verwaltungsservers unterstützt werden.

**Hinweis**  Microsoft bietet Unterstützung für das aktuelle Service Pack und in einigen Fällen das unmittelbar vorhergehende Service Pack. Informationen zu den Support Zeitachsen für Ihr Produkt finden Sie unter [unterstützte Service Packs für Lebenszyklen](https://go.microsoft.com/fwlink/p/?LinkId=31975). Weitere Informationen finden Sie unter [Supportrichtlinien für Microsoft Support-Lebenszyklus](https://go.microsoft.com/fwlink/p/?LinkId=31976) .

 

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Betriebssystem</th>
<th align="left">Service Pack</th>
<th align="left">System Architektur</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Microsoft Windows Server 2012 R2</p></td>
<td align="left"><p></p></td>
<td align="left"><p>64Bit</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft Windows Server 2012</p></td>
<td align="left"><p></p></td>
<td align="left"><p>64Bit</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Microsoft Windows Server 2008 R2</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>64Bit</p></td>
</tr>
</tbody>
</table>

 

**Wichtig**  Die Bereitstellung der Verwaltungsserverrolle auf einem Computer mit aktivierter Remote Desktop Freigabe (RDS) wird nicht unterstützt.

 

### <a href="" id="management-server-hardware-requirements-"></a>Hardwareanforderungen für den Verwaltungsserver

-   Prozessor – 1,4 GHz oder schneller, 64-Bit (x64)-Prozessor

-   RAM – 1 GB RAM (64-Bit)

-   Speicherplatz – 200 MB verfügbarer Festplattenspeicherplatz, nicht einschließlich des Inhaltsverzeichnisses

### Verwaltungsserver-Datenbankanforderungen

In der folgenden Tabelle sind die SQL Server-Versionen aufgeführt, die für die Installation der App-V 5,0 SP3-Verwaltungsdatenbank unterstützt werden.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">SQL Server-Version</th>
<th align="left">Service Pack</th>
<th align="left">System Architektur</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Microsoft SQL Server 2014</p></td>
<td align="left"><p></p></td>
<td align="left"><p>32 Bit oder 64 Bit</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft SQL Server 2012</p></td>
<td align="left"><p>SP2</p></td>
<td align="left"><p>32 Bit oder 64 Bit</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Microsoft SQL Server 2008 R2</p></td>
<td align="left"><p>SP3</p></td>
<td align="left"><p>32 Bit oder 64 Bit</p></td>
</tr>
</tbody>
</table>

 

### Betriebssystemanforderungen für Veröffentlichungsserver

In der folgenden Tabelle sind die Betriebssysteme aufgeführt, die für die Installation von App-V 5,0 SP3-Publishing Server unterstützt werden.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Betriebssystem</th>
<th align="left">Service Pack</th>
<th align="left">System Architektur</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Microsoft Windows Server 2012 R2</p></td>
<td align="left"><p></p></td>
<td align="left"><p>64Bit</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft Windows Server 2012</p></td>
<td align="left"><p></p></td>
<td align="left"><p>64Bit</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Microsoft Windows Server 2008 R2</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>64Bit</p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="publishing-server-hardware-requirements-"></a>Hardwareanforderungen für Veröffentlichungsserver

App-V bietet keine zusätzlichen Anforderungen, die über die von Windows Server hinausgehen.

-   Prozessor – 1,4 GHz oder schneller, 64-Bit (x64)-Prozessor

-   RAM – 2 GB RAM (64-Bit)

-   Speicherplatz – 200 MB verfügbarer Festplattenspeicherplatz, nicht einschließlich des Inhaltsverzeichnisses

### Anforderungen des Reporting Server-Betriebssystems

In der folgenden Tabelle sind die Betriebssysteme aufgeführt, die für die App-V 5,0 SP3 Reporting Server-Installation unterstützt werden.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Betriebssystem</th>
<th align="left">Service Pack</th>
<th align="left">System Architektur</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Microsoft Windows Server 2012 R2</p></td>
<td align="left"><p></p></td>
<td align="left"><p>64Bit</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft Windows Server 2012</p></td>
<td align="left"><p></p></td>
<td align="left"><p>64Bit</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Microsoft Windows Server 2008 R2</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>64Bit</p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="reporting-server-hardware-requirements-"></a>Hardwareanforderungen für den Berichtsserver

App-V bietet keine zusätzlichen Anforderungen, die über die von Windows Server hinausgehen.

-   Prozessor – 1,4 GHz oder schneller, 64-Bit (x64)-Prozessor

-   RAM – 2 GB RAM (64-Bit)

-   Speicherplatz – 200 MB verfügbarer Festplattenspeicherplatz

### Anforderungen für die Berichtsserver-Datenbank

In der folgenden Tabelle sind die SQL Server-Versionen aufgeführt, die für die App-V 5,0 SP3-Berichtsdatenbank-Installation unterstützt werden.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">SQL Server-Version</th>
<th align="left">Service Pack</th>
<th align="left">System Architektur</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Microsoft SQL Server 2014</p></td>
<td align="left"><p></p></td>
<td align="left"><p>32 Bit oder 64 Bit</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft SQL Server 2012</p></td>
<td align="left"><p>SP2</p></td>
<td align="left"><p>32 Bit oder 64 Bit</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Microsoft SQL Server 2008 R2</p></td>
<td align="left"><p>SP3</p></td>
<td align="left"><p>32 Bit oder 64 Bit</p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-client-supp-cfgs"></a>App-V-Clientsystemanforderungen


In der folgenden Tabelle sind die Betriebssysteme aufgeführt, die für die App-V 5,0 SP3-Clientinstallation unterstützt werden.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Betriebssystem</th>
<th align="left">Service Pack</th>
<th align="left">System Architektur</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Microsoft Windows 8.1</p></td>
<td align="left"><p></p></td>
<td align="left"><p>32 Bit oder 64 Bit</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft Windows8</p></td>
<td align="left"><p></p></td>
<td align="left"><p>32 Bit oder 64 Bit</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows7</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>32 Bit oder 64 Bit</p></td>
</tr>
</tbody>
</table>

 

Die folgenden App-V-Client Installationsszenarien werden nicht unterstützt, es sei denn, es wird angegeben:

-   Computer, auf denen Windows Server ausgeführt wird

-   Computer, auf denen App-v 4.6 SP1 oder frühere Versionen ausgeführt werden

-   Der App-V 5,0 SP3-Remote Desktop Dienste-Client wird nur für RDS-fähige Server unterstützt.

### <a href="" id="app-v-client-hardware-requirements-"></a>Hardwareanforderungen für App-V-Clients

In der folgenden Liste wird die unterstützte Hardwarekonfiguration für die App-V 5,0 SP3-Clientinstallation angezeigt.

-   Prozessor – 1,4 GHz oder schneller 32-Bit (x86) oder 64-Bit (x64)-Prozessor

-   RAM – 1 GB (32-Bit) oder 2 GB (64-Bit)

-   Datenträger – 100 MB für die Installation, nicht einschließlich des von virtualisierten Anwendungen verwendeten Speicherplatzes.

## Clientsystemanforderungen für Remote Desktop Dienste


In der folgenden Tabelle sind die Betriebssysteme aufgeführt, die für die App-V 5,0 SP3-Clientinstallation für Remote Desktop Dienste (RDS) unterstützt werden.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Betriebssystem</th>
<th align="left">Service Pack</th>
<th align="left">System Architektur</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Microsoft Windows Server 2012 R2</p></td>
<td align="left"><p></p></td>
<td align="left"><p>64Bit</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft Windows Server 2012</p></td>
<td align="left"><p></p></td>
<td align="left"><p>64Bit</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Microsoft Windows Server 2008 R2</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>64Bit</p></td>
</tr>
</tbody>
</table>

 

### Hardwareanforderungen für Remote Desktop Dienste-Clients

App-V bietet keine zusätzlichen Anforderungen, die über die von Windows Server hinausgehen.

-   Prozessor – 1,4 GHz oder schneller, 64-Bit (x64)-Prozessor

-   RAM – 2 GB RAM (64-Bit)

-   Speicherplatz – 200 MB verfügbarer Festplattenspeicherplatz

## Systemanforderungen für Sequencer


In der folgenden Tabelle sind die Betriebssysteme aufgeführt, die für die App-V 5,0 SP3-Sequencer-Installation unterstützt werden.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Betriebssystem</th>
<th align="left">Service Pack</th>
<th align="left">System Architektur</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Microsoft Windows Server2012 R2</p></td>
<td align="left"></td>
<td align="left"><p>64Bit</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft Windows Server2012</p></td>
<td align="left"><p></p></td>
<td align="left"><p>64Bit</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Microsoft Windows Server2008 R2</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>64Bit</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft Windows 8.1</p></td>
<td align="left"><p></p></td>
<td align="left"><p>32Bit und 64Bit</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Microsoft Windows8</p></td>
<td align="left"><p></p></td>
<td align="left"><p>32Bit und 64Bit</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft Windows7</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>32Bit und 64Bit</p></td>
</tr>
</tbody>
</table>

 

### Hardwareanforderungen für Sequenzer

Die Hardwareanforderungen finden Sie in der Windows-oder Windows Server-Dokumentation. App-V fügt keine zusätzlichen Hardwareanforderungen hinzu.

## <a href="" id="bkmk-supp-ver-sccm"></a>Unterstützte Versionen von System Center Configuration Manager


Der App-V-Client unterstützt die folgenden Versionen von System Center Configuration Manager:

-   MicrosoftSystemCenter2012 ConfigurationManager

-   System Center 2012 R2 Configuration Manager

-   System Center 2012 R2 Configuration Manager SP1

Weitere Informationen zur Integration von Configuration Manager in App-v finden Sie unter [Planen der APP-v-Integration in Configuration Manager](https://technet.microsoft.com/library/jj822982.aspx).






## Verwandte Themen


[Planen der Bereitstellung von App-V](planning-to-deploy-app-v.md)

[Voraussetzungen für App-V 5.0 SP3](app-v-50-sp3-prerequisites.md)

 

 





