---
title: Anfordern der Wiederherstellung eines gelöschten Gruppenrichtlinienobjekts
description: Anfordern der Wiederherstellung eines gelöschten Gruppenrichtlinienobjekts
author: dansimp
ms.assetid: dcc3baea-8af7-4886-a301-98b6ac5819cd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f85620ed7d9afe676caabe4ce0f7da4fd8d5ae13
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808279"
---
# <span data-ttu-id="5d8e4-103">Anfordern der Wiederherstellung eines gelöschten Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="5d8e4-103">Request Restoration of a Deleted GPO</span></span>


<span data-ttu-id="5d8e4-104">Sofern Sie kein Genehmiger oder ein AGPM-Administrator (Vollzugriff) sind, müssen Sie die Wiederherstellung eines gelöschten Gruppenrichtlinienobjekts aus dem Papierkorb anfordern, um es in das Archiv zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="5d8e4-104">Unless you are an Approver or an AGPM Administrator (Full Control), you must request the restoration of a deleted Group Policy Object (GPO) from the Recycle Bin to return it to the archive.</span></span>

<span data-ttu-id="5d8e4-105">Um dieses Verfahren ausführen zu können, ist ein Benutzerkonto mit der Rolle "Editor" oder den erforderlichen Berechtigungen in Advanced Group Policy Management (AGPM) erforderlich.</span><span class="sxs-lookup"><span data-stu-id="5d8e4-105">A user account with the Editor role or necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span> <span data-ttu-id="5d8e4-106">Lesen Sie die Details unter "Weitere Überlegungen" in diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="5d8e4-106">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="5d8e4-107">So fordern Sie die Wiederherstellung eines gelöschten Gruppenrichtlinienobjekts an</span><span class="sxs-lookup"><span data-stu-id="5d8e4-107">To request the restoration of a deleted GPO</span></span>**

1.  <span data-ttu-id="5d8e4-108">Klicken Sie in der Struktur der **Gruppenrichtlinien-Verwaltungskonsole** in der Gesamtstruktur und Domäne, in der Sie GPOs verwalten möchten, auf **Steuerelement ändern** .</span><span class="sxs-lookup"><span data-stu-id="5d8e4-108">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="5d8e4-109">Klicken Sie auf der Registerkarte **Inhalt** auf die Registerkarte **Papierkorb** , um die gelöschten GPOs anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="5d8e4-109">On the **Contents** tab, click the **Recycle Bin** tab to display the deleted GPOs.</span></span>

3.  <span data-ttu-id="5d8e4-110">Klicken Sie mit der rechten Maustaste auf das GPO, das Sie wiederherstellen möchten, und klicken Sie dann auf **Wiederherstellen**.</span><span class="sxs-lookup"><span data-stu-id="5d8e4-110">Right-click the GPO you want to restore, and then click **Restore**.</span></span>

4.  <span data-ttu-id="5d8e4-111">Sofern Sie keine besondere Berechtigung zum Wiederherstellen von GPOs haben, müssen Sie eine Anforderung zur Wiederherstellung des gelöschten Gruppenrichtlinienobjekts übermitteln.</span><span class="sxs-lookup"><span data-stu-id="5d8e4-111">Unless you have special permission to restore GPOs, you must submit a request for restoration of the deleted GPO.</span></span> <span data-ttu-id="5d8e4-112">Wenn Sie eine Kopie der Anfrage erhalten möchten, geben Sie Ihre e-Mail-Adresse in das Feld **CC** ein.</span><span class="sxs-lookup"><span data-stu-id="5d8e4-112">To receive a copy of the request, type your e-mail address in the **Cc** field.</span></span> <span data-ttu-id="5d8e4-113">Geben Sie einen Kommentar ein, der im Überwachungspfad für das Gruppenrichtlinienobjekt angezeigt werden soll, und klicken Sie dann auf **Absenden**.</span><span class="sxs-lookup"><span data-stu-id="5d8e4-113">Type a comment to be displayed in the audit trail for the GPO, and then click **Submit**.</span></span>

5.  <span data-ttu-id="5d8e4-114">Wenn das **Status** Fenster angibt, dass der Gesamtfortschritt abgeschlossen ist, klicken Sie auf **Schließen**.</span><span class="sxs-lookup"><span data-stu-id="5d8e4-114">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="5d8e4-115">Das Gruppenrichtlinienobjekt wird von der Registerkarte " **Papierkorb** " entfernt und auf der Registerkarte " **gesteuert** " angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5d8e4-115">The GPO is removed from the **Recycle Bin** tab and is displayed on the **Controlled** tab.</span></span>

<span data-ttu-id="5d8e4-116">**Hinweis**  Wenn ein GPO aus der Produktionsumgebung gelöscht wurde, wird es nicht automatisch in der Produktionsumgebung erneut bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="5d8e4-116">**Note** If a GPO was deleted from the production environment, restoring it to the archive will not automatically redeploy it to the production environment.</span></span> <span data-ttu-id="5d8e4-117">Wenn Sie das Gruppenrichtlinienobjekt an die Produktionsumgebung zurückgeben möchten, stellen Sie das Gruppenrichtlinienobjekt bereit.</span><span class="sxs-lookup"><span data-stu-id="5d8e4-117">To return the GPO to the production environment, deploy the GPO.</span></span> <span data-ttu-id="5d8e4-118">Informationen finden Sie unter [Bereitstellen eines Gruppenrichtlinienobjekts](deploy-a-gpo-agpm30ops.md).</span><span class="sxs-lookup"><span data-stu-id="5d8e4-118">For information, see [Deploy a GPO](deploy-a-gpo-agpm30ops.md).</span></span>

 

### <span data-ttu-id="5d8e4-119">Weitere Überlegungen</span><span class="sxs-lookup"><span data-stu-id="5d8e4-119">Additional considerations</span></span>

-   <span data-ttu-id="5d8e4-120">Standardmäßig müssen Sie ein Editor sein, um dieses Verfahren ausführen zu können.</span><span class="sxs-lookup"><span data-stu-id="5d8e4-120">By default, you must be an Editor to perform this procedure.</span></span> <span data-ttu-id="5d8e4-121">Insbesondere müssen Sie über die Berechtigung " **Listeninhalt** " und " **Einstellungen bearbeiten** " für das Gruppenrichtlinienobjekt verfügen.</span><span class="sxs-lookup"><span data-stu-id="5d8e4-121">Specifically, you must have **List Contents** and **Edit Settings** permission for the GPO.</span></span>

-   <span data-ttu-id="5d8e4-122">Wenn Sie Ihre Anfrage zurücknehmen möchten, bevor Sie genehmigt wurde, klicken Sie auf die Registerkarte **Ausstehend** . Klicken Sie mit der rechten Maustaste auf das GPO, und klicken Sie dann auf **zurück**</span><span class="sxs-lookup"><span data-stu-id="5d8e4-122">To withdraw your request before it has been approved, click the **Pending** tab. Right-click the GPO, and then click **Withdraw**.</span></span> <span data-ttu-id="5d8e4-123">Das Gruppenrichtlinienobjekt wird auf die Registerkarte **Papierkorb** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="5d8e4-123">The GPO will be returned to the **Recycle Bin** tab.</span></span>

### <span data-ttu-id="5d8e4-124">Weitere Verweise</span><span class="sxs-lookup"><span data-stu-id="5d8e4-124">Additional references</span></span>

-   [<span data-ttu-id="5d8e4-125">Löschen, Wiederherstellen oder Zerstören eines Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="5d8e4-125">Deleting, Restoring, or Destroying a GPO</span></span>](deleting-restoring-or-destroying-a-gpo-agpm30ops.md)

 

 





