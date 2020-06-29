---
title: Benennen Sie ein Gruppenrichtlinienobjekt oder eine Vorlage
description: Benennen Sie ein Gruppenrichtlinienobjekt oder eine Vorlage
author: dansimp
ms.assetid: 84293f7a-4ff7-497e-bdbc-cabb70189a03
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 642622ae0242e614733e8f33ea5840c8b6758db8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807536"
---
# <span data-ttu-id="d797e-103">Benennen Sie ein Gruppenrichtlinienobjekt oder eine Vorlage</span><span class="sxs-lookup"><span data-stu-id="d797e-103">Rename a GPO or Template</span></span>


<span data-ttu-id="d797e-104">Sie können ein gesteuertes Gruppenrichtlinienobjekt oder eine Vorlage umbenennen.</span><span class="sxs-lookup"><span data-stu-id="d797e-104">You can rename a controlled Group Policy Object (GPO) or a template.</span></span>

<span data-ttu-id="d797e-105">Ein Benutzerkonto mit der Rolle "Editor" oder "AGPM-Administrator (Vollzugriff)", das Benutzerkonto der genehmigenden Person, die das Gruppenrichtlinienobjekt erstellt hat, oder ein Benutzerkonto mit den erforderlichen Berechtigungen in Advanced Group Policy Management (AGPM) ist erforderlich, um dieses Verfahren ausführen zu können.</span><span class="sxs-lookup"><span data-stu-id="d797e-105">A user account with the Editor or AGPM Administrator (Full Control) role, the user account of the Approver who created the GPO, or a user account with the necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span> <span data-ttu-id="d797e-106">Lesen Sie die Details unter "Weitere Überlegungen" in diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="d797e-106">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="d797e-107">So benennen Sie ein GPO oder eine Vorlage um</span><span class="sxs-lookup"><span data-stu-id="d797e-107">To rename a GPO or template</span></span>**

1.  <span data-ttu-id="d797e-108">Klicken Sie in der Struktur der **Gruppenrichtlinien-Verwaltungskonsole** in der Gesamtstruktur und Domäne, in der Sie GPOs verwalten möchten, auf **Steuerelement ändern** .</span><span class="sxs-lookup"><span data-stu-id="d797e-108">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="d797e-109">Klicken Sie auf der Registerkarte **Inhalt** auf die Registerkarte **gesteuert** oder **Vorlagen** , um das umzubenennende Element anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="d797e-109">On the **Contents** tab, click the **Controlled** or **Templates** tab to display the item to rename.</span></span>

3.  <span data-ttu-id="d797e-110">Klicken Sie mit der rechten Maustaste auf das zu umbenennende GPO oder die Vorlage, und klicken Sie auf **Umbenennen**.</span><span class="sxs-lookup"><span data-stu-id="d797e-110">Right-click the GPO or template to rename and click **Rename**.</span></span>

4.  <span data-ttu-id="d797e-111">Geben Sie den neuen Namen für das Gruppenrichtlinienobjekt oder die Vorlage und einen Kommentar ein, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="d797e-111">Type the new name for the GPO or template and a comment, and then click **OK**.</span></span>

5.  <span data-ttu-id="d797e-112">Wenn das **Status** Fenster angibt, dass der Gesamtfortschritt abgeschlossen ist, klicken Sie auf **Schließen**.</span><span class="sxs-lookup"><span data-stu-id="d797e-112">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="d797e-113">Das Gruppenrichtlinienobjekt oder die Vorlage wird auf der Registerkarte **Inhalt** unter dem neuen Namen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d797e-113">The GPO or template appears under the new name on the **Contents** tab.</span></span>

### <span data-ttu-id="d797e-114">Weitere Überlegungen</span><span class="sxs-lookup"><span data-stu-id="d797e-114">Additional considerations</span></span>

-   <span data-ttu-id="d797e-115">Standardmäßig müssen Sie die genehmigende Person sein, die das Gruppenrichtlinienobjekt, einen Editor oder einen AGPM-Administrator (Vollzugriff) erstellt oder gesteuert hat, um dieses Verfahren ausführen zu können.</span><span class="sxs-lookup"><span data-stu-id="d797e-115">By default, you must be the Approver who created or controlled the GPO, an Editor, or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="d797e-116">Insbesondere müssen Sie über die Berechtigung " **Listeninhalt** " und " **Einstellungen bearbeiten** " für das Gruppenrichtlinienobjekt verfügen.</span><span class="sxs-lookup"><span data-stu-id="d797e-116">Specifically, you must have **List Contents** and **Edit Settings** permission for the GPO.</span></span>

-   <span data-ttu-id="d797e-117">Wenn Sie ein bereitgestelltes GPO umbenennen, wird der Name sofort im Archiv geändert.</span><span class="sxs-lookup"><span data-stu-id="d797e-117">When you rename a GPO that has been deployed, the name is immediately changed in the archive.</span></span> <span data-ttu-id="d797e-118">Der Name wird in der Produktionsumgebung nur geändert, wenn das Gruppenrichtlinienobjekt erneut bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="d797e-118">The name is changed in the production environment only when the GPO is redeployed.</span></span> <span data-ttu-id="d797e-119">Bis das Gruppenrichtlinienobjekt erneut bereitgestellt wird (oder die Produktionskopie gelöscht wird), wird der alte Name noch in der Produktionsumgebung verwendet und kann daher nicht für ein anderes GPO verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d797e-119">Until the GPO is redeployed (or the production copy is deleted), the old name is still in use in the production environment and therefore cannot be used for another GPO.</span></span> <span data-ttu-id="d797e-120">Ebenso kann das Gruppenrichtlinienobjekt im Archiv erst wieder in seinen ursprünglichen Namen umbenannt werden, nachdem das Gruppenrichtlinienobjekt bereitgestellt wurde (Ändern des Namens der Produktionskopie) oder die Produktionskopie gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="d797e-120">Likewise, the GPO in the archive cannot be renamed back to its original name until the GPO has been deployed (changing the name of the production copy) or the production copy has been deleted.</span></span>

### <span data-ttu-id="d797e-121">Weitere Verweise</span><span class="sxs-lookup"><span data-stu-id="d797e-121">Additional references</span></span>

-   [<span data-ttu-id="d797e-122">Bearbeiten eines Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="d797e-122">Editing a GPO</span></span>](editing-a-gpo-agpm40.md)

 

 





