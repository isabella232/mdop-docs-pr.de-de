---
title: Planen für UE-V-Konfigurationsmethoden
description: Planen für UE-V-Konfigurationsmethoden
author: dansimp
ms.assetid: 57bce7ab-1be5-434b-9ee5-c96026bbe010
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4894644d72392ae984d0de290bf634e137d5b85e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812148"
---
# <span data-ttu-id="28f29-103">Planen für UE-V-Konfigurationsmethoden</span><span class="sxs-lookup"><span data-stu-id="28f29-103">Planning for UE-V Configuration Methods</span></span>


<span data-ttu-id="28f29-104">Microsoft User Experience Virtualization (UE-V)-Konfigurationen legen fest, wie Einstellungen im gesamten Unternehmen synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="28f29-104">Microsoft User Experience Virtualization (UE-V) configurations determine how settings are synchronized throughout the enterprise.</span></span> <span data-ttu-id="28f29-105">In diesem Thema wird beschrieben, wie UE-V-Konfigurationen erstellt werden, die Ihnen helfen, einen Konfigurationsplan zu formulieren, der Ihren geschäftlichen Anforderungen am besten entspricht.</span><span class="sxs-lookup"><span data-stu-id="28f29-105">This topic describes how UE-V configurations are created to help you formulate a configuration plan that best meets your business requirements.</span></span>

## <span data-ttu-id="28f29-106">Konfigurationsmethoden für UE-V</span><span class="sxs-lookup"><span data-stu-id="28f29-106">Configuration methods for UE-V</span></span>


<span data-ttu-id="28f29-107">Je nach verwendeter Konfigurationsmethode können Sie UE-V vor, während oder nach der Agenteninstallation konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="28f29-107">You can configure UE-V before, during, or after agent installation, depending on the configuration method that you use.</span></span>

<span data-ttu-id="28f29-108">**Gruppenrichtlinie:** vorhandene Gruppenrichtlinieninfrastruktur kann verwendet werden, um UE-v vor oder nach der Bereitstellung des UE-v-Agents zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="28f29-108">**Group Policy:** existing Group Policy infrastructure can be used to configure UE-V before or after UE-V Agent deployment.</span></span> <span data-ttu-id="28f29-109">Die UE-v-ADMX-Vorlage ermöglicht die zentrale Verwaltung von allgemeinen UE-v-Agent-Konfigurationsoptionen und umfasst Einstellungen für die Konfiguration der UE-v-Synchronisierung.</span><span class="sxs-lookup"><span data-stu-id="28f29-109">The UE-V ADMX template enables the central management of common UE-V Agent configuration options, and it includes settings to configure UE-V synchronization.</span></span> <span data-ttu-id="28f29-110">Netzwerkumgebungen, die Gruppenrichtlinien verwenden, können UE-V in Erwartung der agentenbereitstellung vorkonfigurieren.</span><span class="sxs-lookup"><span data-stu-id="28f29-110">Network environments that use Group Policy can preconfigure UE-V in anticipation of agent deployment.</span></span>

[<span data-ttu-id="28f29-111">Konfigurieren von UE-V mit Gruppenrichtlinienobjekten</span><span class="sxs-lookup"><span data-stu-id="28f29-111">Configuring UE-V with Group Policy Objects</span></span>](configuring-ue-v-with-group-policy-objects.md)

[<span data-ttu-id="28f29-112">Installieren der ADMX-Vorlagen für UE-V-Gruppenrichtlinien</span><span class="sxs-lookup"><span data-stu-id="28f29-112">Installing the UE-V Group Policy ADMX Templates</span></span>](installing-the-ue-v-group-policy-admx-templates.md)

<span data-ttu-id="28f29-113">**Befehlszeilen-oder Batch Skript Installation:** Parameter, die für die Bereitstellung des UE-v-Agents verwendet werden, ermöglichen die Konfiguration vieler UE-v-Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="28f29-113">**Command-line or Batch Script Installation:** parameters that are used with the deployment of the UE-V Agent allow the configuration of many UE-V settings.</span></span> <span data-ttu-id="28f29-114">Elektronische Softwareverteilungssysteme wie System Center Configuration Manager verwenden diese Parameter, um Ihre Clients beim Bereitstellen und Installieren der UE-V-Agentensoftware zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="28f29-114">Electronic software distribution systems, such as System Center Configuration Manager, use these parameters to configure their clients when deploying and installing the UE-V Agent software.</span></span> <span data-ttu-id="28f29-115">Eine Liste der Installationsparameter und Beispiel Installationsskripts finden Sie unter [Bereitstellen des UE-V-Agents](deploying-the-ue-v-agent.md).</span><span class="sxs-lookup"><span data-stu-id="28f29-115">For a list of installation parameters and sample installation scripts, see [Deploying the UE-V Agent](deploying-the-ue-v-agent.md).</span></span>

<span data-ttu-id="28f29-116">**PowerShell und WMI:** skriptgesteuerte Befehle mit PowerShell oder WMI können verwendet werden, um Konfigurationen nach der Installation des UE-V-Agents zu ändern.</span><span class="sxs-lookup"><span data-stu-id="28f29-116">**PowerShell and WMI:** scripted commands using PowerShell or WMI can be used to modify configurations after the UE-V Agent has been installed.</span></span> <span data-ttu-id="28f29-117">Eine Liste mit PowerShell-und WMI-Befehlen finden Sie unter [Verwalten des UE-V 1,0-Agents und von Paketen mit PowerShell und WMI](managing-the-ue-v-10-agent-and-packages-with-powershell-and-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="28f29-117">For a list of PowerShell and WMI commands, see [Managing the UE-V 1.0 Agent and Packages with PowerShell and WMI](managing-the-ue-v-10-agent-and-packages-with-powershell-and-wmi.md).</span></span>

<span data-ttu-id="28f29-118">**Bearbeiten von Registrierungseinstellungen:** UE-V-Einstellungen werden in der Registrierung gespeichert und können mithilfe eines beliebigen Tools geändert werden, mit dem Registrierungseinstellungen wie Regedit geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="28f29-118">**Edit Registry Settings:** UE-V settings are stored in the registry and can be modified by using any tool that can modify registry settings, such as RegEdit.</span></span>

<span data-ttu-id="28f29-119">**Hinweis**  Die Änderung der Registrierung kann zu Datenverlust führen, oder der Computer reagiert nicht mehr.</span><span class="sxs-lookup"><span data-stu-id="28f29-119">**Note** Registry modification can result in data loss or the computer becoming unresponsive.</span></span> <span data-ttu-id="28f29-120">Wir empfehlen, dass Sie andere Konfigurationsmethoden verwenden.</span><span class="sxs-lookup"><span data-stu-id="28f29-120">We recommend that you use other configuration methods.</span></span>

 

### <span data-ttu-id="28f29-121">UE-V-Konfigurationseinstellungen</span><span class="sxs-lookup"><span data-stu-id="28f29-121">UE-V configuration settings</span></span>

<span data-ttu-id="28f29-122">Im folgenden finden Sie Beispiele für UE-V-Konfigurationseinstellungen:</span><span class="sxs-lookup"><span data-stu-id="28f29-122">The following are examples of UE-V configuration settings:</span></span>

-   <span data-ttu-id="28f29-123">**Festlegen des Speicherpfads:** gibt den Speicherort der Dateifreigabe an, in der die UE-V-Einstellungen gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="28f29-123">**Setting Storage Path:** specifies the location of the file share that stores the UE-V settings.</span></span>

-   <span data-ttu-id="28f29-124">**Katalogpfad für Einstellungs Vorlagen:** gibt den UNC-Pfad (Universal Naming Convention) an, der den Speicherort definiert, der auf neue Einstellungen für Standort Vorlagen überprüft wurde.</span><span class="sxs-lookup"><span data-stu-id="28f29-124">**Settings Template Catalog Path:** specifies the Universal Naming Convention (UNC) path that defines the location that was checked for new settings location templates.</span></span>

-   <span data-ttu-id="28f29-125">**Microsoft-Vorlagen registrieren:** gibt an, ob die Microsoft-Standardvorlagen während der Installation registriert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="28f29-125">**Register Microsoft Templates:** specifies whether the default Microsoft templates should be registered during installation.</span></span>

-   <span data-ttu-id="28f29-126">**Synchronisierungsmethode:** gibt an, ob das Feature Windows-Offlinedateien für die Offlineunterstützung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="28f29-126">**Synchronization Method:** specifies whether the Windows Offline Files feature is used for offline support.</span></span>

-   <span data-ttu-id="28f29-127">**Synchronisierungs Timeout:** gibt die Anzahl der Millisekunden an, die der Computer vor dem Timeout abwartet, wenn die Benutzereinstellungen vom Speicherort der Einstellungen abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="28f29-127">**Synchronization Timeout:** specifies the number of milliseconds that the computer waits before timeout when retrieving the user settings from the settings storage location.</span></span>

-   <span data-ttu-id="28f29-128">**Synchronisierungs Aktivierung:** gibt an, ob die Synchronisierung der UE-V-Einstellungen aktiviert oder deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="28f29-128">**Synchronization Enable:** specifies whether the UE-V settings synchronization is enabled or disabled.</span></span>

-   <span data-ttu-id="28f29-129">**Maximale Paketgröße:** gibt die Größe des Einstellungen-Paketdatei-Schwellenwerts in Bytes an, bei dem der UE-V-Agent eine Warnung meldet.</span><span class="sxs-lookup"><span data-stu-id="28f29-129">**Maximum Package Size:** specifies a settings package file threshold size in bytes at which the UE-V Agent reports a warning.</span></span>

## <span data-ttu-id="28f29-130">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="28f29-130">Related topics</span></span>


[<span data-ttu-id="28f29-131">Planen für UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="28f29-131">Planning for UE-V 1.0</span></span>](planning-for-ue-v-10.md)

[<span data-ttu-id="28f29-132">Planen der UE-V-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="28f29-132">Planning for UE-V Configuration</span></span>](planning-for-ue-v-configuration.md)

 

 





