---
title: Bereitstellungsvoraussetzungen für MBAM 2.0
description: Bereitstellungsvoraussetzungen für MBAM 2.0
author: dansimp
ms.assetid: 57d1c2bb-5ea3-457e-badd-dd9206ff0f20
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: ef7ee64a3661009f18e0963d738c57a59885cb20
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811500"
---
# <span data-ttu-id="5e962-103">Bereitstellungsvoraussetzungen für MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="5e962-103">MBAM 2.0 Deployment Prerequisites</span></span>


<span data-ttu-id="5e962-104">Bevor Sie das Setup von Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) starten, sollten Sie sicherstellen, dass Sie die Voraussetzungen für die Installation des Produkts erfüllt haben.</span><span class="sxs-lookup"><span data-stu-id="5e962-104">Before you start Microsoft BitLocker Administration and Monitoring (MBAM) Setup, you should ensure that you have met the prerequisites to install the product.</span></span> <span data-ttu-id="5e962-105">Dieser Abschnitt enthält Informationen, die Sie beim erfolgreichen Planen Ihrer Computerumgebung unterstützen, bevor Sie die Microsoft BitLocker-Verwaltungs-und Überwachungs Server Features und-Clients bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="5e962-105">This section contains information to help you successfully plan your computing environment before you deploy Microsoft BitLocker Administration and Monitoring Server features and Clients.</span></span> <span data-ttu-id="5e962-106">Wenn Sie MBAM mit Configuration Manager installieren, finden Sie weitere Voraussetzungen unter [Planen der Bereitstellung von MBAM mit Configuration Manager](planning-to-deploy-mbam-with-configuration-manager-2.md) .</span><span class="sxs-lookup"><span data-stu-id="5e962-106">If you are installing MBAM with Configuration Manager, see [Planning to Deploy MBAM with Configuration Manager](planning-to-deploy-mbam-with-configuration-manager-2.md) for additional prerequisites.</span></span>

## <span data-ttu-id="5e962-107">Voraussetzungen für die Installation von MBAM Server Features</span><span class="sxs-lookup"><span data-stu-id="5e962-107">Installation Prerequisites for MBAM Server Features</span></span>


<span data-ttu-id="5e962-108">Für jedes der MBAM-Server Features gelten bestimmte Voraussetzungen, die erfüllt sein müssen, bevor die MBAM-Features erfolgreich installiert werden können.</span><span class="sxs-lookup"><span data-stu-id="5e962-108">Each of the MBAM Server features has specific prerequisites that must be met before the MBAM features can be successfully installed.</span></span> <span data-ttu-id="5e962-109">MBAM-Setup überprüft, ob alle Voraussetzungen erfüllt sind, bevor die Installation gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="5e962-109">MBAM Setup checks that all prerequisites are met before the installation starts.</span></span>

### <span data-ttu-id="5e962-110">Voraussetzungen für Administration und Monitoring Server</span><span class="sxs-lookup"><span data-stu-id="5e962-110">Prerequisites for Administration and Monitoring Server</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="5e962-111">Voraussetzung</span><span class="sxs-lookup"><span data-stu-id="5e962-111">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="5e962-112">Details</span><span class="sxs-lookup"><span data-stu-id="5e962-112">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="5e962-113">Rolle des Windows Server-Webservers</span><span class="sxs-lookup"><span data-stu-id="5e962-113">Windows Server Web Server Role</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="5e962-114">Diese Rolle muss einem Server Betriebssystem hinzugefügt werden, das für die Verwaltungs-und Überwachungsserver Funktion unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="5e962-114">This role must be added to a server operating system that is supported for the Administration and Monitoring Server feature.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="5e962-115">Web Server (IIS)-Verwaltungs Tools</span><span class="sxs-lookup"><span data-stu-id="5e962-115">Web Server (IIS) Management Tools</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="5e962-116">Wählen Sie <strong> IIS-Verwaltungsskripts und-Tools aus </strong> .</span><span class="sxs-lookup"><span data-stu-id="5e962-116">Select <strong>IIS Management Scripts and Tools</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="5e962-117">SSL-Zertifikat</span><span class="sxs-lookup"><span data-stu-id="5e962-117">SSL Certificate</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="5e962-118">Optional.</span><span class="sxs-lookup"><span data-stu-id="5e962-118">Optional.</span></span> <span data-ttu-id="5e962-119">Um die Kommunikation zwischen den Clients und den Webdiensten zu sichern, müssen Sie ein Zertifikat anfordern und installieren, das von einer vertrauenswürdigen Sicherheitsstelle signiert wurde.</span><span class="sxs-lookup"><span data-stu-id="5e962-119">To secure communication between the clients and the web services, you have to obtain and install a certificate that a trusted security authority signed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="5e962-120">Webserver-Rollendienste</span><span class="sxs-lookup"><span data-stu-id="5e962-120">Web Server Role Services</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="5e962-121">Allgemeine HTTP-Features:</span><span class="sxs-lookup"><span data-stu-id="5e962-121">Common HTTP Features:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="5e962-122">Statischer Inhalt</span><span class="sxs-lookup"><span data-stu-id="5e962-122">Static Content</span></span></p></li>
<li><p><span data-ttu-id="5e962-123">Standarddokument</span><span class="sxs-lookup"><span data-stu-id="5e962-123">Default Document</span></span></p></li>
</ul>
<p><strong><span data-ttu-id="5e962-124">Anwendungsentwicklung:</span><span class="sxs-lookup"><span data-stu-id="5e962-124">Application Development:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="5e962-125">ASP.NET</span><span class="sxs-lookup"><span data-stu-id="5e962-125">ASP.NET</span></span></p></li>
<li><p><span data-ttu-id="5e962-126">.NET-Erweiterbarkeit</span><span class="sxs-lookup"><span data-stu-id="5e962-126">.NET Extensibility</span></span></p></li>
<li><p><span data-ttu-id="5e962-127">ISAPI-Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="5e962-127">ISAPI Extensions</span></span></p></li>
<li><p><span data-ttu-id="5e962-128">ISAPI-Filter</span><span class="sxs-lookup"><span data-stu-id="5e962-128">ISAPI Filters</span></span></p></li>
</ul>
<p><strong><span data-ttu-id="5e962-129">Sicherheits</span><span class="sxs-lookup"><span data-stu-id="5e962-129">Security:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="5e962-130">Windows-Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="5e962-130">Windows Authentication</span></span></p></li>
<li><p><span data-ttu-id="5e962-131">Anforderungsfilterung</span><span class="sxs-lookup"><span data-stu-id="5e962-131">Request Filtering</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="5e962-132">Windows Server-Features</span><span class="sxs-lookup"><span data-stu-id="5e962-132">Windows Server Features</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="5e962-133">.NET Framework 3.5.1-Features:</span><span class="sxs-lookup"><span data-stu-id="5e962-133">.NET Framework 3.5.1 features:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="5e962-134">.NET Framework 3.5.1</span><span class="sxs-lookup"><span data-stu-id="5e962-134">.NET Framework 3.5.1</span></span></p></li>
<li><p><span data-ttu-id="5e962-135">WCF-Aktivierung</span><span class="sxs-lookup"><span data-stu-id="5e962-135">WCF Activation</span></span></p>
<ul>
<li><p><span data-ttu-id="5e962-136">HTTP-Aktivierung</span><span class="sxs-lookup"><span data-stu-id="5e962-136">HTTP Activation</span></span></p></li>
<li><p><span data-ttu-id="5e962-137">Nicht-HTTP-Aktivierung</span><span class="sxs-lookup"><span data-stu-id="5e962-137">Non-HTTP Activation</span></span></p></li>
</ul></li>
</ul>
<p><strong><span data-ttu-id="5e962-138">Windows-Prozessaktivierungsdienst:</span><span class="sxs-lookup"><span data-stu-id="5e962-138">Windows Process Activation Service:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="5e962-139">Prozessmodell</span><span class="sxs-lookup"><span data-stu-id="5e962-139">Process Model</span></span></p></li>
<li><p><span data-ttu-id="5e962-140">.NET-Umgebung</span><span class="sxs-lookup"><span data-stu-id="5e962-140">.NET Environment</span></span></p></li>
<li><p><span data-ttu-id="5e962-141">Konfigurations-APIs</span><span class="sxs-lookup"><span data-stu-id="5e962-141">Configuration APIs</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="5e962-142">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="5e962-142">Note</span></span>**  
<span data-ttu-id="5e962-143">Eine Liste der unterstützten Betriebssysteme finden Sie unter [unterstützte MBAM 2,0-Konfigurationen](mbam-20-supported-configurations-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="5e962-143">For a list of supported operating systems, see [MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md).</span></span>



### <span data-ttu-id="5e962-144">Voraussetzungen für Konformitäts-und Überwachungsberichte</span><span class="sxs-lookup"><span data-stu-id="5e962-144">Prerequisites for the Compliance and Audit Reports</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="5e962-145">Voraussetzung</span><span class="sxs-lookup"><span data-stu-id="5e962-145">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="5e962-146">Details</span><span class="sxs-lookup"><span data-stu-id="5e962-146">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5e962-147">Unterstützte Version von SQL Server</span><span class="sxs-lookup"><span data-stu-id="5e962-147">Supported version of SQL Server</span></span></p>
<p><span data-ttu-id="5e962-148">Unterstützte Versionen finden Sie unter <a href="mbam-20-supported-configurations-mbam-2.md" data-raw-source="[MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md)"> unterstützte MBAM 2,0 </a> -Konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="5e962-148">See <a href="mbam-20-supported-configurations-mbam-2.md" data-raw-source="[MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md)">MBAM 2.0 Supported Configurations</a> for supported versions.</span></span></p></td>
<td align="left"><p><span data-ttu-id="5e962-149">Installieren Sie SQL Server mit:</span><span class="sxs-lookup"><span data-stu-id="5e962-149">Install SQL Server with:</span></span></p>
<ul>
<li><p><span data-ttu-id="5e962-150">SQL_Latin1_General_CP1_CI_AS Sortierung</span><span class="sxs-lookup"><span data-stu-id="5e962-150">SQL_Latin1_General_CP1_CI_AS collation</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5e962-151">SQL Server Reporting Services (SSRS)</span><span class="sxs-lookup"><span data-stu-id="5e962-151">SQL Server Reporting Services (SSRS)</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5e962-152">SSRS-Instanzen Rechte – für die Installation von Berichten nur erforderlich, wenn Sie Datenbanken auf einem separaten Server aus den Berichten installieren.</span><span class="sxs-lookup"><span data-stu-id="5e962-152">SSRS instance rights – required for installing reports only if you are installing databases on a separate server from the reports.</span></span></p></td>
<td align="left"><p><span data-ttu-id="5e962-153">Erforderliche Instanzen Rechte:</span><span class="sxs-lookup"><span data-stu-id="5e962-153">Required instance rights:</span></span></p>
<ul>
<li><p><span data-ttu-id="5e962-154">Erstellen von Ordnern</span><span class="sxs-lookup"><span data-stu-id="5e962-154">Create Folders</span></span></p></li>
<li><p><span data-ttu-id="5e962-155">Veröffentlichen von Berichten</span><span class="sxs-lookup"><span data-stu-id="5e962-155">Publish Reports</span></span></p></li>
</ul>
<p><span data-ttu-id="5e962-156">SSRS muss während der Installation von MBAM Server installiert sein und ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="5e962-156">SSRS must be installed and running during the MBAM Server installation.</span></span> <span data-ttu-id="5e962-157">Konfigurieren Sie SSRS im systemeigenen Modus und nicht im Modus "nicht konfiguriert" oder "SharePoint".</span><span class="sxs-lookup"><span data-stu-id="5e962-157">Configure SSRS in “native” mode and not in unconfigured or “SharePoint” mode.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="5e962-158">Voraussetzungen für die Wiederherstellungsdatenbank</span><span class="sxs-lookup"><span data-stu-id="5e962-158">Prerequisites for the Recovery Database</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="5e962-159">Voraussetzung</span><span class="sxs-lookup"><span data-stu-id="5e962-159">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="5e962-160">Details</span><span class="sxs-lookup"><span data-stu-id="5e962-160">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5e962-161">Unterstützte Version von SQL Server</span><span class="sxs-lookup"><span data-stu-id="5e962-161">Supported version of SQL Server</span></span></p>
<p><span data-ttu-id="5e962-162">Unterstützte Versionen finden Sie unter <a href="mbam-20-supported-configurations-mbam-2.md" data-raw-source="[MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md)"> unterstützte MBAM 2,0 </a> -Konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="5e962-162">See <a href="mbam-20-supported-configurations-mbam-2.md" data-raw-source="[MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md)">MBAM 2.0 Supported Configurations</a> for supported versions.</span></span></p></td>
<td align="left"><p><span data-ttu-id="5e962-163">Installieren Sie SQL Server mit:</span><span class="sxs-lookup"><span data-stu-id="5e962-163">Install SQL Server with:</span></span></p>
<ul>
<li><p><span data-ttu-id="5e962-164">SQL_Latin1_General_CP1_CI_AS Sortierung</span><span class="sxs-lookup"><span data-stu-id="5e962-164">SQL_Latin1_General_CP1_CI_AS collation</span></span></p></li>
<li><p><span data-ttu-id="5e962-165">SQL Server-Verwaltungs Tools</span><span class="sxs-lookup"><span data-stu-id="5e962-165">SQL Server Management Tools</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5e962-166">Erforderliche SQL Server-Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="5e962-166">Required SQL Server permissions</span></span></p></td>
<td align="left"><p><span data-ttu-id="5e962-167">Erforderliche Berechtigungen:</span><span class="sxs-lookup"><span data-stu-id="5e962-167">Required permissions:</span></span></p>
<ul>
<li><p><span data-ttu-id="5e962-168">SQL instance-Anmelde Server Rollen:</span><span class="sxs-lookup"><span data-stu-id="5e962-168">SQL instance Login Server roles:</span></span></p>
<ul>
<li><p><span data-ttu-id="5e962-169">dbcreator</span><span class="sxs-lookup"><span data-stu-id="5e962-169">dbcreator</span></span></p></li>
<li><p><span data-ttu-id="5e962-170">processadmin</span><span class="sxs-lookup"><span data-stu-id="5e962-170">processadmin</span></span></p></li>
</ul></li>
<li><p><span data-ttu-id="5e962-171">SQL Server Reporting Services-Instanzen Rechte:</span><span class="sxs-lookup"><span data-stu-id="5e962-171">SQL Server Reporting Services instance rights:</span></span></p>
<ul>
<li><p><span data-ttu-id="5e962-172">Erstellen von Ordnern</span><span class="sxs-lookup"><span data-stu-id="5e962-172">Create Folders</span></span></p></li>
<li><p><span data-ttu-id="5e962-173">Veröffentlichen von Berichten</span><span class="sxs-lookup"><span data-stu-id="5e962-173">Publish Reports</span></span></p></li>
</ul></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5e962-174">Optional – Installieren der Funktion "transparente Datenverschlüsselung (DSA)" in SQL Server</span><span class="sxs-lookup"><span data-stu-id="5e962-174">Optional - Install Transparent Data Encryption (TDE) feature available in SQL Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="5e962-175">Das Feature "DSA SQL Server" führt die Echtzeit-I/O-Verschlüsselung und-Entschlüsselung der Daten-und Protokolldateien durch, die Ihnen helfen können, viele Gesetze, Vorschriften und Richtlinien zu erfüllen, die in verschiedenen Branchen festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="5e962-175">The TDE SQL Server feature performs real-time I/O encryption and decryption of the data and log files, which can help you to comply with many laws, regulations, and guidelines established in various industries.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="5e962-176">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="5e962-176">Note</span></span></strong><br/><p><span data-ttu-id="5e962-177">DSA führt eine echt Zeit Verschlüsselung von Datenbankinformationen durch, was bedeutet, dass die Informationen zum Wiederherstellungsschlüssel sichtbar sind, wenn das Konto, unter dem Sie angemeldet sind, über Berechtigungen für die Datenbank verfügt, während Sie die Wiederherstellungsschlüssel Informationen in den SQL Server-Tabellen anzeigen.</span><span class="sxs-lookup"><span data-stu-id="5e962-177">TDE performs real-time decryption of database information, which means that, if the account under which you are logged on has permissions to the database while you are viewing the recovery key information in the SQL Server tables, the recovery key information is visible.</span></span></p>
</div>
<div>

</div>
<p><span data-ttu-id="5e962-178">Weitere Informationen zu DSA: <a href="mbam-20-security-considerations-mbam-2.md" data-raw-source="[MBAM 2.0 Security Considerations](mbam-20-security-considerations-mbam-2.md)"> MBAM 2,0-Sicherheitsüberlegungen </a> .</span><span class="sxs-lookup"><span data-stu-id="5e962-178">More about TDE: <a href="mbam-20-security-considerations-mbam-2.md" data-raw-source="[MBAM 2.0 Security Considerations](mbam-20-security-considerations-mbam-2.md)">MBAM 2.0 Security Considerations</a>.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="5e962-179">Voraussetzungen für die Compliance-und Audit-Datenbank</span><span class="sxs-lookup"><span data-stu-id="5e962-179">Prerequisites for the Compliance and Audit Database</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="5e962-180">Voraussetzung</span><span class="sxs-lookup"><span data-stu-id="5e962-180">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="5e962-181">Details</span><span class="sxs-lookup"><span data-stu-id="5e962-181">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5e962-182">Unterstützte Version von SQL Server</span><span class="sxs-lookup"><span data-stu-id="5e962-182">Supported version of SQL Server</span></span></p>
<p><span data-ttu-id="5e962-183">Unterstützte Versionen finden Sie unter <a href="mbam-20-supported-configurations-mbam-2.md" data-raw-source="[MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md)"> unterstützte MBAM 2,0 </a> -Konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="5e962-183">See <a href="mbam-20-supported-configurations-mbam-2.md" data-raw-source="[MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md)">MBAM 2.0 Supported Configurations</a> for supported versions.</span></span></p></td>
<td align="left"><p><span data-ttu-id="5e962-184">Installieren Sie SQL Server mit:</span><span class="sxs-lookup"><span data-stu-id="5e962-184">Install SQL Server with:</span></span></p>
<ul>
<li><p><span data-ttu-id="5e962-185">SQL_Latin1_General_CP1_CI_AS Sortierung</span><span class="sxs-lookup"><span data-stu-id="5e962-185">SQL_Latin1_General_CP1_CI_AS collation</span></span></p></li>
<li><p><span data-ttu-id="5e962-186">SQL Server-Verwaltungs Tools</span><span class="sxs-lookup"><span data-stu-id="5e962-186">SQL Server Management Tools</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5e962-187">Erforderliche SQL Server-Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="5e962-187">Required SQL Server permissions</span></span></p></td>
<td align="left"><p><span data-ttu-id="5e962-188">Erforderliche Berechtigungen:</span><span class="sxs-lookup"><span data-stu-id="5e962-188">Required permissions:</span></span></p>
<ul>
<li><p><span data-ttu-id="5e962-189">SQL instance-Anmelde Server Rollen:</span><span class="sxs-lookup"><span data-stu-id="5e962-189">SQL instance Login Server roles:</span></span></p>
<ul>
<li><p><span data-ttu-id="5e962-190">dbcreator</span><span class="sxs-lookup"><span data-stu-id="5e962-190">dbcreator</span></span></p></li>
<li><p><span data-ttu-id="5e962-191">processadmin</span><span class="sxs-lookup"><span data-stu-id="5e962-191">processadmin</span></span></p></li>
</ul></li>
<li><p><span data-ttu-id="5e962-192">SQL Server Reporting Services-Instanzen Rechte:</span><span class="sxs-lookup"><span data-stu-id="5e962-192">SQL Server Reporting Services instance rights:</span></span></p>
<ul>
<li><p><span data-ttu-id="5e962-193">Erstellen von Ordnern</span><span class="sxs-lookup"><span data-stu-id="5e962-193">Create Folders</span></span></p></li>
<li><p><span data-ttu-id="5e962-194">Veröffentlichen von Berichten</span><span class="sxs-lookup"><span data-stu-id="5e962-194">Publish Reports</span></span></p></li>
</ul></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5e962-195">Optional – Installieren der Funktion "transparente Datenverschlüsselung" (DSA) in SQL Server.</span><span class="sxs-lookup"><span data-stu-id="5e962-195">Optional - Install Transparent Data Encryption (TDE) feature in SQL Server.</span></span></p></td>
<td align="left"><p><span data-ttu-id="5e962-196">Das Feature "DSA SQL Server" führt die Echtzeit-I/O-Verschlüsselung und-Entschlüsselung der Daten-und Protokolldateien durch, die Ihnen helfen können, viele Gesetze, Vorschriften und Richtlinien zu erfüllen, die in verschiedenen Branchen festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="5e962-196">The TDE SQL Server feature performs real-time I/O encryption and decryption of the data and log files, which can help you to comply with many laws, regulations, and guidelines established in various industries.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="5e962-197">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="5e962-197">Note</span></span></strong><br/><p><span data-ttu-id="5e962-198">DSA führt eine echt Zeit Verschlüsselung von Datenbankinformationen durch, was bedeutet, dass die Informationen zum Wiederherstellungsschlüssel sichtbar sind, wenn das Konto, unter dem Sie angemeldet sind, über Berechtigungen für die Datenbank verfügt, während Sie die Wiederherstellungsschlüssel Informationen in den SQL Server-Tabellen anzeigen.</span><span class="sxs-lookup"><span data-stu-id="5e962-198">TDE performs real-time decryption of database information, which means that, if the account under which you are logged on has permissions to the database while you are viewing the recovery key information in the SQL Server tables, the recovery key information is visible.</span></span></p>
</div>
<div>

</div>
<p><span data-ttu-id="5e962-199">Weitere Informationen zu DSA: <a href="mbam-20-security-considerations-mbam-2.md" data-raw-source="[MBAM 2.0 Security Considerations](mbam-20-security-considerations-mbam-2.md)"> MBAM 2,0-Sicherheitsüberlegungen</span><span class="sxs-lookup"><span data-stu-id="5e962-199">More about TDE: <a href="mbam-20-security-considerations-mbam-2.md" data-raw-source="[MBAM 2.0 Security Considerations](mbam-20-security-considerations-mbam-2.md)">MBAM 2.0 Security Considerations</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5e962-200">SQL Server muss während der Installation von MBAM Server Datenbankmoduldienste installiert haben und ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="5e962-200">SQL Server must have Database Engine Services installed and running during MBAM Server installation.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5e962-201">Der SQL Server-Agent-Dienst muss auf den ausgewählten Instanzen von SQL Server ausgeführt und auf Auto-Start eingestellt sein.</span><span class="sxs-lookup"><span data-stu-id="5e962-201">The SQL Server Agent service must be running and set to auto-start on the selected instances of SQL Server.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="5e962-202">Voraussetzungen für das Self-Service-Portal</span><span class="sxs-lookup"><span data-stu-id="5e962-202">Prerequisites for the Self-Service Portal</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="5e962-203">Voraussetzung</span><span class="sxs-lookup"><span data-stu-id="5e962-203">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="5e962-204">Details</span><span class="sxs-lookup"><span data-stu-id="5e962-204">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5e962-205">Unterstützte Version von Windows Server</span><span class="sxs-lookup"><span data-stu-id="5e962-205">Supported version of Windows Server</span></span></p>
<p><span data-ttu-id="5e962-206">Unterstützte Versionen finden Sie unter <a href="mbam-20-supported-configurations-mbam-2.md" data-raw-source="[MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md)"> unterstützte MBAM 2,0 </a> -Konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="5e962-206">See <a href="mbam-20-supported-configurations-mbam-2.md" data-raw-source="[MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md)">MBAM 2.0 Supported Configurations</a> for supported versions.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5e962-207">ASP.NET MVC 2,0</span><span class="sxs-lookup"><span data-stu-id="5e962-207">ASP.NET MVC 2.0</span></span></p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=392270" data-raw-source="[ASP.NET MVC 2 download](https://go.microsoft.com/fwlink/?LinkId=392270)"><span data-ttu-id="5e962-208">ASP.NET MVC 2 herunterladen</span><span class="sxs-lookup"><span data-stu-id="5e962-208">ASP.NET MVC 2 download</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5e962-209">Web Service IIS-Verwaltungs Tools</span><span class="sxs-lookup"><span data-stu-id="5e962-209">Web Service IIS Management Tools</span></span></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="5e962-210">Voraussetzungen für MBAM-Clients</span><span class="sxs-lookup"><span data-stu-id="5e962-210">Prerequisites for MBAM Clients</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="5e962-211">Voraussetzung</span><span class="sxs-lookup"><span data-stu-id="5e962-211">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="5e962-212">Details</span><span class="sxs-lookup"><span data-stu-id="5e962-212">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="5e962-213">Windows 7-Clients </strong> - müssen nur über die TPM-Funktion (Trusted Platform Module) verfügen.</span><span class="sxs-lookup"><span data-stu-id="5e962-213">Windows 7 clients only</strong> - must have Trusted Platform Module (TPM) capability.</span></span></p></td>
<td align="left"><p><span data-ttu-id="5e962-214">Die TPM-Version muss 1,2 oder höher sein.</span><span class="sxs-lookup"><span data-stu-id="5e962-214">TPM version must be 1.2 or later.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5e962-215">Der TPM-Chip muss im BIOS aktiviert sein und vom Betriebssystem Rückstellen.</span><span class="sxs-lookup"><span data-stu-id="5e962-215">The TPM chip must be turned on in the BIOS and be resettable from the operating system.</span></span></p></td>
<td align="left"><p><span data-ttu-id="5e962-216">Weitere Informationen finden Sie in der BIOS-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="5e962-216">For more information, see the BIOS documentation.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="5e962-217">Nur für Windows 8 </strong> -Clients: damit MBAM die TPM-Wiederherstellungsschlüssel speichern und verwalten können: die automatische TPM-Bereitstellung muss deaktiviert sein, und MBAM muss als Besitzer des TPM eingestellt sein, bevor Sie MBAM bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="5e962-217">Windows 8 clients only</strong>: To have MBAM store and manage the TPM recovery keys: TPM auto-provisioning must be turned off, and MBAM must be set as the owner of the TPM before you deploy MBAM.</span></span> <span data-ttu-id="5e962-218">Informationen zum Deaktivieren der automatischen Bereitstellung von TPM finden Sie unter <a href="https://go.microsoft.com/fwlink/?LinkId=286468" data-raw-source="[Disable-TpmAutoProvisioning](https://go.microsoft.com/fwlink/?LinkId=286468)"> Disable-TpmAutoProvisioning </a> .</span><span class="sxs-lookup"><span data-stu-id="5e962-218">To turn off TPM auto-provisioning, see <a href="https://go.microsoft.com/fwlink/?LinkId=286468" data-raw-source="[Disable-TpmAutoProvisioning](https://go.microsoft.com/fwlink/?LinkId=286468)">Disable-TpmAutoProvisioning</a>.</span></span></p>
<ul>
<li><p><span data-ttu-id="5e962-219">Die automatische TPM-Bereitstellung muss deaktiviert sein.</span><span class="sxs-lookup"><span data-stu-id="5e962-219">TPM auto-provisioning must be turned off.</span></span></p></li>
<li><p><span data-ttu-id="5e962-220">MBAM muss als Besitzer des TPM gesetzt sein, bevor Sie MBAM bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="5e962-220">MBAM must be set as the owner of the TPM before you deploy MBAM.</span></span></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="5e962-221">Informationen zum Deaktivieren der automatischen Bereitstellung von TPM finden Sie unter <a href="https://go.microsoft.com/fwlink/?LinkId=286468" data-raw-source="[Disable-TpmAutoProvisioning](https://go.microsoft.com/fwlink/?LinkId=286468)"> Disable-TpmAutoProvisioning </a> .</span><span class="sxs-lookup"><span data-stu-id="5e962-221">To turn off TPM auto-provisioning, see <a href="https://go.microsoft.com/fwlink/?LinkId=286468" data-raw-source="[Disable-TpmAutoProvisioning](https://go.microsoft.com/fwlink/?LinkId=286468)">Disable-TpmAutoProvisioning</a>.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="5e962-222">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="5e962-222">Note</span></span></strong><br/><p><span data-ttu-id="5e962-223">Stellen Sie sicher, dass die Tastatur, das Video oder die Maus direkt verbunden sind und nicht über einen KVM-Schalter (Keyboard, Video oder Maus) verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="5e962-223">Ensure that the keyboard, video, or mouse are directly connected and not managed through a keyboard, video, or mouse (KVM) switch.</span></span> <span data-ttu-id="5e962-224">Ein KVM-Switch kann die Fähigkeit des Computers stören, die physische Anwesenheit von Hardware zu erkennen.</span><span class="sxs-lookup"><span data-stu-id="5e962-224">A KVM switch can interfere with the ability of the computer to detect the physical presence of hardware.</span></span></p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="5e962-225">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="5e962-225">Related topics</span></span>


[<span data-ttu-id="5e962-226">Planen der Bereitstellung von MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="5e962-226">Planning to Deploy MBAM 2.0</span></span>](planning-to-deploy-mbam-20-mbam-2.md)

[<span data-ttu-id="5e962-227">Von MBAM 2.0 unterstützte Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="5e962-227">MBAM 2.0 Supported Configurations</span></span>](mbam-20-supported-configurations-mbam-2.md)









