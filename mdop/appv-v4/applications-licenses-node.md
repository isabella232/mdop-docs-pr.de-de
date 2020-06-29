---
title: Knoten „Anwendungslizenzen“
description: Knoten „Anwendungslizenzen“
author: dansimp
ms.assetid: 2b8752ff-aa56-483e-b844-966941af2d94
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 720de1860e72ae2c71298f93e9b346afd66da569
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807936"
---
# Knoten „Anwendungslizenzen“


Der Knoten Anwendungs **Lizenzen** befindet sich eine Ebene unterhalb des Knotens Application Virtualization System im **Bereich** Bereich der Application Virtualization Server-Verwaltungskonsole. Wenn Sie diesen Knoten auswählen, wird im **Ergebnis** Bereich eine Liste der Lizenzen und Lizenzgruppen angezeigt. Die folgenden Lizenztypen sind verfügbar:

-   **Unbegrenzte Lizenz**– bietet Zugriff für eine beliebige Anzahl von gleichzeitigen Benutzern. Diese Lizenzierungsmethode ist geeignet, wenn Sie einer Anwendung eine unternehmensweite Lizenz zuweisen möchten.

-   **Concurrent License**– ermöglicht Ihnen, die maximale Anzahl von gleichzeitigen Benutzern zu definieren, die die Anwendung verwenden dürfen.

-   **Benannte Lizenz**– ermöglicht Ihnen, einem einzelnen Benutzer eine Lizenz zuzuweisen. Eine benannte Lizenz kann verwendet werden, um sicherzustellen, dass ein bestimmter Benutzer immer in der Lage ist, die Anwendung auszuführen.

**Hinweis**  Sie können gleichzeitige und benannte Lizenzen für dieselbe Anwendung kombinieren.

 

Klicken Sie mit der rechten Maustaste auf den Knoten **Anwendungslizenzen** , um ein Popupmenü anzuzeigen, das die folgenden Elemente enthält.

<a href="" id="new-unlimited-license"></a>**Neue unbegrenzte Lizenz**  
Zeigt den Assistenten für neue unbegrenzte Lizenzen an. Dieser Assistent besteht aus den folgenden Seiten:

1.  Geben Sie im Feld **Name der Anwendungslizenzgruppe** den Namen der Lizenzgruppe ein, und geben Sie einen Wert (in Minuten) im Feld " **Lizenzablauf Warnung** " ein. (Sie können einen beliebigen Wert von 0 bis 100 eingeben.) Sie können auch die nach-oben-und nach-unten-Taste verwenden, um die Anzahl der Minuten festzulegen.

2.  Geben Sie im Feld **Lizenzbeschreibung** den kurzen beschreibenden Text ein, und aktivieren Sie das Kontrollkästchen **aktiviert** , um die Lizenz zu aktivieren.

    Optional können Sie das Feld **Ablaufdatum** verwenden, um ein Ablaufdatum für die Lizenz anzugeben. Sie können das Kontrollkästchen aktivieren, um das angezeigte Ablaufdatum zu verwenden, oder Sie können das Kalenderdienstprogramm verwenden, um zum gewünschten Ablaufdatum zu navigieren.

3.  Klicken Sie auf **Fertig stellen** , um die neue Lizenz hinzuzufügen.

<a href="" id="new-concurrent-license"></a>**Neue Concurrent-Lizenz**  
Zeigt den Assistenten für neue parallel Lizenzen an. Dieser Assistent besteht aus den folgenden drei Seiten und ist nahezu identisch mit dem Assistenten für neue unbegrenzte Lizenzen:

1.  Geben Sie im Feld **Name der Anwendungslizenzgruppe** den Namen der Lizenzgruppe ein, und geben Sie einen Wert (in Minuten) im Feld " **Lizenzablauf Warnung** " ein. (Sie können einen beliebigen Wert von 0 bis 100 eingeben.) Sie können auch die nach-oben-und nach-unten-Taste verwenden, um die Anzahl der Minuten festzulegen.

2.  Geben Sie im Feld **Lizenzbeschreibung** einen kurzen beschreibenden Text ein, und geben Sie einen Wert in das Feld **Concurrent License Quantity** ein.

    Sie können auch die aufwärts-und Abwärtspfeile verwenden, um die Anzahl der gleichzeitigen Lizenzen festzulegen. Aktivieren Sie das Kontrollkästchen **aktiviert** , um die Lizenz zu aktivieren.

    Optional können Sie das Feld **Ablaufdatum** verwenden, um ein Ablaufdatum für die Lizenz anzugeben. Sie können das Kontrollkästchen aktivieren, um das angezeigte Ablaufdatum zu verwenden, oder Sie können das Kalenderdienstprogramm verwenden, um zum gewünschten Ablaufdatum zu navigieren.

3.  Klicken Sie auf **Fertig stellen** , um die neuen Lizenzen hinzuzufügen.

<a href="" id="new-named-license"></a>**Neue benannte Lizenz**  
Zeigt den Assistenten für neue benannte Lizenzen an. Dieser Assistent besteht aus den folgenden vier Seiten:

1.  Geben Sie im Feld **Name der Anwendungslizenzgruppe** den Namen der Lizenzgruppe ein, und geben Sie einen Wert (in Minuten) im Feld " **Lizenzablauf Warnung** " ein. (Sie können einen beliebigen Wert von 0 bis 100 eingeben). Sie können auch die nach-oben-und nach-unten-Taste verwenden, um die Anzahl der Minuten festzulegen.

2.  Geben Sie im Feld **Lizenzbeschreibung** den kurzen beschreibenden Text ein, und aktivieren Sie das Kontrollkästchen **aktiviert** , um die Lizenz zu aktivieren.

    Optional können Sie das Feld **Ablaufdatum** verwenden, um ein Ablaufdatum für die Lizenz anzugeben. Sie können das Kontrollkästchen aktivieren, um das angezeigte Ablaufdatum zu verwenden, oder Sie können das Kalenderdienstprogramm verwenden, um zum gewünschten Ablaufdatum zu navigieren.

3.  Klicken Sie auf benannte Benutzer **Hinzufügen**, **Bearbeiten**oder **Entfernen** .

4.  Klicken Sie auf **Fertig stellen** , um die neue Lizenz hinzuzufügen.

<a href="" id="view"></a>**Ansicht**  
Ändert die Darstellung und den Inhalt des **Ergebnis** Bereichs.

<a href="" id="new-window-from-here"></a>**Neues Fenster von hier**  
Öffnet eine neue Verwaltungskonsole mit dem ausgewählten Knoten als Stammknoten.

<a href="" id="refresh"></a>**Aktualisieren**  
Aktualisiert die Ansicht des Servers.

<a href="" id="export-list"></a>**Liste exportieren**  
Erstellt eine tabstoppgetrennte Textdatei, die den Inhalt des **Ergebnis** Bereichs enthält. Dieses Element zeigt das Dialogfeld Standard **Dateispeicherung** an, in dem Sie den Speicherort für die zu erstellende Textdatei angeben.

<a href="" id="help"></a>**Hilfe**  
Zeigt das Hilfesystem für die Application Virtualization Server Management Console an.

Wenn Sie im Bereich Bereich auf eine Lizenzgruppe oder Lizenz klicken, die unter dem Knoten **Anwendungslizenzen** angezeigt wird, **stehen die folgenden** Elemente zur Verfügung.

<a href="" id="view"></a>**Ansicht**  
Ändert die Darstellung und den Inhalt des **Ergebnis** Bereichs.

<a href="" id="new-window-from-here"></a>**Neues Fenster von hier**  
Öffnet eine neue Verwaltungskonsole mit dem ausgewählten Knoten als Stammknoten.

<a href="" id="delete"></a>**Delete**  
Löscht ein Paket aus dem **Ergebnis** Bereich.

<a href="" id="rename"></a>**Rename**  
Ändert den Namen eines Pakets im **Ergebnis** Bereich.

<a href="" id="export-list"></a>**Liste exportieren**  
Erstellt eine tabstoppgetrennte Textdatei, die den Inhalt des **Ergebnis** Bereichs enthält. Dieses Element zeigt das Dialogfeld Standard **Dateispeicherung** an, in dem Sie den Speicherort für die zu erstellende Textdatei angeben.

<a href="" id="properties"></a>**Eigenschaften**  
Zeigt das Dialogfeld " **Eigenschaften** " für die ausgewählte Lizenzgruppe an. Die Registerkarte " **Allgemein** " im Dialogfeld " **Eigenschaften** " zeigt Informationen zur Lizenzgruppe an und ermöglicht Ihnen, den Zeitwert im Warnungsfeld " **Lizenzablauf** " zu ändern. Auf der Registerkarte **Anwendungen** wird die Liste der Anwendungen angezeigt, die der Lizenzgruppe zugeordnet sind.

<a href="" id="help"></a>**Hilfe**  
Zeigt das Hilfesystem für die Application Virtualization Server Management Console an.

## Verwandte Themen


[Informationen zur Anwendungslizenzierung](about-application-licensing.md)

[So verwalten Sie Anwendungslizenzen in der Server Management Console](how-to-manage-application-licenses-in-the-server-management-console.md)

[Server Management Console: Knoten „Anwendungslizenzen“](server-management-console-application-licenses-node.md)

 

 





