---
title: Überprüfen der Konfiguration von MBAM 2.5 Serverfunktionen
description: Überprüfen der Konfiguration von MBAM 2.5 Serverfunktionen
author: dansimp
ms.assetid: f4983a33-ce18-4186-a471-dd6415940504
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f955e0b9ccb7952995574e4aa981674f7c7667fe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812142"
---
# <span data-ttu-id="d7e6b-103">Überprüfen der Konfiguration von MBAM 2.5 Serverfunktionen</span><span class="sxs-lookup"><span data-stu-id="d7e6b-103">Validating the MBAM 2.5 Server Feature Configuration</span></span>


<span data-ttu-id="d7e6b-104">Wenn Sie die Bereitstellung der Microsoft BitLocker-Verwaltungs-und-Überwachungsfunktion (MBAM) 2,5 Server abgeschlossen haben, empfiehlt es sich, die Bereitstellung zu überprüfen, um sicherzustellen, dass alle Features erfolgreich konfiguriert wurden.</span><span class="sxs-lookup"><span data-stu-id="d7e6b-104">When you finish the Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 Server feature deployment, we recommend that you validate the deployment to ensure that all features have been successfully configured.</span></span> <span data-ttu-id="d7e6b-105">Verwenden Sie das Verfahren, das der von Ihnen bereitgestellten Topologie (eigenständige oder System Center Configuration Manager-Integration) entspricht.</span><span class="sxs-lookup"><span data-stu-id="d7e6b-105">Use the procedure that matches the topology (Stand-alone or System Center Configuration Manager Integration) that you deployed.</span></span>

## <span data-ttu-id="d7e6b-106">Überprüfen der MBAM-Server Bereitstellung mit der eigenständigen Topologie</span><span class="sxs-lookup"><span data-stu-id="d7e6b-106">Validating the MBAM Server deployment with the Stand-alone topology</span></span>


<span data-ttu-id="d7e6b-107">Führen Sie die folgenden Schritte aus, um die Bereitstellung Ihres MBAM-Servers mit der eigenständigen Topologie zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="d7e6b-107">Use the following steps to validate your MBAM Server deployment with the Stand-alone topology.</span></span>

**<span data-ttu-id="d7e6b-108">So überprüfen Sie eine eigenständige MBAM-Server Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="d7e6b-108">To validate a Stand-alone MBAM Server deployment</span></span>**

1.  <span data-ttu-id="d7e6b-109">Klicken Sie auf jedem Server, auf dem ein MBAM- **Control Panel** Feature bereitgestellt wird, auf Programme &gt; **Programs** &gt; **und Funktionen**der Systemsteuerung.</span><span class="sxs-lookup"><span data-stu-id="d7e6b-109">On each server where an MBAM feature is deployed, click **Control Panel** &gt; **Programs** &gt; **Programs and Features**.</span></span> <span data-ttu-id="d7e6b-110">Überprüfen Sie, ob die **Microsoft BitLocker-Verwaltung und-Überwachung** in der Liste " **Programme und Features** " angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="d7e6b-110">Verify that **Microsoft BitLocker Administration and Monitoring** appears in the **Programs and Features** list.</span></span>

    **<span data-ttu-id="d7e6b-111">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="d7e6b-111">Note</span></span>**  
    <span data-ttu-id="d7e6b-112">Um die Überprüfung durchführen zu können, müssen Sie ein Domänenkonto verwenden, das auf jedem Server über Administratoranmeldeinformationen des lokalen Computers verfügt.</span><span class="sxs-lookup"><span data-stu-id="d7e6b-112">To do the validation, you must use a domain account that has local computer administrative credentials on each server.</span></span>



2.  <span data-ttu-id="d7e6b-113">Öffnen Sie auf dem Server, auf dem die Wiederherstellungsdatenbank konfiguriert ist, SQL Server Management Studio, und überprüfen Sie, ob die **MBAM-Wiederherstellungs-und-Hardware** Datenbank konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="d7e6b-113">On the server where the Recovery Database is configured, open SQL Server Management Studio and verify that the **MBAM Recovery and Hardware** database is configured.</span></span>

3.  <span data-ttu-id="d7e6b-114">Öffnen Sie auf dem Server, auf dem die Konformitäts-und Überwachungsdatenbank konfiguriert ist, SQL Server Management Studio, und überprüfen Sie, ob die **MBAM-Konformitäts Status Datenbank** konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="d7e6b-114">On the server where the Compliance and Audit Database is configured, open SQL Server Management Studio and verify that the **MBAM Compliance Status Database** is configured.</span></span>

4.  <span data-ttu-id="d7e6b-115">Öffnen Sie auf dem Server, auf dem das Feature Berichte konfiguriert ist, einen Webbrowser mit administrativen Anmeldeinformationen, und navigieren Sie zu "Start" der SQL Server Reporting Services-Website.</span><span class="sxs-lookup"><span data-stu-id="d7e6b-115">On the server where the Reports feature is configured, open a web browser with administrative credentials and browse to the "Home" of the SQL Server Reporting Services site.</span></span>

    <span data-ttu-id="d7e6b-116">Der standardmäßige Startspeicherort einer SQL Server Reporting Services-Websiteinstanz lautet:</span><span class="sxs-lookup"><span data-stu-id="d7e6b-116">The default Home location of a SQL Server Reporting Services site instance is at:</span></span>

    <span data-ttu-id="d7e6b-117">http (s):// &lt; *MBAMReportsServerName* &gt; : &lt; *Port* &gt; /Reports.aspx</span><span class="sxs-lookup"><span data-stu-id="d7e6b-117">http(s)://&lt; *MBAMReportsServerName*&gt;:&lt;*port*&gt;/Reports.aspx</span></span>

    <span data-ttu-id="d7e6b-118">Um die tatsächliche URL zu finden, verwenden Sie das Reporting Services-Konfigurations-Manager-Tool, und wählen Sie die Instanzen aus, die Sie während der Installation angegeben haben.</span><span class="sxs-lookup"><span data-stu-id="d7e6b-118">To find the actual URL, use the Reporting Services Configuration Manager tool and select the instances that you specified during setup.</span></span>

5.  <span data-ttu-id="d7e6b-119">Vergewissern Sie sich, dass ein Berichtsordner mit dem Namen **Microsoft BitLocker-Verwaltung und-Überwachung** eine Datenquelle mit dem Namen **MaltaDataSource** und die Sprachordner enthält.</span><span class="sxs-lookup"><span data-stu-id="d7e6b-119">Confirm that a reports folder named **Microsoft BitLocker Administration and Monitoring** contains a data source called **MaltaDataSource** as well as the language folders.</span></span> <span data-ttu-id="d7e6b-120">Die Datenquelle enthält Ordner mit Namen, die Sprachen darstellen (beispielsweise "en-US").</span><span class="sxs-lookup"><span data-stu-id="d7e6b-120">The data source contains folders with names that represent languages (for example, en-us).</span></span> <span data-ttu-id="d7e6b-121">Die Berichte befinden sich in den Sprachordnern.</span><span class="sxs-lookup"><span data-stu-id="d7e6b-121">The reports are in the language folders.</span></span>

    **<span data-ttu-id="d7e6b-122">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="d7e6b-122">Note</span></span>**  
    <span data-ttu-id="d7e6b-123">Wenn SQL Server Reporting Services (SSRS) als benannte Instanz konfiguriert wurde, sollte die URL wie folgt aussehen: http (s):// &lt; *MBAMReportsServerName* &gt; : &lt; *Port* &gt; /Reports\_ &lt; *SSRSInstanceName*&gt;</span><span class="sxs-lookup"><span data-stu-id="d7e6b-123">If SQL Server Reporting Services (SSRS) was configured as a named instance, the URL should resemble the following: http(s)://&lt; *MBAMReportsServerName*&gt;:&lt;*port*&gt;/Reports\_&lt;*SSRSInstanceName*&gt;</span></span>



~~~
**Note**  
If SSRS was not configured to use Secure Socket Layer (SSL), the URL for the reports will be set to HTTP instead of HTTPS when you install the MBAM Server. If you then go to the Administration and Monitoring Website (also known as Help Desk) and select a report, the following message appears: "Only Secure Content is Displayed." To show the report, click **Show All Content**.
~~~



6. <span data-ttu-id="d7e6b-124">Führen Sie auf dem Server, auf dem die Verwaltungs-und Überwachungs Website-Funktion konfiguriert ist, den **Server-Manager**aus, navigieren Sie zu **Rollen**, und wählen Sie dann **Web Server (** IIS) &gt; **Internetinformationsdienste (IIS)-Manager**aus.</span><span class="sxs-lookup"><span data-stu-id="d7e6b-124">On the server where the Administration and Monitoring Website feature is configured, run **Server Manager**, browse to **Roles**, and then select **Web Server (IIS)** &gt; **Internet Information Services (IIS) Manager**.</span></span>

7. <span data-ttu-id="d7e6b-125">Navigieren Sie in **Verbindungen**zu \* &lt; Computername &gt; \* , und wählen Sie **Websites** &gt; **Microsoft BitLocker-Verwaltung und-Überwachung**aus.</span><span class="sxs-lookup"><span data-stu-id="d7e6b-125">In **Connections**, browse to *&lt;computer name&gt;* and select **Sites** &gt; **Microsoft BitLocker Administration and Monitoring**.</span></span> <span data-ttu-id="d7e6b-126">Überprüfen Sie, ob die folgenden Angaben aufgeführt sind:</span><span class="sxs-lookup"><span data-stu-id="d7e6b-126">Verify that the following are listed:</span></span>

   -   **<span data-ttu-id="d7e6b-127">MBAMAdministrationService</span><span class="sxs-lookup"><span data-stu-id="d7e6b-127">MBAMAdministrationService</span></span>**

   -   **<span data-ttu-id="d7e6b-128">MBAMComplianceStatusService</span><span class="sxs-lookup"><span data-stu-id="d7e6b-128">MBAMComplianceStatusService</span></span>**

   -   **<span data-ttu-id="d7e6b-129">MBAMRecoveryAndHardwareService</span><span class="sxs-lookup"><span data-stu-id="d7e6b-129">MBAMRecoveryAndHardwareService</span></span>**

8. <span data-ttu-id="d7e6b-130">Öffnen Sie auf dem Server, auf dem die Verwaltungs-und Überwachungs Website sowie das Self-Service-Portal konfiguriert sind, einen Webbrowser mit administrativen Anmeldeinformationen.</span><span class="sxs-lookup"><span data-stu-id="d7e6b-130">On the server where the Administration and Monitoring Website and Self-Service Portal are configured, open a web browser with administrative credentials.</span></span>

9. <span data-ttu-id="d7e6b-131">Navigieren Sie zu den folgenden Websites, um sicherzustellen, dass Sie erfolgreich geladen werden:</span><span class="sxs-lookup"><span data-stu-id="d7e6b-131">Browse to the following websites to verify that they load successfully:</span></span>

   -   <span data-ttu-id="d7e6b-132">HTTPS (s):// &lt; *MBAMAdministrationServerName* &gt; : &lt; *Port* &gt; /Helpdesk/– bestätigen Sie die einzelnen Links für Navigation und Berichte.</span><span class="sxs-lookup"><span data-stu-id="d7e6b-132">https(s)://&lt;*MBAMAdministrationServerName*&gt;:&lt;*port*&gt;/HelpDesk/ - confirm each of the links for navigation and reports</span></span>

   -   <span data-ttu-id="d7e6b-133">http (s):// &lt; *MBAMAdministrationServerName* &gt; : &lt; *Port* &gt; /Selfservice/</span><span class="sxs-lookup"><span data-stu-id="d7e6b-133">http(s)://&lt; *MBAMAdministrationServerName*&gt;:&lt;*port*&gt;/SelfService/</span></span>

   **<span data-ttu-id="d7e6b-134">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="d7e6b-134">Note</span></span>**  
   <span data-ttu-id="d7e6b-135">Es wird davon ausgegangen, dass Sie die Server Features auf dem Standardport ohne Netzwerk Verschlüsselung konfiguriert haben.</span><span class="sxs-lookup"><span data-stu-id="d7e6b-135">It is assumed that you configured the server features on the default port without network encryption.</span></span> <span data-ttu-id="d7e6b-136">Wenn Sie die Server Features in einem anderen Port oder virtuellen Verzeichnis konfiguriert haben, ändern Sie die URLs so, dass Sie den entsprechenden Port umfassen, beispielsweise:</span><span class="sxs-lookup"><span data-stu-id="d7e6b-136">If you configured the server features on a different port or virtual directory, change the URLs to include the appropriate port, for example:</span></span>

   <span data-ttu-id="d7e6b-137">http (s):// &lt; *Hostname* &gt; : &lt; *Port* &gt; /Helpdesk/</span><span class="sxs-lookup"><span data-stu-id="d7e6b-137">http(s)://&lt; *host name*&gt;:&lt;*port*&gt;/HelpDesk/</span></span>

   <span data-ttu-id="d7e6b-138">http (s):// &lt; *Hostname* &gt; : &lt; *Port* &gt; / &lt; *VirtualDirectory*&gt;/</span><span class="sxs-lookup"><span data-stu-id="d7e6b-138">http(s)://&lt; *host name*&gt;:&lt;*port*&gt;/&lt;*virtualdirectory*&gt;/</span></span>

   <span data-ttu-id="d7e6b-139">Wenn die Server Features mit Netzwerk Verschlüsselung konfiguriert wurden, ändern Sie http://in https://.</span><span class="sxs-lookup"><span data-stu-id="d7e6b-139">If the server features were configured with network encryption, change http:// to https://.</span></span>



10. <span data-ttu-id="d7e6b-140">Navigieren Sie zu den folgenden Webdiensten, um sicherzustellen, dass Sie erfolgreich geladen werden.</span><span class="sxs-lookup"><span data-stu-id="d7e6b-140">Browse to the following web services to verify that they load successfully.</span></span> <span data-ttu-id="d7e6b-141">Eine Seite wird geöffnet, um anzugeben, dass der Dienst ausgeführt wird, aber auf der Seite werden keine Metadaten angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d7e6b-141">A page opens to indicate that the service is running, but the page does not display any metadata.</span></span>

    -   <span data-ttu-id="d7e6b-142">http (s):// &lt; *MBAMAdministrationServerName* &gt; : &lt; *Port* &gt; /MBAMAdministrationService/AdministrationService.svc</span><span class="sxs-lookup"><span data-stu-id="d7e6b-142">http(s)://&lt; *MBAMAdministrationServerName*&gt;:&lt;*port*&gt;/MBAMAdministrationService/AdministrationService.svc</span></span>

    -   <span data-ttu-id="d7e6b-143">http (s):// &lt; *MBAMAdministrationServerName* &gt; : &lt; *Port* &gt; /MBAMUserSupportService/UserSupportService.svc</span><span class="sxs-lookup"><span data-stu-id="d7e6b-143">http(s)://&lt; *MBAMAdministrationServerName*&gt;:&lt;*port*&gt;/MBAMUserSupportService/UserSupportService.svc</span></span>

    -   <span data-ttu-id="d7e6b-144">http (s):// &lt; *MBAMAdministrationServerName* &gt; : &lt; *Port* &gt; /MBAMComplianceStatusService/StatusReportingService.svc</span><span class="sxs-lookup"><span data-stu-id="d7e6b-144">http(s)://&lt; *MBAMAdministrationServerName*&gt;:&lt;*port*&gt;/MBAMComplianceStatusService/StatusReportingService.svc</span></span>

    -   <span data-ttu-id="d7e6b-145">http (s):// &lt; *MBAMAdministrationServerName* &gt; : &lt; *Port* &gt; /MBAMRecoveryAndHardwareService/CoreService.svc</span><span class="sxs-lookup"><span data-stu-id="d7e6b-145">http(s)://&lt; *MBAMAdministrationServerName*&gt;:&lt;*port*&gt;/MBAMRecoveryAndHardwareService/CoreService.svc</span></span>

## <span data-ttu-id="d7e6b-146">Überprüfen der MBAM-Server Bereitstellung mit der Configuration Manager-Integrations Topologie</span><span class="sxs-lookup"><span data-stu-id="d7e6b-146">Validating the MBAM Server deployment with the Configuration Manager Integration topology</span></span>


<span data-ttu-id="d7e6b-147">Führen Sie die folgenden Schritte aus, um Ihre MBAM-Bereitstellung mit der Configuration Manager-Integrations Topologie zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="d7e6b-147">Use the following steps to validate your MBAM deployment with the Configuration Manager Integration topology.</span></span> <span data-ttu-id="d7e6b-148">Führen Sie die Validierungsschritte aus, die der von Ihnen verwendeten Version von Configuration Manager entsprechen.</span><span class="sxs-lookup"><span data-stu-id="d7e6b-148">Complete the validation steps that match the version of Configuration Manager that you are using.</span></span>

### <a href="" id="validating-the-mbam-server-deployment-with-system-center-2012-configuration-manager-"></a><span data-ttu-id="d7e6b-149">Überprüfen der MBAM-Server Bereitstellung mit dem System Center 2012-Konfigurations-Manager</span><span class="sxs-lookup"><span data-stu-id="d7e6b-149">Validating the MBAM Server deployment with System Center 2012 Configuration Manager</span></span>

<span data-ttu-id="d7e6b-150">Führen Sie die folgenden Schritte aus, um Ihre MBAM-Server Bereitstellung zu überprüfen, wenn Sie MBAM mit dem System Center 2012-Konfigurations-Manager verwenden.</span><span class="sxs-lookup"><span data-stu-id="d7e6b-150">Use these steps to validate your MBAM Server deployment when you are using MBAM with System Center 2012 Configuration Manager.</span></span>

**<span data-ttu-id="d7e6b-151">So überprüfen Sie eine Configuration Manager-Integrations MBAM Server Bereitstellung – System Center 2012-Konfigurations-Manager</span><span class="sxs-lookup"><span data-stu-id="d7e6b-151">To validate a Configuration Manager Integration MBAM Server deployment – System Center 2012 Configuration Manager</span></span>**

1.  <span data-ttu-id="d7e6b-152">Öffnen Sie auf dem Server, auf dem System Center 2012 Configuration Manager bereitgestellt wird, **Programme und Funktionen** **in der Systemsteuerung,** und überprüfen Sie, ob die **Microsoft BitLocker-Verwaltung und-Überwachung** angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="d7e6b-152">On the server where System Center 2012 Configuration Manager is deployed, open **Programs and Features** in **Control Panel**, and verify that **Microsoft BitLocker Administration and Monitoring** appears.</span></span>

    **<span data-ttu-id="d7e6b-153">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="d7e6b-153">Note</span></span>**  
    <span data-ttu-id="d7e6b-154">Um die Konfiguration zu überprüfen, müssen Sie ein Domänenkonto verwenden, das über lokale Computeradministrator Anmeldeinformationen auf jedem Server verfügt.</span><span class="sxs-lookup"><span data-stu-id="d7e6b-154">To validate the configuration, you must use a domain account that has local computer administrative credentials on each server.</span></span>



2.  <span data-ttu-id="d7e6b-155">Klicken Sie in der Configuration Manager-Konsole auf die gerätesammlungen für den **Ressourcen-und Compliance** -Arbeitsbereich &gt; **Device Collections**, und vergewissern Sie sich, dass eine neue Sammlung mit dem Namen **MBAM unterstützte Computer** angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="d7e6b-155">In the Configuration Manager console, click the **Assets and Compliance** workspace &gt; **Device Collections**, and confirm that a new collection called **MBAM Supported Computers** is displayed.</span></span>

3.  <span data-ttu-id="d7e6b-156">Klicken Sie **in der Configuration** Manager-Konsole auf das &gt; **MBAM Bericht Erstellungs** &gt; **Berichte** für Arbeitsbereiche &gt; **MBAM**.</span><span class="sxs-lookup"><span data-stu-id="d7e6b-156">In the Configuration Manager console, click the **Monitoring** workspace &gt; **Reporting** &gt; **Reports** &gt; **MBAM**.</span></span>

4.  <span data-ttu-id="d7e6b-157">Überprüfen Sie, ob der **MBAM** -Ordner Unterordner mit Namen enthält, die verschiedene Sprachen darstellen, und dass die folgenden Berichte in jedem Unterordner "Sprache" aufgeführt sind:</span><span class="sxs-lookup"><span data-stu-id="d7e6b-157">Verify that the **MBAM** folder contains subfolders, with names that represent different languages, and that the following reports are listed in each language subfolder:</span></span>

    -   <span data-ttu-id="d7e6b-158">BitLocker-Computer Konformität</span><span class="sxs-lookup"><span data-stu-id="d7e6b-158">BitLocker Computer Compliance</span></span>

    -   <span data-ttu-id="d7e6b-159">BitLocker Enterprise Compliance-Dashboard</span><span class="sxs-lookup"><span data-stu-id="d7e6b-159">BitLocker Enterprise Compliance Dashboard</span></span>

    -   <span data-ttu-id="d7e6b-160">Details zur BitLocker-Unternehmenskonformität</span><span class="sxs-lookup"><span data-stu-id="d7e6b-160">BitLocker Enterprise Compliance Details</span></span>

    -   <span data-ttu-id="d7e6b-161">Zusammenfassung der BitLocker-Unternehmenskonformität</span><span class="sxs-lookup"><span data-stu-id="d7e6b-161">BitLocker Enterprise Compliance Summary</span></span>

5.  <span data-ttu-id="d7e6b-162">Klicken Sie in der Configuration Manager-Konsole **Assets and Compliance** auf die Konfigurationsbasislinien für Compliance-Einstellungen des Arbeitsbereichs &gt; **Compliance Settings** &gt; **Configuration Baselines**, und vergewissern Sie sich, dass der BitLocker-Konfigurationsbasislinien- **Schutz** aufgeführt ist.</span><span class="sxs-lookup"><span data-stu-id="d7e6b-162">In the Configuration Manager console, click the **Assets and Compliance** workspace &gt; **Compliance Settings** &gt; **Configuration Baselines**, and confirm that the configuration baseline **BitLocker Protection** is listed.</span></span>

6.  <span data-ttu-id="d7e6b-163">Klicken Sie in der Configuration Manager-Konsole auf die Konfigurationselemente für Compliance-Einstellungen für **den Arbeitsbereich** &gt; **Compliance Settings** &gt; **Configuration Items**, und vergewissern Sie sich, dass die folgenden neuen Konfigurationselemente angezeigt werden:</span><span class="sxs-lookup"><span data-stu-id="d7e6b-163">In the Configuration Manager console, click the **Assets and Compliance** workspace &gt; **Compliance Settings** &gt; **Configuration Items**, and confirm that the following new configuration items are displayed:</span></span>

    -   <span data-ttu-id="d7e6b-164">BitLocker-Datenlaufwerke mit fester Datensicherheit</span><span class="sxs-lookup"><span data-stu-id="d7e6b-164">BitLocker Fixed Data Drives Protection</span></span>

    -   <span data-ttu-id="d7e6b-165">BitLocker-Betriebs System-Laufwerkschutz</span><span class="sxs-lookup"><span data-stu-id="d7e6b-165">BitLocker Operating System Drive Protection</span></span>

### <span data-ttu-id="d7e6b-166">Überprüfen der MBAM-Server Bereitstellung mit Configuration Manager 2007</span><span class="sxs-lookup"><span data-stu-id="d7e6b-166">Validating the MBAM Server deployment with Configuration Manager 2007</span></span>

<span data-ttu-id="d7e6b-167">Führen Sie die folgenden Schritte aus, um Ihre MBAM-Server Bereitstellung zu überprüfen, wenn Sie MBAM mit Configuration Manager 2007 verwenden.</span><span class="sxs-lookup"><span data-stu-id="d7e6b-167">Use these steps to validate your MBAM Server deployment when you are using MBAM with Configuration Manager 2007.</span></span>

**<span data-ttu-id="d7e6b-168">So überprüfen Sie eine Configuration Manager-Integrations MBAM Server Bereitstellung – Configuration Manager 2007</span><span class="sxs-lookup"><span data-stu-id="d7e6b-168">To validate a Configuration Manager Integration MBAM Server deployment – Configuration Manager 2007</span></span>**

1.  <span data-ttu-id="d7e6b-169">Öffnen Sie auf dem Server, auf dem Configuration Manager 2007 bereitgestellt wird, **Programme und Funktionen** in der **System** Steuerung, und überprüfen Sie, ob die **Microsoft BitLocker-Verwaltung und-Überwachung** angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="d7e6b-169">On the server where Configuration Manager 2007 is deployed, open **Programs and Features** on **Control Panel** , and verify that **Microsoft BitLocker Administration and Monitoring** appears.</span></span>

    **<span data-ttu-id="d7e6b-170">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="d7e6b-170">Note</span></span>**  
    <span data-ttu-id="d7e6b-171">Um die Konfiguration zu überprüfen, müssen Sie ein Domänenkonto verwenden, das über lokale Computeradministrator Anmeldeinformationen auf jedem Server verfügt.</span><span class="sxs-lookup"><span data-stu-id="d7e6b-171">To validate the configuration, you must use a domain account that has local computer administrative credentials on each server.</span></span>



2.  <span data-ttu-id="d7e6b-172">Klicken Sie in der Configuration Manager-Konsole auf **Website Datenbank &lt; SiteCode &gt;  -  &lt; Servername, Sitename &gt; &lt; &gt; ), Computer Verwaltung**, und vergewissern Sie sich, dass eine neue Sammlung mit dem Namen **MBAM unterstützte Computer** angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="d7e6b-172">In the Configuration Manager console, click **Site Database &lt;SiteCode&gt; - &lt;ServerName&gt;, &lt;SiteName&gt;), Computer Management**, and confirm that a new collection called **MBAM Supported Computers** is displayed.</span></span>

3.  <span data-ttu-id="d7e6b-173">Klicken Sie in der Configuration Manager-Konsole auf **Reporting** &gt; **Services** &gt; \*\* \\\\ &lt; Servername &gt; \*\* &gt; **Report Folders** &gt; **MBAM**.</span><span class="sxs-lookup"><span data-stu-id="d7e6b-173">In the Configuration Manager console, click **Reporting** &gt; **Reporting Services** &gt; **\\\\&lt;ServerName&gt;** &gt; **Report Folders** &gt; **MBAM**.</span></span>

    <span data-ttu-id="d7e6b-174">Überprüfen Sie, ob der **MBAM** -Ordner Unterordner mit Namen enthält, die verschiedene Sprachen darstellen, und dass die folgenden Berichte in jedem Unterordner "Sprache" aufgeführt sind:</span><span class="sxs-lookup"><span data-stu-id="d7e6b-174">Verify that the **MBAM** folder contains subfolders, with names that represent different languages, and that the following reports are listed in each language subfolder:</span></span>

    -   <span data-ttu-id="d7e6b-175">BitLocker-Computer Konformität</span><span class="sxs-lookup"><span data-stu-id="d7e6b-175">BitLocker Computer Compliance</span></span>

    -   <span data-ttu-id="d7e6b-176">BitLocker Enterprise Compliance-Dashboard</span><span class="sxs-lookup"><span data-stu-id="d7e6b-176">BitLocker Enterprise Compliance Dashboard</span></span>

    -   <span data-ttu-id="d7e6b-177">Details zur BitLocker-Unternehmenskonformität</span><span class="sxs-lookup"><span data-stu-id="d7e6b-177">BitLocker Enterprise Compliance Details</span></span>

    -   <span data-ttu-id="d7e6b-178">Zusammenfassung der BitLocker-Unternehmenskonformität</span><span class="sxs-lookup"><span data-stu-id="d7e6b-178">BitLocker Enterprise Compliance Summary</span></span>

4.  <span data-ttu-id="d7e6b-179">Klicken Sie in der Configuration Manager- **Desired Configuration Management** Konsole auf &gt; **Konfigurationsbasislinien**für die gewünschte Konfigurationsverwaltung, und vergewissern Sie sich, dass der **BitLocker** -Konfigurationsbasislinien-Schutz aufgelistet ist.</span><span class="sxs-lookup"><span data-stu-id="d7e6b-179">In the Configuration Manager console, click **Desired Configuration Management** &gt; **Configuration Baselines**, and confirm that the configuration baseline **BitLocker Protection** is listed.</span></span>

5.  <span data-ttu-id="d7e6b-180">Klicken Sie in der Configuration Manager- **Desired Configuration Management** Konsole auf &gt; **Konfigurationselemente**für die Verwaltung der gewünschten Konfiguration, und vergewissern Sie sich, dass die folgenden neuen Konfigurationselemente angezeigt werden:</span><span class="sxs-lookup"><span data-stu-id="d7e6b-180">In the Configuration Manager console, click **Desired Configuration Management** &gt; **Configuration Items**, and confirm that the following new configuration items are displayed:</span></span>

    -   <span data-ttu-id="d7e6b-181">BitLocker-Datenlaufwerke mit fester Datensicherheit</span><span class="sxs-lookup"><span data-stu-id="d7e6b-181">BitLocker Fixed Data Drives Protection</span></span>

    -   <span data-ttu-id="d7e6b-182">BitLocker-Betriebs System-Laufwerkschutz</span><span class="sxs-lookup"><span data-stu-id="d7e6b-182">BitLocker Operating System Drive Protection</span></span>



## <span data-ttu-id="d7e6b-183">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="d7e6b-183">Related topics</span></span>


[<span data-ttu-id="d7e6b-184">Konfigurieren der MBAM 2.5-Serverfunktionen</span><span class="sxs-lookup"><span data-stu-id="d7e6b-184">Configuring the MBAM 2.5 Server Features</span></span>](configuring-the-mbam-25-server-features.md)


## <span data-ttu-id="d7e6b-185">Sie haben einen Vorschlag für MBAM?</span><span class="sxs-lookup"><span data-stu-id="d7e6b-185">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="d7e6b-186">[Hier](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)können Sie Vorschläge hinzufügen oder abstimmen.</span><span class="sxs-lookup"><span data-stu-id="d7e6b-186">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="d7e6b-187">Bei MBAM-Problemen verwenden Sie das [MBAM TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="d7e6b-187">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>






