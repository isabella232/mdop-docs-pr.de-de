---
title: So stellen Sie App-V-Client bereit
description: So stellen Sie App-V-Client bereit
author: dansimp
ms.assetid: 981f57c9-56c3-45da-8261-0972bfad3e5b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/01/2016
ms.openlocfilehash: ea216f6b86820f752e0c0ac693470eac72cb847a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805492"
---
# <span data-ttu-id="3feff-103">So stellen Sie App-V-Client bereit</span><span class="sxs-lookup"><span data-stu-id="3feff-103">How to Deploy the App-V Client</span></span>


<span data-ttu-id="3feff-104">Gehen Sie wie folgt vor, um den Microsoft Application Virtualization (App-V) 5,1-Client und den Remote Desktop Dienste-Client zu installieren.</span><span class="sxs-lookup"><span data-stu-id="3feff-104">Use the following procedure to install the Microsoft Application Virtualization (App-V) 5.1 client and Remote Desktop Services client.</span></span> <span data-ttu-id="3feff-105">Sie müssen die Version des Clients installieren, die dem Betriebssystem des Zielcomputers entspricht.</span><span class="sxs-lookup"><span data-stu-id="3feff-105">You must install the version of the client that matches the operating system of the target computer.</span></span>

<a href="" id="bkmk-clt-install-prereqs"></a>**<span data-ttu-id="3feff-106">Was zu tun ist, bevor Sie beginnen</span><span class="sxs-lookup"><span data-stu-id="3feff-106">What to do before you start</span></span>**

1. <span data-ttu-id="3feff-107">Überprüfen und installieren Sie die erforderlichen Softwarevoraussetzungen:</span><span class="sxs-lookup"><span data-stu-id="3feff-107">Review and install the software prerequisites:</span></span>

   <span data-ttu-id="3feff-108">Installieren Sie die erforderliche Software, die der Version von App-V entspricht, die Sie installieren:</span><span class="sxs-lookup"><span data-stu-id="3feff-108">Install the prerequisite software that corresponds to the version of App-V that you are installing:</span></span>

   -   [<span data-ttu-id="3feff-109">Informationen zu App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="3feff-109">About App-V 5.1</span></span>](about-app-v-51.md)

   -   [<span data-ttu-id="3feff-110">Voraussetzungen für App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="3feff-110">App-V 5.1 Prerequisites</span></span>](app-v-51-prerequisites.md)

2. <span data-ttu-id="3feff-111">Überprüfen Sie die Client Koexistenz und die nicht unterstützten Szenarios, wie Sie für Ihre Installation gelten:</span><span class="sxs-lookup"><span data-stu-id="3feff-111">Review the client coexistence and unsupported scenarios, as applicable to your installation:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="3feff-112">Bereitstellen von nebeneinander vorhandenen App-V-Clients</span><span class="sxs-lookup"><span data-stu-id="3feff-112">Deploying coexisting App-V clients</span></span></p></td>
   <td align="left"><p><a href="planning-for-the-app-v-51-sequencer-and-client-deployment.md" data-raw-source="[Planning for the App-V 5.1 Sequencer and Client Deployment](planning-for-the-app-v-51-sequencer-and-client-deployment.md)"><span data-ttu-id="3feff-113">Planen für die Bereitstellung von App-V 5.1 Sequencer und App-V-Client</span><span class="sxs-lookup"><span data-stu-id="3feff-113">Planning for the App-V 5.1 Sequencer and Client Deployment</span></span></a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="3feff-114">Nicht unterstützte oder begrenzte Installationsszenarien</span><span class="sxs-lookup"><span data-stu-id="3feff-114">Unsupported or limited installation scenarios</span></span></p></td>
   <td align="left"><p><span data-ttu-id="3feff-115">Weitere Informationen finden Sie im Abschnitt "Client" in <a href="app-v-51-supported-configurations.md" data-raw-source="[App-V 5.1 Supported Configurations](app-v-51-supported-configurations.md)"> App-V 5,1 Unterstützte Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="3feff-115">See the client section in <a href="app-v-51-supported-configurations.md" data-raw-source="[App-V 5.1 Supported Configurations](app-v-51-supported-configurations.md)">App-V 5.1 Supported Configurations</span></span></a></p></td>
   </tr>
   </tbody>
   </table>



3. <span data-ttu-id="3feff-116">Überprüfen Sie die Speicherorte für Clientregistrierung, Protokoll und Informationen zur Problembehandlung:</span><span class="sxs-lookup"><span data-stu-id="3feff-116">Review the locations for client registry, log, and troubleshooting information:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3feff-117">Client Registrierungsinformationen</span><span class="sxs-lookup"><span data-stu-id="3feff-117">Client registry information</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="3feff-118">Standardmäßig werden die Clientinformationen nach der Installation des App-V 5,1-Clients in der Registrierung im folgenden Registrierungsschlüssel gespeichert:</span><span class="sxs-lookup"><span data-stu-id="3feff-118">By default, after you install the App-V 5.1 client, the client information is stored in the registry in the following registry key:</span></span></p>
<p><strong><span data-ttu-id="3feff-119">HKEY_LOCAL_MACHINE \ Software \ Microsoft \ APPV \ Client</span><span class="sxs-lookup"><span data-stu-id="3feff-119">HKEY_LOCAL_MACHINE \ SOFTWARE \ MICROSOFT \ APPV \ CLIENT</span></span></strong></p></li>
<li><p><span data-ttu-id="3feff-120">Wenn Sie ein virtualisiertes Paket auf einem Computer bereitstellen, auf dem der App-V-Client ausgeführt wird, werden die zugehörigen Paketdaten an folgendem Speicherort gespeichert:</span><span class="sxs-lookup"><span data-stu-id="3feff-120">When you deploy a virtualized package to a computer that is running the App-V client, the associated package data is stored in the following location:</span></span></p>
<p><strong><span data-ttu-id="3feff-121">C: \ ProgramData \ App-V</span><span class="sxs-lookup"><span data-stu-id="3feff-121">C: \ ProgramData \ App-V</span></span></strong></p>
<p><span data-ttu-id="3feff-122">Sie können diesen Speicherort jedoch mit dem folgenden Registrierungsschlüssel neu konfigurieren:</span><span class="sxs-lookup"><span data-stu-id="3feff-122">However, you can reconfigure this location with the following registry key:</span></span></p>
<p><strong><span data-ttu-id="3feff-123">HKEY_LOCAL_MACHINE \ Software \ Microsoft \ Software \ Microsoft \ APPV \ Client \ Streaming \ PACKAGEINSTALLATIONROOT</span><span class="sxs-lookup"><span data-stu-id="3feff-123">HKEY_LOCAL_MACHINE \ SOFTWARE \ MICROSOFT \ SOFTWARE \ MICROSOFT \ APPV \ CLIENT \ STREAMING \ PACKAGEINSTALLATIONROOT</span></span></strong></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3feff-124">Client Protokolldateien</span><span class="sxs-lookup"><span data-stu-id="3feff-124">Client log files</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="3feff-125">Suchen Sie für Protokolldateiinformationen, die dem App-V 5,1-Client zugeordnet sind, im folgenden Protokoll:</span><span class="sxs-lookup"><span data-stu-id="3feff-125">For log file information that is associated with the App-V 5.1 Client, search in the following log:</span></span></p>
<p><strong><span data-ttu-id="3feff-126">Ereignisprotokolle/Anwendungen und Dienstprotokolle/Microsoft/AppV</span><span class="sxs-lookup"><span data-stu-id="3feff-126">Event logs / Applications and Services Logs / Microsoft / AppV</span></span></strong></p></li>
<li><p><span data-ttu-id="3feff-127">In App-V 5,0 SP3 wurden einige Protokolle konsolidiert und an den folgenden Speicherort verschoben:</span><span class="sxs-lookup"><span data-stu-id="3feff-127">In App-V 5.0 SP3, some logs were consolidated and moved to the following location:</span></span></p>
<p><strong><span data-ttu-id="3feff-128">Ereignisprotokolle/Anwendungen und Dienstprotokolle/Microsoft/AppV/ServiceLog</span><span class="sxs-lookup"><span data-stu-id="3feff-128">Event logs/Applications and Services Logs/Microsoft/AppV/ServiceLog</span></span></strong></p>
<p><span data-ttu-id="3feff-129">Eine Liste der verschobenen Protokolle finden Sie unter <a href="about-app-v-50-sp3.md#bkmk-event-logs-moved" data-raw-source="[About App-V 5.0 SP3](about-app-v-50-sp3.md#bkmk-event-logs-moved)"> Informationen zu App-V 5,0 SP3 </a> .</span><span class="sxs-lookup"><span data-stu-id="3feff-129">For a list of the moved logs, see <a href="about-app-v-50-sp3.md#bkmk-event-logs-moved" data-raw-source="[About App-V 5.0 SP3](about-app-v-50-sp3.md#bkmk-event-logs-moved)">About App-V 5.0 SP3</a>.</span></span></p></li>
<li><p><span data-ttu-id="3feff-130">Pakete, die derzeit auf Computern gespeichert sind, auf denen der App-V 5,1-Client ausgeführt wird, werden an folgendem Speicherort gespeichert:</span><span class="sxs-lookup"><span data-stu-id="3feff-130">Packages that are currently stored on computers that run the App-V 5.1 Client are saved to the following location:</span></span></p>
<p><strong><span data-ttu-id="3feff-131">C:\ProgramData\App-V &amp; lt; Paket-ID &gt; &amp; lt; Versions-ID&gt;</span><span class="sxs-lookup"><span data-stu-id="3feff-131">C:\ProgramData\App-V&amp;lt;package id&gt;&amp;lt;version id&gt;</span></span></strong></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3feff-132">Informationen zur Problembehandlung bei der Client Installation</span><span class="sxs-lookup"><span data-stu-id="3feff-132">Client installation troubleshooting information</span></span></p></td>
<td align="left"><p><span data-ttu-id="3feff-133">Sehen Sie sich das Fehlerprotokoll im <strong> Ordner% Temp% an </strong> .</span><span class="sxs-lookup"><span data-stu-id="3feff-133">See the error log in the <strong>%temp%</strong> folder.</span></span> <span data-ttu-id="3feff-134">Wenn Sie die Protokolldateien überprüfen möchten, klicken Sie auf <strong> Start </strong> , geben Sie <strong> % Temp% </strong> ein, und suchen Sie dann nach dem <strong> appv_ Protokoll </strong> .</span><span class="sxs-lookup"><span data-stu-id="3feff-134">To review the log files, click <strong>Start</strong>, type <strong>%temp%</strong>, and then look for the <strong>appv_ log</strong>.</span></span></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="3feff-135">So installieren Sie den App-V 5,1-Client</span><span class="sxs-lookup"><span data-stu-id="3feff-135">To install the App-V 5.1 Client</span></span>**

1.  <span data-ttu-id="3feff-136">Kopieren Sie die App-V 5,1-Clientinstallationsdatei auf den Computer, auf dem Sie installiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="3feff-136">Copy the App-V 5.1 client installation file to the computer on which it will be installed.</span></span> <span data-ttu-id="3feff-137">Wählen Sie eine der folgenden Clienttypen aus:</span><span class="sxs-lookup"><span data-stu-id="3feff-137">Choose from the following client types:</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="3feff-138">Clienttyp</span><span class="sxs-lookup"><span data-stu-id="3feff-138">Client type</span></span></th>
    <th align="left"><span data-ttu-id="3feff-139">Zu verwendende Datei</span><span class="sxs-lookup"><span data-stu-id="3feff-139">File to use</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="3feff-140">Standard Version des Clients</span><span class="sxs-lookup"><span data-stu-id="3feff-140">Standard version of the client</span></span></p></td>
    <td align="left"><p><strong><span data-ttu-id="3feff-141">appv_client_setup.exe</span><span class="sxs-lookup"><span data-stu-id="3feff-141">appv_client_setup.exe</span></span></strong></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="3feff-142">Version des Clients für Remote Desktop Dienste</span><span class="sxs-lookup"><span data-stu-id="3feff-142">Remote Desktop Services version of the client</span></span></p></td>
    <td align="left"><p><strong><span data-ttu-id="3feff-143">appv_client_setup_rds.exe</span><span class="sxs-lookup"><span data-stu-id="3feff-143">appv_client_setup_rds.exe</span></span></strong></p></td>
    </tr>
    </tbody>
    </table>



2.  <span data-ttu-id="3feff-144">Doppelklicken Sie auf die Installationsdatei, und klicken Sie auf **Installieren**.</span><span class="sxs-lookup"><span data-stu-id="3feff-144">Double-click the installation file, and click **Install**.</span></span> <span data-ttu-id="3feff-145">Vor Beginn der Installation überprüft das Installationsprogramm den Computer auf alle fehlenden [App-V 5,1-Voraussetzungen](app-v-51-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="3feff-145">Before the installation begins, the installer checks the computer for any missing [App-V 5.1 Prerequisites](app-v-51-prerequisites.md).</span></span>

3.  <span data-ttu-id="3feff-146">Überprüfen und akzeptieren Sie die Software-Lizenzbestimmungen, wählen Sie aus, ob Sie Microsoft Update verwenden möchten und ob Sie am Programm zur Verbesserung der Benutzerfreundlichkeit von Microsoft teilnehmen möchten, und klicken Sie auf **Installieren**.</span><span class="sxs-lookup"><span data-stu-id="3feff-146">Review and accept the Software License Terms, choose whether to use Microsoft Update and whether to participate in the Microsoft Customer Experience Improvement Program, and click **Install**.</span></span>

4.  <span data-ttu-id="3feff-147">Klicken Sie auf der Seite **Setup erfolgreich abgeschlossen** auf **Schließen**.</span><span class="sxs-lookup"><span data-stu-id="3feff-147">On the **Setup completed successfully** page, click **Close**.</span></span>

    <span data-ttu-id="3feff-148">Bei der Installation werden die folgenden Einträge für den App-V-Client in **Programmen**erstellt:</span><span class="sxs-lookup"><span data-stu-id="3feff-148">The installation creates the following entries for the App-V client in **Programs**:</span></span>

    -   **<span data-ttu-id="3feff-149">EXE</span><span class="sxs-lookup"><span data-stu-id="3feff-149">.exe</span></span>**

    -   **<span data-ttu-id="3feff-150">.msi</span><span class="sxs-lookup"><span data-stu-id="3feff-150">.msi</span></span>**

    -   **<span data-ttu-id="3feff-151">Sprachpaket</span><span class="sxs-lookup"><span data-stu-id="3feff-151">language pack</span></span>**

        **<span data-ttu-id="3feff-152">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="3feff-152">Note</span></span>**  
        <span data-ttu-id="3feff-153">Nach der Installation kann nur die exe-Datei deinstalliert werden.</span><span class="sxs-lookup"><span data-stu-id="3feff-153">After the installation, only the .exe file can be uninstalled.</span></span>



**<span data-ttu-id="3feff-154">So installieren Sie den App-V 5,1-Client mithilfe eines Skripts</span><span class="sxs-lookup"><span data-stu-id="3feff-154">To install the App-V 5.1 client using a script</span></span>**

1. <span data-ttu-id="3feff-155">Installieren Sie alle erforderlichen Softwarevoraussetzungen auf den Zielcomputern.</span><span class="sxs-lookup"><span data-stu-id="3feff-155">Install all of the required prerequisite software on the target computers.</span></span> <span data-ttu-id="3feff-156">Schauen Sie [sich an, was Sie vor Beginn tun sollten](#bkmk-clt-install-prereqs).</span><span class="sxs-lookup"><span data-stu-id="3feff-156">See [What to do before you start](#bkmk-clt-install-prereqs).</span></span> <span data-ttu-id="3feff-157">Wenn Sie den Client mithilfe einer MSI-Datei installieren, schlägt die Installation fehl, wenn keine Voraussetzungen vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="3feff-157">If you install the client by using an .msi file, the installation will fail if any prerequisites are missing.</span></span>

2. <span data-ttu-id="3feff-158">Wenn Sie ein Skript zum Installieren des App-V 5,1-Clients verwenden möchten, verwenden Sie die folgenden Parameter mit **appv\_client\_setup.exe**.</span><span class="sxs-lookup"><span data-stu-id="3feff-158">To use a script to install the App-V 5.1 client, use the following parameters with **appv\_client\_setup.exe**.</span></span>

   **<span data-ttu-id="3feff-159">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="3feff-159">Note</span></span>**  
   <span data-ttu-id="3feff-160">Der Client Windows Installer (MSI) unterstützt den gleichen Satz von Schaltern, mit Ausnahme des **/Log** -Parameters.</span><span class="sxs-lookup"><span data-stu-id="3feff-160">The client Windows Installer (.msi) supports the same set of switches, except for the **/LOG** parameter.</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="3feff-161">/INSTALLDIR</span><span class="sxs-lookup"><span data-stu-id="3feff-161">/INSTALLDIR</span></span></p></td>
   <td align="left"><p><span data-ttu-id="3feff-162">Gibt das Installationsverzeichnis an.</span><span class="sxs-lookup"><span data-stu-id="3feff-162">Specifies the installation directory.</span></span> <span data-ttu-id="3feff-163">Verwendungsbeispiel: <strong> /INSTALLDIR = C:\Program Files\AppV Client</span><span class="sxs-lookup"><span data-stu-id="3feff-163">Example usage: <strong>/INSTALLDIR=C:\Program Files\AppV Client</span></span></strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="3feff-164">/CEIPOPTIN</span><span class="sxs-lookup"><span data-stu-id="3feff-164">/CEIPOPTIN</span></span></p></td>
   <td align="left"><p><span data-ttu-id="3feff-165">Ermöglicht die Teilnahme am Programm zur Verbesserung der Benutzerfreundlichkeit.</span><span class="sxs-lookup"><span data-stu-id="3feff-165">Enables participation in the Customer Experience Improvement Program.</span></span> <span data-ttu-id="3feff-166">Beispiel Verwendung: <strong> /CEIPOPTIN = [0 | 1]</span><span class="sxs-lookup"><span data-stu-id="3feff-166">Example usage: <strong>/CEIPOPTIN=[0|1]</span></span></strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="3feff-167">/MUOPTIN</span><span class="sxs-lookup"><span data-stu-id="3feff-167">/MUOPTIN</span></span></p></td>
   <td align="left"><p><span data-ttu-id="3feff-168">Aktiviert Microsoft Update.</span><span class="sxs-lookup"><span data-stu-id="3feff-168">Enables Microsoft Update.</span></span> <span data-ttu-id="3feff-169">Beispiel Verwendung: <strong> /MUOPTIN = [0 | 1]</span><span class="sxs-lookup"><span data-stu-id="3feff-169">Example usage: <strong>/MUOPTIN=[0|1]</span></span></strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="3feff-170">/PACKAGEINSTALLATIONROOT</span><span class="sxs-lookup"><span data-stu-id="3feff-170">/PACKAGEINSTALLATIONROOT</span></span></p></td>
   <td align="left"><p><span data-ttu-id="3feff-171">Gibt das Verzeichnis an, in dem alle neuen Anwendungen und Updates installiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="3feff-171">Specifies the directory in which to install all new applications and updates.</span></span> <span data-ttu-id="3feff-172">Beispiel Verwendung: <strong> /PACKAGEINSTALLATIONROOT =&#39;C:\app-V-Pakete&#39;</span><span class="sxs-lookup"><span data-stu-id="3feff-172">Example usage: <strong>/PACKAGEINSTALLATIONROOT=&#39;C:\App-V Packages&#39;</span></span></strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="3feff-173">/PACKAGESOURCEROOT</span><span class="sxs-lookup"><span data-stu-id="3feff-173">/PACKAGESOURCEROOT</span></span></p></td>
   <td align="left"><p><span data-ttu-id="3feff-174">Überschreibt den Quellspeicherort zum Herunterladen von Paketinhalten.</span><span class="sxs-lookup"><span data-stu-id="3feff-174">Overrides the source location for downloading package content.</span></span> <span data-ttu-id="3feff-175">Beispiel Verwendung: <strong> /PACKAGESOURCEROOT =&#39;<a href="http://packageStore" data-raw-source="http://packageStore"> http://packageStore </a>&#39;</span><span class="sxs-lookup"><span data-stu-id="3feff-175">Example usage: <strong>/PACKAGESOURCEROOT=&#39;<a href="http://packageStore" data-raw-source="http://packageStore">http://packageStore</a>&#39;</span></span></strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="3feff-176">/AUTOLOAD</span><span class="sxs-lookup"><span data-stu-id="3feff-176">/AUTOLOAD</span></span></p></td>
   <td align="left"><p><span data-ttu-id="3feff-177">Gibt an, wie neue Pakete von App-V 5,1 auf einem bestimmten Computer geladen werden.</span><span class="sxs-lookup"><span data-stu-id="3feff-177">Specifies how new packages will be loaded by App-V 5.1 on a specific computer.</span></span> <span data-ttu-id="3feff-178">Die folgenden Optionen sind aktiviert: [1]; Alle Pakete automatisch laden [2]; oder laden Sie keine Pakete automatisch [0]. <strong> Beispiel Verwendung:/AUTOLOAD = [0 | 1 | 2]</span><span class="sxs-lookup"><span data-stu-id="3feff-178">The following options are enabled: [1]; automatically load all packages [2]; or automatically load no packages [0].<strong>Example usage: /AUTOLOAD=[0|1|2]</span></span></strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="3feff-179">/SHAREDCONTENTSTOREMODE</span><span class="sxs-lookup"><span data-stu-id="3feff-179">/SHAREDCONTENTSTOREMODE</span></span></p></td>
   <td align="left"><p><span data-ttu-id="3feff-180">Gibt an, dass Streaming-Paketinhalt nicht auf der lokalen Festplatte gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="3feff-180">Specifies that streamed package contents will be not be saved to the local hard disk.</span></span> <span data-ttu-id="3feff-181">Beispiel Verwendung: <strong> /SHAREDCONTENTSTOREMODE = [0 | 1]</span><span class="sxs-lookup"><span data-stu-id="3feff-181">Example usage: <strong>/SHAREDCONTENTSTOREMODE=[0|1]</span></span></strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="3feff-182">/MIGRATIONMODE</span><span class="sxs-lookup"><span data-stu-id="3feff-182">/MIGRATIONMODE</span></span></p></td>
   <td align="left"><p><span data-ttu-id="3feff-183">Ermöglicht es dem App-V 5,1-Client, die Verknüpfungen und FTA zu ändern, die den Paketen zugeordnet sind, die mit einer früheren Version erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="3feff-183">Allows the App-V 5.1 client to modify the shortcuts and FTAs that are associated with the packages that are created with a previous version.</span></span> <span data-ttu-id="3feff-184">Beispiel Verwendung: <strong> /MIGRATIONMODE = [0 | 1]</span><span class="sxs-lookup"><span data-stu-id="3feff-184">Example usage: <strong>/MIGRATIONMODE=[0|1]</span></span></strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="3feff-185">/ENABLEPACKAGESCRIPTS</span><span class="sxs-lookup"><span data-stu-id="3feff-185">/ENABLEPACKAGESCRIPTS</span></span></p></td>
   <td align="left"><p><span data-ttu-id="3feff-186">Aktiviert die Skripts, die in der Datei des paketmanifests oder der Konfigurationsdateien definiert sind, die ausgeführt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="3feff-186">Enables the scripts that are defined in the package manifest file or configuration files that should run.</span></span> <span data-ttu-id="3feff-187">Beispiel Verwendung: <strong> /ENABLEPACKAGESCRIPTS = [0 | 1]</span><span class="sxs-lookup"><span data-stu-id="3feff-187">Example usage: <strong>/ENABLEPACKAGESCRIPTS=[0|1]</span></span></strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="3feff-188">/ROAMINGREGISTRYEXCLUSIONS</span><span class="sxs-lookup"><span data-stu-id="3feff-188">/ROAMINGREGISTRYEXCLUSIONS</span></span></p></td>
   <td align="left"><p><span data-ttu-id="3feff-189">Gibt die Registrierungspfade an, die nicht mit einem Benutzerprofil durchlaufen werden.</span><span class="sxs-lookup"><span data-stu-id="3feff-189">Specifies the registry paths that will not roam with a user profile.</span></span> <span data-ttu-id="3feff-190">Verwendungsbeispiel: <strong> /ROAMINGREGISTRYEXCLUSIONS = software\classes; Software\Clients</span><span class="sxs-lookup"><span data-stu-id="3feff-190">Example usage: <strong>/ROAMINGREGISTRYEXCLUSIONS=software\classes;software\clients</span></span></strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="3feff-191">/ROAMINGFILEEXCLUSIONS</span><span class="sxs-lookup"><span data-stu-id="3feff-191">/ROAMINGFILEEXCLUSIONS</span></span></p></td>
   <td align="left"><p><span data-ttu-id="3feff-192">Gibt die Dateipfade relativ zu% User Profile% an, die nicht mit einem Benutzer&#39;s-Profil Roaming durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="3feff-192">Specifies the file paths relative to %userprofile% that do not roam with a user&#39;s profile.</span></span> <span data-ttu-id="3feff-193">Beispiel Verwendung: <strong> /ROAMINGFILEEXCLUSIONS &#39;Desktop; meine Bilder&#39;</span><span class="sxs-lookup"><span data-stu-id="3feff-193">Example usage: <strong>/ROAMINGFILEEXCLUSIONS &#39;desktop;my pictures&#39;</span></span></strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="3feff-194">/S [1-5] PUBLISHINGSERVERNAME</span><span class="sxs-lookup"><span data-stu-id="3feff-194">/S[1-5]PUBLISHINGSERVERNAME</span></span></p></td>
   <td align="left"><p><span data-ttu-id="3feff-195">Zeigt den Namen des Veröffentlichungsservers an.</span><span class="sxs-lookup"><span data-stu-id="3feff-195">Displays the name of the publishing server.</span></span> <span data-ttu-id="3feff-196">Verwendungsbeispiel: <strong> /S2PUBLISHINGSERVERNAME = MyPublishingServer</span><span class="sxs-lookup"><span data-stu-id="3feff-196">Example usage: <strong>/S2PUBLISHINGSERVERNAME=MyPublishingServer</span></span></strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="3feff-197">/S [1-5] PUBLISHINGSERVERURL</span><span class="sxs-lookup"><span data-stu-id="3feff-197">/S[1-5]PUBLISHINGSERVERURL</span></span></p></td>
   <td align="left"><p><span data-ttu-id="3feff-198">Zeigt die URL des Veröffentlichungsservers an.</span><span class="sxs-lookup"><span data-stu-id="3feff-198">Displays the URL of the publishing server.</span></span> <span data-ttu-id="3feff-199">Verwendungsbeispiel: <strong> /S2PUBLISHINGSERVERURL = \pubserver</span><span class="sxs-lookup"><span data-stu-id="3feff-199">Example usage: <strong>/S2PUBLISHINGSERVERURL=\pubserver</span></span></strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="3feff-200">/S [1-5] GLOBALREFRESHENABLED-</span><span class="sxs-lookup"><span data-stu-id="3feff-200">/S[1-5]GLOBALREFRESHENABLED -</span></span></p></td>
   <td align="left"><p><span data-ttu-id="3feff-201">Aktiviert eine globale Veröffentlichungsaktualisierung.</span><span class="sxs-lookup"><span data-stu-id="3feff-201">Enables a global publishing refresh.</span></span> <span data-ttu-id="3feff-202">Beispiel Verwendung: <strong> /S2GLOBALREFRESHENABLED = [0 | 1]</span><span class="sxs-lookup"><span data-stu-id="3feff-202">Example usage: <strong>/S2GLOBALREFRESHENABLED=[0|1]</span></span></strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="3feff-203">/S [1-5] GLOBALREFRESHONLOGON</span><span class="sxs-lookup"><span data-stu-id="3feff-203">/S[1-5]GLOBALREFRESHONLOGON</span></span></p></td>
   <td align="left"><p><span data-ttu-id="3feff-204">Initiiert eine globale Veröffentlichungsaktualisierung, wenn sich ein Benutzer anmeldet.</span><span class="sxs-lookup"><span data-stu-id="3feff-204">Initiates a global publishing refresh when a user logs on.</span></span> <span data-ttu-id="3feff-205">Beispiel Verwendung: <strong> /S2LOGONREFRESH = [0 | 1]</span><span class="sxs-lookup"><span data-stu-id="3feff-205">Example usage: <strong>/S2LOGONREFRESH=[0|1]</span></span></strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="3feff-206">/S [1-5] GLOBALREFRESHINTERVAL-</span><span class="sxs-lookup"><span data-stu-id="3feff-206">/S[1-5]GLOBALREFRESHINTERVAL -</span></span></p></td>
   <td align="left"><p><span data-ttu-id="3feff-207">Gibt das Aktualisierungsintervall für die Veröffentlichung an, wobei <strong> 0 angibt, dass </strong> Sie nicht regelmäßig aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="3feff-207">Specifies the publishing refresh interval, where <strong>0</strong> indicates do not periodically refresh.</span></span> <span data-ttu-id="3feff-208">Verwendungsbeispiel: <strong> /S2PERIODICREFRESHINTERVAL = [0-744]</span><span class="sxs-lookup"><span data-stu-id="3feff-208">Example usage: <strong>/S2PERIODICREFRESHINTERVAL=[0-744]</span></span></strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="3feff-209">/S [1-5] GLOBALREFRESHINTERVALUNIT</span><span class="sxs-lookup"><span data-stu-id="3feff-209">/S[1-5]GLOBALREFRESHINTERVALUNIT</span></span></p></td>
   <td align="left"><p><span data-ttu-id="3feff-210">Gibt die Intervalleinheit an (Stunden [0], Tage [1]).</span><span class="sxs-lookup"><span data-stu-id="3feff-210">Specifies the interval unit (Hours[0], Days[1]).</span></span> <span data-ttu-id="3feff-211">Beispiel Verwendung: <strong> /S2GLOBALREFRESHINTERVALUNIT = [0 | 1]</span><span class="sxs-lookup"><span data-stu-id="3feff-211">Example usage: <strong>/S2GLOBALREFRESHINTERVALUNIT=[0|1]</span></span></strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="3feff-212">/S [1-5] USERREFRESHENABLED</span><span class="sxs-lookup"><span data-stu-id="3feff-212">/S[1-5]USERREFRESHENABLED</span></span></p></td>
   <td align="left"><p><span data-ttu-id="3feff-213">Aktiviert die Aktualisierung der Benutzer Veröffentlichung.</span><span class="sxs-lookup"><span data-stu-id="3feff-213">Enables user publishing refresh.</span></span> <span data-ttu-id="3feff-214">Beispiel Verwendung: <strong> /S2USERREFRESHENABLED = [0 | 1]</span><span class="sxs-lookup"><span data-stu-id="3feff-214">Example usage: <strong>/S2USERREFRESHENABLED=[0|1]</span></span></strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="3feff-215">/S [1-5] USERREFRESHONLOGON</span><span class="sxs-lookup"><span data-stu-id="3feff-215">/S[1-5]USERREFRESHONLOGON</span></span></p></td>
   <td align="left"><p><span data-ttu-id="3feff-216">Initiiert eine Aktualisierung der Benutzer Veröffentlichung, wenn sich ein Benutzer anmeldet.</span><span class="sxs-lookup"><span data-stu-id="3feff-216">Initiates a user publishing refresh when a user logs on.</span></span> <span data-ttu-id="3feff-217">Beispiel Verwendung: <strong> /S2LOGONREFRESH = [0 | 1]</span><span class="sxs-lookup"><span data-stu-id="3feff-217">Example usage: <strong>/S2LOGONREFRESH=[0|1]</span></span></strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="3feff-218">/S [1-5] USERREFRESHINTERVAL-</span><span class="sxs-lookup"><span data-stu-id="3feff-218">/S[1-5]USERREFRESHINTERVAL -</span></span></p></td>
   <td align="left"><p><span data-ttu-id="3feff-219">Gibt das Aktualisierungsintervall für die Veröffentlichung an, wobei <strong> 0 angibt, dass </strong> Sie nicht regelmäßig aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="3feff-219">Specifies the publishing refresh interval, where <strong>0</strong> indicates do not periodically refresh.</span></span> <span data-ttu-id="3feff-220">Verwendungsbeispiel: <strong> /S2PERIODICREFRESHINTERVAL = [0-744]</span><span class="sxs-lookup"><span data-stu-id="3feff-220">Example usage: <strong>/S2PERIODICREFRESHINTERVAL=[0-744]</span></span></strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="3feff-221">/S [1-5] USERREFRESHINTERVALUNIT</span><span class="sxs-lookup"><span data-stu-id="3feff-221">/S[1-5]USERREFRESHINTERVALUNIT</span></span></p></td>
   <td align="left"><p><span data-ttu-id="3feff-222">Gibt die Intervalleinheit an (Stunden [0], Tage [1]).</span><span class="sxs-lookup"><span data-stu-id="3feff-222">Specifies the interval unit (Hours[0], Days[1]).</span></span> <span data-ttu-id="3feff-223">Beispiel Verwendung: <strong> /S2USERREFRESHINTERVALUNIT = [0 | 1]</span><span class="sxs-lookup"><span data-stu-id="3feff-223">Example usage: <strong>/S2USERREFRESHINTERVALUNIT=[0|1]</span></span></strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="3feff-224">/Log</span><span class="sxs-lookup"><span data-stu-id="3feff-224">/Log</span></span></p></td>
   <td align="left"><p><span data-ttu-id="3feff-225">Gibt einen Speicherort an, an dem die Protokollinformationen gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="3feff-225">Specifies a location where the log information is saved.</span></span> <span data-ttu-id="3feff-226">Der Standardspeicherort ist% Temp%.</span><span class="sxs-lookup"><span data-stu-id="3feff-226">The default location is %Temp%.</span></span> <span data-ttu-id="3feff-227">Verwendungsbeispiel: <strong> /Log C:\logs\log.log</span><span class="sxs-lookup"><span data-stu-id="3feff-227">Example usage: <strong>/log C:\logs\log.log</span></span></strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="3feff-228">/q</span><span class="sxs-lookup"><span data-stu-id="3feff-228">/q</span></span></p></td>
   <td align="left"><p><span data-ttu-id="3feff-229">Gibt eine unbeaufsichtigte Installation an.</span><span class="sxs-lookup"><span data-stu-id="3feff-229">Specifies an unattended installation.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="3feff-230">/Repair</span><span class="sxs-lookup"><span data-stu-id="3feff-230">/REPAIR</span></span></p></td>
   <td align="left"><p><span data-ttu-id="3feff-231">Repariert eine vorherige Clientinstallation.</span><span class="sxs-lookup"><span data-stu-id="3feff-231">Repairs a previous client installation.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="3feff-232">/NORESTART</span><span class="sxs-lookup"><span data-stu-id="3feff-232">/NORESTART</span></span></p></td>
   <td align="left"><p><span data-ttu-id="3feff-233">Verhindert, dass der Computer nach der Clientinstallation neu gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="3feff-233">Prevents the computer from rebooting after the client installation.</span></span></p>
   <p><span data-ttu-id="3feff-234">Der Parameter verhindert, dass der Computer des Endbenutzers nach jedem Update neu gestartet wird, und Sie können den Neustart nach Belieben planen.</span><span class="sxs-lookup"><span data-stu-id="3feff-234">The parameter prevents the end-user computer from rebooting after each update is installed and lets you schedule the reboot at your convenience.</span></span> <span data-ttu-id="3feff-235">So können Sie beispielsweise App-V 5,1 installieren und dann das Hotfix-Paket Y installieren, ohne nach der Installation des Service Packs einen Neustart durchführen zu müssen.</span><span class="sxs-lookup"><span data-stu-id="3feff-235">For example, you can install App-V 5.1 and then install Hotfix Package Y without rebooting after the Service Pack installation.</span></span> <span data-ttu-id="3feff-236">Nach der Installation müssen Sie den Computer neu starten, bevor Sie App-V verwenden.</span><span class="sxs-lookup"><span data-stu-id="3feff-236">After the installation, you must reboot before you start using App-V.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="3feff-237">/Uninstall</span><span class="sxs-lookup"><span data-stu-id="3feff-237">/UNINSTALL</span></span></p></td>
   <td align="left"><p><span data-ttu-id="3feff-238">Deinstalliert den Client.</span><span class="sxs-lookup"><span data-stu-id="3feff-238">Uninstalls the client.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="3feff-239">/ACCEPTEULA</span><span class="sxs-lookup"><span data-stu-id="3feff-239">/ACCEPTEULA</span></span></p></td>
   <td align="left"><p><span data-ttu-id="3feff-240">Akzeptiert den Lizenzvertrag.</span><span class="sxs-lookup"><span data-stu-id="3feff-240">Accepts the license agreement.</span></span> <span data-ttu-id="3feff-241">Dies ist für eine unbeaufsichtigte Installation erforderlich.</span><span class="sxs-lookup"><span data-stu-id="3feff-241">This is required for an unattended installation.</span></span> <span data-ttu-id="3feff-242">Beispiel Verwendung: <strong> /ACCEPTEULA </strong> oder <strong> /ACCEPTEULA = 1 </strong> .</span><span class="sxs-lookup"><span data-stu-id="3feff-242">Example usage: <strong>/ACCEPTEULA</strong> or <strong>/ACCEPTEULA=1</strong>.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="3feff-243">/LAYOUT</span><span class="sxs-lookup"><span data-stu-id="3feff-243">/LAYOUT</span></span></p></td>
   <td align="left"><p><span data-ttu-id="3feff-244">Gibt die zugeordnete Layout-Aktion an.</span><span class="sxs-lookup"><span data-stu-id="3feff-244">Specifies the associated layout action.</span></span> <span data-ttu-id="3feff-245">Außerdem werden die Windows Installer-Dateien (MSI) und Skriptdateien in einen Ordner extrahiert, ohne App-V 5,1 zu installieren.</span><span class="sxs-lookup"><span data-stu-id="3feff-245">It also extracts the Windows Installer (.msi) and script files to a folder without installing App-V 5.1.</span></span> <span data-ttu-id="3feff-246">Es wird kein Wert erwartet.</span><span class="sxs-lookup"><span data-stu-id="3feff-246">No value is expected.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="3feff-247">/LAYOUTDIR</span><span class="sxs-lookup"><span data-stu-id="3feff-247">/LAYOUTDIR</span></span></p></td>
   <td align="left"><p><span data-ttu-id="3feff-248">Gibt das layoutverzeichnis an.</span><span class="sxs-lookup"><span data-stu-id="3feff-248">Specifies the layout directory.</span></span> <span data-ttu-id="3feff-249">Erfordert einen Zeichenfolgenwert.</span><span class="sxs-lookup"><span data-stu-id="3feff-249">Requires a string value.</span></span> <span data-ttu-id="3feff-250">Beispielsyntax: <strong> /LAYOUTDIR = "C:\Application Virtualization Client" </strong> .</span><span class="sxs-lookup"><span data-stu-id="3feff-250">Example usage: <strong>/LAYOUTDIR=”C:\Application Virtualization Client”</strong>.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="3feff-251">/?,/h,/Help</span><span class="sxs-lookup"><span data-stu-id="3feff-251">/?, /h, /help</span></span></p></td>
   <td align="left"><p><span data-ttu-id="3feff-252">Fordert Hilfe zu den vorherigen Installationsparametern an.</span><span class="sxs-lookup"><span data-stu-id="3feff-252">Requests help about the previous installation parameters.</span></span></p></td>
   </tr>
   </tbody>
   </table>



**<span data-ttu-id="3feff-253">So installieren Sie den App-V 5,1-Client mithilfe der Windows Installer-Datei (MSI)</span><span class="sxs-lookup"><span data-stu-id="3feff-253">To install the App-V 5.1 client by using the Windows Installer (.msi) file</span></span>**

1.  <span data-ttu-id="3feff-254">Installieren Sie die erforderlichen Voraussetzungen auf den Zielcomputern.</span><span class="sxs-lookup"><span data-stu-id="3feff-254">Install the required prerequisites on the target computers.</span></span> <span data-ttu-id="3feff-255">Schauen Sie [sich an, was Sie vor Beginn tun sollten](#bkmk-clt-install-prereqs).</span><span class="sxs-lookup"><span data-stu-id="3feff-255">See [What to do before you start](#bkmk-clt-install-prereqs).</span></span> <span data-ttu-id="3feff-256">Wenn keine Voraussetzungen erfüllt sind, schlägt die Installation fehl.</span><span class="sxs-lookup"><span data-stu-id="3feff-256">If any prerequisites are not met, the installation will fail.</span></span>

2.  <span data-ttu-id="3feff-257">Stellen Sie sicher, dass die Zielcomputer keine ausstehenden Neustarts haben, bevor Sie den Client mithilfe der App-V 5,1 Windows Installer-Dateien (MSI) installieren.</span><span class="sxs-lookup"><span data-stu-id="3feff-257">Ensure that the target computers do not have any pending restarts before you install the client using the App-V 5.1 Windows Installer (.msi) files.</span></span> <span data-ttu-id="3feff-258">Die Windows Installer-Dateien kennzeichnen keinen ausstehenden Neustart.</span><span class="sxs-lookup"><span data-stu-id="3feff-258">The Windows Installer files do not flag a pending restart.</span></span>

3.  <span data-ttu-id="3feff-259">Stellen Sie eine der folgenden Windows Installer-Dateien auf dem Zielcomputer bereit.</span><span class="sxs-lookup"><span data-stu-id="3feff-259">Deploy one of the following Windows Installer files to the target computer.</span></span> <span data-ttu-id="3feff-260">Die von Ihnen angegebene Datei muss der Konfiguration des Zielcomputers entsprechen.</span><span class="sxs-lookup"><span data-stu-id="3feff-260">The file that you specify must match the configuration of the target computer.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="3feff-261">Art der Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="3feff-261">Type of deployment</span></span></th>
    <th align="left"><span data-ttu-id="3feff-262">Diese Datei bereitstellen</span><span class="sxs-lookup"><span data-stu-id="3feff-262">Deploy this file</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="3feff-263">Auf dem Computer befindet sich ein Microsoft Windows-32-Bit-Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="3feff-263">Computer is running a 32-bit Microsoft Windows operating system</span></span></p></td>
    <td align="left"><p><span data-ttu-id="3feff-264">appv_client_MSI_x86.msi</span><span class="sxs-lookup"><span data-stu-id="3feff-264">appv_client_MSI_x86.msi</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="3feff-265">Auf dem Computer befindet sich ein Microsoft Windows-64-Bit-Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="3feff-265">Computer is running a 64-bit Microsoft Windows operating system</span></span></p></td>
    <td align="left"><p><span data-ttu-id="3feff-266">appv_client_MSI_x64.msi</span><span class="sxs-lookup"><span data-stu-id="3feff-266">appv_client_MSI_x64.msi</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="3feff-267">Sie stellen den App-V 5,1-Client für Remote Desktop Dienste bereit.</span><span class="sxs-lookup"><span data-stu-id="3feff-267">You are deploying the App-V 5.1 Remote Desktop Services client</span></span></p></td>
    <td align="left"><p><span data-ttu-id="3feff-268">appv_client_rds_MSI_x64.msi</span><span class="sxs-lookup"><span data-stu-id="3feff-268">appv_client_rds_MSI_x64.msi</span></span></p></td>
    </tr>
    </tbody>
    </table>



4.  <span data-ttu-id="3feff-269">Wählen Sie anhand der Informationen in der folgenden Tabelle auf der Grundlage der gewünschten Sprache für den Zielcomputer das entsprechende Sprachpaket **. msi** aus, das Sie installieren möchten.</span><span class="sxs-lookup"><span data-stu-id="3feff-269">Using the information in the following table, select the appropriate language pack **.msi** to install, based on the desired language for the target computer.</span></span> <span data-ttu-id="3feff-270">**Xxxx** in der Tabelle bezieht sich auf das Zielgebietsschema des Sprachpakets.</span><span class="sxs-lookup"><span data-stu-id="3feff-270">The **xxxx** in the table refers to the target locale of the language pack.</span></span>

    **<span data-ttu-id="3feff-271">Was Sie wissen sollten, bevor Sie beginnen:</span><span class="sxs-lookup"><span data-stu-id="3feff-271">What to know before you start:</span></span>**

    -   <span data-ttu-id="3feff-272">Die Sprachpakete sind sowohl für den standardmäßigen App-v 5,1-Client als auch für die Remote Desktop Dienste-Version des App-v 5,1-Clients üblich.</span><span class="sxs-lookup"><span data-stu-id="3feff-272">The language packs are common to both the standard App-V 5.1 client and the Remote Desktop Services version of the App-V 5.1 client.</span></span>

    -   <span data-ttu-id="3feff-273">Wenn Sie den App-V 5,1-Client mithilfe der **exe**-Datei installieren, wird vom Installationsprogramm nur das Sprachpaket bereitgestellt, das dem auf dem Zielcomputer ausgeführten Betriebssystem entspricht.</span><span class="sxs-lookup"><span data-stu-id="3feff-273">If you install the App-V 5.1 client using the **.exe**, the installer will deploy only the language pack that matches the operating system running on the target computer.</span></span>

    -   <span data-ttu-id="3feff-274">Zum Bereitstellen weiterer Sprachpakete auf einem Zielcomputer verwenden Sie das Verfahren **zum Installieren des App-V 5,1-Clients mithilfe der Windows Installer-Datei (MSI)**.</span><span class="sxs-lookup"><span data-stu-id="3feff-274">To deploy additional language packs on a target computer, use the procedure **To install the App-V 5.1 client by using Windows Installer (.msi) file**.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="3feff-275">Art der Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="3feff-275">Type of deployment</span></span></th>
    <th align="left"><span data-ttu-id="3feff-276">Diese Datei bereitstellen</span><span class="sxs-lookup"><span data-stu-id="3feff-276">Deploy this file</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="3feff-277">Auf dem Computer befindet sich ein Microsoft Windows-32-Bit-Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="3feff-277">Computer is running a 32-bit Microsoft Windows operating system</span></span></p></td>
    <td align="left"><p><span data-ttu-id="3feff-278">appv_client_LP_xxxx_ x86.msi</span><span class="sxs-lookup"><span data-stu-id="3feff-278">appv_client_LP_xxxx_ x86.msi</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="3feff-279">Auf dem Computer befindet sich ein Microsoft Windows-64-Bit-Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="3feff-279">Computer is running a 64-bit Microsoft Windows operating system</span></span></p></td>
    <td align="left"><p><span data-ttu-id="3feff-280">appv_client_LP_xxxx_ x64.msi</span><span class="sxs-lookup"><span data-stu-id="3feff-280">appv_client_LP_xxxx_ x64.msi</span></span></p></td>
    </tr>
    </tbody>
    </table>



~~~
**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## <span data-ttu-id="3feff-281">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="3feff-281">Related topics</span></span>


[<span data-ttu-id="3feff-282">Bereitstellen von App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="3feff-282">Deploying App-V 5.1</span></span>](deploying-app-v-51.md)

[<span data-ttu-id="3feff-283">Informationen über Clientkonfigurationseinstellungen</span><span class="sxs-lookup"><span data-stu-id="3feff-283">About Client Configuration Settings</span></span>](about-client-configuration-settings51.md)

[<span data-ttu-id="3feff-284">So deinstallieren Sie den App-V 5.1-Client</span><span class="sxs-lookup"><span data-stu-id="3feff-284">How to Uninstall the App-V 5.1 Client</span></span>](how-to-uninstall-the-app-v-51-client.md)









