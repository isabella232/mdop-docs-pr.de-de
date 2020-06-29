---
title: MBAM 2.5-Servervoraussetzungen für eigenständige und Configuration Manager-Integrationstopologien
description: MBAM 2.5-Servervoraussetzungen für eigenständige und Configuration Manager-Integrationstopologien
author: dansimp
ms.assetid: 76a6047a-5c6e-42ff-af09-a6f382a69537
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: c9af551b1d867f61912bbf3b759574a840b0645c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811491"
---
# <span data-ttu-id="4bc00-103">MBAM 2.5-Servervoraussetzungen für eigenständige und Configuration Manager-Integrationstopologien</span><span class="sxs-lookup"><span data-stu-id="4bc00-103">MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies</span></span>


<span data-ttu-id="4bc00-104">Bevor Sie die Microsoft BitLocker-Verwaltungs-und-überwachungsinstallation (MBAM) starten, müssen Sie die in diesem Thema aufgeführten Voraussetzungen erfüllen.</span><span class="sxs-lookup"><span data-stu-id="4bc00-104">Before starting the Microsoft BitLocker Administration and Monitoring (MBAM) installation, you must complete the prerequisites listed in this topic.</span></span> <span data-ttu-id="4bc00-105">Diese Voraussetzungen gelten für die eigenständige MBAM-Topologie und die System Center Configuration Manager-Integrations Topologie.</span><span class="sxs-lookup"><span data-stu-id="4bc00-105">These prerequisites apply to the MBAM Stand-alone topology and System Center Configuration Manager Integration topology.</span></span>

<span data-ttu-id="4bc00-106">Wenn Sie MBAM mit System Center Configuration Manager bereitstellen, müssen Sie weitere Voraussetzungen erfüllen, die in [MBAM 2,5-Server Voraussetzungen aufgeführt sind, die nur für die Configuration Manager-Integrations Topologie gelten](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md).</span><span class="sxs-lookup"><span data-stu-id="4bc00-106">If you are deploying MBAM with System Center Configuration Manager, you must complete additional prerequisites, which are listed in [MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md).</span></span>

<span data-ttu-id="4bc00-107">Eine Liste der unterstützten Hardware-und Betriebssysteme für MBAM finden Sie unter [unterstützte MBAM 2,5-Konfigurationen](mbam-25-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="4bc00-107">For a list of the supported hardware and operating systems for MBAM, see [MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md).</span></span>

**<span data-ttu-id="4bc00-108">Wichtig</span><span class="sxs-lookup"><span data-stu-id="4bc00-108">Important</span></span>**  
<span data-ttu-id="4bc00-109">Wenn BitLocker ohne MBAM verwendet wurde, müssen Sie das Laufwerk entschlüsseln und dann TPM mit TPM. msc löschen.</span><span class="sxs-lookup"><span data-stu-id="4bc00-109">If BitLocker was used without MBAM, you must decrypt the drive and then clear TPM using tpm.msc.</span></span> <span data-ttu-id="4bc00-110">MBAM kann den Besitz von TPM nicht übernehmen, wenn der Client-PC bereits verschlüsselt ist und das TPM-Besitzerkennwort erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="4bc00-110">MBAM cannot take ownership of TPM if the client PC is already encrypted and the TPM owner password created.</span></span>



## <span data-ttu-id="4bc00-111">Erforderliche MBAM-Rollen und-Konten</span><span class="sxs-lookup"><span data-stu-id="4bc00-111">Required MBAM roles and accounts</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="4bc00-112">Voraussetzung</span><span class="sxs-lookup"><span data-stu-id="4bc00-112">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="4bc00-113">Details</span><span class="sxs-lookup"><span data-stu-id="4bc00-113">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4bc00-114">In Active Directory-Domänendiensten (AD DS) erstellte Gruppen</span><span class="sxs-lookup"><span data-stu-id="4bc00-114">Groups created in Active Directory Domain Services (AD DS)</span></span></p></td>
<td align="left"><p><span data-ttu-id="4bc00-115"><a href="planning-for-mbam-25-groups-and-accounts.md" data-raw-source="[Planning for MBAM 2.5 Groups and Accounts](planning-for-mbam-25-groups-and-accounts.md)"> </a> Eine Beschreibung dieser Gruppen und Konten finden Sie unter Planen von MBAM 2,5-Gruppen und-Konten.</span><span class="sxs-lookup"><span data-stu-id="4bc00-115">See <a href="planning-for-mbam-25-groups-and-accounts.md" data-raw-source="[Planning for MBAM 2.5 Groups and Accounts](planning-for-mbam-25-groups-and-accounts.md)">Planning for MBAM 2.5 Groups and Accounts</a> for a description of these groups and accounts.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="4bc00-116">Voraussetzungen für die Wiederherstellungsdatenbank</span><span class="sxs-lookup"><span data-stu-id="4bc00-116">Prerequisites for the Recovery Database</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="4bc00-117">Voraussetzung</span><span class="sxs-lookup"><span data-stu-id="4bc00-117">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="4bc00-118">Details</span><span class="sxs-lookup"><span data-stu-id="4bc00-118">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4bc00-119">Unterstützte Version von SQL Server</span><span class="sxs-lookup"><span data-stu-id="4bc00-119">Supported version of SQL Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="4bc00-120">Installieren Sie Microsoft SQL Server mit SQL_Latin1_General_CP1_CI_AS Sortierung.</span><span class="sxs-lookup"><span data-stu-id="4bc00-120">Install Microsoft SQL Server with SQL_Latin1_General_CP1_CI_AS collation.</span></span></p>
<p><span data-ttu-id="4bc00-121">Unterstützte Versionen finden Sie unter <a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)"> unterstützte MBAM 2,5 </a> -Konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="4bc00-121">See <a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)">MBAM 2.5 Supported Configurations</a> for supported versions.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4bc00-122">Erforderliche SQL Server-Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="4bc00-122">Required SQL Server permissions</span></span></p></td>
<td align="left"><p><span data-ttu-id="4bc00-123">Erforderliche Berechtigungen:</span><span class="sxs-lookup"><span data-stu-id="4bc00-123">Required permissions:</span></span></p>
<ul>
<li><p><span data-ttu-id="4bc00-124">Anmeldeserver Rollen für SQL Server-Instanzen:</span><span class="sxs-lookup"><span data-stu-id="4bc00-124">SQL Server instance login server roles:</span></span></p>
<ul>
<li><p><span data-ttu-id="4bc00-125">dbcreator</span><span class="sxs-lookup"><span data-stu-id="4bc00-125">dbcreator</span></span></p></li>
<li><p><span data-ttu-id="4bc00-126">processadmin</span><span class="sxs-lookup"><span data-stu-id="4bc00-126">processadmin</span></span></p></li>
</ul></li>
<li><p><span data-ttu-id="4bc00-127">SQL Server Reporting Services-Instanzen Rechte:</span><span class="sxs-lookup"><span data-stu-id="4bc00-127">SQL Server Reporting Services instance rights:</span></span></p>
<ul>
<li><p><span data-ttu-id="4bc00-128">Erstellen von Ordnern</span><span class="sxs-lookup"><span data-stu-id="4bc00-128">Create Folders</span></span></p></li>
<li><p><span data-ttu-id="4bc00-129">Veröffentlichen von Berichten</span><span class="sxs-lookup"><span data-stu-id="4bc00-129">Publish Reports</span></span></p></li>
</ul></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4bc00-130">Optional – Installieren des in SQL Server verfügbaren Features "transparente Datenverschlüsselung" (DSA)</span><span class="sxs-lookup"><span data-stu-id="4bc00-130">Optional - Install the Transparent Data Encryption (TDE) feature available in SQL Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="4bc00-131">Das Feature "DSA SQL Server" führt die Echtzeit-I/O-Verschlüsselung und-Entschlüsselung der Daten-und Protokolldateien durch, die Ihnen helfen können, Gesetze, Vorschriften und Richtlinien zu erfüllen, die für verschiedene Branchen gelten.</span><span class="sxs-lookup"><span data-stu-id="4bc00-131">The TDE SQL Server feature performs real-time I/O encryption and decryption of the data and log files, which can help you to comply with laws, regulations, and guidelines that apply to various industries.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="4bc00-132">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="4bc00-132">Note</span></span></strong><br/><p><span data-ttu-id="4bc00-133">DSA führt eine echt Zeit Verschlüsselung von Datenbankinformationen durch.</span><span class="sxs-lookup"><span data-stu-id="4bc00-133">TDE performs real-time decryption of database information.</span></span> <span data-ttu-id="4bc00-134">Das bedeutet, dass die Informationen zum Wiederherstellungsschlüssel sichtbar sind, wenn Sie Informationen zum Wiederherstellungsschlüssel in der SQL Server-Datenbank anzeigen und unter einem Konto angemeldet sind, das über Berechtigungen für die Datenbank verfügt.</span><span class="sxs-lookup"><span data-stu-id="4bc00-134">This means that, if you are viewing recovery key information in the SQL Server database and you are logged on under an account that has permissions to the database, the recovery key information is visible.</span></span> <span data-ttu-id="4bc00-135">Weitere Informationen zu DSA finden Sie unter <a href="mbam-25-security-considerations.md" data-raw-source="[MBAM 2.5 Security Considerations](mbam-25-security-considerations.md)"> Sicherheitsüberlegungen zu MBAM 2,5 </a> .</span><span class="sxs-lookup"><span data-stu-id="4bc00-135">To read more about TDE, see <a href="mbam-25-security-considerations.md" data-raw-source="[MBAM 2.5 Security Considerations](mbam-25-security-considerations.md)">MBAM 2.5 Security Considerations</a>.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4bc00-136">SQL Server-Datenbankmodul-Dienste</span><span class="sxs-lookup"><span data-stu-id="4bc00-136">SQL Server Database Engine Services</span></span></p></td>
<td align="left"><p><span data-ttu-id="4bc00-137">SQL Server-Datenbankmoduldienste müssen während der Installation von MBAM Server installiert sein und ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="4bc00-137">SQL Server Database Engine Services must be installed and running during MBAM Server installation.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4bc00-138">Windows PowerShell 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="4bc00-138">Windows PowerShell 3.0 or later</span></span></p></td>
<td align="left"><p><span data-ttu-id="4bc00-139">Windows PowerShell muss nicht auf dem Wiederherstellungsdaten Bankserver installiert werden, wenn Sie Windows PowerShell verwenden, um die Datenbank von einem Remotecomputer aus zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="4bc00-139">Windows PowerShell does not have to be installed on the Recovery Database server if you are using Windows PowerShell to configure the database from a remote computer.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="4bc00-140">Voraussetzungen für die Compliance-und Audit-Datenbank</span><span class="sxs-lookup"><span data-stu-id="4bc00-140">Prerequisites for the Compliance and Audit Database</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="4bc00-141">Voraussetzung</span><span class="sxs-lookup"><span data-stu-id="4bc00-141">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="4bc00-142">Details</span><span class="sxs-lookup"><span data-stu-id="4bc00-142">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4bc00-143">Unterstützte Version von SQL Server</span><span class="sxs-lookup"><span data-stu-id="4bc00-143">Supported version of SQL Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="4bc00-144">Installieren Sie SQL Server mit SQL_Latin1_General_CP1_CI_AS Sortierung.</span><span class="sxs-lookup"><span data-stu-id="4bc00-144">Install SQL Server with SQL_Latin1_General_CP1_CI_AS collation.</span></span></p>
<p><span data-ttu-id="4bc00-145">Unterstützte Versionen finden Sie unter <a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)"> unterstützte MBAM 2,5 </a> -Konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="4bc00-145">See <a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)">MBAM 2.5 Supported Configurations</a> for supported versions.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4bc00-146">Erforderliche SQL Server-Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="4bc00-146">Required SQL Server permissions</span></span></p></td>
<td align="left"><p><span data-ttu-id="4bc00-147">Erforderliche Berechtigungen:</span><span class="sxs-lookup"><span data-stu-id="4bc00-147">Required permissions:</span></span></p>
<ul>
<li><p><span data-ttu-id="4bc00-148">Anmeldeserver Rollen für SQL Server-Instanzen:</span><span class="sxs-lookup"><span data-stu-id="4bc00-148">SQL Server instance login server roles:</span></span></p>
<ul>
<li><p><span data-ttu-id="4bc00-149">dbcreator</span><span class="sxs-lookup"><span data-stu-id="4bc00-149">dbcreator</span></span></p></li>
<li><p><span data-ttu-id="4bc00-150">processadmin</span><span class="sxs-lookup"><span data-stu-id="4bc00-150">processadmin</span></span></p></li>
</ul></li>
<li><p><span data-ttu-id="4bc00-151">SQL Server Reporting Services-Instanzen Rechte:</span><span class="sxs-lookup"><span data-stu-id="4bc00-151">SQL Server Reporting Services instance rights:</span></span></p>
<ul>
<li><p><span data-ttu-id="4bc00-152">Erstellen von Ordnern</span><span class="sxs-lookup"><span data-stu-id="4bc00-152">Create Folders</span></span></p></li>
<li><p><span data-ttu-id="4bc00-153">Veröffentlichen von Berichten</span><span class="sxs-lookup"><span data-stu-id="4bc00-153">Publish Reports</span></span></p></li>
</ul></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4bc00-154">Optional – Installieren des Features "transparente Datenverschlüsselung" (DSA) in SQL Server</span><span class="sxs-lookup"><span data-stu-id="4bc00-154">Optional - Install the Transparent Data Encryption (TDE) feature in SQL Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="4bc00-155">Das Feature "DSA SQL Server" führt die Echtzeit-I/O-Verschlüsselung und-Entschlüsselung der Daten-und Protokolldateien durch, die Ihnen helfen können, Gesetze, Vorschriften und Richtlinien zu erfüllen, die für verschiedene Branchen gelten.</span><span class="sxs-lookup"><span data-stu-id="4bc00-155">The TDE SQL Server feature performs real-time I/O encryption and decryption of the data and log files, which can help you to comply with laws, regulations, and guidelines that apply to various industries.</span></span></p>
<p><span data-ttu-id="4bc00-156">DSA führt eine echt Zeit Verschlüsselung von Datenbankinformationen durch.</span><span class="sxs-lookup"><span data-stu-id="4bc00-156">TDE performs real-time decryption of database information.</span></span> <span data-ttu-id="4bc00-157">Das bedeutet, dass die Informationen zum Wiederherstellungsschlüssel sichtbar sind, wenn Sie Informationen zum Wiederherstellungsschlüssel in der SQL Server-Datenbank anzeigen und unter einem Konto angemeldet sind, das über Berechtigungen für die Datenbank verfügt.</span><span class="sxs-lookup"><span data-stu-id="4bc00-157">This means that, if you are viewing recovery key information in the SQL Server database and you are logged on under an account that has permissions to the database, the recovery key information is visible.</span></span> <span data-ttu-id="4bc00-158">Weitere Informationen zu DSA finden Sie unter <a href="mbam-25-security-considerations.md" data-raw-source="[MBAM 2.5 Security Considerations](mbam-25-security-considerations.md)"> Sicherheitsüberlegungen zu MBAM 2,5 </a> .</span><span class="sxs-lookup"><span data-stu-id="4bc00-158">To read more about TDE, see <a href="mbam-25-security-considerations.md" data-raw-source="[MBAM 2.5 Security Considerations](mbam-25-security-considerations.md)">MBAM 2.5 Security Considerations</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4bc00-159">SQL Server-Datenbankmodul-Dienste</span><span class="sxs-lookup"><span data-stu-id="4bc00-159">SQL Server Database Engine Services</span></span></p></td>
<td align="left"><p><span data-ttu-id="4bc00-160">SQL Server-Datenbankmoduldienste müssen während der Installation von MBAM Server installiert sein und ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="4bc00-160">SQL Server Database Engine Services must be installed and running during MBAM Server installation.</span></span> <span data-ttu-id="4bc00-161">SQL Server kann jedoch remote ausgeführt werden. Sie muss sich nicht auf dem Server befinden, auf dem Sie die MBAM-Server Software installieren.</span><span class="sxs-lookup"><span data-stu-id="4bc00-161">However, SQL Server can be running remotely; it doesn’t have to be on the same server on which you are installing the MBAM Server software.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4bc00-162">Windows PowerShell 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="4bc00-162">Windows PowerShell 3.0 or later</span></span></p></td>
<td align="left"><p><span data-ttu-id="4bc00-163">Wenn Sie Windows PowerShell verwenden, um die Datenbank von einem Remotecomputer zu konfigurieren, muss Windows PowerShell nicht auf dem Kompatibilitäts-und Überwachungsdaten Bankserver installiert werden.</span><span class="sxs-lookup"><span data-stu-id="4bc00-163">Windows PowerShell does not have to be installed on the Compliance and Audit Database server if you are using Windows PowerShell to configure the database from a remote computer.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="4bc00-164">Voraussetzungen für die Berichte</span><span class="sxs-lookup"><span data-stu-id="4bc00-164">Prerequisites for the Reports</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="4bc00-165">Voraussetzung</span><span class="sxs-lookup"><span data-stu-id="4bc00-165">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="4bc00-166">Details</span><span class="sxs-lookup"><span data-stu-id="4bc00-166">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4bc00-167">Unterstützte Version von SQL Server</span><span class="sxs-lookup"><span data-stu-id="4bc00-167">Supported version of SQL Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="4bc00-168">Installieren Sie SQL Server mit SQL_Latin1_General_CP1_CI_AS Sortierung.</span><span class="sxs-lookup"><span data-stu-id="4bc00-168">Install SQL Server with SQL_Latin1_General_CP1_CI_AS collation.</span></span></p>
<p><span data-ttu-id="4bc00-169">Unterstützte Versionen finden Sie unter <a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)"> unterstützte MBAM 2,5 </a> -Konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="4bc00-169">See <a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)">MBAM 2.5 Supported Configurations</a> for supported versions.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4bc00-170">SQL Server Reporting Services (SSRS)</span><span class="sxs-lookup"><span data-stu-id="4bc00-170">SQL Server Reporting Services (SSRS)</span></span></p></td>
<td align="left"><p><span data-ttu-id="4bc00-171">SSRS muss während der Installation von MBAM Server installiert sein und ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="4bc00-171">SSRS must be installed and running during the MBAM Server installation.</span></span></p>
<p><span data-ttu-id="4bc00-172">Konfigurieren Sie SSRS im &quot; einheitlichen &quot; Modus und nicht im nicht konfigurierten oder &quot; SharePoint- &quot; Modus.</span><span class="sxs-lookup"><span data-stu-id="4bc00-172">Configure SSRS in &quot;native&quot; mode and not in unconfigured or &quot;SharePoint&quot; mode.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4bc00-173">Berechtigungen für SSRS-Instanzen – für die Konfiguration von Berichten nur erforderlich, wenn Sie Datenbanken auf einem separaten Server auf dem Server installieren, auf dem Berichte konfiguriert sind.</span><span class="sxs-lookup"><span data-stu-id="4bc00-173">SSRS instance rights – required for configuring Reports only if you are installing databases on a separate server from the server where Reports are configured.</span></span></p></td>
<td align="left"><p><span data-ttu-id="4bc00-174">Erforderliche Instanzen Rechte:</span><span class="sxs-lookup"><span data-stu-id="4bc00-174">Required instance rights:</span></span></p>
<ul>
<li><p><span data-ttu-id="4bc00-175">Erstellen von Ordnern</span><span class="sxs-lookup"><span data-stu-id="4bc00-175">Create Folders</span></span></p></li>
<li><p><span data-ttu-id="4bc00-176">Veröffentlichen von Berichten</span><span class="sxs-lookup"><span data-stu-id="4bc00-176">Publish Reports</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4bc00-177">Windows PowerShell 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="4bc00-177">Windows PowerShell 3.0 or later</span></span></p></td>
<td align="left"><p><span data-ttu-id="4bc00-178">Windows PowerShell muss auf diesem Datenbankserver nicht installiert werden, wenn Sie Windows PowerShell verwenden, um die Datenbank von einem Remotecomputer aus zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="4bc00-178">Windows PowerShell does not have to be installed on this Database server if you are using Windows PowerShell to configure the database from a remote computer.</span></span></p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-prereqsams"></a><span data-ttu-id="4bc00-179">Voraussetzungen für den Verwaltungs-und Überwachungs Server</span><span class="sxs-lookup"><span data-stu-id="4bc00-179">Prerequisites for the Administration and Monitoring Server</span></span>


<span data-ttu-id="4bc00-180">In der folgenden Tabelle sind die Installationsvoraussetzungen für den MBAM-Verwaltungs-und-Überwachungs Server aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="4bc00-180">The following table lists the installation prerequisites for the MBAM Administration and Monitoring Server.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="4bc00-181">Voraussetzung</span><span class="sxs-lookup"><span data-stu-id="4bc00-181">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="4bc00-182">Details</span><span class="sxs-lookup"><span data-stu-id="4bc00-182">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4bc00-183">Rolle des Windows Server-Webservers</span><span class="sxs-lookup"><span data-stu-id="4bc00-183">Windows Server Web Server Role</span></span></p></td>
<td align="left"><p><span data-ttu-id="4bc00-184">Diese Rolle muss einem Server Betriebssystem hinzugefügt werden, das für die Verwaltungs-und Überwachungsserver Funktion unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="4bc00-184">This role must be added to a server operating system that is supported for the Administration and Monitoring Server feature.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4bc00-185">Web Server (IIS)-Verwaltungs Tools</span><span class="sxs-lookup"><span data-stu-id="4bc00-185">Web Server (IIS) Management Tools</span></span></p></td>
<td align="left"><p><span data-ttu-id="4bc00-186">Klicken Sie auf <strong> IIS-Verwaltungsskripts und-Tools </strong> .</span><span class="sxs-lookup"><span data-stu-id="4bc00-186">Click <strong>IIS Management Scripts and Tools</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="4bc00-187">SSL-Zertifikat</span><span class="sxs-lookup"><span data-stu-id="4bc00-187">SSL Certificate</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="4bc00-188">Optional.</span><span class="sxs-lookup"><span data-stu-id="4bc00-188">Optional.</span></span> <span data-ttu-id="4bc00-189">Um die Kommunikation zwischen den Clientcomputern und den Webdiensten zu sichern, müssen Sie ein Zertifikat anfordern und installieren, das von einer vertrauenswürdigen Sicherheitsstelle signiert wurde.</span><span class="sxs-lookup"><span data-stu-id="4bc00-189">To secure communication between the client computers and the web services, you must obtain and install a certificate that a trusted security authority signed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4bc00-190">Webserver-Rollendienste</span><span class="sxs-lookup"><span data-stu-id="4bc00-190">Web Server Role Services</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="4bc00-191">Allgemeine HTTP-Features:</span><span class="sxs-lookup"><span data-stu-id="4bc00-191">Common HTTP Features:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="4bc00-192">Statischer Inhalt</span><span class="sxs-lookup"><span data-stu-id="4bc00-192">Static Content</span></span></p></li>
<li><p><span data-ttu-id="4bc00-193">Standarddokument</span><span class="sxs-lookup"><span data-stu-id="4bc00-193">Default Document</span></span></p></li>
</ul>
<p><strong><span data-ttu-id="4bc00-194">Anwendungsentwicklung:</span><span class="sxs-lookup"><span data-stu-id="4bc00-194">Application Development:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="4bc00-195">ASP.NET</span><span class="sxs-lookup"><span data-stu-id="4bc00-195">ASP.NET</span></span></p></li>
<li><p><span data-ttu-id="4bc00-196">.NET-Erweiterbarkeit</span><span class="sxs-lookup"><span data-stu-id="4bc00-196">.NET Extensibility</span></span></p></li>
<li><p><span data-ttu-id="4bc00-197">ISAPI-Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="4bc00-197">ISAPI Extensions</span></span></p></li>
<li><p><span data-ttu-id="4bc00-198">ISAPI-Filter</span><span class="sxs-lookup"><span data-stu-id="4bc00-198">ISAPI Filters</span></span></p></li>
</ul>
<p><strong><span data-ttu-id="4bc00-199">Sicherheits</span><span class="sxs-lookup"><span data-stu-id="4bc00-199">Security:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="4bc00-200">Windows-Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="4bc00-200">Windows Authentication</span></span></p></li>
<li><p><span data-ttu-id="4bc00-201">Anforderungsfilterung</span><span class="sxs-lookup"><span data-stu-id="4bc00-201">Request Filtering</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4bc00-202">Windows Server-Features</span><span class="sxs-lookup"><span data-stu-id="4bc00-202">Windows Server Features</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="4bc00-203">.NET Framework 4,5-Features:</span><span class="sxs-lookup"><span data-stu-id="4bc00-203">.NET Framework 4.5 features:</span></span></strong></p>
<ul>
<li><p><strong><span data-ttu-id="4bc00-204">.NET Framework 4,5 oder 4,6</span><span class="sxs-lookup"><span data-stu-id="4bc00-204">.NET Framework 4.5 or 4.6</span></span></strong></p>
<ul>
<li><p><strong><span data-ttu-id="4bc00-205">Windows Server 2016 </strong> - .NET Framework 4,6 ist bereits für diese Versionen von Windows Server installiert, aber Sie müssen Sie aktivieren.</span><span class="sxs-lookup"><span data-stu-id="4bc00-205">Windows Server 2016</strong> - .NET Framework 4.6 is already installed for these versions of Windows Server, but you must enable it.</span></span></p></li>  
<li><p><strong><span data-ttu-id="4bc00-206">Windows Server 2012 oder Windows Server 2012 R2 </strong> - .NET Framework 4,5 ist bereits für diese Versionen von Windows Server installiert, aber Sie müssen Sie aktivieren.</span><span class="sxs-lookup"><span data-stu-id="4bc00-206">Windows Server 2012 or Windows Server 2012 R2</strong> - .NET Framework 4.5 is already installed for these versions of Windows Server, but you must enable it.</span></span></p></li>
<li><p><strong><span data-ttu-id="4bc00-207">Windows Server 2008 R2 </strong> - .NET Framework 4,5 ist nicht im Lieferumfang von Windows Server 2008 R2 enthalten, daher müssen Sie <a href="https://go.microsoft.com/fwlink/?LinkId=392318" data-raw-source="[download Microsoft .NET Framework 4.5](https://go.microsoft.com/fwlink/?LinkId=392318)"> Microsoft .NET Framework 4,5 herunterladen </a> und separat installieren.</span><span class="sxs-lookup"><span data-stu-id="4bc00-207">Windows Server 2008 R2</strong> - .NET Framework 4.5 is not included with Windows Server 2008 R2, so you must <a href="https://go.microsoft.com/fwlink/?LinkId=392318" data-raw-source="[download Microsoft .NET Framework 4.5](https://go.microsoft.com/fwlink/?LinkId=392318)">download Microsoft .NET Framework 4.5</a> and install it separately.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="4bc00-208">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="4bc00-208">Note</span></span></strong><br/><p><span data-ttu-id="4bc00-209">Wenn Sie ein Upgrade von MBAM 2,0 oder MBAM 2,0 SP1 durchführen und .NET Framework 4,5 installieren müssen, lesen Sie <a href="release-notes-for-mbam-25.md" data-raw-source="[Release Notes for MBAM 2.5](release-notes-for-mbam-25.md)"> Versionshinweise für MBAM 2,5, um </a> einen zusätzlichen erforderlichen Schritt für die Arbeit der Websites zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="4bc00-209">If you are upgrading from MBAM 2.0 or MBAM 2.0 SP1 and need to install .NET Framework 4.5, see <a href="release-notes-for-mbam-25.md" data-raw-source="[Release Notes for MBAM 2.5](release-notes-for-mbam-25.md)">Release Notes for MBAM 2.5</a> for an additional required step to make the websites work.</span></span></p>
</div>
<div>

</div></li>
</ul></li>
<li><p><strong><span data-ttu-id="4bc00-210">WCF-Aktivierung</span><span class="sxs-lookup"><span data-stu-id="4bc00-210">WCF Activation</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="4bc00-211">HTTP-Aktivierung</span><span class="sxs-lookup"><span data-stu-id="4bc00-211">HTTP Activation</span></span></p></li>
<li><p><span data-ttu-id="4bc00-212">Nicht-HTTP-Aktivierung (nur für Windows Server 2008, 2012 und 2012 R2)</span><span class="sxs-lookup"><span data-stu-id="4bc00-212">Non-HTTP Activation (Only for Windows Server 2008, 2012, and 2012 R2)</span></span></p>
<p></p></li>
</ul></li>
<li><p><strong><span data-ttu-id="4bc00-213">TCP-Aktivierung</span><span class="sxs-lookup"><span data-stu-id="4bc00-213">TCP Activation</span></span></strong></p></li>
</ul>
<p><strong><span data-ttu-id="4bc00-214">Windows-Prozessaktivierungsdienst:</span><span class="sxs-lookup"><span data-stu-id="4bc00-214">Windows Process Activation Service:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="4bc00-215">Prozessmodell</span><span class="sxs-lookup"><span data-stu-id="4bc00-215">Process Model</span></span></p></li>
<li><p><span data-ttu-id="4bc00-216">.NET Framework-Umgebung</span><span class="sxs-lookup"><span data-stu-id="4bc00-216">.NET Framework Environment</span></span></p></li>
<li><p><span data-ttu-id="4bc00-217">Konfigurations-APIs</span><span class="sxs-lookup"><span data-stu-id="4bc00-217">Configuration APIs</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4bc00-218">ASP.NET MVC 4,0</span><span class="sxs-lookup"><span data-stu-id="4bc00-218">ASP.NET MVC 4.0</span></span></p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=392271" data-raw-source="[ASP.NET MVC 4 download](https://go.microsoft.com/fwlink/?LinkId=392271)"><span data-ttu-id="4bc00-219">ASP.NET MVC 4-Download</span><span class="sxs-lookup"><span data-stu-id="4bc00-219">ASP.NET MVC 4 download</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4bc00-220">Dienstprinzipal Name (SPN)</span><span class="sxs-lookup"><span data-stu-id="4bc00-220">Service Principal Name (SPN)</span></span></p></td>
<td align="left"><p><span data-ttu-id="4bc00-221">Die Webanwendungen erfordern einen SPN für den virtuellen Host Namen unter dem Domänenkonto, das Sie für die Webanwendungspools verwenden.</span><span class="sxs-lookup"><span data-stu-id="4bc00-221">The web applications require an SPN for the virtual host name under the domain account that you use for the web application pools.</span></span></p>
<p><span data-ttu-id="4bc00-222">Wenn Ihre Administratorrechte es Ihnen ermöglichen, SPNs in den Active Directory-Domänendiensten zu erstellen, erstellt MBAM den SPN für Sie.</span><span class="sxs-lookup"><span data-stu-id="4bc00-222">If your administrative rights permit you to create SPNs in Active Directory Domain Services, MBAM creates the SPN for you.</span></span> <span data-ttu-id="4bc00-223"><a href="https://technet.microsoft.com/library/cc731241.aspx" data-raw-source="[Setspn](https://technet.microsoft.com/library/cc731241.aspx)">Informationen zu </a> den zum Erstellen von SPNs erforderlichen Rechten finden Sie unter Setspn.</span><span class="sxs-lookup"><span data-stu-id="4bc00-223">See <a href="https://technet.microsoft.com/library/cc731241.aspx" data-raw-source="[Setspn](https://technet.microsoft.com/library/cc731241.aspx)">Setspn</a> for information about the rights required to create SPNs.</span></span></p>
<p><span data-ttu-id="4bc00-224">Wenn Sie nicht über Administratorrechte zum Erstellen von SPNs verfügen, müssen Sie die Active Directory-Administratoren in Ihrer Organisation bitten, den SPN für Sie zu erstellen, indem Sie den folgenden Befehl verwenden.</span><span class="sxs-lookup"><span data-stu-id="4bc00-224">If you do not have administrative rights to create SPNs, you must ask the Active Directory administrators in your organization to create the SPN for you by using the following command.</span></span></p>
<pre class="syntax" space="preserve"><code>Setspn -s http/mbamvirtual contoso\mbamapppooluser
Setspn -s http/mbamvirtual.contoso.com contoso\mbamapppooluser</code></pre>
<p><span data-ttu-id="4bc00-225">Im Codebeispiel lautet der Name des virtuellen Hosts mbamvirtual.contoso.com, und das für die Webanwendungspools verwendete Domänenkonto ist contoso\mbamapppooluser.</span><span class="sxs-lookup"><span data-stu-id="4bc00-225">In the code example, the virtual host name is mbamvirtual.contoso.com, and the domain account used for the web application pools is contoso\mbamapppooluser.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="4bc00-226">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="4bc00-226">Note</span></span></strong><br/><p><span data-ttu-id="4bc00-227">Wenn Sie den Lastenausgleich einrichten, verwenden Sie dasselbe Anwendungspoolkonto auf allen Servern.</span><span class="sxs-lookup"><span data-stu-id="4bc00-227">If you are setting up Load Balancing, use the same application pool account on all servers.</span></span></p>
</div>
<div>

</div>
<p><span data-ttu-id="4bc00-228">Weitere Informationen zum Registrieren von SPNs für vollqualifizierte NetBIOS-und benutzerdefinierte Hostnamen finden Sie unter <a href="planning-how-to-secure-the-mbam-websites.md" data-raw-source="[Planning How to Secure the MBAM Websites](planning-how-to-secure-the-mbam-websites.md)"> Planen der Sicherung der MBAM-Websites </a> .</span><span class="sxs-lookup"><span data-stu-id="4bc00-228">For more information about registering SPNs for fully qualified, NetBIOS, and custom host names, see <a href="planning-how-to-secure-the-mbam-websites.md" data-raw-source="[Planning How to Secure the MBAM Websites](planning-how-to-secure-the-mbam-websites.md)">Planning How to Secure the MBAM Websites</a>.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="4bc00-229">Voraussetzungen für das Self-Service-Portal</span><span class="sxs-lookup"><span data-stu-id="4bc00-229">Prerequisites for the Self-Service Portal</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="4bc00-230">Voraussetzung</span><span class="sxs-lookup"><span data-stu-id="4bc00-230">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="4bc00-231">Details</span><span class="sxs-lookup"><span data-stu-id="4bc00-231">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4bc00-232">Unterstützte Version von Windows Server</span><span class="sxs-lookup"><span data-stu-id="4bc00-232">Supported version of Windows Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="4bc00-233">Unterstützte Versionen finden Sie unter <a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)"> unterstützte MBAM 2,5 </a> -Konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="4bc00-233">See <a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)">MBAM 2.5 Supported Configurations</a> for supported versions.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4bc00-234">ASP.NET MVC 4,0</span><span class="sxs-lookup"><span data-stu-id="4bc00-234">ASP.NET MVC 4.0</span></span></p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=392271" data-raw-source="[ASP.NET MVC 4 download](https://go.microsoft.com/fwlink/?LinkId=392271)"><span data-ttu-id="4bc00-235">ASP.NET MVC 4-Download</span><span class="sxs-lookup"><span data-stu-id="4bc00-235">ASP.NET MVC 4 download</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4bc00-236">Web Service IIS-Verwaltungs Tools</span><span class="sxs-lookup"><span data-stu-id="4bc00-236">Web Service IIS Management Tools</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4bc00-237">Dienstprinzipal Name (SPN)</span><span class="sxs-lookup"><span data-stu-id="4bc00-237">Service Principal Name (SPN)</span></span></p></td>
<td align="left"><p><span data-ttu-id="4bc00-238">Die Webanwendungen erfordern einen SPN für den virtuellen Host Namen unter dem Domänenkonto, das Sie für die Webanwendungspools verwenden.</span><span class="sxs-lookup"><span data-stu-id="4bc00-238">The web applications require an SPN for the virtual host name under the domain account that you use for the web application pools.</span></span></p>
<p><span data-ttu-id="4bc00-239">Wenn Ihre Administratorrechte es Ihnen ermöglichen, SPNs in den Active Directory-Domänendiensten zu erstellen, erstellt MBAM den SPN für Sie.</span><span class="sxs-lookup"><span data-stu-id="4bc00-239">If your administrative rights permit you to create SPNs in Active Directory Domain Services, MBAM creates the SPN for you.</span></span> <span data-ttu-id="4bc00-240"><a href="https://technet.microsoft.com/library/cc731241.aspx" data-raw-source="[Setspn](https://technet.microsoft.com/library/cc731241.aspx)">Informationen zu </a> den zum Erstellen von SPNs erforderlichen Rechten finden Sie unter Setspn.</span><span class="sxs-lookup"><span data-stu-id="4bc00-240">See <a href="https://technet.microsoft.com/library/cc731241.aspx" data-raw-source="[Setspn](https://technet.microsoft.com/library/cc731241.aspx)">Setspn</a> for information about the rights required to create SPNs.</span></span></p>
<p><span data-ttu-id="4bc00-241">Wenn Sie nicht über Administratorrechte zum Erstellen von SPNs verfügen, müssen Sie die Active Directory-Administratoren in ihren Organisationsadministratoren in Ihrer Organisation bitten, den SPN für Sie zu erstellen, indem Sie den folgenden Befehl verwenden.</span><span class="sxs-lookup"><span data-stu-id="4bc00-241">If you do not have administrative rights to create SPNs, you must ask the Active Directory administrators in your organization administrators in your organization to create the SPN for you by using the following command.</span></span></p>
<pre class="syntax" space="preserve"><code>Setspn -s http/mbamvirtual contoso\mbamapppooluser
Setspn -s http/mbamvirtual.contoso.com contoso\mbamapppooluser</code></pre>
<p><span data-ttu-id="4bc00-242">Im Codebeispiel lautet der Name des virtuellen Hosts mbamvirtual.contoso.com, und das für die Webanwendungspools verwendete Domänenkonto ist contoso\mbamapppooluser.</span><span class="sxs-lookup"><span data-stu-id="4bc00-242">In the code example, the virtual host name is mbamvirtual.contoso.com, and the domain account used for the web application pools is contoso\mbamapppooluser.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="4bc00-243">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="4bc00-243">Note</span></span></strong><br/><p><span data-ttu-id="4bc00-244">Wenn Sie den Lastenausgleich einrichten, verwenden Sie dasselbe Anwendungspoolkonto auf allen Servern.</span><span class="sxs-lookup"><span data-stu-id="4bc00-244">If you are setting up Load Balancing, use the same application pool account on all servers.</span></span></p>
</div>
<div>

</div>
<p><span data-ttu-id="4bc00-245">Weitere Informationen zum Registrieren von SPNs für vollqualifizierte NetBIOS-und benutzerdefinierte Hostnamen finden Sie unter <a href="planning-how-to-secure-the-mbam-websites.md" data-raw-source="[Planning How to Secure the MBAM Websites](planning-how-to-secure-the-mbam-websites.md)"> Planen der Sicherung der MBAM-Websites </a> .</span><span class="sxs-lookup"><span data-stu-id="4bc00-245">For more information about registering SPNs for fully qualified, NetBIOS, and custom host names, see <a href="planning-how-to-secure-the-mbam-websites.md" data-raw-source="[Planning How to Secure the MBAM Websites](planning-how-to-secure-the-mbam-websites.md)">Planning How to Secure the MBAM Websites</a>.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="4bc00-246">Voraussetzungen für die Verwaltungsarbeitsstation</span><span class="sxs-lookup"><span data-stu-id="4bc00-246">Prerequisites for the Management Workstation</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="4bc00-247">Voraussetzung</span><span class="sxs-lookup"><span data-stu-id="4bc00-247">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="4bc00-248">Details</span><span class="sxs-lookup"><span data-stu-id="4bc00-248">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4bc00-249">Bevor Sie den MBAM-Client installieren, laden Sie die MBAM-Gruppenrichtlinienvorlagen aus, <a href="https://go.microsoft.com/fwlink/p/?LinkId=393941" data-raw-source="[How to Get MDOP Group Policy (.admx) Templates](https://go.microsoft.com/fwlink/p/?LinkId=393941)"> wie Sie MDOP Gruppenrichtlinien (ADMX)-Vorlagen abrufen, </a> und konfigurieren Sie Sie mit den Einstellungen, die Sie in Ihrem Unternehmen für die BitLocker-Laufwerkverschlüsselung implementieren möchten.</span><span class="sxs-lookup"><span data-stu-id="4bc00-249">Before installing the MBAM Client, download the MBAM Group Policy Templates from <a href="https://go.microsoft.com/fwlink/p/?LinkId=393941" data-raw-source="[How to Get MDOP Group Policy (.admx) Templates](https://go.microsoft.com/fwlink/p/?LinkId=393941)">How to Get MDOP Group Policy (.admx) Templates</a> and configure them with the settings that you want to implement in your enterprise for BitLocker Drive Encryption.</span></span></p></td>
<td align="left"><p><span data-ttu-id="4bc00-250">Bevor Sie den MBAM-Client installieren, gehen Sie folgendermaßen vor:</span><span class="sxs-lookup"><span data-stu-id="4bc00-250">Before installing the MBAM Client, do the following:</span></span></p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="4bc00-251">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="4bc00-251">What to do</span></span></th>
<th align="left"><span data-ttu-id="4bc00-252">Wo erhalte ich Anweisungen?</span><span class="sxs-lookup"><span data-stu-id="4bc00-252">Where to get instructions</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4bc00-253">Kopieren der MBAM-Gruppenrichtlinienvorlagen</span><span class="sxs-lookup"><span data-stu-id="4bc00-253">Copy the MBAM Group Policy Templates</span></span></p></td>
<td align="left"><p><a href="copying-the-mbam-25-group-policy-templates.md" data-raw-source="[Copying the MBAM 2.5 Group Policy Templates](copying-the-mbam-25-group-policy-templates.md)"><span data-ttu-id="4bc00-254">Kopieren die Gruppenrichtlinienvorlagen für MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="4bc00-254">Copying the MBAM 2.5 Group Policy Templates</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4bc00-255">Bearbeiten der Gruppenrichtlinieneinstellungen</span><span class="sxs-lookup"><span data-stu-id="4bc00-255">Edit the Group Policy settings</span></span></p></td>
<td align="left"><p><a href="editing-the-mbam-25-group-policy-settings.md" data-raw-source="[Editing the MBAM 2.5 Group Policy Settings](editing-the-mbam-25-group-policy-settings.md)"><span data-ttu-id="4bc00-256">Bearbeiten der Gruppenrichtlinieneinstellungen für MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="4bc00-256">Editing the MBAM 2.5 Group Policy Settings</span></span></a></p></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
</tbody>
</table>





## <span data-ttu-id="4bc00-257">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="4bc00-257">Related topics</span></span>


[<span data-ttu-id="4bc00-258">Vorbereiten der Umgebung für MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="4bc00-258">Preparing your Environment for MBAM 2.5</span></span>](preparing-your-environment-for-mbam-25.md)

[<span data-ttu-id="4bc00-259">Planen der Bereitstellung von MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="4bc00-259">Planning to Deploy MBAM 2.5</span></span>](planning-to-deploy-mbam-25.md)

[<span data-ttu-id="4bc00-260">Von MBAM 2.5 unterstützte Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="4bc00-260">MBAM 2.5 Supported Configurations</span></span>](mbam-25-supported-configurations.md)




## <span data-ttu-id="4bc00-261">Sie haben einen Vorschlag für MBAM?</span><span class="sxs-lookup"><span data-stu-id="4bc00-261">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="4bc00-262">[Hier](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)können Sie Vorschläge hinzufügen oder abstimmen.</span><span class="sxs-lookup"><span data-stu-id="4bc00-262">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span>
- <span data-ttu-id="4bc00-263">Bei MBAM-Problemen verwenden Sie das [MBAM TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="4bc00-263">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>




