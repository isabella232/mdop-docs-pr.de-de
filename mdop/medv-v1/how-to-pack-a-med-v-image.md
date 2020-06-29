---
title: So packen Sie ein MED-V-Image
description: So packen Sie ein MED-V-Image
author: dansimp
ms.assetid: e1ce2307-0f1b-4bf8-b146-e4012dc138d2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0a330b8feca922239691bed083767c3acc57105d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810699"
---
# So packen Sie ein MED-V-Image


Ein MED-V-Abbild muss gepackt sein, bevor es einem Bereitstellungspaket hinzugefügt oder auf den Server hochgeladen werden kann.

**So erstellen Sie ein komprimiertes MED-V-Bild**

1.  Klicken Sie auf die Schaltfläche " **Bilder** Verwaltung".

2.  Klicken Sie im Modul **Bilder** im Bereich **lokal verpackte Bilder** auf **neu**.

3.  Wählen Sie im Dialogfeld **komprimierte Bild Erstellung** das Bild des virtuellen Computers aus, indem Sie eine der folgenden Aktionen ausführen:

    -   Geben Sie im Feld **Basisbild-Datei** den vollständigen Pfad zu dem Verzeichnis ein, in dem sich das für MED-V vorbereitete Microsoft Virtual PC-Abbild befindet.

    -   Klicken Sie auf **Durchsuchen** , um zu dem Verzeichnis zu navigieren, in dem sich das für MED-V vorbereitete Microsoft Virtual PC-Abbild befindet.

4.  Geben Sie den Namen des neuen Bilds an, indem Sie eine der folgenden Aktionen ausführen:

    -   Geben Sie im Feld **Image Name** den gewünschten Namen ein.

        **Hinweis:**  
        Die folgenden Zeichen können im Bildnamen nicht enthalten sein: Leerzeichen " &lt; &gt; | \\ / : \* ?



~~~
    A new packed image will be created.

-   From the drop-down list, select an existing name.

    A new version of the existing image will be created.
~~~

5. Klicken Sie auf **OK**.

   Auf dem Hostcomputer wird ein neues MED-V-gepacktes Bild mit den Eigenschaften erstellt, die in der folgenden Tabelle definiert sind.

**Hinweis:**  
In den **lokalen gepackten Bildern** und **gepackten Bildern** in den Server Bereichen wird die neueste Version der einzelnen Bilder als übergeordneter Knoten angezeigt. Klicken Sie auf den übergeordneten Knoten, um alle anderen vorhandenen Versionen des Bilds anzuzeigen.



**Eigenschaften für lokal verpackte Bilder**

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
<td align="left"><p>Der Name des gepackten Bilds, wie es beim Erstellen des Bilds durch den Administrator definiert wurde.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Version</p></td>
<td align="left"><p>Die Version des angezeigten Bilds.</p>
<div class="alert">
<strong>Hinweis:</strong><br/><p>Alle vorherigen Versionen werden beibehalten, es sei denn, Sie werden gelöscht.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p>Dateigröße (komprimiert)</p></td>
<td align="left"><p>Die physische komprimierte Größe des Bilds.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Bildgröße (unkomprimiert)</p></td>
<td align="left"><p>Die physikalische unkomprimierte Größe des Bilds.</p></td>
</tr>
</tbody>
</table>



## Verwandte Themen


[So installieren Sie den MED-V-Client und die MED-V-Verwaltungskonsole](how-to-install-med-v-client-and-med-v-management-console.md)

[Über die Benutzeroberfläche der MED-V-Management-Konsole](using-the-med-v-management-console-user-interface.md)

[Erstellen eines virtuellen PC-Images für MED-V](creating-a-virtual-pc-image-for-med-v.md)









