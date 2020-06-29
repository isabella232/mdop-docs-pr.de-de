---
title: MBAM 2.5-Servervoraussetzungen, die nur für die Configuration Manager-Integrationstopologie gelten
description: MBAM 2.5-Servervoraussetzungen, die nur für die Configuration Manager-Integrationstopologie gelten
author: dansimp
ms.assetid: 74180d8d-7b0f-460f-b301-53595cde8381
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: dd9b89e1a1383997d6ebc92f8e034fbf2945823f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804322"
---
# <span data-ttu-id="9f46f-103">MBAM 2.5-Servervoraussetzungen, die nur für die Configuration Manager-Integrationstopologie gelten</span><span class="sxs-lookup"><span data-stu-id="9f46f-103">MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology</span></span>


<span data-ttu-id="9f46f-104">Wenn Sie die Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) 2,5 mithilfe des System Center Configuration Manager-Integrationsfeatures installieren, müssen Sie die in diesem Thema beschriebenen Voraussetzungen zusätzlich zu den in [MBAM 2,5-Server Voraussetzungen für eigenständige und Configuration Manager-Integrations Topologien](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)ausführen.</span><span class="sxs-lookup"><span data-stu-id="9f46f-104">If you are installing Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 by using the System Center Configuration Manager Integration feature, you must complete the prerequisites described in this topic, in addition to those in [MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md).</span></span> <span data-ttu-id="9f46f-105">Sie müssen auch MOF-Dateien erstellen oder ändern, die für die Configuration Manager-Integrations Topologie erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="9f46f-105">You must also create or modify .mof files that are needed for the Configuration Manager Integration topology.</span></span>

## <span data-ttu-id="9f46f-106">Voraussetzungen für das Configuration Manager-Integrationsfeature</span><span class="sxs-lookup"><span data-stu-id="9f46f-106">Prerequisites for the Configuration Manager Integration Feature</span></span>


<span data-ttu-id="9f46f-107">Wenn Sie MBAM mit der System Center Configuration Manager-Integrations Topologie konfigurieren, müssen Sie weitere Voraussetzungen erfüllen, die für Configuration Manager erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="9f46f-107">If you are configuring MBAM with the System Center Configuration Manager Integration topology, you must complete additional prerequisites that are required for Configuration Manager.</span></span>

[<span data-ttu-id="9f46f-108">Voraussetzungen für das Configuration Manager-Integrationsfeature</span><span class="sxs-lookup"><span data-stu-id="9f46f-108">Prerequisites for the Configuration Manager Integration Feature</span></span>](prerequisites-for-the-configuration-manager-integration-feature.md)

## <span data-ttu-id="9f46f-109">Bearbeiten der Datei "Configuration. mof"</span><span class="sxs-lookup"><span data-stu-id="9f46f-109">Edit the Configuration.mof file</span></span>


<span data-ttu-id="9f46f-110">Damit die Clientcomputer BitLocker-Kompatibilitätsdetails über die MBAM-Konfigurations-Manager-Berichte melden können, müssen Sie die Datei "Configuration. mof" für SystemCenter2012 ConfigurationManager und Microsoft System Center Configuration Manager 2007 bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="9f46f-110">To enable the client computers to report BitLocker compliance details through the MBAM Configuration Manager Reports, you have to edit the Configuration.mof file for SystemCenter2012 ConfigurationManager and Microsoft System Center Configuration Manager 2007.</span></span>

[<span data-ttu-id="9f46f-111">Bearbeiten der Datei „Configuration.mof“</span><span class="sxs-lookup"><span data-stu-id="9f46f-111">Edit the Configuration.mof File</span></span>](edit-the-configurationmof-file-mbam-25.md)

## <a href="" id="create-or-edit-the-sms-def-mof-file"></a><span data-ttu-id="9f46f-112">Erstellen oder Bearbeiten der SMS \ _def. MOF-Datei</span><span class="sxs-lookup"><span data-stu-id="9f46f-112">Create or edit the Sms\_def.mof file</span></span>


<span data-ttu-id="9f46f-113">Damit die Clientcomputer BitLocker-Kompatibilitätsdetails in den MBAM-Configuration Manager-Berichten melden können, müssen Sie die SMS \ _def. MOF-Datei erstellen oder bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="9f46f-113">To enable the client computers to report BitLocker compliance details in the MBAM Configuration Manager Reports, you have to create or edit the Sms\_def.mof file.</span></span> <span data-ttu-id="9f46f-114">Wenn Sie SystemCenter2012 ConfigurationManager verwenden, müssen Sie die Datei erstellen.</span><span class="sxs-lookup"><span data-stu-id="9f46f-114">If you are using SystemCenter2012 ConfigurationManager, you must create the file.</span></span> <span data-ttu-id="9f46f-115">In Configuration Manager 2007 ist die Datei bereits vorhanden, daher müssen Sie die vorhandene Datei bearbeiten, aber nicht überschreiben.</span><span class="sxs-lookup"><span data-stu-id="9f46f-115">In Configuration Manager 2007, the file already exists, so you need to edit, but not overwrite, the existing file.</span></span>

[<span data-ttu-id="9f46f-116">Erstellen oder Bearbeiten der SMS \ _def. MOF-Datei</span><span class="sxs-lookup"><span data-stu-id="9f46f-116">Create or Edit the Sms\_def.mof File</span></span>](create-or-edit-the-sms-defmof-file-mbam-25.md)


## <span data-ttu-id="9f46f-117">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="9f46f-117">Related topics</span></span>


[<span data-ttu-id="9f46f-118">Vorbereiten der Umgebung für MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="9f46f-118">Preparing your Environment for MBAM 2.5</span></span>](preparing-your-environment-for-mbam-25.md)

[<span data-ttu-id="9f46f-119">Von MBAM 2.5 unterstützte Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="9f46f-119">MBAM 2.5 Supported Configurations</span></span>](mbam-25-supported-configurations.md)

[<span data-ttu-id="9f46f-120">Planen der Bereitstellung von MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="9f46f-120">Planning to Deploy MBAM 2.5</span></span>](planning-to-deploy-mbam-25.md)

 

 
## <span data-ttu-id="9f46f-121">Sie haben einen Vorschlag für MBAM?</span><span class="sxs-lookup"><span data-stu-id="9f46f-121">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="9f46f-122">[Hier](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)können Sie Vorschläge hinzufügen oder abstimmen.</span><span class="sxs-lookup"><span data-stu-id="9f46f-122">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="9f46f-123">Bei MBAM-Problemen verwenden Sie das [MBAM TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="9f46f-123">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>




