---
title: Veröffentlichen von Anwendungen und Clientinteraktionen
description: Veröffentlichen von Anwendungen und Clientinteraktionen
author: dansimp
ms.assetid: 36a4bf6f-a917-41a6-9856-6248686df352
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: b94ef87043d428ac92fe1656b3afeb8a8b743808
ms.sourcegitcommit: 3e0500abde44d6a09c7ac8e3caf5e25929b490a4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2021
ms.locfileid: "11910820"
---
# <a name="application-publishing-and-client-interaction"></a>Veröffentlichen von Anwendungen und Clientinteraktionen


Dieser Artikel enthält technische Informationen zu allgemeinen App-V-Clientvorgängen und deren Integration in das lokale Betriebssystem.

-   [Vom Sequencer erstellte App-V-Paketdateien](#bkmk-appv-pkg-files-list)

-   [Was ist in der Appv-Datei enthalten?](#bkmk-appv-file-contents)

-   [Speicherorte von App-V-Clientdaten](#bkmk-files-data-storage)

-   [Paketregistrierung](#bkmk-pkg-registry)

-   [Verhalten des App-V-Paketspeichers](#bkmk-pkg-store-behavior)

-   [Roamingregistrierung und Daten](#bkmk-roaming-reg-data)

-   [App-V-Clientanwendungslebenszyklusverwaltung](#bkmk-clt-app-lifecycle)

-   [Integration von App-V-Paketen](#bkmk-integr-appv-pkgs)

-   [Dynamische Konfigurationsverarbeitung](#bkmk-dynamic-config)

-   [Parallele Assemblys](#bkmk-sidebyside-assemblies)

-   [Clientprotokollierung](#bkmk-client-logging)

Weitere Referenzinformationen finden Sie auf der Downloadseite der [Dokumentationsressourcen von Microsoft Application Virtualization (App-V).](https://www.microsoft.com/download/details.aspx?id=27760)

## <a name="app-v-package-files-created-by-the-sequencer"></a><a href="" id="bkmk-appv-pkg-files-list"></a>Vom Sequencer erstellte App-V-Paketdateien


Der Sequencer erstellt App-V-Pakete und erzeugt eine virtualisierte Anwendung. Der Sequenzierungsprozess erstellt die folgenden Dateien:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Datei</th>
<th align="left">Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>.appv</p></td>
<td align="left"><ul>
<li><p>Die primäre Paketdatei, die die erfassten Ressourcen und Statusinformationen aus dem Sequenzierungsprozess enthält.</p></li>
<li><p>Architektur der Paketdatei, der Veröffentlichungsinformationen und der Registrierung in einem tokenisierten Format, das bei der Übermittlung erneut auf einen Computer und einen bestimmten Benutzer angewendet werden kann.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>.MSI</p></td>
<td align="left"><p>Ausführbarer Bereitstellungswrapper, den Sie zum manuellen Bereitstellen von APPV-Dateien oder mithilfe einer Bereitstellungsplattform eines Drittanbieters verwenden können.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>_DeploymentConfig.XML</p></td>
<td align="left"><p>Datei zum Anpassen der Standardveröffentlichungsparameter für alle Anwendungen in einem Paket, das global für alle Benutzer auf einem Computer bereitgestellt wird, auf dem der App-V-Client ausgeführt wird.</p></td>
</tr>
<tr class="even">
<td align="left"><p>_UserConfig.XML</p></td>
<td align="left"><p>Datei zum Anpassen der Veröffentlichungsparameter für alle Anwendungen in einem Paket, das für einen bestimmten Benutzer auf einem Computer bereitgestellt wird, auf dem der App-V-Client ausgeführt wird.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Report.xml</p></td>
<td align="left"><p>Zusammenfassung der Nachrichten, die sich aus dem Sequenzierungsprozess ergeben, einschließlich der ausgelassenen Treiber, Dateien und Registrierungsspeicherorte.</p></td>
</tr>
<tr class="even">
<td align="left"><p>.CAB</p></td>
<td align="left"><p><em>Optional: </em> Paketbeschleunigerdatei, die verwendet wird, um ein zuvor sequenziertes virtuelles Anwendungspaket automatisch neu zu erstellen.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>.appvt</p></td>
<td align="left"><p><em>Optional: </em> Die Sequencer-Vorlagendatei wird verwendet, um häufig wiederverwendete Sequencer-Einstellungen beizubehalten.</p></td>
</tr>
</tbody>
</table>

 

Informationen zur Sequenzierung finden Sie im [Handbuch zur Application Virtualization-Sequenzierung.](https://go.microsoft.com/fwlink/?LinkID=269810)

## <a name="whats-in-the-appv-file"></a><a href="" id="bkmk-appv-file-contents"></a>Was ist in der Appv-Datei enthalten?


Die Appv-Datei ist ein Container, in dem XML- und Nicht-XML-Dateien in einer einzigen Entität gespeichert werden. Diese Datei basiert auf dem AppX-Format, das auf dem Open Packaging Conventions (OPC)-Standard basiert.

Um den Inhalt der Appv-Datei anzuzeigen, erstellen Sie eine Kopie des Pakets, und benennen Sie die kopierte Datei in eine ZIP-Erweiterung um.

Die Appv-Datei enthält den folgenden Ordner und die folgenden Dateien, die beim Erstellen und Veröffentlichen einer virtuellen Anwendung verwendet werden:

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Name</th>
<th align="left">Typ</th>
<th align="left">Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Stamm</p></td>
<td align="left"><p>Dateiordner</p></td>
<td align="left"><p>Verzeichnis, das das Dateisystem für die virtualisierte Anwendung enthält, die während der Sequenzierung erfasst wird.</p></td>
</tr>
<tr class="even">
<td align="left"><p>[Content_Types].xml</p></td>
<td align="left"><p>XML-Datei</p></td>
<td align="left"><p>Liste der wichtigsten Inhaltstypen in der Appv-Datei (z. B. DLL, EXE, BIN).</p></td>
</tr>
<tr class="odd">
<td align="left"><p>AppxBlockMap.xml</p></td>
<td align="left"><p>XML-Datei</p></td>
<td align="left"><p>Layout der appv-Datei, die File-, Block- und BlockMap-Elemente verwendet, die den Speicherort und die Überprüfung von Dateien im App-V-Paket ermöglichen.</p></td>
</tr>
<tr class="even">
<td align="left"><p>AppxManifest.xml</p></td>
<td align="left"><p>XML-Datei</p></td>
<td align="left"><p>Metadaten für das Paket, das die erforderlichen Informationen zum Hinzufügen, Veröffentlichen und Starten des Pakets enthält. Enthält Erweiterungspunkte (Dateitypzuordnungen und Verknüpfungen) sowie die Namen und GUIDs, die dem Paket zugeordnet sind.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>FilesystemMetadata.xml</p></td>
<td align="left"><p>XML-Datei</p></td>
<td align="left"><p>Liste der während der Sequenzierung erfassten Dateien, einschließlich Attributen (z. B. Verzeichnisse, Dateien, undurchsichtige Verzeichnisse, leere Verzeichnisse und lange und kurze Namen).</p></td>
</tr>
<tr class="even">
<td align="left"><p>PackageHistory.xml</p></td>
<td align="left"><p>XML-Datei</p></td>
<td align="left"><p>Informationen zum Sequenzierungscomputer (Betriebssystemversion, Internet Explorer-Version, .Net Framework-Version) und Prozess (Upgrade, Paketversion).</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Registry.dat</p></td>
<td align="left"><p>DAT-Datei</p></td>
<td align="left"><p>Registrierungsschlüssel und Werte, die während des Sequenzierungsprozesses für das Paket erfasst werden.</p></td>
</tr>
<tr class="even">
<td align="left"><p>StreamMap.xml</p></td>
<td align="left"><p>XML-Datei</p></td>
<td align="left"><p>Liste der Dateien für den primären und Veröffentlichungsfeatureblock. Der Veröffentlichungsfeatureblock enthält die ICO-Dateien und die erforderlichen Teile von Dateien (EXE und DLL) für die Veröffentlichung des Pakets. Wenn vorhanden, enthält der primäre Featureblock Dateien, die während des Sequenzierungsprozesses für das Streaming optimiert wurden.</p></td>
</tr>
</tbody>
</table>

 

## <a name="app-v-client-data-storage-locations"></a><a href="" id="bkmk-files-data-storage"></a>Speicherorte von App-V-Clientdaten


Der App-V-Client führt Aufgaben aus, um sicherzustellen, dass virtuelle Anwendungen ordnungsgemäß ausgeführt werden und wie lokal installierte Anwendungen funktionieren. Der Vorgang zum Öffnen und Ausführen virtueller Anwendungen erfordert eine Zuordnung aus dem virtuellen Dateisystem und der Registrierung, um sicherzustellen, dass die Anwendung über die erforderlichen Komponenten einer herkömmlichen Anwendung verfügt, die von Benutzern erwartet wird. In diesem Abschnitt werden die Ressourcen beschrieben, die zum Ausführen virtueller Anwendungen erforderlich sind, und der Speicherort, an dem App-V die Objekte speichert.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Name</th>
<th align="left">Pfad</th>
<th align="left">Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Paket-Store</p></td>
<td align="left"><p>%ProgramData%\App-V</p></td>
<td align="left"><p>Standardspeicherort für schreibgeschützte Paketdateien</p></td>
</tr>
<tr class="even">
<td align="left"><p>Computerkatalog</p></td>
<td align="left"><p>%ProgramData%\Microsoft\AppV\Client\Catalog</p></td>
<td align="left"><p>Enthält Konfigurationsdokumente pro Computer</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Benutzerkatalog</p></td>
<td align="left"><p>%AppData%\Microsoft\AppV\Client\Catalog</p></td>
<td align="left"><p>Enthält Benutzerkonfigurationsdokumente</p></td>
</tr>
<tr class="even">
<td align="left"><p>Verknüpfungssicherungen</p></td>
<td align="left"><p>%AppData%\Microsoft\AppV\Client\Integration\ShortCutBackups</p></td>
<td align="left"><p>Speichert vorherige Integrationspunkte, die die Wiederherstellung bei der Veröffentlichung des Pakets ermöglichen</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Copy on Write (SHAPES) Roaming</p></td>
<td align="left"><p>%AppData%\Microsoft\AppV\Client\VFS</p></td>
<td align="left"><p>Beschreibbarer Roamingspeicherort für Paketänderungen</p></td>
</tr>
<tr class="even">
<td align="left"><p>Copy on Write (VOM) Local</p></td>
<td align="left"><p>%LocalAppData%\Microsoft\AppV\Client\VFS</p></td>
<td align="left"><p>Schreibbarer Nicht-Roamingspeicherort für Paketänderungen</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Computerregistrierung</p></td>
<td align="left"><p>HKLM\Software\Microsoft\AppV</p></td>
<td align="left"><p>Enthält Paketstatusinformationen, einschließlich VReg für Computer oder global veröffentlichte Pakete (Computerstruktur)</p></td>
</tr>
<tr class="even">
<td align="left"><p>Benutzerregistrierung</p></td>
<td align="left"><p>HKCU\Software\Microsoft\AppV</p></td>
<td align="left"><p>Enthält Informationen zum Benutzerpaketstatus, einschließlich VReg</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Benutzerregistrierungsklassen</p></td>
<td align="left"><p>HKCU\Software\Classes\AppV</p></td>
<td align="left"><p>Enthält zusätzliche Informationen zum Benutzerpaketstatus</p></td>
</tr>
</tbody>
</table>

 

Weitere Details zur Tabelle finden Sie im abschnitt unten und im gesamten Dokument.

### <a name="package-store"></a>Paketspeicher

Der App-V-Client verwaltet die im Paketspeicher bereitgestellten Anwendungsressourcen. Dieser Standardspeicherort ist `%ProgramData%\App-V` , Aber Sie können ihn während oder nach dem Setup mithilfe des `Set-AppVClientConfiguration` PowerShell-Befehls konfigurieren, der die lokale Registrierung `PackageInstallationRoot` (Wert unter dem `HKLM\Software\Microsoft\AppV\Client\Streaming` Schlüssel) ändert. Der Paketspeicher muss sich in einem lokalen Pfad im Clientbetriebssystem befinden. Die einzelnen Pakete werden im Paketspeicher in Unterverzeichnissen gespeichert, die nach der Paket-GUID und Version-GUID benannt sind.

Beispiel für einen Pfad zu einer bestimmten Anwendung:

``` syntax
C:\ProgramData\App-V\PackGUID\VersionGUID
```

Informationen zum Ändern des Standardspeicherorts des Paketspeichers während des Setups finden Sie unter [Bereitstellen des App-V-Clients.](how-to-deploy-the-app-v-client-51gb18030.md)

### <a name="shared-content-store"></a>Freigegebene Inhalte Store

Wenn der App-V-Client im Modus "Freigegebene Inhalte Store" konfiguriert ist, werden beim Auftreten eines Datenstromfehlers keine Daten auf den Datenträger geschrieben, was bedeutet, dass die Pakete minimalen lokalen Speicherplatz (Veröffentlichungsdaten) benötigen. Die Verwendung von weniger Speicherplatz ist in VDI-Umgebungen sehr wünschenswert, in denen lokaler Speicher eingeschränkt werden kann, und das Streamen der Anwendungen von einem Leistungsfähigen Netzwerkstandort (z. B. san) ist vorzuziehen. Weitere Informationen zum Modus für den freigegebenen Inhaltsspeicher finden Sie unter <https://go.microsoft.com/fwlink/p/?LinkId=392750> .

**Hinweis:**  
Der Computer und der Paketspeicher müssen sich auf einem lokalen Laufwerk befinden, auch wenn Sie freigegebene Inhalte Store Konfigurationen für den App-V-Client verwenden.

 

### <a name="package-catalogs"></a>Paketkataloge

Der App-V-Client verwaltet die folgenden beiden dateibasierten Speicherorte:

-   **Kataloge (Benutzer und Computer).**

-   **Registrierungsspeicherorte** – hängt davon ab, wie das Paket für die Veröffentlichung vorgesehen ist. Es gibt einen Katalog (Datenspeicher) für den Computer und einen Katalog für jeden einzelnen Benutzer. Der Computerkatalog speichert globale Informationen, die für alle Benutzer oder einen beliebigen Benutzer gelten, und der Benutzerkatalog speichert Informationen, die für einen bestimmten Benutzer gelten. Der Katalog ist eine Sammlung dynamischer Konfigurationen und Manifestdateien. es gibt diskrete Daten für Datei und Registrierung pro Paketversion. 

### <a name="machine-catalog"></a>Computerkatalog

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p>Beschreibung</p></td>
<td align="left"><p>Speichert Paketdokumente, die Benutzern auf dem Computer zur Verfügung stehen, wenn Pakete hinzugefügt und veröffentlicht werden. Wenn ein Paket jedoch zur Veröffentlichungszeit "global" ist, sind die Integrationen für alle Benutzer verfügbar.</p>
<p>Wenn ein Paket nicht global ist, werden die Integrationen nur für bestimmte Benutzer veröffentlicht, aber es gibt weiterhin globale Ressourcen, die geändert werden und für jeden auf dem Clientcomputer sichtbar sind (z. B. befindet sich das Paketverzeichnis an einem freigegebenen Datenträgerspeicherort).</p>
<p>Wenn ein Paket für einen Benutzer auf dem Computer verfügbar ist (global oder nicht global), wird das Manifest im Computerkatalog gespeichert. Wenn ein Paket global veröffentlicht wird, gibt es eine dynamische Konfigurationsdatei, die im Computerkatalog gespeichert ist. Daher wird die Bestimmung, ob ein Paket global ist, entsprechend der Angabe definiert, ob im Computerkatalog eine Richtliniendatei (UserDeploymentConfiguration-Datei) vorhanden ist.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Standardspeicherort</p></td>
<td align="left"><p><code>%programdata%\Microsoft\AppV\Client\Catalog&lt;/code&gt;</p>
<p>Dieser Speicherort ist nicht identisch mit dem Speicherort des Pakets Store. Das Paket-Store ist die goldfarbene oder einmalige Kopie der Paketdateien.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Dateien im Computerkatalog</p></td>
<td align="left"><ul>
<li><p>Manifest.xml</p></li>
<li><p>DeploymentConfiguration.xml</p></li>
<li><p>UserManifest.xml (global veröffentlichtes Paket)</p></li>
<li><p>UserDeploymentConfiguration.xml (global veröffentlichtes Paket)</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Zusätzlicher Speicherort des Computerkatalogs, der verwendet wird, wenn das Paket Teil einer Verbindungsgruppe ist</p></td>
<td align="left"><p>Der folgende Speicherort befindet sich zusätzlich zu dem oben erwähnten spezifischen Paketspeicherort:</p>
<p><code>%programdata%\Microsoft\AppV\Client\Catalog\PackageGroups\ConGroupGUID\ConGroupVerGUID</code></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Zusätzliche Dateien im Computerkatalog, wenn das Paket Teil einer Verbindungsgruppe ist</p></td>
<td align="left"><ul>
<li><p>PackageGroupDescriptor.xml</p></li>
<li><p>UserPackageGroupDescriptor.xml (global veröffentlichte Verbindungsgruppe)</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

### <a name="user-catalog"></a>Benutzerkatalog

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p>Beschreibung</p></td>
<td align="left"><p>Wird während des Veröffentlichungsprozesses erstellt. Enthält Informationen zum Veröffentlichen des Pakets und wird auch beim Start verwendet, um sicherzustellen, dass ein Paket für einen bestimmten Benutzer bereitgestellt wird. Erstellt an einem Roamingspeicherort und enthält benutzerspezifische Veröffentlichungsinformationen.</p>
<p>Wenn ein Paket für einen Benutzer veröffentlicht wird, wird die Richtliniendatei im Benutzerkatalog gespeichert. Gleichzeitig wird auch eine Kopie des Manifests im Benutzerkatalog gespeichert. Wenn eine Paketberechtigung für einen Benutzer entfernt wird, werden die relevanten Paketdateien aus dem Benutzerkatalog entfernt. Beim Betrachten des Benutzerkatalogs kann ein Administrator das Vorhandensein einer Dynamischen Konfigurationsdatei anzeigen, die angibt, dass das Paket für diesen Benutzer berechtigt ist.</p>
<p>Für Roamingbenutzer muss sich der Benutzerkatalog an einem Roaming- oder freigegebenen Speicherort befinden, um das alte App-V-Verhalten von Benutzeradressierung standardmäßig beizubehalten. Berechtigungen und Richtlinien sind an einen Benutzer und nicht an einen Computer gebunden. Daher sollten sie mit dem Benutzer roaming, sobald er bereitgestellt wurde.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Standardspeicherort</p></td>
<td align="left"><p><code>appdata\roaming\Microsoft\AppV\Client\Catalog\Packages\PkgGUID\VerGUID</code></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Dateien im Benutzerkatalog</p></td>
<td align="left"><ul>
<li><p>UserManifest.xml</p></li>
<li><p>DynamicConfiguration.xml oder UserDeploymentConfiguration.xml</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Zusätzlicher Speicherort des Benutzerkatalogs, der verwendet wird, wenn das Paket Teil einer Verbindungsgruppe ist</p></td>
<td align="left"><p>Der folgende Speicherort befindet sich zusätzlich zu dem oben erwähnten spezifischen Paketspeicherort:</p>
<p><code>appdata\roaming\Microsoft\AppV\Client\Catalog\PackageGroups\PkgGroupGUID\PkgGroupVerGUID</code></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Zusätzliche Datei im Computerkatalog, wenn das Paket Teil einer Verbindungsgruppe ist</p></td>
<td align="left"><p><code>UserPackageGroupDescriptor.xml</code></p></td>
</tr>
</tbody>
</table>

 

### <a name="shortcut-backups"></a>Verknüpfungssicherungen

Während des Veröffentlichungsprozesses sichert der App-V-Client alle Verknüpfungen und Integrationspunkte `%AppData%\Microsoft\AppV\Client\Integration\ShortCutBackups.` auf Diese Sicherung ermöglicht die Wiederherstellung dieser Integrationspunkte auf die vorherigen Versionen, wenn das Paket nicht veröffentlicht wird.

### <a name="copy-on-write-files"></a>Beim Schreiben von Dateien kopieren

Das Paket Store enthält eine kopie der Paketdateien, die vom Veröffentlichungsserver gestreamt wurden. Während des normalen Betriebs einer App-V-Anwendung kann der Benutzer oder Dienst Änderungen an den Dateien erfordern. Diese Änderungen werden nicht im Paketspeicher vorgenommen, um ihre Fähigkeit zum Reparieren der Anwendung zu erhalten, wodurch diese Änderungen entfernt werden. Diese Speicherorte, die als COPY on Write (MOF) bezeichnet werden, unterstützen sowohl Roaming- als auch Nicht-Roamingspeicherorte. Der Speicherort, an dem die Änderungen gespeichert werden, hängt davon ab, wo die Anwendung so programmiert wurde, dass Änderungen in einer systemeigenen Umgebung geschrieben werden.

### <a name="cow-roaming"></a>ROAMING VON 2013

Der oben beschriebene SPEICHERORT FÜR DAS ROAMING speichert Änderungen an Dateien und Verzeichnissen, die auf den typischen Speicherort "%AppData% " oder "\\Users\\{username}\\AppData\\Roaming" abzielen. Diese Verzeichnisse und Dateien werden dann basierend auf den Betriebssystemeinstellungen verschoben.

### <a name="cow-local"></a>LOKALES GEBIETSSCHEMA

Der LOKALE SPEICHERORT ähnelt dem Roamingspeicherort, aber die Verzeichnisse und Dateien werden nicht auf andere Computer übertragen, auch wenn die Roamingunterstützung konfiguriert wurde. Der oben beschriebene LOKALE SPEICHERORT SPEICHERT Änderungen, die für typische Fenster und nicht für den Speicherort %AppData% gelten. Die aufgeführten Verzeichnisse variieren, es gibt jedoch zwei Speicherorte für alle typischen Windows Speicherorte (z. B. Common AppData und Common AppDataS). S **** gibt den eingeschränkten Speicherort an, wenn der virtuelle Dienst die Änderung als einen anderen erhöhten Benutzer als die angemeldeten Benutzer anfordert. Der**Nicht-S-Speicherort** speichert benutzerbasierte Änderungen.

## <a name="package-registry"></a><a href="" id="bkmk-pkg-registry"></a>Paketregistrierung


Bevor eine Anwendung auf die Paketregistrierungsdaten zugreifen kann, muss der App-V-Client die Paketregistrierungsdaten den Anwendungen zur Verfügung stellen. Der App-V-Client verwendet die echte Registrierung als Sicherungsspeicher für alle Registrierungsdaten.

Wenn dem App-V-Client ein neues Paket hinzugefügt wird, eine Kopie der REGISTRIERUNG. DIE DAT-Datei aus dem Paket wird unter `%ProgramData%\Microsoft\AppV\Client\VREG\{Version GUID}.dat` erstellt. Der Name der Datei ist die Versions-GUID mit der . DAT-Erweiterung. Diese Kopie wird deshalb erstellt, um sicherzustellen, dass die tatsächliche Strukturdatei im Paket nie verwendet wird, was das Entfernen des Pakets zu einem späteren Zeitpunkt verhindern würde.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Registry.dat aus paket Store</strong></p></td>
<td align="left"><p><strong> &gt; </strong></p></td>
<td align="left"><p><strong>%ProgramData%\Microsoft\AppV\Client\Vreg{VersionGuid}.dat</strong></p></td>
</tr>
</tbody>
</table>

 

Wenn die erste Anwendung aus dem Paket auf dem Client gestartet wird, stufet oder kopiert der Client den Inhalt aus der Strukturdatei und erstellt die Paketregistrierungsdaten an einem alternativen Speicherort `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\AppV\Client\Packages\PackageGuid\Versions\VersionGuid\REGISTRY` neu. Die mehrstufigen Registrierungsdaten haben zwei unterschiedliche Typen von Computerdaten und Benutzerdaten. Computerdaten werden für alle Benutzer auf dem Computer freigegeben. Benutzerdaten werden für jeden Benutzer an einem benutzerspezifischen Speicherort `HKCU\Software\Microsoft\AppV\Client\Packages\PackageGuid\Registry\User` aufgeführt. Die Computerdaten werden letztendlich zum Zeitpunkt der Paketentfernung entfernt, und die Benutzerdaten werden bei einem Unveröffentlichten Benutzervorgang entfernt.

### <a name="package-registry-staging-vs-connection-group-registry-staging"></a>Staging der Paketregistrierung im Vergleich zum Staging der Verbindungsgruppenregistrierung

Wenn Verbindungsgruppen vorhanden sind, gilt der vorherige Prozess des Stagings der Registrierung, aber anstatt eine Strukturdatei zu verarbeiten, gibt es mehrere. Die Dateien werden in der Reihenfolge verarbeitet, in der sie in der Verbindungsgruppen-XML angezeigt werden, wobei der erste Writer Konflikte gewonnen hat.

Die mehrstufige Registrierung bleibt auf die gleiche Weise erhalten wie im Fall eines einzelnen Pakets. Mehrstufige Benutzerregistrierungsdaten bleiben für die Verbindungsgruppe erhalten, bis sie deaktiviert sind. Mehrstufige Computerregistrierungsdaten werden beim Entfernen von Verbindungsgruppen entfernt.

### <a name="virtual-registry"></a>Virtuelle Registrierung

Der Zweck der virtuellen Registrierung (VREG) besteht darin, eine einzelne zusammengeführte Ansicht der Paketregistrierung und der systemeigenen Registrierung für Anwendungen bereitzustellen. Es bietet auch SCHREIB-/Kopierfunktion (COPY-on-Write, SCHREIBVORGÄNGE) – d. h. alle Änderungen, die aus dem Kontext eines virtuellen Prozesses an der Registrierung vorgenommen werden, werden an einem separaten ENTF-Speicherort vorgenommen. Dies bedeutet, dass die VREG bis zu drei separate Registrierungsspeicherorte in einer einzigen Ansicht kombinieren muss, basierend auf den aufgefüllten Speicherorten im REGISTRY-PAKET – &gt; &gt; systemintern. Wenn eine Anforderung für eine Registrierungsdaten gestellt wird, wird sie in der Reihenfolge gesucht, bis sie die angeforderten Daten findet. Dies bedeutet, dass ein Wert, der an einem SPEICHERORT gespeichert ist, nicht zu anderen Speicherorten fortgesetzt wird. Wenn sich jedoch keine Daten am SPEICHERORT befinden, wird der Vorgang mit dem Paket und dem systemeigenen Speicherort fortgesetzt, bis die entsprechenden Daten gefunden werden.

### <a name="registry-locations"></a>Registrierungsspeicherorte

Es gibt zwei Paketregistrierungsspeicherorte und zwei Verbindungsgruppenspeicherorte, an denen der App-V-Client Registrierungsinformationen speichert, je nachdem, ob das Paket einzeln oder als Teil einer Verbindungsgruppe veröffentlicht wird. Es gibt drei LOCATIONS-Speicherorte für Pakete und drei für Verbindungsgruppen, die von VREG erstellt und verwaltet werden. Einstellungen für Pakete und Verbindungsgruppen werden nicht freigegeben:

**Single Package VReg:**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Pfad</strong></p></td>
<td align="left"><p><strong>Beschreibung</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>KUH</strong></p></td>
<td align="left"><ul>
<li><p>Computerregistrierung\Client\Pakete\PkgGUID\REGISTRY (Nur Erhöhter Prozess kann schreiben)</p></li>
<li><p>User Registry\Client\Packages\PkgGUID\REGISTRY (User Roaming anything written under HKCU except Software\Classes</p></li>
<li><p>Benutzerregistrierungsklassen\Client\Pakete\PkgGUID\REGISTRY (HKCU\Software\Classes-Schreibvorgänge und HKLM für nicht erhöhten Prozess)</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Paket</strong></p></td>
<td align="left"><ul>
<li><p>Computerregistrierung\Client\Pakete\PkgGUID\Versionen\VerGuid\Registry\Machine</p></li>
<li><p>Benutzerregistrierungsklassen\Client\Pakete\PkgGUID\Versionen\VerGUID\Registry</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Ursprünglich</strong></p></td>
<td align="left"><ul>
<li><p>Systemeigener Anwendungsregistrierungsspeicherort</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

 

**Connection Group VReg:**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Pfad</strong></p></td>
<td align="left"><p><strong>Beschreibung</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>KUH</strong></p></td>
<td align="left"><ul>
<li><p>Computerregistrierung\Client\PackageGroups\GrpGUID\REGISTRY (nur Erhöhter Prozess kann schreiben)</p></li>
<li><p>Benutzerregistrierung\Client\PackageGroups\GrpGUID\REGISTRY (In HKCU geschriebene Elemente außer Software\Klassen</p></li>
<li><p>Benutzerregistrierungsklassen\Client\PackageGroups\GrpGUID\REGISTRY</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Paket</strong></p></td>
<td align="left"><ul>
<li><p>Computerregistrierung\Client\PackageGroups\GrpGUID\Versions\VerGUID\REGISTRY</p></li>
<li><p>Benutzerregistrierungsklassen\Client\PackageGroups\GrpGUID\Versions\VerGUID\REGISTRY</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Ursprünglich</strong></p></td>
<td align="left"><ul>
<li><p>Systemeigener Anwendungsregistrierungsspeicherort</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

 

Es gibt zwei LOCATIONS für HKLM; Prozesse mit erhöhten und nicht erhöhten Rechten. Prozesse mit erhöhten Rechten schreiben HKLM-Änderungen immer in den sicheren XAML-Code unter HKLM. Prozesse, die nicht über erhöhte Rechte verfügen, schreiben HKLM-Änderungen unter HKCU\\Software\\Classes immer in das nicht sichere XAML-Objekt. Wenn eine Anwendung Änderungen von HKLM liest, lesen Prozesse mit erhöhten Rechten Änderungen aus dem sicheren XAML-Element unter HKLM. Lesevorgänge mit nicht erhöhten Rechten werden von beiden gelesen, wobei zuerst die Änderungen bevorzugt werden, die in der unsicheren XAML vorgenommen wurden.

### <a name="pass-through-keys"></a>Pass-Through-Schlüssel

Pass-Through-Schlüssel ermöglichen es einem Administrator, bestimmte Schlüssel so zu konfigurieren, dass sie nur aus der systemeigenen Registrierung gelesen werden können, wobei die Speicherorte "Package" und "CORTANA" umgangen werden. Pass-Through-Speicherorte sind global auf dem Computer (nicht paketspezifisch) und können durch Hinzufügen des Pfads zum Schlüssel konfiguriert werden, der als Pass-Through an den **WERT REG\_MULTI\_SZ** namens **PassThroughPaths** des Schlüssels behandelt werden `HKLM\Software\Microsoft\AppV\Subsystem\VirtualRegistry` sollte. Jeder Schlüssel, der unter diesem Multizeichenfolgenwert (und deren untergeordneten Elemente) angezeigt wird, wird als Pass-Through behandelt.

Die folgenden Speicherorte sind standardmäßig als Pass-Through-Speicherorte konfiguriert:

-   HKEY\_CURRENT\_USER\\SOFTWARE\\Classes\\Local Einstellungen\\Software\\Microsoft\\Windows\\CurrentVersion\\AppModel

-   HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes\\Local Einstellungen\\Software\\Microsoft\\Windows\\CurrentVersion\\AppModel

-   HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows\\CurrentVersion\\WEINVT

-   HKEY\_LOCAL\_MACHINE\\SYSTEM\\CurrentControlSet\\services\\eventlog\\Application

-   HKEY\_LOCAL\_MACHINE\\SYSTEM\\CurrentControlSet\\Control\\WMI\\Autologger

-   HKEY\_CURRENT\_USER\\SOFTWARE\\Microsoft\\Windows\\CurrentVersion\\Internet Einstellungen

-   HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\Perflib

-   HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Policies

-   HKEY\_CURRENT\_USER\\SOFTWARE\\Policies

Der Zweck von Pass-Through-Schlüsseln besteht darin, sicherzustellen, dass eine virtuelle Anwendung keine Registrierungsdaten in die VReg schreibt, die für nicht virtuelle Anwendungen für einen erfolgreichen Vorgang oder eine erfolgreiche Integration erforderlich sind. Der Schlüssel "Richtlinien" stellt sicher, dass gruppenrichtlinienbasierte Einstellungen, die vom Administrator festgelegt wurden, verwendet werden und nicht pro Paket. Der AppModel-Schlüssel ist für die Integration in Windows Modern UI-basierten Anwendungen erforderlich. Es wird empfohlen, dass Die Verwaltungen keine der Standardmäßigen Pass-Through-Schlüssel ändern, aber in einigen Fällen kann es aufgrund des Anwendungsverhaltens erforderlich sein, zusätzliche Pass-Through-Schlüssel hinzuzufügen.

## <a name="app-v-package-store-behavior"></a><a href="" id="bkmk-pkg-store-behavior"></a>Verhalten des App-V-Paketspeichers


App-V 5 verwaltet die Paket-Store. Hierbei handelt es sich um den Speicherort, an dem die erweiterten Objektdateien aus der Appv-Datei gespeichert werden. Dieser Speicherort wird standardmäßig unter %ProgramData%\\App-V gespeichert und ist hinsichtlich der Speicherfunktionen nur durch freien Speicherplatz beschränkt. Der Paketspeicher wird nach den GUIDs für das Paket und die Version organisiert, wie im vorherigen Abschnitt erwähnt.

### <a name="add-packages"></a>Hinzufügen von Paketen

App-V-Pakete werden beim Hinzufügen zum Computer mit dem App-V-Client bereitgestellt. Der App-V-Client bietet Staging bei Bedarf. Während der Veröffentlichung oder eines manuellen Add-AppVClientPackage wird die Datenstruktur im Paketspeicher (c:\\programdata\\App-V\\{PkgGUID}\\{VerGUID}) erstellt. Die Paketdateien, die im im StreamMap.xml definierten Veröffentlichungsblock identifiziert werden, werden dem System hinzugefügt, und die Ordner der obersten Ebene und untergeordneten Dateien werden bereitgestellt, um sicherzustellen, dass beim Start die richtigen Anwendungsressourcen vorhanden sind.

### <a name="mounting-packages"></a>Montagepakete

Pakete können explizit mithilfe der PowerShell `Mount-AppVClientPackage` oder mithilfe der **App-V-Client-Benutzeroberfläche** geladen werden, um ein Paket herunterzuladen. Dieser Vorgang lädt das gesamte Paket vollständig in den Paketspeicher.

### <a name="streaming-packages"></a>Streamingpakete

Der App-V-Client kann so konfiguriert werden, dass das Standardverhalten des Streamings geändert wird. Alle Streamingrichtlinien werden unter dem folgenden Registrierungsschlüssel gespeichert: `HKEY_LOCAL_MAcHINE\Software\Microsoft\AppV\Client\Streaming` . Richtlinien werden mithilfe des PowerShell-Cmdlets `Set-AppvClientConfiguration` festgelegt. Die folgenden Richtlinien gelten für Streaming:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Richtlinie</th>
<th align="left">Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>AllowHighCostLaunch</p></td>
<td align="left"><p>Auf Windows 8 und höher ermöglicht es streaming über 3G und Mobilfunknetze</p></td>
</tr>
<tr class="even">
<td align="left"><p>Autoload</p></td>
<td align="left"><p>Gibt die Einstellung für das Laden im Hintergrund an:</p>
<p><strong>0 </strong> - Deaktiviert</p>
<p><strong>1 </strong> – Nur zuvor verwendete Pakete</p>
<p><strong>2 </strong> – Alle Pakete</p></td>
</tr>
<tr class="odd">
<td align="left"><p>PackageInstallationRoot</p></td>
<td align="left"><p>Der Stammordner für den Paketspeicher auf dem lokalen Computer</p></td>
</tr>
<tr class="even">
<td align="left"><p>PackageSourceRoot</p></td>
<td align="left"><p>Die Stammüberschreibung, von der Pakete gestreamt werden sollen</p></td>
</tr>
<tr class="odd">
<td align="left"><p>SharedContentStoreMode</p></td>
<td align="left"><p>Ermöglicht die Verwendung freigegebener Inhalte Store für VDI-Szenarien</p></td>
</tr>
</tbody>
</table>

 

 

Diese Einstellungen wirken sich auf das Verhalten des Streamings von App-V-Paketressourcen auf den Client aus. Standardmäßig lädt App-V nur die Ressourcen herunter, die nach dem Herunterladen der anfänglichen Veröffentlichungs- und primären Featureblöcke erforderlich sind. Es gibt drei spezifische Verhaltensweisen in Bezug auf Streamingpakete, die erläutert werden müssen:

-   Hintergrundstreaming

-   Optimiertes Streaming

-   Streamfehler

### <a name="background-streaming"></a>Hintergrundstreaming

Das PowerShell-Cmdlet `Get-AppvClientConfiguration` kann verwendet werden, um den aktuellen Modus für das Hintergrundstreaming mit der AutoLoad-Einstellung zu bestimmen und mit dem Cmdlet Set-AppvClientConfiguration oder über die Registrierung (HKLM\\SOFTWARE\\Microsoft\\AppV\\ClientStreaming-Schlüssel) zu ändern. Hintergrundstreaming ist eine Standardeinstellung, bei der die Einstellung für das automatische Laden so festgelegt ist, dass zuvor verwendete Pakete heruntergeladen werden. Das Verhalten basierend auf der Standardeinstellung (Wert =1) lädt App-V-Datenblöcke im Hintergrund herunter, nachdem die Anwendung gestartet wurde. Diese Einstellung kann für alle Pakete (Wert=0) insgesamt deaktiviert oder für alle Pakete aktiviert werden (Wert=2), unabhängig davon, ob sie gestartet wurden.

### <a name="optimized-streaming"></a>Optimiertes Streaming

App-V-Pakete können während der Sequenzierung mit einem primären Featureblock konfiguriert werden. Mit dieser Einstellung kann der Sequenzierungstechniker Startdateien für eine bestimmte Anwendung oder Anwendungen überwachen und die Datenblöcke im App-V-Paket für das Streaming beim ersten Start einer beliebigen Anwendung im Paket markieren.

### <a name="stream-faults"></a>Streamfehler

Nach dem anfänglichen Datenstrom von Veröffentlichungsdaten und dem primären Featureblock führen Anforderungen für zusätzliche Dateien Datenstromfehler aus. Diese Datenblöcke werden nach Bedarf in den Paketspeicher heruntergeladen. Dadurch kann ein Benutzer nur einen kleinen Teil des Pakets herunterladen, in der Regel genug, um das Paket zu starten und normale Aufgaben auszuführen. Alle anderen Blöcke werden heruntergeladen, wenn ein Benutzer einen Vorgang initiiert, der Daten erfordert, die sich derzeit nicht im Paketspeicher befinden.

Weitere Informationen zum Streaming von App-V-Paketen finden Sie unter: <https://go.microsoft.com/fwlink/?LinkId=392770> .

Sequenzierung zur Streamingoptimierung finden Sie unter: <https://go.microsoft.com/fwlink/?LinkId=392771> .

### <a name="package-upgrades"></a>Paketupgrades

App-V-Pakete müssen während des gesamten Anwendungslebenszyklus aktualisiert werden. App-V-Paketupgrades ähneln dem Paketveröffentlichungsvorgang, da jede Version an einem eigenen PackageRoot-Speicherort erstellt wird: `%ProgramData%\App-V\{PkgGUID}\{newVerGUID}` . Der Upgradevorgang wird optimiert, indem feste Links zu identischen und gestreamten Dateien aus anderen Versionen desselben Pakets erstellt werden.

### <a name="package-removal"></a>Entfernen von Paketen

Das Verhalten des App-V-Clients beim Entfernen von Paketen hängt von der Zum Entfernen verwendeten Methode ab. Unter Verwendung einer vollständigen App-V-Infrastruktur zum Aufheben der Veröffentlichung der Anwendung werden die Benutzerkatalogdateien (Computerkatalog für global veröffentlichte Anwendungen) entfernt, der Speicherort des Paketspeichers und DIEWIN-Speicherorte werden jedoch beibehalten. Wenn das `Remove-AppVClientPackge` PowerShell-Cmdlet zum Entfernen eines App-V-Pakets verwendet wird, wird der Speicherort des Paketspeichers bereinigt. Denken Sie daran, dass beim Aufheben der Veröffentlichung eines App-V-Pakets vom Verwaltungsserver kein Remove-Vorgang ausgeführt wird. Bei beiden Vorgängen werden die Paketdateien Store entfernt.

## <a name="roaming-registry-and-data"></a><a href="" id="bkmk-roaming-reg-data"></a>Roamingregistrierung und Daten


App-V 5 kann beim Roaming eine nahezu systemeigene Umgebung bereitstellen, je nachdem, wie die verwendete Anwendung geschrieben wird. Standardmäßig wird App-V appData, die am Roamingspeicherort gespeichert ist, basierend auf der Roamingkonfiguration des Betriebssystems roaminggespeichert. Andere Speicherorte für die Speicherung dateibasierter Daten werden nicht von Computer zu Computer verschoben, da sie sich an Speicherorten befinden, die nicht verschoben werden.

### <a name="roaming-requirements-and-user-catalog-data-storage"></a><a href="" id="bkmk-clt-inter-roam-reqs"></a>Roaminganforderungen und Datenspeicherung im Benutzerkatalog

App-V speichert Daten, die den Status des Katalogs des Benutzers darstellen, in Form von:

-   Dateien unter %appdata%\\Microsoft\\AppV\\Client\\Catalog

-   Registrierungseinstellungen unter `HKEY_CURRENT_USER\Software\Microsoft\AppV\Client\Packages`

Zusammen stellen diese Dateien und Registrierungseinstellungen den Katalog des Benutzers dar, sodass entweder beide verschoben werden müssen oder keines für einen bestimmten Benutzer verschoben werden muss. App-V unterstützt kein Roaming von %AppData%, aber kein Roaming des Benutzerprofils (Registrierung) oder umgekehrt.

**Hinweis:**  
Das Cmdlet **Repair-AppvClientPackage** repariert nicht den Veröffentlichungsstatus von Paketen, wobei der App-V-Status des Benutzers `HKEY_CURRENT_USER` fehlt oder mit den Daten in %appdata% nicht übereinstimmen.

 

### <a name="registry-based-data"></a>Registrierungsbasierte Daten

App-V-Registrierungsroaming fällt in zwei Szenarien, wie in der folgenden Tabelle dargestellt.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Szenario</th>
<th align="left">Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Anwendungen, die als Standardbenutzer ausgeführt werden</p></td>
<td align="left"><p>Wenn ein Standardbenutzer eine App-V-Anwendung startet, werden sowohl HKLM- als auch HKCU für App-V-Anwendungen in der HKCU-Struktur auf dem Computer gespeichert. Dies wird als zwei unterschiedliche Pfade dargestellt:</p>
<ul>
<li><p>HKLM: HKCU\SOFTWARE\Classes\AppV\Client\Packages{PkgGUID}\REGISTRY\MACHINE\SOFTWARE</p></li>
<li><p>HKCU: HKCU\SOFTWARE\Microsoft\AppV\Client\Packages{PkgGUID}\REGISTRY\USER{UserSID}\SOFTWARE</p></li>
</ul>
<p>Die Speicherorte sind basierend auf den Betriebssystemeinstellungen für Roaming aktiviert.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Anwendungen, die mit einer Erweiterung ausgeführt werden</p></td>
<td align="left"><p>Wenn eine Anwendung mit einer Erweiterung gestartet wird:</p>
<ul>
<li><p>HKLM-Daten werden in der HKLM-Struktur auf dem lokalen Computer gespeichert.</p></li>
<li><p>HKCU-Daten werden im Speicherort der Benutzerregistrierung gespeichert.</p></li>
</ul>
<p>In diesem Szenario werden diese Einstellungen nicht mit normalen Roamingkonfigurationen des Betriebssystems verschoben, und die resultierenden Registrierungsschlüssel und -werte werden an folgendem Speicherort gespeichert:</p>
<ul>
<li><p>HKLM\SOFTWARE\Microsoft\AppV\Client\Packages{PkgGUID}{UserSID}\REGISTRY\MACHINE\SOFTWARE</p></li>
<li><p>HKCU\SOFTWARE\Microsoft\AppV\Client\Packages{PkgGUID}\Registry\User{UserSID}\SOFTWARE</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

### <a name="app-v-and-folder-redirection"></a>App-V- und Ordnerumleitung

App-V 5.1 unterstützt die Ordnerumleitung des AppData-Roamingordners (%AppData%). Wenn die virtuelle Umgebung gestartet wird, wird der AppData-Roamingstatus aus dem AppData-Roamingverzeichnis des Benutzers in den lokalen Cache kopiert. Umgekehrt wird beim Herunterfahren der virtuellen Umgebung der lokale Cache, der dem AppData-Roaming eines bestimmten Benutzers zugeordnet ist, an den tatsächlichen Speicherort des AppData-Roamingverzeichnisses dieses Benutzers übertragen.

Ein typisches Paket enthält mehrere Speicherorte, die im Sicherungsspeicher des Benutzers für Einstellungen in "AppData\\Local" und "AppData\\Roaming" zugeordnet sind. Bei diesen Speicherorten handelt es sich um die Speicherorte "Kopieren bei Schreiben", die pro Benutzer im Profil des Benutzers gespeichert werden und zum Speichern von Änderungen an den VFS-Paketverzeichnissen und zum Schützen des VFS-Standardpakets verwendet werden.

In der folgenden Tabelle sind lokale und Roamingspeicherorte aufgeführt, wenn die Ordnerumleitung nicht implementiert wurde.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">VFS-Verzeichnis im Paket</th>
<th align="left">Zugeordneter Speicherort des Sicherungsspeichers</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>ProgramFilesX86</p></td>
<td align="left"><p>C:\users\jsmith\AppData &lt; strong &gt; Local </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \ProgramFilesX86</p></td>
</tr>
<tr class="even">
<td align="left"><p>SystemX86</p></td>
<td align="left"><p>C:\users\jsmith\AppData &lt; strong &gt; Local </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \SystemX86</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows</p></td>
<td align="left"><p>C:\users\jsmith\AppData &lt; strong &gt; Local </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \Windows</p></td>
</tr>
<tr class="even">
<td align="left"><p>appv_ROOT</p></td>
<td align="left"><p>C:\users\jsmith\AppData &lt; strong &gt; Local </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \appv_ROOT</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Appdata</p></td>
<td align="left"><p>C:\users\jsmith\AppData &lt; strong &gt; Roaming </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \AppData</p></td>
</tr>
</tbody>
</table>

 

 

In der folgenden Tabelle sind lokale und Roamingspeicherorte aufgeführt, wenn die Ordnerumleitung für %AppData% implementiert wurde und der Speicherort umgeleitet wurde (in der Regel an einen Netzwerkspeicherort).

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">VFS-Verzeichnis im Paket</th>
<th align="left">Zugeordneter Speicherort des Sicherungsspeichers</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>ProgramFilesX86</p></td>
<td align="left"><p>C:\users\jsmith\AppData &lt; strong &gt; Local </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \ProgramFilesX86</p></td>
</tr>
<tr class="even">
<td align="left"><p>SystemX86</p></td>
<td align="left"><p>C:\users\jsmith\AppData &lt; strong &gt; Local </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \SystemX86</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows</p></td>
<td align="left"><p>C:\users\jsmith\AppData &lt; strong &gt; Local </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \Windows</p></td>
</tr>
<tr class="even">
<td align="left"><p>appv_ROOT</p></td>
<td align="left"><p>C:\users\jsmith\AppData &lt; strong &gt; Local </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \appv_ROOT</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Appdata</p></td>
<td align="left"><p><strong>\Fileserver </strong> \users\jsmith\roaming\Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \AppData</p></td>
</tr>
</tbody>
</table>

 

 

Der aktuelle App-V-Client-VFS-Treiber kann nicht in Netzwerkspeicherorte schreiben, daher erkennt der App-V-Client das Vorhandensein der Ordnerumleitung und kopiert die Daten während der Veröffentlichung und beim Start der virtuellen Umgebung auf dem lokalen Laufwerk. Nachdem der Benutzer die App-V-Anwendung geschlossen und der App-V-Client die virtuelle Umgebung geschlossen hat, wird der lokale Speicher der VFS-AppData zurück in das Netzwerk kopiert, sodass Roaming auf zusätzlichen Computern ermöglicht wird, auf denen der Prozess wiederholt wird. Die detaillierten Schritte der Prozesse sind:

1.  Beim Starten der Veröffentlichung oder virtuellen Umgebung erkennt der App-V-Client den Speicherort des AppData-Verzeichnisses.

2.  Wenn der AppData-Roamingpfad lokal oder ino AppData\\Roaming-Speicherort zugeordnet ist, passiert nichts.

3.  Wenn der AppData-Roamingpfad nicht lokal ist, wird das VFS-AppData-Verzeichnis dem lokalen AppData-Verzeichnis zugeordnet.

Dadurch wird das Problem eines nicht lokalen %AppData%-Werts behoben, der vom App-V-Client-VFS-Treiber nicht unterstützt wird. Die an diesem neuen Speicherort gespeicherten Daten werden jedoch nicht mit der Ordnerumleitung verschoben. Alle Änderungen während der Ausführung der Anwendung erfolgen am lokalen AppData-Speicherort und müssen an den umgeleiteten Speicherort kopiert werden. Die detaillierten Schritte dieses Prozesses sind:

1.  Die App-V-Anwendung wird heruntergefahren, wodurch die virtuelle Umgebung heruntergefahren wird.

2.  Der lokale Cache des AppData-Roamingspeicherorts wird komprimiert und in einer ZIP-Datei gespeichert.

3.  Ein Zeitstempel am Ende des ZIP-Paketprozesses wird verwendet, um die Datei zu benennen.

4.  Der Zeitstempel wird in der Registrierung aufgezeichnet: HKEY\_CURRENT\_USER\\Software\\Microsoft\\AppV\\Client\\Packages\\ &lt; GUID &gt; \\AppDataTime als letzter bekannter AppData-Zeitstempel.

5.  Der Ordnerumleitungsprozess wird aufgerufen, um die ZIP-Datei auszuwerten und in das Roaming-AppData-Verzeichnis hochzuladen.

Der Zeitstempel wird verwendet, um ein Szenario vom Typ "Letzter Writer hat Vorrang" zu ermitteln, wenn ein Konflikt vorliegt, und wird verwendet, um den Download der Daten zu optimieren, wenn die App-V-Anwendung veröffentlicht oder die virtuelle Umgebung gestartet wird. Die Ordnerumleitung stellt die Daten von allen anderen Clients zur Verfügung, die von der unterstützenden Richtlinie abgedeckt werden, und initiiert den Prozess zum Speichern der AppData\\Roaming-Daten am lokalen AppData-Speicherort auf dem Client. Die detaillierten Prozesse sind:

1.  Der Benutzer startet die virtuelle Umgebung, indem er eine Anwendung startet.

2.  Die virtuelle Umgebung der Anwendung prüft, ob die aktuelle ZIP-Datei mit Zeitstempel vorhanden ist.

3.  Die Registrierung wird ggf. auf den letzten bekannten hochgeladenen Zeitstempel überprüft.

4.  Die neueste ZIP-Datei wird heruntergeladen, es sei denn, der lokale letzte bekannte Uploadzeitstempel ist größer oder gleich dem Zeitstempel aus der ZIP-Datei.

5.  Wenn der lokale letzte bekannte Uploadzeitstempel früher als der der neuesten ZIP-Datei im Roamingspeicherort von AppData ist, wird die ZIP-Datei in das lokale temporäre Verzeichnis im Profil des Benutzers extrahiert.

6.  Nachdem die ZIP-Datei erfolgreich extrahiert wurde, wird der lokale Cache des Roaming-AppData-Verzeichnisses umbenannt, und die neuen Daten werden an die stelle verschoben.

7.  Das umbenannte Verzeichnis wird gelöscht, und die Anwendung wird mit den zuletzt gespeicherten AppData-Roamingdaten geöffnet.

Dadurch wird das erfolgreiche Roaming von Anwendungseinstellungen abgeschlossen, die an AppData\\Roaming-Speicherorten vorhanden sind. Die einzige andere Bedingung, die behoben werden muss, ist ein Paketreparaturvorgang. Die Details des Prozesses sind:

1.  Ermitteln Sie während der Reparatur, ob der Pfad zum AppData-Roamingverzeichnis des Benutzers nicht lokal ist.

2.  Zuordnen der nicht lokalen AppData-Roamingpfadziele werden die erwarteten Roaming- und lokalen AppData-Speicherorte neu erstellt.

3.  Löschen Sie ggf. den in der Registrierung gespeicherten Zeitstempel.

Bei diesem Vorgang werden sowohl die lokalen als auch die Netzwerkspeicherorte für AppData neu erstellt und der Registrierungsdatensatz des Zeitstempels entfernt.

## <a name="app-v-client-application-lifecycle-management"></a><a href="" id="bkmk-clt-app-lifecycle"></a>App-V-Clientanwendungslebenszyklusverwaltung


In einer vollständigen App-V-Infrastruktur werden Anwendungen nach der Sequenzverwaltung verwaltet und über die App-V-Verwaltungs- und Veröffentlichungsserver für Benutzer oder Computer veröffentlicht. Dieser Abschnitt beschreibt die Vorgänge, die während der allgemeinen App-V-Anwendungslebenszyklusvorgänge (Hinzufügen, Veröffentlichen, Starten, Upgrade und Entfernen) auftreten, sowie die Datei- und Registrierungsspeicherorte, die aus der Perspektive des App-V-Clients geändert und geändert werden. Die App-V-Clientvorgänge werden als eine Reihe von PowerShell-Befehlen ausgeführt, die auf dem Computer mit dem App-V-Client initiiert werden.

Dieses Dokument konzentriert sich auf App-V Full Infrastructure-Lösungen. Spezifische Informationen zur App-V-Integration in Configuration Manager 2012 finden Sie unter: <https://go.microsoft.com/fwlink/?LinkId=392773> .

Die Lebenszyklusaufgaben der App-V-Anwendung werden bei der Benutzeranmeldung (Standard), beim Computerstart oder als zeitlich festgelegten Hintergrundvorgängen ausgelöst. Die Einstellungen für die App-V-Clientvorgänge, einschließlich Veröffentlichungsserver, Aktualisierungsintervalle, Aktivierung von Paketskripts und andere, werden während des Setups des Clients oder nach dem Setup mit PowerShell-Befehlen konfiguriert. Weitere Informationen finden Sie im Abschnitt "Bereitstellen des Clients" auf TechNet unter: [Bereitstellen des App-V-Clients](how-to-deploy-the-app-v-client-51gb18030.md) oder Verwenden von PowerShell:

```powershell
get-command *appv*
```

### <a name="publishing-refresh"></a>Aktualisierung der Veröffentlichung

Der Veröffentlichungsaktualisierungsprozess besteht aus mehreren kleineren Vorgängen, die auf dem App-V-Client ausgeführt werden. Da App-V eine Anwendungsvirtualisierungstechnologie und keine Aufgabenplanungstechnologie ist, wird der Windows Aufgabenplaner verwendet, um den Prozess bei der Benutzeranmeldung, beim Computerstart und in geplanten Intervallen zu aktivieren. Die Konfiguration des Clients während des oben aufgeführten Setups ist die bevorzugte Methode beim Verteilen des Clients an eine große Gruppe von Computern mit den richtigen Einstellungen. Diese Clienteinstellungen können mit den folgenden PowerShell-Cmdlets konfiguriert werden:

-   **Add-AppVPublishingServer:** Konfiguriert den Client mit einem App-V-Veröffentlichungsserver, der App-V-Pakete bereitstellt.

-   **Set-AppVPublishingServer:** Ändert die aktuellen Einstellungen für den App-V-Veröffentlichungsserver.

-   **Set-AppVClientConfiguration:** Ändert die aktuellen Einstellungen für den App-V-Client.

-   **Sync-AppVPublishingServer:** Initiiert manuell einen App-V-Veröffentlichungsaktualisierungsprozess. Dies wird auch in den geplanten Aufgaben verwendet, die während der Konfiguration des Veröffentlichungsservers erstellt wurden.

Der Schwerpunkt der folgenden Abschnitte liegt auf den Vorgängen, die während verschiedener Phasen einer App-V-Veröffentlichungsaktualisierung auftreten. Die Themen umfassen:

-   Hinzufügen eines App-V-Pakets

-   Veröffentlichen eines App-V-Pakets

### <a name="adding-an-app-v-package"></a>Hinzufügen eines App-V-Pakets

Das Hinzufügen eines App-V-Pakets zum Client ist der erste Schritt des Veröffentlichungsaktualisierungsprozesses. Das Endergebnis entspricht dem `Add-AppVClientPackage` Cmdlet in PowerShell, außer während des Veröffentlichungsaktualisierungs-Add-In-Prozesses wird der konfigurierte Veröffentlichungsserver kontaktiert und übergibt eine allgemeine Liste von Anwendungen zurück an den Client, um detailliertere Informationen abzurufen und nicht einen einzelnen Paket-Add-Vorgang. Der Vorgang wird fortgesetzt, indem der Client für Paket- oder Verbindungsgruppen-Ergänzungen oder -Updates konfiguriert wird und dann auf die Appv-Datei zugegriffen wird. Als Nächstes wird der Inhalt der Appv-Datei erweitert und auf dem lokalen Betriebssystem an den entsprechenden Speicherorten platziert. Es folgt ein detaillierter Workflow des Prozesses, vorausgesetzt, das Paket ist für Fault Streaming konfiguriert.

**So fügen Sie ein App-V-Paket hinzu**

1.  Manuelle Initiierung über PowerShell oder Tasksequenzinitiierung des Veröffentlichungsaktualisierungsprozesses.

    1.  Der App-V-Client stellt eine HTTP-Verbindung und fordert eine Liste der Anwendungen basierend auf dem Ziel an. Der Aktualisierungsprozess für die Veröffentlichung unterstützt die Ausrichtung auf Computer oder Benutzer.

    2.  Der App-V-Veröffentlichungsserver verwendet die Identität des initiierenden Ziels, Benutzers oder Computers und fragt die Datenbank nach einer Liste berechtigter Anwendungen ab. Die Liste der Anwendungen wird als XML-Antwort bereitgestellt, die der Client verwendet, um zusätzliche Anforderungen an den Server zu senden, um weitere Informationen pro Paket zu erhalten.

2.  Der Veröffentlichungs-Agent auf dem App-V-Client führt alle unten aufgeführten Aktionen serialisiert aus.

    Bewerten Sie alle Verbindungsgruppen, die unveröffentlicht oder deaktiviert sind, da Paketversionsupdates, die Teil der Verbindungsgruppe sind, nicht verarbeitet werden können.

3.  Konfigurieren Sie die Pakete durch Identifizieren eines Add- oder Update-Vorgangs.

    1.  Der App-V-Client verwendet die AppX-API aus Windows und greift über den Veröffentlichungsserver auf die AppV-Datei zu.

    2.  Die Paketdatei wird geöffnet, und die AppXManifest.xml und StreamMap.xml werden in die Paket-Store heruntergeladen.

    3.  Veröffentlichungsblockdaten, die im StreamMap.xml definiert sind, werden vollständig streamen. Speichert die Veröffentlichungsblockdaten im Paket Store\\PkgGUID\\VerGUID\\Root.

        -   Symbole: Ziele von Erweiterungspunkten.

        -   Portierbare ausführbare Header (PE-Header): Ziele von Erweiterungspunkten, die die Basisinformationen über das Image enthalten, das auf dem Datenträger benötigt wird, direkt zugänglich oder über Dateitypen.

        -   Skripts: Laden Sie das Skriptverzeichnis für die Verwendung während des gesamten Veröffentlichungsprozesses herunter.

    4.  Füllen Sie den Paketspeicher auf:

        1.  Erstellen Sie nur wenige Dateien auf dem Datenträger, die das extrahierte Paket für alle aufgeführten Verzeichnisse darstellen.

        2.  Bereitstellen von Dateien und Verzeichnissen auf oberster Ebene im Stammverzeichnis.

        3.  Alle anderen Dateien werden erstellt, wenn das Verzeichnis auf dem Datenträger als spärlich aufgeführt und bei Bedarf gestreamt wird.

    5.  Erstellen Sie die Computerkatalogeinträge. Erstellen Sie die Manifest.xml und DeploymentConfiguration.xml aus den Paketdateien (wenn keine DeploymentConfiguration.xml Datei im Paket erstellt wird).

    6.  Erstellen des Speicherorts des Paketspeichers in der Registrierung HKLM\\Software\\Microsoft\\AppV\\Client\\Packages\\PkgGUID\\Versions\\VerGUID\\Catalog

    7.  Erstellen Sie die Datei "Registry.dat" aus dem Paketspeicher in "%ProgramData%\\Microsoft\\AppV\\Client\\VReg\\{VersionGUID}.dat"

    8.  Registrieren Sie das Paket beim App-V-Kernelmodustreiber HKLM\\Microsoft\\Software\\AppV\\MAV

    9.  Aufrufen von Skripts aus der AppxManifest.xml- oder DeploymentConfig.xml datei für die Paketzufügezeit.

4.  Konfigurieren Sie Verbindungsgruppen durch Hinzufügen und Aktivieren oder Deaktivieren.

5.  Entfernen Sie Objekte, die nicht im Ziel (Benutzer oder Computer) veröffentlicht werden.

    **Hinweis:**  
    Dadurch wird kein Paket gelöscht, sondern Integrationspunkte für das spezifische Ziel (Benutzer oder Computer) entfernt und Benutzerkatalogdateien (Computerkatalogdateien für global veröffentlichte Dateien) entfernt.

     

6.  Rufen Sie die Hintergrundlast-Montage basierend auf der Clientkonfiguration auf.

7.  Pakete, die bereits über Veröffentlichungsinformationen für den Computer oder Benutzer verfügen, werden sofort wiederhergestellt.

    **Hinweis:**  
    Diese Bedingung tritt als Produkt der Entfernung auf, ohne die Veröffentlichung mit Hintergrundzufügung des Pakets aufzuheben.

     

Dadurch wird ein App-V-Paket-Add des Veröffentlichungsaktualisierungsprozesses abgeschlossen. Der nächste Schritt besteht darin, das Paket im spezifischen Ziel (Computer oder Benutzer) zu veröffentlichen.

![paketzufügen von Datei- und Registrierungsdaten.](images/packageaddfileandregistrydata.png)

### <a name="publishing-an-app-v-package"></a>Veröffentlichen eines App-V-Pakets

Während des Veröffentlichungsaktualisierungsvorgangs fügt der spezifische Veröffentlichungsvorgang (Publish-AppVClientPackage) Einträge zum Benutzerkatalog hinzu, ordnet dem Benutzer berechtigungen zu, identifiziert den lokalen Speicher und schließt alle Integrationsschritte ab. Im Folgenden finden Sie die detaillierten Schritte.

**Veröffentlichen und App-V-Paket**

1.  Paketeinträge werden dem Benutzerkatalog hinzugefügt.

    1.  Benutzerorientierte Pakete: die UserDeploymentConfiguration.xml und UserManifest.xml werden auf dem Computer im Benutzerkatalog platziert.

    2.  Computerorientierte (globale) Pakete: die UserDeploymentConfiguration.xml wird im Computerkatalog platziert

2.  Registrieren des Pakets beim Kernelmodustreiber für den Benutzer unter HKLM\\Software\\Microsoft\\AppV\\MAV

3.  Ausführen von Integrationsaufgaben.

    1.  Erstellen Sie Erweiterungspunkte.

    2.  Store Sicherungsinformationen im Registrierungs- und Roamingprofil des Benutzers (Verknüpfungssicherungen).

        **Hinweis:**  
        Dadurch werden Erweiterungspunkte wiederhergestellt, wenn das Paket unveröffentlicht ist.

         

    3.  Führen Sie Skripts aus, die für die Veröffentlichungszeit vorgesehen sind.

Das Veröffentlichen eines App-V-Pakets, das Teil einer Verbindungsgruppe ist, ähnelt dem oben genannten Prozess. Für Verbindungsgruppen enthält der Pfad, in dem die spezifischen Kataloginformationen gespeichert werden, PackageGroups als untergeordnetes Element des Katalogverzeichnisses. Weitere Informationen finden Sie oben im Computer- und Benutzerkatalog.

![Paket Hinzufügen von Datei- und Registrierungsdaten – global.](images/packageaddfileandregistrydata-global.png)

### <a name="application-launch"></a>Starten der Anwendung

Nach der Veröffentlichungsaktualisierung startet der Benutzer eine App-V-Anwendung und startet sie anschließend erneut. Der Prozess ist sehr einfach und für den schnellen Start mit einem Minimum an Netzwerkdatenverkehr optimiert. Der App-V-Client überprüft den Pfad zum Benutzerkatalog auf Dateien, die während der Veröffentlichung erstellt wurden. Nachdem Berechtigungen zum Starten des Pakets eingerichtet wurden, erstellt der App-V-Client eine virtuelle Umgebung, beginnt mit dem Streamen aller erforderlichen Daten und wendet die entsprechenden Manifest- und Bereitstellungskonfigurationsdateien während der Erstellung der virtuellen Umgebung an. Nachdem die virtuelle Umgebung für das jeweilige Paket und die Anwendung erstellt und konfiguriert wurde, wird die Anwendung gestartet.

**So starten Sie App-V-Anwendungen**

1.  Der Benutzer startet die Anwendung, indem er auf einen Verknüpfungs- oder Dateitypaufruf klickt.

2.  Der App-V-Client überprüft das Vorhandensein im Benutzerkatalog für die folgenden Dateien.

    -   UserDeploymentConfiguration.xml

    -   UserManifest.xml

3.  Wenn die Dateien vorhanden sind, ist die Anwendung für diesen bestimmten Benutzer berechtigt, und die Anwendung startet den Startvorgang. Zu diesem Zeitpunkt ist kein Netzwerkdatenverkehr vorhanden.

4.  Als Nächstes überprüft der App-V-Client, ob der Pfad für das für den App-V-Clientdienst registrierte Paket in der Registrierung gefunden wird.

5.  Nach dem Suchen des Pfads zum Paketspeicher wird die virtuelle Umgebung erstellt. Wenn dies der erste Start ist, wird der primäre Featureblock heruntergeladen, sofern vorhanden.

6.  Nach dem Herunterladen verwendet der App-V-Clientdienst die Manifest- und Bereitstellungskonfigurationsdateien, um die virtuelle Umgebung zu konfigurieren, und alle App-V-Subsysteme werden geladen.

7.  Die Anwendung wird gestartet. Bei fehlenden Dateien im Paketspeicher (spärliche Dateien) streamt App-V die Dateien bei Bedarf.

    ![Paket Hinzufügen von Datei- und Registrierungsdaten – Datenstrom.](images/packageaddfileandregistrydata-stream.png)

### <a name="upgrading-an-app-v-package"></a>Aktualisieren eines App-V-Pakets

Der App-V 5-Paketupgradeprozess unterscheidet sich von den älteren Versionen von App-V. App-V unterstützt mehrere Versionen desselben Pakets auf einem Computer, der für unterschiedliche Benutzer berechtigt ist. Paketversionen können jederzeit hinzugefügt werden, wenn der Paketspeicher und Kataloge mit den neuen Ressourcen aktualisiert werden. Der einzige spezifische Prozess für das Hinzufügen neuer Versionsressourcen ist die Speicheroptimierung. Während eines Upgrades werden nur die neuen Dateien zum speicherort der neuen Version hinzugefügt, und hardlinks werden für unveränderte Dateien erstellt. Dadurch wird der Gesamtspeicher reduziert, indem die Datei nur an einem Datenträgerspeicherort dargestellt und dann in alle Ordner mit einem Dateispeicherorteintrag auf dem Datenträger projiziert wird. Die spezifischen Details zum Aktualisieren eines App-V-Pakets sind wie folgt:

**So aktualisieren Sie ein App-V-Paket**

1.  Der App-V-Client führt eine Veröffentlichungsaktualisierung durch und ermittelt eine neuere Version eines App-V-Pakets.

2.  Paketeinträge werden dem entsprechenden Katalog für die neue Version hinzugefügt.

    1.  Benutzerorientierte Pakete: die UserDeploymentConfiguration.xml und UserManifest.xml werden auf dem Computer im Benutzerkatalog unter "appdata\\roaming\\Microsoft\\AppV\\Client\\Catalog\\Packages\\PkgGUID\\VerGUID" platziert.

    2.  Computerorientierte (globale) Pakete: die UserDeploymentConfiguration.xml wird im Computerkatalog unter %programdata%\\Microsoft\\AppV\\Client\\Catalog\\Packages\\PkgGUID\\VerGUID platziert.

3.  Registrieren des Pakets beim Kernelmodustreiber für den Benutzer unter HKLM\\Software\\Microsoft\\AppV\\MAV

4.  Ausführen von Integrationsaufgaben.

    -   Integrieren Sie Erweiterungspunkte (EP) aus den Manifestdateien und dynamischen Konfigurationsdateien.

    1.  Dateibasierte EP-Daten werden im Ordner "AppData" unter Verwendung von Verknüpfungspunkten aus dem Paketspeicher gespeichert.

    2.  EPs der Version 1 sind bereits vorhanden, wenn eine neue Version verfügbar wird.

    3.  Die Erweiterungspunkte werden auf den Speicherort der Version 2 in Computer- oder Benutzerkatalogen für neuere oder aktualisierte Erweiterungspunkte umgestellt.

5.  Führen Sie Skripts aus, die für die Veröffentlichungszeit vorgesehen sind.

6.  Installieren Sie bei Bedarf Assemblys nebeneinander.

### <a name="upgrading-an-in-use-app-v-package"></a>Aktualisieren eines verwendeten App-V-Pakets

**Ab App-V 5 SP2:** Wenn Sie versuchen, ein Paket zu aktualisieren, das von einem Endbenutzer verwendet wird, wird die Upgradeaufgabe in den Status "Ausstehend" versetzt. Das Upgrade wird später gemäß den folgenden Regeln ausgeführt:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Art der Hintergrundaufgabe</th>
<th align="left">Anwendbare Regel</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Benutzerbasierte Aufgabe, z. B. veröffentlichen eines Pakets für einen Benutzer</p></td>
<td align="left"><p>Die ausstehende Aufgabe wird ausgeführt, nachdem sich der Benutzer abgemeldet und dann wieder angemeldet hat.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Global basierte Aufgabe, z. B. globales Aktivieren einer Verbindungsgruppe</p></td>
<td align="left"><p>Die ausstehende Aufgabe wird ausgeführt, wenn der Computer heruntergefahren und dann neu gestartet wird.</p></td>
</tr>
</tbody>
</table>

 

Wenn eine Aufgabe in den Zustand "Ausstehend" versetzt wird, generiert der App-V-Client wie folgt auch einen Registrierungsschlüssel für die ausstehende Aufgabe:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Benutzerbasierte oder global basierte Aufgabe</th>
<th align="left">Wo der Registrierungsschlüssel generiert wird</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Benutzerbasierte Aufgaben</p></td>
<td align="left"><p>KEY_CURRENT_USER\Software\Microsoft\AppV\Client\PendingTasks</p></td>
</tr>
<tr class="even">
<td align="left"><p>Global basierte Aufgaben</p></td>
<td align="left"><p>HKEY_LOCAL_MACHINE\Software\Microsoft\AppV\Client\PendingTasks</p></td>
</tr>
</tbody>
</table>

 

Die folgenden Vorgänge müssen abgeschlossen sein, bevor Benutzer die neuere Version des Pakets verwenden können:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Aufgabe</th>
<th align="left">Details</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Hinzufügen des Pakets zum Computer</p></td>
<td align="left"><p>Diese Aufgabe ist computerspezifisch, und Sie können sie jederzeit ausführen, indem Sie die Schritte im Abschnitt "Paket hinzufügen" oben ausführen.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Veröffentlichen des Pakets</p></td>
<td align="left"><p>Schritte finden Sie oben im Abschnitt "Paketveröffentlichung". Für diesen Prozess müssen Sie Erweiterungspunkte auf dem System aktualisieren. Endbenutzer können die Anwendung nicht verwenden, wenn Sie diese Aufgabe ausführen.</p></td>
</tr>
</tbody>
</table>

 

Verwenden Sie die folgenden Beispielszenarien als Leitfaden zum Aktualisieren von Paketen.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Szenario</th>
<th align="left">Anforderungen</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>App-V-Paket wird beim Upgrade nicht verwendet</p></td>
<td align="left"><p>Keine der folgenden Komponenten des Pakets kann verwendet werden: virtuelle Anwendung, COM-Server oder Shell-Erweiterungen.</p>
<p>Der Administrator veröffentlicht eine neuere Version des Pakets, und das Upgrade funktioniert beim nächsten Start einer Komponente oder Anwendung innerhalb des Pakets. Die neue Version des Pakets wird gestreamt und ausgeführt. In diesem Szenario in App-V 5 SP2 hat sich gegenüber früheren Versionen von App-V 5 nichts geändert.</p></td>
</tr>
<tr class="even">
<td align="left"><p>App-V-Paket wird verwendet, wenn der Administrator eine neuere Version des Pakets veröffentlicht</p></td>
<td align="left"><p>Der Upgradevorgang wird vom App-V-Client auf "Ausstehend" festgelegt, d. h., er wird in die Warteschlange eingereiht und später ausgeführt, wenn das Paket nicht verwendet wird.</p>
<p>Wenn die Paketanwendung verwendet wird, beendet der Benutzer die virtuelle Anwendung, nach der das Upgrade erfolgen kann.</p>
<p>Wenn das Paket Shellerweiterungen (Office 2013) aufweist, die dauerhaft von Windows Explorer geladen werden, kann der Benutzer nicht angemeldet werden. Benutzer müssen sich abmelden und sich erneut anmelden, um das App-V-Paketupgrade zu initiieren.</p></td>
</tr>
</tbody>
</table>

 

### <a name="global-vs-user-publishing"></a>Globale Veröffentlichung im Vergleich zur Veröffentlichung durch Benutzer

App-V-Pakete können auf zwei Arten veröffentlicht werden: Benutzer, der ein App-V-Paket an einen bestimmten Benutzer oder eine Gruppe von Benutzern ausgibt, und global, wodurch das App-V-Paket für alle Benutzer des Computers auf dem gesamten Computer bereitgestellt wird. Nachdem ein Paketupgrade erstellt wurde und das App-V-Paket nicht verwendet wird, sollten Sie die beiden Arten der Veröffentlichung in Betracht ziehen:

-   **Global veröffentlicht:** Die Anwendung wird auf einem Computer veröffentlicht; Alle Benutzer auf diesem Computer können es verwenden. Das Upgrade erfolgt, wenn der App-V-Clientdienst gestartet wird. Dies bedeutet, dass ein Computer neu gestartet wird.

-   **Benutzer veröffentlicht:** Die Anwendung wird für einen Benutzer veröffentlicht. Wenn mehrere Benutzer auf dem Computer vorhanden sind, kann die Anwendung für eine Teilmenge der Benutzer veröffentlicht werden. Das Upgrade erfolgt, wenn sich der Benutzer anmeldet oder erneut veröffentlicht wird (in regelmäßigen Abständen, Aktualisierung und Auswertung der ConfigMgr-Richtlinie, regelmäßige Veröffentlichung/Aktualisierung von App-V oder explizit über PowerShell-Befehle).

### <a name="removing-an-app-v-package"></a>Entfernen eines App-V-Pakets

Das Entfernen von App-V-Anwendungen in einer vollständigen Infrastruktur ist ein Unveröffentlichter Vorgang und führt keine Paketentfernung durch. Der Vorgang ist identisch mit dem Veröffentlichungsprozess oben, aber anstatt den Entfernungsprozess hinzuzufügen, werden die Änderungen rückgängig gemacht, die für App-V-Pakete vorgenommen wurden.

### <a name="repairing-an-app-v-package"></a>Reparieren eines App-V-Pakets

Der Reparaturvorgang ist sehr einfach, kann sich jedoch auf viele Positionen auf dem Computer auswirken. Die zuvor erwähnten SPEICHERORTE (Copy on Write) werden entfernt, und Erweiterungspunkte werden deintegriert und dann erneut integriert. Überprüfen Sie die SPEICHERORTE für DIE PLATZIERUNG VON DATEN, indem Sie überprüfen, wo sie in der Registrierung registriert sind. Dieser Vorgang wird automatisch ausgeführt, und es gibt keine andere administrative Kontrolle als das Initiieren eines Reparaturvorgangs über die App-V-Clientkonsole oder über PowerShell (Repair-AppVClientPackage).

## <a name="integration-of-app-v-packages"></a><a href="" id="bkmk-integr-appv-pkgs"></a>Integration von App-V-Paketen


Der App-V-Client und die Paketarchitektur bieten eine spezifische Integration in das lokale Betriebssystem während des Hinzufügens und Veröffentlichens von Paketen. Drei Dateien definieren die Integrations- oder Erweiterungspunkte für ein App-V-Paket:

-   AppXManifest.xml: Gespeichert innerhalb des Pakets mit Fallbackkopien, die im Paketspeicher und im Benutzerprofil gespeichert sind. Enthält die Optionen, die während des Sequenzierungsprozesses erstellt wurden.

-   DeploymentConfig.xml: Stellt Konfigurationsinformationen von computer- und benutzerbasierten Integrationserweiterungspunkten bereit.

-   UserConfig.xml: Eine Teilmenge der Deploymentconfig.xml, die nur benutzerbasierte Konfigurationen bereitstellt und nur auf benutzerbasierte Erweiterungspunkte ausgerichtet ist.

### <a name="rules-of-integration"></a>Integrationsregeln

Wenn App-V-Anwendungen auf einem Computer mit dem App-V-Client veröffentlicht werden, werden einige spezifische Aktionen ausgeführt, wie in der folgenden Liste beschrieben:

-   Globale Veröffentlichung: Verknüpfungen werden am Profilspeicherort "Alle Benutzer" und andere Erweiterungspunkte in der Registrierung in der HKLM-Struktur gespeichert.

-   Benutzerveröffentlichung: Verknüpfungen werden im aktuellen Benutzerkontoprofil und andere Erweiterungspunkte in der Registrierung in der HKCU-Struktur gespeichert.

-   Sicherung und Wiederherstellung: Vorhandene systemeigene Anwendungsdaten und Registrierungen (z. B. FTA-Registrierungen) werden während der Veröffentlichung gesichert.

    1.  App-V-Pakete erhalten den Besitz basierend auf dem letzten integrierten Paket, bei dem der Besitz an die neueste veröffentlichte App-V-Anwendung übergeben wird.

    2.  Besitzübertragungen von einem App-V-Paket zu einem anderen, wenn das besitzende App-V-Paket unveröffentlicht wird. Dadurch wird keine Wiederherstellung der Daten oder der Registrierung initiiert.

    3.  Stellen Sie die gesicherten Daten wieder her, wenn das letzte Paket unveröffentlicht oder pro Erweiterungspunkt entfernt wurde.

### <a name="extension-points"></a>Erweiterungspunkte

Die App-V-Veröffentlichungsdateien (Manifest und dynamische Konfiguration) bieten mehrere Erweiterungspunkte, mit denen die Anwendung in das lokale Betriebssystem integriert werden kann. Diese Erweiterungspunkte führen typische Anwendungsinstallationsaufgaben durch, z. B. das Platzieren von Verknüpfungen, das Erstellen von Dateitypzuordnungen und das Registrieren von Komponenten. Da es sich hierbei um virtualisierte Anwendungen handelt, die nicht auf die gleiche Weise wie eine herkömmliche Anwendung installiert werden, gibt es einige Unterschiede. Nachfolgend finden Sie eine Liste der Erweiterungspunkte, die in diesem Abschnitt behandelt werden:

-   Tastenkombinationen

-   Dateitypzuordnungen

-   Shell-Erweiterungen

-   COM

-   Softwareclients

-   Anwendungsfunktionen

-   URL-Protokollhandler

-   AppPath

-   Virtuelle Anwendung

### <a name="shortcuts"></a>Tastenkombinationen

Die Abkürzung ist eines der grundlegenden Elemente der Integration in das Betriebssystem und die Schnittstelle für den direkten Benutzerstart einer App-V-Anwendung. Während der Veröffentlichung und Aufhebung der Veröffentlichung von App-V-Anwendungen.

Aus dem Paketmanifest und den XML-Dateien der dynamischen Konfiguration kann der Pfad zu einer bestimmten ausführbaren Anwendung in einem Abschnitt wie dem folgenden gefunden werden:

```xml
<Extension Category="AppV.Shortcut">
          <Shortcut>
            <File>[{Common Desktop}]\Adobe Reader 9.lnk</File>
            <Target>[{AppVPackageRoot}]\Reader\AcroRd32.exe</Target>
            <Icon>[{Windows}]\Installer\{AC76BA86-7AD7-1033-7B44-A94000000001}\SC_Reader.ico</Icon>
            <Arguments />
            <WorkingDirectory />
            <ShowCommand>1</ShowCommand>
            <ApplicationId>[{AppVPackageRoot}]\Reader\AcroRd32.exe</ApplicationId>
          </Shortcut>
        </Extension>
```

Wie bereits erwähnt, werden die App-V-Verknüpfungen basierend auf dem Aktualisierungsvorgang standardmäßig im Profil des Benutzers platziert. Die globale Aktualisierung platziert Verknüpfungen im Profil "Alle Benutzer", und die Benutzeraktualisierung speichert sie im Profil des jeweiligen Benutzers. Die eigentliche ausführbare Datei wird im Paket-Store gespeichert. Der Speicherort der ICO-Datei ist ein tokenisierter Speicherort im App-V-Paket.

### <a name="file-type-associations"></a>Dateitypzuordnungen

Der App-V-Client verwaltet die Dateitypzuordnungen des lokalen Betriebssystems während der Veröffentlichung, sodass Benutzer Dateitypaufrufe verwenden oder eine Datei mit einer speziell registrierten Erweiterung (.docx) öffnen können, um eine App-V-Anwendung zu starten. Dateitypzuordnungen sind in den Manifestdateien und dynamischen Konfigurationsdateien vorhanden, wie im folgenden Beispiel dargestellt:

```xml
<Extension Category="AppV.FileTypeAssociation">
          <FileTypeAssociation>
            <FileExtension MimeAssociation="true">
              <Name>.xdp</Name>
              <ProgId>AcroExch.XDPDoc</ProgId>
              <ContentType>application/vnd.adobe.xdp+xml</ContentType>
            </FileExtension>
            <ProgId>
              <Name>AcroExch.XDPDoc</Name>
              <Description>Adobe Acrobat XML Data Package File</Description>
              <EditFlags>65536</EditFlags>
              <DefaultIcon>[{Windows}]\Installer\{AC76BA86-7AD7-1033-7B44-A94000000001}\XDPFile_8.ico</DefaultIcon>
              <ShellCommands>
                <DefaultCommand>Read</DefaultCommand>
                <ShellCommand>
                  <ApplicationId>[{AppVPackageRoot}]\Reader\AcroRd32.exe</ApplicationId>
                  <Name>Open</Name>
                  <CommandLine>"[{AppVPackageRoot}]\Reader\AcroRd32.exe" "%1"</CommandLine>
                </ShellCommand>
                <ShellCommand>
                  <ApplicationId>[{AppVPackageRoot}]\Reader\AcroRd32.exe</ApplicationId>
                  <Name>Printto</Name>
                  <CommandLine>"[{AppVPackageRoot}]\Reader\AcroRd32.exe"  /t "%1" "%2" "%3" "%4"</CommandLine>
                </ShellCommand>
                <ShellCommand>
                  <ApplicationId>[{AppVPackageRoot}]\Reader\AcroRd32.exe</ApplicationId>
                  <Name>Read</Name>
                  <FriendlyName>Open with Adobe Reader 9</FriendlyName>
                  <CommandLine>"[{AppVPackageRoot}]\Reader\AcroRd32.exe" "%1"</CommandLine>
                </ShellCommand>
              </ShellCommands>
            </ProgId>
          </FileTypeAssociation>
        </Extension>
```

**Hinweis:**  
Für dieses Beispiel gilt Folgendes:

-   `<Name>.xdp</Name>` ist die Erweiterung

-   `<Name>AcroExch.XDPDoc</Name>` ist der ProgId-Wert (der auf die angrenzende ProgId verweist)

-   `<CommandLine>"[{AppVPackageRoot}]\Reader\AcroRd32.exe" "%1"</CommandLine>` ist die Befehlszeile, die auf die ausführbare Datei der Anwendung verweist

 

### <a name="shell-extensions"></a>-Shell-Erweiterungen

Shell-Erweiterungen werden während des Sequenzierungsprozesses automatisch in das Paket eingebettet. Wenn das Paket global veröffentlicht wird, bietet die Shellerweiterung Benutzern die gleiche Funktionalität, als ob die Anwendung lokal installiert wäre. Die Anwendung erfordert keine zusätzliche Einrichtung oder Konfiguration auf dem Client, um die Shell-Erweiterungsfunktionalität zu aktivieren.

**Anforderungen für die Verwendung von Shell-Erweiterungen:**

-   Pakete, die eingebettete Shellerweiterungen enthalten, müssen global veröffentlicht werden.

-   Die Bitanzahl der Anwendung, sequencer und des App-V-Clients muss übereinstimmen, andernfalls funktionieren die Shell-Erweiterungen nicht. Zum Beispiel:

    -   Die Version der Anwendung ist 64-Bit.

    -   Der Sequencer wird auf einem 64-Bit-Computer ausgeführt.

    -   Das Paket wird an einen 64-Bit-App-V-Clientcomputer übermittelt.

In der folgenden Tabelle werden die unterstützten Shellerweiterungen angezeigt.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Handler</th>
<th align="left">Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Kontextmenühandler</p></td>
<td align="left"><p>Fügt dem Kontextmenü Menüelemente hinzu. Er wird aufgerufen, bevor das Kontextmenü angezeigt wird.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Drag & Drop-Handler</p></td>
<td align="left"><p>Steuert die Aktion beim Klicken per Drag & Drop mit der rechten Maustaste und ändert das angezeigte Kontextmenü.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Drop-Zielhandler</p></td>
<td align="left"><p>Steuert die Aktion, nachdem ein Datenobjekt über ein Drop-Ziel wie eine Datei gezogen und abgelegt wurde.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Datenobjekthandler</p></td>
<td align="left"><p>Steuert die Aktion, nachdem eine Datei in die Zwischenablage kopiert oder über ein Drop-Ziel gezogen und abgelegt wurde. Es kann zusätzliche Zwischenablageformate für das Dropziel bereitstellen.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Eigenschaftenblatthandler</p></td>
<td align="left"><p>Ersetzt oder fügt Dem Eigenschaftenfenster-Dialogfeld eines Objekts Seiten hinzu.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Infotip-Handler</p></td>
<td align="left"><p>Ermöglicht das Abrufen von Flags und Infotip-Informationen für ein Element und das Anzeigen in einer Popup-QuickInfo beim Mauszeigen.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Spaltenhandler</p></td>
<td align="left"><p>Ermöglicht das Erstellen und Anzeigen benutzerdefinierter Spalten in Windows <em> Explorer-Detailansicht. </em> Es kann verwendet werden, um die Sortierung und Gruppierung zu erweitern.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Vorschauhandler</p></td>
<td align="left"><p>Ermöglicht die Anzeige einer Vorschau einer Datei im Windows Explorer-Vorschaubereich.</p></td>
</tr>
</tbody>
</table>

 

### <a name="com"></a>COM

Der App-V-Client unterstützt Veröffentlichungsanwendungen mit Unterstützung für COM-Integration und Virtualisierung. Die COM-Integration ermöglicht dem App-V-Client das Registrieren von COM-Objekten im lokalen Betriebssystem und die Virtualisierung der Objekte. Für die Zwecke dieses Dokuments erfordert die Integration von COM-Objekten zusätzliche Details.

App-V unterstützt das Registrieren von COM-Objekten aus dem Paket beim lokalen Betriebssystem mit zwei Prozesstypen: Out-of-Process und In-Process. Das Registrieren von COM-Objekten erfolgt mit einem oder einer Kombination aus mehreren Betriebsmodi für ein bestimmtes App-V-Paket, das ausgeschaltet, isoliert und integriert ist. Der integrierte Modus ist für den Out-of-Process- oder In-Process-Typ konfiguriert. Die Konfiguration von COM-Modi und -Typen erfolgt mit dynamischen Konfigurationsdateien (deploymentconfig.xml oder userconfig.xml).

Details zur App-V-Integration finden Sie unter: <https://go.microsoft.com/fwlink/?LinkId=392834> .

### <a name="software-clients-and-application-capabilities"></a>Softwareclients und Anwendungsfunktionen

App-V unterstützt bestimmte Softwareclients und Anwendungsfunktionalitätserweiterungspunkte, mit denen virtualisierte Anwendungen beim Softwareclient des Betriebssystems registriert werden können. Dadurch können Benutzer Standardprogramme für Vorgänge wie E-Mail, Chat und Media Player auswählen. Dieser Vorgang wird in der Systemsteuerung mit "Programmzugriff festlegen" und "Computerstandardeinstellungen" ausgeführt und während der Sequenzierung in den Manifestdateien oder dynamischen Konfigurationsdateien konfiguriert. Anwendungsfunktionen werden nur unterstützt, wenn die App-V-Anwendungen global veröffentlicht werden.

Beispiel für die Softwareclientregistrierung eines App-V-basierten Mailclients.

```xml
    <SoftwareClients Enabled="true">
      <ClientConfiguration EmailEnabled="true" />
      <Extensions>
        <Extension Category="AppV.SoftwareClient">
          <SoftwareClients>
            <EMail MakeDefault="true">
              <Name>Mozilla Thunderbird</Name>
              <Description>Mozilla Thunderbird</Description>
              <DefaultIcon>[{ProgramFilesX86}]\Mozilla Thunderbird\thunderbird.exe,0</DefaultIcon>
              <InstallationInformation>
                <RegistrationCommands>
                  <Reinstall>"[{ProgramFilesX86}]\Mozilla Thunderbird\uninstall\helper.exe" /SetAsDefaultAppGlobal</Reinstall>
                  <HideIcons>"[{ProgramFilesX86}]\Mozilla Thunderbird\uninstall\helper.exe" /HideShortcuts</HideIcons>
                  <ShowIcons>"[{ProgramFilesX86}]\Mozilla Thunderbird\uninstall\helper.exe" /ShowShortcuts</ShowIcons>
                </RegistrationCommands>
                <IconsVisible>1</IconsVisible>
                <OEMSettings />
              </InstallationInformation>
              <ShellCommands>
                <ApplicationId>[{ProgramFilesX86}]\Mozilla Thunderbird\thunderbird.exe</ApplicationId>
                <Open>"[{ProgramFilesX86}]\Mozilla Thunderbird\thunderbird.exe" -mail</Open>
              </ShellCommands>
              <MAPILibrary>[{ProgramFilesX86}]\Mozilla Thunderbird\mozMapi32_InUse.dll</MAPILibrary>
              <MailToProtocol>
                <Description>Thunderbird URL</Description>
                <EditFlags>2</EditFlags>
                <DefaultIcon>[{ProgramFilesX86}]\Mozilla Thunderbird\thunderbird.exe,0</DefaultIcon>
                <ShellCommands>
                  <ApplicationId>[{ProgramFilesX86}]\Mozilla Thunderbird\thunderbird.exe</ApplicationId>
                  <Open>"[{ProgramFilesX86}]\Mozilla Thunderbird\thunderbird.exe" -osint -compose "%1"</Open>
                </ShellCommands>
              </MailToProtocol>
            </EMail>
          </SoftwareClients>
        </Extension>
      </Extensions>
    </SoftwareClients>
```

**Hinweis:**  
Für dieses Beispiel gilt Folgendes:

-   `<ClientConfiguration EmailEnabled="true" />` ist die allgemeine Einstellung für Softwareclients zum Integrieren von E-Mail-Clients

-   `<EMail MakeDefault="true">` ist das Flag, um einen bestimmten E-Mail-Client als Standard-E-Mail-Client festzulegen.

-   `<MAPILibrary>[{ProgramFilesX86}]\Mozilla Thunderbird\mozMapi32_InUse.dll</MAPILibrary>` ist die MAPI-DLL-Registrierung

 

### <a name="url-protocol-handler"></a>URL-Protokollhandler

Anwendungen werden nicht immer spezifisch als virtualisierte Anwendungen bezeichnet, die einen Dateitypaufruf verwenden. Beispielsweise klickt der Benutzer in einer Anwendung, die das Einbetten eines Mailto:-Links in ein Dokument oder eine Webseite unterstützt, auf einen Mailto:-Link und erwartet, dass er den registrierten E-Mail-Client abruft. App-V unterstützt URL-Protokollhandler, die pro Paket mit dem lokalen Betriebssystem registriert werden können. Während der Sequenzierung werden die URL-Protokollhandler automatisch zum Paket hinzugefügt.

In Situationen, in denen mehrere Anwendungen vorhanden sind, die den spezifischen URL-Protokollhandler registrieren können, können die dynamischen Konfigurationsdateien verwendet werden, um das Verhalten zu ändern und dieses Feature für eine Anwendung zu unterdrücken oder zu deaktivieren, die nicht die primäre gestartete Anwendung sein sollte.

### <a name="apppath"></a>AppPath

Der AppPath-Erweiterungspunkt unterstützt das direkte Aufrufen von App-V-Anwendungen über das Betriebssystem. Dies erfolgt in der Regel über den Start- oder Ausführungsbildschirm, je nach Betriebssystem, wodurch Administratoren über Betriebssystembefehle oder Skripts Zugriff auf App-V-Anwendungen gewähren können, ohne den spezifischen Pfad zur ausführbaren Datei aufzurufen. Es wird daher vermieden, die Systempfad-Umgebungsvariable auf allen Systemen zu ändern, da sie während der Veröffentlichung erreicht wird.

Der AppPath-Erweiterungspunkt wird entweder im Manifest oder in den dynamischen Konfigurationsdateien konfiguriert und während der Veröffentlichung für den Benutzer in der Registrierung auf dem lokalen Computer gespeichert. Weitere Informationen zu AppPath finden Sie unter: <https://go.microsoft.com/fwlink/?LinkId=392835> .

### <a name="virtual-application"></a>Virtuelle Anwendung

Dieses Subsystem enthält eine Liste der Anwendungen, die während der Sequenzierung erfasst werden und in der Regel von anderen App-V-Komponenten genutzt werden. Die Integration von Erweiterungspunkten, die zu einer bestimmten Anwendung gehören, kann mithilfe dynamischer Konfigurationsdateien deaktiviert werden. Wenn ein Paket beispielsweise zwei Anwendungen enthält, ist es möglich, alle Erweiterungspunkte zu deaktivieren, die zu einer Anwendung gehören, um nur die Integration von Erweiterungspunkten einer anderen Anwendung zu ermöglichen.

### <a name="extension-point-rules"></a>Erweiterungspunktregeln

Die oben beschriebenen Erweiterungspunkte sind basierend auf der Veröffentlichung der Pakete in das Betriebssystem integriert. Globale Veröffentlichung platziert Erweiterungspunkte an öffentlichen Computerspeicherorten, an denen Benutzerveröffentlichung Erweiterungspunkte an Benutzerspeicherorten platziert. Beispielsweise führt eine Verknüpfung, die auf dem Desktop erstellt und global veröffentlicht wird, zu den Dateidaten für die Verknüpfung (%Public%\\Desktop) und den Registrierungsdaten (HKLM\\Software\\Classes). Dieselbe Verknüpfung würde Dateidaten (%UserProfile%\\Desktop) und Registrierungsdaten (HKCU\\Software\\Classes) aufweisen.

Erweiterungspunkte werden nicht alle auf die gleiche Weise veröffentlicht, wobei einige Erweiterungspunkte eine globale Veröffentlichung erfordern und andere Sequenzierung auf dem spezifischen Betriebssystem und der Architektur, in der sie bereitgestellt werden, erforderlich sind. Nachfolgend finden Sie eine Tabelle, in der diese beiden wichtigsten Regeln beschrieben werden.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Virtuelle Erweiterung</th>
<th align="left">Erfordert die Zielbetriebssystemsequenzierung</th>
<th align="left">Erfordert globale Veröffentlichung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Tastenkombination</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Dateitypzuordnung</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>URL-Protokolle</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>AppPaths</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>COM-Modus</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Softwareclient</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Anwendungsfunktionen</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p>X</p></td>
</tr>
<tr class="even">
<td align="left"><p>Kontextmenühandler</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p>X</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Drag & Drop-Handler</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Data-Objekthandler</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Eigenschaftenblatthandler</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Infotip-Handler</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Spaltenhandler</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Shell-Erweiterungen</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Browserhilfsobjekt</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p>X</p></td>
</tr>
<tr class="even">
<td align="left"><p>Active X-Objekt</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p>X</p></td>
</tr>
</tbody>
</table>

 

## <a name="dynamic-configuration-processing"></a><a href="" id="bkmk-dynamic-config"></a>Dynamische Konfigurationsverarbeitung


Das Bereitstellen von App-V-Paketen auf einem Computer oder Benutzer ist sehr einfach. Da Organisationen AppV-Anwendungen jedoch über Geschäftsbereiche und geografische und politische Grenzen hinweg bereitstellen, ist die Möglichkeit, eine Anwendung einmal mit einer Reihe von Einstellungen abzufolgen, unmöglich. App-V wurde für dieses Szenario entwickelt, da es bestimmte Einstellungen und Konfigurationen während der Sequenzierung in der Manifestdatei erfasst, aber auch Änderungen mit Dynamischen Konfigurationsdateien unterstützt.

Die dynamische App-V-Konfiguration ermöglicht das Angeben einer Richtlinie für ein Paket auf Computerebene oder auf Benutzerebene. Die Dynamic Configuration-Dateien ermöglichen Sequenzierungstechnikern das Ändern der Konfiguration eines Pakets nach der Sequenzierung, um die Anforderungen einzelner Benutzergruppen oder Computer zu erfüllen. In einigen Fällen kann es erforderlich sein, Änderungen an der Anwendung vorzunehmen, um die richtigen Funktionen in der App-V-Umgebung bereitzustellen. Beispielsweise kann es erforderlich sein, Änderungen an den \_\*-config.xml-Dateien vorzunehmen, damit bestimmte Aktionen zu einem bestimmten Zeitpunkt während der Ausführung der Anwendung ausgeführt werden können, z. B. das Deaktivieren einer Mailto-Erweiterung, um zu verhindern, dass eine virtualisierte Anwendung diese Erweiterung aus einer anderen Anwendung überschreibt.

App-V-Pakete enthalten die Manifestdatei in der Appv-Paketdatei, die für Sequenzierungsvorgänge repräsentativ ist und die Richtlinie ihrer Wahl ist, es sei denn, einem bestimmten Paket sind Dynamische Konfigurationsdateien zugewiesen. Nach der Sequenzierung können die Dateien der dynamischen Konfiguration geändert werden, um die Veröffentlichung einer Anwendung auf verschiedenen Desktops oder Benutzern mit unterschiedlichen Erweiterungspunkten zu ermöglichen. Die beiden Dynamic Configuration Files sind die Dynamic Deployment Configuration (DDC)- und dynamic User Configuration (DUC)-Dateien. In diesem Abschnitt liegt der Schwerpunkt auf der Kombination von Manifestdateien und dynamischen Konfigurationsdateien.

### <a name="example-for-dynamic-configuration-files"></a>Beispiel für dynamische Konfigurationsdateien

Das folgende Beispiel zeigt die Kombination der Dateien "Manifest", "Bereitstellungskonfiguration" und "Benutzerkonfiguration" nach der Veröffentlichung und während des normalen Betriebs. Diese Beispiele sind abgekürzte Beispiele für jede der Dateien. Der Zweck besteht darin, nur die Kombination der Dateien anzuzeigen und keine vollständige Beschreibung der spezifischen Kategorien zu sein, die in den einzelnen Dateien verfügbar sind. Weitere Informationen hierzu im Sequenzierungshandbuch für App-V 5 unter: <https://go.microsoft.com/fwlink/?LinkID=269810>

**Manifest**

```xml
<appv:Extension Category="AppV.Shortcut">
     <appv:Shortcut>
          <appv:File>[{Common Programs}]\7-Zip\7-Zip File Manager.lnk</appv:File>
          <appv:Target>[{AppVPackageRoot}]\7zFM.exe</appv:Target>
          <appv:Icon>[{AppVPackageRoot}]\7zFM exe.O.ico</appv:Icon>
     </appv:Shortcut>
</appv:Extension>
```

**Bereitstellungskonfiguration**

```xml
<MachineConfiguration>
     <Subsystems>
          <Registry>
               <Include>
                    <Key Path= "\REGISTRY\Machine\Software\7zip">
                    <Value Type="REG_SZ" Name="Config" Data="1234"/>
                    </Key>
               </Include>
          </Registry>
     </Subsystems>
```

**Benutzerkonfiguration**

```xml
<UserConfiguration>
     <Subsystems>
<appv:ExtensionCategory="AppV.Shortcut">
     <appv:Shortcut>
          <appv:File>[{Desktop}]\7-Zip\7-Zip File Manager.lnk</appv:File>
          <appv:Target>[{AppVPackageRoot}]\7zFM.exe</appv:Target>
          <appv:Icon>[{AppVPackageRoot}]\7zFM exe.O.ico</appv:Icon>
     </appv:Shortcut>
</appv:Extension>
     </Subsystems>
<UserConfiguration>
     <Subsystems>
<appv:Extension Category="AppV.Shortcut">
     <appv:Shortcut>
          <appv:Fìle>[{Desktop}]\7-Zip\7-Zip File Manager.lnk</appv:File>
          <appv:Target>[{AppVPackageRoot}]\7zFM.exe</appv:Target>
          <appv:Icon>[{AppVPackageRoot}]\7zFM.exe.O.ico</appv:Icon>
     </appv:Shortcut>
     <appv:Shortcut>
          <appv:File>[{Common Programs}]\7-Zip\7-Zip File Manager.Ink</appv:File>
          <appv:Target>[{AppVPackageRoot}]\7zFM.exe</appv:Target>
          <appv:Icon>[{AppVPackageRoot)]\7zFM.exe.O.ico</appv: Icon>
     </appv:Shortcut>
</appv:Extension>
     </Subsystems>
<MachineConfiguration>
     <Subsystems>
          <Registry>
               <Include>
                    <Key Path="\REGISTRY\Machine\Software\7zip">
                    <Value Type=”REG_SZ" Name="Config" Data="1234"/>
               </Include>
          </Registry>
     </Subsystems>
```

## <a name="side-by-side-assemblies"></a><a href="" id="bkmk-sidebyside-assemblies"></a>Parallele Assemblys


App-V unterstützt das automatische Verpacken von Parallelassemblys (Side-by-Side, SxS) während der Sequenzierung und Bereitstellung auf dem Client während der Veröffentlichung virtueller Anwendungen. App-V 5 SP2 unterstützt die Erfassung von SxS-Assemblys während der Sequenzierung für Assemblys, die nicht auf dem Sequenzierungscomputer vorhanden sind. Und für Assemblys, die aus Visual C++ (Version 8 und höher) und/oder MSXML Laufzeit bestehen, erkennt und erfasst der Sequencer diese Abhängigkeiten automatisch, auch wenn sie während der Überwachung nicht installiert wurden. Das Feature "Parallele Assemblys" entfernt die Einschränkungen früherer Versionen von App-V, bei denen der App-V Sequencer keine Assemblys erfasst hat, die bereits auf der Sequenzierungsarbeitsstation vorhanden sind, und die Assemblys zu privatisieren, die auf eine Bitversion pro Paket beschränkt sind. Dieses Verhalten führte dazu, dass bereitgestellte App-V-Anwendungen für Clients die erforderlichen SxS-Assemblys fehlten, was zu Anwendungsstartfehlern führte. Dadurch musste der Verpackungsvorgang dokumentiert werden und dann sichergestellt werden, dass alle für Pakete erforderlichen Assemblys lokal auf dem Clientbetriebssystem des Benutzers installiert wurden, um die Unterstützung für die virtuellen Anwendungen sicherzustellen. Basierend auf der Anzahl der Assemblys und der fehlenden Anwendungsdokumentation für die erforderlichen Abhängigkeiten war diese Aufgabe sowohl eine Verwaltungs- als auch eine Implementierungsaufgabe.

Die Unterstützung der Parallelassembly in App-V bietet die folgenden Features.

-   Automatische Erfassung der SxS-Assembly während der Sequenzierung, unabhängig davon, ob die Assembly bereits auf der Sequenzierungsarbeitsstation installiert war.

-   Der App-V-Client installiert die erforderlichen SxS-Assemblys automatisch zum Zeitpunkt der Veröffentlichung auf dem Clientcomputer, wenn sie nicht vorhanden sind.

-   Der Sequencer meldet die VC-Laufzeitabhängigkeit im Sequencer-Berichterstellungsmechanismus.

-   Der Sequencer ermöglicht es, die assemblys, die bereits auf dem Sequencer installiert sind, nicht zu verpacken, was Szenarien unterstützt, in denen die Assemblys zuvor auf den Zielcomputern installiert wurden.

### <a name="automatic-publishing-of-sxs-assemblies"></a>Automatische Veröffentlichung von SxS-Assemblys

Während der Veröffentlichung eines App-V-Pakets mit SxS-Assemblys überprüft der App-V-Client, ob die Assembly auf dem Computer vorhanden ist. Wenn die Assembly nicht vorhanden ist, stellt der Client die Assembly auf dem Computer bereit. Pakete, die Teil von Verbindungsgruppen sind, basieren auf den Parallelassemblyinstallationen, die Teil der Basispakete sind, da die Verbindungsgruppe keine Informationen zur Assemblyinstallation enthält.

**Hinweis:**  
Wenn Sie die Veröffentlichung eines Pakets mit einer Assembly aufheben oder entfernen, werden die Assemblys für dieses Paket nicht entfernt.

 

## <a name="client-logging"></a><a href="" id="bkmk-client-logging"></a>Clientprotokollierung


Der App-V-Client protokolliert Informationen im etw-Standardformat im Windows Ereignisprotokoll. Die spezifischen App-V-Ereignisse finden Sie in der Ereignisanzeige unter "Anwendungs- und Dienstprotokolle\\Microsoft\\AppV\\Client".

**Hinweis:**  
In App-V 5.0 SP3 wurden einige Protokolle konsolidiert und an den folgenden Speicherort verschoben:

`Event logs/Applications and Services Logs/Microsoft/AppV/ServiceLog`

Eine Liste der verschobenen Protokolle finden Sie unter ["Informationen zu App-V 5.0 SP3".](about-app-v-50-sp3.md#bkmk-event-logs-moved)

 

Es gibt drei spezifische Kategorien von Ereignissen, die unten beschrieben werden.

**Administrator:** Protokolliert Ereignisse für Konfigurationen, die auf den App-V-Client angewendet werden, und enthält die primären Warnungen und Fehler.

**Betriebsbereit:** Protokolliert die allgemeine App-V-Ausführung und -Verwendung einzelner Komponenten und erstellt ein Überwachungsprotokoll der App-V-Vorgänge, die auf dem App-V-Client abgeschlossen wurden.

**Virtuelle Anwendung:** Protokolliert das Starten virtueller Anwendungen und die Verwendung von Virtualisierungssubsystemen.






 

 





