---
title: Verwenden von MBAM mit dem Konfigurations-Manager
description: Verwenden von MBAM mit dem Konfigurations-Manager
author: dansimp
ms.assetid: 03868717-4aa7-4897-8166-9a3df5e9519e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9e3c5dd199010ac758ab701b0753d913ea323efd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810165"
---
# <span data-ttu-id="b0b4c-103">Verwenden von MBAM mit dem Konfigurations-Manager</span><span class="sxs-lookup"><span data-stu-id="b0b4c-103">Using MBAM with Configuration Manager</span></span>


<span data-ttu-id="b0b4c-104">Wenn Sie die Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) installieren, können Sie eine Installation auswählen, die die Microsoft BitLocker-Verwaltung und-Überwachung mit System Center Configuration Manager integriert.</span><span class="sxs-lookup"><span data-stu-id="b0b4c-104">When you install Microsoft BitLocker Administration and Monitoring (MBAM), you can choose an installation that integrates Microsoft BitLocker Administration and Monitoring with System Center Configuration Manager.</span></span> <span data-ttu-id="b0b4c-105">Eine Liste der unterstützten Versionen von Configuration Manager finden Sie unter [Planen der Bereitstellung von MBAM mit Configuration Manager](planning-to-deploy-mbam-with-configuration-manager-2.md).</span><span class="sxs-lookup"><span data-stu-id="b0b4c-105">For a list of the supported versions of Configuration Manager, see [Planning to Deploy MBAM with Configuration Manager](planning-to-deploy-mbam-with-configuration-manager-2.md).</span></span>

<span data-ttu-id="b0b4c-106">Durch diese Integration werden die Microsoft BitLocker-Verwaltungs-und-Überwachungs-und-Berichtsinfrastruktur in die systemeigene Umgebung von Microsoft System Center Configuration Manager verschoben.</span><span class="sxs-lookup"><span data-stu-id="b0b4c-106">This integration moves the Microsoft BitLocker Administration and Monitoring compliance and reporting infrastructure into the native environment of Microsoft System Center Configuration Manager.</span></span> <span data-ttu-id="b0b4c-107">Mit der Configuration Manager-Topologie können IT-Administratoren Berichte und den Kompatibilitätsstatus Ihres Unternehmens über die Configuration Manager-Verwaltungskonsole anzeigen.</span><span class="sxs-lookup"><span data-stu-id="b0b4c-107">With the Configuration Manager topology, IT administrators can view reports and the compliance status of their enterprise from the Configuration Manager Management Console.</span></span>

<span data-ttu-id="b0b4c-108">**Wichtig**  Windows to go wird nicht unterstützt, wenn Sie die integrierte Topologie von MBAM mit Configuration Manager 2007 installieren.</span><span class="sxs-lookup"><span data-stu-id="b0b4c-108">**Important** Windows To Go is not supported when you install the integrated topology of MBAM with Configuration Manager 2007.</span></span>

 

## <a href="" id="getting-started---using-mbam-with-configuration-manager"></a><span data-ttu-id="b0b4c-109">Erste Schritte – verwenden von MBAM mit Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="b0b4c-109">Getting Started – Using MBAM with Configuration Manager</span></span>


<span data-ttu-id="b0b4c-110">In diesem Abschnitt wird beschrieben, wie MBAM mit Configuration Manager funktioniert und wie die empfohlene Architektur für die Bereitstellung von MBAM mit der Configuration Manager-Integrations Topologie erläutert wird.</span><span class="sxs-lookup"><span data-stu-id="b0b4c-110">This section describes how MBAM works with Configuration Manager and explains the recommended architecture for deploying MBAM with the Configuration Manager Integration topology.</span></span>

[<span data-ttu-id="b0b4c-111">Erste Schritte – Verwenden von MBAM mit dem Konfigurations-Manager</span><span class="sxs-lookup"><span data-stu-id="b0b4c-111">Getting Started - Using MBAM with Configuration Manager</span></span>](getting-started---using-mbam-with-configuration-manager.md)

## <span data-ttu-id="b0b4c-112">Planen der Bereitstellung von MBAM mit dem Konfigurations-Manager</span><span class="sxs-lookup"><span data-stu-id="b0b4c-112">Planning to Deploy MBAM with Configuration Manager</span></span>


<span data-ttu-id="b0b4c-113">In diesem Abschnitt werden die Voraussetzungen für die Installation, die unterstützten Konfigurationen sowie Hardware-und Softwareanforderungen beschrieben, die Sie vor der Installation von MBAM mit der Configuration Manager-Topologie in Frage stellen müssen.</span><span class="sxs-lookup"><span data-stu-id="b0b4c-113">This section describes the installation prerequisites, supported configurations, and hardware and software requirements that you need to consider before you install MBAM with the Configuration Manager topology.</span></span>

[<span data-ttu-id="b0b4c-114">Planen der Bereitstellung von MBAM mit dem Konfigurations-Manager</span><span class="sxs-lookup"><span data-stu-id="b0b4c-114">Planning to Deploy MBAM with Configuration Manager</span></span>](planning-to-deploy-mbam-with-configuration-manager-2.md)

## <span data-ttu-id="b0b4c-115">Bereitstellen von MBAM mit dem Konfigurations-Manager</span><span class="sxs-lookup"><span data-stu-id="b0b4c-115">Deploying MBAM with Configuration Manager</span></span>


<span data-ttu-id="b0b4c-116">In diesem Abschnitt wird beschrieben, wie Sie MBAM mit Configuration Manager bereitstellen und Anweisungen zum Installieren und Konfigurieren des MBAM auf dem Verwaltungs-und Überwachungsserver und dem Configuration Manager-Server enthalten.</span><span class="sxs-lookup"><span data-stu-id="b0b4c-116">This section describes how to deploy MBAM with Configuration Manager, and includes instructions for installing and configuring the MBAM on the Administration and Monitoring Server and Configuration Manager Server.</span></span>

[<span data-ttu-id="b0b4c-117">Bereitstellen von MBAM mit dem Konfigurations-Manager</span><span class="sxs-lookup"><span data-stu-id="b0b4c-117">Deploying MBAM with Configuration Manager</span></span>](deploying-mbam-with-configuration-manager-mbam2.md)

## <span data-ttu-id="b0b4c-118">Grundlegende Informationen zu MBAM Berichten im Konfigurations-Manager</span><span class="sxs-lookup"><span data-stu-id="b0b4c-118">Understanding MBAM Reports in Configuration Manager</span></span>


<span data-ttu-id="b0b4c-119">In diesem Abschnitt werden die MBAM-Berichte beschrieben, die Sie in Configuration Manager ausführen können, um die Compliance Ihres Unternehmens und die Konformität einzelner Computer in Ihrem Unternehmen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="b0b4c-119">This section describes the MBAM reports that you can run from Configuration Manager to show the compliance of your enterprise and compliance of individual computers in your enterprise.</span></span>

[<span data-ttu-id="b0b4c-120">Grundlegende Informationen zu MBAM Berichten im Konfigurations-Manager</span><span class="sxs-lookup"><span data-stu-id="b0b4c-120">Understanding MBAM Reports in Configuration Manager</span></span>](understanding-mbam-reports-in-configuration-manager.md)

## <span data-ttu-id="b0b4c-121">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="b0b4c-121">Related topics</span></span>


[<span data-ttu-id="b0b4c-122">Vorgänge für MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="b0b4c-122">Operations for MBAM 2.0</span></span>](operations-for-mbam-20-mbam-2.md)

 

 





