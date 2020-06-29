---
title: So wenden Sie eine App-V-Projektvorlage (App-V 4.6 SP1) an
description: So wenden Sie eine App-V-Projektvorlage (App-V 4.6 SP1) an
author: dansimp
ms.assetid: 8ef120ab-8cfb-438c-8136-671167b7bd9d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5b5f04f3f31838bfb13c19eee5f2314c3a3d291f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808716"
---
# <span data-ttu-id="d416f-103">So wenden Sie eine App-V-Projektvorlage (App-V 4.6 SP1) an</span><span class="sxs-lookup"><span data-stu-id="d416f-103">How to Apply an App-V Project Template (App-V 4.6 SP1)</span></span>


<span data-ttu-id="d416f-104">Sie können eine App-V-Projektvorlage verwenden, um allgemeine Einstellungen, die einem vorhandenen virtuellen Anwendungspaket zugeordnet sind, einem neuen virtuellen Anwendungspaket zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="d416f-104">You can use an App-V project template to apply common settings associated with an existing virtual application package to a new virtual application package.</span></span> <span data-ttu-id="d416f-105">Mithilfe von App-V-Projektvorlagen können Sie den Prozess zum Erstellen von virtuellen Anwendungspaketen optimieren, indem Sie allgemeine Einstellungen konfigurieren, bevor Sie mit der Sequenzierung einer Anwendung beginnen.</span><span class="sxs-lookup"><span data-stu-id="d416f-105">Using App-V project templates can help streamline the process of creating virtual application packages by configuring common settings before you begin sequencing an application.</span></span>

<span data-ttu-id="d416f-106">**Hinweis**  Sie können nur dann eine App-V-Projektvorlage anwenden, wenn Sie ein neues virtuelles Anwendungspaket erstellen.</span><span class="sxs-lookup"><span data-stu-id="d416f-106">**Note** You can only apply an App-V project template when you are creating a new virtual application package.</span></span> <span data-ttu-id="d416f-107">Das Anwenden von Projektvorlagen auf vorhandene virtuelle Anwendungspakete wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d416f-107">Applying project templates to existing virtual application packages is not supported.</span></span> <span data-ttu-id="d416f-108">Darüber hinaus ist es nicht möglich, eine Projektvorlage in Verbindung mit einem Paket Beschleuniger zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="d416f-108">Additionally, you cannot use a project template in conjunction with a Package Accelerator.</span></span>

 

<span data-ttu-id="d416f-109">Weitere Informationen zum Erstellen von App-v-Projektvorlagen finden Sie unter [Erstellen einer APP-v-Projektvorlage (app-v 4,6 SP1)](how-to-create-an-app-v-project-template--app-v-46-sp1-.md).</span><span class="sxs-lookup"><span data-stu-id="d416f-109">For more information about creating App-V project templates, see [How to Create an App-V Project Template (App-V 4.6 SP1)](how-to-create-an-app-v-project-template--app-v-46-sp1-.md).</span></span>

**<span data-ttu-id="d416f-110">So wenden Sie eine App-V-Projektvorlage an</span><span class="sxs-lookup"><span data-stu-id="d416f-110">To apply an App-V project template</span></span>**

1.  <span data-ttu-id="d416f-111">Klicken Sie zum Starten des Microsoft Application Virtualization Sequencer auf dem Computer, auf dem App-V Sequencer installiert ist **Start**, auf  /  **Alle Programme**starten  /  **Microsoft Application Virtualization**  /  **Microsoft Application Virtualization Sequencer**.</span><span class="sxs-lookup"><span data-stu-id="d416f-111">To start the Microsoft Application Virtualization Sequencer, on the computer on which App-V Sequencer is installed, click **Start** / **All Programs** / **Microsoft Application Virtualization** / **Microsoft Application Virtualization Sequencer**.</span></span>

2.  <span data-ttu-id="d416f-112">Klicken Sie zum Erstellen eines neuen virtuellen Anwendungspakets mithilfe einer App-V-Projektvorlage auf **Datei**  /  **neu aus Vorlage**.</span><span class="sxs-lookup"><span data-stu-id="d416f-112">To create a new virtual application package by using an App-V project template, click **File** / **New From Template**.</span></span>

3.  <span data-ttu-id="d416f-113">Um die Projektvorlage auszuwählen, die Sie verwenden möchten, navigieren Sie zu dem Verzeichnis, in dem die Projektvorlage gespeichert ist, wählen Sie die Projektvorlage aus, und klicken Sie dann auf **Öffnen**.</span><span class="sxs-lookup"><span data-stu-id="d416f-113">To select the project template that you want to use, browse to the directory where the project template is saved, select the project template, and then click **Open**.</span></span>

4.  <span data-ttu-id="d416f-114">Erstellen Sie das neue virtuelle Anwendungspaket.</span><span class="sxs-lookup"><span data-stu-id="d416f-114">Create the new virtual application package.</span></span> <span data-ttu-id="d416f-115">Die mit der angegebenen Vorlage gespeicherten Einstellungen werden auf das neue virtuelle Anwendungspaket angewendet, das Sie erstellen.</span><span class="sxs-lookup"><span data-stu-id="d416f-115">The settings saved with the specified template will be applied to the new virtual application package that you are creating.</span></span> <span data-ttu-id="d416f-116">Weitere Informationen zum Erstellen eines neuen virtuellen Anwendungspakets finden Sie unter [So ermitteln Sie, welcher Typ von Anwendung für die Sequenz verwendet wird (App-V 4,6 SP1)](how-to-determine-which-type-of-application-to-sequence---app-v-46-sp1-.md), und wählen Sie die entsprechende Vorgehensweise aus.</span><span class="sxs-lookup"><span data-stu-id="d416f-116">For more information about creating a new virtual application package, see [How to Determine Which Type of Application to Sequence (App-V 4.6 SP1)](how-to-determine-which-type-of-application-to-sequence---app-v-46-sp1-.md), and select the appropriate procedure.</span></span>

## <span data-ttu-id="d416f-117">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="d416f-117">Related topics</span></span>


[<span data-ttu-id="d416f-118">Aufgaben für Application Virtualization Sequencer (App-V 4.6 SP1)</span><span class="sxs-lookup"><span data-stu-id="d416f-118">Tasks for the Application Virtualization Sequencer (App-V 4.6 SP1)</span></span>](tasks-for-the-application-virtualization-sequencer--app-v-46-sp1-.md)

[<span data-ttu-id="d416f-119">So erstellen Sie eine App-V-Projektvorlage (App-V 4.6 SP1)</span><span class="sxs-lookup"><span data-stu-id="d416f-119">How to Create an App-V Project Template (App-V 4.6 SP1)</span></span>](how-to-create-an-app-v-project-template--app-v-46-sp1-.md)

 

 





