---
title: Durchführen der Aufgaben von genehmigenden Personen
description: Durchführen der Aufgaben von genehmigenden Personen
author: dansimp
ms.assetid: 9f711824-191b-4b4b-a1c6-a3b2116006a4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d8e4a848608a3be1dbb0632f0145b4fc1d1bc631
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808320"
---
# <span data-ttu-id="e4f2f-103">Durchführen der Aufgaben von genehmigenden Personen</span><span class="sxs-lookup"><span data-stu-id="e4f2f-103">Performing Approver Tasks</span></span>


<span data-ttu-id="e4f2f-104">Eine genehmigende Person ist eine von einem AGPM-Administrator (Vollzugriff) autorisierte Person zum Erstellen, bereitstellen und Löschen von Gruppenrichtlinienobjekten (Group Policy Objects, GPOs) sowie zum genehmigen oder ablehnen von Anforderungen (in der Regel von Editoren) zum Erstellen, bereitstellen oder Löschen von GPOs.</span><span class="sxs-lookup"><span data-stu-id="e4f2f-104">An Approver is a person authorized by an AGPM Administrator (Full Control) to create, deploy, and delete Group Policy Objects (GPOs) and to approve or reject requests (typically from Editors) to create, deploy, or delete GPOs.</span></span>

<span data-ttu-id="e4f2f-105">**Wichtig**  Stellen Sie sicher, dass Sie eine Verbindung mit dem zentralen Archiv für GPOs herstellen.</span><span class="sxs-lookup"><span data-stu-id="e4f2f-105">**Important** Make sure that you are connecting to the central archive for GPOs.</span></span> <span data-ttu-id="e4f2f-106">Weitere Informationen finden Sie unter [Konfigurieren einer AGPM-Server Verbindung](configure-an-agpm-server-connection-reviewer-agpm30ops.md).</span><span class="sxs-lookup"><span data-stu-id="e4f2f-106">For more information, see [Configure an AGPM Server Connection](configure-an-agpm-server-connection-reviewer-agpm30ops.md).</span></span>

 

-   [<span data-ttu-id="e4f2f-107">Genehmigen oder Ablehnen einer ausstehenden Aktion</span><span class="sxs-lookup"><span data-stu-id="e4f2f-107">Approve or Reject a Pending Action</span></span>](approve-or-reject-a-pending-action-agpm30ops.md)

-   [<span data-ttu-id="e4f2f-108">Erstellen, Steuern oder Importieren eines Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="e4f2f-108">Creating, Controlling, or Importing a GPO</span></span>](creating-controlling-or-importing-a-gpo-editor-agpm30ops.md)

-   [<span data-ttu-id="e4f2f-109">Einchecken eines Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="e4f2f-109">Check In a GPO</span></span>](check-in-a-gpo-agpm30ops.md)

-   [<span data-ttu-id="e4f2f-110">Bereitstellen eines Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="e4f2f-110">Deploy a GPO</span></span>](deploy-a-gpo-agpm30ops.md)

-   [<span data-ttu-id="e4f2f-111">Zurücksetzen auf eine frühere Version eines Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="e4f2f-111">Roll Back to a Previous Version of a GPO</span></span>](roll-back-to-a-previous-version-of-a-gpo-agpm30ops.md)

-   [<span data-ttu-id="e4f2f-112">Löschen, Wiederherstellen oder Zerstören eines Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="e4f2f-112">Deleting, Restoring, or Destroying a GPO</span></span>](deleting-restoring-or-destroying-a-gpo-agpm30ops.md)

<span data-ttu-id="e4f2f-113">**Hinweis**  Bevor Sie ein GPO genehmigen, sollte eine genehmigende Person die darin enthaltenen Richtlinieneinstellungen überprüfen.</span><span class="sxs-lookup"><span data-stu-id="e4f2f-113">**Note** Before approving a GPO, an Approver should review the policy settings that it contains.</span></span> <span data-ttu-id="e4f2f-114">Die Rolle genehmigende Person umfasst die Berechtigungen für die Rolle Prüfer, damit eine genehmigende Person Richtlinieneinstellungen überprüfen und GPOs vergleichen kann.</span><span class="sxs-lookup"><span data-stu-id="e4f2f-114">The Approver role includes the permissions for the Reviewer role, so that an Approver can review policy settings and compare GPOs.</span></span> <span data-ttu-id="e4f2f-115">Weitere Informationen finden Sie unter [Ausführen von Aufgaben für Bearbeiter](performing-reviewer-tasks-agpm30ops.md) .</span><span class="sxs-lookup"><span data-stu-id="e4f2f-115">See [Performing Reviewer Tasks](performing-reviewer-tasks-agpm30ops.md) for more information.</span></span>

 

### <span data-ttu-id="e4f2f-116">Weitere Überlegungen</span><span class="sxs-lookup"><span data-stu-id="e4f2f-116">Additional considerations</span></span>

<span data-ttu-id="e4f2f-117">Standardmäßig werden die folgenden Berechtigungen für die genehmigende Rolle bereitgestellt:</span><span class="sxs-lookup"><span data-stu-id="e4f2f-117">By default, the following permissions are provided for the Approver role:</span></span>

-   <span data-ttu-id="e4f2f-118">Listeninhalt</span><span class="sxs-lookup"><span data-stu-id="e4f2f-118">List Contents</span></span>

-   <span data-ttu-id="e4f2f-119">Leseeinstellungen</span><span class="sxs-lookup"><span data-stu-id="e4f2f-119">Read Settings</span></span>

-   <span data-ttu-id="e4f2f-120">Erstellen eines GPO</span><span class="sxs-lookup"><span data-stu-id="e4f2f-120">Create GPO</span></span>

-   <span data-ttu-id="e4f2f-121">Bereitstellen von Gruppenrichtlinienobjekten</span><span class="sxs-lookup"><span data-stu-id="e4f2f-121">Deploy GPO</span></span>

-   <span data-ttu-id="e4f2f-122">Gruppenrichtlinienobjekt löschen</span><span class="sxs-lookup"><span data-stu-id="e4f2f-122">Delete GPO</span></span>

<span data-ttu-id="e4f2f-123">Darüber hinaus hat eine genehmigende Person die vollständige Kontrolle über die von ihm erstellten oder kontrollierten GPOs.</span><span class="sxs-lookup"><span data-stu-id="e4f2f-123">Also, an Approver has full control over GPOs that he created or controlled.</span></span>

 

 





