---
title: Unterstützte App-V 5.0-Konfigurationen
description: Unterstützte App-V 5.0-Konfigurationen
author: dansimp
ms.assetid: 3787ff63-7ce7-45a8-8f01-81b4b6dced34
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 60236743d2a6b418ca7f4705168a7bf064b82156
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805990"
---
# Unterstützte App-V 5.0-Konfigurationen


In diesem Thema werden die Anforderungen beschrieben, die erforderlich sind, um Microsoft Application Virtualization (App-V) 5,0 in Ihrer Umgebung zu installieren und auszuführen.

**Wichtig**  
**Die unterstützten Konfigurationen in diesem Artikel gelten nur für App-V 5,0**. Informationen zu unterstützten Konfigurationen, die für App-V 5,0-Service Packs gelten, finden Sie auf den folgenden Webseiten:

-   [Neuigkeiten in App-V 5.0 SP1](whats-new-in-app-v-50-sp1.md)

-   [Informationen zu App-V 5.0 SP2](about-app-v-50-sp2.md)

-   [Unterstützte App-V 5.0 SP3-Konfigurationen](app-v-50-sp3-supported-configurations.md)



## <a href="" id="---------app-v-5-0-server-system-requirements"></a> Systemanforderungen für App-V 5,0 Server


**Wichtig**  
Der App-V 5,0-Server unterstützt die folgenden Szenarien nicht:



-   Bereitstellung auf einem Computer, auf dem Microsoft Windows Server Core ausgeführt wird

-   Bereitstellung auf einem Computer, auf dem eine frühere Version der App-V 5,0-Server Komponenten ausgeführt wird.

    **Hinweis:**  
    Sie können APP-v 5,0 nebeneinander mit dem App-v 4,5 Lightweight Streaming Server (LWS)-Server installieren. Die Bereitstellung von App-v 5,0 nebeneinander mit dem App-v 4,5 Application Virtualization Management Service (HWS)-Server wird nicht unterstützt.



-   Bereitstellung auf einem Computer, auf dem Microsoft SQL Server Express Edition ausgeführt wird

-   Remote Bereitstellung der Verwaltungsserver-Datenbank oder der Berichtsdatenbank Das Installationsprogramm muss direkt auf dem Computer ausgeführt werden, auf dem Microsoft SQL ausgeführt wird, damit die Datenbankinstallation erfolgreich durchgeführt werden kann.

-   Bereitstellung auf einem Domänencontroller.

-   Kurze Pfade werden nicht unterstützt. Wenn Sie einen kurzen Pfad verwenden möchten, müssen Sie einen neuen Datenträger erstellen.

### Betriebssystemanforderungen für Management Server

In der folgenden Tabelle sind die Betriebssysteme aufgeführt, die für die Installation des App-V 5,0-Verwaltungsservers unterstützt werden.

**Hinweis:**  
Microsoft bietet Unterstützung für das aktuelle Service Pack und in einigen Fällen das unmittelbar vorhergehende Service Pack. Informationen zu den Support Zeitachsen für Ihr Produkt finden Sie unter [unterstützte Service Packs für Lebenszyklen](https://go.microsoft.com/fwlink/p/?LinkId=31975). Weitere Informationen zur Microsoft Support Lifecycle-Richtlinie finden Sie in den [FAQ zu Microsoft Support Lifecycle Support Policy](https://go.microsoft.com/fwlink/p/?LinkId=31976).



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
<td align="left"><p>Microsoft Windows Server 2008 (Standard, Enterprise, Datacenter oder Web Server)</p></td>
<td align="left"><p>R2</p></td>
<td align="left"><p>SP1 und höher</p></td>
<td align="left"><p>64Bit</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft Windows Server 2012 (Standard, Datacenter)</p></td>
<td align="left"><p></p></td>
<td align="left"></td>
<td align="left"><p>64Bit</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Microsoft Windows Server 2012 (Standard, Datacenter)</p></td>
<td align="left"><p>R2</p></td>
<td align="left"></td>
<td align="left"><p>64Bit</p></td>
</tr>
</tbody>
</table>



**Wichtig**  
Die Bereitstellung der Verwaltungsserverrolle auf einem Computer mit aktivierter Remote Desktop Freigabe (RDS) wird nicht unterstützt.



### <a href="" id="management-server-hardware-requirements-"></a>Hardwareanforderungen für den Verwaltungs Server

-   Prozessor – 1,4 GHz oder schneller, 64-Bit (x64)-Prozessor

-   RAM – 1 GB RAM (64-Bit)

-   Speicherplatz – 200 MB verfügbarer Festplattenspeicherplatz, nicht einschließlich des Inhaltsverzeichnisses.

### Betriebssystemanforderungen für Veröffentlichungs Server

In der folgenden Tabelle sind die Betriebssysteme aufgeführt, die für die Installation des App-V 5,0-Publishing Servers unterstützt werden.

**Hinweis:**  
Microsoft bietet Unterstützung für das aktuelle Service Pack und in einigen Fällen das unmittelbar vorhergehende Service Pack. Informationen zu den Support Zeitachsen für Ihr Produkt finden Sie unter [unterstützte Service Packs für Lebenszyklen](https://go.microsoft.com/fwlink/p/?LinkId=31975). Weitere Informationen zur Microsoft Support Lifecycle-Richtlinie finden Sie in den [FAQ zu Microsoft Support Lifecycle Support Policy](https://go.microsoft.com/fwlink/p/?LinkId=31976).



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
<td align="left"><p>Microsoft Windows Server 2008 (Standard, Enterprise, Datacenter oder Web Server)</p></td>
<td align="left"><p>R2</p></td>
<td align="left"><p></p></td>
<td align="left"><p>64Bit</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft Windows Server 2012 (Standard, Datacenter)</p></td>
<td align="left"><p></p></td>
<td align="left"></td>
<td align="left"><p>64Bit</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Microsoft Windows Server 2012 (Standard, Datacenter)</p></td>
<td align="left"><p>R2</p></td>
<td align="left"></td>
<td align="left"><p>64Bit</p></td>
</tr>
</tbody>
</table>



### <a href="" id="publishing-server-hardware-requirements-"></a>Hardwareanforderungen für Veröffentlichungs Server

-   Prozessor – 1,4 GHz oder schneller. 64-Bit (x64)-Prozessor

-   RAM – 2 GB RAM (64-Bit)

-   Speicherplatz – 200 MB verfügbarer Speicherplatz auf der Festplatte. nicht einschließlich Inhaltsverzeichnis

### Anforderungen des Reporting Server-Betriebssystems

In der folgenden Tabelle sind die Betriebssysteme aufgeführt, die für die App-V 5,0 Reporting Server-Installation unterstützt werden.

**Hinweis:**  
Microsoft bietet Unterstützung für das aktuelle Service Pack und in einigen Fällen das unmittelbar vorhergehende Service Pack. Informationen zu den Support Zeitachsen für Ihr Produkt finden Sie unter [unterstützte Service Packs für Lebenszyklen](https://go.microsoft.com/fwlink/p/?LinkId=31975). Weitere Informationen zur Microsoft Support Lifecycle-Richtlinie finden Sie in den [FAQ zu Microsoft Support Lifecycle Support Policy](https://go.microsoft.com/fwlink/p/?LinkId=31976).



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
<td align="left"><p>Microsoft Windows Server 2008 (Standard, Enterprise, Datacenter oder Web Server)</p></td>
<td align="left"><p>R2</p></td>
<td align="left"><p></p></td>
<td align="left"><p>64Bit</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft Windows Server 2012 (Standard, Datacenter)</p></td>
<td align="left"><p></p></td>
<td align="left"></td>
<td align="left"><p>64Bit</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Microsoft Windows Server 2012 (Standard, Datacenter)</p></td>
<td align="left"><p>R2</p></td>
<td align="left"></td>
<td align="left"><p>64Bit</p></td>
</tr>
</tbody>
</table>



### <a href="" id="reporting-server-hardware-requirements-"></a>Hardwareanforderungen für den Berichts Server

-   Prozessor – 1,4 GHz oder schneller. 64-Bit (x64)-Prozessor

-   RAM – 2 GB RAM (64-Bit)

-   Speicherplatz – 200 MB verfügbarer Festplattenspeicherplatz

### <a href="" id="sql-server-database-requirements-"></a>SQL Server-Datenbankanforderungen

In der folgenden Tabelle sind die SQL Server-Versionen aufgeführt, die für die App-V 5,0-Datenbank und die Server Installation unterstützt werden.

<table>
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">App-V 5,0-Servertyp</th>
<th align="left">SQL Server-Version</th>
<th align="left">Edition</th>
<th align="left">Service Pack</th>
<th align="left">System Architektur</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Verwaltung/Berichterstattung</p></td>
<td align="left"><p>Microsoft SQL Server 2008</p>
<p>(Standard, Enterprise, Datacenter oder Developer Edition mit folgendem Feature: <strong> Datenbankmodul </strong> -Dienste.)</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>32 Bit oder 64 Bit</p></td>
</tr>
<tr class="even">
<td align="left"><p>Verwaltung/Berichterstattung</p></td>
<td align="left"><p>Microsoft SQL Server 2008 </p>
<p>(Standard, Enterprise, Datacenter oder Developer Edition mit folgendem Feature: <strong> Datenbankmodul </strong> -Dienste.)</p></td>
<td align="left"><p>R2</p></td>
<td align="left"><p>SP2</p></td>
<td align="left"><p>32 Bit oder 64 Bit</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Verwaltung/Berichterstattung</p></td>
<td align="left"><p>Microsoft SQL Server 2012</p>
<p>(Standard, Enterprise, Datacenter oder Developer Edition mit folgendem Feature: <strong> Datenbankmodul </strong> -Dienste.)</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>32 Bit oder 64 Bit</p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-client-supp-cfgs"></a> App-V 5,0-Clientsystemanforderungen


In der folgenden Tabelle sind die Betriebssysteme aufgeführt, die für die App-V 5,0-Clientinstallation unterstützt werden.

**Hinweis:**  
Microsoft bietet Unterstützung für das aktuelle Service Pack und in einigen Fällen das unmittelbar vorhergehende Service Pack. Informationen zu den Support Zeitachsen für Ihr Produkt finden Sie unter [unterstützte Service Packs für Lebenszyklen](https://go.microsoft.com/fwlink/p/?LinkId=31975). Weitere Informationen zur Microsoft Support Lifecycle-Richtlinie finden Sie in den [FAQ zu Microsoft Support Lifecycle Support Policy](https://go.microsoft.com/fwlink/p/?LinkId=31976).



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
<td align="left"><p>Microsoft Windows 7</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>32 Bit oder 64 Bit</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft Windows 8</p></td>
<td align="left"><p></p></td>
<td align="left"><p>32 Bit oder 64 Bit</p></td>
</tr>
<tr class="odd">
<td align="left"><div class="alert">
<strong>Wichtig</strong><br/><p>Windows 8,1 wird nur von App-V 5,0 SP2 unterstützt</p>
</div>
<div>

</div>
<p>Windows8.1</p></td>
<td align="left"><p></p></td>
<td align="left"><p>32 Bit oder 64 Bit</p></td>
</tr>
</tbody>
</table>



Die folgenden App-V-Client Installationsszenarien werden nicht unterstützt, es sei denn, es wird angegeben:

-   Computer, auf denen Windows Server ausgeführt wird

-   Computer, auf denen App-V 4,6 SP1 oder frühere Versionen ausgeführt werden

-   Der App-V 5,0-Client für Remote Desktop Dienste wird nur für RDS-fähige Server unterstützt.

### <a href="" id="client-hardware-requirements-"></a>Client Hardwareanforderungen

In der folgenden Liste wird die unterstützte Hardwarekonfiguration für die App-V 5,0-Clientinstallation angezeigt.

-   Prozessor – 1,4 GHz oder schneller 32-Bit (x86) oder 64-Bit (x64)-Prozessor

-   RAM – 1 GB (32-Bit) oder 2 GB (64-Bit)

-   Datenträger – 100 MB für die Installation, nicht einschließlich des von virtualisierten Anwendungen verwendeten Speicherplatzes.

## <a href="" id="---------app-v-5-0-remote-desktop-client-system-requirements"></a> App-V 5,0-Systemanforderungen für Remote Desktop Client


In der folgenden Tabelle sind die Betriebssysteme aufgeführt, die für die App-V 5,0-Remote Desktop Client-Installation unterstützt werden.

**Hinweis:**  
Microsoft bietet Unterstützung für das aktuelle Service Pack und in einigen Fällen das unmittelbar vorhergehende Service Pack. Informationen zu den Support Zeitachsen für Ihr Produkt finden Sie unter [unterstützte Service Packs für Lebenszyklen](https://go.microsoft.com/fwlink/p/?LinkId=31975). Weitere Informationen zur Microsoft Support Lifecycle-Richtlinie finden Sie in den [FAQ zu Microsoft Support Lifecycle Support Policy](https://go.microsoft.com/fwlink/p/?LinkId=31976).



Betriebssystem Edition-Service Pack Microsoft Windows Server 2008

R2

SP1

Microsoft Windows Server 2012

**Wichtig**  
Windows Server 2012 R2 wird nur von App-V 5,0 SP2 unterstützt



Microsoft Windows Server 2012 (Standard, Datacenter)

R2

64Bit



### <a href="" id="remote-desktop-client-hardware-requirements-"></a>Hardwareanforderungen für Remote Desktop Client

In der folgenden Liste wird die unterstützte Hardwarekonfiguration für die App-V 5,0-Clientinstallation angezeigt.

-   Prozessor – 1,4 GHz oder schneller 32-Bit (x86) oder 64-Bit (x64)-Prozessor

-   RAM – 1 GB (32-Bit) oder 2 GB (64-Bit)

-   Datenträger – 100 MB für die Installation, nicht einschließlich des von virtualisierten Anwendungen verwendeten Speicherplatzes.

## <a href="" id="---------app-v-5-0-sequencer-system-requirements"></a> Systemanforderungen für App-V 5,0-Sequenzer


In der folgenden Tabelle sind die Betriebssysteme aufgeführt, die für die Installation von App-V 5,0 Sequencer unterstützt werden.

**Hinweis:**  
Microsoft bietet Unterstützung für das aktuelle Service Pack und in einigen Fällen das unmittelbar vorhergehende Service Pack. Informationen zu den Support Zeitachsen für Ihr Produkt finden Sie unter [unterstützte Service Packs für Lebenszyklen](https://go.microsoft.com/fwlink/p/?LinkId=31975). Weitere Informationen zur Microsoft Support Lifecycle-Richtlinie finden Sie in den [FAQ zu Microsoft Support Lifecycle Support Policy](https://go.microsoft.com/fwlink/p/?LinkId=31976).



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
<td align="left"><p>Microsoft Windows 7</p></td>
<td align="left"></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>32Bit und 64Bit</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft Windows 8</p></td>
<td align="left"></td>
<td align="left"><p></p></td>
<td align="left"><p>32Bit und 64Bit</p></td>
</tr>
<tr class="odd">
<td align="left"><div class="alert">
<strong>Wichtig</strong><br/><p>Windows 8,1 wird nur von App-V 5,0 SP2 unterstützt</p>
</div>
<div>

</div>
<p>Windows8.1</p></td>
<td align="left"></td>
<td align="left"><p></p></td>
<td align="left"><p>32 Bit oder 64 Bit</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft Windows Server 2008</p></td>
<td align="left"><p>R2</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>32Bit und 64Bit</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Microsoft Windows Server 2012</p></td>
<td align="left"></td>
<td align="left"><p></p></td>
<td align="left"><p>32Bit und 64Bit</p></td>
</tr>
<tr class="even">
<td align="left"><div class="alert">
<strong>Wichtig</strong><br/><p>Windows Server 2012 R2 wird nur von App-V 5,0 SP2 unterstützt</p>
</div>
<div>

</div>
<p>Microsoft Windows Server 2012</p></td>
<td align="left"><p>R2</p></td>
<td align="left"></td>
<td align="left"><p>64Bit</p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-supp-ver-sccm"></a>Unterstützte Versionen von System Center Configuration Manager


Sie können den Microsoft System Center 2012-Konfigurations-Manager oder den System Center 2012 R2-Konfigurations-Manager verwenden, um virtuelle App-V-Anwendungen, Berichterstellung und andere Funktionen zu verwalten. In der folgenden Tabelle sind die unterstützten Versionen von Configuration Manager für jede anwendbare Version von App-V aufgeführt.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Unterstützte Configuration Manager-Version</th>
<th align="left">App-V-Version</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Microsoft System Center 2012-Konfigurations-Manager</p></td>
<td align="left"><ul>
<li><p>App-V 5,0</p></li>
<li><p>App-V 5,0 SP1</p></li>
<li><p>App-V 5,0 SP2</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>System Center 2012 R2 Configuration Manager</p></td>
<td align="left"><ul>
<li><p>App-V 5,0</p></li>
<li><p>App-V 5,0 SP1</p></li>
<li><p>App-V 5,0 SP2</p></li>
</ul></td>
</tr>
</tbody>
</table>



Weitere Informationen zur Integration von Configuration Manager in App-v finden Sie unter [Planen der APP-v-Integration in Configuration Manager](https://technet.microsoft.com/library/jj822982.aspx).






## Verwandte Themen


[Planen der Bereitstellung von App-V](planning-to-deploy-app-v.md)

[Voraussetzungen für App-V 5.0](app-v-50-prerequisites.md)









