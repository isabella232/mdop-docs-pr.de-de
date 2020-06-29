---
title: Konfigurieren von Protokollierung und Ablaufverfolgung
description: Konfigurieren von Protokollierung und Ablaufverfolgung
author: dansimp
ms.assetid: 4f89552f-e949-48b0-9325-23746034eaa4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e6edcb643dd34a20a845cb3d44a0fe8b353a6291
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807724"
---
# <span data-ttu-id="41bca-103">Konfigurieren von Protokollierung und Ablaufverfolgung</span><span class="sxs-lookup"><span data-stu-id="41bca-103">Configure Logging and Tracing</span></span>


<span data-ttu-id="41bca-104">Sie können die optionale Protokollierung und Ablaufverfolgung mithilfe administrativer Vorlagen zentral konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="41bca-104">You can centrally configure optional logging and tracing using Administrative templates.</span></span> <span data-ttu-id="41bca-105">Dies kann beim Diagnostizieren von Problemen im Zusammenhang mit der erweiterten Gruppenrichtlinienverwaltung (AGPM) hilfreich sein.</span><span class="sxs-lookup"><span data-stu-id="41bca-105">This may be helpful when diagnosing any problems related to Advanced Group Policy Management (AGPM).</span></span>

<span data-ttu-id="41bca-106">Ein Benutzerkonto mit der Rolle AGPM-Administrator (Vollzugriff), dem Benutzerkonto der genehmigenden Person, die das in diesen Verfahren verwendete Gruppenrichtlinienobjekt (Group Policy Object, GPO) erstellt hat, oder ein Benutzerkonto mit den erforderlichen Berechtigungen in AGPM ist erforderlich, um diese Verfahren ausführen zu können.</span><span class="sxs-lookup"><span data-stu-id="41bca-106">A user account with the AGPM Administrator (Full Control) role, the user account of the Approver who created the Group Policy Object (GPO) used in these procedures, or a user account with the necessary permissions in AGPM is required to complete these procedures.</span></span> <span data-ttu-id="41bca-107">Darüber hinaus ist ein Benutzerkonto mit Zugriff auf den AGPM-Server erforderlich, um die Protokollierung auf dem AGPM-Server zu initiieren.</span><span class="sxs-lookup"><span data-stu-id="41bca-107">Additionally, a user account with access to the AGPM Server is required to initiate logging on the AGPM Server.</span></span> <span data-ttu-id="41bca-108">Lesen Sie die Details unter "Weitere Überlegungen" in diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="41bca-108">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="41bca-109">So konfigurieren Sie die Protokollierung und Ablaufverfolgung für AGPM</span><span class="sxs-lookup"><span data-stu-id="41bca-109">To configure logging and tracing for AGPM</span></span>**

1.  <span data-ttu-id="41bca-110">Bearbeiten Sie in der **Gruppenrichtlinien-Verwaltungskonsolen** Struktur ein GPO, das auf alle Gruppenrichtlinienadministratoren angewendet wird, für die Sie die Protokollierung und Ablaufverfolgung aktivieren möchten.</span><span class="sxs-lookup"><span data-stu-id="41bca-110">In the **Group Policy Management Console** tree, edit a GPO that is applied to all Group Policy administrators for which you want to turn on logging and tracing.</span></span> <span data-ttu-id="41bca-111">(Weitere Informationen finden Sie unter [Bearbeiten eines Gruppenrichtlinienobjekts](editing-a-gpo-agpm30ops.md).)</span><span class="sxs-lookup"><span data-stu-id="41bca-111">(For more information, see [Editing a GPO](editing-a-gpo-agpm30ops.md).)</span></span>

2.  <span data-ttu-id="41bca-112">Klicken Sie im Fenster **Gruppenrichtlinien-Verwaltungs-Editor** auf **Computer Konfiguration**, **Richtlinien**, **Administrative Vorlagen**, **Windows-Komponenten**und **AGPM**.</span><span class="sxs-lookup"><span data-stu-id="41bca-112">In the **Group Policy Management Editor** window, click **Computer Configuration**, **Policies**, **Administrative Templates**, **Windows Components**, and **AGPM**.</span></span>

3.  <span data-ttu-id="41bca-113">Doppelklicken Sie im Detailbereich auf **AGPM: Protokollierung konfigurieren**.</span><span class="sxs-lookup"><span data-stu-id="41bca-113">In the details pane, double-click **AGPM: Configure logging**.</span></span>

4.  <span data-ttu-id="41bca-114">Klicken Sie im **Eigenschaften** Fenster auf **aktiviert**, und konfigurieren Sie die Detailebene, die Sie in den Protokollen aufzeichnen möchten.</span><span class="sxs-lookup"><span data-stu-id="41bca-114">In the **Properties** window, click **Enabled**, and configure the level of detail to record in the logs.</span></span>

5.  <span data-ttu-id="41bca-115">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="41bca-115">Click **OK**.</span></span>

6.  <span data-ttu-id="41bca-116">Schließen Sie das Fenster **Gruppenrichtlinien-Verwaltungs-Editor** .</span><span class="sxs-lookup"><span data-stu-id="41bca-116">Close the **Group Policy Management Editor** window.</span></span> <span data-ttu-id="41bca-117">(Weitere Informationen finden Sie unter [Bereitstellen eines GPO](deploy-a-gpo-agpm30ops.md).) Nachdem die Gruppenrichtlinien aktualisiert wurden, müssen Sie den AGPM-Dienst neu starten, um die Protokollierung auf dem AGPM-Server zu starten, zu ändern oder zu beenden.</span><span class="sxs-lookup"><span data-stu-id="41bca-117">(For more information, see [Deploy a GPO](deploy-a-gpo-agpm30ops.md).) After Group Policy is updated, you must restart the AGPM Service to start, modify, or stop logging on the AGPM Server.</span></span> <span data-ttu-id="41bca-118">Gruppenrichtlinienadministratoren müssen die GPMC schließen und neu starten, um die Protokollierung auf ihren Computern zu starten, zu ändern oder zu beenden.</span><span class="sxs-lookup"><span data-stu-id="41bca-118">Group Policy administrators must close and restart the GPMC to start, modify, or stop logging on their computers.</span></span>

    <span data-ttu-id="41bca-119">**Speicherort der Ablaufverfolgungsdatei**:</span><span class="sxs-lookup"><span data-stu-id="41bca-119">**Trace file locations**:</span></span>

    -   <span data-ttu-id="41bca-120">Client:%localappdata%\\Microsoft\\AGPM\\agpm.log</span><span class="sxs-lookup"><span data-stu-id="41bca-120">Client: %LocalAppData%\\Microsoft\\AGPM\\agpm.log</span></span>

    -   <span data-ttu-id="41bca-121">Server:%ProgramData%\\Microsoft\\AGPM\\agpmserv.log</span><span class="sxs-lookup"><span data-stu-id="41bca-121">Server: %ProgramData%\\Microsoft\\AGPM\\agpmserv.log</span></span>

### <span data-ttu-id="41bca-122">Weitere Überlegungen</span><span class="sxs-lookup"><span data-stu-id="41bca-122">Additional considerations</span></span>

-   <span data-ttu-id="41bca-123">Sie müssen in der Lage sein, ein GPO zu bearbeiten und bereitzustellen, um die AGPM-Protokollierung und-Ablaufverfolgung konfigurieren zu können.</span><span class="sxs-lookup"><span data-stu-id="41bca-123">You must be able to edit and deploy a GPO to configure AGPM logging and tracing.</span></span> <span data-ttu-id="41bca-124">Weitere Informationen finden Sie unter [Bearbeiten eines GPO](editing-a-gpo-agpm30ops.md) und [Bereitstellen eines Gruppenrichtlinienobjekts](deploy-a-gpo-agpm30ops.md) .</span><span class="sxs-lookup"><span data-stu-id="41bca-124">See [Editing a GPO](editing-a-gpo-agpm30ops.md) and [Deploy a GPO](deploy-a-gpo-agpm30ops.md) for additional detail.</span></span>

### <span data-ttu-id="41bca-125">Weitere Verweise</span><span class="sxs-lookup"><span data-stu-id="41bca-125">Additional references</span></span>

-   [<span data-ttu-id="41bca-126">Konfigurieren von Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="41bca-126">Configuring Advanced Group Policy Management</span></span>](configuring-advanced-group-policy-management.md)

 

 





