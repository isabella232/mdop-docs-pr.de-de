---
title: Sichtbarkeitseinstellungen für Features
description: Sichtbarkeitseinstellungen für Features
author: dansimp
ms.assetid: 9db2ba03-fb75-4f95-9138-ec89b9fc8d01
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 26f19895d0a9163885779688ba7d89f6d16f2a17
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808455"
---
# <span data-ttu-id="e05eb-103">Sichtbarkeitseinstellungen für Features</span><span class="sxs-lookup"><span data-stu-id="e05eb-103">Feature Visibility Settings</span></span>


<span data-ttu-id="e05eb-104">Mit den Einstellungen für administrative Vorlagen für die erweiterte Gruppenrichtlinienverwaltung (Group Policy Management, AGPM) können Sie die Sichtbarkeit des Knotens " **Änderungssteuerung** " und der Registerkarte " **Verlauf** " für Gruppenrichtlinienadministratoren zentral konfigurieren, denen ein Gruppenrichtlinienobjekt (GPO) mit diesen Einstellungen zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="e05eb-104">The Administrative template settings for Advanced Group Policy Management (AGPM) enable you to centrally configure the visibility of the **Change Control** node and **History** tab for Group Policy administrators to whom a Group Policy object (GPO) with these settings is applied.</span></span>

<span data-ttu-id="e05eb-105">Die folgenden Einstellungen sind unter Benutzer Configuration\\Administrative Templates\\Windows Components\\Microsoft-Verwaltungskonsole \ \ eingeschränkte/zulässige Snap-ins\\Extension-Snap-Ins im **Gruppenrichtlinienobjekt-Editor** verfügbar, wenn Sie ein GPO in der Gruppenrichtlinien-Verwaltungskonsole (Group Policy Management Console, GPMC) bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="e05eb-105">The following settings are available under User Configuration\\Administrative Templates\\Windows Components\\Microsoft Management Console\\Restricted/Permitted Snap-ins\\Extension Snap-ins in the **Group Policy Object Editor** when editing a GPO in the Group Policy Management Console (GPMC).</span></span> <span data-ttu-id="e05eb-106">Wenn dieser Pfad nicht angezeigt wird, klicken Sie mit der rechten Maustaste auf **Administrative Vorlagen**, und fügen Sie die Vorlage AGPM. ADMX oder AGPM. adm hinzu.</span><span class="sxs-lookup"><span data-stu-id="e05eb-106">If this path is not visible, right-click **Administrative Templates**, and add the agpm.admx or agpm.adm template.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="e05eb-107">Einstellung</span><span class="sxs-lookup"><span data-stu-id="e05eb-107">Setting</span></span></th>
<th align="left"><span data-ttu-id="e05eb-108">Effekt</span><span class="sxs-lookup"><span data-stu-id="e05eb-108">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="e05eb-109">AGPM-Änderungs Steuerelement</span><span class="sxs-lookup"><span data-stu-id="e05eb-109">AGPM Change Control</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="e05eb-110">Wenn aktiviert oder nicht konfiguriert, <strong> ist der Knoten Change Control </strong> in der GPMC sichtbar.</span><span class="sxs-lookup"><span data-stu-id="e05eb-110">If enabled or not configured, the <strong>Change Control</strong> node is visible in the GPMC.</span></span></p>
<p><span data-ttu-id="e05eb-111">Wenn diese Option deaktiviert <strong> ist, </strong> ist der Knoten Change Control in der GPMC nicht sichtbar.</span><span class="sxs-lookup"><span data-stu-id="e05eb-111">If disabled, the <strong>Change Control</strong> node is not visible in the GPMC.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="e05eb-112">AGPM-Link Erweiterung</span><span class="sxs-lookup"><span data-stu-id="e05eb-112">AGPM Link Extension</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="e05eb-113">Wenn diese Option aktiviert oder nicht konfiguriert ist, <strong> </strong> wird in der GPMC für jedes verknüpfte Gruppenrichtlinienobjekt die Registerkarte Verlauf angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e05eb-113">If enabled or not configured, a <strong>History</strong> tab appears in the GPMC for each linked GPO.</span></span></p>
<p><span data-ttu-id="e05eb-114">Wenn diese Option deaktiviert <strong> </strong> ist, ist die Registerkarte Verlauf für verknüpfte GPOs nicht sichtbar.</span><span class="sxs-lookup"><span data-stu-id="e05eb-114">If disabled, the <strong>History</strong> tab is not visible for linked GPOs.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="e05eb-115">AGPM-GPO-Erweiterung</span><span class="sxs-lookup"><span data-stu-id="e05eb-115">AGPM GPO Extension</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="e05eb-116">Wenn diese Option aktiviert oder nicht konfiguriert ist, <strong> </strong> wird in der GPMC für jedes GPO eine Verlaufs Registerkarte angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e05eb-116">If enabled or not configured, a <strong>History</strong> tab appears in the GPMC for each GPO.</span></span></p>
<p><span data-ttu-id="e05eb-117">Wenn diese Option deaktiviert <strong> </strong> ist, ist die Registerkarte Verlauf für GPOs nicht sichtbar.</span><span class="sxs-lookup"><span data-stu-id="e05eb-117">If disabled, the <strong>History</strong> tab is not visible for GPOs.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="e05eb-118">Weitere Verweise</span><span class="sxs-lookup"><span data-stu-id="e05eb-118">Additional references</span></span>

-   [<span data-ttu-id="e05eb-119">Einstellungen für administrative Vorlagen</span><span class="sxs-lookup"><span data-stu-id="e05eb-119">Administrative Template Settings</span></span>](administrative-template-settings.md)

 

 





