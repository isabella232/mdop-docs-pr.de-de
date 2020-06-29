---
title: Erste Schritte mit UE-V 2.x
description: Erste Schritte mit UE-V 2.x
author: dansimp
ms.assetid: 526ecbf0-0dee-4f0b-b017-8f8d25357b14
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 02/13/2017
ms.openlocfilehash: d3f01dd67ea9e5f6cfcf5dc3425265deff3f7df1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809865"
---
# <span data-ttu-id="ee90d-103">Erste Schritte mit UE-V 2.x</span><span class="sxs-lookup"><span data-stu-id="ee90d-103">Get Started with UE-V 2.x</span></span>


<span data-ttu-id="ee90d-104">Führen Sie die Schritte in diesem Leitfaden aus, um die Microsoft User Experience Virtualization (UE-V) 2,0 oder 2,1 in einer kleinen Testumgebung schnell bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="ee90d-104">Follow the steps in this guide to quickly deploy Microsoft User Experience Virtualization (UE-V) 2.0 or 2.1 in a small test environment.</span></span> <span data-ttu-id="ee90d-105">So können Sie feststellen, ob UE-V die richtige Lösung zur Verwaltung von Benutzereinstellungen auf mehreren Geräten innerhalb Ihres Unternehmens ist.</span><span class="sxs-lookup"><span data-stu-id="ee90d-105">This helps you determine whether UE-V is the right solution to manage user settings across multiple devices within your enterprise.</span></span>

<span data-ttu-id="ee90d-106">**Hinweis**  Die Informationen in diesem Abschnitt werden während der restlichen Dokumentation ausführlicher wiederholt.</span><span class="sxs-lookup"><span data-stu-id="ee90d-106">**Note** The information in this section is repeated in greater detail throughout the rest of the documentation.</span></span> <span data-ttu-id="ee90d-107">Wenn Sie also bereits wissen, dass UE-v 2 die richtige Lösung ist und Sie es nicht auswerten müssen, können Sie einfach nach rechts [eine UE-v 2. x-Bereitstellung vorbereiten](prepare-a-ue-v-2x-deployment-new-uevv2.md).</span><span class="sxs-lookup"><span data-stu-id="ee90d-107">So if you already know that UE-V 2 is the right solution and you don’t need to evaluate it, you can just go right to [Prepare a UE-V 2.x Deployment](prepare-a-ue-v-2x-deployment-new-uevv2.md).</span></span>

 

<span data-ttu-id="ee90d-108">Die Standardinstallation von UE-V synchronisiert die Standardeinstellungen für Microsoft Windows und Office sowie viele Windows-App-Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="ee90d-108">The standard installation of UE-V synchronizes the default Microsoft Windows and Office settings and many Windows app settings.</span></span> <span data-ttu-id="ee90d-109">Stellen Sie sicher, dass Ihre Testumgebung zwei oder Mehrbenutzercomputer umfasst, die den Netzwerkzugriff freigeben, und Sie in kürzester Zeit UE-V evaluieren.</span><span class="sxs-lookup"><span data-stu-id="ee90d-109">Make sure your test environment includes two or more user computers that share network access and you’ll be evaluating UE-V in just a short time.</span></span>

-   <span data-ttu-id="ee90d-110">[Schritt 1: Überprüfen der Voraussetzungen](#step1): Stellen Sie sicher, dass Ihre Umgebung UE-V ausführen kann, einschließlich Details zu unterstützten Konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="ee90d-110">[Step 1: Confirm Prerequisites](#step1): Make sure your environment is able to run UE-V, including details about supported configurations.</span></span>

-   <span data-ttu-id="ee90d-111">[Schritt 2: Bereitstellen des Speicherorts für die Einstellungen für UE-v 2](#step2): alle UE-v-Bereitstellungen erfordern einen Speicherort für Einstellungs Pakete, die die synchronisierten Einstellungswerte enthalten.</span><span class="sxs-lookup"><span data-stu-id="ee90d-111">[Step 2: Deploy the Settings Storage Location for UE-V 2](#step2): All UE-V deployments require a location for settings packages that contain the synchronized setting values.</span></span>

-   <span data-ttu-id="ee90d-112">[Schritt 3: Bereitstellen des UE-v 2-Agents](#step3): damit die Einstellungen mit UE-v synchronisiert werden können, muss der UE-v-Agent installiert sein und ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="ee90d-112">[Step 3: Deploy the UE-V 2 Agent](#step3): To synchronize settings using UE-V, devices must have the UE-V Agent installed and running.</span></span>

-   <span data-ttu-id="ee90d-113">[Schritt 4: Testen Ihrer UE-v 2-Evaluierungsbereitstellung](#step4): führen Sie einige Tests auf zwei Computern durch, auf denen der UE-v-Agent installiert ist, und sehen Sie, wie UE-v funktioniert.</span><span class="sxs-lookup"><span data-stu-id="ee90d-113">[Step 4: Test Your UE-V 2 Evaluation Deployment](#step4): Run a few tests on two computers that have the UE-V Agent installed and see how UE-V works.</span></span>

<span data-ttu-id="ee90d-114">Das wars!</span><span class="sxs-lookup"><span data-stu-id="ee90d-114">That’s it!</span></span> <span data-ttu-id="ee90d-115">Nachdem Sie die Schritte ausgeführt haben, können Sie bewerten, wie UE-V in Ihrem Unternehmen funktionieren kann.</span><span class="sxs-lookup"><span data-stu-id="ee90d-115">Once you follow the steps, you’ll be able to evaluate how UE-V can work in your enterprise.</span></span>

<span data-ttu-id="ee90d-116">**Weitere Auswertung:** Sie können auch zusätzliche Schritte ausführen, um einige Drittanbieter-und Branchenanwendungen so zu konfigurieren, dass Ihre Einstellungen mithilfe von UE-v wie in [Bereitstellen von UE-v 2. x für benutzerdefinierte Anwendungen](deploy-ue-v-2x-for-custom-applications-new-uevv2.md)synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="ee90d-116">**Further evaluation:** You can also perform additional steps to configure some third-party and line-of-business applications to synchronize their settings using UE-V as detailed in [Deploy UE-V 2.x for Custom Applications](deploy-ue-v-2x-for-custom-applications-new-uevv2.md).</span></span>

## <a href="" id="step1"></a><span data-ttu-id="ee90d-117">Schritt 1: Voraussetzungen bestätigen</span><span class="sxs-lookup"><span data-stu-id="ee90d-117">Step 1: Confirm Prerequisites</span></span>


<span data-ttu-id="ee90d-118">Bevor Sie fortfahren, stellen Sie sicher, dass Ihre Umgebung die folgenden Voraussetzungen für die Ausführung von UE-V umfasst.</span><span class="sxs-lookup"><span data-stu-id="ee90d-118">Before you proceed, make sure your environment includes these requirements for running UE-V.</span></span>

<table style="width:100%;">
<colgroup>
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="ee90d-119">Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="ee90d-119">Operating system</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="ee90d-120">Edition</span><span class="sxs-lookup"><span data-stu-id="ee90d-120">Edition</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="ee90d-121">Service Pack</span><span class="sxs-lookup"><span data-stu-id="ee90d-121">Service pack</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="ee90d-122">System Architektur</span><span class="sxs-lookup"><span data-stu-id="ee90d-122">System architecture</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="ee90d-123">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="ee90d-123">Windows PowerShell</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="ee90d-124">Microsoft .NET Framework</span><span class="sxs-lookup"><span data-stu-id="ee90d-124">Microsoft .NET Framework</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ee90d-125">Windows7</span><span class="sxs-lookup"><span data-stu-id="ee90d-125">Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="ee90d-126">Ultimate-, Enterprise-oder Professional-Edition</span><span class="sxs-lookup"><span data-stu-id="ee90d-126">Ultimate, Enterprise, or Professional Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="ee90d-127">SP1</span><span class="sxs-lookup"><span data-stu-id="ee90d-127">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="ee90d-128">32 Bit oder 64 Bit</span><span class="sxs-lookup"><span data-stu-id="ee90d-128">32-bit or 64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="ee90d-129">Windows PowerShell 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="ee90d-129">Windows PowerShell 3.0 or higher</span></span></p></td>
<td align="left"><p><span data-ttu-id="ee90d-130">.NET Framework 4 oder höher</span><span class="sxs-lookup"><span data-stu-id="ee90d-130">.NET Framework 4 or higher</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ee90d-131">Windows Server2008R2</span><span class="sxs-lookup"><span data-stu-id="ee90d-131">Windows Server2008R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="ee90d-132">Standard, Enterprise, Datacenter oder Web Server</span><span class="sxs-lookup"><span data-stu-id="ee90d-132">Standard, Enterprise, Datacenter, or Web Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="ee90d-133">SP1</span><span class="sxs-lookup"><span data-stu-id="ee90d-133">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="ee90d-134">64Bit</span><span class="sxs-lookup"><span data-stu-id="ee90d-134">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="ee90d-135">Windows PowerShell 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="ee90d-135">Windows PowerShell 3.0 or higher</span></span></p></td>
<td align="left"><p><span data-ttu-id="ee90d-136">.NET Framework 4 oder höher</span><span class="sxs-lookup"><span data-stu-id="ee90d-136">.NET Framework 4 or higher</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ee90d-137">Windows8.1</span><span class="sxs-lookup"><span data-stu-id="ee90d-137">Windows 8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="ee90d-138">Enterprise oder pro</span><span class="sxs-lookup"><span data-stu-id="ee90d-138">Enterprise or Pro</span></span></p></td>
<td align="left"><p><span data-ttu-id="ee90d-139">Keine</span><span class="sxs-lookup"><span data-stu-id="ee90d-139">None</span></span></p></td>
<td align="left"><p><span data-ttu-id="ee90d-140">32 Bit oder 64 Bit</span><span class="sxs-lookup"><span data-stu-id="ee90d-140">32-bit or 64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="ee90d-141">Windows PowerShell 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="ee90d-141">Windows PowerShell 3.0 or higher</span></span></p></td>
<td align="left"><p><span data-ttu-id="ee90d-142">.NET Framework 4,5</span><span class="sxs-lookup"><span data-stu-id="ee90d-142">.NET Framework 4.5</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ee90d-143">Windows Server 2012 oder Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="ee90d-143">Windows Server 2012 or Windows Server 2012 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="ee90d-144">Standard oder Rechenzentrum</span><span class="sxs-lookup"><span data-stu-id="ee90d-144">Standard or Datacenter</span></span></p></td>
<td align="left"><p><span data-ttu-id="ee90d-145">Keine</span><span class="sxs-lookup"><span data-stu-id="ee90d-145">None</span></span></p></td>
<td align="left"><p><span data-ttu-id="ee90d-146">64Bit</span><span class="sxs-lookup"><span data-stu-id="ee90d-146">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="ee90d-147">Windows PowerShell 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="ee90d-147">Windows PowerShell 3.0 or higher</span></span></p></td>
<td align="left"><p><span data-ttu-id="ee90d-148">.NET Framework 4,5</span><span class="sxs-lookup"><span data-stu-id="ee90d-148">.NET Framework 4.5</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ee90d-149">Windows 10, Pre-1607 Version</span><span class="sxs-lookup"><span data-stu-id="ee90d-149">Windows 10, pre-1607 verison</span></span></p></td>
<td align="left"><p><span data-ttu-id="ee90d-150">Enterprise oder pro</span><span class="sxs-lookup"><span data-stu-id="ee90d-150">Enterprise or Pro</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="ee90d-151">32 Bit oder 64 Bit</span><span class="sxs-lookup"><span data-stu-id="ee90d-151">32-bit or 64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="ee90d-152">Windows PowerShell 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="ee90d-152">Windows PowerShell 3.0 or higher</span></span></p></td>
<td align="left"><p><span data-ttu-id="ee90d-153">.NET Framework 4,5</span><span class="sxs-lookup"><span data-stu-id="ee90d-153">.NET Framework 4.5</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ee90d-154">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="ee90d-154">Windows Server 2016</span></span></p></td>
<td align="left"><p><span data-ttu-id="ee90d-155">Standard oder Rechenzentrum</span><span class="sxs-lookup"><span data-stu-id="ee90d-155">Standard or Datacenter</span></span></p></td>
<td align="left"><p><span data-ttu-id="ee90d-156">Keine</span><span class="sxs-lookup"><span data-stu-id="ee90d-156">None</span></span></p></td>
<td align="left"><p><span data-ttu-id="ee90d-157">64Bit</span><span class="sxs-lookup"><span data-stu-id="ee90d-157">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="ee90d-158">Windows PowerShell 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="ee90d-158">Windows PowerShell 3.0 or higher</span></span></p></td>
<td align="left"><p><span data-ttu-id="ee90d-159">.NET Framework 4,5</span><span class="sxs-lookup"><span data-stu-id="ee90d-159">.NET Framework 4.5</span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="ee90d-160">**Hinweis:** Ab Windows 10, Version 1607, ist UE-V in [Windows 10 für Enterprise](https://www.microsoft.com/WindowsForBusiness/windows-for-enterprise) enthalten und nicht mehr Teil des Microsoft-Desktop Optimierungs Pakets.</span><span class="sxs-lookup"><span data-stu-id="ee90d-160">**Note:** Starting with Windows 10, version 1607, UE-V is included with [Windows 10 for Enterprise](https://www.microsoft.com/WindowsForBusiness/windows-for-enterprise) and is no longer part of the Microsoft Desktop Optimization Pack</span></span>

<span data-ttu-id="ee90d-161">Auch...</span><span class="sxs-lookup"><span data-stu-id="ee90d-161">Also…</span></span>

-   <span data-ttu-id="ee90d-162">**MDOP-Lizenz:** Diese Technologie ist Teil des Microsoft Desktop Optimization Pack (MDOP).</span><span class="sxs-lookup"><span data-stu-id="ee90d-162">**MDOP License:** This technology is a part of the Microsoft Desktop Optimization Pack (MDOP).</span></span> <span data-ttu-id="ee90d-163">Unternehmenskunden können MDOP mit Microsoft Software Assurance erhalten.</span><span class="sxs-lookup"><span data-stu-id="ee90d-163">Enterprise customers can get MDOP with Microsoft Software Assurance.</span></span> <span data-ttu-id="ee90d-164">Weitere Informationen zur Microsoft-Software Assurance und zum Erwerb von MDOP finden Sie unter wie erhalte ich MDOP ( https://go.microsoft.com/fwlink/p/?LinkId=322049) .</span><span class="sxs-lookup"><span data-stu-id="ee90d-164">For more information about Microsoft Software Assurance and acquiring MDOP, see How Do I Get MDOP (https://go.microsoft.com/fwlink/p/?LinkId=322049).</span></span>

-   <span data-ttu-id="ee90d-165">**Administratoranmeldeinformationen** für jeden Computer, auf dem die Installation erfolgen soll</span><span class="sxs-lookup"><span data-stu-id="ee90d-165">**Administrative Credentials** for any computer on which you’ll be installing</span></span>

## <a href="" id="step2"></a><span data-ttu-id="ee90d-166">Schritt 2: Bereitstellen des Speicherorts für Einstellungen für UE-V 2</span><span class="sxs-lookup"><span data-stu-id="ee90d-166">Step 2: Deploy the Settings Storage Location for UE-V 2</span></span>


<span data-ttu-id="ee90d-167">Sie müssen einen Speicherort für Einstellungen bereitstellen, eine standardmäßige Netzwerkfreigabe, auf der Benutzereinstellungen in einer Einstellungspaket Datei gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="ee90d-167">You’ll need to deploy a settings storage location, a standard network share where user settings are stored in a settings package file.</span></span> <span data-ttu-id="ee90d-168">Wenn Sie die Speicherfreigabe für Einstellungen erstellen, sollten Sie den Zugriff auf Benutzer einschränken, für die Sie erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="ee90d-168">When you create the settings storage share, you should limit access to users that require it.</span></span> <span data-ttu-id="ee90d-169">[Bereitstellen eines Einstellungsspeicher Orts](https://technet.microsoft.com/library/dn458891.aspx#ssl) bietet ausführlichere Informationen.</span><span class="sxs-lookup"><span data-stu-id="ee90d-169">[Deploy a Settings Storage Location](https://technet.microsoft.com/library/dn458891.aspx#ssl) provides more detailed information.</span></span>

**<span data-ttu-id="ee90d-170">Erstellen einer Netzwerkfreigabe</span><span class="sxs-lookup"><span data-stu-id="ee90d-170">Create a network share</span></span>**

1.  <span data-ttu-id="ee90d-171">Erstellen Sie eine neue Sicherheitsgruppe, und fügen Sie Ihr UE-V-Benutzer hinzu.</span><span class="sxs-lookup"><span data-stu-id="ee90d-171">Create a new security group and add UE-V users to it.</span></span>

2.  <span data-ttu-id="ee90d-172">Erstellen Sie einen neuen Ordner auf dem zentral gelegenen Computer, auf dem die UE-v-Einstellungs Pakete gespeichert sind, und gewähren Sie dem UE-v-Benutzer Zugriff mit Gruppen Berechtigungen für den Ordner.</span><span class="sxs-lookup"><span data-stu-id="ee90d-172">Create a new folder on the centrally located computer that stores the UE-V settings packages, and then grant the UE-V users access with group permissions to the folder.</span></span> <span data-ttu-id="ee90d-173">Der Administrator, der UE-V unterstützt, muss über Berechtigungen für diesen freigegebenen Ordner verfügen.</span><span class="sxs-lookup"><span data-stu-id="ee90d-173">The administrator who supports UE-V must have permissions to this shared folder.</span></span>

3.  <span data-ttu-id="ee90d-174">Zuweisen von Berechtigungen für UE-V-Benutzer zum Erstellen eines Verzeichnisses, wenn Sie eine Verbindung herstellen.</span><span class="sxs-lookup"><span data-stu-id="ee90d-174">Assign UE-V users permission to create a directory when they connect.</span></span> <span data-ttu-id="ee90d-175">Erteilen Sie allen Unterverzeichnissen dieses Verzeichnisses die vollständige Berechtigung, aber blockieren Sie den Zugriff auf etwas darüber.</span><span class="sxs-lookup"><span data-stu-id="ee90d-175">Grant full permission to all subdirectories of that directory, but block access to anything above.</span></span>

    1.  <span data-ttu-id="ee90d-176">Legen Sie die folgenden SMB-Berechtigungen (Share-Level-Server-Nachrichten Block) für den Ordner "Settings-Speicherort" ein.</span><span class="sxs-lookup"><span data-stu-id="ee90d-176">Set the following share-level Server Message Block (SMB) permissions for the settings storage location folder.</span></span>

        <table>
        <colgroup>
        <col width="50%" />
        <col width="50%" />
        </colgroup>
        <thead>
        <tr class="header">
        <th align="left"><strong><span data-ttu-id="ee90d-177">Benutzerkonto</span><span class="sxs-lookup"><span data-stu-id="ee90d-177">User account</span></span></strong></th>
        <th align="left"><strong><span data-ttu-id="ee90d-178">Empfohlene Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="ee90d-178">Recommended permissions</span></span></strong></th>
        </tr>
        </thead>
        <tbody>
        <tr class="odd">
        <td align="left"><p><span data-ttu-id="ee90d-179">Jeder</span><span class="sxs-lookup"><span data-stu-id="ee90d-179">Everyone</span></span></p></td>
        <td align="left"><p><span data-ttu-id="ee90d-180">Keine Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="ee90d-180">No permissions</span></span></p></td>
        </tr>
        <tr class="even">
        <td align="left"><p><span data-ttu-id="ee90d-181">Sicherheitsgruppe der UE-V-Benutzer</span><span class="sxs-lookup"><span data-stu-id="ee90d-181">Security group of UE-V users</span></span></p></td>
        <td align="left"><p><span data-ttu-id="ee90d-182">Vollzugriff</span><span class="sxs-lookup"><span data-stu-id="ee90d-182">Full control</span></span></p></td>
        </tr>
        </tbody>
        </table>

         

    2.  <span data-ttu-id="ee90d-183">Legen Sie die folgenden NTFS-Dateisystemberechtigungen für den Ordner "Settings Storage Location" ein.</span><span class="sxs-lookup"><span data-stu-id="ee90d-183">Set the following NTFS file system permissions for the settings storage location folder.</span></span>

        <table>
        <colgroup>
        <col width="33%" />
        <col width="33%" />
        <col width="33%" />
        </colgroup>
        <thead>
        <tr class="header">
        <th align="left"><strong><span data-ttu-id="ee90d-184">Benutzerkonto</span><span class="sxs-lookup"><span data-stu-id="ee90d-184">User account</span></span></strong></th>
        <th align="left"><strong><span data-ttu-id="ee90d-185">Empfohlene Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="ee90d-185">Recommended permissions</span></span></strong></th>
        <th align="left"><strong><span data-ttu-id="ee90d-186">Ordner</span><span class="sxs-lookup"><span data-stu-id="ee90d-186">Folder</span></span></strong></th>
        </tr>
        </thead>
        <tbody>
        <tr class="odd">
        <td align="left"><p><span data-ttu-id="ee90d-187">Ersteller/Besitzer</span><span class="sxs-lookup"><span data-stu-id="ee90d-187">Creator/owner</span></span></p></td>
        <td align="left"><p><span data-ttu-id="ee90d-188">Vollzugriff</span><span class="sxs-lookup"><span data-stu-id="ee90d-188">Full control</span></span></p></td>
        <td align="left"><p><span data-ttu-id="ee90d-189">Nur Unterordner und Dateien</span><span class="sxs-lookup"><span data-stu-id="ee90d-189">Subfolders and files only</span></span></p></td>
        </tr>
        <tr class="even">
        <td align="left"><p><span data-ttu-id="ee90d-190">Sicherheitsgruppe der UE-V-Benutzer</span><span class="sxs-lookup"><span data-stu-id="ee90d-190">Security group of UE-V users</span></span></p></td>
        <td align="left"><p><span data-ttu-id="ee90d-191">Ordner auflisten/Daten lesen, Ordner erstellen/Daten anfügen</span><span class="sxs-lookup"><span data-stu-id="ee90d-191">List folder/read data, create folders/append data</span></span></p></td>
        <td align="left"><p><span data-ttu-id="ee90d-192">Nur diesen Ordner</span><span class="sxs-lookup"><span data-stu-id="ee90d-192">This folder only</span></span></p></td>
        </tr>
        </tbody>
        </table>

         

**<span data-ttu-id="ee90d-193">Sicherheitshinweis:</span><span class="sxs-lookup"><span data-stu-id="ee90d-193">Security Note:</span></span>**

<span data-ttu-id="ee90d-194">Wenn Sie die Speicherfreigabe für Einstellungen auf einem Computer erstellen, auf dem ein Windows Server-Betriebssystem ausgeführt wird, konfigurieren Sie UE-V, um zu überprüfen, ob die lokale Gruppe Administratoren oder der aktuelle Benutzer der Besitzer des Ordners ist, in dem die Einstellungs Pakete gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="ee90d-194">If you create the settings storage share on a computer running a Windows Server operating system, configure UE-V to verify that either the local Administrators group or the current user is the owner of the folder where settings packages are stored.</span></span> <span data-ttu-id="ee90d-195">Um diese zusätzliche Sicherheit zu aktivieren, geben Sie diese Einstellung im Windows Server-Registrierungs-Editor an:</span><span class="sxs-lookup"><span data-stu-id="ee90d-195">To enable this additional security, specify this setting in the Windows Server Registry Editor:</span></span>

1.  <span data-ttu-id="ee90d-196">Fügen Sie einen Registrierungsschlüssel " **reg \ _DWORD** " mit dem Namen **"RepositoryOwnerCheckEnabled"** zu **HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\uev\\agent\\configuration**.</span><span class="sxs-lookup"><span data-stu-id="ee90d-196">Add a **REG\_DWORD** registry key named **"RepositoryOwnerCheckEnabled"** to **HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\UEV\\Agent\\Configuration**.</span></span>

2.  <span data-ttu-id="ee90d-197">Stellen Sie den Wert für den Registrierungsschlüssel auf *1 ein*.</span><span class="sxs-lookup"><span data-stu-id="ee90d-197">Set the registry key value to *1*.</span></span>

## <a href="" id="step3"></a><span data-ttu-id="ee90d-198">Schritt 3: Bereitstellen des UE-V 2-Agents</span><span class="sxs-lookup"><span data-stu-id="ee90d-198">Step 3: Deploy the UE-V 2 Agent</span></span>


<span data-ttu-id="ee90d-199">Der UE-V-Agent synchronisiert die Anwendungs-und Windows-Einstellungen zwischen den Computern und Geräten der Benutzer.</span><span class="sxs-lookup"><span data-stu-id="ee90d-199">The UE-V Agent synchronizes application and Windows settings between users’ computers and devices.</span></span> <span data-ttu-id="ee90d-200">Installieren Sie den Agenten zu Evaluierungszwecken auf mindestens zwei Computern in Ihrer Testumgebung, die demselben Benutzer gehören.</span><span class="sxs-lookup"><span data-stu-id="ee90d-200">For evaluation purposes, install the agent on at least two computers in your test environment that belong to the same user.</span></span>

<span data-ttu-id="ee90d-201">Führen Sie die AgentSetup.exe-Datei über die Befehlszeile aus, um den UE-V-Agent zu installieren.</span><span class="sxs-lookup"><span data-stu-id="ee90d-201">Run the AgentSetup.exe file from the command line to install the UE-V Agent.</span></span> <span data-ttu-id="ee90d-202">Sie wird sowohl auf 32-Bit-als auch 64-Bit-Betriebssystemen installiert.</span><span class="sxs-lookup"><span data-stu-id="ee90d-202">It installs on both 32-bit and 64-bit operating systems.</span></span>

``` syntax
AgentSetup.exe SettingsStoragePath=\\server\settingsshare\%username%
```

<span data-ttu-id="ee90d-203">Sie müssen den SettingsStoragePath-Befehlszeilenparameter als Netzwerkfreigabe aus Schritt 2 angeben.</span><span class="sxs-lookup"><span data-stu-id="ee90d-203">You must specify the SettingsStoragePath command line parameter as the network share from Step 2.</span></span> <span data-ttu-id="ee90d-204">[Bereitstellen eines UE-V-Agents](https://technet.microsoft.com/library/dn458891.aspx#agent) bietet ausführlichere Informationen.</span><span class="sxs-lookup"><span data-stu-id="ee90d-204">[Deploy a UE-V Agent](https://technet.microsoft.com/library/dn458891.aspx#agent) provides more detailed information.</span></span>

## <a href="" id="step4"></a><span data-ttu-id="ee90d-205">Schritt 4: Testen Ihrer UE-V 2-Evaluierungsbereitstellung</span><span class="sxs-lookup"><span data-stu-id="ee90d-205">Step 4: Test Your UE-V 2 Evaluation Deployment</span></span>


<span data-ttu-id="ee90d-206">Sie können jetzt einige Tests für Ihre UE-v-Evaluierungsbereitstellung ausführen, um zu sehen, wie UE-v funktioniert.</span><span class="sxs-lookup"><span data-stu-id="ee90d-206">You can now run a few tests on your UE-V evaluation deployment to see how UE-V works.</span></span>

****

1.  <span data-ttu-id="ee90d-207">Führen Sie auf dem ersten Computer (Computer A) eine oder mehrere der folgenden Änderungen aus:</span><span class="sxs-lookup"><span data-stu-id="ee90d-207">On the first computer (Computer A), make one or more of these changes:</span></span>

    1.  <span data-ttu-id="ee90d-208">Öffnen Sie den Windows-Desktop, und verschieben Sie die Taskleiste an eine andere Position im Fenster.</span><span class="sxs-lookup"><span data-stu-id="ee90d-208">Open to Windows Desktop and move the taskbar to a different location in the window.</span></span>

    2.  <span data-ttu-id="ee90d-209">Ändern Sie die Standardschriftarten.</span><span class="sxs-lookup"><span data-stu-id="ee90d-209">Change the default fonts.</span></span>

    3.  <span data-ttu-id="ee90d-210">Öffnen Sie Calculator, und setzen Sie den Wert auf **Scientific**.</span><span class="sxs-lookup"><span data-stu-id="ee90d-210">Open Calculator and set to **scientific**.</span></span>

    4.  <span data-ttu-id="ee90d-211">Ändern Sie das Verhalten einer beliebigen Windows-APP, wie in Verwalten von Einstellungen für den [Standort "UE-V 2. x" mithilfe von Windows PowerShell und WMI](managing-ue-v-2x-settings-location-templates-using-windows-powershell-and-wmi-both-uevv2.md)erläutert.</span><span class="sxs-lookup"><span data-stu-id="ee90d-211">Change the behavior of any Windows app, as detailed in [Managing UE-V 2.x Settings Location Templates Using Windows PowerShell and WMI](managing-ue-v-2x-settings-location-templates-using-windows-powershell-and-wmi-both-uevv2.md).</span></span>

    5.  <span data-ttu-id="ee90d-212">Deaktivieren Sie die Einstellungen für die Synchronisierung und das Roaming von Microsoft-Konten.</span><span class="sxs-lookup"><span data-stu-id="ee90d-212">Disable Microsoft Account settings synchronization and Roaming Profiles.</span></span>

2.  <span data-ttu-id="ee90d-213">Abmelden Computer a. die Einstellungen werden in einem UE-V-Einstellungspaket gespeichert, wenn Benutzer eine Anwendung sperren, abmelden, beenden oder wenn der Synchronisierungsanbieter ausgeführt wird (standardmäßig alle 30 Minuten).</span><span class="sxs-lookup"><span data-stu-id="ee90d-213">Log off Computer A. Settings are saved in a UE-V settings package when users lock, logoff, exit an application, or when the sync provider runs (every 30 minutes by default).</span></span>

3.  <span data-ttu-id="ee90d-214">Melden Sie sich beim zweiten Computer (Computer B) als derselbe Benutzer wie Computer A an.</span><span class="sxs-lookup"><span data-stu-id="ee90d-214">Log in to the second computer (Computer B) as the same user as Computer A.</span></span>

4.  <span data-ttu-id="ee90d-215">Öffnen Sie den Windows-Desktop, und überprüfen Sie, ob der Speicherort der Taskleiste mit dem von Computer A übereinstimmt. Überprüfen Sie, ob die Standardschriftarten übereinstimmen und dieser Rechner auf **Scientific**festgesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="ee90d-215">Open to Windows Desktop and verify that the taskbar location matches that of Computer A. Verify that the default fonts match and that Calculator is set to **scientific**.</span></span> <span data-ttu-id="ee90d-216">Überprüfen Sie auch die Änderung, die Sie an einer beliebigen Windows-App vorgenommen haben.</span><span class="sxs-lookup"><span data-stu-id="ee90d-216">Also verify the change you made to any Windows app.</span></span>

<span data-ttu-id="ee90d-217">Sie können die Einstellungen auf dem Computer B wieder auf den ursprünglichen Computer ändern.</span><span class="sxs-lookup"><span data-stu-id="ee90d-217">You can change the settings in Computer B back to the original Computer A settings.</span></span> <span data-ttu-id="ee90d-218">Melden Sie sich dann bei Computer B ab, und melden Sie sich bei Computer a an, um die Änderungen zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="ee90d-218">Then log off Computer B and log in to Computer A to verify the changes.</span></span>

## <span data-ttu-id="ee90d-219">Weitere Ressourcen für dieses Produkt</span><span class="sxs-lookup"><span data-stu-id="ee90d-219">Other resources for this product</span></span>


-   [<span data-ttu-id="ee90d-220">Microsoft User Experience Virtualization (UE-V) 2. x</span><span class="sxs-lookup"><span data-stu-id="ee90d-220">Microsoft User Experience Virtualization (UE-V) 2.x</span></span>](index.md)

-   [<span data-ttu-id="ee90d-221">Vorbereiten einer UE-V 2. x-Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="ee90d-221">Prepare a UE-V 2.x Deployment</span></span>](prepare-a-ue-v-2x-deployment-new-uevv2.md)

-   [<span data-ttu-id="ee90d-222">Verwalten von UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="ee90d-222">Administering UE-V 2.x</span></span>](administering-ue-v-2x-new-uevv2.md)

-   [<span data-ttu-id="ee90d-223">Problembehandlung bei UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="ee90d-223">Troubleshooting UE-V 2.x</span></span>](troubleshooting-ue-v-2x-both-uevv2.md)

-   [<span data-ttu-id="ee90d-224">Technische Referenz für UE-V 2.x</span><span class="sxs-lookup"><span data-stu-id="ee90d-224">Technical Reference for UE-V 2.x</span></span>](technical-reference-for-ue-v-2x-both-uevv2.md)






 

 





