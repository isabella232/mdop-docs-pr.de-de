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
# Überprüfen der Konfiguration von MBAM 2.5 Serverfunktionen


Wenn Sie die Bereitstellung der Microsoft BitLocker-Verwaltungs-und-Überwachungsfunktion (MBAM) 2,5 Server abgeschlossen haben, empfiehlt es sich, die Bereitstellung zu überprüfen, um sicherzustellen, dass alle Features erfolgreich konfiguriert wurden. Verwenden Sie das Verfahren, das der von Ihnen bereitgestellten Topologie (eigenständige oder System Center Configuration Manager-Integration) entspricht.

## Überprüfen der MBAM-Server Bereitstellung mit der eigenständigen Topologie


Führen Sie die folgenden Schritte aus, um die Bereitstellung Ihres MBAM-Servers mit der eigenständigen Topologie zu überprüfen.

**So überprüfen Sie eine eigenständige MBAM-Server Bereitstellung**

1.  Klicken Sie auf jedem Server, auf dem ein MBAM- **Control Panel** Feature bereitgestellt wird, auf Programme &gt; **Programs** &gt; **und Funktionen**der Systemsteuerung. Überprüfen Sie, ob die **Microsoft BitLocker-Verwaltung und-Überwachung** in der Liste " **Programme und Features** " angezeigt wird.

    **Hinweis:**  
    Um die Überprüfung durchführen zu können, müssen Sie ein Domänenkonto verwenden, das auf jedem Server über Administratoranmeldeinformationen des lokalen Computers verfügt.



2.  Öffnen Sie auf dem Server, auf dem die Wiederherstellungsdatenbank konfiguriert ist, SQL Server Management Studio, und überprüfen Sie, ob die **MBAM-Wiederherstellungs-und-Hardware** Datenbank konfiguriert ist.

3.  Öffnen Sie auf dem Server, auf dem die Konformitäts-und Überwachungsdatenbank konfiguriert ist, SQL Server Management Studio, und überprüfen Sie, ob die **MBAM-Konformitäts Status Datenbank** konfiguriert ist.

4.  Öffnen Sie auf dem Server, auf dem das Feature Berichte konfiguriert ist, einen Webbrowser mit administrativen Anmeldeinformationen, und navigieren Sie zu "Start" der SQL Server Reporting Services-Website.

    Der standardmäßige Startspeicherort einer SQL Server Reporting Services-Websiteinstanz lautet:

    http (s):// &lt; *MBAMReportsServerName* &gt; : &lt; *Port* &gt; /Reports.aspx

    Um die tatsächliche URL zu finden, verwenden Sie das Reporting Services-Konfigurations-Manager-Tool, und wählen Sie die Instanzen aus, die Sie während der Installation angegeben haben.

5.  Vergewissern Sie sich, dass ein Berichtsordner mit dem Namen **Microsoft BitLocker-Verwaltung und-Überwachung** eine Datenquelle mit dem Namen **MaltaDataSource** und die Sprachordner enthält. Die Datenquelle enthält Ordner mit Namen, die Sprachen darstellen (beispielsweise "en-US"). Die Berichte befinden sich in den Sprachordnern.

    **Hinweis:**  
    Wenn SQL Server Reporting Services (SSRS) als benannte Instanz konfiguriert wurde, sollte die URL wie folgt aussehen: http (s):// &lt; *MBAMReportsServerName* &gt; : &lt; *Port* &gt; /Reports\_ &lt; *SSRSInstanceName*&gt;



~~~
**Note**  
If SSRS was not configured to use Secure Socket Layer (SSL), the URL for the reports will be set to HTTP instead of HTTPS when you install the MBAM Server. If you then go to the Administration and Monitoring Website (also known as Help Desk) and select a report, the following message appears: "Only Secure Content is Displayed." To show the report, click **Show All Content**.
~~~



6. Führen Sie auf dem Server, auf dem die Verwaltungs-und Überwachungs Website-Funktion konfiguriert ist, den **Server-Manager**aus, navigieren Sie zu **Rollen**, und wählen Sie dann **Web Server (** IIS) &gt; **Internetinformationsdienste (IIS)-Manager**aus.

7. Navigieren Sie in **Verbindungen**zu * &lt; Computername &gt; * , und wählen Sie **Websites** &gt; **Microsoft BitLocker-Verwaltung und-Überwachung**aus. Überprüfen Sie, ob die folgenden Angaben aufgeführt sind:

   -   **MBAMAdministrationService**

   -   **MBAMComplianceStatusService**

   -   **MBAMRecoveryAndHardwareService**

8. Öffnen Sie auf dem Server, auf dem die Verwaltungs-und Überwachungs Website sowie das Self-Service-Portal konfiguriert sind, einen Webbrowser mit administrativen Anmeldeinformationen.

9. Navigieren Sie zu den folgenden Websites, um sicherzustellen, dass Sie erfolgreich geladen werden:

   -   HTTPS (s):// &lt; *MBAMAdministrationServerName* &gt; : &lt; *Port* &gt; /Helpdesk/– bestätigen Sie die einzelnen Links für Navigation und Berichte.

   -   http (s):// &lt; *MBAMAdministrationServerName* &gt; : &lt; *Port* &gt; /Selfservice/

   **Hinweis:**  
   Es wird davon ausgegangen, dass Sie die Server Features auf dem Standardport ohne Netzwerk Verschlüsselung konfiguriert haben. Wenn Sie die Server Features in einem anderen Port oder virtuellen Verzeichnis konfiguriert haben, ändern Sie die URLs so, dass Sie den entsprechenden Port umfassen, beispielsweise:

   http (s):// &lt; *Hostname* &gt; : &lt; *Port* &gt; /Helpdesk/

   http (s):// &lt; *Hostname* &gt; : &lt; *Port* &gt; / &lt; *VirtualDirectory*&gt;/

   Wenn die Server Features mit Netzwerk Verschlüsselung konfiguriert wurden, ändern Sie http://in https://.



10. Navigieren Sie zu den folgenden Webdiensten, um sicherzustellen, dass Sie erfolgreich geladen werden. Eine Seite wird geöffnet, um anzugeben, dass der Dienst ausgeführt wird, aber auf der Seite werden keine Metadaten angezeigt.

    -   http (s):// &lt; *MBAMAdministrationServerName* &gt; : &lt; *Port* &gt; /MBAMAdministrationService/AdministrationService.svc

    -   http (s):// &lt; *MBAMAdministrationServerName* &gt; : &lt; *Port* &gt; /MBAMUserSupportService/UserSupportService.svc

    -   http (s):// &lt; *MBAMAdministrationServerName* &gt; : &lt; *Port* &gt; /MBAMComplianceStatusService/StatusReportingService.svc

    -   http (s):// &lt; *MBAMAdministrationServerName* &gt; : &lt; *Port* &gt; /MBAMRecoveryAndHardwareService/CoreService.svc

## Überprüfen der MBAM-Server Bereitstellung mit der Configuration Manager-Integrations Topologie


Führen Sie die folgenden Schritte aus, um Ihre MBAM-Bereitstellung mit der Configuration Manager-Integrations Topologie zu überprüfen. Führen Sie die Validierungsschritte aus, die der von Ihnen verwendeten Version von Configuration Manager entsprechen.

### <a href="" id="validating-the-mbam-server-deployment-with-system-center-2012-configuration-manager-"></a>Überprüfen der MBAM-Server Bereitstellung mit dem System Center 2012-Konfigurations-Manager

Führen Sie die folgenden Schritte aus, um Ihre MBAM-Server Bereitstellung zu überprüfen, wenn Sie MBAM mit dem System Center 2012-Konfigurations-Manager verwenden.

**So überprüfen Sie eine Configuration Manager-Integrations MBAM Server Bereitstellung – System Center 2012-Konfigurations-Manager**

1.  Öffnen Sie auf dem Server, auf dem System Center 2012 Configuration Manager bereitgestellt wird, **Programme und Funktionen** **in der Systemsteuerung,** und überprüfen Sie, ob die **Microsoft BitLocker-Verwaltung und-Überwachung** angezeigt wird.

    **Hinweis:**  
    Um die Konfiguration zu überprüfen, müssen Sie ein Domänenkonto verwenden, das über lokale Computeradministrator Anmeldeinformationen auf jedem Server verfügt.



2.  Klicken Sie in der Configuration Manager-Konsole auf die gerätesammlungen für den **Ressourcen-und Compliance** -Arbeitsbereich &gt; **Device Collections**, und vergewissern Sie sich, dass eine neue Sammlung mit dem Namen **MBAM unterstützte Computer** angezeigt wird.

3.  Klicken Sie **in der Configuration** Manager-Konsole auf das &gt; **MBAM Bericht Erstellungs** &gt; **Berichte** für Arbeitsbereiche &gt; **MBAM**.

4.  Überprüfen Sie, ob der **MBAM** -Ordner Unterordner mit Namen enthält, die verschiedene Sprachen darstellen, und dass die folgenden Berichte in jedem Unterordner "Sprache" aufgeführt sind:

    -   BitLocker-Computer Konformität

    -   BitLocker Enterprise Compliance-Dashboard

    -   Details zur BitLocker-Unternehmenskonformität

    -   Zusammenfassung der BitLocker-Unternehmenskonformität

5.  Klicken Sie in der Configuration Manager-Konsole **Assets and Compliance** auf die Konfigurationsbasislinien für Compliance-Einstellungen des Arbeitsbereichs &gt; **Compliance Settings** &gt; **Configuration Baselines**, und vergewissern Sie sich, dass der BitLocker-Konfigurationsbasislinien- **Schutz** aufgeführt ist.

6.  Klicken Sie in der Configuration Manager-Konsole auf die Konfigurationselemente für Compliance-Einstellungen für **den Arbeitsbereich** &gt; **Compliance Settings** &gt; **Configuration Items**, und vergewissern Sie sich, dass die folgenden neuen Konfigurationselemente angezeigt werden:

    -   BitLocker-Datenlaufwerke mit fester Datensicherheit

    -   BitLocker-Betriebs System-Laufwerkschutz

### Überprüfen der MBAM-Server Bereitstellung mit Configuration Manager 2007

Führen Sie die folgenden Schritte aus, um Ihre MBAM-Server Bereitstellung zu überprüfen, wenn Sie MBAM mit Configuration Manager 2007 verwenden.

**So überprüfen Sie eine Configuration Manager-Integrations MBAM Server Bereitstellung – Configuration Manager 2007**

1.  Öffnen Sie auf dem Server, auf dem Configuration Manager 2007 bereitgestellt wird, **Programme und Funktionen** in der **System** Steuerung, und überprüfen Sie, ob die **Microsoft BitLocker-Verwaltung und-Überwachung** angezeigt wird.

    **Hinweis:**  
    Um die Konfiguration zu überprüfen, müssen Sie ein Domänenkonto verwenden, das über lokale Computeradministrator Anmeldeinformationen auf jedem Server verfügt.



2.  Klicken Sie in der Configuration Manager-Konsole auf **Website Datenbank &lt; SiteCode &gt;  -  &lt; Servername, Sitename &gt; &lt; &gt; ), Computer Verwaltung**, und vergewissern Sie sich, dass eine neue Sammlung mit dem Namen **MBAM unterstützte Computer** angezeigt wird.

3.  Klicken Sie in der Configuration Manager-Konsole auf **Reporting** &gt; **Services** &gt; ** \\\\ &lt; Servername &gt; ** &gt; **Report Folders** &gt; **MBAM**.

    Überprüfen Sie, ob der **MBAM** -Ordner Unterordner mit Namen enthält, die verschiedene Sprachen darstellen, und dass die folgenden Berichte in jedem Unterordner "Sprache" aufgeführt sind:

    -   BitLocker-Computer Konformität

    -   BitLocker Enterprise Compliance-Dashboard

    -   Details zur BitLocker-Unternehmenskonformität

    -   Zusammenfassung der BitLocker-Unternehmenskonformität

4.  Klicken Sie in der Configuration Manager- **Desired Configuration Management** Konsole auf &gt; **Konfigurationsbasislinien**für die gewünschte Konfigurationsverwaltung, und vergewissern Sie sich, dass der **BitLocker** -Konfigurationsbasislinien-Schutz aufgelistet ist.

5.  Klicken Sie in der Configuration Manager- **Desired Configuration Management** Konsole auf &gt; **Konfigurationselemente**für die Verwaltung der gewünschten Konfiguration, und vergewissern Sie sich, dass die folgenden neuen Konfigurationselemente angezeigt werden:

    -   BitLocker-Datenlaufwerke mit fester Datensicherheit

    -   BitLocker-Betriebs System-Laufwerkschutz



## Verwandte Themen


[Konfigurieren der MBAM 2.5-Serverfunktionen](configuring-the-mbam-25-server-features.md)


## Sie haben einen Vorschlag für MBAM?
- [Hier](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)können Sie Vorschläge hinzufügen oder abstimmen. 
- Bei MBAM-Problemen verwenden Sie das [MBAM TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).






