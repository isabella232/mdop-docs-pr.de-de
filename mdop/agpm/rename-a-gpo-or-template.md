---
title: Benennen Sie ein Gruppenrichtlinienobjekt oder eine Vorlage
description: Benennen Sie ein Gruppenrichtlinienobjekt oder eine Vorlage
author: dansimp
ms.assetid: 64a1aaf4-f672-48b5-94c6-473bf1076cf3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 495fc090487ff324bc19c89dcd36ecf0efbcb151
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807528"
---
# Benennen Sie ein Gruppenrichtlinienobjekt oder eine Vorlage


Sie können ein gesteuertes Gruppenrichtlinienobjekt oder eine Vorlage umbenennen.

Ein Benutzerkonto mit der Rolle "Editor" oder "AGPM-Administrator (Vollzugriff)", das Benutzerkonto der genehmigenden Person, die das Gruppenrichtlinienobjekt erstellt hat, oder ein Benutzerkonto mit den erforderlichen Berechtigungen in der erweiterten Gruppenrichtlinienverwaltung ist erforderlich, um dieses Verfahren ausführen zu können. Lesen Sie die Details unter "Weitere Überlegungen" in diesem Thema.

**So benennen Sie ein GPO oder eine Vorlage um**

1.  Klicken Sie in der Struktur der **Gruppenrichtlinien-Verwaltungskonsole** in der Gesamtstruktur und Domäne, in der Sie GPOs verwalten möchten, auf **Steuerelement ändern** .

2.  Klicken Sie auf der Registerkarte **Inhalt** auf die Registerkarte **gesteuert** oder **Vorlagen** , um das umzubenennende Element anzuzeigen.

3.  Klicken Sie mit der rechten Maustaste auf das zu umbenennende GPO oder die Vorlage, und klicken Sie auf **Umbenennen**.

4.  Geben Sie den neuen Namen für das Gruppenrichtlinienobjekt oder die Vorlage und einen Kommentar ein, und klicken Sie dann auf **OK**.

5.  Wenn das **Status** Fenster angibt, dass der Gesamtfortschritt abgeschlossen ist, klicken Sie auf **Schließen**. Das Gruppenrichtlinienobjekt oder die Vorlage wird auf der Registerkarte **Inhalt** unter dem neuen Namen angezeigt.

### Weitere Überlegungen

-   Standardmäßig müssen Sie die genehmigende Person sein, die das Gruppenrichtlinienobjekt, einen Editor oder einen AGPM-Administrator (Vollzugriff) erstellt oder gesteuert hat, um dieses Verfahren ausführen zu können. Insbesondere müssen Sie über die Berechtigung " **Listeninhalt** " und " **Einstellungen bearbeiten** " für das Gruppenrichtlinienobjekt verfügen.

-   Wenn Sie ein bereitgestelltes GPO umbenennen, wird der Name sofort im Archiv geändert. Der Name wird in der Produktionsumgebung nur geändert, wenn das Gruppenrichtlinienobjekt erneut bereitgestellt wird.

    Bis das Gruppenrichtlinienobjekt erneut bereitgestellt wird (oder die Produktionskopie gelöscht wird), wird der alte Name noch in der Produktionsumgebung verwendet und kann daher nicht für ein anderes GPO verwendet werden. Ebenso kann das Gruppenrichtlinienobjekt im Archiv erst wieder in seinen ursprünglichen Namen umbenannt werden, nachdem das Gruppenrichtlinienobjekt bereitgestellt wurde (Ändern des Namens der Produktionskopie) oder die Produktionskopie gelöscht wurde.

### Weitere Verweise

-   [Bearbeiten eines Gruppenrichtlinienobjekts](editing-a-gpo.md)

 

 





