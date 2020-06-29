---
title: AGPM Server-Verbindungseinstellungen
description: AGPM Server-Verbindungseinstellungen
author: dansimp
ms.assetid: cc67f122-6309-4820-92c2-f6a27d897123
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 55bd5c04f573a421674068bea6fc9c6adcd29a12
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804523"
---
# AGPM Server-Verbindungseinstellungen


Sie können die Einstellungen für administrative Vorlagen für die erweiterte Gruppenrichtlinienverwaltung (Group Policy Management, AGPM) verwenden, um AGPM-Server Verbindungen für Gruppenrichtlinienadministratoren zentral zu konfigurieren, denen ein Gruppenrichtlinienobjekt (GPO) mit diesen Einstellungen zugewiesen ist.

Die folgenden Einstellungen stehen unter Benutzer Configuration\\Policies\\Administrative Templates\\Windows Components\\AGPM beim Bearbeiten eines Gruppenrichtlinienobjekts zur Verfügung.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Einstellung</th>
<th align="left">Effekt</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>AGPM: Angeben des standardmäßigen AGPM-Servers (alle Domänen)</strong></p></td>
<td align="left"><p>Mit dieser Richtlinieneinstellung können Sie einen standardmäßigen AGPM-Server für alle Domänen angeben. Dieser wird nur von AGPM-Clients verwendet und schränkt Gruppenrichtlinienadministratoren ein, eine Verbindung mit einem anderen Archiv herzustellen. Sie können diesen Standardwert für einzelne Domänen mithilfe der AGPM <strong> : Angeben von AGPM-Servereinstellungen außer Kraft setzen </strong> .</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>AGPM: Angeben von AGPM-Servern</strong></p></td>
<td align="left"><p>Mit dieser Richtlinieneinstellung können Sie die AGPM-Server für einzelne Domänen angeben. Dieser wird nur von AGPM-Clients verwendet und schränkt Gruppenrichtlinienadministratoren ein, die Verbindung zu einem anderen Archiv für die angegebene Domäne herzustellen. Wenn Sie einen standardmäßigen AGPM-Server angeben möchten, verwenden Sie die <strong> Einstellung AGPM: standardmäßiger AGPM-Server (alle Domänen) angeben, </strong> und verwenden Sie diese Richtlinieneinstellung, um den Standardwert pro Domäne zu überschreiben.</p></td>
</tr>
</tbody>
</table>

 

### Weitere Verweise

-   [Ordner „Administrative Vorlagen“](administrative-templates-folder-agpm40.md)

-   [Durchführen von AGPM-Administratoraufgaben](performing-agpm-administrator-tasks-agpm40.md)

 

 





