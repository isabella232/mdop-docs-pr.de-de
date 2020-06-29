---
title: Überprüfen von GPO-Einstellungen
description: Überprüfen von GPO-Einstellungen
author: dansimp
ms.assetid: c346bcde-dd6a-4775-aeab-721ca3a361b2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 336118fb8d099fa5a373415320e7ca5ce8bde761
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808248"
---
# <span data-ttu-id="8b066-103">Überprüfen von GPO-Einstellungen</span><span class="sxs-lookup"><span data-stu-id="8b066-103">Review GPO Settings</span></span>


<span data-ttu-id="8b066-104">Sie können HTML-basierte und XML-basierte Berichte zum Überprüfen von Einstellungen innerhalb einer beliebigen Version eines Gruppenrichtlinienobjekts (GPO) erstellen.</span><span class="sxs-lookup"><span data-stu-id="8b066-104">You can generate HTML-based and XML-based reports for reviewing settings within any version of a Group Policy Object (GPO).</span></span>

<span data-ttu-id="8b066-105">Zum Ausführen dieses Verfahrens ist ein Benutzerkonto mit der Rolle Prüfer, Bearbeiter, genehmigende Person oder AGPM-Administrator (Vollzugriff) oder den erforderlichen Berechtigungen in Advanced Group Policy Management (AGPM) erforderlich.</span><span class="sxs-lookup"><span data-stu-id="8b066-105">A user account with the Reviewer, Editor, Approver, or AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management (AGPM)is required to complete this procedure.</span></span> <span data-ttu-id="8b066-106">Lesen Sie die Details unter "Weitere Überlegungen" in diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="8b066-106">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="8b066-107">So überprüfen Sie die Einstellungen in einer beliebigen Version eines Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="8b066-107">To review settings in any version of a GPO</span></span>**

1.  <span data-ttu-id="8b066-108">Klicken Sie in der Struktur der **Gruppenrichtlinien-Verwaltungskonsole** in der Gesamtstruktur und Domäne, in der Sie GPOs verwalten möchten, auf **Steuerelement ändern** .</span><span class="sxs-lookup"><span data-stu-id="8b066-108">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="8b066-109">Klicken Sie im Detailbereich auf der Registerkarte **Inhalt** auf eine Registerkarte, um GPOs anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="8b066-109">On the **Contents** tab in the details pane, click a tab to display GPOs.</span></span>

3.  <span data-ttu-id="8b066-110">Doppelklicken Sie auf das Gruppenrichtlinienobjekt, um dessen Verlauf anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="8b066-110">Double-click the GPO to display its history.</span></span>

4.  <span data-ttu-id="8b066-111">Klicken Sie mit der rechten Maustaste auf die GPO-Version, für die Sie die Einstellungen überprüfen möchten, klicken Sie auf **Einstellungen**, und klicken Sie dann auf **HTML-Bericht** oder **XML-Bericht** , um eine Zusammenfassung der GPO-Einstellungen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="8b066-111">Right-click the GPO version for which to review the settings, click **Settings**, and then click **HTML Report** or **XML Report** to display a summary of the GPO's settings.</span></span>

### <span data-ttu-id="8b066-112">Weitere Überlegungen</span><span class="sxs-lookup"><span data-stu-id="8b066-112">Additional considerations</span></span>

-   <span data-ttu-id="8b066-113">Standardmäßig müssen Sie ein Prüfer, ein Bearbeiter, eine genehmigende Person oder ein AGPM-Administrator (Vollzugriff) sein, um dieses Verfahren ausführen zu können.</span><span class="sxs-lookup"><span data-stu-id="8b066-113">By default, you must be a Reviewer, an Editor, an Approver, or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="8b066-114">Insbesondere müssen Sie über die Berechtigungen **Listeninhalt** und **Leseeinstellungen** für das Gruppenrichtlinienobjekt verfügen.</span><span class="sxs-lookup"><span data-stu-id="8b066-114">Specifically, you must have **List Contents** and **Read Settings** permissions for the GPO.</span></span> <span data-ttu-id="8b066-115">Außerdem müssen Sie zum Anzeigen der Liste der GPOs über die Berechtigung **Listeninhalt** für die Domäne verfügen.</span><span class="sxs-lookup"><span data-stu-id="8b066-115">Also, to display the list of GPOs, you must have **List Contents** permission for the domain.</span></span>

### <span data-ttu-id="8b066-116">Weitere Verweise</span><span class="sxs-lookup"><span data-stu-id="8b066-116">Additional references</span></span>

-   [<span data-ttu-id="8b066-117">Durchführen von Prüferaufgaben</span><span class="sxs-lookup"><span data-stu-id="8b066-117">Performing Reviewer Tasks</span></span>](performing-reviewer-tasks-agpm40.md)

 

 





