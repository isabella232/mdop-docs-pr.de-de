---
title: Wiederherstellen von Anwendungs- und Windows-Einstellungen, die mit UE-V 1.0 synchronisiert sind
description: Wiederherstellen von Anwendungs- und Windows-Einstellungen, die mit UE-V 1.0 synchronisiert sind
author: dansimp
ms.assetid: 254a16b1-f186-44a4-8e22-49a4ee87c734
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 31ae83e0a44f98b66a9930f8c5db2231992a4700
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804181"
---
# Wiederherstellen von Anwendungs- und Windows-Einstellungen, die mit UE-V 1.0 synchronisiert sind


WMI-und PowerShell-Features von Microsoft User Experience Virtualization (UE-V) bieten die Möglichkeit zum Wiederherstellen von Einstellungspaketen. Mit WMI-und PowerShell-Befehlen können Sie die Anwendungs-und Windows-Einstellungen auf die Einstellungswerte zurücksetzen, die sich auf dem Computer befanden, als die Anwendung zum ersten Mal nach der Installation des UE-V-Agents gestartet wurde. Diese Wiederherstellungsaktion wird für einzelne Anwendungs-oder Windows-Einstellungen ausgeführt. Die Einstellungen werden wiederhergestellt, wenn die Anwendung das nächste Mal ausgeführt wird oder wenn sich der Benutzer beim Betriebssystem anmeldet.

**So stellen Sie Anwendungseinstellungen und Windows-Einstellungen mit PowerShell wieder her**

1.  Öffnen Sie das Windows PowerShell-Fenster. Zum Importieren des Microsoft UE-V PowerShell-Moduls geben Sie den folgenden Befehl ein:

    ``` syntax
    Import-module UEV
    ```

2.  Geben Sie das folgende PowerShell-Cmdlet ein, um die Anwendungseinstellungen und Windows-Einstellungen wiederherzustellen.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong>PowerShell-Cmdlet</strong></th>
    <th align="left"><strong>Beschreibung</strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Wiederherstellen – UevUserSetting</p></td>
    <td align="left"><p>Wiederherstellen der Benutzereinstellungen für eine Anwendung oder Wiederherstellen einer Gruppe von Windows-Einstellungen</p></td>
    </tr>
    </tbody>
    </table>

     

**So stellen Sie Anwendungseinstellungen und Windows-Einstellungen mit WMI wieder her**

1.  Öffnen Sie ein PowerShell-Fenster.

2.  Geben Sie den folgenden WMI-Befehl ein, um Anwendungseinstellungen und Windows-Einstellungen wiederherzustellen.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong>WMI-Befehl</strong></th>
    <th align="left"><strong>Beschreibung</strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Invoke-WmiMethod-Namespace root\Microsoft\UEV-Class UserSettings-Name RestoreByTemplateId-argumentlist &lt; template_ID&gt;</p></td>
    <td align="left"><p>Wiederherstellen der Benutzereinstellungen für eine Anwendung oder Wiederherstellen einer Gruppe von Windows-Einstellungen</p></td>
    </tr>
    </tbody>
    </table>

     

## Verwandte Themen


[Verwalten von UE-V 1.0](administering-ue-v-10.md)

[Vorgänge für UE-V 1.0](operations-for-ue-v-10.md)

 

 





