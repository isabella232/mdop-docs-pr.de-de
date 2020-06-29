---
title: Protokollierungs- und Ablaufverfolgungseinstellungen
description: Protokollierungs- und Ablaufverfolgungseinstellungen
author: dansimp
ms.assetid: db6b43c7-fdde-4d11-b5ab-a81346e56940
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: bef0f8367647aad688c2aec7586ecdaae2e22143
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808367"
---
# <span data-ttu-id="596ab-103">Protokollierungs- und Ablaufverfolgungseinstellungen</span><span class="sxs-lookup"><span data-stu-id="596ab-103">Logging and Tracing Settings</span></span>


<span data-ttu-id="596ab-104">Mit den Einstellungen für administrative Vorlagen für erweiterte Gruppenrichtlinienverwaltung (AGPM) können Sie die Protokollierungs-und Ablaufverfolgungsoptionen für AGPM-Server und-Clients zentral konfigurieren, auf die ein Gruppenrichtlinienobjekt (GPO) mit diesen Einstellungen angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="596ab-104">The Administrative Template settings for Advanced Group Policy Management (AGPM) enable you to centrally configure logging and tracing options for AGPM Servers and clients to which a Group Policy object (GPO) with these settings is applied.</span></span>

<span data-ttu-id="596ab-105">Die folgende Einstellung ist unter Computer Configuration\\Administrative Templates\\Windows Components\\AGPM im **Gruppenrichtlinienobjekt-Editor** verfügbar, wenn Sie ein GPO in der Gruppenrichtlinien-Verwaltungskonsole (Group Policy Management Console, GPMC) bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="596ab-105">The following setting is available under Computer Configuration\\Administrative Templates\\Windows Components\\AGPM in the **Group Policy Object Editor** when editing a GPO in the Group Policy Management Console (GPMC).</span></span> <span data-ttu-id="596ab-106">Wenn dieser Pfad nicht angezeigt wird, klicken Sie mit der rechten Maustaste auf **Administrative Vorlagen**, und fügen Sie die Vorlage AGPM. ADMX oder AGPM. adm hinzu.</span><span class="sxs-lookup"><span data-stu-id="596ab-106">If this path is not visible, right-click **Administrative Templates**, and add the agpm.admx or agpm.adm template.</span></span>

<span data-ttu-id="596ab-107">**Speicherort der Ablaufverfolgungsdatei**:</span><span class="sxs-lookup"><span data-stu-id="596ab-107">**Trace file locations**:</span></span>

-   <span data-ttu-id="596ab-108">Client:%localappdata%\\Microsoft\\AGPM\\agpm.log</span><span class="sxs-lookup"><span data-stu-id="596ab-108">Client: %LocalAppData%\\Microsoft\\AGPM\\agpm.log</span></span>

-   <span data-ttu-id="596ab-109">Server:%CommonAppData%\\Microsoft\\AGPM\\agpmserv.log</span><span class="sxs-lookup"><span data-stu-id="596ab-109">Server: %CommonAppData%\\Microsoft\\AGPM\\agpmserv.log</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="596ab-110">Einstellung</span><span class="sxs-lookup"><span data-stu-id="596ab-110">Setting</span></span></th>
<th align="left"><span data-ttu-id="596ab-111">Effekt</span><span class="sxs-lookup"><span data-stu-id="596ab-111">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="596ab-112">AGPM-Protokollierung</span><span class="sxs-lookup"><span data-stu-id="596ab-112">AGPM Logging</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="596ab-113">Wenn diese Option aktiviert ist, wird mit dieser Einstellung konfiguriert, ob die Ablaufverfolgung aktiviert ist und wie detailliert die Detailebene ist.</span><span class="sxs-lookup"><span data-stu-id="596ab-113">If enabled, this setting configures whether tracing is turned on and the level of detail.</span></span> <span data-ttu-id="596ab-114">Diese Einstellung wirkt sich auf Client-und Server Komponenten von AGPM aus.</span><span class="sxs-lookup"><span data-stu-id="596ab-114">This setting affects both client and server components of AGPM.</span></span></p>
<p><span data-ttu-id="596ab-115">Wenn diese Einstellung deaktiviert oder nicht konfiguriert ist, hat dies keine Auswirkungen.</span><span class="sxs-lookup"><span data-stu-id="596ab-115">If disabled or not configured, this setting has no effect.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="596ab-116">Weitere Verweise</span><span class="sxs-lookup"><span data-stu-id="596ab-116">Additional references</span></span>

-   [<span data-ttu-id="596ab-117">Einstellungen für administrative Vorlagen</span><span class="sxs-lookup"><span data-stu-id="596ab-117">Administrative Template Settings</span></span>](administrative-template-settings.md)

 

 





