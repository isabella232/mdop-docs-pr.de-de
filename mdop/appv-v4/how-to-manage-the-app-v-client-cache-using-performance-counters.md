---
title: So verwalten Sie den App-V-Client-Cache mithilfe von Leistungsindikatoren
description: So verwalten Sie den App-V-Client-Cache mithilfe von Leistungsindikatoren
author: dansimp
ms.assetid: 49d6c3f2-68b8-4c69-befa-7598a8737d05
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 396cceaf9a3bde661200be2771a85596a512732f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806984"
---
# So verwalten Sie den App-V-Client-Cache mithilfe von Leistungsindikatoren


Mit dem folgenden Verfahren können Sie ermitteln, wie viel freier Speicherplatz im Application Virtualization (App-V)-Clientcache verfügbar ist, indem Sie die Informationen mithilfe des Systemmonitors grafisch darstellen. Diese Informationen werden auf dem Clientcomputer von einem Leistungsindikator mit dem Namen "App virt-Client Cache" erfasst und enthalten die folgenden Leistungsindikatoren: "Cachegröße (MB)", "Zwischenspeicher Platz (MB)" und "% freier Speicherplatz".

**So ermitteln Sie die Verwendung des Clientcache Speichers**

1.  Öffnen Sie eine Eingabeaufforderung als Administrator, oder klicken Sie auf **Start**, **Ausführen**, geben Sie **perfmon.exe**ein, und klicken Sie auf **OK**.

2.  Klicken Sie je nach verwendetem Windows-Betriebssystem auf das Tool Leistungsmonitor oder Systemmonitor, nachdem das MMC-Fenster geöffnet wurde.

3.  Um Leistungsindikatoren hinzuzufügen, klicken Sie mit der rechten Maustaste auf den Diagrammbereich, und wählen Sie **Indikatoren hinzufügen**aus.

4.  Klicken Sie auf die Dropdownliste, um die Liste der verfügbaren Leistungsindikatoren anzuzeigen, Scrollen Sie, um den **App virt-Client Cache**zu finden, und fügen Sie dann die drei Leistungsindikatoren hinzu.

    **Wichtig**  Da die App-V-Leistungsindikatoren in einer 32-Bit-DLL implementiert sind, müssen Sie den folgenden Befehl verwenden, um die 32-Bit-Version des Systemmonitors zu starten: **MMC/32 Perfmon. msc**. Dieser Befehl muss direkt auf dem Computer ausgeführt werden, der überwacht wird, und kann nicht zum Überwachen eines Remotecomputers, auf dem ein 64-Bit-Betriebssystem ausgeführt wird, verwendet werden.

     

## Verwandte Themen


[So verwalten Sie virtuelle Anwendungen über die Befehlszeile](how-to-manage-virtual-applications-by-using-the-command-line.md)

 

 





