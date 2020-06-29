---
title: Offline-Bearbeitung eines Gruppenrichtlinienobjekts
description: Offline-Bearbeitung eines Gruppenrichtlinienobjekts
author: dansimp
ms.assetid: 4a148952-9fe9-4ec4-8df1-b25e37c97a54
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6753ad21adb810e60e0b284204a61d4dd58c2384
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808487"
---
# <span data-ttu-id="e3202-103">Offline-Bearbeitung eines Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="e3202-103">Edit a GPO Offline</span></span>


<span data-ttu-id="e3202-104">Wenn Sie Änderungen an einem gesteuerten Gruppenrichtlinienobjekt (GPO) vornehmen möchten, müssen Sie zuerst eine Kopie des Gruppenrichtlinienobjekts aus dem Archiv Auschecken.</span><span class="sxs-lookup"><span data-stu-id="e3202-104">To make changes to a controlled Group Policy object (GPO), you must first check out a copy of the GPO from the archive.</span></span> <span data-ttu-id="e3202-105">Niemand sonst kann das Gruppenrichtlinienobjekt so lange ändern, bis es erneut eingecheckt wird, wodurch die Einführung von widersprüchlichen Änderungen durch mehrere Gruppenrichtlinienadministratoren verhindert wird.</span><span class="sxs-lookup"><span data-stu-id="e3202-105">No one else will be able to modify the GPO until it is checked in again, preventing the introduction of conflicting changes by multiple Group Policy administrators.</span></span> <span data-ttu-id="e3202-106">Wenn Sie das Gruppenrichtlinienobjekt geändert haben, überprüfen Sie es in das Archiv, damit es überprüft und in der Produktionsumgebung bereitgestellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="e3202-106">When you have finished modifying the GPO, you check it into the archive, so it can be reviewed and deployed to the production environment.</span></span>

<span data-ttu-id="e3202-107">Ein Benutzerkonto mit der Rolle "Editor" oder "AGPM-Administrator (Vollzugriff)", das Benutzerkonto der genehmigenden Person, die das Gruppenrichtlinienobjekt erstellt hat, oder ein Benutzerkonto mit den erforderlichen Berechtigungen in der erweiterten Gruppenrichtlinienverwaltung ist erforderlich, um dieses Verfahren ausführen zu können.</span><span class="sxs-lookup"><span data-stu-id="e3202-107">A user account with the Editor or AGPM Administrator (Full Control) role, the user account of the Approver who created the GPO, or a user account with the necessary permissions in Advanced Group Policy Management is required to complete this procedure.</span></span> <span data-ttu-id="e3202-108">Lesen Sie die Details unter "Weitere Überlegungen" in diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="e3202-108">Review the details in "Additional considerations" in this topic.</span></span>

## <span data-ttu-id="e3202-109">Offline Bearbeiten eines Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="e3202-109">Editing a GPO offline</span></span>


<span data-ttu-id="e3202-110">Wenn Sie ein GPO bearbeiten möchten, checken Sie das Gruppenrichtlinienobjekt aus dem Archiv aus, bearbeiten das Gruppenrichtlinienobjekt offline, und überprüfen das Gruppenrichtlinienobjekt dann in das Archiv, damit es überprüft und bereitgestellt (oder von anderen Editoren geändert) werden kann.</span><span class="sxs-lookup"><span data-stu-id="e3202-110">To edit a GPO, you check out the GPO from the archive, edit the GPO offline, and then check the GPO into the archive, so it can be reviewed and deployed (or modified by other Editors).</span></span>

-   [<span data-ttu-id="e3202-111">Auschecken eines Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="e3202-111">Check out a GPO</span></span>](#bkmk-checkout)

-   [<span data-ttu-id="e3202-112">Bearbeiten eines Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="e3202-112">Edit a GPO</span></span>](#bkmk-edit)

-   [<span data-ttu-id="e3202-113">Einchecken eines Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="e3202-113">Check in a GPO</span></span>](#bkmk-checkin)

### <a href="" id="bkmk-checkout"></a>

**<span data-ttu-id="e3202-114">So checken Sie ein GPO aus dem Archiv zur Bearbeitung aus</span><span class="sxs-lookup"><span data-stu-id="e3202-114">To check out a GPO from the archive for editing</span></span>**

1.  <span data-ttu-id="e3202-115">Klicken Sie in der Struktur der **Gruppenrichtlinien-Verwaltungskonsole** in der Gesamtstruktur und Domäne, in der Sie GPOs verwalten möchten, auf **Steuerelement ändern** .</span><span class="sxs-lookup"><span data-stu-id="e3202-115">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="e3202-116">Klicken Sie im Detailbereich auf der Registerkarte **Inhalt** auf die Registerkarte **gesteuert** , um die gesteuerten GPOs anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="e3202-116">On the **Contents** tab in the details pane, click the **Controlled** tab to display the controlled GPOs.</span></span>

3.  <span data-ttu-id="e3202-117">Klicken Sie mit der rechten Maustaste auf das zu bearbeitende GPO, und klicken Sie dann auf **Auschecken**.</span><span class="sxs-lookup"><span data-stu-id="e3202-117">Right-click the GPO to be edited, and then click **Check Out**.</span></span>

4.  <span data-ttu-id="e3202-118">Geben Sie einen Kommentar ein, der im Verlauf des Gruppenrichtlinienobjekts angezeigt werden soll, während es ausgecheckt ist, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="e3202-118">Type a comment to be displayed in the History of the GPO while it is checked out, then click **OK**.</span></span>

5.  <span data-ttu-id="e3202-119">Wenn das **Status** Fenster angibt, dass der Gesamtfortschritt abgeschlossen ist, klicken Sie auf **Schließen**.</span><span class="sxs-lookup"><span data-stu-id="e3202-119">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="e3202-120">Auf der Registerkarte **gesteuert** wird der Status des Gruppenrichtlinienobjekts nun als **ausgecheckt**identifiziert.</span><span class="sxs-lookup"><span data-stu-id="e3202-120">On the **Controlled** tab, the state of the GPO is now identified as **Checked Out**.</span></span>

### <a href="" id="bkmk-edit"></a>

**<span data-ttu-id="e3202-121">So bearbeiten Sie ein GPO offline</span><span class="sxs-lookup"><span data-stu-id="e3202-121">To edit a GPO offline</span></span>**

1.  <span data-ttu-id="e3202-122">Klicken Sie auf der Registerkarte **gesteuert** mit der rechten Maustaste auf das Gruppenrichtlinienobjekt, das bearbeitet werden soll, und klicken Sie dann auf **Bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="e3202-122">On the **Controlled** tab, right-click the GPO to be edited, and then click **Edit**.</span></span>

2.  <span data-ttu-id="e3202-123">Nehmen Sie im **Gruppenrichtlinienobjekt-Editor**Änderungen an einer Offlinekopie des Gruppenrichtlinienobjekts vor.</span><span class="sxs-lookup"><span data-stu-id="e3202-123">In the **Group Policy Object Editor**, make changes to an offline copy of the GPO.</span></span>

3.  <span data-ttu-id="e3202-124">Wenn Sie die Änderung des Gruppenrichtlinienobjekts beendet haben, schließen Sie den **Gruppenrichtlinienobjekt-Editor**.</span><span class="sxs-lookup"><span data-stu-id="e3202-124">When you have finished modifying the GPO, close the **Group Policy Object Editor**.</span></span>

### <a href="" id="bkmk-checkin"></a>

**<span data-ttu-id="e3202-125">So überprüfen Sie ein GPO in das Archiv</span><span class="sxs-lookup"><span data-stu-id="e3202-125">To check a GPO into the archive</span></span>**

1.  <span data-ttu-id="e3202-126">Auf der Registerkarte " **gesteuert** ":</span><span class="sxs-lookup"><span data-stu-id="e3202-126">On the **Controlled** tab:</span></span>

    -   <span data-ttu-id="e3202-127">Wenn Sie keine Änderungen am GPO vorgenommen haben, klicken Sie mit der rechten Maustaste auf das Gruppenrichtlinienobjekt, und klicken Sie auf **Auschecken rückgängig machen**, und klicken Sie dann zum bestätigen auf **Ja** .</span><span class="sxs-lookup"><span data-stu-id="e3202-127">If you have made no changes to the GPO, right-click the GPO and click **Undo Check Out**, then click **Yes** to confirm.</span></span>

    -   <span data-ttu-id="e3202-128">Wenn Sie Änderungen am GPO vorgenommen haben, klicken Sie mit der rechten Maustaste auf das Gruppenrichtlinienobjekt, und klicken Sie auf **Einchecken**.</span><span class="sxs-lookup"><span data-stu-id="e3202-128">If you have made changes to the GPO, right-click the GPO and click **Check In**.</span></span>

2.  <span data-ttu-id="e3202-129">Geben Sie einen Kommentar ein, der im Überwachungspfad des Gruppenrichtlinienobjekts angezeigt werden soll, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="e3202-129">Type a comment to be displayed in the audit trail of the GPO, and then click **OK**.</span></span>

3.  <span data-ttu-id="e3202-130">Wenn das **Status** Fenster angibt, dass der Gesamtfortschritt abgeschlossen ist, klicken Sie auf **Schließen**.</span><span class="sxs-lookup"><span data-stu-id="e3202-130">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="e3202-131">Auf der Registerkarte **gesteuert** wird der Status des Gruppenrichtlinienobjekts als **eingecheckt**gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="e3202-131">On the **Controlled** tab, the state of the GPO is identified as **Checked In**.</span></span>

### <span data-ttu-id="e3202-132">Weitere Überlegungen</span><span class="sxs-lookup"><span data-stu-id="e3202-132">Additional considerations</span></span>

-   <span data-ttu-id="e3202-133">Zum Auschecken und Bearbeiten eines Gruppenrichtlinienobjekts müssen Sie standardmäßig die genehmigende Person sein, die das Gruppenrichtlinienobjekt, einen Editor oder einen AGPM-Administrator erstellt oder gesteuert hat (Vollzugriff).</span><span class="sxs-lookup"><span data-stu-id="e3202-133">To check out and edit a GPO, by default, you must be the Approver who created or controlled the GPO, an Editor, or an AGPM Administrator (Full Control).</span></span> <span data-ttu-id="e3202-134">Insbesondere müssen Sie über **Listeninhalte** und Berechtigungen zum **Bearbeiten von Einstellungen** für das Gruppenrichtlinienobjekt verfügen.</span><span class="sxs-lookup"><span data-stu-id="e3202-134">Specifically, you must have **List Contents** and **Edit Settings** permissions for the GPO.</span></span> <span data-ttu-id="e3202-135">Darüber hinaus müssen Sie zum Bearbeiten des Gruppenrichtlinienobjekts die Person sein, die das Gruppenrichtlinienobjekt ausgecheckt hat.</span><span class="sxs-lookup"><span data-stu-id="e3202-135">Additionally, to edit the GPO you must be the individual who has checked out the GPO.</span></span>

-   <span data-ttu-id="e3202-136">Zum Einchecken eines Gruppenrichtlinienobjekts müssen Sie standardmäßig ein Editor, eine genehmigende Person oder ein AGPM-Administrator (Vollzugriff) sein.</span><span class="sxs-lookup"><span data-stu-id="e3202-136">To check in a GPO, by default, you must be an Editor, an Approver, or an AGPM Administrator (Full Control).</span></span> <span data-ttu-id="e3202-137">Insbesondere müssen Sie über **Listeninhalte** und entweder **Einstellungen bearbeiten** oder GPO-Berechtigungen für das Gruppenrichtlinienobjekt **Bereitstellen** .</span><span class="sxs-lookup"><span data-stu-id="e3202-137">Specifically, you must have **List Contents** and either **Edit Settings** or **Deploy GPO** permissions for the GPO.</span></span> <span data-ttu-id="e3202-138">Wenn Sie kein genehmigender oder AGPM-Administrator (oder ein anderer Gruppenrichtlinienadministrator mit der Berechtigung " **GPO bereitstellen** ") sind, müssen Sie der Herausgeber sein, der das Gruppenrichtlinienobjekt ausgecheckt hat.</span><span class="sxs-lookup"><span data-stu-id="e3202-138">If you are not an Approver or AGPM Administrator (or other Group Policy administrator with **Deploy GPO** permission), you must be the Editor who has checked out the GPO.</span></span>

-   <span data-ttu-id="e3202-139">Beim Bearbeiten eines Gruppenrichtlinienobjekts sollten alle Gruppenrichtlinien-Software Installations Upgrades eines Pakets in einem anderen Gruppenrichtlinienobjekt auf das bereitgestellte GPO verweisen, nicht auf die ausgecheckte Kopie.</span><span class="sxs-lookup"><span data-stu-id="e3202-139">When editing a GPO, any Group Policy Software Installation upgrade of a package in another GPO should reference the deployed GPO, not the checked-out copy.</span></span>

### <span data-ttu-id="e3202-140">Weitere Verweise</span><span class="sxs-lookup"><span data-stu-id="e3202-140">Additional references</span></span>

-   [<span data-ttu-id="e3202-141">Bearbeiten eines Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="e3202-141">Editing a GPO</span></span>](editing-a-gpo.md)

-   <span data-ttu-id="e3202-142">Überprüfen eines Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="e3202-142">Reviewing a GPO</span></span>

    -   [<span data-ttu-id="e3202-143">Überprüfen von GPO-Einstellungen</span><span class="sxs-lookup"><span data-stu-id="e3202-143">Review GPO Settings</span></span>](review-gpo-settings.md)

    -   [<span data-ttu-id="e3202-144">Überprüfen von GPO-Links</span><span class="sxs-lookup"><span data-stu-id="e3202-144">Review GPO Links</span></span>](review-gpo-links.md)

    -   [<span data-ttu-id="e3202-145">Ermitteln der Unterschiede zwischen Gruppenrichtlinienobjekten und Versionen oder Vorlagen von Gruppenrichtlinienobjekten</span><span class="sxs-lookup"><span data-stu-id="e3202-145">Identify Differences Between GPOs, GPO Versions, or Templates</span></span>](identify-differences-between-gpos-gpo-versions-or-templates.md)

-   <span data-ttu-id="e3202-146">Bereitstellen eines Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="e3202-146">Deploying a GPO</span></span>

    -   [<span data-ttu-id="e3202-147">Anfordern der Bereitstellung eines Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="e3202-147">Request Deployment of a GPO</span></span>](request-deployment-of-a-gpo.md)

    -   [<span data-ttu-id="e3202-148">Bereitstellen eines Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="e3202-148">Deploy a GPO</span></span>](deploy-a-gpo.md)

 

 





