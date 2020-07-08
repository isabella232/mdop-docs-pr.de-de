---
title: Verwalten von Konfigurationen für UE-V 2.x
description: Verwalten von Konfigurationen für UE-V 2.x
author: dansimp
ms.assetid: e2332eca-a9cd-4446-8f7c-d17058b03466
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 20d5d2942dbd805a4054a9431b237c821cbb70fe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812322"
---
# Verwalten von Konfigurationen für UE-V 2.x


Im Rahmen des Microsoft User Experience Virtualization (UE-v) 2,0, 2,1 oder 2,1 SP1-Lebenszyklus müssen Sie die Konfiguration des UE-v-Agents verwalten und auch Speicherorte für Ressourcen wie Einstellungen-Paketdateien verwalten. Möglicherweise müssen Sie andere Aufgaben ausführen, beispielsweise die Konfiguration des Unternehmenseinstellungen-Centers, um zu definieren, wie Benutzer mit UE-V interagieren. Die folgenden Themen enthalten Anleitungen für die Verwaltung dieser UE-V-Ressourcen.

## Konfigurieren von UE-V 2. x mithilfe von Gruppenrichtlinienobjekten


Sie können Gruppenrichtlinienobjekte verwenden, um die Einstellungen zu ändern, die definieren, wie UE-V die Einstellungen auf Computern synchronisiert.

[Konfigurieren von UE-V 2. x mit Gruppenrichtlinienobjekten](configuring-ue-v-2x-with-group-policy-objects-both-uevv2.md)

## Konfigurieren von UE-V 2. x mit System Center Configuration Manager 2012


Sie können SystemCenter2012 ConfigurationManager verwenden, um den UE-v-Agent mithilfe des UE-v 2-Konfigurationspakets zu verwalten.

[Konfigurieren von UE-V 2. x mit System Center Configuration Manager 2012](configuring-ue-v-2x-with-system-center-configuration-manager-2012-both-uevv2.md)

## Verwalten von UE-V 2. x mit PowerShell und WMI


UE-v bietet Windows PowerShell-Cmdlets, die Administratoren dabei helfen können, verschiedene UE-v-Aufgaben auszuführen.

[Verwalten von UE-V 2. x mit Windows PowerShell und WMI](administering-ue-v-2x-with-windows-powershell-and-wmi-both-uevv2.md)

## Konfigurieren des Unternehmenseinstellungen-Centers für UE-V 2. x


Sie können das Center für Unternehmenseinstellungen konfigurieren, das mit dem UE-v-Agent installiert wird, um zu definieren, wie Benutzer mit UE-v interagieren.

[Konfigurieren des Unternehmenseinstellungen-Centers für UE-V 2. x](configuring-the-company-settings-center-for-ue-v-2x-both-uevv2.md)

## Beispiele für Konfigurationseinstellungen für UE-V 2. x


Nachfolgend finden Sie einige Beispiele für UE-V-Konfigurationseinstellungen:

-   **Speicherpfad für Einstellungen:** Gibt den Speicherort der Dateifreigabe an, in der die UE-V-Einstellungen gespeichert sind.

-   **Katalogpfad für Einstellungs Vorlagen:** Gibt den UNC-Pfad (Universal Naming Convention) an, der den Speicherort definiert, der auf neue Einstellungen für Standort Vorlagen überprüft wurde.

-   **Microsoft-Vorlagen registrieren:** Gibt an, ob die Microsoft-Standardvorlagen während der Installation registriert werden sollen.

-   **Synchronisierungsmethode:** Gibt an, ob UE-V den Synchronisierungsanbieter oder "None" verwendet. Die "SyncProvider" unterstützt Computer, die nicht mit dem Netzwerk verbunden sind. "Keine" gilt, wenn der Computer immer mit dem Netzwerk verbunden ist. Weitere Informationen zur Synchronisierungsmethode finden Sie unter [Synchronisierungsmethoden für UE-V 2. x](sync-methods-for-ue-v-2x-both-uevv2.md).

-   **Synchronisierungs Timeout:** Gibt die Anzahl der Millisekunden an, die der Computer vor dem Timeout wartet, wenn er die Benutzereinstellungen vom Speicherort für Einstellungen abruft.

-   **Synchronisierungs Aktivierung:** Gibt an, ob die Synchronisierung der UE-V-Einstellungen aktiviert oder deaktiviert ist.

-   **Maximale Paketgröße:** Gibt die Größe des Einstellungen-Paketdatei-Schwellenwerts in Bytes an, bei dem der UE-V-Agent eine Warnung meldet.

-   **Windows-App-Einstellungen nicht synchronisieren:** Gibt an, dass UE-V keine Windows-apps synchronisieren soll.

-   **Aktivieren/Deaktivieren der ersten Verwendungs Benachrichtigung:** Gibt an, ob UE-v beim ersten Ausführen des UE-v-Agents auf dem Computer eines Benutzers ein Dialogfeld anzeigt.

-   **Aktivieren/Deaktivieren des Taskleistensymbols:** Gibt an, ob UE-V ein Symbol im Infobereich und alle zugehörigen Benachrichtigungen anzeigt. Das Symbol enthält einen Link zum Unternehmenseinstellungen-Center.

-   **Link für benutzerdefinierten Kontakt:** Definiert den Pfad, Text und die Beschreibung für den Link " **Kontakt** " im Unternehmenseinstellungen-Center.






## Verwandte Themen


[Verwalten von UE-V 2. x](administering-ue-v-2x-new-uevv2.md)

[Bereitstellen der erforderlichen Features für UE-V 2.x](deploy-required-features-for-ue-v-2x-new-uevv2.md)

[Bereitstellen von UE-V 2. x für benutzerdefinierte Anwendungen](deploy-ue-v-2x-for-custom-applications-new-uevv2.md)

 

 





