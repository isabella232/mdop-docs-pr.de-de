---
title: So stellen Sie ein Arbeitsbereich-Image bereit
description: So stellen Sie ein Arbeitsbereich-Image bereit
author: dansimp
ms.assetid: b2c77e0d-101d-4956-a27c-8beb0e4f262e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d691514691286c92bd62d6fda6666345e17eb9f3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812100"
---
# So stellen Sie ein Arbeitsbereich-Image bereit


Wenn Sie ein Bereitstellungspaket verwenden, kann ein neues Bild auf Clientcomputern auf eine der folgenden Arten bereitgestellt werden:

-   [Web-Download](#bkmk-howtodeployaworkspaceimageviatheweb)

-   [Pre-Staging von Bildern](#bkmk-howtodeployaworkspaceimageusingimageprestaging)

-   [Bereitstellen des Bilds im Bereitstellungspaket](#bkmk-howtodeployaworkspaceimageusingadeploymentapackage)

## <a href="" id="bkmk-howtodeployaworkspaceimageviatheweb"></a>Bereitstellen eines Arbeitsbereichs Bilds über das Web


**So stellen Sie ein Arbeitsbereichs Bild über das Web bereit**

1.  Laden Sie das MED-V-Abbild auf den Server hoch.

    Informationen zum Hochladen des Bilds finden Sie unter [Hochladen eines MED-V-Bilds auf den Server](how-to-upload-a-med-v-image-to-the-server.md).

2.  Erstellen Sie ein Bereitstellungspaket, und fügen Sie den Serverpfad zum Speicherort des Bilds ein.

    Informationen zum Erstellen eines Bereitstellungspakets finden Sie unter [Konfigurieren eines Bereitstellungspakets](how-to-configure-a-deployment-package.md).

3.  Bereitstellen des Pakets für Endbenutzer

    Informationen zum Bereitstellen des Pakets finden Sie unter [so wird es gemacht: Installieren des MED-V-Clients](how-to-install-med-v-clientdeployment-package.md).

    Der MED-V-Client wird zum ersten Mal installiert und gestartet. Beim erstmaligen Start downloadet der Client das Bild von der Serveradresse, die in der Clientinstallation angegeben ist.

## <a href="" id="bkmk-howtodeployaworkspaceimageusingimageprestaging"></a>So wird es gemacht: Bereitstellen eines Arbeitsbereichs Abbilds mithilfe von Bild Pre-Staging


**So stellen Sie ein Arbeitsbereichs Bild mithilfe der vorbereitenden Bilder bereit**

1.  Erstellen Sie einen Bild-Pre-stage-Ordner, und drücken Sie das Bild in den Ordner.

    Informationen zum Konfigurieren der Vorabbereitstellung von Bildern finden Sie unter [Konfigurieren der vorinszenierung von Bildern](how-to-configure-image-pre-staging.md).

2.  Erstellen Sie ein Bereitstellungspaket, und fügen Sie den Pfad in den Ordner "Pre-stage" des Bilds ein.

    Informationen zum Erstellen eines Bereitstellungspakets finden Sie unter [Konfigurieren eines Bereitstellungspakets](how-to-configure-a-deployment-package.md).

3.  Bereitstellen des Pakets für Endbenutzer

    Informationen zum Bereitstellen des Pakets finden Sie unter [so wird es gemacht: Installieren des MED-V-Clients](how-to-install-med-v-clientdeployment-package.md).

    Der MED-V-Client wird zum ersten Mal installiert und gestartet. Beim erstmaligen Start ruft der Client das Bild aus dem in der Clientinstallation angegebenen Pre-stage-Ordner ab.

## <a href="" id="bkmk-howtodeployaworkspaceimageusingadeploymentapackage"></a>Bereitstellen eines Arbeitsbereichs Bilds mithilfe eines Bereitstellungspakets


**So stellen Sie ein Arbeitsbereichs Bild mithilfe eines Bereitstellungspakets bereit**

1.  Erstellen Sie ein Bereitstellungspaket, und fügen Sie das Bild in das Paket ein.

    Informationen zum Erstellen eines Bereitstellungspakets finden Sie unter [Konfigurieren eines Bereitstellungspakets](how-to-configure-a-deployment-package.md).

2.  Bereitstellen des Pakets für Endbenutzer

    Informationen zum Bereitstellen des Pakets finden Sie unter [so wird es gemacht: Installieren des MED-V-Clients](how-to-install-med-v-clientdeployment-package.md).

    Das Bild wird als Teil der Paketinstallation in den Host importiert.

## Verwandte Themen


[So konfigurieren Sie den Image-Web-Verteilungsserver](how-to-configure-the-image-web-distribution-server.md)

[So konfigurieren Sie ein Bereitstellungspaket](how-to-configure-a-deployment-package.md)

 

 





