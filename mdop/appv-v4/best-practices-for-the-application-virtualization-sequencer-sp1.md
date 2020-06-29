---
title: Bewährte Methoden für Application Virtualization Sequencer
description: Bewährte Methoden für Application Virtualization Sequencer
author: dansimp
ms.assetid: 95e5e216-864f-41a1-90d4-b8d7e1eb42a0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d859514fb34185a339c7f2c2734f331e5a99d050
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809091"
---
# <span data-ttu-id="950f7-103">Bewährte Methoden für Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="950f7-103">Best Practices for the Application Virtualization Sequencer</span></span>


<span data-ttu-id="950f7-104">In diesem Thema finden Sie bewährte Methoden zum Ausführen des Microsoft Application Virtualization (App-V)-Sequencers.</span><span class="sxs-lookup"><span data-stu-id="950f7-104">This topic provides best practices for running the Microsoft Application Virtualization (App-V) Sequencer.</span></span> <span data-ttu-id="950f7-105">Überprüfen und berücksichtigen Sie bei der Planung und Verwendung des Sequencers in Ihrer Umgebung die folgenden Empfehlungen.</span><span class="sxs-lookup"><span data-stu-id="950f7-105">Review and consider the following recommendations when planning and using the Sequencer in your environment.</span></span>

## <span data-ttu-id="950f7-106">Bewährte Methoden für die Sequenzierung von Computer Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="950f7-106">Sequencing Computer Configuration Best Practices</span></span>


<span data-ttu-id="950f7-107">Bei der Konfiguration des Computers, auf dem der App-V-Sequencer ausgeführt wird, sollten die folgenden bewährten Methoden berücksichtigt werden:</span><span class="sxs-lookup"><span data-stu-id="950f7-107">The following best practices should be considered when configuring the computer running the App-V Sequencer:</span></span>

-   **<span data-ttu-id="950f7-108">Sequenz auf einem Computer mit einer ähnlichen Konfiguration, auf der eine frühere Version des Betriebssystems als auf den Zielcomputern ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="950f7-108">Sequence on a computer that has a similar configuration and that is running an earlier version of the operating system than the target computers.</span></span>**

    <span data-ttu-id="950f7-109">Stellen Sie sicher, dass auf dem Computer, auf dem der Sequencer ausgeführt wird, eine frühere Version des Betriebssystems als auf den Zielcomputern ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="950f7-109">Ensure that the computer that is running the Sequencer is running an earlier version of the operating system than the target computers.</span></span> <span data-ttu-id="950f7-110">Dazu gehören die Versionen des Service Packs und Updates.</span><span class="sxs-lookup"><span data-stu-id="950f7-110">This includes the service pack and update versions.</span></span> <span data-ttu-id="950f7-111">Wenn beispielsweise auf den Zielcomputern Windows Vista und WindowsXP ausgeführt werden, sollten Sie Anwendungen auf einem Computer mit WindowsXP sequenzieren.</span><span class="sxs-lookup"><span data-stu-id="950f7-111">For example, if the target computers are running WindowsVista and WindowsXP, you should sequence applications on a computer that is running WindowsXP.</span></span> <span data-ttu-id="950f7-112">Die Möglichkeit zur Sequenzierung auf einem Betriebssystem und zum Ausführen der virtualisierten Anwendung unter einem anderen Betriebssystem ist nicht garantiert und hängt von der jeweiligen Anwendung und dem jeweiligen Betriebssystem ab.</span><span class="sxs-lookup"><span data-stu-id="950f7-112">The ability to sequence on one operating system and run the virtualized application on a different operating system is not guaranteed, and depends on the particular application and operating system.</span></span> <span data-ttu-id="950f7-113">Wenn Probleme auftreten, müssen Sie möglicherweise eine Sequenz unter der gleichen Betriebssystemumgebung ausführen, auf der der App-V-Client ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="950f7-113">If you encounter issues, you may be required to sequence on the same operating system environment as the one on which the App-V client is running.</span></span>

-   **<span data-ttu-id="950f7-114">Konfigurieren Sie den Computer, auf dem der Sequencer ausgeführt wird, mit mehreren Partitionen.</span><span class="sxs-lookup"><span data-stu-id="950f7-114">Configure the computer running the Sequencer with multiple partitions.</span></span>**

    <span data-ttu-id="950f7-115">Sie sollten den Computer, auf dem der Sequencer ausgeführt wird, mit mindestens zwei primären Partitionen konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="950f7-115">You should configure the computer running the Sequencer with at least two primary partitions.</span></span> <span data-ttu-id="950f7-116">Die erste Partition (**C:**) sollte das Betriebssystem enthalten und mit dem NTFS-Dateisystem formatiert werden.</span><span class="sxs-lookup"><span data-stu-id="950f7-116">The first partition (**C:**) should contain the operating system, and it should be formatted using the NTFS file system.</span></span> <span data-ttu-id="950f7-117">Die zweite Partition (**Q:**) wird als Zielpfad für die Installation der virtuellen Anwendung verwendet und sollte auch mit dem NTFS-Dateisystem formatiert werden.</span><span class="sxs-lookup"><span data-stu-id="950f7-117">The second partition (**Q:**) is used as the destination path for the virtual application installation and should also be formatted using the NTFS file system.</span></span>

-   **<span data-ttu-id="950f7-118">Konfigurieren Sie das temporäre Verzeichnis mit genügend freiem Speicherplatz.</span><span class="sxs-lookup"><span data-stu-id="950f7-118">Configure the temp directory with enough free disk space.</span></span>**

    <span data-ttu-id="950f7-119">Der Sequencer verwendet das Verzeichnis **% tmp%** oder **% Temp%** und das **Scratch** -Verzeichnis, um temporäre Dateien während der Sequenzierung zu speichern.</span><span class="sxs-lookup"><span data-stu-id="950f7-119">The Sequencer uses the **%TMP%** or **%TEMP%** directory and the **Scratch** directory to store temporary files during sequencing.</span></span> <span data-ttu-id="950f7-120">Sie sollten diese Verzeichnisse auf dem Computer, auf dem der Sequencer ausgeführt wird, mit freiem Speicherplatz konfigurieren, der den geschätzten Anwendungs Installationsanforderungen entspricht.</span><span class="sxs-lookup"><span data-stu-id="950f7-120">You should configure these directories on the computer running the Sequencer with free disk space equivalent to the estimated application installation requirements.</span></span> <span data-ttu-id="950f7-121">Sie können den Speicherort des **Scratch** -Verzeichnisses überprüfen, indem Sie die Sequencer-Konsole öffnen und **Tools**, **Optionen**und dann die Registerkarte **Pfade** auswählen. die Konfiguration der temporären Verzeichnisse und des **Scratch** -Verzeichnisses auf verschiedenen Festplattenpartitionen kann die Leistung während der Sequenzierung verbessern.</span><span class="sxs-lookup"><span data-stu-id="950f7-121">You can verify the location of the **Scratch** directory by opening the Sequencer console and selecting **Tools**, **Options**, and then selecting the **Paths** tab. Configuring the temp directories and the **Scratch** directory on different hard drive partitions can improve performance during sequencing.</span></span>

-   **<span data-ttu-id="950f7-122">Sequenz Anwendungen mithilfe von Microsoft VirtualPC</span><span class="sxs-lookup"><span data-stu-id="950f7-122">Sequence applications by using Microsoft VirtualPC.</span></span>**

    <span data-ttu-id="950f7-123">Die meisten Anwendungen werden mehrmals sequenziert.</span><span class="sxs-lookup"><span data-stu-id="950f7-123">You will sequence most applications more than once.</span></span> <span data-ttu-id="950f7-124">Um dies zu erleichtern, sollten Sie die Sequenzierung auf einem Computer in einer virtuellen Umgebung in Frage stellen.</span><span class="sxs-lookup"><span data-stu-id="950f7-124">To help facilitate this, you should consider sequencing on a computer running in a virtual environment.</span></span> <span data-ttu-id="950f7-125">Auf diese Weise können Sie eine Anwendung sequenzieren und mit minimaler Neukonfiguration auf dem Computer, auf dem der Sequencer ausgeführt wird, zu einem sauberen Zustand zurückkehren.</span><span class="sxs-lookup"><span data-stu-id="950f7-125">This will allow you to sequence an application and revert to a clean state, with minimal reconfiguration, on the computer that is running the Sequencer.</span></span>

    <span data-ttu-id="950f7-126">Wenn Sie Microsoft Hyper-v in Ihrer Umgebung ausführen, wird der APP-v-Sequencer ausgeführt, wenn der virtuelle Hyper-v-Computer ausgeführt wird:</span><span class="sxs-lookup"><span data-stu-id="950f7-126">If you are running Microsoft Hyper-V in your environment the App-V sequencer will run when the Hyper-V virtual computer it is running on is:</span></span>

    -   <span data-ttu-id="950f7-127">angehalten und fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="950f7-127">paused and resumed.</span></span>

    -   <span data-ttu-id="950f7-128">hat den Zustand gespeichert und wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="950f7-128">has its state saved and restored.</span></span>

    -   <span data-ttu-id="950f7-129">als Snapshot gespeichert und wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="950f7-129">saved as a snapshot and is restored.</span></span>

    -   <span data-ttu-id="950f7-130">im Rahmen einer Livemigration zu einer anderen Hardware migriert.</span><span class="sxs-lookup"><span data-stu-id="950f7-130">migrated to different hardware as part of a live migration.</span></span>

-   **<span data-ttu-id="950f7-131">Bevor Sie eine neue Anwendung sequenzieren, fahren Sie andere ausgeführte Programme herunter.</span><span class="sxs-lookup"><span data-stu-id="950f7-131">Before you sequence a new application, shut down other running programs.</span></span>**

    <span data-ttu-id="950f7-132">Prozesse und geplante Aufgaben, die normalerweise auf dem Sequenzcomputer ausgeführt werden, können den Sequenzierungsprozess verlangsamen und dazu führen, dass bei der Sequenzierung irrelevante Daten gesammelt werden.</span><span class="sxs-lookup"><span data-stu-id="950f7-132">Processes and scheduled tasks that normally run on the sequencing computer can slow down the sequencing process and cause irrelevant data to be gathered during sequencing.</span></span> <span data-ttu-id="950f7-133">Alle unnötigen Anwendungen und Programme sollten geschlossen werden, bevor Sie mit der Sequenzierung beginnen.</span><span class="sxs-lookup"><span data-stu-id="950f7-133">All unnecessary applications and programs should be shut down before you begin sequencing.</span></span>

-   **<span data-ttu-id="950f7-134">Sequenz auf einem Computer, auf dem die Terminal Dienste ausgeführt werden</span><span class="sxs-lookup"><span data-stu-id="950f7-134">Sequence on a computer that is running Terminal Services</span></span>**

    <span data-ttu-id="950f7-135">Sie sollten den Installationsmodus nicht auf einem Computer konfigurieren, auf dem die Terminal Dienste ausgeführt werden, bevor Sie den Sequencer installieren.</span><span class="sxs-lookup"><span data-stu-id="950f7-135">You should not configure the install mode on a computer that is running Terminal Services before you install the sequencer.</span></span>

## <span data-ttu-id="950f7-136">Bewährte Methoden für die Sequenzierung</span><span class="sxs-lookup"><span data-stu-id="950f7-136">Sequencing Best Practices</span></span>


<span data-ttu-id="950f7-137">Bei der Sequenzierung einer neuen Anwendung sollten die folgenden bewährten Methoden berücksichtigt werden:</span><span class="sxs-lookup"><span data-stu-id="950f7-137">The following best practices should be considered when sequencing a new application:</span></span>

-   

    <span data-ttu-id="950f7-138">**Hinweis**  Wenn Sie mit App-V 4,6 SP1 arbeiten, müssen Sie keine Sequenz zu einem Verzeichnis ausführen, das der 8,3-Benennungskonvention folgt.</span><span class="sxs-lookup"><span data-stu-id="950f7-138">**Note** If you are running App-V 4.6 SP1 you do not need to sequence to a directory that follows the 8.3 naming convention.</span></span>

     

-   **<span data-ttu-id="950f7-139">Sequenz zu einem eindeutigen Verzeichnis, das der 8,3-Benennungskonvention folgt.</span><span class="sxs-lookup"><span data-stu-id="950f7-139">Sequence to a unique directory that follows the 8.3 naming convention.</span></span>**

    <span data-ttu-id="950f7-140">Sie sollten alle Anwendungen in einem Verzeichnis abgleichen, das der 8,3-Benennungskonvention folgt.</span><span class="sxs-lookup"><span data-stu-id="950f7-140">You should sequence all applications to a directory that follows the 8.3 naming convention.</span></span> <span data-ttu-id="950f7-141">Der angegebene Verzeichnisname darf nicht mehr als acht Zeichen enthalten, gefolgt von einer dreistelligen Dateinamenerweiterung – beispielsweise **Q:\\MYAPP. ABC**.</span><span class="sxs-lookup"><span data-stu-id="950f7-141">The specified directory name cannot contain more than eight characters, followed by a three-character file name extension—for example, **Q:\\MYAPP.ABC**.</span></span>

-   **<span data-ttu-id="950f7-142">Sequenz in einen Zielordner im Stammverzeichnis des Laufwerks, nicht in ein Unterverzeichnis.</span><span class="sxs-lookup"><span data-stu-id="950f7-142">Sequence to a destination folder on the root of the drive, not to a subdirectory.</span></span>**

    <span data-ttu-id="950f7-143">Wenn die Anwendungssuite mehrere Teile enthält, installieren Sie die einzelnen Anwendungen in einem Unterverzeichnis des Hauptverzeichnisses.</span><span class="sxs-lookup"><span data-stu-id="950f7-143">If the application suite has multiple parts, install each application to a subdirectory of the main directory.</span></span> <span data-ttu-id="950f7-144">Wenn beispielsweise ein Paket zusammen mit einem Client eine Anwendung enthält, verwenden Sie **Q:\\AppSuite** als Hauptverzeichnis, und Sequenzieren Sie die Hauptanwendung zu **Q:\\AppSuite\\Main**, und führen Sie den Client zu **Q:\\AppSuite\\Client**aus.</span><span class="sxs-lookup"><span data-stu-id="950f7-144">For example, if a package contains an application along with a client, use **Q:\\AppSuite** as the main directory and sequence the main application to **Q:\\AppSuite\\Main**, and sequence the client to **Q:\\AppSuite\\Client**.</span></span>

-   **<span data-ttu-id="950f7-145">Konfigurieren und testen Sie die Anwendung während der Installationsphase.</span><span class="sxs-lookup"><span data-stu-id="950f7-145">Configure and test the application during the installation phase.</span></span>**

    <span data-ttu-id="950f7-146">Zum Abschluss der Installation einer Anwendung müssen häufig mehrere manuelle Schritte ausgeführt werden, die nicht Teil des Installationsvorgangs der Anwendung sind.</span><span class="sxs-lookup"><span data-stu-id="950f7-146">Completing the installation of an application often requires performing several manual steps that are not part of the application installation process.</span></span> <span data-ttu-id="950f7-147">Diese Schritte können die Konfiguration einer Verbindung zu einer Datenbank oder das Kopieren aktualisierter Dateien beinhalten.</span><span class="sxs-lookup"><span data-stu-id="950f7-147">These steps can involve configuring a connection to a database or copying updated files.</span></span> <span data-ttu-id="950f7-148">Führen Sie diese Konfigurationen während der Installationsphase aus, und führen Sie dann die Anwendung aus, um sicherzustellen, dass Sie funktioniert.</span><span class="sxs-lookup"><span data-stu-id="950f7-148">You should perform these configurations during the installation phase and then run the application to make sure it works.</span></span>

-   **<span data-ttu-id="950f7-149">Führen Sie die Anwendung, falls erforderlich, mehrmals aus, bis das Programm stabil ist.</span><span class="sxs-lookup"><span data-stu-id="950f7-149">Run the application, multiple times if necessary, until the program is stable.</span></span>**

    <span data-ttu-id="950f7-150">Sie sollten die Anwendung während der Installation mehrmals ausführen, um sicherzustellen, dass alle zugehörigen Registrierungs-und Dialogfeld Konfigurationen abgeschlossen sind.</span><span class="sxs-lookup"><span data-stu-id="950f7-150">You should run the application multiple times during the installation to ensure all associated registration and dialog box configurations have been completed.</span></span> <span data-ttu-id="950f7-151">Wenn Sie die Anwendung während der Installation mehrmals öffnen, wird sichergestellt, dass nur die relevanten Anwendungsfeatures in den **primären Feature-Block**geladen werden.</span><span class="sxs-lookup"><span data-stu-id="950f7-151">Opening the application multiple times during installation will ensure that only the relevant application features are loaded into the **primary feature block**.</span></span>

-   **<span data-ttu-id="950f7-152">Deaktivieren Sie alle automatischen Update Features, die der Anwendung zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="950f7-152">Disable all automatic update features associated with the application.</span></span>**

    <span data-ttu-id="950f7-153">Einige Anwendungen können während der Installation automatisch auf die neuesten Updates überprüfen.</span><span class="sxs-lookup"><span data-stu-id="950f7-153">Some applications have the ability to check for the latest updates automatically during installation.</span></span> <span data-ttu-id="950f7-154">Wenn Sie die Versionsverwaltung virtueller Anwendungspakete unterstützen möchten, sollten Sie diese Funktion während der Sequenzierung deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="950f7-154">To assist with versioning of virtual application packages, you should disable this feature during sequencing.</span></span> <span data-ttu-id="950f7-155">Wenn Updates erforderlich sind, sollten Sie ein neues virtuelles Anwendungspaket mit den zugehörigen Updates sequenzieren.</span><span class="sxs-lookup"><span data-stu-id="950f7-155">If there are required updates, you should sequence a new virtual application package with the associated updates installed.</span></span>

## <span data-ttu-id="950f7-156">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="950f7-156">Related topics</span></span>


[<span data-ttu-id="950f7-157">Planen der Bereitstellung von Application Virtualization System</span><span class="sxs-lookup"><span data-stu-id="950f7-157">Planning for Application Virtualization System Deployment</span></span>](planning-for-application-virtualization-system-deployment.md)

 

 





