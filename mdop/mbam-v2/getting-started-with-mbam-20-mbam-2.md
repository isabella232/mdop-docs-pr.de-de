---
title: Erste Schritte mit MBAM 2.0
description: Erste Schritte mit MBAM 2.0
author: dansimp
ms.assetid: 29f5c9af-5bbf-4d37-aa0f-0716046904af
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 7c683e3d8718da24ebd2164328bda0dab0123037
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811281"
---
# <span data-ttu-id="e53f7-103">Erste Schritte mit MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="e53f7-103">Getting Started with MBAM 2.0</span></span>


<span data-ttu-id="e53f7-104">Microsoft BitLockerAdministration and Monitoring (MBAM) 2.0 erfordert eine gründliche Planung, bevor Sie es bereitstellen oder seine Funktionen verwenden.</span><span class="sxs-lookup"><span data-stu-id="e53f7-104">Microsoft BitLockerAdministration and Monitoring(MBAM)2.0 requires thorough planning before you deploy it or use its features.</span></span> <span data-ttu-id="e53f7-105">Da sich dieses Produkt auf alle Computer in Ihrer Organisation auswirken kann, können Sie Ihr gesamtes Netzwerk stören, wenn Sie die Bereitstellung nicht sorgfältig planen.</span><span class="sxs-lookup"><span data-stu-id="e53f7-105">Because this product can affect every computer in your organization, you might disrupt your entire network if you do not plan your deployment carefully.</span></span> <span data-ttu-id="e53f7-106">Wenn Sie Ihre Bereitstellung jedoch sorgfältig planen und verwalten, damit Sie Ihren geschäftlichen Anforderungen entspricht, können Sie mithilfe von BitLockerAdministration und Monitoring 2.0 den Verwaltungsaufwand und die Gesamtbetriebskosten reduzieren.</span><span class="sxs-lookup"><span data-stu-id="e53f7-106">However, if you plan your deployment carefully and manage it so that it meets your business requirements, BitLockerAdministration and Monitoring2.0 can help reduce your administrative overhead and total cost of ownership.</span></span>

<span data-ttu-id="e53f7-107">Wenn Sie mit diesem Produkt noch nicht vertraut sind, empfehlen wir Ihnen, die Dokumentation sorgfältig zu lesen.</span><span class="sxs-lookup"><span data-stu-id="e53f7-107">If you are new to this product, we recommend that you read the documentation carefully.</span></span> <span data-ttu-id="e53f7-108">Informationen zum Abrufen der MBAM-Software finden Sie unter [wie erhalte ich MDOP?](https://go.microsoft.com/fwlink/p/?LinkId=322049).</span><span class="sxs-lookup"><span data-stu-id="e53f7-108">To get the MBAM software, see [How Do I Get MDOP?](https://go.microsoft.com/fwlink/p/?LinkId=322049).</span></span> <span data-ttu-id="e53f7-109">Bevor Sie MBAM in einer Produktionsumgebung bereitstellen, empfehlen wir außerdem, den Bereitstellungsplan in einer Testumgebung zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="e53f7-109">Before you deploy MBAM to a production environment, we also recommend that you validate your deployment plan in a test environment.</span></span> <span data-ttu-id="e53f7-110">Sie können auch erwägen, eine Klasse über relevante Technologien zu Unternehmen.</span><span class="sxs-lookup"><span data-stu-id="e53f7-110">You might also consider taking a class about relevant technologies.</span></span> <span data-ttu-id="e53f7-111">Weitere Informationen zu Microsoft-Schulungsmöglichkeiten finden Sie in der Microsoft-Schulungsübersicht unter <https://go.microsoft.com/fwlink/p/?LinkId=80347> .</span><span class="sxs-lookup"><span data-stu-id="e53f7-111">For more information about Microsoft training opportunities, see the Microsoft Training Overview at <https://go.microsoft.com/fwlink/p/?LinkId=80347>.</span></span>

<span data-ttu-id="e53f7-112">Dieser Abschnitt des mbam 2.0-Administrator Handbuchs enthält allgemeine Informationen zu mbam 2.0, um ein grundlegendes Verständnis des Produkts bereitzustellen, bevor Sie mit der Planung der Bereitstellung beginnen.</span><span class="sxs-lookup"><span data-stu-id="e53f7-112">This section of the MBAM2.0 Administrator’s Guide includes high-level information about MBAM2.0 to provide a basic understanding of the product before you begin to plan deployment.</span></span> <span data-ttu-id="e53f7-113">Spezifische Informationen zum Bereitstellen von MBAM mit der integrierten Configuration Manager-Topologie finden Sie unter [Verwenden von MBAM mit Configuration Manager](using-mbam-with-configuration-manager.md).</span><span class="sxs-lookup"><span data-stu-id="e53f7-113">For specific information about deploying MBAM with the Configuration Manager integrated topology, see [Using MBAM with Configuration Manager](using-mbam-with-configuration-manager.md).</span></span> <span data-ttu-id="e53f7-114">Weitere MBAM-Dokumentation finden Sie auf der Microsoft BitLocker-Dokumentation Resources-Download Seite unter <https://go.microsoft.com/fwlink/p/?LinkId=258391> .</span><span class="sxs-lookup"><span data-stu-id="e53f7-114">You can find additional MBAM documentation on the Microsoft BitLocker Administration and Monitoring (MBAM) Documentation Resources Download Page at <https://go.microsoft.com/fwlink/p/?LinkId=258391>.</span></span>

## <span data-ttu-id="e53f7-115">Erste Schritte mit mbam 2.0</span><span class="sxs-lookup"><span data-stu-id="e53f7-115">Getting Started with MBAM2.0</span></span>


-   [<span data-ttu-id="e53f7-116">Informationen zu MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="e53f7-116">About MBAM 2.0</span></span>](about-mbam-20-mbam-2.md)

    <span data-ttu-id="e53f7-117">Bietet eine allgemeine Übersicht über mbam 2.0 und beschreibt, wie es in Ihrer Organisation verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="e53f7-117">Provides a high-level overview of MBAM2.0 and describes how it can be used in your organization.</span></span>

-   [<span data-ttu-id="e53f7-118">Auswerten von MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="e53f7-118">Evaluating MBAM 2.0</span></span>](evaluating-mbam-20-mbam-2.md)

    <span data-ttu-id="e53f7-119">Bietet Informationen dazu, wie Sie mbam 2.0 für die Verwendung in Ihrer Organisation am besten auswerten können.</span><span class="sxs-lookup"><span data-stu-id="e53f7-119">Provides information about how you can best evaluate MBAM2.0 for use in your organization.</span></span>

-   [<span data-ttu-id="e53f7-120">High-Level-Architektur für MBAM2.0</span><span class="sxs-lookup"><span data-stu-id="e53f7-120">High-Level Architecture for MBAM 2.0</span></span>](high-level-architecture-for-mbam-20-mbam-2.md)

    <span data-ttu-id="e53f7-121">Beschreibt die mbam 2.0-Features und die empfohlene Architektur für eine Produktionsumgebung.</span><span class="sxs-lookup"><span data-stu-id="e53f7-121">Describes the MBAM2.0 features and the recommended architecture for a production environment.</span></span>

-   [<span data-ttu-id="e53f7-122">Barrierefreiheit von MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="e53f7-122">Accessibility for MBAM 2.0</span></span>](accessibility-for-mbam-20-mbam-2.md)

    <span data-ttu-id="e53f7-123">Beschreibt die Tastenkombinationen, die für mbam 2.0 verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="e53f7-123">Describes the keyboard shortcuts that are available for MBAM2.0.</span></span>

## <a href="" id="other-resources-for-this-product-"></a><span data-ttu-id="e53f7-124">Weitere Ressourcen für dieses Produkt</span><span class="sxs-lookup"><span data-stu-id="e53f7-124">Other Resources for this Product</span></span>


[<span data-ttu-id="e53f7-125">Administrator Handbuch für Microsoft BitLocker-Verwaltung und-Überwachung 2</span><span class="sxs-lookup"><span data-stu-id="e53f7-125">Microsoft BitLocker Administration and Monitoring 2 Administrator's Guide</span></span>](index.md)

[<span data-ttu-id="e53f7-126">Planen von MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="e53f7-126">Planning for MBAM 2.0</span></span>](planning-for-mbam-20-mbam-2.md)

[<span data-ttu-id="e53f7-127">Bereitstellen von MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="e53f7-127">Deploying MBAM 2.0</span></span>](deploying-mbam-20-mbam-2.md)

[<span data-ttu-id="e53f7-128">Vorgänge für MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="e53f7-128">Operations for MBAM 2.0</span></span>](operations-for-mbam-20-mbam-2.md)

[<span data-ttu-id="e53f7-129">Problembehandlung bei MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="e53f7-129">Troubleshooting MBAM 2.0</span></span>](troubleshooting-mbam-20-mbam-2.md)

 

 





