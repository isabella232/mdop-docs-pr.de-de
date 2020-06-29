---
title: Löschen eines Gruppenrichtlinienobjekts
description: Löschen eines Gruppenrichtlinienobjekts
author: dansimp
ms.assetid: 85fca371-5707-49c1-aa51-813fc3a58dfc
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8a6419943604ee5a76d305228bb7418a8525bf33
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808524"
---
# Löschen eines Gruppenrichtlinienobjekts


Erweiterte Gruppenrichtlinienverwaltung (AGPM) ermöglicht Genehmigern, ein gesteuertes Gruppenrichtlinienobjekt (Group Policy Object, GPO) zu löschen und in den Papierkorb zu verschieben.

Zum Ausführen dieses Verfahrens ist ein Benutzerkonto mit der Rolle Genehmiger oder AGPM-Administrator (Vollzugriff) oder den erforderlichen Berechtigungen in der erweiterten Gruppenrichtlinienverwaltung erforderlich. Lesen Sie die Details unter "Weitere Überlegungen" in diesem Thema.

**So löschen Sie ein gesteuertes Gruppenrichtlinienobjekt**

1.  Klicken Sie in der Struktur der **Gruppenrichtlinien-Verwaltungskonsole** in der Gesamtstruktur und Domäne, in der Sie GPOs verwalten möchten, auf **Steuerelement ändern** .

2.  Klicken Sie auf der Registerkarte **Inhalt** auf die Registerkarte **gesteuert** , um die gesteuerten GPOs anzuzeigen.

3.  Klicken Sie mit der rechten Maustaste auf das zu löschende GPO, und klicken Sie dann auf **Löschen**.

    -   Wenn Sie das Gruppenrichtlinienobjekt aus dem Archiv löschen möchten, während die bereitgestellte Version des Gruppenrichtlinienobjekts in der Produktionsumgebung unangetastet bleibt, klicken Sie auf **GPO nur aus Archiv löschen (uncontrol)**.

    -   Wenn Sie das Gruppenrichtlinienobjekt aus der Archivierungs-und Produktionsumgebung löschen möchten, klicken Sie auf **Gruppenrichtlinienobjekt aus Archiv und Produktion löschen**.

4.  Geben Sie einen Kommentar ein, der im Überwachungspfad für das Gruppenrichtlinienobjekt angezeigt werden soll, und klicken Sie dann auf **OK**.

5.  Wenn das **Status** Fenster angibt, dass der Gesamtfortschritt abgeschlossen ist, klicken Sie auf **Schließen**. Das Gruppenrichtlinienobjekt wird von der Registerkarte " **gesteuert** " entfernt und auf der Registerkarte " **Papierkorb** " angezeigt, wo es wiederhergestellt oder gelöscht werden kann. Wenn das Gruppenrichtlinienobjekt nur aus dem Archiv gelöscht wurde, wird es auch auf der Registerkarte nicht **gesteuert** angezeigt.

### Weitere Überlegungen

-   Standardmäßig müssen Sie eine genehmigende Person oder ein AGPM-Administrator (Vollzugriff) sein, um ein bereitgestelltes GPO zu löschen. Insbesondere müssen Sie über **Listeninhalte** und Berechtigungen zum **Löschen von Gruppenrichtlinienobjekten** für das Gruppenrichtlinienobjekt verfügen.

-   Standardmäßig müssen Sie ein Editor, eine genehmigende Person oder ein AGPM-Administrator (Vollzugriff) sein, um ein GPO aus dem Archiv zu löschen. Insbesondere müssen Sie über **Listeninhalte** und entweder die Berechtigung " **Einstellungen bearbeiten** " oder " **GPO löschen** " für das Gruppenrichtlinienobjekt verfügen.

-   Klicken Sie in der **Gruppenrichtlinien-Verwaltungskonsole**auf **Gesamtstruktur**, klicken Sie auf **Domänen**, klicken Sie auf meine ** &lt; &gt; Domäne**, und klicken Sie dann auf **Gruppenrichtlinienobjekte**, um ein ungesteuertes Gruppenrichtlinienobjekt aus der Produktionsumgebung zu löschen, ohne es zuvor zu kontrollieren. Klicken Sie mit der rechten Maustaste auf das unkontrollierte Gruppenrichtlinienobjekt, und klicken Sie dann auf **Löschen**.

### Weitere Verweise

-   [Löschen, Wiederherstellen oder Zerstören eines Gruppenrichtlinienobjekts](deleting-restoring-or-destroying-a-gpo.md)

 

 





