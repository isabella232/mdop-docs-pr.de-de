---
title: Importieren eines Gruppenrichtlinienobjekts aus der Produktion
description: Importieren eines Gruppenrichtlinienobjekts aus der Produktion
author: dansimp
ms.assetid: ad14203a-2e6a-41d4-a05e-4508c80045fd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 04fd76eff5bac5cce5c02d3d2330226415ba003e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808407"
---
# <span data-ttu-id="e60b3-103">Importieren eines Gruppenrichtlinienobjekts aus der Produktion</span><span class="sxs-lookup"><span data-stu-id="e60b3-103">Import a GPO from Production</span></span>


<span data-ttu-id="e60b3-104">Wenn Änderungen an einem gesteuerten Gruppenrichtlinienobjekt (GPO) außerhalb der erweiterten Gruppenrichtlinienverwaltung (Group Policy Management, AGPM) vorgenommen werden, können Sie eine Kopie des Gruppenrichtlinienobjekts aus der Produktionsumgebung der Domäne importieren und im Archiv speichern, um das Archiv und die Produktionsumgebung in einen konsistenten Zustand zu versetzen.</span><span class="sxs-lookup"><span data-stu-id="e60b3-104">If changes are made to a controlled Group Policy Object (GPO) outside of Advanced Group Policy Management (AGPM), you can import a copy of the GPO from the production environment of the domain and save it to the archive to bring the archive and the production environment to a consistent state.</span></span> <span data-ttu-id="e60b3-105">(Zum Importieren eines nicht kontrollierten Gruppenrichtlinienobjekts steuern Sie das Gruppenrichtlinienobjekt.</span><span class="sxs-lookup"><span data-stu-id="e60b3-105">(To import an uncontrolled GPO, control the GPO.</span></span> <span data-ttu-id="e60b3-106">Siehe [anfordern der Steuerung eines nicht kontrollierten Gruppenrichtlinienobjekts](request-control-of-an-uncontrolled-gpo-agpm40.md).)</span><span class="sxs-lookup"><span data-stu-id="e60b3-106">See [Request Control of an Uncontrolled GPO](request-control-of-an-uncontrolled-gpo-agpm40.md).)</span></span>

<span data-ttu-id="e60b3-107">Zum Ausführen dieses Verfahrens ist ein Benutzerkonto mit der Rolle "Editor", "Genehmiger" oder "AGPM-Administrator" (Vollzugriff) oder den erforderlichen Berechtigungen inagpm erforderlich.</span><span class="sxs-lookup"><span data-stu-id="e60b3-107">A user account with the Editor, Approver, or AGPM Administrator (Full Control) role or necessary permissions inAGPM is required to complete this procedure.</span></span> <span data-ttu-id="e60b3-108">Lesen Sie die Details unter "Weitere Überlegungen" in diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="e60b3-108">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="e60b3-109">So importieren Sie ein GPO aus der Produktionsumgebung der Domäne</span><span class="sxs-lookup"><span data-stu-id="e60b3-109">To import a GPO from the production environment of the domain</span></span>**

1.  <span data-ttu-id="e60b3-110">Klicken Sie in der Struktur der **Gruppenrichtlinien-Verwaltungskonsole** in der Gesamtstruktur und Domäne, in der Sie GPOs verwalten möchten, auf **Steuerelement ändern** .</span><span class="sxs-lookup"><span data-stu-id="e60b3-110">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="e60b3-111">Klicken Sie auf der Registerkarte **Inhalt** auf die Registerkarte **gesteuert** , um die gesteuerten GPOs anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="e60b3-111">On the **Contents** tab, click the **Controlled** tab to display the controlled GPOs.</span></span>

3.  <span data-ttu-id="e60b3-112">Klicken Sie mit der rechten Maustaste auf das Gruppenrichtlinienobjekt, und klicken Sie dann auf **aus Produktion importieren**.</span><span class="sxs-lookup"><span data-stu-id="e60b3-112">Right-click the GPO, and then click **Import from Production**.</span></span>

4.  <span data-ttu-id="e60b3-113">Geben Sie einen Kommentar für den Überwachungspfad des Gruppenrichtlinienobjekts ein, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="e60b3-113">Type a comment for the audit trail of the GPO, and then click **OK**.</span></span>

### <span data-ttu-id="e60b3-114">Weitere Überlegungen</span><span class="sxs-lookup"><span data-stu-id="e60b3-114">Additional considerations</span></span>

-   <span data-ttu-id="e60b3-115">Standardmäßig müssen Sie Bearbeiter, genehmigende Person oder AGPM-Administrator (Vollzugriff) sein, um dieses Verfahren ausführen zu können.</span><span class="sxs-lookup"><span data-stu-id="e60b3-115">By default, you must be an Editor, Approver, or AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="e60b3-116">Insbesondere müssen Sie über **Listeninhalte** und entweder **Einstellungen bearbeiten**, **Gruppenrichtlinienobjekt bereitstellen**oder Berechtigungen für **Gruppenrichtlinienobjekte löschen** für das Gruppenrichtlinienobjekt verfügen.</span><span class="sxs-lookup"><span data-stu-id="e60b3-116">Specifically, you must have **List Contents** and either **Edit Settings**, **Deploy GPO**, or **Delete GPO** permissions for the GPO.</span></span>

### <span data-ttu-id="e60b3-117">Weitere Verweise</span><span class="sxs-lookup"><span data-stu-id="e60b3-117">Additional references</span></span>

-   [<span data-ttu-id="e60b3-118">Erstellen oder Steuern eines Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="e60b3-118">Creating or Controlling a GPO</span></span>](creating-or-controlling-a-gpo-agpm40-ed.md)

 

 





