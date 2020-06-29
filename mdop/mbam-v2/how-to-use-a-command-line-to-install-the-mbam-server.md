---
title: So verwenden Sie eine Befehlszeile zum Installieren des MBAM-Servers
description: So verwenden Sie eine Befehlszeile zum Installieren des MBAM-Servers
author: dansimp
ms.assetid: 6ffc6d41-a793-42c2-b997-95ba47550648
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a689a2df77300300073b2731281004feac87305f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811278"
---
# So verwenden Sie eine Befehlszeile zum Installieren des MBAM-Servers


Sie können eine Befehlszeile verwenden, um den MBAM-Server entweder mit der eigenständigen oder der Configuration Manager-Topologie zu installieren. Das folgende Befehlszeilenbeispiel dient zum Bereitstellen von MBAM auf einem einzelnen Server, bei dem es sich um eine Architektur handelt, die nur in einer Testumgebung verwendet werden sollte. Sie müssen die Befehlszeile beim Bereitstellen von MBAM in einer Produktionsumgebung, die über mehrere Server verfügen soll, entsprechend ändern.

## Befehlszeile für die Bereitstellung des mbam 2.0-Servers mit der eigenständigen Topologie


Sie können eine Befehlszeile verwenden, die der folgenden ähnelt, um den MBAM-Server mit der eigenständigen Topologie zu installieren.

``` syntax
MbamSetup.exe /qb /l*v MaltaServerInstall.log TOPOLOGY=0 I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 ADDLOCAL=KeyDatabase,ReportsDatabase,Reports,AdministrationMonitoringServer,SelfServiceServer,PolicyTemplate,REPORTS_USERACCOUNT=[UserDomain]\[UserName1] REPORTS_USERACCOUNTPW=[UserPwd1] COMPLIDB_SQLINSTANCE=%computername% RECOVERYANDHWDB_SQLINSTANCE=%computername% SRS_INSTANCENAME=%computername% ADMINANDMON_WEBSITE_PORT=83 WEBSITE_PORT=83
```

In der folgenden Tabelle werden die Befehlszeilenparameter für die Bereitstellung des MBAM-Servers mit der eigenständigen Topologie beschrieben.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Parameter</th>
<th align="left">Parameter Wert</th>
<th align="left">Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Topologie</p></td>
<td align="left"><p>0</p></td>
<td align="left"><p>0 – eigenständige Topologie</p></td>
</tr>
<tr class="even">
<td align="left"><p>I_ACCEPT_ENDUSER_LICENSE_AGREEMENT</p></td>
<td align="left"><p>01</p></td>
<td align="left"><p>0 – akzeptieren Sie die Lizenz Abkommen1 – akzeptieren Sie den Lizenzvertrag.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>ADDLOCAL</p></td>
<td align="left"><p></p></td>
<td align="left"><p>Auf dem Server zu installiere Features</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p>Keydatabase</p></td>
<td align="left"><p>Wiederherstellungsdatenbank</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p>ReportsDatabase</p></td>
<td align="left"><p>Datenbank für Konformitäts-und Überwachungsberichte</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p>Berichte</p></td>
<td align="left"><p>Konformitäts-und Überwachungsberichte</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p>AdministrationMonitoringServer</p></td>
<td align="left"><p>Website "Verwaltung und Überwachung"</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p>SelfServiceServer</p></td>
<td align="left"><p>Self-Service-Portal</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p>PolicyTemplate</p></td>
<td align="left"><p>MBAM-Gruppenrichtlinienvorlage</p></td>
</tr>
<tr class="even">
<td align="left"><p>REPORTS_USERACCOUNT</p></td>
<td align="left"><p>User Domain Benutzername1</p></td>
<td align="left"><p>Domäne und Benutzerkonto des Reporting Services-Dienstkontos, das auf die Compliance-und Überwachungsdatenbank zugreifen soll</p></td>
</tr>
<tr class="odd">
<td align="left"><p>REPORTS_USERACCOUNTPW</p></td>
<td align="left"><p>[UserPwd1]</p></td>
<td align="left"><p>Kennwort des Reporting Services-Dienstkontos, das auf die Compliance-und Überwachungsdatenbank zugreifen soll</p></td>
</tr>
<tr class="even">
<td align="left"><p>COMPLIDB_SQLINSTANCE</p></td>
<td align="left"><p>Computername</p></td>
<td align="left"><p>Name der SQL Server-Instanz für die Compliance-und Überwachungsdatenbank – ersetzen <strong> von% Computer </strong> Name% durch den Computernamen</p></td>
</tr>
<tr class="odd">
<td align="left"><p>RECOVERYANDHWDB_SQLINSTANCE</p></td>
<td align="left"><p>Computername</p></td>
<td align="left"><p>Name der SQL Server-Instanz für die Wiederherstellungsdatenbank – ersetzen <strong> von% Computer </strong> Name% durch den Computernamen</p></td>
</tr>
<tr class="even">
<td align="left"><p>SRS_INSTANCENAME</p></td>
<td align="left"><p>Computername</p></td>
<td align="left"><p>SQL Server-Berichtsserverinstanz, in der die Konformitäts-und Überwachungsberichte installiert werden – ersetzen <strong> von% Computer </strong> Name% durch den Computernamen</p></td>
</tr>
<tr class="odd">
<td align="left"><p>ADMINANDMON_WEBSITE_PORT</p></td>
<td align="left"><p>83</p></td>
<td align="left"><p>Port für die Verwaltungs-und Überwachungs Website "83" ist nur ein Beispiel</p></td>
</tr>
<tr class="even">
<td align="left"><p>WEBSITE_PORT</p></td>
<td align="left"><p>83</p></td>
<td align="left"><p>Port für die Self-Service-Portal-Website; "83" ist nur ein Beispiel</p></td>
</tr>
</tbody>
</table>

 

## Befehlszeile für die Bereitstellung des mbam 2.0-Servers mit der Configuration Manager-Topologie


Sie können eine Befehlszeile verwenden, die der folgenden ähnelt, um den MBAM-Server mit der Configuration Manager-Topologie zu installieren.

``` syntax
MbamSetup.exe /qn /l*v MaltaServerInstall.log I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 TOPOLOGY=1 COMPLIDB_SQLINSTANCE=%computername% RECOVERYANDHWDB_SQLINSTANCE=%computername% SRS_INSTANCENAME=%computername% REPORTS_USERACCOUNT=[UserDomain]\[UserName] REPORTS_USERACCOUNTPW=[UserPwd] ADMINANDMON_WEBSITE_PORT=83 WEBSITE_PORT=83
```

In der folgenden Tabelle werden die Befehlszeilenparameter für die Installation des mbam 2.0-Servers mit der Configuration Manager-Topologie beschrieben.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Parameter</th>
<th align="left">Parameter Wert</th>
<th align="left">Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Topologie</p></td>
<td align="left"><p>1</p></td>
<td align="left"><p>1 – Configuration Manager-Topologie</p></td>
</tr>
<tr class="even">
<td align="left"><p>I_ACCEPT_ENDUSER_LICENSE_AGREEMENT</p></td>
<td align="left"><p>01</p></td>
<td align="left"><p>0 – akzeptieren Sie die Lizenz Abkommen1 – akzeptieren Sie den Lizenzvertrag.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>COMPLIDB_SQLINSTANCE</p></td>
<td align="left"><p>Computername</p></td>
<td align="left"><p>Name der SQL Server-Instanz für die Überwachungsdatenbank – ersetzen <strong> von% Computer </strong> Name% durch den Computernamen</p></td>
</tr>
<tr class="even">
<td align="left"><p>RECOVERYANDHWDB_SQLINSTANCE</p></td>
<td align="left"><p>Computername</p></td>
<td align="left"><p>Name der SQL Server-Instanz für die Wiederherstellungsdatenbank – ersetzen <strong> von% Computer </strong> Name% durch den Computernamen</p></td>
</tr>
<tr class="odd">
<td align="left"><p>SRS_INSTANCENAME</p></td>
<td align="left"><p>Computername</p></td>
<td align="left"><p>SQL Server-Berichtsserverinstanz, in der die Überwachungsberichte installiert werden – ersetzen von% Computername% durch den Computernamen</p></td>
</tr>
<tr class="even">
<td align="left"><p>REPORTS_USERACCOUNT</p></td>
<td align="left"><p>User Domain Benutzername1</p></td>
<td align="left"><p>Domäne und Benutzerkonto des Reporting Services-Dienstkontos, das auf die Compliance-und Überwachungsdatenbank zugreifen soll</p></td>
</tr>
<tr class="odd">
<td align="left"><p>REPORTS_USERACCOUNTPW</p></td>
<td align="left"><p>[UserPwd1]</p></td>
<td align="left"><p>Kennwort des Reporting Services-Dienstkontos, das auf die Compliance-und Überwachungsdatenbank zugreifen soll</p></td>
</tr>
<tr class="even">
<td align="left"><p>ADMINANDMON_WEBSITE_PORT</p></td>
<td align="left"><p>83</p></td>
<td align="left"><p>Port für die Verwaltungs-und Überwachungs Website "83" ist nur ein Beispiel</p></td>
</tr>
<tr class="odd">
<td align="left"><p>WEBSITE_PORT</p></td>
<td align="left"><p>83</p></td>
<td align="left"><p>Port für die Self-Service-Portal-Website; "83" ist nur ein Beispiel</p></td>
</tr>
</tbody>
</table>

 

## Verwandte Themen


[Bereitstellen der Serverinfrastruktur von MBAM 2.0](deploying-the-mbam-20-server-infrastructure-mbam-2.md)

 

 





