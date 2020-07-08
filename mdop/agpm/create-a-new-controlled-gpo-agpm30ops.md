---
title: Erstellen eines neuen gesteuerten Gruppenrichtlinienobjekts
description: Erstellen eines neuen gesteuerten Gruppenrichtlinienobjekts
author: dansimp
ms.assetid: f89eaae8-7858-4222-ba3f-a93a9d7ea5a3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9d666edf97459a8499ee0f74155473c692d583ae
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808572"
---
# Erstellen eines neuen gesteuerten Gruppenrichtlinienobjekts


Neue Gruppenrichtlinienobjekte (Group Policy Objects, GPOs), die über den Ordner " **Änderungssteuerung** " erstellt wurden, werden automatisch gesteuert, sodass Sie Sie verwalten können.

Zum Ausführen dieses Verfahrens ist ein Benutzerkonto mit der Rolle Genehmiger oder AGPM-Administrator (Vollzugriff) oder den erforderlichen Berechtigungen in der erweiterten Gruppenrichtlinienverwaltung (Group Policy Management, AGPM) erforderlich. Lesen Sie die Details unter "Weitere Überlegungen" in diesem Thema.

**So erstellen Sie ein neues Gruppenrichtlinienobjekt mit über AGPM verwaltetem Änderungs Steuerelement**

1.  Klicken Sie in der Struktur der **Gruppenrichtlinien-Verwaltungskonsole** in der Gesamtstruktur und Domäne, in der Sie GPOs verwalten möchten, auf **Steuerelement ändern** .

2.  Klicken Sie mit der rechten Maustaste auf **Change Control**, und klicken Sie dann auf **Neues gesteuertes Gruppenrichtlinienobjekt**.

3.  Im Dialogfeld " **Neues gesteuertes GPO** ":

    1.  Geben Sie einen Namen für das neue Gruppenrichtlinienobjekt ein.

    2.  Optional: Geben Sie einen Kommentar für das neue Gruppenrichtlinienobjekt ein, das im **Protokoll** für das Gruppenrichtlinienobjekt angezeigt werden soll.

    3.  Wenn Sie das neue Gruppenrichtlinienobjekt sofort in der Produktionsumgebung bereitstellen möchten, klicken Sie auf **Live erstellen**. Wenn Sie das neue Gruppenrichtlinienobjekt offline erstellen möchten, ohne es sofort bereitzustellen, klicken Sie auf **Offline erstellen**.

    4.  Wählen Sie die GPO-Vorlage aus, die als Ausgangspunkt für das neue Gruppenrichtlinienobjekt verwendet werden soll.

    5.  Klicken Sie auf **OK**.

4.  Wenn das **Status** Fenster angibt, dass der Gesamtfortschritt abgeschlossen ist, klicken Sie auf **Schließen**. Das neue Gruppenrichtlinienobjekt wird in der Liste der GPOs auf der Registerkarte **gesteuert** angezeigt.

### Weitere Überlegungen

-   Standardmäßig müssen Sie eine genehmigende Person oder ein AGPM-Administrator (Vollzugriff) sein, um dieses Verfahren ausführen zu können. Insbesondere müssen Sie über **Listeninhalte** und Berechtigungen zum **Erstellen von Gruppenrichtlinienobjekten** für die Domäne verfügen.

### Weitere Verweise

-   [Erstellen, Steuern oder Importieren eines Gruppenrichtlinienobjekts](creating-controlling-or-importing-a-gpo-editor-agpm30ops.md)

 

 





