---
title: Steuern eines zuvor nicht gesteuerten Gruppenrichtlinienobjekts
description: Steuern eines zuvor nicht gesteuerten Gruppenrichtlinienobjekts
author: dansimp
ms.assetid: 452689a9-4e32-4e3b-8208-56353a82bf36
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9d7349b16b326a49b701efae5379c313bde0964f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807687"
---
# Steuern eines zuvor nicht gesteuerten Gruppenrichtlinienobjekts


Wenn Sie die erweiterte Gruppenrichtlinienverwaltung (Group Policy Management, AGPM) verwenden möchten, um das Änderungs Steuerelement für ein Gruppenrichtlinienobjekt (GPO) bereitzustellen, müssen Sie zuerst das Gruppenrichtlinienobjekt mit AGPM steuern.

Zum Ausführen dieses Verfahrens ist ein Benutzerkonto mit der Rolle Genehmiger oder AGPM-Administrator (Vollzugriff) oder den erforderlichen Berechtigungen in der erweiterten Gruppenrichtlinienverwaltung erforderlich. Lesen Sie die Details unter "Weitere Überlegungen" in diesem Thema.

**So steuern Sie ein zuvor unkontrolliertes Gruppenrichtlinienobjekt**

1.  Klicken Sie in der Struktur der **Gruppenrichtlinien-Verwaltungskonsole** in der Gesamtstruktur und Domäne, in der Sie GPOs verwalten möchten, auf **Steuerelement ändern** .

2.  Klicken Sie im Detailbereich auf der Registerkarte **Inhalt** auf die Registerkarte **unkontrolliert** , um die nicht kontrollierten GPOs anzuzeigen.

3.  Klicken Sie mit der rechten Maustaste auf das Gruppenrichtlinienobjekt, das mit AGPM gesteuert werden soll, und klicken Sie dann auf **Steuerelement**.

4.  Geben Sie einen Kommentar ein, der im Verlauf des Gruppenrichtlinienobjekts angezeigt werden soll, und klicken Sie dann auf **OK**.

5.  Wenn das **Status** Fenster angibt, dass der Gesamtfortschritt abgeschlossen ist, klicken Sie auf **Schließen**. Das Gruppenrichtlinienobjekt wird auf der Registerkarte **unkontrolliert** aus der Liste entfernt und der Registerkarte **gesteuert** hinzugefügt.

### Weitere Überlegungen

-   Standardmäßig müssen Sie eine genehmigende Person oder ein AGPM-Administrator (Vollzugriff) sein, um dieses Verfahren ausführen zu können. Insbesondere müssen Sie über **Listeninhalte** und Berechtigungen zum **Erstellen von Gruppenrichtlinienobjekten** für die Domäne verfügen.

### Weitere Verweise

-   [Erstellen, Steuern oder Importieren eines Gruppenrichtlinienobjekts](creating-controlling-or-importing-a-gpo-approver.md)

 

 





