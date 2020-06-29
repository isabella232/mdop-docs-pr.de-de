---
title: Von MBAM 2.0 unterstützte Konfigurationen
description: Von MBAM 2.0 unterstützte Konfigurationen
author: dansimp
ms.assetid: dca63391-39fe-4273-a570-76d0a2f8a0fd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 8f314adcf818c1bdb17b0b239a7469f97fa849e4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810237"
---
# Von MBAM 2.0 unterstützte Konfigurationen


In diesem Thema werden die Anforderungen zum Installieren und Ausführen von Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) 2,0 in Ihrer Umgebung mithilfe der eigenständigen Topologie angegeben. Informationen zu unterstützten Konfigurationen, die für spätere Versionen gelten, finden Sie in der Dokumentation zur jeweiligen Version.

Wenn Sie beabsichtigen, MBAM 2,0 mithilfe der Configuration Manager-Topologie zu installieren, und eine Liste der Systemanforderungen überprüfen möchten, lesen Sie [Planen der Bereitstellung von MBAM mit Configuration Manager](planning-to-deploy-mbam-with-configuration-manager-2.md).

Die empfohlene Konfiguration für die Ausführung von MBAM in einer Produktionsumgebung besteht je nach Ihren Skalierbarkeitsanforderungen aus zwei Servern. Diese Konfiguration unterstützt bis zu 200.000 MBAM-Clients. Ein Bild und Beschreibungen der eigenständigen MBAM-Serverinfrastruktur finden Sie unter [Architektur auf höherer Ebene für MBAM 2,0](high-level-architecture-for-mbam-20-mbam-2.md).

**Hinweis**  Microsoft bietet Unterstützung für das aktuelle Service Pack und in einigen Fällen das unmittelbar vorhergehende Service Pack. Informationen zu den Support Zeitachsen für Ihr Produkt finden Sie unter [unterstützte Service Packs für Lebenszyklen](https://go.microsoft.com/fwlink/p/?LinkId=31975). Weitere Informationen zur Microsoft Support Lifecycle-Richtlinie finden Sie in den [FAQ zu Microsoft Support Lifecycle Support Policy](https://go.microsoft.com/fwlink/p/?LinkId=31976).

 

## <a href="" id="---------mbam-server-system-requirements"></a> System Anforderungen für MBAM-Server


### Server Betriebssystem-Anforderungen

In der folgenden Tabelle sind die Betriebssysteme aufgeführt, die für die Installation von Microsoft BitLocker-Administration und-Monitoring Server unterstützt werden.

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
<td align="left"><p>WindowsServer2008 R2</p></td>
<td align="left"><p>Standard-, Enterprise-oder Datacenter-Edition</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>64Bit</p></td>
</tr>
<tr class="even">
<td align="left"><p>WindowsServer2012</p></td>
<td align="left"><p>Standard-oder Datacenter Edition</p></td>
<td align="left"></td>
<td align="left"><p>64Bit</p></td>
</tr>
</tbody>
</table>

 

**Hinweis**  Es gibt keine Unterstützung für die Installation von MBAM-Diensten,-Berichten oder-Datenbanken auf einem Domänencontrollercomputer.

 

### <a href="" id="server-processor--ram--and-disk-space-requirements-"></a>Server Prozessor, Arbeitsspeicher und Speicherplatzanforderungen

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Hardware Komponente</th>
<th align="left">Mindestanforderungen</th>
<th align="left">Empfohlene Anforderung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Prozessor</p></td>
<td align="left"><p>2,33 GHz</p></td>
<td align="left"><p>2,33 GHz oder höher</p></td>
</tr>
<tr class="even">
<td align="left"><p>RAM</p></td>
<td align="left"><p>8 GB</p></td>
<td align="left"><p>12 GB</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Freier Speicherplatz</p></td>
<td align="left"><p>1 GB</p></td>
<td align="left"><p>2 GB</p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="sql-server-database-requirements-"></a>SQLServer-Datenbankanforderungen

In der folgenden Tabelle sind die SQLServer-Versionen aufgeführt, die für die Installation von Verwaltungs-und Überwachungs Server Features unterstützt werden, einschließlich der Datenbank für die Wiederherstellung, der Konformitäts-und Überwachungsdatenbank sowie der Konformitäts-und Überwachungsberichte. Die Datenbanken erfordern zusätzlich die Installation der SQL Server-Verwaltungs Tools.

**Hinweis**  MBAM unterstützt keine systemeigenen SQL-Clustering-, Spiegelungs-oder Verfügbarkeitsgruppen. Wenn Sie die Datenbanken installieren möchten, müssen Sie die MBAM-Server Installation auf einem eigenständigen SQL Server ausführen.

 

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">SQL Server-Version</th>
<th align="left">Edition</th>
<th align="left">Service Pack</th>
<th align="left">System Architektur</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>MicrosoftSQLServer2008 R2</p></td>
<td align="left"><p>Standard-, Enterprise-oder Datacenter-Edition</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>64Bit</p></td>
</tr>
<tr class="even">
<td align="left"><p>MicrosoftSQLServer2012</p></td>
<td align="left"><p>Standard-, Enterprise-oder Datacenter-Edition</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>64Bit</p></td>
</tr>
</tbody>
</table>

 

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Hardware Komponente</th>
<th align="left">Mindestanforderungen</th>
<th align="left">Empfohlene Anforderung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Prozessor</p></td>
<td align="left"><p>2,33 GHz</p></td>
<td align="left"><p>2,33 GHz oder höher</p></td>
</tr>
<tr class="even">
<td align="left"><p>RAM</p></td>
<td align="left"><p>8 GB</p></td>
<td align="left"><p>12 GB</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Freier Speicherplatz</p></td>
<td align="left"><p>5 GB</p></td>
<td align="left"><p>5 GB oder höher</p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="---------mbam-client-system-requirements"></a> MBAM-Client System Anforderungen


### Client-Betriebs System Anforderungen

In der folgenden Tabelle sind die Betriebssysteme aufgeführt, die für die Microsoft BitLocker-Verwaltung und-Überwachung der Client Installation unterstützt werden.

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
<td align="left"><p>Enterprise-oder Ultimate-Edition</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>32 Bit oder 64 Bit</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows 8</p></td>
<td align="left"><p>Enterprise Edition</p></td>
<td align="left"><p></p></td>
<td align="left"><p>32 Bit oder 64 Bit</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows To Go</p></td>
<td align="left"><p>Windows 8 Enterprise Edition</p></td>
<td align="left"><p></p></td>
<td align="left"><p>32 Bit oder 64 Bit</p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="client-ram-requirements-"></a>Client-RAM-Anforderungen

Es gibt keine RAM-Anforderungen, die für die Microsoft BitLocker-Administrator-und-Überwachungs Client Installation spezifisch sind.

## <a href="" id="---------mbam-group-policy-system-requirements"></a> System Anforderungen für MBAM-Gruppenrichtlinien


In der folgenden Tabelle sind die Betriebssysteme aufgeführt, die für die Microsoft BitLocker-Verwaltung und-Überwachung der Gruppenrichtlinien-Vorlageninstallation unterstützt werden.

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
<td align="left"><p>Enterprise-oder Ultimate-Edition</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>32 Bit oder 64 Bit</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows 8</p></td>
<td align="left"><p>Enterprise Edition</p></td>
<td align="left"><p></p></td>
<td align="left"><p>32 Bit oder 64 Bit</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server 2008 R2</p></td>
<td align="left"><p>Standard-, Enterprise-oder Datacenter-Edition</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>64Bit</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2012</p></td>
<td align="left"><p>Standard-oder Datacenter Edition</p></td>
<td align="left"><p></p></td>
<td align="left"><p>64Bit</p></td>
</tr>
</tbody>
</table>

 

## Verwandte Themen


[Planen der Bereitstellung von MBAM 2.0](planning-to-deploy-mbam-20-mbam-2.md)

[Bereitstellungsvoraussetzungen für MBAM 2.0](mbam-20-deployment-prerequisites-mbam-2.md)

 

 





