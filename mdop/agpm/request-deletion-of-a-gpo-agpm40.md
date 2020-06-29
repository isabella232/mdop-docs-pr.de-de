---
title: Anfordern der Löschung eines Gruppenrichtlinienobjekts
description: Anfordern der Löschung eines Gruppenrichtlinienobjekts
author: dansimp
ms.assetid: 2410f7a1-ccca-44cf-ab26-76ad474409e7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: cfdb50fba872b76c82152b469f787f2e1a6fb539
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807503"
---
# <span data-ttu-id="5c526-103">Anfordern der Löschung eines Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="5c526-103">Request Deletion of a GPO</span></span>


<span data-ttu-id="5c526-104">Sofern Sie kein Genehmiger oder ein AGPM-Administrator (Vollzugriff) sind, müssen Sie den Löschvorgang für ein Gruppenrichtlinienobjekt (GPO) anfordern.</span><span class="sxs-lookup"><span data-stu-id="5c526-104">Unless you are an Approver or an AGPM Administrator (Full Control), you must request the deletion of a Group Policy Object (GPO).</span></span>

<span data-ttu-id="5c526-105">Um dieses Verfahren ausführen zu können, ist ein Benutzerkonto mit der Rolle "Editor" oder den erforderlichen Berechtigungen in Advanced Group Policy Management (AGPM) erforderlich.</span><span class="sxs-lookup"><span data-stu-id="5c526-105">A user account with the Editor role or necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span> <span data-ttu-id="5c526-106">Lesen Sie die Details unter "Weitere Überlegungen" in diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="5c526-106">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="5c526-107">So fordern Sie das Löschen eines kontrollierten Gruppenrichtlinienobjekts an</span><span class="sxs-lookup"><span data-stu-id="5c526-107">To request the deletion of a controlled GPO</span></span>**

1.  <span data-ttu-id="5c526-108">Klicken Sie in der Struktur der **Gruppenrichtlinien-Verwaltungskonsole** in der Gesamtstruktur und Domäne, in der Sie GPOs verwalten möchten, auf **Steuerelement ändern** .</span><span class="sxs-lookup"><span data-stu-id="5c526-108">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="5c526-109">Klicken Sie auf der Registerkarte **Inhalt** auf die Registerkarte **gesteuert** , um die gesteuerten GPOs anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="5c526-109">On the **Contents** tab, click the **Controlled** tab to display the controlled GPOs.</span></span>

3.  <span data-ttu-id="5c526-110">Klicken Sie mit der rechten Maustaste auf das Gruppenrichtlinienobjekt, das Sie löschen möchten, und klicken Sie dann auf **Löschen**.</span><span class="sxs-lookup"><span data-stu-id="5c526-110">Right-click the GPO you want to delete, and then click **Delete**.</span></span>

    -   <span data-ttu-id="5c526-111">Wenn Sie das Gruppenrichtlinienobjekt aus dem Archiv löschen möchten, während die bereitgestellte Version des Gruppenrichtlinienobjekts in der Produktionsumgebung unangetastet bleibt, klicken Sie auf **GPO nur aus Archiv löschen**.</span><span class="sxs-lookup"><span data-stu-id="5c526-111">To delete the GPO from the archive while leaving the deployed version of the GPO untouched in the production environment, click **Delete GPO from archive only**.</span></span>

    -   <span data-ttu-id="5c526-112">Wenn Sie das Gruppenrichtlinienobjekt aus der Archivierungs-und Produktionsumgebung der Domäne löschen möchten, klicken Sie auf **Gruppenrichtlinienobjekt aus Archiv und Produktion löschen**.</span><span class="sxs-lookup"><span data-stu-id="5c526-112">To delete the GPO from both the archive and production environment of the domain, click **Delete GPO from archive and production**.</span></span>

4.  <span data-ttu-id="5c526-113">Sofern Sie keine besondere Berechtigung zum Löschen von GPOs haben, müssen Sie eine Anforderung zum Löschen des bereitgestellten Gruppenrichtlinienobjekts übermitteln.</span><span class="sxs-lookup"><span data-stu-id="5c526-113">Unless you have special permission to delete GPOs, you must submit a request for deletion of the deployed GPO.</span></span> <span data-ttu-id="5c526-114">Wenn Sie eine Kopie der Anfrage erhalten möchten, geben Sie Ihre e-Mail-Adresse in das Feld **CC** ein.</span><span class="sxs-lookup"><span data-stu-id="5c526-114">To receive a copy of the request, type your e-mail address in the **Cc** field.</span></span> <span data-ttu-id="5c526-115">Geben Sie einen Kommentar ein, der im Überwachungspfad für das Gruppenrichtlinienobjekt angezeigt werden soll, und klicken Sie dann auf **Absenden**.</span><span class="sxs-lookup"><span data-stu-id="5c526-115">Type a comment to be displayed in the audit trail for the GPO, and then click **Submit**.</span></span>

5.  <span data-ttu-id="5c526-116">Wenn das **Status** Fenster angibt, dass der Gesamtfortschritt abgeschlossen ist, klicken Sie auf **Schließen**.</span><span class="sxs-lookup"><span data-stu-id="5c526-116">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="5c526-117">Das Gruppenrichtlinienobjekt wird in der Liste der GPOs auf der Registerkarte **Ausstehend** angezeigt. Wenn eine genehmigende Person Ihre Anfrage genehmigt hat, wird das Gruppenrichtlinienobjekt von der Registerkarte " **Ausstehend** " auf die Registerkarte " **Papierkorb** " verschoben, wo Sie wiederhergestellt oder gelöscht werden kann.</span><span class="sxs-lookup"><span data-stu-id="5c526-117">The GPO is displayed on the list of GPOs on the **Pending** tab. When an Approver has approved your request, the GPO will be moved from the **Pending** tab to the **Recycle Bin** tab, where it can be restored or destroyed.</span></span>

### <span data-ttu-id="5c526-118">Weitere Überlegungen</span><span class="sxs-lookup"><span data-stu-id="5c526-118">Additional considerations</span></span>

-   <span data-ttu-id="5c526-119">Standardmäßig müssen Sie ein Editor sein, um dieses Verfahren ausführen zu können.</span><span class="sxs-lookup"><span data-stu-id="5c526-119">By default, you must be an Editor to perform this procedure.</span></span> <span data-ttu-id="5c526-120">Insbesondere müssen Sie über **Listeninhalte** und Berechtigungen zum **Bearbeiten von Einstellungen** für das Gruppenrichtlinienobjekt verfügen.</span><span class="sxs-lookup"><span data-stu-id="5c526-120">Specifically, you must have **List Contents** and **Edit Settings** permissions for the GPO.</span></span>

-   <span data-ttu-id="5c526-121">Wenn Sie Ihre Anfrage zurücknehmen möchten, bevor Sie genehmigt wurde, klicken Sie auf die Registerkarte **Ausstehend** . Klicken Sie mit der rechten Maustaste auf das GPO, und klicken Sie dann auf **zurück**</span><span class="sxs-lookup"><span data-stu-id="5c526-121">To withdraw your request before it has been approved, click the **Pending** tab. Right-click the GPO, and then click **Withdraw**.</span></span> <span data-ttu-id="5c526-122">Das Gruppenrichtlinienobjekt wird auf die Registerkarte **gesteuert** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="5c526-122">The GPO will be returned to the **Controlled** tab.</span></span>

-   <span data-ttu-id="5c526-123">Klicken Sie in der **Gruppenrichtlinien-Verwaltungskonsole**auf **Gesamtstruktur**, klicken Sie auf **Domänen**, klicken Sie auf meine \*\* &lt; &gt; Domäne\*\*, und klicken Sie dann auf **Gruppenrichtlinienobjekte**, um ein ungesteuertes Gruppenrichtlinienobjekt aus der Produktionsumgebung zu löschen, ohne es zuvor zu kontrollieren.</span><span class="sxs-lookup"><span data-stu-id="5c526-123">To delete an uncontrolled GPO from the production environment without first controlling it, in the **Group Policy Management Console**, click **Forest**, click **Domains**, click **&lt;MyDomain&gt;**, and then click **Group Policy Objects**.</span></span> <span data-ttu-id="5c526-124">Klicken Sie mit der rechten Maustaste auf das unkontrollierte Gruppenrichtlinienobjekt, und klicken Sie dann auf **Löschen**.</span><span class="sxs-lookup"><span data-stu-id="5c526-124">Right-click the uncontrolled GPO, and then click **Delete**.</span></span>

### <span data-ttu-id="5c526-125">Weitere Verweise</span><span class="sxs-lookup"><span data-stu-id="5c526-125">Additional references</span></span>

-   [<span data-ttu-id="5c526-126">Löschen oder Wiederherstellen eines Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="5c526-126">Deleting or Restoring a GPO</span></span>](deleting-or-restoring-a-gpo-agpm40.md)

 

 





