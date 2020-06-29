---
title: So erstellen Sie App-V Package Accelerators (App-V 4.6 SP1)
description: So erstellen Sie App-V Package Accelerators (App-V 4.6 SP1)
author: dansimp
ms.assetid: 585e692e-cebb-48ac-93ab-b2e7eb7ae7ad
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: eb806ccf04fcd5ae7db87c5de21e85217739fcbc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807187"
---
# <span data-ttu-id="1e9de-103">So erstellen Sie App-V Package Accelerators (App-V 4.6 SP1)</span><span class="sxs-lookup"><span data-stu-id="1e9de-103">How to Create App-V Package Accelerators (App-V 4.6 SP1)</span></span>


<span data-ttu-id="1e9de-104">Sie können App-V-Paket Beschleuniger verwenden, um automatisch ein neues virtuelles Anwendungspaket zu generieren.</span><span class="sxs-lookup"><span data-stu-id="1e9de-104">You can use App-V Package Accelerators to automatically generate a new virtual application package.</span></span> <span data-ttu-id="1e9de-105">Nachdem Sie erfolgreich einen Paket Beschleuniger erstellt haben, können Sie den Paket Beschleuniger wieder verwenden und freigeben.</span><span class="sxs-lookup"><span data-stu-id="1e9de-105">After you have successfully created a Package Accelerator, you can reuse and share the Package Accelerator.</span></span> <span data-ttu-id="1e9de-106">Weitere Informationen zu Paket Beschleunigern finden Sie unter [Informationen zu app-v-Paket Beschleunigern (app-v 4,6 SP1)](about-app-v-package-accelerators--app-v-46-sp1-.md).</span><span class="sxs-lookup"><span data-stu-id="1e9de-106">For more information about Package Accelerators, see [About App-V Package Accelerators (App-V 4.6 SP1)](about-app-v-package-accelerators--app-v-46-sp1-.md).</span></span> <span data-ttu-id="1e9de-107">Das Erstellen von App-V-Paket Beschleunigern ist eine erweiterte Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="1e9de-107">Creating App-V Package Accelerators is an advanced task.</span></span> <span data-ttu-id="1e9de-108">Paket Beschleuniger können Kennwort-und benutzerspezifische Informationen enthalten.</span><span class="sxs-lookup"><span data-stu-id="1e9de-108">Package Accelerators can contain password and user-specific information.</span></span> <span data-ttu-id="1e9de-109">Daher müssen Sie Paket Beschleuniger und die zugehörigen Installationsmedien an einem sicheren Speicherort speichern, und Sie sollten den Paket Beschleuniger nach der Erstellung digital signieren, damit der Herausgeber überprüft werden kann, wenn der App-V-Paket Beschleuniger angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="1e9de-109">Therefore you must save Package Accelerators and the associated installation media in a secure location, and you should digitally sign the Package Accelerator after you create it so that the publisher can be verified when the App-V Package Accelerator is applied.</span></span>

<span data-ttu-id="1e9de-110">In einigen Fällen müssen Sie möglicherweise die Anwendung lokal auf dem Computer installieren, auf dem der Sequencer ausgeführt wird, um den Paket Beschleuniger zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="1e9de-110">In some situations, to create the Package Accelerator, you might have to install the application locally on the computer running the Sequencer.</span></span> <span data-ttu-id="1e9de-111">Versuchen Sie zunächst, den Paket Beschleuniger mithilfe des Installationsmediums zu erstellen, und wenn es eine Reihe fehlender Dateien gibt, die erforderlich sind, installieren Sie die Anwendung lokal auf dem Computer, auf dem der Sequencer ausgeführt wird, und erstellen Sie dann den Paket Beschleuniger.</span><span class="sxs-lookup"><span data-stu-id="1e9de-111">First try to create the Package Accelerator by using the installation media, and if there are a number of missing files that are required, install the application locally to the computer running the Sequencer, and then create the Package Accelerator.</span></span>

**<span data-ttu-id="1e9de-112">Wichtig</span><span class="sxs-lookup"><span data-stu-id="1e9de-112">Important</span></span>**  
<span data-ttu-id="1e9de-113">Bevor Sie mit der folgenden Vorgehensweise beginnen, sollten Sie die folgenden Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="1e9de-113">Before you begin the following procedure, you should do the following:</span></span>

-   <span data-ttu-id="1e9de-114">Kopieren Sie das virtuelle Anwendungspaket, das Sie zum Erstellen des Paket Beschleunigers verwenden müssen, lokal auf dem Computer, auf dem der Sequencer ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1e9de-114">Copy the virtual application package that you must use to create the Package Accelerator locally to the computer running the Sequencer.</span></span>

-   <span data-ttu-id="1e9de-115">Kopieren Sie alle erforderlichen Installationsdateien, die dem virtuellen Anwendungspaket zugeordnet sind, auf den Computer, auf dem der Sequencer ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1e9de-115">Copy all required installation files associated with the virtual application package to the computer running the Sequencer.</span></span>



**<span data-ttu-id="1e9de-116">Wichtig</span><span class="sxs-lookup"><span data-stu-id="1e9de-116">Important</span></span>**  
<span data-ttu-id="1e9de-117">Disclaimer: Microsoft Application Virtualization Sequencer gibt Ihnen keine Lizenzrechte für die Softwareanwendung, die Sie zum Erstellen eines Paket Beschleunigers verwenden.</span><span class="sxs-lookup"><span data-stu-id="1e9de-117">Disclaimer: The Microsoft Application Virtualization Sequencer does not give you any license rights to the software application you are using to create a Package Accelerator.</span></span> <span data-ttu-id="1e9de-118">Sie müssen sich an alle Endnutzer-Lizenzbestimmungen für diese Anwendung halten.</span><span class="sxs-lookup"><span data-stu-id="1e9de-118">You must abide by all end user license terms for such application.</span></span> <span data-ttu-id="1e9de-119">Sie müssen sicherstellen, dass die Lizenzbestimmungen der Softwareanwendung es Ihnen ermöglichen, mithilfe von Application Virtualization Sequencer einen Paket Beschleuniger zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="1e9de-119">It is your responsibility to make sure the software application’s license terms allow you to create a Package Accelerator using Application Virtualization Sequencer.</span></span>



**<span data-ttu-id="1e9de-120">So erstellen Sie einen App-V-Paket Beschleuniger</span><span class="sxs-lookup"><span data-stu-id="1e9de-120">To create an App-V Package Accelerator</span></span>**

1.  <span data-ttu-id="1e9de-121">Klicken Sie zum Starten des App-v-Sequencers auf dem Computer, auf dem der APP-v-Sequenzer ausgeführt wird, auf **Start**  /  **Alle Programme**starten  /  **Microsoft Application Virtualization**  /  **Microsoft Application Virtualization Sequencer**.</span><span class="sxs-lookup"><span data-stu-id="1e9de-121">To start the App-V Sequencer, on the computer that is running the App-V Sequencer, click **Start** / **All Programs** / **Microsoft Application Virtualization** / **Microsoft Application Virtualization Sequencer**.</span></span>

2.  <span data-ttu-id="1e9de-122">Klicken Sie zum Starten des App-v-Assistenten zum **Erstellen von Paket Beschleunigern** im App-v-Sequenzer auf **Extras**, die  /  **Paket Beschleuniger erstellen**.</span><span class="sxs-lookup"><span data-stu-id="1e9de-122">To start the App-V **Create Package Accelerator** wizard, in the App-V Sequencer, click **Tools** / **Create Package Accelerator**.</span></span>

3.  <span data-ttu-id="1e9de-123">Klicken Sie auf der Seite **Paket auswählen** zum Angeben eines vorhandenen virtuellen Anwendungspakets, das zum Erstellen des Paket Beschleunigers verwendet werden soll, auf **Durchsuchen**, und suchen Sie das vorhandene virtuelle Anwendungspaket (SPRJ-Datei).</span><span class="sxs-lookup"><span data-stu-id="1e9de-123">On the **Select Package** page, to specify an existing virtual application package to use to create the Package Accelerator, click **Browse**, and locate the existing virtual application package (.sprj file).</span></span>

    **<span data-ttu-id="1e9de-124">Tipp</span><span class="sxs-lookup"><span data-stu-id="1e9de-124">Tip</span></span>**  
    <span data-ttu-id="1e9de-125">Kopieren Sie die Dateien, die dem virtuellen Anwendungspaket zugeordnet sind, das Sie lokal für den Computer verwenden möchten, auf dem der Sequencer ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1e9de-125">Copy the files associated with the virtual application package you plan to use locally to the computer running the Sequencer.</span></span>



~~~
Click **Next**.
~~~

4. <span data-ttu-id="1e9de-126">Klicken Sie auf der Seite **Installationsdateien** auf **Durchsuchen**, um den Ordner mit den Installationsdateien anzugeben, die Sie zum Erstellen des ursprünglichen virtuellen Anwendungspakets verwendet haben, und wählen Sie dann das Verzeichnis aus, das die Installationsdateien enthält.</span><span class="sxs-lookup"><span data-stu-id="1e9de-126">On the **Installation Files** page, to specify the folder that contains the installation files that you used to create the original virtual application package, click **Browse**, and then select the directory that contains the installation files.</span></span>

   **<span data-ttu-id="1e9de-127">Tipp</span><span class="sxs-lookup"><span data-stu-id="1e9de-127">Tip</span></span>**  
   <span data-ttu-id="1e9de-128">Kopieren Sie den Ordner, der die erforderlichen Installationsdateien enthält, auf den Computer, auf dem der Sequencer ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1e9de-128">Copy the folder that contains the required installation files to the computer running the Sequencer.</span></span>



~~~
If the application is already installed on the computer running the Sequencer, to specify the installation file, select **Files installed on local system**. To use this option, the application must already be installed in the default installation location.
~~~

5. <span data-ttu-id="1e9de-129">Überprüfen Sie auf der Seite **Gathering Information** die Dateien, die sich nicht in dem auf der Seite **Installationsdateien** dieses Assistenten angegebenen Speicherort befinden.</span><span class="sxs-lookup"><span data-stu-id="1e9de-129">On the **Gathering Information** page, review the files that were not found in the location specified on the **Installation Files** page of this wizard.</span></span> <span data-ttu-id="1e9de-130">Wenn die angezeigten Dateien nicht erforderlich sind, wählen Sie **diese Dateien entfernen**aus, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="1e9de-130">If the files displayed are not required, select **Remove these files**, and then click **Next**.</span></span> <span data-ttu-id="1e9de-131">Wenn die Dateien erforderlich sind, klicken Sie auf **zurück** , und kopieren Sie die erforderlichen Dateien in das auf der Seite **Installationsdateien** angegebene Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="1e9de-131">If the files are required, click **Previous** and copy the required files to the directory specified on the **Installation Files** page.</span></span>

   **<span data-ttu-id="1e9de-132">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="1e9de-132">Note</span></span>**  
   <span data-ttu-id="1e9de-133">Sie müssen entweder die nicht benötigten Dateien entfernen oder auf **zurück** klicken und die erforderlichen Dateien suchen, um zur nächsten Seite des Assistenten zu gelangen.</span><span class="sxs-lookup"><span data-stu-id="1e9de-133">You must either remove the unrequired files, or click **Previous** and locate the required files to advance to the next page of this wizard.</span></span>



6. <span data-ttu-id="1e9de-134">Überprüfen Sie auf der Seite **"Dateien auswählen** " sorgfältig die gefundenen Dateien, und löschen Sie alle Dateien, die aus dem Paket Beschleuniger entfernt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="1e9de-134">On the **Select Files** page, carefully review the files that were detected, and clear any file that should be removed from the Package Accelerator.</span></span> <span data-ttu-id="1e9de-135">Wählen Sie nur Dateien aus, die erforderlich sind, damit die Anwendung erfolgreich ausgeführt werden kann, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="1e9de-135">Select only files that are required for the application to run successfully, and then click **Next**.</span></span>

7. <span data-ttu-id="1e9de-136">Vergewissern Sie sich auf der Seite **Anwendungen überprüfen** , dass alle Installationsdateien angezeigt werden, die zum Erstellen des Pakets erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="1e9de-136">On the **Verify Applications** page, confirm that all installation files that are required to build the package are displayed.</span></span> <span data-ttu-id="1e9de-137">Wenn der Paket Beschleuniger zum Erstellen eines neuen Pakets verwendet wird, sind alle im Bereich **Anwendungen** angezeigten Installationsdateien erforderlich, um das Paket zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="1e9de-137">When the Package Accelerator is used to create a new package, all installation files displayed in the **Applications** pane are required to create the package.</span></span>

   <span data-ttu-id="1e9de-138">Falls erforderlich, klicken Sie auf **Hinzufügen**, um weitere Installationsprogrammdateien hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="1e9de-138">If necessary, to add additional Installer files, click **Add**.</span></span> <span data-ttu-id="1e9de-139">Wenn Sie nicht benötigte Installationsdateien entfernen möchten, wählen Sie die Installationsdatei aus, und klicken Sie dann auf **Löschen**.</span><span class="sxs-lookup"><span data-stu-id="1e9de-139">To remove unnecessary installation files, select the Installer file, and then click **Delete**.</span></span> <span data-ttu-id="1e9de-140">Wenn Sie die Eigenschaften bearbeiten möchten, die einem Installationsprogramm zugeordnet sind, klicken Sie auf **Bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="1e9de-140">To edit the properties associated with an installer, click **Edit**.</span></span> <span data-ttu-id="1e9de-141">Die in diesem Schritt angegebenen Installationsdateien sind erforderlich, wenn der Paket Beschleuniger zum Erstellen eines neuen virtuellen Anwendungspakets verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1e9de-141">The installation files specified in this step will be required when the Package Accelerator is used to create a new virtual application package.</span></span> <span data-ttu-id="1e9de-142">Nachdem Sie die angezeigten Informationen bestätigt haben, klicken Sie auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="1e9de-142">After you have confirmed the information displayed, click **Next**.</span></span>

8. <span data-ttu-id="1e9de-143">Klicken Sie auf der Seite **"Anleitungen auswählen** " auf **Durchsuchen**, um eine Datei anzugeben, die Informationen zur Funktionsweise des Paket Beschleunigers enthält.</span><span class="sxs-lookup"><span data-stu-id="1e9de-143">On the **Select Guidance** page, to specify a file that contains information about how the Package Accelerator, click **Browse**.</span></span> <span data-ttu-id="1e9de-144">Diese Datei kann beispielsweise Informationen dazu enthalten, wie der Computer, auf dem der Sequencer ausgeführt wird, konfiguriert werden soll, Anwendungs Voraussetzungs Informationen für Zielcomputer und allgemeine Hinweise.</span><span class="sxs-lookup"><span data-stu-id="1e9de-144">For example, this file can contain information about how the computer running the Sequencer should be configured, application prerequisite information for target computers, and general notes.</span></span> <span data-ttu-id="1e9de-145">Sie sollten alle erforderlichen Informationen für die erfolgreiche Anwendung des Paket Beschleunigers angeben.</span><span class="sxs-lookup"><span data-stu-id="1e9de-145">You should provide all required information for the Package Accelerator to be successfully applied.</span></span> <span data-ttu-id="1e9de-146">Die ausgewählte Datei muss im Rich-Text-Format (RTF) oder im Textdateiformat (txt) vorliegen.</span><span class="sxs-lookup"><span data-stu-id="1e9de-146">The file you select must be in rich text (.rtf) or text file (.txt) format.</span></span> <span data-ttu-id="1e9de-147">Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="1e9de-147">Click **Next**.</span></span>

9. <span data-ttu-id="1e9de-148">Klicken Sie auf der Seite **Paket Beschleuniger erstellen** auf **Durchsuchen** , um anzugeben, wo der Paket Beschleuniger gespeichert werden soll, und wählen Sie das Verzeichnis aus.</span><span class="sxs-lookup"><span data-stu-id="1e9de-148">On the **Create Package Accelerator** page, to specify where to save the Package Accelerator, click **Browse** and select the directory.</span></span>

10. <span data-ttu-id="1e9de-149">Klicken Sie auf der Seite **Fertigstellung** auf **Schließen**, um den Assistenten zum **Erstellen von Paket Beschleunigern** zu schließen.</span><span class="sxs-lookup"><span data-stu-id="1e9de-149">On the **Completion** page, to close the **Create Package Accelerator** wizard, click **Close**.</span></span>

   **<span data-ttu-id="1e9de-150">Wichtig</span><span class="sxs-lookup"><span data-stu-id="1e9de-150">Important</span></span>**  
   <span data-ttu-id="1e9de-151">Wenn Sie sicherstellen möchten, dass der Paket Beschleuniger so sicher wie möglich ist und der Herausgeber überprüft werden kann, wenn der Paket Beschleuniger angewendet wird, sollten Sie immer den Paket Beschleuniger digital signieren.</span><span class="sxs-lookup"><span data-stu-id="1e9de-151">To help ensure that the Package Accelerator is as secure as possible, and so that the publisher can be verified when the Package Accelerator is applied, you should always digitally sign the Package Accelerator.</span></span>



## <span data-ttu-id="1e9de-152">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="1e9de-152">Related topics</span></span>


<span data-ttu-id="1e9de-153">Konfigurieren des Application Virtualization Sequencer (app-v 4,6 SP1) so wird es [gemacht: Anwenden eines Paket Beschleunigers zum Erstellen eines virtuellen Anwendungspakets (app-v 4,6 SP1)](how-to-apply-a-package-accelerator-to-create-a-virtual-application-package---app-v-46-sp1-.md)</span><span class="sxs-lookup"><span data-stu-id="1e9de-153">Configuring the Application Virtualization Sequencer (App-V 4.6 SP1) [How to Apply a Package Accelerator to Create a Virtual Application Package (App-V 4.6 SP1)](how-to-apply-a-package-accelerator-to-create-a-virtual-application-package---app-v-46-sp1-.md)</span></span>









