---
title: Übersicht über Application Virtualization Sequencer Console
description: Übersicht über Application Virtualization Sequencer Console
author: dansimp
ms.assetid: 681bb40d-2937-4645-82aa-4a44775232d8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4c2f977fccaaded0309181a1d74c16b749498abb
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809208"
---
# Übersicht über Application Virtualization Sequencer Console


Der Application Virtualization (App-V)-Sequenzer erstellt Anwendungen, damit Sie in einer virtuellen Umgebung als virtuelle Anwendungen ausgeführt werden können. Nachdem eine Anwendung sequenziert wurde, kann Sie von einem App-v-Server ausgeführt werden, um auf Computern, auf denen der APP-v-Desktop Client ausgeführt wird, oder auf dem App-v-Client für Remote Desktop Dienste (ehemals Terminal Dienste) mithilfe eines Prozesses, der als Streaming bezeichnet wird. Der App-V-Sequencer überwacht den Installations-und Einrichtungsprozess für Anwendungen und zeichnet alle Informationen auf, die für die Ausführung der Anwendung in der virtuellen Umgebung erforderlich sind. Dieser Prozess bestimmt auch, welche Dateien und Konfigurationen für alle Benutzer gelten und welche Konfigurationen Benutzer anpassen können. Virtuelle Anwendungen werden auf Zielcomputern ausgeführt und haben keine Auswirkungen auf das auf dem Zielcomputer ausgeführte Betriebssystem oder auf Anwendungen, die auf dem Zielcomputer installiert sind.

## Sicherheitsüberlegungen zu Application Virtualization Sequencer


Der App-V-Sequencer führt alle Dienste, die zur Sequenzierung erkannt werden, unter Verwendung des lokalen System Kontos aus, und es werden keine Sicherheitsbeschreibungen für Dienststeuerungsanforderungen erzwungen. Wenn der Dienst mit einem anderen Benutzerkonto installiert wurde oder wenn die Sicherheitsbeschreibungen anderen Benutzergruppen bestimmte Dienstberechtigungen erteilen sollen, sollten Sie sorgfältig überlegen, ob der Dienst virtualisiert werden soll. In einigen Fällen sollten Sie den Dienst lokal installieren, um sicherzustellen, dass die vorgesehene Dienstsicherheit erhalten bleibt.

## Menü Optionen für Application Virtualization Sequencer-Konsole


Die folgenden Menüelemente stehen in der App-V Sequencer-Konsole zur Verfügung:

-   **Datei**– enthält verschiedene Befehle, mit denen Sie sequenzierte Anwendungen erstellen, öffnen, ändern und speichern können.

-   **Bearbeiten**– enthält verschiedene Befehle zum Bearbeiten vorhandener virtueller Anwendungen.

-   **Ansicht**– enthält verschiedene Befehle zum Anzeigen der Eigenschaften einer virtuellen Anwendung.

-   **Tools**– enthält verschiedene Tools und Diagnosen für die Konfiguration virtueller Anwendungen.

## Toolbar-Optionen für Application Virtualization Sequencer-Konsole


Die folgenden Symbolleistenschaltflächen sind in der App-V Sequencer-Konsole verfügbar:

-   **Neues Paket**– klicken Sie hier, um eine neue sequenzierte Anwendung zu erstellen.

-   **Öffnen**– klicken Sie auf, um ein sequenziertes Anwendungspaket in der App-V Sequencer-Konsole zu öffnen.

-   **Für Upgrade öffnen**– klicken Sie auf, um eine sequenzierte Anwendung zu öffnen, um ein Update zu aktualisieren oder anzuwenden.

-   **Speichern**– klicken Sie, um eine sequenzierte virtuelle Anwendung zu speichern.

-   **Sequenz-Assistent**– klicken Sie, um den Sequenz-Assistenten zu öffnen. Mit dieser Schaltfläche können Sie den Sequenz-Assistenten starten, wenn Sie auf der Registerkarte **Allgemein** unter **Extras**  /  **Optionen**Änderungen vornehmen.

## Registerkarten für virtuelle Anwendungen


Wenn Sie eine virtuelle Anwendung in der App-V Sequencer-Konsole anzeigen, werden die folgenden Registerkarten angezeigt:

-   **Eigenschaften**– zeigt Informationen zur ausgewählten virtuellen Anwendung an. Sie können den **Paketnamen** und die **Kommentare** aktualisieren, die der virtuellen Anwendung zugeordnet sind.

-   **Bereitstellung**– zeigt Informationen dazu an, wie auf den Zielcomputern auf die virtuelle Anwendung zugegriffen wird. Sie können die Bereitstellungsmethode für die virtuelle Anwendung konfigurieren, und Sie können konfigurieren, welche Betriebssysteme auf dem Zielcomputer ausgeführt werden müssen. Sie können auch die zugehörigen Ausgabeoptionen konfigurieren. Wenn Sie planen, dass Clients auf eine virtuelle Anwendung aus einer Datei zugreifen können, verwenden Sie das folgende Format, wenn Sie den Pfad angeben: **file://Server/Share/Path/.SFT**. Wählen Sie **Sicherheitsbeschreibungen erzwingen** aus, um die mit dem Paket während eines Upgrades verknüpfte Sicherheit beizubehalten, oder die Berechtigungen werden während des Upgrades zurückgesetzt.

-   **Protokoll ändern**– zeigt Informationen zu Updates an, die an der virtuellen Anwendung vorgenommen wurden.

-   **Dateien**– zeigt die Dateien an, die der ausgewählten virtuellen Anwendung zugeordnet sind. Sie können kleinere Änderungen an den zugehörigen Dateieigenschaften vornehmen, indem Sie die entsprechenden Felder verwenden.

-   **Virtuelle Registrierung**– zeigt die virtuelle Registrierung an, die der ausgewählten virtuellen Anwendung zugeordnet ist. Sie können Registrierungsschlüssel hinzufügen oder löschen, indem Sie mit der rechten Maustaste auf den entsprechenden Eintrag klicken.

-   **Virtuelles Datei System**– zeigt die virtuellen Dateisysteme an, die der ausgewählten virtuellen Anwendung zugeordnet sind. Auf dieser Registerkarte können Sie Dateisystemeinträge hinzufügen, löschen oder bearbeiten, indem Sie mit der rechten Maustaste auf den entsprechenden Eintrag klicken und die Option auswählen.

-   **Virtuelle Dienste**– zeigt die Dienste an, die der ausgewählten virtuellen Anwendung zugeordnet sind.

-   **OSD**– zeigt Informationen zur geöffneten Software Beschreibung (OSD) an, die der virtuellen Anwendung zugeordnet ist. Sie können die Dateien aktualisieren, die der OSD-Datei zugeordnet sind, indem Sie mit der rechten Maustaste auf den entsprechenden Eintrag klicken und die gewünschte Aktion auswählen.

## Verwandte Themen


[Application Virtualization Sequencer](application-virtualization-sequencer.md)

 

 





