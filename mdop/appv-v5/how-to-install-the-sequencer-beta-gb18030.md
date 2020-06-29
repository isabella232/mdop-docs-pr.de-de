---
title: So installieren Sie den Sequencer
description: So installieren Sie den Sequencer
author: dansimp
ms.assetid: a122caf0-f408-458c-b119-dc84123c1d58
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a8542abfecd7f1d543228ab1a86a59b9ee918947
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805363"
---
# <span data-ttu-id="64fbc-103">So installieren Sie den Sequencer</span><span class="sxs-lookup"><span data-stu-id="64fbc-103">How to Install the Sequencer</span></span>


<span data-ttu-id="64fbc-104">Gehen Sie wie folgt vor, um den Microsoft Application Virtualization (App-V) 5,0-Sequenzer zu installieren.</span><span class="sxs-lookup"><span data-stu-id="64fbc-104">Use the following procedure to install the Microsoft Application Virtualization (App-V) 5.0 sequencer.</span></span> <span data-ttu-id="64fbc-105">Auf dem Computer, auf dem der Sequencer ausgeführt wird, darf keine Version des App-V 5,0-Clients ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="64fbc-105">The computer that will run the sequencer must not be running any version of the App-V 5.0 client.</span></span>

<span data-ttu-id="64fbc-106">Das Upgrade einer vorherigen Installation des App-V-Sequencers wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="64fbc-106">Upgrading a previous installation of the App-V sequencer is not supported.</span></span>

<span data-ttu-id="64fbc-107">**Wichtig**  Eine vollständige Liste der Sequencer-Anforderungen finden Sie unter Sequencer [-Abschnitte der APP-v 5,0-Voraussetzungen](app-v-50-prerequisites.md) und [unterstützten Konfigurationen für App-v 5,0](app-v-50-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="64fbc-107">**Important** For a full list of the sequencer requirements see sequencer sections of [App-V 5.0 Prerequisites](app-v-50-prerequisites.md) and [App-V 5.0 Supported Configurations](app-v-50-supported-configurations.md).</span></span>

 

<span data-ttu-id="64fbc-108">Sie können auch die Befehlszeile verwenden, um den App-V 5,0-Sequenzer zu installieren.</span><span class="sxs-lookup"><span data-stu-id="64fbc-108">You can also use the command line to install the App-V 5.0 sequencer.</span></span> <span data-ttu-id="64fbc-109">In der folgenden Liste werden Informationen zu den Optionen für die Installation des Sequencers über die Befehlszeile und **appv\_sequencer\_setup.exe**angezeigt:</span><span class="sxs-lookup"><span data-stu-id="64fbc-109">The following list displays information about options for installing the sequencer using the command line and **appv\_sequencer\_setup.exe**:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="64fbc-110">Befehl</span><span class="sxs-lookup"><span data-stu-id="64fbc-110">Command</span></span></th>
<th align="left"><span data-ttu-id="64fbc-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="64fbc-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="64fbc-112">/INSTALLDIR</span><span class="sxs-lookup"><span data-stu-id="64fbc-112">/INSTALLDIR</span></span></p></td>
<td align="left"><p><span data-ttu-id="64fbc-113">Gibt das Installationsverzeichnis an.</span><span class="sxs-lookup"><span data-stu-id="64fbc-113">Specifies the installation directory.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="64fbc-114">/CEIPOPTIN</span><span class="sxs-lookup"><span data-stu-id="64fbc-114">/CEIPOPTIN</span></span></p></td>
<td align="left"><p><span data-ttu-id="64fbc-115">Ermöglicht die Teilnahme am Programm zur Verbesserung der Benutzerfreundlichkeit von Microsoft.</span><span class="sxs-lookup"><span data-stu-id="64fbc-115">Enables participation in the Microsoft Customer Experience Improvement Program.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="64fbc-116">/Log</span><span class="sxs-lookup"><span data-stu-id="64fbc-116">/Log</span></span></p></td>
<td align="left"><p><span data-ttu-id="64fbc-117">Gibt an, wo das Installationsprotokoll gespeichert werden soll, der Standardspeicherort ist <strong> % Temp% </strong> .</span><span class="sxs-lookup"><span data-stu-id="64fbc-117">Specifies where the installation log will be saved, the default location is <strong>%Temp%</strong>.</span></span> <span data-ttu-id="64fbc-118">Beispiel: " <strong> c" Logs \ Log. log </strong> .</span><span class="sxs-lookup"><span data-stu-id="64fbc-118">For example, <strong>C:\ Logs \ log.log</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="64fbc-119">/q</span><span class="sxs-lookup"><span data-stu-id="64fbc-119">/q</span></span></p></td>
<td align="left"><p><span data-ttu-id="64fbc-120">Gibt eine ruhige oder unbeaufsichtigte Installation an.</span><span class="sxs-lookup"><span data-stu-id="64fbc-120">Specifies a quiet or silent installation.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="64fbc-121">/Uninstall</span><span class="sxs-lookup"><span data-stu-id="64fbc-121">/Uninstall</span></span></p></td>
<td align="left"><p><span data-ttu-id="64fbc-122">Gibt das Entfernen des Sequencers an.</span><span class="sxs-lookup"><span data-stu-id="64fbc-122">Specifies the removal of the sequencer.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="64fbc-123">/ACCEPTEULA</span><span class="sxs-lookup"><span data-stu-id="64fbc-123">/ACCEPTEULA</span></span></p></td>
<td align="left"><p><span data-ttu-id="64fbc-124">Akzeptiert den Lizenzvertrag.</span><span class="sxs-lookup"><span data-stu-id="64fbc-124">Accepts the license agreement.</span></span> <span data-ttu-id="64fbc-125">Dies ist für eine unbeaufsichtigte Installation erforderlich.</span><span class="sxs-lookup"><span data-stu-id="64fbc-125">This is required for an unattended installation.</span></span> <span data-ttu-id="64fbc-126">Beispiel Verwendung: <strong> /ACCEPTEULA </strong> oder <strong> /ACCEPTEULA = 1 </strong> .</span><span class="sxs-lookup"><span data-stu-id="64fbc-126">Example usage: <strong>/ACCEPTEULA</strong> or <strong>/ACCEPTEULA=1</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="64fbc-127">/LAYOUT</span><span class="sxs-lookup"><span data-stu-id="64fbc-127">/LAYOUT</span></span></p></td>
<td align="left"><p><span data-ttu-id="64fbc-128">Gibt die zugeordnete Layout-Aktion an.</span><span class="sxs-lookup"><span data-stu-id="64fbc-128">Specifies the associated layout action.</span></span> <span data-ttu-id="64fbc-129">Außerdem werden die Windows Installer-Dateien (MSI) und Skriptdateien in einen Ordner extrahiert, ohne App-V 5,0 zu installieren.</span><span class="sxs-lookup"><span data-stu-id="64fbc-129">It also extracts the Windows Installer (.msi) and script files to a folder without installing App-V 5.0.</span></span> <span data-ttu-id="64fbc-130">Es wird kein Wert erwartet.</span><span class="sxs-lookup"><span data-stu-id="64fbc-130">No value is expected.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="64fbc-131">/LAYOUTDIR</span><span class="sxs-lookup"><span data-stu-id="64fbc-131">/LAYOUTDIR</span></span></p></td>
<td align="left"><p><span data-ttu-id="64fbc-132">Gibt das layoutverzeichnis an.</span><span class="sxs-lookup"><span data-stu-id="64fbc-132">Specifies the layout directory.</span></span> <span data-ttu-id="64fbc-133">Erfordert einen Zeichenfolgenwert.</span><span class="sxs-lookup"><span data-stu-id="64fbc-133">Requires a string value.</span></span> <span data-ttu-id="64fbc-134">Beispielsyntax: <strong> /LAYOUTDIR = "C:\Application Virtualization Client" </strong> .</span><span class="sxs-lookup"><span data-stu-id="64fbc-134">Example usage: <strong>/LAYOUTDIR=”C:\Application Virtualization Client”</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="64fbc-135">/?</span><span class="sxs-lookup"><span data-stu-id="64fbc-135">/?</span></span> <span data-ttu-id="64fbc-136">Oder/h oder/Help</span><span class="sxs-lookup"><span data-stu-id="64fbc-136">Or /h or /help</span></span></p></td>
<td align="left"><p><span data-ttu-id="64fbc-137">Zeigt die zugehörige Hilfe an.</span><span class="sxs-lookup"><span data-stu-id="64fbc-137">Displays associated help.</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="64fbc-138">So installieren Sie den App-V 5,0-Sequenzer</span><span class="sxs-lookup"><span data-stu-id="64fbc-138">To install the App-V 5.0 sequencer</span></span>**

1.  <span data-ttu-id="64fbc-139">Kopieren Sie die Installationsdateien der App-V 5,0 Sequencer auf den Computer, auf dem Sie installiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="64fbc-139">Copy the App-V 5.0 sequencer installation files to the computer on which it will be installed.</span></span> <span data-ttu-id="64fbc-140">Doppelklicken Sie auf **appv\_sequencer\_setup.exe** , und klicken Sie dann auf **Installieren**.</span><span class="sxs-lookup"><span data-stu-id="64fbc-140">Double-click **appv\_sequencer\_setup.exe** and then click **Install**.</span></span>

2.  <span data-ttu-id="64fbc-141">Auf der Seite **Software-Lizenzbestimmungen** sollten Sie die Lizenzbestimmungen überprüfen.</span><span class="sxs-lookup"><span data-stu-id="64fbc-141">On the **Software License Terms** page, you should review the license terms.</span></span> <span data-ttu-id="64fbc-142">Wenn Sie die Lizenzbestimmungen akzeptieren möchten, wählen Sie **Ich akzeptiere die Lizenzbestimmungen.**</span><span class="sxs-lookup"><span data-stu-id="64fbc-142">To accept the license terms select **I accept the license terms.**</span></span> <span data-ttu-id="64fbc-143">Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="64fbc-143">Click **Next**.</span></span>

3.  <span data-ttu-id="64fbc-144">Verwenden Sie **Microsoft Update, um die sichere und aktuelle Seite Ihres Computers zu Gewähr** leisten, um Microsoft Updates zu aktivieren, wählen Sie **Microsoft Update verwenden aus, wenn ich auf Updates Suche (empfohlen).**</span><span class="sxs-lookup"><span data-stu-id="64fbc-144">On the **Use Microsoft Update to help keep your computer secure and up-to-date** page, to enable Microsoft updates select **Use Microsoft Update when I check for updates (recommended).**</span></span> <span data-ttu-id="64fbc-145">Wenn Sie Microsoft Updates deaktivieren möchten, wählen Sie **Ich möchte Microsoft Update nicht verwenden**aus.</span><span class="sxs-lookup"><span data-stu-id="64fbc-145">To disable Microsoft updates from running select **I don’t want to use Microsoft Update**.</span></span> <span data-ttu-id="64fbc-146">Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="64fbc-146">Click **Next**.</span></span>

4.  <span data-ttu-id="64fbc-147">Wählen Sie auf der Seite **Programm zur Verbesserung der Benutzerfreundlichkeit** an dem Programm teilnehmen an dem Programm zur **Verbesserung der Benutzerfreundlichkeit**teilnehmen aus.</span><span class="sxs-lookup"><span data-stu-id="64fbc-147">On the **Customer Experience Improvement Program** page, to participate in the program select **Join the Customer Experience Improvement Program**.</span></span> <span data-ttu-id="64fbc-148">Auf diese Weise können Informationen darüber gesammelt werden, wie Sie App-V 5,0 verwenden.</span><span class="sxs-lookup"><span data-stu-id="64fbc-148">This will allow information to be collected about how you are using App-V 5.0.</span></span> <span data-ttu-id="64fbc-149">Wenn Sie nicht an dem Programm teilnehmen möchten, wählen Sie **Ich möchte zurzeit nicht an dem Programm**teilnehmen.</span><span class="sxs-lookup"><span data-stu-id="64fbc-149">If you don’t want to participate in the program select **I don’t want to join the program at this time**.</span></span> <span data-ttu-id="64fbc-150">Klicken Sie auf **Installieren**.</span><span class="sxs-lookup"><span data-stu-id="64fbc-150">Click **Install**.</span></span>

5.  <span data-ttu-id="64fbc-151">Klicken Sie zum Öffnen des Sequencers auf **Start** , und klicken Sie dann auf **Microsoft Application Virtualization Sequencer**.</span><span class="sxs-lookup"><span data-stu-id="64fbc-151">To open the sequencer, click **Start** and then click **Microsoft Application Virtualization Sequencer**.</span></span>

**<span data-ttu-id="64fbc-152">So beheben Sie die Problembehandlung bei der Installation von App-V 5,0 Sequencer</span><span class="sxs-lookup"><span data-stu-id="64fbc-152">To troubleshoot the App-V 5.0 sequencer installation</span></span>**

-   <span data-ttu-id="64fbc-153">Wenn Sie weitere Informationen zur Sequencer-Installation wünschen, können Sie das Fehlerprotokoll im Ordner **% Temp%** anzeigen.</span><span class="sxs-lookup"><span data-stu-id="64fbc-153">For more information regarding the sequencer installation, you can view the error log in the **%temp%** folder.</span></span> <span data-ttu-id="64fbc-154">Wenn Sie die Protokolldateien überprüfen möchten, klicken Sie auf **Start**, geben Sie **% Temp%** ein, und suchen Sie dann nach dem **appv\_-Protokoll**.</span><span class="sxs-lookup"><span data-stu-id="64fbc-154">To review the log files, click **Start**, type **%temp%**, and then look for the **appv\_ log**.</span></span>

    <span data-ttu-id="64fbc-155">Sie **haben einen Vorschlag für App-V**?</span><span class="sxs-lookup"><span data-stu-id="64fbc-155">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="64fbc-156">[Hier](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)können Sie Vorschläge hinzufügen oder abstimmen.</span><span class="sxs-lookup"><span data-stu-id="64fbc-156">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="64fbc-157">Sie haben ein App-V-Problem?</span><span class="sxs-lookup"><span data-stu-id="64fbc-157">Got an App-V issue?</span></span>** <span data-ttu-id="64fbc-158">Verwenden Sie das [App-V TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="64fbc-158">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="64fbc-159">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="64fbc-159">Related topics</span></span>


[<span data-ttu-id="64fbc-160">Planen der Bereitstellung von App-V</span><span class="sxs-lookup"><span data-stu-id="64fbc-160">Planning to Deploy App-V</span></span>](planning-to-deploy-app-v.md)

 

 





