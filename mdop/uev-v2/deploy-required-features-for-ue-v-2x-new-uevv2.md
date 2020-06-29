---
title: Bereitstellen der erforderlichen Features für UE-V 2.x
description: Bereitstellen der erforderlichen Features für UE-V 2.x
author: dansimp
ms.assetid: 10399bb3-cc7b-4578-bc0c-2f6b597abe4d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f2123ec75fb151a8f5b836b9b2522a9d6090b043
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810693"
---
# <span data-ttu-id="223e7-103">Bereitstellen der erforderlichen Features für UE-V 2.x</span><span class="sxs-lookup"><span data-stu-id="223e7-103">Deploy Required Features for UE-V 2.x</span></span>


<span data-ttu-id="223e7-104">Für alle Microsoft User Experience Virtualization (UE-V) 2,0-, 2,1-und 2,1 SP1-Bereitstellungen sind diese Features erforderlich.</span><span class="sxs-lookup"><span data-stu-id="223e7-104">All Microsoft User Experience Virtualization (UE-V) 2.0, 2.1, and 2.1 SP1 deployments require these features</span></span>

-   <span data-ttu-id="223e7-105">[Bereitstellen eines Speicherorts für Einstellungen](#ssl) , auf den Endbenutzer zugreifen können</span><span class="sxs-lookup"><span data-stu-id="223e7-105">[Deploy a Settings Storage Location](#ssl) that is accessible to end users.</span></span>

    <span data-ttu-id="223e7-106">Hierbei handelt es sich um eine standardmäßige Netzwerkfreigabe, die Benutzereinstellungen speichert und abruft.</span><span class="sxs-lookup"><span data-stu-id="223e7-106">This is a standard network share that stores and retrieves user settings.</span></span>

-   [<span data-ttu-id="223e7-107">Auswählen der Konfigurationsmethode für UE-V</span><span class="sxs-lookup"><span data-stu-id="223e7-107">Choose the Configuration Method for UE-V</span></span>](#config)

    <span data-ttu-id="223e7-108">UE-V kann mithilfe allgemeiner Verwaltungstools wie Gruppenrichtlinien, Configuration Manager oder Windows-Verwaltungsinfrastruktur und PowerShell bereitgestellt und konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="223e7-108">UE-V can be deployed and configured using common management tools including group policy, Configuration Manager, or Windows Management Infrastructure and Powershell.</span></span>

-   <span data-ttu-id="223e7-109">[Stellen Sie einen UE-V-Agent bereit](#agent) , der auf jedem Computer installiert werden soll, der die Einstellungen synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="223e7-109">[Deploy a UE-V Agent](#agent) to be installed on every computer that synchronizes settings.</span></span>

    <span data-ttu-id="223e7-110">Damit werden registrierte Anwendungen und das Betriebssystem für alle Einstellungen geändert und die Einstellungen zwischen Computern synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="223e7-110">This monitors registered applications and the operating system for any settings changes and synchronizes those settings between computers.</span></span>

<span data-ttu-id="223e7-111">In den Themen in diesem Abschnitt wird beschrieben, wie diese Features bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="223e7-111">The topics in this section describe how to deploy these features.</span></span>

## <a href="" id="ssl"></a><span data-ttu-id="223e7-112">Bereitstellen eines Speicherorts für UE-V-Einstellungen</span><span class="sxs-lookup"><span data-stu-id="223e7-112">Deploy a UE-V Settings Storage Location</span></span>


<span data-ttu-id="223e7-113">UE-V erfordert einen Speicherort, an dem Benutzereinstellungen in den Einstellungen-Paketdateien gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="223e7-113">UE-V requires a location in which to store user settings in settings package files.</span></span> <span data-ttu-id="223e7-114">Sie können diesen Einstellungs Speicherort auf eine der folgenden Arten konfigurieren:</span><span class="sxs-lookup"><span data-stu-id="223e7-114">You can configure this settings storage location in one of these ways:</span></span>

-   <span data-ttu-id="223e7-115">Erstellen eines eigenen Speicherorts für Einstellungen</span><span class="sxs-lookup"><span data-stu-id="223e7-115">Create your own settings storage location</span></span>

-   <span data-ttu-id="223e7-116">Verwenden des vorhandenen Active Directory für den Speicherort der Einstellungen</span><span class="sxs-lookup"><span data-stu-id="223e7-116">Use existing Active Directory for your settings storage location</span></span>

<span data-ttu-id="223e7-117">Wenn Sie keinen Speicherplatz für Einstellungen erstellen, wird standardmäßig Active Directory (AD) vom UE-V-Agent verwendet.</span><span class="sxs-lookup"><span data-stu-id="223e7-117">If you don’t create a settings storage location, the UE-V Agent will use Active Directory (AD) by default.</span></span>

**<span data-ttu-id="223e7-118">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="223e7-118">Note</span></span>**  
<span data-ttu-id="223e7-119">Im Hinblick auf die [Leistungs-und Kapazitätsplanung](https://technet.microsoft.com/library/dn458932.aspx#capacity) und die Verringerung von Problemen mit der Netzwerklatenz können Sie die Speicherorte für Einstellungen in denselben lokalen Netzwerken erstellen, in denen sich die Computer der Benutzer befinden.</span><span class="sxs-lookup"><span data-stu-id="223e7-119">As a matter of [performance and capacity planning](https://technet.microsoft.com/library/dn458932.aspx#capacity) and to reduce problems with network latency, create settings storage locations on the same local networks where the users’ computers reside.</span></span> <span data-ttu-id="223e7-120">Für den Speicherort der Einstellungen empfehlen wir pro Nutzer 20 MB Speicherplatz.</span><span class="sxs-lookup"><span data-stu-id="223e7-120">We recommend 20 MB of disk space per user for the settings storage location.</span></span>



### <span data-ttu-id="223e7-121">Erstellen eines Speicherorts für UE-V-Einstellungen</span><span class="sxs-lookup"><span data-stu-id="223e7-121">Create a UE-V Settings Storage Location</span></span>

<span data-ttu-id="223e7-122">Vor dem Definieren des Speicherorts für Einstellungen müssen Sie ein Stammverzeichnis mit Lese-/Schreibzugriff für Benutzer erstellen, die die Einstellungen für die Freigabe speichern.</span><span class="sxs-lookup"><span data-stu-id="223e7-122">Before you define the settings storage location, you must create a root directory with read/write permissions for users who store settings on the share.</span></span> <span data-ttu-id="223e7-123">Der UE-V-Agent erstellt benutzerspezifische Ordner unter diesem Stammverzeichnis.</span><span class="sxs-lookup"><span data-stu-id="223e7-123">The UE-V Agent creates user-specific folders under this root directory.</span></span>

<span data-ttu-id="223e7-124">Der Speicherort der Einstellungen wird durch Festlegen der SettingsStoragePath-Konfigurationsoption definiert, die mithilfe einer der folgenden Methoden konfiguriert werden kann:</span><span class="sxs-lookup"><span data-stu-id="223e7-124">The settings storage location is defined by setting the SettingsStoragePath configuration option, which you can configure by using one of these methods:</span></span>

-   <span data-ttu-id="223e7-125">Wenn Sie [den UE-V-Agent](#agent) über einen Befehlszeilenparameter oder in einem Batchskript bereitstellen</span><span class="sxs-lookup"><span data-stu-id="223e7-125">When you [Deploy the UE-V Agent](#agent) through a command-line parameter or in a batch script</span></span>

-   <span data-ttu-id="223e7-126">Über [Gruppenrichtlinien](https://technet.microsoft.com/library/dn458893.aspx) Einstellungen</span><span class="sxs-lookup"><span data-stu-id="223e7-126">Through [Group Policy](https://technet.microsoft.com/library/dn458893.aspx) settings</span></span>

-   <span data-ttu-id="223e7-127">Mit dem [System Center-Konfigurationspaket](https://technet.microsoft.com/library/dn458917.aspx) für UE-V</span><span class="sxs-lookup"><span data-stu-id="223e7-127">With the [System Center Configuration Pack](https://technet.microsoft.com/library/dn458917.aspx) for UE-V</span></span>

-   <span data-ttu-id="223e7-128">Nach der Installation des UE-V-Agents mithilfe von [Windows PowerShell oder Windows-Verwaltungsinstrumentation (WMI)](https://technet.microsoft.com/library/dn458937.aspx)</span><span class="sxs-lookup"><span data-stu-id="223e7-128">After installation of the UE-V Agent, by using [Windows PowerShell or Windows Management Instrumentation (WMI)](https://technet.microsoft.com/library/dn458937.aspx)</span></span>

<span data-ttu-id="223e7-129">Der Pfad muss sich im UNC-Pfad (Universal Naming Convention) des Servers und der Freigabe befinden.</span><span class="sxs-lookup"><span data-stu-id="223e7-129">The path must be in a universal naming convention (UNC) path of the server and share.</span></span> <span data-ttu-id="223e7-130">Beispiel: **\\\\Server\\Settingsshare\\**.</span><span class="sxs-lookup"><span data-stu-id="223e7-130">For example, **\\\\Server\\Settingsshare\\**.</span></span> <span data-ttu-id="223e7-131">Diese Konfigurationsoption unterstützt die Verwendung von Variablen, um bestimmte Synchronisierungsszenarien zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="223e7-131">This configuration option supports the use of variables to enable specific synchronization scenarios.</span></span> <span data-ttu-id="223e7-132">So können Sie beispielsweise die `%username%\%computername%` Variablen verwenden, um die Benutzereinstellungen für Endbenutzer in diesen Szenarien beizubehalten:</span><span class="sxs-lookup"><span data-stu-id="223e7-132">For example, you can use the `%username%\%computername%` variables to preserve the end user settings experience in these scenarios:</span></span>

-   <span data-ttu-id="223e7-133">Endbenutzer, die mehrere physische Computer in Ihrem Unternehmen verwenden</span><span class="sxs-lookup"><span data-stu-id="223e7-133">End users that use multiple physical computers in your enterprise</span></span>

-   <span data-ttu-id="223e7-134">Unternehmens Computer, die von mehreren Endbenutzern verwendet werden</span><span class="sxs-lookup"><span data-stu-id="223e7-134">Enterprise computers that are used by multiple end users</span></span>

<span data-ttu-id="223e7-135">Der UE-V-Agent erstellt dynamisch einen benutzerspezifischen Einstellungsspeicher Pfad mit dem Namen eines versteckten Systemordners `SettingsPackages` basierend auf der Konfigurationseinstellung von **SettingsStoragePath**.</span><span class="sxs-lookup"><span data-stu-id="223e7-135">The UE-V Agent dynamically creates a user-specific settings storage path, with a hidden system folder named `SettingsPackages`, based on the configuration setting of **SettingsStoragePath**.</span></span> <span data-ttu-id="223e7-136">Der Agent liest und schreibt Einstellungen an diesen Speicherort, wie Sie von den registrierten UE-V-Einstellungen für Standort Vorlagen definiert werden.</span><span class="sxs-lookup"><span data-stu-id="223e7-136">The agent reads and writes settings to this location as defined by the registered UE-V settings location templates.</span></span>

<span data-ttu-id="223e7-137">Die **UE-V-Einstellungen werden durch die Regel "letzte Write-WINS" bestimmt:** Wenn der Speicherort für Einstellungen für Benutzer mit mehreren verwalteten Computern identisch ist, liest und schreibt ein UE-V-Agent unabhängig von Agents, die auf anderen Computern ausgeführt werden, den Speicherort für die Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="223e7-137">**UE-V settings are determined by a "Last write wins" rule:** If the settings storage location is the same for user with multiple managed computers, one UE-V Agent reads and writes to the settings location independently of agents running on other computers.</span></span> <span data-ttu-id="223e7-138">Die letzten geschriebenen Einstellungen und Werte sind diejenigen, die angewendet werden, wenn der nächste Agent vom Speicherort für Einstellungen liest.</span><span class="sxs-lookup"><span data-stu-id="223e7-138">The last written settings and values are the ones applied when the next agent reads from the settings storage location.</span></span>

<span data-ttu-id="223e7-139">**Bereitstellen des Speicherorts für Einstellungen:** Führen Sie die folgenden Schritte aus, um den Speicherort für Einstellungen zu definieren, anstatt den vorhandenen Active Directory-Dienst zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="223e7-139">**Deploy the settings storage location:** Follow these steps to define the settings storage location rather than using your existing Active Directory service.</span></span> <span data-ttu-id="223e7-140">Sie sollten den Zugriff auf die Speicherfreigabe für Einstellungen auf die Benutzer beschränken, die dies erfordern, wie in den folgenden Tabellen dargestellt.</span><span class="sxs-lookup"><span data-stu-id="223e7-140">You should limit access to the settings storage share to those users that require it, as shown in the tables below.</span></span>

**<span data-ttu-id="223e7-141">So stellen Sie die UE-V-Netzwerkfreigabe bereit</span><span class="sxs-lookup"><span data-stu-id="223e7-141">To deploy the UE-V network share</span></span>**

1.  <span data-ttu-id="223e7-142">Erstellen Sie eine neue Sicherheitsgruppe für UE-V-Benutzer.</span><span class="sxs-lookup"><span data-stu-id="223e7-142">Create a new security group for UE-V users.</span></span>

2.  <span data-ttu-id="223e7-143">Erstellen Sie einen neuen Ordner auf dem zentral gelegenen Computer, auf dem die UE-v-Einstellungs Pakete gespeichert sind, und gewähren Sie dem UE-v-Benutzer Zugriff mit Gruppen Berechtigungen für den Ordner.</span><span class="sxs-lookup"><span data-stu-id="223e7-143">Create a new folder on the centrally located computer that stores the UE-V settings packages, and then grant the UE-V users access with group permissions to the folder.</span></span> <span data-ttu-id="223e7-144">Der Administrator, der UE-V unterstützt, muss über Berechtigungen für diesen freigegebenen Ordner verfügen.</span><span class="sxs-lookup"><span data-stu-id="223e7-144">The administrator who supports UE-V must have permissions to this shared folder.</span></span>

3.  <span data-ttu-id="223e7-145">Legen Sie die folgenden SMB-Berechtigungen (Share-Level-Server-Nachrichten Block) für den Ordner "Settings-Speicherort" ein.</span><span class="sxs-lookup"><span data-stu-id="223e7-145">Set the following share-level Server Message Block (SMB) permissions for the settings storage location folder.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong><span data-ttu-id="223e7-146">Benutzerkonto</span><span class="sxs-lookup"><span data-stu-id="223e7-146">User account</span></span></strong></th>
    <th align="left"><strong><span data-ttu-id="223e7-147">Empfohlene Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="223e7-147">Recommended permissions</span></span></strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="223e7-148">Jeder</span><span class="sxs-lookup"><span data-stu-id="223e7-148">Everyone</span></span></p></td>
    <td align="left"><p><span data-ttu-id="223e7-149">Keine Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="223e7-149">No permissions</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="223e7-150">Sicherheitsgruppe der UE-V-Benutzer</span><span class="sxs-lookup"><span data-stu-id="223e7-150">Security group of UE-V users</span></span></p></td>
    <td align="left"><p><span data-ttu-id="223e7-151">Vollzugriff</span><span class="sxs-lookup"><span data-stu-id="223e7-151">Full control</span></span></p></td>
    </tr>
    </tbody>
    </table>



4.  <span data-ttu-id="223e7-152">Legen Sie die folgenden NTFS-Dateisystemberechtigungen für den Ordner "Settings Storage Location" ein.</span><span class="sxs-lookup"><span data-stu-id="223e7-152">Set the following NTFS file system permissions for the settings storage location folder.</span></span>

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong><span data-ttu-id="223e7-153">Benutzerkonto</span><span class="sxs-lookup"><span data-stu-id="223e7-153">User account</span></span></strong></th>
    <th align="left"><strong><span data-ttu-id="223e7-154">Empfohlene Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="223e7-154">Recommended permissions</span></span></strong></th>
    <th align="left"><strong><span data-ttu-id="223e7-155">Ordner</span><span class="sxs-lookup"><span data-stu-id="223e7-155">Folder</span></span></strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="223e7-156">Ersteller/Besitzer</span><span class="sxs-lookup"><span data-stu-id="223e7-156">Creator/owner</span></span></p></td>
    <td align="left"><p><span data-ttu-id="223e7-157">Vollzugriff</span><span class="sxs-lookup"><span data-stu-id="223e7-157">Full control</span></span></p></td>
    <td align="left"><p><span data-ttu-id="223e7-158">Nur Unterordner und Dateien</span><span class="sxs-lookup"><span data-stu-id="223e7-158">Subfolders and files only</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="223e7-159">Sicherheitsgruppe der UE-V-Benutzer</span><span class="sxs-lookup"><span data-stu-id="223e7-159">Security group of UE-V users</span></span></p></td>
    <td align="left"><p><span data-ttu-id="223e7-160">Ordner auflisten/Daten lesen, Ordner erstellen/Daten anfügen</span><span class="sxs-lookup"><span data-stu-id="223e7-160">List folder/read data, create folders/append data</span></span></p></td>
    <td align="left"><p><span data-ttu-id="223e7-161">Nur diesen Ordner</span><span class="sxs-lookup"><span data-stu-id="223e7-161">This folder only</span></span></p></td>
    </tr>
    </tbody>
    </table>



<span data-ttu-id="223e7-162">Mit dieser Konfiguration erstellt und sichert der UE-V-Agent einen Settingspackage-Ordner, während er im Kontext des Benutzers ausgeführt wird, und gewährt jedem Benutzer die Berechtigung zum Erstellen von Ordnern für die Speicherung von Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="223e7-162">With this configuration, the UE-V Agent creates and secures a Settingspackage folder while it runs in the context of the user, and grants each user permission to create folders for settings storage.</span></span> <span data-ttu-id="223e7-163">Benutzer erhalten Vollzugriff auf Ihren Settingspackage-Ordner, während andere Benutzer nicht darauf zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="223e7-163">Users receive full control to their Settingspackage folder while other users cannot access it.</span></span>

**<span data-ttu-id="223e7-164">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="223e7-164">Note</span></span>**  
<span data-ttu-id="223e7-165">Wenn Sie die Speicherfreigabe für Einstellungen auf einem Computer erstellen, auf dem ein Windows Server-Betriebssystem ausgeführt wird, konfigurieren Sie UE-V, um zu überprüfen, ob die lokale Gruppe Administratoren oder der aktuelle Benutzer der Besitzer des Ordners ist, in dem die Einstellungs Pakete gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="223e7-165">If you create the settings storage share on a computer running a Windows Server operating system, configure UE-V to verify that either the local Administrators group or the current user is the owner of the folder where settings packages are stored.</span></span> <span data-ttu-id="223e7-166">Um diese zusätzliche Sicherheit zu aktivieren, geben Sie diese Einstellung im Windows Server-Registrierungs-Editor an:</span><span class="sxs-lookup"><span data-stu-id="223e7-166">To enable this additional security, specify this setting in the Windows Server Registry Editor:</span></span>

1.  <span data-ttu-id="223e7-167">Fügen Sie einen Registrierungsschlüssel " **reg \ _DWORD** " mit dem Namen **"RepositoryOwnerCheckEnabled"** zu **HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\uev\\agent\\configuration**.</span><span class="sxs-lookup"><span data-stu-id="223e7-167">Add a **REG\_DWORD** registry key named **"RepositoryOwnerCheckEnabled"** to **HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\UEV\\Agent\\Configuration**.</span></span>

2.  <span data-ttu-id="223e7-168">Stellen Sie den Wert für den Registrierungsschlüssel auf *1 ein*.</span><span class="sxs-lookup"><span data-stu-id="223e7-168">Set the registry key value to *1*.</span></span>



### <span data-ttu-id="223e7-169">Verwenden von Active Directory mit UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="223e7-169">Use Active Directory with UE-V 2.x</span></span>

<span data-ttu-id="223e7-170">Der UE-V-Agent verwendet standardmäßig Active Directory (AD), wenn ein Speicherort für Einstellungen nicht anderweitig definiert ist.</span><span class="sxs-lookup"><span data-stu-id="223e7-170">The UE-V Agent uses Active Directory (AD) by default if a settings storage location is not otherwise defined.</span></span> <span data-ttu-id="223e7-171">In diesen Fällen erstellt der UE-V-Agent dynamisch den Einstellungsspeicher Ordner unter dem Stammverzeichnis des AD Home-Verzeichnisses jedes Benutzers.</span><span class="sxs-lookup"><span data-stu-id="223e7-171">In these cases, the UE-V Agent dynamically creates the settings storage folder under the root of the AD home directory of each user.</span></span> <span data-ttu-id="223e7-172">Wenn jedoch eine benutzerdefinierte Verzeichnis Einstellung in AD konfiguriert ist, wird stattdessen dieses Verzeichnis verwendet.</span><span class="sxs-lookup"><span data-stu-id="223e7-172">But, if a custom directory setting is configured in AD, then that directory is used instead.</span></span>

## <a href="" id="config"></a><span data-ttu-id="223e7-173">Wählen Sie die Konfigurationsmethode für UE-V 2. x aus.</span><span class="sxs-lookup"><span data-stu-id="223e7-173">Choose the Configuration Method for UE-V 2.x</span></span>


<span data-ttu-id="223e7-174">Sie möchten ermitteln, welche Konfigurationsmethode Sie für die Verwaltung von UE-v nach der Bereitstellung verwenden werden, da es sich hierbei um die Konfigurationsmethode handelt, die Sie zum Bereitstellen des UE-v-Agents verwenden.</span><span class="sxs-lookup"><span data-stu-id="223e7-174">You want to figure out which configuration method you'll use to manage UE-V after deployment since this will be the configuration method you use to deploy the UE-V Agent.</span></span> <span data-ttu-id="223e7-175">In der Regel ist dies die Konfigurationsmethode, die Sie bereits in Ihrer Umgebung verwenden, beispielsweise Windows PowerShell oder Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="223e7-175">Typically, this is the configuration method that you already use in your environment, such as Windows PowerShell or Configuration Manager.</span></span>

<span data-ttu-id="223e7-176">Je nach verwendeter Konfigurationsmethode können Sie UE-v vor, während oder nach der Installation des UE-v-Agents konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="223e7-176">You can configure UE-V before, during, or after UE-V Agent installation, depending on the configuration method that you use.</span></span>

-   <span data-ttu-id="223e7-177">[Gruppenrichtlinie](https://technet.microsoft.com/library/dn458893.aspx)**:** Sie können Ihre vorhandene Gruppenrichtlinieninfrastruktur verwenden, um UE-v vor oder nach der Bereitstellung des UE-v-Agents zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="223e7-177">[Group Policy](https://technet.microsoft.com/library/dn458893.aspx)**:** You can use your existing Group Policy infrastructure to configure UE-V before or after UE-V Agent deployment.</span></span> <span data-ttu-id="223e7-178">Die Vorlage UE-v-Gruppenrichtlinien-ADMX ermöglicht die zentrale Verwaltung der allgemeinen Konfigurationsoptionen des UE-v-Agents und umfasst Einstellungen für die Konfiguration der UE-v-Synchronisierung.</span><span class="sxs-lookup"><span data-stu-id="223e7-178">The UE-V Group Policy ADMX template enables the central management of common UE-V Agent configuration options, and it includes settings to configure UE-V synchronization.</span></span>

    <span data-ttu-id="223e7-179">**Installieren der ADMX-Vorlagen für UE-V-Gruppenrichtlinien:** ADMX-Vorlagen für Gruppenrichtlinien für UE-v konfigurieren Sie die Synchronisierungseinstellungen für den UE-v-Agent, und aktivieren Sie die zentrale Verwaltung der allgemeinen Konfigurationseinstellungen des UE-v-Agents mithilfe einer vorhandenen Gruppenrichtlinien-Infrastruktur.</span><span class="sxs-lookup"><span data-stu-id="223e7-179">**Installing the UE-V Group Policy ADMX Templates:** Group Policy ADMX templates for UE-V configure the synchronization settings for the UE-V Agent and enable the central management of common UE-V Agent configuration settings by using an existing Group Policy infrastructure.</span></span>

    <span data-ttu-id="223e7-180">Unterstützte Betriebssysteme für den Domänencontroller, der die Gruppenrichtlinienobjekte bereitstellt, umfassen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="223e7-180">Supported operating systems for the domain controller that deploys the Group Policy Objects include the following:</span></span>

    <span data-ttu-id="223e7-181">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="223e7-181">Windows Server 2008 R2</span></span>

    <span data-ttu-id="223e7-182">Windows Server 2012 und Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="223e7-182">Windows Server 2012 and Windows Server 2012 R2</span></span>

-   <span data-ttu-id="223e7-183">[Konfigurations-Manager](https://technet.microsoft.com/library/dn458917.aspx)**:** mit dem UE-v-Konfigurationspaket können Sie das Feature "Konformitäts Einstellungen" von System Center Configuration Manager 2012 SP1 oder höher verwenden, um konsistente Konfigurationen auf Websites anzuwenden, auf denen UE-v und Configuration Manager installiert sind.</span><span class="sxs-lookup"><span data-stu-id="223e7-183">[Configuration Manager](https://technet.microsoft.com/library/dn458917.aspx)**:** The UE-V Configuration Pack lets you use the Compliance Settings feature of System Center Configuration Manager 2012 SP1 or later to apply consistent configurations across sites where UE-V and Configuration Manager are installed.</span></span>

-   <span data-ttu-id="223e7-184">[Windows PowerShell und WMI](https://technet.microsoft.com/library/dn458937.aspx)**:** Sie können mithilfe von skriptbasierten Befehlen für Windows PowerShell und Windows-Verwaltungsinstrumentation (WMI) Konfigurationen nach der Installation des UE-V-Agents ändern.</span><span class="sxs-lookup"><span data-stu-id="223e7-184">[Windows PowerShell and WMI](https://technet.microsoft.com/library/dn458937.aspx)**:** You can use scripted commands for Windows PowerShell and Windows Management Instrumentation (WMI) to modify configurations after you install the UE-V Agent.</span></span>

    **<span data-ttu-id="223e7-185">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="223e7-185">Note</span></span>**  
    <span data-ttu-id="223e7-186">Die Änderung der Registrierung kann zu Datenverlusten führen, oder der Computer reagiert nicht mehr.</span><span class="sxs-lookup"><span data-stu-id="223e7-186">Registry modification can result in data loss, or the computer becomes unresponsive.</span></span> <span data-ttu-id="223e7-187">Wir empfehlen, dass Sie andere Konfigurationsmethoden verwenden.</span><span class="sxs-lookup"><span data-stu-id="223e7-187">We recommend that you use other configuration methods.</span></span>



-   <span data-ttu-id="223e7-188">**Befehlszeilen-oder Batch Skript Installation:** Parameter, die beim [Bereitstellen des UE-v-Agents](#agent) verwendet werden, konfigurieren viele UE-v-Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="223e7-188">**Command-line or Batch Script Installation:** Parameters that are used when you [Deploy the UE-V Agent](#agent) configure many UE-V settings.</span></span> <span data-ttu-id="223e7-189">Elektronische Softwareverteilungssysteme wie System Center 2012 Configuration Manager verwenden diese Parameter, um Ihre Clients beim Bereitstellen und Installieren der UE-V-Agent-Software zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="223e7-189">Electronic software distribution systems, such as System Center 2012 Configuration Manager, use these parameters to configure their clients when they deploy and install the UE-V Agent software.</span></span>

## <a href="" id="agent"></a><span data-ttu-id="223e7-190">Bereitstellen des UE-V 2. x-Agents</span><span class="sxs-lookup"><span data-stu-id="223e7-190">Deploy the UE-V 2.x Agent</span></span>


<span data-ttu-id="223e7-191">Der UE-v-Agent ist der Kern einer UE-v-Bereitstellung und muss auf jedem Computer ausgeführt werden, der UE-v verwendet, um die Anwendungs-und Windows-Einstellungen zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="223e7-191">The UE-V Agent is the core of a UE-V deployment and must run on each computer that uses UE-V to synchronize application and Windows settings.</span></span>

<span data-ttu-id="223e7-192">**Installationsdateien des UE-V-Agents:** Eine einzelne Installationsdatei, AgentSetup.exe, installiert den UE-V-Agent sowohl auf 32-Bit-als auch 64-Bit-Betriebssystemen.</span><span class="sxs-lookup"><span data-stu-id="223e7-192">**UE-V Agent Installation Files:** A single installation file, AgentSetup.exe, installs the UE-V Agent on both 32-bit and 64-bit operating systems.</span></span> <span data-ttu-id="223e7-193">Darüber hinaus werden AgentSetupx86.msi oder AgentSetupx64.msi architekturspezifische Windows Installer-Dateien bereitgestellt, und da Sie kleiner sind, können Sie die Agenten Bereitstellungen rationalisieren.</span><span class="sxs-lookup"><span data-stu-id="223e7-193">In addition, AgentSetupx86.msi or AgentSetupx64.msi architecture-specific Windows Installer files are provided, and since they are smaller, they might streamline the agent deployments.</span></span> <span data-ttu-id="223e7-194">Die [Befehlszeilenparameter für das AgentSetup.exe-Installationsprogramm](#params) werden auch für die Windows Installer-Installation unterstützt.</span><span class="sxs-lookup"><span data-stu-id="223e7-194">The [command-line parameters for the AgentSetup.exe installer](#params) are supported for the Windows Installer installation as well.</span></span>

**<span data-ttu-id="223e7-195">Wichtig</span><span class="sxs-lookup"><span data-stu-id="223e7-195">Important</span></span>**  
<span data-ttu-id="223e7-196">Bei der Installation oder Deinstallation von UE-V-Agents können Sie entweder die AgentSetup.exe-Datei oder die Sie AgentSetup &lt; arch &gt; . msi-Datei verwenden, aber nicht beide.</span><span class="sxs-lookup"><span data-stu-id="223e7-196">During UE-V Agent installation or uninstallation, you can either use the AgentSetup.exe file or the AgentSetup&lt;arch&gt;.msi file, but not both.</span></span> <span data-ttu-id="223e7-197">Die gleiche Datei muss zum Deinstallieren des UE-v-Agents verwendet werden, der zum Installieren des UE-v-Agents verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="223e7-197">The same file must be used to uninstall the UE-V Agent that was used to install the UE-V Agent.</span></span>



### <span data-ttu-id="223e7-198">Bereitstellen des UE-V-Agents</span><span class="sxs-lookup"><span data-stu-id="223e7-198">To Deploy the UE-V Agent</span></span>

<span data-ttu-id="223e7-199">Sie können die folgenden Methoden zum Bereitstellen des UE-V-Agents verwenden:</span><span class="sxs-lookup"><span data-stu-id="223e7-199">You can use the following methods to deploy the UE-V Agent:</span></span>

-   <span data-ttu-id="223e7-200">Ein ESD-Lösungssystem (Electronic Software Distribution) wie Configuration Manager, mit dem eine Windows Installer-Datei (MSI) installiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="223e7-200">An electronic software distribution (ESD) solution system, such as Configuration Manager, that can install a Windows Installer (.msi) file.</span></span>

-   <span data-ttu-id="223e7-201">Ein Installationsskript, das auf die Windows Installer-Datei (MSI) verweist, die zentral auf einer Freigabe gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="223e7-201">An installation script that references the Windows Installer (.msi) file that is stored centrally on a share.</span></span>

-   <span data-ttu-id="223e7-202">Ein Installationsprogramm, das Sie manuell auf dem Computer ausführen.</span><span class="sxs-lookup"><span data-stu-id="223e7-202">An installation program that you run manually on the computer.</span></span>

<span data-ttu-id="223e7-203">Gehen Sie wie folgt vor, um den UE-V-Agent über eine Netzwerkfreigabe bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="223e7-203">Use the following procedure to deploy the UE-V Agent from a network share.</span></span>

**<span data-ttu-id="223e7-204">So installieren und konfigurieren Sie den UE-V-Agent über eine Netzwerkfreigabe</span><span class="sxs-lookup"><span data-stu-id="223e7-204">To install and configure the UE-V Agent from a network share</span></span>**

1.  <span data-ttu-id="223e7-205">Stufen Sie die Installationsdatei des UE-V-Agents auf einer Netzwerkfreigabe AgentSetup.exe, auf die Benutzer die Berechtigung "lesen" haben.</span><span class="sxs-lookup"><span data-stu-id="223e7-205">Stage the UE-V Agent installation file AgentSetup.exe on a network share to which users have Read permission.</span></span>

2.  <span data-ttu-id="223e7-206">Stellen Sie ein Skript auf Benutzercomputern bereit, die den UE-V-Agent installieren.</span><span class="sxs-lookup"><span data-stu-id="223e7-206">Deploy a script to user computers that installs the UE-V Agent.</span></span> <span data-ttu-id="223e7-207">Das Skript sollte den Speicherort für Einstellungen angeben.</span><span class="sxs-lookup"><span data-stu-id="223e7-207">The script should specify the settings storage location.</span></span>

<span data-ttu-id="223e7-208">**Bereitstellungsoptionen:** Achten Sie beim Installieren des UE-V-Agents darauf, das richtige Variablen Format zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="223e7-208">**Deployment options:** Be sure to use the correct variable format when you install the UE-V Agent.</span></span> <span data-ttu-id="223e7-209">Die folgende Tabelle enthält Beispiele für Bereitstellungsoptionen für die Verwendung der AgentSetup.exe-oder Windows Installer-Dateien (MSI).</span><span class="sxs-lookup"><span data-stu-id="223e7-209">The following table provides examples of deployment options for using the AgentSetup.exe or the Windows Installer (.msi) files.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="223e7-210">Bereitstellungstyp</span><span class="sxs-lookup"><span data-stu-id="223e7-210">Deployment type</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="223e7-211">Bereitstellungs Beschreibung</span><span class="sxs-lookup"><span data-stu-id="223e7-211">Deployment description</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="223e7-212">Beispiel</span><span class="sxs-lookup"><span data-stu-id="223e7-212">Example</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="223e7-213">Eingabeaufforderung</span><span class="sxs-lookup"><span data-stu-id="223e7-213">Command prompt</span></span></p></td>
<td align="left"><p><span data-ttu-id="223e7-214">Wenn Sie den UE-V-Agent an einer Eingabeaufforderung installieren, verwenden Sie das <em> Variable Format% ^ username% </em> .</span><span class="sxs-lookup"><span data-stu-id="223e7-214">When you install the UE-V Agent at a command prompt, use the <em>%^username%</em> variable format.</span></span> <span data-ttu-id="223e7-215">Wenn Anführungszeichen aufgrund von Leerzeichen im Einstellungsspeicher Pfad erforderlich sind, verwenden Sie eine Batchskriptdatei für die Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="223e7-215">If quotation marks are required because of spaces in the settings storage path, use a batch script file for deployment.</span></span></p>
<p></p></td>
<td align="left"><p><code>AgentSetup.exe /quiet /norestart /log &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare%^username%</code></p>
<p></p>
<p><code>msiexec.exe /i &quot;&lt;path to msi file&gt;&quot; /quiet /norestart /l<em>v &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare%^username%</code></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="223e7-216">Batch Skript</span><span class="sxs-lookup"><span data-stu-id="223e7-216">Batch script</span></span></p></td>
<td align="left"><p><span data-ttu-id="223e7-217">Wenn Sie den UE-V-Agent aus einer Batchskriptdatei installieren, verwenden Sie das <em> Variable Format%% username%% </em> .</span><span class="sxs-lookup"><span data-stu-id="223e7-217">When you install the UE-V Agent from a batch script file, use the <em>%%username%%</em> variable format.</span></span> <span data-ttu-id="223e7-218">Wenn Sie diese Installationsmethode verwenden, müssen Sie der Variablen mit den%% Zeichen entkommen.</span><span class="sxs-lookup"><span data-stu-id="223e7-218">If you use this installation method, you must escape the variable with the %% characters.</span></span> <span data-ttu-id="223e7-219">Ohne dieses Zeichen erweitert das Skript die <em> Benutzername </em> -Variable zur Installationszeit anstatt zur Laufzeit, wodurch UE-V dazu veranlasst wird, einen einzelnen Einstellungs Speicherort für alle Benutzer zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="223e7-219">Without this character, the script expands the <em>username</em> variable at installation time, rather than at run time, which causes UE-V to use a single settings storage location for all users.</span></span></p></td>
<td align="left"><p><code>AgentSetup.exe /quiet /norestart /log &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=&quot;\server\settingsshare%%username%%&quot;</code></p>
<p></p>
<p><code>msiexec.exe /i &quot;&lt;path to msi file&gt;&quot; /quiet /norestart /l</em>v &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=&quot;\server\settingsshare%%username%%&quot;</code></p>
<p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="223e7-220">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="223e7-220">Windows PowerShell</span></span></p></td>
<td align="left"><p><span data-ttu-id="223e7-221">Wenn Sie den UE-V-Agent über eine Windows PowerShell-Eingabeaufforderung oder ein Windows PowerShell-Skript installieren, verwenden Sie das <em> Variable Format% username% </em> .</span><span class="sxs-lookup"><span data-stu-id="223e7-221">When you install the UE-V Agent from a Windows PowerShell prompt or a Windows PowerShell script, use the <em>%username%</em> variable format.</span></span></p></td>
<td align="left"><p><code>&amp; AgentSetup.exe /quiet /norestart /log &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare%username%</code></p>
<p></p>
<p><code>&amp; msiexec.exe /i &quot;&lt;path to msi file&gt;&quot; /quiet /norestart /l<em>v &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare%username%</code></p>
<p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="223e7-222">Elektronische Softwareverteilung, beispielsweise Bereitstellung der Configuration Manager-Softwarebereitstellung</span><span class="sxs-lookup"><span data-stu-id="223e7-222">Electronic software distribution, such as deployment of Configuration Manager Software Deployment</span></span></p></td>
<td align="left"><p><span data-ttu-id="223e7-223">Wenn Sie den UE-V-Agent mithilfe von Configuration Manager installieren, verwenden Sie das <em> Variablen Format ^% username ^% </em> .</span><span class="sxs-lookup"><span data-stu-id="223e7-223">When you install the UE-V Agent by using Configuration Manager, use the <em>^%username^%</em> variable format.</span></span></p></td>
<td align="left"><p><code>AgentSetup.exe /quiet /norestart /log &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare^%username^%</code></p>
<p></p>
<p><code>msiexec.exe /i &quot;&lt;path to msi file&gt;&quot; /quiet /norestart /l</em>v &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare^%username^%</code></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="223e7-224">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="223e7-224">Note</span></span>**  
<span data-ttu-id="223e7-225">Die Installation des UE-v-Agents erfordert Administratorrechte, und der Computer erfordert einen Neustart, bevor der UE-v-Agent ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="223e7-225">The installation of the UE-V Agent requires administrator rights, and the computer requires a restart before the UE-V Agent can run.</span></span>



### <a href="" id="params"></a><span data-ttu-id="223e7-226">Befehlszeilenparameter für die Bereitstellung von UE-V-Agents</span><span class="sxs-lookup"><span data-stu-id="223e7-226">Command-line parameters for UE-V Agent deployment</span></span>

<span data-ttu-id="223e7-227">Die Befehlszeilenparameter des UE-V-Agents lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="223e7-227">The command-line parameters of the UE-V Agent are as follows.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="223e7-228">Befehlszeilenparameter</span><span class="sxs-lookup"><span data-stu-id="223e7-228">Command-line parameter</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="223e7-229">Definition</span><span class="sxs-lookup"><span data-stu-id="223e7-229">Definition</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="223e7-230">Anmerkungen</span><span class="sxs-lookup"><span data-stu-id="223e7-230">Notes</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="223e7-231">/Help oder/h oder/?</span><span class="sxs-lookup"><span data-stu-id="223e7-231">/help or /h or /?</span></span></p></td>
<td align="left"><p><span data-ttu-id="223e7-232">Zeigt das Dialogfeld "AgentSetup.exe Verwendung" an.</span><span class="sxs-lookup"><span data-stu-id="223e7-232">Displays the AgentSetup.exe usage dialog box.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="223e7-233">SettingsStoragePath</span><span class="sxs-lookup"><span data-stu-id="223e7-233">SettingsStoragePath</span></span></p></td>
<td align="left"><p><span data-ttu-id="223e7-234">Gibt den UNC-Pfad (Universal Naming Convention) an, der definiert, wo die Einstellungen gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="223e7-234">Indicates the Universal Naming Convention (UNC) path that defines where settings are stored.</span></span></p></td>
<td align="left"><div class="alert">
<strong><span data-ttu-id="223e7-235">Wichtig</span><span class="sxs-lookup"><span data-stu-id="223e7-235">Important</span></span></strong><br/><p><span data-ttu-id="223e7-236">Sie müssen eine SettingsStoragePath in UE-v 2,1 und UE-v 2,1 SP1 angeben.</span><span class="sxs-lookup"><span data-stu-id="223e7-236">You must specify a SettingsStoragePath in UE-V 2.1 and UE-V 2.1 SP1.</span></span> <span data-ttu-id="223e7-237">Sie können die AdHomePath-Zeichenfolge festlegen, um anzugeben, dass der Active Directory-Start Pfad des Benutzers&#39;verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="223e7-237">You can set the AdHomePath string to specify that the user&#39;s Active Directory home path is used.</span></span> <span data-ttu-id="223e7-238">Beispiel: <code>SettingsStoragePath = \share\path|AdHomePath</code>.</span><span class="sxs-lookup"><span data-stu-id="223e7-238">For example, <code>SettingsStoragePath = \share\path|AdHomePath</code>.</span></span></p>
<p><span data-ttu-id="223e7-239">In UE-V 2,0 können Sie SettingsStoragePath leer lassen, um stattdessen den Active Directory-Start Pfad zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="223e7-239">In UE-V 2.0, you can leave SettingsStoragePath blank to use the Active Directory home path instead.</span></span></p>
</div>
<div>

</div>
<p><span data-ttu-id="223e7-240">% Username% oder% Computername% Umgebungsvariablen werden akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="223e7-240">%username% or %computername% environment variables are accepted.</span></span> <span data-ttu-id="223e7-241">Für Skripting können maskierte Variablen erforderlich sein.</span><span class="sxs-lookup"><span data-stu-id="223e7-241">Scripting can require escaped variables.</span></span></p>
<p><strong><span data-ttu-id="223e7-242">Standard </strong> : &lt; keine&gt;</span><span class="sxs-lookup"><span data-stu-id="223e7-242">Default</strong>: &lt;none&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="223e7-243">SettingsStoragePathReg</span><span class="sxs-lookup"><span data-stu-id="223e7-243">SettingsStoragePathReg</span></span></p></td>
<td align="left"><p><span data-ttu-id="223e7-244">Ruft während der Installation den SettingsStoragePath-Wert aus der Registrierung ab.</span><span class="sxs-lookup"><span data-stu-id="223e7-244">Gets the SettingsStoragePath value from the registry during installation.</span></span></p></td>
<td align="left"><p><span data-ttu-id="223e7-245">Geben Sie an der Eingabeaufforderung Folgendes Beispiel ein, um UE-V zu zwingen, den Active Directory-Start Pfad anstelle eines bestimmten UNC-Pfads zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="223e7-245">At the command prompt, type the following example to force UE-V to use the Active Directory home path instead of a specific UNC.</span></span></p>
<p><code>msiexec.exe /i AgentSetupx64.msi acceptlicenseterms=true SettingsStoragePathReg=TRUE /quiet /norestart</code></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="223e7-246">SettingsTemplateCatalogPath</span><span class="sxs-lookup"><span data-stu-id="223e7-246">SettingsTemplateCatalogPath</span></span></p></td>
<td align="left"><p><span data-ttu-id="223e7-247">Gibt den UNC-Pfad (Universal Naming Convention) an, der den Speicherort definiert, der auf neue Einstellungen für Standort Vorlagen überprüft wurde.</span><span class="sxs-lookup"><span data-stu-id="223e7-247">Indicates the Universal Naming Convention (UNC) path that defines the location that was checked for new settings location templates.</span></span></p></td>
<td align="left"><p><span data-ttu-id="223e7-248">Nur für benutzerdefinierte Einstellungen für Standort Vorlagen erforderlich</span><span class="sxs-lookup"><span data-stu-id="223e7-248">Only required for custom settings location templates</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="223e7-249">RegisterMSTemplates</span><span class="sxs-lookup"><span data-stu-id="223e7-249">RegisterMSTemplates</span></span></p></td>
<td align="left"><p><span data-ttu-id="223e7-250">Gibt an, ob die Microsoft-Standardvorlagen während der Installation registriert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="223e7-250">Specifies whether the default Microsoft templates should be registered during installation.</span></span></p></td>
<td align="left"><p><span data-ttu-id="223e7-251">True | False</span><span class="sxs-lookup"><span data-stu-id="223e7-251">True | False</span></span></p>
<p><strong><span data-ttu-id="223e7-252">Standard </strong> : true</span><span class="sxs-lookup"><span data-stu-id="223e7-252">Default</strong>: True</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="223e7-253">SyncMethod</span><span class="sxs-lookup"><span data-stu-id="223e7-253">SyncMethod</span></span></p></td>
<td align="left"><p><span data-ttu-id="223e7-254">Gibt an, welche Synchronisierungsmethode verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="223e7-254">Specifies which synchronization method should be used.</span></span></p></td>
<td align="left"><p><span data-ttu-id="223e7-255">SyncProvider | Keine</span><span class="sxs-lookup"><span data-stu-id="223e7-255">SyncProvider | None</span></span></p>
<p><strong><span data-ttu-id="223e7-256">Standard </strong> : SyncProvider</span><span class="sxs-lookup"><span data-stu-id="223e7-256">Default</strong>: SyncProvider</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="223e7-257">SyncTimeoutInMilliseconds</span><span class="sxs-lookup"><span data-stu-id="223e7-257">SyncTimeoutInMilliseconds</span></span></p></td>
<td align="left"><p><span data-ttu-id="223e7-258">Gibt die Anzahl der Millisekunden an, die der Computer vor dem Timeout wartet, wenn er Benutzereinstellungen vom Speicherort für Einstellungen abruft.</span><span class="sxs-lookup"><span data-stu-id="223e7-258">Specifies the number of milliseconds that the computer waits before time-out when it retrieves user settings from the settings storage location.</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="223e7-259">Standard </strong> : 2000 Millisekunden</span><span class="sxs-lookup"><span data-stu-id="223e7-259">Default</strong>: 2000 milliseconds</span></span></p>
<p><span data-ttu-id="223e7-260">(bis zu 2 Sekunden warten)</span><span class="sxs-lookup"><span data-stu-id="223e7-260">(wait up to 2 seconds)</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="223e7-261">SyncEnabled</span><span class="sxs-lookup"><span data-stu-id="223e7-261">SyncEnabled</span></span></p></td>
<td align="left"><p><span data-ttu-id="223e7-262">Gibt an, ob die UE-V-Synchronisierung aktiviert oder deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="223e7-262">Specifies whether UE-V synchronization is enabled or disabled.</span></span></p></td>
<td align="left"><p><span data-ttu-id="223e7-263">True | False</span><span class="sxs-lookup"><span data-stu-id="223e7-263">True | False</span></span></p>
<p><strong><span data-ttu-id="223e7-264">Standard </strong> : true</span><span class="sxs-lookup"><span data-stu-id="223e7-264">Default</strong>: True</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="223e7-265">MaxPackageSizeInBytes</span><span class="sxs-lookup"><span data-stu-id="223e7-265">MaxPackageSizeInBytes</span></span></p></td>
<td align="left"><p><span data-ttu-id="223e7-266">Gibt eine Dateigröße des Einstellungen-Pakets in Byte an, wenn der UE-V-Agent meldet, dass Dateien den Schwellenwert überschreiten.</span><span class="sxs-lookup"><span data-stu-id="223e7-266">Specifies a settings package file size in bytes when the UE-V Agent reports that files exceed the threshold.</span></span></p></td>
<td align="left"><p><span data-ttu-id="223e7-267">&lt;Größe&gt;</span><span class="sxs-lookup"><span data-stu-id="223e7-267">&lt;size&gt;</span></span></p>
<p><strong><span data-ttu-id="223e7-268">Standard </strong> : None (kein Warnungsschwellenwert)</span><span class="sxs-lookup"><span data-stu-id="223e7-268">Default</strong>: none (no warning threshold)</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="223e7-269">CEIPEnabled</span><span class="sxs-lookup"><span data-stu-id="223e7-269">CEIPEnabled</span></span></p></td>
<td align="left"><p><span data-ttu-id="223e7-270">Gibt die Einstellung für die Teilnahme am Programm zur Verbesserung der Benutzerfreundlichkeit an.</span><span class="sxs-lookup"><span data-stu-id="223e7-270">Specifies the setting for participation in the Customer Experience Improvement program.</span></span> <span data-ttu-id="223e7-271">Wenn die Einstellung <strong> auf </strong> "true" festgelegt ist, werden die Installationsinformationen auf die Microsoft-Website zur Verbesserung der Benutzerfreundlichkeit hochgeladen.</span><span class="sxs-lookup"><span data-stu-id="223e7-271">If set to <strong>True</strong>, installer information is uploaded to the Microsoft Customer Experience Improvement Program site.</span></span> <span data-ttu-id="223e7-272">Wenn Sie auf "false" festgelegt <strong> </strong> ist, werden keine Informationen hochgeladen.</span><span class="sxs-lookup"><span data-stu-id="223e7-272">If set to <strong>False</strong>, no information is uploaded.</span></span></p></td>
<td align="left"><p><span data-ttu-id="223e7-273">True | False</span><span class="sxs-lookup"><span data-stu-id="223e7-273">True | False</span></span></p>
<p><strong><span data-ttu-id="223e7-274">Standard </strong> : falsch</span><span class="sxs-lookup"><span data-stu-id="223e7-274">Default</strong>: False</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="223e7-275">NoRestart</span><span class="sxs-lookup"><span data-stu-id="223e7-275">NoRestart</span></span></p></td>
<td align="left"><p><span data-ttu-id="223e7-276">Unterstützt die Verzögerung des Neustarts des Computers, nachdem der UE-V-Agent installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="223e7-276">Supports deferral of the restart of the computer after the UE-V Agent is installed.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="223e7-277">INSTALLFOLDER</span><span class="sxs-lookup"><span data-stu-id="223e7-277">INSTALLFOLDER</span></span></p></td>
<td align="left"><p><span data-ttu-id="223e7-278">Ermöglicht das Einstellen eines anderen Installationsordners für den UE-v-Agent oder UE-v-Generator.</span><span class="sxs-lookup"><span data-stu-id="223e7-278">Enables a different installation folder to be set for the UE-V Agent or UE-V Generator.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="223e7-279">MUENABLED</span><span class="sxs-lookup"><span data-stu-id="223e7-279">MUENABLED</span></span></p></td>
<td align="left"><p><span data-ttu-id="223e7-280">Ermöglicht es Setup, die Option zu akzeptieren, die im Microsoft Update-Programm enthalten sein soll.</span><span class="sxs-lookup"><span data-stu-id="223e7-280">Enables Setup to accept the option to be included in the Microsoft Update program.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="223e7-281">ACCEPTLICENSETERMS</span><span class="sxs-lookup"><span data-stu-id="223e7-281">ACCEPTLICENSETERMS</span></span></p></td>
<td align="left"><p><span data-ttu-id="223e7-282">Ermöglicht die unbeaufsichtigte Installation von UE-V.</span><span class="sxs-lookup"><span data-stu-id="223e7-282">Lets UE-V be installed silently.</span></span> <span data-ttu-id="223e7-283">Diese muss auf "true" festgelegt werden <strong> </strong> , um UE-v im Hintergrund zu installieren und die Anforderung zu umgehen, dass der Benutzer die UE-v-Lizenzbedingungen akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="223e7-283">This must be set to <strong>True</strong> to install UE-V silently and bypass the requirement that the user accepts the UE-V license terms.</span></span> <span data-ttu-id="223e7-284">Wenn <strong> </strong> der Benutzer auf "false" festgelegt oder leer gelassen wird, erhält er eine Fehlermeldung, und UE-V ist nicht installiert.</span><span class="sxs-lookup"><span data-stu-id="223e7-284">If set to <strong>False</strong> or left empty, the user receives an error message and UE-V is not installed.</span></span></p></td>
<td align="left"><div class="alert">
<strong><span data-ttu-id="223e7-285">Wichtig</span><span class="sxs-lookup"><span data-stu-id="223e7-285">Important</span></span></strong><br/><p><span data-ttu-id="223e7-286">Dieser Parameter ist erforderlich, um UE-V im Hintergrund zu installieren.</span><span class="sxs-lookup"><span data-stu-id="223e7-286">This parameter is required to install UE-V silently.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="223e7-287">NORESTART</span><span class="sxs-lookup"><span data-stu-id="223e7-287">NORESTART</span></span></p></td>
<td align="left"><p><span data-ttu-id="223e7-288">Verhindert einen obligatorischen Neustart nach der Installation des UE-V-Agents.</span><span class="sxs-lookup"><span data-stu-id="223e7-288">Prevents a mandatory restart after the UE-V Agent is installed.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="223e7-289">Aktualisieren des UE-V-Agents</span><span class="sxs-lookup"><span data-stu-id="223e7-289">Update the UE-V Agent</span></span>

<span data-ttu-id="223e7-290">Updates für die UE-V-Agent-Software werden über Microsoft Update bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="223e7-290">Updates for the UE-V Agent software are provided through Microsoft Update.</span></span> <span data-ttu-id="223e7-291">Sie können UE-V-Agenten Updates mithilfe von ESD-Infrastruktursystemen (Enterprise Software Distribution) bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="223e7-291">You can deploy UE-V Agent updates by using Enterprise Software Distribution (ESD) infrastructure systems.</span></span>

<span data-ttu-id="223e7-292">Während eines UE-V-Agent-Upgrades können die standardmäßigen Einstellungen für die Standort Vorlagen für allgemeine Microsoft-Anwendungen und Windows-Einstellungen aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="223e7-292">During a UE-V Agent upgrade, the default group of settings location templates for common Microsoft applications and Windows settings can be updated.</span></span>

### <span data-ttu-id="223e7-293">Upgrade des UE-V 2. x-Agents</span><span class="sxs-lookup"><span data-stu-id="223e7-293">Upgrade the UE-V 2.x Agent</span></span>

<span data-ttu-id="223e7-294">Der UE-V 2. x-Agent führt viele neue Features ein und ändert, wie und wann der Agent Inhalte in die Speicherfreigabe für Einstellungen hochlädt.</span><span class="sxs-lookup"><span data-stu-id="223e7-294">The UE-V 2.x Agent introduces many new features and modifies how and when the agent uploads content to the settings storage share.</span></span> <span data-ttu-id="223e7-295">Der Upgradeprozess automatisiert diese Änderungen.</span><span class="sxs-lookup"><span data-stu-id="223e7-295">The upgrade process automates these changes.</span></span> <span data-ttu-id="223e7-296">Wenn Sie den UE-v-Agent aktualisieren möchten, führen Sie das UE-v-Agent-Installationspaket (AgentSetup.exe, AgentSetupx86.msi oder AgentSetupx64.msi) auf den Computern der Benutzer aus.</span><span class="sxs-lookup"><span data-stu-id="223e7-296">To upgrade the UE-V Agent, run the UE-V Agent install package (AgentSetup.exe, AgentSetupx86.msi, or AgentSetupx64.msi) on users’ computers.</span></span>

**<span data-ttu-id="223e7-297">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="223e7-297">Note</span></span>**  
<span data-ttu-id="223e7-298">Wenn Sie den UE-v-Agent aktualisieren, müssen Sie denselben Installationstyp (exe-Datei oder MSI-Paket) verwenden, der den vorherigen UE-v-Agent installiert hat.</span><span class="sxs-lookup"><span data-stu-id="223e7-298">When you upgrade the UE-V Agent, you must use the same installer type (.exe file or .msi packet) that installed the previous UE-V Agent.</span></span> <span data-ttu-id="223e7-299">Verwenden Sie beispielsweise die AgentSetup.exe UE-v 2, um UE-v 1,0-Agents zu aktualisieren, die mithilfe von AgentSetup.exe installiert wurden.</span><span class="sxs-lookup"><span data-stu-id="223e7-299">For example, use the UE-V 2 AgentSetup.exe to upgrade UE-V 1.0 Agents that were installed by using AgentSetup.exe.</span></span>



<span data-ttu-id="223e7-300">Die folgenden Konfigurationen bleiben erhalten, wenn das Agent-Setup Programm ausgeführt wird:</span><span class="sxs-lookup"><span data-stu-id="223e7-300">The following configurations are preserved when the Agent Setup program runs:</span></span>

-   <span data-ttu-id="223e7-301">Speicherpfad für Einstellungen</span><span class="sxs-lookup"><span data-stu-id="223e7-301">Settings storage path</span></span>

-   <span data-ttu-id="223e7-302">Registrierungseinstellungen</span><span class="sxs-lookup"><span data-stu-id="223e7-302">Registry settings</span></span>

-   <span data-ttu-id="223e7-303">Geplante Vorgänge (Intervalleinstellungen werden auf ihre Standardeinstellungen zurückgesetzt)</span><span class="sxs-lookup"><span data-stu-id="223e7-303">Scheduled tasks (Interval settings are reset to their defaults)</span></span>

**<span data-ttu-id="223e7-304">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="223e7-304">Note</span></span>**  
<span data-ttu-id="223e7-305">Ein Computer mit Standort Vorlagen für UE-v 2. x-Einstellungen, die bei der Registrierung des UE-v 1,0-Agents im Windows-Ereignisprotokoll registriert sind.</span><span class="sxs-lookup"><span data-stu-id="223e7-305">A computer with UE-V 2.x settings location templates that are registered in the UE-V 1.0 Agent register errors in the Windows Event Log.</span></span>



<span data-ttu-id="223e7-306">Sie können den Microsoft System Center 2012-Konfigurations-Manager oder ein anderes Tool für die Unternehmenssoftware Verteilung verwenden, um das Upgrade des UE-V-Agents zu automatisieren und zu verteilen.</span><span class="sxs-lookup"><span data-stu-id="223e7-306">You can use Microsoft System Center 2012 Configuration Manager or another enterprise software distribution tool to automate and distribute the UE-V Agent upgrade.</span></span>

<span data-ttu-id="223e7-307">**Empfehlungen:** Wir empfehlen, dass Sie alle UE-V 1,0-Agents in einer Computerumgebung aktualisieren, dies ist jedoch nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="223e7-307">**Recommendations:** We recommend that you upgrade all of the UE-V 1.0 Agents in a computing environment, but it is not required.</span></span> <span data-ttu-id="223e7-308">Die Standort Vorlagen für die UE-v 2. x-Einstellungen können mit einem UE-v 1,0-Agent interagieren, da Sie nur die Einstellungen aus dem Speicherpfad für Einstellungen freigeben.</span><span class="sxs-lookup"><span data-stu-id="223e7-308">UE-V 2.x settings location templates can interact with a UE-V 1.0 Agent because they only share the settings from the settings storage path.</span></span> <span data-ttu-id="223e7-309">Wir empfehlen jedoch, dass Sie die Bereitstellungen zu einer einzigen Agentenversion verschieben, um die Verwaltung zu vereinfachen und UE-V zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="223e7-309">We recommend, however, that you move the deployments to a single agent version to simplify management and to support UE-V.</span></span>

### <span data-ttu-id="223e7-310">Reparieren des UE-V-Agents nach einem erfolglosen Upgrade</span><span class="sxs-lookup"><span data-stu-id="223e7-310">Repair the UE-V Agent after an unsuccessful upgrade</span></span>

<span data-ttu-id="223e7-311">Nachdem Sie einen der folgenden Vorgänge ausgeführt haben, können Fehler auftreten:</span><span class="sxs-lookup"><span data-stu-id="223e7-311">You might experience errors after you attempt one of the following operations:</span></span>

-   <span data-ttu-id="223e7-312">Upgrade von UE-v 1,0 auf UE-v 2</span><span class="sxs-lookup"><span data-stu-id="223e7-312">Upgrade from UE-V 1.0 to UE-V 2</span></span>

-   <span data-ttu-id="223e7-313">Aktualisieren Sie auf eine neuere Version von Windows, beispielsweise von Windows 7 auf Windows 8 oder von Windows 8 auf Windows 8,1.</span><span class="sxs-lookup"><span data-stu-id="223e7-313">Upgrade to a newer version of Windows, for example, from Windows 7 to Windows 8 or from Windows 8 to Windows 8.1.</span></span>

-   <span data-ttu-id="223e7-314">Deinstallieren des Agents nach dem Upgrade des UE-V-Agents</span><span class="sxs-lookup"><span data-stu-id="223e7-314">Uninstall the agent after upgrading the UE-V Agent</span></span>

<span data-ttu-id="223e7-315">Um Probleme zu beheben, versuchen Sie, den UE-V-Agent zu reparieren, indem Sie diesen Befehl an einer Eingabeaufforderung auf dem Computer eingeben, auf dem der Agent installiert ist.</span><span class="sxs-lookup"><span data-stu-id="223e7-315">To resolve any issues, attempt to repair the UE-V Agent by entering this command at a command prompt on the computer where the agent is installed.</span></span>

``` syntax
msiexec.exe /f "<path to msi file>" /quiet /norestart /l*v "%temp%\UE-VAgentInstaller.log
```

<span data-ttu-id="223e7-316">Sie können dann den Deinstallationsvorgang oder das Upgrade wiederholen, indem Sie die neuere Version des UE-V-Agents installieren.</span><span class="sxs-lookup"><span data-stu-id="223e7-316">You can then retry the uninstall process or upgrade by installing the newer version of the UE-V Agent.</span></span>






## <span data-ttu-id="223e7-317">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="223e7-317">Related topics</span></span>


[<span data-ttu-id="223e7-318">Vorbereiten einer UE-V 2. x-Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="223e7-318">Prepare a UE-V 2.x Deployment</span></span>](prepare-a-ue-v-2x-deployment-new-uevv2.md)

[<span data-ttu-id="223e7-319">Bereitstellen von UE-V 2. x für benutzerdefinierte Anwendungen</span><span class="sxs-lookup"><span data-stu-id="223e7-319">Deploy UE-V 2.x for Custom Applications</span></span>](deploy-ue-v-2x-for-custom-applications-new-uevv2.md)









