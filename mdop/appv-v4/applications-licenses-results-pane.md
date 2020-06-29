---
title: Bereich „Ergebnisse für Anwendungslizenzen“
description: Bereich „Ergebnisse für Anwendungslizenzen“
author: dansimp
ms.assetid: 8b519715-b2fe-451e-ad9b-e9b73f454961
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9e5a86c22e67e061ec873317c455958536fae75b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807935"
---
# Bereich „Ergebnisse für Anwendungslizenzen“


Der Bereich **Anwendungen-Lizenzen Ergebnisse** in der Application Virtualization Server Management Console zeigt eine Liste der verfügbaren Anwendungslizenzgruppen und Anwendungslizenzen an.

Klicken Sie mit der rechten Maustaste auf eine beliebige Anwendungslizenzgruppe, um ein Popupmenü anzuzeigen, das die folgenden Elemente enthält.

<a href="" id="new-unlimited-license"></a>**Neue unbegrenzte Lizenz**  
Zeigt den Assistenten für neue unbegrenzte Lizenzen an. Diese Option steht nur zur Verfügung, wenn die Lizenzgruppe keine Lizenzen aufweist. Dieser Assistent besteht aus drei Seiten:

1.  Geben Sie im Feld Name der **Anwendungslizenzgruppe** einen Gruppennamen und einen Wert (in Minuten) im Feld " **Lizenzablauf Warnung** " ein. (Sie können einen beliebigen Wert von 0 bis 100 eingeben.) Sie können auch die nach-oben-und nach-unten-Taste verwenden, um die Anzahl der Minuten festzulegen.

2.  Geben Sie im Feld **Lizenzbeschreibung** den kurzen beschreibenden Text ein, und aktivieren Sie das Kontrollkästchen **aktiviert** . Optional können Sie das Feld **Ablaufdatum** verwenden, um ein Ablaufdatum für die Lizenz anzugeben. Sie können das Standardkontrollkästchen aktivieren oder das Kalenderdienstprogramm verwenden, um zum gewünschten Ablaufdatum zu wechseln.

3.  Klicken Sie auf **Fertig stellen** , um die neue Lizenz hinzuzufügen.

<a href="" id="new-concurrent-license"></a>**Neue Concurrent-Lizenz**  
Zeigt den Assistenten für neue parallel Lizenzen an. Diese Option steht nur zur Verfügung, wenn die Lizenzgruppe keine unbegrenzten Lizenzen besitzt. Dieser Assistent besteht aus den folgenden Seiten und ist nahezu identisch mit dem Assistenten für neue unbegrenzte Lizenzen:

1.  Geben Sie im Feld Name der **Anwendungslizenzgruppe** einen Gruppennamen und einen Wert (in Minuten) im Feld " **Lizenzablauf Warnung** " ein. (Sie können einen beliebigen Wert von 0 bis 100 eingeben.) Sie können auch die nach-oben-und nach-unten-Taste verwenden, um die Anzahl der Minuten festzulegen.

2.  Geben Sie im Feld **Lizenzbeschreibung** einen kurzen beschreibenden Text ein, und geben Sie einen Wert in das Feld **Concurrent License Quantity** ein. Sie können auch die aufwärts-und Abwärtspfeile verwenden, um die Anzahl der gleichzeitigen Lizenzen festzulegen. Aktivieren Sie das Kontrollkästchen **aktiviert** , um die Lizenz zu aktivieren. Optional können Sie das Feld **Ablaufdatum** verwenden, um ein Ablaufdatum für die Lizenz auszuwählen. Sie können das Kontrollkästchen aktivieren, um das angezeigte Ablaufdatum zu verwenden, oder Sie können das Kalenderdienstprogramm verwenden, um zum gewünschten Ablaufdatum zu navigieren.

3.  Klicken Sie auf **Fertig stellen** , um die neuen Lizenzen hinzuzufügen.

<a href="" id="new-named-license"></a>**Neue benannte Lizenz**  
Zeigt den Assistenten für neue benannte Lizenzen an. Diese Option steht nur zur Verfügung, wenn die Lizenzgruppe keine unbegrenzten Lizenzen besitzt. Dieser Assistent besteht aus den folgenden Seiten:

1.  Geben Sie im Feld Name der **Anwendungslizenzgruppe** einen Gruppennamen und einen Wert (in Minuten) im Feld " **Lizenzablauf Warnung** " ein. (Sie können einen beliebigen Wert von 0 bis 100 eingeben.) Sie können auch die nach-oben-und nach-unten-Taste verwenden, um die Anzahl der Minuten festzulegen.

2.  Geben Sie einen kurzen beschreibenden Text in die **Lizenzbeschreibung**ein, und aktivieren Sie das Kontrollkästchen **aktiviert** . Optional können Sie das Feld **Ablaufdatum** verwenden, um ein Ablaufdatum für die Lizenz anzugeben. Sie können das Kontrollkästchen aktivieren, um das angezeigte Ablaufdatum zu verwenden, oder das Kalenderdienstprogramm verwenden, um zum gewünschten Ablaufdatum zu navigieren.

3.  Klicken Sie auf benannte Benutzer **Hinzufügen**, **Bearbeiten**oder **Entfernen** .

4.  Klicken Sie auf **Fertig stellen** , um die neue Lizenz hinzuzufügen.

<a href="" id="new-window-from-here"></a>**Neues Fenster von hier**  
Öffnet eine neue Verwaltungskonsole mit dem ausgewählten Knoten als Stammknoten.

<a href="" id="delete"></a>**Delete**  
Löscht die Lizenzgruppe aus der Liste.

<a href="" id="rename"></a>**Rename**  
Ändert den Namen der Anwendungslizenzgruppe.

<a href="" id="properties"></a>**Eigenschaften**  
Zeigt das Dialogfeld **Eigenschaften** für die ausgewählten Anwendungslizenzgruppen an. Dieses Dialogfeld enthält die folgenden Registerkarten:

-   Registerkarte **Allgemein** – zeigt allgemeine Informationen zur Lizenzgruppe an. Auf dieser Registerkarte können Sie den Zeitwert (in Minuten) im Feld " **Lizenzablauf Warnung** " ändern. Sie können einen beliebigen Wert von 0 – 100 eingeben.

-   Registerkarte **Anwendungen** – zeigt die Liste der Anwendungen an, die der Lizenzgruppe zugeordnet sind.

<a href="" id="help"></a>**Hilfe**  
Zeigt das Hilfesystem der Application Virtualization Server Management Console an.

Wenn im Bereich " **Ergebnisse** " Anwendungslizenzgruppen angezeigt werden, klicken Sie mit der rechten Maustaste auf eine beliebige Stelle im **Ergebnis** Bereich, mit Ausnahme einer Lizenzgruppe, um ein Popupmenü anzuzeigen, das die folgenden Elemente enthält.

<a href="" id="refresh"></a>**Aktualisieren**  
Aktualisiert die Ansicht des Servers.

<a href="" id="export-list"></a>**Liste exportieren**  
Erstellt eine tabstoppgetrennte Textdatei, die den Inhalt des **Ergebnis** Bereichs enthält. Dieses Element zeigt das Dialogfeld Standard **Dateispeicherung** an, in dem Sie den Speicherort für die zu erstellende Textdatei angeben.

<a href="" id="view"></a>**Ansicht**  
Ändert die Darstellung und den Inhalt des **Ergebnis** Bereichs.

<a href="" id="arrange-line-up-icons"></a>**Symbole für anordnen/ausrichten**  
Ändert, wie die Symbole im **Ergebnis** Bereich angezeigt werden.

<a href="" id="help"></a>**Hilfe**  
Zeigt das Hilfesystem für die Application Virtualization Server Management Console an.

Wenn im Bereich " **Ergebnisse** " Lizenzen angezeigt werden, klicken Sie mit der rechten Maustaste auf eine beliebige Anwendungslizenz, um ein Popupmenü anzuzeigen, das die folgenden Elemente enthält.

<a href="" id="delete"></a>**Delete**  
Löscht die Lizenz aus der Liste.

<a href="" id="rename"></a>**Rename**  
Ändert den Namen der Lizenz.

<a href="" id="properties"></a>**Eigenschaften**  
Zeigt das Dialogfeld **Eigenschaften** für die ausgewählte Anwendungslizenz an.

Die Registerkarte " **Allgemein** " im Dialogfeld " **Eigenschaften** " zeigt Informationen zur Lizenz an und ermöglicht Ihnen, den aktivierten Status, das Ablaufdatum der Lizenz und die Lizenzschlüsselinformationen zu ändern.

<a href="" id="help"></a>**Hilfe**  
Zeigt das Hilfesystem der Serververwaltungskonsole an.

Wenn im Bereich " **Ergebnisse** " Lizenzen angezeigt werden, klicken Sie mit der rechten Maustaste auf eine beliebige Stelle im **Ergebnis** Bereich, außer auf eine Lizenz, um ein Popupmenü anzuzeigen, das die folgenden Elemente enthält.

<a href="" id="export-list"></a>**Liste exportieren**  
Erstellt eine tabstoppgetrennte Textdatei, die den Inhalt des **Ergebnis** Bereichs enthält. Dieses Element zeigt das Dialogfeld Standard **Dateispeicherung** an, in dem Sie den Speicherort für die zu erstellende Textdatei angeben.

<a href="" id="view"></a>**Ansicht**  
Ändert die Darstellung und den Inhalt des **Ergebnis** Bereichs.

<a href="" id="arrange-line-up-icons"></a>**Symbole für anordnen/ausrichten**  
Ändert, wie die Symbole im **Ergebnis** Bereich angezeigt werden.

<a href="" id="properties"></a>**Eigenschaften**  
Zeigt das Dialogfeld " **Eigenschaften** " für die ausgewählte Lizenz an.

Die Registerkarte " **Allgemein** " im Dialogfeld " **Eigenschaften** " zeigt Informationen zur Lizenz an und ermöglicht Ihnen, den aktivierten Status, das Ablaufdatum der Lizenz und die Lizenzschlüsselinformationen zu ändern.

<a href="" id="help"></a>**Hilfe**  
Zeigt das Hilfesystem für die Application Virtualization Server Management Console an.

## Verwandte Themen


[Informationen zur Anwendungslizenzierung](about-application-licensing.md)

[So verwalten Sie Anwendungslizenzen in der Server Management Console](how-to-manage-application-licenses-in-the-server-management-console.md)

[Server Management Console: Knoten „Anwendungslizenzen“](server-management-console-application-licenses-node.md)

 

 





