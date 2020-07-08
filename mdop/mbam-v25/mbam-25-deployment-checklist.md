---
title: Prüfliste für die Bereitstellung von MBAM 2.5
description: Prüfliste für die Bereitstellung von MBAM 2.5
author: dansimp
ms.assetid: 2ba7de17-e3a4-4798-99e0-cd1dc28c5b76
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 11609b3d6d44d62b032e35005e5d967ca6d4e83b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809592"
---
# Prüfliste für die Bereitstellung von MBAM 2.5


Sie können diese Checkliste verwenden, um Sie bei der Bereitstellung von Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) mit einer eigenständigen Topologie zu unterstützen.

**Hinweis:**  
In dieser Checkliste werden die empfohlenen Schritte und eine Liste der Elemente auf höherer Ebene erläutert, die beim Bereitstellen von Microsoft BitLocker-Verwaltungs-und-Überwachungsfeatures berücksichtigt werden sollten. Wir empfehlen, dass Sie diese Checkliste in ein Kalkulationstabellenprogramm kopieren und für ihre Verwendung anpassen.



<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left">Aufgabe</th>
<th align="left">Verweise</th>
<th align="left">Anmerkungen</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Überprüfen und vervollständigen Sie alle Planungsschritte zum Vorbereiten Ihrer Umgebung für die MBAM-Bereitstellung.</p></td>
<td align="left"><p><a href="mbam-25-planning-checklist.md" data-raw-source="[MBAM 2.5 Planning Checklist](mbam-25-planning-checklist.md)">Prüfliste für die Planung von MBAM 2.5</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Überprüfen Sie die unterstützten Konfigurationsinformationen, um sicherzustellen, dass MBAM die ausgewählten Client-und Server Computer unterstützt.</p></td>
<td align="left"><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)">Von MBAM 2.5 unterstützte Konfigurationen</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Installieren Sie die MBAM-Server Software.</p></td>
<td align="left"><p><a href="installing-the-mbam-25-server-software.md" data-raw-source="[Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md)">Installieren der MBAM 2.5-Serversoftware</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Konfigurieren Sie die MBAM-Server Features:</p>
<ul>
<li><p>Compliance-und Audit-Datenbank und Wiederherstellungsdatenbank</p></li>
<li><p>Berichte</p></li>
<li><p>Web Applications</p></li>
<li><p>Configuration Manager-Integrations Topologie (nur erforderlich, wenn Sie MBAM mit dieser Topologie ausführen)</p></li>
</ul>
<div class="alert">
<strong>Hinweis:</strong><br/><p>Notieren Sie die Namen der Server, auf denen Sie die einzelnen Features konfigurieren. Diese Informationen werden während des gesamten Konfigurationsprozesses verwendet.</p>
</div>
<div>

</div></td>
<td align="left"><p><a href="configuring-the-mbam-25-server-features.md" data-raw-source="[Configuring the MBAM 2.5 Server Features](configuring-the-mbam-25-server-features.md)">Konfigurieren der MBAM 2.5-Serverfunktionen</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Überprüfen Sie die MBAM-Konfiguration.</p></td>
<td align="left"><p><a href="validating-the-mbam-25-server-feature-configuration.md" data-raw-source="[Validating the MBAM 2.5 Server Feature Configuration](validating-the-mbam-25-server-feature-configuration.md)">Überprüfen der Konfiguration von MBAM 2.5 Serverfunktionen</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Kopieren Sie die MBAM-Gruppenrichtlinienvorlage, und bearbeiten Sie die Gruppenrichtlinieneinstellungen.</p></td>
<td align="left"><p><a href="copying-the-mbam-25-group-policy-templates.md" data-raw-source="[Copying the MBAM 2.5 Group Policy Templates](copying-the-mbam-25-group-policy-templates.md)">Kopieren der MBAM 2,5-Gruppenrichtlinienvorlagen </a> und <a href="editing-the-mbam-25-group-policy-settings.md" data-raw-source="[Editing the MBAM 2.5 Group Policy Settings](editing-the-mbam-25-group-policy-settings.md)"> Bearbeiten der MBAM 2,5-Gruppenrichtlinieneinstellungen</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Bereitstellen der MBAM-Client Software.</p></td>
<td align="left"><p><a href="deploying-the-mbam-25-client.md" data-raw-source="[Deploying the MBAM 2.5 Client](deploying-the-mbam-25-client.md)">Bereitstellen des MBAM 2.5-Clients</a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>




## Verwandte Themen


[Bereitstellen von MBAM 2.5](deploying-mbam-25.md)




## Sie haben einen Vorschlag für MBAM?
- [Hier](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)können Sie Vorschläge hinzufügen oder abstimmen. 
- Bei MBAM-Problemen verwenden Sie das [MBAM TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).




