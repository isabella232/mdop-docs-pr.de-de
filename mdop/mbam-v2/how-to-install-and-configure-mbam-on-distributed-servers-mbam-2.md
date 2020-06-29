---
title: Installieren und Konfigurieren von MBAM auf verteilten Servern
description: Installieren und Konfigurieren von MBAM auf verteilten Servern
author: dansimp
ms.assetid: 67b91e6b-ae2e-4e47-9ef2-6819aba95976
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 841b894430d14604f0fd923703708d7a3f588c07
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810327"
---
# Installieren und Konfigurieren von MBAM auf verteilten Servern


In den Verfahren in diesem Thema wird beschrieben, wie Sie die Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) 2,0 in der eigenständigen Topologie auf verteilten Servern installieren. Ein Diagramm der empfohlenen Architektur sowie eine Beschreibung der Datenbanken und Features finden Sie unter [Bereitstellen der MBAM 2,0-Server Infrastruktur](deploying-the-mbam-20-server-infrastructure-mbam-2.md). Informationen zum Installieren der Microsoft BitLocker-Verwaltung und-Überwachung mit der Configuration Manager-Topologie finden Sie unter [Bereitstellen von MBAM mit Configuration Manager](deploying-mbam-with-configuration-manager-mbam2.md).

Jedes Server Feature hat bestimmte Voraussetzungen. Wenn Sie sicherstellen möchten, dass Sie die Voraussetzungen und Hardware-und Softwareanforderungen erfüllt haben, lesen Sie [MBAM 2,0-Bereitstellungsvoraussetzungen](mbam-20-deployment-prerequisites-mbam-2.md) und [MBAM 2,0-unterstützte Konfigurationen](mbam-20-supported-configurations-mbam-2.md). Darüber hinaus erfordern einige Features, dass Sie während des Installationsvorgangs bestimmte Informationen bereitstellen, um das Feature erfolgreich bereitzustellen. Sie sollten auch die [Planung für die MBAM 2,0-Server Bereitstellung](planning-for-mbam-20-server-deployment-mbam-2.md) überprüfen, bevor Sie mit der MBAM-Bereitstellung beginnen.

**Hinweis:**  
Um die Setupprotokolldateien zu erhalten, müssen Sie das msiexec-Paket und die Option **/l** &lt; Location verwenden, &gt; um MBAM zu installieren. Protokolldateien werden an dem von Ihnen angegebenen Speicherort erstellt.

Zusätzliche Setupprotokolldateien werden im Ordner% Temp% auf dem Server des Benutzers erstellt, der MBAM installiert.



## <a href="" id="deploying-mbam-server-features-"></a>Bereitstellen von MBAM-Server Features


In den folgenden Schritten wird beschrieben, wie allgemeine MBAM-Features installiert werden.

**So starten Sie den MBAM-Server Installations-Assistenten**

1.  Führen Sie auf dem Server, auf dem Sie die Microsoft BitLocker-Verwaltung und-Überwachung installieren möchten, **MBAMSetup.exe** aus, um den MBAM-Installations-Assistenten zu starten.

2.  Wählen Sie auf der **Willkommens** Seite optional das **Programm zur Verbesserung der Benutzerfreundlichkeit**aus, und klicken Sie dann auf **Start**.

3.  Lesen und akzeptieren Sie den Microsoft-Software-Lizenzvertrag, und klicken Sie auf **weiter** , um die Installation fortzusetzen.

4.  Wählen Sie auf der Seite **Topologie Auswahl** die **eigenständige** Topologie aus, und klicken Sie dann auf **weiter**.

    **Hinweis:**  
    Wenn Sie MBAM mit der integrierten Configuration Manager-Topologie installieren möchten, lesen Sie [Bereitstellen von MBAM mit Configuration Manager](deploying-mbam-with-configuration-manager-mbam2.md).



5.  Wählen Sie die Features aus, die Sie installieren möchten. Standardmäßig sind alle MBAM-Features für die Installation ausgewählt. Deaktivieren Sie die Features, die Sie an anderer Stelle installieren möchten. Features, die auf demselben Computer installiert werden, müssen zur gleichen Zeit zusammen installiert werden. Sie müssen die MBAM-Features in der folgenden Reihenfolge installieren:

    -   Wiederherstellungsdatenbank

    -   Konformitäts-und Überwachungsdatenbank

    -   Konformitäts-und Überwachungsberichte

    -   Self-Service-Portal

    -   Verwaltungs-und Überwachungs Server

    -   MBAM-Gruppenrichtlinienvorlage

    **Hinweis:**  
    Der Installations-Assistent überprüft die Voraussetzungen für die Installation und zeigt die fehlenden Voraussetzungen an. Wenn alle Voraussetzungen erfüllt sind, wird die Installation fortgesetzt. Wenn eine fehlende Voraussetzung erkannt wird, müssen Sie die fehlenden Voraussetzungen beheben und dann **erneut auf Voraussetzungen prüfen**klicken. Wenn dieses Mal alle Voraussetzungen erfüllt sind, wird die Installation fortgesetzt.



~~~
The MBAM Setup wizard displays installation pages for the features that you select. The following sections describe the installation procedures for each feature.

**Note**  
For the following instructions, it is assumed that each feature is to be installed on a separate server. If you install multiple features on a single server, you can change or eliminate some steps.
~~~



**So installieren Sie die Wiederherstellungsdatenbank**

1.  Geben Sie auf der Seite " **Wiederherstellungsdatenbank konfigurieren** " die Namen der Computer an, auf denen das Feature "Verwaltungs-und Überwachungs Server" ausgeführt werden soll. Nach der Bereitstellung des Verwaltungs-und Überwachungs Server Features wird mit dem Domänenkonto eine Verbindung mit der Datenbank hergestellt.

2.  Klicken Sie auf **Weiter**, um den Vorgang fortzusetzen.

3.  Geben Sie den Namen der SQL Server-Instanz und den Namen der Datenbank an, in der die Wiederherstellungsdaten gespeichert werden sollen. Sie müssen außerdem angeben, an welcher Stelle die Datenbank gespeichert werden soll und wo sich die Protokollinformationen befinden sollen.

4.  Klicken Sie auf **weiter** , um mit dem MBAM-Setup-Assistenten fortzufahren.

**So installieren Sie die Konformitäts-und Überwachungsdatenbank**

1.  Geben Sie auf der Seite **Compliance-und Überwachungsdatenbank konfigurieren** das Benutzerkonto an, das für den Zugriff auf die Datenbank für Berichte verwendet wird.

2.  Geben Sie die Computernamen der Computer an, auf denen der Verwaltungs-und Überwachungs Server ausgeführt werden soll, sowie die Konformitäts-und Überwachungsberichte. Nachdem die Verwaltung und Überwachung sowie der Server für Konformitäts-und Überwachungsberichte bereitgestellt wurden, verwenden Sie Ihre Domänenkonten, um eine Verbindung mit den Datenbankenherzustellen.

    **Hinweis:**  
    Wenn Sie die Konformitäts-und Überwachungsdatenbank ohne das Feature Konformitäts-und Überwachungsberichte installieren, müssen Sie auf dem Computer Compliance-und Überwachungsdatenbank eine Ausnahme hinzufügen, um eingehenden Datenverkehr auf dem Microsoft SQL Server-Port zu aktivieren. Die Standardportnummer ist 1433.



3.  Geben Sie den Namen der SQL Server-Instanz und den Namen der Datenbank an, in der die Konformitäts-und Überwachungsdaten gespeichert werden. Sie müssen außerdem angeben, wo sich die Datenbank-und Protokollinformationen befinden sollen.

4.  Klicken Sie auf **weiter** , um den Setup-Assistenten für Microsoft BitLocker-Verwaltung und-Überwachung fortzusetzen.

**So installieren Sie die Konformitäts-und Überwachungsberichte**

1.  Geben Sie auf der Seite **Compliance-und Überwachungsberichte konfigurieren** den Namen der Remote-SQL Server-Instanz an (beispielsweise &lt; Servername &gt; ), in dem die Kompatibilitäts-und Überwachungsdatenbank installiert wurde.

    **Hinweis:**  
    Wenn Sie die Konformitäts-und Überwachungsberichte ohne den Verwaltungs-und Überwachungsserver installieren, müssen Sie auf dem Computer für Konformitäts-und Überwachungsberichte eine Ausnahme hinzufügen, um eingehenden Datenverkehr auf dem Reporting Server-Port zu aktivieren (der Standardport ist 80).



2.  Geben Sie den Namen der Konformitäts-und Überwachungsdatenbank an. Standardmäßig ist der Datenbankname MBAM-Konformitäts Status, obwohl Sie den Namen beim Installieren der Konformitäts-und Überwachungsdatenbank ändern können.

3.  Klicken Sie auf **Weiter**, um den Vorgang fortzusetzen.

4.  Wählen Sie die Instanz von SQL Server Reporting Services aus, in der die Kompatibilitäts-und Überwachungsberichte installiert werden. Stellen Sie ein Domänenbenutzerkonto und ein Kennwort für den Zugriff auf die Datenbank Compliance und Audit bereit. Konfigurieren Sie das Kennwort für dieses Konto so, dass es nie abläuft. Das Benutzerkonto sollte auf alle Daten zugreifen können, die für die Gruppe MBAM-Berichte Benutzer verfügbar sind.

5.  Klicken Sie auf **weiter** , um den Setup-Assistenten für Microsoft BitLocker-Verwaltung und-Überwachung fortzusetzen.

**So installieren Sie das Self-Service-Portal**

1.  Auf der Seite **Self-Service-Portal konfigurieren** können Sie optional die Kommunikation zwischen dem Self-Service-Portal und den Verwaltungs-und Überwachungs Servern verschlüsseln. Wenn Sie die Option zum Verschlüsseln der Kommunikation auswählen, werden Sie aufgefordert, das Zertifikat der Zertifizierungsstelle zu wählen, das für die Verschlüsselung verwendet werden soll.

2.  Klicken Sie auf **Weiter**, um den Vorgang fortzusetzen.

3.  Geben Sie die Remoteinstanz von SQL Server an (beispielsweise * &lt; Servername &gt; *), in der die Kompatibilitäts-und Überwachungsdatenbank installiert wurde.

4.  Geben Sie den Namen der Konformitäts-und Überwachungsdatenbank an. Standardmäßig ist der Datenbankname MBAM-Konformitäts Status. Sie können den Namen jedoch ändern, wenn Sie die Kompatibilitäts-und Überwachungsdatenbank installieren.

5.  Klicken Sie auf **Weiter**, um den Vorgang fortzusetzen.

6.  Geben Sie die Remoteinstanz von SQL Server an (beispielsweise * &lt; Servername &gt; *), in der die Wiederherstellungsdatenbank installiert wurde.

7.  Geben Sie den Namen der Wiederherstellungsdatenbank an. Standardmäßig ist der Datenbankname **MBAM-Wiederherstellung und-Hardware**. Sie können den Namen jedoch bei der Installation des Wiederherstellungsdaten Bank Features ändern.

8.  Klicken Sie auf **Weiter**, um den Vorgang fortzusetzen.

9.  Geben Sie die **Port Nummer**, den **Hostnamen** (optional) und den **Installationspfad** für den MBAM-Verwaltungs-und-Überwachungs Server ein.

    **Hinweis:**  
    Die von Ihnen angegebene Portnummer muss eine nicht verwendete Portnummer auf dem Verwaltungs-und Überwachungsserver sein, sofern Sie keinen eindeutigen Hostheadernamen angeben. Wenn Sie die Windows-Firewall verwenden, wird der Port automatisch geöffnet.



10. Wenn Sie optional einen Dienstprinzipalnamen (Service Principal Name, SPN) für das Self-Service-Portal registrieren möchten, wählen Sie **Dienstprinzipalnamen (Service Principal Names, SPN) dieses Computers registrieren für Active Directory (für die Windows-Authentifizierung erforderlich)** aus. Wenn Sie dieses Kontrollkästchen aktivieren, versucht MBAM Setup nicht, die vorhandenen SPNs zu registrieren, und Sie können den SPN vor oder nach der Installation von MBAM manuell registrieren. Anweisungen zum manuellen Registrieren des SPN finden Sie unter [Manuelle SPN-Registrierung](https://go.microsoft.com/fwlink/?LinkId=286758).

11. Klicken Sie auf **weiter** , um den Setup-Assistenten für Microsoft BitLocker-Verwaltung und-Überwachung fortzusetzen.

12. Geben Sie an, ob Microsoft Updates dazu beitragen soll, Ihren Computer zu schützen, und klicken Sie dann auf **weiter**.

13. Wenn die ausgewählten MBAM-Funktionsinformationen abgeschlossen sind, können Sie die MBAM-Installation mithilfe des Setup-Assistenten starten. Klicken Sie auf **zurück** , um den Assistenten zu durchlaufen, wenn Sie Ihre Installationseinstellungen überprüfen oder ändern müssen. Klicken Sie auf **Installieren** , um die Installation zu starten. Klicken Sie auf **Abbrechen** , um den Assistenten zu beenden. Setup installiert die von Ihnen ausgewählten MBAM-Features und benachrichtigt Sie, dass die Installation abzuschließen ist.

14. Klicken Sie auf **Fertig stellen** , um den Assistenten zu beenden.

    **Hinweis:**  
    Wenn Sie das Self-Service-Portal nach der Installation konfigurieren möchten, sollten Sie das Self-Service-Portal mit dem Namen Ihres Unternehmens und anderen unternehmensspezifischen Informationen versehen, und erfahren Sie, wie Sie das Self- [Service-Portal](how-to-brand-the-self-service-portal.md) für Anweisungen kennzeichnen.



15. Wenn die Clientcomputer Zugriff auf das Microsoft Content Delivery Network (CDN) haben, das dem Self-Service-Portal den erforderlichen Zugriff auf bestimmte JavaScript-Dateien gewährt, sind Sie mit der Installation des Self-Service-Portals am Ende. Wenn die Clientcomputer keinen Zugriff auf das Microsoft CDN haben, führen Sie die Schritte im nächsten Abschnitt aus, um das Self-Service-Portal so zu konfigurieren, dass es von einer barrierefreien Quelle aus auf die JavaScript-Dateien verweist.

**So konfigurieren Sie das Self-Service-Portal, wenn Endbenutzer nicht auf das Microsoft Content Delivery Network zugreifen können**

1. Wenn die Clientcomputer Zugriff auf das Microsoft Content Delivery Network (CDN) haben, das dem Self-Service-Portal den erforderlichen Zugriff auf bestimmte JavaScript-Dateien gewährt, ist die Self-Service-Portal-Installation abgeschlossen. Wenn die Clientcomputer keinen Zugriff auf das Microsoft CDN haben, führen Sie die verbleibenden Schritte in diesem Abschnitt aus, um das Self-Service-Portal so zu konfigurieren, dass es von einer barrierefreien Quelle aus auf die JavaScript-Dateien verweist.

2. Laden Sie die vier JavaScript-Dateien aus dem Microsoft CDN herunter:

   -   jQuery-1.7.2.min.js-[https://go.microsoft.com/p/fwlink/?LinkID=271736](https://go.microsoft.com/fwlink/p/?LinkID=271736)

   -   MicrosoftAjax.js –[https://go.microsoft.com/p/fwlink/?LinkId=272283](https://go.microsoft.com/fwlink/p/?LinkId=272283)

   -   MicrosoftMvcAjax.js-[https://go.microsoft.com/p/fwlink/?LinkId=272284](https://go.microsoft.com/fwlink/p/?LinkId=272284)

   -   MicrosoftMvcValidation.js- <https://go.microsoft.com/fwlink/p/?LinkId=272285>

3. Kopieren Sie die JavaScript-Dateien in das Verzeichnis **Skripts** des Self-Service-Portals. Dieses Verzeichnis befindet sich in <em> &lt; MBAM Self-Service-Installationsverzeichnis &gt; \\ </em> Self-Service Website\\Scripts.

4. Öffnen Sie **Internet Informationsdienste (IIS)-Manager**.

5. Erweitern Sie **Sites** &gt; **Microsoft BitLocker-Verwaltung und-Überwachung**, und markieren Sie **Selfservice**.

   **Hinweis:**  
   *Selfservice* ist der Name des virtuellen Standardverzeichnisses. Wenn Sie während der Installation einen anderen Namen für dieses Verzeichnis gewählt haben, vergessen Sie nicht, *Selfservice* in den restlichen Anweisungen durch den von Ihnen gewählten Namen zu ersetzen.



6. Doppelklicken Sie im mittleren Bereich auf **Anwendungseinstellungen**.

7. Bearbeiten Sie für jedes Element in der folgenden Liste die Anwendungseinstellungen, um auf den neuen Speicherort zu verweisen, indem &lt; Sie virtuelles Verzeichnis durch &gt; /Selfservice/ersetzen (oder den Namen, den Sie während der Installation ausgewählt haben). Beispielsweise ist der Pfad des virtuellen Verzeichnisses mit/Selfservice/Scripts/jquery-1.7.2.min.js vergleichbar.

   -   jQueryPath:/ &lt; virtuelles Verzeichnis &gt; /Scripts/jQuery-1.7.2.min.js

   -   MicrosoftAjaxPath:/ &lt; virtuelles Verzeichnis &gt; /Scripts/MicrosoftAjax.js

   -   MicrosoftMvcAjaxPath:/ &lt; virtuelles Verzeichnis &gt; /Scripts/MicrosoftMvcAjax.js

   -   MicrosoftMvcValidationPath:/ &lt; virtuelles Verzeichnis &gt; /Scripts/MicrosoftMvcValidation.js

**So installieren Sie das Feature "Verwaltungs-und Überwachungs Server"**

1. MBAM kann die Kommunikation zwischen den Webdiensten und den Verwaltungs-und Überwachungs Servern verschlüsseln. Wenn Sie die Option zum Verschlüsseln der Kommunikation auswählen, werden Sie aufgefordert, das Zertifikat der Zertifizierungsstelle zu wählen, das für die Verschlüsselung verwendet werden soll.

2. Klicken Sie auf **Weiter**, um den Vorgang fortzusetzen.

3. Geben Sie die Remoteinstanz von SQL Server an (beispielsweise * &lt; Servername &gt; *), in der die Kompatibilitäts-und Überwachungsdatenbank installiert wurde.

4. Geben Sie den Namen der Konformitäts-und Überwachungsdatenbank an. Standardmäßig ist der Datenbankname MBAM-Konformitäts Status. Sie können den Namen jedoch ändern, wenn Sie die Kompatibilitäts-und Überwachungsdatenbank installieren.

5. Klicken Sie auf **Weiter**, um den Vorgang fortzusetzen.

6. Geben Sie die Remoteinstanz von SQL Server an, auf der die Wiederherstellungsdatenbank installiert wurde (beispielsweise: * &lt; Servername &gt; *).

7. Geben Sie den Namen der Wiederherstellungsdatenbank an. Standardmäßig ist der Datenbankname **MBAM-Wiederherstellung und-Hardware**. Sie können den Namen jedoch bei der Installation des Wiederherstellungsdaten Bank Features ändern.

8. Klicken Sie auf **Weiter**, um den Vorgang fortzusetzen.

9. Geben Sie die URL für das "Home" der SQL Server Reporting Services (SRS)-Website an. Der standardmäßige Startspeicherort einer SQL Server Reporting Services-Websiteinstanz lautet:

   http:// <em> &lt; NameofMBAMReportsServer &gt; / </em> Report Server

   **Hinweis:**  
   Wenn SQL Server Reporting Services als benannte Instanz konfiguriert wurde, sieht die URL wie folgt aus: http://* &lt; NameofMBAMReportsServer &gt; */ReportServer\_* &lt; SRSInstanceName &gt; *.



10. Klicken Sie auf **Weiter**, um den Vorgang fortzusetzen.

11. Geben Sie die **Port Nummer**, den **Hostnamen** (optional) und den **Installationspfad** für den MBAM-Verwaltungs-und-Überwachungs Server ein.

    **Hinweis:**  
    Die von Ihnen angegebene Portnummer muss eine nicht verwendete Portnummer auf dem Verwaltungs-und Überwachungsserver sein, sofern Sie keinen eindeutigen Hostheadernamen angeben. Wenn Sie die Windows-Firewall verwenden, wird der Port automatisch geöffnet.



12. Wenn Sie optional einen Dienstprinzipalnamen (Service Principal Name, SPN) für das Self-Service-Portal registrieren möchten, wählen Sie **Dienstprinzipalnamen (Service Principal Names, SPN) dieses Computers registrieren für Active Directory (für die Windows-Authentifizierung erforderlich)** aus. Wenn Sie dieses Kontrollkästchen aktivieren, versucht MBAM Setup nicht, die vorhandenen SPNs zu registrieren, und Sie können den SPN vor oder nach der Installation von MBAM manuell registrieren. Anweisungen zum manuellen Registrieren des SPN finden Sie unter [Manuelle SPN-Registrierung](https://go.microsoft.com/fwlink/?LinkId=286758).

13. Klicken Sie auf **weiter** , um den Setup-Assistenten für Microsoft BitLocker-Verwaltung und-Überwachung fortzusetzen.

14. Geben Sie an, ob Microsoft Updates dazu beitragen soll, Ihren Computer zu schützen, und klicken Sie dann auf **weiter**.

15. Wenn die ausgewählten MBAM-Funktionsinformationen abgeschlossen sind, können Sie die MBAM-Installation mithilfe des Setup-Assistenten starten. Klicken Sie auf **zurück** , um den Assistenten zu durchlaufen, wenn Sie Ihre Installationseinstellungen überprüfen oder ändern müssen. Klicken Sie auf installieren, um die Installation zu **Installieren** . Klicken Sie auf **Abbrechen** , um den Assistenten zu beenden. Setup installiert die von Ihnen ausgewählten MBAM-Features und benachrichtigt Sie, dass die Installation abzuschließen ist.

16. Klicken Sie auf **Fertig stellen** , um den Assistenten zu beenden.

**So führen Sie die Konfiguration nach der Installation durch**

1.  Fügen Sie auf dem Verwaltungs-und Überwachungs Server den folgenden lokalen Gruppen Benutzer hinzu, um Ihnen Zugriff auf die Features auf der MBAM-Verwaltungs-und-Überwachungs Website zu gewähren.

    -   **MBAM Helpdesk-Benutzer**: Mitglieder dieser lokalen Gruppe können auf der MBAM-Website für Verwaltung und Überwachung auf die Laufwerk Wiederherstellung zugreifen und TPM-Features verwalten. Alle Felder in Laufwerk Wiederherstellung und TPM verwalten sind für einen Helpdesk-Benutzer Pflichtfelder.

    -   **MBAM Advanced Helpdesk-Benutzer**: Mitglieder dieser lokalen Gruppe haben erweiterten Zugriff auf die Drive Recovery-und TPM-Features auf der MBAM-Website für Verwaltung und Überwachung. Für erfahrene Helpdesk-Benutzer ist in Drive Recovery nur das Schlüssel-ID-Feld erforderlich. In **TPM verwalten**sind nur das Feld **Computerdomäne** und das Feld **Computer Name** erforderlich.

2.  Fügen Sie auf dem Server, auf dem die Verwaltungs-und Überwachungsserver sowie die Compliance-und Überwachungsdatenbank gehostet werden, sowie auf dem Server, auf dem die Konformitäts-und Überwachungsberichte gehostet werden, Benutzer zur folgenden lokalen Gruppe hinzu, um Ihnen Zugriff auf das Feature Berichte auf der MBAM-Verwaltungs-und-Überwachungs Website zu gewähren.

    -   **MBAM-Berichtsbenutzer**: Mitglieder dieser lokalen Gruppe können auf die Berichte auf der MBAM-Website zugreifen.

    **Hinweis:**  
    Die identische Benutzer-oder Gruppenmitgliedschaft der lokalen Gruppe **MBAM-Berichtsbenutzer** muss auf allen Computern verwaltet werden, auf denen die MBAM-Verwaltungs-und Überwachungs Server Features, die Kompatibilitäts-und Überwachungsdatenbank sowie die Kompatibilitäts-und Überwachungsberichte installiert sind.



## Überprüfen der MBAM Server-Feature-Installation


Wenn die Installation der Microsoft BitLocker-Verwaltungs-und Monitoring Server-Features abgeschlossen ist, empfehlen wir, dass Sie überprüfen, ob die Installation alle erforderlichen Features für MBAM erfolgreich eingerichtet hat. Gehen Sie wie folgt vor, um zu überprüfen, ob der Dienst Microsoft BitLocker-Verwaltung und-Überwachung funktionsfähig ist.

**So überprüfen Sie eine MBAM-Server Installation**

1. Öffnen Sie auf jedem Server, auf dem ein MBAM-Feature bereitgestellt wird, die **System**Steuerung, wählen Sie **Programme**und dann **Programme und Funktionen**aus. Überprüfen Sie, ob die **Microsoft BitLocker-Verwaltung und-Überwachung** in der Liste " **Programme und Features** " angezeigt wird.

   **Hinweis:**  
   Um die MBAM-Installation zu überprüfen, müssen Sie ein Domänenkonto verwenden, das über lokale Computeradministrator Anmeldeinformationen auf jedem Server verfügt.



2. Öffnen Sie auf dem Server, auf dem die Wiederherstellungsdatenbank installiert ist, SQL Server Management Studio, und überprüfen Sie, ob die **MBAM-Wiederherstellungs-und-Hardware** Datenbank installiert ist.

3. Öffnen Sie auf dem Server, auf dem die Compliance-und Überwachungsdatenbank installiert ist, SQL Server Management Studio, und überprüfen Sie, ob die **MBAM-Konformitäts Status Datenbank** installiert ist.

4. Öffnen Sie auf dem Server, auf dem die Konformitäts-und Überwachungsberichte installiert sind, einen Webbrowser mit administrativen Anmeldeinformationen, und navigieren Sie zu "Start" der SQL Server Reporting Services-Website.

   Der standardmäßige Startspeicherort einer SQL Server Reporting Services-Websiteinstanz befindet sich unter http:// <em> &lt; NameofMBAMReportsServer &gt; </em> /Reports.aspx. Um die tatsächliche URL zu finden, verwenden Sie das Reporting Services-Konfigurations-Manager-Tool, und wählen Sie die Instanzen aus, die während der Installation angegeben wurden.

   Vergewissern Sie sich, dass ein Berichtsordner mit dem Namen **Microsoft BitLocker-Verwaltung und-Überwachung** eine Datenquelle namens **MaltaDataSource** enthält und dass ein **en-US-** Ordner vier Berichte enthält.

   **Hinweis:**  
   Wenn SQL Server Reporting Services als benannte Instanz konfiguriert wurde, sollte die URL wie folgt aussehen: http://* &lt; NameofMBAMReportsServer &gt; */Reports\_* &lt; SRSInstanceName &gt; *



~~~
**Note**  
If SSRS was not configured to use Secure Socket Layer (SSL), the URL for the reports will be set to HTTP instead of HTTPS when you install the MBAM Server. If you then go to the Administration and Monitoring website and select a report, the following message appears: “Only Secure Content is Displayed.” To show the report, click **Show All Content**.
~~~



5. Führen Sie auf dem Server, auf dem die Verwaltungs-und Überwachungsfunktion installiert ist, den **Server-Manager** aus, und navigieren Sie zu **Rollen**. Wählen Sie **Webserver (IIS)** aus, und klicken Sie dann auf **Internet Informationsdienste (IIS)-Manager**.

6. Navigieren Sie in **Verbindungen**zu * &lt; Computername &gt; *, wählen Sie **Websites**aus, und wählen Sie **Microsoft BitLocker-Verwaltung und-Überwachung**aus. Überprüfen Sie, ob **MBAMAdministrationService**, **MBAMComplianceStatusService**und **MBAMRecoveryAndHardwareService** aufgeführt sind.

7. Öffnen Sie auf dem Server, auf dem die Verwaltungs-und Überwachungsfeatures sowie das Self-Service-Portal installiert sind, einen Webbrowser mit administrativen Anmeldeinformationen, und navigieren Sie zu den folgenden Speicherorten, um sicherzustellen, dass Sie erfolgreich geladen werden.

   **Hinweis:**  
   Die URLs, die in ". svc" enden, zeigen keine Website an. Der Erfolg wird durch die Meldung "Metadaten-Veröffentlichung für diesen Dienst ist zurzeit deaktiviert" oder durch Informationen angezeigt, die mit Code vergleichbar sind. Wenn eine andere Fehlermeldung angezeigt wird oder die Seite nicht gefunden wird, wurde die Seite nicht erfolgreich geladen.



~~~
-   *http://&lt;hostname&gt;/HelpDesk/default.aspx* and confirm each of the links for navigation and reports

-   *http://&lt;hostname&gt;/SelfService&gt;/*

-   *http://&lt;computername&gt;/MBAMAdministrationService/AdministrationService.svc*

-   *http://&lt;hostname&gt;/MBAMUserSupportService/UserSupportService.svc*

-   *http://&lt;computername&gt;/MBAMComplianceStatusService/StatusReportingService.svc*

-   *http://&lt;computername&gt;/MBAMRecoveryAndHardwareService/CoreService.svc*

**Note**  
It is assumed that the server features were installed on the default port without network encryption. If you installed the server features on a different port or virtual directory, change the URLs to include the appropriate port, for example, *http://&lt;hostname&gt;:&lt;port&gt;/HelpDesk/default.aspx* or*http://&lt;hostname&gt;:&lt;port&gt;/&lt;virtualdirectory&gt;/default.aspx*

If the server features were installed with network encryption, change http:// to https://.
~~~



8. Überprüfen Sie, ob jede Webseite erfolgreich geladen wurde.

## Verwandte Themen


[Bereitstellen der Serverinfrastruktur von MBAM 2.0](deploying-the-mbam-20-server-infrastructure-mbam-2.md)









