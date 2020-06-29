---
title: App-V 5.1 – Unterstützte Konfigurationen
description: App-V 5.1 – Unterstützte Konfigurationen
author: dansimp
ms.assetid: 8b8db63b-f71c-4ae9-80e7-a6752334e1f6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 04/02/2020
ms.openlocfilehash: fbda364de66b1f7b8730dca38f864a84f7848e58
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805942"
---
# App-V 5.1 – Unterstützte Konfigurationen

>Gilt für: Windows 10, Version 1607; Window Server 2019; Windows Server 2016; Windows Server 2012 R2; Windows Server 2012; Windows Server 2008 R2 (erweitertes Sicherheits Update)

In diesem Thema werden die Anforderungen zum Installieren und Ausführen von Microsoft Application Virtualization (App-V) 5,1 in Ihrer Umgebung angegeben.

## Systemanforderungen für App-V Server

In diesem Abschnitt werden die Betriebssystem-und Hardwareanforderungen für alle App-V-Server Komponenten aufgelistet.

### Nicht unterstützte App-V 5,1-Server Szenarien

Der App-V 5,1-Server unterstützt die folgenden Szenarien nicht:

-   Bereitstellung auf einem Computer, auf dem Microsoft Windows Server Core ausgeführt wird

-   Bereitstellung auf einem Computer, auf dem eine frühere Version der App-V 5,1-Server Komponenten ausgeführt wird. Sie können APP-v 5,1 nebeneinander mit dem App-v 4.5 Lightweight Streaming Server (LWS)-Server installieren. Die Bereitstellung von App-v nebeneinander mit dem App-v 4,5 Application Virtualization Management Service (HWS)-Server wird nicht unterstützt.

-   Bereitstellung auf einem Computer, auf dem Microsoft SQL Server Express Edition ausgeführt wird

-   Bereitstellung auf einem Domänencontroller.

-   Kurze Pfade. Wenn Sie einen kurzen Pfad verwenden möchten, müssen Sie einen neuen Datenträger erstellen.

### Betriebssystemanforderungen für Management Server

In der folgenden Tabelle sind die Betriebssysteme aufgeführt, die für die Installation des App-V 5,1-Verwaltungsservers unterstützt werden.

> [!NOTE]
> Microsoft bietet Unterstützung für das aktuelle Service Pack und in einigen Fällen das unmittelbar vorhergehende Service Pack. Informationen zu den Support Zeitachsen für Ihr Produkt finden Sie unter [unterstützte Service Packs für Lebenszyklen](https://go.microsoft.com/fwlink/p/?LinkId=31975). Weitere Informationen finden Sie unter [Supportrichtlinien für Microsoft Support-Lebenszyklus](https://go.microsoft.com/fwlink/p/?LinkId=31976) .

 | Betriebssystem                 | Service Pack | System Architektur |
|----------------------------------|--------------|---------------------|
| Microsoft Windows Server 2019    |              |        64Bit       |
| Microsoft Windows Server 2016    |              |        64Bit       |
| Microsoft Windows Server 2012 R2 |              |        64Bit       |
| Microsoft Windows Server 2012    |              |        64Bit       |
| [Erweitertes Sicherheits Update](https://www.microsoft.com/windows-server/extended-security-updates) für Microsoft Windows Server 2008 R2|      SP1     |        64Bit       |
 

**Wichtig**  Die Bereitstellung der Verwaltungsserverrolle auf einem Computer mit aktivierter Remote Desktop Freigabe (RDS) wird nicht unterstützt.

 

### <a href="" id="management-server-hardware-requirements-"></a>Hardwareanforderungen für den Verwaltungsserver

-   Prozessor – 1,4 GHz oder schneller, 64-Bit (x64)-Prozessor

-   RAM – 1 GB RAM (64-Bit)

-   Speicherplatz – 200 MB verfügbarer Festplattenspeicherplatz, nicht einschließlich des Inhaltsverzeichnisses

### Verwaltungsserver-Datenbankanforderungen

In der folgenden Tabelle sind die SQL Server-Versionen aufgeführt, die für die Installation der App-V 5,1-Verwaltungsdatenbank unterstützt werden.

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
<tr class="even">
<td align="left"><p>Microsoft SQL Server 2019</p></td>
<td align="left"><p></p></td>
<td align="left"><p>32 Bit oder 64 Bit</p></td>
</tr>

<tr class="odd">
<td align="left"><p>Microsoft SQL Server 2017</p></td>
<td align="left"><p></p></td>
<td align="left"><p>32 Bit oder 64 Bit</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft SQL Server 2016</p></td>
<td align="left"><p>SP2</p></td>
<td align="left"><p>32 Bit oder 64 Bit</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Microsoft SQL Server 2014</p></td>
<td align="left"><p>SP2</p></td>
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

Weitere Informationen zu Benutzer Konfigurationsdateien mit SQL Server 2016 oder höher finden Sie im [Support Artikel](https://support.microsoft.com/help/4548751/app-v-server-publishing-might-fail-when-you-apply-user-configuration-f).

### Betriebssystemanforderungen für Veröffentlichungsserver

In der folgenden Tabelle sind die Betriebssysteme aufgeführt, die für die Installation des App-V 5,1-Publishing Servers unterstützt werden.

| Betriebssystem                 | Service Pack | System Architektur |
|----------------------------------|--------------|---------------------|
| Microsoft Windows Server 2019    |              |        64Bit       |
| Microsoft Windows Server 2016    |              |        64Bit       |
| Microsoft Windows Server 2012 R2 |              |        64Bit       |
| Microsoft Windows Server 2012    |              |        64Bit       |
| [Erweitertes Sicherheits Update](https://www.microsoft.com/windows-server/extended-security-updates) für Microsoft Windows Server 2008 R2 |      SP1     |        64Bit       |

### <a href="" id="publishing-server-hardware-requirements-"></a>Hardwareanforderungen für Veröffentlichungsserver

App-V bietet keine zusätzlichen Anforderungen, die über die von Windows Server hinausgehen.

-   Prozessor – 1,4 GHz oder schneller, 64-Bit (x64)-Prozessor

-   RAM – 2 GB RAM (64-Bit)

-   Speicherplatz – 200 MB verfügbarer Festplattenspeicherplatz, nicht einschließlich des Inhaltsverzeichnisses

### Anforderungen des Reporting Server-Betriebssystems

In der folgenden Tabelle sind die Betriebssysteme aufgeführt, die für die App-V 5,1 Reporting Server-Installation unterstützt werden.

| Betriebssystem                 | Service Pack | System Architektur |
|----------------------------------|--------------|---------------------|
| Microsoft Windows Server 2019    |              |        64Bit       |
| Microsoft Windows Server 2016    |              |        64Bit       |
| Microsoft Windows Server 2012 R2 |              |        64Bit       |
| Microsoft Windows Server 2012    |              |        64Bit       |
| [Erweitertes Sicherheits Update](https://www.microsoft.com/windows-server/extended-security-updates) für Microsoft Windows Server 2008 R2 |      SP1     |        64Bit       |

### <a href="" id="reporting-server-hardware-requirements-"></a>Hardwareanforderungen für den Berichtsserver

App-V bietet keine zusätzlichen Anforderungen, die über die von Windows Server hinausgehen.

-   Prozessor – 1,4 GHz oder schneller, 64-Bit (x64)-Prozessor

-   RAM – 2 GB RAM (64-Bit)

-   Speicherplatz – 200 MB verfügbarer Festplattenspeicherplatz

### Anforderungen für die Berichtsserver-Datenbank

In der folgenden Tabelle sind die SQL Server-Versionen aufgeführt, die für die Installation der App-V 5,1-Berichtsdatenbank unterstützt werden.

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
<td align="left"><p>Microsoft SQL Server 2017</p></td>
<td align="left"><p></p></td>
<td align="left"><p>32 Bit oder 64 Bit</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft SQL Server 2016</p></td>
<td align="left"><p>SP2</p></td>
<td align="left"><p>32 Bit oder 64 Bit</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Microsoft SQL Server 2014</p></td>
<td align="left"><p>SP2</p></td>
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

In der folgenden Tabelle sind die Betriebssysteme aufgeführt, die für die App-V 5,1-Clientinstallation unterstützt werden.

> [!NOTE]
> Mit der Windows 10-Anniversary-Version (aka 1607-Version) ist der APP-v-Client in-Box und blockiert die Installation einer früheren Version des App-v-Clients.

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
<td align="left"><p>Microsoft Windows10 (Pre-1607-Version)</p></td>
<td align="left"><p></p></td>
<td align="left"><p>32 Bit oder 64 Bit</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft Windows 8.1</p></td>
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

-   Der App-V 5,1-Client für Remote Desktop Dienste wird nur für RDS-fähige Server unterstützt.

### <a href="" id="app-v-client-hardware-requirements-"></a>Hardwareanforderungen für App-V-Clients

In der folgenden Liste wird die unterstützte Hardwarekonfiguration für die App-V 5,1-Clientinstallation angezeigt.

-   Prozessor – 1,4 GHz oder schneller 32-Bit (x86) oder 64-Bit (x64)-Prozessor

-   RAM – 1 GB (32-Bit) oder 2 GB (64-Bit)

-   Datenträger – 100 MB für die Installation, nicht einschließlich des von virtualisierten Anwendungen verwendeten Speicherplatzes.

## Clientsystemanforderungen für Remote Desktop Dienste


In der folgenden Tabelle sind die Betriebssysteme aufgeführt, die für die App-V 5,1-Clientinstallation für Remote Desktop Dienste (RDS) unterstützt werden.

| Betriebssystem                 | Service Pack | System Architektur |
|----------------------------------|--------------|---------------------|
| Microsoft Windows Server 2019    |              |        64Bit       |
| Microsoft Windows Server 2016    |              |        64Bit       |
| Microsoft Windows Server 2012 R2 |              |        64Bit       |
| Microsoft Windows Server 2012    |              |        64Bit       |
| [Erweitertes Sicherheits Update](https://www.microsoft.com/windows-server/extended-security-updates) für Microsoft Windows Server 2008 R2 |      SP1     |        64Bit       |

### Hardwareanforderungen für Remote Desktop Dienste-Clients

App-V bietet keine zusätzlichen Anforderungen, die über die von Windows Server hinausgehen.

-   Prozessor – 1,4 GHz oder schneller, 64-Bit (x64)-Prozessor

-   RAM – 2 GB RAM (64-Bit)

-   Speicherplatz – 200 MB verfügbarer Festplattenspeicherplatz

## Systemanforderungen für Sequencer

In der folgenden Tabelle sind die Betriebssysteme aufgeführt, die für die App-V 5,1 Sequencer-Installation unterstützt werden.

| Betriebssystem                 | Service Pack | System Architektur |
|----------------------------------|--------------|---------------------|
| Microsoft Windows Server 2019    |              |        64Bit       |
| Microsoft Windows Server 2016    |              |        64Bit       |
| Microsoft Windows Server 2012 R2 |              |        64Bit       |
| Microsoft Windows Server 2012    |              |        64Bit       |
| [Erweitertes Sicherheits Update](https://www.microsoft.com/windows-server/extended-security-updates) für Microsoft Windows Server 2008 R2 |      SP1     |        64Bit       |
| Microsoft Windows 10             |              | 32Bit und 64Bit   |
| Microsoft Windows 8,1            |              | 32Bit und 64Bit   |
| Microsoft Windows 7              |      SP1     | 32Bit und 64Bit   |

### Hardwareanforderungen für Sequenzer

Die Hardwareanforderungen finden Sie in der Windows-oder Windows Server-Dokumentation. App-V fügt keine zusätzlichen Hardwareanforderungen hinzu.

## <a href="" id="bkmk-supp-ver-sccm"></a>Unterstützte Versionen von System Center Configuration Manager

Der App-V-Client unterstützt die folgenden Versionen von System Center Configuration Manager:

-   MicrosoftSystemCenter2012 ConfigurationManager

-   System Center 2012 R2 Configuration Manager

-   System Center 2012 R2 Configuration Manager SP1

Die folgende APP-v-und System Center Configuration Manager-Versionsmatrix zeigt alle offiziell unterstützten Kombinationen von App-v und Configuration Manager.

> [!NOTE]
> Sowohl App-V 4,5 als auch 4,6 haben die Mainstream-Unterstützung beendet.

<table>
<colgroup>
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">App-V-Version</th>
<th align="left">System Center Configuration Manager 2007</th>
<th align="left">System Center 2012 Configuration Manager</th>
<th align="left">System Center 2012 Configuration Manager SP1</th>
<th align="left">System Center 2012 R2 Configuration Manager</th>
<th align="left">System Center 2012 R2 Configuration Manager SP1</th>
<th align="left">System Center 2012 Configuration Manager SP2</th>
<th align="left">System Center Configuration Manager, Version 1511</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>App-V 5,0 SP3</p></td>
<td align="left"><p>Nur MSI-Wrapper</p></td>
<td align="left"><p>Nein</p></td>
<td align="left"><p>2012 SP1 CU4</p></td>
<td align="left"><p>2012 R2 CU1</p></td>
<td align="left"><p>Ja</p></td>
<td align="left"><p>Ja</p></td>
<td align="left"><p>Ja</p></td>
</tr>
<tr class="even">
<td align="left"><p>App-V 5.1</p></td>
<td align="left"><p>Nur MSI-Wrapper</p></td>
<td align="left"><p>Nein</p></td>
<td align="left"><p>2012 SP1 CU4</p></td>
<td align="left"><p>2012 R2 CU1</p></td>
<td align="left"><p>Ja</p></td>
<td align="left"><p>Ja</p></td>
<td align="left"><p>Ja</p></td>
</tr>
</tbody>
</table>

 

Weitere Informationen zur Integration von Configuration Manager in App-v finden Sie unter [Planen der APP-v-Integration in Configuration Manager](https://technet.microsoft.com/library/jj822982.aspx).

## Verwandte Themen

[Planen der Bereitstellung von App-V](planning-to-deploy-app-v51.md)

[Voraussetzungen für App-V 5.1](app-v-51-prerequisites.md)
