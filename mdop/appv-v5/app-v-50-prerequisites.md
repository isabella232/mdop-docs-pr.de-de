---
title: Voraussetzungen für App-V 5.0
description: Voraussetzungen für App-V 5.0
author: dansimp
ms.assetid: 9756b571-c785-4ce6-a95c-d4e134e89429
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 176c9729d8c909325c6d6694e024938d9ce9df53
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806008"
---
# Voraussetzungen für App-V 5.0

Bevor Sie mit der Installation von Microsoft Application Virtualization (App-V) 5,0 beginnen, sollten Sie sicherstellen, dass Sie die Voraussetzungen für die Installation des Produkts erfüllt haben. Dieses Thema enthält Informationen, die Ihnen bei der erfolgreichen Planung der Vorbereitung Ihrer Computerumgebung helfen, bevor Sie die App-V 5,0-Features bereitstellen.

> [!Important]
> **Die Voraussetzungen in diesem Artikel gelten nur für App-V 5,0**. Weitere Voraussetzungen, die für App-V 5,0-Service Packs gelten, finden Sie auf den folgenden Webseiten:

-   [Neuigkeiten in App-V 5.0 SP1](whats-new-in-app-v-50-sp1.md)

-   [Informationen zu App-V 5.0 SP2](about-app-v-50-sp2.md)

-   [Voraussetzungen für App-V 5.0 SP3](app-v-50-sp3-prerequisites.md)

In der folgenden Tabelle sind die erforderlichen Informationen zu bestimmten Betriebssystemen aufgeführt.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Betriebssysteme</th>
<th align="left">Beschreibung der Voraussetzungen</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Computer, die ausgeführt werden:</p>
<ul>
<li><p>Windows 8</p></li>
<li><p>Windows Server 2012</p></li>
</ul></td>
<td align="left"><p>Die folgenden Voraussetzungen sind bereits installiert:</p>
<ul>
<li><p>Microsoft .NET Framework 4,5 – Sie benötigen Microsoft .NET Framework 4 nicht</p></li>
<li><p>Windows PowerShell 3,0</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Computer, die ausgeführt werden:</p>
<ul>
<li><p>Windows7</p></li>
<li><p>Windows Server 2008</p></li>
</ul></td>
<td align="left"><p>Möglicherweise möchten Sie die folgenden KB herunterladen:</p>
<p><a href="https://support.microsoft.com/kb/2533623" data-raw-source="[Microsoft Security Advisory: Insecure library loading could allow remote code execution](https://support.microsoft.com/kb/2533623)">Microsoft-Sicherheitshinweis: das Laden einer unsicheren Bibliothek kann die Ausführung von Remote Code ermöglichen</a></p>
<p>Achten Sie darauf, auf nachfolgende KBS zu überprüfen, die diese ersetzt haben, und beachten Sie, dass bei einigen KBS möglicherweise frühere Updates deinstalliert werden müssen.</p></td>
</tr>
</tbody>
</table>

## Voraussetzungen für die Installation von App-V 5,0

> [!Note]  
> Die folgenden Voraussetzungen sind bereits für Computer installiert, auf denen Windows 8 ausgeführt wird.

Jedes der APP-v 5,0-Features verfügt über bestimmte Voraussetzungen, die erfüllt sein müssen, bevor die APP-v 5,0-Features erfolgreich installiert werden können.

### Voraussetzungen für den App-V 5,0-Client

In der folgenden Tabelle sind die Voraussetzungen für die Installation des App-V 5,0-Clients aufgeführt:

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
<td align="left"><p><strong>Softwareanforderungen</strong></p></td>
<td align="left"><ul>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=17718" data-raw-source="[Microsoft .NET Framework 4 (Full Package)](https://www.microsoft.com/download/details.aspx?id=17718)">Microsoft .NET Framework 4 (vollständiges Paket)</p></li>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=34595" data-raw-source="[Windows PowerShell 3.0](https://www.microsoft.com/download/details.aspx?id=34595)">Windows PowerShell 3,0</a></p>
<p></p>
<div class="alert">
<strong>Hinweis:</strong><br/><p>Für die Installation von PowerShell 3,0 ist ein Neustart erforderlich.</p>
</div>
<div>

</div></li>
<li><p>Herunterladen und Installieren von <a href="https://support.microsoft.com/kb/2533623" data-raw-source="[KB2533623](https://support.microsoft.com/kb/2533623)"> KB2533623</a></p>
<p></p>
<div class="alert">
<strong>Wichtig</strong><br/><p>Sie können den vorherigen KB-Artikel herunterladen und installieren. Möglicherweise wurde Sie jedoch durch eine neuere Version ersetzt.</p>
</div>
<div>

</div></li>
<li><p>Das Client-Installationsprogramm (. exe) erkennt, ob die folgenden Voraussetzungen installiert werden müssen, und dies wird entsprechend:</p>
<p></p>
<ul>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=40784" data-raw-source="[Visual C++ Redistributable Packages for Visual Studio 2013](https://www.microsoft.com/download/details.aspx?id=40784)">Visual C++-verteilbare Pakete für Visual Studio 2013</a></p>
<p>Diese Voraussetzung ist nur erforderlich, wenn Sie Hotfix-Paket 4 für Application Virtualization 5,0 SP2 oder höher installiert haben.</p>
<p></p></li>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=26999" data-raw-source="[The Microsoft Visual C++ 2010 Redistributable](https://www.microsoft.com/download/details.aspx?id=26999)">Die Microsoft Visual C++ 2010-verteilbare</a></p>
<p></p></li>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=5638" data-raw-source="[Microsoft Visual C++ 2005 SP1 Redistributable Package (x86)](https://www.microsoft.com/download/details.aspx?id=5638)">Microsoft Visual C++ 2005 SP1 Redistributable Package (x86)</a></p></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>

### Voraussetzungen für den App-V 5,0-Remote Desktop Dienste-Client

> [!Note]  
> Die folgenden Voraussetzungen sind bereits für Computer installiert, auf denen Windows Server 2012 ausgeführt wird.

In der folgenden Tabelle sind die Voraussetzungen für die Installation des App-V 5,0-Remote Desktop Dienste-Clients aufgeführt:

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
<td align="left"><p><strong>Softwareanforderungen</strong></p></td>
<td align="left"><ul>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=17718" data-raw-source="[Microsoft.NET Framework 4 (Full Package)](https://www.microsoft.com/download/details.aspx?id=17718)">Microsoft.NET Framework 4 (vollständiges Paket)</a></p></li>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=34595" data-raw-source="[Windows PowerShell 3.0](https://www.microsoft.com/download/details.aspx?id=34595)">Windows PowerShell 3,0</a></p>
<p></p>
<div class="alert">
<strong>Hinweis:</strong><br/><p>Für die Installation von PowerShell 3,0 ist ein Neustart erforderlich.</p>
</div>
<div>

</div></li>
<li><p>Herunterladen und Installieren von <a href="https://go.microsoft.com/fwlink/?LinkId=286102" data-raw-source="[KB2533623](https://go.microsoft.com/fwlink/?LinkId=286102 )"> KB2533623</a></p>
<p></p>
<div class="alert">
<strong>Wichtig</strong><br/><p>Sie können den vorherigen KB-Artikel herunterladen und installieren. Möglicherweise wurde Sie jedoch durch eine neuere Version ersetzt.</p>
</div>
<div>

</div></li>
<li><p>Der Client (. exe) erkennt, ob es notwendig ist, die folgenden Voraussetzungen zu installieren, und dies wird entsprechend:</p>
<p></p>
<ul>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=40784" data-raw-source="[Visual C++ Redistributable Packages for Visual Studio 2013](https://www.microsoft.com/download/details.aspx?id=40784)">Visual C++-verteilbare Pakete für Visual Studio 2013</a></p>
<p>Diese Voraussetzung ist nur erforderlich, wenn Sie Hotfix-Paket 4 für Application Virtualization 5,0 SP2 oder höher installiert haben.</p>
<p></p></li>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=26999" data-raw-source="[The Microsoft Visual C++ 2010 Redistributable](https://www.microsoft.com/download/details.aspx?id=26999)">Die Microsoft Visual C++ 2010-verteilbare</a></p>
<p></p></li>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=5638" data-raw-source="[Microsoft Visual C++ 2005 SP1 Redistributable Package (x86)](https://www.microsoft.com/download/details.aspx?id=5638)">Microsoft Visual C++ 2005 SP1 Redistributable Package (x86)</a></p></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>

### Voraussetzungen für den App-V 5,0-Sequenzer

> [!Note]
> Die folgenden Voraussetzungen sind bereits für Computer installiert, auf denen Windows 8 und Windows Server 2012 ausgeführt wird.

In der folgenden Tabelle sind die Voraussetzungen für die Installation des App-V 5,0-Sequencers aufgeführt. Wenn möglich, sollte der Computer, auf dem der Sequencer ausgeführt wird, die gleichen Hardware-und Softwarekonfigurationen wie die Computer aufweisen, auf denen die virtuellen Anwendungen ausgeführt werden.

> [!Note]  
> Wenn die Systemanforderungen einer lokal installierten Anwendung die Anforderungen des Sequencers überschreiten, müssen Sie den Anforderungen dieser Anwendung genügen. Darüber hinaus empfehlen wir, dass der Computer, auf dem der Sequencer ausgeführt wird, über genügend Arbeitsspeicher, einen schnellen Prozessor und eine schnelle Festplatte verfügt, da der Sequenzierungsprozess Systemressourcen intensiv ist. Weitere Informationen finden Sie unter [unterstützte Konfigurationen für App-V 5,0](app-v-50-supported-configurations.md).

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
<td align="left"><p><strong>Softwareanforderungen</strong></p></td>
<td align="left"><ul>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=40784" data-raw-source="[Visual C++ Redistributable Packages for Visual Studio 2013](https://www.microsoft.com/download/details.aspx?id=40784)">Visual C++-verteilbare Pakete für Visual Studio 2013</a></p>
<p>Diese Voraussetzung ist nur erforderlich, wenn Sie Hotfix-Paket 4 für Application Virtualization 5,0 SP2 installiert haben.</p>
<p></p></li>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=17718" data-raw-source="[Microsoft .NET Framework 4 (Full Package)](https://www.microsoft.com/download/details.aspx?id=17718)">Microsoft .NET Framework 4 (vollständiges Paket)</a></p>
<p></p></li>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=34595" data-raw-source="[Windows PowerShell 3.0](https://www.microsoft.com/download/details.aspx?id=34595)">Windows PowerShell 3,0</a></p>
<p></p></li>
<li><p>Herunterladen und Installieren von <a href="https://support.microsoft.com/kb/2533623" data-raw-source="[KB2533623](https://support.microsoft.com/kb/2533623)"> KB2533623</a></p>
<p></p></li>
<li><p>Für Computer mit Microsoft Windows Server 2008 R2 SP1 laden Sie KB2533623 herunter, und installieren Sie es. <a href="https://go.microsoft.com/fwlink/?LinkId=286102" data-raw-source="[KB2533623](https://go.microsoft.com/fwlink/?LinkId=286102 )"></a></p>
<p></p>
<div class="alert">
<strong>Wichtig</strong><br/><p>Sie können entweder einen der vorhergehenden KB-Artikel herunterladen und installieren. Möglicherweise wurden Sie jedoch durch eine neuere Version ersetzt.</p>
</div>
<div>

</div></li>
</ul></td>
</tr>
</tbody>
</table>

### Voraussetzungen für den App-V 5,0-Server

> [!Note]
> Die folgenden Voraussetzungen sind bereits für Computer installiert, auf denen Windows Server 2012 ausgeführt wird:

-   Microsoft .NET Framework 4,5. Dadurch werden die Anforderungen von Microsoft .NET Framework 4 beseitigt.

-   Windows PowerShell 3,0

-   Herunterladen und Installieren von [KB2533623](https://support.microsoft.com/kb/2533623) (https://support.microsoft.com/kb/2533623)

    > [!Important]
    > Sie können die vorherige KB-Installation weiterhin herunterladen. Möglicherweise wurde Sie jedoch durch eine neuere Version ersetzt.

In der folgenden Tabelle sind die Voraussetzungen für die Installation des App-V 5,0-Servers aufgelistet. Das Konto, mit dem Sie die Server Komponenten installieren, muss über Administratorrechte auf dem Computer verfügen, auf dem Sie die Installation durchführen. Dieses Konto muss auch die Möglichkeit haben, Active Directory-Verzeichnisdienste abzufragen. Bevor Sie die App-V 5,0-Server installieren und konfigurieren, müssen Sie einen Port angeben, in dem die einzelnen Komponenten gehostet werden. Sie müssen auch die zugehörigen Firewallregeln hinzufügen, um eingehende Anforderungen an die angegebenen Ports zu ermöglichen.

> [!Note]
> WebDAV (Web Distributed Authoring and Versioning) wird für den Verwaltungsdienst automatisch deaktiviert.

Der App-V 5,0-Server wird für eine eigenständige Bereitstellung unterstützt, in der alle Komponenten auf dem gleichen Server und eine verteilte Bereitstellung bereitgestellt werden. Je nach der Topologie, die Sie für die Bereitstellung des App-V 5,0-Servers verwenden, ändern sich die Daten, die Sie für die einzelnen Komponenten benötigen, leicht.

> [!Important]
> Die Installation des App-v 5,0-Servers auf einem Computer, auf dem eine frühere Version oder Komponente von App-v ausgeführt wird, wird nicht unterstützt. Darüber hinaus wird die Installation der Server Komponenten auf einem Computer, auf dem Server Core oder ein Domänen Controller ausgeführt wird, ebenfalls nicht unterstützt.

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
<td align="left"><p><strong>Verwaltungs Server</strong></p></td>
<td align="left"><ul>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=17718" data-raw-source="[Microsoft .NET Framework 4 (Full Package)](https://www.microsoft.com/download/details.aspx?id=17718)">Microsoft .NET Framework 4 (vollständiges Paket)</a></p></li>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=34595" data-raw-source="[Windows PowerShell 3.0](https://www.microsoft.com/download/details.aspx?id=34595)">Windows PowerShell 3,0</a></p>
<div class="alert">
<strong>Hinweis:</strong><br/><p>Für die Installation von PowerShell 3,0 ist ein Neustart erforderlich.</p>
</div>
<div>

</div></li>
<li><p>Windows Web Server mit aktivierter IIS-Rolle und den folgenden Features: <strong> Allgemeine HTTP-Features </strong> (statischer Inhalt und Standarddokument), <strong> Anwendungsentwicklung </strong> (ASP.net, .NET-Erweiterbarkeit, ISAPI-Erweiterungen und ISAPI-Filter), <strong> Sicherheit </strong> (Windows-Authentifizierung, Anforderungsfilterung), <strong> Verwaltungs Tools </strong> (IIS-Verwaltungskonsole).</p></li>
<li><p>Herunterladen und Installieren von <a href="https://support.microsoft.com/kb/2533623" data-raw-source="[KB2533623](https://support.microsoft.com/kb/2533623)"> KB2533623</a></p>
<p></p>
<div class="alert">
<strong>Wichtig</strong><br/><p>Sie können die vorherige KB-Installation weiterhin herunterladen. Möglicherweise wurde Sie jedoch durch eine neuere Version ersetzt.</p>
</div>
<div>

</div></li>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=13523" data-raw-source="[Microsoft Visual C++ 2010 SP1 Redistributable Package (x64)](https://www.microsoft.com/download/details.aspx?id=13523)">Microsoft Visual C++ 2010 SP1 Redistributable Package (x64)</a></p></li>
<li><p><a href="https://go.microsoft.com/fwlink/?LinkId=267110" data-raw-source="[Microsoft Visual C++ 2010 SP1 Redistributable Package (x86)](https://go.microsoft.com/fwlink/?LinkId=267110)">Microsoft Visual C++ 2010 SP1 Redistributable Package (x86)</a></p></li>
<li><p>64-Bit ASP.net-Registrierung</p></li>
</ul>
<p>Die Komponenten der App-V 5,0-Server sind abhängig, aber Sie haben unterschiedliche Anforderungen und Installationsoptionen, die bereitgestellt werden müssen. Verwenden Sie die folgenden Informationen, um die Umgebung so vorzubereiten, dass der App-V 5,0-Verwaltungsserver ausgeführt wird.</p>
<ul>
<li><p>Installationsspeicherort – Standardmäßig wird diese Komponente in folgendem installiert: <strong> %ProgramFiles%\Microsoft Application Virtualization Server </strong> .</p></li>
<li><p>Speicherort der App-V 5,0-Verwaltungsdatenbank-SQL Server-Name, SQL-Instanzenname, Datenbankname.</p></li>
<li><p>Zugriffsrechte für die App-V 5,0-Verwaltungskonsole – hierbei handelt es sich um den Benutzer oder die Gruppe, dem am Ende der Bereitstellung der Zugriff auf die Verwaltungskonsole gewährt werden soll. Nach der Bereitstellung können nur diese Benutzer auf die Verwaltungskonsole zugreifen, bis zusätzliche Administratoren über die Verwaltungskonsole hinzugefügt werden.</p>
<div class="alert">
<strong>Hinweis:</strong><br/><p>Sicherheitsgruppen und einzelne Benutzer werden nicht unterstützt. Sie müssen eine AD DS-Gruppe angeben.</p>
</div>
<div>

</div></li>
<li><p>App-V 5,0-Verwaltungsdienst Websitename – geben Sie einen Namen für die Website an, oder verwenden Sie den Standardnamen.</p></li>
<li><p>Portbindung des App-V 5,0-Verwaltungsdiensts – dies sollte eine eindeutige Portnummer sein, die nicht von einer anderen Website auf dem Computer verwendet wird.</p></li>
<li><p>Unterstützung für Microsoft Silverlight – Microsoft Silverlight muss installiert sein, bevor die Verwaltungskonsole verfügbar ist. Obwohl dies keine Voraussetzung für die Bereitstellung ist, muss der Server in der Lage sein, Microsoft Silverlight zu unterstützen.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Verwaltungsdatenbank</strong></p></td>
<td align="left"><p></p>
<div class="alert">
<strong>Hinweis:</strong><br/><p>Die Datenbank ist nur bei Verwendung des App-V 5,0-Verwaltungsservers erforderlich.</p>
</div>
<div>

</div>
<ul>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=17718" data-raw-source="[Microsoft .NET Framework 4 (Full Package)](https://www.microsoft.com/download/details.aspx?id=17718)">Microsoft .NET Framework 4 (vollständiges Paket)</a></p></li>
<li><p><a href="https://go.microsoft.com/fwlink/?LinkId=267110" data-raw-source="[Microsoft Visual C++ 2010 SP1 Redistributable Package (x86)](https://go.microsoft.com/fwlink/?LinkId=267110)">Microsoft Visual C++ 2010 SP1 Redistributable Package (x86)</a></p></li>
</ul>
<p>Die Komponenten der App-V 5,0-Server sind abhängig, aber Sie haben unterschiedliche Anforderungen und Installationsoptionen, die bereitgestellt werden müssen. Verwenden Sie die folgenden Informationen, um Ihre Umgebung für die Ausführung der App-V 5,0-Verwaltungsdatenbank vorzubereiten.</p>
<ul>
<li><p>Installationsspeicherort – Standardmäßig wird diese Komponente auf <strong> %ProgramFiles%\Microsoft Application Virtualization Server installiert </strong> .</p></li>
<li><p>Benutzerdefinierter SQL Server-Instanzname (falls zutreffend) – das Format sollte <strong> instanceName sein </strong> , da bei der Installation davon ausgegangen wird, dass Sie sich auf dem lokalen Computer befindet. Wenn Sie den Namen mit dem folgenden Format angeben, <strong> </strong> schlägt SVR\INSTANCE fehl.</p></li>
<li><p>Benutzerdefinierter App-V 5,0-Datenbankname (falls zutreffend) – Sie müssen einen eindeutigen Datenbanknamen angeben. Der Standardwert für die Verwaltungsdatenbank lautet <strong> AppVManagement </strong> .</p></li>
<li><p>App-V 5,0-Verwaltungsserver Standort – gibt das Computerkonto an, auf dem der Verwaltungsserver bereitgestellt wird. Dies sollte im folgenden Format Domain\MachineAccount angegeben werden <strong> </strong> .</p></li>
<li><p>App-v 5,0 Management Server-Installations Administrator – gibt das Konto an, das zum Installieren des App-v 5,0-Verwaltungsservers verwendet wird. Verwenden Sie das folgende Format: <strong> Domain\AdministratorLoginName </strong> .</p></li>
<li><p>Microsoft SQL Server-Dienst-Agent – konfigurieren Sie den Computer, auf dem die App-V 5,0-Verwaltungsdatenbank ausgeführt wird, damit der Dienst des Microsoft SQL Server-Agents automatisch neu gestartet wird. Weitere Informationen finden Sie unter <a href="https://go.microsoft.com/fwlink/?LinkId=273725" data-raw-source="[Configure SQL Server Agent to Restart Services Automatically](https://go.microsoft.com/fwlink/?LinkId=273725)"> Konfigurieren des SQL Server-Agents, um Dienste automatisch neu zu starten.</a></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Berichts Server</strong></p></td>
<td align="left"><ul>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=17718" data-raw-source="[Microsoft .NET Framework 4 (Full Package)](https://www.microsoft.com/download/details.aspx?id=17718)">Microsoft .NET Framework 4 (vollständiges Paket)</a></p></li>
<li><p><a href="https://go.microsoft.com/fwlink/?LinkId=267110" data-raw-source="[Microsoft Visual C++ 2010 SP1 Redistributable Package (x86)](https://go.microsoft.com/fwlink/?LinkId=267110)">Microsoft Visual C++ 2010 SP1 Redistributable Package (x86)</a></p></li>
<li><div class="alert">
<strong>Hinweis:</strong><br/><p>Um das Risiko von unerwünschten oder böswilligen Daten, die an den Berichtsserver gesendet werden, zu verringern, sollten Sie den Zugriff auf den Reporting Web Service pro Ihre Unternehmenssicherheitsrichtlinie einschränken.</p>
</div>
<div>

</div>
<p>Windows Web Server mit der IIS-Rolle mit den folgenden Features: <strong> Allgemeine HTTP-Features </strong> (statischer Inhalt und Standarddokument), <strong> Anwendungsentwicklung </strong> (ASP.net, .NET-Erweiterbarkeit, ISAPI-Erweiterungen und ISAPI-Filter), <strong> Sicherheit </strong> (Windows-Authentifizierung, Anforderungsfilterung), <strong> Sicherheit </strong> (Windows-Authentifizierung, Anforderungsfilterung), <strong> Verwaltungs Tools </strong> (IIS-Verwaltungskonsole)</p></li>
<li><p>64-Bit ASP.net-Registrierung</p></li>
<li><p>Installationsspeicherort – Standardmäßig wird diese Komponente auf <strong> %ProgramFiles%\Microsoft Application Virtualization Server installiert </strong> .</p></li>
<li><p>App-V 5,0 Reporting Service-Websitename – gibt den Namen der Website oder den Standardnamen an, der verwendet wird.</p></li>
<li><p>App-V 5,0 Reporting Service-Portbindung – dies sollte eine eindeutige Portnummer sein, die nicht bereits von einer anderen Website verwendet wird, die auf dem Computer ausgeführt wird.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Berichtsdatenbank</strong></p></td>
<td align="left"><p></p>
<div class="alert">
<strong>Hinweis:</strong><br/><p>Die Datenbank ist nur bei Verwendung des App-V 5,0-Berichtsservers erforderlich.</p>
</div>
<div>

</div>
<ul>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=17718" data-raw-source="[Microsoft .NET Framework 4 (Full Package)](https://www.microsoft.com/download/details.aspx?id=17718)">Microsoft .NET Framework 4 (vollständiges Paket)</a></p></li>
<li><p><a href="https://go.microsoft.com/fwlink/?LinkId=267110" data-raw-source="[Microsoft Visual C++ 2010 SP1 Redistributable Package (x86)](https://go.microsoft.com/fwlink/?LinkId=267110)">Microsoft Visual C++ 2010 SP1 Redistributable Package (x86)</a></p></li>
</ul>
<p>Die Komponenten der App-V 5,0-Server sind abhängig, aber Sie haben unterschiedliche Anforderungen und Installationsoptionen, die bereitgestellt werden müssen. Verwenden Sie die folgenden Informationen, um Ihre Umgebung für die Ausführung der App-V 5,0-Berichtsdatenbank vorzubereiten.</p>
<ul>
<li><p>Installationsspeicherort – Standardmäßig wird diese Komponente auf <strong> %ProgramFiles%\Microsoft Application Virtualization Server installiert </strong> .</p></li>
<li><p>Benutzerdefinierter SQL Server-Instanzname (falls zutreffend) – das Format sollte <strong> instanceName sein </strong> , da bei der Installation davon ausgegangen wird, dass Sie sich auf dem lokalen Computer befindet. Wenn Sie den Namen mit dem folgenden Format angeben, <strong> </strong> schlägt SVR\INSTANCE fehl.</p></li>
<li><p>Benutzerdefinierter App-V 5,0-Datenbankname (falls zutreffend) – Sie müssen einen eindeutigen Datenbanknamen angeben. Der Standardwert für die Berichtsdatenbank lautet <strong> AppVReporting </strong> .</p></li>
<li><p>App-V 5,0-Berichtsserverstandort – gibt das Computerkonto an, auf dem der Berichtsserver bereitgestellt wird. Dies sollte im folgenden Format Domain\MachineAccount angegeben werden <strong> </strong> .</p></li>
<li><p>App-v 5,0 Reporting Server-Installations Administrator – gibt das Konto an, das zum Installieren des App-v 5,0-Berichtsservers verwendet wird. Verwenden Sie das folgende Format: <strong> Domain\AdministratorLoginName </strong> .</p></li>
<li><p>Microsoft SQL Server-Dienst und der Microsoft SQL Server-Agentdienst – diese Dienste müssen Benutzerkonten zugeordnet sein, die Zugriff auf Abfrage Anzeige haben.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Veröffentlichungs Server</strong></p></td>
<td align="left"><ul>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=17718" data-raw-source="[Microsoft .NET Framework 4 (Full Package)](https://www.microsoft.com/download/details.aspx?id=17718)">Microsoft .NET Framework 4 (vollständiges Paket)</a></p></li>
<li><p><a href="https://go.microsoft.com/fwlink/?LinkId=267110" data-raw-source="[Microsoft Visual C++ 2010 SP1 Redistributable Package (x86)](https://go.microsoft.com/fwlink/?LinkId=267110)">Microsoft Visual C++ 2010 SP1 Redistributable Package (x86)</a></p></li>
<li><p>Windows Web Server mit der IIS-Rolle mit den folgenden Features: <strong> Allgemeine HTTP-Features </strong> (statischer Inhalt und Standarddokument), <strong> Anwendungsentwicklung </strong> (ASP.net, .NET-Erweiterbarkeit, ISAPI-Erweiterungen und ISAPI-Filter), <strong> Sicherheit </strong> (Windows-Authentifizierung, Anforderungsfilterung), <strong> Sicherheit </strong> (Windows-Authentifizierung, Anforderungsfilterung), <strong> Verwaltungs Tools </strong> (IIS-Verwaltungskonsole)</p></li>
<li><p>64-Bit ASP.net-Registrierung</p></li>
</ul>
<p>Die Komponenten der App-V 5,0-Server sind abhängig, aber Sie haben unterschiedliche Anforderungen und Installationsoptionen, die bereitgestellt werden müssen. Verwenden Sie die folgenden Informationen, um Ihre Umgebung so vorzubereiten, dass der App-V 5,0-Veröffentlichungsserver ausgeführt wird.</p>
<ul>
<li><p>Installationsspeicherort – Standardmäßig wird diese Komponente auf <strong> %ProgramFiles%\Microsoft Application Virtualization Server installiert </strong> .</p></li>
<li><p>App-v 5,0-Verwaltungsdienst-URL – gibt die URL des App-v 5,0-Verwaltungsdiensts an. Hierbei handelt es sich um den Port, mit dem der Veröffentlichungsserver kommuniziert, und er sollte mit dem folgenden Format angegeben <strong><a href="http://localhost:12345" data-raw-source="http://localhost:12345"> werden: http://localhost:12345 </a></strong></p></li>
<li><p>Websitename der App-V 5,0 Publishing Service – gibt den Namen der Website oder den Standardnamen an, der verwendet wird.</p></li>
<li><p>Portbindung des App-V 5,0-Publishing Diensts – dies sollte eine eindeutige Portnummer sein, die nicht bereits von einer anderen Website verwendet wird, die auf dem Computer ausgeführt wird.</p></li>
</ul></td>
</tr>
</tbody>
</table>

## Verwandte Themen

[Planen der Bereitstellung von App-V](planning-to-deploy-app-v.md)

[Unterstützte App-V 5.0-Konfigurationen](app-v-50-supported-configurations.md)
