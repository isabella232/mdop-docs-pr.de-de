---
title: Bereitstellungsvoraussetzungen für MBAM 1.0
description: Bereitstellungsvoraussetzungen für MBAM 1.0
author: dansimp
ms.assetid: bd9e1010-7d25-43e7-8dc6-b521226a659d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6ed14343d37a859364bcabbe6ca72c041502a23c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809490"
---
# Bereitstellungsvoraussetzungen für MBAM 1.0


Bevor Sie mit dem Setup für die Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) beginnen, stellen Sie sicher, dass Sie die erforderlichen Voraussetzungen für die Installation des Produkts erfüllen. Dieser Abschnitt enthält Informationen, die Sie beim erfolgreichen Vorbereiten Ihrer Computerumgebung unterstützen, bevor Sie die MBAM-Clients und Server Features bereitstellen.

## Voraussetzungen für die Installation von MBAM Server Features


Für jedes der MBAM-Server Features gelten bestimmte Voraussetzungen, die erfüllt sein müssen, bevor Sie erfolgreich installiert werden können. MBAM-Setup überprüft, ob alle Voraussetzungen erfüllt sind, bevor die Installation gestartet wird.

### Voraussetzungen für die Installation von Administration und Monitoring Server

Die folgende Tabelle enthält die Voraussetzungen für die Installation des MBAM-Verwaltungs-und-Überwachungsservers:

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
<td align="left"><p><strong>Windows ServerWeb-Server Rolle</strong></p></td>
<td align="left"><p>Diese Rolle muss einem Server Betriebssystem hinzugefügt werden, das für das mbam-Verwaltungs-und Überwachungsserver Feature unterstützt wird.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Web Server (IIS)-Verwaltungs Tools</strong></p></td>
<td align="left"><p><strong>IIS-Verwaltungsskripts und-Tools</strong></p></td>
</tr>
<tr class="odd">
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
<tr class="even">
<td align="left"><p><strong>Windows Server-Features</strong></p></td>
<td align="left"><p><strong>Features von Microsoft .NET Framework 3.5.1:</strong></p>
<ul>
<li><p>.NET Framework 3.5.1</p></li>
<li><p>WCF-Aktivierung</p>
<ul>
<li><p>HTTP-Aktivierung</p></li>
<li><p>Nicht-HTTP-Aktivierung</p></li>
</ul></li>
</ul>
<p><strong>Windows-Prozessaktivierungsdienst</strong></p>
<ul>
<li><p>Prozessmodell</p></li>
<li><p>.NET-Umgebung</p></li>
<li><p>Konfigurations-APIs</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

**Hinweis**  Eine Liste der unterstützten Betriebssysteme finden Sie unter [unterstützte MBAM 1,0-Konfigurationen](mbam-10-supported-configurations.md).

 

### Installationsvoraussetzungen für Konformitäts-und Überwachungsberichte

Die Konformitäts-und Überwachungsberichte müssen auf einer unterstützten Version von SQLServer installiert sein. Zu den Installationsvoraussetzungen für dieses Feature gehören SQL Server Reporting Services (SSRS).

SSRS muss während der Installation von MBAM Server installiert sein und ausgeführt werden. SSRS sollte auch im systemeigenen Modus konfiguriert werden, nicht im Modus "nicht konfiguriert" oder "SharePoint".

**Hinweis**  Eine Liste der unterstützten Betriebssysteme und SQLServer-Versionen finden Sie unter [unterstützte MBAM 1,0-Konfigurationen](mbam-10-supported-configurations.md).

 

### Voraussetzungen für die Installation der Wiederherstellungs-und Hardware Datenbank

Die Wiederherstellungs-und Hardware Datenbank muss in einer unterstützten Version von SQLServer installiert sein.

SQL Server muss während der Installation von MBAM Server Datenbankmoduldienste installiert haben und ausgeführt werden. Das Feature "transparente Datenverschlüsselung" (DSA) muss aktiviert sein.

**Hinweis**  Eine Liste der unterstützten Betriebssysteme und SQLServer-Versionen finden Sie unter [unterstützte MBAM 1,0-Konfigurationen](mbam-10-supported-configurations.md).

 

Das Feature "DSA SQLServer" führt eine e/a-Verschlüsselung und-Entschlüsselung der Daten-und Protokolldateien in Echtzeit durch. DSA schützt Daten, die "in Ruhe" sind, die die Daten und die Protokolldateien enthalten. Sie bietet die Möglichkeit, viele Gesetze, Vorschriften und Richtlinien zu erfüllen, die in verschiedenen Branchen etabliert sind.

**Hinweis**  Da DSA die Echt Zeit Verschlüsselung von Datenbankinformationen ausführt, werden die Informationen zum Wiederherstellungsschlüssel angezeigt, wenn das Konto, unter dem Sie angemeldet sind, über Berechtigungen für die Datenbank verfügt, wenn Sie die SQL-Tabellen für Wiederherstellungsschlüssel Informationen anzeigen.

 

### Voraussetzungen für die Installation der Konformitäts-und Überwachungsdatenbank

Die Compliance-und Überwachungsdatenbank muss in einer unterstützten Version von SQLServer installiert sein.

SQL Server muss während der Installation von MBAM Server Datenbankmoduldienste installiert haben und ausgeführt werden.

**Hinweis**  Eine Liste der unterstützten Betriebssysteme und SQLServer-Versionen finden Sie unter [unterstützte MBAM 1,0-Konfigurationen](mbam-10-supported-configurations.md).

 

## Voraussetzungen für die Installation für MBAM-Clients


Die erforderlichen Voraussetzungen, die Sie erfüllen müssen, bevor Sie mit der MBAM-Client Installation beginnen, sind die folgenden:

-   Trusted Platform Module (TPM) v 1.2-Funktion

-   Der TPM-Chip muss im BIOS aktiviert sein und muss vom Betriebssystem rückgestellt werden. Weitere Informationen finden Sie in der BIOS-Dokumentation.

**Warnung**  Stellen Sie sicher, dass Tastatur, Maus und Video direkt mit dem Computer verbunden sind, anstatt mit einem Tastatur-, Video-, Maus-oder KVM-Schalter. Ein KVM-Switch kann die Fähigkeit des Computers stören, die physische Anwesenheit von Hardware zu erkennen.

 

## Verwandte Themen


[Planen der Bereitstellung von MBAM 1.0](planning-to-deploy-mbam-10.md)

[Von MBAM 1.0 unterstützte Konfigurationen](mbam-10-supported-configurations.md)

 

 





