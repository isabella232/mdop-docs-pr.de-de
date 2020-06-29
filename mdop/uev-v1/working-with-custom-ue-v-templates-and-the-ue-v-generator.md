---
title: Arbeiten mit benutzerdefinierten UE-V-Vorlagen und dem UE-V-Generator
description: Arbeiten mit benutzerdefinierten UE-V-Vorlagen und dem UE-V-Generator
author: dansimp
ms.assetid: 7bb2583a-b032-4800-9bf9-eb33528e1d0d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: db5387254842bfdcf3898089bc12a8e929e3813a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810279"
---
# Arbeiten mit benutzerdefinierten UE-V-Vorlagen und dem UE-V-Generator


Um Anwendungen zwischen Benutzercomputern zu durchlaufen, verwendet Microsoft User Experience Virtualization (UE-V) *Einstellungen für Standort Vorlagen*. Einige Einstellungen für Speicherort Vorlagen sind in der Benutzeroberflächen-Virtualisierung enthalten. Sie können mit dem UE-V-Generator auch benutzerdefinierte Standort Vorlagen erstellen, bearbeiten oder überprüfen.

Der UE-V-Generator überwacht eine Anwendung, um die Speicherorte, an denen die Anwendung Ihre Einstellungen speichert, zu ermitteln und zu erfassen. Die Anwendung, die überwacht wird, muss eine herkömmliche Anwendung sein. Der UE-V-Generator kann für die folgenden Anwendungstypen keine Vorlage für eine Einstellungsposition erstellen:

-   Virtualisierte Anwendungen

-   Über die Terminaldienste angebotene Anwendung

-   Java-Anwendungen

-   Windows 8-Anwendungen

## Erstellen von UE-V-Einstellungsortvorlagen mit UE-V-Generator


Verwenden des UE-V-Generators zum Erstellen von Einstellungen für Standort Vorlagen

[Erstellen von UE-V-Einstellungsortvorlagen mit UE-V-Generator](create-ue-v-settings-location-templates-with-the-ue-v-generator.md)

## Bearbeiten von UE-V-Einstellungsortvorlagen mit dem UE-V-Generator


Verwenden des UE-V-Generators zum Bearbeiten von Einstellungen für Standort Vorlagen

[Bearbeiten von UE-V-Einstellungsortvorlagen mit dem UE-V-Generator](edit-ue-v-settings-location-templates-with-the-ue-v-generator.md)

## Überprüfen von UE-V-Einstellungsortvorlagen mit UE-V-Generator


Verwenden des UE-v-Generators zum Überprüfen von Einstellungen für Standort Vorlagen, die außerhalb des UE-v-Generators geändert wurden.

[Überprüfen von UE-V-Einstellungsortvorlagen mit UE-V-Generator](validate-ue-v-settings-location-templates-with-ue-v-generator.md)

## <a href="" id="bkmk-standardnonstandardsettingslocations"></a>Speicherorte für Standard-und nicht Standardeinstellungen


Der UE-V-Generator hilft Ihnen, zu erkennen, wo Anwendungen nach Einstellungsdateien und Registrierungseinstellungen suchen, die Anwendungen zum Speichern von Einstellungsinformationen verwenden. Sie können den UE-V-Generator verwenden, um die Anwendung als Teil des Ermittlungsprozesses zu öffnen, um die Einstellungen an Standardspeicherorten zu erfassen. Zu den Standard Speicherorten gehören die folgenden:

-   **Registrierungseinstellungen** – Registrierungsspeicherorte unter **HKEY \ _CURRENT \ _User**

-   **Anwendungseinstellungsdateien** – Dateien, die unter \ \ **Users** \ \ \ [Benutzername \] \ \ **AppData**  \\  **Roaming** gespeichert sind

Der UE-V-Generator schließt Speicherorte aus, die häufig Anwendungssoftware Dateien speichern, die zwischen Benutzercomputern oder-Umgebungen nicht gut Roaming sind. Der UE-V-Generator schließt diese Speicherorte aus. Ausgeschlossene Speicherorte sind wie folgt:

-   HKEY \ _CURRENT \ _User Registrierungsschlüssel und Dateien, für die der angemeldete Benutzer keine Werte schreiben kann

-   HKEY \ _CURRENT \ _User Registrierungsschlüssel und Dateien, die der Kernfunktionalität des Windows-Betriebssystems zugeordnet sind

-   Alle Registrierungsschlüssel, die sich im HKEY \ _LOCAL \ _MACHINE Hive befinden (Administrator Rechte erforderlich sind und möglicherweise UAC-Vereinbarung festlegen müssen)

-   Dateien, die sich in Verzeichnissen von Programmdateien befinden (erfordert Administrator Rechte und möglicherweise eine UAC-Vereinbarung festzulegen)

-   Dateien, die sich in den Benutzern befinden \ \ \ [Benutzername \] \ \ APPDATA \ \ LocalLow

-   Windows-Betriebssystemdateien, die sich in% SystemRoot% befinden (Administrator Rechte erforderlich sind und möglicherweise eine UAC-Vereinbarung festlegen müssen)

Wenn Registrierungsschlüssel und Dateien, die in diesen Speicherorten gespeichert sind, für das Roaming von Anwendungseinstellungen erforderlich sind, können Sie die ausgeschlossenen Speicherorte während des Erstellungsprozesses der Vorlage manuell zur Vorlage "Settings Location" hinzufügen.

## Weitere Ressourcen für dieses Produkt


[Vorgänge für UE-V 1.0](operations-for-ue-v-10.md)

[Verwalten von UE-V 1.0](administering-ue-v-10.md)

 

 





