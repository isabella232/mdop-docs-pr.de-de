---
title: So konvertieren Sie ein Paket, das in einer früheren Version von App-V erstellt wurde
description: So konvertieren Sie ein Paket, das in einer früheren Version von App-V erstellt wurde
author: dansimp
ms.assetid: 3366d399-2891-491d-8de1-f8cfdf39bbab
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 402e64e3bdbc55eea1edb91d070bb7ebb11c912b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805666"
---
# <span data-ttu-id="9794d-103">So konvertieren Sie ein Paket, das in einer früheren Version von App-V erstellt wurde</span><span class="sxs-lookup"><span data-stu-id="9794d-103">How to Convert a Package Created in a Previous Version of App-V</span></span>


<span data-ttu-id="9794d-104">Sie können das Paket Konverter-Dienstprogrammverwenden, um virtuelle Anwendungspakete zu aktualisieren, die mit früheren Versionen von App-V erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="9794d-104">You can use the package converter utility to upgrade virtual application packages that have been created with previous versions of App-V.</span></span>

**<span data-ttu-id="9794d-105">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="9794d-105">Note</span></span>**  
<span data-ttu-id="9794d-106">Wenn Sie einen Computer mit einer 64-Bit-Architektur ausführen, müssen Sie die x86-Version von PowerShell verwenden.</span><span class="sxs-lookup"><span data-stu-id="9794d-106">If you are running a computer with a 64-bit architecture, you must use the x86 version of PowerShell.</span></span>



<span data-ttu-id="9794d-107">Der Paket Konverter kann nur Pakete direkt konvertieren, die mit dem App-V 4,5-Sequenzer oder einer nachfolgenden Version erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="9794d-107">The package converter can only directly convert packages that were created by using the App-V 4.5 sequencer or a subsequent version.</span></span> <span data-ttu-id="9794d-108">Pakete, die mit einer Version vor App-v 4,5 erstellt wurden, müssen vor der Konvertierung auf das App-v 4,5-oder App-v 4,6-Format aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="9794d-108">Packages that were created using a version prior to App-V 4.5 must be upgraded to the App-V 4.5 or App-V 4.6 format before conversion.</span></span>

<span data-ttu-id="9794d-109">Die folgenden Informationen enthalten eine Anleitung zum Konvertieren vorhandener virtueller Anwendungspakete.</span><span class="sxs-lookup"><span data-stu-id="9794d-109">The following information provides direction for converting existing virtual application packages.</span></span>

**<span data-ttu-id="9794d-110">Wichtig</span><span class="sxs-lookup"><span data-stu-id="9794d-110">Important</span></span>**  
<span data-ttu-id="9794d-111">Sie müssen den Paket Konverter so konfigurieren, dass die Paketinhalts Datei immer an einem sicheren Speicherort und Verzeichnis gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="9794d-111">You must configure the package converter to always save the package ingredients file to a secure location and directory.</span></span> <span data-ttu-id="9794d-112">Auf einen sicheren Speicherort kann nur von einem Administrator zugegriffen werden.</span><span class="sxs-lookup"><span data-stu-id="9794d-112">A secure location is accessible only by an administrator.</span></span> <span data-ttu-id="9794d-113">Wenn Sie das Paket bereitstellen, sollten Sie darüber hinaus das Paket an einem sicheren Speicherort speichern, oder Sie müssen sicherstellen, dass kein anderer Benutzer während des Konvertierungsvorgangs angemeldet werden darf.</span><span class="sxs-lookup"><span data-stu-id="9794d-113">Additionally, when you deploy the package, you should save the package to a location that is secure, or make sure that no other user is allowed to be logged in during the conversion process.</span></span>



**<span data-ttu-id="9794d-114">Der App-V 4,6-Installationsordner wird an das virtuelle Dateisystem-Stammverzeichnis umgeleitet</span><span class="sxs-lookup"><span data-stu-id="9794d-114">App-V 4.6 installation folder is redirected to virtual file system root</span></span>**

<span data-ttu-id="9794d-115">Wenn Sie Pakete von App-v 4,6 in 5,1 konvertieren, kann das App-v 5,1-Paket auf das hart codierte Laufwerk zugreifen, das Sie beim Erstellen von 4,6-Paketen verwenden mussten.</span><span class="sxs-lookup"><span data-stu-id="9794d-115">When you convert packages from App-V 4.6 to 5.1, the App-V 5.1 package can access the hardcoded drive that you were required to use when you created 4.6 packages.</span></span> <span data-ttu-id="9794d-116">Der Laufwerkbuchstabe ist das Laufwerk, das Sie als Installationslaufwerk auf dem 4,6-Sequenzcomputer ausgewählt haben.</span><span class="sxs-lookup"><span data-stu-id="9794d-116">The drive letter will be the drive you selected as the installation drive on the 4.6 sequencing machine.</span></span> <span data-ttu-id="9794d-117">(Der standardmäßige Laufwerkbuchstabe ist Q:\\.)</span><span class="sxs-lookup"><span data-stu-id="9794d-117">(The default drive letter is Q:\\.)</span></span>

<span data-ttu-id="9794d-118">Vor App-v 5,1 wurde der 4,6-Stammordner nicht erkannt, und der Zugriff auf App-v 5,0-Pakete war nicht möglich.</span><span class="sxs-lookup"><span data-stu-id="9794d-118">Prior to App-V 5.1, the 4.6 root folder was not recognized and could not be accessed by App-V 5.0 packages.</span></span> <span data-ttu-id="9794d-119">Nun können APP-v 5,1-Pakete über den vollständigen Pfad auf hart codierte Dateien zugreifen oder Dateien unter dem App-v 4,6-Installations Stamm programmgesteuert auflisten.</span><span class="sxs-lookup"><span data-stu-id="9794d-119">Now, App-V 5.1 packages can access hardcoded files by their full path or can programmatically enumerate files under the App-V 4.6 installation root.</span></span>

<span data-ttu-id="9794d-120">**Technische Informationen:** Der APP-v 5,1-Paket Konverter speichert den App-v 4,6-Installations Stammordner und die kurzen Ordnernamen in der FilesystemMetadata.xml-Datei im File System-Element.</span><span class="sxs-lookup"><span data-stu-id="9794d-120">**Technical Details:** The App-V 5.1 package converter will save the App-V 4.6 installation root folder and short folder names in the FilesystemMetadata.xml file in the Filesystem element.</span></span> <span data-ttu-id="9794d-121">Wenn der APP-v 5,1-Client den virtuellen Prozess erstellt, werden Anforderungen aus dem App-v 4,6-Installations Stamm dem virtuellen Dateisystem Stamm zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="9794d-121">When the App-V 5.1 client creates the virtual process, it will map requests from the App-V 4.6 installation root to the virtual file system root.</span></span>

**<span data-ttu-id="9794d-122">Erste Schritte</span><span class="sxs-lookup"><span data-stu-id="9794d-122">Getting started</span></span>**

1.  <span data-ttu-id="9794d-123">Installieren Sie den App-V-Sequencer auf einem Computer in Ihrer Umgebung.</span><span class="sxs-lookup"><span data-stu-id="9794d-123">Install the App-V Sequencer on a computer in your environment.</span></span> <span data-ttu-id="9794d-124">Informationen zum Installieren des Sequencers finden Sie unter so wird es [gemacht: Installieren des Sequencers](how-to-install-the-sequencer-51beta-gb18030.md).</span><span class="sxs-lookup"><span data-stu-id="9794d-124">For information about how to install the Sequencer, see [How to Install the Sequencer](how-to-install-the-sequencer-51beta-gb18030.md).</span></span>

2.  

    <span data-ttu-id="9794d-125">Die folgenden Cmdlets stehen zur Verfügung:</span><span class="sxs-lookup"><span data-stu-id="9794d-125">The following cmdlets are available:</span></span>

    -   <span data-ttu-id="9794d-126">Test-AppvLegacyPackage – dieses Cmdlet dient zum Überprüfen von Paketen.</span><span class="sxs-lookup"><span data-stu-id="9794d-126">Test-AppvLegacyPackage – This cmdlet is designed to check packages.</span></span> <span data-ttu-id="9794d-127">Es werden Informationen zu Fehlern mit dem Paket wie fehlenden **SFT** -Dateien, einer ungültigen Quelle, **OSD** -Dateifehlern oder einer ungültigen Paketversion zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9794d-127">It will return information about any failures with the package such as missing **.sft** files, an invalid source, **.osd** file errors, or invalid package version.</span></span> <span data-ttu-id="9794d-128">Dieses Cmdlet analysiert die **SFT-** Datei nicht oder führt eine eingehende Überprüfung durch.</span><span class="sxs-lookup"><span data-stu-id="9794d-128">This cmdlet will not parse the **.sft** file or do any in depth validation.</span></span> <span data-ttu-id="9794d-129">Informationen zu Optionen und Grundfunktionen für dieses Cmdlet finden Sie unter Verwenden des PowerShell-cmdline `Test-AppvLegacyPackage -?` .</span><span class="sxs-lookup"><span data-stu-id="9794d-129">For information about options and basic functionality for this cmdlet, using the PowerShell cmdline, type `Test-AppvLegacyPackage -?`.</span></span>

    -   <span data-ttu-id="9794d-130">ConvertFrom-AppvLegacyPackage – geben Sie zum Konvertieren eines vorhandenen Pakets `ConvertFrom-AppvLegacyPackage c:\contentStore c:\convertedPackages` .</span><span class="sxs-lookup"><span data-stu-id="9794d-130">ConvertFrom-AppvLegacyPackage – To convert an existing package, type `ConvertFrom-AppvLegacyPackage c:\contentStore c:\convertedPackages`.</span></span> <span data-ttu-id="9794d-131">In diesem Befehl `c:\contentStore` stellt den Speicherort des vorhandenen Pakets dar und `c:\convertedPackages` ist das Ausgabeverzeichnis, in das die resultierende App-V 5,1-Paketdatei für virtuelle Anwendungen gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="9794d-131">In this command, `c:\contentStore` represents the location of the existing package and `c:\convertedPackages` is the output directory to which the resulting App-V 5.1 virtual application package file will be saved.</span></span> <span data-ttu-id="9794d-132">Wenn Sie keinen neuen Namen angeben, wird standardmäßig der alte Paketname für den App-V 5,1-Dateinamen verwendet.</span><span class="sxs-lookup"><span data-stu-id="9794d-132">By default, if you do not specify a new name, the old package name will be used for the App-V 5.1 filename.</span></span>

        <span data-ttu-id="9794d-133">Darüber hinaus optimiert der Paket Konverter die Leistung von Paketen in App-v 5,1, indem das Paket so festgelegt wird, dass das App-v-Paket den Fehler streamt.</span><span class="sxs-lookup"><span data-stu-id="9794d-133">Additionally, the package converter optimizes performance of packages in App-V 5.1 by setting the package to stream fault the App-V package.</span></span>  <span data-ttu-id="9794d-134">Dies ist leistungsstärker als der primäre Feature-Block und der vollständige Download des Pakets.</span><span class="sxs-lookup"><span data-stu-id="9794d-134">This is more performant than the primary feature block and fully downloading the package.</span></span> <span data-ttu-id="9794d-135">Mit dem Flag **DownloadFullPackageOnFirstLaunch** können Sie das Paket konvertieren und festlegen, dass das Paket standardmäßig vollständig heruntergeladen werden soll.</span><span class="sxs-lookup"><span data-stu-id="9794d-135">The flag **DownloadFullPackageOnFirstLaunch** allows you to convert the package and set the package to be fully downloaded by default.</span></span>

        **<span data-ttu-id="9794d-136">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="9794d-136">Note</span></span>**  
        <span data-ttu-id="9794d-137">Bevor Sie das Ausgabeverzeichnis angeben, müssen Sie das Ausgabeverzeichnis erstellen.</span><span class="sxs-lookup"><span data-stu-id="9794d-137">Before you specify the output directory, you must create the output directory.</span></span>



~~~
**Advanced Conversion Tips**

-   Piping - PowerShell supports piping. Piping allows you to call `dir c:\contentStore\myPackage | Test-AppvLegacyPackage`. In this example, the directory object that represents `myPackage` will be given as input to the `Test-AppvLegacyPackage` command and bound to the `-Source` parameter. Piping like this is especially useful when you want to batch commands together; for example, `dir .\ | Test-AppvLegacyPackage | ConvertFrom-AppvLegacyAppvPackage -Target .\ConvertedPackages`. This piped command would test the packages and then pass those objects on to actually be converted. You can also apply a filter on packages without errors or only specify a directory which contains an **.sprj** file or pipe them to another cmdlet that adds the filtered package to the server or publishes them to the App-V 5.1 client.

-   Batching - The PowerShell command enables batching. More specifically, the cmdlets support taking a string\[\] object for the `-Source` parameter which represents a list of directory paths. This allows you to enter `$packages = dir c:\contentStore` and then call `ConvertFrom-AppvLegacyAppvPackage-Source $packages -Target c:\ConvertedPackages` or to use piping and call `dir c:\ContentStore | ConvertFrom-AppvLegacyAppvPackage -Target C:\ConvertedPackages`.

-   Other functionality - PowerShell has other built-in functionality for features such as aliases, piping, lazy-binding, .NET object, and many others. All of these are usable in PowerShell and can help you create advanced scenarios for the Package Converter.

**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## <span data-ttu-id="9794d-138">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="9794d-138">Related topics</span></span>


[<span data-ttu-id="9794d-139">Vorgänge für App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="9794d-139">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)









