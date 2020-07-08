---
title: Zurücksetzen auf eine frühere Version eines Gruppenrichtlinienobjekts
description: Zurücksetzen auf eine frühere Version eines Gruppenrichtlinienobjekts
author: dansimp
ms.assetid: 028631c0-4cb9-4642-90ad-04cd813051b7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a71740eaa60a4b1292e47ca8aa57d4657231ab57
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808244"
---
# Zurücksetzen auf eine frühere Version eines Gruppenrichtlinienobjekts


Mit der erweiterten Gruppenrichtlinienverwaltung (AGPM) kann eine genehmigende Person Änderungen an einem Gruppenrichtlinienobjekt zurücksetzen, indem Sie eine frühere Version des GPO aus ihrem Verlauf erneut bereitstellen. Durch das Bereitstelleneiner früheren Version eines GPO wird die Version des Gruppenrichtlinienobjekts überschrieben, das sich derzeit in der Produktion befindet.

Zum Ausführen dieses Verfahrens ist ein Benutzerkonto mit der Rolle Genehmiger oder AGPM-Administrator (Vollzugriff) oder den erforderlichen Berechtigungen in der erweiterten Gruppenrichtlinienverwaltung erforderlich. Lesen Sie die Details unter "Weitere Überlegungen" in diesem Thema.

**So stellen Sie eine frühere Version eines GPO in der Produktionsumgebung bereit**

1.  Klicken Sie in der Struktur der **Gruppenrichtlinien-Verwaltungskonsole** in der Gesamtstruktur und Domäne, in der Sie GPOs verwalten möchten, auf **Steuerelement ändern** .

2.  Klicken Sie auf der Registerkarte **Inhalt** auf die Registerkarte **gesteuert** , um die gesteuerten GPOs anzuzeigen.

3.  Doppelklicken Sie auf das Gruppenrichtlinienobjekt, das bereitgestellt werden soll, um dessen **Verlauf**anzuzeigen.

4.  Klicken Sie mit der rechten Maustaste auf die bereit **zustellende**Version, klicken Sie auf bereitstellen, und klicken Sie dann auf **Ja**.

5.  Wenn das **Status** Fenster angibt, dass der Gesamtfortschritt abgeschlossen ist, klicken Sie auf **Schließen**. Klicken Sie im Fenster **Verlauf** auf **Schließen**.

**Hinweis**  Um zu überprüfen, ob die Version, die erneut bereitgestellt wurde, mit der beabsichtigten Version übereinstimmt, untersuchen Sie einen Unterschiedsbericht für die beiden Versionen. Markieren Sie im **Verlaufs** Fenster für das Gruppenrichtlinienobjekt die beiden Versionen, und klicken Sie dann mit der rechten Maustaste, und wählen Sie **Differenz** und entweder **HTML-Bericht** oder **XML-Bericht**aus.

 

### Weitere Überlegungen

-   Standardmäßig müssen Sie eine genehmigende Person oder ein AGPM-Administrator (Vollzugriff) sein, um dieses Verfahren ausführen zu können. Insbesondere müssen Sie über **Listeninhalte** und Berechtigungen zum **Bereitstellen von Gruppenrichtlinienobjekten** für das Gruppenrichtlinienobjekt verfügen.

### Weitere Verweise

-   [Durchführen der Aufgaben von genehmigenden Personen](performing-approver-tasks.md)

 

 





