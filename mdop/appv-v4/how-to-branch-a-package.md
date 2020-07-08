---
title: So verzweigen Sie ein Paket
description: So verzweigen Sie ein Paket
author: dansimp
ms.assetid: bfe46a8a-f0ee-4a71-9e9c-64ac08aac9c1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2de36fae1a09aeae4d1b7b21ebe00f683e3b3693
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807383"
---
# So verzweigen Sie ein Paket


Gehen Sie wie folgt vor, um ein vorhandenes sequenziertes Anwendungspaket so zu ändern, dass es parallel zum ursprünglichen sequenzierten Anwendungspaket ausgeführt werden kann. Dieser Vorgang wird als Verzweigung bezeichnet. Wenn Sie ein virtuelles Anwendungspaket verzweigen, können Sie zwei Versionen desselben Pakets ausführen. So können Sie beispielsweise ein Service Pack auf ein vorhandenes Paket anwenden und es nebeneinander mit dem ursprünglichen sequenzierten virtuellen Anwendungspaket ausführen.

Gehen Sie wie folgt vor, um ein sequenziertes virtuelles Anwendungspaket zu verzweigen.

**So verzweigen Sie ein sequenziertes virtuelles Anwendungspaket**

1.  Öffnen Sie den Microsoft Application Virtualization (App-V)-Sequenzer. Um das Zielverzeichnis anzugeben, in dem sich das Paket (SPRJ) befindet, das Sie verzweigen möchten, wählen Sie **Datei**aus, **Öffnen**.

2.  Navigieren Sie zu dem Verzeichnis, das die sequenzierte Anwendung enthält, die Sie verzweigen möchten, und klicken Sie auf **Öffnen**.

3.  Wenn Sie eine Kopie des Pakets speichern möchten, wählen Sie im App-V-Sequenzer **Datei**, **Speichern**unter aus. Geben Sie einen neuen eindeutigen Namen an, und geben Sie ein neues eindeutiges Paketstammverzeichnis für die Kopie des Pakets an. Klicken Sie auf **Speichern**.

    **Wichtig**  
    Sie müssen einen neuen Paketnamen angeben, oder die vorhandene Version des Pakets wird überschrieben.



~~~
The sequencer will automatically generate new GUID files for the new package. The version number associated with the package will also be automatically appended to the OSD file name.
~~~

4. Nachdem Sie die neue Version gespeichert haben, können Sie die erforderlichen Konfigurationsänderungen übernehmen und die zugehörigen ICO-, OSD-, SFT-und SPRJ-Dateien auf dem Application Virtualization (App-V)-Server speichern.

## Verwandte Themen


[Aufgaben für den Application Virtualization Sequencer](tasks-for-the-application-virtualization-sequencer.md)









