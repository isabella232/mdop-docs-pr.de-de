---
title: Überprüfen von GPO-Links
description: Überprüfen von GPO-Links
author: dansimp
ms.assetid: 3c472448-f16a-493c-a229-5ca60a470965
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fe8b40b4401f08a36217237487bf2b2c0c6c0689
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807468"
---
# <span data-ttu-id="be2bc-103">Überprüfen von GPO-Links</span><span class="sxs-lookup"><span data-stu-id="be2bc-103">Review GPO Links</span></span>


<span data-ttu-id="be2bc-104">Sie können ein Diagramm anzeigen, das zeigt, wo ein von Ihnen ausgewähltes Gruppenrichtlinienobjekt (GPO) oder GPOs mit Organisationseinheiten verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="be2bc-104">You can display a diagram showing where a Group Policy object (GPO) or GPOs that you select are linked to organizational units.</span></span> <span data-ttu-id="be2bc-105">GPO-Verknüpfungs Diagramme werden jedes Mal aktualisiert, wenn das Gruppenrichtlinienobjekt gesteuert, importiert oder eingecheckt wird.</span><span class="sxs-lookup"><span data-stu-id="be2bc-105">GPO link diagrams are updated each time the GPO is controlled, imported, or checked in.</span></span>

<span data-ttu-id="be2bc-106">Um dieses Verfahren ausführen zu können, ist ein Benutzerkonto mit der Rolle Prüfer, Bearbeiter, Genehmiger oder AGPM-Administrator (Vollzugriff) oder den erforderlichen Berechtigungen in der erweiterten Gruppenrichtlinienverwaltung erforderlich.</span><span class="sxs-lookup"><span data-stu-id="be2bc-106">A user account with the Reviewer, Editor, Approver, or AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management is required to complete this procedure.</span></span> <span data-ttu-id="be2bc-107">Lesen Sie die Details unter "Weitere Überlegungen" in diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="be2bc-107">Review the details in "Additional considerations" in this topic.</span></span>

## <span data-ttu-id="be2bc-108">Überprüfen von GPO-Links</span><span class="sxs-lookup"><span data-stu-id="be2bc-108">Reviewing GPO links</span></span>


-   [<span data-ttu-id="be2bc-109">Für ein oder mehrere GPOs</span><span class="sxs-lookup"><span data-stu-id="be2bc-109">For one or more GPOs</span></span>](#bkmk-gpos)

-   [<span data-ttu-id="be2bc-110">Für eine oder mehrere Versionen eines Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="be2bc-110">For one or more versions of a GPO</span></span>](#bkmk-gpo-versions)

### <a href="" id="bkmk-gpos"></a>

**<span data-ttu-id="be2bc-111">So zeigen Sie GPO-Links für ein oder mehrere GPOs an</span><span class="sxs-lookup"><span data-stu-id="be2bc-111">To display GPO links for one or more GPOs</span></span>**

1.  <span data-ttu-id="be2bc-112">Klicken Sie in der Struktur der **Gruppenrichtlinien-Verwaltungskonsole** in der Gesamtstruktur und Domäne, in der Sie GPOs verwalten möchten, auf **Steuerelement ändern** .</span><span class="sxs-lookup"><span data-stu-id="be2bc-112">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="be2bc-113">Klicken Sie im Detailbereich auf der Registerkarte **Inhalt** auf die Registerkarte **gesteuert**, **Ausstehend**oder **Papierkorb** , um GPOs anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="be2bc-113">On the **Contents** tab in the details pane, click the **Controlled**, **Pending**, or **Recycle Bin** tab to display GPOs.</span></span>

3.  <span data-ttu-id="be2bc-114">Wählen Sie ein oder mehrere GPOs aus, für die Links angezeigt werden sollen, klicken Sie mit der rechten Maustaste auf ein ausgewähltes Gruppenrichtlinienobjekt, klicken Sie auf **Einstellungen**, und klicken Sie dann auf **GPO-Links** , um ein Diagramm mit Domänen und Organisationseinheiten mit Links zu den ausgewählten Gruppenrichtlinienobjekten anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="be2bc-114">Select one or more GPOs for which to display links, right-click a selected GPO, click **Settings**, and then click **GPO Links** to display a diagram of domains and organizational units with links to the selected GPO(s).</span></span>

### <a href="" id="bkmk-gpo-versions"></a>

**<span data-ttu-id="be2bc-115">So zeigen Sie GPO-Links für eine oder mehrere Versionen eines GPO an</span><span class="sxs-lookup"><span data-stu-id="be2bc-115">To display GPO links for one or more versions of a GPO</span></span>**

1.  <span data-ttu-id="be2bc-116">Klicken Sie in der Struktur der **Gruppenrichtlinien-Verwaltungskonsole** in der Gesamtstruktur und Domäne, in der Sie GPOs verwalten möchten, auf **Steuerelement ändern** .</span><span class="sxs-lookup"><span data-stu-id="be2bc-116">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="be2bc-117">Klicken Sie im Detailbereich auf der Registerkarte **Inhalt** auf die Registerkarte **gesteuerter** oder **Papierkorb** , um GPOs anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="be2bc-117">On the **Contents** tab in the details pane, click the **Controlled** or **Recycle Bin** tab to display GPOs.</span></span>

3.  <span data-ttu-id="be2bc-118">Doppelklicken Sie auf das Gruppenrichtlinienobjekt, um dessen Verlauf anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="be2bc-118">Double-click the GPO to display its history.</span></span>

4.  <span data-ttu-id="be2bc-119">Klicken Sie mit der rechten Maustaste auf die GPO-Version, für die Sie die Einstellungen überprüfen möchten, klicken Sie auf **Einstellungen**, und klicken Sie dann auf **HTML-Bericht** oder **XML-Bericht** , um eine Zusammenfassung der GPO-Einstellungen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="be2bc-119">Right-click the GPO version for which to review the settings, click **Settings**, and then click **HTML Report** or **XML Report** to display a summary of the GPO's settings.</span></span>

### <span data-ttu-id="be2bc-120">Weitere Überlegungen</span><span class="sxs-lookup"><span data-stu-id="be2bc-120">Additional considerations</span></span>

-   <span data-ttu-id="be2bc-121">Standardmäßig müssen Sie ein Prüfer, ein Bearbeiter, eine genehmigende Person oder ein AGPM-Administrator (Vollzugriff) sein, um dieses Verfahren ausführen zu können.</span><span class="sxs-lookup"><span data-stu-id="be2bc-121">By default, you must be a Reviewer, an Editor, an Approver, or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="be2bc-122">Insbesondere müssen Sie über die Berechtigungen **Listeninhalt** und **Leseeinstellungen** für das Gruppenrichtlinienobjekt verfügen.</span><span class="sxs-lookup"><span data-stu-id="be2bc-122">Specifically, you must have **List Contents** and **Read Settings** permissions for the GPO.</span></span> <span data-ttu-id="be2bc-123">Außerdem müssen Sie zum Anzeigen der Liste der GPOs über die Berechtigung **Listeninhalt** für die Domäne verfügen.</span><span class="sxs-lookup"><span data-stu-id="be2bc-123">Also, to display the list of GPOs, you must have **List Contents** permission for the domain.</span></span>

### <span data-ttu-id="be2bc-124">Weitere Verweise</span><span class="sxs-lookup"><span data-stu-id="be2bc-124">Additional references</span></span>

-   [<span data-ttu-id="be2bc-125">Durchführen von Prüferaufgaben</span><span class="sxs-lookup"><span data-stu-id="be2bc-125">Performing Reviewer Tasks</span></span>](performing-reviewer-tasks.md)

 

 





