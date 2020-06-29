---
title: Voraussetzungen für App-V 5.1
description: Voraussetzungen für App-V 5.1
author: dansimp
ms.assetid: 1bfa03c1-a4ae-45ec-8a2b-b10c2b94bfb0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 24a74d8f8d7148cdb6c32bcafa87f479d24305af
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805954"
---
# Voraussetzungen für App-V 5.1


Bevor Sie Microsoft Application Virtualization (App-V) 5,1 installieren, stellen Sie sicher, dass Sie alle der folgenden erforderlichen Software installiert haben.

Eine Liste der unterstützten Betriebssysteme und Hardwareanforderungen für App-v Server, Sequencer und Client finden Sie unter [unterstützte App-v 5,1-Konfigurationen](app-v-51-supported-configurations.md).

## Zusammenfassung der Software, die auf jedem Betriebssystem vorinstalliert ist


Die folgende Tabelle zeigt die Software, die bereits für unterschiedliche Betriebssysteme installiert ist.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Betriebssystem</th>
<th align="left">Beschreibung der Voraussetzungen</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows 10</p></td>
<td align="left"><p>Alle erforderliche Software ist bereits installiert.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows8.1</p></td>
<td align="left"><p>Alle erforderliche Software ist bereits installiert.</p>
<div class="alert">
<strong>Hinweis:</strong><br/><p>Wenn Sie Windows 8 ausführen, aktualisieren Sie auf Windows 8,1, bevor Sie App-V 5,1 verwenden.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server 2012</p></td>
<td align="left"><p>Die folgende erforderliche Software ist bereits installiert:</p>
<ul>
<li><p>Microsoft .NET Framework 4,5</p></li>
<li><p>Windows PowerShell 3,0</p>
<div class="alert">
<strong>Hinweis:</strong><br/><p>Für die Installation von PowerShell 3,0 ist ein Neustart erforderlich.</p>
</div>
<div>

</div></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Windows7</p></td>
<td align="left"><p>Die erforderliche Software ist noch nicht installiert. Sie müssen es installieren, bevor Sie App-V installieren können.</p></td>
</tr>
</tbody>
</table>



## App-V Server-Voraussetzungs Software


Installieren Sie die erforderliche erforderliche Software für die App-V 5,1-Server Komponenten.

### Was Sie wissen sollten, bevor Sie beginnen

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p>Konto für die Installation des App-V-Servers</p></td>
<td align="left"><p>Das Konto, das Sie zum Installieren der App-V Server-Komponenten verwenden, muss Folgendes aufweisen:</p>
<ul>
<li><p>Administratorrechte auf dem Computer, auf dem Sie die Komponenten installieren.</p></li>
<li><p>Die Möglichkeit, Active Directory-Domänendienste abzufragen.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Port und Firewall</p></td>
<td align="left"><ul>
<li><p>Geben Sie einen Port an, in dem die einzelnen Komponenten gehostet werden.</p></li>
<li><p>Fügen Sie die zugehörigen Firewallregeln hinzu, um eingehende Anforderungen an die angegebenen Ports zu ermöglichen.</p></li>
</ul>
<p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>WebDAV (Web Distributed Authoring and Versioning)</p></td>
<td align="left"><p>WebDAV wird für den Verwaltungsdienst automatisch deaktiviert.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Unterstützte Bereitstellungsszenarien</p></td>
<td align="left"><ul>
<li><p>Eine eigenständige Bereitstellung, in der alle Komponenten auf demselben Server bereitgestellt werden.</p></li>
<li><p>Eine verteilte Bereitstellung.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>Nicht unterstützte Bereitstellungsszenarien</p></td>
<td align="left"><ul>
<li><p>Installieren von nebeneinander angeordneten Instanzen mehrerer App-V-Server Versionen auf demselben Server.</p></li>
<li><p>Installieren der App-V Server-Komponenten auf einem Computer, auf dem Server Core oder Domänencontroller ausgeführt wird</p></li>
</ul></td>
</tr>
</tbody>
</table>



### Verwaltungsserver-Voraussetzungs Software

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Voraussetzungen und erforderliche Einstellungen</th>
<th align="left">Details</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Unterstützte Version von SQL Server</p></td>
<td align="left"><p>Unterstützte Versionen finden Sie unter <a href="app-v-51-supported-configurations.md" data-raw-source="[App-V 5.1 Supported Configurations](app-v-51-supported-configurations.md)"> unterstützte App-V 5,1-Konfigurationen </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="https://www.microsoft.com//download/details.aspx?id=40773" data-raw-source="[Microsoft .NET Framework 4.5.1 (Web Installer)](https://www.microsoft.com//download/details.aspx?id=40773)">Microsoft .NET Framework 4.5.1 (Web Installer)</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=34595" data-raw-source="[Windows PowerShell 3.0](https://www.microsoft.com/download/details.aspx?id=34595)">Windows PowerShell 3,0</a></p></td>
<td align="left"><p>Für die Installation von PowerShell 3,0 ist ein Neustart erforderlich.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Herunterladen und Installieren von <a href="https://support.microsoft.com/kb/2533623" data-raw-source="[KB2533623](https://support.microsoft.com/kb/2533623)"> KB2533623</a></p></td>
<td align="left"><p>Gilt nur für Windows 7.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=40784" data-raw-source="[Visual C++ Redistributable Packages for Visual Studio 2013](https://www.microsoft.com/download/details.aspx?id=40784)">Visual C++-verteilbare Pakete für Visual Studio 2013</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>64-Bit ASP.net-Registrierung</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Rolle des Windows Server-Webservers</p></td>
<td align="left"><p>Diese Rolle muss einem Server Betriebssystem hinzugefügt werden, das für den Verwaltungsserver unterstützt wird.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Web Server (IIS)-Verwaltungs Tools</p></td>
<td align="left"><p>Klicken Sie auf <strong> IIS-Verwaltungsskripts und-Tools </strong> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Webserver-Rollendienste</p></td>
<td align="left"><p><strong>Allgemeine HTTP-Features:</strong></p>
<ul>
<li><p>Statischer Inhalt</p></li>
<li><p>Standarddokument</p></li>
</ul>
<p><strong>Anwendungsentwicklung:</strong></p>
<ul>
<li><p>ASP.NET</p></li>
<li><p>.NET-Erweiterbarkeit</p></li>
<li><p>ISAPI-Erweiterungen</p></li>
<li><p>ISAPI-Filter</p></li>
</ul>
<p><strong>Sicherheits</strong></p>
<ul>
<li><p>Windows-Authentifizierung</p></li>
<li><p>Anforderungsfilterung</p></li>
</ul>
<p><strong>Verwaltungs Tools:</strong></p>
<ul>
<li><p>IIS-Verwaltungskonsole</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Standard Installationsspeicherort</p></td>
<td align="left"><p>%ProgramFiles%\Microsoft Application Virtualization Server</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Speicherort der Verwaltungsdatenbank</p></td>
<td align="left"><p>SQL Server-Datenbankname, Name der SQL Server-Datenbankinstanz und Datenbankname</p></td>
</tr>
<tr class="even">
<td align="left"><p>Verwaltungskonsolen-und Verwaltungsdaten Bank Berechtigungen</p></td>
<td align="left"><p>Ein Benutzer oder eine Gruppe, die nach Abschluss der Bereitstellung auf die Verwaltungskonsole und die Datenbank zugreifen kann. Nur diese Benutzer oder Gruppen haben Zugriff auf die Verwaltungskonsole und die Datenbank, es sei denn, mithilfe der Verwaltungskonsole werden zusätzliche Administratoren hinzugefügt.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Name der Verwaltungsdienst Website</p></td>
<td align="left"><p>Name für die Verwaltungskonsole-Website.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Portbindung des Verwaltungsdiensts</p></td>
<td align="left"><p>Eindeutige Portnummer für den Verwaltungsdienst Dieser Port kann nicht von einem anderen Prozess auf dem Computer verwendet werden.</p></td>
</tr>
</tbody>
</table>



**Wichtig**  
JavaScript muss im Browser aktiviert sein, über den die Webverwaltungs Konsole geöffnet wird.



### Erforderliche Software für die Verwaltungsserver-Datenbank

Die Verwaltungsdatenbank ist nur erforderlich, wenn Sie den App-V 5,1-Verwaltungsserver verwenden.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Voraussetzungen und erforderliche Einstellungen</th>
<th align="left">Details</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="https://www.microsoft.com//download/details.aspx?id=40773" data-raw-source="[Microsoft .NET Framework 4.5.1 (Web Installer)](https://www.microsoft.com//download/details.aspx?id=40773)">Microsoft .NET Framework 4.5.1 (Web Installer)</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=40784" data-raw-source="[Visual C++ Redistributable Packages for Visual Studio 2013](https://www.microsoft.com/download/details.aspx?id=40784)">Visual C++-verteilbare Pakete für Visual Studio 2013</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Standard Installationsspeicherort</p></td>
<td align="left"><p>%ProgramFiles%\Microsoft Application Virtualization Server</p></td>
</tr>
<tr class="even">
<td align="left"><p>Benutzerdefinierter SQL Server-Instanzname (falls zutreffend)</p></td>
<td align="left"><p>Zu verwendender Format: <strong> instanceName</strong></p>
<p>Dieses Format basiert auf der Annahme, dass sich die Installation auf dem lokalen Computer befindet.</p>
<p>Wenn Sie den Namen mit dem Format <strong> SVR\INSTANCE angeben </strong> , schlägt die Installation fehl.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Benutzerdefinierter Datenbankname (falls zutreffend)</p></td>
<td align="left"><p>Eindeutiger Datenbankname</p>
<p>Standard: AppVManagement</p></td>
</tr>
<tr class="even">
<td align="left"><p>Verwaltungsserver Standort</p></td>
<td align="left"><p>Computerkonto, auf dem der Verwaltungsserver bereitgestellt wird.</p>
<p>Zu verwendender Format: Domain\MachineAccount</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Verwaltungsserver-Installations Administrator</p></td>
<td align="left"><p>Konto, das zum Installieren des Verwaltungsservers verwendet wird.</p>
<p>Zu verwendender Format: Domain\AdministratorLoginName</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft SQL Server-Dienst-Agent</p></td>
<td align="left"><p>Konfigurieren Sie den Verwaltungsdaten Bank Computer so, dass der Microsoft SQL Server-Agent-Dienst automatisch neu gestartet wird. Anweisungen hierzu finden Sie unter <a href="https://technet.microsoft.com/magazine/gg313742.aspx" data-raw-source="[Configure SQL Server Agent to Restart Services Automatically](https://technet.microsoft.com/magazine/gg313742.aspx)"> Konfigurieren des SQL Server-Agents, um Dienste automatisch neu zu starten </a> .</p></td>
</tr>
</tbody>
</table>



### Erforderliche Software für Veröffentlichungsserver

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Voraussetzungen und erforderliche Einstellungen</th>
<th align="left">Details</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="https://www.microsoft.com//download/details.aspx?id=40773" data-raw-source="[Microsoft .NET Framework 4.5.1 (Web Installer)](https://www.microsoft.com//download/details.aspx?id=40773)">Microsoft .NET Framework 4.5.1 (Web Installer)</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=40784" data-raw-source="[Visual C++ Redistributable Packages for Visual Studio 2013](https://www.microsoft.com/download/details.aspx?id=40784)">Visual C++-verteilbare Pakete für Visual Studio 2013</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>64-Bit ASP.net-Registrierung</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Rolle des Windows Server-Webservers</p></td>
<td align="left"><p>Diese Rolle muss einem Server Betriebssystem hinzugefügt werden, das für den Verwaltungsserver unterstützt wird.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Web Server (IIS)-Verwaltungs Tools</p></td>
<td align="left"><p>Klicken Sie auf <strong> IIS-Verwaltungsskripts und-Tools </strong> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Webserver-Rollendienste</p></td>
<td align="left"><p><strong>Allgemeine HTTP-Features:</strong></p>
<ul>
<li><p>Statischer Inhalt</p></li>
<li><p>Standarddokument</p></li>
</ul>
<p><strong>Anwendungsentwicklung:</strong></p>
<ul>
<li><p>ASP.NET</p></li>
<li><p>.NET-Erweiterbarkeit</p></li>
<li><p>ISAPI-Erweiterungen</p></li>
<li><p>ISAPI-Filter</p></li>
</ul>
<p><strong>Sicherheits</strong></p>
<ul>
<li><p>Windows-Authentifizierung</p></li>
<li><p>Anforderungsfilterung</p></li>
</ul>
<p><strong>Verwaltungs Tools:</strong></p>
<ul>
<li><p>IIS-Verwaltungskonsole</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>Standard Installationsspeicherort</p></td>
<td align="left"><p>%ProgramFiles%\Microsoft Application Virtualization Server</p></td>
</tr>
<tr class="even">
<td align="left"><p>Verwaltungsdienst-URL</p></td>
<td align="left"><p>Die URL des App-V-Verwaltungsdiensts. Hierbei handelt es sich um den Port, mit dem der Veröffentlichungsserver kommuniziert.</p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Installations Architektur</th>
<th align="left">Für die URL zu verwendende Format</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Verwaltungsserver und Veröffentlichungsserver sind auf demselben Server installiert</p></td>
<td align="left"><p><a href="http://localhost:12345" data-raw-source="http://localhost:12345">http://localhost:12345</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Verwaltungsserver und Veröffentlichungsserver werden auf unterschiedlichen Servern installiert</p></td>
<td align="left"><p><a href="http://MyAppvServer.MyDomain.com" data-raw-source="http://MyAppvServer.MyDomain.com">http://MyAppvServer.MyDomain.com</a></p></td>
</tr>
</tbody>
</table>
<p> </p>
<p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Name der Veröffentlichungsdienst Website</p></td>
<td align="left"><p>Name für die Veröffentlichungswebsite.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Portbindung des Publishing Diensts</p></td>
<td align="left"><p>Eindeutige Portnummer für den Veröffentlichungsdienst. Dieser Port kann nicht von einem anderen Prozess auf dem Computer verwendet werden.</p></td>
</tr>
</tbody>
</table>



### Berichtsserver-Voraussetzungs Software

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Voraussetzungen und erforderliche Einstellungen</th>
<th align="left">Details</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Unterstützte Version von SQL Server</p></td>
<td align="left"><p>Unterstützte Versionen finden Sie unter <a href="app-v-51-supported-configurations.md" data-raw-source="[App-V 5.1 Supported Configurations](app-v-51-supported-configurations.md)"> unterstützte App-V 5,1-Konfigurationen </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="https://www.microsoft.com//download/details.aspx?id=40773" data-raw-source="[Microsoft .NET Framework 4.5.1 (Web Installer)](https://www.microsoft.com//download/details.aspx?id=40773)">Microsoft .NET Framework 4.5.1 (Web Installer)</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=40784" data-raw-source="[Visual C++ Redistributable Packages for Visual Studio 2013](https://www.microsoft.com/download/details.aspx?id=40784)">Visual C++-verteilbare Pakete für Visual Studio 2013</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>64-Bit ASP.net-Registrierung</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Rolle des Windows Server-Webservers</p></td>
<td align="left"><p>Diese Rolle muss einem Server Betriebssystem hinzugefügt werden, das für den Verwaltungsserver unterstützt wird.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Web Server (IIS)-Verwaltungs Tools</p></td>
<td align="left"><p>Klicken Sie auf <strong> IIS-Verwaltungsskripts und-Tools </strong> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Webserver-Rollendienste</p></td>
<td align="left"><p>Um das Risiko von unerwünschten oder böswilligen Daten, die an den Berichtsserver gesendet werden, zu verringern, sollten Sie den Zugriff auf den Reporting Web Service pro Ihre Unternehmenssicherheitsrichtlinie einschränken.</p>
<p><strong>Allgemeine HTTP-Features:</strong></p>
<ul>
<li><p>Statischer Inhalt</p></li>
<li><p>Standarddokument</p></li>
</ul>
<p><strong>Anwendungsentwicklung:</strong></p>
<ul>
<li><p>ASP.NET</p></li>
<li><p>.NET-Erweiterbarkeit</p></li>
<li><p>ISAPI-Erweiterungen</p></li>
<li><p>ISAPI-Filter</p></li>
</ul>
<p><strong>Sicherheits</strong></p>
<ul>
<li><p>Windows-Authentifizierung</p></li>
<li><p>Anforderungsfilterung</p></li>
</ul>
<p><strong>Verwaltungs Tools:</strong></p>
<ul>
<li><p>IIS-Verwaltungskonsole</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Standard Installationsspeicherort</p></td>
<td align="left"><p>%ProgramFiles%\Microsoft Application Virtualization Server</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Name der Berichtsdienst Website</p></td>
<td align="left"><p>Name für die berichterstellungswebsite.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Portbindung des Reporting Services</p></td>
<td align="left"><p>Eindeutige Portnummer für den Berichterstellungsdienst. Dieser Port kann nicht von einem anderen Prozess auf dem Computer verwendet werden.</p></td>
</tr>
</tbody>
</table>



### Erforderliche Software für die Berichtsdatenbank

Die Berichtsdatenbank ist nur erforderlich, wenn Sie den App-V 5,1-Berichtsserver verwenden.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Voraussetzungen und erforderliche Einstellungen</th>
<th align="left">Details</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="https://www.microsoft.com//download/details.aspx?id=40773" data-raw-source="[Microsoft .NET Framework 4.5.1 (Web Installer)](https://www.microsoft.com//download/details.aspx?id=40773)">Microsoft .NET Framework 4.5.1 (Web Installer)</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=40784" data-raw-source="[Visual C++ Redistributable Packages for Visual Studio 2013](https://www.microsoft.com/download/details.aspx?id=40784)">Visual C++-verteilbare Pakete für Visual Studio 2013</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Standard Installationsspeicherort</p></td>
<td align="left"><p>%ProgramFiles%\Microsoft Application Virtualization Server</p></td>
</tr>
<tr class="even">
<td align="left"><p>Benutzerdefinierter SQL Server-Instanzname (falls zutreffend)</p></td>
<td align="left"><p>Zu verwendender Format: <strong> instanceName</strong></p>
<p>Dieses Format basiert auf der Annahme, dass sich die Installation auf dem lokalen Computer befindet.</p>
<p>Wenn Sie den Namen mit dem Format <strong> SVR\INSTANCE angeben </strong> , schlägt die Installation fehl.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Benutzerdefinierter Datenbankname (falls zutreffend)</p></td>
<td align="left"><p>Eindeutiger Datenbankname</p>
<p>Standard: AppVReporting</p></td>
</tr>
<tr class="even">
<td align="left"><p>Speicherort des Berichterstattungs Servers</p></td>
<td align="left"><p>Computerkonto, auf dem der Berichtsserver bereitgestellt wird.</p>
<p>Zu verwendender Format: Domain\MachineAccount</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Reporting Server-Installations Administrator</p></td>
<td align="left"><p>Konto, das zum Installieren des Berichtsservers verwendet wird.</p>
<p>Zu verwendender Format: Domain\AdministratorLoginName</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft SQL Server-Dienst und Microsoft SQL Server-Dienst-Agent</p></td>
<td align="left"><p>Konfigurieren Sie diese Dienste für die Zuordnung zu Benutzerkonten, die Zugriff auf die Abfrage von AD DS haben.</p></td>
</tr>
</tbody>
</table>



## App-V-Client-Voraussetzungs Software


Installieren Sie die folgende erforderliche Software für den App-V-Client.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Voraussetzung</th>
<th align="left">Details</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="https://www.microsoft.com//download/details.aspx?id=40773" data-raw-source="[Microsoft .NET Framework 4.5.1 (Web Installer)](https://www.microsoft.com//download/details.aspx?id=40773)">Microsoft .NET Framework 4.5.1 (Web Installer)</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=34595" data-raw-source="[Windows PowerShell 3.0](https://www.microsoft.com/download/details.aspx?id=34595)">Windows PowerShell 3,0</a></p>
<p></p></td>
<td align="left"><p>Für die Installation von PowerShell 3,0 ist ein Neustart erforderlich.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><a href="https://support.microsoft.com/kb/2533623" data-raw-source="[KB2533623](https://support.microsoft.com/kb/2533623)">KB2533623</a></p></td>
<td align="left"><p>Gilt nur für Windows 7: Laden Sie die KB herunter, und installieren Sie Sie.</p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=40784" data-raw-source="[Visual C++ Redistributable Packages for Visual Studio 2013](https://www.microsoft.com/download/details.aspx?id=40784)">Visual C++-verteilbare Pakete für Visual Studio 2013</a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



## Erforderliche Software für Remote Desktop Dienste-Client


Installieren Sie die folgende erforderliche Software für den App-V-Remote Desktop Dienste-Client.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Voraussetzung</th>
<th align="left">Details</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="https://www.microsoft.com//download/details.aspx?id=40773" data-raw-source="[Microsoft .NET Framework 4.5.1 (Web Installer)](https://www.microsoft.com//download/details.aspx?id=40773)">Microsoft .NET Framework 4.5.1 (Web Installer)</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=34595" data-raw-source="[Windows PowerShell 3.0](https://www.microsoft.com/download/details.aspx?id=34595)">Windows PowerShell 3,0</a></p>
<p></p></td>
<td align="left"><p>Für die Installation von PowerShell 3,0 ist ein Neustart erforderlich.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><a href="https://support.microsoft.com/kb/2533623" data-raw-source="[KB2533623](https://support.microsoft.com/kb/2533623)">KB2533623</a></p></td>
<td align="left"><p>Gilt nur für Windows 7: Laden Sie die KB herunter, und installieren Sie Sie.</p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=40784" data-raw-source="[Visual C++ Redistributable Packages for Visual Studio 2013](https://www.microsoft.com/download/details.aspx?id=40784)">Visual C++-verteilbare Pakete für Visual Studio 2013</a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



## Sequenzer-Voraussetzungs Software


**Was Sie wissen müssen, bevor Sie die Voraussetzungen installieren:**

-   Bewährte Methode: der Computer, auf dem der Sequencer ausgeführt wird, sollte die gleichen Hardware-und Softwarekonfigurationen wie die Computer aufweisen, auf denen die virtuellen Anwendungen ausgeführt werden.

-   Der Sequenzierungsprozess ist ressourcenintensiv, stellen Sie daher sicher, dass der Computer, auf dem der Sequencer ausgeführt wird, genügend Arbeitsspeicher, einen schnellen Prozessor und eine schnelle Festplatte aufweist. Die Systemanforderungen von lokal installierten Anwendungen dürfen die des Sequencers nicht überschreiten. Weitere Informationen finden Sie unter [unterstützte App-V 5,1-Konfigurationen](app-v-51-supported-configurations.md).

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Voraussetzung</th>
<th align="left">Details</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="https://www.microsoft.com//download/details.aspx?id=40773" data-raw-source="[Microsoft .NET Framework 4.5.1 (Web Installer)](https://www.microsoft.com//download/details.aspx?id=40773)">Microsoft .NET Framework 4.5.1 (Web Installer)</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=34595" data-raw-source="[Windows PowerShell 3.0](https://www.microsoft.com/download/details.aspx?id=34595)">Windows PowerShell 3,0</a></p>
<p></p></td>
<td align="left"><p>Für die Installation von PowerShell 3,0 ist ein Neustart erforderlich.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><a href="https://support.microsoft.com/kb/2533623" data-raw-source="[KB2533623](https://support.microsoft.com/kb/2533623)">KB2533623</a></p></td>
<td align="left"><p>Gilt nur für Windows 7: Laden Sie die KB herunter, und installieren Sie Sie.</p></td>
</tr>
</tbody>
</table>








## Verwandte Themen


[Planen von App-V 5.1](planning-for-app-v-51.md)

[App-V 5.1 – Unterstützte Konfigurationen](app-v-51-supported-configurations.md)









