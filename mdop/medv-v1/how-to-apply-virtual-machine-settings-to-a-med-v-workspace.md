---
title: So wenden Sie die Einstellungen des virtuellen Computers auf einen MED-V-Arbeitsbereich an
description: So wenden Sie die Einstellungen des virtuellen Computers auf einen MED-V-Arbeitsbereich an
author: dansimp
ms.assetid: b50d0dfb-8d61-4543-9607-a29bbb1ed45f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9662bb8202285d51971eeea8beaef938b98ed6b0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811476"
---
# So wenden Sie die Einstellungen des virtuellen Computers auf einen MED-V-Arbeitsbereich an


Jedem MED-V-Arbeitsbereich muss ein Microsoft Virtual PC-Abbild zugeordnet sein. Mit den Einstellungen für den virtuellen Computer können Sie ein virtuelles PC-Abbild zuweisen und andere Eigenschaften des virtuellen Computers festlegen.

Alle Einstellungen für den virtuellen Computer werden im **Richtlinien** Modul auf der Registerkarte **Einstellungen für virtuelle Computer** konfiguriert.

**So wenden Sie Einstellungen für virtuelle Computer auf einen MED-V-Arbeitsbereich an**

1.  Klicken Sie auf den MED-V-Arbeitsbereich, den Sie konfigurieren möchten.

2.  Konfigurieren Sie die Eigenschaften des virtuellen Computers wie in der folgenden Tabelle beschrieben.

3.  Wählen Sie im Menü **Richtlinie** die Option **Commit**aus.

**Eigenschaften von virtuellen Computern**

Eigenschaften Beschreibung *Einstellungen für den virtuellen Computer*

Zugewiesenes Bild

Das tatsächliche Microsoft Virtual PC-Abbild, das dem MED-V-Arbeitsbereich zugewiesen ist. Das Menü enthält eine Liste aller verfügbaren Virtual PC-Bilder. Die folgenden Bildtypen befinden sich in der Liste der **aktiven** Bilder:

-   **Lokale Testbilder**– Bilder auf dem lokalen Computer, die noch nicht gepackt sind. Auf diese Bild Namen folgt das Wort "Test" in Klammern (Test) und dient nur zu Testzwecken.

-   **Lokal verpackte Bilder**– komprimierte Bilder auf dem lokalen Computer. Auf diese Bilder folgt das Wort "local" in Klammern (lokal) und kann nicht von Clients heruntergeladen werden, bis der Administrator Sie auf den Server hochgeladen hat.

    Ein lokales Bild kann ausgewählt werden, wenn Sie ein Paket erstellen, das über Wechselmedien (wie USB oder DVD) an den Client verteilt wird.

-   **Komprimierte Bilder auf dem Server**– Bilder auf dem Server, die von Clients heruntergeladen werden können. Klicken Sie auf aktualisieren, um die Liste Bilder zu aktualisieren.

    **Hinweis**  Jedes MED-V Workspace-Bild kann nur von einem Windows-Benutzer verwendet werden.

     

Arbeitsbereich ist persistent

Aktivieren Sie dieses Kontrollkästchen, um den MED-V-Arbeitsbereich als persistent zu konfigurieren. Wenn der Med-v-Arbeitsbereich in einem beständigen Med-v-Arbeitsbereich beendet wird, werden Änderungen und Ergänzungen des Med-v-Arbeitsbereichs im Med-v-Arbeitsbereich gespeichert.

Bei einem Domänen-MED-V-Arbeitsbereich muss diese Option ausgewählt sein.

**Hinweis**  Diese Einstellung sollte nicht geändert werden, nachdem ein MED-V-Arbeitsbereich für Benutzer bereitgestellt wurde.

 

Beenden des virtuellen Computers beim Beenden des Arbeitsbereichs

Aktivieren Sie dieses Kontrollkästchen, um den virtuellen Computer zu beenden, wenn Sie den MED-V-Arbeitsbereich beenden. Wenn dieses Kontrollkästchen deaktiviert ist, wird nach Abschluss jeder Sitzung der virtuelle Computer nicht heruntergefahren, sondern stattdessen wird eine Momentaufnahme des virtuellen Computers erstellt. Nach dem Initiieren einer neuen Sitzung beginnt Windows mit dem Snapshot (das heißt, Windows wird nicht neu gestartet, und es ist keine Anmeldung erforderlich).

**Hinweis**  Diese Eigenschaft ist nur aktiviert, wenn " **Arbeitsbereich ist persistent** " ausgewählt ist.

 

Anmelden bei Windows in VM mithilfe von MED-V-Anmeldeinformationen (SSO)

Aktivieren Sie dieses Kontrollkästchen, um sich bei Windows auf dem virtuellen Computer mit den Med-v-Anmeldeinformationen anzumelden, die bei der Anmeldung bei Med-v-Client eingegeben wurden.

**Hinweis**  Diese Eigenschaft ist nur aktiviert, wenn " **Arbeitsbereich ist persistent** " ausgewählt ist.

 

Arbeitsbereich ist revertible

Aktivieren Sie dieses Kontrollkästchen, um den MED-V-Arbeitsbereich als revertible zu konfigurieren. In einem revertible Med-v-Arbeitsbereich wird nach Abschluss jeder Sitzung (d. h., wenn der Benutzer den Med-v-Arbeitsbereich beendet) der Med-v-Arbeitsbereich auf den ursprünglichen Zustand zurückgesetzt, in dem er sich während der Bereitstellung befand. Keine Änderungen oder Ergänzungen, die der Benutzer vorgenommen hat, werden im MED-V-Arbeitsbereich zwischen Sitzungen gespeichert.

**Hinweis**  Diese Einstellung sollte nicht geändert werden, nachdem ein MED-V-Arbeitsbereich für Benutzer bereitgestellt wurde.

 

Synchronisieren der Arbeitsbereichs Zeitzone mit dem Host

Aktivieren Sie dieses Kontrollkästchen, um die Zeitzone im MED-V-Arbeitsbereich mit dem Host zu synchronisieren.

Die Synchronisierung funktioniert unterschiedlich, je nachdem, ob der MED-V-Arbeitsbereich persistent oder revertible ist, wie im folgenden beschrieben:

-   In einem beständigen MED-V-Arbeitsbereich versucht die Zeitzone zunächst, mit dem Server zu synchronisieren. Wenn das fehlschlägt, wird es mit dem Host synchronisiert.

-   In einem revertible MED-V-Arbeitsbereich wird die Zeitzone mit dem Host synchronisiert.

*Einstellungen sperren*

Sperren des Arbeitsbereichs im Host-Standby/Hibernate-Ereignis

Aktivieren Sie dieses Kontrollkästchen, um den MED-V-Arbeitsbereich automatisch zu sperren, wenn der Hostcomputer in den Standbymodus oder Ruhezustand wechselt.

Sperren des Arbeitsbereichs nach

Aktivieren Sie dieses Kontrollkästchen, um den Med-v-Arbeitsbereich zu sperren, wenn sich der Med-v-Arbeitsbereich für einen bestimmten Zeitraum im Leerlauf befindet. Wenn diese Option ausgewählt ist, ist das Feld Zahl aktiviert. Geben Sie die Anzahl der Minuten der Leerlaufzeit ein, bevor Sie den MED-V-Arbeitsbereich sperren.

**Hinweis**  Die Leerlaufzeit bezieht sich auf die MED-V Workspace-Anwendungen (nicht auf die Hostanwendungen).

 

*Bild Aktualisierungseinstellungen*

Nur beibehalten

Aktivieren Sie dieses Kontrollkästchen, um die Anzahl der alten Bildversionen zu begrenzen, die beibehalten werden sollen.

Wenn diese Option ausgewählt ist, ist das Feld Zahl aktiviert. Geben Sie die Anzahl der alten Versionen ein, die Sie beibehalten möchten.

Update vorschlagen, wenn eine neue Version verfügbar ist

Aktivieren Sie dieses Kontrollkästchen, wenn Sie ein Update vorschlagen (aber nicht erzwingen) möchten, wenn eine neue Version des Bilds verfügbar ist.

Clients sollten Trim-Übertragung beim Herunterladen von Bildern für diesen Arbeitsbereich verwenden.

Aktivieren Sie dieses Kontrollkästchen, um die Trimm Übertragung zu aktivieren (Weitere Informationen finden Sie unter [Med-v Trim Transfer Technology](med-v-trim-transfer-technology-medvv2.md)) beim Herunterladen von Bildern, die diesem Med-v-Arbeitsbereich zugeordnet sind. Wenn dieses Kontrollkästchen deaktiviert ist, wird das vollständige Bild heruntergeladen.

**Hinweis**  Bei der Trimm Übertragung muss die Festplatte indiziert werden, was viel Zeit in Anspruch nehmen kann. Es wird empfohlen, die Trim-Übertragung zu verwenden, wenn die Indizierung der Festplatte effizienter als das Herunterladen der neuen Bildversion ist, beispielsweise beim Herunterladen einer Bildversion, die mit der vorhandenen Version vergleichbar ist.

 

 

## Verwandte Themen


[Erstellen eines MED-V-Images](creating-a-med-v-image.md)

[Über die Benutzeroberfläche der MED-V-Management-Konsole](using-the-med-v-management-console-user-interface.md)

[Erstellen eines MED-V-Arbeitsbereichs](creating-a-med-v-workspacemedv-10-sp1.md)

 

 





