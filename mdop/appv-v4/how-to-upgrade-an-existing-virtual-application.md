---
title: So aktualisieren Sie eine vorhandene virtuelle Anwendung
description: So aktualisieren Sie eine vorhandene virtuelle Anwendung
author: dansimp
ms.assetid: ec531576-2423-4c2c-9b9f-da74174a6858
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 71fb096c103a0bcb9913d4eea33b1259a33a54ee
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806711"
---
# So aktualisieren Sie eine vorhandene virtuelle Anwendung


Sie können eine vorhandene virtuelle Anwendung mithilfe von Application Virtualization (App-V) Sequencer auf eine neue Version aktualisieren. Der Aktualisierungsvorgang ähnelt dem Erstellen einer neuen virtuellen Anwendung. Sie müssen die vorhandene virtuelle Anwendung für ein Upgrade öffnen, die erforderlichen Updates vornehmen und dann die aktualisierte virtuelle Anwendung an einem neuen Speicherort im Paketstammverzeichnis speichern.

Sie können auch die App-V Sequencer-Konsole verwenden, um Änderungen an einer vorhandenen virtuellen Anwendung vorzunehmen, ohne ein Upgrade durchzuführen. Sie können jedoch keine Änderungen am Dateisystem der virtuellen Anwendung mithilfe dieser Methode vornehmen, da der App-V-Sequencer die zugehörige SFT-Datei nicht wirklich dekodiert. Beispiel: Sie können eine vorhandene virtuelle Anwendung in der App-V Sequencer-Konsole öffnen, indem Sie im Menü **Datei** die Option **Öffnen** auswählen. Sie können den **Paketnamen** und die zugehörigen **Kommentare**aktualisieren, und Sie können Änderungen am virtuellen Dateisystem und der virtuellen Registrierung vornehmen. Sie können auch eine Windows Installer-Datei erstellen.

Gehen Sie wie folgt vor, um eine vorhandene virtuelle Anwendung zu aktualisieren.

**So aktualisieren Sie eine vorhandene virtuelle Anwendung**

1.  Wenn Sie die APP-v Sequencer-Konsole starten möchten, wählen Sie auf dem Computer, auf dem der **Start**App-v-Sequencer ausgeführt wird, die Option / **Programme** / **Microsoft Application Virtualization** / **Microsoft Application Virtualization Sequencer**starten aus.

2.  Zum Öffnen der vorhandenen virtuellen Anwendung wählen Sie in der App-V-Konsole **Datei** / **Öffnen aus, um das Paket zu aktualisieren**. Verwenden Sie das Dialogfeld **für Paketaktualisierung öffnen** , um die zugeordnete SPRJ-Datei zu finden, die Sie für das Upgrade öffnen möchten.

3.  Wenn Sie den Speicherort angeben möchten, an dem das Paket decodiert werden soll, klicken Sie auf **Ordner durchsuchen** , und geben Sie den Q:\\. Dies ist der Speicherort, an dem das Paketstammverzeichnis wie in der zugehörigen SFT-Datei angegeben erstellt wird. Wenn Sie die aktualisierte Version des Pakets erstellen, wird diese mit einer sequenziellen Erweiterung des Verzeichnis namens gekennzeichnet, beispielsweise wird "**.1**" dem Verzeichnisnamen hinzugefügt, der sich auf dem Q:\\-Laufwerk befindet.

4.  Zum Öffnen des Sequenz-Assistenten wählen Sie **Tools**- / **Sequenz-Assistent**aus. Geben Sie auf der Seite **Paketinformationen** optional den neuen **Paketnamen** an, und fügen Sie optionale Kommentare hinzu, die der aktualisierten virtuellen Anwendung zugeordnet werden. Klicken Sie auf **Weiter**.

5.  Klicken Sie auf der Seite **Monitor Installation** auf Überwachung **starten**, um mit der Überwachung der neuen Installation zu beginnen. Nachdem die virtuelle Umgebung geladen wurde, installieren Sie die aktualisierte Version der Anwendung, oder wenden Sie Updates auf die vorhandene Anwendung an. Nachdem Sie die Aktualisierung der virtuellen Anwendung beendet haben, klicken Sie auf **Überwachung beenden**, und klicken Sie dann auf **weiter**.

6.  Klicken Sie auf der Seite zusätzliche Dateien, die dem virtuellen Datei **System (VFS) zugeordnet** werden sollen, um weitere Dateien anzugeben, die dem virtuellen Dateisystem (VFS) hinzugefügt werden sollen, auf **Hinzufügen**. Navigieren Sie zu der Datei, die Sie hinzufügen möchten, und klicken Sie auf **Öffnen**. Um vorhandene Dateien zu löschen, die hinzugefügt wurden, klicken Sie auf **Zurücksetzen**, und klicken Sie dann auf **weiter**.

7.  Konfigurieren Sie auf der Seite **Anwendungen konfigurieren** die Verknüpfungen und Dateitypzuordnungen, die der aktualisierten virtuellen Anwendung zugeordnet werden. Wählen Sie das Element aus, das Sie aktualisieren möchten, und klicken Sie dann auf **Speicherorte bearbeiten**. Geben Sie im Dialogfeld **Verknüpfungs Orte** die Konfigurationen an, und klicken Sie dann auf **weiter**.

8.  Wählen Sie auf der Seite **Anwendungen starten** die Anwendung aus, um sicherzustellen, dass das Paket für Streaming optimiert ist, und klicken Sie auf **Start**. Dieser Schritt ist nützlich, um zu konfigurieren, wie die Anwendung zunächst auf Zielcomputern ausgeführt wird und welche zugehörigen Lizenzvereinbarungen akzeptiert werden, bevor das Paket für Clients verfügbar gemacht wird. Wenn diesem Paket mehrere Anwendungen zugeordnet sind, können Sie alle **starten** auswählen, um alle Anwendungen zu öffnen. Klicken Sie auf **weiter**, um die neue Version der virtuellen Anwendung zu sequenzieren.

9.  Klicken Sie auf der Seite **Sequenzpaket** auf **Fertig stellen**, um den Sequenz-Assistenten abzuschließen und zu schließen.

10. Nachdem Sie die virtuelle Anwendung erfolgreich aktualisiert haben, wählen Sie zum Speichern des Pakets in der App-V Sequencer-Konsole im Menü **Datei** die Option **Speichern**aus. Auf die virtuelle Anwendung kann in dem in Schritt 3 angegebenen Verzeichnis zugegriffen werden.

## Verwandte Themen


[Application Virtualization Sequencer](application-virtualization-sequencer.md)

[So aktualisieren Sie eine virtuelle Anwendung über die Befehlszeile](how-to-upgrade-a-virtual-application-by-using-the-command-line.md)

 

 





