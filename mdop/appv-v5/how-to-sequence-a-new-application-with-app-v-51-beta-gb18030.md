---
title: So sequenzieren Sie eine neue Anwendung mit App-V 5.1
description: So sequenzieren Sie eine neue Anwendung mit App-V 5.1
author: dansimp
ms.assetid: 7d7699b1-0cb8-450d-94e7-5af937e16c21
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 43edd9357e31f4884ed7baec3d35fa01bf2abe54
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805186"
---
# <span data-ttu-id="5e29d-103">So sequenzieren Sie eine neue Anwendung mit App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="5e29d-103">How to Sequence a New Application with App-V 5.1</span></span>


**<span data-ttu-id="5e29d-104">Zu überprüfen oder zu tun, bevor Sie mit der Sequenzierung beginnen</span><span class="sxs-lookup"><span data-stu-id="5e29d-104">To review or do before you start sequencing</span></span>**

1.  <span data-ttu-id="5e29d-105">Ermitteln Sie den Typ des virtualisierten Anwendungspakets, das Sie erstellen möchten:</span><span class="sxs-lookup"><span data-stu-id="5e29d-105">Determine the type of virtualized application package you want to create:</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="5e29d-106">Anwendungstyp</span><span class="sxs-lookup"><span data-stu-id="5e29d-106">Application type</span></span></th>
    <th align="left"><span data-ttu-id="5e29d-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5e29d-107">Description</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="5e29d-108">Standard</span><span class="sxs-lookup"><span data-stu-id="5e29d-108">Standard</span></span></p></td>
    <td align="left"><p><span data-ttu-id="5e29d-109">Erstellt ein Paket, das eine Anwendung oder eine Suite von Anwendungen enthält.</span><span class="sxs-lookup"><span data-stu-id="5e29d-109">Creates a package that contains an application or a suite of applications.</span></span> <span data-ttu-id="5e29d-110">Dies ist die bevorzugte Option für die meisten Anwendungstypen.</span><span class="sxs-lookup"><span data-stu-id="5e29d-110">This is the preferred option for most application types.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="5e29d-111">Add-on oder Plug-in</span><span class="sxs-lookup"><span data-stu-id="5e29d-111">Add-on or plug-in</span></span></p></td>
    <td align="left"><p><span data-ttu-id="5e29d-112">Erstellt ein Paket, das die Funktionalität einer Standardanwendung erweitert, beispielsweise ein Plug-in für Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="5e29d-112">Creates a package that extends the functionality of a standard application, for example, a plug-in for Microsoft Excel.</span></span> <span data-ttu-id="5e29d-113">Darüber hinaus können Sie Plug-Ins für nativ installierte Anwendungen oder ein anderes Paket verwenden, das mithilfe von Verbindungsgruppen verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="5e29d-113">Additionally, you can use plug-ins for natively installed applications, or for another package that is linked by using connection groups.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="5e29d-114">Middleware</span><span class="sxs-lookup"><span data-stu-id="5e29d-114">Middleware</span></span></p></td>
    <td align="left"><p><span data-ttu-id="5e29d-115">Erstellt ein Paket, das für eine Standardanwendung, beispielsweise Java, erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="5e29d-115">Creates a package that is required by a standard application, for example, Java.</span></span> <span data-ttu-id="5e29d-116">Middleware-Pakete werden für Verknüpfungen mit anderen Paketen mithilfe von Verbindungsgruppen verwendet.</span><span class="sxs-lookup"><span data-stu-id="5e29d-116">Middleware packages are used for linking to other packages by using connection groups.</span></span></p></td>
    </tr>
    </tbody>
    </table>



2.  <span data-ttu-id="5e29d-117">Kopieren Sie alle erforderlichen Installationsdateien auf den Computer, auf dem der Sequencer ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5e29d-117">Copy all required installation files to the computer that is running the sequencer.</span></span>

3.  <span data-ttu-id="5e29d-118">Erstellen Sie ein Sicherungsabbild Ihrer virtuellen Umgebung, bevor Sie eine Anwendung sequenzieren, und kehren Sie dann jedes Mal wieder zu diesem Bild zurück, nachdem Sie die Sequenzierung einer Anwendung abgeschlossen haben.</span><span class="sxs-lookup"><span data-stu-id="5e29d-118">Make a backup image of your virtual environment before sequencing an application, and then revert to that image each time after you finish sequencing an application.</span></span>

4.  <span data-ttu-id="5e29d-119">Überprüfen Sie die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="5e29d-119">Review the following items:</span></span>

    -   <span data-ttu-id="5e29d-120">Wenn ein Anwendungs Installationsprogramm den Sicherheitszugriff auf eine neue oder vorhandene Datei oder ein vorhandenes Verzeichnis ändert, werden diese Änderungen nicht im Paket erfasst.</span><span class="sxs-lookup"><span data-stu-id="5e29d-120">If an application installer changes the security access to a new or existing file or directory, those changes are not captured in the package.</span></span>

    -   <span data-ttu-id="5e29d-121">Wenn kurze Pfade für das Zielvolumen des virtualisierten Pakets deaktiviert wurden, müssen Sie das Paket auch auf ein Volume abbilden, das erstellt wurde und bei dem die Short-Pfade deaktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="5e29d-121">If short paths have been disabled for the virtualized package’s target volume, you must also sequence the package to a volume that was created and still has short-paths disabled.</span></span> <span data-ttu-id="5e29d-122">Dies kann nicht das System Volume sein.</span><span class="sxs-lookup"><span data-stu-id="5e29d-122">It cannot be the system volume.</span></span>

> [!NOTE]  
> <span data-ttu-id="5e29d-123">App-V 5. x Sequencer kann keine Anwendungen mit Dateinamen abgleichen, die "CO_ &lt; x &gt; " entsprechen, wobei x eine beliebige Zahl ist.</span><span class="sxs-lookup"><span data-stu-id="5e29d-123">The App-V 5.x Sequencer cannot sequence applications with filenames matching "CO_&lt;x&gt;" where x is any numeral.</span></span> <span data-ttu-id="5e29d-124">Fehler 0x8007139F wird generiert.</span><span class="sxs-lookup"><span data-stu-id="5e29d-124">Error 0x8007139F will be generated.</span></span>

**<span data-ttu-id="5e29d-125">So Sequenzieren Sie eine neue Standardanwendung</span><span class="sxs-lookup"><span data-stu-id="5e29d-125">To sequence a new standard application</span></span>**

1.  <span data-ttu-id="5e29d-126">Klicken Sie auf dem Computer, auf dem der Sequencer ausgeführt wird, auf **Alle Programme**, und klicken Sie dann auf **Microsoft Application Virtualization**, und klicken Sie dann auf **Microsoft Application Virtualization Sequencer**.</span><span class="sxs-lookup"><span data-stu-id="5e29d-126">On the computer that runs the sequencer, click **All Programs**, and then Click **Microsoft Application Virtualization**, and then click **Microsoft Application Virtualization Sequencer**.</span></span>

2.  <span data-ttu-id="5e29d-127">Klicken Sie im Sequencer auf **Neues virtuelles Anwendungspaket erstellen**.</span><span class="sxs-lookup"><span data-stu-id="5e29d-127">In the sequencer, click **Create a New Virtual Application Package**.</span></span> <span data-ttu-id="5e29d-128">Wählen Sie **Paket erstellen (Standard)** aus, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="5e29d-128">Select **Create Package (default)**, and then click **Next**.</span></span>

3.  <span data-ttu-id="5e29d-129">Überprüfen Sie auf der Seite **Computer vorbereiten** die Probleme, die dazu führen können, dass die Paketerstellung fehlschlägt oder dass das Paket unnötige Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="5e29d-129">On the **Prepare Computer** page, review the issues that could cause the package creation to fail or could cause the package to contain unnecessary data.</span></span> <span data-ttu-id="5e29d-130">Sie sollten alle potenziellen Probleme beheben, bevor Sie fortfahren.</span><span class="sxs-lookup"><span data-stu-id="5e29d-130">You should resolve all potential issues before you continue.</span></span> <span data-ttu-id="5e29d-131">Nachdem Sie Korrekturen vorgenommen haben, klicken Sie auf **Aktualisieren** , um die aktualisierten Informationen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="5e29d-131">After making any corrections, click **Refresh** to display the updated information.</span></span> <span data-ttu-id="5e29d-132">Nachdem Sie alle potenziellen Probleme behoben haben, klicken Sie auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="5e29d-132">After you have resolved all potential issues, click **Next**.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="5e29d-133">Wenn Sie die Virenscansoftware deaktivieren müssen, sollten Sie zuerst den Computer scannen, auf dem der Sequencer ausgeführt wird, um sicherzustellen, dass dem Paket keine unerwünschten oder böswilligen Dateien hinzugefügt werden können.</span><span class="sxs-lookup"><span data-stu-id="5e29d-133">If you are required to disable virus scanning software, you should first scan the computer that runs the sequencer in order to ensure that no unwanted or malicious files could be added to the package.</span></span>



~~~
> [!NOTE]  
> There is currently no way to disable Windows Defender in Windows 10. If you receive a warning, you can safely ignore it. It is unlikely that Windows Defender will affect sequencing at all.
~~~



4. <span data-ttu-id="5e29d-134">Klicken Sie auf der Seite **Typ der Anwendung** auf das Kontrollkästchen **Standardanwendung (Standard)** , und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="5e29d-134">On the **Type of Application** page, click the **Standard Application (default)** check box, and then click **Next**.</span></span>

5. <span data-ttu-id="5e29d-135">Klicken Sie auf der Seite **Installationsprogramm auswählen** auf **Durchsuchen** , und geben Sie die Installationsdatei für die Anwendung an.</span><span class="sxs-lookup"><span data-stu-id="5e29d-135">On the **Select Installer** page, click **Browse** and specify the installation file for the application.</span></span>

   > [!NOTE]  
   > <span data-ttu-id="5e29d-136">Wenn das angegebene Anwendungs Installationsprogramm den Sicherheitszugriff auf eine Datei oder ein Verzeichnis ändert, vorhandene oder neue, werden die zugehörigen Änderungen nicht in das Paket aufgenommen.</span><span class="sxs-lookup"><span data-stu-id="5e29d-136">If the specified application installer modifies security access to a file or directory, existing or new, the associated changes will not be captured into the package.</span></span>



~~~
If the application does not have an associated installer file and you plan to run all installation steps manually, select the **Perform a Custom Installation** check box, and then Click **Next**.
~~~

6. <span data-ttu-id="5e29d-137">Geben Sie auf der Seite **Package Name** einen Namen ein, der dem Paket zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="5e29d-137">On the **Package Name** page, type a name that will be associated with the package.</span></span> <span data-ttu-id="5e29d-138">Verwenden Sie einen Namen, der hilft, den Zweck und die Version der Anwendung zu identifizieren, die dem Paket hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="5e29d-138">Use a name that helps identify the purpose and version of the application that will be added to the package.</span></span> <span data-ttu-id="5e29d-139">Der Paket Name wird in der App-V 5,0-Verwaltungskonsole angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5e29d-139">The package name is displayed in the App-V 5.0 Management Console.</span></span>

   <span data-ttu-id="5e29d-140">Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="5e29d-140">Click **Next**.</span></span>

7. <span data-ttu-id="5e29d-141">Wenn der Sequencer und das Anwendungs Installationsprogramm bereit sind, können Sie auf der **Installations** Seite fortfahren, die Anwendung zu installieren, damit der Sequencer den Installationsvorgang überwachen kann.</span><span class="sxs-lookup"><span data-stu-id="5e29d-141">On the **Installation** page, when the sequencer and application installer are ready you can proceed to install the application so that the sequencer can monitor the installation process.</span></span>

   > [!IMPORTANT]
   > <span data-ttu-id="5e29d-142">Sie sollten Anwendungen immer an einem sicheren Ort installieren und sicherstellen, dass während der Überwachung keine anderen Benutzer am Computer angemeldet sind, auf dem der Sequencer ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5e29d-142">You should always install applications to a secure location and make sure no other users are logged on to the computer running the sequencer during monitoring.</span></span>



~~~
Use the application's installation process to perform the installation. If additional installation files must be run as part of the installation, click **Run** to locate and run the additional installation files. When you are finished with the installation, select **I am finished installing**. Click **Next**.
~~~

8. <span data-ttu-id="5e29d-143">Warten Sie auf der **Installations** Seite, während der Sequencer das virtualisierte Anwendungspaket konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="5e29d-143">On the **Installation** page, wait while the sequencer configures the virtualized application package.</span></span>

9. <span data-ttu-id="5e29d-144">Führen Sie auf der Seite **Software konfigurieren** optional die Programme aus, die im Paket enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="5e29d-144">On the **Configure Software** page, optionally run the programs contained in the package.</span></span> <span data-ttu-id="5e29d-145">In diesem Schritt können Sie alle erforderlichen Lizenz-oder Konfigurationsaufgaben ausführen, bevor Sie das Paket auf Zielcomputern bereitstellen und ausführen.</span><span class="sxs-lookup"><span data-stu-id="5e29d-145">This step allows you to complete any necessary license or configuration tasks before you deploy and run the package on target computers.</span></span> <span data-ttu-id="5e29d-146">Wenn Sie alle Programme auf einmal ausführen möchten, wählen Sie mindestens ein Programm aus, und klicken Sie dann auf **alle ausführen**.</span><span class="sxs-lookup"><span data-stu-id="5e29d-146">To run all the programs at one time, select at least one program, and then click **Run All**.</span></span> <span data-ttu-id="5e29d-147">Wenn Sie bestimmte Programme ausführen möchten, wählen Sie das Programm oder die Programme aus, und klicken Sie dann auf **ausgewählt ausführen**.</span><span class="sxs-lookup"><span data-stu-id="5e29d-147">To run specific programs, select the program or programs, and then click **Run Selected**.</span></span> <span data-ttu-id="5e29d-148">Führen Sie die erforderlichen Konfigurationsaufgaben aus, und schließen Sie dann die Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="5e29d-148">Complete the required configuration tasks and then close the applications.</span></span> <span data-ttu-id="5e29d-149">Möglicherweise müssen Sie einige Minuten warten, bis alle Programme ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="5e29d-149">You may need to wait several minutes for all programs to run.</span></span>

   > [!NOTE]  
   > <span data-ttu-id="5e29d-150">Wenn Sie Aufgaben der ersten Verwendung für eine Anwendung ausführen möchten, die in der Liste nicht zur Verfügung steht, öffnen Sie die Anwendung.</span><span class="sxs-lookup"><span data-stu-id="5e29d-150">To run first-use tasks for any application that is not available in the list, open the application.</span></span> <span data-ttu-id="5e29d-151">Die zugehörigen Informationen werden in diesem Schritt erfasst.</span><span class="sxs-lookup"><span data-stu-id="5e29d-151">The associated information will be captured during this step.</span></span>



~~~
Click **Next**.
~~~

10. <span data-ttu-id="5e29d-152">Auf der Seite " **Installationsbericht** " können Sie Informationen zum virtualisierten Anwendungspaket, das Sie gerade sequenziert haben, überprüfen.</span><span class="sxs-lookup"><span data-stu-id="5e29d-152">On the **Installation Report** page, you can review information about the virtualized application package you have just sequenced.</span></span> <span data-ttu-id="5e29d-153">Doppelklicken Sie in **zusätzlichen Informationen**auf ein Ereignis, um detailliertere Informationen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="5e29d-153">In **Additional Information**, double-click an event to obtain more detailed information.</span></span> <span data-ttu-id="5e29d-154">Klicken Sie auf **weiter**, um fortzufahren.</span><span class="sxs-lookup"><span data-stu-id="5e29d-154">To proceed, click **Next**.</span></span>

11. <span data-ttu-id="5e29d-155">Die Seite " **Anpassen** " wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5e29d-155">The **Customize** page is displayed.</span></span> <span data-ttu-id="5e29d-156">Wenn Sie die Installation und Konfiguration der virtuellen Anwendung abgeschlossen haben, wählen Sie **jetzt beenden** aus, und fahren Sie mit Schritt 14 dieses Verfahrens fort.</span><span class="sxs-lookup"><span data-stu-id="5e29d-156">If you are finished installing and configuring the virtual application, select **Stop now** and skip to step 14 of this procedure.</span></span> <span data-ttu-id="5e29d-157">Wenn Sie eine der folgenden Anpassungen ausführen möchten, wählen Sie **Anpassen**aus.</span><span class="sxs-lookup"><span data-stu-id="5e29d-157">To perform either of the following customizations, select **Customize**.</span></span>

    -   <span data-ttu-id="5e29d-158">Vorbereiten des virtuellen Pakets für Streaming.</span><span class="sxs-lookup"><span data-stu-id="5e29d-158">Prepare the virtual package for streaming.</span></span> <span data-ttu-id="5e29d-159">Durch Streaming wird die Benutzerfreundlichkeit verbessert, wenn das virtuelle Anwendungspaket auf Zielcomputern ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5e29d-159">Streaming improves the experience when the virtual application package is run on target computers.</span></span>

    -   <span data-ttu-id="5e29d-160">Geben Sie die Betriebssysteme an, die dieses Paket ausführen können.</span><span class="sxs-lookup"><span data-stu-id="5e29d-160">Specify the operating systems that can run this package.</span></span>

    <span data-ttu-id="5e29d-161">Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="5e29d-161">Click **Next**.</span></span>

12. <span data-ttu-id="5e29d-162">Führen Sie auf der Seite " **Streaming** " jedes Programm so aus, dass es optimiert und effizienter auf Zielcomputern ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="5e29d-162">On the **Streaming** page, run each program so that it can be optimized and run more efficiently on target computers.</span></span> <span data-ttu-id="5e29d-163">Es kann mehrere Minuten dauern, bis alle Anwendungen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="5e29d-163">It can take several minutes for all the applications to run.</span></span> <span data-ttu-id="5e29d-164">Schließen Sie alle Anwendungen, nachdem alle Anwendungen ausgeführt wurden, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="5e29d-164">After all applications have run, close each of the applications, and then click **Next**.</span></span>

   > [!NOTE]  
   > <span data-ttu-id="5e29d-165">Wenn Sie während dieses Schritts keine Anwendungen öffnen, ist die standardmäßige Streaming-Methode eine bedarfsgesteuerte Streaming-Übermittlung.</span><span class="sxs-lookup"><span data-stu-id="5e29d-165">If you do not open any applications during this step, the default streaming method is on-demand streaming delivery.</span></span> <span data-ttu-id="5e29d-166">Das bedeutet, dass Anwendungen nach und nach heruntergeladen werden, bis Sie geöffnet werden können, und je nachdem, wie das Laden des Hintergrunds konfiguriert wird, wird die restliche Anwendung geladen.</span><span class="sxs-lookup"><span data-stu-id="5e29d-166">This means applications will be downloaded bit by bit until it can be opened, and then depending on how the background loading is configured, will load the rest of the application.</span></span>



13. <span data-ttu-id="5e29d-167">Geben Sie auf der Seite **Zielbetriebssystem** die Betriebssysteme an, mit denen dieses Paket ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="5e29d-167">On the **Target OS** page, specify the operating systems that can run this package.</span></span> <span data-ttu-id="5e29d-168">Wenn Sie zulassen möchten, dass alle unterstützten Betriebssysteme in Ihrer Umgebung dieses Paket ausführen können, wählen Sie zulassen, dass **Dieses Paket unter einem beliebigen Betriebssystem ausgeführt**wird.</span><span class="sxs-lookup"><span data-stu-id="5e29d-168">To allow all supported operating systems in your environment to run this package, select **Allow this package to run on any operating system**.</span></span> <span data-ttu-id="5e29d-169">Wenn Sie dieses Paket so konfigurieren möchten, dass es nur auf bestimmten Betriebssystemen ausgeführt wird, wählen Sie zulassen, dass **Dieses Paket nur unter den folgenden Betriebssystemen ausgeführt** wird, und wählen Sie die Betriebssysteme aus, die dieses Paket ausführen können.</span><span class="sxs-lookup"><span data-stu-id="5e29d-169">To configure this package to run only on specific operating systems, select **Allow this package to run only on the following operating systems** and select the operating systems that can run this package.</span></span> <span data-ttu-id="5e29d-170">Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="5e29d-170">Click **Next**.</span></span>

   > [!IMPORTANT]
   > <span data-ttu-id="5e29d-171">Stellen Sie sicher, dass die hier angegebenen Betriebssysteme von der Anwendung unterstützt werden, die Sie sequenzieren.</span><span class="sxs-lookup"><span data-stu-id="5e29d-171">Make sure that the operating systems you specify here are supported by the application you are sequencing.</span></span>



14. <span data-ttu-id="5e29d-172">Die Seite **Paket erstellen** wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5e29d-172">The **Create Package** page is displayed.</span></span> <span data-ttu-id="5e29d-173">Wenn Sie das Paket ändern möchten, ohne es zu speichern, wählen Sie weiter aus, um das Paket **ohne Speichern mit dem Paket-Editor zu ändern**.</span><span class="sxs-lookup"><span data-stu-id="5e29d-173">To modify the package without saving it, select **Continue to modify package without saving using the package editor**.</span></span> <span data-ttu-id="5e29d-174">Mit dieser Option wird das Paket in der Sequencer-Konsole geöffnet, sodass Sie das Paket vor dem Speichern ändern können.</span><span class="sxs-lookup"><span data-stu-id="5e29d-174">This option opens the package in the sequencer console so that you can modify the package before it is saved.</span></span> <span data-ttu-id="5e29d-175">Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="5e29d-175">Click **Next**.</span></span>

   <span data-ttu-id="5e29d-176">Wenn Sie das Paket sofort speichern möchten, wählen Sie **das Paket jetzt speichern** (Standard) aus.</span><span class="sxs-lookup"><span data-stu-id="5e29d-176">To save the package immediately, select **Save the package now** (default).</span></span> <span data-ttu-id="5e29d-177">Fügen Sie optionale **Kommentare** hinzu, die dem Paket zugeordnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="5e29d-177">Add optional **Comments** to be associated with the package.</span></span> <span data-ttu-id="5e29d-178">Kommentare sind hilfreich, um die Programmversion und weitere Informationen zum Paket zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="5e29d-178">Comments are useful for identifying the program version and other information about the package.</span></span>

   > [!IMPORTANT]
   > <span data-ttu-id="5e29d-179">Das System unterstützt keine nicht druckbaren Zeichen in **Kommentaren** und **Beschreibungen**.</span><span class="sxs-lookup"><span data-stu-id="5e29d-179">The system does not support non-printable characters in **Comments** and **Descriptions**.</span></span>



~~~
The default **Save Location** is also displayed on this page. To change the default location, click **Browse** and specify the new location. Click **Create**.
~~~

15. <span data-ttu-id="5e29d-180">Die Seite **Fertigstellung** wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5e29d-180">The **Completion** page is displayed.</span></span> <span data-ttu-id="5e29d-181">Überprüfen Sie die Informationen im Bereich **Bericht des virtuellen Anwendungspakets** nach Bedarf, und klicken Sie dann auf **Schließen**.</span><span class="sxs-lookup"><span data-stu-id="5e29d-181">Review the information in the **Virtual Application Package Report** pane as needed, then click **Close**.</span></span> <span data-ttu-id="5e29d-182">Diese Informationen sind auch in der **Report.xml** -Datei verfügbar, die sich in dem Verzeichnis befindet, in dem das Paket erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="5e29d-182">This information is also available in the **Report.xml** file that is located in the directory where the package was created.</span></span>

   <span data-ttu-id="5e29d-183">Das Paket steht jetzt im Sequencer zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="5e29d-183">The package is now available in the sequencer.</span></span>

   > [!IMPORTANT]
   > <span data-ttu-id="5e29d-184">Nachdem Sie ein virtuelles Anwendungspaket erfolgreich erstellt haben, können Sie das virtuelle Anwendungspaket nicht auf dem Computer ausführen, auf dem der Sequencer ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5e29d-184">After you have successfully created a virtual application package, you cannot run the virtual application package on the computer that is running the sequencer.</span></span>



**<span data-ttu-id="5e29d-185">So Sequenzieren Sie eine Add-on-oder Plug-in-Anwendung</span><span class="sxs-lookup"><span data-stu-id="5e29d-185">To sequence an add-on or plug-in application</span></span>**

1. > [!NOTE]  
   > <span data-ttu-id="5e29d-186">Bevor Sie das folgende Verfahren ausführen, installieren Sie die übergeordnete Anwendung lokal auf dem Computer, auf dem der Sequencer ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5e29d-186">Before performing the following procedure, install the parent application locally on the computer that is running the sequencer.</span></span> <span data-ttu-id="5e29d-187">Wenn Sie die übergeordnete Anwendung virtualisiert haben, können Sie die Schritte im Add-on-oder Plug-in-Workflow ausführen, um die übergeordnete Anwendung auf dem Computer zu entpacken.</span><span class="sxs-lookup"><span data-stu-id="5e29d-187">Or if you have the parent application virtualized, you can follow the steps in the add-on or plug-in workflow to unpack the parent application on the computer.</span></span>
   >
   > <span data-ttu-id="5e29d-188">Wenn Sie beispielsweise ein Plug-in für Microsoft Excel sequenzieren, installieren Sie Microsoft Excel lokal auf dem Computer, auf dem der Sequencer ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5e29d-188">For example, if you are sequencing a plug-in for Microsoft Excel, install Microsoft Excel locally on the computer that is running the sequencer.</span></span> <span data-ttu-id="5e29d-189">Installieren Sie die übergeordnete Anwendung auch im gleichen Verzeichnis, in dem die Anwendung auf den Zielcomputern installiert ist.</span><span class="sxs-lookup"><span data-stu-id="5e29d-189">Also install the parent application in the same directory where the application is installed on target computers.</span></span> <span data-ttu-id="5e29d-190">Wenn das Plug-in oder Add-on mit einem vorhandenen virtuellen Anwendungspaket verwendet werden soll, installieren Sie die Anwendung auf dem virtuellen Anwendungs Laufwerk, das beim Erstellen des übergeordneten virtuellen Anwendungspakets verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="5e29d-190">If the plug-in or add-on is going to be used with an existing virtual application package, install the application on the same virtual application drive that was used when you created the parent virtual application package.</span></span>



~~~
On the computer that runs the sequencer, click **All Programs**, and then Click **Microsoft Application Virtualization**, and then click **Microsoft Application Virtualization Sequencer**.
~~~

2. <span data-ttu-id="5e29d-191">\*<strong><em>Klicken Sie im Sequencer auf \* </em> Neues virtuelles Anwendungspaket erstellen </strong> .</span><span class="sxs-lookup"><span data-stu-id="5e29d-191">\*<strong><em>In the sequencer, click \*</em>Create a New Virtual Application Package</strong>.</span></span> <span data-ttu-id="5e29d-192">Wählen Sie **Paket erstellen (Standard)** aus, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="5e29d-192">Select **Create Package (default)**, and then click **Next**.</span></span>

3. <span data-ttu-id="5e29d-193">Überprüfen Sie auf der Seite **Computer vorbereiten** die Probleme, die möglicherweise dazu führen, dass die Paketerstellung fehlschlägt oder dass das Paket unnötige Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="5e29d-193">On the **Prepare Computer** page, review the issues that might cause the package creation to fail or could cause the package to contain unnecessary data.</span></span> <span data-ttu-id="5e29d-194">Sie sollten alle potenziellen Probleme beheben, bevor Sie fortfahren.</span><span class="sxs-lookup"><span data-stu-id="5e29d-194">You should resolve all potential issues before you continue.</span></span> <span data-ttu-id="5e29d-195">Nachdem Sie Korrekturen vorgenommen haben, klicken Sie auf **Aktualisieren** , um die aktualisierten Informationen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="5e29d-195">After making any corrections, click **Refresh** to display the updated information.</span></span> <span data-ttu-id="5e29d-196">Nachdem Sie alle potenziellen Probleme behoben haben, klicken Sie auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="5e29d-196">After you have resolved all potential issues, click **Next**.</span></span>

   > [!IMPORTANT]
   > <span data-ttu-id="5e29d-197">Wenn Sie die Virenscansoftware deaktivieren müssen, sollten Sie zuerst den Computer scannen, auf dem der Sequencer ausgeführt wird, um sicherzustellen, dass dem Paket keine unerwünschten oder böswilligen Dateien hinzugefügt werden können.</span><span class="sxs-lookup"><span data-stu-id="5e29d-197">If you are required to disable virus scanning software, you should first scan the computer that runs the sequencer in order to ensure that no unwanted or malicious files could be added to the package.</span></span>



4. <span data-ttu-id="5e29d-198">Wählen Sie auf der Seite **Art der Anwendung** **Add-on oder Plug-in**aus, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="5e29d-198">On the **Type of Application** page, select **Add-on or Plug-in**, and then click **Next**.</span></span>

5. <span data-ttu-id="5e29d-199">Klicken Sie auf der Seite **Installationsprogramm auswählen** auf **Durchsuchen** , und geben Sie die Installationsdatei für das Add-on oder das Plug-in an.</span><span class="sxs-lookup"><span data-stu-id="5e29d-199">On the **Select Installer** page, click **Browse** and specify the installation file for the add-on or plug-in.</span></span> <span data-ttu-id="5e29d-200">Wenn das Add-on oder Plug-in keine zugeordnete Installationsdatei enthält und Sie alle Installationsschritte manuell ausführen möchten, aktivieren Sie das Kontrollkästchen **diese Option zum Durchführen einer benutzerdefinierten Installation auswählen** , und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="5e29d-200">If the add-on or plug-in does not have an associated installer file and you plan to run all installation steps manually, select the **Select this option to perform a custom installation** check box, and then click **Next**.</span></span>

6. <span data-ttu-id="5e29d-201">Stellen Sie auf der Seite **primäre Installation** sicher, dass die primäre Anwendung auf dem Computer installiert ist, auf dem der Sequencer ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5e29d-201">On the **Install Primary** page, ensure that the primary application is installed on the computer that runs the sequencer.</span></span> <span data-ttu-id="5e29d-202">Alternativ können Sie ein vorhandenes Paket erweitern, das lokal auf dem Computer gespeichert wurde, auf dem der Sequencer ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5e29d-202">Alternatively, you can expand an existing package that has been saved locally on the computer that runs the sequencer.</span></span> <span data-ttu-id="5e29d-203">Klicken Sie dazu auf **Paket erweitern**, und wählen Sie dann das Paket aus.</span><span class="sxs-lookup"><span data-stu-id="5e29d-203">To do this, click **Expand Package**, and then select the package.</span></span> <span data-ttu-id="5e29d-204">Nachdem Sie das übergeordnete Programm erweitert oder installiert haben, wählen Sie **Ich habe das primäre übergeordnete Programm installiert**aus.</span><span class="sxs-lookup"><span data-stu-id="5e29d-204">After you have expanded or installed the parent program, select **I have installed the primary parent program**.</span></span>

   <span data-ttu-id="5e29d-205">Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="5e29d-205">Click **Next**.</span></span>

7. <span data-ttu-id="5e29d-206">Geben Sie auf der Seite **Package Name** einen Namen ein, der dem Paket zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="5e29d-206">On the **Package Name** page, type a name that will be associated with the package.</span></span> <span data-ttu-id="5e29d-207">Verwenden Sie einen Namen, der hilft, den Zweck und die Version der Anwendung zu identifizieren, die dem Paket hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="5e29d-207">Use a name that helps identify the purpose and version of the application that will be added to the package.</span></span> <span data-ttu-id="5e29d-208">Der Paket Name wird in der App-V 5,0-Verwaltungskonsole angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5e29d-208">The package name will be displayed in the App-V 5.0 Management Console.</span></span>

   <span data-ttu-id="5e29d-209">Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="5e29d-209">Click **Next**.</span></span>

8. <span data-ttu-id="5e29d-210">Wenn der Sequencer und das Anwendungs Installationsprogramm bereit sind, können Sie auf der **Installations** Seite mit der Installation des Plug-ins oder der Add-in-Anwendung fortfahren, damit der Sequencer den Installationsvorgang überwachen kann.</span><span class="sxs-lookup"><span data-stu-id="5e29d-210">On the **Installation** page, when the sequencer and application installer are ready you can proceed to install the plug-in or add-in application so the sequencer can monitor the installation process.</span></span> <span data-ttu-id="5e29d-211">Verwenden Sie den Installationsprozess der Anwendung, um die Installation durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="5e29d-211">Use the application's installation process to perform the installation.</span></span> <span data-ttu-id="5e29d-212">Wenn zusätzliche Installationsdateien als Teil der Installation ausgeführt werden müssen, klicken Sie auf **Ausführen** , und führen Sie die zusätzlichen Installationsdateien aus.</span><span class="sxs-lookup"><span data-stu-id="5e29d-212">If additional installation files must be run as part of the installation, click **Run** and locate and run the additional installation files.</span></span> <span data-ttu-id="5e29d-213">Wenn Sie die Installation abgeschlossen haben, wählen Sie **Ich habe die Installation abgeschlossen**aus, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="5e29d-213">When you are finished with the installation, select **I am finished installing**, and then click **Next**.</span></span>

9. <span data-ttu-id="5e29d-214">Auf der Seite **Installationsbericht** können Sie Informationen zu dem soeben sequenzierten virtuellen Anwendungspaket überprüfen.</span><span class="sxs-lookup"><span data-stu-id="5e29d-214">On the **Installation Report** page, you can review information about the virtual application package that you just sequenced.</span></span> <span data-ttu-id="5e29d-215">Eine detailliertere Erläuterung der Informationen, die in **zusätzlichen Informationen**angezeigt werden, finden Sie, indem Sie auf das Ereignis doppelklicken.</span><span class="sxs-lookup"><span data-stu-id="5e29d-215">For a more detailed explanation about the information displayed in **Additional Information**, double-click the event.</span></span> <span data-ttu-id="5e29d-216">Nachdem Sie die Informationen überprüft haben, klicken Sie auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="5e29d-216">After you have reviewed the information, click **Next**.</span></span>

10. <span data-ttu-id="5e29d-217">Die Seite " **Anpassen** " wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5e29d-217">The **Customize** page is displayed.</span></span> <span data-ttu-id="5e29d-218">Wenn Sie die Installation und Konfiguration der virtuellen Anwendung abgeschlossen haben, wählen Sie **jetzt beenden** aus, und fahren Sie mit Schritt 12 dieses Verfahrens fort.</span><span class="sxs-lookup"><span data-stu-id="5e29d-218">If you are finished installing and configuring the virtual application, select **Stop now** and skip to step 12 of this procedure.</span></span> <span data-ttu-id="5e29d-219">Wenn Sie eine der folgenden Anpassungen ausführen möchten, wählen Sie **Anpassen**aus.</span><span class="sxs-lookup"><span data-stu-id="5e29d-219">To perform either of the following customizations, select **Customize**.</span></span>

    -   <span data-ttu-id="5e29d-220">Optimieren Sie, wie das Paket in einem langsamen oder unzuverlässigen Netzwerk ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5e29d-220">Optimize how the package will run across a slow or unreliable network.</span></span>

    -   <span data-ttu-id="5e29d-221">Geben Sie die Betriebssysteme an, die dieses Paket ausführen können.</span><span class="sxs-lookup"><span data-stu-id="5e29d-221">Specify the operating systems that can run this package.</span></span>

    <span data-ttu-id="5e29d-222">Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="5e29d-222">Click **Next**.</span></span>

11. <span data-ttu-id="5e29d-223">Führen Sie auf der Seite " **Streaming** " jedes Programm so aus, dass es optimiert und effizienter auf Zielcomputern ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="5e29d-223">On the **Streaming** page, run each program so that it can be optimized and run more efficiently on target computers.</span></span> <span data-ttu-id="5e29d-224">Durch Streaming wird die Erfahrung verbessert, wenn das virtuelle Anwendungspaket auf Zielcomputern in Netzwerken mit hoher Latenz ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5e29d-224">Streaming improves the experience when the virtual application package is run on target computers on high-latency networks.</span></span> <span data-ttu-id="5e29d-225">Es kann mehrere Minuten dauern, bis alle Anwendungen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="5e29d-225">It can take several minutes for all the applications to run.</span></span> <span data-ttu-id="5e29d-226">Schließen Sie alle Anwendungen, nachdem alle Anwendungen ausgeführt wurden.</span><span class="sxs-lookup"><span data-stu-id="5e29d-226">After all applications have run, close each of the applications.</span></span> <span data-ttu-id="5e29d-227">Sie können das Paket auch so konfigurieren, dass es vor dem Öffnen vollständig heruntergeladen werden muss, indem Sie das Kontrollkästchen **zu herunterzuladende Anwendungen erzwingen** auswählen.</span><span class="sxs-lookup"><span data-stu-id="5e29d-227">You can also configure the package to be required to be fully downloaded before opening by selecting the **Force applications to be downloaded** check-box.</span></span> <span data-ttu-id="5e29d-228">Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="5e29d-228">Click **Next**.</span></span>

    > [!NOTE]  
    > <span data-ttu-id="5e29d-229">Falls erforderlich, können Sie verhindern, dass eine Anwendung während dieses Schritts geladen wird.</span><span class="sxs-lookup"><span data-stu-id="5e29d-229">If necessary, you can stop an application from loading during this step.</span></span> <span data-ttu-id="5e29d-230">Klicken Sie im Dialogfeld **Anwendungsstart** auf **Beenden** , und aktivieren Sie eines der Kontrollkästchen: **alle Anwendungen beenden** oder **nur diese Anwendung beenden**.</span><span class="sxs-lookup"><span data-stu-id="5e29d-230">In the **Application Launch** dialog box, click **Stop** and select one of the check boxes: **Stop all applications** or **Stop this application only**.</span></span>



12. <span data-ttu-id="5e29d-231">Geben Sie auf der Seite **Zielbetriebssystem** die Betriebssysteme an, mit denen dieses Paket ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="5e29d-231">On the **Target OS** page, specify the operating systems that can run this package.</span></span> <span data-ttu-id="5e29d-232">Wenn Sie zulassen möchten, dass alle unterstützten Betriebssysteme in Ihrer Umgebung dieses Paket ausführen können, aktivieren Sie das Kontrollkästchen **Dieses Paket kann auf einem beliebigen Betriebssystem ausgeführt** werden.</span><span class="sxs-lookup"><span data-stu-id="5e29d-232">To allow all supported operating systems in your environment to run this package, select the **Allow this package to run on any operating system** check box.</span></span> <span data-ttu-id="5e29d-233">Um dieses Paket so zu konfigurieren, dass es nur auf bestimmten Betriebssystemen ausgeführt wird, aktivieren Sie das Kontrollkästchen **Dieses Paket nur auf den folgenden Betriebssystemen ausführen lassen** , und wählen Sie dann die Betriebssysteme aus, die dieses Paket ausführen können.</span><span class="sxs-lookup"><span data-stu-id="5e29d-233">To configure this package to run only on specific operating systems, select the **Allow this package to run only on the following operating systems** check box, and then select the operating systems that can run this package.</span></span> <span data-ttu-id="5e29d-234">Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="5e29d-234">Click **Next**.</span></span>

13. <span data-ttu-id="5e29d-235">Die Seite **Paket erstellen** wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5e29d-235">The **Create Package** page is displayed.</span></span> <span data-ttu-id="5e29d-236">Wenn Sie das Paket ändern möchten, ohne es zu speichern, wählen Sie weiter aus, um das Paket **ohne Speichern über das Kontrollkästchen Paket-Editor zu ändern** .</span><span class="sxs-lookup"><span data-stu-id="5e29d-236">To modify the package without saving it, select **Continue to modify package without saving using the package editor** check box.</span></span> <span data-ttu-id="5e29d-237">Mit dieser Option wird das Paket in der Sequencer-Konsole geöffnet, sodass Sie das Paket vor dem Speichern ändern können.</span><span class="sxs-lookup"><span data-stu-id="5e29d-237">This option opens the package in the sequencer console so that you can modify the package before it is saved.</span></span> <span data-ttu-id="5e29d-238">Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="5e29d-238">Click **Next**.</span></span>

    <span data-ttu-id="5e29d-239">Wenn Sie das Paket sofort speichern möchten, wählen Sie **das Paket jetzt speichern**aus.</span><span class="sxs-lookup"><span data-stu-id="5e29d-239">To save the package immediately, select **Save the package now**.</span></span> <span data-ttu-id="5e29d-240">Optional können Sie eine **Beschreibung** hinzufügen, die dem Paket zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="5e29d-240">Optionally, add a **Description** that will be associated with the package.</span></span> <span data-ttu-id="5e29d-241">Beschreibungen sind hilfreich, um die Version und andere Informationen zum Paket zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="5e29d-241">Descriptions are useful for identifying the version and other information about the package.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="5e29d-242">Das System unterstützt keine nicht druckbaren Zeichen in Kommentaren und Beschreibungen.</span><span class="sxs-lookup"><span data-stu-id="5e29d-242">The system does not support non-printable characters in Comments and Descriptions.</span></span>



~~~
The default **Save Location** is also displayed on this page. To change the default location, click **Browse** and specify the new location. Click **Create**.
~~~

**<span data-ttu-id="5e29d-243">So Sequenzieren Sie eine Middleware-Anwendung</span><span class="sxs-lookup"><span data-stu-id="5e29d-243">To sequence a middleware application</span></span>**

1. <span data-ttu-id="5e29d-244">Klicken Sie auf dem Computer, auf dem der Sequencer ausgeführt wird, auf **Alle Programme**, und klicken Sie dann auf **Microsoft Application Virtualization**, und klicken Sie dann auf **Microsoft Application Virtualization Sequencer**.</span><span class="sxs-lookup"><span data-stu-id="5e29d-244">On the computer that runs the sequencer, click **All Programs**, and then Click **Microsoft Application Virtualization**, and then click **Microsoft Application Virtualization Sequencer**.</span></span>

2. <span data-ttu-id="5e29d-245">\*<strong><em>Klicken Sie im Sequencer auf \* </em> Neues virtuelles Anwendungspaket erstellen </strong> .</span><span class="sxs-lookup"><span data-stu-id="5e29d-245">\*<strong><em>In the sequencer, click \*</em>Create a New Virtual Application Package</strong>.</span></span> <span data-ttu-id="5e29d-246">Wählen Sie **Paket erstellen (Standard)** aus, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="5e29d-246">Select **Create Package (default)**, and then click **Next**.</span></span>

3. <span data-ttu-id="5e29d-247">Überprüfen Sie auf der Seite **Computer vorbereiten** die Probleme, die dazu führen können, dass die Paketerstellung fehlschlägt oder dass das Paket unnötige Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="5e29d-247">On the **Prepare Computer** page, review the issues that could cause the package creation to fail or could cause the package to contain unnecessary data.</span></span> <span data-ttu-id="5e29d-248">Sie sollten alle potenziellen Probleme beheben, bevor Sie fortfahren.</span><span class="sxs-lookup"><span data-stu-id="5e29d-248">You should resolve all potential issues before you continue.</span></span> <span data-ttu-id="5e29d-249">Nachdem Sie Korrekturen vorgenommen haben, klicken Sie auf **Aktualisieren** , um die aktualisierten Informationen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="5e29d-249">After making any corrections, click **Refresh** to display the updated information.</span></span> <span data-ttu-id="5e29d-250">Nachdem Sie alle potenziellen Probleme behoben haben, klicken Sie auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="5e29d-250">After you have resolved all potential issues, click **Next**.</span></span>

   > [!IMPORTANT]
   > <span data-ttu-id="5e29d-251">Wenn Sie die Virenscansoftware deaktivieren müssen, sollten Sie zuerst den Computer scannen, auf dem der App-V 5,0-Sequenzer ausgeführt wird, um sicherzustellen, dass dem Paket keine unerwünschten oder bösartigen Dateien hinzugefügt werden können.</span><span class="sxs-lookup"><span data-stu-id="5e29d-251">If you are required to disable virus scanning software, you should first scan the computer that runs the App-V 5.0 Sequencer in order to ensure that no unwanted or malicious files can be added to the package.</span></span>



4. <span data-ttu-id="5e29d-252">Wählen Sie auf der Seite **Art der Anwendung** **Middleware**aus, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="5e29d-252">On the **Type of Application** page, select **Middleware**, and then click **Next**.</span></span>

5. <span data-ttu-id="5e29d-253">Klicken Sie auf der Seite **Installationsprogramm auswählen** auf **Durchsuchen** , und geben Sie die Installationsdatei für die Anwendung an.</span><span class="sxs-lookup"><span data-stu-id="5e29d-253">On the **Select Installer** page, click **Browse** and specify the installation file for the application.</span></span> <span data-ttu-id="5e29d-254">Wenn die Anwendung keine zugeordnete Installationsdatei hat und Sie alle Installationsschritte manuell ausführen möchten, aktivieren Sie das Kontrollkästchen **diese Option zum Durchführen einer benutzerdefinierten Installation auswählen** , und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="5e29d-254">If the application does not have an associated installer file and you plan to run all installation steps manually, select the **Select this option to perform a custom installation** check box, and then click **Next**.</span></span>

6. <span data-ttu-id="5e29d-255">Geben Sie auf der Seite **Package Name** einen Namen ein, der dem Paket zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="5e29d-255">On the **Package Name** page, type a name that will be associated with the package.</span></span> <span data-ttu-id="5e29d-256">Verwenden Sie einen Namen, der hilft, den Zweck und die Version der Anwendung zu identifizieren, die dem Paket hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="5e29d-256">Use a name that helps identify the purpose and version of the application that will be added to the package.</span></span> <span data-ttu-id="5e29d-257">Der Paket Name wird in der App-V 5,0-Verwaltungskonsole angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5e29d-257">The package name is displayed in the App-V 5.0 Management Console.</span></span>

   <span data-ttu-id="5e29d-258">Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="5e29d-258">Click **Next**.</span></span>

7. <span data-ttu-id="5e29d-259">Wenn das Installationsprogramm für Sequencer und Middleware bereit ist, können Sie auf der **Installations** Seite fortfahren, die Anwendung zu installieren, damit der Sequencer den Installationsvorgang überwachen kann.</span><span class="sxs-lookup"><span data-stu-id="5e29d-259">On the **Installation** page, when the sequencer and middleware application installer are ready you can proceed to install the application so that the sequencer can monitor the installation process.</span></span> <span data-ttu-id="5e29d-260">Verwenden Sie den Installationsprozess der Anwendung, um die Installation durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="5e29d-260">Use the application's installation process to perform the installation.</span></span> <span data-ttu-id="5e29d-261">Wenn zusätzliche Installationsdateien als Teil der Installation ausgeführt werden müssen, klicken Sie auf **Ausführen**, um die zusätzlichen Installationsdateien zu suchen und auszuführen.</span><span class="sxs-lookup"><span data-stu-id="5e29d-261">If additional installation files must be run as part of the installation, click **Run**, to locate and run the additional installation files.</span></span> <span data-ttu-id="5e29d-262">Wenn Sie die Installation abgeschlossen haben, aktivieren Sie das Kontrollkästchen **Ich habe die Installation abgeschlossen** , und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="5e29d-262">When you are finished with the installation, select the **I am finished installing** check box, and then click **Next**.</span></span>

8. <span data-ttu-id="5e29d-263">Warten Sie auf der **Installations** Seite, während der Sequencer das virtuelle Anwendungspaket konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="5e29d-263">On the **Installation** page, wait while the sequencer configures the virtual application package.</span></span>

9. <span data-ttu-id="5e29d-264">Auf der Seite **Installationsbericht** können Sie Informationen zu dem soeben sequenzierten virtuellen Anwendungspaket überprüfen.</span><span class="sxs-lookup"><span data-stu-id="5e29d-264">On the **Installation Report** page, you can review information about the virtual application package that you have just sequenced.</span></span> <span data-ttu-id="5e29d-265">Doppelklicken Sie in **zusätzlichen Informationen**auf ein Ereignis, um detailliertere Informationen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="5e29d-265">In **Additional Information**, double-click an event to obtain more detailed information.</span></span> <span data-ttu-id="5e29d-266">Klicken Sie auf **weiter**, um fortzufahren.</span><span class="sxs-lookup"><span data-stu-id="5e29d-266">To proceed, click **Next**.</span></span>

10. <span data-ttu-id="5e29d-267">Geben Sie auf der Seite **Zielbetriebssystem** die Betriebssysteme an, mit denen dieses Paket ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="5e29d-267">On the **Target OS** page, specify the operating systems that can run this package.</span></span> <span data-ttu-id="5e29d-268">Wenn Sie alle unterstützten Betriebssysteme in Ihrer Umgebung zum Ausführen dieses Pakets aktivieren möchten, aktivieren Sie das Kontrollkästchen **Dieses Paket kann auf einem beliebigen Betriebssystem ausgeführt** werden.</span><span class="sxs-lookup"><span data-stu-id="5e29d-268">To enable all supported operating systems in your environment to run this package, select the **Allow this package to run on any operating system** check box.</span></span> <span data-ttu-id="5e29d-269">Wenn Sie dieses Paket so konfigurieren möchten, dass es nur auf bestimmten Betriebssystemen ausgeführt wird, aktivieren Sie das Kontrollkästchen **Dieses Paket darf nur auf dem folgenden Betriebssystem ausgeführt** werden, und wählen Sie die Betriebssysteme aus, mit denen dieses Paket ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="5e29d-269">To configure this package to run only on specific operating systems, select the **Allow this package to run only on the following operating systems** check box and select the operating systems that can run this package.</span></span> <span data-ttu-id="5e29d-270">Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="5e29d-270">Click **Next**.</span></span>

11. <span data-ttu-id="5e29d-271">Auf der Seite **Paket erstellen** wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5e29d-271">On the **Create Package** page is displayed.</span></span> <span data-ttu-id="5e29d-272">Wenn Sie das Paket ändern möchten, ohne es zu speichern, wählen Sie weiter aus, um das Paket **ohne Speichern mit dem Paket-Editor zu ändern**.</span><span class="sxs-lookup"><span data-stu-id="5e29d-272">To modify the package without saving it, select **Continue to modify package without saving using the package editor**.</span></span> <span data-ttu-id="5e29d-273">Mit dieser Option wird das Paket in der Sequencer-Konsole geöffnet, sodass Sie das Paket vor dem Speichern ändern können.</span><span class="sxs-lookup"><span data-stu-id="5e29d-273">This option opens the package in the sequencer console so that you can modify the package before it is saved.</span></span> <span data-ttu-id="5e29d-274">Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="5e29d-274">Click **Next**.</span></span>

    <span data-ttu-id="5e29d-275">Wenn Sie das Paket sofort speichern möchten, wählen Sie **das Paket jetzt speichern**aus.</span><span class="sxs-lookup"><span data-stu-id="5e29d-275">To save the package immediately, select **Save the package now**.</span></span> <span data-ttu-id="5e29d-276">Optional können Sie eine **Beschreibung** hinzufügen, die dem Paket zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="5e29d-276">Optionally, add a **Description** to be associated with the package.</span></span> <span data-ttu-id="5e29d-277">Beschreibungen sind hilfreich, um die Programmversion und weitere Informationen über das Paket zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="5e29d-277">Descriptions are useful for identifying the program version and other information about the package.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="5e29d-278">Das System unterstützt keine nicht druckbaren Zeichen in Kommentaren und Beschreibungen.</span><span class="sxs-lookup"><span data-stu-id="5e29d-278">The system does not support non-printable characters in Comments and Descriptions.</span></span>



~~~
The default **Save Location** is also displayed on this page. To change the default location, click **Browse** and specify the new location. Click **Create**.
~~~

12. <span data-ttu-id="5e29d-279">Die Seite **Fertigstellung** wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5e29d-279">The **Completion** page is displayed.</span></span> <span data-ttu-id="5e29d-280">Überprüfen Sie die Informationen im Bereich **Bericht des virtuellen Anwendungspakets** nach Bedarf, und klicken Sie dann auf **Schließen**.</span><span class="sxs-lookup"><span data-stu-id="5e29d-280">Review the information in the **Virtual Application Package Report** pane as needed, then click **Close**.</span></span> <span data-ttu-id="5e29d-281">Diese Informationen sind auch in der **Report.xml** -Datei verfügbar, die sich in dem in Schritt 11 dieses Verfahrens angegebenen Verzeichnis befindet.</span><span class="sxs-lookup"><span data-stu-id="5e29d-281">This information is also available in the **Report.xml** file that is located in the directory specified in step 11 of this procedure.</span></span>

   <span data-ttu-id="5e29d-282">Das Paket steht jetzt im Sequencer zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="5e29d-282">The package is now available in the sequencer.</span></span> <span data-ttu-id="5e29d-283">Um die Paketeigenschaften zu bearbeiten, klicken Sie auf **Bearbeiten \ [Package Name \]**.</span><span class="sxs-lookup"><span data-stu-id="5e29d-283">To edit the package properties, click **Edit \[Package Name\]**.</span></span>

   > [!IMPORTANT]
   > <span data-ttu-id="5e29d-284">Nachdem Sie ein virtuelles Anwendungspaket erfolgreich erstellt haben, können Sie das virtuelle Anwendungspaket nicht auf dem Computer ausführen, auf dem der Sequencer ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5e29d-284">After you have successfully created a virtual application package, you cannot run the virtual application package on the computer that is running the sequencer.</span></span>



~~~
**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## <span data-ttu-id="5e29d-285">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="5e29d-285">Related topics</span></span>


[<span data-ttu-id="5e29d-286">Vorgänge für App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="5e29d-286">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)









