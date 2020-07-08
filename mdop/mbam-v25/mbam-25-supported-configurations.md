---
title: Von MBAM 2.5 unterstützte Konfigurationen
description: Von MBAM 2.5 unterstützte Konfigurationen
author: dansimp
ms.assetid: ce689aff-9a55-4ae7-a968-23c7bda9b4d6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 10/24/2018
ms.openlocfilehash: 262cd8c259dc37b291cdaf02caf0e20b7515d38b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810228"
---
# Von MBAM 2.5 unterstützte Konfigurationen


Sie können die Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) 2,5 in einer eigenständigen Topologie oder in einer Configuration Manager-Integrations Topologie ausführen, die MBAM in den System Center Configuration Manager integriert. Wenn Sie die empfohlene Konfiguration für beide Topologien in einer Produktionsumgebung verwenden, unterstützt MBAM bis zu 500.000 MBAM-Clients. Informationen zu den empfohlenen Architekturen und Features, die auf den einzelnen Servern für die einzelnen Topologien konfiguriert sind, finden Sie unter [Architektur auf höherer Ebene für MBAM 2,5](high-level-architecture-for-mbam-25.md).

Weitere Konfigurationen, die speziell für die Configuration Manager-Integrations Topologie gelten, finden Sie unter [unterstützte Configuration Manager-Versionen von MBAM](#bkmk-cm-ramreqs).

**Hinweis:**  
Microsoft bietet Unterstützung für das aktuelle Service Pack und in einigen Fällen das unmittelbar vorhergehende Service Pack. Informationen zu den Support Zeitachsen für Ihr Produkt finden Sie unter [unterstützte Service Packs für Lebenszyklen](https://go.microsoft.com/fwlink/p/?LinkId=31975). Weitere Informationen zur Microsoft Support Lifecycle-Richtlinie finden Sie in den [FAQ zu Microsoft Support Lifecycle Support Policy](https://go.microsoft.com/fwlink/p/?LinkId=31976).



## MBAM unterstützte Sprachen


In den folgenden Tabellen werden die Sprachen aufgeführt, die für den MBAM-Client (einschließlich des Self-Service-Portals) und den MBAM-Server in MBAM 2,5 und MBAM 2,5 SP1 unterstützt werden.

**Unterstützte Sprachen in MBAM 2,5 SP1:**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Client Sprachen</th>
<th align="left">Server Sprachen</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Tschechische Republik (Tschechien) cs-cz</p>
<p>Dänisch (Dänemark) da-DK</p>
<p>Niederländisch (Niederlande) nl-nl</p>
<p>Englisch (USA) en-US</p>
<p>Finnisch (Finnland) fi-fi</p>
<p>Französisch (Frankreich) fr-FR</p>
<p>Deutsch (Deutschland) de-de</p>
<p>Griechisch (Griechenland) el-gr</p>
<p>Ungarisch (Ungarn) hu-hu</p>
<p>Italienisch (Italien) IT-IT</p>
<p>Japanisch (Japan) ja-JP</p>
<p>Koreanisch (Korea) ko-kr</p>
<p>Norwegisch, Nynorsk (Norwegen) NB-Nein</p>
<p>Polnisch (Polen) pl-pl</p>
<p>Portugiesisch (Brasilien) pt-br</p>
<p>Portugiesisch (Portugal) pt-pt</p>
<p>Russisch (Russland) ru-ru</p>
<p>Slowakisch (Slowakei) sk-SK</p>
<p>Spanisch (Spanien) es-es</p>
<p>SV-SE für Schwedisch (Schweden)</p>
<p>Türkisch (Türkei) tr-TR</p>
<p>Slowenisch (Slowenien) SL-SI</p>
<p>Vereinfachtes Chinesisch (VR China) zh-cn</p>
<p>Traditionelles Chinesisch (Taiwan) zh-tw</p></td>
<td align="left"><ul>
<li><p>Englisch (USA) en-US</p></li>
<li><p>Französisch (Frankreich) fr-FR</p></li>
<li><p>Deutsch (Deutschland) de-de</p></li>
<li><p>Italienisch (Italien) IT-IT</p></li>
<li><p>Japanisch (Japan) ja-JP</p></li>
<li><p>Koreanisch (Korea) ko-kr</p></li>
<li><p>Portugiesisch (Brasilien) pt-br</p></li>
<li><p>Russisch (Russland) ru-ru</p></li>
<li><p>Spanisch (Spanien) es-es</p></li>
<li><p>Vereinfachtes Chinesisch (VR China) zh-cn</p></li>
<li><p>Traditionelles Chinesisch (Taiwan) zh-tw</p></li>
</ul></td>
</tr>
</tbody>
</table>



**Unterstützte Sprachen in MBAM 2,5:**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Client Sprachen</th>
<th align="left">Server Sprachen</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><ul>
<li><p>Englisch (USA) en-US</p></li>
<li><p>Französisch (Frankreich) fr-FR</p></li>
<li><p>Deutsch (Deutschland) de-de</p></li>
<li><p>Italienisch (Italien) IT-IT</p></li>
<li><p>Japanisch (Japan) ja-JP</p></li>
<li><p>Koreanisch (Korea) ko-kr</p></li>
<li><p>Portugiesisch (Brasilien) pt-br</p></li>
<li><p>Russisch (Russland) ru-ru</p></li>
<li><p>Spanisch (Spanien) es-es</p></li>
<li><p>Vereinfachtes Chinesisch (VR China) zh-cn</p></li>
<li><p>Traditionelles Chinesisch (Taiwan) zh-tw</p></li>
</ul></td>
<td align="left"><ul>
<li><p>Englisch (USA) en-US</p></li>
<li><p>Französisch (Frankreich) fr-FR</p></li>
<li><p>Deutsch (Deutschland) de-de</p></li>
<li><p>Italienisch (Italien) IT-IT</p></li>
<li><p>Japanisch (Japan) ja-JP</p></li>
<li><p>Koreanisch (Korea) ko-kr</p></li>
<li><p>Portugiesisch (Brasilien) pt-br</p></li>
<li><p>Russisch (Russland) ru-ru</p></li>
<li><p>Spanisch (Spanien) es-es</p></li>
<li><p>Vereinfachtes Chinesisch (VR China) zh-cn</p></li>
<li><p>Traditionelles Chinesisch (Taiwan) zh-tw</p></li>
</ul></td>
</tr>
</tbody>
</table>



## <a href="" id="---------mbam-server-system-requirements"></a> Systemanforderungen für MBAM-Server


### MBAM Server-Betriebssystemanforderungen

Wir empfehlen dringend, dass Sie den MBAM-Client und den MBAM-Server auf der gleichen Betriebssystem Zeile ausführen. Beispiel: Windows 10 mit Windows Server 2016, Windows 8,1 mit Windows Server 2012 R2 usw.

In der folgenden Tabelle sind die Betriebssysteme aufgeführt, die für die Installation des MBAM-Servers unterstützt werden.

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
<td align="left"><p>Windows Server 2016</p></td>
<td align="left"><p>Standard oder Rechenzentrum</p></td>
<td align="left"></td>
<td align="left"><p>64Bit</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2012 R2</p></td>
<td align="left"><p>Standard oder Rechenzentrum</p></td>
<td align="left"><p></p></td>
<td align="left"><p>64Bit</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server 2012</p></td>
<td align="left"><p>Standard oder Rechenzentrum</p></td>
<td align="left"></td>
<td align="left"><p>64Bit</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server 2008 R2</p></td>
<td align="left"><p>Standard, Enterprise oder Datacenter</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>64Bit</p></td>
</tr>
</tbody>
</table>



Die Unternehmensdomäne muss mindestens einen Windows Server 2008-Domänencontroller (oder höher) enthalten.

### <a href="" id="bkmk-stand-alone-ramreqs"></a>MBAM-Server Prozessor, RAM und Speicherplatzanforderungen – eigenständige Topologie

Diese Anforderungen gelten für die eigenständige MBAM-Topologie. Die Anforderungen für die Configuration Manager-Integrations Topologie finden Sie unter [MBAM-Server Prozessor, RAM und Speicherplatzanforderungen – Configuration Manager-Integrations Topologie](#bkmk-cm-ramreqs).

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Hardware Element</th>
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



### <a href="" id="bkmk-cm-ramreqs"></a>MBAM-Server Prozessor, RAM und Speicherplatzanforderungen – Configuration Manager-Integrations Topologie

In der folgenden Tabelle sind die Server Prozessor-, RAM-und Speicherplatzanforderungen für MBAM-Server aufgelistet, wenn Sie die Configuration Manager-Integrations Topologie verwenden. Die Anforderungen für die eigenständige Topologie finden Sie unter [MBAM-Server Prozessor, RAM und Speicherplatzanforderungen – eigenständige Topologie](#bkmk-stand-alone-ramreqs).

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Hardware Element</th>
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
<td align="left"><p>4 GB</p></td>
<td align="left"><p>8 GB</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Freier Speicherplatz</p></td>
<td align="left"><p>1 GB</p></td>
<td align="left"><p>2 GB</p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-cmversions"></a>Von MBAM unterstützte Versionen von Configuration Manager

MBAM unterstützt die folgenden Versionen von Configuration Manager.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Unterstützte Version</th>
<th align="left">Service Pack</th>
<th align="left">System Architektur</th>
</tr>
</thead>
<tbody>
<tr class="even">
<td align="left"><p>Microsoft System Center Configuration Manager (aktueller Zweig), Versionen bis zu 1902</p></td>
<td align="left"><p></p></td>
<td align="left"><p>64Bit</p></td>
</tr>

<tr class="odd">
<td align="left"><p>Microsoft System Center Configuration Manager 1806</p></td>
<td align="left"><p></p></td>
<td align="left"><p>64Bit</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft System Center Configuration Manager (LTSB-Version 1606)</p></td>
<td align="left"><p></p></td>
<td align="left"><p>64Bit</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Microsoft System Center 2012-Konfigurations-Manager</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>64Bit</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft System Center Configuration Manager 2007 R2 oder höher</p></td>
<td align="left"><p></p></td>
<td align="left"><p>64Bit</p>

&gt;<strong>Hinweis </strong> Obwohl Configuration Manager 2007 R2 32-Bit ist, müssen Sie es und SQL Server auf einem 64-Bit-Betriebssystem installieren, um der 64-Bit-MBAM-Software entsprechen zu können.
</td>
</tr>
</tbody>
</table>



Eine Liste der unterstützten Konfigurationen für den Configuration Manager-Server finden Sie in der entsprechenden TechNet-Dokumentation für die Version von Configuration Manager, die Sie verwenden. MBAM hat keine zusätzlichen Systemanforderungen für den Configuration Manager-Server.

### <a href="" id="sql-server-database-requirements-"></a>SQL Server-Datenbankanforderungen

In der folgenden Tabelle sind die Microsoft SQL Server-Versionen aufgeführt, die für die MBAM-Server Features unterstützt werden, einschließlich der Datenbank für die Wiederherstellungsdatenbank, der Kompatibilitäts-und Überwachungsdatenbank sowie des Berichtsfeatures. Die erforderlichen Versionen gelten für die eigenständige oder die Configuration Manager-Integrations Topologie.

Sie müssen SQL Server mit dem **SQL \ _Latin1 \ _General \ _CP1 \ _ci \ _AS** Sortierreihenfolge installieren.

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
<td align="left"><p>Microsoft SQL Server 2017</p></td>
<td align="left"><p>Standard, Enterprise oder Datacenter</p></td>
<td align="left"><p></p></td>
<td align="left"><p>64Bit</p></td><br/><tr class="even">
<td align="left"><p>Microsoft SQL Server 2016</p></td>
<td align="left"><p>Standard, Enterprise oder Datacenter</p></td>
<td align="left"><p>SP1</p></td>
<a href="https://www.microsoft.com/download/details.aspx?id=54967" data-raw-source="https://www.microsoft.com/download/details.aspx?id=54967">https://www.microsoft.com/download/details.aspx?id=54967</a><td align="left"><p>64Bit</p></td>
<tr class="odd">
<td align="left"><p>Microsoft SQL Server 2014</p></td>
<td align="left"><p>Standard, Enterprise oder Datacenter</p></td>
<td align="left"><p>SP1, SP2</p></td>
<td align="left"><p>64Bit</p></td>
<tr class="odd">
<td align="left"><p>Microsoft SQL Server 2012</p></td>
<td align="left"><p>Standard, Enterprise oder Datacenter</p></td>
<td align="left"><p>SP3</p></td>
<td align="left"><p>64Bit</p></td>
<tr class="even">
<td align="left"><p>Microsoft SQL Server 2008 R2</p></td>
<td align="left"><p>Standard oder Enterprise</p></td>
<td align="left"><p>SP3</p></td>
<td align="left"><p>64Bit</p></td>
</tr>
</tbody>
</table>

**Hinweis:**  
Um SQL 2016 zu unterstützen, müssen Sie die Service Version für März 2017 für MDOP installieren https://www.microsoft.com/download/details.aspx?id=54967 und SQL 2017 unterstützen, wenn Sie die Version vom Juli 2018 für MDOP installieren müssen https://www.microsoft.com/download/details.aspx?id=57157 . Im allgemeinen bleiben Sie stets auf dem laufenden, indem Sie immer das neueste Wartungsupdate verwenden, da es auch alle Bugfixes und neuen Features enthält.


### <a href="" id="bkmk-sql-stand-alone-ramreqs"></a>SQL Server-Prozessor, RAM und Speicherplatzanforderungen – eigenständige Topologie

In der folgenden Tabelle sind die empfohlenen Server Prozessor-, RAM-und Speicherplatzanforderungen für den SQL Server-Computer aufgeführt, wenn Sie die eigenständige Topologie verwenden. Verwenden Sie diese Anforderungen als Leitfaden. Ihre spezifischen Anforderungen unterscheiden sich je nach der Anzahl der Clientcomputer, die Sie in Ihrem Unternehmen unterstützen. Informationen zum Anzeigen der Anforderungen für die Configuration Manager-Integrations Topologie finden Sie unter [SQL Server-Prozessor, RAM und Speicherplatzanforderungen – Configuration Manager-Integrations Topologie](#bkmk-cm-sql-ramreqs).

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Hardware Element</th>
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



### <a href="" id="bkmk-cm-sql-ramreqs"></a>SQL Server-Prozessor, RAM und Speicherplatzanforderungen – Configuration Manager-Integrations Topologie

In der folgenden Tabelle sind die Anforderungen für den Server Prozessor, den Arbeitsspeicher und den Speicherplatz für den Microsoft SQL Server-Computer aufgeführt, wenn Sie die Configuration Manager-Integrations Topologie verwenden, siehe [SQL Server-Prozessor, RAM und Speicherplatzanforderungen – eigenständige Topologie](#bkmk-sql-stand-alone-ramreqs).

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Hardware Element</th>
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
<td align="left"><p>4 GB</p></td>
<td align="left"><p>8 GB</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Freier Speicherplatz</p></td>
<td align="left"><p>5 GB</p></td>
<td align="left"><p>5 GB</p></td>
</tr>
</tbody>
</table>



## <a href="" id="---------mbam-client-system-requirements"></a> MBAM-Client Systemanforderungen


### Client-Betriebssystemanforderungen

Wir empfehlen dringend, dass Sie den MBAM-Client und den MBAM-Server auf der gleichen Betriebssystem Zeile ausführen. Beispiel: Windows 10 mit Windows Server 2016, Windows 8,1 mit Windows Server 2012 R2 usw.

In der folgenden Tabelle sind die Betriebssysteme aufgeführt, die für die MBAM-Client Installation unterstützt werden. Die gleichen Anforderungen gelten für die eigenständige und die Configuration Manager-Integrations Topologie.

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
<tr class="even">
    <td align="left"><p>Windows 10-viel</p></td>
    <td align="left"><p>Unternehmen</p></td>
    <td align="left"><p></p></td>
    <td align="left"><p>32 Bit oder 64 Bit</p></td>
</tr><br/><tr class="odd">
<td align="left"><p>Windows 10</p></td>
<td align="left"><p>Unternehmen</p></td>
<td align="left"><p></p></td>
<td align="left"><p>32 Bit oder 64 Bit</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows8.1</p></td>
<td align="left"><p>Unternehmen</p></td>
<td align="left"><p></p></td>
<td align="left"><p>32 Bit oder 64 Bit</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows7</p></td>
<td align="left"><p>Enterprise oder Ultimate</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>32 Bit oder 64 Bit</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows To Go</p></td>
<td align="left"><p>Windows 8,1 und Windows 10 Enterprise</p></td>
<td align="left"><p></p></td>
<td align="left"><p>32 Bit oder 64 Bit</p></td>
</tr>
</tbody>
</table>



### <a href="" id="client-ram-requirements-"></a>Client-RAM-Anforderungen

Für die MBAM-Client Installation gibt es keine spezifischen RAM-Anforderungen.

## <a href="" id="---------mbam-group-policy-system-requirements"></a> Systemanforderungen für MBAM-Gruppenrichtlinien


In der folgenden Tabelle sind die Betriebssysteme aufgeführt, die für die Installation von MBAM-Gruppenrichtlinienvorlagen unterstützt werden.

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
 <tr class="even">
      <td align="left"><p>Windows 10-viel</p></td>
      <td align="left"><p>Unternehmen</p></td>
      <td align="left"><p></p></td>
      <td align="left"><p>32 Bit oder 64 Bit</p></td>
 </tr>
<tr class="odd">
<td align="left"><p>Windows 10</p></td>
<td align="left"><p>Unternehmen</p></td>
<td align="left"><p></p></td>
<td align="left"><p>32 Bit oder 64 Bit</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows8.1</p></td>
<td align="left"><p>Unternehmen</p></td>
<td align="left"><p></p></td>
<td align="left"><p>32 Bit oder 64 Bit</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows7</p></td>
<td align="left"><p>Enterprise oder Ultimate</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>32 Bit oder 64 Bit</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2012 R2</p></td>
<td align="left"><p>Standard oder Rechenzentrum</p></td>
<td align="left"><p></p></td>
<td align="left"><p>64Bit</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server 2012</p></td>
<td align="left"><p>Standard oder Rechenzentrum</p></td>
<td align="left"><p></p></td>
<td align="left"><p>64Bit</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2008 R2</p></td>
<td align="left"><p>Standard, Enterprise oder Datacenter</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>64Bit</p></td>
</tr>
</tbody>
</table>

## MBAM in Azure IaaS

Der MBAM-Server kann in Azure Infrastructure as a Service (IaaS) auf einer der oben aufgeführten unterstützten Betriebssystemversionen bereitgestellt werden, die eine Verbindung mit einem lokal gehosteten Active Directory oder einem Active Directory herstellt, das auch in Azure IaaS gehostet wird.  Die Dokumentation zum Einrichten und Konfigurieren von Active Directory auf Azure IaaS finden Sie [hier](https://msdn.microsoft.com/library/azure/jj156090.aspx).

Der MBAM-Client wird auf virtuellen Computern nicht unterstützt und auch auf Azure IaaS nicht unterstützt.


## Dienstversionen 

- [Hotfix für April 2016](https://support.microsoft.com/help/3144445/april-2016-hotfix-rollup-for-microsoft-desktop-optimization-pack)
- [September 2016](https://support.microsoft.com/ms-my/help/3168628/september-2016-servicing-release-for-microsoft-desktop-optimization-pa)
- [Dezember 2016](https://support.microsoft.com/help/3198158/december-2016-servicing-release-for-microsoft-desktop-optimization-pac)
- [März 2017](https://support.microsoft.com/en-ie/help/4014009/march-2017-servicing-release-for-microsoft-desktop-optimization-pack) 
- [Juni 2017](https://support.microsoft.com/af-za/help/4018510/june-2017-servicing-release-for-microsoft-desktop-optimization-pack)
- [September2017](https://support.microsoft.com/en-ie/help/4041137/september-2017-servicing-release-for-microsoft-desktop-optimization)
- [März 2018](https://support.microsoft.com/help/4074878/march-2018-servicing-release-for-microsoft-desktop-optimization-pack)
- [Juli 2018](https://support.microsoft.com/help/4340040/july-2018-servicing-release-for-microsoft-desktop-optimization-pack)
- [Mai 2019](https://support.microsoft.com/help/4505175/may-2019-servicing-release-for-microsoft-desktop-optimization-pack)

## Verwandte Themen


[Planen der Bereitstellung von MBAM 2.5](planning-to-deploy-mbam-25.md)

[Vorbereiten der Umgebung für MBAM 2.5](preparing-your-environment-for-mbam-25.md)




## Sie haben einen Vorschlag für MBAM?
- [Hier](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)können Sie Vorschläge hinzufügen oder abstimmen. 
- Bei MBAM-Problemen verwenden Sie das [MBAM TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).




