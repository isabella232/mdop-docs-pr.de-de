---
title: Durchführen von AGPM-Administratoraufgaben
description: Durchführen von AGPM-Administratoraufgaben
author: dansimp
ms.assetid: 9678b0f4-70a5-411e-a896-afa4dc9ea6c4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 26b412e5b22e46af938d127751fdca1da722a8c6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809346"
---
# <span data-ttu-id="119b7-103">Durchführen von AGPM-Administratoraufgaben</span><span class="sxs-lookup"><span data-stu-id="119b7-103">Performing AGPM Administrator Tasks</span></span>


<span data-ttu-id="119b7-104">In Advanced Group Policy Management (AGPM) konfiguriert ein AGPM-Administrator (Vollzugriff) domänenweite Optionen und delegiert Berechtigungen für genehmigende Personen, Bearbeiter, Prüfer und andere AGPM-Administratoren.</span><span class="sxs-lookup"><span data-stu-id="119b7-104">In Advanced Group Policy Management (AGPM), an AGPM Administrator (Full Control) configures domain-wide options and delegates permissions to Approvers, Editors, Reviewers, and other AGPM Administrators.</span></span> <span data-ttu-id="119b7-105">Standardmäßig handelt es sich bei einem AGPM-Administrator um eine Person mit Vollzugriff (alle AGPM-Berechtigungen), die daher Aufgaben ausführen kann, die mit einer Rolle verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="119b7-105">By default, an AGPM Administrator is an individual with Full Control—all AGPM permissions—and who therefore can perform tasks associated with any role.</span></span>

<span data-ttu-id="119b7-106">In einer Umgebung, in der mehrere Personengruppen Richtlinienobjekte (Group Policy Objects, GPOs) entwickeln, können Sie auswählen, ob alle AGPM-Benutzer die gleichen Aufgaben ausführen und über die gleiche Zugriffsebene verfügen oder ob AGPM-Administratoren Berechtigungen für Editoren delegieren, die Änderungen an GPOs vornehmen, und Genehmigern, die GPOs in der Produktionsumgebung bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="119b7-106">In an environment in which multiple people develop Group Policy Objects (GPOs), you can choose whether all AGPM users perform the same tasks and have the same level of access or whether AGPM Administrators delegate permissions to Editors who make changes to GPOs and to Approvers who deploy GPOs to the production environment.</span></span> <span data-ttu-id="119b7-107">AGPM-Administratoren können Berechtigungen so konfigurieren, dass Sie den Anforderungen Ihrer Organisation entsprechen.</span><span class="sxs-lookup"><span data-stu-id="119b7-107">AGPM Administrators can configure permissions to meet the needs of your organization.</span></span>

-   <span data-ttu-id="119b7-108">[Konfigurieren der erweiterten Gruppenrichtlinienverwaltung](configuring-advanced-group-policy-management.md): Konfigurieren der AGPM-Server Verbindung und e-Mail-Benachrichtigung, Delegieren des Zugriffs auf GPOs in der Produktionsumgebung und Konfigurieren der Protokollierung und Ablaufverfolgung für die Problembehandlung.</span><span class="sxs-lookup"><span data-stu-id="119b7-108">[Configuring Advanced Group Policy Management](configuring-advanced-group-policy-management.md): Configure the AGPM Server Connection and e-mail notification, delegate access to GPOs in the production environment, and configure logging and tracing for troubleshooting.</span></span>

-   <span data-ttu-id="119b7-109">[Verwalten des Archivs](managing-the-archive.md): Delegieren des Zugriffs auf GPOs im Archiv und begrenzen der Anzahl der Versionen jedes gespeicherten Gruppenrichtlinienobjekts.</span><span class="sxs-lookup"><span data-stu-id="119b7-109">[Managing the Archive](managing-the-archive.md): Delegate access to GPOs in the archive and limit the number of versions of each GPO stored.</span></span>

-   <span data-ttu-id="119b7-110">[Verwalten des AGPM-Diensts](managing-the-agpm-service-agpm30ops.md): beenden und starten Sie den AGPM-Dienst, oder ändern Sie den Archivierungspfad, das AGPM-Dienstkonto oder den Port, auf dem der AGPM-Dienst lauscht.</span><span class="sxs-lookup"><span data-stu-id="119b7-110">[Managing the AGPM Service](managing-the-agpm-service-agpm30ops.md): Stop and start the AGPM Service or change the archive path, the AGPM Service Account, or the port on which the AGPM Service listens.</span></span>

-   <span data-ttu-id="119b7-111">[Verschieben Sie den AGPM-Server und das Archiv](move-the-agpm-server-and-the-archive.md): Verschieben Sie den AGPM-Dienst, das Archiv oder beides auf einen anderen Server.</span><span class="sxs-lookup"><span data-stu-id="119b7-111">[Move the AGPM Server and the Archive](move-the-agpm-server-and-the-archive.md): Move the AGPM Service, the archive, or both to a different server.</span></span>

<span data-ttu-id="119b7-112">Da die Rolle des AGPM-Administrators auch die Berechtigungen für alle anderen Rollen umfasst, kann ein AGPM-Administrator die Aufgaben ausführen, die normalerweise mit einer anderen Rolle verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="119b7-112">Also, because the AGPM Administrator role includes the permissions for all other roles, an AGPM Administrator can perform the tasks normally associated with any other role.</span></span>

-   <span data-ttu-id="119b7-113">[Durchführen von genehmigenden Aufgaben](performing-approver-tasks-agpm30ops.md)wie erstellen, bereitstellen oder Löschen von GPOs</span><span class="sxs-lookup"><span data-stu-id="119b7-113">[Performing Approver Tasks](performing-approver-tasks-agpm30ops.md), such as creating, deploying, or deleting GPOs</span></span>

-   <span data-ttu-id="119b7-114">[Durchführen von Editor Aufgaben](performing-editor-tasks-agpm30ops.md)wie bearbeiten, umbenennen, kennzeichnen oder Importieren von GPOs, Erstellen von Vorlagen oder Festlegen einer Standardvorlage</span><span class="sxs-lookup"><span data-stu-id="119b7-114">[Performing Editor Tasks](performing-editor-tasks-agpm30ops.md), such as editing, renaming, labeling, or importing GPOs, creating templates, or setting a default template</span></span>

-   <span data-ttu-id="119b7-115">[Ausführen von Aufgaben mit Bearbeiter](performing-reviewer-tasks-agpm30ops.md), wie das Überprüfen von Einstellungen und Vergleichen von GPOs</span><span class="sxs-lookup"><span data-stu-id="119b7-115">[Performing Reviewer Tasks](performing-reviewer-tasks-agpm30ops.md), such as reviewing settings and comparing GPOs</span></span>

### <span data-ttu-id="119b7-116">Weitere Überlegungen</span><span class="sxs-lookup"><span data-stu-id="119b7-116">Additional considerations</span></span>

<span data-ttu-id="119b7-117">Standardmäßig verfügt die AGPM-Administrator Rolle über Vollzugriff – alle AGPM-Berechtigungen:</span><span class="sxs-lookup"><span data-stu-id="119b7-117">By default, the AGPM Administrator role has Full Control—all AGPM permissions:</span></span>

-   <span data-ttu-id="119b7-118">Listeninhalt</span><span class="sxs-lookup"><span data-stu-id="119b7-118">List Contents</span></span>

-   <span data-ttu-id="119b7-119">Leseeinstellungen</span><span class="sxs-lookup"><span data-stu-id="119b7-119">Read Settings</span></span>

-   <span data-ttu-id="119b7-120">Bearbeiten von Einstellungen</span><span class="sxs-lookup"><span data-stu-id="119b7-120">Edit Settings</span></span>

-   <span data-ttu-id="119b7-121">Erstellen eines GPO</span><span class="sxs-lookup"><span data-stu-id="119b7-121">Create GPO</span></span>

-   <span data-ttu-id="119b7-122">Bereitstellen von Gruppenrichtlinienobjekten</span><span class="sxs-lookup"><span data-stu-id="119b7-122">Deploy GPO</span></span>

-   <span data-ttu-id="119b7-123">Gruppenrichtlinienobjekt löschen</span><span class="sxs-lookup"><span data-stu-id="119b7-123">Delete GPO</span></span>

-   <span data-ttu-id="119b7-124">Optionen ändern</span><span class="sxs-lookup"><span data-stu-id="119b7-124">Modify Options</span></span>

-   <span data-ttu-id="119b7-125">Ändern der Sicherheit</span><span class="sxs-lookup"><span data-stu-id="119b7-125">Modify Security</span></span>

-   <span data-ttu-id="119b7-126">Erstellen einer Vorlage</span><span class="sxs-lookup"><span data-stu-id="119b7-126">Create Template</span></span>

<span data-ttu-id="119b7-127">Die Berechtigungen zum **ändern** und **Ändern der Sicherheit** sind eindeutig für die Rolle des AGPM-Administrators.</span><span class="sxs-lookup"><span data-stu-id="119b7-127">The **Modify Options** and **Modify Security** permissions are unique to the role of AGPM Administrator.</span></span>

 

 





