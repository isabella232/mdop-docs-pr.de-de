---
title: Anwendungsveröffentlichung und Clientinteraktion
description: Anwendungsveröffentlichung und Clientinteraktion
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
ms.openlocfilehash: 69fcf119faaf35e53ae36f386bcb3480e2ee3b0e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805948"
---
# Anwendungsveröffentlichung und Clientinteraktion


Dieser Artikel enthält technische Informationen zu allgemeinen App-V-Clientvorgängen und deren Integration in das lokale Betriebssystem.

-   [App-V-Paketdateien, die vom Sequencer erstellt wurden](#bkmk-appv-pkg-files-list)

-   [Was befindet sich in der AppV-Datei?](#bkmk-appv-file-contents)

-   [App-V-Client Datenspeicherorte](#bkmk-files-data-storage)

-   [Paket Registrierung](#bkmk-pkg-registry)

-   [App-V-Paketspeicher Verhalten](#bkmk-pkg-store-behavior)

-   [Roaming-Registrierung und Daten](#bkmk-roaming-reg-data)

-   [App-V Client Application Lifecycle Management](#bkmk-clt-app-lifecycle)

-   [Integration von App-V-Paketen](#bkmk-integr-appv-pkgs)

-   [Verarbeitung dynamischer Konfigurationen](#bkmk-dynamic-config)

-   [Nebeneinander angeordnete Assemblys](#bkmk-sidebyside-assemblies)

-   [Client Protokollierung](#bkmk-client-logging)

Weitere Referenzinformationen finden Sie unter [Dokumentation der Microsoft Application Virtualization (App-V)-Download Seite](https://www.microsoft.com/download/details.aspx?id=27760).

## <a href="" id="bkmk-appv-pkg-files-list"></a>App-V-Paketdateien, die vom Sequencer erstellt wurden


Der Sequencer erstellt App-V-Pakete und erstellt eine virtualisierte Anwendung. Der Sequenzierungsprozess erstellt die folgenden Dateien:

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
<td align="left"><p>. AppV</p></td>
<td align="left"><ul>
<li><p>Die primäre Paketdatei, die die erfassten Ressourcen und Zustandsinformationen aus dem Sequenz Prozess enthält.</p></li>
<li><p>Architektur der Paketdatei, Veröffentlichungsinformationen und Registrierung in einem Token-Formular, das bei der Zustellung erneut auf einen Computer und einen bestimmten Benutzer angewendet werden kann.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>. MSI</p></td>
<td align="left"><p>Ausführbarer Bereitstellungs Wrapper, mit dem Sie AppV-Dateien manuell oder mithilfe einer Bereitstellungsplattform eines Drittanbieters bereitstellen können.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>_DeploymentConfig.XML</p></td>
<td align="left"><p>Datei, die verwendet wird, um die Standard Veröffentlichungs Parameter für alle Anwendungen in einem Paket anzupassen, das für alle Benutzer auf einem Computer, auf dem der App-V-Client ausgeführt wird, Global bereitgestellt wird.</p></td>
</tr>
<tr class="even">
<td align="left"><p>_UserConfig.XML</p></td>
<td align="left"><p>Datei, die verwendet wird, um die Veröffentlichungs Parameter für alle Anwendungen in einem Paket anzupassen, das für einen bestimmten Benutzer auf einem Computer bereitgestellt wird, auf dem der App-V-Client ausgeführt wird.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Report.xml</p></td>
<td align="left"><p>Zusammenfassung der Nachrichten, die sich aus dem Sequenz Prozess ergeben, einschließlich weggelassener Treiber, Dateien und Registrierungsspeicherorte.</p></td>
</tr>
<tr class="even">
<td align="left"><p>. CAB</p></td>
<td align="left"><p><em>Optional: </em> Paket Beschleunigerdatei, die zum automatischen Neuaufbau eines zuvor sequenzierten virtuellen Anwendungspakets verwendet wird.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>.appvt</p></td>
<td align="left"><p><em>Optional: </em> Sequencer-Vorlagendatei zur Beibehaltung häufig wieder verwendeter Sequenzer-Einstellungen.</p></td>
</tr>
</tbody>
</table>

 

Informationen zur Sequenzierung finden Sie unter [Application Virtualization sequenceing Guide](https://go.microsoft.com/fwlink/?LinkID=269810).

## <a href="" id="bkmk-appv-file-contents"></a>Was befindet sich in der AppV-Datei?


Bei der AppV-Datei handelt es sich um einen Container, in dem XML-und nicht-XML-Dateien zusammen in einer einzelnen Entität gespeichert werden. Diese Datei wurde aus dem AppX-Format erstellt, das auf dem OPC-Standard (Open Packaging Conventions) basiert.

Wenn Sie den Inhalt der AppV-Datei anzeigen möchten, erstellen Sie eine Kopie des Pakets, und benennen Sie die kopierte Datei dann in eine ZIP-Erweiterung um.

Die AppV-Datei enthält die folgenden Ordner und Dateien, die beim Erstellen und Veröffentlichen einer virtuellen Anwendung verwendet werden:

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
<td align="left"><p>Verzeichnis, das das Dateisystem für die virtualisierte Anwendung enthält, das während der Sequenzierung erfasst wird.</p></td>
</tr>
<tr class="even">
<td align="left"><p>[Content_Types]. XML</p></td>
<td align="left"><p>XML-Datei</p></td>
<td align="left"><p>Liste der Hauptinhalts Typen in der AppV-Datei (z. b. dll, exe, bin)</p></td>
</tr>
<tr class="odd">
<td align="left"><p>AppxBlockMap.xml</p></td>
<td align="left"><p>XML-Datei</p></td>
<td align="left"><p>Das Layout der AppV-Datei, in der Datei-, Block-und BlockMap-Elemente verwendet werden, die den Speicherort und die Überprüfung von Dateien im App-V-Paket ermöglichen.</p></td>
</tr>
<tr class="even">
<td align="left"><p>AppxManifest.xml</p></td>
<td align="left"><p>XML-Datei</p></td>
<td align="left"><p>Metadaten für das Paket, das die erforderlichen Informationen zum Hinzufügen, veröffentlichen und Starten des Pakets enthält. Enthält Erweiterungspunkte (Dateitypzuordnungen und Tastenkombinationen) sowie die Namen und GUIDs, die dem Paket zugeordnet sind.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>FilesystemMetadata.xml</p></td>
<td align="left"><p>XML-Datei</p></td>
<td align="left"><p>Liste der Dateien, die während der Sequenzierung erfasst werden, einschließlich Attribute (z. b. Verzeichnisse, Dateien, undurchsichtige Verzeichnisse, leere Verzeichnisse sowie lange und kurze Namen).</p></td>
</tr>
<tr class="even">
<td align="left"><p>PackageHistory.xml</p></td>
<td align="left"><p>XML-Datei</p></td>
<td align="left"><p>Informationen zum Sequenzcomputer (Betriebssystemversion, Internet Explorer-Version, .NET Framework-Version) und Prozess (Upgrade, Paketversion).</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Registry. dat</p></td>
<td align="left"><p>DAT-Datei</p></td>
<td align="left"><p>Registrierungsschlüssel und Werte, die während des Sequenz Prozesses für das Paket erfasst wurden.</p></td>
</tr>
<tr class="even">
<td align="left"><p>StreamMap.xml</p></td>
<td align="left"><p>XML-Datei</p></td>
<td align="left"><p>Liste der Dateien für den Haupt-und Veröffentlichungs-Feature-Block. Der Veröffentlichungsfeature-Block enthält die ICO-Dateien und die erforderlichen Teile von Dateien (exe und dll) für die Veröffentlichung des Pakets. Wenn vorhanden, enthält der primäre Feature-Block Dateien, die während des Sequenz Prozesses für Streaming optimiert wurden.</p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-files-data-storage"></a>App-V-Client Datenspeicherorte


Der App-V-Client führt Aufgaben aus, um sicherzustellen, dass virtuelle Anwendungen ordnungsgemäß ausgeführt werden und wie lokal installierte Anwendungen funktionieren. Der Vorgang zum Öffnen und Ausführen virtueller Anwendungen erfordert eine Zuordnung aus dem virtuellen Dateisystem und der Registrierung, um sicherzustellen, dass die Anwendung über die erforderlichen Komponenten einer herkömmlichen Anwendung verfügt, die von Benutzern erwartet wird. In diesem Abschnitt werden die Ressourcen beschrieben, die für die Ausführung virtueller Anwendungen erforderlich sind, und der Ort, an dem App-V die Ressourcen speichert.

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
<td align="left"><p>Paketspeicher</p></td>
<td align="left"><p>%ProgramData%\App-V</p></td>
<td align="left"><p>Standardspeicherort für nur-Lese-Paketdateien</p></td>
</tr>
<tr class="even">
<td align="left"><p>Computer Katalog</p></td>
<td align="left"><p>%ProgramData%\Microsoft\AppV\Client\Catalog</p></td>
<td align="left"><p>Enthält Konfigurationsdokumente pro Computer</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Benutzer Katalog</p></td>
<td align="left"><p>%AppData%\Microsoft\AppV\Client\Catalog</p></td>
<td align="left"><p>Enthält Konfigurationsdokumente pro Benutzer</p></td>
</tr>
<tr class="even">
<td align="left"><p>Verknüpfungs Sicherungen</p></td>
<td align="left"><p>%AppData%\Microsoft\AppV\Client\Integration\ShortCutBackups</p></td>
<td align="left"><p>Speichert vorherige Integrationspunkte, die die Wiederherstellung bei der Paket Veröffentlichung aktivieren</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Roaming auf Write (Kuh) kopieren</p></td>
<td align="left"><p>%AppData%\Microsoft\AppV\Client\VFS</p></td>
<td align="left"><p>Beschreibbarer Roaming-Speicherort für Paketänderungen</p></td>
</tr>
<tr class="even">
<td align="left"><p>Auf Schreib (Kuh) lokal kopieren</p></td>
<td align="left"><p>%LocalAppData%\Microsoft\AppV\Client\VFS</p></td>
<td align="left"><p>Beschreibbarer Speicherort für nicht-Roaming für Paketänderung</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Computerregistrierung</p></td>
<td align="left"><p>HKLM\Software\Microsoft\AppV</p></td>
<td align="left"><p>Enthält Paket Zustandsinformationen, einschließlich VReg für Computer-oder Global veröffentlichte Pakete (Machine Hive)</p></td>
</tr>
<tr class="even">
<td align="left"><p>Benutzerregistrierung</p></td>
<td align="left"><p>HKCU\Software\Microsoft\AppV</p></td>
<td align="left"><p>Enthält Informationen zum Paket Zustand des Benutzers, einschließlich VReg</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Benutzer Registrierungsklassen</p></td>
<td align="left"><p>HKCU\Software\Classes\AppV</p></td>
<td align="left"><p>Enthält zusätzliche Informationen zum Benutzerpaket Zustand</p></td>
</tr>
</tbody>
</table>

 

Weitere Details zur Tabelle finden Sie im Abschnitt unten und im gesamten Dokument.

### Paketspeicher

Der App-V-Client verwaltet die im Paketspeicher bereitgestellten Anwendungsressourcen. Dieser Standardspeicherort ist `%ProgramData%\App-V` , Sie können ihn aber während oder nach dem Setup konfigurieren, indem Sie den `Set-AppVClientConfiguration` PowerShell-Befehl verwenden, der die lokale Registrierung ändert ( `PackageInstallationRoot` Wert unter dem `HKLM\Software\Microsoft\AppV\Client\Streaming` Schlüssel). Der Paketspeicher muss sich im lokalen Pfad des Clientbetriebssystems befinden. Die einzelnen Pakete werden im Paketspeicher in Unterverzeichnissen gespeichert, die für Paket-GUID und Versions-GUID benannt sind.

Beispiel für einen Pfad zu einer bestimmten Anwendung:

``` syntax
C:\ProgramData\App-V\PackGUID\VersionGUID
```

Informationen zum Ändern des Standardspeicherorts des Paketspeichers während der Installation finden Sie unter [Bereitstellen des App-V-Clients](how-to-deploy-the-app-v-client-51gb18030.md).

### Freigegebener Inhaltsspeicher

Wenn der App-V-Client im freigegebenen Inhaltsspeicher Modus konfiguriert ist, werden keine Daten auf den Datenträger geschrieben, wenn ein Datenstromfehler auftritt, was bedeutet, dass für die Pakete nur minimaler lokaler Speicherplatz benötigt wird (Veröffentlichungsdaten). Die Verwendung von weniger Speicherplatz ist in VDI-Umgebungen, in denen der lokale Speicher limitiert werden kann, und das Streaming der Anwendungen von einem Hochleistungsnetzwerk Standort (wie einem SAN) vorzuziehen. Weitere Informationen zum Speichermodus für freigegebene Inhalte finden Sie unter <https://go.microsoft.com/fwlink/p/?LinkId=392750> .

**Hinweis**  Der Computer und der Paketspeicher müssen sich auf einem lokalen Laufwerk befinden, auch wenn Sie für den App-V-Client freigegebene Inhaltsspeicher Konfigurationen verwenden.

 

### Paket Kataloge

Der App-V-Client verwaltet die folgenden beiden dateibasierten Speicherorte:

-   **Kataloge (Benutzer und Computer).**

-   **Registrierungsspeicherorte** – hängt davon ab, wie das Paket für die Veröffentlichung vorgesehen ist. Es gibt einen Katalog (Datenspeicher) für den Computer und einen Katalog für jeden einzelnen Benutzer. Der Computer Katalog speichert globale Informationen, die für alle Benutzer oder einen beliebigen Benutzer gelten, und der Benutzer Katalog speichert Informationen, die für einen bestimmten Benutzer gelten. Der Katalog ist eine Sammlung von dynamischen Konfigurationen und Manifestdateien; Es gibt diskrete Daten für Datei und Registrierung pro Paketversion. 

### Computer Katalog

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p>Beschreibung</p></td>
<td align="left"><p>Speichert Paket Dokumente, die für Benutzer auf dem Computer verfügbar sind, wenn Pakete hinzugefügt und veröffentlicht werden. Wenn ein Paket jedoch zum Zeitpunkt der Veröffentlichung "Global" ist, stehen die Integrationen allen Benutzern zur Verfügung.</p>
<p>Wenn ein Paket nicht global ist, werden die Integrationen nur für bestimmte Benutzer veröffentlicht, es gibt jedoch weiterhin globale Ressourcen, die für jeden auf dem Clientcomputer geändert und sichtbar sind (beispielsweise befindet sich das Paketverzeichnis an einem freigegebenen Datenträgerspeicherort).</p>
<p>Wenn ein Paket für einen Benutzer auf dem Computer (Global oder nicht global) zur Verfügung steht, wird das Manifest im Computer Katalog gespeichert. Wenn ein Paket Global veröffentlicht wird, gibt es eine dynamische Konfigurationsdatei, die im Computer Katalog gespeichert ist. Daher wird festgelegt, ob ein Paket Global ist, je nachdem, ob im Computer Katalog eine Richtliniendatei (UserDeploymentConfiguration-Datei) vorhanden ist.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Standardspeicherort</p></td>
<td align="left"><p><code>%programdata%\Microsoft\AppV\Client\Catalog&lt;/code&gt;</p>
<p>Dieser Speicherort ist nicht mit dem Speicherort des Paketspeichers identisch. Der Paketspeicher ist die Goldene oder ursprüngliche Kopie der Paketdateien.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Dateien im Computer Katalog</p></td>
<td align="left"><ul>
<li><p>Manifest.xml</p></li>
<li><p>DeploymentConfiguration.xml</p></li>
<li><p>UserManifest.xml (Global veröffentlichtes Paket)</p></li>
<li><p>UserDeploymentConfiguration.xml (Global veröffentlichtes Paket)</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Zusätzlicher Standort des Computer Katalogs, der verwendet wird, wenn das Paket zu einer Verbindungsgruppe gehört</p></td>
<td align="left"><p>Der folgende Standort ist zusätzlich zu dem oben genannten speziellen Paketspeicherort:</p>
<p><code>%programdata%\Microsoft\AppV\Client\Catalog\PackageGroups\ConGroupGUID\ConGroupVerGUID</code></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Zusätzliche Dateien im Computer Katalog, wenn das Paket zu einer Verbindungsgruppe gehört</p></td>
<td align="left"><ul>
<li><p>PackageGroupDescriptor.xml</p></li>
<li><p>UserPackageGroupDescriptor.xml (Globally published Connection Group)</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

### Benutzer Katalog

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p>Beschreibung</p></td>
<td align="left"><p>Während des Veröffentlichungsprozesses erstellt. Enthält Informationen, die für die Veröffentlichung des Pakets verwendet werden, und wird auch beim Start verwendet, um sicherzustellen, dass ein Paket für einen bestimmten Benutzer bereitgestellt wird. Wird in einem Roaming-Speicherort erstellt und enthält benutzerspezifische Veröffentlichungsinformationen.</p>
<p>Wenn ein Paket für einen Benutzer veröffentlicht wird, wird die Richtliniendatei im Benutzer Katalog gespeichert. Gleichzeitig wird eine Kopie des Manifests auch im Benutzer Katalog gespeichert. Wenn ein Paket Anspruch für einen Benutzer entfernt wird, werden die entsprechenden Paketdateien aus dem Benutzer Katalog entfernt. Wenn Sie sich den Benutzer Katalog ansehen, kann ein Administrator das vorhanden sein einer dynamischen Konfigurationsdatei anzeigen, die angibt, dass das Paket für diesen Benutzer berechtigt ist.</p>
<p>Für Roaming-Benutzer muss sich der Benutzer Katalog an einem Roaming-oder freigegebenen Speicherort befinden, um das Legacy-App-V-Verhalten für die standardmäßige Ausrichtung von Benutzern beizubehalten. Der Anspruch und die Richtlinie sind an einen Benutzer und nicht an einen Computer gebunden, daher sollten Sie mit dem Benutzer Roaming durchlaufen, sobald er bereitgestellt wurde.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Standardspeicherort</p></td>
<td align="left"><p><code>appdata\roaming\Microsoft\AppV\Client\Catalog\Packages\PkgGUID\VerGUID</code></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Dateien im Benutzer Katalog</p></td>
<td align="left"><ul>
<li><p>UserManifest.xml</p></li>
<li><p>DynamicConfiguration.xml oder UserDeploymentConfiguration.xml</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Zusätzlicher Speicherort des Benutzer Katalogs, der verwendet wird, wenn das Paket zu einer Verbindungsgruppe gehört</p></td>
<td align="left"><p>Der folgende Standort ist zusätzlich zu dem oben genannten speziellen Paketspeicherort:</p>
<p><code>appdata\roaming\Microsoft\AppV\Client\Catalog\PackageGroups\PkgGroupGUID\PkgGroupVerGUID</code></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Zusätzliche Datei im Computer Katalog, wenn das Paket zu einer Verbindungsgruppe gehört</p></td>
<td align="left"><p><code>UserPackageGroupDescriptor.xml</code></p></td>
</tr>
</tbody>
</table>

 

### Verknüpfungs Sicherungen

Während des Veröffentlichungsprozesses unterstützt der App-V-Client alle Verknüpfungen, und Integrationspunkte für `%AppData%\Microsoft\AppV\Client\Integration\ShortCutBackups.` diese Sicherung ermöglichen die Wiederherstellung dieser Integrationspunkte in den vorherigen Versionen, wenn das Paket nicht veröffentlicht wurde.

### Beim Schreiben von Dateien kopieren

Der Paketspeicher enthält eine ursprüngliche Kopie der Paketdateien, die vom Veröffentlichungsserver gestreamt wurden. Während des normalen Betriebs einer App-V-Anwendung erfordert der Benutzer oder Dienst möglicherweise Änderungen an den Dateien. Diese Änderungen werden nicht im Paketspeicher vorgenommen, um die Möglichkeit zu erhalten, die Anwendung zu reparieren, wodurch diese Änderungen entfernt werden. Diese Speicherorte, so genannte Copy on Write (Cow), unterstützen sowohl Roaming-als auch nicht-Roaming-Speicherorte. Der Speicherort, an dem die Änderungen gespeichert werden, hängt davon ab, wo die Anwendung so programmiert wurde, dass Änderungen in einer systemeigenen Umgebung geschrieben werden.

### Kuh-Roaming

Der oben beschriebene Cow-Roaming-Standort speichert Änderungen an Dateien und Verzeichnissen, die auf den typischen Standort "% AppData%" oder "\\Users\\{username}\\AppData\\Roaming" ausgerichtet sind. Diese Verzeichnisse und Dateien werden dann basierend auf den Einstellungen des Betriebssystems durchlaufen.

### Kuh lokal

Der lokale Speicherort der Kuh ähnelt dem Roaming-Speicherort, aber die Verzeichnisse und Dateien werden nicht auf anderen Computern gespeichert, auch wenn Roaming-Unterstützung konfiguriert wurde. Der oben beschriebene Cow-Standort speichert Änderungen, die für typische Fenster gelten, und nicht die Position% APPDATA%. Die aufgelisteten Verzeichnisse sind unterschiedlich, es gibt jedoch zwei Speicherorte für typische Windows-Speicherorte (beispielsweise Common APPDATA und Common AppDataS). Das **S** gibt den eingeschränkten Speicherort an, wenn der virtuelle Dienst die Änderung als einen anderen erhöhten Benutzer von den angemeldeten Benutzern anfordert. Der nicht-**S** -Standort speichert benutzerbasierte Änderungen.

## <a href="" id="bkmk-pkg-registry"></a>Paket Registrierung


Bevor eine Anwendung auf die Paket Registrierungsdaten zugreifen kann, muss der App-V-Client die Paket Registrierungsdaten für die Anwendungen verfügbar machen. Der App-V-Client verwendet die echte Registrierung als Sicherungsspeicher für alle Registrierungsdaten.

Wenn dem App-V-Client ein neues Paket hinzugefügt wird, eine Kopie der Registrierung. DAT-Datei aus dem Paket wird erstellt am `%ProgramData%\Microsoft\AppV\Client\VREG\{Version GUID}.dat` . Der Name der Datei ist die Versions-GUID mit dem. DAT-Erweiterung. Der Grund für diese Kopie besteht darin, sicherzustellen, dass die eigentliche Hive-Datei im Paket nie verwendet wird, wodurch das Entfernen des Pakets zu einem späteren Zeitpunkt verhindert werden kann.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Registry. dat aus dem Paketspeicher</strong></p></td>
<td align="left"><p><strong> &gt; </strong></p></td>
<td align="left"><p><strong>%ProgramData%\Microsoft\AppV\Client\Vreg {VersionGuid}. dat</strong></p></td>
</tr>
</tbody>
</table>

 

Wenn die erste Anwendung aus dem Paket auf dem Client gestartet wird, wird der Client den Inhalt aus der hivedatei wiederherstellen oder kopieren, wodurch die Paket Registrierungsdaten an einem alternativen Speicherort neu erstellt werden `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\AppV\Client\Packages\PackageGuid\Versions\VersionGuid\REGISTRY` . Die bereitgestellten Registrierungsdaten weisen zwei unterschiedliche Typen von Computer Daten und Benutzerdaten auf. Computer Daten werden für alle Benutzer auf dem Computer freigegeben. Benutzerdaten werden für jeden Benutzer an einem benutzerabhängige-Speicherort bereitgestellt `HKCU\Software\Microsoft\AppV\Client\Packages\PackageGuid\Registry\User` . Die Computer Daten werden letztendlich beim Entfernen des Pakets entfernt, und die Benutzerdaten werden bei einem Veröffentlichungsvorgang des Benutzers entfernt.

### Staging von Paket Registrierungen vs. Verbindungsgruppen Registrierung

Wenn Verbindungsgruppen vorhanden sind, gilt der vorherige Prozess der Staging der Registrierung als wahr, doch anstatt eine Strukturdatei zu verarbeiten, gibt es mehr als eine. Die Dateien werden in der Reihenfolge verarbeitet, in der Sie in der Verbindungsgruppe XML angezeigt werden, wobei der erste Writer Konflikte gewinnt.

Die bereitgestellte Registrierung bleibt auf die gleiche Weise wie im einzelnen Paket Fall erhalten. Die bereitgestellten Benutzerregistrierungsdaten verbleibt für die Verbindungsgruppe, bis Sie deaktiviert ist. die Registrierungsdaten für ein Stagingcomputer werden beim Entfernen der Verbindungsgruppe entfernt.

### Virtuelle Registrierung

Der Zweck der virtuellen Registrierung (VREG) besteht darin, eine einzelne zusammengeführte Ansicht der Paket Registrierung und der systemeigenen Registrierung für Anwendungen bereitzustellen. Darüber hinaus bietet es die Funktion Copy-on-Write (Cow) – das heißt, dass alle Änderungen an der Registrierung aus dem Kontext eines virtuellen Prozesses an einem separaten Cow-Speicherort vorgenommen werden. Das bedeutet, dass der VREG bis zu drei getrennte Registrierungsspeicherorte in einer einzigen Ansicht basierend auf den aufgefüllten Speicherorten in der Registrierungs-Cow- &gt; Package-Native kombinieren muss &gt; . Wenn eine Anforderung für Registrierungsdaten erfolgt, findet Sie in der Reihenfolge, bis Sie die angeforderten Daten gefunden hat. Bedeutet dies, dass ein Wert, der in einem Cow-Speicherort gespeichert ist, nicht an andere Speicherorte weitergeleitet wird, wenn sich am Speicherort der Kuh keine Daten befinden, wird das Paket und dann der systemeigene Speicherort weitergeleitet, bis die entsprechenden Daten gefunden wurden.

### Registrierungsspeicherorte

Je nachdem, ob das Paket einzeln oder als Teil einer Verbindungsgruppe veröffentlicht wird, gibt es zwei Speicherorte für die Paket Registrierung und zwei Verbindungsgruppen Speicherorte, an denen der App-V-Client Registrierungsinformationen speichert. Es gibt drei Cow-Speicherorte für Pakete und drei für Verbindungsgruppen, die von der VREG erstellt und verwaltet werden. Einstellungen für Pakete und Verbindungsgruppen werden nicht freigegeben:

**Einzelnes Paket VReg:**

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
<td align="left"><p><strong>Kuhanzug</strong></p></td>
<td align="left"><ul>
<li><p>Machine Registry\Client\Packages\PkgGUID\REGISTRY (nur Elevate-Prozess kann schreiben)</p></li>
<li><p>Benutzer Registry\Client\Packages\PkgGUID\REGISTRY (Benutzer-Roaming-alles, was unter HKCU außer Software\Classes geschrieben wurde</p></li>
<li><p>Benutzer Registrierungs Classes\Client\Packages\PkgGUID\REGISTRY (HKCU\Software\Classes-Schreibvorgänge und HKLM für nicht erhöhten Prozess)</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Paket</strong></p></td>
<td align="left"><ul>
<li><p>Machine Registry\Client\Packages\PkgGUID\Versions\VerGuid\Registry\Machine</p></li>
<li><p>Benutzer Registrierungs Classes\Client\Packages\PkgGUID\Versions\VerGUID\Registry</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Systemeigene</strong></p></td>
<td align="left"><ul>
<li><p>Registrierungsspeicherort der systemeigenen Anwendung</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

 

**Verbindungsgruppe VReg:**

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
<td align="left"><p><strong>Kuhanzug</strong></p></td>
<td align="left"><ul>
<li><p>Machine Registry\Client\PackageGroups\GrpGUID\REGISTRY (nur Elevate-Prozess kann schreiben)</p></li>
<li><p>Benutzer Registry\Client\PackageGroups\GrpGUID\REGISTRY (alles, was in HKCU außer Software\Classes geschrieben wurde</p></li>
<li><p>Benutzer Registrierungs Classes\Client\PackageGroups\GrpGUID\REGISTRY</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Paket</strong></p></td>
<td align="left"><ul>
<li><p>Machine Registry\Client\PackageGroups\GrpGUID\Versions\VerGUID\REGISTRY</p></li>
<li><p>Benutzer Registrierungs Classes\Client\PackageGroups\GrpGUID\Versions\VerGUID\REGISTRY</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Systemeigene</strong></p></td>
<td align="left"><ul>
<li><p>Registrierungsspeicherort der systemeigenen Anwendung</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

 

Es gibt zwei Kuh-Standorte für HKLM; erhöhte und nicht erhöhte Prozesse. Erhöhte Prozesse schreiben immer HKLM-Änderungen in die sichere Kuh unter HKLM. Nicht erhöhte Prozesse schreiben immer HKLM-Änderungen an der nicht sicheren Kuh unter HKCU\\Software\\Classes. Wenn eine Anwendung Änderungen von HKLM liest, lesen erhöhte Prozesse Änderungen aus der sicheren Kuh unter HKLM. Nicht erhöhte Lesevorgänge von beiden, begünstigt die Änderungen, die in der unsicheren Kuh zuerst vorgenommen wurden.

### Pass-Through-Tasten

Durch Pass-Through-Tasten können Administratoren bestimmte Schlüssel so konfigurieren, dass Sie nur aus der systemeigenen Registrierung gelesen werden können, wobei die Speicherorte für Pakete und Kühe umgangen werden. Pass-Through-Speicherorte sind global auf dem Computer (nicht Paket spezifisch) und können konfiguriert werden, indem Sie den Pfad zum Schlüssel hinzufügen, der als Pass-Through für das **reg \ _MULTI \ _SZ** Wert **PassThroughPaths** des Schlüssels behandelt werden soll `HKLM\Software\Microsoft\AppV\Subsystem\VirtualRegistry` . Jede Taste, die unter diesem mehrteiligen Zeichenfolgenwert (und ihren untergeordneten Elementen) angezeigt wird, wird als Passthrough behandelt.

Die folgenden Speicherorte sind standardmäßig als Pass-Through-Speicherorte konfiguriert:

-   HKEY \ _CURRENT \ _User \\software\\classes\\local Settings\\Software\\Microsoft\\Windows\\CurrentVersion\\AppModel

-   HKEY \ _LOCAL \ _MACHINE \\software\\classes\\local Settings\\Software\\Microsoft\\Windows\\CurrentVersion\\AppModel

-   HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\windows\\currentversion\\winevt

-   HKEY \ _LOCAL \ _MACHINE \\system\\currentcontrolset\\services\\eventlog\\application

-   HKEY \ _LOCAL \ _MACHINE \\system\\currentcontrolset\\control\\wmi\\autologger

-   HKEY \ _CURRENT \ _User \\software\\microsoft\\windows\\currentversion\\internet-Einstellungen

-   HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\windows NT\\CurrentVersion\\Perflib

-   HKEY \ _LOCAL \ _MACHINE \\software\\policies

-   HKEY \ _CURRENT \ _User \\software\\policies

Der Zweck von Pass-Through-Schlüsseln besteht darin, sicherzustellen, dass eine virtuelle Anwendung keine Registrierungsdaten in die VReg schreibt, die für nicht virtuelle Anwendungen für den erfolgreichen Betrieb oder die Integration erforderlich sind. Mit dem Richtlinienschlüssel wird sichergestellt, dass die vom Administrator festgelegten gruppenrichtlinienbasierten Einstellungen verwendet werden und nicht pro Paketeinstellungen. Der AppModel-Schlüssel ist für die Integration in Windows moderne UI-basierte Anwendungen erforderlich. Es wird empfohlen, dass Verwaltungen keine der standardmäßigen Pass-Through-Schlüssel ändern, aber in einigen Fällen erfordert das Hinzufügen von zusätzlichen Pass-Through-Schlüsseln möglicherweise auf Grundlage des Anwendungsverhaltens.

## <a href="" id="bkmk-pkg-store-behavior"></a>App-V-Paketspeicher Verhalten


App-V 5 verwaltet den Paketspeicher, also den Speicherort, an dem die erweiterten Objektdateien aus der AppV-Datei gespeichert werden. Dieser Speicherort wird standardmäßig unter%ProgramData%\\App-V gespeichert und ist in Bezug auf Speicherfunktionen nur durch freien Speicherplatz limitiert. Der Paketspeicher wird nach den GUIDs für das Paket und die Version organisiert, wie im vorherigen Abschnitt erwähnt.

### Pakete hinzufügen

App-v-Pakete werden beim Hinzufügen des Computers mit dem App-v-Client bereitgestellt. Der App-V-Client bietet Staging auf Abruf. Während der Veröffentlichung oder einem manuellen Add-AppVClientPackage wird die Datenstruktur im Paketspeicher (c:\\programdata\\App-V\\{PkgGUID}\\{VerGUID}) erstellt. Die im StreamMap.xml definierten Veröffentlichungs Blocks werden dem System und den Ordnern der obersten Ebene und untergeordneten Dateien hinzugefügt, um sicherzustellen, dass beim Start geeignete Anwendungsressourcen vorhanden sind.

### Befestigungs Pakete

Pakete können explizit mit der PowerShell oder mithilfe `Mount-AppVClientPackage` der **App-V-Client-Benutzeroberfläche** geladen werden, um ein Paket herunterzuladen. Durch diesen Vorgang wird das gesamte Paket vollständig in den Paketspeicher geladen.

### Streaming-Pakete

Der App-V-Client kann so konfiguriert werden, dass das Standardverhalten von Streaming geändert wird. Alle Streaming-Richtlinien werden unter dem folgenden Registrierungsschlüssel gespeichert: `HKEY_LOCAL_MAcHINE\Software\Microsoft\AppV\Client\Streaming` Richtlinien werden mit dem PowerShell-Cmdlet gesetzt `Set-AppvClientConfiguration` . Die folgenden Richtlinien gelten für Streaming:

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
<td align="left"><p>Unter Windows 8 und höher ermöglicht es das Streaming über 3G-und Mobilfunknetze.</p></td>
</tr>
<tr class="even">
<td align="left"><p>AutoLoad</p></td>
<td align="left"><p>Gibt die Einstellung für den Hintergrund Ladevorgang an:</p>
<p><strong>0 </strong> - deaktiviert</p>
<p><strong>1 </strong> – nur zuvor verwendete Pakete</p>
<p><strong>2 </strong> – alle Pakete</p></td>
</tr>
<tr class="odd">
<td align="left"><p>PackageInstallationRoot</p></td>
<td align="left"><p>Der Stammordner für den Paketspeicher auf dem lokalen Computer</p></td>
</tr>
<tr class="even">
<td align="left"><p>PackageSourceRoot</p></td>
<td align="left"><p>Die Root-Überschreibung, von der Pakete gestreamt werden sollen</p></td>
</tr>
<tr class="odd">
<td align="left"><p>SharedContentStoreMode</p></td>
<td align="left"><p>Ermöglicht die Verwendung des freigegebenen Inhaltsspeichers für VDI-Szenarien</p></td>
</tr>
</tbody>
</table>

 

 

Diese Einstellungen wirken sich auf das Verhalten von Streaming-App-V-Paketressourcen auf den Client aus. Standardmäßig downloadet App-V nur die Ressourcen, die nach dem Herunterladen der ersten Veröffentlichungs-und primären Feature-Blöcke erforderlich sind. Es gibt drei spezifische Verhaltensweisen rund um Streaming-Pakete, die erläutert werden müssen:

-   Hintergrund Streaming

-   Optimiertes Streaming

-   Datenstromfehler

### Hintergrund Streaming

Das PowerShell `Get-AppvClientConfiguration` -Cmdlet kann verwendet werden, um den aktuellen Modus für das Hintergrund Streaming mit der Einstellung "automatischer Lademodus" zu ermitteln und mit dem Cmdlet "AppvClientConfiguration" oder "Registry" (HKLM\\SOFTWARE\\Microsoft\\AppV\\ClientStreaming-Schlüssel) zu ändern. "Hintergrund Streaming" ist eine Standardeinstellung, bei der die Einstellung "automatisch laden" so eingestellt ist, dass zuvor verwendete Pakete heruntergeladen werden. Das Verhalten, das auf der Standardeinstellung (Wert = 1) basiert, downloadet App-V-Datenblöcke im Hintergrund, nachdem die Anwendung gestartet wurde. Diese Einstellung kann alle zusammen (Wert = 0) oder aktiviert für alle Pakete (Wert = 2) deaktiviert werden, unabhängig davon, ob Sie gestartet wurden.

### Optimiertes Streaming

App-V-Pakete können während der Sequenzierung mit einem primären Feature-Block konfiguriert werden. Diese Einstellung ermöglicht es dem Sequenz Ingenieur, Startdateien für eine bestimmte Anwendung oder Anwendungen zu überwachen und die Datenblöcke im App-V-Paket für Streaming beim ersten Start einer beliebigen Anwendung im Paket zu kennzeichnen.

### Datenstromfehler

Nach dem anfänglichen Datenstrom von Veröffentlichungsdaten und dem primären Feature-Block führen Anforderungen für zusätzliche Dateien Datenstromfehler aus. Diese Datenblöcke werden nach Bedarf in den Paketspeicher heruntergeladen. Auf diese Weise kann ein Benutzer nur einen kleinen Teil des Pakets herunterladen, was in der Regel ausreicht, um das Paket zu starten und normale Aufgaben auszuführen. Alle anderen Blöcke werden heruntergeladen, wenn ein Benutzer einen Vorgang initiiert, der Daten erfordert, die derzeit nicht im Paketspeicher enthalten sind.

Weitere Informationen zum App-V-Paketstreaming finden Sie unter: <https://go.microsoft.com/fwlink/?LinkId=392770> .

Die Sequenzierung für die Streaming-Optimierung steht unter: <https://go.microsoft.com/fwlink/?LinkId=392771> .

### Paketaktualisierungen

App-V-Pakete erfordern eine Aktualisierung während des gesamten Lebenszyklus der Anwendung. App-V-Paketaktualisierungen ähneln dem Paket Veröffentlichungsvorgang, da jede Version in Ihrem eigenen PackageRoot-Speicherort erstellt wird: `%ProgramData%\App-V\{PkgGUID}\{newVerGUID}` . Der Upgradevorgang wird durch das Erstellen von festen Links zu identischen und gestreamten Dateien aus anderen Versionen desselben Pakets optimiert.

### Paketentfernung

Das Verhalten des App-V-Clients, wenn Pakete entfernt werden, hängt von der zum Entfernen verwendeten Methode ab. Wenn Sie eine vollständige App-V-Infrastruktur verwenden, um die Veröffentlichung der Anwendung aufzuheben, werden die Benutzer Katalogdateien (Computer Katalog für Global veröffentlichte Anwendungen) entfernt, aber der Speicherort des Paketspeichers und die Standorte für Kühe bleiben erhalten. Wenn das PowerShell `Remove-AppVClientPackge` -Cmdlet zum Entfernen eines App-V-Pakets verwendet wird, wird der Speicherort des Paketspeichers bereinigt. Beachten Sie, dass beim Aufheben der Veröffentlichung eines App-V-Pakets vom Verwaltungs Server keine Entfernungs Operation durchgeführt wird. Bei keinem Vorgang werden die Paketspeicher Paketdateien entfernt.

## <a href="" id="bkmk-roaming-reg-data"></a>Roaming-Registrierung und Daten


App-V 5 ist in der Lage, in Abhängigkeit davon, wie die verwendete Anwendung geschrieben wird, beim Roaming eine nahezu native Umgebung bereitzustellen. Standardmäßig wird App-V auf der Grundlage der Roaming-Konfiguration des Betriebssystems APPDATA-Dateien durchlaufen, die am Roaming-Speicherort gespeichert sind. Andere Speicherorte für die Speicherung dateibasierter Daten werden nicht von einem Computer zu einem Computer durchlaufen, da Sie sich an Speicherorten befinden, die nicht durchlaufen werden.

### <a href="" id="bkmk-clt-inter-roam-reqs"></a>Roaming-Anforderungen und Datenspeicher für Benutzer Kataloge

App-V speichert Daten, die den Zustand des Katalogs des Benutzers darstellen, in der folgenden Form:

-   Dateien unter%APPDATA%\\Microsoft\\AppV\\Client\\Catalog

-   Registrierungseinstellungen unter `HKEY_CURRENT_USER\Software\Microsoft\AppV\Client\Packages`

Zusammenstellen diese Dateien und Registrierungseinstellungen den Katalog des Benutzers dar, sodass entweder beide Roaming durchgeführt werden müssen, oder dass für einen bestimmten Benutzer kein Roaming durchgeführt werden muss. App-V unterstützt kein Roaming von% APPDATA%, aber nicht das Roaming des Benutzerprofils (Registrierung) oder umgekehrt.

**Hinweis**  Das Cmdlet **Repair-AppvClientPackage** repariert den Veröffentlichungsstatus von Paketen nicht, wobei der App-V-Zustand des Benutzers unter `HKEY_CURRENT_USER` fehlt oder mit den Daten in% APPDATA% nicht übereinstimmt.

 

### Registrierungsbasierte Daten

Das App-V-Registrierungs-Roaming fällt in zwei Szenarien, wie in der folgenden Tabelle dargestellt.

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
<td align="left"><p>Wenn ein Standardbenutzer eine APP-v-Anwendung startet, werden sowohl HKLM-als auch HKCU für App-v-Anwendungen in der HKCU-Struktur auf dem Computer gespeichert. Dies stellt zwei unterschiedliche Pfade dar:</p>
<ul>
<li><p>HKLM: HKCU\SOFTWARE\Classes\AppV\Client\Packages {PkgGUID} \ REGISTRY\MACHINE\SOFTWARE</p></li>
<li><p>HKCU: HKCU\SOFTWARE\Microsoft\AppV\Client\Packages {PkgGUID} \ REGISTRY\USER {Benutzer-Nr} \ Software</p></li>
</ul>
<p>Die Speicherorte sind für das Roaming auf der Grundlage der Betriebssystemeinstellungen aktiviert.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Anwendungen, die mit Elevation ausgeführt werden</p></td>
<td align="left"><p>Wenn eine Anwendung mit Elevation gestartet wird:</p>
<ul>
<li><p>HKLM-Daten werden in der HKLM-Struktur auf dem lokalen Computer gespeichert.</p></li>
<li><p>HKCU-Daten werden am Speicherort der Benutzerregistrierung gespeichert</p></li>
</ul>
<p>In diesem Szenario werden diese Einstellungen nicht mit normalen Roaming-Konfigurationen des Betriebssystems durchlaufen, und die resultierenden Registrierungsschlüssel und-Werte werden an folgendem Speicherort gespeichert:</p>
<ul>
<li><p>HKLM\SOFTWARE\Microsoft\AppV\Client\Packages {PkgGUID} {Benutzer-Nr} \ REGISTRY\MACHINE\SOFTWARE</p></li>
<li><p>HKCU\SOFTWARE\Microsoft\AppV\Client\Packages {PkgGUID} \ Registry\User {Benutzer-Nr} \ Software</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

### App-V und Ordnerumleitung

App-V 5,1 unterstützt die Ordnerumleitung des Roaming-APPDATA-Ordners (% APPDATA%). Wenn die virtuelle Umgebung gestartet wird, wird der Roaming-APPDATA-Zustand aus dem Roaming-AppData-Verzeichnis des Benutzers in den lokalen Cache kopiert. Umgekehrt wird beim Beenden der virtuellen Umgebung der lokale Cache, der dem Roaming-APPDATA eines bestimmten Benutzers zugeordnet ist, an den tatsächlichen Speicherort des Roaming-APPDATA-Verzeichnisses dieses Benutzers übertragen.

Ein typisches Paket enthält mehrere Speicherorte, die im Sicherungsspeicher des Benutzers für Einstellungen in AppData\\Local und AppData\\Roaming. zugeordnet sind. Bei diesen Speicherorten handelt es sich um die Kopie an Schreib Speicherorten, die pro Benutzer im Profil des Benutzers gespeichert werden und die zum Speichern von Änderungen an den Paket-VFS-Verzeichnissen und zum Schutz des Standardpakets VFS verwendet werden.

In der folgenden Tabelle sind lokale und Roaming-Speicherorte aufgeführt, wenn die Ordnerumleitung nicht implementiert wurde.

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
<td align="left"><p>C:\users\jsmith\AppData &lt; Strong &gt; local </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID- &gt; \ProgramFilesX86</p></td>
</tr>
<tr class="even">
<td align="left"><p>SystemX86</p></td>
<td align="left"><p>C:\users\jsmith\AppData &lt; Strong &gt; local </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID- &gt; \SystemX86</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows</p></td>
<td align="left"><p>C:\users\jsmith\AppData &lt; Strong &gt; local </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt;</p></td>
</tr>
<tr class="even">
<td align="left"><p>appv_ROOT</p></td>
<td align="left"><p>C:\users\jsmith\AppData &lt; Strong &gt; local </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \ appv_ROOT</p></td>
</tr>
<tr class="odd">
<td align="left"><p>APPDATA</p></td>
<td align="left"><p>C:\users\jsmith\AppData &lt; Strong &gt; Roaming </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID- &gt; \AppData</p></td>
</tr>
</tbody>
</table>

 

 

In der folgenden Tabelle sind lokale und Roaming-Speicherorte aufgeführt, wenn die Ordnerumleitung für% APPDATA% implementiert wurde und der Standort umgeleitet wurde (in der Regel an einen Netzwerkspeicherort).

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
<td align="left"><p>C:\users\jsmith\AppData &lt; Strong &gt; local </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID- &gt; \ProgramFilesX86</p></td>
</tr>
<tr class="even">
<td align="left"><p>SystemX86</p></td>
<td align="left"><p>C:\users\jsmith\AppData &lt; Strong &gt; local </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID- &gt; \SystemX86</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows</p></td>
<td align="left"><p>C:\users\jsmith\AppData &lt; Strong &gt; local </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt;</p></td>
</tr>
<tr class="even">
<td align="left"><p>appv_ROOT</p></td>
<td align="left"><p>C:\users\jsmith\AppData &lt; Strong &gt; local </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \ appv_ROOT</p></td>
</tr>
<tr class="odd">
<td align="left"><p>APPDATA</p></td>
<td align="left"><p><strong>\Fileserver </strong> \users\jsmith\roaming\Microsoft\AppV\Client\VFS &amp; lt; GUID- &gt; \AppData</p></td>
</tr>
</tbody>
</table>

 

 

Der aktuelle App-v-Client-VFS-Treiber kann nicht in Netzwerkspeicherorte schreiben, sodass der APP-v-Client das vorhanden sein einer Ordnerumleitung erkennt und die Daten auf dem lokalen Laufwerk während der Veröffentlichung und beim Starten der virtuellen Umgebung kopiert. Nachdem der Benutzer die APP-v-Anwendung geschlossen hat und der APP-v-Client die virtuelle Umgebung geschlossen hat, wird der lokale Speicher des VFS-APPDATA wieder in das Netzwerk kopiert, sodass Roaming auf weiteren Computern möglich ist, in denen der Vorgang wiederholt wird. Die detaillierten Schritte der Prozesse sind:

1.  Während des Starts der Veröffentlichung oder virtuellen Umgebung erkennt der App-V-Client den Speicherort des APPDATA-Verzeichnisses.

2.  Wenn der Roaming-APPDATA-Pfad lokal ist oder Ino AppData\\Roaming Standort zugeordnet ist, geschieht nichts.

3.  Wenn der Roaming-APPDATA-Pfad nicht lokal ist, wird das VFS-AppData-Verzeichnis dem lokalen AppData-Verzeichnis zugeordnet.

Durch diesen Vorgang wird das Problem eines nicht lokalen% APPDATA% behoben, das vom App-V-Client-VFS-Treiber nicht unterstützt wird. Die in diesem neuen Speicherort gespeicherten Daten werden jedoch nicht mit der Ordnerumleitung durchlaufen. Alle Änderungen während der Ausführung der Anwendung erfolgen am lokalen APPDATA-Speicherort und müssen in den umgeleiteten Speicherort kopiert werden. Die detaillierten Schritte dieses Prozesses sind:

1.  App-V-Anwendung wird heruntergefahren, wodurch die virtuelle Umgebung beendet wird.

2.  Der lokale Cache des Roaming-APPDATA-Speicherorts wird komprimiert und in einer ZIP-Datei gespeichert.

3.  Ein Zeitstempel am Ende des ZIP-Verpackungsprozesses wird verwendet, um die Datei zu benennen.

4.  Der Zeitstempel wird in der Registrierung aufgezeichnet: HKEY \ _CURRENT \ _User \\software\\microsoft\\appv\\client\\packages\\ &lt; GUID &gt; \\AppDataTime als letzten bekannten APPDATA-Zeitstempel.

5.  Der Ordner-Umleitungsprozess wird aufgerufen, um die ZIP-Datei auszuwerten und zu initiieren, die in das Roaming AppData-Verzeichnis hochgeladen wurde.

Der timestamp wird verwendet, um ein Szenario des letzten Writer-WINS-Szenarios zu ermitteln, wenn ein Konflikt vorliegt, der zum Optimieren des Downloads der Daten verwendet wird, wenn die App-V-Anwendung veröffentlicht wird oder die virtuelle Umgebung gestartet wird. Durch die Ordnerumleitung werden die Daten von allen anderen Clients zur Verfügung gestellt, die unter die unterstützende Richtlinie fallen, und der Vorgang zum Speichern der AppData\\Roaming-Daten am lokalen APPDATA-Speicherort auf dem Client wird initiiert. Die detaillierten Prozesse sind:

1.  Der Benutzer startet die virtuelle Umgebung, indem er eine Anwendung startet.

2.  Die virtuelle Umgebung der Anwendung überprüft, falls vorhanden, die neueste ZIP-Datei mit Zeitstempel.

3.  Sofern vorhanden, wird die Registrierung auf den letzten bekannt geladenen Timestamp überprüft.

4.  Die neueste ZIP-Datei wird heruntergeladen, es sei denn, der lokale letzte bekannte Upload-Zeitstempel ist größer als oder gleich dem Timestamp aus der ZIP-Datei.

5.  Wenn der lokale letzte bekannte Upload-Zeitstempel vor der letzten ZIP-Datei im Roaming-APPDATA-Speicherort liegt, wird die ZIP-Datei in das lokale temporäre Verzeichnis im Profil des Benutzers extrahiert.

6.  Nachdem die ZIP-Datei erfolgreich extrahiert wurde, wird der lokale Cache des Roaming-APPDATA-Verzeichnisses umbenannt, und die neuen Daten werden in Position verschoben.

7.  Das umbenannte Verzeichnis wird gelöscht, und die Anwendung wird mit den zuletzt gespeicherten Roaming-APPDATA-Daten geöffnet.

Dadurch wird das erfolgreiche Roaming von Anwendungseinstellungen abgeschlossen, die in AppData\\Roaming-Speicherorten vorhanden sind. Die einzige andere Bedingung, die behoben werden muss, ist ein Paket Reparaturvorgang. Die Details des Prozesses lauten wie folgt:

1.  Ermitteln Sie während der Reparatur, ob der Pfad zum Roaming-AppData-Verzeichnis des Benutzers nicht lokal ist.

2.  Karte die nicht lokalen Roaming-APPDATA-Pfad Ziele werden die erwarteten Roaming-und lokalen APPDATA-Speicherorte neu erstellt.

3.  Löschen Sie den in der Registrierung gespeicherten Zeitstempel, falls vorhanden.

Durch diesen Vorgang werden sowohl die lokale als auch die Netzwerkspeicherorte für APPDATA neu erstellt, und der Registrierungseintrag des Zeitstempels wird entfernt.

## <a href="" id="bkmk-clt-app-lifecycle"></a>App-V Client Application Lifecycle Management


In einer vollständigen APP-v-Infrastruktur werden nach der Sequenzierung von Anwendungen verwaltet und auf Benutzern oder Computern über die APP-v-Verwaltungs-und Veröffentlichungsserver veröffentlicht. In diesem Abschnitt werden die Vorgänge erläutert, die während der gemeinsamen App-v-Anwendungslebenszyklus Vorgänge (hinzufügen, veröffentlichen, starten, aktualisieren und entfernen) sowie der Datei-und Registrierungsspeicherorte auftreten, die aus der Perspektive des App-v-Clients geändert und geändert werden. Die APP-v-Client Vorgänge werden als eine Reihe von PowerShell-Befehlen ausgeführt, die auf dem Computer mit dem App-v-Client initiiert wurden.

Dieses Dokument befasst sich mit den vollständigen Infrastrukturlösungen von App V. Spezifische Informationen zur App-V-Integration in Configuration Manager 2012 finden Sie unter: <https://go.microsoft.com/fwlink/?LinkId=392773> .

Die Aufgaben des App-V-Anwendungslebenszyklus werden bei der Benutzeranmeldung (Standardeinstellung), beim Start des Computers oder als zeitgesteuerte Vorgänge im Hintergrund ausgelöst. Die Einstellungen für die App-V-Client Vorgänge, einschließlich Veröffentlichungsserver, Aktualisierungsintervalle, Paket Skriptaktivierung und andere, werden während des Setups des Clients oder nach dem Setup mit PowerShell-Befehlen konfiguriert. Weitere Informationen finden Sie unter Vorgehensweise zum Bereitstellen des Clients auf der TechNet-Seite unter: [Bereitstellen des App-V-Clients](how-to-deploy-the-app-v-client-51gb18030.md) oder verwenden der PowerShell:

```powershell
get-command *appv*
```

### Veröffentlichungsaktualisierung

Der Veröffentlichungs Aktualisierungsprozess umfasst mehrere kleinere Vorgänge, die auf dem App-V-Client ausgeführt werden. Da es sich bei App-V um eine Application Virtualization-Technologie und nicht um eine Vorgangs Planungstechnologie handelt, wird der Windows-Taskplaner verwendet, um den Prozess bei der Benutzeranmeldung, beim Starten des Computers und in geplanten Intervallen zu aktivieren. Die Konfiguration des Clients während des oben aufgeführten Setups ist die bevorzugte Methode beim Verteilen des Clients an eine große Gruppe von Computern mit den richtigen Einstellungen. Diese Clienteinstellungen können mit den folgenden PowerShell-Cmdlets konfiguriert werden:

-   **Add-AppVPublishingServer:** Konfiguriert den Client mit einem App-v-Veröffentlichungs Server, der APP-v-Pakete bereitstellt.

-   **Satz-AppVPublishingServer:** Ändert die aktuellen Einstellungen für den App-V-Veröffentlichungs Server.

-   **Satz-AppVClientConfiguration:** Ändert die aktuelle Einstellungen für den App-V-Client.

-   **Sync-AppVPublishingServer:** Initiiert einen Aktualisierungsvorgang für die App-V-Veröffentlichung manuell. Dies wird auch in den geplanten Aufgaben verwendet, die während der Konfiguration des Veröffentlichungsservers erstellt wurden.

Im Fokus der folgenden Abschnitte finden Sie Informationen zu den Vorgängen, die in verschiedenen Phasen einer App-V-Veröffentlichungsaktualisierung ausgeführt werden. Zu den Themen gehören:

-   Hinzufügen eines App-V-Pakets

-   Veröffentlichen eines App-V-Pakets

### Hinzufügen eines App-V-Pakets

Das Hinzufügen eines App-V-Pakets zum Client ist der erste Schritt des Veröffentlichungs Aktualisierungsprozesses. Das Endergebnis ist mit dem `Add-AppVClientPackage` Cmdlet in PowerShell identisch, mit der Ausnahme, dass der konfigurierte Veröffentlichungsserver mit Ausnahme des Veröffentlichungs Aktualisierungs Add-Vorgangs kontaktiert wird und eine Liste der Anwendungen auf höherer Ebene zurück an den Client übergibt, um detailliertere Informationen und nicht einen einzelnen Paket-Add-Vorgang abzurufen. Der Prozess wird fortgesetzt, indem der Client für Paket-oder Verbindungsgruppen Erweiterungen oder-Updates konfiguriert und dann auf die AppV-Datei zugegriffen wird. Als nächstes werden die Inhalte der AppV-Datei erweitert und auf dem lokalen Betriebssystem an den entsprechenden Speicherorten gespeichert. Im folgenden finden Sie einen detaillierten Workflow des Prozesses, vorausgesetzt, das Paket ist für das Fehler Streaming konfiguriert.

**Hinzufügen eines App-V-Pakets**

1.  Manuelle Initiierung über PowerShell oder Task Sequenz Initiierung des Veröffentlichungs Aktualisierungsprozesses.

    1.  Der App-V-Client erstellt eine HTTP-Verbindung und fordert eine Liste der auf dem Ziel basierenden Anwendungen an. Der Veröffentlichungs Aktualisierungsprozess unterstützt die Zielgruppenadressierung von Computern oder Benutzern.

    2.  Der App-V-Veröffentlichungs Server verwendet die Identität des initiierenden Ziels, Benutzers oder Computers und fragt die Datenbank nach einer Liste der berechtigten Anwendungen ab. Die Liste der Anwendungen wird als XML-Antwort bereitgestellt, die der Client zum Senden zusätzlicher Anforderungen an den Server verwendet, um weitere Informationen pro Paket zu erhalten.

2.  Der Veröffentlichungs-Agent auf dem App-V-Client führt alle unter serialisierten Aktionen aus.

    Bewerten Sie alle Verbindungsgruppen, die nicht veröffentlicht oder deaktiviert sind, da Paketversions Updates, die Teil der Verbindungsgruppe sind, nicht verarbeitet werden können.

3.  Konfigurieren Sie die Pakete, indem Sie einen Add-oder Update-Vorgang identifizieren.

    1.  Der App-V-Client verwendet die AppX-API von Windows und greift auf die AppV-Datei vom Veröffentlichungsserver zu.

    2.  Die Paketdatei wird geöffnet, und die AppXManifest.xml und StreamMap.xml werden in den Paketspeicher heruntergeladen.

    3.  Vollständiges Streamen von Veröffentlichungs Blockdaten, die im StreamMap.xml definiert sind. Speichert die Veröffentlichungs Blockdaten im Paket Store\\PkgGUID\\VerGUID\\Root.

        -   Symbole: Ziele von Erweiterungspunkten.

        -   Portable ausführbare Header (PE-Header): Ziele von Erweiterungspunkten, die die Basisinformationen zum Bild benötigen, auf einem Datenträger, auf den direkt zugegriffen wird, oder über Dateitypen.

        -   Skripts: Download des Skripts-Verzeichnisses zur Verwendung im gesamten Veröffentlichungsprozess.

    4.  Füllen Sie den Paketspeicher aus:

        1.  Erstellen Sie Dateien mit geringer Dichte auf einem Datenträger, die das extrahierte Paket für alle aufgelisteten Verzeichnisse darstellen.

        2.  Stufen Sie Dateien und Verzeichnisse der obersten Ebene unter root ein.

        3.  Alle anderen Dateien werden erstellt, wenn das Verzeichnis auf dem Datenträger als "spärlich" aufgeführt und bei Bedarf gestreamt wird.

    5.  Erstellen Sie die Einträge des Computer Katalogs. Erstellen Sie die Manifest.xml und DeploymentConfiguration.xml aus den Paketdateien (wenn keine DeploymentConfiguration.xml Datei im Paket ein Platzhalter erstellt wird).

    6.  Erstellen des Speicherorts des Paketspeichers in der Registrierungs-HKLM\\Software\\Microsoft\\AppV\\Client\\Packages\\PkgGUID\\Versions\\VerGUID\\Catalog

    7.  Erstellen Sie die Datei "Registry. dat" aus dem Paketspeicher auf%ProgramData%\\Microsoft\\AppV\\Client\\VReg\\ {VersionGUID}. dat

    8.  Registrieren des Pakets mit dem App-V-Kernel Modus-Treiber HKLM\\Microsoft\\Software\\AppV\\MAV

    9.  Rufen Sie Skripting aus der AppxManifest.xml oder DeploymentConfig.xml Datei auf, um die Anzeigedauer für das Paket hinzuzufügen.

4.  Konfigurieren Sie Verbindungsgruppen durch Hinzufügen und aktivieren oder deaktivieren.

5.  Entfernen Sie Objekte, die nicht auf dem Ziel veröffentlicht sind (Benutzer oder Computer).

    **Hinweis**  Dadurch wird keine Paketlöschung durchgeführt, sondern es werden vielmehr Integrationspunkte für das jeweilige Ziel (Benutzer oder Computer) entfernt und Benutzer Katalogdateien (Computer Katalogdateien für Global veröffentlicht) entfernt.

     

6.  Aufrufen der Hintergrund Lade Montage auf der Grundlage der Clientkonfiguration.

7.  Pakete, die bereits Veröffentlichungsinformationen für den Computer oder Benutzer aufweisen, werden sofort wiederhergestellt.

    **Hinweis**  Diese Bedingung tritt als ein Produkt der Entfernung auf, ohne die Veröffentlichung mit Hintergrund Addition des Pakets aufzuheben.

     

Damit ist ein App-V-Paket zum Veröffentlichen des Aktualisierungsprozesses abgeschlossen. Im nächsten Schritt wird das Paket auf dem jeweiligen Ziel (Computer oder Benutzer) veröffentlicht.

![Paket zum Hinzufügen von Datei-und Registrierungsdaten](images/packageaddfileandregistrydata.png)

### Veröffentlichen eines App-V-Pakets

Während des Veröffentlichungs Aktualisierungsvorgangs fügt der jeweilige Veröffentlichungsvorgang (Publish-AppVClientPackage) dem Benutzer Katalogeinträge hinzu, ordnet dem Benutzer den Berechtigungen zu, identifiziert den lokalen Speicher und beendet die einzelnen Integrationsschritte. Im folgenden finden Sie die detaillierten Schritte.

**Veröffentlichen und App-V-Paket**

1.  Dem Benutzer Katalog werden Paket Einträge hinzugefügt.

    1.  Benutzerorientierte Pakete: die UserDeploymentConfiguration.xml und UserManifest.xml werden auf dem Computer im Benutzer Katalog gespeichert.

    2.  Maschinell ausgerichtete (globale) Pakete: die UserDeploymentConfiguration.xml wird im Computer Katalog gespeichert.

2.  Registrieren des Pakets mit dem Kernelmodus-Treiber für den Benutzer unter HKLM\\Software\\Microsoft\\AppV\\MAV

3.  Durchführen von Integrationsaufgaben

    1.  Erstellen Sie Erweiterungspunkte.

    2.  Speichern von Sicherungsinformationen in der Registrierung und im Roaming-Profil des Benutzers (Verknüpfungs Sicherungen).

        **Hinweis**  Dies ermöglicht das Wiederherstellen von Erweiterungspunkten, wenn das Paket nicht veröffentlicht wurde.

         

    3.  Führen Sie Skripts aus, die für die Veröffentlichungs Anzeige vorgesehen sind.

Das Veröffentlichen eines App-V-Pakets, das Teil einer Verbindungsgruppe ist, ähnelt dem oben beschriebenen Verfahren. Für Verbindungsgruppen enthält der Pfad, in dem die spezifischen Kataloginformationen gespeichert sind, PackageGroups als untergeordnetes Element des Katalog Verzeichnisses. Weitere Informationen finden Sie in den Kataloginformationen zu Computer und Benutzern oben.

![Paketdatei-und Registrierungsdaten hinzufügen – Global](images/packageaddfileandregistrydata-global.png)

### Anwendungsstart

Nach dem Veröffentlichungs Aktualisierungsvorgang startet der Benutzer eine App-V-Anwendung und startet Sie anschließend erneut. Der Vorgang ist sehr einfach und für einen schnellen Start mit einem mindestnetzwerkverkehr optimiert. Der App-V-Client überprüft den Pfad zu dem Benutzer Katalog für Dateien, die während der Veröffentlichung erstellt wurden. Nachdem die Rechte zum Starten des Pakets festgelegt wurden, erstellt der App-V-Client eine virtuelle Umgebung, beginnt mit dem Streaming aller erforderlichen Daten und wendet die entsprechenden Manifest-und Bereitstellungskonfigurationsdateien während der Erstellung der virtuellen Umgebung an. Bei der Erstellung und Konfiguration der virtuellen Umgebung für das jeweilige Paket und die Anwendung wird die Anwendung gestartet.

**Starten von App-V-Anwendungen**

1.  Der Benutzer startet die Anwendung durch Klicken auf einen Verknüpfungs-oder Dateityp Aufruf.

2.  Der App-V-Client überprüft die Existenz im Benutzer Katalog für die folgenden Dateien:

    -   UserDeploymentConfiguration.xml

    -   UserManifest.xml

3.  Wenn die Dateien vorhanden sind, ist die Anwendung für diesen bestimmten Benutzer berechtigt, und die Anwendung startet den Vorgang für den Start. An diesem Punkt ist kein Netzwerkdatenverkehr vorhanden.

4.  Als nächstes überprüft der APP-v-Client, ob sich der Pfad für das für den App-v-Client Dienst registrierte Paket in der Registrierung befindet.

5.  Nachdem Sie den Pfad zum Paketspeicher gefunden haben, wird die virtuelle Umgebung erstellt. Wenn es sich um den ersten Start handelt, blockiert das primäre Feature Downloads, falls vorhanden.

6.  Nach dem Download verbraucht der APP-v-Client Dienst die Konfigurationsdateien für Manifest und Bereitstellung, um die virtuelle Umgebung zu konfigurieren, und alle App-v-Subsysteme werden geladen.

7.  Die Anwendung wird gestartet. Für alle fehlenden Dateien im Paketspeicher (Sparse-Dateien) streamt App-V Fehler Dateien nach Bedarf.

    ![Paket zum Hinzufügen von Datei-und Registrierungsdaten strömen](images/packageaddfileandregistrydata-stream.png)

### Aktualisieren eines App-V-Pakets

Das Upgrade des App-v 5-Pakets unterscheidet sich von den älteren Versionen von App-v. App-V unterstützt mehrere Versionen desselben Pakets auf einem Computer, der für verschiedene Benutzer berechtigt ist. Paketversionen können jederzeit hinzugefügt werden, wenn der Paketspeicher und die Kataloge mit den neuen Ressourcen aktualisiert werden. Der einzige für das Hinzufügen neuer Versionsressourcen spezifischer Prozess ist die Speicheroptimierung. Während eines Upgrades werden nur die neuen Dateien zum neuen Versionsspeicher Standort hinzugefügt, und es werden harte Links für unveränderte Dateien erstellt. Dadurch wird der Gesamtspeicher reduziert, indem die Datei nur auf einem Datenträger gespeichert und dann in alle Ordner mit einem Dateispeicherort Eintrag auf dem Datenträger projiziert wird. Die speziellen Details zum Upgrade eines App-V-Pakets lauten wie folgt:

**Aktualisieren eines App-V-Pakets**

1.  Der APP-v-Client führt eine Veröffentlichungsaktualisierung durch und ermittelt eine neuere Version eines App-v-Pakets.

2.  Paket Einträge werden dem entsprechenden Katalog für die neue Version hinzugefügt.

    1.  Benutzerorientierte Pakete: die UserDeploymentConfiguration.xml und UserManifest.xml werden auf dem Computer im Benutzer Katalog unter appdata\\roaming\\Microsoft\\AppV\\Client\\Catalog\\Packages\\PkgGUID\\VerGUID

    2.  Maschinell ausgerichtete (globale) Pakete: die UserDeploymentConfiguration.xml wird im Computer Katalog unter%ProgramData%\\Microsoft\\AppV\\Client\\Catalog\\Packages\\PkgGUID\\VerGUID gespeichert.

3.  Registrieren des Pakets mit dem Kernelmodus-Treiber für den Benutzer unter HKLM\\Software\\Microsoft\\AppV\\MAV

4.  Durchführen von Integrationsaufgaben

    -   Integrieren Sie Erweiterungspunkte (EP) aus den Manifesten und dynamischen Konfigurationsdateien.

    1.  Dateibasierte EP-Daten werden im AppData-Ordner unter Verwendung von Abzweigungspunkten aus dem Paketspeicher gespeichert.

    2.  Version 1 EPS ist bereits vorhanden, wenn eine neue Version verfügbar ist.

    3.  Die Erweiterungspunkte werden in Maschinen-oder Benutzer Katalogen für neuere oder aktualisierte Erweiterungspunkte auf den Standort Version 2 umgeschaltet.

5.  Führen Sie Skripts aus, die für die Veröffentlichungs Anzeige vorgesehen sind.

6.  Installieren Sie nebeneinander angeordnete Assemblys nach Bedarf.

### Aktualisieren eines in-use-App-V-Pakets

**Ab App-V 5 SP2**: Wenn Sie versuchen, ein Paket zu aktualisieren, das von einem Endbenutzer verwendet wird, wird die Aktualisierungsaufgabe in einem ausstehenden Zustand gespeichert. Das Upgrade wird später entsprechend den folgenden Regeln ausgeführt:

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
<td align="left"><p>Benutzerbasierte Aufgaben, beispielsweise die Veröffentlichung eines Pakets für einen Benutzer</p></td>
<td align="left"><p>Die ausstehende Aufgabe wird ausgeführt, nachdem sich der Benutzer abgemeldet hat und sich dann wieder anmeldet.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Global basierender Vorgang, beispielsweise Aktivieren einer Verbindungsgruppe Global</p></td>
<td align="left"><p>Die ausstehende Aufgabe wird ausgeführt, wenn der Computer heruntergefahren und neu gestartet wird.</p></td>
</tr>
</tbody>
</table>

 

Wenn eine Aufgabe in einem ausstehenden Zustand befindet, generiert der App-V-Client auch einen Registrierungsschlüssel für die ausstehende Aufgabe wie folgt:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Benutzerbasierter oder Global basierter Vorgang</th>
<th align="left">Ort, an dem der Registrierungsschlüssel generiert wird</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Benutzerbasierte Aufgaben</p></td>
<td align="left"><p>KEY_CURRENT_USER \software\microsoft\appv\client\pendingtasks</p></td>
</tr>
<tr class="even">
<td align="left"><p>Global basierte Aufgaben</p></td>
<td align="left"><p>HKEY_LOCAL_MACHINE \software\microsoft\appv\client\pendingtasks</p></td>
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
<td align="left"><p>Diese Aufgabe ist Computer spezifisch, und Sie können Sie jederzeit durchführen, indem Sie die Schritte im Abschnitt Paket hinzufügen oben ausführen.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Veröffentlichen des Pakets</p></td>
<td align="left"><p>Weitere Informationen finden Sie im Abschnitt Paket Veröffentlichung oben unter Schritte. Dieser Vorgang erfordert, dass Sie Erweiterungspunkte auf dem System aktualisieren. Endbenutzer können die Anwendung nicht verwenden, wenn Sie diese Aufgabe ausführen.</p></td>
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
<td align="left"><p>Das App-V-Paket wird nicht verwendet, wenn Sie versuchen, ein Upgrade durchzuführen.</p></td>
<td align="left"><p>Keine der folgenden Komponenten des Pakets kann verwendet werden: virtuelle Anwendung, com-Server oder Shell-Erweiterungen.</p>
<p>Der Administrator veröffentlicht eine neuere Version des Pakets, und das Upgrade funktioniert, wenn eine Komponente oder Anwendung innerhalb des Pakets das nächste Mal gestartet wird. Die neue Version des Pakets wird gestreamt und ausgeführt. In diesem Szenario wurde in App-v 5 SP2 aus früheren Versionen von App-v 5 nichts geändert.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Das App-V-Paket wird verwendet, wenn der Administrator eine neuere Version des Pakets veröffentlicht.</p></td>
<td align="left"><p>Der Aktualisierungsvorgang wird vom App-V-Client auf Ausstehend festgesetzt, was bedeutet, dass er in die Warteschlange gestellt und später ausgeführt wird, wenn das Paket nicht verwendet wird.</p>
<p>Wenn die Paketanwendung verwendet wird, fährt der Benutzer die virtuelle Anwendung herunter, nach der das Upgrade ausgeführt werden kann.</p>
<p>Wenn das Paket über Shell-Erweiterungen (Office 2013) verfügt, die vom Windows-Explorer dauerhaft geladen werden, kann der Benutzer nicht angemeldet werden. Benutzer müssen sich ab-und wieder anmelden, um das App-V-PaketUpgrade zu initiieren.</p></td>
</tr>
</tbody>
</table>

 

### Global vs User Publishing

App-V-Pakete können auf eine von zwei Arten veröffentlicht werden. Benutzer, der ein App-v-Paket für einen bestimmten Benutzer oder eine Gruppe von Benutzern und Global anrechtet, das das App-v-Paket für alle Benutzer des Computers zum gesamten Computer berechtigt. Nachdem ein PaketUpgrade vorangestellt wurde und das App-V-Paket nicht verwendet wird, sollten Sie die beiden Arten der Veröffentlichung in Frage stellen:

-   **Global veröffentlicht**: die Anwendung wird auf einem Computer veröffentlicht. alle Benutzer auf diesem Computer können Sie verwenden. Das Upgrade wird durchgeführt, wenn der App-V-Client Dienst gestartet wird, was effektiv einen Neustart des Computers bedeutet.

-   **Benutzer veröffentlicht**: die Anwendung wird für einen Benutzer veröffentlicht. Wenn auf dem Computer mehrere Benutzer vorhanden sind, kann die Anwendung in einer Teilmenge der Benutzer veröffentlicht werden. Das Upgrade erfolgt, wenn sich der Benutzer anmeldet oder wenn er erneut veröffentlicht wird (regelmäßige Aktualisierung und Auswertung der ConfigMgr-Richtlinie oder regelmäßige Veröffentlichung/Aktualisierung von App-V oder explizit über PowerShell-Befehle).

### Entfernen eines App-V-Pakets

Das Entfernen von App-V-Anwendungen in einer vollständigen Infrastruktur ist eine Veröffentlichungsoperation, bei der keine Paketentfernung durchgeführt wird. Der Prozess ist derselbe wie der obige Veröffentlichungsprozess, doch anstelle des Hinzufügens des Entfernungsprozesses werden die Änderungen, die für App-V-Pakete vorgenommen wurden, umgekehrt.

### Reparieren eines App-V-Pakets

Der Reparaturvorgang ist sehr einfach, kann sich aber auf viele Speicherorte auf dem Computer auswirken. Die zuvor erwähnten Exemplare auf Write (Cow)-Speicherorten werden entfernt, und Erweiterungspunkte werden deintegriert und dann wieder integriert. Überprüfen Sie die Position der Cow-Daten Platzierungen, indem Sie überprüfen, wo Sie in der Registrierung registriert sind. Dieser Vorgang erfolgt automatisch, und es gibt keine andere administrative Steuerung als das Initiieren eines Reparaturvorgangs über die App-V-Client Konsole oder über PowerShell (Repair-AppVClientPackage).

## <a href="" id="bkmk-integr-appv-pkgs"></a>Integration von App-V-Paketen


Die App-V-Client-und-Paketarchitektur bietet beim Hinzufügen und Veröffentlichen von Paketen eine spezifische Integration in das lokale Betriebssystem. Drei Dateien definieren die Integrations-oder Erweiterungspunkte für ein App-V-Paket:

-   AppXManifest.xml: innerhalb des Pakets mit Fall Back Kopien gespeichert, die im Paketspeicher und im Benutzerprofilgespeichert sind. Enthält die während des Sequenz Prozesses erstellten Optionen.

-   DeploymentConfig.xml: enthält Konfigurationsinformationen zu Erweiterungspunkten für Computer-und benutzerbasierte Integrationen.

-   UserConfig.xml: eine Teilmenge der Deploymentconfig.xml, die nur benutzerbasierte Konfigurationen bereitstellt und nur auf benutzerbasierte Erweiterungspunkte ausgerichtet ist.

### Regeln für die Integration

Wenn App-v-Anwendungen auf einem Computer mit dem App-v-Client veröffentlicht werden, finden einige spezifische Aktionen statt, wie in der folgenden Liste beschrieben:

-   Global Publishing: Verknüpfungen werden im Profilspeicherort alle Benutzer gespeichert, und andere Erweiterungspunkte werden in der Registrierung in der HKLM-Struktur gespeichert.

-   Benutzer Veröffentlichung: Verknüpfungen werden im aktuellen Benutzerkontoprofil gespeichert, und andere Erweiterungspunkte werden in der Registrierung in der HKCU-Struktur gespeichert.

-   Sicherung und Wiederherstellung: vorhandene systemeigene Anwendungsdaten und Registrierung (wie FTA-Registrierungen) werden während der Veröffentlichung gesichert.

    1.  App-v-Pakete erhalten den Besitz auf der Grundlage des letzten integrierten Pakets, in dem der Besitz an die neueste veröffentlichte App-v-Anwendung übergeben wird.

    2.  Besitzer Übertragungen von einem App-v-Paket zu einem anderen, wenn das besitzende App-v-Paket nicht veröffentlicht wurde. Dadurch wird keine Wiederherstellung der Daten oder der Registrierung initiiert.

    3.  Wiederherstellen der gesicherten Daten, wenn das letzte Paket unveröffentlicht oder auf einer Basis für die Erweiterung entfernt wurde.

### Erweiterungspunkte

Die App-V-Veröffentlichungsdateien (Manifest und dynamische Konfiguration) bieten mehrere Erweiterungspunkte, mit denen die Anwendung in das lokale Betriebssystem integriert werden kann. Diese Erweiterungspunkte führen typische Anwendungs Installationsaufgaben aus, beispielsweise das Platzieren von Verknüpfungen, das Erstellen von Dateitypzuordnungen und das Registrieren von Komponenten. Da es sich um virtualisierte Anwendungen handelt, die nicht auf die gleiche Weise wie eine herkömmliche Anwendung installiert sind, gibt es einige Unterschiede. Im folgenden finden Sie eine Liste der in diesem Abschnitt behandelten Erweiterungspunkte:

-   Kombinationen

-   Dateitypzuordnungen

-   Shell-Erweiterungen

-   COM

-   Software-Clients

-   Anwendungsfunktionen

-   URL-Protokoll Handler

-   AppPath

-   Virtuelle Anwendung

### Kombinationen

Die Abkürzung ist eines der grundlegenden Elemente der Integration mit dem Betriebssystem und ist die Schnittstelle für die direkte Benutzereinführung einer App-V-Anwendung. Beim Veröffentlichen und Aufheben der Veröffentlichung von App-V-Anwendungen.

In den XML-Dateien des paketmanifests und der Dynamic Configuration-XML-Datei befindet sich der Pfad zu einer bestimmten ausführbaren Anwendung in einem Abschnitt ähnlich der folgenden:

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

Wie bereits erwähnt, werden die App-V-Tastenkombinationen standardmäßig im Profil des Benutzers basierend auf dem Aktualisierungsvorgang gespeichert. Im Profil "alle Benutzer" werden die Tastenkombinationen für globale Aktualisierung platziert, und die Benutzeraktualisierung speichert Sie im Profil des jeweiligen Benutzers. Die tatsächliche ausführbare Datei wird im Paketspeicher gespeichert. Der Speicherort der ICO-Datei ist eine Token-Position im App-V-Paket.

### Dateitypzuordnungen

Der APP-v-Client verwaltet die lokalen Dateitypzuordnungen während der Veröffentlichung, wodurch Benutzern die Verwendung von Dateityp aufrufen oder das Öffnen einer Datei mit einer speziell registrierten Erweiterung (DOCX) ermöglicht wird, um eine App-V-Anwendung zu starten. Dateitypzuordnungen sind in den Manifest-und dynamischen Konfigurationsdateien vorhanden, wie im folgenden Beispiel dargestellt:

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

**Hinweis**  In diesem Beispiel:

-   `<Name>.xdp</Name>` ist die Erweiterung

-   `<Name>AcroExch.XDPDoc</Name>` der ProgID-Wert (der auf die benachbarte ProgID zeigt)

-   `<CommandLine>"[{AppVPackageRoot}]\Reader\AcroRd32.exe" "%1"</CommandLine>` ist die Befehlszeile, die auf die ausführbare Anwendung verweist.

 

### -Shell-Erweiterungen

Shell-Erweiterungen werden während des Sequenz Prozesses automatisch in das Paket eingebettet. Wenn das Paket Global veröffentlicht wird, gibt die Shell-Erweiterung Benutzern dieselbe Funktionalität wie bei der lokalen Installation der Anwendung. Die Anwendung erfordert keine zusätzliche Einrichtung oder Konfiguration auf dem Client, um die Shell-Erweiterungsfunktion zu aktivieren.

**Voraussetzungen für die Verwendung von Shell-Erweiterungen:**

-   Pakete, die eingebettete Shell-Erweiterungen enthalten, müssen global veröffentlicht werden.

-   Die "Bitanzahl" der Anwendung, des Sequencers und des App-V-Clients müssen übereinstimmen, oder die Shell-Erweiterungen funktionieren nicht. Beispiel:

    -   Die Version der Anwendung ist 64-Bit.

    -   Der Sequencer wird auf einem 64-Bit-Computer ausgeführt.

    -   Das Paket wird an einen 64-Bit-App-V-Clientcomputer übermittelt.

In der folgenden Tabelle werden die unterstützten Shell-Erweiterungen angezeigt.

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
<td align="left"><p>Kontextmenü Handler</p></td>
<td align="left"><p>Fügt dem Kontextmenü Menüelemente hinzu. Sie wird aufgerufen, bevor das Kontextmenü angezeigt wird.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Drag & Drop-Handler</p></td>
<td align="left"><p>Steuert die Aktion beim Klicken mit der rechten Maustaste auf Drag & Drop und ändert das angezeigte Kontextmenü.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Ablegen eines Ziel Handlers</p></td>
<td align="left"><p>Steuert die Aktion, nachdem ein Datenobjekt gezogen und über ein Ablageziel wie eine Datei abgelegt wurde.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Datenobjekt-Handler</p></td>
<td align="left"><p>Steuert die Aktion, nachdem eine Datei in die Zwischenablage kopiert oder über ein Ablageziel gezogen und abgelegt wurde. Sie kann dem Ablageziel zusätzliche Zwischenablageformate zur Verfügung stellen.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Eigenschaftentabellen-Handler</p></td>
<td align="left"><p>Ersetzt oder fügt Seiten in das DialogfeldEigenschaften Fenster eines Objekts ein.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Infotipp-Handler</p></td>
<td align="left"><p>Ermöglicht das Abrufen von Flags und Infotipp-Informationen für ein Element und das Anzeigen des Elements in einer Popup-QuickInfo beim Mauszeiger.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Spalten Handler</p></td>
<td align="left"><p>Ermöglicht das Erstellen und Anzeigen benutzerdefinierter Spalten in der Windows-Explorer- <em> Detailansicht </em> . Sie kann zum Erweitern von Sortierung und Gruppierung verwendet werden.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Vorschauhandler</p></td>
<td align="left"><p>Ermöglicht das Anzeigen einer Vorschau einer Datei im Vorschaubereich von Windows-Explorer.</p></td>
</tr>
</tbody>
</table>

 

### COM

Der App-V-Client unterstützt Veröffentlichungs Anwendungen mit Unterstützung für com-Integration und-Virtualisierung. Die com-Integration ermöglicht es dem App-V-Client, com-Objekte auf dem lokalen Betriebssystem und die Virtualisierung der Objekte zu registrieren. Für die Zwecke dieses Dokuments erfordert die Integration von COM-Objekten zusätzliche Details.

App-V unterstützt das Registrieren von COM-Objekten aus dem Paket auf dem lokalen Betriebssystem mit zwei Prozesstypen: Out-of-Process-und in-Process-Prozesse. Das Registrieren von COM-Objekten erfolgt mit einer oder einer Kombination mehrerer Betriebsmodi für ein bestimmtes App-V-Paket, das aus, isoliert und integriert umfasst. Der integrierte Modus ist entweder für den Out-of-Process-oder in-Process-Typ konfiguriert. Die Konfiguration von com-Modi und-Typen erfolgt mit dynamischen Konfigurationsdateien (deploymentconfig.xml oder userconfig.xml).

Details zur App-V-Integration finden Sie unter: <https://go.microsoft.com/fwlink/?LinkId=392834> .

### Software-Clients und Anwendungsfunktionen

App-V unterstützt bestimmte Software-Clients und Erweiterungspunkte für Anwendungsfunktionen, mit denen virtualisierte Anwendungen beim Software-Client des Betriebssystems registriert werden können. Dadurch können Benutzer Standard Programme für Vorgänge wie e-Mail, Chat und Media Player auswählen. Dieser Vorgang wird in der Systemsteuerung mit dem festgelegten Programm Zugriffs-und Computer Standard durchgeführt und während der Sequenzierung in den Manifest-oder Dynamic Configuration-Dateien konfiguriert. Anwendungsfunktionen werden nur unterstützt, wenn die App-V-Anwendungen Global veröffentlicht werden.

Beispiel für die Software Clientregistrierung eines App-V-basierten e-Mail-Clients.

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

**Hinweis**  In diesem Beispiel:

-   `<ClientConfiguration EmailEnabled="true" />` ist die Gesamteinstellung für Software Clients zum Integrieren von e-Mail-Clients

-   `<EMail MakeDefault="true">` ist die Kennzeichnung, um einen bestimmten e-Mail-Client als Standard-e-Mail-Client einzurichten

-   `<MAPILibrary>[{ProgramFilesX86}]\Mozilla Thunderbird\mozMapi32_InUse.dll</MAPILibrary>` ist die MAPI-DLL-Registrierung

 

### URL-Protokollhandler

Anwendungen werden nicht immer ausdrücklich als virtualisierte Anwendungen bezeichnet, die den Dateityp Aufruf verwenden. In einer Anwendung, die das Einbetten eines mailto:-Links in ein Dokument oder eine Webseite unterstützt, klickt der Benutzer beispielsweise auf einen mailto:-Link und erwartet, dass er seinen registrierten e-Mail-Client erhält. App-V unterstützt URL-Protokollhandler, die pro Paket mit dem lokalen Betriebssystem registriert werden können. Während der Sequenzierung werden die URL-Protokollhandler automatisch dem Paket hinzugefügt.

In Situationen, in denen es mehr als eine Anwendung gibt, die den spezifischen URL-Protokollhandler registrieren kann, können die dynamischen Konfigurationsdateien verwendet werden, um das Verhalten zu ändern und dieses Feature für eine Anwendung zu unterdrücken oder zu deaktivieren, die nicht die primäre Anwendung sein sollte, die gestartet werden soll.

### AppPath

Der AppPath-Erweiterungspunkt unterstützt das direkte Aufrufen von App-V-Anwendungen aus dem Betriebssystem. Dies erfolgt in der Regel über den Startbildschirm, je nach Betriebssystem, wodurch Administratoren den Zugriff auf App-V-Anwendungen über Betriebssystembefehle oder Skripts ermöglichen können, ohne den spezifischen Pfad zur ausführbaren Datei aufzurufen. Sie vermeidet daher die Änderung der Umgebungsvariablen "System Path" auf allen Systemen, wie Sie während der Veröffentlichung ausgeführt wird.

Der AppPath-Erweiterungspunkt wird entweder im Manifest oder in den dynamischen Konfigurationsdateien konfiguriert und während der Veröffentlichung für den Benutzer in der Registrierung auf dem lokalen Computer gespeichert. Weitere Informationen zur AppPath-Überprüfung finden Sie unter: <https://go.microsoft.com/fwlink/?LinkId=392835> .

### Virtuelle Anwendung

Dieses Subsystem stellt eine Liste der während der Sequenzierung erfassten Anwendungen bereit, die normalerweise von anderen App-V-Komponenten verwendet werden. Die Integration von Erweiterungspunkten, die zu einer bestimmten Anwendung gehören, kann mit dynamischen Konfigurationsdateien deaktiviert werden. Wenn ein Paket beispielsweise zwei Anwendungen enthält, ist es möglich, alle Erweiterungspunkte zu deaktivieren, die zu einer Anwendung gehören, damit nur Erweiterungspunkte anderer Anwendungen integriert werden können.

### Erweiterungspunkt Regeln

Die oben beschriebenen Erweiterungspunkte sind in das Betriebssystem integriert, je nachdem, wie die Pakete veröffentlicht wurden. Bei der globalen Veröffentlichung werden Erweiterungspunkte an öffentlichen Speicherorten platziert, an denen die Benutzer Veröffentlichung Erweiterungspunkte an Benutzerspeicherorten platziert. Beispiel: eine auf dem Desktop erstellte und Global veröffentlichte Verknüpfung führt zu den Dateidaten für die Verknüpfung (%Public%\\Desktop) und den Registrierungsdaten (HKLM\\Software\\Classes). Die gleiche Verknüpfung hätte Dateidaten (%USERPROFILE%\\Desktop) und Registrierungsdaten (HKCU\\Software\\Classes).

Erweiterungspunkte werden nicht alle auf die gleiche Weise veröffentlicht, wobei für einige Erweiterungspunkte eine globale Veröffentlichung erforderlich ist und andere eine Sequenzierung des jeweiligen Betriebssystems und der Architektur erfordern, in der Sie zugestellt werden. Nachfolgend finden Sie eine Tabelle, in der diese beiden Schlüssel Regeln beschrieben werden.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Virtuelle Erweiterung</th>
<th align="left">Erfordert eine Ziel-OS-Sequenzierung</th>
<th align="left">Erfordert globales publizieren</th>
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
<td align="left"><p>Software-Client</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Anwendungsfunktionen</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p>X</p></td>
</tr>
<tr class="even">
<td align="left"><p>Kontextmenü Handler</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p>X</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Drag & Drop-Handler</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Datenobjekt-Handler</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Eigenschaftentabellen-Handler</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Infotipp-Handler</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Spalten Handler</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Shell-Erweiterungen</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Browser Helper-Objekt</p></td>
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

 

## <a href="" id="bkmk-dynamic-config"></a>Verarbeitung dynamischer Konfigurationen


Das Bereitstellen von App-V-Paketen auf einem Computer oder Benutzer ist sehr einfach. Da Organisationen AppV-Anwendungen jedoch über Unternehmensgrenzen hinweg sowie über geografische und politische Grenzen hinweg bereitstellen, ist die Möglichkeit, eine Anwendung einmal mit einem Satz von Einstellungen zu sequenzieren, unmöglich. App-V wurde für dieses Szenario entwickelt, da es bestimmte Einstellungen und Konfigurationen während der Sequenzierung in der Manifestdatei erfasst, aber auch Änderungen mit dynamischen Konfigurationsdateien unterstützt.

Mit der dynamischen App-V-Konfiguration können Sie eine Richtlinie für ein Paket entweder auf Computerebene oder auf Benutzerebene angeben. Mit den Dynamic Configuration-Dateien können Sequenzierungs Ingenieure die Konfiguration eines Pakets nach der Reihenfolge ändern, um die Anforderungen einzelner Benutzer-oder Computergruppen zu erfüllen. In einigen Fällen kann es notwendig sein, Änderungen an der Anwendung vorzunehmen, um die richtige Funktionalität innerhalb der App-V-Umgebung bereitzustellen. Beispielsweise kann es erforderlich sein, Änderungen an den \ _ \ * config.xml-Dateien vorzunehmen, damit bestimmte Aktionen während der Ausführung der Anwendung zu einem bestimmten Zeitpunkt ausgeführt werden können, wie das Deaktivieren einer mailto-Erweiterung, um zu verhindern, dass eine virtualisierte Anwendung diese Erweiterung aus einer anderen Anwendung überschreibt.

App-V-Pakete enthalten die Manifestdatei innerhalb der AppV-Paketdatei, die für Sequenz Vorgänge repräsentativ ist und die Richtlinie der Wahl ist, wenn einem bestimmten Paket keine dynamischen Konfigurationsdateien zugewiesen werden. Nach der Sequenzierung können die dynamischen Konfigurationsdateien geändert werden, um die Veröffentlichung einer Anwendung für verschiedene Desktops oder Benutzer mit unterschiedlichen Erweiterungspunkten zu ermöglichen. Die beiden dynamischen Konfigurationsdateien sind die Dynamic Deployment Configuration (DDC)-und Dynamic User Configuration (Duc)-Dateien. In diesem Abschnitt wird die Kombination der Manifest-und Dynamic Configuration-Dateien behandelt.

### Beispiel für dynamische Konfigurationsdateien

Das folgende Beispiel zeigt die Kombination aus Manifest, Bereitstellungskonfiguration und Benutzerkonfigurationsdateien nach der Veröffentlichung und im normalen Betrieb. Diese Beispiele sind verkürzte Beispiele für die einzelnen Dateien. Der Zweck besteht darin, die Kombination der Dateien nur anzuzeigen und keine vollständige Beschreibung der in den einzelnen Dateien verfügbaren spezifischen Kategorien zu sein. Weitere Informationen finden Sie im App-V 5-Sequenzierungs Handbuch unter: <https://go.microsoft.com/fwlink/?LinkID=269810>

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

## <a href="" id="bkmk-sidebyside-assemblies"></a>Nebeneinander angeordnete Assemblys


App-V unterstützt das automatische Verpacken von nebeneinander angeordneten (SxS)-Assemblys während der Sequenzierung und Bereitstellung auf dem Client während der Veröffentlichung virtueller Anwendungen. App-V 5 SP2 unterstützt das Aufzeichnen von SxS-Assemblys während der Sequenzierung für Assemblys, die auf dem Sequenzcomputer nicht vorhanden sind. Und für Assemblys, bestehend aus Visual C++ (Version 8 und neuer) und/oder MSXML-Laufzeit, erkennt und erfasst der Sequencer diese Abhängigkeiten automatisch, selbst wenn Sie während der Überwachung nicht installiert wurden. Das Feature für nebeneinander angeordnete Assemblys entfernt die Einschränkungen früherer Versionen von App-v, wobei der APP-v-Sequenzer keine bereits auf der Sequenzierungs Arbeitsstation vorhandenen Assemblys erfasst und die Assemblys privatisiert hat, die auf eine Bit-Version pro Paket beschränkt sind. Dieses Verhalten hat dazu geführt, dass App-V-Anwendungen für Clients fehlen, die die erforderlichen SxS-Assemblys aufweisen, wodurch Anwendungsstart Fehler verursacht wurden. Dieser zwang den Verpackungsprozess, zu dokumentieren und sicherzustellen, dass alle für Pakete erforderlichen Assemblys lokal auf dem Clientbetriebssystem des Benutzers installiert wurden, um die Unterstützung für die virtuellen Anwendungen zu gewährleisten. Auf der Grundlage der Anzahl der Assemblys und der fehlenden Anwendungsdokumentation für die erforderlichen Abhängigkeiten war diese Aufgabe sowohl eine Herausforderung für die Verwaltung als auch die Implementierung.

Die Unterstützung von nebeneinander angeordneten Assemblys in App-V bietet die folgenden Features.

-   Automatische Erfassung von SxS-Assemblierungen während der Sequenzierung, unabhängig davon, ob die Assembly bereits auf der Sequenzierungs Arbeitsstation installiert war.

-   Der App-V-Client installiert erforderliche SxS-Assemblys automatisch zur Veröffentlichungszeit auf dem Clientcomputer, wenn diese nicht vorhanden sind.

-   Der Sequencer meldet die VC-Laufzeitabhängigkeit in Sequencer-Berichterstattungsmechanismus.

-   Der Sequencer ermöglicht die Entscheidung, die Assemblys, die bereits auf dem Sequencer installiert sind, nicht zu verpacken, wodurch Szenarien unterstützt werden, in denen die Assemblys zuvor auf den Zielcomputern installiert wurden.

### Automatisches Veröffentlichen von SxS-Assemblys

Während der Veröffentlichung eines App-v-Pakets mit SxS-Assemblys überprüft der APP-v-Client, ob die Assembly auf dem Computer vorhanden ist. Wenn die Assembly nicht vorhanden ist, stellt der Client die Assembly auf dem Computer bereit. Pakete, die Bestandteil von Verbindungsgruppen sind, basieren auf den nebeneinander angeordneten Baugruppen Installationen, die Bestandteil der Basispakete sind, da die Verbindungsgruppe keine Informationen zur Assemblierungs Installation enthält.

**Hinweis**  Beim Aufheben der Veröffentlichung oder beim Entfernen eines Pakets mit einer Assembly werden die Assemblys für dieses Paket nicht entfernt.

 

## <a href="" id="bkmk-client-logging"></a>Client Protokollierung


Der App-V-Client protokolliert Informationen im Windows-Ereignisprotokoll im standardmäßigen etw-Format. Die spezifischen App-V-Ereignisse finden Sie in der Ereignisanzeige unter Anwendungen und Dienste Logs\\Microsoft\\AppV\\Client.

**Hinweis**  In App-V 5,0 SP3 wurden einige Protokolle konsolidiert und an den folgenden Speicherort verschoben:

`Event logs/Applications and Services Logs/Microsoft/AppV/ServiceLog`

Eine Liste der verschobenen Protokolle finden Sie unter [Informationen zu App-V 5,0 SP3](about-app-v-50-sp3.md#bkmk-event-logs-moved).

 

Nachfolgend werden drei spezifische Kategorien von Ereignissen aufgezeichnet.

**Administrator**: protokolliert Ereignisse für Konfigurationen, die auf den App-V-Client angewendet werden, und enthält die primären Warnungen und Fehler.

**Betriebsbereit**: protokolliert die allgemeine App-v-Ausführung und-Verwendung einzelner Komponenten und erstellt ein Überwachungsprotokoll der APP-v-Vorgänge, die auf dem App-v-Client abgeschlossen wurden.

**Virtuelle Anwendung**: protokolliert die Einführung virtueller Anwendungen und die Verwendung von Virtualisierungs-Subsysteme.






 

 





