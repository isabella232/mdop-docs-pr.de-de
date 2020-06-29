---
title: Erstellen eines MED-V-Arbeitsbereichs
description: Erstellen eines MED-V-Arbeitsbereichs
author: dansimp
ms.assetid: 9578bb99-8a09-44c1-b88f-538901f16ad3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 189da6b28515f0d234c8a258138a27be7a7375d2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810810"
---
# <span data-ttu-id="204e5-103">Erstellen eines MED-V-Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="204e5-103">Creating a MED-V Workspace</span></span>


<span data-ttu-id="204e5-104">Ein Med-v-Arbeitsbereich ist die Desktopumgebung, in der Endbenutzer mit dem virtuellen Computer interagieren, der von Med-v bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="204e5-104">A MED-V workspace is the desktop environment in which end users interact with the virtual machine provided by MED-V.</span></span> <span data-ttu-id="204e5-105">Der Arbeitsbereich MED-V wird vom Administrator erstellt und angepasst.</span><span class="sxs-lookup"><span data-stu-id="204e5-105">The MED-V workspace is created and customized by the administrator.</span></span> <span data-ttu-id="204e5-106">Es besteht aus einem Bild und der Richtlinie, die die Regeln und Funktionen des MED-V-Arbeitsbereichs definiert.</span><span class="sxs-lookup"><span data-stu-id="204e5-106">It consists of an image and the policy, which defines the rules and functionality of the MED-V workspace.</span></span> <span data-ttu-id="204e5-107">Es können mehrere MED-V-Arbeitsbereiche erstellt werden, die jeweils mit eigener Konfiguration, Einstellungen und Regeln angepasst werden.</span><span class="sxs-lookup"><span data-stu-id="204e5-107">Multiple MED-V workspaces can be created, each customized with its own configuration, settings, and rules.</span></span> <span data-ttu-id="204e5-108">Einem Benutzer, einer Gruppe oder mehreren Benutzern oder Gruppen kann jeder Med-v-Arbeitsbereich zugeordnet werden, wodurch der Med-v-Arbeitsbereich nur für die Computer des zugehörigen Benutzers oder der Gruppe verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="204e5-108">A user, group, or multiple users or groups can be associated with each MED-V workspace, thereby making the MED-V workspace available only for the associated user's or group's computers.</span></span>

## <span data-ttu-id="204e5-109">Hinzufügen eines MED-V-Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="204e5-109">How to Add a MED-V Workspace</span></span>


**<span data-ttu-id="204e5-110">So fügen Sie einen MED-V-Arbeitsbereich hinzu</span><span class="sxs-lookup"><span data-stu-id="204e5-110">To add a MED-V workspace</span></span>**

1.  <span data-ttu-id="204e5-111">Klicken Sie auf die Schaltfläche **Richtlinien** Verwaltung, um das **Richtlinien** Modul zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="204e5-111">Click the **Policy** management button to open the **Policy** module.</span></span>

    <span data-ttu-id="204e5-112">Das **Richtlinien** Modul besteht aus dem Menü " **Arbeitsbereiche** " auf der linken Seite und den Registerkarten **Allgemein**, **Virtual Machine**, **Deployment**, **Applications**, **Web**, **VM Setup**, **Netzwerk**und **Leistung** .</span><span class="sxs-lookup"><span data-stu-id="204e5-112">The **Policy** module consists of the **Workspaces** menu on the left and the **General**, **Virtual Machine**, **Deployment**, **Applications**, **Web**, **VM Setup**, **Network**, and **Performance** tabs.</span></span>

2.  <span data-ttu-id="204e5-113">Wählen Sie im Menü **Richtlinie** den Eintrag **neuer Arbeitsbereich**aus, oder klicken Sie auf **Hinzufügen** , um einen neuen MED-V-Arbeitsbereich zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="204e5-113">On the **Policy** menu, select **New Workspace**, or click **Add** to create a new MED-V workspace.</span></span>

3.  <span data-ttu-id="204e5-114">Geben Sie auf der Registerkarte **Allgemein** im Feld **Name** den Namen des MED-V-Arbeitsbereichs ein.</span><span class="sxs-lookup"><span data-stu-id="204e5-114">On the **General** tab, in the **Name** field, enter the name of the MED-V workspace.</span></span>

4.  <span data-ttu-id="204e5-115">Geben Sie im Feld **Beschreibung** eine Beschreibung für den MED-V-Arbeitsbereich ein.</span><span class="sxs-lookup"><span data-stu-id="204e5-115">In the **Description** field, enter a description for the MED-V workspace.</span></span>

5.  <span data-ttu-id="204e5-116">Geben Sie im Feld **Support Kontakt** Informationen die Kontaktinformationen für den technischen Support ein.</span><span class="sxs-lookup"><span data-stu-id="204e5-116">In the **Support contact info** field, enter the contact information for technical support.</span></span>

    <span data-ttu-id="204e5-117">Weitere Informationen zum Konfigurieren eines Med-v-Arbeitsbereichs finden Sie unter [Konfigurieren von Med-v-Arbeitsbereichs Richtlinien](configuring-med-v-workspace-policies.md).</span><span class="sxs-lookup"><span data-stu-id="204e5-117">For more information about configuring a MED-V workspace, see [Configuring MED-V Workspace Policies](configuring-med-v-workspace-policies.md).</span></span>

## <span data-ttu-id="204e5-118">Klonen eines MED-V-Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="204e5-118">How to Clone a MED-V Workspace</span></span>


<span data-ttu-id="204e5-119">Ein Med-v-Arbeitsbereich kann geklont werden, damit Sie einen Med-v-Arbeitsbereich erstellen können, der mit einem vorhandenen Med-v-Arbeitsbereich identisch ist.</span><span class="sxs-lookup"><span data-stu-id="204e5-119">A MED-V workspace can be cloned so that you can create a MED-V workspace identical to an existing MED-V workspace.</span></span>

**<span data-ttu-id="204e5-120">So Klonen Sie einen MED-V-Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="204e5-120">To clone a MED-V workspace</span></span>**

1.  <span data-ttu-id="204e5-121">Klicken Sie zum Klonen auf den MED-V-Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="204e5-121">Click the MED-V workspace to clone.</span></span>

2.  <span data-ttu-id="204e5-122">Wählen Sie im Menü **Richtlinie** die Option **Arbeitsbereich duplizieren**aus.</span><span class="sxs-lookup"><span data-stu-id="204e5-122">On the **Policy** menu, select **Clone Workspace**.</span></span>

    <span data-ttu-id="204e5-123">Ein neuer Med-v-Arbeitsbereich wird mit dem Namen &lt; Original Med-v Workspace Name &gt; -2 erstellt.</span><span class="sxs-lookup"><span data-stu-id="204e5-123">A new MED-V workspace is created with the name &lt;Original MED-V workspace name&gt; - 2.</span></span>

## <span data-ttu-id="204e5-124">So löschen Sie einen MED-V-Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="204e5-124">How to Delete a MED-V Workspace</span></span>


**<span data-ttu-id="204e5-125">So löschen Sie einen MED-V-Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="204e5-125">To delete a MED-V workspace</span></span>**

-   <span data-ttu-id="204e5-126">Klicken Sie im **Richtlinien** Modul, während sich der Arbeitsbereich im Fokus befindet, auf **Entfernen**.</span><span class="sxs-lookup"><span data-stu-id="204e5-126">In the **Policy** module, while the workspace pane is in focus, click **Remove**.</span></span>

## <span data-ttu-id="204e5-127">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="204e5-127">Related topics</span></span>


[<span data-ttu-id="204e5-128">Über die Benutzeroberfläche der MED-V-Management-Konsole</span><span class="sxs-lookup"><span data-stu-id="204e5-128">Using the MED-V Management Console User Interface</span></span>](using-the-med-v-management-console-user-interface.md)

 

 





