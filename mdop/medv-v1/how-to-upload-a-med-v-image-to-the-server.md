---
title: So laden Sie ein MED-V-Bild auf den Server hoch
description: So laden Sie ein MED-V-Bild auf den Server hoch
author: dansimp
ms.assetid: 0e70dfdf-3e3a-4860-970c-535806caa907
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6703eb24bc3542c280af41988a257a2f14643645
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811314"
---
# So laden Sie ein MED-V-Bild auf den Server hoch


Nachdem ein MED-V-Abbild getestet wurde, kann es gepackt und dann auf den Server hochgeladen werden. Informationen zum Konfigurieren eines Image Web Distribution-Servers finden Sie unter [Konfigurieren des Image Web Distribution-Servers](how-to-configure-the-image-web-distribution-server.md).

Sobald ein MED-V-Abbild gepackt und auf den Server hochgeladen wurde, kann es mithilfe eines Enterprise-Software Verteilungs Centers an Benutzer verteilt werden, oder es kann von Benutzern mithilfe eines Bereitstellungspakets heruntergeladen werden. Informationen zur Bereitstellung mithilfe eines Software Verteilungs Centers für Unternehmen finden Sie unter [Bereitstellen eines MED-V-Arbeitsbereichs mithilfe eines Softwareverteilungssystems für Unternehmen](deploying-a-med-v-workspace-using-an-enterprise-software-distribution-system.md). Informationen zur Bereitstellung mithilfe eines Pakets finden Sie unter [Bereitstellen eines MED-V-Arbeitsbereichs mithilfe eines Bereitstellungspakets](deploying-a-med-v-workspace-using-a-deployment-package.md).

**Hinweis:**  
Bevor Sie ein Bild hochladen, stellen Sie sicher, dass in Ihren Browsereinstellungen kein WebProxy definiert ist und dass Windows Update zurzeit nicht ausgeführt wird.



**So laden Sie ein MED-V-Abbild auf den Server hoch**

1.  Wählen Sie im Bereich **lokal verpackte Bilder** das erstellte Bild aus.

2.  Klicken Sie auf **hochladen**.

    Das Bild wird auf den Server hochgeladen. Dies kann sehr viel Zeit in Anspruch nehmen.

    Bilder auf dem Server sind mit den Eigenschaften definiert, die in der folgenden Tabelle aufgeführt sind.

**Komprimierte Bilder auf Server Eigenschaften**

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

[So packen Sie ein MED-V-Image](how-to-pack-a-med-v-image.md)









