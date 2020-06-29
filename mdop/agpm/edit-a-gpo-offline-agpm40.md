---
title: Offline-Bearbeitung eines Gruppenrichtlinienobjekts
description: Offline-Bearbeitung eines Gruppenrichtlinienobjekts
author: dansimp
ms.assetid: 9c75eb3c-d4d5-41e0-b65e-8b4464a42cd9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d7ba0f72d7bfa8e2c597f62f7675a754807525ac
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808488"
---
# <span data-ttu-id="fa7f5-103">Offline-Bearbeitung eines Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="fa7f5-103">Edit a GPO Offline</span></span>


<span data-ttu-id="fa7f5-104">Wenn Sie Änderungen an einem gesteuerten Gruppenrichtlinienobjekt (GPO) vornehmen möchten, müssen Sie zuerst eine Kopie des Gruppenrichtlinienobjekts aus dem Archiv Auschecken.</span><span class="sxs-lookup"><span data-stu-id="fa7f5-104">To make changes to a controlled Group Policy Object (GPO), you must first check out a copy of the GPO from the archive.</span></span> <span data-ttu-id="fa7f5-105">Niemand sonst kann das Gruppenrichtlinienobjekt so lange ändern, bis es erneut eingecheckt wird, wodurch die Einführung von widersprüchlichen Änderungen durch mehrere Gruppenrichtlinienadministratoren verhindert wird.</span><span class="sxs-lookup"><span data-stu-id="fa7f5-105">No one else will be able to modify the GPO until it is checked in again, preventing the introduction of conflicting changes by multiple Group Policy administrators.</span></span> <span data-ttu-id="fa7f5-106">Wenn Sie das Gruppenrichtlinienobjekt geändert haben, überprüfen Sie es in das Archiv, damit es überprüft und in der Produktionsumgebung bereitgestellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="fa7f5-106">When you have finished modifying the GPO, you check it into the archive so that it can be reviewed and deployed to the production environment.</span></span>

<span data-ttu-id="fa7f5-107">Ein Benutzerkonto mit der Rolle "Editor" oder "AGPM-Administrator (Vollzugriff)", das Benutzerkonto der genehmigenden Person, die das Gruppenrichtlinienobjekt erstellt hat, oder ein Benutzerkonto mit den erforderlichen Berechtigungen in Advanced Group Policy Management (AGPM) ist erforderlich, um dieses Verfahren ausführen zu können.</span><span class="sxs-lookup"><span data-stu-id="fa7f5-107">A user account with the Editor or AGPM Administrator (Full Control) role, the user account of the Approver who created the GPO, or a user account with the necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span> <span data-ttu-id="fa7f5-108">Lesen Sie die Details unter "Weitere Überlegungen" in diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="fa7f5-108">Review the details in "Additional considerations" in this topic.</span></span>

## <span data-ttu-id="fa7f5-109">Offline Bearbeiten eines Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="fa7f5-109">Editing a GPO offline</span></span>


<span data-ttu-id="fa7f5-110">Zum Bearbeiten eines Gruppenrichtlinienobjekts checken Sie das Gruppenrichtlinienobjekt aus dem Archiv aus, bearbeiten das Gruppenrichtlinienobjekt offline, und überprüfen das Gruppenrichtlinienobjekt dann in das Archiv, damit es überprüft und bereitgestellt (oder von anderen Editoren geändert) werden kann.</span><span class="sxs-lookup"><span data-stu-id="fa7f5-110">To edit a GPO, you check out the GPO from the archive, edit the GPO offline, and then check the GPO into the archive so that it can be reviewed and deployed (or modified by other Editors).</span></span>

-   [<span data-ttu-id="fa7f5-111">Auschecken eines GPO aus dem Archiv zur Bearbeitung</span><span class="sxs-lookup"><span data-stu-id="fa7f5-111">Check out a GPO from the archive for editing</span></span>](#bkmk-checkout)

-   [<span data-ttu-id="fa7f5-112">Offline Bearbeiten eines Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="fa7f5-112">Edit a GPO offline</span></span>](#bkmk-edit)

-   [<span data-ttu-id="fa7f5-113">Überprüfen eines Gruppenrichtlinienobjekts in das Archiv</span><span class="sxs-lookup"><span data-stu-id="fa7f5-113">Check a GPO into the archive</span></span>](#bkmk-checkin)

### <a href="" id="bkmk-checkout"></a>

**<span data-ttu-id="fa7f5-114">So checken Sie ein GPO aus dem Archiv zur Bearbeitung aus</span><span class="sxs-lookup"><span data-stu-id="fa7f5-114">To check out a GPO from the archive for editing</span></span>**

1.  <span data-ttu-id="fa7f5-115">Klicken Sie in der Struktur der **Gruppenrichtlinien-Verwaltungskonsole** in der Gesamtstruktur und Domäne, in der Sie GPOs verwalten möchten, auf **Steuerelement ändern** .</span><span class="sxs-lookup"><span data-stu-id="fa7f5-115">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="fa7f5-116">Klicken Sie auf der Registerkarte **Inhalt** auf die Registerkarte **gesteuert** , um die gesteuerten GPOs anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="fa7f5-116">On the **Contents** tab, click the **Controlled** tab to display the controlled GPOs.</span></span>

3.  <span data-ttu-id="fa7f5-117">Klicken Sie mit der rechten Maustaste auf das zu bearbeitende GPO, und klicken Sie dann auf **Auschecken**.</span><span class="sxs-lookup"><span data-stu-id="fa7f5-117">Right-click the GPO to be edited, and then click **Check Out**.</span></span>

4.  <span data-ttu-id="fa7f5-118">Geben Sie einen Kommentar ein, der im Verlauf des Gruppenrichtlinienobjekts angezeigt werden soll, während es ausgecheckt ist, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="fa7f5-118">Type a comment to be displayed in the History of the GPO while it is checked out, and then click **OK**.</span></span>

5.  <span data-ttu-id="fa7f5-119">Wenn das **Status** Fenster angibt, dass der Gesamtfortschritt abgeschlossen ist, klicken Sie auf **Schließen**.</span><span class="sxs-lookup"><span data-stu-id="fa7f5-119">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="fa7f5-120">Auf der Registerkarte **gesteuert** wird der Status des Gruppenrichtlinienobjekts nun als **ausgecheckt**identifiziert.</span><span class="sxs-lookup"><span data-stu-id="fa7f5-120">On the **Controlled** tab, the state of the GPO is now identified as **Checked Out**.</span></span>

### <a href="" id="bkmk-edit"></a>

**<span data-ttu-id="fa7f5-121">So bearbeiten Sie ein GPO offline</span><span class="sxs-lookup"><span data-stu-id="fa7f5-121">To edit a GPO offline</span></span>**

1.  <span data-ttu-id="fa7f5-122">Klicken Sie auf der Registerkarte **gesteuert** mit der rechten Maustaste auf das Gruppenrichtlinienobjekt, das bearbeitet werden soll, und klicken Sie dann auf **Bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="fa7f5-122">On the **Controlled** tab, right-click the GPO to be edited, and then click **Edit**.</span></span>

2.  <span data-ttu-id="fa7f5-123">Nehmen Sie im Fenster **Gruppenrichtlinien-Verwaltungs-Editor** Änderungen an einer Offlinekopie des Gruppenrichtlinienobjekts vor.</span><span class="sxs-lookup"><span data-stu-id="fa7f5-123">In the **Group Policy Management Editor** window, make changes to an offline copy of the GPO.</span></span>

    <span data-ttu-id="fa7f5-124">**Hinweis**  Wenn Sie alle Computerkonfigurations Einstellungen oder alle Benutzerkonfigurationseinstellungen deaktivieren möchten, klicken Sie im Fenster **Gruppenrichtlinien-Verwaltungs-Editor** mit der rechten Maustaste auf das Gruppenrichtlinienobjekt, und klicken Sie auf **Eigenschaften**.</span><span class="sxs-lookup"><span data-stu-id="fa7f5-124">**Note** To disable all Computer Configuration settings or all User Configuration settings, right-click the GPO in the **Group Policy Management Editor** window and click **Properties**.</span></span> <span data-ttu-id="fa7f5-125">Wählen Sie **Computer Konfigurationseinstellungen deaktivieren** oder die **Benutzerkonfigurationseinstellungen** je nach Bedarf deaktivieren aus.</span><span class="sxs-lookup"><span data-stu-id="fa7f5-125">Select **Disable Computer Configuration settings** or **Disable User Configuration settings** as appropriate.</span></span>

     

3.  <span data-ttu-id="fa7f5-126">Wenn Sie die Änderung des Gruppenrichtlinienobjekts beendet haben, schließen Sie das Fenster **Gruppenrichtlinien-Verwaltungs-Editor** .</span><span class="sxs-lookup"><span data-stu-id="fa7f5-126">When you have finished modifying the GPO, close the **Group Policy Management Editor** window.</span></span>

### <a href="" id="bkmk-checkin"></a>

**<span data-ttu-id="fa7f5-127">So überprüfen Sie ein GPO in das Archiv</span><span class="sxs-lookup"><span data-stu-id="fa7f5-127">To check a GPO into the archive</span></span>**

1.  <span data-ttu-id="fa7f5-128">Auf der Registerkarte " **gesteuert** ":</span><span class="sxs-lookup"><span data-stu-id="fa7f5-128">On the **Controlled** tab:</span></span>

    -   <span data-ttu-id="fa7f5-129">Wenn Sie keine Änderungen am GPO vorgenommen haben, klicken Sie mit der rechten Maustaste auf das Gruppenrichtlinienobjekt, und klicken Sie auf **Auschecken rückgängig machen**, und klicken Sie dann zum bestätigen auf **Ja** .</span><span class="sxs-lookup"><span data-stu-id="fa7f5-129">If you have made no changes to the GPO, right-click the GPO and click **Undo Check Out**, and then click **Yes** to confirm.</span></span>

    -   <span data-ttu-id="fa7f5-130">Wenn Sie Änderungen am GPO vorgenommen haben, klicken Sie mit der rechten Maustaste auf das Gruppenrichtlinienobjekt, und klicken Sie auf **Einchecken**.</span><span class="sxs-lookup"><span data-stu-id="fa7f5-130">If you have made changes to the GPO, right-click the GPO and click **Check In**.</span></span>

2.  <span data-ttu-id="fa7f5-131">Geben Sie einen Kommentar ein, der im Überwachungspfad des Gruppenrichtlinienobjekts angezeigt werden soll, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="fa7f5-131">Type a comment to be displayed in the audit trail of the GPO, and then click **OK**.</span></span>

3.  <span data-ttu-id="fa7f5-132">Wenn das **Status** Fenster angibt, dass der Gesamtfortschritt abgeschlossen ist, klicken Sie auf **Schließen**.</span><span class="sxs-lookup"><span data-stu-id="fa7f5-132">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="fa7f5-133">Auf der Registerkarte **gesteuert** wird der Status des Gruppenrichtlinienobjekts als **eingecheckt**gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="fa7f5-133">On the **Controlled** tab, the state of the GPO is identified as **Checked In**.</span></span>

### <span data-ttu-id="fa7f5-134">Weitere Überlegungen</span><span class="sxs-lookup"><span data-stu-id="fa7f5-134">Additional considerations</span></span>

-   <span data-ttu-id="fa7f5-135">Zum Auschecken und Bearbeiten eines GPO müssen Sie standardmäßig die genehmigende Person sein, die das Gruppenrichtlinienobjekt, einen Editor oder einen AGPM-Administrator erstellt oder gesteuert hat (Vollzugriff).</span><span class="sxs-lookup"><span data-stu-id="fa7f5-135">To check out and edit a GPO, by default you must be the Approver who created or controlled the GPO, an Editor, or an AGPM Administrator (Full Control).</span></span> <span data-ttu-id="fa7f5-136">Insbesondere müssen Sie über **Listeninhalte** und Berechtigungen zum **Bearbeiten von Einstellungen** für das Gruppenrichtlinienobjekt verfügen.</span><span class="sxs-lookup"><span data-stu-id="fa7f5-136">Specifically, you must have **List Contents** and **Edit Settings** permissions for the GPO.</span></span> <span data-ttu-id="fa7f5-137">Darüber hinaus müssen Sie zum Bearbeiten des Gruppenrichtlinienobjekts die Person sein, die das Gruppenrichtlinienobjekt ausgecheckt hat.</span><span class="sxs-lookup"><span data-stu-id="fa7f5-137">Additionally, to edit the GPO you must be the individual who has checked out the GPO.</span></span>

-   <span data-ttu-id="fa7f5-138">Zum Einchecken eines Gruppenrichtlinienobjekts müssen Sie standardmäßig ein Editor, eine genehmigende Person oder ein AGPM-Administrator (Vollzugriff) sein.</span><span class="sxs-lookup"><span data-stu-id="fa7f5-138">To check in a GPO, by default, you must be an Editor, an Approver, or an AGPM Administrator (Full Control).</span></span> <span data-ttu-id="fa7f5-139">Insbesondere müssen Sie über **Listeninhalte** und entweder **Einstellungen bearbeiten** oder GPO-Berechtigungen für das Gruppenrichtlinienobjekt **Bereitstellen** .</span><span class="sxs-lookup"><span data-stu-id="fa7f5-139">Specifically, you must have **List Contents** and either **Edit Settings** or **Deploy GPO** permissions for the GPO.</span></span> <span data-ttu-id="fa7f5-140">Wenn Sie kein genehmigender oder AGPM-Administrator (oder ein anderer Gruppenrichtlinienadministrator mit der Berechtigung " **GPO bereitstellen** ") sind, müssen Sie der Herausgeber sein, der das Gruppenrichtlinienobjekt ausgecheckt hat.</span><span class="sxs-lookup"><span data-stu-id="fa7f5-140">If you are not an Approver or AGPM Administrator (or other Group Policy administrator with **Deploy GPO** permission), you must be the Editor who has checked out the GPO.</span></span>

-   <span data-ttu-id="fa7f5-141">Beim Bearbeiten eines Gruppenrichtlinienobjekts sollten alle Gruppenrichtlinien-Software Installations Upgrades eines Pakets in einem anderen Gruppenrichtlinienobjekt auf das bereitgestellte Gruppenrichtlinienobjekt und nicht auf die ausgecheckte Kopie verweisen.</span><span class="sxs-lookup"><span data-stu-id="fa7f5-141">When editing a GPO, any Group Policy Software Installation upgrade of a package in another GPO should reference the deployed GPO, and not the checked-out copy.</span></span>

### <span data-ttu-id="fa7f5-142">Weitere Verweise</span><span class="sxs-lookup"><span data-stu-id="fa7f5-142">Additional references</span></span>

-   [<span data-ttu-id="fa7f5-143">Bearbeiten eines Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="fa7f5-143">Editing a GPO</span></span>](editing-a-gpo-agpm40.md)

-   <span data-ttu-id="fa7f5-144">Überprüfen eines Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="fa7f5-144">Reviewing a GPO</span></span>

    -   [<span data-ttu-id="fa7f5-145">Überprüfen von GPO-Einstellungen</span><span class="sxs-lookup"><span data-stu-id="fa7f5-145">Review GPO Settings</span></span>](review-gpo-settings-agpm40.md)

    -   [<span data-ttu-id="fa7f5-146">Überprüfen von GPO-Links</span><span class="sxs-lookup"><span data-stu-id="fa7f5-146">Review GPO Links</span></span>](review-gpo-links-agpm40.md)

    -   [<span data-ttu-id="fa7f5-147">Ermitteln der Unterschiede zwischen Gruppenrichtlinienobjekten und Versionen oder Vorlagen von Gruppenrichtlinienobjekten</span><span class="sxs-lookup"><span data-stu-id="fa7f5-147">Identify Differences Between GPOs, GPO Versions, or Templates</span></span>](identify-differences-between-gpos-gpo-versions-or-templates-agpm40.md)

-   <span data-ttu-id="fa7f5-148">Bereitstellen eines Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="fa7f5-148">Deploying a GPO</span></span>

    -   [<span data-ttu-id="fa7f5-149">Anfordern der Bereitstellung eines Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="fa7f5-149">Request Deployment of a GPO</span></span>](request-deployment-of-a-gpo-agpm40.md)

    -   [<span data-ttu-id="fa7f5-150">Bereitstellen eines Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="fa7f5-150">Deploy a GPO</span></span>](deploy-a-gpo-agpm40.md)

 

 





