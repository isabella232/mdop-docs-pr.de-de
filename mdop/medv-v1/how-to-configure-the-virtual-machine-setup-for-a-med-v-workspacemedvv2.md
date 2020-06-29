---
title: So konfigurieren Sie die Einrichtung des virtuellen Computer für einen MED-V-Arbeitsbereich
description: So konfigurieren Sie die Einrichtung des virtuellen Computer für einen MED-V-Arbeitsbereich
author: dansimp
ms.assetid: 50bbf58b-842c-4b63-bb93-3783903f6c7d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d0ba24f0e9aa5befeaf385acf06273a53feaae29
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812136"
---
# So konfigurieren Sie die Einrichtung des virtuellen Computer für einen MED-V-Arbeitsbereich


Alle Konfigurationseinstellungen für das virtuelle Computer Setup werden im **Richtlinien** Modul auf der Registerkarte **VM-Setup** konfiguriert.

## Konfigurieren der Einrichtung eines virtuellen Computers für einen beständigen MED-V-Arbeitsbereich


**So konfigurieren Sie die Einrichtung eines virtuellen Computers für einen beständigen MED-V-Arbeitsbereich**

1.  Klicken Sie auf einen persistenten MED-V-Arbeitsbereich, der konfiguriert werden soll.

2.  Konfigurieren Sie im Abschnitt **persistent VM Setup** die Eigenschaften wie in der folgenden Tabelle beschrieben.

    **Hinweis:**  
    Die beständigen VM-Setupeigenschaften sind nur für einen beständigen MED-V-Arbeitsbereich aktiviert.



3.  Wählen Sie im Menü **Richtlinie** die Option **Commit**aus.

**Beständige VM-Setup Eigenschaften**

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
<td align="left"><p>Ausführen des VM-Setups</p></td>
<td align="left"><p>Aktivieren Sie dieses Kontrollkästchen, um ein Setupskript auszuführen, wenn der MED-V-Arbeitsbereich zum ersten Mal ausgeführt wird.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Skript-Editor</p></td>
<td align="left"><p>Klicken Sie hier, um das Setupskript zu konfigurieren. Weitere Informationen finden Sie unter <a href="how-to-set-up-script-actions.md" data-raw-source="[How to Set Up Script Actions](how-to-set-up-script-actions.md)"> so wird es gemacht: Einrichten von Skriptaktionen </a> .</p>
<div class="alert">
<strong>Hinweis:</strong><br/><p>Diese Schaltfläche ist nur aktiviert <strong> , wenn das VM-Setup Skript ausführen </strong> ausgewählt ist.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p>Meldung, die angezeigt wird, wenn Skript ausgeführt wird</p></td>
<td align="left"><p>Eine Meldung, die angezeigt werden soll, während das Skript ausgeführt wird. Wenn Sie leer bleiben, wird die Standardmeldung angezeigt.</p>
<div class="alert">
<strong>Hinweis:</strong><br/><p>Dieses Feld ist nur aktiviert, wenn das <strong> VM-Setup Skript ausführen aktiviert </strong> ist.</p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



## Konfigurieren der Einrichtung eines virtuellen Computers für einen Revertible MED-V-Arbeitsbereich


**So konfigurieren Sie die Einrichtung eines virtuellen Computers für einen revertible MED-V-Arbeitsbereich**

1.  Klicken Sie auf einen revertible MED-V-Arbeitsbereich, den Sie konfigurieren möchten.

2.  Konfigurieren Sie im Abschnitt **Revertible VM Setup** die Eigenschaften wie in der folgenden Tabelle beschrieben.

    **Hinweis:**  
    Die Setupeigenschaften von revertible VM sind nur für einen revertible MED-V-Arbeitsbereich aktiviert.



3.  Wählen Sie im Menü **Richtlinie** die Option **Commit**aus.

**Revertible-VM-Setup Eigenschaften**

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
<td align="left"><p>Umbenennen des virtuellen Computers basierend auf dem Computernamens Muster</p></td>
<td align="left"><p>Aktivieren Sie dieses Kontrollkästchen, um jedem Computer mit dem Med-v-Arbeitsbereich einen eindeutigen Namen zuzuweisen, damit Sie zwischen mehreren Computern unterscheiden können, die denselben Med-v-Arbeitsbereich verwenden.</p>
<p>Weitere Informationen zum Konfigurieren von Computerabbild Namen finden Sie unter <a href="how-to-configure-vm-computer-name-pattern-propertiesmedvv2.md" data-raw-source="[How to Configure VM Computer Name Pattern Properties](how-to-configure-vm-computer-name-pattern-propertiesmedvv2.md)"> Konfigurieren von VM-Computernamens Mustereigenschaften </a> .</p></td>
</tr>
</tbody>
</table>



## Verwandte Themen


[Über die Benutzeroberfläche der MED-V-Management-Konsole](using-the-med-v-management-console-user-interface.md)

[Erstellen eines MED-V-Arbeitsbereichs](creating-a-med-v-workspacemedv-10-sp1.md)

[Beispiele für VM-Konfigurationen](examples-of-virtual-machine-configurationsv2.md)









