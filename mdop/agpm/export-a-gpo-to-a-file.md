---
title: Exportieren eines Gruppenrichtlinienobjekts in eine Datei
description: Exportieren eines Gruppenrichtlinienobjekts in eine Datei
author: dansimp
ms.assetid: 0d01b1f7-a6a4-4d0d-9aa7-2d6f1ae93d9d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4622930cb0e5b439649cc0445ae2b3d02d7d3224
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808472"
---
# <span data-ttu-id="5c23c-103">Exportieren eines Gruppenrichtlinienobjekts in eine Datei</span><span class="sxs-lookup"><span data-stu-id="5c23c-103">Export a GPO to a File</span></span>


<span data-ttu-id="5c23c-104">Sie können ein gesteuertes Gruppenrichtlinienobjekt (GPO) in eine CAB-Datei exportieren, damit Sie es in eine Domäne in einer anderen Gesamtstruktur kopieren und das Gruppenrichtlinienobjekt in die erweiterte Gruppenrichtlinienverwaltung (Group Policy Management, AGPM) in dieser Domäne importieren können.</span><span class="sxs-lookup"><span data-stu-id="5c23c-104">You can export a controlled Group Policy Object (GPO) to a CAB file so that you can copy it to a domain in another forest and import the GPO into Advanced Group Policy Management (AGPM) in that domain.</span></span> <span data-ttu-id="5c23c-105">Informationen zum Importieren von GPO-Einstellungen in ein neues oder vorhandenes GPO finden Sie unter [Importieren eines Gruppenrichtlinienobjekts aus einer Datei](import-a-gpo-from-a-file-ed.md).</span><span class="sxs-lookup"><span data-stu-id="5c23c-105">For information about how to import GPO settings into a new or existing GPO, see [Import a GPO from a File](import-a-gpo-from-a-file-ed.md).</span></span>

<span data-ttu-id="5c23c-106">Zum Ausführen dieses Verfahrens ist ein Benutzerkonto mit der Rolle "Editor" oder "AGPM-Administrator" (Vollzugriff) oder den erforderlichen Berechtigungen in der erweiterten Gruppenrichtlinienverwaltung (Group Policy Management, AGPM) erforderlich.</span><span class="sxs-lookup"><span data-stu-id="5c23c-106">A user account with the Editor or AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span><span data-ttu-id="5c23c-107">Lesen Sie die Details unter "Weitere Überlegungen" in diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="5c23c-107">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="5c23c-108">So exportieren Sie ein GPO in eine Datei</span><span class="sxs-lookup"><span data-stu-id="5c23c-108">To export a GPO to a file</span></span>**

1.  <span data-ttu-id="5c23c-109">Klicken Sie in der Struktur der **Gruppenrichtlinien-Verwaltungskonsole** in der Gesamtstruktur und Domäne, in der Sie GPOs verwalten möchten, auf **Steuerelement ändern** .</span><span class="sxs-lookup"><span data-stu-id="5c23c-109">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="5c23c-110">Klicken Sie auf der Registerkarte **Inhalt** auf die Registerkarte **gesteuert** , um die gesteuerten GPOs anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="5c23c-110">On the **Contents** tab, click the **Controlled** tab to display the controlled GPOs.</span></span>

3.  <span data-ttu-id="5c23c-111">Klicken Sie mit der rechten Maustaste auf das Gruppenrichtlinienobjekt, und klicken Sie dann auf **Exportieren nach**.</span><span class="sxs-lookup"><span data-stu-id="5c23c-111">Right-click the GPO, and then click **Export to**.</span></span>

4.  <span data-ttu-id="5c23c-112">Geben Sie einen Dateinamen für die Datei ein, in die Sie das Gruppenrichtlinienobjekt exportieren möchten, und klicken Sie dann auf **exportieren**.</span><span class="sxs-lookup"><span data-stu-id="5c23c-112">Enter a file name for the file to which you want to export the GPO, and then click **Export**.</span></span> <span data-ttu-id="5c23c-113">Wenn die Datei nicht vorhanden ist, wird Sie erstellt.</span><span class="sxs-lookup"><span data-stu-id="5c23c-113">If the file does not exist, it is created.</span></span> <span data-ttu-id="5c23c-114">Wenn Sie bereits vorhanden ist, wird Sie ersetzt.</span><span class="sxs-lookup"><span data-stu-id="5c23c-114">If it already exists, it is replaced.</span></span>

### <span data-ttu-id="5c23c-115">Weitere Überlegungen</span><span class="sxs-lookup"><span data-stu-id="5c23c-115">Additional considerations</span></span>

-   <span data-ttu-id="5c23c-116">Standardmäßig müssen Sie ein Editor oder ein AGPM-Administrator (Vollzugriff) sein, um dieses Verfahren ausführen zu können.</span><span class="sxs-lookup"><span data-stu-id="5c23c-116">By default, you must be an Editor or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="5c23c-117">Insbesondere müssen Sie über **Listeninhalt**, **Leseeinstellungen**und Berechtigungen für das Gruppenrichtlinienobjekt **exportieren** verfügen.</span><span class="sxs-lookup"><span data-stu-id="5c23c-117">Specifically, you must have **List Contents**, **Read Settings**, and **Export GPO** permissions for the GPO.</span></span>

### <span data-ttu-id="5c23c-118">Weitere Verweise</span><span class="sxs-lookup"><span data-stu-id="5c23c-118">Additional references</span></span>

-   [<span data-ttu-id="5c23c-119">Verwenden einer Testumgebung</span><span class="sxs-lookup"><span data-stu-id="5c23c-119">Using a Test Environment</span></span>](using-a-test-environment.md)

 

 





