---
title: Genehmigen oder Ablehnen einer ausstehenden Aktion
description: Genehmigen oder Ablehnen einer ausstehenden Aktion
author: dansimp
ms.assetid: 6d78989a-b600-4876-9dd9-bc6207ff2ce7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5a787e032a441a8b33a48667afecfc98ec2a3642
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807831"
---
# <span data-ttu-id="49dc0-103">Genehmigen oder Ablehnen einer ausstehenden Aktion</span><span class="sxs-lookup"><span data-stu-id="49dc0-103">Approve or Reject a Pending Action</span></span>


<span data-ttu-id="49dc0-104">Die Hauptverantwortung einer genehmigenden Person besteht darin, Anforderungen für die Erstellung, Bereitstellung und Löschung von Gruppenrichtlinienobjekten (Group Policy Object, GPO) zu evaluieren und anschließend zu genehmigen oder abzulehnen.</span><span class="sxs-lookup"><span data-stu-id="49dc0-104">The core responsibility of an Approver is to evaluate and then approve or reject requests for Group Policy Object (GPO) creation, deployment, and deletion from Editors or Reviewers who do not have permission to complete those actions.</span></span> <span data-ttu-id="49dc0-105">Berichte können einer genehmigenden Person beim Auswerten einer neuen Version eines Gruppenrichtlinienobjekts behilflich sein.</span><span class="sxs-lookup"><span data-stu-id="49dc0-105">Reports can assist an Approver with evaluating a new version of a GPO.</span></span>

<span data-ttu-id="49dc0-106">Zum Ausführen dieses Verfahrens ist ein Benutzerkonto mit der Rolle Genehmiger oder AGPM-Administrator (Vollzugriff) oder den erforderlichen Berechtigungen in der erweiterten Gruppenrichtlinienverwaltung (Group Policy Management, AGPM) erforderlich.</span><span class="sxs-lookup"><span data-stu-id="49dc0-106">A user account with the Approver or AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span> <span data-ttu-id="49dc0-107">Lesen Sie die Details unter "Weitere Überlegungen" in diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="49dc0-107">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="49dc0-108">So genehmigen oder ablehnen Sie eine ausstehende Anforderung</span><span class="sxs-lookup"><span data-stu-id="49dc0-108">To approve or reject a pending request</span></span>**

1.  <span data-ttu-id="49dc0-109">Klicken Sie in der Struktur der **Gruppenrichtlinien-Verwaltungskonsole** in der Gesamtstruktur und Domäne, in der Sie GPOs verwalten möchten, auf **Steuerelement ändern** .</span><span class="sxs-lookup"><span data-stu-id="49dc0-109">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="49dc0-110">Klicken Sie auf der Registerkarte **Inhalt** auf die Registerkarte **Ausstehend** , um die ausstehenden GPOs anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="49dc0-110">On the **Contents** tab, click the **Pending** tab to display the pending GPOs.</span></span>

3.  <span data-ttu-id="49dc0-111">Klicken Sie mit der rechten Maustaste auf ein ausstehender GPO, und klicken Sie dann entweder auf **genehmigen** oder **ablehnen**.</span><span class="sxs-lookup"><span data-stu-id="49dc0-111">Right-click a pending GPO, and then click either **Approve** or **Reject**.</span></span>

4.  <span data-ttu-id="49dc0-112">Wenn Sie die Bereitstellung genehmigen, klicken Sie im Dialogfeld **ausstehender Vorgang genehmigen** auf **erweitert** , um Links zum Gruppenrichtlinienobjekt zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="49dc0-112">If approving deployment, click **Advanced** in the **Approve Pending Operation** dialog box to review links to the GPO.</span></span> <span data-ttu-id="49dc0-113">Zeigen Sie mit dem Mauszeiger auf ein Element in der Struktur, um Details anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="49dc0-113">Pause the mouse pointer on an item in the tree to display details.</span></span>

    -   <span data-ttu-id="49dc0-114">Standardmäßig werden alle Verknüpfungen mit dem Gruppenrichtlinienobjekt wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="49dc0-114">By default, all links to the GPO will be restored.</span></span>

    -   <span data-ttu-id="49dc0-115">Um zu verhindern, dass eine Verknüpfung wiederhergestellt wird, deaktivieren Sie das Kontrollkästchen für diesen Link.</span><span class="sxs-lookup"><span data-stu-id="49dc0-115">To prevent a link from being restored, clear the check box for that link.</span></span>

    -   <span data-ttu-id="49dc0-116">Um zu verhindern, dass alle Verknüpfungen wiederhergestellt werden, deaktivieren Sie das Kontrollkästchen **Verknüpfungen wiederherstellen** im Dialogfeld **Gruppenrichtlinienobjekt bereitstellen** .</span><span class="sxs-lookup"><span data-stu-id="49dc0-116">To prevent all links from being restored, clear the **Restore Links** check box in the **Deploy GPO** dialog box.</span></span>

5.  <span data-ttu-id="49dc0-117">Klicken Sie auf **Ja** oder **OK** , um die Genehmigung oder Ablehnung der ausstehenden Aktion zu bestätigen.</span><span class="sxs-lookup"><span data-stu-id="49dc0-117">Click **Yes** or **OK** to confirm approval or rejection of the pending action.</span></span> <span data-ttu-id="49dc0-118">Wenn Sie die Anforderung genehmigt haben, wird das Gruppenrichtlinienobjekt auf die entsprechende Registerkarte für die auszuführende Aktion verschoben.</span><span class="sxs-lookup"><span data-stu-id="49dc0-118">If you have approved the request, the GPO is moved to the appropriate tab for the action performed.</span></span>

    <span data-ttu-id="49dc0-119">**Hinweis**  Wenn die e-Mail-Adresse einer genehmigenden Person im Feld **an e-Mail-Adresse** auf der Registerkarte **Domänen** **Delegierung** enthalten ist, empfängt die genehmigende Person e-Mail-Nachrichten aus dem AGPM-Alias, wenn ein Bearbeiter oder Bearbeiter eine Anforderung absendet.</span><span class="sxs-lookup"><span data-stu-id="49dc0-119">**Note** If an Approver's e-mail address is included in the **To e-mail address** field on the **Domain** **Delegation** tab, the Approver will receive e-mail from the AGPM alias when an Editor or Reviewer submits a request.</span></span>

     

### <span data-ttu-id="49dc0-120">Weitere Überlegungen</span><span class="sxs-lookup"><span data-stu-id="49dc0-120">Additional considerations</span></span>

-   <span data-ttu-id="49dc0-121">Standardmäßig müssen Sie eine genehmigende Person oder ein AGPM-Administrator (Vollzugriff) sein, um dieses Verfahren ausführen zu können.</span><span class="sxs-lookup"><span data-stu-id="49dc0-121">By default, you must be an Approver or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="49dc0-122">Insbesondere müssen Sie über die erforderlichen Berechtigungen verfügen, um die von Ihnen genehmigte Anforderung ausführen zu können.</span><span class="sxs-lookup"><span data-stu-id="49dc0-122">Specifically, you must have the permissions required to perform the request that you are approving.</span></span>

### <span data-ttu-id="49dc0-123">Weitere Verweise</span><span class="sxs-lookup"><span data-stu-id="49dc0-123">Additional references</span></span>

-   [<span data-ttu-id="49dc0-124">Durchführen der Aufgaben von genehmigenden Personen</span><span class="sxs-lookup"><span data-stu-id="49dc0-124">Performing Approver Tasks</span></span>](performing-approver-tasks-agpm30ops.md)

 

 





