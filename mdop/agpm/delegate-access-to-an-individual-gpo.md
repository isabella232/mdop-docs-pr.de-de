---
title: Delegieren des Zugriffs auf eine einzelne Gruppenrichtlinienobjekte
description: Delegieren des Zugriffs auf eine einzelne Gruppenrichtlinienobjekte
author: dansimp
ms.assetid: b2a7d550-14bf-4b41-b6e4-2cc091eedd2d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9e5d2ae8c6ef52eae39feb67b9df42e84f523300
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807624"
---
# Delegieren des Zugriffs auf eine einzelne Gruppenrichtlinienobjekte


Als AGPM-Administrator (Vollzugriff) können Sie die Verwaltung eines kontrollierten Gruppenrichtlinienobjekts (GPO) delegieren, damit ausgewählte Gruppen und Bearbeiter es bearbeiten können, Prüfer Sie überprüfen können, und Genehmiger können es genehmigen.

Ein Benutzerkonto mit der Rolle AGPM-Administrator (Vollzugriff), dem Benutzerkonto der genehmigenden Person, die das Gruppenrichtlinienobjekt erstellt hat, oder ein Benutzerkonto mit den erforderlichen Berechtigungen in der erweiterten Gruppenrichtlinienverwaltung ist erforderlich, um dieses Verfahren ausführen zu können. Lesen Sie die Details unter "Weitere Überlegungen" in diesem Thema.

**So delegieren Sie die Verwaltung eines kontrollierten Gruppenrichtlinienobjekts**

1.  Klicken Sie in der Struktur der **Gruppenrichtlinien-Verwaltungskonsole** in der Gesamtstruktur und Domäne, in der Sie GPOs verwalten möchten, auf **Steuerelement ändern** .

2.  Klicken Sie im Detailbereich auf der Registerkarte **Inhalt** auf die Registerkarte **gesteuert** , um gesteuerte GPOs anzuzeigen, und klicken Sie dann auf das zu delegierende Gruppenrichtlinienobjekt.

3.  Klicken Sie auf die Schaltfläche **Hinzufügen** , wählen Sie die Benutzer oder Gruppen aus, denen Sie Zugriff gewähren möchten, und klicken Sie dann auf **OK**.

4.  Um die Berechtigungen für die einzelnen Benutzer oder Gruppen anzupassen, klicken Sie auf der Registerkarte **Inhalt** auf die Schaltfläche **erweitert** , und überprüfen Sie die Rollen Berechtigungen auf zulassen oder ablehnen. (Wenn Sie eine genauere Steuerung haben, klicken Sie im Dialogfeld **Berechtigungen** auf **erweitert** .)

5.  Klicken Sie auf über **nehmen**, und klicken Sie dann im Dialogfeld **Berechtigungen** auf **OK** .

### Weitere Überlegungen

-   Standardmäßig müssen Sie die genehmigende Person sein, die das Gruppenrichtlinienobjekt erstellt oder kontrolliert hat, oder einen AGPM-Administrator (Vollzugriff), um dieses Verfahren ausführen zu können. Insbesondere müssen Sie über die Berechtigung **Listeninhalt** für die Domäne und die Berechtigung zum **Ändern der Sicherheit** für das Gruppenrichtlinienobjekt verfügen.

-   Wenn Sie den Lesezugriff an Gruppenrichtlinienadministratoren delegieren möchten, die AGPM verwenden, müssen Sie Ihnen **Listeninhalte** und Berechtigungen zum **Lesen von Einstellungen** erteilen. Dadurch können Sie GPOs auf der Registerkarte **Inhalt** von AGPM anzeigen. Legen Sie die Berechtigung für **dieses Objekt und verschachtelte Objekte**auf. Andere Berechtigungen müssen explizit delegiert werden.

-   Redakteure müssen über die Berechtigung " **Lesen** " für die bereitgestellte Kopie eines Gruppenrichtlinienobjekts verfügen, um die Gruppenrichtlinien-Software Installation vollständig nutzen zu können.

-   Die Mitgliedschaft in der Gruppe Richtlinien Ersteller-Besitzer sollte eingeschränkt sein, damit Sie nicht zur Umgehung der AGPM-Verwaltung des Zugriffs auf GPOs verwendet wird. (Klicken Sie in der **Gruppenrichtlinien-Verwaltungskonsole**auf **Gruppenrichtlinienobjekte** in der Gesamtstruktur und Domäne, in der Sie GPOs verwalten möchten, klicken Sie auf **Delegierung**, und konfigurieren Sie dann die Einstellungen, um die Anforderungen Ihrer Organisation zu erfüllen.)

### Weitere Verweise

-   [Durchführen von AGPM-Administratoraufgaben](performing-agpm-administrator-tasks.md)

 

 





