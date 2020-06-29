---
title: Sichern des Archivs
description: Sichern des Archivs
author: dansimp
ms.assetid: 538d85eb-3596-4c1d-bbd7-26bc28857c28
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8c6888d61e126d603aefa4e818f1070c5a493ea6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807816"
---
# Sichern des Archivs


Um bei der Wiederherstellung des Archivs für erweiterte Gruppenrichtlinienverwaltung (AGPM) bei einem Notfall zu helfen, sollte ein AGPM-Administrator (Vollzugriff) das Archiv häufig sichern. Standardmäßig wird das Archiv in%ProgramData%\\Microsoft\\AGPM. erstellt. Sie können jedoch während der Einrichtung des Microsoft Advanced Group Policy Management-Servers einen anderen Pfad angeben.

Ein Benutzerkonto, das Zugriff auf den AGPM-Server hat – den Computer, auf dem der AGPM-Dienst installiert ist – und auf den Ordner, der das Archiv enthält, ist erforderlich, um dieses Verfahren auszuführen.

**So sichern Sie das Archiv**

1.  Beenden Sie den AGPM-Dienst. Weitere Informationen finden Sie unter [starten und Beenden des AGPM-Diensts](start-and-stop-the-agpm-service-agpm40.md).

2.  Sichern Sie den Archivordner mithilfe von Windows-Explorer, xcopy, Windows Server®-Sicherung oder einem anderen Sicherungstool. Stellen Sie sicher, dass Sie versteckte, System-und schreibgeschützte Dateien sichern.

3.  Speichern Sie die Archivsicherung an einem sicheren Ort.

4.  Starten Sie den AGPM-Dienst erneut. Weitere Informationen finden Sie unter [starten und Beenden des AGPM-Diensts](start-and-stop-the-agpm-service-agpm40.md).

**Hinweis**  Wenn ein AGPM-Administrator das Archiv selten zurückgibt, sind die Gruppenrichtlinienobjekte (Group Policy Objects, GPOs) in der Archivsicherung nicht aktuell. Um sicherzustellen, dass die Archivsicherung aktuell ist, sichern Sie das Archiv im Rahmen der täglichen Backup-Strategie Ihrer Organisation.

 

### Weitere Verweise

-   [Wiederherstellen des Archivs aus einer Sicherung](restore-the-archive-from-a-backup-agpm40.md)

-   [Verschieben des AGPM-Servers und -Archivs](move-the-agpm-server-and-the-archive-agpm40.md)

-   [Verwalten des Archivs](managing-the-archive-agpm40.md)

 

 





