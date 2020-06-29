---
title: So erstellen Sie einen Package Accelerator
description: So erstellen Sie einen Package Accelerator
author: dansimp
ms.assetid: dfe305e5-7cf8-498f-9581-4805ffc722bd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0710bff5e5ea420119ac3c395c2e8917f7c582dd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805606"
---
# <span data-ttu-id="ff4b1-103">So erstellen Sie einen Package Accelerator</span><span class="sxs-lookup"><span data-stu-id="ff4b1-103">How to Create a Package Accelerator</span></span>


<span data-ttu-id="ff4b1-104">App-V 5,0-Paket Beschleuniger generieren automatisch neue virtuelle Anwendungspakete.</span><span class="sxs-lookup"><span data-stu-id="ff4b1-104">App-V 5.0 package accelerators automatically generate new virtual application packages.</span></span>

**<span data-ttu-id="ff4b1-105">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="ff4b1-105">Note</span></span>**  
<span data-ttu-id="ff4b1-106">Sie können PowerShell zum Erstellen eines Paket Beschleunigers verwenden.</span><span class="sxs-lookup"><span data-stu-id="ff4b1-106">You can use PowerShell to create a package accelerator.</span></span> <span data-ttu-id="ff4b1-107">Weitere Informationen finden Sie unter [Erstellen eines Paket Beschleunigers mithilfe von PowerShell](how-to-create-a-package-accelerator-by-using-powershell.md).</span><span class="sxs-lookup"><span data-stu-id="ff4b1-107">For more information see [How to Create a Package Accelerator by Using PowerShell](how-to-create-a-package-accelerator-by-using-powershell.md).</span></span>



<span data-ttu-id="ff4b1-108">Gehen Sie wie folgt vor, um einen Paket Beschleuniger zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="ff4b1-108">Use the following procedure to create a package accelerator.</span></span>

**<span data-ttu-id="ff4b1-109">Wichtig</span><span class="sxs-lookup"><span data-stu-id="ff4b1-109">Important</span></span>**  
<span data-ttu-id="ff4b1-110">Paket Beschleuniger können Kennwort-und benutzerspezifische Informationen enthalten.</span><span class="sxs-lookup"><span data-stu-id="ff4b1-110">Package Accelerators can contain password and user-specific information.</span></span> <span data-ttu-id="ff4b1-111">Daher müssen Sie Paket Beschleuniger und die zugehörigen Installationsmedien an einem sicheren Speicherort speichern, und Sie sollten den Paket Beschleuniger nach der Erstellung digital signieren, damit der Herausgeber überprüft werden kann, wenn der App-V 5,0-Paket Beschleuniger angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="ff4b1-111">Therefore you must save Package Accelerators and the associated installation media in a secure location, and you should digitally sign the Package Accelerator after you create it so that the publisher can be verified when the App-V 5.0 Package Accelerator is applied.</span></span>



**<span data-ttu-id="ff4b1-112">Wichtig</span><span class="sxs-lookup"><span data-stu-id="ff4b1-112">Important</span></span>**  
<span data-ttu-id="ff4b1-113">Bevor Sie mit der folgenden Vorgehensweise beginnen, sollten Sie die folgenden Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="ff4b1-113">Before you begin the following procedure, you should perform the following:</span></span>

-   <span data-ttu-id="ff4b1-114">Kopieren Sie das virtuelle Anwendungspaket, das Sie zum Erstellen des Paket Beschleunigers verwenden, lokal auf dem Computer, auf dem der Sequencer ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ff4b1-114">Copy the virtual application package that you will use to create the package accelerator locally to the computer running the sequencer.</span></span>

-   <span data-ttu-id="ff4b1-115">Kopieren Sie alle erforderlichen Installationsdateien, die dem virtuellen Anwendungspaket zugeordnet sind, auf den Computer, auf dem der Sequencer ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ff4b1-115">Copy all required installation files associated with the virtual application package to the computer running the sequencer.</span></span>



**<span data-ttu-id="ff4b1-116">So erstellen Sie einen Paket Beschleuniger</span><span class="sxs-lookup"><span data-stu-id="ff4b1-116">To create a package accelerator</span></span>**

1.  **<span data-ttu-id="ff4b1-117">Wichtig</span><span class="sxs-lookup"><span data-stu-id="ff4b1-117">Important</span></span>**  
    <span data-ttu-id="ff4b1-118">Der App-V 5,0-Sequenzer gewährt der Softwareanwendung, die Sie zum Erstellen des Paket Beschleunigers verwenden, keine Lizenzrechte.</span><span class="sxs-lookup"><span data-stu-id="ff4b1-118">The App-V 5.0 Sequencer does not grant any license rights to the software application you are using to create the Package Accelerator.</span></span> <span data-ttu-id="ff4b1-119">Sie müssen sich an alle Endbenutzer-Lizenzbestimmungen für die von Ihnen verwendete Anwendung halten.</span><span class="sxs-lookup"><span data-stu-id="ff4b1-119">You must abide by all end user license terms for the application you are using.</span></span> <span data-ttu-id="ff4b1-120">Sie müssen sicherstellen, dass die Lizenzbestimmungen der Softwareanwendung es Ihnen ermöglichen, mithilfe von App-V 5,0 Sequencer einen Paket Beschleuniger zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="ff4b1-120">It is your responsibility to make sure the software application’s license terms allow you to create a Package Accelerator using App-V 5.0 Sequencer.</span></span>



~~~
To start the App-V 5.0 sequencer, on the computer that is running the sequencer, click **Start** / **All Programs** / **Microsoft Application Virtualization** / **Microsoft Application Virtualization Sequencer**.
~~~

2. <span data-ttu-id="ff4b1-121">Wenn Sie den App-v 5,0-Assistenten zum **Erstellen von Paket Beschleunigern** starten möchten, klicken Sie in der APP-v 5,0-Sequenzer-Konsole auf **Extras**  /  **Beschleuniger erstellen**.</span><span class="sxs-lookup"><span data-stu-id="ff4b1-121">To start the App-V 5.0 **Create Package Accelerator** wizard, in the App-V 5.0 sequencer console, click **Tools** / **Create Accelerator**.</span></span>

3. <span data-ttu-id="ff4b1-122">Klicken Sie auf der Seite **Paket auswählen** zum Angeben eines vorhandenen virtuellen Anwendungspakets, das zum Erstellen des Paket Beschleunigers verwendet werden soll, auf **Durchsuchen**, und suchen Sie das vorhandene virtuelle Anwendungspaket (AppV-Datei).</span><span class="sxs-lookup"><span data-stu-id="ff4b1-122">On the **Select Package** page, to specify an existing virtual application package to use to create the Package Accelerator, click **Browse**, and locate the existing virtual application package (.appv file).</span></span>

   **<span data-ttu-id="ff4b1-123">Tipp</span><span class="sxs-lookup"><span data-stu-id="ff4b1-123">Tip</span></span>**  
   <span data-ttu-id="ff4b1-124">Kopieren Sie die Dateien, die dem virtuellen Anwendungspaket zugeordnet sind, das Sie lokal für den Computer verwenden möchten, auf dem der Sequencer ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ff4b1-124">Copy the files associated with the virtual application package you plan to use locally to the computer running the Sequencer.</span></span>



~~~
Click **Next**.
~~~

4. <span data-ttu-id="ff4b1-125">Klicken Sie auf der Seite **Installationsdateien** auf **Durchsuchen**, um den Ordner mit den Installationsdateien anzugeben, die Sie zum Erstellen des ursprünglichen virtuellen Anwendungspakets verwendet haben, und wählen Sie dann das Verzeichnis aus, das die Installationsdateien enthält.</span><span class="sxs-lookup"><span data-stu-id="ff4b1-125">On the **Installation Files** page, to specify the folder that contains the installation files that you used to create the original virtual application package, click **Browse**, and then select the directory that contains the installation files.</span></span>

   **<span data-ttu-id="ff4b1-126">Tipp</span><span class="sxs-lookup"><span data-stu-id="ff4b1-126">Tip</span></span>**  
   <span data-ttu-id="ff4b1-127">Kopieren Sie den Ordner, der die erforderlichen Installationsdateien enthält, auf den Computer, auf dem der Sequencer ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ff4b1-127">Copy the folder that contains the required installation files to the computer running the Sequencer.</span></span>



5. <span data-ttu-id="ff4b1-128">Wenn die Anwendung bereits auf dem Computer installiert ist, auf dem der Sequencer ausgeführt wird, wählen Sie im **lokalen System installierte Dateien**aus, um die Installationsdatei anzugeben.</span><span class="sxs-lookup"><span data-stu-id="ff4b1-128">If the application is already installed on the computer running the sequencer, to specify the installation file, select **Files installed on local system**.</span></span> <span data-ttu-id="ff4b1-129">Um diese Option verwenden zu können, muss die Anwendung bereits im Standardinstallationspfad installiert sein.</span><span class="sxs-lookup"><span data-stu-id="ff4b1-129">To use this option, the application must already be installed in the default installation location.</span></span>

6. <span data-ttu-id="ff4b1-130">Überprüfen Sie auf der Seite **Gathering Information** die Dateien, die sich nicht in dem auf der Seite **Installationsdateien** dieses Assistenten angegebenen Speicherort befinden.</span><span class="sxs-lookup"><span data-stu-id="ff4b1-130">On the **Gathering Information** page, review the files that were not found in the location specified on the **Installation Files** page of this wizard.</span></span> <span data-ttu-id="ff4b1-131">Wenn die angezeigten Dateien nicht erforderlich sind, wählen Sie **diese Dateien entfernen**aus, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="ff4b1-131">If the files displayed are not required, select **Remove these files**, and then click **Next**.</span></span> <span data-ttu-id="ff4b1-132">Wenn die Dateien erforderlich sind, klicken Sie auf **zurück** , und kopieren Sie die erforderlichen Dateien in das auf der Seite **Installationsdateien** angegebene Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="ff4b1-132">If the files are required, click **Previous** and copy the required files to the directory specified on the **Installation Files** page.</span></span>

   **<span data-ttu-id="ff4b1-133">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="ff4b1-133">Note</span></span>**  
   <span data-ttu-id="ff4b1-134">Sie müssen entweder die nicht benötigten Dateien entfernen oder auf **zurück** klicken und die erforderlichen Dateien suchen, um zur nächsten Seite des Assistenten zu gelangen.</span><span class="sxs-lookup"><span data-stu-id="ff4b1-134">You must either remove the unrequired files, or click **Previous** and locate the required files to advance to the next page of this wizard.</span></span>



7. <span data-ttu-id="ff4b1-135">Überprüfen Sie auf der Seite **"Dateien auswählen** " sorgfältig die gefundenen Dateien, und löschen Sie alle Dateien, die aus dem Paket Beschleuniger entfernt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="ff4b1-135">On the **Select Files** page, carefully review the files that were detected, and clear any file that should be removed from the package accelerator.</span></span> <span data-ttu-id="ff4b1-136">Wählen Sie nur Dateien aus, die erforderlich sind, damit die Anwendung erfolgreich ausgeführt werden kann, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="ff4b1-136">Select only files that are required for the application to run successfully, and then click **Next**.</span></span>

8. <span data-ttu-id="ff4b1-137">Vergewissern Sie sich auf der Seite **Anwendungen überprüfen** , dass alle Installationsdateien angezeigt werden, die zum Erstellen des Pakets erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="ff4b1-137">On the **Verify Applications** page, confirm that all installation files that are required to build the package are displayed.</span></span> <span data-ttu-id="ff4b1-138">Wenn der Paket Beschleuniger zum Erstellen eines neuen Pakets verwendet wird, sind alle im Bereich **Anwendungen** angezeigten Installationsdateien erforderlich, um das Paket zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="ff4b1-138">When the Package Accelerator is used to create a new package, all installation files displayed in the **Applications** pane are required to create the package.</span></span>

   <span data-ttu-id="ff4b1-139">Falls erforderlich, klicken Sie auf **Hinzufügen**, um weitere Installationsprogrammdateien hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="ff4b1-139">If necessary, to add additional Installer files, click **Add**.</span></span> <span data-ttu-id="ff4b1-140">Wenn Sie nicht benötigte Installationsdateien entfernen möchten, wählen Sie die Installationsdatei aus, und klicken Sie dann auf **Löschen**.</span><span class="sxs-lookup"><span data-stu-id="ff4b1-140">To remove unnecessary installation files, select the Installer file, and then click **Delete**.</span></span> <span data-ttu-id="ff4b1-141">Wenn Sie die Eigenschaften bearbeiten möchten, die einem Installationsprogramm zugeordnet sind, klicken Sie auf **Bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="ff4b1-141">To edit the properties associated with an installer, click **Edit**.</span></span> <span data-ttu-id="ff4b1-142">Die in diesem Schritt angegebenen Installationsdateien sind erforderlich, wenn der Paket Beschleuniger zum Erstellen eines neuen virtuellen Anwendungspakets verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ff4b1-142">The installation files specified in this step will be required when the Package Accelerator is used to create a new virtual application package.</span></span> <span data-ttu-id="ff4b1-143">Nachdem Sie die angezeigten Informationen bestätigt haben, klicken Sie auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="ff4b1-143">After you have confirmed the information displayed, click **Next**.</span></span>

9. <span data-ttu-id="ff4b1-144">Klicken Sie auf der Seite **"Anleitungen auswählen** " auf **Durchsuchen**, um eine Datei anzugeben, die Informationen zur Funktionsweise des Paket Beschleunigers enthält.</span><span class="sxs-lookup"><span data-stu-id="ff4b1-144">On the **Select Guidance** page, to specify a file that contains information about how the Package Accelerator, click **Browse**.</span></span> <span data-ttu-id="ff4b1-145">Diese Datei kann beispielsweise Informationen dazu enthalten, wie der Computer, auf dem der Sequencer ausgeführt wird, konfiguriert werden soll, Anwendungs Voraussetzungs Informationen für Zielcomputer und allgemeine Hinweise.</span><span class="sxs-lookup"><span data-stu-id="ff4b1-145">For example, this file can contain information about how the computer running the Sequencer should be configured, application prerequisite information for target computers, and general notes.</span></span> <span data-ttu-id="ff4b1-146">Sie sollten alle erforderlichen Informationen für die erfolgreiche Anwendung des Paket Beschleunigers angeben.</span><span class="sxs-lookup"><span data-stu-id="ff4b1-146">You should provide all required information for the Package Accelerator to be successfully applied.</span></span> <span data-ttu-id="ff4b1-147">Die ausgewählte Datei muss im Rich-Text-Format (RTF) oder im Textdateiformat (txt) vorliegen.</span><span class="sxs-lookup"><span data-stu-id="ff4b1-147">The file you select must be in rich text (.rtf) or text file (.txt) format.</span></span> <span data-ttu-id="ff4b1-148">Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="ff4b1-148">Click **Next**.</span></span>

10. <span data-ttu-id="ff4b1-149">Klicken Sie auf der Seite **Paket Beschleuniger erstellen** auf **Durchsuchen** , um anzugeben, wo der Paket Beschleuniger gespeichert werden soll, und wählen Sie das Verzeichnis aus.</span><span class="sxs-lookup"><span data-stu-id="ff4b1-149">On the **Create Package Accelerator** page, to specify where to save the Package Accelerator, click **Browse** and select the directory.</span></span>

11. <span data-ttu-id="ff4b1-150">Klicken Sie auf der Seite **Fertigstellung** auf **Schließen**, um den Assistenten zum **Erstellen von Paket Beschleunigern** zu schließen.</span><span class="sxs-lookup"><span data-stu-id="ff4b1-150">On the **Completion** page, to close the **Create Package Accelerator** wizard, click **Close**.</span></span>

   **<span data-ttu-id="ff4b1-151">Wichtig</span><span class="sxs-lookup"><span data-stu-id="ff4b1-151">Important</span></span>**  
   <span data-ttu-id="ff4b1-152">Wenn Sie sicherstellen möchten, dass der Paket Beschleuniger so sicher wie möglich ist und der Herausgeber überprüft werden kann, wenn der Paket Beschleuniger angewendet wird, sollten Sie immer den Paket Beschleuniger digital signieren.</span><span class="sxs-lookup"><span data-stu-id="ff4b1-152">To help ensure that the package accelerator is as secure as possible, and so that the publisher can be verified when the package accelerator is applied, you should always digitally sign the package accelerator.</span></span>



~~~
**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## <span data-ttu-id="ff4b1-153">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="ff4b1-153">Related topics</span></span>


[<span data-ttu-id="ff4b1-154">Vorgänge für App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="ff4b1-154">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

[<span data-ttu-id="ff4b1-155">So erstellen Sie ein virtuelles Anwendungspaket mit einem App-V Package Accelerator</span><span class="sxs-lookup"><span data-stu-id="ff4b1-155">How to Create a Virtual Application Package Using an App-V Package Accelerator</span></span>](how-to-create-a-virtual-application-package-using-an-app-v-package-accelerator.md)









