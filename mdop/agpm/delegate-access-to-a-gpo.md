---
title: Delegieren des Zugriffs auf ein Gruppenrichtlinienobjekt
description: Delegieren des Zugriffs auf ein Gruppenrichtlinienobjekt
author: dansimp
ms.assetid: f1d6bb6c-d5bf-4080-a6cb-32774689f804
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 57a71528120b65676d25d952d9f9392dc0250ae4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807644"
---
# Delegieren des Zugriffs auf ein Gruppenrichtlinienobjekt


Eine genehmigende Person kann die Verwaltung eines **von dieser genehmigenden Person erstellten**kontrollierten Gruppenrichtlinienobjekts (GPO) delegieren. Wie ein AGPM-Administrator (Vollzugriff) kann die genehmigende Person den Zugriff auf ein solches Gruppenrichtlinienobjekt delegieren, sodass ausgewählte Bearbeiter Sie bearbeiten können, Prüfer Sie überprüfen können, und andere Genehmiger Sie genehmigen können. Standardmäßig kann eine genehmigende Person keinen Zugriff auf GPOs delegieren, die von einem anderen Gruppenrichtlinienadministrator erstellt wurden.

Ein Benutzerkonto mit der Rolle AGPM-Administrator (Vollzugriff), dem Benutzerkonto der genehmigenden Person, die das Gruppenrichtlinienobjekt erstellt hat, oder ein Benutzerkonto mit den erforderlichen Berechtigungen in der erweiterten Gruppenrichtlinienverwaltung ist erforderlich, um dieses Verfahren ausführen zu können. Lesen Sie die Details unter "Weitere Überlegungen" in diesem Thema.

**So delegieren Sie die Verwaltung eines kontrollierten Gruppenrichtlinienobjekts**

1.  Klicken Sie in der Struktur der **Gruppenrichtlinien-Verwaltungskonsole** in der Gesamtstruktur und Domäne, in der Sie GPOs verwalten möchten, auf **Steuerelement ändern** .

2.  Klicken Sie im Detailbereich auf der Registerkarte **Inhalt** auf die Registerkarte **gesteuert** , um gesteuerte GPOs anzuzeigen, und klicken Sie dann auf das zu delegierende Gruppenrichtlinienobjekt.

3.  Klicken Sie auf die Schaltfläche **Hinzufügen** , wählen Sie die Benutzer oder Gruppen aus, denen Sie Zugriff gewähren möchten, und klicken Sie dann auf **OK**.

4.  Um die Berechtigungen für die einzelnen Benutzer anzupassen, klicken Sie auf der Registerkarte **Inhalt** auf die Schaltfläche **erweitert** , und überprüfen Sie die Rollen Berechtigungen auf zulassen oder ablehnen. (Wenn Sie eine genauere Steuerung haben, klicken Sie im Dialogfeld **Berechtigungen** auf **erweitert** .)

5.  Klicken Sie auf über **nehmen**, und klicken Sie dann im Dialogfeld **Berechtigungen** auf **OK** .

### Weitere Überlegungen

-   Standardmäßig müssen Sie die genehmigende Person sein, die das Gruppenrichtlinienobjekt erstellt oder kontrolliert hat, oder einen AGPM-Administrator (Vollzugriff), um dieses Verfahren ausführen zu können. Insbesondere müssen Sie über die Berechtigung **Listeninhalt** für die Domäne und die Berechtigung zum **Ändern der Sicherheit** für das Gruppenrichtlinienobjekt verfügen.

### Weitere Verweise

-   [Erstellen, Steuern oder Importieren eines Gruppenrichtlinienobjekts](creating-controlling-or-importing-a-gpo-approver.md)

 

 





