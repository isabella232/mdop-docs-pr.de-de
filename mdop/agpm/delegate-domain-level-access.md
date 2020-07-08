---
title: Delegieren des Domänenebenenzugriffs
description: Delegieren des Domänenebenenzugriffs
author: dansimp
ms.assetid: 64c8e773-38cc-4991-9ed2-5a801094d06e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7eb4c33e60b0d995e45fca6c9e91a26c30dd4a7f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808531"
---
# Delegieren des Domänenebenenzugriffs


Richten Sie eine Delegierung für Ihre Umgebung ein, damit Gruppenrichtlinienadministratoren über den entsprechenden Zugriff auf und die Kontrolle über Gruppenrichtlinienobjekte (Group Policy Objects, GPOs) verfügen. Es gibt Baseline-Berechtigungen, die Sie anwenden können, um den Betrieb von Advanced Group Policy Management (AGPM) effizienter zu gestalten. Sie können Berechtigungen auf jede Art und Weise erteilen, die den Anforderungen Ihrer Organisation entspricht.

Zum Ausführen dieses Verfahrens ist ein Benutzerkonto mit der Rolle AGPM-Administrator (Vollzugriff) oder den erforderlichen Berechtigungen in der erweiterten Gruppenrichtlinienverwaltung erforderlich. Lesen Sie die Details unter "Weitere Überlegungen" in diesem Thema.

**So delegieren Sie den Zugriff, damit Benutzer und Gruppen über die entsprechenden Berechtigungen für alle GPOs in einer Domäne verfügen**

1.  Klicken Sie in der Struktur der **Gruppenrichtlinien-Verwaltungskonsole** in der Gesamtstruktur und Domäne, in der Sie GPOs verwalten möchten, auf **Steuerelement ändern** .

2.  Klicken Sie auf die Registerkarte **Domänendelegierung** , und klicken Sie dann auf die Schaltfläche **erweitert** .

3.  Klicken Sie im Dialogfeld **Berechtigungen** auf das Kontrollkästchen für jede Rolle, die einer Person zugewiesen werden soll, und klicken Sie dann auf die Schaltfläche **erweitert** .

    **Hinweis**  Editor und Genehmiger sind Berechtigungen für Bearbeiter.

     

4.  Wählen Sie im Dialogfeld **Erweiterte Sicherheitseinstellungen** einen Gruppenrichtlinienadministrator aus, und klicken Sie dann auf **Bearbeiten**.

5.  Wählen Sie für **anwenden auf**die Option **dieses Objekt und verschachtelte Objekte**aus, konfigurieren Sie alle speziellen Berechtigungen über die standardmäßigen AGPM-Rollen hinaus, und klicken Sie dann im Dialogfeld **Berechtigungs** **Eintrag** auf **OK** .

6.  Klicken Sie im Dialogfeld **Erweiterte Sicherheitseinstellungen** auf **OK**.

7.  Klicken Sie im Dialogfeld **Berechtigungen** auf **OK**.

### Weitere Überlegungen

-   Standardmäßig müssen Sie ein AGPM-Administrator (Vollzugriff) sein, um dieses Verfahren ausführen zu können. Insbesondere müssen Sie die Berechtigung zum **Ändern der Sicherheit** für die Domäne besitzen.

-   Wenn Sie den Lesezugriff an Gruppenrichtlinienadministratoren delegieren möchten, die AGPM verwenden, müssen Sie Ihnen **Listeninhalte** und Berechtigungen zum **Lesen von Einstellungen** erteilen. Dadurch können Sie GPOs auf der Registerkarte **Inhalt** von AGPM anzeigen. Legen Sie die Berechtigung für **dieses Objekt und verschachtelte Objekte**auf. Andere Berechtigungen müssen explizit delegiert werden.

-   Editoren muss die **Lese** Berechtigung für die bereitgestellte Kopie eines GPO gewährt werden, damit die Gruppenrichtlinien-Software Installation vollständig genutzt werden kann.

-   Die Mitgliedschaft in der Gruppe Richtlinien Ersteller-Besitzer sollte eingeschränkt sein, damit Sie nicht zur Umgehung der AGPM-Verwaltung des Zugriffs auf GPOs verwendet wird. (Klicken Sie in der **Gruppenrichtlinien-Verwaltungskonsole**auf **Gruppenrichtlinienobjekte** in der Gesamtstruktur und Domäne, in der Sie GPOs verwalten möchten, klicken Sie auf **Delegierung**, und konfigurieren Sie dann die Einstellungen, um die Anforderungen Ihrer Organisation zu erfüllen.)

### Weitere Verweise

-   [Durchführen von AGPM-Administratoraufgaben](performing-agpm-administrator-tasks.md)

 

 





