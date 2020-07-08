---
title: Anfordern der Steuerung eines zuvor nicht gesteuerten Gruppenrichtlinienobjekts
description: Anfordern der Steuerung eines zuvor nicht gesteuerten Gruppenrichtlinienobjekts
author: dansimp
ms.assetid: 00e8725d-5d7f-4eed-a5e6-c3631632cfbd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a92db48d87398568900fc0031e688c862a69b417
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807516"
---
# Anfordern der Steuerung eines zuvor nicht gesteuerten Gruppenrichtlinienobjekts


Um die erweiterte Gruppenrichtlinienverwaltung (Group Policy Management, AGPM) zum Bereitstellen von Änderungs Steuerelementen für ein vorhandenes Gruppenrichtlinienobjekt (GPO) zu verwenden, muss das Gruppenrichtlinienobjekt mit AGPM gesteuert werden. Sofern Sie keine genehmigende Person oder ein AGPM-Administrator (Vollzugriff) sind, müssen Sie die Steuerung des GPO anfordern.

Zum Ausführen dieses Verfahrens ist ein Benutzerkonto mit der Rolle "Bearbeiter" oder "Prüfer" oder die erforderlichen Berechtigungen in der erweiterten Gruppenrichtlinienverwaltung erforderlich. Lesen Sie die Details unter "Weitere Überlegungen" in diesem Thema.

**So steuern Sie ein zuvor unkontrolliertes Gruppenrichtlinienobjekt**

1.  Klicken Sie in der Struktur der **Gruppenrichtlinien-Verwaltungskonsole** in der Gesamtstruktur und Domäne, in der Sie GPOs verwalten möchten, auf **Steuerelement ändern** .

2.  Klicken Sie im Detailbereich auf der Registerkarte **Inhalt** auf die Registerkarte **unkontrolliert** , um die nicht kontrollierten GPOs anzuzeigen.

3.  Klicken Sie mit der rechten Maustaste auf das Gruppenrichtlinienobjekt, das mit AGPM gesteuert werden soll, und klicken Sie dann auf **Steuerelement**.

4.  Sofern Sie keine spezielle Berechtigung zum Steuern von GPOs haben, müssen Sie eine Kontroll Anforderung einreichen. Wenn Sie eine Kopie der Anfrage erhalten möchten, geben Sie Ihre e-Mail-Adresse in das Feld **CC** ein. Geben Sie einen Kommentar ein, der im **Verlauf** des Gruppenrichtlinienobjekts angezeigt werden soll, und klicken Sie dann auf **Absenden**.

5.  Wenn das **Status** Fenster angibt, dass der Gesamtfortschritt abgeschlossen ist, klicken Sie auf **Schließen**. Das Gruppenrichtlinienobjekt wird auf der Registerkarte **unkontrolliert** aus der Liste entfernt und der Registerkarte **Ausstehend** hinzugefügt. Wenn eine genehmigende Person Ihre Anfrage genehmigt hat, wird das Gruppenrichtlinienobjekt auf die Registerkarte **gesteuert** verschoben.

### Weitere Überlegungen

-   Standardmäßig müssen Sie ein Editor oder ein Bearbeiter sein, um dieses Verfahren ausführen zu können. Insbesondere müssen Sie über die Berechtigungen **Listeninhalt** und **Leseeinstellungen** für die Domäne verfügen.

-   Wenn Sie Ihre Anfrage zurücknehmen möchten, bevor Sie genehmigt wurde, klicken Sie auf die Registerkarte **Ausstehend** . Klicken Sie mit der rechten Maustaste auf das GPO, und klicken Sie dann auf **zurück** Das Gruppenrichtlinienobjekt wird auf die Registerkarte **unkontrolliert** zurückgegeben.

### Weitere Verweise

-   [Erstellen, Steuern oder Importieren eines Gruppenrichtlinienobjekts](creating-controlling-or-importing-a-gpo-editor.md)

 

 





