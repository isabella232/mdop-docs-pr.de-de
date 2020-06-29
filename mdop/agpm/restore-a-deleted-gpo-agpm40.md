---
title: Wiederherstellen eines gelöschten Gruppenrichtlinienobjekts
description: Wiederherstellen eines gelöschten Gruppenrichtlinienobjekts
author: dansimp
ms.assetid: 0a131d26-a741-4a51-b612-c0bc7dbba06b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 14fdf2f74f2d3db4be0db1aab7c185f5c1ab2cd1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807500"
---
# <span data-ttu-id="7d160-103">Wiederherstellen eines gelöschten Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="7d160-103">Restore a Deleted GPO</span></span>


<span data-ttu-id="7d160-104">Genehmigende Personen können ein gelöschtes Gruppenrichtlinienobjekt (GPO) aus dem Papierkorb wiederherstellen und an das Archiv zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="7d160-104">Approvers can restore a deleted Group Policy Object (GPO) from the Recycle Bin, returning it to the archive.</span></span>

<span data-ttu-id="7d160-105">Zum Ausführen dieses Verfahrens ist ein Benutzerkonto mit der Rolle Genehmiger oder AGPM-Administrator (Vollzugriff) oder den erforderlichen Berechtigungen in der erweiterten Gruppenrichtlinienverwaltung (Group Policy Management, AGPM) erforderlich.</span><span class="sxs-lookup"><span data-stu-id="7d160-105">A user account with the Approver or AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span> <span data-ttu-id="7d160-106">Lesen Sie die Details unter "Weitere Überlegungen" in diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="7d160-106">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="7d160-107">So stellen Sie ein gelöschtes Gruppenrichtlinienobjekt wieder her</span><span class="sxs-lookup"><span data-stu-id="7d160-107">To restore a deleted GPO</span></span>**

1.  <span data-ttu-id="7d160-108">Klicken Sie in der Struktur der **Gruppenrichtlinien-Verwaltungskonsole** in der Gesamtstruktur und Domäne, in der Sie GPOs verwalten möchten, auf **Steuerelement ändern** .</span><span class="sxs-lookup"><span data-stu-id="7d160-108">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="7d160-109">Klicken Sie auf der Registerkarte **Inhalt** auf die Registerkarte **Papierkorb** , um die gelöschten GPOs anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="7d160-109">On the **Contents** tab, click the **Recycle Bin** tab to display the deleted GPOs.</span></span>

3.  <span data-ttu-id="7d160-110">Klicken Sie mit der rechten Maustaste auf das wiederherzustellende GPO, und klicken Sie dann auf **Wiederherstellen**.</span><span class="sxs-lookup"><span data-stu-id="7d160-110">Right-click the GPO to restore, and then click **Restore**.</span></span>

4.  <span data-ttu-id="7d160-111">Geben Sie einen Kommentar ein, der im Verlauf des Gruppenrichtlinienobjekts angezeigt werden soll, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="7d160-111">Type a comment to be displayed in the history of the GPO, and then click **OK**.</span></span>

5.  <span data-ttu-id="7d160-112">Wenn das **Status** Fenster angibt, dass der Gesamtfortschritt abgeschlossen ist, klicken Sie auf **Schließen**.</span><span class="sxs-lookup"><span data-stu-id="7d160-112">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="7d160-113">Das Gruppenrichtlinienobjekt wird von der Registerkarte " **Papierkorb** " entfernt und auf der Registerkarte " **gesteuert** " angezeigt.</span><span class="sxs-lookup"><span data-stu-id="7d160-113">The GPO is removed from the **Recycle Bin** tab and is displayed on the **Controlled** tab.</span></span>

<span data-ttu-id="7d160-114">**Hinweis**  Wenn ein GPO aus der Produktionsumgebung gelöscht wurde, wird es nicht automatisch in der Produktionsumgebung erneut bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="7d160-114">**Note** If a GPO was deleted from the production environment, restoring it to the archive will not automatically redeploy it to the production environment.</span></span> <span data-ttu-id="7d160-115">Wenn Sie das Gruppenrichtlinienobjekt an die Produktionsumgebung zurückgeben möchten, stellen Sie das Gruppenrichtlinienobjekt bereit.</span><span class="sxs-lookup"><span data-stu-id="7d160-115">To return the GPO to the production environment, deploy the GPO.</span></span> <span data-ttu-id="7d160-116">Informationen finden Sie unter [Bereitstellen eines Gruppenrichtlinienobjekts](deploy-a-gpo-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="7d160-116">For information, see [Deploy a GPO](deploy-a-gpo-agpm40.md).</span></span>

 

### <span data-ttu-id="7d160-117">Weitere Überlegungen</span><span class="sxs-lookup"><span data-stu-id="7d160-117">Additional considerations</span></span>

-   <span data-ttu-id="7d160-118">Standardmäßig müssen Sie eine genehmigende Person oder ein AGPM-Administrator (Vollzugriff) sein, um dieses Verfahren ausführen zu können.</span><span class="sxs-lookup"><span data-stu-id="7d160-118">By default, you must be an Approver or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="7d160-119">Insbesondere müssen Sie über **Listeninhalte** verfügen und entweder **Gruppenrichtlinienobjekte bereitstellen** oder GPO-Berechtigungen **Löschen** .</span><span class="sxs-lookup"><span data-stu-id="7d160-119">Specifically, you must have **List Contents** and either **Deploy GPO** or **Delete GPO** permissions for the GPO.</span></span>

### <span data-ttu-id="7d160-120">Weitere Verweise</span><span class="sxs-lookup"><span data-stu-id="7d160-120">Additional references</span></span>

-   [<span data-ttu-id="7d160-121">Löschen, Wiederherstellen oder Zerstören eines Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="7d160-121">Deleting, Restoring, or Destroying a GPO</span></span>](deleting-restoring-or-destroying-a-gpo-agpm40.md)

 

 





