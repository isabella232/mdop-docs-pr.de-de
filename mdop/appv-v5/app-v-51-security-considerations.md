---
title: Sicherheitsüberlegungen zu App-V 5.1
description: Sicherheitsüberlegungen zu App-V 5.1
author: dansimp
ms.assetid: 6bc6c1fc-f813-47d4-b763-06fd4faf6a72
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 8a5606b3e0ba5e6fb8c62f14e2ed8d93ea2cf134
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805972"
---
# Sicherheitsüberlegungen zu App-V 5.1


Dieses Thema enthält eine kurze Übersicht über die Konten und Gruppen, Protokolldateien und andere sicherheitsbezogene Überlegungen für Microsoft Application Virtualization (App-V) 5,1.

**Wichtig**  
App-V 5,1 ist kein Sicherheitsprodukt und bietet keine Garantien für eine sichere Umgebung.



## PackageStoreAccessControl (PSAC erklärte)-Feature wurde als veraltet markiert


Ab Juni 2014 wurde das PackageStoreAccessControl (PSAC erklärte)-Feature, das in Microsoft Application Virtualization (App-V) 5,0 Service Pack 2 (SP2) eingeführt wurde, in Umgebungen mit einzelnen Benutzern und mehreren Benutzern als veraltet markiert.

## Allgemeine Sicherheitsüberlegungen


**Grundlegendes zu den Sicherheitsrisiken** Das schwerwiegendste Risiko für App-v 5,1 besteht darin, dass die Funktionalität von einem nicht autorisierten Benutzer übernommen werden kann, der dann die wichtigsten Daten auf App-v 5,1-Clients neu konfigurieren kann. Der Verlust der App-V 5,1-Funktionalität für kurze Zeit aufgrund eines Denial-of-Service-Angriffs hätte in der Regel keine katastrophalen Auswirkungen.

**Physisches sichern ihrer Computer**. Sicherheit ist ohne physische Sicherheit unvollständig. Jeder mit physischem Zugriff auf einen App-V 5,1-Server kann potenziell die gesamte Clientbasis angreifen. Mögliche physische Angriffe müssen als Risiko behaftet und entsprechend verringert werden. App-V 5,1-Server sollten in einem physisch sicheren Serverraum mit kontrolliertem Zugriff gespeichert werden. Sichern Sie diese Computer, wenn Administratoren physisch nicht anwesend sind, indem Sie das Betriebssystem sperren oder einen sicheren Bildschirmschoner verwenden.

**Wenden Sie die neuesten Sicherheitsupdates auf alle Computer an**. Wenn Sie über die neuesten Updates für Betriebssysteme, Microsoft SQL Server und App-V 5,1 auf dem Laufenden bleiben möchten, abonnieren Sie den Sicherheitsbenachrichtigungsdienst ( <https://go.microsoft.com/fwlink/p/?LinkId=28819> ).

**Verwenden Sie sichere Kennwörter oder Passphrasen**. Verwenden Sie immer starke Kennwörter mit 15 oder mehr Zeichen für alle App-v 5,1-und App-v 5,1-Administratorkonten. Verwenden Sie niemals leere Kennwörter. Weitere Informationen zu Kenn Wort Konzepten finden Sie im Whitepaper "Kontokennwörter und-Richtlinien" auf TechNet ( <https://go.microsoft.com/fwlink/p/?LinkId=30009> ).

## Konten und Gruppen in App-V 5,1


Eine bewährte Methode für die Verwaltung von Benutzerkonten ist das Erstellen globaler Domänengruppen und das Hinzufügen von Benutzerkonten. Fügen Sie dann die globalen Domänenkonten den erforderlichen App-v 5,1-lokalen Gruppen auf den App-v 5,1-Servern hinzu.

**Hinweis:**  
App-V-Clientcomputerkonten, die eine Verbindung mit dem Veröffentlichungsserver herstellen müssen, müssen Teil der lokalen Gruppe **Benutzer** des Veröffentlichungsservers sein. Standardmäßig sind alle Computer in der Domäne Teil der Gruppe **autorisierte Benutzer** , die Teil der lokalen Gruppe **Benutzer** ist.



### <a href="" id="-------------app-v-5-1-server-security"></a> App-V 5,1-Server Sicherheit

Während der App-V 5,1-Einrichtung werden keine Gruppen automatisch erstellt. Sie sollten die folgenden globalen Active Directory-Domänendienste-Gruppen erstellen, um die App-V 5,1-Server Vorgänge zu verwalten.

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
<td align="left"><p>App-V-Verwaltungs Administratorgruppe</p></td>
<td align="left"><p>Wird verwendet, um den App-V 5,1-Verwaltungsserver zu verwalten. Diese Gruppe wird während der Installation des App-V 5,1-Verwaltungsservers erstellt.</p>
<div class="alert">
<strong>Wichtig</strong><br/><p>Nachdem Sie die Installation abgeschlossen haben, gibt es keine Methode zum Erstellen der Gruppe mithilfe der Verwaltungskonsole.</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>Datenbank-Lese-/Schreibzugriff für Verwaltungsdienst Konto</p></td>
<td align="left"><p>Bietet Lese-und Schreibzugriff auf die Verwaltungsdatenbank. Dieses Konto sollte während der Installation der App-V 5,1-Verwaltungsdatenbank erstellt werden.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>App-V-Verwaltungsdienst: Administratorkonto installieren</p>
<div class="alert">
<strong>Hinweis:</strong><br/><p>Dies ist nur erforderlich, wenn die Verwaltungsdatenbank separat vom Dienst installiert wird.</p>
</div>
<div>

</div></td>
<td align="left"><p>Bietet öffentlichen Zugriff auf die Tabelle "Schemaversion" in der Verwaltungsdatenbank. Dieses Konto sollte während der Installation der App-V 5,1-Verwaltungsdatenbank erstellt werden.</p></td>
</tr>
<tr class="even">
<td align="left"><p>App-V Reporting Service-Administratorkonto installieren</p>
<div class="alert">
<strong>Hinweis:</strong><br/><p>Dies ist nur erforderlich, wenn die Berichtsdatenbank separat vom Dienst installiert wird.</p>
</div>
<div>

</div></td>
<td align="left"><p>Öffentlicher Zugriff auf die Tabelle "Schemaversion" in der Berichtsdatenbank. Dieses Konto sollte während der Installation der App-V 5,1-Berichtsdatenbank erstellt werden.</p></td>
</tr>
</tbody>
</table>



Bedenken Sie die folgenden zusätzlichen Informationen:

-   Zugriff auf die Paketfreigaben – wenn eine Freigabe auf demselben Computer wie der Verwaltungs Server vorhanden ist, erfordert der **Netzwerk** Dienst Lesezugriff auf die Freigabe. Darüber hinaus muss jeder App-V-Clientcomputer über Lesezugriff auf die Paketfreigabe verfügen.

    **Hinweis:**  
    In früheren Versionen von App-V wurde die Paketfreigabe als Inhaltsfreigabe bezeichnet.



-   Registrieren von Veröffentlichungsservern mit dem Verwaltungsserver – ein Veröffentlichungsserver muss beim Verwaltungsserver registriert sein. Beispielsweise muss Sie der Datenbank hinzugefügt werden, damit die Computerkonten des Publishing Servers in die Verwaltungsdienst-API aufgerufen werden können.

### <a href="" id="-------------app-v-5-1-package-security"></a> App-V 5,1-Paketsicherheit

Im folgenden wird erläutert, wie Sie sicherstellen können, dass virtualisierte Pakete sicher sind.

-   Wenn ein Anwendungs Installationsprogramm eine Zugriffssteuerungsliste (ACL) auf eine Datei oder ein Verzeichnis anwendet, wird diese ACL nicht im Paket beibehalten. Wenn das Paket bereitgestellt wird und die Datei oder das Verzeichnis von einem Benutzer geändert wird, erbt es entweder die ACL in **% User Profile%** oder erbt die ACL des Verzeichnisses des Zielcomputers. Der erste Fall tritt auf, wenn die Datei oder das Verzeichnis nicht an einem Speicherort des virtuellen Dateisystems vorhanden ist. der letzte Fall tritt auf, wenn die Datei oder das Verzeichnis an einem virtuellen Dateisystemspeicherort vorhanden ist, beispielsweise **% windir%**.

## <a href="" id="---------app-v-5-1-log-files"></a> App-V 5,1-Protokolldateien


Während der Installation von App-V 5,1 werden Setupprotokolldateien im Ordner **% Temp%** des Installations Benutzers erstellt.






## Verwandte Themen


[Vorbereiten der Umgebung für App-V 5.1](preparing-your-environment-for-app-v-51.md)









