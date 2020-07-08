---
title: Festlegen einer Standardvorlage
description: Festlegen einer Standardvorlage
author: dansimp
ms.assetid: e0acf980-437f-4357-b237-298aaebe490d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 870c1d4c13049992509f6aa831966736e6ba25ef
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808223"
---
# Festlegen einer Standardvorlage


Als Editor können Sie angeben, welche der verfügbaren Vorlagen die Standardvorlage sein soll, die für alle Gruppenrichtlinienadministratoren vorgeschlagen wird, die neue Gruppenrichtlinienobjekte (Group Policy Objects, GPOs) erstellen.

**Hinweis**  Eine Vorlage ist eine nicht bearbeitbare, statische Version eines GPO, die als Ausgangspunkt zum Erstellen neuer, bearbeitbarer GPOs verwendet werden kann.

 

Zum Ausführen dieses Verfahrens ist ein Benutzerkonto mit der Rolle "Editor" oder "AGPM-Administrator" (Vollzugriff) oder den erforderlichen Berechtigungen in der erweiterten Gruppenrichtlinienverwaltung erforderlich. Lesen Sie die Details unter "Weitere Überlegungen" in diesem Thema.

**So legen Sie die Standardvorlage für die Verwendung beim Erstellen neuer GPOs vor**

1.  Klicken Sie in der Struktur der **Gruppenrichtlinien-Verwaltungskonsole** in der Gesamtstruktur und Domäne, in der Sie GPOs verwalten möchten, auf **Steuerelement ändern** .

2.  Klicken Sie im Detailbereich auf der Registerkarte **Inhalt** auf die Registerkarte **Vorlagen** , um die verfügbaren Vorlagen anzuzeigen.

3.  Klicken Sie mit der rechten Maustaste auf die Vorlage, die Sie als Standard festlegen möchten, und klicken Sie dann auf **als Standard festlegen**.

4.  Klicken Sie zum bestätigen auf **Ja** .

5.  Wenn das **Status** Fenster angibt, dass der Gesamtfortschritt abgeschlossen ist, klicken Sie auf **Schließen**. Die Standardvorlage weist ein blaues Symbol auf, und der Status wird auf der Registerkarte **Vorlagen** als **Vorlage (Standard)** bezeichnet.

### Weitere Überlegungen

-   Standardmäßig müssen Sie ein Editor oder ein AGPM-Administrator (Vollzugriff) sein, um dieses Verfahren ausführen zu können. Insbesondere müssen Sie über **Listeninhalte** und **Vorlagen** Berechtigungen für die Domäne verfügen.

-   Nachdem Sie eine Vorlage als Standardvorlage festgelegt haben, wird diese Vorlage im Dialogfeld **Neues gesteuertes Gruppenrichtlinienobjekt** ausgewählt, wenn Gruppenrichtlinienadministratoren neue GPOs erstellen. Sie haben jedoch die Möglichkeit, eine beliebige andere GPO-Vorlage zu wählen, einschließlich eines ** &lt; leeren Gruppenrichtlinienobjekts &gt; **, das keine Einstellungen enthält.

-   Das Umbenennen oder Löschen einer Vorlage wirkt sich nicht auf GPOs aus, die mit dieser Vorlage erstellt wurden.

-   Da Sie nicht geändert werden kann, hat eine Vorlage keinen Verlauf.

### Weitere Verweise

-   [Erstellen einer Vorlage und zum Festlegen einer Standardvorlage](creating-a-template-and-setting-a-default-template.md)

-   [Anfordern der Erstellung eines neuen gesteuerten Gruppenrichtlinienobjekts](request-the-creation-of-a-new-controlled-gpo.md)

 

 





