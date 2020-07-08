---
title: Sicherheitsüberlegungen zu MBAM2.0
description: Sicherheitsüberlegungen zu MBAM2.0
author: dansimp
ms.assetid: 0aa5c6e2-d92c-4e30-9f6a-b48abb667ae5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 04dc9b667faddecab629b50f4c5d909fd7b2829e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810240"
---
# Sicherheitsüberlegungen zu MBAM2.0


Dieses Thema enthält eine kurze Übersicht über die Konten und Gruppen, Protokolldateien und andere sicherheitsbezogene Überlegungen für die Microsoft BitLocker-Verwaltung und-Überwachung (MBAM). Weitere Informationen finden Sie unter den Links in diesem Artikel.

## Allgemeine Sicherheitsüberlegungen


**Grundlegendes zu den Sicherheitsrisiken** Das schwerwiegendste Risiko aus der Microsoft BitLocker-Verwaltung und-Überwachung besteht darin, dass die Funktionalität von einem nicht autorisierten Benutzer übernommen werden kann, der dann die BitLocker-Verschlüsselung neu konfigurieren und BitLocker-Verschlüsselungsschlüssel Daten auf MBAM-Clients erhalten kann. Der Verlust von MBAM-Funktionen für kurze Zeit aufgrund eines Denial-of-Service-Angriffs hat jedoch im Allgemeinen keine katastrophalen Auswirkungen, wie beispielsweise e-Mail, Netzwerkkommunikation, Licht und Strom.

**Physisches sichern ihrer Computer**. Es gibt keine Sicherheit ohne physische Sicherheit. Ein Angreifer, der physischen Zugriff auf einen MBAM-Server erhält, kann ihn potenziell zum Angriff auf die gesamte Clientbasis verwenden. Alle potenziellen körperlichen Angriffe müssen als Risiko behaftet und entsprechend verringert werden. MBAM-Server sollten in einem sicheren Serverraum mit kontrolliertem Zugriff gespeichert werden. Sichern Sie diese Computer, wenn Administratoren physisch nicht anwesend sind, indem Sie das Betriebssystem sperren oder einen sicheren Bildschirmschoner verwenden.

**Wenden Sie die neuesten Sicherheitsupdates auf alle Computer an**. Informieren Sie sich über neue Updates für Betriebssysteme, Microsoft SQL Server und MBAM, indem Sie den Security Notification Service ( <https://go.microsoft.com/fwlink/?LinkId=28819> ) abonnieren.

**Verwenden Sie sichere Kennwörter oder Passphrasen**. Verwenden Sie immer starke Kennwörter mit 15 oder mehr Zeichen für alle MBAM-und MBAM-Administratorkonten. Verwenden Sie niemals leere Kennwörter. Weitere Informationen zu Kenn Wort Konzepten finden Sie im Whitepaper "Kontokennwörter und-Richtlinien" auf TechNet ( <https://go.microsoft.com/fwlink/?LinkId=30009> ).

## Konten und Gruppen in MBAM


Die bewährte Methode zum Verwalten von Benutzerkonten ist das Erstellen globaler Domänengruppen und das Hinzufügen von Benutzerkonten. Fügen Sie dann die globalen Domänenkonten den erforderlichen lokalen MBAM-Gruppen auf den MBAM-Servern hinzu.

### ActiveDirectoryDomainServices-Gruppen

Während des MBAM-Setupprozesses werden keine Active Directory-Gruppen automatisch erstellt. Es wird jedoch empfohlen, dass Sie die folgenden globalen ActiveDirectoryDomainServices-Gruppen erstellen, um MBAM-Vorgänge zu verwalten.

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
<td align="left"><p>Diese Gruppe erstellen, um Mitglieder der lokalen Gruppe MBAM Advanced Helpdesk-Benutzer zu verwalten, die während des MBAM-Setups erstellt wurde.</p></td>
</tr>
<tr class="even">
<td align="left"><p>MBAM Compliance Auditing DB Access</p></td>
<td align="left"><p>Diese Gruppe erstellen, um die Mitglieder der MBAM-Konformitätsprüfung zu verwalten, die beim MBAM-Setup erstellt wurde.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>MBAM Helpdesk-Benutzer</p></td>
<td align="left"><p>Diese Gruppe erstellen, um Mitglieder der lokalen Gruppe MBAM Helpdesk-Benutzer zu verwalten, die während des MBAM-Setups erstellt wurde.</p></td>
</tr>
<tr class="even">
<td align="left"><p>MBAM Recovery-und Hardware-DB-Zugriff</p></td>
<td align="left"><p>Diese Gruppe erstellen, um die Mitglieder der lokalen Gruppe MBAM Recovery and Hardware DB Access zu verwalten, die während des MBAM-Setups erstellt wurde.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>MBAM-Berichtsbenutzer</p></td>
<td align="left"><p>Diese Gruppe erstellen, um Mitglieder der lokalen Gruppe MBAM-Berichtsbenutzer zu verwalten, die während des MBAM-Setups erstellt wurde.</p></td>
</tr>
<tr class="even">
<td align="left"><p>MBAM-System Administratoren</p></td>
<td align="left"><p>Diese Gruppe erstellen, um Mitglieder der lokalen Gruppe MBAM-System Administratoren zu verwalten, die während des MBAM-Setups erstellt wurde.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Ausnahmen für BitLocker-Verschlüsselung</p></td>
<td align="left"><p>Erstellen Sie diese Gruppe zum Verwalten von Benutzerkonten, die von der BitLocker-Verschlüsselung ab Computern, bei denen Sie sich anmelden, ausgenommen werden sollen.</p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="-------------mbam-server-local-groups"></a> Lokale MBAM-Server Gruppen

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
<td align="left"><p>Mitglieder dieser Gruppe haben erhöhten Zugriff auf die Helpdesk-Features von MBAM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>MBAM Compliance Auditing DB Access</p></td>
<td align="left"><p>Enthält die Computer, die Zugriff auf die MBAM-Konformitäts-und Überwachungsdatenbank haben.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>MBAM Helpdesk-Benutzer</p></td>
<td align="left"><p>Mitglieder dieser Gruppe können auf einige der Helpdesk-Features von MBAM zugreifen.</p></td>
</tr>
<tr class="even">
<td align="left"><p>MBAM Recovery-und Hardware-DB-Zugriff</p></td>
<td align="left"><p>Enthält die Computer, die Zugriff auf die MBAM-Wiederherstellungsdatenbank haben.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>MBAM-Berichtsbenutzer</p></td>
<td align="left"><p>Mitglieder dieser Gruppe haben Zugriff auf die Konformitäts-und Überwachungsberichte von MBAM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>MBAM-System Administratoren</p></td>
<td align="left"><p>Mitglieder dieser Gruppe haben Zugriff auf alle MBAM-Features.</p></td>
</tr>
</tbody>
</table>

 

### SSRS-Berichtsdienst Konto

Das SSRS-Berichtsdienst Konto bietet den Sicherheitskontext zum Ausführen der MBAM-Berichte, die über SSRS zur Verfügung stehen. Sie wird während des MBAM-Setups konfiguriert.

Wenn Sie das SSRS-Berichtsdienst Konto konfigurieren, geben Sie ein Domänenbenutzerkonto an, und konfigurieren Sie das Kennwort so, dass es nie abläuft.

**Hinweis**  Wenn Sie den Namen des Dienstkontos ändern, nachdem Sie MBAM bereitgestellt haben, müssen Sie die Berichterstellungsdaten Quelle neu konfigurieren, um die neuen Dienstkontoanmeldeinformationen zu verwenden. Andernfalls können Sie nicht auf das Helpdesk-Portal zugreifen.

 

## <a href="" id="---------mbam-log-files"></a> MBAM-Protokolldateien


Die folgenden MBAM-Setupprotokolldateien werden im Ordner "% Temp%" des Installations Benutzers während des MBAM-Setups erstellt:

**MBAM Server Setup-Protokolldateien**

<a href="" id="msi-five-random-characters--log"></a>MSI <em> &lt; fünf zufällige Zeichen &gt; </em> . log  
Protokolliert die Aktionen, die während der Installation von MBAM-Setup und der MBAM-Server Funktion ausgeführt wurden.

<a href="" id="installcompliancedatabase-log"></a>InstallComplianceDatabase. log  
Protokolliert Aktionen, die zum Erstellen der MBAM-Konformitäts-und Überwachungsdatenbank-Einrichtung ausgeführt wurden.

<a href="" id="installkeycompliancedatabase-log"></a>InstallKeyComplianceDatabase. log  
Protokolliert Aktionen, die zum Erstellen der MBAM-Wiederherstellungsdatenbank ausgeführt wurden.

<a href="" id="addhelpdeskdbauditusers-log"></a>AddHelpDeskDbAuditUsers. log  
Protokolliert Aktionen zum Erstellen der SQL Server-Anmeldungen in der MBAM-Konformitäts-und Überwachungsdatenbank und Autorisieren des Helpdesk-Webdiensts für Berichte in der Datenbank.

<a href="" id="addhelpdeskdbusers-log"></a>AddHelpDeskDbUsers. log  
Protokolliert Aktionen, die zum Autorisieren von Webdiensten zur Datenbank für die Schlüsselwiederherstellung und zum Erstellen von Anmeldungen in der MBAM-Wiederherstellungsdatenbank ausgeführt werden.

<a href="" id="addkeycompliancedbusers-log"></a>AddKeyComplianceDbUsers. log  
Protokolliert Aktionen zum Autorisieren von Webdiensten für MBAM Compliance-und Audit-Datenbank für Compliance-Berichte.

<a href="" id="addrecoveryandhardwaredbusers-log"></a>AddRecoveryAndHardwareDbUsers. log  
Protokolliert Aktionen, die zum Autorisieren von Webdiensten zur MBAM-Wiederherstellungsdatenbank für die Schlüsselwiederherstellung ergriffen wurden.

**Hinweis**  Um zusätzliche MBAM-Setup Protokolldateien zu erhalten, müssen Sie MBAM mithilfe des msiexec-Pakets und der Option "/l &lt; Location &gt; " installieren. Protokolldateien werden an dem angegebenen Speicherort erstellt.

 

**MBAM-Client Setup-Protokolldateien**

<a href="" id="msi-five-random-characters--log"></a>MSI <em> &lt; fünf zufällige Zeichen &gt; </em> . log  
Protokolliert die während der MBAM-Client Installation ausgeführten Aktionen.

## <a href="" id="---------mbam-database-tde-considerations"></a> Überlegungen zu MBAM-Daten Bank DSA


Das in SQL Server verfügbare Feature "transparente Datenverschlüsselung (DSA)" ist eine optionale Installation für die Datenbankinstanzen, in denen MBAM-Datenbankfeatures gehostet werden.

Mit DSA können Sie die vollständige Verschlüsselung auf Datenbankebene in Echtzeit durchführen. DSA ist die optimale Lösung für die Massenverschlüsselung, um behördliche Compliance-oder Unternehmensdaten Sicherheitsstandards zu erfüllen. DSA funktioniert auf der Dateiebene, die zwei Windows-Features ähnelt: EFS (Encrypting File System) und BitLocker-Laufwerkverschlüsselung, die beide auch Daten auf der Festplatte verschlüsseln. DSA ersetzt nicht die Verschlüsselung auf Zellenebene, EFS oder BitLocker.

Wenn DSA für eine Datenbank aktiviert ist, werden alle Sicherungen verschlüsselt. Daher muss besonders darauf geachtet werden, dass das zum Schützen des Datenbank-Verschlüsselungsschlüssels verwendete Zertifikat mit der Datenbanksicherung gesichert und verwaltet wird. Wenn dieses Zertifikat (oder Zertifikate) verloren geht, sind die Daten nicht lesbar. Sichern Sie das Zertifikat zusammen mit der Datenbank. Für jede Zertifikat Sicherung sollten zwei Dateien vorhanden sein. Beide Dateien sollten archiviert werden (idealerweise getrennt von der Datenbanksicherungsdatei zur Sicherheit). Alternativ können Sie die erweiterbare Schlüssel Verwaltungsfunktion (Extensible Key Management, erweiterbare Schlüsselverwaltung) für die Speicherung und Wartung von Schlüsseln verwenden, die für DSA verwendet werden.

Ein Beispiel für die Aktivierung von DSA für MBAM-Datenbankinstanzen finden Sie unter [Auswerten von MBAM 2,0](evaluating-mbam-20-mbam-2.md).

Weitere Informationen zu DSA in SQLServer 2008 finden Sie unter [SQL Server-Verschlüsselung]( https://go.microsoft.com/fwlink/?LinkId=299883).

## Verwandte Themen


[Sicherheit und Datenschutz für MBAM 2.0](security-and-privacy-for-mbam-20-mbam-2.md)

 

 





