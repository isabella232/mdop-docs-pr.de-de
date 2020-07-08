---
title: Bereich „Ergebnisse“ von „Anwendungen“
description: Bereich „Ergebnisse“ von „Anwendungen“
author: dansimp
ms.assetid: 977a4d35-5344-41fa-af66-14957b38ed47
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1cdabaeee0b9aaa1c96b6ae732ae4bb5b6d63ef3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807928"
---
# Bereich „Ergebnisse“ von „Anwendungen“


Der Bereich "Anwendungs **Ergebnisse** " in der Application Virtualization Client Management Console zeigt eine Liste der verfügbaren Anwendungen an. Benutzer können eine Liste der Anwendungen sehen, für die Ihnen Zugriffsrechte gewährt wurden.

Weitere Informationen zu den Verfahren, die Sie in diesem Bereich ausführen können, finden Sie unter [Verwalten von Anwendungen in der Client Verwaltungskonsole](how-to-manage-applications-in-the-client-management-console.md).

Klicken Sie mit der rechten Maustaste auf eine beliebige Anwendung, um ein Popupmenü anzuzeigen, das die folgenden Elemente enthält.

<a href="" id="new-shortcut"></a>**Neue Verknüpfung**  
In diesem Menüelement wird der Assistent für neue Tastenkombinationen angezeigt. Dieser Assistent besteht aus drei Seiten:

1.  Wählen Sie ein Symbol aus, und geben Sie einen Namen für die Verknüpfung an:

    1.  **Symbol "ändern"**– zeigt einen Standardbrowser für Windows-Symbole an. Navigieren Sie zu dem gewünschten Symbol, und wählen Sie es aus.

    2.  **Verknüpfungs Titel**– geben Sie den Namen ein, dem Sie die Tastenkombination zuweisen möchten. In diesem Feld wird standardmäßig der vorhandene Name und die Version der Anwendung verwendet.

2.  Ermitteln Sie den Speicherort der veröffentlichten Verknüpfung.

    1.  **Speicherort der Verknüpfung**– wählen Sie einen Speicherort aus, indem Sie eines der Kontrollkästchen aktivieren. Die verfügbaren Speicherorte sind **Desktop**, **Schnellstartleiste**, **Menü "Senden an"** **, Startmenü**und **ein anderer Speicherort**.

    2.  **Programme im Menü "Start"**– Wenn Sie das Kontrollkästchen **"Start"** aktivieren, wird dieses Feld aktiviert. Lassen Sie dieses Feld leer, um die Verknüpfung direkt im Stammverzeichnis des Ordners Programme zu veröffentlichen, oder geben Sie einen Ordnernamen oder eine Hierarchie ein, beispielsweise "meine \ _Computer \\office-Anwendungen". Auf diese Weise erstellte Tastenkombinationen stehen nur für den aktuellen Benutzer zur Verfügung.

    3.  **Ein anderer Speicherort** und die Schaltfläche "Durchsuchen" – Wenn Sie das Kontrollkästchen " **anderer Speicherort** " aktivieren, wird dieses Feld aktiviert. Geben Sie einen beliebigen gültigen Speicherort auf dem Computer oder einen beliebigen verfügbaren UNC-Pfad (Universal Naming Convention) (freigegebene Datei oder Verzeichnis in einem Netzwerk) ein. Die Schaltfläche "Durchsuchen" zeigt das Dialogfeld "Windows-Standard **Datei öffnen** " an.

3.  Geben Sie die gewünschten Befehlszeilenparameter ein, und klicken Sie dann auf **Fertig stellen** , um den Assistenten zu beenden.

<a href="" id="new-association"></a>**Neue Zuordnung**  
In diesem Menüelement wird der Assistent für neue Assoziationen angezeigt. Dieser Assistent besteht aus zwei Seiten:

1.  Geben Sie eine Dateinamenerweiterung ein, und ordnen Sie die Erweiterung einem Dateityp zu.

    1.  **Erweiterung**– geben Sie eine Dateinamenerweiterung ein. Dieses Feld ist standardmäßig leer.

    2.  **Erstellen eines neuen Dateityps mit dieser Beschreibung**– wählen Sie dieses Optionsfeld aus, um eine neue Dateitypen Beschreibung in das aktive Feld einzugeben. Diese Schaltfläche ist standardmäßig aktiviert, und das aktive Feld ist leer.

    3.  **Diesen Dateityp auf alle Benutzer anwenden**– aktivieren Sie dieses Kontrollkästchen, wenn diese Zuordnung für alle Benutzer Global sein soll. Dieses Kontrollkästchen ist standardmäßig nicht aktiviert.

    4.  **Diese Erweiterung mit einem vorhandenen Dateityp verknüpfen**– aktivieren Sie dieses Optionsfeld, um die Erweiterung einem vorhandenen Dateityp zuzuordnen. Wählen Sie in der Dropdownliste den gewünschten Dateityp aus. Wenn Sie diese Option auswählen, wird " **weiter** " in " **Fertig stellen**" geändert.

2.  Wählen Sie die Anwendung aus, die Dateien mit der angegebenen Erweiterung öffnen soll:

    1.  **Öffnen von Dateien mit der ausgewählten Anwendung**– aktivieren Sie dieses Optionsfeld, um die Datei mit einer vorhandenen Anwendung zu öffnen. Wählen Sie in der Dropdownliste der verfügbaren Anwendungen eine Anwendung aus.

    2.  **Öffnen einer Datei mit der in dieser OSD-Datei beschriebenen Zuordnung**– aktivieren Sie dieses Optionsfeld, um eine OSD-Datei (Open Software Descriptor) anzugeben, die die zum Öffnen der Datei verwendete Anwendung bestimmt. Verwenden Sie die Schaltfläche Durchsuchen, um einen vorhandenen Speicherort auszuwählen, oder geben Sie einen Pfad oder eine HTTP-formatierte URL in dieses Feld ein.

<a href="" id="repair"></a>**Repair**  
Setzt die Standardeinstellungen der Anwendung zurück und beseitigt alle benutzerdefinierten Einstellungen für die ausgewählte Anwendung.

<a href="" id="load-or-unload"></a>**Laden** oder **entladen**  
Lädt oder entlädt die ausgewählte Anwendung in den Cache. Dieser Befehl steht nicht zur Verfügung, wenn sich 100% der Anwendung im Cache befinden.

<a href="" id="clear"></a>**Clear**  
Entfernt die Einstellungen, Verknüpfungen und Dateitypzuordnungen des Benutzers für die ausgewählte Anwendung. Dieses Element ist nicht verfügbar, wenn ein Benutzer eine Anwendung aus einer Suite von Anwendungen ausführt. Zeigt eine Bestätigungsaufforderung an.

<a href="" id="lock-or-unlock"></a>**Sperren** oder **entsperren**  
Sperrt oder entsperrt eine Anwendung im Cache. Wenn eine Anwendung gesperrt ist, kann Sie nicht gelöscht oder überschrieben werden.

<a href="" id="import"></a>**Import**  
Importiert eine Anwendung direkt aus diesem Befehl im Knoten **Applications** in den Cache.

<a href="" id="delete"></a>**Delete**  
Löscht eine Anwendung aus dem **Ergebnis** Bereich und vom Computer und löscht die Anwendung aus dem Cache.

<a href="" id="refresh"></a>**Aktualisieren**  
Aktualisiert den Inhalt des Bereichs **Ergebnisse** .

<a href="" id="properties"></a>**Eigenschaften**  
Zeigt das Dialogfeld " **Eigenschaften** " für die ausgewählte Anwendung an. Dieses Dialogfeld enthält zwei Registerkarten:

1.  Auf der Registerkarte **Allgemein** werden das Anwendungssymbol und der Name, der Speicherort, an dem die Anwendung gestreamt wurde, und der Pfad zur lokalen OSD-Datei angezeigt. Auf dieser Registerkarte können Sie das Symbol für die Anwendung ändern, oder Sie können die Einstellungen löschen (wodurch die Verknüpfungen und die Dateitypzuordnungen entfernt werden).

2.  Auf der Registerkarte " **Paket** " werden Informationen zum Anwendungspaket angezeigt, und Sie können Anwendungen **Sperren**, **entsperren**, **Laden**, **entladen**und **importieren** .

<a href="" id="help"></a>**Hilfe**  
Zeigt das Hilfesystem der Client Verwaltungskonsole an.

## Anzeigen allgemeiner Optionen für den Ergebnisbereich


Klicken Sie mit der rechten Maustaste auf eine beliebige Stelle im **Ergebnis** Bereich, um ein Popupmenü anzuzeigen, das die folgenden Elemente enthält.

<a href="" id="new-application"></a>**Neue Anwendung**  
In diesem Menüelement wird der Assistent für neue Anwendungen angezeigt. Dieser Assistent besteht aus einer Seite, auf der Sie ein Symbol für die Anwendung auswählen und eine URL oder einen Pfad zur OSD-Datei durchsuchen oder eingeben können:

1.  **Symbol "ändern"**– zeigt einen Standardbrowser für Windows-Symbole an. Navigieren Sie zu dem gewünschten Symbol, und wählen Sie es aus.

2.  **OSD**-Dateipfad oder-URL: Geben Sie einen lokalen absoluten Pfad, einen vollständigen UNC-Pfad oder eine HTTP-URL ein.

3.  **... (Schaltfläche "Durchsuchen")** – Zeigt das Windows-Standarddialogfeld " **Datei öffnen** " an. Navigieren Sie zu der gewünschten Datei.

<a href="" id="refresh"></a>**Aktualisieren**  
Aktualisiert den Bereich **Ergebnisse** .

<a href="" id="export-list"></a>**Liste exportieren**  
Mit diesem Menüelement können Sie eine tabstoppgetrennte Textdatei erstellen, die den Inhalt des **Ergebnis** Bereichs enthält. Dieses Element zeigt das Dialogfeld Standard **Dateispeicherung** an, in dem Sie den Speicherort für die zu erstellende Textdatei angeben.

<a href="" id="view"></a>**Ansicht**  
In dieser Popupliste mit Menüelementen können Sie die Darstellung und den Inhalt des **Ergebnis** Bereichs ändern.

<a href="" id="arrange-line-up-icons"></a>**Symbole für anordnen/ausrichten**  
Diese Menüelemente können verwendet werden, um zu ändern, wie die Symbole im **Ergebnis** Bereich angezeigt werden.

<a href="" id="help"></a>**Hilfe**  
Zeigt das Hilfesystem für die Verwaltungskonsole an.

## Verwandte Themen


[Anwendungsknoten](applications-node.md)

[Spalten des Bereichs „Ergebnisse“ von „Anwendungen“](applications-results-pane-columns.md)

[Referenz zur Application Virtualization Client Management Console](application-virtualization-client-management-console-reference.md)

[So verwalten Sie Anwendungen in der Client Management Console](how-to-manage-applications-in-the-client-management-console.md)

 

 





