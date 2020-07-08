---
title: Versionshinweise für Microsoft Advanced Group Policy Management 4.0 SP2
description: Versionshinweise für Microsoft Advanced Group Policy Management 4.0 SP2
author: dansimp
ms.assetid: 0593cd11-3308-4942-bf19-8a7bb9447f01
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 736eb8d41cbb72b274a2941c60b0357bbc948c9d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808287"
---
# Versionshinweise für Microsoft Advanced Group Policy Management 4.0 SP2


Drücken Sie STRG + F, um diese Versionshinweise zu durchsuchen.

Lesen Sie diese Versionshinweise gründlich, bevor Sie Microsoft Advanced Group Policy Management (AGPM) 4.0 Service Pack2 (SP2) installieren. Diese Anmerkungen zu dieser Version enthalten Informationen, die erforderlich sind, um AGPM 4.0 SP2 erfolgreich zu installieren und Informationen zu enthalten, die in der Produktdokumentation nicht zur Verfügung stehen. Wenn es einen Unterschied zwischen diesen Versionshinweisen und anderen AGPM-Dokumentationen gibt, sollten Sie die neueste autorisierende Änderung in Frage stellen. Diese Versionshinweise ersetzen die Inhalte, die in diesem Produkt enthalten sind.

## Bekannte Probleme mit AGPM 4.0 SP2


In diesem Abschnitt werden die bekannten Probleme für AGPM 4,0 SP2 beschrieben.

### <a href="" id="control-panel-s--uninstall--tool-may-not-work-when-you-try-to-change-agpm-server-settings"></a>Das Tool "deinstallieren" der Systemsteuerung funktioniert möglicherweise nicht, wenn Sie versuchen, AGPM-Server Einstellungen zu ändern.

Das Tool in der Systemsteuerung, mit dem Sie ein Programm deinstallieren oder ändern, funktioniert möglicherweise nicht, wenn Sie versuchen, AGPM-Server Einstellungen zu ändern.

**Problemumgehung:** Bevor Sie versuchen, AGPM-Server Einstellungen mithilfe der Systemsteuerung zu ändern, erstellen Sie eine Kopie des AGPM-Archivordners. Anschließend können Sie Setup.exe verwenden, um den AGPM-Server erneut zu installieren und die gewünschten Konfigurationsparameter auszuwählen.

### In Berichten werden die Links, die einem Gruppenrichtlinienobjekt hinzugefügt wurden, nicht angezeigt.

Die AGPM-Einstellungen und-Differenz Berichte zeigen nicht die Links an, die einem Gruppenrichtlinienobjekt (Group Policy Object, GPO) hinzugefügt wurden.

**Problemumgehung:** Wenn Sie die Links in den Berichten anzeigen möchten, wählen Sie das Gruppenrichtlinienobjekt in der Gruppenrichtlinien-Verwaltungskonsole (Group Policy Management Console, GPMC) aus, und klicken Sie dann im rechten Bereich auf die Registerkarte **Einstellungen** .

### In Berichten werden nicht alle Eigenschafteneinstellungen für Auswahloptionen angezeigt

Die AGPM-Einstellungen und-Differenz Berichte zeigen nicht alle Einstellungen an, die im Eigenschaftenfenster der **Auswahloptionen** im Gruppenrichtlinienobjekt-Editor ausgewählt wurden.

**Problemumgehung:** Verwenden Sie die GPMC, um die ausgewählten Eigenschafteneinstellungen für **Auswahloptionen** in den Berichten anzuzeigen.

### In bestimmten Browsern werden die Registerkarten "einblenden" und "ausblenden" möglicherweise nicht angezeigt

Die Registerkarten " **Einblenden** " und " **Ausblenden** " auf der rechten Seite der AGPM-Einstellungen und-Differenz Berichte werden möglicherweise nicht angezeigt, wenn Sie die Berichte in Google Chrome oder Mozilla Firefox anzeigen.

**Problemumgehung:** Zeigen Sie die Berichte mithilfe des Internet Explorer-Browsers an.

### AGPM-Einstellungen und Unterschiedsberichte können unterschiedliche Inhalte aus GPMC-Berichten anzeigen.

Die AGPM-Einstellungen und-Differenz Berichte zeigen möglicherweise nicht denselben Inhalt wie Berichte in der GPMC an.

**Problemumgehung:** Verwenden Sie die GPMC, um die AGPM-Berichte anzuzeigen.

### AGPM-Dienst wird nicht gestartet, wenn der Domänencontroller offline ist

Wenn der AGPM-Dienst auf einem Domänencontroller auf den Betriebssystemen Windows® 8 oder höher installiert ist, wird der Dienst nicht gestartet, wenn der Domänencontroller offline ist.

**Problemumgehung:** Starten Sie den AGPM-Dienst manuell, nachdem der Domänencontroller online ist.

### Das Upgrade des AGPM-Servers auf AGPM 4.0 SP2 wird blockiert, wenn Sie ein Upgrade von der AGPM 4.0-Version plus HotFix1 durchführen.

Wenn Sie versuchen, den AGPM-Server auf AGPM 4,0 zu aktualisieren. SP2 nach der Installation von AGPM 4,0 Server und dem Installieren des AGPM-Hotfix namens AGPM 4,0 werden falsche Unterschiede im HTML-Bericht gemeldet (siehe Knowledge Base-Artikel [2643502](https://go.microsoft.com/fwlink/?LinkId=254474)), das Upgrade schlägt fehl, und kann nicht abgeschlossen werden.

**Problemumgehung:** Deinstallieren Sie den AGPM 4,0-Server, und installieren Sie dann AGPM 4,0 SP2.

### In Berichten werden keine Organisations Einheits Verknüpfungen angezeigt

Wenn Sie ein nicht gesteuertes Gruppenrichtlinienobjekt mit einer Organisationseinheit verknüpfen und dann das Gruppenrichtlinienobjekt mithilfe von AGPM steuern, werden in den AGPM-Einstellungen und-Unterschiedsberichten die Links für die Organisationseinheit nicht angezeigt.

**Problemumgehung:** Klicken Sie auf der Registerkarte **gesteuert** des Knotens **Einstellungen ändern** mit der rechten Maustaste auf das Gruppenrichtlinienobjekt, klicken Sie auf **Einstellungen**, und klicken Sie dann auf **GPO-Links** , um die organisatorischen Links anzuzeigen. Sie können auch die GPMC verwenden, um die Links zu einem GPO über die Registerkarte **Bereich** anzuzeigen.

### AGPM zeigt einen Fehler an, wenn Sie im Dialogfeld "AGPM-Client ändern, reparieren oder entfernen" auf die Schaltfläche "zurück" klicken

Wenn Sie in der Systemsteuerung zu **Programme und Funktionen** navigieren und dann **Microsoft Advanced Group Policy Management – Client**auswählen, zeigt AGPM einen Fehler an, wenn Sie auf **ändern** klicken und dann im Dialogfeld **AGPM-Client ändern, reparieren oder entfernen** auf die Schaltfläche **zurück** klicken.

**Problemumgehung:** Klicken Sie auf **Abbrechen** , um den Fehler zu löschen, und starten Sie den Vorgang dann erneut. Klicken Sie nicht auf die Schaltfläche **zurück** , nachdem Sie auf **ändern** geklickt haben.

### Kommentar wird im Fenster "Verlauf" nicht angezeigt, wenn die genehmigende Person ein GPO bereitstellt und einen Kommentar eingibt

Wenn ein Benutzer mit der Rolle "Bearbeiter" eine Anforderung zum Bereitstellen eines Gruppenrichtlinienobjekts übermittelt und der Benutzer, der die Rolle "genehmigende Person" hat, das Gruppenrichtlinienobjekt bereitstellt und einen Kommentar eingibt, wird der Kommentar im Fenster " **Verlauf** " nicht angezeigt.

**Problemumgehung:** Keine.

## Verwandte Themen


[Advanced Group Policy Management](index.md)

[Neuigkeiten in AGPM 4.0 SP2](whats-new-in-agpm-40-sp2.md)

 

 





