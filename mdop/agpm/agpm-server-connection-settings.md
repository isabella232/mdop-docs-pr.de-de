---
title: AGPM Server-Verbindungseinstellungen
description: AGPM Server-Verbindungseinstellungen
author: dansimp
ms.assetid: faf78e5b-2b0d-4069-9b8c-910add892200
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d63163de0a1adf744e6d442b8073e5b32352ed67
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804664"
---
# AGPM Server-Verbindungseinstellungen


Sie können die Einstellungen für administrative Vorlagen für die erweiterte Gruppenrichtlinienverwaltung (Group Policy Management, AGPM) verwenden, um AGPM-Server Verbindungen für Gruppenrichtlinienadministratoren zentral zu konfigurieren, denen ein Gruppenrichtlinienobjekt (GPO) mit diesen Einstellungen zugewiesen ist.

Die folgenden Einstellungen stehen unter Benutzer Configuration\\Administrative Templates\\Windows Components\\AGPM beim Bearbeiten eines Gruppenrichtlinienobjekts zur Verfügung. Wenn dieser Pfad nicht angezeigt wird, klicken Sie mit der rechten Maustaste auf **Administrative Vorlagen**, und fügen Sie die Vorlage AGPM. ADMX oder AGPM. adm hinzu.

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
<td align="left"><p><strong>AGPM-Server (alle Domänen)</strong></p></td>
<td align="left"><p>Wenn diese Option aktiviert ist, konfiguriert diese Einstellung zentral eine AGPM-Serververbindung für die Verwendung durch alle Domänen und deaktiviert die Einstellungen auf der <strong> Registerkarte AGPM-Server </strong> für Gruppenrichtlinienadministratoren. Konfigurieren Sie für mehrere AGPM-Server diese Einstellung mit einem Standardserver, und konfigurieren <strong> Sie dann die Einstellung AGPM-Server </strong> in der administrativen Vorlage, um diesen Server für andere Domänen zu überschreiben.</p>
<p>Wenn diese Option deaktiviert oder nicht konfiguriert ist, muss jeder Gruppenrichtlinienadministrator den AGPM-Server auswählen, der für jede Domäne auf der <strong> </strong> Registerkarte AGPM-Server in AGPM angezeigt werden soll.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>AGPM-Server</strong></p></td>
<td align="left"><p>Wenn diese Einstellung aktiviert ist, werden mehrere domänenspezifische AGPM-Server zentral konfiguriert, wobei die <strong> Einstellung AGPM-Server (alle Domänen) </strong> in der administrativen Vorlage überschrieben wird. Wenn für Ihre Umgebung nur ein einzelner AGPM-Server erforderlich ist, verwenden Sie <strong> </strong> in der administrativen Vorlage nur die Einstellung AGPM-Server (alle Domänen).</p>
<p>Wenn diese Option deaktiviert oder nicht konfiguriert ist, wird <strong> mit der Einstellung AGPM-Server (alle Domänen) </strong> in der administrativen Vorlage die AGPM-Serververbindung konfiguriert.</p></td>
</tr>
</tbody>
</table>

 

### Weitere Verweise

-   [Einstellungen für administrative Vorlagen](administrative-template-settings.md)

-   [Durchführen von AGPM-Administratoraufgaben](performing-agpm-administrator-tasks.md)

 

 





