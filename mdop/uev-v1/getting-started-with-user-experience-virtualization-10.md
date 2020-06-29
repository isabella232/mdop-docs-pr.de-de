---
title: Erste Schritte mit User Experience Virtualization 1.0
description: Erste Schritte mit User Experience Virtualization 1.0
author: dansimp
ms.assetid: 74a068dc-4f87-4cb4-b114-8ca2a37149f7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 010cefc42c8f2d65ac7f815eff51ec2df42df4d0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812163"
---
# <span data-ttu-id="f6051-103">Erste Schritte mit User Experience Virtualization 1.0</span><span class="sxs-lookup"><span data-stu-id="f6051-103">Getting Started With User Experience Virtualization 1.0</span></span>


<span data-ttu-id="f6051-104">Microsoft User Experience Virtualization (UE-V) erfasst und zentralisiert Anwendungseinstellungen und Windows-Betriebssystemeinstellungen für den Benutzer.</span><span class="sxs-lookup"><span data-stu-id="f6051-104">Microsoft User Experience Virtualization (UE-V) captures and centralizes application settings and Windows operating system settings for the user.</span></span> <span data-ttu-id="f6051-105">Diese Einstellungen werden dann auf die verschiedenen Computer angewendet, auf die der Benutzer zugreifen kann, einschließlich Desktopcomputern, Laptopcomputern und VDI-Sitzungen (Virtual Desktop Infrastructure).</span><span class="sxs-lookup"><span data-stu-id="f6051-105">These settings are then applied to the different computers that are accessed by the user, including desktop computers, laptop computers, and virtual desktop infrastructure (VDI) sessions.</span></span>

<span data-ttu-id="f6051-106">UE-V bietet die Synchronisierung von Einstellungen für allgemeine Microsoft-Anwendungen und Windows-Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="f6051-106">UE-V offers settings synchronization for common Microsoft applications and Windows settings.</span></span> <span data-ttu-id="f6051-107">Darüber hinaus werden Benutzereinstellungen jederzeit an alle Benutzer übermittelt, die im gesamten Unternehmen arbeiten.</span><span class="sxs-lookup"><span data-stu-id="f6051-107">It also delivers user settings at any time to wherever users work throughout the enterprise.</span></span> <span data-ttu-id="f6051-108">Mit UE-V können Administratoren angeben, welche Anwendungseinstellungen und Windows-Einstellungen durchlaufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="f6051-108">UE-V allows administrators to specify which application settings and Windows settings roam.</span></span> <span data-ttu-id="f6051-109">UE-V unterstützt Administratoren beim Erstellen benutzerdefinierter Einstellungen für Standort Vorlagen für Drittanbieter-oder Branchenanwendungen, die im Unternehmen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f6051-109">UE-V helps administrators to create custom settings location templates for third-party or line-of-business applications that are used in the enterprise.</span></span>

<span data-ttu-id="f6051-110">Die Virtualisierung der Benutzeroberfläche bietet eine erweiterte Benutzerstatus-Virtualisierung.</span><span class="sxs-lookup"><span data-stu-id="f6051-110">User Experience Virtualization delivers an enhanced user state virtualization experience.</span></span> <span data-ttu-id="f6051-111">Sie bietet eine konsistente Personalisierung der Benutzereinstellungen in den folgenden Szenarien:</span><span class="sxs-lookup"><span data-stu-id="f6051-111">It provides consistent personalization of the user’s settings in the following scenarios:</span></span>

-   <span data-ttu-id="f6051-112">Roaming-Benutzeranwendung und Windows-Einstellungen zwischen Computern.</span><span class="sxs-lookup"><span data-stu-id="f6051-112">Roaming user application and Windows settings between computers.</span></span>

-   <span data-ttu-id="f6051-113">Roaming-Benutzereinstellungen zwischen den Instanzen einer Anwendung, die mithilfe verschiedener Methoden bereitgestellt werden:</span><span class="sxs-lookup"><span data-stu-id="f6051-113">Roaming user settings between the instances of an application that are deployed by using different methods:</span></span>

    -   <span data-ttu-id="f6051-114">Installierte Anwendungen</span><span class="sxs-lookup"><span data-stu-id="f6051-114">Installed applications</span></span>

    -   <span data-ttu-id="f6051-115">Application Virtualization (App-V)-sequenzierte Anwendungen</span><span class="sxs-lookup"><span data-stu-id="f6051-115">Application Virtualization (App-V) sequenced applications</span></span>

    -   <span data-ttu-id="f6051-116">RemoteApp-Anwendungen (Remote Desktop-Virtualisierung)</span><span class="sxs-lookup"><span data-stu-id="f6051-116">RemoteApp (Remote Desktop Virtualization) applications</span></span>

-   <span data-ttu-id="f6051-117">Wiederherstellen von Einstellungen für einen Computer nach dem Austausch, dem Hardware Upgrade oder dem reimage.</span><span class="sxs-lookup"><span data-stu-id="f6051-117">Recovering settings for a computer after replacement, hardware upgrade, or reimage.</span></span>

<span data-ttu-id="f6051-118">Dieses Produkt erfordert eine gründliche Planung, bevor Sie es bereitstellen oder seine Funktionen verwenden.</span><span class="sxs-lookup"><span data-stu-id="f6051-118">This product requires thorough planning before you deploy it or use its features.</span></span> <span data-ttu-id="f6051-119">Da sich dieses Produkt auf alle Computer in Ihrer Organisation auswirken kann, können Sie Ihr gesamtes Netzwerk stören, wenn Sie die Bereitstellung nicht sorgfältig planen.</span><span class="sxs-lookup"><span data-stu-id="f6051-119">Because this product can affect every computer in your organization, you might disrupt your entire network if you do not plan your deployment carefully.</span></span> <span data-ttu-id="f6051-120">Wenn Sie Ihre Bereitstellung aber sorgfältig planen und verwalten, damit Sie Ihren geschäftlichen Anforderungen entspricht, kann dieses Produkt dazu beitragen, den Verwaltungsaufwand und die Gesamtbetriebskosten zu reduzieren.</span><span class="sxs-lookup"><span data-stu-id="f6051-120">However, if you plan your deployment carefully and manage it so that it meets your business needs, this product can help reduce your administrative overhead and total cost of ownership.</span></span>

<span data-ttu-id="f6051-121">Wenn Sie mit diesem Produkt noch nicht vertraut sind, empfehlen wir Ihnen, die Dokumentation sorgfältig zu lesen.</span><span class="sxs-lookup"><span data-stu-id="f6051-121">If you are new to this product, we recommend that you read the documentation carefully.</span></span> <span data-ttu-id="f6051-122">Bevor Sie das Produkt in einer Produktionsumgebung bereitstellen, empfehlen wir außerdem, den Bereitstellungsplan in einer Testnetzwerkumgebung zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="f6051-122">Before you deploy the product to a production environment, we also recommend that you validate your deployment plan in a test network environment.</span></span> <span data-ttu-id="f6051-123">Sie können auch erwägen, eine Klasse über relevante Technologien zu Unternehmen.</span><span class="sxs-lookup"><span data-stu-id="f6051-123">You might also consider taking a class about relevant technologies.</span></span> <span data-ttu-id="f6051-124">Weitere Informationen zu Microsoft-Schulungsmöglichkeiten finden Sie in der Microsoft-Schulungsübersicht unter <https://go.microsoft.com/fwlink/p/?LinkId=80347> .</span><span class="sxs-lookup"><span data-stu-id="f6051-124">For more information about Microsoft training opportunities, see the Microsoft Training Overview at <https://go.microsoft.com/fwlink/p/?LinkId=80347>.</span></span>

<span data-ttu-id="f6051-125">**Hinweis**  Eine herunterladbare Version des Administratorhandbuchs steht nicht zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="f6051-125">**Note** A downloadable version of this administrator’s guide is not available.</span></span> <span data-ttu-id="f6051-126">Sie können sich jedoch mit einem speziellen Modus der TechNet-Bibliothek vertraut machen, der es Ihnen ermöglicht, Artikel auszuwählen, Sie in einer Sammlung zu gruppieren, zu drucken oder in eine Datei unter (zu exportieren <https://go.microsoft.com/fwlink/?LinkId=272497> https://go.microsoft.com/fwlink/?LinkId=272497) .</span><span class="sxs-lookup"><span data-stu-id="f6051-126">However, you can learn about a special mode of the TechNet Library that allows you to select articles, group them in a collection, and print them or export them to a file at <https://go.microsoft.com/fwlink/?LinkId=272497> (https://go.microsoft.com/fwlink/?LinkId=272497).</span></span>

 

## <span data-ttu-id="f6051-127">Erste Schritte mit Microsoft User Experience Virtualization-Themen</span><span class="sxs-lookup"><span data-stu-id="f6051-127">Getting started with Microsoft User Experience Virtualization topics</span></span>


-   [<span data-ttu-id="f6051-128">Informationen zu User Experience Virtualization 1.0</span><span class="sxs-lookup"><span data-stu-id="f6051-128">About User Experience Virtualization 1.0</span></span>](about-user-experience-virtualization-10.md)

    <span data-ttu-id="f6051-129">Beschreibt die Funktionen und Features der Benutzeroberflächen-Virtualisierung.</span><span class="sxs-lookup"><span data-stu-id="f6051-129">Describes the functionality and features of User Experience Virtualization.</span></span>

-   [<span data-ttu-id="f6051-130">High-Level-Architektur für UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="f6051-130">High-Level Architecture for UE-V 1.0</span></span>](high-level-architecture-for-ue-v-10.md)

    <span data-ttu-id="f6051-131">Erläutert die Features der Benutzeroberflächen-Virtualisierung.</span><span class="sxs-lookup"><span data-stu-id="f6051-131">Explains the features of User Experience Virtualization.</span></span>

-   [<span data-ttu-id="f6051-132">Versionshinweise zu Microsoft User Experience Virtualization (UE-V) 1.0</span><span class="sxs-lookup"><span data-stu-id="f6051-132">Microsoft User Experience Virtualization (UE-V) 1.0 Release Notes</span></span>](microsoft-user-experience-virtualization--ue-v--10-release-notes.md)

    <span data-ttu-id="f6051-133">Beschreibt die bekannten Probleme bei UE-V.</span><span class="sxs-lookup"><span data-stu-id="f6051-133">Describes the known issues for UE-V.</span></span>

-   [<span data-ttu-id="f6051-134">Eingabehilfen für UE-V</span><span class="sxs-lookup"><span data-stu-id="f6051-134">Accessibility for UE-V</span></span>](accessibility-for-ue-v.md)

    <span data-ttu-id="f6051-135">Beschreibt die Tastenkombinationen und Informationen zur Barrierefreiheit für UE-V.</span><span class="sxs-lookup"><span data-stu-id="f6051-135">Describes the keyboard shortcuts and accessibility information for UE-V.</span></span>

## <span data-ttu-id="f6051-136">Weitere Ressourcen für dieses Produkt</span><span class="sxs-lookup"><span data-stu-id="f6051-136">Other resources for this product</span></span>


-   [<span data-ttu-id="f6051-137">Microsoft-User Experience Virtualization (UE-V) 1.0</span><span class="sxs-lookup"><span data-stu-id="f6051-137">Microsoft User Experience Virtualization (UE-V) 1.0</span></span>](index.md)

-   [<span data-ttu-id="f6051-138">Planen für UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="f6051-138">Planning for UE-V 1.0</span></span>](planning-for-ue-v-10.md)

-   [<span data-ttu-id="f6051-139">Bereitstellen von UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="f6051-139">Deploying UE-V 1.0</span></span>](deploying-ue-v-10.md)

-   [<span data-ttu-id="f6051-140">Vorgänge für UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="f6051-140">Operations for UE-V 1.0</span></span>](operations-for-ue-v-10.md)

-   [<span data-ttu-id="f6051-141">Problembehandlung für UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="f6051-141">Troubleshooting UE-V 1.0</span></span>](troubleshooting-ue-v-10.md)

 

 





