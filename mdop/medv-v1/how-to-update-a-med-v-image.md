---
title: So aktualisieren Sie ein MED-V-Image
description: So aktualisieren Sie ein MED-V-Image
author: dansimp
ms.assetid: 61eacf50-3a00-4bb8-b2f3-7350a6467fa1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2f62cbd54d8593646460700a86ea48b5df4ce437
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804271"
---
# So aktualisieren Sie ein MED-V-Image


## So aktualisieren Sie ein MED-V-Image


Ein vorhandenes MED-V-Bild kann aktualisiert werden, wodurch eine neue Version des Bilds erstellt wird. Die neue Version kann dann auf Clientcomputern bereitgestellt werden, um das vorhandene Bild zu ersetzen.

**Hinweis**  Wenn eine neue Version auf dem Client bereitgestellt wird, wird das vorhandene Bild überschrieben. Stellen Sie beim Aktualisieren eines Bilds sicher, dass keine Daten auf dem Client gespeichert werden müssen.

 

**So aktualisieren Sie ein MED-V-Bild**

1.  Öffnen Sie das vorhandene Bild in Virtual PC2007.

2.  Nehmen Sie die erforderlichen Änderungen am Bild vor, und aktualisieren Sie das Bild (beispielsweise die Installation neuer Software).

3.  Schließen Sie den virtuellen PC2007.

4.  Testen Sie das Bild.

5.  Nachdem das Bild getestet wurde, packen Sie es mit dem gleichen Namen wie das vorhandene Bild in das lokale Repository ein.

    **Hinweis**  Wenn Sie dem Bild einen anderen Namen als die vorhandene Version geben, wird anstelle einer neuen Version des vorhandenen Bilds ein neues Bild erstellt.

     

6.  Laden Sie die neue Version auf den Server hoch, oder verteilen Sie Sie über ein Bereitstellungspaket.

## Verwandte Themen


[Erstellen eines virtuellen PC-Images für MED-V](creating-a-virtual-pc-image-for-med-v.md)

[So erstellen und testen Sie ein MED-V-Image](how-to-create-and-test-a-med-v-image.md)

[So packen Sie ein MED-V-Image](how-to-pack-a-med-v-image.md)

[So laden Sie ein MED-V-Bild auf den Server hoch](how-to-upload-a-med-v-image-to-the-server.md)

[Aktualisieren eines MED-V-Arbeitsbereich-Images](updating-a-med-v-workspace-image.md)

 

 





