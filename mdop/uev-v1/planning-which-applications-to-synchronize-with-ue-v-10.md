---
title: Planen der Verwendung von Anwendungen zum Synchronisieren mit UE-V 1.0
description: Planen der Verwendung von Anwendungen zum Synchronisieren mit UE-V 1.0
author: dansimp
ms.assetid: c718274f-87b4-47f3-8ef7-5e1bd5557a9d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7f2b04942588d0f6efad03d5e0249534cd325c09
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804211"
---
# Planen der Verwendung von Anwendungen zum Synchronisieren mit UE-V 1.0


Microsoft User Experience Virtualization (UE-v) verwendet Einstellungen-Standort Vorlagen (XML-Dateien), die die Einstellungen definieren, die von UE-v erfasst und angewendet werden. UE-V enthält eine Reihe vordefinierter Einstellungen für Standort Vorlagen und ermöglicht es Administratoren auch, benutzerdefinierte Einstellungen für Standort Vorlagen für Drittanbieter-oder Branchenanwendungen zu erstellen, die im Unternehmen verwendet werden.

Wenn Sie als Administrator berücksichtigen, welche Anwendungen in Ihre UE-V-Lösung einbezogen werden sollen, sollten Sie berücksichtigen, welche Einstellungen von Benutzern angepasst werden können und wie und wo die Anwendung die Einstellungen speichert. Nicht alle Anwendungen verfügen über Einstellungen, die angepasst oder regelmäßig von Benutzern angepasst werden können. Darüber hinaus können nicht alle Anwendungseinstellungen über mehrere Computer oder Umgebungen sicher durchlaufen werden. Synchronisieren Sie die Einstellungen, die die folgenden Kriterien erfüllen:

-   Einstellungen, die in Benutzer zugänglichen Speicherorten gespeichert sind. Synchronisieren Sie beispielsweise nicht die Einstellungen, die im System32-oder outside HKCU-Abschnitt der Registrierung gespeichert sind.

-   Einstellungen, die nicht für den jeweiligen Computer spezifisch sind. Schließen Sie beispielsweise Netzwerk-oder Hardwarekonfigurationen aus.

-   Einstellungen, die zwischen Computern synchronisiert werden können, ohne dass ein Risiko für beschädigte Daten besteht. Verwenden Sie beispielsweise keine Einstellungen, die in einer Datenbankdatei gespeichert sind.

## In UE-V enthaltene Positions Vorlagen für Einstellungen


**Standort Vorlagen für UE-V-Anwendungseinstellungen**

Die Installationssoftware des UE-V-Agents installiert den Agenten und registriert eine Standardgruppe von Einstellungen-Standort Vorlagen für gängige Microsoft-Anwendungen. Mit den Einstellungen für die Positions Vorlagen werden die Einstellungswerte für die folgenden Anwendungen erfasst:

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
<td align="left"><p>Microsoft Office 2010-Anwendungen</p></td>
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
<p>Microsoft OneNote 2010</p></td>
</tr>
<tr class="even">
<td align="left"><p>Browser Optionen (Internet Explorer 8, Internet Explorer 9 und Internet Explorer 10)</p></td>
<td align="left"><p>Favoriten, Startseite, Tabstopps und Symbolleisten.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows-Zubehör</p></td>
<td align="left"><p>Rechner, Notepad, WordPad.</p></td>
</tr>
</tbody>
</table>

 

Anwendungseinstellungen werden auf die Anwendung angewendet, wenn die Anwendung gestartet wird. Sie werden beim Schließen der Anwendung gespeichert.

**Standort Vorlagen für UE-V-Windows-Einstellungen**

Die Virtualisierung der Benutzeroberfläche umfasst Einstellungen-Speicherort Vorlagen, mit denen Einstellungswerte für die folgenden Windows-Einstellungen erfasst werden:

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Windows-Einstellungen</th>
<th align="left">Beschreibung</th>
<th align="left">Anwenden auf</th>
<th align="left">Standardzustand</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Desktophintergrund</p></td>
<td align="left"><p>Derzeit aktiver Desktop Hintergrund</p></td>
<td align="left"><p>Anmelden, entsperren, Remoteverbindung.</p></td>
<td align="left"><p>Aktiviert</p></td>
</tr>
<tr class="even">
<td align="left"><p>Erleichterte Bedienung</p></td>
<td align="left"><p>Bedienungshilfen und Eingabeeinstellungen, Bildschirmlupe, Sprachausgabe und Bildschirmtastatur.</p></td>
<td align="left"><p>Anmelden, entsperren, Remoteverbindung.</p></td>
<td align="left"><p>Deaktiviert</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Desktop Einstellungen</p></td>
<td align="left"><p>Startmenü-und Taskleisteneinstellungen, Ordneroptionen, Standard Desktopsymbole, zusätzliche Uhren sowie Regions-und Spracheinstellungen.</p></td>
<td align="left"><p>Nur Anmeldung.</p></td>
<td align="left"><p>Deaktiviert</p></td>
</tr>
</tbody>
</table>

 

Der Windows-Desktop Hintergrund und die Einstellungen für die erleichterte Bedienung werden angewendet, wenn sich der Benutzer anmeldet, wenn der Computer entriegelt wird, oder wenn eine Remoteverbindung mit einem anderen Computer besteht. Der Agent speichert diese Einstellungen, wenn sich der Benutzer abmeldet, wenn der Computer gesperrt ist oder wenn eine Remoteverbindung getrennt wird. Standardmäßig werden die Windows-Desktop Hintergrundeinstellungen zwischen Computern der gleichen Betriebssystemversion durchsucht.

Windows-Desktop und Einstellungen für die erleichterte Bedienung werden bei der Anmeldung angewendet, bevor der Desktop dem Benutzer angezeigt wird. Um die Anmelde Erfahrung zu optimieren, werden diese Einstellungen nicht standardmäßig durchsucht. Die Einstellungen für Desktop und erleichterte Bedienung können mithilfe von Gruppenrichtlinien, PowerShell und WMI aktiviert werden.

UE-V unterstützt nicht das Roaming von Einstellungen zwischen Betriebssystemen mit unterschiedlichen Sprachen. Beispielsweise wird die Synchronisierung zwischen Englisch und Deutsch nicht unterstützt. Die Sprache aller Computer, auf die UE-V die Benutzereinstellungen durchstreift, müssen übereinstimmen.

**Hinweis**  Wenn Sie die von Microsoft bereitgestellten Einstellungen für Standort Vorlagen ändern, funktioniert die Virtualisierung der Benutzeroberfläche möglicherweise nicht ordnungsgemäß für die vorgesehene Anwendung oder Windows-Einstellungsgruppe.

 

## <a href="" id="prevent-unintentional-user-settings-configuration-"></a>Verhindern der unbeabsichtigten Konfiguration von Benutzereinstellungen


Virtualisierung der Benutzeroberfläche überprüft, ob neue Informationen zu den Benutzereinstellungen verwendet werden, und downloadet diese Informationen entsprechend von einem Speicherort für Einstellungen. Anschließend werden die Einstellungen in den folgenden Fällen auf den lokalen Computer angewendet:

-   Jedes Mal, wenn eine Anwendung gestartet wird, die über eine registrierte UE-V-Vorlage verfügt.

-   Wenn sich ein Benutzer bei seinem Computer anmeldet.

-   Wenn ein Benutzer seinen Computer entsperrt.

-   Wenn eine Verbindung mit einem Remote Desktopcomputer hergestellt wird, auf dem UE-V installiert ist.

Wenn UE-V auf Computer a und Computer B installiert ist und die gewünschten Einstellungen für die Anwendung auf Computer a liegen, muss Computer a die Anwendung zuerst öffnen und schließen. Wenn eine Anwendung zuerst auf Computer b geöffnet und geschlossen wird, werden die Anwendungseinstellungen auf Computer A so konfiguriert, dass Sie mit den Anwendungseinstellungen auf Computer b identisch sind.

Dieses Szenario gilt auch für Windows-Einstellungen. Wenn die Windows-Einstellungen auf Computer B mit den Windows-Einstellungen auf Computer a identisch sein sollten, sollte sich der Benutzer zuerst anmelden und den Computer abmelden.

Wenn die gewünschten Benutzereinstellungen in der falschen Reihenfolge angewendet werden, können Sie wiederhergestellt werden, indem Sie einen Wiederherstellungsvorgang für die jeweilige Anwendung oder Windows-Konfiguration auf dem Computer ausführen, auf dem die Einstellungen überschrieben wurden. Weitere Informationen finden Sie unter [Wiederherstellen von Anwendungs-und Windows-Einstellungen, die mit UE-V 1,0 synchronisiert](restoring-application-and-windows-settings-synchronized-with-ue-v-10.md)wurden.

## Benutzerdefinierte Standort Vorlagen für UE-V-Einstellungen


Mithilfe des UE-V-Generators können Sie benutzerdefinierte Standort Vorlagen für Einstellungen erstellen. Nachdem Sie eine Standort Vorlage für benutzerdefinierte Einstellungen in einer Testumgebung erstellt und getestet haben, können Sie die Einstellungen-Speicherort Vorlagen auf Computern im Unternehmen bereitstellen. Speicherort Vorlagen für benutzerdefinierte Einstellungen müssen mit einer vorhandenen Bereitstellungsinfrastruktur bereitgestellt werden, beispielsweise mit der Enterprise Software Distribution (ESD)-Methode, mit Einstellungen oder durch Konfigurieren eines UE-V-Einstellungs Vorlagen Katalogs. Vorlagen, die mit ESD-oder Gruppenrichtlinien bereitgestellt werden, müssen mit UE-V WMI oder PowerShell registriert werden. Weitere Informationen zu den Standort Vorlagen für benutzerdefinierte Einstellungen finden Sie unter [Planen der Bereitstellung von benutzerdefinierten Vorlagen für UE-V 1,0](planning-for-custom-template-deployment-for-ue-v-10.md).

Anleitungen dazu, ob eine Branchenanwendung synchronisiert werden soll, finden Sie unter [Checkliste für die Evaluierung von Branchenanwendungen für UE-V 1,0](checklist-for-evaluating-line-of-business-applications-for-ue-v-10.md).

## Verwandte Themen


[Planen für UE-V 1.0](planning-for-ue-v-10.md)

[Planen der Bereitstellung von benutzerdefinierten Vorlagen für UE-V 1.0](planning-for-custom-template-deployment-for-ue-v-10.md)

[Bereitstellen von UE-V 1.0](deploying-ue-v-10.md)

 

 





