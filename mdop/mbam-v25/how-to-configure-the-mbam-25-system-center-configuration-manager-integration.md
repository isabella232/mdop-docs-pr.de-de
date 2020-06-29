---
title: So konfigurieren Sie die Integration von MBAM 2.5 in System Center Configuration Manager
description: So konfigurieren Sie die Integration von MBAM 2.5 in System Center Configuration Manager
author: dansimp
ms.assetid: 2b8a4c13-1dad-41e8-89ac-6889c5f7e051
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7c6fb0a0b06399baf1dc6493a40d17e76a51741f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804232"
---
# <span data-ttu-id="6ce7a-103">So konfigurieren Sie die Integration von MBAM 2.5 in System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="6ce7a-103">How to Configure the MBAM 2.5 System Center Configuration Manager Integration</span></span>


<span data-ttu-id="6ce7a-104">In diesem Thema wird erläutert, wie Sie die Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) für die Verwendung der System Center Configuration Manager-Integrations Topologie konfigurieren, die MBAM mit Configuration Manager integriert.</span><span class="sxs-lookup"><span data-stu-id="6ce7a-104">This topic explains how to configure Microsoft BitLocker Administration and Monitoring (MBAM) to use the System Center Configuration Manager Integration topology, which integrates MBAM with Configuration Manager.</span></span>

<span data-ttu-id="6ce7a-105">In den Anweisungen wird erläutert, wie Sie die Configuration Manager-Integration mit folgenden Schritten konfigurieren:</span><span class="sxs-lookup"><span data-stu-id="6ce7a-105">The instructions explain how to configure Configuration Manager Integration by using:</span></span>

-   <span data-ttu-id="6ce7a-106">Ein Windows PowerShell-Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6ce7a-106">A Windows PowerShell cmdlet</span></span>

-   <span data-ttu-id="6ce7a-107">Der Serverkonfigurations-Assistent von MBAM</span><span class="sxs-lookup"><span data-stu-id="6ce7a-107">The MBAM Server Configuration wizard</span></span>

<span data-ttu-id="6ce7a-108">Die Anweisungen basieren auf der empfohlenen Architektur in der [Architektur auf hoher Ebene für MBAM 2,5](high-level-architecture-for-mbam-25.md).</span><span class="sxs-lookup"><span data-stu-id="6ce7a-108">The instructions are based on the recommended architecture in [High-Level Architecture for MBAM 2.5](high-level-architecture-for-mbam-25.md).</span></span>

**<span data-ttu-id="6ce7a-109">Bevor Sie die Konfiguration starten:</span><span class="sxs-lookup"><span data-stu-id="6ce7a-109">Before you start the configuration:</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="6ce7a-110">Schritt</span><span class="sxs-lookup"><span data-stu-id="6ce7a-110">Step</span></span></th>
<th align="left"><span data-ttu-id="6ce7a-111">Wo erhalte ich Anweisungen?</span><span class="sxs-lookup"><span data-stu-id="6ce7a-111">Where to get instructions</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6ce7a-112">Überprüfen Sie die empfohlene Architektur für MBAM.</span><span class="sxs-lookup"><span data-stu-id="6ce7a-112">Review the recommended architecture for MBAM.</span></span></p></td>
<td align="left"><p><a href="high-level-architecture-of-mbam-25-with-configuration-manager-integration-topology.md" data-raw-source="[High-Level Architecture of MBAM 2.5 with Configuration Manager Integration Topology](high-level-architecture-of-mbam-25-with-configuration-manager-integration-topology.md)"><span data-ttu-id="6ce7a-113">High-Level-Architektur von MBAM 2.5 mit Configuration Manager-Integrationstopologie</span><span class="sxs-lookup"><span data-stu-id="6ce7a-113">High-Level Architecture of MBAM 2.5 with Configuration Manager Integration Topology</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6ce7a-114">Überprüfen Sie die unterstützten Konfigurationen für MBAM.</span><span class="sxs-lookup"><span data-stu-id="6ce7a-114">Review the supported configurations for MBAM.</span></span></p></td>
<td align="left"><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)"><span data-ttu-id="6ce7a-115">Von MBAM 2.5 unterstützte Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="6ce7a-115">MBAM 2.5 Supported Configurations</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6ce7a-116">Führen Sie die erforderlichen Voraussetzungen für jeden Server aus.</span><span class="sxs-lookup"><span data-stu-id="6ce7a-116">Complete the required prerequisites on each server.</span></span></p></td>
<td align="left"><ul>
<li><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)"><span data-ttu-id="6ce7a-117">MBAM 2.5-Servervoraussetzungen für eigenständige und Configuration Manager-Integrationstopologien</span><span class="sxs-lookup"><span data-stu-id="6ce7a-117">MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies</span></span></a></p></li>
<li><p><a href="mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md" data-raw-source="[MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md)"><span data-ttu-id="6ce7a-118">MBAM 2.5-Servervoraussetzungen, die nur für die Configuration Manager-Integrationstopologie gelten</span><span class="sxs-lookup"><span data-stu-id="6ce7a-118">MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology</span></span></a></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6ce7a-119">Installieren Sie die MBAM-Server Software auf jedem Server, auf dem Sie ein MBAM-Server Feature konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="6ce7a-119">Install the MBAM Server software on each server where you will configure an MBAM Server feature.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="6ce7a-120">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="6ce7a-120">Note</span></span></strong><br/><p><span data-ttu-id="6ce7a-121">Bei dieser Topologie müssen Sie die Configuration Manager-Konsole auf dem Computer installieren, auf dem Sie die MBAM-Server Software installieren.</span><span class="sxs-lookup"><span data-stu-id="6ce7a-121">For this topology, you must install the Configuration Manager console on the computer where you are installing the MBAM Server software.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><a href="installing-the-mbam-25-server-software.md" data-raw-source="[Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md)"><span data-ttu-id="6ce7a-122">Installieren der MBAM 2.5-Serversoftware</span><span class="sxs-lookup"><span data-stu-id="6ce7a-122">Installing the MBAM 2.5 Server Software</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6ce7a-123">Überprüfen Sie die Voraussetzungen für Windows PowerShell (nur anwendbar, wenn Sie Windows PowerShell-Cmdlets zum Konfigurieren von MBAM verwenden möchten).</span><span class="sxs-lookup"><span data-stu-id="6ce7a-123">Review Windows PowerShell prerequisites (applicable only if you are going to use Windows PowerShell cmdlets to configure MBAM).</span></span></p></td>
<td align="left"><p><a href="configuring-mbam-25-server-features-by-using-windows-powershell.md" data-raw-source="[Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)"><span data-ttu-id="6ce7a-124">Konfigurieren von MBAM 2.5 Serverfunktionen mithilfe von Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="6ce7a-124">Configuring MBAM 2.5 Server Features by Using Windows PowerShell</span></span></a></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="6ce7a-125">So konfigurieren Sie die Integration von Configuration Manager mithilfe von Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="6ce7a-125">To configure Configuration Manager Integration by using Windows PowerShell</span></span>**

1.  <span data-ttu-id="6ce7a-126">Bevor Sie die Konfiguration starten, lesen Sie [Konfigurieren von MBAM 2,5-Server Features mithilfe von Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md) zum Überprüfen der Voraussetzungen für die Verwendung von Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="6ce7a-126">Before you start the configuration, see [Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md) to review the prerequisites for using Windows PowerShell.</span></span>

2.  <span data-ttu-id="6ce7a-127">Verwenden Sie das Windows PowerShell **-Cmdlet Enable-MbamCMIntegration** , um die Berichte zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="6ce7a-127">Use the **Enable-MbamCMIntegration** Windows PowerShell cmdlet to configure the Reports.</span></span> <span data-ttu-id="6ce7a-128">Um Informationen zu diesem Cmdlet abzurufen, geben **Sie Get-Help enable-MbamCMIntegration**ein.</span><span class="sxs-lookup"><span data-stu-id="6ce7a-128">To get information about this cmdlet, type **Get-Help Enable-MbamCMIntegration**.</span></span>

**<span data-ttu-id="6ce7a-129">So konfigurieren Sie die Integration von System Center Configuration Manager mithilfe des Assistenten</span><span class="sxs-lookup"><span data-stu-id="6ce7a-129">To configure the System Center Configuration Manager Integration by using the wizard</span></span>**

1.  <span data-ttu-id="6ce7a-130">Starten Sie auf dem Server, auf dem Sie das System Center Configuration Manager-Integrations Feature konfigurieren möchten, den MBAM-Serverkonfigurations-Assistenten.</span><span class="sxs-lookup"><span data-stu-id="6ce7a-130">On the server where you want to configure the System Center Configuration Manager Integration feature, start the MBAM Server Configuration wizard.</span></span> <span data-ttu-id="6ce7a-131">Sie können **MBAM Server Configuration** im **Startmenü** auswählen, um den Assistenten zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="6ce7a-131">You can select **MBAM Server Configuration** from the **Start** menu to open the wizard.</span></span>

2.  <span data-ttu-id="6ce7a-132">Klicken Sie auf **neue Features hinzufügen**, wählen Sie **System Center Configuration Manager-Integration**aus, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="6ce7a-132">Click **Add New Features**, select **System Center Configuration Manager Integration**, and then click **Next**.</span></span>

    <span data-ttu-id="6ce7a-133">Der Assistent überprüft, ob alle Voraussetzungen für die Integration von Configuration Manager erfüllt sind.</span><span class="sxs-lookup"><span data-stu-id="6ce7a-133">The wizard checks that all prerequisites for the Configuration Manager Integration have been met.</span></span>

3.  <span data-ttu-id="6ce7a-134">Wenn die Voraussetzungsprüfung erfolgreich ist, klicken Sie auf **weiter** , um fortzufahren.</span><span class="sxs-lookup"><span data-stu-id="6ce7a-134">If the prerequisite check is successful, click **Next** to continue.</span></span> <span data-ttu-id="6ce7a-135">Beheben Sie andernfalls alle fehlenden Voraussetzungen, und klicken Sie dann **erneut auf Voraussetzungen prüfen**.</span><span class="sxs-lookup"><span data-stu-id="6ce7a-135">Otherwise, resolve any missing prerequisites, and then click **Check prerequisites again**.</span></span>

4.  <span data-ttu-id="6ce7a-136">Verwenden Sie die folgenden Beschreibungen, um die Feldwerte im Assistenten einzugeben:</span><span class="sxs-lookup"><span data-stu-id="6ce7a-136">Use the following descriptions to enter the field values in the wizard:</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="6ce7a-137">Feld</span><span class="sxs-lookup"><span data-stu-id="6ce7a-137">Field</span></span></th>
    <th align="left"><span data-ttu-id="6ce7a-138">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6ce7a-138">Description</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><strong><span data-ttu-id="6ce7a-139">SQL Server Reporting Services-Server</span><span class="sxs-lookup"><span data-stu-id="6ce7a-139">SQL Server Reporting Services server</span></span></strong></p></td>
    <td align="left"><p><span data-ttu-id="6ce7a-140">Vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) des Servers mit der Rolle des Berichterstattungsdienst Punkts.</span><span class="sxs-lookup"><span data-stu-id="6ce7a-140">Fully qualified domain name (FQDN) of the server with the Reporting Service point role.</span></span> <span data-ttu-id="6ce7a-141">Dies ist der Server, auf dem die MBAM Configuration Manager-Berichte bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="6ce7a-141">This is the server to which the MBAM Configuration Manager Reports are deployed.</span></span></p>
    <p><span data-ttu-id="6ce7a-142">Wenn Sie keinen Server angeben, werden die Configuration Manager-Berichte auf dem lokalen Server bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="6ce7a-142">If you don’t specify a server, the Configuration Manager Reports will be deployed to the local server.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong><span data-ttu-id="6ce7a-143">SQL Server Reporting Services-Instanz</span><span class="sxs-lookup"><span data-stu-id="6ce7a-143">SQL Server Reporting Services instance</span></span></strong></p></td>
    <td align="left"><p><span data-ttu-id="6ce7a-144">Der Name der SQL Server Reporting Services (SSRS)-Instanz, in der die Configuration Manager-Berichte bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="6ce7a-144">Name of the SQL Server Reporting Services (SSRS) instance where the Configuration Manager Reports are deployed.</span></span></p>
    <p><span data-ttu-id="6ce7a-145">Wenn Sie keine Instanz angeben, werden die Configuration Manager-Berichte im standardmäßigen SSRS-Instanzennamen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="6ce7a-145">If you don’t specify an instance, the Configuration Manager Reports will be deployed to the default SSRS instance name.</span></span> <span data-ttu-id="6ce7a-146">Der eingegebene Wert wird ignoriert, wenn auf dem Server der System Center 2012-Konfigurations-Manager installiert ist.</span><span class="sxs-lookup"><span data-stu-id="6ce7a-146">The value you enter is ignored if the server has System Center 2012 Configuration Manager installed.</span></span></p></td>
    </tr>
    </tbody>
    </table>



5.  <span data-ttu-id="6ce7a-147">Überprüfen Sie auf der Seite **Zusammenfassung** die Features, die hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="6ce7a-147">On the **Summary** page, review the features that will be added.</span></span>

    **<span data-ttu-id="6ce7a-148">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="6ce7a-148">Note</span></span>**  
    <span data-ttu-id="6ce7a-149">Wenn Sie ein Windows PowerShell-Skript der soeben erstellten Einträge erstellen möchten, klicken Sie auf **PowerShell-Skript exportieren** , und speichern Sie das Skript.</span><span class="sxs-lookup"><span data-stu-id="6ce7a-149">To create a Windows PowerShell script of the entries you just made, click **Export PowerShell Script** and save the script.</span></span>



6.  <span data-ttu-id="6ce7a-150">Klicken Sie auf **Hinzufügen** , um dem Server das Configuration Manager-Integrations Feature hinzuzufügen, und klicken Sie dann auf **Schließen**.</span><span class="sxs-lookup"><span data-stu-id="6ce7a-150">Click **Add** to add the Configuration Manager Integration feature to the server, and then click **Close**.</span></span>



## <span data-ttu-id="6ce7a-151">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="6ce7a-151">Related topics</span></span>


[<span data-ttu-id="6ce7a-152">Konfigurieren der MBAM 2.5-Serverfunktionen</span><span class="sxs-lookup"><span data-stu-id="6ce7a-152">Configuring the MBAM 2.5 Server Features</span></span>](configuring-the-mbam-25-server-features.md)

[<span data-ttu-id="6ce7a-153">Überprüfen der Konfiguration von MBAM 2.5 Serverfunktionen</span><span class="sxs-lookup"><span data-stu-id="6ce7a-153">Validating the MBAM 2.5 Server Feature Configuration</span></span>](validating-the-mbam-25-server-feature-configuration.md)


## <span data-ttu-id="6ce7a-154">Sie haben einen Vorschlag für MBAM?</span><span class="sxs-lookup"><span data-stu-id="6ce7a-154">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="6ce7a-155">[Hier](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)können Sie Vorschläge hinzufügen oder abstimmen.</span><span class="sxs-lookup"><span data-stu-id="6ce7a-155">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="6ce7a-156">Bei MBAM-Problemen verwenden Sie das [MBAM TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="6ce7a-156">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>






