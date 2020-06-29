---
title: Checkliste Verwalten des AGPM-Servers und des Archivs
description: Checkliste Verwalten des AGPM-Servers und des Archivs
author: dansimp
ms.assetid: 0b2eb536-c3cc-462f-a42f-27a53f57bc55
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f872a476a4a8ddd93546778c6278c175ec715850
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807792"
---
# <span data-ttu-id="c64ac-103">Prüfliste: Verwalten des AGPM-Servers und -Archivs</span><span class="sxs-lookup"><span data-stu-id="c64ac-103">Checklist: Administer the AGPM Server and Archive</span></span>


<span data-ttu-id="c64ac-104">In Advanced Group Policy Management (AGPM) werden sowohl der AGPM-Dienst als auch das Archiv von AGPM-Administratoren verwaltet (Vollzugriff).</span><span class="sxs-lookup"><span data-stu-id="c64ac-104">In Advanced Group Policy Management (AGPM), both the AGPM Service and the archive are managed by AGPM Administrators (Full Control).</span></span> <span data-ttu-id="c64ac-105">Im folgenden finden Sie typische Aufgaben für einen AGPM-Administrator.</span><span class="sxs-lookup"><span data-stu-id="c64ac-105">The following are typical tasks for an AGPM Administrator.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c64ac-106">Häufige Aufgabe</span><span class="sxs-lookup"><span data-stu-id="c64ac-106">Frequent Task</span></span></th>
<th align="left"><span data-ttu-id="c64ac-107">Verweis</span><span class="sxs-lookup"><span data-stu-id="c64ac-107">Reference</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c64ac-108">Delegieren des Zugriffs auf Gruppenrichtlinienobjekte (Group Policy Objects, GPOs) im Archiv</span><span class="sxs-lookup"><span data-stu-id="c64ac-108">Delegate access to Group Policy Objects (GPOs) in the archive.</span></span></p></td>
<td align="left"><p><a href="delegate-domain-level-access-to-the-archive-agpm30ops.md" data-raw-source="[Delegate Domain-Level Access to the Archive](delegate-domain-level-access-to-the-archive-agpm30ops.md)"><span data-ttu-id="c64ac-109">Delegieren des Domänenebenenzugriffs auf das Archiv</span><span class="sxs-lookup"><span data-stu-id="c64ac-109">Delegate Domain-Level Access to the Archive</span></span></a></p>
<p><a href="delegate-access-to-an-individual-gpo-in-the-archive-agpm30ops.md" data-raw-source="[Delegate Access to an Individual GPO in the Archive](delegate-access-to-an-individual-gpo-in-the-archive-agpm30ops.md)"><span data-ttu-id="c64ac-110">Delegieren des Zugriffs auf ein einzelnes Gruppenrichtlinienobjekt im Archiv</span><span class="sxs-lookup"><span data-stu-id="c64ac-110">Delegate Access to an Individual GPO in the Archive</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c64ac-111">Sichern Sie das Archiv, um eine Disaster Recovery zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="c64ac-111">Back up the archive to enable disaster recovery.</span></span></p></td>
<td align="left"><p><a href="back-up-the-archive.md" data-raw-source="[Back Up the Archive](back-up-the-archive.md)"><span data-ttu-id="c64ac-112">Sichern des Archivs</span><span class="sxs-lookup"><span data-stu-id="c64ac-112">Back Up the Archive</span></span></a></p></td>
</tr>
</tbody>
</table>

 

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c64ac-113">Seltene Aufgabe</span><span class="sxs-lookup"><span data-stu-id="c64ac-113">Infrequent Task</span></span></th>
<th align="left"><span data-ttu-id="c64ac-114">Verweis</span><span class="sxs-lookup"><span data-stu-id="c64ac-114">Reference</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c64ac-115">Wiederherstellen des Archivs aus einer Sicherung zur Wiederherstellung nach einem Notfall</span><span class="sxs-lookup"><span data-stu-id="c64ac-115">Restore the archive from a backup to recover from a disaster.</span></span></p></td>
<td align="left"><p><a href="restore-the-archive-from-a-backup.md" data-raw-source="[Restore the Archive from a Backup](restore-the-archive-from-a-backup.md)"><span data-ttu-id="c64ac-116">Wiederherstellen des Archivs aus einer Sicherung</span><span class="sxs-lookup"><span data-stu-id="c64ac-116">Restore the Archive from a Backup</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c64ac-117">Verschieben Sie den AGPM-Dienst, das Archiv oder beides auf einen anderen Server.</span><span class="sxs-lookup"><span data-stu-id="c64ac-117">Move the AGPM Service, the archive, or both to a different server.</span></span></p></td>
<td align="left"><p><a href="move-the-agpm-server-and-the-archive.md" data-raw-source="[Move the AGPM Server and the Archive](move-the-agpm-server-and-the-archive.md)"><span data-ttu-id="c64ac-118">Verschieben des AGPM-Servers und -Archivs</span><span class="sxs-lookup"><span data-stu-id="c64ac-118">Move the AGPM Server and the Archive</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c64ac-119">Ändern Sie den Archivierungspfad, das AGPM-Dienstkonto oder den Port, auf dem der AGPM-Dienst lauscht.</span><span class="sxs-lookup"><span data-stu-id="c64ac-119">Change the archive path, the AGPM Service Account, or the port on which the AGPM Service listens.</span></span></p></td>
<td align="left"><p><a href="modify-the-agpm-service-agpm30ops.md" data-raw-source="[Modify the AGPM Service](modify-the-agpm-service-agpm30ops.md)"><span data-ttu-id="c64ac-120">Ändern des AGPM-Diensts</span><span class="sxs-lookup"><span data-stu-id="c64ac-120">Modify the AGPM Service</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c64ac-121">Problembehandlung bei häufig auftretenden Problemen mit dem AGPM-Server.</span><span class="sxs-lookup"><span data-stu-id="c64ac-121">Troubleshoot common problems with the AGPM Server.</span></span></p></td>
<td align="left"><p><a href="troubleshooting-advanced-group-policy-management-agpm30ops.md" data-raw-source="[Troubleshooting Advanced Group Policy Management](troubleshooting-advanced-group-policy-management-agpm30ops.md)"><span data-ttu-id="c64ac-122">Problembehandlung bei Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="c64ac-122">Troubleshooting Advanced Group Policy Management</span></span></a></p>
<p><a href="configure-logging-and-tracing-agpm30ops.md" data-raw-source="[Configure Logging and Tracing](configure-logging-and-tracing-agpm30ops.md)"><span data-ttu-id="c64ac-123">Konfigurieren von Protokollierung und Ablaufverfolgung</span><span class="sxs-lookup"><span data-stu-id="c64ac-123">Configure Logging and Tracing</span></span></a></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="c64ac-124">Weitere Verweise</span><span class="sxs-lookup"><span data-stu-id="c64ac-124">Additional references</span></span>

-   [<span data-ttu-id="c64ac-125">Betriebshandbuch für Microsoft Advanced Group Policy Management 3.0</span><span class="sxs-lookup"><span data-stu-id="c64ac-125">Operations Guide for Microsoft Advanced Group Policy Management 3.0</span></span>](operations-guide-for-microsoft-advanced-group-policy-management-30-agpm30ops.md)

 

 





