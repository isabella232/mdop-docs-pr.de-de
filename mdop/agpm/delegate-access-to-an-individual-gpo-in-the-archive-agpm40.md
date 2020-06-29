---
title: Delegieren des Zugriffs auf ein einzelnes Gruppenrichtlinienobjekt im Archiv
description: Delegieren des Zugriffs auf ein einzelnes Gruppenrichtlinienobjekt im Archiv
author: dansimp
ms.assetid: 284d2aa2-7c10-4ffa-8978-bbe30867c1c1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9da2a699568f961d030b05a966b76e08aef3aec8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808547"
---
# <span data-ttu-id="bb82d-103">Delegieren des Zugriffs auf ein einzelnes Gruppenrichtlinienobjekt im Archiv</span><span class="sxs-lookup"><span data-stu-id="bb82d-103">Delegate Access to an Individual GPO in the Archive</span></span>


<span data-ttu-id="bb82d-104">Als AGPM-Administrator (Vollzugriff) können Sie die Verwaltung eines kontrollierten Gruppenrichtlinienobjekts (GPO) im Archiv delegieren, damit es von ausgewählten Gruppen und Herausgebern bearbeitet werden kann, Prüfer Sie überprüfen können und von genehmigenden Personen genehmigt werden können.</span><span class="sxs-lookup"><span data-stu-id="bb82d-104">As an AGPM Administrator (Full Control), you can delegate the management of a controlled Group Policy Object (GPO) in the archive so that selected groups and Editors can edit it, Reviewers can review it, and Approvers can approve it.</span></span>

<span data-ttu-id="bb82d-105">Ein Benutzerkonto mit der Rolle AGPM-Administrator (Vollzugriff), dem Benutzerkonto der genehmigenden Person, die das Gruppenrichtlinienobjekt erstellt hat, oder ein Benutzerkonto mit den erforderlichen Berechtigungen in der erweiterten Gruppenrichtlinienverwaltung (Group Policy Management, AGPM) ist erforderlich, um dieses Verfahren ausführen zu können.</span><span class="sxs-lookup"><span data-stu-id="bb82d-105">A user account with the AGPM Administrator (Full Control) role, the user account of the Approver who created the GPO, or a user account with the necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span> <span data-ttu-id="bb82d-106">Lesen Sie die Details unter "Weitere Überlegungen" in diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="bb82d-106">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="bb82d-107">So delegieren Sie die Verwaltung eines kontrollierten Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="bb82d-107">To delegate the management of a controlled GPO</span></span>**

1.  <span data-ttu-id="bb82d-108">Klicken Sie in der Struktur der **Gruppenrichtlinien-Verwaltungskonsole** in der Gesamtstruktur und Domäne, in der Sie GPOs verwalten möchten, auf **Steuerelement ändern** .</span><span class="sxs-lookup"><span data-stu-id="bb82d-108">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="bb82d-109">Klicken Sie im Detailbereich auf der Registerkarte **Inhalt** auf die Registerkarte **gesteuert** , um gesteuerte GPOs anzuzeigen, und klicken Sie dann auf das zu delegierende Gruppenrichtlinienobjekt:</span><span class="sxs-lookup"><span data-stu-id="bb82d-109">On the **Contents** tab in the details pane, click the **Controlled** tab to display controlled GPOs, and then click the GPO to delegate:</span></span>

    1.  <span data-ttu-id="bb82d-110">Klicken Sie zum Hinzufügen von Zugriff für einen Benutzer oder eine Gruppe auf die Schaltfläche **Hinzufügen** , wählen Sie den Benutzer oder die Gruppe aus, und klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="bb82d-110">To add access for a user or group, click the **Add** button, select the user or group, and click **OK**.</span></span> <span data-ttu-id="bb82d-111">Wählen Sie im Dialogfeld **Gruppe oder Benutzer hinzufügen** eine Rolle aus, und klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="bb82d-111">In the **Add Group or User** dialog box, select a role and click **OK**.</span></span>

    2.  <span data-ttu-id="bb82d-112">Wenn Sie den Zugriff für einen Benutzer oder eine Gruppe entfernen möchten, wählen Sie den Benutzer oder die Gruppe aus, und klicken Sie auf die Schaltfläche **Entfernen** .</span><span class="sxs-lookup"><span data-stu-id="bb82d-112">To remove access for a user or group, select the user or group, and click the **Remove** button.</span></span>

        <span data-ttu-id="bb82d-113">**Hinweis**  Wenn ein Benutzer oder eine Gruppe domänenweiten Zugriff erbt, ist die Schaltfläche **Entfernen** nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="bb82d-113">**Note** If a user or group inherits domain-wide access, the **Remove** button is unavailable.</span></span> <span data-ttu-id="bb82d-114">Sie können den domänenweiten Zugriff auf der Registerkarte **Domänendelegierung** ändern.</span><span class="sxs-lookup"><span data-stu-id="bb82d-114">You can modify domain-wide access on the **Domain Delegation** tab.</span></span>

         

    3.  <span data-ttu-id="bb82d-115">Wenn Sie die Rollen und Berechtigungen ändern möchten, die an einen Benutzer oder eine Gruppe delegiert wurden, klicken Sie auf die Schaltfläche **erweitert** .</span><span class="sxs-lookup"><span data-stu-id="bb82d-115">To modify the roles and permissions delegated to a user or group, click the **Advanced** button.</span></span> <span data-ttu-id="bb82d-116">Wählen Sie im Dialogfeld **Berechtigungen** den Benutzer oder die Gruppe aus, aktivieren Sie das Kontrollkästchen für jede Rolle, die diesem Benutzer oder dieser Gruppe zugewiesen werden soll, und klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="bb82d-116">In the **Permissions** dialog box, select the user or group, select the check box for each role to be assigned to that user or group, and click **OK**.</span></span>

        <span data-ttu-id="bb82d-117">**Hinweis**  Editor und Genehmiger sind Berechtigungen für Bearbeiter.</span><span class="sxs-lookup"><span data-stu-id="bb82d-117">**Note** Editor and Approver include Reviewer permissions.</span></span>

         

### <span data-ttu-id="bb82d-118">Weitere Überlegungen</span><span class="sxs-lookup"><span data-stu-id="bb82d-118">Additional considerations</span></span>

-   <span data-ttu-id="bb82d-119">Standardmäßig müssen Sie die genehmigende Person sein, die das Gruppenrichtlinienobjekt erstellt oder kontrolliert hat, oder einen AGPM-Administrator (Vollzugriff), um dieses Verfahren ausführen zu können.</span><span class="sxs-lookup"><span data-stu-id="bb82d-119">By default, you must be the Approver who created or controlled the GPO or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="bb82d-120">Insbesondere müssen Sie über die Berechtigung **Listeninhalt** für die Domäne und die Berechtigung zum **Ändern der Sicherheit** für das Gruppenrichtlinienobjekt verfügen.</span><span class="sxs-lookup"><span data-stu-id="bb82d-120">Specifically, you must have **List Contents** permission for the domain and **Modify Security** permission for the GPO.</span></span>

-   <span data-ttu-id="bb82d-121">Wenn Sie den Lesezugriff an Gruppenrichtlinienadministratoren delegieren möchten, die AGPM verwenden, müssen Sie Ihnen **Listeninhalte** und Berechtigungen zum **Lesen von Einstellungen** erteilen.</span><span class="sxs-lookup"><span data-stu-id="bb82d-121">To delegate read access to Group Policy administrators who use AGPM, you must grant them **List Contents** as well as **Read Settings** permissions.</span></span> <span data-ttu-id="bb82d-122">Dadurch können Sie GPOs auf der Registerkarte **Inhalt** von AGPM anzeigen.</span><span class="sxs-lookup"><span data-stu-id="bb82d-122">This enables them to view GPOs on the **Contents** tab of AGPM.</span></span> <span data-ttu-id="bb82d-123">Andere Berechtigungen müssen explizit delegiert werden.</span><span class="sxs-lookup"><span data-stu-id="bb82d-123">Other permissions must be explicitly delegated.</span></span>

-   <span data-ttu-id="bb82d-124">Redakteure müssen über die Berechtigung " **Lesen** " für die bereitgestellte Kopie eines Gruppenrichtlinienobjekts verfügen, um die Gruppenrichtlinien-Software Installation vollständig nutzen zu können.</span><span class="sxs-lookup"><span data-stu-id="bb82d-124">Editors must have **Read** permission for the deployed copy of a GPO to make full use of Group Policy Software Installation.</span></span>

-   <span data-ttu-id="bb82d-125">Die Mitgliedschaft in der Gruppe Richtlinien Ersteller-Besitzer sollte eingeschränkt sein, soit wird nicht verwendet, um die AGPM-Verwaltung des Zugriffs auf GPOs zu umgehen.</span><span class="sxs-lookup"><span data-stu-id="bb82d-125">Membership in the Group Policy Creator Owners group should be restricted, soit is not used to circumvent AGPM management of access to GPOs.</span></span> <span data-ttu-id="bb82d-126">(Klicken Sie in der **Gruppenrichtlinien-Verwaltungskonsole**auf **Gruppenrichtlinienobjekte** in der Gesamtstruktur und Domäne, in der Sie GPOs verwalten möchten, klicken Sie auf **Delegierung**, und konfigurieren Sie dann die Einstellungen, um die Anforderungen Ihrer Organisation zu erfüllen.)</span><span class="sxs-lookup"><span data-stu-id="bb82d-126">(In the **Group Policy Management Console**, click **Group Policy Objects** in the forest and domain in which you want to manage GPOs, click **Delegation**, and then configure the settings to meet the needs of your organization.)</span></span>

### <span data-ttu-id="bb82d-127">Weitere Verweise</span><span class="sxs-lookup"><span data-stu-id="bb82d-127">Additional references</span></span>

-   [<span data-ttu-id="bb82d-128">Verwalten des Archivs</span><span class="sxs-lookup"><span data-stu-id="bb82d-128">Managing the Archive</span></span>](managing-the-archive-agpm40.md)

 

 





