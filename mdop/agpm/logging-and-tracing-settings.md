---
title: Protokollierungs- und Ablaufverfolgungseinstellungen
description: Protokollierungs- und Ablaufverfolgungseinstellungen
author: dansimp
ms.assetid: db6b43c7-fdde-4d11-b5ab-a81346e56940
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: bef0f8367647aad688c2aec7586ecdaae2e22143
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808367"
---
# Protokollierungs- und Ablaufverfolgungseinstellungen


Mit den Einstellungen für administrative Vorlagen für erweiterte Gruppenrichtlinienverwaltung (AGPM) können Sie die Protokollierungs-und Ablaufverfolgungsoptionen für AGPM-Server und-Clients zentral konfigurieren, auf die ein Gruppenrichtlinienobjekt (GPO) mit diesen Einstellungen angewendet wird.

Die folgende Einstellung ist unter Computer Configuration\\Administrative Templates\\Windows Components\\AGPM im **Gruppenrichtlinienobjekt-Editor** verfügbar, wenn Sie ein GPO in der Gruppenrichtlinien-Verwaltungskonsole (Group Policy Management Console, GPMC) bearbeiten. Wenn dieser Pfad nicht angezeigt wird, klicken Sie mit der rechten Maustaste auf **Administrative Vorlagen**, und fügen Sie die Vorlage AGPM. ADMX oder AGPM. adm hinzu.

**Speicherort der Ablaufverfolgungsdatei**:

-   Client:%localappdata%\\Microsoft\\AGPM\\agpm.log

-   Server:%CommonAppData%\\Microsoft\\AGPM\\agpmserv.log

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
<td align="left"><p><strong>AGPM-Protokollierung</strong></p></td>
<td align="left"><p>Wenn diese Option aktiviert ist, wird mit dieser Einstellung konfiguriert, ob die Ablaufverfolgung aktiviert ist und wie detailliert die Detailebene ist. Diese Einstellung wirkt sich auf Client-und Server Komponenten von AGPM aus.</p>
<p>Wenn diese Einstellung deaktiviert oder nicht konfiguriert ist, hat dies keine Auswirkungen.</p></td>
</tr>
</tbody>
</table>

 

### Weitere Verweise

-   [Einstellungen für administrative Vorlagen](administrative-template-settings.md)

 

 





