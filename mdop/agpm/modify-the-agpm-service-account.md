---
title: Ändern des AGPM-Dienstkontos
description: Ändern des AGPM-Dienstkontos
author: dansimp
ms.assetid: 0d8d8c7b-f299-4fee-8414-406492156942
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0672ceed2fba17060e17d2ffcfa264da458b9897
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808340"
---
# Ändern des AGPM-Dienstkontos


Der AGPM-Dienst ist ein Windows-Dienst, der als Sicherheitsproxy fungiert und den Clientzugriff auf Gruppenrichtlinienobjekte (Group Policy Objects, GPOs) in der Archivierungs-und Produktionsumgebung verwaltet. Wenn dieser Dienst beendet oder deaktiviert ist, können AGPM-Clients keine Vorgänge über den Server ausführen.

Der Archivierungspfad und das AGPM-Dienstkonto werden während der Installation von AGPM Server konfiguriert und können anschließend über die **Option Software** auf dem AGPM-Server geändert werden.

**Vorsicht**  Ändern Sie die Einstellungen für den AGPM-Dienst nicht über **Administrative Tools** und **Dienste** im Betriebssystem. Dadurch kann der Start des AGPM-Diensts verhindert werden.

 

Ein Benutzerkonto, das ein Mitglied der Gruppe der Domänenadministratoren ist und Zugriff auf den AGPM-Server hat (der Computer, auf dem Microsoft Advanced Group Policy Management-Server installiert ist), ist erforderlich, um dieses Verfahren ausführen zu können.

**Wichtig**  Das AGPM-Dienstkonto muss Vollzugriff auf die GPOs haben, die es verwalten soll, und es wird die Berechtigung **Anmelden als Dienst** gewährt. Wenn Sie GPOs in einer einzelnen Domäne verwalten, können Sie das Konto Lokales System für den primären Domänencontroller als AGPM-Dienstkonto festlegen.

Wenn Sie GPOs in mehreren Domänen verwalten oder wenn es sich bei einem Mitgliedsserver um den AGPM-Server handelt, sollten Sie ein anderes Konto als AGPM-Dienstkonto konfigurieren, da das lokale System Konto für einen Domänencontroller nicht auf GPOs in anderen Domänen zugreifen kann.

 

**So ändern Sie das AGPM-Dienstkonto**

1.  Klicken Sie auf dem Computer, auf dem Microsoft Advanced Group Policy Management-Server installiert ist, auf **Start**, klicken Sie auf **System**Steuerung, klicken Sie auf **Programme hinzufügen oder entfernen**.

2.  Klicken Sie auf **Microsoft Advanced Group Policy Management-Server**, und klicken Sie dann auf **ändern**.

3.  Klicken Sie auf **weiter**, und klicken Sie dann auf **ändern**.

4.  Folgen Sie den Anweisungen auf dem Bildschirm, um die Einstellungen für den AGPM-Dienst zu konfigurieren:

    1.  Für den Archivierungspfad bestätigen oder ändern Sie den Speicherort für das Archiv relativ zum AGPM-Server. Der Archivierungspfad kann auf einen Ordner auf dem AGPM-Server oder an anderer Stelle verweisen, aber der Speicherort sollte über genügend Speicherplatz zum Speichern aller GPOs und Verlaufsdaten verfügen, die von diesem AGPM-Server verwaltet werden.

    2.  Geben Sie neue Anmeldeinformationen für das AGPM-Dienstkonto ein.

    3.  Geben Sie für den Archiv Besitzer die Anmeldeinformationen eines AGPM-Administrators (Vollzugriff) ein.

5.  Klicken Sie auf **ändern**, und klicken Sie nach Abschluss der Installation auf **Fertig stellen**.

### Weitere Verweise

-   [Verwalten des AGPM-Dienstes](managing-the-agpm-service.md)

 

 





