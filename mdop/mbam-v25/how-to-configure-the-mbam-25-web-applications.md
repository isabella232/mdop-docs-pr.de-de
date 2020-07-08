---
title: So konfigurieren Sie die MBAM 2.5-Webanwendungen
description: So konfigurieren Sie die MBAM 2.5-Webanwendungen
author: dansimp
ms.assetid: 909bf2d3-028c-4ac1-9247-171532a1eeae
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0336d24f51167a00c8565ccd081f4bc5dfb2c4cd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810591"
---
# So konfigurieren Sie die MBAM 2.5-Webanwendungen


In diesem Thema wird erläutert, wie Sie die 2,5-Webanwendungen für Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) für die empfohlene [allgemeine Architektur für MBAM 2,5](high-level-architecture-for-mbam-25.md) mithilfe einer der folgenden Methoden konfigurieren:

-   Ein Windows PowerShell-Cmdlet

-   Der Serverkonfigurations-Assistent von MBAM

Die Web-Anwendungen umfassen die folgenden Websites und die entsprechenden Webdienste:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Webseite</th>
<th align="left">Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Website "Verwaltung und Überwachung"</p></td>
<td align="left"><p>Website, auf der angegebene Benutzer Berichte anzeigen und Endbenutzern helfen können, ihre Computer wiederherzustellen, wenn Sie Ihre PIN oder Ihr Kennwort vergessen</p></td>
</tr>
<tr class="even">
<td align="left"><p>Self-Service-Portal</p></td>
<td align="left"><p>Website, auf die Endbenutzer zugreifen können, um den Zugriff auf Ihre Computer unabhängig voneinander wiederherzustellen, wenn Sie Ihre PIN oder Ihr Kennwort vergessen</p></td>
</tr>
</tbody>
</table>



**Bevor Sie die Konfiguration starten:**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Schritt</th>
<th align="left">Wo erhalte ich Anweisungen?</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Überprüfen Sie die empfohlene Architektur für MBAM.</p></td>
<td align="left"><p><a href="high-level-architecture-for-mbam-25.md" data-raw-source="[High-Level Architecture for MBAM 2.5](high-level-architecture-for-mbam-25.md)">High-Level-Architektur für MBAM2.5</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Überprüfen Sie die unterstützten Konfigurationen für MBAM.</p></td>
<td align="left"><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)">Von MBAM 2.5 unterstützte Konfigurationen</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Führen Sie die erforderlichen Voraussetzungen für jeden Server aus.</p>
<div class="alert">
<strong>Hinweis:</strong><br/><p>Stellen Sie sicher, dass Sie die SQL-ServerReporting-Dienste (SSRS) so konfigurieren, dass Sie die Secure Sockets Layer (SSL) verwenden, bevor Sie die Website Verwaltung und Überwachung konfigurieren. Andernfalls verwendet das Feature Berichte http statt HTTPS.</p>
</div>
<div>

</div></td>
<td align="left"><ul>
<li><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)">MBAM 2.5-Servervoraussetzungen für eigenständige und Configuration Manager-Integrationstopologien</a></p></li>
<li><p><a href="mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md" data-raw-source="[MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md)">MBAM 2,5-Server Voraussetzungen, die nur für die Configuration Manager-Integrations Topologie gelten </a> (falls zutreffend)</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Registrieren Sie Dienstprinzipalnamen (SPN) für das Anwendungspoolkonto für die Websites. Sie müssen diesen Schritt nur ausführen, wenn Sie in den Active Directory-Domänendiensten (AD DS) nicht über administrative Domänenrechte verfügen. Wenn Sie über diese Rechte in AD DS verfügen, erstellt MBAM die SPNs für Sie.</p></td>
<td align="left"><p><a href="planning-how-to-secure-the-mbam-websites.md#bkmk-regvirtualspn" data-raw-source="[Planning How to Secure the MBAM Websites](planning-how-to-secure-the-mbam-websites.md#bkmk-regvirtualspn)">Planen der Sicherung von MBAM-Websites</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Installieren Sie die MBAM-Server Software auf jedem Server, auf dem Sie ein MBAM-Server Feature konfigurieren.</p>
<div class="alert">
<strong>Hinweis:</strong><br/><p>Wenn Sie beabsichtigen, die Websites auf einem Server und die Webdienste auf einem anderen Server zu installieren, können Sie diese nur mithilfe des <strong> Windows PowerShell-Cmdlets Enable-MbamWebApplication konfigurieren </strong> . Der MBAM-Serverkonfigurations-Assistent unterstützt keine Konfiguration dieser Elemente auf separaten Servern.</p>
</div>
<div>

</div></td>
<td align="left"><p><a href="installing-the-mbam-25-server-software.md" data-raw-source="[Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md)">Installieren der MBAM 2.5-Serversoftware</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Überprüfen Sie die Voraussetzungen für die Verwendung von Windows PowerShell, wenn Sie beabsichtigen, Cmdlets zum Konfigurieren der MBAM-Server Features zu verwenden.</p></td>
<td align="left"><p><a href="configuring-mbam-25-server-features-by-using-windows-powershell.md" data-raw-source="[Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)">Konfigurieren von MBAM 2.5 Serverfunktionen mithilfe von Windows PowerShell</a></p></td>
</tr>
</tbody>
</table>



**So konfigurieren Sie die Webanwendungen mithilfe von Windows PowerShell**

1.  Bevor Sie die Konfiguration starten, lesen Sie [Konfigurieren von MBAM 2,5-Server Features mithilfe von Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md) zum Überprüfen der Voraussetzungen für die Verwendung von Windows PowerShell.

2.  Verwenden Sie das Cmdlet **enable-MbamWebApplication** , um die Webanwendungen mithilfe von Windows PowerShell zu konfigurieren. Um Informationen zu diesem Cmdlet abzurufen, geben **Sie Get-Help enable-MbamWebApplication**ein.

**So konfigurieren Sie die Einstellungen für alle Webanwendungen mithilfe des Assistenten**

1. Starten Sie auf dem Server, auf dem Sie die Webanwendungen konfigurieren möchten, den MBAM-Serverkonfigurations-Assistenten. Sie können **MBAM Server Configuration** im **Startmenü** auswählen, um den Assistenten zu öffnen.

2. Klicken Sie auf **neue Features hinzufügen**, wählen Sie Website und **Self-Service-Portal** **Verwalten und überwachen** aus, und klicken Sie dann auf **weiter**. Der Assistent überprüft, ob alle Voraussetzungen für die Webanwendungen erfüllt sind.

3. Wenn die Voraussetzungsprüfung erfolgreich ist, klicken Sie auf **weiter** , um fortzufahren. Beheben Sie andernfalls alle fehlenden Voraussetzungen, und klicken Sie dann **erneut auf Voraussetzungen prüfen**.

4. Verwenden Sie die folgenden Beschreibungen, um die Feldwerte im Assistenten einzugeben.

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><strong>Feld</strong></th>
   <th align="left">Beschreibung</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong>Sicherheitszertifikat</strong></p></td>
   <td align="left"><p>Wählen Sie ein zuvor erstelltes Zertifikat aus, um die Kommunikation zwischen den Webdiensten und dem Server, auf dem Sie die Websites konfigurieren, optional zu verschlüsseln. Wenn Sie <strong> ein Zertifikat nicht verwenden auswählen </strong> , ist die Webkommunikation möglicherweise nicht sicher.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong>Hostname</strong></p></td>
   <td align="left"><p>Name des Hostcomputers, auf dem Sie die Websites konfigurieren.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong>Installationspfad</strong></p></td>
   <td align="left"><p>Pfad, in dem Sie die Websites installieren.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong>Port</strong></p></td>
   <td align="left"><p>Port Nummer, die für die Website-und Dienst Kommunikation verwendet werden soll.</p>
   <div class="alert">
   <strong>Hinweis:</strong><br/><p>Sie müssen eine Firewall-Ausnahme festlegen, um die Kommunikation über den angegebenen Port zu ermöglichen.</p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong>Domänenkonto und Kennwort des Webdienst-Anwendungspools</strong></p></td>
   <td align="left"><p>Domänenbenutzerkonto und Kennwort für den Webdienst-Anwendungspool.</p>
   <p>Wenn Sie einen Benutzernamen in das <strong> Feld Lese/Schreibzugriff-Domänenbenutzer oder-Gruppe </strong> auf der <strong> Seite Datenbanken konfigurieren eingeben </strong> , müssen Sie diesen Wert in dieses Feld eingeben.</p>
   <p>Wenn Sie einen Gruppennamen in das <strong> Feld Lese-/Schreibzugriff-Domänenbenutzer oder-Gruppe </strong> auf der <strong> Seite Datenbanken konfigurieren eingeben </strong> , muss der in dieses Feld eingegebene Wert ein Mitglied dieser Gruppe sein.</p>
   <p>Wenn Sie keine Anmeldeinformationen angeben, werden die Anmeldeinformationen verwendet, die für eine zuvor aktivierte Webanwendung angegeben wurden. Alle Webanwendungen müssen die gleichen Anmeldeinformationen für den Anwendungspool verwenden. Wenn Sie für verschiedene Webanwendungen unterschiedliche Anmeldeinformationen angeben, wird der zuletzt angegebene Wert verwendet.</p>
   <div class="alert">
   <strong>Wichtig</strong><br/><p>Um die Sicherheit zu verbessern, legen Sie das in den Anmeldeinformationen angegebene Konto auf begrenzte Benutzerrechte fest. Legen Sie außerdem das Kennwort des Kontos so ein, dass es nie abläuft.</p>
   </div>
   <div>

   </div></td>
   </tr>
   </tbody>
   </table>



5. Überprüfen Sie, ob das integrierte IIS \ _IUSRS-Konto oder das Anwendungspoolkonto dem **Identitätswechsel zu einem Client nach der Authentifizierung** und den lokalen Sicherheitseinstellungen für das **Anmelden als Stapelverarbeitungsauftrag** hinzugefügt wurde.

   Wenn Sie überprüfen möchten, ob Sie den lokalen Sicherheitseinstellungen hinzugefügt wurde, öffnen Sie den **lokalen Sicherheitsrichtlinien-Editor**, erweitern Sie den Knoten **lokale Richtlinien** , klicken Sie auf den Knoten **Benutzerrechtezuweisung** , und doppelklicken Sie auf **Identitätswechsel für einen Client nach Authentifizierung** , und **melden Sie sich als batchauftrags** Richtlinien im rechten Bereich an.

**So konfigurieren Sie Verbindungsinformationen für die Datenbanken mithilfe des Assistenten**

1.  Verwenden Sie die folgenden Feldbeschreibungen, um die Verbindungsinformationen im Assistenten für die Konformitäts-und Überwachungsdatenbank zu konfigurieren.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Feld</th>
    <th align="left">Beschreibung</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><strong>SQL Server-Name</strong></p></td>
    <td align="left"><p>Der Name des Servers, auf dem die Konformitäts-und Überwachungsdatenbank konfiguriert ist.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong>SQL Server-Datenbankinstanz</strong></p></td>
    <td align="left"><p>SQL Server-Instanzname, in dem die Konformitäts-und Überwachungsdatenbank konfiguriert ist.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><strong>Datenbankname</strong></p></td>
    <td align="left"><p>Der Name der Konformitäts-und Überwachungsdatenbank.</p></td>
    </tr>
    </tbody>
    </table>



2.  Verwenden Sie die folgenden Feldbeschreibungen, um die Verbindungsinformationen im Assistenten für die Wiederherstellungsdatenbank zu konfigurieren.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Feld</th>
    <th align="left">Beschreibung</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><strong>SQL Server-Name</strong></p></td>
    <td align="left"><p>Der Name des Servers, auf dem die Wiederherstellungsdatenbank konfiguriert ist.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong>SQL Server-Datenbankinstanz</strong></p></td>
    <td align="left"><p>SQL Server-Instanzname, in dem die Wiederherstellungsdatenbank konfiguriert ist.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><strong>Datenbankname</strong></p></td>
    <td align="left"><p>Der Name der Wiederherstellungsdatenbank.</p></td>
    </tr>
    </tbody>
    </table>



**So konfigurieren Sie die Webanwendungen mithilfe des Assistenten**

1. Verwenden Sie die folgenden Beschreibungen, um die Feldwerte im Assistenten einzugeben, um die Website "Verwaltung und Überwachung" zu konfigurieren.

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left">Feld</th>
   <th align="left">Beschreibung</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong>Erweiterte Helpdesk-Rollen Domänengruppe</strong></p></td>
   <td align="left"><p>Domänenbenutzergruppe, deren Mitglieder Zugriff auf alle Bereiche der Verwaltungs-und Überwachungs Website haben, mit Ausnahme des Bereichs "Berichte".</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong>Gruppe "Helpdesk Role Domain"</strong></p></td>
   <td align="left"><p>Domänenbenutzergruppe, deren Mitglieder Zugriff auf die <strong> Bereiche "TPM verwalten" </strong> und " <strong> Laufwerk Wiederherstellung </strong> " der Website "Verwaltung und Überwachung" haben.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong>Verwenden der System Center Configuration Manager-Integration</strong></p></td>
   <td align="left"><p>Aktivieren Sie dieses Kontrollkästchen, wenn Sie MBAM mit der Configuration Manager-Integrations Topologie konfigurieren. Wenn Sie dieses Kontrollkästchen aktivieren, werden alle Berichte, mit Ausnahme des Wiederherstellungs Überwachungsberichts, in Configuration Manager anstatt auf der Website Verwaltung und Überwachung angezeigt.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong>Gruppe "Berichtsrolle-Domäne"</strong></p></td>
   <td align="left"><p>Domänenbenutzergruppe, deren Mitglieder schreibgeschützten Zugriff auf den Bereich "Berichte" der Website "Verwaltung und Überwachung" haben.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong>SQL Server Reporting Services-URL</strong></p></td>
   <td align="left"><p>Die URL für den SSRS-Server, auf dem die MBAM-Berichte konfiguriert sind.</p>
   <p>Beispiele für Berichts-URLs:</p>
   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left">Typ des Hostnamens</th>
   <th align="left">Beispiel</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p>Beispiel mit einem vollqualifizierten Domänennamen</p></td>
   <td align="left"><p><a href="https://MyReportServer.Contoso.com/ReportServer" data-raw-source="https://MyReportServer.Contoso.com/ReportServer">https://MyReportServer.Contoso.com/ReportServer</a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>Beispiel mit einem benutzerdefinierten Hostnamen</p></td>
   <td align="left"><p><a href="https://MyReportServer/ReportServer" data-raw-source="https://MyReportServer/ReportServer">https://MyReportServer/ReportServer</a></p></td>
   </tr>
   </tbody>
   </table>
   <p> </p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong>Virtuelles Verzeichnis</strong></p></td>
   <td align="left"><p>Virtuelles Verzeichnis der Verwaltungs-und Überwachungs Website. Dieser Name entspricht dem physikalischen Verzeichnis der Website auf dem Server und wird dem Hostnamen der Website angefügt, beispielsweise:</p>
   <p>http (s):// &lt; <em> Hostname </em> &gt; : &lt; <em> Port </em> &gt; /Helpdesk/</p>
   <p>Wenn Sie kein virtuelles Verzeichnis angeben, wird der Wert <strong> Helpdesk </strong> verwendet.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong>Domänengruppe "Daten Migrations Rolle" </strong> (optional)</p></td>
   <td align="left"><p>Die Domänenbenutzergruppe, deren Mitglieder Zugriff haben, um die mbam *-Informations-Cmdlets zu verwenden, um Wiederherstellungsinformationen über diesen Endpunkt zu schreiben.</p></td>
   </tr>
   </tbody>
   </table>



2. Verwenden Sie die folgende Beschreibung, um die Feldwerte im Assistenten einzugeben, um das Self-Service-Portal zu konfigurieren.

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left">Feld</th>
   <th align="left">Beschreibung</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong>Virtuelles Verzeichnis</strong></p></td>
   <td align="left"><p>Virtuelles Verzeichnis der Web-Anwendung. Dieser Name entspricht dem physikalischen Verzeichnis der Website auf dem Server und wird dem Hostnamen der Website angefügt, beispielsweise:</p>
   <p>http (s):// &lt; <em> Hostname </em> &gt; : &lt; <em> Port </em> &gt; /Selfservice/</p>
   <p>Wenn Sie kein virtuelles Verzeichnis angeben, wird der Wert <strong> Selfservice </strong> verwendet.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>Firmenname</p></td>
   <td align="left"><p>Geben Sie einen Firmennamen für das Self-Service-Portal an, beispielsweise:</p>
   <p>Contoso IT</p>
   <p>Dieser Firmenname wird von allen Self-Service-Portal Benutzern angezeigt.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>Helpdesk-URL-Text</p></td>
   <td align="left"><p>Geben Sie eine Text Anweisung an, die die Benutzer an die Helpdesk-Website Ihrer Organisation weiterleitet, beispielsweise:</p>
   <p>Helpdesk oder IT-Abteilung kontaktieren</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>Helpdesk-URL</p></td>
   <td align="left"><p>Geben Sie die URL für die Helpdesk-Website Ihrer Organisation an, beispielsweise:</p>
   <p>http (s):// &lt; <em> companyHelpdeskURL</em>&gt;/</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>Hinweistext Datei</p></td>
   <td align="left"><p>Wählen Sie eine Datei aus, die den Hinweis enthält, der Benutzern auf der Startseite des Self-Service-Portals angezeigt werden soll.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>Hinweistext für Benutzer nicht anzeigen</p></td>
   <td align="left"><p>Aktivieren Sie dieses Kontrollkästchen, um anzugeben, dass der Hinweistext für die Benutzer nicht angezeigt wird.</p></td>
   </tr>
   </tbody>
   </table>



3. Wenn Sie Ihre Eingaben abgeschlossen haben, klicken Sie auf **weiter**.

   Der Assistent überprüft, ob alle Voraussetzungen für die Webanwendungen erfüllt sind.

4. Klicken Sie auf **Weiter**, um den Vorgang fortzusetzen.

5. Überprüfen Sie auf der Seite **Zusammenfassung** die Features, die hinzugefügt werden sollen.

   **Hinweis:**  
   Wenn Sie ein Windows PowerShell-Skript für die von Ihnen erstellten Einträge erstellen möchten, klicken Sie auf **PowerShell-Skript exportieren** , und speichern Sie das Skript.



6. Klicken Sie auf **Hinzufügen** , um die Webanwendungen zum Server hinzuzufügen, und klicken Sie dann auf **Schließen**.

   Informationen zum Anpassen des Self-Service-Portals durch Hinzufügen von benutzerdefiniertem Benachrichtigungstext, dem Namen Ihres Unternehmens, verweisen auf Weitere Informationen usw. finden Sie unter [Anpassen des Self-Service-Portals für Ihre Organisation](customizing-the-self-service-portal-for-your-organization.md).

**So konfigurieren Sie das Self-Service-Portal, wenn Clientcomputer nicht auf das CDN zugreifen können**

1.  Ermitteln Sie, ob Sie Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) 2,5 SP1 ausführen. Wenn ja, tun Sie nichts. Ihre Self-Service-Portal-Konfiguration ist abgeschlossen.

    **Hinweis:**  
    Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) 2,5 SP1 installiert die JavaScript-Dateien in Setup und muss daher nicht mit dem Microsoft AJAX-Inhalts Zustellungs Netzwerk verbunden sein, um das Self-Service-Portal konfigurieren zu können. Die folgenden Schritte sind nur erforderlich, wenn Sie eine Version von Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) 2,5 zurück zu SP1 verwenden.



2.  Ermitteln Sie, ob Ihre Clientcomputer Zugriff auf das Microsoft AJAX Content Delivery Network (CDN) haben.

    Das CDN gewährt dem Self-Service-Portal den erforderlichen Zugriff auf bestimmte JavaScript-Dateien. Wenn Sie das Self-Service-Portal nicht konfigurieren, wenn Clientcomputer nicht auf das CDN zugreifen können, werden nur der Firmenname und das Konto angezeigt, unter dem der Benutzer angemeldet ist. Es wird keine Fehlermeldung angezeigt.

3.  Führen Sie eine der folgenden Aktionen aus:

    -   Wenn Ihre Clientcomputer Zugriff auf das CDN haben, tun Sie nichts. Ihre Self-Service-Portal-Konfiguration ist abgeschlossen.

    -   Wenn Ihre Clientcomputer keinen Zugriff auf das CDN haben, führen Sie die Schritte unter [Konfigurieren des Self-Service-Portals aus, wenn Clientcomputer nicht auf das Microsoft Content Delivery Network zugreifen können](how-to-configure-the-self-service-portal-when-client-computers-cannot-access-the-microsoft-content-delivery-network.md).


## Verwandte Themen


[Serverereignisprotokolle](server-event-logs.md)

[Konfigurieren der MBAM 2.5-Serverfunktionen](configuring-the-mbam-25-server-features.md)

[So konfigurieren Sie das Self-Service-Portal, wenn Clientcomputer nicht auf das Microsoft Content Delivery Network zugreifen können](how-to-configure-the-self-service-portal-when-client-computers-cannot-access-the-microsoft-content-delivery-network.md)

[Anpassen des Self-Service-Portals für Ihre Organisation](customizing-the-self-service-portal-for-your-organization.md)

[Überprüfen der Konfiguration von MBAM 2.5 Serverfunktionen](validating-the-mbam-25-server-feature-configuration.md)



## Sie haben einen Vorschlag für MBAM?
- [Hier](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)können Sie Vorschläge hinzufügen oder abstimmen. 
- Bei MBAM-Problemen verwenden Sie das [MBAM TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





