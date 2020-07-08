---
title: Sicherheitsüberlegungen für UE-V 2.x
description: Sicherheitsüberlegungen für UE-V 2.x
author: dansimp
ms.assetid: 9d5c3cae-9fcb-4dea-bd67-741b3dea63be
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 8e24e9e37de11053663bb90974fabf2ff369aeca
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810690"
---
# Sicherheitsüberlegungen für UE-V 2.x


Dieses Thema enthält eine kurze Übersicht über Konten und Gruppen, Protokolldateien und andere sicherheitsrelevante Überlegungen für Microsoft User Experience Virtualization (UE-V) 2,0, 2,1 und 2,1 SP1. Wenn Sie weitere Informationen wünschen, folgen Sie den Links, die hier bereitgestellt werden.

## Sicherheitsüberlegungen für die UE-V-Konfiguration


**Wichtig**  Wenn Sie die Speicherfreigabe für Einstellungen erstellen, beschränken Sie den Freigabe Zugriff auf Benutzer, die Zugriff benötigen.

 

Da Einstellungs Pakete persönliche Informationen enthalten können, sollten Sie darauf achten, Sie so gut wie möglich zu schützen. Gehen Sie im Allgemeinen wie folgt vor:

-   Beschränken Sie die Freigabe auf die Benutzer, die Zugriff benötigen. Erstellen Sie eine Sicherheitsgruppe für Benutzer, die Ordner auf einer bestimmten Freigabe umgeleitet haben, und beschränken Sie den Zugriff auf diese Benutzer.

-   Wenn Sie die Freigabe erstellen, blenden Sie die Freigabe aus, indem Sie einen $ hinter den Freigabenamen setzen. Dieser Zusatz blendet die Freigabe aus beiläufigen Browsern aus, und die Freigabe ist in "meine Netzwerkumgebung" nicht sichtbar.

-   Gewähren Sie Benutzern nur die Mindestberechtigungen, die Sie benötigen. In den folgenden Tabellen werden die erforderlichen Berechtigungen angezeigt.

    1.  Legen Sie die folgenden SMB-Berechtigungen auf Freigabeebene für den Ordner für das Festlegen des Speicherorts fest.

        | Benutzerkonto | Empfohlene Berechtigungen |
        | - | - |
        | Jeder | Keine Berechtigungen |
        |Sicherheitsgruppe UE-V | Vollzugriff |

    2.  Legen Sie die folgenden NTFS-Dateisystemberechtigungen für den Ordner "Settings Storage Location" ein.

        | Benutzerkonto | Empfohlene Berechtigungen | Ordner |
        | - | - | - |
        | Ersteller/Besitzer | Vollzugriff | Nur Unterordner und Dateien|
        | Domänenadministratoren | Vollzugriff | Dieser Ordner, Unterordner und Dateien |
        | Sicherheitsgruppe der UE-V-Benutzer | Ordner auflisten/Daten lesen, Ordner erstellen/Daten anfügen | Nur diesen Ordner |
        | Jeder | Entfernen aller Berechtigungen | Keine Berechtigungen |

    3.  Legen Sie die folgenden SMB-Berechtigungen auf Freigabeebene für den Ordner "Einstellungs Vorlagenkatalog" ein.

        | Benutzerkonto | Berechtigungen empfehlen |
        | - | - |
        | Jeder | Keine Berechtigungen |
        | Domänencomputer | Lesen von Berechtigungsstufen |
        | Administratoren | Berechtigungsstufen für Lesen/Schreiben |
         
    4.  Legen Sie die folgenden NTFS-Berechtigungen für den Katalogordner "Settings" (Einstellungen).

        | Benutzerkonto | Empfohlene Berechtigungen | Anwenden auf |
        | - | - | - |
        | Ersteller/Besitzer | Vollzugriff | Dieser Ordner, Unterordner und Dateien |
        | Domänencomputer | Listen Ordnerinhalte und Leseberechtigungen | Dieser Ordner, Unterordner und Dateien|
        | Jeder| Keine Berechtigungen| Keine Berechtigungen|
        | Administratoren| Vollzugriff| Dieser Ordner, Unterordner und Dateien|

### Verwenden von Windows Server ab windowsserver2003 zum Hosten umgeleiteter Dateifreigaben

Benutzereinstellungen-Paketdateien enthalten persönliche Informationen, die zwischen dem Clientcomputer und dem Server, auf dem die Einstellungs Pakete gespeichert sind, übertragen werden. Aufgrund dieses Prozesses sollten Sie sicherstellen, dass die Daten geschützt sind, während Sie über das Netzwerk transportiert werden.

Die Daten der Benutzereinstellungen sind anfällig für diese potenziellen Bedrohungen: Abfangen der Daten bei der Überführung über das Netzwerk, manipulieren der Daten bei der Überführung über das Netzwerk und Spoofing des Servers, auf dem die Daten gehostet werden.

Ab Windows Server2003 können verschiedene Features des Windows Server-Betriebssystems beim Sichern von Benutzerdaten helfen:

-   **Kerberos** -Kerberos ist in allen Versionen von Microsoft Windows2000Server und Windows Server, beginnend mit WindowsServer2003, Standard. Kerberos gewährleistet die höchste Sicherheitsstufe für Netzwerkressourcen. NTLM authentifiziert nur den Client; Kerberos authentifiziert den Server und den Client. Wenn NTLM verwendet wird, weiß der Client nicht, ob der Server gültig ist. Dieser Unterschied ist besonders wichtig, wenn der Client persönliche Dateien mit dem Server austauscht, wie dies bei Roaming-Benutzerprofilen der Fall ist. Kerberos bietet eine bessere Sicherheit als NTLM. Kerberos steht auf dem Betriebssystem Microsoft WindowsNTServer 4,0 oder früheren Versionen nicht zur Verfügung.

-   **IPSec** – das IP-Sicherheitsprotokoll (IPSec) bietet Authentifizierung auf Netzwerkebene, Datenintegrität und Verschlüsselung. IPSec stellt Folgendes sicher:

    -   Roamingdaten sind sicher vor Datenänderungen, während Daten unterwegs sind.

    -   Roaming-Daten sind sicher vor dem Abfangen, anzeigen oder kopieren.

    -   Roaming-Daten sind von nicht authentifizierten Personen sicher vor dem Zugriff.

-   **SMB-Signierung** : das SMB-Authentifizierungsprotokoll (Server Message Block) unterstützt die Nachrichtenauthentifizierung, wodurch aktive Nachrichten und "man-in-the-Middle"-Angriffe verhindert werden. Die SMB-Signierung bietet diese Authentifizierung, indem eine digitale Signatur in jedem SMB platziert wird. Die digitale Signatur wird dann sowohl vom Client als auch vom Server überprüft. Um die SMB-Signierung verwenden zu können, müssen Sie Sie zunächst entweder aktivieren oder auf dem SMB-Client und dem SMB-Server anfordern. Beachten Sie, dass bei der SMB-Signierung eine Leistungs Verhängung erzwungen wird. Sie verbraucht keine Netzwerkbandbreite, beansprucht aber mehr CPU-Zyklen auf Client-und Serverseite.

### Verwenden Sie immer das NTFS-Dateisystem für Volumes, die Benutzerdaten enthalten.

Konfigurieren Sie für die sicherste Konfiguration Server, die die UE-V-Einstellungsdateien hosten, um das NTFS-Dateisystem zu verwenden. Im Gegensatz zum FAT-Dateisystem unterstützt NTFS Discretionary Access Control Lists (DACLs) und System Access Control Lists (SACLs). DACLs und SACLs steuern, wer Vorgänge für eine Datei ausführen kann und welche Ereignisse die Protokollierung von Aktionen auslösen, die für eine Datei ausgeführt werden.

### Verlassen Sie sich nicht auf EFS, um Benutzer Dateien zu verschlüsseln, wenn Sie über das Netzwerk übertragen werden.

Wenn Sie das verschlüsselnde Datei System (Encrypting File System, EFS) zum Verschlüsseln von Dateien auf einem Remoteserver verwenden, werden die verschlüsselten Daten während der Übertragung über das Netzwerk nicht verschlüsselt. Sie wird nur verschlüsselt, wenn Sie auf einem Datenträger gespeichert ist.

Dieser Verschlüsselungsprozess trifft nicht zu, wenn Ihr System IPSec (Internet Protocol Security) oder WebDAV (Web Distributed Authoring and Versioning) umfasst. IPSec verschlüsselt Daten, während Sie über ein TCP/IP-Netzwerk transportiert werden. Wenn die Datei verschlüsselt ist, bevor Sie in einen WebDAV-Ordner auf einem Server kopiert oder verschoben wird, bleibt Sie während der Übertragung verschlüsselt und wird auf dem Server gespeichert.

### Der UE-V-Agent soll Ordner für jeden Benutzer erstellen

Um sicherzustellen, dass UE-v optimal funktioniert, erstellen Sie nur die Stammfreigabe auf dem Server, und lassen Sie den UE-v-Agent die Ordner für jeden Benutzer erstellen. UE-V erstellt diese Benutzerordner mit der entsprechenden Sicherheit.

Diese Berechtigungskonfiguration ermöglicht Benutzern das Erstellen von Ordnern für den Einstellungsspeicher. Der UE-V-Agent erstellt und sichert einen Ordner für Einstellungs Pakete, während er im Kontext des Benutzers ausgeführt wird. Die Benutzer erhalten Vollzugriff auf den Ordner mit den Einstellungen des Pakets. Andere Benutzer erben keinen Zugriff auf diesen Ordner. Sie müssen keine einzelnen Benutzerverzeichnisse erstellen und sichern. Der Agent, der im Kontext des Benutzers ausgeführt wird, führt ihn automatisch aus.

**Hinweis**  Zusätzliche Sicherheit kann konfiguriert werden, wenn ein Windows-Server für die Einstellungen Speicherfreigabe verwendet wird. UE-V kann so konfiguriert werden, dass entweder die lokale Gruppe Administratoren oder der aktuelle Benutzer der Besitzer des Ordners ist, in dem die Einstellungs Pakete gespeichert sind. Verwenden Sie den folgenden Befehl, um zusätzliche Sicherheit zu aktivieren:

1.  Fügen Sie dem Registrierungsschlüssel "reg \ _DWORD" RepositoryOwnerCheckEnabled `HKEY_LOCAL_MACHINE\Software\Microsoft\UEV\Agent\Configuration` .

2.  Stellen Sie den Wert für den Registrierungsschlüssel auf *1 ein*.

Wenn diese Konfigurationseinstellung eingerichtet ist, überprüft der UE-V-Agent, ob die lokale Gruppe Administratoren oder der aktuelle Benutzer der Besitzer des Ordners Einstellungen-Paket ist. Wenn dies nicht der Fall ist, gewährt der UE-V-Agent keinen Zugriff auf den Ordner.

 

Wenn Sie Ordner für die Benutzer erstellen müssen, stellen Sie sicher, dass Sie über die richtigen Berechtigungen verfügen.

Wir empfehlen dringend, dass Sie keine Ordner vorab erstellen. Lassen Sie stattdessen den UE-V-Agent den Ordner für den Benutzer erstellen.

### Sicherstellen, dass die Berechtigungen zum Speichern der UE-V 2-Einstellungen in einem privaten Verzeichnis oder in einem benutzerdefinierten Verzeichnis korrekt sind

Wenn Sie die UE-V-Einstellungen in das private Verzeichnis eines Benutzers oder ein benutzerdefiniertes Active Directory (AD)-Verzeichnis umleiten, stellen Sie sicher, dass die Berechtigungen für das Verzeichnis für Ihre Organisation entsprechend festgesetzt sind.






## Verwandte Themen


[Technische Referenz für UE-V 2.x](technical-reference-for-ue-v-2x-both-uevv2.md)

 

 





