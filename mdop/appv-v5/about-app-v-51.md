---
title: Informationen zu App-V 5.1
description: Informationen zu App-V 5.1
author: dansimp
ms.assetid: 35bc9908-d502-4a9c-873f-8ee17b6d9d74
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 4f2404dcd431b32f5d9a4ae7c49f1e376979e04e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806110"
---
# Informationen zu App-V 5.1


Verwenden Sie die folgenden Abschnitte, um Informationen zu bedeutenden Änderungen zu überprüfen, die für Application Virtualization (App-V) 5,1 gelten:

[App-V 5,1-Softwarevoraussetzungen und unterstützte Konfigurationen](#bkmk-51-prereq-configs)

[Migrieren zu App-V 5,1](#bkmk-migrate-to-51)

[Neuerungen in App-V 5,1](#bkmk-whatsnew)

[App-V-Unterstützung für Windows 10](#bkmk-win10support)

[Änderungen der App-V-Verwaltungskonsole](#bkmk-mgmtconsole)

[Verbesserungen des Sequencers](#bkmk-seqimprove)

[Verbesserungen beim Paket Konverter](#bkmk-pkgconvimprove)

[Unterstützung für mehrere Skripts in einem einzelnen Ereignisauslöser](#bkmk-supmultscripts)

[Hartcodierter Pfad zum Installationsordner wird an das virtuelle Dateisystem-Stammverzeichnis umgeleitet](#bkmk-hardcodepath)

## <a href="" id="bkmk-51-prereq-configs"></a>App-V 5,1-Softwarevoraussetzungen und unterstützte Konfigurationen


Unter den folgenden Links finden Sie die Voraussetzungen für die App-V 5,1-Software und die unterstützten Konfigurationen.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Links zu Voraussetzungen und unterstützten Konfigurationen</th>
<th align="left">Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="app-v-51-prerequisites.md" data-raw-source="[App-V 5.1 Prerequisites](app-v-51-prerequisites.md)">Voraussetzungen für App-V 5.1</a></p></td>
<td align="left"><p>Erforderliche Software, die Sie vor dem Starten der App-V 5,1-Installation installieren müssen</p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="app-v-51-supported-configurations.md" data-raw-source="[App-V 5.1 Supported Configurations](app-v-51-supported-configurations.md)">App-V 5.1 – Unterstützte Konfigurationen</a></p></td>
<td align="left"><p>Unterstützte Betriebssysteme und Hardwareanforderungen für App-V Server, Sequencer und Client Komponenten</p></td>
</tr>
</tbody>
</table>



**Unterstützung für die Verwendung von Configuration Manager mit App-V:** App-V 5,1 unterstützt System Center 2012 R2 Configuration Manager SP1. Informationen zum Integrieren ihrer App-v-Umgebung in Configuration Manager und Configuration Manager finden Sie unter [Planen der APP-v-Integration in Configuration Manager](https://technet.microsoft.com/library/jj822982.aspx) .

## <a href="" id="bkmk-migrate-to-51"></a>Migrieren zu App-V 5,1


Verwenden Sie die folgenden Informationen, um aus früheren Versionen auf App-V 5,1 zu aktualisieren. Weitere Informationen finden Sie unter [Migrieren zu App-V 5,1 aus einer früheren Version](migrating-to-app-v-51-from-a-previous-version.md) .

### Vor dem Starten des Upgrades

Überprüfen Sie die folgenden Informationen, bevor Sie das Upgrade starten:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Zu überprüfende Elemente vor dem Upgrade</th>
<th align="left">Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Zu aktualisierbare Komponenten in beliebiger Reihenfolge</p></td>
<td align="left"><ol>
<li><p>App-V-Server</p></li>
<li><p>Sequencer</p></li>
<li><p>App-v Client oder App-v Remote Desktop Dienste (RDS)-Client</p></li>
</ol>
<div class="alert">
<strong>Hinweis:</strong><br/><p>Vor App-v 5,0 SP2 wurde die Client Verwaltungsbenutzeroberfläche mit der APP-v-Clientinstallation bereitgestellt. Für App-V 5,0 SP2-Installationen (oder höher) können Sie die Benutzeroberfläche der Clientverwaltung verwenden, indem Sie die <a href="https://www.microsoft.com/download/details.aspx?id=41186" data-raw-source="[Application Virtualization 5.0 Client UI Application](https://www.microsoft.com/download/details.aspx?id=41186)"> Benutzeroberflächenanwendung Application Virtualization 5,0 Client herunterladen </a> .</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>Aktualisieren von App-V 4. x</p></td>
<td align="left"><p>Sie müssen zuerst auf App-V 5,0 aktualisieren. Sie können nicht direkt von App-v 4. x auf App-v 5,1 aktualisieren. Weitere Informationen finden Sie unter:</p>
<ul>
<li><p>"Unterschiede zwischen App-v 4,6 und App-v 5,0" in der <a href="about-app-v-50.md" data-raw-source="[About App-V 5.0](about-app-v-50.md)"> App-v 5,0</a></p></li>
<li><p><a href="planning-for-migrating-from-a-previous-version-of-app-v.md" data-raw-source="[Planning for Migrating from a Previous Version of App-V](planning-for-migrating-from-a-previous-version-of-app-v.md)">Planen der Migration von einer früheren Version von App-V</a></p></li>
</ul>
<p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Aktualisieren von App-V 5,0 oder höher</p></td>
<td align="left"><p>Sie können direkt von einer der folgenden Versionen auf App-V 5,1 aktualisieren:</p>
<ul>
<li><p>App-V 5,0</p></li>
<li><p>App-V 5,0 SP1</p></li>
<li><p>App-V 5,0 SP2</p></li>
<li><p>App-V 5,0 SP3</p></li>
</ul>
<p>Führen Sie die Schritte in den verbleibenden Abschnitten dieses Themas aus, um auf App-V 5,1 zu aktualisieren.</p>
<p>Pakete und Verbindungsgruppen funktionieren weiterhin mit App-V 5,1, wie dies derzeit der Fall ist.</p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-steps-upgrd-infrastruc"></a>Schritte zum Upgrade der App-V-Infrastruktur

Führen Sie die folgenden Schritte aus, um die einzelnen Komponenten der APP-v-Infrastruktur auf App-v 5,1 zu aktualisieren. Die folgende Reihenfolge ist nur ein Vorschlag; Sie können Komponenten in beliebiger Reihenfolge aktualisieren.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Schritt</th>
<th align="left">Weitere Informationen</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Schritt 1: Aktualisieren Sie den App-V-Server.</p>
<div class="alert">
<strong>Hinweis:</strong><br/><p>Wenn Sie den App-V-Server nicht verwenden, überspringen Sie diesen Schritt, und fahren Sie mit dem nächsten Schritt fort.</p>
</div>
<div>

</div></td>
<td align="left"><p>Führen Sie folgende Schritte aus: </p>
<ol>
<li><p>Führen Sie eine der folgenden Aktionen aus, je nachdem, welche Methode Sie verwenden, um die Verwaltungsdatenbank und/oder die Berichtsdatenbank zu aktualisieren:</p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Daten Bank Aktualisierungsmethode</th>
<th align="left">Schritt</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows Installer</p></td>
<td align="left"><p>Überspringen Sie diesen Schritt, und wechseln Sie zu Schritt 2, "Wenn Sie den App-V-Server aktualisieren..."</p></td>
</tr>
<tr class="even">
<td align="left"><p>SQL-Skripts</p></td>
<td align="left"><p>Führen Sie die Schritte unter <a href="how-to-deploy-the-app-v-databases-by-using-sql-scripts.md" data-raw-source="[How to Deploy the App-V Databases by Using SQL Scripts](how-to-deploy-the-app-v-databases-by-using-sql-scripts.md)"> Vorgehensweise zum Bereitstellen der App-V-Datenbanken mithilfe von SQL-Skripts aus </a> .</p></td>
</tr>
</tbody>
</table>
<li><p>Wenn Sie den App-v-Server vom APP-v 5,0 SP1-Hotfix-Paket 3 oder höher aktualisieren, führen Sie die Schritte in Abschnitt <a href="check-reg-key-svr.md" data-raw-source="[Check registry keys after installing the App-V 5.0 SP3 Server](check-reg-key-svr.md)"> Überprüfen der Registrierungsschlüssel nach der Installation des App-v 5,0 SP3-Servers aus </a> .</p></li>
<li><p>Führen Sie die Schritte unter <a href="how-to-deploy-the-app-v-51-server.md" data-raw-source="[How to Deploy the App-V 5.1 Server](how-to-deploy-the-app-v-51-server.md)"> Bereitstellen des App-V 5,1-Servers aus.</a></p></li>
<p> </p></li>
</ol></td>
</tr>
<tr class="even">
<td align="left"><p>Schritt 2: Aktualisieren Sie den App-V-Sequenzer.</p></td>
<td align="left"><p>Weitere Informationen finden Sie unter <a href="how-to-install-the-sequencer-beta-gb18030.md" data-raw-source="[How to Install the Sequencer](how-to-install-the-sequencer-beta-gb18030.md)"> Installieren des Sequencers </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Schritt 3: Aktualisieren Sie den App-v-Client oder den App-v-RDS-Client.</p></td>
<td align="left"><p>Weitere Informationen finden Sie unter <a href="how-to-deploy-the-app-v-client-gb18030.md" data-raw-source="[How to Deploy the App-V Client](how-to-deploy-the-app-v-client-gb18030.md)"> Bereitstellen des App-V-Clients </a> .</p></td>
</tr>
</tbody>
</table>



### Konvertieren von Paketen, die mit einer früheren Version von App-V erstellt wurden

Verwenden Sie das Paket Konverter-Dienstprogramm, um virtuelle Anwendungspakete zu aktualisieren, die mit den Versionen von App-v vor App-v 5,0 erstellt wurden. Der Paket Konverter verwendet PowerShell zum Konvertieren von Paketen und kann die Automatisierung des Prozesses unterstützen, wenn viele Pakete vorhanden sind, für die eine Konvertierung erforderlich ist.

**Hinweis:**  
App-v 5,1-Pakete sind genauso wie App-v 5,0-Pakete. Es wurde keine Änderung des Paketformats zwischen den Versionen vorgenommen, und daher ist es nicht erforderlich, App-v 5,0-Pakete in App-v 5,1-Pakete zu konvertieren.



## <a href="" id="bkmk-whatsnew"></a>Neuerungen in App-V 5,1


Diese Abschnitte gelten für Benutzer, die bereits mit App-v vertraut sind und wissen möchten, was sich in App-v 5,1 geändert hat. Wenn Sie noch nicht mit App-v vertraut sind, sollten Sie zunächst die [Planung für App-v 5,1](planning-for-app-v-51.md)lesen.

### <a href="" id="bkmk-win10support"></a>App-V-Unterstützung für Windows 10

Die folgende Tabelle enthält die Windows 10-Unterstützung für App-V. Windows 10 wird in den Versionen von App-v vor App-v 5,1 nicht unterstützt.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Komponente</th>
<th align="left">App-V 5.1</th>
<th align="left">App-V 5,0</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>App-V-Client</p></td>
<td align="left"><p>Ja</p></td>
<td align="left"><p>Nein</p></td>
</tr>
<tr class="even">
<td align="left"><p>App-V RDS-Client</p></td>
<td align="left"><p>Ja</p></td>
<td align="left"><p>Nein</p></td>
</tr>
<tr class="odd">
<td align="left"><p>App-V-Sequenzer</p></td>
<td align="left"><p>Ja</p></td>
<td align="left"><p>Nein</p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-mgmtconsole"></a>Änderungen der App-V-Verwaltungskonsole

In diesem Abschnitt werden die aktuelle und die vorherige Funktionalität der App-V-Verwaltungskonsole verglichen.

### Silverlight ist nicht mehr erforderlich

Für die Benutzeroberfläche der Verwaltungskonsole ist Silverlight nicht mehr erforderlich. Die 5,1-Verwaltungskonsole ist auf HTML5 und JavaScript aufgebaut.

### Benachrichtigungen und Nachrichten werden in einem Dialogfeld einzeln angezeigt

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Neu in App-V 5,1</th>
<th align="left">Vor App-V 5,1</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Indikator für die Anzahl der Nachrichten:</strong></p>
<p>Auf der Titelleiste der App-V-Verwaltungskonsole wird nun neben einem Kennzeichnungssymbol eine Zahl angezeigt, die die Anzahl der Nachrichten angibt, die gelesen werden sollen.</p></td>
<td align="left"><p>Sie können jeweils nur eine Nachricht oder einen Fehler sehen, und Sie konnten nicht feststellen, wie viele Nachrichten vorhanden waren.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Nachrichtendarstellung:</strong></p>
<ul>
<li><p>Nachrichten, die eine Benutzereingabe erfordern, werden in einem separaten Dialogfeld angezeigt, das oben auf der aktuellen Seite angezeigt wird, die Sie gerade anzeigen, und eine Antwort anfordern, bevor Sie Sie schließen können.</p></li>
<li><p>Nachrichten und Fehler werden in einer Liste mit einer unter dem anderen angezeigt.</p></li>
</ul></td>
<td align="left"><p>Sie können jeweils nur eine Nachricht oder einen Fehler sehen.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Nachrichten werden nicht mehr angezeigt:</strong></p>
<p>Verwenden Sie den <strong> Link alle verwerfen, </strong> um alle Nachrichten und Fehler gleichzeitig zu schließen oder einzeln zu schließen.</p></td>
<td align="left"><p>Sie können Nachrichten und Fehler nur jeweils einzeln entlassen.</p></td>
</tr>
</tbody>
</table>



### Konsolenseiten sind nun getrennte URLs

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Neu in App-V 5,1</th>
<th align="left">Vor App-V 5,1</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Jede Seite in der Konsole hat eine andere URL, mit der Sie bestimmte Seiten für den schnellen Zugriff in Zukunft mit einer Textmarke versehen können.</p>
<p>Die Zahl, die in einigen URLs angezeigt wird, gibt das jeweilige Paket an. Diese Nummern sind eindeutig.</p></td>
<td align="left"><p>Auf alle Konsolenseiten wird über die gleiche URL zugegriffen.</p></td>
</tr>
</tbody>
</table>



### Neue, getrennte Seite für Verbindungsgruppen und Menüoption

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Neu in App-V 5,1</th>
<th align="left">Vor App-V 5,1</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Die Seite "Verbindungsgruppen" ist jetzt Teil des Hauptmenüs, auf der gleichen Ebene wie die Seite "Pakete".</p></td>
<td align="left"><p>Wenn Sie die Seite Verbindungsgruppen öffnen möchten, navigieren Sie auf der Seite Pakete.</p></td>
</tr>
</tbody>
</table>



### Menü Optionen für Pakete wurden geändert

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Neu in App-V 5,1</th>
<th align="left">Vor App-V 5,1</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Die folgenden Optionen sind jetzt Schaltflächen, die unten auf der Seite "Pakete" angezeigt werden:</p>
<ul>
<li><p>Hinzufügen oder aktualisieren</p></li>
<li><p>Veröffentlichen</p></li>
<li><p>Veröffentlichung</p></li>
<li><p>Delete</p></li>
</ul>
<p>Die folgenden Optionen werden weiterhin angezeigt, wenn Sie mit der rechten Maustaste auf ein Paket klicken, um das Dropdown-Kontextmenü zu öffnen:</p>
<ul>
<li><p>Veröffentlichen</p></li>
<li><p>Veröffentlichung</p></li>
<li><p>Bearbeiten von anzeigen Zugriffen</p></li>
<li><p>Bearbeiten der Bereitstellungskonfiguration</p></li>
<li><p>Bereitstellungskonfiguration übertragen von...</p></li>
<li><p>Zugriff und Konfiguration übertragen von...</p></li>
<li><p>Delete</p></li>
</ul>
<p>Wenn Sie auf <strong> Löschen klicken, </strong> um ein Paket zu entfernen, wird ein Dialogfeld geöffnet, in dem Sie aufgefordert werden, zu bestätigen, dass Sie das Paket löschen möchten.</p></td>
<td align="left"><p>Die <strong> Option zum Hinzufügen oder aktualisieren </strong> war eine Schaltfläche oben rechts auf der Seite "Pakete".</p>
<p>Die <strong> Optionen zum Veröffentlichen, Aufheben der </strong> <strong> Veröffentlichung </strong> und zum <strong> Löschen </strong> waren nur verfügbar, wenn Sie in der Liste Pakete mit der rechten Maustaste auf einen Paketnamen geklickt haben.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Die folgenden Paketvorgänge sind jetzt Schaltflächen auf der Paketdetailseite für jedes Paket:</p>
<ul>
<li><p>Übertragen (Dropdownmenü mit den folgenden Optionen):</p>
<ul>
<li><p>Bereitstellungskonfiguration übertragen von...</p></li>
<li><p>Zugriff und Konfiguration übertragen von...</p></li>
</ul></li>
<li><p>Bearbeiten (Verbindungsgruppen und anzeigen Zugriff)</p></li>
<li><p>Veröffentlichung</p></li>
<li><p>Delete</p></li>
<li><p>Bearbeiten der Standardkonfiguration</p></li>
</ul></td>
<td align="left"><p>Diese Paketoptionen waren nur verfügbar, wenn Sie in der Liste Pakete mit der rechten Maustaste auf einen Paketnamen geklickt haben.</p></td>
</tr>
</tbody>
</table>



### Symbole im linken Bereich haben neue Farben und Text

Die Farben der Symbole im linken Bereich wurden geändert, und Text wurde hinzugefügt, damit die Symbole mit anderen Microsoft-Produkten konsistent sind.

### Die Übersichtsseite wurde entfernt

Im linken Bereich der Verwaltungskonsole wurden die Menüoption Übersicht und die zugehörige Übersichtsseite entfernt.

### <a href="" id="bkmk-seqimprove"></a>Verbesserungen des Sequencers

Die folgenden Verbesserungen wurden am Paket-Editor im App-V 5,1-Sequenzer vorgenommen.

### Importieren und Exportieren der Manifestdatei

Sie können die AppxManifest.xml-Datei importieren und exportieren. Um die Manifestdatei zu exportieren, wählen Sie die Registerkarte **erweitert** aus, und klicken Sie im Feld Manifestdatei auf **exportieren...**. Sie können Änderungen an der Manifestdatei vornehmen, beispielsweise das Entfernen von Shell-Erweiterungen oder das Bearbeiten von Dateitypzuordnungen.

Nachdem Sie Ihre Änderungen vorgenommen haben, klicken Sie auf **importieren...** und wählen Sie die Datei aus, die Sie bearbeitet haben. Nachdem Sie das Dokument erfolgreich wieder in importiert haben, wird die Manifestdatei im Paket-Editor sofort aktualisiert.

**Achtung**  
Wenn Sie die Datei importieren, werden Ihre Änderungen mit dem XML-Schema überprüft. Wenn die Datei nicht gültig ist, wird eine Fehlermeldung angezeigt. Beachten Sie, dass es möglich ist, eine Datei zu importieren, die mit dem XML-Schema überprüft wird, die aber möglicherweise aus anderen Gründen noch nicht ausgeführt werden kann.



### Hinzufügen von Windows 10 zu Betriebssystemliste

Auf der Registerkarte Bereitstellung wurden die Windows-10 32-Bit-und Windows 10-64-Bit der Liste der Betriebssysteme hinzugefügt, für die Sie ein Paket sequenzieren können. Wenn Sie **ein beliebiges Betriebs System**auswählen, wird Windows 10 automatisch in die Betriebssysteme aufgenommen, die vom sequenzierten Paket unterstützt werden.

### Aktueller Pfad wird unten im virtuellen Registrierungs-Editor angezeigt

Auf der Registerkarte virtuelle Registrierung wird der Pfad nun unten im virtuellen Registrierungs-Editor angezeigt, mit dem Sie den aktuell ausgewählten Schlüssel ermitteln können. Zuvor mussten Sie durch die Registrierungsstruktur scrollen, um den aktuell ausgewählten Schlüssel zu finden.

### <a href="" id="combined--find-and-replace--dialog-box-and-shortcut-keys-added-in-virtual-registry-editor"></a>Kombiniertes Dialogfeld "suchen und ersetzen" und im virtuellen Registrierungs-Editor hinzugefügte Tastenkombinationen

Im virtuellen Registrierungs-Editor wurden Tastenkombinationen für die Option suchen (STRG + F) hinzugefügt, und ein Dialogfeld, in dem die Aufgaben "suchen" und "ersetzen" kombiniert wurden, wurde hinzugefügt, damit Sie Werte und Daten suchen und ersetzen können. Wenn Sie auf dieses kombinierte Dialogfeld zugreifen möchten, wählen Sie einen Schlüssel aus, und führen Sie eine der folgenden Aktionen aus:

-   Drücken Sie **STRG + H** .

-   Klicken Sie mit der rechten Maustaste auf einen Schlüssel, und wählen Sie **ersetzen**aus.

-   Wählen **View** Sie &gt; **virtueller Registrierungs** &gt; **Austausch**anzeigen aus.

Zuvor war das Dialogfeld "ersetzen" nicht vorhanden, und Sie mussten Änderungen manuell vornehmen.

### Erfolgreiches Umbenennen von Registrierungsschlüsseln und Paketdateien

Sie können virtuelle Registrierungsschlüssel und Dateien umbenennen, ohne dass ein Sequencer-Problem auftritt. Zuvor hat der Sequencer nicht mehr funktioniert, wenn Sie versucht haben, einen Schlüssel umzubenennen.

### Importieren und Exportieren von virtuellen Registrierungsschlüsseln

Sie können virtuelle Registrierungsschlüssel importieren und exportieren. Wenn Sie einen Schlüssel importieren möchten, klicken Sie mit der rechten Maustaste auf den Knoten, unter dem Sie den Schlüssel importieren möchten, navigieren Sie zu dem zu importierenden Schlüssel, und klicken Sie dann auf **importieren**. Um einen Schlüssel zu exportieren, klicken Sie mit der rechten Maustaste auf den Schlüssel, und wählen Sie **exportieren**aus.

### Importieren eines Verzeichnisses in das virtuelle Dateisystem

Sie können ein Verzeichnis in VFS importieren. Wenn Sie ein Verzeichnis importieren möchten, klicken Sie auf die Registerkarte **Paketdateien** , und klicken Sie dann auf **View** &gt; **Virtuelles Datei System** - &gt; **Importverzeichnis**anzeigen. Wenn Sie versuchen, ein Verzeichnis zu importieren, das Dateien enthält, die sich bereits im VFS befinden, schlägt der Import fehl, und es wird eine erläuternde Meldung angezeigt. Vor App-V 5,1 konnten keine Verzeichnisse importiert werden.

### Importieren oder Exportieren einer VFS-Datei, ohne Sie löschen und dann wieder zum Paket hinzufügen zu müssen

Sie können Dateien aus dem VFS importieren oder exportieren, ohne die Datei löschen und dann wieder zum Paket hinzufügen zu müssen. So können Sie beispielsweise dieses Feature verwenden, um ein Änderungsprotokoll in ein lokales Laufwerk zu exportieren, die Datei mit einem externen Editor zu bearbeiten und dann die Datei in VFS erneut zu importieren.

Wenn Sie eine Datei exportieren möchten, wählen Sie die Registerkarte **Paketdateien** aus, klicken Sie mit der rechten Maustaste auf die Datei im VFS, klicken Sie auf **exportieren**, und wählen Sie einen Exportspeicherort aus, aus dem Sie Ihre Änderungen vornehmen können.

Wenn Sie eine Datei importieren möchten, wählen Sie die Registerkarte **Paketdateien** aus, und klicken Sie mit der rechten Maustaste auf die Datei, die Sie exportiert haben. Navigieren Sie zu der Datei, die Sie bearbeitet haben, und klicken Sie dann auf **importieren**. Mit der importierten Datei wird die vorhandene Datei überschrieben.

Nachdem Sie eine Datei importiert haben, müssen Sie das Paket speichern, indem Sie auf **Datei** &gt; **Speichern**klicken.

### Menü zum Hinzufügen einer Paketdatei wurde verschoben

Die Menüoption zum Hinzufügen einer Paketdatei wurde verschoben. Um die Option hinzufügen zu finden, **Wählen Sie die** Registerkarte **Paketdateien** aus, und klicken Sie dann auf &gt; **virtuelle Datei System** &gt; **Datei hinzufügen**. Zuvor haben Sie mit der rechten Maustaste auf einen Ordner unter dem VFS-Knoten geklickt und dann **Datei hinzufügen**ausgewählt.

### Virtueller Registrierungsknoten erweitert die Computer-und Benutzer Strukturen standardmäßig

Wenn Sie die virtuelle Registrierung öffnen, werden die Computer-und Benutzer Strukturen unterhalb des Registrierungs Knotens der obersten Ebene angezeigt. Zuvor mussten Sie den Registrierungsknoten erweitern, um die darunter befindlichen Strukturen anzuzeigen.

### Aktivieren oder Deaktivieren von Browser Helper-Objekten

Sie können Browser Hilfsobjekte aktivieren oder deaktivieren, indem Sie auf der Registerkarte Erweitert der Sequencer-Benutzeroberfläche ein neues Kontrollkästchen aktivieren, Browser Hilfsobjekte aktivieren. Wenn Browser-helferobjekte:

-   Im Paket vorhanden und aktiviert sind, ist das Kontrollkästchen standardmäßig aktiviert.

-   Im Paket vorhanden und deaktiviert sind, ist das Kontrollkästchen standardmäßig deaktiviert.

-   Im Paket vorhanden ist, mit einem oder mehreren aktivierten und einem oder mehreren deaktivierten, ist das Kontrollkästchen standardmäßig auf unbestimmt eingestellt.

-   Im Paket nicht vorhanden ist, ist das Kontrollkästchen deaktiviert.

### <a href="" id="bkmk-pkgconvimprove"></a>Verbesserungen beim Paket Konverter

Sie können jetzt den Paket Konverter verwenden, um App-V 4,6-Pakete zu konvertieren, die Skripts enthalten, und Registrierungsinformationen und Skripts aus den Dateien des Quell-OSD sind jetzt in der Ausgabe des Paket Konverters enthalten.

Weitere Informationen, einschließlich Beispielen, finden Sie unter [Migrieren zu App-V 5,1 aus einer früheren Version](migrating-to-app-v-51-from-a-previous-version.md).

### <a href="" id="bkmk-supmultscripts"></a>Unterstützung für mehrere Skripts in einem einzelnen Ereignisauslöser

App-v 5,1 unterstützt die Verwendung mehrerer Skripts für einen einzelnen Ereignisauslöser für App-v-Pakete, einschließlich der Pakete, die Sie von App-v 4,6 in App-v 5,0 oder höher konvertieren. Um die Verwendung mehrerer Skripts zu ermöglichen, verwendet App-v 5,1 eine Skript Startanwendung mit dem Namen ScriptRunner.exe, die als Teil der APP-v-Clientinstallation installiert wird.

Weitere Informationen, einschließlich einer Liste der Ereignisauslöser und des Kontexts, unter dem Skripts ausgeführt werden können, finden Sie im Abschnitt Skripts in der [dynamischen Konfiguration von App-V 5,1](about-app-v-51-dynamic-configuration.md).

### <a href="" id="bkmk-hardcodepath"></a>Hartcodierter Pfad zum Installationsordner wird an das virtuelle Dateisystem-Stammverzeichnis umgeleitet

Wenn Sie Pakete von App-v 4,6 in 5,1 konvertieren, kann das App-v 5,1-Paket auf das hart codierte Laufwerk zugreifen, das Sie beim Erstellen von 4,6-Paketen verwenden mussten. Der Laufwerkbuchstabe ist das Laufwerk, das Sie als Installationslaufwerk auf dem 4,6-Sequenzcomputer ausgewählt haben. (Der standardmäßige Laufwerkbuchstabe ist Q:\\.)

Zuvor wurde der 4,6-Stammordner nicht erkannt, und der Zugriff auf App-V 5,0-Pakete war nicht möglich. App-v 5,1-Pakete können über den vollständigen Pfad auf hart codierte Dateien zugreifen oder Dateien unter dem App-V 4,6-Installations Stamm programmgesteuert auflisten.

**Technische Informationen:** Der APP-v 5,1-Paket Konverter speichert den App-v 4,6-Installations Stammordner und die kurzen Ordnernamen in der FilesystemMetadata.xml-Datei im File System-Element. Wenn der APP-v 5,1-Client den virtuellen Prozess erstellt, werden Anforderungen aus dem App-v 4,6-Installations Stamm dem virtuellen Dateisystem Stamm zugeordnet.

## So erhalten Sie MDOP-Technologien


App-V ist Teil des Microsoft Desktop Optimization Pack (MDOP). MDOP ist Teil von Microsoft Software Assurance. Weitere Informationen zur Microsoft-Software Assurance und zum Erwerb von MDOP finden Sie unter [wie erhalte ich MDOP](https://go.microsoft.com/fwlink/?LinkId=322049).






## Verwandte Themen


[Versionshinweise für App-V 5.1](release-notes-for-app-v-51.md)









