---
title: Löschen eines Gruppenrichtlinienobjekts
description: Löschen eines Gruppenrichtlinienobjekts
author: dansimp
ms.assetid: 66be3dde-653e-4c25-8cb7-00e7090c8d31
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6c27ddf87a12ed6010c481d93bfc85bb531f3d4f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808520"
---
# Löschen eines Gruppenrichtlinienobjekts


Als Editor verfügen Sie möglicherweise nicht über die Berechtigung zum Durchführen des Löschens eines Gruppenrichtlinienobjekts (GPO), aber Sie verfügen über die erforderliche Berechtigung, um mit dem Vorgang zu beginnen und Ihre Anforderung an eine genehmigende Person zu übermitteln.

Zum Ausführen dieses Verfahrens ist ein Benutzerkonto mit der Rolle "Editor" oder den erforderlichen Berechtigungen in der erweiterten Gruppenrichtlinienverwaltung erforderlich. Lesen Sie die Details unter "Weitere Überlegungen" in diesem Thema.

**So fordern Sie das Löschen eines kontrollierten Gruppenrichtlinienobjekts an**

1.  Klicken Sie in der Struktur der **Gruppenrichtlinien-Verwaltungskonsole** in der Gesamtstruktur und Domäne, in der Sie GPOs verwalten möchten, auf **Steuerelement ändern** .

2.  Klicken Sie auf der Registerkarte **Inhalt** auf die Registerkarte **gesteuert** , um die gesteuerten GPOs anzuzeigen.

3.  Klicken Sie mit der rechten Maustaste auf das zu löschende GPO, und klicken Sie dann auf **Löschen**.

    -   Wenn Sie das Gruppenrichtlinienobjekt aus dem Archiv löschen möchten, während die bereitgestellte Version des Gruppenrichtlinienobjekts in der Produktionsumgebung unangetastet bleibt, klicken Sie auf **GPO nur aus Archiv löschen (uncontrol)**.

    -   Wenn Sie das Gruppenrichtlinienobjekt aus der Archivierungs-und Produktionsumgebung löschen möchten, klicken Sie auf **Gruppenrichtlinienobjekt aus Archiv und Produktion löschen**.

        Sofern Sie keine besondere Berechtigung zum Löschen von GPOs haben, müssen Sie eine Anforderung zum Löschen des bereitgestellten Gruppenrichtlinienobjekts übermitteln. Wenn Sie eine Kopie der Anfrage erhalten möchten, geben Sie Ihre e-Mail-Adresse in das Feld **CC** ein. Geben Sie einen Kommentar ein, der im Überwachungspfad für das Gruppenrichtlinienobjekt angezeigt werden soll, und klicken Sie dann auf **Absenden**.

4.  Wenn das **Status** Fenster angibt, dass der Gesamtfortschritt abgeschlossen ist, klicken Sie auf **Schließen**. Das Gruppenrichtlinienobjekt wird in der Liste der GPOs auf der Registerkarte **Ausstehend** angezeigt. Wenn eine genehmigende Person Ihre Anfrage genehmigt hat, wird das Gruppenrichtlinienobjekt von der Registerkarte " **Ausstehend** " auf die Registerkarte " **Papierkorb** " verschoben, wo Sie wiederhergestellt oder gelöscht werden kann.

### Weitere Überlegungen

-   Standardmäßig müssen Sie ein Editor sein, um das Löschen eines bereitgestellten Gruppenrichtlinienobjekts anzufordern. Insbesondere müssen Sie über **Listeninhalte** und Berechtigungen zum **Bearbeiten von Einstellungen** für das Gruppenrichtlinienobjekt verfügen.

-   Standardmäßig müssen Sie ein Editor, eine genehmigende Person oder ein AGPM-Administrator (Vollzugriff) sein, um ein GPO aus dem Archiv zu löschen. Insbesondere müssen Sie über **Listeninhalte** und entweder die Berechtigung " **Einstellungen bearbeiten** " oder " **GPO löschen** " für das Gruppenrichtlinienobjekt verfügen.

-   Wenn Sie Ihre Anfrage zurücknehmen möchten, bevor Sie genehmigt wurde, klicken Sie auf die Registerkarte **Ausstehend** . Klicken Sie mit der rechten Maustaste auf das GPO, und klicken Sie dann auf **zurück** Das Gruppenrichtlinienobjekt wird auf die Registerkarte **gesteuert** zurückgegeben.

-   Klicken Sie in der **Gruppenrichtlinien-Verwaltungskonsole**auf **Gesamtstruktur**, klicken Sie auf **Domänen**, klicken Sie auf meine ** &lt; &gt; Domäne**, und klicken Sie dann auf **Gruppenrichtlinienobjekte**, um ein ungesteuertes Gruppenrichtlinienobjekt aus der Produktionsumgebung zu löschen, ohne es zuvor zu kontrollieren. Klicken Sie mit der rechten Maustaste auf das unkontrollierte Gruppenrichtlinienobjekt, und klicken Sie dann auf **Löschen**.

### Weitere Verweise

-   [Durchführen von Editor-Aufgaben](performing-editor-tasks.md)

 

 





