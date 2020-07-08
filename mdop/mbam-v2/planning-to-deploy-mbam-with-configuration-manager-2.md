---
title: Planen der Bereitstellung von MBAM mit dem Konfigurations-Manager
description: Planen der Bereitstellung von MBAM mit dem Konfigurations-Manager
author: dansimp
ms.assetid: fb768306-48c2-40b4-ac4e-c279db987391
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: e8588ce03c86a8a5138d591327e5f95503dce5ad
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811269"
---
# Planen der Bereitstellung von MBAM mit dem Konfigurations-Manager


Zur Bereitstellung von MBAM mit der Configuration Manager-Topologie wird eine Architektur mit drei Servern empfohlen, die 200.000-Clients unterstützt. Verwenden Sie einen separaten Server zum Ausführen von Configuration Manager, und installieren Sie die grundlegenden Verwaltungs-und Überwachungsfeatures auf zwei Servern, wie im Architektur Bild unter [Erste Schritte – verwenden von MBAM mit Configuration Manager](getting-started---using-mbam-with-configuration-manager.md)dargestellt.

**Wichtig**  
Windows to go wird nicht unterstützt, wenn Sie die integrierte Topologie von MBAM mit Configuration Manager 2007 installieren.



## Voraussetzungen für die Bereitstellung für die Installation von MBAM mit Configuration Manager


Stellen Sie sicher, dass Sie die folgenden Voraussetzungen erfüllt haben, bevor Sie MBAM mit Configuration Manager installieren:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Voraussetzung</th>
<th align="left">Weitere Informationen</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Stellen Sie sicher, dass der Configuration Manager-Server ein primärer Standort im Configuration Manager-System ist.</p></td>
<td align="left"><p>n.v.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Aktivieren Sie den Hardware Inventur Client-Agent auf dem Configuration Manager-Server.</p></td>
<td align="left"><p>Informationen zu Configuration Manager 2007 finden Sie unter <a href="https://go.microsoft.com/fwlink/?LinkId=301656" data-raw-source="[How to Configure Hardware Inventory for a Site](https://go.microsoft.com/fwlink/?LinkId=301656)"> Konfigurieren der Hardware Inventur für eine Website </a> .</p>
<p>Informationen zu System Center 2012-Konfigurations-Manager finden Sie unter <a href="https://go.microsoft.com/fwlink/?LinkId=301685" data-raw-source="[How to Configure Hardware Inventory in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=301685)"> Konfigurieren der Hardware Inventur in Configuration Manager </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Aktivieren Sie den DCM-Agent (Desired Configuration Management) oder die Kompatibilitätseinstellungen, abhängig von der Version von Configuration Manager, die Sie verwenden.</p></td>
<td align="left"><p>Aktivieren Sie für Configuration Manager 2007 die Eigenschaften des Client-Agents für die <a href="https://go.microsoft.com/fwlink/?LinkId=301686" data-raw-source="[Desired Configuration Management Client Agent Properties](https://go.microsoft.com/fwlink/?LinkId=301686)"> Verwaltung der gewünschten Konfiguration </a> .</p>
<p>Informationen zu System Center 2012-Konfigurations-Manager finden Sie unter <a href="https://go.microsoft.com/fwlink/?LinkId=301687" data-raw-source="[Configuring Compliance Settings in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=301687)"> Konfigurieren von Kompatibilitätseinstellungen in Configuration Manager </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Definieren Sie einen Reporting Services-Punkt in Configuration Manager. Für SQL Reporting Services erforderlich.</p></td>
<td align="left"><p>Informationen zu Configuration Manager 2007 finden Sie unter <a href="https://go.microsoft.com/fwlink/?LinkId=301688" data-raw-source="[How to Create a Reporting Services Point for SQL Reporting Services](https://go.microsoft.com/fwlink/?LinkId=301688)"> Erstellen eines Reporting Services-Punkts für SQL Reporting Services </a> .</p>
<p>Informationen zu System Center 2012-Konfigurations-Manager finden Sie unter <a href="https://go.microsoft.com/fwlink/?LinkId=301689" data-raw-source="[Prerequisites for Reporting in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=301689)"> Voraussetzungen für die Berichterstellung in Configuration Manager </a> .</p></td>
</tr>
</tbody>
</table>



## <a href="" id="---------configuration-manager-supported-versions"></a> Von Configuration Manager unterstützte Versionen


MBAM unterstützt die folgenden Versionen von Configuration Manager:

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
<tr class="odd">
<td align="left"><p>Microsoft System Center Configuration Manager 2007 R2</p></td>
<td align="left"><p>SP1 oder höher</p></td>
<td align="left"><p>64Bit</p>
<div class="alert">
<strong>Hinweis:</strong><br/><p>Obwohl der Configuration Manager 2007 32-Bit ist, müssen Sie ihn und SQL Server auf einem 64-Bit-Betriebssystem installieren, um der 64-Bit-MBAM-Software entsprechen zu können.</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft System Center 2012-Konfigurations-Manager</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>64Bit</p></td>
</tr>
</tbody>
</table>



Eine Liste der unterstützten Konfigurationen für den Configuration Manager-Server finden Sie auf der entsprechenden Webseite für die Version von Configuration Manager, die Sie verwenden. MBAM hat keine zusätzlichen Systemanforderungen für den Configuration Manager-Server.

## <a href="" id="---------mbam-and-sql-server-system-requirements"></a> MBAM-und SQL Server-System Anforderungen


Die unterstützten Konfigurationen und Systemanforderungen für die MBAM-Server und SQL Server für die Configuration Manager-Topologie sind dieselben wie für die eigenständige Topologie. Die eigenständigen Systemanforderungen finden Sie unter [unterstützte MBAM 2,0-Konfigurationen](mbam-20-supported-configurations-mbam-2.md). Informationen zu den Anforderungen des MBAM-Servers und des SQL Server-Prozessors, des Arbeitsspeichers und des Speicherplatzes für die Configuration Manager-Topologie finden Sie in den folgenden Abschnitten.

## MBAM-Server Prozessor, RAM und Speicherplatzanforderungen für MBAM


In der folgenden Tabelle sind die Server Prozessor-, RAM-und Speicherplatzanforderungen für MBAM-Server aufgelistet, wenn Sie die Configuration Manager-Integrations Topologie verwenden.

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



## SQL Server-Prozessor, Arbeitsspeicher und Speicherplatzanforderungen


In der folgenden Tabelle sind die Anforderungen für den Server Prozessor, den Arbeitsspeicher und den Speicherplatz für den SQL Server-Computer aufgeführt, wenn Sie die Configuration Manager-Integrations Topologie verwenden.

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
<td align="left"><p>4 GB</p></td>
<td align="left"><p>8 GB</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Freier Speicherplatz</p></td>
<td align="left"><p>5 GB</p></td>
<td align="left"><p>5 GB oder höher</p></td>
</tr>
</tbody>
</table>



## Erforderliche Berechtigungen zum Installieren des MBAM-Servers


Zum Installieren von MBAM mit Configuration Manager müssen Sie über einen Administrator Benutzer in Configuration Manager verfügen, der über eine Sicherheitsrolle mit den in der folgenden Tabelle aufgeführten Mindestberechtigungen verfügt. Die Tabelle enthält auch die Rechte, die Sie über die grundlegenden Computeradministrator Rechte hinaus benötigen, um den MBAM-Server zu installieren.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Berechtigungen</th>
<th align="left">MBAM-Server Feature</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>SQL instance-Anmelde Server Rollen:-dbcreator-processadmin</p></td>
<td align="left"><p>- Wiederherstellungsdatenbank – Überwachungsdatenbank</p></td>
</tr>
<tr class="even">
<td align="left"><p>SQL Server Reporting Services-Instanzen Rechte:-Erstellen von Ordnern-veröffentlichen von Berichten</p></td>
<td align="left"><p>- Integration von System Center Configuration Manager</p></td>
</tr>
</tbody>
</table>



**System Center 2012 Configuration Manager**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Berechtigungen</th>
<th align="left">Configuration Manager-Server Feature</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Configuration Manager-Website Rechte:-Lesen</p></td>
<td align="left"><p>Integration von System Center Configuration Manager</p></td>
</tr>
<tr class="even">
<td align="left"><p>Configuration Manager-Sammlungs Rechte:-Erstellen-Löschen-lesen-ändern – Bereitstellen von Konfigurationselementen</p></td>
<td align="left"><p>Integration von System Center Configuration Manager</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Configuration Manager-Konfigurationselement Rechte:-Create-DELETE-Read</p></td>
<td align="left"><p>Integration von System Center Configuration Manager</p></td>
</tr>
</tbody>
</table>



**Configuration Manager 2007**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Berechtigungen</th>
<th align="left">Configuration Manager-Server Feature</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Configuration Manager-Website Rechte:-Lesen</p></td>
<td align="left"><p>Integration von System Center Configuration Manager</p></td>
</tr>
<tr class="even">
<td align="left"><p>Configuration Manager-Sammlungs Rechte:-Create-DELETE-Read-ReadResource</p></td>
<td align="left"><p>Integration von System Center Configuration Manager</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Configuration Manager-Konfigurationselement Rechte:-Create-DELETE-Read-Distribute</p></td>
<td align="left"><p>Integration von System Center Configuration Manager</p></td>
</tr>
</tbody>
</table>



## Reihenfolge der Bereitstellung von MBAM-Features für die Configuration Manager-Topologie


Wenn Sie MBAM auf dem Configuration Manager-Server bereitstellen, müssen Sie die Bereitstellungsaufgaben in der folgenden Reihenfolge ausführen:

1.  Bearbeiten Sie die Datei "Configuration. mof" auf dem Configuration Manager-Server.

2.  Erstellen oder bearbeiten Sie den SMS-_def. MOF-Datei-Konfigurations-Manager-Server.

3.  Installieren Sie MBAM auf dem Configuration Manager-Server.

4.  Installieren Sie die Wiederherstellungsdatenbank und die Überwachungsdatenbank auf dem Datenbankserver.

5.  Installieren Sie die MBAM-Features auf dem Verwaltungs-und Überwachungs Server.

## Prüfliste für die Planung für die Installation von MBAM mit Configuration Manager


In dieser Checkliste werden die empfohlenen Schritte und eine Liste der Elemente auf höherer Ebene erläutert, die bei der Planung einer Microsoft BitLocker-Verwaltungs-und-Überwachungs Bereitstellung mit Configuration Manager berücksichtigt werden sollten. Es wird empfohlen, dass Sie diese Checkliste in ein Kalkulationstabellenprogramm kopieren und für ihre Verwendung anpassen.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left">Aufgabe</th>
<th align="left">Verweise</th>
<th align="left">Anmerkungen</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Lesen Sie die Informationen zu den ersten Schritten, in denen beschrieben wird, wie der Configuration Manager mit MBAM funktioniert, und zeigt die empfohlene Architektur auf hoher Ebene an.</p></td>
<td align="left"><p><a href="getting-started---using-mbam-with-configuration-manager.md" data-raw-source="[Getting Started - Using MBAM with Configuration Manager](getting-started---using-mbam-with-configuration-manager.md)">Erste Schritte – Verwenden von MBAM mit dem Konfigurations-Manager</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Überprüfen Sie die Planungsinformationen, in denen die Voraussetzungen für die Bereitstellung, unterstützte Konfigurationen, erforderliche Berechtigungen und Bereitstellungsreihenfolge für die einzelnen Features beschrieben sind.</p></td>
<td align="left"><p>Planen der Bereitstellung von MBAM mit dem Konfigurations-Manager</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Planen und Konfigurieren von MBAM-Gruppenrichtlinienanforderungen</p></td>
<td align="left"><p><a href="planning-for-mbam-20-group-policy-requirements-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Group Policy Requirements](planning-for-mbam-20-group-policy-requirements-mbam-2.md)">Planen der Gruppenrichtlinienanforderungen für MBAM 2.0</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Planen und erstellen Sie die erforderlichen Active Directory-Domänendienste-Sicherheitsgruppen, und planen Sie die Mitgliedschaftsanforderungen für MBAM Local Security Group.</p></td>
<td align="left"><p><a href="planning-for-mbam-20-administrator-roles-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Administrator Roles](planning-for-mbam-20-administrator-roles-mbam-2.md)">Planen der Administratorrollen für MBAM 2.0</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Planen der Bereitstellung der MBAM-Client Bereitstellung</p></td>
<td align="left"><p><a href="planning-for-mbam-20-client-deployment-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Client Deployment](planning-for-mbam-20-client-deployment-mbam-2.md)">Planen der Clientbereitstellung für MBAM 2.0</a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



## Verwandte Themen


[Verwenden von MBAM mit dem Konfigurations-Manager](using-mbam-with-configuration-manager.md)









