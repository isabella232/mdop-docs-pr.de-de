---
title: Importieren eines Gruppenrichtlinienobjekts aus einer Datei
description: Importieren eines Gruppenrichtlinienobjekts aus einer Datei
author: dansimp
ms.assetid: 2cbcda72-4de3-47ad-aaf8-4fc7341d5a00
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 04819dacac8df73f0a61cace0dab8b9fa79b7307
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808432"
---
# <span data-ttu-id="ea4c4-103">Importieren eines Gruppenrichtlinienobjekts aus einer Datei</span><span class="sxs-lookup"><span data-stu-id="ea4c4-103">Import a GPO from a File</span></span>


<span data-ttu-id="ea4c4-104">Wenn Sie ein AGPM-Administrator (Vollzugriff) sind und ein Gruppenrichtlinienobjekt (GPO) in eine CAB-Datei exportiert haben, können Sie in der erweiterten Gruppenrichtlinienverwaltung (AGPM) die Richtlinieneinstellungen aus diesem Gruppenrichtlinienobjekt in ein neues Gruppenrichtlinienobjekt oder in ein vorhandenes GPO in einer Domäne in einer anderen Gesamtstruktur importieren.</span><span class="sxs-lookup"><span data-stu-id="ea4c4-104">In Advanced Group Policy Management (AGPM), if you are an AGPM Administrator (Full Control) and you have exported a Group Policy Object (GPO) to a CAB file, you can import the policy settings from that GPO into a new GPO or an existing GPO in a domain in another forest.</span></span> <span data-ttu-id="ea4c4-105">Informationen zum Exportieren von GPO-Einstellungen in eine CAB-Datei finden Sie unter [Exportieren eines Gruppenrichtlinienobjekts in eine Datei](export-a-gpo-to-a-file.md).</span><span class="sxs-lookup"><span data-stu-id="ea4c4-105">For information about exporting GPO settings to a CAB file, see [Export a GPO to a File](export-a-gpo-to-a-file.md).</span></span>

<span data-ttu-id="ea4c4-106">Ein Benutzerkonto mit der Rolle "AGPM-Administrator" oder die erforderlichen Berechtigungen in AGPM sind erforderlich, um Richtlinieneinstellungen in ein neues gesteuertes Gruppenrichtlinienobjekt zu importieren.</span><span class="sxs-lookup"><span data-stu-id="ea4c4-106">A user account with the AGPM Administrator role or the necessary permissions in AGPM is required to import policy settings into a new controlled GPO.</span></span> <span data-ttu-id="ea4c4-107">Ein Benutzerkonto mit der Rolle "Editor" oder "AGPM-Administrator" oder die erforderlichen Berechtigungen in AGPM sind erforderlich, um Richtlinieneinstellungen in ein vorhandenes Gruppenrichtlinienobjekt zu importieren.</span><span class="sxs-lookup"><span data-stu-id="ea4c4-107">A user account with the Editor or AGPM Administrator role or necessary permissions in AGPM is required to import policy settings into an existing GPO.</span></span> <span data-ttu-id="ea4c4-108">Lesen Sie die Details unter "Weitere Überlegungen" in diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="ea4c4-108">Review the details in "Additional considerations" in this topic.</span></span>

## <span data-ttu-id="ea4c4-109">Importieren von Richtlinieneinstellungen aus einer Datei</span><span class="sxs-lookup"><span data-stu-id="ea4c4-109">Importing policy settings from a file</span></span>


<span data-ttu-id="ea4c4-110">Wenn Sie Richtlinieneinstellungen aus einer Datei importieren, können Sie Sie in ein neues GPO oder ein vorhandenes Gruppenrichtlinienobjekt importieren.</span><span class="sxs-lookup"><span data-stu-id="ea4c4-110">When you import policy settings from a file, you can import them into a new GPO or an existing GPO.</span></span> <span data-ttu-id="ea4c4-111">Wenn Sie jedoch Richtlinieneinstellungen in ein vorhandenes GPO importieren, werden alle darin enthaltenen Richtlinieneinstellungen ersetzt.</span><span class="sxs-lookup"><span data-stu-id="ea4c4-111">However, if you import policy settings into an existing GPO, all policy settings within it are replaced.</span></span>

-   [<span data-ttu-id="ea4c4-112">Importieren von Richtlinieneinstellungen in ein neues gesteuertes Gruppenrichtlinienobjekt</span><span class="sxs-lookup"><span data-stu-id="ea4c4-112">Import policy settings into a new controlled GPO</span></span>](#bkmk-new)

-   [<span data-ttu-id="ea4c4-113">Importieren von Richtlinieneinstellungen in ein vorhandenes Gruppenrichtlinienobjekt</span><span class="sxs-lookup"><span data-stu-id="ea4c4-113">Import policy settings into an existing GPO</span></span>](#bkmk-existing)

### <a href="" id="bkmk-new"></a>

**<span data-ttu-id="ea4c4-114">So importieren Sie Richtlinieneinstellungen in ein neues gesteuertes Gruppenrichtlinienobjekt</span><span class="sxs-lookup"><span data-stu-id="ea4c4-114">To import policy settings into a new controlled GPO</span></span>**

1.  <span data-ttu-id="ea4c4-115">Klicken Sie in der **Gruppenrichtlinien-Verwaltungskonsolen** Struktur in der Domäne, für die Sie Richtlinieneinstellungen importieren möchten, auf **Steuerelement ändern** .</span><span class="sxs-lookup"><span data-stu-id="ea4c4-115">In the **Group Policy Management Console** tree, click **Change Control** in the domain to which you want to import policy settings.</span></span>

2.  <span data-ttu-id="ea4c4-116">Klicken Sie auf der Registerkarte **Inhalt** auf die Registerkarte **gesteuert** , um die gesteuerten GPOs anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="ea4c4-116">On the **Contents** tab, click the **Controlled** tab to display the controlled GPOs.</span></span>

3.  <span data-ttu-id="ea4c4-117">Erstellen eines neuen kontrollierten Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="ea4c4-117">Create a new controlled GPO.</span></span> <span data-ttu-id="ea4c4-118">Klicken Sie im Dialogfeld **Neues gesteuertes GPO** auf **importieren** und dann auf **Start-Assistent**.</span><span class="sxs-lookup"><span data-stu-id="ea4c4-118">In the **New Controlled GPO** dialog box, click **Import** and then click **Launch Wizard**.</span></span> <span data-ttu-id="ea4c4-119">Weitere Informationen zum Erstellen eines Gruppenrichtlinienobjekts finden Sie unter [Erstellen eines neuen kontrollierten Gruppenrichtlinienobjekts](create-a-new-controlled-gpo-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="ea4c4-119">For more information about how to create a GPO, see [Create a New Controlled GPO](create-a-new-controlled-gpo-agpm40.md).</span></span>

4.  <span data-ttu-id="ea4c4-120">Befolgen Sie die Anweisungen im **Assistenten zum Importieren von Einstellungen** , um eine GPO-Sicherung auszuwählen, die Richtlinieneinstellungen für das neue GPO zu importieren, und geben Sie einen Kommentar für den Überwachungspfad des neuen Gruppenrichtlinienobjekts ein.</span><span class="sxs-lookup"><span data-stu-id="ea4c4-120">Follow the instructions in the **Import Settings Wizard** to select a GPO backup, import policy settings from it for the new GPO, and enter a comment for the audit trail of the new GPO.</span></span>

### <a href="" id="bkmk-existing"></a>

**<span data-ttu-id="ea4c4-121">So importieren Sie Richtlinieneinstellungen in ein vorhandenes Gruppenrichtlinienobjekt</span><span class="sxs-lookup"><span data-stu-id="ea4c4-121">To import policy settings into an existing GPO</span></span>**

1.  <span data-ttu-id="ea4c4-122">Klicken Sie in der **Gruppenrichtlinien-Verwaltungskonsolen** Struktur in der Domäne, für die Sie Richtlinieneinstellungen importieren möchten, auf **Steuerelement ändern** .</span><span class="sxs-lookup"><span data-stu-id="ea4c4-122">In the **Group Policy Management Console** tree, click **Change Control** in the domain to which you want to import policy settings.</span></span>

2.  <span data-ttu-id="ea4c4-123">Klicken Sie auf der Registerkarte **Inhalt** auf die Registerkarte **gesteuert** , um die gesteuerten GPOs anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="ea4c4-123">On the **Contents** tab, click the **Controlled** tab to display the controlled GPOs.</span></span>

3.  <span data-ttu-id="ea4c4-124">Überprüfen Sie das Ziel-GPO, in das Sie Richtlinieneinstellungen importieren möchten.</span><span class="sxs-lookup"><span data-stu-id="ea4c4-124">Check out the destination GPO to which you want to import policy settings.</span></span>

4.  <span data-ttu-id="ea4c4-125">Klicken Sie mit der rechten Maustaste auf das Ziel-GPO, zeigen Sie auf **Importieren von**, und klicken Sie dann auf **Datei**.</span><span class="sxs-lookup"><span data-stu-id="ea4c4-125">Right-click the destination GPO, point to **Import from**, and then click **File**.</span></span>

5.  <span data-ttu-id="ea4c4-126">Befolgen Sie die Anweisungen im **Assistenten zum Importieren von Einstellungen** , um eine GPO-Sicherung auszuwählen, importieren Sie deren Richtlinieneinstellungen, um diese im Zielgruppen Richtlinienobjekt zu ersetzen, und geben Sie einen Kommentar für den Überwachungspfad des Zielgruppen Richtlinienobjekts ein.</span><span class="sxs-lookup"><span data-stu-id="ea4c4-126">Follow the instructions in the **Import Settings Wizard** to select a GPO backup, import its policy settings to replace those in the destination GPO, and enter a comment for the audit trail of the destination GPO.</span></span> <span data-ttu-id="ea4c4-127">Standardmäßig ist das Ziel-GPO nach Abschluss des Assistenten eingecheckt.</span><span class="sxs-lookup"><span data-stu-id="ea4c4-127">By default, the destination GPO is checked in when the wizard is finished.</span></span>

### <span data-ttu-id="ea4c4-128">Weitere Überlegungen</span><span class="sxs-lookup"><span data-stu-id="ea4c4-128">Additional considerations</span></span>

-   <span data-ttu-id="ea4c4-129">Wenn Sie Richtlinieneinstellungen in ein neues gesteuertes Gruppenrichtlinienobjekt importieren möchten, müssen Sie über **Listeninhalt**, **Gruppenrichtlinienobjekt importieren**und Berechtigungen zum **Erstellen von Gruppenrichtlinienobjekten** für die Domäne verfügen.</span><span class="sxs-lookup"><span data-stu-id="ea4c4-129">To import policy settings to a new controlled GPO, you must have **List Contents**, **Import GPO**, and **Create GPO** permissions for the domain.</span></span> <span data-ttu-id="ea4c4-130">Standardmäßig müssen Sie ein AGPM-Administrator sein, um dieses Verfahren ausführen zu können.</span><span class="sxs-lookup"><span data-stu-id="ea4c4-130">By default, you must be an AGPM Administrator to perform this procedure.</span></span>

-   <span data-ttu-id="ea4c4-131">Wenn Sie Richtlinieneinstellungen in ein vorhandenes Gruppenrichtlinienobjekt importieren möchten, müssen Sie über **Listeninhalt**, **Einstellungen zum Bearbeiten**und **Importieren von GPO** -Berechtigungen für die Domäne verfügen, und das Gruppenrichtlinienobjekt muss von Ihnen ausgecheckt werden.</span><span class="sxs-lookup"><span data-stu-id="ea4c4-131">To import policy settings to an existing GPO, you must have **List Contents**, **Edit Settings**, and **Import GPO** permissions for the domain, and the GPO must be checked out by you.</span></span> <span data-ttu-id="ea4c4-132">Standardmäßig müssen Sie ein Editor oder ein AGPM-Administrator (Vollzugriff) sein, um dieses Verfahren ausführen zu können.</span><span class="sxs-lookup"><span data-stu-id="ea4c4-132">By default, you must be an Editor or an AGPM Administrator (Full Control) to perform this procedure.</span></span>

### <span data-ttu-id="ea4c4-133">Weitere Verweise</span><span class="sxs-lookup"><span data-stu-id="ea4c4-133">Additional references</span></span>

-   [<span data-ttu-id="ea4c4-134">Verwalten des Archivs</span><span class="sxs-lookup"><span data-stu-id="ea4c4-134">Managing the Archive</span></span>](managing-the-archive-agpm40.md)

 

 





