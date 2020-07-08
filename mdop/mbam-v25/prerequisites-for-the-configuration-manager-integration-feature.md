---
title: Voraussetzungen für das Configuration Manager-Integrationsfeature
description: Voraussetzungen für das Configuration Manager-Integrationsfeature
author: dansimp
ms.assetid: b318cbd3-b009-44b8-991b-f7364c1cae88
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: af7abd50f6218810dd6718f091512b48fee32652
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810900"
---
# Voraussetzungen für das Configuration Manager-Integrationsfeature


Wenn Sie MBAM mit der System Center Configuration Manager-Integrations Topologie bereitstellen, empfehlen wir eine Architektur mit drei Servern, wie in [der allgemeinen Architektur von MBAM 2,5 mit der Configuration Manager-Integrations Topologie](high-level-architecture-of-mbam-25-with-configuration-manager-integration-topology.md)beschrieben. Diese Architektur kann 500.000-Clientcomputer unterstützen.

**Wichtig**  
Windows to go wird bei der Installation der Configuration Manager-Integrations Topologie nicht unterstützt, wenn Sie Configuration Manager 2007 verwenden.



## Allgemeine Voraussetzungen für das Configuration Manager-Integrations Feature


Wenn Sie MBAM mit Configuration Manager installieren, sind zusätzlich zu den Voraussetzungen für die eigenständige Topologie die folgenden zusätzlichen Voraussetzungen erforderlich.

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
<td align="left"><p>Der Configuration Manager-Server ist ein primärer Standort im Configuration Manager-System.</p></td>
<td align="left"><p>n.v.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Der Hardware Inventur Client-Agent befindet sich auf dem Configuration Manager-Server.</p></td>
<td align="left"><p>Informationen zu System Center 2012-Konfigurations-Manager finden Sie unter <a href="https://go.microsoft.com/fwlink/?LinkId=301685" data-raw-source="[How to Configure Hardware Inventory in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=301685)"> Konfigurieren der Hardware Inventur in Configuration Manager </a> .</p>
<p>Informationen zu Configuration Manager 2007 finden Sie unter <a href="https://go.microsoft.com/fwlink/?LinkId=301656" data-raw-source="[How to Configure Hardware Inventory for a Site](https://go.microsoft.com/fwlink/?LinkId=301656)"> Konfigurieren der Hardware Inventur für eine Website </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Je nach der von Ihnen verwendeten Version von Configuration Manager ist eine der folgenden Optionen aktiviert:</p>
<ul>
<li><p>Kompatibilitätseinstellungen – (System Center 2012-Konfigurations-Manager)</p></li>
<li><p>DCM-Client-Agent (Desired Configuration Management) – (Configuration Manager 2007)</p></li>
</ul></td>
<td align="left"><p>Informationen zu System Center 2012-Konfigurations-Manager finden Sie unter <a href="https://go.microsoft.com/fwlink/?LinkId=301687" data-raw-source="[Configuring Compliance Settings in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=301687)"> Konfigurieren von Kompatibilitätseinstellungen in Configuration Manager </a> .</p>
<p>Informationen zu Configuration Manager 2007 finden Sie unter <a href="https://go.microsoft.com/fwlink/?LinkId=301686" data-raw-source="[Desired Configuration Management Client Agent Properties](https://go.microsoft.com/fwlink/?LinkId=301686)"> Client-Agent-Eigenschaften der gewünschten Configuration-Verwaltung </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Ein Reporting Services-Punkt ist in Configuration Manager definiert. Erforderlich für SQL Server Reporting Services (SSRS).</p></td>
<td align="left"><p>Informationen zu System Center 2012-Konfigurations-Manager finden Sie unter <a href="https://go.microsoft.com/fwlink/?LinkId=301689" data-raw-source="[Prerequisites for Reporting in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=301689)"> Voraussetzungen für die Berichterstellung in Configuration Manager </a> .</p>
<p>Informationen zu Configuration Manager 2007 finden Sie unter <a href="https://go.microsoft.com/fwlink/?LinkId=301688" data-raw-source="[How to Create a Reporting Services Point for SQL Reporting Services](https://go.microsoft.com/fwlink/?LinkId=301688)"> Erstellen eines Reporting Services-Punkts für SQL Reporting Services </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Configuration Manager 2007 erfordert Microsoft .NET Framework 2,0</p></td>
<td align="left"><p>Der DCM-Client-Agent (Desired Configuration Management) in Configuration Manager 2007 erfordert .NET Framework 2,0, um die Kompatibilität zu melden.</p>
<div class="alert">
<strong>Hinweis:</strong><br/><p>Beim Installieren von .NET Framework 3,5 wird .NET Framework 2,0 automatisch installiert.</p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



## Erforderliche Berechtigungen zum Installieren von MBAM mit Configuration Manager


Zum Installieren von MBAM mit Configuration Manager müssen Sie über einen Administrator Benutzer in Configuration Manager verfügen, der über eine Sicherheitsrolle mit den in der folgenden Tabelle aufgeführten Mindestberechtigungen verfügt. Die Tabelle enthält auch die Rechte, die Sie über die grundlegenden Computeradministrator Rechte hinaus benötigen, um den MBAM-Server zu installieren.

**Die Berechtigungen in der folgenden Tabelle gelten für beide Versionen von Configuration Manager.**

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
<td align="left"><p>SQL Server-Instanz-Anmelde Server Rollen:-dbcreator-processadmin</p></td>
<td align="left"><p>- Wiederherstellungsdatenbank – Überwachungsdatenbank</p></td>
</tr>
<tr class="even">
<td align="left"><p>Rechte von SSRS-Instanzen:-Erstellen von Ordnern-veröffentlichen von Berichten</p></td>
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



## Erforderliche Änderungen für die MOF-Dateien


Damit die Clientcomputer BitLocker-Kompatibilitätsdetails über die MBAM-Konfigurations-Manager-Berichte melden können, müssen Sie die Datei "Configuration. mof" und die SMS \ _def. MOF-Datei für System Center 2012 Configuration Manager und Microsoft System Center Configuration Manager 2007 bearbeiten. Anweisungen hierzu finden Sie unter [Voraussetzungen für MBAM 2,5-Server, die nur für die Configuration Manager-Integrations Topologie gelten](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md).



## Verwandte Themen


[MBAM 2.5-Servervoraussetzungen für eigenständige und Configuration Manager-Integrationstopologien](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)

[MBAM 2.5-Servervoraussetzungen, die nur für die Configuration Manager-Integrationstopologie gelten](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md)



## Sie haben einen Vorschlag für MBAM?
- [Hier](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)können Sie Vorschläge hinzufügen oder abstimmen. 
- Bei MBAM-Problemen verwenden Sie das [MBAM TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





