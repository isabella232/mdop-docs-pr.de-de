---
title: Bereitstellen des Katalogs für Einstellungsvorlagen für UE-V 1.0
description: Bereitstellen des Katalogs für Einstellungsvorlagen für UE-V 1.0
author: dansimp
ms.assetid: 0e6ab5ef-8eeb-40b4-be7b-a841bd83be96
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f342daa958607a077fa5eb2a27ec705c8d99e67f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811872"
---
# Bereitstellen des Katalogs für Einstellungsvorlagen für UE-V 1.0


Speicherort Vorlagen für benutzerdefinierte Einstellungen können auf einem Ordnerpfad auf Microsoft User Experience Virtualization (UE-V)-Computern oder auf einer SMB-Netzwerkfreigabe (Server Message Block) gespeichert werden. Ein geplanter Task auf dem Computer sucht nach neuen oder aktualisierten Vorlagen von diesem Speicherort. Der Task überprüft diesen Ort einmal täglich und aktualisiert sein Synchronisierungsverhalten auf der Grundlage der Vorlagen in diesem Ordner. Vorlagen, die seit der letzten Überprüfung in diesem Ordner hinzugefügt oder aktualisiert wurden, werden vom UE-V-Agent registriert. Der UE-V-Agent hebt die Registrierung von Vorlagen auf, die aus diesem Ordner entfernt wurden. Der geplante Task wird als System ausgeführt. Die Netzwerkfreigabe muss mindestens die Berechtigungen für die Gruppe "Domänencomputer" erteilen. Erteilen Sie außerdem Zugriffsberechtigungen für den Netzwerkfreigabeordner für Administratoren, die die gespeicherten Vorlagen verwalten sollen. Weitere Informationen zu Vorlagen für benutzerdefinierte Einstellungen finden Sie unter [Planen der Bereitstellung von benutzerdefinierten Vorlagen für UE-V 1,0](planning-for-custom-template-deployment-for-ue-v-10.md).

**So konfigurieren Sie den Vorlagenkatalog für die Einstellungen für UE-V**

1.  Erstellen Sie einen neuen Ordner auf dem Computer, auf dem der Vorlagenkatalog für UE-V-Einstellungen gespeichert werden soll.

2.  Legen Sie die folgenden SMB-Berechtigungen (Freigabeebene) für den Katalogordner "Einstellungs Vorlagen" ein.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong>Benutzerkonto</strong></th>
    <th align="left"><strong>Berechtigungen empfehlen</strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Jeder</p></td>
    <td align="left"><p>Keine Berechtigungen</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Domänencomputer</p></td>
    <td align="left"><p>Lesen von Berechtigungsstufen</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Administratoren</p></td>
    <td align="left"><p>Berechtigungsstufen für Lesen/Schreiben</p></td>
    </tr>
    </tbody>
    </table>

     

3.  Legen Sie die folgenden NTFS-Berechtigungen für den Katalogordner "Settings" (Einstellungen).

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Benutzerkonto</th>
    <th align="left">Empfohlene Berechtigungen</th>
    <th align="left">Anwenden auf</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Ersteller/Besitzer</p></td>
    <td align="left"><p>Vollzugriff</p></td>
    <td align="left"><p>Dieser Ordner, Unterordner und Dateien</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Domänencomputer</p></td>
    <td align="left"><p>Ordnerinhalte auflisten und lesen</p></td>
    <td align="left"><p>Dieser Ordner, Unterordner und Dateien</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Jeder</p></td>
    <td align="left"><p>Keine Berechtigungen</p></td>
    <td align="left"><p>Keine Berechtigungen</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Administratoren</p></td>
    <td align="left"><p>Vollzugriff</p></td>
    <td align="left"><p>Dieser Ordner, Unterordner und Dateien</p></td>
    </tr>
    </tbody>
    </table>

     

4.  Klicken Sie auf **OK** , um die Dialogfelder zu schließen.

## Verwandte Themen


[Bereitstellen von UE-V 1.0](deploying-ue-v-10.md)

[Planen der Bereitstellung von benutzerdefinierten Vorlagen für UE-V 1.0](planning-for-custom-template-deployment-for-ue-v-10.md)

 

 





