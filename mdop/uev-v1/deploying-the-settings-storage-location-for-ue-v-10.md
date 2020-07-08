---
title: Bereitstellen des Speicherorts für die Einstellungen für UE-V 1.0
description: Bereitstellen des Speicherorts für die Einstellungen für UE-V 1.0
author: dansimp
ms.assetid: b187d44d-649b-487e-98d3-a61ee2be8c2f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c179be0882bc6a0efc0f11f21fc231f03b63b0fe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811875"
---
# Bereitstellen des Speicherorts für die Einstellungen für UE-V 1.0


Die Bereitstellung von Microsoft User Experience Virtualization (UE-V) erfordert einen Speicherort für Einstellungen, in dem die Benutzereinstellungen in einer Einstellungspaket Datei gespeichert sind. Der Speicherort für Einstellungen kann auf eine der folgenden zwei Arten konfiguriert werden:

-   **Active Directory-Basisverzeichnis** – wenn für den Benutzer in Active Directory ein Home-Verzeichnis definiert ist, verwendet der UE-V-Agent diesen Speicherort zum Speichern von Einstellungen für Standort Pakete. Der UE-V-Agent erstellt dynamisch den benutzerspezifischen Speicherordner unter dem Stammverzeichnis des Basisverzeichnisses. Der Agent verwendet nur das Home-Verzeichnis des Active Directory, wenn kein Speicherort für Einstellungen festgelegt ist.

-   **Erstellen einer Speicherfreigabe für Einstellungen** – die Speicherfreigabe für Einstellungen ist eine standardmäßige Netzwerkfreigabe, auf die UE-V-Benutzer zugreifen können.

## Bereitstelleneiner Speicherfreigabe für UE-V-Einstellungen


Wenn Sie die Speicherfreigabe für Einstellungen erstellen, sollten Sie den Zugriff nur auf Benutzer beschränken, die Zugriff benötigen. Die erforderlichen Berechtigungen werden in den folgenden Tabellen angezeigt.

**So stellen Sie die UE-V-Netzwerkfreigabe bereit**

1.  Erstellen Sie eine neue Sicherheitsgruppe für UE-V-Benutzer.

2.  Erstellen Sie einen neuen Ordner auf dem zentral gelegenen Computer, auf dem die UE-v-Einstellungs Pakete gespeichert werden, und erteilen Sie den UE-v-Benutzern dann Gruppen Berechtigungen für den Ordner. Der Administrator, der UE-V unterstützt, benötigt Berechtigungen für diesen freigegebenen Ordner.

3.  Legen Sie die folgenden SMB-Berechtigungen (Freigabeebene) für den Ordner für die Einstellung des Speicherorts fest:

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong>Benutzerkonto</strong></th>
    <th align="left"><strong>Empfohlene Berechtigungen</strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Jeder</p></td>
    <td align="left"><p>Keine Berechtigungen</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Sicherheitsgruppe der UE-V-Benutzer</p></td>
    <td align="left"><p>Vollzugriff</p></td>
    </tr>
    </tbody>
    </table>

     

4.  Legen Sie die folgenden NTFS-Berechtigungen für den Ordner "Settings Storage Location":

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong>Benutzerkonto</strong></th>
    <th align="left"><strong>Empfohlene Berechtigungen</strong></th>
    <th align="left"><strong>Ordner</strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Ersteller/Besitzer</p></td>
    <td align="left"><p>Vollzugriff</p></td>
    <td align="left"><p>Nur Unterordner und Dateien</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Sicherheitsgruppe der UE-V-Benutzer</p></td>
    <td align="left"><p>Ordner auflisten/Daten lesen, Ordner erstellen/Daten anfügen</p></td>
    <td align="left"><p>Nur diesen Ordner</p></td>
    </tr>
    </tbody>
    </table>

     

5.  Klicken Sie auf **OK** , um die Dialogfelder zu schließen.

Diese Berechtigungskonfiguration ermöglicht Benutzern das Erstellen von Ordnern für den Einstellungsspeicher. Der UE-V-Agent erstellt und sichert einen `settingspackage` Ordner, während er im Kontext des Benutzers ausgeführt wird. Der Benutzer erhält die vollständige Kontrolle über seinen `settingspackage` Ordner. Andere Benutzer erben keinen Zugriff auf diesen Ordner. Es ist nicht erforderlich, einzelne Benutzerverzeichnisse zu erstellen und zu sichern, da dies automatisch vom Agent erfolgt, der im Kontext des Benutzers ausgeführt wird.

**Hinweis**  Zusätzliche Sicherheit kann konfiguriert werden, wenn ein Windows-Server für die Speicherfreigabe "Einstellungen" verwendet wird. UE-V kann so konfiguriert werden, dass entweder die Gruppe des lokalen Administrators oder der aktuelle Benutzer der Besitzer des Ordners ist, in dem die Einstellungs Pakete gespeichert sind. Führen Sie die folgenden Schritte aus, um zusätzliche Sicherheit zu aktivieren:

1.  Fügen Sie einen Registrierungsschlüssel " **reg \ _DWORD** " mit dem Namen "RepositoryOwnerCheckEnabled" zu **HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\uev\\agent\\configuration.**

2.  Stellen Sie den Registrierungsschlüsselwert auf 1 ein.

 

## Verwandte Themen


[Bereitstellen von UE-V 1.0](deploying-ue-v-10.md)

[Unterstützte Konfigurationen für UE-V 1.0](supported-configurations-for-ue-v-10.md)

Bereitstellen des zentralen Speichers für die Einstellungen für Benutzeroberflächen-Virtualisierungs-Vorlagen und-Einstellungen Pakete [beim Installieren des UE-V-Generators](installing-the-ue-v-generator.md)

[Bereitstellen von UE-V-Agent](deploying-the-ue-v-agent.md)

 

 





