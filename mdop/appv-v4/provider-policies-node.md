---
title: Knoten „Anbieterrichtlinien“
description: Knoten „Anbieterrichtlinien“
author: dansimp
ms.assetid: 89b47076-7732-4128-93cc-8e6d5b671c8e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 221171b22471a4a8614b13023b24dd21fd571dd3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806464"
---
# Knoten „Anbieterrichtlinien“


Der Knoten **Anbieterrichtlinien** befindet sich eine Ebene unterhalb des Knotens Application Virtualization System im **Bereich** Bereich der Application Virtualization Server-Verwaltungskonsole. Wenn Sie diesen Knoten auswählen, wird im **Ergebnis** Bereich eine Liste der Anbieterrichtlinien angezeigt. Klicken Sie mit der rechten Maustaste auf den Knoten **Anbieterrichtlinien** , um ein Popupmenü anzuzeigen, das die folgenden Elemente enthält.

<a href="" id="new-provider-policy"></a>**Neue Anbieterrichtlinie**  
Zeigt den Assistenten für neue Anbieterrichtlinien an. Dieser Assistent besteht aus den folgenden Seiten:

1.  Geben Sie im Feld **Anbieterrichtlinien Name** einen Namen ein. Aktivieren Sie das Kontrollkästchen **Clientdesktop mithilfe der Verwaltungskonsole verwalten** , wenn Sie diese Funktion verwenden möchten. Aktivieren Sie eines oder beide der folgenden Kontrollkästchen, wenn Sie die zugehörigen Funktionen nutzen möchten:

    -   **Aktualisieren der Veröffentlichungskonfiguration, wenn sich ein Benutzer anmeldet**

    -   **Aktualisieren Sie die Konfiguration alle**. Nachdem Sie diese Option ausgewählt haben, geben Sie eine Nummer ein, und wählen Sie die gewünschte Einheit aus dem Dropdown-Menü aus. Gültige Einträge liegen zwischen einem Mindestbetrag von **30 Minuten** und maximal **999 Tagen**.

2.  Klicken Sie auf **Hinzufügen** oder **Entfernen** , um eine Gruppenaufgabe hinzuzufügen oder zu entfernen. Verwenden Sie das Windows-Standarddialogfeld " **Durchsuchen** ", um eine Benutzergruppe zu finden.

3.  Aktivieren Sie eines der folgenden Kontrollkästchen im Dialogfeld " **Anbieter Pipeline Konfiguration** ", um das zugeordnete Feature zu aktivieren:

    -   **Authentifizierung**– wählen Sie in der Dropdownliste den Authentifizierungstyp aus.

    -   **Erzwingen der Zugriffsberechtigungseinstellungen**

    -   **Informationen zur Protokollnutzung**

    -   **Lizenzierung**– wählen Sie in der Dropdownliste ein Erzwingungs Schema aus.

4.  Klicken Sie auf **Fertig stellen** , um die neue Anbieterrichtlinie hinzuzufügen.

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

## Verwandte Themen


[Server Management Console: Knoten „Anbieterrichtlinien“](server-management-console-provider-policies-node.md)

 

 





