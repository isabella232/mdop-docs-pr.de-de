---
title: Bereitstellen eines MED-V-Arbeitsbereichs über ein Enterprise Software Distribution-System
description: Bereitstellen eines MED-V-Arbeitsbereichs über ein Enterprise Software Distribution-System
author: dansimp
ms.assetid: 867faed6-74ce-4573-84be-8bf26e66c08c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fb9ebbc0fb605f84c5a8e67fc77fd9be51b29ff4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810069"
---
# Bereitstellen eines MED-V-Arbeitsbereichs über ein Enterprise Software Distribution-System


Der MED-V-Client kann mithilfe eines Unternehmenssoftware Verteilungssystems wie Microsoft System Center Configuration Manager verteilt werden.

**Hinweis**  Wenn Med-v mithilfe von Microsoft System Center Configuration Manager installiert wird, legen Sie beim Erstellen eines Pakets für med-v den Ausführungsmodus auf Administratorrechte.

 

Bevor Sie Med-v mithilfe eines Enterprise-Softwareverteilungssystems bereitstellen, stellen Sie sicher, dass Sie ein Med-v-Abbild erstellt haben, das bereitgestellt werden kann. Weitere Informationen zum Erstellen eines Med-v-Bilds finden Sie unter [Erstellen eines Med-v-Bilds](creating-a-med-v-image.md).

Nachdem das MED-V-Abbild vorbereitet wurde, sollten Sie die beste Methode zum Verteilen des Bilds in Ihrer Umgebung in Frage stellen. Das Bild kann auf eine der folgenden Arten verteilt werden:

-   Im Web heruntergeladen und per Webdownload vertrieben, optional mit Trim-Transfer-Technologie.

-   Wird mithilfe von Bild Pre-Staging verteilt.

## Bereitstellen des Bilds über das Web


Wenn Sie das Bild über das Web bereitstellen, laden Sie das MED-V-Abbild auf einen Bild-webverteilungs Server hoch. Informationen zum Konfigurieren eines Image Web Distribution-Servers finden Sie unter [Konfigurieren des Image Web Distribution-Servers](how-to-configure-the-image-web-distribution-server.md). Informationen zum Hochladen eines Bilds auf den Server finden Sie unter [Hochladen eines MED-V-Images auf den](how-to-upload-a-med-v-image-to-the-server.md)Server.

## Bereitstellen des Bilds über Pre-Staging


Wenn Sie das Bild über Pre-Staging für das Bild bereitstellen, konfigurieren Sie den Ordner "Pre-stage", und drücken Sie das MED-V-Bild in den Ordner. Weitere Informationen zum Konfigurieren von Bild Pre-Staging finden Sie unter [so wird es gemacht: Konfigurieren der Vorabbereitstellung von Bildern](how-to-configure-image-pre-staging.md).

**Hinweis**  Wenn Sie die vorinszenierung von Bildern verwenden, ist es wichtig, vor dem pushen des Client. msi-Pakets den Pre-stage-Ordner des Bilds zu konfigurieren. Der Pfad des Ordners muss im Client. MSI-Paket enthalten sein.

 

Und schließlich: Pushen Sie das Client. MSI-Paket mithilfe Ihres Software Verteilungs Centers für Unternehmen. MED-V kann dann installiert und das Bild bereitgestellt werden. Weitere Informationen zum Installieren des Med-v-Clients finden Sie unter [so wird es gemacht: Installieren des Med-v-Clients](how-to-install-med-v-clientesds.md). Weitere Informationen zum Bereitstellen des Bilds finden Sie unter [Bereitstellen eines Arbeitsbereichs Bilds](how-to-deploy-a-workspace-imageesds.md).

 

 





