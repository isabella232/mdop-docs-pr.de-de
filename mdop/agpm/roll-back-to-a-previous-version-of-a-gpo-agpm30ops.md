---
title: Zurücksetzen auf eine frühere Version eines Gruppenrichtlinienobjekts
description: Zurücksetzen auf eine frühere Version eines Gruppenrichtlinienobjekts
author: dansimp
ms.assetid: 2a98ad8f-32cb-41eb-ab99-0318f2a55d81
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 715f70ad6e87a0b2fa463426d4f6a8955250e446
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808247"
---
# Zurücksetzen auf eine frühere Version eines Gruppenrichtlinienobjekts


Eine genehmigende Person kann Änderungen an einem Gruppenrichtlinienobjekt (GPO) zurücksetzen, indem Sie eine frühere Version des Gruppenrichtlinienobjekts aus ihrem Verlauf erneut bereitstellt. Durch das Bereitstelleneiner früheren Version eines GPO wird die Version des Gruppenrichtlinienobjekts überschrieben, das sich derzeit in der Produktion befindet.

Zum Ausführen dieses Verfahrens ist ein Benutzerkonto mit der Rolle Genehmiger oder AGPM-Administrator (Vollzugriff) oder den erforderlichen Berechtigungen in der erweiterten Gruppenrichtlinienverwaltung (Group Policy Management, AGPM) erforderlich. Lesen Sie die Details unter "Weitere Überlegungen" in diesem Thema.

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

-   [Durchführen der Aufgaben von genehmigenden Personen](performing-approver-tasks-agpm30ops.md)

 

 





