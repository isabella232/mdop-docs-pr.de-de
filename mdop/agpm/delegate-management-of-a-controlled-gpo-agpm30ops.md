---
title: Delegieren der Verwaltung eines gesteuerten Gruppenrichtlinienobjekts
description: Delegieren der Verwaltung eines gesteuerten Gruppenrichtlinienobjekts
author: dansimp
ms.assetid: 509b02e7-ce0b-4919-b58a-c3a33051152e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9d34231f25c172951cd0176b3e490dab84b98f1d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807619"
---
# <span data-ttu-id="81ed4-103">Delegieren der Verwaltung eines gesteuerten Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="81ed4-103">Delegate Management of a Controlled GPO</span></span>


<span data-ttu-id="81ed4-104">Eine genehmigende Person kann die Verwaltung eines von dieser genehmigenden Person erstellten kontrollierten Gruppenrichtlinienobjekts (GPO) delegieren.</span><span class="sxs-lookup"><span data-stu-id="81ed4-104">An Approver can delegate the management of a controlled Group Policy Object (GPO) that was created by that Approver.</span></span> <span data-ttu-id="81ed4-105">Wie ein AGPM-Administrator (Vollzugriff) kann die genehmigende Person den Zugriff auf ein solches Gruppenrichtlinienobjekt delegieren, damit ausgewählte Bearbeiter Sie bearbeiten können, Prüfer Sie überprüfen können, und andere genehmigende Personen können Sie genehmigen.</span><span class="sxs-lookup"><span data-stu-id="81ed4-105">Like an AGPM Administrator (Full Control), the Approver can delegate access to such a GPO so that selected Editors can edit it, Reviewers can review it, and other Approvers can approve it.</span></span> <span data-ttu-id="81ed4-106">Standardmäßig kann eine genehmigende Person keinen Zugriff auf GPOs delegieren, die von einem anderen Gruppenrichtlinienadministrator erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="81ed4-106">By default, an Approver cannot delegate access to GPOs created by another Group Policy administrator.</span></span>

<span data-ttu-id="81ed4-107">Ein Benutzerkonto mit der Rolle AGPM-Administrator (Vollzugriff), dem Benutzerkonto der genehmigenden Person, die das Gruppenrichtlinienobjekt erstellt hat, oder ein Benutzerkonto mit den erforderlichen Berechtigungen in der erweiterten Gruppenrichtlinienverwaltung (Group Policy Management, AGPM) ist erforderlich, um dieses Verfahren ausführen zu können.</span><span class="sxs-lookup"><span data-stu-id="81ed4-107">A user account with the AGPM Administrator (Full Control) role, the user account of the Approver who created the GPO, or a user account with the necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span> <span data-ttu-id="81ed4-108">Lesen Sie die Details unter "Weitere Überlegungen" in diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="81ed4-108">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="81ed4-109">So delegieren Sie die Verwaltung eines kontrollierten Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="81ed4-109">To delegate the management of a controlled GPO</span></span>**

1.  <span data-ttu-id="81ed4-110">Klicken Sie in der Struktur der **Gruppenrichtlinien-Verwaltungskonsole** in der Gesamtstruktur und Domäne, in der Sie GPOs verwalten möchten, auf **Steuerelement ändern** .</span><span class="sxs-lookup"><span data-stu-id="81ed4-110">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="81ed4-111">Klicken Sie im Detailbereich auf der Registerkarte **Inhalt** auf die Registerkarte **gesteuert** , um gesteuerte GPOs anzuzeigen, und klicken Sie dann auf das zu delegierende Gruppenrichtlinienobjekt:</span><span class="sxs-lookup"><span data-stu-id="81ed4-111">On the **Contents** tab in the details pane, click the **Controlled** tab to display controlled GPOs, and then click the GPO to delegate:</span></span>

    1.  <span data-ttu-id="81ed4-112">Klicken Sie zum Hinzufügen von Zugriff für einen Benutzer oder eine Gruppe auf die Schaltfläche **Hinzufügen** , wählen Sie den Benutzer oder die Gruppe aus, und klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="81ed4-112">To add access for a user or group, click the **Add** button, select the user or group, and click **OK**.</span></span> <span data-ttu-id="81ed4-113">Wählen Sie im Dialogfeld **Gruppe oder Benutzer hinzufügen** eine Rolle aus, und klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="81ed4-113">In the **Add Group or User** dialog box, select a role and click **OK**.</span></span>

    2.  <span data-ttu-id="81ed4-114">Wenn Sie den Zugriff für einen Benutzer oder eine Gruppe entfernen möchten, wählen Sie den Benutzer oder die Gruppe aus, und klicken Sie dann auf die Schaltfläche **Entfernen** .</span><span class="sxs-lookup"><span data-stu-id="81ed4-114">To remove access for a user or group, select the user or group, and then click the **Remove** button.</span></span>

        <span data-ttu-id="81ed4-115">**Hinweis**  Wenn ein Benutzer oder eine Gruppe domänenweiten Zugriff erbt, ist die Schaltfläche **Entfernen** nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="81ed4-115">**Note** If a user or group inherits domain-wide access, the **Remove** button is unavailable.</span></span> <span data-ttu-id="81ed4-116">Sie können den domänenweiten Zugriff auf der Registerkarte **Domänendelegierung** ändern.</span><span class="sxs-lookup"><span data-stu-id="81ed4-116">You can modify domain-wide access on the **Domain Delegation** tab.</span></span>

         

    3.  <span data-ttu-id="81ed4-117">Wenn Sie die Rollen und Berechtigungen ändern möchten, die an einen Benutzer oder eine Gruppe delegiert wurden, klicken Sie auf die Schaltfläche **erweitert** .</span><span class="sxs-lookup"><span data-stu-id="81ed4-117">To modify the roles and permissions delegated to a user or group, click the **Advanced** button.</span></span> <span data-ttu-id="81ed4-118">Wählen Sie im Dialogfeld **Berechtigungen** den Benutzer oder die Gruppe aus, aktivieren Sie das Kontrollkästchen für jede Rolle, die diesem Benutzer oder dieser Gruppe zugewiesen werden soll, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="81ed4-118">In the **Permissions** dialog box, select the user or group, select the check box for each role to be assigned to that user or group, and then click **OK**.</span></span>

        <span data-ttu-id="81ed4-119">**Hinweis**  Editor und Genehmiger sind Berechtigungen für Bearbeiter.</span><span class="sxs-lookup"><span data-stu-id="81ed4-119">**Note** Editor and Approver include Reviewer permissions.</span></span>

         

### <span data-ttu-id="81ed4-120">Weitere Überlegungen</span><span class="sxs-lookup"><span data-stu-id="81ed4-120">Additional considerations</span></span>

-   <span data-ttu-id="81ed4-121">Standardmäßig müssen Sie die genehmigende Person sein, die das Gruppenrichtlinienobjekt erstellt oder kontrolliert hat, oder einen AGPM-Administrator (Vollzugriff), um dieses Verfahren ausführen zu können.</span><span class="sxs-lookup"><span data-stu-id="81ed4-121">By default, you must be the Approver who created or controlled the GPO or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="81ed4-122">Insbesondere müssen Sie über die Berechtigung **Listeninhalt** für die Domäne und die Berechtigung zum **Ändern der Sicherheit** für das Gruppenrichtlinienobjekt verfügen.</span><span class="sxs-lookup"><span data-stu-id="81ed4-122">Specifically, you must have **List Contents** permission for the domain and **Modify Security** permission for the GPO.</span></span>

-   <span data-ttu-id="81ed4-123">Wenn Sie den Lesezugriff an Gruppenrichtlinienadministratoren delegieren möchten, die AGPM verwenden, müssen Sie Ihnen **Listeninhalte** und Berechtigungen zum **Lesen von Einstellungen** erteilen.</span><span class="sxs-lookup"><span data-stu-id="81ed4-123">To delegate read access to Group Policy administrators who use AGPM, you must grant them **List Contents** as well as **Read Settings** permissions.</span></span> <span data-ttu-id="81ed4-124">Dadurch können Sie GPOs auf der Registerkarte **Inhalt** von AGPM anzeigen.</span><span class="sxs-lookup"><span data-stu-id="81ed4-124">This enables them to view GPOs on the **Contents** tab of AGPM.</span></span> <span data-ttu-id="81ed4-125">Andere Berechtigungen müssen explizit delegiert werden.</span><span class="sxs-lookup"><span data-stu-id="81ed4-125">Other permissions must be explicitly delegated.</span></span>

-   <span data-ttu-id="81ed4-126">Redakteure müssen über die Berechtigung " **Lesen** " für die bereitgestellte Kopie eines Gruppenrichtlinienobjekts verfügen, um die Gruppenrichtlinien-Software Installation vollständig nutzen zu können.</span><span class="sxs-lookup"><span data-stu-id="81ed4-126">Editors must have **Read** permission for the deployed copy of a GPO to make full use of Group Policy Software Installation.</span></span>

### <span data-ttu-id="81ed4-127">Weitere Verweise</span><span class="sxs-lookup"><span data-stu-id="81ed4-127">Additional references</span></span>

-   [<span data-ttu-id="81ed4-128">Erstellen, Steuern oder Importieren eines Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="81ed4-128">Creating, Controlling, or Importing a GPO</span></span>](creating-controlling-or-importing-a-gpo-editor-agpm30ops.md)

 

 





