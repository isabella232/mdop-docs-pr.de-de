---
title: Zurücksetzen auf eine frühere Version eines Gruppenrichtlinienobjekts
description: Zurücksetzen auf eine frühere Version eines Gruppenrichtlinienobjekts
author: dansimp
ms.assetid: 028631c0-4cb9-4642-90ad-04cd813051b7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a71740eaa60a4b1292e47ca8aa57d4657231ab57
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808244"
---
# <span data-ttu-id="1eebe-103">Zurücksetzen auf eine frühere Version eines Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="1eebe-103">Roll Back to a Previous Version of a GPO</span></span>


<span data-ttu-id="1eebe-104">Mit der erweiterten Gruppenrichtlinienverwaltung (AGPM) kann eine genehmigende Person Änderungen an einem Gruppenrichtlinienobjekt zurücksetzen, indem Sie eine frühere Version des GPO aus ihrem Verlauf erneut bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="1eebe-104">Advanced Group Policy Management (AGPM) enables an Approver to roll back changes to a Group Policy object (GPO) by redeploying an earlier version of the GPO from its history.</span></span> <span data-ttu-id="1eebe-105">Durch das Bereitstelleneiner früheren Version eines GPO wird die Version des Gruppenrichtlinienobjekts überschrieben, das sich derzeit in der Produktion befindet.</span><span class="sxs-lookup"><span data-stu-id="1eebe-105">Deploying an earlier version of a GPO overwrites the version of the GPO currently in production.</span></span>

<span data-ttu-id="1eebe-106">Zum Ausführen dieses Verfahrens ist ein Benutzerkonto mit der Rolle Genehmiger oder AGPM-Administrator (Vollzugriff) oder den erforderlichen Berechtigungen in der erweiterten Gruppenrichtlinienverwaltung erforderlich.</span><span class="sxs-lookup"><span data-stu-id="1eebe-106">A user account with the Approver or AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management is required to complete this procedure.</span></span> <span data-ttu-id="1eebe-107">Lesen Sie die Details unter "Weitere Überlegungen" in diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="1eebe-107">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="1eebe-108">So stellen Sie eine frühere Version eines GPO in der Produktionsumgebung bereit</span><span class="sxs-lookup"><span data-stu-id="1eebe-108">To deploy a previous version of a GPO to the production environment</span></span>**

1.  <span data-ttu-id="1eebe-109">Klicken Sie in der Struktur der **Gruppenrichtlinien-Verwaltungskonsole** in der Gesamtstruktur und Domäne, in der Sie GPOs verwalten möchten, auf **Steuerelement ändern** .</span><span class="sxs-lookup"><span data-stu-id="1eebe-109">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="1eebe-110">Klicken Sie auf der Registerkarte **Inhalt** auf die Registerkarte **gesteuert** , um die gesteuerten GPOs anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="1eebe-110">On the **Contents** tab, click the **Controlled** tab to display the controlled GPOs.</span></span>

3.  <span data-ttu-id="1eebe-111">Doppelklicken Sie auf das Gruppenrichtlinienobjekt, das bereitgestellt werden soll, um dessen **Verlauf**anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="1eebe-111">Double-click the GPO to be deployed to display its **History**.</span></span>

4.  <span data-ttu-id="1eebe-112">Klicken Sie mit der rechten Maustaste auf die bereit **zustellende**Version, klicken Sie auf bereitstellen, und klicken Sie dann auf **Ja**.</span><span class="sxs-lookup"><span data-stu-id="1eebe-112">Right-click the version to be deployed, click **Deploy**, and then click **Yes**.</span></span>

5.  <span data-ttu-id="1eebe-113">Wenn das **Status** Fenster angibt, dass der Gesamtfortschritt abgeschlossen ist, klicken Sie auf **Schließen**.</span><span class="sxs-lookup"><span data-stu-id="1eebe-113">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="1eebe-114">Klicken Sie im Fenster **Verlauf** auf **Schließen**.</span><span class="sxs-lookup"><span data-stu-id="1eebe-114">In the **History** window, click **Close**.</span></span>

<span data-ttu-id="1eebe-115">**Hinweis**  Um zu überprüfen, ob die Version, die erneut bereitgestellt wurde, mit der beabsichtigten Version übereinstimmt, untersuchen Sie einen Unterschiedsbericht für die beiden Versionen.</span><span class="sxs-lookup"><span data-stu-id="1eebe-115">**Note** To verify that the version that has been redeployed matches the version intended, examine a difference report for the two versions.</span></span> <span data-ttu-id="1eebe-116">Markieren Sie im **Verlaufs** Fenster für das Gruppenrichtlinienobjekt die beiden Versionen, und klicken Sie dann mit der rechten Maustaste, und wählen Sie **Differenz** und entweder **HTML-Bericht** oder **XML-Bericht**aus.</span><span class="sxs-lookup"><span data-stu-id="1eebe-116">In the **History** window for the GPO, highlight the two versions, and then right-click and select **Difference** and either **HTML Report** or **XML Report**.</span></span>

 

### <span data-ttu-id="1eebe-117">Weitere Überlegungen</span><span class="sxs-lookup"><span data-stu-id="1eebe-117">Additional considerations</span></span>

-   <span data-ttu-id="1eebe-118">Standardmäßig müssen Sie eine genehmigende Person oder ein AGPM-Administrator (Vollzugriff) sein, um dieses Verfahren ausführen zu können.</span><span class="sxs-lookup"><span data-stu-id="1eebe-118">By default, you must be an Approver or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="1eebe-119">Insbesondere müssen Sie über **Listeninhalte** und Berechtigungen zum **Bereitstellen von Gruppenrichtlinienobjekten** für das Gruppenrichtlinienobjekt verfügen.</span><span class="sxs-lookup"><span data-stu-id="1eebe-119">Specifically, you must have **List Contents** and **Deploy GPO** permissions for the GPO.</span></span>

### <span data-ttu-id="1eebe-120">Weitere Verweise</span><span class="sxs-lookup"><span data-stu-id="1eebe-120">Additional references</span></span>

-   [<span data-ttu-id="1eebe-121">Durchführen der Aufgaben von genehmigenden Personen</span><span class="sxs-lookup"><span data-stu-id="1eebe-121">Performing Approver Tasks</span></span>](performing-approver-tasks.md)

 

 





