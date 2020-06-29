---
title: So installieren und Konfigurieren von MBAM auf einem Server
description: So installieren und Konfigurieren von MBAM auf einem Server
author: dansimp
ms.assetid: 55841c63-bad9-44e7-b7fd-ea7037febbd7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 225f66493ceafce5461df3fcc6f701e9a2922a5f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810351"
---
# So installieren und Konfigurieren von MBAM auf einem Server


Die Verfahren in diesem Thema beschreiben die vollständige Installation der Features Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) auf einem einzelnen Server.

Jedes Server Feature hat bestimmte Voraussetzungen. Wenn Sie überprüfen möchten, ob Sie die Voraussetzungen und die Hardware-und Softwareanforderungen erfüllt haben, lesen Sie [MBAM 1,0-Bereitstellungsvoraussetzungen](mbam-10-deployment-prerequisites.md) und [MBAM 1,0-unterstützte Konfigurationen](mbam-10-supported-configurations.md). Darüber hinaus verfügen einige Features auch über Informationen, die während des Installationsvorgangs bereitgestellt werden müssen, um das Feature erfolgreich bereitzustellen. Sie sollten auch überprüfen, [wie Sie Ihre Umgebung für MBAM 1,0 vorbereiten](preparing-your-environment-for-mbam-10.md) , bevor Sie mit der MBAM-Bereitstellung beginnen.

**Hinweis**  Um die Setupprotokolldateien zu erhalten, müssen Sie MBAM mit dem **msiexec** -Paket und der Option " **/l** &lt; Location &gt; " installieren. Protokolldateien werden an dem von Ihnen angegebenen Speicherort erstellt.

Zusätzliche Setupprotokolldateien werden im Ordner "% Temp%" des Benutzers erstellt, der MBAM installiert.

 

## So installieren Sie die MBAM-Server Features auf einem einzelnen Server


In den folgenden Schritten wird beschrieben, wie allgemeine MBAM-Features installiert werden.

**Hinweis**  Stellen Sie sicher, dass Sie das 32-Bit-Setup auf 32-Bit-Servern und das 64-Bit-Setup auf 64-Bit-Servern verwenden.

 

**So starten Sie die Installation von MBAM Server Features**

1.  Starten Sie den MBAM-Installations-Assistenten. Klicken Sie auf der Willkommensseite auf **Installieren** .

2.  Lesen und akzeptieren Sie die Microsoft-Software-Lizenzbestimmungen, und klicken Sie auf **weiter** , um die Installation fortzusetzen.

3.  Standardmäßig sind alle MBAM-Features für die Installation ausgewählt. Features, die auf demselben Computer installiert werden, müssen zur gleichen Zeit zusammen installiert werden. Deaktivieren Sie die Features, die Sie an anderer Stelle installieren möchten. Sie müssen die MBAM-Features in der folgenden Reihenfolge installieren:

    -   Wiederherstellungs-und Hardware Datenbank

    -   Konformitäts-und Überwachungsdatenbank

    -   Konformitätsprüfung und Berichte

    -   Verwaltungs-und Überwachungs Server

    -   MBAM-Gruppenrichtlinienvorlage

    **Hinweis**  Der Installations-Assistent überprüft die Voraussetzungen für die Installation und zeigt die fehlenden Voraussetzungen an. Wenn alle Voraussetzungen erfüllt sind, wird die Installation fortgesetzt. Wenn eine fehlende Voraussetzung erkannt wird, müssen Sie die fehlenden Voraussetzungen beheben und dann **erneut auf Voraussetzungen prüfen**klicken. Nachdem alle Voraussetzungen erfüllt wurden, wird die Installation fortgesetzt.

     

4.  Sie werden aufgefordert, die Netzwerk Kommunikationssicherheit zu konfigurieren. MBAM kann die Kommunikation zwischen der Wiederherstellungs-und Hardware Datenbank, dem Verwaltungs-und Überwachungs Server und den Clients verschlüsseln. Wenn Sie sich entschließen, die Kommunikation zu verschlüsseln, werden Sie aufgefordert, das Zertifizierungsstellenzertifikat auszuwählen, das für die Verschlüsselung verwendet wird.

5.  Klicken Sie auf **Weiter**, um den Vorgang fortzusetzen.

6.  Der MBAM-Setup-Assistent zeigt die Installationsseiten für die ausgewählten Features an.

**So stellen Sie MBAM-Server Features bereit**

1.  Geben Sie im Fenster **Wiederherstellungs-und Hardware Datenbank konfigurieren** die Instanz von SQL Server und den Namen der Datenbank an, in der die Wiederherstellungs-und Hardware Daten gespeichert werden. Außerdem müssen Sie sowohl den Speicherort der Datenbankdateien als auch den Speicherort der Protokollinformationen angeben.

2.  Klicken Sie auf **Weiter**, um den Vorgang fortzusetzen.

3.  Geben Sie im Fenster **Compliance-und Überwachungsdatenbank konfigurieren** die Instanz von SQL Server und den Namen der Datenbank an, in der die Konformitäts-und Überwachungsdaten gespeichert werden. Geben Sie dann den Speicherort der Datenbankdateien und den Speicherort der Protokollinformationen an.

4.  Klicken Sie auf **Weiter**, um den Vorgang fortzusetzen.

5.  Geben Sie im Fenster **Konformitäts-und Überwachungsberichte** die Instanz des Berichts Diensts an, die verwendet wird, und geben Sie ein Domänenbenutzerkonto für den Zugriff auf die Datenbank an. Hierbei sollte es sich um ein Benutzerkonto handeln, das speziell für diese Verwendung bereitgestellt wird. Das Benutzerkonto sollte in der Lage sein, auf alle Daten zuzugreifen, die der Gruppe MBAM-Berichte Benutzer zur Verfügung stehen.

6.  Klicken Sie auf **Weiter**, um den Vorgang fortzusetzen.

7.  Geben Sie im Fenster **Verwaltungs-und Überwachungsserver konfigurieren** die **Port Bindung**, den **Hostnamen** (optional) und den **Installationspfad** für den MBAM-Verwaltungs-und-Überwachungsserver ein.

    **Warnung**  Die von Ihnen angegebene Portnummer muss eine nicht verwendete Portnummer auf dem Verwaltungs-und Überwachungsserver sein, es sei denn, es wird ein eindeutiger Hostheadername angegeben.

     

8.  Klicken Sie auf **Weiter**, um den Vorgang fortzusetzen.

9.  Geben Sie an, ob Microsoft Updates dazu beitragen soll, Ihren Computer zu schützen, und klicken Sie dann auf **weiter**. Mit der Option "Microsoft Updates" werden die automatischen Updates in Windows nicht aktiviert.

10. Wenn der Setup-Assistent die erforderlichen Funktionsinformationen gesammelt hat, kann die MBAM-Installation gestartet werden. Klicken Sie auf **zurück** , um durch den Assistenten zurückzukehren, wenn Sie die Installationseinstellungen überprüfen oder ändern möchten. Klicken Sie auf **Installieren** , um mit der Installation zu beginnen. Klicken Sie auf **Abbrechen** , um Setup zu beenden. Setup installiert die MBAM-Features und benachrichtigt Sie, dass die Installation abgeschlossen ist.

11. Klicken Sie auf **Fertig stellen** , um den Assistenten zu beenden.

12. Nachdem Sie die MBAM-Server Features installiert haben, müssen Sie den MBAM-Rollen Benutzer hinzufügen. Weitere Informationen finden Sie unter [Planen von MBAM 1,0-Administrator Rollen](planning-for-mbam-10-administrator-roles.md).

**So führen Sie die Konfiguration nach der Installation durch**

1.  Nach Abschluss des Setups müssen Sie Benutzerrollen hinzufügen, damit Sie Benutzern den Zugriff auf Features auf der MBAM-Verwaltungswebsite gewähren können. Fügen Sie auf dem Verwaltungs-und Überwachungs Server den folgenden lokalen Gruppen Benutzer hinzu:

    -   **MBAM-Hardware Benutzer**: Mitglieder dieser lokalen Gruppe können auf das Hardware Feature auf der MBAM-Verwaltungswebsite zugreifen.

    -   **MBAM Helpdesk-Benutzer**: Mitglieder dieser lokalen Gruppe können auf die Laufwerk Wiederherstellung zugreifen und TPM-Features auf der MBAM-Verwaltungswebsite verwalten. Alle Felder in Laufwerk Wiederherstellung und TPM verwalten sind für einen Helpdesk-Benutzer Pflichtfelder.

    -   **MBAM Advanced Helpdesk-Benutzer**: Mitglieder dieser lokalen Gruppe haben erweiterten Zugriff auf die Drive Recovery-und TPM-Features auf der MBAM-Verwaltungswebsite. Für erfahrene Helpdesk-Benutzer ist in Drive Recovery nur das Schlüssel-ID-Feld erforderlich. Für das Verwalten von TPM-Benutzern sind nur das Feld Computerdomäne und der Computer Name erforderlich.

2.  Fügen Sie auf der Verwaltungs-und Überwachungs Server-, Konformitäts-und Überwachungsdatenbank sowie auf dem Computer, der die Konformitäts-und Überwachungsberichte hostet, Benutzer zur folgenden lokalen Gruppe hinzu, damit Sie auf das Feature Berichte auf der MBAM-Verwaltungswebsite zugreifen können:

    -   **MBAM-Berichtsbenutzer**: Mitglieder dieser lokalen Gruppe können auf die Berichtsfeatures auf der MBAM-Verwaltungswebsite zugreifen.

    **Hinweis**  Identische Benutzermitgliedschaften oder Gruppenmitgliedschaften der lokalen Gruppe **MBAM-Berichtsbenutzer** müssen auf allen Computern verwaltet werden, auf denen die Verwaltungs-und Überwachungs Server Features, die Kompatibilitäts-und Überwachungsdatenbank sowie Compliance-und Überwachungsberichte installiert sind.

    Wenn Sie identische Mitgliedschaften auf allen Computern beibehalten möchten, sollten Sie eine Domänensicherheitsgruppe erstellen und diese Domänengruppe jeder lokalen MBAM-Berichtsbenutzer Gruppe hinzufügen. In diesem Fall können Sie die Gruppenmitgliedschaften mithilfe der Domänengruppe verwalten.

     

## Überprüfen der MBAM Server-Feature-Installation


Wenn die MBAM-Installation abgeschlossen ist, überprüfen Sie, ob die Installation alle erforderlichen MBAM-Features erfolgreich eingerichtet hat, die für die BitLocker-Verwaltung erforderlich sind. Gehen Sie wie folgt vor, um zu überprüfen, ob der MBAM-Dienst funktionsfähig ist:

**So überprüfen Sie die Installation von MBAM Server Features**

1. Öffnen Sie auf jedem Server, auf dem ein MBAM-Feature bereitgestellt wird, die **System**Steuerung. Klicken Sie auf **Programme**und dann auf **Programme und Funktionen**. Überprüfen Sie, ob die **Microsoft BitLocker-Verwaltung und-Überwachung** in der Liste " **Programme und Features** " angezeigt wird.

   **Hinweis:**  
   Um die Installation zu überprüfen, müssen Sie ein Domänenkonto verwenden, das über lokale Computeradministrator Anmeldeinformationen auf jedem Server verfügt.

     

2. Öffnen Sie auf dem Server, auf dem die Wiederherstellungs-und Hardware Datenbank installiert ist, SQL Server Management Studio, und überprüfen Sie, ob die **MBAM-Wiederherstellungs-und Hardware** Datenbank installiert ist.

3. Öffnen Sie auf dem Server, auf dem die Compliance-und Überwachungsdatenbank installiert ist, SQL Server Management Studio, und überprüfen Sie, ob die **MBAM-Konformitäts-und Überwachungsdatenbank** installiert ist.

4. Öffnen Sie auf dem Server, auf dem die Konformitäts-und Überwachungsberichte installiert sind, einen Webbrowser mit Administratorrechten, und navigieren Sie zu "Start" der SQL Server Reporting Services-Website.

   Der standardmäßige Startspeicherort einer SQL Server Reporting Services-Websiteinstanz befindet sich unter http:// <em> &lt; NameofMBAMReportsServer &gt; </em> /Reports. Um die tatsächliche URL zu finden, verwenden Sie das Reporting Services-Konfigurations-Manager-Tool, und wählen Sie die während des Setups angegebenen Instanzen aus.

   Vergewissern Sie sich, dass ein Ordner mit dem Namen **Malta-Konformitätsberichte** aufgelistet ist und fünf Berichte und eine Datenquelle enthält.

   **Hinweis:**  
   Wenn SQL Server Reporting Services als benannte Instanz konfiguriert wurde, sollte die URL wie folgt aussehen: http://* &lt; NameofMBAMReportsServer &gt; */Reports\_* &lt; SRSInstanceName &gt; *

     

5. Führen Sie auf dem Server, auf dem die Verwaltungs-und Überwachungsfunktion installiert ist, den **Server-Manager** aus, navigieren Sie zu **Rollen**, wählen Sie **Webserver (IIS)** aus, und klicken Sie auf **Internet Informationsdienste (IIS)-Manager** .

6. Navigieren Sie in **Verbindungen**zu * &lt; Computername &gt; *, wählen Sie **Websites**aus, und wählen Sie **Microsoft BitLocker-Verwaltung und-Überwachung**aus. Überprüfen Sie, ob **MBAMAdministrationService**, **MBAMComplianceStatusService**und **MBAMRecoveryAndHardwareService** aufgeführt sind.

7. Öffnen Sie auf dem Server, auf dem die Verwaltungs-und Überwachungsfunktion installiert ist, einen Webbrowser mit Administratorrechten, und navigieren Sie dann zu den folgenden Speicherorten auf der MBAM-Website, um sicherzustellen, dass Sie erfolgreich geladen werden:

   -   *http:// &lt; Computername &gt; /default.aspx* , und bestätigen Sie die einzelnen Links für Navigation und Berichte.

   -   *http:// &lt; Computername &gt; /MBAMAdministrationService/AdministrationService.svc*

   -   *http:// &lt; Computername &gt; /MBAMComplianceStatusService/StatusReportingService.svc*

   -   *http:// &lt; Computername &gt; /MBAMRecoveryAndHardwareService/CoreService.svc*

   **Hinweis:**  
   In der Regel werden die Dienste auf dem Standard Port 80 ohne Netzwerk Verschlüsselung installiert. Wenn die Dienste an einem anderen Port installiert sind, ändern Sie die URLs so, dass Sie den entsprechenden Port umfassen. Beispiel* &lt; : http://Computername &gt; : &lt; Port &gt; */default.aspx oder http:// <em> &lt; Hostheadername &gt; / </em> default. aspx.

   Wenn die Dienste mit Netzwerk Verschlüsselung installiert werden, ändern Sie http://in https://.

     

## Verwandte Themen


[Bereitstellen der Serverinfrastruktur von MBAM 1.0](deploying-the-mbam-10-server-infrastructure.md)

 

 





