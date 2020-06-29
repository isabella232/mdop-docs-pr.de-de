---
title: Planen für UE-V-Konfigurationsmethoden
description: Planen für UE-V-Konfigurationsmethoden
author: dansimp
ms.assetid: 57bce7ab-1be5-434b-9ee5-c96026bbe010
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4894644d72392ae984d0de290bf634e137d5b85e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812148"
---
# Planen für UE-V-Konfigurationsmethoden


Microsoft User Experience Virtualization (UE-V)-Konfigurationen legen fest, wie Einstellungen im gesamten Unternehmen synchronisiert werden. In diesem Thema wird beschrieben, wie UE-V-Konfigurationen erstellt werden, die Ihnen helfen, einen Konfigurationsplan zu formulieren, der Ihren geschäftlichen Anforderungen am besten entspricht.

## Konfigurationsmethoden für UE-V


Je nach verwendeter Konfigurationsmethode können Sie UE-V vor, während oder nach der Agenteninstallation konfigurieren.

**Gruppenrichtlinie:** vorhandene Gruppenrichtlinieninfrastruktur kann verwendet werden, um UE-v vor oder nach der Bereitstellung des UE-v-Agents zu konfigurieren. Die UE-v-ADMX-Vorlage ermöglicht die zentrale Verwaltung von allgemeinen UE-v-Agent-Konfigurationsoptionen und umfasst Einstellungen für die Konfiguration der UE-v-Synchronisierung. Netzwerkumgebungen, die Gruppenrichtlinien verwenden, können UE-V in Erwartung der agentenbereitstellung vorkonfigurieren.

[Konfigurieren von UE-V mit Gruppenrichtlinienobjekten](configuring-ue-v-with-group-policy-objects.md)

[Installieren der ADMX-Vorlagen für UE-V-Gruppenrichtlinien](installing-the-ue-v-group-policy-admx-templates.md)

**Befehlszeilen-oder Batch Skript Installation:** Parameter, die für die Bereitstellung des UE-v-Agents verwendet werden, ermöglichen die Konfiguration vieler UE-v-Einstellungen. Elektronische Softwareverteilungssysteme wie System Center Configuration Manager verwenden diese Parameter, um Ihre Clients beim Bereitstellen und Installieren der UE-V-Agentensoftware zu konfigurieren. Eine Liste der Installationsparameter und Beispiel Installationsskripts finden Sie unter [Bereitstellen des UE-V-Agents](deploying-the-ue-v-agent.md).

**PowerShell und WMI:** skriptgesteuerte Befehle mit PowerShell oder WMI können verwendet werden, um Konfigurationen nach der Installation des UE-V-Agents zu ändern. Eine Liste mit PowerShell-und WMI-Befehlen finden Sie unter [Verwalten des UE-V 1,0-Agents und von Paketen mit PowerShell und WMI](managing-the-ue-v-10-agent-and-packages-with-powershell-and-wmi.md).

**Bearbeiten von Registrierungseinstellungen:** UE-V-Einstellungen werden in der Registrierung gespeichert und können mithilfe eines beliebigen Tools geändert werden, mit dem Registrierungseinstellungen wie Regedit geändert werden können.

**Hinweis**  Die Änderung der Registrierung kann zu Datenverlust führen, oder der Computer reagiert nicht mehr. Wir empfehlen, dass Sie andere Konfigurationsmethoden verwenden.

 

### UE-V-Konfigurationseinstellungen

Im folgenden finden Sie Beispiele für UE-V-Konfigurationseinstellungen:

-   **Festlegen des Speicherpfads:** gibt den Speicherort der Dateifreigabe an, in der die UE-V-Einstellungen gespeichert sind.

-   **Katalogpfad für Einstellungs Vorlagen:** gibt den UNC-Pfad (Universal Naming Convention) an, der den Speicherort definiert, der auf neue Einstellungen für Standort Vorlagen überprüft wurde.

-   **Microsoft-Vorlagen registrieren:** gibt an, ob die Microsoft-Standardvorlagen während der Installation registriert werden sollen.

-   **Synchronisierungsmethode:** gibt an, ob das Feature Windows-Offlinedateien für die Offlineunterstützung verwendet wird.

-   **Synchronisierungs Timeout:** gibt die Anzahl der Millisekunden an, die der Computer vor dem Timeout abwartet, wenn die Benutzereinstellungen vom Speicherort der Einstellungen abgerufen werden.

-   **Synchronisierungs Aktivierung:** gibt an, ob die Synchronisierung der UE-V-Einstellungen aktiviert oder deaktiviert ist.

-   **Maximale Paketgröße:** gibt die Größe des Einstellungen-Paketdatei-Schwellenwerts in Bytes an, bei dem der UE-V-Agent eine Warnung meldet.

## Verwandte Themen


[Planen für UE-V 1.0](planning-for-ue-v-10.md)

[Planen der UE-V-Konfiguration](planning-for-ue-v-configuration.md)

 

 





