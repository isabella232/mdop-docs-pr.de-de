---
title: App-V 4.6 SP3 – Versionshinweise
description: App-V 4.6 SP3 – Versionshinweise
author: dansimp
ms.assetid: 206fadeb-59cc-47b4-836f-191ab1c27ff8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: dd0b82c5e12cbe161066a7f4a4e0932cb92cca42
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808048"
---
# <span data-ttu-id="8a935-103">App-V 4.6 SP3 – Versionshinweise</span><span class="sxs-lookup"><span data-stu-id="8a935-103">App-V 4.6 SP3 Release Notes</span></span>


<span data-ttu-id="8a935-104">Drücken Sie STRG + F, um diese Versionshinweise zu durchsuchen.</span><span class="sxs-lookup"><span data-stu-id="8a935-104">To search these Release Notes, press CTRL+F.</span></span>

<span data-ttu-id="8a935-105">Lesen Sie diese Versionshinweise gründlich, bevor Sie das Microsoft Application Virtualization (App-V)-Verwaltungs System installieren.</span><span class="sxs-lookup"><span data-stu-id="8a935-105">Read these Release Notes thoroughly before you install the Microsoft Application Virtualization (App-V) Management System.</span></span> <span data-ttu-id="8a935-106">Diese Anmerkungen zu dieser Version enthalten Informationen, die Ihnen bei der erfolgreichen Installation von Application Virtualization (App-V) 4.6 SP3 helfen.</span><span class="sxs-lookup"><span data-stu-id="8a935-106">These Release Notes contain information that helps you successfully install Application Virtualization (App-V)4.6 SP3.</span></span> <span data-ttu-id="8a935-107">Dieses Dokument enthält Informationen, die in der Produktdokumentation nicht zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="8a935-107">This document contains information that is not available in the product documentation.</span></span> <span data-ttu-id="8a935-108">Wenn es einen Unterschied zwischen diesen Anmerkungen zu dieser Version und einer anderen App-V-Dokumentation gibt, sollte die neueste Änderung als autorisierend angesehen werden.</span><span class="sxs-lookup"><span data-stu-id="8a935-108">If there is a difference between these Release Notes and other App-V documentation, the latest change should be considered authoritative.</span></span> <span data-ttu-id="8a935-109">Diese Versionshinweise ersetzen die Inhalte, die in diesem Produkt enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="8a935-109">These release notes supersede the content that is included with this product.</span></span>

## <span data-ttu-id="8a935-110">Schutz vor Sicherheitsrisiken und Viren</span><span class="sxs-lookup"><span data-stu-id="8a935-110">Protect Against Security Vulnerabilities and Viruses</span></span>


<span data-ttu-id="8a935-111">Zum Schutz vor Sicherheitsrisiken und Viren ist es wichtig, die neuesten verfügbaren Sicherheitsupdates für jede neue Software zu installieren, die installiert wird.</span><span class="sxs-lookup"><span data-stu-id="8a935-111">To help protect against security vulnerabilities and viruses, it is important to install the latest available security updates for any new software being installed.</span></span> <span data-ttu-id="8a935-112">Weitere Informationen finden Sie auf der [Microsoft-Sicherheitswebsite](https://go.microsoft.com/fwlink/?LinkId=3482) ( https://go.microsoft.com/fwlink/?LinkId=3482) .</span><span class="sxs-lookup"><span data-stu-id="8a935-112">For more information, see the [Microsoft Security website](https://go.microsoft.com/fwlink/?LinkId=3482) (https://go.microsoft.com/fwlink/?LinkId=3482).</span></span>

## <span data-ttu-id="8a935-113">Bekannte Probleme mit Application Virtualization 4.6 SP3</span><span class="sxs-lookup"><span data-stu-id="8a935-113">Known Issues with Application Virtualization4.6 SP3</span></span>


<span data-ttu-id="8a935-114">In diesem Abschnitt finden Sie die neuesten Informationen zu Problemen mit Microsoft Application Virtualization (App-V) 4.6 SP3.</span><span class="sxs-lookup"><span data-stu-id="8a935-114">This section provides the most up-to-date information about issues with Microsoft Application Virtualization (App-V)4.6SP3.</span></span> <span data-ttu-id="8a935-115">Diese Probleme werden in der Produktdokumentation nicht angezeigt und können in einigen Fällen der vorhandenen Produktdokumentation widersprechen.</span><span class="sxs-lookup"><span data-stu-id="8a935-115">These issues do not appear in the product documentation and in some cases might contradict existing product documentation.</span></span> <span data-ttu-id="8a935-116">Wenn dies möglich ist, werden diese Probleme in späteren Versionen behoben.</span><span class="sxs-lookup"><span data-stu-id="8a935-116">When it is possible, these issues will be addressed in later releases.</span></span>

### <span data-ttu-id="8a935-117">In der virtuellen Umgebung können keine Links mit Internet Explorer11 auf Microsoft Windows 8,1 geöffnet werden</span><span class="sxs-lookup"><span data-stu-id="8a935-117">Unable to open hyperlinks using Internet Explorer11 on Microsoft Windows 8.1 within the Virtual Environment</span></span>

<span data-ttu-id="8a935-118">Der Versuch, Hyperlinks innerhalb einer virtuellen Umgebung zu öffnen, schlägt in Windows 8,1 mit Internet Explorer 11 fehl.</span><span class="sxs-lookup"><span data-stu-id="8a935-118">Attempting to open hyperlinks from within a virtual environment will fail on Windows 8.1 using Internet Explorer 11.</span></span> <span data-ttu-id="8a935-119">Der Grund dafür ist, dass Internet Explorer 11 nun standardmäßig mit aktiviertem erweiterten Schutzmodus (EPM) ausgeliefert wird und App-V nicht in der Lage ist, auf erforderliche Registrierungsschlüssel, Dateien und Kommunikations Port Objekte zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="8a935-119">This is because Internet Explorer 11 now ships with the Enhanced Protection Mode (EPM) enabled by default and this causes App-V to be unable to access required registry keys, files and communication port objects.</span></span>

<span data-ttu-id="8a935-120">Problemumgehung: Deaktivieren Sie EPM in Internet Explorer11, bevor Sie ein App-V-Paket öffnen.</span><span class="sxs-lookup"><span data-stu-id="8a935-120">WORKAROUND: Disable EPM in Internet Explorer11 before opening an App-V package.</span></span> <span data-ttu-id="8a935-121">Auf diese Weise können Sie Internet Explorer in der virtuellen Umgebung öffnen.</span><span class="sxs-lookup"><span data-stu-id="8a935-121">This will allow you to open Internet Explorer from within the virtual environment.</span></span>

## <span data-ttu-id="8a935-122">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="8a935-122">Related topics</span></span>


[<span data-ttu-id="8a935-123">Informationen zu Microsoft Application Virtualization 4.6SP3</span><span class="sxs-lookup"><span data-stu-id="8a935-123">About Microsoft Application Virtualization 4.6 SP3</span></span>](about-microsoft-application-virtualization-46-sp3.md)

 

 





