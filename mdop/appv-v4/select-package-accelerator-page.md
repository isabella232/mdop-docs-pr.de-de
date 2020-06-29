---
title: Seite „Package Accelerator auswählen“
description: Seite „Package Accelerator auswählen“
author: dansimp
ms.assetid: 865c2702-4dfd-41ae-8cfc-3514d5f41f76
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a5723f8244563539c27a3fa915c1a680905e61e9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806368"
---
# <span data-ttu-id="04bbe-103">Seite „Package Accelerator auswählen“</span><span class="sxs-lookup"><span data-stu-id="04bbe-103">Select Package Accelerator Page</span></span>


<span data-ttu-id="04bbe-104">Auf der Seite **Paket Beschleuniger auswählen** können Sie den Paket Beschleuniger auswählen, der zum Erstellen des neuen virtuellen Anwendungspakets verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="04bbe-104">Use the **Select Package Accelerator** page to select the Package Accelerator that will be used to create the new virtual application package.</span></span> <span data-ttu-id="04bbe-105">Sie müssen den Paket Beschleuniger in einen Ordner auf dem Computer kopieren, auf dem der App-V-Sequencer ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="04bbe-105">You must copy the Package Accelerator to a folder on the computer running the App-V Sequencer.</span></span> <span data-ttu-id="04bbe-106">Weitere Informationen finden Sie unter [Informationen zu app-v-Paket Beschleunigern (app-v 4,6 SP1)](about-app-v-package-accelerators--app-v-46-sp1-.md).</span><span class="sxs-lookup"><span data-stu-id="04bbe-106">For more information, see [About App-V Package Accelerators (App-V 4.6 SP1)](about-app-v-package-accelerators--app-v-46-sp1-.md).</span></span>

<span data-ttu-id="04bbe-107">Führen Sie nur Paket Beschleuniger von Herausgebern aus, denen Sie vertrauen.</span><span class="sxs-lookup"><span data-stu-id="04bbe-107">Only run Package Accelerators from publishers that you trust.</span></span> <span data-ttu-id="04bbe-108">Paket Beschleuniger beinhalten in der Regel eine digitale Signatur.</span><span class="sxs-lookup"><span data-stu-id="04bbe-108">Package Accelerators usually include a digital signature.</span></span> <span data-ttu-id="04bbe-109">Bei einer digitalen Signatur handelt es sich um ein elektronisches Sicherheitszeichen, das den Herausgeber der Software kennzeichnet und angibt, ob das Paket manipuliert wurde, nachdem die Transformation ursprünglich signiert wurde.</span><span class="sxs-lookup"><span data-stu-id="04bbe-109">A digital signature is an electronic security mark that can help indicate the publisher of the software, and whether the package has been tampered with after the transform was originally signed.</span></span> <span data-ttu-id="04bbe-110">Wenn Sie eine Transform-Datenbank verwenden, die von einem Verleger digital signiert wurde und der Herausgeber seine Identität bei einer Zertifizierungsstelle überprüft hat, können Sie sicher sein, dass die Transformation von diesem bestimmten Herausgeber stammt und nicht geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="04bbe-110">If you use a transform that has been digitally signed by a publisher and the publisher has verified its identity with a certification authority, you can be more confident that the transform comes from that specific publisher and has not been altered.</span></span>

<span data-ttu-id="04bbe-111">Der App-V-Sequenzer benachrichtigt Sie, wenn eine der folgenden Bedingungen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="04bbe-111">The App-V Sequencer notifies you if any of the following conditions are true:</span></span>

-   <span data-ttu-id="04bbe-112">Die ausgewählte Transformation wurde nicht digital signiert.</span><span class="sxs-lookup"><span data-stu-id="04bbe-112">The selected transform has not been digitally signed.</span></span>

-   <span data-ttu-id="04bbe-113">Die ausgewählte Transformation wird von einem Verleger signiert, dessen Identität bei einer Zertifizierungsstelle nicht überprüft wurde.</span><span class="sxs-lookup"><span data-stu-id="04bbe-113">The selected transform is signed by a publisher that has not verified its identity with a certification authority.</span></span>

-   <span data-ttu-id="04bbe-114">Die ausgewählte Transformation wurde geändert, nachdem Sie digital signiert und freigegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="04bbe-114">The selected transform has been altered after it was digitally signed and released.</span></span>

<span data-ttu-id="04bbe-115">Wenn eine dieser Nachrichten angezeigt wird, wenn Sie eine Paket Beschleuniger verwenden, besuchen Sie die Website des Paket Beschleunigers Publisher, um eine Digital signierte Version der Transformation abzurufen.</span><span class="sxs-lookup"><span data-stu-id="04bbe-115">If any of these messages are displayed when using a Package Accelerators, visit the Package Accelerators publisher’s website to get a digitally signed version of the transform.</span></span>

<span data-ttu-id="04bbe-116">Diese Seite enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="04bbe-116">This page contains the following elements:</span></span>

<a href="" id="browse"></a>**<span data-ttu-id="04bbe-117">Durchsuchen</span><span class="sxs-lookup"><span data-stu-id="04bbe-117">Browse</span></span>**  
<span data-ttu-id="04bbe-118">Klicken Sie auf **Durchsuchen** , um den Paket Beschleuniger anzugeben, den Sie zum Erstellen des virtuellen Anwendungspakets verwenden werden.</span><span class="sxs-lookup"><span data-stu-id="04bbe-118">Click **Browse** to specify the Package Accelerator that you will use to create the virtual application package.</span></span> <span data-ttu-id="04bbe-119">Speichern Sie den von Ihnen festgelegten Paket Beschleuniger lokal auf dem Computer, auf dem der Sequencer ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="04bbe-119">Save the Package Accelerator you specified locally on the computer that is running the Sequencer.</span></span>

## <span data-ttu-id="04bbe-120">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="04bbe-120">Related topics</span></span>


[<span data-ttu-id="04bbe-121">Sequencer-Assistent - Package Accelerator (AppV 4.6 SP1)</span><span class="sxs-lookup"><span data-stu-id="04bbe-121">Sequencer Wizard - Package Accelerator (AppV 4.6 SP1)</span></span>](sequencer-wizard---package-accelerator--appv-46-sp1-.md)

 

 





