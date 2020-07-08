---
title: Installieren und Konfigurieren von MBAM auf verteilten Servern
description: Installieren und Konfigurieren von MBAM auf verteilten Servern
author: dansimp
ms.assetid: 9ee766aa-6339-422a-8d00-4f58e4646a5e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 51f56a12d4e59226f834c7e474af0f1e96c1e8e9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811287"
---
# Installieren und Konfigurieren von MBAM auf verteilten Servern


Die Verfahren in diesem Thema beschreiben die vollständige Installation der Features Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) auf verteilten Servern.

Jedes Server Feature hat bestimmte Voraussetzungen. Wenn Sie sicherstellen möchten, dass Sie die Voraussetzungen und Hardware-und Softwareanforderungen erfüllt haben, lesen Sie [MBAM 1,0-Bereitstellungsvoraussetzungen](mbam-10-deployment-prerequisites.md) und [MBAM 1,0-unterstützte Konfigurationen](mbam-10-supported-configurations.md). Darüber hinaus erfordern einige Features, dass Sie während des Installationsvorgangs bestimmte Informationen bereitstellen, um das Feature erfolgreich bereitzustellen.

**Hinweis:**  
Um die Setupprotokolldateien zu erhalten, müssen Sie MBAM installieren, indem Sie das **msiexec** -Paket und die Option " **/l &lt; Location &gt; ** " verwenden. Protokolldateien werden an dem von Ihnen angegebenen Speicherort erstellt.

Zusätzliche Setupprotokolldateien werden im Ordner "% Temp%" des Benutzers erstellt, der die MBAM-Installation ausführt.



## <a href="" id="deploy-the-mbam-server-features-"></a>Bereitstellen der MBAM-Server Features


In den folgenden Schritten wird beschrieben, wie die allgemeinen MBAM-Features installiert werden.

**Hinweis:**  
Stellen Sie sicher, dass Sie das 32-Bit-Setup auf 32-Bit-Servern und das 64-Bit-Setup auf 64-Bit-Servern verwenden.



**So stellen Sie MBAM-Server Features bereit**

1.  Starten Sie den MBAM-Installations-Assistenten, und klicken Sie auf der Willkommensseite auf **Installieren** .

2.  Lesen und akzeptieren Sie die Microsoft-Software-Lizenzbestimmungen, und klicken Sie auf **weiter** , um die Installation fortzusetzen.

3.  Standardmäßig sind alle MBAM-Features für die Installation ausgewählt. Deaktivieren Sie die Features, die Sie an anderer Stelle installieren möchten. Features, die Sie auf demselben Computer installieren möchten, müssen alle zur gleichen Zeit installiert sein. MBAM-Features müssen in der folgenden Reihenfolge installiert werden:

    -   Wiederherstellungs-und Hardware Datenbank

    -   Konformitäts-und Überwachungsdatenbank

    -   Konformitätsprüfung und Berichte

    -   Verwaltungs-und Überwachungs Server

    -   MBAM-Gruppenrichtlinienvorlage

    **Hinweis:**  
    Der Installations-Assistent überprüft die Voraussetzungen für die Installation und zeigt die fehlenden Voraussetzungen an. Wenn alle Voraussetzungen erfüllt sind, wird die Installation fortgesetzt. Wenn eine fehlende Voraussetzung erkannt wird, müssen Sie die fehlenden Voraussetzungen beheben und dann **erneut auf Voraussetzungen prüfen**klicken. Wenn dieses Mal alle Voraussetzungen erfüllt sind, wird die Installation fortgesetzt.



4.  Der MBAM-Setup-Assistent zeigt die Installationsseiten für die ausgewählten Features an. In den folgenden Abschnitten werden die Installationsverfahren für die einzelnen Features beschrieben.

    **Hinweis:**  
    In der Regel wird jedes Feature auf einem separaten Server installiert. Wenn Sie mehrere Features auf einem einzelnen Server installieren möchten, können Sie einige der folgenden Schritte ändern oder entfernen.



~~~
**To install the Recovery and Hardware Database**

1.  Choose an option for MBAM communication encryption. MBAM can encrypt the communication between the Recovery and Hardware Database and the Administration and Monitoring servers. If you choose the option to encrypt communication, you are asked to select the authority-provisioned certificate that is used for encryption.

2.  Click **Next** to continue.

3.  Specify the names of the computers that will be running the Administration and Monitoring Server feature, to configure access to the Recovery and Hardware Database.. Once the Administration and Monitoring Server feature is deployed, it connects to the database by using its domain account.

4.  Click **Next** to continue.

5.  Specify the **Database Configuration** for the SQL Server instance that stores the recovery and hardware data. You must also specify where the database will be located and where the log information will be located.

6.  Click **Next** to continue with the MBAM Setup wizard.

**To install the Compliance and Audit Database**

1.  Choose an option for the MBAM communication encryption. MBAM can encrypt the communication between the Compliance and Audit Database and the Administration and Monitoring servers. If you choose the option to encrypt communication, you are asked to select the authority-provisioned certificate that will be used for encryption.

2.  Click **Next** to continue.

3.  Specify the user account that will be used to access the database for reports.

4.  Click **Next** to continue.

5.  Specify the computer names of the computers that you want to run the Administration and Monitoring Server and the Compliance and Audit Reports, to configure the access to the Compliance and Audit Database.. After the Administration and Monitoring and the Compliance and Audit Reports Server are deployed, they will connect to the databases by using their domain accounts.

6.  Specify the **Database Configuration** for the SQL Server instance that will store the compliance and audit data. You must also specify where the database will be located and where the log information will be located.

7.  Click **Next** to continue with the MBAM Setup wizard.

**To install the Compliance and Audit Reports**

1.  Specify the remote SQL Server instance. For example, *&lt;ServerName&gt;*,where the Compliance and Audit Database are installed.

2.  Specify the name of the Compliance and Audit Database. By default, the database name is “MBAM Compliance Status”, but you can change the name when you install the Compliance and Audit Database.

3.  Click **Next** to continue.

4.  Select the SQL Server Reporting Services instance where the Compliance and Audit Reports will be installed. Provide the username and password used to access the compliance database.

5.  Click **Next** to continue with the MBAM Setup wizard.

**To install the Administration and Monitoring Server feature**

1.  Choose an option for the MBAM communication encryption. MBAM can encrypt the communication between the Recovery and Hardware Database and the Administration and Monitoring servers. If you choose the option to encrypt communication, you are asked to select the authority-provisioned certificate that is used for encryption.

2.  Click **Next** to continue.

3.  Specify the remote SQL Server instance, For example, *&lt;ServerName&gt;*, where the Compliance and Audit Database are installed.

4.  Specify the name of the Compliance and Audit Database. By default, the database name is MBAM Compliance Status, but, you can change the name when you install the Compliance and Audit Database.

5.  Click **Next** to continue.

6.  Specify the remote SQL Server instance. For example, *&lt;ServerName&gt;*,where the Recovery and Hardware Database are installed.

7.  Specify the name of the Recovery and Hardware Database. By default, the database name is **MBAM Recovery and Hardware**, but you can change the name when you install the Recovery and Hardware Database feature.

8.  Click **Next** to continue.

9.  Specify the URL for the “Home” of the SQL Server Reporting Services (SRS) site. The default Home location of a SQL Server Reporting Services site instance is at:

    http://*&lt;NameofMBAMReportsServer&gt;/*ReportServer

    **Note**  
    If you configured the SQL Server Reporting Services as a named instance, the URL resembles the following:http://*&lt;NameofMBAMReportsServer&gt;*/ReportServer\_*&lt;SRSInstanceName&gt;*



10. Click **Next** to continue.

11. Enter the **Port Number**, the **Host Name** (optional), and the **Installation Path** for the MBAM Administration and Monitoring server

    **Warning**  
    The port number that you specify must be an unused port number on the Administration and Monitoring server, unless you specify a unique host header name.



12. Click **Next** to continue with the MBAM Setup wizard.
~~~

5. 

   Geben Sie an, ob Microsoft Updates dazu beitragen soll, Ihren Computer zu schützen, und klicken Sie dann auf **weiter**.

6. Wenn die ausgewählten MBAM-Funktionsinformationen abgeschlossen sind, können Sie die MBAM-Installation mit dem Setup-Assistenten starten. Klicken Sie auf **zurück** , um den Assistenten zu durchlaufen, wenn Sie Ihre Installationseinstellungen überprüfen oder ändern müssen. Klicken Sie auf **Installieren** , um mit der Installation zu beginnen. Klicken Sie auf **Abbrechen** , um den Assistenten zu beenden. Setup installiert die von Ihnen ausgewählten MBAM-Features und benachrichtigt Sie, dass die Installation abzuschließen ist.

7. Klicken Sie auf **Fertig stellen** , um den Assistenten zu beenden.

8. Fügen Sie Benutzer zu geeigneten MBAM-Rollen hinzu, nachdem die MBAM-Server Features installiert wurden. Weitere Informationen finden Sie unter [Planen von MBAM 1,0-Administrator Rollen](planning-for-mbam-10-administrator-roles.md).

**Konfiguration nach der Installation**

1.  Nach Abschluss des MBAM-Setups müssen Sie Benutzerrollen hinzufügen, bevor Benutzer auf Features auf der MBAM-Verwaltungswebsite zugreifen können. Fügen Sie auf dem Verwaltungs-und Überwachungs Server den folgenden lokalen Gruppen Benutzer hinzu.

    -   **MBAM-Hardware Benutzer**: Mitglieder dieser lokalen Gruppe können auf das Hardware Feature auf der MBAM-Verwaltungswebsite zugreifen.

    -   **MBAM Helpdesk-Benutzer**: Mitglieder dieser lokalen Gruppe können auf die Drive Recovery zugreifen und TPM-Features (Trusted Platform Modules) auf der MBAM-Verwaltungswebsite verwalten. Alle Felder in Laufwerk Wiederherstellung und TPM verwalten sind für einen Helpdesk-Benutzer Pflichtfelder.

    -   **MBAM Advanced Helpdesk-Benutzer**: Mitglieder dieser lokalen Gruppe haben erweiterten Zugriff auf die Drive Recovery-und TPM-Features auf der MBAM-Verwaltungswebsite. Für erfahrene Helpdesk-Benutzer ist in Drive Recovery nur das Schlüssel-ID-Feld erforderlich. In TPM verwalten sind nur das Feld Computerdomäne und das Feld Computer Name erforderlich.

2.  Fügen Sie auf der Verwaltungs-und Überwachungsserver-, Konformitäts-und Überwachungsdatenbank sowie auf dem Server, auf dem die Konformitäts-und Überwachungsberichte gehostet werden, Benutzer zur folgenden lokalen Gruppe hinzu, um Ihnen Zugriff auf das Feature Berichte auf der MBAM-Verwaltungswebsite zu gewähren.

    -   **MBAM-Berichtsbenutzer**: Mitglieder dieser lokalen Gruppe können auf die Berichte auf der MBAM-Verwaltungswebsite zugreifen.

    **Hinweis:**  
    Die identische Benutzer-oder Gruppenmitgliedschaft der lokalen Gruppe **MBAM-Berichtsbenutzer** muss auf allen Computern verwaltet werden, auf denen die MBAM-Verwaltungs-und Überwachungs Server Features, die Kompatibilitäts-und Überwachungsdatenbank sowie die Kompatibilitäts-und Überwachungsberichte installiert sind.



## Überprüfen der MBAM Server-Feature-Installation


Wenn die MBAM-Server Feature-Installation abgeschlossen ist, sollten Sie überprüfen, ob die Installation alle erforderlichen Features für MBAM erfolgreich eingerichtet hat. Gehen Sie wie folgt vor, um zu überprüfen, ob der MBAM-Dienst funktionsfähig ist.

**So überprüfen Sie eine MBAM-Installation**

1. Öffnen Sie auf jedem Server, auf dem ein MBAM-Feature bereitgestellt wird, die **System**Steuerung, klicken Sie auf **Programme**und dann auf **Programme und Funktionen**. Überprüfen Sie, ob die **Microsoft BitLocker-Verwaltung und-Überwachung** in der Liste " **Programme und Features** " angezeigt wird.

   **Hinweis:**  
   Um die MBAM-Installation zu überprüfen, müssen Sie ein Domänenkonto verwenden, das über lokale Computeradministrator Anmeldeinformationen auf jedem Server verfügt.



2. Öffnen Sie auf dem Server, auf dem die Wiederherstellungs-und Hardware Datenbank installiert ist, SQL Server Management Studio, und überprüfen Sie, ob die **MBAM-Wiederherstellungs-und Hardware** Datenbank installiert ist.

3. Öffnen Sie auf dem Server, auf dem die Compliance-und Überwachungsdatenbank installiert ist, SQL Server Management Studio, und überprüfen Sie, ob die **MBAM-Konformitäts Status** Datenbank installiert ist.

4. Öffnen Sie auf dem Server, auf dem die Konformitäts-und Überwachungsberichte installiert sind, einen Webbrowser mit Administratorrechten, und navigieren Sie zu "Start" der SQL Server Reporting Services-Website.

   Der standardmäßige Startspeicherort einer SQL Server Reporting Services-Websiteinstanz finden Sie unter http:// <em> &lt; NameofMBAMReportsServer &gt; </em> /Reports.aspx. Um die tatsächliche URL zu finden, verwenden Sie das Reporting Services-Konfigurations-Manager-Tool, und wählen Sie die während des Setups angegebenen Instanzen aus.

   Vergewissern Sie sich, dass ein Ordner mit dem Namen **Malta-Konformitätsberichte** aufgelistet ist und fünf Berichte und eine Datenquelle enthält.

   **Hinweis:**  
   Wenn SQL Server Reporting Services als benannte Instanz konfiguriert wurde, sollte die URL wie folgt aussehen: http://* &lt; NameofMBAMReportsServer &gt; */Reports\_* &lt; SRSInstanceName &gt; *



5. Führen Sie auf dem Server, auf dem die Verwaltungs-und Überwachungsfunktion installiert ist, den **Server-Manager** aus, navigieren Sie zu **Rollen**, wählen Sie **Webserver (IIS)** aus, und klicken Sie dann auf **Internet Informationsdienste (IIS)-Manager**. Navigieren Sie in **Verbindungen** zu * &lt; Computer &gt; Name*, klicken Sie auf **Websites**, und klicken Sie auf **Microsoft BitLocker-Verwaltung und-Überwachung**. Überprüfen Sie, ob **MBAMAdministrationService**, **MBAMComplianceStatusService**und **MBAMRecoveryAndHardwareService** aufgeführt sind.

6. Öffnen Sie auf dem Server, auf dem die Verwaltungs-und Überwachungsfunktion installiert ist, einen Webbrowser mit Administratorrechten, und navigieren Sie zu den folgenden Speicherorten auf der MBAM-Website, um sicherzustellen, dass Sie erfolgreich geladen werden:

   -   *http:// &lt; Computername &gt; /default.aspx* , und bestätigen Sie die einzelnen Links für Navigation und Berichte.

   -   *http:// &lt; Computername &gt; /MBAMAdministrationService/AdministrationService.svc*

   -   *http:// &lt; Computername &gt; /MBAMComplianceStatusService/StatusReportingService.svc*

   -   *http:// &lt; Computername &gt; /MBAMRecoveryAndHardwareService/CoreService.svc*

   **Hinweis:**  
   In der Regel werden Dienste auf dem Standard Port 80 ohne Netzwerk Verschlüsselung installiert. Wenn die Dienste an einem anderen Port installiert sind, ändern Sie die URLs so, dass Sie den entsprechenden Port umfassen. Beispiel* &lt; : http://Computername &gt; : &lt; Port &gt; */default.aspx oder http:// <em> &lt; Hostheadername &gt; / </em> default. aspx

   Wenn die Dienste mit Netzwerk Verschlüsselung installiert wurden, ändern Sie http://in https://.



~~~
Verify that each web page loads successfully.
~~~

## Verwandte Themen


[Bereitstellen der Serverinfrastruktur von MBAM 1.0](deploying-the-mbam-10-server-infrastructure.md)









