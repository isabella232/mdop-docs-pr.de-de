---
title: Offline-Bearbeitung eines Gruppenrichtlinienobjekts
description: Offline-Bearbeitung eines Gruppenrichtlinienobjekts
author: dansimp
ms.assetid: 4a148952-9fe9-4ec4-8df1-b25e37c97a54
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6753ad21adb810e60e0b284204a61d4dd58c2384
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808487"
---
# Offline-Bearbeitung eines Gruppenrichtlinienobjekts


Wenn Sie Änderungen an einem gesteuerten Gruppenrichtlinienobjekt (GPO) vornehmen möchten, müssen Sie zuerst eine Kopie des Gruppenrichtlinienobjekts aus dem Archiv Auschecken. Niemand sonst kann das Gruppenrichtlinienobjekt so lange ändern, bis es erneut eingecheckt wird, wodurch die Einführung von widersprüchlichen Änderungen durch mehrere Gruppenrichtlinienadministratoren verhindert wird. Wenn Sie das Gruppenrichtlinienobjekt geändert haben, überprüfen Sie es in das Archiv, damit es überprüft und in der Produktionsumgebung bereitgestellt werden kann.

Ein Benutzerkonto mit der Rolle "Editor" oder "AGPM-Administrator (Vollzugriff)", das Benutzerkonto der genehmigenden Person, die das Gruppenrichtlinienobjekt erstellt hat, oder ein Benutzerkonto mit den erforderlichen Berechtigungen in der erweiterten Gruppenrichtlinienverwaltung ist erforderlich, um dieses Verfahren ausführen zu können. Lesen Sie die Details unter "Weitere Überlegungen" in diesem Thema.

## Offline Bearbeiten eines Gruppenrichtlinienobjekts


Wenn Sie ein GPO bearbeiten möchten, checken Sie das Gruppenrichtlinienobjekt aus dem Archiv aus, bearbeiten das Gruppenrichtlinienobjekt offline, und überprüfen das Gruppenrichtlinienobjekt dann in das Archiv, damit es überprüft und bereitgestellt (oder von anderen Editoren geändert) werden kann.

-   [Auschecken eines Gruppenrichtlinienobjekts](#bkmk-checkout)

-   [Bearbeiten eines Gruppenrichtlinienobjekts](#bkmk-edit)

-   [Einchecken eines Gruppenrichtlinienobjekts](#bkmk-checkin)

### <a href="" id="bkmk-checkout"></a>

**So checken Sie ein GPO aus dem Archiv zur Bearbeitung aus**

1.  Klicken Sie in der Struktur der **Gruppenrichtlinien-Verwaltungskonsole** in der Gesamtstruktur und Domäne, in der Sie GPOs verwalten möchten, auf **Steuerelement ändern** .

2.  Klicken Sie im Detailbereich auf der Registerkarte **Inhalt** auf die Registerkarte **gesteuert** , um die gesteuerten GPOs anzuzeigen.

3.  Klicken Sie mit der rechten Maustaste auf das zu bearbeitende GPO, und klicken Sie dann auf **Auschecken**.

4.  Geben Sie einen Kommentar ein, der im Verlauf des Gruppenrichtlinienobjekts angezeigt werden soll, während es ausgecheckt ist, und klicken Sie dann auf **OK**.

5.  Wenn das **Status** Fenster angibt, dass der Gesamtfortschritt abgeschlossen ist, klicken Sie auf **Schließen**. Auf der Registerkarte **gesteuert** wird der Status des Gruppenrichtlinienobjekts nun als **ausgecheckt**identifiziert.

### <a href="" id="bkmk-edit"></a>

**So bearbeiten Sie ein GPO offline**

1.  Klicken Sie auf der Registerkarte **gesteuert** mit der rechten Maustaste auf das Gruppenrichtlinienobjekt, das bearbeitet werden soll, und klicken Sie dann auf **Bearbeiten**.

2.  Nehmen Sie im **Gruppenrichtlinienobjekt-Editor**Änderungen an einer Offlinekopie des Gruppenrichtlinienobjekts vor.

3.  Wenn Sie die Änderung des Gruppenrichtlinienobjekts beendet haben, schließen Sie den **Gruppenrichtlinienobjekt-Editor**.

### <a href="" id="bkmk-checkin"></a>

**So überprüfen Sie ein GPO in das Archiv**

1.  Auf der Registerkarte " **gesteuert** ":

    -   Wenn Sie keine Änderungen am GPO vorgenommen haben, klicken Sie mit der rechten Maustaste auf das Gruppenrichtlinienobjekt, und klicken Sie auf **Auschecken rückgängig machen**, und klicken Sie dann zum bestätigen auf **Ja** .

    -   Wenn Sie Änderungen am GPO vorgenommen haben, klicken Sie mit der rechten Maustaste auf das Gruppenrichtlinienobjekt, und klicken Sie auf **Einchecken**.

2.  Geben Sie einen Kommentar ein, der im Überwachungspfad des Gruppenrichtlinienobjekts angezeigt werden soll, und klicken Sie dann auf **OK**.

3.  Wenn das **Status** Fenster angibt, dass der Gesamtfortschritt abgeschlossen ist, klicken Sie auf **Schließen**. Auf der Registerkarte **gesteuert** wird der Status des Gruppenrichtlinienobjekts als **eingecheckt**gekennzeichnet.

### Weitere Überlegungen

-   Zum Auschecken und Bearbeiten eines Gruppenrichtlinienobjekts müssen Sie standardmäßig die genehmigende Person sein, die das Gruppenrichtlinienobjekt, einen Editor oder einen AGPM-Administrator erstellt oder gesteuert hat (Vollzugriff). Insbesondere müssen Sie über **Listeninhalte** und Berechtigungen zum **Bearbeiten von Einstellungen** für das Gruppenrichtlinienobjekt verfügen. Darüber hinaus müssen Sie zum Bearbeiten des Gruppenrichtlinienobjekts die Person sein, die das Gruppenrichtlinienobjekt ausgecheckt hat.

-   Zum Einchecken eines Gruppenrichtlinienobjekts müssen Sie standardmäßig ein Editor, eine genehmigende Person oder ein AGPM-Administrator (Vollzugriff) sein. Insbesondere müssen Sie über **Listeninhalte** und entweder **Einstellungen bearbeiten** oder GPO-Berechtigungen für das Gruppenrichtlinienobjekt **Bereitstellen** . Wenn Sie kein genehmigender oder AGPM-Administrator (oder ein anderer Gruppenrichtlinienadministrator mit der Berechtigung " **GPO bereitstellen** ") sind, müssen Sie der Herausgeber sein, der das Gruppenrichtlinienobjekt ausgecheckt hat.

-   Beim Bearbeiten eines Gruppenrichtlinienobjekts sollten alle Gruppenrichtlinien-Software Installations Upgrades eines Pakets in einem anderen Gruppenrichtlinienobjekt auf das bereitgestellte GPO verweisen, nicht auf die ausgecheckte Kopie.

### Weitere Verweise

-   [Bearbeiten eines Gruppenrichtlinienobjekts](editing-a-gpo.md)

-   Überprüfen eines Gruppenrichtlinienobjekts

    -   [Überprüfen von GPO-Einstellungen](review-gpo-settings.md)

    -   [Überprüfen von GPO-Links](review-gpo-links.md)

    -   [Ermitteln der Unterschiede zwischen Gruppenrichtlinienobjekten und Versionen oder Vorlagen von Gruppenrichtlinienobjekten](identify-differences-between-gpos-gpo-versions-or-templates.md)

-   Bereitstellen eines Gruppenrichtlinienobjekts

    -   [Anfordern der Bereitstellung eines Gruppenrichtlinienobjekts](request-deployment-of-a-gpo.md)

    -   [Bereitstellen eines Gruppenrichtlinienobjekts](deploy-a-gpo.md)

 

 





