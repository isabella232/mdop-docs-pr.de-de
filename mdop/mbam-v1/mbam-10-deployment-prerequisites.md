---
title: Bereitstellungsvoraussetzungen für MBAM 1.0
description: Bereitstellungsvoraussetzungen für MBAM 1.0
author: dansimp
ms.assetid: bd9e1010-7d25-43e7-8dc6-b521226a659d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6ed14343d37a859364bcabbe6ca72c041502a23c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809490"
---
# <span data-ttu-id="a94c3-103">Bereitstellungsvoraussetzungen für MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="a94c3-103">MBAM 1.0 Deployment Prerequisites</span></span>


<span data-ttu-id="a94c3-104">Bevor Sie mit dem Setup für die Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) beginnen, stellen Sie sicher, dass Sie die erforderlichen Voraussetzungen für die Installation des Produkts erfüllen.</span><span class="sxs-lookup"><span data-stu-id="a94c3-104">Before you begin the Microsoft BitLocker Administration and Monitoring (MBAM) Setup, make sure that you meet the necessary prerequisites to install the product.</span></span> <span data-ttu-id="a94c3-105">Dieser Abschnitt enthält Informationen, die Sie beim erfolgreichen Vorbereiten Ihrer Computerumgebung unterstützen, bevor Sie die MBAM-Clients und Server Features bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="a94c3-105">This section contains information to help you successfully prepare your computing environment before you deploy the MBAM Clients and Server features.</span></span>

## <span data-ttu-id="a94c3-106">Voraussetzungen für die Installation von MBAM Server Features</span><span class="sxs-lookup"><span data-stu-id="a94c3-106">Installation prerequisites for MBAM Server features</span></span>


<span data-ttu-id="a94c3-107">Für jedes der MBAM-Server Features gelten bestimmte Voraussetzungen, die erfüllt sein müssen, bevor Sie erfolgreich installiert werden können.</span><span class="sxs-lookup"><span data-stu-id="a94c3-107">Each of the MBAM server features has specific prerequisites that must be met before they can be successfully installed.</span></span> <span data-ttu-id="a94c3-108">MBAM-Setup überprüft, ob alle Voraussetzungen erfüllt sind, bevor die Installation gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="a94c3-108">MBAM Setup verifies if all prerequisites are met before the installation starts.</span></span>

### <span data-ttu-id="a94c3-109">Voraussetzungen für die Installation von Administration und Monitoring Server</span><span class="sxs-lookup"><span data-stu-id="a94c3-109">Installation prerequisites for Administration and Monitoring Server</span></span>

<span data-ttu-id="a94c3-110">Die folgende Tabelle enthält die Voraussetzungen für die Installation des MBAM-Verwaltungs-und-Überwachungsservers:</span><span class="sxs-lookup"><span data-stu-id="a94c3-110">The following table contains the installation prerequisites for the MBAM Administration and Monitoring Server:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="a94c3-111">Voraussetzung</span><span class="sxs-lookup"><span data-stu-id="a94c3-111">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="a94c3-112">Details</span><span class="sxs-lookup"><span data-stu-id="a94c3-112">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="a94c3-113">Windows ServerWeb-Server Rolle</span><span class="sxs-lookup"><span data-stu-id="a94c3-113">Windows ServerWeb Server Role</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="a94c3-114">Diese Rolle muss einem Server Betriebssystem hinzugefügt werden, das für das mbam-Verwaltungs-und Überwachungsserver Feature unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="a94c3-114">This role must be added to a server operating system supported for the mbam Administration and Monitoring Server feature.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="a94c3-115">Web Server (IIS)-Verwaltungs Tools</span><span class="sxs-lookup"><span data-stu-id="a94c3-115">Web Server (IIS) Management Tools</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="a94c3-116">IIS-Verwaltungsskripts und-Tools</span><span class="sxs-lookup"><span data-stu-id="a94c3-116">IIS Management Scripts and Tools</span></span></strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="a94c3-117">Webserver-Rollendienste</span><span class="sxs-lookup"><span data-stu-id="a94c3-117">Web Server Role Services</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="a94c3-118">Allgemeine HTTP-Features:</span><span class="sxs-lookup"><span data-stu-id="a94c3-118">Common HTTP Features:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="a94c3-119">Statischer Inhalt</span><span class="sxs-lookup"><span data-stu-id="a94c3-119">Static Content</span></span></p></li>
<li><p><span data-ttu-id="a94c3-120">Standarddokument</span><span class="sxs-lookup"><span data-stu-id="a94c3-120">Default Document</span></span></p></li>
</ul>
<p><strong><span data-ttu-id="a94c3-121">Anwendungsentwicklung:</span><span class="sxs-lookup"><span data-stu-id="a94c3-121">Application Development:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="a94c3-122">ASP.NET</span><span class="sxs-lookup"><span data-stu-id="a94c3-122">ASP.NET</span></span></p></li>
<li><p><span data-ttu-id="a94c3-123">.NET-Erweiterbarkeit</span><span class="sxs-lookup"><span data-stu-id="a94c3-123">.NET Extensibility</span></span></p></li>
<li><p><span data-ttu-id="a94c3-124">ISAPI-Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="a94c3-124">ISAPI Extensions</span></span></p></li>
<li><p><span data-ttu-id="a94c3-125">ISAPI-Filter</span><span class="sxs-lookup"><span data-stu-id="a94c3-125">ISAPI Filters</span></span></p></li>
</ul>
<p><strong><span data-ttu-id="a94c3-126">Sicherheits</span><span class="sxs-lookup"><span data-stu-id="a94c3-126">Security:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="a94c3-127">Windows-Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="a94c3-127">Windows Authentication</span></span></p></li>
<li><p><span data-ttu-id="a94c3-128">Anforderungsfilterung</span><span class="sxs-lookup"><span data-stu-id="a94c3-128">Request Filtering</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="a94c3-129">Windows Server-Features</span><span class="sxs-lookup"><span data-stu-id="a94c3-129">Windows Server Features</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="a94c3-130">Features von Microsoft .NET Framework 3.5.1:</span><span class="sxs-lookup"><span data-stu-id="a94c3-130">Microsoft .NET Framework 3.5.1 features:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="a94c3-131">.NET Framework 3.5.1</span><span class="sxs-lookup"><span data-stu-id="a94c3-131">.NET Framework 3.5.1</span></span></p></li>
<li><p><span data-ttu-id="a94c3-132">WCF-Aktivierung</span><span class="sxs-lookup"><span data-stu-id="a94c3-132">WCF Activation</span></span></p>
<ul>
<li><p><span data-ttu-id="a94c3-133">HTTP-Aktivierung</span><span class="sxs-lookup"><span data-stu-id="a94c3-133">HTTP Activation</span></span></p></li>
<li><p><span data-ttu-id="a94c3-134">Nicht-HTTP-Aktivierung</span><span class="sxs-lookup"><span data-stu-id="a94c3-134">Non-HTTP Activation</span></span></p></li>
</ul></li>
</ul>
<p><strong><span data-ttu-id="a94c3-135">Windows-Prozessaktivierungsdienst</span><span class="sxs-lookup"><span data-stu-id="a94c3-135">Windows Process Activation Service</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="a94c3-136">Prozessmodell</span><span class="sxs-lookup"><span data-stu-id="a94c3-136">Process Model</span></span></p></li>
<li><p><span data-ttu-id="a94c3-137">.NET-Umgebung</span><span class="sxs-lookup"><span data-stu-id="a94c3-137">.NET Environment</span></span></p></li>
<li><p><span data-ttu-id="a94c3-138">Konfigurations-APIs</span><span class="sxs-lookup"><span data-stu-id="a94c3-138">Configuration APIs</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="a94c3-139">**Hinweis**  Eine Liste der unterstützten Betriebssysteme finden Sie unter [unterstützte MBAM 1,0-Konfigurationen](mbam-10-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="a94c3-139">**Note** For a list of supported operating systems, see [MBAM 1.0 Supported Configurations](mbam-10-supported-configurations.md).</span></span>

 

### <span data-ttu-id="a94c3-140">Installationsvoraussetzungen für Konformitäts-und Überwachungsberichte</span><span class="sxs-lookup"><span data-stu-id="a94c3-140">Installation prerequisites for the Compliance and Audit Reports</span></span>

<span data-ttu-id="a94c3-141">Die Konformitäts-und Überwachungsberichte müssen auf einer unterstützten Version von SQLServer installiert sein.</span><span class="sxs-lookup"><span data-stu-id="a94c3-141">The Compliance and Audit Reports must be installed on a supported version of SQLServer.</span></span> <span data-ttu-id="a94c3-142">Zu den Installationsvoraussetzungen für dieses Feature gehören SQL Server Reporting Services (SSRS).</span><span class="sxs-lookup"><span data-stu-id="a94c3-142">Installation prerequisites for this feature include SQL Server Reporting Services (SSRS).</span></span>

<span data-ttu-id="a94c3-143">SSRS muss während der Installation von MBAM Server installiert sein und ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="a94c3-143">SSRS must be installed and running during MBAM server installation.</span></span> <span data-ttu-id="a94c3-144">SSRS sollte auch im systemeigenen Modus konfiguriert werden, nicht im Modus "nicht konfiguriert" oder "SharePoint".</span><span class="sxs-lookup"><span data-stu-id="a94c3-144">SSRS should also be configured in “native” mode, not in the “unconfigured” or “SharePoint” mode.</span></span>

<span data-ttu-id="a94c3-145">**Hinweis**  Eine Liste der unterstützten Betriebssysteme und SQLServer-Versionen finden Sie unter [unterstützte MBAM 1,0-Konfigurationen](mbam-10-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="a94c3-145">**Note** For a list of supported operating systems and SQLServer versions, see [MBAM 1.0 Supported Configurations](mbam-10-supported-configurations.md).</span></span>

 

### <span data-ttu-id="a94c3-146">Voraussetzungen für die Installation der Wiederherstellungs-und Hardware Datenbank</span><span class="sxs-lookup"><span data-stu-id="a94c3-146">Installation prerequisites for the Recovery and Hardware Database</span></span>

<span data-ttu-id="a94c3-147">Die Wiederherstellungs-und Hardware Datenbank muss in einer unterstützten Version von SQLServer installiert sein.</span><span class="sxs-lookup"><span data-stu-id="a94c3-147">The Recovery and Hardware Database must be installed on a supported version of SQLServer.</span></span>

<span data-ttu-id="a94c3-148">SQL Server muss während der Installation von MBAM Server Datenbankmoduldienste installiert haben und ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="a94c3-148">SQL Server must have Database Engine Services installed and running during the MBAM server installation.</span></span> <span data-ttu-id="a94c3-149">Das Feature "transparente Datenverschlüsselung" (DSA) muss aktiviert sein.</span><span class="sxs-lookup"><span data-stu-id="a94c3-149">The Transparent Data Encryption (TDE) feature must be enabled.</span></span>

<span data-ttu-id="a94c3-150">**Hinweis**  Eine Liste der unterstützten Betriebssysteme und SQLServer-Versionen finden Sie unter [unterstützte MBAM 1,0-Konfigurationen](mbam-10-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="a94c3-150">**Note** For a list of supported operating systems and SQLServer versions, see [MBAM 1.0 Supported Configurations](mbam-10-supported-configurations.md).</span></span>

 

<span data-ttu-id="a94c3-151">Das Feature "DSA SQLServer" führt eine e/a-Verschlüsselung und-Entschlüsselung der Daten-und Protokolldateien in Echtzeit durch.</span><span class="sxs-lookup"><span data-stu-id="a94c3-151">The TDE SQLServer feature performs real-time input/output (I/O) encryption and decryption of the data and log files.</span></span> <span data-ttu-id="a94c3-152">DSA schützt Daten, die "in Ruhe" sind, die die Daten und die Protokolldateien enthalten.</span><span class="sxs-lookup"><span data-stu-id="a94c3-152">TDE protects data that is "at rest,” which include the data and the log files.</span></span> <span data-ttu-id="a94c3-153">Sie bietet die Möglichkeit, viele Gesetze, Vorschriften und Richtlinien zu erfüllen, die in verschiedenen Branchen etabliert sind.</span><span class="sxs-lookup"><span data-stu-id="a94c3-153">It provides the ability to comply with many laws, regulations, and guidelines that are established in various industries.</span></span>

<span data-ttu-id="a94c3-154">**Hinweis**  Da DSA die Echt Zeit Verschlüsselung von Datenbankinformationen ausführt, werden die Informationen zum Wiederherstellungsschlüssel angezeigt, wenn das Konto, unter dem Sie angemeldet sind, über Berechtigungen für die Datenbank verfügt, wenn Sie die SQL-Tabellen für Wiederherstellungsschlüssel Informationen anzeigen.</span><span class="sxs-lookup"><span data-stu-id="a94c3-154">**Note** Because TDE performs real-time decryption of database information, the recovery key information will be visible if the account under which you are logged in has permissions to the database when you view the recovery key information SQL tables.</span></span>

 

### <span data-ttu-id="a94c3-155">Voraussetzungen für die Installation der Konformitäts-und Überwachungsdatenbank</span><span class="sxs-lookup"><span data-stu-id="a94c3-155">Installation prerequisites for the Compliance and Audit Database</span></span>

<span data-ttu-id="a94c3-156">Die Compliance-und Überwachungsdatenbank muss in einer unterstützten Version von SQLServer installiert sein.</span><span class="sxs-lookup"><span data-stu-id="a94c3-156">The Compliance and Audit Database must be installed on a supported version of SQLServer.</span></span>

<span data-ttu-id="a94c3-157">SQL Server muss während der Installation von MBAM Server Datenbankmoduldienste installiert haben und ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="a94c3-157">SQL Server must have Database Engine Services installed and running during MBAM server installation.</span></span>

<span data-ttu-id="a94c3-158">**Hinweis**  Eine Liste der unterstützten Betriebssysteme und SQLServer-Versionen finden Sie unter [unterstützte MBAM 1,0-Konfigurationen](mbam-10-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="a94c3-158">**Note** For a list of supported operating systems and SQLServer versions, see [MBAM 1.0 Supported Configurations](mbam-10-supported-configurations.md).</span></span>

 

## <span data-ttu-id="a94c3-159">Voraussetzungen für die Installation für MBAM-Clients</span><span class="sxs-lookup"><span data-stu-id="a94c3-159">Installation prerequisites for MBAM Clients</span></span>


<span data-ttu-id="a94c3-160">Die erforderlichen Voraussetzungen, die Sie erfüllen müssen, bevor Sie mit der MBAM-Client Installation beginnen, sind die folgenden:</span><span class="sxs-lookup"><span data-stu-id="a94c3-160">The necessary prerequisites that you must meet before you begin the MBAM Client installation are the following:</span></span>

-   <span data-ttu-id="a94c3-161">Trusted Platform Module (TPM) v 1.2-Funktion</span><span class="sxs-lookup"><span data-stu-id="a94c3-161">Trusted Platform Module (TPM) v1.2 capability</span></span>

-   <span data-ttu-id="a94c3-162">Der TPM-Chip muss im BIOS aktiviert sein und muss vom Betriebssystem rückgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="a94c3-162">The TPM chip must be turned on in the BIOS and it must be resettable from the operating system.</span></span> <span data-ttu-id="a94c3-163">Weitere Informationen finden Sie in der BIOS-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="a94c3-163">For more information, see the BIOS documentation.</span></span>

<span data-ttu-id="a94c3-164">**Warnung**  Stellen Sie sicher, dass Tastatur, Maus und Video direkt mit dem Computer verbunden sind, anstatt mit einem Tastatur-, Video-, Maus-oder KVM-Schalter.</span><span class="sxs-lookup"><span data-stu-id="a94c3-164">**Warning** Ensure that the keyboard, mouse, and video are directly connected to the computer, instead of to a keyboard, video, mouse (KVM) switch.</span></span> <span data-ttu-id="a94c3-165">Ein KVM-Switch kann die Fähigkeit des Computers stören, die physische Anwesenheit von Hardware zu erkennen.</span><span class="sxs-lookup"><span data-stu-id="a94c3-165">A KVM switch can interfere with the ability of the computer to detect the physical presence of hardware.</span></span>

 

## <span data-ttu-id="a94c3-166">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="a94c3-166">Related topics</span></span>


[<span data-ttu-id="a94c3-167">Planen der Bereitstellung von MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="a94c3-167">Planning to Deploy MBAM 1.0</span></span>](planning-to-deploy-mbam-10.md)

[<span data-ttu-id="a94c3-168">Von MBAM 1.0 unterstützte Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="a94c3-168">MBAM 1.0 Supported Configurations</span></span>](mbam-10-supported-configurations.md)

 

 





