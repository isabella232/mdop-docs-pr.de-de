---
title: Delegieren des Domänenebenenzugriffs auf das Archiv
description: Delegieren des Domänenebenenzugriffs auf das Archiv
author: dansimp
ms.assetid: 11ca1d40-4b5c-496e-8922-d01412717858
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b33c0ec8821248ab4eddc051e67e7f0e6c073a9e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807620"
---
# <span data-ttu-id="8ec07-103">Delegieren des Domänenebenenzugriffs auf das Archiv</span><span class="sxs-lookup"><span data-stu-id="8ec07-103">Delegate Domain-Level Access to the Archive</span></span>


<span data-ttu-id="8ec07-104">Richten Sie eine Delegierung für Ihre Umgebung ein, damit Gruppenrichtlinienadministratoren über den entsprechenden Zugriff auf und die Kontrolle über Gruppenrichtlinienobjekte (Group Policy Objects, GPOs) im Archiv verfügen.</span><span class="sxs-lookup"><span data-stu-id="8ec07-104">Set up delegation for your environment so that Group Policy administrators have the appropriate access to and control over Group Policy Objects (GPOs) in the archive.</span></span> <span data-ttu-id="8ec07-105">Es gibt Baseline-Berechtigungen, die Sie anwenden können, um den Vorgang effizienter zu gestalten.</span><span class="sxs-lookup"><span data-stu-id="8ec07-105">There are baseline permissions you can apply to make operation more efficient.</span></span> <span data-ttu-id="8ec07-106">Sie können Berechtigungen auf jede Art und Weise erteilen, die den Anforderungen Ihrer Organisation entspricht.</span><span class="sxs-lookup"><span data-stu-id="8ec07-106">You can grant permissions in any manner that meets the needs of your organization.</span></span>

<span data-ttu-id="8ec07-107">Zum Ausführen dieses Verfahrens ist ein Benutzerkonto mit der Rolle AGPM-Administrator (Vollzugriff) oder den erforderlichen Berechtigungen in Advanced Group Policy Management (AGPM) erforderlich.</span><span class="sxs-lookup"><span data-stu-id="8ec07-107">A user account with the AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span> <span data-ttu-id="8ec07-108">Lesen Sie die Details unter "Weitere Überlegungen" in diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="8ec07-108">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="8ec07-109">So delegieren Sie den Zugriff, damit Benutzer und Gruppen über die entsprechenden Berechtigungen für alle GPOs in einer Domäne verfügen</span><span class="sxs-lookup"><span data-stu-id="8ec07-109">To delegate access so that users and groups have appropriate permissions to all GPOs throughout a domain</span></span>**

1.  <span data-ttu-id="8ec07-110">Klicken Sie in der Struktur der **Gruppenrichtlinien-Verwaltungskonsole** in der Gesamtstruktur und Domäne, in der Sie GPOs verwalten möchten, auf **Steuerelement ändern** .</span><span class="sxs-lookup"><span data-stu-id="8ec07-110">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="8ec07-111">Klicken Sie auf die Registerkarte **Domänendelegierung** , und konfigurieren Sie den Zugriff auf alle GPOs in der Domäne:</span><span class="sxs-lookup"><span data-stu-id="8ec07-111">Click the **Domain Delegation** tab, and configure access to all GPOs in the domain:</span></span>

    1.  <span data-ttu-id="8ec07-112">Klicken Sie zum Hinzufügen von Zugriff für einen Benutzer oder eine Gruppe auf die Schaltfläche **Hinzufügen** , wählen Sie den Benutzer oder die Gruppe aus, und klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="8ec07-112">To add access for a user or group, click the **Add** button, select the user or group, and click **OK**.</span></span> <span data-ttu-id="8ec07-113">Wählen Sie im Dialogfeld **Gruppe oder Benutzer hinzufügen** eine Rolle aus, und klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="8ec07-113">In the **Add Group or User** dialog box, select a role and click **OK**.</span></span>

    2.  <span data-ttu-id="8ec07-114">Wenn Sie den Zugriff für einen Benutzer oder eine Gruppe entfernen möchten, wählen Sie den Benutzer oder die Gruppe aus, und klicken Sie auf die Schaltfläche **Entfernen** .</span><span class="sxs-lookup"><span data-stu-id="8ec07-114">To remove access for a user or group, select the user or group, and click the **Remove** button.</span></span>

    3.  <span data-ttu-id="8ec07-115">Wenn Sie die Rollen und Berechtigungen ändern möchten, die an einen Benutzer oder eine Gruppe delegiert wurden, klicken Sie auf die Schaltfläche **erweitert** .</span><span class="sxs-lookup"><span data-stu-id="8ec07-115">To modify the roles and permissions delegated to a user or group, select click the **Advanced** button.</span></span> <span data-ttu-id="8ec07-116">Wählen Sie im Dialogfeld **Berechtigungen** den Benutzer oder die Gruppe aus, aktivieren Sie das Kontrollkästchen für jede Rolle, die diesem Benutzer oder dieser Gruppe zugewiesen werden soll, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="8ec07-116">In the **Permissions** dialog box, select the user or group, select the check box for each role to be assigned to that user or group, and then click **OK**.</span></span>

        <span data-ttu-id="8ec07-117">**Hinweis**  Editor und Genehmiger sind Berechtigungen für Bearbeiter.</span><span class="sxs-lookup"><span data-stu-id="8ec07-117">**Note** Editor and Approver include Reviewer permissions.</span></span>

         

### <span data-ttu-id="8ec07-118">Weitere Überlegungen</span><span class="sxs-lookup"><span data-stu-id="8ec07-118">Additional considerations</span></span>

-   <span data-ttu-id="8ec07-119">Standardmäßig müssen Sie ein AGPM-Administrator (Vollzugriff) sein, um dieses Verfahren ausführen zu können.</span><span class="sxs-lookup"><span data-stu-id="8ec07-119">By default, you must be an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="8ec07-120">Insbesondere müssen Sie die Berechtigung zum **Ändern der Sicherheit** für die Domäne besitzen.</span><span class="sxs-lookup"><span data-stu-id="8ec07-120">Specifically, you must have **Modify Security** permission for the domain.</span></span>

-   <span data-ttu-id="8ec07-121">Wenn Sie den Lesezugriff an Gruppenrichtlinienadministratoren delegieren möchten, die AGPM verwenden, müssen Sie Ihnen **Listeninhalte** und Berechtigungen zum **Lesen von Einstellungen** erteilen.</span><span class="sxs-lookup"><span data-stu-id="8ec07-121">To delegate read access to Group Policy administrators who use AGPM, you must grant them **List Contents** as well as **Read Settings** permissions.</span></span> <span data-ttu-id="8ec07-122">Dadurch können Sie GPOs auf der Registerkarte **Inhalt** von AGPM anzeigen.</span><span class="sxs-lookup"><span data-stu-id="8ec07-122">This enables them to view GPOs on the **Contents** tab of AGPM.</span></span> <span data-ttu-id="8ec07-123">Andere Berechtigungen müssen explizit delegiert werden.</span><span class="sxs-lookup"><span data-stu-id="8ec07-123">Other permissions must be explicitly delegated.</span></span>

-   <span data-ttu-id="8ec07-124">Editoren muss die **Lese** Berechtigung für die bereitgestellte Kopie eines GPO gewährt werden, damit die Gruppenrichtlinien-Software Installation vollständig genutzt werden kann.</span><span class="sxs-lookup"><span data-stu-id="8ec07-124">Editors must be granted **Read** permission for the deployed copy of a GPO to make full use of Group Policy Software Installation.</span></span>

-   <span data-ttu-id="8ec07-125">Die Mitgliedschaft in der Gruppe Richtlinien Ersteller-Besitzer sollte eingeschränkt sein, soit wird nicht verwendet, um die AGPM-Verwaltung des Zugriffs auf GPOs zu umgehen.</span><span class="sxs-lookup"><span data-stu-id="8ec07-125">Membership in the Group Policy Creator Owners group should be restricted, soit is not used to circumvent AGPM management of access to GPOs.</span></span> <span data-ttu-id="8ec07-126">(Klicken Sie in der **Gruppenrichtlinien-Verwaltungskonsole**auf **Gruppenrichtlinienobjekte** in der Gesamtstruktur und Domäne, in der Sie GPOs verwalten möchten, klicken Sie auf **Delegierung**, und konfigurieren Sie dann die Einstellungen, um die Anforderungen Ihrer Organisation zu erfüllen.)</span><span class="sxs-lookup"><span data-stu-id="8ec07-126">(In the **Group Policy Management Console**, click **Group Policy Objects** in the forest and domain in which you want to manage GPOs, click **Delegation**, and then configure the settings to meet the needs of your organization.)</span></span>

### <span data-ttu-id="8ec07-127">Weitere Verweise</span><span class="sxs-lookup"><span data-stu-id="8ec07-127">Additional references</span></span>

-   [<span data-ttu-id="8ec07-128">Verwalten des Archivs</span><span class="sxs-lookup"><span data-stu-id="8ec07-128">Managing the Archive</span></span>](managing-the-archive-agpm40.md)

 

 





