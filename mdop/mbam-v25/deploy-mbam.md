---
title: Bereitstellen von MBAM 2,5 in einer eigenständigen Konfiguration
description: Hier erfahren Sie, wie Sie MBAM 2,5 in einer eigenständigen Konfiguration bereitstellen.
author: Deland-Han
ms.reviewer: dcscontentpm
manager: dansimp
ms.author: delhan
ms.sitesec: library
ms.prod: w10
ms.date: 09/16/2019
ms.openlocfilehash: 905eb7a40483a7a7b499d6dced8472331c87b838
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811752"
---
# Bereitstellen von MBAM 2,5 in einer eigenständigen Konfiguration

Dieser Artikel enthält Schritt-für-Schritt-Anleitungen zum Installieren der Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) 2,5 in einer eigenständigen Konfiguration. In diesem Leitfaden wird eine Konfiguration mit zwei Servern verwendet. Einer der beiden Server ist ein Datenbankserver, auf dem Microsoft SQL Server 2012 ausgeführt wird. Dieser Server hostet die MBAM-Datenbanken und-Berichte. Der zusätzliche Server ist ein Windows Server 2012-Webserver, der "Verwaltungs-und Überwachungsserver" und "Self-Service-Portal" hostet.

## Vorbereitungsschritte vor der Installation der MBAM 2,5-Server Software

### Schritt 1: Installieren und Konfigurieren von Servern

Bevor wir mit der Konfiguration von MBAM 2,5 beginnen, müssen wir sicherstellen, dass beide Server gemäß den Systemanforderungen für MBAM konfiguriert sind. Sehen Sie sich die [Mindestsystemanforderungen für MBAM an](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/mbam-25-supported-configurations#-mbam-server-system-requirements), und wählen Sie eine Konfiguration aus, die diese Anforderungen erfüllt. 

#### Schritt 1,1: Bereitstellen von Voraussetzungen für Datenbank und Berichtsserver

1. Installieren und konfigurieren Sie einen Server mit dem Betriebssystem Windows Server 2008 R2 (oder höher).

2. Installieren Sie Windows PowerShell 3,0.

3. Installieren Sie Microsoft SQL Server 2008 R2 oder eine neuere Version, die das neueste Service Pack enthält. Wenn Sie eine neue Instanz von SQL Server für MBAM installieren, stellen Sie sicher, dass der von Ihnen installierte SQL Server die SQL_Latin1_General_CP1_CI_AS Sortierung umfasst. Sie müssen die folgenden SQL Server-Features installieren:

    * Datenbankmodul
    * Reporting Services
    * Client Tools-Konnektivität
    * Verwaltungs Tools – abgeschlossen

    > [!Note]
    > Optional können Sie auch das Feature " [transparente Datenverschlüsselung (DSA)" in SQL Server](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/mbam-25-security-considerations)installieren.

    SQL Server Reporting Services muss im systemeigenen Modus und nicht im Modus "nicht konfiguriert" oder "SharePoint" installiert und konfiguriert sein.

    ![Die erforderlichen SQL Server-Features](images/deploying-MBAM-1.png)

4. Wenn Sie beabsichtigen, SSL für die Verwaltungs-und Überwachungs Website zu verwenden, stellen Sie sicher, dass Sie SQL Server Reporting Services (SSRS) so konfigurieren, dass das SSL-Protokoll (Secure Sockets Layer) verwendet wird, bevor Sie die Websiteverwaltung und Überwachung konfigurieren. Andernfalls verwendet das Feature "Berichte" unverschlüsselten (http)-Datentransport anstatt verschlüsselt (HTTPS).

    Sie können die [Konfiguration von SSL-Verbindungen](https://docs.microsoft.com/sql/reporting-services/security/configure-ssl-connections-on-a-native-mode-report-server?view=sql-server-2017) auf einem Berichtsserver im systemeigenen Modus ausführen, um SSL auf dem Berichtsserver zu konfigurieren.
    
    > [!Note]
    > Sie können dem SQL Server-Installationshandbuch für ihre jeweilige Version von SQL Server folgen, um SQL Server zu installieren. Die Links sind wie folgt:
        > * [SQL Server 2014](https://docs.microsoft.com/sql/sql-server/install/planning-a-sql-server-installation?view=sql-server-2014)
        > * [SQL Server 2012](https://docs.microsoft.com/previous-versions/sql/sql-server-2012/bb500442(v=sql.110))
        > * [SQL Server 2008 R2](https://docs.microsoft.com/previous-versions/sql/sql-server-2012/bb500442(v=sql.110))

5. Stellen Sie bei der nach der Installation von SQL Server sicher, dass das Benutzerkonto in SQL Server bereitgestellt wird, und weisen Sie dem Benutzer die folgenden Berechtigungen zu, der die MBAM-Datenbank und die Berichts Rollen auf dem Daten Bank Server konfiguriert.

    Rollen für die Instanz von SQL Server:
        
    * dbcreator
    * processadmin

    Rechte für die Instanz von SQL Server Reporting Services:
    
    * Erstellen von Ordnern
    * Veröffentlichen von Berichten

Der Datenbankserver ist bereit für die Konfiguration von MBAM 2,5-Rollen. Wechseln Sie zum nächsten Server.

#### Schritt 1,2: Bereitstellen von Voraussetzungen für die Verwaltung und den Monitoring Server

Wählen Sie einen Server aus, der die Hardwarekonfiguration erfüllt, wie im [MBAM-System Anforderungsdokument](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/mbam-25-supported-configurations#-mbam-server-system-requirements)erläutert. Es muss Windows Server 2008 R2 oder ein höheres Betriebssystem zusammen mit den neuesten Service Packs und Updates ausgeführt werden. Nachdem der Server bereit ist, installieren Sie die folgenden Rollen und Features:

##### Rollen

* Web Server (IIS)-Verwaltungstools (IIS-Verwaltungsskripts und-Tools auswählen)

* Webserver-Rollendienste

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

    * Web Service IIS-Verwaltungs Tools

##### Feature

* .NET Framework 4,5-Features
  
  * Microsoft .NET Framework 4,5
  
    Für Windows Server 2012 oder Windows Server 2012 R2 ist .NET Framework 4,5 bereits für diese Versionen von Windows Server installiert. Sie müssen Sie jedoch aktivieren.
  
    Für Windows Server 2008 R2 ist .NET Framework 4,5 nicht im Lieferumfang von Windows Server 2008 R2 enthalten. Daher müssen Sie .NET Framework 4,5 herunterladen und separat installieren.
  
  * WCF-Aktivierung<br />
    HTTP-Aktivierung<br />
    Nicht-HTTP-Aktivierung
  
  * TCP-Aktivierung
  
  * Windows-Prozessaktivierungsdienst:<br />
    Prozessmodell<br />
    .NET Framework-Umgebung<br />
    Konfigurations-APIs

Damit das Self-Service-Portal funktioniert, sollten Sie auch [ASP.NET MVC 4,0 herunterladen und installieren](https://go.microsoft.com/fwlink/?linkid=392271).

Im nächsten Schritt erstellen Sie die erforderlichen MBAM-Benutzer und-Gruppen in Active Directory.

### Schritt 2: Erstellen von Benutzern und Gruppen in den Active Directory-Domänendiensten
 
Als Teil der Voraussetzungen müssen Sie bestimmte Rollen und Konten definieren, die in MBAM verwendet werden, um Sicherheit und Zugriffsrechte für bestimmte Server und Features bereitzustellen, beispielsweise die Datenbanken, die auf der Instanz von SQL Server ausgeführt werden, und die Webanwendungen, die auf dem Verwaltungs-und Überwachungs Server ausgeführt werden.

Erstellen Sie die folgenden Gruppen und Benutzer in Active Directory. (Sie können einen beliebigen Namen für die Gruppen und Benutzer verwenden.) Benutzer müssen nicht über größere Benutzerrechte verfügen. Ein Domänenbenutzerkonto ist ausreichend. Sie müssen während der Konfiguration von MBAM 2,5 den Namen dieser Gruppen angeben:

* **MBAMAppPool**  

  **Typ**: Domänenbenutzer

  **Beschreibung**: Domänenbenutzer mit Lese-oder Schreibberechtigung für die Compliance-und Überwachungsdatenbank und die Wiederherstellungsdatenbank, damit die Webanwendungen auf die Daten und Berichte in diesen Datenbanken zugreifen können. Sie wird auch vom Anwendungspool für die Webanwendungen verwendet.

  **Konto Rollen (während der Konfiguration von MBAM)**:

  1. Domänenkonto des Webdienst-Anwendungspools

  2. Konformitäts-und Überwachungsdatenbank-und Wiederherstellungsdatenbank, Benutzer für Berichte lesen/schreiben

* **MBAMROUser**

  **Typ**: Domänenbenutzer

  **Beschreibung**: Domänenbenutzer, der über schreibgeschützten Zugriff auf die Compliance-und Überwachungsdatenbank verfügt, damit die Berichte auf die Kompatibilitäts-und Überwachungsdaten in dieser Datenbank zugreifen können. Es ist auch das Domänenbenutzerkonto, das von der lokalen SQL Server Reporting Services-Instanz für den Zugriff auf die Compliance-und Überwachungsdatenbank verwendet wird.

  **Konto Rollen (während der Konfiguration von MBAM)**:

  1. Konformitäts-und Überwachungsdatenbank-schreibgeschützter Benutzer für Berichte

  2. Kompatibilitäts-und Überwachungsdatenbank-Domänenbenutzerkonto

* **MBAMAdvHelpDsk**

  **Typ**: Domänengruppe

  **Beschreibung**: MBAM Advanced Helpdesk users Access Group: Domain User Group, deren Mitglieder Zugriff auf alle Bereiche der Verwaltungs-und Überwachungs Website haben. Benutzer, die über diese Rolle verfügen, müssen nur den Wiederherstellungsschlüssel eingeben, nicht die Domäne des Benutzers und den Benutzernamen, wenn er Benutzern beim Wiederherstellen Ihrer Laufwerke hilft. Wenn ein Benutzer ein Mitglied der Gruppe MBAM Helpdesk-Benutzer und der Gruppe der erweiterten Helpdesk-Benutzer von MBAM ist, überschreiben die Berechtigungen der Gruppe erweiterte Helpdesk-Benutzer MBAM die Berechtigungen für die MBAM-Helpdesk-Gruppe.

  **Konto Rollen (während der Konfiguration von MBAM)**: MBAM Advanced Helpdesk-Benutzer

* **MBAMHelpDsk**

  **Typ**: Domänengruppe

  **Beschreibung**: MBAM Helpdesk users Access Group: Domänenbenutzergruppe, deren Mitglieder Zugriff auf die Bereiche Manage TPM und Drive Recovery der MBAM-Verwaltungs-und-Überwachungs Website haben. Personen, die diese Rolle besitzen, müssen alle Felder ausfüllen, wenn Sie eine der beiden Optionen verwenden. Dies umfasst die Domäne und den Kontonamen des Benutzers.

  **Konto Rollen (während der Konfiguration von MBAM)**: MBAM Helpdesk-Benutzer

* **MBAMRUGrp**

  **Typ**: Domänengruppe

  **Beschreibung**: Domänenbenutzergruppe, deren Mitglieder schreibgeschützten Zugriff auf die Berichte im Bereich "Berichte" der Website "Verwaltung und Überwachung" haben.

  **Konto Rollen (während der Konfiguration von MBAM)**:

  1. Meldet schreibgeschützte Domänenzugriffs Gruppe

  2. MBAM-Berichtsbenutzer (Access-Gruppe)

### Schritt 3 (optional): Konfigurieren und Installieren des SSL-Zertifikats auf Verwaltungs-und Überwachungs Servern

Obwohl dies optional ist, empfehlen wir dringend, ein Zertifikat zu verwenden, um die Kommunikation zwischen dem MBAM-Client und der Website für Verwaltung und Überwachung sowie den Self-Service-Portal-Websites zu sichern. Es wird nicht empfohlen, aus offensichtlichen Sicherheitsgründen selbstsignierte Zertifikate zu verwenden. Wir empfehlen, dass Sie ein Webserver Typen Zertifikat von einer vertrauenswürdigen Zertifizierungsstelle verwenden. Zu diesem Zweck können Sie den Abschnitt "Verwenden des Zertifikats, das von der Zertifizierungsstelle genehmigt wurde" aus [KB 2754259](https://support.microsoft.com/help/2754259)verweisen.

Nachdem das Zertifikat ausgestellt wurde, sollten Sie das Zertifikat dem persönlichen Speicher des Verwaltungs-und Überwachungsservers hinzufügen. Zum Hinzufügen des Zertifikats öffnen Sie den Zertifikatspeicher auf dem lokalen Computer. Gehen Sie hierzu folgendermaßen vor:

1. Klicken Sie mit der rechten Maustaste auf Start, und wählen Sie dann ausführen aus.

   ![Auswählen ](images/deploying-MBAM-2.png)

2. Geben Sie "MMC.EXE" (ohne die Anführungszeichen) ein, und wählen Sie dann **OK**aus.

   ![Feld "ausführen"](images/deploying-MBAM-3.png) 

3. Wählen Sie **Datei** in der neu geöffneten MMC aus, und wählen Sie dann **Snap-in hinzufügen/entfernen**aus.
   
   ![Auswählen](images/deploying-MBAM-4.png)

4. Heben Sie das **Zertifikat** -Snap-in auf, und wählen Sie dann **Hinzufügen**aus.

   ![Fenster "Snap-Ins hinzufügen oder entfernen"](images/deploying-MBAM-5.png)

5. Wählen Sie die Option **Computer Konto** aus, und wählen Sie dann **weiter**aus.
   
   ![Zertifikat-Snap-in-Fenster](images/deploying-MBAM-6.png)

6. Wählen Sie auf dem nächsten Bildschirm den **lokalen Computer** aus, und wählen Sie dann **Fertig stellen**aus.
   
   ![Fenster "Computer auswählen"](images/deploying-MBAM-7.png)

7. Sie haben jetzt das Zertifikat-Snap-in hinzugefügt. Auf diese Weise können Sie mit Zertifikaten im Zertifikatspeicher Ihres Computers arbeiten.

   ![Fenster "Snap-Ins hinzufügen oder entfernen"](images/deploying-MBAM-8.png)

8. Importieren Sie das Webserverzertifikat in den Zertifikatspeicher Ihres Computers.

   Nachdem Sie nun über Zugriff auf das Zertifikat-Snap-in verfügen, können Sie das Webserverzertifikat in den Zertifikatspeicher Ihres Computers importieren. Führen Sie dazu die nächsten Schritte aus.

9. Öffnen Sie das Snap-in Zertifikate (lokaler Computer), und navigieren Sie zu **persönliche** und dann **Zertifikate**.
   
   ![Snap-in-Fenster "Zertifikate" (lokaler Computer)](images/deploying-MBAM-9.png)

   > [!Note]
   > Das Zertifikat-Snap-in ist möglicherweise nicht aufgeführt. Wenn dies nicht der Fall ist, werden keine Zertifikate installiert.

10. Klicken Sie mit der rechten Maustaste auf **Zertifikate**, wählen Sie **alle Aufgaben**aus, und wählen Sie dann **importieren**aus.

    ![Snap-in-Fenster "Zertifikate" (lokaler Computer)](images/deploying-MBAM-10.png)

11. Wenn der Assistent gestartet wird, wählen Sie **weiter**aus. Navigieren Sie zu der Datei, die Sie erstellt haben, die das Serverzertifikat und den privaten Schlüssel enthält, und wählen Sie dann **weiter**aus.

    ![Fenster "Zertifikat Import-Assistent"](images/deploying-MBAM-11.png)

12. Geben Sie das Kennwort ein, wenn Sie eine Datei für die Datei angegeben haben, als Sie Sie erstellt haben.

   ![Fenster "Kennwort eingeben"](images/deploying-MBAM-12.png)

   > [!Note]
   > Stellen Sie sicher, dass die Option **Schlüssel als exportierbar kennzeichnen** aktiviert ist, wenn Sie das Schlüsselpaar erneut von diesem Computer exportieren können möchten. Als zusätzliche Sicherheitsmaßnahme empfiehlt es sich, diese Option deaktiviert zu lassen, um sicherzustellen, dass niemand eine Sicherungskopie Ihres privaten Schlüssels erstellen kann.
 
13. Wählen Sie **weiter**aus, und wählen Sie dann den **Zertifikatspeicher** aus, in dem Sie das Zertifikat speichern möchten.

    ![Fenster "Zertifikat Import-Assistent"](images/deploying-MBAM-13.png)

    > [!Note]
    > Sie sollten " **persönlich**" auswählen, da es sich um ein Webserverzertifikat handelt. Wenn Sie das Zertifikat in die Zertifizierungshierarchie aufgenommen haben, wird es auch diesem Store hinzugefügt.
 
14. Wählen Sie **weiter**aus, und wählen Sie dann **Fertig stellen**aus.

    ![Fenster "Zertifikat Import-Assistent"](images/deploying-MBAM-14.png)

Nun wird das Serverzertifikat für Ihren Webserver in der Liste der persönlichen Zertifikate angezeigt. Sie wird durch den allgemeinen Namen des Servers gekennzeichnet. (Dies finden Sie im Abschnitt Betreff des Zertifikats.)

Weitere Informationen finden Sie unter:

[Sicherheitsüberlegungen zu MBAM2.5](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/mbam-25-security-considerations)

[Planen der Sicherung von MBAM-Websites](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/planning-how-to-secure-the-mbam-websites)

Im nächsten Schritt müssen Sie einen Dienstprinzipalnamen für das Anwendungspoolkonto registrieren.

### Schritt 4: Konfigurieren des SSL-Zertifikats für MBAM Web Server

Wenn Sie die SSL-Kommunikation zwischen dem Client und dem Server verwenden, sollten Sie sicherstellen, dass das Zertifikat erweiterte Schlüsselverwendung (1.3.6.1.5.5.7.3.1) und (1.3.6.1.5.5.7.3.2) aufweist. Das heißt, Sie sollten sicherstellen, dass die Server Authentifizierung und die Client Authentifizierung hinzugefügt werden.

Wenn beim Versuch, Dienst-URLs zu durchsuchen, ein Zertifikat Fehler angezeigt wird, verwenden Sie ein Zertifikat, das für einen anderen Namen ausgestellt wurde, oder Sie suchen mithilfe einer falschen URL.

Obwohl der Browser Sie möglicherweise mit einer Zertifikat Fehlermeldung auffordert, Sie aber fortsetzen kann, wird der MBAM-Webdienst keine Zertifikat Fehler ignorieren und die Verbindung blockieren. Im MBAM-Ereignisprotokoll des MBAM-Clients werden zertifikatbezogene Fehler festgestellt. Wenn Sie einen Alias zum Herstellen einer Verbindung mit dem Verwaltungs-und Überwachungsserver verwenden, sollten Sie ein Zertifikat für den Aliasnamen ausgeben. Das heißt, der Antragstellername des Zertifikats sollte der Alias Name sein, und der DNS-Name des lokalen Servers sollte dem Feld " **alternativer Name** " des Zertifikats hinzugefügt werden.

Beispiel:

Wenn der virtuelle Name "BitLocker.contoso.com" lautet und der Name der MBAM-Verwaltungs-und-Überwachungsserver "adminserver.contoso.com" lautet, sollte das Zertifikat für BitLocker.contoso.com (Antragstellername) ausgestellt und adminserver.contoso.com dem Feld " **alternativer Name** " des Zertifikats hinzugefügt werden.

Wenn Sie mehrere Verwaltungs-und Überwachungsserver installiert haben, um die Last mithilfe eines Load Balancer auszugleichen, sollten Sie das SSL-Zertifikat für den virtuellen Namen ausgeben. Das heißt, das Feld "Antragstellername" des Zertifikats sollte den virtuellen Namen haben, und die Namen aller lokalen Server sollten im Feld " **Subject Alternative Name** " des Zertifikats hinzugefügt werden.

Beispiel:

Wenn der virtuelle Name "BitLocker.contoso.com" lautet und die Server "adminserver1.contoso.com" und "adminiserver2.contoso.com" sind, sollte das Zertifikat für BitLocker.contoso.com (Antragstellername) und adminserver1.contoso.com ausgestellt werden, und adminiserver2.contoso.com sollte dem Feld **alternativer Name** des Zertifikats hinzugefügt werden.

Die Schritte zum Konfigurieren der SSL-Kommunikation mithilfe von MBAM werden im folgenden Knowledge Base-Artikel beschrieben: [KB 2754259](https://support.microsoft.com/help/2754259).

### Schritt 5: Registrieren von SPNS für das Anwendungspoolkonto und Konfigurieren der beschränkten Delegierung

> [!Note]
> Die beschränkte Delegierung ist nur für 2,5 erforderlich und für 2,5 Service Pack 1 und höher nicht erforderlich.

Damit die MBAM-Server die Kommunikation über die Verwaltungs-und Überwachungs Website und das Self-Service-Portal authentifizieren können, müssen Sie einen Dienstprinzipalnamen (Service Principal Name, SPN) für den Hostnamen unter dem Domänenkonto registrieren, das Sie für den Webanwendungspool verwenden. Der folgende Artikel enthält Schritt-für-Schritt-Anweisungen zum Registrieren von SPNs: [planen, wie die MBAM-Websites geschützt werden](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/planning-how-to-secure-the-mbam-websites)

Nachdem Sie den SPN konfiguriert haben, sollten Sie eine begrenzte Delegierung für den SPN einrichten. Gehen Sie hierzu folgendermaßen vor:

1. Wechseln Sie zu Active Directory, und suchen Sie die APP-Pool-Anmeldeinformationen, die Sie für MBAM-Websites in den vorherigen Schritten konfiguriert haben.

2. Klicken Sie mit der rechten Maustaste auf die Anmeldeinformationen, und wählen Sie dann **Eigenschaften**aus.

3. Wählen Sie die Registerkarte **Delegierung** aus.

4. Wählen Sie die Option für die Kerberos-Authentifizierung aus.

5. Wählen Sie **Durchsuchen**aus, und suchen Sie erneut nach den Anmeldeinformationen Ihres App-Pools. Sie sollten dann die alle SPNs sehen, die im App-Pool creds-Konto eingerichtet sind. (Der SPN sollte "http/BitLocker. FQDN. com" ähneln). Markieren Sie den SPN, der mit dem Hostnamen identisch ist, den Sie während der MBAM-Installation angegeben haben.

6. Wählen Sie **OK** aus.

Jetzt sind Sie mit den Voraussetzungen gut. In den nächsten Schritten installieren Sie die MBAM-Software auf den Servern und konfigurieren Sie.

## Installieren und Konfigurieren der MBAM 2,5-Server Software

### Schritt 6: Installieren der MBAM 2,5-Server Software 

Führen Sie die folgenden Schritte aus, um die MBAM-Server Software mithilfe des Setup-Assistenten für die Microsoft BitLocker-Verwaltung und-Überwachung sowohl auf dem Datenbankserver als auch auf dem Verwaltungs-und Überwachungs Server zu installieren.

1. Führen Sie auf dem Server, auf dem Sie MBAM installieren möchten, MBAMserversetup.exe aus, um den Setup-Assistenten für Microsoft BitLocker-Verwaltung und-Überwachung zu starten.

2. Wählen Sie auf der Seite Willkommen die Option **weiter**aus.

3. Lesen und akzeptieren Sie den Microsoft-Software-Lizenzvertrag, und wählen Sie dann **weiter** aus, um die Installation fortzusetzen.

4. Entscheiden Sie, ob Sie Microsoft Update verwenden möchten, wenn Sie nach Updates suchen, und wählen Sie dann **weiter**aus.

5. Entscheiden Sie, ob Sie am Programm zur Verbesserung der Benutzerfreundlichkeit teilnehmen möchten, und wählen Sie dann **weiter**aus.

6. Um die Installation zu starten, wählen Sie **Installieren**aus.

7. Wenn Sie die Server Features nach Abschluss der Installation der MBAM-Server Software konfigurieren möchten, aktivieren Sie das Kontrollkästchen **MBAM-Serverkonfiguration ausführen, nachdem der Assistent geschlossen** wurde. Oder Sie können MBAM später mithilfe der **MBAM-Server Konfigurations** Verknüpfung konfigurieren, die von der Server Installation im **Startmenü** erstellt wird.

8. Wählen Sie **Fertig stellen**aus.

Weitere Informationen finden Sie unter [Installieren der MBAM 2,5-Server Software](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/installing-the-mbam-25-server-software).

### Schritt 7: Konfigurieren der MBAM 2,5-Datenbank-und-Berichtsrolle

In diesem Schritt konfigurieren wir die MBAM 2,5-Datenbanken und die Berichtskomponente mithilfe des MBAM-Assistenten:

1. Konfigurieren Sie die Kompatibilitäts-und Überwachungsdatenbank und die Wiederherstellungsdatenbank mithilfe des Assistenten:
   
   1. Starten Sie auf dem Server, auf dem Sie die Datenbanken konfigurieren möchten, den **MBAM-Serverkonfigurations-Assistenten**. Sie können **MBAM Server Configuration** im **Startmenü** auswählen, um den Assistenten zu öffnen.

   2. Wählen Sie **neue Features hinzufügen**aus, wählen Sie **Compliance und Überwachungsdatenbank**, **Wiederherstellungsdatenbank und Berichte**aus, und wählen Sie dann **weiter**aus. Der Assistent überprüft, ob alle Voraussetzungen für die Datenbanken erfüllt sind.

   3. Wenn die Voraussetzungsprüfung erfolgreich ist, wählen Sie **weiter** aus, um fortzufahren. Beheben Sie andernfalls alle fehlenden Voraussetzungen, und wählen Sie dann die Option **Voraussetzungen erneut überprüfen**aus.
   
   4. Geben Sie anhand der folgenden Beschreibungen die Feldwerte im Assistenten ein:

2. Konformitäts-und Überwachungsdatenbank

   |Feld   |Beschreibung|
   |-------|-------|
   |SQL Server-Name |Der Name des Servers, auf dem Sie die Kompatibilitäts-und Überwachungsdatenbank konfigurieren. <br /> Sie müssen auf dem Computer Compliance und Audit Database eine Ausnahme hinzufügen, um eingehenden eingehenden Datenverkehr am SQL Server-Port zu aktivieren. Die Standardportnummer ist 1433.|
   |SQL Server-Datenbankinstanz    |Der Name der Datenbankinstanz, in der die Konformitäts-und Überwachungsdaten gespeichert werden. Wenn Sie die Standardinstanz verwenden, müssen Sie dieses Feld leer lassen. Sie müssen außerdem angeben, wo sich die Datenbankinformationen befinden sollen.|
   |Datenbankname   |Der Name der Datenbank, in der die Kompatibilitätsdaten gespeichert werden. Sie müssen den Namen der Datenbank notieren, die Sie hier angeben, da diese Informationen in späteren Schritten bereitgestellt werden müssen.|
   |Berechtigung zum Lesen/Schreiben von Domänenbenutzern oder-Gruppen  |Geben Sie den Namen des MBAMAppPool-Benutzers an, wie in Schritt 2 konfiguriert.|
   |Schreibgeschützter Zugriffsdomänen Benutzer oder-Gruppe   |Geben Sie den Namen des MBAMROUser-Benutzers an, wie in Schritt 2 konfiguriert.|

3. Wiederherstellungsdatenbank.

   |Feld   |Beschreibung|
   |-----|-----|
   |SQL Server-Name |Der Name des Servers, auf dem Sie die Wiederherstellungsdatenbank konfigurieren. Sie müssen auf dem Wiederherstellungsdaten Bank Computer eine Ausnahme hinzufügen, um eingehenden eingehenden Datenverkehr am SQL Server-Port zu aktivieren. Die Standardportnummer ist 1433.|
   |SQL Server-Datenbankinstanz    |Der Name der Datenbankinstanz, in der die Wiederherstellungsdaten gespeichert werden. Wenn Sie die Standardinstanz verwenden, müssen Sie dieses Feld leer lassen. Sie müssen außerdem angeben, wo sich die Datenbankinformationen befinden sollen.|
   |Datenbankname   |Der Name der Datenbank, in der die Wiederherstellungsdaten gespeichert werden.|
   |Berechtigung zum Lesen/Schreiben von Domänenbenutzern oder-Gruppen  |Domänenbenutzer oder-Gruppe, die über die Berechtigung "Lesen/Schreiben" für diese Datenbank verfügt, damit die Webanwendungen auf die Daten und Berichte in dieser Datenbank zugreifen können. <br />Wenn Sie einen Benutzer in dieses Feld eingeben, muss er mit dem Wert im Feld **Domänenkonto des Webdienst-Anwendungspools** auf der Seite **Webanwendungen konfigurieren** identisch sein. <br />Wenn Sie eine Gruppe in dieses Feld eingeben, muss der Wert im Feld " **Webdienst-Anwendungspool Domäne** " auf der Seite " **Webanwendungen konfigurieren** " ein Mitglied der Gruppe sein, die Sie in dieses Feld eingeben.|
   
   Wenn Sie Ihre Eingaben abgeschlossen haben, wählen Sie **weiter**aus. Der Assistent überprüft, ob alle Voraussetzungen für die Datenbanken erfüllt sind.
   
   Wenn die Voraussetzungsprüfung erfolgreich ist, wählen Sie **weiter** aus, um fortzufahren. Beheben Sie andernfalls alle fehlenden Voraussetzungen, und wählen Sie dann erneut **weiter** aus.

4. Berichte.

   |Feld   |Beschreibung|
   |----|----|
   |SQL Server Reporting Services-Instanz  |Instanz von SQL Server Reporting Services, in der die Berichte konfiguriert werden. Wenn Sie die Standardinstanz verwenden, müssen Sie dieses Feld leer lassen.|
   |Gruppe "Berichtsrolle-Domäne" |Geben Sie den Namen des MBAMRUGrp an, wie in Schritt 2 erwähnt.|
   |SQL Server-Name |Der Name des Servers, auf dem die Konformitäts-und Überwachungsdatenbank konfiguriert ist.|
   |SQL Server-Datenbankinstanz    |Der Name der Datenbankinstanz, in der die Konformitäts-und Überwachungsdaten konfiguriert sind. Wenn Sie die Standardinstanz verwenden, müssen Sie dieses Feld leer lassen. <br />Sie müssen auf dem Computer "Berichte" eine Ausnahme hinzufügen, um eingehenden Datenverkehr über den Port des Berichtsservers zu ermöglichen. (Der Standardport ist 80.)|
   |Datenbankname|  Der Name der Konformitäts-und Überwachungsdatenbank. Standardmäßig ist der Datenbankname MBAM-Konformitäts Status.|
   |Compliance-und Audit-Daten Bank Domänenkonto    |Geben Sie den Namen des MBAMROUser-Benutzers an, wie in Schritt 2 konfiguriert.|
   
   Wenn Sie Ihre Eingaben abgeschlossen haben, wählen Sie **weiter**aus. Der Assistent überprüft, ob alle Voraussetzungen für das Berichtsfeature erfüllt sind. Wählen Sie Weiter, um fortzufahren. Überprüfen Sie auf der Seite **Zusammenfassung** die Features, die hinzugefügt werden sollen.
   
   Weitere Informationen finden Sie im folgenden Artikel: [Konfigurieren der MBAM 2,5-Datenbanken](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/how-to-configure-the-mbam-25-databases).

### Schritt 8: Konfigurieren der MBAM 2,5 Web Applications-Rolle

1. Starten Sie auf dem Server, auf dem Sie die Webanwendungen konfigurieren möchten, den MBAM-Serverkonfigurations-Assistenten. Sie können **MBAM Server Configuration** im **Startmenü** auswählen, um den Assistenten zu öffnen.

2. Wählen Sie **neue Funktionen hinzufügen**aus, wählen Sie Website und **Self-Service-Portal** **Verwalten und überwachen** aus, und wählen Sie dann **weiter**aus. Der Assistent überprüft, ob alle Voraussetzungen für die Datenbanken erfüllt sind.

3. Wenn die Voraussetzungsprüfung erfolgreich ist, wählen Sie **weiter** aus, um fortzufahren. Beheben Sie andernfalls alle fehlenden Voraussetzungen, und wählen Sie dann die Option **Voraussetzungen erneut überprüfen**aus.

4. Verwenden Sie die folgenden Beschreibungen, um die Feldwerte im Assistenten einzugeben.

   |Feld   |Beschreibung|
   |-----|-----|
   |Sicherheitszertifikat    |Wählen Sie in Schritt 3 ein zuvor erstelltes Zertifikat aus, um die Kommunikation zwischen den Webdiensten und dem Server, auf dem Sie die Verwaltungs-und Überwachungs Website konfigurieren, optional zu verschlüsseln. Wenn Sie ein Zertifikat nicht verwenden auswählen, ist Ihre Internetkommunikation möglicherweise nicht sicher.|
   |Hostname   |Name des Hostcomputers, auf dem Sie die Website "Verwaltung und Überwachung" konfigurieren. <br />Es muss sich nicht um den Hostnamen des Computers handeln. Wenn sich der Hostname aber vom NetBIOS-Namen des Computers unterscheidet, müssen Sie einen A-Eintrag erstellen und sicherstellen, dass der SPN den benutzerdefinierten Hostnamen und nicht den NetBIOS-Namen verwendet. Dies ist bei Lastenausgleichsszenarien üblich.|
   |Installationspfad   |Der Pfad, auf dem Sie die Website "Verwaltung und Überwachung" installieren.|
   |Port    |Die für die Website Kommunikation zu verwendende Port Nummer. <br /> Sie müssen eine Firewall-Ausnahme festlegen, um die Kommunikation über den angegebenen Port zu ermöglichen.|
   |Domänenkonto und Kennwort des Webdienst-Anwendungspools    |Geben Sie das Benutzerkonto und das Kennwort des MBAMAppPool-Benutzers an, wie in Schritt 2 konfiguriert. <br /> Um die Sicherheit zu verbessern, legen Sie das in den Anmeldeinformationen angegebene Konto auf begrenzte Benutzerrechte fest. Legen Sie außerdem das Kennwort des Kontos so ein, dass es nie abläuft.|

5. Überprüfen Sie, ob das integrierte IIS_IUSRS Konto oder das Anwendungspoolkonto dem **Identitätswechsel zu einem Client nach der Authentifizierung** und den lokalen Sicherheitseinstellungen des **stapelverarbeitungsauftrags** hinzugefügt wurde.

   Wenn Sie überprüfen möchten, ob das Konto zu den lokalen Sicherheitseinstellungen hinzugefügt wurde, öffnen Sie den **lokalen Sicherheitsrichtlinien-Editor**, erweitern Sie den Knoten **lokale Richtlinien** , wählen Sie den Knoten **Benutzerrechtezuweisung** aus, und doppelklicken Sie auf **Identitätswechsel für einen Client nach Authentifizierung** , und **melden Sie sich als batchauftrags** Richtlinien im rechten Bereich an.

6. Verwenden Sie die folgenden Feldbeschreibungen, um die Verbindungsinformationen im Assistenten für die Konformitäts-und Überwachungsdatenbank zu konfigurieren.
   |Feld   |Beschreibung|
   |------|------|
   |SQL Server-Name |Der Name des Servers, auf dem die Konformitäts-und Überwachungsdatenbank konfiguriert ist.|
   |SQL Server-Datenbankinstanz    |Name der Instanz von SQL Server (beispielsweise \<Server Name\> ) und für die die Compliance-und Überwachungsdatenbank konfiguriert ist. Lassen Sie dieses Feld leer, wenn Sie die Standardinstanz verwenden.|
   |Datenbankname   |Der Name der Konformitäts-und Überwachungsdatenbank. Standardmäßig lautet der Wert "MBAM-Konformitäts Status".|

7. Verwenden Sie die folgenden Feldbeschreibungen, um die Verbindungsinformationen im Assistenten für die Wiederherstellungsdatenbank zu konfigurieren.
   |Feld   |Beschreibung|
   |----|----|
   |SQL Server-Name |Der Name des Servers, auf dem die Wiederherstellungsdatenbank konfiguriert ist.|
   |SQL Server-Datenbankinstanz    |Der Name der Instanz von SQL Server (beispielsweise \<Server Name\> ), auf der die Wiederherstellungsdatenbank konfiguriert ist. Lassen Sie dieses Feld leer, wenn Sie die Standardinstanz verwenden.|
   |Datenbankname   |Der Name der Wiederherstellungsdatenbank. Standardmäßig handelt es sich um "MBAM-Wiederherstellung und-Hardware".|

8. Verwenden Sie die folgenden Beschreibungen, um die Feldwerte im Assistenten einzugeben, um die Website "Verwaltung und Überwachung" zu konfigurieren.
   |Feld   |Beschreibung|
   |----|----|
   |Erweiterte Helpdesk-Rollen Domänengruppe |Geben Sie den Namen der MBAMAdvHelpDsk-Gruppe an, wie in Schritt 2 konfiguriert.|
   |Gruppe "Helpdesk Role Domain"  |Geben Sie den Namen der MBAMHelpDsk-Gruppe an, wie in Schritt 2 konfiguriert.|
   |Verwenden der System Center Configuration Manager-Integration |Aktivieren Sie dieses Kontrollkästchen, um das Kontrollkästchen zu deaktivieren.     |
   |Gruppe "Berichtsrolle-Domäne" |Geben Sie den Namen der MBAMRUGrp-Gruppe an, wie in Schritt 2 konfiguriert.    |
   |SQL Server Reporting Services-URL   |Geben Sie die URL des Webdiensts für den SSRS-Server an, auf dem die MBAM-Berichte konfiguriert sind. Sie können diese Informationen finden, indem Sie sich beim Reporting Services-Konfigurations-Manager auf dem Daten Bank Server anmelden. <br /> Beispiel für einen vollqualifizierten Domänennamen:https://MyReportServer.Contoso.com/ReportServer <br />Beispiel für einen benutzerdefinierten Hostnamen:https://MyReportServer/ReportServer|
   |Virtuelles Verzeichnis   |Virtuelles Verzeichnis der Verwaltungs-und Überwachungs Website. Dieser Name entspricht dem physikalischen Verzeichnis der Website auf dem Server und wird dem Hostnamen der Website angefügt. Beispiel: <br />http (s):// *\<host name\>* : *\<port\>* /Helpdesk/ <br />Wenn Sie kein virtuelles Verzeichnis angeben, wird der Wert Helpdesk verwendet.     |

9. Verwenden Sie die folgende Beschreibung, um die Feldwerte im Assistenten einzugeben, um das Self-Service-Portal zu konfigurieren.

   |Feld   |Beschreibung|
   |----|----|
   |Virtuelles Verzeichnis   |Virtuelles Verzeichnis der Web-Anwendung. Dieser Name entspricht dem physikalischen Verzeichnis der Website auf dem Server und wird dem Hostnamen der Website angefügt. Beispiel:<br />http (s):// *\<host name\>* : *\<port\>* /Selfservice/<br /> Wenn Sie kein virtuelles Verzeichnis angeben, wird der Wert "Selfservice" verwendet.|

10. Wenn Sie Ihre Eingaben abgeschlossen haben, wählen Sie **weiter**aus. Der Assistent überprüft, ob alle Voraussetzungen für die Webanwendungen erfüllt sind.

11. Wählen Sie **weiter** aus, um fortzufahren.

12. Überprüfen Sie auf der Seite **Zusammenfassung** die Features, die hinzugefügt werden sollen.

13. Wählen Sie **Hinzufügen** aus, um die Webanwendungen zum Server hinzuzufügen, und wählen Sie dann **Schließen**aus.

## Anpassen und Validieren von Schritten nach der Installation der MBAM 2,5-Server Software

### Schritt 9: Anpassen des Self-Server-Portals für Ihre Organisation

Informationen zum Anpassen des Self-Service-Portals durch Hinzufügen von benutzerdefiniertem Benachrichtigungstext, dem Namen Ihres Unternehmens, verweisen auf Weitere Informationen usw. finden Sie unter [Anpassen des Self-Service-Portals für Ihre Organisation](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/customizing-the-self-service-portal-for-your-organization).
 
### Schritt 10: Konfigurieren des Self-Server-Portals, wenn Clientcomputer nicht auf das CDN zugreifen können 

Ermitteln Sie, ob Ihre Clientcomputer Zugriff auf das Microsoft AJAX Content Delivery Network (CDN) haben. Das CDN gewährt dem Self-Service-Portal den erforderlichen Zugriff auf bestimmte JavaScript-Dateien. Wenn Sie das Self-Service-Portal nicht konfigurieren, wenn Clientcomputer nicht auf das CDN zugreifen können, werden nur der Firmenname und das Konto angezeigt, unter dem der Benutzer angemeldet ist. Es wird keine Fehlermeldung angezeigt.

Führen Sie eine der folgenden Aktionen aus:

* Wenn Ihre Clientcomputer Zugriff auf das CDN haben, tun Sie nichts. Ihre Self-Service-Portal-Konfiguration ist abgeschlossen.

* Wenn Ihre Clientcomputer keinen Zugriff auf das CDN haben, führen Sie die Schritte unter [Konfigurieren des Self-Service-Portals aus, wenn Clientcomputer nicht auf das Microsoft Content Delivery Network zugreifen können](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/how-to-configure-the-self-service-portal-when-client-computers-cannot-access-the-microsoft-content-delivery-network).

### Schritt 11: Überprüfen der MBAM 2,5 Server-Feature-Konfiguration 

Führen Sie die folgenden Schritte aus, um Ihre MBAM-Server Bereitstellung zur Verwendung der eigenständigen Topologie zu überprüfen.

1. Wählen Sie auf jedem Server, auf dem ein MBAM-Feature **Control Panel**bereitgestellt wird, die Option  >  **Programme**  >  **und Funktionen**der Systemsteuerung aus. Überprüfen Sie, ob die **Microsoft BitLocker-Verwaltung und-Überwachung** in der Liste " **Programme und Features** " angezeigt wird.
   > [!Note]
   > Zum Durchführen der Überprüfung müssen Sie ein Domänenkonto verwenden, das auf jedem Server über Administratoranmeldeinformationen des lokalen Computers verfügt.

2. Öffnen Sie auf dem Server, auf dem die Wiederherstellungsdatenbank konfiguriert ist, SQL Server Management Studio, und überprüfen Sie, ob die **MBAM-Wiederherstellungs-und-Hardware** Datenbank konfiguriert ist.

3. Öffnen Sie auf dem Server, auf dem die Konformitäts-und Überwachungsdatenbank konfiguriert ist, SQL Server Management Studio, und überprüfen Sie, ob die MBAM-Konformitäts Status Datenbank konfiguriert ist.

4. Öffnen Sie auf dem Server Onm, auf dem das Feature Berichte konfiguriert ist, einen Webbrowser mithilfe administrativer Anmeldeinformationen, und navigieren Sie zur Homepage der SQL Server Reporting Services-Website.
   
   Der Standardspeicherort für die Homepage einer SQL Server Reporting Services-Websiteinstanz lautet wie folgt: http (s):// *\<MBAM Reports Server Name\>* : *\<port\>* /Reports.aspx
   
   Um die tatsächliche URL zu finden, verwenden Sie das Reporting Services-Konfigurations-Manager-Tool, und wählen Sie die Instanzen aus, die Sie während der Installation angegeben haben.
   
5. Überprüfen Sie, ob ein Berichtsordner mit dem Namen Microsoft BitLocker-Verwaltung und-Überwachung eine Datenquelle mit dem Namen MaltaDataSource enthält. Diese Datenquelle enthält Ordner mit Namen, die Sprachgebietsschemas darstellen (beispielsweise en-US). Die Berichte befinden sich in den Sprachordnern.

   > [!Note]
   > Wenn SQL Server Reporting Services (SSRS) als benannte Instanz konfiguriert wurde, sollte die URL wie folgt aussehen: http (s):// \<MBAM Reports Server Name\> : \<port\> /Reports_\<SSRS Instance Name\>
   >
   > Wenn SSRS nicht für die Verwendung von Secure Socket Layer (SSL) konfiguriert wurde, wird bei der Installation des MBAM-Servers die URL für die Berichte auf "http" anstelle von "https" festgelegt. Wenn Sie dann zur Website Verwaltung und Überwachung (auch als Helpdesk bezeichnet) wechseln und einen Bericht auswählen, wird die folgende Meldung angezeigt: "nur sichere Inhalte werden angezeigt." Wenn Sie den Bericht anzeigen möchten, wählen Sie **alle Inhalte anzeigen**aus.

6. Führen Sie auf dem Server, auf dem das Feature Verwaltungs-und Überwachungs Website konfiguriert ist, den Server-Manager aus, navigieren Sie zu **Rollen**, und wählen Sie dann **Web Server (** IIS)  >  **Internetinformationsdienste (IIS)** -Manager aus.

7. Navigieren Sie in **Verbindungen**zu, \<computer name\> und wählen Sie dann **Websites**  >  **Microsoft BitLocker-Verwaltung und-Überwachung**aus. Überprüfen Sie, ob die folgenden Angaben aufgeführt sind:

   * MBAMAdministrationService
   * MBAMComplianceStatusService
   * MBAMRecoveryAndHardwareService

8. Öffnen Sie auf dem Server, auf dem die Verwaltungs-und Überwachungs Website und das Self-Service-Portal konfiguriert sind, mithilfe administrativer Anmeldeinformationen einen Webbrowser.

9. Navigieren Sie zu den folgenden Websites, um sicherzustellen, dass Sie erfolgreich geladen werden:
   * HTTPS (s):// \<MBAM Administration Server Name\> : \<port\> /Helpdesk/(bestätigen Sie die einzelnen Links für Navigation und Berichte)
   * http (s):// \<MBAM Administration Server Name\> : \<port\> /Selfservice/

   > [!Note]
   > Es wird davon ausgegangen, dass Sie die Server Features auf dem Standardport ohne Netzwerk Verschlüsselung konfiguriert haben. Wenn Sie die Server Features in einem anderen Port oder virtuellen Verzeichnis konfiguriert haben, ändern Sie die URLs so, dass Sie den entsprechenden Port umfassen. Beispiel: http (s):// \<host name\> : \<port\> /Helpdesk/http (s):// \<host name\> : \<port\> / \<virtualdirectory\> /Wenn die Server Features für die Verwendung der Netzwerk Verschlüsselung konfiguriert wurden, ändern Sie http://in https://.
   
10. Navigieren Sie zu den folgenden Webdiensten, um sicherzustellen, dass Sie erfolgreich geladen werden. Eine Seite wird geöffnet, um anzugeben, dass der Dienst ausgeführt wird. Auf der Seite werden jedoch keine Metadaten angezeigt.

    * http (s):// \<MBAM Administration Server Name> : \<port> /MBAMAdministrationService/AdministrationService.svc
    * http (s):// \<MBAM Administration Server Name> : \<port> /MBAMUserSupportService/UserSupportService.svc
    * http (s):// \<MBAM Administration Server Name> : \<port> /MBAMComplianceStatusService/StatusReportingService.svc
    * http (s):// \<MBAM Administration Server Name> : \<port> /MBAMRecoveryAndHardwareService/CoreService.svc

### Schritt 12: Konfigurieren der MBAM-Gruppenrichtlinienvorlagen

Zum Bereitstellen von MBAM müssen Sie Gruppenrichtlinieneinstellungen festlegen, die MBAM-Implementierungs Einstellungen für die BitLocker-Laufwerkverschlüsselung definieren. Zum Ausführen dieser Aufgabe müssen Sie die MBAM-Gruppenrichtlinienvorlagen auf einen Server oder eine Workstation kopieren, auf dem die Gruppenrichtlinien-Verwaltungskonsole (Group Policy Management Console, GPMC) oder erweiterte Gruppenrichtlinienverwaltung (Group Policy Management, AGPM) ausgeführt werden kann, und dann die Einstellungen bearbeiten.

> [!Important]
> Ändern Sie die Gruppenrichtlinieneinstellungen im **BitLocker Drive Encryption** -Knoten nicht, oder MBAM wird nicht ordnungsgemäß funktionieren. Wenn Sie die Gruppenrichtlinieneinstellungen im MDOP- **MBAM (BitLocker-Verwaltungsknoten)** konfigurieren, konfiguriert MBAM automatisch die **BitLocker-Laufwerk Verschlüsselungs** Einstellungen für Sie.
 
#### Kopieren der MBAM 2,5-Gruppenrichtlinienvorlagen

Bevor Sie den MBAM-Client installieren, müssen Sie MBAM-spezifische Gruppenrichtlinienobjekte (Group Policy Objects, GPOs) auf die Verwaltungsarbeitsstation kopieren. Diese GPOs definieren MBAM-Implementierungs Einstellungen für BitLocker. Sie können die Gruppenrichtlinienvorlagen auf alle Server oder Workstations kopieren, die ein unterstützter Windows-basierter Server oder Clientcomputer sind und die Gruppenrichtlinien-Verwaltungskonsole (Group Policy Management Console, GPMC) oder erweiterte Gruppenrichtlinienverwaltung (Group Policy Management, AGPM) ausführen können.

Weitere Informationen finden Sie unter [Kopieren der MBAM 2,5-Gruppenrichtlinienvorlagen](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/copying-the-mbam-25-group-policy-templates).
 
#### Bearbeiten von MBAM 2,5-GPO-Einstellungen

Nachdem Sie die erforderlichen GPOs erstellt haben, müssen Sie die MBAM-Gruppenrichtlinieneinstellungen auf den Clientcomputern Ihrer Organisation bereitstellen. Um GPOs anzuzeigen und zu erstellen, müssen Sie die Gruppenrichtlinien-Verwaltungskonsole (Group Policy Management Console, GPMC) oder eine erweiterte Gruppenrichtlinienverwaltung (Group Policy Management, AGPM) installiert haben.

Weitere Informationen finden Sie unter [Bearbeiten der MBAM 2,5-Gruppenrichtlinieneinstellungen](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/editing-the-mbam-25-group-policy-settings) und [Planen der MBAM 2,5-Gruppenrichtlinienanforderungen](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/planning-for-mbam-25-group-policy-requirements).
 
### Schritt 13: Bereitstellen des MBAM 2,5-Clients

Je nachdem, ob Sie die Microsoft BitLocker-Verwaltungs-und-Überwachungs Client Software bereitstellen, können Sie BitLocker auf einem Computer in Ihrer Organisation aktivieren, bevor der Benutzer den Computer empfängt, oder anschließend, indem Sie die Gruppenrichtlinie konfigurieren und die MBAM-Client Software mithilfe eines Enterprise-Software Bereitstellungssystems bereitstellen.
 
#### Bereitstellen des MBAM-Clients auf Desktop-oder tragbaren Computern

Nachdem Sie die Gruppenrichtlinieneinstellungen konfiguriert haben, können Sie ein Produkt für die Bereitstellung von Unternehmenssoftware wie Microsoft System Center 2012 Configuration Manager oder Active Directory-Domänendienste (AD DS) verwenden, um die Windows Installer-Dateien für die MBAM-Clientinstallation auf Zielcomputern bereitzustellen. Sie können entweder die 32-Bit-oder 64-Bit-MbamClientSetup.exe-Dateien oder die 32-Bit-oder 64-Bit-MBAMClient.msi Dateien verwenden. Diese werden zusammen mit der MBAM-Client Software bereitgestellt.

Weitere Informationen finden Sie unter [Bereitstellen des MBAM-Clients auf Desktop-oder Laptop Computern](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/how-to-deploy-the-mbam-client-to-desktop-or-laptop-computers-mbam-25).
 
#### Bereitstellen des MBAM-Clients als Teil einer Windows-Bereitstellung

In Organisationen, in denen Computer zentral empfangen und konfiguriert werden, können Sie den MBAM-Client installieren, um die BitLocker-Laufwerkverschlüsselung auf jedem Computer zu verwalten, bevor Benutzerdaten darin geschrieben werden. Der Vorteil dieses Prozesses liegt darin, dass jeder Computer dann BitLocker-kompatibel ist. Diese Methode ist nicht auf Benutzeraktionen angewiesen, da der Administrator den Computer bereits verschlüsselt hat. Eine wichtige Annahme für dieses Szenario besteht darin, dass die Richtlinie der Organisation darin besteht, ein Windows-Abbild des Unternehmens zu installieren, bevor der Computer an den Benutzer übermittelt wird. Wenn die Gruppenrichtlinieneinstellungen so konfiguriert sind, dass eine PIN erforderlich ist, werden die Benutzer aufgefordert, eine PIN festzulegen, nachdem Sie die Richtlinie erhalten haben.

Weitere Informationen finden Sie unter [Bereitstellen des MBAM-Clients als Teil einer Windows-Bereitstellung](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/how-to-enable-bitlocker-by-using-mbam-as-part-of-a-windows-deploymentmbam-25).
 
#### Bereitstellen des MBAM-Clients mithilfe einer Befehlszeile

Weitere Informationen finden Sie unter [Bereitstellen des MBAM-Clients mithilfe einer Befehlszeile](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/how-to-deploy-the-mbam-client-by-using-a-command-line).

#### Nach der Bereitstellung von Clients

Nachdem Sie die Bereitstellungs Aktivität abgeschlossen haben, sollten Sie die folgenden Protokolle überprüfen und ermitteln, ob die Clients erfolgreich an die MBAM-Datenbank gemeldet werden.

## Häufig gestellte Fragen

### Erstellen von IIS-Servern mit Lastenausgleich

* SPN muss nur für den Anzeigenamen registriert werden (Beispiel: BitLocker.Corp.net) und darf nicht auf einzelnen IIS-Servern registriert sein.

* Wenn ein Zertifikat verwendet wird, muss das Zertifikat sowohl FQDN-als auch NetBIOS-Namen enthalten, die in das Feld " **Subject Alternative Name** " für alle IIS-Server in der Gruppe "Lastenausgleich" eingegeben werden, sowie den Anzeige Namen (beispielsweise: BitLocker.Corp.net). Andernfalls wird das Zertifikat vom Browser beim Durchsuchen von Adressen mit Lastenausgleich als nicht vertrauenswürdig gemeldet.

Weitere Informationen finden Sie unter [IIS-Netzwerklastenausgleich](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/planning-for-mbam-25-high-availability#a-href-idbkmk-load-balanceaiis-network-load-balancing) und [Registrieren von SPNs für das Anwendungspoolkonto](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/planning-how-to-secure-the-mbam-websites#registering-spns-for-the-application-pool-account).

### So konfigurieren Sie ein Zertifikat

* Sie benötigen zwei Zertifikate. Für SQL Server wird ein Zertifikat verwendet, und das andere wird für IIS verwendet. Sie müssen vor dem Starten der MBAM-Installation installiert werden.

* Wir empfehlen, dass Sie das Installationsprogramm verwenden, um das Zertifikat zur IIS-Konfiguration hinzuzufügen, anstatt die web.config-Datei manuell zu bearbeiten.

* Das Zertifikat wird vom MBAM-Konfigurator nicht akzeptiert, wenn das Feld "ausgestellt an" des Zertifikats nicht mit dem Namen des Servers übereinstimmt. Erstellen Sie in diesem Fall vorübergehend ein selbstsigniertes Zertifikat über die IIS-Konsole, und verwenden Sie es im Konfigurator. Dadurch wird nsure, dass die Web-Apps für SSL und HTTPS installiert sind. Anschließend können Sie das Zertifikat aus IIS-Bindungen für die MBAM-Website in eins ändern.

### Die SQL-Berechtigungsanforderung für die Installation

Erstellen Sie ein Konto für den MBAM-App-Pool, und geben Sie ihm nur SecurityAdmin-, Public-und dbcreator-Berechtigungen.

Weitere Informationen finden Sie unter [MBAM-Datenbankkonfiguration – minimale Berechtigungen](https://blogs.technet.microsoft.com/dubaisec/2016/02/02/mbam-database-configuration-minimum-permissions/) .

> [!Note]
> * In einigen Situationen sind für die anfänglichen Installations-und Aktualisierungsvorgänge weitere Berechtigungen erforderlich.
> * Verwenden Sie ein Konto mit temporärer SA für die Installation.
> * Starten Sie die Konfiguration nicht im Kontext eines Benutzerkontos (Ausführen als), das nicht über die erforderlichen Berechtigungen zum vornehmen von Änderungen an SQL Server verfügt, da dadurch Installationsfehler verursacht werden.
> * Sie müssen mit einem Konto angemeldet sein, das über Berechtigungen für SQL Server verfügt. Sie können nur SQL Server-Datenbankenerstellen oder aktualisieren, indem Sie den MBAM-Konfigurator Remote ausführen. Für SSRS-Server müssen Sie MBAM installieren und Configurator lokal ausführen, um die MBAM-SSRS-Berichte zu installieren oder zu aktualisieren.

### Die für die SPN-Registrierung erforderliche Berechtigung

Ein Konto, das für die IIS-Portal Installation verwendet wird, muss über Schreib-servicePrincipalName und überprüfte SPN-Berechtigungen verfügen. Ohne diese Berechtigungen gibt die Installation eine Warnmeldung zurück, die besagt, dass Sie den SPN nicht registrieren kann.

> [!Note]
> Diese Warnung wird Ihnen zwei Mal angezeigt. Dies bedeutet nicht, dass für den SPN zwei Objekte registriert sein müssen.

Weitere Informationen finden Sie unter [MBAM-Setup schlägt fehl, wenn die Fehlermeldung "SPN verzögert registrieren"](https://support.microsoft.com/help/2754138/)angezeigt wird.

### Musste ich die ADMX-Vorlagen auf die neueste Version aktualisieren?

Nachdem Sie die ADMX-Vorlagen auf die neuesten Versionen aktualisiert haben, werden im MBAM-Stammknoten für Gruppenrichtlinienobjekte mehrere Betriebssystemoptionen angezeigt. Beispiel: Windows 7, Windows 8,1 und Windows 10, Version 1511 und höhere Versionen.

Weitere Informationen zum Aktualisieren der ADMX-Vorlagen finden Sie in den folgenden Artikeln:
* [Herunterladen und Bereitstellen von MDOP-Gruppenrichtlinienvorlagen (ADMX-Dateien)](https://docs.microsoft.com/microsoft-desktop-optimization-pack/solutions/how-to-download-and-deploy-mdop-group-policy--admx--templates)
* [Planen der Gruppenrichtlinienanforderungen für MBAM 2.5](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/planning-for-mbam-25-group-policy-requirements)
* [Microsoft Desktop Optimization Pack-administrative Vorlagen für Gruppenrichtlinien](https://www.microsoft.com/en-us/download/details.aspx?id=55531)
