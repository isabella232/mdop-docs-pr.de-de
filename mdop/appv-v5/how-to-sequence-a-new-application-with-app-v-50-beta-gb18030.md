---
title: So sequenzieren Sie eine neue Anwendung mit App-V 5.0
description: So sequenzieren Sie eine neue Anwendung mit App-V 5.0
author: dansimp
ms.assetid: a263fa84-cd6d-4219-a5c2-eb6a553b826c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 13fdda066f79d918da1970e0cab6c1d6e60f6585
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805189"
---
# <span data-ttu-id="3eaa3-103">So sequenzieren Sie eine neue Anwendung mit App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="3eaa3-103">How to Sequence a New Application with App-V 5.0</span></span>


**<span data-ttu-id="3eaa3-104">Zu überprüfen oder zu tun, bevor Sie mit der Sequenzierung beginnen</span><span class="sxs-lookup"><span data-stu-id="3eaa3-104">To review or do before you start sequencing</span></span>**

1.  <span data-ttu-id="3eaa3-105">Ermitteln Sie den Typ des virtualisierten Anwendungspakets, das Sie erstellen möchten:</span><span class="sxs-lookup"><span data-stu-id="3eaa3-105">Determine the type of virtualized application package you want to create:</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="3eaa3-106">Anwendungstyp</span><span class="sxs-lookup"><span data-stu-id="3eaa3-106">Application type</span></span></th>
    <th align="left"><span data-ttu-id="3eaa3-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3eaa3-107">Description</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="3eaa3-108">Standard</span><span class="sxs-lookup"><span data-stu-id="3eaa3-108">Standard</span></span></p></td>
    <td align="left"><p><span data-ttu-id="3eaa3-109">Erstellt ein Paket, das eine Anwendung oder eine Suite von Anwendungen enthält.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-109">Creates a package that contains an application or a suite of applications.</span></span> <span data-ttu-id="3eaa3-110">Dies ist die bevorzugte Option für die meisten Anwendungstypen.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-110">This is the preferred option for most application types.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="3eaa3-111">Add-on oder Plug-in</span><span class="sxs-lookup"><span data-stu-id="3eaa3-111">Add-on or plug-in</span></span></p></td>
    <td align="left"><p><span data-ttu-id="3eaa3-112">Erstellt ein Paket, das die Funktionalität einer Standardanwendung erweitert, beispielsweise ein Plug-in für Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-112">Creates a package that extends the functionality of a standard application, for example, a plug-in for Microsoft Excel.</span></span> <span data-ttu-id="3eaa3-113">Darüber hinaus können Sie Plug-Ins für nativ installierte Anwendungen oder ein anderes Paket verwenden, das mithilfe von Verbindungsgruppen verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-113">Additionally, you can use plug-ins for natively installed applications, or for another package that is linked by using connection groups.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="3eaa3-114">Middleware</span><span class="sxs-lookup"><span data-stu-id="3eaa3-114">Middleware</span></span></p></td>
    <td align="left"><p><span data-ttu-id="3eaa3-115">Erstellt ein Paket, das für eine Standardanwendung, beispielsweise Java, erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-115">Creates a package that is required by a standard application, for example, Java.</span></span> <span data-ttu-id="3eaa3-116">Middleware-Pakete werden für Verknüpfungen mit anderen Paketen mithilfe von Verbindungsgruppen verwendet.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-116">Middleware packages are used for linking to other packages by using connection groups.</span></span></p></td>
    </tr>
    </tbody>
    </table>



2.  <span data-ttu-id="3eaa3-117">Kopieren Sie alle erforderlichen Installationsdateien auf den Computer, auf dem der Sequencer ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-117">Copy all required installation files to the computer that is running the sequencer.</span></span>

3.  <span data-ttu-id="3eaa3-118">Erstellen Sie ein Sicherungsabbild Ihrer virtuellen Umgebung, bevor Sie eine Anwendung sequenzieren, und kehren Sie dann jedes Mal wieder zu diesem Bild zurück, nachdem Sie die Sequenzierung einer Anwendung abgeschlossen haben.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-118">Make a backup image of your virtual environment before sequencing an application, and then revert to that image each time after you finish sequencing an application.</span></span>

4.  <span data-ttu-id="3eaa3-119">Überprüfen Sie die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="3eaa3-119">Review the following items:</span></span>

    -   <span data-ttu-id="3eaa3-120">Wenn ein Anwendungs Installationsprogramm den Sicherheitszugriff auf eine neue oder vorhandene Datei oder ein vorhandenes Verzeichnis ändert, werden diese Änderungen nicht im Paket erfasst.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-120">If an application installer changes the security access to a new or existing file or directory, those changes are not captured in the package.</span></span>

    -   <span data-ttu-id="3eaa3-121">Wenn kurze Pfade für das Zielvolumen des virtualisierten Pakets deaktiviert wurden, müssen Sie das Paket auch auf ein Volume abbilden, das erstellt wurde und bei dem die Short-Pfade deaktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-121">If short paths have been disabled for the virtualized package’s target volume, you must also sequence the package to a volume that was created and still has short-paths disabled.</span></span> <span data-ttu-id="3eaa3-122">Dies kann nicht das System Volume sein.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-122">It cannot be the system volume.</span></span>

    -   <span data-ttu-id="3eaa3-123">Ab App-V 5,0 SP3 ist das primäre Virtual Application Directory (PVAD) ausgeblendet, Sie können es aber wieder aktivieren.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-123">Starting in App-V 5.0 SP3, the primary virtual application directory (PVAD) is hidden, but you can turn it back on.</span></span> <span data-ttu-id="3eaa3-124">Informationen finden Sie unter [App-V 5,0 SP3](about-app-v-50-sp3.md#bkmk-pvad-hidden).</span><span class="sxs-lookup"><span data-stu-id="3eaa3-124">See [About App-V 5.0 SP3](about-app-v-50-sp3.md#bkmk-pvad-hidden).</span></span>

**<span data-ttu-id="3eaa3-125">So Sequenzieren Sie eine neue Standardanwendung</span><span class="sxs-lookup"><span data-stu-id="3eaa3-125">To sequence a new standard application</span></span>**

1.  <span data-ttu-id="3eaa3-126">Klicken Sie auf dem Computer, auf dem der Sequencer ausgeführt wird, auf **Alle Programme**, und klicken Sie dann auf **Microsoft Application Virtualization**, und klicken Sie dann auf **Microsoft Application Virtualization Sequencer**.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-126">On the computer that runs the sequencer, click **All Programs**, and then Click **Microsoft Application Virtualization**, and then click **Microsoft Application Virtualization Sequencer**.</span></span>

2.  <span data-ttu-id="3eaa3-127">Klicken Sie im Sequencer auf **Neues virtuelles Anwendungspaket erstellen**.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-127">In the sequencer, click **Create a New Virtual Application Package**.</span></span> <span data-ttu-id="3eaa3-128">Wählen Sie **Paket erstellen (Standard)** aus, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-128">Select **Create Package (default)**, and then click **Next**.</span></span>

3.  <span data-ttu-id="3eaa3-129">Überprüfen Sie auf der Seite **Computer vorbereiten** die Probleme, die dazu führen können, dass die Paketerstellung fehlschlägt oder dass das Paket unnötige Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-129">On the **Prepare Computer** page, review the issues that could cause the package creation to fail or could cause the package to contain unnecessary data.</span></span> <span data-ttu-id="3eaa3-130">Sie sollten alle potenziellen Probleme beheben, bevor Sie fortfahren.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-130">You should resolve all potential issues before you continue.</span></span> <span data-ttu-id="3eaa3-131">Nachdem Sie Korrekturen vorgenommen haben, klicken Sie auf **Aktualisieren** , um die aktualisierten Informationen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-131">After making any corrections, click **Refresh** to display the updated information.</span></span> <span data-ttu-id="3eaa3-132">Nachdem Sie alle potenziellen Probleme behoben haben, klicken Sie auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-132">After you have resolved all potential issues, click **Next**.</span></span>

    **<span data-ttu-id="3eaa3-133">Wichtig</span><span class="sxs-lookup"><span data-stu-id="3eaa3-133">Important</span></span>**  
    <span data-ttu-id="3eaa3-134">Wenn Sie die Virenscansoftware deaktivieren müssen, sollten Sie zuerst den Computer scannen, auf dem der Sequencer ausgeführt wird, um sicherzustellen, dass dem Paket keine unerwünschten oder böswilligen Dateien hinzugefügt werden können.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-134">If you are required to disable virus scanning software, you should first scan the computer that runs the sequencer in order to ensure that no unwanted or malicious files could be added to the package.</span></span>



4.  <span data-ttu-id="3eaa3-135">Klicken Sie auf der Seite **Typ der Anwendung** auf das Kontrollkästchen **Standardanwendung (Standard)** , und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-135">On the **Type of Application** page, click the **Standard Application (default)** check box, and then click **Next**.</span></span>

5.  <span data-ttu-id="3eaa3-136">Klicken Sie auf der Seite **Installationsprogramm auswählen** auf **Durchsuchen** , und geben Sie die Installationsdatei für die Anwendung an.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-136">On the **Select Installer** page, click **Browse** and specify the installation file for the application.</span></span>

    **<span data-ttu-id="3eaa3-137">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="3eaa3-137">Note</span></span>**  
    <span data-ttu-id="3eaa3-138">Wenn das angegebene Anwendungs Installationsprogramm den Sicherheitszugriff auf eine Datei oder ein Verzeichnis ändert, vorhandene oder neue, werden die zugehörigen Änderungen nicht in das Paket aufgenommen.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-138">If the specified application installer modifies security access to a file or directory, existing or new, the associated changes will not be captured into the package.</span></span>



~~~
If the application does not have an associated installer file and you plan to run all installation steps manually, select the **Perform a Custom Installation** check box, and then Click **Next**.
~~~

6. <span data-ttu-id="3eaa3-139">Geben Sie auf der Seite **Package Name** einen Namen ein, der dem Paket zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-139">On the **Package Name** page, type a name that will be associated with the package.</span></span> <span data-ttu-id="3eaa3-140">Verwenden Sie einen Namen, der hilft, den Zweck und die Version der Anwendung zu identifizieren, die dem Paket hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-140">Use a name that helps identify the purpose and version of the application that will be added to the package.</span></span> <span data-ttu-id="3eaa3-141">Der Paket Name wird in der App-V 5,0-Verwaltungskonsole angezeigt.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-141">The package name is displayed in the App-V 5.0 Management Console.</span></span>

   <span data-ttu-id="3eaa3-142">Das **primäre virtuelle Anwendungsverzeichnis** zeigt den Pfad an, in dem die Anwendung auf den Zielcomputern installiert wird.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-142">The **Primary Virtual Application Directory** displays the path where the application will be installed on target computers.</span></span> <span data-ttu-id="3eaa3-143">Wenn Sie diesen Speicherort angeben möchten, wählen Sie **Durchsuchen**aus.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-143">To specify this location, select **Browse**.</span></span>

   **<span data-ttu-id="3eaa3-144">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="3eaa3-144">Note</span></span>**  
   <span data-ttu-id="3eaa3-145">Ab App-V 5,0 SP3 ist das primäre Virtual Application Directory (PVAD) ausgeblendet, Sie können es aber wieder aktivieren.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-145">Starting in App-V 5.0 SP3, the primary virtual application directory (PVAD) is hidden, but you can turn it back on.</span></span> <span data-ttu-id="3eaa3-146">Informationen finden Sie unter [App-V 5,0 SP3](about-app-v-50-sp3.md#bkmk-pvad-hidden).</span><span class="sxs-lookup"><span data-stu-id="3eaa3-146">See [About App-V 5.0 SP3](about-app-v-50-sp3.md#bkmk-pvad-hidden).</span></span>



~~~
**Important**  
The primary application virtual directory should match the installation location for the application that is being sequenced. For example, if you install Notepad to **C:\\Program Files\\Notepad**; you should configure **C:\\Program Files\\Notepad** as your primary virtual directory. Alternatively, you can choose to set **C:\\Notepad** as the primary virtual application directory, as long as during installation time, you configure the installer to install to **C:\\Notepad**. Editing the Application Virtualization path is an advanced configuration task. For most applications, the default path is recommended for the following reasons:

-   Application Compatibility. Some virtualized applications will not function correctly, or will fail to open if the directories are not configured with identical virtual directory paths.

-   Performance. Since no file system redirection is required, the runtime performance can improve.



**Tip**  
It is recommended that prior to Sequencing an application, you open the associated installer to determine the default installation directory, and then configure that location as the **Primary Virtual Application Directory**.



Click **Next**.
~~~

7. <span data-ttu-id="3eaa3-147">Wenn der Sequencer und das Anwendungs Installationsprogramm bereit sind, können Sie auf der **Installations** Seite fortfahren, die Anwendung zu installieren, damit der Sequencer den Installationsvorgang überwachen kann.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-147">On the **Installation** page, when the sequencer and application installer are ready you can proceed to install the application so that the sequencer can monitor the installation process.</span></span>

   **<span data-ttu-id="3eaa3-148">Wichtig</span><span class="sxs-lookup"><span data-stu-id="3eaa3-148">Important</span></span>**  
   <span data-ttu-id="3eaa3-149">Sie sollten Anwendungen immer an einem sicheren Ort installieren und sicherstellen, dass während der Überwachung keine anderen Benutzer am Computer angemeldet sind, auf dem der Sequencer ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-149">You should always install applications to a secure location and make sure no other users are logged on to the computer running the sequencer during monitoring.</span></span>



~~~
Use the application's installation process to perform the installation. If additional installation files must be run as part of the installation, click **Run** to locate and run the additional installation files. When you are finished with the installation, select **I am finished installing**. Click **Next**.
~~~

8. <span data-ttu-id="3eaa3-150">Warten Sie auf der **Installations** Seite, während der Sequencer das virtualisierte Anwendungspaket konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-150">On the **Installation** page, wait while the sequencer configures the virtualized application package.</span></span>

9. <span data-ttu-id="3eaa3-151">Führen Sie auf der Seite **Software konfigurieren** optional die Programme aus, die im Paket enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-151">On the **Configure Software** page, optionally run the programs contained in the package.</span></span> <span data-ttu-id="3eaa3-152">In diesem Schritt können Sie alle erforderlichen Lizenz-oder Konfigurationsaufgaben ausführen, bevor Sie das Paket auf Zielcomputern bereitstellen und ausführen.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-152">This step allows you to complete any necessary license or configuration tasks before you deploy and run the package on target computers.</span></span> <span data-ttu-id="3eaa3-153">Wenn Sie alle Programme auf einmal ausführen möchten, wählen Sie mindestens ein Programm aus, und klicken Sie dann auf **alle ausführen**.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-153">To run all the programs at one time, select at least one program, and then click **Run All**.</span></span> <span data-ttu-id="3eaa3-154">Wenn Sie bestimmte Programme ausführen möchten, wählen Sie das Programm oder die Programme aus, und klicken Sie dann auf **ausgewählt ausführen**.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-154">To run specific programs, select the program or programs, and then click **Run Selected**.</span></span> <span data-ttu-id="3eaa3-155">Führen Sie die erforderlichen Konfigurationsaufgaben aus, und schließen Sie dann die Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-155">Complete the required configuration tasks and then close the applications.</span></span> <span data-ttu-id="3eaa3-156">Möglicherweise müssen Sie einige Minuten warten, bis alle Programme ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-156">You may need to wait several minutes for all programs to run.</span></span>

   **<span data-ttu-id="3eaa3-157">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="3eaa3-157">Note</span></span>**  
   <span data-ttu-id="3eaa3-158">Wenn Sie Aufgaben der ersten Verwendung für eine Anwendung ausführen möchten, die in der Liste nicht zur Verfügung steht, öffnen Sie die Anwendung.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-158">To run first-use tasks for any application that is not available in the list, open the application.</span></span> <span data-ttu-id="3eaa3-159">Die zugehörigen Informationen werden in diesem Schritt erfasst.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-159">The associated information will be captured during this step.</span></span>



~~~
Click **Next**.
~~~

10. <span data-ttu-id="3eaa3-160">Auf der Seite " **Installationsbericht** " können Sie Informationen zum virtualisierten Anwendungspaket, das Sie gerade sequenziert haben, überprüfen.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-160">On the **Installation Report** page, you can review information about the virtualized application package you have just sequenced.</span></span> <span data-ttu-id="3eaa3-161">Doppelklicken Sie in **zusätzlichen Informationen**auf ein Ereignis, um detailliertere Informationen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-161">In **Additional Information**, double-click an event to obtain more detailed information.</span></span> <span data-ttu-id="3eaa3-162">Klicken Sie auf **weiter**, um fortzufahren.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-162">To proceed, click **Next**.</span></span>

11. <span data-ttu-id="3eaa3-163">Die Seite " **Anpassen** " wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-163">The **Customize** page is displayed.</span></span> <span data-ttu-id="3eaa3-164">Wenn Sie die Installation und Konfiguration der virtuellen Anwendung abgeschlossen haben, wählen Sie **jetzt beenden** aus, und fahren Sie mit Schritt 14 dieses Verfahrens fort.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-164">If you are finished installing and configuring the virtual application, select **Stop now** and skip to step 14 of this procedure.</span></span> <span data-ttu-id="3eaa3-165">Wenn Sie eine der folgenden Anpassungen ausführen möchten, wählen Sie **Anpassen**aus.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-165">To perform either of the following customizations, select **Customize**.</span></span>

    -   <span data-ttu-id="3eaa3-166">Vorbereiten des virtuellen Pakets für Streaming.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-166">Prepare the virtual package for streaming.</span></span> <span data-ttu-id="3eaa3-167">Durch Streaming wird die Benutzerfreundlichkeit verbessert, wenn das virtuelle Anwendungspaket auf Zielcomputern ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-167">Streaming improves the experience when the virtual application package is run on target computers.</span></span>

    -   <span data-ttu-id="3eaa3-168">Geben Sie die Betriebssysteme an, die dieses Paket ausführen können.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-168">Specify the operating systems that can run this package.</span></span>

    <span data-ttu-id="3eaa3-169">Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-169">Click **Next**.</span></span>

12. <span data-ttu-id="3eaa3-170">Führen Sie auf der Seite " **Streaming** " jedes Programm so aus, dass es optimiert und effizienter auf Zielcomputern ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-170">On the **Streaming** page, run each program so that it can be optimized and run more efficiently on target computers.</span></span> <span data-ttu-id="3eaa3-171">Es kann mehrere Minuten dauern, bis alle Anwendungen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-171">It can take several minutes for all the applications to run.</span></span> <span data-ttu-id="3eaa3-172">Schließen Sie alle Anwendungen, nachdem alle Anwendungen ausgeführt wurden, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-172">After all applications have run, close each of the applications, and then click **Next**.</span></span>

   **<span data-ttu-id="3eaa3-173">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="3eaa3-173">Note</span></span>**  
   <span data-ttu-id="3eaa3-174">Wenn Sie während dieses Schritts keine Anwendungen öffnen, ist die standardmäßige Streaming-Methode eine bedarfsgesteuerte Streaming-Übermittlung.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-174">If you do not open any applications during this step, the default streaming method is on-demand streaming delivery.</span></span> <span data-ttu-id="3eaa3-175">Das bedeutet, dass Anwendungen nach und nach heruntergeladen werden, bis Sie geöffnet werden können, und je nachdem, wie das Laden des Hintergrunds konfiguriert wird, wird die restliche Anwendung geladen.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-175">This means applications will be downloaded bit by bit until it can be opened, and then depending on how the background loading is configured, will load the rest of the application.</span></span>



13. <span data-ttu-id="3eaa3-176">Geben Sie auf der Seite **Zielbetriebssystem** die Betriebssysteme an, mit denen dieses Paket ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-176">On the **Target OS** page, specify the operating systems that can run this package.</span></span> <span data-ttu-id="3eaa3-177">Wenn Sie zulassen möchten, dass alle unterstützten Betriebssysteme in Ihrer Umgebung dieses Paket ausführen können, wählen Sie zulassen, dass **Dieses Paket unter einem beliebigen Betriebssystem ausgeführt**wird.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-177">To allow all supported operating systems in your environment to run this package, select **Allow this package to run on any operating system**.</span></span> <span data-ttu-id="3eaa3-178">Wenn Sie dieses Paket so konfigurieren möchten, dass es nur auf bestimmten Betriebssystemen ausgeführt wird, wählen Sie zulassen, dass **Dieses Paket nur unter den folgenden Betriebssystemen ausgeführt** wird, und wählen Sie die Betriebssysteme aus, die dieses Paket ausführen können.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-178">To configure this package to run only on specific operating systems, select **Allow this package to run only on the following operating systems** and select the operating systems that can run this package.</span></span> <span data-ttu-id="3eaa3-179">Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-179">Click **Next**.</span></span>

   **<span data-ttu-id="3eaa3-180">Wichtig</span><span class="sxs-lookup"><span data-stu-id="3eaa3-180">Important</span></span>**  
   <span data-ttu-id="3eaa3-181">Stellen Sie sicher, dass die hier angegebenen Betriebssysteme von der Anwendung unterstützt werden, die Sie sequenzieren.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-181">Make sure that the operating systems you specify here are supported by the application you are sequencing.</span></span>



14. <span data-ttu-id="3eaa3-182">Die Seite **Paket erstellen** wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-182">The **Create Package** page is displayed.</span></span> <span data-ttu-id="3eaa3-183">Wenn Sie das Paket ändern möchten, ohne es zu speichern, wählen Sie weiter aus, um das Paket **ohne Speichern mit dem Paket-Editor zu ändern**.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-183">To modify the package without saving it, select **Continue to modify package without saving using the package editor**.</span></span> <span data-ttu-id="3eaa3-184">Mit dieser Option wird das Paket in der Sequencer-Konsole geöffnet, sodass Sie das Paket vor dem Speichern ändern können.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-184">This option opens the package in the sequencer console so that you can modify the package before it is saved.</span></span> <span data-ttu-id="3eaa3-185">Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-185">Click **Next**.</span></span>

   <span data-ttu-id="3eaa3-186">Wenn Sie das Paket sofort speichern möchten, wählen Sie **das Paket jetzt speichern** (Standard) aus.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-186">To save the package immediately, select **Save the package now** (default).</span></span> <span data-ttu-id="3eaa3-187">Fügen Sie optionale **Kommentare** hinzu, die dem Paket zugeordnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-187">Add optional **Comments** to be associated with the package.</span></span> <span data-ttu-id="3eaa3-188">Kommentare sind hilfreich, um die Programmversion und weitere Informationen zum Paket zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-188">Comments are useful for identifying the program version and other information about the package.</span></span>

   **<span data-ttu-id="3eaa3-189">Wichtig</span><span class="sxs-lookup"><span data-stu-id="3eaa3-189">Important</span></span>**  
   <span data-ttu-id="3eaa3-190">Das System unterstützt keine nicht druckbaren Zeichen in **Kommentaren** und **Beschreibungen**.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-190">The system does not support non-printable characters in **Comments** and **Descriptions**.</span></span>



~~~
The default **Save Location** is also displayed on this page. To change the default location, click **Browse** and specify the new location. Click **Create**.
~~~

15. <span data-ttu-id="3eaa3-191">Die Seite **Fertigstellung** wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-191">The **Completion** page is displayed.</span></span> <span data-ttu-id="3eaa3-192">Überprüfen Sie die Informationen im Bereich **Bericht des virtuellen Anwendungspakets** nach Bedarf, und klicken Sie dann auf **Schließen**.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-192">Review the information in the **Virtual Application Package Report** pane as needed, then click **Close**.</span></span> <span data-ttu-id="3eaa3-193">Diese Informationen sind auch in der **Report.xml** -Datei verfügbar, die sich in dem Verzeichnis befindet, in dem das Paket erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-193">This information is also available in the **Report.xml** file that is located in the directory where the package was created.</span></span>

   <span data-ttu-id="3eaa3-194">Das Paket steht jetzt im Sequencer zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-194">The package is now available in the sequencer.</span></span>

   **<span data-ttu-id="3eaa3-195">Wichtig</span><span class="sxs-lookup"><span data-stu-id="3eaa3-195">Important</span></span>**  
   <span data-ttu-id="3eaa3-196">Nachdem Sie ein virtuelles Anwendungspaket erfolgreich erstellt haben, können Sie das virtuelle Anwendungspaket nicht auf dem Computer ausführen, auf dem der Sequencer ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-196">After you have successfully created a virtual application package, you cannot run the virtual application package on the computer that is running the sequencer.</span></span>



**<span data-ttu-id="3eaa3-197">So Sequenzieren Sie eine Add-on-oder Plug-in-Anwendung</span><span class="sxs-lookup"><span data-stu-id="3eaa3-197">To sequence an add-on or plug-in application</span></span>**

1.  

    **<span data-ttu-id="3eaa3-198">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="3eaa3-198">Note</span></span>**  
    <span data-ttu-id="3eaa3-199">Bevor Sie das folgende Verfahren ausführen, installieren Sie die übergeordnete Anwendung lokal auf dem Computer, auf dem der Sequencer ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-199">Before performing the following procedure, install the parent application locally on the computer that is running the sequencer.</span></span> <span data-ttu-id="3eaa3-200">Wenn Sie die übergeordnete Anwendung virtualisiert haben, können Sie die Schritte im Add-on-oder Plug-in-Workflow ausführen, um die übergeordnete Anwendung auf dem Computer zu entpacken.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-200">Or if you have the parent application virtualized, you can follow the steps in the add-on or plug-in workflow to unpack the parent application on the computer.</span></span>

    <span data-ttu-id="3eaa3-201">Wenn Sie beispielsweise ein Plug-in für Microsoft Excel sequenzieren, installieren Sie Microsoft Excel lokal auf dem Computer, auf dem der Sequencer ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-201">For example, if you are sequencing a plug-in for Microsoft Excel, install Microsoft Excel locally on the computer that is running the sequencer.</span></span> <span data-ttu-id="3eaa3-202">Installieren Sie die übergeordnete Anwendung auch im gleichen Verzeichnis, in dem die Anwendung auf den Zielcomputern installiert ist.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-202">Also install the parent application in the same directory where the application is installed on target computers.</span></span> <span data-ttu-id="3eaa3-203">Wenn das Plug-in oder Add-on mit einem vorhandenen virtuellen Anwendungspaket verwendet werden soll, installieren Sie die Anwendung auf dem virtuellen Anwendungs Laufwerk, das beim Erstellen des übergeordneten virtuellen Anwendungspakets verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-203">If the plug-in or add-on is going to be used with an existing virtual application package, install the application on the same virtual application drive that was used when you created the parent virtual application package.</span></span>



~~~
On the computer that runs the sequencer, click **All Programs**, and then Click **Microsoft Application Virtualization**, and then click **Microsoft Application Virtualization Sequencer**.
~~~

2. <span data-ttu-id="3eaa3-204">\*<strong><em>Klicken Sie im Sequencer auf \* </em> Neues virtuelles Anwendungspaket erstellen </strong> .</span><span class="sxs-lookup"><span data-stu-id="3eaa3-204">\*<strong><em>In the sequencer, click \*</em>Create a New Virtual Application Package</strong>.</span></span> <span data-ttu-id="3eaa3-205">Wählen Sie **Paket erstellen (Standard)** aus, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-205">Select **Create Package (default)**, and then click **Next**.</span></span>

3. <span data-ttu-id="3eaa3-206">Überprüfen Sie auf der Seite **Computer vorbereiten** die Probleme, die möglicherweise dazu führen, dass die Paketerstellung fehlschlägt oder dass das Paket unnötige Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-206">On the **Prepare Computer** page, review the issues that might cause the package creation to fail or could cause the package to contain unnecessary data.</span></span> <span data-ttu-id="3eaa3-207">Sie sollten alle potenziellen Probleme beheben, bevor Sie fortfahren.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-207">You should resolve all potential issues before you continue.</span></span> <span data-ttu-id="3eaa3-208">Nachdem Sie Korrekturen vorgenommen haben, klicken Sie auf **Aktualisieren** , um die aktualisierten Informationen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-208">After making any corrections, click **Refresh** to display the updated information.</span></span> <span data-ttu-id="3eaa3-209">Nachdem Sie alle potenziellen Probleme behoben haben, klicken Sie auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-209">After you have resolved all potential issues, click **Next**.</span></span>

   **<span data-ttu-id="3eaa3-210">Wichtig</span><span class="sxs-lookup"><span data-stu-id="3eaa3-210">Important</span></span>**  
   <span data-ttu-id="3eaa3-211">Wenn Sie die Virenscansoftware deaktivieren müssen, sollten Sie zuerst den Computer scannen, auf dem der Sequencer ausgeführt wird, um sicherzustellen, dass dem Paket keine unerwünschten oder böswilligen Dateien hinzugefügt werden können.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-211">If you are required to disable virus scanning software, you should first scan the computer that runs the sequencer in order to ensure that no unwanted or malicious files could be added to the package.</span></span>



4. <span data-ttu-id="3eaa3-212">Wählen Sie auf der Seite **Art der Anwendung** **Add-on oder Plug-in**aus, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-212">On the **Type of Application** page, select **Add-on or Plug-in**, and then click **Next**.</span></span>

5. <span data-ttu-id="3eaa3-213">Klicken Sie auf der Seite **Installationsprogramm auswählen** auf **Durchsuchen** , und geben Sie die Installationsdatei für das Add-on oder das Plug-in an.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-213">On the **Select Installer** page, click **Browse** and specify the installation file for the add-on or plug-in.</span></span> <span data-ttu-id="3eaa3-214">Wenn das Add-on oder Plug-in keine zugeordnete Installationsdatei enthält und Sie alle Installationsschritte manuell ausführen möchten, aktivieren Sie das Kontrollkästchen **diese Option zum Durchführen einer benutzerdefinierten Installation auswählen** , und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-214">If the add-on or plug-in does not have an associated installer file and you plan to run all installation steps manually, select the **Select this option to perform a custom installation** check box, and then click **Next**.</span></span>

6. <span data-ttu-id="3eaa3-215">Stellen Sie auf der Seite **primäre Installation** sicher, dass die primäre Anwendung auf dem Computer installiert ist, auf dem der Sequencer ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-215">On the **Install Primary** page, ensure that the primary application is installed on the computer that runs the sequencer.</span></span> <span data-ttu-id="3eaa3-216">Alternativ können Sie ein vorhandenes Paket erweitern, das lokal auf dem Computer gespeichert wurde, auf dem der Sequencer ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-216">Alternatively, you can expand an existing package that has been saved locally on the computer that runs the sequencer.</span></span> <span data-ttu-id="3eaa3-217">Klicken Sie dazu auf **Paket erweitern**, und wählen Sie dann das Paket aus.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-217">To do this, click **Expand Package**, and then select the package.</span></span> <span data-ttu-id="3eaa3-218">Nachdem Sie das übergeordnete Programm erweitert oder installiert haben, wählen Sie **Ich habe das primäre übergeordnete Programm installiert**aus.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-218">After you have expanded or installed the parent program, select **I have installed the primary parent program**.</span></span>

   <span data-ttu-id="3eaa3-219">Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-219">Click **Next**.</span></span>

7. <span data-ttu-id="3eaa3-220">Geben Sie auf der Seite **Package Name** einen Namen ein, der dem Paket zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-220">On the **Package Name** page, type a name that will be associated with the package.</span></span> <span data-ttu-id="3eaa3-221">Verwenden Sie einen Namen, der hilft, den Zweck und die Version der Anwendung zu identifizieren, die dem Paket hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-221">Use a name that helps identify the purpose and version of the application that will be added to the package.</span></span> <span data-ttu-id="3eaa3-222">Der Paket Name wird in der App-V 5,0-Verwaltungskonsole angezeigt.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-222">The package name will be displayed in the App-V 5.0 Management Console.</span></span> <span data-ttu-id="3eaa3-223">Das **primäre virtuelle Anwendungsverzeichnis** zeigt den Pfad an, in dem die Anwendung installiert wird.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-223">The **Primary Virtual Application Directory** displays the path where the application will be installed.</span></span> <span data-ttu-id="3eaa3-224">Wenn Sie diesen Speicherort angeben möchten, geben Sie den Pfad ein, oder klicken Sie auf **Durchsuchen**.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-224">To specify this location, type the path, or click **Browse**.</span></span>

   **<span data-ttu-id="3eaa3-225">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="3eaa3-225">Note</span></span>**  
   <span data-ttu-id="3eaa3-226">Ab App-V 5,0 SP3 ist das primäre Virtual Application Directory (PVAD) ausgeblendet, Sie können es aber wieder aktivieren.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-226">Starting in App-V 5.0 SP3, the primary virtual application directory (PVAD) is hidden, but you can turn it back on.</span></span> <span data-ttu-id="3eaa3-227">Informationen finden Sie unter [App-V 5,0 SP3](about-app-v-50-sp3.md#bkmk-pvad-hidden).</span><span class="sxs-lookup"><span data-stu-id="3eaa3-227">See [About App-V 5.0 SP3](about-app-v-50-sp3.md#bkmk-pvad-hidden).</span></span>



~~~
Click **Next**.
~~~

8. <span data-ttu-id="3eaa3-228">Wenn der Sequencer und das Anwendungs Installationsprogramm bereit sind, können Sie auf der **Installations** Seite mit der Installation des Plug-ins oder der Add-in-Anwendung fortfahren, damit der Sequencer den Installationsvorgang überwachen kann.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-228">On the **Installation** page, when the sequencer and application installer are ready you can proceed to install the plug-in or add-in application so the sequencer can monitor the installation process.</span></span> <span data-ttu-id="3eaa3-229">Verwenden Sie den Installationsprozess der Anwendung, um die Installation durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-229">Use the application's installation process to perform the installation.</span></span> <span data-ttu-id="3eaa3-230">Wenn zusätzliche Installationsdateien als Teil der Installation ausgeführt werden müssen, klicken Sie auf **Ausführen** , und führen Sie die zusätzlichen Installationsdateien aus.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-230">If additional installation files must be run as part of the installation, click **Run** and locate and run the additional installation files.</span></span> <span data-ttu-id="3eaa3-231">Wenn Sie die Installation abgeschlossen haben, wählen Sie **Ich habe die Installation abgeschlossen**aus, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-231">When you are finished with the installation, select **I am finished installing**, and then click **Next**.</span></span>

9. <span data-ttu-id="3eaa3-232">Auf der Seite **Installationsbericht** können Sie Informationen zu dem soeben sequenzierten virtuellen Anwendungspaket überprüfen.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-232">On the **Installation Report** page, you can review information about the virtual application package that you just sequenced.</span></span> <span data-ttu-id="3eaa3-233">Eine detailliertere Erläuterung der Informationen, die in **zusätzlichen Informationen**angezeigt werden, finden Sie, indem Sie auf das Ereignis doppelklicken.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-233">For a more detailed explanation about the information displayed in **Additional Information**, double-click the event.</span></span> <span data-ttu-id="3eaa3-234">Nachdem Sie die Informationen überprüft haben, klicken Sie auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-234">After you have reviewed the information, click **Next**.</span></span>

10. <span data-ttu-id="3eaa3-235">Die Seite " **Anpassen** " wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-235">The **Customize** page is displayed.</span></span> <span data-ttu-id="3eaa3-236">Wenn Sie die Installation und Konfiguration der virtuellen Anwendung abgeschlossen haben, wählen Sie **jetzt beenden** aus, und fahren Sie mit Schritt 12 dieses Verfahrens fort.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-236">If you are finished installing and configuring the virtual application, select **Stop now** and skip to step 12 of this procedure.</span></span> <span data-ttu-id="3eaa3-237">Wenn Sie eine der folgenden Anpassungen ausführen möchten, wählen Sie **Anpassen**aus.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-237">To perform either of the following customizations, select **Customize**.</span></span>

    -   <span data-ttu-id="3eaa3-238">Optimieren Sie, wie das Paket in einem langsamen oder unzuverlässigen Netzwerk ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-238">Optimize how the package will run across a slow or unreliable network.</span></span>

    -   <span data-ttu-id="3eaa3-239">Geben Sie die Betriebssysteme an, die dieses Paket ausführen können.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-239">Specify the operating systems that can run this package.</span></span>

    <span data-ttu-id="3eaa3-240">Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-240">Click **Next**.</span></span>

11. <span data-ttu-id="3eaa3-241">Führen Sie auf der Seite " **Streaming** " jedes Programm so aus, dass es optimiert und effizienter auf Zielcomputern ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-241">On the **Streaming** page, run each program so that it can be optimized and run more efficiently on target computers.</span></span> <span data-ttu-id="3eaa3-242">Durch Streaming wird die Erfahrung verbessert, wenn das virtuelle Anwendungspaket auf Zielcomputern in Netzwerken mit hoher Latenz ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-242">Streaming improves the experience when the virtual application package is run on target computers on high-latency networks.</span></span> <span data-ttu-id="3eaa3-243">Es kann mehrere Minuten dauern, bis alle Anwendungen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-243">It can take several minutes for all the applications to run.</span></span> <span data-ttu-id="3eaa3-244">Schließen Sie alle Anwendungen, nachdem alle Anwendungen ausgeführt wurden.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-244">After all applications have run, close each of the applications.</span></span> <span data-ttu-id="3eaa3-245">Sie können das Paket auch so konfigurieren, dass es vor dem Öffnen vollständig heruntergeladen werden muss, indem Sie das Kontrollkästchen **zu herunterzuladende Anwendungen erzwingen** auswählen.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-245">You can also configure the package to be required to be fully downloaded before opening by selecting the **Force applications to be downloaded** check-box.</span></span> <span data-ttu-id="3eaa3-246">Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-246">Click **Next**.</span></span>

   **<span data-ttu-id="3eaa3-247">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="3eaa3-247">Note</span></span>**  
   <span data-ttu-id="3eaa3-248">Falls erforderlich, können Sie verhindern, dass eine Anwendung während dieses Schritts geladen wird.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-248">If necessary, you can stop an application from loading during this step.</span></span> <span data-ttu-id="3eaa3-249">Klicken Sie im Dialogfeld **Anwendungsstart** auf **Beenden** , und aktivieren Sie eines der Kontrollkästchen: **alle Anwendungen beenden** oder **nur diese Anwendung beenden**.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-249">In the **Application Launch** dialog box, click **Stop** and select one of the check boxes: **Stop all applications** or **Stop this application only**.</span></span>



12. <span data-ttu-id="3eaa3-250">Geben Sie auf der Seite **Zielbetriebssystem** die Betriebssysteme an, mit denen dieses Paket ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-250">On the **Target OS** page, specify the operating systems that can run this package.</span></span> <span data-ttu-id="3eaa3-251">Wenn Sie zulassen möchten, dass alle unterstützten Betriebssysteme in Ihrer Umgebung dieses Paket ausführen können, aktivieren Sie das Kontrollkästchen **Dieses Paket kann auf einem beliebigen Betriebssystem ausgeführt** werden.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-251">To allow all supported operating systems in your environment to run this package, select the **Allow this package to run on any operating system** check box.</span></span> <span data-ttu-id="3eaa3-252">Um dieses Paket so zu konfigurieren, dass es nur auf bestimmten Betriebssystemen ausgeführt wird, aktivieren Sie das Kontrollkästchen **Dieses Paket nur auf den folgenden Betriebssystemen ausführen lassen** , und wählen Sie dann die Betriebssysteme aus, die dieses Paket ausführen können.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-252">To configure this package to run only on specific operating systems, select the **Allow this package to run only on the following operating systems** check box, and then select the operating systems that can run this package.</span></span> <span data-ttu-id="3eaa3-253">Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-253">Click **Next**.</span></span>

13. <span data-ttu-id="3eaa3-254">Die Seite **Paket erstellen** wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-254">The **Create Package** page is displayed.</span></span> <span data-ttu-id="3eaa3-255">Wenn Sie das Paket ändern möchten, ohne es zu speichern, wählen Sie weiter aus, um das Paket **ohne Speichern über das Kontrollkästchen Paket-Editor zu ändern** .</span><span class="sxs-lookup"><span data-stu-id="3eaa3-255">To modify the package without saving it, select **Continue to modify package without saving using the package editor** check box.</span></span> <span data-ttu-id="3eaa3-256">Mit dieser Option wird das Paket in der Sequencer-Konsole geöffnet, sodass Sie das Paket vor dem Speichern ändern können.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-256">This option opens the package in the sequencer console so that you can modify the package before it is saved.</span></span> <span data-ttu-id="3eaa3-257">Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-257">Click **Next**.</span></span>

   <span data-ttu-id="3eaa3-258">Wenn Sie das Paket sofort speichern möchten, wählen Sie **das Paket jetzt speichern**aus.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-258">To save the package immediately, select **Save the package now**.</span></span> <span data-ttu-id="3eaa3-259">Optional können Sie eine **Beschreibung** hinzufügen, die dem Paket zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-259">Optionally, add a **Description** that will be associated with the package.</span></span> <span data-ttu-id="3eaa3-260">Beschreibungen sind hilfreich, um die Version und andere Informationen zum Paket zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-260">Descriptions are useful for identifying the version and other information about the package.</span></span>

   **<span data-ttu-id="3eaa3-261">Wichtig</span><span class="sxs-lookup"><span data-stu-id="3eaa3-261">Important</span></span>**  
   <span data-ttu-id="3eaa3-262">Das System unterstützt keine nicht druckbaren Zeichen in Kommentaren und Beschreibungen.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-262">The system does not support non-printable characters in Comments and Descriptions.</span></span>



~~~
The default **Save Location** is also displayed on this page. To change the default location, click **Browse** and specify the new location. Click **Create**.
~~~

**<span data-ttu-id="3eaa3-263">So Sequenzieren Sie eine Middleware-Anwendung</span><span class="sxs-lookup"><span data-stu-id="3eaa3-263">To sequence a middleware application</span></span>**

1. <span data-ttu-id="3eaa3-264">Klicken Sie auf dem Computer, auf dem der Sequencer ausgeführt wird, auf **Alle Programme**, und klicken Sie dann auf **Microsoft Application Virtualization**, und klicken Sie dann auf **Microsoft Application Virtualization Sequencer**.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-264">On the computer that runs the sequencer, click **All Programs**, and then Click **Microsoft Application Virtualization**, and then click **Microsoft Application Virtualization Sequencer**.</span></span>

2. <span data-ttu-id="3eaa3-265">\*<strong><em>Klicken Sie im Sequencer auf \* </em> Neues virtuelles Anwendungspaket erstellen </strong> .</span><span class="sxs-lookup"><span data-stu-id="3eaa3-265">\*<strong><em>In the sequencer, click \*</em>Create a New Virtual Application Package</strong>.</span></span> <span data-ttu-id="3eaa3-266">Wählen Sie **Paket erstellen (Standard)** aus, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-266">Select **Create Package (default)**, and then click **Next**.</span></span>

3. <span data-ttu-id="3eaa3-267">Überprüfen Sie auf der Seite **Computer vorbereiten** die Probleme, die dazu führen können, dass die Paketerstellung fehlschlägt oder dass das Paket unnötige Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-267">On the **Prepare Computer** page, review the issues that could cause the package creation to fail or could cause the package to contain unnecessary data.</span></span> <span data-ttu-id="3eaa3-268">Sie sollten alle potenziellen Probleme beheben, bevor Sie fortfahren.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-268">You should resolve all potential issues before you continue.</span></span> <span data-ttu-id="3eaa3-269">Nachdem Sie Korrekturen vorgenommen haben, klicken Sie auf **Aktualisieren** , um die aktualisierten Informationen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-269">After making any corrections, click **Refresh** to display the updated information.</span></span> <span data-ttu-id="3eaa3-270">Nachdem Sie alle potenziellen Probleme behoben haben, klicken Sie auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-270">After you have resolved all potential issues, click **Next**.</span></span>

   **<span data-ttu-id="3eaa3-271">Wichtig</span><span class="sxs-lookup"><span data-stu-id="3eaa3-271">Important</span></span>**  
   <span data-ttu-id="3eaa3-272">Wenn Sie die Virenscansoftware deaktivieren müssen, sollten Sie zuerst den Computer scannen, auf dem der App-V 5,0-Sequenzer ausgeführt wird, um sicherzustellen, dass dem Paket keine unerwünschten oder bösartigen Dateien hinzugefügt werden können.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-272">If you are required to disable virus scanning software, you should first scan the computer that runs the App-V 5.0 Sequencer in order to ensure that no unwanted or malicious files can be added to the package.</span></span>



4. <span data-ttu-id="3eaa3-273">Wählen Sie auf der Seite **Art der Anwendung** **Middleware**aus, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-273">On the **Type of Application** page, select **Middleware**, and then click **Next**.</span></span>

5. <span data-ttu-id="3eaa3-274">Klicken Sie auf der Seite **Installationsprogramm auswählen** auf **Durchsuchen** , und geben Sie die Installationsdatei für die Anwendung an.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-274">On the **Select Installer** page, click **Browse** and specify the installation file for the application.</span></span> <span data-ttu-id="3eaa3-275">Wenn die Anwendung keine zugeordnete Installationsdatei hat und Sie alle Installationsschritte manuell ausführen möchten, aktivieren Sie das Kontrollkästchen **diese Option zum Durchführen einer benutzerdefinierten Installation auswählen** , und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-275">If the application does not have an associated installer file and you plan to run all installation steps manually, select the **Select this option to perform a custom installation** check box, and then click **Next**.</span></span>

6. <span data-ttu-id="3eaa3-276">Geben Sie auf der Seite **Package Name** einen Namen ein, der dem Paket zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-276">On the **Package Name** page, type a name that will be associated with the package.</span></span> <span data-ttu-id="3eaa3-277">Verwenden Sie einen Namen, der hilft, den Zweck und die Version der Anwendung zu identifizieren, die dem Paket hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-277">Use a name that helps identify the purpose and version of the application that will be added to the package.</span></span> <span data-ttu-id="3eaa3-278">Der Paket Name wird in der App-V 5,0-Verwaltungskonsole angezeigt.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-278">The package name is displayed in the App-V 5.0 Management Console.</span></span> <span data-ttu-id="3eaa3-279">Das **primäre virtuelle Anwendungsverzeichnis** zeigt den Pfad an, in dem die Anwendung installiert wird.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-279">The **Primary Virtual Application Directory** displays the path where the application will be installed.</span></span> <span data-ttu-id="3eaa3-280">Wenn Sie diesen Speicherort angeben möchten, geben Sie den Pfad ein, oder klicken Sie auf **Durchsuchen**.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-280">To specify this location, type the path or click **Browse**.</span></span>

   <span data-ttu-id="3eaa3-281">Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-281">Click **Next**.</span></span>

7. <span data-ttu-id="3eaa3-282">Wenn das Installationsprogramm für Sequencer und Middleware bereit ist, können Sie auf der **Installations** Seite fortfahren, die Anwendung zu installieren, damit der Sequencer den Installationsvorgang überwachen kann.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-282">On the **Installation** page, when the sequencer and middleware application installer are ready you can proceed to install the application so that the sequencer can monitor the installation process.</span></span> <span data-ttu-id="3eaa3-283">Verwenden Sie den Installationsprozess der Anwendung, um die Installation durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-283">Use the application's installation process to perform the installation.</span></span> <span data-ttu-id="3eaa3-284">Wenn zusätzliche Installationsdateien als Teil der Installation ausgeführt werden müssen, klicken Sie auf **Ausführen**, um die zusätzlichen Installationsdateien zu suchen und auszuführen.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-284">If additional installation files must be run as part of the installation, click **Run**, to locate and run the additional installation files.</span></span> <span data-ttu-id="3eaa3-285">Wenn Sie die Installation abgeschlossen haben, aktivieren Sie das Kontrollkästchen **Ich habe die Installation abgeschlossen** , und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-285">When you are finished with the installation, select the **I am finished installing** check box, and then click **Next**.</span></span>

8. <span data-ttu-id="3eaa3-286">Warten Sie auf der **Installations** Seite, während der Sequencer das virtuelle Anwendungspaket konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-286">On the **Installation** page, wait while the sequencer configures the virtual application package.</span></span>

9. <span data-ttu-id="3eaa3-287">Auf der Seite **Installationsbericht** können Sie Informationen zu dem soeben sequenzierten virtuellen Anwendungspaket überprüfen.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-287">On the **Installation Report** page, you can review information about the virtual application package that you have just sequenced.</span></span> <span data-ttu-id="3eaa3-288">Doppelklicken Sie in **zusätzlichen Informationen**auf ein Ereignis, um detailliertere Informationen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-288">In **Additional Information**, double-click an event to obtain more detailed information.</span></span> <span data-ttu-id="3eaa3-289">Klicken Sie auf **weiter**, um fortzufahren.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-289">To proceed, click **Next**.</span></span>

10. <span data-ttu-id="3eaa3-290">Geben Sie auf der Seite **Zielbetriebssystem** die Betriebssysteme an, mit denen dieses Paket ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-290">On the **Target OS** page, specify the operating systems that can run this package.</span></span> <span data-ttu-id="3eaa3-291">Wenn Sie alle unterstützten Betriebssysteme in Ihrer Umgebung zum Ausführen dieses Pakets aktivieren möchten, aktivieren Sie das Kontrollkästchen **Dieses Paket kann auf einem beliebigen Betriebssystem ausgeführt** werden.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-291">To enable all supported operating systems in your environment to run this package, select the **Allow this package to run on any operating system** check box.</span></span> <span data-ttu-id="3eaa3-292">Wenn Sie dieses Paket so konfigurieren möchten, dass es nur auf bestimmten Betriebssystemen ausgeführt wird, aktivieren Sie das Kontrollkästchen **Dieses Paket darf nur auf dem folgenden Betriebssystem ausgeführt** werden, und wählen Sie die Betriebssysteme aus, mit denen dieses Paket ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-292">To configure this package to run only on specific operating systems, select the **Allow this package to run only on the following operating systems** check box and select the operating systems that can run this package.</span></span> <span data-ttu-id="3eaa3-293">Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-293">Click **Next**.</span></span>

11. <span data-ttu-id="3eaa3-294">Auf der Seite **Paket erstellen** wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-294">On the **Create Package** page is displayed.</span></span> <span data-ttu-id="3eaa3-295">Wenn Sie das Paket ändern möchten, ohne es zu speichern, wählen Sie weiter aus, um das Paket **ohne Speichern mit dem Paket-Editor zu ändern**.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-295">To modify the package without saving it, select **Continue to modify package without saving using the package editor**.</span></span> <span data-ttu-id="3eaa3-296">Mit dieser Option wird das Paket in der Sequencer-Konsole geöffnet, sodass Sie das Paket vor dem Speichern ändern können.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-296">This option opens the package in the sequencer console so that you can modify the package before it is saved.</span></span> <span data-ttu-id="3eaa3-297">Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-297">Click **Next**.</span></span>

    <span data-ttu-id="3eaa3-298">Wenn Sie das Paket sofort speichern möchten, wählen Sie **das Paket jetzt speichern**aus.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-298">To save the package immediately, select **Save the package now**.</span></span> <span data-ttu-id="3eaa3-299">Optional können Sie eine **Beschreibung** hinzufügen, die dem Paket zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-299">Optionally, add a **Description** to be associated with the package.</span></span> <span data-ttu-id="3eaa3-300">Beschreibungen sind hilfreich, um die Programmversion und weitere Informationen über das Paket zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-300">Descriptions are useful for identifying the program version and other information about the package.</span></span>

    **<span data-ttu-id="3eaa3-301">Wichtig</span><span class="sxs-lookup"><span data-stu-id="3eaa3-301">Important</span></span>**  
    <span data-ttu-id="3eaa3-302">Das System unterstützt keine nicht druckbaren Zeichen in Kommentaren und Beschreibungen.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-302">The system does not support non-printable characters in Comments and Descriptions.</span></span>



~~~
The default **Save Location** is also displayed on this page. To change the default location, click **Browse** and specify the new location. Click **Create**.
~~~

12. <span data-ttu-id="3eaa3-303">Die Seite **Fertigstellung** wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-303">The **Completion** page is displayed.</span></span> <span data-ttu-id="3eaa3-304">Überprüfen Sie die Informationen im Bereich **Bericht des virtuellen Anwendungspakets** nach Bedarf, und klicken Sie dann auf **Schließen**.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-304">Review the information in the **Virtual Application Package Report** pane as needed, then click **Close**.</span></span> <span data-ttu-id="3eaa3-305">Diese Informationen sind auch in der **Report.xml** -Datei verfügbar, die sich in dem in Schritt 11 dieses Verfahrens angegebenen Verzeichnis befindet.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-305">This information is also available in the **Report.xml** file that is located in the directory specified in step 11 of this procedure.</span></span>

   <span data-ttu-id="3eaa3-306">Das Paket steht jetzt im Sequencer zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-306">The package is now available in the sequencer.</span></span> <span data-ttu-id="3eaa3-307">Um die Paketeigenschaften zu bearbeiten, klicken Sie auf **Bearbeiten \ [Package Name \]**.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-307">To edit the package properties, click **Edit \[Package Name\]**.</span></span>

   **<span data-ttu-id="3eaa3-308">Wichtig</span><span class="sxs-lookup"><span data-stu-id="3eaa3-308">Important</span></span>**  
   <span data-ttu-id="3eaa3-309">Nachdem Sie ein virtuelles Anwendungspaket erfolgreich erstellt haben, können Sie das virtuelle Anwendungspaket nicht auf dem Computer ausführen, auf dem der Sequencer ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3eaa3-309">After you have successfully created a virtual application package, you cannot run the virtual application package on the computer that is running the sequencer.</span></span>



~~~
**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## <span data-ttu-id="3eaa3-310">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="3eaa3-310">Related topics</span></span>


[<span data-ttu-id="3eaa3-311">Vorgänge für App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="3eaa3-311">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)









