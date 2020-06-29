---
title: Wiederherstellen eines gelöschten Gruppenrichtlinienobjekts
description: Wiederherstellen eines gelöschten Gruppenrichtlinienobjekts
author: dansimp
ms.assetid: 0a131d26-a741-4a51-b612-c0bc7dbba06b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 14fdf2f74f2d3db4be0db1aab7c185f5c1ab2cd1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807500"
---
# Wiederherstellen eines gelöschten Gruppenrichtlinienobjekts


Genehmigende Personen können ein gelöschtes Gruppenrichtlinienobjekt (GPO) aus dem Papierkorb wiederherstellen und an das Archiv zurückgeben.

Zum Ausführen dieses Verfahrens ist ein Benutzerkonto mit der Rolle Genehmiger oder AGPM-Administrator (Vollzugriff) oder den erforderlichen Berechtigungen in der erweiterten Gruppenrichtlinienverwaltung (Group Policy Management, AGPM) erforderlich. Lesen Sie die Details unter "Weitere Überlegungen" in diesem Thema.

**So stellen Sie ein gelöschtes Gruppenrichtlinienobjekt wieder her**

1.  Klicken Sie in der Struktur der **Gruppenrichtlinien-Verwaltungskonsole** in der Gesamtstruktur und Domäne, in der Sie GPOs verwalten möchten, auf **Steuerelement ändern** .

2.  Klicken Sie auf der Registerkarte **Inhalt** auf die Registerkarte **Papierkorb** , um die gelöschten GPOs anzuzeigen.

3.  Klicken Sie mit der rechten Maustaste auf das wiederherzustellende GPO, und klicken Sie dann auf **Wiederherstellen**.

4.  Geben Sie einen Kommentar ein, der im Verlauf des Gruppenrichtlinienobjekts angezeigt werden soll, und klicken Sie dann auf **OK**.

5.  Wenn das **Status** Fenster angibt, dass der Gesamtfortschritt abgeschlossen ist, klicken Sie auf **Schließen**. Das Gruppenrichtlinienobjekt wird von der Registerkarte " **Papierkorb** " entfernt und auf der Registerkarte " **gesteuert** " angezeigt.

**Hinweis**  Wenn ein GPO aus der Produktionsumgebung gelöscht wurde, wird es nicht automatisch in der Produktionsumgebung erneut bereitgestellt. Wenn Sie das Gruppenrichtlinienobjekt an die Produktionsumgebung zurückgeben möchten, stellen Sie das Gruppenrichtlinienobjekt bereit. Informationen finden Sie unter [Bereitstellen eines Gruppenrichtlinienobjekts](deploy-a-gpo-agpm40.md).

 

### Weitere Überlegungen

-   Standardmäßig müssen Sie eine genehmigende Person oder ein AGPM-Administrator (Vollzugriff) sein, um dieses Verfahren ausführen zu können. Insbesondere müssen Sie über **Listeninhalte** verfügen und entweder **Gruppenrichtlinienobjekte bereitstellen** oder GPO-Berechtigungen **Löschen** .

### Weitere Verweise

-   [Löschen, Wiederherstellen oder Zerstören eines Gruppenrichtlinienobjekts](deleting-restoring-or-destroying-a-gpo-agpm40.md)

 

 





