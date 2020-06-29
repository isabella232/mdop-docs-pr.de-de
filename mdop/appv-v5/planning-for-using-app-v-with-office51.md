---
title: Planen der Verwendung von App-V mit Office
description: Planen der Verwendung von App-V mit Office
author: dansimp
ms.assetid: e7a19b43-1746-469f-bad6-8e75cf4b3f67
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 03/16/2017
ms.openlocfilehash: ae225db3c47faca5fba790fb9963bfd4dc2c66b0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804958"
---
# Planen der Verwendung von App-V mit Office


Verwenden Sie die folgenden Informationen, um zu planen, wie Office mithilfe von Microsoft Application Virtualization (App-V) 5,1 bereitgestellt wird. Dieser Artikel enthält:

-   [App-V-Unterstützung für Sprachpakete](#bkmk-lang-pack)

-   [Unterstützte Versionen von Microsoft Office](#bkmk-office-vers-supp-appv)

-   [Planen der Verwendung von App-V mit vorhandenen Office-Versionen](#bkmk-plan-coexisting)

-   [Integration von Office in Windows bei der Bereitstellung von use App-V für die Bereitstellung von Office](#bkmk-office-integration-win)

## <a href="" id="bkmk-lang-pack"></a>App-V-Unterstützung für Sprachpakete


Sie können den App-V 5,1-Sequenzer verwenden, um Plug-in-Pakete für Sprachpakete, Sprachschnittstellen Pakete, Korrekturhilfen und QuickInfo-Sprachen zu erstellen. Sie können dann zusammen mit dem Office 2013-Paket, das Sie mit dem Office Deployment Toolkit erstellen, die Plug-in-Pakete in eine Verbindungsgruppe einbeziehen. Die Office-Anwendungen und die Plug-in-Sprachpakete interagieren nahtlos in derselben Verbindungsgruppe, genau wie alle anderen Pakete, die in einer Verbindungsgruppe gruppiert sind.

>**Hinweis**  Microsoft Visio und Microsoft Project bieten keine Unterstützung für das Thai-Sprachpaket.

 

## <a href="" id="bkmk-office-vers-supp-appv"></a>Unterstützte Versionen von Microsoft Office

Eine Liste der unterstützten Office-Produkte finden Sie unter [Microsoft Office-Produkt-IDs, die App-V unterstützt](https://support.microsoft.com/help/2842297/product-ids-that-are-supported-by-the-office-deployment-tool-for-click) .
>**Note** &nbsp; Hinweis &nbsp; Sie müssen das Office-Bereitstellungs Tool verwenden, um App-V-Pakete für Microsoft 365-Apps für Unternehmen zu erstellen. Das Erstellen von Paketen für die Volumen lizenzierten Versionen von Office Professional Plus oder Office Standard wird nicht unterstützt. Sie können den App-V-Sequenzer nicht verwenden.

 

## <a href="" id="bkmk-plan-coexisting"></a>Planen der Verwendung von App-V mit vorhandenen Office-Versionen


Sie können mehr als eine Version von Microsoft Office nebeneinander auf demselben Computer installieren, indem Sie "Microsoft Office-Koexistenz" verwenden. Mithilfe der Windows Installer-basierten (MSI)-Version von Office, Klick-und-Los und App-V 5,1 können Sie die Office-Koexistenz mit Kombinationen aus allen Hauptversionen von Office und den Installationsmethoden implementieren. Die Verwendung der Office-Koexistenz wird von Microsoft jedoch nicht empfohlen.

Microsoft empfiehlt bewährte Methoden, die Zusammenarbeit von Office komplett zu vermeiden, um Kompatibilitätsprobleme zu vermeiden. Wenn Sie jedoch zu einer neueren Version von Office migrieren, treten gelegentlich Probleme auf, die nicht sofort behoben werden können, sodass Sie die Koexistenz vorübergehend implementieren können, um eine schnellere Migration zur neuesten Produktversion zu ermöglichen. Die Verwendung von Office-Koexistenz auf lange Sicht wird nie empfohlen, und Ihre Organisation sollte in nächster Zukunft einen Plan für den vollständigen Übergang haben.

### Bevor Sie die Office-Koexistenz implementieren

Bevor Sie die Office-Koexistenz implementieren, lesen Sie die folgende Office-Dokumentation. Wählen Sie den Artikel aus, der der neuesten Version von Office entspricht, für die Sie die Koexistenz durchführen möchten.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Office-Version</th>
<th align="left">Link zur Anleitung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Office 2013</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2784668" data-raw-source="[Information about how to use Office 2013 suites and programs (MSI deployment) on a computer that is running another version of Office](https://support.microsoft.com/kb/2784668)">Informationen zur Verwendung von Office 2013-Suites und-Programmen (MSI-Bereitstellung) auf einem Computer, auf dem eine andere Version von Office ausgeführt wird</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Office 2010</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2121447" data-raw-source="[Information about how to use Office 2010 suites and programs on a computer that is running another version of Office](https://support.microsoft.com/kb/2121447)">Informationen zum Verwenden von Office 2010-Suites und-Programmen auf einem Computer, auf dem eine andere Office-Version ausgeführt wird</a></p></td>
</tr>
</tbody>
</table>

 

Die Office-Dokumentation bietet umfassende Anleitungen zur Koexistenz für Windows Installer-basierte (MSI)-und Klick-und-Los-Installationen von Office. Dieses app-v-Thema zur Koexistenz ergänzt die Office-Anleitung mit Informationen, die für App-v-Bereitstellungen spezifisch sind.

### Unterstützte Szenarien für die Koexistenz von Office

In den folgenden Tabellen werden die unterstützten Koexistenz-Szenarien zusammengefasst. Sie werden gemäß der Version und der Bereitstellungsmethode organisiert, mit der Sie beginnen, und der Version und Bereitstellungsmethode, zu der Sie migrieren. Testen Sie alle Koexistenz-Lösungen unbedingt, bevor Sie Sie für eine Produktionsgruppe bereitstellen.

>**Hinweis**  Microsoft unterstützt nicht die Verwendung mehrerer Office-Versionen in Windows Server-Umgebungen, in denen der Rollendienst "Remote Desktop-Sitzungs Host" aktiviert ist. Zum Ausführen von Szenarien für die Koexistenz von Office müssen Sie diesen Rollendienst deaktivieren.

 

### Windows-Integrationen & Office-Koexistenz

Die Windows Installer-basierten und Klick-und-Los-Installationsmethoden werden in bestimmte Punkte des zugrunde liegenden Windows-Betriebssystems integriert. Wenn Sie die Koexistenz verwenden, können allgemeine Betriebssystem Integrationen zwischen zwei Office-Versionen zu Konflikten führen, wodurch Kompatibilitäts-und Benutzer Probleme auftreten. Mit App-V können Sie bestimmte Office-Versionen abgleichen, um Integrationen auszuschließen, wodurch Sie aus dem Betriebssystem "isoliert" werden.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left">Modus, in dem App-V diese Version von Office Sequenzieren kann</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Office 2007</p></td>
<td align="left"><p>Immer nicht integriert. App-V bietet keine Betriebssystem Integrationen mit einer virtualisierten Version von Office 2007.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Office 2010</p></td>
<td align="left"><p>Integrierter und nicht integrierter Modus.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Office 2013</p></td>
<td align="left"><p>Immer integriert. Windows-Betriebssystem Integrationen können nicht deaktiviert werden.</p></td>
</tr>
</tbody>
</table>

 

Microsoft empfiehlt, dass Sie die Office-Koexistenz mit nur einer integrierten Office-Instanz bereitstellen. Wenn Sie beispielsweise App-V zum Bereitstellen von Office 2010 und Office 2013 verwenden, sollten Sie Office 2010 im nicht integrierten Modus sequenzieren. Weitere Informationen zur Sequenzierung von Office im nicht Integrationsmodus (isoliert) finden Sie unter [so wird es gemacht: Sequenzierung von Microsoft Office 2010 in Microsoft Application Virtualization 5,0](https://support.microsoft.com/kb/2830069).

### Bekannte Einschränkungen von Szenarien für die Koexistenz von Office

In den folgenden Abschnitten werden einige Probleme beschrieben, die bei der Verwendung von App-V zur Implementierung der Koexistenz mit Office auftreten können.

### Einschränkungen, die für Windows Installer-basierte/Klick-und-Los-und App-V-Koexistenz-Szenarien üblich sind

Die folgenden Einschränkungen können auftreten, wenn Sie die folgenden Office-Versionen auf demselben Computer installieren:

-   Office 2010 mit Windows Installer-basierter Version

-   Office 2013 mithilfe von App-V

Nachdem Sie Office 2013 mithilfe von App-V nebeneinander mit einer früheren Version des Windows Installer-basierten Office 2010 veröffentlicht haben, kann dies auch dazu führen, dass Windows Installer gestartet wird. Dies liegt daran, dass die Windows Installer-basierte oder Klick-und-Los-Version von Office 2010 versucht, sich automatisch auf dem Computer zu registrieren.

Führen Sie die folgenden Schritte aus, um den automatischen Registrierungsvorgang für systemeigene Word 2010 zu umgehen:

1.  Beenden Sie Word 2010.

2.  Starten Sie den Registrierungs-Editor, indem Sie wie folgt vorgehen:

    -   Unter Windows 7: Klicken Sie auf **Start**, geben Sie im Feld Suche starten den **Befehl regedit** ein, und drücken Sie dann die EINGABETASTE.

    -   Geben Sie in Windows 8,1 oder Windows 10 **Regedit** ein, drücken Sie die Eingabetaste auf der Start Seite, und drücken Sie dann die EINGABETASTE.

    Wenn Sie zur Eingabe eines Administratorkennworts oder zur Bestätigung aufgefordert werden, geben Sie das Kennwort ein, oder klicken Sie auf **weiter**.

3.  Suchen Sie den folgenden Registrierungsunterschlüssel, und wählen Sie ihn aus:

    ``` syntax
    HKEY_CURRENT_USER\Software\Microsoft\Office\14.0\Word\Options
    ```

4.  Klicken Sie im Menü **Bearbeiten** auf **neu**, und klicken Sie dann auf **DWORD-Wert**.

5.  Geben Sie **NoReReg**ein, und drücken Sie dann die EINGABETASTE.

6.  Klicken Sie mit der rechten Maustaste auf **NoReReg** , und klicken Sie dann auf **ändern**.

7.  Geben Sie im Feld **Valuedata** **1 ein**, und klicken Sie dann auf **OK**.

8.  Klicken Sie im Menü Datei auf **Beenden** , um den Registrierungs-Editor zu schließen.

## <a href="" id="bkmk-office-integration-win"></a>Integration von Office in Windows bei Verwendung von App-V zum Bereitstellen von Office


Wenn Sie Office 2013 mithilfe von App-v bereitstellen, ist Office vollständig in das Betriebssystem integriert, das Endbenutzern dieselben Features und Funktionen wie Office bietet, wenn es ohne APP-v bereitgestellt wird.

Das Office 2013-App-V-Paket unterstützt die folgenden Integrationspunkte mit dem Windows-Betriebssystem:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Erweiterungspunkt</th>
<th align="left">Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Lync-Besprechungsteilnahme-Plug-in für Firefox und Chrome</p></td>
<td align="left"><p>Benutzer können über Firefox und Chrome an lync-Besprechungen teilnehmen</p></td>
</tr>
<tr class="even">
<td align="left"><p>An den OneNote-Druckertreiber gesendet</p></td>
<td align="left"><p>Benutzer kann in OneNote drucken</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Verknüpfte OneNote-Notizen</p></td>
<td align="left"><p>Verknüpfte OneNote-Notizen</p></td>
</tr>
<tr class="even">
<td align="left"><p>An OneNote Internet Explorer-Add-in senden</p></td>
<td align="left"><p>Benutzer kann von IE an OneNote senden</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Firewall-Ausnahme für lync und Outlook</p></td>
<td align="left"><p>Firewall-Ausnahme für lync und Outlook</p></td>
</tr>
<tr class="even">
<td align="left"><p>MAPI-Client</p></td>
<td align="left"><p>Systemeigene apps und Add-Ins können mit Virtual Outlook über MAPI interagieren</p></td>
</tr>
<tr class="odd">
<td align="left"><p>SharePoint-Plug-in für Firefox</p></td>
<td align="left"><p>Benutzer kann SharePoint-Features in Firefox verwenden</p></td>
</tr>
<tr class="even">
<td align="left"><p>Applet für Mail-Systemsteuerung</p></td>
<td align="left"><p>Der Benutzer erhält das Applet für die Mail-Systemsteuerung in Outlook</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Primäre Interop-Assemblys</p></td>
<td align="left"><p>Unterstützung verwalteter Add-ins</p></td>
</tr>
<tr class="even">
<td align="left"><p>Cache Handler für Office-Dokumente</p></td>
<td align="left"><p>Ermöglicht den Dokumenten Cache für Office-Anwendungen</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Outlook-Protokoll such Handler</p></td>
<td align="left"><p>Benutzer kann in Outlook suchen</p></td>
</tr>
<tr class="even">
<td align="left"><p>ActiveX-Steuerelemente:</p></td>
<td align="left"><p>Weitere Informationen zu ActiveX-Steuerelementen finden Sie unter <a href="https://go.microsoft.com/fwlink/p/?LinkId=331361" data-raw-source="[ActiveX Control API Reference](https://go.microsoft.com/fwlink/p/?LinkId=331361)"> API-Referenz für ActiveX-Steuerelemente </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>   Groove. SiteClient</p></td>
<td align="left"><p>Active X-Steuerelement</p></td>
</tr>
<tr class="even">
<td align="left"><p>   PortalConnect.PersonalSite</p></td>
<td align="left"><p>Active X-Steuerelement</p></td>
</tr>
<tr class="odd">
<td align="left"><p>   SharePoint. OpenDocuments</p></td>
<td align="left"><p>Active X-Steuerelement</p></td>
</tr>
<tr class="even">
<td align="left"><p>   SharePoint. ExportDatabase</p></td>
<td align="left"><p>Active X-Steuerelement</p></td>
</tr>
<tr class="odd">
<td align="left"><p>   SharePoint. SpreadSheetLauncher</p></td>
<td align="left"><p>Active X-Steuerelement</p></td>
</tr>
<tr class="even">
<td align="left"><p>   SharePoint. StssyncHander</p></td>
<td align="left"><p>Active X-Steuerelement</p></td>
</tr>
<tr class="odd">
<td align="left"><p>   SharePoint. DragUploadCtl</p></td>
<td align="left"><p>Active X-Steuerelement</p></td>
</tr>
<tr class="even">
<td align="left"><p>   SharePoint. DragDownloadCtl</p></td>
<td align="left"><p>Active X-Steuerelement</p></td>
</tr>
<tr class="odd">
<td align="left"><p>   SharePoint. XMLDocuments</p></td>
<td align="left"><p>Active X-Steuerelement</p></td>
</tr>
<tr class="even">
<td align="left"><p>   SharePoint. ClipboardCtl</p></td>
<td align="left"><p>Active X-Steuerelement</p></td>
</tr>
<tr class="odd">
<td align="left"><p>   Winproj. Activator</p></td>
<td align="left"><p>Active X-Steuerelement</p></td>
</tr>
<tr class="even">
<td align="left"><p>   Name. NameCtrl</p></td>
<td align="left"><p>Active X-Steuerelement</p></td>
</tr>
<tr class="odd">
<td align="left"><p>   STSUPld. CopyCtl</p></td>
<td align="left"><p>Active X-Steuerelement</p></td>
</tr>
<tr class="even">
<td align="left"><p>   CommunicatorMeetingJoinAx. joinmanager</p></td>
<td align="left"><p>Active X-Steuerelement</p></td>
</tr>
<tr class="odd">
<td align="left"><p>   LISTNET. Listnet</p></td>
<td align="left"><p>Active X-Steuerelement</p></td>
</tr>
<tr class="even">
<td align="left"><p>   OneDrive pro-Browser-Helfer</p></td>
<td align="left"><p>Active X-Steuerelement]</p></td>
</tr>
<tr class="odd">
<td align="left"><p>OneDrive pro-symbolüberlagerungen</p></td>
<td align="left"><p>Windows Explorer-Shell-Symbol Overlays, wenn Benutzerordner OneDrive pro-Ordner anzeigen</p></td>
</tr>
<tr class="even">
<td align="left"><p>-Shell-Erweiterungen</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Kombinationen</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Search</p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>

 






 

 





