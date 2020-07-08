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
ms.openlocfilehash: 53e170f421bdce8dd6f771af3902af627a15a085
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810333"
---
# So installieren und Konfigurieren von MBAM auf einem Server


In den Verfahren in diesem Thema wird beschrieben, wie Sie die Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) in der eigenständigen Topologie auf einem einzelnen Server installieren. Verwenden Sie die Konfiguration mit einem Server nur in einer Testumgebung. Verwenden Sie für Produktionsumgebungen zwei oder mehr Server. Wenn Sie die Microsoft BitLocker-Verwaltung und-Überwachung mithilfe der Configuration Manager-Topologie installieren, lesen Sie [Bereitstellen von MBAM mit Configuration Manager](deploying-mbam-with-configuration-manager-mbam2.md).

Das folgende Diagramm zeigt ein Beispiel für eine Architektur mit einem einzelnen Server. Eine Beschreibung der Datenbanken und Features finden Sie unter [Architektur auf höherer Ebene für MBAM 2,0](high-level-architecture-for-mbam-20-mbam-2.md).

![mbam 2 Einzelserver-Bereitstellungstopologie](images/mbam2-1-server.gif)

Jedes Server Feature hat bestimmte Voraussetzungen. Wenn Sie sicherstellen möchten, dass Sie die Voraussetzungen und Hardware-und Softwareanforderungen erfüllt haben, lesen Sie [MBAM 2,0-Bereitstellungsvoraussetzungen](mbam-20-deployment-prerequisites-mbam-2.md) und [MBAM 2,0-unterstützte Konfigurationen](mbam-20-supported-configurations-mbam-2.md). Darüber hinaus verfügen einige Features auch über Informationen, die während des Installationsvorgangs bereitgestellt werden müssen, um das Feature erfolgreich bereitzustellen. Sie sollten auch überprüfen, [wie Sie Ihre Umgebung für MBAM 2,0 vorbereiten](preparing-your-environment-for-mbam-20-mbam-2.md) , bevor Sie mit der MBAM-Bereitstellung beginnen.

**Hinweis:**  
Um die Setupprotokolldateien zu erhalten, verwenden Sie das msiexec-Paket und die Option **/l** &lt; Location &gt; , um MBAM zu installieren. Protokolldateien werden an dem von Ihnen angegebenen Speicherort erstellt.

Zusätzliche Setupprotokolldateien werden im Ordner% Temp% auf dem Server des Benutzers erstellt, der MBAM installiert.



## So installieren Sie die MBAM-Server Features auf einem einzelnen Server


In den folgenden Schritten wird beschrieben, wie allgemeine MBAM-Features installiert werden.

**So starten Sie die Installation von MBAM Server Features**

1.  Führen Sie auf dem Server, auf dem Sie MBAM installieren möchten, **MBAMSetup.exe** aus, um den MBAM-Installations-Assistenten zu starten.

2.  Wählen Sie auf der **Willkommens** Seite optional das **Programm zur Verbesserung der Benutzerfreundlichkeit**aus, und klicken Sie dann auf **Start**.

3.  Lesen und akzeptieren Sie den Microsoft-Software-Lizenzvertrag, und klicken Sie auf **weiter** , um die Installation fortzusetzen.

4.  Wählen Sie auf der Seite **Topologie Auswahl** die **eigenständige** Topologie aus, und klicken Sie dann auf **weiter**.

5.  Wählen Sie auf der Seite **zu installierende Features auswählen** die Features aus, die Sie installieren möchten. Standardmäßig sind alle MBAM-Features für die Installation ausgewählt. Features, die auf demselben Computer installiert werden sollen, müssen zur gleichen Zeit zusammen installiert werden. Deaktivieren Sie die Kontrollkästchen für alle Features, die Sie an anderer Stelle installieren möchten. Sie müssen die MBAM-Features in der folgenden Reihenfolge installieren:

    -   Wiederherstellungsdatenbank

    -   Konformitäts-und Überwachungsdatenbank

    -   Konformitäts-und Überwachungsberichte

    -   Self-Service-Server

    -   Verwaltungs-und Überwachungs Server

    -   MBAM-Gruppenrichtlinienvorlage

    **Hinweis:**  
    Der Installations-Assistent überprüft die Voraussetzungen für die Installation und zeigt die fehlenden Voraussetzungen an. Wenn alle Voraussetzungen erfüllt sind, wird die Installation fortgesetzt. Wenn eine fehlende Voraussetzung erkannt wird, müssen Sie die fehlenden Voraussetzungen beheben und dann **erneut auf Voraussetzungen prüfen**klicken. Wenn dieses Mal alle Voraussetzungen erfüllt sind, wird die Installation fortgesetzt.



6.  Wählen Sie auf der Seite **Netzwerk Kommunikationssicherheit konfigurieren** aus, ob die Kommunikation zwischen den Webdiensten auf dem Administrations-und Überwachungs Server und den Clients verschlüsselt werden soll. Wenn Sie sich entschließen, die Kommunikation zu verschlüsseln, wählen Sie das für die Verschlüsselung zu verwendende Zertifizierungsstellenzertifikat aus. Das Zertifikat muss vor diesem Schritt erstellt werden, damit Sie es auf dieser Seite auswählen können.

    **Hinweis:**  
    Diese Seite wird nur angezeigt, wenn Sie auf der Seite **zu installierende Features auswählen** das Self-Service-Portal oder die Verwaltungs-und Überwachungs Server Funktion ausgewählt haben.



7.  Klicken Sie auf **weiter**, und fahren Sie mit den nächsten Schritten fort, um die MBAM-Server Features zu konfigurieren.

**So konfigurieren Sie die MBAM-Server Features**

1.  Geben Sie auf der Seite " **Wiederherstellungsdatenbank konfigurieren** " den Namen der SQL Server-Instanz und den Namen der Datenbank an, in der die Wiederherstellungsdaten gespeichert werden. Sie müssen außerdem angeben, wo die Datenbankdateien gespeichert werden sollen und wo sich die Protokollinformationen befinden sollen.

2.  Klicken Sie auf **Weiter**, um den Vorgang fortzusetzen.

3.  Geben Sie auf der Seite **Compliance-und Überwachungsdatenbank konfigurieren** den Namen der SQL Server-Instanz und den Namen der Datenbank an, in der die Konformitäts-und Überwachungsdaten gespeichert werden. Sie müssen außerdem angeben, wo die Datenbankdateien gespeichert werden sollen und wo sich die Protokollinformationen befinden sollen.

4.  Klicken Sie auf **Weiter**, um den Vorgang fortzusetzen.

5.  Geben Sie auf der Seite **Compliance-und Überwachungsberichte konfigurieren** die SQL Server Reporting Services-Instanz an, in der die Kompatibilitäts-und Überwachungsberichte installiert werden, und geben Sie ein Domänenbenutzerkonto und ein Kennwort für den Zugriff auf die Datenbank Compliance und Audit an. Konfigurieren Sie das Kennwort für dieses Konto so, dass es nie abläuft. Das Benutzerkonto sollte in der Lage sein, auf alle Daten zuzugreifen, die der Gruppe MBAM-Berichte Benutzer zur Verfügung stehen.

6.  Klicken Sie auf **Weiter**, um den Vorgang fortzusetzen.

7.  Geben Sie auf der Seite **Self-Service-Portal konfigurieren** die Portnummer, den Hostnamen, den Namen des virtuellen Verzeichnisses und den Installationspfad für das Self-Service-Portal ein.

    **Hinweis:**  
    Die von Ihnen angegebene Portnummer muss eine nicht verwendete Portnummer auf dem Verwaltungs-und Überwachungs Server sein, sofern Sie keinen eindeutigen Hostheadernamen angeben. Wenn Sie die Windows-Firewall verwenden, wird der Port automatisch geöffnet.



8.  Klicken Sie auf **Weiter**, um den Vorgang fortzusetzen.

9.  Geben Sie an, ob Microsoft Updates dazu beitragen soll, Ihren Computer zu schützen, und klicken Sie dann auf **weiter**. Damit werden die automatischen Updates in Windows nicht aktiviert.

10. Geben Sie auf der Seite **Verwaltungs-und Überwachungs Server konfigurieren** die Portnummer, den Hostnamen, den Namen des virtuellen Verzeichnisses und den Installationspfad für die Helpdesk-Website ein.

    **Hinweis:**  
    Die von Ihnen angegebene Portnummer muss eine nicht verwendete Portnummer auf dem Verwaltungs-und Überwachungs Server sein, sofern Sie keinen eindeutigen Hostheadernamen angeben. Wenn Sie die Windows-Firewall verwenden, wird der Port automatisch geöffnet.



11. Überprüfen Sie auf der Seite **Installationszusammenfassung** die Liste der Features, die installiert werden sollen, und klicken Sie auf **Installieren** , um mit der Installation der MBAM-Features zu beginnen. Klicken Sie auf **zurück** , um durch den Assistenten zurückzukehren, wenn Sie die Installationseinstellungen überprüfen oder ändern müssen, oder klicken Sie auf **Abbrechen** , um Setup zu beenden. Setup installiert die MBAM-Features und benachrichtigt Sie, dass die Installation abgeschlossen ist.

12. Klicken Sie auf **Fertig stellen** , um den Assistenten zu beenden. Nachdem die Microsoft BitLocker-Verwaltungs-und Überwachungs Server Features installiert wurden, fahren Sie mit dem nächsten Abschnitt fort, und führen Sie die Schritte zum Hinzufügen von Benutzern zu den Microsoft BitLocker-Verwaltungs-und Überwachungs Rollen aus. Weitere Informationen zu Rollen finden Sie unter [Planen von MBAM 2,0-Administrator Rollen](planning-for-mbam-20-administrator-roles-mbam-2.md).

**So führen Sie die Konfiguration nach der Installation durch**

1.  Fügen Sie auf dem Verwaltungs-und Überwachungs Server den folgenden lokalen Gruppen Benutzer hinzu, um Ihnen Zugriff auf die Features der MBAM Help Desk-Website zu gewähren:

    -   **MBAM Helpdesk-Benutzer**: Mitglieder dieser lokalen Gruppe können auf der MBAM-Website für Verwaltung und Überwachung auf die Laufwerk Wiederherstellung zugreifen und TPM-Features verwalten. Alle Felder in Laufwerk Wiederherstellung und TPM verwalten sind für einen Helpdesk-Benutzer Pflichtfelder.

    -   **MBAM Advanced Helpdesk-Benutzer**: Mitglieder dieser lokalen Gruppe haben erweiterten Zugriff auf die Drive Recovery-und TPM-Features auf der MBAM-Website für Verwaltung und Überwachung. Für erfahrene Helpdesk-Benutzer ist in Drive Recovery nur das **Schlüssel-ID-** Feld erforderlich. In TPM verwalten sind nur das Feld **Computerdomäne** und das Feld **Computer Name** erforderlich.

2.  Fügen Sie auf dem Verwaltungs-und Überwachungs Server der folgenden lokalen Gruppe Benutzer hinzu, damit Sie auf der MBAM-Websiteverwaltung und Überwachung auf das Feature Berichte zugreifen können:

    -   **MBAM-Berichtsbenutzer**: Mitglieder dieser lokalen Gruppe können auf die Berichtsfeatures auf der MBAM-Website für Verwaltung und Überwachung zugreifen.

    -   Branding des Self-Service-Portals mit dem Namen Ihres Unternehmens, dem Hinweistext und anderen unternehmensspezifischen Informationen Anweisungen hierzu finden Sie unter so wird es [gemacht: Branding des Self-Service-Portals](how-to-brand-the-self-service-portal.md).

    **Hinweis:**  
    Die identische Benutzer-oder Gruppenmitgliedschaft der lokalen Gruppe " **MBAM-Berichtsbenutzer** " muss auf allen Computern verwaltet werden, auf denen die MBAM-Verwaltungs-und Überwachungs Server Features, die Kompatibilitäts-und Überwachungsdatenbank sowie Compliance-und Überwachungsberichte installiert sind. Die empfohlene Vorgehensweise besteht darin, eine Domänensicherheitsgruppe zu erstellen und diese Domänengruppe jeder lokalen MBAM-Berichtsbenutzer Gruppe hinzuzufügen. Wenn Sie diesen Prozess verwenden, können Sie die Gruppenmitgliedschaften über die Domänengruppe verwalten.



## Überprüfen der MBAM Server-Feature-Installation


Wenn die Microsoft BitLocker-Administrator-und-überwachungsinstallation abgeschlossen ist, überprüfen Sie, ob die Installation alle erforderlichen MBAM-Features erfolgreich eingerichtet hat, die für die BitLocker-Verwaltung erforderlich sind. Gehen Sie wie folgt vor, um zu überprüfen, ob der MBAM-Dienst funktionsfähig ist.

**So überprüfen Sie die Installation von MBAM Server Features**

1. Öffnen Sie auf jedem Server, auf dem ein MBAM-Feature bereitgestellt wird, die **System**Steuerung. Wählen Sie **Programme**und dann **Programme und Funktionen**aus. Überprüfen Sie, ob die **Microsoft BitLocker-Verwaltung und-Überwachung** in der Liste " **Programme und Features** " angezeigt wird.

   **Hinweis:**  
   Um die Installation zu überprüfen, müssen Sie ein Domänenkonto verwenden, das über lokale Computeradministrator Anmeldeinformationen auf jedem Server verfügt.



2. Öffnen Sie auf dem Server, auf dem die Wiederherstellungsdatenbank installiert ist, SQL Server Management Studio, und überprüfen Sie, ob die **MBAM-Wiederherstellungs-und-Hardware** Datenbank installiert ist.

3. Öffnen Sie auf dem Server, auf dem die Compliance-und Überwachungsdatenbank installiert ist, SQL Server Management Studio, und überprüfen Sie, ob die **MBAM-Konformitäts Status Datenbank** installiert ist.

4. Öffnen Sie auf dem Server, auf dem die Konformitäts-und Überwachungsberichte installiert sind, einen Webbrowser mit administrativen Anmeldeinformationen, und navigieren Sie zu "Start" der SQL Server Reporting Services-Website.

   Der standardmäßige Startspeicherort einer SQL Server Reporting Services-Websiteinstanz befindet sich unter http:// <em> &lt; NameofMBAMReportsServer &gt; </em> /Reports. Um die tatsächliche URL zu finden, verwenden Sie das Reporting Services-Konfigurations-Manager-Tool, und wählen Sie die Instanzen aus, die während der Installation angegeben werden.

   Vergewissern Sie sich, dass ein Berichtsordner mit dem Namen Microsoft BitLocker-Verwaltung und-Überwachung eine Datenquelle namens **MaltaDataSource** enthält und dass ein **en-US-** Ordner vier Berichte enthält.

   **Hinweis:**  
   Wenn SQL Server Reporting Services als benannte Instanz konfiguriert wurde, sollte die URL wie folgt aussehen: http://* &lt; NameofMBAMReportsServer &gt; */Reports\_* &lt; SRSInstanceName &gt; *



~~~
**Note**  
If SSRS was not configured to use Secure Socket Layer (SSL), the URL for the reports will be set to HTTP instead of HTTPS when you install the MBAM Server. If you then go to the Administration and Monitoring website and select a report, the following message appears: “Only Secure Content is Displayed.” To show the report, click **Show All Content**.
~~~



5. Führen Sie auf dem Server, auf dem die Verwaltungs-und Überwachungsfunktion installiert ist, den **Server-Manager** aus, und navigieren Sie zu **Rollen**. Wählen Sie **Webserver (IIS)** aus, und klicken Sie dann auf **Internet Informationsdienste (IIS)-Manager.**

6. Navigieren Sie in **Verbindungen** zu * &lt; Computername &gt; *, wählen Sie **Websites**aus, und wählen Sie dann **Microsoft BitLocker-Verwaltung und-Überwachung**aus. Überprüfen Sie, ob **MBAMAdministrationService**, **MBAMUserSupportService**, **MBAMComplianceStatusService**und **MBAMRecoveryAndHardwareService** aufgeführt sind.

7. Öffnen Sie auf dem Server, auf dem die Verwaltungs-und Überwachungsfeatures sowie das Self-Service-Portal installiert sind, einen Webbrowser mit administrativen Anmeldeinformationen, und navigieren Sie zu den folgenden Speicherorten, um sicherzustellen, dass Sie erfolgreich geladen werden:

   -   *http:// &lt; Hostname &gt; /Helpdesk/default.aspx* , und bestätigen Sie die einzelnen Links für Navigation und Berichte.

   -   *http:// &lt; Hostname &gt; /Selfservice&gt;/*

   -   *http:// &lt; Computername &gt; /MBAMAdministrationService/AdministrationService.svc*

   -   *http:// &lt; Hostname &gt; /MBAMUserSupportService/UserSupportService.svc*

   -   *http:// &lt; Computername &gt; /MBAMComplianceStatusService/StatusReportingService.svc*

   -   *http:// &lt; Computername &gt; /MBAMRecoveryAndHardwareService/CoreService.svc*

   **Hinweis:**  
   Es wird davon ausgegangen, dass die Server Features auf dem Standardport ohne Netzwerk Verschlüsselung installiert wurden. Wenn Sie die Server Features in einem anderen Port oder virtuellen Verzeichnis installiert haben, ändern Sie die URLs so, dass Sie den entsprechenden Port aufweisen, beispielsweise *http:// &lt; Hostname &gt; : &lt; Port &gt; /Helpdesk/default.ASP*x oder*http:// &lt; Hostname &gt; : &lt; Port &gt; / &lt; VirtualDirectory &gt; /default.aspx*

   Wenn die Server Features mit Netzwerk Verschlüsselung installiert wurden, ändern Sie http://in https://.



## Verwandte Themen


[Bereitstellen der Serverinfrastruktur von MBAM 2.0](deploying-the-mbam-20-server-infrastructure-mbam-2.md)









