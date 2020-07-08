---
title: Anfordern der Wiederherstellung eines gelöschten Gruppenrichtlinienobjekts
description: Anfordern der Wiederherstellung eines gelöschten Gruppenrichtlinienobjekts
author: dansimp
ms.assetid: bac5ca3b-be47-49b5-bf1b-96280625fda8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 606690554ca1f813e1c20787bca59cfe2de6432d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808280"
---
# Anfordern der Wiederherstellung eines gelöschten Gruppenrichtlinienobjekts


Sofern Sie kein Genehmiger oder ein AGPM-Administrator (Vollzugriff) sind, müssen Sie die Wiederherstellung eines gelöschten Gruppenrichtlinienobjekts aus dem Papierkorb anfordern, um es in das Archiv zurückzugeben.

Um dieses Verfahren ausführen zu können, ist ein Benutzerkonto mit der Rolle "Editor" oder den erforderlichen Berechtigungen in Advanced Group Policy Management (AGPM) erforderlich. Lesen Sie die Details unter "Weitere Überlegungen" in diesem Thema.

**So fordern Sie die Wiederherstellung eines gelöschten Gruppenrichtlinienobjekts an**

1.  Klicken Sie in der Struktur der **Gruppenrichtlinien-Verwaltungskonsole** in der Gesamtstruktur und Domäne, in der Sie GPOs verwalten möchten, auf **Steuerelement ändern** .

2.  Klicken Sie auf der Registerkarte **Inhalt** auf die Registerkarte **Papierkorb** , um die gelöschten GPOs anzuzeigen.

3.  Klicken Sie mit der rechten Maustaste auf das GPO, das Sie wiederherstellen möchten, und klicken Sie dann auf **Wiederherstellen**.

4.  Sofern Sie keine besondere Berechtigung zum Wiederherstellen von GPOs haben, müssen Sie eine Anforderung zur Wiederherstellung des gelöschten Gruppenrichtlinienobjekts übermitteln. Wenn Sie eine Kopie der Anfrage erhalten möchten, geben Sie Ihre e-Mail-Adresse in das Feld **CC** ein. Geben Sie einen Kommentar ein, der im Überwachungspfad für das Gruppenrichtlinienobjekt angezeigt werden soll, und klicken Sie dann auf **Absenden**.

5.  Wenn das **Status** Fenster angibt, dass der Gesamtfortschritt abgeschlossen ist, klicken Sie auf **Schließen**. Das Gruppenrichtlinienobjekt wird von der Registerkarte " **Papierkorb** " entfernt und auf der Registerkarte " **gesteuert** " angezeigt.

**Hinweis**  Wenn ein GPO aus der Produktionsumgebung gelöscht wurde, wird es nicht automatisch in der Produktionsumgebung erneut bereitgestellt. Wenn Sie das Gruppenrichtlinienobjekt an die Produktionsumgebung zurückgeben möchten, stellen Sie das Gruppenrichtlinienobjekt bereit. Informationen hierzu finden Sie unter [anfordern der Bereitstellungeines Gruppenrichtlinienobjekts](request-deployment-of-a-gpo-agpm40.md).

 

### Weitere Überlegungen

-   Standardmäßig müssen Sie ein Editor sein, um dieses Verfahren ausführen zu können. Insbesondere müssen Sie über die Berechtigung " **Listeninhalt** " und " **Einstellungen bearbeiten** " für das Gruppenrichtlinienobjekt verfügen.

-   Wenn Sie Ihre Anfrage zurücknehmen möchten, bevor Sie genehmigt wurde, klicken Sie auf die Registerkarte **Ausstehend** . Klicken Sie mit der rechten Maustaste auf das GPO, und klicken Sie dann auf **zurück** Das Gruppenrichtlinienobjekt wird auf die Registerkarte **Papierkorb** zurückgegeben.

### Weitere Verweise

-   [Löschen oder Wiederherstellen eines Gruppenrichtlinienobjekts](deleting-or-restoring-a-gpo-agpm40.md)

 

 





