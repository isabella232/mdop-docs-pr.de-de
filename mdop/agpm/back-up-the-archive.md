---
title: Sichern des Archivs
description: Sichern des Archivs
author: dansimp
ms.assetid: 400176da-3518-4475-ad19-c96cda6ca7ba
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8a75099e7a6624850ee0511cf65feddf63909a0c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807815"
---
# Sichern des Archivs


Um bei der Wiederherstellung des Archivs für erweiterte Gruppenrichtlinienverwaltung (AGPM) bei einem Notfall zu helfen, sollte ein AGPM-Administrator (Vollzugriff) das Archiv häufig sichern. Standardmäßig wird das Archiv in%ProgramData%\\Microsoft\\AGPM. erstellt. Sie können jedoch während der Einrichtung des Microsoft Advanced Group Policy Management-Servers einen anderen Pfad angeben.

Ein Benutzerkonto, das Zugriff auf den AGPM-Server hat – den Computer, auf dem der AGPM-Dienst installiert ist – und auf den Ordner, der das Archiv enthält, ist erforderlich, um dieses Verfahren auszuführen.

**So sichern Sie das Archiv**

1.  Beenden Sie den AGPM-Dienst. Weitere Informationen finden Sie unter [starten und Beenden des AGPM-Diensts](start-and-stop-the-agpm-service-agpm30ops.md).

2.  Sichern Sie den Archivordner mithilfe von Windows-Explorer, xcopy, Windows Server®-Sicherung oder einem anderen Sicherungstool. Stellen Sie sicher, dass Sie versteckte, System-und schreibgeschützte Dateien sichern.

3.  Speichern Sie die Archivsicherung an einem sicheren Ort.

4.  Starten Sie den AGPM-Dienst erneut. Weitere Informationen finden Sie unter [starten und Beenden des AGPM-Diensts](start-and-stop-the-agpm-service-agpm30ops.md).

**Hinweis**  Wenn ein AGPM-Administrator das Archiv selten zurückgibt, sind die Gruppenrichtlinienobjekte (Group Policy Objects, GPOs) in der Archivsicherung nicht aktuell. Um sicherzustellen, dass die Archivsicherung aktuell ist, sichern Sie das Archiv im Rahmen der täglichen Backup-Strategie Ihrer Organisation.

 

### Weitere Verweise

-   [Wiederherstellen des Archivs aus einer Sicherung](restore-the-archive-from-a-backup.md)

-   [Verschieben des AGPM-Servers und -Archivs](move-the-agpm-server-and-the-archive.md)

-   [Verwalten des Archivs](managing-the-archive.md)

 

 





