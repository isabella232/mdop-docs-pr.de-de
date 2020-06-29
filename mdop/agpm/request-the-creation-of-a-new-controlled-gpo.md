---
title: Anfordern der Erstellung eines neuen gesteuerten Gruppenrichtlinienobjekts
description: Anfordern der Erstellung eines neuen gesteuerten Gruppenrichtlinienobjekts
author: dansimp
ms.assetid: e1875d81-8553-42ee-8f3a-023d6ced86ca
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b7994e1af80c0ae32940d52955f7e5f773d1ee6a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808256"
---
# <span data-ttu-id="27fdc-103">Anfordern der Erstellung eines neuen gesteuerten Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="27fdc-103">Request the Creation of a New Controlled GPO</span></span>


<span data-ttu-id="27fdc-104">Sofern Sie kein Genehmiger oder ein AGPM-Administrator (Vollzugriff) sind, müssen Sie die Erstellung eines neuen Gruppenrichtlinienobjekts anfordern, wenn es mithilfe der erweiterten Gruppenrichtlinienverwaltung (Group Policy Management, AGPM) verwaltet werden soll.</span><span class="sxs-lookup"><span data-stu-id="27fdc-104">Unless you are an Approver or an AGPM Administrator (Full Control), you must request the creation of a new Group Policy object (GPO) if it is to be managed using Advanced Group Policy Management (AGPM).</span></span>

<span data-ttu-id="27fdc-105">Zum Ausführen dieses Verfahrens ist ein Benutzerkonto mit der Rolle "Bearbeiter" oder "Prüfer" oder die erforderlichen Berechtigungen in der erweiterten Gruppenrichtlinienverwaltung erforderlich.</span><span class="sxs-lookup"><span data-stu-id="27fdc-105">A user account with the Editor or Reviewer role or necessary permissions in Advanced Group Policy Management is required to complete this procedure.</span></span> <span data-ttu-id="27fdc-106">Lesen Sie die Details unter "Weitere Überlegungen" in diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="27fdc-106">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="27fdc-107">So erstellen Sie ein neues Gruppenrichtlinienobjekt mit über AGPM verwaltetem Änderungs Steuerelement</span><span class="sxs-lookup"><span data-stu-id="27fdc-107">To create a new GPO with change control managed through AGPM</span></span>**

1.  <span data-ttu-id="27fdc-108">Klicken Sie in der Struktur der **Gruppenrichtlinien-Verwaltungskonsole** in der Gesamtstruktur und Domäne, in der Sie GPOs verwalten möchten, auf **Steuerelement ändern** .</span><span class="sxs-lookup"><span data-stu-id="27fdc-108">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="27fdc-109">Klicken Sie mit der rechten Maustaste auf den Knoten **Change Control** , und klicken Sie dann auf **Neues gesteuertes Gruppenrichtlinienobjekt**.</span><span class="sxs-lookup"><span data-stu-id="27fdc-109">Right-click the **Change Control** node, and then click **New Controlled GPO**.</span></span>

3.  <span data-ttu-id="27fdc-110">Sofern Sie keine besondere Berechtigung zum Erstellen von GPOs haben, müssen Sie eine Anforderung zur Erstellung einreichen.</span><span class="sxs-lookup"><span data-stu-id="27fdc-110">Unless you have special permission to create GPOs, you must submit a request for creation.</span></span> <span data-ttu-id="27fdc-111">Im Dialogfeld " **Neues gesteuertes GPO** ":</span><span class="sxs-lookup"><span data-stu-id="27fdc-111">In the **New Controlled GPO** dialog box:</span></span>

    1.  <span data-ttu-id="27fdc-112">Wenn Sie eine Kopie der Anfrage erhalten möchten, geben Sie Ihre e-Mail-Adresse in das Feld **CC** ein.</span><span class="sxs-lookup"><span data-stu-id="27fdc-112">To receive a copy of the request, enter your e-mail address in the **Cc** field.</span></span>

    2.  <span data-ttu-id="27fdc-113">Geben Sie einen Namen für das neue Gruppenrichtlinienobjekt ein.</span><span class="sxs-lookup"><span data-stu-id="27fdc-113">Type a name for the new GPO.</span></span>

    3.  <span data-ttu-id="27fdc-114">Optional: Geben Sie einen Kommentar für das neue Gruppenrichtlinienobjekt ein.</span><span class="sxs-lookup"><span data-stu-id="27fdc-114">Optional: Type a comment for the new GPO.</span></span>

    4.  <span data-ttu-id="27fdc-115">Wenn Sie das neue Gruppenrichtlinienobjekt unmittelbar nach der Genehmigung in der Produktionsumgebung bereitstellen möchten, klicken Sie auf **Live erstellen**.</span><span class="sxs-lookup"><span data-stu-id="27fdc-115">To deploy the new GPO to the production environment immediately upon approval, click **Create live**.</span></span> <span data-ttu-id="27fdc-116">Wenn Sie das neue Gruppenrichtlinienobjekt offline erstellen möchten, ohne es sofort nach der Genehmigung bereitzustellen, klicken Sie auf **Offline erstellen**.</span><span class="sxs-lookup"><span data-stu-id="27fdc-116">To create the new GPO offline without immediately deploying it upon approval, click **Create offline**.</span></span>

    5.  <span data-ttu-id="27fdc-117">Wählen Sie die GPO-Vorlage aus, die als Ausgangspunkt für das neue Gruppenrichtlinienobjekt verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="27fdc-117">Select the GPO template to use as a starting point for the new GPO.</span></span>

    6.  <span data-ttu-id="27fdc-118">Klicken Sie auf **Übermitteln**.</span><span class="sxs-lookup"><span data-stu-id="27fdc-118">Click **Submit**.</span></span>

4.  <span data-ttu-id="27fdc-119">Wenn das **Status** Fenster angibt, dass der Gesamtfortschritt abgeschlossen ist, klicken Sie auf **Schließen**.</span><span class="sxs-lookup"><span data-stu-id="27fdc-119">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="27fdc-120">Das neue Gruppenrichtlinienobjekt wird in der Liste der GPOs auf der Registerkarte **Ausstehend** angezeigt. Wenn eine genehmigende Person Ihre Anfrage genehmigt hat, wird das Gruppenrichtlinienobjekt auf die Registerkarte **gesteuert** verschoben.</span><span class="sxs-lookup"><span data-stu-id="27fdc-120">The new GPO is displayed in the list of GPOs on the **Pending** tab. When an Approver has approved your request, the GPO will be moved to the **Controlled** tab.</span></span>

### <span data-ttu-id="27fdc-121">Weitere Überlegungen</span><span class="sxs-lookup"><span data-stu-id="27fdc-121">Additional considerations</span></span>

-   <span data-ttu-id="27fdc-122">Standardmäßig müssen Sie ein Editor oder ein Bearbeiter sein, um dieses Verfahren ausführen zu können.</span><span class="sxs-lookup"><span data-stu-id="27fdc-122">By default, you must be an Editor or a Reviewer to perform this procedure.</span></span> <span data-ttu-id="27fdc-123">Insbesondere müssen Sie über die Berechtigung **Listeninhalte** für die Domäne verfügen.</span><span class="sxs-lookup"><span data-stu-id="27fdc-123">Specifically, you must have **List Contents** permission for the domain.</span></span>

-   <span data-ttu-id="27fdc-124">Wenn Sie Ihre Anfrage zurücknehmen möchten, bevor Sie genehmigt wurde, klicken Sie auf die Registerkarte **Ausstehend** . Klicken Sie mit der rechten Maustaste auf das Gruppenrichtlinienobjekt und dann auf **zurück**</span><span class="sxs-lookup"><span data-stu-id="27fdc-124">To withdraw your request before it has been approved, click the **Pending** tab. Right-click the GPO, then click **Withdraw**.</span></span> <span data-ttu-id="27fdc-125">Das Gruppenrichtlinienobjekt wird gelöscht.</span><span class="sxs-lookup"><span data-stu-id="27fdc-125">The GPO will be destroyed.</span></span>

### <span data-ttu-id="27fdc-126">Weitere Verweise</span><span class="sxs-lookup"><span data-stu-id="27fdc-126">Additional references</span></span>

-   [<span data-ttu-id="27fdc-127">Erstellen, Steuern oder Importieren eines Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="27fdc-127">Creating, Controlling, or Importing a GPO</span></span>](creating-controlling-or-importing-a-gpo-editor.md)

 

 





