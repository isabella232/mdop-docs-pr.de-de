---
title: So verwalten Sie virtuelle Anwendungen manuell
description: So verwalten Sie virtuelle Anwendungen manuell
author: dansimp
ms.assetid: 583c5255-d3f4-4197-85cd-2a59868d85de
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e8dd5bb9d62950ac1a03ad0ec14802d9e0ff56e8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806976"
---
# So verwalten Sie virtuelle Anwendungen manuell


Sie können die Clientverwaltungskonsole Application Virtualization (app-v) verwenden, um virtuelle Anwendungen im App-v-Desktop Client oder auf dem App-v-Client für Remote Desktop Dienste (vormals Terminal Dienste) zu verwalten. App-V-Administratoren können die folgenden Aufgaben ausführen:

## Laden oder Entladen einer App-V-Anwendung


Mit den folgenden Verfahren können Sie eine Anwendung direkt aus dem Cache im Bereich **Ergebnisse** des **Anwendungs** Knotens in der Application Virtualization Client-Verwaltungskonsole laden oder entladen. Wenn Sie diesen Knoten auswählen, wird im **Ergebnis** Bereich eine Liste der Anwendungen angezeigt.

**Hinweis**  Beim Laden oder Entladen eines Pakets werden alle Anwendungen im Paket in den Cache geladen oder daraus entfernt. Wenn Sie beim Laden eines Pakets nicht genügend Speicherplatz im Cache haben, um die Anwendungen zu laden, müssen Sie die Cachegröße erhöhen. Weitere Informationen zur Cachegröße finden Sie unter [Ändern der Cachegröße und der Laufwerkbuchstaben Bezeichnung](how-to-change-the-cache-size-and-the-drive-letter-designation.md).

 

**So laden Sie eine App-V-Anwendung**

1.  Bewegen Sie den Cursor in den **Ergebnis** Bereich, klicken Sie mit der rechten Maustaste auf die gewünschte Anwendung, und wählen Sie im Popupmenü **Laden** aus.

2.  Die Anwendung wird automatisch geladen. Der Fortschritt wird in der Spalte mit der Bezeichnung **Paket Status**nachverfolgt. Sie müssen die Ansicht aktualisieren, um festzustellen, ob die Auslastung abgeschlossen ist, oder um den Fortschritt anzuzeigen.

**So entladen Sie eine App-V-Anwendung**

1.  Bewegen Sie den Cursor in den **Ergebnis** Bereich, klicken Sie mit der rechten Maustaste auf die gewünschte Anwendung, und wählen Sie im Popupmenü **entladen** aus.

2.  Die Anwendung wird automatisch entladen, und die Spalte **Paket Status** wird aktualisiert, um die Änderung wiederzugeben.

## So löschen Sie eine App-V-Anwendung


Sie können eine Anwendung aus der Konsole direkt aus dem Bereich " **Ergebnisse** " des **Anwendungs** Knotens in der Application Virtualization Client Management Console löschen. Wenn Sie eine Anwendung löschen, entfernt das System die Einstellungen, Verknüpfungen und Dateitypzuordnungen, die der Anwendung entsprechen, und entfernt die Anwendung auch aus der Liste der Anwendungen des Benutzers.

**Hinweis**  Wenn Sie eine Anwendung von der Konsole löschen, können Sie diese Anwendung nicht mehr verwenden. Die Anwendung verbleibt jedoch im Cache und steht weiterhin anderen Benutzern im gleichen System zur Verfügung. Nach einer Veröffentlichungsaktualisierung werden die gelöschten Anwendungen wieder zur Verfügung gestellt. Wenn in einem Paket mehrere Anwendungen vorhanden sind, werden die Einstellungen des Benutzers erst entfernt, wenn alle Anwendungen gelöscht wurden.

 

**So löschen Sie eine Anwendung über die Konsole**

1.  Bewegen Sie den Cursor in den **Ergebnis** Bereich, klicken Sie mit der rechten Maustaste auf die gewünschte Anwendung, und wählen Sie im Popupmenü die Option **Löschen** aus.

2.  Klicken Sie bei der Bestätigungsaufforderung auf **Ja** , um die Anwendung zu entfernen, oder auf **Nein** , um den Vorgang abzubrechen.

## Reparieren einer App-V-Anwendung


Wenn Sie eine ausgewählte Anwendung reparieren möchten, können Sie das folgende Verfahren direkt im Bereich " **Ergebnisse** " des **Anwendungs** Knotens in der Application Virtualization Client-Verwaltungskonsole ausführen. Wenn Sie eine Anwendung reparieren, werden alle benutzerdefinierten Benutzereinstellungen entfernt und die Standardeinstellungen wiederhergestellt. Mit dieser Aktion werden keine Verknüpfungen oder Dateitypzuordnungen geändert oder gelöscht, und die Anwendung wird nicht aus dem Cache entfernt.

**So reparieren Sie eine App-V-Anwendung**

1.  Bewegen Sie den Cursor in den Bereich **Ergebnisse** .

2.  Klicken Sie mit der rechten Maustaste auf die gewünschte Anwendung, und wählen Sie dann im Popupmenü **Reparieren** aus.

3.  Klicken Sie bei der Bestätigungsaufforderung auf **Ja** , um die Anwendung zu reparieren, oder auf **Nein** , um den Vorgang abzubrechen.

## Importieren einer App-V-Anwendung


Mit dem folgenden Verfahren können Sie eine Anwendung direkt aus dem Bereich **Ergebnisse** des **Anwendungs** Knotens in der Application Virtualization Client-Verwaltungskonsole in den Cache importieren.

**So importieren Sie eine App-V-Anwendung**

1.  Bewegen Sie den Cursor in den **Ergebnis** Bereich, klicken Sie mit der rechten Maustaste auf die gewünschte Anwendung, und wählen Sie im Popupmenü **importieren** aus.

2.  Navigieren Sie im Fenster **Durchsuchen** zum Speicherort der Paketdatei für die gewünschte Anwendung, und klicken Sie dann auf **OK**.

    **Hinweis**  Wenn Sie bereits einen Such Pfad für den Import konfiguriert haben oder sich die SFT-Datei im gleichen Pfad wie der letzte erfolgreiche Import befindet, ist Schritt 2 nicht erforderlich.

     

## Sperren oder Entsperren einer App-V-Anwendung


Mit den folgenden Verfahren können Sie alle Anwendungen im Application Virtualization Desktop Client-Cache oder im Client für Remote Desktop Dienste (ehemals Terminal Dienste) sperren oder entsperren. Eine gesperrte Anwendung kann nicht aus dem Cache entfernt werden, um Platz für neue Anwendungen zu schaffen. Um eine gesperrte Anwendung aus dem Application Virtualization Desktop Client-Cache oder dem Client für Remote Desktop Dienste-Cache zu entfernen, müssen Sie Sie zuerst entsperren.

**So sperren Sie eine Anwendung**

1.  Bewegen Sie den Cursor in den Bereich **Ergebnisse** .

2.  Klicken Sie mit der rechten Maustaste auf die gewünschte Anwendung, und wählen Sie im Popupmenü die Option **Sperren** aus. Die ausgewählte Anwendung ist im Cache gesperrt.

**So entsperren Sie eine Anwendung**

1.  Bewegen Sie den Cursor in den Bereich **Ergebnisse** .

2.  Klicken Sie mit der rechten Maustaste auf die gewünschte Anwendung, und wählen Sie im Popupmenü **entsperren** aus. Die ausgewählte Anwendung wird im Cache freigegeben und kann entfernt werden.

## So löschen Sie eine App-V-Anwendung


Wenn Sie den **Anwendungs** Knoten in der Application Virtualization Client Management Console auswählen, wird im **Ergebnis** Bereich eine Liste der Anwendungen angezeigt. Sie können das folgende Verfahren verwenden, um eine Anwendung aus dem **Ergebnis** Bereich zu löschen, wodurch auch die Anwendung aus dem Cache entfernt wird.

**Hinweis**  Wenn Sie eine Anwendung löschen, steht die ausgewählte Anwendung nicht mehr für alle Benutzer dieses Clients zur Verfügung. Verknüpfungen und Dateitypzuordnungen werden ausgeblendet, und die Anwendung wird aus dem Cache gelöscht. Wenn sich eine andere Anwendung jedoch auf Daten in den Dateisystem-Cachedaten für die ausgewählte Anwendung bezieht, werden diese Elemente nicht gelöscht.

Nach einer Veröffentlichungsaktualisierung werden die gelöschten Anwendungen wieder zur Verfügung gestellt.

 

**So löschen Sie eine Anwendung**

1.  Bewegen Sie den Cursor in den **Ergebnis** Bereich, klicken Sie mit der rechten Maustaste auf die gewünschte Anwendung, und wählen Sie im Popupmenü **Löschen** aus.

2.  Klicken Sie bei der Bestätigungsaufforderung auf **Ja** , um die Anwendung zu entfernen, oder auf **Nein** , um den Vorgang abzubrechen.

## So ändern Sie ein App-V-Anwendungssymbol


Mit dem folgenden Verfahren können Sie ein Symbol, das der ausgewählten Anwendung zugeordnet ist, direkt aus dem Bereich **Ergebnisse** des **Anwendungs** Knotens in der Application Virtualization Client-Verwaltungskonsole ändern.

**So ändern Sie ein Anwendungssymbol**

1.  Bewegen Sie den Cursor in den Bereich **Ergebnisse** , und klicken Sie mit der rechten Maustaste auf die gewünschte Anwendung.

2.  Wählen Sie **Eigenschaften**aus.

3.  Klicken Sie auf der Registerkarte **Allgemein** auf **Symbol ändern**.

4.  Wählen Sie das gewünschte Symbol aus, oder navigieren Sie zu einem anderen Speicherort, um das Symbol auszuwählen. Nachdem Sie das Symbol ausgewählt haben, klicken Sie auf **OK**. Das Symbol "neu" wird im **Ergebnis** Bereich angezeigt.

## So wird es gemacht: Hinzufügen einer App-V-Anwendung


Mit dem folgenden Verfahren können Sie eine Anwendung direkt aus dem Bereich **Ergebnisse** des **Anwendungs** Knotens in der Application Virtualization Client Management Console hinzufügen.

**So fügen Sie eine Anwendung hinzu**

1.  Klicken Sie im **Ergebnis** Bereich mit der rechten Maustaste, und wählen Sie im Popupmenü die Option **neue Anwendung** aus.

2.  Auf der Seite des Assistenten können Sie die folgenden Aufgaben ausführen:

    1.  **Symbol "ändern"**– zeigt einen Standardbrowser für Windows-Symbole an. Navigieren Sie zu dem gewünschten Symbol, und wählen Sie es aus.

    2.  **OSD**-Dateipfad oder-URL: Geben Sie einen lokalen absoluten Pfad, einen vollständigen UNC-Pfad (freigegebene Datei oder ein Verzeichnis in einem Netzwerk) oder eine HTTP-URL ein.

    3.  **(Schaltfläche "Durchsuchen")**– zeigt das Windows-Standarddialogfeld " **Datei öffnen** " an. Navigieren Sie zu der gewünschten Datei.

3.  Klicken Sie auf **Fertig stellen** , um die Anwendung dem **Ergebnis** Bereich hinzuzufügen.

## Veröffentlichen einer App-V-Anwendungsverknüpfung


Mit dem folgenden Verfahren können Sie Verknüpfungen zu einer Anwendung direkt im **Ergebnis** Bereich des **Anwendungs** Knotens in der Application Virtualization Client-Verwaltungskonsole veröffentlichen.

**So veröffentlichen Sie Anwendungsverknüpfungen**

1.  Bewegen Sie den Cursor in den **Ergebnis** Bereich, klicken Sie mit der rechten Maustaste auf die gewünschte Anwendung, und wählen Sie im Popupmenü die Option **neue Verknüpfung** aus, um den Assistenten für neue Tastenkombinationen anzuzeigen.

2.  Wählen Sie auf der ersten Seite des Assistenten für neue Tastenkombinationen ein Symbol aus, und geben Sie einen Namen für die Verknüpfung an.

    1.  **Symbol "ändern"**– zeigt einen Standardbrowser für Windows-Symbole an. Navigieren Sie zu dem gewünschten Symbol, und wählen Sie es aus.

    2.  **Verknüpfungs Titel**– geben Sie den Namen ein, dem Sie die Tastenkombination zuweisen möchten. In diesem Feld wird standardmäßig der vorhandene Name und die Version der Anwendung verwendet.

3.  Ermitteln Sie auf der zweiten Seite des Assistenten den Speicherort der veröffentlichten Verknüpfung.

    1.  **Desktop**: Aktivieren Sie dieses Kontrollkästchen, um die Verknüpfung auf dem Desktop zu veröffentlichen.

    2.  **Die Schnellstartleiste**– aktivieren Sie dieses Kontrollkästchen, um die Verknüpfung auf der Schnellstartleiste zu veröffentlichen.

    3.  **Das Menü "Senden an"**: Aktivieren Sie dieses Kontrollkästchen, um die Verknüpfung im Menü **Senden an** zu veröffentlichen.

    4.  **Programme im Menü "Start"**– Wenn Sie das Kontrollkästchen **"Start"** aktivieren, wird dieses Feld aktiviert. Lassen Sie dieses Feld leer, um die Verknüpfung direkt im Stammverzeichnis des Ordners Programme zu veröffentlichen, oder geben Sie einen Ordnernamen oder eine Hierarchie ein, beispielsweise "meine \ _Computer \\office-Anwendungen". Auf diese Weise erstellte Tastenkombinationen stehen nur für den aktuellen Benutzer zur Verfügung.

    5.  **Ein anderer Speicherort** und die Schaltfläche " **Durchsuchen** " – Wenn Sie das Kontrollkästchen " **anderer Speicherort** " aktivieren, wird dieses Feld aktiviert. Geben Sie einen beliebigen gültigen Speicherort auf dem Computer oder einen beliebigen verfügbaren UNC-Pfad (freigegebene Datei oder Verzeichnis in einem Netzwerk) ein. Die Schaltfläche " **Durchsuchen** " zeigt das Dialogfeld "Windows-Standard **Datei öffnen** " an.

4.  Geben Sie auf der dritten Seite des Assistenten die gewünschten Befehlszeilenparameter ein.

5.  Klicken Sie auf **Fertig stellen** , um die Verknüpfungen zu veröffentlichen und zum Bereich **Ergebnisse** zu beenden.

## Hinzufügen einer Dateitypzuordnung für eine App-V-Anwendung


Mit dem folgenden Verfahren können Sie mithilfe des Knotens **Dateitypzuordnungen** in der Application Virtualization Client-Verwaltungskonsole eine Dateitypzuordnung hinzufügen.

**So fügen Sie eine Dateitypzuordnung hinzu**

1.  Klicken Sie mit der rechten Maustaste auf den Knoten **Dateitypzuordnungen** , und wählen Sie im Popupmenü die Option **neue Zuordnung** aus.

2.  Führen Sie den ersten Schritt des Dialogfelds aus, indem Sie die folgenden Informationen ausfüllen, und klicken Sie dann auf **weiter**:

    1.  **Erweiterung**– geben Sie eine neue Dateinamenerweiterung ein. Dieses Feld ist standardmäßig leer.

    2.  **Erstellen eines neuen Dateityps mit dieser Beschreibung**– wählen Sie dieses Optionsfeld aus, um eine neue Dateitypen Beschreibung in das aktive Feld einzugeben. Diese Schaltfläche ist standardmäßig aktiviert, und das aktive Feld ist leer.

    3.  **Diesen Dateityp auf alle Benutzer anwenden**– aktivieren Sie dieses Kontrollkästchen, wenn diese Zuordnung für alle Benutzer Global sein soll. Standardmäßig ist dieses Kontrollkästchen deaktiviert.

    4.  **Diese Erweiterung mit einem vorhandenen Dateityp verknüpfen**– aktivieren Sie dieses Optionsfeld, um die Erweiterung einem vorhandenen Dateityp zuzuordnen. Suchen Sie in der Dropdownliste einen Dateityp aus. Wenn Sie diese Option auswählen, wird " **weiter** " in " **Fertig stellen**" geändert.

3.  Führen Sie den zweiten Schritt des Dialogfelds aus, indem Sie die folgenden Informationen ausfüllen, und klicken Sie dann auf **Fertig stellen** , um zur Client Verwaltungskonsole zurückzukehren:

    1.  **Symbol "ändern**" – klicken Sie auf diese Schaltfläche, um das Anwendungssymbol zu ändern. Wählen Sie eines der verfügbaren Symbole aus, oder navigieren Sie zu einem neuen Speicherort, und wählen Sie ein Symbol aus.

    2.  **Öffnen von Dateien mit der ausgewählten Anwendung**– aktivieren Sie dieses Optionsfeld, um die Datei mit einer vorhandenen Anwendung zu öffnen. Wählen Sie in der Dropdownliste der verfügbaren Anwendungen eine Anwendung aus.

    3.  **Öffnen einer Datei mit der in dieser OSD-Datei beschriebenen Zuordnung**– aktivieren Sie dieses Optionsfeld, um eine OSD-Datei (Open Software Descriptor) anzugeben, die die zum Öffnen der Datei verwendete Anwendung bestimmt. Verwenden Sie die Schaltfläche Durchsuchen, um einen vorhandenen Speicherort auszuwählen, oder geben Sie einen Pfad oder eine HTTP-formatierte URL in dieses Feld ein.

## So löschen Sie eine Dateitypzuordnung für eine App-V-Anwendung


Sie können das folgende Verfahren verwenden, um eine Dateitypzuordnung zu löschen. Der Knoten " **Dateitypzuordnungen** " befindet sich eine Ebene unterhalb des Knotens " **Application Virtualization** " im **Bereich** Bereich. Wenn Sie diesen Knoten auswählen, wird im **Ergebnis** Bereich eine Liste der Dateitypzuordnungen angezeigt.

**So entfernen Sie eine Dateitypzuordnung**

1.  Klicken Sie im **Ergebnis** Bereich mit der rechten Maustaste auf die Erweiterung der Dateitypen Zuordnung, die Sie löschen möchten.

2.  Wählen Sie im Popupmenü **Löschen** aus.

3.  Klicken Sie auf **Ja** , um die Zuordnung zu löschen, oder klicken Sie auf **Nein** , um zum **Ergebnis** Bereich zurückzukehren.

## Verwandte Themen


[Application Virtualization Client](application-virtualization-client.md)

 

 





