---
title: Erstellen und Verwalten virtualisierter App-V 5.0-Anwendungen
description: Erstellen und Verwalten virtualisierter App-V 5.0-Anwendungen
author: dansimp
ms.assetid: 66bab403-d7e0-4e7b-bc8f-a29a98a7160a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 86332c7753b70abbaaf289fc1ba046bf59d1dd89
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805924"
---
# <span data-ttu-id="5a4eb-103">Erstellen und Verwalten virtualisierter App-V 5.0-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="5a4eb-103">Creating and Managing App-V 5.0 Virtualized Applications</span></span>


<span data-ttu-id="5a4eb-104">Nachdem Sie den Microsoft Application Virtualization (App-V) 5,0-Sequenzer ordnungsgemäß bereitgestellt haben, können Sie ihn zum Überwachen und Aufzeichnen des Installations-und Setupprozesses verwenden, damit eine Anwendung als virtualisierte Anwendung ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="5a4eb-104">After you have properly deployed the Microsoft Application Virtualization (App-V) 5.0 sequencer, you can use it to monitor and record the installation and setup process for an application to be run as a virtualized application.</span></span>

<span data-ttu-id="5a4eb-105">**Hinweis**  Weitere Informationen zum Konfigurieren von Microsoft Application Virtualization (App-V) 5,0-Sequenzer, zum Sequenzieren bewährter Methoden und ein Beispiel für das Erstellen und Aktualisieren einer virtuellen Anwendung finden Sie im [Microsoft Application Virtualization 5,0-Sequenzierungs Handbuch](https://download.microsoft.com/download/F/7/8/F784A197-73BE-48FF-83DA-4102C05A6D44/App-V 5.0 Sequencing Guide.docx) ( https://download.microsoft.com/download/F/7/8/F784A197-73BE-48FF-83DA-4102C05A6D44/App-V 5,0-Sequenzierungs Guide.docx).</span><span class="sxs-lookup"><span data-stu-id="5a4eb-105">**Note** For more information about configuring the Microsoft Application Virtualization (App-V) 5.0 sequencer, sequencing best practices, and an example of creating and updating a virtual application, see the [Microsoft Application Virtualization 5.0 Sequencing Guide](https://download.microsoft.com/download/F/7/8/F784A197-73BE-48FF-83DA-4102C05A6D44/App-V 5.0 Sequencing Guide.docx) (https://download.microsoft.com/download/F/7/8/F784A197-73BE-48FF-83DA-4102C05A6D44/App-V 5.0 Sequencing Guide.docx).</span></span>

 

## <span data-ttu-id="5a4eb-106">Sequenzieren einer Anwendung</span><span class="sxs-lookup"><span data-stu-id="5a4eb-106">Sequencing an application</span></span>


<span data-ttu-id="5a4eb-107">Mit dem App-V 5,0-Sequenzer können Sie die folgenden Aufgaben ausführen:</span><span class="sxs-lookup"><span data-stu-id="5a4eb-107">You can use the App-V 5.0 Sequencer to perform the following tasks:</span></span>

-   <span data-ttu-id="5a4eb-108">Erstellen Sie virtuelle Pakete, die auf Computern mit dem App-V 5,0-Client bereitgestellt werden können.</span><span class="sxs-lookup"><span data-stu-id="5a4eb-108">Create virtual packages that can be deployed to computers running the App-V 5.0 client.</span></span>

-   <span data-ttu-id="5a4eb-109">Aktualisieren vorhandener Pakete</span><span class="sxs-lookup"><span data-stu-id="5a4eb-109">Upgrade existing packages.</span></span> <span data-ttu-id="5a4eb-110">Sie können ein vorhandenes Paket auf dem Computer erweitern, auf dem der Sequencer ausgeführt wird, und dann die Anwendung aktualisieren, um eine neuere Version zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="5a4eb-110">You can expand an existing package onto the computer running the sequencer and then upgrade the application to create a newer version.</span></span>

-   <span data-ttu-id="5a4eb-111">Bearbeiten von Konfigurationsinformationen, die einem vorhandenen Paket zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="5a4eb-111">Edit configuration information associated with an existing package.</span></span> <span data-ttu-id="5a4eb-112">So können Sie beispielsweise eine Verknüpfung hinzufügen oder eine Dateitypzuordnung ändern.</span><span class="sxs-lookup"><span data-stu-id="5a4eb-112">For example, you can add a shortcut or modify a file type association.</span></span>

    <span data-ttu-id="5a4eb-113">**Hinweis**  Sie müssen Verknüpfungen erstellen und diese an einem verfügbaren Netzwerkspeicherort speichern, um Roaming zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="5a4eb-113">**Note** You must create shortcuts and save them to an available network location to allow roaming.</span></span> <span data-ttu-id="5a4eb-114">Wenn eine Verknüpfung erstellt und an einem privaten Speicherort gespeichert wird, muss das Paket lokal auf dem Computer veröffentlicht werden, auf dem der App-V 5,0-Client ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5a4eb-114">If a shortcut is created and saved in a private location, the package must be published locally to the computer running the App-V 5.0 client.</span></span>

     

-   <span data-ttu-id="5a4eb-115">Umwandeln vorhandener virtueller Pakete</span><span class="sxs-lookup"><span data-stu-id="5a4eb-115">Convert existing virtual packages.</span></span>

<span data-ttu-id="5a4eb-116">Der Sequencer verwendet das% **tmp% \ \ Scratch** oder **% Temp% \ \ Scratch** -Verzeichnis und das **Temp** -Verzeichnis, um temporäre Dateien während der Sequenzierung zu speichern.</span><span class="sxs-lookup"><span data-stu-id="5a4eb-116">The sequencer uses the **%TMP% \\ Scratch** or **%TEMP% \\ Scratch** directory and the **Temp** directory to store temporary files during sequencing.</span></span> <span data-ttu-id="5a4eb-117">Auf dem Computer, auf dem der Sequencer ausgeführt wird, sollten Sie diese Verzeichnisse mit freiem Speicherplatz konfigurieren, der den geschätzten Anwendungs Installationsanforderungen entspricht.</span><span class="sxs-lookup"><span data-stu-id="5a4eb-117">On the computer that runs the sequencer, you should configure these directories with free disk space equivalent to the estimated application installation requirements.</span></span> <span data-ttu-id="5a4eb-118">Das Konfigurieren der temporären Verzeichnisse und des temporären Verzeichnisses auf unterschiedlichen Festplattenpartitionen kann zur Verbesserung der Leistung während der Sequenzierung beitragen.</span><span class="sxs-lookup"><span data-stu-id="5a4eb-118">Configuring the temp directories and the Temp directory on different hard drive partitions can help improve performance during sequencing.</span></span>

<span data-ttu-id="5a4eb-119">Wenn Sie den Sequencer zum Erstellen einer neuen virtuellen Anwendung verwenden, werden die folgenden aufgelisteten Dateien erstellt.</span><span class="sxs-lookup"><span data-stu-id="5a4eb-119">When you use the sequencer to create a new virtual application, the following listed files are created.</span></span> <span data-ttu-id="5a4eb-120">Diese Dateien umfassen das App-V 5,0-Paket.</span><span class="sxs-lookup"><span data-stu-id="5a4eb-120">These files comprise the App-V 5.0 package.</span></span>

-   <span data-ttu-id="5a4eb-121">MSI-Datei.</span><span class="sxs-lookup"><span data-stu-id="5a4eb-121">.msi file.</span></span> <span data-ttu-id="5a4eb-122">Diese Windows Installer-Datei (MSI) wird vom Sequencer erstellt und zum Installieren des virtuellen Pakets auf Zielcomputern verwendet.</span><span class="sxs-lookup"><span data-stu-id="5a4eb-122">This Windows Installer (.msi) file is created by the sequencer and is used to install the virtual package on target computers.</span></span>

-   <span data-ttu-id="5a4eb-123">Report.xml-Datei.</span><span class="sxs-lookup"><span data-stu-id="5a4eb-123">Report.xml file.</span></span> <span data-ttu-id="5a4eb-124">In dieser Datei speichert der Sequencer alle Probleme, Warnungen und Fehler, die während der Sequenzierung ermittelt wurden.</span><span class="sxs-lookup"><span data-stu-id="5a4eb-124">In this file, the sequencer saves all issues, warnings, and errors that were discovered during sequencing.</span></span> <span data-ttu-id="5a4eb-125">Nachdem das Paket erstellt wurde, werden die Informationen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5a4eb-125">It displays the information after the package has been created.</span></span> <span data-ttu-id="5a4eb-126">Diesen Bericht können Sie uns zur Diagnose und zur Problembehebung entnehmen.</span><span class="sxs-lookup"><span data-stu-id="5a4eb-126">You can us this report for diagnosing and troubleshooting.</span></span>

-   <span data-ttu-id="5a4eb-127">AppV-Datei.</span><span class="sxs-lookup"><span data-stu-id="5a4eb-127">.appv file.</span></span> <span data-ttu-id="5a4eb-128">Dies ist die virtuelle Anwendungsdatei.</span><span class="sxs-lookup"><span data-stu-id="5a4eb-128">This is the virtual application file.</span></span>

-   <span data-ttu-id="5a4eb-129">Konfigurationsdatei für die Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="5a4eb-129">Deployment configuration file.</span></span> <span data-ttu-id="5a4eb-130">Die Konfigurationsdatei für die Bereitstellung bestimmt, wie die virtuelle Anwendung auf den Zielcomputern bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="5a4eb-130">The deployment configuration file determines how the virtual application will be deployed to target computers.</span></span>

-   <span data-ttu-id="5a4eb-131">Konfigurationsdatei für Benutzer.</span><span class="sxs-lookup"><span data-stu-id="5a4eb-131">User configuration file.</span></span> <span data-ttu-id="5a4eb-132">Die Benutzerkonfigurationsdatei legt fest, wie die virtuelle Anwendung auf Zielcomputern ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="5a4eb-132">The user configuration file determines how the virtual application will run on target computers.</span></span>

<span data-ttu-id="5a4eb-133">**Wichtig**  Sie müssen die Ordner% tmp% und% Temp% konfigurieren, die vom Paket Konverter als sicherer Speicherort und Verzeichnis verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5a4eb-133">**Important** You must configure the %TMP% and %TEMP% folders that the package converter uses to be a secure location and directory.</span></span> <span data-ttu-id="5a4eb-134">Ein sicherer Standort kann nur von einem Administrator abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="5a4eb-134">A secure location is only accessible by an administrator.</span></span> <span data-ttu-id="5a4eb-135">Wenn Sie das Paket sequenzieren, sollten Sie darüber hinaus das Paket an einem sicheren Speicherort speichern, oder Sie müssen sicherstellen, dass kein anderer Benutzer während des Konvertierungs-und Überwachungsprozesses angemeldet werden darf.</span><span class="sxs-lookup"><span data-stu-id="5a4eb-135">Additionally, when you sequence the package you should save the package to a location that is secure, or make sure that no other user is allowed to be logged in during the conversion and monitoring process.</span></span>

 

<span data-ttu-id="5a4eb-136">Das Dialogfeld " **Optionen** " in der Sequencer-Konsole enthält die folgenden Registerkarten:</span><span class="sxs-lookup"><span data-stu-id="5a4eb-136">The **Options** dialog box in the sequencer console contains the following tabs:</span></span>

-   <span data-ttu-id="5a4eb-137">**Allgemein**.</span><span class="sxs-lookup"><span data-stu-id="5a4eb-137">**General**.</span></span> <span data-ttu-id="5a4eb-138">Verwenden Sie diese Registerkarte, um die Ausführung von Microsoft-Updates während der Sequenzierung zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="5a4eb-138">Use this tab to enable Microsoft Updates to run during sequencing.</span></span> <span data-ttu-id="5a4eb-139">Wählen Sie **Paket Version an filename anfügen** aus, um die Sequenz so zu konfigurieren, dass dem virtualisierten Paket, das sequenziert wird, eine Versionsnummer hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="5a4eb-139">Select **Append Package Version to Filename** to configure the sequence to add a version number to the virtualized package that is being sequenced.</span></span> <span data-ttu-id="5a4eb-140">Wählen Sie **der Quelle von Paket Beschleunigern immer vertrauen** aus, um virtualisierte Pakete mithilfe eines Paket Beschleunigers zu erstellen, ohne zur Autorisierung aufgefordert zu werden.</span><span class="sxs-lookup"><span data-stu-id="5a4eb-140">Select **Always trust the source of Package Accelerators** to create virtualized packages using a package accelerator without being prompted for authorization.</span></span>

    <span data-ttu-id="5a4eb-141">**Wichtig**  Mit App-v 4.6 erstellte Paket Beschleuniger werden von App-v 5,0 nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="5a4eb-141">**Important** Package Accelerators created using App-V4.6 are not supported by App-V 5.0.</span></span>

     

-   <span data-ttu-id="5a4eb-142">**Analysieren von Elementen**</span><span class="sxs-lookup"><span data-stu-id="5a4eb-142">**Parse Items**.</span></span> <span data-ttu-id="5a4eb-143">Auf dieser Registerkarte werden die zugehörigen Dateipfad-Speicherorte angezeigt, die in der virtuellen Umgebung analysiert oder in Tokens umgewandelt werden.</span><span class="sxs-lookup"><span data-stu-id="5a4eb-143">This tab displays the associated file path locations that will be parsed or tokenized into in the virtual environment.</span></span> <span data-ttu-id="5a4eb-144">Token sind hilfreich beim Hinzufügen von Dateien auf der Registerkarte **Paketdateien** in der **erweiterten Bearbeitung**.</span><span class="sxs-lookup"><span data-stu-id="5a4eb-144">Tokens are useful for adding files using the **Package Files** tab in **Advanced Editing**.</span></span>

-   <span data-ttu-id="5a4eb-145">**Ausschlusselemente**.</span><span class="sxs-lookup"><span data-stu-id="5a4eb-145">**Exclusion Items**.</span></span> <span data-ttu-id="5a4eb-146">Auf dieser Registerkarte können Sie angeben, welche Ordner und Verzeichnisse während der Sequenzierung nicht überwacht werden sollen.</span><span class="sxs-lookup"><span data-stu-id="5a4eb-146">Use this tab to specify which folders and directories should not be monitored during sequencing.</span></span> <span data-ttu-id="5a4eb-147">Wenn Sie lokale Anwendungsdaten hinzufügen möchten, die im lokalen app-Datenordner im Paket gespeichert sind, klicken Sie auf **neu** , und geben Sie den Speicherort und den zugehörigen **Zuordnungstyp**an.</span><span class="sxs-lookup"><span data-stu-id="5a4eb-147">To add local application data that is saved in the Local App Data folder in the package, click **New** and specify the location and the associated **Mapping Type**.</span></span> <span data-ttu-id="5a4eb-148">Diese Option ist für einige Pakete erforderlich.</span><span class="sxs-lookup"><span data-stu-id="5a4eb-148">This option is required for some packages.</span></span>

<span data-ttu-id="5a4eb-149">App-V 5,0 unterstützt Anwendungen, die Microsoft Windows-Dienste umfassen.</span><span class="sxs-lookup"><span data-stu-id="5a4eb-149">App-V 5.0 supports applications that include Microsoft Windows Services.</span></span> <span data-ttu-id="5a4eb-150">Wenn eine Anwendung einen Windows-Dienst enthält, wird der Dienst in das sequenzierte virtuelle Paket aufgenommen, solange er während der Überwachung durch den Sequencer installiert wird.</span><span class="sxs-lookup"><span data-stu-id="5a4eb-150">If an application includes a Windows service, the Service will be included in the sequenced virtual package as long as it is installed while being monitored by the sequencer.</span></span> <span data-ttu-id="5a4eb-151">Wenn eine virtuelle Anwendung beim anfänglichen ausführen einen Windows-Dienst erstellt, muss die Anwendung später nach der Installation ausgeführt werden, während der Sequencer überwacht wird, damit der Windows-Dienst dem Paket hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="5a4eb-151">If a virtual application creates a Windows service when it initially runs, then later, after installation, the application must be run while the sequencer is monitoring so that the Windows Service will be added to the package.</span></span> <span data-ttu-id="5a4eb-152">Nur Dienste, die unter dem lokalen System Konto ausgeführt werden, werden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="5a4eb-152">Only Services that run under the Local System account are supported.</span></span> <span data-ttu-id="5a4eb-153">Dienste, die für Autostart oder verzögerter Autostart konfiguriert sind, werden gestartet, bevor die erste virtuelle Anwendung in einem Paket innerhalb der virtuellen Umgebung des Pakets ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5a4eb-153">Services that are configured for AutoStart or Delayed AutoStart are started before the first virtual application in a package runs inside the package’s Virtual Environment.</span></span> <span data-ttu-id="5a4eb-154">Windows-Dienste, die so konfiguriert sind, dass Sie bei Bedarf von einer Anwendung gestartet werden, werden gestartet, wenn die virtuelle Anwendung im Paket den Dienst über API-Aufruf startet.</span><span class="sxs-lookup"><span data-stu-id="5a4eb-154">Windows Services that are configured to be started on demand by an application are started when the virtual application inside the package starts the Service via API call.</span></span>

[<span data-ttu-id="5a4eb-155">So sequenzieren Sie eine neue Anwendung mit App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="5a4eb-155">How to Sequence a New Application with App-V 5.0</span></span>](how-to-sequence-a-new-application-with-app-v-50-beta-gb18030.md)

## <a href="" id="---------app-v-5-0-sp2-shell-extension-support"></a> <span data-ttu-id="5a4eb-156">App-V 5.0 SP2-Unterstützung für Shell-Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="5a4eb-156">App-V 5.0SP2 shell extension support</span></span>


<span data-ttu-id="5a4eb-157">App-V 5.0 SP2 unterstützt Shell-Erweiterungen.</span><span class="sxs-lookup"><span data-stu-id="5a4eb-157">App-V 5.0SP2 supports shell extensions.</span></span> <span data-ttu-id="5a4eb-158">Shell-Erweiterungen werden während der Sequenzierung erkannt und in das Paket eingebettet.</span><span class="sxs-lookup"><span data-stu-id="5a4eb-158">Shell extensions will be detected and embedded in the package during sequencing.</span></span>

<span data-ttu-id="5a4eb-159">Shell-Erweiterungen werden während des Sequenz Prozesses automatisch in das Paket eingebettet.</span><span class="sxs-lookup"><span data-stu-id="5a4eb-159">Shell extensions are embedded in the package automatically during the sequencing process.</span></span> <span data-ttu-id="5a4eb-160">Wenn das Paket veröffentlicht wird, gibt die Shell-Erweiterung Benutzern dieselbe Funktionalität wie bei der lokalen Installation der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="5a4eb-160">When the package is published, the shell extension gives users the same functionality as if the application were locally installed.</span></span>

**<span data-ttu-id="5a4eb-161">Voraussetzungen für die Verwendung von Shell-Erweiterungen:</span><span class="sxs-lookup"><span data-stu-id="5a4eb-161">Requirements for using shell extensions:</span></span>**

-   <span data-ttu-id="5a4eb-162">Pakete, die eingebettete Shell-Erweiterungen enthalten, müssen global veröffentlicht werden.</span><span class="sxs-lookup"><span data-stu-id="5a4eb-162">Packages that contain embedded shell extensions must be published globally.</span></span> <span data-ttu-id="5a4eb-163">Die Anwendung erfordert keine zusätzliche Einrichtung oder Konfiguration auf dem Client, um die Shell-Erweiterungsfunktion zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="5a4eb-163">The application requires no additional setup or configuration on the client to enable the shell extension functionality.</span></span>

-   <span data-ttu-id="5a4eb-164">Die "Bitanzahl" der Anwendung, des Sequencers und des App-V-Clients müssen übereinstimmen, oder die Shell-Erweiterungen funktionieren nicht.</span><span class="sxs-lookup"><span data-stu-id="5a4eb-164">The “bitness” of the application, Sequencer, and App-V client must match, or the shell extensions won’t work.</span></span> <span data-ttu-id="5a4eb-165">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="5a4eb-165">For example:</span></span>

    -   <span data-ttu-id="5a4eb-166">Die Version der Anwendung ist 64-Bit.</span><span class="sxs-lookup"><span data-stu-id="5a4eb-166">The version of the application is 64-bit.</span></span>

    -   <span data-ttu-id="5a4eb-167">Der Sequencer wird auf einem 64-Bit-Computer ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5a4eb-167">The Sequencer is running on a 64-bit computer.</span></span>

    -   <span data-ttu-id="5a4eb-168">Das Paket wird an einen 64-Bit-App-V-Clientcomputer übermittelt.</span><span class="sxs-lookup"><span data-stu-id="5a4eb-168">The package is being delivered to a 64-bit App-V client computer.</span></span>

<span data-ttu-id="5a4eb-169">In der folgenden Tabelle sind die unterstützten Shell-Erweiterungen aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="5a4eb-169">The following table lists the supported shell extensions:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="5a4eb-170">Handler</span><span class="sxs-lookup"><span data-stu-id="5a4eb-170">Handler</span></span></th>
<th align="left"><span data-ttu-id="5a4eb-171">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5a4eb-171">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5a4eb-172">Kontextmenü Handler</span><span class="sxs-lookup"><span data-stu-id="5a4eb-172">Context menu handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="5a4eb-173">Fügt dem Kontextmenü Menüelemente hinzu.</span><span class="sxs-lookup"><span data-stu-id="5a4eb-173">Adds menu items to the context menu.</span></span> <span data-ttu-id="5a4eb-174">Sie wird aufgerufen, bevor das Kontextmenü angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="5a4eb-174">It is called before the context menu is displayed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5a4eb-175">Drag & Drop-Handler</span><span class="sxs-lookup"><span data-stu-id="5a4eb-175">Drag-and-drop handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="5a4eb-176">Steuert die Aktion, bei der mit der rechten Maustaste, ziehen und ablegen und das Kontextmenü geändert wird, das angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="5a4eb-176">Controls the action where right-click, drag and drop and modifies the context menu that appears.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5a4eb-177">Ablegen eines Ziel Handlers</span><span class="sxs-lookup"><span data-stu-id="5a4eb-177">Drop target handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="5a4eb-178">Steuert die Aktion, nachdem ein Datenobjekt gezogen und über ein Ablageziel wie eine Datei abgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="5a4eb-178">Controls the action after a data object is dragged and dropped over a drop target such as a file.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5a4eb-179">Datenobjekt-Handler</span><span class="sxs-lookup"><span data-stu-id="5a4eb-179">Data object handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="5a4eb-180">Steuert die Aktion, nachdem eine Datei in die Zwischenablage kopiert oder auf einem Ablageziel gezogen und abgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="5a4eb-180">Controls the action after a file is copied to the clipboard or dragged and dropped over a drop target.</span></span> <span data-ttu-id="5a4eb-181">Sie kann dem Ablageziel zusätzliche Zwischenablageformate zur Verfügung stellen.</span><span class="sxs-lookup"><span data-stu-id="5a4eb-181">It can provide additional clipboard formats to the drop target.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5a4eb-182">Eigenschaftentabellen-Handler</span><span class="sxs-lookup"><span data-stu-id="5a4eb-182">Property sheet handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="5a4eb-183">Ersetzt oder fügt Seiten in das DialogfeldEigenschaften Fenster eines Objekts ein.</span><span class="sxs-lookup"><span data-stu-id="5a4eb-183">Replaces or adds pages to the property sheet dialog box of an object.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5a4eb-184">Infotipp-Handler</span><span class="sxs-lookup"><span data-stu-id="5a4eb-184">Infotip handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="5a4eb-185">Ermöglicht das Abrufen von Flags und Infotipp-Informationen für ein Element und das Anzeigen des Elements in einer Popup-QuickInfo, wenn Sie den Mauszeiger bewegen.</span><span class="sxs-lookup"><span data-stu-id="5a4eb-185">Allows retrieving flags and infotip information for an item and displaying it inside a pop-up tooltip upon mouse hover.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5a4eb-186">Spalten Handler</span><span class="sxs-lookup"><span data-stu-id="5a4eb-186">Column handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="5a4eb-187">Ermöglicht das Erstellen und Anzeigen benutzerdefinierter Spalten in der <strong> Windows-Explorer-Detailansicht </strong> .</span><span class="sxs-lookup"><span data-stu-id="5a4eb-187">Allows creating and displaying custom columns in <strong>Windows Explorer Details view</strong>.</span></span> <span data-ttu-id="5a4eb-188">Sie kann zum Erweitern von Sortierung und Gruppierung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5a4eb-188">It can be used to extend sorting and grouping.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5a4eb-189">Vorschauhandler</span><span class="sxs-lookup"><span data-stu-id="5a4eb-189">Preview handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="5a4eb-190">Ermöglicht das Anzeigen einer Vorschau einer Datei im Vorschaubereich von Windows-Explorer.</span><span class="sxs-lookup"><span data-stu-id="5a4eb-190">Enables a preview of a file to be displayed in the Windows Explorer Preview pane.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="5a4eb-191">Unterstützung für die Dateierweiterung beim Schreiben (Kuh)</span><span class="sxs-lookup"><span data-stu-id="5a4eb-191">Copy on Write (CoW) file extension support</span></span>


<span data-ttu-id="5a4eb-192">Die Dateierweiterungen Copy on Write (Cow) ermöglichen es App-V 5,0, dynamisch an bestimmte Speicherorte zu schreiben, die im virtuellen Paket enthalten sind, während es verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5a4eb-192">Copy on write (CoW) file extensions allow App-V 5.0 to dynamically write to specific locations contained in the virtual package while it is being used.</span></span>

<span data-ttu-id="5a4eb-193">In der folgenden Tabelle werden die Dateitypen angezeigt, die in einem virtuellen Paket unter dem VFS-Verzeichnis vorhanden sein können, aber auf dem Computer, auf dem der App-V 5,0-Client ausgeführt wird, nicht aktualisiert werden können.</span><span class="sxs-lookup"><span data-stu-id="5a4eb-193">The following table displays the file types that can exist in a virtual package under the VFS directory, but cannot be updated on the computer running the App-V 5.0 client.</span></span> <span data-ttu-id="5a4eb-194">Alle anderen Dateien und Verzeichnisse können geändert werden.</span><span class="sxs-lookup"><span data-stu-id="5a4eb-194">All other files and directories can be modified.</span></span>

<span data-ttu-id="5a4eb-195">. acm</span><span class="sxs-lookup"><span data-stu-id="5a4eb-195">.acm</span></span>

<span data-ttu-id="5a4eb-196">. ASA</span><span class="sxs-lookup"><span data-stu-id="5a4eb-196">.asa</span></span>

<span data-ttu-id="5a4eb-197">.asp</span><span class="sxs-lookup"><span data-stu-id="5a4eb-197">.asp</span></span>

<span data-ttu-id="5a4eb-198">. aspx</span><span class="sxs-lookup"><span data-stu-id="5a4eb-198">.aspx</span></span>

<span data-ttu-id="5a4eb-199">AX</span><span class="sxs-lookup"><span data-stu-id="5a4eb-199">.ax</span></span>

<span data-ttu-id="5a4eb-200">BAT</span><span class="sxs-lookup"><span data-stu-id="5a4eb-200">.bat</span></span>

<span data-ttu-id="5a4eb-201">.cer</span><span class="sxs-lookup"><span data-stu-id="5a4eb-201">.cer</span></span>

<span data-ttu-id="5a4eb-202">.chm</span><span class="sxs-lookup"><span data-stu-id="5a4eb-202">.chm</span></span>

<span data-ttu-id="5a4eb-203">. CLB</span><span class="sxs-lookup"><span data-stu-id="5a4eb-203">.clb</span></span>

<span data-ttu-id="5a4eb-204">.cmd</span><span class="sxs-lookup"><span data-stu-id="5a4eb-204">.cmd</span></span>

<span data-ttu-id="5a4eb-205">.cnt</span><span class="sxs-lookup"><span data-stu-id="5a4eb-205">.cnt</span></span>

<span data-ttu-id="5a4eb-206">. cnv</span><span class="sxs-lookup"><span data-stu-id="5a4eb-206">.cnv</span></span>

<span data-ttu-id="5a4eb-207">.com</span><span class="sxs-lookup"><span data-stu-id="5a4eb-207">.com</span></span>

<span data-ttu-id="5a4eb-208">.cpl</span><span class="sxs-lookup"><span data-stu-id="5a4eb-208">.cpl</span></span>

<span data-ttu-id="5a4eb-209">. CPX</span><span class="sxs-lookup"><span data-stu-id="5a4eb-209">.cpx</span></span>

<span data-ttu-id="5a4eb-210">.crt</span><span class="sxs-lookup"><span data-stu-id="5a4eb-210">.crt</span></span>

<span data-ttu-id="5a4eb-211">.dll</span><span class="sxs-lookup"><span data-stu-id="5a4eb-211">.dll</span></span>

<span data-ttu-id="5a4eb-212">.drv</span><span class="sxs-lookup"><span data-stu-id="5a4eb-212">.drv</span></span>

<span data-ttu-id="5a4eb-213">EXE</span><span class="sxs-lookup"><span data-stu-id="5a4eb-213">.exe</span></span>

<span data-ttu-id="5a4eb-214">.fon</span><span class="sxs-lookup"><span data-stu-id="5a4eb-214">.fon</span></span>

<span data-ttu-id="5a4eb-215">.grp</span><span class="sxs-lookup"><span data-stu-id="5a4eb-215">.grp</span></span>

<span data-ttu-id="5a4eb-216">.hlp</span><span class="sxs-lookup"><span data-stu-id="5a4eb-216">.hlp</span></span>

<span data-ttu-id="5a4eb-217">.hta</span><span class="sxs-lookup"><span data-stu-id="5a4eb-217">.hta</span></span>

<span data-ttu-id="5a4eb-218">. IME</span><span class="sxs-lookup"><span data-stu-id="5a4eb-218">.ime</span></span>

<span data-ttu-id="5a4eb-219">INF</span><span class="sxs-lookup"><span data-stu-id="5a4eb-219">.inf</span></span>

<span data-ttu-id="5a4eb-220">INS</span><span class="sxs-lookup"><span data-stu-id="5a4eb-220">.ins</span></span>

<span data-ttu-id="5a4eb-221">.isp</span><span class="sxs-lookup"><span data-stu-id="5a4eb-221">.isp</span></span>

<span data-ttu-id="5a4eb-222">. its</span><span class="sxs-lookup"><span data-stu-id="5a4eb-222">.its</span></span>

<span data-ttu-id="5a4eb-223">.js</span><span class="sxs-lookup"><span data-stu-id="5a4eb-223">.js</span></span>

<span data-ttu-id="5a4eb-224">.jse</span><span class="sxs-lookup"><span data-stu-id="5a4eb-224">.jse</span></span>

<span data-ttu-id="5a4eb-225">.lnk</span><span class="sxs-lookup"><span data-stu-id="5a4eb-225">.lnk</span></span>

<span data-ttu-id="5a4eb-226">.msc</span><span class="sxs-lookup"><span data-stu-id="5a4eb-226">.msc</span></span>

<span data-ttu-id="5a4eb-227">.msi</span><span class="sxs-lookup"><span data-stu-id="5a4eb-227">.msi</span></span>

<span data-ttu-id="5a4eb-228">.msp</span><span class="sxs-lookup"><span data-stu-id="5a4eb-228">.msp</span></span>

<span data-ttu-id="5a4eb-229">.mst</span><span class="sxs-lookup"><span data-stu-id="5a4eb-229">.mst</span></span>

<span data-ttu-id="5a4eb-230">. MUI</span><span class="sxs-lookup"><span data-stu-id="5a4eb-230">.mui</span></span>

<span data-ttu-id="5a4eb-231">. nls</span><span class="sxs-lookup"><span data-stu-id="5a4eb-231">.nls</span></span>

<span data-ttu-id="5a4eb-232">.ocx</span><span class="sxs-lookup"><span data-stu-id="5a4eb-232">.ocx</span></span>

<span data-ttu-id="5a4eb-233">. PAL</span><span class="sxs-lookup"><span data-stu-id="5a4eb-233">.pal</span></span>

<span data-ttu-id="5a4eb-234">.pcd</span><span class="sxs-lookup"><span data-stu-id="5a4eb-234">.pcd</span></span>

<span data-ttu-id="5a4eb-235">.pif</span><span class="sxs-lookup"><span data-stu-id="5a4eb-235">.pif</span></span>

<span data-ttu-id="5a4eb-236">.reg</span><span class="sxs-lookup"><span data-stu-id="5a4eb-236">.reg</span></span>

<span data-ttu-id="5a4eb-237">.scf</span><span class="sxs-lookup"><span data-stu-id="5a4eb-237">.scf</span></span>

<span data-ttu-id="5a4eb-238">.scr</span><span class="sxs-lookup"><span data-stu-id="5a4eb-238">.scr</span></span>

<span data-ttu-id="5a4eb-239">. SCT</span><span class="sxs-lookup"><span data-stu-id="5a4eb-239">.sct</span></span>

<span data-ttu-id="5a4eb-240">.shb</span><span class="sxs-lookup"><span data-stu-id="5a4eb-240">.shb</span></span>

<span data-ttu-id="5a4eb-241">.shs</span><span class="sxs-lookup"><span data-stu-id="5a4eb-241">.shs</span></span>

<span data-ttu-id="5a4eb-242">.sys</span><span class="sxs-lookup"><span data-stu-id="5a4eb-242">.sys</span></span>

<span data-ttu-id="5a4eb-243">. tlb</span><span class="sxs-lookup"><span data-stu-id="5a4eb-243">.tlb</span></span>

<span data-ttu-id="5a4eb-244">. tsp</span><span class="sxs-lookup"><span data-stu-id="5a4eb-244">.tsp</span></span>

<span data-ttu-id="5a4eb-245">.url</span><span class="sxs-lookup"><span data-stu-id="5a4eb-245">.url</span></span>

<span data-ttu-id="5a4eb-246">.vb</span><span class="sxs-lookup"><span data-stu-id="5a4eb-246">.vb</span></span>

<span data-ttu-id="5a4eb-247">.vbe</span><span class="sxs-lookup"><span data-stu-id="5a4eb-247">.vbe</span></span>

<span data-ttu-id="5a4eb-248">.vbs</span><span class="sxs-lookup"><span data-stu-id="5a4eb-248">.vbs</span></span>

<span data-ttu-id="5a4eb-249">.vsmacros</span><span class="sxs-lookup"><span data-stu-id="5a4eb-249">.vsmacros</span></span>

<span data-ttu-id="5a4eb-250">.ws</span><span class="sxs-lookup"><span data-stu-id="5a4eb-250">.ws</span></span>

<span data-ttu-id="5a4eb-251">. ESC</span><span class="sxs-lookup"><span data-stu-id="5a4eb-251">.esc</span></span>

<span data-ttu-id="5a4eb-252">.wsf</span><span class="sxs-lookup"><span data-stu-id="5a4eb-252">.wsf</span></span>

<span data-ttu-id="5a4eb-253">.wsh</span><span class="sxs-lookup"><span data-stu-id="5a4eb-253">.wsh</span></span>

 

## <span data-ttu-id="5a4eb-254">Ändern eines vorhandenen virtuellen Anwendungspakets</span><span class="sxs-lookup"><span data-stu-id="5a4eb-254">Modifying an existing virtual application package</span></span>


<span data-ttu-id="5a4eb-255">Sie können den Sequencer verwenden, um ein vorhandenes Paket zu ändern.</span><span class="sxs-lookup"><span data-stu-id="5a4eb-255">You can use the sequencer to modify an existing package.</span></span> <span data-ttu-id="5a4eb-256">Der Computer, auf dem Sie dies tun, sollte der Chiparchitektur des Computers entsprechen, den Sie zum Erstellen der Anwendung verwendet haben.</span><span class="sxs-lookup"><span data-stu-id="5a4eb-256">The computer on which you do this should match the chip architecture of the computer you used to create the application.</span></span> <span data-ttu-id="5a4eb-257">Wenn Sie beispielsweise ein Paket zunächst auf einem Computer mit einem 64-Bit-Betriebssystem sequenziert haben, sollten Sie das Paket auf einem Computer ändern, auf dem ein 64-Bit-Betriebssystem ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5a4eb-257">For example, if you initially sequenced a package using a computer running a 64-bit operating system, you should modify the package using a computer running a 64-bit operating system.</span></span>

[<span data-ttu-id="5a4eb-258">So ändern Sie ein vorhandenes virtuelles Anwendungspaket</span><span class="sxs-lookup"><span data-stu-id="5a4eb-258">How to Modify an Existing Virtual Application Package</span></span>](how-to-modify-an-existing-virtual-application-package-beta.md)

## <span data-ttu-id="5a4eb-259">Erstellen einer Projektvorlage</span><span class="sxs-lookup"><span data-stu-id="5a4eb-259">Creating a project template</span></span>


<span data-ttu-id="5a4eb-260">Bei einer appvt-Datei handelt es sich um eine Projektvorlage, die verwendet werden kann, um häufig angewendete, angepasste Einstellungen zu speichern.</span><span class="sxs-lookup"><span data-stu-id="5a4eb-260">A .appvt file is a project template that can be used to save commonly applied, customized settings.</span></span> <span data-ttu-id="5a4eb-261">Sie können diese Einstellungen dann einfacher für zukünftige Sequenzen verwenden.</span><span class="sxs-lookup"><span data-stu-id="5a4eb-261">You can then more easily use these settings for future sequencings.</span></span>

<span data-ttu-id="5a4eb-262">App-v 5,0-Projektvorlagen unterscheiden sich von App-v 5,0-Anwendungs Beschleunigern, da App-v 5,0-Anwendungs Beschleuniger anwendungsspezifisch sind und App-v 5,0-Projektvorlagen auf mehrere Anwendungen angewendet werden können.</span><span class="sxs-lookup"><span data-stu-id="5a4eb-262">App-V 5.0 project templates differ from App-V 5.0 Application Accelerators because App-V 5.0 Application Accelerators are application-specific, and App-V 5.0 project templates can be applied to multiple applications.</span></span> <span data-ttu-id="5a4eb-263">Darüber hinaus können Sie keine Projektvorlage verwenden, wenn Sie ein Paket Beschleuniger zum Erstellen eines virtuellen Anwendungspakets verwenden.</span><span class="sxs-lookup"><span data-stu-id="5a4eb-263">Additionally, you cannot use a project template when you use a Package Accelerator to create a virtual application package.</span></span> <span data-ttu-id="5a4eb-264">Die folgenden allgemeinen Einstellungen werden mit einer App-V 5,0-Projektvorlage gespeichert:</span><span class="sxs-lookup"><span data-stu-id="5a4eb-264">The following general settings are saved with an App-V 5.0 project template:</span></span>

<span data-ttu-id="5a4eb-265">Eine Vorlage kann mehrere Einstellungen wie folgt angeben und speichern:</span><span class="sxs-lookup"><span data-stu-id="5a4eb-265">A template can specify and store multiple settings as follows:</span></span>

-   <span data-ttu-id="5a4eb-266">**Erweiterte Überwachungsoptionen**.</span><span class="sxs-lookup"><span data-stu-id="5a4eb-266">**Advanced Monitoring Options**.</span></span> <span data-ttu-id="5a4eb-267">Ermöglicht die Ausführung von Microsoft Update während der Überwachung.</span><span class="sxs-lookup"><span data-stu-id="5a4eb-267">Enables Microsoft Update to run during monitoring.</span></span> <span data-ttu-id="5a4eb-268">Speichert Einstellungen für lokale interaktionsoptionen zulassen</span><span class="sxs-lookup"><span data-stu-id="5a4eb-268">Saves allow local interaction option settings</span></span>

-   <span data-ttu-id="5a4eb-269">**Allgemeine Optionen**.</span><span class="sxs-lookup"><span data-stu-id="5a4eb-269">**General Options**.</span></span> <span data-ttu-id="5a4eb-270">Aktiviert die Verwendung von **Windows Installer**und **fügt die Paket Version an filename an**.</span><span class="sxs-lookup"><span data-stu-id="5a4eb-270">Enables the use of **Windows Installer**, **Append Package Version to Filename**.</span></span>

-   **<span data-ttu-id="5a4eb-271">Ausschlusselemente.</span><span class="sxs-lookup"><span data-stu-id="5a4eb-271">Exclusion Items.</span></span>** <span data-ttu-id="5a4eb-272">Enthält die Ausschlussmuster Liste.</span><span class="sxs-lookup"><span data-stu-id="5a4eb-272">Contains the Exclusion pattern list.</span></span>

[<span data-ttu-id="5a4eb-273">So erstellen und verwenden Sie eine Projektvorlage</span><span class="sxs-lookup"><span data-stu-id="5a4eb-273">How to Create and Use a Project Template</span></span>](how-to-create-and-use-a-project-template.md)

## <span data-ttu-id="5a4eb-274">Erstellen eines Paket Beschleunigers</span><span class="sxs-lookup"><span data-stu-id="5a4eb-274">Creating a package accelerator</span></span>


<span data-ttu-id="5a4eb-275">**Hinweis**  Paket Beschleuniger, die mit einer früheren Version von App-v erstellt wurden, müssen mit App-v 5,0 neu erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="5a4eb-275">**Note** Package accelerators created using a previous version of App-V must be recreated using App-V 5.0.</span></span>

 

<span data-ttu-id="5a4eb-276">Sie können App-V 5,0-Paket Beschleuniger verwenden, um automatisch neue virtuelle Anwendungspakete zu generieren.</span><span class="sxs-lookup"><span data-stu-id="5a4eb-276">You can use App-V 5.0 package accelerators to automatically generate a new virtual application packages.</span></span> <span data-ttu-id="5a4eb-277">Nachdem Sie erfolgreich einen Paket Beschleuniger erstellt haben, können Sie den Paket Beschleuniger wieder verwenden und freigeben.</span><span class="sxs-lookup"><span data-stu-id="5a4eb-277">After you have successfully created a package accelerator, you can reuse and share the package accelerator.</span></span>

<span data-ttu-id="5a4eb-278">In einigen Fällen müssen Sie möglicherweise die Anwendung lokal auf dem Computer installieren, auf dem der Sequencer ausgeführt wird, um den Paket Beschleuniger zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="5a4eb-278">In some situations, to create the package accelerator, you might have to install the application locally on the computer that runs the sequencer.</span></span> <span data-ttu-id="5a4eb-279">In solchen Fällen sollten Sie zunächst versuchen, den Paket Beschleuniger mit dem Installationsmedium zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="5a4eb-279">In such cases, you should first try to create the package accelerator with the installation media.</span></span> <span data-ttu-id="5a4eb-280">Wenn mehrere fehlende Dateien erforderlich sind, sollten Sie die Anwendung lokal auf dem Computer installieren, auf dem der Sequencer ausgeführt wird, und dann den Paket Beschleuniger erstellen.</span><span class="sxs-lookup"><span data-stu-id="5a4eb-280">If multiple missing files are required, you should install the application locally to the computer that runs the sequencer, and then create the package accelerator.</span></span>

<span data-ttu-id="5a4eb-281">Nachdem Sie erfolgreich einen Paket Beschleuniger erstellt haben, können Sie den Paket Beschleuniger wieder verwenden und freigeben.</span><span class="sxs-lookup"><span data-stu-id="5a4eb-281">After you have successfully created a Package Accelerator, you can reuse and share the Package Accelerator.</span></span> <span data-ttu-id="5a4eb-282">Das Erstellen von App-V 5,0-Paket Beschleunigern ist eine erweiterte Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="5a4eb-282">Creating App-V 5.0 Package Accelerators is an advanced task.</span></span> <span data-ttu-id="5a4eb-283">Paket Beschleuniger können Kennwort-und benutzerspezifische Informationen enthalten.</span><span class="sxs-lookup"><span data-stu-id="5a4eb-283">Package Accelerators can contain password and user-specific information.</span></span> <span data-ttu-id="5a4eb-284">Daher müssen Sie Paket Beschleuniger und die zugehörigen Installationsmedien an einem sicheren Speicherort speichern, und Sie sollten den Paket Beschleuniger nach der Erstellung digital signieren, damit der Herausgeber überprüft werden kann, wenn der App-V 5,0-Paket Beschleuniger angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="5a4eb-284">Therefore you must save Package Accelerators and the associated installation media in a secure location, and you should digitally sign the Package Accelerator after you create it so that the publisher can be verified when the App-V 5.0 Package Accelerator is applied.</span></span>

[<span data-ttu-id="5a4eb-285">So erstellen Sie einen Package Accelerator</span><span class="sxs-lookup"><span data-stu-id="5a4eb-285">How to Create a Package Accelerator</span></span>](how-to-create-a-package-accelerator.md)

[<span data-ttu-id="5a4eb-286">So erstellen Sie ein virtuelles Anwendungspaket mit einem App-V Package Accelerator</span><span class="sxs-lookup"><span data-stu-id="5a4eb-286">How to Create a Virtual Application Package Using an App-V Package Accelerator</span></span>](how-to-create-a-virtual-application-package-using-an-app-v-package-accelerator.md)

## <span data-ttu-id="5a4eb-287">Sequenzer-Fehlerberichterstattung</span><span class="sxs-lookup"><span data-stu-id="5a4eb-287">Sequencer error reporting</span></span>


<span data-ttu-id="5a4eb-288">Der App-V 5,0-Sequenzer kann häufige Sequenzierungs Probleme während der Sequenzierung erkennen.</span><span class="sxs-lookup"><span data-stu-id="5a4eb-288">The App-V 5.0 Sequencer can detect common sequencing issues during sequencing.</span></span> <span data-ttu-id="5a4eb-289">Auf der Seite " **Installationsbericht** " am Ende des Sequenz-Assistenten werden in Abhängigkeit vom Schweregrad des Problems diagnostische Nachrichten angezeigt, die in **Fehler**, **Warnungen**und **Informationen** kategorisiert sind.</span><span class="sxs-lookup"><span data-stu-id="5a4eb-289">The **Installation Report** page at the end of the sequencing wizard displays diagnostic messages categorized into **Errors**, **Warnings**, and **Info** depending on the severity of the issue.</span></span>

<span data-ttu-id="5a4eb-290">Weitere Informationen zu Sequenz Fehlern finden Sie auch unter Verwendung der Windows-Ereignisanzeige.</span><span class="sxs-lookup"><span data-stu-id="5a4eb-290">You can also find additional information about sequencing errors using the Windows Event Viewer.</span></span>






## <a href="" id="other-resources-for-the-app-v-5-0-sequencer-"></a><span data-ttu-id="5a4eb-291">Weitere Ressourcen für den App-V 5,0-Sequenzer</span><span class="sxs-lookup"><span data-stu-id="5a4eb-291">Other resources for the App-V 5.0 sequencer</span></span>


-   [<span data-ttu-id="5a4eb-292">Vorgänge für App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="5a4eb-292">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

 

 





