---
title: So erstellen Sie eine App-V-Projektvorlage (App-V 4.6 SP1)
description: So erstellen Sie eine App-V-Projektvorlage (App-V 4.6 SP1)
author: dansimp
ms.assetid: 7e87fba2-b72a-4bc9-92b8-220e25aae99a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4e264d5c41b663bc9c450dc642e2b26297ee7ea1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807191"
---
# So erstellen Sie eine App-V-Projektvorlage (App-V 4.6 SP1)


Sie können eine App-V-Projektvorlage verwenden, um häufig verwendete Einstellungen zu speichern, die mit einem vorhandenen virtuellen Anwendungspaket verknüpft sind. Diese Einstellungen können dann angewendet werden, wenn Sie in Ihrer Umgebung neue virtuelle Anwendungspakete erstellen, die dazu beitragen können, das Erstellen von virtuellen Anwendungspaketen zu vereinfachen.

**Hinweis**  Sie können nur dann eine App-V-Projektvorlage anwenden, wenn Sie ein neues virtuelles Anwendungspaket erstellen. Das Anwenden von Projektvorlagen auf vorhandene virtuelle Anwendungspakete wird nicht unterstützt.

 

Weitere Informationen zum Anwenden einer APP-v-Projektvorlage finden Sie unter [Anwenden einer APP-v-Projektvorlage (app-v 4,6 SP1)](how-to-apply-an-app-v-project-template--app-v-46-sp1-.md).

App-v-Projektvorlagen unterscheiden sich von App-v-Anwendungs Beschleunigern, da App-v-Anwendungs Beschleuniger anwendungsspezifisch sind und App-v-Projektvorlagen auf mehrere Anwendungen angewendet werden können. Darüber hinaus können Sie keine Projektvorlage verwenden, wenn Sie ein Paket Beschleuniger zum Erstellen eines virtuellen Anwendungspakets verwenden.

Die folgenden allgemeinen Einstellungen werden mit einer App-V-Projektvorlage gespeichert:

-   **Erweiterte Überwachungsoptionen**. Ermöglicht die Ausführung von Microsoft Update während der Überwachung, rebase **. dll's**.

-   **Paket Bereitstellungseinstellungen**. Enthält **Protokoll**, **Hostname**, **Port**, **Pfad**, **Betriebssysteme**, **Sicherheitsbeschreibungen erzwingen**, **MSI erstellen**, **Paket komprimieren**.

-   **Allgemeine Optionen**. Ermöglicht es Ihnen, das **Microsoft Windows Installer-Paket (MSI) zu generieren** , die **Virtualisierung von Ereignissen zu ermöglichen**, die **Virtualisierung von Diensten zu ermöglichen**, **die Paket Version an filename anzufügen**.

-   **Ausschlusselemente**. Enthält die Ausschlussmuster Liste.

**So erstellen Sie eine Projektvorlage**

1.  Klicken Sie zum Starten des App-v-Sequencers auf dem Computer, auf dem der APP-v-Sequenzer ausgeführt wird, auf **Start**  /  **Alle Programme**starten  /  **Microsoft Application Virtualization**  /  **Microsoft Application Virtualization Sequencer**.

2.  Wenn das virtuelle Anwendungspaket zurzeit im App-V-Sequenzer geöffnet ist, fahren Sie mit Schritt 3 dieses Verfahrens fort. Zum Öffnen des vorhandenen virtuellen Anwendungspakets, das die Einstellungen enthält, die Sie mit der App-V-Projektvorlage speichern möchten, klicken Sie auf **Datei**  /  **Öffnen** , und klicken Sie auf **Paket** **Bearbeiten** . Klicken Sie auf der Seite **Paket auswählen** auf **Durchsuchen** , und suchen Sie nach dem virtuellen Anwendungspaket, das Sie öffnen möchten. Klicken Sie auf **Bearbeiten**.

3.  Klicken Sie in der App-V Sequencer-Konsole auf **Datei**  /  **als Vorlage speichern**. Nachdem Sie die Einstellungen überprüft haben, die mit der neuen Vorlage gespeichert werden, klicken Sie auf **OK**. Geben Sie einen Namen an, der der neuen App-V-Projektvorlage zugeordnet werden soll. Klicken Sie auf **Speichern**.

    Die neue App-V-Projektvorlage wird in dem in Schritt 3 dieser Vorgehensweise angegebenen Verzeichnis gespeichert.

## Verwandte Themen


[Aufgaben für Application Virtualization Sequencer (App-V 4.6 SP1)](tasks-for-the-application-virtualization-sequencer--app-v-46-sp1-.md)

[So wenden Sie eine App-V-Projektvorlage (App-V 4.6 SP1) an](how-to-apply-an-app-v-project-template--app-v-46-sp1-.md)

 

 





