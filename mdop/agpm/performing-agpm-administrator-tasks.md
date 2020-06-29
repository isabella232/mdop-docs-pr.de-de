---
title: Durchführen von AGPM-Administratoraufgaben
description: Durchführen von AGPM-Administratoraufgaben
author: dansimp
ms.assetid: 32e694a7-be64-4943-bce2-2a3a15e5341f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0daa8df93a88ed155e9f894011d4dd835761948b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808323"
---
# <span data-ttu-id="921da-103">Durchführen von AGPM-Administratoraufgaben</span><span class="sxs-lookup"><span data-stu-id="921da-103">Performing AGPM Administrator Tasks</span></span>


<span data-ttu-id="921da-104">Ein AGPM-Administrator (Vollzugriff) konfiguriert domänenweite Optionen und delegiert Berechtigungen für genehmigende Personen, Bearbeiter, Prüfer und andere AGPM-Administratoren.</span><span class="sxs-lookup"><span data-stu-id="921da-104">An AGPM Administrator (Full Control) configures domain-wide options and delegates permissions to Approvers, Editors, Reviewers, and other AGPM Administrators.</span></span> <span data-ttu-id="921da-105">Standardmäßig handelt es sich bei einem AGPM-Administrator um eine Person mit Vollzugriff (alle erweiterten Gruppenrichtlinienverwaltung \ [AGPM \]-Berechtigungen), und Sie können daher auch Aufgaben ausführen, die mit einer Rolle verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="921da-105">By default, an AGPM Administrator is an individual with Full Control (all Advanced Group Policy Management \[AGPM\] permissions) and therefore can also perform tasks associated with any role.</span></span>

<span data-ttu-id="921da-106">In einer Umgebung, in der mehrere Personengruppen Richtlinienobjekte (Group Policy Objects, GPOs) entwickeln, können Sie auswählen, ob alle Benutzer der erweiterten Gruppenrichtlinienverwaltung (Group Policy Management, AGPM) dieselben Aufgaben ausführen und über die gleiche Zugriffsebene verfügen oder ob AGPM-Administratoren Berechtigungen für Bearbeiter delegieren, die Änderungen an GPOs vornehmen, und Genehmigern, die GPOs in der Produktionsumgebung bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="921da-106">In an environment in which multiple people develop Group Policy objects (GPOs), you can choose whether all Advanced Group Policy Management (AGPM) users perform the same tasks and have the same level of access or whether AGPM Administrators delegate permissions to Editors who make changes to GPOs and to Approvers who deploy GPOs to the production environment.</span></span> <span data-ttu-id="921da-107">AGPM-Administratoren können Berechtigungen so konfigurieren, dass Sie den Anforderungen Ihrer Organisation entsprechen.</span><span class="sxs-lookup"><span data-stu-id="921da-107">AGPM Administrators can configure permissions to meet the needs of your organization.</span></span>

-   [<span data-ttu-id="921da-108">Konfigurieren der AGPM-Server-Verbindung</span><span class="sxs-lookup"><span data-stu-id="921da-108">Configure the AGPM Server Connection</span></span>](configure-the-agpm-server-connection.md)

-   [<span data-ttu-id="921da-109">Konfigurieren von E-Mail-Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="921da-109">Configure E-Mail Notification</span></span>](configure-e-mail-notification.md)

-   [<span data-ttu-id="921da-110">Delegieren des Domänenebenenzugriffs</span><span class="sxs-lookup"><span data-stu-id="921da-110">Delegate Domain-Level Access</span></span>](delegate-domain-level-access.md)

-   [<span data-ttu-id="921da-111">Delegieren des Zugriffs auf eine einzelne Gruppenrichtlinienobjekte</span><span class="sxs-lookup"><span data-stu-id="921da-111">Delegate Access to an Individual GPO</span></span>](delegate-access-to-an-individual-gpo.md)

-   [<span data-ttu-id="921da-112">Konfigurieren von Protokollierung und Ablaufverfolgung</span><span class="sxs-lookup"><span data-stu-id="921da-112">Configure Logging and Tracing</span></span>](configure-logging-and-tracing.md)

-   [<span data-ttu-id="921da-113">Verwalten des AGPM-Dienstes</span><span class="sxs-lookup"><span data-stu-id="921da-113">Managing the AGPM Service</span></span>](managing-the-agpm-service.md)

    -   [<span data-ttu-id="921da-114">Starten und Beenden des AGPM-Diensts</span><span class="sxs-lookup"><span data-stu-id="921da-114">Start and Stop the AGPM Service</span></span>](start-and-stop-the-agpm-service.md)

    -   [<span data-ttu-id="921da-115">Ändern des Archivpfads</span><span class="sxs-lookup"><span data-stu-id="921da-115">Modify the Archive Path</span></span>](modify-the-archive-path.md)

    -   [<span data-ttu-id="921da-116">Ändern des AGPM-Dienstkontos</span><span class="sxs-lookup"><span data-stu-id="921da-116">Modify the AGPM Service Account</span></span>](modify-the-agpm-service-account.md)

    -   [<span data-ttu-id="921da-117">Ändern Sie den Port, den der AGPM-Dienst überwacht</span><span class="sxs-lookup"><span data-stu-id="921da-117">Modify the Port on Which the AGPM Service Listens</span></span>](modify-the-port-on-which-the-agpm-service-listens.md)

<span data-ttu-id="921da-118">Da die Rolle des AGPM-Administrators auch die Berechtigungen für alle anderen Rollen umfasst, kann ein AGPM-Administrator die Aufgaben ausführen, die normalerweise mit einer anderen Rolle verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="921da-118">Also, because the AGPM Administrator role includes the permissions for all other roles, an AGPM Administrator can perform the tasks normally associated with any other role.</span></span>

-   <span data-ttu-id="921da-119">[Durchführen von genehmigenden Aufgaben](performing-approver-tasks.md)wie erstellen, bereitstellen oder Löschen von GPOs</span><span class="sxs-lookup"><span data-stu-id="921da-119">[Performing Approver Tasks](performing-approver-tasks.md), such as creating, deploying, or deleting GPOs</span></span>

-   <span data-ttu-id="921da-120">[Durchführen von Editor Aufgaben](performing-editor-tasks.md)wie bearbeiten, umbenennen, kennzeichnen oder Importieren von GPOs, Erstellen von Vorlagen oder Festlegen einer Standardvorlage</span><span class="sxs-lookup"><span data-stu-id="921da-120">[Performing Editor Tasks](performing-editor-tasks.md), such as editing, renaming, labeling, or importing GPOs, creating templates, or setting a default template</span></span>

-   <span data-ttu-id="921da-121">[Ausführen von Aufgaben mit Bearbeiter](performing-reviewer-tasks.md), wie das Überprüfen von Einstellungen und Vergleichen von GPOs</span><span class="sxs-lookup"><span data-stu-id="921da-121">[Performing Reviewer Tasks](performing-reviewer-tasks.md), such as reviewing settings and comparing GPOs</span></span>

### <span data-ttu-id="921da-122">Weitere Überlegungen</span><span class="sxs-lookup"><span data-stu-id="921da-122">Additional considerations</span></span>

<span data-ttu-id="921da-123">Standardmäßig verfügt die AGPM-Administrator Rolle über Vollzugriff – alle AGPM-Berechtigungen:</span><span class="sxs-lookup"><span data-stu-id="921da-123">By default, the AGPM Administrator role has Full Control—all AGPM permissions:</span></span>

-   <span data-ttu-id="921da-124">Listeninhalt</span><span class="sxs-lookup"><span data-stu-id="921da-124">List Contents</span></span>

-   <span data-ttu-id="921da-125">Leseeinstellungen</span><span class="sxs-lookup"><span data-stu-id="921da-125">Read Settings</span></span>

-   <span data-ttu-id="921da-126">Bearbeiten von Einstellungen</span><span class="sxs-lookup"><span data-stu-id="921da-126">Edit Settings</span></span>

-   <span data-ttu-id="921da-127">Erstellen eines GPO</span><span class="sxs-lookup"><span data-stu-id="921da-127">Create GPO</span></span>

-   <span data-ttu-id="921da-128">Bereitstellen von Gruppenrichtlinienobjekten</span><span class="sxs-lookup"><span data-stu-id="921da-128">Deploy GPO</span></span>

-   <span data-ttu-id="921da-129">Gruppenrichtlinienobjekt löschen</span><span class="sxs-lookup"><span data-stu-id="921da-129">Delete GPO</span></span>

-   <span data-ttu-id="921da-130">Optionen ändern</span><span class="sxs-lookup"><span data-stu-id="921da-130">Modify Options</span></span>

-   <span data-ttu-id="921da-131">Ändern der Sicherheit</span><span class="sxs-lookup"><span data-stu-id="921da-131">Modify Security</span></span>

-   <span data-ttu-id="921da-132">Erstellen einer Vorlage</span><span class="sxs-lookup"><span data-stu-id="921da-132">Create Template</span></span>

<span data-ttu-id="921da-133">Die Berechtigungen zum **ändern** und **Ändern der Sicherheit** sind eindeutig für die Rolle des AGPM-Administrators.</span><span class="sxs-lookup"><span data-stu-id="921da-133">The **Modify Options** and **Modify Security** permissions are unique to the role of AGPM Administrator.</span></span>

 

 





