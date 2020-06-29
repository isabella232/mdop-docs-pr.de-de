---
title: So verwenden Sie das Verwaltungsfeature für den Cachespeicher
description: So verwenden Sie das Verwaltungsfeature für den Cachespeicher
author: dansimp
ms.assetid: 60965660-c015-46a8-88ac-54cbc050fe33
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fcb9cc4bc076e1acf52fb1c03797384c45b82f7b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806695"
---
# So verwenden Sie das Verwaltungsfeature für den Cachespeicher


Das Speicher Verwaltungsfeature für das Dateisystem-Cache verwendet einen am wenigsten zuletzt verwendeten Algorithmus (LRU) und ist standardmäßig aktiviert. Wenn der Platz, der für ein neues Paket erforderlich ist, den verfügbaren freien Speicherplatz im Cache überschreitet, verwendet der Application Virtualization (App-V)-Client dieses Feature, um zu ermitteln, welche, falls vorhanden, vorhandene Pakete aus dem Cache löschen können, um Platz für das neue Paket zu schaffen. Der Client löscht das Paket mit dem ältesten Datum des letzten Zugriffs, wenn es älter als der im Registrierungswert MinPkgAge angegebene Wert ist. Die Verwendung des Dateisystem-Cache-Speicherplatz Verwaltungsfeatures kann auch dazu beitragen, niedrige Speicherplatzprobleme zu vermeiden.

Wenn erforderlich, werden mehr als ein Paket gelöscht. Gesperrte Pakete werden nicht gelöscht.

**Hinweis**  Wenn Sie sicherstellen möchten, dass der Cache über genügend Speicherplatz für alle Pakete verfügt, die möglicherweise bereitgestellt werden, verwenden Sie die Einstellung Speicher **Platz für freien Speicherplatz verwenden** , wenn Sie den Client so konfigurieren, dass der Cache nach Bedarf erweitert werden kann. Sie können aber auch im voraus ermitteln, wie viel Speicherplatz für den App-V-Cache benötigt wird, und die Cachegröße zur Installationszeit entsprechend festlegen.

 

Das Cache-Speicherplatz Verwaltungsfeature wird vom Registrierungswert UnloadLeastRecentlyUsed gesteuert. Der Wert 1 aktiviert das Feature, und der Wert 0 (null) deaktiviert es.

**So aktivieren oder deaktivieren Sie das Feature "Cachespeicherverwaltung"**

-   Setzen Sie den folgenden Registrierungswert auf 1, um den LRU-Algorithmus zu aktivieren. Setzen Sie den Wert auf 0 (null), um das Feature zu deaktivieren.

    HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\softgrid\\4.5\\client\\appfs\\unloadleastrecentlyused

**So steuern Sie, welche Pakete verworfen werden können**

-   Wenn Sie feststellen möchten, wann das Paket für verwerfen ausgewählt werden kann, legen Sie den folgenden Registrierungswert auf die minimale Anzahl von Tagen fest, die Sie verstreichen möchten, nachdem das Paket zuletzt zugegriffen wurde. Pakete, die in letzter Zeit verwendet wurden, werden nicht verworfen.

    HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\softgrid\\4.5\\client\\appfs\\minpkgage

    **Vorsicht**  Der Höchstwert für diesen Registrierungsschlüssel lautet 0x00011111. Durch größere Werte wird die ordnungsgemäße Funktion des Cachespeicher Verwaltungsfeatures verhindert.

     

## Verwandte Themen


[So konfigurieren Sie die App-V-Client-Registrierungseinstellungen über die Befehlszeile](how-to-configure-the-app-v-client-registry-settings-by-using-the-command-line.md)

 

 





