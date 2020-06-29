---
title: Delegieren des Zugriffs auf ein Gruppenrichtlinienobjekt
description: Delegieren des Zugriffs auf ein Gruppenrichtlinienobjekt
author: dansimp
ms.assetid: f1d6bb6c-d5bf-4080-a6cb-32774689f804
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 57a71528120b65676d25d952d9f9392dc0250ae4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807644"
---
# <span data-ttu-id="8fe35-103">Delegieren des Zugriffs auf ein Gruppenrichtlinienobjekt</span><span class="sxs-lookup"><span data-stu-id="8fe35-103">Delegate Access to a GPO</span></span>


<span data-ttu-id="8fe35-104">Eine genehmigende Person kann die Verwaltung eines **von dieser genehmigenden Person erstellten**kontrollierten Gruppenrichtlinienobjekts (GPO) delegieren.</span><span class="sxs-lookup"><span data-stu-id="8fe35-104">An Approver can delegate the management of a controlled Group Policy object (GPO) that was **created by that Approver**.</span></span> <span data-ttu-id="8fe35-105">Wie ein AGPM-Administrator (Vollzugriff) kann die genehmigende Person den Zugriff auf ein solches Gruppenrichtlinienobjekt delegieren, sodass ausgewählte Bearbeiter Sie bearbeiten können, Prüfer Sie überprüfen können, und andere Genehmiger Sie genehmigen können.</span><span class="sxs-lookup"><span data-stu-id="8fe35-105">Like an AGPM Administrator (Full Control), the Approver can delegate access to such a GPO, so selected Editors can edit it, Reviewers can review it, and other Approvers can approve it.</span></span> <span data-ttu-id="8fe35-106">Standardmäßig kann eine genehmigende Person keinen Zugriff auf GPOs delegieren, die von einem anderen Gruppenrichtlinienadministrator erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="8fe35-106">By default, an Approver cannot delegate access to GPOs created by another Group Policy administrator.</span></span>

<span data-ttu-id="8fe35-107">Ein Benutzerkonto mit der Rolle AGPM-Administrator (Vollzugriff), dem Benutzerkonto der genehmigenden Person, die das Gruppenrichtlinienobjekt erstellt hat, oder ein Benutzerkonto mit den erforderlichen Berechtigungen in der erweiterten Gruppenrichtlinienverwaltung ist erforderlich, um dieses Verfahren ausführen zu können.</span><span class="sxs-lookup"><span data-stu-id="8fe35-107">A user account with the AGPM Administrator (Full Control) role, the user account of the Approver who created the GPO, or a user account with the necessary permissions in Advanced Group Policy Management is required to complete this procedure.</span></span> <span data-ttu-id="8fe35-108">Lesen Sie die Details unter "Weitere Überlegungen" in diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="8fe35-108">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="8fe35-109">So delegieren Sie die Verwaltung eines kontrollierten Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="8fe35-109">To delegate the management of a controlled GPO</span></span>**

1.  <span data-ttu-id="8fe35-110">Klicken Sie in der Struktur der **Gruppenrichtlinien-Verwaltungskonsole** in der Gesamtstruktur und Domäne, in der Sie GPOs verwalten möchten, auf **Steuerelement ändern** .</span><span class="sxs-lookup"><span data-stu-id="8fe35-110">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="8fe35-111">Klicken Sie im Detailbereich auf der Registerkarte **Inhalt** auf die Registerkarte **gesteuert** , um gesteuerte GPOs anzuzeigen, und klicken Sie dann auf das zu delegierende Gruppenrichtlinienobjekt.</span><span class="sxs-lookup"><span data-stu-id="8fe35-111">On the **Contents** tab in the details pane, click the **Controlled** tab to display controlled GPOs, and then click the GPO to delegate.</span></span>

3.  <span data-ttu-id="8fe35-112">Klicken Sie auf die Schaltfläche **Hinzufügen** , wählen Sie die Benutzer oder Gruppen aus, denen Sie Zugriff gewähren möchten, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="8fe35-112">Click the **Add** button, select the users or groups to be permitted access, and then click **OK**.</span></span>

4.  <span data-ttu-id="8fe35-113">Um die Berechtigungen für die einzelnen Benutzer anzupassen, klicken Sie auf der Registerkarte **Inhalt** auf die Schaltfläche **erweitert** , und überprüfen Sie die Rollen Berechtigungen auf zulassen oder ablehnen.</span><span class="sxs-lookup"><span data-stu-id="8fe35-113">To customize the permissions for each, click the **Advanced** button on the **Contents** tab and check role permissions to allow or deny.</span></span> <span data-ttu-id="8fe35-114">(Wenn Sie eine genauere Steuerung haben, klicken Sie im Dialogfeld **Berechtigungen** auf **erweitert** .)</span><span class="sxs-lookup"><span data-stu-id="8fe35-114">(For more detailed control, click **Advanced** in the **Permissions** dialog box.)</span></span>

5.  <span data-ttu-id="8fe35-115">Klicken Sie auf über **nehmen**, und klicken Sie dann im Dialogfeld **Berechtigungen** auf **OK** .</span><span class="sxs-lookup"><span data-stu-id="8fe35-115">Click **Apply**, and then click **OK** in the **Permissions** dialog box.</span></span>

### <span data-ttu-id="8fe35-116">Weitere Überlegungen</span><span class="sxs-lookup"><span data-stu-id="8fe35-116">Additional considerations</span></span>

-   <span data-ttu-id="8fe35-117">Standardmäßig müssen Sie die genehmigende Person sein, die das Gruppenrichtlinienobjekt erstellt oder kontrolliert hat, oder einen AGPM-Administrator (Vollzugriff), um dieses Verfahren ausführen zu können.</span><span class="sxs-lookup"><span data-stu-id="8fe35-117">By default, you must be the Approver who created or controlled the GPO or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="8fe35-118">Insbesondere müssen Sie über die Berechtigung **Listeninhalt** für die Domäne und die Berechtigung zum **Ändern der Sicherheit** für das Gruppenrichtlinienobjekt verfügen.</span><span class="sxs-lookup"><span data-stu-id="8fe35-118">Specifically, you must have **List Contents** permission for the domain and **Modify Security** permission for the GPO.</span></span>

### <span data-ttu-id="8fe35-119">Weitere Verweise</span><span class="sxs-lookup"><span data-stu-id="8fe35-119">Additional references</span></span>

-   [<span data-ttu-id="8fe35-120">Erstellen, Steuern oder Importieren eines Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="8fe35-120">Creating, Controlling, or Importing a GPO</span></span>](creating-controlling-or-importing-a-gpo-approver.md)

 

 





