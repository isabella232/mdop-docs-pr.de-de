---
title: Überprüfen von GPO-Links
description: Überprüfen von GPO-Links
author: dansimp
ms.assetid: 3aaba9da-f0aa-466f-bd1c-49f11d00ea54
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3884a6f3852986cf02e499af59bb56fcaf404ef8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807471"
---
# Überprüfen von GPO-Links


Sie können ein Diagramm anzeigen, das zeigt, wo ein von Ihnen ausgewähltes Gruppenrichtlinienobjekt (GPO) oder GPOs mit Organisationseinheiten verknüpft sind. GPO-Verknüpfungs Diagramme werden jedes Mal aktualisiert, wenn das Gruppenrichtlinienobjekt gesteuert, importiert oder eingecheckt wird.

Zum Ausführen dieses Verfahrens ist ein Benutzerkonto mit der Rolle Prüfer, Bearbeiter, genehmigende Person oder AGPM-Administrator (Vollzugriff) oder den erforderlichen Berechtigungen in Advanced Group Policy Management (AGPM) erforderlich. Lesen Sie die Details unter "Weitere Überlegungen" in diesem Thema.

## Überprüfen von GPO-Links


-   [Für ein oder mehrere GPOs](#bkmk-gpos)

-   [Für eine oder mehrere Versionen eines Gruppenrichtlinienobjekts](#bkmk-gpo-versions)

### <a href="" id="bkmk-gpos"></a>

**So zeigen Sie GPO-Links für ein oder mehrere GPOs an**

1.  Klicken Sie in der Struktur der **Gruppenrichtlinien-Verwaltungskonsole** in der Gesamtstruktur und Domäne, in der Sie GPOs verwalten möchten, auf **Steuerelement ändern** .

2.  Klicken Sie im Detailbereich auf der Registerkarte **Inhalt** auf die Registerkarte **gesteuert**, **Ausstehend**oder **Papierkorb** , um GPOs anzuzeigen.

3.  Wählen Sie ein oder mehrere GPOs aus, für die Links angezeigt werden sollen, klicken Sie mit der rechten Maustaste auf ein ausgewähltes Gruppenrichtlinienobjekt, klicken Sie auf **Einstellungen**, und klicken Sie dann auf **GPO-Links** , um ein Diagramm mit Domänen und Organisationseinheiten mit Links zu den ausgewählten Gruppenrichtlinienobjekten anzuzeigen.

### <a href="" id="bkmk-gpo-versions"></a>

**So zeigen Sie GPO-Links für eine oder mehrere Versionen eines GPO an**

1.  Klicken Sie in der Struktur der **Gruppenrichtlinien-Verwaltungskonsole** in der Gesamtstruktur und Domäne, in der Sie GPOs verwalten möchten, auf **Steuerelement ändern** .

2.  Klicken Sie im Detailbereich auf der Registerkarte **Inhalt** auf die Registerkarte **gesteuerter** oder **Papierkorb** , um GPOs anzuzeigen.

3.  Doppelklicken Sie auf das Gruppenrichtlinienobjekt, um dessen Verlauf anzuzeigen.

4.  Klicken Sie mit der rechten Maustaste auf die GPO-Version, für die Sie die Einstellungen überprüfen möchten, klicken Sie auf **Einstellungen**, und klicken Sie dann auf **HTML-Bericht** oder **XML-Bericht** , um eine Zusammenfassung der GPO-Einstellungen anzuzeigen.

### Weitere Überlegungen

-   Standardmäßig müssen Sie ein Prüfer, ein Bearbeiter, eine genehmigende Person oder ein AGPM-Administrator (Vollzugriff) sein, um dieses Verfahren ausführen zu können. Insbesondere müssen Sie über die Berechtigungen **Listeninhalt** und **Leseeinstellungen** für das Gruppenrichtlinienobjekt verfügen. Außerdem müssen Sie zum Anzeigen der Liste der GPOs über die Berechtigung **Listeninhalt** für die Domäne verfügen.

### Weitere Verweise

-   [Durchführen von Prüferaufgaben](performing-reviewer-tasks-agpm40.md)

 

 





