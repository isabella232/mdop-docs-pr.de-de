---
title: Prüfliste für die Installationsvorbereitung von App-V
description: Prüfliste für die Installationsvorbereitung von App-V
author: dansimp
ms.assetid: 3af609b1-2c09-4edb-b083-b913b6d5e8c4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 70e71d3dea02daeadedb4cff78c58302ac743dda
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808047"
---
# Prüfliste für die Installationsvorbereitung von App-V


Die folgende Checkliste dient dazu, eine Liste der allgemeinen Elemente zu erstellen, die Sie berücksichtigen sollten, und beschreibt die Schritte, die Sie vor der Installation der Microsoft Application Virtualization (App-V)-Server ausführen sollten.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Schritt</th>
<th align="left">Verweis</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Stellen Sie sicher, dass Ihre Computerumgebung die unterstützten Konfigurationen erfüllt, die für App-V erforderlich sind.</p></td>
<td align="left"><p><a href="application-virtualization-deployment-requirements.md" data-raw-source="[Application Virtualization Deployment Requirements](application-virtualization-deployment-requirements.md)">Bereitstellungsanforderungen für Application Virtualization</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Konfigurieren Sie die erforderlichen Active Directory-Gruppen und-Konten.</p></td>
<td align="left"><p><a href="configuring-prerequisite-groups-in-active-directory-for-app-v.md" data-raw-source="[Configuring Prerequisite Groups in Active Directory for App-V](configuring-prerequisite-groups-in-active-directory-for-app-v.md)">Konfigurieren von erforderlichen Gruppen in Active Directory für App-V</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Konfigurieren Sie die Einstellungen für Internet Informationsdienste (IIS) auf dem Server, auf dem IIS ausgeführt wird.</p></td>
<td align="left"><p><a href="how-to-configure-windows-server-2008-for-app-v-management-servers.md" data-raw-source="[How to Configure Windows Server 2008 for App-V Management Servers](how-to-configure-windows-server-2008-for-app-v-management-servers.md)">Konfigurieren von Windows Server 2008 für App-V Management Server</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Konfigurieren Sie den Server, auf dem IIS ausgeführt wird, für die Delegierung als vertrauenswürdig.</p>
<div class="alert">
<strong>Hinweis:</strong><br/><p>Dies ist nur erforderlich, wenn Sie den App-v-Verwaltungs Server mithilfe einer verteilten Systemarchitektur installieren, das heißt, wenn Sie die APP-v-Verwaltungskonsole, den Verwaltungs-Webdienst und die Datenbank auf unterschiedlichen Computern installieren.</p>
</div>
<div>

</div></td>
<td align="left"><p><a href="how-to-configure-the-server-to-be-trusted-for-delegation.md" data-raw-source="[How to Configure the Server to be Trusted for Delegation](how-to-configure-the-server-to-be-trusted-for-delegation.md)">So konfigurieren Sie den Server, damit ihm für Delegierungszwecke vertraut wird</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Installieren Sie Microsoft SQL Server 2008.</p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=181924" data-raw-source="[Install SQL Server 2008](https://go.microsoft.com/fwlink/?LinkId=181924)">Installieren Sie SQL Server 2008 </a> ( <a href="https://go.microsoft.com/fwlink/?LinkId=181924" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=181924"> https://go.microsoft.com/fwlink/?LinkId=181924 </a> ).</p></td>
</tr>
</tbody>
</table>



## Verwandte Themen


[Bereitstellung und Upgrade von Application Virtualization](application-virtualization-deployment-and-upgrade-checklists.md)

[Prüfliste für die App-V-Installation](app-v-installation-checklist.md)









