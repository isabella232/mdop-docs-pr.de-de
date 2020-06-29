---
title: Bereitstellen eines MED-V-Arbeitsbereichs mit einem Bereitstellungspaket
description: Bereitstellen eines MED-V-Arbeitsbereichs mit einem Bereitstellungspaket
author: dansimp
ms.assetid: e07fa70a-1a9f-486f-9a86-b33593b234da
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: dc16b32fd44e45606df5502fda2e580d404dbb19
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810072"
---
# Bereitstellen eines MED-V-Arbeitsbereichs mit einem Bereitstellungspaket


Die Installation des Bereitstellungspakets bietet eine Methode zum Installieren des MED-V-Clients zusammen mit allen erforderlichen Voraussetzungen sowie sämtlichen vom Administrator vordefinierten Einstellungen.

Wenn Sie ein Bereitstellungspaket verwenden, wird das Paket über ein freigegebenes Netzwerk oder Wechselmedien verteilt. Das Bild kann im Paket enthalten sein oder separat verteilt werden.

Bevor Sie ein Bereitstellungspaket erstellen, stellen Sie sicher, dass Sie ein MED-V-Abbild erstellt haben, das bereitgestellt werden soll. Weitere Informationen zum Erstellen eines Med-v-Bilds finden Sie unter [Erstellen eines Med-v-Bilds](creating-a-med-v-image.md).

Nachdem das MED-V-Abbild vorbereitet wurde, sollten Sie die beste Methode zum Verteilen des Bilds in Ihrer Umgebung in Frage stellen. Das Bild kann auf eine der folgenden Arten verteilt werden:

-   Im Web heruntergeladen und per Webdownload verteilt, optional mit Trim-Transfer-Technologie.

-   Wird mithilfe von Bild Pre-Staging verteilt.

-   Im Bereitstellungspaket enthalten und zusammen mit allen anderen MED-V-Komponenten verteilt.

Wenn das Bild in das Paket aufgenommen wird, sind keine weiteren Konfigurationen für das Bild erforderlich. Wenn das Bild nicht im Bereitstellungspaket enthalten sein soll, führen Sie eine der folgenden Aktionen aus:

-   Wenn Sie das Bild über das Web bereitstellen, laden Sie das MED-V-Abbild auf den Bild-webverteilungs Server hoch. Informationen zum Konfigurieren eines Image Web Distribution-Servers finden Sie unter [Konfigurieren des Image Web Distribution-Servers](how-to-configure-the-image-web-distribution-server.md). Informationen zum Hochladen eines Bilds auf den Server finden Sie unter [Hochladen eines MED-V-Images auf den](how-to-upload-a-med-v-image-to-the-server.md)Server.

-   Wenn Sie das Bild über Pre-Staging für das Bild bereitstellen, konfigurieren Sie den Ordner "Pre-stage", und drücken Sie das MED-V-Bild in den Ordner. Weitere Informationen zum Konfigurieren der vorinszenierung von Bildern finden Sie unter [Konfigurieren der vorinszenierung von Bildern](how-to-configure-image-pre-staging.md).

**Hinweis**  Wenn Sie die vorinszenierung von Bildern verwenden, ist es wichtig, vor dem Erstellen des Bereitstellungspakets den Pre-stage-Ordner des Bilds zu konfigurieren. Der Ordnerpfad muss im Bereitstellungspaket enthalten sein.

 

Erstellen Sie schließlich das Bereitstellungspaket. Weitere Informationen zum Erstellen eines Bereitstellungspakets finden Sie unter [Konfigurieren eines Bereitstellungspakets](how-to-configure-a-deployment-package.md). Nachdem das Paket abgeschlossen ist, verteilen Sie es für die Bereitstellung.

Nachdem das Bereitstellungspaket verteilt wurde, kann der MED-V-Client installiert und das Bild bereitgestellt werden. Weitere Informationen zum Installieren des Med-v-Clients finden Sie unter [so wird es gemacht: Installieren des Med-v-Clients](how-to-install-med-v-clientdeployment-package.md). Weitere Informationen zum Bereitstellen des Bilds finden Sie unter [Bereitstellen eines Arbeitsbereichs Bilds](how-to-deploy-a-workspace-imagedeployment-package.md).

 

 





