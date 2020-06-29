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
# <span data-ttu-id="fb7e9-103">Registerkarte „Domänendelegierung“</span><span class="sxs-lookup"><span data-stu-id="fb7e9-103">Domain Delegation Tab</span></span>


<span data-ttu-id="fb7e9-104">Die Registerkarte " **Domänendelegierung** " im Bereich " **Änderungssteuerung** " enthält eine Liste der Gruppenrichtlinienadministratoren, die Zugriff auf das Archiv auf Domänenebene haben und die jeweiligen Rollen angeben.</span><span class="sxs-lookup"><span data-stu-id="fb7e9-104">The **Domain Delegation** tab on the **Change Control** pane provides a list of Group Policy administrators who have domain-level access to the archive and indicates the roles of each.</span></span> <span data-ttu-id="fb7e9-105">Auf dieser Registerkarte können AGPM-Administratoren (Vollzugriff) außerdem Berechtigungen auf Domänenebene für Redakteure, genehmigende Personen, Prüfer und andere AGPM-Administratoren konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="fb7e9-105">Additionally, this tab enables AGPM Administrators (Full Control) to configure domain-level permissions for Editors, Approvers, Reviewers, and other AGPM Administrators.</span></span> <span data-ttu-id="fb7e9-106">Auf der Registerkarte " **Domänendelegierung** " gibt es zwei Abschnitte: Konfiguration von e-Mail-Benachrichtigungen und rollenbasierte Delegierung für erweiterte Gruppenrichtlinienverwaltung (AGPM) auf Domänenebene.</span><span class="sxs-lookup"><span data-stu-id="fb7e9-106">There are two sections on the **Domain Delegation** tab—configuration of e-mail notification and role-based delegation for Advanced Group Policy Management (AGPM) at the domain level.</span></span>

## <span data-ttu-id="fb7e9-107">Konfiguration einer e-Mail-Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="fb7e9-107">Configuration of e-mail notification</span></span>


<span data-ttu-id="fb7e9-108">Im Abschnitt e-Mail-Benachrichtigung auf dieser Registerkarte werden die Genehmiger identifiziert, die Benachrichtigungen erhalten, wenn Vorgänge in AGPM ausstehen.</span><span class="sxs-lookup"><span data-stu-id="fb7e9-108">The e-mail notification section of this tab identifies the Approvers that will receive notification when operations are pending in AGPM.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="fb7e9-109">Einstellung</span><span class="sxs-lookup"><span data-stu-id="fb7e9-109">Setting</span></span></th>
<th align="left"><span data-ttu-id="fb7e9-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fb7e9-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="fb7e9-111">Von</span><span class="sxs-lookup"><span data-stu-id="fb7e9-111">From</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="fb7e9-112">Der AGPM-Alias, aus dem Benachrichtigungen an genehmigende Personen gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="fb7e9-112">The AGPM alias from which notification is sent to Approvers.</span></span> <span data-ttu-id="fb7e9-113">In einer Umgebung mit mehreren Domänen kann es sich um denselben Alias in der gesamten Umgebung oder um einen anderen Alias für jede Domäne handeln.</span><span class="sxs-lookup"><span data-stu-id="fb7e9-113">In an environment with multiple domains, this can be the same alias throughout the environment or a different alias for each domain.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="fb7e9-114">Zweck</span><span class="sxs-lookup"><span data-stu-id="fb7e9-114">To</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="fb7e9-115">Eine durch trennzeichengetrennte Liste der e-Mail-Adressen von Genehmigern, an die eine Benachrichtigung gesendet werden soll</span><span class="sxs-lookup"><span data-stu-id="fb7e9-115">A comma-delimited list of e-mail addresses of Approvers to whom notification is to be sent</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="fb7e9-116">SMTP-Server</span><span class="sxs-lookup"><span data-stu-id="fb7e9-116">SMTP server</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="fb7e9-117">Der Name des e-Mail-Servers, beispielsweise Mail.contoso.com</span><span class="sxs-lookup"><span data-stu-id="fb7e9-117">The name of the e-mail server, such as mail.contoso.com</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="fb7e9-118">Benutzername</span><span class="sxs-lookup"><span data-stu-id="fb7e9-118">User name</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="fb7e9-119">Ein Benutzer mit Zugriff auf den SMTP-Server</span><span class="sxs-lookup"><span data-stu-id="fb7e9-119">A user with access to the SMTP server</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="fb7e9-120">Kennwort</span><span class="sxs-lookup"><span data-stu-id="fb7e9-120">Password</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="fb7e9-121">Kennwort des Benutzers für die Authentifizierung beim SMTP-Server</span><span class="sxs-lookup"><span data-stu-id="fb7e9-121">User's password for authentication to the SMTP server</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="fb7e9-122">Passwort bestätigen</span><span class="sxs-lookup"><span data-stu-id="fb7e9-122">Confirm password</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="fb7e9-123">Kennwort des Benutzers bestätigen</span><span class="sxs-lookup"><span data-stu-id="fb7e9-123">Confirm user's password</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="fb7e9-124">Rollenbasierte Delegierung auf Domänenebene</span><span class="sxs-lookup"><span data-stu-id="fb7e9-124">Domain-level role-based delegation</span></span>


<span data-ttu-id="fb7e9-125">Der Abschnitt Rollenbasierte Delegierung auf dieser Registerkarte zeigt an und ermöglicht einem AGPM-Administrator das Delegieren von zulässigen, verweigerten und vererbten Berechtigungen für jede Gruppe und jeden Benutzer in der Domäne mit Zugriff auf das Archiv.</span><span class="sxs-lookup"><span data-stu-id="fb7e9-125">The role-based delegation section of this tab displays and enables an AGPM Administrator to delegate allowed, denied, and inherited permissions for each group and user on the domain with access to the archive.</span></span> <span data-ttu-id="fb7e9-126">Ein AGPM-Administrator kann domänenweite Berechtigungen mithilfe von standardmäßigen AGPM-Rollen (Editor, genehmigende Person, Prüfer und AGPM-Administrator) oder einer benutzerdefinierten Kombination von Berechtigungen für jeden Gruppenrichtlinienadministrator konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="fb7e9-126">An AGPM Administrator can configure domain-wide permissions using either standard AGPM roles (Editor, Approver, Reviewer, and AGPM Administrator) or a customized combination of permissions for each Group Policy administrator.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="fb7e9-127">Button</span><span class="sxs-lookup"><span data-stu-id="fb7e9-127">Button</span></span></th>
<th align="left"><span data-ttu-id="fb7e9-128">Effekt</span><span class="sxs-lookup"><span data-stu-id="fb7e9-128">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="fb7e9-129">Add</span><span class="sxs-lookup"><span data-stu-id="fb7e9-129">Add</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="fb7e9-130">Fügen Sie der Sicherheitsbeschreibung einen neuen Eintrag hinzu.</span><span class="sxs-lookup"><span data-stu-id="fb7e9-130">Add a new entry to the security descriptor.</span></span> <span data-ttu-id="fb7e9-131">Alle Benutzer oder Gruppen in Active Directory können als Gruppenrichtlinienadministratoren hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="fb7e9-131">Any users or groups in Active Directory can be added as Group Policy administrators.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="fb7e9-132">Entfernen</span><span class="sxs-lookup"><span data-stu-id="fb7e9-132">Remove</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="fb7e9-133">Entfernen Sie die ausgewählten Gruppenrichtlinienadministratoren aus der Zugriffssteuerungsliste.</span><span class="sxs-lookup"><span data-stu-id="fb7e9-133">Remove the selected Group Policy administrators from the Access Control List.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="fb7e9-134">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="fb7e9-134">Properties</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="fb7e9-135">Anzeigen der Eigenschaften für die ausgewählten Gruppenrichtlinienadministratoren</span><span class="sxs-lookup"><span data-stu-id="fb7e9-135">Display the properties for the selected Group Policy administrators.</span></span> <span data-ttu-id="fb7e9-136">Die Seite "Eigenschaften" wird für ein Objekt in <strong> Active Directory-Benutzer und-Computer angezeigt </strong> .</span><span class="sxs-lookup"><span data-stu-id="fb7e9-136">The properties page is the same one displayed for an object in <strong>Active Directory User and Computers</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="fb7e9-137">Erweitert</span><span class="sxs-lookup"><span data-stu-id="fb7e9-137">Advanced</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="fb7e9-138">Öffnen Sie den Editor für die <strong> Zugriffssteuerungsliste </strong> .</span><span class="sxs-lookup"><span data-stu-id="fb7e9-138">Open the <strong>Access Control List Editor</strong>.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="fb7e9-139">Weitere Überlegungen</span><span class="sxs-lookup"><span data-stu-id="fb7e9-139">Additional considerations</span></span>

-   <span data-ttu-id="fb7e9-140">Informationen zu Rollen und Berechtigungen, die sich auf bestimmte Aufgaben beziehen, finden Sie unter Ausführen von Aufgaben im Rahmen von [AGPM-Administratoren](performing-agpm-administrator-tasks.md), Ausführen von [Editor Aufgaben](performing-editor-tasks.md), Ausführen von [genehmigenden Aufgaben](performing-approver-tasks.md)und [Ausführen von Aufgaben](performing-reviewer-tasks.md)für Bearbeiter.</span><span class="sxs-lookup"><span data-stu-id="fb7e9-140">For information about roles and permissions related to specific tasks, see the tasks under [Performing AGPM Administrator Tasks](performing-agpm-administrator-tasks.md), [Performing Editor Tasks](performing-editor-tasks.md), [Performing Approver Tasks](performing-approver-tasks.md), and [Performing Reviewer Tasks](performing-reviewer-tasks.md).</span></span>

### <span data-ttu-id="fb7e9-141">Weitere Verweise</span><span class="sxs-lookup"><span data-stu-id="fb7e9-141">Additional references</span></span>

-   [<span data-ttu-id="fb7e9-142">Benutzeroberfläche: Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="fb7e9-142">User Interface: Advanced Group Policy Management</span></span>](user-interface-advanced-group-policy-management.md)

-   [<span data-ttu-id="fb7e9-143">Durchführen von AGPM-Administratoraufgaben</span><span class="sxs-lookup"><span data-stu-id="fb7e9-143">Performing AGPM Administrator Tasks</span></span>](performing-agpm-administrator-tasks.md)

 

 





