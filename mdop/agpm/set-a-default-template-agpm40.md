---
title: Festlegen einer Standardvorlage
description: Festlegen einer Standardvorlage
author: dansimp
ms.assetid: 07208b6b-cb3a-4f6c-9c84-36d4dc1486d8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 51a13c2c57e38adca883a6eb962d8c5eae4316db
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808224"
---
# <span data-ttu-id="f7cb0-103">Festlegen einer Standardvorlage</span><span class="sxs-lookup"><span data-stu-id="f7cb0-103">Set a Default Template</span></span>


<span data-ttu-id="f7cb0-104">Als Editor können Sie angeben, welche der verfügbaren Vorlagen die Standardvorlage sein soll, die für alle Gruppenrichtlinienadministratoren vorgeschlagen wird, die neue Gruppenrichtlinienobjekte (Group Policy Objects, GPOs) erstellen.</span><span class="sxs-lookup"><span data-stu-id="f7cb0-104">As an Editor, you can specify which of the available templates will be the default template suggested for all Group Policy administrators creating new Group Policy Objects (GPOs).</span></span>

<span data-ttu-id="f7cb0-105">**Hinweis**  Eine Vorlage ist eine nicht bearbeitbare, statische Version eines GPO, die als Ausgangspunkt zum Erstellen neuer, bearbeitbarer GPOs verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="f7cb0-105">**Note** A template is an uneditable, static version of a GPO for use as a starting point for creating new, editable GPOs.</span></span>

 

<span data-ttu-id="f7cb0-106">Zum Ausführen dieses Verfahrens ist ein Benutzerkonto mit der Rolle "Editor" oder "AGPM-Administrator" (Vollzugriff) oder den erforderlichen Berechtigungen in der erweiterten Gruppenrichtlinienverwaltung (Group Policy Management, AGPM) erforderlich.</span><span class="sxs-lookup"><span data-stu-id="f7cb0-106">A user account with the Editor or AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span> <span data-ttu-id="f7cb0-107">Lesen Sie die Details unter "Weitere Überlegungen" in diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="f7cb0-107">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="f7cb0-108">So legen Sie die Standardvorlage für die Verwendung beim Erstellen neuer GPOs vor</span><span class="sxs-lookup"><span data-stu-id="f7cb0-108">To set the default template for use when creating new GPOs</span></span>**

1.  <span data-ttu-id="f7cb0-109">Klicken Sie in der Struktur der **Gruppenrichtlinien-Verwaltungskonsole** in der Gesamtstruktur und Domäne, in der Sie GPOs verwalten möchten, auf **Steuerelement ändern** .</span><span class="sxs-lookup"><span data-stu-id="f7cb0-109">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="f7cb0-110">Klicken Sie im Detailbereich auf der Registerkarte **Inhalt** auf die Registerkarte **Vorlagen** , um die verfügbaren Vorlagen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="f7cb0-110">On the **Contents** tab in the details pane, click the **Templates** tab to display available templates.</span></span>

3.  <span data-ttu-id="f7cb0-111">Klicken Sie mit der rechten Maustaste auf die Vorlage, die Sie als Standard festlegen möchten, und klicken Sie dann auf **als Standard festlegen**.</span><span class="sxs-lookup"><span data-stu-id="f7cb0-111">Right-click the template that you want to set as the default, and then click **Set as Default**.</span></span>

4.  <span data-ttu-id="f7cb0-112">Klicken Sie zum bestätigen auf **Ja** .</span><span class="sxs-lookup"><span data-stu-id="f7cb0-112">Click **Yes** to confirm.</span></span>

5.  <span data-ttu-id="f7cb0-113">Wenn das **Status** Fenster angibt, dass der Gesamtfortschritt abgeschlossen ist, klicken Sie auf **Schließen**.</span><span class="sxs-lookup"><span data-stu-id="f7cb0-113">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="f7cb0-114">Die Standardvorlage weist ein blaues Symbol auf, und der Status wird auf der Registerkarte **Vorlagen** als **Vorlage (Standard)** bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="f7cb0-114">The default template has a blue icon and the state is identified as **Template (default)** on the **Templates** tab.</span></span>

### <span data-ttu-id="f7cb0-115">Weitere Überlegungen</span><span class="sxs-lookup"><span data-stu-id="f7cb0-115">Additional considerations</span></span>

-   <span data-ttu-id="f7cb0-116">Standardmäßig müssen Sie ein Editor oder ein AGPM-Administrator (Vollzugriff) sein, um dieses Verfahren ausführen zu können.</span><span class="sxs-lookup"><span data-stu-id="f7cb0-116">By default, you must be an Editor or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="f7cb0-117">Insbesondere müssen Sie über **Listeninhalte** und **Vorlagen** Berechtigungen für die Domäne verfügen.</span><span class="sxs-lookup"><span data-stu-id="f7cb0-117">Specifically, you must have **List Contents** and **Create Template** permissions for the domain.</span></span>

-   <span data-ttu-id="f7cb0-118">Nachdem Sie eine Vorlage als Standardvorlage festgelegt haben, wird diese Vorlage im Dialogfeld **Neues gesteuertes Gruppenrichtlinienobjekt** ausgewählt, wenn Gruppenrichtlinienadministratoren neue GPOs erstellen.</span><span class="sxs-lookup"><span data-stu-id="f7cb0-118">After you set a template as the default, that template will be the one initially selected in the **New Controlled GPO** dialog box when Group Policy administrators create new GPOs.</span></span> <span data-ttu-id="f7cb0-119">Sie haben jedoch die Möglichkeit, eine beliebige andere GPO-Vorlage zu wählen, einschließlich eines \*\* &lt; leeren Gruppenrichtlinienobjekts &gt; \*\*, das keine Einstellungen enthält.</span><span class="sxs-lookup"><span data-stu-id="f7cb0-119">However, they will have the option to select any other GPO template, including **&lt;Empty GPO&gt;**, which does not include any settings.</span></span>

-   <span data-ttu-id="f7cb0-120">Das Umbenennen oder Löschen einer Vorlage wirkt sich nicht auf GPOs aus, die mit dieser Vorlage erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="f7cb0-120">Renaming or deleting a template does not impact GPOs created from that template.</span></span>

-   <span data-ttu-id="f7cb0-121">Da Sie nicht geändert werden kann, hat eine Vorlage keinen Verlauf.</span><span class="sxs-lookup"><span data-stu-id="f7cb0-121">Because it cannot be altered, a template does not have a history.</span></span>

### <span data-ttu-id="f7cb0-122">Weitere Verweise</span><span class="sxs-lookup"><span data-stu-id="f7cb0-122">Additional references</span></span>

-   [<span data-ttu-id="f7cb0-123">Erstellen einer Vorlage und zum Festlegen einer Standardvorlage</span><span class="sxs-lookup"><span data-stu-id="f7cb0-123">Creating a Template and Setting a Default Template</span></span>](creating-a-template-and-setting-a-default-template-agpm40.md)

-   [<span data-ttu-id="f7cb0-124">Anfordern der Erstellung eines neuen gesteuerten Gruppenrichtlinienobjekts</span><span class="sxs-lookup"><span data-stu-id="f7cb0-124">Request the Creation of a New Controlled GPO</span></span>](request-the-creation-of-a-new-controlled-gpo-agpm40.md)

 

 





