---
title: So konfigurieren Sie den Image-Web-Verteilungsserver
description: So konfigurieren Sie den Image-Web-Verteilungsserver
author: dansimp
ms.assetid: 2d32ae79-dff5-4c05-a412-dd15452b6007
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 8a21b14fbaca6bbc09d4c35b4d8fb86365c42e3b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810987"
---
# So konfigurieren Sie den Image-Web-Verteilungsserver


Bei einem Bild-Repository handelt es sich um einen optionalen Server, der für die Bildverteilung verwendet wird (wobei Administratoren neue Bilder hochladen und Clientcomputer alle 15 Minuten den Server überprüfen und das Bild aktualisieren, wenn ein neues verfügbar ist).

## <a href="" id="bkmk-configuringanimagereporitoryusingiis"></a>


Für einen Bildverteilungsserver ist Folgendes erforderlich:

-   Internetinformationsdienste (IIS) – Informationen finden Sie unter [Internetinformationsdienste](https://go.microsoft.com/fwlink/?LinkId=142995).

    Wählen Sie während der IIS-Installation beim Hinzufügen von Rollendiensten die folgenden unterstützten Authentifizierungsmethoden aus:

    -   **Standardauthentifizierung**

    -   **Windows-Authentifizierung**

    -   **Authentifizierung der Client Zertifikatzuordnung**

    Schließen Sie beim Konfigurieren von IIS Folgendes ein:

    -   Fügen Sie ein virtuelles Verzeichnis mit dem Alias " **MEDVImages**" hinzu. Der physikalische Pfad sollte auf die Position der Bilder verweisen.

    -   Aktivieren Sie Bits.

    -   Fügen Sie die folgenden MIME-Typen hinzu:

        -   **. CKM (Application/Oktett-Stream)**

        -   **. Index (Application/Oktett-Stream**)

    -   Fügen Sie auf der MED-V-Website **jedem Benutzer**Leseberechtigungen hinzu.

    -   Starten Sie IIS neu.

-   BITS-Servererweiterungen für IIS – Informationen finden Sie unter [Installieren von BITS-Servererweiterungen](https://go.microsoft.com/fwlink/?LinkId=142996).

## Verwandte Themen


[Unterstützte Konfigurationen](supported-configurationsmedv-orientation.md)

[Entwerfen Sie die MED-V-Image-Repositorys](design-the-med-v-image-repositories.md)

 

 





