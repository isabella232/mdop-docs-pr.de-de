---
title: Anfordern der Erstellung eines neuen gesteuerten Gruppenrichtlinienobjekts
description: Anfordern der Erstellung eines neuen gesteuerten Gruppenrichtlinienobjekts
author: dansimp
ms.assetid: 4194c2f3-8116-4a35-be1a-81c84072daec
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4f9d7dd8a604bf2d2e3638142c070fed8b6d44e2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808263"
---
# Anfordern der Erstellung eines neuen gesteuerten Gruppenrichtlinienobjekts


Sofern Sie kein Genehmiger oder ein AGPM-Administrator (Vollzugriff) sind, müssen Sie die Erstellung eines neuen Gruppenrichtlinienobjekts (GPO) anfordern.

Um dieses Verfahren ausführen zu können, ist ein Benutzerkonto mit der Rolle "Bearbeiter" oder "Prüfer" oder die erforderlichen Berechtigungen in Advanced Group Policy Management (AGPM) erforderlich. Lesen Sie die Details unter "Weitere Überlegungen" in diesem Thema.

**So erstellen Sie ein neues Gruppenrichtlinienobjekt mit über AGPM verwaltetem Änderungs Steuerelement**

1.  Klicken Sie in der Struktur der **Gruppenrichtlinien-Verwaltungskonsole** in der Gesamtstruktur und Domäne, in der Sie GPOs verwalten möchten, auf **Steuerelement ändern** .

2.  Klicken Sie mit der rechten Maustaste auf **Change Control**, und klicken Sie dann auf **Neues gesteuertes Gruppenrichtlinienobjekt**.

3.  Sofern Sie keine besondere Berechtigung zum Erstellen von GPOs haben, müssen Sie eine Anforderung zur Erstellung einreichen. Im Dialogfeld " **Neues gesteuertes GPO** ":

    1.  Wenn Sie eine Kopie der Anfrage erhalten möchten, geben Sie Ihre e-Mail-Adresse in das Feld **CC** ein.

    2.  Geben Sie einen Namen für das neue Gruppenrichtlinienobjekt ein.

    3.  Optional: Geben Sie einen Kommentar für das neue Gruppenrichtlinienobjekt ein.

    4.  Wenn Sie das neue Gruppenrichtlinienobjekt unmittelbar nach der Genehmigung in der Produktionsumgebung bereitstellen möchten, klicken Sie auf **Live erstellen**. Wenn Sie das neue Gruppenrichtlinienobjekt offline erstellen möchten, ohne es sofort nach der Genehmigung bereitzustellen, klicken Sie auf **Offline erstellen**.

    5.  Wählen Sie die GPO-Vorlage aus, die als Ausgangspunkt für das neue Gruppenrichtlinienobjekt verwendet werden soll.

    6.  Klicken Sie auf **Übermitteln**.

4.  Wenn das **Status** Fenster angibt, dass der Gesamtfortschritt abgeschlossen ist, klicken Sie auf **Schließen**. Das neue Gruppenrichtlinienobjekt wird in der Liste der GPOs auf der Registerkarte **Ausstehend** angezeigt. Wenn eine genehmigende Person Ihre Anfrage genehmigt hat, wird das Gruppenrichtlinienobjekt auf die Registerkarte **gesteuert** verschoben.

### Weitere Überlegungen

-   Standardmäßig müssen Sie ein Editor oder ein Bearbeiter sein, um dieses Verfahren ausführen zu können. Insbesondere müssen Sie über die Berechtigung **Listeninhalte** für die Domäne verfügen.

-   Wenn Sie Ihre Anfrage zurücknehmen möchten, bevor Sie genehmigt wurde, klicken Sie auf die Registerkarte **Ausstehend** . Klicken Sie mit der rechten Maustaste auf das Gruppenrichtlinienobjekt und dann auf **zurück** Das Gruppenrichtlinienobjekt wird gelöscht.

### Weitere Verweise

-   [Erstellen, Steuern oder Importieren eines Gruppenrichtlinienobjekts](creating-controlling-or-importing-a-gpo-agpm30ops.md)

 

 





