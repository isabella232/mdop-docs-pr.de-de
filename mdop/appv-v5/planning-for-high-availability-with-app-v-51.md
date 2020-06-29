---
title: Planen hoher Verfügbarkeit mit App-V 5.1
description: Planen hoher Verfügbarkeit mit App-V 5.1
author: dansimp
ms.assetid: 1f190a0e-10ee-4fbe-a602-7e807e943033
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 5c8e0e684051859a4caa2c4ef983c040295bc6d4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805009"
---
# <span data-ttu-id="4c55a-103">Planen hoher Verfügbarkeit mit App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="4c55a-103">Planning for High Availability with App-V 5.1</span></span>


<span data-ttu-id="4c55a-104">Microsoft Application Virtualization (App-V) 5,1-Systemkonfigurationen können die Vorteile von Optionen nutzen, die einen hohen verfügbaren Service gewährleisten.</span><span class="sxs-lookup"><span data-stu-id="4c55a-104">Microsoft Application Virtualization (App-V) 5.1 system configurations can take advantage of options that maintain a high level of available service.</span></span>

<span data-ttu-id="4c55a-105">Verwenden Sie die Informationen in den folgenden Abschnitten, damit Sie die Optionen für die Bereitstellung von App-V 5,1 in einer hoch verfügbaren Konfiguration verstehen können.</span><span class="sxs-lookup"><span data-stu-id="4c55a-105">Use the information in the following sections to help you understand the options to deploy App-V 5.1 in a highly available configuration.</span></span>

-   [<span data-ttu-id="4c55a-106">Unterstützung für Microsoft SQL Server-Clustering</span><span class="sxs-lookup"><span data-stu-id="4c55a-106">Support for Microsoft SQL Server clustering</span></span>](#bkmk-sqlcluster)

-   [<span data-ttu-id="4c55a-107">Unterstützung für den IIS-Netzwerklastenausgleich</span><span class="sxs-lookup"><span data-stu-id="4c55a-107">Support for IIS Network Load Balancing</span></span>](#bkmk-iisloadbal)

-   [<span data-ttu-id="4c55a-108">Unterstützung von Cluster-Dateiservern beim Ausführen von (SCS)-Modus</span><span class="sxs-lookup"><span data-stu-id="4c55a-108">Support for clustered file servers when running (SCS) mode</span></span>](#bkmk-clusterscsmode)

-   [<span data-ttu-id="4c55a-109">Unterstützung für die Microsoft SQL Server-Spiegelung</span><span class="sxs-lookup"><span data-stu-id="4c55a-109">Support for Microsoft SQL Server Mirroring</span></span>](#bkmk-sqlmirroring)

-   [<span data-ttu-id="4c55a-110">Unterstützung für Microsoft SQL Server immer aktiviert</span><span class="sxs-lookup"><span data-stu-id="4c55a-110">Support for Microsoft SQL Server Always On</span></span>](#bkmk-sqlalwayson)

## <a href="" id="bkmk-sqlcluster"></a><span data-ttu-id="4c55a-111">Unterstützung für Microsoft SQL Server-Clustering</span><span class="sxs-lookup"><span data-stu-id="4c55a-111">Support for Microsoft SQL Server clustering</span></span>


<span data-ttu-id="4c55a-112">Sie können die App-V-Verwaltungsdatenbank und die Berichtsdatenbank auf Computern ausführen, auf denen Microsoft SQL Server-Cluster ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="4c55a-112">You can run the App-V Management database and Reporting database on computers that are running Microsoft SQL Server clusters.</span></span> <span data-ttu-id="4c55a-113">Sie müssen die Datenbanken jedoch mithilfe von Skripts installieren.</span><span class="sxs-lookup"><span data-stu-id="4c55a-113">However, you must install the databases using scripts.</span></span>

<span data-ttu-id="4c55a-114">Anweisungen hierzu finden Sie unter [Bereitstellen der App-V-Datenbanken mithilfe von SQL-Skripts](how-to-deploy-the-app-v-databases-by-using-sql-scripts51.md).</span><span class="sxs-lookup"><span data-stu-id="4c55a-114">For instructions, see [How to Deploy the App-V Databases by Using SQL Scripts](how-to-deploy-the-app-v-databases-by-using-sql-scripts51.md).</span></span>

## <a href="" id="bkmk-iisloadbal"></a><span data-ttu-id="4c55a-115">Unterstützung für den IIS-Netzwerklastenausgleich</span><span class="sxs-lookup"><span data-stu-id="4c55a-115">Support for IIS Network Load Balancing</span></span>


<span data-ttu-id="4c55a-116">Sie können den Internet Informationsdienste (IIS)-Netzwerklastenausgleich verwenden, um eine hoch verfügbare Umgebung für Computer zu konfigurieren, auf denen die App-V 5. x-Verwaltungs-, Veröffentlichungs-und Reporting Services ausgeführt werden, die über IIS bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="4c55a-116">You can use Internet Information Services (IIS) Network Load Balancing to configure a highly available environment for computers running the App-V 5.x Management, Publishing, and Reporting services which are deployed through IIS.</span></span>

<span data-ttu-id="4c55a-117">Weitere Informationen zum Konfigurieren von IIS und Netzwerklastenausgleich für Computer mit Windows Server-Betriebssystemen finden Sie im folgenden:</span><span class="sxs-lookup"><span data-stu-id="4c55a-117">Review the following for more information about configuring IIS and Network Load Balancing for computers running Windows Server operating systems:</span></span>

-   <span data-ttu-id="4c55a-118">Enthält Informationen zum Konfigurieren von Internet Informationsdienste (IIS) 7,0.</span><span class="sxs-lookup"><span data-stu-id="4c55a-118">Provides information about configuring Internet Information Services (IIS) 7.0.</span></span>

    <span data-ttu-id="4c55a-119">[Erreichen von hoher Verfügbarkeit und Skalierbarkeit – arr und NLB](https://go.microsoft.com/fwlink/?LinkId=316369) (https://go.microsoft.com/fwlink/?LinkId=316369)</span><span class="sxs-lookup"><span data-stu-id="4c55a-119">[Achieving High Availability and Scalability - ARR and NLB](https://go.microsoft.com/fwlink/?LinkId=316369) (https://go.microsoft.com/fwlink/?LinkId=316369)</span></span>

-   <span data-ttu-id="4c55a-120">Konfigurieren von Microsoft Windows Server</span><span class="sxs-lookup"><span data-stu-id="4c55a-120">Configuring Microsoft Windows Server</span></span>

    <span data-ttu-id="4c55a-121">[Netzwerklastenausgleich](https://go.microsoft.com/fwlink/?LinkId=316370) ( https://go.microsoft.com/fwlink/?LinkId=316370) .</span><span class="sxs-lookup"><span data-stu-id="4c55a-121">[Network Load Balancing](https://go.microsoft.com/fwlink/?LinkId=316370) (https://go.microsoft.com/fwlink/?LinkId=316370).</span></span>

    <span data-ttu-id="4c55a-122">Diese Informationen gelten auch für IIS-Netzwerklastenausgleichs-Cluster in Windows Server2008, Windows Server2008R2 oder Windows Server2012.</span><span class="sxs-lookup"><span data-stu-id="4c55a-122">This information also applies to IIS Network Load Balancing (NLB) clusters in Windows Server2008, Windows Server2008R2, or Windows Server2012.</span></span>

    <span data-ttu-id="4c55a-123">**Hinweis**  Die IIS-Netzwerklastenausgleich-Funktion in Windows Server2012 ist in der Regel identisch mit der in Windows Server2008R2.</span><span class="sxs-lookup"><span data-stu-id="4c55a-123">**Note** The IIS Network Load Balancing functionality in Windows Server2012 is generally the same as in Windows Server2008R2.</span></span> <span data-ttu-id="4c55a-124">Einige Aufgabendetails werden jedoch in Windows Server2012 geändert.</span><span class="sxs-lookup"><span data-stu-id="4c55a-124">However, some task details are changed in Windows Server2012.</span></span> <span data-ttu-id="4c55a-125">Informationen zu neuen Methoden für Aufgaben finden Sie unter [allgemeine Verwaltungsaufgaben und Navigation in Windows Server 2012 R2 Preview und Windows Server 2012](https://go.microsoft.com/fwlink/?LinkId=316371) ( https://go.microsoft.com/fwlink/?LinkId=316371) .</span><span class="sxs-lookup"><span data-stu-id="4c55a-125">For information on new ways to do tasks, see [Common Management Tasks and Navigation in Windows Server 2012 R2 Preview and Windows Server 2012](https://go.microsoft.com/fwlink/?LinkId=316371) (https://go.microsoft.com/fwlink/?LinkId=316371).</span></span>

     

## <a href="" id="bkmk-clusterscsmode"></a><span data-ttu-id="4c55a-126">Unterstützung von Cluster-Dateiservern beim Ausführen von (SCS)-Modus</span><span class="sxs-lookup"><span data-stu-id="4c55a-126">Support for clustered file servers when running (SCS) mode</span></span>


<span data-ttu-id="4c55a-127">Das Ausführen von App-V 5,1 im Share Content Store (SCS)-Modus mit gruppierten Dateiservern wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4c55a-127">Running App-V 5.1 in Share Content Store (SCS) mode with clustered file servers is supported.</span></span>

<span data-ttu-id="4c55a-128">Die folgenden Schritte können verwendet werden, um diese Konfiguration zu aktivieren:</span><span class="sxs-lookup"><span data-stu-id="4c55a-128">The following steps can be used to enable this configuration:</span></span>

-   <span data-ttu-id="4c55a-129">Konfigurieren Sie App-V 5,1, um im Client-SCS-Modus ausgeführt zu werden.</span><span class="sxs-lookup"><span data-stu-id="4c55a-129">Configure App-V 5.1 to run in client SCS mode.</span></span> <span data-ttu-id="4c55a-130">Weitere Informationen zum Konfigurieren des App-v 5,1 SCS-Modus finden Sie unter so wird es [gemacht: Installieren des App-v 5,1-Clients für den freigegebenen Inhaltsspeicher Modus](how-to-install-the-app-v-51-client-for-shared-content-store-mode.md).</span><span class="sxs-lookup"><span data-stu-id="4c55a-130">For more information about configuring App-V 5.1 SCS mode, see [How to Install the App-V 5.1 Client for Shared Content Store Mode](how-to-install-the-app-v-51-client-for-shared-content-store-mode.md).</span></span>

-   <span data-ttu-id="4c55a-131">Konfigurieren Sie den im Microsoft Server2012-Skalierungsmodus und im Pre **2012** -Modus konfigurierten Dateiservercluster mit einem virtuellen San.</span><span class="sxs-lookup"><span data-stu-id="4c55a-131">Configure the file server cluster configured in both the Microsoft Server2012 scale out mode and pre **2012** mode with a virtual SAN.</span></span>

<span data-ttu-id="4c55a-132">Die folgenden Schritte können verwendet werden, um die Konfiguration zu überprüfen:</span><span class="sxs-lookup"><span data-stu-id="4c55a-132">The following steps can be used to validate the configuration:</span></span>

1.  <span data-ttu-id="4c55a-133">Fügen Sie ein Paket auf dem Veröffentlichungsserver hinzu.</span><span class="sxs-lookup"><span data-stu-id="4c55a-133">Add a package on the publishing server.</span></span> <span data-ttu-id="4c55a-134">Weitere Informationen zum Hinzufügen eines Pakets finden Sie unter so wird es [gemacht: Hinzufügen oder Aktualisieren von Paketen mithilfe der Verwaltungskonsole](how-to-add-or-upgrade-packages-by-using-the-management-console-51-gb18030.md).</span><span class="sxs-lookup"><span data-stu-id="4c55a-134">For more information about adding a package, see [How to Add or Upgrade Packages by Using the Management Console](how-to-add-or-upgrade-packages-by-using-the-management-console-51-gb18030.md).</span></span>

2.  <span data-ttu-id="4c55a-135">Führen Sie eine Veröffentlichungsaktualisierung auf dem Computer durch, auf dem der App-V 5,1-Client ausgeführt wird, und öffnen Sie eine Anwendung.</span><span class="sxs-lookup"><span data-stu-id="4c55a-135">Perform a publishing refresh on the computer running the App-V 5.1 client and open an application.</span></span>

3.  <span data-ttu-id="4c55a-136">Wechseln Sie die Clusterknoten in der Mitte des Veröffentlichungs Aktualisierungs-und Mid-Streaming, um sicherzustellen, dass ein Failover ordnungsgemäß funktioniert.</span><span class="sxs-lookup"><span data-stu-id="4c55a-136">Switch cluster nodes mid-publishing refresh and mid-streaming to ensure fail-over works correctly.</span></span>

<span data-ttu-id="4c55a-137">Weitere Informationen zum Konfigurieren von Windows Server-Failoverclustern finden Sie im folgenden:</span><span class="sxs-lookup"><span data-stu-id="4c55a-137">Review the following for more information about configuring Windows Server Failover clusters:</span></span>

-   <span data-ttu-id="4c55a-138">[Prüfliste: Erstellen eines gruppierten Dateiservers](https://go.microsoft.com/fwlink/?LinkId=316372) ( https://go.microsoft.com/fwlink/?LinkId=316372) .</span><span class="sxs-lookup"><span data-stu-id="4c55a-138">[Checklist: Create a Clustered File Server](https://go.microsoft.com/fwlink/?LinkId=316372) (https://go.microsoft.com/fwlink/?LinkId=316372).</span></span>

-   <span data-ttu-id="4c55a-139">[Verwenden freigegebener Clustervolumes in einem Windows Server 2012-Failovercluster](https://go.microsoft.com/fwlink/?LinkId=316373) ( https://go.microsoft.com/fwlink/?LinkId=316373) .</span><span class="sxs-lookup"><span data-stu-id="4c55a-139">[Use Cluster Shared Volumes in a Windows Server 2012 Failover Cluster](https://go.microsoft.com/fwlink/?LinkId=316373) (https://go.microsoft.com/fwlink/?LinkId=316373).</span></span>

## <a href="" id="bkmk-sqlmirroring"></a><span data-ttu-id="4c55a-140">Unterstützung für die Microsoft SQL Server-Spiegelung</span><span class="sxs-lookup"><span data-stu-id="4c55a-140">Support for Microsoft SQL Server Mirroring</span></span>


<span data-ttu-id="4c55a-141">Bei Verwendung der Microsoft SQL Server-Spiegelung, bei der die APP-v 5,1-Verwaltungsserver Datenbank mithilfe von zwei SQL Server-Instanzen gespiegelt wird, wird für App-v 5,1-Verwaltungsserver Datenbanken unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4c55a-141">Using Microsoft SQL Server mirroring, where the App-V 5.1 management server database is mirrored utilizing two SQL Server instances, for App-V 5.1 management server databases is supported.</span></span>

<span data-ttu-id="4c55a-142">Weitere Informationen zum Konfigurieren der Microsoft SQL Server-Spiegelung finden Sie im folgenden:</span><span class="sxs-lookup"><span data-stu-id="4c55a-142">Review the following for more information about configuring Microsoft SQL Server Mirroring:</span></span>

-   <span data-ttu-id="4c55a-143">[Vorgehensweise: Vorbereiten einer Spiegeldatenbank für die Spiegelung (Transact-SQL)](https://go.microsoft.com/fwlink/?LinkId=316375) (https://go.microsoft.com/fwlink/?LinkId=316375)</span><span class="sxs-lookup"><span data-stu-id="4c55a-143">[How to: Prepare a Mirror Database for Mirroring (Transact-SQL)](https://go.microsoft.com/fwlink/?LinkId=316375) (https://go.microsoft.com/fwlink/?LinkId=316375)</span></span>

-   <span data-ttu-id="4c55a-144">[Einrichten einer Datenbankspiegelungssitzung mithilfe der Windows-Authentifizierung (SQL Server Management Studio)](https://go.microsoft.com/fwlink/?LinkId=316377) (https://go.microsoft.com/fwlink/?LinkId=316377)</span><span class="sxs-lookup"><span data-stu-id="4c55a-144">[Establish a Database Mirroring Session Using Windows Authentication (SQL Server Management Studio)](https://go.microsoft.com/fwlink/?LinkId=316377) (https://go.microsoft.com/fwlink/?LinkId=316377)</span></span>

<span data-ttu-id="4c55a-145">Die folgenden Schritte können verwendet werden, um die Konfiguration zu überprüfen:</span><span class="sxs-lookup"><span data-stu-id="4c55a-145">The following steps can be used to validate the configuration:</span></span>

1.  <span data-ttu-id="4c55a-146">Initiieren Sie eine Microsoft SQL Server-Spiegelungssitzung.</span><span class="sxs-lookup"><span data-stu-id="4c55a-146">Initiate a Microsoft SQL Server Mirroring session.</span></span>

2.  <span data-ttu-id="4c55a-147">Wählen Sie **Failover** aus, um eine neue Master-Microsoft SQL Server-Instanz festzulegen.</span><span class="sxs-lookup"><span data-stu-id="4c55a-147">Select **Failover** to designate a new master Microsoft SQL Server instance.</span></span>

3.  <span data-ttu-id="4c55a-148">Überprüfen Sie, ob der App-V 5,1-Verwaltungsserver nach dem Failover weiterhin wie erwartet funktioniert.</span><span class="sxs-lookup"><span data-stu-id="4c55a-148">Verify that the App-V 5.1 management server continues to function as expected after the failover.</span></span>

<span data-ttu-id="4c55a-149">Die Verbindungszeichenfolge auf dem Verwaltungsserver kann geändert werden, um **Failover-Partner &lt; = &gt; Server2**einzubeziehen.</span><span class="sxs-lookup"><span data-stu-id="4c55a-149">The connection string on the management server can be modified to include **failover partner = &lt;server2&gt;**.</span></span> <span data-ttu-id="4c55a-150">Dies hilft nur, wenn das primäre auf der Spiegelung auf das sekundäre Failover und der Computer, auf dem der App-V 5,1-Client ausgeführt wird, eine neue Verbindung ausführt (sagen wir nach einem Neustart).</span><span class="sxs-lookup"><span data-stu-id="4c55a-150">This will only help when the primary on the mirror has failed over to the secondary and the computer running the App-V 5.1 client is doing a fresh connection (say after reboot).</span></span>

<span data-ttu-id="4c55a-151">Führen Sie die folgenden Schritte aus, um die Verbindungszeichenfolge so zu ändern, dass Sie **Failover-Partner = &lt; &gt; Server2**umfasst:</span><span class="sxs-lookup"><span data-stu-id="4c55a-151">Use the following steps to modify the connection string to include **failover partner = &lt;server2&gt;**:</span></span>

<span data-ttu-id="4c55a-152">**Wichtig**  In diesem Thema wird beschrieben, wie Sie die Windows-Registrierung mit dem Registrierungs-Editor ändern.</span><span class="sxs-lookup"><span data-stu-id="4c55a-152">**Important** This topic describes how to change the Windows registry by using Registry Editor.</span></span> <span data-ttu-id="4c55a-153">Wenn Sie die Windows-Registrierung falsch ändern, können Sie zu schwerwiegenden Problemen führen, bei denen Sie möglicherweise eine Neuinstallation von Windows erforderlich machen.</span><span class="sxs-lookup"><span data-stu-id="4c55a-153">If you change the Windows registry incorrectly, you can cause serious problems that might require you to reinstall Windows.</span></span> <span data-ttu-id="4c55a-154">Bevor Sie die Registrierung ändern, sollten Sie eine Sicherungskopie der Registrierungsdateien (System. dat und User. dat) erstellen.</span><span class="sxs-lookup"><span data-stu-id="4c55a-154">You should make a backup copy of the registry files (System.dat and User.dat) before you change the registry.</span></span> <span data-ttu-id="4c55a-155">Microsoft kann nicht garantieren, dass die Probleme, die beim Ändern der Registrierung auftreten, behoben werden können.</span><span class="sxs-lookup"><span data-stu-id="4c55a-155">Microsoft cannot guarantee that the problems that might occur when you change the registry can be resolved.</span></span> <span data-ttu-id="4c55a-156">Ändern Sie die Registrierung auf Ihr eigenes Risiko.</span><span class="sxs-lookup"><span data-stu-id="4c55a-156">Change the registry at your own risk.</span></span>

 

1.  <span data-ttu-id="4c55a-157">Melden Sie sich beim Verwaltungsserver an, und öffnen Sie **Regedit**.</span><span class="sxs-lookup"><span data-stu-id="4c55a-157">Login to the management server and open **regedit**.</span></span>

2.  <span data-ttu-id="4c55a-158">Navigieren Sie zu **HKEY \ _LOCAL \ _MACHINE**  \\  **Software**  \\  **Microsoft**  \\  **AppV**  \\  **Server**  \\  **Managementservice**.</span><span class="sxs-lookup"><span data-stu-id="4c55a-158">Navigate to **HKEY\_LOCAL\_MACHINE** \\ **Software** \\ **Microsoft** \\ **AppV** \\ **Server** \\ **ManagementService**.</span></span>

3.  <span data-ttu-id="4c55a-159">Ändern Sie die **Verwaltung \ _SQL \ _CONNECTION \ _STRING** Wert mit dem \*\*Failover-Partner = &lt; Server2 &gt; \*\*.</span><span class="sxs-lookup"><span data-stu-id="4c55a-159">Modify the **MANAGEMENT\_SQL\_CONNECTION\_STRING** value with the **failover partner = &lt;server2&gt;**.</span></span>

4.  <span data-ttu-id="4c55a-160">Starten Sie den Verwaltungsdienst mithilfe der IIS-Konsole erneut.</span><span class="sxs-lookup"><span data-stu-id="4c55a-160">Restart management service using the IIS console.</span></span>

    <span data-ttu-id="4c55a-161">**Hinweis**  Die Datenbankspiegelung befindet sich in der Liste der veralteten Datenbankmodul Features für Microsoft SQL Server2012 aufgrund der in Microsoft SQL Server 2012 verfügbaren **AlwaysOn** -Funktion.</span><span class="sxs-lookup"><span data-stu-id="4c55a-161">**Note** Database Mirroring is on the list of Deprecated Database Engine Features for Microsoft SQL Server2012 due to the **AlwaysOn** feature available with Microsoft SQL Server 2012.</span></span>

     

<span data-ttu-id="4c55a-162">Klicken Sie auf einen der folgenden Links, um weitere Informationen zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="4c55a-162">Click any of the following links for more information:</span></span>

-   <span data-ttu-id="4c55a-163">[Vorgehensweise: Vorbereiten einer Spiegeldatenbank für die Spiegelung (Transact-SQL)](https://go.microsoft.com/fwlink/?LinkId=394235) ( https://go.microsoft.com/fwlink/?LinkId=394235) .</span><span class="sxs-lookup"><span data-stu-id="4c55a-163">[How to: Prepare a Mirror Database for Mirroring (Transact-SQL)](https://go.microsoft.com/fwlink/?LinkId=394235) (https://go.microsoft.com/fwlink/?LinkId=394235).</span></span>

-   <span data-ttu-id="4c55a-164">[Vorgehensweise: Konfigurieren einer Datenbankspiegelungssitzung (SQL Server Management Studio)](https://go.microsoft.com/fwlink/?LinkId=394236) ( https://go.microsoft.com/fwlink/?LinkId=394236) .</span><span class="sxs-lookup"><span data-stu-id="4c55a-164">[How to: Configure a Database Mirroring Session (SQL Server Management Studio)](https://go.microsoft.com/fwlink/?LinkId=394236) (https://go.microsoft.com/fwlink/?LinkId=394236).</span></span>

-   <span data-ttu-id="4c55a-165">[Einrichten einer Datenbankspiegelungssitzung mithilfe der Windows-Authentifizierung (SQL Server Management Studio)](https://go.microsoft.com/fwlink/?LinkId=394237) ( https://go.microsoft.com/fwlink/?LinkId=394237) .</span><span class="sxs-lookup"><span data-stu-id="4c55a-165">[Establish a Database Mirroring Session Using Windows Authentication (SQL Server Management Studio)](https://go.microsoft.com/fwlink/?LinkId=394237) (https://go.microsoft.com/fwlink/?LinkId=394237).</span></span>

-   <span data-ttu-id="4c55a-166">[Veraltete Datenbankmodul Features in SQL Server 2012](https://go.microsoft.com/fwlink/?LinkId=394238) ( https://go.microsoft.com/fwlink/?LinkId=394238) .</span><span class="sxs-lookup"><span data-stu-id="4c55a-166">[Deprecated Database Engine Features in SQL Server 2012](https://go.microsoft.com/fwlink/?LinkId=394238) (https://go.microsoft.com/fwlink/?LinkId=394238).</span></span>

## <a href="" id="bkmk-sqlalwayson"></a><span data-ttu-id="4c55a-167">Unterstützung für Microsoft SQL Server immer für die Konfiguration</span><span class="sxs-lookup"><span data-stu-id="4c55a-167">Support for Microsoft SQL Server Always On configuration</span></span>


<span data-ttu-id="4c55a-168">Die App-V 5,1-Verwaltungsserver-Datenbank unterstützt Bereitstellungen auf Computern, auf denen Microsoft SQL Server ausgeführt wird, mit der **Always on** -Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="4c55a-168">The App-V 5.1 management server database supports deployments to computers running Microsoft SQL Server with the **Always On** configuration.</span></span>






## <span data-ttu-id="4c55a-169">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="4c55a-169">Related topics</span></span>


[<span data-ttu-id="4c55a-170">Planen der Bereitstellung von App-V</span><span class="sxs-lookup"><span data-stu-id="4c55a-170">Planning to Deploy App-V</span></span>](planning-to-deploy-app-v51.md)

 

 





