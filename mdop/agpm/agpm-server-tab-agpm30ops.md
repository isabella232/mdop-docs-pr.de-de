---
title: Registerkarte „AGPM-Server“
description: Registerkarte „AGPM-Server“
author: dansimp
ms.assetid: fb3b0265-53ed-4bf6-88a4-c409f5f1bed4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 335cad07691f914884583636cef01be8dbaa0266
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807847"
---
# <span data-ttu-id="8dcf0-103">Registerkarte „AGPM-Server“</span><span class="sxs-lookup"><span data-stu-id="8dcf0-103">AGPM Server Tab</span></span>


<span data-ttu-id="8dcf0-104">Auf der Registerkarte **AGPM Server** im Bereich **Änderungssteuerung** können Sie einen AGPM-Server auswählen, indem Sie einen vollqualifizierten Computernamen und-Port eingeben und ältere Versionen von Gruppenrichtlinienobjekten (Group Policy Objects, GPOs) aus dem Archiv löschen, um Speicherplatz auf dem AGPM-Server zu sparen.</span><span class="sxs-lookup"><span data-stu-id="8dcf0-104">The **AGPM Server** tab on the **Change Control** pane enables you to select an AGPM Server by entering a fully-qualified computer name and port, and to delete older versions of Group Policy Objects (GPOs) from the archive to conserve disk space on the AGPM Server.</span></span>

## <span data-ttu-id="8dcf0-105">Angeben des AGPM-Servers</span><span class="sxs-lookup"><span data-stu-id="8dcf0-105">Specifying the AGPM Server</span></span>


<span data-ttu-id="8dcf0-106">Der ausgewählte AGPM-Server bestimmt, welches Archiv auf der Registerkarte **Inhalt** angezeigt wird und an welchen Speicherort die Einstellungen für die **Domänendelegierung** angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="8dcf0-106">The AGPM Server selected determines which archive is displayed for you on the **Contents** tab and to which location the **Domain Delegation** settings are applied.</span></span> <span data-ttu-id="8dcf0-107">Der Standardport für Advanced Group Policy Management (AGPM) ist Port 4600.</span><span class="sxs-lookup"><span data-stu-id="8dcf0-107">The default port for Advanced Group Policy Management (AGPM) is port 4600.</span></span>

<span data-ttu-id="8dcf0-108">Wenn die AGPM-Server Verbindung zentral mithilfe von Einstellungen für administrative Vorlagen konfiguriert ist, sind die Optionen auf dieser Registerkarte zum Konfigurieren der Verbindung nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="8dcf0-108">If the AGPM Server connection is centrally configured using Administrative template settings, the options on this tab for configuring the connection are unavailable.</span></span> <span data-ttu-id="8dcf0-109">Weitere Informationen finden Sie unter [Konfigurieren von AGPM-Server Verbindungen](configure-agpm-server-connections-agpm30ops.md).</span><span class="sxs-lookup"><span data-stu-id="8dcf0-109">For more information, see [Configure AGPM Server Connections](configure-agpm-server-connections-agpm30ops.md).</span></span>

## <span data-ttu-id="8dcf0-110">Löschen alter GPO-Versionen</span><span class="sxs-lookup"><span data-stu-id="8dcf0-110">Deleting old GPO versions</span></span>


<span data-ttu-id="8dcf0-111">Standardmäßig werden alle Versionen jedes kontrollierten Gruppenrichtlinienobjekts im Archiv aufbewahrt.</span><span class="sxs-lookup"><span data-stu-id="8dcf0-111">By default, all versions of every controlled GPO are retained in the archive.</span></span> <span data-ttu-id="8dcf0-112">Sie können den AGPM-Dienst jedoch so konfigurieren, dass die Anzahl der für die einzelnen Gruppenrichtlinienobjekte aufbewahrten Versionen eingeschränkt wird, und die älteste Version wird automatisch gelöscht, wenn diese Grenze überschritten wird.</span><span class="sxs-lookup"><span data-stu-id="8dcf0-112">However, you can configure the AGPM Service to limit the number of versions retained for each GPO and automatically delete the oldest version when that limit is exceeded.</span></span> <span data-ttu-id="8dcf0-113">Nur auf der Registerkarte " **eindeutige Versionen** " des **Verlaufs** Fensters werden nur die Gruppenrichtlinienobjekte angezeigt, die auf die Grenze begrenzt sind.</span><span class="sxs-lookup"><span data-stu-id="8dcf0-113">Only GPO versions displayed on the **Unique Versions** tab of the **History** window count toward the limit.</span></span>

<span data-ttu-id="8dcf0-114">**Hinweis**  Die maximale Anzahl von eindeutigen Versionen, die für jedes GPO gespeichert werden, enthält nicht die aktuelle Version, sodass die Eingabe von 0 nur die aktuelle Version aufrecht erhält.</span><span class="sxs-lookup"><span data-stu-id="8dcf0-114">**Note** The maximum number of unique versions to store for each GPO does not include the current version, so entering 0 retains only the current version.</span></span> <span data-ttu-id="8dcf0-115">Der Grenzwert darf nicht größer als 999-Versionen sein.</span><span class="sxs-lookup"><span data-stu-id="8dcf0-115">The limit must be no greater than 999 versions.</span></span>

<span data-ttu-id="8dcf0-116">Wenn eine GPO-Version gelöscht wird, verbleibt ein Datensatz dieser Version im Verlauf des Gruppenrichtlinienobjekts, aber die GPO-Version selbst wird aus dem Archiv gelöscht.</span><span class="sxs-lookup"><span data-stu-id="8dcf0-116">When a GPO version is deleted, a record of that version remains in the history of the GPO, but the GPO version itself is deleted from the archive.</span></span> <span data-ttu-id="8dcf0-117">Sie können verhindern, dass eine GPO-Version gelöscht wird, indem Sie Sie im Protokoll als nicht löschbar kennzeichnen.</span><span class="sxs-lookup"><span data-stu-id="8dcf0-117">You can prevent a GPO version from being deleted by marking it in the history as not deletable.</span></span>

 

### <span data-ttu-id="8dcf0-118">Weitere Verweise</span><span class="sxs-lookup"><span data-stu-id="8dcf0-118">Additional references</span></span>

-   [<span data-ttu-id="8dcf0-119">Benutzeroberfläche: Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="8dcf0-119">User Interface: Advanced Group Policy Management</span></span>](user-interface-advanced-group-policy-management-agpm30ops.md)

-   [<span data-ttu-id="8dcf0-120">Durchführen von AGPM-Administratoraufgaben</span><span class="sxs-lookup"><span data-stu-id="8dcf0-120">Performing AGPM Administrator Tasks</span></span>](performing-agpm-administrator-tasks-agpm30ops.md)

-   [<span data-ttu-id="8dcf0-121">Durchführen von Prüferaufgaben</span><span class="sxs-lookup"><span data-stu-id="8dcf0-121">Performing Reviewer Tasks</span></span>](performing-reviewer-tasks-agpm30ops.md)

 

 





