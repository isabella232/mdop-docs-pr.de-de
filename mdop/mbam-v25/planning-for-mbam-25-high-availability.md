---
title: Planen der hohen Verfügbarkeit von MBAM 2.5
description: Planen der hohen Verfügbarkeit von MBAM 2.5
author: dansimp
ms.assetid: 1e29b30c-33f1-4a52-9442-8c1391f0049c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 20c304f669cfe9e1484be47dea1b9fcc917aea2c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812058"
---
# <span data-ttu-id="c98bf-103">Planen der hohen Verfügbarkeit von MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="c98bf-103">Planning for MBAM 2.5 High Availability</span></span>


<span data-ttu-id="c98bf-104">Die Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) kann eine höhere Verfügbarkeit durch Verwendung einer oder mehrerer der folgenden Technologien gewährleisten, die in den folgenden Abschnitten beschrieben werden:</span><span class="sxs-lookup"><span data-stu-id="c98bf-104">Microsoft BitLocker Administration and Monitoring (MBAM) can maintain high availability through use of one or more of the following technologies, which are described in the following sections:</span></span>

-   [<span data-ttu-id="c98bf-105">Verfügbarkeitsgruppen für SQL Server-AlwaysOn</span><span class="sxs-lookup"><span data-stu-id="c98bf-105">SQL Server AlwaysOn availability groups</span></span>](#bkmk-alwayson)

-   [<span data-ttu-id="c98bf-106">Microsoft SQL Server-Clustering</span><span class="sxs-lookup"><span data-stu-id="c98bf-106">Microsoft SQL Server clustering</span></span>](#bkmk-sql-clustering)

-   [<span data-ttu-id="c98bf-107">IIS-Netzwerklastenausgleich</span><span class="sxs-lookup"><span data-stu-id="c98bf-107">IIS Network Load Balancing</span></span>](#bkmk-load-balance)

-   [<span data-ttu-id="c98bf-108">Datenbankspiegelung in SQL Server</span><span class="sxs-lookup"><span data-stu-id="c98bf-108">Database mirroring in SQL Server</span></span>](#bkmk-db-mirroring)

-   [<span data-ttu-id="c98bf-109">Sichern von MBAM-Datenbanken mithilfe des Volumeschattenkopie-Diensts (Volume Shadow Copy Service, VSS)</span><span class="sxs-lookup"><span data-stu-id="c98bf-109">Backing up MBAM databases by using the Volume Shadow Copy Service (VSS)</span></span>](#bkmk-vss)

<span data-ttu-id="c98bf-110">Verwenden Sie die Informationen in den folgenden Abschnitten, damit Sie die Optionen zum Bereitstellen von MBAM in einer hoch verfügbaren Konfiguration verstehen können.</span><span class="sxs-lookup"><span data-stu-id="c98bf-110">Use the information in the following sections to help you understand the options to deploy MBAM in a highly available configuration.</span></span>

## <a href="" id="bkmk-alwayson"></a><span data-ttu-id="c98bf-111">Unterstützung für SQL Server AlwaysOn-Verfügbarkeitsgruppen</span><span class="sxs-lookup"><span data-stu-id="c98bf-111">Support for SQL Server AlwaysOn availability groups</span></span>


<span data-ttu-id="c98bf-112">MBAM ermöglicht es Ihnen, Verfügbarkeitsgruppen für die Datenbanken in Microsoft SQL Server zu konfigurieren und zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="c98bf-112">MBAM enables you to configure and manage availability groups for the databases in Microsoft SQL Server.</span></span> <span data-ttu-id="c98bf-113">Eine verfügbarkeitsgruppe für MBAM unterstützt eine Failover-Umgebung, in der die Konformitäts-und Überwachungsdatenbank und die Wiederherstellungsdatenbank nicht mehr einzeln, sondern gemeinsam ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="c98bf-113">An availability group for MBAM supports a failover environment where the Compliance and Audit Database and the Recovery Database fail over together rather than separately.</span></span>

<span data-ttu-id="c98bf-114">Eine verfügbarkeitsgruppe unterstützt einen Satz von Lese-und Schreib Primärdatenbanken sowie eine bis vier Gruppen entsprechender sekundärer Datenbanken.</span><span class="sxs-lookup"><span data-stu-id="c98bf-114">An availability group supports a set of read/write primary databases and one to four sets of corresponding secondary databases.</span></span> <span data-ttu-id="c98bf-115">Optional können sekundäre Datenbanken für schreibgeschützte Berechtigungen, einige Sicherungsvorgänge oder beides zur Verfügung gestellt werden.</span><span class="sxs-lookup"><span data-stu-id="c98bf-115">Optionally, secondary databases can be made available for read-only permission, some backup operations, or for both.</span></span>

<span data-ttu-id="c98bf-116">Informationen zum Einrichten von Verfügbarkeitsgruppen finden Sie unter [AlwaysOn-Verfügbarkeitsgruppen](https://go.microsoft.com/fwlink/?LinkId=393277).</span><span class="sxs-lookup"><span data-stu-id="c98bf-116">For information about how to set up availability groups, see [AlwaysOn Availability Groups](https://go.microsoft.com/fwlink/?LinkId=393277).</span></span>

## <a href="" id="bkmk-sql-clustering"></a><span data-ttu-id="c98bf-117">Microsoft SQL Server-Clustering</span><span class="sxs-lookup"><span data-stu-id="c98bf-117">Microsoft SQL Server clustering</span></span>


<span data-ttu-id="c98bf-118">Sie können die MBAM 2,5-Konformitäts-und Überwachungsdatenbank und die Wiederherstellungsdatenbank auf Computern ausführen, auf denen SQL Server-Cluster ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="c98bf-118">You can run the MBAM 2.5 Compliance and Audit Database and the Recovery Database on computers that are running SQL Server clusters.</span></span>

## <a href="" id="bkmk-load-balance"></a><span data-ttu-id="c98bf-119">IIS-Netzwerklastenausgleich</span><span class="sxs-lookup"><span data-stu-id="c98bf-119">IIS Network Load Balancing</span></span>


<span data-ttu-id="c98bf-120">Sie können den Netzwerklastenausgleich verwenden, um eine hoch verfügbare Umgebung für Computer zu konfigurieren, auf denen die Website Verwaltung und Überwachung (auch bekannt als Help Desk), das Self-Service-Portal und die Webdienste ausgeführt werden, die über Internet Informationsdienste (IIS) bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="c98bf-120">You can use Network Load Balancing to configure a highly available environment for computers that are running the Administration and Monitoring Website (also known as Help Desk), the Self-Service Portal, and the web services, which are deployed through Internet Information Services (IIS).</span></span>

### <span data-ttu-id="c98bf-121">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="c98bf-121">Prerequisites</span></span>

<span data-ttu-id="c98bf-122">Bevor Sie den Lastenausgleich konfigurieren, stellen Sie sicher, dass Sie die folgenden Voraussetzungen erfüllt haben:</span><span class="sxs-lookup"><span data-stu-id="c98bf-122">Before configuring load balancing, ensure that you have met the following prerequisites:</span></span>

-   <span data-ttu-id="c98bf-123">Es muss ein Lastenausgleichsmodul verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="c98bf-123">A load balancer must be available.</span></span> <span data-ttu-id="c98bf-124">Sie können Load-Balancer von Microsoft oder einem anderen Unternehmen verwenden.</span><span class="sxs-lookup"><span data-stu-id="c98bf-124">You can use load balancers from Microsoft or another company.</span></span> <span data-ttu-id="c98bf-125">Weitere Informationen zur Microsoft Load Balancer-Technologie finden Sie unter [Erstellen einer Webfarm mit IIS-Servern](https://go.microsoft.com/fwlink/?LinkId=393326).</span><span class="sxs-lookup"><span data-stu-id="c98bf-125">For more information about Microsoft load balancer technology, see [Build a Web Farm with IIS Servers](https://go.microsoft.com/fwlink/?LinkId=393326).</span></span>

-   <span data-ttu-id="c98bf-126">Mindestens zwei Server führen IIS aus und erfüllen alle MBAM-Voraussetzungen, um die WebFeatures, einschließlich ASP.NET MVC 4, zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="c98bf-126">At least two servers are running IIS and have met all of the MBAM prerequisites to support its web features, including ASP.NET MVC 4.</span></span>

-   <span data-ttu-id="c98bf-127">MBAM-Datenbanken und-Berichte werden auf einem Server ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c98bf-127">MBAM databases and reports are running on a server.</span></span>

### <a href="" id="-------------mbam-specific-changes-that-are-required-to-enable-load-balancing"></a> <span data-ttu-id="c98bf-128">MBAM-spezifische Änderungen, die erforderlich sind, um den Lastenausgleich zu aktivieren</span><span class="sxs-lookup"><span data-stu-id="c98bf-128">MBAM-specific changes that are required to enable Load Balancing</span></span>

<span data-ttu-id="c98bf-129">Führen Sie die folgenden Aufgaben aus:</span><span class="sxs-lookup"><span data-stu-id="c98bf-129">Complete the following tasks:</span></span>

1.  <span data-ttu-id="c98bf-130">Registrieren Sie einen Dienstprinzipalnamen (Service Principal Name, SPN) für den virtuellen Host Namen unter dem Domänenkonto, das Sie für die Webanwendungspools verwenden.</span><span class="sxs-lookup"><span data-stu-id="c98bf-130">Register a Service Principal Name (SPN) for the virtual host name under the domain account that you are using for the web application pools.</span></span> <span data-ttu-id="c98bf-131">Wenn beispielsweise der Name des virtuellen Hosts mbamvirtual.contoso.com ist und das für die Webanwendungspools verwendete Domänenkonto contoso\\mbamapppooluser ist, wird der SPN vom folgenden Befehl entsprechend registriert.</span><span class="sxs-lookup"><span data-stu-id="c98bf-131">For example, if the virtual host name is mbamvirtual.contoso.com, and the domain account used for the web application pools is contoso\\mbamapppooluser, the following command registers the SPN appropriately.</span></span>

    `Setspn -s http//mbamvirtual contoso\mbamapppooluser`

    `Setspn -s http//mbamvirtual.contoso.com contoso\mbamapppooluser`

2.  <span data-ttu-id="c98bf-132">Konfigurieren Sie die folgenden MBAM-WebFeatures:</span><span class="sxs-lookup"><span data-stu-id="c98bf-132">Configure the following MBAM web features:</span></span>

    -   <span data-ttu-id="c98bf-133">Verwenden Sie auf jedem Server, auf dem die MBAM-WebFeatures gehostet werden, das gleiche Domänenkonto für die administrativen Anmeldeinformationen des Anwendungspools.</span><span class="sxs-lookup"><span data-stu-id="c98bf-133">On each server that will host the MBAM web features, use the same domain account for the application pool administrative credentials.</span></span>

    -   <span data-ttu-id="c98bf-134">Geben Sie einen Hostnamen an, der dem virtuellen Hostnamen (DNS-Name) des lastenausgleichsclusters entspricht.</span><span class="sxs-lookup"><span data-stu-id="c98bf-134">Specify a host name that matches the virtual host name (DNS name) of the Load Balancing cluster.</span></span> <span data-ttu-id="c98bf-135">Wenn Sie beispielsweise MBAM auf einem Server namens "NLB1" mit einem virtuellen Hostnamen von **mbamvirtual.contoso.com**installieren, stellen Sie sicher, dass der Hostname, den Sie im Windows PowerShell-Cmdlet angeben, **mbamvirtual.contoso.com**ist.</span><span class="sxs-lookup"><span data-stu-id="c98bf-135">For example, when you install MBAM on a server called "NLB1" with a virtual host name of **mbamvirtual.contoso.com**, ensure that the host name that you specify in the Windows PowerShell cmdlet is **mbamvirtual.contoso.com**.</span></span>

3.  <span data-ttu-id="c98bf-136">Wenn Sie die Websites in einer Webfarm mit einem Lastenausgleichsmodul konfigurieren, müssen Sie die Websites so konfigurieren, dass derselbe Computerschlüssel verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c98bf-136">If you are configuring the websites in a web farm with a load balancer, you must configure the websites to use the same machine key.</span></span>

    <span data-ttu-id="c98bf-137">Weitere Informationen finden Sie in den folgenden Abschnitten im [machineKey-Element (ASP.net-Einstellungs Schema)](https://msdn.microsoft.com/library/vstudio/w8h3skw9.aspx):</span><span class="sxs-lookup"><span data-stu-id="c98bf-137">For more information, see the following sections in [machineKey Element (ASP.NET Settings Schema)](https://msdn.microsoft.com/library/vstudio/w8h3skw9.aspx):</span></span>

    -   <span data-ttu-id="c98bf-138">Computerschlüssel erläutert</span><span class="sxs-lookup"><span data-stu-id="c98bf-138">Machine Key Explained</span></span>

    -   <span data-ttu-id="c98bf-139">Überlegungen zur Webfarmbereitstellung</span><span class="sxs-lookup"><span data-stu-id="c98bf-139">Web Farm Deployment Considerations</span></span>

    <span data-ttu-id="c98bf-140">Anweisungen dazu, wie Sie einen Schlüssel automatisch generieren, finden Sie unter [Generieren eines Computerschlüssels (IIS 7.0)](https://technet.microsoft.com/library/cc772287.aspx).</span><span class="sxs-lookup"><span data-stu-id="c98bf-140">For instructions about how to automatically generate a key, see [Generate a Machine Key (IIS 7)](https://technet.microsoft.com/library/cc772287.aspx).</span></span>

<span data-ttu-id="c98bf-141">Die Informationen zum Lastenausgleich gelten auch für IIS-Netzwerklastenausgleichs-Cluster (NLB) in Windows Server 2012 oder Windows Server2008R2.</span><span class="sxs-lookup"><span data-stu-id="c98bf-141">The information about Load Balancing also applies to IIS Network Load Balancing (NLB) clusters in Windows Server 2012 or Windows Server2008R2.</span></span> <span data-ttu-id="c98bf-142">Die IIS-Netzwerklastenausgleich-Funktion in Windows Server 2012 ist in der Regel identisch mit der in Windows Server2008R2.</span><span class="sxs-lookup"><span data-stu-id="c98bf-142">The IIS Network Load Balancing functionality in Windows Server 2012 is generally the same as in Windows Server2008R2.</span></span> <span data-ttu-id="c98bf-143">Einige Aufgabendetails unterscheiden sich jedoch in Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="c98bf-143">However, some task details are different in Windows Server 2012.</span></span> <span data-ttu-id="c98bf-144">Informationen zu neuen Methoden für Aufgaben finden Sie unter [allgemeine Verwaltungsaufgaben und Navigation in Windows Server 2012 R2 Preview und Windows Server 2012](https://go.microsoft.com/fwlink/?LinkId=316371).</span><span class="sxs-lookup"><span data-stu-id="c98bf-144">For information about new ways to do tasks, see [Common Management Tasks and Navigation in Windows Server 2012 R2 Preview and Windows Server 2012](https://go.microsoft.com/fwlink/?LinkId=316371).</span></span>

## <a href="" id="bkmk-db-mirroring"></a><span data-ttu-id="c98bf-145">Datenbankspiegelung in SQL Server</span><span class="sxs-lookup"><span data-stu-id="c98bf-145">Database mirroring in SQL Server</span></span>


<span data-ttu-id="c98bf-146">MBAM unterstützt die Verwendung der SQL Server-Spiegelung, bei der die Kompatibilitäts-und Überwachungsdatenbank sowie die Wiederherstellungsdatenbank mithilfe von zwei Instanzen von SQL Server für jede Datenbank gespiegelt werden.</span><span class="sxs-lookup"><span data-stu-id="c98bf-146">MBAM supports the use of SQL Server mirroring, where the Compliance and Audit Database and the Recovery Database are mirrored by using two instances of SQL Server for each database.</span></span> <span data-ttu-id="c98bf-147">Beachten Sie vor der Implementierung der Spiegelung, dass die Spiegelung langsam ablaufen wird, zugunsten von Verfügbarkeitsgruppen, die weiter oben in diesem Thema erläutert werden.</span><span class="sxs-lookup"><span data-stu-id="c98bf-147">Before implementing mirroring, be aware that mirroring is slowly being phased out, in favor of availability groups, which are discussed earlier in this topic.</span></span>

<span data-ttu-id="c98bf-148">Zum Implementieren der Spiegelung für MBAM müssen Sie die entsprechenden Verbindungszeichenfolgen für die gespiegelte Datenbankkonfiguration mithilfe des Windows PowerShell-Cmdlets **enable-MbamWebApplication** angeben.</span><span class="sxs-lookup"><span data-stu-id="c98bf-148">To implement mirroring for MBAM, you must specify the appropriate connection strings for the mirrored database configuration by using the **Enable-MbamWebApplication** Windows PowerShell cmdlet.</span></span> <span data-ttu-id="c98bf-149">Weitere Informationen zu den MBAM 2,5 Windows PowerShell-Cmdlets finden Sie unter [Konfigurieren von MBAM 2,5-Server Features mithilfe von Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md).</span><span class="sxs-lookup"><span data-stu-id="c98bf-149">For more information about the MBAM 2.5 Windows PowerShell cmdlets, see [Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md).</span></span>

### <span data-ttu-id="c98bf-150">Beispiele für die Implementierung der SQL Server-Spiegelung mithilfe von Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="c98bf-150">Examples of implementing SQL Server mirroring by using Windows PowerShell</span></span>

<span data-ttu-id="c98bf-151">In den folgenden Beispielen wird gezeigt, wie Sie die SQL Server-Spiegelung mithilfe von Windows PowerShell-Cmdlets implementieren können.</span><span class="sxs-lookup"><span data-stu-id="c98bf-151">The following examples show how you might implement SQL Server mirroring by using Windows PowerShell cmdlets.</span></span>

**<span data-ttu-id="c98bf-152">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c98bf-152">Example 1</span></span>**

``` syntax
Enable-MbamWebApplication -AdministrationPortal -ComplianceAndAuditDBConnectionString 'Integrated Security=SSPI;Data Source=MyDatabaseServer;Failover Partner=myMirrorServerAddress;Initial Catalog="MBAM Compliance Status";' -RecoveryDBConnectionString 'Integrated Security=SSPI;Data Source=MyDatabaseServer;Failover Partner=myMirrorServerAddress;Initial Catalog="MBAM Recovery and Hardware";' -AdvancedHelpdeskAccessGroup “MyDomain\AdvancedUserGroup” -HelpdeskAccessGroup “MyDomain\StandardUserGroup” -ReportsReadOnlyAccessGroup "MyDomain\ReportUserGroup" -ReportUrl "https://MyReportServer/ReportServer" -Port 443 -WebServiceApplicationPoolCredential (Get-Credential) -Certificate (dir cert:\LocalMachine\My\E2A7EA5533890D6567E40DFC46F53B3D31D6B689)
```

**<span data-ttu-id="c98bf-153">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="c98bf-153">Example 2</span></span>**

``` syntax
Enable-MbamWebApplication -SelfServicePortal -ComplianceAndAuditDBConnectionString 'Integrated Security=SSPI;Data Source=MyDatabaseServer; Failover Partner=myMirrorServerAddress;Initial Catalog="MBAM Compliance Status";' -RecoveryDBConnectionString 'Integrated Security=SSPI;Data Source=MyDatabaseServer;I Failover Partner=myMirrorServerAddress;Initial Catalog="MBAM Recovery and Hardware";' -Port 443 -WebServiceApplicationPoolCredential (Get-Credential) -Certificate (dir cert:\LocalMachine\My\E2A7EA5533890D6567E40DFC46F53B3D31D6B689)
```

### <span data-ttu-id="c98bf-154">Weitere Informationen zur SQL Server-Spiegelung</span><span class="sxs-lookup"><span data-stu-id="c98bf-154">More information about SQL Server mirroring</span></span>

<span data-ttu-id="c98bf-155">Die folgenden Links enthalten weitere Informationen zum Konfigurieren der SQL Server-Spiegelung:</span><span class="sxs-lookup"><span data-stu-id="c98bf-155">The following links provide more information about configuring SQL Server mirroring:</span></span>

-   [<span data-ttu-id="c98bf-156">Vorgehensweise: Vorbereiten einer Spiegeldatenbank für die Spiegelung (Transact-SQL)</span><span class="sxs-lookup"><span data-stu-id="c98bf-156">How to: Prepare a Mirror Database for Mirroring (Transact-SQL)</span></span>](https://go.microsoft.com/fwlink/?LinkId=316375)

-   [<span data-ttu-id="c98bf-157">Einrichten einer Datenbankspiegelungssitzung mithilfe der Windows-Authentifizierung (SQL Server Management Studio)</span><span class="sxs-lookup"><span data-stu-id="c98bf-157">Establish a Database Mirroring Session Using Windows Authentication (SQL Server Management Studio)</span></span>](https://go.microsoft.com/fwlink/?LinkId=316377)

## <a href="" id="bkmk-vss"></a><span data-ttu-id="c98bf-158">Sichern von MBAM-Datenbanken mithilfe des Volumeschattenkopie-Diensts (Volume Shadow Copy Service, VSS)</span><span class="sxs-lookup"><span data-stu-id="c98bf-158">Backing up MBAM databases by using the Volume Shadow Copy Service (VSS)</span></span>


<span data-ttu-id="c98bf-159">MBAM stellt einen VSS-Writer (Volume Shadow Copy Service) bereit, der als Microsoft BitLocker-Verwaltungs-und-Verwaltungs-Writer bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="c98bf-159">MBAM provides a Volume Shadow Copy Service (VSS) writer, called the Microsoft BitLocker Administration and Management Writer.</span></span> <span data-ttu-id="c98bf-160">Dieser VSS-Writer vereinfacht die Sicherung der Konformitäts-und Überwachungsdatenbank sowie der Wiederherstellungsdatenbank.</span><span class="sxs-lookup"><span data-stu-id="c98bf-160">This VSS writer facilitates the backup of the Compliance and Audit Database and the Recovery Database.</span></span>

<span data-ttu-id="c98bf-161">Der VSS-Writer ist auf jedem Server registriert, auf dem Sie eine MBAM-Webanwendung aktivieren.</span><span class="sxs-lookup"><span data-stu-id="c98bf-161">The VSS writer is registered on every server where you enable an MBAM web application.</span></span> <span data-ttu-id="c98bf-162">Der MBAM-VSS-Writer hängt vom SQL Server VSS Writer ab, der als Teil der Microsoft SQL Server-Installation registriert ist.</span><span class="sxs-lookup"><span data-stu-id="c98bf-162">The MBAM VSS writer depends on the SQL Server VSS Writer, which is registered as part of the Microsoft SQL Server installation.</span></span> <span data-ttu-id="c98bf-163">Jede Sicherungstechnologie, die VSS-Writer zum Durchführen einer Sicherung verwendet, kann den MBAM VSS-Writer ermitteln.</span><span class="sxs-lookup"><span data-stu-id="c98bf-163">Any backup technology that uses VSS writers to perform backup can discover the MBAM VSS writer.</span></span>



## <span data-ttu-id="c98bf-164">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="c98bf-164">Related topics</span></span>


[<span data-ttu-id="c98bf-165">Planen der Bereitstellung von MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="c98bf-165">Planning to Deploy MBAM 2.5</span></span>](planning-to-deploy-mbam-25.md)

 

 
## <span data-ttu-id="c98bf-166">Sie haben einen Vorschlag für MBAM?</span><span class="sxs-lookup"><span data-stu-id="c98bf-166">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="c98bf-167">[Hier](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)können Sie Vorschläge hinzufügen oder abstimmen.</span><span class="sxs-lookup"><span data-stu-id="c98bf-167">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span>
- <span data-ttu-id="c98bf-168">Bei MBAM-Problemen verwenden Sie das [MBAM TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="c98bf-168">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>




