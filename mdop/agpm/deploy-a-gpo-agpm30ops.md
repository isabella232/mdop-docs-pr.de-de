---
title: Bereitstellen eines Gruppenrichtlinienobjekts
description: Bereitstellen eines Gruppenrichtlinienobjekts
author: dansimp
ms.assetid: 3767b722-db43-40f1-a714-bb8e38bcaa10
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 71c08a3b2d4f5af5bc7f1b69f964e9bb707d889c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808496"
---
# <span data-ttu-id="f41e9-103">Bereitstellen eines Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="f41e9-103">Deploy a GPO</span></span>


<span data-ttu-id="f41e9-104">Eine genehmigende Person kann ein neues oder bearbeitetes Gruppenrichtlinienobjekt (GPO) in der Produktionsumgebung bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="f41e9-104">An Approver can deploy a new or edited Group Policy Object (GPO) to the production environment.</span></span> <span data-ttu-id="f41e9-105">Informationen zum erneuten Bereitstelleneiner früheren Version eines GPO finden Sie unter [Zurücksetzen auf eine frühere Version eines Gruppenrichtlinienobjekts](roll-back-to-a-previous-version-of-a-gpo-agpm30ops.md).</span><span class="sxs-lookup"><span data-stu-id="f41e9-105">For information about redeploying a previous version of a GPO, see [Roll Back to a Previous Version of a GPO](roll-back-to-a-previous-version-of-a-gpo-agpm30ops.md).</span></span>

<span data-ttu-id="f41e9-106">Zum Ausführen dieses Verfahrens ist ein Benutzerkonto mit der Rolle Genehmiger oder AGPM-Administrator (Vollzugriff) oder den erforderlichen Berechtigungen in der erweiterten Gruppenrichtlinienverwaltung (Group Policy Management, AGPM) erforderlich.</span><span class="sxs-lookup"><span data-stu-id="f41e9-106">A user account with the Approver or AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span> <span data-ttu-id="f41e9-107">Lesen Sie die Details unter "Weitere Überlegungen" in diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="f41e9-107">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="f41e9-108">So stellen Sie ein GPO in der Produktionsumgebung bereit</span><span class="sxs-lookup"><span data-stu-id="f41e9-108">To deploy a GPO to the production environment</span></span>**

1.  <span data-ttu-id="f41e9-109">Klicken Sie in der Struktur der **Gruppenrichtlinien-Verwaltungskonsole** in der Gesamtstruktur und Domäne, in der Sie GPOs verwalten möchten, auf **Steuerelement ändern** .</span><span class="sxs-lookup"><span data-stu-id="f41e9-109">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="f41e9-110">Klicken Sie auf der Registerkarte **Inhalt** auf die Registerkarte **gesteuert** , um die gesteuerten GPOs anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="f41e9-110">On the **Contents** tab, click the **Controlled** tab to display the controlled GPOs.</span></span>

3.  <span data-ttu-id="f41e9-111">Klicken Sie mit der rechten Maustaste auf das zu implementierende GPO, und klicken Sie dann auf **Bereitstellen**.</span><span class="sxs-lookup"><span data-stu-id="f41e9-111">Right-click the GPO to be deployed and then click **Deploy**.</span></span>

4.  <span data-ttu-id="f41e9-112">Klicken Sie auf **erweitert**, um Links zu dem Gruppenrichtlinienobjekt zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="f41e9-112">To review links to the GPO, click **Advanced**.</span></span> <span data-ttu-id="f41e9-113">Zeigen Sie mit dem Mauszeiger auf ein Element in der Struktur, um Details anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="f41e9-113">Pause the mouse pointer on an item in the tree to display details.</span></span>

    -   <span data-ttu-id="f41e9-114">Standardmäßig werden alle Verknüpfungen mit dem Gruppenrichtlinienobjekt wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="f41e9-114">By default, all links to the GPO will be restored.</span></span>

    -   <span data-ttu-id="f41e9-115">Um zu verhindern, dass eine Verknüpfung wiederhergestellt wird, deaktivieren Sie das Kontrollkästchen für diesen Link.</span><span class="sxs-lookup"><span data-stu-id="f41e9-115">To prevent a link from being restored, clear the check box for that link.</span></span>

    -   <span data-ttu-id="f41e9-116">Um zu verhindern, dass alle Verknüpfungen wiederhergestellt werden, deaktivieren Sie das Kontrollkästchen **Verknüpfungen wiederherstellen** im Dialogfeld **Gruppenrichtlinienobjekt bereitstellen** .</span><span class="sxs-lookup"><span data-stu-id="f41e9-116">To prevent all links from being restored, clear the **Restore Links** check box in the **Deploy GPO** dialog box.</span></span>

5.  <span data-ttu-id="f41e9-117">Klicken Sie auf **Ja**.</span><span class="sxs-lookup"><span data-stu-id="f41e9-117">Click **Yes**.</span></span> <span data-ttu-id="f41e9-118">Wenn das **Status** Fenster angibt, dass der Gesamtfortschritt abgeschlossen ist, klicken Sie auf **Schließen**.</span><span class="sxs-lookup"><span data-stu-id="f41e9-118">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span>

<span data-ttu-id="f41e9-119">**Hinweis**  Um zu überprüfen, ob die neueste Version eines GPO bereitgestellt wurde, doppelklicken Sie auf der Registerkarte **gesteuert** auf das Gruppenrichtlinienobjekt, um dessen **Verlauf**anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="f41e9-119">**Note** To verify whether the most recent version of a GPO has been deployed, on the **Controlled** tab, double-click the GPO to display its **History**.</span></span> <span data-ttu-id="f41e9-120">Im **Protokoll** für das Gruppenrichtlinienobjekt gibt die Spalte **Status** an, ob ein GPO bereitgestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="f41e9-120">In the **History** for the GPO, the **State** column indicates whether a GPO has been deployed.</span></span>

 

### <span data-ttu-id="f41e9-121">Weitere Überlegungen</span><span class="sxs-lookup"><span data-stu-id="f41e9-121">Additional considerations</span></span>

-   <span data-ttu-id="f41e9-122">Standardmäßig müssen Sie eine genehmigende Person oder ein AGPM-Administrator (Vollzugriff) sein, um dieses Verfahren ausführen zu können.</span><span class="sxs-lookup"><span data-stu-id="f41e9-122">By default, you must be an Approver or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="f41e9-123">Insbesondere müssen Sie über **Listeninhalte** und Berechtigungen zum **Bereitstellen von Gruppenrichtlinienobjekten** für das Gruppenrichtlinienobjekt verfügen.</span><span class="sxs-lookup"><span data-stu-id="f41e9-123">Specifically, you must have **List Contents** and **Deploy GPO** permissions for the GPO.</span></span>

### <span data-ttu-id="f41e9-124">Weitere Verweise</span><span class="sxs-lookup"><span data-stu-id="f41e9-124">Additional references</span></span>

-   [<span data-ttu-id="f41e9-125">Durchführen der Aufgaben von genehmigenden Personen</span><span class="sxs-lookup"><span data-stu-id="f41e9-125">Performing Approver Tasks</span></span>](performing-approver-tasks-agpm30ops.md)

 

 





