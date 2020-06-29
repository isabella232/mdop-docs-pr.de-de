---
title: Migrieren von UE-V 2. x-Einstellungspaketen
description: Migrieren von UE-V 2. x-Einstellungspaketen
author: dansimp
ms.assetid: f79381f4-e142-405c-b728-5c048502aa70
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0aa1f1c36594d69de40306dfa70a4a0cf5c86dbb
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811203"
---
# Migrieren von UE-V 2. x-Einstellungspaketen


Im Lebenszyklus einer Microsoft User Experience Virtualization (UE-V) 2,0, 2,1 oder 2,1 SP1-Bereitstellung müssen Sie möglicherweise die Benutzer Einstellungs Pakete neu positionieren, wenn Sie zu einem neuen Server migrieren oder Sicherungen durchführen. Einstellungs Pakete müssen möglicherweise in den folgenden Szenarien migriert werden:

-   Upgrade vorhandener Server Hardware auf einen moderneren Server.

-   Migration einer Einstellungen-Speicherorts Freigabe von einem Testserver zu einem Produktionsserver.

Durch einfaches Kopieren der Dateien und Ordner bleiben die Sicherheitseinstellungen und-Berechtigungen nicht erhalten. In den folgenden Schritten wird beschrieben, wie Sie das Einstellungspaket zusammen mit den Berechtigungen für das NTFS-Dateisystem ordnungsgemäß auf eine neue Freigabe kopieren.

**So erhalten Sie die UE-V 2-Einstellungs Pakete beim Migrieren zu einem neuen Server**

1.  Erstellen Sie an einem neuen Speicherort auf einem anderen Server einen neuen Ordner, beispielsweise "meine Einstellungen".

2.  Deaktivieren der Freigabe für die alte Ordnerfreigabe auf dem alten Server

3.  So kopieren Sie die vorhandenen Einstellungs Pakete auf den neuen Server mit Robocopy

    ``` syntax
    C:\start robocopy "\\servername\E$\MySettings" "\\servername\E$\MySettings" /b /sec /secfix /e /LOG:D:\Robocopylogs\MySettings.txt
    ```

    **Hinweis**  Öffnen Sie MySettings.txt mit einer Protokollanzeige wie Trace32, um den Kopierfortschritt zu überwachen.

     

4.  Erteilen Sie der neuen Freigabeberechtigungen für Freigabeebenen. Belasse die NTFS-Dateisystemberechtigungen, wie Sie von Robocopy eingestellt wurden.

    Aktualisieren Sie auf Computern, auf denen der UE-V-Agent ausgeführt wird, die **SettingsStoragePath** -Konfigurationseinstellung auf den UNC-Pfad (Universal Naming Convention) der neuen Freigabe.

    Sie **haben einen Vorschlag für UE-V**? [Hier](http://uev.uservoice.com/forums/280428-microsoft-user-experience-virtualization)können Sie Vorschläge hinzufügen oder abstimmen. **Haben Sie ein UE-V-Problem**? Verwenden Sie das [UE-V TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopuev).

## Verwandte Themen


[Verwalten von UE-V 2. x](administering-ue-v-2x-new-uevv2.md)

 

 





