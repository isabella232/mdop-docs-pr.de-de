---
title: So stellen Sie DaRT 7.0 bereit
description: So stellen Sie DaRT 7.0 bereit
author: dansimp
ms.assetid: 30522441-40cb-4eca-99b4-dff758f5c647
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c2059b64e5f3ae7af8926bc00e5965598ede4288
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804685"
---
# <span data-ttu-id="8afd8-103">So stellen Sie DaRT 7.0 bereit</span><span class="sxs-lookup"><span data-stu-id="8afd8-103">How to Deploy DaRT 7.0</span></span>


<span data-ttu-id="8afd8-104">In diesem Thema finden Sie Anweisungen zum Bereitstellen von Microsoft Diagnostics and Recovery Toolset (Dart) 7 in Ihrer Umgebung.</span><span class="sxs-lookup"><span data-stu-id="8afd8-104">This topic provides instructions to deploy Microsoft Diagnostics and Recovery Toolset (DaRT)7 in your environment.</span></span> <span data-ttu-id="8afd8-105">Im ersten Verfahren in diesem Thema wird davon ausgegangen, dass Sie alle Funktionen auf einem Administratorcomputer installieren.</span><span class="sxs-lookup"><span data-stu-id="8afd8-105">The first procedure in this topic assumes that you are installing all functionality on one administrator computer.</span></span> <span data-ttu-id="8afd8-106">Wenn Sie Dart auf mehreren Computern mithilfe eines elektronischen Softwareverteilungssystems bereitstellen oder deinstallieren müssen, ist es möglicherweise einfacher, Befehlszeilen Installationsoptionen zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="8afd8-106">When you need to deploy or uninstall DaRT on multiple computers, using an electronic software distribution system for example, it might be easier to use command line installation options.</span></span> <span data-ttu-id="8afd8-107">Diese Optionen werden in der zweiten Vorgehensweise in diesem Thema definiert, die eine Beispiel Verwendung für die verfügbaren Befehlszeilenoptionen bietet.</span><span class="sxs-lookup"><span data-stu-id="8afd8-107">Those options are defined in the second procedure in this topic which provides example usage for the available command line options.</span></span>

<span data-ttu-id="8afd8-108">**Wichtig**  Bevor Sie Dart installieren, stellen Sie sicher, dass der Computer die Mindestsystemanforderungen erfüllt, die in [Dart 7,0-unterstützten Konfigurationen](dart-70-supported-configurations-dart-7.md)aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="8afd8-108">**Important** Before you install DaRT, ensure that the computer meets the minimum system requirements listed in [DaRT 7.0 Supported Configurations](dart-70-supported-configurations-dart-7.md).</span></span>

 

**<span data-ttu-id="8afd8-109">So installieren Sie Dart auf einem Administratorcomputer</span><span class="sxs-lookup"><span data-stu-id="8afd8-109">To install DaRT on an administrator computer</span></span>**

1.  <span data-ttu-id="8afd8-110">Suchen Sie die Dart-Installationsdateien, die Sie im Rahmen Ihres Software Downloads erhalten haben.</span><span class="sxs-lookup"><span data-stu-id="8afd8-110">Locate the DaRT installation files that you received as part of your software download.</span></span>

2.  <span data-ttu-id="8afd8-111">Doppelklicken Sie auf die Dart-Installationsdatei, die ihren Systemanforderungen entspricht, entweder 32-Bit oder 64-Bit.</span><span class="sxs-lookup"><span data-stu-id="8afd8-111">Double-click the DaRT installation file that corresponds to your system requirements, either 32-bit or 64-bit.</span></span> <span data-ttu-id="8afd8-112">Die Dart-Installationsdatei hat den Namen **MSDaRT70.msi**.</span><span class="sxs-lookup"><span data-stu-id="8afd8-112">The DaRT installation file is named **MSDaRT70.msi**.</span></span>

3.  <span data-ttu-id="8afd8-113">Akzeptieren Sie die Microsoft-Software-Lizenzbestimmungen, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="8afd8-113">Accept the Microsoft Software License Terms, and then click **Next**.</span></span>

4.  <span data-ttu-id="8afd8-114">Wählen Sie den Zielordner für die Installation von DART aus, wählen Sie aus, ob Dart für alle Benutzer oder nur für den aktuellen Benutzer installiert werden soll, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="8afd8-114">Select the destination folder for installing DaRT, select whether DaRT should be installed for all users or just the current user, and then click **Next**.</span></span>

5.  <span data-ttu-id="8afd8-115">Wählen Sie aus, ob die Installation **Normal**, **Benutzerdefiniert**oder **abgeschlossen**sein soll, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="8afd8-115">Select whether the installation should be **Typical**, **Custom**, or **Complete**, and then click **Next**.</span></span>

    -   <span data-ttu-id="8afd8-116">**Standard** installiert die Tools, die am häufigsten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8afd8-116">**Typical** installs the tools that are most frequently used.</span></span> <span data-ttu-id="8afd8-117">Diese Methode wird für die meisten Benutzer empfohlen.</span><span class="sxs-lookup"><span data-stu-id="8afd8-117">This method is recommended for most users.</span></span>

    -   <span data-ttu-id="8afd8-118">Mit **Benutzerdefiniert** können Sie die Tools auswählen, die installiert sind und wo Sie installiert werden.</span><span class="sxs-lookup"><span data-stu-id="8afd8-118">**Custom** lets you select the tools that are installed and where they will be installed.</span></span> <span data-ttu-id="8afd8-119">Dies wird für erfahrene Benutzer empfohlen, insbesondere dann, wenn Sie verschiedene Dart-Tools auf verschiedenen Helpdesk-Computern installieren.</span><span class="sxs-lookup"><span data-stu-id="8afd8-119">This is recommended for advanced users, especially if you are installing different DaRT tools on different helpdesk computers.</span></span>

    -   <span data-ttu-id="8afd8-120">**Complete** installiert alle Dart-Tools und benötigt den meisten Speicherplatz.</span><span class="sxs-lookup"><span data-stu-id="8afd8-120">**Complete** installs all DaRT tools and requires the most disk space.</span></span>

    <span data-ttu-id="8afd8-121">Nachdem Sie Ihre Installationsmethode ausgewählt haben, klicken Sie auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="8afd8-121">After you have selected your method of installation, click **Next**.</span></span>

6.  <span data-ttu-id="8afd8-122">Klicken Sie auf **Installieren**, um die Installation zu starten.</span><span class="sxs-lookup"><span data-stu-id="8afd8-122">To start the installation, click **Install**.</span></span>

7.  <span data-ttu-id="8afd8-123">Nachdem die Installation erfolgreich abgeschlossen wurde, klicken Sie auf **Fertig stellen** , um den Assistenten zu beenden.</span><span class="sxs-lookup"><span data-stu-id="8afd8-123">After the installation is completed successfully, click **Finish** to exit the wizard.</span></span>

**<span data-ttu-id="8afd8-124">So installieren Sie Dart an der Eingabeaufforderung</span><span class="sxs-lookup"><span data-stu-id="8afd8-124">To install DaRT at the command prompt</span></span>**

1.  <span data-ttu-id="8afd8-125">Im folgenden Beispiel wird gezeigt, wie alle DART-Funktionen installiert werden.</span><span class="sxs-lookup"><span data-stu-id="8afd8-125">The following example shows how to install all DaRT functionality.</span></span>

    ``` syntax
    msiexec /i MSDaRT70.msi ADDLOCAL=CommonFiles,MSDaRTHelp,DaRTRecoveryImage,CrashAnalyzer,RemoteViewer 
    ```

2.  <span data-ttu-id="8afd8-126">Im folgenden Beispiel wird gezeigt, wie Sie nur den **Dart-Wiederherstellungsbild-Assistenten**installieren.</span><span class="sxs-lookup"><span data-stu-id="8afd8-126">The following example shows how to install only the **DaRT Recovery Image Wizard**.</span></span>

    ``` syntax
    msiexec /i MSDaRT70.msi ADDLOCAL=CommonFiles,MSDaRTHelp,DaRTRecoveryImage
    ```

3.  <span data-ttu-id="8afd8-127">Im folgenden Beispiel wird gezeigt, wie nur der Absturzanalyse-und der Dart-Remote Verbindungs Viewer installiert werden.</span><span class="sxs-lookup"><span data-stu-id="8afd8-127">The following example shows how to install only the Crash Analyzer and the DaRT Remote Connection Viewer.</span></span>

    ``` syntax
    msiexec /i MSDaRT70.msi ADDLOCAL=CommonFiles,MSDaRTHelp,CrashAnalyzer,RemoteViewer 
    ```

4.  <span data-ttu-id="8afd8-128">Im folgenden Beispiel wird ein Setupprotokoll für Windows Installer erstellt.</span><span class="sxs-lookup"><span data-stu-id="8afd8-128">The following example creates a setup log for the Windows Installer.</span></span> <span data-ttu-id="8afd8-129">Dies ist für das Debuggen hilfreich.</span><span class="sxs-lookup"><span data-stu-id="8afd8-129">This is valuable for debugging.</span></span>

    ``` syntax
    msiexec.exe /i MSDaRT70.msi /l*v log.txt 
    ```

<span data-ttu-id="8afd8-130">**Hinweis**  Sie können/qn oder/qb zu einer der Optionen für die Eingabeaufforderung zur Dart-Installation hinzufügen, um eine unbeaufsichtigte Installation durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="8afd8-130">**Note** You can add /qn or /qb to any of the DaRT installation command prompt options to perform a silent installation.</span></span>

 

## <span data-ttu-id="8afd8-131">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="8afd8-131">Related topics</span></span>


[<span data-ttu-id="8afd8-132">Bereitstellen von DaRT 7.0 für Administratorcomputer</span><span class="sxs-lookup"><span data-stu-id="8afd8-132">Deploying DaRT 7.0 to Administrator Computers</span></span>](deploying-dart-70-to-administrator-computers-dart-7.md)

 

 




