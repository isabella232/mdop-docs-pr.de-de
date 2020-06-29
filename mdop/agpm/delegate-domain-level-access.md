---
title: Delegieren des Domänenebenenzugriffs
description: Delegieren des Domänenebenenzugriffs
author: dansimp
ms.assetid: 64c8e773-38cc-4991-9ed2-5a801094d06e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7eb4c33e60b0d995e45fca6c9e91a26c30dd4a7f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808531"
---
# <span data-ttu-id="e19a5-103">Delegieren des Domänenebenenzugriffs</span><span class="sxs-lookup"><span data-stu-id="e19a5-103">Delegate Domain-Level Access</span></span>


<span data-ttu-id="e19a5-104">Richten Sie eine Delegierung für Ihre Umgebung ein, damit Gruppenrichtlinienadministratoren über den entsprechenden Zugriff auf und die Kontrolle über Gruppenrichtlinienobjekte (Group Policy Objects, GPOs) verfügen.</span><span class="sxs-lookup"><span data-stu-id="e19a5-104">Set up delegation for your environment so Group Policy administrators have the appropriate access to and control over Group Policy objects (GPOs).</span></span> <span data-ttu-id="e19a5-105">Es gibt Baseline-Berechtigungen, die Sie anwenden können, um den Betrieb von Advanced Group Policy Management (AGPM) effizienter zu gestalten.</span><span class="sxs-lookup"><span data-stu-id="e19a5-105">There are baseline permissions you can apply to make the operation of Advanced Group Policy Management (AGPM) more efficient.</span></span> <span data-ttu-id="e19a5-106">Sie können Berechtigungen auf jede Art und Weise erteilen, die den Anforderungen Ihrer Organisation entspricht.</span><span class="sxs-lookup"><span data-stu-id="e19a5-106">You can grant permissions in any manner that meets the needs of your organization.</span></span>

<span data-ttu-id="e19a5-107">Zum Ausführen dieses Verfahrens ist ein Benutzerkonto mit der Rolle AGPM-Administrator (Vollzugriff) oder den erforderlichen Berechtigungen in der erweiterten Gruppenrichtlinienverwaltung erforderlich.</span><span class="sxs-lookup"><span data-stu-id="e19a5-107">A user account with the AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management is required to complete this procedure.</span></span> <span data-ttu-id="e19a5-108">Lesen Sie die Details unter "Weitere Überlegungen" in diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="e19a5-108">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="e19a5-109">So delegieren Sie den Zugriff, damit Benutzer und Gruppen über die entsprechenden Berechtigungen für alle GPOs in einer Domäne verfügen</span><span class="sxs-lookup"><span data-stu-id="e19a5-109">To delegate access so users and groups have appropriate permissions to all GPOs throughout a domain</span></span>**

1.  <span data-ttu-id="e19a5-110">Klicken Sie in der Struktur der **Gruppenrichtlinien-Verwaltungskonsole** in der Gesamtstruktur und Domäne, in der Sie GPOs verwalten möchten, auf **Steuerelement ändern** .</span><span class="sxs-lookup"><span data-stu-id="e19a5-110">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="e19a5-111">Klicken Sie auf die Registerkarte **Domänendelegierung** , und klicken Sie dann auf die Schaltfläche **erweitert** .</span><span class="sxs-lookup"><span data-stu-id="e19a5-111">Click the **Domain Delegation** tab, then click the **Advanced** button.</span></span>

3.  <span data-ttu-id="e19a5-112">Klicken Sie im Dialogfeld **Berechtigungen** auf das Kontrollkästchen für jede Rolle, die einer Person zugewiesen werden soll, und klicken Sie dann auf die Schaltfläche **erweitert** .</span><span class="sxs-lookup"><span data-stu-id="e19a5-112">In the **Permissions** dialog box, click the check box for each role to be assigned to an individual, and then click the **Advanced** button.</span></span>

    <span data-ttu-id="e19a5-113">**Hinweis**  Editor und Genehmiger sind Berechtigungen für Bearbeiter.</span><span class="sxs-lookup"><span data-stu-id="e19a5-113">**Note** Editor and Approver include Reviewer permissions.</span></span>

     

4.  <span data-ttu-id="e19a5-114">Wählen Sie im Dialogfeld **Erweiterte Sicherheitseinstellungen** einen Gruppenrichtlinienadministrator aus, und klicken Sie dann auf **Bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="e19a5-114">In the **Advanced Security Settings** dialog box, select a Group Policy administrator, and then click **Edit**.</span></span>

5.  <span data-ttu-id="e19a5-115">Wählen Sie für **anwenden auf**die Option **dieses Objekt und verschachtelte Objekte**aus, konfigurieren Sie alle speziellen Berechtigungen über die standardmäßigen AGPM-Rollen hinaus, und klicken Sie dann im Dialogfeld **Berechtigungs** **Eintrag** auf **OK** .</span><span class="sxs-lookup"><span data-stu-id="e19a5-115">For **Apply onto**, select **This object and nested objects**, configure any special permissions beyond the standard AGPM roles, then click **OK** in the **Permission** **Entry** dialog box.</span></span>

6.  <span data-ttu-id="e19a5-116">Klicken Sie im Dialogfeld **Erweiterte Sicherheitseinstellungen** auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="e19a5-116">In the **Advanced Security Settings** dialog box, click **OK**.</span></span>

7.  <span data-ttu-id="e19a5-117">Klicken Sie im Dialogfeld **Berechtigungen** auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="e19a5-117">In the **Permissions** dialog box, click **OK**.</span></span>

### <span data-ttu-id="e19a5-118">Weitere Überlegungen</span><span class="sxs-lookup"><span data-stu-id="e19a5-118">Additional considerations</span></span>

-   <span data-ttu-id="e19a5-119">Standardmäßig müssen Sie ein AGPM-Administrator (Vollzugriff) sein, um dieses Verfahren ausführen zu können.</span><span class="sxs-lookup"><span data-stu-id="e19a5-119">By default, you must be an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="e19a5-120">Insbesondere müssen Sie die Berechtigung zum **Ändern der Sicherheit** für die Domäne besitzen.</span><span class="sxs-lookup"><span data-stu-id="e19a5-120">Specifically, you must have **Modify Security** permission for the domain.</span></span>

-   <span data-ttu-id="e19a5-121">Wenn Sie den Lesezugriff an Gruppenrichtlinienadministratoren delegieren möchten, die AGPM verwenden, müssen Sie Ihnen **Listeninhalte** und Berechtigungen zum **Lesen von Einstellungen** erteilen.</span><span class="sxs-lookup"><span data-stu-id="e19a5-121">To delegate read access to Group Policy administrators who use AGPM, you must grant them **List Contents** as well as **Read Settings** permissions.</span></span> <span data-ttu-id="e19a5-122">Dadurch können Sie GPOs auf der Registerkarte **Inhalt** von AGPM anzeigen.</span><span class="sxs-lookup"><span data-stu-id="e19a5-122">This enables them to view GPOs on the **Contents** tab of AGPM.</span></span> <span data-ttu-id="e19a5-123">Legen Sie die Berechtigung für **dieses Objekt und verschachtelte Objekte**auf.</span><span class="sxs-lookup"><span data-stu-id="e19a5-123">Set the permission to apply to **This object and nested objects**.</span></span> <span data-ttu-id="e19a5-124">Andere Berechtigungen müssen explizit delegiert werden.</span><span class="sxs-lookup"><span data-stu-id="e19a5-124">Other permissions must be explicitly delegated.</span></span>

-   <span data-ttu-id="e19a5-125">Editoren muss die **Lese** Berechtigung für die bereitgestellte Kopie eines GPO gewährt werden, damit die Gruppenrichtlinien-Software Installation vollständig genutzt werden kann.</span><span class="sxs-lookup"><span data-stu-id="e19a5-125">Editors must be granted **Read** permission for the deployed copy of a GPO to make full use of Group Policy Software Installation.</span></span>

-   <span data-ttu-id="e19a5-126">Die Mitgliedschaft in der Gruppe Richtlinien Ersteller-Besitzer sollte eingeschränkt sein, damit Sie nicht zur Umgehung der AGPM-Verwaltung des Zugriffs auf GPOs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e19a5-126">Membership in the Group Policy Creator Owners group should be restricted so that it is not used to circumvent AGPM management of access to GPOs.</span></span> <span data-ttu-id="e19a5-127">(Klicken Sie in der **Gruppenrichtlinien-Verwaltungskonsole**auf **Gruppenrichtlinienobjekte** in der Gesamtstruktur und Domäne, in der Sie GPOs verwalten möchten, klicken Sie auf **Delegierung**, und konfigurieren Sie dann die Einstellungen, um die Anforderungen Ihrer Organisation zu erfüllen.)</span><span class="sxs-lookup"><span data-stu-id="e19a5-127">(In the **Group Policy Management Console**, click **Group Policy Objects** in the forest and domain in which you want to manage GPOs, click **Delegation**, and then configure the settings to meet the needs of your organization.)</span></span>

### <span data-ttu-id="e19a5-128">Weitere Verweise</span><span class="sxs-lookup"><span data-stu-id="e19a5-128">Additional references</span></span>

-   [<span data-ttu-id="e19a5-129">Durchführen von AGPM-Administratoraufgaben</span><span class="sxs-lookup"><span data-stu-id="e19a5-129">Performing AGPM Administrator Tasks</span></span>](performing-agpm-administrator-tasks.md)

 

 





