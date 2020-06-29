---
title: Überprüfen von GPO-Einstellungen
description: Überprüfen von GPO-Einstellungen
author: dansimp
ms.assetid: bed956d0-082e-4fa9-bf1e-572d0d3d02ec
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 23d18eb5a41b4246964b79f687eb9fa44b98b730
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807467"
---
# Überprüfen von GPO-Einstellungen


Sie können HTML-basierte und XML-basierte Berichte zum Überprüfen von Einstellungen innerhalb einer beliebigen Version eines Gruppenrichtlinienobjekts (GPO) erstellen.

Zum Ausführen dieses Verfahrens ist ein Benutzerkonto mit der Rolle Prüfer, Bearbeiter, genehmigende Person oder AGPM-Administrator (Vollzugriff) oder den erforderlichen Berechtigungen in Advanced Group Policy Management (AGPM) erforderlich. Lesen Sie die Details unter "Weitere Überlegungen" in diesem Thema.

**So überprüfen Sie die Einstellungen in einer beliebigen Version eines Gruppenrichtlinienobjekts**

1.  Klicken Sie in der Struktur der **Gruppenrichtlinien-Verwaltungskonsole** in der Gesamtstruktur und Domäne, in der Sie GPOs verwalten möchten, auf **Steuerelement ändern** .

2.  Klicken Sie im Detailbereich auf der Registerkarte **Inhalt** auf eine Registerkarte, um GPOs anzuzeigen.

3.  Doppelklicken Sie auf das Gruppenrichtlinienobjekt, um dessen Verlauf anzuzeigen.

4.  Klicken Sie mit der rechten Maustaste auf die GPO-Version, für die Sie die Einstellungen überprüfen möchten, klicken Sie auf **Einstellungen**, und klicken Sie dann auf **HTML-Bericht** oder **XML-Bericht** , um eine Zusammenfassung der GPO-Einstellungen anzuzeigen.

### Weitere Überlegungen

-   Standardmäßig müssen Sie ein Prüfer, ein Bearbeiter, eine genehmigende Person oder ein AGPM-Administrator (Vollzugriff) sein, um dieses Verfahren ausführen zu können. Insbesondere müssen Sie über die Berechtigungen **Listeninhalt** und **Leseeinstellungen** für das Gruppenrichtlinienobjekt verfügen. Außerdem müssen Sie zum Anzeigen der Liste der GPOs über die Berechtigung **Listeninhalt** für die Domäne verfügen.

### Weitere Verweise

-   [Durchführen von Prüferaufgaben](performing-reviewer-tasks-agpm30ops.md)

 

 





