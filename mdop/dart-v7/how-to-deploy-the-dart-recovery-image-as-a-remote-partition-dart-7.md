---
title: Bereitstellen des DaRT-Wiederherstellungsabbilds in einer Remotepartition
description: Bereitstellen des DaRT-Wiederherstellungsabbilds in einer Remotepartition
author: dansimp
ms.assetid: 757c9340-8eac-42e8-85de-4302e436713a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: a3acdbf72a2c6dac0238f868c7280f1c389b1311
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810033"
---
# Bereitstellen des DaRT-Wiederherstellungsabbilds in einer Remotepartition


Nachdem Sie den Dart-Wiederherstellungsbild-Assistenten ausgeführt und das Wiederherstellungsabbild erstellt haben, können Sie die Datei "Boot. wim" aus der ISO-Abbilddatei extrahieren und als Remotepartition im Netzwerk bereitstellen.

**So stellen Sie Dart als Remotepartition bereit**

1.  Extrahieren Sie die Datei "Boot. wim" aus der Dart-ISO-Abbilddatei.

    1.  Montieren Sie die ISO-Bilddatei, die Sie im Dialogfeld **Startabbild erstellen** erstellt haben, mithilfe der bevorzugten Methode des Unternehmens zum Einbinden eines Bilds.

    2.  Öffnen Sie die ISO-Abbilddatei, und kopieren Sie die Datei "Boot. wim" aus dem \\sources-Ordner im bereitgestellten Bild an einen Speicherort auf Ihrem Computer oder auf einem externen Laufwerk.

        **Hinweis**  Wenn Sie eine CD oder DVD des Wiederherstellungsabbilds gebrannt haben, können Sie die Dateien auf der CD oder DVD öffnen und die Datei "Boot. wim" aus dem \\sources-Ordner kopieren. Damit können Sie die Notwendigkeit überspringen, das Bild bereitzustellen.

         

2.  Stellen Sie die Datei "Boot. wim" auf einem WDS-Server bereit, auf den von Endbenutzercomputern in Ihrem Unternehmen aus zugegriffen werden kann.

3.  Konfigurieren Sie den WDS-Server so, dass die Boot. WIM-Datei für Dart verwendet wird, indem Sie die Standard Bereitstellungsverfahren für WDS befolgen.

Weitere Informationen zum Bereitstellen von Dart als Remotepartition finden Sie unter den folgenden Themen:

-   [Exemplarische Vorgehensweise: Bereitstellen eines Bilds mithilfe von PXE](https://go.microsoft.com/fwlink/?LinkId=212108)

-   [Leitfaden für Windows-Bereitstellungsdienste – erste Schritte](https://go.microsoft.com/fwlink/?LinkId=212106)

## Verwandte Themen


[Bereitstellen der Wiederherstellungsabbilder von DaRT 7.0](deploying-the-dart-70-recovery-image-dart-7.md)

 

 





