---
title: Prüfliste für die Bereitstellung von MBAM 1.0
description: Prüfliste für die Bereitstellung von MBAM 1.0
author: dansimp
ms.assetid: 7e00be23-36a0-4b0f-8663-3c4f2c71546d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 96725183af2cb4e3d86d3f42973452c598497773
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804301"
---
# Prüfliste für die Bereitstellung von MBAM 1.0


Diese Checkliste dient zur Vereinfachung der Bereitstellung von Microsoft BitLocker-Verwaltung und-Überwachung (MBAM).

**Hinweis:**  
In dieser Checkliste werden die empfohlenen Schritte sowie eine Liste der Elemente auf höherer Ebene erläutert, die beim Bereitstellen der MBAM-Features berücksichtigt werden sollten. Wir empfehlen, dass Sie diese Checkliste in ein Kalkulationstabellenprogramm kopieren und für Ihre speziellen Anforderungen anpassen.



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
<td align="left"><p>Führen Sie die Planungsphase aus, um die Computing-Umgebung für die MBAM-Bereitstellung vorzubereiten.</p></td>
<td align="left"><p><a href="mbam-10-planning-checklist.md" data-raw-source="[MBAM 1.0 Planning Checklist](mbam-10-planning-checklist.md)">Prüfliste für die Planung von MBAM 1.0</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Überprüfen Sie die Informationen zu MBAM-unterstützten Konfigurationen, um sicherzustellen, dass Ihre ausgewählten Client-und Server Computer für die MBAM-Feature-Installation unterstützt werden.</p></td>
<td align="left"><p><a href="mbam-10-supported-configurations.md" data-raw-source="[MBAM 1.0 Supported Configurations](mbam-10-supported-configurations.md)">Von MBAM 1.0 unterstützte Konfigurationen</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Führen Sie MBAM-Setup aus, um die MBAM-Server Features in der folgenden Reihenfolge bereitzustellen:</p>
<ol>
<li><p>Wiederherstellungs-und Hardware Datenbank</p></li>
<li><p>Kompatibilitäts Status-Datenbank</p></li>
<li><p>Konformitätsprüfung und Berichte</p></li>
<li><p>Verwaltungs-und Überwachungs Server</p></li>
<li><p>MBAM-Gruppenrichtlinienvorlage</p></li>
</ol>
<div class="alert">
<strong>Hinweis:</strong><br/><p>Verfolgen Sie die Namen der Server, auf denen die einzelnen Features installiert sind. Sie werden diese Informationen während des Installationsvorgangs verwenden.</p>
</div>
<div>

</div></td>
<td align="left"><p><a href="deploying-the-mbam-10-server-infrastructure.md" data-raw-source="[Deploying the MBAM 1.0 Server Infrastructure](deploying-the-mbam-10-server-infrastructure.md)">Bereitstellen der Serverinfrastruktur von MBAM 1.0</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Hinzufügen von Sicherheitsgruppen für Active Directory-Domänendienste, die während der Planungsphase erstellt wurden, zu den entsprechenden lokalen MBAM Server Feature-Administratoren Gruppen auf den entsprechenden Servern.</p></td>
<td align="left"><p><a href="planning-for-mbam-10-administrator-roles.md" data-raw-source="[Planning for MBAM 1.0 Administrator Roles](planning-for-mbam-10-administrator-roles.md)">Planen von MBAM 1,0-Administratorrollen </a> und <a href="how-to-manage-mbam-administrator-roles-mbam-1.md" data-raw-source="[How to Manage MBAM Administrator Roles](how-to-manage-mbam-administrator-roles-mbam-1.md)"> Verwalten von MBAM-Administratorrollen</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Erstellen und Bereitstellen der erforderlichen MBAM-Gruppenrichtlinienobjekte</p></td>
<td align="left"><p><a href="deploying-mbam-10-group-policy-objects.md" data-raw-source="[Deploying MBAM 1.0 Group Policy Objects](deploying-mbam-10-group-policy-objects.md)">Bereitstellen von Gruppenrichtlinienobjekten für MBAM 1.0</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Bereitstellen der MBAM-Client Software.</p></td>
<td align="left"><p><a href="deploying-the-mbam-10-client.md" data-raw-source="[Deploying the MBAM 1.0 Client](deploying-the-mbam-10-client.md)">Bereitstellen des MBAM 1.0-Clients</a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



## Verwandte Themen


[Bereitstellen von MBAM 1.0](deploying-mbam-10.md)









