---
title: Delegieren des Domänenebenenzugriffs auf das Archiv
description: Delegieren des Domänenebenenzugriffs auf das Archiv
author: dansimp
ms.assetid: d232069e-71d5-4b4d-b22e-bef11de1cfd4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 01fbc4964493da6ba40382ac40671922eeffa30e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808535"
---
# Delegieren des Domänenebenenzugriffs auf das Archiv


Richten Sie eine Delegierung für Ihre Umgebung ein, damit Gruppenrichtlinienadministratoren über den entsprechenden Zugriff auf und die Kontrolle über Gruppenrichtlinienobjekte (Group Policy Objects, GPOs) im Archiv verfügen. Es gibt Baseline-Berechtigungen, die Sie anwenden können, um den Vorgang effizienter zu gestalten. Sie können Berechtigungen auf jede Art und Weise erteilen, die den Anforderungen Ihrer Organisation entspricht.

Zum Ausführen dieses Verfahrens ist ein Benutzerkonto mit der Rolle AGPM-Administrator (Vollzugriff) oder den erforderlichen Berechtigungen in Advanced Group Policy Management (AGPM) erforderlich. Lesen Sie die Details unter "Weitere Überlegungen" in diesem Thema.

**So delegieren Sie den Zugriff, damit Benutzer und Gruppen über die entsprechenden Berechtigungen für alle GPOs in einer Domäne verfügen**

1.  Klicken Sie in der Struktur der **Gruppenrichtlinien-Verwaltungskonsole** in der Gesamtstruktur und Domäne, in der Sie GPOs verwalten möchten, auf **Steuerelement ändern** .

2.  Klicken Sie auf die Registerkarte **Domänendelegierung** , und konfigurieren Sie den Zugriff auf alle GPOs in der Domäne:

    1.  Klicken Sie zum Hinzufügen von Zugriff für einen Benutzer oder eine Gruppe auf die Schaltfläche **Hinzufügen** , wählen Sie den Benutzer oder die Gruppe aus, und klicken Sie auf **OK**. Wählen Sie im Dialogfeld **Gruppe oder Benutzer hinzufügen** eine Rolle aus, und klicken Sie auf **OK**.

    2.  Wenn Sie den Zugriff für einen Benutzer oder eine Gruppe entfernen möchten, wählen Sie den Benutzer oder die Gruppe aus, und klicken Sie auf die Schaltfläche **Entfernen** .

    3.  Wenn Sie die Rollen und Berechtigungen ändern möchten, die an einen Benutzer oder eine Gruppe delegiert wurden, klicken Sie auf die Schaltfläche **erweitert** . Wählen Sie im Dialogfeld **Berechtigungen** den Benutzer oder die Gruppe aus, aktivieren Sie das Kontrollkästchen für jede Rolle, die diesem Benutzer oder dieser Gruppe zugewiesen werden soll, und klicken Sie dann auf **OK**.

        **Hinweis**  Editor und Genehmiger sind Berechtigungen für Bearbeiter.

         

### Weitere Überlegungen

-   Standardmäßig müssen Sie ein AGPM-Administrator (Vollzugriff) sein, um dieses Verfahren ausführen zu können. Insbesondere müssen Sie die Berechtigung zum **Ändern der Sicherheit** für die Domäne besitzen.

-   Wenn Sie den Lesezugriff an Gruppenrichtlinienadministratoren delegieren möchten, die AGPM verwenden, müssen Sie Ihnen **Listeninhalte** und Berechtigungen zum **Lesen von Einstellungen** erteilen. Dadurch können Sie GPOs auf der Registerkarte **Inhalt** von AGPM anzeigen. Andere Berechtigungen müssen explizit delegiert werden.

-   Editoren muss die **Lese** Berechtigung für die bereitgestellte Kopie eines GPO gewährt werden, damit die Gruppenrichtlinien-Software Installation vollständig genutzt werden kann.

-   Die Mitgliedschaft in der Gruppe Richtlinien Ersteller-Besitzer sollte eingeschränkt sein, soit wird nicht verwendet, um die AGPM-Verwaltung des Zugriffs auf GPOs zu umgehen. (Klicken Sie in der **Gruppenrichtlinien-Verwaltungskonsole**auf **Gruppenrichtlinienobjekte** in der Gesamtstruktur und Domäne, in der Sie GPOs verwalten möchten, klicken Sie auf **Delegierung**, und konfigurieren Sie dann die Einstellungen, um die Anforderungen Ihrer Organisation zu erfüllen.)

### Weitere Verweise

-   [Verwalten des Archivs](managing-the-archive.md)

 

 





