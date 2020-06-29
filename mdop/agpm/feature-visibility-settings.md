---
title: Sichtbarkeitseinstellungen für Features
description: Sichtbarkeitseinstellungen für Features
author: dansimp
ms.assetid: 9db2ba03-fb75-4f95-9138-ec89b9fc8d01
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 26f19895d0a9163885779688ba7d89f6d16f2a17
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808455"
---
# Sichtbarkeitseinstellungen für Features


Mit den Einstellungen für administrative Vorlagen für die erweiterte Gruppenrichtlinienverwaltung (Group Policy Management, AGPM) können Sie die Sichtbarkeit des Knotens " **Änderungssteuerung** " und der Registerkarte " **Verlauf** " für Gruppenrichtlinienadministratoren zentral konfigurieren, denen ein Gruppenrichtlinienobjekt (GPO) mit diesen Einstellungen zugewiesen ist.

Die folgenden Einstellungen sind unter Benutzer Configuration\\Administrative Templates\\Windows Components\\Microsoft-Verwaltungskonsole \ \ eingeschränkte/zulässige Snap-ins\\Extension-Snap-Ins im **Gruppenrichtlinienobjekt-Editor** verfügbar, wenn Sie ein GPO in der Gruppenrichtlinien-Verwaltungskonsole (Group Policy Management Console, GPMC) bearbeiten. Wenn dieser Pfad nicht angezeigt wird, klicken Sie mit der rechten Maustaste auf **Administrative Vorlagen**, und fügen Sie die Vorlage AGPM. ADMX oder AGPM. adm hinzu.

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
<td align="left"><p><strong>AGPM-Änderungs Steuerelement</strong></p></td>
<td align="left"><p>Wenn aktiviert oder nicht konfiguriert, <strong> ist der Knoten Change Control </strong> in der GPMC sichtbar.</p>
<p>Wenn diese Option deaktiviert <strong> ist, </strong> ist der Knoten Change Control in der GPMC nicht sichtbar.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>AGPM-Link Erweiterung</strong></p></td>
<td align="left"><p>Wenn diese Option aktiviert oder nicht konfiguriert ist, <strong> </strong> wird in der GPMC für jedes verknüpfte Gruppenrichtlinienobjekt die Registerkarte Verlauf angezeigt.</p>
<p>Wenn diese Option deaktiviert <strong> </strong> ist, ist die Registerkarte Verlauf für verknüpfte GPOs nicht sichtbar.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>AGPM-GPO-Erweiterung</strong></p></td>
<td align="left"><p>Wenn diese Option aktiviert oder nicht konfiguriert ist, <strong> </strong> wird in der GPMC für jedes GPO eine Verlaufs Registerkarte angezeigt.</p>
<p>Wenn diese Option deaktiviert <strong> </strong> ist, ist die Registerkarte Verlauf für GPOs nicht sichtbar.</p></td>
</tr>
</tbody>
</table>

 

### Weitere Verweise

-   [Einstellungen für administrative Vorlagen](administrative-template-settings.md)

 

 





