---
title: Definieren Sie den Projektumfang
description: Definieren Sie den Projektumfang
author: dansimp
ms.assetid: 84637d2a-2e30-417d-b150-dc81f414b3a5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4f33562452327bba9036f56d9f6f96650f00c1f0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810078"
---
# <span data-ttu-id="a997d-103">Definieren Sie den Projektumfang</span><span class="sxs-lookup"><span data-stu-id="a997d-103">Define the Project Scope</span></span>


<span data-ttu-id="a997d-104">Legen Sie beim Definieren des Projektumfangs Folgendes fest:</span><span class="sxs-lookup"><span data-stu-id="a997d-104">When defining the project scope, determine the following:</span></span>

1.  <span data-ttu-id="a997d-105">Die Med-v-Endbenutzer – der Speicherort und die Anzahl der Endbenutzer werden verwendet, um den Standort der Med-v-Clientinstallationen und die Anzahl der Med-v-Instanzen sowie die Anzahl und die Platzierung von Med-v-Bild Depots zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="a997d-105">The MED-V end users—the location and number of end users are used in determining the location of MED-V client installations and the number of MED-V instances, as well as the number and placement of MED-V image repositories.</span></span>

2.  <span data-ttu-id="a997d-106">Die VM-Bilder (Virtual Machine), die von MED-V verwaltet werden sollen, um die Methode zum Verteilen von Bildern und zur Platzierung von Bild-Repositories zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="a997d-106">The virtual machine (VM) images to be managed by MED-V—to determine the method of distributing images and placement of image repositories.</span></span>

3.  <span data-ttu-id="a997d-107">Die Erwartungen des Unternehmens an den Service Level: Ermitteln der Leistungs-und Fehlertoleranzanforderungen für den MED-V-Server und die Datenbank sowie das Bild-Repository.</span><span class="sxs-lookup"><span data-stu-id="a997d-107">The organization’s service level expectations—to determine the performance and fault-tolerance requirements for the MED-V server and database as well as the image repository.</span></span>

4.  <span data-ttu-id="a997d-108">Überprüfen Sie mit dem Unternehmen – stellen Sie sicher, dass Sie wissen, wie sich die geplante Infrastruktur auf das Unternehmen auswirkt.</span><span class="sxs-lookup"><span data-stu-id="a997d-108">Validate with the business—ensure there is a complete understanding of how the planned infrastructure affects the business.</span></span>

## <span data-ttu-id="a997d-109">Definieren der MED-V-Endbenutzer</span><span class="sxs-lookup"><span data-stu-id="a997d-109">Define the MED-V End Users</span></span>


<span data-ttu-id="a997d-110">Ermitteln Sie zunächst, wo sich die Endbenutzer befinden, sowie die Anzahl der Benutzer an jedem Standort.</span><span class="sxs-lookup"><span data-stu-id="a997d-110">First, determine where the end users are located, as well as the number of users in each location.</span></span> <span data-ttu-id="a997d-111">Rufen Sie als nächstes ein Netzwerkinfrastruktur Diagramm ab, in dem die Benutzerspeicherorte und die verfügbare Bandbreite an diesen Speicherorten angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="a997d-111">Second, obtain a network infrastructure diagram that displays the user locations and the available bandwidth to those locations.</span></span> <span data-ttu-id="a997d-112">Drittens: finden Sie heraus, ob Benutzerzwischenspeicher Orten reisen.</span><span class="sxs-lookup"><span data-stu-id="a997d-112">Third, find out if users travel between locations.</span></span> <span data-ttu-id="a997d-113">Wenn Benutzer Reisen, ist möglicherweise zusätzliche Kapazität beim Entwurf der Serverinfrastruktur und der Bild Depots erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a997d-113">If users travel, additional capacity may be required in the design of the server infrastructure and image repositories.</span></span>

## <span data-ttu-id="a997d-114">Ermitteln der Med-v-Bilder, die von Med-v verwaltet werden sollen</span><span class="sxs-lookup"><span data-stu-id="a997d-114">Determine the MED-V Images to Be Managed by MED-V</span></span>


<span data-ttu-id="a997d-115">Nachdem die Med-v-Endbenutzer definiert wurden, ermitteln Sie, welche VMS von Med-v für die Benutzer an den einzelnen Speicherorten verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="a997d-115">After the MED-V end users have been defined, determine which VMs will be managed by MED-V for the users in each location.</span></span>

<span data-ttu-id="a997d-116">Wenn eines der VMs in einer zentralisierten Bibliothek gespeichert ist, ermitteln Sie den Speicherort der Bibliothek, damit Sie für die Verwendung als MED-V-Repository ausgewertet werden kann.</span><span class="sxs-lookup"><span data-stu-id="a997d-116">If any of the VMs are stored in a centralized library, determine the location of the library so that it may be evaluated for use as a MED-V repository.</span></span>

## <a href="" id="determine-the-organization-s-service-level-expectations"></a><span data-ttu-id="a997d-117">Ermitteln der Service-Level-Erwartungen des Unternehmens</span><span class="sxs-lookup"><span data-stu-id="a997d-117">Determine the Organization’s Service Level Expectations</span></span>


<span data-ttu-id="a997d-118">Notieren Sie sich für jeden MED-V-Arbeitsbereich die akzeptable Zeit, zu der ein neues Bild geladen werden soll, und den Zeitrahmen für die Bereitstellung kritischer Updates.</span><span class="sxs-lookup"><span data-stu-id="a997d-118">For each MED-V workspace, note the acceptable time for a new image to load and the timeframe for critical updates to be deployed.</span></span>

<span data-ttu-id="a997d-119">Notieren Sie sich ggf. die Erwartungen des Service Levels für MED-V-Berichte, die beim Entwurf der Serverinfrastruktur zu verwenden sind.</span><span class="sxs-lookup"><span data-stu-id="a997d-119">If applicable, record the service level expectations for MED-V reporting, to be used in the design of the server infrastructure.</span></span>

## <span data-ttu-id="a997d-120">Überprüfen mit dem Unternehmen</span><span class="sxs-lookup"><span data-stu-id="a997d-120">Validate with the Business</span></span>


<span data-ttu-id="a997d-121">Bitten Sie Unternehmen und Anwendungsbesitzer, die folgenden Fragen zu beantworten:</span><span class="sxs-lookup"><span data-stu-id="a997d-121">Ask business stakeholders and application owners the following questions:</span></span>

-   <span data-ttu-id="a997d-122">Gibt es vorhandene Bilder, die kombiniert werden können?</span><span class="sxs-lookup"><span data-stu-id="a997d-122">Are there any existing images that can be combined?</span></span> <span data-ttu-id="a997d-123">Wenn beispielsweise die Anwendung a unter WindowsXP ein VPC-Bild und die Anwendung B unter WindowsXP ein weiteres VPC-Abbild ist, kann ein einzelnes Bild möglicherweise beide Anwendungen enthalten und dadurch den Speicherplatz und die Bandbreite reduzieren, die für den Download von Bildern erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="a997d-123">For example, if application A on WindowsXP is one VPC image and application B on WindowsXP is another VPC image, perhaps a single image can contain both applications, thereby reducing repository space and bandwidth required for image download.</span></span>

-   <span data-ttu-id="a997d-124">Sind die in-Scope-Anwendungen lizenziert und unterstützt, wenn Sie von MED-V in einem VM bereitgestellt werden?</span><span class="sxs-lookup"><span data-stu-id="a997d-124">Are the in-scope applications licensable and supportable if delivered in a VM by MED-V?</span></span> <span data-ttu-id="a997d-125">Wenden Sie sich an den Anbieter der Anwendung, um sicherzustellen, dass die Lizenz-und Support Bestimmungen nicht verletzt werden, indem Sie die Anwendung über MED-V bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="a997d-125">Check with the application supplier to ensure that licensing and support terms will not be violated by delivering the application through MED-V.</span></span>

 

 





