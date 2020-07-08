---
title: Auswerten von MBAM 1.0
description: Auswerten von MBAM 1.0
author: dansimp
ms.assetid: a1e2b674-eda9-4e1c-9b4c-e748470c71f2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: f09b06af52f5738fd50bfe727987b760d98552d9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811044"
---
# Auswerten von MBAM 1.0


Bevor Sie die Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) in einer Produktionsumgebung bereitstellen, sollten Sie Sie in einer Lab-Umgebung auswerten. Sie können die Informationen in diesem Thema verwenden, um MBAM in einer einzigen Server-Lab-Umgebung zu Evaluierungszwecken einzurichten.

Während die tatsächlichen Bereitstellungsschritte dem Szenario ähnlich sind, das unter [Anleitung zum Installieren und Konfigurieren von MBAM auf einem einzelnen Server](how-to-install-and-configure-mbam-on-a-single-server-mbam-1.md)beschrieben wird, enthält dieses Thema zusätzliche Informationen, mit denen Sie in kürzester Zeit eine MBAM-Evaluierungsumgebung einrichten können.

## Einrichten der Lab-Umgebung


Auch wenn Sie eine Nichtproduktionsinstanz von MBAM für die Auswertung in einer Lab-Umgebung einrichten, sollten Sie dennoch sicherstellen, dass Sie die Voraussetzungen für die Bereitstellung sowie die Hardware-und Softwareanforderungen erfüllt haben. Weitere Informationen finden Sie unter [Voraussetzungen für die MBAM 1,0-Bereitstellung](mbam-10-deployment-prerequisites.md) und [unterstützte MBAM 1,0-Konfigurationen](mbam-10-supported-configurations.md). Sie sollten auch überprüfen, [wie Sie Ihre Umgebung für MBAM 1,0 vorbereiten](preparing-your-environment-for-mbam-10.md) , bevor Sie mit der MBAM-Evaluierungsbereitstellung beginnen.

### Planen einer MBAM-Evaluierungsbereitstellung

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left">Aufgabe</th>
<th align="left">Verweise</th>
<th align="left">Anmerkungen</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Lesen Sie die Informationen zu den ersten Schritten zu MBAM, um ein grundlegendes Verständnis des Produkts zu erhalten, bevor Sie mit der Bereitstellungsplanung beginnen.</p></td>
<td align="left"><p><a href="getting-started-with-mbam-10.md" data-raw-source="[Getting Started with MBAM 1.0](getting-started-with-mbam-10.md)">Erste Schritte mit MBAM 1.0</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p></p>
<p>Bereiten Sie Ihre Computerumgebung für die MBAM-Installation vor. Dazu müssen Sie die transparente Datenverschlüsselung (transparent Data Encryption, DSA) auf den SQL Server-Instanzen aktivieren, die MBAM-Datenbanken hosten werden. Zum Aktivieren von DSA in ihrer Lab-Umgebung können Sie eine SQL-Datei erstellen, die für die Master-Datenbank ausgeführt wird, die auf der Instanz von SQL Server gehostet wird, die von MBAM verwendet wird.</p>
<div class="alert">
<strong>Hinweis:</strong><br/><p>Mit dem folgenden Beispiel können Sie eine SQL-Datei für Ihre Lab-Umgebung erstellen, um DSA schnell auf der SQL Server-Instanz zu aktivieren, die die MBAM-Datenbanken hosten soll. Mit diesen SQL Server-Befehlen wird DSA mithilfe eines lokal signierten SQL Server-Zertifikats aktiviert. Stellen Sie sicher, dass das DSA-Zertifikat und der zugehörige Verschlüsselungsschlüssel auf dem Beispiel lokalen Sicherungspfad von C:\backup gesichert werden <em> </em> . Das DSA-Zertifikat und der Schlüssel sind erforderlich, wenn Sie die Datenbank wiederherstellen oder das Zertifikat und den Schlüssel auf einen anderen Server verschieben, auf dem die DSA-Verschlüsselung vorhanden ist.</p>
</div>
<div>

</div>
<pre class="syntax" space="preserve"><code>USE master;
GO
CREATE MASTER KEY ENCRYPTION BY PASSWORD = &#39;P@55w0rd&#39;;
GO
CREATE CERTIFICATE tdeCert WITH SUBJECT = &#39;TDE Certificate&#39;;
GO
BACKUP CERTIFICATE tdeCert TO FILE = &#39;C:\Backup\TDECertificate.cer&#39;
   WITH PRIVATE KEY (
         FILE = &#39;C:\Backup\TDECertificateKey.pvk&#39;,
         ENCRYPTION BY PASSWORD = &#39;P@55w0rd&#39;);
GO</code></pre></td>
<td align="left"><p><a href="mbam-10-deployment-prerequisites.md" data-raw-source="[MBAM 1.0 Deployment Prerequisites](mbam-10-deployment-prerequisites.md)">Bereitstellungsvoraussetzungen für MBAM 1.0</a></p>
<p><a href="https://go.microsoft.com/fwlink/?LinkId=269703" data-raw-source="[Database Encryption in SQL Server 2008 Enterprise Edition](https://go.microsoft.com/fwlink/?LinkId=269703)">Datenbankverschlüsselung in SQL Server 2008 Enterprise Edition</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Planen und Konfigurieren von MBAM-Gruppenrichtlinienanforderungen</p></td>
<td align="left"><p><a href="planning-for-mbam-10-group-policy-requirements.md" data-raw-source="[Planning for MBAM 1.0 Group Policy Requirements](planning-for-mbam-10-group-policy-requirements.md)">Planen der Gruppenrichtlinienanforderungen für MBAM 1.0</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Planen und erstellen Sie die erforderlichen Active Directory-Domänendienste-Sicherheitsgruppen, und planen Sie die Mitgliedschaftsanforderungen für MBAM Local Security Group.</p></td>
<td align="left"><p><a href="planning-for-mbam-10-administrator-roles.md" data-raw-source="[Planning for MBAM 1.0 Administrator Roles](planning-for-mbam-10-administrator-roles.md)">Planen der Administratorrollen für MBAM 1.0</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Planen der Bereitstellung von MBAM Server Features</p></td>
<td align="left"><p><a href="planning-for-mbam-10-server-deployment.md" data-raw-source="[Planning for MBAM 1.0 Server Deployment](planning-for-mbam-10-server-deployment.md)">Planen der Serverbereitstellung für MBAM 1.0</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Planen der MBAM-Client Bereitstellung</p></td>
<td align="left"><p><a href="planning-for-mbam-10-client-deployment.md" data-raw-source="[Planning for MBAM 1.0 Client Deployment](planning-for-mbam-10-client-deployment.md)">Planen der Clientbereitstellung für MBAM 1.0</a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



### Durchführen einer MBAM-Evaluierungsbereitstellung

Nachdem Sie die erforderlichen Planungs-und Softwarevoraussetzungen installiert haben, um Ihre Computerumgebung für eine MBAM-Installation vorzubereiten, können Sie mit der MBAM-Evaluierungsbereitstellung beginnen.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Überprüfen Sie die MBAM-unterstützten Konfigurationsinformationen, um sicherzustellen, dass die ausgewählten Client-und Server Computer für die MBAM-Feature-Installation unterstützt werden.</p></td>
<td align="left"><p><a href="mbam-10-supported-configurations.md" data-raw-source="[MBAM 1.0 Supported Configurations](mbam-10-supported-configurations.md)">Von MBAM 1.0 unterstützte Konfigurationen</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Führen Sie MBAM-Setup aus, um MBAM-Server Features für Evaluierungszwecke auf einem einzelnen Server bereitzustellen.</p></td>
<td align="left"><p><a href="how-to-install-and-configure-mbam-on-a-single-server-mbam-1.md" data-raw-source="[How to Install and Configure MBAM on a Single Server](how-to-install-and-configure-mbam-on-a-single-server-mbam-1.md)">So installieren und Konfigurieren von MBAM auf einem Server</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Fügen Sie die Sicherheitsgruppen für Active Directory-Domänendienste, die Sie während der Planungsphase erstellt haben, zu den entsprechenden lokalen MBAM-Server Feature-lokalen Gruppen auf dem neuen MBAM-Server hinzu.</p></td>
<td align="left"><p><a href="planning-for-mbam-10-administrator-roles.md" data-raw-source="[Planning for MBAM 1.0 Administrator Roles](planning-for-mbam-10-administrator-roles.md)">Planen von MBAM 1,0-Administratorrollen </a> und <a href="how-to-manage-mbam-administrator-roles-mbam-1.md" data-raw-source="[How to Manage MBAM Administrator Roles](how-to-manage-mbam-administrator-roles-mbam-1.md)"> Verwalten von MBAM-Administratorrollen</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Erstellen und Bereitstellen der erforderlichen MBAM-Gruppenrichtlinienobjekte</p></td>
<td align="left"><p><a href="deploying-mbam-10-group-policy-objects.md" data-raw-source="[Deploying MBAM 1.0 Group Policy Objects](deploying-mbam-10-group-policy-objects.md)">Bereitstellen von Gruppenrichtlinienobjekten für MBAM 1.0</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Bereitstellen der MBAM-Client Software.</p></td>
<td align="left"><p><a href="deploying-the-mbam-10-client.md" data-raw-source="[Deploying the MBAM 1.0 Client](deploying-the-mbam-10-client.md)">Bereitstellen des MBAM 1.0-Clients</a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



## Konfigurieren von Lab-Computern für die MBAM-Evaluierung


Mit dem Registrierungs-Editor können Sie die Häufigkeitseinstellungen für den MBAM-Client Statusbericht ändern. Diese Änderungen sollten jedoch nur zu Testzwecken verwendet werden.

**Warnung**  
In diesem Thema wird beschrieben, wie Sie die Windows-Registrierung mit dem Registrierungs-Editor ändern. Wenn Sie die Windows-Registrierung falsch ändern, können Sie zu schwerwiegenden Problemen führen, bei denen Sie möglicherweise eine Neuinstallation von Windows erforderlich machen. Bevor Sie die Registrierung ändern, sollten Sie eine Sicherungskopie der Registrierungsdateien (System. dat und User. dat) erstellen. Microsoft kann nicht garantieren, dass die Probleme, die beim Ändern der Registrierung auftreten, behoben werden können. Ändern Sie die Registrierung auf Ihr eigenes Risiko.



### <a href="" id="modify-the-frequency-settings-on-mbam-client-status-reporting-"></a>Ändern der Häufigkeitseinstellungen für MBAM-Client Status Berichte

Die MBAM-Client Aktivierungs-und Statusberichts Frequenzen weisen einen Mindestwert von 90 Minuten auf, wenn Sie für die Verwendung von Gruppenrichtlinien eingestellt sind. Sie können diese Frequenzen auf MBAM-Clientcomputern ändern, indem Sie die Windows-Registrierung auf niedrigere Werte bearbeiten, wodurch die Tests beschleunigt werden. Wenn Sie die Häufigkeitseinstellungen für MBAM-Client Statusberichte ändern möchten, verwenden Sie einen Registrierungs-Editor, um zu **HKLM\\Software\\Policies\\FVE\\MDOPBitLockerManagement**zu navigieren, ändern Sie die Werte für **ClientWakeupFrequency** und **StatusReportingFrequency** in **1** als Mindestwert für vom Client unterstützt, und starten Sie dann den BitLocker-Verwaltungs Client Dienst erneut. Wenn Sie diese Änderung vornehmen, wird der MBAM-Client jede Minute darüber berichten. Sie können diese Werte nur dann einstellen, wenn Sie dies manuell in der Registrierung tun.

### <a href="" id="modify-the-startup-delay-on-mbam-client-service-"></a>Ändern der Startverzögerung für den MBAM-Client Dienst

Zusätzlich zu den MBAM-Client Wakeup-und Statusberichts Frequenzen gibt es eine zufällige Verzögerung von bis zu 90 Minuten, wenn der MBAM-Client-Agent-Dienst auf Clientcomputern gestartet wird. Wenn Sie die zufällige Verzögerung nicht möchten, erstellen Sie einen **DWORD** -Wert von **NoStartupDelay** unter **HKLM\\Software\\Microsoft\\MBAM**, legen Sie seinen Wert auf **1**, und starten Sie dann den BitLocker-Verwaltungs Client Dienst erneut.

## Verwandte Themen


[Erste Schritte mit MBAM 1.0](getting-started-with-mbam-10.md)









