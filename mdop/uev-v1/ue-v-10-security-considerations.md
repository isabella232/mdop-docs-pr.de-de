---
title: Sicherheitsüberlegungen für UE-V 1.0
description: Sicherheitsüberlegungen für UE-V 1.0
author: dansimp
ms.assetid: c5cdf9ff-dc96-4491-98e9-0eada898ffe0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b503028ae327f92759fe0f64f33fe0cffc62b05c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810291"
---
# Sicherheitsüberlegungen für UE-V 1.0


Dieses Thema enthält eine kurze Übersicht über Konten und Gruppen, Protokolldateien und andere sicherheitsrelevante Überlegungen für Microsoft User Experience Virtualization (UE-V). Wenn Sie weitere Informationen wünschen, folgen Sie den Links, die hier bereitgestellt werden.

## Sicherheitsüberlegungen für die UE-V-Konfiguration


**Wenn Sie die Speicherfreigabe für Einstellungen erstellen, beschränken Sie den Freigabe Zugriff auf Benutzer, die Zugriff benötigen.**

Da Einstellungs Pakete personenbezogene Informationen enthalten können, sollten Sie darauf achten, diese so gut wie möglich zu schützen. Gehen Sie im Allgemeinen wie folgt vor:

-   Beschränken Sie die Freigabe auf die Benutzer, die Zugriff benötigen. Erstellen Sie eine Sicherheitsgruppe für Benutzer, die Ordner auf einer bestimmten Freigabe umgeleitet haben, und beschränken Sie den Zugriff auf diese Benutzer.

-   Wenn Sie die Freigabe erstellen, blenden Sie die Freigabe aus, indem Sie einen $ hinter den Freigabenamen setzen. Dadurch wird die Freigabe aus beiläufigen Browsern ausgeblendet, und die Freigabe wird in "meine Netzwerkumgebung" nicht angezeigt.

-   Gewähren Sie Benutzern nur die Mindestberechtigungen, die erforderlich sind. Die erforderlichen Berechtigungen werden in den folgenden Tabellen angezeigt.

    1.  Legen Sie die folgenden SMB-Berechtigungen (Freigabeebene) für den Ordner für die Einstellung des Speicherorts fest:

        <table>
        <colgroup>
        <col width="50%" />
        <col width="50%" />
        </colgroup>
        <thead>
        <tr class="header">
        <th align="left">Benutzerkonto</th>
        <th align="left">Empfohlene Berechtigungen</th>
        </tr>
        </thead>
        <tbody>
        <tr class="odd">
        <td align="left"><p>Jeder</p></td>
        <td align="left"><p>Keine Berechtigungen</p></td>
        </tr>
        <tr class="even">
        <td align="left"><p>Sicherheitsgruppe UE-V</p></td>
        <td align="left"><p>Vollzugriff</p></td>
        </tr>
        </tbody>
        </table>



~~~
2.  Set the following NTFS permissions for the settings storage location folder:

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">User account</th>
    <th align="left">Recommended permissions</th>
    <th align="left">Folder</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Creator/Owner</p></td>
    <td align="left"><p>No Permissions</p></td>
    <td align="left"><p>No Permissions</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Domain Admins</p></td>
    <td align="left"><p>Full Control</p></td>
    <td align="left"><p>This Folder, Subfolders and Files</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Security group of UE-V users</p></td>
    <td align="left"><p>List Folder/Read Data, Create Folders/Append Data</p></td>
    <td align="left"><p>This Folder Only</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Everyone</p></td>
    <td align="left"><p>Remove all Permissions</p></td>
    <td align="left"><p>No Permissions</p></td>
    </tr>
    </tbody>
    </table>



3.  Set the following share-level (SMB) permissions for the settings template catalog folder.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">User account</th>
    <th align="left">Recommend permissions</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Everyone</p></td>
    <td align="left"><p>No Permissions</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Domain Computers</p></td>
    <td align="left"><p>Read Permission Levels</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Administrators</p></td>
    <td align="left"><p>Read/Write Permission Levels</p></td>
    </tr>
    </tbody>
    </table>



4.  Set the following NTFS permissions for the settings template catalog folder.

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">User account</th>
    <th align="left">Recommended permissions</th>
    <th align="left">Apply to</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Creator/Owner</p></td>
    <td align="left"><p>Full Control</p></td>
    <td align="left"><p>This Folder, Subfolders and Files</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Domain Computers</p></td>
    <td align="left"><p>List Folder Contents and Read</p></td>
    <td align="left"><p>This Folder, Subfolders and Files</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Everyone</p></td>
    <td align="left"><p>No Permissions</p></td>
    <td align="left"><p>No Permissions</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Administrators</p></td>
    <td align="left"><p>Full Control</p></td>
    <td align="left"><p>This Folder, Subfolders and Files</p></td>
    </tr>
    </tbody>
    </table>
~~~



### Verwenden von Servern mit Windows Server 2003 oder höher zum Hosten umgeleiteter Dateifreigaben

Benutzereinstellungen-Paketdateien enthalten persönliche Informationen, die zwischen dem Clientcomputer und dem Server, auf dem die Einstellungs Pakete gespeichert sind, übertragen werden. Aus diesem Grund sollten Sie sicherstellen, dass die Daten geschützt sind, während Sie über das Netzwerk transportiert werden.

Benutzereinstellungsdaten sind anfällig für diese potenziellen Bedrohungen: Abfangen der Daten, die über das Netzwerk geleitet werden. Manipulation der Daten bei der über das Netzwerk übertragenen Daten; und Spoofing des Servers, der die Daten hostet.

Verschiedene Features von Windows Server 2003 und höher können dazu beitragen, Benutzerdaten zu schützen:

-   **Kerberos** -Kerberos ist in allen Versionen von Windows 2000 und Windows Server 2003 und höher Standard. Kerberos gewährleistet die höchste Sicherheitsstufe für Netzwerkressourcen. NTLM authentifiziert nur den Client; Kerberos authentifiziert den Server und den Client. Wenn NTLM verwendet wird, weiß der Client nicht, ob der Server gültig ist. Dies ist besonders wichtig, wenn der Client persönliche Dateien mit dem Server austauscht, wie dies bei Roaming-Profilen der Fall ist. Kerberos bietet eine bessere Sicherheit als NTLM. Kerberos steht unter Windows NT, Version 4,0 oder früheren Betriebssystemen, nicht zur Verfügung.

-   **IPSec** – das IP-Sicherheitsprotokoll (IPSec) bietet Authentifizierung auf Netzwerkebene, Datenintegrität und Verschlüsselung. IPSec stellt Folgendes sicher:

    -   Roaming-Daten sind während der Weiterleitung sicher vor Datenänderungen.

    -   Roaming-Daten sind sicher vor dem Abfangen, anzeigen oder kopieren.

    -   Auf Roaming-Daten kann nicht authentifizierte Personen zugreifen.

-   **SMB-Signierung** : das SMB-Authentifizierungsprotokoll (Server Message Block) unterstützt die Nachrichtenauthentifizierung, die eine aktive Nachricht und "man-in-the-Middle"-Angriffe verhindert. Die SMB-Signierung bietet diese Authentifizierung, indem eine digitale Signatur in jedem SMB platziert wird. Die digitale Signatur wird dann sowohl vom Client als auch vom Server überprüft. Um die SMB-Signierung verwenden zu können, müssen Sie Sie zuerst entweder aktivieren oder auf dem SMB-Client und dem SMB-Server anfordern. Beachten Sie, dass bei der SMB-Signierung eine Leistungs Verhängung erzwungen wird. Sie verbraucht keine Netzwerkbandbreite, beansprucht aber mehr CPU-Zyklen auf Client-und Serverseite.

### Verwenden Sie immer das NTFS-Dateisystem für Volumes, in denen Benutzerdaten gespeichert sind.

Konfigurieren Sie für die sicherste Konfiguration Server, die die UE-V-Einstellungsdateien hosten, um das NTFS-Datei System zu verwenden. Im Gegensatz zu FAT unterstützt NTFS Discretionary Access Control Lists (DACLs) und System Access Control Lists (SACLs). DACLs und SACLs steuern, wer Vorgänge für eine Datei ausführen kann und welche Ereignisse die Protokollierung von Aktionen auslösen, die für eine Datei ausgeführt werden.

### <a href="" id="do-not-rely-on-efs-to-encrypt-users--files-when-transmitted-over-the-network"></a>Verlassen Sie sich nicht auf EFS, um die Dateien von Benutzern zu verschlüsseln, wenn Sie über das Netzwerk gesendet werden.

Wenn Sie EFS (Encrypting File System) zum Verschlüsseln von Dateien auf einem Remoteserver verwenden, werden die verschlüsselten Daten während der Übertragung über das Netzwerk nicht verschlüsselt. Sie wird nur verschlüsselt, wenn Sie auf einem Datenträger gespeichert ist.

Die Ausnahmen sind, wenn Ihr System IPSec (Internet Protocol Security) oder WebDAV (Web Distributed Authoring and Versioning) umfasst. IPSec verschlüsselt Daten, während Sie über ein TCP/IP-Netzwerk transportiert werden. Wenn die Datei verschlüsselt ist, bevor Sie kopiert oder in einen WebDAV-Ordner auf einem Server verschoben wird, bleibt Sie während der Übertragung verschlüsselt und wird auf dem Server gespeichert.

### Verschlüsseln des Offline Dateicaches

Standardmäßig ist der Cache für Offline Dateien durch ACLs auf NTFS-Partitionen geschützt, aber durch die Verschlüsselung des Caches wird die Sicherheit auf einem lokalen Computer weiter verbessert. Standardmäßig ist der Cache auf dem lokalen Computer nicht verschlüsselt, sodass alle im Netzwerk zwischengespeicherten verschlüsselten Dateien auf dem lokalen Computer nicht verschlüsselt sind. Dies kann in einigen Umgebungen ein Sicherheitsrisiko darstellen.

Wenn die Verschlüsselung aktiviert ist, werden alle Dateien im Offline Dateicache verschlüsselt. Dies umfasst das Verschlüsseln vorhandener Dateien sowie von Dateien, die später hinzugefügt werden. Die zwischengespeicherte Kopie auf dem lokalen Computer ist betroffen, die zugehörige Netzwerkkopie jedoch nicht.

Der Cache kann auf eine von zwei Arten verschlüsselt werden:

1.  Über Gruppenrichtlinien. – Aktivieren Sie im Gruppenrichtlinien-Editor die Einstellung **Offline Datei-Cache verschlüsseln** , die sich auf Computer Configuration\\Administrative Templates\\Network\\Offline-Dateien befindet.

2.  Manuell. – Wählen Sie im Windows-Explorer im Befehlsmenü Extras und dann Ordneroptionen aus. Wählen Sie die Registerkarte Offlinedateien aus, und aktivieren Sie dann das Kontrollkästchen **Offlinedateien zum Sichern von Daten verschlüsseln** .

### Der UE-V-Agent soll Ordner für jeden Benutzer erstellen

Um sicherzustellen, dass UE-v optimal funktioniert, erstellen Sie nur die Stammfreigabe auf dem Server, und lassen Sie den UE-v-Agent die Ordner für jeden Benutzer erstellen. In UE-V werden diese Benutzerordner mit der entsprechenden Sicherheit erstellt.

Diese Berechtigungskonfiguration ermöglicht Benutzern das Erstellen von Ordnern für den Einstellungsspeicher. Der UE-V-Agent erstellt und sichert einen settingspackage-Ordner, während er im Kontext des Benutzers ausgeführt wird. Der Benutzer erhält Vollzugriff auf seinen settingspackage-Ordner. Andere Benutzer erben keinen Zugriff auf diesen Ordner. Es ist nicht erforderlich, einzelne Benutzerverzeichnisse zu erstellen und zu sichern. Dies erfolgt automatisch durch den Agenten, der im Kontext des Benutzers ausgeführt wird.

**Hinweis:**  
Zusätzliche Sicherheit kann konfiguriert werden, wenn ein Windows-Server für die Speicherfreigabe "Einstellungen" verwendet wird. UE-V kann so konfiguriert werden, dass entweder die Gruppe des lokalen Administrators oder der aktuelle Benutzer der Besitzer des Ordners ist, in dem die Einstellungs Pakete gespeichert sind. Verwenden Sie den folgenden Befehl, um zusätzliche Sicherheit zu aktivieren:

1.  Fügen Sie einen Registrierungsschlüssel "reg \ _DWORD" mit dem Namen "RepositoryOwnerCheckEnabled" hinzu `HKEY_LOCAL_MACHINE\Software\Microsoft\UEV\Agent\Configuration` .

2.  Stellen Sie den Registrierungsschlüsselwert auf 1 ein.

Wenn diese Konfigurationseinstellung eingerichtet ist, überprüft der UE-V-Agent, ob die Gruppe des lokalen Administrators oder der aktuelle Benutzer der Besitzer des settingspackage-Ordners ist. Wenn dies nicht der Fall ist, ermöglicht der UE-V-Agent keinen Zugriff auf den Ordner.



Wenn Sie Ordner für die Benutzer erstellen müssen, und stellen Sie sicher, dass Sie die richtigen Berechtigungen festzulegen.

Wir empfehlen dringend, dass Sie keine Ordner vorerstellen und stattdessen dem UE-V-Agent das Erstellen des Ordners für den Benutzer gestatten.

### <a href="" id="ensure-that-correct-permissions-are-set-when-storing-ue-v-settings-in-a-user-s-home-directory"></a>Sicherstellen, dass die richtigen Berechtigungen beim Speichern der UE-V-Einstellungen im Basisverzeichnis eines Benutzers festgesetzt werden

Wenn Sie die UE-V-Einstellungen in das private Verzeichnis eines Benutzers umleiten, stellen Sie sicher, dass die Berechtigungen für das private Verzeichnis des Benutzers für Ihre Organisation entsprechend festgesetzt sind.

## Verwandte Themen


[Sicherheit und Datenschutz für UE-V 1.0](security-and-privacy-for-ue-v-10.md)









