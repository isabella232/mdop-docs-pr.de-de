---
title: Importieren eines Gruppenrichtlinienobjekts aus der Produktion
description: Importieren eines Gruppenrichtlinienobjekts aus der Produktion
author: dansimp
ms.assetid: 071270fa-1890-40ce-ab89-ce070a54aa59
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6974edc08805b56a7a69925f4c10233720488314
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808408"
---
# Importieren eines Gruppenrichtlinienobjekts aus der Produktion


Wenn Änderungen an einem gesteuerten Gruppenrichtlinienobjekt (GPO) außerhalb der erweiterten Gruppenrichtlinienverwaltung (Group Policy Management, AGPM) vorgenommen werden, können Sie eine Kopie des Gruppenrichtlinienobjekts aus der Produktionsumgebung importieren und im Archiv speichern, um das Archiv und die Produktionsumgebung in einen konsistenten Zustand zu versetzen. (Zum Importieren eines nicht kontrollierten Gruppenrichtlinienobjekts steuern Sie das Gruppenrichtlinienobjekt. Siehe [Steuern eines zuvor unkontrollierten Gruppenrichtlinienobjekts](control-a-previously-uncontrolled-gpo.md).)

Zum Ausführen dieses Verfahrens ist ein Benutzerkonto mit der Rolle "Editor", "Genehmiger" oder "AGPM-Administrator" (Vollzugriff) oder den erforderlichen Berechtigungen in der erweiterten Gruppenrichtlinienverwaltung erforderlich. Lesen Sie die Details unter "Weitere Überlegungen" in diesem Thema.

**So importieren Sie ein GPO aus der Produktionsumgebung**

1.  Klicken Sie in der Struktur der **Gruppenrichtlinien-Verwaltungskonsole** in der Gesamtstruktur und Domäne, in der Sie GPOs verwalten möchten, auf **Steuerelement ändern** .

2.  Klicken Sie auf der Registerkarte **Inhalt** auf die Registerkarte **gesteuert** , um die gesteuerten GPOs anzuzeigen.

3.  Klicken Sie mit der rechten Maustaste auf das Gruppenrichtlinienobjekt, und klicken Sie dann auf **aus Produktion importieren**.

4.  Geben Sie einen Kommentar für den Überwachungspfad des Gruppenrichtlinienobjekts ein, und klicken Sie dann auf **OK**.

### Weitere Überlegungen

-   Standardmäßig müssen Sie Bearbeiter, genehmigende Person oder AGPM-Administrator (Vollzugriff) sein, um dieses Verfahren ausführen zu können. Insbesondere müssen Sie über **Listeninhalte** und entweder **Einstellungen bearbeiten**, **Gruppenrichtlinienobjekt bereitstellen**oder Berechtigungen für **Gruppenrichtlinienobjekte löschen** für das Gruppenrichtlinienobjekt verfügen.

### Weitere Verweise

-   [Erstellen, Steuern oder Importieren eines Gruppenrichtlinienobjekts](creating-controlling-or-importing-a-gpo-approver.md)

 

 





