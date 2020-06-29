---
title: Konfigurieren von MBAM 2.5 Serverfunktionen mithilfe von Windows PowerShell
description: Konfigurieren von MBAM 2.5 Serverfunktionen mithilfe von Windows PowerShell
author: dansimp
ms.assetid: 826429fd-29bb-44be-b47e-5f5c7d20dd1d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: f350a9eb96a20f50644cfdc1965b7f72741a2c29
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809595"
---
# <span data-ttu-id="9e06a-103">Konfigurieren von MBAM 2.5 Serverfunktionen mithilfe von Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="9e06a-103">Configuring MBAM 2.5 Server Features by Using Windows PowerShell</span></span>


<span data-ttu-id="9e06a-104">Nachdem Sie die MBAM 2,5-Server Software installiert haben, können Sie mithilfe von Windows PowerShell-Cmdlets oder dem MBAM-Serverkonfigurations-Assistenten MBAM 2,5-Server Features konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="9e06a-104">After you install the MBAM 2.5 Server software, you can use configure MBAM 2.5 Server features by using Windows PowerShell cmdlets or the MBAM Server Configuration wizard.</span></span> <span data-ttu-id="9e06a-105">In diesem Thema wird beschrieben, wie Sie MBAM 2,5 mithilfe der Windows PowerShell-Cmdlets konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="9e06a-105">This topic describes how to configure MBAM 2.5 by using the Windows PowerShell cmdlets.</span></span> <span data-ttu-id="9e06a-106">Informationen zum Verwenden des Assistenten finden Sie unter [Konfigurieren der MBAM 2,5-Server Features](configuring-the-mbam-25-server-features.md).</span><span class="sxs-lookup"><span data-stu-id="9e06a-106">To use the wizard instead, see [Configuring the MBAM 2.5 Server Features](configuring-the-mbam-25-server-features.md).</span></span>

## <span data-ttu-id="9e06a-107">Inhalt dieses Themas</span><span class="sxs-lookup"><span data-stu-id="9e06a-107">In this topic</span></span>


<span data-ttu-id="9e06a-108">Dieses Thema enthält die folgenden Informationen zur Verwendung von Windows PowerShell zum Konfigurieren von MBAM:</span><span class="sxs-lookup"><span data-stu-id="9e06a-108">This topic includes the following information about using Windows PowerShell to configure MBAM:</span></span>

-   [<span data-ttu-id="9e06a-109">Laden der Windows PowerShell-Hilfe für MBAM 2,5</span><span class="sxs-lookup"><span data-stu-id="9e06a-109">How to load Windows PowerShell Help for MBAM 2.5</span></span>](#bkmk-load-posh-help)

-   [<span data-ttu-id="9e06a-110">So erhalten Sie Hilfe zu einem MBAM Windows PowerShell-Cmdlet</span><span class="sxs-lookup"><span data-stu-id="9e06a-110">How to get Help about an MBAM Windows PowerShell cmdlet</span></span>](#bkmk-help-specific-cmdlet)

-   [<span data-ttu-id="9e06a-111">Konfigurationen, die Sie nur mit Windows PowerShell ausführen können, aber nicht mit dem Serverkonfigurations-Assistenten von MBAM</span><span class="sxs-lookup"><span data-stu-id="9e06a-111">Configurations that you can do only with Windows PowerShell but not with the MBAM Server Configuration wizard</span></span>](#bkmk-config-only-posh)

-   [<span data-ttu-id="9e06a-112">Voraussetzungen und Voraussetzungen für die Verwendung von Windows PowerShell zum Konfigurieren von MBAM-Server Features</span><span class="sxs-lookup"><span data-stu-id="9e06a-112">Prerequisites and requirements for using Windows PowerShell to configure MBAM Server features</span></span>](#bkmk-prereqs-posh-mbamsvr)

-   [<span data-ttu-id="9e06a-113">Verwenden von Windows PowerShell zum Konfigurieren von MBAM auf einem Remotecomputer</span><span class="sxs-lookup"><span data-stu-id="9e06a-113">Using Windows PowerShell to configure MBAM on a remote computer</span></span>](#bkmk-remote-config)

-   [<span data-ttu-id="9e06a-114">Erforderliche Konten und entsprechende Windows PowerShell-Cmdlet-Parameter</span><span class="sxs-lookup"><span data-stu-id="9e06a-114">Required accounts and corresponding Windows PowerShell cmdlet parameters</span></span>](#bkmk-reqd-posh-accts)

<span data-ttu-id="9e06a-115">Informationen zu den Windows PowerShell-Cmdlets " **Get-MbamBitLockerRecoveryKey** " und " **Get-MbamTPMOwnerPassword** ", die für die Verwaltung von MBAM verwendet werden, finden Sie unter [Verwenden von Windows PowerShell zum Verwalten von MBAM 2,5](using-windows-powershell-to-administer-mbam-25.md).</span><span class="sxs-lookup"><span data-stu-id="9e06a-115">For information about the **Get-MbamBitLockerRecoveryKey** and **Get-MbamTPMOwnerPassword** Windows PowerShell cmdlets, which are used to administer MBAM, see [Using Windows PowerShell to Administer MBAM 2.5](using-windows-powershell-to-administer-mbam-25.md).</span></span>

## <a href="" id="bkmk-load-posh-help"></a><span data-ttu-id="9e06a-116">Laden der Windows PowerShell-Hilfe für MBAM 2,5</span><span class="sxs-lookup"><span data-stu-id="9e06a-116">How to load Windows PowerShell Help for MBAM 2.5</span></span>


<span data-ttu-id="9e06a-117">Eine Liste der Windows PowerShell-Cmdlets auf TechNet finden Sie unter [Automatisierung des Microsoft-Desktop Optimierungs Pakets mit Windows PowerShell](https://go.microsoft.com/fwlink/?LinkId=392816).</span><span class="sxs-lookup"><span data-stu-id="9e06a-117">For a list of the Windows PowerShell cmdlets on TechNet, see [Microsoft Desktop Optimization Pack Automation with Windows PowerShell](https://go.microsoft.com/fwlink/?LinkId=392816).</span></span>

**<span data-ttu-id="9e06a-118">So laden Sie die MBAM 2,5-Hilfe für Windows PowerShell-Cmdlets nach der Installation der MBAM-Server Software</span><span class="sxs-lookup"><span data-stu-id="9e06a-118">To load the MBAM 2.5 Help for Windows PowerShell cmdlets after installing the MBAM Server software</span></span>**

1.  <span data-ttu-id="9e06a-119">Öffnen Sie Windows PowerShell oder Windows PowerShell Integrated Scripting Environment (ISE).</span><span class="sxs-lookup"><span data-stu-id="9e06a-119">Open Windows PowerShell or Windows PowerShell Integrated Scripting Environment (ISE).</span></span>

2.  <span data-ttu-id="9e06a-120">Geben Sie **Update-Help-Module Microsoft. MBAM**.</span><span class="sxs-lookup"><span data-stu-id="9e06a-120">Type **Update-Help –Module Microsoft.MBAM**.</span></span>

## <a href="" id="bkmk-help-specific-cmdlet"></a><span data-ttu-id="9e06a-121">So erhalten Sie Hilfe zu einem MBAM Windows PowerShell-Cmdlet</span><span class="sxs-lookup"><span data-stu-id="9e06a-121">How to get Help about an MBAM Windows PowerShell cmdlet</span></span>


<span data-ttu-id="9e06a-122">Die Windows PowerShell-Hilfe für MBAM ist in den folgenden Formaten verfügbar:</span><span class="sxs-lookup"><span data-stu-id="9e06a-122">Windows PowerShell Help for MBAM is available in the following formats:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="9e06a-123">Windows PowerShell-Hilfeformat</span><span class="sxs-lookup"><span data-stu-id="9e06a-123">Windows PowerShell Help format</span></span></th>
<th align="left"><span data-ttu-id="9e06a-124">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="9e06a-124">More information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9e06a-125">Geben Sie an einer Windows PowerShell-Eingabeaufforderung <strong> Get-Help- </strong> &lt; <em> Cmdlet ein.</em>&gt;</span><span class="sxs-lookup"><span data-stu-id="9e06a-125">At a Windows PowerShell command prompt, type <strong>Get-Help</strong> &lt;<em>cmdlet</em>&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e06a-126">Wenn Sie die neuesten Windows PowerShell-Cmdlets hochladen möchten, befolgen Sie die Anweisungen im vorherigen Abschnitt zum Laden der Windows PowerShell-Hilfe für MBAM.</span><span class="sxs-lookup"><span data-stu-id="9e06a-126">To upload the latest Windows PowerShell cmdlets, follow the instructions in the previous section on how to load Windows PowerShell Help for MBAM.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9e06a-127">Auf TechNet als Webseiten</span><span class="sxs-lookup"><span data-stu-id="9e06a-127">On TechNet as webpages</span></span></p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=393498" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=393498">https://go.microsoft.com/fwlink/?LinkId=393498</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9e06a-128">Im Download Center als Word. docx-Datei</span><span class="sxs-lookup"><span data-stu-id="9e06a-128">On the Download Center as a Word .docx file</span></span></p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=393497" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=393497">https://go.microsoft.com/fwlink/?LinkId=393497</a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9e06a-129">Im Download Center als PDF-Datei</span><span class="sxs-lookup"><span data-stu-id="9e06a-129">On the Download Center as a .pdf file</span></span></p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=393499" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=393499">https://go.microsoft.com/fwlink/?LinkId=393499</a></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-config-only-posh"></a><span data-ttu-id="9e06a-130">Konfigurationen, die Sie nur mit Windows PowerShell ausführen können, aber nicht mit dem Serverkonfigurations-Assistenten von MBAM</span><span class="sxs-lookup"><span data-stu-id="9e06a-130">Configurations that you can do only with Windows PowerShell but not with the MBAM Server Configuration wizard</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="9e06a-131">Konfigurationen, die nur mithilfe von Windows PowerShell möglich sind</span><span class="sxs-lookup"><span data-stu-id="9e06a-131">Configurations that you can do only by using Windows PowerShell</span></span></th>
<th align="left"><span data-ttu-id="9e06a-132">Details</span><span class="sxs-lookup"><span data-stu-id="9e06a-132">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9e06a-133">Installieren Sie die Webdienste auf einem anderen Computer als die Webanwendungen.</span><span class="sxs-lookup"><span data-stu-id="9e06a-133">Install the web services on a separate computer from the web applications.</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e06a-134">Sie müssen die Webdienste und Webanwendungen mithilfe des Assistenten auf demselben Computer installieren.</span><span class="sxs-lookup"><span data-stu-id="9e06a-134">Using the wizard, you must install the web services and web applications on the same computer.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9e06a-135">Aktivieren Sie Berichte auf einem separaten Reporting Services-Punkt, ohne alle Configuration Manager-Objekte zu installieren.</span><span class="sxs-lookup"><span data-stu-id="9e06a-135">Enable reports on a separate reporting services point without installing all of the Configuration Manager objects.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9e06a-136">Löschen Sie alle Objekte aus Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="9e06a-136">Delete all of the objects from Configuration Manager.</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e06a-137">Wenn Sie die Objekte löschen, werden alle Kompatibilitätsdaten aus Configuration Manager gelöscht.</span><span class="sxs-lookup"><span data-stu-id="9e06a-137">Deleting the objects in turn deletes all of the compliance data from Configuration Manager.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9e06a-138">Geben Sie eine benutzerdefinierte Verbindungszeichenfolge für die Datenbanken ein.</span><span class="sxs-lookup"><span data-stu-id="9e06a-138">Enter a custom connection string for the databases.</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e06a-139">Beispiel: Wenn Sie die Webanwendungen so konfigurieren möchten, dass Sie mit der Spiegelung arbeiten, müssen Sie das <strong> Cmdlet Enable-MbamWebApplication verwenden </strong> , um die entsprechende Failover-Partner-Syntax in der Verbindungszeichenfolge anzugeben.</span><span class="sxs-lookup"><span data-stu-id="9e06a-139">Example: To configure the web applications to work with mirroring, you must use the <strong>Enable-MbamWebApplication</strong> cmdlet to specify the appropriate failover partner syntax in the connection string.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9e06a-140">Überspringen Sie die Validierung, und konfigurieren Sie ein Feature, obwohl die Voraussetzungen nicht überprüft wurden.</span><span class="sxs-lookup"><span data-stu-id="9e06a-140">Skip validation and configure a feature even though the prerequisite check failed.</span></span></p></td>
<td align="left"></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="9e06a-141">**Hinweis**  Sie können die MBAM-Datenbanken mit einem Windows PowerShell-Cmdlet oder dem Serverkonfigurations-Assistenten für MBAM nicht deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="9e06a-141">**Note** You cannot disable the MBAM databases with a Windows PowerShell cmdlet or the MBAM Server Configuration wizard.</span></span> <span data-ttu-id="9e06a-142">Um zu verhindern, dass Ihre Konformitäts-und Überwachungsdaten versehentlich entfernt werden, müssen Datenbankadministratoren Datenbanken manuell entfernen.</span><span class="sxs-lookup"><span data-stu-id="9e06a-142">To prevent the accidental removal of your compliance and audit data, database administrators must remove databases manually.</span></span>

 

## <a href="" id="bkmk-prereqs-posh-mbamsvr"></a><span data-ttu-id="9e06a-143">Voraussetzungen und Voraussetzungen für die Verwendung von Windows PowerShell zum Konfigurieren von MBAM-Server Features</span><span class="sxs-lookup"><span data-stu-id="9e06a-143">Prerequisites and requirements for using Windows PowerShell to configure MBAM Server features</span></span>


<span data-ttu-id="9e06a-144">Bevor Sie mit der Konfiguration beginnen, führen Sie die folgenden Voraussetzungen aus.</span><span class="sxs-lookup"><span data-stu-id="9e06a-144">Before starting the configuration, complete the following prerequisites.</span></span>

**<span data-ttu-id="9e06a-145">Kontobezogene Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="9e06a-145">Account-related prerequisites</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="9e06a-146">Voraussetzung</span><span class="sxs-lookup"><span data-stu-id="9e06a-146">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="9e06a-147">Details oder weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="9e06a-147">Details or additional information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9e06a-148">Erstellen Sie die erforderlichen Konten.</span><span class="sxs-lookup"><span data-stu-id="9e06a-148">Create the required accounts.</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e06a-149">Weitere Informationen finden Sie <strong> </strong> weiter unten in diesem Thema unter Abschnitt erforderliche Konten und entsprechende Windows PowerShell-Cmdlet-Parameter.</span><span class="sxs-lookup"><span data-stu-id="9e06a-149">See section <strong>Required accounts and corresponding Windows PowerShell cmdlet parameters</strong> later in this topic.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9e06a-150">Benutzerkonten und Gruppen, die Sie als Parameter an die Windows PowerShell-Cmdlets übergeben, müssen gültige Konten in der Domäne sein.</span><span class="sxs-lookup"><span data-stu-id="9e06a-150">User accounts and groups that you pass as parameters to the Windows PowerShell cmdlets must be valid accounts in the domain.</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e06a-151">Sie können keine lokalen Konten verwenden.</span><span class="sxs-lookup"><span data-stu-id="9e06a-151">You cannot use local accounts.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9e06a-152">Geben Sie Konten im Format der untergeordneten Ebene an.</span><span class="sxs-lookup"><span data-stu-id="9e06a-152">Specify accounts in the down-level format.</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e06a-153">Beispiele:</span><span class="sxs-lookup"><span data-stu-id="9e06a-153">Examples:</span></span></p>
<p><span data-ttu-id="9e06a-154">domainNetBiosName\userdomainNetBiosName\group</span><span class="sxs-lookup"><span data-stu-id="9e06a-154">domainNetBiosName\userdomainNetBiosName\group</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="9e06a-155">Berechtigungsbezogene Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="9e06a-155">Permission-related prerequisites</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="9e06a-156">Voraussetzung</span><span class="sxs-lookup"><span data-stu-id="9e06a-156">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="9e06a-157">Details oder weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="9e06a-157">Details or additional information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9e06a-158">Sie müssen ein Administrator auf dem lokalen Computer sein, auf dem Sie das MBAM-Feature konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="9e06a-158">You must be an administrator on the local computer where you are configuring the MBAM feature.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9e06a-159">Verwenden Sie eine erweiterte Windows PowerShell-Eingabeaufforderung, um alle Windows PowerShell-Cmdlets auszuführen.</span><span class="sxs-lookup"><span data-stu-id="9e06a-159">Use an elevated Windows PowerShell command prompt to run all Windows PowerShell cmdlets.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9e06a-160">Nur für das <strong> Cmdlet Enable-MbamDatabase </strong> :</span><span class="sxs-lookup"><span data-stu-id="9e06a-160">For the <strong>Enable-MbamDatabase</strong> cmdlet only:</span></span></p>
<p><span data-ttu-id="9e06a-161">Sie müssen &quot; über CREATE ANY DATABASE &quot; -Berechtigungen für die Instanz der Microsoft SQL Server-Zieldatenbank verfügen.</span><span class="sxs-lookup"><span data-stu-id="9e06a-161">You must have &quot;create any database&quot; permissions on the instance of the target Microsoft SQL Server database.</span></span></p>
<p><span data-ttu-id="9e06a-162">Dieses Benutzerkonto muss Teil der lokalen Gruppe Administratoren oder der Gruppe Sicherungs-Operatoren sein, um den VSS-Writer (MBAM Volume Shadow Copy Service) registrieren zu können.</span><span class="sxs-lookup"><span data-stu-id="9e06a-162">This user account must be a part of the local administrators group or the Backup Operators group to register the MBAM Volume Shadow Copy Service (VSS) Writer.</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e06a-163">Standardmäßig verfügt der Datenbankadministrator oder System Administrator über die erforderlichen &quot; CREATE ANY DATABASE- &quot; Berechtigungen.</span><span class="sxs-lookup"><span data-stu-id="9e06a-163">By default, the database administrator or system administrator has the required &quot;create any database&quot; permissions.</span></span></p>
<p></p>
<p><span data-ttu-id="9e06a-164">Weitere Informationen zu VSS Writer finden Sie unter <a href="https://go.microsoft.com/fwlink/?LinkId=392814" data-raw-source="[Volume Shadow Copy Service](https://go.microsoft.com/fwlink/?LinkId=392814)"> Volumeschattenkopie-Dienst </a> .</span><span class="sxs-lookup"><span data-stu-id="9e06a-164">For more information about VSS Writer, see <a href="https://go.microsoft.com/fwlink/?LinkId=392814" data-raw-source="[Volume Shadow Copy Service](https://go.microsoft.com/fwlink/?LinkId=392814)">Volume Shadow Copy Service</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9e06a-165">Nur für das <strong> System Center Configuration Manager-Integrations </strong> Feature:</span><span class="sxs-lookup"><span data-stu-id="9e06a-165">For the <strong>System Center Configuration Manager Integration</strong> feature only:</span></span></p>
<p><span data-ttu-id="9e06a-166">Der Benutzer, der dieses Feature aktiviert, muss über diese Rechte in Configuration Manager verfügen:</span><span class="sxs-lookup"><span data-stu-id="9e06a-166">The user who enables this feature must have these rights in Configuration Manager:</span></span></p></td>
<td align="left"><table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="9e06a-167">Art der Rechte in Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="9e06a-167">Type of rights in Configuration Manager</span></span></th>
<th align="left"><span data-ttu-id="9e06a-168">Erforderliche Rechte</span><span class="sxs-lookup"><span data-stu-id="9e06a-168">Required rights</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9e06a-169">Configuration Manager-Website Rechte:</span><span class="sxs-lookup"><span data-stu-id="9e06a-169">Configuration Manager Site rights:</span></span></p></td>
<td align="left"><p>- <span data-ttu-id="9e06a-170">Lesen</span><span class="sxs-lookup"><span data-stu-id="9e06a-170">Read</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9e06a-171">Sammlungs Rechte für Configuration Manager:</span><span class="sxs-lookup"><span data-stu-id="9e06a-171">Configuration Manager Collection rights:</span></span></p></td>
<td align="left"><p>- <span data-ttu-id="9e06a-172">Erstellen – Löschen – lesen – ändern – Bereitstellen von Konfigurationselementen</span><span class="sxs-lookup"><span data-stu-id="9e06a-172">Create- Delete- Read- Modify- Deploy Configuration Items</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9e06a-173">Configuration Manager-Konfigurationselement Rechte:</span><span class="sxs-lookup"><span data-stu-id="9e06a-173">Configuration Manager Configuration item rights:</span></span></p></td>
<td align="left"><p>- <span data-ttu-id="9e06a-174">Erstellen-Löschen-lesen</span><span class="sxs-lookup"><span data-stu-id="9e06a-174">Create- Delete- Read</span></span></p></td>
</tr>
</tbody>
</table>
<p> </p>
<p></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-remote-config"></a><span data-ttu-id="9e06a-175">Verwenden von Windows PowerShell zum Konfigurieren von MBAM auf einem Remotecomputer</span><span class="sxs-lookup"><span data-stu-id="9e06a-175">Using Windows PowerShell to configure MBAM on a remote computer</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="9e06a-176">Verwendung dieser Funktion</span><span class="sxs-lookup"><span data-stu-id="9e06a-176">When to use this capability</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="9e06a-177">Wenn Sie die MBAM 2,5-Server Features auf einem Remotecomputer konfigurieren möchten.</span><span class="sxs-lookup"><span data-stu-id="9e06a-177">When you want to configure the MBAM 2.5 Server features on a remote computer.</span></span> <span data-ttu-id="9e06a-178">Die Windows PowerShell-Cmdlets werden auf einem Computer ausgeführt, und Sie konfigurieren die Features auf einem anderen Remotecomputer.</span><span class="sxs-lookup"><span data-stu-id="9e06a-178">The Windows PowerShell cmdlets are running on one computer, and you are configuring the features on a different, remote computer.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="9e06a-179">Was Sie tun müssen</span><span class="sxs-lookup"><span data-stu-id="9e06a-179">What you have to do</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="9e06a-180">Wenn Sie Windows PowerShell zum Konfigurieren der MBAM 2,5-Server Features auf einem Remotecomputer verwenden möchten, müssen Sie Folgendes ausführen:</span><span class="sxs-lookup"><span data-stu-id="9e06a-180">To use Windows PowerShell to configure MBAM 2.5 Server features on a remote computer, you must:</span></span></p>
<ul>
<li><p><span data-ttu-id="9e06a-181">Stellen Sie sicher, dass die MBAM 2,5-Server Software auf dem Remotecomputer installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="9e06a-181">Ensure that the MBAM 2.5 Server software has been installed on the remote computer.</span></span></p></li>
<li><p><span data-ttu-id="9e06a-182">Verwenden Sie das CredSSP-Protokoll (Credential Security Support Provider), um die Windows PowerShell-Sitzung zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="9e06a-182">Use the Credential Security Support Provider (CredSSP) Protocol to open the Windows PowerShell session.</span></span></p></li>
<li><p><span data-ttu-id="9e06a-183">Aktivieren Sie die Windows-Remote Verwaltung (WinRM).</span><span class="sxs-lookup"><span data-stu-id="9e06a-183">Enable Windows Remote Management (WinRM).</span></span> <span data-ttu-id="9e06a-184">Wenn Sie WinRM nicht aktivieren und richtig konfigurieren, <strong> </strong> zeigt das in dieser Tabelle beschriebene Cmdlet New-PSSession einen Fehler an, und es wird beschrieben, wie Sie das Problem beheben können.</span><span class="sxs-lookup"><span data-stu-id="9e06a-184">If you fail to enable WinRM and to configure it correctly, the <strong>New-PSSession</strong> cmdlet that is described in this table displays an error and describes how to fix the issue.</span></span> <span data-ttu-id="9e06a-185">Weitere Informationen zu WinRM finden Sie unter <a href="https://go.microsoft.com/fwlink/?LinkId=393064" data-raw-source="[Using Windows Remote Management](https://go.microsoft.com/fwlink/?LinkId=393064)"> Verwenden der Windows-Remote Verwaltung </a> .</span><span class="sxs-lookup"><span data-stu-id="9e06a-185">For more information about WinRM, see <a href="https://go.microsoft.com/fwlink/?LinkId=393064" data-raw-source="[Using Windows Remote Management](https://go.microsoft.com/fwlink/?LinkId=393064)">Using Windows Remote Management</a>.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="9e06a-186">Warum müssen Sie das tun?</span><span class="sxs-lookup"><span data-stu-id="9e06a-186">Why you have to do it</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="9e06a-187">Dieses Protokoll ermöglicht es den Windows PowerShell-Cmdlets, mithilfe der administrativen Anmeldeinformationen des Benutzers eine Verbindung mit Active Directory-Domänendiensten herzustellen.</span><span class="sxs-lookup"><span data-stu-id="9e06a-187">This protocol enables the Windows PowerShell cmdlets to connect to Active Directory Domain Services by using the user’s administrative credentials.</span></span> <span data-ttu-id="9e06a-188">Möglicherweise erhalten Sie einen Überprüfungsfehler, wenn Sie die Windows PowerShell-Sitzung ohne dieses Protokoll starten.</span><span class="sxs-lookup"><span data-stu-id="9e06a-188">You might get a validation error if you start the Windows PowerShell session without this protocol.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="9e06a-189">Starten einer Windows PowerShell-Sitzung mit dem CredSSP-Protokoll</span><span class="sxs-lookup"><span data-stu-id="9e06a-189">How to start a Windows PowerShell session with the CredSSP protocol</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="9e06a-190">Geben Sie den folgenden Code an der Windows PowerShell-Eingabeaufforderung ein:</span><span class="sxs-lookup"><span data-stu-id="9e06a-190">Type the following code at the Windows PowerShell prompt:</span></span></p>
<p><code>$s = New-PSSession -ComputerName xxx -Authentication Credssp -Credential xxx</code></p>
<p><span data-ttu-id="9e06a-191">Der folgende Code zeigt ein Beispiel.</span><span class="sxs-lookup"><span data-stu-id="9e06a-191">The following code shows an example.</span></span></p>
<p><code>$session = New-PSSession -ComputerName &lt;MBAM_server_name&gt; -Authentication Credssp -Credential (Get-Credential)</code></p>
<p><code>Enter-PSSession $session</code></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-reqd-posh-accts"></a><span data-ttu-id="9e06a-192">Erforderliche Konten und entsprechende Windows PowerShell-Cmdlet-Parameter</span><span class="sxs-lookup"><span data-stu-id="9e06a-192">Required accounts and corresponding Windows PowerShell cmdlet parameters</span></span>


<span data-ttu-id="9e06a-193">In der folgenden Tabelle werden die Konten beschrieben, die für die Konfiguration der MBAM 2,5-Server Features erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="9e06a-193">The following table describes the accounts that are required to configure MBAM 2.5 Server features.</span></span> <span data-ttu-id="9e06a-194">Außerdem werden das entsprechende Windows PowerShell-Cmdlet und der zugehörige Parameter aufgelistet, für die Sie das Konto während der Konfiguration angeben müssen.</span><span class="sxs-lookup"><span data-stu-id="9e06a-194">It also lists the corresponding Windows PowerShell cmdlet and parameter for which you have to specify the account during configuration.</span></span>

<span data-ttu-id="9e06a-195">Cmdlet-Parametertyp (Benutzer oder Gruppe) Description enable-MBAMDatabase</span><span class="sxs-lookup"><span data-stu-id="9e06a-195">Cmdlet Parameter Type (User or Group) Description Enable-MBAMDatabase</span></span>

<span data-ttu-id="9e06a-196">AccessAccount</span><span class="sxs-lookup"><span data-stu-id="9e06a-196">AccessAccount</span></span>

<span data-ttu-id="9e06a-197">Benutzer oder Gruppe</span><span class="sxs-lookup"><span data-stu-id="9e06a-197">User or Group</span></span>

<span data-ttu-id="9e06a-198">Geben Sie einen Domänenbenutzer oder eine Gruppe mit Lese-/Schreibzugriff für diese Datenbank an, damit die Webanwendungen auf Daten und Berichte in dieser Datenbank zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="9e06a-198">Specify a domain user or group that has read/write permission to this database to give the web applications access to data and reports in this database.</span></span> <span data-ttu-id="9e06a-199">Wenn der Wert ein Domänenbenutzer ist, muss der **WebServiceApplicationPoolCredential** -Parameter, der beim Ausführen des Cmdlets **enable-MbamWebApplication** verwendet wird, dasselbe Benutzerkonto verwenden.</span><span class="sxs-lookup"><span data-stu-id="9e06a-199">If the value is a domain user, then the **WebServiceApplicationPoolCredential** parameter that is used when running the **Enable-MbamWebApplication** cmdlet must use the same user account.</span></span> <span data-ttu-id="9e06a-200">Wenn es sich bei dem Wert um eine Domänenbenutzergruppe handelt, muss das vom **WebServiceApplicationPoolCredential** -Parameter verwendete Domänenkonto Mitglied dieser Gruppe sein.</span><span class="sxs-lookup"><span data-stu-id="9e06a-200">If the value is a domain Users group, then the domain account that is used by the **WebServiceApplicationPoolCredential** parameter must be a member of this group.</span></span>

<span data-ttu-id="9e06a-201">ReportAccount</span><span class="sxs-lookup"><span data-stu-id="9e06a-201">ReportAccount</span></span>

<span data-ttu-id="9e06a-202">Benutzer oder Gruppe</span><span class="sxs-lookup"><span data-stu-id="9e06a-202">User or Group</span></span>

<span data-ttu-id="9e06a-203">Geben Sie einen Domänenbenutzer oder eine Benutzergruppe an, die über die Berechtigung "schreibgeschützt" für diese Datenbank verfügt, um dem MBAM-Berichtzugriff auf die Konformitäts-und Überwachungsdaten bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="9e06a-203">Specify a domain user or Users group that has read-only permission to this database to provide the MBAM reports access to the compliance and audit data.</span></span> <span data-ttu-id="9e06a-204">Wenn der Wert ein Domänenbenutzer ist, muss der **ComplianceAndAuditDBCredential** -Parameter des Cmdlets **enable-MbamReport** das gleiche Benutzerkonto verwenden.</span><span class="sxs-lookup"><span data-stu-id="9e06a-204">If the value is a domain user, then the **ComplianceAndAuditDBCredential** parameter of the **Enable-MbamReport** cmdlet must use the same user account.</span></span> <span data-ttu-id="9e06a-205">Wenn es sich bei dem Wert um eine Domänenbenutzergruppe handelt, muss das vom **ComplianceAndAuditDBCredential** -Parameter verwendete Domänenkonto Mitglied dieser Gruppe sein.</span><span class="sxs-lookup"><span data-stu-id="9e06a-205">If the value is a domain Users group, then the domain account that is used by the **ComplianceAndAuditDBCredential** parameter must be a member of this group.</span></span>

<span data-ttu-id="9e06a-206">Enable-MbamReport</span><span class="sxs-lookup"><span data-stu-id="9e06a-206">Enable-MbamReport</span></span>

<span data-ttu-id="9e06a-207">ComplianceAndAuditDBCredential</span><span class="sxs-lookup"><span data-stu-id="9e06a-207">ComplianceAndAuditDBCredential</span></span>

<span data-ttu-id="9e06a-208">Benutzer</span><span class="sxs-lookup"><span data-stu-id="9e06a-208">User</span></span>

<span data-ttu-id="9e06a-209">Gibt die Administratoranmeldeinformationen an, die von der lokalen SSRS-Instanz für die Verbindung mit der MBAM-Konformitäts-und Überwachungsdatenbank verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9e06a-209">Specifies the administrative credential that the local SSRS instance uses to connect to the MBAM Compliance and Audit Database.</span></span> <span data-ttu-id="9e06a-210">Der Domänenbenutzer in den administrativen Anmeldeinformationen muss mit dem Benutzerkonto identisch sein, das für den **ReportAccount** -Parameter verwendet wird, der während der Ausführung des Cmdlets **enable-MbamDatabase** verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9e06a-210">The domain user in the administrative credential must be the same as the user account that is used for the **ReportAccount** parameter, which is used while running the **Enable-MbamDatabase** cmdlet.</span></span> <span data-ttu-id="9e06a-211">Wenn eine Gruppe von Domänenbenutzern mit dem **ReportAccount** -Parameter verwendet wurde, sollte dieses Konto ein Mitglied dieser Gruppe sein.</span><span class="sxs-lookup"><span data-stu-id="9e06a-211">If a domain Users group was used with the **ReportAccount** parameter, this account should be a member of that group.</span></span>

<span data-ttu-id="9e06a-212">**Wichtig**  Das in den administrativen Anmeldeinformationen angegebene Konto sollte über beschränkte Benutzerrechte verfügen, um die Sicherheit zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="9e06a-212">**Important** The account specified in the administrative credentials should have limited user rights for improved security.</span></span> <span data-ttu-id="9e06a-213">Außerdem sollte das Kennwort des Kontos auf nicht ablaufen festgesetzt werden.</span><span class="sxs-lookup"><span data-stu-id="9e06a-213">Also, the password of the account should be set to not expire.</span></span>

 

<span data-ttu-id="9e06a-214">ReportsReadOnlyAccessGroup</span><span class="sxs-lookup"><span data-stu-id="9e06a-214">ReportsReadOnlyAccessGroup</span></span>

<span data-ttu-id="9e06a-215">Gruppe</span><span class="sxs-lookup"><span data-stu-id="9e06a-215">Group</span></span>

<span data-ttu-id="9e06a-216">Gibt die Domänenbenutzergruppe an, die über Leseberechtigungen für die Berichte verfügt.</span><span class="sxs-lookup"><span data-stu-id="9e06a-216">Specifies the domain user group that has read permissions to the reports.</span></span> <span data-ttu-id="9e06a-217">Die angegebene Gruppe muss dieselbe Gruppe sein, die für den **ReportsReadOnlyAccessGroup** -Parameter im Cmdlet **enable-MbamWebApplication** verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9e06a-217">The specified group must be the same group that is used for the **ReportsReadOnlyAccessGroup** parameter in the **Enable-MbamWebApplication** cmdlet.</span></span>

<span data-ttu-id="9e06a-218">Enable-MBAMWebApplication</span><span class="sxs-lookup"><span data-stu-id="9e06a-218">Enable-MBAMWebApplication</span></span>

<span data-ttu-id="9e06a-219">AdvancedHelpdeskAccessGroup</span><span class="sxs-lookup"><span data-stu-id="9e06a-219">AdvancedHelpdeskAccessGroup</span></span>

<span data-ttu-id="9e06a-220">Gruppe</span><span class="sxs-lookup"><span data-stu-id="9e06a-220">Group</span></span>

<span data-ttu-id="9e06a-221">Gibt die Gruppe "Domänenbenutzer" an, die auf alle Bereiche der Verwaltungs-und Überwachungs Website mit Ausnahme des Bereichs "Berichte" zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="9e06a-221">Specifies the domain Users group that has access to all areas of the Administration and Monitoring Website except the Reports area.</span></span>

<span data-ttu-id="9e06a-222">HelpdeskAccessGroup</span><span class="sxs-lookup"><span data-stu-id="9e06a-222">HelpdeskAccessGroup</span></span>

<span data-ttu-id="9e06a-223">Gruppe</span><span class="sxs-lookup"><span data-stu-id="9e06a-223">Group</span></span>

<span data-ttu-id="9e06a-224">Gibt die Gruppe "Domänenbenutzer" an, die Zugriff auf die Bereiche " **TPM verwalten** " und " **Laufwerk Wiederherstellung** " der Website "Verwaltung und Überwachung" hat.</span><span class="sxs-lookup"><span data-stu-id="9e06a-224">Specifies the domain Users group that has access to the **Manage TPM** and **Drive Recovery** areas of the Administration and Monitoring Website.</span></span>

<span data-ttu-id="9e06a-225">ReportsReadOnlyAccessGroup</span><span class="sxs-lookup"><span data-stu-id="9e06a-225">ReportsReadOnlyAccessGroup</span></span>

<span data-ttu-id="9e06a-226">Gruppe</span><span class="sxs-lookup"><span data-stu-id="9e06a-226">Group</span></span>

<span data-ttu-id="9e06a-227">Gibt die Gruppe "Domänenbenutzer" an, die über die Berechtigung "lesen" für den Bereich " **Berichte** " der Website "Verwaltung und Überwachung" verfügt.</span><span class="sxs-lookup"><span data-stu-id="9e06a-227">Specifies the domain Users group that has read permission to the **Reports** area of the Administration and Monitoring Website.</span></span> <span data-ttu-id="9e06a-228">Die angegebene Gruppe muss dieselbe Gruppe sein, die für den **ReportsReadOnlyAccessGroup** -Parameter im Cmdlet **enable-MbamReport** verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9e06a-228">The specified group must be the same group that is used for the **ReportsReadOnlyAccessGroup** parameter in the **Enable-MbamReport** cmdlet.</span></span>

<span data-ttu-id="9e06a-229">WebServiceApplicationPoolCredential</span><span class="sxs-lookup"><span data-stu-id="9e06a-229">WebServiceApplicationPoolCredential</span></span>

<span data-ttu-id="9e06a-230">Benutzer</span><span class="sxs-lookup"><span data-stu-id="9e06a-230">User</span></span>

<span data-ttu-id="9e06a-231">Gibt den Domänenbenutzer an, der vom Anwendungspool für die MBAM-Webanwendungen verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="9e06a-231">Specifies the domain user to be used by the application pool for the MBAM web applications.</span></span> <span data-ttu-id="9e06a-232">Es muss sich um das gleiche Domänenbenutzerkonto handeln, das im **AccessAccount** -Parameter des Cmdlets **enable-MbamDatabase** angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="9e06a-232">It must be the same domain user account that is specified in the **AccessAccount** parameter of the **Enable-MbamDatabase** cmdlet.</span></span> <span data-ttu-id="9e06a-233">Wenn der **AccessAccount** -Parameter beim Ausführen des **enable-MbamDatabase-** Cmdlets eine Domänenbenutzergruppe verwendet hat, muss der hier angegebene Domänenbenutzer ein Mitglied dieser Gruppe sein.</span><span class="sxs-lookup"><span data-stu-id="9e06a-233">If a domain Users group was used by the **AccessAccount** parameter when running the **Enable-MbamDatabase** cmdlet, the domain user that is specified here must be a member of that group.</span></span> <span data-ttu-id="9e06a-234">Wenn Sie die administrativen Anmeldeinformationen nicht angeben, werden die Administratoranmeldeinformationen verwendet, die von einer zuvor aktivierten Webanwendung angegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="9e06a-234">If you do not specify the administrative credentials, the administrative credentials that were specified by any previously enabled web application are used.</span></span> <span data-ttu-id="9e06a-235">Alle Webanwendungen verwenden dieselbe Anwendungspoolidentität.</span><span class="sxs-lookup"><span data-stu-id="9e06a-235">All of the web applications use the same application pool identity.</span></span> <span data-ttu-id="9e06a-236">Wenn Sie mehrmals angegeben wird, wird der zuletzt angegebene Wert verwendet.</span><span class="sxs-lookup"><span data-stu-id="9e06a-236">If it is specified multiple times, the most recently specified value is used.</span></span>

<span data-ttu-id="9e06a-237">**Wichtig**  Um die Sicherheit zu verbessern, legen Sie das in den administrativen Anmeldeinformationen angegebene Konto auf begrenzte Benutzerrechte fest.</span><span class="sxs-lookup"><span data-stu-id="9e06a-237">**Important** For improved security, set the account that is specified in the administrative credentials to limited user rights.</span></span> <span data-ttu-id="9e06a-238">Legen Sie außerdem das Kennwort des Kontos so ein, dass es nie abläuft.</span><span class="sxs-lookup"><span data-stu-id="9e06a-238">Also, set the password of the account to never expire.</span></span> <span data-ttu-id="9e06a-239">Stellen Sie sicher, dass entweder das integrierte IIS \ _IUSRS-Konto oder das Konto, das für den **WebServiceApplicationPoolCredential** -Parameter verwendet wird, zur Einstellung für den **Identitätswechsel zu einem Client nach der Authentifizierungs** lokalen Sicherheit hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="9e06a-239">Ensure that either the built-in IIS\_IUSRS account or the account that is used for the **WebServiceApplicationPoolCredential** parameter has been added to the **Impersonate a client after authentication** local security setting.</span></span>

<span data-ttu-id="9e06a-240">Wenn Sie die lokale Sicherheitseinstellung anzeigen möchten, öffnen Sie den **lokalen Sicherheitsrichtlinien-Editor**, erweitern Sie den Knoten **lokale Richtlinien** , wählen Sie den Knoten **Benutzerrechtezuweisung** aus, und doppelklicken Sie dann im Detailbereich auf die Einstellungen für **Client nach Authentifizierung** und **Anmeldung als Stapelverarbeitungsauftrag** .</span><span class="sxs-lookup"><span data-stu-id="9e06a-240">To view the local security setting, open the **Local Security Policy editor**, expand the **Local Policies** node, select the **User Rights Assignment** node, and then double-click the **Impersonate a client after authentication** and **Log on as a batch job** Group Policy settings in the details pane.</span></span>

 

 




## <span data-ttu-id="9e06a-241">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="9e06a-241">Related topics</span></span>


[<span data-ttu-id="9e06a-242">Konfigurieren der MBAM 2.5-Serverfunktionen</span><span class="sxs-lookup"><span data-stu-id="9e06a-242">Configuring the MBAM 2.5 Server Features</span></span>](configuring-the-mbam-25-server-features.md)

[<span data-ttu-id="9e06a-243">Überprüfen der Konfiguration von MBAM 2.5 Serverfunktionen</span><span class="sxs-lookup"><span data-stu-id="9e06a-243">Validating the MBAM 2.5 Server Feature Configuration</span></span>](validating-the-mbam-25-server-feature-configuration.md)

[<span data-ttu-id="9e06a-244">Verwenden von Windows PowerShell zum Verwalten von MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="9e06a-244">Using Windows PowerShell to Administer MBAM 2.5</span></span>](using-windows-powershell-to-administer-mbam-25.md)

 
## <span data-ttu-id="9e06a-245">Sie haben einen Vorschlag für MBAM?</span><span class="sxs-lookup"><span data-stu-id="9e06a-245">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="9e06a-246">[Hier](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)können Sie Vorschläge hinzufügen oder abstimmen.</span><span class="sxs-lookup"><span data-stu-id="9e06a-246">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="9e06a-247">Bei MBAM-Problemen verwenden Sie das [MBAM TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="9e06a-247">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>
 





