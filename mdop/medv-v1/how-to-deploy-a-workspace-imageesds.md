---
title: So stellen Sie ein Arbeitsbereich-Image bereit
description: So stellen Sie ein Arbeitsbereich-Image bereit
author: dansimp
ms.assetid: ccc8e89b-1625-4b58-837e-4c6d93d46070
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4cb16b0a4c278d135fdc9b737aa7a6e9b46115e1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812094"
---
# So stellen Sie ein Arbeitsbereich-Image bereit


Bei Verwendung eines Enterprise-Softwareverteilungssystems kann ein neues Bild auf Clientcomputern auf eine der folgenden Arten bereitgestellt werden:

-   [Web-Download](#bkmk-howtodeployaworkspaceimageviatheweb)

-   [Pre-Staging von Bildern](#bkmk-howtodeployaworkspaceimageusingimageprestaging)

## <a href="" id="bkmk-howtodeployaworkspaceimageviatheweb"></a>Bereitstellen eines Arbeitsbereichs Bilds über das Web


**So stellen Sie ein Arbeitsbereichs Bild über das Web bereit**

1.  Laden Sie das MED-V-Abbild auf den Server hoch.

    Informationen zum Hochladen des Bilds finden Sie unter [Hochladen eines MED-V-Bilds auf den Server](how-to-upload-a-med-v-image-to-the-server.md).

2.  Installieren Sie mithilfe Ihres Softwareverteilungssystems für Unternehmen das MED-V-Client. MSI-Paket auf den Computern der Benutzer.

    Informationen zum Installieren des Med-v Client. msi-Pakets finden Sie unter [so wird es gemacht: Installieren des Med-v-Clients](how-to-install-med-v-clientesds.md).

    Der MED-V-Client wird zum ersten Mal installiert und gestartet. Beim erstmaligen Start downloadet der Client das Bild von der Serveradresse, die in der Clientinstallation angegeben ist.

## <a href="" id="bkmk-howtodeployaworkspaceimageusingimageprestaging"></a>So wird es gemacht: Bereitstellen eines Arbeitsbereichs Abbilds mithilfe von Bild Pre-Staging


**So stellen Sie ein Arbeitsbereichs Bild mithilfe der vorbereitenden Bilder bereit**

1.  Erstellen Sie einen Bild-Pre-stage-Ordner, und drücken Sie das Bild in den Ordner.

    Informationen zum Konfigurieren der Vorabbereitstellung von Bildern finden Sie unter [Konfigurieren der vorinszenierung von Bildern](how-to-configure-image-pre-staging.md).

2.  Installieren Sie mithilfe Ihres Softwareverteilungssystems für Unternehmen das MED-V-Client. MSI-Paket auf den Computern der Benutzer.

    Informationen zum Installieren des Med-v Client. msi-Pakets finden Sie unter [so wird es gemacht: Installieren des Med-v-Clients](how-to-install-med-v-clientesds.md).

    Der MED-V-Client wird zum ersten Mal installiert und gestartet. Beim erstmaligen Start ruft der Client das Bild aus dem in der Clientinstallation angegebenen Pre-stage-Ordner ab.

## Verwandte Themen


[So konfigurieren Sie den Image-Web-Verteilungsserver](how-to-configure-the-image-web-distribution-server.md)

 

 





