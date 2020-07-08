---
title: Leistungsleitfaden zu Application Virtualization 5.0
description: Leistungsleitfaden zu Application Virtualization 5.0
author: dansimp
ms.assetid: 6b3a3255-b957-4b9b-8bfc-a93fe8438a81
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 3b0f5ef07935fc34adce772e7b2fff85a12b01dc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805051"
---
# Leistungsleitfaden zu Application Virtualization 5.0


Erfahren Sie, wie Sie App-V 5,0 für optimale Leistung konfigurieren, virtuelle App-Pakete optimieren und eine bessere Benutzererfahrung mit RDS und VDI bieten.

Durch die Implementierung mehrerer Methoden können Sie die Benutzerfreundlichkeit verbessern. Allerdings unterstützt Ihre Umgebung möglicherweise nicht alle Methoden.

Lesen und verstehen Sie die folgenden Informationen, bevor Sie dieses Dokument lesen.

-   [Microsoft Application Virtualization 5,0-Administrator Handbuch](microsoft-application-virtualization-50-administrators-guide.md)

-   [App-V 5 SP2-Anwendungsveröffentlichung und Client Interaktion](https://go.microsoft.com/fwlink/?LinkId=395206)

-   [Microsoft Application Virtualization 5,0-Sequenzierungs Handbuch](https://go.microsoft.com/fwlink/?LinkId=269953)

**Hinweis:**  
Einige in diesem Dokument verwendete Begriffe können je nach externer Quelle und Kontext unterschiedlich sein. Weitere Informationen zu den in diesem Dokument verwendeten Begriffen gefolgt von einem Sternchen **\\** * finden Sie im Abschnitt " [Application Virtualization-Leistungsleitfaden](#bkmk-terms1) " dieses Dokuments.



Schließlich erhalten Sie in diesem Dokument die Informationen zum Konfigurieren des Computers, auf dem der App-V 5,0-Client und die Umgebung ausgeführt werden, um eine optimale Leistung zu erzielen. Optimieren Sie Ihre virtuellen Anwendungspakete für die Leistung mithilfe des Sequencers, und verstehen Sie, wie Sie die Benutzeroberflächen-Virtualisierung (UE-v) oder andere Benutzer Umgebungs Verwaltungstechnologien verwenden können, um die optimale Benutzererfahrung mit App-V 5,0 sowohl in Remote Desktop Diensten (RDS) als auch in nicht persistenter virtueller Desktopinfrastruktur (VDI) bereitzustellen.

Wenn Sie ermitteln möchten, welche Informationen für Ihre Umgebung relevant sind, sollten Sie die Kurzübersicht und die Anwendungs Checkliste für jeden Abschnitt überprüfen.

## <a href="" id="---------app-v-5-0-in-stateful--non-persistent-deployments"></a> App-V 5,0 in Stateful \ * nicht persistente Bereitstellungen


Dieser Abschnitt enthält Informationen zu einem Ansatz, der sicherstellt, dass ein Benutzer innerhalb von Sekunden nach der Anmeldung auf alle virtuellen Anwendungen zugreifen kann. Dies wird erreicht, indem die häufig lange andauernde App-V 5,0-Veröffentlichungsaktualisierung eindeutig adressiert wird. Wie Sie feststellen werden, ist die Grundlage des Ansatzes die schnellste Veröffentlichungsaktualisierung, die nicht wirklich etwas tun muss. Es müssen eine Reihe von Bedingungen erfüllt sein, und es werden Schritte ausgeführt, um die optimale Benutzererfahrung bereitzustellen.

Verwenden Sie die Informationen im folgenden Abschnitt, um weitere Informationen zu erhalten:

[Verwendungsszenarien](#bkmk-us) – beachten Sie bei der Überprüfung der beiden Szenarien, dass es sich hierbei um extreme Ansätze handelt. Basierend auf Ihren Nutzungsanforderungen können Sie diese Schritte auf eine Teilmenge von Benutzern und/oder virtuellen Anwendungspaketen anwenden.

-   Optimiert für die Leistung: um die optimale Benutzerfreundlichkeit zu gewährleisten, können Sie davon ausgehen, dass das Basisabbild einige der virtuellen App-V-Anwendungspakete umfasst. Diese und andere Anforderungen werden besprochen.

-   Optimiert für den Speicher – wenn Sie sich mit den Auswirkungen auf den Speicher befassen, hilft Ihnen dieses Szenario, diese Probleme zu beheben.

[Vorbereiten Ihrer Umgebung](#bkmk-pe)

-   Schritte zum Vorbereiten des Basis Bilds – egal, ob es sich um eine nicht persistente VDI-oder RDSH-Umgebung handelt, es müssen nur wenige Schritte im Basisabbild ausgeführt werden, um diesen Ansatz zu aktivieren.

-   Verwenden Sie UE-v 2,0 als die Benutzerprofilverwaltung (UPM)-Lösung für den App-v-Ansatz – der Eckpfeiler dieses Ansatzes ist die Fähigkeit einer UEM-Lösung, die Inhalte von nur wenigen Registrierungs-und Dateispeicherorten beizubehalten. Diese Speicherorte stellen die Benutzer Integrationen \ * dar. Überprüfen Sie unbedingt die spezifischen Anforderungen für die UPM-Lösung.

[Benutzerfreundlichkeit durchlaufen](#bkmk-uewt)

-   Durchlaufen – Dies ist ein Schritt-für-Schritt-durchlaufen der APP-v-und UE-v-Vorgänge und die Erwartungen der Benutzer.

-   Ergebnis – Dies beschreibt die erwarteten Ergebnisse.

[Auswirkungen auf den Paket Lebenszyklus](#bkmk-plc)

[Verbessern der VDI-Erfahrung durch Leistungsoptimierung/-Optimierung](#bkmk-evdi)

### <a href="" id="applicability-checklist-"></a>Anwendungs Checkliste

Bereitstellungsumgebung

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Nicht persistente VDI-oder RDSH.</p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Benutzeroberflächen-Virtualisierung (UE-V), andere UPM-Lösungen oder Benutzerprofil Datenträger (UPD).</p></td>
</tr>
</tbody>
</table>



Erwartete Konfiguration

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Benutzeroberflächen-Virtualisierung (UE-v) mit aktivierter App-v-Benutzerstatus Vorlage oder UPM-Software (User Profile Management). Nicht-UE-V UPM-Software muss bei der Anmeldung oder beim Starten und Abmelden von Prozessen/Anwendungen ausgelöst werden können.</p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>App-V Shared Content Store (SCS) ist konfiguriert oder kann konfiguriert werden.</p></td>
</tr>
</tbody>
</table>



IT-Verwaltung

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Der Administrator muss möglicherweise das VM-Basisabbild regelmäßig aktualisieren, um eine optimale Leistung zu gewährleisten, oder Administrator muss möglicherweise mehrere Bilder für verschiedene Benutzergruppen verwalten.</p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-us"></a>Verwendungsszenario

Beachten Sie beim Überprüfen der beiden Szenarien, dass diese sich den extremen annähern. Basierend auf Ihren Nutzungsanforderungen können Sie diese Schritte auf eine Teilmenge von Benutzern, virtuellen Anwendungspaketen oder beides anwenden.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Optimiert für die Leistung</th>
<th align="left">Optimiert für den Speicher</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Damit die optimale Benutzererfahrung gewährleistet wird, nutzt dieser Ansatz die Funktionen einer UPM-Lösung und erfordert eine zusätzliche Bildvorbereitung und kann einen zusätzlichen Overhead bei der Bildverwaltung verursachen.</p>
<p>Im folgenden werden viele Leistungsverbesserungen in Stateful-nicht persistenten Bereitstellungen beschrieben. Weitere Informationen finden Sie in den <strong> Schritten zur Sequenzierung, um Pakete für die Veröffentlichungs Leistung zu optimieren, </strong> und verweisen auf <strong> App-V 5,0-Sequenzierungs Handbuch </strong> im <strong> Abschnitt Siehe auch dieses Dokuments </strong> .</p></td>
<td align="left"><p>Die allgemeinen Erwartungen des vorherigen Szenarios gelten hier weiterhin. Beachten Sie jedoch, dass VM-Bilder in der Regel in sehr kostspieligen Arrays gespeichert werden. eine geringfügige Änderung des Ansatzes ist zu verzeichnen. Verwenden Sie keine vorkonfigurierten benutzerbezogenen virtuellen Anwendungspakete im Basisabbild.</p>
<p>Die Auswirkungen dieser Änderung sind im Abschnitt Benutzeroberflächen-Exemplarische Vorgehensweise dieses Dokuments detailliert beschrieben.</p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-pe"></a>Vorbereiten Ihrer Umgebung

In der folgenden Tabelle werden die erforderlichen Schritte zum Vorbereiten des Basis Bilds und der UE-V-oder einer anderen UPM-Lösung für den Ansatz angezeigt.

**Vorbereiten des Basis Bilds**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Optimiert für die Leistung</th>
<th align="left">Optimiert für den Speicher</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p></p>
<ul>
<li><p>Installieren Sie das Hotfix-Paket 4 für Application Virtualization 5,0 SP2-Client Version des Clients.</p></li>
<li><p>Installieren Sie UE-v, und laden Sie die APP-v-Einstellungs Vorlage aus dem UE-v-Vorlagenkatalog herunter, und lesen Sie die folgenden Schritte.</p></li>
<li><p>Konfigurieren Sie den Modus für freigegebenen Inhaltsspeicher (SCS). Weitere Informationen finden Sie unter <a href="how-to-install-the-app-v-50-client-for-shared-content-store-mode.md" data-raw-source="[How to Install the App-V 5.0 Client for Shared Content Store Mode](how-to-install-the-app-v-50-client-for-shared-content-store-mode.md)"> Installieren des App-V 5,0-Clients für den freigegebenen Inhaltsspeicher Modus </a> .</p></li>
<li><p>Konfigurieren Sie die Beibehaltung der Benutzer Integrationen im DWORD-Anmelde Registrierungseintrag.</p></li>
<li><p>Konfigurieren Sie alle Benutzer-und Global gezielten Pakete, beispielsweise <strong> Add-AppvClientPackage, vor </strong> .</p></li>
<li><p>Konfigurieren Sie alle Benutzer-und Global-Zielgruppen für Verbindungen, beispielsweise <strong> Add-AppvClientConnectionGroup </strong> .</p></li>
<li><p>Veröffentlichen Sie alle Global-Targeted-Pakete vorab.</p>
<p></p>
<p>Alternativ</p>
<ul>
<li><p>Durchführen einer globalen Veröffentlichung/Aktualisierung</p></li>
<li><p>Durchführen einer Benutzer Veröffentlichung/-Aktualisierung</p></li>
<li><p>Alle benutzerbezogenen Pakete nicht veröffentlichen.</p></li>
<li><p>Löschen Sie die folgenden VFS-Einträge (User-Virtual File System).</p></li>
</ul>
<p><code>AppData\Local\Microsoft\AppV\Client\VFS</code></p>
<p><code>AppData\Roaming\Microsoft\AppV\Client\VFS</code></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>Installieren Sie das Hotfix-Paket 4 für Application Virtualization 5,0 SP2-Client Version des Clients.</p></li>
<li><p>Installieren Sie UE-v, und laden Sie die APP-v-Einstellungs Vorlage aus dem UE-v-Vorlagenkatalog herunter, und lesen Sie die folgenden Schritte.</p></li>
<li><p>Konfigurieren Sie den Modus für freigegebenen Inhaltsspeicher (SCS). Weitere Informationen finden Sie unter <a href="how-to-install-the-app-v-50-client-for-shared-content-store-mode.md" data-raw-source="[How to Install the App-V 5.0 Client for Shared Content Store Mode](how-to-install-the-app-v-50-client-for-shared-content-store-mode.md)"> Installieren des App-V 5,0-Clients für den freigegebenen Inhaltsspeicher Modus </a> .</p></li>
<li><p>Konfigurieren Sie die Beibehaltung der Benutzer Integrationen im DWORD-Anmelde Registrierungseintrag.</p></li>
<li><p>Vorkonfigurieren aller Global gezielten Pakete, beispielsweise <strong> Add-AppvClientPackage </strong> .</p></li>
<li><p>Konfigurieren Sie alle Global-Targeted Connection Groups, beispielsweise <strong> Add-AppvClientConnectionGroup </strong> .</p></li>
<li><p>Veröffentlichen Sie alle Global-Targeted-Pakete vorab.</p>
<p></p></li>
</ul></td>
</tr>
</tbody>
</table>



**Konfigurationen** – für kritische App-V-Client Konfigurationen und für ein wenig mehr Kontext und Vorgehensweise überprüfen Sie die folgenden Informationen:

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Konfigurationseinstellung</th>
<th align="left">Was bedeutet das?</th>
<th align="left">Wie sollte ich es verwenden?</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Modus für freigegebene Inhaltsspeicher (SCS)</p>
<ul>
<li><p>Konfigurierbar in PowerShell mithilfe von " <strong> AppvClientConfiguration </strong> – <strong> SharedContentStoreMode" </strong> oder</p></li>
<li><p>Während der Installation des App-V 5,0-Clients.</p></li>
</ul></td>
<td align="left"><p>Beim Ausführen des freigegebenen Inhaltsspeichers werden nur Veröffentlichungsdaten auf der Festplatte verwaltet. andere Ressourcen der virtuellen Anwendung werden im Arbeitsspeicher (RAM) verwaltet.</p>
<p>Auf diese Weise können Sie den lokalen Speicherplatz sparen und die Datenträger-e/a pro Sekunde (IOPS) minimieren.</p></td>
<td align="left"><p>Diese Vorgehensweise wird empfohlen, wenn Verbindungen zwischen dem App-V-Client Endpunkt und dem SCS-Inhaltsserver San verfügbar sind.</p></td>
</tr>
<tr class="even">
<td align="left"><p>PreserveUserIntegrationsOnLogin</p>
<ul>
<li><p>Konfigurieren Sie in der Registrierung unter <strong> HKEY_LOCAL_MACHINE </strong>  \  <strong> Software </strong>  \  <strong> </strong>  \  <strong> </strong>  \  <strong> -Client </strong>  \  <strong> Integration </strong> von Microsoft AppV.</p></li>
<li><p>Erstellen Sie den DWORD <strong> -Wert PreserveUserIntegrationsOnLogin </strong> mit dem Wert <strong> 1 </strong> .</p></li>
<li><p>Starten Sie den App-v-Client Dienst neu, oder starten Sie den Computer mit dem App-v-Client neu.</p></li>
</ul></td>
<td align="left"><p>Wenn Sie ein bestimmtes Paket nicht vorkonfiguriert haben ( <strong> Add-AppvClientPackage </strong> ) und diese Einstellung nicht konfiguriert ist, wird der App-V-Client * die beibehaltenen Benutzer Integrationen deintegrieren und dann * erneut integrieren.</p>
<p>Für jedes Paket, das die oben genannten Bedingungen erfüllt, wird die Arbeit beim Veröffentlichen/Aktualisieren effektiv zweimal ausgeführt.</p></td>
<td align="left"><p>Wenn Sie nicht beabsichtigen, alle verfügbaren Benutzer Pakete im Basisabbild vorab zu konfigurieren, verwenden Sie diese Einstellung.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>MaxConcurrentPublishingRefresh</p>
<ul>
<li><p>Konfigurieren Sie in der Registrierung unter <strong> HKEY_LOCAL_MACHINE </strong> &lt; starke &gt; Software für </strong>  \  <strong> Microsoft </strong>  \  <strong> AppV </strong> &lt; starke &gt; Client </strong>  \  <strong> Veröffentlichung </strong> .</p></li>
<li><p>Erstellen Sie den DWORD <strong> -Wert MaxConcurrentPublishingrefresh </strong> mit der gewünschten maximalen Anzahl gleichzeitiger Veröffentlichungs Aktualisierungen.</p></li>
<li><p>Der App-V-Client Dienst und-Computer müssen nicht neu gestartet werden.</p></li>
</ul></td>
<td align="left"><p>Diese Einstellung bestimmt, wie viele Benutzer gleichzeitig eine Veröffentlichungsaktualisierung/-Synchronisierung durchführen können. Die Standardeinstellung ist "No Limit".</p></td>
<td align="left"><p>Das Begrenzen der Anzahl gleichzeitiger Veröffentlichungs Aktualisierungen verhindert eine übermäßige CPU-Auslastung, die sich auf die Computerleistung auswirken kann. Dieser Grenzwert wird in einer RDS-Umgebung empfohlen, in der sich mehrere Benutzer gleichzeitig an demselben Computer anmelden und eine Veröffentlichungs Aktualisierungs Synchronisierung durchführen können.</p>
<p>Wenn der Schwellenwert für die gleichzeitige Veröffentlichungsaktualisierung erreicht ist, kann die Zeit, die zum Veröffentlichen neuer Anwendungen erforderlich ist, und für Endbenutzer verfügbar machen, nachdem Sie sich angemeldet haben, eine unbestimmte Zeitspanne dauern.</p></td>
</tr>
</tbody>
</table>



### Konfigurieren der UE-v-Lösung für App-v-Ansatz

Wir empfehlen die Verwendung von Microsoft User Experience Virtualization (UE-V), um Anwendungseinstellungen und Windows-Betriebssystemeinstellungen für einen bestimmten Benutzer zu erfassen und zu zentralisieren. Diese Einstellungen werden dann auf die verschiedenen Computer angewendet, auf die der Benutzer zugreifen kann, einschließlich Desktopcomputern, Laptopcomputern und VDI-Sitzungen (Virtual Desktop Infrastructure). UE-V ist für RDS-und VDI-Szenarien optimiert.

Weitere Informationen finden Sie unter [Erste Schritte mit der User Experience Virtualization 2,0](https://technet.microsoft.com/library/dn458936.aspx)

Im Wesentlichen müssen Sie lediglich den UE-v-Client installieren und die folgende von Microsoft erstellte App-v-Einstellungs Vorlage aus dem [Vorlagenkatalog für Microsoft User Experience Virtualization (UE-v)](https://gallery.technet.microsoft.com/Authored-UE-V-Settings-bb442a33)herunterladen. Registrieren Sie die Vorlage. Weitere Informationen zu UE-v-Vorlagen finden Sie in [der UE-v-spezifischen Ressource für den Erwerb und die Registrierung der Vorlage](https://technet.microsoft.com/library/dn458936.aspx).

**Hinweis:**  
Ohne einen zusätzlichen Konfigurationsschritt zu durchführen, kann die Microsoft-Benutzer Umgebungs-Virtualisierung (UE-V) die Start Menüverknüpfungen (LNK-Dateien) auf dem Zielcomputer nicht synchronisieren. Der lnk-Dateityp ist standardmäßig ausgeschlossen.

UE-V unterstützt nur das Entfernen des lnk-Dateityps aus der Ausschlussliste in den RDS-und VDI-Szenarien, in denen auf dem Gerät jedes Benutzers dieselbe Gruppe von Anwendungen am gleichen Speicherort installiert ist und jede LNK-Datei für alle Geräte der Benutzer gültig ist. UE-V unterstützt beispielsweise derzeit nicht die folgenden 2 Szenarien, da das Ergebnis darin besteht, dass die Verknüpfung auf einem, aber nicht auf allen Geräten gültig ist.

-   Wenn ein Benutzer auf einem Gerät eine Anwendung installiert hat, deren LNK-Dateien aktiviert sind, und die gleiche systemeigene Anwendung auf einem anderen Gerät auf einem anderen Installations Stamm installiert ist und die LNK-Dateien aktiviert sind.

-   Wenn ein Benutzer eine Anwendung auf einem Gerät installiert hat, aber nicht eine andere, wenn LNK-Dateien aktiviert sind.



**Wichtig**  
In diesem Thema wird beschrieben, wie Sie die Windows-Registrierung mit dem Registrierungs-Editor ändern. Wenn Sie die Windows-Registrierung falsch ändern, können Sie zu schwerwiegenden Problemen führen, bei denen Sie möglicherweise eine Neuinstallation von Windows erforderlich machen. Bevor Sie die Registrierung ändern, sollten Sie eine Sicherungskopie der Registrierungsdateien (System. dat und User. dat) erstellen. Microsoft kann nicht garantieren, dass die Probleme, die beim Ändern der Registrierung auftreten, behoben werden können. Ändern Sie die Registrierung auf Ihr eigenes Risiko.



Navigieren Sie mithilfe des Microsoft Registry-Editors (regedit.exe) zu **HKEY \ _LOCAL \ _MACHINE**  \\  **Software**  \\  **Microsoft**  \\  **UEV**  \\  **Agent**  \\  **Configuration**  \\  **ExcludedFileTypes** , und entfernen Sie **lnk** aus den ausgeschlossenen Dateitypen.

**Konfigurieren einer anderen UPM-Lösung (User Profile Management) für App-V-Ansatz**

Die Erwartung in einer statusbehafteten Umgebung besteht darin, dass eine UPM-Lösung implementiert ist und die Persistenz von Benutzerdaten zwischen Sitzungen und zwischen Anmeldungen unterstützenkann.

Die Anforderungen für die UPM-Lösung lauten wie folgt:

Um eine optimierte Anmeldungs Erfahrung zu ermöglichen, beispielsweise den App-V 5,0-Ansatz für den Benutzer, muss die Lösung in der Lage sein:

-   Beibehalten der folgenden Benutzer Integrationen als Teil des Benutzerprofils/der Benutzerrolle

-   Auslösen einer Benutzerprofil Synchronisierung bei der Anmeldung (oder Anwendungsstart), die gewährleisten kann, dass alle Benutzer Integrationen vor der Veröffentlichung/Aktualisierung angewendet werden, oder

-   Anfügen und Trennen eines Benutzerprofil Datenträgers (UPD) oder einer ähnlichen Technologie, die die Benutzer Integrationen enthält.

-   Erfassen von Änderungen an den Speicherorten, die die Benutzer Integrationen darstellen, bevor Sie die Sitzung abmelden.

Mit App-V 5,0, wenn Sie einen Veröffentlichungsserver (**Add-AppvPublishingServer**) hinzufügen, können Sie die Synchronisierung konfigurieren, beispielsweise beim Aktualisieren während der Anmeldung und/oder nach einem angegebenen Aktualisierungsintervall. In beiden Fällen wird eine geplante Aufgabe erstellt.

In früheren Versionen von App-V 5,0 wurden beide geplanten Aufgaben mit einem VBScript konfiguriert, das den Benutzer und die globale Aktualisierung initiiert. Mit dem Hotfix-Paket 4 für Application Virtualization 5,0 SP2 wird die Benutzeraktualisierung bei der Anmeldung von **SyncAppvPublishingServer.exe**initiiert. Diese Änderung wurde eingeführt, um UPM-Lösungen einen triggerprozess zur Verfügung zu stellen. Dieser Vorgang verzögert die Veröffentlichungs-/Refresh, damit die UPM-Lösung die Benutzer Integrationen anwenden kann. Sobald die Veröffentlichung/Aktualisierung abgeschlossen ist, wird Sie beendet.

**Benutzer Integrationen**

Registrierung – HKEY \ _CURRENT \ _User

-   Path-Software\\Classes

    Ausschließen: lokale Einstellungen, ActivatableClasses, AppX \ *

-   Path-Software\\Microsoft\\AppV

-   Path-Software\\Microsoft\\Windows\\CurrentVersion\\App-Pfade

**Dateispeicherorte**

-   Root – "Umgebungs Variable" APPDATA

    Path – Microsoft\\AppV\\Client\\Catalog

-   Root – "Umgebungs Variable" APPDATA

    Path – Microsoft\\AppV\\Client\\Integration

-   Root – "Umgebungs Variable" APPDATA

    Path-Microsoft\\Windows\\Start Menu\\Programs

-   (Zum Beibehalten aller Desktopverknüpfungen, virtuell und nicht virtuell)

    Root-"KnownFolder" {B4BFCC3A-DB2C-424C-B029-7FE99A87C641} filemask-\ *. lnk

**Microsoft User Experience Virtualization (UE-V)**

Darüber hinaus empfehlen wir die Verwendung von Microsoft User Experience Virtualization (UE-V), um Anwendungseinstellungen und Windows-Betriebssystemeinstellungen für einen bestimmten Benutzer zu erfassen und zu zentralisieren. Diese Einstellungen werden dann auf die verschiedenen Computer angewendet, auf die der Benutzer zugreifen kann, einschließlich Desktopcomputern, Laptopcomputern und VDI-Sitzungen (Virtual Desktop Infrastructure).

Weitere Informationen finden Sie unter [Erste Schritte mit Benutzeroberflächen-Virtualisierungs-1,0](https://technet.microsoft.com/library/jj680015.aspx) und [Speicherort Vorlagen für Freigabeeinstellungen mit dem UE-V-Vorlagenkatalog](https://technet.microsoft.com/library/jj679972.aspx).

### <a href="" id="bkmk-uewt"></a>Benutzerfreundlichkeit durchlaufen

Im folgenden finden Sie eine schrittweise Einführung in die App-V-und UPM-Vorgänge und die Erwartungen, die Benutzer erwarten sollten.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Optimiert für die Leistung</th>
<th align="left">Optimiert für den Speicher</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Nach der Implementierung dieses Ansatzes in der VDI/RDSH-Umgebung bei der ersten Anmeldung</p>
<ul>
<li><p>Vorgang Eine Benutzer Veröffentlichung/-Aktualisierung wird initiiert. Erwartung Wenn ein Benutzer zum ersten Mal virtuelle Anwendungen (beispielsweise nicht persistent) veröffentlicht hat, wird die übliche Dauer einer Veröffentlichung/Aktualisierung übernommen.</p></li>
<li><p>Vorgang Nach dem Veröffentlichen/Aktualisieren erfasst die UPM-Lösung die Benutzer Integrationen. Erwartung Je nachdem, wie die UPM-Lösung konfiguriert ist, kann dies im Rahmen des Abmelde Prozesses erfolgen. Dies führt zu demselben/ähnlichen Overhead wie das Beibehalten des Benutzerzustands.</p></li>
</ul>
<p>Bei nachfolgenden Anmeldungen:</p>
<ul>
<li><p>Vorgang Die UPM-Lösung wendet die Benutzer Integrationen vor der Veröffentlichung/Aktualisierung auf das System an.</p>
<p>Erwartung Es werden Tastenkombinationen auf dem Desktop oder im Startmenü angezeigt, die sofort funktionieren. Wenn das Veröffentlichen/Aktualisieren abgeschlossen wird (d. h., dass Paket Ansprüche geändert werden), können einige davon verschwinden.</p></li>
<li><p>Vorgang Beim Veröffentlichen/Aktualisieren werden Vorgänge zum Veröffentlichen und Veröffentlichen von Änderungen der Benutzerpaket Berechtigungen verarbeitet. Erwartung Wenn keine Berechtigungsänderungen vorhanden sind, wird publishing1 in Sekunden abgeschlossen. Andernfalls wird die Veröffentlichung/Aktualisierung relativ zur Anzahl und Komplexität * von virtuellen Anwendungen zunehmen.</p></li>
<li><p>Vorgang Die UPM-Lösung erfasst die Benutzer Integrationen bei der Abmeldung erneut. Erwartung Wie vorherige.</p></li>
</ul>
<p>¹ der Veröffentlichungsvorgang ( <strong> Publish-AppVClientPackage </strong> ) fügt dem Benutzer Katalogeinträge hinzu, ordnet dem Benutzer den Anspruch zu, identifiziert den lokalen Store und beendet die einzelnen Integrationsschritte.</p></td>
<td align="left"><p>Nach der Implementierung dieses Ansatzes in der VDI/RDSH-Umgebung bei der ersten Anmeldung</p>
<ul>
<li><p>Vorgang Eine Benutzer Veröffentlichung/-Aktualisierung wird initiiert. Erwartung</p>
<ul>
<li><p>Wenn ein Benutzer zum ersten Mal virtuelle Anwendungen (z. b. nicht persistent) veröffentlicht hat, wird die übliche Dauer einer Veröffentlichung/Aktualisierung übernommen.</p></li>
<li><p>Die ersten und nachfolgenden Anmeldungen werden durch die Vorkonfiguration von Paketen (hinzufügen/aktualisieren) beeinträchtigt.</p>
<p></p></li>
</ul></li>
<li><p>Vorgang Nach dem Veröffentlichen/Aktualisieren erfasst die UPM-Lösung die Benutzer Integrationen. Erwartung Je nachdem, wie die UPM-Lösung konfiguriert ist, kann dies im Rahmen des Abmelde Prozesses erfolgen. Dies führt zu demselben/ähnlichen Overhead wie das Beibehalten des Benutzerzustands.</p></li>
</ul>
<p>Bei nachfolgenden Anmeldungen:</p>
<ul>
<li><p>Vorgang Die UPM-Lösung wendet die Benutzer Integrationen vor der Veröffentlichung/Aktualisierung auf das System an.</p></li>
<li><p>Vorgang "Hinzufügen/aktualisieren" muss alle benutzerspezifischen Anwendungen vorab konfigurieren. Erwartung</p>
<ul>
<li><p>Dadurch kann die Verfügbarkeit der Anwendung deutlich verkürzt werden (in der Reihenfolge von 10 Sekunden).</p></li>
<li><p>Dadurch wird die Veröffentlichungs Aktualisierungszeit relativ zur Anzahl und Komplexität * von virtuellen Anwendungen erhöht.</p>
<p></p></li>
</ul></li>
<li><p>Vorgang Beim Veröffentlichen/Aktualisieren werden Vorgänge zum Veröffentlichen und Veröffentlichen von Änderungen an Benutzerpaket Berechtigungen verarbeitet.</p></li>
</ul></td>
</tr>
</tbody>
</table>



<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Ergebnis</th>
<th align="left">Ergebnis</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p></p>
<ul>
<li><p>Da die Benutzer Integrationen vollständig erhalten sind, wird es keine Arbeit geben, beispielsweise die Integration, um die Veröffentlichung/Aktualisierung abzuschließen. Alle virtuellen Anwendungen werden innerhalb von Sekunden nach der Anmeldung zur Verfügung stehen.</p></li>
<li><p>Beim Veröffentlichen/Aktualisieren werden Änderungen an den Benutzern mit dem Titel "virtuelle Anwendungen" verarbeitet, die sich auf die Benutzeroberfläche auswirken.</p></li>
</ul></td>
<td align="left"><p>Da die Add/Refresh-Konfiguration alle virtuellen Anwendungen auf dem virtuellen Computer neu konfigurieren muss, wird die Veröffentlichungs Aktualisierungszeit bei jeder Anmeldung verlängert.</p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-plc"></a>Auswirkungen auf den Paket Lebenszyklus

Das Upgrade eines Pakets ist ein entscheidender Aspekt des Paket Lebenszyklus. Wenn Sie sicherstellen möchten, dass Benutzer Zugriff auf die entsprechenden aktualisierten (veröffentlichten) oder herabgestuften (nicht veröffentlichten) virtuellen Anwendungspakete haben, empfiehlt es sich, das Basis Bild so zu aktualisieren, dass diese Änderungen wiedergegeben werden. Erläutern Sie, warum der folgende Abschnitt überprüft werden sollte:

App-V 5,0 SP2 hat das Konzept der ausstehenden Zustände eingeführt. In der Vergangenheit

-   Wenn ein Administrator die Berechtigungen geändert oder eine neue Version eines Pakets erstellt (aktualisiert) hat und während einer Veröffentlichung/Aktualisierung dieses Paket in Verwendung war, schlägt der Vorgang zum Veröffentlichen oder veröffentlichen fehl.

-   Wenn nun ein Paket in Verwendung ist, wird der Vorgang vorangestellt. Die Vorgänge für die Veröffentlichung und Veröffentlichung werden beim Neustart des Diensts verarbeitet, oder es wird ein anderer Befehl zum Veröffentlichen oder deinstallieren veröffentlicht. Im letzteren Fall verbleibt die virtuelle Anwendung in einem ausstehenden Zustand, wenn die virtuelle Anwendung anderweitig verwendet wird. Für Global veröffentlichte Pakete wird häufig ein Neustart (oder ein Dienstneustart) benötigt.

In einer nicht persistenten Umgebung ist es unwahrscheinlich, dass diese vorangestellt-Vorgänge verarbeitet werden. Die vorangestellt-Vorgänge, beispielsweise Aufgaben, werden unter **HKEY \ _CURRENT \ _User**  \\  **Software**  \\  **Microsoft**  \\  **AppV**  \\  **Client**  \\  **PendingTasks**erfasst. Obwohl dieser Speicherort von der UPM-Lösung beibehalten wird, wird er nicht verarbeitet, wenn er vor der Anmeldung nicht auf die Umgebung angewendet wird.

### <a href="" id="bkmk-evdi"></a>Verbessern der VDI-Erfahrung durch Optimierung der Leistungsoptimierung

Der folgende Abschnitt enthält Listen mit Informationen zur Microsoft-Dokumentation und Downloads, die bei der Optimierung Ihrer Umgebung für die Leistung hilfreich sein können.

**.Net ngen-Blog und-Skript (dringend empfohlen)**

Informationen zu ngen-Technologien

-   [So beschleunigen Sie die ngen-Optimierung](https://blogs.msdn.com/b/dotnet/archive/2013/08/06/wondering-why-mscorsvw-exe-has-high-cpu-usage-you-can-speed-it-up.aspx)

-   [Skript](https://aka.ms/DrainNGenQueue)

**Windows Server-und Serverrollen**

Richtlinien zur Server Leistungsoptimierung für

-   [Microsoft Windows Server 2012 R2](https://msdn.microsoft.com/library/windows/hardware/dn529133.aspx)

-   [Microsoft Windows Server 2012](https://download.microsoft.com/download/0/0/B/00BE76AF-D340-4759-8ECD-C80BC53B6231/performance-tuning-guidelines-windows-server-2012.docx)

-   [Microsoft Windows Server 2008 R2](https://download.microsoft.com/download/6/B/2/6B2EBD3A-302E-4553-AC00-9885BBF31E21/Perf-tun-srv-R2.docx)

**Server Rollen**

-   [Host für Remote Desktop-Virtualisierung](https://msdn.microsoft.com/library/windows/hardware/dn567643.aspx)

-   [Host für Remote Desktop Sitzungen](https://msdn.microsoft.com/library/windows/hardware/dn567648.aspx)

-   [IIS-Relevanz: App-V-Verwaltung, Veröffentlichung, Reporting-Webdienste](https://msdn.microsoft.com/library/windows/hardware/dn567678.aspx)

-   [Relevanz für Datei Server (SMB): bei Verwendung für App-V Content-Speicherung und-Zustellung im SCS-Modus](https://technet.microsoft.com/library/jj134210.aspx)

**Leitfaden zur Leistungsoptimierung für Windows-Clients (Gastbetriebssystem)**

-   [Microsoft Windows 7](https://download.microsoft.com/download/E/5/7/E5783D68-160B-4366-8387-114FC3E45EB4/Performance Tuning Guidelines for Windows 7 Desktop Virtualization v1.9.docx)

-   [Optimierungs Skript: (vom Microsoft-Support bereitgestellt)](https://blogs.technet.com/b/jeff_stokes/archive/2012/10/15/the-microsoft-premier-field-engineer-pfe-view-on-virtual-desktop-vdi-density.aspx)

-   [Microsoft Windows 8](https://download.microsoft.com/download/6/0/1/601D7797-A063-4FA7-A2E5-74519B57C2B4/Windows_8_VDI_Image_Client_Tuning_Guide.pdf)

-   [Optimierungs Skript: (vom Microsoft-Support bereitgestellt)](https://blogs.technet.com/b/jeff_stokes/archive/2013/04/09/hot-off-the-presses-get-it-now-the-windows-8-vdi-optimization-script-courtesy-of-pfe.aspx)

## Schritte zur Sequenzierung zur Optimierung von Paketen für die Veröffentlichungs Leistung


App-v 5,0 und App-v 5,0 SP2 liefern in ihren jeweiligen Versionen einen signifikanten Wert. Verschiedene Features erleichtern neue Szenarien oder aktivieren neue Kunden Bereitstellungsszenarien. Diese folgenden Features können sich auf die Leistung der Veröffentlichungs-und Startvorgänge auswirken.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Schritt</th>
<th align="left">Überlegung</th>
<th align="left">Vorteile</th>
<th align="left">Nachteile</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Kein Funktionsbaustein 1 (fb1, auch als primärer FB bezeichnet)</p></td>
<td align="left"><p>Kein fb1 bedeutet, dass die Anwendung sofort gestartet wird und Datenstromfehler (Anwendung erfordert Datei, dll und muss über das Netzwerk Herunterfahren) während des Starts ist. Wenn Netzwerkeinschränkungen vorhanden sind, wird fb1:</p>
<ul>
<li><p>Verringern Sie die Anzahl der Datenstromfehler und die Netzwerkbandbreite, die beim erstmaligen Starten einer Anwendung verwendet werden.</p></li>
<li><p>Verzögern Sie den Start, bis der gesamte fb1 gestreamt wurde.</p></li>
</ul></td>
<td align="left"><p>Durch Datenstromfehler wird die Startzeit verringert.</p></td>
<td align="left"><p>Virtuelle Anwendungspakete mit konfigurierter fb1 müssen neu sequenziert werden.</p></td>
</tr>
</tbody>
</table>



### Entfernen von fb1

Zum Entfernen von fb1 ist das Installationsprogramm für die ursprüngliche Anwendung nicht erforderlich. Nachdem Sie die folgenden Schritte ausgeführt haben, wird empfohlen, den Computer, auf dem der Sequencer ausgeführt wird, auf einen sauberen Snapshot zurückzusetzen.

**Sequencer UI** – erstellen Sie ein neues virtuelles Anwendungspaket.

1.  Führen Sie die Schritte zur Sequenzierung bis zum Anpassen- &gt; Streaming aus.

2.  Wählen Sie beim Streaming-Schritt nicht **das Paket für die Bereitstellung über langsames oder unzuverlässiges Netzwerk optimieren**aus.

3.  Wenn gewünscht, fahren Sie mit dem **Zielbetriebssystem**fort.

**Ändern eines vorhandenen virtuellen Anwendungspakets**

1.  Führen Sie die Schritte zur Sequenzierung bis zum Streaming durch.

2.  Wählen Sie **das Paket für die Bereitstellung nicht über ein langsames oder unzuverlässiges Netzwerk optimieren**aus.

3.  Zum **Erstellen eines Pakets**wechseln

**PowerShell** – Aktualisieren eines vorhandenen virtuellen Anwendungspakets

1.  Öffnen Sie eine erweiterte PowerShell-Sitzung.

2.  Importieren-Modul **appvsequencer**.

3.  **Update-AppvSequencerPackage**  -  **AppvPackageFilePath**

    "C:\\Packages\\MyPackage.AppV"-Installationsprogramm

    "C:\\PackageInstall\\PackageUpgrade.exe empty.exe"-OutputPath

    "C:\\UpgradedPackages"

    **Hinweis:**  
    Dieses Cmdlet erfordert eine ausführbare Datei (exe) oder eine Batchdatei (bat). Sie müssen eine leere (tut nichts) ausführbare oder Batchdatei angeben.



<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Schritt</th>
<th align="left">Erwägungen</th>
<th align="left">Vorteile</th>
<th align="left">Nachteile</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Keine SxS-Installation bei Veröffentlichung (Pre-install SxS-Assemblys)</p></td>
<td align="left"><p>Virtuelle Anwendungspakete müssen nicht neu sequenziert werden. SxS-Assemblys können im virtuellen Anwendungspaket verbleiben.</p></td>
<td align="left"><p>Die Abhängigkeiten der SxS-Assembly werden nicht zur Veröffentlichungszeit installiert.</p></td>
<td align="left"><p>SxS-Assemblierungs Abhängigkeiten müssen bereits vorinstalliert sein.</p></td>
</tr>
</tbody>
</table>



### Erstellen eines neuen virtuellen Anwendungspakets auf dem Sequenzer

Wenn während der Sequencer-Überwachung eine SxS-Assembly (wie eine VC + +-Laufzeit) als Teil der Installation einer Anwendung installiert wird, wird die SxS-Assembly automatisch erkannt und im Paket enthalten. Der Administrator wird benachrichtigt und kann die SxS-Assembly ausschließen.

**Client Seite**:

Beim Veröffentlichen eines virtuellen Anwendungspakets wird vom App-V 5,0 SP2-Client erkannt, ob bereits eine erforderliche SxS-Abhängigkeit installiert ist. Wenn die Abhängigkeit auf dem Computer nicht verfügbar ist und im Paket enthalten ist, wird ein herkömmlicher Windows Installer (.** MSI**) die Installation der SxS-Assembly wird initiiert. Wie zuvor dokumentiert, installieren Sie einfach die Abhängigkeit auf dem Computer, auf dem der Client ausgeführt wird, um sicherzustellen, dass die Windows Installer-Installation (MSI) nicht erfolgt.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Schritt</th>
<th align="left">Erwägungen</th>
<th align="left">Vorteile</th>
<th align="left">Nachteile</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Selektives verwenden dynamischer Konfigurationsdateien</p></td>
<td align="left"><p>Der App-V 5,0-Client muss diese dynamischen Konfigurationsdateien analysieren und verarbeiten.</p>
<p>Achten Sie auf die Größe und Komplexität (Skriptausführung, VREG Einschlüsse/Ausschlüsse) der Datei.</p>
<p>Zahlreiche virtuelle Anwendungspakete verfügen möglicherweise bereits über Benutzer-oder computerspezifische Dynamic Configuration Files-Dateien.</p></td>
<td align="left"><p>Die Veröffentlichungszeit wird verbessert, wenn diese Dateien selektiv oder überhaupt nicht verwendet werden.</p></td>
<td align="left"><p>Virtuelle Anwendungspakete müssten einzeln oder über die App-V Server-Verwaltungskonsole neu konfiguriert werden, um zugeordnete dynamische Konfigurationsdateien zu entfernen.</p></td>
</tr>
</tbody>
</table>



### Deaktivieren einer dynamischen Konfiguration mithilfe von PowerShell

-   Für bereits veröffentlichte Pakete können Sie `Set-AppVClientPackage –Name Myapp –Path c:\Packages\Apps\MyApp.appv` ohne

    **-DynamicDeploymentConfiguration-** Parameter

-   Verwenden Sie beim Hinzufügen neuer Pakete `Add-AppVClientPackage –Path c:\Packages\Apps\MyApp.appv` nicht die

    **-DynamicDeploymentConfiguration-** Parameter.

Eine Dokumentation zur Anwendung einer dynamischen Konfiguration finden Sie unter:

-   [So wenden Sie die Benutzerkonfigurationsdatei mithilfe von PowerShell an](how-to-apply-the-user-configuration-file-by-using-powershell.md)

-   [Sie wenden Sie die Bereitstellungskonfigurationsdatei mithilfe von PowerShell an](how-to-apply-the-deployment-configuration-file-by-using-powershell.md)

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Schritt</th>
<th align="left">Erwägungen</th>
<th align="left">Vorteile</th>
<th align="left">Nachteile</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Konto für synchrone Skriptausführung während des Paket Lebenszyklus.</p></td>
<td align="left"><p>Wenn Skript Sicherheiten in das Paket eingebettet sind, kann Add (PowerShell) erheblich langsamer sein.</p>
<p>Die Ausführung von Skripts während des Starts virtueller Anwendungen (StartVirtualEnvironment, StartProcess) und/oder Add + Publish wirkt sich auf die wahrgenommene Leistung während eines oder mehrerer dieser Lebenszyklus Vorgänge aus.</p></td>
<td align="left"><p>Durch die Verwendung von asynchronen (nicht blockierenden) Skripts wird sichergestellt, dass die Lebenszyklus Vorgänge effizient abgeschlossen werden.</p></td>
<td align="left"><p>Dieser Schritt erfordert Kenntnisse über alle virtuellen Anwendungspakete mit eingebetteten Skript Sicherheiten, denen dynamische Konfigurationsdateien zugeordnet sind, und die synchron Skripts referenzieren und ausführen.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Entfernen Sie überflüssige virtuelle Schriftarten aus dem Paket.</p></td>
<td align="left"><p>Die Mehrzahl der vom App-V-Produktteam untersuchten Anwendungen enthielt eine geringe Anzahl von Schriftarten, in der Regel weniger als 20.</p></td>
<td align="left"><p>Virtuelle Schriftarten wirken sich auf die Veröffentlichungs Aktualisierungsleistung aus.</p></td>
<td align="left"><p>Die gewünschten Schriftarten müssen nativ aktiviert/installiert werden. Anweisungen hierzu finden Sie unter Installieren oder Deinstallieren von Schriftarten.</p></td>
</tr>
</tbody>
</table>



### Ermitteln, welche virtuellen Schriftarten im Paket vorhanden sind

-   Erstellen Sie eine Kopie des Pakets.

-   Paket umbenennen \ _Copy. AppV zu Package\_copy.zip

-   Öffnen Sie AppxManifest.xml, und suchen Sie nach folgendem:

    &lt;AppV: Extension Category = "AppV. Fonts"&gt;

    &lt;AppV: Schriftarten&gt;

    &lt;AppV: Font Path = "\ [{Fonts} \] \\private\\CalibriL.ttf" DelayLoad = "true" &gt; &lt; /AppV: Font&gt;

    **Hinweis:**  
    Wenn Schriftarten als " **DelayLoad**" gekennzeichnet sind, wirkt sich dies nicht auf den ersten Start aus.



~~~
&lt;/appv:Fonts&gt;
~~~

### Ausschließen virtueller Schriftarten aus dem Paket

Verwenden Sie die dynamische Konfigurationsdatei, die am besten für den Benutzerbereich geeignet ist – Bereitstellungskonfiguration für alle Benutzer auf dem Computer, Benutzerkonfiguration für bestimmte Benutzer oder Benutzer.

-   Deaktivieren Sie Schriftarten mit der Bereitstellungs-oder Benutzerkonfiguration.

Schriftarten

--&gt;

&lt;Schriftarten aktiviert = "falsch"/&gt;

&lt;!--

## <a href="" id="bkmk-terms1"></a> App-V 5,0-Terminologie zur Leistungssteuerung


Die folgenden Begriffe werden verwendet, wenn Konzepte und Aktionen im Zusammenhang mit der App-V 5,0-Leistungsoptimierung beschrieben werden.

-   **Komplexität** : bezieht sich auf ein oder mehrere Paket Merkmale, die sich auf die Leistung bei der Vorkonfiguration (**Add-AppvClientPackage**) oder Integration (**Publish-AppvClientPackage**) auswirken können. Einige Beispiel Merkmale sind: Manifestgröße, Anzahl der virtuellen Schriftarten, Anzahl der Dateien.

-   **De-Integration** – entfernt die Benutzer Integrationen

-   **Re-Integration** – wendet die Benutzer Integrationen an.

-   **Nicht persistent, gebündelt** – erstellt bei jeder Anmeldung einen Computer, auf dem eine virtuelle Umgebung ausgeführt wird.

-   **Persistent, persönlich** – ein Computer mit einer virtuellen Umgebung, der bei jedem Login gleich bleibt.

-   **Stateful** -für dieses Dokument impliziert, dass Benutzer Integrationen zwischen Sitzungen beibehalten werden und eine Technologie für die Benutzer Umgebungsverwaltung in Verbindung mit nicht persistenten RDSH oder VDI verwendet wird.

-   **Statuslos** – stellt ein Szenario dar, in dem kein Benutzerstatus zwischen Sitzungen beibehalten wird.

-   **Trigger** – (oder systemeigene Aktions Trigger). UPM verwendet diese Typen von Triggern, um Überwachungs-oder Synchronisierungsvorgänge zu initiieren.

-   **Benutzererfahrung** – im Kontext von App-V 5,0 ist die Benutzeroberfläche quantitativ die Summe der folgenden Teile:

    -   Ab dem Punkt, an dem Benutzer eine Anmeldung initiieren, wenn Sie den Desktop manipulieren können.

    -   Ab dem Punkt, an dem der Desktop mit dem Punkt interagieren kann, an dem eine Veröffentlichungsaktualisierung beginnt (in PowerShell-Ausdrücken, synchronisieren), wenn die vollständige Serverinfrastruktur von App-V 5,0 verwendet wird. In eigenständigen Instanzen werden die PowerShell-Befehle **Add-AppVClientPackage** und **Publish-AppVClientPackage** initiiert.

    -   Vom Anfang bis zum Abschluss der Veröffentlichungsaktualisierung. In eigenständigen Instanzen ist dies die erste letzte virtuelle Anwendung, die veröffentlicht wurde.

    -   Ab dem Punkt, an dem die virtuelle Anwendung für den Start über eine Verknüpfung verfügbar ist. Alternativ dazu befindet Sie sich ab dem Zeitpunkt, zu dem die Dateitypzuordnung registriert ist, und startet eine angegebene virtuelle Anwendung.

-   **Verwaltung von Benutzerprofilen** – der kontrollierte und strukturierte Ansatz zum Verwalten von Benutzer Komponenten, die mit der Umgebung verknüpft sind. Beispielsweise Benutzerprofile, Einstellungen und Richtlinienverwaltung, Anwendungssteuerung und Anwendungsbereitstellung. Sie können mithilfe von Skripting oder Lösungen von Drittanbietern die Umgebung nach Bedarf konfigurieren.






## Verwandte Themen


[Microsoft Application Virtualization 5,0-Administrator Handbuch](microsoft-application-virtualization-50-administrators-guide.md)









