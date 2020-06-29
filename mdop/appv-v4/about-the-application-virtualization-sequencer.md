---
title: Informationen über Application Virtualization Sequencer
description: Informationen über Application Virtualization Sequencer
author: dansimp
ms.assetid: bee193ca-58bd-40c9-b41a-310435633895
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 83709bcceabe3312fba34512b47d28a24b4dc52c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808131"
---
# <span data-ttu-id="ba1e8-103">Informationen über Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="ba1e8-103">About the Application Virtualization Sequencer</span></span>


<span data-ttu-id="ba1e8-104">Der Microsoft Application Virtualization (App-V)-Sequenzer überwacht und zeichnet alle Installations-und Einrichtungsprozesse für eine Anwendung auf und erstellt die folgenden Dateien: **ICO**, **OSD**, **SFT**und **SPRJ**.</span><span class="sxs-lookup"><span data-stu-id="ba1e8-104">The Microsoft Application Virtualization (App-V) Sequencer monitors and records all installation and setup processes for an application and creates the following files: **ICO**, **OSD**, **SFT**, and **SPRJ**.</span></span> <span data-ttu-id="ba1e8-105">Diese Dateien enthalten alle erforderlichen Informationen zu einer Anwendung, damit die Anwendung in einer virtuellen Umgebung auf Zielcomputern ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="ba1e8-105">These files contain all the necessary information about an application so the application can run in a virtual environment on target computers.</span></span> <span data-ttu-id="ba1e8-106">Sie können den Microsoft Application Virtualization (App-V)-Sequenzer verwenden, um virtuelle Anwendungen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="ba1e8-106">You can use the Microsoft Application Virtualization (App-V) Sequencer to create virtual applications.</span></span> <span data-ttu-id="ba1e8-107">Nachdem Sie eine Anwendung sequenziert haben, kann Sie auf Zielcomputer gestreamt werden, oder die virtuelle Anwendung kann von Zielcomputern ausgeführt werden, indem der Inhalt des virtuellen Anwendungspakets heruntergeladen und die Anwendung lokal ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ba1e8-107">After you sequence an application, it can be streamed to target computers, or target computers can run the virtual application by downloading the contents of the virtual application package and running the application locally.</span></span>

<span data-ttu-id="ba1e8-108">**Wichtig**  Zum Ausführen eines virtuellen Anwendungspakets muss auf dem Zielcomputer die entsprechende Version des App-V-Clients ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="ba1e8-108">**Important** To run a virtual application package the target computer must be running the appropriate version of the App-V client.</span></span>

 

<span data-ttu-id="ba1e8-109">Virtuelle Anwendungspakete werden auf Zielcomputern ausgeführt, ohne mit dem zugrunde liegenden Betriebssystem auf dem Zielcomputer zu interagieren, da jede Anwendung in einer virtuellen Umgebung ausgeführt wird und von anderen Anwendungen isoliert ist, die auf dem Zielcomputer installiert oder ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="ba1e8-109">Virtual application packages run on target computers without interacting with the underlying operating system on the target computer because each application runs in a virtual environment and is isolated from other applications that are installed or running on the target computer.</span></span> <span data-ttu-id="ba1e8-110">Durch diese Isolierung können Anwendungskonflikte verringert und die erforderliche Anzahl von Anwendungstests vor der Bereitstellung verringert werden.</span><span class="sxs-lookup"><span data-stu-id="ba1e8-110">This isolation can reduce application conflicts and can help decrease the required amount of application pre-deployment testing.</span></span>

## <span data-ttu-id="ba1e8-111">Sequenzer-Terminologie</span><span class="sxs-lookup"><span data-stu-id="ba1e8-111">Sequencer Terminology</span></span>


<a href="" id="application-virtualization-drive"></a><span data-ttu-id="ba1e8-112">Application Virtualization-Laufwerk</span><span class="sxs-lookup"><span data-stu-id="ba1e8-112">Application Virtualization drive</span></span>  
<span data-ttu-id="ba1e8-113">Das Application Virtualization Drive ist das Standardlaufwerk (Laufwerk q:\) auf dem Zielcomputer, aus dem sequenzierte Anwendungen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="ba1e8-113">The application virtualization drive is the default drive (Q:\) on the target computer from which sequenced applications are run.</span></span>

<a href="" id="ico-file"></a><span data-ttu-id="ba1e8-114">ICO-Datei</span><span class="sxs-lookup"><span data-stu-id="ba1e8-114">ICO file</span></span>  
<span data-ttu-id="ba1e8-115">Die Symboldatei auf dem Clientdesktop, die zum Starten einer sequenzierten Anwendung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ba1e8-115">The icon file on the client desktop which is used to launch a sequenced application.</span></span>

<a href="" id="installation-directory"></a><span data-ttu-id="ba1e8-116">Installationsverzeichnis</span><span class="sxs-lookup"><span data-stu-id="ba1e8-116">Installation directory</span></span>  
<span data-ttu-id="ba1e8-117">Das Verzeichnis, das vom Sequencer zum Platzieren von Installationsdateien während des Setups verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ba1e8-117">The directory used by the sequencer to place installation files during setup.</span></span>

<a href="" id="open-software-descriptor--osd--file"></a><span data-ttu-id="ba1e8-118">Open Software Descriptor (OSD)-Datei</span><span class="sxs-lookup"><span data-stu-id="ba1e8-118">Open Software Descriptor (OSD) file</span></span>  
<span data-ttu-id="ba1e8-119">Eine XML-basierte Datei, in der der APP-v-Client angewiesen wird, wie die sequenzierte Anwendung vom APP-v-Streamingserver abgerufen und wie die sequenzierte Anwendung in der virtuellen Umgebung ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="ba1e8-119">An XML-based file that instructs the App-V client how to retrieve the sequenced application from the App-V streaming server and how to run the sequenced application in the virtual environment.</span></span>

<a href="" id="package-root-directory"></a><span data-ttu-id="ba1e8-120">Paketstammverzeichnis</span><span class="sxs-lookup"><span data-stu-id="ba1e8-120">Package root directory</span></span>  
<span data-ttu-id="ba1e8-121">Das Verzeichnis auf dem Sequenzcomputer, auf dem die Dateien für das sequenzierte Anwendungspaket installiert sind.</span><span class="sxs-lookup"><span data-stu-id="ba1e8-121">The directory on the sequencing computer on which files for the sequenced application package are installed.</span></span> <span data-ttu-id="ba1e8-122">Dieses Verzeichnis ist auch virtuell auf dem Computer vorhanden, auf den eine sequenzierte Anwendung gestreamt wird.</span><span class="sxs-lookup"><span data-stu-id="ba1e8-122">This directory also exists virtually on the computer to which a sequenced application will be streamed.</span></span>

<a href="" id="sequenced-application"></a><span data-ttu-id="ba1e8-123">Sequenzierte Anwendung</span><span class="sxs-lookup"><span data-stu-id="ba1e8-123">Sequenced application</span></span>  
<span data-ttu-id="ba1e8-124">Eine Anwendung, die vom Sequencer überwacht wurde, aufgeteilt in primäre und sekundäre Funktionsblöcke, gestreamt auf einem Zielcomputer, auf dem der App-V-Client t ausgeführt wird, und führt eine virtuelle Umgebung aus.</span><span class="sxs-lookup"><span data-stu-id="ba1e8-124">An application that has been monitored by the sequencer, broken up into primary and secondary feature blocks, streamed to a target computer running the App-V client t, and runs a virtual environment.</span></span>

<a href="" id="sequenced-application-package"></a><span data-ttu-id="ba1e8-125">Sequenziertes Anwendungspaket</span><span class="sxs-lookup"><span data-stu-id="ba1e8-125">Sequenced application package</span></span>  
<span data-ttu-id="ba1e8-126">Die Dateien, die eine virtuelle Anwendung enthalten und die Ausführung einer virtuellen Anwendung ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="ba1e8-126">The files that comprise a virtual application and allow a virtual application to run.</span></span> <span data-ttu-id="ba1e8-127">Diese Dateien werden nach der Sequenzierung erstellt und umfassen insbesondere **OSD**-, **SFT**-, **SPRJ**-und **ICO** -Dateien.</span><span class="sxs-lookup"><span data-stu-id="ba1e8-127">These files are created after sequencing and specifically include **.osd**, **.sft**, **.sprj**, and **.ico** files.</span></span>

<a href="" id="sequencing"></a><span data-ttu-id="ba1e8-128">Sequenzierung</span><span class="sxs-lookup"><span data-stu-id="ba1e8-128">Sequencing</span></span>  
<span data-ttu-id="ba1e8-129">Der Vorgang zum Erstellen eines Anwendungspakets mit dem App-V-Sequenzer.</span><span class="sxs-lookup"><span data-stu-id="ba1e8-129">The process of creating an application package using the App-V Sequencer.</span></span> <span data-ttu-id="ba1e8-130">In diesem Prozess wird eine Anwendung überwacht, Ihre Tastenkombinationen konfiguriert und ein sequenziertes Anwendungspaket erstellt.</span><span class="sxs-lookup"><span data-stu-id="ba1e8-130">In this process, an application is monitored, its shortcuts are configured, and a sequenced application package is created.</span></span>

<a href="" id="sequencing-computer"></a><span data-ttu-id="ba1e8-131">Sequenzcomputer</span><span class="sxs-lookup"><span data-stu-id="ba1e8-131">Sequencing computer</span></span>  
<span data-ttu-id="ba1e8-132">Der Computer, mit dem eine Anwendung sequenziert wird.</span><span class="sxs-lookup"><span data-stu-id="ba1e8-132">The computer used to sequence an application.</span></span>

<a href="" id="virtual-application"></a><span data-ttu-id="ba1e8-133">Virtuelle Anwendung</span><span class="sxs-lookup"><span data-stu-id="ba1e8-133">Virtual application</span></span>  
<span data-ttu-id="ba1e8-134">Eine vom Sequencer verpackte Anwendung, die in einer eigenständigen virtuellen Umgebung ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="ba1e8-134">An application packaged by the Sequencer to run in a self-contained, virtual environment.</span></span> <span data-ttu-id="ba1e8-135">Die virtuelle Umgebung enthält die Informationen, die erforderlich sind, um die Anwendung auf dem Client auszuführen, ohne die Anwendung lokal zu installieren.</span><span class="sxs-lookup"><span data-stu-id="ba1e8-135">The virtual environment contains the information necessary to run the application on the client without installing the application locally.</span></span>

<a href="" id="primary-feature-block"></a><span data-ttu-id="ba1e8-136">Primärer Feature-Block</span><span class="sxs-lookup"><span data-stu-id="ba1e8-136">Primary feature block</span></span>  
<span data-ttu-id="ba1e8-137">Der minimale Inhalt eines virtuellen Anwendungspakets, das für die Ausführung einer Anwendung auf einem Zielcomputer erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="ba1e8-137">The minimum content in a virtual application package that is necessary for an application to run on a target computer.</span></span> <span data-ttu-id="ba1e8-138">Der Inhalt des primären Funktionsblocks wird während der Anwendungsphase der Sequenzierung identifiziert und besteht in der Regel aus dem Inhalt der am häufigsten verwendeten Anwendungsfeatures.</span><span class="sxs-lookup"><span data-stu-id="ba1e8-138">The content in the primary feature block is identified during the application phase of sequencing and typically consists of the content for the most used application features.</span></span>

## <a href="" id="sequencing-applications-"></a><span data-ttu-id="ba1e8-139">Sequenzierung von Anwendungen</span><span class="sxs-lookup"><span data-stu-id="ba1e8-139">Sequencing Applications</span></span>


<span data-ttu-id="ba1e8-140">Es gibt zwei Methoden zum Erstellen und Ändern von virtuellen Anwendungspaketen in Ihrer Umgebung.</span><span class="sxs-lookup"><span data-stu-id="ba1e8-140">There are two methods to create and modify virtual application packages in your environment.</span></span> <span data-ttu-id="ba1e8-141">Die erste Methode ist die Verwendung des **Sequenz** -Assistenten.</span><span class="sxs-lookup"><span data-stu-id="ba1e8-141">The first method is by using the **Sequencing** wizard.</span></span> <span data-ttu-id="ba1e8-142">Mit dem **Sequenz** -Assistenten können Sie neue, vorhandene virtuelle Anwendungspakete erstellen oder ändern.</span><span class="sxs-lookup"><span data-stu-id="ba1e8-142">The **Sequencing** wizard allows you to create new, or modify existing virtual application packages.</span></span> <span data-ttu-id="ba1e8-143">Weitere Informationen zur Verwendung des **Sequenz** -Assistenten finden Sie unter [so wird es gemacht: Sequenzierung einer neuen Anwendung](how-to-sequence-a-new-application.md).</span><span class="sxs-lookup"><span data-stu-id="ba1e8-143">For more information about using the **Sequencing** wizard see, [How to Sequence a New Application](how-to-sequence-a-new-application.md).</span></span> <span data-ttu-id="ba1e8-144">Die zweite Methode ist die Verwendung der Befehlszeile.</span><span class="sxs-lookup"><span data-stu-id="ba1e8-144">The second method is by using the command-line.</span></span> <span data-ttu-id="ba1e8-145">Über die Befehlszeile können Sie mit der Eingabeaufforderung neue, vorhandene virtuelle Anwendungspakete erstellen oder ändern.</span><span class="sxs-lookup"><span data-stu-id="ba1e8-145">The command-line allows you to create new, or modify existing virtual application packages using the command prompt.</span></span> <span data-ttu-id="ba1e8-146">Weitere Informationen zur Verwendung der Befehlszeile finden Sie unter [Verwalten virtueller Anwendungen über die Befehlszeile](how-to-manage-virtual-applications-using-the-command-line.md).</span><span class="sxs-lookup"><span data-stu-id="ba1e8-146">For more information about using the command line see, [How to Manage Virtual Applications Using the Command Line](how-to-manage-virtual-applications-using-the-command-line.md).</span></span>

<span data-ttu-id="ba1e8-147">Der **Sequenz** -Assistent bietet die folgenden Funktionen zum Erstellen virtueller Anwendungspakete:</span><span class="sxs-lookup"><span data-stu-id="ba1e8-147">The **Sequencing** wizard provides the following functions for creating virtual application packages:</span></span>

1.  <span data-ttu-id="ba1e8-148">**Paketkonfiguration**: der **Sequenz** -Assistent fordert zum Ausführen der OSD-Datei (Open Software Descriptor) Informationen zur Paketkonfiguration auf, bei der es sich um eine erforderliche Datei zum Starten eines sequenzierten Anwendungspakets handelt.</span><span class="sxs-lookup"><span data-stu-id="ba1e8-148">**Package Configuration**: The **Sequencing** Wizard prompts for package configuration information necessary to complete the Open Software Descriptor (OSD) file, which is a required file for starting a sequenced application package.</span></span>

2.  <span data-ttu-id="ba1e8-149">**Anwendungsinstallation**: der **Sequenz** -Assistent sammelt Informationen zu den Installations-und Startkonfigurationen einer Anwendung.</span><span class="sxs-lookup"><span data-stu-id="ba1e8-149">**Application Installation**: The **Sequencing** Wizard gathers information about an application’s installation and startup configurations.</span></span> <span data-ttu-id="ba1e8-150">Es überwacht und zeichnet die Installations-und Startinformationen auf, die mit der Anwendung verknüpft sind, um die Dateien zu erstellen, die für ein virtuelles Anwendungspaket erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="ba1e8-150">It monitors and records the installation and startup information associated with the application to create the files necessary for a virtual application package.</span></span>

3.  <span data-ttu-id="ba1e8-151">**Anwendungsstart**: der **Sequenz** -Assistent sammelt Informationen zum Kompilieren und Sortieren der Codeblöcke, die erforderlich sind, um den ersten Start des sequenzierten Anwendungspakets auf dem Zielcomputer durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="ba1e8-151">**Application Startup**: The **Sequencing** Wizard gathers information for compiling and ordering the blocks of code necessary to perform the initial startup of the sequenced application package on the target computer.</span></span> <span data-ttu-id="ba1e8-152">Die Kompilierung des Codeblocks wird als primärer Feature-Block bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="ba1e8-152">The compilation of the code block is referred to as the primary feature block.</span></span>

## <span data-ttu-id="ba1e8-153">Sicherheitsüberlegungen zu Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="ba1e8-153">Application Virtualization Sequencer Security Considerations</span></span>


<span data-ttu-id="ba1e8-154">Der App-V-Sequencer führt alle Dienste, die zur Sequenzierung erkannt werden, unter Verwendung des lokalen System Kontos aus, und es werden keine Sicherheitsbeschreibungen für Dienststeuerungsanforderungen erzwungen.</span><span class="sxs-lookup"><span data-stu-id="ba1e8-154">The App-V Sequencer runs all services detected at sequencing time using the Local System account and does not enforce security descriptors on service control requests.</span></span> <span data-ttu-id="ba1e8-155">Wenn der Dienst mit einem anderen Benutzerkonto installiert wurde oder wenn die Sicherheitsbeschreibungen anderen Benutzergruppen bestimmte Dienstberechtigungen erteilen sollen, sollten Sie sorgfältig überlegen, ob der Dienst virtualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="ba1e8-155">If the service was installed using a different user account or if the security descriptors are intended to grant different user groups specific service permissions, consider carefully whether the service should be virtualized.</span></span> <span data-ttu-id="ba1e8-156">In einigen Fällen sollten Sie den Dienst lokal installieren, um sicherzustellen, dass die vorgesehene Dienstsicherheit erhalten bleibt.</span><span class="sxs-lookup"><span data-stu-id="ba1e8-156">In some cases, you should install the service locally to ensure that the intended service security is preserved.</span></span>

<span data-ttu-id="ba1e8-157">**Wichtig**  Sie sollten virtuelle Anwendungspakete immer an einem sicheren Ort speichern.</span><span class="sxs-lookup"><span data-stu-id="ba1e8-157">**Important** You should always save virtual application packages in a secure location.</span></span>

 

## <span data-ttu-id="ba1e8-158">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="ba1e8-158">Related topics</span></span>


[<span data-ttu-id="ba1e8-159">Application Virtualization Sequencer – Übersicht</span><span class="sxs-lookup"><span data-stu-id="ba1e8-159">Application Virtualization Sequencer Overview</span></span>](application-virtualization-sequencer-overview.md)

 

 





