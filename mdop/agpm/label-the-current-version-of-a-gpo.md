---
title: Beschriften der aktuellen Version eines Gruppenrichtlinienobjekts
description: Beschriften der aktuellen Version eines Gruppenrichtlinienobjekts
author: dansimp
ms.assetid: 5e4e50f8-e4a8-4bda-aac4-1569d5fbd6a7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a34232dfd1f7a755dd81cdecbe3d5d1957f01294
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808383"
---
# <span data-ttu-id="98224-103">Beschriften der aktuellen Version eines Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="98224-103">Label the Current Version of a GPO</span></span>


<span data-ttu-id="98224-104">Sie können die aktuelle Version eines Gruppenrichtlinienobjekts zur einfachen Identifizierung in seinem Protokoll beschriften.</span><span class="sxs-lookup"><span data-stu-id="98224-104">You can label the current version of a Group Policy object (GPO) for easy identification in its history.</span></span> <span data-ttu-id="98224-105">Sie können eine Bezeichnung verwenden, um eine zweifelsfrei funktionierende Version zu identifizieren, bei der ein Rollback ausgeführt werden kann, wenn ein Problem auftritt.</span><span class="sxs-lookup"><span data-stu-id="98224-105">You can use a label to identify a known good version to which you could roll back if a problem occurs.</span></span> <span data-ttu-id="98224-106">Wenn Sie mehrere GPOs gleichzeitig mit demselben Etikett versehen, können Sie auch Verwandte GPOs kennzeichnen, für die ein Rollback zum gleichen Zeitpunkt ausgeführt werden soll, wenn später ein Rollback erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="98224-106">Also, by labeling multiple GPOs with the same label at one time, you can mark related GPOs that should be rolled back to the same point if rollback should later be necessary.</span></span>

<span data-ttu-id="98224-107">Zum Ausführen dieses Verfahrens ist ein Benutzerkonto mit der Rolle "Editor", "Genehmiger" oder "AGPM-Administrator" (Vollzugriff) oder den erforderlichen Berechtigungen in der erweiterten Gruppenrichtlinienverwaltung erforderlich.</span><span class="sxs-lookup"><span data-stu-id="98224-107">A user account with the Editor, Approver, or AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management is required to complete this procedure.</span></span> <span data-ttu-id="98224-108">Lesen Sie die Details unter "Weitere Überlegungen" in diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="98224-108">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="98224-109">So beschriften Sie die aktuelle Version von GPOs in ihren Verlaufsdaten</span><span class="sxs-lookup"><span data-stu-id="98224-109">To label the current version of GPOs in their histories</span></span>**

1.  <span data-ttu-id="98224-110">Klicken Sie in der Struktur der **Gruppenrichtlinien-Verwaltungskonsole** in der Gesamtstruktur und Domäne, in der Sie GPOs verwalten möchten, auf **Steuerelement ändern** .</span><span class="sxs-lookup"><span data-stu-id="98224-110">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="98224-111">Klicken Sie auf der Registerkarte **Inhalt** auf die Registerkarte **gesteuert** , um die gesteuerten GPOs anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="98224-111">On the **Contents** tab, click the **Controlled** tab to display the controlled GPOs.</span></span>

3.  <span data-ttu-id="98224-112">Klicken Sie auf ein GPO, für das die aktuelle Version beschriftet werden soll.</span><span class="sxs-lookup"><span data-stu-id="98224-112">Click a GPO for which to label the current version.</span></span> <span data-ttu-id="98224-113">Wenn Sie mehrere GPOs auswählen möchten, drücken Sie die UMSCHALTTASTE, und klicken Sie auf das letzte GPO in einer zusammenhängenden Gruppe von GPOs, oder drücken Sie STRG, und klicken Sie auf einzelne GPOs.</span><span class="sxs-lookup"><span data-stu-id="98224-113">To select multiple GPOs, press SHIFT and click the last GPO in a contiguous group of GPOs, or press CTRL and click individual GPOs.</span></span> <span data-ttu-id="98224-114">Klicken Sie mit der rechten Maustaste auf ein ausgewähltes Gruppenrichtlinienobjekt, und klicken Sie dann auf **Beschriftung**.</span><span class="sxs-lookup"><span data-stu-id="98224-114">Right-click a selected GPO, and then click **Label**.</span></span>

4.  <span data-ttu-id="98224-115">Geben Sie eine Beschriftung und einen Kommentar ein, die im Verlauf der einzelnen ausgewählten Gruppenrichtlinienobjekte angezeigt werden sollen, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="98224-115">Type a label and a comment to be displayed in the history of each GPO selected, and then click **OK**.</span></span>

5.  <span data-ttu-id="98224-116">Wenn das **Status** Fenster angibt, dass der Gesamtfortschritt abgeschlossen ist, klicken Sie auf **Schließen**.</span><span class="sxs-lookup"><span data-stu-id="98224-116">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span>

### <span data-ttu-id="98224-117">Weitere Überlegungen</span><span class="sxs-lookup"><span data-stu-id="98224-117">Additional considerations</span></span>

-   <span data-ttu-id="98224-118">Standardmäßig müssen Sie ein Editor, eine genehmigende Person oder ein AGPM-Administrator (Vollzugriff) sein, um dieses Verfahren ausführen zu können.</span><span class="sxs-lookup"><span data-stu-id="98224-118">By default, you must be an Editor, an Approver, or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="98224-119">Insbesondere müssen Sie über **Listeninhalte** und entweder **Einstellungen bearbeiten** oder GPO-Berechtigungen für das Gruppenrichtlinienobjekt **Bereitstellen** .</span><span class="sxs-lookup"><span data-stu-id="98224-119">Specifically, you must have **List Contents** and either **Edit Settings** or **Deploy GPO** permissions for the GPO.</span></span>

### <span data-ttu-id="98224-120">Weitere Verweise</span><span class="sxs-lookup"><span data-stu-id="98224-120">Additional references</span></span>

-   [<span data-ttu-id="98224-121">Bearbeiten eines Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="98224-121">Editing a GPO</span></span>](editing-a-gpo.md)

 

 





