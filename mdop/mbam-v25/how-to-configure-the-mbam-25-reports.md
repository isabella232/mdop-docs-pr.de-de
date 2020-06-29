---
title: So konfigurieren Sie die MBAM 2.5-Berichte
description: So konfigurieren Sie die MBAM 2.5-Berichte
author: dansimp
ms.assetid: ec462879-0253-4d9c-83c7-a9bcad479725
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6b372bd6bc38a3729aef43354ecf19b2619b7856
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811863"
---
# <span data-ttu-id="404cc-103">So konfigurieren Sie die MBAM 2.5-Berichte</span><span class="sxs-lookup"><span data-stu-id="404cc-103">How to Configure the MBAM 2.5 Reports</span></span>


<span data-ttu-id="404cc-104">In diesem Thema wird erläutert, wie Sie das 2,5-Feature für die Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) mithilfe von folgendem konfigurieren:</span><span class="sxs-lookup"><span data-stu-id="404cc-104">This topic explains how to configure the Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 Reports feature by using:</span></span>

-   <span data-ttu-id="404cc-105">Ein Windows PowerShell-Cmdlet</span><span class="sxs-lookup"><span data-stu-id="404cc-105">A Windows PowerShell cmdlet</span></span>

-   <span data-ttu-id="404cc-106">Der Serverkonfigurations-Assistent von MBAM</span><span class="sxs-lookup"><span data-stu-id="404cc-106">The MBAM Server Configuration wizard</span></span>

<span data-ttu-id="404cc-107">Die Anweisungen basieren auf der empfohlenen Architektur in der [Architektur auf hoher Ebene für MBAM 2,5](high-level-architecture-for-mbam-25.md).</span><span class="sxs-lookup"><span data-stu-id="404cc-107">The instructions are based on the recommended architecture in [High-Level Architecture for MBAM 2.5](high-level-architecture-for-mbam-25.md).</span></span>

**<span data-ttu-id="404cc-108">Bevor Sie die Konfiguration starten:</span><span class="sxs-lookup"><span data-stu-id="404cc-108">Before you start the configuration:</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="404cc-109">Schritt</span><span class="sxs-lookup"><span data-stu-id="404cc-109">Step</span></span></th>
<th align="left"><span data-ttu-id="404cc-110">Wo erhalte ich Anweisungen?</span><span class="sxs-lookup"><span data-stu-id="404cc-110">Where to get instructions</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="404cc-111">Überprüfen Sie die empfohlene Architektur für MBAM.</span><span class="sxs-lookup"><span data-stu-id="404cc-111">Review the recommended architecture for MBAM.</span></span></p></td>
<td align="left"><p><a href="high-level-architecture-for-mbam-25.md" data-raw-source="[High-Level Architecture for MBAM 2.5](high-level-architecture-for-mbam-25.md)"><span data-ttu-id="404cc-112">High-Level-Architektur für MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="404cc-112">High-Level Architecture for MBAM 2.5</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="404cc-113">Überprüfen Sie die unterstützten Konfigurationen für MBAM.</span><span class="sxs-lookup"><span data-stu-id="404cc-113">Review the supported configurations for MBAM.</span></span></p></td>
<td align="left"><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)"><span data-ttu-id="404cc-114">Von MBAM 2.5 unterstützte Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="404cc-114">MBAM 2.5 Supported Configurations</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="404cc-115">Führen Sie die erforderlichen Voraussetzungen für jeden Server aus.</span><span class="sxs-lookup"><span data-stu-id="404cc-115">Complete the required prerequisites on each server.</span></span></p></td>
<td align="left"><ul>
<li><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)"><span data-ttu-id="404cc-116">MBAM 2.5-Servervoraussetzungen für eigenständige und Configuration Manager-Integrationstopologien</span><span class="sxs-lookup"><span data-stu-id="404cc-116">MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies</span></span></a></p></li>
<li><p><a href="mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md" data-raw-source="[MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md)"><span data-ttu-id="404cc-117">MBAM 2,5-Server Voraussetzungen, die nur für die Configuration Manager-Integrations Topologie gelten </a> (falls zutreffend)</span><span class="sxs-lookup"><span data-stu-id="404cc-117">MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology</a> (if applicable)</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="404cc-118">Installieren Sie die MBAM-Server Software auf jedem Server, auf dem Sie ein MBAM-Server Feature konfigurieren möchten.</span><span class="sxs-lookup"><span data-stu-id="404cc-118">Install the MBAM Server software on each server where you plan to configure an MBAM Server feature.</span></span></p></td>
<td align="left"><p><a href="installing-the-mbam-25-server-software.md" data-raw-source="[Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md)"><span data-ttu-id="404cc-119">Installieren der MBAM 2.5-Serversoftware</span><span class="sxs-lookup"><span data-stu-id="404cc-119">Installing the MBAM 2.5 Server Software</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="404cc-120">Überprüfen Sie die Voraussetzungen für die Verwendung von Windows PowerShell, wenn Sie Windows PowerShell-Cmdlets zum Konfigurieren der MBAM-Server Features verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="404cc-120">Review the prerequisites for using Windows PowerShell if you plan to use Windows PowerShell cmdlets to configure MBAM Server features.</span></span></p></td>
<td align="left"><p><a href="configuring-mbam-25-server-features-by-using-windows-powershell.md" data-raw-source="[Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)"><span data-ttu-id="404cc-121">Konfigurieren von MBAM 2.5 Serverfunktionen mithilfe von Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="404cc-121">Configuring MBAM 2.5 Server Features by Using Windows PowerShell</span></span></a></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="404cc-122">So konfigurieren Sie die Berichte mithilfe von Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="404cc-122">To configure the Reports by using Windows PowerShell</span></span>**

1.  <span data-ttu-id="404cc-123">Bevor Sie die Konfiguration starten, lesen Sie [Konfigurieren von MBAM 2,5-Server Features mithilfe von Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md) zum Überprüfen der Voraussetzungen für die Verwendung von Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="404cc-123">Before you start the configuration, see [Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md) to review the prerequisites for using Windows PowerShell.</span></span>

2.  <span data-ttu-id="404cc-124">Verwenden Sie das Windows PowerShell **-Cmdlet Enable-MbamReport** , um die Berichte zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="404cc-124">Use the **Enable-MbamReport** Windows PowerShell cmdlet to configure the Reports.</span></span> <span data-ttu-id="404cc-125">Um Informationen zu diesem Windows PowerShell-Cmdlet abzurufen, geben **Sie Get-Help enable-MbamReport**ein.</span><span class="sxs-lookup"><span data-stu-id="404cc-125">To get information about this Windows PowerShell cmdlet, type **Get-Help Enable-MbamReport**.</span></span>

**<span data-ttu-id="404cc-126">So konfigurieren Sie die Berichte mit dem Assistenten</span><span class="sxs-lookup"><span data-stu-id="404cc-126">To configure the Reports by using the wizard</span></span>**

1. <span data-ttu-id="404cc-127">Starten Sie auf dem Server, auf dem Sie die Berichte konfigurieren möchten, den **MBAM-Serverkonfigurations** -Assistenten.</span><span class="sxs-lookup"><span data-stu-id="404cc-127">On the server where you want to configure the Reports, start the **MBAM Server Configuration** wizard.</span></span> <span data-ttu-id="404cc-128">Sie können **MBAM Server Configuration** im **Startmenü** auswählen, um den Assistenten zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="404cc-128">You can select **MBAM Server Configuration** from the **Start** menu to open the wizard.</span></span>

2. <span data-ttu-id="404cc-129">Klicken Sie auf **neue Features hinzufügen**, wählen Sie **Berichte**aus, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="404cc-129">Click **Add New Features**, select **Reports**, and then click **Next**.</span></span> <span data-ttu-id="404cc-130">Der Assistent überprüft, ob alle Voraussetzungen für die Berichte erfüllt wurden.</span><span class="sxs-lookup"><span data-stu-id="404cc-130">The wizard checks that all prerequisites for the Reports have been met.</span></span>

3. <span data-ttu-id="404cc-131">Klicken Sie auf **Weiter**, um den Vorgang fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="404cc-131">Click **Next** to continue.</span></span>

4. <span data-ttu-id="404cc-132">Geben Sie anhand der folgenden Beschreibungen die Feldwerte im Assistenten ein:</span><span class="sxs-lookup"><span data-stu-id="404cc-132">Using the following descriptions, enter the field values in the wizard:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="404cc-133">Feld</span><span class="sxs-lookup"><span data-stu-id="404cc-133">Field</span></span></th>
   <th align="left"><span data-ttu-id="404cc-134">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="404cc-134">Description</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="404cc-135">SQL Server Reporting Services-Instanz</span><span class="sxs-lookup"><span data-stu-id="404cc-135">SQL Server Reporting Services instance</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="404cc-136">Instanz von SQL Server Reporting Services, in der die Berichte konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="404cc-136">Instance of SQL Server Reporting Services where the Reports will be configured.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="404cc-137">Gruppe "Berichtsrolle-Domäne"</span><span class="sxs-lookup"><span data-stu-id="404cc-137">Reporting role domain group</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="404cc-138">Name der Gruppe "Domänenbenutzer", deren Mitglieder über Rechte für den Zugriff auf die Berichte auf dem Verwaltungs-und Überwachungs Server verfügen</span><span class="sxs-lookup"><span data-stu-id="404cc-138">Name of the domain Users group whose members have rights to access the reports on the Administration and Monitoring Server.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="404cc-139">SQL Server-Name</span><span class="sxs-lookup"><span data-stu-id="404cc-139">SQL Server name</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="404cc-140">Der Name des Servers, auf dem die Konformitäts-und Überwachungsdatenbank konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="404cc-140">Name of the server where the Compliance and Audit Database is configured.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="404cc-141">SQL Server-Datenbankinstanz</span><span class="sxs-lookup"><span data-stu-id="404cc-141">SQL Server database instance</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="404cc-142">Der Name der Instanz von SQL Server (beispielsweise <em> MSSQLSERVER </em> ), in der die Compliance-und Überwachungsdatenbank konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="404cc-142">Name of the instance of SQL Server (for example, <em>MSSQLSERVER</em>) where the Compliance and Audit Database is configured.</span></span></p>
   <div class="alert">
   <strong><span data-ttu-id="404cc-143">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="404cc-143">Note</span></span></strong><br/><p><span data-ttu-id="404cc-144">Sie müssen auf dem Computer "Berichte" eine Ausnahme hinzufügen, um eingehenden Datenverkehr am Port des Berichtsservers zu aktivieren (der Standardport ist 80).</span><span class="sxs-lookup"><span data-stu-id="404cc-144">You must add an exception on the Reports computer to enable inbound traffic on the port of the Reporting Server (the default port is 80).</span></span></p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="404cc-145">Datenbankname</span><span class="sxs-lookup"><span data-stu-id="404cc-145">Database name</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="404cc-146">Der Name der Konformitäts-und Überwachungsdatenbank.</span><span class="sxs-lookup"><span data-stu-id="404cc-146">Name of the Compliance and Audit Database.</span></span> <span data-ttu-id="404cc-147">Standardmäßig ist der Datenbankname <strong> MBAM-Konformitäts Status </strong> , obwohl Sie den Namen ändern können, wenn Sie die Kompatibilitäts-und Überwachungsdatenbank konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="404cc-147">By default, the database name is <strong>MBAM Compliance Status</strong>, although you can change the name when you configure the Compliance and Audit Database.</span></span></p>
   <div class="alert">
   <strong><span data-ttu-id="404cc-148">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="404cc-148">Note</span></span></strong><br/><p><span data-ttu-id="404cc-149">Wenn Sie ein Upgrade von einer früheren Version von MBAM durchführen, müssen Sie denselben Datenbanknamen wie den in der vorherigen Bereitstellung verwendeten Namen verwenden.</span><span class="sxs-lookup"><span data-stu-id="404cc-149">If you are upgrading from a previous version of MBAM, you must use the same database name as the name used in your previous deployment.</span></span></p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="404cc-150">Compliance-und Audit-Daten Bank Domänenkonto</span><span class="sxs-lookup"><span data-stu-id="404cc-150">Compliance and Audit Database domain account</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="404cc-151">Domänenbenutzerkonto und Kennwort für den Zugriff auf die Datenbank "Konformitäts-und Überwachungsdatenbank".</span><span class="sxs-lookup"><span data-stu-id="404cc-151">Domain user account and password to access the Compliance and Audit Database.</span></span></p>
   <p><span data-ttu-id="404cc-152">Wenn der Wert, den Sie in das <strong> Feld "Schreibgeschützter Zugriffsdomänen Benutzer" oder "Gruppe" </strong> auf der <strong> Seite "Datenbanken konfigurieren </strong> " eingeben, ein Benutzer ist, müssen Sie diesen Wert in dieses Feld eingeben.</span><span class="sxs-lookup"><span data-stu-id="404cc-152">If the value you enter in the <strong>Read-only access domain user or group</strong> field on the <strong>Configure Databases</strong> page is a user, you must enter that same value in this field.</span></span></p>
   <p><span data-ttu-id="404cc-153">Wenn der Wert, den Sie in das <strong> Feld "Schreibgeschützter Zugriffsdomänen Benutzer" oder "Gruppe" </strong> auf der <strong> Seite "Datenbanken konfigurieren" eingeben </strong> , eine Gruppe ist, muss der Wert, den Sie in dieses Feld eingeben, Mitglied dieser Gruppe sein.</span><span class="sxs-lookup"><span data-stu-id="404cc-153">If the value that you enter in the <strong>Read-only access domain user or group</strong> field on the <strong>Configure Databases</strong> page is a group, the value that you enter in this field must be a member of that group.</span></span></p>
   <p><span data-ttu-id="404cc-154">Konfigurieren Sie das Kennwort für dieses Konto so, dass es nie abläuft.</span><span class="sxs-lookup"><span data-stu-id="404cc-154">Configure the password for this account to never expire.</span></span> <span data-ttu-id="404cc-155">Das Benutzerkonto sollte auf alle Daten zugreifen können, die für die Gruppe MBAM-Berichte Benutzer verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="404cc-155">The user account should be able to access all data that is available to the MBAM Reports Users group.</span></span></p></td>
   </tr>
   </tbody>
   </table>



5. <span data-ttu-id="404cc-156">Wenn Sie Ihre Eingaben abgeschlossen haben, klicken Sie auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="404cc-156">When you finish your entries, click **Next**.</span></span>

   <span data-ttu-id="404cc-157">Der Assistent überprüft, ob alle Voraussetzungen für das Berichtsfeature erfüllt wurden.</span><span class="sxs-lookup"><span data-stu-id="404cc-157">The wizard checks that all prerequisites for the Reports feature have been met.</span></span>

6. <span data-ttu-id="404cc-158">Klicken Sie auf **Weiter**, um den Vorgang fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="404cc-158">Click **Next** to continue.</span></span>

7. <span data-ttu-id="404cc-159">Überprüfen Sie auf der Seite **Zusammenfassung** die Features, die hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="404cc-159">On the **Summary** page, review the features that will be added.</span></span>

   **<span data-ttu-id="404cc-160">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="404cc-160">Note</span></span>**  
   <span data-ttu-id="404cc-161">Wenn Sie ein Windows PowerShell-Skript der soeben erstellten Einträge erstellen möchten, klicken Sie auf **PowerShell-Skript exportieren**, und speichern Sie dann das Skript.</span><span class="sxs-lookup"><span data-stu-id="404cc-161">To create a Windows PowerShell script of the entries that you just made, click **Export PowerShell Script**, and then save the script.</span></span>



8. <span data-ttu-id="404cc-162">Klicken Sie auf **Hinzufügen** , um die Berichte auf dem Server hinzuzufügen, und klicken Sie dann auf **Schließen**.</span><span class="sxs-lookup"><span data-stu-id="404cc-162">Click **Add** to add the Reports on the server, and then click **Close**.</span></span>



## <span data-ttu-id="404cc-163">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="404cc-163">Related topics</span></span>


[<span data-ttu-id="404cc-164">Serverereignisprotokolle</span><span class="sxs-lookup"><span data-stu-id="404cc-164">Server Event Logs</span></span>](server-event-logs.md)

[<span data-ttu-id="404cc-165">Konfigurieren der MBAM 2.5-Serverfunktionen</span><span class="sxs-lookup"><span data-stu-id="404cc-165">Configuring the MBAM 2.5 Server Features</span></span>](configuring-the-mbam-25-server-features.md)

[<span data-ttu-id="404cc-166">So konfigurieren Sie die MBAM 2.5-Webanwendungen</span><span class="sxs-lookup"><span data-stu-id="404cc-166">How to Configure the MBAM 2.5 Web Applications</span></span>](how-to-configure-the-mbam-25-web-applications.md)

[<span data-ttu-id="404cc-167">Überprüfen der Konfiguration von MBAM 2.5 Serverfunktionen</span><span class="sxs-lookup"><span data-stu-id="404cc-167">Validating the MBAM 2.5 Server Feature Configuration</span></span>](validating-the-mbam-25-server-feature-configuration.md)


## <span data-ttu-id="404cc-168">Sie haben einen Vorschlag für MBAM?</span><span class="sxs-lookup"><span data-stu-id="404cc-168">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="404cc-169">[Hier](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)können Sie Vorschläge hinzufügen oder abstimmen.</span><span class="sxs-lookup"><span data-stu-id="404cc-169">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="404cc-170">Bei MBAM-Problemen verwenden Sie das [MBAM TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="404cc-170">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>






