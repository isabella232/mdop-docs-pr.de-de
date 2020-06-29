---
title: Importieren eines Gruppenrichtlinienobjekts aus einer Datei
description: Importieren eines Gruppenrichtlinienobjekts aus einer Datei
author: dansimp
ms.assetid: 6e901a52-1101-4fed-9f90-3819b573b378
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e15704806f089bb0d8530cd84df64b0889413426
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808420"
---
# <span data-ttu-id="97f2c-103">Importieren eines Gruppenrichtlinienobjekts aus einer Datei</span><span class="sxs-lookup"><span data-stu-id="97f2c-103">Import a GPO from a File</span></span>


<span data-ttu-id="97f2c-104">Wenn Sie in der erweiterten Gruppenrichtlinienverwaltung (Group Policy Management, AGPM) ein Gruppenrichtlinienobjekt in eine CAB-Datei exportiert haben, können Sie die Richtlinieneinstellungen aus diesem GPO in ein vorhandenes GPO in einer Domäne in einer anderen Gesamtstruktur importieren.</span><span class="sxs-lookup"><span data-stu-id="97f2c-104">In Advanced Group Policy Management (AGPM), if you have exported a Group Policy Object (GPO) to a CAB file, you can import the policy settings from that GPO into an existing GPO in a domain in another forest.</span></span> <span data-ttu-id="97f2c-105">Durch das Importieren von Richtlinieneinstellungen in ein vorhandenes GPO werden alle Richtlinieneinstellungen innerhalb dieses Gruppenrichtlinienobjekts ersetzt.</span><span class="sxs-lookup"><span data-stu-id="97f2c-105">Importing policy settings into an existing GPO replaces all policy settings within that GPO.</span></span> <span data-ttu-id="97f2c-106">Informationen zum Exportieren von GPO-Einstellungen in eine CAB-Datei finden Sie unter [Exportieren eines Gruppenrichtlinienobjekts in eine Datei](export-a-gpo-to-a-file.md).</span><span class="sxs-lookup"><span data-stu-id="97f2c-106">For information about exporting GPO settings to a CAB file, see [Export a GPO to a File](export-a-gpo-to-a-file.md).</span></span>

<span data-ttu-id="97f2c-107">Zum Ausführen dieses Verfahrens ist ein Benutzerkonto mit der Rolle "Editor" oder "AGPM-Administrator" (Vollzugriff) oder den erforderlichen Berechtigungen in der erweiterten Gruppenrichtlinienverwaltung (Group Policy Management, AGPM) erforderlich.</span><span class="sxs-lookup"><span data-stu-id="97f2c-107">A user account with the Editor or AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span><span data-ttu-id="97f2c-108">Lesen Sie die Details unter "Weitere Überlegungen" in diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="97f2c-108">Review the details in "Additional considerations" in this topic.</span></span>

## <a href="" id="bkmk-existing"></a>


**<span data-ttu-id="97f2c-109">So importieren Sie Richtlinieneinstellungen in ein vorhandenes Gruppenrichtlinienobjekt</span><span class="sxs-lookup"><span data-stu-id="97f2c-109">To import policy settings into an existing GPO</span></span>**

1.  <span data-ttu-id="97f2c-110">Klicken Sie in der **Gruppenrichtlinien-Verwaltungskonsolen** Struktur in der Domäne, für die Sie Richtlinieneinstellungen importieren möchten, auf **Steuerelement ändern** .</span><span class="sxs-lookup"><span data-stu-id="97f2c-110">In the **Group Policy Management Console** tree, click **Change Control** in the domain to which you want to import policy settings.</span></span>

2.  <span data-ttu-id="97f2c-111">Klicken Sie auf der Registerkarte **Inhalt** auf die Registerkarte **gesteuert** , um die gesteuerten GPOs anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="97f2c-111">On the **Contents** tab, click the **Controlled** tab to display the controlled GPOs.</span></span>

3.  <span data-ttu-id="97f2c-112">Überprüfen Sie das Ziel-GPO, in das Sie Richtlinieneinstellungen importieren möchten.</span><span class="sxs-lookup"><span data-stu-id="97f2c-112">Check out the destination GPO to which you want to import policy settings.</span></span>

4.  <span data-ttu-id="97f2c-113">Klicken Sie mit der rechten Maustaste auf das Ziel-GPO, zeigen Sie auf **Importieren von**, und klicken Sie dann auf **Datei**.</span><span class="sxs-lookup"><span data-stu-id="97f2c-113">Right-click the destination GPO, point to **Import from**, and then click **File**.</span></span>

5.  <span data-ttu-id="97f2c-114">Befolgen Sie die Anweisungen im **Assistenten zum Importieren von Einstellungen** , um eine GPO-Sicherung auszuwählen, importieren Sie deren Richtlinieneinstellungen, um diese im Zielgruppen Richtlinienobjekt zu ersetzen, und geben Sie einen Kommentar für den Überwachungspfad des Zielgruppen Richtlinienobjekts ein.</span><span class="sxs-lookup"><span data-stu-id="97f2c-114">Follow the instructions in the **Import Settings Wizard** to select a GPO backup, import its policy settings to replace those in the destination GPO, and enter a comment for the audit trail of the destination GPO.</span></span> <span data-ttu-id="97f2c-115">Standardmäßig ist das Ziel-GPO nach Abschluss des Assistenten eingecheckt.</span><span class="sxs-lookup"><span data-stu-id="97f2c-115">By default, the destination GPO is checked in when the wizard is finished.</span></span>

### <span data-ttu-id="97f2c-116">Weitere Überlegungen</span><span class="sxs-lookup"><span data-stu-id="97f2c-116">Additional considerations</span></span>

-   <span data-ttu-id="97f2c-117">Standardmäßig müssen Sie ein Editor oder ein AGPM-Administrator (Vollzugriff) sein, um dieses Verfahren ausführen zu können.</span><span class="sxs-lookup"><span data-stu-id="97f2c-117">By default, you must be an Editor or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="97f2c-118">Insbesondere müssen Sie über **Listeninhalte**, **Einstellungen zum Bearbeiten**und **Importieren von GPO** -Berechtigungen für die Domäne verfügen, und das Gruppenrichtlinienobjekt muss von Ihnen ausgecheckt sein.</span><span class="sxs-lookup"><span data-stu-id="97f2c-118">Specifically, you must have **List Contents**, **Edit Settings**, and **Import GPO** permissions for the domain, and the GPO must be checked out by you.</span></span>

-   <span data-ttu-id="97f2c-119">Obwohl ein Editor während der Erstellung keine Richtlinieneinstellungen in ein neues GPO importieren kann, kann ein Editor die Erstellung eines neuen Gruppenrichtlinienobjekts anfordern und dann Richtlinieneinstellungen importieren, nachdem es erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="97f2c-119">Although an Editor cannot import policy settings into a new GPO during its creation, an Editor can request the creation of a new GPO and then import policy settings into it after it is created.</span></span>

### <span data-ttu-id="97f2c-120">Weitere Verweise</span><span class="sxs-lookup"><span data-stu-id="97f2c-120">Additional references</span></span>

-   [<span data-ttu-id="97f2c-121">Verwenden einer Testumgebung</span><span class="sxs-lookup"><span data-stu-id="97f2c-121">Using a Test Environment</span></span>](using-a-test-environment.md)

 

 





