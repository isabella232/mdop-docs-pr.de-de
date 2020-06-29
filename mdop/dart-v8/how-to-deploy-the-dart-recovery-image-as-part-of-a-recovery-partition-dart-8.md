---
title: So stellen Sie das DaRT-Wiederherstellungsabbild als Teil einer Wiederherstellungspartition bereit
description: So stellen Sie das DaRT-Wiederherstellungsabbild als Teil einer Wiederherstellungspartition bereit
author: dansimp
ms.assetid: 07c5d539-51d9-4759-adc7-72b40d5d7bb3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: e3647d684f64a0635e2875314498bde841204369
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810522"
---
# So stellen Sie das DaRT-Wiederherstellungsabbild als Teil einer Wiederherstellungspartition bereit


Nachdem Sie den Microsoft Diagnostics and Recovery Toolset (Dart) 8,0-Wiederherstellungsbild-Assistenten ausgeführt und das Wiederherstellungsabbild erstellt haben, können Sie die Datei "Boot. wim" aus der ISO-Abbilddatei extrahieren und als Wiederherstellungspartition in einem Windows 8-Abbild bereitstellen. Eine Partition wird empfohlen, da alle Beschädigungsprobleme, die das Starten des Windows-Betriebssystems verhindern, auch das Starten des Wiederherstellungs Bilds verhindern. Eine separate Partition verhindert auch, dass der BitLocker-Wiederherstellungsschlüssel zweimal bereitgestellt wird. Sie sollten die Partition ausblenden, um zu verhindern, dass Benutzer Dateien darin speichern.

**So stellen Sie Dart auf der Wiederherstellungspartition eines Windows 8-Bilds bereit**

1.  Erstellen Sie eine Zielpartition in Ihrem Windows 8-Abbild, die größer oder gleich der Größe der ISO-Abbilddatei ist, die Sie mit dem **Dart 8,0-Wiederherstellungsbild-Assistenten**erstellt haben.

    Die für eine Dart-Partition erforderliche Mindestgröße beträgt 500 MB, um die Remote Verbindungsfunktion in DART zu berücksichtigen.

2.  Extrahieren Sie die Datei "Boot. wim" aus der Dart-ISO-Abbilddatei.

    1.  Montieren Sie die ISO-Bilddatei, die Sie auf der Seite **Startabbild erstellen** erstellt haben, mithilfe der bevorzugten Methode Ihres Unternehmens.

    2.  Öffnen Sie die ISO-Abbilddatei, und kopieren Sie die Datei "Boot. wim" aus dem \\sources-Ordner im bereitgestellten Bild an einen Speicherort auf Ihrem Computer oder auf einem externen Laufwerk.

        **Hinweis**  Wenn Sie eine CD, DVD oder einen USB-Anschluss des Wiederherstellungs Bilds gebrannt haben, können Sie die Dateien auf dem Wechselmedium öffnen und die Datei "Boot. wim" aus dem \\sources-Ordner kopieren. Wenn Sie die Datei "Boot. wim" kopieren, müssen Sie das Bild nicht bereitstellen.

         

3.  Verwenden Sie die Datei "Boot. wim" zum Erstellen einer startbaren Wiederherstellungspartition mithilfe der Standardmethode Ihres Unternehmens zum Erstellen eines benutzerdefinierten Windows RE-Abbilds.

    Weitere Informationen zum Erstellen oder Anpassen einer Wiederherstellungspartition finden Sie unter [Anpassen der Windows RE-Benutzeroberfläche](https://go.microsoft.com/fwlink/?LinkId=214222).

4.  Ersetzen Sie die Zielpartition in Ihrem Windows 8-Abbild durch die Wiederherstellungspartition.

    Weitere Informationen dazu, wie Sie eine Wiederherstellungslösung bereitstellen, um das Factory-Abbild bei einem Systemfehler erneut zu installieren, finden Sie unter [Bereitstellen eines System Wiederherstellungsabbilds](https://go.microsoft.com/fwlink/?LinkId=214221).

## Verwandte Themen


[Erstellen des DaRT 8.0-Wiederherstellungsabbilds](creating-the-dart-80-recovery-image-dart-8.md)

[Bereitstellen der DaRT-Recovery-Images](deploying-the-dart-recovery-image-dart-8.md)

[Planen von DaRT 8.0](planning-for-dart-80-dart-8.md)

 

 





