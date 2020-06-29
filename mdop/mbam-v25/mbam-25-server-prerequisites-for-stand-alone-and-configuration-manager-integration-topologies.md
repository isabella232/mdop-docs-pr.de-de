---
title: MBAM 2.5-Servervoraussetzungen für eigenständige und Configuration Manager-Integrationstopologien
description: MBAM 2.5-Servervoraussetzungen für eigenständige und Configuration Manager-Integrationstopologien
author: dansimp
ms.assetid: 76a6047a-5c6e-42ff-af09-a6f382a69537
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: c9af551b1d867f61912bbf3b759574a840b0645c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811491"
---
# MBAM 2.5-Servervoraussetzungen für eigenständige und Configuration Manager-Integrationstopologien


Bevor Sie die Microsoft BitLocker-Verwaltungs-und-überwachungsinstallation (MBAM) starten, müssen Sie die in diesem Thema aufgeführten Voraussetzungen erfüllen. Diese Voraussetzungen gelten für die eigenständige MBAM-Topologie und die System Center Configuration Manager-Integrations Topologie.

Wenn Sie MBAM mit System Center Configuration Manager bereitstellen, müssen Sie weitere Voraussetzungen erfüllen, die in [MBAM 2,5-Server Voraussetzungen aufgeführt sind, die nur für die Configuration Manager-Integrations Topologie gelten](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md).

Eine Liste der unterstützten Hardware-und Betriebssysteme für MBAM finden Sie unter [unterstützte MBAM 2,5-Konfigurationen](mbam-25-supported-configurations.md).

**Wichtig**  
Wenn BitLocker ohne MBAM verwendet wurde, müssen Sie das Laufwerk entschlüsseln und dann TPM mit TPM. msc löschen. MBAM kann den Besitz von TPM nicht übernehmen, wenn der Client-PC bereits verschlüsselt ist und das TPM-Besitzerkennwort erstellt wurde.



## Erforderliche MBAM-Rollen und-Konten


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
<td align="left"><p>In Active Directory-Domänendiensten (AD DS) erstellte Gruppen</p></td>
<td align="left"><p><a href="planning-for-mbam-25-groups-and-accounts.md" data-raw-source="[Planning for MBAM 2.5 Groups and Accounts](planning-for-mbam-25-groups-and-accounts.md)"> </a> Eine Beschreibung dieser Gruppen und Konten finden Sie unter Planen von MBAM 2,5-Gruppen und-Konten.</p></td>
</tr>
</tbody>
</table>



## Voraussetzungen für die Wiederherstellungsdatenbank


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
<td align="left"><p>Unterstützte Version von SQL Server</p></td>
<td align="left"><p>Installieren Sie Microsoft SQL Server mit SQL_Latin1_General_CP1_CI_AS Sortierung.</p>
<p>Unterstützte Versionen finden Sie unter <a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)"> unterstützte MBAM 2,5 </a> -Konfigurationen.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Erforderliche SQL Server-Berechtigungen</p></td>
<td align="left"><p>Erforderliche Berechtigungen:</p>
<ul>
<li><p>Anmeldeserver Rollen für SQL Server-Instanzen:</p>
<ul>
<li><p>dbcreator</p></li>
<li><p>processadmin</p></li>
</ul></li>
<li><p>SQL Server Reporting Services-Instanzen Rechte:</p>
<ul>
<li><p>Erstellen von Ordnern</p></li>
<li><p>Veröffentlichen von Berichten</p></li>
</ul></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>Optional – Installieren des in SQL Server verfügbaren Features "transparente Datenverschlüsselung" (DSA)</p></td>
<td align="left"><p>Das Feature "DSA SQL Server" führt die Echtzeit-I/O-Verschlüsselung und-Entschlüsselung der Daten-und Protokolldateien durch, die Ihnen helfen können, Gesetze, Vorschriften und Richtlinien zu erfüllen, die für verschiedene Branchen gelten.</p>
<div class="alert">
<strong>Hinweis:</strong><br/><p>DSA führt eine echt Zeit Verschlüsselung von Datenbankinformationen durch. Das bedeutet, dass die Informationen zum Wiederherstellungsschlüssel sichtbar sind, wenn Sie Informationen zum Wiederherstellungsschlüssel in der SQL Server-Datenbank anzeigen und unter einem Konto angemeldet sind, das über Berechtigungen für die Datenbank verfügt. Weitere Informationen zu DSA finden Sie unter <a href="mbam-25-security-considerations.md" data-raw-source="[MBAM 2.5 Security Considerations](mbam-25-security-considerations.md)"> Sicherheitsüberlegungen zu MBAM 2,5 </a> .</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>SQL Server-Datenbankmodul-Dienste</p></td>
<td align="left"><p>SQL Server-Datenbankmoduldienste müssen während der Installation von MBAM Server installiert sein und ausgeführt werden.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows PowerShell 3,0 oder höher</p></td>
<td align="left"><p>Windows PowerShell muss nicht auf dem Wiederherstellungsdaten Bankserver installiert werden, wenn Sie Windows PowerShell verwenden, um die Datenbank von einem Remotecomputer aus zu konfigurieren.</p></td>
</tr>
</tbody>
</table>



## Voraussetzungen für die Compliance-und Audit-Datenbank


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
<td align="left"><p>Unterstützte Version von SQL Server</p></td>
<td align="left"><p>Installieren Sie SQL Server mit SQL_Latin1_General_CP1_CI_AS Sortierung.</p>
<p>Unterstützte Versionen finden Sie unter <a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)"> unterstützte MBAM 2,5 </a> -Konfigurationen.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Erforderliche SQL Server-Berechtigungen</p></td>
<td align="left"><p>Erforderliche Berechtigungen:</p>
<ul>
<li><p>Anmeldeserver Rollen für SQL Server-Instanzen:</p>
<ul>
<li><p>dbcreator</p></li>
<li><p>processadmin</p></li>
</ul></li>
<li><p>SQL Server Reporting Services-Instanzen Rechte:</p>
<ul>
<li><p>Erstellen von Ordnern</p></li>
<li><p>Veröffentlichen von Berichten</p></li>
</ul></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>Optional – Installieren des Features "transparente Datenverschlüsselung" (DSA) in SQL Server</p></td>
<td align="left"><p>Das Feature "DSA SQL Server" führt die Echtzeit-I/O-Verschlüsselung und-Entschlüsselung der Daten-und Protokolldateien durch, die Ihnen helfen können, Gesetze, Vorschriften und Richtlinien zu erfüllen, die für verschiedene Branchen gelten.</p>
<p>DSA führt eine echt Zeit Verschlüsselung von Datenbankinformationen durch. Das bedeutet, dass die Informationen zum Wiederherstellungsschlüssel sichtbar sind, wenn Sie Informationen zum Wiederherstellungsschlüssel in der SQL Server-Datenbank anzeigen und unter einem Konto angemeldet sind, das über Berechtigungen für die Datenbank verfügt. Weitere Informationen zu DSA finden Sie unter <a href="mbam-25-security-considerations.md" data-raw-source="[MBAM 2.5 Security Considerations](mbam-25-security-considerations.md)"> Sicherheitsüberlegungen zu MBAM 2,5 </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>SQL Server-Datenbankmodul-Dienste</p></td>
<td align="left"><p>SQL Server-Datenbankmoduldienste müssen während der Installation von MBAM Server installiert sein und ausgeführt werden. SQL Server kann jedoch remote ausgeführt werden. Sie muss sich nicht auf dem Server befinden, auf dem Sie die MBAM-Server Software installieren.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows PowerShell 3,0 oder höher</p></td>
<td align="left"><p>Wenn Sie Windows PowerShell verwenden, um die Datenbank von einem Remotecomputer zu konfigurieren, muss Windows PowerShell nicht auf dem Kompatibilitäts-und Überwachungsdaten Bankserver installiert werden.</p></td>
</tr>
</tbody>
</table>



## Voraussetzungen für die Berichte


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
<td align="left"><p>Unterstützte Version von SQL Server</p></td>
<td align="left"><p>Installieren Sie SQL Server mit SQL_Latin1_General_CP1_CI_AS Sortierung.</p>
<p>Unterstützte Versionen finden Sie unter <a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)"> unterstützte MBAM 2,5 </a> -Konfigurationen.</p></td>
</tr>
<tr class="even">
<td align="left"><p>SQL Server Reporting Services (SSRS)</p></td>
<td align="left"><p>SSRS muss während der Installation von MBAM Server installiert sein und ausgeführt werden.</p>
<p>Konfigurieren Sie SSRS im &quot; einheitlichen &quot; Modus und nicht im nicht konfigurierten oder &quot; SharePoint- &quot; Modus.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Berechtigungen für SSRS-Instanzen – für die Konfiguration von Berichten nur erforderlich, wenn Sie Datenbanken auf einem separaten Server auf dem Server installieren, auf dem Berichte konfiguriert sind.</p></td>
<td align="left"><p>Erforderliche Instanzen Rechte:</p>
<ul>
<li><p>Erstellen von Ordnern</p></li>
<li><p>Veröffentlichen von Berichten</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Windows PowerShell 3,0 oder höher</p></td>
<td align="left"><p>Windows PowerShell muss auf diesem Datenbankserver nicht installiert werden, wenn Sie Windows PowerShell verwenden, um die Datenbank von einem Remotecomputer aus zu konfigurieren.</p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-prereqsams"></a>Voraussetzungen für den Verwaltungs-und Überwachungs Server


In der folgenden Tabelle sind die Installationsvoraussetzungen für den MBAM-Verwaltungs-und-Überwachungs Server aufgelistet.

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
<td align="left"><p>Rolle des Windows Server-Webservers</p></td>
<td align="left"><p>Diese Rolle muss einem Server Betriebssystem hinzugefügt werden, das für die Verwaltungs-und Überwachungsserver Funktion unterstützt wird.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Web Server (IIS)-Verwaltungs Tools</p></td>
<td align="left"><p>Klicken Sie auf <strong> IIS-Verwaltungsskripts und-Tools </strong> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>SSL-Zertifikat</strong></p></td>
<td align="left"><p>Optional. Um die Kommunikation zwischen den Clientcomputern und den Webdiensten zu sichern, müssen Sie ein Zertifikat anfordern und installieren, das von einer vertrauenswürdigen Sicherheitsstelle signiert wurde.</p></td>
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
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server-Features</p></td>
<td align="left"><p><strong>.NET Framework 4,5-Features:</strong></p>
<ul>
<li><p><strong>.NET Framework 4,5 oder 4,6</strong></p>
<ul>
<li><p><strong>Windows Server 2016 </strong> - .NET Framework 4,6 ist bereits für diese Versionen von Windows Server installiert, aber Sie müssen Sie aktivieren.</p></li>  
<li><p><strong>Windows Server 2012 oder Windows Server 2012 R2 </strong> - .NET Framework 4,5 ist bereits für diese Versionen von Windows Server installiert, aber Sie müssen Sie aktivieren.</p></li>
<li><p><strong>Windows Server 2008 R2 </strong> - .NET Framework 4,5 ist nicht im Lieferumfang von Windows Server 2008 R2 enthalten, daher müssen Sie <a href="https://go.microsoft.com/fwlink/?LinkId=392318" data-raw-source="[download Microsoft .NET Framework 4.5](https://go.microsoft.com/fwlink/?LinkId=392318)"> Microsoft .NET Framework 4,5 herunterladen </a> und separat installieren.</p>
<div class="alert">
<strong>Hinweis:</strong><br/><p>Wenn Sie ein Upgrade von MBAM 2,0 oder MBAM 2,0 SP1 durchführen und .NET Framework 4,5 installieren müssen, lesen Sie <a href="release-notes-for-mbam-25.md" data-raw-source="[Release Notes for MBAM 2.5](release-notes-for-mbam-25.md)"> Versionshinweise für MBAM 2,5, um </a> einen zusätzlichen erforderlichen Schritt für die Arbeit der Websites zu erhalten.</p>
</div>
<div>

</div></li>
</ul></li>
<li><p><strong>WCF-Aktivierung</strong></p>
<ul>
<li><p>HTTP-Aktivierung</p></li>
<li><p>Nicht-HTTP-Aktivierung (nur für Windows Server 2008, 2012 und 2012 R2)</p>
<p></p></li>
</ul></li>
<li><p><strong>TCP-Aktivierung</strong></p></li>
</ul>
<p><strong>Windows-Prozessaktivierungsdienst:</strong></p>
<ul>
<li><p>Prozessmodell</p></li>
<li><p>.NET Framework-Umgebung</p></li>
<li><p>Konfigurations-APIs</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>ASP.NET MVC 4,0</p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=392271" data-raw-source="[ASP.NET MVC 4 download](https://go.microsoft.com/fwlink/?LinkId=392271)">ASP.NET MVC 4-Download</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Dienstprinzipal Name (SPN)</p></td>
<td align="left"><p>Die Webanwendungen erfordern einen SPN für den virtuellen Host Namen unter dem Domänenkonto, das Sie für die Webanwendungspools verwenden.</p>
<p>Wenn Ihre Administratorrechte es Ihnen ermöglichen, SPNs in den Active Directory-Domänendiensten zu erstellen, erstellt MBAM den SPN für Sie. <a href="https://technet.microsoft.com/library/cc731241.aspx" data-raw-source="[Setspn](https://technet.microsoft.com/library/cc731241.aspx)">Informationen zu </a> den zum Erstellen von SPNs erforderlichen Rechten finden Sie unter Setspn.</p>
<p>Wenn Sie nicht über Administratorrechte zum Erstellen von SPNs verfügen, müssen Sie die Active Directory-Administratoren in Ihrer Organisation bitten, den SPN für Sie zu erstellen, indem Sie den folgenden Befehl verwenden.</p>
<pre class="syntax" space="preserve"><code>Setspn -s http/mbamvirtual contoso\mbamapppooluser
Setspn -s http/mbamvirtual.contoso.com contoso\mbamapppooluser</code></pre>
<p>Im Codebeispiel lautet der Name des virtuellen Hosts mbamvirtual.contoso.com, und das für die Webanwendungspools verwendete Domänenkonto ist contoso\mbamapppooluser.</p>
<div class="alert">
<strong>Hinweis:</strong><br/><p>Wenn Sie den Lastenausgleich einrichten, verwenden Sie dasselbe Anwendungspoolkonto auf allen Servern.</p>
</div>
<div>

</div>
<p>Weitere Informationen zum Registrieren von SPNs für vollqualifizierte NetBIOS-und benutzerdefinierte Hostnamen finden Sie unter <a href="planning-how-to-secure-the-mbam-websites.md" data-raw-source="[Planning How to Secure the MBAM Websites](planning-how-to-secure-the-mbam-websites.md)"> Planen der Sicherung der MBAM-Websites </a> .</p></td>
</tr>
</tbody>
</table>



## Voraussetzungen für das Self-Service-Portal


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
<td align="left"><p>Unterstützte Version von Windows Server</p></td>
<td align="left"><p>Unterstützte Versionen finden Sie unter <a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)"> unterstützte MBAM 2,5 </a> -Konfigurationen.</p></td>
</tr>
<tr class="even">
<td align="left"><p>ASP.NET MVC 4,0</p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=392271" data-raw-source="[ASP.NET MVC 4 download](https://go.microsoft.com/fwlink/?LinkId=392271)">ASP.NET MVC 4-Download</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Web Service IIS-Verwaltungs Tools</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Dienstprinzipal Name (SPN)</p></td>
<td align="left"><p>Die Webanwendungen erfordern einen SPN für den virtuellen Host Namen unter dem Domänenkonto, das Sie für die Webanwendungspools verwenden.</p>
<p>Wenn Ihre Administratorrechte es Ihnen ermöglichen, SPNs in den Active Directory-Domänendiensten zu erstellen, erstellt MBAM den SPN für Sie. <a href="https://technet.microsoft.com/library/cc731241.aspx" data-raw-source="[Setspn](https://technet.microsoft.com/library/cc731241.aspx)">Informationen zu </a> den zum Erstellen von SPNs erforderlichen Rechten finden Sie unter Setspn.</p>
<p>Wenn Sie nicht über Administratorrechte zum Erstellen von SPNs verfügen, müssen Sie die Active Directory-Administratoren in ihren Organisationsadministratoren in Ihrer Organisation bitten, den SPN für Sie zu erstellen, indem Sie den folgenden Befehl verwenden.</p>
<pre class="syntax" space="preserve"><code>Setspn -s http/mbamvirtual contoso\mbamapppooluser
Setspn -s http/mbamvirtual.contoso.com contoso\mbamapppooluser</code></pre>
<p>Im Codebeispiel lautet der Name des virtuellen Hosts mbamvirtual.contoso.com, und das für die Webanwendungspools verwendete Domänenkonto ist contoso\mbamapppooluser.</p>
<div class="alert">
<strong>Hinweis:</strong><br/><p>Wenn Sie den Lastenausgleich einrichten, verwenden Sie dasselbe Anwendungspoolkonto auf allen Servern.</p>
</div>
<div>

</div>
<p>Weitere Informationen zum Registrieren von SPNs für vollqualifizierte NetBIOS-und benutzerdefinierte Hostnamen finden Sie unter <a href="planning-how-to-secure-the-mbam-websites.md" data-raw-source="[Planning How to Secure the MBAM Websites](planning-how-to-secure-the-mbam-websites.md)"> Planen der Sicherung der MBAM-Websites </a> .</p></td>
</tr>
</tbody>
</table>



## Voraussetzungen für die Verwaltungsarbeitsstation


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
<td align="left"><p>Bevor Sie den MBAM-Client installieren, laden Sie die MBAM-Gruppenrichtlinienvorlagen aus, <a href="https://go.microsoft.com/fwlink/p/?LinkId=393941" data-raw-source="[How to Get MDOP Group Policy (.admx) Templates](https://go.microsoft.com/fwlink/p/?LinkId=393941)"> wie Sie MDOP Gruppenrichtlinien (ADMX)-Vorlagen abrufen, </a> und konfigurieren Sie Sie mit den Einstellungen, die Sie in Ihrem Unternehmen für die BitLocker-Laufwerkverschlüsselung implementieren möchten.</p></td>
<td align="left"><p>Bevor Sie den MBAM-Client installieren, gehen Sie folgendermaßen vor:</p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Erforderlich</th>
<th align="left">Wo erhalte ich Anweisungen?</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Kopieren der MBAM-Gruppenrichtlinienvorlagen</p></td>
<td align="left"><p><a href="copying-the-mbam-25-group-policy-templates.md" data-raw-source="[Copying the MBAM 2.5 Group Policy Templates](copying-the-mbam-25-group-policy-templates.md)">Kopieren die Gruppenrichtlinienvorlagen für MBAM 2.5</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Bearbeiten der Gruppenrichtlinieneinstellungen</p></td>
<td align="left"><p><a href="editing-the-mbam-25-group-policy-settings.md" data-raw-source="[Editing the MBAM 2.5 Group Policy Settings](editing-the-mbam-25-group-policy-settings.md)">Bearbeiten der Gruppenrichtlinieneinstellungen für MBAM 2.5</a></p></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
</tbody>
</table>





## Verwandte Themen


[Vorbereiten der Umgebung für MBAM 2.5](preparing-your-environment-for-mbam-25.md)

[Planen der Bereitstellung von MBAM 2.5](planning-to-deploy-mbam-25.md)

[Von MBAM 2.5 unterstützte Konfigurationen](mbam-25-supported-configurations.md)




## Sie haben einen Vorschlag für MBAM?
- [Hier](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)können Sie Vorschläge hinzufügen oder abstimmen.
- Bei MBAM-Problemen verwenden Sie das [MBAM TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).




