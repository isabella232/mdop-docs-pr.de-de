---
title: Bereitstellen eines Gruppenrichtlinienobjekts
description: Bereitstellen eines Gruppenrichtlinienobjekts
author: dansimp
ms.assetid: a6febeaa-144b-4c02-99af-d972f0f2b544
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 208fd95ec48f81b6c3a2a59bf92f53128eb3d529
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807612"
---
# Bereitstellen eines Gruppenrichtlinienobjekts


Eine genehmigende Person kann ein neues oder bearbeitetes Gruppenrichtlinienobjekt (GPO) in der Produktionsumgebung bereitstellen. Informationen zum erneuten Bereitstelleneiner früheren Version eines GPO finden Sie unter [Zurücksetzen auf eine frühere Version eines Gruppenrichtlinienobjekts](roll-back-to-an-earlier-version-of-a-gpo-agpm40.md).

Zum Ausführen dieses Verfahrens ist ein Benutzerkonto mit der Rolle Genehmiger oder AGPM-Administrator (Vollzugriff) oder den erforderlichen Berechtigungen in der erweiterten Gruppenrichtlinienverwaltung (Group Policy Management, AGPM) erforderlich. Lesen Sie die Details unter "Weitere Überlegungen" in diesem Thema.

**So stellen Sie ein GPO in der Produktionsumgebung bereit**

1.  Klicken Sie in der Struktur der **Gruppenrichtlinien-Verwaltungskonsole** in der Gesamtstruktur und Domäne, in der Sie GPOs verwalten möchten, auf **Steuerelement ändern** .

2.  Klicken Sie auf der Registerkarte **Inhalt** auf die Registerkarte **gesteuert** , um die gesteuerten GPOs anzuzeigen.

3.  Klicken Sie mit der rechten Maustaste auf das zu implementierende GPO, und klicken Sie dann auf **Bereitstellen**.

4.  Klicken Sie auf **erweitert**, um Links zu dem Gruppenrichtlinienobjekt zu überprüfen. Zeigen Sie mit dem Mauszeiger auf ein Element in der Struktur, um Details anzuzeigen.

    -   Standardmäßig werden alle Verknüpfungen mit dem Gruppenrichtlinienobjekt wiederhergestellt.

    -   Um zu verhindern, dass eine Verknüpfung wiederhergestellt wird, deaktivieren Sie das Kontrollkästchen für diesen Link.

    -   Um zu verhindern, dass alle Verknüpfungen wiederhergestellt werden, deaktivieren Sie das Kontrollkästchen **Verknüpfungen wiederherstellen** im Dialogfeld **Gruppenrichtlinienobjekt bereitstellen** .

5.  Klicken Sie auf **Ja**. Wenn das **Status** Fenster angibt, dass der Gesamtfortschritt abgeschlossen ist, klicken Sie auf **Schließen**.

**Hinweis**  Um zu überprüfen, ob die neueste Version eines GPO bereitgestellt wurde, doppelklicken Sie auf der Registerkarte **gesteuert** auf das Gruppenrichtlinienobjekt, um dessen **Verlauf**anzuzeigen. Im **Protokoll** für das Gruppenrichtlinienobjekt gibt die Spalte **Status** an, ob ein GPO bereitgestellt wurde.

 

### Weitere Überlegungen

-   Standardmäßig müssen Sie eine genehmigende Person oder ein AGPM-Administrator (Vollzugriff) sein, um dieses Verfahren ausführen zu können. Insbesondere müssen Sie über **Listeninhalte** und Berechtigungen zum **Bereitstellen von Gruppenrichtlinienobjekten** für das Gruppenrichtlinienobjekt verfügen.

### Weitere Verweise

-   [Durchführen der Aufgaben von genehmigenden Personen](performing-approver-tasks-agpm40.md)

 

 





