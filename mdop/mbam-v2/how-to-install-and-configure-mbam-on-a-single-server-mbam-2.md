---
title: So installieren und Konfigurieren von MBAM auf einem Server
description: So installieren und Konfigurieren von MBAM auf einem Server
author: dansimp
ms.assetid: 45e6a012-6c8c-4d90-902c-d09de9a0cbea
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4dffe2e2dcb82866b86a3ac281aca8a0dcaab686
ms.sourcegitcommit: 3e0500abde44d6a09c7ac8e3caf5e25929b490a4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2021
ms.locfileid: "11910660"
---
# <a name="how-to-install-and-configure-mbam-on-a-single-server"></a>So installieren und Konfigurieren von MBAM auf einem Server


In den Verfahren in diesem Thema wird beschrieben, wie Microsoft BitLocker Administration and Monitoring (MBAM) in der eigenständigen Topologie auf einem einzelnen Server installiert wird. Verwenden Sie die Konfiguration mit einem einzelnen Server nur in einer Testumgebung. Verwenden Sie für Produktionsumgebungen mindestens zwei Server. Wenn Sie die Microsoft BitLocker-Verwaltung und -Überwachung mithilfe der Configuration Manager-Topologie installieren, finden Sie weitere Informationen unter [Deploying MBAM with Configuration Manager.](deploying-mbam-with-configuration-manager-mbam2.md)

Das folgende Diagramm zeigt ein Beispiel für eine Architektur mit einem einzelnen Server. Eine Beschreibung der Datenbanken und Features finden Sie unter ["High-Level Architecture" für MBAM 2.0.](high-level-architecture-for-mbam-20-mbam-2.md)

![Mbam 2-Bereitstellungstopologie mit einem Einzelnen Server.](images/mbam2-1-server.gif)

Jedes Serverfeature hat bestimmte Voraussetzungen. Informationen dazu, ob sie die Voraussetzungen sowie die Hardware- und Softwareanforderungen erfüllt haben, finden Sie unter ["Mbam 2.0 Deployment Prerequisites"](mbam-20-deployment-prerequisites-mbam-2.md) und ["MBAM 2.0 Supported Configurations".](mbam-20-supported-configurations-mbam-2.md) Darüber hinaus verfügen einige Features auch über Informationen, die während des Installationsvorgangs bereitgestellt werden müssen, um das Feature erfolgreich bereitstellen zu können. Lesen Sie auch ["Vorbereiten der Umgebung für MBAM 2.0",](preparing-your-environment-for-mbam-20-mbam-2.md) bevor Sie mit der MBAM-Bereitstellung beginnen.

**Hinweis:**  
Um die Setupprotokolldateien abzurufen, verwenden Sie das **** Msiexec-Paket und die &lt; &gt; /L-Speicherortoption, um MBAM zu installieren. Protokolldateien werden an dem von Ihnen angegebenen Speicherort erstellt.

Zusätzliche Setupprotokolldateien werden im Ordner "%temp%" auf dem Server des Benutzers erstellt, der MBAM installiert.



## <a name="to-install-mbam-server-features-on-a-single-server"></a>So installieren Sie MBAM Server-Features auf einem einzelnen Server


In den folgenden Schritten wird beschrieben, wie allgemeine MBAM-Features installiert werden.

**So starten Sie die Installation der MBAM Server-Features**

1.  Führen Sie auf dem Server, auf dem Sie MBAM installieren möchten, **MBAMSetup.exe** aus, um den MBAM-Installations-Assistenten zu starten.

2.  Wählen Sie auf der **Willkommensseite** optional das Programm zur Verbesserung der **Benutzerfreundlichkeit**aus, und klicken Sie dann auf **"Start".**

3.  Lesen und akzeptieren Sie den Microsoft-Softwarelizenzvertrag, und klicken Sie dann auf **"Weiter",** um die Installation fortzusetzen.

4.  Wählen Sie auf der Seite **"Topologieauswahl"** die **eigenständige** Topologie aus, und klicken Sie dann auf **"Weiter".**

5.  Wählen Sie auf der Seite **"Zu installierende Features auswählen"** die Features aus, die Sie installieren möchten. Standardmäßig sind alle MBAM-Features für die Installation ausgewählt. Features, die auf demselben Computer installiert werden sollen, müssen gleichzeitig zusammen installiert werden. Deaktivieren Sie die Kontrollkästchen für alle Features, die Sie an anderer Stelle installieren möchten. Sie müssen MBAM-Features in der folgenden Reihenfolge installieren:

    -   Wiederherstellungsdatenbank

    -   Compliance- und Überwachungsdatenbank

    -   Compliance- und Überwachungsberichte

    -   Self-Service Server

    -   Verwaltungs- und Überwachungsserver

    -   MBAM-Gruppenrichtlinienvorlage

    **Hinweis:**  
    Der Installations-Assistent überprüft die Erforderlichen für Ihre Installation und zeigt die fehlenden Voraussetzungen an. Wenn alle Voraussetzungen erfüllt sind, wird die Installation fortgesetzt. Wenn eine fehlende Voraussetzung erkannt wird, müssen Sie die fehlenden Voraussetzungen beheben und dann erneut auf **"Voraussetzungen überprüfen"** klicken. Wenn dieses Mal alle Voraussetzungen erfüllt sind, wird die Installation fortgesetzt.



6.  Wählen Sie auf der Seite **"Netzwerkkommunikationssicherheit konfigurieren"** aus, ob die Kommunikation zwischen den Webdiensten auf dem Verwaltungs- und Überwachungsserver und den Clients verschlüsselt werden soll. Wenn Sie die Kommunikation verschlüsseln möchten, wählen Sie das Zertifikat aus, das von der Zertifizierungsstelle bereitgestellt wird, das für die Verschlüsselung verwendet werden soll. Das Zertifikat muss vor diesem Schritt erstellt werden, damit Sie es auf dieser Seite auswählen können.

    **Hinweis:**  
    Diese Seite wird nur angezeigt, wenn Sie das Self-Service Portal oder das Feature "Verwaltungs- und Überwachungsserver" auf der Seite **"Zu installierende Features auswählen"** ausgewählt haben.



7.  Klicken Sie auf **"Weiter",** und fahren Sie mit dem nächsten Schritt fort, um die MBAM-Serverfeatures zu konfigurieren.

**So konfigurieren Sie die MBAM Server-Features**

1.  Geben Sie auf der Seite **"Wiederherstellungsdatenbank konfigurieren"** den Namen SQL Server Instanz und den Namen der Datenbank an, in der die Wiederherstellungsdaten gespeichert werden. Außerdem müssen Sie angeben, wo sich die Datenbankdateien befinden und wo sich die Protokollinformationen befinden.

2.  Klicken Sie auf **Weiter**, um den Vorgang fortzusetzen.

3.  Geben Sie auf der Seite **"Compliance- und Überwachungsdatenbank konfigurieren"** den Namen SQL Server Instanz und den Namen der Datenbank an, in der die Konformitäts- und Überwachungsdaten gespeichert werden. Außerdem müssen Sie angeben, wo sich die Datenbankdateien befinden und wo sich die Protokollinformationen befinden.

4.  Klicken Sie auf **Weiter**, um den Vorgang fortzusetzen.

5.  Geben Sie auf der Seite **"Compliance- und Überwachungsberichte konfigurieren"** die SQL Server Reporting Services Instanz an, in der die Compliance- und Überwachungsberichte installiert werden, und geben Sie ein Domänenbenutzerkonto und ein Kennwort für den Zugriff auf die Compliance- und Überwachungsdatenbank an. Konfigurieren Sie das Kennwort für dieses Konto so, dass es nie abläuft. Das Benutzerkonto sollte in der Lage sein, auf alle Daten zuzugreifen, die für die Gruppe "BENUTZER von MBAM-Berichten" verfügbar sind.

6.  Klicken Sie auf **Weiter**, um den Vorgang fortzusetzen.

7.  Geben **Sie** auf der Seite Self-Service Portal konfigurieren die Portnummer, den Hostnamen, den Namen des virtuellen Verzeichnisses und den Installationspfad für das Self-Service Portal ein.

    **Hinweis:**  
    Die von Ihnen angegebene Portnummer muss eine nicht verwendete Portnummer auf dem Verwaltungs- und Überwachungsserver sein, es sei denn, Sie geben einen eindeutigen Hostheadernamen an. Wenn Sie Windows Firewall verwenden, wird der Port automatisch geöffnet.



8.  Klicken Sie auf **Weiter**, um den Vorgang fortzusetzen.

9.  Geben Sie an, ob Microsoft Updates verwendet werden soll, um die Sicherheit Ihres Computers zu gewährleisten, und klicken Sie dann auf **"Weiter".** Dadurch werden keine automatischen Updates in Windows aktiviert.

10. Geben Sie auf der Seite **"Verwaltungs- und Überwachungsserver konfigurieren"** die Portnummer, den Hostnamen, den Namen des virtuellen Verzeichnisses und den Installationspfad für die Helpdesk-Website ein.

    **Hinweis:**  
    Die von Ihnen angegebene Portnummer muss eine nicht verwendete Portnummer auf dem Verwaltungs- und Überwachungsserver sein, es sei denn, Sie geben einen eindeutigen Hostheadernamen an. Wenn Sie Windows Firewall verwenden, wird der Port automatisch geöffnet.



11. Überprüfen Sie auf der Seite **"Installationszusammenfassung"** die Liste der Features, die installiert werden sollen, und klicken Sie auf **"Installieren",** um mit der Installation der MBAM-Features zu beginnen. Klicken Sie auf **"Zurück",** um den Assistenten zu durchlaufen, wenn Sie ihre Installationseinstellungen überprüfen oder ändern müssen, oder klicken Sie auf **"Abbrechen",** um setup zu beenden. Setup installiert die MBAM-Features und benachrichtigt Sie, dass die Installation abgeschlossen ist.

12. Klicken Sie auf **Fertig stellen,** um den Assistenten zu beenden. Fahren Sie nach der Installation der Features von Microsoft BitLocker Administration and Monitoring Server mit dem nächsten Abschnitt fort, und führen Sie die Schritte aus, um den Microsoft BitLocker-Verwaltungs- und -Überwachungsrollen Benutzer hinzuzufügen. Weitere Informationen zu Rollen finden Sie unter [Planning for MBAM 2.0 Administrator Roles](planning-for-mbam-20-administrator-roles-mbam-2.md).

**So führen Sie die Konfiguration nach der Installation aus**

1.  Fügen Sie auf dem Verwaltungs- und Überwachungsserver Benutzer zu den folgenden lokalen Gruppen hinzu, um ihnen Zugriff auf die Features der MBAM-Helpdesk-Website zu gewähren:

    -   **MBAM-Helpdeskbenutzer:** Mitglieder dieser lokalen Gruppe können auf der Website für die MBAM-Verwaltung und -Überwachung auf die Tpm-Features für die Laufwerkwiederherstellung und -verwaltung zugreifen. Alle Felder in Drive Recovery und Manage TPM sind erforderliche Felder für einen Helpdesk-Benutzer.

    -   **MBAM Advanced Helpdesk-Benutzer:** Mitglieder dieser lokalen Gruppe haben erweiterten Zugriff auf die Drive Recovery and Manage TPM-Features auf der MBAM-Verwaltungs- und Überwachungswebsite. Für erweiterte Helpdesk-Benutzer ist in der Laufwerkwiederherstellung nur das **Schlüssel-ID-Feld** erforderlich. In "TPM verwalten" sind nur das Feld **"Computerdomäne"** und **"Computername"** erforderlich.

2.  Fügen Sie auf dem Verwaltungs- und Überwachungsserver der folgenden lokalen Gruppe Benutzer hinzu, damit sie auf der Website für MBAM-Verwaltung und -Überwachung auf das Feature "Berichte" zugreifen können:

    -   **MBAM-Berichtsbenutzer:** Mitglieder dieser lokalen Gruppe können auf die Berichtsfeatures auf der Mbam-Verwaltungs- und Überwachungswebsite zugreifen.

    -   Branding des Self-Service-Portals mit Ihrem Firmennamen, Benachrichtigungstext und anderen unternehmensspezifischen Informationen. Anweisungen finden Sie unter [How to Branding the Self-Service Portal](how-to-brand-the-self-service-portal.md).

    **Hinweis:**  
    Identische Benutzer- oder Gruppenmitgliedschaften der lokalen Gruppe **"MBAM-Berichtbenutzer"** müssen auf allen Computern verwaltet werden, auf denen die MbaM-Verwaltungs- und Überwachungsserverfeatures, die Compliance- und Überwachungsdatenbank sowie Die Compliance- und Überwachungsberichte installiert sind. Die empfohlene Vorgehensweise besteht darin, eine Domänensicherheitsgruppe zu erstellen und diese Domänengruppe jeder lokalen GRUPPE "MBAM-Berichtsbenutzer" hinzuzufügen. Wenn Sie diesen Prozess verwenden, verwalten Sie die Gruppenmitgliedschaften über die Domänengruppe.



## <a name="validating-the-mbam-server-feature-installation"></a>Überprüfen der MBAM Server-Featureinstallation


Überprüfen Sie nach Abschluss der Installation der Microsoft BitLocker-Verwaltung und -Überwachung, ob die Installation alle erforderlichen MBAM-Features, die für die BitLocker-Verwaltung erforderlich sind, erfolgreich eingerichtet hat. Verwenden Sie das folgende Verfahren, um zu überprüfen, ob der MBAM-Dienst funktionsfähig ist.

**So überprüfen Sie die MBAM Server-Featureinstallation**

1. Öffnen Sie auf jedem Server, auf dem ein MBAM-Feature bereitgestellt wird, **die Systemsteuerung.** Wählen Sie **"Programme"** und dann **"Programme und Features"** aus. Stellen Sie sicher, dass die **Microsoft BitLocker-Verwaltung und -Überwachung** in der Liste **"Programme und Features"** angezeigt wird.

   **Hinweis:**  
   Um die Installation zu überprüfen, müssen Sie ein Domänenkonto verwenden, das über Administratoranmeldeinformationen für den lokalen Computer auf jedem Server verfügt.



2. Öffnen Sie auf dem Server, auf dem die Wiederherstellungsdatenbank installiert ist, SQL Server Management Studio, und stellen Sie sicher, dass die **MBAM-Wiederherstellungs- und Hardwaredatenbank** installiert ist.

3. Öffnen Sie auf dem Server, auf dem die Compliance- und Überwachungsdatenbank installiert ist, SQL Server Management Studio, und überprüfen Sie, ob die **MBAM-Konformitätsstatusdatenbank** installiert ist.

4. Öffnen Sie auf dem Server, auf dem die Compliance- und Überwachungsberichte installiert sind, einen Webbrowser mit Administratoranmeldeinformationen, und navigieren Sie zur Startseite der SQL Server Reporting Services Website.

   Der Standardmäßige Startspeicherort einer SQL Server Reporting Services Websiteinstanz befindet sich unter http:// <em> &lt; NameofMBAMReportsServer &gt; </em> /Reports. Um die tatsächliche URL zu finden, verwenden Sie das Configuration Manager-Tool für Reporting Services, und wählen Sie die Instanzen aus, die während des Setups angegeben werden.

   Vergewissern Sie sich, dass der Ordner "Berichte" mit dem Namen "Microsoft BitLocker Administration and Monitoring" eine Datenquelle namens **"DezimalDataSource"** enthält und dass ein **"en-us"-Ordner** vier Berichte enthält.

   **Hinweis:**  
   Wenn SQL Server Reporting Services als benannte Instanz konfiguriert wurde, sollte die URL wie folgt aussehen: http://* &lt; NameofMBAMReportsServer &gt; */Reports\_* &lt; SRSInstanceName &gt; *



~~~
**Note**  
If SSRS was not configured to use Secure Socket Layer (SSL), the URL for the reports will be set to HTTP instead of HTTPS when you install the MBAM Server. If you then go to the Administration and Monitoring website and select a report, the following message appears: “Only Secure Content is Displayed.” To show the report, click **Show All Content**.
~~~



5. Führen Sie auf dem Server, auf dem das Verwaltungs- und Überwachungsfeature installiert ist, **den Server-Manager aus,** und navigieren Sie zu **"Rollen".** Wählen Sie **Webserver (IIS)** aus, und klicken Sie dann auf **Internetinformationsdienste (IIS)-Manager.**

6. Navigieren Sie in **"Verbindungen"** zu * &lt; &gt; "Computername",* wählen Sie **"Websites"** und dann **"Microsoft BitLocker-Verwaltung und -Überwachung"** aus. Stellen Sie sicher, dass **MBAMAdministrationService**, **MBAMUserSupportService**, **MBAMComplianceStatusService**und **MBAMRecoveryAndHardwareService** aufgeführt sind.

7. Öffnen Sie auf dem Server, auf dem die Verwaltungs- und Überwachungsfeatures und Self-Service Portal installiert sind, einen Webbrowser mit Administratoranmeldeinformationen, und navigieren Sie zu den folgenden Speicherorten, um zu überprüfen, ob sie erfolgreich geladen wurden:

   -   *http:// &lt; Hostname &gt; /HelpDesk/default.aspx* und bestätigen Sie jeden der Links für Navigation und Berichte.

   -   *http:// &lt; Hostname &gt; /SelfService&gt;/*

   -   *http:// &lt; Computername &gt; /MBAMAdministrationService/AdministrationService.svc*

   -   *http:// &lt; Hostname &gt; /MBAMUserSupportService/UserSupportService.svc*

   -   *http:// &lt; Computername &gt; /MBAMComplianceStatusService/StatusReportingService.svc*

   -   *http:// &lt; Computername &gt; /MBAMRecoveryAndHardwareService/CoreService.svc*

   **Hinweis:**  
   Es wird davon ausgegangen, dass die Serverfeatures auf dem Standardport ohne Netzwerkverschlüsselung installiert wurden. Wenn Sie die Serverfeatures auf einem anderen Port oder virtuellen Verzeichnis installiert haben, ändern Sie die URLs so, dass sie den entsprechenden Port enthalten, z. *B. http:// &lt; Hostname &gt; : Port &lt; &gt; /HelpDesk/default.asp*x oder*http:// &lt; &gt; Hostname: port &lt; &gt; / &lt; virtualdirectory &gt; /default.aspx*

   Wenn die Serverfeatures mit Netzwerkverschlüsselung installiert wurden, ändern Sie http:// in https://.



## <a name="related-topics"></a>Verwandte Themen


[Bereitstellen der Serverinfrastruktur von MBAM 2.0](deploying-the-mbam-20-server-infrastructure-mbam-2.md)









