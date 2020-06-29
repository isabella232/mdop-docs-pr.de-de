---
title: Seite „Package Accelerator auswählen“ (Weitere Informationen)
description: Seite „Package Accelerator auswählen“ (Weitere Informationen)
author: dansimp
ms.assetid: 2db51514-8695-4b5e-b3e5-1e96e3ee4cc7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d51df0f8eb16816bacf681b1acaf4c911ee9da55
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806371"
---
# <span data-ttu-id="16a9b-103">Seite „Package Accelerator auswählen“ (Weitere Informationen)</span><span class="sxs-lookup"><span data-stu-id="16a9b-103">Select Package Accelerator (Learn More) Page</span></span>


<span data-ttu-id="16a9b-104">Führen Sie nur Paket Beschleuniger von Herausgebern aus, denen Sie vertrauen.</span><span class="sxs-lookup"><span data-stu-id="16a9b-104">Only run Package Accelerators from publishers that you trust.</span></span> <span data-ttu-id="16a9b-105">Paket Beschleuniger beinhalten in der Regel eine digitale Signatur.</span><span class="sxs-lookup"><span data-stu-id="16a9b-105">Package Accelerators usually include a digital signature.</span></span> <span data-ttu-id="16a9b-106">Bei einer digitalen Signatur handelt es sich um ein elektronisches Sicherheitszeichen, mit dem der Herausgeber der Software angegeben werden kann, und dass das Paket nach der ursprünglichen Signatur des Transform-Pakets nicht manipuliert wurde.</span><span class="sxs-lookup"><span data-stu-id="16a9b-106">A digital signature is an electronic security mark that can help indicate the publisher of the software, and that the package has not been tampered with after the transform was originally signed.</span></span> <span data-ttu-id="16a9b-107">Wenn Sie eine Transform-Datenbank verwenden, die von einem Verleger digital signiert wurde und der Herausgeber seine Identität bei einer Zertifizierungsstelle überprüft hat, können Sie sicher sein, dass die Transformation von diesem bestimmten Herausgeber stammt und nicht geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="16a9b-107">If you use a transform that has been digitally signed by a publisher and the publisher has verified its identity with a certification authority, you can be more confident that the transform comes from that specific publisher and has not been altered.</span></span>

<span data-ttu-id="16a9b-108">Der Sequencer benachrichtigt Sie, wenn eine der folgenden Bedingungen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="16a9b-108">The sequencer notifies you if any of the following conditions are true:</span></span>

-   <span data-ttu-id="16a9b-109">Die ausgewählte Transformation wurde nicht digital signiert.</span><span class="sxs-lookup"><span data-stu-id="16a9b-109">The selected transform has not been digitally signed.</span></span>

-   <span data-ttu-id="16a9b-110">Die ausgewählte Transformation wird von einem Verleger signiert, dessen Identität bei einer Zertifizierungsstelle nicht überprüft wurde.</span><span class="sxs-lookup"><span data-stu-id="16a9b-110">The selected transform is signed by a publisher that has not verified its identity with a certification authority.</span></span>

-   <span data-ttu-id="16a9b-111">Die ausgewählte Transformation wurde geändert, nachdem Sie digital signiert und freigegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="16a9b-111">The selected transform has been altered after it was digitally signed and released.</span></span>

<span data-ttu-id="16a9b-112">Wenn eine dieser Nachrichten angezeigt wird, wenn Sie einen Paket Beschleuniger verwenden, besuchen Sie die Website des Paket Beschleunigers Publisher, um eine Digital signierte Version der Transformation abzurufen.</span><span class="sxs-lookup"><span data-stu-id="16a9b-112">If any of these messages are displayed when using a Package Accelerator, visit the Package Accelerators publisher’s website to get a digitally signed version of the transform.</span></span>

## <span data-ttu-id="16a9b-113">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="16a9b-113">Related topics</span></span>


[<span data-ttu-id="16a9b-114">Sequencer-Assistent - Package Accelerator (AppV 4.6 SP1)</span><span class="sxs-lookup"><span data-stu-id="16a9b-114">Sequencer Wizard - Package Accelerator (AppV 4.6 SP1)</span></span>](sequencer-wizard---package-accelerator--appv-46-sp1-.md)

 

 





