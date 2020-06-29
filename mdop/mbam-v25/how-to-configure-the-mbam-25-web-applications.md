---
title: So konfigurieren Sie die MBAM 2.5-Webanwendungen
description: So konfigurieren Sie die MBAM 2.5-Webanwendungen
author: dansimp
ms.assetid: 909bf2d3-028c-4ac1-9247-171532a1eeae
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0336d24f51167a00c8565ccd081f4bc5dfb2c4cd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810591"
---
# <span data-ttu-id="30100-103">So konfigurieren Sie die MBAM 2.5-Webanwendungen</span><span class="sxs-lookup"><span data-stu-id="30100-103">How to Configure the MBAM 2.5 Web Applications</span></span>


<span data-ttu-id="30100-104">In diesem Thema wird erläutert, wie Sie die 2,5-Webanwendungen für Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) für die empfohlene [allgemeine Architektur für MBAM 2,5](high-level-architecture-for-mbam-25.md) mithilfe einer der folgenden Methoden konfigurieren:</span><span class="sxs-lookup"><span data-stu-id="30100-104">This topic explains how to configure the Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 web applications for the recommended [High-Level Architecture for MBAM 2.5](high-level-architecture-for-mbam-25.md) by using one of the following methods:</span></span>

-   <span data-ttu-id="30100-105">Ein Windows PowerShell-Cmdlet</span><span class="sxs-lookup"><span data-stu-id="30100-105">A Windows PowerShell cmdlet</span></span>

-   <span data-ttu-id="30100-106">Der Serverkonfigurations-Assistent von MBAM</span><span class="sxs-lookup"><span data-stu-id="30100-106">The MBAM Server Configuration wizard</span></span>

<span data-ttu-id="30100-107">Die Web-Anwendungen umfassen die folgenden Websites und die entsprechenden Webdienste:</span><span class="sxs-lookup"><span data-stu-id="30100-107">The web applications comprise the following websites and their corresponding web services:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="30100-108">Webseite</span><span class="sxs-lookup"><span data-stu-id="30100-108">Website</span></span></th>
<th align="left"><span data-ttu-id="30100-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="30100-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="30100-110">Website "Verwaltung und Überwachung"</span><span class="sxs-lookup"><span data-stu-id="30100-110">Administration and Monitoring Website</span></span></p></td>
<td align="left"><p><span data-ttu-id="30100-111">Website, auf der angegebene Benutzer Berichte anzeigen und Endbenutzern helfen können, ihre Computer wiederherzustellen, wenn Sie Ihre PIN oder Ihr Kennwort vergessen</span><span class="sxs-lookup"><span data-stu-id="30100-111">Website where specified users can view reports and help end users recover their computers when they forget their PIN or password</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="30100-112">Self-Service-Portal</span><span class="sxs-lookup"><span data-stu-id="30100-112">Self-Service Portal</span></span></p></td>
<td align="left"><p><span data-ttu-id="30100-113">Website, auf die Endbenutzer zugreifen können, um den Zugriff auf Ihre Computer unabhängig voneinander wiederherzustellen, wenn Sie Ihre PIN oder Ihr Kennwort vergessen</span><span class="sxs-lookup"><span data-stu-id="30100-113">Website that end users can access to independently regain access to their computers if they forget their PIN or password</span></span></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="30100-114">Bevor Sie die Konfiguration starten:</span><span class="sxs-lookup"><span data-stu-id="30100-114">Before you start the configuration:</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="30100-115">Schritt</span><span class="sxs-lookup"><span data-stu-id="30100-115">Step</span></span></th>
<th align="left"><span data-ttu-id="30100-116">Wo erhalte ich Anweisungen?</span><span class="sxs-lookup"><span data-stu-id="30100-116">Where to get instructions</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="30100-117">Überprüfen Sie die empfohlene Architektur für MBAM.</span><span class="sxs-lookup"><span data-stu-id="30100-117">Review the recommended architecture for MBAM.</span></span></p></td>
<td align="left"><p><a href="high-level-architecture-for-mbam-25.md" data-raw-source="[High-Level Architecture for MBAM 2.5](high-level-architecture-for-mbam-25.md)"><span data-ttu-id="30100-118">High-Level-Architektur für MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="30100-118">High-Level Architecture for MBAM 2.5</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="30100-119">Überprüfen Sie die unterstützten Konfigurationen für MBAM.</span><span class="sxs-lookup"><span data-stu-id="30100-119">Review the supported configurations for MBAM.</span></span></p></td>
<td align="left"><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)"><span data-ttu-id="30100-120">Von MBAM 2.5 unterstützte Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="30100-120">MBAM 2.5 Supported Configurations</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="30100-121">Führen Sie die erforderlichen Voraussetzungen für jeden Server aus.</span><span class="sxs-lookup"><span data-stu-id="30100-121">Complete the required prerequisites on each server.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="30100-122">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="30100-122">Note</span></span></strong><br/><p><span data-ttu-id="30100-123">Stellen Sie sicher, dass Sie die SQL-ServerReporting-Dienste (SSRS) so konfigurieren, dass Sie die Secure Sockets Layer (SSL) verwenden, bevor Sie die Website Verwaltung und Überwachung konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="30100-123">Ensure that you configure SQL ServerReporting Services (SSRS) to use the Secure Sockets Layer (SSL) before you configure the Administration and Monitoring Website.</span></span> <span data-ttu-id="30100-124">Andernfalls verwendet das Feature Berichte http statt HTTPS.</span><span class="sxs-lookup"><span data-stu-id="30100-124">Otherwise, the Reports feature will use HTTP instead of HTTPS.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><ul>
<li><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)"><span data-ttu-id="30100-125">MBAM 2.5-Servervoraussetzungen für eigenständige und Configuration Manager-Integrationstopologien</span><span class="sxs-lookup"><span data-stu-id="30100-125">MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies</span></span></a></p></li>
<li><p><a href="mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md" data-raw-source="[MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md)"><span data-ttu-id="30100-126">MBAM 2,5-Server Voraussetzungen, die nur für die Configuration Manager-Integrations Topologie gelten </a> (falls zutreffend)</span><span class="sxs-lookup"><span data-stu-id="30100-126">MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology</a> (if applicable)</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="30100-127">Registrieren Sie Dienstprinzipalnamen (SPN) für das Anwendungspoolkonto für die Websites.</span><span class="sxs-lookup"><span data-stu-id="30100-127">Register service principal names (SPNs) for the application pool account for the websites.</span></span> <span data-ttu-id="30100-128">Sie müssen diesen Schritt nur ausführen, wenn Sie in den Active Directory-Domänendiensten (AD DS) nicht über administrative Domänenrechte verfügen.</span><span class="sxs-lookup"><span data-stu-id="30100-128">You need to do this step only if you do not have administrative domain rights in Active Directory Domain Services (AD DS).</span></span> <span data-ttu-id="30100-129">Wenn Sie über diese Rechte in AD DS verfügen, erstellt MBAM die SPNs für Sie.</span><span class="sxs-lookup"><span data-stu-id="30100-129">If you do have these rights in AD DS, MBAM will create the SPNs for you.</span></span></p></td>
<td align="left"><p><a href="planning-how-to-secure-the-mbam-websites.md#bkmk-regvirtualspn" data-raw-source="[Planning How to Secure the MBAM Websites](planning-how-to-secure-the-mbam-websites.md#bkmk-regvirtualspn)"><span data-ttu-id="30100-130">Planen der Sicherung von MBAM-Websites</span><span class="sxs-lookup"><span data-stu-id="30100-130">Planning How to Secure the MBAM Websites</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="30100-131">Installieren Sie die MBAM-Server Software auf jedem Server, auf dem Sie ein MBAM-Server Feature konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="30100-131">Install the MBAM Server software on each server where you will configure an MBAM Server feature.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="30100-132">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="30100-132">Note</span></span></strong><br/><p><span data-ttu-id="30100-133">Wenn Sie beabsichtigen, die Websites auf einem Server und die Webdienste auf einem anderen Server zu installieren, können Sie diese nur mithilfe des <strong> Windows PowerShell-Cmdlets Enable-MbamWebApplication konfigurieren </strong> .</span><span class="sxs-lookup"><span data-stu-id="30100-133">If you plan to install the websites on one server and the web services on another, you will be able to configure them only by using the <strong>Enable-MbamWebApplication</strong> Windows PowerShell cmdlet.</span></span> <span data-ttu-id="30100-134">Der MBAM-Serverkonfigurations-Assistent unterstützt keine Konfiguration dieser Elemente auf separaten Servern.</span><span class="sxs-lookup"><span data-stu-id="30100-134">The MBAM Server Configuration wizard does not support configuring these items on separate servers.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><a href="installing-the-mbam-25-server-software.md" data-raw-source="[Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md)"><span data-ttu-id="30100-135">Installieren der MBAM 2.5-Serversoftware</span><span class="sxs-lookup"><span data-stu-id="30100-135">Installing the MBAM 2.5 Server Software</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="30100-136">Überprüfen Sie die Voraussetzungen für die Verwendung von Windows PowerShell, wenn Sie beabsichtigen, Cmdlets zum Konfigurieren der MBAM-Server Features zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="30100-136">Review the prerequisites for using Windows PowerShell if you plan to use cmdlets to configure MBAM Server features.</span></span></p></td>
<td align="left"><p><a href="configuring-mbam-25-server-features-by-using-windows-powershell.md" data-raw-source="[Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)"><span data-ttu-id="30100-137">Konfigurieren von MBAM 2.5 Serverfunktionen mithilfe von Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="30100-137">Configuring MBAM 2.5 Server Features by Using Windows PowerShell</span></span></a></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="30100-138">So konfigurieren Sie die Webanwendungen mithilfe von Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="30100-138">To configure the web applications by using Windows PowerShell</span></span>**

1.  <span data-ttu-id="30100-139">Bevor Sie die Konfiguration starten, lesen Sie [Konfigurieren von MBAM 2,5-Server Features mithilfe von Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md) zum Überprüfen der Voraussetzungen für die Verwendung von Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="30100-139">Before you start the configuration, see [Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md) to review the prerequisites for using Windows PowerShell.</span></span>

2.  <span data-ttu-id="30100-140">Verwenden Sie das Cmdlet **enable-MbamWebApplication** , um die Webanwendungen mithilfe von Windows PowerShell zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="30100-140">Use the **Enable-MbamWebApplication** cmdlet to configure the web applications using Windows PowerShell.</span></span> <span data-ttu-id="30100-141">Um Informationen zu diesem Cmdlet abzurufen, geben **Sie Get-Help enable-MbamWebApplication**ein.</span><span class="sxs-lookup"><span data-stu-id="30100-141">To get information about this cmdlet, type **Get-Help Enable-MbamWebApplication**.</span></span>

**<span data-ttu-id="30100-142">So konfigurieren Sie die Einstellungen für alle Webanwendungen mithilfe des Assistenten</span><span class="sxs-lookup"><span data-stu-id="30100-142">To configure the settings for all web applications using the wizard</span></span>**

1. <span data-ttu-id="30100-143">Starten Sie auf dem Server, auf dem Sie die Webanwendungen konfigurieren möchten, den MBAM-Serverkonfigurations-Assistenten.</span><span class="sxs-lookup"><span data-stu-id="30100-143">On the server where you want to configure the web applications, start the MBAM Server Configuration wizard.</span></span> <span data-ttu-id="30100-144">Sie können **MBAM Server Configuration** im **Startmenü** auswählen, um den Assistenten zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="30100-144">You can select **MBAM Server Configuration** from the **Start** menu to open the wizard.</span></span>

2. <span data-ttu-id="30100-145">Klicken Sie auf **neue Features hinzufügen**, wählen Sie Website und **Self-Service-Portal** **Verwalten und überwachen** aus, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="30100-145">Click **Add New Features**, select **Administration and Monitoring Website** and **Self-Service Portal**, and then click **Next**.</span></span> <span data-ttu-id="30100-146">Der Assistent überprüft, ob alle Voraussetzungen für die Webanwendungen erfüllt sind.</span><span class="sxs-lookup"><span data-stu-id="30100-146">The wizard checks that all prerequisites for the web applications have been met.</span></span>

3. <span data-ttu-id="30100-147">Wenn die Voraussetzungsprüfung erfolgreich ist, klicken Sie auf **weiter** , um fortzufahren.</span><span class="sxs-lookup"><span data-stu-id="30100-147">If the prerequisite check is successful, click **Next** to continue.</span></span> <span data-ttu-id="30100-148">Beheben Sie andernfalls alle fehlenden Voraussetzungen, und klicken Sie dann **erneut auf Voraussetzungen prüfen**.</span><span class="sxs-lookup"><span data-stu-id="30100-148">Otherwise, resolve any missing prerequisites, and then click **Check prerequisites again**.</span></span>

4. <span data-ttu-id="30100-149">Verwenden Sie die folgenden Beschreibungen, um die Feldwerte im Assistenten einzugeben.</span><span class="sxs-lookup"><span data-stu-id="30100-149">Use the following descriptions to enter the field values in the wizard.</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><strong><span data-ttu-id="30100-150">Feld</span><span class="sxs-lookup"><span data-stu-id="30100-150">Field</span></span></strong></th>
   <th align="left"><span data-ttu-id="30100-151">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="30100-151">Description</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="30100-152">Sicherheitszertifikat</span><span class="sxs-lookup"><span data-stu-id="30100-152">Security certificate</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="30100-153">Wählen Sie ein zuvor erstelltes Zertifikat aus, um die Kommunikation zwischen den Webdiensten und dem Server, auf dem Sie die Websites konfigurieren, optional zu verschlüsseln.</span><span class="sxs-lookup"><span data-stu-id="30100-153">Select a previously created certificate to optionally encrypt the communication between the web services and the server on which you are configuring the websites.</span></span> <span data-ttu-id="30100-154">Wenn Sie <strong> ein Zertifikat nicht verwenden auswählen </strong> , ist die Webkommunikation möglicherweise nicht sicher.</span><span class="sxs-lookup"><span data-stu-id="30100-154">If you choose <strong>Do not use a certificate</strong>, your web communication may not be secure.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="30100-155">Hostname</span><span class="sxs-lookup"><span data-stu-id="30100-155">Host name</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="30100-156">Name des Hostcomputers, auf dem Sie die Websites konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="30100-156">Name of the host computer where you are configuring the websites.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="30100-157">Installationspfad</span><span class="sxs-lookup"><span data-stu-id="30100-157">Installation path</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="30100-158">Pfad, in dem Sie die Websites installieren.</span><span class="sxs-lookup"><span data-stu-id="30100-158">Path where you are installing the websites.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="30100-159">Port</span><span class="sxs-lookup"><span data-stu-id="30100-159">Port</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="30100-160">Port Nummer, die für die Website-und Dienst Kommunikation verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="30100-160">Port number to use for website and service communication.</span></span></p>
   <div class="alert">
   <strong><span data-ttu-id="30100-161">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="30100-161">Note</span></span></strong><br/><p><span data-ttu-id="30100-162">Sie müssen eine Firewall-Ausnahme festlegen, um die Kommunikation über den angegebenen Port zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="30100-162">You must set a firewall exception to enable communication through the specified port.</span></span></p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="30100-163">Domänenkonto und Kennwort des Webdienst-Anwendungspools</span><span class="sxs-lookup"><span data-stu-id="30100-163">Web service application pool domain account and password</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="30100-164">Domänenbenutzerkonto und Kennwort für den Webdienst-Anwendungspool.</span><span class="sxs-lookup"><span data-stu-id="30100-164">Domain user account and password for the web service application pool.</span></span></p>
   <p><span data-ttu-id="30100-165">Wenn Sie einen Benutzernamen in das <strong> Feld Lese/Schreibzugriff-Domänenbenutzer oder-Gruppe </strong> auf der <strong> Seite Datenbanken konfigurieren eingeben </strong> , müssen Sie diesen Wert in dieses Feld eingeben.</span><span class="sxs-lookup"><span data-stu-id="30100-165">If you enter a user name in the <strong>Read/write access domain user or group</strong> field on the <strong>Configure Databases</strong> page, you must enter that same value in this field.</span></span></p>
   <p><span data-ttu-id="30100-166">Wenn Sie einen Gruppennamen in das <strong> Feld Lese-/Schreibzugriff-Domänenbenutzer oder-Gruppe </strong> auf der <strong> Seite Datenbanken konfigurieren eingeben </strong> , muss der in dieses Feld eingegebene Wert ein Mitglied dieser Gruppe sein.</span><span class="sxs-lookup"><span data-stu-id="30100-166">If you enter a group name in the <strong>Read/write access domain user or group</strong> field on the <strong>Configure Databases</strong> page, the value you enter in this field must be a member of that group.</span></span></p>
   <p><span data-ttu-id="30100-167">Wenn Sie keine Anmeldeinformationen angeben, werden die Anmeldeinformationen verwendet, die für eine zuvor aktivierte Webanwendung angegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="30100-167">If you do not specify credentials, the credentials that were specified for any previously enabled web application will be used.</span></span> <span data-ttu-id="30100-168">Alle Webanwendungen müssen die gleichen Anmeldeinformationen für den Anwendungspool verwenden.</span><span class="sxs-lookup"><span data-stu-id="30100-168">All web applications must use the same application pool credentials.</span></span> <span data-ttu-id="30100-169">Wenn Sie für verschiedene Webanwendungen unterschiedliche Anmeldeinformationen angeben, wird der zuletzt angegebene Wert verwendet.</span><span class="sxs-lookup"><span data-stu-id="30100-169">If you specify different credentials for different web applications, the most recently specified value will be used.</span></span></p>
   <div class="alert">
   <strong><span data-ttu-id="30100-170">Wichtig</span><span class="sxs-lookup"><span data-stu-id="30100-170">Important</span></span></strong><br/><p><span data-ttu-id="30100-171">Um die Sicherheit zu verbessern, legen Sie das in den Anmeldeinformationen angegebene Konto auf begrenzte Benutzerrechte fest.</span><span class="sxs-lookup"><span data-stu-id="30100-171">For improved security, set the account that is specified in the credentials to have limited user rights.</span></span> <span data-ttu-id="30100-172">Legen Sie außerdem das Kennwort des Kontos so ein, dass es nie abläuft.</span><span class="sxs-lookup"><span data-stu-id="30100-172">Also, set the password of the account to never expire.</span></span></p>
   </div>
   <div>

   </div></td>
   </tr>
   </tbody>
   </table>



5. <span data-ttu-id="30100-173">Überprüfen Sie, ob das integrierte IIS \ _IUSRS-Konto oder das Anwendungspoolkonto dem **Identitätswechsel zu einem Client nach der Authentifizierung** und den lokalen Sicherheitseinstellungen für das **Anmelden als Stapelverarbeitungsauftrag** hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="30100-173">Verify that the built-in IIS\_IUSRS account or the application pool account has been added to the **Impersonate a client after authentication** and the **Log on as a batch job** local security settings.</span></span>

   <span data-ttu-id="30100-174">Wenn Sie überprüfen möchten, ob Sie den lokalen Sicherheitseinstellungen hinzugefügt wurde, öffnen Sie den **lokalen Sicherheitsrichtlinien-Editor**, erweitern Sie den Knoten **lokale Richtlinien** , klicken Sie auf den Knoten **Benutzerrechtezuweisung** , und doppelklicken Sie auf **Identitätswechsel für einen Client nach Authentifizierung** , und **melden Sie sich als batchauftrags** Richtlinien im rechten Bereich an.</span><span class="sxs-lookup"><span data-stu-id="30100-174">To check whether it has been added to the local security settings, open the **Local Security Policy editor**, expand the **Local Policies** node, click the **User Rights Assignment** node, and double-click **Impersonate a client after authentication** and **Log on as a batch job** policies in the right pane.</span></span>

**<span data-ttu-id="30100-175">So konfigurieren Sie Verbindungsinformationen für die Datenbanken mithilfe des Assistenten</span><span class="sxs-lookup"><span data-stu-id="30100-175">To configure connection information for the databases by using the wizard</span></span>**

1.  <span data-ttu-id="30100-176">Verwenden Sie die folgenden Feldbeschreibungen, um die Verbindungsinformationen im Assistenten für die Konformitäts-und Überwachungsdatenbank zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="30100-176">Use the following field descriptions to configure the connection information in the wizard for the Compliance and Audit Database.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="30100-177">Feld</span><span class="sxs-lookup"><span data-stu-id="30100-177">Field</span></span></th>
    <th align="left"><span data-ttu-id="30100-178">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="30100-178">Description</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><strong><span data-ttu-id="30100-179">SQL Server-Name</span><span class="sxs-lookup"><span data-stu-id="30100-179">SQL Server name</span></span></strong></p></td>
    <td align="left"><p><span data-ttu-id="30100-180">Der Name des Servers, auf dem die Konformitäts-und Überwachungsdatenbank konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="30100-180">Name of the server where the Compliance and Audit Database is configured.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong><span data-ttu-id="30100-181">SQL Server-Datenbankinstanz</span><span class="sxs-lookup"><span data-stu-id="30100-181">SQL Server database instance</span></span></strong></p></td>
    <td align="left"><p><span data-ttu-id="30100-182">SQL Server-Instanzname, in dem die Konformitäts-und Überwachungsdatenbank konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="30100-182">SQL Server instance name where the Compliance and Audit Database is configured.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><strong><span data-ttu-id="30100-183">Datenbankname</span><span class="sxs-lookup"><span data-stu-id="30100-183">Database name</span></span></strong></p></td>
    <td align="left"><p><span data-ttu-id="30100-184">Der Name der Konformitäts-und Überwachungsdatenbank.</span><span class="sxs-lookup"><span data-stu-id="30100-184">Name of the Compliance and Audit Database.</span></span></p></td>
    </tr>
    </tbody>
    </table>



2.  <span data-ttu-id="30100-185">Verwenden Sie die folgenden Feldbeschreibungen, um die Verbindungsinformationen im Assistenten für die Wiederherstellungsdatenbank zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="30100-185">Use the following field descriptions to configure the connection information in the wizard for the Recovery Database.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="30100-186">Feld</span><span class="sxs-lookup"><span data-stu-id="30100-186">Field</span></span></th>
    <th align="left"><span data-ttu-id="30100-187">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="30100-187">Description</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><strong><span data-ttu-id="30100-188">SQL Server-Name</span><span class="sxs-lookup"><span data-stu-id="30100-188">SQL Server name</span></span></strong></p></td>
    <td align="left"><p><span data-ttu-id="30100-189">Der Name des Servers, auf dem die Wiederherstellungsdatenbank konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="30100-189">Name of the server where the Recovery Database is configured.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong><span data-ttu-id="30100-190">SQL Server-Datenbankinstanz</span><span class="sxs-lookup"><span data-stu-id="30100-190">SQL Server database instance</span></span></strong></p></td>
    <td align="left"><p><span data-ttu-id="30100-191">SQL Server-Instanzname, in dem die Wiederherstellungsdatenbank konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="30100-191">SQL Server instance name where the Recovery Database is configured.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><strong><span data-ttu-id="30100-192">Datenbankname</span><span class="sxs-lookup"><span data-stu-id="30100-192">Database name</span></span></strong></p></td>
    <td align="left"><p><span data-ttu-id="30100-193">Der Name der Wiederherstellungsdatenbank.</span><span class="sxs-lookup"><span data-stu-id="30100-193">Name of the Recovery Database.</span></span></p></td>
    </tr>
    </tbody>
    </table>



**<span data-ttu-id="30100-194">So konfigurieren Sie die Webanwendungen mithilfe des Assistenten</span><span class="sxs-lookup"><span data-stu-id="30100-194">To configure the web applications by using the wizard</span></span>**

1. <span data-ttu-id="30100-195">Verwenden Sie die folgenden Beschreibungen, um die Feldwerte im Assistenten einzugeben, um die Website "Verwaltung und Überwachung" zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="30100-195">Use the following descriptions to enter the field values in the wizard to configure the Administration and Monitoring Website.</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="30100-196">Feld</span><span class="sxs-lookup"><span data-stu-id="30100-196">Field</span></span></th>
   <th align="left"><span data-ttu-id="30100-197">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="30100-197">Description</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="30100-198">Erweiterte Helpdesk-Rollen Domänengruppe</span><span class="sxs-lookup"><span data-stu-id="30100-198">Advanced Helpdesk role domain group</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="30100-199">Domänenbenutzergruppe, deren Mitglieder Zugriff auf alle Bereiche der Verwaltungs-und Überwachungs Website haben, mit Ausnahme des Bereichs "Berichte".</span><span class="sxs-lookup"><span data-stu-id="30100-199">Domain user group whose members have access to all areas of the Administration and Monitoring Website except the Reports area.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="30100-200">Gruppe "Helpdesk Role Domain"</span><span class="sxs-lookup"><span data-stu-id="30100-200">Helpdesk role domain group</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="30100-201">Domänenbenutzergruppe, deren Mitglieder Zugriff auf die <strong> Bereiche "TPM verwalten" </strong> und " <strong> Laufwerk Wiederherstellung </strong> " der Website "Verwaltung und Überwachung" haben.</span><span class="sxs-lookup"><span data-stu-id="30100-201">Domain user group whose members have access to the <strong>Manage TPM</strong> and <strong>Drive Recovery</strong> areas of the Administration and Monitoring Website.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="30100-202">Verwenden der System Center Configuration Manager-Integration</span><span class="sxs-lookup"><span data-stu-id="30100-202">Use System Center Configuration Manager Integration</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="30100-203">Aktivieren Sie dieses Kontrollkästchen, wenn Sie MBAM mit der Configuration Manager-Integrations Topologie konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="30100-203">Select this check box if you are configuring MBAM with the Configuration Manager Integration topology.</span></span> <span data-ttu-id="30100-204">Wenn Sie dieses Kontrollkästchen aktivieren, werden alle Berichte, mit Ausnahme des Wiederherstellungs Überwachungsberichts, in Configuration Manager anstatt auf der Website Verwaltung und Überwachung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="30100-204">Selecting this check box makes all reports, except the Recovery Audit report, appear in Configuration Manager instead of in the Administration and Monitoring Website.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="30100-205">Gruppe "Berichtsrolle-Domäne"</span><span class="sxs-lookup"><span data-stu-id="30100-205">Reporting role domain group</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="30100-206">Domänenbenutzergruppe, deren Mitglieder schreibgeschützten Zugriff auf den Bereich "Berichte" der Website "Verwaltung und Überwachung" haben.</span><span class="sxs-lookup"><span data-stu-id="30100-206">Domain user group whose members have read-only access to the Reports area of the Administration and Monitoring Website.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="30100-207">SQL Server Reporting Services-URL</span><span class="sxs-lookup"><span data-stu-id="30100-207">SQL Server Reporting Services URL</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="30100-208">Die URL für den SSRS-Server, auf dem die MBAM-Berichte konfiguriert sind.</span><span class="sxs-lookup"><span data-stu-id="30100-208">URL for the SSRS server where the MBAM Reports are configured.</span></span></p>
   <p><span data-ttu-id="30100-209">Beispiele für Berichts-URLs:</span><span class="sxs-lookup"><span data-stu-id="30100-209">Examples of report URLs:</span></span></p>
   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="30100-210">Typ des Hostnamens</span><span class="sxs-lookup"><span data-stu-id="30100-210">Type of host name</span></span></th>
   <th align="left"><span data-ttu-id="30100-211">Beispiel</span><span class="sxs-lookup"><span data-stu-id="30100-211">Example</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="30100-212">Beispiel mit einem vollqualifizierten Domänennamen</span><span class="sxs-lookup"><span data-stu-id="30100-212">Example with a fully qualified domain name</span></span></p></td>
   <td align="left"><p><a href="https://MyReportServer.Contoso.com/ReportServer" data-raw-source="https://MyReportServer.Contoso.com/ReportServer">https://MyReportServer.Contoso.com/ReportServer</a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="30100-213">Beispiel mit einem benutzerdefinierten Hostnamen</span><span class="sxs-lookup"><span data-stu-id="30100-213">Example with a custom host name</span></span></p></td>
   <td align="left"><p><a href="https://MyReportServer/ReportServer" data-raw-source="https://MyReportServer/ReportServer">https://MyReportServer/ReportServer</a></p></td>
   </tr>
   </tbody>
   </table>
   <p> </p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="30100-214">Virtuelles Verzeichnis</span><span class="sxs-lookup"><span data-stu-id="30100-214">Virtual directory</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="30100-215">Virtuelles Verzeichnis der Verwaltungs-und Überwachungs Website.</span><span class="sxs-lookup"><span data-stu-id="30100-215">Virtual directory of the Administration and Monitoring Website.</span></span> <span data-ttu-id="30100-216">Dieser Name entspricht dem physikalischen Verzeichnis der Website auf dem Server und wird dem Hostnamen der Website angefügt, beispielsweise:</span><span class="sxs-lookup"><span data-stu-id="30100-216">This name corresponds to the website’s physical directory on the server and is appended to the website’s host name, for example:</span></span></p>
   <p><span data-ttu-id="30100-217">http (s):// &lt; <em> Hostname </em> &gt; : &lt; <em> Port </em> &gt; /Helpdesk/</span><span class="sxs-lookup"><span data-stu-id="30100-217">http(s)://&lt;<em>hostname</em>&gt;:&lt;<em>port</em>&gt;/HelpDesk/</span></span></p>
   <p><span data-ttu-id="30100-218">Wenn Sie kein virtuelles Verzeichnis angeben, wird der Wert <strong> Helpdesk </strong> verwendet.</span><span class="sxs-lookup"><span data-stu-id="30100-218">If you do not specify a virtual directory, the value <strong>HelpDesk</strong> will be used.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="30100-219">Domänengruppe "Daten Migrations Rolle" </strong> (optional)</span><span class="sxs-lookup"><span data-stu-id="30100-219">Data Migration role domain group</strong> (optional)</span></span></p></td>
   <td align="left"><p><span data-ttu-id="30100-220">Die Domänenbenutzergruppe, deren Mitglieder Zugriff haben, um die mbam \*-Informations-Cmdlets zu verwenden, um Wiederherstellungsinformationen über diesen Endpunkt zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="30100-220">Domain user group whose members have access to use the Write-Mbam\*Information Cmdlets to write recovery information via this endpoint.</span></span></p></td>
   </tr>
   </tbody>
   </table>



2. <span data-ttu-id="30100-221">Verwenden Sie die folgende Beschreibung, um die Feldwerte im Assistenten einzugeben, um das Self-Service-Portal zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="30100-221">Use the following description to enter the field values in the wizard to configure the Self-Service Portal.</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="30100-222">Feld</span><span class="sxs-lookup"><span data-stu-id="30100-222">Field</span></span></th>
   <th align="left"><span data-ttu-id="30100-223">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="30100-223">Description</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="30100-224">Virtuelles Verzeichnis</span><span class="sxs-lookup"><span data-stu-id="30100-224">Virtual directory</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="30100-225">Virtuelles Verzeichnis der Web-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="30100-225">Virtual directory of the web application.</span></span> <span data-ttu-id="30100-226">Dieser Name entspricht dem physikalischen Verzeichnis der Website auf dem Server und wird dem Hostnamen der Website angefügt, beispielsweise:</span><span class="sxs-lookup"><span data-stu-id="30100-226">This name corresponds to the website’s physical directory on the server, and is appended to the website’s host name, for example:</span></span></p>
   <p><span data-ttu-id="30100-227">http (s):// &lt; <em> Hostname </em> &gt; : &lt; <em> Port </em> &gt; /Selfservice/</span><span class="sxs-lookup"><span data-stu-id="30100-227">http(s)://&lt;<em>hostname</em>&gt;:&lt;<em>port</em>&gt;/SelfService/</span></span></p>
   <p><span data-ttu-id="30100-228">Wenn Sie kein virtuelles Verzeichnis angeben, wird der Wert <strong> Selfservice </strong> verwendet.</span><span class="sxs-lookup"><span data-stu-id="30100-228">If you do not specify a virtual directory, the value <strong>SelfService</strong> will be used.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="30100-229">Firmenname</span><span class="sxs-lookup"><span data-stu-id="30100-229">Company name</span></span></p></td>
   <td align="left"><p><span data-ttu-id="30100-230">Geben Sie einen Firmennamen für das Self-Service-Portal an, beispielsweise:</span><span class="sxs-lookup"><span data-stu-id="30100-230">Specify a company name for the Self-Service Portal, for example:</span></span></p>
   <p><span data-ttu-id="30100-231">Contoso IT</span><span class="sxs-lookup"><span data-stu-id="30100-231">Contoso IT</span></span></p>
   <p><span data-ttu-id="30100-232">Dieser Firmenname wird von allen Self-Service-Portal Benutzern angezeigt.</span><span class="sxs-lookup"><span data-stu-id="30100-232">This company name is viewed by all Self-Service Portal users.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="30100-233">Helpdesk-URL-Text</span><span class="sxs-lookup"><span data-stu-id="30100-233">Helpdesk URL text</span></span></p></td>
   <td align="left"><p><span data-ttu-id="30100-234">Geben Sie eine Text Anweisung an, die die Benutzer an die Helpdesk-Website Ihrer Organisation weiterleitet, beispielsweise:</span><span class="sxs-lookup"><span data-stu-id="30100-234">Specify a text statement that directs users to your organization's Helpdesk website, for example:</span></span></p>
   <p><span data-ttu-id="30100-235">Helpdesk oder IT-Abteilung kontaktieren</span><span class="sxs-lookup"><span data-stu-id="30100-235">Contact Helpdesk or IT department</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="30100-236">Helpdesk-URL</span><span class="sxs-lookup"><span data-stu-id="30100-236">Helpdesk URL</span></span></p></td>
   <td align="left"><p><span data-ttu-id="30100-237">Geben Sie die URL für die Helpdesk-Website Ihrer Organisation an, beispielsweise:</span><span class="sxs-lookup"><span data-stu-id="30100-237">Specify the URL for your organization's Helpdesk website, for example:</span></span></p>
   <p><span data-ttu-id="30100-238">http (s):// &lt; <em> companyHelpdeskURL</em>&gt;/</span><span class="sxs-lookup"><span data-stu-id="30100-238">http(s)://&lt;<em>companyHelpdeskURL</em>&gt;/</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="30100-239">Hinweistext Datei</span><span class="sxs-lookup"><span data-stu-id="30100-239">Notice text file</span></span></p></td>
   <td align="left"><p><span data-ttu-id="30100-240">Wählen Sie eine Datei aus, die den Hinweis enthält, der Benutzern auf der Startseite des Self-Service-Portals angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="30100-240">Select a file that contains the notice you want displayed to users on the Self-Service Portal landing page.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="30100-241">Hinweistext für Benutzer nicht anzeigen</span><span class="sxs-lookup"><span data-stu-id="30100-241">Do not display notice text to users</span></span></p></td>
   <td align="left"><p><span data-ttu-id="30100-242">Aktivieren Sie dieses Kontrollkästchen, um anzugeben, dass der Hinweistext für die Benutzer nicht angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="30100-242">Select this check box to specify that the notice text is not displayed to users.</span></span></p></td>
   </tr>
   </tbody>
   </table>



3. <span data-ttu-id="30100-243">Wenn Sie Ihre Eingaben abgeschlossen haben, klicken Sie auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="30100-243">When you finish your entries, click **Next**.</span></span>

   <span data-ttu-id="30100-244">Der Assistent überprüft, ob alle Voraussetzungen für die Webanwendungen erfüllt sind.</span><span class="sxs-lookup"><span data-stu-id="30100-244">The wizard checks that all prerequisites for the web applications have been met.</span></span>

4. <span data-ttu-id="30100-245">Klicken Sie auf **Weiter**, um den Vorgang fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="30100-245">Click **Next** to continue.</span></span>

5. <span data-ttu-id="30100-246">Überprüfen Sie auf der Seite **Zusammenfassung** die Features, die hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="30100-246">On the **Summary** page, review the features that will be added.</span></span>

   **<span data-ttu-id="30100-247">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="30100-247">Note</span></span>**  
   <span data-ttu-id="30100-248">Wenn Sie ein Windows PowerShell-Skript für die von Ihnen erstellten Einträge erstellen möchten, klicken Sie auf **PowerShell-Skript exportieren** , und speichern Sie das Skript.</span><span class="sxs-lookup"><span data-stu-id="30100-248">To create a Windows PowerShell script for the entries you made, click **Export PowerShell Script** and save the script.</span></span>



6. <span data-ttu-id="30100-249">Klicken Sie auf **Hinzufügen** , um die Webanwendungen zum Server hinzuzufügen, und klicken Sie dann auf **Schließen**.</span><span class="sxs-lookup"><span data-stu-id="30100-249">Click **Add** to add the web applications to the server, and then click **Close**.</span></span>

   <span data-ttu-id="30100-250">Informationen zum Anpassen des Self-Service-Portals durch Hinzufügen von benutzerdefiniertem Benachrichtigungstext, dem Namen Ihres Unternehmens, verweisen auf Weitere Informationen usw. finden Sie unter [Anpassen des Self-Service-Portals für Ihre Organisation](customizing-the-self-service-portal-for-your-organization.md).</span><span class="sxs-lookup"><span data-stu-id="30100-250">To customize the Self-Service Portal by adding custom notice text, your company name, pointers to more information, and so on, see [Customizing the Self-Service Portal for Your Organization](customizing-the-self-service-portal-for-your-organization.md).</span></span>

**<span data-ttu-id="30100-251">So konfigurieren Sie das Self-Service-Portal, wenn Clientcomputer nicht auf das CDN zugreifen können</span><span class="sxs-lookup"><span data-stu-id="30100-251">To configure the Self-Service Portal if client computers cannot access the CDN</span></span>**

1.  <span data-ttu-id="30100-252">Ermitteln Sie, ob Sie Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) 2,5 SP1 ausführen.</span><span class="sxs-lookup"><span data-stu-id="30100-252">Determine whether you are running Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 SP1.</span></span> <span data-ttu-id="30100-253">Wenn ja, tun Sie nichts.</span><span class="sxs-lookup"><span data-stu-id="30100-253">If so, do nothing.</span></span> <span data-ttu-id="30100-254">Ihre Self-Service-Portal-Konfiguration ist abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="30100-254">Your Self-Service Portal configuration is complete.</span></span>

    **<span data-ttu-id="30100-255">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="30100-255">Note</span></span>**  
    <span data-ttu-id="30100-256">Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) 2,5 SP1 installiert die JavaScript-Dateien in Setup und muss daher nicht mit dem Microsoft AJAX-Inhalts Zustellungs Netzwerk verbunden sein, um das Self-Service-Portal konfigurieren zu können.</span><span class="sxs-lookup"><span data-stu-id="30100-256">Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 SP1 installs the JavaScript files in setup, and so does not need to be connected to the Microsoft Ajax Content Delivery Network in order to configure the Self-Service Portal.</span></span> <span data-ttu-id="30100-257">Die folgenden Schritte sind nur erforderlich, wenn Sie eine Version von Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) 2,5 zurück zu SP1 verwenden.</span><span class="sxs-lookup"><span data-stu-id="30100-257">The following steps are necessary only if you are using a version of Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 previous to SP1.</span></span>



2.  <span data-ttu-id="30100-258">Ermitteln Sie, ob Ihre Clientcomputer Zugriff auf das Microsoft AJAX Content Delivery Network (CDN) haben.</span><span class="sxs-lookup"><span data-stu-id="30100-258">Determine if your client computers have access to the Microsoft Ajax Content Delivery Network (CDN).</span></span>

    <span data-ttu-id="30100-259">Das CDN gewährt dem Self-Service-Portal den erforderlichen Zugriff auf bestimmte JavaScript-Dateien.</span><span class="sxs-lookup"><span data-stu-id="30100-259">The CDN gives the Self-Service Portal the access it requires to certain JavaScript files.</span></span> <span data-ttu-id="30100-260">Wenn Sie das Self-Service-Portal nicht konfigurieren, wenn Clientcomputer nicht auf das CDN zugreifen können, werden nur der Firmenname und das Konto angezeigt, unter dem der Benutzer angemeldet ist.</span><span class="sxs-lookup"><span data-stu-id="30100-260">If you don’t configure the Self-Service Portal when client computers cannot access the CDN, only the company name and the account under which the end user signed in will be displayed.</span></span> <span data-ttu-id="30100-261">Es wird keine Fehlermeldung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="30100-261">No error message will be shown.</span></span>

3.  <span data-ttu-id="30100-262">Führen Sie eine der folgenden Aktionen aus:</span><span class="sxs-lookup"><span data-stu-id="30100-262">Do one of the following:</span></span>

    -   <span data-ttu-id="30100-263">Wenn Ihre Clientcomputer Zugriff auf das CDN haben, tun Sie nichts.</span><span class="sxs-lookup"><span data-stu-id="30100-263">If your client computers have access to the CDN, do nothing.</span></span> <span data-ttu-id="30100-264">Ihre Self-Service-Portal-Konfiguration ist abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="30100-264">Your Self-Service Portal configuration is complete.</span></span>

    -   <span data-ttu-id="30100-265">Wenn Ihre Clientcomputer keinen Zugriff auf das CDN haben, führen Sie die Schritte unter [Konfigurieren des Self-Service-Portals aus, wenn Clientcomputer nicht auf das Microsoft Content Delivery Network zugreifen können](how-to-configure-the-self-service-portal-when-client-computers-cannot-access-the-microsoft-content-delivery-network.md).</span><span class="sxs-lookup"><span data-stu-id="30100-265">If your client computers do not have access to the CDN, complete the steps in [How to Configure the Self-Service Portal When Client Computers Cannot Access the Microsoft Content Delivery Network](how-to-configure-the-self-service-portal-when-client-computers-cannot-access-the-microsoft-content-delivery-network.md).</span></span>


## <span data-ttu-id="30100-266">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="30100-266">Related topics</span></span>


[<span data-ttu-id="30100-267">Serverereignisprotokolle</span><span class="sxs-lookup"><span data-stu-id="30100-267">Server Event Logs</span></span>](server-event-logs.md)

[<span data-ttu-id="30100-268">Konfigurieren der MBAM 2.5-Serverfunktionen</span><span class="sxs-lookup"><span data-stu-id="30100-268">Configuring the MBAM 2.5 Server Features</span></span>](configuring-the-mbam-25-server-features.md)

[<span data-ttu-id="30100-269">So konfigurieren Sie das Self-Service-Portal, wenn Clientcomputer nicht auf das Microsoft Content Delivery Network zugreifen können</span><span class="sxs-lookup"><span data-stu-id="30100-269">How to Configure the Self-Service Portal When Client Computers Cannot Access the Microsoft Content Delivery Network</span></span>](how-to-configure-the-self-service-portal-when-client-computers-cannot-access-the-microsoft-content-delivery-network.md)

[<span data-ttu-id="30100-270">Anpassen des Self-Service-Portals für Ihre Organisation</span><span class="sxs-lookup"><span data-stu-id="30100-270">Customizing the Self-Service Portal for Your Organization</span></span>](customizing-the-self-service-portal-for-your-organization.md)

[<span data-ttu-id="30100-271">Überprüfen der Konfiguration von MBAM 2.5 Serverfunktionen</span><span class="sxs-lookup"><span data-stu-id="30100-271">Validating the MBAM 2.5 Server Feature Configuration</span></span>](validating-the-mbam-25-server-feature-configuration.md)



## <span data-ttu-id="30100-272">Sie haben einen Vorschlag für MBAM?</span><span class="sxs-lookup"><span data-stu-id="30100-272">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="30100-273">[Hier](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)können Sie Vorschläge hinzufügen oder abstimmen.</span><span class="sxs-lookup"><span data-stu-id="30100-273">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="30100-274">Bei MBAM-Problemen verwenden Sie das [MBAM TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="30100-274">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





