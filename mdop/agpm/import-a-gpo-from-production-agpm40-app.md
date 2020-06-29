---
title: Importieren eines Gruppenrichtlinienobjekts aus der Produktion
description: Importieren eines Gruppenrichtlinienobjekts aus der Produktion
author: dansimp
ms.assetid: c5b2f40d-1dc7-4dbf-b8b3-4d97ad73e1e5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ea01341e13696f8b06f22e3f352034b60a713f8a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808415"
---
# <span data-ttu-id="8d156-103">Importieren eines Gruppenrichtlinienobjekts aus der Produktion</span><span class="sxs-lookup"><span data-stu-id="8d156-103">Import a GPO from Production</span></span>


<span data-ttu-id="8d156-104">Wenn Änderungen an einem gesteuerten Gruppenrichtlinienobjekt (GPO) außerhalb der erweiterten Gruppenrichtlinienverwaltung (Group Policy Management, AGPM) vorgenommen werden, können Sie eine Kopie des Gruppenrichtlinienobjekts aus der Produktionsumgebung der Domäne importieren und im Archiv speichern, um das Archiv und die Produktionsumgebung in einen konsistenten Zustand zu versetzen.</span><span class="sxs-lookup"><span data-stu-id="8d156-104">If changes are made to a controlled Group Policy Object (GPO) outside of Advanced Group Policy Management (AGPM), you can import a copy of the GPO from the production environment of the domain and save it to the archive to bring the archive and the production environment to a consistent state.</span></span> <span data-ttu-id="8d156-105">(Zum Importieren eines nicht kontrollierten Gruppenrichtlinienobjekts steuern Sie das Gruppenrichtlinienobjekt.</span><span class="sxs-lookup"><span data-stu-id="8d156-105">(To import an uncontrolled GPO, control the GPO.</span></span> <span data-ttu-id="8d156-106">Siehe [Steuern eines nicht kontrollierten Gruppenrichtlinienobjekts](control-an-uncontrolled-gpo-agpm40.md).)</span><span class="sxs-lookup"><span data-stu-id="8d156-106">See [Control an Uncontrolled GPO](control-an-uncontrolled-gpo-agpm40.md).)</span></span>

<span data-ttu-id="8d156-107">Zum Ausführen dieses Verfahrens ist ein Benutzerkonto mit der Rolle "Editor", "Genehmiger" oder "AGPM-Administrator" (Vollzugriff) oder den erforderlichen Berechtigungen inagpm erforderlich.</span><span class="sxs-lookup"><span data-stu-id="8d156-107">A user account with the Editor, Approver, or AGPM Administrator (Full Control) role or necessary permissions inAGPM is required to complete this procedure.</span></span> <span data-ttu-id="8d156-108">Lesen Sie die Details unter "Weitere Überlegungen" in diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="8d156-108">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="8d156-109">So importieren Sie ein GPO aus der Produktionsumgebung der Domäne</span><span class="sxs-lookup"><span data-stu-id="8d156-109">To import a GPO from the production environment of the domain</span></span>**

1.  <span data-ttu-id="8d156-110">Klicken Sie in der Struktur der **Gruppenrichtlinien-Verwaltungskonsole** in der Gesamtstruktur und Domäne, in der Sie GPOs verwalten möchten, auf **Steuerelement ändern** .</span><span class="sxs-lookup"><span data-stu-id="8d156-110">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="8d156-111">Klicken Sie auf der Registerkarte **Inhalt** auf die Registerkarte **gesteuert** , um die gesteuerten GPOs anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="8d156-111">On the **Contents** tab, click the **Controlled** tab to display the controlled GPOs.</span></span>

3.  <span data-ttu-id="8d156-112">Klicken Sie mit der rechten Maustaste auf das Gruppenrichtlinienobjekt, und klicken Sie dann auf **aus Produktion importieren**.</span><span class="sxs-lookup"><span data-stu-id="8d156-112">Right-click the GPO, and then click **Import from Production**.</span></span>

4.  <span data-ttu-id="8d156-113">Geben Sie einen Kommentar für den Überwachungspfad des Gruppenrichtlinienobjekts ein, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="8d156-113">Type a comment for the audit trail of the GPO, and then click **OK**.</span></span>

### <span data-ttu-id="8d156-114">Weitere Überlegungen</span><span class="sxs-lookup"><span data-stu-id="8d156-114">Additional considerations</span></span>

-   <span data-ttu-id="8d156-115">Standardmäßig müssen Sie Bearbeiter, genehmigende Person oder AGPM-Administrator (Vollzugriff) sein, um dieses Verfahren ausführen zu können.</span><span class="sxs-lookup"><span data-stu-id="8d156-115">By default, you must be an Editor, Approver, or AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="8d156-116">Insbesondere müssen Sie über **Listeninhalte** und entweder **Einstellungen bearbeiten**, **Gruppenrichtlinienobjekt bereitstellen**oder Berechtigungen für **Gruppenrichtlinienobjekte löschen** für das Gruppenrichtlinienobjekt verfügen.</span><span class="sxs-lookup"><span data-stu-id="8d156-116">Specifically, you must have **List Contents** and either **Edit Settings**, **Deploy GPO**, or **Delete GPO** permissions for the GPO.</span></span>

### <span data-ttu-id="8d156-117">Weitere Verweise</span><span class="sxs-lookup"><span data-stu-id="8d156-117">Additional references</span></span>

-   [<span data-ttu-id="8d156-118">Erstellen oder Steuern eines Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="8d156-118">Creating or Controlling a GPO</span></span>](creating-or-controlling-a-gpo-agpm40-app.md)

 

 





