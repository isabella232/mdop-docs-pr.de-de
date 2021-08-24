---
title: Bereitstellen von MBAM 2,5 in einer eigenständigen Konfiguration
description: Einführung in die Bereitstellung von MBAM 2.5 in einer eigenständigen Konfiguration.
author: Deland-Han
ms.reviewer: dcscontentpm
manager: dansimp
ms.author: delhan
ms.sitesec: library
ms.prod: w10
ms.date: 09/16/2019
ms.openlocfilehash: 1ceccf3973bb131484f91917c2b80cd676d1c31b
ms.sourcegitcommit: 3e0500abde44d6a09c7ac8e3caf5e25929b490a4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2021
ms.locfileid: "11910470"
---
# <a name="deploying-mbam-25-in-a-standalone-configuration"></a>Bereitstellen von MBAM 2.5 in einer eigenständigen Konfiguration

Dieser Artikel enthält schrittweise Anweisungen zum Installieren von Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 in einer eigenständigen Konfiguration. In diesem Leitfaden verwenden wir eine Konfiguration mit zwei Servern. Einer der beiden Server ist ein Datenbankserver, der Microsoft SQL Server 2012 ausgeführt wird. Auf diesem Server werden die MBAM-Datenbanken und -Berichte gehostet. Der zusätzliche Server ist ein Windows Server 2012 Webserver, der "Verwaltungs- und Überwachungsserver" und "Self-Service-Portal" hostet.

## <a name="preparation-steps-before-installing-mbam-25-server-software"></a>Vorbereitungsschritte vor der Installation von MBAM 2.5-Serversoftware

### <a name="step-1-installation-and-configuration-of-servers"></a>Schritt 1: Installation und Konfiguration von Servern

Bevor wir mit der Konfiguration von MBAM 2.5 beginnen, müssen wir sicherstellen, dass beide Server gemäß den MBAM-Systemanforderungen konfiguriert sind. Sehen Sie sich die [Mindestsystemanforderungen](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/mbam-25-supported-configurations#-mbam-server-system-requirements)für MBAM an, und wählen Sie eine Konfiguration aus, die diese Anforderungen erfüllt. 

#### <a name="step-11-deploying-prerequisites-for-database-and-reporting-server"></a>Schritt 1.1: Bereitstellen der Voraussetzungen für Datenbank- und Berichtsserver

1. Installieren und konfigurieren Sie einen Server, auf dem Windows Server 2008 R2 -Betriebssystem (oder höher) ausgeführt wird.

2. Installieren Sie Windows PowerShell 3.0.

3. Installieren Sie Microsoft SQL Server 2008 R2 oder eine höhere Version, die das neueste Service Pack enthält. Wenn Sie eine neue Instanz von SQL Server für MBAM installieren, stellen Sie sicher, dass die SQL Server, die Sie installieren, die SQL_Latin1_General_CP1_CI_AS Sortierung enthält. Sie müssen die folgenden SQL Server Features installieren:

    * Datenbank-Engine
    * Reporting Services
    * Clienttools-Konnektivität
    * Verwaltungstools – vollständig

    > [!Note]
    > Optional können Sie auch das [Feature Transparent Data Encryption (TDE) in SQL Server](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/mbam-25-security-considerations)installieren.

    SQL Server Reporting Services müssen im "nativen" Modus und nicht im unkonfigurierten Modus oder im Modus "SharePoint" installiert und konfiguriert werden.

    ![Die erforderlichen SQL Server Features.](images/deploying-MBAM-1.png)

4. Wenn Sie beabsichtigen, SSL für die Verwaltungs- und Überwachungswebsite zu verwenden, stellen Sie sicher, dass Sie SQL Server Reporting Services (SSRS) so konfigurieren, dass das SSL-Protokoll (Secure Sockets Layer) verwendet wird, bevor Sie die Verwaltungs- und Überwachungswebsite konfigurieren. Andernfalls verwendet das Feature "Berichte" den unverschlüsselten (HTTP)-Datentransport anstelle von verschlüsselten Daten (HTTPS).

    Sie können ["KONFIGURIEREN VON SSL-Verbindungen auf](https://docs.microsoft.com/sql/reporting-services/security/configure-ssl-connections-on-a-native-mode-report-server?view=sql-server-2017) einem Berichtsserver im nativen Modus" befolgen, um SSL auf dem Berichtsserver zu konfigurieren.
    
    > [!Note]
    > Sie können das SQL Server Installationshandbuch für Ihre jeweilige Version von SQL Server befolgen, um SQL Server zu installieren. Die Links sind wie folgt:
        > * [SQL Server 2014](https://docs.microsoft.com/sql/sql-server/install/planning-a-sql-server-installation?view=sql-server-2014)
        > * [SQL Server 2012](https://docs.microsoft.com/previous-versions/sql/sql-server-2012/bb500442(v=sql.110))
        > * [SQL Server 2008 R2](https://docs.microsoft.com/previous-versions/sql/sql-server-2012/bb500442(v=sql.110))

5. Stellen Sie nach der Installation von SQL Server sicher, dass Sie das Benutzerkonto in SQL Server bereitstellen, und weisen Sie dem Benutzer, der die MBAM-Datenbank und Berichtsrollen auf dem Datenbankserver konfigurieren wird, die folgenden Berechtigungen zu.

    Rollen für die Instanz von SQL Server:
        
    * Dbcreator
    * processadmin

    Rechte für die Instanz von SQL Server Reporting Services:
    
    * Erstellen von Ordnern
    * Veröffentlichen von Berichten

Ihr Datenbankserver ist bereit für die Konfiguration von MBAM 2.5-Rollen. Wechseln wir zum nächsten Server.

#### <a name="step-12-deploying-prerequisites-for-administration-and-monitoring-server"></a>Schritt 1.2: Bereitstellen der Voraussetzungen für den Verwaltungs- und Überwachungsserver

Wählen Sie einen Server aus, der die Hardwarekonfiguration erfüllt, wie im Dokument mit den [MBAM-Systemanforderungen](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/mbam-25-supported-configurations#-mbam-server-system-requirements)erläutert. Es muss Windows Server 2008 R2 oder höher zusammen mit dem neuesten Service Pack und Updates ausgeführt werden. Nachdem der Server bereit ist, installieren Sie die folgenden Rollen und Features:

##### <a name="roles"></a>Rollen

* Webserver-Verwaltungstools (IIS) (Wählen Sie IIS-Verwaltungsskripts und -Tools aus.)

* Webserverrollendienste

    * Allgemeine HTTP-Features<br />
      Statischer Inhalt<br />
      Standarddokument

    * Anwendungsentwicklung<br />
      ASP.NET<br />
      .NET-Erweiterbarkeit<br />
      ISAPI-Erweiterungen<br />
      ISAPI-Filter<br />
      Sicherheit<br />
      Windows-Authentifizierung<br />
      Anforderungsfilterung

    * Webdienst-IIS-Verwaltungstools

##### <a name="feature"></a>Feature

* features .NET Framework 4.5
  
  * Microsoft .NET Framework 4.5
  
    Für Windows Server 2012 oder Windows Server 2012 R2 ist .NET Framework 4.5 bereits für diese Versionen von Windows Server installiert. Sie müssen sie jedoch aktivieren.
  
    Für Windows Server 2008 R2 ist .NET Framework 4.5 nicht in Windows Server 2008 R2 enthalten. Daher müssen Sie .NET Framework 4.5 herunterladen und separat installieren.
  
  * WCF-Aktivierung<br />
    HTTP-Aktivierung<br />
    Nicht-HTTP-Aktivierung
  
  * TCP-Aktivierung
  
  * Windows Prozessaktivierungsdienst:<br />
    Prozessmodell<br />
    .NET Framework Umgebung<br />
    Konfigurations-APIs

Damit das Self-Service-Portal funktioniert, sollten Sie auch [ASP.NET MVC 4.0 herunterladen und installieren.](https://go.microsoft.com/fwlink/?linkid=392271)

Der nächste Schritt besteht darin, die erforderlichen MBAM-Benutzer und -Gruppen in Active Directory zu erstellen.

### <a name="step-2-creating-users-and-groups-in-active-directory-domain-services"></a>Schritt 2: Erstellen von Benutzern und Gruppen in Active Directory Domain Services
 
Als Teil der Voraussetzungen müssen Sie bestimmte Rollen und Konten definieren, die in MBAM verwendet werden, um Sicherheits- und Zugriffsrechte für bestimmte Server und Features bereitzustellen, z. B. die Datenbanken, die auf der Instanz von SQL Server ausgeführt werden, und die Webanwendungen, die auf dem Verwaltungs- und Überwachungsserver ausgeführt werden.

Erstellen Sie die folgenden Gruppen und Benutzer in Active Directory. (Sie können einen beliebigen Namen für die Gruppen und Benutzer verwenden.) Benutzer müssen nicht über größere Benutzerrechte verfügen. Ein Domänenbenutzerkonto ist ausreichend. Sie müssen den Namen dieser Gruppen während der Konfiguration von MBAM 2.5 angeben:

* **MBAMAppPool**  

  **Typ:** Domänenbenutzer

  **Beschreibung:** Domänenbenutzer mit Lese- oder Schreibberechtigung für die Compliance- und Überwachungsdatenbank und die Wiederherstellungsdatenbank, damit die Webanwendungen auf die Daten und Berichte in diesen Datenbanken zugreifen können. Sie wird auch vom Anwendungspool für die Webanwendungen verwendet.

  **Kontorollen (während der Konfiguration von MBAM):**

  1. Domänenkonto des Webdienstanwendungspools

  2. Benutzer mit Lese-/Schreibzugriff auf Kompatibilität und Überwachungsdatenbank und Wiederherstellungsdatenbank für Berichte

* **MBAMROUser**

  **Typ:** Domänenbenutzer

  **Beschreibung:** Domänenbenutzer, der Read-Only Zugriff auf die Compliance- und Überwachungsdatenbank hat, damit die Berichte auf die Compliance- und Überwachungsdaten in dieser Datenbank zugreifen können. Es ist auch das Domänenbenutzerkonto, das die lokale SQL Server Reporting Services Instanz für den Zugriff auf die Compliance- und Überwachungsdatenbank verwendet.

  **Kontorollen (während der Konfiguration von MBAM):**

  1. Schreibgeschützter Benutzer der Compliance- und Überwachungsdatenbank für Berichte

  2. Benutzerkonto der Compliance- und Überwachungsdatenbankdomäne

* **MBAMAdvHelpDsk**

  **Typ:** Domänengruppe

  **Beschreibung:** Zugriffsgruppe für ERWEITERTE HELPDESK-Benutzer von MBAM: Domänenbenutzergruppe, deren Mitglieder Zugriff auf alle Bereiche der Verwaltungs- und Überwachungswebsite haben. Benutzer mit dieser Rolle müssen nur den Wiederherstellungsschlüssel und nicht die Domäne und den Benutzernamen des Benutzers eingeben, wenn sie Benutzern helfen, ihre Laufwerke wiederherzustellen. Wenn ein Benutzer Mitglied sowohl der Gruppe "MBAM-Helpdeskbenutzer" als auch der Gruppe "Mbam Advanced Helpdesk-Benutzer" ist, überschreiben die Gruppenberechtigungen der erweiterten MBAM-Helpdeskbenutzer die Berechtigungen der MBAM-Helpdesk-Gruppe.

  **Kontorollen (während der Konfiguration von MBAM):** MBAM Advanced Helpdesk-Benutzer

* **MBAMHelpdsk**

  **Typ:** Domänengruppe

  **Beschreibung:** Zugriffsgruppe für MBAM-Helpdeskbenutzer: Domänenbenutzergruppe, deren Mitglieder Zugriff auf die Bereiche "TPM verwalten" und "Wiederherstellung" der MBAM-Verwaltungs- und -Überwachungswebsite haben. Personen mit dieser Rolle müssen alle Felder ausfüllen, wenn sie beide Optionen verwenden. Dazu gehören die Domäne und der Kontoname des Benutzers.

  **Kontorollen (während der Konfiguration von MBAM):** MBAM-Helpdesk-Benutzer

* **MBAMRUGrp**

  **Typ:** Domänengruppe

  **Beschreibung:** Domänenbenutzergruppe, deren Mitglieder schreibgeschützten Zugriff auf die Berichte im Bereich "Berichte" der Verwaltungs- und Überwachungswebsite haben.

  **Kontorollen (während der Konfiguration von MBAM):**

  1. Meldet schreibgeschützte Domänenzugriffsgruppe

  2. Zugriffsgruppe für MBAM-Berichtbenutzer

### <a name="step-3-optional-configure-and-install-ssl-certificate-on-administration-and-monitoring-server"></a>Schritt 3 (Optional): Konfigurieren und Installieren des SSL-Zertifikats auf dem Verwaltungs- und Überwachungsserver

Obwohl dies optional ist, wird dringend empfohlen, ein Zertifikat zu verwenden, um die Kommunikation zwischen dem MBAM-Client und der Verwaltungs- und Überwachungswebsite und den Websites des Self-Service-Portals zu sichern. Es wird nicht empfohlen, selbstsignte Zertifikate aus offensichtlichen Sicherheitsgründen zu verwenden. Es wird empfohlen, ein Webservertypzertifikat von einer vertrauenswürdigen Zertifizierungsstelle zu verwenden. Zu diesem Zweck können Sie den Abschnitt "Using Certificate Approved by Certificate Approved by Certificate Authority" von [KB 2754259](https://support.microsoft.com/help/2754259).

Nachdem das Zertifikat ausgestellt wurde, sollten Sie das Zertifikat dem persönlichen Speicher des Verwaltungs- und Überwachungsservers hinzufügen. Um das Zertifikat hinzuzufügen, öffnen Sie den Zertifikatspeicher auf dem lokalen Computer. Gehen Sie hierzu folgendermaßen vor:

1. Wählen Sie mit der rechten Maustaste "Start" und dann "Ausführen" aus.

   ![Auswählen.](images/deploying-MBAM-2.png)

2. Geben Sie "MMC.EXE" (ohne Anführungszeichen) ein, und wählen Sie dann **OK**aus.

   ![Run box.](images/deploying-MBAM-3.png) 

3. Wählen Sie **"Datei"** in der neuen MMC aus, die Sie geöffnet haben, und wählen Sie dann **Snap-In hinzufügen/entfernen**aus.
   
   ![Auswählen.](images/deploying-MBAM-4.png)

4. Markieren Sie das Snap-In **"Zertifikate",** und wählen Sie dann **"Hinzufügen"** aus.

   ![Add or Remove Snap-ins window.](images/deploying-MBAM-5.png)

5. Wählen Sie die Option **"Computerkonto"** und dann **"Weiter"** aus.
   
   ![Snap-In-Fenster "Zertifikate".](images/deploying-MBAM-6.png)

6. Wählen Sie auf dem nächsten Bildschirm **"Lokaler Computer"** und dann **"Fertig stellen"** aus.
   
   ![Wählen Sie das Fenster "Computer" aus.](images/deploying-MBAM-7.png)

7. Sie haben nun das Zertifikat-Snap-In hinzugefügt. Auf diese Weise können Sie mit allen Zertifikaten im Zertifikatspeicher Ihres Computers arbeiten.

   ![Add or Remove Snap-ins window.](images/deploying-MBAM-8.png)

8. Importieren Sie das Webserverzertifikat in den Zertifikatspeicher Des Computers.

   Nachdem Sie nun Zugriff auf das Zertifikat-Snap-In haben, können Sie das Webserverzertifikat in den Zertifikatspeicher Des Computers importieren. Führen Sie dazu die nächsten Schritte aus.

9. Öffnen Sie das Snap-In Zertifikate (lokaler Computer), und navigieren Sie zu **"Persönlich"** und dann zu **"Zertifikate".**
   
   ![Snap-In-Fenster "Zertifikate (lokaler Computer)".](images/deploying-MBAM-9.png)

   > [!Note]
   > Das Zertifikat-Snap-In wird möglicherweise nicht aufgeführt. Ist dies nicht der Typ, werden keine Zertifikate installiert.

10. Wählen Sie mit der rechten Maustaste **"Zertifikate",** **"Alle Aufgaben"** und dann **"Importieren"** aus.

    ![Snap-In-Fenster "Zertifikate (lokaler Computer)".](images/deploying-MBAM-10.png)

11. Wenn der Assistent gestartet wird, wählen Sie **Weiter**. Navigieren Sie zu der datei, die Sie erstellt haben, die Ihr Serverzertifikat und ihren privaten Schlüssel enthält, und wählen Sie dann **"Weiter"** aus.

    ![Fenster des Assistenten zum Importieren von Zertifikaten.](images/deploying-MBAM-11.png)

12. Geben Sie das Kennwort ein, wenn Sie bei der Erstellung ein Kennwort für die Datei angegeben haben.

   ![Geben Sie das Kennwortfenster ein.](images/deploying-MBAM-12.png)

   > [!Note]
   > Stellen Sie sicher, dass die Option **"Schlüssel als exportierbar markieren"** ausgewählt ist, wenn Sie das Schlüsselpaar erneut von diesem Computer exportieren möchten. Als zusätzliche Sicherheitsmaßnahme sollten Sie diese Option deaktiviert lassen, um sicherzustellen, dass niemand eine Sicherung Ihres privaten Schlüssels erstellen kann.
 
13. Wählen Sie **"Weiter"** aus, und wählen Sie dann das **Zertifikat Store** aus, in dem Sie das Zertifikat speichern möchten.

    ![Fenster des Assistenten zum Importieren von Zertifikaten.](images/deploying-MBAM-13.png)

    > [!Note]
    > Sie sollten **"Persönlich"** auswählen, da es sich um ein Webserverzertifikat handelt. Wenn Sie das Zertifikat in die Zertifizierungshierarchie aufgenommen haben, wird es diesem Speicher ebenfalls hinzugefügt.
 
14. Wählen Sie **"Weiter"** und dann **"Fertig stellen"** aus.

    ![Fenster des Assistenten zum Importieren von Zertifikaten.](images/deploying-MBAM-14.png)

Das Serverzertifikat für Ihren Webserver wird nun in der Liste der persönlichen Zertifikate angezeigt. Sie wird durch den allgemeinen Namen des Servers gekennzeichnet. (Sie finden dies im Abschnitt "Betreff" des Zertifikats.)

Weitere Informationen:

[Sicherheitsüberlegungen zu MBAM 2.5](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/mbam-25-security-considerations)

[Planen der Sicherung von MBAM-Websites](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/planning-how-to-secure-the-mbam-websites)

Der nächste Schritt besteht darin, einen Dienstprinzipanamen für das Anwendungspoolkonto zu registrieren.

### <a name="step-4-configuring-ssl-certificate-for-mbam-web-server"></a>Schritt 4: Konfigurieren des SSL-Zertifikats für MBAM-Webserver

Wenn Sie die SSL-Kommunikation zwischen Client und Server verwenden, sollten Sie sicherstellen, dass das Zertifikat über erweiterte Schlüsselverwendungs-OIDs (1.3.6.1.5.5.7.3.1) und (1.3.6.1.5.5.7.3.2) verfügt. Das heißt, Sie sollten sicherstellen, dass die Serverauthentifizierung und die Clientauthentifizierung hinzugefügt werden.

Wenn beim Durchsuchen von Dienst-URLs ein Zertifikatfehler angezeigt wird, verwenden Sie ein Zertifikat, das mit einem anderen Namen ausgestellt wurde, oder sie durchsuchen eine falsche URL.

Der Browser fordert Sie zwar möglicherweise mit einer Zertifikatsfehlermeldung auf, lässt Sie aber fortfahren, der MBAM-Webdienst ignoriert keine Zertifikatfehler und blockiert die Verbindung. Sie werden zertifikatbezogene Fehler im MBAM-Ereignisprotokoll des MBAM-Clients bemerken. Wenn Sie einen Alias verwenden, um eine Verbindung mit dem Verwaltungs- und Überwachungsserver herzustellen, sollten Sie ein Zertifikat für den Aliasnamen ausstellen. Das heißt, der Antragstellername des Zertifikats sollte der Aliasname sein, und der DNS-Name des lokalen Servers sollte dem Feld **"Alternativer Antragstellername"** des Zertifikats hinzugefügt werden.

Beispiel:

Wenn der virtuelle Name "bitlocker.contoso.com" lautet und der MBAM-Verwaltungs- und Überwachungsservername "adminserver.contoso.com" lautet, sollte das Zertifikat an bitlocker.contoso.com (Antragstellername) ausgestellt werden, und adminserver.contoso.com sollte dem Feld **"Alternativer Antragstellername"** des Zertifikats hinzugefügt werden.

Entsprechend sollten Sie, wenn Sie mehrere Verwaltungs- und Überwachungsserver installiert haben, um die Last mithilfe eines Lastenausgleichs auszugleichen, das SSL-Zertifikat für den virtuellen Namen ausstellen. Das heißt, das Feld "Antragstellername" des Zertifikats sollte den virtuellen Namen haben, und die Namen aller lokalen Server sollten im Feld **"Alternativer Antragstellername"** des Zertifikats hinzugefügt werden.

Beispiel:

Wenn der virtuelle Name "bitlocker.contoso.com" lautet und die Server "adminserver1.contoso.com" und "adminiserver2.contoso.com" sind, sollte das Zertifikat für bitlocker.contoso.com (Antragstellername) und adminserver1.contoso.com ausgestellt werden, und adminiserver2.contoso.com sollte dem Feld **"Alternativer Antragstellername"** des Zertifikats hinzugefügt werden.

Die Schritte zum Konfigurieren der SSL-Kommunikation mithilfe von MBAM werden im folgenden Knowledge Base-Artikel beschrieben: [KB 2754259](https://support.microsoft.com/help/2754259).

### <a name="step-5-register-spns-for-the-application-pool-account-and-configure-constrained-delegation"></a>Schritt 5: Registrieren von SPNS für das Anwendungspoolkonto und Konfigurieren der eingeschränkten Delegierung

> [!Note]
> Eingeschränkte Delegierung ist nur für 2.5 und nicht für 2.5 Service Pack 1 und höher erforderlich.

Damit die MBAM-Server die Kommunikation über die Verwaltungs- und Überwachungswebsite und das Self-Service-Portal authentifizieren können, müssen Sie einen Dienstprinzipalnamen (SPN) für den Hostnamen unter dem Domänenkonto registrieren, das Sie für den Webanwendungspool verwenden. Der folgende Artikel enthält Schritt-für-Schritt-Anweisungen zum Registrieren von SPNs: [Planning How to Secure the MBAM Websites](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/planning-how-to-secure-the-mbam-websites)

Nachdem Sie den SPN konfiguriert haben, sollten Sie eine eingeschränkte Delegierung für den SPN einrichten. Gehen Sie hierzu folgendermaßen vor:

1. Wechseln Sie zu Active Directory, und suchen Sie die App-Poolanmeldeinformationen, die Sie in den vorherigen Schritten für MBAM-Websites konfiguriert haben.

2. Klicken Sie mit der rechten Maustaste auf die Anmeldeinformationen, und wählen Sie dann **Eigenschaften**aus.

3. Wählen Sie die Registerkarte **"Delegierung"** aus.

4. Wählen Sie die Option für die Kerberos-Authentifizierung aus.

5. Wählen Sie **"Durchsuchen"** aus, und suchen Sie erneut nach Ihren App-Poolanmeldeinformationen. Sie sollten dann alle SPNs sehen, die für das App-Pool-Creds-Konto eingerichtet sind. (Der SPN sollte "http/bitlocker.fqdn.com" ähneln. Markieren Sie den SPN, der dem Hostnamen entspricht, den Sie während der MBAM-Installation angegeben haben.

6. Wählen Sie **OK** aus.

Jetzt sind Sie mit den Voraussetzungen gut vertraut. In den nächsten Schritten installieren Sie die MBAM-Software auf den Servern und konfigurieren sie.

## <a name="installing-and-configuring-mbam-25-server-software"></a>Installieren und Konfigurieren von MBAM 2.5-Serversoftware

### <a name="step-6-install-mbam-25-server-software"></a>Schritt 6: Installieren von MBAM 2.5-Serversoftware 

Führen Sie die folgenden Schritte aus, um die MBAM Server-Software mithilfe des Microsoft BitLocker-Assistenten für die Verwaltung und Überwachung auf dem Datenbankserver und auf dem Verwaltungs- und Überwachungsserver zu installieren.

1. Führen Sie auf dem Server, auf dem SIE MBAM installieren möchten, MBAMserversetup.exe aus, um den Assistenten für die Microsoft BitLocker-Verwaltungs- und -Überwachungseinrichtung zu starten.

2. Wählen Sie auf der Willkommensseite **"Weiter"** aus.

3. Lesen und akzeptieren Sie den Microsoft-Softwarelizenzvertrag, und wählen Sie dann **"Weiter"** aus, um die Installation fortzusetzen.

4. Entscheiden Sie, ob Microsoft Update verwendet werden soll, wenn Sie nach Updates suchen, und wählen Sie dann **"Weiter"** aus.

5. Entscheiden Sie, ob Sie am Programm zur Verbesserung der Benutzerfreundlichkeit teilnehmen möchten, und wählen Sie dann **"Weiter"** aus.

6. Wählen Sie zum Starten der Installation die Option **"Installieren" aus.**

7. Aktivieren Sie zum Konfigurieren der Serverfeatures nach Abschluss der Installation der MBAM Server-Software das Kontrollkästchen **"MBAM-Serverkonfiguration ausführen", nachdem der Assistent geschlossen** wurde. Oder Sie können MBAM später mithilfe der **MBAM-Serverkonfigurationsverknüpfung** konfigurieren, die die Serverinstallation im **Startmenü** erstellt.

8. Wählen Sie **"Fertig stellen"** aus.

Weitere Informationen finden Sie unter [Installieren der MBAM 2.5-Serversoftware.](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/installing-the-mbam-25-server-software)

### <a name="step-7-configure-mbam-25-database-and-reports-role"></a>Schritt 7: Konfigurieren der Rolle "MBAM 2.5-Datenbank und Berichte"

In diesem Schritt konfigurieren wir die MBAM 2.5-Datenbanken und die Berichtskomponente mithilfe des MBAM-Assistenten:

1. Konfigurieren Sie die Konformitäts- und Überwachungsdatenbank und die Wiederherstellungsdatenbank mithilfe des Assistenten:
   
   1. Starten Sie auf dem Server, auf dem Sie die Datenbanken konfigurieren möchten, den Assistenten für die **MBAM-Serverkonfiguration.** Sie können **MBAM-Serverkonfiguration** im **Startmenü** auswählen, um den Assistenten zu öffnen.

   2. Wählen Sie **"Neue Features hinzufügen",** **"Compliance- und Überwachungsdatenbank",** **"Wiederherstellungsdatenbank und Berichte" und**dann **"Weiter"** aus. Der Assistent überprüft, ob alle Voraussetzungen für die Datenbanken erfüllt sind.

   3. Wenn die Voraussetzungsprüfung erfolgreich ist, wählen Sie **Weiter** aus, um fortzufahren. Beheben Sie andernfalls alle fehlenden Voraussetzungen, und wählen Sie dann **erneut "Voraussetzungen überprüfen" aus.**
   
   4. Geben Sie unter Verwendung der folgenden Beschreibungen die Feldwerte in den Assistenten ein:

2. Compliance- und Überwachungsdatenbank

   |Feld   |Beschreibung|
   |-------|-------|
   |SQL Server Name |Name des Servers, auf dem Sie die Compliance- und Überwachungsdatenbank konfigurieren. <br /> Sie müssen eine Ausnahme auf dem Compliance- und Überwachungsdatenbankcomputer hinzufügen, um eingehenden eingehenden Datenverkehr auf dem SQL Server Port zu aktivieren. Die Standardportnummer ist 1433.|
   |SQL Server Datenbankinstanz    |Name der Datenbankinstanz, in der die Konformitäts- und Überwachungsdaten gespeichert werden. Wenn Sie die Standardinstanz verwenden, müssen Sie dieses Feld leer lassen. Sie müssen auch angeben, wo sich die Datenbankinformationen befinden.|
   |Datenbankname   |Name der Datenbank, in der die Konformitätsdaten gespeichert werden. Sie müssen den Namen der Datenbank notieren, die Sie hier angeben, da Sie diese Informationen in späteren Schritten angeben müssen.|
   |Benutzer oder Gruppe der Berechtigungsdomäne mit Lese-/Schreibzugriff  |Geben Sie den Namen des MBAMAppPool-Benutzers wie in Schritt 2 konfiguriert an.|
   |Domänenbenutzer oder -gruppe mit schreibgeschütztem Zugriff   |Geben Sie den Namen des MBAMROUser-Benutzers wie in Schritt 2 konfiguriert an.|

3. Wiederherstellungsdatenbank.

   |Feld   |Beschreibung|
   |-----|-----|
   |SQL Server Name |Name des Servers, auf dem Sie die Wiederherstellungsdatenbank konfigurieren. Sie müssen eine Ausnahme auf dem Wiederherstellungsdatenbankcomputer hinzufügen, um eingehenden eingehenden Datenverkehr auf dem SQL Server Port zu aktivieren. Die Standardportnummer ist 1433.|
   |SQL Server Datenbankinstanz    |Name der Datenbankinstanz, in der die Wiederherstellungsdaten gespeichert werden. Wenn Sie die Standardinstanz verwenden, müssen Sie dieses Feld leer lassen. Sie müssen auch angeben, wo sich die Datenbankinformationen befinden.|
   |Datenbankname   |Name der Datenbank, in der die Wiederherstellungsdaten gespeichert werden.|
   |Benutzer oder Gruppe der Berechtigungsdomäne mit Lese-/Schreibzugriff  |Domänenbenutzer oder -gruppe mit Lese-/Schreibberechtigung für diese Datenbank, damit die Webanwendungen auf die Daten und Berichte in dieser Datenbank zugreifen können. <br />Wenn Sie einen Benutzer in dieses Feld eingeben, muss dies derselbe Wert wie der Wert im **Domänenkontofeld des Webdienstanwendungspools** auf der Seite **"Webanwendungen konfigurieren"** sein. <br />Wenn Sie eine Gruppe in dieses Feld eingeben, muss der Wert im **Domänenkontofeld des Webdienstanwendungspools** auf der Seite **"Webanwendungen konfigurieren"** Mitglied der Gruppe sein, die Sie in dieses Feld eingeben.|
   
   Wenn Sie Ihre Einträge abgeschlossen haben, wählen Sie **Weiter**. Der Assistent überprüft, ob alle Voraussetzungen für die Datenbanken erfüllt sind.
   
   Wenn die Voraussetzungsprüfung erfolgreich ist, wählen Sie **Weiter** aus, um fortzufahren. Beheben Sie andernfalls alle fehlenden Voraussetzungen, und wählen Sie dann erneut **"Weiter"** aus.

4. Berichte.

   |Feld   |Beschreibung|
   |----|----|
   |SQL Server Reporting Services Instanz  |Instanz von SQL Server Reporting Services, in der die Berichte konfiguriert werden. Wenn Sie die Standardinstanz verwenden, müssen Sie dieses Feld leer lassen.|
   |Domänengruppe "Berichtsrolle" |Geben Sie den Namen des MBAMRUGrp wie in Schritt 2 erwähnt an.|
   |SQL Server Name |Name des Servers, auf dem die Konformitäts- und Überwachungsdatenbank konfiguriert ist.|
   |SQL Server Datenbankinstanz    |Name der Datenbankinstanz, in der die Konformitäts- und Überwachungsdaten konfiguriert sind. Wenn Sie die Standardinstanz verwenden, müssen Sie dieses Feld leer lassen. <br />Sie müssen eine Ausnahme auf dem Computer "Berichte" hinzufügen, um eingehenden Datenverkehr am Port des Berichtsservers zu aktivieren. (Der Standardport ist 80.)|
   |Datenbankname|  Name der Konformitäts- und Überwachungsdatenbank. Standardmäßig lautet der Datenbankname MBAM Compliance Status.|
   |Domänenkonto für Compliance- und Überwachungsdatenbank    |Geben Sie den Namen des MBAMROUser-Benutzers wie in Schritt 2 konfiguriert an.|
   
   Wenn Sie Ihre Einträge abgeschlossen haben, wählen Sie **Weiter**. Der Assistent überprüft, ob alle Voraussetzungen für das Feature "Berichte" erfüllt sind. Wählen Sie Weiter, um fortzufahren. Überprüfen Sie auf der Seite **"Zusammenfassung"** die Features, die hinzugefügt werden.
   
   Weitere Informationen finden Sie im folgenden Artikel: [Konfigurieren der MBAM 2.5-Datenbanken.](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/how-to-configure-the-mbam-25-databases)

### <a name="step-8-configure-the-mbam-25-web-applications-role"></a>Schritt 8: Konfigurieren der Rolle "MBAM 2.5-Webanwendungen"

1. Starten Sie auf dem Server, auf dem Sie die Webanwendungen konfigurieren möchten, den Assistenten für die MBAM-Serverkonfiguration. Sie können **MBAM-Serverkonfiguration** im **Startmenü** auswählen, um den Assistenten zu öffnen.

2. Wählen Sie **"Neue Features hinzufügen",** **"Verwaltungs- und Überwachungswebsite"** und **"Self-Service-Portal"** und dann **"Weiter"** aus. Der Assistent überprüft, ob alle Voraussetzungen für die Datenbanken erfüllt sind.

3. Wenn die Voraussetzungsprüfung erfolgreich ist, wählen Sie **Weiter** aus, um fortzufahren. Beheben Sie andernfalls alle fehlenden Voraussetzungen, und wählen Sie dann **erneut "Voraussetzungen überprüfen" aus.**

4. Verwenden Sie die folgenden Beschreibungen, um die Feldwerte im Assistenten einzugeben.

   |Feld   |Beschreibung|
   |-----|-----|
   |Sicherheitszertifikat    |Wählen Sie in Schritt 3 ein zuvor erstelltes Zertifikat aus, um optional die Kommunikation zwischen den Webdiensten und dem Server zu verschlüsseln, auf dem Sie die Verwaltungs- und Überwachungswebsite konfigurieren. Wenn Sie "Kein Zertifikat verwenden" auswählen, ist Ihre Webkommunikation möglicherweise nicht sicher.|
   |Hostname   |Name des Hostcomputers, auf dem Sie die Verwaltungs- und Überwachungswebsite konfigurieren. <br />Es muss nicht der Hostname des Computers sein, er kann beliebig sein. Wenn sich der Hostname jedoch vom Netbios-Namen des Computers unterscheidet, müssen Sie einen A-Eintrag erstellen und sicherstellen, dass der SPN den benutzerdefinierten Hostnamen und nicht den Netbios-Namen verwendet. Dies ist in Lastenausgleichsszenarien üblich.|
   |Installationspfad   |Pfad, unter dem Sie die Verwaltungs- und Überwachungswebsite installieren.|
   |Port    |Portnummer, die für die Websitekommunikation verwendet werden soll. <br /> Sie müssen eine Firewallausnahme festlegen, um die Kommunikation über den angegebenen Port zu ermöglichen.|
   |Domänenkonto und Kennwort des Webdienstanwendungspools    |Geben Sie das Benutzerkonto und das Kennwort des MBAMAppPool-Benutzers wie in Schritt 2 konfiguriert an. <br /> Um die Sicherheit zu verbessern, legen Sie das in den Anmeldeinformationen angegebene Konto auf eingeschränkte Benutzerrechte fest. Legen Sie außerdem das Kennwort des Kontos so fest, dass es nie abläuft.|

5. Stellen Sie sicher, dass das integrierte IIS_IUSRS konto oder das Anwendungspoolkonto dem Client nach der **Authentifizierung** und der Anmeldung als lokale Sicherheitseinstellungen **für einen Batchauftrag** hinzugefügt wurde.

   Um zu überprüfen, ob das Konto den lokalen Sicherheitseinstellungen hinzugefügt wurde, öffnen Sie den Editor für **lokale Sicherheitsrichtlinien,** erweitern Sie den Knoten **"Lokale Richtlinien",** wählen Sie den Knoten **"Zuweisung von Benutzerrechten"** aus, und wählen Sie **nach der Authentifizierung** die Identität eines Clients aus, und melden Sie sich im rechten Bereich **als Batchauftragsrichtlinien an.**

6. Verwenden Sie die folgenden Feldbeschreibungen, um die Verbindungsinformationen im Assistenten für die Compliance- und Überwachungsdatenbank zu konfigurieren.
   |Feld   |Beschreibung|
   |------|------|
   |SQL Server Name |Name des Servers, auf dem die Konformitäts- und Überwachungsdatenbank konfiguriert ist.|
   |SQL Server Datenbankinstanz    |Name der Instanz von SQL Server (z. \<Server Name\> B. ) und für die die Konformitäts- und Überwachungsdatenbank konfiguriert ist. Lassen Sie diesen Wert leer, wenn Sie die Standardinstanz verwenden.|
   |Datenbankname   |Name der Konformitäts- und Überwachungsdatenbank. Standardmäßig ist dies "MBAM Compliance Status".|

7. Verwenden Sie die folgenden Feldbeschreibungen, um die Verbindungsinformationen im Assistenten für die Wiederherstellungsdatenbank zu konfigurieren.
   |Feld   |Beschreibung|
   |----|----|
   |SQL Server Name |Name des Servers, auf dem die Wiederherstellungsdatenbank konfiguriert ist.|
   |SQL Server Datenbankinstanz    |Name der Instanz von SQL Server (z. \<Server Name\> B. ), für die die Wiederherstellungsdatenbank konfiguriert ist. Lassen Sie diesen Wert leer, wenn Sie die Standardinstanz verwenden.|
   |Datenbankname   |Name der Wiederherstellungsdatenbank. Standardmäßig ist dies "MBAM-Wiederherstellung und Hardware".|

8. Verwenden Sie die folgenden Beschreibungen, um die Feldwerte im Assistenten einzugeben, um die Verwaltungs- und Überwachungswebsite zu konfigurieren.
   |Feld   |Beschreibung|
   |----|----|
   |Erweiterte Helpdesk-Rollendomänengruppe |Geben Sie den Namen der MBAMAdvHelpDsk-Gruppe wie in Schritt 2 konfiguriert an.|
   |Helpdesk-Rollendomänengruppe  |Geben Sie den Namen der MBAMHelpDsk-Gruppe wie in Schritt 2 konfiguriert an.|
   |Verwenden System Center Configuration Manager-Integration |Aktivieren Sie dieses Kontrollkästchen, um dieses Kontrollkästchen zu deaktivieren.     |
   |Domänengruppe "Berichtsrolle" |Geben Sie den Namen der MBAMRUGrp-Gruppe wie in Schritt 2 konfiguriert an.    |
   |SQL Server Reporting Services URL   |Geben Sie die Webdienst-URL für den SSRS-Server an, auf dem die MBAM-Berichte konfiguriert sind. Sie finden diese Informationen, indem Sie sich bei Reporting Services Configuration Manager auf dem Datenbankserver anmelden. <br /> Beispiel für einen vollqualifizierten Domänennamen: https://MyReportServer.Contoso.com/ReportServer <br />Beispiel für einen benutzerdefinierten Hostnamen: https://MyReportServer/ReportServer|
   |Virtuelles Verzeichnis   |Virtuelles Verzeichnis der Verwaltungs- und Überwachungswebsite. Dieser Name entspricht dem physischen Verzeichnis der Website auf dem Server und wird an den Hostnamen der Website angefügt. Zum Beispiel: <br />http(s):// *\<host name\>* : *\<port\>* /HelpDesk/ <br />Wenn Sie kein virtuelles Verzeichnis angeben, wird der Wert HelpDesk verwendet.     |

9. Verwenden Sie die folgende Beschreibung, um die Feldwerte im Assistenten einzugeben, um das Self-Service Portal zu konfigurieren.

   |Feld   |Beschreibung|
   |----|----|
   |Virtuelles Verzeichnis   |Virtuelles Verzeichnis der Webanwendung. Dieser Name entspricht dem physischen Verzeichnis der Website auf dem Server und wird an den Hostnamen der Website angefügt. Zum Beispiel:<br />http(s):// *\<host name\>* : *\<port\>* /SelfService/<br /> Wenn Sie kein virtuelles Verzeichnis angeben, wird der Wert "SelfService" verwendet.|

10. Wenn Sie Ihre Einträge abgeschlossen haben, wählen Sie **Weiter**. Der Assistent überprüft, ob alle Voraussetzungen für die Webanwendungen erfüllt sind.

11. Wählen Sie **"Weiter"** aus, um fortzufahren.

12. Überprüfen Sie auf der Seite **"Zusammenfassung"** die Features, die hinzugefügt werden.

13. Wählen Sie **"Hinzufügen"** aus, um die Webanwendungen zum Server hinzuzufügen, und wählen Sie dann **"Schließen"** aus.

## <a name="customizing-and-validating-steps-after-installing-mbam-25-server-software"></a>Anpassen und Überprüfen der Schritte nach der Installation von MBAM 2.5-Serversoftware

### <a name="step-9-customizing-the-self-server-portal-for-your-organization"></a>Schritt 9: Anpassen des Self-Server-Portals für Ihre Organisation

Informationen zum Anpassen des Self-Service-Portals durch Hinzufügen eines benutzerdefinierten Hinweistexts, Ihres Unternehmensnamens, Zeiger auf weitere Informationen usw. finden Sie unter [Customizing the Self-Service Portal for Your Organization.](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/customizing-the-self-service-portal-for-your-organization)
 
### <a name="step-10-configure-the-self-server-portal-if-client-computers-cannot-access-the-cdn"></a>Schritt 10: Konfigurieren des Self-Server-Portals, wenn Clientcomputer nicht auf die CDN 

Bestimmen Sie, ob Ihre Clientcomputer Zugriff auf die Microsoft AJAX-Content Delivery Network (CDN) haben. Die CDN ermöglicht dem Self-Service-Portal den Zugriff auf bestimmte JavaScript-Dateien. Wenn Sie das Self-Service Portal nicht konfigurieren, wenn Clientcomputer nicht auf die CDN zugreifen können, werden nur der Unternehmensname und das Konto angezeigt, unter dem sich der Benutzer angemeldet hat. Es wird keine Fehlermeldung angezeigt.

Führen Sie eine der folgenden Aktionen aus:

* Wenn Ihre Clientcomputer Zugriff auf die CDN haben, führen Sie nichts aus. Die Konfiguration des Self-Service Portals ist abgeschlossen.

* Wenn Ihre Clientcomputer keinen Zugriff auf die CDN haben, führen Sie die Schritte unter [Konfigurieren des Self-Service-Portals aus, wenn Clientcomputer nicht auf microsoft Content Delivery Network zugreifen können.](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/how-to-configure-the-self-service-portal-when-client-computers-cannot-access-the-microsoft-content-delivery-network)

### <a name="step-11-validate-the-mbam-25-server-feature-configuration"></a>Schritt 11: Überprüfen der Konfiguration der MBAM 2.5-Serverfeatures 

Führen Sie die folgenden Schritte aus, um die MBAM Server-Bereitstellung für die Verwendung der eigenständigen Topologie zu überprüfen.

1. Wählen Sie auf jedem Server, auf dem ein MBAM-Feature bereitgestellt wird, die Option **"Systemsteuerungsprogramme**  >  ****  >  **und Features"** aus. Stellen Sie sicher, dass die **Microsoft BitLocker-Verwaltung und -Überwachung** in der Liste **"Programme und Features"** angezeigt wird.
   > [!Note]
   > Um die Überprüfung durchzuführen, müssen Sie ein Domänenkonto verwenden, das über Administratoranmeldeinformationen für den lokalen Computer auf jedem Server verfügt.

2. Öffnen Sie auf dem Server, auf dem die Wiederherstellungsdatenbank konfiguriert ist, SQL Server Management Studio, und überprüfen Sie, ob die **MBAM-Wiederherstellungs- und Hardwaredatenbank** konfiguriert ist.

3. Öffnen Sie auf dem Server om, auf dem die Compliance- und Überwachungsdatenbank konfiguriert ist, SQL Server Management Studio, und überprüfen Sie, ob die MBAM-Konformitätsstatusdatenbank konfiguriert ist.

4. Öffnen Sie auf dem Server, auf dem das Berichtfeature konfiguriert ist, einen Webbrowser mithilfe von Administratoranmeldeinformationen, und navigieren Sie zur Homepage der SQL Server Reporting Services Website.
   
   Der Standardmäßige Startseitenspeicherort einer SQL Server Reporting Services Websiteinstanz lautet wie folgt: http(s):// *\<MBAM Reports Server Name\>* : *\<port\>* /Reports.aspx
   
   Um die tatsächliche URL zu finden, verwenden Sie das Configuration Manager-Tool für Reporting Services, und wählen Sie die Instanzen aus, die Sie während des Setups angegeben haben.
   
5. Stellen Sie sicher, dass ein Berichtsordner mit dem Namen "Microsoft BitLocker Administration and Monitoring" eine Datenquelle mit dem Namen "MaltaDataSource" enthält. Diese Datenquelle enthält Ordner mit Namen, die Gebietsschemas der Sprache darstellen (z. B. "en-us"). Die Berichte befinden sich in den Sprachordnern.

   > [!Note]
   > Wenn SQL Server Reporting Services (SSRS) als benannte Instanz konfiguriert wurde, sollte die URL wie folgt aussehen: http(s):// \<MBAM Reports Server Name\> : \<port\> /Reports_\<SSRS Instance Name\>
   >
   > Wenn SSRS nicht für die Verwendung von Ssl (Secure Socket Layer) konfiguriert wurde, wird die URL für die Berichte bei der Installation des MBAM-Servers auf "HTTP" anstelle von "HTTPS" festgelegt. Wenn Sie dann zur Verwaltungs- und Überwachungswebsite (auch als Helpdesk bezeichnet) navigieren und einen Bericht auswählen, erhalten Sie die folgende Meldung: "Nur sicherer Inhalt wird angezeigt." Wählen Sie zum Anzeigen des Berichts **"Alle Inhalte anzeigen" aus.**

6. Führen Sie auf dem Server, auf dem das Feature für die Verwaltungs- und Überwachungswebsite konfiguriert ist, den Server-Manager aus, navigieren Sie zu **"Rollen",** und wählen Sie dann **Webserver (IIS)**  >  **Internetinformationsdienste -Manager (IIS)** aus.

7. Navigieren Sie in **"Verbindungen"** zu \<computer name\> **"Sites**  >  **Microsoft BitLocker Administration and Monitoring", und**wählen Sie sie aus. Stellen Sie sicher, dass Folgendes aufgeführt ist:

   * MBAMAdministrationService
   * MBAMComplianceStatusService
   * MBAMRecoveryAndHardwareService

8. Öffnen Sie auf dem Server, auf dem die Verwaltungs- und Überwachungswebsite und Self-Service Portal konfiguriert sind, einen Webbrowser mithilfe von Administratoranmeldeinformationen.

9. Navigieren Sie zu den folgenden Websites, um zu überprüfen, ob sie erfolgreich geladen wurden:
   * https(s):// \<MBAM Administration Server Name\> : \<port\> /HelpDesk/ (bestätigen Sie jeden Link für Navigation und Berichte)
   * http(s):// \<MBAM Administration Server Name\> : \<port\> /SelfService/

   > [!Note]
   > Es wird davon ausgegangen, dass Sie die Serverfeatures auf dem Standardport ohne Netzwerkverschlüsselung konfiguriert haben. Wenn Sie die Serverfeatures für einen anderen Port oder ein anderes virtuelles Verzeichnis konfiguriert haben, ändern Sie die URLs so, dass sie den entsprechenden Port enthalten. Beispiel: http(s):// \<host name\> : \<port\> /HelpDesk/ http(s):// \<host name\> : / Wenn die \<port\> / \<virtualdirectory\> Serverfeatures für die Verwendung der Netzwerkverschlüsselung konfiguriert wurden, ändern Sie http:// in https://.
   
10. Navigieren Sie zu den folgenden Webdiensten, um zu überprüfen, ob sie erfolgreich geladen wurden. Eine Seite wird geöffnet, um anzugeben, dass der Dienst ausgeführt wird. Die Seite zeigt jedoch keine Metadaten an.

    * http(s):// \<MBAM Administration Server Name> : \<port> /MBAMAdministrationService/AdministrationService.svc
    * http(s):// \<MBAM Administration Server Name> : \<port> /MBAMUserSupportService/UserSupportService.svc
    * http(s):// \<MBAM Administration Server Name> : \<port> /MBAMComplianceStatusService/StatusReportingService.svc
    * http(s):// \<MBAM Administration Server Name> : \<port> /MBAMRecoveryAndHardwareService/CoreService.svc

### <a name="step-12-configure-the-mbam-group-policy-templates"></a>Schritt 12: Konfigurieren der Gruppenrichtlinienvorlagen für MBAM

Um MBAM bereitzustellen, müssen Sie Gruppenrichtlinieneinstellungen festlegen, die MBAM-Implementierungseinstellungen für die BitLocker-Laufwerkverschlüsselung definieren. Um diese Aufgabe abzuschließen, müssen Sie die MBAM-Gruppenrichtlinienvorlagen auf einen Server oder eine Arbeitsstation kopieren, auf dem die Gruppenrichtlinien-Verwaltungskonsole (Group Policy Management Console, GPMC) oder die erweiterte Gruppenrichtlinienverwaltung (Advanced Group Policy Management, AGPM) ausgeführt werden kann, und dann die Einstellungen bearbeiten.

> [!Important]
> Ändern Sie die Gruppenrichtlinieneinstellungen im **BitLocker-Laufwerkverschlüsselungsknoten** nicht, oder MBAM funktioniert nicht ordnungsgemäß. Wenn Sie die Gruppenrichtlinieneinstellungen im **Knoten MDOP MBAM (BitLocker-Verwaltung)** konfigurieren, konfiguriert MBAM automatisch die **BitLocker-Laufwerkverschlüsselungseinstellungen** für Sie.
 
#### <a name="copying-the-mbam-25-group-policy-templates"></a>Kopieren der Gruppenrichtlinienvorlagen für MBAM 2.5

Bevor Sie den MBAM-Client installieren, müssen Sie MBAM-spezifische Gruppenrichtlinienobjekte (Group Policy Objects, GPOs) auf die Verwaltungsarbeitsstation kopieren. Diese GPOs definieren MBAM-Implementierungseinstellungen für BitLocker. Sie können die Gruppenrichtlinienvorlagen auf einen beliebigen Server oder jede Arbeitsstation kopieren, bei der es sich um einen unterstützten Windows-basierten Server oder Clientcomputer handelt und auf dem die Gruppenrichtlinien-Verwaltungskonsole (Group Policy Management Console, GPMC) oder die erweiterte Gruppenrichtlinienverwaltung (Advanced Group Policy Management, AGPM) ausgeführt werden kann.

Weitere Informationen finden Sie unter [Kopieren der Gruppenrichtlinienvorlagen für MBAM 2.5.](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/copying-the-mbam-25-group-policy-templates)
 
#### <a name="editing-mbam-25-gpo-settings"></a>Bearbeiten von MBAM 2.5 GPO-Einstellungen

Nachdem Sie die erforderlichen Gruppenrichtlinienobjekte erstellt haben, müssen Sie die Gruppenrichtlinieneinstellungen für MBAM auf den Clientcomputern Ihrer Organisation bereitstellen. Zum Anzeigen und Erstellen von Gruppenrichtlinienobjekten müssen Die Gruppenrichtlinien-Verwaltungskonsole (Group Policy Management Console, GPMC) oder die erweiterte Gruppenrichtlinienverwaltung (Advanced Group Policy Management, AGPM) installiert sein.

Weitere Informationen finden Sie unter [Bearbeiten der Gruppenrichtlinienanforderungen für MBAM 2.5 Einstellungen](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/editing-the-mbam-25-group-policy-settings) und Planen von [MBAM 2.5-Gruppenrichtlinien.](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/planning-for-mbam-25-group-policy-requirements)
 
### <a name="step-13-deploying-the-mbam-25-client"></a>Schritt 13: Bereitstellen des MBAM 2.5-Clients

Je nachdem, wann Sie die Microsoft BitLocker Administration and Monitoring Client-Software bereitstellen, können Sie BitLocker auf einem Computer in Ihrer Organisation aktivieren, bevor der Benutzer den Computer empfängt, oder danach, indem Sie die Gruppenrichtlinie konfigurieren und die MBAM-Clientsoftware mithilfe eines Unternehmenssoftware-Bereitstellungssystems bereitstellen.
 
#### <a name="deploy-the-mbam-client-to-desktop-or-portable-computers"></a>Bereitstellen des MBAM-Clients auf Desktopcomputern oder tragbaren Computern

Nach dem Konfigurieren von Gruppenrichtlinieneinstellungen können Sie ein Enterprise-Softwarebereitstellungssystemprodukt wie Microsoft System Center 2012 Configuration Manager oder Active Directory Domain Services (AD DS) verwenden, um die MBAM-Clientinstallation Windows Installer-Dateien auf Zielcomputern bereitzustellen. Sie können entweder die 32-Bit- oder 64-Bit-MbamClientSetup.exe dateien oder die 32-Bit- oder 64-Bit-MBAMClient.msi-Dateien verwenden. Diese werden zusammen mit der MBAM-Clientsoftware bereitgestellt.

Weitere Informationen finden Sie unter [So stellen Sie den MBAM-Client auf Desktop- oder Laptopcomputern bereit.](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/how-to-deploy-the-mbam-client-to-desktop-or-laptop-computers-mbam-25)
 
#### <a name="deploy-the-mbam-client-as-part-of-a-windows-deployment"></a>Bereitstellen des MBAM-Clients als Teil einer Windows Bereitstellung

In Organisationen, in denen Computer zentral empfangen und konfiguriert werden, können Sie den MBAM-Client installieren, um die BitLocker-Laufwerkverschlüsselung auf jedem Computer zu verwalten, bevor Benutzerdaten darauf geschrieben werden. Der Vorteil dieses Prozesses besteht darin, dass jeder Computer dann BitLocker-kompatibel ist. Diese Methode ist nicht auf Benutzeraktionen angewiesen, da der Administrator den Computer bereits verschlüsselt hat. Eine wichtige Annahme für dieses Szenario ist, dass die Richtlinie der Organisation darin besteht, ein Unternehmensimage Windows zu installieren, bevor der Computer an den Benutzer übermittelt wird. Wenn die Gruppenrichtlinieneinstellungen so konfiguriert sind, dass eine PIN erforderlich ist, werden Benutzer aufgefordert, eine PIN festzulegen, nachdem sie die Richtlinie erhalten haben.

Weitere Informationen finden Sie unter [How to Deploy the MBAM Client as Part of a Windows Deployment](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/how-to-enable-bitlocker-by-using-mbam-as-part-of-a-windows-deploymentmbam-25).
 
#### <a name="how-to-deploy-the-mbam-client-by-using-a-command-line"></a>So stellen Sie den MBAM-Client über eine Befehlszeile bereit

Weitere Informationen finden Sie unter ["Bereitstellen des MBAM-Clients mithilfe einer Befehlszeile".](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/how-to-deploy-the-mbam-client-by-using-a-command-line)

#### <a name="post-deployment-of-clients"></a>Nach der Bereitstellung von Clients

Nachdem Sie die Bereitstellungsaktivität abgeschlossen haben, sollten Sie die folgenden Protokolle überprüfen und ermitteln, ob die Clients erfolgreich an die MBAM-Datenbank berichten.

## <a name="faq"></a>FAQ

### <a name="how-to-create-a-load-balanced-iis-servers"></a>So erstellen Sie IIS-Server mit Lastenausgleich

* SPN muss nur für den Anzeigenamen (z. B. bitlocker.corp.net) registriert werden und darf nicht auf einzelnen IIS-Servern registriert werden.

* Wenn ein Zertifikat verwendet wird, müssen sowohl FQDN- als auch NetBIOS-Namen in das Feld **"Alternativer Antragstellername"** für alle IIS-Server in der Lastenausgleichsgruppe und auch als Anzeigename (z. B. bitlocker.corp.net) eingegeben werden. Andernfalls wird das Zertifikat vom Browser als nicht vertrauenswürdig gemeldet, wenn Sie Adressen mit Lastenausgleich durchsuchen.

Weitere Informationen finden Sie unter [IIS-Netzwerklastenausgleich](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/planning-for-mbam-25-high-availability#a-href-idbkmk-load-balanceaiis-network-load-balancing) und [Registrieren von SPNs für das Anwendungspoolkonto.](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/planning-how-to-secure-the-mbam-websites#registering-spns-for-the-application-pool-account)

### <a name="how-to-configure-a-certificate"></a>Konfigurieren eines Zertifikats

* Sie müssen über zwei Zertifikate verfügen. Ein Zertifikat wird für SQL Server und das andere für IIS verwendet. Sie müssen vor dem Starten der MBAM-Installation installiert werden.

* Es wird empfohlen, das Zertifikat mithilfe des Installationsprogramms der IIS-Konfiguration hinzuzufügen, anstatt die datei web.config manuell zu bearbeiten.

* Das Zertifikat wird vom MBAM-Configurator nicht akzeptiert, wenn das Feld "Ausgestellt an" auf dem Zertifikat nicht mit dem Namen des Servers übereinstimmt. Erstellen Sie in diesem Fall vorübergehend ein selbstsignierbares Zertifikat aus der IIS-Konsole, und verwenden Sie es im Configurator. Dadurch wird sichergestellt, dass die Web-Apps für SSL und HTTPS installiert sind. Danach können Sie das Zertifikat aus IIS-Bindungen für die MBAM-Website in eine ändern.

### <a name="the-sql-permissions-requirement-for-installation"></a>Die SQL Berechtigungsanforderung für die Installation

Erstellen Sie ein Konto für DEN MBAM-App-Pool, und erteilen Sie ihm nur Die Berechtigungen "SecurityAdmin", "Public" und "DBCreator".

Weitere Informationen finden Sie unter [MBAM-Datenbankkonfiguration – Mindestberechtigungen.](https://blogs.technet.microsoft.com/dubaisec/2016/02/02/mbam-database-configuration-minimum-permissions/)

> [!Note]
> * In einigen Situationen sind weitere Berechtigungen für die anfänglichen Installations- und Upgradevorgänge erforderlich.
> * Verwenden Sie ein Konto mit temporärer SA für die Installation.
> * Starten Sie den Configurator nicht im Kontext eines Benutzerkontos (Run As), das nicht über genügend Berechtigungen zum Vornehmen von Änderungen an SQL Server verfügt, da dies Installationsfehler verursacht.
> * Sie müssen mit einem Konto angemeldet sein, das über Berechtigungen für SQL Server verfügt. Nur SQL Server Datenbanken können erstellt oder aktualisiert werden, indem MBAM Configurator remote ausgeführt wird. Für SSRS-Server müssen Sie MBAM installieren und Configurator lokal ausführen, um die MBAM-SSRS-Berichte zu installieren oder zu aktualisieren.

### <a name="the-permission-required-for-spn-registration"></a>Die für die SPN-Registrierung erforderliche Berechtigung

Ein Konto, das für die IIS-Portalinstallation verwendet wird, muss über die Berechtigungen "ServicePrincipalName" und "Write Validated SPN" verfügen. Ohne diese Berechtigungen gibt die Installation eine Warnmeldung zurück, die besagt, dass der SPN nicht registriert werden kann.

> [!Note]
> Diese Warnmeldung wird zweimal angezeigt. Dies bedeutet nicht, dass im SPN zwei Objekte registriert sein müssen.

Weitere Informationen finden Sie unter [MBAM Setup schlägt mit der Fehlermeldung "SpN verzögert registrieren" fehl.](https://support.microsoft.com/help/2754138/)

### <a name="did-i-have-to-update-the-admx-templates-to-the-latest-version"></a>Musste ich die ADMX-Vorlagen auf die neueste Version aktualisieren?

Im MBAM-Stammknoten für GPO werden mehrere Betriebssystemoptionen angezeigt, nachdem Sie die ADMX-Vorlagen auf die neuesten Versionen aktualisiert haben. Beispielsweise Windows Version 7, Windows 8.1 und Windows 10, Version 1511 und höher.

Weitere Informationen zum Aktualisieren der ADMX-Vorlagen finden Sie in den folgenden Artikeln:
* [Herunterladen und Bereitstellen von MDOP-Gruppenrichtlinienvorlagen (ADMX-Dateien)](https://docs.microsoft.com/microsoft-desktop-optimization-pack/solutions/how-to-download-and-deploy-mdop-group-policy--admx--templates)
* [Planen der Gruppenrichtlinienanforderungen für MBAM 2.5](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/planning-for-mbam-25-group-policy-requirements)
* [Administrative Vorlagen für Gruppenrichtlinien für Microsoft Desktop Optimization Pack](https://www.microsoft.com/en-us/download/details.aspx?id=55531)
