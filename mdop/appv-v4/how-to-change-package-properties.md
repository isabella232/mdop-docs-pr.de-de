---
title: So ändern Sie die Paketeigenschaften
description: So ändern Sie die Paketeigenschaften
author: dansimp
ms.assetid: 6050916a-d4fe-4dac-8f2a-47308dbbf481
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d2427a2651f3941f967c171ae7854facc62b4aa9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807348"
---
# So ändern Sie die Paketeigenschaften


Mit den folgenden Verfahren können Sie den Namen eines Application Virtualization-Pakets und die zugehörigen Kommentare ändern.

Wenn dies das erste Mal ist, dass das Paket erstellt wurde, können Sie auch die Blockgröße des Sequenz-Parameters ändern, die bestimmt, wie ein sequenziertes Anwendungspaket von einem Application Virtualization Server an einen Application Virtualization-Desktop Client gestreamt wird.

**Hinweis**  Wenn Sie eine Blockgröße auswählen, sollten Sie die Größe der SFT-Datei und die Netzwerkbandbreite in Frage stellen. Eine Datei mit einer kleineren Blockgröße dauert länger, um über das Netzwerk zu streamen, es ist jedoch weniger bandbreitenintensiv. Dateien mit größeren Blockgrößen können schneller gestreamt werden, verwenden aber mehr Netzwerkbandbreite. Durch experimentieren können Sie die optimale Blockgröße für Streaming-Anwendungen in Ihrem Netzwerk ermitteln.

 

Die restlichen Paketeigenschaften auf der Registerkarte **Eigenschaften** werden automatisch generiert und können auf dieser Registerkarte nicht geändert werden.

**So ändern Sie den Paketnamen oder die Kommentare**

1.  Klicken Sie auf die Registerkarte **Eigenschaften** .

2.  Geben Sie im Textfeld **Paketname** den einzelnen für das Paket verwendeten Namen ein, der mehrere Anwendungen enthalten kann.

3.  Geben Sie im Textfeld **Kommentare** optional Kommentare ein, oder bearbeiten Sie Sie. Die empfohlene bewährte Vorgehensweise besteht darin, Detailinformationen zum Paket und zur Sequenzierung bereitzustellen.

4.  Wählen Sie im Menü **Datei** die Option **Speichern**aus.

**So ändern Sie die Blockgröße**

1.  Klicken Sie auf die Registerkarte **Eigenschaften** .

2.  Wählen Sie in der Dropdownliste **Block Größe** die Option **4 KB**, **16 KB**, **32 KB**oder **64 KB**aus.

3.  Wählen Sie im Menü **Datei** die Option **Speichern**aus.

## Verwandte Themen


[Informationen zur Registerkarte „Eigenschaften“](about-the-properties-tab.md)

[Sequencer Console](sequencer-console.md)

 

 





