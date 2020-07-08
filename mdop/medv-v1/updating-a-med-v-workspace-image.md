---
title: Aktualisieren eines MED-V-Arbeitsbereich-Images
description: Aktualisieren eines MED-V-Arbeitsbereich-Images
author: dansimp
ms.assetid: 1b9c4a73-3487-43d2-98e3-43dbc79e10e3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 60a5d12622e0cb7012c6d0a22124d63c085f6d0a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811404"
---
# Aktualisieren eines MED-V-Arbeitsbereich-Images


Ein Bild kann auf eine der folgenden Arten aktualisiert werden:

-   Das Update kann über Ihr Unternehmenssoftware-Verteilungssystem an das Gastbetriebssystem übertragen werden.

-   Das Update kann auf den Image Web Distribution-Server hochgeladen und dann vom Client heruntergeladen und auf das MED-V-Abbild angewendet werden.

-   Das MED-V-Basis Bild kann aktualisiert und erneut bereitgestellt werden.

## <a href="" id="bkmk-howtoupdateamedvimageusinganesd"></a>Aktualisieren eines MED-V-Images mithilfe eines Unternehmens Software Verteilungssystems


**So aktualisieren Sie ein MED-V-Abbild mithilfe eines Enterprise-Softwareverteilungssystems**

-   Lesen Sie die Dokumentation des Systems, das Sie verwenden.

## <a href="" id="bkmk-howtoupdateamedvimageusingwebdownload"></a>Aktualisieren eines MED-V-Bilds mit dem Web-Download


**So aktualisieren Sie ein MED-V-Bild mit dem Web-Download**

1.  Stellen Sie in der Med-v-Verwaltung auf der Registerkarte **virtueller Computer** sicher, dass die folgenden Einstellungen auf die Med-v-Arbeitsbereichs Richtlinien angewendet werden, die mit dem zu aktualisierenden Med-v-Bild verknüpft sind:

    -   Das Kontrollkästchen **Update vorschlagen, wenn eine neue Version verfügbar ist** , ist aktiviert.

    -   Optional können die Clients das Kontrollkästchen **beim Herunterladen von Bildern für diesen Arbeitsbereich auf die Option "Übertragung kürzen" verwenden** .

    Weitere Informationen finden Sie unter [Anwenden von Einstellungen für virtuelle Computer auf einen MED-V-Arbeitsbereich](how-to-apply-virtual-machine-settings-to-a-med-v-workspace.md).

2.  Laden Sie das Image-Update auf den Image Web Distribution-Server hoch.

    Alle Clients mit Bildern, die aktualisiert werden müssen, laden das Update automatisch herunter und wenden es auf das Bild an.

## <a href="" id="bkmk-howtoupdateamedvbaseimage"></a>Aktualisieren eines MED-V-Basis Bilds


**So aktualisieren Sie ein MED-V-Basis Bild**

1.  Öffnen Sie das vorhandene Bild in Virtual PC2007.

2.  Nehmen Sie die erforderlichen Änderungen am Bild vor, und aktualisieren Sie das Bild (beispielsweise die Installation neuer Software).

3.  Schließen Sie den virtuellen PC2007.

4.  Testen Sie das Bild.

5.  Nachdem das Bild getestet wurde, packen Sie es mit dem gleichen Namen wie das vorhandene Bild in das lokale Repository ein.

    **Hinweis**  Wenn Sie dem Bild einen anderen Namen als die vorhandene Version geben, wird anstelle einer neuen Version des vorhandenen Bilds ein neues Bild erstellt.

     

6.  Laden Sie die neue Version auf den Server hoch, schieben Sie Sie in den Ordner "Pre-stage" des Bilds, oder verteilen Sie Sie über ein Bereitstellungspaket.

## Verwandte Themen


[Erstellen eines MED-V-Images](creating-a-med-v-image.md)

[So aktualisieren Sie ein MED-V-Image](how-to-update-a-med-v-image.md)

[Konfigurieren von MED-V-Arbeitsbereichsrichtlinien](configuring-med-v-workspace-policies.md)

[So konfigurieren Sie den Image-Web-Verteilungsserver](how-to-configure-the-image-web-distribution-server.md)

 

 





