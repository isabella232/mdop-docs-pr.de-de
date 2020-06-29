---
title: Versionshinweise für MBAM 1.0
description: Versionshinweise für MBAM 1.0
author: dansimp
ms.assetid: d82fddde-c360-48ef-86a0-d9b5fe066861
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 705fd1b936da1454081dd14a7f075f642fc4a405
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811509"
---
# <span data-ttu-id="02bab-103">Versionshinweise für MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="02bab-103">Release Notes for MBAM 1.0</span></span>


**<span data-ttu-id="02bab-104">Drücken Sie STRG + F, um nach einem bestimmten Problem in diesen Versionshinweisen zu suchen.</span><span class="sxs-lookup"><span data-stu-id="02bab-104">To search for a specific issue in these release notes, press CTRL+F.</span></span>**

<span data-ttu-id="02bab-105">Lesen Sie diese Versionshinweise gründlich, bevor Sie die Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) installieren.</span><span class="sxs-lookup"><span data-stu-id="02bab-105">Read these release notes thoroughly before you install Microsoft BitLocker Administration and Monitoring (MBAM).</span></span>

<span data-ttu-id="02bab-106">Diese Versionshinweise enthalten Informationen, die zur erfolgreichen Installation von MBAM erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="02bab-106">These release notes contain information that is required to successfully install MBAM.</span></span> <span data-ttu-id="02bab-107">Die Anmerkungen zu dieser Version enthalten auch Informationen, die in der Produktdokumentation nicht zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="02bab-107">The release notes also contain information that is not available in the product documentation.</span></span> <span data-ttu-id="02bab-108">Wenn es einen Unterschied zwischen diesen Versionshinweisen und anderer MBAM-Dokumentation gibt, sollte die neueste Änderung als autorisierend angesehen werden.</span><span class="sxs-lookup"><span data-stu-id="02bab-108">If there is a difference between these release notes and other MBAM documentation, the latest change should be considered authoritative.</span></span> <span data-ttu-id="02bab-109">Diese Versionshinweise ersetzen die Inhalte, die in diesem Produkt enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="02bab-109">These release notes supersede the content that is included with this product.</span></span>

## <span data-ttu-id="02bab-110">Informationen zur Produktdokumentation</span><span class="sxs-lookup"><span data-stu-id="02bab-110">About the Product Documentation</span></span>


<span data-ttu-id="02bab-111">Informationen zur MBAM-Dokumentation finden Sie auf der MBAM-Startseite auf der Microsoft TechNet-Website.</span><span class="sxs-lookup"><span data-stu-id="02bab-111">For information about MBAM documentation, see the MBAM home page on Microsoft TechNet.</span></span>

<span data-ttu-id="02bab-112">Eine herunterladbare Kopie der MBAM-Dokumentation finden Sie <https://go.microsoft.com/fwlink/p/?LinkId=225356> im Microsoft Download Center.</span><span class="sxs-lookup"><span data-stu-id="02bab-112">To obtain a downloadable copy of the MBAM documentation, see <https://go.microsoft.com/fwlink/p/?LinkId=225356> on the Microsoft Download Center.</span></span>

## <span data-ttu-id="02bab-113">Feedback geben</span><span class="sxs-lookup"><span data-stu-id="02bab-113">Provide Feedback</span></span>


<span data-ttu-id="02bab-114">Wir sind an Ihrem Feedback zu MBAM interessiert.</span><span class="sxs-lookup"><span data-stu-id="02bab-114">We are interested in your feedback on MBAM.</span></span> <span data-ttu-id="02bab-115">Sie können Ihr Feedback an senden <mdopdocs@microsoft.com> .</span><span class="sxs-lookup"><span data-stu-id="02bab-115">You can send your feedback to <mdopdocs@microsoft.com>.</span></span>

<span data-ttu-id="02bab-116">**Hinweis**  Diese e-Mail-Adresse ist kein Supportkanal, aber Ihr Feedback wird uns helfen, zukünftige Änderungen in unseren Dokumentations-und Produktversionen zu planen.</span><span class="sxs-lookup"><span data-stu-id="02bab-116">**Note** This email address is not a support channel, but your feedback will help us to plan for future changes in our documentation and product releases.</span></span>

 

<span data-ttu-id="02bab-117">Die neuesten Informationen zu MDOP und weiteren Lernressourcen finden Sie auf der Seite [MDOP-Informationen](https://go.microsoft.com/fwlink/p/?LinkId=236032) .</span><span class="sxs-lookup"><span data-stu-id="02bab-117">For the latest information about MDOP and additional learning resources, see the [MDOP Information Experience](https://go.microsoft.com/fwlink/p/?LinkId=236032) page.</span></span>

<span data-ttu-id="02bab-118">Wenn Sie weitere Informationen zu neuen Updates oder Feedback geben möchten, folgen Sie uns auf [Facebook](https://go.microsoft.com/fwlink/p/?LinkId=242445) oder [Twitter](https://go.microsoft.com/fwlink/p/?LinkId=242447).</span><span class="sxs-lookup"><span data-stu-id="02bab-118">For more information about new updates or to provide feedback, follow us on [Facebook](https://go.microsoft.com/fwlink/p/?LinkId=242445) or [Twitter](https://go.microsoft.com/fwlink/p/?LinkId=242447).</span></span>

## <span data-ttu-id="02bab-119">Bekannte Probleme mit MBAM 1,0</span><span class="sxs-lookup"><span data-stu-id="02bab-119">Known Issues with MBAM 1.0</span></span>


<span data-ttu-id="02bab-120">Dieser Abschnitt enthält Versionshinweise zu den bekannten Problemen bei der Einrichtung und Installation von MBAM.</span><span class="sxs-lookup"><span data-stu-id="02bab-120">This section contains release notes about the known issues with MBAM setup and installation.</span></span>

### <a href="" id="if-you-select-the--use-a-certificate-to-encrypt-the-network-communication--option-during-setup--existing-database-connections-and-dependent-applications-can-stop-functioning-"></a><span data-ttu-id="02bab-121">Wenn Sie während des Setups die Option "Zertifikat zum Verschlüsseln der Netzwerkkommunikation verwenden" auswählen, können vorhandene Datenbankverbindungen und abhängige Anwendungen nicht mehr funktionieren.</span><span class="sxs-lookup"><span data-stu-id="02bab-121">If you select the “Use a certificate to encrypt the network communication” option during Setup, existing database connections and dependent applications can stop functioning</span></span>

<span data-ttu-id="02bab-122">Sie können MBAM für eine **verschlüsselte Netzwerkkommunikation** konfigurieren, nachdem Sie die Wiederherstellungs-und Hardware Datenbank oder die Kompatibilitäts Status-Datenbankfeatures installiert haben.</span><span class="sxs-lookup"><span data-stu-id="02bab-122">You can configure MBAM for **Encrypted network communication** after you install either the Recovery and Hardware Database or the Compliance Status Database features.</span></span> <span data-ttu-id="02bab-123">Wenn Sie MBAM für die verschlüsselte Netzwerkkommunikation konfigurieren, konfiguriert MBAM Setup die Instanz von SQL Server-Datenbankmodul für die Verwendung von Secure Sockets Layer (SSL) für die Kommunikation zwischen der betreffenden Datenbank und dem Verwaltungs-und Überwachungsserver sowie den Funktionen für Compliance-und Überwachungsberichts Server.</span><span class="sxs-lookup"><span data-stu-id="02bab-123">If you choose to configure MBAM for Encrypted network communication, MBAM Setup configures the instance of the SQL Server Database Engine to use Secure Sockets Layer (SSL) for communication between the applicable database and both the Administration and Monitoring Server and the Compliance and Audit Report Server features.</span></span>

-   <span data-ttu-id="02bab-124">Wenn die Instanz des SQL Server-Datenbankmoduls noch nicht für die Verwendung von SSL konfiguriert ist, wird Sie von MBAM Setup so konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="02bab-124">If the instance of the SQL Server Database Engine is not already configured to use SSL, MBAM Setup configures it to do so.</span></span> <span data-ttu-id="02bab-125">Dadurch kann verhindert werden, dass Anwendungen, die versuchen, nicht MBAM-Datenbanken auf der Instanz von SQL Server-Datenbankmodul zu verwenden, die Kommunikation mit ihren Datenbanken verhindern.</span><span class="sxs-lookup"><span data-stu-id="02bab-125">This can prevent applications that try to use non-MBAM databases on the instance of the SQL Server Database Engine from communicating with their databases.</span></span>

-   <span data-ttu-id="02bab-126">Wenn die Instanz des SQL Server-Datenbankmoduls bereits für die Verwendung von SSL konfiguriert ist, ist Sie für die Verwendung des Zertifikats konfiguriert, das der Benutzer während der Installation ausgewählt hat.</span><span class="sxs-lookup"><span data-stu-id="02bab-126">If the instance of the SQL Server Database Engine is already configured to use SSL, it is configured to use the certificate that the user selected during setup.</span></span> <span data-ttu-id="02bab-127">Wenn sich dieses Zertifikat von dem bereits verwendeten unterscheidet, kann es verhindern, dass Anwendungen, die SQL Server-Datenbanken auf der Instanz des SQL Server-Datenbankmoduls verwenden, ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="02bab-127">If this certificate differs from the one that was already in use, it can prevent applications that use SQL Server databases on the instance of the SQL Server Database Engine from running.</span></span>

<span data-ttu-id="02bab-128">**Problemumgehung:** Keine</span><span class="sxs-lookup"><span data-stu-id="02bab-128">**WORKAROUND:** None</span></span>

### <span data-ttu-id="02bab-129">MBAM-Setup schlägt während der Installation fehl, wenn Sie ein lokales Administrator Konto verwenden</span><span class="sxs-lookup"><span data-stu-id="02bab-129">MBAM Setup fails during installation when you use a local Administrator account</span></span>

<span data-ttu-id="02bab-130">MBAM-Setup schlägt fehl, wenn Sie ein lokales Administrator Konto verwenden.</span><span class="sxs-lookup"><span data-stu-id="02bab-130">MBAM Setup fails when you use a local Administrator account.</span></span> <span data-ttu-id="02bab-131">Die Protokolldatei enthält die folgenden Informationen:</span><span class="sxs-lookup"><span data-stu-id="02bab-131">The log file contains the following information:</span></span>

``` syntax
Locating group 'MBAM Report Users'
Adding <GUID>' to group 'MBAM Report Users'
Locating group 'MBAM Recovery and Hardware DB Access'
Adding 'S-1-5-20' to group 'MBAM Recovery and Hardware DB Access'
Exception: A new member could not be added to a local group because the member has the wrong account type.
 
  StackTrace:    at System.DirectoryServices.AccountManagement.SAMStoreCtx.UpdateGroupMembership(Principal group, DirectoryEntry de, NetCred credentials, AuthenticationTypes authTypes)
   at System.DirectoryServices.AccountManagement.SDSUtils.ApplyChangesToDirectory(Principal p, StoreCtx storeCtx, GroupMembershipUpdater updateGroupMembership, NetCred credentials, AuthenticationTypes authTypes)
   at System.DirectoryServices.AccountManagement.SAMStoreCtx.Update(Principal p)
   at Microsoft.Windows.Mdop.BitlockerManagement.Setup.Groups.CreateGroupsDeferred(Session session)
  InnerException:Exception: A new member could not be added to a local group because the member has the wrong account type.
 
    InnerException:StackTrace:    at System.DirectoryServices.AccountManagement.UnsafeNativeMethods.IADsGroup.Add(String bstrNewItem)
   at System.DirectoryServices.AccountManagement.SAMStoreCtx.UpdateGroupMembership(Principal group, DirectoryEntry de, NetCred credentials, AuthenticationTypes authTypes)
CustomAction MbamCreateGroupsDeferred returned actual error code 1603 (note this may not be 100% accurate if translation happened inside sandbox)
Action ended 11:41:29: InstallExecute. Return value 3.
```

<span data-ttu-id="02bab-132">**Problemumgehung:** Verwenden Sie bei der Installation von MBAM ein Domänenkonto mit administrativen Anmeldeinformationen auf dem Server Computer.</span><span class="sxs-lookup"><span data-stu-id="02bab-132">**WORKAROUND:** Use a domain account with administrative credentials on the server computer when you install MBAM.</span></span>

### <span data-ttu-id="02bab-133">MBAM-Setup konfiguriert die Instanz von SQL Server-Datenbankmodul neu, um SSL nicht zu verwenden, wenn Sie "Netzwerkkommunikation nicht verschlüsseln" auswählen.</span><span class="sxs-lookup"><span data-stu-id="02bab-133">MBAM Setup reconfigures the instance of the SQL Server Database Engine to not use SSL if you select “Do not encrypt network communication”</span></span>

<span data-ttu-id="02bab-134">Wenn Sie entweder die Wiederherstellungs-und Hardware Datenbank oder die Kompatibilitäts Status Datenbank installieren, können Sie mithilfe von Setup MBAM konfigurieren, indem Sie die **verschlüsselte Netzwerkkommunikation**auswählen.</span><span class="sxs-lookup"><span data-stu-id="02bab-134">When you install either the Recovery and Hardware Database or the Compliance Status Database, you can use Setup to configure MBAM by selecting **Encrypted network communication**.</span></span> <span data-ttu-id="02bab-135">Wenn Sie sich entschließen, die Netzwerkkommunikation zu verschlüsseln, konfiguriert MBAM Setup die Instanz von SQL Server-Datenbankmodul neu, sodass SSL nicht verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="02bab-135">If you decide not to encrypt the network communication, MBAM Setup reconfigures the instance of the SQL Server Database Engine so that it does not use SSL.</span></span>

-   <span data-ttu-id="02bab-136">Wenn die Instanz des SQL Server-Datenbankmoduls bereits für die Verwendung von SSL konfiguriert ist, deaktiviert das MBAM-Setup SSL für die Instanz des SQL Server-Datenbankmoduls.</span><span class="sxs-lookup"><span data-stu-id="02bab-136">If the instance of the SQL Server Database Engine is already configured to use SSL, MBAM Setup disables SSL on the instance of the SQL Server Database Engine.</span></span> <span data-ttu-id="02bab-137">Dadurch wird die Kommunikationssicherheit zwischen den Anwendungen geändert, die Datenbanken verwenden, die nicht mit MBAM-Datenbanken in der Instanz von SQL Server-Datenbankmodul verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="02bab-137">This changes the communication security between the applications that use databases that are not related to MBAM databases on the instance of the SQL Server Database Engine.</span></span>

<span data-ttu-id="02bab-138">**Problemumgehung:** Keine</span><span class="sxs-lookup"><span data-stu-id="02bab-138">**WORKAROUND:** None</span></span>

### <span data-ttu-id="02bab-139">Fehlende Voraussetzung für die Internetinformationsdienste (IIS)-Verwaltungsskripts und Tools-Webserver Feature</span><span class="sxs-lookup"><span data-stu-id="02bab-139">Missing prerequisite for the Internet Information Services (IIS) Management Scripts and Tools web server feature</span></span>

<span data-ttu-id="02bab-140">MBAM-Setup ist vom IIS-Verwaltungsskripts und Tools-Webserver Feature abhängig, ist aber keine erzwungene Voraussetzung.</span><span class="sxs-lookup"><span data-stu-id="02bab-140">MBAM Setup is dependent on the IIS Management Scripts and Tools web server feature, but it is not an enforced prerequisite.</span></span> <span data-ttu-id="02bab-141">Mit dem Server-Setup können Sie MBAM installieren, wenn dieses Feature nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="02bab-141">Server setup lets you install MBAM when this feature is missing.</span></span> <span data-ttu-id="02bab-142">Dies führt jedoch dazu, dass der VSS-Writer des Sicherungsdiensts MBAM gestartet und dann beendet wird, da er nicht die Windows-Verwaltungsinstrumentation (WMI) und den Internet Informationsdienste (IIS)-Anbieter finden kann.</span><span class="sxs-lookup"><span data-stu-id="02bab-142">However, this will cause the backup service MBAM VSS Writer to start and then stop, because it cannot locate the Windows Management Instrumentation (WMI) and the Internet Information Services (IIS) provider.</span></span> <span data-ttu-id="02bab-143">Es ist keine Fehlermeldung für diese Bedingung vorhanden, es sei denn, dies geschieht im Ereignisprotokoll.</span><span class="sxs-lookup"><span data-stu-id="02bab-143">There is no error message for this condition, except that which occurs in the event log.</span></span> <span data-ttu-id="02bab-144">Die Installation von MBAM ohne IIS-Verwaltungsskripts und-Tools führt dazu, dass die Sicherungsvorgänge nicht für MBAM ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="02bab-144">Installation of MBAM without IIS Management Scripts and Tools causes the backup operations not to run for MBAM.</span></span>

<span data-ttu-id="02bab-145">**Problemumgehung:** Stellen Sie sicher, dass das Feature IIS-Verwaltungsskripts und Tools-Webserver installiert ist, bevor Sie das MBAM-Setup starten.</span><span class="sxs-lookup"><span data-stu-id="02bab-145">**WORKAROUND:** Ensure that the IIS Management Scripts and Tools web server feature is installed before you start the MBAM Setup.</span></span>

### <a href="" id="mbam-setup-stops-responding-during-the--installing-selected-features--phase-when-setup-is-configured-to-use-a-certificate"></a><span data-ttu-id="02bab-146">MBAM-Setup reagiert nicht mehr während der Phase "ausgewählte Features installieren", wenn Setup für die Verwendung eines Zertifikats konfiguriert ist</span><span class="sxs-lookup"><span data-stu-id="02bab-146">MBAM Setup stops responding during the “Installing selected features” phase when setup is configured to use a certificate</span></span>

<span data-ttu-id="02bab-147">MBAM-Setup reagiert während der **Installation der ausgewählten Features** -Phase des Setups nicht mehr.</span><span class="sxs-lookup"><span data-stu-id="02bab-147">MBAM Setup stops responding during the **Installing selected features** phase of setup.</span></span> <span data-ttu-id="02bab-148">Dies tritt während der Installation der Wiederherstellungs-und Hardware Datenbank oder der Kompatibilitäts Status Datenbank auf, nachdem Sie die Option **Zertifikat zum Verschlüsseln der Netzwerkkommunikation verwenden** ausgewählt haben.</span><span class="sxs-lookup"><span data-stu-id="02bab-148">This occurs during the installation of the Recovery and Hardware Database or the Compliance Status Database, after you select the **Use a certificate to encrypt the network communication** option.</span></span> <span data-ttu-id="02bab-149">Darüber hinaus reagiert das MBAM-Setup nicht mehr, wenn die Instanz des SQL Server-Datenbankmoduls nicht auf das Zertifikat zugreifen kann, das während des Setups angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="02bab-149">Furthermore, the MBAM Setup stops responding if the instance of the SQL Server Database Engine cannot access the certificate that was specified during setup.</span></span>

<span data-ttu-id="02bab-150">**Problemumgehung:** Aktualisieren Sie die Berechtigungen für das Zertifikat, damit der Windows-Dienst für die anwendbare Instanz von SQL Server-Datenbankmodul auf das Zertifikat zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="02bab-150">**WORKAROUND:** Update the permissions on the certificate, so that the Windows service for the applicable instance of the SQL Server Database Engine can access the certificate.</span></span> <span data-ttu-id="02bab-151">Sie können auch das Konto ändern, unter dem die Instanz des SQL Server-Datenbankmoduls ausgeführt wird, damit Datenbankmodul das Zertifikat verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="02bab-151">You can also change the account under which the instance of the SQL Server Database Engine runs, for the database engine to use the certificate.</span></span> <span data-ttu-id="02bab-152">Wenn Sie die Berechtigungen für das Zertifikat ermitteln möchten, geben Sie an der Eingabeaufforderung den folgenden Befehl ein: **certutil-v-Store My**</span><span class="sxs-lookup"><span data-stu-id="02bab-152">To determine the permissions for the certificate, type the following command at the command prompt: **certutil -v -store MY**</span></span>

### <span data-ttu-id="02bab-153">MBAM-Setup wird angehalten, wenn Sie SQL Server Reporting Services installieren</span><span class="sxs-lookup"><span data-stu-id="02bab-153">MBAM Setup pauses when you install SQL Server Reporting Services</span></span>

<span data-ttu-id="02bab-154">Wenn Sie während der MBAM-Installation eine Instanz von SQL Server Reporting Services (SSRS) auswählen und die SSRS-Instanz nicht verfügbar oder falsch konfiguriert ist, wird das MBAM-Setup möglicherweise bis zu einer Minute angehalten, während es versucht, mit der SSRS-Instanz zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="02bab-154">During MBAM installation, when you select an instance of SQL Server Reporting Services (SSRS) and SSRS instance is not available or it is configured incorrectly, the MBAM Setup might pause for up to one minute while it attempts to communicate with the SSRS instance.</span></span>

<span data-ttu-id="02bab-155">**Problemumgehung:** Warten Sie mindestens eine Minute, bis das MBAM-Setup fortgesetzt wird, während das Setup-Programm versucht, sich mit der Instanz von SSRS in Verbindung zu setzen.</span><span class="sxs-lookup"><span data-stu-id="02bab-155">**WORKAROUND:** Wait for at least one minute for MBAM Setup to resume while the Setup program attempts to contact the instance of SSRS.</span></span>

### <a href="" id="administration-and-monitoring-server-does-not-run-after-setup-"></a><span data-ttu-id="02bab-156">Der Administrations-und Überwachungs Server wird nach dem Setup nicht ausgeführt</span><span class="sxs-lookup"><span data-stu-id="02bab-156">Administration and Monitoring Server does not run after setup</span></span>

<span data-ttu-id="02bab-157">Nachdem das MBAM-Setup die Verwaltungs-und Überwachungs Server Funktion erfolgreich installiert hat, zeigt MBAM Fehlermeldungen an, wenn Sie versuchen, auf die MBAM-Administratorwebsite zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="02bab-157">After MBAM Setup successfully installs the Administration and Monitoring Server feature, MBAM displays error messages when you try to access the MBAM administrator website.</span></span> <span data-ttu-id="02bab-158">Dieses Problem tritt aus einem der folgenden Gründe auf:</span><span class="sxs-lookup"><span data-stu-id="02bab-158">This issue occurs for one of the following reasons:</span></span>

-   <span data-ttu-id="02bab-159">Eine oder mehrere Voraussetzungen für den Verwaltungs-und Überwachungs Server wurden nach der MBAM-Installation entfernt.</span><span class="sxs-lookup"><span data-stu-id="02bab-159">One or more prerequisites on the Administration and Monitoring Server were removed after the MBAM installation.</span></span>

-   <span data-ttu-id="02bab-160">Eine oder mehrere Voraussetzungen wurden auf dem Server installiert, und später wurden Sie entfernt, bevor Sie das MBAM-Setup ausführen.</span><span class="sxs-lookup"><span data-stu-id="02bab-160">One or more prerequisites were installed on the server and later they were removed before running the MBAM Setup.</span></span>

<span data-ttu-id="02bab-161">**Problemumgehung:** Überprüfen Sie die MBAM-Dokumentation, und stellen Sie sicher, dass alle MBAM-Voraussetzungen installiert sind.</span><span class="sxs-lookup"><span data-stu-id="02bab-161">**WORKAROUND:** Review the MBAM documentation and confirm that all MBAM prerequisites are installed.</span></span>

### <span data-ttu-id="02bab-162">Wenn Sie während des Setups auf "Dokumentations Verknüpfungen" klicken, wird nach Abschluss des Setups ein Anwendungsfehler angezeigt</span><span class="sxs-lookup"><span data-stu-id="02bab-162">Clicking documentation links during Setup results in an application error after Setup is finished</span></span>

<span data-ttu-id="02bab-163">Wenn Sie während des Setups auf einen Link zur Dokumentation klicken und dann das Setup-Programm schließen, indem Sie auf **Abbrechen** oder **Fertig stellen** klicken, nachdem das Setup erfolgreich abgeschlossen wurde, wird eine Fehlermeldung mit der Anwendung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="02bab-163">When you click a documentation link during setup and then close the Setup program by clicking **Cancel** or **Finish** after Setup has successfully finished, an application error message appears..</span></span> <span data-ttu-id="02bab-164">Das Problem wird durch einen Zugriffsverletzungsfehler im Windows-Aufgabenplaner verursacht.</span><span class="sxs-lookup"><span data-stu-id="02bab-164">The problem is caused by an access violation error in the Windows Task Scheduler.</span></span>

<span data-ttu-id="02bab-165">**Problemumgehung:** Keine.</span><span class="sxs-lookup"><span data-stu-id="02bab-165">**WORKAROUND:** None.</span></span> <span data-ttu-id="02bab-166">Sie können diesen Fehler ignorieren.</span><span class="sxs-lookup"><span data-stu-id="02bab-166">You can ignore this error.</span></span>

### <span data-ttu-id="02bab-167">Fehler MBAM-Setup entfernt keine neuen Datenbanken</span><span class="sxs-lookup"><span data-stu-id="02bab-167">Failed MBAM Setup does not remove new databases</span></span>

<span data-ttu-id="02bab-168">Wenn das MBAM-Setup fehlschlägt, entfernt Setup die neu erstellten Datenbanken möglicherweise nicht.</span><span class="sxs-lookup"><span data-stu-id="02bab-168">If the MBAM Setup fails, Setup might not remove the newly created databases.</span></span> <span data-ttu-id="02bab-169">Dies kann bei nachfolgenden Installationen zu Fehlern führen.</span><span class="sxs-lookup"><span data-stu-id="02bab-169">This can cause failures during subsequent installations.</span></span>

<span data-ttu-id="02bab-170">**Problemumgehung:** Wählen Sie bei der nachfolgenden Installation einen anderen Namen für die Datenbankinstanz aus.</span><span class="sxs-lookup"><span data-stu-id="02bab-170">**WORKAROUND:** Choose a different name for the database instance during the subsequent installation.</span></span>

### <span data-ttu-id="02bab-171">MBAM-Setup erkennt keine gültigen Netzwerklastenausgleich-Cluster Zertifikate</span><span class="sxs-lookup"><span data-stu-id="02bab-171">MBAM Setup does not recognize valid network load-balancing cluster certificates</span></span>

<span data-ttu-id="02bab-172">Während der Installation von MBAM Administration and Monitoring Server wird das Cluster Zertifikat bei Auswahl der Option Netzwerk Verschlüsselung nicht als gültiges Zertifikat erkannt.</span><span class="sxs-lookup"><span data-stu-id="02bab-172">During the MBAM Administration and Monitoring Server installation, with the network encryption option selected, the cluster certificate is not recognized as a valid certificate.</span></span> <span data-ttu-id="02bab-173">Sie wird als gültig erkannt, wenn das Zertifikat für die Kommunikation mit der Datenbank installiert ist, aber für die Kommunikation durch den Lastenausgleichscluster abgelehnt wurde.</span><span class="sxs-lookup"><span data-stu-id="02bab-173">It is recognized as valid when the certificate for communication with the database is installed, but it is rejected for communication by the load-balancing cluster.</span></span>

<span data-ttu-id="02bab-174">**Problemumgehung:** Überprüfen Sie, ob die dem Zertifikat zugeordnete Zertifikatsperrliste (Certificate Revocation List, CRL) barrierefrei ist, oder verwenden Sie ein Zertifikat, das keine Validierung mithilfe der CRL erfordert.</span><span class="sxs-lookup"><span data-stu-id="02bab-174">**WORKAROUND:** Confirm that the certificate revocation list (CRL) associated with the certificate is accessible, or use a certificate that does not require validation by using the CRL.</span></span>

## <span data-ttu-id="02bab-175">Anmerkungen zu dieser Version Copyright-Informationen</span><span class="sxs-lookup"><span data-stu-id="02bab-175">Release Notes Copyright Information</span></span>


<span data-ttu-id="02bab-176">Microsoft, Active Directory, ActiveX, Bing, Excel, Silverlight, SQLServer, Windows, MicrosoftIntune und WindowsPowerShell sind Marken der Microsoft-Unternehmensgruppe.</span><span class="sxs-lookup"><span data-stu-id="02bab-176">Microsoft, Active Directory, ActiveX, Bing, Excel, Silverlight, SQLServer, Windows, MicrosoftIntune, and WindowsPowerShell are trademarks of the Microsoft group of companies.</span></span> <span data-ttu-id="02bab-177">Alle anderen Marken sind Eigentum ihrer jeweiligen Eigentümer.</span><span class="sxs-lookup"><span data-stu-id="02bab-177">All other trademarks are property of their respective owners.</span></span>



## <span data-ttu-id="02bab-178">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="02bab-178">Related topics</span></span>


[<span data-ttu-id="02bab-179">Informationen zu MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="02bab-179">About MBAM 1.0</span></span>](about-mbam-10.md)

 

 





