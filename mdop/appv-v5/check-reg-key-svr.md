---
title: Überprüfen der Registrierungsschlüssel vor der Installation von App-V 5.x Server
description: Überprüfen der Registrierungsschlüssel vor der Installation von App-V 5.x Server
author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.openlocfilehash: 9fe5a1b37d0fb5208d138939bb2fc79c89171fb3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805930"
---
# Überprüfen der Registrierungsschlüssel vor der Installation von App-V 5.x Server

Wenn Sie den App-v-Server vom APP-v 5,0 SP1-Hotfix-Paket 3 oder höher aktualisieren, führen Sie die Schritte in diesem Abschnitt aus, bevor Sie den App-v 5. x-Server installieren.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Wenn dieser Schritt erforderlich ist</strong></p></td>
<td align="left"><p>Sie Aktualisieren von App-V 5,0 SP1 mit allen nachfolgenden Hotfix-Paketen, die Sie mithilfe einer MSP-Datei installiert haben.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Für welche Komponenten muss dieser Schritt ausgeführt werden?</strong></p></td>
<td align="left"><p>Nur die App-V Server-Komponenten, die Sie aktualisieren.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Wenn Sie diesen Schritt ausführen müssen</strong></p></td>
<td align="left"><p>Vor dem Upgrade des App-v-Servers auf App-v 5. x</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Was Sie tun müssen</strong></p></td>
<td align="left"><p>Aktualisieren Sie anhand der Informationen in den folgenden Tabellen jeden Registrierungsschlüsselwert unter <code>HKLM\Software\Microsoft\AppV\Server</code> mit dem Wert, den Sie in der ursprünglichen Server Installation angegeben haben. Durch das Abschließen dieses Schritts werden Registrierungswerte wiederhergestellt, die möglicherweise entfernt wurden, als App-V 5,0 SP1-Hotfix-Pakete installiert wurden.</p></td>
</tr>
</tbody>
</table>

 

**ManagementDatabase-Taste**

Wenn Sie die Verwaltungsdatenbank installieren, legen Sie diese Registrierungsschlüssel unter `HKLM\Software\Microsoft\AppV\Server\ManagementDatabase` .

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Schlüsselname</th>
<th align="left">Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>IS_MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</p></td>
<td align="left"><p>Beschreibt, ob ein öffentliches Zugriffskonto für den Zugriff auf nicht lokale Verwaltungs Datenbanken erforderlich ist. Value ist auf "1" gesetzt, wenn dies erforderlich ist.</p></td>
</tr>
<tr class="even">
<td align="left"><p>MANAGEMENT_DB_NAME</p></td>
<td align="left"><p>Der Name der Verwaltungsdatenbank.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT</p></td>
<td align="left"><p>Konto, das für den Lesezugriff auf die Verwaltungsdatenbank verwendet wird.</p>
<p>Wird verwendet <code>IS_MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code> , wenn auf 1 gesetzt ist.</p></td>
</tr>
<tr class="even">
<td align="left"><p>MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_SID</p></td>
<td align="left"><p>Secure Identifier (SID) des Kontos, das für den Zugriff auf die Verwaltungsdatenbank für Read (Public) verwendet wird.</p>
<p>Wird verwendet <code>IS_MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code> , wenn auf 1 gesetzt ist.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>MANAGEMENT_DB_SQL_INSTANCE</p></td>
<td align="left"><p>SQL Server-Instanz für die Verwaltungsdatenbank.</p>
<p>Wenn der Wert leer ist, wird die Standarddatenbankinstanz verwendet.</p></td>
</tr>
<tr class="even">
<td align="left"><p>MANAGEMENT_DB_WRITE_ACCESS_ACCOUNT</p></td>
<td align="left"><p>Konto, das für den Schreibzugriff (Administrator) für die Verwaltungsdatenbank verwendet wird.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>MANAGEMENT_DB_WRITE_ACCESS_ACCOUNT_SID</p></td>
<td align="left"><p>Secure Identifier (SID) des Kontos, das für den Schreibzugriff (Administrator) auf die Verwaltungsdatenbank verwendet wird.</p></td>
</tr>
<tr class="even">
<td align="left"><p>MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</p></td>
<td align="left"><p>Verwaltungsserver-Remotecomputer Konto (Domain\Account).</p></td>
</tr>
<tr class="odd">
<td align="left"><p>MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</p></td>
<td align="left"><p>Installations Administrator-Anmeldung für den Verwaltungsserver (Domain\Account).</p></td>
</tr>
<tr class="even">
<td align="left"><p>MANAGEMENT_SERVER_MACHINE_USE_LOCAL</p></td>
<td align="left"><p>Gültige Werte sind:</p>
<ul>
<li><p><strong>1 </strong> – der Verwaltungsdienst befindet sich auf dem lokalen Computer, das heißt, MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT ist leer.</p></li>
<li><p><strong>0 </strong> - der Verwaltungsdienst befindet sich auf einem anderen Computer als auf dem lokalen Computer.</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

**Managementservice-Taste**

Wenn Sie den Verwaltungsserver installieren, legen Sie diese Registrierungsschlüssel unter `HKLM\Software\Microsoft\AppV\Server\ManagementService` .

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Schlüsselname</th>
<th align="left">Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>MANAGEMENT_ADMINACCOUNT</p></td>
<td align="left"><p>Active Directory-Domänendienste (AD DS)-Gruppe oder-Konto, das zum Verwalten von App-V (Domain\Account) autorisiert ist.</p></td>
</tr>
<tr class="even">
<td align="left"><p>MANAGEMENT_DB_SQL_INSTANCE</p></td>
<td align="left"><p>SQL Server-Instanz, die die Verwaltungsdatenbank enthält.</p>
<p>Wenn der Wert leer ist, wird die Standarddatenbankinstanz verwendet.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>MANAGEMENT_DB_SQL_SERVER_NAME</p></td>
<td align="left"><p>Der Name des Remote-SQL-Servers mit der Verwaltungsdatenbank.</p>
<p>Wenn der Wert leer ist, wird der lokale Computer verwendet.</p></td>
</tr>
</tbody>
</table>

 

**ReportingDatabase-Taste**

Wenn Sie die Berichtsdatenbank installieren, legen Sie diese Registrierungsschlüssel unter `HKLM\Software\Microsoft\AppV\Server\ReportingDatabase` .

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Schlüsselname</th>
<th align="left">Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>IS_REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</p></td>
<td align="left"><p>Beschreibt, ob ein öffentliches Zugriffskonto für den Zugriff auf nicht lokale Berichtsdatenbanken erforderlich ist. Value ist auf "1" gesetzt, wenn dies erforderlich ist.</p></td>
</tr>
<tr class="even">
<td align="left"><p>REPORTING_DB_NAME</p></td>
<td align="left"><p>Der Name der Berichtsdatenbank.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>REPORTING_DB_PUBLIC_ACCESS_ACCOUNT</p></td>
<td align="left"><p>Konto, das für den Lesezugriff auf die Berichtsdatenbank verwendet wird.</p>
<p>Wird verwendet <code>IS_REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code> , wenn auf 1 gesetzt ist.</p></td>
</tr>
<tr class="even">
<td align="left"><p>REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_SID</p></td>
<td align="left"><p>Secure Identifier (SID) des Kontos, das für den Zugriff auf die Berichtsdatenbank gelesen (öffentlich) verwendet wird.</p>
<p>Wird verwendet <code>IS_REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code> , wenn auf 1 gesetzt ist.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>REPORTING_DB_SQL_INSTANCE</p></td>
<td align="left"><p>SQL Server-Instanz für die Berichtsdatenbank.</p>
<p>Wenn der Wert leer ist, wird die Standarddatenbankinstanz verwendet.</p></td>
</tr>
<tr class="even">
<td align="left"><p>REPORTING_DB_WRITE_ACCESS_ACCOUNT</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>REPORTING_DB_WRITE_ACCESS_ACCOUNT_SID</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</p></td>
<td align="left"><p>Reporting Server-Remotecomputer Konto (Domain\Account).</p></td>
</tr>
<tr class="odd">
<td align="left"><p>REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</p></td>
<td align="left"><p>Installations Administrator-Anmeldung für den Berichtsserver (Domain\Account).</p></td>
</tr>
<tr class="even">
<td align="left"><p>REPORTING_SERVER_MACHINE_USE_LOCAL</p></td>
<td align="left"><p>Gültige Werte sind:</p>
<ul>
<li><p><strong>1 </strong> – der Berichterstattungsdienst befindet sich auf dem lokalen Computer, das heißt, REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT ist leer.</p></li>
<li><p><strong>0 </strong> - der Berichterstattungsdienst befindet sich auf einem anderen Computer als auf dem lokalen Computer.</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

**ReportingService-Taste**

Wenn Sie den Berichtsserver installieren, legen Sie diese Registrierungsschlüssel unter `HKLM\Software\Microsoft\AppV\Server\ReportingService` .

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Schlüsselname</th>
<th align="left">Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>REPORTING_DB_SQL_INSTANCE</p></td>
<td align="left"><p>SQL Server-Instanz für die Berichtsdatenbank.</p>
<p>Wenn der Wert leer ist, wird die Standarddatenbankinstanz verwendet.</p></td>
</tr>
<tr class="even">
<td align="left"><p>REPORTING_DB_SQL_SERVER_NAME</p></td>
<td align="left"><p>Der Name des Remote-SQL-Servers mit der Berichtsdatenbank.</p>
<p>Wenn der Wert leer ist, wird der lokale Computer verwendet.</p></td>
</tr>
</tbody>
</table>

