---
title: Erkennen von Netzwerkänderungen, die MED-V beeinflussen
description: Erkennen von Netzwerkänderungen, die MED-V beeinflussen
author: dansimp
ms.assetid: fd29b95a-cda2-464d-b86d-50b6bd64b4ca
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b5f43c30dee9ef8e06a7ae226849a4f21e83257c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809916"
---
# <span data-ttu-id="0171b-103">Erkennen von Netzwerkänderungen, die MED-V beeinflussen</span><span class="sxs-lookup"><span data-stu-id="0171b-103">Detecting Network Changes that Affect MED-V</span></span>


<span data-ttu-id="0171b-104">Mit der Microsoft Enterprise Desktop Virtualization (Med-v) 2,0-Lösung können Sie Ihre Umgebung so konfigurieren, dass bestimmte Netzwerkänderungen erkannt werden, die möglicherweise nach der Bereitstellung von Med-v-Arbeitsbereichen auftreten und sich auf Med-v auswirken können.</span><span class="sxs-lookup"><span data-stu-id="0171b-104">The Microsoft Enterprise Desktop Virtualization (MED-V) 2.0 solution lets you configure your environment to detect certain network changes that might occur after MED-V workspaces are deployed and that can affect MED-V.</span></span>

<span data-ttu-id="0171b-105">Das Feature umfasst eine im Gastbetriebssystem ausgeführte Komponente, die über Änderungen an der Netzwerkkonfiguration auf dem Hostcomputer benachrichtigt wird.</span><span class="sxs-lookup"><span data-stu-id="0171b-105">The feature includes a component running in the guest operating system that is notified of network configuration changes on the host computer.</span></span> <span data-ttu-id="0171b-106">Damit kann eine nicht von Microsoft ausgeführte ESD-oder andere Anwendung, die im Gast ausgeführt wird, zu denselben Netzwerkendpunkten aufgelöst werden, zu denen die Host-ESD oder-Anwendung aufgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="0171b-106">It allows a non-Microsoft ESD or other application that is running in the guest to resolve to the same network endpoints that the host ESD or application resolves to.</span></span>

<span data-ttu-id="0171b-107">**Hinweis**  Dieses Feature ist nur verfügbar, wenn der virtuelle Computer für den NAT-Modus (Network Address Translation) konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="0171b-107">**Note** This feature is only available if the virtual machine is configured for network address translation (NAT) mode.</span></span> <span data-ttu-id="0171b-108">Wenn der virtuelle Computer für den Überbrückungsmodus konfiguriert ist, werden keine Änderungshinweise generiert.</span><span class="sxs-lookup"><span data-stu-id="0171b-108">If the virtual machine is configured for BRIDGED mode, no change indications are generated.</span></span>

 

<span data-ttu-id="0171b-109">Dieser Abschnitt enthält Informationen und Anweisungen zur Unterstützung bei der Überwachung dieser Netzwerkänderungen, die sich auf MED-V auswirken können.</span><span class="sxs-lookup"><span data-stu-id="0171b-109">This section provides information and instruction to assist you in monitoring those network changes that can affect MED-V.</span></span>

## <span data-ttu-id="0171b-110">So erkennen Sie Netzwerkänderungen für MED-V</span><span class="sxs-lookup"><span data-stu-id="0171b-110">To detect network changes for MED-V</span></span>


<span data-ttu-id="0171b-111">Nachdem Sie Ihre MED-V-Arbeitsbereiche bereitgestellt haben, können Sie Änderungen an bestimmten Netzwerkkonfigurationen überwachen, indem Sie die folgenden Aufgaben Vorformen:</span><span class="sxs-lookup"><span data-stu-id="0171b-111">After you have deployed your MED-V workspaces, you can monitor changes to certain network configurations by preforming the following tasks:</span></span>

1. <span data-ttu-id="0171b-112">Erstellen Sie eine MOF-Datei (Managed Object Format), die nach den Netzwerkkonfigurationsänderungen sucht, die überwacht werden sollen.</span><span class="sxs-lookup"><span data-stu-id="0171b-112">Create a Managed Object Format (MOF) file that will look for the network configuration changes that you want to monitor.</span></span> <span data-ttu-id="0171b-113">Der folgende Code zeigt ein Beispiel für die MOF-Datei, die Sie erstellen können.</span><span class="sxs-lookup"><span data-stu-id="0171b-113">The following code shows an example of the MOF file that you can create.</span></span>

   ``` syntax
   #pragma namespace ("\\\\.\\root\\ccm\\NetworkConfig")

   class CCM_IPConfig
   {
       [NotNull: ToInstance ToSubClass] uint32 AddressFamily; // AF_INET, AF_INET6
       [Key, NotNull: ToInstance ToSubClass] string IPAddress; // IPv4 or IPv6 address
       [NotNull: ToInstance ToSubClass] string SubnetMask; // IPv4 subnet mask
   };

   class CCM_NetworkAdapter
   {
       [Key, NotNull: ToInstance ToSubClass] string Name;
       [NotNull: ToInstance ToSubClass] uint32 DHCPEnabled = 0; 
       [NotNull: ToInstance ToSubClass] uint32 Quarantined = 0; // To check if it is quarantined.
       CCM_IPConfig IPConfigInfo[];
   };

   [singleton]
   class CCM_NetworkAdapters
   {
       [NotNull: ToInstance ToSubClass] String ProviderName; // MED-V or other provider
       CCM_NetworkAdapter AdaptersInfo[];
   };
   ```

2. <span data-ttu-id="0171b-114">Kompilieren Sie die MOF-Datei.</span><span class="sxs-lookup"><span data-stu-id="0171b-114">Compile the MOF file.</span></span>

3. <span data-ttu-id="0171b-115">Installieren Sie die MOF-Datei im Gast.</span><span class="sxs-lookup"><span data-stu-id="0171b-115">Install the MOF file in the guest.</span></span>

<span data-ttu-id="0171b-116">Nachdem Sie die MOF-Datei installiert haben, können Sie ein Ereignisabonnement erstellen, das Windows Management Instrumentation (WMI)-Erstellungs-, Änderungs-oder Löschereignisse für die **ccm \ _NetworkAdapters** Klasse abonniert.</span><span class="sxs-lookup"><span data-stu-id="0171b-116">After you have installed the MOF file, you can create an event subscription that subscribes to Windows Management Instrumentation (WMI) creation, modification, or deletion events for the **CCM\_NetworkAdapters** class.</span></span> <span data-ttu-id="0171b-117">Damit werden die folgenden Änderungen am Host erkannt:</span><span class="sxs-lookup"><span data-stu-id="0171b-117">This detects the following changes to the host:</span></span>

<span data-ttu-id="0171b-118">Gibt es Konfigurationsänderungen am Netzwerk, beispielsweise Änderungen an der IP-Adresse oder am Netzwerkadapter?</span><span class="sxs-lookup"><span data-stu-id="0171b-118">Are there any configuration changes to the network, such as changes to the IP address or network adapter?</span></span>

<span data-ttu-id="0171b-119">Ist das Netzwerk verfügbar oder nicht verfügbar?</span><span class="sxs-lookup"><span data-stu-id="0171b-119">Is the network available or unavailable?</span></span>

<span data-ttu-id="0171b-120">Wurde das Netzwerk Setup vom Brückenmodus in den NAT-Modus geändert?</span><span class="sxs-lookup"><span data-stu-id="0171b-120">Was the network setup changed from BRIDGED mode to NAT mode?</span></span>

<span data-ttu-id="0171b-121">Wurde das Netzwerk Setup vom NAT-Modus in den Überbrückungsmodus geändert?</span><span class="sxs-lookup"><span data-stu-id="0171b-121">Was the network setup changed from NAT mode to BRIDGED mode?</span></span>

<span data-ttu-id="0171b-122">Eine MED-V-Komponente auf dem Host überwacht das Netzwerk für diese Änderungen und signalisiert dem Gast dann die Änderung.</span><span class="sxs-lookup"><span data-stu-id="0171b-122">A MED-V component on the host monitors the network for these changes and then signals the guest of the change.</span></span> <span data-ttu-id="0171b-123">Eine Komponente im Gast erstellt eine WMI-Instanz, um den MED-V-Arbeitsbereich für diese Änderungen zu überwachen.</span><span class="sxs-lookup"><span data-stu-id="0171b-123">A component in the guest creates a WMI instance to monitor the MED-V workspace for these changes.</span></span>

<span data-ttu-id="0171b-124">Das von Ihnen erstellte Ereignisabonnement bietet eine Benachrichtigung über das WMI-System, wenn mindestens eine dieser Netzwerkänderungen – erstellen, ändern oder löschen – eintritt.</span><span class="sxs-lookup"><span data-stu-id="0171b-124">The event subscription you created provides notification through the WMI system when one or more of these network changes – creation, modification, or deletion – occurs.</span></span>

## <span data-ttu-id="0171b-125">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="0171b-125">Related topics</span></span>


[<span data-ttu-id="0171b-126">Überwachen von MED-V-Arbeitsbereichen</span><span class="sxs-lookup"><span data-stu-id="0171b-126">Monitor MED-V Workspaces</span></span>](monitor-med-v-workspaces.md)

[<span data-ttu-id="0171b-127">Verwalten von MED-V-Arbeitsbereichseinstellungen</span><span class="sxs-lookup"><span data-stu-id="0171b-127">Manage MED-V Workspace Settings</span></span>](manage-med-v-workspace-settings.md)

 

 





