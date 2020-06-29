---
title: Planen der Bereitstellung von MBAM 2.0
description: Planen der Bereitstellung von MBAM 2.0
author: dansimp
ms.assetid: 2dc05fcd-aed9-4315-aeaf-92aaa9e0e955
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c7f065e52655212261dfe8b6b3f081f697142473
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811272"
---
# <span data-ttu-id="9dd0f-103">Planen der Bereitstellung von MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="9dd0f-103">Planning to Deploy MBAM 2.0</span></span>


<span data-ttu-id="9dd0f-104">Sie sollten eine Reihe unterschiedlicher Bereitstellungskonfigurationen und Voraussetzungen berücksichtigen, bevor Sie Ihren Bereitstellungsplan für Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) erstellen.</span><span class="sxs-lookup"><span data-stu-id="9dd0f-104">You should consider a number of different deployment configurations and prerequisites before you create your deployment plan for Microsoft BitLocker Administration and Monitoring (MBAM).</span></span> <span data-ttu-id="9dd0f-105">Dieser Abschnitt enthält Informationen, die Ihnen beim Sammeln der erforderlichen Informationen helfen können, um einen Bereitstellungsplan zu formulieren, der Ihren geschäftlichen Anforderungen am besten entspricht.</span><span class="sxs-lookup"><span data-stu-id="9dd0f-105">This section includes information that can help you gather the necessary information to formulate a deployment plan that best meets your business requirements.</span></span> <span data-ttu-id="9dd0f-106">Wenn Sie MBAM mit der Configuration Manager-Topologie installieren, lesen Sie [Planen der Bereitstellung von MBAM mit Configuration Manager](planning-to-deploy-mbam-with-configuration-manager-2.md) für zusätzliche Planungsinformationen.</span><span class="sxs-lookup"><span data-stu-id="9dd0f-106">If you are installing MBAM with the Configuration Manager topology, see [Planning to Deploy MBAM with Configuration Manager](planning-to-deploy-mbam-with-configuration-manager-2.md) for additional planning information.</span></span>

## <span data-ttu-id="9dd0f-107">Überprüfen der von MBAM 2,0 unterstützten Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="9dd0f-107">Review the MBAM 2.0 Supported Configurations</span></span>


<span data-ttu-id="9dd0f-108">Stellen Sie nach dem Vorbereiten Ihrer Computerumgebung für die MBAM-Server-und-Client Feature-Installation sicher, dass Sie die unterstützten Konfigurationen überprüfen, um zu bestätigen, dass die Computer, auf denen Sie die Installation durchführen, die Mindestanforderungen für Hardware und Betriebssystem MBAM erfüllen.</span><span class="sxs-lookup"><span data-stu-id="9dd0f-108">After preparing your computing environment for the MBAM Server and Client feature installation, make sure that you review the Supported Configurations to confirm that the computers on which you are installing MBAM meet the minimum hardware and operating system requirements.</span></span> <span data-ttu-id="9dd0f-109">Weitere Informationen zu den Voraussetzungen für die MBAM-Bereitstellung finden Sie unter [MBAM 2,0-Bereitstellungsvoraussetzungen](mbam-20-deployment-prerequisites-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="9dd0f-109">For more information about MBAM deployment prerequisites, see [MBAM 2.0 Deployment Prerequisites](mbam-20-deployment-prerequisites-mbam-2.md).</span></span>

[<span data-ttu-id="9dd0f-110">Von MBAM 2.0 unterstützte Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="9dd0f-110">MBAM 2.0 Supported Configurations</span></span>](mbam-20-supported-configurations-mbam-2.md)

## <span data-ttu-id="9dd0f-111">Planen der MBAM 2,0-Server-und-Client Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="9dd0f-111">Plan for MBAM 2.0 Server and Client Deployment</span></span>


<span data-ttu-id="9dd0f-112">Die MBAM-Serverinfrastruktur hängt von einer Reihe von Server Features ab, die basierend auf den Anforderungen des Unternehmens auf einem oder mehreren Server Computern installiert werden können.</span><span class="sxs-lookup"><span data-stu-id="9dd0f-112">The MBAM Server infrastructure depends on a set of server features that can be installed on one or more server computers, based on the requirements of the enterprise.</span></span> <span data-ttu-id="9dd0f-113">Diese Features können in einer verteilten Konfiguration auf mehreren Servern installiert werden.</span><span class="sxs-lookup"><span data-stu-id="9dd0f-113">These features can be installed in a distributed configuration across multiple servers.</span></span>

<span data-ttu-id="9dd0f-114">**Hinweis**  Eine MBAM-Installation auf einem einzelnen Server wird nur für Lab-Umgebungen empfohlen.</span><span class="sxs-lookup"><span data-stu-id="9dd0f-114">**Note** An MBAM installation on a single server is recommended only for lab environments.</span></span>

 

<span data-ttu-id="9dd0f-115">Der MBAM-Client ermöglicht Administratoren das erzwingen und Überwachen der BitLocker-Laufwerkverschlüsselung auf Computern im Unternehmen.</span><span class="sxs-lookup"><span data-stu-id="9dd0f-115">The MBAM Client enables administrators to enforce and monitor BitLocker drive encryption on computers in the enterprise.</span></span> <span data-ttu-id="9dd0f-116">Der BitLocker-Client kann in eine Organisation integriert werden, indem der Client über ein Enterprise-Software Bereitstellungssystem bereitgestellt oder der Client-Agent auf Clientcomputern als Teil des anfänglichen Imaging-Prozesses installiert wird.</span><span class="sxs-lookup"><span data-stu-id="9dd0f-116">The BitLocker client can be integrated into an organization by deploying the client through an enterprise software delivery system or by installing the client agent on client computers as part of the initial imaging process.</span></span>

<span data-ttu-id="9dd0f-117">Mit MBAM können Sie einen Computer in Ihrer Organisation verschlüsseln, entweder bevor der Endbenutzer den Computer empfängt, oder anschließend mithilfe von Gruppenrichtlinien.</span><span class="sxs-lookup"><span data-stu-id="9dd0f-117">With MBAM, you can encrypt a computer in your organization either before the end user receives the computer, or afterwards by using Group Policy.</span></span>

[<span data-ttu-id="9dd0f-118">Planen der Serverbereitstellung für MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="9dd0f-118">Planning for MBAM 2.0 Server Deployment</span></span>](planning-for-mbam-20-server-deployment-mbam-2.md)

[<span data-ttu-id="9dd0f-119">Planen der Clientbereitstellung für MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="9dd0f-119">Planning for MBAM 2.0 Client Deployment</span></span>](planning-for-mbam-20-client-deployment-mbam-2.md)

## <a href="" id="other-resources-for-mbam-planning-"></a><span data-ttu-id="9dd0f-120">Weitere Ressourcen für die Planung von MBAM</span><span class="sxs-lookup"><span data-stu-id="9dd0f-120">Other Resources for MBAM Planning</span></span>


[<span data-ttu-id="9dd0f-121">Planen von MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="9dd0f-121">Planning for MBAM 2.0</span></span>](planning-for-mbam-20-mbam-2.md)

 

 





