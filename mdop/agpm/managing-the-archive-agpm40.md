---
title: Verwalten des Archivs
description: Verwalten des Archivs
author: dansimp
ms.assetid: b11a3d71-74ea-4dd7-b243-6f2880b7af2d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 682d720b4095dbfa6a7cc4d868109f57c4f54641
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808355"
---
# <span data-ttu-id="76766-103">Verwalten des Archivs</span><span class="sxs-lookup"><span data-stu-id="76766-103">Managing the Archive</span></span>


<span data-ttu-id="76766-104">In Advanced Group Policy Management (AGPM) können Sie als AGPM-Administrator (Vollzugriff) den Zugriff auf das Archiv verwalten und die Anzahl der Versionen der einzelnen Gruppenrichtlinienobjekte begrenzen, die im Archiv gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="76766-104">In Advanced Group Policy Management (AGPM), as an AGPM Administrator (Full Control), you manage access to the archive and have the option to limit the number of versions of each Group Policy Object (GPO) stored in the archive.</span></span> <span data-ttu-id="76766-105">Sie können den Zugriff auf GPOs im Archiv auf Domänenebene oder auf GPO-Ebene delegieren.</span><span class="sxs-lookup"><span data-stu-id="76766-105">You can delegate access to GPOs in the archive at the domain level or GPO level.</span></span> <span data-ttu-id="76766-106">Darüber hinaus können Sie das Archiv sichern, damit Sie es möglicherweise wiederherstellen können, wenn ein Notfall eintritt.</span><span class="sxs-lookup"><span data-stu-id="76766-106">Additionally, you can back up the archive so that you may be able to recover it if a disaster occurs.</span></span>

<span data-ttu-id="76766-107">Als AGPM-Administrator können Sie ein GPO in eine Datei exportieren, die Datei in eine andere Gesamtstruktur kopieren und dann das Gruppenrichtlinienobjekt in eine Domäne in dieser Gesamtstruktur importieren.</span><span class="sxs-lookup"><span data-stu-id="76766-107">As an AGPM Administrator, you can export a GPO to a file, copy the file to another forest, and then import the GPO into a domain in that forest.</span></span> <span data-ttu-id="76766-108">Im Gegensatz zu einem Editor können Sie Richtlinieneinstellungen aus einer GPO-Sicherung direkt in ein neues gesteuertes GPO importieren, wenn Sie es erstellen.</span><span class="sxs-lookup"><span data-stu-id="76766-108">Unlike an Editor, you can import policy settings from a GPO backup directly into a new controlled GPO when you create it.</span></span> <span data-ttu-id="76766-109">Informationen zum Exportieren eines Gruppenrichtlinienobjekts finden Sie unter [Exportieren eines Gruppenrichtlinienobjekts in eine Datei](export-a-gpo-to-a-file.md).</span><span class="sxs-lookup"><span data-stu-id="76766-109">For information about how to export a GPO, see [Export a GPO to a File](export-a-gpo-to-a-file.md).</span></span>

-   [<span data-ttu-id="76766-110">Delegieren des Domänenebenenzugriffs auf das Archiv</span><span class="sxs-lookup"><span data-stu-id="76766-110">Delegate Domain-Level Access to the Archive</span></span>](delegate-domain-level-access-to-the-archive-agpm40.md)

-   [<span data-ttu-id="76766-111">Delegieren des Zugriffs auf ein einzelnes Gruppenrichtlinienobjekt im Archiv</span><span class="sxs-lookup"><span data-stu-id="76766-111">Delegate Access to an Individual GPO in the Archive</span></span>](delegate-access-to-an-individual-gpo-in-the-archive-agpm40.md)

-   [<span data-ttu-id="76766-112">Beschränken der gespeicherten GPO-Versionen</span><span class="sxs-lookup"><span data-stu-id="76766-112">Limit the GPO Versions Stored</span></span>](limit-the-gpo-versions-stored-agpm40.md)

-   [<span data-ttu-id="76766-113">Importieren eines Gruppenrichtlinienobjekts aus einer Datei</span><span class="sxs-lookup"><span data-stu-id="76766-113">Import a GPO from a File</span></span>](import-a-gpo-from-a-file-agpmadmin.md)

-   [<span data-ttu-id="76766-114">Sichern des Archivs</span><span class="sxs-lookup"><span data-stu-id="76766-114">Back Up the Archive</span></span>](back-up-the-archive-agpm40.md)

-   [<span data-ttu-id="76766-115">Wiederherstellen des Archivs aus einer Sicherung</span><span class="sxs-lookup"><span data-stu-id="76766-115">Restore the Archive from a Backup</span></span>](restore-the-archive-from-a-backup-agpm40.md)

### <span data-ttu-id="76766-116">Weitere Verweise</span><span class="sxs-lookup"><span data-stu-id="76766-116">Additional references</span></span>

-   <span data-ttu-id="76766-117">Informationen zum Delegieren des Zugriffs auf GPOs in der Produktionsumgebung finden Sie unter [Delegieren des Zugriffs auf die Produktionsumgebung](delegate-access-to-the-production-environment-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="76766-117">For information about how to delegate access to GPOs in the production environment, see [Delegate Access to the Production Environment](delegate-access-to-the-production-environment-agpm40.md).</span></span>

-   <span data-ttu-id="76766-118">Informationen zum Verschieben des Archivs finden Sie unter [Verschieben des AGPM-Servers und des Archivs](move-the-agpm-server-and-the-archive-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="76766-118">For information about how to move the archive, see [Move the AGPM Server and the Archive](move-the-agpm-server-and-the-archive-agpm40.md).</span></span>

-   [<span data-ttu-id="76766-119">Durchführen von AGPM-Administratoraufgaben</span><span class="sxs-lookup"><span data-stu-id="76766-119">Performing AGPM Administrator Tasks</span></span>](performing-agpm-administrator-tasks-agpm40.md)

 

 





