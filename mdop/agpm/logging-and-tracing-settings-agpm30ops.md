---
title: Protokollierungs- und Ablaufverfolgungseinstellungen
description: Protokollierungs- und Ablaufverfolgungseinstellungen
author: dansimp
ms.assetid: 858b6fbf-65b4-42fa-95a9-69b04e5734d7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 078bda16b5fcf968d45e0c4890487471105e8c44
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808368"
---
# <span data-ttu-id="ee30c-103">Protokollierungs- und Ablaufverfolgungseinstellungen</span><span class="sxs-lookup"><span data-stu-id="ee30c-103">Logging and Tracing Settings</span></span>


<span data-ttu-id="ee30c-104">Mit den Einstellungen für administrative Vorlagen für erweiterte Gruppenrichtlinienverwaltung (AGPM) können Sie die Protokollierungs-und Ablaufverfolgungsoptionen für AGPM-Server und-Clients zentral konfigurieren, auf die ein Gruppenrichtlinienobjekt (GPO) mit diesen Einstellungen angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="ee30c-104">The Administrative template settings for Advanced Group Policy Management (AGPM) enable you to centrally configure logging and tracing options for AGPM Servers and clients to which a Group Policy Object (GPO) with these settings is applied.</span></span>

<span data-ttu-id="ee30c-105">Die folgende Einstellung ist unter Computer Configuration\\Policies\\Administrative Templates\\Windows Components\\AGPM beim Bearbeiten eines Gruppenrichtlinienobjekts verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ee30c-105">The following setting is available under Computer Configuration\\Policies\\Administrative Templates\\Windows Components\\AGPM when editing a GPO.</span></span>

<span data-ttu-id="ee30c-106">**Speicherort der Ablaufverfolgungsdatei**:</span><span class="sxs-lookup"><span data-stu-id="ee30c-106">**Trace file locations**:</span></span>

-   <span data-ttu-id="ee30c-107">Client:%localappdata%\\Microsoft\\AGPM\\agpm.log</span><span class="sxs-lookup"><span data-stu-id="ee30c-107">Client: %LocalAppData%\\Microsoft\\AGPM\\agpm.log</span></span>

-   <span data-ttu-id="ee30c-108">Server:%ProgramData%\\Microsoft\\AGPM\\agpmserv.log</span><span class="sxs-lookup"><span data-stu-id="ee30c-108">Server: %ProgramData%\\Microsoft\\AGPM\\agpmserv.log</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ee30c-109">Einstellung</span><span class="sxs-lookup"><span data-stu-id="ee30c-109">Setting</span></span></th>
<th align="left"><span data-ttu-id="ee30c-110">Effekt</span><span class="sxs-lookup"><span data-stu-id="ee30c-110">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="ee30c-111">AGPM: Konfigurieren der Protokollierung</span><span class="sxs-lookup"><span data-stu-id="ee30c-111">AGPM: Configure logging</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="ee30c-112">Mit dieser Richtlinieneinstellung können Sie die Protokollierung für AGPM aktivieren und konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="ee30c-112">This policy setting allows you to turn on and configure logging for AGPM.</span></span> <span data-ttu-id="ee30c-113">Diese Einstellung wirkt sich auf Client-und Server Komponenten von AGPM aus.</span><span class="sxs-lookup"><span data-stu-id="ee30c-113">This setting affects both client and server components of AGPM.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="ee30c-114">Weitere Verweise</span><span class="sxs-lookup"><span data-stu-id="ee30c-114">Additional references</span></span>

-   [<span data-ttu-id="ee30c-115">Ordner „Administrative Vorlagen“</span><span class="sxs-lookup"><span data-stu-id="ee30c-115">Administrative Templates Folder</span></span>](administrative-templates-folder-agpm30ops.md)

 

 





