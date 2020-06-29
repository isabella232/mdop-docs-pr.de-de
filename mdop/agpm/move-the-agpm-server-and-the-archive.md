---
title: Verschieben des AGPM-Servers und -Archivs
description: Verschieben des AGPM-Servers und -Archivs
author: dansimp
ms.assetid: 13cb83c4-bb42-4e81-8660-5b7540f473d8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 6ae5ba9c2346caf81f5aff9f57f6b9dc97127ad1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809403"
---
# Verschieben des AGPM-Servers und -Archivs


Wenn Sie den AGPM-Server und den Server ersetzen, auf dem das Archiv gehostet wird, müssen Sie den AGPM-Dienst und das Archiv verschieben. Wenn Sie möchten, können Sie den AGPM-Dienst und das Archiv separat verschieben.

**Hinweis:**  
-   Der AGPM-Server ist der Computer, auf dem der AGPM-Dienst gehostet wird, und der Computer, auf dem Microsoft Advanced Group Policy Management – Server installiert ist.

-   Standardmäßig wird das Archiv auf dem AGPM-Server gehostet, doch Sie können stattdessen einen Archivierungspfad angeben, um ihn auf einem anderen Server zu hosten.

 

Ein Benutzerkonto, das Mitglied der Gruppe der Domänenadministratoren ist und Zugriff auf die vorherigen und neuen AGPM-Server hat, ist erforderlich, um dieses Verfahren ausführen zu können. Darüber hinaus müssen Sie die Anmeldeinformationen für das AGPM-Dienstkonto angeben, das vom neuen AGPM-Server verwendet werden soll, um dieses Verfahren ausführen zu können.

**So verschieben Sie den AGPM-Dienst und das Archiv auf einen anderen Server oder auf einen anderen Server**

1.  Sichern Sie das Archiv. Weitere Informationen finden Sie unter [Sichern des Archivs](back-up-the-archive.md).

2.  Verschieben Sie den AGPM-Dienst:

    1.  Beenden Sie den AGPM-Dienst. Weitere Informationen finden Sie unter [starten und Beenden des AGPM-Diensts](start-and-stop-the-agpm-service-agpm30ops.md).

    2.  Installieren Sie Microsoft Advanced Group Policy Management-Server auf dem neuen Server, der den AGPM-Dienst hosten soll. Während dieses Vorgangs geben Sie den neuen Archivierungspfad, den Speicherort für das Archiv, in Bezug auf den AGPM-Server an. Weitere Informationen finden Sie unter Schritt-für-Schritt-Anleitung für Microsoft Advanced Group Policy Management 3,0 ( <https://go.microsoft.com/fwlink/?LinkId=132706> ) und Planungshandbuch für Microsoft Advanced Group Policy Management ( <https://go.microsoft.com/fwlink/?LinkId=141871> ).

    3.  Entweder ein AGPM-Administrator (Vollzugriff) muss die AGPM-Serververbindung für alle Gruppenrichtlinienadministratoren konfigurieren, die den neuen AGPM-Server verwenden und die Verbindung für den alten AGPM-Server entfernen, da sonst jeder Gruppenrichtlinienadministrator die neue AGPM-Serververbindung manuell konfigurieren und die alte AGPM-Serververbindung für das AGPM-Snap-in auf dem Computer entfernen muss. Weitere Informationen finden Sie unter [Konfigurieren von AGPM-Server Verbindungen](configure-agpm-server-connections-agpm30ops.md).

        **Hinweis**  Als bewährte Methode sollten Sie Microsoft Advanced Group Policy Management – Server vom vorherigen AGPM-Server deinstallieren. Dadurch wird sichergestellt, dass der AGPM-Dienst nicht versehentlich auf diesem Server neu gestartet werden kann und möglicherweise Verwirrung verursacht, wenn keine AGPM-Serververbindungen mehr vorhanden sind.

         

3.  Kopieren Sie das Archiv von der Sicherung auf den neuen Server, der das Archiv hosten soll. Weitere Informationen finden Sie unter [Wiederherstellen des Archivs aus einer Sicherung](restore-the-archive-from-a-backup.md).

    **Wichtig**  Wenn Sie das Archiv verschoben haben, ohne den AGPM-Dienst zur gleichen Zeit zu verschieben:

    1.  Sie müssen den Archivierungspfad so ändern, dass er auf den neuen Speicherort für das Archiv in Bezug auf den AGPM-Server verweist. Weitere Informationen finden Sie unter [Ändern des AGPM-Diensts](modify-the-agpm-service-agpm30ops.md).

    2.  Sie müssen das Kennwort erneut eingeben und auf der Registerkarte **Domänendelegierung** bestätigen. Weitere Informationen finden Sie unter [Konfigurieren von e-Mail-Benachrichtigungen](configure-e-mail-notification-agpm30ops.md).

     

### Weitere Verweise

-   [Sichern des Archivs](back-up-the-archive.md)

-   [Wiederherstellen des Archivs aus einer Sicherung](restore-the-archive-from-a-backup.md)

-   [Konfigurieren von AGPM-Server-Verbindungen](configure-agpm-server-connections-agpm30ops.md)

-   [Ändern des AGPM-Diensts](modify-the-agpm-service-agpm30ops.md)

-   Schritt-für-Schritt-Anleitung für Microsoft Advanced Group Policy Management 3,0 ( <https://go.microsoft.com/fwlink/?LinkId=132706> )

-   Planungshandbuch für Microsoft Advanced Group Policy Management ( <https://go.microsoft.com/fwlink/?LinkId=141871> )

-   [Durchführen von AGPM-Administratoraufgaben](performing-agpm-administrator-tasks-agpm30ops.md)

 

 





