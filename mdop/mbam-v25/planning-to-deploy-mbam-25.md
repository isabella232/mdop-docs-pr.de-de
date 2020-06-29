---
title: Planen der Bereitstellung von MBAM 2.5
description: Planen der Bereitstellung von MBAM 2.5
author: dansimp
ms.assetid: 1343b80c-d87a-42e7-b912-e84ba997d7e3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2e955b426b00539aa2a4ef0b7c3a6650b05633a5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811908"
---
# <span data-ttu-id="b873a-103">Planen der Bereitstellung von MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="b873a-103">Planning to Deploy MBAM 2.5</span></span>


<span data-ttu-id="b873a-104">Sie sollten eine Reihe unterschiedlicher Bereitstellungskonfigurationen und Voraussetzungen berücksichtigen, bevor Sie Ihren Bereitstellungsplan für Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) erstellen.</span><span class="sxs-lookup"><span data-stu-id="b873a-104">You should consider a number of different deployment configurations and prerequisites before you create your deployment plan for Microsoft BitLocker Administration and Monitoring (MBAM).</span></span> <span data-ttu-id="b873a-105">Dieser Abschnitt enthält Informationen, die Ihnen beim Sammeln der erforderlichen Informationen helfen können, um einen Bereitstellungsplan zu formulieren, der Ihren geschäftlichen Anforderungen am besten entspricht.</span><span class="sxs-lookup"><span data-stu-id="b873a-105">This section includes information that can help you gather the necessary information to formulate a deployment plan that best meets your business requirements.</span></span>

## <span data-ttu-id="b873a-106">Überprüfen der von MBAM 2,5 unterstützten Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="b873a-106">Review the MBAM 2.5 supported configurations</span></span>


<span data-ttu-id="b873a-107">Nachdem Sie Ihre Computerumgebung für die Bereitstellung von MBAM-Servern und-Clients vorbereitet haben, vergewissern Sie sich, dass Sie die unterstützten Konfigurationen überprüfen, um zu bestätigen, dass die Computer, auf denen Sie die Installation durchführen, die Mindestanforderungen für Hardware und Betriebssystem MBAM.</span><span class="sxs-lookup"><span data-stu-id="b873a-107">After preparing your computing environment for the MBAM Server and Client feature deployment, make sure that you review the Supported Configurations to confirm that the computers on which you are installing MBAM meet the minimum hardware and operating system requirements.</span></span> <span data-ttu-id="b873a-108">Weitere Informationen zu den Voraussetzungen für die MBAM-Bereitstellung finden Sie unter [MBAM 2,5-Bereitstellungsvoraussetzungen](mbam-25-deployment-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="b873a-108">For more information about MBAM deployment prerequisites, see [MBAM 2.5 Deployment Prerequisites](mbam-25-deployment-prerequisites.md).</span></span>

[<span data-ttu-id="b873a-109">Von MBAM 2.5 unterstützte Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="b873a-109">MBAM 2.5 Supported Configurations</span></span>](mbam-25-supported-configurations.md)

## <span data-ttu-id="b873a-110">Planen der MBAM 2,5-Server-und-Client Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="b873a-110">Plan for MBAM 2.5 Server and Client deployment</span></span>


<span data-ttu-id="b873a-111">Die MBAM-Serverinfrastruktur hängt von einer Reihe von Server Features ab, die basierend auf den Anforderungen des Unternehmens auf einem oder mehreren Server Computern konfiguriert werden können.</span><span class="sxs-lookup"><span data-stu-id="b873a-111">The MBAM Server infrastructure depends on a set of server features that can be configured on one or more server computers, based on the requirements of the enterprise.</span></span> <span data-ttu-id="b873a-112">Diese Features können in einer verteilten Konfiguration auf mehreren Servern konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="b873a-112">These features can be configured in a distributed configuration across multiple servers.</span></span>

<span data-ttu-id="b873a-113">**Hinweis**  Eine MBAM-Installation auf einem einzelnen Server wird nur für Lab-Umgebungen empfohlen.</span><span class="sxs-lookup"><span data-stu-id="b873a-113">**Note** An MBAM installation on a single server is recommended only for lab environments.</span></span>

 

<span data-ttu-id="b873a-114">Der MBAM-Client ermöglicht Administratoren das erzwingen und Überwachen der BitLocker-Laufwerkverschlüsselung auf Computern im Unternehmen.</span><span class="sxs-lookup"><span data-stu-id="b873a-114">The MBAM Client enables administrators to enforce and monitor BitLocker drive encryption on computers in the enterprise.</span></span> <span data-ttu-id="b873a-115">Der BitLocker-Client kann in eine Organisation integriert werden, indem der Client über ein Enterprise-Software Delivery-System bereitgestellt oder der Client auf Clientcomputern im Rahmen des anfänglichen Imaging-Prozesses installiert wird.</span><span class="sxs-lookup"><span data-stu-id="b873a-115">The BitLocker client can be integrated into an organization by deploying the client through an enterprise software delivery system or by installing the Client on client computers as part of the initial imaging process.</span></span>

<span data-ttu-id="b873a-116">Mit MBAM können Sie einen Computer in Ihrer Organisation verschlüsseln, entweder bevor der Endbenutzer den Computer empfängt, oder anschließend mithilfe von Gruppenrichtlinien.</span><span class="sxs-lookup"><span data-stu-id="b873a-116">With MBAM, you can encrypt a computer in your organization either before the end user receives the computer, or afterwards by using Group Policy.</span></span>

[<span data-ttu-id="b873a-117">Planen der Serverbereitstellung für MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="b873a-117">Planning for MBAM 2.5 Server Deployment</span></span>](planning-for-mbam-25-server-deployment.md)

[<span data-ttu-id="b873a-118">Planen der Clientbereitstellung für MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="b873a-118">Planning for MBAM 2.5 Client Deployment</span></span>](planning-for-mbam-25-client-deployment.md)

## <a href="" id="other-resources-for-mbam-planning-"></a><span data-ttu-id="b873a-119">Weitere Ressourcen für die Planung von MBAM</span><span class="sxs-lookup"><span data-stu-id="b873a-119">Other resources for MBAM planning</span></span>


[<span data-ttu-id="b873a-120">Planen von MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="b873a-120">Planning for MBAM 2.5</span></span>](planning-for-mbam-25.md)

## <span data-ttu-id="b873a-121">Sie haben einen Vorschlag für MBAM?</span><span class="sxs-lookup"><span data-stu-id="b873a-121">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="b873a-122">[Hier](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)können Sie Vorschläge hinzufügen oder abstimmen.</span><span class="sxs-lookup"><span data-stu-id="b873a-122">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="b873a-123">Bei MBAM-Problemen verwenden Sie das [MBAM TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="b873a-123">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>

 

 





