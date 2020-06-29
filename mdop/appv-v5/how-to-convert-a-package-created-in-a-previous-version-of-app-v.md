---
title: So konvertieren Sie ein Paket, das in einer früheren Version von App-V erstellt wurde
description: So konvertieren Sie ein Paket, das in einer früheren Version von App-V erstellt wurde
author: dansimp
ms.assetid: b092a5f8-cc5f-4df8-a5a2-0a68fd7bd5b2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3bd0d5db7cb406a5a7fe67c69ff77461cce2b0a9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805669"
---
# <span data-ttu-id="99082-103">So konvertieren Sie ein Paket, das in einer früheren Version von App-V erstellt wurde</span><span class="sxs-lookup"><span data-stu-id="99082-103">How to Convert a Package Created in a Previous Version of App-V</span></span>


<span data-ttu-id="99082-104">Sie können das Paket Konverter-Dienstprogrammverwenden, um virtuelle Anwendungspakete zu aktualisieren, die mit früheren Versionen von App-V erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="99082-104">You can use the package converter utility to upgrade virtual application packages that have been created with previous versions of App-V.</span></span>

**<span data-ttu-id="99082-105">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="99082-105">Note</span></span>**  
<span data-ttu-id="99082-106">Wenn Sie einen Computer mit einer 64-Bit-Architektur ausführen, müssen Sie die x86-Version von PowerShell verwenden.</span><span class="sxs-lookup"><span data-stu-id="99082-106">If you are running a computer with a 64-bit architecture, you must use the x86 version of PowerShell.</span></span>



<span data-ttu-id="99082-107">Der Paket Konverter kann nur Pakete direkt konvertieren, die mit dem App-V 4,5-Sequenzer oder einer nachfolgenden Version erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="99082-107">The package converter can only directly convert packages that were created by using the App-V 4.5 sequencer or a subsequent version.</span></span> <span data-ttu-id="99082-108">Pakete, die mit einer Version vor App-v 4,5 erstellt wurden, müssen vor der Konvertierung auf das App-v 4,5-oder App-v 4,6-Format aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="99082-108">Packages that were created using a version prior to App-V 4.5 must be upgraded to the App-V 4.5 or App-V 4.6 format before conversion.</span></span>

<span data-ttu-id="99082-109">Die folgenden Informationen enthalten eine Anleitung zum Konvertieren vorhandener virtueller Anwendungspakete.</span><span class="sxs-lookup"><span data-stu-id="99082-109">The following information provides direction for converting existing virtual application packages.</span></span>

**<span data-ttu-id="99082-110">Wichtig</span><span class="sxs-lookup"><span data-stu-id="99082-110">Important</span></span>**  
<span data-ttu-id="99082-111">Sie müssen den Paket Konverter so konfigurieren, dass die Paketinhalts Datei immer an einem sicheren Speicherort und Verzeichnis gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="99082-111">You must configure the package converter to always save the package ingredients file to a secure location and directory.</span></span> <span data-ttu-id="99082-112">Auf einen sicheren Speicherort kann nur von einem Administrator zugegriffen werden.</span><span class="sxs-lookup"><span data-stu-id="99082-112">A secure location is accessible only by an administrator.</span></span> <span data-ttu-id="99082-113">Wenn Sie das Paket bereitstellen, sollten Sie darüber hinaus das Paket an einem sicheren Speicherort speichern, oder Sie müssen sicherstellen, dass kein anderer Benutzer während des Konvertierungsvorgangs angemeldet werden darf.</span><span class="sxs-lookup"><span data-stu-id="99082-113">Additionally, when you deploy the package, you should save the package to a location that is secure, or make sure that no other user is allowed to be logged in during the conversion process.</span></span>



**<span data-ttu-id="99082-114">Erste Schritte</span><span class="sxs-lookup"><span data-stu-id="99082-114">Getting started</span></span>**

1.  <span data-ttu-id="99082-115">Installieren Sie den App-V-Sequencer auf einem Computer in Ihrer Umgebung.</span><span class="sxs-lookup"><span data-stu-id="99082-115">Install the App-V Sequencer on a computer in your environment.</span></span> <span data-ttu-id="99082-116">Informationen zum Installieren des Sequencers finden Sie unter so wird es [gemacht: Installieren des Sequencers](how-to-install-the-sequencer-beta-gb18030.md).</span><span class="sxs-lookup"><span data-stu-id="99082-116">For information about how to install the Sequencer, see [How to Install the Sequencer](how-to-install-the-sequencer-beta-gb18030.md).</span></span>

2. <span data-ttu-id="99082-117">Importieren des erforderlichen PowerShell-Moduls</span><span class="sxs-lookup"><span data-stu-id="99082-117">Import the required Powershell Module</span></span>

```powershell
Import-Module AppVPkgConverter
```

3. <span data-ttu-id="99082-118">Die folgenden Cmdlets stehen zur Verfügung:</span><span class="sxs-lookup"><span data-stu-id="99082-118">The following cmdlets are available:</span></span>

   -   <span data-ttu-id="99082-119">Test-AppvLegacyPackage – dieses Cmdlet dient zum Überprüfen von Paketen.</span><span class="sxs-lookup"><span data-stu-id="99082-119">Test-AppvLegacyPackage – This cmdlet is designed to check packages.</span></span> <span data-ttu-id="99082-120">Es werden Informationen zu Fehlern mit dem Paket wie fehlenden **SFT** -Dateien, einer ungültigen Quelle, **OSD** -Dateifehlern oder einer ungültigen Paketversion zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="99082-120">It will return information about any failures with the package such as missing **.sft** files, an invalid source, **.osd** file errors, or invalid package version.</span></span> <span data-ttu-id="99082-121">Dieses Cmdlet analysiert die **SFT-** Datei nicht oder führt eine eingehende Überprüfung durch.</span><span class="sxs-lookup"><span data-stu-id="99082-121">This cmdlet will not parse the **.sft** file or do any in depth validation.</span></span> <span data-ttu-id="99082-122">Informationen zu Optionen und Grundfunktionen für dieses Cmdlet finden Sie unter Verwenden des PowerShell-cmdline `Test-AppvLegacyPackage -?` .</span><span class="sxs-lookup"><span data-stu-id="99082-122">For information about options and basic functionality for this cmdlet, using the PowerShell cmdline, type `Test-AppvLegacyPackage -?`.</span></span>

   -   <span data-ttu-id="99082-123">ConvertFrom-AppvLegacyPackage – geben Sie zum Konvertieren eines vorhandenen Pakets `ConvertFrom-AppvLegacyPackage c:\contentStore c:\convertedPackages` .</span><span class="sxs-lookup"><span data-stu-id="99082-123">ConvertFrom-AppvLegacyPackage – To convert an existing package, type `ConvertFrom-AppvLegacyPackage c:\contentStore c:\convertedPackages`.</span></span> <span data-ttu-id="99082-124">In diesem Befehl `c:\contentStore` stellt den Speicherort des vorhandenen Pakets dar und `c:\convertedPackages` ist das Ausgabeverzeichnis, in das die resultierende App-V 5,0-Paketdatei für virtuelle Anwendungen gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="99082-124">In this command, `c:\contentStore` represents the location of the existing package and `c:\convertedPackages` is the output directory to which the resulting App-V 5.0 virtual application package file will be saved.</span></span> <span data-ttu-id="99082-125">Wenn Sie keinen neuen Namen angeben, wird standardmäßig der alte Paketname für den App-V 5,0-Dateinamen verwendet.</span><span class="sxs-lookup"><span data-stu-id="99082-125">By default, if you do not specify a new name, the old package name will be used for the App-V 5.0 filename.</span></span>

       <span data-ttu-id="99082-126">Darüber hinaus optimiert der Paket Konverter die Leistung von Paketen in App-v 5,0, indem das Paket so festgelegt wird, dass das App-v-Paket den Fehler streamt.</span><span class="sxs-lookup"><span data-stu-id="99082-126">Additionally, the package converter optimizes performance of packages in App-V 5.0 by setting the package to stream fault the App-V package.</span></span>  <span data-ttu-id="99082-127">Dies ist leistungsstärker als der primäre Feature-Block und der vollständige Download des Pakets.</span><span class="sxs-lookup"><span data-stu-id="99082-127">This is more performant than the primary feature block and fully downloading the package.</span></span> <span data-ttu-id="99082-128">Mit dem Flag **DownloadFullPackageOnFirstLaunch** können Sie das Paket konvertieren und festlegen, dass das Paket standardmäßig vollständig heruntergeladen werden soll.</span><span class="sxs-lookup"><span data-stu-id="99082-128">The flag **DownloadFullPackageOnFirstLaunch** allows you to convert the package and set the package to be fully downloaded by default.</span></span>

       **<span data-ttu-id="99082-129">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="99082-129">Note</span></span>**  
       <span data-ttu-id="99082-130">Bevor Sie das Ausgabeverzeichnis angeben, müssen Sie das Ausgabeverzeichnis erstellen.</span><span class="sxs-lookup"><span data-stu-id="99082-130">Before you specify the output directory, you must create the output directory.</span></span>



~~~
**Advanced Conversion Tips**

-   Piping - PowerShell supports piping. Piping allows you to call `dir c:\contentStore\myPackage | Test-AppvLegacyPackage`. In this example, the directory object that represents `myPackage` will be given as input to the `Test-AppvLegacyPackage` command and bound to the `-Source` parameter. Piping like this is especially useful when you want to batch commands together; for example, `dir .\ | Test-AppvLegacyPackage | ConvertFrom-AppvLegacyAppvPackage -Target .\ConvertedPackages`. This piped command would test the packages and then pass those objects on to actually be converted. You can also apply a filter on packages without errors or only specify a directory which contains an **.sprj** file or pipe them to another cmdlet that adds the filtered package to the server or publishes them to the App-V 5.0 client.

-   Batching - The PowerShell command enables batching. More specifically, the cmdlets support taking a string\[\] object for the `-Source` parameter which represents a list of directory paths. This allows you to enter `$packages = dir c:\contentStore` and then call `ConvertFrom-AppvLegacyAppvPackage-Source $packages -Target c:\ConvertedPackages` or to use piping and call `dir c:\ContentStore | ConvertFrom-AppvLegacyAppvPackage -Target C:\ConvertedPackages`.

-   Other functionality - PowerShell has other built-in functionality for features such as aliases, piping, lazy-binding, .NET object, and many others. All of these are usable in PowerShell and can help you create advanced scenarios for the Package Converter.

**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## <span data-ttu-id="99082-131">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="99082-131">Related topics</span></span>


[<span data-ttu-id="99082-132">Vorgänge für App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="99082-132">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)









