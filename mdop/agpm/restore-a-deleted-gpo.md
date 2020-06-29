---
title: Wiederherstellen eines gelöschten Gruppenrichtlinienobjekts
description: Wiederherstellen eines gelöschten Gruppenrichtlinienobjekts
author: dansimp
ms.assetid: e6953296-7b7d-4d1e-ad82-d4a23044cdd7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2cba097ecd651a91f828901d8115a7020d6da819
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807496"
---
# Wiederherstellen eines gelöschten Gruppenrichtlinienobjekts


Mit der erweiterten Gruppenrichtlinienverwaltung (AGPM) können genehmigende Personen ein gelöschtes Gruppenrichtlinienobjekt aus dem Papierkorb wiederherstellen und dann in das Archiv zurücksenden.

Zum Ausführen dieses Verfahrens ist ein Benutzerkonto mit der Rolle "Editor", "Genehmiger" oder "AGPM-Administrator" (Vollzugriff) oder den erforderlichen Berechtigungen in der erweiterten Gruppenrichtlinienverwaltung erforderlich. Lesen Sie die Details unter "Weitere Überlegungen" in diesem Thema.

**So stellen Sie ein gelöschtes Gruppenrichtlinienobjekt wieder her**

1.  Klicken Sie in der Struktur der **Gruppenrichtlinien-Verwaltungskonsole** in der Gesamtstruktur und Domäne, in der Sie GPOs verwalten möchten, auf **Steuerelement ändern** .

2.  Klicken Sie auf der Registerkarte **Inhalt** auf die Registerkarte **Papierkorb** , um die gelöschten GPOs anzuzeigen.

3.  Klicken Sie mit der rechten Maustaste auf das wiederherzustellende GPO, und klicken Sie dann auf **Wiederherstellen**.

4.  Geben Sie einen Kommentar ein, der im Verlauf des Gruppenrichtlinienobjekts angezeigt werden soll, und klicken Sie dann auf **OK**.

5.  Wenn das **Status** Fenster angibt, dass der Gesamtfortschritt abgeschlossen ist, klicken Sie auf **Schließen**. Das Gruppenrichtlinienobjekt wird von der Registerkarte " **Papierkorb** " entfernt und auf der Registerkarte " **gesteuert** " angezeigt.

**Hinweis**  Wenn ein GPO aus der Produktionsumgebung gelöscht wurde, wird es nicht automatisch in der Produktionsumgebung erneut bereitgestellt. Wenn Sie das Gruppenrichtlinienobjekt an die Produktionsumgebung zurückgeben möchten, stellen Sie das Gruppenrichtlinienobjekt bereit. Informationen finden Sie unter [Bereitstellen eines Gruppenrichtlinienobjekts](deploy-a-gpo.md).

 

### Weitere Überlegungen

-   Standardmäßig müssen Sie ein Editor, eine genehmigende Person oder ein AGPM-Administrator (Vollzugriff) sein, um dieses Verfahren ausführen zu können. Insbesondere müssen Sie über **Listeninhalte** und entweder **Einstellungen bearbeiten**, **Gruppenrichtlinienobjekt bereitstellen**oder Berechtigungen für **Gruppenrichtlinienobjekte löschen** für das Gruppenrichtlinienobjekt verfügen.

### Weitere Verweise

-   [Löschen, Wiederherstellen oder Zerstören eines Gruppenrichtlinienobjekts](deleting-restoring-or-destroying-a-gpo.md)

 

 





