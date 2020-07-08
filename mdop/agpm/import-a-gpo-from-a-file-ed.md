---
title: Importieren eines Gruppenrichtlinienobjekts aus einer Datei
description: Importieren eines Gruppenrichtlinienobjekts aus einer Datei
author: dansimp
ms.assetid: 6e901a52-1101-4fed-9f90-3819b573b378
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e15704806f089bb0d8530cd84df64b0889413426
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808420"
---
# Importieren eines Gruppenrichtlinienobjekts aus einer Datei


Wenn Sie in der erweiterten Gruppenrichtlinienverwaltung (Group Policy Management, AGPM) ein Gruppenrichtlinienobjekt in eine CAB-Datei exportiert haben, können Sie die Richtlinieneinstellungen aus diesem GPO in ein vorhandenes GPO in einer Domäne in einer anderen Gesamtstruktur importieren. Durch das Importieren von Richtlinieneinstellungen in ein vorhandenes GPO werden alle Richtlinieneinstellungen innerhalb dieses Gruppenrichtlinienobjekts ersetzt. Informationen zum Exportieren von GPO-Einstellungen in eine CAB-Datei finden Sie unter [Exportieren eines Gruppenrichtlinienobjekts in eine Datei](export-a-gpo-to-a-file.md).

Zum Ausführen dieses Verfahrens ist ein Benutzerkonto mit der Rolle "Editor" oder "AGPM-Administrator" (Vollzugriff) oder den erforderlichen Berechtigungen in der erweiterten Gruppenrichtlinienverwaltung (Group Policy Management, AGPM) erforderlich.Lesen Sie die Details unter "Weitere Überlegungen" in diesem Thema.

## <a href="" id="bkmk-existing"></a>


**So importieren Sie Richtlinieneinstellungen in ein vorhandenes Gruppenrichtlinienobjekt**

1.  Klicken Sie in der **Gruppenrichtlinien-Verwaltungskonsolen** Struktur in der Domäne, für die Sie Richtlinieneinstellungen importieren möchten, auf **Steuerelement ändern** .

2.  Klicken Sie auf der Registerkarte **Inhalt** auf die Registerkarte **gesteuert** , um die gesteuerten GPOs anzuzeigen.

3.  Überprüfen Sie das Ziel-GPO, in das Sie Richtlinieneinstellungen importieren möchten.

4.  Klicken Sie mit der rechten Maustaste auf das Ziel-GPO, zeigen Sie auf **Importieren von**, und klicken Sie dann auf **Datei**.

5.  Befolgen Sie die Anweisungen im **Assistenten zum Importieren von Einstellungen** , um eine GPO-Sicherung auszuwählen, importieren Sie deren Richtlinieneinstellungen, um diese im Zielgruppen Richtlinienobjekt zu ersetzen, und geben Sie einen Kommentar für den Überwachungspfad des Zielgruppen Richtlinienobjekts ein. Standardmäßig ist das Ziel-GPO nach Abschluss des Assistenten eingecheckt.

### Weitere Überlegungen

-   Standardmäßig müssen Sie ein Editor oder ein AGPM-Administrator (Vollzugriff) sein, um dieses Verfahren ausführen zu können. Insbesondere müssen Sie über **Listeninhalte**, **Einstellungen zum Bearbeiten**und **Importieren von GPO** -Berechtigungen für die Domäne verfügen, und das Gruppenrichtlinienobjekt muss von Ihnen ausgecheckt sein.

-   Obwohl ein Editor während der Erstellung keine Richtlinieneinstellungen in ein neues GPO importieren kann, kann ein Editor die Erstellung eines neuen Gruppenrichtlinienobjekts anfordern und dann Richtlinieneinstellungen importieren, nachdem es erstellt wurde.

### Weitere Verweise

-   [Verwenden einer Testumgebung](using-a-test-environment.md)

 

 





