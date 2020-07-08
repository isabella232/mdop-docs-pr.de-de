---
title: Beschriften der aktuellen Version eines Gruppenrichtlinienobjekts
description: Beschriften der aktuellen Version eines Gruppenrichtlinienobjekts
author: dansimp
ms.assetid: 5e4e50f8-e4a8-4bda-aac4-1569d5fbd6a7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a34232dfd1f7a755dd81cdecbe3d5d1957f01294
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808383"
---
# Beschriften der aktuellen Version eines Gruppenrichtlinienobjekts


Sie können die aktuelle Version eines Gruppenrichtlinienobjekts zur einfachen Identifizierung in seinem Protokoll beschriften. Sie können eine Bezeichnung verwenden, um eine zweifelsfrei funktionierende Version zu identifizieren, bei der ein Rollback ausgeführt werden kann, wenn ein Problem auftritt. Wenn Sie mehrere GPOs gleichzeitig mit demselben Etikett versehen, können Sie auch Verwandte GPOs kennzeichnen, für die ein Rollback zum gleichen Zeitpunkt ausgeführt werden soll, wenn später ein Rollback erforderlich ist.

Zum Ausführen dieses Verfahrens ist ein Benutzerkonto mit der Rolle "Editor", "Genehmiger" oder "AGPM-Administrator" (Vollzugriff) oder den erforderlichen Berechtigungen in der erweiterten Gruppenrichtlinienverwaltung erforderlich. Lesen Sie die Details unter "Weitere Überlegungen" in diesem Thema.

**So beschriften Sie die aktuelle Version von GPOs in ihren Verlaufsdaten**

1.  Klicken Sie in der Struktur der **Gruppenrichtlinien-Verwaltungskonsole** in der Gesamtstruktur und Domäne, in der Sie GPOs verwalten möchten, auf **Steuerelement ändern** .

2.  Klicken Sie auf der Registerkarte **Inhalt** auf die Registerkarte **gesteuert** , um die gesteuerten GPOs anzuzeigen.

3.  Klicken Sie auf ein GPO, für das die aktuelle Version beschriftet werden soll. Wenn Sie mehrere GPOs auswählen möchten, drücken Sie die UMSCHALTTASTE, und klicken Sie auf das letzte GPO in einer zusammenhängenden Gruppe von GPOs, oder drücken Sie STRG, und klicken Sie auf einzelne GPOs. Klicken Sie mit der rechten Maustaste auf ein ausgewähltes Gruppenrichtlinienobjekt, und klicken Sie dann auf **Beschriftung**.

4.  Geben Sie eine Beschriftung und einen Kommentar ein, die im Verlauf der einzelnen ausgewählten Gruppenrichtlinienobjekte angezeigt werden sollen, und klicken Sie dann auf **OK**.

5.  Wenn das **Status** Fenster angibt, dass der Gesamtfortschritt abgeschlossen ist, klicken Sie auf **Schließen**.

### Weitere Überlegungen

-   Standardmäßig müssen Sie ein Editor, eine genehmigende Person oder ein AGPM-Administrator (Vollzugriff) sein, um dieses Verfahren ausführen zu können. Insbesondere müssen Sie über **Listeninhalte** und entweder **Einstellungen bearbeiten** oder GPO-Berechtigungen für das Gruppenrichtlinienobjekt **Bereitstellen** .

### Weitere Verweise

-   [Bearbeiten eines Gruppenrichtlinienobjekts](editing-a-gpo.md)

 

 





