---
title: Einchecken eines Gruppenrichtlinienobjekts
description: Einchecken eines Gruppenrichtlinienobjekts
author: dansimp
ms.assetid: 437397db-c94b-4940-b1a4-05442619ebee
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8c37144cb7c2d150d46dd1172a37717743f76ee3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807807"
---
# Einchecken eines Gruppenrichtlinienobjekts


In der Regel sollten Editoren Gruppenrichtlinienobjekte (Group Policy Objects, GPOs) überprüfen, die Sie bearbeitet haben, wenn Ihre Änderungen abgeschlossen sind. (Ausführliche Informationen finden Sie unter [Bearbeiten eines GPO Offline](edit-a-gpo-offline-agpm30ops.md).) Wenn der Editor jedoch nicht zur Verfügung steht, kann eine genehmigende Person auch ein GPO einchecken.

Zum Ausführen dieses Verfahrens ist ein Benutzerkonto mit der Rolle "Editor", "Genehmiger" oder "AGPM-Administrator" (Vollzugriff) oder den erforderlichen Berechtigungen in der erweiterten Gruppenrichtlinienverwaltung (AGPM) erforderlich. Lesen Sie die Details unter "Weitere Überlegungen" in diesem Thema.

**So checken Sie ein Gruppenrichtlinienobjekt ein, das von einem Editor ausgecheckt wurde**

1.  Klicken Sie in der Struktur der **Gruppenrichtlinien-Verwaltungskonsole** in der Gesamtstruktur und Domäne, in der Sie GPOs verwalten möchten, auf **Steuerelement ändern** .

2.  Klicken Sie auf der Registerkarte **Inhalt** auf die Registerkarte **gesteuert** , um die gesteuerten GPOs anzuzeigen.

    -   Wenn Sie alle Änderungen des Editors verwerfen möchten, klicken Sie mit der rechten Maustaste auf das Gruppenrichtlinienobjekt, klicken Sie auf **Auschecken rückgängig machen**, und klicken Sie dann zum bestätigen auf **Ja** .

    -   Um die vom Editor vorgenommenen Änderungen beizubehalten, klicken Sie mit der rechten Maustaste auf das Gruppenrichtlinienobjekt, und klicken Sie dann auf **Einchecken**.

3.  Geben Sie einen Kommentar ein, der im Überwachungspfad des Gruppenrichtlinienobjekts angezeigt werden soll, und klicken Sie dann auf **OK**.

4.  Wenn das **Status** Fenster angibt, dass der Gesamtfortschritt abgeschlossen ist, klicken Sie auf **Schließen**. Auf der Registerkarte **gesteuert** wird der Status des Gruppenrichtlinienobjekts als **eingecheckt**gekennzeichnet.

### Weitere Überlegungen

-   Standardmäßig müssen Sie ein Editor, eine genehmigende Person oder ein AGPM-Administrator (Vollzugriff) sein, um dieses Verfahren ausführen zu können. Insbesondere müssen Sie über **Listeninhalte** und entweder **Einstellungen bearbeiten** oder GPO-Berechtigungen für das Gruppenrichtlinienobjekt **Bereitstellen** . Wenn Sie kein genehmigender oder AGPM-Administrator (oder ein anderer Gruppenrichtlinienadministrator mit der Berechtigung " **GPO bereitstellen** ") sind, müssen Sie der Herausgeber sein, der das Gruppenrichtlinienobjekt ausgecheckt hat.

### Weitere Verweise

-   [Durchführen der Aufgaben von genehmigenden Personen](performing-approver-tasks-agpm30ops.md)

-   [Offline-Bearbeitung eines Gruppenrichtlinienobjekts](edit-a-gpo-offline-agpm30ops.md)

 

 





