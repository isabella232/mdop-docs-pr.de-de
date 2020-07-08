---
title: Knoten „Veröffentlichungsserver“
description: Knoten „Veröffentlichungsserver“
author: dansimp
ms.assetid: b5823c6c-15bc-4e8d-aeeb-acc366ffedd1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8c001e246c63919773d29a2317d5a43937c0813f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806451"
---
# Knoten „Veröffentlichungsserver“


Der Knoten **Publishing Servers** befindet sich eine Ebene unterhalb des Knotens **Application Virtualization** im **Bereich** Bereich der Application Virtualization Client-Verwaltungskonsole. Wenn Sie diesen Knoten auswählen, wird im **Ergebnis** Bereich eine Liste der Veröffentlichungsserver angezeigt.

Klicken Sie mit der rechten Maustaste auf den Knoten **Publishing Servers** , um ein Popupmenü anzuzeigen, das die folgenden Elemente enthält.

<a href="" id="new-server"></a>**Neuer Server**  
Dieses Menüelement zeigt den Assistenten für neue Server an. Dieser Assistent besteht aus zwei Seiten:

1.  Geben Sie einen Serveranzeigenamen und Servertyp ein:

    -   **Anzeigename**: Geben Sie einen Namen ein, der für den Server angezeigt werden soll. Dieses Feld ist standardmäßig leer.

    -   **Typ**– wählen Sie in der Dropdownliste der Servertypen den Servertyp aus.

2.  Geben Sie die Verbindungseinstellungen für den Server an:

    -   **Hostname**: Geben Sie den Namen oder die IP-Adresse des Servers ein.

    -   **Port**: Geben Sie einen numerischen Wert ein, der der Portnummer entspricht. Der Standardwert ist 554, wenn der Servertyp "Application Virtualization Server" und 80 ist, wenn der Servertyp "Standard-HTTP-Server" lautet.

    -   **Path**: Dieses Feld ist standardmäßig "/" und schreibgeschützt, wenn der Servertyp "Application Virtualization Server" oder "Enhanced Security Application Virtualization Server" lautet. Wenn der Servertyp "Standard-HTTP-Server" oder "Enhanced Security http Server" lautet, kann das Feld **path** ebenfalls bearbeitet werden.

<a href="" id="new-window-from-here"></a>**Neues Fenster von hier**  
Wählen Sie dieses Menüelement aus, um eine neue Verwaltungskonsole mit dem ausgewählten Knoten als Stammknoten zu öffnen.

<a href="" id="export-list"></a>**Liste exportieren**  
Mit diesem Menüelement können Sie eine tabstoppgetrennte Textdatei erstellen, die den Inhalt des **Ergebnis** Bereichs enthält. Dieses Element zeigt das Dialogfeld Standard **Dateispeicherung** an, in dem Sie den Speicherort für die zu erstellende Textdatei angeben.

<a href="" id="view"></a>**Ansicht**  
In dieser Popupliste mit Menüelementen können Sie die Darstellung und den Inhalt des **Ergebnis** Bereichs ändern.

<a href="" id="refresh"></a>**Aktualisieren**  
Wählen Sie dieses Element aus, um die Verwaltungskonsole zu aktualisieren.

<a href="" id="help"></a>**Hilfe**  
Dieses Element zeigt das Hilfesystem für die Verwaltungskonsole an.

## Verwandte Themen


[Bereich "Ergebnisse" der Veröffentlichungsserver](publishing-servers-results-pane.md)

[Spalten des Bereichs "Ergebnisse" der Veröffentlichungsserver](publishing-servers-results-pane-columns.md)

 

 





