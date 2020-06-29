---
title: Durchführen von AGPM-Administratoraufgaben
description: Durchführen von AGPM-Administratoraufgaben
author: dansimp
ms.assetid: bc746f39-bdc9-4e2a-bc48-c3c7905de098
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 609b5b8b27fe24ff93e86bea7113929b1e04984d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809343"
---
# <span data-ttu-id="9dcfc-103">Durchführen von AGPM-Administratoraufgaben</span><span class="sxs-lookup"><span data-stu-id="9dcfc-103">Performing AGPM Administrator Tasks</span></span>


<span data-ttu-id="9dcfc-104">Mit der erweiterten Gruppenrichtlinienverwaltung (AGPM) kann ein AGPM-Administrator (Vollzugriff) domänenweite Optionen konfigurieren und Berechtigungen für genehmigende Personen, Bearbeiter, Bearbeiter und AGPM-Administratoren delegieren.</span><span class="sxs-lookup"><span data-stu-id="9dcfc-104">Advanced Group Policy Management (AGPM) lets an AGPM Administrator (Full Control) configure domain-wide options and delegate permissions to Approvers, Editors, Reviewers, and AGPM Administrators.</span></span> <span data-ttu-id="9dcfc-105">Standardmäßig handelt es sich bei einem AGPM-Administrator um eine Person, die Vollzugriff hat – alle AGPM-Berechtigungen – und die daher Aufgaben ausführen kann, die mit einer Rolle verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="9dcfc-105">By default, an AGPM Administrator is someone who has Full Control— all AGPM permissions—and who therefore can perform tasks associated with any role.</span></span>

<span data-ttu-id="9dcfc-106">In einer Umgebung, in der mehrere Personengruppen Richtlinienobjekte (Group Policy Objects, GPOs) entwickeln, können Sie festlegen, dass alle Gruppenrichtlinienadministratoren dieselben Aufgaben ausführen und über die gleiche Zugriffsebene verfügen.</span><span class="sxs-lookup"><span data-stu-id="9dcfc-106">In an environment in which multiple people develop Group Policy Objects (GPOs), you can choose to let all Group Policy administrators perform the same tasks and have the same level of access.</span></span> <span data-ttu-id="9dcfc-107">Sie können aber auch festlegen, dass AGPM-Administratoren Berechtigungen für Editoren delegieren können, die Gruppenrichtlinienobjekte ändern und Genehmigern, die GPOs in der Produktionsumgebung bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="9dcfc-107">Or, you can choose to let AGPM Administrators delegate permissions to Editors who can change GPOs and to Approvers who deploy GPOs to the production environment.</span></span> <span data-ttu-id="9dcfc-108">AGPM-Administratoren können Berechtigungen so konfigurieren, dass Sie den Anforderungen Ihrer Organisation entsprechen.</span><span class="sxs-lookup"><span data-stu-id="9dcfc-108">AGPM Administrators can configure permissions to meet the needs of your organization.</span></span>

-   <span data-ttu-id="9dcfc-109">[Konfigurieren der erweiterten Gruppenrichtlinienverwaltung](configuring-advanced-group-policy-management-agpm40.md): Konfigurieren der AGPM-Server Verbindung und e-Mail-Benachrichtigung, Delegieren des Zugriffs auf GPOs in der Produktionsumgebung und Konfigurieren der Protokollierung und Ablaufverfolgung für die Problembehandlung.</span><span class="sxs-lookup"><span data-stu-id="9dcfc-109">[Configuring Advanced Group Policy Management](configuring-advanced-group-policy-management-agpm40.md): Configure the AGPM Server Connection and e-mail notification, delegate access to GPOs in the production environment, and configure logging and tracing for troubleshooting.</span></span>

-   <span data-ttu-id="9dcfc-110">[Verwalten des Archivs](managing-the-archive-agpm40.md): Delegieren des Zugriffs auf GPOs im Archiv, begrenzen der Anzahl der Versionen der einzelnen gespeicherten Gruppenrichtlinienobjekte, Importieren eines GPO aus einer anderen Domäne und sichern und Wiederherstellen des Archivs.</span><span class="sxs-lookup"><span data-stu-id="9dcfc-110">[Managing the Archive](managing-the-archive-agpm40.md): Delegate access to GPOs in the archive, limit the number of versions of each GPO stored, import a GPO from another domain, and back up and restore the archive.</span></span>

-   <span data-ttu-id="9dcfc-111">[Verwalten des AGPM-Diensts](managing-the-agpm-service-agpm40.md): beenden und starten Sie den AGPM-Dienst, oder ändern Sie den Archivierungspfad, das AGPM-Dienstkonto oder den Port, auf dem der AGPM-Dienst lauscht.</span><span class="sxs-lookup"><span data-stu-id="9dcfc-111">[Managing the AGPM Service](managing-the-agpm-service-agpm40.md): Stop and start the AGPM Service or change the archive path, the AGPM Service Account, or the port on which the AGPM Service listens.</span></span>

-   <span data-ttu-id="9dcfc-112">[Verschieben Sie den AGPM-Server und das Archiv](move-the-agpm-server-and-the-archive-agpm40.md): Verschieben Sie den AGPM-Dienst, das Archiv oder beides auf einen anderen Server.</span><span class="sxs-lookup"><span data-stu-id="9dcfc-112">[Move the AGPM Server and the Archive](move-the-agpm-server-and-the-archive-agpm40.md): Move the AGPM Service, the archive, or both to a different server.</span></span>

<span data-ttu-id="9dcfc-113">**Hinweis**  Da die Rolle AGPM-Administrator die Berechtigungen für alle anderen Rollen umfasst, kann ein AGPM-Administrator die Aufgaben ausführen, die normalerweise mit einer anderen Rolle verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="9dcfc-113">**Note** Because the AGPM Administrator role includes the permissions for all other roles, an AGPM Administrator can perform the tasks usually associated with any other role.</span></span>

<span data-ttu-id="9dcfc-114">[Durchführen von genehmigenden Aufgaben](performing-approver-tasks-agpm40.md)wie erstellen, bereitstellen oder Löschen von GPOs</span><span class="sxs-lookup"><span data-stu-id="9dcfc-114">[Performing Approver Tasks](performing-approver-tasks-agpm40.md), such as creating, deploying, or deleting GPOs</span></span>

<span data-ttu-id="9dcfc-115">[Durchführen von Editor Aufgaben](performing-editor-tasks-agpm40.md)wie bearbeiten, umbenennen, kennzeichnen oder Importieren von GPOs, Erstellen von Vorlagen oder Festlegen einer Standardvorlage</span><span class="sxs-lookup"><span data-stu-id="9dcfc-115">[Performing Editor Tasks](performing-editor-tasks-agpm40.md), such as editing, renaming, labeling, or importing GPOs, creating templates, or setting a default template</span></span>

<span data-ttu-id="9dcfc-116">[Ausführen von Aufgaben mit Bearbeiter](performing-reviewer-tasks-agpm40.md), wie das Überprüfen von Einstellungen und Vergleichen von GPOs</span><span class="sxs-lookup"><span data-stu-id="9dcfc-116">[Performing Reviewer Tasks](performing-reviewer-tasks-agpm40.md), such as reviewing settings and comparing GPOs</span></span>

 

### <span data-ttu-id="9dcfc-117">Weitere Überlegungen</span><span class="sxs-lookup"><span data-stu-id="9dcfc-117">Additional considerations</span></span>

<span data-ttu-id="9dcfc-118">Standardmäßig verfügt die AGPM-Administrator Rolle über Vollzugriff – alle AGPM-Berechtigungen:</span><span class="sxs-lookup"><span data-stu-id="9dcfc-118">By default, the AGPM Administrator role has Full Control—all AGPM permissions:</span></span>

-   <span data-ttu-id="9dcfc-119">Listeninhalt</span><span class="sxs-lookup"><span data-stu-id="9dcfc-119">List Contents</span></span>

-   <span data-ttu-id="9dcfc-120">Leseeinstellungen</span><span class="sxs-lookup"><span data-stu-id="9dcfc-120">Read Settings</span></span>

-   <span data-ttu-id="9dcfc-121">Bearbeiten von Einstellungen</span><span class="sxs-lookup"><span data-stu-id="9dcfc-121">Edit Settings</span></span>

-   <span data-ttu-id="9dcfc-122">Erstellen eines GPO</span><span class="sxs-lookup"><span data-stu-id="9dcfc-122">Create GPO</span></span>

-   <span data-ttu-id="9dcfc-123">Bereitstellen von Gruppenrichtlinienobjekten</span><span class="sxs-lookup"><span data-stu-id="9dcfc-123">Deploy GPO</span></span>

-   <span data-ttu-id="9dcfc-124">Gruppenrichtlinienobjekt löschen</span><span class="sxs-lookup"><span data-stu-id="9dcfc-124">Delete GPO</span></span>

-   <span data-ttu-id="9dcfc-125">Exportieren von Gruppenrichtlinienobjekten</span><span class="sxs-lookup"><span data-stu-id="9dcfc-125">Export GPO</span></span>

-   <span data-ttu-id="9dcfc-126">Importieren von Gruppenrichtlinienobjekten</span><span class="sxs-lookup"><span data-stu-id="9dcfc-126">Import GPO</span></span>

-   <span data-ttu-id="9dcfc-127">Erstellen einer Vorlage</span><span class="sxs-lookup"><span data-stu-id="9dcfc-127">Create Template</span></span>

-   <span data-ttu-id="9dcfc-128">Optionen ändern</span><span class="sxs-lookup"><span data-stu-id="9dcfc-128">Modify Options</span></span>

-   <span data-ttu-id="9dcfc-129">Ändern der Sicherheit</span><span class="sxs-lookup"><span data-stu-id="9dcfc-129">Modify Security</span></span>

<span data-ttu-id="9dcfc-130">Die Berechtigungen zum **ändern** und **Ändern der Sicherheit** sind eindeutig für die Rolle des AGPM-Administrators.</span><span class="sxs-lookup"><span data-stu-id="9dcfc-130">The **Modify Options** and **Modify Security** permissions are unique to the role of AGPM Administrator.</span></span>

 

 





