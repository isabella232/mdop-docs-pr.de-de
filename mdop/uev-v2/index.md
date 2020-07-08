---
title: Microsoft User Experience Virtualization (UE-V) 2. x
description: Microsoft User Experience Virtualization (UE-V) 2. x
author: dansimp
ms.assetid: b860fed0-b846-415d-bdd6-ba60231a64be
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 04/19/2017
ms.openlocfilehash: 573b8bb2027e5c7f117a8254005a43c656f047a9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10795814"
---
# Microsoft User Experience Virtualization (UE-V) 2. x

>[!NOTE]
>Diese Dokumentation ist eine für die Version von UE-V, die im Microsoft-Desktop Optimierungspaket (MDOP) enthalten war. Informationen zur neuesten Version von UE-v, die in Windows 10 Enterprise enthalten ist, finden Sie unter [Erste Schritte mit UE-v](https://docs.microsoft.com/windows/configuration/ue-v/uev-getting-started).


Erfassen und zentralisieren Sie die Anwendungseinstellungen und Windows-Betriebssystem Einstellungen Ihrer Benutzer, indem Sie die Microsoft User Experience Virtualization (UE-V) 2,0 oder 2,1 implementieren. Wenden Sie diese Einstellungen dann auf die Geräte an, auf die Benutzer in Ihrem Unternehmen zugreifen, wie Desktopcomputer, Laptops oder VDI-Sitzungen (Virtual Desktop Infrastructure).

**Mit UE-V können Sie...**

-   Angeben, welche Anwendungs-und Desktopeinstellungen synchronisiert werden sollen

-   Orts- und zeitunabhängige Bereitstellung der Einstellungen im Unternehmen

-   Erstellen benutzerdefinierter Vorlagen für Drittanbieter- oder Branchenanwendungen

-   Wiederherstellen von Einstellungen nach dem Hardwareaustausch oder-Upgrade oder nach dem erneuten Imaging einer virtuellen Maschine in Ihrem ursprünglichen Zustand

## Komponenten von UE-V 2. x


Dieses Diagramm zeigt, wie die bereitgestellten UE-V-Komponenten zum Synchronisieren von Einstellungen zusammenarbeiten.

![uev2-Architekturdiagramm](images/uev2archdiagram.gif)

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Komponente</th>
<th align="left">Funktion</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>UE-V-Agent</strong></p></td>
<td align="left"><p>Auf jedem Computer, auf dem die Einstellungen synchronisiert werden müssen, <strong> überwacht der UE-V-Agent </strong> registrierte Anwendungen und das Betriebssystem für alle Einstellungen und synchronisiert dann diese Einstellungen zwischen Computern.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Einstellungen-Pakete</strong></p></td>
<td align="left"><p>Anwendungseinstellungen und Windows-Einstellungen werden in <strong> </strong> den vom UE-V-Agent erstellten Einstellungspaketen gespeichert. Einstellungspakete werden erstellt, lokal gespeichert und an den Speicherort für die Einstellungen kopiert.</p>
<ul>
<li><p>Die Einstellungswerte für <strong> Desktopanwendungen </strong> werden gespeichert, wenn der Benutzer die Anwendung schließt.</p></li>
<li><p>Werte für <strong> Windows </strong> -Einstellungen werden gespeichert, wenn sich der Benutzer abmeldet, wenn der Computer gesperrt ist oder wenn der Benutzer die Verbindung von einem Computer entfernt trennt.</p></li>
</ul>
<p>Der Synchronisierungsanbieter bestimmt, wann die Anwendungs-oder Betriebssystemeinstellungen aus den <strong> Einstellungspaketen gelesen </strong> und synchronisiert werden.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Speicherort des Einstellungs Speichers</strong></p></td>
<td align="left"><p>Hierbei handelt es sich um eine standardmäßige Netzwerkfreigabe, auf die Ihre Benutzer zugreifen können. Der UE-V-Agent überprüft den Standort und erstellt einen versteckten Systemordner, in dem Benutzereinstellungen gespeichert und abgerufen werden können.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Einstellungen-Speicherort Vorlagen</strong></p></td>
<td align="left"><p>UE-V verwendet XML-Dateien als Speicherort Vorlagen für Einstellungen, um die Einstellungen für die Desktopanwendung und die Windows-Desktopeinstellungen zwischen den Benutzercomputern zu überwachen und zu synchronisieren. Standardmäßig sind einige Einstellungen für Speicherort Vorlagen in UE-V enthalten. Sie können auch Standort Vorlagen für benutzerdefinierte Einstellungen erstellen, bearbeiten oder überprüfen, indem Sie die <a href="#customapps" data-raw-source="[managing settings synchronization for custom applications](#customapps)"> Synchronisierung von Einstellungen für benutzerdefinierte Anwendungen verwalten </a> .</p>
<div class="alert">
<strong>Hinweis:</strong><br/><p>Für Windows-apps sind keine Speicherort Vorlagen für Einstellungen erforderlich.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Windows-App-Liste</strong></p></td>
<td align="left"><p>Einstellungen für Windows-apps werden erfasst und dynamisch angewendet. Der App-Entwickler gibt die Einstellungen an, die für jede APP synchronisiert werden. UE-V legt fest, welche Windows-Apps für die Synchronisierung von Einstellungen unter Verwendung einer verwalteten Liste von apps aktiviert sind. Diese Liste enthält standardmäßig die meisten Windows-apps.</p>
<p>Sie können Anwendungen in der Windows-App-Liste hinzufügen oder entfernen, indem Sie die hier gezeigten Verfahren befolgen <a href="https://technet.microsoft.com/library/dn458925.aspx" data-raw-source="[here](https://technet.microsoft.com/library/dn458925.aspx)"> </a> .</p></td>
</tr>
</tbody>
</table>



### <a href="" id="customapps"></a>Verwalten der Synchronisierung von Einstellungen für benutzerdefinierte Anwendungen

Verwenden Sie diese UE-V-Komponenten, um benutzerdefinierte Vorlagen für Ihre Drittanbieter-oder Branchenanwendungen zu erstellen und zu verwalten.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>UE-V-Generator</strong></p></td>
<td align="left"><p>Verwenden <strong> Sie den UE-V-Generator </strong> , um benutzerdefinierte Standort Vorlagen für Einstellungen zu erstellen, die Sie dann an Benutzer Computer verteilen können. Mit dem UE-V-Generator können Sie auch eine vorhandene Vorlage bearbeiten oder eine Vorlage überprüfen, die mit einem anderen XML-Editor erstellt wurde.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Vorlagenkatalog für Einstellungen</strong></p></td>
<td align="left"><p>Der <strong> Einstellungs Vorlagenkatalog </strong> ist ein Ordnerpfad auf UE-V-Computern oder eine SMB-Netzwerkfreigabe (Server Message Block), in der die Speicherort Vorlagen für benutzerdefinierte Einstellungen gespeichert sind. Der UE-V-Agent überprüft diesen Speicherort einmal täglich, ruft neue oder aktualisierte Vorlagen ab und aktualisiert das Synchronisierungsverhalten.</p>
<p>Wenn Sie nur die Standort Vorlagen für die UE-V-Standardeinstellungen verwenden, ist ein Einstellungs Vorlagenkatalog nicht erforderlich. Weitere Informationen zu Einstellungen für die Bereitstellungs Kataloge finden Sie unter <a href="https://technet.microsoft.com/library/dn458942.aspx#deploycatalogue" data-raw-source="[Configure a UE-V settings template catalog](https://technet.microsoft.com/library/dn458942.aspx#deploycatalogue)"> Konfigurieren eines UE-V-Einstellungs Vorlagen Katalogs </a> .</p></td>
</tr>
</tbody>
</table>



![UE-v-Generator Prozess](images/ue-vgeneratorprocess.gif)

## Standardmäßige Synchronisierung von Einstellungen


UE-V synchronisiert die Einstellungen für diese Anwendungen standardmäßig. Eine vollständige Liste und ausführlichere Informationen finden Sie unter [Einstellungen, die in einer UE-V-Bereitstellung automatisch synchronisiert werden](https://technet.microsoft.com/library/dn458932.aspx#autosyncsettings).

Microsoft Office 2013-Anwendungen (UE-V 2,1 SP1 und 2,1)

Microsoft Office 2010-Anwendungen (UE-V 2,1 SP1, 2,1 und 2,0)

Microsoft Office 2007-Anwendungen (nur UE-V 2,0)

Internet Explorer 8, 9 und 10

Internet Explorer 11 in UE-V 2,1 SP1 und 2,1

Viele Windows-Anwendungen wie Xbox

Viele Windows-Desktopanwendungen wie Notepad

Viele Windows-Einstellungen wie Desktop Hintergrund oder Hintergrund

**Hinweis:**  
Sie können [UE-V auch so anpassen, dass Einstellungen](https://technet.microsoft.com/library/dn458942.aspx) für Anwendungen synchronisiert werden, die nicht standardmäßig synchronisiert sind.



## Vergleich von UE-V mit anderen Microsoft-Produkten


Verwenden Sie diese Tabelle, um UE-V zu vergleichen, um Profile in Windows 7 zu synchronisieren, Profile in Windows 8 zu synchronisieren und das Feature Synchronisierungs-PC-Einstellungen von Microsoft-Konto zu synchronisieren.

<table style="width:100%;">
<colgroup>
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Feature</th>
<th align="left">Synchronisieren von Profilen mit Windows 7</th>
<th align="left">Synchronisieren von Profilen mit Windows 8</th>
<th align="left">Synchronisieren von Profilen mithilfe von Windows 10</th>
<th align="left">Microsoft-Konto</th>
<th align="left">UE-V 2,0</th>
<th align="left">UE-V 2,1 und 2,1 SP1</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Synchronisieren von Einstellungen zwischen mehreren Computern</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
</tr>
<tr class="even">
<td align="left"><p>Synchronisieren von Einstellungen zwischen physischen und virtuellen apps</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Synchronisieren von Windows-App-Einstellungen</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
</tr>
<tr class="even">
<td align="left"><p>Verwalten über WMI</p></td>
<td align="left"><p></p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p></p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Regelmäßige Synchronisierung von Einstellungsänderungen</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
</tr>
<tr class="even">
<td align="left"><p>Minimale Konfiguration für Setup</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Unterstützt auf Computern, die nicht mit der Domäne verbunden sind</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>●</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Active Directory-Attribut für primären Computer unterstützt</p></td>
<td align="left"><p></p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Synchronisiert die Einstellungen zwischen Virtual Desktop Infrastructure (VDI)/Remote-Desktop Diensten (RDS) und Rich-Desktops</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
</tr>
<tr class="even">
<td align="left"><p>Unbegrenzter Speicherplatz</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p></p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Auswahl der zu synchronisierenden App-Einstellungen</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
</tr>
<tr class="even">
<td align="left"><p>Backup/Restore für IT-Experten</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>Teilweise</p></td>
<td align="left"><p>●</p></td>
</tr>
</tbody>
</table>



## UE-V 2. x – Anmerkungen zu dieser Version


Weitere Informationen und aktuelle Nachrichten, die nicht in die Dokumentation eingehen, finden Sie unter

-   [Versionshinweise zu Microsoft User Experience Virtualization (UE-V) 2.1 SP1](microsoft-user-experience-virtualization--ue-v--21-sp1-release-notes.md)

-   [Versionshinweise zu Microsoft User Experience Virtualization (UE-V) 2.1](microsoft-user-experience-virtualization--ue-v--21-release-notesuevv21.md)

-   [Versionshinweise zu Microsoft User Experience Virtualization (UE-V) 2.0](microsoft-user-experience-virtualization--ue-v--20-release-notesuevv2.md)

## Weitere Ressourcen für dieses Produkt


-   [Erste Schritte mit UE-V 2.x](get-started-with-ue-v-2x-new-uevv2.md)

-   [Vorbereiten einer UE-V 2. x-Bereitstellung](prepare-a-ue-v-2x-deployment-new-uevv2.md)

-   [Verwalten von UE-V 2. x](administering-ue-v-2x-new-uevv2.md)

-   [Problembehandlung bei UE-V 2. x](troubleshooting-ue-v-2x-both-uevv2.md)

-   [Technische Referenz für UE-V 2.x](technical-reference-for-ue-v-2x-both-uevv2.md)

### Weitere Informationen

<a href="" id="mdop-techcenter-page"></a>[MDOP-TechCenter-Seite](https://go.microsoft.com/fwlink/p/?LinkId=225286) Informieren Sie sich über die neuesten MDOP-Informationen und-Ressourcen.

<a href="" id="mdop-information-experience"></a>[MDOP-Informations Erfahrung](https://go.microsoft.com/fwlink/p/?LinkId=236032) Finden Sie Dokumentation, Videos und andere Ressourcen für MDOP-Technologien. Sie können [uns auch Feedback senden](mailto:MDOPDocs@microsoft.com) oder Informationen zu Updates erhalten, indem Sie uns auf [Facebook](https://go.microsoft.com/fwlink/p/?LinkId=242445) oder [Twitter](https://go.microsoft.com/fwlink/p/?LinkId=242447)folgen.














