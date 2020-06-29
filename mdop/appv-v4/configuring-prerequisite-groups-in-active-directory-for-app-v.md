---
title: Konfigurieren von erforderlichen Gruppen in Active Directory für App-V
description: Konfigurieren von erforderlichen Gruppen in Active Directory für App-V
author: dansimp
ms.assetid: 0010d534-46c0-44a3-b5c1-621b4d5e2c31
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: aa1ab6393dee20203b715311d4e1dfdc4c22c679
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809010"
---
# Konfigurieren von erforderlichen Gruppen in Active Directory für App-V


Bevor Sie den Microsoft Application Virtualization (App-V)-Verwaltungs Server installieren, müssen Sie die folgenden Objekte in Active Directory erstellen. App-V verwendet Active Directory-Gruppen, um den Zugriff auf Anwendungen und administrative Funktionen zu steuern. Sie werden diese Gruppen während des Server Installationsvorgangs und beim Veröffentlichen von Anwendungen verwenden.

## Konfigurieren von erforderlichen Gruppen in Active Directory für Application Virtualization


In dieser Tabelle sind die Active Directory-Gruppen aufgeführt, die für die Installation von App-V erforderlich sind.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Objekt</th>
<th align="left">Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Organisationseinheit (OU)</p></td>
<td align="left"><p>Erstellen Sie eine OU in Active Directory für die speziellen Gruppen, die für App-V erforderlich sind.</p></td>
</tr>
<tr class="even">
<td align="left"><p>App-V-administrative Gruppe</p></td>
<td align="left"><p>Während der Installation des App-v-Verwaltungsservers müssen Sie eine Active Directory-Gruppe auswählen, die als App-v-Administratorgruppe verwendet werden soll, um den administrativen Zugriff auf die Verwaltungskonsole zu steuern. Erstellen Sie eine Sicherheitsgruppe für App-V-Administratoren, und fügen Sie dieser Gruppe alle Benutzer hinzu, die die Verwaltungskonsole verwenden müssen. Sie können diese Gruppe nicht direkt über das App-V Management Server-Installationsprogramm erstellen.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>App-V-Benutzergruppe</p></td>
<td align="left"><p>App-v setzt voraus, dass jedes Benutzerkonto, das auf App-v-Funktionen zugreift, Mitglied einer Anbieterrichtlinie ist, die einer einzelnen Gruppe für den allgemeinen Platt Form Zugriff zugeordnet ist. Verwenden einer vorhandenen Gruppe beispielsweise Domänenbenutzer, wenn alle Benutzer Zugriff auf App-V haben oder eine neue Gruppe erstellen möchten.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Anwendungsgruppen</p></td>
<td align="left"><p>App-V ordnet das Recht zur Verwendung einer einzelnen Anwendung mit einer Active Directory-Gruppe zu. Erstellen Sie für jede Anwendung eine Active Directory-Gruppe, und weisen Sie Benutzer diesen Gruppen nach Bedarf zu, um den Benutzer Zugriff auf die Anwendungen zu kontrollieren.</p></td>
</tr>
</tbody>
</table>

 

## Verwandte Themen


[Bereitstellungsanforderungen für Application Virtualization](application-virtualization-deployment-requirements.md)

[Konfigurieren von Windows Server 2008 für App-V Management Server](how-to-configure-windows-server-2008-for-app-v-management-servers.md)

 

 





