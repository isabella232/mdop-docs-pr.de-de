---
title: Konfigurieren von MED-V für Remote-Netzwerke
description: Konfigurieren von MED-V für Remote-Netzwerke
author: dansimp
ms.assetid: 4d2f0081-622f-4a6f-8d73-f8c2108036e0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 328376046ee5213f3d5bb09be7adf8c81f8508b1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811926"
---
# Konfigurieren von MED-V für Remote-Netzwerke


Sie können MED-V so konfigurieren, dass Sie in einem Netzwerk, Remote oder sowohl aus dem Netzwerk als auch aus der Ferne aus arbeiten.

## <a href="" id="bkmk-howtoconfiguremedvtoworkfrominsideanetworkorremotely"></a>


**So konfigurieren Sie MED-V für die Arbeit in einem Netzwerk**

-   Konfigurieren Sie einen MED-V-Server und die Bildverteilung innerhalb des Netzwerks.

**So konfigurieren Sie MED-V für die Remote Arbeit**

1.  Konfigurieren Sie einen MED-V-Server und einen Bildverteilungsserver, auf die über das Internet zugegriffen werden kann.

2.  Konfigurieren Sie bei Bedarf ein Umkreisnetzwerk (auch als DMZ bezeichnet) Reverse-Proxy.

3.  Legen Sie die Authentifizierungsmethode in der *ClientSettings.xml* -Datei fest, die im Ordner **Servers\\Configuration Server\\** zu finden ist.

**So konfigurieren Sie MED-V für die Arbeit in einem Netzwerk und Remote**

1.  Konfigurieren Sie einen MED-V-Server und einen Bildverteilungsserver im Netzwerk.

2.  Stellen Sie sicher, dass auf die Server über das Internet zugegriffen werden kann.

3.  Konfigurieren Sie die DNS-Auflösung so, dass Sie, wenn der Client versucht, eine Verbindung mit einem Server herzustellen, automatisch eine Verbindung mit dem richtigen Server (im Netzwerk oder über das Internet) herstellt, der auf dem Clientstandort basiert.

4.  Konfigurieren Sie bei Bedarf einen Reverse-Proxy für Umkreisnetzwerke.

5.  Legen Sie die Authentifizierungsmethode in der *ClientSettings.xml* -Datei fest, die im Ordner **Servers\\Configuration Server\\** zu finden ist.

**Hinweis**  Bei der Anwendung neuer Einstellungen muss der Dienst neu gestartet werden.

 

-   Sie können das IIS-Authentifizierungsschema auf eine der folgenden Optionen ändern: Basic, Digest, NTLM oder Negotiate. Der Standardwert ist Negotiate und verwendet den folgenden Eintrag:

    ```xml
    <ImageDistribution>
    <!-- The authentication used for image download. Basic and digest authentication should be used only under SSL.-->
       <!-- The line below can be one of the following: -->
       <!--BG_AUTH_SCHEME>BG_AUTH_SCHEME_BASIC</BG_AUTH_SCHEME-->
       <!--BG_AUTH_SCHEME>BG_AUTH_SCHEME_DIGEST</BG_AUTH_SCHEME-->
       <!--BG_AUTH_SCHEME>BG_AUTH_SCHEME_NTLM</BG_AUTH_SCHEME-->
       <!--BG_AUTH_SCHEME>BG_AUTH_SCHEME_NEGOTIATE</BG_AUTH_SCHEME-->
       <Authentication type="Kidaro.Foundation.Bits.BG_AUTH_SCHEME">
          <BG_AUTH_SCHEME>BG_AUTH_SCHEME_NEGOTIATE</BG_AUTH_SCHEME>
       </Authentication>
    </ImageDistribution>
    ```

## Verwandte Themen


[Planen und Entwerfen der MED-V-Infrastruktur](med-v-infrastructure-planning-and-design.md)

 

 





