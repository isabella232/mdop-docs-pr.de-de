---
title: Bereitstellen von App-V 5.0-Sequencer und -Client
description: Bereitstellen von App-V 5.0-Sequencer und -Client
author: dansimp
ms.assetid: 84cc84bd-5bc0-41aa-9519-0ded2932c078
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: 647ea12018bf966592b9e831d532c7c08093d367
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805846"
---
# <span data-ttu-id="74902-103">Bereitstellen von App-V 5.0-Sequencer und -Client</span><span class="sxs-lookup"><span data-stu-id="74902-103">Deploying the App-V 5.0 Sequencer and Client</span></span>


<span data-ttu-id="74902-104">Mit dem App-V 5,0-Sequenzer und-Client können Administratoren virtualisierte Anwendungen virtualisieren und ausführen.</span><span class="sxs-lookup"><span data-stu-id="74902-104">The App-V 5.0 Sequencer and client enable administrators to virtualize and run virtualized applications.</span></span>

## <span data-ttu-id="74902-105">Bereitstellen des Clients</span><span class="sxs-lookup"><span data-stu-id="74902-105">Deploy the client</span></span>


<span data-ttu-id="74902-106">Der App-V 5,0-Client ist die Komponente, die eine virtualisierte Anwendung auf einem Zielcomputer ausführt.</span><span class="sxs-lookup"><span data-stu-id="74902-106">The App-V 5.0 client is the component that runs a virtualized application on a target computer.</span></span> <span data-ttu-id="74902-107">Der Client ermöglicht Benutzern die Interaktion mit Symbolen und das Doppelklicken auf Dateitypen, damit Sie eine virtualisierte Anwendung starten können.</span><span class="sxs-lookup"><span data-stu-id="74902-107">The client enables users to interact with icons and to double-click file types, so that they can start a virtualized application.</span></span> <span data-ttu-id="74902-108">Der Client kann auch den Inhalt der virtuellen Anwendung vom Verwaltungsserver abrufen.</span><span class="sxs-lookup"><span data-stu-id="74902-108">The client can also obtain the virtual application content from the management server.</span></span>

[<span data-ttu-id="74902-109">So stellen Sie App-V-Client bereit</span><span class="sxs-lookup"><span data-stu-id="74902-109">How to Deploy the App-V Client</span></span>](how-to-deploy-the-app-v-client-gb18030.md)

[<span data-ttu-id="74902-110">So deinstallieren Sie den App-V 5.0-Client</span><span class="sxs-lookup"><span data-stu-id="74902-110">How to Uninstall the App-V 5.0 Client</span></span>](how-to-uninstall-the-app-v-50-client.md)

[<span data-ttu-id="74902-111">Bereitstellen der APP-v 4,6 und des App-v 5,0-Clients auf demselben Computer</span><span class="sxs-lookup"><span data-stu-id="74902-111">How to Deploy the App-V 4.6 and the App-V 5.0 Client on the Same Computer</span></span>](how-to-deploy-the-app-v-46-and-the-app-v--50-client-on-the-same-computer.md)

## <span data-ttu-id="74902-112">Client Konfigurationseinstellungen</span><span class="sxs-lookup"><span data-stu-id="74902-112">Client Configuration Settings</span></span>


<span data-ttu-id="74902-113">Der App-V 5,0-Client speichert seine Konfiguration in der Registrierung.</span><span class="sxs-lookup"><span data-stu-id="74902-113">The App-V 5.0 client stores its configuration in the registry.</span></span> <span data-ttu-id="74902-114">Sie können einige nützliche Informationen zu dem Client sammeln, wenn Sie das Format der Daten in der Registrierung verstehen.</span><span class="sxs-lookup"><span data-stu-id="74902-114">You can gather some useful information about the client if you understand the format of data in the registry.</span></span> <span data-ttu-id="74902-115">Sie können auch viele Clientaktionen konfigurieren, indem Sie Registrierungseinträge ändern.</span><span class="sxs-lookup"><span data-stu-id="74902-115">You can also configure many client actions by changing registry entries.</span></span>

[<span data-ttu-id="74902-116">Informationen über Clientkonfigurationseinstellungen</span><span class="sxs-lookup"><span data-stu-id="74902-116">About Client Configuration Settings</span></span>](about-client-configuration-settings.md)

## <span data-ttu-id="74902-117">Konfigurieren des Clients mithilfe der ADMX-Vorlage und der Gruppenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="74902-117">Configure the client by using the ADMX template and Group Policy</span></span>


<span data-ttu-id="74902-118">Sie können die Vorlage Microsoft ADMX verwenden, um die Clienteinstellungen für den App-V 5,0-Client und den Remote Desktop Dienste-Client zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="74902-118">You can use the Microsoft ADMX template to configure the client settings for the App-V 5.0 client and the Remote Desktop Services client.</span></span> <span data-ttu-id="74902-119">Die ADMX-Vorlage verwaltet allgemeine Clientkonfigurationen mithilfe einer vorhandenen Gruppenrichtlinieninfrastruktur und umfasst Einstellungen für die App-V 5,0-Clientkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="74902-119">The ADMX template manages common client configurations by using an existing Group Policy infrastructure and it includes settings for the App-V 5.0 client configuration.</span></span>

<span data-ttu-id="74902-120">**Wichtig**  Sie können die App-V 5,0 ADMX-Vorlage aus dem Microsoft Download Center abrufen.</span><span class="sxs-lookup"><span data-stu-id="74902-120">**Important** You can obtain the App-V 5.0 ADMX template from the Microsoft Download Center.</span></span>

 

<span data-ttu-id="74902-121">Nachdem Sie die ADMX-Vorlage heruntergeladen und installiert haben, führen Sie die folgenden Schritte auf dem Computer aus, den Sie zum Verwalten von Gruppenrichtlinien verwenden werden.</span><span class="sxs-lookup"><span data-stu-id="74902-121">After you download and install the ADMX template, perform the following steps on the computer that you will use to manage Group Policy.</span></span> <span data-ttu-id="74902-122">Dies ist normalerweise der Domänen Controller.</span><span class="sxs-lookup"><span data-stu-id="74902-122">This is typically the Domain Controller.</span></span>

1.  <span data-ttu-id="74902-123">Speichern Sie die **ADMX-** Datei im folgenden Verzeichnis: **Windows \ \ PolicyDefinitions**</span><span class="sxs-lookup"><span data-stu-id="74902-123">Save the **.admx** file to the following directory: **Windows \\ PolicyDefinitions**</span></span>

2.  <span data-ttu-id="74902-124">Speichern Sie die **ADML-** Datei im folgenden Verzeichnis: \*\*Windows \ \ PolicyDefinitions \ \ &lt; Language Directory &gt; \*\*</span><span class="sxs-lookup"><span data-stu-id="74902-124">Save the **.adml** file to the following directory: **Windows \\ PolicyDefinitions \\ &lt;Language Directory&gt;**</span></span>

<span data-ttu-id="74902-125">Nachdem Sie die vorherigen Schritte ausgeführt haben, können Sie die Einstellungen für die App-V 5,0-Clientkonfiguration über die **Gruppenrichtlinien-Verwaltungs** Konsole verwalten.</span><span class="sxs-lookup"><span data-stu-id="74902-125">After you have completed the preceding steps, you can manage the App-V 5.0 client configuration settings with the **Group Policy Management** console.</span></span>

<span data-ttu-id="74902-126">Der App-V 5,0-Client speichert auch seine Konfiguration in der Registrierung.</span><span class="sxs-lookup"><span data-stu-id="74902-126">The App-V 5.0 client also stores its configuration in the registry.</span></span> <span data-ttu-id="74902-127">Sie können einige nützliche Informationen zu dem Client sammeln, wenn Sie das Format der Daten in der Registrierung verstehen.</span><span class="sxs-lookup"><span data-stu-id="74902-127">You can gather some useful information about the client if you understand the format of the data in the registry.</span></span> <span data-ttu-id="74902-128">Sie können auch viele Clientaktionen konfigurieren, indem Sie Registrierungseinträge ändern.</span><span class="sxs-lookup"><span data-stu-id="74902-128">You can also configure many client actions by changing registry entries.</span></span>

[<span data-ttu-id="74902-129">So ändern Sie die App-V 5.0-Clientkonfiguration mithilfe der ADMX-Vorlage und -Gruppenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="74902-129">How to Modify App-V 5.0 Client Configuration Using the ADMX Template and Group Policy</span></span>](how-to-modify-app-v-50-client-configuration-using-the-admx-template-and-group-policy.md)

## <span data-ttu-id="74902-130">Bereitstellen des Clients mithilfe des freigegebenen Inhaltsspeicher Modus</span><span class="sxs-lookup"><span data-stu-id="74902-130">Deploy the client by using the Shared Content Store mode</span></span>


<span data-ttu-id="74902-131">Der APP-v 5,0 Shared Content Store (SCS)-Modus ermöglicht es den SCS-App-v 5,0-Clients, virtualisierte Anwendungen auszuführen, ohne die zugehörigen Paketdaten lokal zu speichern.</span><span class="sxs-lookup"><span data-stu-id="74902-131">The App-V 5.0 Shared Content Store (SCS) mode enables the SCS App-V 5.0 clients to run virtualized applications without saving any of the associated package data locally.</span></span> <span data-ttu-id="74902-132">Alle erforderlichen virtualisierten Paketdaten werden über das Netzwerk übertragen. Daher sollten Sie den SCS-Modus nur in Umgebungen mit einer schnellen Verbindung verwenden.</span><span class="sxs-lookup"><span data-stu-id="74902-132">All required virtualized package data is transmitted across the network; therefore, you should only use the SCS mode in environments with a fast connection.</span></span> <span data-ttu-id="74902-133">Sowohl die Remote Desktop Dienste (RDS) als auch die Standard Version des App-V 5,0-Clients werden im SCS-Modus unterstützt.</span><span class="sxs-lookup"><span data-stu-id="74902-133">Both the Remote Desktop Services (RDS) and the standard version of the App-V 5.0 client are supported with SCS mode.</span></span>

<span data-ttu-id="74902-134">**Wichtig**  Wenn der APP-v 5,0-Client so konfiguriert ist, dass er im SCS-Modus ausgeführt wird, muss der Speicherort, von dem die APP-v 5,0-Pakete gestreamt werden, verfügbar sein, andernfalls schlägt das virtualisierte Paket fehl.</span><span class="sxs-lookup"><span data-stu-id="74902-134">**Important** If the App-V 5.0 client is configured to run in the SCS mode, the location where the App-V 5.0 packages are streamed from must be available, otherwise, the virtualized package will fail.</span></span> <span data-ttu-id="74902-135">Darüber hinaus empfehlen wir die Bereitstellung virtualisierter Anwendungen nicht auf Computern, auf denen der App-V 5,0-Client im SCS-Modus über das Internet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="74902-135">Additionally, we do not recommend deployment of virtualized applications to computers that run the App-V 5.0 client in the SCS mode across the internet.</span></span>

 

<span data-ttu-id="74902-136">Darüber hinaus ist das SCS kein physikalischer Speicherort, der virtualisierte Pakete enthält.</span><span class="sxs-lookup"><span data-stu-id="74902-136">Additionally, the SCS is not a physical location that contains virtualized packages.</span></span> <span data-ttu-id="74902-137">Dieser Modus ermöglicht es dem App-V 5,0-Client, die erforderlichen virtualisierten Paketdaten über das Netzwerk zu streamen.</span><span class="sxs-lookup"><span data-stu-id="74902-137">It is a mode that allows the App-V 5.0 client to stream the required virtualized package data across the network.</span></span>

<span data-ttu-id="74902-138">Der SCS-Modus ist in den folgenden Szenarien hilfreich:</span><span class="sxs-lookup"><span data-stu-id="74902-138">The SCS mode is helpful in the following scenarios:</span></span>

-   <span data-ttu-id="74902-139">VDI-Bereitstellungen (Virtual Desktop Infrastructure)</span><span class="sxs-lookup"><span data-stu-id="74902-139">Virtual desktop infrastructure (VDI) deployments</span></span>

-   <span data-ttu-id="74902-140">Remote Desktop Dienste (RDS)-Bereitstellungen</span><span class="sxs-lookup"><span data-stu-id="74902-140">Remote desktop services (RDS) deployments</span></span>

<span data-ttu-id="74902-141">Um SCS in Ihrer Umgebung verwenden zu können, müssen Sie den App-V 5,0-Client aktivieren, damit er im SCS-Modus ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="74902-141">To use SCS in your environment, you must enable the App-V 5.0 client to run in SCS mode.</span></span> <span data-ttu-id="74902-142">Diese Einstellung sollte während der Installation angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="74902-142">This setting should be specified during installation.</span></span> <span data-ttu-id="74902-143">Standardmäßig ist der Client nicht für die Verwendung des SCS-Modus konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="74902-143">By default, the client is not configured to use SCS mode.</span></span> <span data-ttu-id="74902-144">Wenn Sie beabsichtigen, SCS zu verwenden, sollten Sie den Client mithilfe des vorgeschlagenen Verfahrens installieren.</span><span class="sxs-lookup"><span data-stu-id="74902-144">You should install the client by using the suggested procedure if you plan to use SCS.</span></span> <span data-ttu-id="74902-145">Sie können jedoch einen vorhandenen APP-v 5,0-Client so konfigurieren, dass er im SCS-Modus ausgeführt wird, indem Sie den folgenden PowerShell-Befehl auf dem Computer eingeben, auf dem der APP-v 5,0-Client ausgeführt wird:</span><span class="sxs-lookup"><span data-stu-id="74902-145">However, you can configure an existing App-V 5.0 client to run in SCS mode by entering the following PowerShell command on the computer that runs the App-V 5.0 client:</span></span>

**<span data-ttu-id="74902-146">Satz-AppvClientConfiguration-SharedContentStoreMode 1</span><span class="sxs-lookup"><span data-stu-id="74902-146">set-AppvClientConfiguration -SharedContentStoreMode 1</span></span>**

<span data-ttu-id="74902-147">Es kann vorkommen, dass der Administrator einige virtuelle Anwendungen auf dem Computer vorlädt, auf dem der App-V 5,0-Client im SCS-Modus ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="74902-147">There might be cases when the administrator pre-loads some virtual applications on the computer that runs the App-V 5.0 client in SCS mode.</span></span> <span data-ttu-id="74902-148">Dies kann mit PowerShell-Befehlen durchgeführt werden, um das Paket hinzuzufügen, zu veröffentlichen und bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="74902-148">This can be accomplished with PowerShell commands to add, publish, and mount the package.</span></span> <span data-ttu-id="74902-149">Wenn ein Paket beispielsweise auf allen Computern bereits vorinstalliert ist, kann der Administrator das Paket mithilfe von PowerShell-Befehlen hinzufügen, veröffentlichen und bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="74902-149">For example, if a package is pre-loaded on all computers, the administrator could add, publish, and mount the package by using PowerShell commands.</span></span> <span data-ttu-id="74902-150">Das Paket konnte nicht über das Netzwerk gestreamt werden, da es lokal gespeichert werden würde.</span><span class="sxs-lookup"><span data-stu-id="74902-150">The package would not stream across the network because it would be locally stored.</span></span>

[<span data-ttu-id="74902-151">So installieren Sie den App-V 5.0-Client für den SCS-Modus (Shared Content Store)</span><span class="sxs-lookup"><span data-stu-id="74902-151">How to Install the App-V 5.0 Client for Shared Content Store Mode</span></span>](how-to-install-the-app-v-50-client-for-shared-content-store-mode.md)

## <span data-ttu-id="74902-152">Bereitstellen des Sequencers</span><span class="sxs-lookup"><span data-stu-id="74902-152">Deploy the Sequencer</span></span>


<span data-ttu-id="74902-153">Der Sequencer ist ein Tool, mit dem Standardanwendungen in virtuelle Pakete für die Bereitstellung auf Computern konvertiert werden, auf denen der App-V 5,0-Client ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="74902-153">The Sequencer is a tool that is used to convert standard applications into virtual packages for deployment to computers that run the App-V 5.0 client.</span></span> <span data-ttu-id="74902-154">Der Sequencer hilft bei der Bereitstellungeines einfachen und vorhersehbaren Konvertierungsprozesses mit minimalen Änderungen an vorherigen Sequenzierungs Workflows.</span><span class="sxs-lookup"><span data-stu-id="74902-154">The Sequencer helps provide a simple and predictable conversion process with minimal changes to prior sequencing workflows.</span></span> <span data-ttu-id="74902-155">Darüber hinaus ermöglicht der Sequencer Benutzern die einfachere Konfiguration von Anwendungen, um Verbindungen virtualisierter Anwendungen zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="74902-155">In addition, the Sequencer allows users to more easily configure applications to enable connections of virtualized applications.</span></span>

<span data-ttu-id="74902-156">Eine Liste der Änderungen im App-v 5,0-Sequenzer finden Sie unter [Neuerungen in App-v 5,0](whats-new-in-app-v-50.md).</span><span class="sxs-lookup"><span data-stu-id="74902-156">For a list of changes in the App-V 5.0 Sequencer, see [What's New in App-V 5.0](whats-new-in-app-v-50.md).</span></span>

[<span data-ttu-id="74902-157">So installieren Sie den Sequencer</span><span class="sxs-lookup"><span data-stu-id="74902-157">How to Install the Sequencer</span></span>](how-to-install-the-sequencer-beta-gb18030.md)

## <a href="" id="---------app-v-5-0-client-and-sequencer-logs"></a> <span data-ttu-id="74902-158">App-V 5,0-Client-und-Sequenzer-Protokolle</span><span class="sxs-lookup"><span data-stu-id="74902-158">App-V 5.0 Client and Sequencer logs</span></span>


<span data-ttu-id="74902-159">Sie können die Protokollinformationen für App-v 5,0-Sequencer verwenden, um bei der Behandlung von Sequencer-Installations-und-Betriebsereignissen bei Verwendung von App-v 5,0 zu helfen.</span><span class="sxs-lookup"><span data-stu-id="74902-159">You can use the App-V 5.0 Sequencer log information to help troubleshoot the Sequencer installation and operational events while using App-V 5.0.</span></span> <span data-ttu-id="74902-160">Die Sequencer-bezogenen Protokollinformationen können mit der **Ereignisanzeige**überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="74902-160">The Sequencer-related log information can be reviewed with the **Event Viewer**.</span></span> <span data-ttu-id="74902-161">In der folgenden Zeile wird der spezifische Pfad für Sequenzer bezogene Ereignisse angezeigt:</span><span class="sxs-lookup"><span data-stu-id="74902-161">The following line displays the specific path for Sequencer-related events:</span></span>

<span data-ttu-id="74902-162">**Ereignisanzeige \ \ Anwendungen und Dienstprotokolle \ \ Microsoft \ \ App V**. Sequencer-bezogene Ereignisse werden **AppV \ _Sequencer**vorangestellt.</span><span class="sxs-lookup"><span data-stu-id="74902-162">**Event Viewer \\ Applications and Services Logs \\ Microsoft \\ App V**. Sequencer-related events are prepended with **AppV\_Sequencer**.</span></span> <span data-ttu-id="74902-163">Client bezogene Ereignisse werden **AppV \ _Client**vorangestellt.</span><span class="sxs-lookup"><span data-stu-id="74902-163">Client-related events are prepended with **AppV\_Client**.</span></span>

<span data-ttu-id="74902-164">In App-V 5,0 SP3 wurden einige Protokolle konsolidiert.</span><span class="sxs-lookup"><span data-stu-id="74902-164">In App-V 5.0 SP3, some logs have been consolidated.</span></span> <span data-ttu-id="74902-165">Informationen finden Sie unter [App-V 5,0 SP3](about-app-v-50-sp3.md#bkmk-event-logs-moved).</span><span class="sxs-lookup"><span data-stu-id="74902-165">See [About App-V 5.0 SP3](about-app-v-50-sp3.md#bkmk-event-logs-moved).</span></span>

## <span data-ttu-id="74902-166">Weitere Ressourcen für die Bereitstellung von Sequencer und Client</span><span class="sxs-lookup"><span data-stu-id="74902-166">Other resources for deploying the Sequencer and client</span></span>


[<span data-ttu-id="74902-167">Bereitstellen von App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="74902-167">Deploying App-V 5.0</span></span>](deploying-app-v-50.md)

[<span data-ttu-id="74902-168">Planen für App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="74902-168">Planning for App-V 5.0</span></span>](planning-for-app-v-50-rc.md)






 

 





