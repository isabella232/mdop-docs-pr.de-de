---
title: Ermitteln der Unterschiede zwischen Gruppenrichtlinienobjekten und Versionen oder Vorlagen von Gruppenrichtlinienobjekten
description: Ermitteln der Unterschiede zwischen Gruppenrichtlinienobjekten und Versionen oder Vorlagen von Gruppenrichtlinienobjekten
author: dansimp
ms.assetid: 6320afc4-af81-47e8-9f4c-463ff99d5a53
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fd7966c9c72b2f0d30595af55520940c779a409f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808435"
---
# <span data-ttu-id="621fc-103">Ermitteln der Unterschiede zwischen Gruppenrichtlinienobjekten und Versionen oder Vorlagen von Gruppenrichtlinienobjekten</span><span class="sxs-lookup"><span data-stu-id="621fc-103">Identify Differences Between GPOs, GPO Versions, or Templates</span></span>


<span data-ttu-id="621fc-104">Sie können HTML-basierte oder XML-basierte Differenz Berichte generieren, um die Unterschiede zwischen Gruppenrichtlinienobjekten (Group Policy Objects, GPOs), Vorlagen oder unterschiedlichen Versionen eines GPO zu analysieren.</span><span class="sxs-lookup"><span data-stu-id="621fc-104">You can generate HTML-based or XML-based difference reports to analyze the differences between Group Policy objects (GPOs), templates, or different versions of a GPO.</span></span>

<span data-ttu-id="621fc-105">Um dieses Verfahren ausführen zu können, ist ein Benutzerkonto mit der Rolle Prüfer, Bearbeiter, Genehmiger oder AGPM-Administrator (Vollzugriff) oder den erforderlichen Berechtigungen in der erweiterten Gruppenrichtlinienverwaltung erforderlich.</span><span class="sxs-lookup"><span data-stu-id="621fc-105">A user account with the Reviewer, Editor, Approver, or AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management is required to complete this procedure.</span></span> <span data-ttu-id="621fc-106">Lesen Sie die Details unter "Weitere Überlegungen" in diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="621fc-106">Review the details in "Additional considerations" in this topic.</span></span>

## <span data-ttu-id="621fc-107">Erkennen von Unterschieden zwischen GPOs, GPO-Versionen oder Vorlagen</span><span class="sxs-lookup"><span data-stu-id="621fc-107">Identifying differences between GPOs, GPO versions, or templates</span></span>


-   [<span data-ttu-id="621fc-108">Zwischen zwei GPOs oder Vorlagen</span><span class="sxs-lookup"><span data-stu-id="621fc-108">Between two GPOs or templates</span></span>](#bkmk-two-gpos)

-   [<span data-ttu-id="621fc-109">Zwischen einem Gruppenrichtlinienobjekt und einer Vorlage</span><span class="sxs-lookup"><span data-stu-id="621fc-109">Between a GPO and a template</span></span>](#bkmk-gpo-and-template)

-   [<span data-ttu-id="621fc-110">Zwischen zwei Versionen eines GPO</span><span class="sxs-lookup"><span data-stu-id="621fc-110">Between two versions of one GPO</span></span>](#bkmk-two-versions)

-   [<span data-ttu-id="621fc-111">Zwischen einer GPO-Version und einer Vorlage</span><span class="sxs-lookup"><span data-stu-id="621fc-111">Between a GPO version and a template</span></span>](#bkmk-gpo-version-and-template)

## <a href="" id="bkmk-two-gpos"></a>


**<span data-ttu-id="621fc-112">So ermitteln Sie Unterschiede zwischen zwei GPOs oder Vorlagen</span><span class="sxs-lookup"><span data-stu-id="621fc-112">To identify differences between two GPOs or templates</span></span>**

1.  <span data-ttu-id="621fc-113">Klicken Sie in der Struktur der **Gruppenrichtlinien-Verwaltungskonsole** in der Gesamtstruktur und Domäne, in der Sie GPOs verwalten möchten, auf **Steuerelement ändern** .</span><span class="sxs-lookup"><span data-stu-id="621fc-113">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="621fc-114">Klicken Sie im Detailbereich auf der Registerkarte **Inhalt** auf eine Registerkarte, um GPOs anzuzeigen (oder Vorlagen, wenn Sie zwei Vorlagen vergleichen).</span><span class="sxs-lookup"><span data-stu-id="621fc-114">On the **Contents** tab in the details pane, click a tab to display GPOs (or templates, if comparing two templates).</span></span>

3.  <span data-ttu-id="621fc-115">Wählen Sie die beiden GPOs oder Vorlagen aus.</span><span class="sxs-lookup"><span data-stu-id="621fc-115">Select the two GPOs or templates.</span></span>

4.  <span data-ttu-id="621fc-116">Klicken Sie mit der rechten Maustaste auf eine der GPOs oder Vorlagen, klicken Sie auf **Unterschiede**, und klicken Sie dann auf **HTML-Bericht** oder **XML-Bericht** , um einen Unterschiedsbericht anzuzeigen, der die Einstellungen der GPOs oder Vorlagen zusammenfasst.</span><span class="sxs-lookup"><span data-stu-id="621fc-116">Right-click one of the GPOs or templates, click **Differences**, and then click **HTML Report** or **XML Report** to display a difference report summarizing the settings of the GPOs or templates.</span></span>

### <a href="" id="bkmk-gpo-and-template"></a>

**<span data-ttu-id="621fc-117">So ermitteln Sie Unterschiede zwischen einem Gruppenrichtlinienobjekt und einer Vorlage</span><span class="sxs-lookup"><span data-stu-id="621fc-117">To identify differences between a GPO and a template</span></span>**

1.  <span data-ttu-id="621fc-118">Klicken Sie in der Struktur der **Gruppenrichtlinien-Verwaltungskonsole** in der Gesamtstruktur und Domäne, in der Sie GPOs verwalten möchten, auf **Steuerelement ändern** .</span><span class="sxs-lookup"><span data-stu-id="621fc-118">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="621fc-119">Klicken Sie im Detailbereich auf der Registerkarte **Inhalt** auf eine Registerkarte, um GPOs anzuzeigen (oder Vorlagen, wenn Sie zwei Vorlagen vergleichen).</span><span class="sxs-lookup"><span data-stu-id="621fc-119">On the **Contents** tab in the details pane, click a tab to display GPOs (or templates, if comparing two templates).</span></span>

3.  <span data-ttu-id="621fc-120">Klicken Sie mit der rechten Maustaste auf das Gruppenrichtlinienobjekt, klicken Sie auf **Unterschiede**und dann auf **Vorlage**.</span><span class="sxs-lookup"><span data-stu-id="621fc-120">Right-click the GPO, click **Differences**, and then click **Template**.</span></span>

4.  <span data-ttu-id="621fc-121">Wählen Sie die Vorlage und den Typ des Berichts aus, und klicken Sie dann auf **OK** , um einen Unterschiedsbericht anzuzeigen, in dem die Einstellungen für das Gruppenrichtlinienobjekt und die Vorlage zusammengefasst sind.</span><span class="sxs-lookup"><span data-stu-id="621fc-121">Select the template and type of report, and then click **OK** to display a difference report summarizing the settings of the GPO and template.</span></span>

### <a href="" id="bkmk-two-versions"></a>

**<span data-ttu-id="621fc-122">So ermitteln Sie Unterschiede zwischen zwei Versionen eines GPO</span><span class="sxs-lookup"><span data-stu-id="621fc-122">To identify differences between two versions of one GPO</span></span>**

1.  <span data-ttu-id="621fc-123">Klicken Sie in der Struktur der **Gruppenrichtlinien-Verwaltungskonsole** in der Gesamtstruktur und Domäne, in der Sie GPOs verwalten möchten, auf **Steuerelement ändern** .</span><span class="sxs-lookup"><span data-stu-id="621fc-123">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="621fc-124">Klicken Sie im Detailbereich auf der Registerkarte **Inhalt** auf eine Registerkarte, um GPOs anzuzeigen (oder Vorlagen, wenn Sie zwei Vorlagen vergleichen).</span><span class="sxs-lookup"><span data-stu-id="621fc-124">On the **Contents** tab in the details pane, click a tab to display GPOs (or templates, if comparing two templates).</span></span>

3.  <span data-ttu-id="621fc-125">Doppelklicken Sie auf das Gruppenrichtlinienobjekt, um dessen Verlauf anzuzeigen, und markieren Sie dann die zu vergleichenden Versionen.</span><span class="sxs-lookup"><span data-stu-id="621fc-125">Double-click the GPO to display its history, and then highlight the versions to be compared.</span></span>

4.  <span data-ttu-id="621fc-126">Klicken Sie mit der rechten Maustaste auf eine der Versionen, klicken Sie auf **Unterschiede**, und klicken Sie dann auf **HTML-Bericht** oder **XML-Bericht** , um einen Unterschiedsbericht anzuzeigen, der die Einstellungen der GPOs zusammenfasst.</span><span class="sxs-lookup"><span data-stu-id="621fc-126">Right-click one of the versions, click **Differences**, and then click **HTML Report** or **XML Report** to display a difference report summarizing the settings of the GPOs.</span></span>

### <a href="" id="bkmk-gpo-version-and-template"></a>

**<span data-ttu-id="621fc-127">So ermitteln Sie Unterschiede zwischen einer GPO-Version und einer Vorlage</span><span class="sxs-lookup"><span data-stu-id="621fc-127">To identify differences between a GPO version and a template</span></span>**

1.  <span data-ttu-id="621fc-128">Klicken Sie in der Struktur der **Gruppenrichtlinien-Verwaltungskonsole** in der Gesamtstruktur und Domäne, in der Sie GPOs verwalten möchten, auf **Steuerelement ändern** .</span><span class="sxs-lookup"><span data-stu-id="621fc-128">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="621fc-129">Klicken Sie im Detailbereich auf der Registerkarte **Inhalt** auf eine Registerkarte, um GPOs anzuzeigen (oder Vorlagen, wenn Sie zwei Vorlagen vergleichen).</span><span class="sxs-lookup"><span data-stu-id="621fc-129">On the **Contents** tab in the details pane, click a tab to display GPOs (or templates, if comparing two templates).</span></span>

3.  <span data-ttu-id="621fc-130">Doppelklicken Sie auf das Gruppenrichtlinienobjekt, um dessen Verlauf anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="621fc-130">Double-click the GPO to display its history.</span></span>

4.  <span data-ttu-id="621fc-131">Klicken Sie mit der rechten Maustaste auf die zu interessierende GPO-Version, klicken Sie auf **Differenzen**, und klicken Sie dann auf **Vorlage**.</span><span class="sxs-lookup"><span data-stu-id="621fc-131">Right-click the GPO version of interest, click **Differences**, and then click **Template**.</span></span>

5.  <span data-ttu-id="621fc-132">Wählen Sie die Vorlage und den Typ des Berichts aus, und klicken Sie dann auf **OK** , um einen Unterschiedsbericht anzuzeigen, in dem die Einstellungen der GPO-Version und-Vorlage zusammengefasst sind.</span><span class="sxs-lookup"><span data-stu-id="621fc-132">Select the template and type of report, and then click **OK** to display a difference report summarizing the settings of the GPO version and template.</span></span>

## <span data-ttu-id="621fc-133">Schlüssel für Unterschiedsberichte</span><span class="sxs-lookup"><span data-stu-id="621fc-133">Key to difference reports</span></span>


<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="621fc-134">Symbol</span><span class="sxs-lookup"><span data-stu-id="621fc-134">Symbol</span></span></th>
<th align="left"><span data-ttu-id="621fc-135">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="621fc-135">Meaning</span></span></th>
<th align="left"><span data-ttu-id="621fc-136">Farbe</span><span class="sxs-lookup"><span data-stu-id="621fc-136">Color</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="621fc-137">Keine</span><span class="sxs-lookup"><span data-stu-id="621fc-137">None</span></span></p></td>
<td align="left"><p><span data-ttu-id="621fc-138">Element mit identischen Einstellungen in beiden GPOs vorhanden</span><span class="sxs-lookup"><span data-stu-id="621fc-138">Item exists with identical settings in both GPOs</span></span></p></td>
<td align="left"><p><span data-ttu-id="621fc-139">Variiert je nach Ebene</span><span class="sxs-lookup"><span data-stu-id="621fc-139">Varies with level</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="621fc-140">[#]</span><span class="sxs-lookup"><span data-stu-id="621fc-140">[#]</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="621fc-141">Element ist in beiden GPOs vorhanden, jedoch mit geänderten Einstellungen</span><span class="sxs-lookup"><span data-stu-id="621fc-141">Item exists in both GPOs, but with changed settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="621fc-142">Blaue</span><span class="sxs-lookup"><span data-stu-id="621fc-142">Blue</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="621fc-143">[-]</span><span class="sxs-lookup"><span data-stu-id="621fc-143">[-]</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="621fc-144">Element ist nur im ersten GPO vorhanden</span><span class="sxs-lookup"><span data-stu-id="621fc-144">Item exists only in the first GPO</span></span></p></td>
<td align="left"><p><span data-ttu-id="621fc-145">Rot</span><span class="sxs-lookup"><span data-stu-id="621fc-145">Red</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="621fc-146">[+]</span><span class="sxs-lookup"><span data-stu-id="621fc-146">[+]</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="621fc-147">Element ist nur im zweiten GPO vorhanden</span><span class="sxs-lookup"><span data-stu-id="621fc-147">Item exists only in the second GPO</span></span></p></td>
<td align="left"><p><span data-ttu-id="621fc-148">Grün</span><span class="sxs-lookup"><span data-stu-id="621fc-148">Green</span></span></p></td>
</tr>
</tbody>
</table>

 

-   <span data-ttu-id="621fc-149">Bei Elementen mit geänderten Einstellungen werden die geänderten Einstellungen identifiziert, wenn das Element erweitert wird.</span><span class="sxs-lookup"><span data-stu-id="621fc-149">For items with changed settings, the changed settings are identified when the item is expanded.</span></span> <span data-ttu-id="621fc-150">Der Wert für das Attribut in den einzelnen Gruppenrichtlinienobjekten wird in der Reihenfolge angezeigt, in der die GPOs im Bericht angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="621fc-150">The value for the attribute in each GPO is displayed in the same order that the GPOs are displayed in the report.</span></span>

-   <span data-ttu-id="621fc-151">Einige Änderungen an Einstellungen können dazu führen, dass ein Element als zwei unterschiedliche Elemente gemeldet wird (eines ist nur im ersten GPO vorhanden, das nur in der zweiten vorhanden ist) und nicht als ein Element, das sich geändert hat.</span><span class="sxs-lookup"><span data-stu-id="621fc-151">Some changes to settings may cause an item to be reported as two different items (one present only in the first GPO, one present only in the second) rather than as one item that has changed.</span></span>

### <span data-ttu-id="621fc-152">Weitere Überlegungen</span><span class="sxs-lookup"><span data-stu-id="621fc-152">Additional considerations</span></span>

-   <span data-ttu-id="621fc-153">Standardmäßig müssen Sie ein Prüfer, ein Bearbeiter, eine genehmigende Person oder ein AGPM-Administrator (Vollzugriff) sein, um dieses Verfahren ausführen zu können.</span><span class="sxs-lookup"><span data-stu-id="621fc-153">By default, you must be a Reviewer, an Editor, an Approver, or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="621fc-154">Insbesondere müssen Sie über die Berechtigungen **Listeninhalt** und **Leseeinstellungen** für das Gruppenrichtlinienobjekt verfügen.</span><span class="sxs-lookup"><span data-stu-id="621fc-154">Specifically, you must have **List Contents** and **Read Settings** permissions for the GPO.</span></span> <span data-ttu-id="621fc-155">Außerdem müssen Sie zum Anzeigen der Liste der GPOs über die Berechtigung **Listeninhalt** für die Domäne verfügen.</span><span class="sxs-lookup"><span data-stu-id="621fc-155">Also, to display the list of GPOs, you must have **List Contents** permission for the domain.</span></span>

### <span data-ttu-id="621fc-156">Weitere Verweise</span><span class="sxs-lookup"><span data-stu-id="621fc-156">Additional references</span></span>

-   [<span data-ttu-id="621fc-157">Durchführen von Prüferaufgaben</span><span class="sxs-lookup"><span data-stu-id="621fc-157">Performing Reviewer Tasks</span></span>](performing-reviewer-tasks.md)

 

 





