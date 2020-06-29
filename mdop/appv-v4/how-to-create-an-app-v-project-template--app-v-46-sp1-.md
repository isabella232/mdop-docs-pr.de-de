---
title: So erstellen Sie eine App-V-Projektvorlage (App-V 4.6 SP1)
description: So erstellen Sie eine App-V-Projektvorlage (App-V 4.6 SP1)
author: dansimp
ms.assetid: 7e87fba2-b72a-4bc9-92b8-220e25aae99a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4e264d5c41b663bc9c450dc642e2b26297ee7ea1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807191"
---
# <span data-ttu-id="83370-103">So erstellen Sie eine App-V-Projektvorlage (App-V 4.6 SP1)</span><span class="sxs-lookup"><span data-stu-id="83370-103">How to Create an App-V Project Template (App-V 4.6 SP1)</span></span>


<span data-ttu-id="83370-104">Sie können eine App-V-Projektvorlage verwenden, um häufig verwendete Einstellungen zu speichern, die mit einem vorhandenen virtuellen Anwendungspaket verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="83370-104">You can use an App-V project template to save commonly applied settings associated with an existing virtual application package.</span></span> <span data-ttu-id="83370-105">Diese Einstellungen können dann angewendet werden, wenn Sie in Ihrer Umgebung neue virtuelle Anwendungspakete erstellen, die dazu beitragen können, das Erstellen von virtuellen Anwendungspaketen zu vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="83370-105">These settings can then be applied when you create new virtual application packages in your environment which can help streamline the process of creating virtual application packages.</span></span>

<span data-ttu-id="83370-106">**Hinweis**  Sie können nur dann eine App-V-Projektvorlage anwenden, wenn Sie ein neues virtuelles Anwendungspaket erstellen.</span><span class="sxs-lookup"><span data-stu-id="83370-106">**Note** You can only apply an App-V project template when you are creating a new virtual application package.</span></span> <span data-ttu-id="83370-107">Das Anwenden von Projektvorlagen auf vorhandene virtuelle Anwendungspakete wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="83370-107">Applying project templates to existing virtual application packages is not supported.</span></span>

 

<span data-ttu-id="83370-108">Weitere Informationen zum Anwenden einer APP-v-Projektvorlage finden Sie unter [Anwenden einer APP-v-Projektvorlage (app-v 4,6 SP1)](how-to-apply-an-app-v-project-template--app-v-46-sp1-.md).</span><span class="sxs-lookup"><span data-stu-id="83370-108">For more information about applying an App-V project template, see [How to Apply an App-V Project Template (App-V 4.6 SP1)](how-to-apply-an-app-v-project-template--app-v-46-sp1-.md).</span></span>

<span data-ttu-id="83370-109">App-v-Projektvorlagen unterscheiden sich von App-v-Anwendungs Beschleunigern, da App-v-Anwendungs Beschleuniger anwendungsspezifisch sind und App-v-Projektvorlagen auf mehrere Anwendungen angewendet werden können.</span><span class="sxs-lookup"><span data-stu-id="83370-109">App-V project templates differ from App-V Application Accelerators because App-V Application Accelerators are application-specific, and App-V project templates can be applied to multiple applications.</span></span> <span data-ttu-id="83370-110">Darüber hinaus können Sie keine Projektvorlage verwenden, wenn Sie ein Paket Beschleuniger zum Erstellen eines virtuellen Anwendungspakets verwenden.</span><span class="sxs-lookup"><span data-stu-id="83370-110">Additionally, you cannot use a project template when you use a Package Accelerator to create a virtual application package.</span></span>

<span data-ttu-id="83370-111">Die folgenden allgemeinen Einstellungen werden mit einer App-V-Projektvorlage gespeichert:</span><span class="sxs-lookup"><span data-stu-id="83370-111">The following general settings are saved with an App-V project template:</span></span>

-   <span data-ttu-id="83370-112">**Erweiterte Überwachungsoptionen**.</span><span class="sxs-lookup"><span data-stu-id="83370-112">**Advanced Monitoring Options**.</span></span> <span data-ttu-id="83370-113">Ermöglicht die Ausführung von Microsoft Update während der Überwachung, rebase **. dll's**.</span><span class="sxs-lookup"><span data-stu-id="83370-113">Enables Microsoft Update to run during monitoring, Rebase **.dll’s**.</span></span>

-   <span data-ttu-id="83370-114">**Paket Bereitstellungseinstellungen**.</span><span class="sxs-lookup"><span data-stu-id="83370-114">**Package Deployment Settings**.</span></span> <span data-ttu-id="83370-115">Enthält **Protokoll**, **Hostname**, **Port**, **Pfad**, **Betriebssysteme**, **Sicherheitsbeschreibungen erzwingen**, **MSI erstellen**, **Paket komprimieren**.</span><span class="sxs-lookup"><span data-stu-id="83370-115">Contains **Protocol**, **Host Name**, **Port**, **Path**, **Operating Systems**, **Enforce Security Descriptors**, **Create MSI**, **Compress Package**.</span></span>

-   <span data-ttu-id="83370-116">**Allgemeine Optionen**.</span><span class="sxs-lookup"><span data-stu-id="83370-116">**General Options**.</span></span> <span data-ttu-id="83370-117">Ermöglicht es Ihnen, das **Microsoft Windows Installer-Paket (MSI) zu generieren** , die **Virtualisierung von Ereignissen zu ermöglichen**, die **Virtualisierung von Diensten zu ermöglichen**, **die Paket Version an filename anzufügen**.</span><span class="sxs-lookup"><span data-stu-id="83370-117">Allows you to **Generate Microsoft Windows Installer (MSI)** package, **Allow Virtualization of Events**, **Allow Virtualization of Services**, **Append Package Version to Filename**.</span></span>

-   <span data-ttu-id="83370-118">**Ausschlusselemente**.</span><span class="sxs-lookup"><span data-stu-id="83370-118">**Exclusion Items**.</span></span> <span data-ttu-id="83370-119">Enthält die Ausschlussmuster Liste.</span><span class="sxs-lookup"><span data-stu-id="83370-119">Contains the Exclusion pattern list.</span></span>

**<span data-ttu-id="83370-120">So erstellen Sie eine Projektvorlage</span><span class="sxs-lookup"><span data-stu-id="83370-120">To create a project template</span></span>**

1.  <span data-ttu-id="83370-121">Klicken Sie zum Starten des App-v-Sequencers auf dem Computer, auf dem der APP-v-Sequenzer ausgeführt wird, auf **Start**  /  **Alle Programme**starten  /  **Microsoft Application Virtualization**  /  **Microsoft Application Virtualization Sequencer**.</span><span class="sxs-lookup"><span data-stu-id="83370-121">To start the App-V Sequencer, on the computer that is running the App-V Sequencer, click **Start** / **All Programs** / **Microsoft Application Virtualization** / **Microsoft Application Virtualization Sequencer**.</span></span>

2.  <span data-ttu-id="83370-122">Wenn das virtuelle Anwendungspaket zurzeit im App-V-Sequenzer geöffnet ist, fahren Sie mit Schritt 3 dieses Verfahrens fort.</span><span class="sxs-lookup"><span data-stu-id="83370-122">If the virtual application package is currently open in the App-V Sequencer, skip to step 3 of this procedure.</span></span> <span data-ttu-id="83370-123">Zum Öffnen des vorhandenen virtuellen Anwendungspakets, das die Einstellungen enthält, die Sie mit der App-V-Projektvorlage speichern möchten, klicken Sie auf **Datei**  /  **Öffnen** , und klicken Sie auf **Paket** **Bearbeiten** .</span><span class="sxs-lookup"><span data-stu-id="83370-123">To open the existing virtual application package that contains the settings you want to save with the App-V project template, click **File** / **Open** and click **Edit** **Package**.</span></span> <span data-ttu-id="83370-124">Klicken Sie auf der Seite **Paket auswählen** auf **Durchsuchen** , und suchen Sie nach dem virtuellen Anwendungspaket, das Sie öffnen möchten.</span><span class="sxs-lookup"><span data-stu-id="83370-124">On the **Select Package** page, click **Browse** and locate the virtual application package that you want to open.</span></span> <span data-ttu-id="83370-125">Klicken Sie auf **Bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="83370-125">Click **Edit**.</span></span>

3.  <span data-ttu-id="83370-126">Klicken Sie in der App-V Sequencer-Konsole auf **Datei**  /  **als Vorlage speichern**.</span><span class="sxs-lookup"><span data-stu-id="83370-126">In the App-V Sequencer console, click **File** / **Save As Template**.</span></span> <span data-ttu-id="83370-127">Nachdem Sie die Einstellungen überprüft haben, die mit der neuen Vorlage gespeichert werden, klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="83370-127">After you have reviewed the settings that will be saved with the new template, click **OK**.</span></span> <span data-ttu-id="83370-128">Geben Sie einen Namen an, der der neuen App-V-Projektvorlage zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="83370-128">Specify a name that will be associated with the new App-V project template.</span></span> <span data-ttu-id="83370-129">Klicken Sie auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="83370-129">Click **Save**.</span></span>

    <span data-ttu-id="83370-130">Die neue App-V-Projektvorlage wird in dem in Schritt 3 dieser Vorgehensweise angegebenen Verzeichnis gespeichert.</span><span class="sxs-lookup"><span data-stu-id="83370-130">The new App-V project template is saved in the directory specified in step 3 of this procedure.</span></span>

## <span data-ttu-id="83370-131">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="83370-131">Related topics</span></span>


[<span data-ttu-id="83370-132">Aufgaben für Application Virtualization Sequencer (App-V 4.6 SP1)</span><span class="sxs-lookup"><span data-stu-id="83370-132">Tasks for the Application Virtualization Sequencer (App-V 4.6 SP1)</span></span>](tasks-for-the-application-virtualization-sequencer--app-v-46-sp1-.md)

[<span data-ttu-id="83370-133">So wenden Sie eine App-V-Projektvorlage (App-V 4.6 SP1) an</span><span class="sxs-lookup"><span data-stu-id="83370-133">How to Apply an App-V Project Template (App-V 4.6 SP1)</span></span>](how-to-apply-an-app-v-project-template--app-v-46-sp1-.md)

 

 





