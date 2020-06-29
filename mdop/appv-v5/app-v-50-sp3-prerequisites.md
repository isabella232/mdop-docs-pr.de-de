---
title: Voraussetzungen für App-V 5.0 SP3
description: Voraussetzungen für App-V 5.0 SP3
author: dansimp
ms.assetid: fa8d5578-3a53-4e8a-95c7-e7a5f6e4a31c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d8e8318a71d2d3631b0ad47e3c3db3c569488790
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805999"
---
# <span data-ttu-id="e0836-103">Voraussetzungen für App-V 5.0 SP3</span><span class="sxs-lookup"><span data-stu-id="e0836-103">App-V 5.0 SP3 Prerequisites</span></span>


<span data-ttu-id="e0836-104">Bevor Sie Microsoft Application Virtualization (App-V) 5,0 SP3 installieren, stellen Sie sicher, dass Sie alle der folgenden erforderlichen Software installiert haben.</span><span class="sxs-lookup"><span data-stu-id="e0836-104">Before installing Microsoft Application Virtualization (App-V) 5.0 SP3, ensure that you have installed all of the following required prerequisite software.</span></span>

<span data-ttu-id="e0836-105">Eine Liste der unterstützten Betriebssysteme und Hardwareanforderungen für App-v Server, Sequencer und Client finden Sie unter [unterstützte Konfigurationen für App-v 5,0 SP3](app-v-50-sp3-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="e0836-105">For a list of supported operating systems and hardware requirements for the App-V Server, Sequencer, and Client, see [App-V 5.0 SP3 Supported Configurations](app-v-50-sp3-supported-configurations.md).</span></span>

## <span data-ttu-id="e0836-106">Zusammenfassung der Software, die auf jedem Betriebssystem vorinstalliert ist</span><span class="sxs-lookup"><span data-stu-id="e0836-106">Summary of software preinstalled on each operating system</span></span>


<span data-ttu-id="e0836-107">Die folgende Tabelle zeigt die Software, die bereits für unterschiedliche Betriebssysteme installiert ist.</span><span class="sxs-lookup"><span data-stu-id="e0836-107">The following table indicates the software that is already installed for different operating systems.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="e0836-108">Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="e0836-108">Operating system</span></span></th>
<th align="left"><span data-ttu-id="e0836-109">Beschreibung der Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="e0836-109">Prerequisite description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e0836-110">Windows8.1</span><span class="sxs-lookup"><span data-stu-id="e0836-110">Windows 8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="e0836-111">Alle erforderliche Software ist bereits installiert.</span><span class="sxs-lookup"><span data-stu-id="e0836-111">All of the prerequisite software is already installed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e0836-112">Windows 8</span><span class="sxs-lookup"><span data-stu-id="e0836-112">Windows 8</span></span></p>
<p><span data-ttu-id="e0836-113">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e0836-113">Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="e0836-114">Die folgende erforderliche Software ist bereits installiert:</span><span class="sxs-lookup"><span data-stu-id="e0836-114">The following prerequisite software is already installed:</span></span></p>
<ul>
<li><p><span data-ttu-id="e0836-115">Microsoft .NET Framework 4,5</span><span class="sxs-lookup"><span data-stu-id="e0836-115">Microsoft .NET Framework 4.5</span></span></p></li>
<li><p><span data-ttu-id="e0836-116">Windows PowerShell 3,0</span><span class="sxs-lookup"><span data-stu-id="e0836-116">Windows PowerShell 3.0</span></span></p>
<div class="alert">
<strong><span data-ttu-id="e0836-117">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="e0836-117">Note</span></span></strong><br/><p><span data-ttu-id="e0836-118">Für die Installation von PowerShell 3,0 ist ein Neustart erforderlich.</span><span class="sxs-lookup"><span data-stu-id="e0836-118">Installing PowerShell 3.0 requires a restart.</span></span></p>
</div>
<div>

</div></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e0836-119">Windows7</span><span class="sxs-lookup"><span data-stu-id="e0836-119">Windows 7</span></span></p></td>
<td align="left"><p><span data-ttu-id="e0836-120">Die erforderliche Software ist noch nicht installiert.</span><span class="sxs-lookup"><span data-stu-id="e0836-120">The prerequisite software is not already installed.</span></span> <span data-ttu-id="e0836-121">Sie müssen es installieren, bevor Sie App-V installieren können.</span><span class="sxs-lookup"><span data-stu-id="e0836-121">You must install it before you can install App-V.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="e0836-122">App-V Server-Voraussetzungs Software</span><span class="sxs-lookup"><span data-stu-id="e0836-122">App-V Server prerequisite software</span></span>


<span data-ttu-id="e0836-123">Installieren Sie die erforderliche erforderliche Software für die App-V 5,0 SP3-Server Komponenten.</span><span class="sxs-lookup"><span data-stu-id="e0836-123">Install the required prerequisite software for the App-V 5.0 SP3 Server components.</span></span>

### <span data-ttu-id="e0836-124">Was Sie wissen sollten, bevor Sie beginnen</span><span class="sxs-lookup"><span data-stu-id="e0836-124">What to know before you start</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e0836-125">Konto für die Installation des App-V-Servers</span><span class="sxs-lookup"><span data-stu-id="e0836-125">Account for installing the App-V Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="e0836-126">Das Konto, das Sie zum Installieren der App-V Server-Komponenten verwenden, muss Folgendes aufweisen:</span><span class="sxs-lookup"><span data-stu-id="e0836-126">The account that you use to install the App-V Server components must have:</span></span></p>
<ul>
<li><p><span data-ttu-id="e0836-127">Administratorrechte auf dem Computer, auf dem Sie die Komponenten installieren.</span><span class="sxs-lookup"><span data-stu-id="e0836-127">Administrative rights on the computer on which you are installing the components.</span></span></p></li>
<li><p><span data-ttu-id="e0836-128">Die Möglichkeit, Active Directory-Domänendienste abzufragen.</span><span class="sxs-lookup"><span data-stu-id="e0836-128">The ability to query Active Directory Domain Services.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e0836-129">Port und Firewall</span><span class="sxs-lookup"><span data-stu-id="e0836-129">Port and firewall</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="e0836-130">Geben Sie einen Port an, in dem die einzelnen Komponenten gehostet werden.</span><span class="sxs-lookup"><span data-stu-id="e0836-130">Specify a port where each component will be hosted.</span></span></p></li>
<li><p><span data-ttu-id="e0836-131">Fügen Sie die zugehörigen Firewallregeln hinzu, um eingehende Anforderungen an die angegebenen Ports zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="e0836-131">Add the associated firewall rules to allow incoming requests to the specified ports.</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e0836-132">WebDAV (Web Distributed Authoring and Versioning)</span><span class="sxs-lookup"><span data-stu-id="e0836-132">Web Distributed Authoring and Versioning (WebDAV)</span></span></p></td>
<td align="left"><p><span data-ttu-id="e0836-133">WebDAV wird für den Verwaltungsdienst automatisch deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="e0836-133">WebDAV is automatically disabled for the Management Service.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e0836-134">Unterstützte Bereitstellungsszenarien</span><span class="sxs-lookup"><span data-stu-id="e0836-134">Supported deployment scenarios</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="e0836-135">Eine eigenständige Bereitstellung, in der alle Komponenten auf demselben Server bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="e0836-135">A stand-alone deployment, where all components are deployed on the same server.</span></span></p></li>
<li><p><span data-ttu-id="e0836-136">Eine verteilte Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="e0836-136">A distributed deployment.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e0836-137">Nicht unterstützte Bereitstellungsszenarien</span><span class="sxs-lookup"><span data-stu-id="e0836-137">Unsupported deployment scenarios</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="e0836-138">Installieren des App-v-Servers auf einem Computer, auf dem eine frühere Version oder Komponente von App-v ausgeführt wird</span><span class="sxs-lookup"><span data-stu-id="e0836-138">Installing the App-V Server on a computer that runs any previous version or component of App-V.</span></span></p></li>
<li><p><span data-ttu-id="e0836-139">Installieren der App-V Server-Komponenten auf einem Computer, auf dem Server Core oder Domänencontroller ausgeführt wird</span><span class="sxs-lookup"><span data-stu-id="e0836-139">Installing the App-V server components on a computer that runs server core or domain controller.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="e0836-140">Verwaltungsserver-Voraussetzungs Software</span><span class="sxs-lookup"><span data-stu-id="e0836-140">Management server prerequisite software</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="e0836-141">Voraussetzungen und erforderliche Einstellungen</span><span class="sxs-lookup"><span data-stu-id="e0836-141">Prerequisites and required settings</span></span></th>
<th align="left"><span data-ttu-id="e0836-142">Details</span><span class="sxs-lookup"><span data-stu-id="e0836-142">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e0836-143">Unterstützte Version von SQL Server</span><span class="sxs-lookup"><span data-stu-id="e0836-143">Supported version of SQL Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="e0836-144">Unterstützte Versionen finden Sie unter <a href="app-v-50-sp3-supported-configurations.md" data-raw-source="[App-V 5.0 SP3 Supported Configurations](app-v-50-sp3-supported-configurations.md)"> unterstützte Konfigurationen für App-V 5,0 SP3 </a> .</span><span class="sxs-lookup"><span data-stu-id="e0836-144">For supported versions, see <a href="app-v-50-sp3-supported-configurations.md" data-raw-source="[App-V 5.0 SP3 Supported Configurations](app-v-50-sp3-supported-configurations.md)">App-V 5.0 SP3 Supported Configurations</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="https://www.microsoft.com//download/details.aspx?id=40773" data-raw-source="[Microsoft .NET Framework 4.5.1 (Web Installer)](https://www.microsoft.com//download/details.aspx?id=40773)"><span data-ttu-id="e0836-145">Microsoft .NET Framework 4.5.1 (Web Installer)</span><span class="sxs-lookup"><span data-stu-id="e0836-145">Microsoft .NET Framework 4.5.1 (Web Installer)</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=34595" data-raw-source="[Windows PowerShell 3.0](https://www.microsoft.com/download/details.aspx?id=34595)"><span data-ttu-id="e0836-146">Windows PowerShell 3,0</span><span class="sxs-lookup"><span data-stu-id="e0836-146">Windows PowerShell 3.0</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="e0836-147">Für die Installation von PowerShell 3,0 ist ein Neustart erforderlich.</span><span class="sxs-lookup"><span data-stu-id="e0836-147">Installing PowerShell 3.0 requires a restart.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e0836-148">Herunterladen und Installieren von <a href="https://support.microsoft.com/kb/2533623" data-raw-source="[KB2533623](https://support.microsoft.com/kb/2533623)"> KB2533623</span><span class="sxs-lookup"><span data-stu-id="e0836-148">Download and install <a href="https://support.microsoft.com/kb/2533623" data-raw-source="[KB2533623](https://support.microsoft.com/kb/2533623)">KB2533623</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="e0836-149">Gilt nur für Windows 7.</span><span class="sxs-lookup"><span data-stu-id="e0836-149">Applies to Windows 7 only.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=40784" data-raw-source="[Visual C++ Redistributable Packages for Visual Studio 2013](https://www.microsoft.com/download/details.aspx?id=40784)"><span data-ttu-id="e0836-150">Visual C++-verteilbare Pakete für Visual Studio 2013</span><span class="sxs-lookup"><span data-stu-id="e0836-150">Visual C++ Redistributable Packages for Visual Studio 2013</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e0836-151">64-Bit ASP.net-Registrierung</span><span class="sxs-lookup"><span data-stu-id="e0836-151">64-bit ASP.NET registration</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e0836-152">Rolle des Windows Server-Webservers</span><span class="sxs-lookup"><span data-stu-id="e0836-152">Windows Server Web Server Role</span></span></p></td>
<td align="left"><p><span data-ttu-id="e0836-153">Diese Rolle muss einem Server Betriebssystem hinzugefügt werden, das für den Verwaltungsserver unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="e0836-153">This role must be added to a server operating system that is supported for the Management server.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e0836-154">Web Server (IIS)-Verwaltungs Tools</span><span class="sxs-lookup"><span data-stu-id="e0836-154">Web Server (IIS) Management Tools</span></span></p></td>
<td align="left"><p><span data-ttu-id="e0836-155">Klicken Sie auf <strong> IIS-Verwaltungsskripts und-Tools </strong> .</span><span class="sxs-lookup"><span data-stu-id="e0836-155">Click <strong>IIS Management Scripts and Tools</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e0836-156">Webserver-Rollendienste</span><span class="sxs-lookup"><span data-stu-id="e0836-156">Web Server Role Services</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="e0836-157">Allgemeine HTTP-Features:</span><span class="sxs-lookup"><span data-stu-id="e0836-157">Common HTTP Features:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="e0836-158">Statischer Inhalt</span><span class="sxs-lookup"><span data-stu-id="e0836-158">Static Content</span></span></p></li>
<li><p><span data-ttu-id="e0836-159">Standarddokument</span><span class="sxs-lookup"><span data-stu-id="e0836-159">Default Document</span></span></p></li>
</ul>
<p><strong><span data-ttu-id="e0836-160">Anwendungsentwicklung:</span><span class="sxs-lookup"><span data-stu-id="e0836-160">Application Development:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="e0836-161">ASP.NET</span><span class="sxs-lookup"><span data-stu-id="e0836-161">ASP.NET</span></span></p></li>
<li><p><span data-ttu-id="e0836-162">.NET-Erweiterbarkeit</span><span class="sxs-lookup"><span data-stu-id="e0836-162">.NET Extensibility</span></span></p></li>
<li><p><span data-ttu-id="e0836-163">ISAPI-Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="e0836-163">ISAPI Extensions</span></span></p></li>
<li><p><span data-ttu-id="e0836-164">ISAPI-Filter</span><span class="sxs-lookup"><span data-stu-id="e0836-164">ISAPI Filters</span></span></p></li>
</ul>
<p><strong><span data-ttu-id="e0836-165">Sicherheits</span><span class="sxs-lookup"><span data-stu-id="e0836-165">Security:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="e0836-166">Windows-Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="e0836-166">Windows Authentication</span></span></p></li>
<li><p><span data-ttu-id="e0836-167">Anforderungsfilterung</span><span class="sxs-lookup"><span data-stu-id="e0836-167">Request Filtering</span></span></p></li>
</ul>
<p><strong><span data-ttu-id="e0836-168">Verwaltungs Tools:</span><span class="sxs-lookup"><span data-stu-id="e0836-168">Management Tools:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="e0836-169">IIS-Verwaltungskonsole</span><span class="sxs-lookup"><span data-stu-id="e0836-169">IIS Management Console</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e0836-170">Standard Installationsspeicherort</span><span class="sxs-lookup"><span data-stu-id="e0836-170">Default installation location</span></span></p></td>
<td align="left"><p><span data-ttu-id="e0836-171">%ProgramFiles%\Microsoft Application Virtualization Server</span><span class="sxs-lookup"><span data-stu-id="e0836-171">%PROGRAMFILES%\Microsoft Application Virtualization Server</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e0836-172">Speicherort der Verwaltungsdatenbank</span><span class="sxs-lookup"><span data-stu-id="e0836-172">Location of the Management database</span></span></p></td>
<td align="left"><p><span data-ttu-id="e0836-173">SQL Server-Datenbankname, Name der SQL Server-Datenbankinstanz und Datenbankname</span><span class="sxs-lookup"><span data-stu-id="e0836-173">SQL Server database name, SQL Server database instance name, and database name.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e0836-174">Verwaltungskonsolen-und Verwaltungsdaten Bank Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="e0836-174">Management console and Management database permissions</span></span></p></td>
<td align="left"><p><span data-ttu-id="e0836-175">Ein Benutzer oder eine Gruppe, die nach Abschluss der Bereitstellung auf die Verwaltungskonsole und die Datenbank zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="e0836-175">A user or group that can access the Management console and database after the deployment is complete.</span></span> <span data-ttu-id="e0836-176">Nur diese Benutzer oder Gruppen haben Zugriff auf die Verwaltungskonsole und die Datenbank, es sei denn, mithilfe der Verwaltungskonsole werden zusätzliche Administratoren hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="e0836-176">Only these users or groups will have access to the Management console and database unless additional administrators are added by using the Management console.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e0836-177">Name der Verwaltungsdienst Website</span><span class="sxs-lookup"><span data-stu-id="e0836-177">Management service website name</span></span></p></td>
<td align="left"><p><span data-ttu-id="e0836-178">Name für die Verwaltungskonsole-Website.</span><span class="sxs-lookup"><span data-stu-id="e0836-178">Name for the Management console website.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e0836-179">Portbindung des Verwaltungsdiensts</span><span class="sxs-lookup"><span data-stu-id="e0836-179">Management service port binding</span></span></p></td>
<td align="left"><p><span data-ttu-id="e0836-180">Eindeutige Portnummer für den Verwaltungsdienst</span><span class="sxs-lookup"><span data-stu-id="e0836-180">Unique port number for the Management service.</span></span> <span data-ttu-id="e0836-181">Dieser Port kann nicht von einem anderen Prozess auf dem Computer verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e0836-181">This port cannot be used by another process on the computer.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e0836-182">Microsoft Silverlight 5</span><span class="sxs-lookup"><span data-stu-id="e0836-182">Microsoft Silverlight 5</span></span></p></td>
<td align="left"><p><span data-ttu-id="e0836-183">Die Verwaltungskonsole ist nur verfügbar, wenn Silverlight installiert ist.</span><span class="sxs-lookup"><span data-stu-id="e0836-183">The Management console is available only if Silverlight is installed.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="e0836-184">Erforderliche Software für die Verwaltungsserver-Datenbank</span><span class="sxs-lookup"><span data-stu-id="e0836-184">Management server database prerequisite software</span></span>

<span data-ttu-id="e0836-185">Die Verwaltungsdatenbank ist nur erforderlich, wenn Sie den App-V 5,0 SP3-Verwaltungsserver verwenden.</span><span class="sxs-lookup"><span data-stu-id="e0836-185">The Management database is required only if you are using the App-V 5.0 SP3 Management server.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="e0836-186">Voraussetzungen und erforderliche Einstellungen</span><span class="sxs-lookup"><span data-stu-id="e0836-186">Prerequisites and required settings</span></span></th>
<th align="left"><span data-ttu-id="e0836-187">Details</span><span class="sxs-lookup"><span data-stu-id="e0836-187">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="https://www.microsoft.com//download/details.aspx?id=40773" data-raw-source="[Microsoft .NET Framework 4.5.1 (Web Installer)](https://www.microsoft.com//download/details.aspx?id=40773)"><span data-ttu-id="e0836-188">Microsoft .NET Framework 4.5.1 (Web Installer)</span><span class="sxs-lookup"><span data-stu-id="e0836-188">Microsoft .NET Framework 4.5.1 (Web Installer)</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=40784" data-raw-source="[Visual C++ Redistributable Packages for Visual Studio 2013](https://www.microsoft.com/download/details.aspx?id=40784)"><span data-ttu-id="e0836-189">Visual C++-verteilbare Pakete für Visual Studio 2013</span><span class="sxs-lookup"><span data-stu-id="e0836-189">Visual C++ Redistributable Packages for Visual Studio 2013</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e0836-190">Standard Installationsspeicherort</span><span class="sxs-lookup"><span data-stu-id="e0836-190">Default installation location</span></span></p></td>
<td align="left"><p><span data-ttu-id="e0836-191">%ProgramFiles%\Microsoft Application Virtualization Server</span><span class="sxs-lookup"><span data-stu-id="e0836-191">%PROGRAMFILES%\Microsoft Application Virtualization Server</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e0836-192">Benutzerdefinierter SQL Server-Instanzname (falls zutreffend)</span><span class="sxs-lookup"><span data-stu-id="e0836-192">Custom SQL Server instance name (if applicable)</span></span></p></td>
<td align="left"><p><span data-ttu-id="e0836-193">Zu verwendender Format: <strong> instanceName</span><span class="sxs-lookup"><span data-stu-id="e0836-193">Format to use: <strong>INSTANCENAME</span></span></strong></p>
<p><span data-ttu-id="e0836-194">Dieses Format basiert auf der Annahme, dass sich die Installation auf dem lokalen Computer befindet.</span><span class="sxs-lookup"><span data-stu-id="e0836-194">This format is based on the assumption that the installation is on the local computer.</span></span></p>
<p><span data-ttu-id="e0836-195">Wenn Sie den Namen mit dem Format <strong> SVR\INSTANCE angeben </strong> , schlägt die Installation fehl.</span><span class="sxs-lookup"><span data-stu-id="e0836-195">If you specify the name with the format <strong>SVR\INSTANCE</strong>, the installation will fail.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e0836-196">Benutzerdefinierter Datenbankname (falls zutreffend)</span><span class="sxs-lookup"><span data-stu-id="e0836-196">Custom database name (if applicable)</span></span></p></td>
<td align="left"><p><span data-ttu-id="e0836-197">Eindeutiger Datenbankname</span><span class="sxs-lookup"><span data-stu-id="e0836-197">Unique database name.</span></span></p>
<p><span data-ttu-id="e0836-198">Standard: AppVManagement</span><span class="sxs-lookup"><span data-stu-id="e0836-198">Default: AppVManagement</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e0836-199">Verwaltungsserver Standort</span><span class="sxs-lookup"><span data-stu-id="e0836-199">Management server location</span></span></p></td>
<td align="left"><p><span data-ttu-id="e0836-200">Computerkonto, auf dem der Verwaltungsserver bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="e0836-200">Machine account on which the Management server is deployed.</span></span></p>
<p><span data-ttu-id="e0836-201">Zu verwendender Format: Domain\MachineAccount</span><span class="sxs-lookup"><span data-stu-id="e0836-201">Format to use: Domain\MachineAccount</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e0836-202">Verwaltungsserver-Installations Administrator</span><span class="sxs-lookup"><span data-stu-id="e0836-202">Management server installation administrator</span></span></p></td>
<td align="left"><p><span data-ttu-id="e0836-203">Konto, das zum Installieren des Verwaltungsservers verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e0836-203">Account used to install the Management server.</span></span></p>
<p><span data-ttu-id="e0836-204">Zu verwendender Format: Domain\AdministratorLoginName</span><span class="sxs-lookup"><span data-stu-id="e0836-204">Format to use: Domain\AdministratorLoginName</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e0836-205">Microsoft SQL Server-Dienst-Agent</span><span class="sxs-lookup"><span data-stu-id="e0836-205">Microsoft SQL Server Service Agent</span></span></p></td>
<td align="left"><p><span data-ttu-id="e0836-206">Konfigurieren Sie den Verwaltungsdaten Bank Computer so, dass der Microsoft SQL Server-Agent-Dienst automatisch neu gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="e0836-206">Configure the Management database computer so that the Microsoft SQL Server Agent service is restarted automatically.</span></span> <span data-ttu-id="e0836-207">Anweisungen hierzu finden Sie unter <a href="https://technet.microsoft.com/magazine/gg313742.aspx" data-raw-source="[Configure SQL Server Agent to Restart Services Automatically](https://technet.microsoft.com/magazine/gg313742.aspx)"> Konfigurieren des SQL Server-Agents, um Dienste automatisch neu zu starten </a> .</span><span class="sxs-lookup"><span data-stu-id="e0836-207">For instructions, see <a href="https://technet.microsoft.com/magazine/gg313742.aspx" data-raw-source="[Configure SQL Server Agent to Restart Services Automatically](https://technet.microsoft.com/magazine/gg313742.aspx)">Configure SQL Server Agent to Restart Services Automatically</a>.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="e0836-208">Erforderliche Software für Veröffentlichungsserver</span><span class="sxs-lookup"><span data-stu-id="e0836-208">Publishing server prerequisite software</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="e0836-209">Voraussetzungen und erforderliche Einstellungen</span><span class="sxs-lookup"><span data-stu-id="e0836-209">Prerequisites and required settings</span></span></th>
<th align="left"><span data-ttu-id="e0836-210">Details</span><span class="sxs-lookup"><span data-stu-id="e0836-210">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="https://www.microsoft.com//download/details.aspx?id=40773" data-raw-source="[Microsoft .NET Framework 4.5.1 (Web Installer)](https://www.microsoft.com//download/details.aspx?id=40773)"><span data-ttu-id="e0836-211">Microsoft .NET Framework 4.5.1 (Web Installer)</span><span class="sxs-lookup"><span data-stu-id="e0836-211">Microsoft .NET Framework 4.5.1 (Web Installer)</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=40784" data-raw-source="[Visual C++ Redistributable Packages for Visual Studio 2013](https://www.microsoft.com/download/details.aspx?id=40784)"><span data-ttu-id="e0836-212">Visual C++-verteilbare Pakete für Visual Studio 2013</span><span class="sxs-lookup"><span data-stu-id="e0836-212">Visual C++ Redistributable Packages for Visual Studio 2013</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e0836-213">64-Bit ASP.net-Registrierung</span><span class="sxs-lookup"><span data-stu-id="e0836-213">64-bit ASP.NET registration</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e0836-214">Rolle des Windows Server-Webservers</span><span class="sxs-lookup"><span data-stu-id="e0836-214">Windows Server Web Server Role</span></span></p></td>
<td align="left"><p><span data-ttu-id="e0836-215">Diese Rolle muss einem Server Betriebssystem hinzugefügt werden, das für den Verwaltungsserver unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="e0836-215">This role must be added to a server operating system that is supported for the Management server.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e0836-216">Web Server (IIS)-Verwaltungs Tools</span><span class="sxs-lookup"><span data-stu-id="e0836-216">Web Server (IIS) Management Tools</span></span></p></td>
<td align="left"><p><span data-ttu-id="e0836-217">Klicken Sie auf <strong> IIS-Verwaltungsskripts und-Tools </strong> .</span><span class="sxs-lookup"><span data-stu-id="e0836-217">Click <strong>IIS Management Scripts and Tools</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e0836-218">Webserver-Rollendienste</span><span class="sxs-lookup"><span data-stu-id="e0836-218">Web Server Role Services</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="e0836-219">Allgemeine HTTP-Features:</span><span class="sxs-lookup"><span data-stu-id="e0836-219">Common HTTP Features:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="e0836-220">Statischer Inhalt</span><span class="sxs-lookup"><span data-stu-id="e0836-220">Static Content</span></span></p></li>
<li><p><span data-ttu-id="e0836-221">Standarddokument</span><span class="sxs-lookup"><span data-stu-id="e0836-221">Default Document</span></span></p></li>
</ul>
<p><strong><span data-ttu-id="e0836-222">Anwendungsentwicklung:</span><span class="sxs-lookup"><span data-stu-id="e0836-222">Application Development:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="e0836-223">ASP.NET</span><span class="sxs-lookup"><span data-stu-id="e0836-223">ASP.NET</span></span></p></li>
<li><p><span data-ttu-id="e0836-224">.NET-Erweiterbarkeit</span><span class="sxs-lookup"><span data-stu-id="e0836-224">.NET Extensibility</span></span></p></li>
<li><p><span data-ttu-id="e0836-225">ISAPI-Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="e0836-225">ISAPI Extensions</span></span></p></li>
<li><p><span data-ttu-id="e0836-226">ISAPI-Filter</span><span class="sxs-lookup"><span data-stu-id="e0836-226">ISAPI Filters</span></span></p></li>
</ul>
<p><strong><span data-ttu-id="e0836-227">Sicherheits</span><span class="sxs-lookup"><span data-stu-id="e0836-227">Security:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="e0836-228">Windows-Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="e0836-228">Windows Authentication</span></span></p></li>
<li><p><span data-ttu-id="e0836-229">Anforderungsfilterung</span><span class="sxs-lookup"><span data-stu-id="e0836-229">Request Filtering</span></span></p></li>
</ul>
<p><strong><span data-ttu-id="e0836-230">Verwaltungs Tools:</span><span class="sxs-lookup"><span data-stu-id="e0836-230">Management Tools:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="e0836-231">IIS-Verwaltungskonsole</span><span class="sxs-lookup"><span data-stu-id="e0836-231">IIS Management Console</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e0836-232">Standard Installationsspeicherort</span><span class="sxs-lookup"><span data-stu-id="e0836-232">Default installation location</span></span></p></td>
<td align="left"><p><span data-ttu-id="e0836-233">%ProgramFiles%\Microsoft Application Virtualization Server</span><span class="sxs-lookup"><span data-stu-id="e0836-233">%PROGRAMFILES%\Microsoft Application Virtualization Server</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e0836-234">Verwaltungsdienst-URL</span><span class="sxs-lookup"><span data-stu-id="e0836-234">Management service URL</span></span></p></td>
<td align="left"><p><span data-ttu-id="e0836-235">Die URL des App-V-Verwaltungsdiensts.</span><span class="sxs-lookup"><span data-stu-id="e0836-235">URL of the App-V Management service.</span></span> <span data-ttu-id="e0836-236">Hierbei handelt es sich um den Port, mit dem der Veröffentlichungsserver kommuniziert.</span><span class="sxs-lookup"><span data-stu-id="e0836-236">This is the port with which the Publishing server communicates.</span></span></p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="e0836-237">Installations Architektur</span><span class="sxs-lookup"><span data-stu-id="e0836-237">Installation architecture</span></span></th>
<th align="left"><span data-ttu-id="e0836-238">Für die URL zu verwendende Format</span><span class="sxs-lookup"><span data-stu-id="e0836-238">Format to use for the URL</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e0836-239">Verwaltungsserver und Veröffentlichungsserver sind auf demselben Server installiert</span><span class="sxs-lookup"><span data-stu-id="e0836-239">Management server and Publishing server are installed on the same server</span></span></p></td>
<td align="left"><p><a href="http://localhost:12345" data-raw-source="http://localhost:12345">http://localhost:12345</a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e0836-240">Verwaltungsserver und Veröffentlichungsserver werden auf unterschiedlichen Servern installiert</span><span class="sxs-lookup"><span data-stu-id="e0836-240">Management server and Publishing server are installed on different servers</span></span></p></td>
<td align="left"><p><a href="http://MyAppvServer.MyDomain.com" data-raw-source="http://MyAppvServer.MyDomain.com">http://MyAppvServer.MyDomain.com</a></p></td>
</tr>
</tbody>
</table>
<p> </p>
<p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e0836-241">Name der Veröffentlichungsdienst Website</span><span class="sxs-lookup"><span data-stu-id="e0836-241">Publishing service website name</span></span></p></td>
<td align="left"><p><span data-ttu-id="e0836-242">Name für die Veröffentlichungswebsite.</span><span class="sxs-lookup"><span data-stu-id="e0836-242">Name for the Publishing website.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e0836-243">Portbindung des Publishing Diensts</span><span class="sxs-lookup"><span data-stu-id="e0836-243">Publishing service port binding</span></span></p></td>
<td align="left"><p><span data-ttu-id="e0836-244">Eindeutige Portnummer für den Veröffentlichungsdienst.</span><span class="sxs-lookup"><span data-stu-id="e0836-244">Unique port number for the Publishing service.</span></span> <span data-ttu-id="e0836-245">Dieser Port kann nicht von einem anderen Prozess auf dem Computer verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e0836-245">This port cannot be used by another process on the computer.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="e0836-246">Berichtsserver-Voraussetzungs Software</span><span class="sxs-lookup"><span data-stu-id="e0836-246">Reporting server prerequisite software</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="e0836-247">Voraussetzungen und erforderliche Einstellungen</span><span class="sxs-lookup"><span data-stu-id="e0836-247">Prerequisites and required settings</span></span></th>
<th align="left"><span data-ttu-id="e0836-248">Details</span><span class="sxs-lookup"><span data-stu-id="e0836-248">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e0836-249">Unterstützte Version von SQL Server</span><span class="sxs-lookup"><span data-stu-id="e0836-249">Supported version of SQL Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="e0836-250">Unterstützte Versionen finden Sie unter <a href="app-v-50-sp3-supported-configurations.md" data-raw-source="[App-V 5.0 SP3 Supported Configurations](app-v-50-sp3-supported-configurations.md)"> unterstützte Konfigurationen für App-V 5,0 SP3 </a> .</span><span class="sxs-lookup"><span data-stu-id="e0836-250">For supported versions, see <a href="app-v-50-sp3-supported-configurations.md" data-raw-source="[App-V 5.0 SP3 Supported Configurations](app-v-50-sp3-supported-configurations.md)">App-V 5.0 SP3 Supported Configurations</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="https://www.microsoft.com//download/details.aspx?id=40773" data-raw-source="[Microsoft .NET Framework 4.5.1 (Web Installer)](https://www.microsoft.com//download/details.aspx?id=40773)"><span data-ttu-id="e0836-251">Microsoft .NET Framework 4.5.1 (Web Installer)</span><span class="sxs-lookup"><span data-stu-id="e0836-251">Microsoft .NET Framework 4.5.1 (Web Installer)</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=40784" data-raw-source="[Visual C++ Redistributable Packages for Visual Studio 2013](https://www.microsoft.com/download/details.aspx?id=40784)"><span data-ttu-id="e0836-252">Visual C++-verteilbare Pakete für Visual Studio 2013</span><span class="sxs-lookup"><span data-stu-id="e0836-252">Visual C++ Redistributable Packages for Visual Studio 2013</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e0836-253">64-Bit ASP.net-Registrierung</span><span class="sxs-lookup"><span data-stu-id="e0836-253">64-bit ASP.NET registration</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e0836-254">Rolle des Windows Server-Webservers</span><span class="sxs-lookup"><span data-stu-id="e0836-254">Windows Server Web Server Role</span></span></p></td>
<td align="left"><p><span data-ttu-id="e0836-255">Diese Rolle muss einem Server Betriebssystem hinzugefügt werden, das für den Verwaltungsserver unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="e0836-255">This role must be added to a server operating system that is supported for the Management server.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e0836-256">Web Server (IIS)-Verwaltungs Tools</span><span class="sxs-lookup"><span data-stu-id="e0836-256">Web Server (IIS) Management Tools</span></span></p></td>
<td align="left"><p><span data-ttu-id="e0836-257">Klicken Sie auf <strong> IIS-Verwaltungsskripts und-Tools </strong> .</span><span class="sxs-lookup"><span data-stu-id="e0836-257">Click <strong>IIS Management Scripts and Tools</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e0836-258">Webserver-Rollendienste</span><span class="sxs-lookup"><span data-stu-id="e0836-258">Web Server Role Services</span></span></p></td>
<td align="left"><p><span data-ttu-id="e0836-259">Um das Risiko von unerwünschten oder böswilligen Daten, die an den Berichtsserver gesendet werden, zu verringern, sollten Sie den Zugriff auf den Reporting Web Service pro Ihre Unternehmenssicherheitsrichtlinie einschränken.</span><span class="sxs-lookup"><span data-stu-id="e0836-259">To reduce the risk of unwanted or malicious data being sent to the Reporting server, you should restrict access to the Reporting Web Service per your corporate security policy.</span></span></p>
<p><strong><span data-ttu-id="e0836-260">Allgemeine HTTP-Features:</span><span class="sxs-lookup"><span data-stu-id="e0836-260">Common HTTP Features:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="e0836-261">Statischer Inhalt</span><span class="sxs-lookup"><span data-stu-id="e0836-261">Static Content</span></span></p></li>
<li><p><span data-ttu-id="e0836-262">Standarddokument</span><span class="sxs-lookup"><span data-stu-id="e0836-262">Default Document</span></span></p></li>
</ul>
<p><strong><span data-ttu-id="e0836-263">Anwendungsentwicklung:</span><span class="sxs-lookup"><span data-stu-id="e0836-263">Application Development:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="e0836-264">ASP.NET</span><span class="sxs-lookup"><span data-stu-id="e0836-264">ASP.NET</span></span></p></li>
<li><p><span data-ttu-id="e0836-265">.NET-Erweiterbarkeit</span><span class="sxs-lookup"><span data-stu-id="e0836-265">.NET Extensibility</span></span></p></li>
<li><p><span data-ttu-id="e0836-266">ISAPI-Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="e0836-266">ISAPI Extensions</span></span></p></li>
<li><p><span data-ttu-id="e0836-267">ISAPI-Filter</span><span class="sxs-lookup"><span data-stu-id="e0836-267">ISAPI Filters</span></span></p></li>
</ul>
<p><strong><span data-ttu-id="e0836-268">Sicherheits</span><span class="sxs-lookup"><span data-stu-id="e0836-268">Security:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="e0836-269">Windows-Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="e0836-269">Windows Authentication</span></span></p></li>
<li><p><span data-ttu-id="e0836-270">Anforderungsfilterung</span><span class="sxs-lookup"><span data-stu-id="e0836-270">Request Filtering</span></span></p></li>
</ul>
<p><strong><span data-ttu-id="e0836-271">Verwaltungs Tools:</span><span class="sxs-lookup"><span data-stu-id="e0836-271">Management Tools:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="e0836-272">IIS-Verwaltungskonsole</span><span class="sxs-lookup"><span data-stu-id="e0836-272">IIS Management Console</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e0836-273">Standard Installationsspeicherort</span><span class="sxs-lookup"><span data-stu-id="e0836-273">Default installation location</span></span></p></td>
<td align="left"><p><span data-ttu-id="e0836-274">%ProgramFiles%\Microsoft Application Virtualization Server</span><span class="sxs-lookup"><span data-stu-id="e0836-274">%PROGRAMFILES%\Microsoft Application Virtualization Server</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e0836-275">Name der Berichtsdienst Website</span><span class="sxs-lookup"><span data-stu-id="e0836-275">Reporting service website name</span></span></p></td>
<td align="left"><p><span data-ttu-id="e0836-276">Name für die berichterstellungswebsite.</span><span class="sxs-lookup"><span data-stu-id="e0836-276">Name for the Reporting website.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e0836-277">Portbindung des Reporting Services</span><span class="sxs-lookup"><span data-stu-id="e0836-277">Reporting service port binding</span></span></p></td>
<td align="left"><p><span data-ttu-id="e0836-278">Eindeutige Portnummer für den Berichterstellungsdienst.</span><span class="sxs-lookup"><span data-stu-id="e0836-278">Unique port number for the Reporting service.</span></span> <span data-ttu-id="e0836-279">Dieser Port kann nicht von einem anderen Prozess auf dem Computer verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e0836-279">This port cannot be used by another process on the computer.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="e0836-280">Erforderliche Software für die Berichtsdatenbank</span><span class="sxs-lookup"><span data-stu-id="e0836-280">Reporting database prerequisite software</span></span>

<span data-ttu-id="e0836-281">Die Berichtsdatenbank ist nur erforderlich, wenn Sie den App-V 5,0 SP3-Berichtsserver verwenden.</span><span class="sxs-lookup"><span data-stu-id="e0836-281">The Reporting database is required only if you are using the App-V 5.0 SP3 Reporting server.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="e0836-282">Voraussetzungen und erforderliche Einstellungen</span><span class="sxs-lookup"><span data-stu-id="e0836-282">Prerequisites and required settings</span></span></th>
<th align="left"><span data-ttu-id="e0836-283">Details</span><span class="sxs-lookup"><span data-stu-id="e0836-283">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="https://www.microsoft.com//download/details.aspx?id=40773" data-raw-source="[Microsoft .NET Framework 4.5.1 (Web Installer)](https://www.microsoft.com//download/details.aspx?id=40773)"><span data-ttu-id="e0836-284">Microsoft .NET Framework 4.5.1 (Web Installer)</span><span class="sxs-lookup"><span data-stu-id="e0836-284">Microsoft .NET Framework 4.5.1 (Web Installer)</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=40784" data-raw-source="[Visual C++ Redistributable Packages for Visual Studio 2013](https://www.microsoft.com/download/details.aspx?id=40784)"><span data-ttu-id="e0836-285">Visual C++-verteilbare Pakete für Visual Studio 2013</span><span class="sxs-lookup"><span data-stu-id="e0836-285">Visual C++ Redistributable Packages for Visual Studio 2013</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e0836-286">Standard Installationsspeicherort</span><span class="sxs-lookup"><span data-stu-id="e0836-286">Default installation location</span></span></p></td>
<td align="left"><p><span data-ttu-id="e0836-287">%ProgramFiles%\Microsoft Application Virtualization Server</span><span class="sxs-lookup"><span data-stu-id="e0836-287">%PROGRAMFILES%\Microsoft Application Virtualization Server</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e0836-288">Benutzerdefinierter SQL Server-Instanzname (falls zutreffend)</span><span class="sxs-lookup"><span data-stu-id="e0836-288">Custom SQL Server instance name (if applicable)</span></span></p></td>
<td align="left"><p><span data-ttu-id="e0836-289">Zu verwendender Format: <strong> instanceName</span><span class="sxs-lookup"><span data-stu-id="e0836-289">Format to use: <strong>INSTANCENAME</span></span></strong></p>
<p><span data-ttu-id="e0836-290">Dieses Format basiert auf der Annahme, dass sich die Installation auf dem lokalen Computer befindet.</span><span class="sxs-lookup"><span data-stu-id="e0836-290">This format is based on the assumption that the installation is on the local computer.</span></span></p>
<p><span data-ttu-id="e0836-291">Wenn Sie den Namen mit dem Format <strong> SVR\INSTANCE angeben </strong> , schlägt die Installation fehl.</span><span class="sxs-lookup"><span data-stu-id="e0836-291">If you specify the name with the format <strong>SVR\INSTANCE</strong>, the installation will fail.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e0836-292">Benutzerdefinierter Datenbankname (falls zutreffend)</span><span class="sxs-lookup"><span data-stu-id="e0836-292">Custom database name (if applicable)</span></span></p></td>
<td align="left"><p><span data-ttu-id="e0836-293">Eindeutiger Datenbankname</span><span class="sxs-lookup"><span data-stu-id="e0836-293">Unique database name.</span></span></p>
<p><span data-ttu-id="e0836-294">Standard: AppVReporting</span><span class="sxs-lookup"><span data-stu-id="e0836-294">Default: AppVReporting</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e0836-295">Speicherort des Berichterstattungs Servers</span><span class="sxs-lookup"><span data-stu-id="e0836-295">Reporting server location</span></span></p></td>
<td align="left"><p><span data-ttu-id="e0836-296">Computerkonto, auf dem der Berichtsserver bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="e0836-296">Machine account on which the Reporting server is deployed.</span></span></p>
<p><span data-ttu-id="e0836-297">Zu verwendender Format: Domain\MachineAccount</span><span class="sxs-lookup"><span data-stu-id="e0836-297">Format to use: Domain\MachineAccount</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e0836-298">Reporting Server-Installations Administrator</span><span class="sxs-lookup"><span data-stu-id="e0836-298">Reporting server installation administrator</span></span></p></td>
<td align="left"><p><span data-ttu-id="e0836-299">Konto, das zum Installieren des Berichtsservers verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e0836-299">Account used to install the Reporting server.</span></span></p>
<p><span data-ttu-id="e0836-300">Zu verwendender Format: Domain\AdministratorLoginName</span><span class="sxs-lookup"><span data-stu-id="e0836-300">Format to use: Domain\AdministratorLoginName</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e0836-301">Microsoft SQL Server-Dienst und Microsoft SQL Server-Dienst-Agent</span><span class="sxs-lookup"><span data-stu-id="e0836-301">Microsoft SQL Server Service and Microsoft SQL Server Service Agent</span></span></p></td>
<td align="left"><p><span data-ttu-id="e0836-302">Konfigurieren Sie diese Dienste für die Zuordnung zu Benutzerkonten, die Zugriff auf die Abfrage von AD DS haben.</span><span class="sxs-lookup"><span data-stu-id="e0836-302">Configure these services to be associated with user accounts that have access to query AD DS.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="e0836-303">App-V-Client-Voraussetzungs Software</span><span class="sxs-lookup"><span data-stu-id="e0836-303">App-V client prerequisite software</span></span>


<span data-ttu-id="e0836-304">Installieren Sie die folgende erforderliche Software für den App-V-Client.</span><span class="sxs-lookup"><span data-stu-id="e0836-304">Install the following prerequisite software for the App-V client.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="e0836-305">Voraussetzung</span><span class="sxs-lookup"><span data-stu-id="e0836-305">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="e0836-306">Details</span><span class="sxs-lookup"><span data-stu-id="e0836-306">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="https://www.microsoft.com//download/details.aspx?id=40773" data-raw-source="[Microsoft .NET Framework 4.5.1 (Web Installer)](https://www.microsoft.com//download/details.aspx?id=40773)"><span data-ttu-id="e0836-307">Microsoft .NET Framework 4.5.1 (Web Installer)</span><span class="sxs-lookup"><span data-stu-id="e0836-307">Microsoft .NET Framework 4.5.1 (Web Installer)</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=34595" data-raw-source="[Windows PowerShell 3.0](https://www.microsoft.com/download/details.aspx?id=34595)"><span data-ttu-id="e0836-308">Windows PowerShell 3,0</span><span class="sxs-lookup"><span data-stu-id="e0836-308">Windows PowerShell 3.0</span></span></a></p>
<p></p></td>
<td align="left"><p><span data-ttu-id="e0836-309">Für die Installation von PowerShell 3,0 ist ein Neustart erforderlich.</span><span class="sxs-lookup"><span data-stu-id="e0836-309">Installing PowerShell 3.0 requires a restart.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><a href="https://support.microsoft.com/kb/2533623" data-raw-source="[KB2533623](https://support.microsoft.com/kb/2533623)"><span data-ttu-id="e0836-310">KB2533623</span><span class="sxs-lookup"><span data-stu-id="e0836-310">KB2533623</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="e0836-311">Gilt nur für Windows 7: Laden Sie die KB herunter, und installieren Sie Sie.</span><span class="sxs-lookup"><span data-stu-id="e0836-311">Applies to Windows 7 only: Download and install the KB.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=40784" data-raw-source="[Visual C++ Redistributable Packages for Visual Studio 2013](https://www.microsoft.com/download/details.aspx?id=40784)"><span data-ttu-id="e0836-312">Visual C++-verteilbare Pakete für Visual Studio 2013</span><span class="sxs-lookup"><span data-stu-id="e0836-312">Visual C++ Redistributable Packages for Visual Studio 2013</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="e0836-313">Erforderliche Software für Remote Desktop Dienste-Client</span><span class="sxs-lookup"><span data-stu-id="e0836-313">Remote Desktop Services client prerequisite software</span></span>


<span data-ttu-id="e0836-314">Installieren Sie die folgende erforderliche Software für den App-V-Remote Desktop Dienste-Client.</span><span class="sxs-lookup"><span data-stu-id="e0836-314">Install the following prerequisite software for the App-V Remote Desktop Services client.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="e0836-315">Voraussetzung</span><span class="sxs-lookup"><span data-stu-id="e0836-315">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="e0836-316">Details</span><span class="sxs-lookup"><span data-stu-id="e0836-316">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="https://www.microsoft.com//download/details.aspx?id=40773" data-raw-source="[Microsoft .NET Framework 4.5.1 (Web Installer)](https://www.microsoft.com//download/details.aspx?id=40773)"><span data-ttu-id="e0836-317">Microsoft .NET Framework 4.5.1 (Web Installer)</span><span class="sxs-lookup"><span data-stu-id="e0836-317">Microsoft .NET Framework 4.5.1 (Web Installer)</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=34595" data-raw-source="[Windows PowerShell 3.0](https://www.microsoft.com/download/details.aspx?id=34595)"><span data-ttu-id="e0836-318">Windows PowerShell 3,0</span><span class="sxs-lookup"><span data-stu-id="e0836-318">Windows PowerShell 3.0</span></span></a></p>
<p></p></td>
<td align="left"><p><span data-ttu-id="e0836-319">Für die Installation von PowerShell 3,0 ist ein Neustart erforderlich.</span><span class="sxs-lookup"><span data-stu-id="e0836-319">Installing PowerShell 3.0 requires a restart.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><a href="https://support.microsoft.com/kb/2533623" data-raw-source="[KB2533623](https://support.microsoft.com/kb/2533623)"><span data-ttu-id="e0836-320">KB2533623</span><span class="sxs-lookup"><span data-stu-id="e0836-320">KB2533623</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="e0836-321">Gilt nur für Windows 7: Laden Sie die KB herunter, und installieren Sie Sie.</span><span class="sxs-lookup"><span data-stu-id="e0836-321">Applies to Windows 7 only: Download and install the KB.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=40784" data-raw-source="[Visual C++ Redistributable Packages for Visual Studio 2013](https://www.microsoft.com/download/details.aspx?id=40784)"><span data-ttu-id="e0836-322">Visual C++-verteilbare Pakete für Visual Studio 2013</span><span class="sxs-lookup"><span data-stu-id="e0836-322">Visual C++ Redistributable Packages for Visual Studio 2013</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="e0836-323">Sequenzer-Voraussetzungs Software</span><span class="sxs-lookup"><span data-stu-id="e0836-323">Sequencer prerequisite software</span></span>


**<span data-ttu-id="e0836-324">Was Sie wissen müssen, bevor Sie die Voraussetzungen installieren:</span><span class="sxs-lookup"><span data-stu-id="e0836-324">What to know before installing the prerequisites:</span></span>**

-   <span data-ttu-id="e0836-325">Bewährte Methode: der Computer, auf dem der Sequencer ausgeführt wird, sollte die gleichen Hardware-und Softwarekonfigurationen wie die Computer aufweisen, auf denen die virtuellen Anwendungen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="e0836-325">Best practice: The computer that runs the Sequencer should have the same hardware and software configurations as the computers that will run the virtual applications.</span></span>

-   <span data-ttu-id="e0836-326">Der Sequenzierungsprozess ist ressourcenintensiv, stellen Sie daher sicher, dass der Computer, auf dem der Sequencer ausgeführt wird, genügend Arbeitsspeicher, einen schnellen Prozessor und eine schnelle Festplatte aufweist.</span><span class="sxs-lookup"><span data-stu-id="e0836-326">The sequencing process is resource intensive, so make sure that the computer that runs the Sequencer has plenty of memory, a fast processor, and a fast hard drive.</span></span> <span data-ttu-id="e0836-327">Die Systemanforderungen von lokal installierten Anwendungen dürfen die des Sequencers nicht überschreiten.</span><span class="sxs-lookup"><span data-stu-id="e0836-327">The system requirements of locally installed applications cannot exceed those of the Sequencer.</span></span> <span data-ttu-id="e0836-328">Weitere Informationen finden Sie unter [unterstützte App-V 5,0-Konfigurationen](app-v-50-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="e0836-328">For more information, see [App-V 5.0 Supported Configurations](app-v-50-supported-configurations.md).</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="e0836-329">Voraussetzung</span><span class="sxs-lookup"><span data-stu-id="e0836-329">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="e0836-330">Details</span><span class="sxs-lookup"><span data-stu-id="e0836-330">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="https://www.microsoft.com//download/details.aspx?id=40773" data-raw-source="[Microsoft .NET Framework 4.5.1 (Web Installer)](https://www.microsoft.com//download/details.aspx?id=40773)"><span data-ttu-id="e0836-331">Microsoft .NET Framework 4.5.1 (Web Installer)</span><span class="sxs-lookup"><span data-stu-id="e0836-331">Microsoft .NET Framework 4.5.1 (Web Installer)</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=34595" data-raw-source="[Windows PowerShell 3.0](https://www.microsoft.com/download/details.aspx?id=34595)"><span data-ttu-id="e0836-332">Windows PowerShell 3,0</span><span class="sxs-lookup"><span data-stu-id="e0836-332">Windows PowerShell 3.0</span></span></a></p>
<p></p></td>
<td align="left"><p><span data-ttu-id="e0836-333">Für die Installation von PowerShell 3,0 ist ein Neustart erforderlich.</span><span class="sxs-lookup"><span data-stu-id="e0836-333">Installing PowerShell 3.0 requires a restart.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><a href="https://support.microsoft.com/kb/2533623" data-raw-source="[KB2533623](https://support.microsoft.com/kb/2533623)"><span data-ttu-id="e0836-334">KB2533623</span><span class="sxs-lookup"><span data-stu-id="e0836-334">KB2533623</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="e0836-335">Gilt nur für Windows 7: Laden Sie die KB herunter, und installieren Sie Sie.</span><span class="sxs-lookup"><span data-stu-id="e0836-335">Applies to Windows 7 only: Download and install the KB.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=40784" data-raw-source="[Visual C++ Redistributable Packages for Visual Studio 2013](https://www.microsoft.com/download/details.aspx?id=40784)"><span data-ttu-id="e0836-336">Visual C++-verteilbare Pakete für Visual Studio 2013</span><span class="sxs-lookup"><span data-stu-id="e0836-336">Visual C++ Redistributable Packages for Visual Studio 2013</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>








## <span data-ttu-id="e0836-337">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="e0836-337">Related topics</span></span>


[<span data-ttu-id="e0836-338">Planen für App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="e0836-338">Planning for App-V 5.0</span></span>](planning-for-app-v-50-rc.md)

[<span data-ttu-id="e0836-339">Unterstützte App-V 5.0 SP3-Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="e0836-339">App-V 5.0 SP3 Supported Configurations</span></span>](app-v-50-sp3-supported-configurations.md)









