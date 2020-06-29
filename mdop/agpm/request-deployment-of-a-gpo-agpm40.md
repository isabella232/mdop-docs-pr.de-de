---
title: Anfordern der Bereitstellung eines Gruppenrichtlinienobjekts
description: Anfordern der Bereitstellung eines Gruppenrichtlinienobjekts
author: dansimp
ms.assetid: 5783cfd0-bd93-46b4-8fa0-684bd39aa8fc
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 46e9cc0fc12962dbdd7758c429a20fdd7c55b3cb
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808284"
---
# <span data-ttu-id="62ee8-103">Anfordern der Bereitstellung eines Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="62ee8-103">Request Deployment of a GPO</span></span>


<span data-ttu-id="62ee8-104">Nachdem Sie ein Gruppenrichtlinienobjekt (GPO) geändert und eingecheckt haben, stellen Sie das Gruppenrichtlinienobjekt bereit, damit es in der Produktionsumgebung wirksam wird.</span><span class="sxs-lookup"><span data-stu-id="62ee8-104">After you have modified and checked in a Group Policy Object (GPO), deploy the GPO, so it will take effect in the production environment.</span></span>

<span data-ttu-id="62ee8-105">Um dieses Verfahren ausführen zu können, ist ein Benutzerkonto mit der Rolle "Editor" oder den erforderlichen Berechtigungen in Advanced Group Policy Management (AGPM) erforderlich.</span><span class="sxs-lookup"><span data-stu-id="62ee8-105">A user account with the Editor role or necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span> <span data-ttu-id="62ee8-106">Lesen Sie die Details unter "Weitere Überlegungen" in diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="62ee8-106">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="62ee8-107">So fordern Sie die Bereitstellungeines GPO in der Produktionsumgebung der Domäne an</span><span class="sxs-lookup"><span data-stu-id="62ee8-107">To request the deployment of a GPO to the production environment of the domain</span></span>**

1.  <span data-ttu-id="62ee8-108">Klicken Sie in der Struktur der **Gruppenrichtlinien-Verwaltungskonsole** in der Gesamtstruktur und Domäne, in der Sie GPOs verwalten möchten, auf **Steuerelement ändern** .</span><span class="sxs-lookup"><span data-stu-id="62ee8-108">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="62ee8-109">Klicken Sie auf der Registerkarte **Inhalt** auf die Registerkarte **gesteuert** , um die gesteuerten GPOs anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="62ee8-109">On the **Contents** tab, click the **Controlled** tab to display the controlled GPOs.</span></span>

3.  <span data-ttu-id="62ee8-110">Klicken Sie mit der rechten Maustaste auf das zu implementierende GPO, und klicken Sie dann auf **Bereitstellen**.</span><span class="sxs-lookup"><span data-stu-id="62ee8-110">Right-click the GPO to be deployed, and then click **Deploy**.</span></span>

4.  <span data-ttu-id="62ee8-111">Sofern Sie kein genehmigender oder AGPM-Administrator sind oder über eine besondere Berechtigung zum Bereitstellen von GPOs verfügen, müssen Sie eine Anforderung für die Bereitstellung einreichen.</span><span class="sxs-lookup"><span data-stu-id="62ee8-111">Unless you are an Approver or AGPM Administrator or have special permission to deploy GPOs, you must submit a request for deployment.</span></span> <span data-ttu-id="62ee8-112">Wenn Sie eine Kopie der Anfrage erhalten möchten, geben Sie Ihre e-Mail-Adresse in das Feld **CC** ein.</span><span class="sxs-lookup"><span data-stu-id="62ee8-112">To receive a copy of the request, type your e-mail address in the **Cc** field.</span></span> <span data-ttu-id="62ee8-113">Geben Sie einen Kommentar ein, der im **Protokoll** für das Gruppenrichtlinienobjekt angezeigt werden soll, und klicken Sie dann auf **Absenden**.</span><span class="sxs-lookup"><span data-stu-id="62ee8-113">Type a comment to be displayed in the **History** for the GPO, and then click **Submit**.</span></span>

5.  <span data-ttu-id="62ee8-114">Wenn das **Status** Fenster angibt, dass der Gesamtfortschritt abgeschlossen ist, klicken Sie auf **Schließen**.</span><span class="sxs-lookup"><span data-stu-id="62ee8-114">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="62ee8-115">Das Gruppenrichtlinienobjekt wird in der Liste der GPOs auf der Registerkarte **Ausstehend** angezeigt. Wenn eine genehmigende Person Ihre Anforderung genehmigt hat, wird das Gruppenrichtlinienobjekt von der Registerkarte **Ausstehend** auf die Registerkarte **gesteuert** verschoben und bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="62ee8-115">The GPO is displayed on the list of GPOs on the **Pending** tab. When an Approver has approved your request, the GPO will be moved from the **Pending** tab to the **Controlled** tab and be deployed.</span></span>

### <span data-ttu-id="62ee8-116">Weitere Überlegungen</span><span class="sxs-lookup"><span data-stu-id="62ee8-116">Additional considerations</span></span>

-   <span data-ttu-id="62ee8-117">Standardmäßig müssen Sie ein Editor sein, um dieses Verfahren ausführen zu können.</span><span class="sxs-lookup"><span data-stu-id="62ee8-117">By default, you must be an Editor to perform this procedure.</span></span> <span data-ttu-id="62ee8-118">Insbesondere müssen Sie über **Listeninhalte** und Berechtigungen zum **Bearbeiten von Einstellungen** für das Gruppenrichtlinienobjekt verfügen.</span><span class="sxs-lookup"><span data-stu-id="62ee8-118">Specifically, you must have **List Contents** and **Edit Settings** permissions for the GPO.</span></span>

-   <span data-ttu-id="62ee8-119">Wenn Sie Ihre Anfrage zurücknehmen möchten, bevor Sie genehmigt wurde, klicken Sie auf die Registerkarte **Ausstehend** . Klicken Sie mit der rechten Maustaste auf das GPO, und klicken Sie dann auf **zurück**</span><span class="sxs-lookup"><span data-stu-id="62ee8-119">To withdraw your request before it has been approved, click the **Pending** tab. Right-click the GPO, and then click **Withdraw**.</span></span> <span data-ttu-id="62ee8-120">Das Gruppenrichtlinienobjekt wird auf die Registerkarte **gesteuert** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="62ee8-120">The GPO will be returned to the **Controlled** tab.</span></span>

### <span data-ttu-id="62ee8-121">Weitere Verweise</span><span class="sxs-lookup"><span data-stu-id="62ee8-121">Additional references</span></span>

-   [<span data-ttu-id="62ee8-122">Durchführen von Editor-Aufgaben</span><span class="sxs-lookup"><span data-stu-id="62ee8-122">Performing Editor Tasks</span></span>](performing-editor-tasks-agpm40.md)

 

 





