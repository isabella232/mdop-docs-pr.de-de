---
title: Anfordern eines nicht gesteuerten Gruppenrichtlinienobjekts
description: Anfordern eines nicht gesteuerten Gruppenrichtlinienobjekts
author: dansimp
ms.assetid: a34e0aeb-33a1-4c9f-b187-1d08493a785c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: bfccd7285f82990c2447319485738131cf559f48
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807511"
---
# <span data-ttu-id="61a13-103">Anfordern eines nicht gesteuerten Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="61a13-103">Request Control of an Uncontrolled GPO</span></span>


<span data-ttu-id="61a13-104">Um das Change-Steuerelement für ein vorhandenes Gruppenrichtlinienobjekt (GPO) bereitstellen zu können, muss das Gruppenrichtlinienobjekt gesteuert werden.</span><span class="sxs-lookup"><span data-stu-id="61a13-104">To provide change control for an existing Group Policy Object (GPO), the GPO must be controlled.</span></span> <span data-ttu-id="61a13-105">Sofern Sie keine genehmigende Person oder ein AGPM-Administrator (Vollzugriff) sind, müssen Sie die Steuerung des GPO anfordern.</span><span class="sxs-lookup"><span data-stu-id="61a13-105">Unless you are an Approver or an AGPM Administrator (Full Control), you must request that the GPO be controlled.</span></span>

<span data-ttu-id="61a13-106">Um dieses Verfahren ausführen zu können, ist ein Benutzerkonto mit der Rolle "Bearbeiter" oder "Prüfer" oder die erforderlichen Berechtigungen in Advanced Group Policy Management (AGPM) erforderlich.</span><span class="sxs-lookup"><span data-stu-id="61a13-106">A user account with the Editor or Reviewer role or necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span> <span data-ttu-id="61a13-107">Lesen Sie die Details unter "Weitere Überlegungen" in diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="61a13-107">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="61a13-108">So steuern Sie ein nicht gesteuertes Gruppenrichtlinienobjekt</span><span class="sxs-lookup"><span data-stu-id="61a13-108">To control an uncontrolled GPO</span></span>**

1.  <span data-ttu-id="61a13-109">Klicken Sie in der Struktur der **Gruppenrichtlinien-Verwaltungskonsole** in der Gesamtstruktur und Domäne, in der Sie GPOs verwalten möchten, auf **Steuerelement ändern** .</span><span class="sxs-lookup"><span data-stu-id="61a13-109">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="61a13-110">Klicken Sie im Detailbereich auf der Registerkarte **Inhalt** auf die Registerkarte **unkontrolliert** , um die nicht kontrollierten GPOs anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="61a13-110">On the **Contents** tab in the details pane, click the **Uncontrolled** tab to display the uncontrolled GPOs.</span></span>

3.  <span data-ttu-id="61a13-111">Klicken Sie mit der rechten Maustaste auf das Gruppenrichtlinienobjekt, das mit AGPM gesteuert werden soll, und klicken Sie dann auf **Steuerelement**.</span><span class="sxs-lookup"><span data-stu-id="61a13-111">Right-click the GPO to be controlled with AGPM, and then click **Control**.</span></span>

4.  <span data-ttu-id="61a13-112">Sofern Sie keine spezielle Berechtigung zum Steuern von GPOs haben, müssen Sie eine Kontroll Anforderung einreichen.</span><span class="sxs-lookup"><span data-stu-id="61a13-112">Unless you have special permission to control GPOs, you must submit a request for control.</span></span> <span data-ttu-id="61a13-113">Wenn Sie eine Kopie der Anfrage erhalten möchten, geben Sie Ihre e-Mail-Adresse in das Feld **CC** ein.</span><span class="sxs-lookup"><span data-stu-id="61a13-113">To receive a copy of the request, type your e-mail address in the **Cc** field.</span></span> <span data-ttu-id="61a13-114">Geben Sie einen Kommentar ein, der im **Verlauf** des Gruppenrichtlinienobjekts angezeigt werden soll, und klicken Sie dann auf **Absenden**.</span><span class="sxs-lookup"><span data-stu-id="61a13-114">Type a comment to be displayed in the **History** of the GPO, and then click **Submit**.</span></span>

5.  <span data-ttu-id="61a13-115">Wenn das **Status** Fenster angibt, dass der Gesamtfortschritt abgeschlossen ist, klicken Sie auf **Schließen**.</span><span class="sxs-lookup"><span data-stu-id="61a13-115">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="61a13-116">Das Gruppenrichtlinienobjekt wird auf der Registerkarte **unkontrolliert** aus der Liste entfernt und der Registerkarte **Ausstehend** hinzugefügt. Wenn eine genehmigende Person Ihre Anfrage genehmigt hat, wird das Gruppenrichtlinienobjekt auf die Registerkarte **gesteuert** verschoben.</span><span class="sxs-lookup"><span data-stu-id="61a13-116">The GPO is removed from the list on the **Uncontrolled** tab and added to the **Pending** tab. When an Approver has approved your request, the GPO will be moved to the **Controlled** tab.</span></span>

### <span data-ttu-id="61a13-117">Weitere Überlegungen</span><span class="sxs-lookup"><span data-stu-id="61a13-117">Additional considerations</span></span>

-   <span data-ttu-id="61a13-118">Standardmäßig müssen Sie ein Editor oder ein Bearbeiter sein, um dieses Verfahren ausführen zu können.</span><span class="sxs-lookup"><span data-stu-id="61a13-118">By default, you must be an Editor or a Reviewer to perform this procedure.</span></span> <span data-ttu-id="61a13-119">Insbesondere müssen Sie über die Berechtigungen **Listeninhalt** und **Leseeinstellungen** für die Domäne verfügen.</span><span class="sxs-lookup"><span data-stu-id="61a13-119">Specifically, you must have **List Contents** and **Read Settings** permissions for the domain.</span></span>

-   <span data-ttu-id="61a13-120">Wenn Sie Ihre Anfrage zurücknehmen möchten, bevor Sie genehmigt wurde, klicken Sie auf die Registerkarte **Ausstehend** . Klicken Sie mit der rechten Maustaste auf das GPO, und klicken Sie dann auf **zurück**</span><span class="sxs-lookup"><span data-stu-id="61a13-120">To withdraw your request before it has been approved, click the **Pending** tab. Right-click the GPO, and then click **Withdraw**.</span></span> <span data-ttu-id="61a13-121">Das Gruppenrichtlinienobjekt wird auf die Registerkarte **unkontrolliert** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="61a13-121">The GPO will be returned to the **Uncontrolled** tab.</span></span>

### <span data-ttu-id="61a13-122">Weitere Verweise</span><span class="sxs-lookup"><span data-stu-id="61a13-122">Additional references</span></span>

-   [<span data-ttu-id="61a13-123">Erstellen oder Steuern eines Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="61a13-123">Creating or Controlling a GPO</span></span>](creating-or-controlling-a-gpo-agpm40-ed.md)

 

 





