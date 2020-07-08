---
title: Delegieren des Zugriffs auf ein einzelnes Gruppenrichtlinienobjekt im Archiv
description: Delegieren des Zugriffs auf ein einzelnes Gruppenrichtlinienobjekt im Archiv
author: dansimp
ms.assetid: 284d2aa2-7c10-4ffa-8978-bbe30867c1c1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9da2a699568f961d030b05a966b76e08aef3aec8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808547"
---
# Delegieren des Zugriffs auf ein einzelnes Gruppenrichtlinienobjekt im Archiv


Als AGPM-Administrator (Vollzugriff) können Sie die Verwaltung eines kontrollierten Gruppenrichtlinienobjekts (GPO) im Archiv delegieren, damit es von ausgewählten Gruppen und Herausgebern bearbeitet werden kann, Prüfer Sie überprüfen können und von genehmigenden Personen genehmigt werden können.

Ein Benutzerkonto mit der Rolle AGPM-Administrator (Vollzugriff), dem Benutzerkonto der genehmigenden Person, die das Gruppenrichtlinienobjekt erstellt hat, oder ein Benutzerkonto mit den erforderlichen Berechtigungen in der erweiterten Gruppenrichtlinienverwaltung (Group Policy Management, AGPM) ist erforderlich, um dieses Verfahren ausführen zu können. Lesen Sie die Details unter "Weitere Überlegungen" in diesem Thema.

**So delegieren Sie die Verwaltung eines kontrollierten Gruppenrichtlinienobjekts**

1.  Klicken Sie in der Struktur der **Gruppenrichtlinien-Verwaltungskonsole** in der Gesamtstruktur und Domäne, in der Sie GPOs verwalten möchten, auf **Steuerelement ändern** .

2.  Klicken Sie im Detailbereich auf der Registerkarte **Inhalt** auf die Registerkarte **gesteuert** , um gesteuerte GPOs anzuzeigen, und klicken Sie dann auf das zu delegierende Gruppenrichtlinienobjekt:

    1.  Klicken Sie zum Hinzufügen von Zugriff für einen Benutzer oder eine Gruppe auf die Schaltfläche **Hinzufügen** , wählen Sie den Benutzer oder die Gruppe aus, und klicken Sie auf **OK**. Wählen Sie im Dialogfeld **Gruppe oder Benutzer hinzufügen** eine Rolle aus, und klicken Sie auf **OK**.

    2.  Wenn Sie den Zugriff für einen Benutzer oder eine Gruppe entfernen möchten, wählen Sie den Benutzer oder die Gruppe aus, und klicken Sie auf die Schaltfläche **Entfernen** .

        **Hinweis**  Wenn ein Benutzer oder eine Gruppe domänenweiten Zugriff erbt, ist die Schaltfläche **Entfernen** nicht verfügbar. Sie können den domänenweiten Zugriff auf der Registerkarte **Domänendelegierung** ändern.

         

    3.  Wenn Sie die Rollen und Berechtigungen ändern möchten, die an einen Benutzer oder eine Gruppe delegiert wurden, klicken Sie auf die Schaltfläche **erweitert** . Wählen Sie im Dialogfeld **Berechtigungen** den Benutzer oder die Gruppe aus, aktivieren Sie das Kontrollkästchen für jede Rolle, die diesem Benutzer oder dieser Gruppe zugewiesen werden soll, und klicken Sie auf **OK**.

        **Hinweis**  Editor und Genehmiger sind Berechtigungen für Bearbeiter.

         

### Weitere Überlegungen

-   Standardmäßig müssen Sie die genehmigende Person sein, die das Gruppenrichtlinienobjekt erstellt oder kontrolliert hat, oder einen AGPM-Administrator (Vollzugriff), um dieses Verfahren ausführen zu können. Insbesondere müssen Sie über die Berechtigung **Listeninhalt** für die Domäne und die Berechtigung zum **Ändern der Sicherheit** für das Gruppenrichtlinienobjekt verfügen.

-   Wenn Sie den Lesezugriff an Gruppenrichtlinienadministratoren delegieren möchten, die AGPM verwenden, müssen Sie Ihnen **Listeninhalte** und Berechtigungen zum **Lesen von Einstellungen** erteilen. Dadurch können Sie GPOs auf der Registerkarte **Inhalt** von AGPM anzeigen. Andere Berechtigungen müssen explizit delegiert werden.

-   Redakteure müssen über die Berechtigung " **Lesen** " für die bereitgestellte Kopie eines Gruppenrichtlinienobjekts verfügen, um die Gruppenrichtlinien-Software Installation vollständig nutzen zu können.

-   Die Mitgliedschaft in der Gruppe Richtlinien Ersteller-Besitzer sollte eingeschränkt sein, soit wird nicht verwendet, um die AGPM-Verwaltung des Zugriffs auf GPOs zu umgehen. (Klicken Sie in der **Gruppenrichtlinien-Verwaltungskonsole**auf **Gruppenrichtlinienobjekte** in der Gesamtstruktur und Domäne, in der Sie GPOs verwalten möchten, klicken Sie auf **Delegierung**, und konfigurieren Sie dann die Einstellungen, um die Anforderungen Ihrer Organisation zu erfüllen.)

### Weitere Verweise

-   [Verwalten des Archivs](managing-the-archive-agpm40.md)

 

 





