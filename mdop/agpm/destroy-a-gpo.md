---
title: Zerstören eines Gruppenrichtlinienobjekts
description: Zerstören eines Gruppenrichtlinienobjekts
author: dansimp
ms.assetid: d74941a3-beef-46cd-a4ca-80a324dcfadf
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5545918c417fce16bfc2369ebc6fc2199390adc6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807591"
---
# <span data-ttu-id="21212-103">Zerstören eines Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="21212-103">Destroy a GPO</span></span>


<span data-ttu-id="21212-104">Mit der erweiterten Gruppenrichtlinienverwaltung (AGPM) können genehmigende Personen ein Gruppenrichtlinienobjekt (Group Policy Object, GPO) vernichten, es aus dem Papierkorb entfernen und es endgültig löschen, damit es nicht mehr wiederhergestellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="21212-104">Advanced Group Policy Management (AGPM) enables Approvers to destroy a Group Policy object (GPO), removing it from the Recycle Bin and permanently deleting it so that it can no longer be restored.</span></span>

<span data-ttu-id="21212-105">Zum Ausführen dieses Verfahrens ist ein Benutzerkonto mit der Rolle Genehmiger oder AGPM-Administrator (Vollzugriff) oder den erforderlichen Berechtigungen in der erweiterten Gruppenrichtlinienverwaltung erforderlich.</span><span class="sxs-lookup"><span data-stu-id="21212-105">A user account with the Approver or AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management is required to complete this procedure.</span></span> <span data-ttu-id="21212-106">Lesen Sie die Details unter "Weitere Überlegungen" in diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="21212-106">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="21212-107">So löschen Sie ein GPO endgültig, damit es nicht mehr wiederhergestellt werden kann</span><span class="sxs-lookup"><span data-stu-id="21212-107">To permanently delete a GPO so it can no longer be restored</span></span>**

1.  <span data-ttu-id="21212-108">Klicken Sie in der Struktur der **Gruppenrichtlinien-Verwaltungskonsole** in der Gesamtstruktur und Domäne, in der Sie GPOs verwalten möchten, auf **Steuerelement ändern** .</span><span class="sxs-lookup"><span data-stu-id="21212-108">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="21212-109">Klicken Sie auf der Registerkarte **Inhalt** auf die Registerkarte **Papierkorb** , um die gelöschten GPOs anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="21212-109">On the **Contents** tab, click the **Recycle Bin** tab to display the deleted GPOs.</span></span>

3.  <span data-ttu-id="21212-110">Klicken Sie mit der rechten Maustaste auf das zu vernichtende GPO, und klicken Sie dann auf **zerstören**.</span><span class="sxs-lookup"><span data-stu-id="21212-110">Right-click the GPO to destroy, and then click **Destroy**.</span></span>

4.  <span data-ttu-id="21212-111">Klicken Sie auf **Ja** , um zu bestätigen, dass Sie das ausgewählte Gruppenrichtlinienobjekt und alle Sicherungen aus dem Archiv endgültig löschen möchten.</span><span class="sxs-lookup"><span data-stu-id="21212-111">Click **Yes** to confirm that you want to permanently delete the selected GPO and all backups from the archive.</span></span>

5.  <span data-ttu-id="21212-112">Wenn das **Status** Fenster angibt, dass der Gesamtfortschritt abgeschlossen ist, klicken Sie auf **Schließen**.</span><span class="sxs-lookup"><span data-stu-id="21212-112">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="21212-113">Das Gruppenrichtlinienobjekt wird von der Registerkarte " **Papierkorb** " entfernt und endgültig gelöscht.</span><span class="sxs-lookup"><span data-stu-id="21212-113">The GPO is removed from the **Recycle Bin** tab and is permanently deleted.</span></span>

### <span data-ttu-id="21212-114">Weitere Überlegungen</span><span class="sxs-lookup"><span data-stu-id="21212-114">Additional considerations</span></span>

-   <span data-ttu-id="21212-115">Standardmäßig müssen Sie eine genehmigende Person oder ein AGPM-Administrator (Vollzugriff) sein, um dieses Verfahren ausführen zu können.</span><span class="sxs-lookup"><span data-stu-id="21212-115">By default, you must be an Approver or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="21212-116">Insbesondere müssen Sie über **Listeninhalte** und Berechtigungen zum **Löschen von Gruppenrichtlinienobjekten** für das Gruppenrichtlinienobjekt verfügen.</span><span class="sxs-lookup"><span data-stu-id="21212-116">Specifically, you must have **List Contents** and **Delete GPO** permissions for the GPO.</span></span>

### <span data-ttu-id="21212-117">Weitere Verweise</span><span class="sxs-lookup"><span data-stu-id="21212-117">Additional references</span></span>

-   [<span data-ttu-id="21212-118">Löschen, Wiederherstellen oder Zerstören eines Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="21212-118">Deleting, Restoring, or Destroying a GPO</span></span>](deleting-restoring-or-destroying-a-gpo.md)

 

 





