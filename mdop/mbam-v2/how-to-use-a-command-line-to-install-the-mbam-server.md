---
title: So verwenden Sie eine Befehlszeile zum Installieren des MBAM-Servers
description: So verwenden Sie eine Befehlszeile zum Installieren des MBAM-Servers
author: dansimp
ms.assetid: 6ffc6d41-a793-42c2-b997-95ba47550648
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a689a2df77300300073b2731281004feac87305f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811278"
---
# <span data-ttu-id="9e6ca-103">So verwenden Sie eine Befehlszeile zum Installieren des MBAM-Servers</span><span class="sxs-lookup"><span data-stu-id="9e6ca-103">How to Use a Command Line to Install the MBAM Server</span></span>


<span data-ttu-id="9e6ca-104">Sie können eine Befehlszeile verwenden, um den MBAM-Server entweder mit der eigenständigen oder der Configuration Manager-Topologie zu installieren.</span><span class="sxs-lookup"><span data-stu-id="9e6ca-104">You can use a command line to install the MBAM Server with either the Stand-alone or Configuration Manager topology.</span></span> <span data-ttu-id="9e6ca-105">Das folgende Befehlszeilenbeispiel dient zum Bereitstellen von MBAM auf einem einzelnen Server, bei dem es sich um eine Architektur handelt, die nur in einer Testumgebung verwendet werden sollte.</span><span class="sxs-lookup"><span data-stu-id="9e6ca-105">The following command line example is for deploying MBAM on a single server, which is an architecture that should be used only in a test environment.</span></span> <span data-ttu-id="9e6ca-106">Sie müssen die Befehlszeile beim Bereitstellen von MBAM in einer Produktionsumgebung, die über mehrere Server verfügen soll, entsprechend ändern.</span><span class="sxs-lookup"><span data-stu-id="9e6ca-106">You will need to change the command line accordingly when you deploy MBAM to a production environment, which should have multiple servers.</span></span>

## <span data-ttu-id="9e6ca-107">Befehlszeile für die Bereitstellung des mbam 2.0-Servers mit der eigenständigen Topologie</span><span class="sxs-lookup"><span data-stu-id="9e6ca-107">Command Line for Deploying the MBAM2.0 Server with the Stand-alone Topology</span></span>


<span data-ttu-id="9e6ca-108">Sie können eine Befehlszeile verwenden, die der folgenden ähnelt, um den MBAM-Server mit der eigenständigen Topologie zu installieren.</span><span class="sxs-lookup"><span data-stu-id="9e6ca-108">You can use a command line that is similar to the following to install the MBAM Server with the Stand-alone topology.</span></span>

``` syntax
MbamSetup.exe /qb /l*v MaltaServerInstall.log TOPOLOGY=0 I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 ADDLOCAL=KeyDatabase,ReportsDatabase,Reports,AdministrationMonitoringServer,SelfServiceServer,PolicyTemplate,REPORTS_USERACCOUNT=[UserDomain]\[UserName1] REPORTS_USERACCOUNTPW=[UserPwd1] COMPLIDB_SQLINSTANCE=%computername% RECOVERYANDHWDB_SQLINSTANCE=%computername% SRS_INSTANCENAME=%computername% ADMINANDMON_WEBSITE_PORT=83 WEBSITE_PORT=83
```

<span data-ttu-id="9e6ca-109">In der folgenden Tabelle werden die Befehlszeilenparameter für die Bereitstellung des MBAM-Servers mit der eigenständigen Topologie beschrieben.</span><span class="sxs-lookup"><span data-stu-id="9e6ca-109">The following table describes the command line parameters for deploying the MBAM Server with the Stand-alone topology.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="9e6ca-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="9e6ca-110">Parameter</span></span></th>
<th align="left"><span data-ttu-id="9e6ca-111">Parameter Wert</span><span class="sxs-lookup"><span data-stu-id="9e6ca-111">Parameter Value</span></span></th>
<th align="left"><span data-ttu-id="9e6ca-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9e6ca-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9e6ca-113">Topologie</span><span class="sxs-lookup"><span data-stu-id="9e6ca-113">TOPOLOGY</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e6ca-114">0</span><span class="sxs-lookup"><span data-stu-id="9e6ca-114">0</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e6ca-115">0 – eigenständige Topologie</span><span class="sxs-lookup"><span data-stu-id="9e6ca-115">0 – Stand-alone topology</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9e6ca-116">I_ACCEPT_ENDUSER_LICENSE_AGREEMENT</span><span class="sxs-lookup"><span data-stu-id="9e6ca-116">I_ACCEPT_ENDUSER_LICENSE_AGREEMENT</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e6ca-117">01</span><span class="sxs-lookup"><span data-stu-id="9e6ca-117">01</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e6ca-118">0 – akzeptieren Sie die Lizenz Abkommen1 – akzeptieren Sie den Lizenzvertrag.</span><span class="sxs-lookup"><span data-stu-id="9e6ca-118">0 – do not accept the license agreement1 – accept the license agreement</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9e6ca-119">ADDLOCAL</span><span class="sxs-lookup"><span data-stu-id="9e6ca-119">ADDLOCAL</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="9e6ca-120">Auf dem Server zu installiere Features</span><span class="sxs-lookup"><span data-stu-id="9e6ca-120">Features to be installed on the Server</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="9e6ca-121">Keydatabase</span><span class="sxs-lookup"><span data-stu-id="9e6ca-121">KeyDatabase</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e6ca-122">Wiederherstellungsdatenbank</span><span class="sxs-lookup"><span data-stu-id="9e6ca-122">Recovery Database</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="9e6ca-123">ReportsDatabase</span><span class="sxs-lookup"><span data-stu-id="9e6ca-123">ReportsDatabase</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e6ca-124">Datenbank für Konformitäts-und Überwachungsberichte</span><span class="sxs-lookup"><span data-stu-id="9e6ca-124">Compliance and Audit Reports Database</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="9e6ca-125">Berichte</span><span class="sxs-lookup"><span data-stu-id="9e6ca-125">Reports</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e6ca-126">Konformitäts-und Überwachungsberichte</span><span class="sxs-lookup"><span data-stu-id="9e6ca-126">Compliance and Audit Reports</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="9e6ca-127">AdministrationMonitoringServer</span><span class="sxs-lookup"><span data-stu-id="9e6ca-127">AdministrationMonitoringServer</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e6ca-128">Website "Verwaltung und Überwachung"</span><span class="sxs-lookup"><span data-stu-id="9e6ca-128">Administration and Monitoring website</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="9e6ca-129">SelfServiceServer</span><span class="sxs-lookup"><span data-stu-id="9e6ca-129">SelfServiceServer</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e6ca-130">Self-Service-Portal</span><span class="sxs-lookup"><span data-stu-id="9e6ca-130">Self-Service Portal</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="9e6ca-131">PolicyTemplate</span><span class="sxs-lookup"><span data-stu-id="9e6ca-131">PolicyTemplate</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e6ca-132">MBAM-Gruppenrichtlinienvorlage</span><span class="sxs-lookup"><span data-stu-id="9e6ca-132">MBAM Group Policy template</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9e6ca-133">REPORTS_USERACCOUNT</span><span class="sxs-lookup"><span data-stu-id="9e6ca-133">REPORTS_USERACCOUNT</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e6ca-134">User Domain Benutzername1</span><span class="sxs-lookup"><span data-stu-id="9e6ca-134">[UserDomain][UserName1]</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e6ca-135">Domäne und Benutzerkonto des Reporting Services-Dienstkontos, das auf die Compliance-und Überwachungsdatenbank zugreifen soll</span><span class="sxs-lookup"><span data-stu-id="9e6ca-135">Domain and user account of the Reporting Services service account that will access the Compliance and Audit database</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9e6ca-136">REPORTS_USERACCOUNTPW</span><span class="sxs-lookup"><span data-stu-id="9e6ca-136">REPORTS_USERACCOUNTPW</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e6ca-137">[UserPwd1]</span><span class="sxs-lookup"><span data-stu-id="9e6ca-137">[UserPwd1]</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e6ca-138">Kennwort des Reporting Services-Dienstkontos, das auf die Compliance-und Überwachungsdatenbank zugreifen soll</span><span class="sxs-lookup"><span data-stu-id="9e6ca-138">Password of the Reporting Services service account that will access the Compliance and Audit database</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9e6ca-139">COMPLIDB_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="9e6ca-139">COMPLIDB_SQLINSTANCE</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e6ca-140">Computername</span><span class="sxs-lookup"><span data-stu-id="9e6ca-140">%computername%</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e6ca-141">Name der SQL Server-Instanz für die Compliance-und Überwachungsdatenbank – ersetzen <strong> von% Computer </strong> Name% durch den Computernamen</span><span class="sxs-lookup"><span data-stu-id="9e6ca-141">SQL Server instance name for the Compliance and Audit Database – replace <strong>%computername%</strong> with the computer name</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9e6ca-142">RECOVERYANDHWDB_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="9e6ca-142">RECOVERYANDHWDB_SQLINSTANCE</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e6ca-143">Computername</span><span class="sxs-lookup"><span data-stu-id="9e6ca-143">%computername%</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e6ca-144">Name der SQL Server-Instanz für die Wiederherstellungsdatenbank – ersetzen <strong> von% Computer </strong> Name% durch den Computernamen</span><span class="sxs-lookup"><span data-stu-id="9e6ca-144">SQL Server instance name for the Recovery Database – replace <strong>%computername%</strong> with the computer name</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9e6ca-145">SRS_INSTANCENAME</span><span class="sxs-lookup"><span data-stu-id="9e6ca-145">SRS_INSTANCENAME</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e6ca-146">Computername</span><span class="sxs-lookup"><span data-stu-id="9e6ca-146">%computername%</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e6ca-147">SQL Server-Berichtsserverinstanz, in der die Konformitäts-und Überwachungsberichte installiert werden – ersetzen <strong> von% Computer </strong> Name% durch den Computernamen</span><span class="sxs-lookup"><span data-stu-id="9e6ca-147">SQL Server Reporting Server instance where the Compliance and Audit reports will be installed – replace <strong>%computername%</strong> with the computer name</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9e6ca-148">ADMINANDMON_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="9e6ca-148">ADMINANDMON_WEBSITE_PORT</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e6ca-149">83</span><span class="sxs-lookup"><span data-stu-id="9e6ca-149">83</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e6ca-150">Port für die Verwaltungs-und Überwachungs Website "83" ist nur ein Beispiel</span><span class="sxs-lookup"><span data-stu-id="9e6ca-150">Port for the Administration and Monitoring website; “83” is only an example</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9e6ca-151">WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="9e6ca-151">WEBSITE_PORT</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e6ca-152">83</span><span class="sxs-lookup"><span data-stu-id="9e6ca-152">83</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e6ca-153">Port für die Self-Service-Portal-Website; "83" ist nur ein Beispiel</span><span class="sxs-lookup"><span data-stu-id="9e6ca-153">Port for the Self-Service Portal website; “83” is only an example</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="9e6ca-154">Befehlszeile für die Bereitstellung des mbam 2.0-Servers mit der Configuration Manager-Topologie</span><span class="sxs-lookup"><span data-stu-id="9e6ca-154">Command Line for Deploying the MBAM2.0 Server with the Configuration Manager Topology</span></span>


<span data-ttu-id="9e6ca-155">Sie können eine Befehlszeile verwenden, die der folgenden ähnelt, um den MBAM-Server mit der Configuration Manager-Topologie zu installieren.</span><span class="sxs-lookup"><span data-stu-id="9e6ca-155">You can use a command line that is similar to the following to install the MBAM Server with the Configuration Manager topology.</span></span>

``` syntax
MbamSetup.exe /qn /l*v MaltaServerInstall.log I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 TOPOLOGY=1 COMPLIDB_SQLINSTANCE=%computername% RECOVERYANDHWDB_SQLINSTANCE=%computername% SRS_INSTANCENAME=%computername% REPORTS_USERACCOUNT=[UserDomain]\[UserName] REPORTS_USERACCOUNTPW=[UserPwd] ADMINANDMON_WEBSITE_PORT=83 WEBSITE_PORT=83
```

<span data-ttu-id="9e6ca-156">In der folgenden Tabelle werden die Befehlszeilenparameter für die Installation des mbam 2.0-Servers mit der Configuration Manager-Topologie beschrieben.</span><span class="sxs-lookup"><span data-stu-id="9e6ca-156">The following table describes the command line parameters for installing the MBAM2.0 Server with the Configuration Manager topology.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="9e6ca-157">Parameter</span><span class="sxs-lookup"><span data-stu-id="9e6ca-157">Parameter</span></span></th>
<th align="left"><span data-ttu-id="9e6ca-158">Parameter Wert</span><span class="sxs-lookup"><span data-stu-id="9e6ca-158">Parameter Value</span></span></th>
<th align="left"><span data-ttu-id="9e6ca-159">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9e6ca-159">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9e6ca-160">Topologie</span><span class="sxs-lookup"><span data-stu-id="9e6ca-160">TOPOLOGY</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e6ca-161">1</span><span class="sxs-lookup"><span data-stu-id="9e6ca-161">1</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e6ca-162">1 – Configuration Manager-Topologie</span><span class="sxs-lookup"><span data-stu-id="9e6ca-162">1 – Configuration Manager topology</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9e6ca-163">I_ACCEPT_ENDUSER_LICENSE_AGREEMENT</span><span class="sxs-lookup"><span data-stu-id="9e6ca-163">I_ACCEPT_ENDUSER_LICENSE_AGREEMENT</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e6ca-164">01</span><span class="sxs-lookup"><span data-stu-id="9e6ca-164">01</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e6ca-165">0 – akzeptieren Sie die Lizenz Abkommen1 – akzeptieren Sie den Lizenzvertrag.</span><span class="sxs-lookup"><span data-stu-id="9e6ca-165">0 – do not accept the license agreement1 – accept the license agreement</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9e6ca-166">COMPLIDB_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="9e6ca-166">COMPLIDB_SQLINSTANCE</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e6ca-167">Computername</span><span class="sxs-lookup"><span data-stu-id="9e6ca-167">%computername%</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e6ca-168">Name der SQL Server-Instanz für die Überwachungsdatenbank – ersetzen <strong> von% Computer </strong> Name% durch den Computernamen</span><span class="sxs-lookup"><span data-stu-id="9e6ca-168">SQL Server instance name for the Audit Database – replace <strong>%computername%</strong> with the computer name</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9e6ca-169">RECOVERYANDHWDB_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="9e6ca-169">RECOVERYANDHWDB_SQLINSTANCE</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e6ca-170">Computername</span><span class="sxs-lookup"><span data-stu-id="9e6ca-170">%computername%</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e6ca-171">Name der SQL Server-Instanz für die Wiederherstellungsdatenbank – ersetzen <strong> von% Computer </strong> Name% durch den Computernamen</span><span class="sxs-lookup"><span data-stu-id="9e6ca-171">SQL Server instance name for the Recovery Database - replace <strong>%computername%</strong> with the computer name</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9e6ca-172">SRS_INSTANCENAME</span><span class="sxs-lookup"><span data-stu-id="9e6ca-172">SRS_INSTANCENAME</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e6ca-173">Computername</span><span class="sxs-lookup"><span data-stu-id="9e6ca-173">%computername%</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e6ca-174">SQL Server-Berichtsserverinstanz, in der die Überwachungsberichte installiert werden – ersetzen von% Computername% durch den Computernamen</span><span class="sxs-lookup"><span data-stu-id="9e6ca-174">SQL Server Reporting Server instance where the Audit reports will be installed – replace %computername% with the computer name</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9e6ca-175">REPORTS_USERACCOUNT</span><span class="sxs-lookup"><span data-stu-id="9e6ca-175">REPORTS_USERACCOUNT</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e6ca-176">User Domain Benutzername1</span><span class="sxs-lookup"><span data-stu-id="9e6ca-176">[UserDomain][UserName1]</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e6ca-177">Domäne und Benutzerkonto des Reporting Services-Dienstkontos, das auf die Compliance-und Überwachungsdatenbank zugreifen soll</span><span class="sxs-lookup"><span data-stu-id="9e6ca-177">Domain and user account of the Reporting Services service account that will access the Compliance and Audit database</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9e6ca-178">REPORTS_USERACCOUNTPW</span><span class="sxs-lookup"><span data-stu-id="9e6ca-178">REPORTS_USERACCOUNTPW</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e6ca-179">[UserPwd1]</span><span class="sxs-lookup"><span data-stu-id="9e6ca-179">[UserPwd1]</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e6ca-180">Kennwort des Reporting Services-Dienstkontos, das auf die Compliance-und Überwachungsdatenbank zugreifen soll</span><span class="sxs-lookup"><span data-stu-id="9e6ca-180">Password of the Reporting Services service account that will access the Compliance and Audit database</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9e6ca-181">ADMINANDMON_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="9e6ca-181">ADMINANDMON_WEBSITE_PORT</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e6ca-182">83</span><span class="sxs-lookup"><span data-stu-id="9e6ca-182">83</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e6ca-183">Port für die Verwaltungs-und Überwachungs Website "83" ist nur ein Beispiel</span><span class="sxs-lookup"><span data-stu-id="9e6ca-183">Port for the Administration and Monitoring website; “83” is only an example</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9e6ca-184">WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="9e6ca-184">WEBSITE_PORT</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e6ca-185">83</span><span class="sxs-lookup"><span data-stu-id="9e6ca-185">83</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e6ca-186">Port für die Self-Service-Portal-Website; "83" ist nur ein Beispiel</span><span class="sxs-lookup"><span data-stu-id="9e6ca-186">Port for the Self-Service Portal website; “83” is only an example</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="9e6ca-187">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="9e6ca-187">Related topics</span></span>


[<span data-ttu-id="9e6ca-188">Bereitstellen der Serverinfrastruktur von MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="9e6ca-188">Deploying the MBAM 2.0 Server Infrastructure</span></span>](deploying-the-mbam-20-server-infrastructure-mbam-2.md)

 

 





