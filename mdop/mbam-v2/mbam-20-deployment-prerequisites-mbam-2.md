---
title: Bereitstellungsvoraussetzungen für MBAM 2.0
description: Bereitstellungsvoraussetzungen für MBAM 2.0
author: dansimp
ms.assetid: 57d1c2bb-5ea3-457e-badd-dd9206ff0f20
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: ef7ee64a3661009f18e0963d738c57a59885cb20
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811500"
---
# Bereitstellungsvoraussetzungen für MBAM 2.0


Bevor Sie das Setup von Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) starten, sollten Sie sicherstellen, dass Sie die Voraussetzungen für die Installation des Produkts erfüllt haben. Dieser Abschnitt enthält Informationen, die Sie beim erfolgreichen Planen Ihrer Computerumgebung unterstützen, bevor Sie die Microsoft BitLocker-Verwaltungs-und Überwachungs Server Features und-Clients bereitstellen. Wenn Sie MBAM mit Configuration Manager installieren, finden Sie weitere Voraussetzungen unter [Planen der Bereitstellung von MBAM mit Configuration Manager](planning-to-deploy-mbam-with-configuration-manager-2.md) .

## Voraussetzungen für die Installation von MBAM Server Features


Für jedes der MBAM-Server Features gelten bestimmte Voraussetzungen, die erfüllt sein müssen, bevor die MBAM-Features erfolgreich installiert werden können. MBAM-Setup überprüft, ob alle Voraussetzungen erfüllt sind, bevor die Installation gestartet wird.

### Voraussetzungen für Administration und Monitoring Server

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
<td align="left"><p><strong>Rolle des Windows Server-Webservers</strong></p></td>
<td align="left"><p>Diese Rolle muss einem Server Betriebssystem hinzugefügt werden, das für die Verwaltungs-und Überwachungsserver Funktion unterstützt wird.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Web Server (IIS)-Verwaltungs Tools</strong></p></td>
<td align="left"><p>Wählen Sie <strong> IIS-Verwaltungsskripts und-Tools aus </strong> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>SSL-Zertifikat</strong></p></td>
<td align="left"><p>Optional. Um die Kommunikation zwischen den Clients und den Webdiensten zu sichern, müssen Sie ein Zertifikat anfordern und installieren, das von einer vertrauenswürdigen Sicherheitsstelle signiert wurde.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Webserver-Rollendienste</strong></p></td>
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
<td align="left"><p><strong>Windows Server-Features</strong></p></td>
<td align="left"><p><strong>.NET Framework 3.5.1-Features:</strong></p>
<ul>
<li><p>.NET Framework 3.5.1</p></li>
<li><p>WCF-Aktivierung</p>
<ul>
<li><p>HTTP-Aktivierung</p></li>
<li><p>Nicht-HTTP-Aktivierung</p></li>
</ul></li>
</ul>
<p><strong>Windows-Prozessaktivierungsdienst:</strong></p>
<ul>
<li><p>Prozessmodell</p></li>
<li><p>.NET-Umgebung</p></li>
<li><p>Konfigurations-APIs</p></li>
</ul></td>
</tr>
</tbody>
</table>



**Hinweis:**  
Eine Liste der unterstützten Betriebssysteme finden Sie unter [unterstützte MBAM 2,0-Konfigurationen](mbam-20-supported-configurations-mbam-2.md).



### Voraussetzungen für Konformitäts-und Überwachungsberichte

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
<td align="left"><p>Unterstützte Version von SQL Server</p>
<p>Unterstützte Versionen finden Sie unter <a href="mbam-20-supported-configurations-mbam-2.md" data-raw-source="[MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md)"> unterstützte MBAM 2,0 </a> -Konfigurationen.</p></td>
<td align="left"><p>Installieren Sie SQL Server mit:</p>
<ul>
<li><p>SQL_Latin1_General_CP1_CI_AS Sortierung</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>SQL Server Reporting Services (SSRS)</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>SSRS-Instanzen Rechte – für die Installation von Berichten nur erforderlich, wenn Sie Datenbanken auf einem separaten Server aus den Berichten installieren.</p></td>
<td align="left"><p>Erforderliche Instanzen Rechte:</p>
<ul>
<li><p>Erstellen von Ordnern</p></li>
<li><p>Veröffentlichen von Berichten</p></li>
</ul>
<p>SSRS muss während der Installation von MBAM Server installiert sein und ausgeführt werden. Konfigurieren Sie SSRS im systemeigenen Modus und nicht im Modus "nicht konfiguriert" oder "SharePoint".</p></td>
</tr>
</tbody>
</table>



### Voraussetzungen für die Wiederherstellungsdatenbank

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
<td align="left"><p>Unterstützte Version von SQL Server</p>
<p>Unterstützte Versionen finden Sie unter <a href="mbam-20-supported-configurations-mbam-2.md" data-raw-source="[MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md)"> unterstützte MBAM 2,0 </a> -Konfigurationen.</p></td>
<td align="left"><p>Installieren Sie SQL Server mit:</p>
<ul>
<li><p>SQL_Latin1_General_CP1_CI_AS Sortierung</p></li>
<li><p>SQL Server-Verwaltungs Tools</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Erforderliche SQL Server-Berechtigungen</p></td>
<td align="left"><p>Erforderliche Berechtigungen:</p>
<ul>
<li><p>SQL instance-Anmelde Server Rollen:</p>
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
<td align="left"><p>Optional – Installieren der Funktion "transparente Datenverschlüsselung (DSA)" in SQL Server</p></td>
<td align="left"><p>Das Feature "DSA SQL Server" führt die Echtzeit-I/O-Verschlüsselung und-Entschlüsselung der Daten-und Protokolldateien durch, die Ihnen helfen können, viele Gesetze, Vorschriften und Richtlinien zu erfüllen, die in verschiedenen Branchen festgelegt sind.</p>
<div class="alert">
<strong>Hinweis:</strong><br/><p>DSA führt eine echt Zeit Verschlüsselung von Datenbankinformationen durch, was bedeutet, dass die Informationen zum Wiederherstellungsschlüssel sichtbar sind, wenn das Konto, unter dem Sie angemeldet sind, über Berechtigungen für die Datenbank verfügt, während Sie die Wiederherstellungsschlüssel Informationen in den SQL Server-Tabellen anzeigen.</p>
</div>
<div>

</div>
<p>Weitere Informationen zu DSA: <a href="mbam-20-security-considerations-mbam-2.md" data-raw-source="[MBAM 2.0 Security Considerations](mbam-20-security-considerations-mbam-2.md)"> MBAM 2,0-Sicherheitsüberlegungen </a> .</p></td>
</tr>
</tbody>
</table>



### Voraussetzungen für die Compliance-und Audit-Datenbank

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
<td align="left"><p>Unterstützte Version von SQL Server</p>
<p>Unterstützte Versionen finden Sie unter <a href="mbam-20-supported-configurations-mbam-2.md" data-raw-source="[MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md)"> unterstützte MBAM 2,0 </a> -Konfigurationen.</p></td>
<td align="left"><p>Installieren Sie SQL Server mit:</p>
<ul>
<li><p>SQL_Latin1_General_CP1_CI_AS Sortierung</p></li>
<li><p>SQL Server-Verwaltungs Tools</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Erforderliche SQL Server-Berechtigungen</p></td>
<td align="left"><p>Erforderliche Berechtigungen:</p>
<ul>
<li><p>SQL instance-Anmelde Server Rollen:</p>
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
<td align="left"><p>Optional – Installieren der Funktion "transparente Datenverschlüsselung" (DSA) in SQL Server.</p></td>
<td align="left"><p>Das Feature "DSA SQL Server" führt die Echtzeit-I/O-Verschlüsselung und-Entschlüsselung der Daten-und Protokolldateien durch, die Ihnen helfen können, viele Gesetze, Vorschriften und Richtlinien zu erfüllen, die in verschiedenen Branchen festgelegt sind.</p>
<div class="alert">
<strong>Hinweis:</strong><br/><p>DSA führt eine echt Zeit Verschlüsselung von Datenbankinformationen durch, was bedeutet, dass die Informationen zum Wiederherstellungsschlüssel sichtbar sind, wenn das Konto, unter dem Sie angemeldet sind, über Berechtigungen für die Datenbank verfügt, während Sie die Wiederherstellungsschlüssel Informationen in den SQL Server-Tabellen anzeigen.</p>
</div>
<div>

</div>
<p>Weitere Informationen zu DSA: <a href="mbam-20-security-considerations-mbam-2.md" data-raw-source="[MBAM 2.0 Security Considerations](mbam-20-security-considerations-mbam-2.md)"> MBAM 2,0-Sicherheitsüberlegungen</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>SQL Server muss während der Installation von MBAM Server Datenbankmoduldienste installiert haben und ausgeführt werden.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Der SQL Server-Agent-Dienst muss auf den ausgewählten Instanzen von SQL Server ausgeführt und auf Auto-Start eingestellt sein.</p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



### Voraussetzungen für das Self-Service-Portal

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
<td align="left"><p>Unterstützte Version von Windows Server</p>
<p>Unterstützte Versionen finden Sie unter <a href="mbam-20-supported-configurations-mbam-2.md" data-raw-source="[MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md)"> unterstützte MBAM 2,0 </a> -Konfigurationen.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>ASP.NET MVC 2,0</p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=392270" data-raw-source="[ASP.NET MVC 2 download](https://go.microsoft.com/fwlink/?LinkId=392270)">ASP.NET MVC 2 herunterladen</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Web Service IIS-Verwaltungs Tools</p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



## Voraussetzungen für MBAM-Clients


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
<td align="left"><p><strong>Windows 7-Clients </strong> - müssen nur über die TPM-Funktion (Trusted Platform Module) verfügen.</p></td>
<td align="left"><p>Die TPM-Version muss 1,2 oder höher sein.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Der TPM-Chip muss im BIOS aktiviert sein und vom Betriebssystem Rückstellen.</p></td>
<td align="left"><p>Weitere Informationen finden Sie in der BIOS-Dokumentation.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Nur für Windows 8 </strong> -Clients: damit MBAM die TPM-Wiederherstellungsschlüssel speichern und verwalten können: die automatische TPM-Bereitstellung muss deaktiviert sein, und MBAM muss als Besitzer des TPM eingestellt sein, bevor Sie MBAM bereitstellen. Informationen zum Deaktivieren der automatischen Bereitstellung von TPM finden Sie unter <a href="https://go.microsoft.com/fwlink/?LinkId=286468" data-raw-source="[Disable-TpmAutoProvisioning](https://go.microsoft.com/fwlink/?LinkId=286468)"> Disable-TpmAutoProvisioning </a> .</p>
<ul>
<li><p>Die automatische TPM-Bereitstellung muss deaktiviert sein.</p></li>
<li><p>MBAM muss als Besitzer des TPM gesetzt sein, bevor Sie MBAM bereitstellen.</p></li>
</ul></td>
<td align="left"><p>Informationen zum Deaktivieren der automatischen Bereitstellung von TPM finden Sie unter <a href="https://go.microsoft.com/fwlink/?LinkId=286468" data-raw-source="[Disable-TpmAutoProvisioning](https://go.microsoft.com/fwlink/?LinkId=286468)"> Disable-TpmAutoProvisioning </a> .</p>
<div class="alert">
<strong>Hinweis:</strong><br/><p>Stellen Sie sicher, dass die Tastatur, das Video oder die Maus direkt verbunden sind und nicht über einen KVM-Schalter (Keyboard, Video oder Maus) verwaltet werden. Ein KVM-Switch kann die Fähigkeit des Computers stören, die physische Anwesenheit von Hardware zu erkennen.</p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



## Verwandte Themen


[Planen der Bereitstellung von MBAM 2.0](planning-to-deploy-mbam-20-mbam-2.md)

[Von MBAM 2.0 unterstützte Konfigurationen](mbam-20-supported-configurations-mbam-2.md)









