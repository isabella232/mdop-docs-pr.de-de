---
title: Bereitstellen des DaRT-Wiederherstellungsabbilds in einer Remotepartition
description: Bereitstellen des DaRT-Wiederherstellungsabbilds in einer Remotepartition
author: dansimp
ms.assetid: 06a5e250-b992-4f6a-ad74-e7715f9e96e7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 3cdb1313a64bacd652a5253c09f36fa792d0fa3c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804697"
---
# Bereitstellen des DaRT-Wiederherstellungsabbilds in einer Remotepartition


Nachdem Sie den Microsoft Diagnostics and Recovery Toolset (Dart) 10-Wiederherstellungsbild-Assistenten ausgeführt und das Wiederherstellungsabbild erstellt haben, können Sie die Datei "Boot. wim" aus der ISO-Abbilddatei extrahieren und als Remotepartition im Netzwerk bereitstellen.

**So stellen Sie Dart 10 als Remotepartition bereit**

1.  Extrahieren Sie die Datei "Boot. wim" aus der Dart-ISO-Abbilddatei.

    1.  Montieren Sie die ISO-Bilddatei, die Sie im Dialogfeld **Startabbild erstellen** erstellt haben, mithilfe der bevorzugten Methode des Unternehmens zum Einbinden eines Bilds.

    2.  Öffnen Sie die ISO-Abbilddatei, und kopieren Sie die Datei "Boot. wim" aus dem \\sources-Ordner im bereitgestellten Bild an einen Speicherort auf Ihrem Computer oder auf einem externen Laufwerk.

        **Hinweis**  Wenn Sie eine CD oder DVD des Wiederherstellungsabbilds gebrannt haben, können Sie die Dateien auf der CD oder DVD öffnen und die Datei "Boot. wim" aus dem \\sources-Ordner kopieren. Damit können Sie die Notwendigkeit überspringen, das Bild bereitzustellen.

         

2.  Stellen Sie die Datei "Boot. wim" auf einem WDS-Server bereit, auf den von Endbenutzercomputern in Ihrem Unternehmen aus zugegriffen werden kann.

3.  Konfigurieren Sie den WDS-Server so, dass die Boot. WIM-Datei für Dart verwendet wird, indem Sie die Standard Bereitstellungsverfahren für WDS befolgen.

Weitere Informationen zum Bereitstellen von Dart als Remotepartition finden Sie unter [Exemplarische Vorgehensweise: Bereitstellen eines Bilds mithilfe der PXE](https://go.microsoft.com/fwlink/?LinkId=212108) -und [Windows-Bereitstellungsdienste – Leitfaden für erste Schritte](https://go.microsoft.com/fwlink/?LinkId=212106).

## Verwandte Themen


[Erstellen des DaRT 10-Wiederherstellungsabbilds](creating-the-dart-10-recovery-image.md)

[Bereitstellen des DaRT-Wiederherstellungsabbilds](deploying-the-dart-recovery-image-dart-10.md)

[Planen von DaRT 10](planning-for-dart-10.md)

 

 





