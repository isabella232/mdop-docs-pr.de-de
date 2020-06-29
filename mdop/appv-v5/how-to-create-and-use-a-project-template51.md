---
title: So erstellen und verwenden Sie eine Projektvorlage
description: So erstellen und verwenden Sie eine Projektvorlage
author: dansimp
ms.assetid: e5ac1dc8-a88f-4b16-8e3c-df07ef5e4c3b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: de3471eca39d3804e8c5f070c5ec37560fae5dc5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805585"
---
# <span data-ttu-id="2740b-103">So erstellen und verwenden Sie eine Projektvorlage</span><span class="sxs-lookup"><span data-stu-id="2740b-103">How to Create and Use a Project Template</span></span>


<span data-ttu-id="2740b-104">Sie können eine App-V 5,1-Projektvorlage verwenden, um häufig angewendete Einstellungen zu speichern, die mit einem vorhandenen virtuellen Anwendungspaket verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="2740b-104">You can use an App-V 5.1 project template to save commonly applied settings associated with an existing virtual application package.</span></span> <span data-ttu-id="2740b-105">Diese Einstellungen können dann angewendet werden, wenn Sie neue virtuelle Anwendungspakete in Ihrer Umgebung erstellen.</span><span class="sxs-lookup"><span data-stu-id="2740b-105">These settings can then be applied when you create new virtual application packages in your environment.</span></span> <span data-ttu-id="2740b-106">Die Verwendung einer Projektvorlage kann den Prozess zum Erstellen virtueller Anwendungspakete rationalisieren.</span><span class="sxs-lookup"><span data-stu-id="2740b-106">Using a project template can streamline the process of creating virtual application packages.</span></span>

**<span data-ttu-id="2740b-107">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="2740b-107">Note</span></span>**  
<span data-ttu-id="2740b-108">Sie können und sollten häufig eine App-V 5,1-Projektvorlage während eines Paket Upgrades anwenden.</span><span class="sxs-lookup"><span data-stu-id="2740b-108">You can, and often should apply an App-V 5.1 project template during a package upgrade.</span></span> <span data-ttu-id="2740b-109">Wenn Sie beispielsweise eine Anwendung mit einer benutzerdefinierten Ausschlussliste sequenziert haben, empfiehlt es sich, eine zugeordnete Vorlage für die spätere Verwendung beim Upgrade der sequenzierten Anwendung zu erstellen und zu speichern.</span><span class="sxs-lookup"><span data-stu-id="2740b-109">For example, if you sequenced an application with a custom exclusion list, it is recommended that an associated template is created and saved for later use while upgrading the sequenced application.</span></span>



<span data-ttu-id="2740b-110">App-v 5,1-Projektvorlagen unterscheiden sich von App-v 5,1-Anwendungs Beschleunigern, da App-v 5,1-Anwendungs Beschleuniger anwendungsspezifisch sind und App-v 5,1-Projektvorlagen auf mehrere Anwendungen angewendet werden können.</span><span class="sxs-lookup"><span data-stu-id="2740b-110">App-V 5.1 project templates differ from App-V 5.1 Application Accelerators because App-V 5.1 Application Accelerators are application-specific, and App-V 5.1 project templates can be applied to multiple applications.</span></span>

<span data-ttu-id="2740b-111">Gehen Sie wie folgt vor, um eine neue Vorlage zu erstellen und anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="2740b-111">Use the following procedures to create and apply a new template.</span></span>

**<span data-ttu-id="2740b-112">So erstellen Sie eine Projektvorlage</span><span class="sxs-lookup"><span data-stu-id="2740b-112">To create a project template</span></span>**

1.  <span data-ttu-id="2740b-113">Um den App-V 5,1-Sequenzer zu starten, klicken Sie auf dem Computer, auf dem der **Start**Sequencer ausgeführt wird, auf  /  **Alle Programme**starten  /  **Microsoft Application Virtualization**  /  **Microsoft Application Virtualization Sequencer**.</span><span class="sxs-lookup"><span data-stu-id="2740b-113">To start the App-V 5.1 sequencer, on the computer that is running the sequencer, click **Start** / **All Programs** / **Microsoft Application Virtualization** / **Microsoft Application Virtualization Sequencer**.</span></span>

2.  **<span data-ttu-id="2740b-114">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="2740b-114">Note</span></span>**  
    <span data-ttu-id="2740b-115">Wenn das virtuelle Anwendungspaket derzeit in der App-V 5,1-Sequenzer-Konsole geöffnet ist, fahren Sie mit Schritt 3 dieses Verfahrens fort.</span><span class="sxs-lookup"><span data-stu-id="2740b-115">If the virtual application package is currently open in the App-V 5.1 Sequencer console, skip to step 3 of this procedure.</span></span>



~~~
To open the existing virtual application package that contains the settings you want to save with the App-V 5.1 project template, click **File** / **Open**, and then click **Edit Package**. On the **Select Package** page, click **Browse** and locate the virtual application package that you want to open. Click **Edit**.
~~~

3. <span data-ttu-id="2740b-116">Klicken Sie in der App-V 5,1-Sequenzer-Konsole auf **Datei**  /  **als Vorlage speichern**, um die Vorlagendatei zu speichern.</span><span class="sxs-lookup"><span data-stu-id="2740b-116">In the App-V 5.1 Sequencer console, to save the template file, click **File** / **Save As Template**.</span></span> <span data-ttu-id="2740b-117">Nachdem Sie die Einstellungen überprüft haben, die mit der neuen Vorlage gespeichert werden, klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="2740b-117">After you have reviewed the settings that will be saved with the new template, click **OK**.</span></span> <span data-ttu-id="2740b-118">Geben Sie einen Namen an, der der neuen App-V 5,1-Projektvorlage zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="2740b-118">Specify a name that will be associated with the new App-V 5.1 project template.</span></span> <span data-ttu-id="2740b-119">Klicken Sie auf Speichern.</span><span class="sxs-lookup"><span data-stu-id="2740b-119">Click Save.</span></span>

   <span data-ttu-id="2740b-120">Die neue App-V 5,1-Projektvorlage wird in dem in Schritt 3 dieser Vorgehensweise angegebenen Verzeichnis gespeichert.</span><span class="sxs-lookup"><span data-stu-id="2740b-120">The new App-V 5.1 project template is saved in the directory specified in step 3 of this procedure.</span></span>

**<span data-ttu-id="2740b-121">So wenden Sie eine Projektvorlage an</span><span class="sxs-lookup"><span data-stu-id="2740b-121">To apply a project template</span></span>**

1.  **<span data-ttu-id="2740b-122">Wichtig</span><span class="sxs-lookup"><span data-stu-id="2740b-122">Important</span></span>**  
    <span data-ttu-id="2740b-123">Das Erstellen eines virtuellen Anwendungspakets unter Verwendung einer Projektvorlage in Verbindung mit einem Paket Beschleuniger wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2740b-123">Creating a virtual application package using a project template in conjunction with a Package Accelerator is not supported.</span></span>



~~~
To start the App-V 5.1 sequencer, on the computer that is running the sequencer, click **Start** / **All Programs** / **Microsoft Application Virtualization** / **Microsoft Application Virtualization Sequencer**.
~~~

2. <span data-ttu-id="2740b-124">Wenn Sie ein neues virtuelles Anwendungspaket mithilfe einer App-V 5,1-Projektvorlage erstellen oder aktualisieren möchten, klicken Sie auf **Datei**  /  **neu aus Vorlage**.</span><span class="sxs-lookup"><span data-stu-id="2740b-124">To create or upgrade a new virtual application package by using an App-V 5.1 project template, click **File** / **New From Template**.</span></span>

3. <span data-ttu-id="2740b-125">Um die Projektvorlage auszuwählen, die Sie verwenden möchten, navigieren Sie zu dem Verzeichnis, in dem die Projektvorlage gespeichert ist, wählen Sie die Projektvorlage aus, und klicken Sie dann auf **Öffnen**.</span><span class="sxs-lookup"><span data-stu-id="2740b-125">To select the project template that you want to use, browse to the directory where the project template is saved, select the project template, and then click **Open**.</span></span>

   <span data-ttu-id="2740b-126">Erstellen Sie das neue virtuelle Anwendungspaket.</span><span class="sxs-lookup"><span data-stu-id="2740b-126">Create the new virtual application package.</span></span> <span data-ttu-id="2740b-127">Die mit der angegebenen Vorlage gespeicherten Einstellungen werden auf das neue virtuelle Anwendungspaket angewendet, das Sie erstellen.</span><span class="sxs-lookup"><span data-stu-id="2740b-127">The settings saved with the specified template will be applied to the new virtual application package that you are creating.</span></span>

   <span data-ttu-id="2740b-128">Sie **haben einen Vorschlag für App-V**?</span><span class="sxs-lookup"><span data-stu-id="2740b-128">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="2740b-129">[Hier](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)können Sie Vorschläge hinzufügen oder abstimmen.</span><span class="sxs-lookup"><span data-stu-id="2740b-129">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="2740b-130">Sie haben ein App-V-Problem?</span><span class="sxs-lookup"><span data-stu-id="2740b-130">Got an App-V issue?</span></span>** <span data-ttu-id="2740b-131">Verwenden Sie das [App-V TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="2740b-131">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="2740b-132">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="2740b-132">Related topics</span></span>


[<span data-ttu-id="2740b-133">Vorgänge für App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="2740b-133">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)









