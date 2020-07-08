---
title: Von MBAM 1.0 unterstützte Konfigurationen
description: Von MBAM 1.0 unterstützte Konfigurationen
author: dansimp
ms.assetid: 1f5ac58e-6a3f-47df-8a9b-4b57631ab9ee
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 2c72320379d1c9328a6b40537d37998402b1b38b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811455"
---
# Von MBAM 1.0 unterstützte Konfigurationen


In diesem Thema werden die erforderlichen Anforderungen zum Installieren und Ausführen von Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) in Ihrer Umgebung angegeben.

## <a href="" id="---------mbam-server-system-requirements"></a> Systemanforderungen für MBAM-Server


### Server Betriebssystem-Anforderungen

In der folgenden Tabelle sind die Betriebssysteme aufgeführt, die für die Installation von Microsoft BitLocker-Administration und-Monitoring Server unterstützt werden.

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
<td align="left"><p>Windows Server 2008</p></td>
<td align="left"><p>Standard, Enterprise, Datacenter oder Web Server</p></td>
<td align="left"><p>Nur SP2</p></td>
<td align="left"><p>32 Bit oder 64 Bit</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2008 R2</p></td>
<td align="left"><p>Standard, Enterprise, Datacenter oder Web Server</p></td>
<td align="left"></td>
<td align="left"><p>64Bit</p></td>
</tr>
</tbody>
</table>



**Warnung**  
Es gibt keine Unterstützung für die Installation von MBAM-Diensten,-Berichten oder-Datenbanken auf einem Domänencontrollercomputer.



### <a href="" id="server-random-access-memory--ram--requirements-"></a>Server-RAM-Anforderungen (Random Access Memory)

Für die Installation von MBAM-Servern gibt es keine spezifischen RAM-Anforderungen.

### <a href="" id="sql-server-database-requirements-"></a>SQL Server-Datenbankanforderungen

In der folgenden Tabelle sind die SQL Server-Versionen aufgeführt, die für die Installation von MBAM Server Features unterstützt werden.

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
<th align="left">MBAM-Server Feature</th>
<th align="left">SQL Server-Version</th>
<th align="left">Edition</th>
<th align="left">Service Pack</th>
<th align="left">System Architektur</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Konformitäts-und Überwachungsberichte</p></td>
<td align="left"><p>Microsoft SQL Server 2008 </p></td>
<td align="left"><p>R2, Standard, Enterprise, Datacenter oder Developer Edition</p></td>
<td align="left"><p>SP2</p></td>
<td align="left"><p>32 Bit oder 64 Bit</p></td>
</tr>
<tr class="even">
<td align="left"><p>Wiederherstellungs-und Hardware Datenbank</p></td>
<td align="left"><p>Microsoft SQL Server 2008 </p></td>
<td align="left"><p>R2, Enterprise, Datacenter oder Developer Edition</p>
<div class="alert">
<strong>Wichtig</strong><br/><p>SQL Server-Standard Editionen werden für die MBAM-Wiederherstellung und die Installation von Hardware-Datenbankservern nicht unterstützt.</p>
</div>
<div>

</div></td>
<td align="left"><p>SP2</p></td>
<td align="left"><p>32 Bit oder 64 Bit</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Konformitäts-und Überwachungsdatenbank</p></td>
<td align="left"><p>Microsoft SQL Server 2008 </p></td>
<td align="left"><p>R2, Standard, Enterprise, Datacenter oder Developer Edition</p></td>
<td align="left"><p>SP2</p></td>
<td align="left"><p>32 Bit oder 64 Bit</p></td>
</tr>
</tbody>
</table>



## <a href="" id="---------mbam-client-system-requirements"></a> MBAM-Client Systemanforderungen


### Client-Betriebssystemanforderungen

In der folgenden Tabelle sind die Betriebssysteme aufgeführt, die für die MBAM-Client Installation unterstützt werden.

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
<td align="left"><p>Windows7</p></td>
<td align="left"><p>Enterprise Edition</p></td>
<td align="left"><p>Keine, SP1</p></td>
<td align="left"><p>32 Bit oder 64 Bit</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows7</p></td>
<td align="left"><p>Ultimate Edition</p></td>
<td align="left"><p>Keine, SP1</p></td>
<td align="left"><p>32 Bit oder 64 Bit</p></td>
</tr>
</tbody>
</table>



### <a href="" id="client-ram-requirements-"></a>Client-RAM-Anforderungen

Für die MBAM-Client Installation gibt es keine spezifischen RAM-Anforderungen.

## Verwandte Themen


[Planen der Bereitstellung von MBAM 1.0](planning-to-deploy-mbam-10.md)

[Bereitstellungsvoraussetzungen für MBAM 1.0](mbam-10-deployment-prerequisites.md)









