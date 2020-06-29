---
title: Übersicht über Application Virtualization Sequencer Console
description: Übersicht über Application Virtualization Sequencer Console
author: dansimp
ms.assetid: 681bb40d-2937-4645-82aa-4a44775232d8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4c2f977fccaaded0309181a1d74c16b749498abb
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809208"
---
# <span data-ttu-id="84c2b-103">Übersicht über Application Virtualization Sequencer Console</span><span class="sxs-lookup"><span data-stu-id="84c2b-103">Application Virtualization Sequencer Console Overview</span></span>


<span data-ttu-id="84c2b-104">Der Application Virtualization (App-V)-Sequenzer erstellt Anwendungen, damit Sie in einer virtuellen Umgebung als virtuelle Anwendungen ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="84c2b-104">The Application Virtualization (App-V) Sequencer creates applications so that they can be run in a virtual environment, as virtual applications.</span></span> <span data-ttu-id="84c2b-105">Nachdem eine Anwendung sequenziert wurde, kann Sie von einem App-v-Server ausgeführt werden, um auf Computern, auf denen der APP-v-Desktop Client ausgeführt wird, oder auf dem App-v-Client für Remote Desktop Dienste (ehemals Terminal Dienste) mithilfe eines Prozesses, der als Streaming bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="84c2b-105">After an application has been sequenced, it can run from an App-V Server to target computers that are running the App-V Desktop Client or the App-V Client for Remote Desktop Services (formerly Terminal Services) by using a process called streaming.</span></span> <span data-ttu-id="84c2b-106">Der App-V-Sequencer überwacht den Installations-und Einrichtungsprozess für Anwendungen und zeichnet alle Informationen auf, die für die Ausführung der Anwendung in der virtuellen Umgebung erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="84c2b-106">The App-V Sequencer monitors the installation and setup process for applications, and it records all the information necessary for the application to run in the virtual environment.</span></span> <span data-ttu-id="84c2b-107">Dieser Prozess bestimmt auch, welche Dateien und Konfigurationen für alle Benutzer gelten und welche Konfigurationen Benutzer anpassen können.</span><span class="sxs-lookup"><span data-stu-id="84c2b-107">This process also determines which files and configurations are applicable to all users and which configurations users can customize.</span></span> <span data-ttu-id="84c2b-108">Virtuelle Anwendungen werden auf Zielcomputern ausgeführt und haben keine Auswirkungen auf das auf dem Zielcomputer ausgeführte Betriebssystem oder auf Anwendungen, die auf dem Zielcomputer installiert sind.</span><span class="sxs-lookup"><span data-stu-id="84c2b-108">Virtual applications run on target computers and have no effect on the operating system running on the target computer or on any applications that are installed on the target computer.</span></span>

## <span data-ttu-id="84c2b-109">Sicherheitsüberlegungen zu Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="84c2b-109">Application Virtualization Sequencer Security Considerations</span></span>


<span data-ttu-id="84c2b-110">Der App-V-Sequencer führt alle Dienste, die zur Sequenzierung erkannt werden, unter Verwendung des lokalen System Kontos aus, und es werden keine Sicherheitsbeschreibungen für Dienststeuerungsanforderungen erzwungen.</span><span class="sxs-lookup"><span data-stu-id="84c2b-110">The App-V Sequencer runs all services detected at sequencing time using the Local System account and does not enforce security descriptors on service control requests.</span></span> <span data-ttu-id="84c2b-111">Wenn der Dienst mit einem anderen Benutzerkonto installiert wurde oder wenn die Sicherheitsbeschreibungen anderen Benutzergruppen bestimmte Dienstberechtigungen erteilen sollen, sollten Sie sorgfältig überlegen, ob der Dienst virtualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="84c2b-111">If the service was installed using a different user account or if the security descriptors are intended to grant different user groups specific service permissions, consider carefully whether the service should be virtualized.</span></span> <span data-ttu-id="84c2b-112">In einigen Fällen sollten Sie den Dienst lokal installieren, um sicherzustellen, dass die vorgesehene Dienstsicherheit erhalten bleibt.</span><span class="sxs-lookup"><span data-stu-id="84c2b-112">In some cases, you should install the service locally to ensure that the intended service security is preserved.</span></span>

## <span data-ttu-id="84c2b-113">Menü Optionen für Application Virtualization Sequencer-Konsole</span><span class="sxs-lookup"><span data-stu-id="84c2b-113">Application Virtualization Sequencer Console Menu Options</span></span>


<span data-ttu-id="84c2b-114">Die folgenden Menüelemente stehen in der App-V Sequencer-Konsole zur Verfügung:</span><span class="sxs-lookup"><span data-stu-id="84c2b-114">The following menu items are available in the App-V Sequencer Console:</span></span>

-   <span data-ttu-id="84c2b-115">**Datei**– enthält verschiedene Befehle, mit denen Sie sequenzierte Anwendungen erstellen, öffnen, ändern und speichern können.</span><span class="sxs-lookup"><span data-stu-id="84c2b-115">**File**—Contains various commands to help create, open, modify, and save sequenced applications.</span></span>

-   <span data-ttu-id="84c2b-116">**Bearbeiten**– enthält verschiedene Befehle zum Bearbeiten vorhandener virtueller Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="84c2b-116">**Edit**—Contains various commands for editing existing virtual applications.</span></span>

-   <span data-ttu-id="84c2b-117">**Ansicht**– enthält verschiedene Befehle zum Anzeigen der Eigenschaften einer virtuellen Anwendung.</span><span class="sxs-lookup"><span data-stu-id="84c2b-117">**View**—Contains various commands for viewing properties of a virtual application.</span></span>

-   <span data-ttu-id="84c2b-118">**Tools**– enthält verschiedene Tools und Diagnosen für die Konfiguration virtueller Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="84c2b-118">**Tools**—Contains various tools and diagnostics for configuring virtual applications.</span></span>

## <span data-ttu-id="84c2b-119">Toolbar-Optionen für Application Virtualization Sequencer-Konsole</span><span class="sxs-lookup"><span data-stu-id="84c2b-119">Application Virtualization Sequencer Console Toolbar Options</span></span>


<span data-ttu-id="84c2b-120">Die folgenden Symbolleistenschaltflächen sind in der App-V Sequencer-Konsole verfügbar:</span><span class="sxs-lookup"><span data-stu-id="84c2b-120">The following toolbar buttons are available in the App-V Sequencer Console:</span></span>

-   <span data-ttu-id="84c2b-121">**Neues Paket**– klicken Sie hier, um eine neue sequenzierte Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="84c2b-121">**New Package**—Click to create a new sequenced application.</span></span>

-   <span data-ttu-id="84c2b-122">**Öffnen**– klicken Sie auf, um ein sequenziertes Anwendungspaket in der App-V Sequencer-Konsole zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="84c2b-122">**Open**—Click to open a sequenced application package in the App-V Sequencer Console.</span></span>

-   <span data-ttu-id="84c2b-123">**Für Upgrade öffnen**– klicken Sie auf, um eine sequenzierte Anwendung zu öffnen, um ein Update zu aktualisieren oder anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="84c2b-123">**Open for Upgrade**—Click to open a sequenced application to upgrade or apply an update.</span></span>

-   <span data-ttu-id="84c2b-124">**Speichern**– klicken Sie, um eine sequenzierte virtuelle Anwendung zu speichern.</span><span class="sxs-lookup"><span data-stu-id="84c2b-124">**Save**—Click to save a sequenced virtual application.</span></span>

-   <span data-ttu-id="84c2b-125">**Sequenz-Assistent**– klicken Sie, um den Sequenz-Assistenten zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="84c2b-125">**Sequencing Wizard**—Click to open the Sequencing Wizard.</span></span> <span data-ttu-id="84c2b-126">Mit dieser Schaltfläche können Sie den Sequenz-Assistenten starten, wenn Sie auf der Registerkarte **Allgemein** unter **Extras**  /  **Optionen**Änderungen vornehmen.</span><span class="sxs-lookup"><span data-stu-id="84c2b-126">You should use this button to start the Sequencing Wizard if you make any changes on the **General** tab under **Tools** / **Options**.</span></span>

## <span data-ttu-id="84c2b-127">Registerkarten für virtuelle Anwendungen</span><span class="sxs-lookup"><span data-stu-id="84c2b-127">Virtual Application Tabs</span></span>


<span data-ttu-id="84c2b-128">Wenn Sie eine virtuelle Anwendung in der App-V Sequencer-Konsole anzeigen, werden die folgenden Registerkarten angezeigt:</span><span class="sxs-lookup"><span data-stu-id="84c2b-128">The following tabs are displayed when you view a virtual application in the App-V Sequencer Console:</span></span>

-   <span data-ttu-id="84c2b-129">**Eigenschaften**– zeigt Informationen zur ausgewählten virtuellen Anwendung an.</span><span class="sxs-lookup"><span data-stu-id="84c2b-129">**Properties**—Displays information about the selected virtual application.</span></span> <span data-ttu-id="84c2b-130">Sie können den **Paketnamen** und die **Kommentare** aktualisieren, die der virtuellen Anwendung zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="84c2b-130">You can update the **Package Name** and **Comments** associated with the virtual application.</span></span>

-   <span data-ttu-id="84c2b-131">**Bereitstellung**– zeigt Informationen dazu an, wie auf den Zielcomputern auf die virtuelle Anwendung zugegriffen wird.</span><span class="sxs-lookup"><span data-stu-id="84c2b-131">**Deployment**—Displays information about how the virtual application will be accessed by target computers.</span></span> <span data-ttu-id="84c2b-132">Sie können die Bereitstellungsmethode für die virtuelle Anwendung konfigurieren, und Sie können konfigurieren, welche Betriebssysteme auf dem Zielcomputer ausgeführt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="84c2b-132">You can configure the virtual application delivery method, and you can configure which operating systems must be running on the target computer.</span></span> <span data-ttu-id="84c2b-133">Sie können auch die zugehörigen Ausgabeoptionen konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="84c2b-133">You can also configure the associated output options.</span></span> <span data-ttu-id="84c2b-134">Wenn Sie planen, dass Clients auf eine virtuelle Anwendung aus einer Datei zugreifen können, verwenden Sie das folgende Format, wenn Sie den Pfad angeben: **file://Server/Share/Path/.SFT**.</span><span class="sxs-lookup"><span data-stu-id="84c2b-134">If you plan to have clients access a virtual application from a file, use the following format when specifying the path: **File://server/share/path/.sft**.</span></span> <span data-ttu-id="84c2b-135">Wählen Sie **Sicherheitsbeschreibungen erzwingen** aus, um die mit dem Paket während eines Upgrades verknüpfte Sicherheit beizubehalten, oder die Berechtigungen werden während des Upgrades zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="84c2b-135">Select **Enforce Security Descriptors** to preserve security associated with the package during an upgrade, or the permissions will be reset during the upgrade.</span></span>

-   <span data-ttu-id="84c2b-136">**Protokoll ändern**– zeigt Informationen zu Updates an, die an der virtuellen Anwendung vorgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="84c2b-136">**Change History**—Displays information about updates that have been made to the virtual application.</span></span>

-   <span data-ttu-id="84c2b-137">**Dateien**– zeigt die Dateien an, die der ausgewählten virtuellen Anwendung zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="84c2b-137">**Files**—Displays the files associated with the selected virtual application.</span></span> <span data-ttu-id="84c2b-138">Sie können kleinere Änderungen an den zugehörigen Dateieigenschaften vornehmen, indem Sie die entsprechenden Felder verwenden.</span><span class="sxs-lookup"><span data-stu-id="84c2b-138">You can make minor revisions to the associated file properties by using the appropriate fields.</span></span>

-   <span data-ttu-id="84c2b-139">**Virtuelle Registrierung**– zeigt die virtuelle Registrierung an, die der ausgewählten virtuellen Anwendung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="84c2b-139">**Virtual Registry**—Displays the virtual registry associated with the selected virtual application.</span></span> <span data-ttu-id="84c2b-140">Sie können Registrierungsschlüssel hinzufügen oder löschen, indem Sie mit der rechten Maustaste auf den entsprechenden Eintrag klicken.</span><span class="sxs-lookup"><span data-stu-id="84c2b-140">You can add or delete registry keys by right-clicking the appropriate entry.</span></span>

-   <span data-ttu-id="84c2b-141">**Virtuelles Datei System**– zeigt die virtuellen Dateisysteme an, die der ausgewählten virtuellen Anwendung zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="84c2b-141">**Virtual File System**—Displays the virtual file systems associated with the selected virtual application.</span></span> <span data-ttu-id="84c2b-142">Auf dieser Registerkarte können Sie Dateisystemeinträge hinzufügen, löschen oder bearbeiten, indem Sie mit der rechten Maustaste auf den entsprechenden Eintrag klicken und die Option auswählen.</span><span class="sxs-lookup"><span data-stu-id="84c2b-142">You can add, delete, or edit file system entries on this tab by right-clicking the appropriate entry and selecting the option.</span></span>

-   <span data-ttu-id="84c2b-143">**Virtuelle Dienste**– zeigt die Dienste an, die der ausgewählten virtuellen Anwendung zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="84c2b-143">**Virtual Services**—Displays the services associated with the selected virtual application.</span></span>

-   <span data-ttu-id="84c2b-144">**OSD**– zeigt Informationen zur geöffneten Software Beschreibung (OSD) an, die der virtuellen Anwendung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="84c2b-144">**OSD**—Displays information about the Open Software Descriptor (OSD) associated with the virtual application.</span></span> <span data-ttu-id="84c2b-145">Sie können die Dateien aktualisieren, die der OSD-Datei zugeordnet sind, indem Sie mit der rechten Maustaste auf den entsprechenden Eintrag klicken und die gewünschte Aktion auswählen.</span><span class="sxs-lookup"><span data-stu-id="84c2b-145">You can update the files associated with the OSD file by right-clicking the appropriate entry and selecting the action that you want.</span></span>

## <span data-ttu-id="84c2b-146">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="84c2b-146">Related topics</span></span>


[<span data-ttu-id="84c2b-147">Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="84c2b-147">Application Virtualization Sequencer</span></span>](application-virtualization-sequencer.md)

 

 





