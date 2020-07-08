---
title: Ändern des AGPM-Diensts
description: Ändern des AGPM-Diensts
author: dansimp
ms.assetid: 3239d088-bb86-4ec4-bc56-dbe8f1c710f5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: be39b170ef4cdc14c0f447bb6bd09a4ea92c82fe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808331"
---
# Ändern des AGPM-Diensts


Der AGPM-Dienst ist ein Windows-Dienst, der als Sicherheitsproxy fungiert und den Clientzugriff auf Gruppenrichtlinienobjekte (Group Policy Objects, GPOs) in der Archivierungs-und Produktionsumgebung der Domäne verwaltet. Wenn dieser Dienst beendet oder deaktiviert ist, können AGPM-Clients keine Vorgänge über den Server ausführen. Sie können den Archivierungspfad, das AGPM-Dienstkonto und den Port ändern, auf den der AGPM-Dienst lauscht.

**Vorsicht**  Ändern Sie die Einstellungen für den AGPM-Dienst nicht über **Administrative Tools** und **Dienste** im Betriebssystem. Dadurch kann der Start des AGPM-Diensts verhindert werden.

 

Ein Benutzerkonto, das ein Mitglied der Gruppe der Domänenadministratoren ist und Zugriff auf den AGPM-Server hat (der Computer, auf dem Microsoft Advanced Group Policy Management-Server installiert ist), ist erforderlich, um dieses Verfahren ausführen zu können. Darüber hinaus müssen Sie die Anmeldeinformationen für das AGPM-Dienstkonto angeben, um dieses Verfahren ausführen zu können.

**So ändern Sie den AGPM-Dienst**

1.  Klicken Sie auf dem Computer, auf dem Microsoft Advanced Group Policy Management-Server installiert ist, auf **Start**, **System**Steuerung, **Programme**und **Programme und Funktionen**.

2.  Klicken Sie mit der rechten Maustaste auf **Microsoft Advanced Group Policy Management-Server**, und klicken Sie dann auf **ändern**.

3.  Klicken Sie auf **weiter**, und klicken Sie dann auf **ändern**.

4.  Befolgen Sie die Anweisungen zum Konfigurieren des AGPM-Diensts:

    1.  Geben Sie im Dialogfeld **Archivpfad** einen neuen Speicherort für das Archiv relativ zum AGPM-Server ein, oder bestätigen Sie den aktuellen Archivierungspfad, und klicken Sie dann auf **weiter**.

        **Wichtig**  Der Archivierungspfad kann auf einen Ordner auf dem AGPM-Server oder an anderer Stelle verweisen, aber der Speicherort sollte über genügend Speicherplatz zum Speichern aller GPOs und Verlaufsdaten verfügen, die von diesem AGPM-Server verwaltet werden.

         

    2.  Geben Sie im Dialogfeld **AGPM-Dienstkonto** die Anmeldeinformationen für ein Dienstkonto ein, unter dem der AGPM-Dienst ausgeführt werden soll, und klicken Sie auf **weiter**.

        **Wichtig**  Durch Ändern der Installation werden die Anmeldeinformationen für das AGPM-Dienstkonto gelöscht. Sie müssen die Anmeldeinformationen erneut eingeben, sind aber nicht für die Übereinstimmung mit den Anmeldeinformationen erforderlich, die während der ursprünglichen Installation verwendet wurden.

        Das AGPM-Dienstkonto muss Vollzugriff auf die GPOs haben, die es verwalten soll, und es wird die Berechtigung **Anmelden als Dienst** gewährt. Wenn Sie GPOs in einer einzelnen Domäne verwalten, können Sie das Konto Lokales System für den primären Domänencontroller als AGPM-Dienstkonto festlegen.

        Wenn Sie GPOs in mehreren Domänen verwalten oder wenn es sich bei einem Mitgliedsserver um den AGPM-Server handelt, sollten Sie ein anderes Konto als AGPM-Dienstkonto konfigurieren, da das lokale System Konto für einen Domänencontroller nicht auf GPOs in anderen Domänen zugreifen kann.

         

    3.  Geben Sie im Dialogfeld **Besitzer des Archivs** den Benutzernamen eines AGPM-Administrators (Vollzugriff) oder einer Gruppe von AGPM-Administratoren ein, und klicken Sie auf **weiter**.

        **Hinweis**  Durch Ändern der Installation werden die Anmeldeinformationen für den Besitzer des Archivs gelöscht. Sie müssen die Anmeldeinformationen erneut eingeben, sind aber nicht für die Übereinstimmung mit den Anmeldeinformationen erforderlich, die während der ursprünglichen Installation verwendet wurden.

         

    4.  Geben Sie im Dialogfeld **Port Konfiguration** einen neuen Port ein, an dem der AGPM-Dienst den aktuell ausgewählten Port überwachen oder bestätigen soll, und klicken Sie auf **weiter**.

        **Hinweis**  Standardmäßig überwacht der AGPM-Dienst Port 4600.

        Wenn Sie Portausnahmen manuell konfigurieren oder Regeln zum Konfigurieren von Portausnahmen haben, können Sie das Kontrollkästchen **Portausnahme zu Firewall hinzufügen** deaktivieren.

         

5.  Klicken Sie auf **ändern**, und klicken Sie nach Abschluss der Installation auf **Fertig stellen**.

6.  Wenn Sie den Port geändert haben, auf dem der AGPM-Dienst lauscht, ändern Sie den Port in der AGPM-Server Verbindung für jeden Gruppenrichtlinienadministrator. (Weitere Informationen finden Sie unter [Konfigurieren von AGPM-Server Verbindungen](configure-agpm-server-connections-agpm40.md).)

7.  Wiederholen Sie diesen Vorgang für jeden AGPM-Server, auf den die Konfigurationsänderungen angewendet werden sollen.

### Weitere Verweise

-   [Verwalten des AGPM-Dienstes](managing-the-agpm-service-agpm40.md)

 

 





