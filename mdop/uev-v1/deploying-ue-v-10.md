---
title: Bereitstellen von UE-V 1.0
description: Bereitstellen von UE-V 1.0
author: dansimp
ms.assetid: 519598bb-8c81-4af7-bee7-357696bff880
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1a1c515f9be950d8ca7b0a199344d34f7852073d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812181"
---
# <span data-ttu-id="ba2e8-103">Bereitstellen von UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="ba2e8-103">Deploying UE-V 1.0</span></span>


<span data-ttu-id="ba2e8-104">Es gibt eine Reihe unterschiedlicher Bereitstellungskonfigurationen, die von Microsoft User Experience Virtualization (UE-V) unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="ba2e8-104">There are a number of different deployment configurations that Microsoft User Experience Virtualization (UE-V) supports.</span></span> <span data-ttu-id="ba2e8-105">Dieser Abschnitt enthält allgemeine Informationen und schrittweise Anleitungen, die Ihnen bei der erfolgreichen Durchführung der Aufgaben helfen, die Sie in verschiedenen Phasen Ihrer Bereitstellung ausführen müssen.</span><span class="sxs-lookup"><span data-stu-id="ba2e8-105">This section includes general information and step-by-step procedures to help you successfully perform the tasks that you must complete at different stages of your deployment.</span></span>

## <span data-ttu-id="ba2e8-106">Bereitstellungsinformationen für UE-V</span><span class="sxs-lookup"><span data-stu-id="ba2e8-106">Deployment information for UE-V</span></span>


<span data-ttu-id="ba2e8-107">Eine UE-v-Bereitstellung erfordert einen Speicherort für Einstellungen auf einer Netzwerkfreigabe und einen UE-v-Agent, der auf jedem Computer installiert ist, auf dem die Einstellungen synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="ba2e8-107">A UE-V deployment requires a settings storage location on a network share and a UE-V agent installed on every computer that synchronizes settings.</span></span> <span data-ttu-id="ba2e8-108">Die UE-v-Gruppenrichtlinienvorlagen können verwendet werden, um UE-v-Einstellungen zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="ba2e8-108">The UE-V Group Policy templates can be used to manage UE-V settings.</span></span> <span data-ttu-id="ba2e8-109">In den folgenden Themen wird beschrieben, wie diese Features bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="ba2e8-109">The following topics describe how to deploy these features.</span></span>

[<span data-ttu-id="ba2e8-110">Bereitstellen des Speicherorts für die Einstellungen für UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="ba2e8-110">Deploying the Settings Storage Location for UE-V 1.0</span></span>](deploying-the-settings-storage-location-for-ue-v-10.md)

<span data-ttu-id="ba2e8-111">Alle UE-V-Bereitstellungen erfordern einen Speicherort für Einstellungen, in dem sich die Einstellungs Pakete befinden, die die synchronisierten Einstellungswerte enthalten.</span><span class="sxs-lookup"><span data-stu-id="ba2e8-111">All UE-V deployments require a settings storage location where the settings packages that contain the synchronized setting values are located.</span></span>

[<span data-ttu-id="ba2e8-112">Bereitstellen von UE-V-Agent</span><span class="sxs-lookup"><span data-stu-id="ba2e8-112">Deploying the UE-V Agent</span></span>](deploying-the-ue-v-agent.md)

<span data-ttu-id="ba2e8-113">Damit die Einstellungen mithilfe von UE-v synchronisiert werden können, muss der UE-v-Agent auf einem Computer installiert sein und ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="ba2e8-113">To synchronize settings by using UE-V, a computer must have the UE-V Agent installed and running.</span></span>

[<span data-ttu-id="ba2e8-114">Installieren der ADMX-Vorlagen für UE-V-Gruppenrichtlinien</span><span class="sxs-lookup"><span data-stu-id="ba2e8-114">Installing the UE-V Group Policy ADMX Templates</span></span>](installing-the-ue-v-group-policy-admx-templates.md)

<span data-ttu-id="ba2e8-115">Sie können Gruppenrichtlinien verwenden, um die UE-v-Einstellungen vorab zu konfigurieren, bevor Sie den UE-v-Agent sowie die standardmäßige UE-v-Konfiguration bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="ba2e8-115">You can use Group Policy to preconfigure UE-V settings before you deploy the UE-V Agent as well as standard UE-V configuration.</span></span>

## <span data-ttu-id="ba2e8-116">Bereitstellungsinformationen für die benutzerdefinierte Vorlagenbereitstellung</span><span class="sxs-lookup"><span data-stu-id="ba2e8-116">Deployment information for custom template deployment</span></span>


<span data-ttu-id="ba2e8-117">Wenn Sie beabsichtigen, benutzerdefinierte Speicherort Vorlagen für Anwendungen zu erstellen, die nicht die Microsoft-Anwendungen sind, die in UE-v enthalten sind, beispielsweise Branchenanwendungen, können Sie einen Vorlagenkatalog für die Einstellungen bereitstellen und den UE-v-Generator installieren, um diese Vorlagen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="ba2e8-117">If you plan to create custom settings location templates for applications other than the Microsoft applications that are included in UE-V, such as line-of-business applications, then you can deploy a settings template catalog and you must install the UE-V Generator to create those templates.</span></span> <span data-ttu-id="ba2e8-118">Weitere Informationen finden Sie unter [Planen der Bereitstellung von benutzerdefinierten Vorlagen für UE-V 1,0](planning-for-custom-template-deployment-for-ue-v-10.md).</span><span class="sxs-lookup"><span data-stu-id="ba2e8-118">For more information, see [Planning for Custom Template Deployment for UE-V 1.0](planning-for-custom-template-deployment-for-ue-v-10.md).</span></span>

[<span data-ttu-id="ba2e8-119">Installieren von UE-V-Generator</span><span class="sxs-lookup"><span data-stu-id="ba2e8-119">Installing the UE-V Generator</span></span>](installing-the-ue-v-generator.md)

<span data-ttu-id="ba2e8-120">Verwenden Sie den UE-V-Generator zum Erstellen, bearbeiten und Überprüfen von Speicherort Vorlagen für benutzerdefinierte Einstellungen, mit denen die Einstellungen anderer Anwendungen als der Standardanwendungen synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="ba2e8-120">Use the UE-V Generator to create, edit, and validate custom settings location templates that help synchronize settings of applications other than the default applications.</span></span>

[<span data-ttu-id="ba2e8-121">Bereitstellen des Katalogs für Einstellungsvorlagen für UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="ba2e8-121">Deploying the Settings Template Catalog for UE-V 1.0</span></span>](deploying-the-settings-template-catalog-for-ue-v-10.md)

<span data-ttu-id="ba2e8-122">Wenn Sie benutzerdefinierte Einstellungen für Standort Vorlagen bereitstellen müssen, um andere Anwendungen als die Standardanwendungen des UE-V-Agents zu unterstützen, müssen Sie einen Einstellungs Vorlagenkatalog konfigurieren, um Sie zu speichern.</span><span class="sxs-lookup"><span data-stu-id="ba2e8-122">If you need to deploy custom settings location templates to support applications other than the default applications in the UE-V Agent, you must configure a settings template catalog to store them.</span></span>

[<span data-ttu-id="ba2e8-123">Bereitstellen von UE-V-Speicherortvorlagen für UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="ba2e8-123">Deploying UE-V Settings Location Templates for UE-V 1.0</span></span>](deploying-ue-v-settings-location-templates-for-ue-v-10.md)

<span data-ttu-id="ba2e8-124">Wenn Sie andere Anwendungen als die Standardanwendungen des UE-v-Agents synchronisieren müssen, können die mit dem UE-v-Generator erstellten benutzerdefinierten Einstellungen für den Speicherort an den Vorlagenkatalog für UE-v-Einstellungen verteilt werden.</span><span class="sxs-lookup"><span data-stu-id="ba2e8-124">If you need to synchronize applications other than the default applications in the UE-V Agent, the custom setting location templates that are created with UE-V Generator can be distributed to the UE-V settings template catalog.</span></span>

<span data-ttu-id="ba2e8-125">**Hinweis**  Das Bereitstellen von benutzerdefinierten Vorlagen erfordert einen Vorlagenkatalog für Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="ba2e8-125">**Note** Deploying custom templates requires a settings template catalog.</span></span> <span data-ttu-id="ba2e8-126">Die Standardvorlagen für Microsoft-Anwendungen werden mit dem UE-V-Agent bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="ba2e8-126">The default Microsoft application templates are deployed with the UE-V Agent.</span></span>

 

## <span data-ttu-id="ba2e8-127">Themen für dieses Produkt</span><span class="sxs-lookup"><span data-stu-id="ba2e8-127">Topics for this product</span></span>


[<span data-ttu-id="ba2e8-128">Microsoft-User Experience Virtualization (UE-V) 1.0</span><span class="sxs-lookup"><span data-stu-id="ba2e8-128">Microsoft User Experience Virtualization (UE-V) 1.0</span></span>](index.md)

[<span data-ttu-id="ba2e8-129">Erste Schritte mit User Experience Virtualization 1.0</span><span class="sxs-lookup"><span data-stu-id="ba2e8-129">Getting Started With User Experience Virtualization 1.0</span></span>](getting-started-with-user-experience-virtualization-10.md)

[<span data-ttu-id="ba2e8-130">Planen für UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="ba2e8-130">Planning for UE-V 1.0</span></span>](planning-for-ue-v-10.md)

[<span data-ttu-id="ba2e8-131">Vorgänge für UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="ba2e8-131">Operations for UE-V 1.0</span></span>](operations-for-ue-v-10.md)

[<span data-ttu-id="ba2e8-132">Problembehandlung für UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="ba2e8-132">Troubleshooting UE-V 1.0</span></span>](troubleshooting-ue-v-10.md)

 

 





