---
title: Informationen zu App-V 5.0 SP3
description: Informationen zu App-V 5.0 SP3
author: dansimp
ms.assetid: 67b5268b-edc1-4027-98b0-b3937dd70a6b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/02/2016
ms.openlocfilehash: bc72f3f72c2b06470287dfe4ba3ed22abcc6068b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806120"
---
# Informationen zu App-V 5.0 SP3


Verwenden Sie die folgenden Abschnitte, um Informationen zu bedeutenden Änderungen zu überprüfen, die für Microsoft Application Virtualization (App-V) 5,0 SP3 gelten:

-   [Software-Voraussetzungen und unterstützte Konfigurationen für App-V 5,0 SP3](#bkmk-sp3-prereq-configs)

-   [Migrieren zu App-V 5,0 SP3](#bkmk-migrate-to-50sp3)

-   [Die XML-Datei für eine manuell erstellte Verbindungsgruppe erfordert ein Update auf ein Schema](#bkmk-update-schema-cg)

-   [Verbesserungen an Verbindungsgruppen](#bkmk-cg-improvements)

-   [Administratoren können Pakete für einen bestimmten Benutzer veröffentlichen und deren Veröffentlichung aufheben.](#bkmk-usersid-pub-pkgs-specf-user)

-   [Nur Administratoren das Veröffentlichen und Aufheben der Veröffentlichung von Paketen ermöglichen](#bkmk-admins-only-pub-unpub-pkgs)

-   [RunVirtual-Registrierungsschlüssel unterstützt Pakete, die für den Benutzer veröffentlicht werden](#bkmk-runvirtual-reg-key)

-   [Neue PowerShell-Cmdlets und Hilfe zu aktualisierbaren Cmdlets](#bkmk-posh-cmdlets-help)

-   [Primäres virtuelles Anwendungsverzeichnis (PVAD) ist ausgeblendet, kann aber aktiviert werden](#bkmk-pvad-hidden)

-   [Clientversion ist erforderlich, um die App-V-Veröffentlichungsmetadaten anzuzeigen.](#bkmk-pub-metadata-clientversion)

-   [App-V-Ereignisprotokolle wurden konsolidiert](#bkmk-event-logs-moved)

## <a href="" id="bkmk-sp3-prereq-configs"></a>Software-Voraussetzungen und unterstützte Konfigurationen für App-V 5,0 SP3


Unter den folgenden Links finden Sie die Voraussetzungen für die App-V 5,0 SP3 und die unterstützten Konfigurationen.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Links zu Voraussetzungen und unterstützten Konfigurationen</th>
<th align="left">Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="app-v-50-sp3-prerequisites.md" data-raw-source="[App-V 5.0 SP3 Prerequisites](app-v-50-sp3-prerequisites.md)">Voraussetzungen für App-V 5.0 SP3</a></p></td>
<td align="left"><p>Erforderliche Software, die Sie vor dem Starten der App-V 5,0 SP3-Installation installieren müssen</p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="app-v-50-sp3-supported-configurations.md" data-raw-source="[App-V 5.0 SP3 Supported Configurations](app-v-50-sp3-supported-configurations.md)">Unterstützte App-V 5.0 SP3-Konfigurationen</a></p></td>
<td align="left"><p>Unterstützte Betriebssysteme und Hardwareanforderungen für App-V Server, Sequencer und Client Komponenten</p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-migrate-to-50sp3"></a>Migrieren zu App-V 5,0 SP3


Verwenden Sie die folgenden Informationen, um aus früheren Versionen auf App-V 5,0 SP3 zu aktualisieren.

### Vor dem Starten des Upgrades

Überprüfen Sie die folgenden Informationen, bevor Sie das Upgrade starten:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Zu überprüfende Elemente vor dem Upgrade</th>
<th align="left">Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Zu aktualisierbare Komponenten</p></td>
<td align="left"><ol>
<li><p>App-V-Server</p></li>
<li><p>Sequencer</p></li>
<li><p>App-v Client oder App-v Remote Desktop Dienste (RDS)-Client</p></li>
<li><p>Verbindungsgruppen</p></li>
</ol>
<div class="alert">
<strong>Hinweis:</strong><br/><p>Wenn Sie die App-V-Clientbenutzeroberfläche verwenden möchten, laden Sie die vorhandene Version aus der <a href="https://www.microsoft.com/download/details.aspx?id=41186" data-raw-source="[Microsoft Application Virtualization 5.0 Client UI Application](https://www.microsoft.com/download/details.aspx?id=41186)"> Microsoft Application Virtualization 5,0-Client-UI-Anwendung herunter </a> .</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>Aktualisieren von App-V 4. x</p></td>
<td align="left"><p>Sie müssen zuerst auf App-V 5,0 aktualisieren. Sie können nicht direkt von App-v 4. x auf App-v 5,0 SP3 aktualisieren.</p>
<p>Weitere Informationen finden Sie unter:</p>
<ul>
<li><p><a href="about-app-v-50.md" data-raw-source="[About App-V 5.0](about-app-v-50.md)">Informationen zu App-V 5.0</a> </p></li>
<li><p><a href="planning-for-migrating-from-a-previous-version-of-app-v.md" data-raw-source="[Planning for Migrating from a Previous Version of App-V](planning-for-migrating-from-a-previous-version-of-app-v.md)">Planen der Migration von einer früheren Version von App-V</a></p></li>
</ul>
<p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Aktualisieren von App-V 5,0 oder höher</p></td>
<td align="left"><p>Sie können direkt von einer der folgenden Versionen auf App-V 5,0 SP3 aktualisieren:</p>
<ul>
<li><p>App-V 5,0</p></li>
<li><p>App-V 5,0 SP1</p></li>
<li><p>App-V 5,0 SP2</p></li>
</ul>
<p>Führen Sie die Schritte in den verbleibenden Abschnitten dieses Artikels aus, um auf App-V 5,0 SP3 zu aktualisieren.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Erforderliche Änderungen an Paketen und Verbindungsgruppen nach dem Upgrade</p></td>
<td align="left"><p>Keine Pakete und Verbindungsgruppen funktionieren weiterhin wie bisher.</p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-steps-upgrd-infrastruc"></a>Schritte zum Upgrade der App-V-Infrastruktur

Führen Sie die folgenden Schritte aus, um die einzelnen Komponenten der APP-v-Infrastruktur auf App-v 5,0 SP3 zu aktualisieren.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Schritt</th>
<th align="left">Weitere Informationen</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Schritt 1: Aktualisieren Sie den App-V-Server.</p>
<p>Wenn Sie den App-V-Server nicht verwenden, überspringen Sie diesen Schritt, und fahren Sie mit dem nächsten Schritt fort.</p>
<div class="alert">
<strong>Hinweis:</strong><br/><p>Der APP-v 5,0 SP3-Client ist mit dem App-v 5,0 SP1-Server kompatibel.</p>
</div>
<div>

</div></td>
<td align="left"><p>Führen Sie folgende Schritte aus: </p>
<ol>
<li><p>Lesen Sie die <a href="release-notes-for-app-v-50-sp3.md" data-raw-source="[Release Notes for App-V 5.0 SP3](release-notes-for-app-v-50-sp3.md)"> Versionshinweise für App-v 5,0 SP3 </a> für Probleme, die sich auf die Installation des App-v-Servers auswirken können.</p></li>
<li><p>Führen Sie eine der folgenden Aktionen aus, je nachdem, welche Methode Sie verwenden, um die Verwaltungsdatenbank und/oder die Berichtsdatenbank zu aktualisieren:</p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Daten Bank Aktualisierungsmethode</th>
<th align="left">Schritt</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows Installer</p></td>
<td align="left"><p>Überspringen Sie diesen Schritt, und wechseln Sie zu Schritt 3, "Wenn Sie den App-V-Server aktualisieren..."</p></td>
</tr>
<tr class="even">
<td align="left"><p>SQL-Skripts</p></td>
<td align="left"><table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Verwaltungsdatenbank</strong></p></td>
<td align="left"><p>Informationen zum Installieren oder Aktualisieren finden Sie unter <a href="https://support.microsoft.com/kb/3031340" data-raw-source="[SQL scripts to install or upgrade the App-V 5.0 SP3 Management Server database fail](https://support.microsoft.com/kb/3031340)"> SQL-Skripts zum Installieren oder Aktualisieren der App-V 5,0 SP3-Verwaltungs Server-Datenbank Fehler </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Berichtsdatenbank</strong></p></td>
<td align="left"><p>Führen Sie die Schritte unter <a href="how-to-deploy-the-app-v-databases-by-using-sql-scripts.md" data-raw-source="[How to Deploy the App-V Databases by Using SQL Scripts](how-to-deploy-the-app-v-databases-by-using-sql-scripts.md)"> Vorgehensweise zum Bereitstellen der App-V-Datenbanken mithilfe von SQL-Skripts aus </a> .</p></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
</tbody>
</table>
<p> </p></li>
<li><p>Wenn Sie den App-v-Server vom APP-v 5,0 SP1-Hotfix-Paket 3 oder höher aktualisieren, führen Sie die Schritte in Abschnitt <a href="#bkmk-check-reg-key-svr" data-raw-source="[Check registry keys after installing the App-V 5.0 SP3 Server](#bkmk-check-reg-key-svr)"> Überprüfen der Registrierungsschlüssel nach der Installation des App-v 5,0 SP3-Servers aus </a> .</p></li>
<li><p>Führen Sie die Schritte unter <a href="how-to-deploy-the-app-v-50-server-50sp3.md" data-raw-source="[How to Deploy the App-V 5.0 Server](how-to-deploy-the-app-v-50-server-50sp3.md)"> Bereitstellen des App-V 5,0-Servers aus </a> .</p></li>
</ol></td>
</tr>
<tr class="even">
<td align="left"><p>Schritt 2: Aktualisieren Sie den App-V-Sequenzer.</p></td>
<td align="left"><p>Weitere Informationen finden Sie unter <a href="how-to-install-the-sequencer-beta-gb18030.md" data-raw-source="[How to Install the Sequencer](how-to-install-the-sequencer-beta-gb18030.md)"> Installieren des Sequencers </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Schritt 3: Aktualisieren Sie den App-v-Client oder den App-v-RDS-Client.</p></td>
<td align="left"><p>Weitere Informationen finden Sie unter <a href="how-to-deploy-the-app-v-client-gb18030.md" data-raw-source="[How to Deploy the App-V Client](how-to-deploy-the-app-v-client-gb18030.md)"> Bereitstellen des App-V-Clients </a> .</p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-check-reg-key-svr"></a>Überprüfen der Registrierungsschlüssel vor der Installation des App-V 5,0 SP3-Servers

Dies ist Schritt 3 aus der vorhergehenden Tabelle.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Wenn dieser Schritt erforderlich ist</strong></p></td>
<td align="left"><p>Sie Aktualisieren von App-V SP1 mit allen nachfolgenden Hotfix-Paketen, die Sie mithilfe einer MSP-Datei installiert haben.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Für welche Komponenten muss dieser Schritt ausgeführt werden?</strong></p></td>
<td align="left"><p>Nur die App-V Server-Komponenten, die Sie aktualisieren.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Wenn Sie diesen Schritt ausführen müssen</strong></p></td>
<td align="left"><p>Vor dem Upgrade des App-v-Servers auf App-v 5,0 SP3</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Was Sie tun müssen</strong></p></td>
<td align="left"><p>Aktualisieren Sie anhand der Informationen in den folgenden Tabellen jeden Registrierungsschlüsselwert unter <code>HKLM\Software\Microsoft\AppV\Server</code> mit dem Wert, den Sie in der ursprünglichen Server Installation angegeben haben. Durch das Abschließen dieses Schritts werden Registrierungswerte wiederhergestellt, die möglicherweise entfernt wurden, als App-V SP1-Hotfix-Pakete installiert wurden.</p></td>
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



## <a href="" id="bkmk-update-schema-cg"></a>Die XML-Datei für eine manuell erstellte Verbindungsgruppe erfordert ein Update auf ein Schema


Wenn Sie die Verbindungsgruppen-XML-Datei manuell erstellen und die neuen Features "optionale Pakete" und "Verwenden einer beliebigen Version" verwenden möchten, die unter [Verbesserungen der Verbindungsgruppen](#bkmk-cg-improvements)beschrieben werden, müssen Sie das folgende Schema in der XML-Datei angeben:

`xmlns="http://schemas.microsoft.com/appv/2014/virtualapplicationconnectiongroup"`

Beispiele und weitere Informationen finden Sie unter Informationen zur [Verbindungsgruppen Datei](about-the-connection-group-file.md).

## <a href="" id="bkmk-cg-improvements"></a>Verbesserungen an Verbindungsgruppen


Sie können Verbindungsgruppen einfacher verwalten, indem Sie optionale Pakete und andere Verbesserungen verwenden, die in App-V 5,0 SP3 hinzugefügt wurden. In der folgenden Tabelle werden die Aufgaben zusammengefasst, die Sie mithilfe der neuen Verbindungsgruppen Features ausführen können, sowie Links zu ausführlicheren Informationen zu den einzelnen Aufgaben.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Aufgabe/Funktion</th>
<th align="left">Beschreibung</th>
<th align="left">Links zu weiteren Informationen</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Aktivieren einer Verbindungsgruppe zum einbeziehen Optionaler Pakete</p></td>
<td align="left"><p>Durch die Verwendung optionaler Pakete in einer Verbindungsgruppe können Sie anhand der Anwendungen, auf die Benutzer Anspruch haben, dynamisch ermitteln, welche Anwendungen in der virtuellen Umgebung der Verbindungsgruppe enthalten sein sollen.</p>
<p>Sie müssen nicht so viele Verbindungsgruppen verwalten, da Sie optionale und nicht optionale Pakete in derselben Verbindungsgruppe kombinieren können. Durch das Mischen von Paketen können verschiedene Benutzergruppen dieselbe Verbindungsgruppe verwenden, auch wenn die Benutzer möglicherweise nur ein Paket gemeinsam haben.</p>
<p><strong>Beispiel </strong> : Sie können ein Paket mit Microsoft Office für alle Benutzer aktivieren, aber verschiedene optionale Pakete, die unterschiedliche Office-Plug-ins enthalten, für verschiedene Teilmengen von Benutzern aktivieren.</p></td>
<td align="left"><p><a href="how-to-use-optional-packages-in-connection-groups.md#bkmk-apps-plugs-optional" data-raw-source="[How to Use Optional Packages in Connection Groups](how-to-use-optional-packages-in-connection-groups.md#bkmk-apps-plugs-optional)">So verwenden Sie optionale Pakete in Verbindungsgruppen</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Aufheben der Veröffentlichung oder Löschen eines optionalen Pakets, ohne die Verbindungsgruppe zu ändern</p></td>
<td align="left"><p>Aufheben der Veröffentlichung oder Löschung oder Aufheben der Veröffentlichung und erneuten Veröffentlichung eines optionalen Pakets, das sich in einer Verbindungsgruppe befindet, ohne die Verbindungsgruppe auf dem App-V-Client deaktivieren oder erneut aktivieren zu müssen.</p></td>
<td align="left"><p><a href="how-to-use-optional-packages-in-connection-groups.md#bkmk-apps-plugs-optional" data-raw-source="[How to Use Optional Packages in Connection Groups](how-to-use-optional-packages-in-connection-groups.md#bkmk-apps-plugs-optional)">So verwenden Sie optionale Pakete in Verbindungsgruppen</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Veröffentlichen von Verbindungsgruppen, die von Benutzern veröffentlichte und Global veröffentlichte Pakete enthalten</p></td>
<td align="left"><p>Erstellen einer vom Benutzer veröffentlichten Verbindungsgruppe, die von Benutzern veröffentlichte und Global veröffentlichte Pakete enthält</p></td>
<td align="left"><p><a href="how-to-create-a-connection-group-with-user-published-and-globally-published-packages.md" data-raw-source="[How to Create a Connection Group with User-Published and Globally Published Packages](how-to-create-a-connection-group-with-user-published-and-globally-published-packages.md)">So erstellen Sie eine Verbindungsgruppe mit von Benutzern und global veröffentlichten Paketen</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Veranlassen, dass eine Verbindungsgruppe die Paketversion ignoriert</p></td>
<td align="left"><p>Konfigurieren Sie eine Verbindungsgruppe, um eine beliebige Version eines Pakets zu akzeptieren, mit der Sie ein Paket aktualisieren können, ohne die Verbindungsgruppe deaktivieren zu müssen. Wenn ein optionales Paket mit einer falschen Version in der Verbindungsgruppe vorhanden ist, wird das Paket ignoriert und verhindert, dass die virtuelle Umgebung der Verbindungsgruppe nicht erstellt wird.</p></td>
<td align="left"><p><a href="how-to-make-a-connection-group-ignore-the-package-version.md" data-raw-source="[How to Make a Connection Group Ignore the Package Version](how-to-make-a-connection-group-ignore-the-package-version.md)">So stellen Sie sicher, dass eine Verbindungsgruppe die Paketversion ignoriert</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Einschränken der Veröffentlichungsfunktionen von Endbenutzern</p></td>
<td align="left"><p>Aktivieren Sie nur Administratoren (nicht Endbenutzer), um Pakete zu veröffentlichen und Verbindungsgruppen zu aktivieren.</p></td>
<td align="left"><p>Informationen zu Verbindungsgruppen finden Sie unter <a href="how-to-allow-only-administrators-to-enable-connection-groups.md" data-raw-source="[How to Allow Only Administrators to Enable Connection Groups](how-to-allow-only-administrators-to-enable-connection-groups.md)"> so wird es gemacht: zulassen, dass nur Administratoren Verbindungsgruppen aktivieren</a></p>
<p>Informationen zu Paketen finden Sie in den folgenden Artikeln:</p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Methode</th>
<th align="left">Link zu weiteren Informationen</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Verwaltungskonsole</p></td>
<td align="left"><p><a href="how-to-publish-a-package-by-using-the-management-console-50.md" data-raw-source="[How to Publish a Package by Using the Management Console](how-to-publish-a-package-by-using-the-management-console-50.md)">So veröffentlichen Sie mithilfe der Verwaltungskonsole ein Paket</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>PowerShell</p></td>
<td align="left"><p><a href="how-to-manage-connection-groups-on-a-stand-alone-computer-by-using-powershell.md#bkmk-admin-only-posh-topic-cg" data-raw-source="[How to Manage Connection Groups on a Stand-alone Computer by Using PowerShell](how-to-manage-connection-groups-on-a-stand-alone-computer-by-using-powershell.md#bkmk-admin-only-posh-topic-cg)">So verwalten Sie Verbindungsgruppen auf einem eigenständigen Computer mithilfe von PowerShell</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Elektronisches Software-Delivery-System von Drittanbietern</p></td>
<td align="left"><p><a href="how-to-enable-only-administrators-to-publish-packages-by-using-an-esd.md" data-raw-source="[How to Enable Only Administrators to Publish Packages by Using an ESD](how-to-enable-only-administrators-to-publish-packages-by-using-an-esd.md)">So schränken Sie die Veröffentlichung von Paketen mithilfe einer ESD auf Administratoren ein</a></p></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
<tr class="even">
<td align="left"><p>Aktivieren oder Deaktivieren einer Verbindungsgruppe für einen bestimmten Benutzer</p></td>
<td align="left"><p>Administratoren können eine Verbindungsgruppe für einen bestimmten Benutzer aktivieren oder deaktivieren, indem Sie den optionalen <strong> -User- </strong> Parameter mit den folgenden Cmdlets verwenden:</p>
<ul>
<li><p>Enable-AppVClientConnectionGroup</p></li>
<li><p>Deaktivieren-AppVClientConnectionGroup</p></li>
</ul></td>
<td align="left"><p><a href="how-to-manage-connection-groups-on-a-stand-alone-computer-by-using-powershell.md#bkmk-enable-cg-for-user-poshtopic" data-raw-source="[How to Manage Connection Groups on a Stand-alone Computer by Using PowerShell](how-to-manage-connection-groups-on-a-stand-alone-computer-by-using-powershell.md#bkmk-enable-cg-for-user-poshtopic)">So verwalten Sie Verbindungsgruppen auf einem eigenständigen Computer mithilfe von PowerShell</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Zusammenführen identischer Paket Pfade zu einem virtuellen Verzeichnis in Verbindungsgruppen</p></td>
<td align="left"><p>Wenn zwei oder mehr Pakete in einer Verbindungsgruppe identische Verzeichnispfade enthalten, werden die Pfade in einem einzigen virtuellen Verzeichnis innerhalb der virtuellen Umgebung der Verbindungsgruppe zusammengeführt.</p>
<p>Dieses Zusammenführen von Pfaden ermöglicht es einer Anwendung in einem Paket, auf Dateien zuzugreifen, die in einem anderen Paket enthalten sind.</p></td>
<td align="left"><p><a href="about-the-connection-group-virtual-environment.md#bkmk-merged-root-ve-exp" data-raw-source="[About the Connection Group Virtual Environment](about-the-connection-group-virtual-environment.md#bkmk-merged-root-ve-exp)">Über die virtuelle Verbindungsgruppenumgebung</a></p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-usersid-pub-pkgs-specf-user"></a>Administratoren können Pakete für einen bestimmten Benutzer veröffentlichen und deren Veröffentlichung aufheben.


Administratoren können mithilfe der folgenden Cmdlets Pakete für einen bestimmten Benutzer veröffentlichen oder deren Veröffentlichung aufheben. Um die Cmdlets zu verwenden, geben Sie den **-User-ID-** Parameter und dann die Sicherheits-ID (SID) des Benutzers ein. Weitere Informationen finden Sie unter:

-   [So verwalten Sie App-V 5.0-Pakete auf einem eigenständigen Computer mithilfe von PowerShell](how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md#bkmk-pub-pkg-a-user-standalone-posh)

-   [So verwalten Sie App-V 5.0-Pakete auf einem eigenständigen Computer mithilfe von PowerShell](how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md#bkmk-unpub-pkg-specfc-use)

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Cmdlet</th>
<th align="left">Beispiele</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Publish-AppvClientPackage</p></td>
<td align="left"><p>Publish-AppvClientPackage "ContosoApplication"-Benutzer-e-1-2-34-56789012-3456789012-345678901-2345</p></td>
</tr>
<tr class="even">
<td align="left"><p>Veröffentlichung aufheben – AppvClientPackage</p></td>
<td align="left"><p>UNPUBLISH-AppvClientPackage "ContosoApplication"-Benutzer-e-1-2-34-56789012-3456789012-345678901-2345</p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-admins-only-pub-unpub-pkgs"></a>Nur Administratoren das Veröffentlichen und Aufheben der Veröffentlichung von Paketen ermöglichen


Mit einer der folgenden Methoden können Sie nur Administratoren (nicht Endbenutzern) das Veröffentlichen und Aufheben der Veröffentlichung von Paketen ermöglichen:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Methode</th>
<th align="left">Weitere Informationen</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Gruppenrichtlinieneinstellung</p></td>
<td align="left"><p>Navigieren Sie zum folgenden Gruppenrichtlinien-Objektknoten:</p>
<p><strong>Computerkonfigurations &gt; Richtlinien &gt; Administrative Vorlagen &gt; System &gt; App-V &gt; Publishing </strong> .</p>
<p>Aktivieren Sie die <strong> </strong> Gruppenrichtlinieneinstellung Veröffentlichung als Administrator anfordern.</p></td>
</tr>
<tr class="even">
<td align="left"><p>PowerShell</p></td>
<td align="left"><p><a href="how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md#bkmk-admins-pub-pkgs" data-raw-source="[How to Manage App-V 5.0 Packages Running on a Stand-Alone Computer by Using PowerShell](how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md#bkmk-admins-pub-pkgs)">So verwalten Sie App-V 5.0-Pakete auf einem eigenständigen Computer mithilfe von PowerShell</a></p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-runvirtual-reg-key"></a>RunVirtual-Registrierungsschlüssel unterstützt Pakete, die für den Benutzer veröffentlicht werden


App-V 5,0 SP3 bietet Unterstützung für die Verwendung des **RunVirtual** -Registrierungsschlüssels mit virtualisierten Anwendungen, die in vom Benutzer veröffentlichten Paketen enthalten sind. Mit dem Registrierungsschlüssel **RunVirtual** können Sie eine lokal installierte Anwendung in einer virtuellen Umgebung sowie Anwendungen ausführen, die mithilfe von App-V virtualisiert wurden.

Zuvor mussten die virtualisierten Anwendungen in App-V-Paketen Global veröffentlicht werden. Weitere Informationen zu **RunVirtual** und zu anderen Methoden zum Ausführen lokal installierter Anwendungen in einer virtuellen Umgebung mit virtualisierten Anwendungen finden Sie unter [Ausführen einer lokal installierten Anwendung in einer virtuellen Umgebung mit virtualisierten Anwendungen](running-a-locally-installed-application-inside-a-virtual-environment-with-virtualized-applications.md).

## <a href="" id="bkmk-posh-cmdlets-help"></a>Neue PowerShell-Cmdlets und Hilfe zu aktualisierbaren Cmdlets


Neue PowerShell-Cmdlets und Hilfe zu aktualisierbaren Cmdlets sind in App-V 5,0 SP3 enthalten. Informationen zum Herunterladen der Cmdlet-Module finden Sie unter [Laden der PowerShell-Cmdlets und Abrufen der Cmdlet-Hilfe](how-to-load-the-powershell-cmdlets-and-get-cmdlet-help-50-sp3.md#bkmk-load-cmdlets).

### Neue App-V 5,0 SP3-Cmdlets für Server-PowerShell

Neue Windows PowerShell-Cmdlets für den App-V-Server wurden hinzugefügt, um Sie beim Verwalten von Verbindungsgruppen zu unterstützen.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Cmdlet</th>
<th align="left">Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Add-AppvServerConnectionGroupPackage</p></td>
<td align="left"><p>Fügt ein Paket an das Ende einer Verbindungsgruppe&#39;s-Paketliste an und ermöglicht Ihnen, das Paket als optional und/oder ohne Version innerhalb der Verbindungsgruppe zu konfigurieren.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Satz-AppvServerConnectionGroupPackage</p></td>
<td align="left"><p>Ermöglicht es Ihnen, Details zum Verbindungsgruppen Paket zu bearbeiten, beispielsweise, ob es optional ist.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Remove-AppvServerConnectionGroupPackage</p></td>
<td align="left"><p>Entfernt ein Paket aus einer Verbindungsgruppe.</p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-get-cmdlet-help"></a>Aufrufen von Hilfe zu den PowerShell-Cmdlets

Die Hilfe zu einem Cmdlet steht in den folgenden Formaten zur Verfügung:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Format</th>
<th align="left">Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Als herunterladbares Modul</p></td>
<td align="left"><p>So erhalten Sie die neueste Hilfe nach dem Herunterladen des Cmdlet-Moduls:</p>
<ol>
<li><p>Öffnen Sie Windows PowerShell oder Windows PowerShell Integrated Scripting Environment (ISE).</p></li>
<li><p>Geben Sie einen der folgenden Befehle ein, um die Cmdlets für das gewünschte Modul zu laden:</p></li>
</ol>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">App-V-Komponente</th>
<th align="left">Befehl zum eingeben</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>App-V-Server</p></td>
<td align="left"><p>Update-Hilfe-Modul AppvServer</p></td>
</tr>
<tr class="even">
<td align="left"><p>App-V-Sequenzer</p></td>
<td align="left"><p>Update-Hilfe-Modul AppvSequencer</p></td>
</tr>
<tr class="odd">
<td align="left"><p>App-V-Client</p></td>
<td align="left"><p>Update-Hilfe-Modul AppvClient</p></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
<tr class="even">
<td align="left"><p>Auf TechNet als Web-Seiten</p></td>
<td align="left"><p>Weitere Informationen finden Sie unter App-V-Knoten unter <a href="https://technet.microsoft.com/library/dn520245.aspx" data-raw-source="[Microsoft Desktop Optimization Pack Automation with Windows PowerShell](https://technet.microsoft.com/library/dn520245.aspx)"> Microsoft Desktop Optimization Pack-Automatisierung mit Windows PowerShell </a> .</p></td>
</tr>
</tbody>
</table>



Weitere Informationen finden Sie unter [Laden der PowerShell-Cmdlets und Abrufen der Cmdlet-Hilfe](how-to-load-the-powershell-cmdlets-and-get-cmdlet-help-50-sp3.md).

## <a href="" id="bkmk-pvad-hidden"></a>Primäres virtuelles Anwendungsverzeichnis (PVAD) ist ausgeblendet, kann aber aktiviert werden


Das primäre Virtual Application Directory (PVAD) ist in App-V 5,0 SP3 ausgeblendet, Sie können es aber wieder aktivieren und mit einer der folgenden Methoden sichtbar machen:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Methode</th>
<th align="left">Schritte</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Verwenden eines Befehlszeilenparameters</p></td>
<td align="left"><p>Übergeben <strong> Sie den Parameter – EnablePVADControl </strong> an den <strong>Sequencer.exe</strong> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Erstellen eines Registrierungsunterschlüssels</p></td>
<td align="left"><ol>
<li><p>Navigieren Sie im Registrierungs-Editor zu: <code>HKLM\SOFTWARE\Microsoft\AppV\Sequencer\Compatibility</code></p>
<div class="alert">
<strong>Hinweis:</strong><br/><p>Wenn der unter <code>Compatibility</code> Schlüssel nicht vorhanden ist, müssen Sie ihn erstellen.</p>
</div>
<div>

</div></li>
<li><p>Erstellen Sie einen DWORD-Wert mit dem Namen <strong> EnablePVADControl </strong> , und legen Sie den Wert auf <strong> 1 </strong> .</p>
<p>Der Wert <strong> 0 </strong> bedeutet, dass PVAD ausgeblendet ist.</p></li>
</ol></td>
</tr>
</tbody>
</table>



**Weitere Informationen zu PVAD:** Wenn Sie zum Erstellen eines Pakets den Sequencer verwenden, können Sie einen beliebigen Installationspfad für das Paket eingeben. In früheren Versionen von App-V mussten Sie das primäre Virtual Application Directory (PVAD) der Anwendung als Pfad angeben. PVAD ist das Verzeichnis, in dem Sie normalerweise eine Anwendung auf Ihrem lokalen Computer installieren würden, wenn Sie App-V nicht verwendet haben. Wenn Sie beispielsweise Office auf einem Computer installiert haben, wäre das PVAD in der Regel c:\\Programme c:\\Programme\\Microsoft Office\\.

## <a href="" id="bkmk-pub-metadata-clientversion"></a>Clientversion ist erforderlich, um die App-V-Veröffentlichungsmetadaten anzuzeigen.


In App-v 5,0 SP3 müssen Sie die folgenden Werte in der Adresse angeben, wenn Sie den App-v-Veröffentlichungsserver nach Metadaten Abfragen:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Wert</th>
<th align="left">Zusätzliche Details</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>ClientVersion</strong></p></td>
<td align="left"><p>Wenn Sie den <strong> Clientversion </strong> -Parameter aus der Abfrage weglassen, schließen die Metadaten die neuen App-V 5,0 SP3-Features aus.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Kunden</strong></p></td>
<td align="left"><p>Sie müssen diesen Wert nur angeben, wenn Sie beim Sequenzieren des Pakets bestimmte Clientbetriebssysteme auswählen. Wenn Sie die Standardeinstellung (alle Betriebssysteme) auswählen, geben Sie diesen Wert in der Abfrage nicht an.</p>
<p>Wenn Sie den <strong> Client </strong> -Parameter aus der Abfrage weglassen, werden nur die Pakete, die für die Unterstützung eines beliebigen Betriebssystems sequenziert wurden, in den Metadaten angezeigt.</p></td>
</tr>
</tbody>
</table>



Syntax und Beispiele für diese Abfrage finden Sie unter [Anzeigen von App-V Server-Veröffentlichungsmetadaten](viewing-app-v-server-publishing-metadata.md).

## <a href="" id="bkmk-event-logs-moved"></a>App-V-Ereignisprotokolle wurden konsolidiert


Die folgenden Ereignisprotokolle, die sich zuvor bei **Applications and Services Logs/Microsoft/AppV/ &lt; App-V &gt; -Komponenten**befanden, wurden in **Anwendungen und Dienstprotokolle/Microsoft/AppV/ServiceLog**verschoben.

Wenn Sie die Protokolle anzeigen möchten **, wählen Sie** &gt; in der Ereignisanzeige Anwendung die Option **Analyse-und Debug-Protokolle** anzeigen aus.

Client-catalog Client-Integration Client-Orchestrierungs Client-PackageConfig Client-Scripting Client-Service Client-Vemgr Client-VFSC FilesystemMetadataLibrary ManifestLibrary PolicyLibrary-Subsysteme-ActiveX-Subsysteme-AppPath-Subsystem-com-Subsysteme-FTA

## So erhalten Sie MDOP-Technologien


App-V ist Teil des Microsoft Desktop Optimization Pack (MDOP). MDOP ist Teil von Microsoft Software Assurance. Weitere Informationen zur Microsoft-Software Assurance und zum Erwerb von MDOP finden Sie unter [wie erhalte ich MDOP](https://go.microsoft.com/fwlink/?LinkId=322049).






## Verwandte Themen


[Versionshinweise für App-V 5.0 SP3](release-notes-for-app-v-50-sp3.md)









