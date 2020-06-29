---
title: Anfordern der Löschung eines Gruppenrichtlinienobjekts
description: Anfordern der Löschung eines Gruppenrichtlinienobjekts
author: dansimp
ms.assetid: 576ece5c-dc6d-4b5e-8628-01c15ae2c9a8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 87368d9f132d1ef7dc6a70fffa0611d33a23aa78
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807508"
---
# Anfordern der Löschung eines Gruppenrichtlinienobjekts


Sofern Sie kein Genehmiger oder ein AGPM-Administrator (Vollzugriff) sind, müssen Sie den Löschvorgang für ein Gruppenrichtlinienobjekt (GPO) anfordern.

Um dieses Verfahren ausführen zu können, ist ein Benutzerkonto mit der Rolle "Editor" oder den erforderlichen Berechtigungen in Advanced Group Policy Management (AGPM) erforderlich. Lesen Sie die Details unter "Weitere Überlegungen" in diesem Thema.

**So fordern Sie das Löschen eines kontrollierten Gruppenrichtlinienobjekts an**

1.  Klicken Sie in der Struktur der **Gruppenrichtlinien-Verwaltungskonsole** in der Gesamtstruktur und Domäne, in der Sie GPOs verwalten möchten, auf **Steuerelement ändern** .

2.  Klicken Sie auf der Registerkarte **Inhalt** auf die Registerkarte **gesteuert** , um die gesteuerten GPOs anzuzeigen.

3.  Klicken Sie mit der rechten Maustaste auf das Gruppenrichtlinienobjekt, das Sie löschen möchten, und klicken Sie dann auf **Löschen**.

    -   Wenn Sie das Gruppenrichtlinienobjekt aus dem Archiv löschen möchten, während die bereitgestellte Version des Gruppenrichtlinienobjekts in der Produktionsumgebung unangetastet bleibt, klicken Sie auf **GPO nur aus Archiv löschen**.

    -   Wenn Sie das Gruppenrichtlinienobjekt aus der Archivierungs-und Produktionsumgebung löschen möchten, klicken Sie auf **Gruppenrichtlinienobjekt aus Archiv und Produktion löschen**.

4.  Sofern Sie keine besondere Berechtigung zum Löschen von GPOs haben, müssen Sie eine Anforderung zum Löschen des bereitgestellten Gruppenrichtlinienobjekts übermitteln. Wenn Sie eine Kopie der Anfrage erhalten möchten, geben Sie Ihre e-Mail-Adresse in das Feld **CC** ein. Geben Sie einen Kommentar ein, der im Überwachungspfad für das Gruppenrichtlinienobjekt angezeigt werden soll, und klicken Sie dann auf **Absenden**.

5.  Wenn das **Status** Fenster angibt, dass der Gesamtfortschritt abgeschlossen ist, klicken Sie auf **Schließen**. Das Gruppenrichtlinienobjekt wird in der Liste der GPOs auf der Registerkarte **Ausstehend** angezeigt. Wenn eine genehmigende Person Ihre Anfrage genehmigt hat, wird das Gruppenrichtlinienobjekt von der Registerkarte " **Ausstehend** " auf die Registerkarte " **Papierkorb** " verschoben, wo Sie wiederhergestellt oder gelöscht werden kann.

### Weitere Überlegungen

-   Standardmäßig müssen Sie ein Editor sein, um dieses Verfahren ausführen zu können. Insbesondere müssen Sie über **Listeninhalte** und Berechtigungen zum **Bearbeiten von Einstellungen** für das Gruppenrichtlinienobjekt verfügen.

-   Wenn Sie Ihre Anfrage zurücknehmen möchten, bevor Sie genehmigt wurde, klicken Sie auf die Registerkarte **Ausstehend** . Klicken Sie mit der rechten Maustaste auf das GPO, und klicken Sie dann auf **zurück** Das Gruppenrichtlinienobjekt wird auf die Registerkarte **gesteuert** zurückgegeben.

-   Klicken Sie in der **Gruppenrichtlinien-Verwaltungskonsole**auf **Gesamtstruktur**, klicken Sie auf **Domänen**, klicken Sie auf meine ** &lt; &gt; Domäne**, und klicken Sie dann auf **Gruppenrichtlinienobjekte**, um ein ungesteuertes Gruppenrichtlinienobjekt aus der Produktionsumgebung zu löschen, ohne es zuvor zu kontrollieren. Klicken Sie mit der rechten Maustaste auf das unkontrollierte Gruppenrichtlinienobjekt, und klicken Sie dann auf **Löschen**.

### Weitere Verweise

-   [Durchführen von Editor-Aufgaben](performing-editor-tasks-agpm30ops.md)

 

 





