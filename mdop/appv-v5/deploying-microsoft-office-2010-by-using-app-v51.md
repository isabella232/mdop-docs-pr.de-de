---
title: Bereitstellen von Microsoft Office2010 mit App-V
description: Bereitstellen von Microsoft Office2010 mit App-V
author: dansimp
ms.assetid: ae0b0459-c0d6-4946-b62d-ff153f52d1fb
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 90454373e9a1c894eba8cbf1b8642656b986bc94
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805867"
---
# Bereitstellen von Microsoft Office2010 mit App-V


Sie können Office 2010-Pakete für Microsoft Application Virtualization (App-V) 5,1 mithilfe einer der folgenden Methoden erstellen:

-   Application Virtualization (App-V)-Sequenzer

-   Application Virtualization (App-V)-Paket Beschleuniger

## App-V-Unterstützung für Office 2010


In der folgenden Tabelle sind die App-V-Versionen, Methoden der Office-Paketerstellung, unterstützte Lizenzierung und unterstützte Bereitstellungen für Office 2010 zu finden.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Unterstütztes Element</th>
<th align="left">Supportstufe</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Unterstützte App-V-Versionen</p></td>
<td align="left"><ul>
<li><p>4,6</p></li>
<li><p>5.0</p></li>
<li><p>5,1</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Paketerstellung</p></td>
<td align="left"><ul>
<li><p>Sequenzierung</p></li>
<li><p>Paket Beschleuniger</p></li>
<li><p>Office Deployment Kit</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>Unterstützte Lizenzierung</p></td>
<td align="left"><p>Volumenlizenzierung</p></td>
</tr>
<tr class="even">
<td align="left"><p>Unterstützte Bereitstellungen</p></td>
<td align="left"><ul>
<li><p>Desktop</p></li>
<li><p>Persönlicher VDI</p></li>
<li><p>RDS</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

## Erstellen von Office 2010 App-V 5,1 mithilfe des Sequencers


Die Sequenzierung von Office 2010 ist eine der Hauptmethoden zum Erstellen eines Office 2010-Pakets unter App-V 5,1. Microsoft hat in einem Knowledge Base-Artikel eine detaillierte Anleitung bereitgestellt. Informationen zum Erstellen eines Office 2010-Pakets unter App-V 5,1 finden Sie unter dem folgenden Link für detaillierte Anweisungen:

[Sequenzierung von Microsoft Office 2010 in Microsoft Application Virtualization 5,0](https://go.microsoft.com/fwlink/p/?LinkId=330676)

## Erstellen von Office 2010-App-V 5,1-Paketen mithilfe von Paket Beschleunigern


Office 2010 App-V 5,1-Pakete können über Paket Beschleuniger erstellt werden. Microsoft hat Paket Beschleuniger für die Erstellung von Office 2010 unter Windows 10, Windows 8 und Windows 7 bereitgestellt. Informationen zum Erstellen von Office 2010-Paketen für App-V mithilfe von Paket Beschleunigern finden Sie auf den folgenden Seiten, um auf den entsprechenden Paket Beschleuniger zuzugreifen:

-   [App-V 5,0-Paket Beschleuniger für Office Professional Plus 2010 – Windows 8](https://go.microsoft.com/fwlink/p/?LinkId=330677)

-   [App-V 5,0-Paket Beschleuniger für Office Professional Plus 2010 – Windows 7](https://go.microsoft.com/fwlink/p/?LinkId=330678)

Ausführliche Anweisungen zum Erstellen von virtuellen Anwendungspaketen mithilfe von App-v-Paket Beschleunigern finden Sie unter [Erstellen eines virtuellen Anwendungspakets mithilfe eines App-v-Paket Beschleunigers](how-to-create-a-virtual-application-package-using-an-app-v-package-accelerator51.md).

## Bereitstellen des Microsoft Office-Pakets für App-V 5,1


Sie können Office 2010-Pakete mithilfe einer der folgenden Bereitstellungsmethoden für App-V bereitstellen:

-   System Center Konfigurations-Manager

-   App-V-Server

-   Eigenständige über PowerShell-Befehle

## Office-App-V-Paketverwaltung und-Anpassung


Office 2010-Pakete können wie alle anderen App-V 5,1-Pakete über bekannte Paket Verwaltungsmechanismen verwaltet werden. Es sind keine speziellen Anweisungen erforderlich, beispielsweise zum Hinzufügen, veröffentlichen, Aufheben der Veröffentlichung oder Entfernen von Office-Paketen.

## Integration von Microsoft Office in Windows


Die folgende Tabelle enthält eine vollständige Liste der unterstützten Integrationspunkte für Office 2010.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Erweiterungspunkt</th>
<th align="left">Beschreibung</th>
<th align="left">Office 2010</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Lync-Besprechungsteilnahme-Plug-in für Firefox und Chrome</p></td>
<td align="left"><p>Benutzer können über Firefox und Chrome an lync-Besprechungen teilnehmen</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>An den OneNote-Druckertreiber gesendet</p></td>
<td align="left"><p>Benutzer kann in OneNote drucken</p></td>
<td align="left"><p>Ja</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Verknüpfte OneNote-Notizen</p></td>
<td align="left"><p>Verknüpfte OneNote-Notizen</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>An OneNote Internet Explorer-Add-in senden</p></td>
<td align="left"><p>Benutzer kann von IE an OneNote senden</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Firewall-Ausnahme für lync und Outlook</p></td>
<td align="left"><p>Firewall-Ausnahme für lync und Outlook</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>MAPI-Client</p></td>
<td align="left"><p>Systemeigene apps und Add-Ins können mit Virtual Outlook über MAPI interagieren</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>SharePoint-Plug-in für Firefox</p></td>
<td align="left"><p>Benutzer kann SharePoint-Features in Firefox verwenden</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Applet für Mail-Systemsteuerung</p></td>
<td align="left"><p>Der Benutzer erhält das Applet für die Mail-Systemsteuerung in Outlook</p></td>
<td align="left"><p>Ja</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Primäre Interop-Assemblys</p></td>
<td align="left"><p>Unterstützung verwalteter Add-ins</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Cache Handler für Office-Dokumente</p></td>
<td align="left"><p>Ermöglicht den Dokumenten Cache für Office-Anwendungen</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Outlook-Protokoll such Handler</p></td>
<td align="left"><p>Benutzer kann in Outlook suchen</p></td>
<td align="left"><p>Ja</p></td>
</tr>
<tr class="even">
<td align="left"><p>ActiveX-Steuerelemente:</p></td>
<td align="left"><p>Weitere Informationen zu ActiveX-Steuerelementen finden Sie unter <a href="https://go.microsoft.com/fwlink/p/?LinkId=331361" data-raw-source="[ActiveX Control API Reference](https://go.microsoft.com/fwlink/p/?LinkId=331361)"> API-Referenz für ActiveX-Steuerelemente </a> .</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   Groove. SiteClient</p></td>
<td align="left"><p>Active X-Steuerelement</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   PortalConnect.PersonalSite</p></td>
<td align="left"><p>Active X-Steuerelement</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   SharePoint. OpenDocuments</p></td>
<td align="left"><p>Active X-Steuerelement</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   SharePoint. ExportDatabase</p></td>
<td align="left"><p>Active X-Steuerelement</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   SharePoint. SpreadSheetLauncher</p></td>
<td align="left"><p>Active X-Steuerelement</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   SharePoint. StssyncHander</p></td>
<td align="left"><p>Active X-Steuerelement</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   SharePoint. DragUploadCtl</p></td>
<td align="left"><p>Active X-Steuerelement</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   SharePoint. DragDownloadCtl</p></td>
<td align="left"><p>Active X-Steuerelement</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   Sharpoint. XMLDocuments</p></td>
<td align="left"><p>Active X-Steuerelement</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   SharePoint. ClipboardCtl</p></td>
<td align="left"><p>Active X-Steuerelement</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   Winproj. Activator</p></td>
<td align="left"><p>Active X-Steuerelement</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   Name. NameCtrl</p></td>
<td align="left"><p>Active X-Steuerelement</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   STSUPld. CopyCtl</p></td>
<td align="left"><p>Active X-Steuerelement</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   CommunicatorMeetingJoinAx. joinmanager</p></td>
<td align="left"><p>Active X-Steuerelement</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   LISTNET. Listnet</p></td>
<td align="left"><p>Active X-Steuerelement</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   OneDrive pro-Browser-Helfer</p></td>
<td align="left"><p>Active X-Steuerelement]</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>OneDrive pro-symbolüberlagerungen</p></td>
<td align="left"><p>Windows Explorer-Shell-Symbol Overlays, wenn Benutzerordner OneDrive pro-Ordner anzeigen</p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>

 

## Zusätzliche Ressourcen


**Office 2013-App-V-Pakete – zusätzliche Ressourcen**

[Unterstützte Szenarien für die Bereitstellung von Microsoft Office als sequenziertes App-V-Paket](https://go.microsoft.com/fwlink/p/?LinkId=330680)

**Office 2010-App-V-Pakete**

[Microsoft Office 2010-Sequenzierung-Kit für Microsoft Application Virtualization 5,0](https://go.microsoft.com/fwlink/p/?LinkId=330681)

[Bekannte Probleme beim Erstellen oder Verwenden eines App-V 5,0 Office 2010-Pakets](https://go.microsoft.com/fwlink/p/?LinkId=330682)

[Sequenzierung von Microsoft Office 2010 in Microsoft Application Virtualization 5,0](https://go.microsoft.com/fwlink/p/?LinkId=330676)

**Verbindungsgruppen**

[Bereitstellen von Verbindungsgruppen in Microsoft App-V V5](https://go.microsoft.com/fwlink/p/?LinkId=330683)

[Verwalten von Verbindungsgruppen](managing-connection-groups51.md)

**Dynamische Konfiguration**

[Informationen zur dynamischen Konfiguration in App-V 5.1](about-app-v-51-dynamic-configuration.md)






 

 





