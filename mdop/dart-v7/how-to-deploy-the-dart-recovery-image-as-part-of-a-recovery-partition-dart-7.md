---
title: So stellen Sie das DaRT-Wiederherstellungsabbild als Teil einer Wiederherstellungspartition bereit
description: So stellen Sie das DaRT-Wiederherstellungsabbild als Teil einer Wiederherstellungspartition bereit
author: dansimp
ms.assetid: 462f2d08-f03b-4a07-b2d3-c69205dc6f70
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: e75c3f9e58d784c13003feb84001f89c4607115d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810027"
---
# So stellen Sie das DaRT-Wiederherstellungsabbild als Teil einer Wiederherstellungspartition bereit


Nachdem Sie den Dart-Wiederherstellungsbild-Assistenten ausgeführt und das Wiederherstellungsabbild erstellt haben, können Sie die Datei "Boot. wim" aus der ISO-Abbilddatei extrahieren und als Wiederherstellungspartition in einem Windows 7-Abbild bereitstellen.

**So stellen Sie Dart auf der Wiederherstellungspartition eines Windows 7-Bilds bereit**

1.  Erstellen Sie eine Zielpartition in Ihrem Windows 7-Abbild, die größer oder gleich der Größe der ISO-Abbilddatei ist, die Sie mit dem **Dart-Bild-Assistenten**erstellt haben.

    Die für eine Dart-Partition erforderliche Mindestgröße beträgt etwa 300MB. Es wird jedoch empfohlen, 450mb gelangte für die Remote Verbindungsfunktion in DART zu unterstützen.

2.  Extrahieren Sie die Datei "Boot. wim" aus der Dart-ISO-Abbilddatei.

    1.  Montieren Sie die ISO-Bilddatei, die Sie im Dialogfeld **Startabbild erstellen** erstellt haben, mithilfe der bevorzugten Methode des Unternehmens zum Einbinden eines Bilds.

    2.  Öffnen Sie die ISO-Abbilddatei, und kopieren Sie die Datei "Boot. wim" aus dem \\sources-Ordner im bereitgestellten Bild an einen Speicherort auf Ihrem Computer oder auf einem externen Laufwerk.

        **Hinweis**  Wenn Sie eine CD oder DVD des Wiederherstellungsabbilds gebrannt haben, können Sie die Dateien auf der CD oder DVD öffnen und die Datei "Boot. wim" aus dem \\sources-Ordner kopieren. Damit können Sie die Notwendigkeit überspringen, das Bild bereitzustellen.

         

3.  Verwenden Sie die Datei "Boot. wim" zum Erstellen einer startbaren Wiederherstellungspartition mithilfe der Standardmethode Ihres Unternehmens zum Erstellen eines benutzerdefinierten Windows RE-Abbilds.

    Weitere Informationen zum Erstellen oder Anpassen einer Wiederherstellungspartition finden Sie unter [Anpassen der Windows RE-Benutzeroberfläche](https://go.microsoft.com/fwlink/?LinkId=214222).

4.  Ersetzen Sie die Zielpartition in Ihrem Windows 7-Abbild durch die Wiederherstellungspartition.

Nachdem Sie Ihr Windows 7-Abbild bereitgestellt haben, können Sie es mithilfe des standardmäßigen Bereitstellungsprozesses Ihres Unternehmens an Computer in Ihrem Unternehmen verteilen. Weitere Informationen zum Erstellen eines Windows 7-Bilds finden Sie unter Erstellen [eines Standard Abbilds von Windows 7: schrittweise Anleitung](https://go.microsoft.com/fwlink/?LinkId=212103).

Weitere Informationen dazu, wie Sie eine Wiederherstellungslösung bereitstellen, um das Factory-Abbild bei einem Systemfehler erneut zu installieren, finden Sie unter [Bereitstellen eines System Wiederherstellungsabbilds](https://go.microsoft.com/fwlink/?LinkId=214221).

## Verwandte Themen


[Bereitstellen der Wiederherstellungsabbilder von DaRT 7.0](deploying-the-dart-70-recovery-image-dart-7.md)

 

 





