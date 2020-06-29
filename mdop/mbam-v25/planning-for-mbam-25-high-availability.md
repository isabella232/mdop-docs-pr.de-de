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
# Planen der hohen Verfügbarkeit von MBAM 2.5


Die Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) kann eine höhere Verfügbarkeit durch Verwendung einer oder mehrerer der folgenden Technologien gewährleisten, die in den folgenden Abschnitten beschrieben werden:

-   [Verfügbarkeitsgruppen für SQL Server-AlwaysOn](#bkmk-alwayson)

-   [Microsoft SQL Server-Clustering](#bkmk-sql-clustering)

-   [IIS-Netzwerklastenausgleich](#bkmk-load-balance)

-   [Datenbankspiegelung in SQL Server](#bkmk-db-mirroring)

-   [Sichern von MBAM-Datenbanken mithilfe des Volumeschattenkopie-Diensts (Volume Shadow Copy Service, VSS)](#bkmk-vss)

Verwenden Sie die Informationen in den folgenden Abschnitten, damit Sie die Optionen zum Bereitstellen von MBAM in einer hoch verfügbaren Konfiguration verstehen können.

## <a href="" id="bkmk-alwayson"></a>Unterstützung für SQL Server AlwaysOn-Verfügbarkeitsgruppen


MBAM ermöglicht es Ihnen, Verfügbarkeitsgruppen für die Datenbanken in Microsoft SQL Server zu konfigurieren und zu verwalten. Eine verfügbarkeitsgruppe für MBAM unterstützt eine Failover-Umgebung, in der die Konformitäts-und Überwachungsdatenbank und die Wiederherstellungsdatenbank nicht mehr einzeln, sondern gemeinsam ausgeführt werden.

Eine verfügbarkeitsgruppe unterstützt einen Satz von Lese-und Schreib Primärdatenbanken sowie eine bis vier Gruppen entsprechender sekundärer Datenbanken. Optional können sekundäre Datenbanken für schreibgeschützte Berechtigungen, einige Sicherungsvorgänge oder beides zur Verfügung gestellt werden.

Informationen zum Einrichten von Verfügbarkeitsgruppen finden Sie unter [AlwaysOn-Verfügbarkeitsgruppen](https://go.microsoft.com/fwlink/?LinkId=393277).

## <a href="" id="bkmk-sql-clustering"></a>Microsoft SQL Server-Clustering


Sie können die MBAM 2,5-Konformitäts-und Überwachungsdatenbank und die Wiederherstellungsdatenbank auf Computern ausführen, auf denen SQL Server-Cluster ausgeführt werden.

## <a href="" id="bkmk-load-balance"></a>IIS-Netzwerklastenausgleich


Sie können den Netzwerklastenausgleich verwenden, um eine hoch verfügbare Umgebung für Computer zu konfigurieren, auf denen die Website Verwaltung und Überwachung (auch bekannt als Help Desk), das Self-Service-Portal und die Webdienste ausgeführt werden, die über Internet Informationsdienste (IIS) bereitgestellt werden.

### Voraussetzungen

Bevor Sie den Lastenausgleich konfigurieren, stellen Sie sicher, dass Sie die folgenden Voraussetzungen erfüllt haben:

-   Es muss ein Lastenausgleichsmodul verfügbar sein. Sie können Load-Balancer von Microsoft oder einem anderen Unternehmen verwenden. Weitere Informationen zur Microsoft Load Balancer-Technologie finden Sie unter [Erstellen einer Webfarm mit IIS-Servern](https://go.microsoft.com/fwlink/?LinkId=393326).

-   Mindestens zwei Server führen IIS aus und erfüllen alle MBAM-Voraussetzungen, um die WebFeatures, einschließlich ASP.NET MVC 4, zu unterstützen.

-   MBAM-Datenbanken und-Berichte werden auf einem Server ausgeführt.

### <a href="" id="-------------mbam-specific-changes-that-are-required-to-enable-load-balancing"></a> MBAM-spezifische Änderungen, die erforderlich sind, um den Lastenausgleich zu aktivieren

Führen Sie die folgenden Aufgaben aus:

1.  Registrieren Sie einen Dienstprinzipalnamen (Service Principal Name, SPN) für den virtuellen Host Namen unter dem Domänenkonto, das Sie für die Webanwendungspools verwenden. Wenn beispielsweise der Name des virtuellen Hosts mbamvirtual.contoso.com ist und das für die Webanwendungspools verwendete Domänenkonto contoso\\mbamapppooluser ist, wird der SPN vom folgenden Befehl entsprechend registriert.

    `Setspn -s http//mbamvirtual contoso\mbamapppooluser`

    `Setspn -s http//mbamvirtual.contoso.com contoso\mbamapppooluser`

2.  Konfigurieren Sie die folgenden MBAM-WebFeatures:

    -   Verwenden Sie auf jedem Server, auf dem die MBAM-WebFeatures gehostet werden, das gleiche Domänenkonto für die administrativen Anmeldeinformationen des Anwendungspools.

    -   Geben Sie einen Hostnamen an, der dem virtuellen Hostnamen (DNS-Name) des lastenausgleichsclusters entspricht. Wenn Sie beispielsweise MBAM auf einem Server namens "NLB1" mit einem virtuellen Hostnamen von **mbamvirtual.contoso.com**installieren, stellen Sie sicher, dass der Hostname, den Sie im Windows PowerShell-Cmdlet angeben, **mbamvirtual.contoso.com**ist.

3.  Wenn Sie die Websites in einer Webfarm mit einem Lastenausgleichsmodul konfigurieren, müssen Sie die Websites so konfigurieren, dass derselbe Computerschlüssel verwendet wird.

    Weitere Informationen finden Sie in den folgenden Abschnitten im [machineKey-Element (ASP.net-Einstellungs Schema)](https://msdn.microsoft.com/library/vstudio/w8h3skw9.aspx):

    -   Computerschlüssel erläutert

    -   Überlegungen zur Webfarmbereitstellung

    Anweisungen dazu, wie Sie einen Schlüssel automatisch generieren, finden Sie unter [Generieren eines Computerschlüssels (IIS 7.0)](https://technet.microsoft.com/library/cc772287.aspx).

Die Informationen zum Lastenausgleich gelten auch für IIS-Netzwerklastenausgleichs-Cluster (NLB) in Windows Server 2012 oder Windows Server2008R2. Die IIS-Netzwerklastenausgleich-Funktion in Windows Server 2012 ist in der Regel identisch mit der in Windows Server2008R2. Einige Aufgabendetails unterscheiden sich jedoch in Windows Server 2012. Informationen zu neuen Methoden für Aufgaben finden Sie unter [allgemeine Verwaltungsaufgaben und Navigation in Windows Server 2012 R2 Preview und Windows Server 2012](https://go.microsoft.com/fwlink/?LinkId=316371).

## <a href="" id="bkmk-db-mirroring"></a>Datenbankspiegelung in SQL Server


MBAM unterstützt die Verwendung der SQL Server-Spiegelung, bei der die Kompatibilitäts-und Überwachungsdatenbank sowie die Wiederherstellungsdatenbank mithilfe von zwei Instanzen von SQL Server für jede Datenbank gespiegelt werden. Beachten Sie vor der Implementierung der Spiegelung, dass die Spiegelung langsam ablaufen wird, zugunsten von Verfügbarkeitsgruppen, die weiter oben in diesem Thema erläutert werden.

Zum Implementieren der Spiegelung für MBAM müssen Sie die entsprechenden Verbindungszeichenfolgen für die gespiegelte Datenbankkonfiguration mithilfe des Windows PowerShell-Cmdlets **enable-MbamWebApplication** angeben. Weitere Informationen zu den MBAM 2,5 Windows PowerShell-Cmdlets finden Sie unter [Konfigurieren von MBAM 2,5-Server Features mithilfe von Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md).

### Beispiele für die Implementierung der SQL Server-Spiegelung mithilfe von Windows PowerShell

In den folgenden Beispielen wird gezeigt, wie Sie die SQL Server-Spiegelung mithilfe von Windows PowerShell-Cmdlets implementieren können.

**Beispiel 1**

``` syntax
Enable-MbamWebApplication -AdministrationPortal -ComplianceAndAuditDBConnectionString 'Integrated Security=SSPI;Data Source=MyDatabaseServer;Failover Partner=myMirrorServerAddress;Initial Catalog="MBAM Compliance Status";' -RecoveryDBConnectionString 'Integrated Security=SSPI;Data Source=MyDatabaseServer;Failover Partner=myMirrorServerAddress;Initial Catalog="MBAM Recovery and Hardware";' -AdvancedHelpdeskAccessGroup “MyDomain\AdvancedUserGroup” -HelpdeskAccessGroup “MyDomain\StandardUserGroup” -ReportsReadOnlyAccessGroup "MyDomain\ReportUserGroup" -ReportUrl "https://MyReportServer/ReportServer" -Port 443 -WebServiceApplicationPoolCredential (Get-Credential) -Certificate (dir cert:\LocalMachine\My\E2A7EA5533890D6567E40DFC46F53B3D31D6B689)
```

**Beispiel 2**

``` syntax
Enable-MbamWebApplication -SelfServicePortal -ComplianceAndAuditDBConnectionString 'Integrated Security=SSPI;Data Source=MyDatabaseServer; Failover Partner=myMirrorServerAddress;Initial Catalog="MBAM Compliance Status";' -RecoveryDBConnectionString 'Integrated Security=SSPI;Data Source=MyDatabaseServer;I Failover Partner=myMirrorServerAddress;Initial Catalog="MBAM Recovery and Hardware";' -Port 443 -WebServiceApplicationPoolCredential (Get-Credential) -Certificate (dir cert:\LocalMachine\My\E2A7EA5533890D6567E40DFC46F53B3D31D6B689)
```

### Weitere Informationen zur SQL Server-Spiegelung

Die folgenden Links enthalten weitere Informationen zum Konfigurieren der SQL Server-Spiegelung:

-   [Vorgehensweise: Vorbereiten einer Spiegeldatenbank für die Spiegelung (Transact-SQL)](https://go.microsoft.com/fwlink/?LinkId=316375)

-   [Einrichten einer Datenbankspiegelungssitzung mithilfe der Windows-Authentifizierung (SQL Server Management Studio)](https://go.microsoft.com/fwlink/?LinkId=316377)

## <a href="" id="bkmk-vss"></a>Sichern von MBAM-Datenbanken mithilfe des Volumeschattenkopie-Diensts (Volume Shadow Copy Service, VSS)


MBAM stellt einen VSS-Writer (Volume Shadow Copy Service) bereit, der als Microsoft BitLocker-Verwaltungs-und-Verwaltungs-Writer bezeichnet wird. Dieser VSS-Writer vereinfacht die Sicherung der Konformitäts-und Überwachungsdatenbank sowie der Wiederherstellungsdatenbank.

Der VSS-Writer ist auf jedem Server registriert, auf dem Sie eine MBAM-Webanwendung aktivieren. Der MBAM-VSS-Writer hängt vom SQL Server VSS Writer ab, der als Teil der Microsoft SQL Server-Installation registriert ist. Jede Sicherungstechnologie, die VSS-Writer zum Durchführen einer Sicherung verwendet, kann den MBAM VSS-Writer ermitteln.



## Verwandte Themen


[Planen der Bereitstellung von MBAM 2.5](planning-to-deploy-mbam-25.md)

 

 
## Sie haben einen Vorschlag für MBAM?
- [Hier](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)können Sie Vorschläge hinzufügen oder abstimmen.
- Bei MBAM-Problemen verwenden Sie das [MBAM TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).




