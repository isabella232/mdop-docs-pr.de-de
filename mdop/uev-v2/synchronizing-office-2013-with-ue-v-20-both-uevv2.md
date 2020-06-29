---
title: Synchronisieren von Office 2013 mit UE-V 2,0
description: Synchronisieren von Office 2013 mit UE-V 2,0
author: dansimp
ms.assetid: c46feb6d-28a8-4799-888d-053531dc5842
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: c9b079d3f21e6ced689fa2101f5321fa9b1406c8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812025"
---
# Synchronisieren von Office 2013 mit UE-V 2,0


Microsoft User Experience Virtualization (UE-v) 2,0 unterstützt die Synchronisierung der Microsoft Office 2013-Anwendungseinstellung mithilfe einer Vorlage aus dem UE-v-Vorlagenkatalog. Die Kombination aus UE-v 2 und App-v 5,0 SP2 Unterstützung von Office 2013 Professional Plus ermöglicht die gleiche Erfahrung auf virtualisierten Instanzen von Office 2013 von jedem UE-v-fähigen Gerät oder virtualisierten Desktop.

Um die Unterstützung von UE-v-Anwendungseinstellungen von Office 2013 zu aktivieren, können Sie die offiziellen UE-v Office 2013-Vorlagen aus dem [Vorlagenkatalog Microsoft User Experience Virtualization (UE-v) 2](https://go.microsoft.com/fwlink/p/?LinkId=246589)herunterladen. Diese Ressource bietet von Microsoft verfasste UE-V-Einstellungen für Standort Vorlagen sowie von der Community entwickelte Einstellungen für Standort Vorlagen.

## Microsoft Office-Support in UE-V


UE-v 1,0 und UE-v 2 umfassen Einstellungen-Speicherort Vorlagen für Microsoft Office 2010. Diese Vorlagen werden als Teil des UE-V-Agenten Installationsprozesses verteilt und registriert. Mithilfe dieser Vorlagen können Sie die Office-Benutzererfahrung zwischen Geräten synchronisieren. Die UE-V-Vorlagen für Office 2013 bieten eine sehr ähnliche Einstellungs Oberfläche für die Vorlagen für Office 2010. Microsoft Office 2013-Einstellungen, die durch die Office 365-Umgebung durchlaufen wurden, sind in diesen Einstellungen nicht enthalten. Eine Liste der Office 365-spezifischen Einstellungen finden Sie unter [Übersicht über die Einstellungen für Benutzer und Roaming für Office 2013](https://go.microsoft.com/fwlink/p/?LinkId=391220).

## Synchronisierte Office 2013-Einstellungen


Die folgenden Tabellen enthalten die Details für die Office 2013-Unterstützung in UE-V:

### Unterstützte UE-V-Vorlagen für Microsoft Office

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Office 2013-Vorlagen (UE-v 2,0, verfügbar auf dem UE-v-Katalog):</th>
<th align="left">Office 2010-Vorlagen (UE-V 1,0 &amp; 1,0 SP1):</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>MicrosoftOffice2013Win32.xml</p>
<p>MicrosoftOffice2013Win64.xml</p>
<p>MicrosoftLync2013Win32.xml</p>
<p>MicrosoftLync2013Win64.xml</p></td>
<td align="left"><p>MicrosoftOffice2010Win32.xml</p>
<p>MicrosoftOffice2010Win64.xml</p>
<p>MicrosoftLync2010.xml</p>
<p></p></td>
</tr>
</tbody>
</table>

 

### Von den UE-V-Vorlagen unterstützte Microsoft Office-Anwendungen

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p>Microsoft Access 2013</p>
<p>Microsoft lync 2013</p>
<p>Microsoft Excel 2013</p>
<p>Microsoft InfoPath 2013</p>
<p>Microsoft OneNote 2013</p>
<p>Microsoft Outlook 2013</p>
<p>Microsoft PowerPoint 2013</p>
<p>Microsoft Project 2013</p>
<p>Microsoft Publisher 2013</p>
<p>Microsoft SharePoint Designer 2013</p>
<p>Microsoft Visio 2013</p>
<p>Microsoft Word 2013</p>
<p>Microsoft Office Upload-Manager</p></td>
<td align="left"><p>Microsoft Access 2010</p>
<p>Microsoft lync 2010</p>
<p>Microsoft Excel 2010</p>
<p>Microsoft InfoPath 2010</p>
<p>Microsoft OneNote 2010</p>
<p>Microsoft Outlook 2010</p>
<p>Microsoft PowerPoint 2010</p>
<p>Microsoft Project 2010</p>
<p>Microsoft Publisher 2010</p>
<p>Microsoft SharePoint Designer 2010</p>
<p>Microsoft Visio 2010</p>
<p>Microsoft Word 2010</p>
<p></p></td>
</tr>
</tbody>
</table>

 

## Bereitstellen der Office 2013-Vorlagen


Sie können die Standort Vorlage für UE-V-Einstellungen mit den folgenden Methoden bereitstellen:

-   **Registrieren einer Vorlage über PowerShell** Wenn Sie Windows PowerShell zum Verwalten von Computern verwenden, führen Sie den folgenden Windows PowerShell-Befehl als Administrator öffnen aus, um die Speicherort Vorlage für diese Einstellungen zu registrieren:

    ``` syntax
    Register-UevTemplate -Path <Path_to_Template>
    ```

    Weitere Informationen zur Verwendung von UE-v und Windows PowerShell finden Sie unter [Verwalten von Standort Vorlagen für die UE-v 2. x-Einstellungen mithilfe von Windows PowerShell und WMI](managing-ue-v-2x-settings-location-templates-using-windows-powershell-and-wmi-both-uevv2.md).

-   **Registrieren einer Vorlage über den Vorlagenkatalog Pfad** Wenn Sie den Katalogpfad der Einstellungs Vorlage zum Verwalten von Vorlagen auf den Computern der Benutzer verwenden, kopieren Sie die Office 2013-Vorlage in den Ordner, der im UE-V-Agent definiert ist. Wenn der geplante Task "Vorlage automatisch aktualisieren (ApplySettingsCatalog.exe)" das nächste Mal ausgeführt wird, wird die Vorlage "Settings Location" auf dem Gerät registriert. Weitere Informationen finden Sie unter [Bereitstellen des Einstellungs Vorlagen Katalogs für UE-V 2](https://technet.microsoft.com/library/dn458942.aspx#deploycatalogue).

-   **Registrieren einer Vorlage über Configuration Manager** Wenn Sie Configuration Manager zum Verwalten Ihrer Speicher Vorlagen für UE-V-Einstellungen verwenden, erstellen Sie die Vorlage-Baseline-CAB neu, importieren Sie Sie in Configuration Manager, und stellen Sie dann den Basisplan für Ihre Clients bereit. Weitere Informationen finden Sie in den Anleitungen in der Dokumentation zum [System Center 2012-Konfigurationspaket für Microsoft User Experience Virtualization 2](https://go.microsoft.com/fwlink/?LinkId=317263).






 

 





