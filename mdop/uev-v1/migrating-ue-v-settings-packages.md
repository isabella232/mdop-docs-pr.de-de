---
title: Migrieren von UE-V-Einstellungspaketen
description: Migrieren von UE-V-Einstellungspaketen
author: dansimp
ms.assetid: 93d99254-3e17-4e96-92ad-87059d8554a7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d0087f334e916c06e7611d2671d0b50e7d1dd916
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809817"
---
# Migrieren von UE-V-Einstellungspaketen


Im Lebenszyklus einer Microsoft User Experience Virtualization (UE-V)-Bereitstellung müssen Sie möglicherweise die Benutzer Einstellungs Pakete bei der Migration zu einem neuen Server oder zu Sicherungszwecken neu positionieren. Die Migration von Einstellungspaketen kann in den folgenden Szenarien erforderlich sein:

-   Upgrade vorhandener Server Hardware auf einen moderneren Server.

-   Migration einer Speicherorts Freigabe für Einstellungen aus einer Übungseinheit auf einen Produktionsserver.

Durch einfaches Kopieren der Dateien und Ordner bleiben die Sicherheitseinstellungen und-Berechtigungen nicht erhalten. Mit den folgenden Schritten werden die Einstellungen-Paketdateien mit ihren NTFS-Berechtigungen ordnungsgemäß auf eine neue Freigabe kopiert.

**Beibehalten der UE-V-Einstellungs Pakete beim Migrieren zu einem neuen Server**

1.  Erstellen Sie an einem neuen Speicherort auf einem anderen Server einen neuen Ordner. Beispiel: MySettings.

2.  Deaktivieren der Freigabe für die alte Ordnerfreigabe auf dem alten Server

3.  Verschieben Sie die vorhandenen Einstellungs Pakete über die Befehlszeile auf den neuen Server mit Robocopy. Beispiel:

    ``` syntax
    c:\start robocopy "\\servername\E$\MySettings" "\\servername\E$\MySettings" /b /sec /secfix /e /LOG:D:\Robocopylogs\MySettings.txt
    ```

    **Hinweis**  Öffnen Sie MySettings.txt mit einem Protokolldatei Leser wie Trace32, um den Kopierfortschritt zu überwachen.

     

4.  Erteilen Sie der neuen Freigabeberechtigungen für Freigabeebenen. Übernehmen Sie die NTFS-Berechtigungen, wie Sie von Robocopy eingestellt wurden.

    Aktualisieren Sie auf Computern, auf denen der UE-V-Agent ausgeführt wird, die SettingsStoragePath-Konfigurationseinstellung auf den UNC-Pfad der neuen Freigabe.

## Verwandte Themen


[Verwalten von UE-V 1.0](administering-ue-v-10.md)

[Vorgänge für UE-V 1.0](operations-for-ue-v-10.md)

 

 





