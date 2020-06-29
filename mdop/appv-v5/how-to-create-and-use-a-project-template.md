---
title: So erstellen und verwenden Sie eine Projektvorlage
description: So erstellen und verwenden Sie eine Projektvorlage
author: dansimp
ms.assetid: 2063f0b3-47a1-4090-bf99-0f26b107331c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e7640b9dc1e7baec194315400ee5672dfa83f394
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805594"
---
# So erstellen und verwenden Sie eine Projektvorlage


Sie können eine App-V 5,0-Projektvorlage verwenden, um häufig angewendete Einstellungen zu speichern, die mit einem vorhandenen virtuellen Anwendungspaket verknüpft sind. Diese Einstellungen können dann angewendet werden, wenn Sie neue virtuelle Anwendungspakete in Ihrer Umgebung erstellen. Die Verwendung einer Projektvorlage kann den Prozess zum Erstellen virtueller Anwendungspakete rationalisieren.

**Hinweis**  Sie können und sollten häufig eine App-V 5,0-Projektvorlage während eines Paket Upgrades anwenden. Wenn Sie beispielsweise eine Anwendung mit einer benutzerdefinierten Ausschlussliste sequenziert haben, empfiehlt es sich, eine zugeordnete Vorlage für die spätere Verwendung beim Upgrade der sequenzierten Anwendung zu erstellen und zu speichern.

App-v 5,0-Projektvorlagen unterscheiden sich von App-v 5,0-Anwendungs Beschleunigern, da App-v 5,0-Anwendungs Beschleuniger anwendungsspezifisch sind und App-v 5,0-Projektvorlagen auf mehrere Anwendungen angewendet werden können.

Gehen Sie wie folgt vor, um eine neue Vorlage zu erstellen und anzuwenden.

**So erstellen Sie eine Projektvorlage**

1.  Um den App-V 5,0-Sequenzer zu starten, klicken Sie auf dem Computer, auf dem der **Start**Sequencer ausgeführt wird, auf  /  **Alle Programme**starten  /  **Microsoft Application Virtualization**  /  **Microsoft Application Virtualization Sequencer**.

**Hinweis**  Wenn das virtuelle Anwendungspaket derzeit in der App-V 5,0-Sequenzer-Konsole geöffnet ist, fahren Sie mit Schritt 3 dieses Verfahrens fort.

2. Zum Öffnen des vorhandenen virtuellen Anwendungspakets, das die Einstellungen enthält, die Sie mit der App-V 5,0-Projektvorlage speichern möchten, klicken Sie auf **Datei**  /  **Öffnen**, und klicken Sie dann auf **Paket bearbeiten**. Klicken Sie auf der Seite **Paket auswählen** auf **Durchsuchen** , und suchen Sie nach dem virtuellen Anwendungspaket, das Sie öffnen möchten. Klicken Sie auf **Bearbeiten**.

3. Klicken Sie in der App-V 5,0-Sequenzer-Konsole auf **Datei**  /  **als Vorlage speichern**, um die Vorlagendatei zu speichern. Nachdem Sie die Einstellungen überprüft haben, die mit der neuen Vorlage gespeichert werden, klicken Sie auf **OK**. Geben Sie einen Namen an, der der neuen App-V 5,0-Projektvorlage zugeordnet werden soll. Klicken Sie auf Speichern.
   Die neue App-V 5,0-Projektvorlage wird in dem in Schritt 3 dieser Vorgehensweise angegebenen Verzeichnis gespeichert.

**So wenden Sie eine Projektvorlage an**

**Wichtig**  Das Erstellen eines virtuellen Anwendungspakets unter Verwendung einer Projektvorlage in Verbindung mit einem Paket Beschleuniger wird nicht unterstützt.

1.  Um den App-V 5,0-Sequenzer zu starten, klicken Sie auf dem Computer, auf dem der **Start**Sequencer ausgeführt wird, auf  /  **Alle Programme**starten  /  **Microsoft Application Virtualization**  /  **Microsoft Application Virtualization Sequencer**.

2.  Wenn Sie ein neues virtuelles Anwendungspaket mithilfe einer App-V 5,0-Projektvorlage erstellen oder aktualisieren möchten, klicken Sie auf **Datei**  /  **neu aus Vorlage**.

3.  Um die Projektvorlage auszuwählen, die Sie verwenden möchten, navigieren Sie zu dem Verzeichnis, in dem die Projektvorlage gespeichert ist, wählen Sie die Projektvorlage aus, und klicken Sie dann auf **Öffnen**.

    Erstellen Sie das neue virtuelle Anwendungspaket. Die mit der angegebenen Vorlage gespeicherten Einstellungen werden auf das neue virtuelle Anwendungspaket angewendet, das Sie erstellen.

    Sie **haben einen Vorschlag für App-V**? [Hier](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)können Sie Vorschläge hinzufügen oder abstimmen. **Sie haben ein App-V-Problem?** Verwenden Sie das [App-V TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Verwandte Themen


[Vorgänge für App-V 5.0](operations-for-app-v-50.md)









