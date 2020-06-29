---
title: Einchecken eines Gruppenrichtlinienobjekts
description: Einchecken eines Gruppenrichtlinienobjekts
author: dansimp
ms.assetid: 437397db-c94b-4940-b1a4-05442619ebee
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8c37144cb7c2d150d46dd1172a37717743f76ee3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807807"
---
# <span data-ttu-id="35f0b-103">Einchecken eines Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="35f0b-103">Check In a GPO</span></span>


<span data-ttu-id="35f0b-104">In der Regel sollten Editoren Gruppenrichtlinienobjekte (Group Policy Objects, GPOs) überprüfen, die Sie bearbeitet haben, wenn Ihre Änderungen abgeschlossen sind.</span><span class="sxs-lookup"><span data-stu-id="35f0b-104">Ordinarily, Editors should check in Group Policy Objects (GPOs) that they have edited when their modifications are complete.</span></span> <span data-ttu-id="35f0b-105">(Ausführliche Informationen finden Sie unter [Bearbeiten eines GPO Offline](edit-a-gpo-offline-agpm30ops.md).) Wenn der Editor jedoch nicht zur Verfügung steht, kann eine genehmigende Person auch ein GPO einchecken.</span><span class="sxs-lookup"><span data-stu-id="35f0b-105">(For details, see [Edit a GPO Offline](edit-a-gpo-offline-agpm30ops.md).) However, if the Editor is unavailable, an Approver can also check in a GPO.</span></span>

<span data-ttu-id="35f0b-106">Zum Ausführen dieses Verfahrens ist ein Benutzerkonto mit der Rolle "Editor", "Genehmiger" oder "AGPM-Administrator" (Vollzugriff) oder den erforderlichen Berechtigungen in der erweiterten Gruppenrichtlinienverwaltung (AGPM) erforderlich.</span><span class="sxs-lookup"><span data-stu-id="35f0b-106">A user account with the Editor, Approver, or AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span> <span data-ttu-id="35f0b-107">Lesen Sie die Details unter "Weitere Überlegungen" in diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="35f0b-107">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="35f0b-108">So checken Sie ein Gruppenrichtlinienobjekt ein, das von einem Editor ausgecheckt wurde</span><span class="sxs-lookup"><span data-stu-id="35f0b-108">To check in a GPO that has been checked out by an Editor</span></span>**

1.  <span data-ttu-id="35f0b-109">Klicken Sie in der Struktur der **Gruppenrichtlinien-Verwaltungskonsole** in der Gesamtstruktur und Domäne, in der Sie GPOs verwalten möchten, auf **Steuerelement ändern** .</span><span class="sxs-lookup"><span data-stu-id="35f0b-109">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="35f0b-110">Klicken Sie auf der Registerkarte **Inhalt** auf die Registerkarte **gesteuert** , um die gesteuerten GPOs anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="35f0b-110">On the **Contents** tab, click the **Controlled** tab to display the controlled GPOs.</span></span>

    -   <span data-ttu-id="35f0b-111">Wenn Sie alle Änderungen des Editors verwerfen möchten, klicken Sie mit der rechten Maustaste auf das Gruppenrichtlinienobjekt, klicken Sie auf **Auschecken rückgängig machen**, und klicken Sie dann zum bestätigen auf **Ja** .</span><span class="sxs-lookup"><span data-stu-id="35f0b-111">To discard any changes made by the Editor, right-click the GPO, click **Undo Check Out**, and then click **Yes** to confirm.</span></span>

    -   <span data-ttu-id="35f0b-112">Um die vom Editor vorgenommenen Änderungen beizubehalten, klicken Sie mit der rechten Maustaste auf das Gruppenrichtlinienobjekt, und klicken Sie dann auf **Einchecken**.</span><span class="sxs-lookup"><span data-stu-id="35f0b-112">To retain changes made by the Editor, right-click the GPO and then click **Check In**.</span></span>

3.  <span data-ttu-id="35f0b-113">Geben Sie einen Kommentar ein, der im Überwachungspfad des Gruppenrichtlinienobjekts angezeigt werden soll, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="35f0b-113">Type a comment to be displayed in the audit trail of the GPO, and then click **OK**.</span></span>

4.  <span data-ttu-id="35f0b-114">Wenn das **Status** Fenster angibt, dass der Gesamtfortschritt abgeschlossen ist, klicken Sie auf **Schließen**.</span><span class="sxs-lookup"><span data-stu-id="35f0b-114">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="35f0b-115">Auf der Registerkarte **gesteuert** wird der Status des Gruppenrichtlinienobjekts als **eingecheckt**gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="35f0b-115">On the **Controlled** tab, the state of the GPO is identified as **Checked In**.</span></span>

### <span data-ttu-id="35f0b-116">Weitere Überlegungen</span><span class="sxs-lookup"><span data-stu-id="35f0b-116">Additional considerations</span></span>

-   <span data-ttu-id="35f0b-117">Standardmäßig müssen Sie ein Editor, eine genehmigende Person oder ein AGPM-Administrator (Vollzugriff) sein, um dieses Verfahren ausführen zu können.</span><span class="sxs-lookup"><span data-stu-id="35f0b-117">By default, you must be an Editor, an Approver, or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="35f0b-118">Insbesondere müssen Sie über **Listeninhalte** und entweder **Einstellungen bearbeiten** oder GPO-Berechtigungen für das Gruppenrichtlinienobjekt **Bereitstellen** .</span><span class="sxs-lookup"><span data-stu-id="35f0b-118">Specifically, you must have **List Contents** and either **Edit Settings** or **Deploy GPO** permissions for the GPO.</span></span> <span data-ttu-id="35f0b-119">Wenn Sie kein genehmigender oder AGPM-Administrator (oder ein anderer Gruppenrichtlinienadministrator mit der Berechtigung " **GPO bereitstellen** ") sind, müssen Sie der Herausgeber sein, der das Gruppenrichtlinienobjekt ausgecheckt hat.</span><span class="sxs-lookup"><span data-stu-id="35f0b-119">If you are not an Approver or AGPM Administrator (or other Group Policy administrator with **Deploy GPO** permission), you must be the Editor who has checked out the GPO.</span></span>

### <span data-ttu-id="35f0b-120">Weitere Verweise</span><span class="sxs-lookup"><span data-stu-id="35f0b-120">Additional references</span></span>

-   [<span data-ttu-id="35f0b-121">Durchführen der Aufgaben von genehmigenden Personen</span><span class="sxs-lookup"><span data-stu-id="35f0b-121">Performing Approver Tasks</span></span>](performing-approver-tasks-agpm30ops.md)

-   [<span data-ttu-id="35f0b-122">Offline-Bearbeitung eines Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="35f0b-122">Edit a GPO Offline</span></span>](edit-a-gpo-offline-agpm30ops.md)

 

 





