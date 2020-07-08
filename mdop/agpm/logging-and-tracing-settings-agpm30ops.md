---
title: Protokollierungs- und Ablaufverfolgungseinstellungen
description: Protokollierungs- und Ablaufverfolgungseinstellungen
author: dansimp
ms.assetid: 858b6fbf-65b4-42fa-95a9-69b04e5734d7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 078bda16b5fcf968d45e0c4890487471105e8c44
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808368"
---
# Protokollierungs- und Ablaufverfolgungseinstellungen


Mit den Einstellungen für administrative Vorlagen für erweiterte Gruppenrichtlinienverwaltung (AGPM) können Sie die Protokollierungs-und Ablaufverfolgungsoptionen für AGPM-Server und-Clients zentral konfigurieren, auf die ein Gruppenrichtlinienobjekt (GPO) mit diesen Einstellungen angewendet wird.

Die folgende Einstellung ist unter Computer Configuration\\Policies\\Administrative Templates\\Windows Components\\AGPM beim Bearbeiten eines Gruppenrichtlinienobjekts verfügbar.

**Speicherort der Ablaufverfolgungsdatei**:

-   Client:%localappdata%\\Microsoft\\AGPM\\agpm.log

-   Server:%ProgramData%\\Microsoft\\AGPM\\agpmserv.log

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
<td align="left"><p><strong>AGPM: Konfigurieren der Protokollierung</strong></p></td>
<td align="left"><p>Mit dieser Richtlinieneinstellung können Sie die Protokollierung für AGPM aktivieren und konfigurieren. Diese Einstellung wirkt sich auf Client-und Server Komponenten von AGPM aus.</p></td>
</tr>
</tbody>
</table>

 

### Weitere Verweise

-   [Ordner „Administrative Vorlagen“](administrative-templates-folder-agpm30ops.md)

 

 





