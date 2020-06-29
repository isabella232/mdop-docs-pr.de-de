---
title: So konfigurieren Sie einen schreibgeschützten Cache für App-V Client (RDS)
description: So konfigurieren Sie einen schreibgeschützten Cache für App-V Client (RDS)
author: dansimp
ms.assetid: b6607fe2-6f92-4567-99f1-d8e3c8a591e0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: a44844ae9ffc3497151be7713f6a43fda0ccd8fa
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807311"
---
# <span data-ttu-id="7c4a0-103">So konfigurieren Sie einen schreibgeschützten Cache für App-V Client (RDS)</span><span class="sxs-lookup"><span data-stu-id="7c4a0-103">How to Configure a Read-only Cache on the App-V Client (RDS)</span></span>


<span data-ttu-id="7c4a0-104">**Wichtig**  Sie müssen App-V 4,6, SP1 ausführen, um dieses Verfahren verwenden zu können.</span><span class="sxs-lookup"><span data-stu-id="7c4a0-104">**Important** You must be running App-V 4.6, SP1 to use this procedure.</span></span>

 

<span data-ttu-id="7c4a0-105">Sie können den App-V-Client mithilfe eines freigegebenen Caches bereitstellen, der mit allen Anwendungen aufgefüllt ist, die für alle Benutzer erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="7c4a0-105">You can deploy the App-V client by using a shared cache that is populated with all the applications required for all users.</span></span> <span data-ttu-id="7c4a0-106">Anschließend konfigurieren Sie die App-V-Remote Desktop Dienste (RDS)-Clients so, dass Sie dieselbe Cachedatei verwenden.</span><span class="sxs-lookup"><span data-stu-id="7c4a0-106">Then you configure the App-V Remote Desktop Services (RDS) Clients to use the same cache file.</span></span> <span data-ttu-id="7c4a0-107">Benutzern wird mithilfe des App-V-Veröffentlichungsprozesses der Zugriff auf bestimmte Anwendungen gewährt.</span><span class="sxs-lookup"><span data-stu-id="7c4a0-107">Users are granted access to specific applications by using the App-V publishing process.</span></span> <span data-ttu-id="7c4a0-108">Da der Cache bereits mit allen Anwendungen vorinstalliert ist, erfolgt kein Streaming, wenn ein Benutzer eine Anwendung startet.</span><span class="sxs-lookup"><span data-stu-id="7c4a0-108">Because the cache is already preloaded with all applications, no streaming occurs when a user starts an application.</span></span> <span data-ttu-id="7c4a0-109">Die Pakete, die zum Vorfüllen des Caches verwendet werden, müssen jedoch auf einem App-v-Server abgelegt werden, der RTSP-Streaming (Real Time Streaming Protocol) unterstützt und den App-v-Clients Zugriffsberechtigungen gewährt.</span><span class="sxs-lookup"><span data-stu-id="7c4a0-109">However, the packages used to prepopulate the cache must be put on an App-V server that supports Real Time Streaming Protocol (RTSP) streaming and that grants access permissions to the App-V Clients.</span></span> <span data-ttu-id="7c4a0-110">Wenn Sie die Anwendungen mithilfe eines App-V-Verwaltungsservers veröffentlichen, können Sie diese Funktion zum Bereitstellen dieser Streamingfunktion verwenden.</span><span class="sxs-lookup"><span data-stu-id="7c4a0-110">If you publish the applications by using an App-V Management Server, you can use it to provide this streaming function.</span></span>

<span data-ttu-id="7c4a0-111">**Hinweis**  Die in diesen Verfahren beschriebenen Details sind nur als Beispiele vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="7c4a0-111">**Note** The details outlined in these procedures are intended as examples only.</span></span> <span data-ttu-id="7c4a0-112">Sie können verschiedene Methoden verwenden, um den gesamten Prozess abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="7c4a0-112">You might use different methods to complete the overall process.</span></span>

 

## <span data-ttu-id="7c4a0-113">Bereitstellen des App-V-Clients in einem RDS-Szenario</span><span class="sxs-lookup"><span data-stu-id="7c4a0-113">Deploying the App-V Client in an RDS Scenario</span></span>


<span data-ttu-id="7c4a0-114">Der Bereitstellungsprozess besteht aus vier Hauptaufgaben:</span><span class="sxs-lookup"><span data-stu-id="7c4a0-114">The deployment process consists of four primary tasks:</span></span>

-   <span data-ttu-id="7c4a0-115">Erstellen und Auffüllen der freigegebenen mastercachedatei</span><span class="sxs-lookup"><span data-stu-id="7c4a0-115">Creating and populating the master shared cache file</span></span>

-   <span data-ttu-id="7c4a0-116">Kopieren der freigegebenen Cachedatei in den Server Speicher</span><span class="sxs-lookup"><span data-stu-id="7c4a0-116">Copying the shared cache file to the server storage</span></span>

-   <span data-ttu-id="7c4a0-117">Konfigurieren der App-V-Client Software</span><span class="sxs-lookup"><span data-stu-id="7c4a0-117">Configuring the App-V client software</span></span>

-   <span data-ttu-id="7c4a0-118">Verwalten des Update Bereitstellungszyklus für die freigegebene Cachedatei nach der ersten Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="7c4a0-118">Managing the update deployment cycle for the shared cache file after the initial deployment</span></span>

<span data-ttu-id="7c4a0-119">Für diese Aufgaben ist eine sorgfältige Planung erforderlich.</span><span class="sxs-lookup"><span data-stu-id="7c4a0-119">These tasks require careful planning.</span></span> <span data-ttu-id="7c4a0-120">Wir empfehlen, dass Sie einen methodischen, reproduzierbaren Prozess vorbereiten und dokumentieren, dem Ihre Organisation folgen kann.</span><span class="sxs-lookup"><span data-stu-id="7c4a0-120">We recommend that you prepare and document a methodical, reproducible process for your organization to follow.</span></span> <span data-ttu-id="7c4a0-121">Dies ist besonders wichtig für die Vorbereitung und Bereitstellung der freigegebenen mastercachedatei sowie für die laufende Verwaltung von Anwendungsupdates, für die jeweils eine Aktualisierung des freigegebenen Master Caches erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="7c4a0-121">This is especially important for the preparation and deployment of the master shared cache file, and for the ongoing management of application updates, each of which require an update to the master shared cache.</span></span> <span data-ttu-id="7c4a0-122">Führen Sie die folgenden Verfahren aus, um diese primären Aufgaben auszuführen.</span><span class="sxs-lookup"><span data-stu-id="7c4a0-122">Use the following procedures to complete these primary tasks.</span></span>

<span data-ttu-id="7c4a0-123">**Hinweis**  Obwohl Sie die Anwendungen mithilfe verschiedener Methoden veröffentlichen können, basieren die folgenden Verfahren auf der Verwendung eines App-V-Verwaltungsservers für die Veröffentlichung.</span><span class="sxs-lookup"><span data-stu-id="7c4a0-123">**Note** Although you can publish the applications by using several different methods, the following procedures are based on your using an App-V Management Server for publishing.</span></span>

 

**<span data-ttu-id="7c4a0-124">So konfigurieren Sie den schreibgeschützten Cache für die Erstbereitstellung</span><span class="sxs-lookup"><span data-stu-id="7c4a0-124">To configure the read-only cache for initial deployment</span></span>**

1. <span data-ttu-id="7c4a0-125">Einrichten und Konfigurieren eines App-V-Verwaltungsservers zum Bereitstellen von Benutzerauthentifizierung und Veröffentlichungs Unterstützung.</span><span class="sxs-lookup"><span data-stu-id="7c4a0-125">Set up and configure an App-V Management Server to provide user authentication and publishing support.</span></span>

2. <span data-ttu-id="7c4a0-126">Füllen Sie den Inhaltsordner dieses Verwaltungsservers mit allen Anwendungspaketen, die für alle Benutzer erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="7c4a0-126">Populate the Content folder of this Management Server with all the application packages required for all users.</span></span>

3. <span data-ttu-id="7c4a0-127">Richten Sie einen Bereitstellungscomputer ein, auf dem der App-V-Client installiert ist.</span><span class="sxs-lookup"><span data-stu-id="7c4a0-127">Set up a staging computer that has the App-V Client installed.</span></span> <span data-ttu-id="7c4a0-128">Melden Sie sich bei dem Stagingcomputer mit einem Konto an, das Zugriff auf alle Anwendungen hat, damit der vollständige Satz der Anwendungen auf dem Computer veröffentlicht wird, und Streamen Sie die Anwendungen dann in den Zwischenspeicher, damit Sie vollständig geladen werden.</span><span class="sxs-lookup"><span data-stu-id="7c4a0-128">Log on to the staging computer by using an account that has access to all applications so that the complete set of applications are published to the computer, and then stream the applications to cache so that they are fully loaded.</span></span>

   **<span data-ttu-id="7c4a0-129">Wichtig</span><span class="sxs-lookup"><span data-stu-id="7c4a0-129">Important</span></span>**  
   <span data-ttu-id="7c4a0-130">Der Bereitstellungscomputer muss denselben Betriebssystemtyp und dieselbe Systemarchitektur wie die von den VMS verwenden, auf denen der App-V-Client ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7c4a0-130">The staging computer must use the same operating system type and system architecture as those used by the VMs on which the App-V Client will run.</span></span>

     

4. <span data-ttu-id="7c4a0-131">Starten Sie den Bereitstellungscomputer im abgesicherten Modus neu, um sicherzustellen, dass die Treiber nicht gestartet werden, da hierdurch die Cachedatei gesperrt wird.</span><span class="sxs-lookup"><span data-stu-id="7c4a0-131">Restart the staging computer in safe mode to make sure that the drivers are not started, because this would lock the cache file.</span></span>

   **<span data-ttu-id="7c4a0-132">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="7c4a0-132">Note</span></span>**  
   <span data-ttu-id="7c4a0-133">Alternativ können Sie den Application Virtualization Service beenden und deaktivieren und dann den Computer neu starten.</span><span class="sxs-lookup"><span data-stu-id="7c4a0-133">Or, you can stop and disable the Application Virtualization service, and then restart the computer.</span></span> <span data-ttu-id="7c4a0-134">Denken Sie nach dem Kopieren der Datei daran, den Dienst erneut zu aktivieren und zu starten.</span><span class="sxs-lookup"><span data-stu-id="7c4a0-134">After the file is copied, remember to enable and start the service again.</span></span>

     

5. <span data-ttu-id="7c4a0-135">Kopieren Sie die sftfs. FSD-Cachedatei in ein San, in dem alle RDS-Server darauf zugreifen können, beispielsweise in einem freigegebenen Ordner.</span><span class="sxs-lookup"><span data-stu-id="7c4a0-135">Copy the Sftfs.fsd cache file to a SAN where all the RDS servers can access it, such as in a shared folder.</span></span> <span data-ttu-id="7c4a0-136">Legen Sie die Berechtigungen für den Ordner Zugriff für die Gruppe Jeder und für Administratoren, die die Cachedatei Updates verwalten, auf schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="7c4a0-136">Set the folder access permissions to Read-only for the group Everyone and to Full Control for administrators who will manage the cache file updates.</span></span> <span data-ttu-id="7c4a0-137">Der Speicherort der Cachedatei kann über die Registrierungs-AppFS\\FileName. abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="7c4a0-137">The location of the cache file can be obtained from the registry AppFS\\FileName.</span></span>

   **<span data-ttu-id="7c4a0-138">Wichtig</span><span class="sxs-lookup"><span data-stu-id="7c4a0-138">Important</span></span>**  
   <span data-ttu-id="7c4a0-139">Sie müssen die FSD-Datei an einem Speicherort ablegen, auf dem die Reaktionsfähigkeit und Zuverlässigkeit der lokal angeschlossenen Speicherleistung entspricht, beispielsweise einem San.</span><span class="sxs-lookup"><span data-stu-id="7c4a0-139">You must put the FSD file in a location that has the responsiveness and reliability equal to locally attached storage performance, for example, a SAN.</span></span>

     

6. <span data-ttu-id="7c4a0-140">Installieren Sie den App-V RDS-Client auf jedem RDS-Server, und konfigurieren Sie ihn für die Verwendung des schreibgeschützten Caches, indem Sie dem AppFS-Schlüssel auf dem Client die folgenden Registrierungsschlüsselwerte hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="7c4a0-140">Install the App-V RDS Client on each RDS server, and then configure it to use the read-only cache by adding the following registry key values to the AppFS key on the client.</span></span> <span data-ttu-id="7c4a0-141">Der AppFS-Schlüssel befindet sich unter HKEY \ _LOCAL \ _MACHINE \\software\\\] Microsoft\\SoftGrid\\4.5\\Client\\AppFS für 32-Bit-Computer und bei HKEY \ _LOCAL \ _MACHINE \\software\\wow6432node\\microsoft\\softgrid\\4.5\\client\\appfs für 64-Bit-Computer.</span><span class="sxs-lookup"><span data-stu-id="7c4a0-141">The AppFS key is located at HKEY\_LOCAL\_MACHINE\\SOFTWARE\\\]Microsoft\\SoftGrid\\4.5\\Client\\AppFS for 32-bit computers and at HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\Client\\AppFS for 64-bit computers.</span></span>

   <table>
   <colgroup>
   <col width="25%" />
   <col width="25%" />
   <col width="25%" />
   <col width="25%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="7c4a0-142">Key</span><span class="sxs-lookup"><span data-stu-id="7c4a0-142">Key</span></span></th>
   <th align="left"><span data-ttu-id="7c4a0-143">Typ</span><span class="sxs-lookup"><span data-stu-id="7c4a0-143">Type</span></span></th>
   <th align="left"><span data-ttu-id="7c4a0-144">Wert</span><span class="sxs-lookup"><span data-stu-id="7c4a0-144">Value</span></span></th>
   <th align="left"><span data-ttu-id="7c4a0-145">Zweck</span><span class="sxs-lookup"><span data-stu-id="7c4a0-145">Purpose</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="7c4a0-146">FileName</span><span class="sxs-lookup"><span data-stu-id="7c4a0-146">FileName</span></span></p></td>
   <td align="left"><p><span data-ttu-id="7c4a0-147">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="7c4a0-147">String</span></span></p></td>
   <td align="left"><p><span data-ttu-id="7c4a0-148">Pfad von FSD</span><span class="sxs-lookup"><span data-stu-id="7c4a0-148">path of FSD</span></span></p></td>
   <td align="left"><p><span data-ttu-id="7c4a0-149">Gibt den Pfad der freigegebenen Cachedatei an, beispielsweise \RDSServername\Sharefolder\SFTFS. FSD (erforderlich).</span><span class="sxs-lookup"><span data-stu-id="7c4a0-149">Specifies the path of the shared cache file, for example, \RDSServername\Sharefolder\SFTFS.FSD (Required).</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="7c4a0-150">ReadOnlyFSD</span><span class="sxs-lookup"><span data-stu-id="7c4a0-150">ReadOnlyFSD</span></span></p></td>
   <td align="left"><p><span data-ttu-id="7c4a0-151">DWORD</span><span class="sxs-lookup"><span data-stu-id="7c4a0-151">DWORD</span></span></p></td>
   <td align="left"><p><span data-ttu-id="7c4a0-152">1</span><span class="sxs-lookup"><span data-stu-id="7c4a0-152">1</span></span></p></td>
   <td align="left"><p><span data-ttu-id="7c4a0-153">Konfiguriert den Client so, dass er im schreibgeschützten Modus ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7c4a0-153">Configures the client to operate in Read-Only mode.</span></span> <span data-ttu-id="7c4a0-154">Dadurch wird sichergestellt, dass der Client nicht versucht, Aktualisierungen an den Paketcache zu streamen.</span><span class="sxs-lookup"><span data-stu-id="7c4a0-154">This ensures that the client will not try to stream updates to the package cache.</span></span> <span data-ttu-id="7c4a0-155">(Erforderlich)</span><span class="sxs-lookup"><span data-stu-id="7c4a0-155">(Required)</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="7c4a0-156">ErrorLogLocation</span><span class="sxs-lookup"><span data-stu-id="7c4a0-156">ErrorLogLocation</span></span></p></td>
   <td align="left"><p><span data-ttu-id="7c4a0-157">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="7c4a0-157">String</span></span></p></td>
   <td align="left"><p><span data-ttu-id="7c4a0-158">Pfad der Fehlerprotokolldatei (ETL)</span><span class="sxs-lookup"><span data-stu-id="7c4a0-158">path of error log (.etl) file</span></span></p></td>
   <td align="left"><p><span data-ttu-id="7c4a0-159">Eintrag, der zum Angeben des Pfads des Fehlerprotokolls verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7c4a0-159">Entry used to specify the path of the error log.</span></span> <span data-ttu-id="7c4a0-160">Empfohlen.</span><span class="sxs-lookup"><span data-stu-id="7c4a0-160">(Recommended.</span></span> <span data-ttu-id="7c4a0-161">Verwenden Sie einen lokalen Pfad wie C:\Logs\Sftfs.ETL).</span><span class="sxs-lookup"><span data-stu-id="7c4a0-161">Use a local path such as C:\Logs\Sftfs.etl).</span></span></p></td>
   </tr>
   </tbody>
   </table>

     

7. <span data-ttu-id="7c4a0-162">Konfigurieren Sie die einzelnen RDS-Server in der Farm so, dass Sie den Veröffentlichungsserver verwenden, und verwenden Sie die Veröffentlichungsaktualisierung, wenn sich Benutzer anmelden.</span><span class="sxs-lookup"><span data-stu-id="7c4a0-162">Configure each RDS server in the farm to use the publishing server and to use publishing update when users log on.</span></span> <span data-ttu-id="7c4a0-163">Wenn sich Benutzer bei den RDS-Servern anmelden, wird ein Veröffentlichungs Aktualisierungszyklus durchgeführt, und es werden alle Anwendungen veröffentlicht, für die Ihr Konto autorisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="7c4a0-163">As users log on to the RDS servers, a publishing update cycle occurs and publishes all the applications for which their account is authorized.</span></span> <span data-ttu-id="7c4a0-164">Diese Anwendungen werden im freigegebenen Cache ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7c4a0-164">These applications are run from the shared cache.</span></span>

**<span data-ttu-id="7c4a0-165">So konfigurieren Sie den RDS-Client für die Paketaktualisierung</span><span class="sxs-lookup"><span data-stu-id="7c4a0-165">To configure the RDS client for package upgrade</span></span>**

1.  <span data-ttu-id="7c4a0-166">Führen Sie das Upgrade und Testen des Anwendungspakets durch.</span><span class="sxs-lookup"><span data-stu-id="7c4a0-166">Complete the upgrade and testing of the application package.</span></span>

2.  <span data-ttu-id="7c4a0-167">Aktualisieren Sie das Paket auf dem App-V-Server.</span><span class="sxs-lookup"><span data-stu-id="7c4a0-167">Upgrade the package on the App-V server.</span></span> <span data-ttu-id="7c4a0-168">Veröffentlichen und Streamen Sie dann die neue Version der Anwendungen auf dem Bereitstellungscomputer auf dem Client, damit Sie vollständig in den Cache geladen werden.</span><span class="sxs-lookup"><span data-stu-id="7c4a0-168">Then, publish and stream the new version of the applications to the client on the staging computer so that they are fully loaded into cache.</span></span>

3.  <span data-ttu-id="7c4a0-169">Starten Sie den Bereitstellungscomputer im abgesicherten Modus neu, um sicherzustellen, dass die Treiber nicht gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="7c4a0-169">Restart the staging computer in safe mode to ensure the drivers are not started.</span></span>

    <span data-ttu-id="7c4a0-170">**Hinweis**  Oder Sie können den Application Virtualization Service zunächst beenden und dann im Services. msc deaktivieren und den Computer neu starten.</span><span class="sxs-lookup"><span data-stu-id="7c4a0-170">**Note** Or, you can first stop and then disable the Application Virtualization service in the Services.msc, and restart the computer.</span></span> <span data-ttu-id="7c4a0-171">Nachdem die Datei kopiert wurde, denken Sie daran, den Dienst erneut zu aktivieren und zu starten.</span><span class="sxs-lookup"><span data-stu-id="7c4a0-171">After the file has been copied, remember to enable and start the service again.</span></span>

     

4.  <span data-ttu-id="7c4a0-172">Kopieren Sie die sftfs. FSD-Cachedatei in ein San, in dem alle RDS-Server darauf zugreifen können, beispielsweise in einem freigegebenen Ordner.</span><span class="sxs-lookup"><span data-stu-id="7c4a0-172">Copy the Sftfs.fsd cache file to a SAN where all the RDS servers can access it, such as in a shared folder.</span></span> <span data-ttu-id="7c4a0-173">Sie können einen anderen Dateinamen verwenden, beispielsweise SFTFS \ _V2. FSD, um die neue Version zu unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="7c4a0-173">You can use a different file name, for example, SFTFS\_V2.FSD, to distinguish the new version.</span></span>

5.  <span data-ttu-id="7c4a0-174">Um den App-V RDS-Client auf jedem RDS-Server in der Farm so zu konfigurieren, dass die aktualisierte freigegebene Cachedatei verwendet wird, ändern Sie den FileName-Wert des AppFS-Registrierungsschlüssels so, dass er auf den Speicherort der aktualisierten Datei verweist, beispielsweise \\\\RDSServername\\Sharefolder\\SFTFS\ _V2. FSD.</span><span class="sxs-lookup"><span data-stu-id="7c4a0-174">To configure the App-V RDS Client on each RDS server in the farm to use the updated shared cache file, change the AppFS registry key FILENAME value to point to the location of the updated file, for example, \\\\RDSServername\\Sharefolder\\SFTFS\_V2.FSD.</span></span> <span data-ttu-id="7c4a0-175">Dadurch wird sichergestellt, dass jeder RDS-Server die aktualisierte Kopie des Caches erhält, wenn die APP-innerhalb seiner vClient-Treiber neu gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="7c4a0-175">This guarantees that each RDS server receives the updated copy of the cache when the App-Vclient drivers restart.</span></span>

    <span data-ttu-id="7c4a0-176">**Wichtig**  Sie müssen die RDS-Server neu starten, um die aktualisierte freigegebene Cachedatei verwenden zu können.</span><span class="sxs-lookup"><span data-stu-id="7c4a0-176">**Important** You must restart the RDS servers in order to use the updated shared cache file.</span></span>

     

## <span data-ttu-id="7c4a0-177">Verwenden symbolischer Links beim Aktualisieren des Caches</span><span class="sxs-lookup"><span data-stu-id="7c4a0-177">How to Use Symbolic Links when Upgrading the Cache</span></span>


<span data-ttu-id="7c4a0-178">Anstatt den AppFS-Schlüsseldatei Namen jedes Mal zu ändern, wenn eine neue Cachedatei bereitgestellt wird, die neue oder aktualisierte Pakete enthält, können Sie in den folgenden Betriebssystemen einen symbolischen Link verwenden: Windows Vista, Windows 7 und Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="7c4a0-178">Instead of changing the AppFS key FILENAME value every time that a new cache file is deployed that contains new or upgraded packages, you can use a symbolic link in the following operating systems: Windows Vista, Windows 7, and Windows Server 2008.</span></span> <span data-ttu-id="7c4a0-179">Weitere Informationen zu symbolischen Links finden Sie unter [symbolische Links](https://go.microsoft.com/fwlink/?LinkId=157626) ( https://go.microsoft.com/fwlink/?LinkId=157626) .</span><span class="sxs-lookup"><span data-stu-id="7c4a0-179">For more information about symbolic links, see [Symbolic Links](https://go.microsoft.com/fwlink/?LinkId=157626) (https://go.microsoft.com/fwlink/?LinkId=157626).</span></span> <span data-ttu-id="7c4a0-180">Im Gegensatz dazu unterstützt Windows XP nicht die Verwendung symbolischer Links, und Sie müssen stattdessen Abzweigungspunkte verwenden.</span><span class="sxs-lookup"><span data-stu-id="7c4a0-180">In contrast, Windows XP does not support the use of symbolic links, and you must use junction points instead.</span></span> <span data-ttu-id="7c4a0-181">Weitere Informationen zu Junctions finden Sie im [Artikel 205524](https://go.microsoft.com/fwlink/?LinkId=182553) in der Microsoft Knowledge Base ( https://go.microsoft.com/fwlink/?LinkId=182553) und auch in der Tool [Verzweigung v 1.05](https://go.microsoft.com/fwlink/?LinkId=182554) ( https://go.microsoft.com/fwlink/?LinkId=182554) .</span><span class="sxs-lookup"><span data-stu-id="7c4a0-181">For more information about junctions, see [article 205524](https://go.microsoft.com/fwlink/?LinkId=182553) in the Microsoft Knowledge Base (https://go.microsoft.com/fwlink/?LinkId=182553), and also the tool [Junction v1.05](https://go.microsoft.com/fwlink/?LinkId=182554) (https://go.microsoft.com/fwlink/?LinkId=182554).</span></span>

**<span data-ttu-id="7c4a0-182">So konfigurieren Sie einen symbolischen Link, um auf den Cache zu verweisen</span><span class="sxs-lookup"><span data-stu-id="7c4a0-182">To configure a symbolic link to reference the cache</span></span>**

1.  <span data-ttu-id="7c4a0-183">Öffnen Sie während der anfänglichen Bereitstellungsphase ein Eingabeaufforderungsfenster als lokaler Administrator auf dem RDS-Server-Betriebssystem.</span><span class="sxs-lookup"><span data-stu-id="7c4a0-183">During the initial deployment stage, open a Command Prompt window as a local administrator on the RDS server host operating system.</span></span>

2.  <span data-ttu-id="7c4a0-184">Erstellen Sie einen symbolischen Link mit dem Befehl mklink, und konfigurieren Sie ihn so, dass er auf die Datei sftfs. FSD verweist.</span><span class="sxs-lookup"><span data-stu-id="7c4a0-184">Create a symbolic link by using the MKLINK command, and then configure it to point to the Sftfs.fsd file.</span></span>

    **     <span data-ttu-id="7c4a0-185">mklink symlinkname \\\\rdshostserver\\sharefolder\\sftfs.FSD</span><span class="sxs-lookup"><span data-stu-id="7c4a0-185">mklink symlinkname \\\\rdshostserver\\sharefolder\\sftfs.fsd</span></span>**

3.  <span data-ttu-id="7c4a0-186">Öffnen Sie auf dem VDI-Master-VM-Bild ein Eingabeaufforderungsfenster, indem Sie die Option " **als Administrator ausführen** " verwenden und Remote Link Berechtigungen erteilen, damit der VM auf den symbolischen Link auf dem VDI-Host Betriebssystem zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="7c4a0-186">On the VDI Master VM Image, open a Command Prompt window by using the **Run as administrator** option and grant remote link permissions so that the VM can access the symbolic link on the VDI Host operating system.</span></span> <span data-ttu-id="7c4a0-187">Standardmäßig sind Remote Link-Berechtigungen deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="7c4a0-187">By default, remote link permissions are disabled.</span></span>

    **<span data-ttu-id="7c4a0-188">fsutil-Verhaltens Satz SymlinkEvaluation R2R: 1</span><span class="sxs-lookup"><span data-stu-id="7c4a0-188">fsutil behavior set SymlinkEvaluation R2R:1</span></span>**

    <span data-ttu-id="7c4a0-189">**Hinweis**  Auf dem Speicherserver müssen entsprechende Link Berechtigungen aktiviert sein.</span><span class="sxs-lookup"><span data-stu-id="7c4a0-189">**Note** On the storage server, appropriate link permissions must be enabled.</span></span> <span data-ttu-id="7c4a0-190">Je nach Speicherort des Links und der Datei "sftfs. FSD" sind die Berechtigungen **L2L: 1** oder **L2R: 1** oder **R2L: 1** oder **R2R: 1**.</span><span class="sxs-lookup"><span data-stu-id="7c4a0-190">Depending on the location of link and the Sftfs.fsd file, the permissions are **L2L:1** or **L2R:1** or **R2L:1** or **R2R:1**.</span></span>

     

4.  <span data-ttu-id="7c4a0-191">Wenn Sie den App-V RDS-Client konfigurieren, legen Sie den AppFS-Schlüssel FileName-Wert gleich dem UNC-Pfad der FSD-Datei fest, die den symbolischen Link verwendet.</span><span class="sxs-lookup"><span data-stu-id="7c4a0-191">When you configure the App-V RDS Client, set the AppFS key FILENAME value equal to the UNC path of the FSD file that is using the symbolic link.</span></span> <span data-ttu-id="7c4a0-192">Legen Sie beispielsweise den Dateinamen auf \\\\VDIHostserver\\Symlinkname.</span><span class="sxs-lookup"><span data-stu-id="7c4a0-192">For example, set the file name to \\\\VDIHostserver\\Symlinkname.</span></span> <span data-ttu-id="7c4a0-193">Wenn der App-V-Client zuerst auf den Cache zugreift, übergibt der symbolische Link an den Client ein Handle für die Cachedatei.</span><span class="sxs-lookup"><span data-stu-id="7c4a0-193">When the App-V client first accesses the cache, the symbolic link passes to the client a handle to the cache file.</span></span> <span data-ttu-id="7c4a0-194">Der Client verwendet dieses Handle weiterhin, solange der Client ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7c4a0-194">The client continues to use that handle as long as the client is running.</span></span> <span data-ttu-id="7c4a0-195">Der Wert des symbolischen Links kann auch dann sicher aktualisiert werden, wenn vorhandene Clients den alten freigegebenen Cache geöffnet haben.</span><span class="sxs-lookup"><span data-stu-id="7c4a0-195">The value of the symbolic link can safely be updated even if existing clients have the old shared cache open.</span></span>

5.  <span data-ttu-id="7c4a0-196">Wenn Sie ein Paket aktualisieren oder dem Cache ein neues Paket hinzufügen müssen, führen Sie die Schritte 1 bis 4 des Aktualisierungsvorgangs aus.</span><span class="sxs-lookup"><span data-stu-id="7c4a0-196">When you must upgrade a package or to add a new package to the cache, follow steps 1 through 4 of the upgrade procedure.</span></span> <span data-ttu-id="7c4a0-197">Löschen Sie dann den symbolischen Link, und erstellen Sie ihn erneut, um auf die neue Version der freigegebenen Cachedatei zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="7c4a0-197">Then, delete the symbolic link and re-create it to point to the new version of the shared cache file.</span></span> <span data-ttu-id="7c4a0-198">Dadurch wird sichergestellt, dass jeder RDS-Server die aktualisierte Kopie des Caches erhält, wenn die App-V-Clienttreiber neu gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="7c4a0-198">This guarantees that each RDS server receives the updated copy of the cache when the App-V client drivers restart.</span></span> <span data-ttu-id="7c4a0-199">Beim Neustart des RDS-Servers erhält der App-V-Client ein Handle für die aktualisierte Kopie des Caches, da der Client den Pfad verwendet, der den aktualisierten symbolischen Link enthält.</span><span class="sxs-lookup"><span data-stu-id="7c4a0-199">When the RDS server is restarted, the App-V client receives a handle to the updated copy of the cache because the client uses the path that contains the updated symbolic link.</span></span> <span data-ttu-id="7c4a0-200">Dann können die Benutzer auf die neuen und aktualisierten Anwendungen zugreifen.</span><span class="sxs-lookup"><span data-stu-id="7c4a0-200">Then, the users have access to the new and updated applications.</span></span>

## <span data-ttu-id="7c4a0-201">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="7c4a0-201">Related topics</span></span>


[<span data-ttu-id="7c4a0-202">So installieren Sie Application Virtualization Management Server</span><span class="sxs-lookup"><span data-stu-id="7c4a0-202">How to Install Application Virtualization Management Server</span></span>](how-to-install-application-virtualization-management-server.md)

[<span data-ttu-id="7c4a0-203">So installieren Sie Application Virtualization Client manuell</span><span class="sxs-lookup"><span data-stu-id="7c4a0-203">How to Manually Install the Application Virtualization Client</span></span>](how-to-manually-install-the-application-virtualization-client.md)

[<span data-ttu-id="7c4a0-204">So installieren Sie den Client über die Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="7c4a0-204">How to Install the Client by Using the Command Line</span></span>](how-to-install-the-client-by-using-the-command-line-new.md)

 

 





