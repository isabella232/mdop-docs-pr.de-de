---
title: Wiederherstellen des Archivs aus einer Sicherung
description: Wiederherstellen des Archivs aus einer Sicherung
author: dansimp
ms.assetid: b83f6173-a236-4da2-b16e-8df20920d4cc
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3a1b7039ad587cf9c8d7f914fe3b963e12ba8949
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807491"
---
# <span data-ttu-id="7dcc5-103">Wiederherstellen des Archivs aus einer Sicherung</span><span class="sxs-lookup"><span data-stu-id="7dcc5-103">Restore the Archive from a Backup</span></span>


<span data-ttu-id="7dcc5-104">Wenn ein Notfall auftritt und das Archiv für Advanced Group Policy Management (AGPM) beschädigt oder zerstört ist, kann ein AGPM-Administrator (Vollzugriff) das Archiv aus einer im Voraus vorbereiteten Sicherungskopie wiederherstellen und dann aus der Produktionsumgebung der Domäne alle Gruppenrichtlinienobjekte (Group Policy Objects, GPOs) importieren, die sich nicht im Archiv befinden oder für die die Version in der Produktion aktueller ist als im</span><span class="sxs-lookup"><span data-stu-id="7dcc5-104">If a disaster occurs and the archive for Advanced Group Policy Management (AGPM) is damaged or destroyed, an AGPM Administrator (Full Control) can restore the archive from a backup copy prepared in advance and then import from the production environment of the domain any Group Policy Objects (GPOs) that are not in the archive or for which the version in production is more current than that in the archive.</span></span> <span data-ttu-id="7dcc5-105">Informationen zum Wiederherstellen einer Archivsicherung auf einem anderen Server finden Sie unter [Verschieben des AGPM-Servers und des Archivs](move-the-agpm-server-and-the-archive-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="7dcc5-105">For information about how to restore an archive backup to a different server, see [Move the AGPM Server and the Archive](move-the-agpm-server-and-the-archive-agpm40.md).</span></span>

<span data-ttu-id="7dcc5-106">Ein Benutzerkonto, das Zugriff auf den AGPM-Server (den Computer, auf dem der AGPM-Dienst installiert ist) und den Ordner mit dem Archiv hat, ist erforderlich, um dieses Verfahren ausführen zu können.</span><span class="sxs-lookup"><span data-stu-id="7dcc5-106">A user account that has access to the AGPM Server (the computer on which the AGPM Service is installed) and to the folder that contains the archive is required to complete this procedure.</span></span>

**<span data-ttu-id="7dcc5-107">So stellen Sie das Archiv aus einer Sicherung wieder her</span><span class="sxs-lookup"><span data-stu-id="7dcc5-107">To restore the archive from a backup</span></span>**

1.  <span data-ttu-id="7dcc5-108">Beenden Sie den AGPM-Dienst.</span><span class="sxs-lookup"><span data-stu-id="7dcc5-108">Stop the AGPM Service.</span></span> <span data-ttu-id="7dcc5-109">Weitere Informationen finden Sie unter [starten und Beenden des AGPM-Diensts](start-and-stop-the-agpm-service-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="7dcc5-109">For more information, see [Start and Stop the AGPM Service](start-and-stop-the-agpm-service-agpm40.md).</span></span>

2.  <span data-ttu-id="7dcc5-110">Entfernen des vorhandenen Archivs</span><span class="sxs-lookup"><span data-stu-id="7dcc5-110">Remove the existing archive.</span></span> <span data-ttu-id="7dcc5-111">Standardmäßig ist der Archivordner%ProgramData%\\Microsoft\\AGPM, doch der AGPM-Administrator, der den Microsoft Advanced Group Policy Management-Server installiert hat, hat möglicherweise während des Setups einen anderen Speicherort eingegeben.</span><span class="sxs-lookup"><span data-stu-id="7dcc5-111">By default, the archive folder is %ProgramData%\\Microsoft\\AGPM, however the AGPM Administrator who installed Microsoft Advanced Group Policy Management - Server may have entered a different location during setup.</span></span>

3.  <span data-ttu-id="7dcc5-112">Erstellen Sie den Archivordner neu, indem Sie den Archivierungspfad, das AGPM-Dienstkonto, den Archiv Besitzer und den Abhör-Port konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="7dcc5-112">Re-create the archive folder by configuring the archive path, AGPM Service Account, Archive Owner, and listening port.</span></span> <span data-ttu-id="7dcc5-113">Es ist nicht erforderlich, dieselben Werte wie bei der ursprünglichen Installation zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="7dcc5-113">Using the same values as used during the original installation is not necessary.</span></span> <span data-ttu-id="7dcc5-114">Weitere Informationen finden Sie unter [Ändern des AGPM-Diensts](modify-the-agpm-service-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="7dcc5-114">For more information, see [Modify the AGPM Service](modify-the-agpm-service-agpm40.md).</span></span>

4.  <span data-ttu-id="7dcc5-115">Kopieren Sie den Inhalt der Archivsicherung in den Archivordner, kopieren Sie die Unterordner und Dateien, um sicherzustellen, dass jeder Unterordner und jede Datei die Berechtigungen des Archivordners erbt.</span><span class="sxs-lookup"><span data-stu-id="7dcc5-115">Copy the contents of the archive backup to the archive folder, copying the subfolders and files to make sure that each subfolder and file inherits the permissions of the archive folder.</span></span> <span data-ttu-id="7dcc5-116">Achten Sie darauf, den Archivordner nicht zu überschreiben.</span><span class="sxs-lookup"><span data-stu-id="7dcc5-116">Be careful not to overwrite the archive folder.</span></span>

5.  <span data-ttu-id="7dcc5-117">Wenn Sie nicht sicher sind, ob ein GPO in der Archivsicherung aktueller als die Kopie dieses Gruppenrichtlinienobjekts in der Produktion ist, erstellen Sie einen Unterschiedsbericht, und vergleichen Sie deren Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="7dcc5-117">If you not sure about whether a GPO in the archive backup is more current than the copy of that GPO in production, generate a difference report and compare their settings.</span></span> <span data-ttu-id="7dcc5-118">Weitere Informationen finden Sie unter [Identifizieren von Unterschieden zwischen GPOs, GPO-Versionen oder Vorlagen](identify-differences-between-gpos-gpo-versions-or-templates-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="7dcc5-118">For more information, see [Identify Differences Between GPOs, GPO Versions, or Templates](identify-differences-between-gpos-gpo-versions-or-templates-agpm40.md).</span></span>

6.  <span data-ttu-id="7dcc5-119">Starten Sie den AGPM-Dienst erneut.</span><span class="sxs-lookup"><span data-stu-id="7dcc5-119">Restart the AGPM Service.</span></span> <span data-ttu-id="7dcc5-120">Weitere Informationen finden Sie unter [starten und Beenden des AGPM-Diensts](start-and-stop-the-agpm-service-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="7dcc5-120">For more information, see [Start and Stop the AGPM Service](start-and-stop-the-agpm-service-agpm40.md).</span></span>

### <span data-ttu-id="7dcc5-121">Weitere Verweise</span><span class="sxs-lookup"><span data-stu-id="7dcc5-121">Additional references</span></span>

-   [<span data-ttu-id="7dcc5-122">Sichern des Archivs</span><span class="sxs-lookup"><span data-stu-id="7dcc5-122">Back Up the Archive</span></span>](back-up-the-archive-agpm40.md)

-   [<span data-ttu-id="7dcc5-123">Verschieben des AGPM-Servers und -Archivs</span><span class="sxs-lookup"><span data-stu-id="7dcc5-123">Move the AGPM Server and the Archive</span></span>](move-the-agpm-server-and-the-archive-agpm40.md)

-   [<span data-ttu-id="7dcc5-124">Verwalten des Archivs</span><span class="sxs-lookup"><span data-stu-id="7dcc5-124">Managing the Archive</span></span>](managing-the-archive-agpm40.md)

 

 





