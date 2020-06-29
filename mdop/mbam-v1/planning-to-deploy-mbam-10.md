---
title: Planen der Bereitstellung von MBAM 1.0
description: Planen der Bereitstellung von MBAM 1.0
author: dansimp
ms.assetid: 30ad4304-45c6-427d-8e33-ebe8053c7871
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c2ff25e705717db5086150ed08a5640335bbacb8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809805"
---
# <span data-ttu-id="3057e-103">Planen der Bereitstellung von MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="3057e-103">Planning to Deploy MBAM 1.0</span></span>


<span data-ttu-id="3057e-104">Sie sollten eine Reihe unterschiedlicher Bereitstellungskonfigurationen und Voraussetzungen berücksichtigen, bevor Sie den 1,0-Bereitstellungsplan für Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) erstellen.</span><span class="sxs-lookup"><span data-stu-id="3057e-104">You should consider a number of different deployment configurations and prerequisites before you create your Microsoft BitLocker Administration and Monitoring (MBAM) 1.0 deployment plan.</span></span> <span data-ttu-id="3057e-105">Dieser Abschnitt enthält Informationen, die Ihnen bei der Erfassung der Informationen helfen können, die Sie benötigen, um einen Bereitstellungsplan zu formulieren, der Ihren geschäftlichen Anforderungen am besten entspricht.</span><span class="sxs-lookup"><span data-stu-id="3057e-105">This section includes information that can help you gather the information that you must have to formulate a deployment plan that best meets your business requirements.</span></span>

## <span data-ttu-id="3057e-106">Überprüfen der von MBAM 1,0 unterstützten Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="3057e-106">Review the MBAM 1.0 supported configurations</span></span>


<span data-ttu-id="3057e-107">Nachdem Sie Ihre Computing-Umgebung für die MBAM-Client-und Server-Feature-Installation vorbereitet haben, überprüfen Sie, ob Sie die unterstützten Konfigurationsinformationen für MBAM, um zu bestätigen, dass die Computer, auf denen Sie MBAM installieren, die Mindestanforderungen für Hardware und Betriebssystem erfüllen.</span><span class="sxs-lookup"><span data-stu-id="3057e-107">After you prepare your computing environment for the MBAM Client and Server feature installation, make sure that you review the Supported Configurations information for MBAM to confirm that the computers on which you install MBAM meet the minimum hardware and operating system requirements.</span></span> <span data-ttu-id="3057e-108">Weitere Informationen zu den Voraussetzungen für die MBAM-Bereitstellung finden Sie unter [MBAM 1,0-Bereitstellungsvoraussetzungen](mbam-10-deployment-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="3057e-108">For more information about MBAM deployment prerequisites, see [MBAM 1.0 Deployment Prerequisites](mbam-10-deployment-prerequisites.md).</span></span>

[<span data-ttu-id="3057e-109">Von MBAM 1.0 unterstützte Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="3057e-109">MBAM 1.0 Supported Configurations</span></span>](mbam-10-supported-configurations.md)

## <span data-ttu-id="3057e-110">Planen der MBAM 1,0-Server-und-Client Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="3057e-110">Plan for MBAM 1.0 Server and Client deployment</span></span>


<span data-ttu-id="3057e-111">Die MBAM-Serverinfrastruktur hängt von einer Reihe von Server Features ab, die basierend auf den Anforderungen des Unternehmens auf einem oder mehreren Server Computern installiert werden können.</span><span class="sxs-lookup"><span data-stu-id="3057e-111">The MBAM server infrastructure depends on a set of server features that can be installed on one or more server computers, based on the requirements of the enterprise.</span></span> <span data-ttu-id="3057e-112">Diese Features können auf einem einzelnen Server installiert oder auf mehrere Server verteilt werden.</span><span class="sxs-lookup"><span data-stu-id="3057e-112">These features can be installed on a single server or distributed across multiple servers.</span></span>

<span data-ttu-id="3057e-113">Der MBAM-Client ermöglicht es Administratoren, die BitLocker-Laufwerkverschlüsselung auf Computern im Unternehmen durchzusetzen und zu überwachen.</span><span class="sxs-lookup"><span data-stu-id="3057e-113">The MBAM Client enables administrators to enforce and monitor the BitLocker drive encryption on computers in the enterprise.</span></span> <span data-ttu-id="3057e-114">Der BitLocker-Client kann in eine Organisation integriert werden, indem der Client mithilfe von Tools wie Active Directory-Domänendiensten oder durch direkte Verschlüsselung der Clientcomputer im Rahmen des anfänglichen Imaging-Prozesses bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="3057e-114">The BitLocker client can be integrated into an organization by deploying the client through tools like Active Directory Domain Services or by directly encrypting the client computers as part of the initial imaging process.</span></span>

<span data-ttu-id="3057e-115">Mit MBAM können Sie einen Computer in Ihrer Organisation verschlüsseln, bevor der Endbenutzer den Computer oder anschließend mithilfe von Gruppenrichtlinien empfängt.</span><span class="sxs-lookup"><span data-stu-id="3057e-115">With MBAM, you can encrypt a computer in your organization either before the end user receives the computer or afterwards, by using Group Policy.</span></span> <span data-ttu-id="3057e-116">Sie können eine oder beide Methoden in Ihrer Organisation verwenden.</span><span class="sxs-lookup"><span data-stu-id="3057e-116">You can use one or both methods in your organization.</span></span> <span data-ttu-id="3057e-117">Wenn Sie beide Methoden verwenden, können Sie Compliance, Berichterstellung und Unterstützung für die Schlüsselwiederherstellung verbessern.</span><span class="sxs-lookup"><span data-stu-id="3057e-117">If you choose to use both methods, you can improve compliance, reporting, and key recovery support.</span></span>

[<span data-ttu-id="3057e-118">Planen der Serverbereitstellung für MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="3057e-118">Planning for MBAM 1.0 Server Deployment</span></span>](planning-for-mbam-10-server-deployment.md)

[<span data-ttu-id="3057e-119">Planen der Clientbereitstellung für MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="3057e-119">Planning for MBAM 1.0 Client Deployment</span></span>](planning-for-mbam-10-client-deployment.md)

## <a href="" id="other-resources-for-mbam-planning-"></a><span data-ttu-id="3057e-120">Weitere Ressourcen für die Planung von MBAM</span><span class="sxs-lookup"><span data-stu-id="3057e-120">Other resources for MBAM planning</span></span>


-   [<span data-ttu-id="3057e-121">Planen von MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="3057e-121">Planning for MBAM 1.0</span></span>](planning-for-mbam-10.md)

 

 





