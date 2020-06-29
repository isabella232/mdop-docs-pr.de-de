---
title: So konfigurieren Sie einen Domänenbenutzer oder eine Gruppe
description: So konfigurieren Sie einen Domänenbenutzer oder eine Gruppe
author: dansimp
ms.assetid: 055aba81-a9c9-4b98-969d-775e603becf3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4c51da13808df657c1341572767c24860d9d5e8b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812211"
---
# So konfigurieren Sie einen Domänenbenutzer oder eine Gruppe


Die Bereitstellungseinstellungen ermöglichen Ihnen, zu steuern, welche Benutzer oder Gruppen auf den Med-v-Arbeitsbereich zugreifen können, sowie, wie lange der Med-v-Arbeitsbereich genutzt werden kann und ob er offline verwendet werden kann. Sie können auch zusätzliche Regeln konfigurieren, um den Zugriff zwischen dem MED-V-Arbeitsbereich und dem Host zu steuern.

Alle Berechtigungen des MED-V-Arbeitsbereichs sind im **Richtlinien** Modul auf der Registerkarte **Bereitstellung** konfiguriert.

Damit Benutzer den Med-v-Arbeitsbereich verwenden können, müssen Sie zunächst Domänenbenutzer oder-Gruppen zu den Med-v Workspace-Berechtigungen hinzufügen. Sie können dann Berechtigungen für jeden Benutzer oder jede Gruppe einstellen.

## Hinzufügen eines Domänenbenutzers oder einer Gruppe


**So fügen Sie einen Domänenbenutzer oder eine Gruppe hinzu**

1.  Klicken Sie im Fenster **Benutzer/Gruppen** auf **hinzufügen.**

2.  Wählen Sie im Dialogfeld **Benutzer-oder Gruppennamen eingeben** eine der folgenden Aktionen aus:

    -   Geben Sie im Feld **Benutzer-oder Gruppennamen eingeben** einen Benutzer oder eine Gruppe ein, der in der Domäne oder als lokaler Benutzer oder eine Gruppe auf dem Computer vorhanden ist. Klicken Sie dann auf **Namen überprüfen** , um Sie in den vollständigen vorhandenen Namen aufzulösen.

    -   Klicken Sie auf **Suchen** , um das Dialogfeld **Benutzer oder Gruppen Standard auswählen** zu öffnen. Wählen Sie dann Domänenbenutzer oder Gruppen aus.

3.  Klicken Sie auf **OK**.

    Die Domänenbenutzer oder-Gruppen werden hinzugefügt.

    **Hinweis:**  
    Benutzer aus vertrauenswürdigen Domänen sollten manuell hinzugefügt werden.



~~~
**Warning**  
Do not run the management application from a computer that is part of a domain that is not trusted by the domain the server is installed on.
~~~



## Entfernen eines Domänenbenutzers oder einer Gruppe


**So entfernen Sie einen Domänenbenutzer oder eine Gruppe**

1.  Wählen Sie im Fenster **Benutzer/Gruppen** einen Benutzer oder eine Gruppe aus.

2.  Klicken Sie auf **Entfernen**.

    Der Benutzer oder die Gruppe wird gelöscht.

## Einrichten von Berechtigungen für einen Benutzer oder eine Gruppe


**So setzen Sie Berechtigungen für einen Benutzer oder eine Gruppe**

1.  Klicken Sie auf den Benutzer oder die Gruppe, für den Sie die Berechtigungen festlegen möchten.

2.  Konfigurieren Sie die MED-V Workspace-Eigenschaften wie in der folgenden Tabelle beschrieben.

3.  Wählen Sie im Menü **Richtlinie** die Option **Commit**aus.

**Arbeitsbereichs Bereitstellungseigenschaften**

Eigenschaftsbeschreibung *Allgemein*

Arbeitsbereich für &lt; Benutzer oder Gruppen aktivieren&gt;

Aktivieren Sie dieses Kontrollkästchen, um den MED-V-Arbeitsbereich für diesen Benutzer oder diese Gruppe zu aktivieren.

Arbeitsbereich läuft an diesem Datum ab

Aktivieren Sie dieses Kontrollkästchen, um dem Berechtigungssatz für diesen Benutzer oder diese Gruppe ein Ablaufdatum zuzuweisen.

Wenn diese Option ausgewählt ist, ist das Datumsfeld aktiviert. Legen Sie das Datum fest, und die Berechtigungen werden am Ende des angegebenen Datums ablaufen.

Offline Arbeit ist auf

Aktivieren Sie dieses Kontrollkästchen, um einen Zeitraum zuzuweisen, in dem die Richtlinie für diesen Benutzer oder diese Gruppe aktualisiert werden muss. Wenn diese Option ausgewählt ist, ist das Feld Zeitraum aktiviert. Legen Sie die Anzahl der Tage oder Stunden fest, und am Ende des angegebenen Zeitraums kann der Benutzer oder die Gruppe keine Verbindung herstellen, wenn die Richtlinie nicht aktualisiert wird.

Arbeitsbereichs Löschoptionen

Klicken Sie, um die Löschoptionen für den MED-V-Arbeitsbereich zu definieren. Weitere Informationen finden Sie unter [so wird es gemacht: Einrichten von Optionen für den Arbeitsbereichs Löschvorgang in MED-V](how-to-set-med-v-workspace-deletion-options.md).

*Datenübertragung*

Unterstützen Zwischenablage zwischen Host und Arbeitsbereich

Aktivieren Sie dieses Kontrollkästchen, um das Kopieren und Einfügen zwischen dem Host und dem MED-V-Arbeitsbereich zu aktivieren.

Unterstützung der Dateiübertragung zwischen dem Host und dem Arbeitsbereich

Aktivieren Sie dieses Kontrollkästchen, um die Übertragung von Dateien zwischen dem Host und dem MED-V-Arbeitsbereich zu aktivieren. Wählen Sie im Feld " **Dateiübertragung** " eine der folgenden Optionen aus:

-   **Beides**: Aktivieren Sie die Übertragung von Dateien zwischen dem Host und dem MED-V-Arbeitsbereich.

-   **Host to Workspace**– aktivieren Sie die Übertragung von Dateien vom Host in den MED-V-Arbeitsbereich.

-   **Arbeitsbereich für Host**: Aktivieren Sie die Übertragung von Dateien aus dem MED-V-Arbeitsbereich an den Host.

**Hinweis:**  
Wenn ein Benutzer ohne Berechtigungen versucht, Dateien zu übertragen, wird ein Fenster eingeblendet, in dem er aufgefordert wird, die Anmeldeinformationen eines Benutzers einzugeben, der über die Berechtigung zum Durchführen der Dateiübertragung verfügt.



**Wichtig**  
Um die Dateiübertragung in Windows XP SP3 zu unterstützen, müssen Sie die Offlinedateisynchronisierung deaktivieren, indem Sie die Registrierung wie folgt bearbeiten:

`REG ADD HKLM\software\microsoft\windows\currentversion\netcache /V Enabled /T REG_DWORD /F /D 0`



Erweitert

Klicken Sie, um die erweiterten Dateiübertragungsoptionen zu definieren. Weitere Informationen finden Sie unter [Vorgehensweise beim Einrichten erweiterter Dateiübertragungsoptionen](how-to-set-advanced-file-transfer-options.md).

*Gerätesteuerung*

Aktivieren des Druckvorgangs für Drucker, die mit dem Host verbunden sind

Aktivieren Sie dieses Kontrollkästchen, um Benutzern das Drucken aus dem MED-V-Arbeitsbereich mithilfe des Host Druckers zu ermöglichen.

**Hinweis:**  
Der Druck wird von den auf dem Host definierten Druckern ausgeführt.



Aktivieren des Zugriffs auf CD/DVD

Aktivieren Sie dieses Kontrollkästchen, um den Zugriff auf ein CD-oder DVD-Laufwerk über diesen MED-V-Arbeitsbereich zu ermöglichen.



**Mehrere Mitgliedschaften**

1.  Wenn der Benutzer Teil einer Gruppe ist und dem Benutzer sowie der Gruppe, der Sie angehören, Berechtigungen zugewiesen wurden, werden alle Berechtigungen angewendet.

2.  Wenn der Benutzer ein Mitglied von zwei verschiedenen Gruppen ist, werden die am wenigsten restriktiven Berechtigungen angewendet.

## Verwandte Themen


[Über die Benutzeroberfläche der MED-V-Management-Konsole](using-the-med-v-management-console-user-interface.md)

[Erstellen eines MED-V-Arbeitsbereichs](creating-a-med-v-workspacemedv-10-sp1.md)

[So legen Sie Optionen zum Löschen von MED-V-Arbeitsbereichen fest](how-to-set-med-v-workspace-deletion-options.md)

[So legen Sie erweiterte Optionen für die Dateiübertragung fest](how-to-set-advanced-file-transfer-options.md)









