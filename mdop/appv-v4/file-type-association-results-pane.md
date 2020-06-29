---
title: Bereich "Ergebnisse" von "Dateitypzuordnung"
description: Bereich "Ergebnisse" von "Dateitypzuordnung"
author: dansimp
ms.assetid: bc5ceb48-1b9f-45d9-a770-1bac90629c76
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 73ea8e0e4145aeae309abff362a790287f19f6af
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808830"
---
# Bereich "Ergebnisse" von "Dateitypzuordnung"


Der Bereich **Datei Zuordnungs** **Ergebnisse** befindet sich eine Ebene unterhalb des **System** Bereichs in der Application Virtualization Client Management Console, und es wird eine Liste der verfügbaren Dateitypzuordnungen angezeigt. Benutzer können eine Liste der Dateitypen Erweiterungen und der Anwendungen anzeigen, denen Sie entsprechen.

Wenn Sie bestimmte Optionen für Dateitypen anzeigen möchten, klicken Sie mit der rechten Maustaste auf eine beliebige Anwendungserweiterung, um ein Popupmenü anzuzeigen, das die folgenden Elemente enthält.

<a href="" id="delete"></a>**Delete**  
Löscht die Dateinamenerweiterung aus der Liste und entfernt die Zuordnung zum Dateityp.

<a href="" id="properties"></a>**Eigenschaften**  
Zeigt das Dialogfeld **Eigenschaften** für die ausgewählte Anwendungserweiterung an. Dieses Dialogfeld enthält zwei Registerkarten:

-   Auf der Registerkarte **Allgemein** werden allgemeine Informationen zur Dateitypzuordnung angezeigt, einschließlich des Anwendungssymbols und des Namens:

    -   **Symbol**– zeigt das ausgewählte Symbol für den zugehörigen Dateityp an.

    -   **Zuordnungsname**: zeigt den Namen des Dateityps an.

    -   **Symbol "ändern**" – klicken Sie auf diese Schaltfläche, um das Symbol für die Dateitypzuordnung zu ändern.

    -   **Erweiterung**– zeigt die Erweiterungen oder Erweiterungen an, die einem bestimmten Dateityp zugeordnet sind.

    -   **Verknüpfung aufheben**: diese Schaltfläche ist aktiviert, wenn einer Anwendung mehr als eine Erweiterung zugeordnet ist. Klicken Sie auf **Verknüpfung aufheben** , um die Dateinamenerweiterung getrennt von der Erweiterung zu verwalten, mit der Sie derzeit verknüpft ist.

    -   **Angegebene Anwendung**– wählen Sie dieses Optionsfeld aus, und wählen Sie in der Dropdownliste der verfügbaren Anwendungen eine Anwendung aus. Sie ändern die Anwendung, die von der Standardaktion verwendet wird. Sie können auch suchen, um eine Anwendung zu finden, wenn Sie in der Dropdownliste nicht verfügbar ist.

    -   **OSD-Datei**– wählen Sie dieses Optionsfeld aus, und geben Sie einen Pfad zu einer OSD-Datei (Open Software Descriptor) an. Sie können auch zu einer OSD-Datei navigieren.

-   Auf der Registerkarte **erweitert** werden detaillierte Informationen zur Dateitypzuordnung angezeigt:

    -   **Aktion**– zeigt eine Liste der verfügbaren Aktionen für den zugehörigen Dateityp an.

    -   **Inhaltstyp**– zeigt eine Beschreibung des Inhalts des Dateityps an. Wenn dieses Feld leer bleibt, wird es vom Client gefüllt.

    -   **Wahrgenommener Typ**– zeigt den Dateityp an. Sie können eine der Optionen in der Dropdownliste auswählen oder eigene hinzufügen.

    -   **Nach dem Download Öffnen bestätigen**– aktivieren Sie dieses Kontrollkästchen, um eine Bestätigungsmeldung anzuzeigen, nachdem eine Datei geladen wurde. Wenn dieses Kontrollkästchen aktiviert ist und Sie versuchen, eine Datei dieses Typs zu öffnen, indem Sie Sie in einen Webbrowser herunterladen, werden Sie vom Browser aufgefordert, zu überprüfen, ob Sie die Datei speichern möchten, anstatt Sie direkt im Browser ohne Bestätigung zu öffnen.

    -   **Erweiterung immer anzeigen**– aktivieren Sie dieses Kontrollkästchen, um anzugeben, dass Erweiterungen angezeigt werden sollen, auch wenn der Benutzer anfordert, dass das Systemerweiterungen für bekannte Dateitypen ausblenden soll.

    -   **Zu neuem Menü hinzufügen**– aktivieren Sie dieses Kontrollkästchen, um anzugeben, dass die Erweiterungen oder Erweiterungen im **neuen** Kontextmenü der Shell aufgeführt werden sollen.

    -   **Für alle Benutzer übernehmen**– aktivieren Sie dieses Kontrollkästchen, um anzugeben, dass Erweiterungen für alle Benutzer verfügbar sein sollen.

<a href="" id="help"></a>**Hilfe**  
Zeigt das Hilfesystem der Client Verwaltungskonsole an.

Wenn Sie die allgemeinen Optionen für den **Ergebnis** Bereich anzeigen möchten, klicken Sie mit der rechten Maustaste auf eine beliebige Stelle im **Ergebnis** Bereich, um ein Popupmenü anzuzeigen, das die folgenden Elemente enthält.

<a href="" id="new-association"></a>**Neue Zuordnung**  
In diesem Menüelement wird der Assistent für neue Assoziationen angezeigt. Dieser Assistent besteht aus zwei Seiten:

1.  Geben Sie eine neue oder vorhandene Dateinamenerweiterung ein, und ordnen Sie die Erweiterung einem Dateityp zu:

    -   **Erweiterung**– geben Sie eine neue Dateinamenerweiterung ein. Dieses Feld ist standardmäßig leer.

    -   **Erstellen eines neuen Dateityps mit dieser Beschreibung**– wählen Sie dieses Optionsfeld aus, um eine neue Dateitypen Beschreibung in das aktive Feld einzugeben. Diese Schaltfläche ist standardmäßig aktiviert, und das aktive Feld ist leer.

    -   **Diesen Dateityp auf alle Benutzer anwenden**– aktivieren Sie dieses Kontrollkästchen, wenn diese Zuordnung für alle Benutzer Global sein soll. Dieses Kontrollkästchen ist standardmäßig nicht aktiviert.

    -   **Diese Erweiterung mit einem vorhandenen Dateityp verknüpfen**– aktivieren Sie dieses Optionsfeld, um die Erweiterung einem vorhandenen Dateityp zuzuordnen. Suchen Sie in der Dropdownliste einen Dateityp aus. Wenn Sie diese Option auswählen, wird " **weiter** " in " **Fertig stellen**" geändert.

2.  Wählen Sie die Anwendung aus, die Dateien mit der angegebenen Erweiterung öffnen soll:

    -   **Öffnen von Dateien mit der ausgewählten Anwendung**– aktivieren Sie dieses Optionsfeld, um die Datei mit einer vorhandenen Anwendung zu öffnen. Wählen Sie in der Dropdownliste der verfügbaren Anwendungen eine Anwendung aus.

    -   **Öffnen einer Datei mit der in dieser OSD-Datei beschriebenen Zuordnung**– aktivieren Sie dieses Optionsfeld, um eine OSD-Datei anzugeben, die die zum Öffnen der Datei verwendete Anwendung bestimmt. Verwenden Sie die Schaltfläche Durchsuchen, um einen vorhandenen Speicherort auszuwählen, oder geben Sie einen Pfad oder eine HTTP-formatierte URL in dieses Feld ein.

<a href="" id="refresh"></a>**Aktualisieren**  
Dieses Element aktualisiert den **Ergebnis** Bereich.

<a href="" id="export-list"></a>**Liste exportieren**  
Mit diesem Menüelement können Sie eine tabstoppgetrennte Textdatei erstellen, die den Inhalt des **Ergebnis** Bereichs enthält. Dieses Element zeigt das Dialogfeld Standard **Dateispeicherung** an, in dem Sie den Speicherort für die zu erstellende Textdatei angeben.

<a href="" id="view"></a>**Ansicht**  
In dieser Popupliste des Menüelements können Sie die Darstellung und den Inhalt des **Ergebnis** Bereichs ändern.

<a href="" id="arrange-line-up-icons"></a>**Symbole für anordnen/ausrichten**  
Diese Menüelemente können verwendet werden, um zu ändern, wie die Symbole im **Ergebnis** Bereich angezeigt werden.

<a href="" id="help"></a>**Hilfe**  
Dieses Element zeigt das Hilfesystem für die Verwaltungskonsole an.

## Verwandte Themen


[So ändern Sie das Anwendungssymbol](how-to-change-an-application-icon.md)

[Knoten „Dateitypzuordnungen“](file-type-associations-node-client.md)

[Spalten des Bereichs „Ergebnisse“ für Dateitypzuordnungen](file-type-association-results-pane-columns.md)

 

 





