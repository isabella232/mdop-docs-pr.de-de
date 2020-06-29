---
title: Steuern eines nicht gesteuerten Gruppenrichtlinienobjekts
description: Steuern eines nicht gesteuerten Gruppenrichtlinienobjekts
author: dansimp
ms.assetid: dc81545c-8da5-4b6f-b266-f01a82e27c6b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 418e2a4100e1d824198b7d05034443948ec8a44c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807692"
---
# Steuern eines nicht gesteuerten Gruppenrichtlinienobjekts


Wenn Sie das Änderungs Steuerelement für ein Gruppenrichtlinienobjekt (GPO) bereitstellen möchten, müssen Sie zuerst das Gruppenrichtlinienobjekt steuern.

Zum Ausführen dieses Verfahrens ist ein Benutzerkonto mit der Rolle Genehmiger oder AGPM-Administrator (Vollzugriff) oder den erforderlichen Berechtigungen in der erweiterten Gruppenrichtlinienverwaltung (Group Policy Management, AGPM) erforderlich. Lesen Sie die Details unter "Weitere Überlegungen" in diesem Thema.

**So steuern Sie ein nicht gesteuertes Gruppenrichtlinienobjekt**

1.  Klicken Sie in der Struktur der **Gruppenrichtlinien-Verwaltungskonsole** in der Gesamtstruktur und Domäne, in der Sie GPOs verwalten möchten, auf **Steuerelement ändern** .

2.  Klicken Sie im Detailbereich auf der Registerkarte **Inhalt** auf die Registerkarte **unkontrolliert** , um die nicht kontrollierten GPOs anzuzeigen.

3.  Klicken Sie mit der rechten Maustaste auf das Gruppenrichtlinienobjekt, das mit AGPM gesteuert werden soll, und klicken Sie dann auf **Steuerelement**.

4.  Geben Sie einen Kommentar ein, der im Verlauf des Gruppenrichtlinienobjekts angezeigt werden soll, und klicken Sie dann auf **OK**.

5.  Wenn das **Status** Fenster angibt, dass der Gesamtfortschritt abgeschlossen ist, klicken Sie auf **Schließen**. Das Gruppenrichtlinienobjekt wird auf der Registerkarte **unkontrolliert** aus der Liste entfernt und der Registerkarte **gesteuert** hinzugefügt.

### Weitere Überlegungen

-   Standardmäßig müssen Sie eine genehmigende Person oder ein AGPM-Administrator (Vollzugriff) sein, um dieses Verfahren ausführen zu können. Insbesondere müssen Sie über **Listeninhalte** und Berechtigungen zum **Erstellen von Gruppenrichtlinienobjekten** für die Domäne verfügen.

### Weitere Verweise

-   [Erstellen oder Steuern eines Gruppenrichtlinienobjekts](creating-or-controlling-a-gpo-agpm40-app.md)

 

 





