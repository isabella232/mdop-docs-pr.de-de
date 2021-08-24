---
title: Erste Schritte – Verwenden von MBAM mit dem Konfigurations-Manager
description: Erste Schritte – Verwenden von MBAM mit dem Konfigurations-Manager
author: dansimp
ms.assetid: b0a1d3cc-0b01-4b69-a2cd-fd09fb3beda4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9f23a0eba923608fb6e25e44ee2843f3cde4c2dc
ms.sourcegitcommit: 3e0500abde44d6a09c7ac8e3caf5e25929b490a4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2021
ms.locfileid: "11910810"
---
# <a name="getting-started---using-mbam-with-configuration-manager"></a>Erste Schritte – Verwenden von MBAM mit dem Konfigurations-Manager


Wenn Sie Microsoft BitLocker Administration and Monitoring (MBAM) installieren, können Sie eine Topologie auswählen, die MBAM in Configuration Manager 2007 oder System Center 2012 Configuration Manager integriert. Eine Liste der unterstützten Versionen von Configuration Manager, die MBAM unterstützt, finden Sie unter [Planning to Deploy MBAM with Configuration Manager](planning-to-deploy-mbam-with-configuration-manager-2.md). In der integrierten Topologie werden die Hardwarecompliance- und Berichterstellungsfeatures aus MBAM entfernt und über Configuration Manager aufgerufen.

**Wichtig**  
Windows To Go wird nicht unterstützt, wenn Sie die integrierte Topologie von MBAM mit Configuration Manager 2007 installieren.

 

## <a name="using-mbam-with-configuration-manager"></a>Verwenden von MBAM mit dem Konfigurations-Manager


Die Integration von MBAM basiert auf einem neuen Configuration Pack, das die folgenden drei Elemente in Configuration Manager 2007 oder System Center 2012 Configuration Manager installiert, die in den folgenden Abschnitten ausführlich beschrieben werden:

Konfigurationsdaten, die aus Konfigurationselementen und einer Konfigurationsbaseline bestehen

Sammlung

Berichte

### <a name="configuration-data"></a>Konfigurationsdaten

Die Konfigurationsdaten installieren eine Konfigurationsbaseline namens "BitLocker Protection", die zwei Konfigurationselemente enthält: "BitLocker Operating System Drive Protection" und "BitLocker Fixed Data Drives Protection". Die Konfigurationsbasislinie wird in der Sammlung bereitgestellt, die auch bei der Installation von MBAM erstellt wird. Die beiden Konfigurationselemente bieten die Grundlage für die Bewertung des Kompatibilitätsstatus der Clientcomputer. Diese Informationen werden in Configuration Manager erfasst, gespeichert und ausgewertet. Die Konfigurationselemente basieren auf den Complianceanforderungen für Betriebssystemlaufwerke (OSDs) und Festplattenlaufwerke (Fixed Data Drives, FDDs). Die erforderlichen Details für die bereitgestellten Computer werden gesammelt, damit die Kompatibilität für diese Laufwerkstypen ausgewertet werden kann. Standardmäßig wertet der Konfigurationsbaseline den Compliancestatus alle 12 Stunden aus und sendet die Compliancedaten an Configuration Manager.

### <a name="collection"></a>Sammlung

MBAM erstellt eine Sammlung, die als MBAM-unterstützte Computer bezeichnet wird. Der Konfigurationsbaseline ist auf Clientcomputer in dieser Sammlung ausgerichtet. Dies ist eine dynamische Sammlung, die standardmäßig alle 12 Stunden ausgeführt wird und die Mitgliedschaft auswertet. Die Mitgliedschaft basiert auf drei Kriterien:

-   Es handelt sich um eine unterstützte Version des Windows Betriebssystems. Derzeit unterstützt MBAM nur Windows 7 Enterprise und Windows 7 Ultimate, Windows 8 Enterprise und Windows To Go, wenn Windows To Go auf Windows 8 Enterprise ausgeführt wird.

-   Es handelt sich um einen physischen Computer. Virtuelle Computer werden nicht unterstützt.

-   Trusted Platform Module (TPM) ist verfügbar. Für Windows 7 ist eine kompatible Version von TPM 1.2 oder höher erforderlich. Windows 8 und Windows To Go erfordern kein TPM.

Die Auflistung wird für alle Computer ausgewertet und erstellt die Teilmenge kompatibler Computer, die die Grundlage für die Compliancebewertung und Berichterstellung für die MBAM-Integration bietet.

### <a name="reports"></a>Berichte

Es gibt vier Berichte, die Sie zum Anzeigen der Compliance verwenden können. Sie lauten wie folgt:

-   **BitLocker Enterprise Compliance-Dashboard** – bietet IT-Administratoren drei verschiedene Ansichten von Informationen in einem einzigen Bericht: Compliancestatusverteilung, nicht konform – Fehlerverteilung und Compliancestatusverteilung nach Laufwerkstyp. Mithilfe von Drilldownoptionen im Bericht können IT-Administratoren durch die Daten klicken und eine Liste der Computer anzeigen, die dem von Ihnen ausgewählten Status entsprechen.

-   **BitLocker Enterprise Compliancedetails** – ermöglicht IT-Administratoren das Anzeigen von Informationen zum BitLocker-Verschlüsselungscompliancestatus des Unternehmens sowie den Compliancestatus für jeden Computer. Mithilfe von Drilldownoptionen im Bericht können IT-Administratoren durch die Daten klicken und eine Liste der Computer anzeigen, die dem von Ihnen ausgewählten Status entsprechen.

-   **BitLocker-Computercompliance** – ermöglicht IT-Administratoren, einen einzelnen Computer anzuzeigen und zu bestimmen, warum er mit einem bestimmten Status als kompatibel oder nicht kompatibel gemeldet wurde. Der Bericht zeigt auch den Verschlüsselungsstatus der Betriebssystemlaufwerke (OSD) und der Festplattenlaufwerke (Fixed Data Drives, FDDs) an.

-   **BitLocker Enterprise Compliancezusammenfassung** : Ermöglicht IT-Administratoren, den Status der Compliance des Unternehmens mit mbam-Richtlinie anzuzeigen. Jeder Computerstatus wird ausgewertet, und der Bericht enthält eine Zusammenfassung der Kompatibilität aller Computer im Unternehmen mit der Richtlinie. Mithilfe von Drilldownoptionen im Bericht können IT-Administratoren durch die Daten klicken und eine Liste der Computer anzeigen, die dem von Ihnen ausgewählten Status entsprechen.

## <a name="high-level-architecture-of-mbam-with-configuration-manager"></a>High-Level Architektur von MBAM mit Configuration Manager


Die folgende Abbildung zeigt die MBAM-Architektur mit der Configuration Manager-Topologie. Diese Konfiguration unterstützt bis zu 200.000 MBAM-Clients in einer Produktionsumgebung.

![mbam-Architektur mit Konfigurations-Manager.](images/mbam2-cmserver.gif)

Es folgt eine Beschreibung der Server, Datenbanken und Features dieser Architektur. Die Serverfeatures und Datenbanken im Architekturimage sind unter dem Computer oder Server aufgeführt, auf dem sie installiert werden sollten.

-   **Datenbankserver** **– Die Wiederherstellungsdatenbank,** **überwachungsdatenbank**und **Überwachungsberichte** werden auf einem Windows Server installiert und SQL Server Instanz unterstützt. Die Wiederherstellungsdatenbank speichert Wiederherstellungsdaten, die von MBAM-Clientcomputern gesammelt werden. Die Überwachungsdatenbank speichert Überwachungsaktivitätsdaten, die von Clientcomputern gesammelt werden, die auf Wiederherstellungsdaten zugegriffen haben. Die Überwachungsberichte enthalten Daten über den Compliancestatus von Clientcomputern in Ihrem Unternehmen.

-   **Configuration Manager Primary Site Server** – Der Configuration Manager-Server enthält die MBAM-Serverinstallation mit der System Center Configuration Manager Integrationstopologie, die auf einem primären Configuration Manager-Standortserver installiert werden muss. Der Configuration Manager-Server sammelt die Hardwareinventurinformationen von Clientcomputern und wird verwendet, um die BitLocker-Kompatibilität von Clientcomputern zu melden. Wenn Sie die Installation des MBAM-Setupservers ausführen, werden eine Sammlung und die Konfigurationsdaten auf dem primären Konfigurations-Manager-Standortserver installiert.

-   **Verwaltungs- und Überwachungsserver** – Der **Verwaltungs- und Überwachungsserver** wird auf einem Windows Server installiert und besteht aus der Verwaltungs- und Überwachungswebsite und den Überwachungsdiensten. Die Verwaltungs- und Überwachungswebsite wird verwendet, um Aktivitäten zu überwachen und auf Wiederherstellungsdaten zuzugreifen (z. B. BitLocker-Wiederherstellungsschlüssel). Das **Self-Service-Portal** wird auch auf dem Verwaltungs- und Überwachungsserver installiert. Das Portal ermöglicht Endbenutzern auf Clientcomputern die unabhängige Anmeldung bei einer Website, um einen Wiederherstellungsschlüssel zu erhalten, wenn sie ihr BitLocker-Kennwort verlieren oder vergessen. Die Überwachungsberichte werden auch auf dem Verwaltungs- und Überwachungsserver installiert.

-   **Verwaltungsarbeitsstation** : Die **Richtlinienvorlage** besteht aus Gruppenrichtlinienobjekten, die MBAM-Implementierungseinstellungen für die BitLocker-Laufwerkverschlüsselung definieren. Sie können die Richtlinienvorlage auf einem beliebigen Server oder jeder Arbeitsstation installieren, sie wird jedoch häufig auf einer Verwaltungsarbeitsstation installiert, die Windows Server oder Clientcomputer unterstützt wird. Die Arbeitsstation muss kein dedizierter Computer sein.

-   **Computer mit MBAM-Client** und **Configuration Manager-Client**

    -   Der **MBAM-Client** führt die folgenden Aufgaben aus:

        -   Verwendet Gruppenrichtlinienobjekte, um die BitLocker-Verschlüsselung von Clientcomputern im Unternehmen zu erzwingen.

        -   Erfasst den Wiederherstellungsschlüssel für die drei BitLocker-Datentypen: Betriebssystemlaufwerke, Festplattenlaufwerke und USB-Laufwerke (Wechseldaten).

        -   Sammelt Wiederherstellungsinformationen und Computerinformationen zu den Clientcomputern.

    -   **Configuration Manager-Client** – Der Configuration Manager-Client ermöglicht Configuration Manager das Sammeln von Hardwarekompatibilitätsdaten über die Clientcomputer und ermöglicht Configuration Manager die Meldung von Complianceinformationen.

## <a name="related-topics"></a>Verwandte Themen


[Verwenden von MBAM mit dem Konfigurations-Manager](using-mbam-with-configuration-manager.md)

 

 





