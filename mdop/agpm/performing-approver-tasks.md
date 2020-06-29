---
title: Durchführen der Aufgaben von genehmigenden Personen
description: Durchführen der Aufgaben von genehmigenden Personen
author: dansimp
ms.assetid: 6f6310b3-19c1-47c9-8615-964ddd10ce14
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fc77a1dd9a3d54e637ae4baeb452d327672ed250
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808303"
---
# <span data-ttu-id="db159-103">Durchführen der Aufgaben von genehmigenden Personen</span><span class="sxs-lookup"><span data-stu-id="db159-103">Performing Approver Tasks</span></span>


<span data-ttu-id="db159-104">Eine genehmigende Person ist eine von einem AGPM-Administrator (Vollzugriff) autorisierte Person zum Erstellen, bereitstellen und Löschen von Gruppenrichtlinienobjekten (Group Policy Objects, GPOs) sowie zum genehmigen oder ablehnen von Anforderungen (in der Regel von Editoren) zum Erstellen, bereitstellen oder Löschen von GPOs.</span><span class="sxs-lookup"><span data-stu-id="db159-104">An Approver is a person authorized by an AGPM Administrator (Full Control) to create, deploy, and delete Group Policy objects (GPOs) and to approve or reject requests (typically from Editors) to create, deploy, or delete GPOs.</span></span>

<span data-ttu-id="db159-105">**Wichtig**  Stellen Sie sicher, dass Sie eine Verbindung mit dem zentralen Archiv für GPOs herstellen.</span><span class="sxs-lookup"><span data-stu-id="db159-105">**Important** Ensure that you are connecting to the central archive for GPOs.</span></span> <span data-ttu-id="db159-106">Weitere Informationen finden Sie unter [Konfigurieren der AGPM-Server Verbindung](configure-the-agpm-server-connection-reviewer.md).</span><span class="sxs-lookup"><span data-stu-id="db159-106">For more information, see [Configure the AGPM Server Connection](configure-the-agpm-server-connection-reviewer.md).</span></span>

 

-   [<span data-ttu-id="db159-107">Genehmigen oder Ablehnen einer ausstehenden Aktion</span><span class="sxs-lookup"><span data-stu-id="db159-107">Approve or Reject a Pending Action</span></span>](approve-or-reject-a-pending-action.md)

-   [<span data-ttu-id="db159-108">Erstellen, Steuern oder Importieren eines Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="db159-108">Creating, Controlling, or Importing a GPO</span></span>](creating-controlling-or-importing-a-gpo-approver.md)

-   [<span data-ttu-id="db159-109">Einchecken eines Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="db159-109">Check In a GPO</span></span>](check-in-a-gpo-approver.md)

-   [<span data-ttu-id="db159-110">Bereitstellen eines Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="db159-110">Deploy a GPO</span></span>](deploy-a-gpo.md)

-   [<span data-ttu-id="db159-111">Zurücksetzen auf eine frühere Version eines Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="db159-111">Roll Back to a Previous Version of a GPO</span></span>](roll-back-to-a-previous-version-of-a-gpo.md)

-   [<span data-ttu-id="db159-112">Löschen, Wiederherstellen oder Zerstören eines Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="db159-112">Deleting, Restoring, or Destroying a GPO</span></span>](deleting-restoring-or-destroying-a-gpo.md)

<span data-ttu-id="db159-113">**Hinweis**  Da die genehmigende Rolle die Berechtigungen für die Rolle Prüfer umfasst, kann eine genehmigende Person auch Einstellungen überprüfen und GPOs vergleichen.</span><span class="sxs-lookup"><span data-stu-id="db159-113">**Note** Because the Approver role includes the permissions for the Reviewer role, an Approver can also review settings and compare GPOs.</span></span> <span data-ttu-id="db159-114">Weitere Informationen finden Sie unter [Ausführen von Aufgaben für Bearbeiter](performing-reviewer-tasks.md) .</span><span class="sxs-lookup"><span data-stu-id="db159-114">See [Performing Reviewer Tasks](performing-reviewer-tasks.md) for more information.</span></span>

 

### <span data-ttu-id="db159-115">Weitere Überlegungen</span><span class="sxs-lookup"><span data-stu-id="db159-115">Additional considerations</span></span>

<span data-ttu-id="db159-116">Standardmäßig werden die folgenden Berechtigungen für die genehmigende Rolle bereitgestellt:</span><span class="sxs-lookup"><span data-stu-id="db159-116">By default, the following permissions are provided for the Approver role:</span></span>

-   <span data-ttu-id="db159-117">Listeninhalt</span><span class="sxs-lookup"><span data-stu-id="db159-117">List Contents</span></span>

-   <span data-ttu-id="db159-118">Leseeinstellungen</span><span class="sxs-lookup"><span data-stu-id="db159-118">Read Settings</span></span>

-   <span data-ttu-id="db159-119">Erstellen eines GPO</span><span class="sxs-lookup"><span data-stu-id="db159-119">Create GPO</span></span>

-   <span data-ttu-id="db159-120">Bereitstellen von Gruppenrichtlinienobjekten</span><span class="sxs-lookup"><span data-stu-id="db159-120">Deploy GPO</span></span>

-   <span data-ttu-id="db159-121">Gruppenrichtlinienobjekt löschen</span><span class="sxs-lookup"><span data-stu-id="db159-121">Delete GPO</span></span>

<span data-ttu-id="db159-122">Darüber hinaus hat eine genehmigende Person die vollständige Kontrolle über die von ihm erstellten oder kontrollierten GPOs.</span><span class="sxs-lookup"><span data-stu-id="db159-122">Also, an Approver has full control over GPOs that he created or controlled.</span></span>

 

 





