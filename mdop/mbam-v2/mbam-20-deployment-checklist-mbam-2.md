---
title: Prüfliste für die Bereitstellung von MBAM 2.0
description: Prüfliste für die Bereitstellung von MBAM 2.0
author: dansimp
ms.assetid: 7905d31d-f21c-4683-b9c4-95b815e08fab
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5d8d0ce1a3ff48d4bf2f84e61b4a578b170264a0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811755"
---
# Prüfliste für die Bereitstellung von MBAM 2.0


Diese Checkliste kann verwendet werden, um Sie während der Microsoft BitLocker-MBAM-Bereitstellung mit einer eigenständigen Topologie zu unterstützen.

**Hinweis:**  
In dieser Checkliste werden die empfohlenen Schritte und eine Liste der Elemente auf höherer Ebene erläutert, die beim Bereitstellen von Microsoft BitLocker-Verwaltungs-und-Überwachungsfeatures berücksichtigt werden sollten. Es wird empfohlen, dass Sie diese Checkliste in ein Kalkulationstabellenprogramm kopieren und für ihre Verwendung anpassen.



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
<td align="left"><p><a href="mbam-20-planning-checklist-mbam-2.md" data-raw-source="[MBAM 2.0 Planning Checklist](mbam-20-planning-checklist-mbam-2.md)">Prüfliste für die Planung von MBAM 2.0</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Überprüfen Sie die MBAM unterstützten Konfigurationsinformationen, um sicherzustellen, dass ausgewählte Client-und Server Computer für die MBAM-Feature-Installation unterstützt werden.</p></td>
<td align="left"><p><a href="mbam-20-supported-configurations-mbam-2.md" data-raw-source="[MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md)">Von MBAM 2.0 unterstützte Konfigurationen</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Führen Sie MBAM-Setup aus, um die MBAM-Server Features in der folgenden Reihenfolge bereitzustellen:</p>
<ol>
<li><p>Wiederherstellungsdatenbank</p></li>
<li><p>Konformitäts-und Überwachungsdatenbank</p></li>
<li><p>Konformitätsprüfung und Berichte</p></li>
<li><p>Self-Service-Server</p></li>
<li><p>Verwaltungs-und Überwachungs Server</p></li>
<li><p>MBAM-Gruppenrichtlinienvorlage</p></li>
</ol>
<div class="alert">
<strong>Hinweis:</strong><br/><p>Verfolgen Sie die Namen der Server, auf denen die einzelnen Features installiert sind. Diese Informationen werden während des Installationsvorgangs verwendet.</p>
</div>
<div>

</div></td>
<td align="left"><p><a href="deploying-the-mbam-20-server-infrastructure-mbam-2.md" data-raw-source="[Deploying the MBAM 2.0 Server Infrastructure](deploying-the-mbam-20-server-infrastructure-mbam-2.md)">Bereitstellen der Serverinfrastruktur von MBAM 2.0</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Hinzufügen von Sicherheitsgruppen für Active Directory-Domänendienste, die während der Planungsphase erstellt wurden, zu den entsprechenden lokalen MBAM Server Feature-Administratoren Gruppen auf den entsprechenden Servern.</p></td>
<td align="left"><p><a href="planning-for-mbam-20-administrator-roles-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Administrator Roles](planning-for-mbam-20-administrator-roles-mbam-2.md)">Planen von MBAM 2,0-Administratorrollen </a> und <a href="how-to-manage-mbam-administrator-roles-mbam-2.md" data-raw-source="[How to Manage MBAM Administrator Roles](how-to-manage-mbam-administrator-roles-mbam-2.md)"> Verwalten von MBAM-Administratorrollen</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Erstellen und Bereitstellen erforderlicher MBAM-Gruppenrichtlinienobjekte</p></td>
<td align="left"><p><a href="deploying-mbam-20-group-policy-objects-mbam-2.md" data-raw-source="[Deploying MBAM 2.0 Group Policy Objects](deploying-mbam-20-group-policy-objects-mbam-2.md)">Bereitstellen von Gruppenrichtlinienobjekten für MBAM 2.0</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Bereitstellen der MBAM-Client Software.</p></td>
<td align="left"><p><a href="deploying-the-mbam-20-client-mbam-2.md" data-raw-source="[Deploying the MBAM 2.0 Client](deploying-the-mbam-20-client-mbam-2.md)">Bereitstellen des MBAM 2.0-Clients</a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



## Verwandte Themen


[Bereitstellen von MBAM 2.0](deploying-mbam-20-mbam-2.md)









