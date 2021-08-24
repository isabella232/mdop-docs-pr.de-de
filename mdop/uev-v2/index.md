---
title: Microsoft User Experience Virtualization (UE-V) 2,x
description: Microsoft User Experience Virtualization (UE-V) 2,x
author: dansimp
ms.assetid: b860fed0-b846-415d-bdd6-ba60231a64be
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 04/19/2017
ms.openlocfilehash: 79748e04ae1a59afdc8f9dae3c5dc77c50e3c253
ms.sourcegitcommit: 3e0500abde44d6a09c7ac8e3caf5e25929b490a4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2021
ms.locfileid: "11910540"
---
# <a name="microsoft-user-experience-virtualization-ue-v-2x"></a>Microsoft User Experience Virtualization (UE-V) 2,x

>[!NOTE]
>Diese Dokumentation ist eine Version von UE-V, die im Microsoft Desktop Optimization Pack (MDOP) enthalten war. Informationen zur neuesten Version von UE-V, die in Windows 10 Enterprise enthalten ist, finden Sie unter [Erste Schritte mit UE-V.](https://docs.microsoft.com/windows/configuration/ue-v/uev-getting-started)


Erfassen und zentralisieren Sie die Anwendungseinstellungen Ihrer Benutzer und Windows Betriebssystemeinstellungen, indem Sie Microsoft User Experience Virtualization (UE-V) 2.0 oder 2.1 implementieren. Wenden Sie diese Einstellungen dann auf die Geräte an, auf die Benutzer in Ihrem Unternehmen zugreifen, z. B. Desktopcomputer, Laptops oder VDI-Sitzungen (Virtual Desktop Infrastructure).

**Mit UE-V können Sie...**

-   Angeben, welche Anwendungs- und Desktopeinstellungen synchronisiert werden

-   Orts- und zeitunabhängige Bereitstellung der Einstellungen im Unternehmen

-   Erstellen benutzerdefinierter Vorlagen für Drittanbieter- oder Branchenanwendungen

-   Wiederherstellen von Einstellungen nach dem Hardwareaustausch oder -upgrade oder nach dem Neuinagieren eines virtuellen Computers in den ursprünglichen Zustand

## <a name="components-of-ue-v-2x"></a>Komponenten von UE-V 2.x


Dieses Diagramm zeigt, wie bereitgestellte UE-V-Komponenten zusammenarbeiten, um Einstellungen zu synchronisieren.

![uev2-Architekturdiagramm.](images/uev2archdiagram.gif)

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
<td align="left"><p><strong>UE-V Agent</strong></p></td>
<td align="left"><p>Auf jedem Computer installiert, der Einstellungen synchronisieren muss, überwacht der <strong> UE-V-Agent </strong> registrierte Anwendungen und das Betriebssystem auf Alle Einstellungsänderungen und synchronisiert diese Einstellungen dann zwischen Computern.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Einstellungen Pakete</strong></p></td>
<td align="left"><p>Anwendungseinstellungen und Windows Einstellungen werden in <strong> Einstellungspaketen gespeichert, </strong> die vom UE-V-Agent erstellt wurden. Einstellungspakete werden erstellt, lokal gespeichert und an den Speicherort für die Einstellungen kopiert.</p>
<ul>
<li><p>Die Einstellungswerte für <strong> Desktopanwendungen </strong> werden gespeichert, wenn der Benutzer die Anwendung schließt.</p></li>
<li><p>Werte für <strong> Windows Einstellungen </strong> werden gespeichert, wenn sich der Benutzer abmeldet, wenn der Computer gesperrt ist oder wenn der Benutzer die Remoteverbindung von einem Computer trennt.</p></li>
</ul>
<p>Der Synchronisierungsanbieter bestimmt, wann die Anwendungs- oder Betriebssystemeinstellungen aus dem Einstellungen Pakete gelesen <strong> </strong> und synchronisiert werden.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Einstellungen Speicherort</strong></p></td>
<td align="left"><p>Dies ist eine Standardnetzwerkfreigabe, auf die Ihre Benutzer zugreifen können. Der UE-V-Agent überprüft den Speicherort und erstellt einen ausgeblendeten Systemordner, in dem Benutzereinstellungen gespeichert und abgerufen werden.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Einstellungen Standortvorlagen</strong></p></td>
<td align="left"><p>UE-V verwendet XML-Dateien als Speicherortvorlagen für Einstellungen zum Überwachen und Synchronisieren von Desktopanwendungseinstellungen und Windows Desktopeinstellungen zwischen Benutzercomputern. Standardmäßig sind einige Einstellungsortvorlagen in UE-V enthalten. Sie können auch benutzerdefinierte Einstellungsspeicherortvorlagen erstellen, bearbeiten oder überprüfen, indem Sie die <a href="#customapps" data-raw-source="[managing settings synchronization for custom applications](#customapps)"> Einstellungssynchronisierung für benutzerdefinierte Anwendungen </a> verwalten.</p>
<div class="alert">
<strong>Hinweis:</strong><br/><p>Einstellungen Standortvorlagen sind für Windows Apps nicht erforderlich.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Windows App-Liste</strong></p></td>
<td align="left"><p>Einstellungen für Windows Apps werden erfasst und dynamisch angewendet. Der App-Entwickler gibt die Einstellungen an, die für jede App synchronisiert werden. UE-V bestimmt mithilfe einer verwalteten Liste von Apps, welche Windows Apps für die Einstellungssynchronisierung aktiviert sind. Standardmäßig enthält diese Liste die meisten Windows-Apps.</p>
<p>Sie können Anwendungen in der Windows App-Liste hinzufügen oder entfernen, indem Sie die hier gezeigten Verfahren <a href="https://technet.microsoft.com/library/dn458925.aspx" data-raw-source="[here](https://technet.microsoft.com/library/dn458925.aspx)"> </a> ausführen.</p></td>
</tr>
</tbody>
</table>



### <a name="managing-settings-synchronization-for-custom-applications"></a><a href="" id="customapps"></a>Verwalten Einstellungen Synchronisierung für benutzerdefinierte Anwendungen

Verwenden Sie diese UE-V Komponenten, um benutzerdefinierte Vorlagen für Ihre Drittanbieter- oder Branchenanwendungen zu erstellen und zu verwalten.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>UE-V Generator</strong></p></td>
<td align="left"><p>Verwenden Sie den <strong> UE-V </strong> Generator, um benutzerdefinierte Einstellungsspeicherortvorlagen zu erstellen, die Sie dann auf Benutzercomputer verteilen können. Mit dem UE-V-Generator können Sie auch eine vorhandene Vorlage bearbeiten oder eine Vorlage überprüfen, die mit einem anderen XML-Editor erstellt wurde.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Einstellungen Vorlagenkatalog</strong></p></td>
<td align="left"><p>Der <strong> Einstellungsvorlagenkatalog </strong> ist ein Ordnerpfad auf UE-V Computern oder eine SMB-Netzwerkfreigabe (Server Message Block), in der die benutzerdefinierten Einstellungsspeicherortvorlagen gespeichert sind. Der UE-V-Agent überprüft diesen Speicherort einmal täglich, ruft neue oder aktualisierte Vorlagen ab und aktualisiert das Synchronisierungsverhalten.</p>
<p>Wenn Sie nur die UE-V Standardeinstellungsspeicherortvorlagen verwenden, ist kein Einstellungsvorlagenkatalog erforderlich. Weitere Informationen zu Einstellungsbereitstellungskatalogen finden Sie unter <a href="https://technet.microsoft.com/library/dn458942.aspx#deploycatalogue" data-raw-source="[Configure a UE-V settings template catalog](https://technet.microsoft.com/library/dn458942.aspx#deploycatalogue)"> Konfigurieren eines UE-V Einstellungsvorlagenkatalogs. </a></p></td>
</tr>
</tbody>
</table>



![ue-v-Generatorprozess.](images/ue-vgeneratorprocess.gif)

## <a name="settings-synchronized-by-default"></a>Einstellungen Standardmäßig synchronisiert


UE-V synchronisiert einstellungen für diese Anwendungen standardmäßig. Eine vollständige Liste und ausführlichere Informationen finden Sie unter [Einstellungen, die in einer UE-V Bereitstellung automatisch synchronisiert werden.](https://technet.microsoft.com/library/dn458932.aspx#autosyncsettings)

Microsoft Office 2013-Anwendungen (UE-V 2.1 SP1 und 2.1)

Microsoft Office 2010-Anwendungen (UE-V 2.1 SP1, 2.1 und 2.0)

Microsoft Office 2007 Anwendungen (nur UE-V 2.0)

Internet Explorer 8, 9 und 10

Internet Explorer 11 in UE-V 2.1 SP1 und 2.1

Viele Windows-Anwendungen, z. B. Xbox

Viele Windows Desktopanwendungen, z. B. Editor

Viele Windows Einstellungen, z. B. Desktophintergrund oder Hintergrundbild

**Hinweis:**  
Sie können [auch UE-V anpassen, um Einstellungen](https://technet.microsoft.com/library/dn458942.aspx) für anwendungen zu synchronisieren, die nicht standardmäßig synchronisiert werden.



## <a name="compare-ue-v-to-other-microsoft-products"></a>Vergleichen UE-V mit anderen Microsoft-Produkten


Verwenden Sie diese Tabelle, um UE-V mit der Synchronisierung von Profilen in Windows 7, der Synchronisierung von Profilen in Windows 8 und dem Feature "Synchronisierungs-PC Einstellungen Microsoft-Kontos" zu vergleichen.

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
<th align="left">Synchronisieren von Profilen mithilfe von Windows 8</th>
<th align="left">Synchronisieren von Profilen mithilfe von Windows 10</th>
<th align="left">Microsoft-Konto</th>
<th align="left">UE-V 2.0</th>
<th align="left">UE-V 2.1 und 2.1 SP1</th>
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
<td align="left"><p>Synchronisieren von Einstellungen zwischen physischen und virtuellen Apps</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Synchronisieren Windows App-Einstellungen</p></td>
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
<td align="left"><p>Regelmäßiges Synchronisieren von Einstellungsänderungen</p></td>
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
<td align="left"><p>Unterstützt auf Computern, die keiner Domäne angehören</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>●</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Unterstützt das Active Directory-Attribut "Primärer Computer"</p></td>
<td align="left"><p></p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Synchronisiert Einstellungen zwischen virtueller Desktopinfrastruktur (VDI)/Remotedesktopdienste (RDS) und Rich-Desktops.</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
</tr>
<tr class="even">
<td align="left"><p>Unbegrenztes Festlegen des Speicherplatzes</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p></p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Auswahl, in welcher App-Einstellungen synchronisiert werden soll</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
</tr>
<tr class="even">
<td align="left"><p>Sicherung/Wiederherstellung für IT-Pro</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>Teilweise</p></td>
<td align="left"><p>●</p></td>
</tr>
</tbody>
</table>



## <a name="ue-v-2x-release-notes"></a>UE-V Versionshinweise zu 2.x


Weitere Informationen und späte Neuigkeiten, die nicht in die Dokumentation gelangt sind, finden Sie unter

-   [Versionshinweise zu Microsoft User Experience Virtualization (UE-V) 2.1 SP1](microsoft-user-experience-virtualization--ue-v--21-sp1-release-notes.md)

-   [Versionshinweise zu Microsoft User Experience Virtualization (UE-V) 2.1](microsoft-user-experience-virtualization--ue-v--21-release-notesuevv21.md)

-   [Versionshinweise zu Microsoft User Experience Virtualization (UE-V) 2.0](microsoft-user-experience-virtualization--ue-v--20-release-notesuevv2.md)

## <a name="other-resources-for-this-product"></a>Weitere Ressourcen für dieses Produkt


-   [Erste Schritte mit UE-V 2.x](get-started-with-ue-v-2x-new-uevv2.md)

-   [Vorbereiten einer UE-V 2.x-Bereitstellung](prepare-a-ue-v-2x-deployment-new-uevv2.md)

-   [Verwalten von UE-V 2.x](administering-ue-v-2x-new-uevv2.md)

-   [Problembehandlung UE-V 2.x](troubleshooting-ue-v-2x-both-uevv2.md)

-   [Technische Referenz für UE-V 2.x](technical-reference-for-ue-v-2x-both-uevv2.md)

### <a name="more-information"></a>Weitere Informationen

<a href="" id="mdop-techcenter-page"></a>[MDOP TechCenter-Seite](https://go.microsoft.com/fwlink/p/?LinkId=225286) Erfahren Sie mehr über die neuesten MDOP-Informationen und -Ressourcen.

<a href="" id="mdop-information-experience"></a>[MDOP Information Experience](https://go.microsoft.com/fwlink/p/?LinkId=236032) Hier finden Sie Dokumentationen, Videos und andere Ressourcen für MDOP-Technologien. Sie können uns auch [Feedback senden](mailto:MDOPDocs@microsoft.com) oder Sich über Updates informieren, indem Sie uns auf [Facebook](https://go.microsoft.com/fwlink/p/?LinkId=242445) oder [Twitter](https://go.microsoft.com/fwlink/p/?LinkId=242447)folgen.














