---
title: Aktualisieren von MBAM 2.5 oder MBAM 2.5 SP1 von früheren Versionen
description: Aktualisieren von MBAM 2.5 oder MBAM 2.5 SP1 von früheren Versionen
author: dansimp
ms.assetid: a9edb4b8-5d5e-42ab-8db6-619db2878e50
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 07a03ebbbfce45f7f69a85000e18ddf1a58e53ad
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804463"
---
# <span data-ttu-id="15021-103">Aktualisieren von MBAM 2.5 oder MBAM 2.5 SP1 von früheren Versionen</span><span class="sxs-lookup"><span data-stu-id="15021-103">Upgrading to MBAM 2.5 or MBAM 2.5 SP1 from Previous Versions</span></span>


<span data-ttu-id="15021-104">In diesem Thema wird der Vorgang zum Aktualisieren des Microsoft BitLocker-Verwaltungs-und Überwachungsservers (MBAM) und des MBAM-Clients aus früheren Versionen von MBAM beschrieben.</span><span class="sxs-lookup"><span data-stu-id="15021-104">This topic describes the process for upgrading the Microsoft BitLocker Administration and Monitoring (MBAM) Server and the MBAM Client from earlier versions of MBAM.</span></span>

<span data-ttu-id="15021-105">**Hinweis**  Sie können ein Upgrade direkt auf MBAM 2,5 oder MBAM 2,5 SP1 aus einer beliebigen vorherigen Version von MBAM durchführen.</span><span class="sxs-lookup"><span data-stu-id="15021-105">**Note** You can upgrade directly to MBAM 2.5 or MBAM 2.5 SP1 from any previous version of MBAM.</span></span>

 

## <span data-ttu-id="15021-106">Vor dem Starten des Upgrades</span><span class="sxs-lookup"><span data-stu-id="15021-106">Before you start the upgrade</span></span>


<span data-ttu-id="15021-107">Überprüfen Sie die folgenden Informationen, bevor Sie mit dem Upgrade beginnen.</span><span class="sxs-lookup"><span data-stu-id="15021-107">Review the following information before you start the upgrade.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="15021-108">Was Sie wissen sollten, bevor Sie beginnen</span><span class="sxs-lookup"><span data-stu-id="15021-108">What to know before you start</span></span></th>
<th align="left"><span data-ttu-id="15021-109">Details</span><span class="sxs-lookup"><span data-stu-id="15021-109">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="15021-110">Wenn Sie die MBAM-Websites auf einem Server und die Webdienste auf einem anderen Server installieren, müssen Sie Windows PowerShell-Cmdlets verwenden, um Sie zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="15021-110">If you are installing the MBAM websites on one server and the web services on another server, you have to use Windows PowerShell cmdlets to configure them.</span></span></p></td>
<td align="left"><p><span data-ttu-id="15021-111">Der MBAM-Serverkonfigurations-Assistent unterstützt nicht die Konfiguration der Websites auf einem Server und die Webdienste auf einem anderen Server.</span><span class="sxs-lookup"><span data-stu-id="15021-111">The MBAM Server Configuration wizard does not support configuring the websites on one server and the web services on a different server.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="15021-112">Wenn Sie ein Upgrade auf mbam 2.5 oder 2,5 SP1 von mbam 2.0 oder 2,0 SP1 in Windows Server2008 R2 ausführen:</span><span class="sxs-lookup"><span data-stu-id="15021-112">If you are upgrading to MBAM2.5 or 2.5 SP1 from MBAM2.0 or 2.0 SP1 in Windows Server2008 R2:</span></span></p>
<p><span data-ttu-id="15021-113">Die Verwaltungs-und Überwachungs Website und das Self-Service-Portal funktionieren nicht, wenn Sie die erforderliche .NET Framework 4.5-Software installieren, nachdem Internet Informationsdienste (IIS) bereits installiert ist.</span><span class="sxs-lookup"><span data-stu-id="15021-113">The Administration and Monitoring Website and the Self-Service Portal will not work if you install the required .NET Framework4.5 software after Internet Information Services (IIS) is already installed.</span></span></p>
<p><span data-ttu-id="15021-114">Dieses Problem tritt auf, weil ASP.net bei IIS nicht ordnungsgemäß registriert werden kann, wenn .NET Framework installiert ist, nachdem IIS bereits installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="15021-114">This issue occurs because ASP.NET cannot be registered correctly with IIS if the .NET Framework is installed after IIS has already been installed.</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="15021-115">So beheben Sie dieses Problem:</span><span class="sxs-lookup"><span data-stu-id="15021-115">To resolve this issue:</span></span></strong></p>
<p><span data-ttu-id="15021-116">Führen Sie <strong> aspnet_regiis – i </strong> von folgendem Speicherort aus:</span><span class="sxs-lookup"><span data-stu-id="15021-116">Run <strong>aspnet_regiis –i</strong> from the following location:</span></span></p>
<p><span data-ttu-id="15021-117">C:\windows\microsoft.net\Framework\v4.0.30319</span><span class="sxs-lookup"><span data-stu-id="15021-117">C:\windows\microsoft.net\Framework\v4.0.30319</span></span></p>
<p><span data-ttu-id="15021-118">Weitere Informationen finden Sie unter: <a href="https://go.microsoft.com/fwlink/?LinkId=393272" data-raw-source="[ASP.NET IIS Registration Tool](https://go.microsoft.com/fwlink/?LinkId=393272)"> ASP.NET IIS-Registrierungs Tool </a> .</span><span class="sxs-lookup"><span data-stu-id="15021-118">For more information, see: <a href="https://go.microsoft.com/fwlink/?LinkId=393272" data-raw-source="[ASP.NET IIS Registration Tool](https://go.microsoft.com/fwlink/?LinkId=393272)">ASP.NET IIS Registration Tool</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="15021-119">Registrieren Sie einen SPN für das Anwendungspoolkonto, wenn alle folgenden Bedingungen erfüllt sind:</span><span class="sxs-lookup"><span data-stu-id="15021-119">Register an SPN on the application pool account if all of the following are true:</span></span></p>
<ul>
<li><p><span data-ttu-id="15021-120">Sie aktualisieren eine frühere Version von MBAM.</span><span class="sxs-lookup"><span data-stu-id="15021-120">You are upgrading from a previous version of MBAM.</span></span></p></li>
<li><p><span data-ttu-id="15021-121">Zurzeit führen Sie die MBAM-Websites nicht in einer Lastenausgleichs-oder verteilten Konfiguration aus, aber Sie möchten dies beim Upgrade auf MBAM 2.5 oder 2,5 SP1 tun.</span><span class="sxs-lookup"><span data-stu-id="15021-121">Currently, you are not running the MBAM websites in a load-balanced or distributed configuration, but you would like to do so when you upgrade to MBAM2.5 or 2.5 SP1.</span></span></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="15021-122">Anweisungen hierzu finden Sie unter <a href="planning-how-to-secure-the-mbam-websites.md#bkmk-registerspn" data-raw-source="[Planning How to Secure the MBAM Websites](planning-how-to-secure-the-mbam-websites.md#bkmk-registerspn)"> Planen der Sicherung der MBAM-Websites </a> .</span><span class="sxs-lookup"><span data-stu-id="15021-122">For instructions, see <a href="planning-how-to-secure-the-mbam-websites.md#bkmk-registerspn" data-raw-source="[Planning How to Secure the MBAM Websites](planning-how-to-secure-the-mbam-websites.md#bkmk-registerspn)">Planning How to Secure the MBAM Websites</a>.</span></span></p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="15021-123">Was wir empfehlen</span><span class="sxs-lookup"><span data-stu-id="15021-123">What we recommend</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="15021-124">Registrieren Sie einen Dienstprinzipalnamen (Service Principal Name, SPN) für das Anwendungspoolkonto, obwohl Sie möglicherweise bereits über registrierte SPNs für das Computerkonto verfügen.</span><span class="sxs-lookup"><span data-stu-id="15021-124">Register a service principal name (SPN) for the application pool account, even though you may already have registered SPNs for the machine account.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="15021-125">Warum wir es empfehlen</span><span class="sxs-lookup"><span data-stu-id="15021-125">Why we recommend it</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="15021-126">Das Registrieren eines SPN für das Anwendungspoolkonto ist erforderlich, um die Websites in einer Lastenausgleich-oder verteilten Konfiguration zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="15021-126">Registering an SPN on the application pool account is required to configure the websites in a load-balanced or distributed configuration.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="15021-127">Was geschieht, wenn SPNs bereits für ein Computerkonto konfiguriert sind?</span><span class="sxs-lookup"><span data-stu-id="15021-127">What happens if SPNs are already configured on a machine account?</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="15021-128">MBAM verwendet die SPNs, die Sie bereits registriert haben, und Sie müssen keine zusätzlichen SPNs konfigurieren, aber Sie können die Websites nicht in einer Lastenausgleich-oder verteilten Konfiguration konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="15021-128">MBAM will use the SPNs that you have already registered, and you don’t need to configure additional SPNs, but you are not able to configure the websites in a load-balanced or distributed configuration.</span></span></p></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="15021-129">Schritte zum Upgrade der MBAM-Server Infrastruktur</span><span class="sxs-lookup"><span data-stu-id="15021-129">Steps to upgrade the MBAM Server infrastructure</span></span>


<span data-ttu-id="15021-130">Führen Sie die Schritte in den folgenden Abschnitten aus, um MBAM für die eigenständige Topologie oder die System Center Configuration Manager-Integrations Topologie zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="15021-130">Use the steps in the following sections to upgrade MBAM for the Stand-alone topology or the System Center Configuration Manager Integration topology.</span></span>

**<span data-ttu-id="15021-131">So aktualisieren Sie die MBAM-Server Infrastruktur für eigenständige Topologie</span><span class="sxs-lookup"><span data-stu-id="15021-131">To upgrade the MBAM Server infrastructure for Stand-alone topology</span></span>**

1.  <span data-ttu-id="15021-132">Deinstallieren Sie frühere Versionen von MBAM aus **Programmen und Funktionen** sowie von Webservern, um sicherzustellen, dass Informationen nicht von MBAM-Clients in die MBAM-Infrastruktur geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="15021-132">Uninstall previous versions of MBAM from **Programs and Features** and from web servers to make sure that information is not being written from MBAM clients to the MBAM infrastructure.</span></span> <span data-ttu-id="15021-133">Anweisungen hierzu finden Sie unter [Entfernen von MBAM-Server Features oder Software](removing-mbam-server-features-or-software.md#bkmk-removeserverfeatures).</span><span class="sxs-lookup"><span data-stu-id="15021-133">For instructions, see [Removing MBAM Server Features or Software](removing-mbam-server-features-or-software.md#bkmk-removeserverfeatures).</span></span>

2.  <span data-ttu-id="15021-134">Sichern Sie Ihre Datenbanken.</span><span class="sxs-lookup"><span data-stu-id="15021-134">Back up your databases.</span></span>

3.  <span data-ttu-id="15021-135">Deinstallieren Sie frühere Versionen von MBAM von SQL Server mithilfe von **Programmen und Features**, einschließlich SQL-Servern, die die MBAM-Berichte über SQL Server Reporting Services hosten.</span><span class="sxs-lookup"><span data-stu-id="15021-135">Uninstall previous versions of MBAM from SQL Server by using **Programs and Features**, including SQL Servers hosting the MBAM reports via SQL Server Reporting Services.</span></span> <span data-ttu-id="15021-136">Entfernen Sie alle verbleibenden temporären MBAM Server-Dateien oder-Ordner aus dem Datenbankserver und Reporting Services.</span><span class="sxs-lookup"><span data-stu-id="15021-136">Remove any remaining MBAM server temporary files or folders from the database server and reporting services.</span></span>

    <span data-ttu-id="15021-137">**Hinweis**  Die Datenbankenwerden nicht entfernt, und alle Kompatibilitäts-und Wiederherstellungsdaten werden in der Datenbank verwaltet.</span><span class="sxs-lookup"><span data-stu-id="15021-137">**Note** The databases will not be removed, and all compliance and recovery data is maintained in the database.</span></span>

     

4.  <span data-ttu-id="15021-138">Installieren und konfigurieren Sie die mbam 2.5-oder 2,5 SP1-Datenbanken,-Berichte und-Webanwendungen in dieser Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="15021-138">Install and configure the MBAM2.5 or 2.5 SP1 databases, reports, and web applications, in that order.</span></span> <span data-ttu-id="15021-139">Die Datenbankenwerden direkt aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="15021-139">The databases are upgraded in place.</span></span>

5.  <span data-ttu-id="15021-140">Aktualisieren Sie die Gruppenrichtlinienobjekte (Group Policy Objects, GPOs) mithilfe der MBAM 2,5-Vorlagen, um die neuen Features in MBAM, wie erzwungene Verschlüsselung, zu nutzen.</span><span class="sxs-lookup"><span data-stu-id="15021-140">Update the Group Policy Objects (GPOs) using the MBAM 2.5 Templates to leverage the new features in MBAM, such as enforced encryption.</span></span> <span data-ttu-id="15021-141">Wenn Sie die GPOs und den MBAM-Client nicht auf MBAM 2,5 aktualisieren, werden frühere Versionen von MBAM-Clients weiterhin mit eingeschränkter Funktionalität gegen ihre aktuellen GPOs gemeldet.</span><span class="sxs-lookup"><span data-stu-id="15021-141">If you do not update the GPOs and the MBAM client to MBAM 2.5, earlier versions of MBAM clients will continue to report against your current GPOs with reduced functionality.</span></span> <span data-ttu-id="15021-142">Informationen zum Herunterladen der neuesten ADMX-Vorlagen finden Sie unter [Abrufen von MDOP-Gruppenrichtlinien (ADMX)](https://www.microsoft.com/download/details.aspx?id=41183) .</span><span class="sxs-lookup"><span data-stu-id="15021-142">See [How to Get MDOP Group Policy (.admx) Templates](https://www.microsoft.com/download/details.aspx?id=41183) to download the latest ADMX templates.</span></span>

    <span data-ttu-id="15021-143">Nachdem Sie die MBAM-Serverinfrastruktur aktualisiert haben, werden die vorhandenen Clientcomputer weiterhin erfolgreich an den MBAM 2.5-oder 2,5 SP1-Server gemeldet, und die Wiederherstellungsdaten werden weiterhin gespeichert.</span><span class="sxs-lookup"><span data-stu-id="15021-143">After you upgrade the MBAM Server infrastructure, the existing client computers continue to successfully report to the MBAM2.5 or 2.5 SP1 Server, and recovery data continues to be stored.</span></span>

6.  <span data-ttu-id="15021-144">Installieren Sie den neuesten mbam 2.5-oder 2,5 SP1-Client.</span><span class="sxs-lookup"><span data-stu-id="15021-144">Install the latest MBAM2.5 or 2.5 SP1 Client.</span></span> <span data-ttu-id="15021-145">Client Computer müssen nach der Bereitstellung nicht neu gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="15021-145">Client computers do not need to be rebooted after the deployment.</span></span>

**<span data-ttu-id="15021-146">So aktualisieren Sie die MBAM-Infrastruktur für die System Center Configuration Manager-Integrations Topologie</span><span class="sxs-lookup"><span data-stu-id="15021-146">To upgrade the MBAM infrastructure for System Center Configuration Manager Integration topology</span></span>**

1.  <span data-ttu-id="15021-147">Deinstallieren Sie frühere Versionen von MBAM aus **Programmen und Funktionen** sowie von Webservern, um sicherzustellen, dass Informationen nicht von MBAM-Clients in die MBAM-Infrastruktur geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="15021-147">Uninstall previous versions of MBAM from **Programs and Features** and from web servers to make sure that information is not being written from MBAM clients to the MBAM infrastructure.</span></span> <span data-ttu-id="15021-148">Anweisungen hierzu finden Sie unter [Entfernen von MBAM-Server Features oder Software](removing-mbam-server-features-or-software.md#bkmk-removeserverfeatures).</span><span class="sxs-lookup"><span data-stu-id="15021-148">For instructions, see [Removing MBAM Server Features or Software](removing-mbam-server-features-or-software.md#bkmk-removeserverfeatures).</span></span>

2.  <span data-ttu-id="15021-149">Sichern Sie Ihre Datenbanken.</span><span class="sxs-lookup"><span data-stu-id="15021-149">Back up your databases.</span></span>

3.  <span data-ttu-id="15021-150">Deinstallieren Sie frühere Versionen von MBAM von SQL Server mithilfe von **Programmen und Features**, einschließlich SQL-Servern, die die MBAM-Berichte über SQL Server Reporting Services hosten.</span><span class="sxs-lookup"><span data-stu-id="15021-150">Uninstall previous versions of MBAM from SQL Server by using **Programs and Features**, including SQL Servers hosting the MBAM reports via SQL Server Reporting Services.</span></span> <span data-ttu-id="15021-151">Entfernen Sie alle verbleibenden temporären MBAM Server-Dateien oder-Ordner aus dem Datenbankserver und Reporting Services.</span><span class="sxs-lookup"><span data-stu-id="15021-151">Remove any remaining MBAM server temporary files or folders from the database server and reporting services.</span></span>

4.  <span data-ttu-id="15021-152">Deinstallieren Sie MBAM vom Configuration Manager-Server.</span><span class="sxs-lookup"><span data-stu-id="15021-152">Uninstall MBAM from the Configuration Manager server.</span></span>

    <span data-ttu-id="15021-153">**Hinweis**  Die Datenbanken und die Configuration Manager-Objekte (Baseline, MBAM unterstützte Computersammlung und Berichte) werden nicht entfernt, und alle Kompatibilitäts-und Wiederherstellungsdaten werden in der Datenbank verwaltet.</span><span class="sxs-lookup"><span data-stu-id="15021-153">**Note** The databases and the Configuration Manager objects (baseline, MBAM supported computers collection, and Reports) will not be removed, and all compliance and recovery data is maintained in the database.</span></span>

     

5.  <span data-ttu-id="15021-154">Aktualisieren Sie die MOF-Dateien.</span><span class="sxs-lookup"><span data-stu-id="15021-154">Update the .mof files.</span></span>

6.  <span data-ttu-id="15021-155">Installieren und konfigurieren Sie die mbam 2.5-oder 2,5 SP1-Datenbanken,-Berichte,-Webanwendungen und die Configuration Manager-Integration in dieser Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="15021-155">Install and configure the MBAM2.5 or 2.5 SP1 databases, reports, web applications, and Configuration Manager integration, in that order.</span></span> <span data-ttu-id="15021-156">Die Datenbanken und Configuration Manager-Objekte werden direkt aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="15021-156">The databases and Configuration Manager objects are upgraded in place.</span></span>

7.  <span data-ttu-id="15021-157">Aktualisieren Sie optional die Gruppenrichtlinienobjekte (Group Policy Objects, GPOs), und bearbeiten Sie die Einstellungen, wenn Sie neue Features in MBAM implementieren möchten, beispielsweise erzwungene Verschlüsselung.</span><span class="sxs-lookup"><span data-stu-id="15021-157">Optionally, update the Group Policy Objects (GPOs), and edit the settings if you want to implement new features in MBAM, such as enforced encryption.</span></span> <span data-ttu-id="15021-158">Wenn Sie die GPOs nicht aktualisieren, wird MBAM weiterhin für Ihre aktuellen GPOs gemeldet.</span><span class="sxs-lookup"><span data-stu-id="15021-158">If you do not update the GPOs, MBAM will continue to report against your current GPOs.</span></span> <span data-ttu-id="15021-159">Informationen zum Herunterladen der neuesten ADMX-Vorlagen finden Sie unter [Abrufen von MDOP-Gruppenrichtlinien (ADMX)](https://docs.microsoft.com/microsoft-desktop-optimization-pack/solutions/how-to-download-and-deploy-mdop-group-policy--admx--templates) .</span><span class="sxs-lookup"><span data-stu-id="15021-159">See [How to Get MDOP Group Policy (.admx) Templates](https://docs.microsoft.com/microsoft-desktop-optimization-pack/solutions/how-to-download-and-deploy-mdop-group-policy--admx--templates) to download the latest ADMX templates.</span></span>

    <span data-ttu-id="15021-160">Nachdem Sie die MBAM-Serverinfrastruktur aktualisiert haben, werden die vorhandenen Clientcomputer weiterhin erfolgreich an den MBAM 2.5-oder 2,5 SP1-Server gemeldet, und die Wiederherstellungsdaten werden weiterhin gespeichert.</span><span class="sxs-lookup"><span data-stu-id="15021-160">After you upgrade the MBAM Server infrastructure, the existing client computers continue to successfully report to the MBAM2.5 or 2.5 SP1 Server, and recovery data continues to be stored.</span></span>

8.  <span data-ttu-id="15021-161">Installieren Sie den neuesten mbam 2.5-oder 2,5 SP1-Client.</span><span class="sxs-lookup"><span data-stu-id="15021-161">Install the latest MBAM2.5 or 2.5 SP1 Client.</span></span> <span data-ttu-id="15021-162">Client Computer müssen nach der Bereitstellung nicht neu gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="15021-162">Client computers do not need to be rebooted after the deployment.</span></span>

## <span data-ttu-id="15021-163">Upgrade-Unterstützung für den MBAM-Client</span><span class="sxs-lookup"><span data-stu-id="15021-163">Upgrade support for the MBAM Client</span></span>


<span data-ttu-id="15021-164">MBAM unterstützt Upgrades auf den MBAM 2.5-Client aus einer früheren Version des MBAM-Clients.</span><span class="sxs-lookup"><span data-stu-id="15021-164">MBAM supports upgrades to the MBAM2.5 Client from any earlier version of the MBAM Client.</span></span>

**<span data-ttu-id="15021-165">Möglichkeiten zum Installieren des MBAM-Clients:</span><span class="sxs-lookup"><span data-stu-id="15021-165">Ways to install the MBAM Client:</span></span>**

-   <span data-ttu-id="15021-166">Aktualisieren Sie die Computer, auf denen der MBAM-Client ausgeführt wird, alle auf einmal oder schrittweise nach der Installation der MBAM 2.5-Server Infrastruktur.</span><span class="sxs-lookup"><span data-stu-id="15021-166">Upgrade the computers running MBAM Client all at once or gradually after you install the MBAM2.5 Server infrastructure.</span></span>

-   <span data-ttu-id="15021-167">Installieren Sie den MBAM-Client über ein elektronisches Softwareverteilungssystem oder über Tools wie Active Directory-Domänendienste oder System Center Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="15021-167">Install the MBAM Client through an electronic software distribution system or through tools such as Active Directory Domain Services or System Center Configuration Manager.</span></span>



## <span data-ttu-id="15021-168">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="15021-168">Related topics</span></span>


[<span data-ttu-id="15021-169">Bereitstellen von MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="15021-169">Deploying MBAM 2.5</span></span>](deploying-mbam-25.md)

[<span data-ttu-id="15021-170">Bereitstellen des MBAM 2.5-Clients</span><span class="sxs-lookup"><span data-stu-id="15021-170">Deploying the MBAM 2.5 Client</span></span>](deploying-the-mbam-25-client.md)

[<span data-ttu-id="15021-171">Konfigurieren der MBAM 2.5-Serverfunktionen</span><span class="sxs-lookup"><span data-stu-id="15021-171">Configuring the MBAM 2.5 Server Features</span></span>](configuring-the-mbam-25-server-features.md)

 

## <span data-ttu-id="15021-172">Sie haben einen Vorschlag für MBAM?</span><span class="sxs-lookup"><span data-stu-id="15021-172">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="15021-173">[Hier](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)können Sie Vorschläge hinzufügen oder abstimmen.</span><span class="sxs-lookup"><span data-stu-id="15021-173">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span>
- <span data-ttu-id="15021-174">Bei MBAM-Problemen verwenden Sie das [MBAM TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="15021-174">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





