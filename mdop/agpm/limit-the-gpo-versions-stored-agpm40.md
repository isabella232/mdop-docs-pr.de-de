---
title: Beschränken der gespeicherten GPO-Versionen
description: Beschränken der gespeicherten GPO-Versionen
author: dansimp
ms.assetid: d802c7b6-f303-4b23-aefd-f19f1300b0ff
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: df6f6df2e2b1bae2cd972b67b76c27905622a723
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808379"
---
# <span data-ttu-id="9f9de-103">Beschränken der gespeicherten GPO-Versionen</span><span class="sxs-lookup"><span data-stu-id="9f9de-103">Limit the GPO Versions Stored</span></span>


<span data-ttu-id="9f9de-104">Standardmäßig werden alle Versionen der einzelnen gesteuerten Gruppenrichtlinienobjekte im Archiv auf dem AGPM-Server aufbewahrt.</span><span class="sxs-lookup"><span data-stu-id="9f9de-104">By default, all versions of every controlled Group Policy Object (GPO) are retained in the archive on the AGPM Server.</span></span> <span data-ttu-id="9f9de-105">Allerdings können Sie die Anzahl der Versionen beschränken, die für jedes GPO aufbewahrt werden, und ältere Versionen löschen, wenn diese Grenze überschritten wird.</span><span class="sxs-lookup"><span data-stu-id="9f9de-105">However, you can limit the number of versions retained for each GPO and delete older versions when that limit is exceeded.</span></span> <span data-ttu-id="9f9de-106">Wenn GPO-Versionen gelöscht werden, verbleibt ein Datensatz der Version im Verlauf des Gruppenrichtlinienobjekts, aber die GPO-Version selbst wird aus dem Archiv gelöscht.</span><span class="sxs-lookup"><span data-stu-id="9f9de-106">When GPO versions are deleted, a record of the version remains in the history of the GPO, but the GPO version itself is deleted from the archive.</span></span>

<span data-ttu-id="9f9de-107">Zum Ausführen dieses Verfahrens ist ein Benutzerkonto mit der Rolle AGPM-Administrator (Vollzugriff) oder den erforderlichen Berechtigungen in Advanced Group Policy Management (AGPM) erforderlich.</span><span class="sxs-lookup"><span data-stu-id="9f9de-107">A user account with the AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span> <span data-ttu-id="9f9de-108">Lesen Sie die Details unter "Weitere Überlegungen" in diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="9f9de-108">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="9f9de-109">So begrenzen Sie die Anzahl der gespeicherten GPO-Versionen</span><span class="sxs-lookup"><span data-stu-id="9f9de-109">To limit the number of GPO versions stored</span></span>**

1.  <span data-ttu-id="9f9de-110">Klicken Sie in der Struktur der **Gruppenrichtlinien-Verwaltungskonsole** in der Gesamtstruktur und Domäne, in der Sie GPOs verwalten möchten, auf **Steuerelement ändern** .</span><span class="sxs-lookup"><span data-stu-id="9f9de-110">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="9f9de-111">Klicken Sie im Detailbereich auf die Registerkarte **AGPM-Server** .</span><span class="sxs-lookup"><span data-stu-id="9f9de-111">In the details pane, click the **AGPM Server** tab.</span></span>

3.  <span data-ttu-id="9f9de-112">Aktivieren Sie das Kontrollkästchen **alte Versionen jedes GPO aus dem Archiv löschen** , und geben Sie die maximale Anzahl von Gruppenrichtlinienobjekten ein, die für die einzelnen Gruppenrichtlinienobjekte gespeichert werden sollen, und nicht die aktuelle Version.</span><span class="sxs-lookup"><span data-stu-id="9f9de-112">Select the **Delete old versions of each GPO from the archive** check box, and type the maximum number of GPO versions to store for each GPO, not including the current version.</span></span> <span data-ttu-id="9f9de-113">Wenn Sie nur die aktuelle Version beibehalten möchten, geben Sie 0 ein.</span><span class="sxs-lookup"><span data-stu-id="9f9de-113">To retain only the current version, enter 0.</span></span> <span data-ttu-id="9f9de-114">Der Höchstwert darf nicht größer als 999 sein.</span><span class="sxs-lookup"><span data-stu-id="9f9de-114">The maximum must be no greater than 999.</span></span>

    <span data-ttu-id="9f9de-115">**Wichtig**  Nur auf der Registerkarte " **eindeutige Versionen** " des **Verlaufs** Fensters werden nur die Gruppenrichtlinienobjekte angezeigt, die auf die Grenze begrenzt sind.</span><span class="sxs-lookup"><span data-stu-id="9f9de-115">**Important** Only GPO versions displayed on the **Unique Versions** tab of the **History** window count toward the limit.</span></span>

     

4.  <span data-ttu-id="9f9de-116">Klicken Sie auf die Schaltfläche über **nehmen** .</span><span class="sxs-lookup"><span data-stu-id="9f9de-116">Click the **Apply** button.</span></span>

### <span data-ttu-id="9f9de-117">Weitere Überlegungen</span><span class="sxs-lookup"><span data-stu-id="9f9de-117">Additional considerations</span></span>

-   <span data-ttu-id="9f9de-118">Standardmäßig müssen Sie ein AGPM-Administrator (Vollzugriff) sein, um dieses Verfahren ausführen zu können.</span><span class="sxs-lookup"><span data-stu-id="9f9de-118">By default, you must be an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="9f9de-119">Insbesondere müssen Sie über die Berechtigungen **Listeninhalt** und **Änderungsoptionen** für die Domäne verfügen.</span><span class="sxs-lookup"><span data-stu-id="9f9de-119">Specifically, you must have **List Contents** and **Modify Options** permissions for the domain.</span></span>

-   <span data-ttu-id="9f9de-120">Sie können verhindern, dass eine GPO-Version gelöscht wird, indem Sie Sie im Verlauf als nicht löschbar kennzeichnen.</span><span class="sxs-lookup"><span data-stu-id="9f9de-120">You can prevent a GPO version from being deleted by marking it in the history as ineligible for deletion.</span></span> <span data-ttu-id="9f9de-121">Klicken Sie dazu mit der rechten Maustaste auf die Version im Verlauf des Gruppenrichtlinienobjekts, und klicken Sie auf **nicht löschen**.</span><span class="sxs-lookup"><span data-stu-id="9f9de-121">To do so, right-click the version in the history of the GPO and click **Do Not Delete**.</span></span>

### <span data-ttu-id="9f9de-122">Weitere Verweise</span><span class="sxs-lookup"><span data-stu-id="9f9de-122">Additional references</span></span>

-   [<span data-ttu-id="9f9de-123">Verwalten des Archivs</span><span class="sxs-lookup"><span data-stu-id="9f9de-123">Managing the Archive</span></span>](managing-the-archive-agpm40.md)

 

 





