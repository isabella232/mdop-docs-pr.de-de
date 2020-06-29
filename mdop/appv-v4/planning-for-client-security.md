---
title: Planen der Clientsicherheit
description: Planen der Clientsicherheit
author: dansimp
ms.assetid: 4840a60f-4c91-489c-ad0b-6671882abf9b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: e0038f7cbc8592d6c7fcdfa485111da88c17791d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806504"
---
# Planen der Clientsicherheit


Der App-V-Client bietet mehrere Sicherheitsverbesserungen, die in früheren Versionen des Produkts nicht vorhanden waren. Diese Änderungen stellen eine verbesserte Sicherheit nach der Installation und durch eine spätere Konfiguration der Clienteinstellungen dar. In diesem Thema werden einige dieser Verbesserungen beschrieben, und es werden mehrere wichtige sicherheitsrelevante Konfigurationseinstellungen aufgeführt, die Sie während des Planungsprozesses berücksichtigen sollten. Beachten Sie, dass virtuelle Anwendungen weiterhin ausführbar sind, sodass Sie sicherstellen müssen, dass diese Ressourcen nicht von unbefugten Personen manipuliert werden können. Aus diesem Grund wird der OSD-Dateicache (Open Software Descriptor) wie weiter unten in diesem Thema beschrieben geschützt, und es wird dringend empfohlen, RTSPS, HTTPS und IPSec zu verwenden, um die Veröffentlichung und das Streaming zu schützen.

## App-V-Client Sicherheit


Standardmäßig ist bei der Installation der App-V-Client mit den erforderlichen Mindestberechtigungen konfiguriert, damit ein Benutzer eine Veröffentlichungsaktualisierung durchführen und Anwendungen starten kann. Zu den anderen im App-V-Client bereitgestellten Sicherheitsverbesserungen gehören die folgenden:

-   Standardmäßig kann der OSD-Dateicache nur von Administratoren und mithilfe des Veröffentlichungs Aktualisierungsprozesses aktualisiert werden.

-   Auf die Protokolldatei (sftlog.txt) kann nur von Konten mit lokalem Administratorzugriff auf den Client zugegriffen werden.

-   Die Protokolldatei hat nun eine maximale Größe.

### Dateitypzuordnungen

Standardmäßig registriert die Installation des Clients die Dateitypen Zuordnungen (FTA) für OSD-Dateien, sodass Benutzer Anwendungen direkt aus OSD-Dateien anstelle der veröffentlichten Tastenkombinationen starten können. Wenn ein Benutzer mit lokalen Administratorrechten eine OSD-Datei mit Schadcode erhält, entweder per e-Mail oder von einer Website heruntergeladen, kann der Benutzer die OSD-Datei öffnen und die Anwendung starten, selbst wenn der Client so eingestellt ist, dass die Berechtigung zum **Hinzufügen von Anwendungen** eingeschränkt wird. Um dieses Risiko zu verringern, können Sie die Registrierung der FTA für das OSD-Konto aufheben. Darüber hinaus können Sie diese Erweiterung im e-Mail-System und der Firewall blockieren. Weitere Informationen zum Konfigurieren von Outlook zum Blockieren von Erweiterungen finden Sie unter <https://go.microsoft.com/fwlink/?LinkId=133278> .

**Sicherheitshinweis:**

Beginnend mit App-v, Version 4.6, wird die Dateitypzuordnung nicht mehr für OSD-Dateien während einer neuen Installation des Clients erstellt, obwohl die vorhandenen Einstellungen während eines Upgrades von Version 4,2 oder 4,5 des App-V-Clients beibehalten werden. Wenn Sie aus irgendeinem Grund unbedingt die Dateitypzuordnung erstellen müssen, können Sie die folgenden Registrierungsschlüssel erstellen und ihre Werte wie gezeigt einstellen:

    Create HKEY\_CLASSES\_ROOT\\.osd with a default value of SoftGrid.osd.File

    Under HKEY\_LOCAL\_MACHINE\\software\\classes\\Softgrid.osd.file, create a string value named AppUserModelID with a data value of Microsoft.AppV.Client.Tray

### Autorisierung

Während der Installation können Sie den **RequireAuthorizationIfCached** -Parameter verwenden, um den Client so zu konfigurieren, dass eine Autorisierung vom Server erforderlich ist, wenn der Benutzer versucht, eine Anwendung zu starten. Sie sollten sorgfältig überlegen, wie Sie diesen Parameter einstellen. Wenn der App-V-Server aus irgendeinem Grund nicht verfügbar ist, verwendet die Anwendung den zuletzt gespeicherten Zustand dieses Parameters, um den Benutzer Zugriff auf die Anwendung zu steuern. Wenn der Benutzer die Anwendung nicht erfolgreich gestartet hat, bevor der App-V-Server nicht mehr verfügbar ist, können Sie die Anwendung erst starten, nachdem Sie mit dem Server kommunizieren und die Autorisierung empfangen kann. Wenn Sie den Parameter jedoch so festlegen, dass der Client keine Autorisierung erfordert und der Server nicht verfügbar ist, können alle zuvor zwischengespeicherten Anwendungen gestartet werden, ob Sie autorisiert sind oder nicht. Wenn der Benutzer die Berechtigung hat, den Client zu ändern, um über Berechtigungen in den Offline Modus zu wechseln, oder wenn der Benutzer ein lokaler Administrator ist, kann der Benutzer alle zwischengespeicherten Pakete öffnen, als ob die App-V-Infrastruktur nicht verfügbar war.

### Antivirus-Scans

Antivirensoftware, die auf einem App-V-Client Computer ausgeführt wird, kann eine infizierte Datei in der virtuellen Umgebung erkennen und melden. Die Datei kann jedoch nicht desinfiziert werden. Wenn ein Virus in der virtuellen Umgebung erkannt wird, würde die Antivirensoftware den konfigurierten Quarantäne-oder Reparaturvorgang im Cache durchführen, nicht im eigentlichen Paket. Konfigurieren Sie die Antivirensoftware mit einer Ausnahme für die Datei "sftfs. FSD". Diese Datei ist die Cache-Datei, in der Pakete auf dem App-V-Client gespeichert werden.

**Sicherheitshinweis:**

Wenn ein Virus in einer Anwendung oder einem Paket, das in der Produktionsumgebung bereitgestellt wird, erkannt wird, ersetzen Sie die Anwendung oder das Paket durch eine virusfreie Version.

## Kommunikation zwischen Client und Server


Veröffentlichungs Aktualisierungen und Paketstreaming sind auch Bereiche, in denen Sicherheitsüberlegungen in Bezug auf die Client-Server-Kommunikation wichtig sind.

### Veröffentlichungsaktualisierung

Wenn der Client mit dem Server kommuniziert, um eine Veröffentlichungsaktualisierung durchzuführen, verwendet er die Anmeldeinformationen des angemeldeten Benutzers, um Informationen zu den Anwendungspaketen anzufordern. Sie sollten die Kommunikation zwischen dem App-v-Client und dem App-v-Verwaltungs Server sichern, um sicherzustellen, dass keine Veröffentlichungsinformationen bei der Übertragung manipuliert werden können. Dies erfolgt mithilfe der erweiterten Sicherheitsoption, bei der RTSPS/HTTPS verwendet werden. Die Kommunikation zwischen dem Client und dem Speicherort, an dem die ICO-und OSD-Dateien gespeichert sind, sollte IPSec für SMB/CIFS-Freigaben und HTTPS für einen IIS-Server verwenden.

**Hinweis**  Wenn Sie IIS zum Veröffentlichen der ICO-und OSD-Dateien verwenden, konfigurieren Sie einen MIME-Typ für OSD = txt; Andernfalls verweigert IIS die Bereitstellung der ICO-und OSD-Dateien für Clients.

 

### Paket Streaming

Wenn ein Benutzer zum ersten Mal eine Anwendung startet oder wenn Parameter für das automatische Laden auf dem Client eingestellt wurden, wird das Anwendungspaket von einem Server an den Clientcache gestreamt. Dieser Prozess unterstützt die Protokolle RTSP/RTSPS, HTTP/HTTPS und SMB/CIFS. Die OSD-Dateien steuern, welche Protokolle verwendet werden, es sei denn, die **ApplicationSourceRoot** -oder **OVERRIDEURL** -Einstellung wurde auf den Clients konfiguriert. Sie sollten die Kommunikation so konfigurieren, dass Sie über RTSPS, HTTPS oder IPSec für SMB/CIFS erfolgt, um ein höheres Sicherheitsniveau zu erreichen. Weitere Informationen zum Auswählen der zu verwendenden Kommunikationsmethode finden Sie im App-V-Handbuch zur Planung und Bereitstellung unter <https://go.microsoft.com/fwlink/?LinkId=122063> .

**Hinweis**  Wenn Sie IIS zum Veröffentlichen von Paketen (SFT-Dateien) verwenden, konfigurieren Sie einen MIME-Typ für SFT = Binary; Andernfalls verweigert IIS die Bereitstellung der SFT-Dateien für Clients.

 

### Roaming-Profile und Ordnerumleitung

Das App-V-System speichert benutzerspezifische Änderungen an Paketen in der usrvol \ _sftfs \ _V1. pkg-Datei. Diese Datei befindet sich im Ordner "Anwendungsdaten" des Profils eines Benutzers. Da das Profil oder ein umgeleiteter Anwendungsdatenordner zwischen dem Client und dem Server übertragen wird, verwenden Sie IPSec, um die Kommunikation zu sichern.

## Überlegungen für mit dem Internet verbundene Clients


Für mit dem Internet verbundene Clients ist es wichtig zu prüfen, ob der Client der Domäne beigetreten ist oder nicht der Domäne beigetreten ist.

### Domäne, die dem Client beigetreten ist

Standardmäßig verwenden App-V-Clients Kerberos-Tickets, die von Active Directory-Domänendiensten für die Authentifizierung und Autorisierung im Intranet ausgestellt wurden. Diese Kerberos-Tickets sind standardmäßig 10 Stunden gültig. Der Client verwendet dieses Ticket für den Zugriff auf den App-V-Server, solange das Ticket gültig ist, auch wenn der Computer keine Verbindung mit dem Domänencontroller herstellen kann, um das Ticket zu aktualisieren. Wenn das Kerberos-Ticket abläuft, wird der App-V-Client zur NTLM-Authentifizierung zurückkehren und die zwischengespeicherten Anmeldeinformationen des Benutzers verwenden.

### Client, der nicht der Domäne angehört

Wenn ein Benutzer Home-Based ist und der Computer nicht der Unternehmensdomäne beigetreten ist, kann App-V weiterhin die Bereitstellung von Anwendungen unterstützen. Wenn Sie einen Benutzer authentifizieren und autorisieren möchten, um eine Veröffentlichungsaktualisierung durchzuführen und Anwendungen zu starten, konfigurieren Sie das Benutzerkonto auf dem Clientcomputer, um den Benutzernamen und das Kennwort für den Zugriff auf die App-V-Umgebung zu speichern und die entsprechenden Berechtigungen für die Anwendungen bereitzustellen.

## Verwandte Themen


[Planen der Sicherheit und von Schutzmaßnahmen](planning-for-security-and-protection.md)

 

 





