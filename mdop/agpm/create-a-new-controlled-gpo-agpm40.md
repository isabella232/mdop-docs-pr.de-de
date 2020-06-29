---
title: Erstellen eines neuen gesteuerten Gruppenrichtlinienobjekts
description: Erstellen eines neuen gesteuerten Gruppenrichtlinienobjekts
author: dansimp
ms.assetid: 5ce760f6-9f05-42b4-b787-7835ab8e324e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 67c6af686b9ba7254cdaf93bd2d294b2d5bbb681
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808571"
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

    3.  Wenn Sie das neue Gruppenrichtlinienobjekt sofort in der Produktionsumgebung der Domäne bereitstellen möchten, klicken Sie auf **Live erstellen**. Wenn Sie das neue Gruppenrichtlinienobjekt offline erstellen möchten, ohne es sofort bereitzustellen, klicken Sie auf **Offline erstellen**.

    4.  Wählen Sie die GPO-Vorlage aus, die als Ausgangspunkt für das neue Gruppenrichtlinienobjekt verwendet werden soll, und klicken Sie dann auf **OK**.

4.  Wenn das **Status** Fenster angibt, dass der Gesamtfortschritt abgeschlossen ist, klicken Sie auf **Schließen**. Das neue Gruppenrichtlinienobjekt wird in der Liste der GPOs auf der Registerkarte **gesteuert** angezeigt.

### Weitere Überlegungen

-   Standardmäßig müssen Sie eine genehmigende Person oder ein AGPM-Administrator (Vollzugriff) sein, um dieses Verfahren ausführen zu können. Insbesondere müssen Sie über **Listeninhalte** und Berechtigungen zum **Erstellen von Gruppenrichtlinienobjekten** für die Domäne verfügen.

### Weitere Verweise

-   [Erstellen oder Steuern eines Gruppenrichtlinienobjekts](creating-or-controlling-a-gpo-agpm40-app.md)

 

 





