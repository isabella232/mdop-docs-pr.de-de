---
title: Durchführen der Aufgaben von genehmigenden Personen
description: Durchführen der Aufgaben von genehmigenden Personen
author: dansimp
ms.assetid: e0a4b7fe-ce69-4755-9104-c7f523ea6b62
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2a0815bdd6c34a7a23b27075b3b5367757c1f84e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808319"
---
# <span data-ttu-id="43252-103">Durchführen der Aufgaben von genehmigenden Personen</span><span class="sxs-lookup"><span data-stu-id="43252-103">Performing Approver Tasks</span></span>


<span data-ttu-id="43252-104">Eine genehmigende Person ist eine von einem AGPM-Administrator (Vollzugriff) autorisierte Person zum Erstellen, bereitstellen und Löschen von Gruppenrichtlinienobjekten (Group Policy Objects, GPOs) sowie zum genehmigen oder ablehnen von Anforderungen (in der Regel von Editoren) zum Erstellen, bereitstellen oder Löschen von GPOs.</span><span class="sxs-lookup"><span data-stu-id="43252-104">An Approver is a person authorized by an AGPM Administrator (Full Control) to create, deploy, and delete Group Policy Objects (GPOs) and to approve or reject requests (typically from Editors) to create, deploy, or delete GPOs.</span></span>

<span data-ttu-id="43252-105">**Wichtig**  Stellen Sie sicher, dass Sie eine Verbindung mit dem zentralen Archiv für GPOs herstellen.</span><span class="sxs-lookup"><span data-stu-id="43252-105">**Important** Make sure that you are connecting to the central archive for GPOs.</span></span> <span data-ttu-id="43252-106">Weitere Informationen finden Sie unter [Konfigurieren einer AGPM-Server Verbindung](configure-an-agpm-server-connection-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="43252-106">For more information, see [Configure an AGPM Server Connection](configure-an-agpm-server-connection-agpm40.md).</span></span>

 

-   [<span data-ttu-id="43252-107">Genehmigen oder Ablehnen einer ausstehenden Aktion</span><span class="sxs-lookup"><span data-stu-id="43252-107">Approve or Reject a Pending Action</span></span>](approve-or-reject-a-pending-action-agpm40.md)

-   [<span data-ttu-id="43252-108">Erstellen oder Steuern eines Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="43252-108">Creating or Controlling a GPO</span></span>](creating-or-controlling-a-gpo-agpm40-app.md)

-   [<span data-ttu-id="43252-109">Einchecken eines Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="43252-109">Check In a GPO</span></span>](check-in-a-gpo-agpm40.md)

-   [<span data-ttu-id="43252-110">Bereitstellen eines Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="43252-110">Deploy a GPO</span></span>](deploy-a-gpo-agpm40.md)

-   [<span data-ttu-id="43252-111">Zurücksetzen auf eine frühere Version eines Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="43252-111">Roll Back to an Earlier Version of a GPO</span></span>](roll-back-to-an-earlier-version-of-a-gpo-agpm40.md)

-   [<span data-ttu-id="43252-112">Löschen, Wiederherstellen oder Zerstören eines Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="43252-112">Deleting, Restoring, or Destroying a GPO</span></span>](deleting-restoring-or-destroying-a-gpo-agpm40.md)

<span data-ttu-id="43252-113">**Hinweis**  Bevor Sie ein GPO genehmigen, sollte eine genehmigende Person die darin enthaltenen Richtlinieneinstellungen überprüfen.</span><span class="sxs-lookup"><span data-stu-id="43252-113">**Note** Before approving a GPO, an Approver should review the policy settings that it contains.</span></span> <span data-ttu-id="43252-114">Die Rolle genehmigende Person umfasst die Berechtigungen für die Rolle Prüfer, damit eine genehmigende Person Richtlinieneinstellungen überprüfen und GPOs vergleichen kann.</span><span class="sxs-lookup"><span data-stu-id="43252-114">The Approver role includes the permissions for the Reviewer role, so that an Approver can review policy settings and compare GPOs.</span></span> <span data-ttu-id="43252-115">Weitere Informationen finden Sie unter [Ausführen von Aufgaben für Bearbeiter](performing-reviewer-tasks-agpm40.md) .</span><span class="sxs-lookup"><span data-stu-id="43252-115">See [Performing Reviewer Tasks](performing-reviewer-tasks-agpm40.md) for more information.</span></span>

 

### <span data-ttu-id="43252-116">Weitere Überlegungen</span><span class="sxs-lookup"><span data-stu-id="43252-116">Additional considerations</span></span>

<span data-ttu-id="43252-117">Standardmäßig werden die folgenden Berechtigungen für die genehmigende Rolle bereitgestellt:</span><span class="sxs-lookup"><span data-stu-id="43252-117">By default, the following permissions are provided for the Approver role:</span></span>

-   <span data-ttu-id="43252-118">Listeninhalt</span><span class="sxs-lookup"><span data-stu-id="43252-118">List Contents</span></span>

-   <span data-ttu-id="43252-119">Leseeinstellungen</span><span class="sxs-lookup"><span data-stu-id="43252-119">Read Settings</span></span>

-   <span data-ttu-id="43252-120">Erstellen eines GPO</span><span class="sxs-lookup"><span data-stu-id="43252-120">Create GPO</span></span>

-   <span data-ttu-id="43252-121">Bereitstellen von Gruppenrichtlinienobjekten</span><span class="sxs-lookup"><span data-stu-id="43252-121">Deploy GPO</span></span>

-   <span data-ttu-id="43252-122">Gruppenrichtlinienobjekt löschen</span><span class="sxs-lookup"><span data-stu-id="43252-122">Delete GPO</span></span>

<span data-ttu-id="43252-123">Darüber hinaus hat eine genehmigende Person die vollständige Kontrolle über die von ihm erstellten oder kontrollierten GPOs.</span><span class="sxs-lookup"><span data-stu-id="43252-123">Also, an Approver has full control over GPOs that he created or controlled.</span></span>

 

 





