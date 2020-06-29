---
title: So konfigurieren Sie die MBAM 2.5-Datenbanken
description: So konfigurieren Sie die MBAM 2.5-Datenbanken
author: dansimp
ms.assetid: 66e1c81b-f785-4398-9175-bb5f112c2a35
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c11cb58d8fd9266bd0322e4cf9aa96256b7fbb6a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811866"
---
# <span data-ttu-id="2431d-103">So konfigurieren Sie die MBAM 2.5-Datenbanken</span><span class="sxs-lookup"><span data-stu-id="2431d-103">How to Configure the MBAM 2.5 Databases</span></span>


<span data-ttu-id="2431d-104">In diesem Thema wird erläutert, wie Sie die Microsoft BitLocker-MBAM-2,5-Konformitäts-und-Überwachungsdatenbank und die Wiederherstellungsdatenbank mit folgenden Schritten konfigurieren:</span><span class="sxs-lookup"><span data-stu-id="2431d-104">This topic explains how to configure the Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 Compliance and Audit Database and the Recovery Database by using:</span></span>

-   <span data-ttu-id="2431d-105">Ein Windows PowerShell-Cmdlet</span><span class="sxs-lookup"><span data-stu-id="2431d-105">A Windows PowerShell cmdlet</span></span>

-   <span data-ttu-id="2431d-106">Der Serverkonfigurations-Assistent von MBAM</span><span class="sxs-lookup"><span data-stu-id="2431d-106">The MBAM Server Configuration wizard</span></span>

<span data-ttu-id="2431d-107">Die Anweisungen basieren auf der empfohlenen Architektur in der [Architektur auf hoher Ebene für MBAM 2,5](high-level-architecture-for-mbam-25.md).</span><span class="sxs-lookup"><span data-stu-id="2431d-107">The instructions are based on the recommended architecture in [High-Level Architecture for MBAM 2.5](high-level-architecture-for-mbam-25.md).</span></span>

**<span data-ttu-id="2431d-108">Bevor Sie die Konfiguration starten:</span><span class="sxs-lookup"><span data-stu-id="2431d-108">Before you start the configuration:</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="2431d-109">Schritt</span><span class="sxs-lookup"><span data-stu-id="2431d-109">Step</span></span></th>
<th align="left"><span data-ttu-id="2431d-110">Wo erhalte ich Anweisungen?</span><span class="sxs-lookup"><span data-stu-id="2431d-110">Where to get instructions</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2431d-111">Überprüfen Sie die empfohlene Architektur für MBAM.</span><span class="sxs-lookup"><span data-stu-id="2431d-111">Review the recommended architecture for MBAM.</span></span></p></td>
<td align="left"><p><a href="high-level-architecture-for-mbam-25.md" data-raw-source="[High-Level Architecture for MBAM 2.5](high-level-architecture-for-mbam-25.md)"><span data-ttu-id="2431d-112">High-Level-Architektur für MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="2431d-112">High-Level Architecture for MBAM 2.5</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2431d-113">Überprüfen Sie die unterstützten Konfigurationen für MBAM.</span><span class="sxs-lookup"><span data-stu-id="2431d-113">Review the supported configurations for MBAM.</span></span></p></td>
<td align="left"><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)"><span data-ttu-id="2431d-114">Von MBAM 2.5 unterstützte Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="2431d-114">MBAM 2.5 Supported Configurations</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2431d-115">Führen Sie die erforderlichen Voraussetzungen für jeden Server aus.</span><span class="sxs-lookup"><span data-stu-id="2431d-115">Complete the required prerequisites on each server.</span></span></p></td>
<td align="left"><ul>
<li><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)"><span data-ttu-id="2431d-116">MBAM 2.5-Servervoraussetzungen für eigenständige und Configuration Manager-Integrationstopologien</span><span class="sxs-lookup"><span data-stu-id="2431d-116">MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies</span></span></a></p></li>
<li><p><a href="mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md" data-raw-source="[MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md)"><span data-ttu-id="2431d-117">MBAM 2,5-Server Voraussetzungen, die nur für die Configuration Manager-Integrations Topologie gelten </a> (falls zutreffend)</span><span class="sxs-lookup"><span data-stu-id="2431d-117">MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology</a> (if applicable)</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2431d-118">Installieren Sie die MBAM-Server Software auf jedem Server, auf dem Sie ein MBAM-Server Feature konfigurieren möchten.</span><span class="sxs-lookup"><span data-stu-id="2431d-118">Install the MBAM Server software on each server where you plan to configure an MBAM Server feature.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="2431d-119">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="2431d-119">Note</span></span></strong><br/><p><span data-ttu-id="2431d-120">Sie können die Datenbanken auf einem SQL Server-Remotecomputer mit Windows PowerShell oder einem exportierten Data-tier Application (DAC)-Paket installieren.</span><span class="sxs-lookup"><span data-stu-id="2431d-120">You can install the databases to a remote SQL Server computer by using Windows PowerShell or an exported data-tier application (DAC) package.</span></span> <span data-ttu-id="2431d-121">Weitere Informationen zu DAC-Paketen finden Sie unter <a href="https://technet.microsoft.com/library/ee210546.aspx" data-raw-source="[Data-tier Applications](https://technet.microsoft.com/library/ee210546.aspx)"> Datenebenen-Anwendungen </a> .</span><span class="sxs-lookup"><span data-stu-id="2431d-121">For more information about DAC packages, see <a href="https://technet.microsoft.com/library/ee210546.aspx" data-raw-source="[Data-tier Applications](https://technet.microsoft.com/library/ee210546.aspx)">Data-tier Applications</a>.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><a href="installing-the-mbam-25-server-software.md" data-raw-source="[Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md)"><span data-ttu-id="2431d-122">Installieren der MBAM 2.5-Serversoftware</span><span class="sxs-lookup"><span data-stu-id="2431d-122">Installing the MBAM 2.5 Server Software</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2431d-123">Überprüfen Sie die Voraussetzungen für die Verwendung von Windows PowerShell, wenn Sie Windows PowerShell-Cmdlets zum Konfigurieren der MBAM-Server Features verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="2431d-123">Review the prerequisites for using Windows PowerShell if you plan to use Windows PowerShell cmdlets to configure MBAM Server features.</span></span></p></td>
<td align="left"><p><a href="configuring-mbam-25-server-features-by-using-windows-powershell.md" data-raw-source="[Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)"><span data-ttu-id="2431d-124">Konfigurieren von MBAM 2.5 Serverfunktionen mithilfe von Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="2431d-124">Configuring MBAM 2.5 Server Features by Using Windows PowerShell</span></span></a></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="2431d-125">So konfigurieren Sie die Datenbanken mithilfe von Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="2431d-125">To configure the databases by using Windows PowerShell</span></span>**

1.  <span data-ttu-id="2431d-126">Bevor Sie die Konfiguration starten, lesen Sie [Konfigurieren von MBAM 2,5-Server Features mithilfe von Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md) zum Überprüfen der Voraussetzungen für die Verwendung von Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="2431d-126">Before you start the configuration, see [Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md) to review the prerequisites for using Windows PowerShell.</span></span>

2.  <span data-ttu-id="2431d-127">Verwenden Sie das Windows PowerShell **-Cmdlet Enable-MbamDatabase** , um die Datenbanken zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="2431d-127">Use the **Enable-MbamDatabase** Windows PowerShell cmdlet to configure the databases.</span></span> <span data-ttu-id="2431d-128">Um Informationen zu diesem Windows PowerShell-Cmdlet abzurufen, geben **Sie Get-Help enable-MbamDatabase**ein.</span><span class="sxs-lookup"><span data-stu-id="2431d-128">To get information about this Windows PowerShell cmdlet, type **Get-Help Enable-MbamDatabase**.</span></span>

**<span data-ttu-id="2431d-129">So konfigurieren Sie die Konformitäts-und Überwachungsdatenbank mithilfe des Assistenten</span><span class="sxs-lookup"><span data-stu-id="2431d-129">To configure the Compliance and Audit Database by using the wizard</span></span>**

1. <span data-ttu-id="2431d-130">Starten Sie auf dem Server, auf dem Sie die Datenbanken konfigurieren möchten, den **MBAM-Serverkonfigurations** -Assistenten.</span><span class="sxs-lookup"><span data-stu-id="2431d-130">On the server where you want to configure the databases, start the **MBAM Server Configuration** wizard.</span></span> <span data-ttu-id="2431d-131">Sie können **MBAM Server Configuration** im **Startmenü** auswählen, um den Assistenten zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="2431d-131">You can select **MBAM Server Configuration** from the **Start** menu to open the wizard.</span></span>

2. <span data-ttu-id="2431d-132">Klicken Sie auf **neue Features hinzufügen**, wählen Sie **Compliance und Audit Database** und **Recovery Database**aus, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="2431d-132">Click **Add New Features**, select **Compliance and Audit Database** and **Recovery Database**, and then click **Next**.</span></span> <span data-ttu-id="2431d-133">Der Assistent überprüft, ob alle Voraussetzungen für die Datenbanken erfüllt sind.</span><span class="sxs-lookup"><span data-stu-id="2431d-133">The wizard checks that all prerequisites for the databases have been met.</span></span>

3. <span data-ttu-id="2431d-134">Wenn die Voraussetzungsprüfung erfolgreich ist, klicken Sie auf **weiter** , um fortzufahren.</span><span class="sxs-lookup"><span data-stu-id="2431d-134">If the prerequisite check is successful, click **Next** to continue.</span></span> <span data-ttu-id="2431d-135">Beheben Sie andernfalls alle fehlenden Voraussetzungen, und klicken Sie dann **erneut auf Voraussetzungen prüfen**.</span><span class="sxs-lookup"><span data-stu-id="2431d-135">Otherwise, resolve any missing prerequisites, and then click **Check prerequisites again**.</span></span>

4. <span data-ttu-id="2431d-136">Geben Sie anhand der folgenden Beschreibungen die Feldwerte im Assistenten ein:</span><span class="sxs-lookup"><span data-stu-id="2431d-136">Using the following descriptions, enter the field values in the wizard:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="2431d-137">Feld</span><span class="sxs-lookup"><span data-stu-id="2431d-137">Field</span></span></th>
   <th align="left"><span data-ttu-id="2431d-138">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2431d-138">Description</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="2431d-139">SQL Server-Name</span><span class="sxs-lookup"><span data-stu-id="2431d-139">SQL Server name</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="2431d-140">Der Name des Servers, auf dem Sie die Kompatibilitäts-und Überwachungsdatenbank konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="2431d-140">Name of the server where you are configuring the Compliance and Audit Database.</span></span></p>
   <div class="alert">
   <strong><span data-ttu-id="2431d-141">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="2431d-141">Note</span></span></strong><br/><p><span data-ttu-id="2431d-142">Sie müssen auf dem Computer Compliance und Audit Database eine Ausnahme hinzufügen, um eingehenden Datenverkehr auf dem Microsoft SQL Server-Port zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="2431d-142">You must add an exception on the Compliance and Audit Database computer to enable inbound traffic on the Microsoft SQL Server port.</span></span> <span data-ttu-id="2431d-143">Die Standardportnummer ist 1433.</span><span class="sxs-lookup"><span data-stu-id="2431d-143">The default port number is 1433.</span></span></p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="2431d-144">SQL Server-Datenbankinstanz</span><span class="sxs-lookup"><span data-stu-id="2431d-144">SQL Server database instance</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="2431d-145">Der Name der Datenbankinstanz, in der die Konformitäts-und Überwachungsdaten gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="2431d-145">Name of the database instance where the compliance and audit data will be stored.</span></span> <span data-ttu-id="2431d-146">Sie müssen außerdem angeben, wo sich die Datenbankinformationen befinden sollen.</span><span class="sxs-lookup"><span data-stu-id="2431d-146">You must also specify where the database information will be located.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="2431d-147">Datenbankname</span><span class="sxs-lookup"><span data-stu-id="2431d-147">Database name</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="2431d-148">Der Name der Datenbank, in der die Kompatibilitätsdaten gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="2431d-148">Name of the database that will store the compliance data.</span></span></p>
   <div class="alert">
   <strong><span data-ttu-id="2431d-149">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="2431d-149">Note</span></span></strong><br/><p><span data-ttu-id="2431d-150">Wenn Sie ein Upgrade von einer früheren Version von MBAM durchführen, müssen Sie denselben Datenbanknamen wie den Namen verwenden, der in der vorherigen Bereitstellung verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="2431d-150">If you are upgrading from a previous version of MBAM, you must use the same database name as the name that was used in your previous deployment.</span></span></p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="2431d-151">Lese/Schreib-Zugriffsdomänen Benutzer oder-Gruppe</span><span class="sxs-lookup"><span data-stu-id="2431d-151">Read/write access domain user or group</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="2431d-152">Domänenbenutzer oder-Gruppe, die über die Berechtigung "Lesen/Schreiben" für diese Datenbank verfügt, damit die Webanwendungen auf die Daten und Berichte in dieser Datenbank zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="2431d-152">Domain user or group that has read/write permission to this database to enable the web applications to access the data and reports in this database.</span></span></p>
   <p><span data-ttu-id="2431d-153">Wenn Sie einen Benutzer in dieses Feld eingeben, muss er mit dem Wert im <strong> Feld Domänenkonto des Webdienst-Anwendungspools </strong> auf der <strong> Seite Webanwendungen konfigurieren identisch sein </strong> .</span><span class="sxs-lookup"><span data-stu-id="2431d-153">If you enter a user in this field, it must be the same value as the value in the <strong>Web service application pool domain account</strong> field on the <strong>Configure Web Applications</strong> page.</span></span></p>
   <p><span data-ttu-id="2431d-154">Wenn Sie eine Gruppe in dieses Feld eingeben, muss der Wert im <strong> Feld "Webdienst-Anwendungspool Domäne" </strong> auf der <strong> Seite "Webanwendungen konfigurieren" </strong> ein Mitglied der Gruppe sein, die Sie in dieses Feld eingeben.</span><span class="sxs-lookup"><span data-stu-id="2431d-154">If you enter a group in this field, the value in the <strong>Web service application pool domain account</strong> field on the <strong>Configure Web Applications</strong> page must be a member of the group you enter in this field.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="2431d-155">Schreibgeschützter Zugriffsdomänen Benutzer oder-Gruppe</span><span class="sxs-lookup"><span data-stu-id="2431d-155">Read-only access domain user or group</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="2431d-156">Der Name des Benutzers oder der Gruppe, der über die Berechtigung "schreibgeschützt" für diese Datenbank verfügt, damit die Berichte auf die Kompatibilitätsdaten in dieser Datenbank zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="2431d-156">Name of the user or group that will have read-only permission to this database to enable the reports to access the compliance data in this database.</span></span></p>
   <p><span data-ttu-id="2431d-157">Wenn Sie einen Benutzer in dieses Feld eingeben, muss er derselbe Benutzer sein, den Sie im <strong> Feld Konformitäts-und Überwachungsdatenbank-Domänenkonto </strong> auf der <strong> Seite Berichte konfigurieren angeben </strong> .</span><span class="sxs-lookup"><span data-stu-id="2431d-157">If you enter a user in this field, it must be the same user as the one you specify in the <strong>Compliance and Audit Database domain account</strong> field on the <strong>Configure Reports</strong> page.</span></span></p>
   <p><span data-ttu-id="2431d-158">Wenn Sie eine Gruppe in dieses Feld eingeben, muss der Wert, den Sie im <strong> Feld Compliance und Audit Database Domain Account angeben, </strong> auf der <strong> Seite "Berichte konfigurieren" </strong> ein Mitglied der Gruppe sein, die Sie in diesem Feld angeben.</span><span class="sxs-lookup"><span data-stu-id="2431d-158">If you enter a group in this field, the value that you specify in the <strong>Compliance and Audit Database domain account</strong> field on the <strong>Configure Reports</strong> page must be a member of the group that you specify in this field.</span></span></p></td>
   </tr>
   </tbody>
   </table>



5. <span data-ttu-id="2431d-159">Fahren Sie mit dem nächsten Abschnitt fort, um die Wiederherstellungsdatenbank zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="2431d-159">Continue to the next section to configure the Recovery Database.</span></span>

**<span data-ttu-id="2431d-160">So konfigurieren Sie die Wiederherstellungsdatenbank mithilfe des Assistenten</span><span class="sxs-lookup"><span data-stu-id="2431d-160">To configure the Recovery Database by using the wizard</span></span>**

1. <span data-ttu-id="2431d-161">Geben Sie anhand der folgenden Beschreibungen die Feldwerte im Assistenten ein:</span><span class="sxs-lookup"><span data-stu-id="2431d-161">Using the following descriptions, enter the field values in the wizard:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="2431d-162">Feld</span><span class="sxs-lookup"><span data-stu-id="2431d-162">Field</span></span></th>
   <th align="left"><span data-ttu-id="2431d-163">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2431d-163">Description</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="2431d-164">SQL Server-Name</span><span class="sxs-lookup"><span data-stu-id="2431d-164">SQL Server name</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="2431d-165">Der Name des Servers, auf dem Sie die Wiederherstellungsdatenbank konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="2431d-165">Name of the server where you are configuring the Recovery Database.</span></span></p>
   <div class="alert">
   <strong><span data-ttu-id="2431d-166">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="2431d-166">Note</span></span></strong><br/><p><span data-ttu-id="2431d-167">Sie müssen auf dem Wiederherstellungsdaten Bank Computer eine Ausnahme hinzufügen, um eingehenden Datenverkehr auf dem Microsoft SQL Server-Port zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="2431d-167">You must add an exception on the Recovery Database computer to enable inbound traffic on the Microsoft SQL Server port.</span></span> <span data-ttu-id="2431d-168">Die Standardportnummer ist 1433.</span><span class="sxs-lookup"><span data-stu-id="2431d-168">The default port number is 1433.</span></span></p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="2431d-169">SQL Server-Datenbankinstanz</span><span class="sxs-lookup"><span data-stu-id="2431d-169">SQL Server database instance</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="2431d-170">Der Name der Datenbankinstanz, in der die Wiederherstellungsdaten gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="2431d-170">Name of the database instance where the recovery data will be stored.</span></span> <span data-ttu-id="2431d-171">Sie müssen außerdem angeben, wo sich die Datenbankinformationen befinden sollen.</span><span class="sxs-lookup"><span data-stu-id="2431d-171">You must also specify where the database information will be located.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="2431d-172">Datenbankname</span><span class="sxs-lookup"><span data-stu-id="2431d-172">Database name</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="2431d-173">Der Name der Datenbank, in der die Wiederherstellungsdaten gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="2431d-173">Name of the database that will store the recovery data.</span></span></p>
   <div class="alert">
   <strong><span data-ttu-id="2431d-174">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="2431d-174">Note</span></span></strong><br/><p><span data-ttu-id="2431d-175">Wenn Sie ein Upgrade von einer früheren Version von MBAM durchführen, müssen Sie denselben Datenbanknamen wie den Namen verwenden, der in der vorherigen Bereitstellung verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="2431d-175">If you are upgrading from a previous version of MBAM, you must use the same database name as the name that was used in your previous deployment.</span></span></p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="2431d-176">Lese/Schreib-Zugriffsdomänen Benutzer oder-Gruppe</span><span class="sxs-lookup"><span data-stu-id="2431d-176">Read/write access domain user or group</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="2431d-177">Domänenbenutzer oder-Gruppe, die über die Berechtigung "Lesen/Schreiben" für diese Datenbank verfügt, damit die Webanwendungen auf die Daten und Berichte in dieser Datenbank zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="2431d-177">Domain user or group that has read/write permission to this database to enable the web applications to access the data and reports in this database.</span></span></p>
   <p><span data-ttu-id="2431d-178">Wenn Sie einen Benutzer in dieses Feld eingeben, muss er mit dem Wert im <strong> Feld Domänenkonto des Webdienst-Anwendungspools </strong> auf der <strong> Seite Webanwendungen konfigurieren identisch sein </strong> .</span><span class="sxs-lookup"><span data-stu-id="2431d-178">If you enter a user in this field, it must be the same value as the value in the <strong>Web service application pool domain account</strong> field on the <strong>Configure Web Applications</strong> page.</span></span></p>
   <p><span data-ttu-id="2431d-179">Wenn Sie eine Gruppe in dieses Feld eingeben, muss der Wert im <strong> Feld "Webdienst-Anwendungspool Domäne" </strong> auf der <strong> Seite "Webanwendungen konfigurieren" </strong> ein Mitglied der Gruppe sein, die Sie in dieses Feld eingeben.</span><span class="sxs-lookup"><span data-stu-id="2431d-179">If you enter a group in this field, the value in the <strong>Web service application pool domain account</strong> field on the <strong>Configure Web Applications</strong> page must be a member of the group you enter in this field.</span></span></p></td>
   </tr>
   </tbody>
   </table>



2. <span data-ttu-id="2431d-180">Wenn Sie Ihre Eingaben abgeschlossen haben, klicken Sie auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="2431d-180">When you finish your entries, click **Next**.</span></span>

   <span data-ttu-id="2431d-181">Der Assistent überprüft, ob alle Voraussetzungen für die Datenbanken erfüllt sind.</span><span class="sxs-lookup"><span data-stu-id="2431d-181">The wizard checks that all prerequisites for the databases have been met.</span></span>

3. <span data-ttu-id="2431d-182">Wenn die Voraussetzungsprüfung erfolgreich ist, klicken Sie auf **weiter** , um fortzufahren.</span><span class="sxs-lookup"><span data-stu-id="2431d-182">If the prerequisite check is successful, click **Next** to continue.</span></span> <span data-ttu-id="2431d-183">Beheben Sie andernfalls alle fehlenden Voraussetzungen, und klicken Sie dann erneut auf **weiter** .</span><span class="sxs-lookup"><span data-stu-id="2431d-183">Otherwise, resolve any missing prerequisites, and then click **Next** again.</span></span>

4. <span data-ttu-id="2431d-184">Überprüfen Sie auf der Seite **Zusammenfassung** die Features, die hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="2431d-184">On the **Summary** page, review the features that will be added.</span></span>

   **<span data-ttu-id="2431d-185">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="2431d-185">Note</span></span>**  
   <span data-ttu-id="2431d-186">Wenn Sie ein Windows PowerShell-Skript der soeben erstellten Einträge erstellen möchten, klicken Sie auf **PowerShell-Skript exportieren**, und speichern Sie dann das Skript.</span><span class="sxs-lookup"><span data-stu-id="2431d-186">To create a Windows PowerShell script of the entries that you just made, click **Export PowerShell Script**, and then save the script.</span></span>



5. <span data-ttu-id="2431d-187">Klicken Sie auf **Hinzufügen** , um die MBAM-Datenbanken auf dem Server hinzuzufügen, und klicken Sie dann auf **Schließen**.</span><span class="sxs-lookup"><span data-stu-id="2431d-187">Click **Add** to add the MBAM databases on the server, and then click **Close**.</span></span>



## <span data-ttu-id="2431d-188">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="2431d-188">Related topics</span></span>


[<span data-ttu-id="2431d-189">Serverereignisprotokolle</span><span class="sxs-lookup"><span data-stu-id="2431d-189">Server Event Logs</span></span>](server-event-logs.md)

[<span data-ttu-id="2431d-190">Konfigurieren der MBAM 2.5-Serverfunktionen</span><span class="sxs-lookup"><span data-stu-id="2431d-190">Configuring the MBAM 2.5 Server Features</span></span>](configuring-the-mbam-25-server-features.md)

[<span data-ttu-id="2431d-191">So konfigurieren Sie die MBAM 2.5-Berichte</span><span class="sxs-lookup"><span data-stu-id="2431d-191">How to Configure the MBAM 2.5 Reports</span></span>](how-to-configure-the-mbam-25-reports.md)

[<span data-ttu-id="2431d-192">So konfigurieren Sie die MBAM 2.5-Webanwendungen</span><span class="sxs-lookup"><span data-stu-id="2431d-192">How to Configure the MBAM 2.5 Web Applications</span></span>](how-to-configure-the-mbam-25-web-applications.md)

[<span data-ttu-id="2431d-193">Überprüfen der Konfiguration von MBAM 2.5 Serverfunktionen</span><span class="sxs-lookup"><span data-stu-id="2431d-193">Validating the MBAM 2.5 Server Feature Configuration</span></span>](validating-the-mbam-25-server-feature-configuration.md)



## <span data-ttu-id="2431d-194">Sie haben einen Vorschlag für MBAM?</span><span class="sxs-lookup"><span data-stu-id="2431d-194">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="2431d-195">[Hier](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)können Sie Vorschläge hinzufügen oder abstimmen.</span><span class="sxs-lookup"><span data-stu-id="2431d-195">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span>
- <span data-ttu-id="2431d-196">Bei MBAM-Problemen verwenden Sie das [MBAM TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="2431d-196">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





