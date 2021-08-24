---
title: Vorbereiten einer UE-V 2.x-Bereitstellung
description: Vorbereiten einer UE-V 2.x-Bereitstellung
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
ms.openlocfilehash: 3e4d4b69975deda473372345733d8e8593a4775d
ms.sourcegitcommit: 3e0500abde44d6a09c7ac8e3caf5e25929b490a4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2021
ms.locfileid: "11910530"
---
# <a name="prepare-a-ue-v-2x-deployment"></a>Vorbereiten einer UE-V 2.x-Bereitstellung


Es gibt einige Planungen und Vorbereitungen, bevor Sie Microsoft User Experience Virtualization (UE-V) 2.0 oder 2.1 als Lösung für die Synchronisierung von Einstellungen zwischen Geräten bereitstellen, auf die Benutzer in Ihrem Unternehmen zugreifen. In diesem Thema erfahren Sie, welche Art von Bereitstellung Sie durchführen werden und welche Vorbereitungen Sie im Voraus treffen können, damit die Bereitstellung erfolgreich ist.

Sehen wir uns zunächst die Aufgaben an, die Sie für die Bereitstellung UE-V ausführen:

-   Planen der bereitstellung UE-V

    Bevor Sie etwas bereitstellen, sollten Sie zunächst etwas planen, damit Sie ermitteln können, welche UE-V Features Sie bereitstellen werden. Wenn Sie diese Seite verlassen, stellen Sie also sicher, dass Sie zurückkehren und die folgenden Planungsinformationen lesen.

-   [Bereitstellen der erforderlichen Features für UE-V 2.x](deploy-required-features-for-ue-v-2x-new-uevv2.md)

    Für jede UE-V Bereitstellung sind die folgenden Aktivitäten erforderlich:

    -   [Definieren eines Speicherorts für Einstellungen](https://technet.microsoft.com/library/dn458891.aspx#ssl)

    -   [Entscheiden, wie der UE-V-Agent bereitgestellt und UE-V-Konfigurationen verwaltet werden sollen](https://technet.microsoft.com/library/dn458891.aspx#config)

    -   [Installieren des UE-V-Agents](https://technet.microsoft.com/library/dn458891.aspx#agent) auf jedem Benutzercomputer, auf dem Einstellungen synchronisiert werden müssen

-   Optional können Sie [UE-V 2.x für benutzerdefinierte Anwendungen bereitstellen.](deploy-ue-v-2x-for-custom-applications-new-uevv2.md)

    Die Planung hilft Ihnen herauszufinden, ob UE-V die Synchronisierung von Einstellungen für benutzerdefinierte Anwendungen (Drittanbieter oder Branchen) unterstützen soll, die die folgenden UE-V Features erfordern:

    -   [Installieren Sie den UEV-Generator,](https://technet.microsoft.com/library/dn458942.aspx#uevgen) damit Sie die benutzerdefinierten Einstellungsspeicherortvorlagen erstellen, bearbeiten und überprüfen können, die zum Synchronisieren benutzerdefinierter Anwendungseinstellungen erforderlich sind.

    -   [Erstellen benutzerdefinierter Einstellungsspeicherortvorlagen](https://technet.microsoft.com/library/dn458942.aspx#createcustomtemplates) mithilfe des UE-V-Generators

    -   [Bereitstellen eines UE-V Einstellungsvorlagenkatalogs,](https://technet.microsoft.com/library/dn458942.aspx#deploycatalogue) mit dem Sie Ihre benutzerdefinierten Speicherortvorlagen für Einstellungen speichern

Dieses Workflowdiagramm bietet ein allgemeines Verständnis für eine UE-V Bereitstellung und die Entscheidungen, die bestimmen, wie Sie UE-V in Ihrem Unternehmen bereitstellen.

![deploymentworkflow.](images/deploymentworkflow.png)

**Planen einer UE-V Bereitstellung:** Zunächst möchten Sie etwas planen, damit Sie bestimmen können, welche UE-V Komponenten Sie bereitstellen werden. Die Planung einer UE-V Bereitstellung umfasst folgende Dinge:

-   [Entscheiden, ob Einstellungen für benutzerdefinierte Anwendungen synchronisiert werden sollen](#deciding)

    Dadurch wird bestimmt, ob Sie den UE-V-Generator während der Bereitstellung installieren, mit dem Sie benutzerdefinierte Einstellungsspeicherortvorlagen erstellen können. Dies umfasst Folgendes:

    Überprüfen Sie die [Einstellungen, die in einer UE-V Bereitstellung automatisch synchronisiert werden.](#autosyncsettings)

    [Bestimmen Sie, ob Einstellungen für andere Anwendungen synchronisiert werden müssen.](#determinesettingssync)

-   Überprüfen Sie [andere Überlegungen für die Bereitstellung von UE-V,](#considerations)z. B. hohe Verfügbarkeit und Kapazitätsplanung.

-   [Bestätigen der Voraussetzungen und unterstützten Konfigurationen für UE-V](#prereqs)

## <a name="decide-whether-to-synchronize-settings-for-custom-applications"></a><a href="" id="deciding"></a>Entscheiden, ob Einstellungen für benutzerdefinierte Anwendungen synchronisiert werden sollen


In einer UE-V Bereitstellung werden viele Einstellungen automatisch synchronisiert. Sie können jedoch auch UE-V anpassen, um Einstellungen für andere Anwendungen wie Branchen- und Drittanbieter-Apps zu synchronisieren.

Die Entscheidung, ob UE-V Einstellungen für benutzerdefinierte Anwendungen synchronisieren möchten, ist wahrscheinlich der wichtigste Teil der Planung Ihrer UE-V Bereitstellung. Die Themen in diesem Abschnitt helfen Ihnen bei der Entscheidung.

### <a name="settings-that-are-automatically-synchronized-in-a-ue-v-deployment"></a><a href="" id="autosyncsettings"></a>Einstellungen, die in einer UE-V Bereitstellung automatisch synchronisiert werden

Dieser Abschnitt enthält Informationen zu den Einstellungen, die standardmäßig in UE-V synchronisiert werden, einschließlich der folgenden:

Desktopanwendungen, deren Einstellungen standardmäßig synchronisiert werden

Windows Desktopeinstellungen, die standardmäßig synchronisiert werden

Unterstützungserklärung für Windows App-Einstellungssynchronisierung

Weitere Informationen zum Herunterladen einer vollständigen Liste der spezifischen Einstellungen Microsoft Office 2013, Microsoft Office 2010 und Microsoft Office 2007, die von UE-V synchronisiert werden, finden Sie unter [UE-V-Einstellungsvorlagen für](https://www.microsoft.com/download/details.aspx?id=46367) Microsoft Office.

### <a name="desktop-applications-synchronized-by-default-in-ue-v-21-and-ue-v-21-sp1"></a>Standardmäßig in UE-V 2.1 und UE-V 2.1 SP1 synchronisierte Desktopanwendungen

Wenn Sie den UE-V 2.1- oder 2.1 SP1-Agent installieren, wird eine Standardgruppe von Einstellungsspeicherortvorlagen registriert, die Einstellungswerte für diese gängigen Microsoft-Anwendungen erfassen.

**Tipp**  
**Microsoft Office 2007 Einstellungen Synchronisierung** : In UE-V 2.1 und 2.1 SP1 ist eine Einstellungsspeicherortvorlage für Office 2007-Anwendungen nicht mehr standardmäßig enthalten. Sie können jedoch weiterhin Office 2007-Vorlagen aus UE-V 2.0 oder früheren Versionen verwenden und die Vorlagen aus dem [UE-V Vorlagenkatalog](https://go.microsoft.com/fwlink/p/?LinkID=246589)abrufen.



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
<p>( <a href="https://www.microsoft.com/download/details.aspx?id=46367" data-raw-source="[Download a list of all settings synced](https://www.microsoft.com/download/details.aspx?id=46367)"> Laden Sie eine Liste aller synchronisierten Einstellungen </a> herunter)</p></td>
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
<p>Microsoft Lync 2010</p>
<p>Microsoft OneNote 2010</p>
<p>Microsoft SharePoint Designer 2010</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft Office 2013-Anwendungen</p>
<p>( <a href="https://www.microsoft.com/download/details.aspx?id=46367" data-raw-source="[Download a list of all settings synced](https://www.microsoft.com/download/details.aspx?id=46367)"> Laden Sie eine Liste aller synchronisierten Einstellungen </a> herunter)</p></td>
<td align="left"><p>Microsoft Word 2013</p>
<p>Microsoft Excel 2013</p>
<p>Microsoft Outlook 2013</p>
<p>Microsoft Access 2013</p>
<p>Microsoft Project 2013</p>
<p>Microsoft PowerPoint 2013</p>
<p>Microsoft Publisher 2013</p>
<p>Microsoft Visio 2013</p>
<p>Microsoft InfoPath 2013</p>
<p>Microsoft Lync 2013</p>
<p>Microsoft OneNote 2013</p>
<p>Microsoft SharePoint Designer 2013</p>
<p>Microsoft Office 2013 Hochladen Center</p>
<p>Microsoft OneDrive for Business 2013</p>
<p>Die Einstellungsvorlagen UE-V 2.1 und 2.1 SP1 Microsoft Office 2013 enthalten verbesserte Outlook Signaturunterstützung. Wir haben die Synchronisierung der Standardsignatureinstellungen für neue, antwortende und weitergeleitete E-Mails hinzugefügt.</p>
<div class="alert">
<strong>Hinweis:</strong><br/><p>Ein Outlook Profil muss für jedes Gerät erstellt werden, auf dem ein Benutzer seine Outlook Signatur synchronisieren möchte. Wenn das Profil noch nicht erstellt wurde, kann der Benutzer ein Profil erstellen und dann Outlook auf diesem Gerät neu starten, um die Signatursynchronisierung zu aktivieren.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p>Browseroptionen: Internet Explorer 8, Internet Explorer 9, Internet Explorer 10 und Internet Explorer 11</p></td>
<td align="left"><p>Favoriten, Startseite, Registerkarten und Symbolleisten.</p>
<div class="alert">
<strong>Hinweis:</strong><br/><p>UE-V führt keine Roamingeinstellungen für Internet Explorer-Cookies durch.</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Zubehör</p></td>
<td align="left"><p>Microsoft Rechner, Editor, WordPad.</p></td>
</tr>
</tbody>
</table>



**Hinweis:**  
UE-V 2.1 SP1 synchronisiert keine Einstellungen zwischen dem Microsoft Rechner in Windows 10 und dem Microsoft Rechner in vorherigen Betriebssystemen.



### <a name="desktop-applications-synchronized-by-default-in-ue-v-20"></a>Standardmäßig in UE-V 2.0 synchronisierte Desktopanwendungen

Wenn Sie den UE-V 2.0-Agent installieren, wird eine Standardgruppe von Einstellungsspeicherortvorlagen registriert, die Einstellungswerte für diese gängigen Microsoft-Anwendungen erfassen.

**Tipp**  
**Microsoft Office 2013 Einstellungen Synchronisierung** – In UE-V 2.0 ist eine Einstellungsspeicherortvorlage für Office 2013-Anwendungen nicht standardmäßig enthalten, steht jedoch im [Vorlagenkatalog UE-V](https://go.microsoft.com/fwlink/p/?LinkID=246589)zum Download zur Verfügung. [Die Synchronisierung von Office 2013 mit UE-V 2.0](synchronizing-office-2013-with-ue-v-20-both-uevv2.md) enthält Details zu den unterstützten Vorlagen, die Office 2013-Einstellungen synchronisieren.



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
<p>( <a href="https://www.microsoft.com/download/details.aspx?id=46367" data-raw-source="[Download a list of all settings synced](https://www.microsoft.com/download/details.aspx?id=46367)"> Laden Sie eine Liste aller synchronisierten Einstellungen </a> herunter)</p></td>
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
<p>( <a href="https://www.microsoft.com/download/details.aspx?id=46367" data-raw-source="[Download a list of all settings synced](https://www.microsoft.com/download/details.aspx?id=46367)"> Laden Sie eine Liste aller synchronisierten Einstellungen </a> herunter)</p></td>
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
<p>Microsoft Lync 2010</p>
<p>Microsoft OneNote 2010</p>
<p>Microsoft SharePoint Designer 2010</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Browseroptionen: Internet Explorer 8, Internet Explorer 9 und Internet Explorer 10</p></td>
<td align="left"><p>Favoriten, Startseite, Registerkarten und Symbolleisten.</p>
<div class="alert">
<strong>Hinweis:</strong><br/><p>UE-V führt keine Roamingeinstellungen für Internet Explorer-Cookies durch.</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Zubehör</p></td>
<td align="left"><p>Microsoft Rechner, Editor, WordPad.</p></td>
</tr>
</tbody>
</table>



### <a name="windows-settings-synchronized-by-default"></a><a href="" id="autosyncsettings2"></a>Windows Standardmäßig synchronisierte Einstellungen

UE-V enthält Einstellungsspeicherortvorlagen, die Einstellungswerte für diese Windows Einstellungen erfassen.

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
<th align="left">Exportieren nach</th>
<th align="left">Standardzustand</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Desktophintergrund</p></td>
<td align="left"><p>Derzeit aktiver Desktophintergrund oder Hintergrund.</p></td>
<td align="left"><p>Anmelden, Entsperren, Remoteverbindung, Geplante Aufgabenereignisse.</p></td>
<td align="left"><p>Abmelden, Sperren, Trennen der Remoteverbindung, Klicken des Benutzers auf <strong> "Jetzt </strong> synchronisieren" im Unternehmen Einstellungen Center oder geplantes Aufgabenintervall</p></td>
<td align="left"><p>Aktiviert</p></td>
</tr>
<tr class="even">
<td align="left"><p>Erleichterte Bedienung</p></td>
<td align="left"><p>Eingabe- und Eingabeeinstellungen, Microsoft-Bildschirmlupe, Sprachausgabe und Bildschirmtastatur.</p></td>
<td align="left"><p>Nur Anmeldung.</p></td>
<td align="left"><p>Abmelden, Benutzer, der im Unternehmen Einstellungen Center auf <strong> "Jetzt synchronisieren" </strong> klickt, oder geplantes Aufgabenintervall</p></td>
<td align="left"><p>Aktiviert</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Desktopeinstellungen</p></td>
<td align="left"><p>Startmenü- und Taskleisteneinstellungen, Ordneroptionen, Standarddesktopsymbole, zusätzliche Uhrzeiten sowie Regions- und Spracheinstellungen.</p></td>
<td align="left"><p>Nur Anmeldung.</p></td>
<td align="left"><p>Abmelden, Benutzer klicken <strong> im Unternehmen Einstellungen Center auf "Jetzt synchronisieren" oder geplante </strong> Aufgabe</p></td>
<td align="left"><p>Aktiviert</p></td>
</tr>
</tbody>
</table>



**Hinweis:**  
Ab Windows 8 werden für UE-V keine Roamingeinstellungen im Zusammenhang mit dem Startbildschirm erstellt, z. B. Elemente und Speicherorte. Darüber hinaus unterstützt UE-V keine Synchronisierung angehefteter Taskleistenelemente oder Windows Dateiverknüpfungen.



**Wichtig**  
UE-V 2.1 SP1 werden taskleisteneinstellungen zwischen Windows 10 Geräten roaming. UE-V synchronisiert jedoch keine Taskleisteneinstellungen zwischen Windows 10 Geräten und Geräten mit vorherigen Betriebssystemen.



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
<th align="left">„Übernehmen“</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Anwendungseinstellungen</strong></p></td>
<td align="left"><p>Windows-Apps  </p></td>
<td align="left"><p>App schließen</p>
<p>Änderungsereignis für Windows App-Einstellungen</p></td>
<td align="left"><p>Starten des UE-V App Monitor beim Start</p>
<p>App öffnen</p>
<p>Windows App-Einstellungen-Änderungsereignis</p>
<p>Einführung eines Einstellungspakets</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p>Desktopanwendungen</p></td>
<td align="left"><p>Anwendung wird geschlossen</p></td>
<td align="left"><p>Anwendung wird geöffnet und geschlossen</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Desktopeinstellungen</strong></p></td>
<td align="left"><p>Desktophintergrund</p></td>
<td align="left"><p>Sperren oder Abmelden</p></td>
<td align="left"><p>Anmeldung, Entsperrung, Remoteverbindung, Benachrichtigung über die Ankunft des neuen Pakets, Benutzer klickt im Unternehmen Einstellungen Center auf <strong> "Jetzt </strong> synchronisieren", oder geplante Aufgaben werden ausgeführt.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p>Erleichterte Bedienung (allgemein – Barrierefreiheit, Sprachausgabe, Bildschirmlupe, Bildschirmtastatur)</p></td>
<td align="left"><p>Sperren oder Abmelden</p></td>
<td align="left"><p>Anmeldung</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p>Erleichterte Bedienung (Shell – Audio, Barrierefreiheit, Tastatur, Maus)</p></td>
<td align="left"><p>Sperren oder Abmelden</p></td>
<td align="left"><p>Anmeldung, Entsperrung, Remoteverbindung, Benachrichtigung über die Ankunft des neuen Pakets, Benutzer klickt im Unternehmen Einstellungen Center auf <strong> "Jetzt synchronisieren" </strong> oder geplante Aufgaben werden ausgeführt</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p>Desktopeinstellungen</p></td>
<td align="left"><p>Sperren oder Abmelden</p></td>
<td align="left"><p>Anmeldung</p></td>
</tr>
</tbody>
</table>



### <a name="ue-v-support-for-windows-apps"></a>UE-V-Unterstützung für Windows Apps

Für Windows Apps gibt der App-Entwickler die Einstellungen an, die synchronisiert werden. Sie können angeben, welche Windows Apps für die Einstellungssynchronisierung aktiviert sind.

Um eine Liste der Windows Apps anzuzeigen, die Einstellungen auf einem Computer mit ihrem Paketfamiliennamen, dem aktivierten Status und der aktivierten Quelle synchronisieren können, geben Sie an einer Windows PowerShell Eingabeaufforderung Folgendes ein: `Get-UevAppxPackage`

**Hinweis:**  
Ab Windows 8 synchronisiert UE-V Windows App-Einstellungen nicht, wenn der Domänenbenutzer seine Anmeldeinformationen mit dem Microsoft-Konto verknüpft. Durch diese Verknüpfung werden Einstellungen mit Microsoft OneDrive synchronisiert, sodass UE-V, wodurch die Synchronisierung von Windows App-Einstellungen deaktiviert wird.



### <a name="ue-v-support-for-roaming-printers"></a>UE-V-Unterstützung für Roamingdrucker

UE-V 2.1 SP1 ermöglicht das Roaming von Netzwerkdruckern zwischen Geräten, sodass ein Benutzer zugriff auf seine Netzwerkdrucker hat, wenn er sich bei einem beliebigen Gerät im Netzwerk angemeldet hat. Dazu gehört das Roaming des Druckers, den sie als Standard festlegen.

Für das Druckerroaming in UE-V ist eines der folgenden Szenarien erforderlich:

-   Der Druckserver kann den erforderlichen Treiber herunterladen, wenn er auf ein neues Gerät übertragen wird.

-   Der Treiber für den Roamingnetzwerkdrucker ist auf allen Geräten vorinstalliert, die auf diesen Netzwerkdrucker zugreifen müssen.

-   Der Druckertreiber kann über Windows Update abgerufen werden.

**Hinweis:**  
Die UE-V Druckerroamingfunktion führt **keine** Roamingdruckereinstellungen oder -einstellungen durch, z. B. doppelseitiges Drucken.



### <a name="determine-whether-you-need-settings-synchronized-for-other-applications"></a><a href="" id="determinesettingssync"></a>Ermitteln, ob Einstellungen für andere Anwendungen synchronisiert werden müssen

Nachdem Sie die Einstellungen überprüft haben, die in einer UE-V Bereitstellung automatisch synchronisiert werden, möchten Sie entscheiden, ob Sie Einstellungen für andere Anwendungen synchronisieren, da dies bestimmt, wie Sie UE-V im gesamten Unternehmen bereitstellen.

Wenn Sie als Administrator überlegen, welche Desktopanwendungen in Ihre UE-V Lösung aufgenommen werden sollen, sollten Sie überlegen, welche Einstellungen von Benutzern angepasst werden können und wie und wo die Anwendung ihre Einstellungen speichert. Nicht alle Desktopanwendungen verfügen über Einstellungen, die angepasst oder von Benutzern routinemäßig angepasst werden können. Darüber hinaus können nicht alle Desktopanwendungen sicher auf mehreren Computern oder Umgebungen synchronisiert werden.

Im Allgemeinen können Sie Einstellungen synchronisieren, die die folgenden Kriterien erfüllen:

-   Einstellungen, die an Speicherorten gespeichert werden, auf die der Benutzer zugriffen kann. Synchronisieren Sie beispielsweise keine Einstellungen, die in System32 oder außerhalb des Hkcu-Abschnitts (HKEY\_CURRENT\_USER) der Registrierung gespeichert sind.

-   Einstellungen, die nicht für den jeweiligen Computer spezifisch sind. Schließen Sie beispielsweise Netzwerk- oder Hardwarekonfigurationen aus.

-   Einstellungen, die zwischen Computern synchronisiert werden können, ohne dass das Risiko beschädigter Daten besteht. Verwenden Sie beispielsweise keine Einstellungen, die in einer Datenbankdatei gespeichert sind.

### <a name="checklist-for-evaluating-custom-applications"></a><a href="" id="checklistsettingssync"></a>Prüfliste für die Auswertung von benutzerdefinierten Anwendungen

Wenn Sie sich entschieden haben, dass Einstellungen für andere Anwendungen synchronisiert werden müssen, können Sie diese Prüfliste verwenden, um herauszufinden, welche Anwendungen Sie einschließen werden.

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
<td align="left"><p>Enthält diese Anwendung Einstellungen, die der Benutzer anpassen kann?</p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Ist es für den Benutzer wichtig, dass diese Einstellungen synchronisiert werden?</p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Werden diese Benutzereinstellungen bereits von einer Anwendungsverwaltungs- oder Einstellungsrichtlinienlösung verwaltet? UE-V wendet Anwendungseinstellungen beim Anwendungsstart und Windows Einstellungen bei Anmelde-, Entsperrungs- oder Remoteverbindungsereignissen an. Wenn Sie UE-V mit anderen Lösungen für die Freigabe von Einstellungen verwenden, kann es bei Benutzern zu Inkonsistenzen zwischen synchronisierten Einstellungen kommt.</p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Sind die Anwendungseinstellungen für den Computer spezifisch? Anwendungseinstellungen und Anpassungen, die Hardware oder bestimmten Computerkonfigurationen zugeordnet sind, werden nicht konsistent sitzungsübergreifend synchronisiert und können zu einer schlechten Anwendungserfahrung führen.</p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Speichert die Anwendung Einstellungen im Verzeichnis "Programmdateien" oder im Dateiverzeichnis, das sich im <strong> </strong> starken &lt; &gt; "AppData </strong> &lt; strong &gt; LocalLow"-Verzeichnis </strong> "Benutzer [Benutzername] befindet? Anwendungsdaten, die an einem dieser Speicherorte gespeichert sind, sollten in der Regel nicht mit dem Benutzer synchronisiert werden, da diese Daten für den Computer spezifisch sind oder weil die Daten zu groß für die Synchronisierung sind.</p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Speichert die Anwendung Einstellungen in einer Datei, die andere Anwendungsdaten enthält, die nicht synchronisiert werden sollen? UE-V synchronisiert Dateien als einzelne Einheit. Wenn Einstellungen in Dateien gespeichert werden, die andere Anwendungsdaten als Einstellungen enthalten, kann die Synchronisierung dieser zusätzlichen Daten zu einer schlechten Anwendungserfahrung führen.</p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Wie groß sind die Dateien, die die Einstellungen enthalten? Die Leistung der Einstellungssynchronisierung kann durch große Dateien beeinflusst werden. Das Einschließen großer Dateien kann sich auf die Leistung der Einstellungssynchronisierung auswirken.</p></td>
</tr>
</tbody>
</table>



## <a name="other-considerations-when-preparing-a-ue-v-deployment"></a><a href="" id="considerations"></a>Weitere Überlegungen bei der Vorbereitung einer UE-V Bereitstellung


Sie sollten auch die folgenden Punkte berücksichtigen, wenn Sie sich auf die Bereitstellung von UE-V vorbereiten:

-   [Verwalten der Synchronisierung von Anmeldeinformationen](#creds)

-   [Synchronisierung von app-Einstellungen Windows](#appxsettings)

-   [Speicherortvorlagen für benutzerdefinierte UE-V-Einstellungen](#custom)

-   [Unbeabsichtigte Konfigurationen von Benutzereinstellungen](#prevent)

-   [Leistung und Kapazität](#capacity)

-   [Hohe Verfügbarkeit](#high)

-   [Synchronisierung der Computeruhr](#clocksync)

### <a name="managing-credentials-synchronization-in-ue-v-21-and-ue-v-21-sp1"></a><a href="" id="creds"></a>Verwalten der Synchronisierung von Anmeldeinformationen in UE-V 2.1 und UE-V 2.1 SP1

Viele Unternehmensanwendungen, einschließlich Microsoft Outlook und Lync, fordern Benutzer bei der Anmeldung zur Eingabe ihrer Domänenanmeldeinformationen auf. Benutzer haben die Möglichkeit, ihre Anmeldeinformationen auf dem Datenträger zu speichern, um zu verhindern, dass sie sie jedes Mal eingeben müssen, wenn sie diese Anwendungen öffnen. Wenn Sie die Synchronisierung von Roaminganmeldeinformationen aktivieren, können Benutzer ihre Anmeldeinformationen auf einem Computer speichern und vermeiden, sie auf jedem Computer erneut einzugeben, den sie in ihrer Umgebung verwenden. Benutzer können einige Domänenanmeldeinformationen mit UE-V 2.1 und 2.1 SP1 synchronisieren.

**Wichtig**  
Die Synchronisierung von Anmeldeinformationen ist standardmäßig deaktiviert. Sie müssen die Synchronisierung von Anmeldeinformationen während der Bereitstellung explizit aktivieren, um dieses Feature zu implementieren.



UE-V 2.1 und 2.1 SP1 können Unternehmensanmeldeinformationen synchronisieren, aber keine Roaminganmeldeinformationen ausführen, die nur für die Verwendung auf dem lokalen Computer vorgesehen sind.

Anmeldeinformationen sind synchrone Einstellungen, d. h. sie werden auf Ihr Profil angewendet, wenn Sie sich zum ersten Mal bei Ihrem Computer anmelden, nachdem UE-V synchronisiert wurde.

Die Synchronisierung von Anmeldeinformationen wird durch eine eigene Einstellungsspeicherortvorlage verwaltet, die standardmäßig deaktiviert ist. Sie können diese Vorlage mit denselben Methoden aktivieren oder deaktivieren, die auch für andere Vorlagen verwendet werden. Der Vorlagenbezeichner für dieses Feature ist RoamingCredentialSettings.

**Wichtig**  
Wenn Sie Active Directory Credential Roaming in Ihrer Umgebung verwenden, wird empfohlen, die UE-V-Anmeldeinformations-Roamingvorlage nicht zu aktivieren.



Verwenden Sie eine der folgenden Methoden, um die Synchronisierung von Anmeldeinformationen zu aktivieren:

-   Company Einstellungen Center

-   PowerShell

-   Gruppenrichtlinie

**Hinweis:**  
Anmeldeinformationen werden während der Synchronisierung verschlüsselt.



[Unternehmenscenter Einstellungen:](https://technet.microsoft.com/library/dn458903.aspx)**** Aktivieren Sie das Kontrollkästchen "Roaminganmeldeinformationen Einstellungen" unter Windows Einstellungen, um die Synchronisierung von Anmeldeinformationen zu aktivieren. Deaktivieren Sie das Kontrollkästchen, um es zu deaktivieren. Dieses Kontrollkästchen wird im Unternehmen Einstellungen Center nur angezeigt, wenn Ihr Konto nicht für die Synchronisierung von Einstellungen mithilfe eines Microsoft-Kontos konfiguriert ist.

[PowerShell:](https://technet.microsoft.com/library/dn458937.aspx)**** Dieses PowerShell-Cmdlet ermöglicht die Synchronisierung von Anmeldeinformationen:

``` syntax
Enable-UevTemplate RoamingCredentialSettings
```

Mit diesem PowerShell-Cmdlet wird die Synchronisierung von Anmeldeinformationen deaktiviert:

``` syntax
Disable-UevTemplate RoamingCredentialSettings
```

[Gruppenrichtlinie:](https://technet.microsoft.com/library/dn458893.aspx)**** Sie müssen [die neueste MDOP ADMX-Vorlage bereitstellen,](https://go.microsoft.com/fwlink/p/?LinkId=393944) um die Synchronisierung von Anmeldeinformationen über gruppenrichtlinien zu aktivieren. Die Synchronisierung von Anmeldeinformationen wird mit den Windows-Einstellungen verwaltet. Um dieses Feature mithilfe von Gruppenrichtlinien zu verwalten, aktivieren Sie die Richtlinie zum Synchronisieren Windows Einstellungen.

1.  Öffnen Sie den Gruppenrichtlinien-Editor, und navigieren Sie zu **Benutzerkonfiguration – Administrative Vorlagen – Windows Komponenten – Microsoft User Experience Virtualization.**

2.  Doppelklicken Sie auf **"Windows Einstellungen synchronisieren".**

3.  Wenn diese Richtlinie aktiviert ist, können Sie die Synchronisierung von Anmeldeinformationen aktivieren, indem Sie das Kontrollkästchen **"Roaminganmeldeinformationen"** aktivieren oder die Synchronisierung von Anmeldeinformationen deaktivieren, indem Sie sie deaktivieren.

4.  Klicken Sie auf **OK**.

### <a name="credential-locations-synchronized-by-ue-v"></a>Von UE-V synchronisierte Anmeldeinformationsspeicherorte

Anmeldeinformationsdateien, die von Anwendungen an den folgenden Speicherorten gespeichert werden, werden synchronisiert:

-   %UserProfile%\\AppData\\Roaming\\Microsoft\\Credentials\\

-   %UserProfile%\\AppData\\Roaming\\Microsoft\\Crypto\\

-   %UserProfile%\\AppData\\Roaming\\Microsoft\\Protect\\

-   %UserProfile%\\AppData\\Roaming\\Microsoft\\SystemCertificates\\

An anderen Speicherorten gespeicherte Anmeldeinformationen werden nicht von UE-V synchronisiert.

### <a name="windows-app-settings-synchronization"></a><a href="" id="appxsettings"></a>Synchronisierung von Windows-App-Einstellungen

UE-V verwaltet Windows App-Einstellungssynchronisierung auf drei Arten:

-   **Synchronisieren Windows Apps:** Zulassen oder Verweigern Windows App-Synchronisierung

-   **Windows App-Liste:** Synchronisieren einer Liste von Windows Apps

-   **Nicht aufgelistetes Standardsynchronisierungsverhalten:** Bestimmen Sie das Synchronisierungsverhalten von Windows Apps, die nicht in der Windows App-Liste enthalten sind.

Weitere Informationen finden Sie in der [Windows App-Liste.](https://technet.microsoft.com/library/dn458925.aspx#win8applist)

### <a name="custom-ue-v-settings-location-templates"></a><a href="" id="custom"></a>Speicherortvorlagen für benutzerdefinierte UE-V-Einstellungen

Wenn Sie UE-V bereitstellen, um Einstellungen für benutzerdefinierte Anwendungen zu synchronisieren, verwenden Sie den UE-V-Generator, um benutzerdefinierte Einstellungsspeicherortvorlagen für diese Desktopanwendungen zu erstellen. Nachdem Sie eine benutzerdefinierte Einstellungsspeicherortvorlage in einer Testumgebung erstellt und getestet haben, können Sie die Einstellungsspeicherortvorlagen auf Computern im Unternehmen bereitstellen.

Benutzerdefinierte Einstellungsspeicherortvorlagen müssen mit einer vorhandenen Bereitstellungsinfrastruktur bereitgestellt werden, z. B. einer ESD-Methode (Enterprise Software Distribution), z. B. System Center Configuration Manager, mit Voreinstellungen oder durch Konfigurieren eines UE-V Einstellungsvorlagenkatalogs. Vorlagen, die mit Configuration Manager oder Gruppenrichtlinien bereitgestellt werden, müssen mit UE-V WMI oder Windows PowerShell registriert werden.

Weitere Informationen zu Speicherortvorlagen für benutzerdefinierte Einstellungen finden Sie unter [Deploy UE-V 2.x for Custom Applications](deploy-ue-v-2x-for-custom-applications-new-uevv2.md). Weitere Informationen zur Verwendung von UE-V mit Configuration Manager finden Sie unter [Konfigurieren von UE-V 2.x mit System Center Configuration Manager 2012.](configuring-ue-v-2x-with-system-center-configuration-manager-2012-both-uevv2.md)

### <a name="prevent-unintentional-user-settings-configuration"></a><a href="" id="prevent"></a>Verhindern der unbeabsichtigten Konfiguration von Benutzereinstellungen

UE-V lädt informationen zu neuen Benutzereinstellungen von einem Speicherort für Einstellungen herunter und wendet die Einstellungen in diesen Fällen auf den lokalen Computer an:

-   Jedes Mal, wenn eine Anwendung gestartet wird, die über eine registrierte UE-V Vorlage verfügt.

-   Wenn sich ein Benutzer bei einem Computer anmeldet.

-   Wenn ein Benutzer einen Computer entsperrt.

-   Wenn eine Verbindung mit einem Remotedesktopcomputer hergestellt wird, auf dem UE-V installiert ist.

-   Wenn die geplante Aufgabe der Synchronisierungscontrolleranwendung ausgeführt wird.

Wenn UE-V auf Computer A und Computer B installiert ist und sich die gewünschten Einstellungen für die Anwendung auf Computer A befinden, sollte Computer A die Anwendung zuerst öffnen und schließen. Wenn die Anwendung zuerst auf Computer B geöffnet und geschlossen wird, werden die Anwendungseinstellungen auf Computer A mit den Anwendungseinstellungen auf Computer B konfiguriert. Einstellungen zwischen Computern pro Anwendung synchronisiert werden. Im Laufe der Zeit werden die Einstellungen zwischen Computern konsistent, wenn sie mit bevorzugten Einstellungen geöffnet und geschlossen werden.

Dieses Szenario gilt auch für Windows Einstellungen. Wenn die Windows Einstellungen auf Computer B mit den Windows Einstellungen auf Computer A übereinstimmen sollen, sollte sich der Benutzer zuerst bei Computer A anmelden und abmelden.

Wenn die vom Benutzer gewünschten Benutzereinstellungen in der falschen Reihenfolge angewendet werden, können sie wiederhergestellt werden, indem sie einen Wiederherstellungsvorgang für die bestimmte Anwendung oder Windows Konfiguration auf dem Computer ausführen, auf dem die Einstellungen überschrieben wurden. Weitere Informationen finden Sie unter [Verwalten der administrativen Sicherung und Wiederherstellung in UE-V 2.x](manage-administrative-backup-and-restore-in-ue-v-2x-new-topic-for-21.md).

### <a name="performance-and-capacity-planning"></a><a href="" id="capacity"></a>Leistungs- und Kapazitätsplanung

Geben Sie Ihre Anforderungen für UE-V mit standardmäßiger Datenträgerkapazität und Netzwerkintegritätsüberwachung an.

UE-V verwendet eine Server Message Block (SMB)-Freigabe für die Speicherung von Einstellungspaketen. Die Größe von Einstellungspaketen hängt von den Einstellungsinformationen für jede Anwendung ab. Obwohl die meisten Einstellungspakete klein sind, kann die Synchronisierung von potenziell großen Dateien, z. B. Desktopimages, zu einer schlechten Leistung führen, insbesondere in langsameren Netzwerken.

Um Probleme mit der Netzwerklatenz zu verringern, erstellen Sie Speicherorte für Einstellungen in denselben lokalen Netzwerken, in denen sich die Computer der Benutzer befinden. Wir empfehlen 20 MB Speicherplatz pro Benutzer für den Speicherort der Einstellungen.

Standardmäßig führt UE-V Synchronisierung nach 2 Sekunden zu einem Timeout, um übermäßige Verzögerungen aufgrund eines umfangreichen Einstellungspakets zu vermeiden. Sie können die Einstellung SyncMethod=SyncProvider mithilfe von [Gruppenrichtlinienobjekten](https://technet.microsoft.com/library/dn458893.aspx)konfigurieren.

### <a name="high-availability-for-ue-v"></a><a href="" id="high"></a>Hohe Verfügbarkeit für UE-V

Der UE-V Speicherort der Einstellungen und des Vorlagenkatalogs für Einstellungen unterstützt das Speichern von Benutzerdaten auf einer beliebigen beschreibbaren Freigabe. Um hohe Verfügbarkeit sicherzustellen, befolgen Sie die folgenden Kriterien:

-   Formatieren Sie das Speichervolume mit einem NTFS-Dateisystem.

-   Die Freigabe kann dfs (Distributed File System) verwenden, es gibt jedoch Einschränkungen.
Insbesondere wird die DfS-R-Konfiguration (Distributed File System Replication) mit oder ohne dfs-N (Distributed File System Namespace) unterstützt.
Ebenso wird nur die Konfiguration eines einzelnen Ziels mit DFS-N unterstützt.
Ausführliche Informationen finden Sie in [der Microsoft-Supportanweisung zu replizierten Benutzerprofildaten](https://go.microsoft.com/fwlink/p/?LinkId=313991) und informationen [zur Microsoft-Supportrichtlinie für ein DFS-R- und DFS-N-Bereitstellungsszenario.](https://support.microsoft.com/kb/2533009)

    Da SYSVOL außerdem DFS-R für die Replikation verwendet, kann SYSVOL nicht für UE-V Datendateireplikation verwendet werden.

-   Konfigurieren Sie die Freigabeberechtigungen und NTFS-Zugriffssteuerungslisten (ACCESS Control Lists, ACLs) gemäß der Angabe unter [Deploying the Einstellungen Storage Location for UE-V 2.x](https://technet.microsoft.com/library/dn458891.aspx#ssl).

-   Verwenden Sie das Dateiserverclustering zusammen mit dem UE-V-Agent, um im Falle von Kommunikationsfehlern Zugriff auf Kopien von Benutzerstatusdaten bereitzustellen.

-   Sie können die Einstellungsspeicherpfaddaten (Benutzerdaten) und Katalogvorlagen für Einstellungsvorlagen in gruppierten Freigaben, in DFS-N-Freigaben oder in beiden speichern.

### <a name="synchronize-computer-clocks-for-ue-v-settings-synchronization"></a><a href="" id="clocksync"></a>Synchronisieren von Computeruhren für die UE-V-Einstellungssynchronisierung

Computer, auf denen der UE-V-Agent ausgeführt wird, müssen einen Zeitserver verwenden, um eine konsistente Einstellungserfahrung zu gewährleisten. UE-V ermittelt mithilfe von Zeitstempeln, ob Einstellungen vom Speicherort der Einstellungen synchronisiert werden müssen. Wenn die Computeruhr ungenau ist, können ältere Einstellungen neuere Einstellungen überschreiben, oder die neuen Einstellungen werden möglicherweise nicht am Speicherort der Einstellungen gespeichert.

## <a name="confirm-prerequisites-and-supported-configurations-for-ue-v"></a><a href="" id="prereqs"></a>Bestätigen der voraussetzungen und unterstützten Konfigurationen für UE-V


Bevor Sie fortfahren, stellen Sie sicher, dass Ihre Umgebung diese Anforderungen für die Ausführung von UE-V enthält.

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
<th align="left"><strong>Systemarchitektur</strong></th>
<th align="left"><strong>Windows PowerShell</strong></th>
<th align="left"><strong>Microsoft .NET Framework</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows 7</p></td>
<td align="left"><p>Ultimate, Enterprise oder Professional Edition</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>32 Bit oder 64 Bit</p></td>
<td align="left"><p>Windows PowerShell 3.0 oder höher</p></td>
<td align="left"><p>.NET Framework 4.5 oder höher für UE-V 2.1.</p>
<p>.NET Framework 4 oder höher für UE-V 2.0.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2008 R2</p></td>
<td align="left"><p>Standard, Enterprise, Datacenter oder Webserver</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>64 Bit</p></td>
<td align="left"><p>Windows PowerShell 3.0 oder höher</p></td>
<td align="left"><p>.NET Framework 4.5 oder höher für UE-V 2.1.</p>
<p>.NET Framework 4 oder höher für UE-V 2.0.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows 8 und Windows 8.1</p></td>
<td align="left"><p>Enterprise oder Pro</p></td>
<td align="left"><p>Keiner</p></td>
<td align="left"><p>32 Bit oder 64 Bit</p></td>
<td align="left"><p>Windows PowerShell 3.0 oder höher</p></td>
<td align="left"><p>.NET Framework 4.5 oder höher</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows 10, Version vor 1607</p>
<div class="alert">
<strong>Hinweis:</strong><br/><p>Nur UE-V 2.1 SP1 unterstützt Windows 10 Version vor 1607.</p>
</div>
<div>

</div></td>
<td align="left"><p>Enterprise oder Pro</p></td>
<td align="left"><p>Keiner</p></td>
<td align="left"><p>32 Bit oder 64 Bit</p></td>
<td align="left"><p>Windows PowerShell 3.0 oder höher</p></td>
<td align="left"><p>.NET Framework 4.6</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server 2012 und Windows Server 2012 R2</p></td>
<td align="left"><p>Standard oder Datacenter</p></td>
<td align="left"><p>Keiner</p></td>
<td align="left"><p>64 Bit</p></td>
<td align="left"><p>Windows PowerShell 3.0 oder höher</p></td>
<td align="left"><p>.NET Framework 4.5 oder höher</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2016</p></td>
<td align="left"><p>Standard oder Datacenter</p></td>
<td align="left"><p>Keiner</p></td>
<td align="left"><p>64 Bit</p></td>
<td align="left"><p>Windows PowerShell 3.0 oder höher</p></td>
<td align="left"><p>.NET Framework 4.6 oder höher</p></td>
</tr>
</tbody>
</table>



Auch...

-   **MDOP-Lizenz:** Diese Technologie ist Teil des Microsoft Desktop Optimization Pack (MDOP). Enterprise Kunden mdop mit Microsoft Software Assurance erhalten können. Weitere Informationen zu Microsoft Software Assurance und zum Erwerb von MDOP finden Sie unter How Do I Get MDOP ( https://go.microsoft.com/fwlink/p/?LinkId=322049) .

-   **Administrative Anmeldeinformationen** für jeden Computer, auf dem Sie installieren werden

**Hinweis:**  

-   Ab WIndows 10, Version 1607, ist UE-V in [Windows 10 für Enterprise](https://www.microsoft.com/WindowsForBusiness/windows-for-enterprise) enthalten und nicht mehr Teil des Microsoft Desktop Optimization Packs.

-   Für die UE-V Windows PowerShell-Funktion des UE-V-Agents müssen .NET Framework 4 oder höher und Windows PowerShell 3.0 oder höher aktiviert sein. Laden Sie [hier](https://go.microsoft.com/fwlink/?LinkId=309609)Windows PowerShell 3.0 herunter.

-   Installieren Sie .NET Framework 4 oder .NET Framework 4.5 auf Computern, auf denen das Betriebssystem Windows 7 oder Windows Server 2008 R2 ausgeführt wird. Die Betriebssysteme Windows 8, Windows 8.1 und Windows Server 2012 sind mit .NET Framework 4.5 installiert. Das Windows 10 Betriebssystem ist mit .NET Framework 4.6 installiert.
-   Die Richtlinie "Roamingcache löschen" für obligatorische Profile wird mit UE-V nicht unterstützt und sollte nicht verwendet werden.



Es gibt keine speziellen Ram-Anforderungen (Random Access Memory), die für UE-V spezifisch sind.

### <a name="synchronization-of-settings-through-the-sync-provider"></a>Synchronisierung von Einstellungen über den Synchronisierungsanbieter

Der Synchronisierungsanbieter ist die Standardeinstellung für Benutzer, die einen lokalen Cache mit dem Speicherort der Einstellungen in diesen Instanzen synchronisiert:

-   Anmeldung/Abmeldung

-   Sperren/Entsperren

-   Remotedesktopverbindung/-verbindung trennen

-   Öffnen/Schließen der Anwendung

Eine geplante Aufgabe verwaltet diese Synchronisierung von Einstellungen alle 30 Minuten oder über bestimmte Triggerereignisse für bestimmte Anwendungen. Weitere Informationen finden Sie unter [Changing the Frequency of UE-V 2.x Scheduled Tasks](changing-the-frequency-of-ue-v-2x-scheduled-tasks-both-uevv2.md).

Der UE-V-Agent synchronisiert Benutzereinstellungen für Computer, die nicht immer mit dem Unternehmensnetzwerk verbunden sind (Remotecomputer und Laptops) und Computer, die immer mit dem Netzwerk verbunden sind (Computer, die Windows Server- und Host-VDI-Sitzungen (Virtual Desktop Interface) ausführen).

**Synchronisierung für Computer mit immer verfügbaren Verbindungen:** Wenn Sie UE-V auf Computern verwenden, die immer mit dem Netzwerk verbunden sind, müssen Sie den UE-V-Agent so konfigurieren, dass Einstellungen mithilfe des Parameters *SyncMethod=None* synchronisiert werden, der den Einstellungsspeicherserver als Standardnetzwerkfreigabe behandelt. In dieser Konfiguration kann der UE-V-Agent so konfiguriert werden, dass er benachrichtigt wird, wenn der Import der Anwendungseinstellungen verzögert wird.

Aktivieren Sie diese Konfiguration über eine der folgenden Methoden:

-   Legen Sie während UE-V Installation an der Eingabeaufforderung oder in einer Batchdatei den parameter AgentSetup.exe *SyncMethod = None*fest. [Die Bereitstellung des UE-V 2.x-Agents](https://technet.microsoft.com/library/dn458891.aspx#agent) bietet weitere Informationen.

-   Verwenden Sie nach der UE-V Installation das Einstellungen-Verwaltungsfeature in System Center 2012 Configuration Manager oder die MDOP ADMX-Vorlagen, um *syncMethod = Keine* Konfiguration per Push zu übertragen.

-   Verwenden Sie Windows PowerShell oder Windows-Verwaltungsinstrumentation (Management Instrumentation, WMI), um die *Konfiguration SyncMethod = None* festzulegen.

    **Hinweis:**  
    Diese beiden letzten Methoden funktionieren nicht für VDI-Umgebungen (Pooled Virtual Desktop Infrastructure).



Sie müssen den Computer neu starten, bevor die Einstellungen synchronisiert werden.

**Hinweis:**  
Wenn Sie *SyncMethod = None*festlegen, werden alle Einstellungsänderungen direkt auf dem Server gespeichert. Wenn die Netzwerkverbindung mit dem Einstellungsspeicherpfad nicht gefunden wird, werden die Einstellungsänderungen auf dem Gerät zwischengespeichert und bei der nächsten Ausführung des Synchronisierungsanbieters synchronisiert. Wenn der Einstellungsspeicherpfad nicht gefunden wird und das Benutzerprofil bei der Abmeldung aus einer VDI-Poolumgebung entfernt wird, gehen die Einstellungsänderungen verloren, und der Benutzer muss die Änderung erneut anwenden, wenn der Computer wieder mit dem Einstellungsspeicherpfad verbunden wird.



**Synchronisierung für externe Synchronisierungsmodule:** Der Parameter *SyncMethod=External* gibt an, dass, wenn UE-V Einstellungen in einen lokalen Ordner auf dem Benutzercomputer geschrieben werden, jedes externe Synchronisierungsmodul (z. B. OneDrive for Business, Arbeitsordner, Sharepoint oder Dropbox) verwendet werden kann, um diese Einstellungen auf die verschiedenen Computer anzuwenden, auf die Benutzer zugreifen.

**Unterstützung für freigegebene VDI-Sitzungen:** UE-V 2.1 und 2.1 SP1 bieten Unterstützung für VDI-Sitzungen, die von Endbenutzern gemeinsam genutzt werden. Sie können eine spezielle VDI-Vorlage registrieren und konfigurieren, wodurch sichergestellt wird, dass UE-V alle Funktionen für nicht persistente VDI-Sitzungen erhalten.

**Hinweis:**  
Wenn Sie den VDI-Modus für nicht persistente VDI-Sitzungen nicht aktivieren, funktionieren bestimmte Features nicht, [z. B. Sicherung/Wiederherstellung und letztes bekanntes Gut (LKG).](https://technet.microsoft.com/library/dn878331.aspx)



Die VDI-Vorlage wird mit UE-V 2.1 und 2.1 SP1 bereitgestellt und ist in der Regel nach der Installation hier verfügbar: C:\\Program Files\\Microsoft User Experience Virtualization\\Templates\\VdiState.xml

### <a name="prerequisites-for-ue-v-generator-support"></a>Voraussetzungen für UE-V Generator-Unterstützung

Installieren Sie den UE-V-Generator auf dem Computer, der zum Erstellen benutzerdefinierter Einstellungsspeicherortvorlagen verwendet wird. Dieser Computer sollte in der Lage sein, die Anwendungen auszuführen, deren Einstellungen synchronisiert werden. Sie müssen Mitglied der Gruppe "Administratoren" auf dem Computer sein, auf dem die UE-V-Generator-Software ausgeführt wird.

Der UE-V-Generator muss auf einem Computer installiert sein, der ein NTFS-Dateisystem verwendet. Die UE-V-Generator-Software erfordert .NET Framework 4. Weitere Informationen finden Sie unter [Deploy UE-V 2.x for Custom Applications](deploy-ue-v-2x-for-custom-applications-new-uevv2.md).

## <a name="other-resources-for-this-product"></a>Weitere Ressourcen für dieses Produkt


-   [Microsoft User Experience Virtualization (UE-V) 2,x](index.md)

-   [Erste Schritte mit UE-V 2.x](get-started-with-ue-v-2x-new-uevv2.md)

-   [Verwalten von UE-V 2.x](administering-ue-v-2x-new-uevv2.md)

-   [Problembehandlung UE-V 2.x](troubleshooting-ue-v-2x-both-uevv2.md)

-   [Technische Referenz für UE-V 2.x](technical-reference-for-ue-v-2x-both-uevv2.md)














