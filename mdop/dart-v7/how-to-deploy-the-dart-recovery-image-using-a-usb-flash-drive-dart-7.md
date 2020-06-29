---
title: So stellen Sie das DaRT-Wiederherstellungsabbild über ein USB-Flashlaufwerk bereit
description: So stellen Sie das DaRT-Wiederherstellungsabbild über ein USB-Flashlaufwerk bereit
author: dansimp
ms.assetid: 5b7aa843-731e-47e7-b5f9-48d08da732d6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 1228c9cb5f870162f285d726d48721dde1185107
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810093"
---
# So stellen Sie das DaRT-Wiederherstellungsabbild über ein USB-Flashlaufwerk bereit


Nachdem Sie den Bild-Assistenten für die **Dart-Wiederherstellung**ausgeführt haben, können Sie das Tool unter verwenden, um <https://go.microsoft.com/fwlink/?LinkId=218888> die ISO-Bilddatei auf ein USB-Flashlaufwerk (USB-Stick) zu kopieren.

Sie können die ISO-Abbilddatei auch manuell auf ein USB-Flashlaufwerk kopieren, indem Sie die Schritte in diesem Abschnitt ausführen.

**So speichern Sie das DART-Wiederherstellungsabbild auf einem USB-Speicherstick**

1.  Formatieren Sie den USB-Speicherstick.

    1.  Legen Sie in einer laufenden gültigen Betriebssystem-oder windowsPE-Sitzung Ihr USB-Flashlaufwerk ein.

    2.  Geben Sie an der Eingabeaufforderung mit Administratorberechtigungen **DiskPart** ein, und geben Sie dann **List Disk**ein.

        Das Eingabeaufforderungsfenster zeigt die Datenträgernummer Ihres USB-Flashlaufwerks an, beispielsweise **Datenträger 1**.

    3.  Geben Sie die folgenden Befehle einzeln an der Eingabeaufforderung ein.

        ``` syntax
        SELECT DISK 1
        CLEAN
        CREATE PARTITION PRIMARY
        SELECT PARTITION 1
        ACTIVE
        FORMAT FS=NTFS
        ASSIGN
        EXIT
        ```

        **Hinweis**  Im vorherigen Codebeispiel wird davon ausgegangen, dass Disk1 das USB-Laufwerk ist. Wenn dies erforderlich ist, ersetzen Sie Datenträger 1 durch ihre Datenträgernummer.

         

2.  Wenn Sie die bevorzugte Methode Ihres Unternehmens zum Montieren eines Bilds verwenden, montieren Sie die ISO-Bilddatei, die Sie im Dialogfeld **Startabbild erstellen** des **Dart-Assistenten**für die Bildwiederherstellung erstellt haben. Dies erfordert, dass Sie eine Methode zum Bereitstelleneiner Bilddatei zur Verfügung haben.

3.  Öffnen Sie die bereitgestellte ISO-Abbilddatei, und kopieren Sie den gesamten Inhalt auf den formatierten USB-Stick.

    **Hinweis**  Wenn Sie eine CD oder DVD des Wiederherstellungsabbilds gebrannt haben, können Sie die Dateien auf der CD oder DVD öffnen und den Inhalt auf das USB-Flashlaufwerk kopieren. Damit können Sie die Notwendigkeit überspringen, das Bild bereitzustellen.

     

## Verwandte Themen


[Bereitstellen der Wiederherstellungsabbilder von DaRT 7.0](deploying-the-dart-70-recovery-image-dart-7.md)

 

 





