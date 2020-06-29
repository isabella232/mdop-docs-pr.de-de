---
title: Planen der Verwendung der Ordnerumleitung mit App-V
description: Planen der Verwendung der Ordnerumleitung mit App-V
author: dansimp
ms.assetid: 6bea9a8f-a915-4d7d-be67-ef1cca1398ed
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 507aef186579da0efdb3af7b6e1088a5e725ad70
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804937"
---
# <span data-ttu-id="e6e27-103">Planen der Verwendung der Ordnerumleitung mit App-V</span><span class="sxs-lookup"><span data-stu-id="e6e27-103">Planning to Use Folder Redirection with App-V</span></span>


<span data-ttu-id="e6e27-104">Microsoft Application Virtualization (App-V) 5,1 unterstützt die Verwendung der Ordnerumleitung, ein Feature, mit dem Benutzer und Administratoren den Pfad eines Ordners an einen neuen Speicherort umleiten können.</span><span class="sxs-lookup"><span data-stu-id="e6e27-104">Microsoft Application Virtualization (App-V) 5.1 supports the use of folder redirection, a feature that enables users and administrators to redirect the path of a folder to a new location.</span></span>

<span data-ttu-id="e6e27-105">Dieses Thema enthält die folgenden Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="e6e27-105">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="e6e27-106">Voraussetzungen für die Verwendung der Ordnerumleitung</span><span class="sxs-lookup"><span data-stu-id="e6e27-106">Requirements for using folder redirection</span></span>](#bkmk-folder-redir-reqs)

-   [<span data-ttu-id="e6e27-107">Konfigurieren der Ordnerumleitung zur Verwendung mit App-V</span><span class="sxs-lookup"><span data-stu-id="e6e27-107">How to configure folder redirection for use with App-V</span></span>](#bkmk-folder-redir-cfg)

-   [<span data-ttu-id="e6e27-108">Funktionsweise der Ordnerumleitung mit App-V</span><span class="sxs-lookup"><span data-stu-id="e6e27-108">How folder redirection works with App-V</span></span>](#bkmk-folder-redir-works)

-   [<span data-ttu-id="e6e27-109">Übersicht über die Ordnerumleitung</span><span class="sxs-lookup"><span data-stu-id="e6e27-109">Overview of folder redirection</span></span>](#bkmk-folder-redir-overview)

## <a href="" id="bkmk-folder-redir-reqs"></a><span data-ttu-id="e6e27-110">Anforderungen und nicht unterstützte Szenarien für die Verwendung der Ordnerumleitung</span><span class="sxs-lookup"><span data-stu-id="e6e27-110">Requirements and unsupported scenarios for using folder redirection</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e6e27-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e6e27-111">Requirements</span></span></p></td>
<td align="left"><p><span data-ttu-id="e6e27-112">Um die Ordnerumleitung von% APPDATA% zu verwenden, müssen Sie Folgendes ausführen:</span><span class="sxs-lookup"><span data-stu-id="e6e27-112">To use %AppData% folder redirection, you must:</span></span></p>
<ul>
<li><p><span data-ttu-id="e6e27-113">Verfügen Sie über ein App-V-Paket mit einem VFS-Ordner (APPDATA Virtual File System).</span><span class="sxs-lookup"><span data-stu-id="e6e27-113">Have an App-V package that has an AppData virtual file system (VFS) folder.</span></span></p></li>
<li><p><span data-ttu-id="e6e27-114">Aktivieren Sie die Ordnerumleitung, und leiten Sie die Ordner der Benutzer in einen freigegebenen Ordner um, in der Regel in einem Netzwerkordner.</span><span class="sxs-lookup"><span data-stu-id="e6e27-114">Enable folder redirection and redirect users’ folders to a shared folder, typically a network folder.</span></span></p></li>
<li><p><span data-ttu-id="e6e27-115">Roamen Sie beide oder keine der folgenden Optionen:</span><span class="sxs-lookup"><span data-stu-id="e6e27-115">Roam both or neither of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="e6e27-116">Dateien unter%APPDATA%\Microsoft\AppV\Client\Catalog</span><span class="sxs-lookup"><span data-stu-id="e6e27-116">Files under %appdata%\Microsoft\AppV\Client\Catalog</span></span></p></li>
<li><p><span data-ttu-id="e6e27-117">Registrierungseinstellungen unter HKEY_CURRENT_USER \software\microsoft\appv\client\packages</span><span class="sxs-lookup"><span data-stu-id="e6e27-117">Registry settings under HKEY_CURRENT_USER\Software\Microsoft\AppV\Client\Packages</span></span></p>
<p><span data-ttu-id="e6e27-118">Weitere Informationen finden Sie unter <a href="application-publishing-and-client-interaction.md#bkmk-clt-inter-roam-reqs" data-raw-source="[Application Publishing and Client Interaction](application-publishing-and-client-interaction.md#bkmk-clt-inter-roam-reqs)"> Anwendungsveröffentlichung und Client Interaktion </a> .</span><span class="sxs-lookup"><span data-stu-id="e6e27-118">For more detail, see <a href="application-publishing-and-client-interaction.md#bkmk-clt-inter-roam-reqs" data-raw-source="[Application Publishing and Client Interaction](application-publishing-and-client-interaction.md#bkmk-clt-inter-roam-reqs)">Application Publishing and Client Interaction</a>.</span></span></p></li>
</ul></li>
<li><p><span data-ttu-id="e6e27-119">Stellen Sie sicher, dass die folgenden Ordner für jeden Benutzer verfügbar sind, der sich bei dem Computer anmeldet, auf dem der Client App-V 5,0 SP2 oder höher ausgeführt wird:</span><span class="sxs-lookup"><span data-stu-id="e6e27-119">Ensure that the following folders are available to each user who logs into the computer that is running the App-V 5.0 SP2 or later client:</span></span></p>
<ul>
<li><p><span data-ttu-id="e6e27-120">% APPDATA% ist für den gewünschten Netzwerkspeicherort konfiguriert (mit oder ohne <a href="https://technet.microsoft.com/library/cc780552.aspx" data-raw-source="[Offline Files](https://technet.microsoft.com/library/cc780552.aspx)"> Unterstützung für Offline Dateien </a> ).</span><span class="sxs-lookup"><span data-stu-id="e6e27-120">%AppData% is configured to the desired network location (with or without <a href="https://technet.microsoft.com/library/cc780552.aspx" data-raw-source="[Offline Files](https://technet.microsoft.com/library/cc780552.aspx)">Offline Files</a> support).</span></span></p></li>
<li><p><span data-ttu-id="e6e27-121">% LocalAppData% ist für den gewünschten lokalen Ordner konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="e6e27-121">%LocalAppData% is configured to the desired local folder.</span></span></p></li>
</ul></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e6e27-122">Nicht unterstützte Szenarien</span><span class="sxs-lookup"><span data-stu-id="e6e27-122">Unsupported scenarios</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="e6e27-123">Konfigurieren von% LocalAppData% als Netzlaufwerk.</span><span class="sxs-lookup"><span data-stu-id="e6e27-123">Configuring %LocalAppData% as a network drive.</span></span></p></li>
<li><p><span data-ttu-id="e6e27-124">Umleiten des Start Menüs an einen einzelnen Ordner für mehrere Benutzer</span><span class="sxs-lookup"><span data-stu-id="e6e27-124">Redirecting the Start menu to a single folder for multiple users.</span></span></p></li>
<li><p><span data-ttu-id="e6e27-125">Wenn Roaming-APPDATA (% APPDATA%) an eine nicht verfügbare Netzwerkfreigabe umgeleitet wird, können App-V-Anwendungen wie folgt nicht gestartet werden:</span><span class="sxs-lookup"><span data-stu-id="e6e27-125">If roaming AppData (%AppData%) is redirected to a network share that is not available, App-V applications will fail to launch as follows:</span></span></p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="e6e27-126">App-V-Version</span><span class="sxs-lookup"><span data-stu-id="e6e27-126">App-V version</span></span></th>
<th align="left"><span data-ttu-id="e6e27-127">Beschreibung des Szenarios</span><span class="sxs-lookup"><span data-stu-id="e6e27-127">Scenario description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e6e27-128">In App-v 5,0 über APP-v 5,0 SP2 Plus Hotfixes</span><span class="sxs-lookup"><span data-stu-id="e6e27-128">In App-V 5.0 through App-V 5.0 SP2 plus hotfixes</span></span></p></td>
<td align="left"><p><span data-ttu-id="e6e27-129">Dieser Fehler tritt unabhängig davon auf, ob Offline Dateien aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="e6e27-129">This failure will occur regardless of whether Offline Files is enabled.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e6e27-130">In App-V 5,0 SP3 und höher</span><span class="sxs-lookup"><span data-stu-id="e6e27-130">In App-V 5.0 SP3 and later</span></span></p></td>
<td align="left"><p><span data-ttu-id="e6e27-131">Wenn die nicht verfügbare Netzwerkfreigabe für Offline Dateien aktiviert wurde, wird die App-V-Anwendung erfolgreich gestartet.</span><span class="sxs-lookup"><span data-stu-id="e6e27-131">If the unavailable network share has been enabled for Offline Files, the App-V application will start successfully.</span></span></p></td>
</tr>
</tbody>
</table>
<p> </p></li>
</ul></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-folder-redir-cfg"></a><span data-ttu-id="e6e27-132">Konfigurieren der Ordnerumleitung zur Verwendung mit App-V</span><span class="sxs-lookup"><span data-stu-id="e6e27-132">How to configure folder redirection for use with App-V</span></span>


<span data-ttu-id="e6e27-133">Die Ordnerumleitung kann auf verschiedene Ordner wie Desktop, eigene Dateien, meine Bilder usw. angewendet werden. Der einzige Ordner, der sich auf die Verwendung von App-V-Anwendungen auswirkt, ist jedoch der Roaming-AppData-Ordner des Benutzers (% APPDATA%).</span><span class="sxs-lookup"><span data-stu-id="e6e27-133">Folder redirection can be applied to different folders, such as Desktop, My Documents, My Pictures, etc. However, the only folder that impacts the use of App-V applications is the user’s roaming AppData folder (%AppData%).</span></span> <span data-ttu-id="e6e27-134">Sie können die Ordnerumleitung auf alle anderen unterstützten Ordner anwenden, ohne Auswirkungen auf App-V zu haben.</span><span class="sxs-lookup"><span data-stu-id="e6e27-134">You can apply folder redirection to any other supported folders without impacting App-V.</span></span>

## <a href="" id="bkmk-folder-redir-works"></a><span data-ttu-id="e6e27-135">Funktionsweise der Ordnerumleitung mit App-V</span><span class="sxs-lookup"><span data-stu-id="e6e27-135">How folder redirection works with App-V</span></span>


<span data-ttu-id="e6e27-136">In der folgenden Tabelle wird beschrieben, wie die Ordnerumleitung funktioniert, wenn% APPDATA% an ein Netzwerk umgeleitet wird und wenn Sie die oben in diesem Artikel aufgelisteten Anforderungen erfüllt haben.</span><span class="sxs-lookup"><span data-stu-id="e6e27-136">The following table describes how folder redirection works when %AppData% is redirected to a network and when you have met the requirements listed earlier in this article.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="e6e27-137">Zustand der virtuellen Umgebung</span><span class="sxs-lookup"><span data-stu-id="e6e27-137">Virtual environment state</span></span></th>
<th align="left"><span data-ttu-id="e6e27-138">Aktion, die Eintritt</span><span class="sxs-lookup"><span data-stu-id="e6e27-138">Action that occurs</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e6e27-139">Wenn die virtuelle Umgebung gestartet wird</span><span class="sxs-lookup"><span data-stu-id="e6e27-139">When the virtual environment starts</span></span></p></td>
<td align="left"><p><span data-ttu-id="e6e27-140">Der AppData-Ordner des virtuellen Dateisystems (VFS) wird dem lokalen AppData-Ordner (% LocalAppData%) zugeordnet. anstelle des Roaming-APPDATA-Ordners (% APPDATA%) des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="e6e27-140">The virtual file system (VFS) AppData folder is mapped to the local AppData folder (%LocalAppData%) instead of to the user’s roaming AppData folder (%AppData%).</span></span></p>
<ul>
<li><p><span data-ttu-id="e6e27-141">LocalAppData enthält einen lokalen Cache des Roaming-APPDATA-Ordners des Benutzers für das verwendete Paket.</span><span class="sxs-lookup"><span data-stu-id="e6e27-141">LocalAppData contains a local cache of the user’s roaming AppData folder for the package in use.</span></span> <span data-ttu-id="e6e27-142">Der lokale Cache befindet sich unter:</span><span class="sxs-lookup"><span data-stu-id="e6e27-142">The local cache is located under:</span></span></p>
<p><code>%LocalAppData%\Microsoft\AppV\Client\VFS\PackageGUID\AppData</code></p></li>
<li><p><span data-ttu-id="e6e27-143">Die neuesten Daten aus dem Roaming-AppData-Ordner des Benutzers werden in die Daten kopiert und ersetzt, die sich derzeit im lokalen Cache befinden.</span><span class="sxs-lookup"><span data-stu-id="e6e27-143">The latest data from the user’s roaming AppData folder is copied to and replaces the data currently in the local cache.</span></span></p></li>
<li><p><span data-ttu-id="e6e27-144">Während die virtuelle Umgebung ausgeführt wird, werden die Daten weiterhin im lokalen Cache gespeichert.</span><span class="sxs-lookup"><span data-stu-id="e6e27-144">While the virtual environment is running, data continues to be saved to the local cache.</span></span> <span data-ttu-id="e6e27-145">Daten werden nur von% LocalAppData% bereitgestellt und nicht verschoben oder mit% APPDATA% synchronisiert, bis der Endbenutzer den Computer herunterfährt.</span><span class="sxs-lookup"><span data-stu-id="e6e27-145">Data is served only out of %LocalAppData% and is not moved or synchronized with %AppData% until the end user shuts down the computer.</span></span></p></li>
<li><p><span data-ttu-id="e6e27-146">Einträge im AppData-Ordner werden über den Benutzerkontext und nicht über den Systemkontext erstellt.</span><span class="sxs-lookup"><span data-stu-id="e6e27-146">Entries to the AppData folder are made using the user context, not the system context.</span></span></p></li>
</ul>
<div class="alert">
<strong><span data-ttu-id="e6e27-147">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="e6e27-147">Note</span></span></strong><br/><p><span data-ttu-id="e6e27-148">Bei der Umleitung des App-V-Client Ordners können Dateien manchmal nicht von% APPDATA% auf% LocalAppData% verschoben werden.</span><span class="sxs-lookup"><span data-stu-id="e6e27-148">The App-V client folder redirection sometimes fails to move files from %AppData% to %LocalAppData%.</span></span> <span data-ttu-id="e6e27-149">Weitere Informationen finden Sie unter <a href="release-notes-for-app-v-50-sp2.md#bkmk-folderredirection" data-raw-source="[Release Notes for App-V 5.0 SP2](release-notes-for-app-v-50-sp2.md#bkmk-folderredirection)"> Versionshinweise für App-V 5,0 SP2 </a> .</span><span class="sxs-lookup"><span data-stu-id="e6e27-149">See <a href="release-notes-for-app-v-50-sp2.md#bkmk-folderredirection" data-raw-source="[Release Notes for App-V 5.0 SP2](release-notes-for-app-v-50-sp2.md#bkmk-folderredirection)">Release Notes for App-V 5.0 SP2</a>.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e6e27-150">Wenn die virtuelle Umgebung heruntergefahren wird</span><span class="sxs-lookup"><span data-stu-id="e6e27-150">When the virtual environment shuts down</span></span></p></td>
<td align="left"><p><span data-ttu-id="e6e27-151">Die lokalen zwischengespeicherten Daten in APPDATA (Roaming) werden gezippt und in% APPDATA% in den Ordner "echte" Roaming-APPDATA kopiert.</span><span class="sxs-lookup"><span data-stu-id="e6e27-151">The local cached data in AppData (roaming) is zipped up and copied to the “real” roaming AppData folder in %AppData%.</span></span> <span data-ttu-id="e6e27-152">Ein Zeitstempel, der den letzten bekannten Upload angibt, wird gleichzeitig als Registrierungsschlüssel unter gespeichert:</span><span class="sxs-lookup"><span data-stu-id="e6e27-152">A time stamp, which indicates the last known upload, is simultaneously saved as a registry key under:</span></span></p>
<p><code>HKCU\Software\Microsoft\AppV\Client\Packages&amp;lt;PACKAGE_GUID&gt;\AppDataTime</code></p>
<p><span data-ttu-id="e6e27-153">Zur Bereitstellung von Redundanz speichert App-V die drei letzten Kopien der komprimierten Daten unter% APPDATA%.</span><span class="sxs-lookup"><span data-stu-id="e6e27-153">To provide redundancy, App-V keeps the three most recent copies of the compressed data under %AppData%.</span></span></p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-folder-redir-overview"></a><span data-ttu-id="e6e27-154">Übersicht über die Ordnerumleitung</span><span class="sxs-lookup"><span data-stu-id="e6e27-154">Overview of folder redirection</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e6e27-155">Zweck</span><span class="sxs-lookup"><span data-stu-id="e6e27-155">Purpose</span></span></p></td>
<td align="left"><p><span data-ttu-id="e6e27-156">Ermöglicht es Endbenutzern, mit Dateien zu arbeiten, die in einen anderen Ordner umgeleitet wurden, als ob die Dateien noch auf dem lokalen Laufwerk vorhanden waren.</span><span class="sxs-lookup"><span data-stu-id="e6e27-156">Enables end users to work with files, which have been redirected to another folder, as if the files still existed on the local drive.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e6e27-157">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e6e27-157">Description</span></span></p></td>
<td align="left"><p><span data-ttu-id="e6e27-158">Mit der Ordnerumleitung können Benutzer und Administratoren den Pfad eines Ordners an einen Netzwerkspeicherort umleiten.</span><span class="sxs-lookup"><span data-stu-id="e6e27-158">Folder redirection allows users and administrators to redirect the path of a folder to a network location.</span></span> <span data-ttu-id="e6e27-159">Die Dokumente im Ordner stehen dem Benutzer auf jedem Computer im Netzwerk zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="e6e27-159">The documents in the folder are available to the user from any computer on the network.</span></span></p>
<ul>
<li><p><span data-ttu-id="e6e27-160">Mit der Ordnerumleitung können Benutzer und Administratoren den Pfad eines Ordners an einen Netzwerkspeicherort umleiten.</span><span class="sxs-lookup"><span data-stu-id="e6e27-160">Folder redirection allows users and administrators to redirect the path of a folder to a network location.</span></span> <span data-ttu-id="e6e27-161">Die Dokumente im Ordner stehen dem Benutzer auf jedem Computer im Netzwerk zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="e6e27-161">The documents in the folder are available to the user from any computer on the network.</span></span></p></li>
<li><p><span data-ttu-id="e6e27-162">Der neue Speicherort kann ein Ordner auf dem lokalen Computer oder ein Ordner in einem freigegebenen Netzwerk sein.</span><span class="sxs-lookup"><span data-stu-id="e6e27-162">The new location can be a folder on the local computer or a folder on a shared network.</span></span></p></li>
<li><p><span data-ttu-id="e6e27-163">Durch die Ordnerumleitung werden die Dateien sofort aktualisiert, während Roamingdaten in der Regel synchronisiert werden, wenn sich der Benutzer anmeldet oder abmeldet.</span><span class="sxs-lookup"><span data-stu-id="e6e27-163">Folder redirection updates the files immediately, whereas roaming data is typically synchronized when the user logs in or logs off.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e6e27-164">Verwendungsbeispiel</span><span class="sxs-lookup"><span data-stu-id="e6e27-164">Usage example</span></span></p></td>
<td align="left"><p><span data-ttu-id="e6e27-165">Sie können den Ordner "Dokumente", der in der Regel auf der lokalen Festplatte des Computers&#39;gespeichert ist, an einen Netzwerkspeicherort umleiten.</span><span class="sxs-lookup"><span data-stu-id="e6e27-165">You can redirect the Documents folder, which is usually stored on the computer&#39;s local hard disk, to a network location.</span></span> <span data-ttu-id="e6e27-166">Der Benutzer kann von jedem Computer im Netzwerk aus auf die Dokumente im Ordner zugreifen.</span><span class="sxs-lookup"><span data-stu-id="e6e27-166">The user can access the documents in the folder from any computer on the network.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e6e27-167">Weitere Ressourcen</span><span class="sxs-lookup"><span data-stu-id="e6e27-167">More resources</span></span></p></td>
<td align="left"><p><a href="https://technet.microsoft.com/library/cc778976.aspx" data-raw-source="[Folder redirection overview](https://technet.microsoft.com/library/cc778976.aspx)"><span data-ttu-id="e6e27-168">Übersicht über Ordnerumleitung</span><span class="sxs-lookup"><span data-stu-id="e6e27-168">Folder redirection overview</span></span></a></p></td>
</tr>
</tbody>
</table>
















