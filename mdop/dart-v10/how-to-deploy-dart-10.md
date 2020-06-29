---
title: So stellen Sie DaRT 10 bereit
description: So stellen Sie DaRT 10 bereit
author: dansimp
ms.assetid: 13e8ba20-21c3-4870-94ed-6d3106d69f21
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 9e78f55e238cce16798525915487e4b753d92e6c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804703"
---
# <span data-ttu-id="cea3b-103">So stellen Sie DaRT 10 bereit</span><span class="sxs-lookup"><span data-stu-id="cea3b-103">How to Deploy DaRT 10</span></span>


<span data-ttu-id="cea3b-104">Die folgenden Anweisungen erläutern, wie Sie Microsoft Diagnostics and Recovery Toolset (Dart) 10 in Ihrer Umgebung bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="cea3b-104">The following instructions explain how to deploy Microsoft Diagnostics and Recovery Toolset (DaRT) 10 in your environment.</span></span> <span data-ttu-id="cea3b-105">Informationen zum Abrufen der Dart-Software finden Sie unter [Abrufen von MDOP](https://go.microsoft.com/fwlink/?LinkId=322049).</span><span class="sxs-lookup"><span data-stu-id="cea3b-105">To get the DaRT software, see [How to Get MDOP](https://go.microsoft.com/fwlink/?LinkId=322049).</span></span> <span data-ttu-id="cea3b-106">Es wird davon ausgegangen, dass Sie alle Funktionen auf einem Administratorcomputer installieren.</span><span class="sxs-lookup"><span data-stu-id="cea3b-106">It is assumed that you are installing all functionality on one administrator computer.</span></span> <span data-ttu-id="cea3b-107">Wenn Sie Dart 10 auf mehreren Computern mithilfe eines elektronischen Softwareverteilungssystems bereitstellen oder deinstallieren müssen, ist es möglicherweise einfacher, Befehlszeilen Installationsoptionen zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="cea3b-107">If you need to deploy or uninstall DaRT 10 on multiple computers, using an electronic software distribution system, for example, it might be easier to use command line installation options.</span></span> <span data-ttu-id="cea3b-108">Beschreibungen und Beispiele der verfügbaren Befehlszeilenoptionen finden Sie in diesem Abschnitt.</span><span class="sxs-lookup"><span data-stu-id="cea3b-108">Descriptions and examples of the available command line options are provided in this section.</span></span>

<span data-ttu-id="cea3b-109">**Wichtig**  Bevor Sie Dart installieren, lesen Sie [Dart 10 unterstützte Konfigurationen](dart-10-supported-configurations.md) , um sicherzustellen, dass Sie alle erforderlichen Software installiert haben und der Computer die Mindestsystemanforderungen erfüllt.</span><span class="sxs-lookup"><span data-stu-id="cea3b-109">**Important** Before you install DaRT, see [DaRT 10 Supported Configurations](dart-10-supported-configurations.md) to ensure that you have installed all of the prerequisite software and that the computer meets the minimum system requirements.</span></span> <span data-ttu-id="cea3b-110">Auf dem Computer, auf dem Sie Dart installieren, muss Windows 10 ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="cea3b-110">The computer onto which you install DaRT must be running Windows 10.</span></span>

 

<span data-ttu-id="cea3b-111">Sie können Dart mithilfe einer von zwei unterschiedlichen Konfigurationen installieren:</span><span class="sxs-lookup"><span data-stu-id="cea3b-111">You can install DaRT using one of two different configurations:</span></span>

-   <span data-ttu-id="cea3b-112">Installieren Sie Dart und alle Dart-Tools auf dem Administratorcomputer.</span><span class="sxs-lookup"><span data-stu-id="cea3b-112">Install DaRT and all of the DaRT tools on the administrator computer.</span></span>

-   <span data-ttu-id="cea3b-113">Installieren Sie auf dem Administratorcomputer nur die Tools, die Sie zum Erstellen des DART-Wiederherstellungs Bilds benötigen, und installieren Sie dann den **Remote Verbindungs-Viewer** und optional **Crash Analyzer** auf einem Helpdesk-Computer.</span><span class="sxs-lookup"><span data-stu-id="cea3b-113">Install on the administrator computer only the tools that you need to create the DaRT recovery image, and then install the **Remote Connection Viewer** and, optionally, **Crash Analyzer** on a help desk computer.</span></span>

<span data-ttu-id="cea3b-114">Die Dart-Installationsdatei steht sowohl in 32-Bit-als auch in 64-Bit-Versionen zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="cea3b-114">The DaRT installation file is available in both 32-bit and 64-bit versions.</span></span> <span data-ttu-id="cea3b-115">Installieren Sie die Version, die der Architektur des Computers entspricht, auf dem Sie den Dart-Wiederherstellungsbild-Assistenten ausführen, nicht die Computerarchitektur des Wiederherstellungs Bilds, das Sie erstellen.</span><span class="sxs-lookup"><span data-stu-id="cea3b-115">Install the version that matches the architecture of the computer on which you are running the DaRT Recovery Image wizard, not the computer architecture of the recovery image that you are creating.</span></span>

<span data-ttu-id="cea3b-116">Sie können eine der beiden Versionen der Dart-Installationsdatei verwenden, um ein Wiederherstellungsabbild für 32-Bit-oder 64-Bit-Computer zu erstellen, Sie können jedoch kein Wiederherstellungsabbild für 32-Bit-und 64-Bit-Computer erstellen.</span><span class="sxs-lookup"><span data-stu-id="cea3b-116">You can use either version of the DaRT installation file to create a recovery image for either 32-bit or 64-bit computers, but you cannot create one recovery image for both 32-bit and 64-bit computers.</span></span>

**<span data-ttu-id="cea3b-117">So installieren Sie Dart und alle Dart-Tools auf einem Administratorcomputer</span><span class="sxs-lookup"><span data-stu-id="cea3b-117">To install DaRT and all DaRT tools on an administrator computer</span></span>**

1.  <span data-ttu-id="cea3b-118">Laden Sie die 32-Bit-oder 64-Bit-Version der Dart 10-Installationsdatei herunter.</span><span class="sxs-lookup"><span data-stu-id="cea3b-118">Download the 32-bit or 64-bit version of the DaRT 10 installer file.</span></span> <span data-ttu-id="cea3b-119">Wählen Sie die Architektur aus, die dem Computer entspricht, auf dem Sie Dart installieren, und führen Sie den Dart-Wiederherstellungsbild-Assistenten aus.</span><span class="sxs-lookup"><span data-stu-id="cea3b-119">Choose the architecture that matches the computer on which you are installing DaRT and running the DaRT Recovery Image wizard.</span></span>

2.  <span data-ttu-id="cea3b-120">Führen Sie in dem Ordner, in den Sie Dart 10 heruntergeladen haben, die **MSDaRT.msi** Installationsdatei aus, die ihren Systemanforderungen entspricht.</span><span class="sxs-lookup"><span data-stu-id="cea3b-120">From the folder into which you downloaded DaRT 10, run the **MSDaRT.msi** installation file that corresponds to your system requirements.</span></span>

3.  <span data-ttu-id="cea3b-121">Klicken Sie auf der Seite **Willkommen beim Setup-Assistenten von Microsoft Dart 10** auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="cea3b-121">On the **Welcome to the Microsoft DaRT 10 Setup Wizard** page, click **Next**.</span></span>

4.  <span data-ttu-id="cea3b-122">Akzeptieren Sie die Microsoft-Software-Lizenzbestimmungen, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="cea3b-122">Accept the Microsoft Software License Terms, and then click **Next**.</span></span>

5.  <span data-ttu-id="cea3b-123">Aktivieren Sie auf der Seite **Microsoft Update** die Option **Microsoft Update verwenden, wenn ich nach Updates Suche**, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="cea3b-123">On the **Microsoft Update** page, select **Use Microsoft Update when I check for updates**, and then click **Next**.</span></span>

6.  <span data-ttu-id="cea3b-124">Wählen Sie auf der Seite **Installationsordner auswählen** einen Ordner aus, oder klicken Sie auf **weiter** , um Dart im Standardinstallationspfad zu installieren.</span><span class="sxs-lookup"><span data-stu-id="cea3b-124">On the **Select Installation Folder** page, select a folder, or click **Next** to install DaRT in the default installation location.</span></span>

7.  <span data-ttu-id="cea3b-125">Wählen Sie auf der Seite **Setup Optionen** die Dart-Features aus, die Sie installieren möchten, oder klicken Sie auf **weiter** , um Dart mit allen Features zu installieren.</span><span class="sxs-lookup"><span data-stu-id="cea3b-125">On the **Setup Options** page, select the DaRT features that you want to install, or click **Next** to install DaRT with all of the features.</span></span>

8.  <span data-ttu-id="cea3b-126">Klicken Sie auf **Installieren**, um die Installation zu starten.</span><span class="sxs-lookup"><span data-stu-id="cea3b-126">To start the installation, click **Install**.</span></span>

9.  <span data-ttu-id="cea3b-127">Nachdem die Installation erfolgreich abgeschlossen wurde, klicken Sie auf **Fertig stellen** , um den Assistenten zu beenden.</span><span class="sxs-lookup"><span data-stu-id="cea3b-127">After the installation has completed successfully, click **Finish** to exit the wizard.</span></span>

## <span data-ttu-id="cea3b-128">So installieren Sie Dart und alle Dart-Tools auf einem Administratorcomputer mithilfe einer Eingabeaufforderung</span><span class="sxs-lookup"><span data-stu-id="cea3b-128">To install DaRT and all DaRT tools on an administrator computer by using a command prompt</span></span>


<span data-ttu-id="cea3b-129">Wenn Sie Dart installieren oder deinstallieren, haben Sie die Möglichkeit, die Installationsdateien an der Eingabeaufforderung auszuführen.</span><span class="sxs-lookup"><span data-stu-id="cea3b-129">When you install or uninstall DaRT, you have the option of running the installation files at the command prompt.</span></span> <span data-ttu-id="cea3b-130">In diesem Abschnitt werden einige Beispiele für verschiedene Optionen beschrieben, die Sie bei der Installation oder Deinstallation von DART an der Eingabeaufforderung angeben können.</span><span class="sxs-lookup"><span data-stu-id="cea3b-130">This section describes some examples of different options that you can specify when you install or uninstall DaRT at the command prompt.</span></span>

<span data-ttu-id="cea3b-131">Im folgenden Beispiel wird gezeigt, wie alle DART-Funktionen installiert werden.</span><span class="sxs-lookup"><span data-stu-id="cea3b-131">The following example shows how to install all DaRT functionality.</span></span>

``` syntax
msiexec /i MSDaRT.msi ADDLOCAL=CommonFiles, DaRTRecoveryImage,CrashAnalyzer,RemoteViewer 
```

<span data-ttu-id="cea3b-132">Im folgenden Beispiel wird gezeigt, wie Sie nur den Dart-Wiederherstellungsbild-Assistenten installieren.</span><span class="sxs-lookup"><span data-stu-id="cea3b-132">The following example shows how to install only the DaRT Recovery Image wizard.</span></span>

``` syntax
msiexec /i MSDaRT.msi ADDLOCAL=CommonFiles, ,DaRTRecoveryImage
```

<span data-ttu-id="cea3b-133">Im folgenden Beispiel wird gezeigt, wie nur der Absturzanalyse-und der Dart-Remote Verbindungs Viewer installiert werden.</span><span class="sxs-lookup"><span data-stu-id="cea3b-133">The following example shows how to install only the Crash Analyzer and the DaRT Remote Connection Viewer.</span></span>

``` syntax
msiexec /i MSDaRT.msi ADDLOCAL=CommonFiles,CrashAnalyzer,RemoteViewer 
```

<span data-ttu-id="cea3b-134">Im folgenden Beispiel wird ein Setupprotokoll für Windows Installer erstellt.</span><span class="sxs-lookup"><span data-stu-id="cea3b-134">The following example creates a setup log for the Windows Installer.</span></span> <span data-ttu-id="cea3b-135">Dies ist für das Debuggen hilfreich.</span><span class="sxs-lookup"><span data-stu-id="cea3b-135">This is valuable for debugging.</span></span>

``` syntax
msiexec.exe /i MSDaRT.msi /l*v log.txt 
```

<span data-ttu-id="cea3b-136">**Hinweis**  Sie können/qn oder/qb hinzufügen, um eine unbeaufsichtigte Installation durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="cea3b-136">**Note** You can add /qn or /qb to perform a silent installation.</span></span>

 

**<span data-ttu-id="cea3b-137">So überprüfen Sie die Dart-Installation</span><span class="sxs-lookup"><span data-stu-id="cea3b-137">To validate the DaRT installation</span></span>**

1.  <span data-ttu-id="cea3b-138">Klicken Sie auf **Start**, und wählen Sie **Diagnose-und Wiederherstellungs-Toolset**aus.</span><span class="sxs-lookup"><span data-stu-id="cea3b-138">Click **Start**, and select **Diagnostics and Recovery Toolset**.</span></span>

    <span data-ttu-id="cea3b-139">Das Fenster " **Diagnose-und Wiederherstellungs-Toolset** " wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="cea3b-139">The **Diagnostics and Recovery Toolset** window opens.</span></span>

2.  <span data-ttu-id="cea3b-140">Überprüfen Sie, ob alle Dart-Tools, die Sie für die Installation ausgewählt haben, erfolgreich installiert wurden.</span><span class="sxs-lookup"><span data-stu-id="cea3b-140">Check that all of the DaRT tools that you selected for installation were successfully installed.</span></span>

## <span data-ttu-id="cea3b-141">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="cea3b-141">Related topics</span></span>


[<span data-ttu-id="cea3b-142">Bereitstellen von DaRT 10 für Administratorcomputer</span><span class="sxs-lookup"><span data-stu-id="cea3b-142">Deploying DaRT 10 to Administrator Computers</span></span>](deploying-dart-10-to-administrator-computers.md)

 

 





