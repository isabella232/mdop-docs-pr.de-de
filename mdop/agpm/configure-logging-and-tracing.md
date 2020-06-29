---
title: Konfigurieren von Protokollierung und Ablaufverfolgung
description: Konfigurieren von Protokollierung und Ablaufverfolgung
author: dansimp
ms.assetid: 419231f9-e9db-4f91-a7cf-a0a73db25256
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fa3dfa71edb25f6641ade595cd4469e846410ac2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807720"
---
# <span data-ttu-id="cafe0-103">Konfigurieren von Protokollierung und Ablaufverfolgung</span><span class="sxs-lookup"><span data-stu-id="cafe0-103">Configure Logging and Tracing</span></span>


<span data-ttu-id="cafe0-104">Sie können die optionale Protokollierung und Ablaufverfolgung für erweiterte Gruppenrichtlinienverwaltung (AGPM) mithilfe administrativer Vorlagen zentral konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="cafe0-104">You can centrally configure optional logging and tracing for Advanced Group Policy Management (AGPM) using Administrative templates.</span></span>

<span data-ttu-id="cafe0-105">Ein Benutzerkonto mit der Rolle AGPM-Administrator (Vollzugriff), dem Benutzerkonto der genehmigenden Person, die das in diesen Verfahren verwendete Gruppenrichtlinienobjekt erstellt hat, oder ein Benutzerkonto mit den erforderlichen Berechtigungen in der erweiterten Gruppenrichtlinienverwaltung ist erforderlich, um diese Verfahren ausführen zu können.</span><span class="sxs-lookup"><span data-stu-id="cafe0-105">A user account with the AGPM Administrator (Full Control) role, the user account of the Approver who created the GPO used in these procedures, or a user account with the necessary permissions in Advanced Group Policy Management is required to complete these procedures.</span></span> <span data-ttu-id="cafe0-106">Darüber hinaus ist ein Benutzerkonto mit Zugriff auf den AGPM-Server erforderlich, um die Protokollierung auf dem AGPM-Server zu initiieren.</span><span class="sxs-lookup"><span data-stu-id="cafe0-106">Additionally, a user account with access to the AGPM Server is required to initiate logging on the AGPM Server.</span></span> <span data-ttu-id="cafe0-107">Lesen Sie die Details unter "Weitere Überlegungen" in diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="cafe0-107">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="cafe0-108">So konfigurieren Sie die Protokollierung und Ablaufverfolgung für AGPM</span><span class="sxs-lookup"><span data-stu-id="cafe0-108">To configure logging and tracing for AGPM</span></span>**

1.  <span data-ttu-id="cafe0-109">Bearbeiten Sie in der **Gruppenrichtlinien-Verwaltungskonsolen** Struktur ein GPO, das auf alle Gruppenrichtlinienadministratoren angewendet wird, für die Sie die Protokollierung und Ablaufverfolgung aktivieren möchten.</span><span class="sxs-lookup"><span data-stu-id="cafe0-109">In the **Group Policy Management Console** tree, edit a GPO that is applied to all Group Policy administrators for which you want to turn on logging and tracing.</span></span> <span data-ttu-id="cafe0-110">(Weitere Informationen finden Sie unter [Bearbeiten eines Gruppenrichtlinienobjekts](editing-a-gpo.md).)</span><span class="sxs-lookup"><span data-stu-id="cafe0-110">(For more information, see [Editing a GPO](editing-a-gpo.md).)</span></span>

2.  <span data-ttu-id="cafe0-111">Klicken Sie im **Gruppenrichtlinienobjekt-Editor**auf **Computer Konfiguration**, **Administrative Vorlagen**und **Windows-Komponenten**.</span><span class="sxs-lookup"><span data-stu-id="cafe0-111">In the **Group Policy Object Editor**, click **Computer Configuration**, **Administrative Templates**, and **Windows Components**.</span></span>

3.  <span data-ttu-id="cafe0-112">Wenn **AGPM** nicht unter Windows- **Komponenten**aufgeführt ist:</span><span class="sxs-lookup"><span data-stu-id="cafe0-112">If **AGPM** is not listed under **Windows Components**:</span></span>

    1.  <span data-ttu-id="cafe0-113">Klicken Sie mit der rechten Maustaste auf **Administrative Vorlagen** , und klicken Sie auf **Vorlagen hinzufügen/entfernen**.</span><span class="sxs-lookup"><span data-stu-id="cafe0-113">Right-click **Administrative Templates** and click **Add/Remove Templates**.</span></span>

    2.  <span data-ttu-id="cafe0-114">Klicken Sie auf **Hinzufügen**, wählen Sie **AGPM. ADMX** oder **AGPM. adm**aus, klicken Sie auf **Öffnen**und dann auf **Schließen**.</span><span class="sxs-lookup"><span data-stu-id="cafe0-114">Click **Add**, select **agpm.admx** or **agpm.adm**, click **Open**, and then click **Close**.</span></span>

4.  <span data-ttu-id="cafe0-115">Doppelklicken Sie unter **Windows-Komponenten**auf **AGPM**.</span><span class="sxs-lookup"><span data-stu-id="cafe0-115">Under **Windows Components**, double-click **AGPM**.</span></span>

5.  <span data-ttu-id="cafe0-116">Doppelklicken Sie im Detailbereich auf **AGPM-Protokollierung**.</span><span class="sxs-lookup"><span data-stu-id="cafe0-116">In the details pane, double-click **AGPM Logging**.</span></span>

6.  <span data-ttu-id="cafe0-117">Klicken Sie im Fenster **AGPM-Protokollierungseigenschaften** auf **aktiviert**, und konfigurieren Sie die Detailebene, die in den Protokollen aufgezeichnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="cafe0-117">In the **AGPM Logging Properties** window, click **Enabled**, and configure the level of detail to record in the logs.</span></span>

7.  <span data-ttu-id="cafe0-118">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="cafe0-118">Click **OK**.</span></span>

8.  <span data-ttu-id="cafe0-119">Schließen Sie den **Gruppenrichtlinienobjekt-Editor**.</span><span class="sxs-lookup"><span data-stu-id="cafe0-119">Close the **Group Policy Object Editor**.</span></span> <span data-ttu-id="cafe0-120">(Weitere Informationen finden Sie unter [Bereitstellen eines GPO](deploy-a-gpo.md).) Nachdem die Gruppenrichtlinie aktualisiert wurde, müssen Sie den AGPM-Dienst neu starten, um mit der Protokollierung auf dem AGPM-Server zu beginnen.</span><span class="sxs-lookup"><span data-stu-id="cafe0-120">(For more information, see [Deploy a GPO](deploy-a-gpo.md).) After Group Policy is updated, you must restart the AGPM Service to begin logging on the AGPM Server.</span></span> <span data-ttu-id="cafe0-121">Gruppenrichtlinienadministratoren müssen die GPMC schließen und neu starten, um mit der Protokollierung auf ihren Computern zu beginnen.</span><span class="sxs-lookup"><span data-stu-id="cafe0-121">Group Policy administrators must close and restart the GPMC to begin logging on their computers.</span></span>

    <span data-ttu-id="cafe0-122">**Speicherort der Ablaufverfolgungsdatei**:</span><span class="sxs-lookup"><span data-stu-id="cafe0-122">**Trace file locations**:</span></span>

    -   <span data-ttu-id="cafe0-123">Client:%localappdata%\\Microsoft\\AGPM\\agpm.log</span><span class="sxs-lookup"><span data-stu-id="cafe0-123">Client: %LocalAppData%\\Microsoft\\AGPM\\agpm.log</span></span>

    -   <span data-ttu-id="cafe0-124">Server:%ProgramData%\\Microsoft\\AGPM\\agpmserv.log</span><span class="sxs-lookup"><span data-stu-id="cafe0-124">Server: %ProgramData%\\Microsoft\\AGPM\\agpmserv.log</span></span>

### <span data-ttu-id="cafe0-125">Weitere Überlegungen</span><span class="sxs-lookup"><span data-stu-id="cafe0-125">Additional considerations</span></span>

-   <span data-ttu-id="cafe0-126">Sie müssen in der Lage sein, ein GPO zu bearbeiten und bereitzustellen, um die AGPM-Protokollierung und-Ablaufverfolgung konfigurieren zu können.</span><span class="sxs-lookup"><span data-stu-id="cafe0-126">You must be able to edit and deploy a GPO to configure AGPM logging and tracing.</span></span> <span data-ttu-id="cafe0-127">Weitere Informationen finden Sie unter [Bearbeiten eines GPO](editing-a-gpo.md) und [Bereitstellen eines Gruppenrichtlinienobjekts](deploy-a-gpo.md) .</span><span class="sxs-lookup"><span data-stu-id="cafe0-127">See [Editing a GPO](editing-a-gpo.md) and [Deploy a GPO](deploy-a-gpo.md) for additional detail.</span></span>

### <span data-ttu-id="cafe0-128">Weitere Verweise</span><span class="sxs-lookup"><span data-stu-id="cafe0-128">Additional references</span></span>

-   [<span data-ttu-id="cafe0-129">Durchführen von AGPM-Administratoraufgaben</span><span class="sxs-lookup"><span data-stu-id="cafe0-129">Performing AGPM Administrator Tasks</span></span>](performing-agpm-administrator-tasks.md)

 

 





