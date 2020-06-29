---
title: Anfordern der Erstellung eines neuen gesteuerten Gruppenrichtlinienobjekts
description: Anfordern der Erstellung eines neuen gesteuerten Gruppenrichtlinienobjekts
author: dansimp
ms.assetid: cb265238-386f-4780-a59a-0c9a4a87d736
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 85a435f84e055013c5100a720377f4bffaef4319
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808259"
---
# <span data-ttu-id="29c43-103">Anfordern der Erstellung eines neuen gesteuerten Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="29c43-103">Request the Creation of a New Controlled GPO</span></span>


<span data-ttu-id="29c43-104">Sofern Sie kein Genehmiger oder ein AGPM-Administrator (Vollzugriff) sind, müssen Sie die Erstellung eines neuen Gruppenrichtlinienobjekts (GPO) anfordern.</span><span class="sxs-lookup"><span data-stu-id="29c43-104">Unless you are an Approver or an AGPM Administrator (Full Control), you must request the creation of a new Group Policy Object (GPO).</span></span>

<span data-ttu-id="29c43-105">Um dieses Verfahren ausführen zu können, ist ein Benutzerkonto mit der Rolle "Bearbeiter" oder "Prüfer" oder die erforderlichen Berechtigungen in Advanced Group Policy Management (AGPM) erforderlich.</span><span class="sxs-lookup"><span data-stu-id="29c43-105">A user account with the Editor or Reviewer role or necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span> <span data-ttu-id="29c43-106">Lesen Sie die Details unter "Weitere Überlegungen" in diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="29c43-106">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="29c43-107">So erstellen Sie ein neues Gruppenrichtlinienobjekt mit über AGPM verwaltetem Änderungs Steuerelement</span><span class="sxs-lookup"><span data-stu-id="29c43-107">To create a new GPO with change control managed through AGPM</span></span>**

1.  <span data-ttu-id="29c43-108">Klicken Sie in der Struktur der **Gruppenrichtlinien-Verwaltungskonsole** in der Gesamtstruktur und Domäne, in der Sie GPOs verwalten möchten, auf **Steuerelement ändern** .</span><span class="sxs-lookup"><span data-stu-id="29c43-108">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="29c43-109">Klicken Sie mit der rechten Maustaste auf **Change Control**, und klicken Sie dann auf **Neues gesteuertes Gruppenrichtlinienobjekt**.</span><span class="sxs-lookup"><span data-stu-id="29c43-109">Right-click **Change Control**, and then click **New Controlled GPO**.</span></span>

3.  <span data-ttu-id="29c43-110">Sofern Sie keine besondere Berechtigung zum Erstellen von GPOs haben, müssen Sie eine Anforderung zur Erstellung einreichen.</span><span class="sxs-lookup"><span data-stu-id="29c43-110">Unless you have special permission to create GPOs, you must submit a request for creation.</span></span> <span data-ttu-id="29c43-111">Im Dialogfeld " **Neues gesteuertes GPO** ":</span><span class="sxs-lookup"><span data-stu-id="29c43-111">In the **New Controlled GPO** dialog box:</span></span>

    1.  <span data-ttu-id="29c43-112">Wenn Sie eine Kopie der Anfrage erhalten möchten, geben Sie Ihre e-Mail-Adresse in das Feld **CC** ein.</span><span class="sxs-lookup"><span data-stu-id="29c43-112">To receive a copy of the request, enter your e-mail address in the **Cc** field.</span></span>

    2.  <span data-ttu-id="29c43-113">Geben Sie einen Namen für das neue Gruppenrichtlinienobjekt ein.</span><span class="sxs-lookup"><span data-stu-id="29c43-113">Type a name for the new GPO.</span></span>

    3.  <span data-ttu-id="29c43-114">Optional: Geben Sie einen Kommentar für das neue Gruppenrichtlinienobjekt ein.</span><span class="sxs-lookup"><span data-stu-id="29c43-114">Optional: Type a comment for the new GPO.</span></span>

    4.  <span data-ttu-id="29c43-115">Wenn Sie das neue Gruppenrichtlinienobjekt unmittelbar nach der Genehmigung in der Produktionsumgebung der Domäne bereitstellen möchten, klicken Sie auf **Live erstellen**.</span><span class="sxs-lookup"><span data-stu-id="29c43-115">To deploy the new GPO to the production environment of the domain immediately upon approval, click **Create live**.</span></span> <span data-ttu-id="29c43-116">Wenn Sie das neue Gruppenrichtlinienobjekt offline erstellen möchten, ohne es sofort nach der Genehmigung bereitzustellen, klicken Sie auf **Offline erstellen**.</span><span class="sxs-lookup"><span data-stu-id="29c43-116">To create the new GPO offline without immediately deploying it upon approval, click **Create offline**.</span></span>

    5.  <span data-ttu-id="29c43-117">Wählen Sie die GPO-Vorlage aus, die als Ausgangspunkt für das neue Gruppenrichtlinienobjekt verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="29c43-117">Select the GPO template to use as a starting point for the new GPO.</span></span>

    6.  <span data-ttu-id="29c43-118">Klicken Sie auf **Übermitteln**.</span><span class="sxs-lookup"><span data-stu-id="29c43-118">Click **Submit**.</span></span>

4.  <span data-ttu-id="29c43-119">Wenn das **Status** Fenster angibt, dass der Gesamtfortschritt abgeschlossen ist, klicken Sie auf **Schließen**.</span><span class="sxs-lookup"><span data-stu-id="29c43-119">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="29c43-120">Das neue Gruppenrichtlinienobjekt wird in der Liste der GPOs auf der Registerkarte **Ausstehend** angezeigt. Wenn eine genehmigende Person Ihre Anfrage genehmigt hat, wird das Gruppenrichtlinienobjekt auf die Registerkarte **gesteuert** verschoben.</span><span class="sxs-lookup"><span data-stu-id="29c43-120">The new GPO is displayed in the list of GPOs on the **Pending** tab. When an Approver has approved your request, the GPO will be moved to the **Controlled** tab.</span></span>

### <span data-ttu-id="29c43-121">Weitere Überlegungen</span><span class="sxs-lookup"><span data-stu-id="29c43-121">Additional considerations</span></span>

-   <span data-ttu-id="29c43-122">Standardmäßig müssen Sie ein Editor oder ein Bearbeiter sein, um dieses Verfahren ausführen zu können.</span><span class="sxs-lookup"><span data-stu-id="29c43-122">By default, you must be an Editor or a Reviewer to perform this procedure.</span></span> <span data-ttu-id="29c43-123">Insbesondere müssen Sie über die Berechtigung **Listeninhalte** für die Domäne verfügen.</span><span class="sxs-lookup"><span data-stu-id="29c43-123">Specifically, you must have **List Contents** permission for the domain.</span></span>

-   <span data-ttu-id="29c43-124">Wenn Sie Ihre Anfrage zurücknehmen möchten, bevor Sie genehmigt wurde, klicken Sie auf die Registerkarte **Ausstehend** . Klicken Sie mit der rechten Maustaste auf das Gruppenrichtlinienobjekt und dann auf **zurück**</span><span class="sxs-lookup"><span data-stu-id="29c43-124">To withdraw your request before it has been approved, click the **Pending** tab. Right-click the GPO, then click **Withdraw**.</span></span> <span data-ttu-id="29c43-125">Das Gruppenrichtlinienobjekt wird gelöscht.</span><span class="sxs-lookup"><span data-stu-id="29c43-125">The GPO will be destroyed.</span></span>

### <span data-ttu-id="29c43-126">Weitere Verweise</span><span class="sxs-lookup"><span data-stu-id="29c43-126">Additional references</span></span>

-   [<span data-ttu-id="29c43-127">Erstellen oder Steuern eines Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="29c43-127">Creating or Controlling a GPO</span></span>](creating-or-controlling-a-gpo-agpm40-ed.md)

 

 





