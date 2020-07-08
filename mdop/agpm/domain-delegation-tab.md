---
title: Registerkarte „Domänendelegierung“
description: Registerkarte „Domänendelegierung“
author: dansimp
ms.assetid: 15a9bfff-e25b-4b62-9ebc-521a5f4eae96
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d49083bcefe6c7edcb3a95dc63d2249826d50327
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807583"
---
# Registerkarte „Domänendelegierung“


Die Registerkarte " **Domänendelegierung** " im Bereich " **Änderungssteuerung** " enthält eine Liste der Gruppenrichtlinienadministratoren, die Zugriff auf das Archiv auf Domänenebene haben und die jeweiligen Rollen angeben. Auf dieser Registerkarte können AGPM-Administratoren (Vollzugriff) außerdem Berechtigungen auf Domänenebene für Redakteure, genehmigende Personen, Prüfer und andere AGPM-Administratoren konfigurieren. Auf der Registerkarte " **Domänendelegierung** " gibt es zwei Abschnitte: Konfiguration von e-Mail-Benachrichtigungen und rollenbasierte Delegierung für erweiterte Gruppenrichtlinienverwaltung (AGPM) auf Domänenebene.

## Konfiguration einer e-Mail-Benachrichtigung


Im Abschnitt e-Mail-Benachrichtigung auf dieser Registerkarte werden die Genehmiger identifiziert, die Benachrichtigungen erhalten, wenn Vorgänge in AGPM ausstehen.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Einstellung</th>
<th align="left">Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Von</strong></p></td>
<td align="left"><p>Der AGPM-Alias, aus dem Benachrichtigungen an genehmigende Personen gesendet werden. In einer Umgebung mit mehreren Domänen kann es sich um denselben Alias in der gesamten Umgebung oder um einen anderen Alias für jede Domäne handeln.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Zweck</strong></p></td>
<td align="left"><p>Eine durch trennzeichengetrennte Liste der e-Mail-Adressen von Genehmigern, an die eine Benachrichtigung gesendet werden soll</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>SMTP-Server</strong></p></td>
<td align="left"><p>Der Name des e-Mail-Servers, beispielsweise Mail.contoso.com</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Benutzername</strong></p></td>
<td align="left"><p>Ein Benutzer mit Zugriff auf den SMTP-Server</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Kennwort</strong></p></td>
<td align="left"><p>Kennwort des Benutzers für die Authentifizierung beim SMTP-Server</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Passwort bestätigen</strong></p></td>
<td align="left"><p>Kennwort des Benutzers bestätigen</p></td>
</tr>
</tbody>
</table>

 

## Rollenbasierte Delegierung auf Domänenebene


Der Abschnitt Rollenbasierte Delegierung auf dieser Registerkarte zeigt an und ermöglicht einem AGPM-Administrator das Delegieren von zulässigen, verweigerten und vererbten Berechtigungen für jede Gruppe und jeden Benutzer in der Domäne mit Zugriff auf das Archiv. Ein AGPM-Administrator kann domänenweite Berechtigungen mithilfe von standardmäßigen AGPM-Rollen (Editor, genehmigende Person, Prüfer und AGPM-Administrator) oder einer benutzerdefinierten Kombination von Berechtigungen für jeden Gruppenrichtlinienadministrator konfigurieren.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Button</th>
<th align="left">Effekt</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Add</strong></p></td>
<td align="left"><p>Fügen Sie der Sicherheitsbeschreibung einen neuen Eintrag hinzu. Alle Benutzer oder Gruppen in Active Directory können als Gruppenrichtlinienadministratoren hinzugefügt werden.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Entfernen</strong></p></td>
<td align="left"><p>Entfernen Sie die ausgewählten Gruppenrichtlinienadministratoren aus der Zugriffssteuerungsliste.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Eigenschaften</strong></p></td>
<td align="left"><p>Anzeigen der Eigenschaften für die ausgewählten Gruppenrichtlinienadministratoren Die Seite "Eigenschaften" wird für ein Objekt in <strong> Active Directory-Benutzer und-Computer angezeigt </strong> .</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Erweitert</strong></p></td>
<td align="left"><p>Öffnen Sie den Editor für die <strong> Zugriffssteuerungsliste </strong> .</p></td>
</tr>
</tbody>
</table>

 

### Weitere Überlegungen

-   Informationen zu Rollen und Berechtigungen, die sich auf bestimmte Aufgaben beziehen, finden Sie unter Ausführen von Aufgaben im Rahmen von [AGPM-Administratoren](performing-agpm-administrator-tasks.md), Ausführen von [Editor Aufgaben](performing-editor-tasks.md), Ausführen von [genehmigenden Aufgaben](performing-approver-tasks.md)und [Ausführen von Aufgaben](performing-reviewer-tasks.md)für Bearbeiter.

### Weitere Verweise

-   [Benutzeroberfläche: Advanced Group Policy Management](user-interface-advanced-group-policy-management.md)

-   [Durchführen von AGPM-Administratoraufgaben](performing-agpm-administrator-tasks.md)

 

 





