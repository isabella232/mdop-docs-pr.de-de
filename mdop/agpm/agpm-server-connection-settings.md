---
title: AGPM Server-Verbindungseinstellungen
description: AGPM Server-Verbindungseinstellungen
author: dansimp
ms.assetid: faf78e5b-2b0d-4069-9b8c-910add892200
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d63163de0a1adf744e6d442b8073e5b32352ed67
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804664"
---
# <span data-ttu-id="deebd-103">AGPM Server-Verbindungseinstellungen</span><span class="sxs-lookup"><span data-stu-id="deebd-103">AGPM Server Connection Settings</span></span>


<span data-ttu-id="deebd-104">Sie können die Einstellungen für administrative Vorlagen für die erweiterte Gruppenrichtlinienverwaltung (Group Policy Management, AGPM) verwenden, um AGPM-Server Verbindungen für Gruppenrichtlinienadministratoren zentral zu konfigurieren, denen ein Gruppenrichtlinienobjekt (GPO) mit diesen Einstellungen zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="deebd-104">You can use Administrative template settings for Advanced Group Policy Management (AGPM) to centrally configure AGPM Server connections for Group Policy administrators to whom a Group Policy object (GPO) with these settings is applied.</span></span>

<span data-ttu-id="deebd-105">Die folgenden Einstellungen stehen unter Benutzer Configuration\\Administrative Templates\\Windows Components\\AGPM beim Bearbeiten eines Gruppenrichtlinienobjekts zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="deebd-105">The following settings are available under User Configuration\\Administrative Templates\\Windows Components\\AGPM when editing a GPO.</span></span> <span data-ttu-id="deebd-106">Wenn dieser Pfad nicht angezeigt wird, klicken Sie mit der rechten Maustaste auf **Administrative Vorlagen**, und fügen Sie die Vorlage AGPM. ADMX oder AGPM. adm hinzu.</span><span class="sxs-lookup"><span data-stu-id="deebd-106">If this path is not visible, right-click **Administrative Templates**, and add the agpm.admx or agpm.adm template.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="deebd-107">Einstellung</span><span class="sxs-lookup"><span data-stu-id="deebd-107">Setting</span></span></th>
<th align="left"><span data-ttu-id="deebd-108">Effekt</span><span class="sxs-lookup"><span data-stu-id="deebd-108">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="deebd-109">AGPM-Server (alle Domänen)</span><span class="sxs-lookup"><span data-stu-id="deebd-109">AGPM Server (all domains)</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="deebd-110">Wenn diese Option aktiviert ist, konfiguriert diese Einstellung zentral eine AGPM-Serververbindung für die Verwendung durch alle Domänen und deaktiviert die Einstellungen auf der <strong> Registerkarte AGPM-Server </strong> für Gruppenrichtlinienadministratoren.</span><span class="sxs-lookup"><span data-stu-id="deebd-110">If enabled, this setting centrally configures one AGPM Server connection for use by all domains and disables the settings on the <strong>AGPM Server</strong> tab for Group Policy administrators.</span></span> <span data-ttu-id="deebd-111">Konfigurieren Sie für mehrere AGPM-Server diese Einstellung mit einem Standardserver, und konfigurieren <strong> Sie dann die Einstellung AGPM-Server </strong> in der administrativen Vorlage, um diesen Server für andere Domänen zu überschreiben.</span><span class="sxs-lookup"><span data-stu-id="deebd-111">For multiple AGPM Servers, configure this setting with a default server and then configure the <strong>AGPM Server</strong> setting in the Administrative template to override this server for other domains.</span></span></p>
<p><span data-ttu-id="deebd-112">Wenn diese Option deaktiviert oder nicht konfiguriert ist, muss jeder Gruppenrichtlinienadministrator den AGPM-Server auswählen, der für jede Domäne auf der <strong> </strong> Registerkarte AGPM-Server in AGPM angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="deebd-112">If disabled or not configured, each Group Policy administrator must select the AGPM Server to display for each domain on the <strong>AGPM Server</strong> tab in AGPM.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="deebd-113">AGPM-Server</span><span class="sxs-lookup"><span data-stu-id="deebd-113">AGPM Server</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="deebd-114">Wenn diese Einstellung aktiviert ist, werden mehrere domänenspezifische AGPM-Server zentral konfiguriert, wobei die <strong> Einstellung AGPM-Server (alle Domänen) </strong> in der administrativen Vorlage überschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="deebd-114">If enabled, this setting centrally configures multiple domain-specific AGPM Servers, overriding the <strong>AGPM Server (all domains)</strong> setting in the Administrative template.</span></span> <span data-ttu-id="deebd-115">Wenn für Ihre Umgebung nur ein einzelner AGPM-Server erforderlich ist, verwenden Sie <strong> </strong> in der administrativen Vorlage nur die Einstellung AGPM-Server (alle Domänen).</span><span class="sxs-lookup"><span data-stu-id="deebd-115">If your environment requires only a single AGPM Server, use only the <strong>AGPM Server (all domains)</strong> setting in the Administrative template.</span></span></p>
<p><span data-ttu-id="deebd-116">Wenn diese Option deaktiviert oder nicht konfiguriert ist, wird <strong> mit der Einstellung AGPM-Server (alle Domänen) </strong> in der administrativen Vorlage die AGPM-Serververbindung konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="deebd-116">If disabled or not configured, the <strong>AGPM Server (all domains)</strong> setting in the Administrative template configures the AGPM Server connection.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="deebd-117">Weitere Verweise</span><span class="sxs-lookup"><span data-stu-id="deebd-117">Additional references</span></span>

-   [<span data-ttu-id="deebd-118">Einstellungen für administrative Vorlagen</span><span class="sxs-lookup"><span data-stu-id="deebd-118">Administrative Template Settings</span></span>](administrative-template-settings.md)

-   [<span data-ttu-id="deebd-119">Durchführen von AGPM-Administratoraufgaben</span><span class="sxs-lookup"><span data-stu-id="deebd-119">Performing AGPM Administrator Tasks</span></span>](performing-agpm-administrator-tasks.md)

 

 





