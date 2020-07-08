---
title: Problembehandlung für MED-V
description: Problembehandlung für MED-V
author: dansimp
ms.assetid: f43dae36-6485-4e06-9c66-0a646e27079d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 38d13be699a92368ff258026acd8e0d5f0e28cd6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811410"
---
# Problembehandlung für MED-V


Dieser Abschnitt enthält Informationen zur Problembehandlung bei allgemeinen Problemen mit Microsoft Enterprise Desktop Virtualization (MED-V).

## Wenn Sie die Hostauflösung ändern und dann den MED-V-Arbeitsbereich maximieren, wird der Desktop schwarz angezeigt.


Wenn Sie im vollständigen Desktopmodus arbeiten und die Hostauflösung ändern und dann das Med-v Workspace-Fenster maximieren, wird der Desktop schwarz angezeigt, und der Med-v-Arbeitsbereich reagiert möglicherweise nicht.

### Lösung

Beenden Sie den MED-V-Arbeitsbereich, und starten Sie ihn dann.

## Das Starten eines MED-V-Arbeitsbereichs mit deaktiviertem Netzwerkadapter und späterer Aktivierung des Adapters stellt keine Netzwerkkonnektivität wieder her


Wenn Sie einen Med-v-Arbeitsbereich im Brückenmodus konfigurieren und dann den Med-v-Arbeitsbereich starten, während ein Netzwerkadapter deaktiviert ist, wird die Netzwerkverbindung über diesen Adapter nicht wiederhergestellt, wenn der Adapter später aktiviert ist.

### Lösung

Beenden Sie den MED-V-Arbeitsbereich, und starten Sie ihn dann.

## Ein Bild kann nur von einem Windows-Benutzer pro Computer verwendet werden.


Ein MED-V Workspace-Bild kann nur von Windows-Benutzern verwendet werden, die das Bild heruntergeladen oder importiert haben. Dieser Benutzer ist der einzige Benutzer neben Administratoren, die über die Berechtigungen für den Ordner verfügen, in dem sich die heruntergeladenen Bilder befinden.

### Lösung

Manuelles Ändern der Zugriffssteuerungsliste (ACL) im Bildspeicher

## Bei der Installation von MED-V mithilfe von Configuration Manager mit aktivierten Benutzerrechten schlägt die Deinstallation fehl


Wenn MED-V mit Microsoft System Center Configuration Manager installiert ist und der Ausführungsmodus des Pakets auf Benutzerrechte festgesetzt ist, schlägt die Deinstallation mit einer Fehlermeldung fehl, die besagt, dass nur administrative Benutzer MED-V deinstallieren können.

### Lösung

Legen Sie beim Erstellen eines Configuration Manager-Pakets für MED-V den Ausführungsmodus auf Administratorrechte.

## Wenn Sie MED-V mithilfe eines Unternehmens Bereitstellungssystems installieren, in dem die Installation so konfiguriert ist, dass der Client nach der Installation ausgeführt wird, können Sie den Client nicht ausführen.


Wenn Med-v mit einem Unternehmens Bereitstellungssystem installiert ist und das Installationspaket so konfiguriert ist, dass der Med-v-Client nach der Installation ausgeführt wird, können Sie nach dem Ausführen des Clients unter dem Systemkonto nicht sehen, dass der Client ausgeführt wird (außer im Infobereich), und Sie können nicht mit ihm interagieren.

### Lösung

Wenn Sie MED-V mithilfe eines Unternehmens Bereitstellungssystems installieren, verwenden Sie den Parameter *Start \ _MEDV = 0* . msi.

## MED-V-Testbild kann nicht gestartet werden


Wenn ein MED-V-Testbild nicht gestartet werden kann, wird es nie wiederhergestellt, und alle zukünftigen Starts werden mit der Fehlermeldung "Gina-Fehler beim Laden" fehlschlagen.

### Lösung

Löschen Sie das vorhandene Test Abbild, und erstellen Sie es dann erneut.

## Nach dem Versuch, einer Domäne mit den falschen Anmeldeinformationen beizutreten, gelingt es dem Bild nie, der Domäne beizutreten.


Wenn ein Konfigurationsfehler im Building Block der Join-Domäne vorhanden ist, der zum erstmaligen Setup-Skript der virtuellen Maschine gehört, bewirkt dies, dass der MED-V-Arbeitsbereich beim Versuch, einer Domäne beizutreten, fehlschlägt. Nachdem der Konfigurationsfehler behoben wurde, kann das im MED-V-Arbeitsbereich enthaltene Bild nicht zur Domäne hinzugefügt werden.

### Lösung

Wenn das Bild bereitgestellt wurde, verteilen Sie es erneut. Wenn es sich bei dem Bild um ein Testbild handelt, erstellen Sie das Bild erneut.

## MED-V unterstützt nicht mehrere Monitore


MED-V unterstützt die Anzeige von veröffentlichten Anwendungen auf mehreren Monitoren nicht. Veröffentlichte Anwendungen und andere Clientfenster werden möglicherweise auf dem falschen Bildschirm angezeigt, und manchmal, nachdem ein Bildschirm getrennt wurde, versucht MED-V, den Bildschirm an den Monitor zu senden, damit der angeschlossene Monitor leer angezeigt wird.

### Lösung

Trennen Sie den zusätzlichen Bildschirm, und starten Sie den Client neu.

## Der Med-v-Arbeitsbereich kann nicht gestartet werden, wenn der Host während des Starts des Med-v-Arbeitsbereichs abstürzt


Wenn der Host während des Startvorgangs des Med-v-Arbeitsbereichs abstürzt und eine Fehlermeldung mit dem Hinweis "Stammelement fehlt" angezeigt wird, kann der Med-v-Arbeitsbereich Daten zu einer leeren VMC-Datei (Virtual Machine Configuration) hinzufügen, wodurch der Startvorgang fehlschlägt.

### Lösung

Ersetzen Sie die leere VMC-Datei durch eine VMC-Datei aus dem Basis Bild.

## Die Tastatur reagiert in veröffentlichten Anwendungsfenstern nicht


Wenn Sie in einem MED-V-Arbeitsbereich die Windows-Logo-Taste drücken, während sich eine veröffentlichte Anwendung im Fokus befindet, reagiert die Tastatur nicht mehr in veröffentlichten Anwendungsfenstern.

### Lösung

Drücken Sie die Windows-Logo-Taste, während eine veröffentlichte Anwendung den Fokus hat.

## Ein Domänen-MED-V-Arbeitsbereich aktualisiert keine Domänenanmeldeinformationen


Wenn Sie einen beständigen Med-v-Arbeitsbereich in einer Domänenumgebung verwenden und Ihr Domänenkennwort ändern, aktualisiert der Med-v-Client die Anmeldeinformationen für die Med-v Workspace-Domäne nicht. Wenn eine veröffentlichte Anwendung versucht, auf eine Netzwerkressource zuzugreifen, erhalten Sie eine Fehlermeldung, in der Sie darüber informiert werden, dass Ihre Anmeldeinformationen abgelaufen sind.

### Lösung

Starten Sie das Betriebssystem MED-V Workspace neu.

## Maximierte veröffentlichte Anwendungsfenster decken die Host-Taskleiste ab


Wenn Sie ein veröffentlichtes Anwendungsfenster auf Vollbild maximieren, kann es die Host-Taskleiste abdecken.

### Lösung

Führen Sie eine der folgenden Aktionen aus:

Minimieren Sie das Fenster "veröffentlichte Anwendung", um Zugriff auf den Infobereich zu erhalten, und starten Sie den MED-V-Arbeitsbereich neu.

Minimieren Sie das Fenster der veröffentlichten Anwendung, und stellen Sie das Fenster dann auf seinen maximierten Zustand zurück.

## Das Hinzufügen von Benutzern oder Gruppen im MED-V Server-Konfigurations-Manager funktioniert nicht


Beim Hinzufügen von Benutzern oder Gruppen im Dialogfeld **Benutzer oder Gruppen auswählen** werden die ausgewählten Benutzer oder Gruppen nicht zur Zugriffssteuerungsliste im MED-V Server-Konfigurations-Manager hinzugefügt.

### Lösung

Hinzufügen von Benutzern oder Gruppen mithilfe des Dialogfelds **Benutzer-oder Gruppennamen eingeben** . Ausführliche Informationen finden Sie unter [so wird es gemacht: Installieren und Konfigurieren der MED-V-Server Komponente](how-to-install-and-configure-the-med-v-server-component.md#bkmk-configuringpermissions).

## MED-V funktioniert nicht auf Computern, auf denen Windows Virtual PC für Windows 7 installiert ist


Für MED-V ist Windows Virtual PC2007 erforderlich. Windows Virtual PC für Windows7 und Virtual PC2007 SP1 können nicht auf demselben Computer installiert werden.

### Lösung

Deinstallieren Sie Virtual PC für Windows7, bevor Sie Virtual PC2007 SP1 und MED-V installieren.

## <a href="" id="med-v-does-not-support-virtual-pc-and-windows-xp-mode-images-"></a>MED-V unterstützt keine Images für Virtual PC und WindowsXP-Modus


Med-v 1.0 SP1 unterstützt keine Bilder, die von Windows Virtual PC für Windows7 erstellt wurden. Wenn ein virtueller PC für Windows7-Bild verwendet wird, schlägt der Client während des Starts fehl.

### Lösung

Erstellen Sie MED-V-Bilder mithilfe von Virtual PC2007 SP1.

## Die Windows-Firewall blockiert die virtuelle PC2007 SP1-Netzwerkaktivität


Standardmäßig blockiert die Windows-Firewall virtuelle PC2007 SP1-Netzwerkaktivitäten, und wenn Virtual PC2007 SP1 auf dem Clientcomputer initiiert wird, gibt es eine Firewall-Nachricht, die die Startsequenz und den gesamten Netzwerkzugriff blockiert.

### Lösung

Aktualisieren Sie die Firewall-Ausnahme mithilfe von Gruppenrichtlinien, bevor MED-V vom Endbenutzer verwendet wird.

## Beim Aktualisieren des Clients wird eine Fehlermeldung angezeigt.


Wenn Sie den Client von Med-v 1.0 auf Med-v 1.0 SP1 aktualisieren, wird möglicherweise eine Meldung angezeigt, in der Sie darüber informiert werden, dass kein Med-v-Arbeitsbereich definiert ist.

### Lösung

Schließen Sie den Client, und starten Sie ihn erneut.

## Verwandte Themen


[Versionshinweise für MED-V 1.0](med-v-10-release-notesmedv-10.md)

[MED-V 1.0 SP1 und SP2-Versionshinweise](med-v-10-sp1-and-sp2-release-notesmedv-10-sp1.md)

 

 





