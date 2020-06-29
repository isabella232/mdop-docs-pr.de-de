---
title: Anfordern eines nicht gesteuerten Gruppenrichtlinienobjekts
description: Anfordern eines nicht gesteuerten Gruppenrichtlinienobjekts
author: dansimp
ms.assetid: a34e0aeb-33a1-4c9f-b187-1d08493a785c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: bfccd7285f82990c2447319485738131cf559f48
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807511"
---
# Anfordern eines nicht gesteuerten Gruppenrichtlinienobjekts


Um das Change-Steuerelement für ein vorhandenes Gruppenrichtlinienobjekt (GPO) bereitstellen zu können, muss das Gruppenrichtlinienobjekt gesteuert werden. Sofern Sie keine genehmigende Person oder ein AGPM-Administrator (Vollzugriff) sind, müssen Sie die Steuerung des GPO anfordern.

Um dieses Verfahren ausführen zu können, ist ein Benutzerkonto mit der Rolle "Bearbeiter" oder "Prüfer" oder die erforderlichen Berechtigungen in Advanced Group Policy Management (AGPM) erforderlich. Lesen Sie die Details unter "Weitere Überlegungen" in diesem Thema.

**So steuern Sie ein nicht gesteuertes Gruppenrichtlinienobjekt**

1.  Klicken Sie in der Struktur der **Gruppenrichtlinien-Verwaltungskonsole** in der Gesamtstruktur und Domäne, in der Sie GPOs verwalten möchten, auf **Steuerelement ändern** .

2.  Klicken Sie im Detailbereich auf der Registerkarte **Inhalt** auf die Registerkarte **unkontrolliert** , um die nicht kontrollierten GPOs anzuzeigen.

3.  Klicken Sie mit der rechten Maustaste auf das Gruppenrichtlinienobjekt, das mit AGPM gesteuert werden soll, und klicken Sie dann auf **Steuerelement**.

4.  Sofern Sie keine spezielle Berechtigung zum Steuern von GPOs haben, müssen Sie eine Kontroll Anforderung einreichen. Wenn Sie eine Kopie der Anfrage erhalten möchten, geben Sie Ihre e-Mail-Adresse in das Feld **CC** ein. Geben Sie einen Kommentar ein, der im **Verlauf** des Gruppenrichtlinienobjekts angezeigt werden soll, und klicken Sie dann auf **Absenden**.

5.  Wenn das **Status** Fenster angibt, dass der Gesamtfortschritt abgeschlossen ist, klicken Sie auf **Schließen**. Das Gruppenrichtlinienobjekt wird auf der Registerkarte **unkontrolliert** aus der Liste entfernt und der Registerkarte **Ausstehend** hinzugefügt. Wenn eine genehmigende Person Ihre Anfrage genehmigt hat, wird das Gruppenrichtlinienobjekt auf die Registerkarte **gesteuert** verschoben.

### Weitere Überlegungen

-   Standardmäßig müssen Sie ein Editor oder ein Bearbeiter sein, um dieses Verfahren ausführen zu können. Insbesondere müssen Sie über die Berechtigungen **Listeninhalt** und **Leseeinstellungen** für die Domäne verfügen.

-   Wenn Sie Ihre Anfrage zurücknehmen möchten, bevor Sie genehmigt wurde, klicken Sie auf die Registerkarte **Ausstehend** . Klicken Sie mit der rechten Maustaste auf das GPO, und klicken Sie dann auf **zurück** Das Gruppenrichtlinienobjekt wird auf die Registerkarte **unkontrolliert** zurückgegeben.

### Weitere Verweise

-   [Erstellen oder Steuern eines Gruppenrichtlinienobjekts](creating-or-controlling-a-gpo-agpm40-ed.md)

 

 





