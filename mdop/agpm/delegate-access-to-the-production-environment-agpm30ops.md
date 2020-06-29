---
title: Delegieren des Zugriffs auf die Produktionsumgebung
description: Delegieren des Zugriffs auf die Produktionsumgebung
author: dansimp
ms.assetid: c1ebae2e-909b-4e64-b368-b7d3cc67b1eb
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4667a23f1584d7aab6143860721e326da6407afb
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808536"
---
# <span data-ttu-id="bc324-103">Delegieren des Zugriffs auf die Produktionsumgebung</span><span class="sxs-lookup"><span data-stu-id="bc324-103">Delegate Access to the Production Environment</span></span>


<span data-ttu-id="bc324-104">Sie können den Zugriff auf Gruppenrichtlinienobjekte (Group Policy Objects, GPOs) in der Produktionsumgebung ändern und vorhandene Berechtigungen für diese GPOs ersetzen.</span><span class="sxs-lookup"><span data-stu-id="bc324-104">You can change access to Group Policy Objects (GPOs) in the production environment, replacing any existing permissions on those GPOs.</span></span> <span data-ttu-id="bc324-105">Sie können Berechtigungen auf Domänenebene so konfigurieren, dass Benutzer das Bearbeiten, löschen oder Ändern der Sicherheit von GPOs in der Produktionsumgebung zulassen oder verhindern, wenn Sie den Ordner **Change Control** nicht in der Gruppenrichtlinien-Verwaltungskonsole (Group Policy Management Console, GPMC) verwenden.</span><span class="sxs-lookup"><span data-stu-id="bc324-105">You can configure permissions at the domain level to either allow or prevent users from editing, deleting, or modifying the security of GPOs in the production environment when they are not using the **Change Control** folder in the Group Policy Management Console (GPMC).</span></span>

**<span data-ttu-id="bc324-106">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="bc324-106">Note</span></span>**  
-   <span data-ttu-id="bc324-107">Das Delegieren des Zugriffs auf die Produktionsumgebung hat keinen Einfluss auf die Möglichkeit der Benutzer, GPOs zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="bc324-107">Delegating access to the production environment does not affect users’ ability to link GPOs.</span></span>

-   <span data-ttu-id="bc324-108">Wenn GPOs kontrolliert oder bereitgestellt werden, wird der Zugriff auf alle anderen Konten, mit Ausnahme der Berechtigungen **Lesen** und **anwenden** , entfernt.</span><span class="sxs-lookup"><span data-stu-id="bc324-108">When GPOs are controlled or deployed, access for any other accounts except those with **Read** and **Apply** permissions is removed.</span></span>

 

<span data-ttu-id="bc324-109">Zum Ausführen dieses Verfahrens ist ein Benutzerkonto erforderlich, das entweder über die erforderlichen Berechtigungen in der erweiterten Gruppenrichtlinienverwaltung (Group Policy Management, AGPM) oder die Rolle des AGPM-Administrators (Vollzugriff) verfügt.</span><span class="sxs-lookup"><span data-stu-id="bc324-109">A user account that has either the necessary permissions in Advanced Group Policy Management (AGPM) or the role of AGPM Administrator (Full Control) is required to complete this procedure.</span></span> <span data-ttu-id="bc324-110">Lesen Sie die Details unter "Weitere Überlegungen" in diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="bc324-110">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="bc324-111">So ändern Sie den Zugriff auf GPOs in der Produktionsumgebung</span><span class="sxs-lookup"><span data-stu-id="bc324-111">To change access to GPOs in the production environment</span></span>**

1.  <span data-ttu-id="bc324-112">Klicken Sie in der Struktur der **Gruppenrichtlinien-Verwaltungskonsole** in der Gesamtstruktur und Domäne, in der Sie GPOs verwalten möchten, auf **Steuerelement ändern** .</span><span class="sxs-lookup"><span data-stu-id="bc324-112">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="bc324-113">Klicken Sie auf die Registerkarte **Produktions Delegierung** .</span><span class="sxs-lookup"><span data-stu-id="bc324-113">Click the **Production Delegation** tab.</span></span>

3.  <span data-ttu-id="bc324-114">So fügen Sie Berechtigungen für einen Benutzer oder eine Gruppe hinzu, die keinen Zugriff auf die Produktionsumgebung haben, oder um die Berechtigungen für einen Benutzer oder eine Gruppe zu ersetzen, der Zugriff hat:</span><span class="sxs-lookup"><span data-stu-id="bc324-114">To add permissions for a user or group that does not have access to the production environment, or to replace the permissions for a user or group that does have access:</span></span>

    1.  <span data-ttu-id="bc324-115">Klicken Sie auf **Hinzufügen**, wählen Sie einen Benutzer oder eine Gruppe aus, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="bc324-115">Click **Add**, select a user or group, and then click **OK**.</span></span>

    2.  <span data-ttu-id="bc324-116">Wählen Sie Berechtigungen aus, die an diesen Benutzer oder die Gruppe für die Produktionsumgebung delegiert werden sollen, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="bc324-116">Select permissions to delegate to that user or group for the production environment, and then click **OK**.</span></span>

4.  <span data-ttu-id="bc324-117">Wenn Sie alle Berechtigungen für die Produktionsumgebung für einen Benutzer oder eine Gruppe entfernen möchten, wählen Sie den Benutzer oder die Gruppe aus, klicken Sie auf **Entfernen**, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="bc324-117">To remove all permissions to the production environment for a user or group, select the user or group, click **Remove**, and then click **OK**.</span></span>

### <span data-ttu-id="bc324-118">Weitere Überlegungen</span><span class="sxs-lookup"><span data-stu-id="bc324-118">Additional considerations</span></span>

-   <span data-ttu-id="bc324-119">Standardmäßig müssen Sie ein AGPM-Administrator (Vollzugriff) sein, um dieses Verfahren ausführen zu können.</span><span class="sxs-lookup"><span data-stu-id="bc324-119">By default, you must be an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="bc324-120">Insbesondere müssen Sie die Berechtigung zum **Ändern der Sicherheit** für die Domäne besitzen.</span><span class="sxs-lookup"><span data-stu-id="bc324-120">Specifically, you must have **Modify Security** permission for the domain.</span></span>

-   <span data-ttu-id="bc324-121">Berechtigungen für das AGPM-Dienstkonto können auf der Registerkarte **Produktions Delegierung** nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="bc324-121">Permissions for the AGPM Service Account cannot be changed on the **Production Delegation** tab.</span></span>

-   <span data-ttu-id="bc324-122">Die folgenden Konten verfügen standardmäßig über Berechtigungen für GPOs in der Produktionsumgebung:</span><span class="sxs-lookup"><span data-stu-id="bc324-122">By default, the following accounts have permissions for GPOs in the production environment:</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="bc324-123">Account</span><span class="sxs-lookup"><span data-stu-id="bc324-123">Account</span></span></th>
    <th align="left"><span data-ttu-id="bc324-124">Standardberechtigungen für GPOs</span><span class="sxs-lookup"><span data-stu-id="bc324-124">Default Permissions for GPOs</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="bc324-125">&lt;AGPM-Dienstkonto&gt;</span><span class="sxs-lookup"><span data-stu-id="bc324-125">&lt;AGPM Service Account&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="bc324-126">Bearbeiten von Einstellungen, löschen, Ändern der Sicherheit</span><span class="sxs-lookup"><span data-stu-id="bc324-126">Edit Settings, Delete, Modify Security</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="bc324-127">Authentifizierte Benutzer</span><span class="sxs-lookup"><span data-stu-id="bc324-127">Authenticated Users</span></span></p></td>
    <td align="left"><p><span data-ttu-id="bc324-128">Lesen, anwenden</span><span class="sxs-lookup"><span data-stu-id="bc324-128">Read, Apply</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="bc324-129">Domänenadministratoren</span><span class="sxs-lookup"><span data-stu-id="bc324-129">Domain Admins</span></span></p></td>
    <td align="left"><p><span data-ttu-id="bc324-130">Bearbeiten von Einstellungen, löschen, Ändern der Sicherheit</span><span class="sxs-lookup"><span data-stu-id="bc324-130">Edit Settings, Delete, Modify Security</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="bc324-131">Unternehmensadministratoren</span><span class="sxs-lookup"><span data-stu-id="bc324-131">Enterprise Admins</span></span></p></td>
    <td align="left"><p><span data-ttu-id="bc324-132">Bearbeiten von Einstellungen, löschen, Ändern der Sicherheit</span><span class="sxs-lookup"><span data-stu-id="bc324-132">Edit Settings, Delete, Modify Security</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="bc324-133">Unternehmensdomänencontroller</span><span class="sxs-lookup"><span data-stu-id="bc324-133">Enterprise Domain Controllers</span></span></p></td>
    <td align="left"><p><span data-ttu-id="bc324-134">Lesen</span><span class="sxs-lookup"><span data-stu-id="bc324-134">Read</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="bc324-135">System</span><span class="sxs-lookup"><span data-stu-id="bc324-135">System</span></span></p></td>
    <td align="left"><p><span data-ttu-id="bc324-136">Bearbeiten von Einstellungen, löschen, Ändern der Sicherheit</span><span class="sxs-lookup"><span data-stu-id="bc324-136">Edit Settings, Delete, Modify Security</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

-   <span data-ttu-id="bc324-137">Die Mitgliedschaft in der Gruppe Richtlinien Ersteller-Besitzer sollte eingeschränkt sein, soit wird nicht verwendet, um die AGPM-Verwaltung des Zugriffs auf GPOs zu umgehen.</span><span class="sxs-lookup"><span data-stu-id="bc324-137">Membership in the Group Policy Creator Owners group should be restricted, soit is not used to circumvent AGPM management of access to GPOs.</span></span> <span data-ttu-id="bc324-138">(Klicken Sie in der **Gruppenrichtlinien-Verwaltungskonsole**auf **Gruppenrichtlinienobjekte** in der Gesamtstruktur und Domäne, in der Sie GPOs verwalten möchten, klicken Sie auf **Delegierung**, und konfigurieren Sie dann die Einstellungen, um die Anforderungen Ihrer Organisation zu erfüllen.)</span><span class="sxs-lookup"><span data-stu-id="bc324-138">(In the **Group Policy Management Console**, click **Group Policy Objects** in the forest and domain in which you want to manage GPOs, click **Delegation**, and then configure the settings to meet the needs of your organization.)</span></span>

### <span data-ttu-id="bc324-139">Weitere Verweise</span><span class="sxs-lookup"><span data-stu-id="bc324-139">Additional references</span></span>

-   [<span data-ttu-id="bc324-140">Konfigurieren von Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="bc324-140">Configuring Advanced Group Policy Management</span></span>](configuring-advanced-group-policy-management.md)

 

 





