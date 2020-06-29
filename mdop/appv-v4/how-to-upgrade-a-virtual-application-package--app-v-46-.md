---
title: So aktualisieren Sie ein virtuelles Anwendungspaket (App-V 4.6)
description: So aktualisieren Sie ein virtuelles Anwendungspaket (App-V 4.6)
author: dansimp
ms.assetid: 3566227e-f3dc-4c32-af1f-e0211588118c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ac722dc0e9ce1650f53d8dd22db5428d33cfcf13
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806715"
---
# So aktualisieren Sie ein virtuelles Anwendungspaket (App-V 4.6)


Gehen Sie wie folgt vor, um eine vorhandene virtuelle Anwendung mithilfe von Application Virtualization (App-V) Sequencer zu aktualisieren. Sie können auch die APP-v Sequencer-Konsole verwenden, um Änderungen an einer vorhandenen virtuellen Anwendung vorzunehmen, ohne ein Upgrade durchzuführen, aber Sie können mit dieser Methode keine Änderungen am Dateisystem der virtuellen Anwendung vornehmen, da der APP-v-Sequenzer die zugehörige SFT-Datei nicht decodiert. Weitere Informationen zum Bearbeiten eines vorhandenen Pakets finden Sie unter [so wird es gemacht: Ändern eines virtuellen Anwendungspakets (App-V 4,6)](how-to-modify-a-virtual-application-package--app-v-46-.md).

**So aktualisieren Sie eine vorhandene virtuelle Anwendung**

1.  Wenn Sie die APP-v Sequencer-Konsole starten möchten, wählen Sie auf dem Computer, auf dem der **Start**App-v-Sequencer ausgeführt wird, die Option  /  **Programme**  /  **Microsoft Application Virtualization**  /  **Microsoft Application Virtualization Sequencer**starten aus.

2.  Wenn Sie das vorhandene virtuelle Anwendungspaket öffnen und den **Sequenz-Assistenten**starten möchten, wählen Sie **Paket aktualisieren**aus. Suchen Sie das Paket, das Sie aktualisieren möchten, und klicken Sie auf **Öffnen**. Geben Sie im Dialogfeld **Ordner suchen** den Speicherort an, an dem die aktualisierte Version des Pakets gespeichert werden soll. Dieser angegebene Speicherort muss sich auf dem Laufwerk befinden, das als Application Virtualization Drive angegeben ist, in der Regel das Q:\\-Laufwerk. Wenn Sie einen neuen Ordner erstellen möchten, wählen Sie **neuen Ordner**erstellen aus.

    **Warnung**  Sie müssen den Stammordner der vorhandenen virtuellen Anwendung angeben. Erstellen Sie keinen Unterordner manuell, oder das Upgrade schlägt fehl.

     

3.  Geben Sie auf der Seite **Paketinformationen** den **Paketnamen** an, der dem aktualisierten Paket zugewiesen werden soll. Der Paketname ist erforderlich, um die zugehörige Windows Installer-Datei zu generieren. Sie sollten auch einen optionalen Kommentar hinzufügen, der dem Paket zugewiesen wird und der detaillierte Informationen zur virtuellen Anwendung bereitstellt – beispielsweise eine Versionsnummer. Wenn Sie die Seite **Erweiterte Optionen** anzeigen möchten, wählen Sie **erweiterte Überwachungsoptionen anzeigen** aus, und klicken Sie auf **weiter**. fahren Sie andernfalls mit Schritt 5 fort.

4.  Wählen Sie auf der Seite **Erweiterte Optionen** aus, damit Microsoft Update die Anwendung während der Reihenfolge aktualisieren kann, und aktivieren Sie die **Ausführung von Microsoft Update während der Überwachung**. Wenn Sie diese Option auswählen, können Microsoft-Updates während der Überwachungsphase installiert werden, und Sie müssen die zugehörigen Updates akzeptieren, damit Sie installiert werden. Wenn Sie die unterstützten dll-Dateien (Dynamic Link Library) neu zuordnen möchten, damit Sie einen zusammenhängenden Speicherbereich verwenden, wählen Sie **DLLs**erneut erstellen aus. Wenn Sie diese Option auswählen, können Sie Arbeitsspeicher sparen und die Leistung verbessern. Klicken Sie auf **Weiter**.

5.  Wenn Sie bereit sind, die Anwendung zu aktualisieren, klicken Sie auf der Seite **Monitor Installation** auf **Überwachung beginnen**.

    Wenn die Updates für die Anwendung angewendet wurden, klicken Sie auf **Überwachung beenden**. Klicken Sie auf **Weiter**.

6.  Konfigurieren Sie bei Bedarf auf der Seite **Anwendungen konfigurieren** die Verknüpfungen und Dateitypzuordnungen, die der virtuellen Anwendung zugeordnet werden. Wenn Sie eine neue Dateitypzuordnung oder Verknüpfung hinzufügen möchten, klicken Sie auf **hinzu**fügen, und geben Sie im Dialogfeld **Anwendung hinzufügen** das neue Element an. Wenn Sie eine vorhandene Verknüpfung oder Dateitypzuordnung entfernen möchten, klicken Sie auf **Entfernen**. Wenn Sie ein vorhandenes Element bearbeiten möchten, wählen Sie das zu ändernde Element aus, und klicken Sie dann auf **Bearbeiten**. Geben Sie die Konfigurationen im Dialogfeld " **Anwendung bearbeiten** " an. Klicken Sie auf **Speichern**. Klicken Sie auf **Weiter**.

7.  Klicken Sie auf der Seite **Anwendungen starten** , um die Anwendung zu starten, um sicherzustellen, dass das Paket ordnungsgemäß installiert wurde und für Streaming optimiert ist, wählen Sie das Paket aus, und klicken Sie auf **starten**. Dieser Schritt ist nützlich, um zu konfigurieren, wie die Anwendung zunächst auf Zielcomputern ausgeführt wird und welche zugehörigen Lizenzvereinbarungen akzeptiert werden, bevor das Paket für App-V-Clients zur Verfügung gestellt wird. Wenn diesem Paket mehrere Anwendungen zugeordnet sind, können Sie alle **starten** auswählen, um alle Anwendungen zu öffnen. Klicken Sie auf **weiter**, um das Paket zu sequenzieren.

8.  Klicken Sie zum Schließen des Sequenz-Assistenten auf **Fertig stellen**. Zum Speichern des aktualisierten Pakets wählen Sie in der Sequencer-Konsole **Datei**  /  **Speichern**aus.

    Wenn Sie das aktualisierte Paket mithilfe einer Windows Installer-Datei (MSI) bereitstellen möchten, müssen Sie ein neues Paket wie folgt erstellen: Wählen Sie in der Sequencer-Konsole **Tools**  /  **Create MSI**aus. Die neue Windows Installer-Datei wird in dem Verzeichnis erstellt und gespeichert, in dem das aktualisierte virtuelle Anwendungspaket gespeichert ist.

## Verwandte Themen


[So sequenzieren Sie eine neue Anwendung (App-V 4.6)](how-to-sequence-a-new-application--app-v-46-.md)

 

 





