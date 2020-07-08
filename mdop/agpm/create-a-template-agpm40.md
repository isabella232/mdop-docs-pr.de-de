---
title: Erstellen einer Vorlage
description: Erstellen einer Vorlage
author: dansimp
ms.assetid: b38423af-7d24-437a-98bc-01f1ae891127
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: dd50dd41863e383b931b8563854a8bbd4ee196d5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808560"
---
# Erstellen einer Vorlage


Beim Erstellen einer Vorlage können Sie alle Einstellungen einer bestimmten Version eines Gruppenrichtlinienobjekts speichern, um Sie als Ausgangspunkt zum Erstellen neuer GPOs zu verwenden.

**Hinweis**  Eine Vorlage ist eine nicht bearbeitbare, statische Version eines GPO, die als Ausgangspunkt zum Erstellen neuer, bearbeitbarer GPOs verwendet werden kann.

 

Zum Ausführen dieses Verfahrens ist ein Benutzerkonto mit der Rolle "Editor" oder "AGPM-Administrator" (Vollzugriff) oder den erforderlichen Berechtigungen in der erweiterten Gruppenrichtlinienverwaltung (Group Policy Management, AGPM) erforderlich. Lesen Sie die Details unter "Weitere Überlegungen" in diesem Thema.

**So erstellen Sie eine Vorlage auf der Grundlage eines vorhandenen Gruppenrichtlinienobjekts**

1.  Klicken Sie in der Struktur der **Gruppenrichtlinien-Verwaltungskonsole** in der Gesamtstruktur und Domäne, in der Sie GPOs verwalten möchten, auf **Steuerelement ändern** .

2.  Klicken Sie im Detailbereich auf der Registerkarte **Inhalt** auf die Registerkarte **gesteuert** oder **unkontrolliert** , um verfügbare GPOs anzuzeigen.

3.  Klicken Sie mit der rechten Maustaste auf das Gruppenrichtlinienobjekt, aus dem Sie eine Vorlage erstellen möchten, und klicken Sie dann auf **als Vorlage speichern**.

4.  Geben Sie einen Namen für die Vorlage und einen Kommentar ein, und klicken Sie dann auf **OK**.

5.  Wenn das **Status** Fenster angibt, dass der Gesamtfortschritt abgeschlossen ist, klicken Sie auf **Schließen**. Die neue Vorlage wird auf der Registerkarte **Vorlagen** angezeigt.

### Weitere Überlegungen

-   Standardmäßig müssen Sie ein Editor oder ein AGPM-Administrator (Vollzugriff) sein, um dieses Verfahren ausführen zu können. Insbesondere müssen Sie über **Listeninhalte** und **Vorlagen** Berechtigungen für die Domäne verfügen.

-   Das Umbenennen oder Löschen einer Vorlage wirkt sich nicht auf GPOs aus, die mit dieser Vorlage erstellt wurden.

-   Da Sie nicht geändert werden kann, hat eine Vorlage keinen Verlauf.

### Weitere Verweise

-   [Erstellen einer Vorlage und zum Festlegen einer Standardvorlage](creating-a-template-and-setting-a-default-template-agpm40.md)

-   [Anfordern der Erstellung eines neuen gesteuerten Gruppenrichtlinienobjekts](request-the-creation-of-a-new-controlled-gpo-agpm40.md)

 

 





