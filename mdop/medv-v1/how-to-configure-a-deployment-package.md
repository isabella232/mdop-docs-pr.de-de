---
title: So konfigurieren Sie ein Bereitstellungspaket
description: So konfigurieren Sie ein Bereitstellungspaket
author: dansimp
ms.assetid: 748272a1-6af2-476e-a3f1-87435b8e94b1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: aba5e91a4da92f9e51a5ccc70502658ae724d76f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811461"
---
# <span data-ttu-id="57949-103">So konfigurieren Sie ein Bereitstellungspaket</span><span class="sxs-lookup"><span data-stu-id="57949-103">How to Configure a Deployment Package</span></span>


<span data-ttu-id="57949-104">Der Verpackungs-Assistent führt Sie durch die Erstellung eines Pakets, indem Sie einen Ordner auf dem lokalen Computer erstellen und alle erforderlichen Installationsdateien in den einzelnen Ordner übertragen.</span><span class="sxs-lookup"><span data-stu-id="57949-104">The Packaging wizard walks you through the creation of a package by creating a folder on your local computer and transferring all the required installation files to the single folder.</span></span> <span data-ttu-id="57949-105">Der Inhalt des Ordners kann dann zur Verteilung auf mehrere Wechselmedienlaufwerke verschoben werden.</span><span class="sxs-lookup"><span data-stu-id="57949-105">The contents of the folder can then be moved to multiple removable media drives for distribution.</span></span>

**<span data-ttu-id="57949-106">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="57949-106">Note</span></span>**  
<span data-ttu-id="57949-107">Ein einzelnes Paket kann keine Installationsdateien für x86-und x64-Systeme enthalten.</span><span class="sxs-lookup"><span data-stu-id="57949-107">A single package cannot contain installation files for both x86 and x64 systems.</span></span>



## <span data-ttu-id="57949-108">Erstellen eines Bereitstellungspakets</span><span class="sxs-lookup"><span data-stu-id="57949-108">How to Create a Deployment Package</span></span>


**<span data-ttu-id="57949-109">So erstellen Sie ein Bereitstellungspaket</span><span class="sxs-lookup"><span data-stu-id="57949-109">To create a deployment package</span></span>**

1. <span data-ttu-id="57949-110">Überprüfen Sie im Modul **Bilder** , dass Sie mindestens ein lokal verpacktes Bild erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="57949-110">Verify in the **Images** module that you have created at least one local packed image.</span></span>

2. <span data-ttu-id="57949-111">Klicken Sie im Menü **Extras** auf **Verpackungs-Assistent**.</span><span class="sxs-lookup"><span data-stu-id="57949-111">On the **Tools** menu, select **Packaging wizard**.</span></span>

3. <span data-ttu-id="57949-112">Klicken Sie auf der Willkommensseite des **Verpackungs-Assistenten** auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="57949-112">On the **Packaging wizard** welcome page, click **Next**.</span></span>

4. <span data-ttu-id="57949-113">Aktivieren Sie auf der Seite **Workspace Image** das Kontrollkästchen **Bild in das Paket einbeziehen** , um ein Bild in das Paket einzubeziehen.</span><span class="sxs-lookup"><span data-stu-id="57949-113">On the **Workspace Image** page, select the **Include image in the package** check box to include an image in the package.</span></span>

   <span data-ttu-id="57949-114">Das Feld " **Bild** " ist aktiviert.</span><span class="sxs-lookup"><span data-stu-id="57949-114">The **Image** field is enabled.</span></span>

   **<span data-ttu-id="57949-115">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="57949-115">Note</span></span>**  
   <span data-ttu-id="57949-116">In einem MED-V-Paket ist kein Bild erforderlich; das Paket kann ohne ein Bild erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="57949-116">An image is not required in a MED-V package; the package can be created without an image.</span></span> <span data-ttu-id="57949-117">In einem solchen Fall sollte das Bild auf den Server hochgeladen werden, damit es später über das Netzwerk auf den Client heruntergeladen oder in einen Ordner mit Vorstufen für Bilder verschoben werden kann.</span><span class="sxs-lookup"><span data-stu-id="57949-117">In such a case, the image should be uploaded to the server so that it can later be downloaded over the network to the client, or pushed to an image pre-stage folder.</span></span>



5. <span data-ttu-id="57949-118">Klicken Sie **auf die** Bildliste, um alle verfügbaren Bilder anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="57949-118">Click the **Image** list to view all available images.</span></span> <span data-ttu-id="57949-119">Wählen Sie das Bild aus, das in das Paket kopiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="57949-119">Select the image to be copied to the package.</span></span> <span data-ttu-id="57949-120">Klicken Sie auf **Aktualisieren** , um die Liste der verfügbaren Bilder zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="57949-120">Click **Refresh** to refresh the list of available images.</span></span>

6. <span data-ttu-id="57949-121">Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="57949-121">Click **Next**.</span></span>

7. <span data-ttu-id="57949-122">Wählen Sie auf der Seite **Med-v-Installationseinstellungen** die Med-v-Installationsdatei aus, indem Sie eine der folgenden Aktionen ausführen:</span><span class="sxs-lookup"><span data-stu-id="57949-122">On the **MED-V Installation Settings** page, select the MED-V installation file by doing one of the following:</span></span>

   -   <span data-ttu-id="57949-123">Geben Sie im Feld **MED-V-Installationsdatei** den vollständigen Pfad zu dem Verzeichnis ein, in dem sich die Installationsdatei befindet.</span><span class="sxs-lookup"><span data-stu-id="57949-123">In the **MED-V installation file** field, type the full path to the directory where the installation file is located.</span></span>

   -   <span data-ttu-id="57949-124">Klicken Sie auf **...** , um zu dem Verzeichnis zu navigieren, in dem sich die Installationsdatei befindet.</span><span class="sxs-lookup"><span data-stu-id="57949-124">Click **...** to browse to the directory where the installation file is located.</span></span>

   **<span data-ttu-id="57949-125">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="57949-125">Note</span></span>**  
   <span data-ttu-id="57949-126">Dieses Feld ist obligatorisch, und der Assistent wird nicht ohne gültigen Dateinamen fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="57949-126">This field is mandatory, and the wizard will not continue without a valid file name.</span></span>



8. <span data-ttu-id="57949-127">Geben Sie im Feld **Serveradresse** den Servernamen oder die IP-Adresse ein.</span><span class="sxs-lookup"><span data-stu-id="57949-127">In the **Server address** field, type the server name or IP address.</span></span>

9. <span data-ttu-id="57949-128">Geben Sie im Feld **Server Port** den Serverport ein.</span><span class="sxs-lookup"><span data-stu-id="57949-128">In the **Server port** field, type the server port.</span></span>

10. <span data-ttu-id="57949-129">Aktivieren Sie das Kontrollkästchen **Server wird über HTTPS zugegriffen** , um eine HTTPS-Verbindung zum Herstellen einer Verbindung mit dem Server zu fordern.</span><span class="sxs-lookup"><span data-stu-id="57949-129">Select the **Server is accessed using https** check box to require an https connection to connect to the server.</span></span>

11. <span data-ttu-id="57949-130">Führen Sie eine der folgenden Aktionen aus:</span><span class="sxs-lookup"><span data-stu-id="57949-130">Do one of the following:</span></span>

    -   <span data-ttu-id="57949-131">Klicken Sie auf **Standardinstallationseinstellungen**, und klicken Sie dann auf **weiter** , um fortzufahren, und behalten Sie die Standardeinstellungen bei.</span><span class="sxs-lookup"><span data-stu-id="57949-131">Click **Default installation settings**, and then click **Next** to continue and leave the default settings.</span></span>

    -   <span data-ttu-id="57949-132">Klicken Sie auf **benutzerdefinierte Installationseinstellungen**, und klicken Sie dann auf **weiter** , um die Installationseinstellungen anzupassen.</span><span class="sxs-lookup"><span data-stu-id="57949-132">Click **Custom installation settings**, and then click **Next** to customize the installation settings.</span></span>

        1.  <span data-ttu-id="57949-133">Geben Sie auf der Seite **benutzerdefinierte Einstellungen für die Med-v-Installation** im Feld **Installationsordner** den Pfad des Ordners ein, in dem die Med-v-Dateien auf dem Hostcomputer installiert werden.</span><span class="sxs-lookup"><span data-stu-id="57949-133">On the **MED-V Installation Custom Settings** page, in the **Installation folder** field, type the path of the folder where the MED-V files will be installed on the host computer.</span></span>

            **<span data-ttu-id="57949-134">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="57949-134">Note</span></span>**  
            <span data-ttu-id="57949-135">Es wird empfohlen, Variablen im Pfad anstelle von Konstanten zu verwenden, die von Computer zu Computer unterschiedlich sein können.</span><span class="sxs-lookup"><span data-stu-id="57949-135">It is recommended to use variables in the path rather than constants, which might vary from computer to computer.</span></span>

            <span data-ttu-id="57949-136">Verwenden Sie beispielsweise *%ProgramFiles%\\MED-V* anstelle von *c:\\MED-V*.</span><span class="sxs-lookup"><span data-stu-id="57949-136">For example, use *%ProgramFiles%\\MED-V* instead of *c:\\MED-V*.</span></span>



    ~~~
    2.  In the **Virtual machines images folder** field, type the path of the folder where the virtual images files will be installed on the host computer.

        **Note**  
        If you are using image pre-staging, this is the image pre-stage folder where the image is located.



    3.  In the **Minimal required RAM** field, enter the RAM required to install a MED-V package. If the user installing the MED-V package does not have the minimal required RAM, the installation will fail.

    4.  Select the **Install the MED-V management application** check box to include the MED-V management console application in the installation.

    5.  Select the **Create a shortcut to MED-V on the desktop** check box to create a shortcut to MED-V on the host's desktop.

    6.  Select the **Start automatically on computer startup** check box to start MED-V automatically on startup.

    7.  Click **Next**.
    ~~~

12. <span data-ttu-id="57949-137">Aktivieren Sie auf der Seite **Zusätzliche Installationen** das Kontrollkästchen **Installation der Virtualisierungssoftware einbeziehen** , um die Installation von Virtual PC in das Paket einzubeziehen.</span><span class="sxs-lookup"><span data-stu-id="57949-137">On the **Additional Installations** page, select the **Include installation of virtualization software** check box to include the Virtual PC installation in the package.</span></span>

    <span data-ttu-id="57949-138">Das Feld " **Installationsdatei** " ist aktiviert.</span><span class="sxs-lookup"><span data-stu-id="57949-138">The **Installation file** field is enabled.</span></span> <span data-ttu-id="57949-139">Geben Sie den vollständigen Pfad der Installationsdatei für die Virtualisierungssoftware ein, oder klicken Sie auf **...** , um das Verzeichnis zu durchsuchen.</span><span class="sxs-lookup"><span data-stu-id="57949-139">Type the full path of the virtualization software installation file, or click **...** to browse to the directory.</span></span>

13. <span data-ttu-id="57949-140">Aktivieren Sie das Kontrollkästchen **Installation von Virtual PC QFE einbeziehen** , um die Installation des Virtual PC-Updates in das Paket einzubeziehen.</span><span class="sxs-lookup"><span data-stu-id="57949-140">Select the **Include installation of Virtual PC QFE** check box to include Virtual PC update installation in the package.</span></span>

    <span data-ttu-id="57949-141">Das Feld " **Installationsdatei** " ist aktiviert.</span><span class="sxs-lookup"><span data-stu-id="57949-141">The **Installation file** field is enabled.</span></span> <span data-ttu-id="57949-142">Geben Sie den vollständigen Pfad der Installationsdatei für das Virtual PC-Update ein, oder klicken Sie auf **...** , um zum Verzeichnis zu wechseln.</span><span class="sxs-lookup"><span data-stu-id="57949-142">Type the full path of the Virtual PC update installation file, or click **...** to browse to the directory.</span></span>

14. <span data-ttu-id="57949-143">Aktivieren Sie das Kontrollkästchen **Installation von Microsoft .NET Framework 2,0** , um die Installation von Microsoft .NET Framework 2,0 in das Paket einzubeziehen.</span><span class="sxs-lookup"><span data-stu-id="57949-143">Select the **Include installation of Microsoft .NET Framework 2.0** check box to include the Microsoft .NET Framework 2.0 installation in the package.</span></span>

    <span data-ttu-id="57949-144">Das Feld " **Installationsdatei** " ist aktiviert.</span><span class="sxs-lookup"><span data-stu-id="57949-144">The **Installation file** field is enabled.</span></span> <span data-ttu-id="57949-145">Geben Sie den vollständigen Pfad der Installationsdatei für Microsoft .NET Framework 2,0 ein, oder klicken Sie auf **...** , um zum Verzeichnis zu navigieren.</span><span class="sxs-lookup"><span data-stu-id="57949-145">Type the full path of the Microsoft .NET Framework 2.0 installation file, or click **...** to browse to the directory.</span></span>

15. <span data-ttu-id="57949-146">Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="57949-146">Click **Next**.</span></span>

16. <span data-ttu-id="57949-147">Wählen Sie auf der Seite **Finalize** den Speicherort aus, an dem das Paket gespeichert werden soll, indem Sie eine der folgenden Aktionen ausführen:</span><span class="sxs-lookup"><span data-stu-id="57949-147">On the **Finalize** page, select the location where the package should be saved by doing one of the following:</span></span>

    -   <span data-ttu-id="57949-148">Geben Sie im Feld **Paket Ziel** den vollständigen Pfad zu dem Verzeichnis ein, in dem das Paket gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="57949-148">In the **Package destination** field, type the full path to the directory where the package should be saved.</span></span>

    -   <span data-ttu-id="57949-149">Klicken Sie auf **...** , um zu dem Verzeichnis zu navigieren, in dem die Installationsdateien gespeichert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="57949-149">Click **...** to browse to the directory where the installation files should be saved.</span></span>

    **<span data-ttu-id="57949-150">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="57949-150">Note</span></span>**  
    <span data-ttu-id="57949-151">Das Erstellen des Pakets kann mehr Speicherplatz als die tatsächliche Paketgröße beanspruchen.</span><span class="sxs-lookup"><span data-stu-id="57949-151">Building the package might consume more space than the actual package size.</span></span> <span data-ttu-id="57949-152">Es wird daher empfohlen, das Paket auf der Festplatte zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="57949-152">It is therefore recommended to build the package on the hard drive.</span></span> <span data-ttu-id="57949-153">Nachdem das Paket erstellt wurde, kann es auf den USB-Anschluss kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="57949-153">After the package is created, it can then be copied to the USB.</span></span>



17. <span data-ttu-id="57949-154">Geben Sie im Feld **Paketname** einen Namen für das Paket ein.</span><span class="sxs-lookup"><span data-stu-id="57949-154">In the **Package name** field, enter a name for the package.</span></span>

18. <span data-ttu-id="57949-155">Klicken Sie auf **Fertig stellen** , um das Paket zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="57949-155">Click **Finish** to create the package.</span></span>

    <span data-ttu-id="57949-156">Das Paket wird erstellt.</span><span class="sxs-lookup"><span data-stu-id="57949-156">The package is created.</span></span> <span data-ttu-id="57949-157">Dies kann einige Minuten dauern.</span><span class="sxs-lookup"><span data-stu-id="57949-157">This might take several minutes.</span></span>

    <span data-ttu-id="57949-158">Nachdem das Paket erstellt wurde, wird eine Meldung angezeigt, in der Sie darüber informiert werden, dass es erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="57949-158">After the package is created, a message appears notifying you that it has been completed successfully.</span></span>

**<span data-ttu-id="57949-159">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="57949-159">Note</span></span>**  
<span data-ttu-id="57949-160">Wenn Sie alle Dateien lokal und nicht direkt auf dem Wechselmedium gespeichert haben, stellen Sie sicher, dass Sie nur den Inhalt des Ordners und nicht den Ordner selbst auf die Wechselmedien kopieren.</span><span class="sxs-lookup"><span data-stu-id="57949-160">If you saved all the files locally, and not directly on the removable media, ensure that you copy only the contents of the folder and not the folder itself to the removable media.</span></span>



**<span data-ttu-id="57949-161">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="57949-161">Note</span></span>**  
<span data-ttu-id="57949-162">Die Wechselmedien müssen groß genug sein, damit der Inhalt des Pakets maximal drei Viertel des Speichers der Wechselmedien beansprucht.</span><span class="sxs-lookup"><span data-stu-id="57949-162">The removable media must be large enough so that the package contents consume a maximum of only three-quarters of the removable media's memory.</span></span>



**<span data-ttu-id="57949-163">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="57949-163">Note</span></span>**  
<span data-ttu-id="57949-164">Beim Erstellen des Pakets ist möglicherweise eine bis zu doppelte Größe der tatsächlichen Paketgröße erforderlich, wenn der Build abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="57949-164">When creating the package, up to double the size of the actual package size might be required when the build is complete.</span></span>



## <span data-ttu-id="57949-165">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="57949-165">Related topics</span></span>


[<span data-ttu-id="57949-166">Erstellen eines MED-V-Images</span><span class="sxs-lookup"><span data-stu-id="57949-166">Creating a MED-V Image</span></span>](creating-a-med-v-image.md)









