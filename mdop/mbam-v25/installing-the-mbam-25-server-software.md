---
title: Installieren der MBAM 2.5-Serversoftware
description: Installieren der MBAM 2.5-Serversoftware
author: dansimp
ms.assetid: b9dbe697-5400-4bac-acfb-ee6dc6586c30
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6612bf52aa53ae693694d7ac02c5cab212d4e24f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809928"
---
# <span data-ttu-id="5bde8-103">Installieren der MBAM 2.5-Serversoftware</span><span class="sxs-lookup"><span data-stu-id="5bde8-103">Installing the MBAM 2.5 Server Software</span></span>


<span data-ttu-id="5bde8-104">In diesem Thema wird beschrieben, wie Sie die Microsoft BitLocker-Verwaltungs-und Überwachungssoftware (MBAM) 2,5-Server Software mithilfe des Setup-Assistenten für die Microsoft BitLocker-Verwaltung und-Überwachung oder mithilfe von Befehlszeilenparametern installieren.</span><span class="sxs-lookup"><span data-stu-id="5bde8-104">This topic describes how to install the Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 Server software by using the Microsoft BitLocker Administration and Monitoring Setup wizard or by using command-line parameters.</span></span> <span data-ttu-id="5bde8-105">Wiederholen Sie den Server Installationsvorgang für jeden Server, auf dem Sie die MBAM 2,5-Server Features konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="5bde8-105">Repeat the server installation process for each server on which you are configuring MBAM 2.5 Server features.</span></span> <span data-ttu-id="5bde8-106">Nachdem Sie die Installation abgeschlossen haben, lesen Sie [Konfigurieren der MBAM 2,5-Server Features](configuring-the-mbam-25-server-features.md) , um Schritte zum Konfigurieren der Server Features zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="5bde8-106">After you finish the installation, see [Configuring the MBAM 2.5 Server Features](configuring-the-mbam-25-server-features.md) for steps about configuring the Server features.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="5bde8-107">Vorbereitung</span><span class="sxs-lookup"><span data-stu-id="5bde8-107">Before you start</span></span></th>
<th align="left"><span data-ttu-id="5bde8-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5bde8-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5bde8-109">Überprüfen der MBAM 2,5-Planungsinformationen</span><span class="sxs-lookup"><span data-stu-id="5bde8-109">Review the MBAM 2.5 planning information</span></span></p></td>
<td align="left"><ul>
<li><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)"><span data-ttu-id="5bde8-110">MBAM 2.5-Servervoraussetzungen für eigenständige und Configuration Manager-Integrationstopologien</span><span class="sxs-lookup"><span data-stu-id="5bde8-110">MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies</span></span></a></p></li>
<li><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)"><span data-ttu-id="5bde8-111">Von MBAM 2.5 unterstützte Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="5bde8-111">MBAM 2.5 Supported Configurations</span></span></a></p></li>
<li><p><a href="high-level-architecture-for-mbam-25.md" data-raw-source="[High-Level Architecture for MBAM 2.5](high-level-architecture-for-mbam-25.md)"><span data-ttu-id="5bde8-112">High-Level-Architektur für MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="5bde8-112">High-Level Architecture for MBAM 2.5</span></span></a></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5bde8-113">Lesen Sie, wie Protokolldateien abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="5bde8-113">Read how to get log files</span></span></p></td>
<td align="left"><p><span data-ttu-id="5bde8-114">Standardmäßig werden Protokolldateien im Ordner% Temp% des lokalen Computers erstellt.</span><span class="sxs-lookup"><span data-stu-id="5bde8-114">By default, log files are created in the local computer’s %temp% folder.</span></span> <span data-ttu-id="5bde8-115">Wenn Sie die Protokolldateien an einen bestimmten Speicherort anstatt in den <strong> Ordner% Temp </strong> % schreiben möchten, verwenden Sie das <strong> /log- </strong> &lt; <em> Standort </em> &gt; Argument.</span><span class="sxs-lookup"><span data-stu-id="5bde8-115">To write the log files to a specific location rather than to the <strong>%temp</strong>% folder, use the <strong>/log</strong> &lt;<em>location</em>&gt; argument.</span></span></p>
<p><span data-ttu-id="5bde8-116">Zusätzliche Ereignisse werden möglicherweise in der Ereignisanzeige in den <strong> MBAM-Setup- </strong> oder <strong> MBAM-Web- </strong> Knoten unter <strong> Anwendungen und Dienste protokolliert &gt; Microsoft &gt; Windows protokolliert </strong> .</span><span class="sxs-lookup"><span data-stu-id="5bde8-116">Additional events might be logged in Event Viewer in the <strong>MBAM-Setup</strong> or <strong>MBAM-Web</strong> nodes under <strong>Applications and Services Logs &gt; Microsoft &gt; Windows</strong>.</span></span> <span data-ttu-id="5bde8-117">Wenn Sie beispielsweise MBAM deinstallieren, wird das Deinstallationsprogramm auch die MBAM-und MBAM-Web-Protokolle in Event Viewer deinstallieren.</span><span class="sxs-lookup"><span data-stu-id="5bde8-117">For example, if you uninstall MBAM, the uninstaller will also uninstall the MBAM-Setup and MBAM-Web logs in EventViewer.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="5bde8-118">Installieren der MBAM 2,5-Server Software mithilfe des Setup-Assistenten für die Microsoft BitLocker-Verwaltung und-Überwachung</span><span class="sxs-lookup"><span data-stu-id="5bde8-118">Installing the MBAM 2.5 Server software by using the Microsoft BitLocker Administration and Monitoring Setup wizard</span></span>


<span data-ttu-id="5bde8-119">Führen Sie die folgenden Schritte aus, um die MBAM-Server Software mithilfe des Setup-Assistenten für die Microsoft BitLocker-Verwaltung und-Überwachung zu installieren.</span><span class="sxs-lookup"><span data-stu-id="5bde8-119">Use these steps to install the MBAM Server software by using the Microsoft BitLocker Administration and Monitoring Setup wizard.</span></span>

**<span data-ttu-id="5bde8-120">So installieren Sie die MBAM 2,5-Server Software mithilfe des Assistenten</span><span class="sxs-lookup"><span data-stu-id="5bde8-120">To install the MBAM 2.5 Server software by using the wizard</span></span>**

1.  <span data-ttu-id="5bde8-121">Führen Sie auf dem Server, auf dem Sie MBAM installieren möchten, **MBAMserversetup.exe** aus, um den Setup-Assistenten für Microsoft BitLocker-Verwaltung und-Überwachung zu starten.</span><span class="sxs-lookup"><span data-stu-id="5bde8-121">On the server where you want to install MBAM, run **MBAMserversetup.exe** to start the Microsoft BitLocker Administration and Monitoring Setup wizard.</span></span>

2.  <span data-ttu-id="5bde8-122">Klicken Sie auf der Seite **Willkommen** auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="5bde8-122">On the **Welcome** page, click **Next**.</span></span>

3.  <span data-ttu-id="5bde8-123">Lesen und akzeptieren Sie den Microsoft-Software-Lizenzvertrag, und klicken Sie auf **weiter** , um die Installation fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="5bde8-123">Read and accept the Microsoft Software License Agreement, and then click **Next** to continue the installation.</span></span>

4.  <span data-ttu-id="5bde8-124">Wählen Sie aus, ob Sie Microsoft Update verwenden möchten, wenn Sie nach Updates suchen, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="5bde8-124">Choose whether to use Microsoft Update when you check for updates, and then click **Next**.</span></span>

5.  <span data-ttu-id="5bde8-125">Wählen Sie aus, ob Sie am Programm zur Verbesserung der Benutzerfreundlichkeit teilnehmen möchten, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="5bde8-125">Choose whether to participate in the Customer Experience Improvement Program, and then click **Next**.</span></span>

6.  <span data-ttu-id="5bde8-126">Klicken Sie auf **Installieren**, um die Installation zu starten.</span><span class="sxs-lookup"><span data-stu-id="5bde8-126">To start the installation, click **Install**.</span></span>

7.  <span data-ttu-id="5bde8-127">Wenn Sie die Server Features nach Abschluss der Installation der MBAM-Server Software konfigurieren möchten, aktivieren Sie das Kontrollkästchen **MBAM-Serverkonfiguration ausführen, nachdem der Assistent geschlossen** wurde.</span><span class="sxs-lookup"><span data-stu-id="5bde8-127">To configure the server features after the MBAM Server software finishes installing, select the **Run MBAM Server Configuration after the wizard closes** check box.</span></span> <span data-ttu-id="5bde8-128">Alternativ können Sie MBAM später mithilfe der **MBAM-Server Konfigurations** Verknüpfung konfigurieren, die von der Server Installation im **Startmenü** erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="5bde8-128">Alternatively, you can configure MBAM later by using the **MBAM Server Configuration** shortcut that the server installation creates on your **Start** menu.</span></span>

8.  <span data-ttu-id="5bde8-129">Klicken Sie auf **Fertig stellen**.</span><span class="sxs-lookup"><span data-stu-id="5bde8-129">Click **Finish**.</span></span>

## <span data-ttu-id="5bde8-130">Installieren der MBAM 2,5-Server Software über ein Eingabeaufforderungsfenster</span><span class="sxs-lookup"><span data-stu-id="5bde8-130">Installing the MBAM 2.5 Server software by using a Command Prompt window</span></span>


<span data-ttu-id="5bde8-131">Geben Sie an der Eingabeaufforderung einen Befehl ähnlich dem folgenden Befehl ein, um die MBAM-Server Software zu installieren.</span><span class="sxs-lookup"><span data-stu-id="5bde8-131">At a command prompt, type a command similar to the following command to install the MBAM Server software.</span></span>

``` syntax
MbamServerSetup.exe MBAMServerInstall.log
CEIPENABLED=True OPTIN_FOR_MICROFOST_UPDATES=True INSTALLDIR=c:\mbaminstall
```

<span data-ttu-id="5bde8-132">In der folgenden Tabelle werden die Befehlszeilenparameter für die Installation der MBAM 2,5-Server Software beschrieben.</span><span class="sxs-lookup"><span data-stu-id="5bde8-132">The following table describes the command-line parameters for installing the MBAM 2.5 Server software.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="5bde8-133">Parameter</span><span class="sxs-lookup"><span data-stu-id="5bde8-133">Parameter</span></span></th>
<th align="left"><span data-ttu-id="5bde8-134">Parameter Wert</span><span class="sxs-lookup"><span data-stu-id="5bde8-134">Parameter value</span></span></th>
<th align="left"><span data-ttu-id="5bde8-135">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5bde8-135">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5bde8-136">CEIPENABLED</span><span class="sxs-lookup"><span data-stu-id="5bde8-136">CEIPENABLED</span></span></p></td>
<td align="left"><p><span data-ttu-id="5bde8-137">Wahr falsch</span><span class="sxs-lookup"><span data-stu-id="5bde8-137">True False</span></span></p></td>
<td align="left"><p><span data-ttu-id="5bde8-138">True – nehmen Sie am Programm zur Verbesserung der Benutzerfreundlichkeit Teil, das Microsoft dabei hilft, zu ermitteln, welche MBAM-Features verbessert werden können.</span><span class="sxs-lookup"><span data-stu-id="5bde8-138">True - participate in the Customer Improvement Experience Program, which helps Microsoft identify which MBAM features to improve.</span></span></p>
<p><span data-ttu-id="5bde8-139">Falsch – nehmen Sie nicht am Programm zur Verbesserung der Benutzerfreundlichkeit teil.</span><span class="sxs-lookup"><span data-stu-id="5bde8-139">False – do not participate in the Customer Improvement Experience Program.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5bde8-140">OPTIN_FOR_MICROSOFT_UPDATES</span><span class="sxs-lookup"><span data-stu-id="5bde8-140">OPTIN_FOR_MICROSOFT_UPDATES</span></span></p></td>
<td align="left"><p><span data-ttu-id="5bde8-141">Wahr falsch</span><span class="sxs-lookup"><span data-stu-id="5bde8-141">True False</span></span></p></td>
<td align="left"><p><span data-ttu-id="5bde8-142">True – verwenden Sie Microsoft Update, um Ihren Computer für Windows und andere Microsoft-Produkte, einschließlich MBAM, zu schützen und auf dem neuesten Stand zu halten.</span><span class="sxs-lookup"><span data-stu-id="5bde8-142">True - use Microsoft Update to keep your computer secure and up-to-date for Windows and other Microsoft products, including MBAM.</span></span></p>
<p><span data-ttu-id="5bde8-143">Falsch – Microsoft Update nicht verwenden</span><span class="sxs-lookup"><span data-stu-id="5bde8-143">False – do not use Microsoft Update</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5bde8-144">INSTALLDIR</span><span class="sxs-lookup"><span data-stu-id="5bde8-144">INSTALLDIR</span></span></p></td>
<td align="left"><p><span data-ttu-id="5bde8-145">&lt;Pfad&gt;</span><span class="sxs-lookup"><span data-stu-id="5bde8-145">&lt;Path&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="5bde8-146">Der Speicherort, an dem Sie MBAM installieren möchten.</span><span class="sxs-lookup"><span data-stu-id="5bde8-146">Location where you want to install MBAM.</span></span></p>
<p><span data-ttu-id="5bde8-147">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="5bde8-147">Example:</span></span></p>
<p><span data-ttu-id="5bde8-148">INSTALLDIR = c:\mbaminstall</span><span class="sxs-lookup"><span data-stu-id="5bde8-148">INSTALLDIR=c:\mbaminstall</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5bde8-149">FORCE_UNINSTALL</span><span class="sxs-lookup"><span data-stu-id="5bde8-149">FORCE_UNINSTALL</span></span></p></td>
<td align="left"><p><span data-ttu-id="5bde8-150">Wahr falsch</span><span class="sxs-lookup"><span data-stu-id="5bde8-150">True False</span></span></p></td>
<td align="left"><p><span data-ttu-id="5bde8-151">True: setzen Sie den Vorgang der Deinstallation von MBAM fort, auch wenn Features nicht entfernt werden können.</span><span class="sxs-lookup"><span data-stu-id="5bde8-151">True - continue the process of uninstalling MBAM, even if any features fail to be removed.</span></span></p>
<p><span data-ttu-id="5bde8-152">False (Standard), wenn die benutzerdefinierte Aktion "Deinstallation" ein hinzugefügtes MBAM-Server Feature nicht entfernen kann, die Deinstallation fehlschlägt und MBAM weiterhin installiert ist.</span><span class="sxs-lookup"><span data-stu-id="5bde8-152">False (default) if the uninstallation custom action fails to remove an added MBAM Server feature, the uninstallation fails, and MBAM remains installed.</span></span></p>
<p><span data-ttu-id="5bde8-153">In beiden Fällen bleiben alle Features, die während des Versuchs zur Deinstallation von MBAM erfolgreich entfernt wurden, entfernt.</span><span class="sxs-lookup"><span data-stu-id="5bde8-153">In both instances, any features that were successfully removed during the attempt to uninstall MBAM stay removed.</span></span></p></td>
</tr>
</tbody>
</table>

 



## <span data-ttu-id="5bde8-154">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="5bde8-154">Related topics</span></span>


[<span data-ttu-id="5bde8-155">Bereitstellen von MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="5bde8-155">Deploying MBAM 2.5</span></span>](deploying-mbam-25.md)

[<span data-ttu-id="5bde8-156">Konfigurieren der MBAM 2.5-Serverfunktionen</span><span class="sxs-lookup"><span data-stu-id="5bde8-156">Configuring the MBAM 2.5 Server Features</span></span>](configuring-the-mbam-25-server-features.md)

 

## <span data-ttu-id="5bde8-157">Sie haben einen Vorschlag für MBAM?</span><span class="sxs-lookup"><span data-stu-id="5bde8-157">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="5bde8-158">[Hier](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)können Sie Vorschläge hinzufügen oder abstimmen.</span><span class="sxs-lookup"><span data-stu-id="5bde8-158">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="5bde8-159">Bei MBAM-Problemen verwenden Sie das [MBAM TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="5bde8-159">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





