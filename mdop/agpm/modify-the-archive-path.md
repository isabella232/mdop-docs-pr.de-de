---
title: Ändern des Archivpfads
description: Ändern des Archivpfads
author: dansimp
ms.assetid: 6d90daf9-58db-4166-b5b3-e84bb261164a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1fc6ba2bf415d3d1bc67144d0dec1030c6173026
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808328"
---
# Ändern des Archivpfads


Der Archivpfad ist der Speicherort des Archivs relativ zum AGPM-Server. Der Archivpfad kann auf einen Ordner auf dem AGPM-Server oder auf einem anderen Server in derselben Gesamtstruktur verweisen.

Der Archivierungspfad und das AGPM-Dienstkonto werden während der Installation von AGPM Server konfiguriert und können anschließend über die **Option Software** auf dem AGPM-Server geändert werden.

Ein Benutzerkonto, das ein Mitglied der Gruppe der Domänenadministratoren ist und Zugriff auf den AGPM-Server hat (der Computer, auf dem Microsoft Advanced Group Policy Management-Server installiert ist), ist erforderlich, um dieses Verfahren ausführen zu können.

**So ändern Sie den Archivpfad**

1.  Klicken Sie auf dem Computer, auf dem Microsoft Advanced Group Policy Management-Server installiert ist, auf **Start**, klicken Sie auf **System**Steuerung, klicken Sie auf **Programme hinzufügen oder entfernen**.

2.  Klicken Sie auf **Microsoft Advanced Group Policy Management-Server**, und klicken Sie dann auf **ändern**.

3.  Klicken Sie auf **weiter**, und klicken Sie dann auf **ändern**.

4.  Folgen Sie den Anweisungen auf dem Bildschirm, um die Einstellungen für den AGPM-Dienst zu konfigurieren:

    1.  Geben Sie für den Archivpfad einen neuen Speicherort für das Archiv relativ zum AGPM-Server ein. Der Archivierungspfad kann auf einen Ordner auf dem AGPM-Server oder an anderer Stelle verweisen, aber der Speicherort sollte über genügend Speicherplatz zum Speichern aller GPOs und Verlaufsdaten verfügen, die von diesem AGPM-Server verwaltet werden.

    2.  Geben Sie die Anmeldeinformationen für das AGPM-Dienstkonto ein.

        **Wichtig**  Durch Ändern der Installation werden die Anmeldeinformationen für das AGPM-Dienstkonto gelöscht. Sie müssen die Anmeldeinformationen erneut eingeben, sind aber nicht für die Übereinstimmung mit den Anmeldeinformationen erforderlich, die während der ursprünglichen Installation verwendet wurden.

        Das AGPM-Dienstkonto muss Vollzugriff auf die GPOs haben, die es verwalten soll. Wenn Sie GPOs in einer einzelnen Domäne verwalten, können Sie das Konto Lokales System für den primären Domänencontroller als AGPM-Dienstkonto festlegen.

        Wenn Sie GPOs in mehreren Domänen verwalten oder wenn es sich bei einem Mitgliedsserver um den AGPM-Server handelt, sollten Sie ein anderes Konto als AGPM-Dienstkonto konfigurieren, da das lokale System Konto für einen Domänencontroller nicht auf GPOs in anderen Domänen zugreifen kann.

         

    3.  Geben Sie für den Archiv Besitzer die Anmeldeinformationen eines AGPM-Administrators (Vollzugriff) ein.

5.  Klicken Sie auf **ändern**, und klicken Sie nach Abschluss der Installation auf **Fertig stellen**.

### Weitere Verweise

-   [Verwalten des AGPM-Dienstes](managing-the-agpm-service.md)

 

 





