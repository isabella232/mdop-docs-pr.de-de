---
title: Planen der Serversicherheit
description: Planen der Serversicherheit
author: dansimp
ms.assetid: c7cd8227-b359-41e7-a8ae-d0d5718a76a2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 9bea1bd8287a15385200bbfb425ed8e00fbcdb02
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806492"
---
# Planen der Serversicherheit


Um die Sicherheit einer Umgebung zu verbessern, müssen Sie sich mit der Gefährdung potenzieller Bedrohungen in der Umgebung befassen. Für die Bereitstellung von Sicherheit für eine APP-v-Infrastruktur müssen Sie die spezifischen app-v-Sicherheitsfeatures sowie die Sicherheitsmethoden und-Features für die zugrunde liegende Infrastruktur verwenden. Durch die Sicherung der zugrunde liegenden Infrastruktur für Dienste wie Internet Informationsdienste (IIS), Active Directory-Domänendienste und SQL Server wird die allgemeine Sicherheit für Ihr App-V-System verbessert.

Die Standardeinstellungen für die Server Installation bieten die höchsten Sicherheitsstufen. Einige Komponenten verlassen sich jedoch auf die zugrunde liegende Infrastruktur, die nicht als Teil der Installation konfiguriert ist. Wenn Sie nach der Installation Vorgehen, wird die Sicherheit der App-V-Infrastruktur verbessert.

Das Inhaltsverzeichnis enthält alle Pakete, die an Clients gestreamt werden sollen. Diese Ressourcen müssen so sicher wie möglich sein, um viele mögliche Sicherheitsrisiken zu vermeiden. Die folgende Liste enthält einige zusätzliche Anleitungen:

-   UNC-basiertes veröffentlichen und/oder Streaming – die Berechtigungen für dieses Element sollten in der Umgebung am restriktivsten sein. Verwenden Sie NTFS-Berechtigungen, um die restriktivsten Zugriffssteuerungslisten (ACLs) für das Inhaltsverzeichnis zu implementieren (Benutzer = lesen, Administratoren = lesen und schreiben).

-   IIS für die Veröffentlichung und/oder das Streaming: Konfigurieren Sie IIS so, dass nur die Windows-integrierte Authentifizierung unterstützt wird. Entfernen Sie den anonymen Zugriff auf den IIS-Server, und beschränken Sie den Zugriff auf das Verzeichnis mit NTFS-Berechtigungen.

-   RTSP/RTSPS zum Streamen von Anwendungspaketen – konfigurieren Sie die App-V-Anbieterrichtlinie so, dass Authentifizierung erforderlich ist, Zugriffsberechtigungen erzwungen werden, und aktivieren Sie nur erforderliche Gruppen, um auf die Anbieterrichtlinie zugreifen zu können. Konfigurieren Sie Anwendungen mit den entsprechenden Berechtigungen in der Datenbank.

Halten Sie die Anzahl der Benutzer mit Administratorrechten auf ein minimales Niveau, um mögliche Bedrohungen für die Daten im Datenspeicher zu verringern und zu vermeiden, dass schädliche Anwendungen in der Infrastruktur veröffentlicht werden.

## Application Virtualization-Sicherheit


App-V verwendet verschiedene Kommunikationsmethoden zwischen den verschiedenen Komponenten der Infrastruktur. Wenn Sie Ihre App-V-Infrastruktur planen, kann das Sichern der Kommunikation zwischen Servern die Sicherheitsrisiken reduzieren, die möglicherweise bereits im vorhandenen Netzwerk vorhanden sind.

### Datenspeicher

Der Application Virtualization Management Server und Application Virtualization Management Service kommunizieren mit dem Datenspeicher mithilfe einer SQL-Verbindung über TCP-Port 1433. Der Verwaltungs Server verwendet den Datenspeicher, um Anwendungs-und Konfigurationsdaten abzurufen, und schreibt Nutzungsinformationen in die Datenbank. Der Verwaltungsdienst kommuniziert mit dem Datenspeicher im Auftrag eines Administrators, der die App-V-Infrastruktur konfiguriert. Da der Datenspeicher wichtige Informationen enthält, ist es wichtig, Bedrohungen für diese Daten zu minimieren.

Es wird empfohlen, die Kommunikation zwischen App-V-Verwaltungs Server, Verwaltungsdienst und Datenspeicher mit IPSec (Internet Protocol Security) zu sichern. Erstellen Sie insbesondere Richtlinien, die den Kommunikationskanal zwischen dem Datenspeicher (SQL) und dem Verwaltungs Server und dem Datenspeicher und dem Verwaltungsdienst sichern. Sie können die Server-und Domänenisolierung auch mit IPSec bereitstellen, um sicherzustellen, dass alle Komponenten der App-V-Infrastruktur nur mit sicheren Kanälen kommunizieren. Informationen zum Implementieren von IPSec finden Sie in der folgenden Dokumentation:

-   Informationen zu Windows Server2003 finden Sie unter <https://go.microsoft.com/fwlink/?LinkId=133226> ( https://go.microsoft.com/fwlink/?LinkId=133226) .

-   Informationen zu Windows Server2008 finden Sie unter <https://go.microsoft.com/fwlink/?LinkId=133227> ( https://go.microsoft.com/fwlink/?LinkId=133227) .

### Inhaltsverzeichnis

Die Installation des App-V-Verwaltungsservers konfiguriert einen Speicherort für das Inhaltsverzeichnis. Dieses Verzeichnis ist der Speicherort für virtualisierte Anwendungspakete. Dieser Speicherort kann lokal auf dem Server oder auf einer Remotenetzwerkfreigabe gespeichert werden. Implementieren Sie daher IPSec, um die Kommunikation mit einem Remotespeicherort für das Inhaltsverzeichnis zu sichern.

Sie können auch ein virtuelles Verzeichnis auf einem IIS-Server verwenden, um Pakete an die Clients zu streamen. Wenn sich das für Inhalte erstellte virtuelle Verzeichnis auf einer Remotequelle befindet, verwenden Sie IPSec, um die Kommunikation zwischen dem IIS-Server und dem Remotespeicherort zu sichern.

Das Inhaltsverzeichnis enthält alle Pakete, die an Clients gestreamt werden. Diese Ressourcen müssen so sicher wie möglich sein, um viele mögliche Sicherheitsrisiken zu vermeiden.

### Sicherheitsprotokolle

Sie können RTSPS oder HTTPS verwenden, um die sichere Kommunikation zu verbessern. RTSPS ist das von App-V-Servern verwendete Protokoll, und HTTPS ist das von IIS-Servern verwendete Protokoll. Diese Protokolle werden verwendet, wenn Anwendungen vom Server auf dem Application Virtualization Desktop-Client veröffentlicht werden. Nachdem Sie das gewünschte Protokoll festgelegt haben, fügen Sie einen Veröffentlichungsserver hinzu, der dieses Protokoll verwendet.

### <a href="" id="configuring-app-v-servers-for-rtsps-"></a>Konfigurieren von App-V-Servern für RTSPS

Wenn Sie einen app-v-Verwaltungs Server oder Streamingserver für die Verwendung von erweiterter Sicherheit (beispielsweise TLS) installieren oder konfigurieren, muss ein X. 509 v3-Zertifikat für den App-v-Server bereitgestellt werden. Wenn Sie die Installation oder Konfiguration der Sicherheit für einen Server vorbereiten, müssen Sie bestimmte Anforderungen erfüllen. Technische Voraussetzungen für die Bereitstellung und Konfiguration von Zertifikaten für einen sichereren App-V-Verwaltungsserver oder Streamingserver sind die folgenden:

-   Das Zertifikat muss gültig sein. Andernfalls beendet der Client die Verbindung.

-   Das Zertifikat muss die richtige Enhanced Key Usage (EKU)-Server Authentifizierung (OID 1.3.6.1.5.5.7.3.1) enthalten. Andernfalls beendet der Client die Verbindung.

-   Der vollqualifizierte Zertifikat-Domänenname (Fully Qualified Domain Name, FQDN) muss mit dem Server übereinstimmen, auf dem er installiert ist. Wenn beispielsweise der Client angerufen wird `RTSPS://Myserver.mycompany.com/content/MyApp.sft` , das für das Feld **ausgestellte** Zertifikat jedoch enthalten ist `Myserver1.mycompany.com` , stellt der Client keine Verbindung mit dem Server her, und die Sitzung wird beendet, auch wenn er `Myserver.mycompany.com` `Myserver1.mycompany.com` mit der gleichen IP-Adresse aufgelöst wird.

    **Hinweis**  Wenn Sie App-V in einem Cluster mit Netzwerklastenausgleich verwenden, muss das Zertifikat mit " *Subject Alternate Names* (SANs)" konfiguriert werden, um RTSPS zu unterstützen. Informationen zum Konfigurieren der Zertifizierungsstelle (Certification Authority, ca) und zum Erstellen von Zertifikaten mit Sans finden Sie unter <https://go.microsoft.com/fwlink/?LinkId=133228> ( https://go.microsoft.com/fwlink/?LinkId=133228) .

     

-   Die Zertifizierungsstelle, die das Zertifikat an den App-V-Server ausgibt, muss vom Client als vertrauenswürdig eingestuft werden. Andernfalls beendet der Client die Verbindung.

-   Sie müssen die Berechtigungen für den *privaten Zertifikatschlüssel* ändern, um den Zugriff durch den Server-App-V-Dienst zu aktivieren. Standardmäßig werden der App-V-Verwaltungs Server und die Streaming Server-Dienste unter dem Netzwerkdienstkonto ausgeführt. Wenn auf dem Server eine PKCS \ #10 generiert wird, wird ein privater Schlüssel erstellt. Nur die Gruppen lokales System und Administratoren können auf diesen Schlüssel zugreifen. Diese Standard-ACLs verhindern, dass der App-V-Server sichere Verbindungen akzeptiert.

    **Hinweis**  Informationen zum Konfigurieren einer Public Key-Infrastruktur (PKI) finden Sie unter <https://go.microsoft.com/fwlink/?LinkId=133229> ( https://go.microsoft.com/fwlink/?LinkId=133229) .

     

### Konfigurieren von IIS-Servern mit HTTPS

App-V kann IIS-Server in bestimmten Infrastrukturkonfigurationen verwenden. Weitere Informationen zum Konfigurieren von IIS-Servern finden Sie unter <https://go.microsoft.com/fwlink/?LinkId=133230> ( https://go.microsoft.com/fwlink/?LinkId=133230) .

**Hinweis**  Wenn Sie IIS zum Veröffentlichen der ICO-und OSD-Dateien verwenden, konfigurieren Sie einen MIME-Typ für OSD = txt; Andernfalls verweigert IIS die Bereitstellung der ICO-und OSD-Dateien für Clients.

 

### Sicherheit auf Anwendungsebene

Sie können die Server so konfigurieren, dass bestimmte Anwendungen auf dem Desktop eines Benutzers gestreamt werden. Die Zugriffsberechtigung wird jedoch tatsächlich auf Paketebene gewährt, nicht auf Anwendungsebene. Obwohl eine bestimmte Anwendung möglicherweise nicht auf dem Desktop des Benutzers veröffentlicht wird, wenn der Benutzer die Berechtigung zum Hinzufügen von Anwendungen hat oder ein Administrator auf dem Clientcomputer ist, kann der Benutzer eine Verknüpfung auf dem Client erstellen und verwenden, um alle Anwendungen in einem Paket auszuführen.

## Konfigurieren von App-V-Verwaltung für eine verteilte Umgebung


Wenn Sie die Infrastruktur für Ihre spezifische Organisation entwerfen, können Sie den App-v Management Web Service auf einem anderen Computer als dem Computer installieren, auf dem Sie den App-v-Verwaltungs Server installieren. Häufige Gründe für die Trennung dieser App-V-Komponenten sind die folgenden:

-   Leistung

-   Zuverlässigkeit

-   Verfügbarkeit

-   Skalierbarkeit

Damit die Infrastruktur ordnungsgemäß funktioniert, erfordert die Trennung der App-V-Verwaltungskonsole, des Verwaltungsservers und des Verwaltungs-Webdiensts eine zusätzliche Konfiguration. Detaillierte Informationen zum Konfigurieren des Servers finden Sie unter [Konfigurieren des Servers, der für die Delegierung als vertrauenswürdig eingestuft wird](how-to-configure-the-server-to-be-trusted-for-delegation.md).

## Verwandte Themen


[Planen der Sicherheit und von Schutzmaßnahmen](planning-for-security-and-protection.md)

 

 





