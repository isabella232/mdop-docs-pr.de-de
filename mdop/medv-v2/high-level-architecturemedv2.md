---
title: High-Level-Architektur
description: High-Level-Architektur
author: dansimp
ms.assetid: a00edb9f-207b-4f32-9e8f-522ea2739d2f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8a5db4a56b2abfb0df19b0d6d86f4bf88380c2bf
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812268"
---
# <span data-ttu-id="4a1cb-103">High-Level-Architektur</span><span class="sxs-lookup"><span data-stu-id="4a1cb-103">High-Level Architecture</span></span>


<span data-ttu-id="4a1cb-104">In diesem Abschnitt werden die allgemeine Systemarchitektur und der Komponentenentwurf von Microsoft Enterprise Desktop Virtualization (MED-V) 2,0 beschrieben.</span><span class="sxs-lookup"><span data-stu-id="4a1cb-104">This section describes the high-level system architecture and component design of Microsoft Enterprise Desktop Virtualization (MED-V) 2.0.</span></span>

## <span data-ttu-id="4a1cb-105">System Architektur</span><span class="sxs-lookup"><span data-stu-id="4a1cb-105">System Architecture</span></span>


<span data-ttu-id="4a1cb-106">MED-V verbessert den Windows Virtual PC, um zwei Betriebssysteme auf einem Gerät auszuführen, wobei die Bereitstellung virtueller Bilder, die gruppenrichtlinienbasierte Bereitstellung und die zentralisierte Verwaltung hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="4a1cb-106">MED-V enhances Windows Virtual PC to run two operating systems on one device, adding virtual image delivery, Group Policy-based provisioning, and centralized management.</span></span> <span data-ttu-id="4a1cb-107">Mithilfe von MED-V können Sie Windows Virtual PC-Images auf einem beliebigen Windows-basierten Desktop, auf dem Windows 7 Professional, Enterprise oder Windows 7 Ultimate ausgeführt wird, problemlos konfigurieren, bereitstellen und verwalten.</span><span class="sxs-lookup"><span data-stu-id="4a1cb-107">By using MED-V, you can easily configure, deploy, and manage corporate Windows Virtual PC images on any Windows-based desktop running Windows 7 Professional, Enterprise, or Windows 7 Ultimate.</span></span> <span data-ttu-id="4a1cb-108">Die MED-V-Lösung umfasst die folgenden Komponenten:</span><span class="sxs-lookup"><span data-stu-id="4a1cb-108">The MED-V solution includes the following components:</span></span>

<a href="" id="---------------med-v-host"></a> **<span data-ttu-id="4a1cb-109">MED-V-Host</span><span class="sxs-lookup"><span data-stu-id="4a1cb-109">MED-V Host</span></span>**  
<span data-ttu-id="4a1cb-110">Eine Windows 7-Umgebung mit einem Med-v-Host-Agent, einem ESD-System (Electronic Software Distribution), einem Registrierungs Verwaltungssystem und einem Med-v-Gast.</span><span class="sxs-lookup"><span data-stu-id="4a1cb-110">A Windows 7 environment that includes a MED-V Host Agent, an electronic software distribution (ESD) system, a registry management system, and a MED-V guest.</span></span> <span data-ttu-id="4a1cb-111">Der Med-v-Host interagiert mit dem Med-v-Gast, damit bestimmte Setup Funktionen und Systeminformationen verarbeitet werden können.</span><span class="sxs-lookup"><span data-stu-id="4a1cb-111">The MED-V host interacts with the MED-V guest so that certain setup functions and system information can be processed.</span></span>

<a href="" id="-------------------med-v-host-agent"></a> **<span data-ttu-id="4a1cb-112">MED-V-Host-Agent</span><span class="sxs-lookup"><span data-stu-id="4a1cb-112">MED-V Host Agent</span></span>**  
<span data-ttu-id="4a1cb-113">Die im Med-v-Host enthaltene Med-v-Software, die einen Kanal für die Kommunikation mit dem Med-v-Gast bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="4a1cb-113">The MED-V software contained in the MED-V host that provides a channel to communicate with the MED-V guest.</span></span> <span data-ttu-id="4a1cb-114">Darüber hinaus bietet es Funktionen wie das erstmalige Einrichten und die Anwendungsveröffentlichung.</span><span class="sxs-lookup"><span data-stu-id="4a1cb-114">It also provides functionality such as first time setup and application publishing.</span></span>

<span data-ttu-id="4a1cb-115">**Hinweis**  Nachdem Med-v und die erforderlichen Komponenten installiert sind, muss Med-v konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="4a1cb-115">**Note** After MED-V and its required components are installed MED-V must be configured.</span></span> <span data-ttu-id="4a1cb-116">Die Konfiguration von MED-V wird als erstmalige Einrichtung bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="4a1cb-116">The configuration of MED-V is referred to as first time setup.</span></span>

 

<a href="" id="esd-system"></a>**<span data-ttu-id="4a1cb-117">ESD-System</span><span class="sxs-lookup"><span data-stu-id="4a1cb-117">ESD System</span></span>**  
<span data-ttu-id="4a1cb-118">Ihre vorhandene Softwareverteilungsmethode, mit der Sie die von Med-v erstellten Med-v-Arbeitsbereichs Paketdateien bereitstellen und installieren können.</span><span class="sxs-lookup"><span data-stu-id="4a1cb-118">Your existing software distribution method that lets you deploy and install the MED-V workspace package files that MED-V creates.</span></span>

<a href="" id="registry-management-system"></a>**<span data-ttu-id="4a1cb-119">Registrierungs Verwaltungs System</span><span class="sxs-lookup"><span data-stu-id="4a1cb-119">Registry Management System</span></span>**  
<span data-ttu-id="4a1cb-120">Ihre vorhandene Methode zum Verwalten von Gruppenrichtlinieneinstellungen und-Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="4a1cb-120">Your existing method of managing Group Policy settings and preferences.</span></span>

<a href="" id="windows-virtual-pc-image"></a>**<span data-ttu-id="4a1cb-121">Windows Virtual PC-Bild</span><span class="sxs-lookup"><span data-stu-id="4a1cb-121">Windows Virtual PC Image</span></span>**  
<span data-ttu-id="4a1cb-122">Ein vom Administrator definierter virtueller Computer, der die folgenden Komponenten enthält:</span><span class="sxs-lookup"><span data-stu-id="4a1cb-122">An administrator-defined virtual machine that contains the following components:</span></span>

<a href="" id="corporate-operating-system"></a>**<span data-ttu-id="4a1cb-123">Betriebs System des Unternehmens</span><span class="sxs-lookup"><span data-stu-id="4a1cb-123">Corporate Operating System</span></span>**  
<span data-ttu-id="4a1cb-124">Ihr Standard-Betriebssystem für Unternehmen.</span><span class="sxs-lookup"><span data-stu-id="4a1cb-124">Your standard corporate operating system.</span></span>

<a href="" id="management-and-security-tools"></a>**<span data-ttu-id="4a1cb-125">Verwaltungs-und Sicherheits Tools</span><span class="sxs-lookup"><span data-stu-id="4a1cb-125">Management and Security Tools</span></span>**  
<span data-ttu-id="4a1cb-126">Ihre standardmäßigen Verwaltungs-und Sicherheitstools wie Virenschutz.</span><span class="sxs-lookup"><span data-stu-id="4a1cb-126">Your standard management and security tools, such as virus protection.</span></span>

<a href="" id="-----------------------med-v-guest"></a> **<span data-ttu-id="4a1cb-127">MED-V-Gast</span><span class="sxs-lookup"><span data-stu-id="4a1cb-127">MED-V Guest</span></span>**  
<span data-ttu-id="4a1cb-128">Eine Windows XP SP3-Umgebung als Teil eines Windows Virtual PC unter Windows 7 mit den folgenden Komponenten:</span><span class="sxs-lookup"><span data-stu-id="4a1cb-128">A Windows XP SP3 environment, as part of a Windows Virtual PC running on Windows 7 that contains the following components:</span></span>

<a href="" id="---------------------------med-v-guest-agent"></a> **<span data-ttu-id="4a1cb-129">MED-V-Gast-Agent</span><span class="sxs-lookup"><span data-stu-id="4a1cb-129">MED-V Guest Agent</span></span>**  
<span data-ttu-id="4a1cb-130">Die im Med-v-Gast enthaltene Med-v-Software, die einen Kanal für die Kommunikation mit dem Med-v-Host bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="4a1cb-130">The MED-V software contained in the MED-V guest that provides a channel to communicate with the MED-V host.</span></span> <span data-ttu-id="4a1cb-131">Darüber hinaus unterstützt der MED-V-Host-Agent Funktionen wie das Durchführen der erstmaligen Einrichtung.</span><span class="sxs-lookup"><span data-stu-id="4a1cb-131">It also supports the MED-V Host Agent with functions like performing first time setup.</span></span>

<span data-ttu-id="4a1cb-132">**Hinweis**  Der MED-V-Gast-Agent wird während der erstmaligen Einrichtung automatisch installiert.</span><span class="sxs-lookup"><span data-stu-id="4a1cb-132">**Note** The MED-V Guest Agent is installed automatically during first time setup.</span></span>

 

<a href="" id="esd-client"></a>**<span data-ttu-id="4a1cb-133">ESD-Client</span><span class="sxs-lookup"><span data-stu-id="4a1cb-133">ESD Client</span></span>**  
<span data-ttu-id="4a1cb-134">Ein optionaler Teil Ihres ESD-Systems, mit dem Softwarepakete und Statusberichte für das ESD-System installiert werden.</span><span class="sxs-lookup"><span data-stu-id="4a1cb-134">An optional part of your ESD system that installs software packages and reports status to the ESD system.</span></span>

## <span data-ttu-id="4a1cb-135">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="4a1cb-135">Related topics</span></span>


[<span data-ttu-id="4a1cb-136">Planen der Betriebssystemkompatibilität der Anwendung</span><span class="sxs-lookup"><span data-stu-id="4a1cb-136">Planning for Application Operating System Compatibility</span></span>](planning-for-application-operating-system-compatibility.md)

[<span data-ttu-id="4a1cb-137">Vorbereiten der Bereitstellungsumgebung für MED-V</span><span class="sxs-lookup"><span data-stu-id="4a1cb-137">Prepare the Deployment Environment for MED-V</span></span>](prepare-the-deployment-environment-for-med-v.md)

 

 





