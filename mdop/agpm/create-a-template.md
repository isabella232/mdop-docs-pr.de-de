---
title: Erstellen einer Vorlage
description: Erstellen einer Vorlage
author: dansimp
ms.assetid: 6992bd55-4a4f-401f-9815-c468bac598ef
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9ad57204170fc3f49b01b571d82b00e1faf62de0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808559"
---
# <span data-ttu-id="4dad8-103">Erstellen einer Vorlage</span><span class="sxs-lookup"><span data-stu-id="4dad8-103">Create a Template</span></span>


<span data-ttu-id="4dad8-104">Beim Erstellen einer Vorlage können Sie alle Einstellungen einer bestimmten Version eines Gruppenrichtlinienobjekts speichern, um Sie als Ausgangspunkt zum Erstellen neuer GPOs zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="4dad8-104">Creating a template enables you to save all of the settings of a particular version of a Group Policy object (GPO) to use as a starting point for creating new GPOs.</span></span>

<span data-ttu-id="4dad8-105">**Hinweis**  Eine Vorlage ist eine nicht bearbeitbare, statische Version eines GPO, die als Ausgangspunkt zum Erstellen neuer, bearbeitbarer GPOs verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="4dad8-105">**Note** A template is an uneditable, static version of a GPO for use as a starting point for creating new, editable GPOs.</span></span>

 

<span data-ttu-id="4dad8-106">Zum Ausführen dieses Verfahrens ist ein Benutzerkonto mit der Rolle "Editor" oder "AGPM-Administrator" (Vollzugriff) oder den erforderlichen Berechtigungen in der erweiterten Gruppenrichtlinienverwaltung erforderlich.</span><span class="sxs-lookup"><span data-stu-id="4dad8-106">A user account with the Editor or AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management is required to complete this procedure.</span></span> <span data-ttu-id="4dad8-107">Lesen Sie die Details unter "Weitere Überlegungen" in diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="4dad8-107">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="4dad8-108">So erstellen Sie eine Vorlage auf der Grundlage eines vorhandenen Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="4dad8-108">To create a template based on an existing GPO</span></span>**

1.  <span data-ttu-id="4dad8-109">Klicken Sie in der Struktur der **Gruppenrichtlinien-Verwaltungskonsole** in der Gesamtstruktur und Domäne, in der Sie GPOs verwalten möchten, auf **Steuerelement ändern** .</span><span class="sxs-lookup"><span data-stu-id="4dad8-109">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="4dad8-110">Klicken Sie im Detailbereich auf der Registerkarte **Inhalt** auf die Registerkarte **gesteuert** oder **unkontrolliert** , um verfügbare GPOs anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="4dad8-110">On the **Contents** tab in the details pane, click the **Controlled** or **Uncontrolled** tab to display available GPOs.</span></span>

3.  <span data-ttu-id="4dad8-111">Klicken Sie mit der rechten Maustaste auf das Gruppenrichtlinienobjekt, aus dem Sie eine Vorlage erstellen möchten, und klicken Sie dann auf **als Vorlage speichern**.</span><span class="sxs-lookup"><span data-stu-id="4dad8-111">Right-click the GPO from which you want to create a template, then click **Save as Template**.</span></span>

4.  <span data-ttu-id="4dad8-112">Geben Sie einen Namen für die Vorlage und einen Kommentar ein, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="4dad8-112">Type a name for the template and a comment, then click **OK**.</span></span>

5.  <span data-ttu-id="4dad8-113">Wenn das **Status** Fenster angibt, dass der Gesamtfortschritt abgeschlossen ist, klicken Sie auf **Schließen**.</span><span class="sxs-lookup"><span data-stu-id="4dad8-113">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="4dad8-114">Die neue Vorlage wird auf der Registerkarte **Vorlagen** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="4dad8-114">The new template appears on the **Templates** tab.</span></span>

### <span data-ttu-id="4dad8-115">Weitere Überlegungen</span><span class="sxs-lookup"><span data-stu-id="4dad8-115">Additional considerations</span></span>

-   <span data-ttu-id="4dad8-116">Standardmäßig müssen Sie ein Editor oder ein AGPM-Administrator (Vollzugriff) sein, um dieses Verfahren ausführen zu können.</span><span class="sxs-lookup"><span data-stu-id="4dad8-116">By default, you must be an Editor or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="4dad8-117">Insbesondere müssen Sie über **Listeninhalte** und **Vorlagen** Berechtigungen für die Domäne verfügen.</span><span class="sxs-lookup"><span data-stu-id="4dad8-117">Specifically, you must have **List Contents** and **Create Template** permissions for the domain.</span></span>

-   <span data-ttu-id="4dad8-118">Das Umbenennen oder Löschen einer Vorlage wirkt sich nicht auf GPOs aus, die mit dieser Vorlage erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="4dad8-118">Renaming or deleting a template does not impact GPOs created from that template.</span></span>

-   <span data-ttu-id="4dad8-119">Da Sie nicht geändert werden kann, hat eine Vorlage keinen Verlauf.</span><span class="sxs-lookup"><span data-stu-id="4dad8-119">Because it cannot be altered, a template does not have a history.</span></span>

### <span data-ttu-id="4dad8-120">Weitere Verweise</span><span class="sxs-lookup"><span data-stu-id="4dad8-120">Additional references</span></span>

-   [<span data-ttu-id="4dad8-121">Erstellen einer Vorlage und zum Festlegen einer Standardvorlage</span><span class="sxs-lookup"><span data-stu-id="4dad8-121">Creating a Template and Setting a Default Template</span></span>](creating-a-template-and-setting-a-default-template.md)

-   [<span data-ttu-id="4dad8-122">Anfordern der Erstellung eines neuen gesteuerten Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="4dad8-122">Request the Creation of a New Controlled GPO</span></span>](request-the-creation-of-a-new-controlled-gpo.md)

 

 





