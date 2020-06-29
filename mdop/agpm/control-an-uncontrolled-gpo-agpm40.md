---
title: Steuern eines nicht gesteuerten Gruppenrichtlinienobjekts
description: Steuern eines nicht gesteuerten Gruppenrichtlinienobjekts
author: dansimp
ms.assetid: dc81545c-8da5-4b6f-b266-f01a82e27c6b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 418e2a4100e1d824198b7d05034443948ec8a44c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807692"
---
# <span data-ttu-id="3d360-103">Steuern eines nicht gesteuerten Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="3d360-103">Control an Uncontrolled GPO</span></span>


<span data-ttu-id="3d360-104">Wenn Sie das Änderungs Steuerelement für ein Gruppenrichtlinienobjekt (GPO) bereitstellen möchten, müssen Sie zuerst das Gruppenrichtlinienobjekt steuern.</span><span class="sxs-lookup"><span data-stu-id="3d360-104">To provide change control for a Group Policy Object (GPO), you must first control the GPO.</span></span>

<span data-ttu-id="3d360-105">Zum Ausführen dieses Verfahrens ist ein Benutzerkonto mit der Rolle Genehmiger oder AGPM-Administrator (Vollzugriff) oder den erforderlichen Berechtigungen in der erweiterten Gruppenrichtlinienverwaltung (Group Policy Management, AGPM) erforderlich.</span><span class="sxs-lookup"><span data-stu-id="3d360-105">A user account with the Approver or AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span> <span data-ttu-id="3d360-106">Lesen Sie die Details unter "Weitere Überlegungen" in diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="3d360-106">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="3d360-107">So steuern Sie ein nicht gesteuertes Gruppenrichtlinienobjekt</span><span class="sxs-lookup"><span data-stu-id="3d360-107">To control an uncontrolled GPO</span></span>**

1.  <span data-ttu-id="3d360-108">Klicken Sie in der Struktur der **Gruppenrichtlinien-Verwaltungskonsole** in der Gesamtstruktur und Domäne, in der Sie GPOs verwalten möchten, auf **Steuerelement ändern** .</span><span class="sxs-lookup"><span data-stu-id="3d360-108">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="3d360-109">Klicken Sie im Detailbereich auf der Registerkarte **Inhalt** auf die Registerkarte **unkontrolliert** , um die nicht kontrollierten GPOs anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="3d360-109">On the **Contents** tab in the details pane, click the **Uncontrolled** tab to display the uncontrolled GPOs.</span></span>

3.  <span data-ttu-id="3d360-110">Klicken Sie mit der rechten Maustaste auf das Gruppenrichtlinienobjekt, das mit AGPM gesteuert werden soll, und klicken Sie dann auf **Steuerelement**.</span><span class="sxs-lookup"><span data-stu-id="3d360-110">Right-click the GPO to be controlled with AGPM, and then click **Control**.</span></span>

4.  <span data-ttu-id="3d360-111">Geben Sie einen Kommentar ein, der im Verlauf des Gruppenrichtlinienobjekts angezeigt werden soll, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="3d360-111">Type a comment to be displayed in the history of the GPO, and then click **OK**.</span></span>

5.  <span data-ttu-id="3d360-112">Wenn das **Status** Fenster angibt, dass der Gesamtfortschritt abgeschlossen ist, klicken Sie auf **Schließen**.</span><span class="sxs-lookup"><span data-stu-id="3d360-112">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="3d360-113">Das Gruppenrichtlinienobjekt wird auf der Registerkarte **unkontrolliert** aus der Liste entfernt und der Registerkarte **gesteuert** hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3d360-113">The GPO is removed from the list on the **Uncontrolled** tab and added to the **Controlled** tab.</span></span>

### <span data-ttu-id="3d360-114">Weitere Überlegungen</span><span class="sxs-lookup"><span data-stu-id="3d360-114">Additional considerations</span></span>

-   <span data-ttu-id="3d360-115">Standardmäßig müssen Sie eine genehmigende Person oder ein AGPM-Administrator (Vollzugriff) sein, um dieses Verfahren ausführen zu können.</span><span class="sxs-lookup"><span data-stu-id="3d360-115">By default, you must be an Approver or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="3d360-116">Insbesondere müssen Sie über **Listeninhalte** und Berechtigungen zum **Erstellen von Gruppenrichtlinienobjekten** für die Domäne verfügen.</span><span class="sxs-lookup"><span data-stu-id="3d360-116">Specifically, you must have **List Contents** and **Create GPO** permissions for the domain.</span></span>

### <span data-ttu-id="3d360-117">Weitere Verweise</span><span class="sxs-lookup"><span data-stu-id="3d360-117">Additional references</span></span>

-   [<span data-ttu-id="3d360-118">Erstellen oder Steuern eines Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="3d360-118">Creating or Controlling a GPO</span></span>](creating-or-controlling-a-gpo-agpm40-app.md)

 

 





