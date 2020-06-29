---
title: Überprüfen der Registrierungsschlüssel vor der Installation von App-V 5.x Server
description: Überprüfen der Registrierungsschlüssel vor der Installation von App-V 5.x Server
author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.openlocfilehash: 9fe5a1b37d0fb5208d138939bb2fc79c89171fb3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805930"
---
# <span data-ttu-id="1fef7-103">Überprüfen der Registrierungsschlüssel vor der Installation von App-V 5.x Server</span><span class="sxs-lookup"><span data-stu-id="1fef7-103">Check Registry Keys before installing App-V 5.x Server</span></span>

<span data-ttu-id="1fef7-104">Wenn Sie den App-v-Server vom APP-v 5,0 SP1-Hotfix-Paket 3 oder höher aktualisieren, führen Sie die Schritte in diesem Abschnitt aus, bevor Sie den App-v 5. x-Server installieren.</span><span class="sxs-lookup"><span data-stu-id="1fef7-104">If you are upgrading the App-V Server from App-V 5.0 SP1 Hotfix Package 3 or later, complete the steps in this section before installing the App-V 5.x Server</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="1fef7-105">Wenn dieser Schritt erforderlich ist</span><span class="sxs-lookup"><span data-stu-id="1fef7-105">When this step is required</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="1fef7-106">Sie Aktualisieren von App-V 5,0 SP1 mit allen nachfolgenden Hotfix-Paketen, die Sie mithilfe einer MSP-Datei installiert haben.</span><span class="sxs-lookup"><span data-stu-id="1fef7-106">You are upgrading from App-V 5.0 SP1 with any subsequent Hotfix Packages that you installed by using an .msp file.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="1fef7-107">Für welche Komponenten muss dieser Schritt ausgeführt werden?</span><span class="sxs-lookup"><span data-stu-id="1fef7-107">Which components require that you do this step</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="1fef7-108">Nur die App-V Server-Komponenten, die Sie aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="1fef7-108">Only the App-V Server components that you are upgrading.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="1fef7-109">Wenn Sie diesen Schritt ausführen müssen</span><span class="sxs-lookup"><span data-stu-id="1fef7-109">When you need to do this step</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="1fef7-110">Vor dem Upgrade des App-v-Servers auf App-v 5. x</span><span class="sxs-lookup"><span data-stu-id="1fef7-110">Before you upgrade the App-V Server to App-V 5.x</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="1fef7-111">Was Sie tun müssen</span><span class="sxs-lookup"><span data-stu-id="1fef7-111">What you need to do</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="1fef7-112">Aktualisieren Sie anhand der Informationen in den folgenden Tabellen jeden Registrierungsschlüsselwert unter <code>HKLM\Software\Microsoft\AppV\Server</code> mit dem Wert, den Sie in der ursprünglichen Server Installation angegeben haben.</span><span class="sxs-lookup"><span data-stu-id="1fef7-112">Using the information in the following tables, update each registry key value under <code>HKLM\Software\Microsoft\AppV\Server</code> with the value that you provided in your original server installation.</span></span> <span data-ttu-id="1fef7-113">Durch das Abschließen dieses Schritts werden Registrierungswerte wiederhergestellt, die möglicherweise entfernt wurden, als App-V 5,0 SP1-Hotfix-Pakete installiert wurden.</span><span class="sxs-lookup"><span data-stu-id="1fef7-113">Completing this step restores registry values that may have been removed when App-V 5.0 SP1 Hotfix Packages were installed.</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="1fef7-114">ManagementDatabase-Taste</span><span class="sxs-lookup"><span data-stu-id="1fef7-114">ManagementDatabase key</span></span>**

<span data-ttu-id="1fef7-115">Wenn Sie die Verwaltungsdatenbank installieren, legen Sie diese Registrierungsschlüssel unter `HKLM\Software\Microsoft\AppV\Server\ManagementDatabase` .</span><span class="sxs-lookup"><span data-stu-id="1fef7-115">If you are installing the Management database, set these registry keys under `HKLM\Software\Microsoft\AppV\Server\ManagementDatabase`.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="1fef7-116">Schlüsselname</span><span class="sxs-lookup"><span data-stu-id="1fef7-116">Key name</span></span></th>
<th align="left"><span data-ttu-id="1fef7-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1fef7-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1fef7-118">IS_MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</span><span class="sxs-lookup"><span data-stu-id="1fef7-118">IS_MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</span></span></p></td>
<td align="left"><p><span data-ttu-id="1fef7-119">Beschreibt, ob ein öffentliches Zugriffskonto für den Zugriff auf nicht lokale Verwaltungs Datenbanken erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="1fef7-119">Describes whether a public access account is required to access non-local management databases.</span></span> <span data-ttu-id="1fef7-120">Value ist auf "1" gesetzt, wenn dies erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="1fef7-120">Value is set to “1” if it is required.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1fef7-121">MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="1fef7-121">MANAGEMENT_DB_NAME</span></span></p></td>
<td align="left"><p><span data-ttu-id="1fef7-122">Der Name der Verwaltungsdatenbank.</span><span class="sxs-lookup"><span data-stu-id="1fef7-122">Name of the Management database.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1fef7-123">MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="1fef7-123">MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT</span></span></p></td>
<td align="left"><p><span data-ttu-id="1fef7-124">Konto, das für den Lesezugriff auf die Verwaltungsdatenbank verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1fef7-124">Account used for read (public) access to the Management database.</span></span></p>
<p><span data-ttu-id="1fef7-125">Wird verwendet <code>IS_MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code> , wenn auf 1 gesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="1fef7-125">Used when <code>IS_MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code> is set to 1.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1fef7-126">MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_SID</span><span class="sxs-lookup"><span data-stu-id="1fef7-126">MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_SID</span></span></p></td>
<td align="left"><p><span data-ttu-id="1fef7-127">Secure Identifier (SID) des Kontos, das für den Zugriff auf die Verwaltungsdatenbank für Read (Public) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1fef7-127">Secure identifier (SID) of the account used for read (public) access to the Management database.</span></span></p>
<p><span data-ttu-id="1fef7-128">Wird verwendet <code>IS_MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code> , wenn auf 1 gesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="1fef7-128">Used when <code>IS_MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code> is set to 1.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1fef7-129">MANAGEMENT_DB_SQL_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="1fef7-129">MANAGEMENT_DB_SQL_INSTANCE</span></span></p></td>
<td align="left"><p><span data-ttu-id="1fef7-130">SQL Server-Instanz für die Verwaltungsdatenbank.</span><span class="sxs-lookup"><span data-stu-id="1fef7-130">SQL Server instance for the Management database.</span></span></p>
<p><span data-ttu-id="1fef7-131">Wenn der Wert leer ist, wird die Standarddatenbankinstanz verwendet.</span><span class="sxs-lookup"><span data-stu-id="1fef7-131">If the value is blank, the default database instance is used.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1fef7-132">MANAGEMENT_DB_WRITE_ACCESS_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="1fef7-132">MANAGEMENT_DB_WRITE_ACCESS_ACCOUNT</span></span></p></td>
<td align="left"><p><span data-ttu-id="1fef7-133">Konto, das für den Schreibzugriff (Administrator) für die Verwaltungsdatenbank verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1fef7-133">Account used for write (administrator) access to the Management database.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1fef7-134">MANAGEMENT_DB_WRITE_ACCESS_ACCOUNT_SID</span><span class="sxs-lookup"><span data-stu-id="1fef7-134">MANAGEMENT_DB_WRITE_ACCESS_ACCOUNT_SID</span></span></p></td>
<td align="left"><p><span data-ttu-id="1fef7-135">Secure Identifier (SID) des Kontos, das für den Schreibzugriff (Administrator) auf die Verwaltungsdatenbank verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1fef7-135">Secure identifier (SID) of the account used for write (administrator) access to the Management database.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1fef7-136">MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="1fef7-136">MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</span></span></p></td>
<td align="left"><p><span data-ttu-id="1fef7-137">Verwaltungsserver-Remotecomputer Konto (Domain\Account).</span><span class="sxs-lookup"><span data-stu-id="1fef7-137">Management server remote computer account (domain\account).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1fef7-138">MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="1fef7-138">MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span></span></p></td>
<td align="left"><p><span data-ttu-id="1fef7-139">Installations Administrator-Anmeldung für den Verwaltungsserver (Domain\Account).</span><span class="sxs-lookup"><span data-stu-id="1fef7-139">Installation administrator login for the Management server (domain\account).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1fef7-140">MANAGEMENT_SERVER_MACHINE_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="1fef7-140">MANAGEMENT_SERVER_MACHINE_USE_LOCAL</span></span></p></td>
<td align="left"><p><span data-ttu-id="1fef7-141">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="1fef7-141">Valid values are:</span></span></p>
<ul>
<li><p><strong><span data-ttu-id="1fef7-142">1 </strong> – der Verwaltungsdienst befindet sich auf dem lokalen Computer, das heißt, MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT ist leer.</span><span class="sxs-lookup"><span data-stu-id="1fef7-142">1</strong> – the Management service is on the local computer, that is, MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT is blank.</span></span></p></li>
<li><p><strong><span data-ttu-id="1fef7-143">0 </strong> - der Verwaltungsdienst befindet sich auf einem anderen Computer als auf dem lokalen Computer.</span><span class="sxs-lookup"><span data-stu-id="1fef7-143">0</strong> - the Management service is on a different computer from the local computer.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="1fef7-144">Managementservice-Taste</span><span class="sxs-lookup"><span data-stu-id="1fef7-144">ManagementService key</span></span>**

<span data-ttu-id="1fef7-145">Wenn Sie den Verwaltungsserver installieren, legen Sie diese Registrierungsschlüssel unter `HKLM\Software\Microsoft\AppV\Server\ManagementService` .</span><span class="sxs-lookup"><span data-stu-id="1fef7-145">If you are installing the Management server, set these registry keys under `HKLM\Software\Microsoft\AppV\Server\ManagementService`.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="1fef7-146">Schlüsselname</span><span class="sxs-lookup"><span data-stu-id="1fef7-146">Key name</span></span></th>
<th align="left"><span data-ttu-id="1fef7-147">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1fef7-147">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1fef7-148">MANAGEMENT_ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="1fef7-148">MANAGEMENT_ADMINACCOUNT</span></span></p></td>
<td align="left"><p><span data-ttu-id="1fef7-149">Active Directory-Domänendienste (AD DS)-Gruppe oder-Konto, das zum Verwalten von App-V (Domain\Account) autorisiert ist.</span><span class="sxs-lookup"><span data-stu-id="1fef7-149">Active Directory Domain Services (AD DS) group or account that is authorized to manage App-V (domain\account).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1fef7-150">MANAGEMENT_DB_SQL_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="1fef7-150">MANAGEMENT_DB_SQL_INSTANCE</span></span></p></td>
<td align="left"><p><span data-ttu-id="1fef7-151">SQL Server-Instanz, die die Verwaltungsdatenbank enthält.</span><span class="sxs-lookup"><span data-stu-id="1fef7-151">SQL server instance that contains the Management database.</span></span></p>
<p><span data-ttu-id="1fef7-152">Wenn der Wert leer ist, wird die Standarddatenbankinstanz verwendet.</span><span class="sxs-lookup"><span data-stu-id="1fef7-152">If the value is blank, the default database instance is used.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1fef7-153">MANAGEMENT_DB_SQL_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="1fef7-153">MANAGEMENT_DB_SQL_SERVER_NAME</span></span></p></td>
<td align="left"><p><span data-ttu-id="1fef7-154">Der Name des Remote-SQL-Servers mit der Verwaltungsdatenbank.</span><span class="sxs-lookup"><span data-stu-id="1fef7-154">Name of the remote SQL server with the Management database.</span></span></p>
<p><span data-ttu-id="1fef7-155">Wenn der Wert leer ist, wird der lokale Computer verwendet.</span><span class="sxs-lookup"><span data-stu-id="1fef7-155">If the value is blank, the local computer is used.</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="1fef7-156">ReportingDatabase-Taste</span><span class="sxs-lookup"><span data-stu-id="1fef7-156">ReportingDatabase key</span></span>**

<span data-ttu-id="1fef7-157">Wenn Sie die Berichtsdatenbank installieren, legen Sie diese Registrierungsschlüssel unter `HKLM\Software\Microsoft\AppV\Server\ReportingDatabase` .</span><span class="sxs-lookup"><span data-stu-id="1fef7-157">If you are installing the Reporting database, set these registry keys under `HKLM\Software\Microsoft\AppV\Server\ReportingDatabase`.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="1fef7-158">Schlüsselname</span><span class="sxs-lookup"><span data-stu-id="1fef7-158">Key name</span></span></th>
<th align="left"><span data-ttu-id="1fef7-159">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1fef7-159">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1fef7-160">IS_REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</span><span class="sxs-lookup"><span data-stu-id="1fef7-160">IS_REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</span></span></p></td>
<td align="left"><p><span data-ttu-id="1fef7-161">Beschreibt, ob ein öffentliches Zugriffskonto für den Zugriff auf nicht lokale Berichtsdatenbanken erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="1fef7-161">Describes whether a public access account is required to access non-local reporting databases.</span></span> <span data-ttu-id="1fef7-162">Value ist auf "1" gesetzt, wenn dies erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="1fef7-162">Value is set to “1” if it is required.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1fef7-163">REPORTING_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="1fef7-163">REPORTING_DB_NAME</span></span></p></td>
<td align="left"><p><span data-ttu-id="1fef7-164">Der Name der Berichtsdatenbank.</span><span class="sxs-lookup"><span data-stu-id="1fef7-164">Name of the Reporting database.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1fef7-165">REPORTING_DB_PUBLIC_ACCESS_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="1fef7-165">REPORTING_DB_PUBLIC_ACCESS_ACCOUNT</span></span></p></td>
<td align="left"><p><span data-ttu-id="1fef7-166">Konto, das für den Lesezugriff auf die Berichtsdatenbank verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1fef7-166">Account used for read (public) access to the Reporting database.</span></span></p>
<p><span data-ttu-id="1fef7-167">Wird verwendet <code>IS_REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code> , wenn auf 1 gesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="1fef7-167">Used when <code>IS_REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code> is set to 1.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1fef7-168">REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_SID</span><span class="sxs-lookup"><span data-stu-id="1fef7-168">REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_SID</span></span></p></td>
<td align="left"><p><span data-ttu-id="1fef7-169">Secure Identifier (SID) des Kontos, das für den Zugriff auf die Berichtsdatenbank gelesen (öffentlich) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1fef7-169">Secure identifier (SID) of the account used for read (public) access to the Reporting database.</span></span></p>
<p><span data-ttu-id="1fef7-170">Wird verwendet <code>IS_REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code> , wenn auf 1 gesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="1fef7-170">Used when <code>IS_REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code> is set to 1.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1fef7-171">REPORTING_DB_SQL_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="1fef7-171">REPORTING_DB_SQL_INSTANCE</span></span></p></td>
<td align="left"><p><span data-ttu-id="1fef7-172">SQL Server-Instanz für die Berichtsdatenbank.</span><span class="sxs-lookup"><span data-stu-id="1fef7-172">SQL Server instance for the Reporting database.</span></span></p>
<p><span data-ttu-id="1fef7-173">Wenn der Wert leer ist, wird die Standarddatenbankinstanz verwendet.</span><span class="sxs-lookup"><span data-stu-id="1fef7-173">If the value is blank, the default database instance is used.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1fef7-174">REPORTING_DB_WRITE_ACCESS_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="1fef7-174">REPORTING_DB_WRITE_ACCESS_ACCOUNT</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1fef7-175">REPORTING_DB_WRITE_ACCESS_ACCOUNT_SID</span><span class="sxs-lookup"><span data-stu-id="1fef7-175">REPORTING_DB_WRITE_ACCESS_ACCOUNT_SID</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1fef7-176">REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="1fef7-176">REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</span></span></p></td>
<td align="left"><p><span data-ttu-id="1fef7-177">Reporting Server-Remotecomputer Konto (Domain\Account).</span><span class="sxs-lookup"><span data-stu-id="1fef7-177">Reporting server remote computer account (domain\account).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1fef7-178">REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="1fef7-178">REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span></span></p></td>
<td align="left"><p><span data-ttu-id="1fef7-179">Installations Administrator-Anmeldung für den Berichtsserver (Domain\Account).</span><span class="sxs-lookup"><span data-stu-id="1fef7-179">Installation administrator login for the Reporting server (domain\account).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1fef7-180">REPORTING_SERVER_MACHINE_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="1fef7-180">REPORTING_SERVER_MACHINE_USE_LOCAL</span></span></p></td>
<td align="left"><p><span data-ttu-id="1fef7-181">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="1fef7-181">Valid values are:</span></span></p>
<ul>
<li><p><strong><span data-ttu-id="1fef7-182">1 </strong> – der Berichterstattungsdienst befindet sich auf dem lokalen Computer, das heißt, REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT ist leer.</span><span class="sxs-lookup"><span data-stu-id="1fef7-182">1</strong> – the Reporting service is on the local computer, that is, REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT is blank.</span></span></p></li>
<li><p><strong><span data-ttu-id="1fef7-183">0 </strong> - der Berichterstattungsdienst befindet sich auf einem anderen Computer als auf dem lokalen Computer.</span><span class="sxs-lookup"><span data-stu-id="1fef7-183">0</strong> - the Reporting service is on a different computer from the local computer.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="1fef7-184">ReportingService-Taste</span><span class="sxs-lookup"><span data-stu-id="1fef7-184">ReportingService key</span></span>**

<span data-ttu-id="1fef7-185">Wenn Sie den Berichtsserver installieren, legen Sie diese Registrierungsschlüssel unter `HKLM\Software\Microsoft\AppV\Server\ReportingService` .</span><span class="sxs-lookup"><span data-stu-id="1fef7-185">If you are installing the Reporting server, set these registry keys under `HKLM\Software\Microsoft\AppV\Server\ReportingService`.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="1fef7-186">Schlüsselname</span><span class="sxs-lookup"><span data-stu-id="1fef7-186">Key name</span></span></th>
<th align="left"><span data-ttu-id="1fef7-187">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1fef7-187">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1fef7-188">REPORTING_DB_SQL_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="1fef7-188">REPORTING_DB_SQL_INSTANCE</span></span></p></td>
<td align="left"><p><span data-ttu-id="1fef7-189">SQL Server-Instanz für die Berichtsdatenbank.</span><span class="sxs-lookup"><span data-stu-id="1fef7-189">SQL Server instance for the Reporting database.</span></span></p>
<p><span data-ttu-id="1fef7-190">Wenn der Wert leer ist, wird die Standarddatenbankinstanz verwendet.</span><span class="sxs-lookup"><span data-stu-id="1fef7-190">If the value is blank, the default database instance is used.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1fef7-191">REPORTING_DB_SQL_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="1fef7-191">REPORTING_DB_SQL_SERVER_NAME</span></span></p></td>
<td align="left"><p><span data-ttu-id="1fef7-192">Der Name des Remote-SQL-Servers mit der Berichtsdatenbank.</span><span class="sxs-lookup"><span data-stu-id="1fef7-192">Name of the remote SQL server with the Reporting database.</span></span></p>
<p><span data-ttu-id="1fef7-193">Wenn der Wert leer ist, wird der lokale Computer verwendet.</span><span class="sxs-lookup"><span data-stu-id="1fef7-193">If the value is blank, the local computer is used.</span></span></p></td>
</tr>
</tbody>
</table>

