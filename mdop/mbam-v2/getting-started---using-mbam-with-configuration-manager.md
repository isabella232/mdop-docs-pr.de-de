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
ms.openlocfilehash: 654de38918102a41395efe37dc593ce8f49113e4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810993"
---
# Erste Schritte – Verwenden von MBAM mit dem Konfigurations-Manager


Wenn Sie die Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) installieren, können Sie eine Topologie auswählen, die MBAM mit Configuration Manager 2007 oder SystemCenter2012 ConfigurationManager integriert. Eine Liste der unterstützten Versionen von Configuration Manager, die von MBAM unterstützt werden, finden Sie unter [Planen der Bereitstellung von MBAM mit Configuration Manager](planning-to-deploy-mbam-with-configuration-manager-2.md). In der integrierten Topologie werden die Hardware Konformitäts-und Berichterstellungsfeatures aus MBAM entfernt, und Sie können über den Configuration Manager darauf zugreifen.

**Wichtig**  Windows to go wird nicht unterstützt, wenn Sie die integrierte Topologie von MBAM mit Configuration Manager 2007 installieren.

 

## Verwenden von MBAM mit dem Konfigurations-Manager


Die Integration von MBAM basiert auf einem neuen Konfigurationspaket, das die folgenden drei Elemente in Configuration Manager 2007 oder SystemCenter2012 ConfigurationManager installiert, die in den folgenden Abschnitten ausführlich beschrieben werden:

Konfigurationsdaten, die aus Konfigurationselementen und einer Konfigurationsbasislinie bestehen

Sammlung

Berichte

### Konfigurationsdaten

Mit den Konfigurationsdaten wird eine Konfigurationsbasislinie mit dem Namen "BitLocker-Schutz" installiert, die zwei Konfigurationselemente enthält: "BitLocker-Betriebs System-Laufwerkschutz" und "BitLocker-Schutz für feste Datenlaufwerke". Die Konfigurationsbasislinie wird in der Sammlung bereitgestellt, die auch bei der Installation von MBAM erstellt wird. Die beiden Konfigurationselemente stellen die Grundlage für die Auswertung des Kompatibilitätsstatus der Clientcomputer dar. Diese Informationen werden in Configuration Manager erfasst, gespeichert und ausgewertet. Die Konfigurationselemente basieren auf den Compliance-Anforderungen für Operating System Drives (OSDs) und Fixed Data Drives (FDDs). Die erforderlichen Details für die bereitgestellten Computer werden erfasst, damit die Kompatibilität dieser Laufwerktypen ausgewertet werden kann. Standardmäßig wird der Kompatibilitätsstatus vom Konfigurations Basisplan alle 12 Stunden ausgewertet, und die Kompatibilitätsdaten werden an Configuration Manager gesendet.

### Sammlung

MBAM erstellt eine Sammlung, die als MBAM unterstützte Computer bezeichnet wird. Die Konfigurationsbasislinie richtet sich an Clientcomputer, die in dieser Sammlung enthalten sind. Hierbei handelt es sich um eine dynamische Sammlung, die standardmäßig alle 12 Stunden ausgeführt wird und die Mitgliedschaft bewertet. Die Mitgliedschaft basiert auf drei Kriterien:

-   Es handelt sich um eine unterstützte Version des Windows-Betriebssystems. Derzeit unterstützt MBAM nur Windows 7 Enterprise und Windows 7 Ultimate, Windows 8 Enterprise und Windows to go, wenn Windows to go unter Windows 8 Enterprise ausgeführt wird.

-   Es handelt sich um einen physikalischen Computer. Virtuelle Computer werden nicht unterstützt.

-   TPM (Trusted Platform Module) steht zur Verfügung. Eine kompatible Version von TPM 1,2 oder höher ist für Windows 7 erforderlich. Für Windows 8 und Windows to go ist kein TPM erforderlich.

Die Sammlung wird für alle Computer ausgewertet und erstellt die Teilmenge der kompatiblen Computer, die die Grundlage für die Kompatibilitäts Auswertung und-Berichterstellung für die MBAM-Integration bildet.

### Berichte

Es gibt vier Berichte, die Sie zum Anzeigen der Kompatibilität verwenden können. Sie lauten wie folgt:

-   **BitLocker Enterprise Compliance-Dashboard** – bietet IT-Administratoren drei verschiedene Ansichten von Informationen zu einem einzelnen Bericht: Kompatibilitätsstatus Verteilung, nicht kompatibel – Fehlerverteilung und Kompatibilitätsstatus Verteilung nach Laufwerks. Mit den Drilldown-Optionen im Bericht können IT-Administratoren durch die Daten klicken und eine Liste der Computer anzeigen, die dem von Ihnen ausgewählten Zustand entsprechen.

-   **BitLocker Enterprise Compliance Details** – ermöglicht IT-Administratoren die Anzeige von Informationen über den BitLocker-Verschlüsselungs Kompatibilitätsstatus des Unternehmens und umfasst den Kompatibilitätsstatus für jeden Computer. Mit den Drilldown-Optionen im Bericht können IT-Administratoren durch die Daten klicken und eine Liste der Computer anzeigen, die dem von Ihnen ausgewählten Zustand entsprechen.

-   **BitLocker-Computer Kompatibilität** – ermöglicht es Administratoren, einen einzelnen Computer anzuzeigen und zu ermitteln, warum er mit einem bestimmten Status kompatibel oder nicht kompatibel gemeldet wurde. Der Bericht zeigt auch den Verschlüsselungsstatus der Betriebssystemlaufwerke (OSD) und fest Netzlaufwerke (FDDs) an.

-   **BitLocker Enterprise Compliance Summary** – ermöglicht IT-Administratoren, den Status der Konformität des Unternehmens mit der MBAM-Richtlinie anzuzeigen. Der Status jedes Computers wird ausgewertet, und der Bericht zeigt eine Zusammenfassung der Konformität aller Computer im Unternehmen mit der Richtlinie. Mit den Drilldown-Optionen im Bericht können IT-Administratoren durch die Daten klicken und eine Liste der Computer anzeigen, die dem von Ihnen ausgewählten Zustand entsprechen.

## Allgemeine Architektur von MBAM mit Configuration Manager


Die folgende Abbildung zeigt die MBAM-Architektur mit der Configuration Manager-Topologie. Mit dieser Konfiguration werden bis zu 200.000 MBAM-Clients in einer Produktionsumgebung unterstützt.

![mbam-Architektur mit Configuration Manager](images/mbam2-cmserver.gif)

Eine Beschreibung der Server, Datenbanken und Features dieser Architektur folgt. Die Server Features und-Datenbanken im Architektur Bild sind unter dem Computer oder Server aufgelistet, auf dem wir die Installation empfehlen.

-   **Daten Bank Server** – die **Wiederherstellungsdatenbank**, die **Überwachungsdatenbank**und die **Überwachungsberichte** werden auf einer Windows Server-und unterstützten SQLServer-Instanz installiert. Die Wiederherstellungsdatenbank speichert Wiederherstellungsdaten, die von MBAM-Clientcomputern erfasst werden. In der Überwachungsdatenbank werden Überwachungs Aktivitätsdaten gespeichert, die von Clientcomputern erfasst werden, die auf Wiederherstellungsdaten zugreifen. Die Überwachungsberichte liefern Daten zum Kompatibilitätsstatus von Clientcomputern in Ihrem Unternehmen.

-   **Primärer Configuration Manager-Standortserver** : der Configuration Manager-Server enthält die MBAM-Server Installation mit der System Center Configuration Manager-Integrations Topologie, die auf einem primären Configuration Manager-Standortserver installiert werden muss. Der Configuration Manager-Server sammelt die Hardwareinventurinformationen von Clientcomputern und wird verwendet, um die BitLocker-Kompatibilität von Clientcomputern zu melden. Wenn Sie die Installation des MBAM-Setup Servers ausführen, werden eine Sammlung und die Konfigurationsdaten auf dem primären Configuration Manager-Standortserver installiert.

-   **Verwaltungs-und Überwachungsserver** – der **Verwaltungs-und Überwachungsserver** ist auf einem Windows-Server installiert und besteht aus der Websiteverwaltung und Überwachung sowie den Überwachungs-Webdiensten. Die Websiteverwaltung und Überwachung wird verwendet, um Aktivitäten zu überwachen und auf Wiederherstellungsdaten zuzugreifen (beispielsweise BitLocker-Wiederherstellungsschlüssel). Das **Self-Service-Portal** ist auch auf dem Administrations-und Überwachungs Server installiert. Das Portal ermöglicht Endbenutzern auf Clientcomputern die unabhängige Anmeldung bei einer Website, um einen Wiederherstellungsschlüssel abzurufen, wenn Sie Ihr BitLocker-Kennwort verlieren oder vergessen. Die Überwachungsberichte sind auch auf dem Verwaltungs-und Überwachungs Server installiert.

-   **Verwaltungsarbeitsstation** – die **Richtlinienvorlage** besteht aus Gruppenrichtlinienobjekten, die MBAM-Implementierungs Einstellungen für die BitLocker-Laufwerkverschlüsselung definieren. Sie können die Richtlinienvorlage auf einem beliebigen Server oder auf einer Arbeitsstation installieren, Sie wird jedoch häufig auf einer Verwaltungsarbeitsstation installiert, die ein unterstützter Windows-Server oder-Clientcomputer ist. Die Workstation muss kein dedizierter Computer sein.

-   **MBAM-Client** und **Configuration Manager-Client** Computer

    -   Der **MBAM-Client** führt die folgenden Aufgaben aus:

        -   Verwendet Gruppenrichtlinienobjekte, um die BitLocker-Verschlüsselung von Clientcomputern im Unternehmen durchzusetzen.

        -   Sammelt den Wiederherstellungsschlüssel für die drei BitLocker-Datenlaufwerk Typen: Betriebssystemlaufwerke, fest Netzlaufwerke und austauschbare Datenlaufwerke (USB).

        -   Sammelt Wiederherstellungsinformationen und Computer Informationen zu den Clientcomputern.

    -   **Configuration Manager-Client** – der Configuration Manager-Client ermöglicht es Configuration Manager, Hardware Kompatibilitätsdaten zu den Client Computern zu sammeln, und ermöglicht es Configuration Manager, Kompatibilitätsinformationen zu melden.

## Verwandte Themen


[Verwenden von MBAM mit dem Konfigurations-Manager](using-mbam-with-configuration-manager.md)

 

 





