---
title: So erstellen und testen Sie ein MED-V-Image
description: So erstellen und testen Sie ein MED-V-Image
author: dansimp
ms.assetid: 40e4aba6-12cb-4794-967d-2c09dc20d808
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9f7989871a695b09c987124ab02c0143082148f3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812118"
---
# So erstellen und testen Sie ein MED-V-Image


Der Med-v-Administrator erstellt ein Med-v-Abbild, damit es hochgeladen, einem Med-v-Arbeitsbereich zugeordnet und dann an den Client über das Web verteilt, zu einem Med-v-Paket hinzugefügt oder über ein Drittanbietersystem auf den Client heruntergeladen werden kann. Es wird empfohlen, zunächst ein Testbild zu erstellen und es auf dem MED-V-Client zu testen, bevor es bereitgestellt wird.

Beim Erstellen eines MED-V-Bilds durchläuft es die folgenden Schritte:

1.  **Lokales Test Abbild**– ein grundlegendes Bild, das lokal getestet werden kann.

2.  **Lokal verpacktes Bild**– nachdem das Bild getestet wurde, wird das Bild vor dem Testen gepackt. Im gepackten Bild sind keine Änderungen enthalten, die während der Tests vorgenommen wurden.

3.  **Gepacktes Bild auf dem Server**– das komprimierte Bild wird auf den Server hochgeladen.

## Erstellen eines MED-V-Test Bilds


**So erstellen Sie ein neues MED-V-Testbild**

1.  Klicken Sie auf die Schaltfläche " **Bilder** Verwaltung".

    Das Modul **Bilder** wird angezeigt.

    -   Das Modul **Bilder** besteht aus den folgenden Bereichen:

        -   **Lokale Test Bilder**– lokale ungepackte Bilder.

        -   **Lokal verpackte Bilder**– alle komprimierten Bilder auf dem lokalen Computer.

        -   **Komprimierte Bilder auf dem Server**– alle Bilder, die gepackt und auf den Server hochgeladen wurden.

    -   In den **lokalen gepackten Bildern** und **gepackten Bildern** in den Server Bereichen wird die neueste Version der einzelnen Bilder als übergeordneter Knoten angezeigt. Klicken Sie auf den übergeordneten Knoten, um alle anderen vorhandenen Versionen des Bilds anzuzeigen.

2.  Klicken Sie im Bereich **lokale Test Bilder** auf **neu**.

3.  Wählen Sie im Dialogfeld **Bild Erstellung testen** das Bild des virtuellen Computers aus, das Sie als MED-V-Testbild konfigurieren möchten, indem Sie eine der folgenden Aktionen ausführen:

    -   Geben Sie im Feld **Basisbild** -Datei den vollständigen Pfad zu dem Verzeichnis ein, in dem sich das für MED-V vorbereitete Microsoft Virtual PC-Abbild befindet.

    -   Klicken Sie auf **Durchsuchen** , um zu dem Verzeichnis zu navigieren, in dem sich das für MED-V vorbereitete Microsoft Virtual PC-Abbild befindet.

4.  Geben Sie im Feld **Image Name** den gewünschten Namen ein, oder wählen Sie ihn aus.

    **Hinweis**  Die folgenden Zeichen können im Bildnamen nicht enthalten sein: Leerzeichen " &lt; &gt; | \\ / : \* ?

     

5.  Klicken Sie auf **OK**.

    Auf dem Hostcomputer wird ein neues MED-V-Testbild mit den Eigenschaften erstellt, die in der folgenden Tabelle definiert sind.

    Weitere Informationen zum Konfigurieren des Med-v Workspace-Bilds finden Sie unter [Konfigurieren von Med-v-Arbeitsbereichs Richtlinien](configuring-med-v-workspace-policies.md).

**Eigenschaften für lokale Test Bilder**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Eigenschaft</th>
<th align="left">Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Name des Bilds</p></td>
<td align="left"><p>Der Name des Testbilds, wie es beim Erstellen des Bilds durch den Administrator definiert wurde.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Bild Pfad</p></td>
<td align="left"><p>Der lokale Pfad des Test Bilds.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Erstellt</p></td>
<td align="left"><p>Das Datum, an dem das Testbild erstellt wurde.</p></td>
</tr>
</tbody>
</table>

 

## Testen eines Med-v-Bilds vom Med-v-Client


Nachdem ein MED-V-Testbild erstellt wurde, verwenden Sie das folgende Verfahren, um das Bild lokal zu testen.

**So testen Sie ein MED-V-Bild**

1.  Klicken Sie auf die Schaltfläche **Richtlinien** Verwaltung.

2.  Weisen Sie im **Richtlinien** Modul das Med-v-Testbild einem Med-v-Arbeitsbereich zu, indem Sie wie folgt vorgehen:

    1.  Klicken Sie auf die Registerkarte **virtueller Computer** .

    2.  Wählen Sie im Feld **zugewiesene Bild** das von Ihnen erstellte MED-V-Testbild aus. Wenn das Testbild nicht in der Liste aufgeführt ist, klicken Sie auf **Aktualisieren**.

    3.  Klicken Sie auf der Symbolleiste auf **Änderungen speichern**.

3.  Konfigurieren Sie alle anderen MED-V Workspace-Einstellungen, die getestet werden sollen. Weitere Informationen finden Sie unter [Konfigurieren von MED-V-Arbeitsbereichs Richtlinien](configuring-med-v-workspace-policies.md).

4.  Starten Sie den MED-V-Client.

5.  Klicken Sie im Dialogfeld **Test Bestätigung bestätigen** auf **Testbild verwenden**.

6.  Testen Sie das MED-V Workspace-Testbild.

    Informationen zum Starten und Ausführen des Med-v-Clients finden Sie unter [Med-v-Client Vorgänge](med-v-client-operations.md).

**Hinweis**  Öffnen Sie beim Testen eines Bilds nicht VPC, und nehmen Sie Änderungen am Bild vor.

 

**Hinweis**  Beim Testen eines Bilds werden keine Änderungen zwischen den Sitzungen auf dem Bild gespeichert. Stattdessen werden Sie in einer separaten, temporären Datei gespeichert. Dadurch wird sichergestellt, dass das Bild, wenn es in der Produktionsumgebung verpackt und ausgeführt wird, das ursprüngliche, saubere Bild darstellt.

 

## Verwandte Themen


[Erstellen eines virtuellen PC-Images für MED-V](creating-a-virtual-pc-image-for-med-v.md)

[Erstellen eines MED-V-Arbeitsbereichs](creating-a-med-v-workspacemedv-10-sp1.md)

[Konfigurieren von MED-V-Arbeitsbereichsrichtlinien](configuring-med-v-workspace-policies.md)

[MED-V-Client-Vorgänge](med-v-client-operations.md)

 

 





