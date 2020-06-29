---
title: End-to-End-Bereitstellungsszenario für MED-V 2.0
description: End-to-End-Bereitstellungsszenario für MED-V 2.0
author: dansimp
ms.assetid: 91bb5a9a-5fb1-4743-8494-9d4dee2ec222
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6d56e70ad359ebf2d76cf3f30f54f73cd9ca1c66
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811596"
---
# <span data-ttu-id="c6320-103">End-to-End-Bereitstellungsszenario für MED-V 2.0</span><span class="sxs-lookup"><span data-stu-id="c6320-103">End-to-End Deployment Scenario for MED-V 2.0</span></span>


<span data-ttu-id="c6320-104">Dieses Beispielszenario für Microsoft Enterprise Desktop Virtualization (Med-v) 2,0 unterstützt Sie beim Bereitstellen der Med-v-Komponenten in Ihrem Unternehmen, indem Sie mehrere Szenarien durchgängig verwenden.</span><span class="sxs-lookup"><span data-stu-id="c6320-104">This sample scenario for Microsoft Enterprise Desktop Virtualization (MED-V) 2.0 helps you deploy the MED-V components in your enterprise by using multiple scenarios end-to-end.</span></span> <span data-ttu-id="c6320-105">Sie können sich dieses Beispielszenario als eine Fallstudie vorstellen, die dazu beiträgt, die einzelnen Szenarien und Prozeduren im Kontext zu platzieren.</span><span class="sxs-lookup"><span data-stu-id="c6320-105">You can think of this sample scenario as a case study that helps put the individual scenarios and procedures in context.</span></span>

<span data-ttu-id="c6320-106">Dieser Abschnitt enthält grundlegende Informationen und Anweisungen zum Bereitstellen von MED-V-Komponenten als End-to-End-Lösung in Ihrem Unternehmen.</span><span class="sxs-lookup"><span data-stu-id="c6320-106">This section provides basic information and directions for deploying MED-V components as an end-to-end solution in your enterprise.</span></span>

## <span data-ttu-id="c6320-107">Schritt-für-Schritt-Szenario für MED-V-Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="c6320-107">MED-V Deployment Step-by-step Scenario</span></span>


<span data-ttu-id="c6320-108">Zu den Themen in diesem schrittweisen Szenario gehören die folgenden:</span><span class="sxs-lookup"><span data-stu-id="c6320-108">The topics in this step-by-step scenario include the following:</span></span>

-   <span data-ttu-id="c6320-109">In den von [Med-v 2,0 unterstützten Konfigurationen](med-v-20-supported-configurations.md) werden die Anforderungen beschrieben, die Sie benötigen, um Microsoft Enterprise Desktop Virtualization (Med-v) 2.0 in Ihrer Umgebung zu installieren und auszuführen.</span><span class="sxs-lookup"><span data-stu-id="c6320-109">[MED-V 2.0 Supported Configurations](med-v-20-supported-configurations.md) discusses the requirements that you must have to install and run Microsoft Enterprise Desktop Virtualization (MED-V) 2.0in your environment.</span></span> <span data-ttu-id="c6320-110">In diesem Thema werden die Betriebssystemanforderungen, die Konfigurationsanforderungen und die Anforderungen des MED-V-Arbeitsbereichs angegeben.</span><span class="sxs-lookup"><span data-stu-id="c6320-110">This topic specifies the operating system requirements, configuration requirements, and MED-V workspace requirements.</span></span> <span data-ttu-id="c6320-111">Dieses Thema enthält auch Lokalisierungsinformationen zu den Sprachen, die von MED-V 2,0 unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="c6320-111">This topic also includes localization information about the languages that MED-V 2.0 supports.</span></span>

-   <span data-ttu-id="c6320-112">In der [Med-v 2,0-Bereitstellungsübersicht](med-v-20-deployment-overview.md) werden allgemeine Informationen und Anweisungen erläutert, die Sie beim Installieren und Bereitstellen von Med-v im gesamten Unternehmen unterstützen.</span><span class="sxs-lookup"><span data-stu-id="c6320-112">[MED-V 2.0 Deployment Overview](med-v-20-deployment-overview.md) discusses general information and instructions to help you install and deploy MED-V throughout your enterprise.</span></span> <span data-ttu-id="c6320-113">Die MED-V-Komponenten sind Client basiert und werden mithilfe Ihrer vorhandenen Unternehmensinfrastruktur und-Prozesse bereitgestellt und verwaltet.</span><span class="sxs-lookup"><span data-stu-id="c6320-113">The MED-V components are client-based and are delivered and managed by using your existing enterprise infrastructure and processes.</span></span> <span data-ttu-id="c6320-114">Dieses Thema enthält eine Übersicht über die Med-v-Lösung, die Informationen zu den Med-v-Installationsdateien und den von Ihnen bereitgestellten Med-v-Komponenten enthält.</span><span class="sxs-lookup"><span data-stu-id="c6320-114">This topic provides an overview of the MED-V solution that includes information about the MED-V installation files and the MED-V components that you deploy.</span></span> <span data-ttu-id="c6320-115">Dieses Thema bietet auch eine allgemeine Übersicht über den MED-V-Installations-und Bereitstellungsprozess.</span><span class="sxs-lookup"><span data-stu-id="c6320-115">This topic also provides a high-level overview of the MED-V installation and deployment process.</span></span>

-   <span data-ttu-id="c6320-116">[Vorbereiten der Bereitstellungsumgebung für med-v](prepare-the-deployment-environment-for-med-v.md) erläutert, wie Sie Ihre Umgebung für eine Med-v 2,0-Bereitstellung vorbereiten.</span><span class="sxs-lookup"><span data-stu-id="c6320-116">[Prepare the Deployment Environment for MED-V](prepare-the-deployment-environment-for-med-v.md) discusses how to prepare your environment for a MED-V 2.0 deployment.</span></span> <span data-ttu-id="c6320-117">In diesem Abschnitt werden die Voraussetzungen beschrieben, die für die MED-V-Umgebung erforderlich sind, wie etwa Microsoft Windows 7 und eine Active Directory-Infrastruktur, in der Sie Gruppenrichtlinien verwenden, um eine zentralisierte Verwaltung und Konfiguration von Betriebssystemen, Anwendungen und Benutzereinstellungen bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="c6320-117">This section describes the prerequisites that are required for the MED-V environment, such as Microsoft Windows 7 and an Active Directory infrastructure in which you use Group Policy to provide centralized management and configuration of operating systems, applications, and users' settings.</span></span> <span data-ttu-id="c6320-118">In diesem Abschnitt werden auch die Voraussetzungen beschrieben, die Sie für die Installation und Bereitstellung von MED-V 2,0 im gesamten Unternehmen benötigen, wie etwa Windows Virtual PC und das erforderliche Windows Virtual PC-Update.</span><span class="sxs-lookup"><span data-stu-id="c6320-118">This section also describes the prerequisites that you must have for installing and deploying MED-V 2.0 throughout your enterprise, such as Windows Virtual PC and the required Windows Virtual PC update.</span></span>

-   <span data-ttu-id="c6320-119">[Bereitstellen der Med-v-Komponenten](deploy-the-med-v-components.md) beschreibt die verschiedenen Möglichkeiten, wie Sie alle erforderlichen Installationsdateien und Med-v-Komponenten im gesamten Unternehmen installieren können.</span><span class="sxs-lookup"><span data-stu-id="c6320-119">[Deploy the MED-V Components](deploy-the-med-v-components.md) discusses the different ways you can install all of the necessary installation files and MED-V components throughout your enterprise.</span></span> <span data-ttu-id="c6320-120">Zum Installieren und Bereitstellen von MED-V führen Sie in der Regel die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="c6320-120">To install and deploy MED-V, you typically follow these steps:</span></span>

    1.  <span data-ttu-id="c6320-121">Installieren Sie den **Med-v Workspace Packager** auf dem Administratorcomputer, den Sie zum Erstellen der Med-v Workspace-Pakete verwenden werden.</span><span class="sxs-lookup"><span data-stu-id="c6320-121">Install the **MED-V Workspace Packager** on the administrator computer that you will use to build the MED-V workspace packages.</span></span> <span data-ttu-id="c6320-122">Weitere Informationen finden Sie unter [so wird es gemacht: Installieren des MED-V-Arbeitsbereichs Pakets](how-to-install-the-med-v-workspace-packager.md).</span><span class="sxs-lookup"><span data-stu-id="c6320-122">For more information, see [How to Install the MED-V Workspace Packager](how-to-install-the-med-v-workspace-packager.md).</span></span>

    2.  <span data-ttu-id="c6320-123">Erstellen und testen Sie Ihre MED-V-Arbeitsbereichs Pakete.</span><span class="sxs-lookup"><span data-stu-id="c6320-123">Create and test your MED-V workspace packages.</span></span> <span data-ttu-id="c6320-124">Weitere Informationen finden Sie unter [Erstellen eines Med-v-Arbeitsbereichs Pakets](create-a-med-v-workspace-package.md) und [Testen des Med-v-Arbeitsbereichs Pakets](testing-the-med-v-workspace-package.md).</span><span class="sxs-lookup"><span data-stu-id="c6320-124">For more information, see [Create a MED-V Workspace Package](create-a-med-v-workspace-package.md) and [Testing the MED-V Workspace Package](testing-the-med-v-workspace-package.md).</span></span>

    3.  <span data-ttu-id="c6320-125">Stellen Sie MED-V im gesamten Unternehmen bereit, indem Sie die vorhandene Methode des Unternehmens zum Bereitstellen von Anwendungen verwenden.</span><span class="sxs-lookup"><span data-stu-id="c6320-125">Deploy MED-V throughout your enterprise by using your company’s existing method for deploying applications.</span></span> <span data-ttu-id="c6320-126">Weitere Informationen finden Sie unter [Bereitstellen des MED-V-Arbeitsbereichs Pakets](deploying-the-med-v-workspace-package.md).</span><span class="sxs-lookup"><span data-stu-id="c6320-126">For more information, see [Deploying the MED-V Workspace Package](deploying-the-med-v-workspace-package.md).</span></span>

## <span data-ttu-id="c6320-127">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="c6320-127">Related topics</span></span>


[<span data-ttu-id="c6320-128">Bereitstellung von MED-V</span><span class="sxs-lookup"><span data-stu-id="c6320-128">Deployment of MED-V</span></span>](deployment-of-med-v.md)

[<span data-ttu-id="c6320-129">End-to-End-Planungszenario für MED-V 2.0</span><span class="sxs-lookup"><span data-stu-id="c6320-129">End-to-End Planning Scenario for MED-V 2.0</span></span>](end-to-end-planning-scenario-for-med-v-20.md)

[<span data-ttu-id="c6320-130">End-to-End-Vorgangsszenario für MED-V 2.0</span><span class="sxs-lookup"><span data-stu-id="c6320-130">End-to-End Operations Scenario for MED-V 2.0</span></span>](end-to-end-operations-scenario-for-med-v-20.md)

 

 





