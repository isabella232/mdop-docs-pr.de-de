---
title: AGPM Server-Verbindungseinstellungen
description: AGPM Server-Verbindungseinstellungen
author: dansimp
ms.assetid: cc67f122-6309-4820-92c2-f6a27d897123
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 55bd5c04f573a421674068bea6fc9c6adcd29a12
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804523"
---
# <span data-ttu-id="91c43-103">AGPM Server-Verbindungseinstellungen</span><span class="sxs-lookup"><span data-stu-id="91c43-103">AGPM Server Connection Settings</span></span>


<span data-ttu-id="91c43-104">Sie können die Einstellungen für administrative Vorlagen für die erweiterte Gruppenrichtlinienverwaltung (Group Policy Management, AGPM) verwenden, um AGPM-Server Verbindungen für Gruppenrichtlinienadministratoren zentral zu konfigurieren, denen ein Gruppenrichtlinienobjekt (GPO) mit diesen Einstellungen zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="91c43-104">You can use Administrative template settings for Advanced Group Policy Management (AGPM) to centrally configure AGPM Server connections for Group Policy administrators to whom a Group Policy Object (GPO) with these settings is applied.</span></span>

<span data-ttu-id="91c43-105">Die folgenden Einstellungen stehen unter Benutzer Configuration\\Policies\\Administrative Templates\\Windows Components\\AGPM beim Bearbeiten eines Gruppenrichtlinienobjekts zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="91c43-105">The following settings are available under User Configuration\\Policies\\Administrative Templates\\Windows Components\\AGPM when editing a GPO.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="91c43-106">Einstellung</span><span class="sxs-lookup"><span data-stu-id="91c43-106">Setting</span></span></th>
<th align="left"><span data-ttu-id="91c43-107">Effekt</span><span class="sxs-lookup"><span data-stu-id="91c43-107">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="91c43-108">AGPM: Angeben des standardmäßigen AGPM-Servers (alle Domänen)</span><span class="sxs-lookup"><span data-stu-id="91c43-108">AGPM: Specify default AGPM Server (all domains)</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="91c43-109">Mit dieser Richtlinieneinstellung können Sie einen standardmäßigen AGPM-Server für alle Domänen angeben.</span><span class="sxs-lookup"><span data-stu-id="91c43-109">This policy setting allows you to specify a default AGPM Server for all domains.</span></span> <span data-ttu-id="91c43-110">Dieser wird nur von AGPM-Clients verwendet und schränkt Gruppenrichtlinienadministratoren ein, eine Verbindung mit einem anderen Archiv herzustellen.</span><span class="sxs-lookup"><span data-stu-id="91c43-110">This is used only by AGPM Clients, and restricts Group Policy administrators from connecting to another archive.</span></span> <span data-ttu-id="91c43-111">Sie können diesen Standardwert für einzelne Domänen mithilfe der AGPM <strong> : Angeben von AGPM-Servereinstellungen außer Kraft setzen </strong> .</span><span class="sxs-lookup"><span data-stu-id="91c43-111">You can override this default for individual domains using the <strong>AGPM: Specify AGPM Servers</strong> setting.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="91c43-112">AGPM: Angeben von AGPM-Servern</span><span class="sxs-lookup"><span data-stu-id="91c43-112">AGPM: Specify AGPM Servers</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="91c43-113">Mit dieser Richtlinieneinstellung können Sie die AGPM-Server für einzelne Domänen angeben.</span><span class="sxs-lookup"><span data-stu-id="91c43-113">This policy setting allows you to specify the AGPM Servers for individual domains.</span></span> <span data-ttu-id="91c43-114">Dieser wird nur von AGPM-Clients verwendet und schränkt Gruppenrichtlinienadministratoren ein, die Verbindung zu einem anderen Archiv für die angegebene Domäne herzustellen.</span><span class="sxs-lookup"><span data-stu-id="91c43-114">This is used only by AGPM Clients, and restricts Group Policy administrators from connecting to a different archive for the specified domain.</span></span> <span data-ttu-id="91c43-115">Wenn Sie einen standardmäßigen AGPM-Server angeben möchten, verwenden Sie die <strong> Einstellung AGPM: standardmäßiger AGPM-Server (alle Domänen) angeben, </strong> und verwenden Sie diese Richtlinieneinstellung, um den Standardwert pro Domäne zu überschreiben.</span><span class="sxs-lookup"><span data-stu-id="91c43-115">To specify a default AGPM Server, use the <strong>AGPM: Specify default AGPM Server (all domains)</strong> setting and use this policy setting to override the default on a per domain basis.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="91c43-116">Weitere Verweise</span><span class="sxs-lookup"><span data-stu-id="91c43-116">Additional references</span></span>

-   [<span data-ttu-id="91c43-117">Ordner „Administrative Vorlagen“</span><span class="sxs-lookup"><span data-stu-id="91c43-117">Administrative Templates Folder</span></span>](administrative-templates-folder-agpm40.md)

-   [<span data-ttu-id="91c43-118">Durchführen von AGPM-Administratoraufgaben</span><span class="sxs-lookup"><span data-stu-id="91c43-118">Performing AGPM Administrator Tasks</span></span>](performing-agpm-administrator-tasks-agpm40.md)

 

 





