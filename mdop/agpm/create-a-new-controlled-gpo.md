---
title: Erstellen eines neuen gesteuerten Gruppenrichtlinienobjekts
description: Erstellen eines neuen gesteuerten Gruppenrichtlinienobjekts
author: dansimp
ms.assetid: b43ce0f4-4519-4278-83c4-c7d5163ddd11
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0a64e22036bfe99e1d5012d732e3f2e081acdcca
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808568"
---
# <span data-ttu-id="cc6a5-103">Erstellen eines neuen gesteuerten Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="cc6a5-103">Create a New Controlled GPO</span></span>


<span data-ttu-id="cc6a5-104">Neue Gruppenrichtlinienobjekte (Group Policy Objects, GPOs), die über den Knoten **Change Control** erstellt wurden, werden automatisch gesteuert, sodass Sie mit der erweiterten Gruppenrichtlinienverwaltung (Group Policy Management, AGPM) verwaltet werden können.</span><span class="sxs-lookup"><span data-stu-id="cc6a5-104">New Group Policy objects (GPOs) created through the **Change Control** node will automatically be controlled, enabling you to manage them with Advanced Group Policy Management (AGPM).</span></span>

<span data-ttu-id="cc6a5-105">Zum Ausführen dieses Verfahrens ist ein Benutzerkonto mit der Rolle Genehmiger oder AGPM-Administrator (Vollzugriff) oder den erforderlichen Berechtigungen in der erweiterten Gruppenrichtlinienverwaltung erforderlich.</span><span class="sxs-lookup"><span data-stu-id="cc6a5-105">A user account with the Approver or AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management is required to complete this procedure.</span></span> <span data-ttu-id="cc6a5-106">Lesen Sie die Details unter "Weitere Überlegungen" in diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="cc6a5-106">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="cc6a5-107">So erstellen Sie ein neues Gruppenrichtlinienobjekt mit über AGPM verwaltetem Änderungs Steuerelement</span><span class="sxs-lookup"><span data-stu-id="cc6a5-107">To create a new GPO with change control managed through AGPM</span></span>**

1.  <span data-ttu-id="cc6a5-108">Klicken Sie in der Struktur der **Gruppenrichtlinien-Verwaltungskonsole** in der Gesamtstruktur und Domäne, in der Sie GPOs verwalten möchten, auf **Steuerelement ändern** .</span><span class="sxs-lookup"><span data-stu-id="cc6a5-108">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="cc6a5-109">Klicken Sie mit der rechten Maustaste auf den Knoten **Change Control** , und klicken Sie dann auf **Neues gesteuertes Gruppenrichtlinienobjekt**.</span><span class="sxs-lookup"><span data-stu-id="cc6a5-109">Right-click the **Change Control** node, and then click **New Controlled GPO**.</span></span>

3.  <span data-ttu-id="cc6a5-110">Im Dialogfeld " **Neues gesteuertes GPO** ":</span><span class="sxs-lookup"><span data-stu-id="cc6a5-110">In the **New Controlled GPO** dialog box:</span></span>

    1.  <span data-ttu-id="cc6a5-111">Geben Sie einen Namen für das neue Gruppenrichtlinienobjekt ein.</span><span class="sxs-lookup"><span data-stu-id="cc6a5-111">Type a name for the new GPO.</span></span>

    2.  <span data-ttu-id="cc6a5-112">Optional: Geben Sie einen Kommentar für das neue Gruppenrichtlinienobjekt ein, das im **Protokoll** für das Gruppenrichtlinienobjekt angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="cc6a5-112">Optional: Type a comment for the new GPO to be displayed in the **History** for the GPO.</span></span>

    3.  <span data-ttu-id="cc6a5-113">Wenn Sie das neue Gruppenrichtlinienobjekt sofort in der Produktionsumgebung bereitstellen möchten, klicken Sie auf **Live erstellen**.</span><span class="sxs-lookup"><span data-stu-id="cc6a5-113">To immediately deploy the new GPO to the production environment, click **Create live**.</span></span> <span data-ttu-id="cc6a5-114">Wenn Sie das neue Gruppenrichtlinienobjekt offline erstellen möchten, ohne es sofort bereitzustellen, klicken Sie auf **Offline erstellen**.</span><span class="sxs-lookup"><span data-stu-id="cc6a5-114">To create the new GPO offline without immediately deploying it, click **Create offline**.</span></span>

    4.  <span data-ttu-id="cc6a5-115">Wählen Sie die GPO-Vorlage aus, die als Ausgangspunkt für das neue Gruppenrichtlinienobjekt verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="cc6a5-115">Select the GPO template to use as a starting point for the new GPO.</span></span>

    5.  <span data-ttu-id="cc6a5-116">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="cc6a5-116">Click **OK**.</span></span>

4.  <span data-ttu-id="cc6a5-117">Wenn das **Status** Fenster angibt, dass der Gesamtfortschritt abgeschlossen ist, klicken Sie auf **Schließen**.</span><span class="sxs-lookup"><span data-stu-id="cc6a5-117">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="cc6a5-118">Das neue Gruppenrichtlinienobjekt wird in der Liste der GPOs auf der Registerkarte **gesteuert** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="cc6a5-118">The new GPO is displayed in the list of GPOs on the **Controlled** tab.</span></span>

### <span data-ttu-id="cc6a5-119">Weitere Überlegungen</span><span class="sxs-lookup"><span data-stu-id="cc6a5-119">Additional considerations</span></span>

-   <span data-ttu-id="cc6a5-120">Standardmäßig müssen Sie eine genehmigende Person oder ein AGPM-Administrator (Vollzugriff) sein, um dieses Verfahren ausführen zu können.</span><span class="sxs-lookup"><span data-stu-id="cc6a5-120">By default, you must be an Approver or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="cc6a5-121">Insbesondere müssen Sie über **Listeninhalte** und Berechtigungen zum **Erstellen von Gruppenrichtlinienobjekten** für die Domäne verfügen.</span><span class="sxs-lookup"><span data-stu-id="cc6a5-121">Specifically, you must have **List Contents** and **Create GPO** permissions for the domain.</span></span>

### <span data-ttu-id="cc6a5-122">Weitere Verweise</span><span class="sxs-lookup"><span data-stu-id="cc6a5-122">Additional references</span></span>

-   [<span data-ttu-id="cc6a5-123">Erstellen, Steuern oder Importieren eines Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="cc6a5-123">Creating, Controlling, or Importing a GPO</span></span>](creating-controlling-or-importing-a-gpo-approver.md)

 

 




