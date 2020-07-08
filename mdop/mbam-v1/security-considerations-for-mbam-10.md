---
title: Sicherheitsüberlegungen zu MBAM 1.0
description: Sicherheitsüberlegungen zu MBAM 1.0
author: dansimp
ms.assetid: 5e1c8b8c-235b-4a92-8b0b-da50dca17353
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: b06c343c8193293dde91bc7af2541f35f332d261
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811608"
---
# Sicherheitsüberlegungen zu MBAM 1.0


Dieses Thema enthält eine kurze Übersicht über die Konten und Gruppen, Protokolldateien und andere sicherheitsbezogene Überlegungen für die Microsoft BitLocker-Verwaltung und-Überwachung (MBAM). Weitere Informationen finden Sie unter den Links in diesem Artikel.

## Allgemeine Sicherheitsüberlegungen


**Grundlegendes zu den Sicherheitsrisiken** Das schwerwiegendste Risiko für MBAM besteht darin, dass seine Funktionalität von einem nicht autorisierten Benutzer gekapert werden kann, der dann die BitLocker-Verschlüsselung neu konfigurieren und BitLocker-Verschlüsselungsschlüssel Daten auf MBAM-Clients erhalten kann. Der Verlust von MBAM-Funktionen für einen kurzen Zeitraum aufgrund eines Denial-of-Service-Angriffs würde jedoch im Allgemeinen keine katastrophalen Auswirkungen haben.

**Physisches sichern ihrer Computer**. Sicherheit ist ohne physische Sicherheit unvollständig. Jeder, der über einen physischen Zugriff auf einen MBAM-Server verfügt, kann möglicherweise die gesamte Clientbasis angreifen. Mögliche physische Angriffe müssen als Risiko behaftet und entsprechend verringert werden. MBAM-Server sollten in einem physisch sicheren Serverraum mit kontrolliertem Zugriff gespeichert werden. Sichern Sie diese Computer, wenn Administratoren physisch nicht anwesend sind, indem Sie das Betriebssystem sperren oder einen sicheren Bildschirmschoner verwenden.

**Wenden Sie die neuesten Sicherheitsupdates auf alle Computer an**. Informieren Sie sich über neue Updates für Betriebssysteme, Microsoft SQL Server und MBAM, indem Sie den Security Notification Service ( <https://go.microsoft.com/fwlink/p/?LinkId=28819> ) abonnieren.

**Verwenden Sie sichere Kennwörter oder Passphrasen**. Verwenden Sie immer starke Kennwörter mit 15 oder mehr Zeichen für alle MBAM-und MBAM-Administratorkonten. Verwenden Sie niemals leere Kennwörter. Weitere Informationen zu Kenn Wort Konzepten finden Sie im Whitepaper "Kontokennwörter und-Richtlinien" auf TechNet ( <https://go.microsoft.com/fwlink/p/?LinkId=30009> ).

## Konten und Gruppen in MBAM


Eine bewährte Methode für die Verwaltung von Benutzerkonten ist das Erstellen globaler Domänengruppen und das Hinzufügen von Benutzerkonten. Fügen Sie dann die globalen Domänenkonten den erforderlichen lokalen MBAM-Gruppen auf den MBAM-Servern hinzu.

### ActiveDirectoryDomainServices-Gruppen

Während der MBAM-Einrichtung werden keine Gruppen automatisch erstellt. Sie sollten jedoch die folgenden globalen ActiveDirectoryDomainServices-Gruppen erstellen, um MBAM-Vorgänge zu verwalten.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Gruppenname</th>
<th align="left">Details</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>MBAM Advanced Helpdesk-Benutzer</p></td>
<td align="left"><p>Erstellen Sie diese Gruppe zum Verwalten von Mitgliedern der lokalen Gruppe MBAM Advanced Helpdesk-Benutzer, die während des MBAM-Setups erstellt wurde.</p></td>
</tr>
<tr class="even">
<td align="left"><p>MBAM Compliance Auditing DB Access</p></td>
<td align="left"><p>Erstellen Sie diese Gruppe zum Verwalten von Mitgliedern der lokalen Gruppe MBAM Compliance Auditing DB Access, die während des MBAM-Setups erstellt wurde.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>MBAM-Hardware Benutzer</p></td>
<td align="left"><p>Erstellen Sie diese Gruppe, um die Mitglieder der lokalen Gruppe MBAM-Hardware Benutzer zu verwalten, die während des MBAM-Setups erstellt wurde.</p></td>
</tr>
<tr class="even">
<td align="left"><p>MBAM Helpdesk-Benutzer</p></td>
<td align="left"><p>Erstellen Sie diese Gruppe, um Mitglieder der lokalen Gruppe MBAM Helpdesk-Benutzer zu verwalten, die während des MBAM-Setups erstellt wurde.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>MBAM Recovery-und Hardware-DB-Zugriff</p></td>
<td align="left"><p>Erstellen Sie diese Gruppe, um die Mitglieder der lokalen Gruppe MBAM Recovery and Hardware DB Access zu verwalten, die während des MBAM-Setups erstellt wurde.</p></td>
</tr>
<tr class="even">
<td align="left"><p>MBAM-Berichtsbenutzer</p></td>
<td align="left"><p>Erstellen Sie diese Gruppe, um Mitglieder der lokalen Gruppe MBAM-Berichtsbenutzer zu verwalten, die während des MBAM-Setups erstellt wurde.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>MBAM-System Administratoren</p></td>
<td align="left"><p>Erstellen Sie diese Gruppe, um die Mitglieder der lokalen Gruppe MBAM-System Administratoren zu verwalten, die während des MBAM-Setups erstellt wurde.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Ausnahmen für BitLocker-Verschlüsselung</p></td>
<td align="left"><p>Erstellen Sie diese Gruppe zum Verwalten von Benutzerkonten, die von der BitLocker-Verschlüsselung ab Computern, bei denen Sie sich anmelden, ausgenommen werden sollen.</p></td>
</tr>
</tbody>
</table>

 

### Lokale MBAM-Server Gruppen

MBAM Setup erstellt lokale Gruppen, um MBAM-Vorgänge zu unterstützen. Sie sollten die globalen ActiveDirectoryDomainServices-Gruppen den entsprechenden lokalen MBAM-Gruppen hinzufügen, um MBAM-Sicherheits-und Datenzugriffsberechtigungen zu konfigurieren.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Gruppenname</th>
<th align="left">Details</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>MBAM Advanced Helpdesk-Benutzer</p></td>
<td align="left"><p>Mitglieder dieser Gruppe haben erweiterten Zugriff auf die Helpdesk-Features der Microsoft BitLocker-Verwaltung und-Überwachung.</p></td>
</tr>
<tr class="even">
<td align="left"><p>MBAM Compliance Auditing DB Access</p></td>
<td align="left"><p>Diese Gruppe enthält die Computer, die Zugriff auf die MBAM-Konformitäts Überwachungsdatenbank haben.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>MBAM-Hardware Benutzer</p></td>
<td align="left"><p>Mitglieder dieser Gruppe haben Zugriff auf einige der Hardware Funktionen von Microsoft BitLocker-Verwaltung und-Überwachung.</p></td>
</tr>
<tr class="even">
<td align="left"><p>MBAM Helpdesk-Benutzer</p></td>
<td align="left"><p>Mitglieder dieser Gruppe können über die Microsoft BitLocker-Verwaltung und-Überwachung auf einige der Helpdesk-Features zugreifen.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>MBAM Recovery-und Hardware-DB-Zugriff</p></td>
<td align="left"><p>Diese Gruppe enthält die Computer, die Zugriff auf die MBAM-Wiederherstellungs-und-Hardware Datenbank haben.</p></td>
</tr>
<tr class="even">
<td align="left"><p>MBAM-Berichtsbenutzer</p></td>
<td align="left"><p>Mitglieder dieser Gruppe haben Zugriff auf die Konformitäts-und Überwachungsberichte aus der Microsoft BitLocker-Verwaltung und-Überwachung.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>MBAM-System Administratoren</p></td>
<td align="left"><p>Mitglieder dieser Gruppe haben Zugriff auf alle Features der Microsoft BitLocker-Verwaltung und-Überwachung.</p></td>
</tr>
</tbody>
</table>

 

### Zugriffskonto für SSRS-Berichte

Das SQL Server Reporting Services (SSRS)-Berichtsdienst Konto bietet den Sicherheitskontext zum Ausführen der MBAM-Berichte, die über SSRS zur Verfügung stehen. Dieses Konto wird während des MBAM-Setups konfiguriert.

## MBAM-Protokolldateien


Während des MBAM-Setups werden die folgenden MBAM-Setupprotokolldateien im Ordner "% Temp%" des Benutzers erstellt, der den

**MBAM Server Setup-Protokolldateien**

<a href="" id="msi-five-random-characters--log"></a>MSI <em> &lt; fünf zufällige Zeichen &gt; </em> . log  
Protokolliert die Aktionen, die während der Installation von MBAM-Setup und der MBAM-Server Funktion ausgeführt wurden.

<a href="" id="installcompliancedatabase-log"></a>InstallComplianceDatabase. log  
Protokolliert die Aktionen, die zum Erstellen der MBAM-Konformitäts Status Datenbank ausgeführt wurden.

<a href="" id="installkeycompliancedatabase-log"></a>InstallKeyComplianceDatabase. log  
Protokolliert die Aktionen, die zum Erstellen der MBAM-Wiederherstellungs-und-Hardware Datenbank ausgeführt wurden.

<a href="" id="addhelpdeskdbauditusers-log"></a>AddHelpDeskDbAuditUsers. log  
Protokolliert die Aktionen, die zum Erstellen der SQL Server-Anmeldungen in der MBAM-Konformitäts Status Datenbank ergriffen wurden, und Autorisieren des Helpdesk-Webdiensts zur Datenbank für Berichte.

<a href="" id="addhelpdeskdbusers-log"></a>AddHelpDeskDbUsers. log  
Protokolliert die Aktionen, die zum Autorisieren von Webdiensten zur Datenbank für die Schlüsselwiederherstellung und zum Erstellen von Anmeldungen in der MBAM-Wiederherstellungs-und-Hardware Datenbank ausgeführt werden

<a href="" id="addkeycompliancedbusers-log"></a>AddKeyComplianceDbUsers. log  
Protokolliert die Aktionen, die zum Autorisieren von Webdiensten zur MBAM-Konformitäts Status Datenbank für Konformitätsberichte ergriffen wurden.

<a href="" id="addrecoveryandhardwaredbusers-log"></a>AddRecoveryAndHardwareDbUsers. log  
Protokolliert die Aktionen, die zum Autorisieren von Webdiensten zur MBAM-Wiederherstellung und Hardware Datenbank für die Schlüsselwiederherstellung ergriffen wurden.

**Hinweis**  Um weitere MBAM-Setup Protokolldateien zu erhalten, müssen Sie die Microsoft BitLocker-Verwaltung und-Überwachung mithilfe des **msiexec** -Pakets und der Option " **/l** &lt; Location &gt; " installieren. Protokolldateien werden an dem angegebenen Speicherort erstellt.

 

**MBAM-Client Setup-Protokolldateien**

<a href="" id="msi-five-random-characters--log"></a>MSI <em> &lt; fünf zufällige Zeichen &gt; </em> . log  
Protokolliert die während der MBAM-Client Installation ausgeführten Aktionen.

## Überlegungen zu MBAM-Daten Bank DSA


Das in SQL Server 2008 verfügbare Feature "transparente Datenverschlüsselung (DSA)" ist eine erforderliche Installationsvoraussetzung für die Datenbankinstanzen, in denen MBAM-Datenbankfeatures gehostet werden.

Mit DSA können Sie die vollständige Verschlüsselung auf Datenbankebene in Echtzeit durchführen. DSA eignet sich hervorragend für die Massenverschlüsselung, um behördliche Compliance-oder Unternehmensdaten Sicherheitsstandards zu erfüllen. DSA funktioniert auf der Dateiebene, die zwei Windows-Features ähnelt: EFS (Encrypting File System) und BitLocker-Laufwerkverschlüsselung, die beide auch Daten auf der Festplatte verschlüsseln. DSA ersetzt nicht die Verschlüsselung auf Zellenebene, EFS oder BitLocker.

Wenn DSA für eine Datenbank aktiviert ist, werden alle Sicherungen verschlüsselt. Daher muss besonders darauf geachtet werden, dass das zum Schützen des Daten Bank Verschlüsselungsschlüssels (DEK) verwendete Zertifikat mit der Datenbanksicherung gesichert und verwaltet wird. Ohne ein Zertifikat sind die Daten nicht lesbar. Sichern Sie das Zertifikat zusammen mit der Datenbank. Für jede Zertifikat Sicherung sollten zwei Dateien vorhanden sein. Beide Dateien sollten archiviert werden. Es empfiehlt sich, die Daten aus der Datenbank-Sicherungsdatei für die Sicherheit separat zu archivieren.

Ein Beispiel für die Aktivierung von DSA für MBAM-Datenbankinstanzen finden Sie unter [Auswerten von MBAM 1,0](evaluating-mbam-10.md).

Weitere Informationen zu DSA in SQLServer 2008 finden Sie unter [Datenbankverschlüsselung in SQL Server 2008 Enterprise Edition](https://go.microsoft.com/fwlink/?LinkId=269703).

## Verwandte Themen


[Sicherheit und Datenschutz für MBAM 1.0](security-and-privacy-for-mbam-10.md)

 

 





