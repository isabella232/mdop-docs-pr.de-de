---
title: Löschen eines Gruppenrichtlinienobjekts
description: Löschen eines Gruppenrichtlinienobjekts
author: dansimp
ms.assetid: 85fca371-5707-49c1-aa51-813fc3a58dfc
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8a6419943604ee5a76d305228bb7418a8525bf33
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808524"
---
# <span data-ttu-id="390c1-103">Löschen eines Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="390c1-103">Delete a GPO</span></span>


<span data-ttu-id="390c1-104">Erweiterte Gruppenrichtlinienverwaltung (AGPM) ermöglicht Genehmigern, ein gesteuertes Gruppenrichtlinienobjekt (Group Policy Object, GPO) zu löschen und in den Papierkorb zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="390c1-104">Advanced Group Policy Management (AGPM) enables Approvers to delete a controlled Group Policy object (GPO), moving it to the Recycle Bin.</span></span>

<span data-ttu-id="390c1-105">Zum Ausführen dieses Verfahrens ist ein Benutzerkonto mit der Rolle Genehmiger oder AGPM-Administrator (Vollzugriff) oder den erforderlichen Berechtigungen in der erweiterten Gruppenrichtlinienverwaltung erforderlich.</span><span class="sxs-lookup"><span data-stu-id="390c1-105">A user account with the Approver or AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management is required to complete this procedure.</span></span> <span data-ttu-id="390c1-106">Lesen Sie die Details unter "Weitere Überlegungen" in diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="390c1-106">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="390c1-107">So löschen Sie ein gesteuertes Gruppenrichtlinienobjekt</span><span class="sxs-lookup"><span data-stu-id="390c1-107">To delete a controlled GPO</span></span>**

1.  <span data-ttu-id="390c1-108">Klicken Sie in der Struktur der **Gruppenrichtlinien-Verwaltungskonsole** in der Gesamtstruktur und Domäne, in der Sie GPOs verwalten möchten, auf **Steuerelement ändern** .</span><span class="sxs-lookup"><span data-stu-id="390c1-108">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="390c1-109">Klicken Sie auf der Registerkarte **Inhalt** auf die Registerkarte **gesteuert** , um die gesteuerten GPOs anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="390c1-109">On the **Contents** tab, click the **Controlled** tab to display the controlled GPOs.</span></span>

3.  <span data-ttu-id="390c1-110">Klicken Sie mit der rechten Maustaste auf das zu löschende GPO, und klicken Sie dann auf **Löschen**.</span><span class="sxs-lookup"><span data-stu-id="390c1-110">Right-click the GPO to delete, and then click **Delete**.</span></span>

    -   <span data-ttu-id="390c1-111">Wenn Sie das Gruppenrichtlinienobjekt aus dem Archiv löschen möchten, während die bereitgestellte Version des Gruppenrichtlinienobjekts in der Produktionsumgebung unangetastet bleibt, klicken Sie auf **GPO nur aus Archiv löschen (uncontrol)**.</span><span class="sxs-lookup"><span data-stu-id="390c1-111">To delete the GPO from the archive while leaving the deployed version of the GPO untouched in the production environment, click **Delete GPO from archive only (uncontrol)**.</span></span>

    -   <span data-ttu-id="390c1-112">Wenn Sie das Gruppenrichtlinienobjekt aus der Archivierungs-und Produktionsumgebung löschen möchten, klicken Sie auf **Gruppenrichtlinienobjekt aus Archiv und Produktion löschen**.</span><span class="sxs-lookup"><span data-stu-id="390c1-112">To delete the GPO from both the archive and production environment, click **Delete GPO from archive and production**.</span></span>

4.  <span data-ttu-id="390c1-113">Geben Sie einen Kommentar ein, der im Überwachungspfad für das Gruppenrichtlinienobjekt angezeigt werden soll, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="390c1-113">Type a comment to be displayed in the audit trail for the GPO, and then click **OK**.</span></span>

5.  <span data-ttu-id="390c1-114">Wenn das **Status** Fenster angibt, dass der Gesamtfortschritt abgeschlossen ist, klicken Sie auf **Schließen**.</span><span class="sxs-lookup"><span data-stu-id="390c1-114">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="390c1-115">Das Gruppenrichtlinienobjekt wird von der Registerkarte " **gesteuert** " entfernt und auf der Registerkarte " **Papierkorb** " angezeigt, wo es wiederhergestellt oder gelöscht werden kann.</span><span class="sxs-lookup"><span data-stu-id="390c1-115">The GPO is removed from the **Controlled** tab and is displayed on the **Recycle Bin** tab, where it can be restored or destroyed.</span></span> <span data-ttu-id="390c1-116">Wenn das Gruppenrichtlinienobjekt nur aus dem Archiv gelöscht wurde, wird es auch auf der Registerkarte nicht **gesteuert** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="390c1-116">If the GPO was deleted only from the archive, it is also displayed on the **Uncontrolled** tab.</span></span>

### <span data-ttu-id="390c1-117">Weitere Überlegungen</span><span class="sxs-lookup"><span data-stu-id="390c1-117">Additional considerations</span></span>

-   <span data-ttu-id="390c1-118">Standardmäßig müssen Sie eine genehmigende Person oder ein AGPM-Administrator (Vollzugriff) sein, um ein bereitgestelltes GPO zu löschen.</span><span class="sxs-lookup"><span data-stu-id="390c1-118">By default, you must be an Approver or an AGPM Administrator (Full Control) to delete a deployed GPO.</span></span> <span data-ttu-id="390c1-119">Insbesondere müssen Sie über **Listeninhalte** und Berechtigungen zum **Löschen von Gruppenrichtlinienobjekten** für das Gruppenrichtlinienobjekt verfügen.</span><span class="sxs-lookup"><span data-stu-id="390c1-119">Specifically, you must have **List Contents** and **Delete GPO** permissions for the GPO.</span></span>

-   <span data-ttu-id="390c1-120">Standardmäßig müssen Sie ein Editor, eine genehmigende Person oder ein AGPM-Administrator (Vollzugriff) sein, um ein GPO aus dem Archiv zu löschen.</span><span class="sxs-lookup"><span data-stu-id="390c1-120">By default, you must be an Editor, an Approver, or an AGPM Administrator (Full Control) to delete a GPO from the archive.</span></span> <span data-ttu-id="390c1-121">Insbesondere müssen Sie über **Listeninhalte** und entweder die Berechtigung " **Einstellungen bearbeiten** " oder " **GPO löschen** " für das Gruppenrichtlinienobjekt verfügen.</span><span class="sxs-lookup"><span data-stu-id="390c1-121">Specifically, you must have **List Contents** and either **Edit Settings** or **Delete GPO** permissions for the GPO.</span></span>

-   <span data-ttu-id="390c1-122">Klicken Sie in der **Gruppenrichtlinien-Verwaltungskonsole**auf **Gesamtstruktur**, klicken Sie auf **Domänen**, klicken Sie auf meine \*\* &lt; &gt; Domäne\*\*, und klicken Sie dann auf **Gruppenrichtlinienobjekte**, um ein ungesteuertes Gruppenrichtlinienobjekt aus der Produktionsumgebung zu löschen, ohne es zuvor zu kontrollieren.</span><span class="sxs-lookup"><span data-stu-id="390c1-122">To delete an uncontrolled GPO from the production environment without first controlling it, in the **Group Policy Management Console**, click **Forest**, click **Domains**, click **&lt;MyDomain&gt;**, and then click **Group Policy Objects**.</span></span> <span data-ttu-id="390c1-123">Klicken Sie mit der rechten Maustaste auf das unkontrollierte Gruppenrichtlinienobjekt, und klicken Sie dann auf **Löschen**.</span><span class="sxs-lookup"><span data-stu-id="390c1-123">Right-click the uncontrolled GPO, and then click **Delete**.</span></span>

### <span data-ttu-id="390c1-124">Weitere Verweise</span><span class="sxs-lookup"><span data-stu-id="390c1-124">Additional references</span></span>

-   [<span data-ttu-id="390c1-125">Löschen, Wiederherstellen oder Zerstören eines Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="390c1-125">Deleting, Restoring, or Destroying a GPO</span></span>](deleting-restoring-or-destroying-a-gpo.md)

 

 





