---
title: Versionshinweise für App-V 5.1
description: Versionshinweise für App-V 5.1
author: dansimp
ms.assetid: 62c5be3b-0a46-4512-93ed-97c23184f343
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 09/26/2016
ms.openlocfilehash: 7437a16bc10b21bb15b0f8307c2711177e78cb72
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804880"
---
# <span data-ttu-id="1bce7-103">Versionshinweise für App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="1bce7-103">Release Notes for App-V 5.1</span></span>


<span data-ttu-id="1bce7-104">Im folgenden werden bekannte Probleme in Microsoft Application Virtualization (App-V) 5,1.</span><span class="sxs-lookup"><span data-stu-id="1bce7-104">The following are known issues in Microsoft Application Virtualization (App-V) 5.1.</span></span>

## <span data-ttu-id="1bce7-105">Beim Aktualisieren der Veröffentlichung zwischen App-v 5,0 SP3-Verwaltungs Server und App-v 5,1-Client unter Windows 10 tritt ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="1bce7-105">Error occurs during publishing refresh between App-V 5.0 SP3 Management Server and App-V 5.1 Client on Windows 10</span></span>


<span data-ttu-id="1bce7-106">Beim Synchronisieren von Paketen vom APP-v 5,0 SP3-Verwaltungsserver zu einem App-v 5,1-Client unter Windows 10 wird ein Fehler während der Veröffentlichungsaktualisierung generiert.</span><span class="sxs-lookup"><span data-stu-id="1bce7-106">An error is generated during publishing refresh when synchronizing packages from the App-V 5.0 SP3 management server to an App-V 5.1 client on Windows 10 .</span></span> <span data-ttu-id="1bce7-107">Dieser Fehler tritt auf, weil der App-V 5,0 SP3-Server das Windows 10-Betriebssystem nicht versteht, das in der Veröffentlichungs-URL angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="1bce7-107">This error occurs because the App-V 5.0 SP3 server does not understand the Windows 10 operating system that is specified in the publishing URL.</span></span> <span data-ttu-id="1bce7-108">Das Problem wurde für den App-v 5,1-Veröffentlichungsserver behoben, wird jedoch nicht in Versionen von App-v 5,0 SP3 oder früher portiert.</span><span class="sxs-lookup"><span data-stu-id="1bce7-108">The issue is fixed for App-V 5.1 publishing server, but is not backported to versions of App-V 5.0 SP3 or earlier.</span></span>

<span data-ttu-id="1bce7-109">**Problemumgehung**: Aktualisieren Sie den App-v 5,0-Verwaltungsserver auf den App-v 5,1-Verwaltungsserver für Windows 10-Clients.</span><span class="sxs-lookup"><span data-stu-id="1bce7-109">**Workaround**: Upgrade the App-V 5.0 Management server to the App-V 5.1 Management server for Windows 10 Clients.</span></span>

## <span data-ttu-id="1bce7-110">Benutzerdefinierte Konfigurationen werden nicht auf Pakete angewendet, die Global veröffentlicht werden, wenn Sie mit dem App-V 5,1-Server festgesetzt werden.</span><span class="sxs-lookup"><span data-stu-id="1bce7-110">Custom configurations do not get applied for packages that will be published globally if they are set using the App-V 5.1 Server</span></span>


<span data-ttu-id="1bce7-111">Wenn Sie einer Anzeigengruppe, die Computerkonten enthält, ein Paket zuweisen und eine benutzerdefinierte Konfiguration mit dem App-V-Server auf diese Gruppe anwenden, wird die benutzerdefinierte Konfiguration nicht auf diese Computer angewendet.</span><span class="sxs-lookup"><span data-stu-id="1bce7-111">If you assign a package to an AD group that contains machine accounts and apply a custom configuration to that group using the App-V Server, the custom configuration will not be applied to those machines.</span></span> <span data-ttu-id="1bce7-112">Der App-V 5,1-Client veröffentlicht Pakete, die einem Computerkonto Global zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="1bce7-112">The App-V 5.1 Client will publish packages assigned to a machine account globally.</span></span> <span data-ttu-id="1bce7-113">Es werden jedoch benutzerdefinierte Konfigurationsdateien pro Benutzer im Profil jedes Benutzers gespeichert.</span><span class="sxs-lookup"><span data-stu-id="1bce7-113">However, it stores custom configuration files per user in each user’s profile.</span></span> <span data-ttu-id="1bce7-114">Global veröffentlichte Pakete haben keinen Zugriff auf diese benutzerdefinierte Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="1bce7-114">Globally published packages will not have access to this custom configuration.</span></span>

<span data-ttu-id="1bce7-115">**Problemumgehung**: führen Sie eine der folgenden Aktionen aus:</span><span class="sxs-lookup"><span data-stu-id="1bce7-115">**Workaround**: Do one of the following:</span></span>

-   <span data-ttu-id="1bce7-116">Weisen Sie das Paketgruppen zu, die nur Benutzerkonten enthalten.</span><span class="sxs-lookup"><span data-stu-id="1bce7-116">Assign the package to groups containing only user accounts.</span></span> <span data-ttu-id="1bce7-117">Dadurch wird sichergestellt, dass die benutzerdefinierte Konfiguration des Pakets in den Profilen jedes Benutzers gespeichert wird und ordnungsgemäß angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="1bce7-117">This will ensure that the package’s custom configuration will be stored in each user’s profile and will be applied correctly.</span></span>

-   <span data-ttu-id="1bce7-118">Erstellen Sie eine benutzerdefinierte Konfigurationsdatei für die Bereitstellung, und wenden Sie Sie auf das Paket auf dem Client mithilfe des Cmdlets "Add-AppvClientPackage" mit dem Parameter "– DynamicDeploymentConfiguration" an.</span><span class="sxs-lookup"><span data-stu-id="1bce7-118">Create a custom deployment configuration file and apply it to the package on the client using the Add-AppvClientPackage cmdlet with the –DynamicDeploymentConfiguration parameter.</span></span> <span data-ttu-id="1bce7-119">Weitere Informationen finden Sie unter Informationen [zur dynamischen Konfiguration von App-V 5,1](about-app-v-51-dynamic-configuration.md) .</span><span class="sxs-lookup"><span data-stu-id="1bce7-119">See [About App-V 5.1 Dynamic Configuration](about-app-v-51-dynamic-configuration.md) for more information.</span></span>

-   <span data-ttu-id="1bce7-120">Erstellen Sie ein neues Paket mit der benutzerdefinierten Konfiguration mit dem App-V 5,1-Sequenzer.</span><span class="sxs-lookup"><span data-stu-id="1bce7-120">Create a new package with the custom configuration using the App-V 5.1 Sequencer.</span></span>

## <span data-ttu-id="1bce7-121">Server Dateien werden nach der Installation der neuen App-V 5,1-Server nicht gelöscht</span><span class="sxs-lookup"><span data-stu-id="1bce7-121">Server files not deleted after new App-V 5.1 Server installation</span></span>


<span data-ttu-id="1bce7-122">Wenn Sie den App-v 5,0 SP1-Server deinstallieren und dann den App-v 5,1-Server installieren, schlägt die Installation fehl, die falsche Version des Verwaltungsservers wird installiert, und es wird eine Fehlermeldung zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="1bce7-122">If you uninstall the App-V 5.0 SP1 Server and then install the App-V 5.1 Server, the installation fails, the wrong version of the Management server is installed, and an error message is returned.</span></span> <span data-ttu-id="1bce7-123">Das Problem tritt auf, weil die Server Dateien nicht gelöscht werden, wenn Sie App-V 5,0 SP1 deinstallieren, sodass der Installationsvorgang anstelle einer neuen Installation ein Upgrade durchführt.</span><span class="sxs-lookup"><span data-stu-id="1bce7-123">The issue occurs because the Server files are not being deleted when you uninstall App-V 5.0 SP1, so the installation process does an upgrade instead of a new installation.</span></span>

<span data-ttu-id="1bce7-124">**Problemumgehung**: Löschen Sie diesen Registrierungsschlüssel, bevor Sie mit der Installation von App-V 5,1 beginnen:</span><span class="sxs-lookup"><span data-stu-id="1bce7-124">**Workaround**: Delete this registry key before you start installing App-V 5.1:</span></span>

<span data-ttu-id="1bce7-125">Suchen und löschen Sie unter HKEY \ _LOCAL \ _MACHINE \\software\\wow6432node\\microsoft\\windows\\currentversion\\uninstall den Installations-GUID-Schlüssel, der den DWORD-Wert "DisplayName" mit dem Wert "Microsoft Application Virtualization (App-V) Server" enthält.</span><span class="sxs-lookup"><span data-stu-id="1bce7-125">Under HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Wow6432Node\\Microsoft\\Windows\\CurrentVersion\\Uninstall, locate and delete the installation GUID key that contains the DWORD value "DisplayName" with value data "Microsoft Application Virtualization (App-V) Server".</span></span> <span data-ttu-id="1bce7-126">Dies ist der einzige Schlüssel, der gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="1bce7-126">This is the only key that should be deleted.</span></span>

## <span data-ttu-id="1bce7-127">Manuell hinzugefügte Dateitypen Zuordnungen werden nicht ordnungsgemäß gespeichert</span><span class="sxs-lookup"><span data-stu-id="1bce7-127">File type associations added manually are not saved correctly</span></span>


<span data-ttu-id="1bce7-128">Dateitypzuordnungen, die einem Anwendungspaket manuell mithilfe der Registerkarte Verknüpfungen und FTA am Ende des Anwendungs Aktualisierungs-Assistenten hinzugefügt wurden, werden nicht ordnungsgemäß gespeichert.</span><span class="sxs-lookup"><span data-stu-id="1bce7-128">File type associations added to an application package manually using the Shortcuts and FTAs tab at the end of the application upgrade wizard are not saved correctly.</span></span> <span data-ttu-id="1bce7-129">Sie stehen dem App-V-Client oder dem Sequencer beim erneuten Aktualisieren des gespeicherten Pakets nicht zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="1bce7-129">They will not be available to the App-V Client or to the Sequencer when updating the saved package again.</span></span>

<span data-ttu-id="1bce7-130">**Problemumgehung**: Wenn Sie eine Dateitypzuordnung hinzufügen möchten, öffnen Sie das Paket zur Änderung, und führen Sie den Update-Assistenten aus.</span><span class="sxs-lookup"><span data-stu-id="1bce7-130">**Workaround**: To add a file type association, open the package for modification and run the update wizard.</span></span> <span data-ttu-id="1bce7-131">Fügen Sie während des Installationsschritts die neue Dateitypzuordnung über das Betriebssystem hinzu.</span><span class="sxs-lookup"><span data-stu-id="1bce7-131">During the Installation step, add the new file type association through the operating system.</span></span> <span data-ttu-id="1bce7-132">Der Sequencer erkennt die neue Zuordnung in der Systemregistrierung und fügt Sie der virtuellen Registrierung des Pakets hinzu, wo Sie für den Client verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="1bce7-132">The sequencer will detect the new association in the system registry and add it to the package’s virtual registry, where it will be available to the client.</span></span>

## <span data-ttu-id="1bce7-133">Beim Streaming von Paketen im freigegebenen Inhaltsspeicher (SCS)-Modus zu einem Client, der auch mit AppLocker verwaltet wird, werden zusätzliche Daten auf den lokalen Datenträger geschrieben.</span><span class="sxs-lookup"><span data-stu-id="1bce7-133">When streaming packages in Shared Content Store (SCS) mode to a client that is also managed with AppLocker, additional data is written to the local disk.</span></span>


<span data-ttu-id="1bce7-134">Um die Menge der auf den lokalen Datenträger des Clients geschriebenen Daten zu verringern, können Sie den SCS-Modus auf dem App-V 5,1-Client aktivieren, um den Inhalt eines Pakets bei Bedarf zu streamen.</span><span class="sxs-lookup"><span data-stu-id="1bce7-134">To decrease the amount of data written to a client’s local disk, you can enable SCS mode on the App-V 5.1 Client to stream the contents of a package on demand.</span></span> <span data-ttu-id="1bce7-135">Wenn AppLocker jedoch eine Anwendung innerhalb des Pakets verwaltet, werden möglicherweise einige Daten auf den lokalen Datenträger des Clients geschrieben, die sonst nicht geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="1bce7-135">However, if AppLocker manages an application within the package, some data might be written to the client’s local disk that would not otherwise be written.</span></span>

<span data-ttu-id="1bce7-136">**Problemumgehung**: keine</span><span class="sxs-lookup"><span data-stu-id="1bce7-136">**Workaround**: None</span></span>

## <span data-ttu-id="1bce7-137">Im Dialogfeld "Management Console-Paket hinzufügen" steht die Schaltfläche "Durchsuchen" bei Verwendung von Chrome oder Firefox nicht zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="1bce7-137">In the Management Console Add Package dialog box, the Browse button is not available when using Chrome or Firefox</span></span>


<span data-ttu-id="1bce7-138">Wenn Sie auf der Seite Pakete der Verwaltungskonsole in der unteren rechten Ecke auf **Hinzufügen oder aktualisieren** klicken, wird das Dialogfeld **Paket hinzufügen** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="1bce7-138">On the Packages page of the Management Console, if you click **Add or Upgrade** in the lower-right corner, the **Add Package** dialog box appears.</span></span> <span data-ttu-id="1bce7-139">Wenn Sie mit Chrome oder Firefox als Browser auf die Verwaltungskonsole zugreifen, können Sie nicht zum Speicherort des Pakets navigieren.</span><span class="sxs-lookup"><span data-stu-id="1bce7-139">If you are accessing the Management Console using Chrome or Firefox as your browser, you will not be able to browse to the location of the package.</span></span>

<span data-ttu-id="1bce7-140">**Problemumgehung**: Geben Sie den Pfad des Pakets in das Eingabefeld **Paket hinzufügen** ein, oder kopieren Sie ihn, und fügen Sie ihn ein.</span><span class="sxs-lookup"><span data-stu-id="1bce7-140">**Workaround**: Type or copy and paste the path to the package into the **Add Package** input field.</span></span> <span data-ttu-id="1bce7-141">Wenn die Verwaltungskonsole Zugriff auf diesen Pfad hat, können Sie das Paket hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="1bce7-141">If the Management Console has access to this path, you will be able to add the package.</span></span> <span data-ttu-id="1bce7-142">Wenn sich das Paket auf einer Netzwerkfreigabe befindet, können Sie mit dem Datei-Explorer zu dem Speicherort navigieren, indem Sie die folgenden Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="1bce7-142">If the package is on a network share, you can browse to the location using File Explorer by doing these steps:</span></span>

1.  <span data-ttu-id="1bce7-143">Klicken Sie bei gedrückter **UMSCHALTTASTE**mit der rechten Maustaste auf die Paketdatei.</span><span class="sxs-lookup"><span data-stu-id="1bce7-143">While pressing **Shift**, right-click on the package file</span></span>

2.  <span data-ttu-id="1bce7-144">Wählen Sie **als Pfad kopieren** aus.</span><span class="sxs-lookup"><span data-stu-id="1bce7-144">Select **Copy as path**</span></span>

3.  <span data-ttu-id="1bce7-145">Einfügen des Pfads in das Eingabefeld des Dialogfelds " **Paket hinzufügen** "</span><span class="sxs-lookup"><span data-stu-id="1bce7-145">Paste the path into the **Add Package** dialog box input field</span></span>

## <a href="" id="upgrading-app-v-management-server-to-5-1-sometimes-fails-with-the-message--a-database-error-occurred-"></a><span data-ttu-id="1bce7-146">Das Upgrade von App-V Management Server auf 5,1 schlägt manchmal mit der Meldung "ein Datenbankfehler ist aufgetreten" fehl</span><span class="sxs-lookup"><span data-stu-id="1bce7-146">Upgrading App-V Management Server to 5.1 sometimes fails with the message “A database error occurred”</span></span>


<span data-ttu-id="1bce7-147">Wenn Sie den App-v 5,0 SP1-Verwaltungsserver installieren und dann versuchen, auf App-v 5,1-Server zu aktualisieren, wenn mehrere Verbindungsgruppen konfiguriert und aktiviert sind, wird der folgende Fehler angezeigt: "ein Datenbankfehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="1bce7-147">If you install the App-V 5.0 SP1 Management Server, and then try to upgrade to App-V 5.1 Server when multiple connection groups are configured and enabled, the following error is displayed: “A database error occurred.</span></span> <span data-ttu-id="1bce7-148">Ursache: ' Ungültiger Spaltenname ' PackageOptional '.</span><span class="sxs-lookup"><span data-stu-id="1bce7-148">Reason: 'Invalid column name 'PackageOptional'.</span></span> <span data-ttu-id="1bce7-149">Ungültiger Spaltenname ' VersionOptional '. "</span><span class="sxs-lookup"><span data-stu-id="1bce7-149">Invalid column name 'VersionOptional'.”</span></span>

<span data-ttu-id="1bce7-150">**Problemumgehung**: führen Sie diesen Befehl für Ihre SQL-Datenbank aus:</span><span class="sxs-lookup"><span data-stu-id="1bce7-150">**Workaround**: Run this command on your SQL database:</span></span>

`ALTER TABLE AppVManagement.dbo.PackageGroupMembers ADD PackageOptional bit NOT NULL DEFAULT 0, VersionOptional bit NOT NULL DEFAULT 0`

<span data-ttu-id="1bce7-151">Dabei ist "AppVManagement" der Name der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="1bce7-151">where “AppVManagement” is the name of the database.</span></span>

## <span data-ttu-id="1bce7-152">Benutzer können ein Paket nicht in einer vom Benutzer veröffentlichten Verbindungsgruppe öffnen, wenn Sie ein optionales Paket hinzufügen oder entfernen.</span><span class="sxs-lookup"><span data-stu-id="1bce7-152">Users cannot open a package in a user-published connection group if you add or remove an optional package</span></span>


<span data-ttu-id="1bce7-153">In Umgebungen, in denen der RDS-Client ausgeführt wird oder die mehrere gleichzeitige Benutzer pro Computer aufweisen, können angemeldete Benutzer keine Anwendungen in Paketen öffnen, die sich in einer vom Benutzer veröffentlichten Verbindungsgruppe befinden, wenn ein optionales Paket zur Verbindungsgruppe hinzugefügt oder daraus entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="1bce7-153">In environments that are running the RDS Client or that have multiple concurrent users per computer, logged-in users cannot open applications in packages that are in a user-published connection group if an optional package is added to or removed from the connection group.</span></span>

<span data-ttu-id="1bce7-154">**Problemumgehung**: lassen Sie die Benutzer sich abmelden und melden Sie sich dann wieder an.</span><span class="sxs-lookup"><span data-stu-id="1bce7-154">**Workaround**: Have users log out and then log back in.</span></span>

## <span data-ttu-id="1bce7-155">Fehlermeldung wird fälschlicherweise angezeigt, wenn die Verbindungsgruppe nur für den Benutzer veröffentlicht wird</span><span class="sxs-lookup"><span data-stu-id="1bce7-155">Error message is erroneously displayed when the connection group is published only to the user</span></span>


<span data-ttu-id="1bce7-156">Wenn Sie Repair-AppvClientConnectionGroup ausführen, wird der folgende Fehler angezeigt, auch wenn die Verbindungsgruppe nur für den Benutzer veröffentlicht wird: "interner App-V-Integrations Fehler: das Paket wurde nicht für den Benutzer integriert.</span><span class="sxs-lookup"><span data-stu-id="1bce7-156">When you run Repair-AppvClientConnectionGroup, the following error is displayed, even when the connection group is published only to the user: “Internal App-V Integration error: Package not integrated for the user.</span></span> <span data-ttu-id="1bce7-157">Stellen Sie sicher, dass das Paket dem Computer hinzugefügt und für den Benutzer veröffentlicht wird. "</span><span class="sxs-lookup"><span data-stu-id="1bce7-157">Please ensure that the package is added to the machine and published to the user.”</span></span>

<span data-ttu-id="1bce7-158">**Problemumgehung**: führen Sie eine der folgenden Aktionen aus:</span><span class="sxs-lookup"><span data-stu-id="1bce7-158">**Workaround**: Do one of the following:</span></span>

-   <span data-ttu-id="1bce7-159">Alle Pakete in einer Verbindungsgruppe veröffentlichen</span><span class="sxs-lookup"><span data-stu-id="1bce7-159">Publish all packages in a connection group.</span></span>

    <span data-ttu-id="1bce7-160">Das Problem tritt auf, wenn die zu reparierende Verbindungsgruppe Pakete enthält, die für den Benutzer nicht verfügbar sind oder nicht zur Verfügung stehen (also nicht global oder für den Benutzer veröffentlicht werden).</span><span class="sxs-lookup"><span data-stu-id="1bce7-160">The problem arises when the connection group being repaired has packages that are missing or not available to the user (that is, not published globally or to the user).</span></span> <span data-ttu-id="1bce7-161">Die Reparatur funktioniert jedoch, wenn alle Pakete der Verbindungsgruppe verfügbar sind, um sicherzustellen, dass alle Pakete veröffentlicht werden.</span><span class="sxs-lookup"><span data-stu-id="1bce7-161">However, the repair will work if all of the connection group’s packages are available, so ensure that all packages are published.</span></span>

-   <span data-ttu-id="1bce7-162">Reparieren Sie Pakete einzeln mit dem Befehl reparieren-AppvClientPackage statt mit dem Befehl Repair-AppvClientConnectionGroup.</span><span class="sxs-lookup"><span data-stu-id="1bce7-162">Repair packages individually using the Repair-AppvClientPackage command rather than the Repair-AppvClientConnectionGroup command.</span></span>

    <span data-ttu-id="1bce7-163">Ermitteln Sie, welche Pakete für die Benutzer verfügbar sind, und führen Sie dann den Befehl Repair-AppvClientPackage einmal für jedes Paket aus.</span><span class="sxs-lookup"><span data-stu-id="1bce7-163">Determine which packages are available to users and then run the Repair-AppvClientPackage command once for each package.</span></span> <span data-ttu-id="1bce7-164">Verwenden Sie PowerShell-Cmdlets, um folgende Aktionen auszuführen:</span><span class="sxs-lookup"><span data-stu-id="1bce7-164">Use PowerShell cmdlets to do the following:</span></span>

    1.  <span data-ttu-id="1bce7-165">Rufen Sie alle Pakete in einer Verbindungsgruppe ab.</span><span class="sxs-lookup"><span data-stu-id="1bce7-165">Get all the packages in a connection group.</span></span>

    2.  <span data-ttu-id="1bce7-166">Überprüfen Sie, ob die einzelnen Pakete aktuell veröffentlicht sind.</span><span class="sxs-lookup"><span data-stu-id="1bce7-166">Check to see if each package is currently published.</span></span>

    3.  <span data-ttu-id="1bce7-167">Wenn das Paket aktuell veröffentlicht wird, führen Sie AppvClientPackage für dieses Paket aus.</span><span class="sxs-lookup"><span data-stu-id="1bce7-167">If the package is currently published, run Repair-AppvClientPackage on that package.</span></span>

## <span data-ttu-id="1bce7-168">Symbole werden in Sequencer nicht richtig angezeigt</span><span class="sxs-lookup"><span data-stu-id="1bce7-168">Icons not displayed properly in Sequencer</span></span>


<span data-ttu-id="1bce7-169">Symbole auf der Registerkarte Verknüpfungen und Dateitypzuordnungen werden beim Ändern eines Pakets im App-V-Sequenzer nicht richtig angezeigt.</span><span class="sxs-lookup"><span data-stu-id="1bce7-169">Icons in the Shortcuts and File Type Associations tab are not displayed correctly when modifying a package in the App-V Sequencer.</span></span> <span data-ttu-id="1bce7-170">Dieses Problem tritt auf, wenn die Größe der Symbole nicht 16x16 oder 32 x 32 ist.</span><span class="sxs-lookup"><span data-stu-id="1bce7-170">This problem occurs when the size of the icons are not 16x16 or 32x32.</span></span>

<span data-ttu-id="1bce7-171">**Problemumgehung**: Verwenden Sie nur Symbole, die 16x16 oder 32 x 32 sind.</span><span class="sxs-lookup"><span data-stu-id="1bce7-171">**Workaround**: Only use icons that are 16x16 or 32x32.</span></span>

## <span data-ttu-id="1bce7-172">InsertVersionInfo. SQL-Skript ist für die Verwaltungsdatenbank nicht mehr erforderlich</span><span class="sxs-lookup"><span data-stu-id="1bce7-172">InsertVersionInfo.sql script no longer required for the Management Database</span></span>


<span data-ttu-id="1bce7-173">Das InsertVersionInfo. SQL-Skript ist für Versionen der APP-v-Verwaltungsdatenbank später als App-v 5,0 SP3 nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="1bce7-173">The InsertVersionInfo.sql script is not required for versions of the App-V management database later than App-V 5.0 SP3.</span></span>

<span data-ttu-id="1bce7-174">Das Skript "Permissions. SQL" sollte gemäß **Schritt 2** im [KB-Artikel 3031340](https://support.microsoft.com/kb/3031340)aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="1bce7-174">The Permissions.sql script should be updated according to **Step 2** in [KB article 3031340](https://support.microsoft.com/kb/3031340).</span></span>

<span data-ttu-id="1bce7-175">**Wichtig** 
 **Schritt 1** ist für Versionen von App-v später als App-v 5,0 SP3 nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="1bce7-175">**Important**
**Step 1** is not required for versions of App-V later than App-V 5.0 SP3.</span></span>

 

## <span data-ttu-id="1bce7-176">Microsoft Visual Studio 2012 nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="1bce7-176">Microsoft Visual Studio 2012 not supported</span></span>


<span data-ttu-id="1bce7-177">App-V 5,1 unterstützt Visual Studio 2012 nicht.</span><span class="sxs-lookup"><span data-stu-id="1bce7-177">App-V 5.1 does not support Visual Studio 2012.</span></span>

<span data-ttu-id="1bce7-178">**Problemumgehung**: keine</span><span class="sxs-lookup"><span data-stu-id="1bce7-178">**Workaround**: None</span></span>

## <span data-ttu-id="1bce7-179">Einschränkungen für Anwendungsdatei Namen für App-V 5. x-Sequenzer</span><span class="sxs-lookup"><span data-stu-id="1bce7-179">Application filename restrictions for App-V 5.x Sequencer</span></span>


<span data-ttu-id="1bce7-180">App-V 5. x Sequencer kann keine Anwendungen mit Dateinamen abgleichen, die "CO_ &lt; x &gt; " entsprechen, wobei x eine beliebige Zahl ist.</span><span class="sxs-lookup"><span data-stu-id="1bce7-180">The App-V 5.x Sequencer cannot sequence applications with filenames matching "CO_&lt;x&gt;" where x is any numeral.</span></span> <span data-ttu-id="1bce7-181">Fehler 0x8007139F wird generiert.</span><span class="sxs-lookup"><span data-stu-id="1bce7-181">Error 0x8007139F will be generated.</span></span>

<span data-ttu-id="1bce7-182">**Problemumgehung**: Verwenden Sie einen anderen Dateinamen</span><span class="sxs-lookup"><span data-stu-id="1bce7-182">**Workaround**: Use a different filename</span></span>

## <span data-ttu-id="1bce7-183">Zeitweilige Fehlermeldung "Datei nicht gefunden" beim Bereitstellen eines Pakets</span><span class="sxs-lookup"><span data-stu-id="1bce7-183">Intermittent "File Not Found" error when Mounting a Package</span></span>


<span data-ttu-id="1bce7-184">Gelegentlich wird beim Bereitstellen eines Pakets ein Fehler "Datei nicht gefunden" (0x80070002) generiert.</span><span class="sxs-lookup"><span data-stu-id="1bce7-184">Occasionally when mounting a package, a "File Not Found" (0x80070002) error is generated.</span></span> <span data-ttu-id="1bce7-185">In der Regel tritt dies auf, wenn ein Ordner in einem App-V-Paket viele Dateien enthält (also 20K oder mehr).</span><span class="sxs-lookup"><span data-stu-id="1bce7-185">Typically, this occurs when a folder in an App-V package contains many files ( i.e. 20K or more).</span></span> <span data-ttu-id="1bce7-186">Dies kann dazu führen, dass Streaming länger als erwartet dauert und zu einem Timeout führt, das die Fehlermeldung "Datei nicht gefunden" generiert.</span><span class="sxs-lookup"><span data-stu-id="1bce7-186">This can cause streaming to take longer than expected and to time out which generates the "File Not Found" error.</span></span>

<span data-ttu-id="1bce7-187">**Problemumgehung**: ab HF06 wurde ein neuer Registrierungsschlüssel eingeführt, um die Verlängerung dieses Timeoutzeitraums zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="1bce7-187">**Workaround**: Starting with HF06, a new registry key has been introduced to enable extending this time-out period.</span></span>

<table>
<colgroup>
<col width="20%" />
<col width="80%" />
</colgroup>
<tbody>
<tr>
<td align="left"><span data-ttu-id="1bce7-188">Pfad</span><span class="sxs-lookup"><span data-stu-id="1bce7-188">Path</span></span></td>
<td align="left"><span data-ttu-id="1bce7-189">HKEY_LOCAL_MACHINE \software\microsoft\appv\client\streaming</span><span class="sxs-lookup"><span data-stu-id="1bce7-189">HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\AppV\Client\Streaming</span></span></td>
</tr>
<tr>
<td align="left"><span data-ttu-id="1bce7-190">Einstellung</span><span class="sxs-lookup"><span data-stu-id="1bce7-190">Setting</span></span></td>
<td align="left"><span data-ttu-id="1bce7-191">StreamResponseWaitTimeout</span><span class="sxs-lookup"><span data-stu-id="1bce7-191">StreamResponseWaitTimeout</span></span></td>
</tr>
<tr>
<td align="left"><span data-ttu-id="1bce7-192">Datentyp</span><span class="sxs-lookup"><span data-stu-id="1bce7-192">DataType</span></span></td>
<td align="left"><span data-ttu-id="1bce7-193">DWORD</span><span class="sxs-lookup"><span data-stu-id="1bce7-193">DWORD</span></span></td>
</tr>
<tr>
<td align="left"><span data-ttu-id="1bce7-194">Einheiten</span><span class="sxs-lookup"><span data-stu-id="1bce7-194">Units</span></span></td>
<td align="left"><span data-ttu-id="1bce7-195">Sekunden</span><span class="sxs-lookup"><span data-stu-id="1bce7-195">Seconds</span></span></td>
</tr>
<tr>
<td align="left"><span data-ttu-id="1bce7-196">Standard</span><span class="sxs-lookup"><span data-stu-id="1bce7-196">Default</span></span></td>
<td align="left"><span data-ttu-id="1bce7-197">5</span><span class="sxs-lookup"><span data-stu-id="1bce7-197">5</span></span><br />
<strong><span data-ttu-id="1bce7-198">Hinweis </strong> : dieser Wert ist der Standardwert, wenn der Registrierungsschlüssel nicht definiert ist oder ein Wert &lt; = 5 angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="1bce7-198">Note</strong>: this value is the default if the registry key is not defined or a value &lt;=5 is specified.</span></span>
</td>
</tr>
</tbody>
</table>






## <span data-ttu-id="1bce7-199">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="1bce7-199">Related topics</span></span>


[<span data-ttu-id="1bce7-200">Informationen zu App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="1bce7-200">About App-V 5.1</span></span>](about-app-v-51.md)

 

 





