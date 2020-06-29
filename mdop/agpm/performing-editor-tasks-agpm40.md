---
title: Durchführen von Editor-Aufgaben
description: Durchführen von Editor-Aufgaben
author: dansimp
ms.assetid: 81976a01-2a95-4256-b703-9fb3c884ef34
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b8e23bb91d8762d19eed9ae817967ba5a57505a9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808295"
---
# <span data-ttu-id="67988-103">Durchführen von Editor-Aufgaben</span><span class="sxs-lookup"><span data-stu-id="67988-103">Performing Editor Tasks</span></span>


<span data-ttu-id="67988-104">In der erweiterten Gruppenrichtlinienverwaltung (Group Policy Management, AGPM) ist ein Editor eine Person, die von einem AGPM-Administrator (Vollzugriff) autorisiert wurde, Gruppenrichtlinienobjekte (Group Policy Objects, GPOs) zu ändern und GPO-Vorlagen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="67988-104">In Advanced Group Policy Management (AGPM), an Editor is a person authorized by an AGPM Administrator (Full Control) to change Group Policy Objects (GPOs) and create GPO templates.</span></span> <span data-ttu-id="67988-105">Darüber hinaus kann ein Editor anfordern, dass ein GPO erstellt, gelöscht oder wiederhergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="67988-105">Additionally, an Editor can request that a GPO be created, deleted, or restored.</span></span> <span data-ttu-id="67988-106">Eine genehmigende Person muss die Anforderung zur Implementierung genehmigen.</span><span class="sxs-lookup"><span data-stu-id="67988-106">An Approver must approve the request for it to be implemented.</span></span> <span data-ttu-id="67988-107">Ein Editor kann ein GPO in eine Datei exportieren, damit es in eine Domäne in einer anderen Gesamtstruktur kopiert werden kann, und ein Gruppenrichtlinienobjekt importieren, das aus einer anderen Domäne kopiert wurde.</span><span class="sxs-lookup"><span data-stu-id="67988-107">An Editor can export a GPO to a file so that it can be copied to a domain in another forest, and import a GPO that was copied from another domain.</span></span>

<span data-ttu-id="67988-108">**Wichtig**  Stellen Sie sicher, dass Sie eine Verbindung mit dem zentralen Archiv für GPOs herstellen.</span><span class="sxs-lookup"><span data-stu-id="67988-108">**Important** Make sure that you are connecting to the central archive for GPOs.</span></span> <span data-ttu-id="67988-109">Weitere Informationen finden Sie unter [Konfigurieren einer AGPM-Server Verbindung](configure-an-agpm-server-connection-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="67988-109">For more information, see [Configure an AGPM Server Connection](configure-an-agpm-server-connection-agpm40.md).</span></span>

 

-   [<span data-ttu-id="67988-110">Erstellen oder Steuern eines Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="67988-110">Creating or Controlling a GPO</span></span>](creating-or-controlling-a-gpo-agpm40-ed.md)

-   [<span data-ttu-id="67988-111">Bearbeiten eines Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="67988-111">Editing a GPO</span></span>](editing-a-gpo-agpm40.md)

-   [<span data-ttu-id="67988-112">Verwenden einer Testumgebung</span><span class="sxs-lookup"><span data-stu-id="67988-112">Using a Test Environment</span></span>](using-a-test-environment.md)

-   [<span data-ttu-id="67988-113">Anfordern der Bereitstellung eines Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="67988-113">Request Deployment of a GPO</span></span>](request-deployment-of-a-gpo-agpm40.md)

-   [<span data-ttu-id="67988-114">Erstellen einer Vorlage und Festlegen einer Standardvorlage</span><span class="sxs-lookup"><span data-stu-id="67988-114">Creating a Template and Setting a Default Template</span></span>](creating-a-template-and-setting-a-default-template-agpm40.md)

-   [<span data-ttu-id="67988-115">Löschen oder Wiederherstellen eines Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="67988-115">Deleting or Restoring a GPO</span></span>](deleting-or-restoring-a-gpo-agpm40.md)

<span data-ttu-id="67988-116">**Hinweis**  Da die Rolle des Editors die Berechtigungen für die Prüferrolle umfasst, kann ein Editor auch Einstellungen überprüfen und GPOs vergleichen.</span><span class="sxs-lookup"><span data-stu-id="67988-116">**Note** Because the Editor role includes the permissions for the Reviewer role, an Editor can also review settings and compare GPOs.</span></span> <span data-ttu-id="67988-117">Weitere Informationen finden Sie unter [Ausführen von Aufgaben für Bearbeiter](performing-reviewer-tasks-agpm40.md) .</span><span class="sxs-lookup"><span data-stu-id="67988-117">See [Performing Reviewer Tasks](performing-reviewer-tasks-agpm40.md) for more information.</span></span>

 

### <span data-ttu-id="67988-118">Weitere Überlegungen</span><span class="sxs-lookup"><span data-stu-id="67988-118">Additional considerations</span></span>

<span data-ttu-id="67988-119">Standardmäßig werden die folgenden Berechtigungen für die Editor-Rolle bereitgestellt:</span><span class="sxs-lookup"><span data-stu-id="67988-119">By default, the following permissions are provided for the Editor role:</span></span>

-   <span data-ttu-id="67988-120">Listeninhalt</span><span class="sxs-lookup"><span data-stu-id="67988-120">List Contents</span></span>

-   <span data-ttu-id="67988-121">Leseeinstellungen</span><span class="sxs-lookup"><span data-stu-id="67988-121">Read Settings</span></span>

-   <span data-ttu-id="67988-122">Bearbeiten von Einstellungen</span><span class="sxs-lookup"><span data-stu-id="67988-122">Edit Settings</span></span>

-   <span data-ttu-id="67988-123">Exportieren von Gruppenrichtlinienobjekten</span><span class="sxs-lookup"><span data-stu-id="67988-123">Export GPO</span></span>

-   <span data-ttu-id="67988-124">Importieren von Gruppenrichtlinienobjekten</span><span class="sxs-lookup"><span data-stu-id="67988-124">Import GPO</span></span>

-   <span data-ttu-id="67988-125">Erstellen einer Vorlage</span><span class="sxs-lookup"><span data-stu-id="67988-125">Create Template</span></span>

 

 





