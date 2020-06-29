---
title: Erste Schritte mit MBAM 1.0
description: Erste Schritte mit MBAM 1.0
author: dansimp
ms.assetid: 4fab4e4a-d25e-4661-b235-2b45bf5ac3e4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: e0bbbcabfb25cfc8b24cbb4cbc3d344d4e7f209b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811056"
---
# <span data-ttu-id="98041-103">Erste Schritte mit MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="98041-103">Getting Started with MBAM 1.0</span></span>

> <span data-ttu-id="98041-104">**Wichtig** MBAM 1,0 wird am Ende des Supports am 14. September 2021.</span><span class="sxs-lookup"><span data-stu-id="98041-104">**IMPORTANT** MBAM 1.0 will reach end of support on September 14, 2021.</span></span> 
> <span data-ttu-id="98041-105">Weitere Informationen finden Sie auf unserer [Lebenszyklus-Seite](https://support.microsoft.com/lifecycle/search?alpha=Microsoft%20BitLocker%20Administration%20and%20Monitoring%201.0) .</span><span class="sxs-lookup"><span data-stu-id="98041-105">See our [lifecycle page](https://support.microsoft.com/lifecycle/search?alpha=Microsoft%20BitLocker%20Administration%20and%20Monitoring%201.0) for more information.</span></span> <span data-ttu-id="98041-106">Es wird empfohlen, [auf MBAM 2,5](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/upgrading-to-mbam-25-or-mbam-25-sp1-from-previous-versions) oder eine andere unterstützte Version von MBAM zu migrieren oder ihre BitLocker-Verwaltung zu [Microsoft Endpoint Manager](https://www.microsoft.com/microsoft-365/microsoft-endpoint-manager)zu migrieren.</span><span class="sxs-lookup"><span data-stu-id="98041-106">We recommend [migrating to MBAM 2.5](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/upgrading-to-mbam-25-or-mbam-25-sp1-from-previous-versions) or another supported version of MBAM, or migrating your BitLocker management to [Microsoft Endpoint Manager](https://www.microsoft.com/microsoft-365/microsoft-endpoint-manager).</span></span>


<span data-ttu-id="98041-107">Die Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) erfordert eine gründliche Planung, bevor Sie Sie bereitstellen oder deren Funktionen verwenden.</span><span class="sxs-lookup"><span data-stu-id="98041-107">Microsoft BitLocker Administration and Monitoring (MBAM) requires thorough planning before you deploy it or use its features.</span></span> <span data-ttu-id="98041-108">Da sich dieses Produkt auf alle Computer in Ihrer Organisation auswirken kann, können Sie Ihr gesamtes Netzwerk stören, wenn Sie die Bereitstellung nicht sorgfältig planen.</span><span class="sxs-lookup"><span data-stu-id="98041-108">Because this product can affect every computer in your organization, you might disrupt your entire network if you do not plan your deployment carefully.</span></span> <span data-ttu-id="98041-109">Wenn Sie Ihre Bereitstellung jedoch sorgfältig planen und verwalten, damit Sie Ihren geschäftlichen Anforderungen entspricht, kann MBAM dazu beitragen, den Verwaltungsaufwand und die Gesamtbetriebskosten zu reduzieren.</span><span class="sxs-lookup"><span data-stu-id="98041-109">However, if you plan your deployment carefully and manage it so that it meets your business needs, MBAM can help reduce your administrative overhead and total cost of ownership.</span></span>

<span data-ttu-id="98041-110">Wenn Sie mit diesem Produkt noch nicht vertraut sind, empfehlen wir Ihnen, die Dokumentation gründlich zu lesen.</span><span class="sxs-lookup"><span data-stu-id="98041-110">If you are new to this product, we recommend that you read the documentation thoroughly.</span></span> <span data-ttu-id="98041-111">Bevor Sie die Anwendung in einer Produktionsumgebung bereitstellen, empfehlen wir auch, den Bereitstellungsplan in einer Testnetzwerkumgebung zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="98041-111">Before you deploy it to a production environment, we also recommend that you validate your deployment plan in a test network environment.</span></span> <span data-ttu-id="98041-112">Sie können auch erwägen, eine Klasse über relevante Technologien zu Unternehmen.</span><span class="sxs-lookup"><span data-stu-id="98041-112">You might also consider taking a class about relevant technologies.</span></span> <span data-ttu-id="98041-113">Weitere Informationen zu Microsoft-Schulungsmöglichkeiten finden Sie in der Microsoft-Schulungsübersicht unter <https://go.microsoft.com/fwlink/p/?LinkId=80347> .</span><span class="sxs-lookup"><span data-stu-id="98041-113">For more information about Microsoft training opportunities, see the Microsoft Training Overview at <https://go.microsoft.com/fwlink/p/?LinkId=80347>.</span></span>

<span data-ttu-id="98041-114">**Hinweis**  Eine herunterladbare Version dieser Dokumentation und das MBAM-Evaluierungshandbuch finden Sie unter <https://go.microsoft.com/fwlink/p/?LinkId=225356> .</span><span class="sxs-lookup"><span data-stu-id="98041-114">**Note** You can find a downloadable version of this documentation and the MBAM Evaluation Guide at <https://go.microsoft.com/fwlink/p/?LinkId=225356>.</span></span>

 

<span data-ttu-id="98041-115">Dieser Abschnitt des MBAM-Administrator Handbuchs enthält allgemeine Informationen zu MBAM, um Ihnen ein grundlegendes Verständnis des Produkts zu vermitteln, bevor Sie mit der Bereitstellungsplanung beginnen.</span><span class="sxs-lookup"><span data-stu-id="98041-115">This section of the MBAM Administrator’s Guide includes high-level information about MBAM to provide you with a basic understanding of the product before you begin the deployment planning.</span></span> <span data-ttu-id="98041-116">Weitere MBAM-Dokumentation finden Sie auf der Seite MBAM Documentation Resources Download unter <https://go.microsoft.com/fwlink/p/?LinkId=258391> .</span><span class="sxs-lookup"><span data-stu-id="98041-116">Additional MBAM documentation can be found on the MBAM Documentation Resources Download page at <https://go.microsoft.com/fwlink/p/?LinkId=258391>.</span></span>

## <span data-ttu-id="98041-117">Erste Schritte mit MBAM 1,0</span><span class="sxs-lookup"><span data-stu-id="98041-117">Getting started with MBAM 1.0</span></span>


-   [<span data-ttu-id="98041-118">Informationen zu MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="98041-118">About MBAM 1.0</span></span>](about-mbam-10.md)

    <span data-ttu-id="98041-119">Bietet eine allgemeine Übersicht über MBAM und die Art und Weise, wie es in Ihrer Organisation verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="98041-119">Provides a high-level overview of MBAM and how it can be used in your organization.</span></span>

-   [<span data-ttu-id="98041-120">Auswerten von MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="98041-120">Evaluating MBAM 1.0</span></span>](evaluating-mbam-10.md)

    <span data-ttu-id="98041-121">Bietet Informationen dazu, wie Sie MBAM für die Verwendung in Ihrer Organisation am besten auswerten können.</span><span class="sxs-lookup"><span data-stu-id="98041-121">Provides information about how you can best evaluate MBAM for use in your organization.</span></span>

-   [<span data-ttu-id="98041-122">High-Level-Architektur für MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="98041-122">High Level Architecture for MBAM 1.0</span></span>](high-level-architecture-for-mbam-10.md)

    <span data-ttu-id="98041-123">Enthält eine Beschreibung der MBAM-Features und ihrer Zusammenarbeit.</span><span class="sxs-lookup"><span data-stu-id="98041-123">Provides a description of the MBAM features and how they work together.</span></span>

-   [<span data-ttu-id="98041-124">Barrierefreiheit von MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="98041-124">Accessibility for MBAM 1.0</span></span>](accessibility-for-mbam-10.md)

    <span data-ttu-id="98041-125">Bietet Informationen zu Features und Diensten, mit denen dieses Produkt und die zugehörige Dokumentation für Personen mit Behinderungen barrierefreier sind.</span><span class="sxs-lookup"><span data-stu-id="98041-125">Provides information about features and services that make this product and its corresponding documentation more accessible for people with disabilities.</span></span>

## <a href="" id="other-resources-for-this-product-"></a><span data-ttu-id="98041-126">Weitere Ressourcen für dieses Produkt</span><span class="sxs-lookup"><span data-stu-id="98041-126">Other resources for this product</span></span>


-   [<span data-ttu-id="98041-127">Administrator Handbuch für Microsoft BitLocker-Verwaltung und-Überwachung 1</span><span class="sxs-lookup"><span data-stu-id="98041-127">Microsoft BitLocker Administration and Monitoring 1 Administrator's Guide</span></span>](index.md)

-   [<span data-ttu-id="98041-128">Planen von MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="98041-128">Planning for MBAM 1.0</span></span>](planning-for-mbam-10.md)

-   [<span data-ttu-id="98041-129">Bereitstellen von MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="98041-129">Deploying MBAM 1.0</span></span>](deploying-mbam-10.md)

-   [<span data-ttu-id="98041-130">Vorgänge für MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="98041-130">Operations for MBAM 1.0</span></span>](operations-for-mbam-10.md)

-   [<span data-ttu-id="98041-131">Problembehandlung bei MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="98041-131">Troubleshooting MBAM 1.0</span></span>](troubleshooting-mbam-10.md)

 

 





