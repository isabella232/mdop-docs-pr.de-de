---
title: So wenden Sie allgemeine Einstellungen auf einen MED-V-Arbeitsbereich an
description: So wenden Sie allgemeine Einstellungen auf einen MED-V-Arbeitsbereich an
author: dansimp
ms.assetid: 6152dced-e301-4fa2-bfa0-aecf3c23f23a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 176564ae1d22b27a24625d988f46c9746b291748
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811815"
---
# So wenden Sie allgemeine Einstellungen auf einen MED-V-Arbeitsbereich an


Mit den allgemeinen Einstellungen können Sie die grundlegende Benutzeroberfläche beim Arbeiten mit einem Med-v-Arbeitsbereich konfigurieren, indem Sie definieren, ob der Med-v-Arbeitsbereich in der nahtlosen Integration oder im vollständigen Desktopmodus angezeigt werden soll. Die nahtlose Integration umfasst Legacyanwendungen im Host Desktop, sodass Sie so aussehen, als ob Sie direkt auf dem Host installiert werden. Der vollständige Desktop stellt den Desktop des MED-V Workspace-Betriebssystems in einem separaten Fenster auf dem Host dar.

Alle allgemeinen Einstellungen werden im **Richtlinien** Modul auf der Registerkarte **Allgemein** konfiguriert.

**So wenden Sie allgemeine Einstellungen auf einen MED-V-Arbeitsbereich an**

1.  Klicken Sie auf den MED-V-Arbeitsbereich, den Sie konfigurieren möchten.

2.  Konfigurieren Sie die allgemeinen Eigenschaften wie in der folgenden Tabelle beschrieben.

3.  Wählen Sie im Menü **Richtlinie** die Option **Commit**aus.

**Allgemeine Arbeitsbereichseigenschaften**

Eigenschaft Beschreibung *Arbeitsbereichseigenschaften*

Name

Der Name des MED-V-Arbeitsbereichs.

**Warnung**  Benennen Sie einen vorhandenen MED-V-Arbeitsbereich nicht um, während er auf einem Clientcomputer ausgeführt wird.

 

Beschreibung

Beschreibung des Med-v-Arbeitsbereichs, der den Inhalt oder Status des Med-v-Arbeitsbereichs sowie alle anderen nützlichen Informationen enthalten kann.

**Hinweis**  Die Beschreibung ist für die Verwendung durch den Administrator vorgesehen und hat keine Auswirkungen auf die Richtlinie.

 

Support – Kontaktinfos

Die Kontaktinformationen für den technischen Support. Die eingegebenen Informationen werden auf dem Bildschirm Supportkontaktinformationen angezeigt, auf den Sie über den Infobereich des MED-V-Clients zugreifen können.

*Arbeitsbereich-Benutzeroberfläche*

Nahtlose Integration

Wählen Sie diese Option für die Windows-, Taskleisten-und Infobereich-Symbole des MED-V Workspace aus, um sich nahtlos in den Host Desktop zu integrieren.

Zeichnen eines Rahmens um jedes Arbeitsbereichsfenster

Wenn Sie die nahtlose Integration verwenden, wählen Sie diese Option aus, um einen farbigen Rahmen um alle Anwendungen zu erstellen, die im MED-V-Arbeitsbereich ausgeführt werden, sowie einen farbigen Hintergrund für alle Symbolleistenschaltflächen. Wählen Sie im Feld **Rahmenfarbe** die gewünschte Farbe aus.

Vollständiger Desktop

Wählen Sie diese Option aus, um den MED-V-Arbeitsbereich als gesamten Desktop anzuzeigen, ohne den Host zu integrieren.

*Host Überprüfung*

Befehlszeile

Geben Sie eine Befehlszeile ein, die auf dem Host ausgeführt werden soll, bevor Sie den MED-V-Arbeitsbereich starten.

Starten Sie den Arbeitsbereich nicht, wenn die Überprüfung fehlschlägt (Exitcode ist nicht "0")

Aktivieren Sie dieses Kontrollkästchen, wenn Sie eine Befehlszeile verwenden und den MED-V-Arbeitsbereich nur starten möchten, wenn das Skript erfolgreich abgeschlossen wurde.

 

Vor dem Starten des MED-V-Arbeitsbereichs kann eine Befehlszeile auf dem Host ausgeführt werden.

**So führen Sie eine Befehlszeile aus, bevor Sie einen MED-V-Arbeitsbereich starten**

1.  Geben Sie im Feld **Befehlszeile** eine Befehlszeile ein.

2.  Wenn Sie den MED-V-Arbeitsbereich nur starten möchten, wenn die Befehlszeile erfolgreich war, aktivieren Sie das Kontrollkästchen **Arbeitsbereich nicht starten, wenn die Überprüfung fehlschlägt** .

## Verwandte Themen


[Über die Benutzeroberfläche der MED-V-Management-Konsole](using-the-med-v-management-console-user-interface.md)

[Erstellen eines MED-V-Arbeitsbereichs](creating-a-med-v-workspacemedv-10-sp1.md)

 

 





