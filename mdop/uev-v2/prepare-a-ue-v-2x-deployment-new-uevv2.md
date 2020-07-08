---
title: Vorbereiten einer UE-V 2. x-Bereitstellung
description: Vorbereiten einer UE-V 2. x-Bereitstellung
author: dansimp
ms.assetid: c429fd06-13ff-48c5-b9c9-fa1ec01ab800
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 04/19/2017
ms.openlocfilehash: e6b2de407990536e1a08532632dcea19ea0d0ee9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811746"
---
# Vorbereiten einer UE-V 2. x-Bereitstellung


Bevor Sie Microsoft User Experience Virtualization (UE-V) 2,0 oder 2,1 als Lösung für die Synchronisierung von Einstellungen zwischen Geräten bereitstellen, auf die Benutzer in Ihrem Unternehmen zugreifen, müssen Sie einige Schritte planen und vorbereiten. In diesem Thema erfahren Sie, welche Art von Bereitstellung Sie ausführen werden und welche Vorbereitungen Sie im Voraus vornehmen können, damit Ihre Bereitstellung erfolgreich ist.

Sehen wir uns zunächst die Aufgaben an, die Sie für die Bereitstellung von UE-V ausführen werden:

-   Planen der UE-V-Bereitstellung

    Bevor Sie etwas bereitstellen, besteht ein guter erster Schritt darin, etwas zu planen, damit Sie ermitteln können, welche UE-V-Features bereitgestellt werden. Wenn Sie diese Seite nun belassen, sollten Sie die folgenden Planungsinformationen durchlesen.

-   [Bereitstellen der erforderlichen Features für UE-V 2.x](deploy-required-features-for-ue-v-2x-new-uevv2.md)

    Für jede UE-V-Bereitstellung sind diese Aktivitäten erforderlich:

    -   [Definieren eines Speicherorts für Einstellungen](https://technet.microsoft.com/library/dn458891.aspx#ssl)

    -   [Entscheiden, wie der UE-v-Agent bereitgestellt und UE-v-Konfigurationen verwaltet werden](https://technet.microsoft.com/library/dn458891.aspx#config)

    -   [Installieren des UE-V-Agents](https://technet.microsoft.com/library/dn458891.aspx#agent) auf jedem Benutzer Computer, auf dem die Einstellungen synchronisiert werden müssen

-   Optional können Sie [UE-V 2. x für benutzerdefinierte Anwendungen bereitstellen.](deploy-ue-v-2x-for-custom-applications-new-uevv2.md)

    Die Planung hilft Ihnen herauszufinden, ob UE-v die Synchronisierung von Einstellungen für benutzerdefinierte Anwendungen (Drittanbieter oder Branchen) unterstützen soll, für die diese UE-v-Features erforderlich sind:

    -   [Installieren des UEV-Generators](https://technet.microsoft.com/library/dn458942.aspx#uevgen) zum Erstellen, bearbeiten und Überprüfen der Speicherort Vorlagen für benutzerdefinierte Einstellungen, die zum Synchronisieren von benutzerdefinierten Anwendungseinstellungen erforderlich sind

    -   [Erstellen von Speicherort Vorlagen für benutzerdefinierte Einstellungen](https://technet.microsoft.com/library/dn458942.aspx#createcustomtemplates) mithilfe des UE-V-Generators

    -   [Bereitstellen eines UE-V-Einstellungs Vorlagen Katalogs](https://technet.microsoft.com/library/dn458942.aspx#deploycatalogue) , mit dem Sie die Speicherort Vorlagen für benutzerdefinierte Einstellungen speichern

Dieses Workflowdiagramm bietet eine allgemeine Übersicht über eine UE-v-Bereitstellung und die Entscheidungen, die bestimmen, wie UE-v in Ihrem Unternehmen bereitgestellt wird.

![deploymentworkflow](images/deploymentworkflow.png)

**Planen einer UE-V-Bereitstellung:** Zunächst möchten Sie etwas planen, damit Sie ermitteln können, welche UE-V-Komponenten bereitgestellt werden. Die Planung einer UE-V-Bereitstellung umfasst folgende Dinge:

-   [Entscheiden, ob Einstellungen für benutzerdefinierte Anwendungen synchronisiert werden sollen](#deciding)

    Dadurch wird bestimmt, ob Sie den UE-V-Generator während der Bereitstellung installieren, wodurch Sie benutzerdefinierte Speicherort Vorlagen für Einstellungen erstellen können. Sie umfasst Folgendes:

    Überprüfen Sie die [Einstellungen, die automatisch in einer UE-V-Bereitstellung synchronisiert werden](#autosyncsettings).

    [Ermitteln Sie, ob die Einstellungen für andere Anwendungen synchronisiert werden müssen](#determinesettingssync).

-   Lesen Sie [Weitere Überlegungen zur Bereitstellung von UE-V](#considerations), wie beispielsweise die Höchstverfügbarkeit und die Kapazitätsplanung.

-   [Voraussetzungen und unterstützte Konfigurationen für UE-V bestätigen](#prereqs)

## <a href="" id="deciding"></a>Entscheiden, ob Einstellungen für benutzerdefinierte Anwendungen synchronisiert werden sollen


In einer UE-V-Bereitstellung werden viele Einstellungen automatisch synchronisiert. Sie können UE-V aber auch so anpassen, dass Einstellungen für andere Anwendungen wie Branchen-und Drittanbieter-apps synchronisiert werden.

Die Entscheidung, ob UE-v die Einstellungen für benutzerdefinierte Anwendungen synchronisieren soll, ist wahrscheinlich der wichtigste Teil bei der Planung Ihrer UE-v-Bereitstellung. Die Themen in diesem Abschnitt werden Ihnen bei der Entscheidung helfen.

### <a href="" id="autosyncsettings"></a>Einstellungen, die in einer UE-V-Bereitstellung automatisch synchronisiert werden

Dieser Abschnitt enthält Informationen zu den Einstellungen, die in UE-V standardmäßig synchronisiert werden, einschließlich der folgenden:

Desktop Anwendungen, deren Einstellungen standardmäßig synchronisiert werden

Windows-Desktopeinstellungen, die standardmäßig synchronisiert werden

Eine Erklärung zur Unterstützung für die Synchronisierung der Windows-App-Einstellungen

Eine vollständige Liste der Einstellungen für Microsoft Office 2013, Microsoft Office 2010 und Microsoft Office 2007, die von UE-v synchronisiert werden, finden Sie unter [Vorlagen für die Benutzeroberflächen-Virtualisierung (UE-v) für Microsoft Office](https://www.microsoft.com/download/details.aspx?id=46367) .

### Standardmäßig synchronisierte Desktop Anwendungen in UE-v 2,1 und UE-v 2,1 SP1

Wenn Sie den UE-V 2,1-oder 2,1 SP1-Agent installieren, registriert er eine Standardgruppe von Einstellungen-Standort Vorlagen, mit denen die Einstellungswerte für diese gängigen Microsoft-Anwendungen erfasst werden.

**Tipp**  
**Synchronisierung von Microsoft Office 2007-Einstellungen** – in UE-V 2,1 und 2,1 SP1 ist eine Vorlage für den Einstellungs Speicherort standardmäßig nicht mehr für Office 2007-Anwendungen enthalten. Sie können jedoch weiterhin Office 2007-Vorlagen von UE-v 2,0 oder früher verwenden und die Vorlagen aus dem [UE-v-Vorlagenkatalog](https://go.microsoft.com/fwlink/p/?LinkID=246589)abrufen.



<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong>Anwendungskategorie</strong></th>
<th align="left"><strong>Beschreibung</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Microsoft Office 2010-Anwendungen</p>
<p>( <a href="https://www.microsoft.com/download/details.aspx?id=46367" data-raw-source="[Download a list of all settings synced](https://www.microsoft.com/download/details.aspx?id=46367)"> Eine Liste aller synchronisierten Einstellungen herunterladen </a> )</p></td>
<td align="left"><p>Microsoft Word 2010</p>
<p>Microsoft Excel 2010</p>
<p>Microsoft Outlook 2010</p>
<p>Microsoft Access 2010</p>
<p>Microsoft Project 2010</p>
<p>Microsoft PowerPoint 2010</p>
<p>Microsoft Publisher 2010</p>
<p>Microsoft Visio 2010</p>
<p>Microsoft SharePoint Workspace 2010</p>
<p>Microsoft InfoPath 2010</p>
<p>Microsoft lync 2010</p>
<p>Microsoft OneNote 2010</p>
<p>Microsoft SharePoint Designer 2010</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft Office 2013-Anwendungen</p>
<p>( <a href="https://www.microsoft.com/download/details.aspx?id=46367" data-raw-source="[Download a list of all settings synced](https://www.microsoft.com/download/details.aspx?id=46367)"> Eine Liste aller synchronisierten Einstellungen herunterladen </a> )</p></td>
<td align="left"><p>Microsoft Word 2013</p>
<p>Microsoft Excel 2013</p>
<p>Microsoft Outlook 2013</p>
<p>Microsoft Access 2013</p>
<p>Microsoft Project 2013</p>
<p>Microsoft PowerPoint 2013</p>
<p>Microsoft Publisher 2013</p>
<p>Microsoft Visio 2013</p>
<p>Microsoft InfoPath 2013</p>
<p>Microsoft lync 2013</p>
<p>Microsoft OneNote 2013</p>
<p>Microsoft SharePoint Designer 2013</p>
<p>Microsoft Office 2013 Upload Center</p>
<p>Microsoft OneDrive for Business 2013</p>
<p>Die Standort Vorlagen für UE-V 2,1 und 2,1 SP1 Microsoft Office 2013-Einstellungen umfassen eine verbesserte Unterstützung für Outlook-Signaturen. Wir haben die Synchronisierung von standardmäßigen Signatureinstellungen für neue, Antworten und weitergeleitete e-Mails hinzugefügt.</p>
<div class="alert">
<strong>Hinweis:</strong><br/><p>Für jedes Gerät, auf dem ein Benutzer seine Outlook-Signatur synchronisieren möchte, muss ein Outlook-Profil erstellt werden. Wenn das Profil noch nicht erstellt wurde, kann der Benutzer eine erstellen und dann Outlook auf diesem Gerät neu starten, um die Signatur Synchronisierung zu aktivieren.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p>Browser Optionen: Internet Explorer 8, Internet Explorer 9, Internet Explorer 10 und Internet Explorer 11</p></td>
<td align="left"><p>Favoriten, Startseite, Tabstopps und Symbolleisten.</p>
<div class="alert">
<strong>Hinweis:</strong><br/><p>UE-V führt keine Roaming-Einstellungen für Internet Explorer-Cookies durch.</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>Windows-Zubehör</p></td>
<td align="left"><p>Microsoft Calculator, Notepad, WordPad.</p></td>
</tr>
</tbody>
</table>



**Hinweis:**  
UE-V 2,1 SP1 synchronisiert keine Einstellungen zwischen dem Microsoft-Rechner in Windows 10 und dem Microsoft-Rechner in früheren Betriebssystemen.



### Standardmäßig synchronisierte Desktop Anwendungen in UE-V 2,0

Wenn Sie den UE-V 2,0-Agent installieren, registriert er eine Standardgruppe von Einstellungen-Standort Vorlagen, mit denen die Einstellungswerte für diese gängigen Microsoft-Anwendungen erfasst werden.

**Tipp**  
**Synchronisierung von Microsoft Office 2013-Einstellungen** – in UE-v 2,0 ist eine Vorlage für den einstellungensort nicht standardmäßig für Office 2013-Anwendungen enthalten, steht aber aus dem [UE-v-Vorlagenkatalog](https://go.microsoft.com/fwlink/p/?LinkID=246589)zum Download zur Verfügung. Beim [Synchronisieren von Office 2013 mit UE-V 2,0](synchronizing-office-2013-with-ue-v-20-both-uevv2.md) werden Details zu den unterstützten Vorlagen bereitgestellt, mit denen die Office 2013-Einstellungen synchronisiert werden.



<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong>Anwendungskategorie</strong></th>
<th align="left"><strong>Beschreibung</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Microsoft Office 2007-Anwendungen</p>
<p>( <a href="https://www.microsoft.com/download/details.aspx?id=46367" data-raw-source="[Download a list of all settings synced](https://www.microsoft.com/download/details.aspx?id=46367)"> Eine Liste aller synchronisierten Einstellungen herunterladen </a> )</p></td>
<td align="left"><p>Microsoft Access 2007</p>
<p>Microsoft Communicator 2007</p>
<p>Microsoft Excel 2007</p>
<p>Microsoft InfoPath 2007</p>
<p>Microsoft OneNote 2007</p>
<p>Microsoft Outlook 2007</p>
<p>Microsoft PowerPoint 2007</p>
<p>Microsoft Project 2007</p>
<p>Microsoft Publisher 2007</p>
<p>Microsoft SharePoint Designer 2007</p>
<p>Microsoft Visio 2007</p>
<p>Microsoft Word 2007</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft Office 2010-Anwendungen</p>
<p>( <a href="https://www.microsoft.com/download/details.aspx?id=46367" data-raw-source="[Download a list of all settings synced](https://www.microsoft.com/download/details.aspx?id=46367)"> Eine Liste aller synchronisierten Einstellungen herunterladen </a> )</p></td>
<td align="left"><p>Microsoft Word 2010</p>
<p>Microsoft Excel 2010</p>
<p>Microsoft Outlook 2010</p>
<p>Microsoft Access 2010</p>
<p>Microsoft Project 2010</p>
<p>Microsoft PowerPoint 2010</p>
<p>Microsoft Publisher 2010</p>
<p>Microsoft Visio 2010</p>
<p>Microsoft SharePoint Workspace 2010</p>
<p>Microsoft InfoPath 2010</p>
<p>Microsoft lync 2010</p>
<p>Microsoft OneNote 2010</p>
<p>Microsoft SharePoint Designer 2010</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Browser Optionen: Internet Explorer 8, Internet Explorer 9 und Internet Explorer 10</p></td>
<td align="left"><p>Favoriten, Startseite, Tabstopps und Symbolleisten.</p>
<div class="alert">
<strong>Hinweis:</strong><br/><p>UE-V führt keine Roaming-Einstellungen für Internet Explorer-Cookies durch.</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>Windows-Zubehör</p></td>
<td align="left"><p>Microsoft Calculator, Notepad, WordPad.</p></td>
</tr>
</tbody>
</table>



### <a href="" id="autosyncsettings2"></a>Standardmäßige Synchronisierung von Windows-Einstellungen

UE-V enthält Einstellungen für Standort Vorlagen, mit denen die Einstellungswerte für diese Windows-Einstellungen erfasst werden.

<table>
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Windows-Einstellungen</th>
<th align="left">Beschreibung</th>
<th align="left">Anwenden auf</th>
<th align="left">Exportieren auf</th>
<th align="left">Standardzustand</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Desktophintergrund</p></td>
<td align="left"><p>Derzeit aktiver Desktop Hintergrund oder Hintergrund.</p></td>
<td align="left"><p>Anmelden, entsperren, Remoteverbindung, geplante Aufgaben Ereignisse.</p></td>
<td align="left"><p>Abmelden, sperren, Remote Trennung, Benutzer: <strong> jetzt </strong> im Unternehmenseinstellungen-Center auf "synchronisieren" klicken oder Intervall für geplante Aufgaben</p></td>
<td align="left"><p>Aktiviert</p></td>
</tr>
<tr class="even">
<td align="left"><p>Erleichterte Bedienung</p></td>
<td align="left"><p>Barrierefreiheits-und Eingabeeinstellungen, Microsoft-Bildschirmlupe, Sprachausgabe und Bildschirmtastatur.</p></td>
<td align="left"><p>Nur Anmeldung.</p></td>
<td align="left"><p>Abmelden, Benutzer klickt <strong> jetzt </strong> im Unternehmenseinstellungen-Center auf "synchronisieren" oder geplantes Aufgaben Intervall</p></td>
<td align="left"><p>Aktiviert</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Desktop Einstellungen</p></td>
<td align="left"><p>Startmenü-und Taskleisteneinstellungen, Ordneroptionen, Standard Desktopsymbole, zusätzliche Uhren sowie Regions-und Spracheinstellungen.</p></td>
<td align="left"><p>Nur Anmeldung.</p></td>
<td align="left"><p>Abmelden, Benutzer klickt <strong> jetzt </strong> im Unternehmenseinstellungen-Center auf "synchronisieren" oder geplanter Vorgang</p></td>
<td align="left"><p>Aktiviert</p></td>
</tr>
</tbody>
</table>



**Hinweis:**  
Ab Windows 8 durchlaufen UE-V keine Einstellungen, die sich auf den Start Bildschirm beziehen, beispielsweise Elemente und Speicherorte. Darüber hinaus unterstützt UE-V keine Synchronisierung von angehefteten Taskleisten Elementen oder Windows-Dateiverknüpfungen.



**Wichtig**  
UE-V 2,1 SP1 durchstreift die Taskleisteneinstellungen zwischen Windows 10-Geräten. UE-V synchronisiert jedoch keine Taskleisteneinstellungen zwischen Windows 10-Geräten und Geräten, auf denen frühere Betriebssysteme ausgeführt werden.



<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Einstellungsgruppe</th>
<th align="left">Kategorie</th>
<th align="left">Erfassen</th>
<th align="left">„Anwenden“</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Anwendungseinstellungen</strong></p></td>
<td align="left"><p>Windows-Apps  </p></td>
<td align="left"><p>APP schließen</p>
<p>Change-Ereignis für Windows-App-Einstellungen</p></td>
<td align="left"><p>Starten des UE-V-App-Monitors beim Start</p>
<p>APP öffnen</p>
<p>Change-Ereignis für Windows-App-Einstellungen</p>
<p>Eintreffen eines Einstellungs Pakets</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p>Desktopanwendungen</p></td>
<td align="left"><p>Anwendung wird geschlossen</p></td>
<td align="left"><p>Anwendung wird geöffnet und geschlossen</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Desktop Einstellungen</strong></p></td>
<td align="left"><p>Desktophintergrund</p></td>
<td align="left"><p>Sperren oder abmelden</p></td>
<td align="left"><p>Logon, entsperren, Remote Connect, Benachrichtigung über die Ankunft des neuen Pakets, Benutzer klickt <strong> jetzt </strong> im Unternehmenseinstellungen Center auf "synchronisieren" oder geplanter Task wird ausgeführt.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p>Erleichterte Bedienung (häufig – Barrierefreiheit, Sprachausgabe, Bildschirmlupe, Bildschirmtastatur)</p></td>
<td align="left"><p>Sperren oder abmelden</p></td>
<td align="left"><p>Anmelde</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p>Erleichterte Bedienung (Shell-Audio, Barrierefreiheit, Tastatur, Maus)</p></td>
<td align="left"><p>Sperren oder abmelden</p></td>
<td align="left"><p>Anmelden, entsperren, Remoteverbindung, Benachrichtigung über das Eintreffen neuer Pakete, Benutzer klickt <strong> auf "Jetzt synchronisieren" </strong> im Unternehmenseinstellungen-Center oder geplante Task-Läufe</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p>Desktop Einstellungen</p></td>
<td align="left"><p>Sperren oder abmelden</p></td>
<td align="left"><p>Anmelde</p></td>
</tr>
</tbody>
</table>



### UE-V – Unterstützung für Windows-apps

Für Windows-apps gibt der App-Entwickler die Einstellungen an, die synchronisiert werden. Sie können angeben, welche Windows-Apps für die Synchronisierung von Einstellungen aktiviert sind.

Um eine Liste der Windows-apps anzuzeigen, die die Einstellungen auf einem Computer mit dem Namen der paketfamilie, dem aktivierten Status und der aktivierten Quelle synchronisieren können, geben Sie an einer Windows PowerShell-Eingabeaufforderung Folgendes ein: `Get-UevAppxPackage`

**Hinweis:**  
Ab Windows 8 synchronisiert UE-V keine Windows-App-Einstellungen, wenn der Domänenbenutzer seine Anmeldeinformationen mit seinem Microsoft-Konto verknüpft. Diese Verknüpfung synchronisiert Einstellungen mit Microsoft OneDrive so UE-V, wodurch die Synchronisierung der Windows-App-Einstellungen deaktiviert wird.



### UE-V-Unterstützung für Roaming-Drucker

Mit UE-V 2,1 SP1 können Netzwerkdrucker zwischen Geräten Roaming durchlaufen, damit ein Benutzer auf seine Netzwerkdrucker zugreifen kann, wenn er sich bei einem beliebigen Gerät im Netzwerk anmeldet. Dies umfasst das Roaming des Druckers, den Sie als Standard festlegen.

Für das Drucker-Roaming in UE-V ist eines der folgenden Szenarien erforderlich:

-   Der Druckserver kann den erforderlichen Treiber herunterladen, wenn er auf ein neues Gerät wechselt.

-   Der Treiber für den Roaming-Netzwerkdrucker ist auf allen Geräten vorinstalliert, die auf diesen Netzwerkdrucker zugreifen müssen.

-   Der Druckertreiber kann über Windows Update abgerufen werden.

**Hinweis:**  
Das UE-V Printer-Roaming-Feature unterstützt **keine** Druckereinstellungen oder-Einstellungen, beispielsweise das doppelseitige Drucken.



### <a href="" id="determinesettingssync"></a>Ermitteln, ob Einstellungen für andere Anwendungen synchronisiert werden müssen

Nachdem Sie die Einstellungen überprüft haben, die automatisch in einer UE-v-Bereitstellung synchronisiert werden, möchten Sie entscheiden, ob Sie die Einstellungen für andere Anwendungen synchronisieren, da dadurch festgelegt wird, wie Sie UE-v im gesamten Unternehmen bereitstellen.

Wenn Sie als Administrator berücksichtigen, welche Desktopanwendungen in Ihre UE-V-Lösung einbezogen werden sollen, sollten Sie berücksichtigen, welche Einstellungen von Benutzern angepasst werden können und wie und wo die Anwendung die Einstellungen speichert. Nicht alle Desktopanwendungen verfügen über Einstellungen, die angepasst oder regelmäßig von Benutzern angepasst werden können. Darüber hinaus können nicht alle Desktopanwendungen-Einstellungen sicher über mehrere Computer oder Umgebungen synchronisiert werden.

Im Allgemeinen können Sie Einstellungen synchronisieren, die den folgenden Kriterien entsprechen:

-   Einstellungen, die in Benutzer zugänglichen Speicherorten gespeichert sind. Synchronisieren Sie beispielsweise nicht die Einstellungen, die in System32 oder außerhalb des HKEY \ _CURRENT \ _User (HKCU)-Abschnitts der Registrierung gespeichert sind.

-   Einstellungen, die nicht für den jeweiligen Computer spezifisch sind. Schließen Sie beispielsweise Netzwerk-oder Hardwarekonfigurationen aus.

-   Einstellungen, die zwischen Computern synchronisiert werden können, ohne dass ein Risiko für beschädigte Daten besteht. Verwenden Sie beispielsweise keine Einstellungen, die in einer Datenbankdatei gespeichert sind.

### <a href="" id="checklistsettingssync"></a>Prüfliste für die Auswertung benutzerdefinierter Anwendungen

Wenn Sie sich für die Synchronisierung von Einstellungen für andere Anwendungen entschieden haben, können Sie anhand dieser Checkliste ermitteln, welche Anwendungen Sie aufnehmen.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left">Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Enthält diese Anwendung Einstellungen, die vom Benutzer angepasst werden können?</p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Ist es für den Benutzer wichtig, dass diese Einstellungen synchronisiert werden?</p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Werden diese Benutzereinstellungen bereits von einer Anwendungs Verwaltungs-oder Einstellungsrichtlinien Lösung verwaltet? UE-V wendet Anwendungseinstellungen beim Start von Anwendungen und Windows-Einstellungen bei Anmeldung, entsperren oder Remote Verbindungsereignissen an. Wenn Sie UE-V mit anderen Lösungen für die Freigabe von Einstellungen verwenden, können Benutzer in synchronisierten Einstellungen Inkonsistenzen erfahren.</p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Sind die Anwendungseinstellungen für den Computer spezifisch? Anwendungseinstellungen und Anpassungen, die Hardware oder bestimmten Computerkonfigurationen zugeordnet sind, werden nicht konsistent zwischen Sitzungen synchronisiert und können zu einer unzureichenden Anwendungsumgebung führen.</p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Speichert die Anwendung die Einstellungen im Verzeichnis "Programmdateien" oder im Dateiverzeichnis, das sich im <strong> Verzeichnis Benutzer </strong> [Benutzername] &lt; Strong &gt; AppData </strong> &lt; Strong &gt; LocalLow befindet </strong> ? Anwendungsdaten, die an einem dieser Speicherorte gespeichert sind, sollten normalerweise nicht mit dem Benutzer synchronisiert werden, da diese Daten für den Computer spezifisch sind oder weil die Daten für die Synchronisierung zu groß sind.</p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Speichert die Anwendung alle Einstellungen in einer Datei, die andere Anwendungsdaten enthält, die nicht synchronisiert werden sollen? UE-V synchronisiert Dateien als einzelne Einheit. Wenn Einstellungen in Dateien gespeichert werden, die Anwendungsdaten außer Einstellungen enthalten, kann das Synchronisieren dieser zusätzlichen Daten zu einer unzureichenden Anwendungsumgebung führen.</p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Wie groß sind die Dateien, die die Einstellungen enthalten? Die Leistung der Synchronisierung von Einstellungen kann von umfangreichen Dateien beeinflusst werden. Das einbeziehen großer Dateien kann sich auf die Leistung der Synchronisierung von Einstellungen auswirken.</p></td>
</tr>
</tbody>
</table>



## <a href="" id="considerations"></a>Weitere Überlegungen beim Vorbereiten einer UE-V-Bereitstellung


Sie sollten diese Aspekte auch berücksichtigen, wenn Sie die Bereitstellung von UE-V vorbereiten:

-   [Verwalten der Anmeldeinformationen-Synchronisierung](#creds)

-   [Synchronisierung der Windows-App-Einstellungen](#appxsettings)

-   [Benutzerdefinierte Standort Vorlagen für UE-V-Einstellungen](#custom)

-   [Unbeabsichtigte Konfigurationen für Benutzereinstellungen](#prevent)

-   [Leistung und Kapazität](#capacity)

-   [Hohe Verfügbarkeit](#high)

-   [Synchronisierung des Computer Takts](#clocksync)

### <a href="" id="creds"></a>Verwalten der Anmeldeinformationen für die Synchronisierung in UE-v 2,1 und UE-v 2,1 SP1

Viele Enterprise-Anwendungen, einschließlich Microsoft Outlook und lync, fordern Benutzer bei der Anmeldung zur Eingabe Ihrer Domänenanmeldeinformationen auf. Benutzer haben die Möglichkeit, Ihre Anmeldeinformationen auf einem Datenträger zu speichern, um zu verhindern, dass Sie bei jedem Öffnen dieser Anwendungen eingegeben werden müssen. Durch das Aktivieren der Synchronisierung von Roaming-Anmeldeinformationen können Benutzer ihre Anmeldeinformationen auf einem Computer speichern und Sie nicht auf jedem Computer, den Sie in Ihrer Umgebung verwenden, erneut eingeben. Benutzer können einige Domänenanmeldeinformationen mit UE-V 2,1 und 2,1 SP1 synchronisieren.

**Wichtig**  
Die Synchronisierung der Anmeldeinformationen ist standardmäßig deaktiviert. Sie müssen die Anmeldeinformationen-Synchronisierung während der Bereitstellung explizit aktivieren, um dieses Feature zu implementieren.



UE-V 2,1 und 2,1 SP1 können Enterprise-Anmeldeinformationen synchronisieren, jedoch keine Roaming-Anmeldeinformationen, die nur für die Verwendung auf dem lokalen Computer vorgesehen sind.

Anmeldeinformationen sind synchrone Einstellungen, was bedeutet, dass Sie bei der ersten Anmeldung an Ihrem Computer nach UE-V synchronisiert werden.

Die Synchronisierung der Anmeldeinformationen wird durch eine eigene Einstellungen-Speicherort Vorlage verwaltet, die standardmäßig deaktiviert ist. Sie können diese Vorlage über die für andere Vorlagen verwendeten Methoden aktivieren oder deaktivieren. Der Vorlagenbezeichner für dieses Feature lautet RoamingCredentialSettings.

**Wichtig**  
Wenn Sie das Roaming von Active Directory-Anmeldeinformationen in Ihrer Umgebung verwenden, empfiehlt es sich, die Vorlage für die Roaming-Anmeldeinformationen in UE-V nicht zu aktivieren.



Verwenden Sie eine der folgenden Methoden, um die Synchronisierung der Anmeldeinformationen zu aktivieren:

-   Unternehmenseinstellungen (Center)

-   PowerShell

-   Gruppenrichtlinie

**Hinweis:**  
Anmeldeinformationen werden während der Synchronisierung verschlüsselt.



[Unternehmens Einstellungs Center](https://technet.microsoft.com/library/dn458903.aspx)**:** aktivieren Sie das Kontrollkästchen Einstellungen für Roaming-Anmeldeinformationen unter Windows-Einstellungen, um die Synchronisierung der Anmeldeinformationen zu aktivieren. Deaktivieren Sie das Kontrollkästchen, um es zu deaktivieren. Dieses Kontrollkästchen wird nur im Unternehmenseinstellungen-Center angezeigt, wenn Ihr Konto nicht so konfiguriert ist, dass die Einstellungen mit einem Microsoft-Konto synchronisiert werden.

[PowerShell](https://technet.microsoft.com/library/dn458937.aspx)**:** dieses PowerShell-Cmdlet ermöglicht die Synchronisierung von Anmeldeinformationen:

``` syntax
Enable-UevTemplate RoamingCredentialSettings
```

Dieses PowerShell-Cmdlet deaktiviert die Synchronisierung von Anmeldeinformationen:

``` syntax
Disable-UevTemplate RoamingCredentialSettings
```

[Gruppenrichtlinie](https://technet.microsoft.com/library/dn458893.aspx)**:** Sie müssen [die neueste MDOP-ADMX-Vorlage bereitstellen](https://go.microsoft.com/fwlink/p/?LinkId=393944) , um die Synchronisierung von Anmeldeinformationen über Gruppenrichtlinien zu ermöglichen. Die Synchronisierung der Anmeldeinformationen wird mit den Windows-Einstellungen verwaltet. Wenn Sie dieses Feature mit Gruppenrichtlinien verwalten möchten, aktivieren Sie die Richtlinie Windows-Einstellungen synchronisieren.

1.  Öffnen Sie den Gruppenrichtlinien-Editor, und navigieren Sie zu **Benutzerkonfiguration – Administrative Vorlagen – Windows-Komponenten – Microsoft User Experience Virtualization**.

2.  Doppelklicken Sie auf **Windows-Einstellungen synchronisieren**.

3.  Wenn diese Richtlinie aktiviert ist, können Sie die Synchronisierung der Anmeldeinformationen aktivieren, indem Sie das Kontrollkästchen **Roaming-Anmeldeinformationen** aktivieren, oder die Synchronisierung von Anmeldeinformationen deaktivieren, indem Sie Sie deaktivieren.

4.  Klicken Sie auf **OK**.

### Von UE-V synchronisierte Speicherorte für Anmeldeinformationen

Von Anwendungen gespeicherte Anmeldeinformationsdateien an den folgenden Speicherorten werden synchronisiert:

-   %UserProfile%\\AppData\\Roaming\\Microsoft\\Credentials\\

-   %UserProfile%\\AppData\\Roaming\\Microsoft\\Crypto\\

-   %UserProfile%\\AppData\\Roaming\\Microsoft\\Protect\\

-   %UserProfile%\\AppData\\Roaming\\Microsoft\\SystemCertificates\\

An anderen Speicherorten gespeicherte Anmeldeinformationen werden nicht von UE-V synchronisiert.

### <a href="" id="appxsettings"></a>Synchronisierung der Windows-App-Einstellungen

UE-V verwaltet die Synchronisierung der Windows-App-Einstellungen auf drei Arten:

-   **Synchronisieren von Windows-apps:** Zulassen oder Verweigern einer Windows-App-Synchronisierung

-   **Windows-App-Liste:** Synchronisieren einer Liste von Windows-apps

-   Nicht **aufgelistetes Standard Synchronisierungsverhalten:** Bestimmen Sie das Synchronisierungsverhalten von Windows-apps, die nicht in der Windows-App-Liste enthalten sind.

Weitere Informationen finden Sie in der [Windows-App-Liste](https://technet.microsoft.com/library/dn458925.aspx#win8applist).

### <a href="" id="custom"></a>Benutzerdefinierte Standort Vorlagen für UE-V-Einstellungen

Wenn Sie UE-v zum Synchronisieren von Einstellungen für benutzerdefinierte Anwendungen bereitstellen, verwenden Sie den UE-v-Generator, um benutzerdefinierte Speicherort Vorlagen für diese Desktopanwendungen zu erstellen. Nachdem Sie eine Standort Vorlage für benutzerdefinierte Einstellungen in einer Testumgebung erstellt und getestet haben, können Sie die Einstellungen-Speicherort Vorlagen auf Computern im Unternehmen bereitstellen.

Speicherort Vorlagen für benutzerdefinierte Einstellungen müssen mit einer vorhandenen Bereitstellungsinfrastruktur bereitgestellt werden, wie eine ESD-Methode (Enterprise Software Distribution) wie System Center Configuration Manager, mit Einstellungen oder durch Konfigurieren eines UE-V-Einstellungs Vorlagen Katalogs. Vorlagen, die mit Configuration Manager oder Gruppenrichtlinien bereitgestellt werden, müssen mit UE-V WMI oder Windows PowerShell registriert werden.

Weitere Informationen zu den Standort Vorlagen für benutzerdefinierte Einstellungen finden Sie unter [Bereitstellen von UE-V 2. x für benutzerdefinierte Anwendungen](deploy-ue-v-2x-for-custom-applications-new-uevv2.md). Weitere Informationen zur Verwendung von UE-v mit Configuration Manager finden Sie unter [Konfigurieren von UE-v 2. x mit System Center Configuration Manager 2012](configuring-ue-v-2x-with-system-center-configuration-manager-2012-both-uevv2.md).

### <a href="" id="prevent"></a>Verhindern der unbeabsichtigten Konfiguration von Benutzereinstellungen

UE-V downloadet neue Benutzereinstellungsinformationen von einem Einstellungs Speicherort und wendet die Einstellungen in diesen Fällen auf den lokalen Computer an:

-   Jedes Mal, wenn eine Anwendung gestartet wird, die über eine registrierte UE-V-Vorlage verfügt.

-   Wenn sich ein Benutzer an einem Computer anmeldet.

-   Wenn ein Benutzer einen Computer entsperrt.

-   Wenn eine Verbindung mit einem Remote Desktopcomputer hergestellt wird, auf dem UE-V installiert ist.

-   Wenn der geplante Task der Synchronisierungs Controller Anwendung ausgeführt wird.

Wenn UE-V auf Computer a und Computer B installiert ist und die für die Anwendung gewünschten Einstellungen sich auf Computer a befinden, sollte Computer a die Anwendung zuerst öffnen und schließen. Wenn die Anwendung zuerst auf Computer b geöffnet und geschlossen wird, werden die Anwendungseinstellungen auf Computer A für die Anwendungseinstellungen auf Computer b konfiguriert. die Einstellungen werden pro Anwendung zwischen Computern synchronisiert. Im Laufe der Zeit werden die Einstellungen zwischen Computern konsistent, während Sie mit bevorzugten Einstellungen geöffnet und geschlossen werden.

Dieses Szenario gilt auch für Windows-Einstellungen. Wenn die Windows-Einstellungen auf Computer B mit den Windows-Einstellungen auf Computer a identisch sein sollten, sollte sich der Benutzer zuerst anmelden und den Computer abmelden.

Wenn die Benutzereinstellungen, die der Benutzer wünscht, in der falschen Reihenfolge angewendet werden, können Sie wiederhergestellt werden, indem Sie einen Wiederherstellungsvorgang für die jeweilige Anwendung oder Windows-Konfiguration auf dem Computer ausführen, auf dem die Einstellungen überschrieben wurden. Weitere Informationen finden Sie unter [Verwalten der administrativen Sicherung und Wiederherstellung in UE-V 2. x](manage-administrative-backup-and-restore-in-ue-v-2x-new-topic-for-21.md).

### <a href="" id="capacity"></a>Leistungs-und Kapazitätsplanung

Geben Sie Ihre Anforderungen für UE-V mit Standardfestplatten Kapazität und Netzwerkstatusüberwachung an.

UE-V verwendet eine SMB-Freigabe (Server Message Block) für die Speicherung von Einstellungspaketen. Die Größe der Einstellungs Pakete hängt von den Einstellungsinformationen für die einzelnen Anwendungen ab. Während die meisten Einstellungs Pakete klein sind, kann die Synchronisierung von potenziell umfangreichen Dateien, wie etwa Desktop Bildern, zu einer schlechten Leistung führen, insbesondere bei langsameren Netzwerken.

Wenn Sie Probleme mit der Netzwerklatenz verringern möchten, erstellen Sie die Speicherorte für Einstellungen in den lokalen Netzwerken, in denen sich die Computer der Benutzer befinden. Für den Speicherort der Einstellungen empfehlen wir pro Nutzer 20 MB Speicherplatz.

Standardmäßig wird die UE-V-Synchronisierung nach 2 Sekunden durchgeführt, um zu hohen Verzögerungen aufgrund eines umfangreichen Einstellungs Pakets zu verhindern. Sie können die Einstellung SyncMethod = SyncProvider mithilfe von [Gruppenrichtlinienobjekten](https://technet.microsoft.com/library/dn458893.aspx)konfigurieren.

### <a href="" id="high"></a>Höhere Verfügbarkeit für UE-V

Der Speicherstandort und der Einstellungs Vorlagenkatalog für UE-V-Einstellungen unterstützen das Speichern von Benutzerdaten auf einer beliebigen schreibbaren Freigabe. Führen Sie die folgenden Kriterien aus, um eine höhere Verfügbarkeit zu gewährleisten:

-   Formatieren Sie das Speichervolume mit einem NTFS-Dateisystem.

-   Die Freigabe kann Distributed File System (DFS) verwenden, es gibt jedoch Einschränkungen.
Insbesondere wird die verteilte Datei systemreplizierung (DFS-R) mit einer einzelnen Zielkonfiguration mit oder ohne einen verteilten Dateisystem-Namespace (DFS-N) unterstützt.
Ebenso wird nur eine Zielkonfiguration mit DFS-N unterstützt.
Detaillierte Informationen finden Sie [in der Microsoft-Support-Anweisung rund um replizierte Benutzerprofildaten](https://go.microsoft.com/fwlink/p/?LinkId=313991) und auch [Informationen zur Microsoft-Supportrichtlinie für ein DFS-R-und DFS-N-Bereitstellungsszenario](https://support.microsoft.com/kb/2533009).

    Da SYSVOL auch DFS-R für die Replikation verwendet, kann SYSVOL nicht für die UE-V-Datendatei Replikation verwendet werden.

-   Konfigurieren Sie die Freigabeberechtigungen und NTFS-Zugriffssteuerungslisten (ACLs) gemäß [den Angaben unter Bereitstellen des Speicherorts für die Einstellungen für UE-V 2. x](https://technet.microsoft.com/library/dn458891.aspx#ssl).

-   Verwenden Sie das Dateiserver-Clustering zusammen mit dem UE-V-Agent, um den Zugriff auf Kopien von Benutzerzustandsdaten im Falle von Kommunikationsfehlern zu ermöglichen.

-   Sie können die Einstellungen Speicherpfad Daten (Benutzerdaten) und Vorlagen für Vorlagen für Vorlagen auf gruppierten Freigaben, auf DFS-N-Freigaben oder auf beiden speichern.

### <a href="" id="clocksync"></a>Synchronisieren von Computeruhren für die Synchronisierung von UE-V-Einstellungen

Computer, auf denen der UE-V-Agent ausgeführt wird, müssen einen Zeitserver verwenden, um eine konsistente Einstellungen zu gewährleisten. UE-V verwendet Zeitstempel, um festzustellen, ob die Einstellungen vom Speicherort der Einstellungen synchronisiert werden müssen. Wenn die Uhrzeit des Computers falsch ist, können ältere Einstellungen neuere Einstellungen überschreiben, oder die neuen Einstellungen werden möglicherweise nicht am Speicherort des Einstellungs Speichers gespeichert.

## <a href="" id="prereqs"></a>Voraussetzungen und unterstützte Konfigurationen für UE-V bestätigen


Bevor Sie fortfahren, stellen Sie sicher, dass Ihre Umgebung die folgenden Voraussetzungen für die Ausführung von UE-V umfasst.

<table style="width:100%;">
<colgroup>
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong>Betriebssystem</strong></th>
<th align="left"><strong>Edition</strong></th>
<th align="left"><strong>Service Pack</strong></th>
<th align="left"><strong>System Architektur</strong></th>
<th align="left"><strong>Windows PowerShell</strong></th>
<th align="left"><strong>Microsoft .NET Framework</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows7</p></td>
<td align="left"><p>Ultimate-, Enterprise-oder Professional-Edition</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>32 Bit oder 64 Bit</p></td>
<td align="left"><p>Windows PowerShell 3,0 oder höher</p></td>
<td align="left"><p>.NET Framework 4,5 oder höher für UE-V 2,1.</p>
<p>.NET Framework 4 oder höher für UE-V 2,0.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2008 R2</p></td>
<td align="left"><p>Standard, Enterprise, Datacenter oder Web Server</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>64Bit</p></td>
<td align="left"><p>Windows PowerShell 3,0 oder höher</p></td>
<td align="left"><p>.NET Framework 4,5 oder höher für UE-V 2,1.</p>
<p>.NET Framework 4 oder höher für UE-V 2,0.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows 8 und Windows 8,1</p></td>
<td align="left"><p>Enterprise oder pro</p></td>
<td align="left"><p>Keine</p></td>
<td align="left"><p>32 Bit oder 64 Bit</p></td>
<td align="left"><p>Windows PowerShell 3,0 oder höher</p></td>
<td align="left"><p>.NET Framework 4,5 oder höher</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows 10, Version vor 1607</p>
<div class="alert">
<strong>Hinweis:</strong><br/><p>Nur UE-V 2,1 SP1 unterstützt Windows 10, Pre-1607-Version</p>
</div>
<div>

</div></td>
<td align="left"><p>Enterprise oder pro</p></td>
<td align="left"><p>Keine</p></td>
<td align="left"><p>32 Bit oder 64 Bit</p></td>
<td align="left"><p>Windows PowerShell 3,0 oder höher</p></td>
<td align="left"><p>.NET Framework 4.6</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server 2012 und Windows Server 2012 R2</p></td>
<td align="left"><p>Standard oder Rechenzentrum</p></td>
<td align="left"><p>Keine</p></td>
<td align="left"><p>64Bit</p></td>
<td align="left"><p>Windows PowerShell 3,0 oder höher</p></td>
<td align="left"><p>.NET Framework 4,5 oder höher</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2016</p></td>
<td align="left"><p>Standard oder Rechenzentrum</p></td>
<td align="left"><p>Keine</p></td>
<td align="left"><p>64Bit</p></td>
<td align="left"><p>Windows PowerShell 3,0 oder höher</p></td>
<td align="left"><p>.NET Framework 4,6 oder höher</p></td>
</tr>
</tbody>
</table>



Auch...

-   **MDOP-Lizenz:** Diese Technologie ist Teil des Microsoft Desktop Optimization Pack (MDOP). Unternehmenskunden können MDOP mit Microsoft Software Assurance erhalten. Weitere Informationen zur Microsoft-Software Assurance und zum Erwerb von MDOP finden Sie unter wie erhalte ich MDOP ( https://go.microsoft.com/fwlink/p/?LinkId=322049) .

-   **Administratoranmeldeinformationen** für jeden Computer, auf dem die Installation erfolgen soll

**Hinweis:**  

-   Ab Windows 10, Version 1607, ist UE-V in [Windows 10 für Enterprise](https://www.microsoft.com/WindowsForBusiness/windows-for-enterprise) enthalten und nicht mehr Teil des Microsoft-Desktop Optimierungs Pakets.

-   Das Windows PowerShell-Feature UE-v des UE-v-Agents erfordert .NET Framework 4 oder höher und Windows PowerShell 3,0 oder höher, um aktiviert zu werden. Laden Sie Windows PowerShell 3,0 [hier](https://go.microsoft.com/fwlink/?LinkId=309609)herunter.

-   Installieren Sie .NET Framework 4 oder .NET Framework 4,5 auf Computern, auf denen das BetriebssystemWindows 7 oder Windows Server 2008 R2 ausgeführt wird. Die Betriebssysteme Windows 8, Windows 8,1 und Windows Server 2012 sind mit .NET Framework 4,5 installiert. Das Betriebssystem Windows 10 ist mit .NET Framework 4,6 installiert.
-   Die Richtlinie "Roaming-Cache löschen" für obligatorische Profile wird von UE-V nicht unterstützt und sollte nicht verwendet werden.



Es gibt keine speziellen RAM-Anforderungen (Random Access Memory), die für UE-V spezifisch sind.

### Synchronisierung von Einstellungen über den Synchronisierungsanbieter

Der Synchronisierungsanbieter ist die Standardeinstellung für Benutzer, die einen lokalen Cache mit dem Speicherort für Einstellungen in diesen Instanzen synchronisiert:

-   Anmelden/Abmelden

-   Sperren/Entsperren

-   Verbinden/Trennen des Remote Desktops

-   Anwendung öffnen/schließen

Ein geplanter Task verwaltet diese Synchronisierung von Einstellungen alle 30 Minuten oder durch bestimmte Trigger-Ereignisse für bestimmte Anwendungen. Weitere Informationen finden Sie unter [Ändern der Häufigkeit von geplanten Aufgaben in UE-V 2. x](changing-the-frequency-of-ue-v-2x-scheduled-tasks-both-uevv2.md).

Der UE-V-Agent synchronisiert Benutzereinstellungen für Computer, die nicht immer mit dem Unternehmensnetzwerk (Remotecomputer und Laptops) verbunden sind, und Computern, die immer mit dem Netzwerk verbunden sind (Computer, auf denen Windows Server ausgeführt wird, und Host Virtual Desktop Interface (VDI)-Sitzungen).

**Synchronisierung für Computer mit immer verfügbaren Verbindungen:** Wenn Sie UE-v auf Computern verwenden, die immer mit dem Netzwerk verbunden sind, müssen Sie den UE-v-Agent so konfigurieren, dass die Einstellungen mithilfe des *SyncMethod = None* -Parameters synchronisiert werden, der den Einstellungen-Speicherserver als standardmäßige Netzwerkfreigabe behandelt. In dieser Konfiguration kann der UE-V-Agent so konfiguriert werden, dass er benachrichtigt, wenn der Import der Anwendungseinstellungen verzögert wird.

Aktivieren Sie diese Konfiguration mithilfe einer der folgenden Methoden:

-   Legen Sie während der UE-V-Installation an der Eingabeaufforderung oder in einer Batchdatei den AgentSetup.exe-Parameter *SyncMethod = None*. [Die Bereitstellung des UE-V 2. x-Agents](https://technet.microsoft.com/library/dn458891.aspx#agent) bietet weitere Informationen.

-   Verwenden Sie nach der UE-V-Installation das Feature einstellungenverwaltung in System Center 2012 Configuration Manager oder die MDOP ADMX-Vorlagen, um die *SyncMethod = None* -Konfiguration zu drücken.

-   Verwenden Sie Windows PowerShell oder WMI (Windows Management Instrumentation), um die *SyncMethod = None* -Konfiguration einzurichten.

    **Hinweis:**  
    Diese beiden letzten Methoden funktionieren nicht für Umgebungen mit Pooling Virtual Desktop Infrastructure (VDI).



Sie müssen den Computer neu starten, bevor die Einstellungen für die Synchronisierung beginnen.

**Hinweis:**  
Wenn Sie *SyncMethod = None*festlegen, werden Änderungen an den Einstellungen direkt auf dem Server gespeichert. Wenn die Netzwerkverbindung mit dem Einstellungsspeicher Pfad nicht gefunden wird, werden die Einstellungsänderungen auf dem Gerät zwischengespeichert und beim nächsten Ausführen des Synchronisierungsanbieters synchronisiert. Wenn der Speicherpfad für Einstellungen nicht gefunden wird und das Benutzerprofil bei der Abmeldung aus einer gepoolten VDI-Umgebung entfernt wird, gehen die Änderungen an den Einstellungen verloren, und der Benutzer muss die Änderung erneut anwenden, wenn der Computer erneut mit dem Speicherpfad der Einstellungen verbunden ist.



**Synchronisierung für externe Synchronisierungs Module:** Der *SyncMethod = External* -Parameter gibt an, dass wenn UE-V-Einstellungen in einen lokalen Ordner auf dem Benutzer Computer geschrieben werden, dann ein externes Synchronisierungsmodul (wie OneDrive for Business, Arbeitsordner, SharePoint oder Dropbox) verwendet werden kann, um diese Einstellungen auf die verschiedenen Computer anzuwenden, auf die Benutzer zugreifen.

**Unterstützung für freigegebene VDI-Sitzungen:** UE-V 2,1 und 2,1 SP1 bieten Unterstützung für VDI-Sitzungen, die für Endbenutzer freigegeben werden. Sie können eine spezielle VDI-Vorlage registrieren und konfigurieren, die sicherstellt, dass UE-V alle Funktionen für nicht persistente VDI-Sitzungen intakt hält.

**Hinweis:**  
Wenn Sie den VDI-Modus nicht für nicht persistente VDI-Sitzungen aktivieren, funktionieren bestimmte Features nicht, beispielsweise " [sichern/wiederherstellen" und "Letzte als funktionierend bekannt" (LKG)](https://technet.microsoft.com/library/dn878331.aspx).



Die VDI-Vorlage wird mit UE-V 2,1 und 2,1 SP1 bereitgestellt und ist in der Regel nach der Installation hier verfügbar: c:\\Programme c:\\Programme\\Microsoft-Benutzeroberfläche Virtualization\\Templates\\VdiState.xml

### Voraussetzungen für die Unterstützung des UE-V-Generators

Installieren Sie den UE-V-Generator auf dem Computer, der zum Erstellen benutzerdefinierter Einstellungen für Standort Vorlagen verwendet wird. Dieser Computer sollte in der Lage sein, die Anwendungen auszuführen, deren Einstellungen synchronisiert werden. Sie müssen ein Mitglied der Gruppe Administratoren auf dem Computer sein, auf dem die UE-V-Generator Software ausgeführt wird.

Der UE-V-Generator muss auf einem Computer installiert sein, auf dem ein NTFS-Dateisystem verwendet wird. Die UE-V-Generator Software erfordert .NET Framework 4. Weitere Informationen finden Sie unter [Bereitstellen von UE-V 2. x für benutzerdefinierte Anwendungen](deploy-ue-v-2x-for-custom-applications-new-uevv2.md).

## Weitere Ressourcen für dieses Produkt


-   [Microsoft User Experience Virtualization (UE-V) 2. x](index.md)

-   [Erste Schritte mit UE-V 2.x](get-started-with-ue-v-2x-new-uevv2.md)

-   [Verwalten von UE-V 2. x](administering-ue-v-2x-new-uevv2.md)

-   [Problembehandlung bei UE-V 2. x](troubleshooting-ue-v-2x-both-uevv2.md)

-   [Technische Referenz für UE-V 2.x](technical-reference-for-ue-v-2x-both-uevv2.md)














