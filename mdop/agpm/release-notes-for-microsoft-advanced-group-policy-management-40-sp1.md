---
title: Versionshinweise für Microsoft Advanced Group Policy Management 4.0 SP1
description: Versionshinweise für Microsoft Advanced Group Policy Management 4.0 SP1
author: dansimp
ms.assetid: 91835bf8-e53c-4202-986e-8d37050d1267
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: ff9ce0405df766aef9b30e67d07ceb579c4fa89f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807544"
---
# Versionshinweise für Microsoft Advanced Group Policy Management 4.0 SP1


Drücken Sie STRG + F, um diese Versionshinweise zu durchsuchen.

Lesen Sie diese Versionshinweise gründlich, bevor Sie Microsoft Advanced Group Policy Management (AGPM) 4,0 SP1 installieren. Diese Versionshinweise enthalten Informationen, die erforderlich sind, um AGPM 4,0 SP1 erfolgreich zu installieren und Informationen zu enthalten, die in der Produktdokumentation nicht zur Verfügung stehen. Wenn es einen Unterschied zwischen diesen Versionshinweisen und anderer AGPM-Dokumentation gibt, sollte die neueste Änderung als autorisierend angesehen werden. Diese Versionshinweise ersetzen die Inhalte, die in diesem Produkt enthalten sind.

## Bekannte Probleme mit AGPM 4,0 SP1


Dieser Abschnitt enthält Anmerkungen zu dieser Version von AGPM 4,0 SP1.

### <a href="" id="control-panel-s--uninstall--tool-may-not-work-when-you-try-to-change-agpm-server-settings"></a>Das Tool "deinstallieren" der Systemsteuerung funktioniert möglicherweise nicht, wenn Sie versuchen, AGPM-Server Einstellungen zu ändern.

Das Tool in der Systemsteuerung, mit dem Sie ein Programm deinstallieren oder ändern können, funktioniert möglicherweise nicht, wenn Sie versuchen, AGPM-Servereinstellungen zu ändern.

Problemumgehung: Erstellen Sie eine Kopie des AGPM-Archivordners, bevor Sie versuchen, AGPM-Servereinstellungen mithilfe der Systemsteuerung zu ändern. Anschließend können Sie Setup.exe verwenden, um den AGPM-Server erneut zu installieren und die gewünschten Konfigurationsparameter auszuwählen.

### In Berichten werden die Links, die einem Gruppenrichtlinienobjekt hinzugefügt wurden, nicht angezeigt.

Die AGPM-Einstellungen und-Differenz Berichte zeigen nicht die Links an, die einem Gruppenrichtlinienobjekt (Group Policy Object, GPO) hinzugefügt wurden.

Problemumgehung: Wenn Sie die Links in den Berichten anzeigen möchten, wählen Sie das Gruppenrichtlinienobjekt in der Gruppenrichtlinien-Verwaltungskonsole (Group Policy Management Console, GPMC) aus, und klicken Sie im rechten Bereich auf die Registerkarte **Einstellungen** .

### <a href="" id="reports-do-not-display-all--choice-options-properties--settings"></a>In den Berichten werden nicht alle Einstellungen für "Auswahloptionen" angezeigt

Die AGPM-Einstellungen und-Differenz Berichte zeigen nicht alle Einstellungen an, die im Eigenschaftenfenster der Auswahloptionen im Gruppenrichtlinienobjekt-Editor ausgewählt wurden.

Problemumgehung: Verwenden Sie die GPMC, um die ausgewählten Eigenschafteneinstellungen für Auswahloptionen in den Berichten anzuzeigen.

### In bestimmten Browsern werden in Berichten die Registerkarten "einblenden" und "ausblenden" nicht angezeigt

Die Registerkarten "einblenden" und "ausblenden" werden auf der rechten Seite der AGPM-Einstellungen und-Differenz Berichte nicht angezeigt, wenn Sie die Berichte in Google Chrome oder Mozilla Firefox anzeigen.

Problemumgehung: Anzeigen der Berichte mithilfe von Internet Explorer.

### AGPM-Einstellungen und Unterschiedsberichte können unterschiedliche Inhalte aus GPMC-Berichten anzeigen.

Die AGPM-Einstellungen und-Differenz Berichte zeigen möglicherweise nicht denselben Inhalt wie Berichte in der Gruppenrichtlinien-Verwaltungskonsole (Group Policy Management Console, GPMC) an.

Problemumgehung: Verwenden Sie die GPMC, um die AGPM-Berichte anzuzeigen.

### AGPM-Dienst wird nicht gestartet, wenn der Domänencontroller nicht online ist

Wenn der AGPM-Dienst auf einem Domänencontroller unter Windows 8 installiert ist, wird der Dienst nicht gestartet, wenn der Domänencontroller nicht online ist.

Problemumgehung: Starten Sie den AGPM-Dienst manuell, nachdem der Domänencontroller online ist.

### Das Upgrade des AGPM-Servers auf AGPM 4,0 SP1 wird blockiert, wenn Sie ein Upgrade von der AGPM 4,0-Version und dem Hotfix durchführen.

Wenn Sie versuchen, den AGPM-Server auf AGPM 4,0 zu aktualisieren. SP1 nachdem Sie AGPM 4,0 installiert und dann den AGPM-Hotfix installiert haben (siehe Knowledge Base-Artikel [2643502](https://go.microsoft.com/fwlink/?LinkId=254474)), schlägt die Aktualisierung fehl und kann nicht abgeschlossen werden.

Problemumgehung: Deinstallieren Sie den AGPM 4,0-Server, und installieren Sie dann AGPM 4,0 SP1.

### In Berichten werden keine Organisations Einheits Verknüpfungen angezeigt

Wenn Sie ein nicht gesteuertes Gruppenrichtlinienobjekt mit einer Organisationseinheit verknüpfen und dann das Gruppenrichtlinienobjekt mithilfe von AGPM steuern, werden in den AGPM-Einstellungen und-Unterschiedsberichten die Links für die Organisationseinheit nicht angezeigt.

Problemumgehung: Klicken Sie auf der Registerkarte **gesteuert** des Knotens **Einstellungen ändern** mit der rechten Maustaste auf das Gruppenrichtlinienobjekt, klicken Sie auf **Einstellungen** , und klicken Sie dann auf **GPO-Links** , um die Organisations Verknüpfungen anzuzeigen. Sie können auch die GPMC verwenden, um die Links zu einem GPO über die Registerkarte **Bereich** anzuzeigen.

## Verwandte Themen


[Advanced Group Policy Management](index.md)

[Neuigkeiten in AGPM 4.0 SP1](whats-new-in-agpm-40-sp1.md)

 

 





