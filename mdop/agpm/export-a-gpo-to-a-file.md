---
title: Exportieren eines Gruppenrichtlinienobjekts in eine Datei
description: Exportieren eines Gruppenrichtlinienobjekts in eine Datei
author: dansimp
ms.assetid: 0d01b1f7-a6a4-4d0d-9aa7-2d6f1ae93d9d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4622930cb0e5b439649cc0445ae2b3d02d7d3224
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808472"
---
# Exportieren eines Gruppenrichtlinienobjekts in eine Datei


Sie können ein gesteuertes Gruppenrichtlinienobjekt (GPO) in eine CAB-Datei exportieren, damit Sie es in eine Domäne in einer anderen Gesamtstruktur kopieren und das Gruppenrichtlinienobjekt in die erweiterte Gruppenrichtlinienverwaltung (Group Policy Management, AGPM) in dieser Domäne importieren können. Informationen zum Importieren von GPO-Einstellungen in ein neues oder vorhandenes GPO finden Sie unter [Importieren eines Gruppenrichtlinienobjekts aus einer Datei](import-a-gpo-from-a-file-ed.md).

Zum Ausführen dieses Verfahrens ist ein Benutzerkonto mit der Rolle "Editor" oder "AGPM-Administrator" (Vollzugriff) oder den erforderlichen Berechtigungen in der erweiterten Gruppenrichtlinienverwaltung (Group Policy Management, AGPM) erforderlich.Lesen Sie die Details unter "Weitere Überlegungen" in diesem Thema.

**So exportieren Sie ein GPO in eine Datei**

1.  Klicken Sie in der Struktur der **Gruppenrichtlinien-Verwaltungskonsole** in der Gesamtstruktur und Domäne, in der Sie GPOs verwalten möchten, auf **Steuerelement ändern** .

2.  Klicken Sie auf der Registerkarte **Inhalt** auf die Registerkarte **gesteuert** , um die gesteuerten GPOs anzuzeigen.

3.  Klicken Sie mit der rechten Maustaste auf das Gruppenrichtlinienobjekt, und klicken Sie dann auf **Exportieren nach**.

4.  Geben Sie einen Dateinamen für die Datei ein, in die Sie das Gruppenrichtlinienobjekt exportieren möchten, und klicken Sie dann auf **exportieren**. Wenn die Datei nicht vorhanden ist, wird Sie erstellt. Wenn Sie bereits vorhanden ist, wird Sie ersetzt.

### Weitere Überlegungen

-   Standardmäßig müssen Sie ein Editor oder ein AGPM-Administrator (Vollzugriff) sein, um dieses Verfahren ausführen zu können. Insbesondere müssen Sie über **Listeninhalt**, **Leseeinstellungen**und Berechtigungen für das Gruppenrichtlinienobjekt **exportieren** verfügen.

### Weitere Verweise

-   [Verwenden einer Testumgebung](using-a-test-environment.md)

 

 





