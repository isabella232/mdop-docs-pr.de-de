---
title: Ändern der Häufigkeit von geplanten UE-V-Aufgaben
description: Ändern der Häufigkeit von geplanten UE-V-Aufgaben
author: dansimp
ms.assetid: 33c2674e-0df4-4717-9c3d-820a90b16e19
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: ced608608ffae82a29fb5ca84cfca281082b8127
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809505"
---
# Ändern der Häufigkeit von geplanten UE-V-Aufgaben


Der Microsoft User Experience Virtualization (UE-v)-Agent-Installationsprogramm, AgentSetup.exe, erstellt zwei geplante Aufgaben während der Installation des UE-v-Agents. Bei den beiden Aufgaben handelt es sich um den Aufgabenbereich " **automatische Aktualisierungs Vorlage** " und die Einstellung "Speicherort **Status** ". Diese geplanten Aufgaben können mit den UE-V-Tools nicht konfiguriert werden. Administratoren, die die geplante Aufgabe für diese Elemente ändern möchten, können ein Skript erstellen, das die Schtasks.exe Befehlszeilenoptionen verwendet.

Weitere Informationen zu Schtasks.exe finden Sie unter [so wird es gemacht: Verwenden von schtasks, exe zum Planen von Aufgaben in Windows Server 2003](https://go.microsoft.com/fwlink/?LinkID=264854).

## Automatische Aktualisierung der Vorlage


Mit dem **automatischen Aktualisierungs** Vorgang der Vorlage wird der Einstellungs Vorlagenkatalog auf neue, aktualisierte oder entfernte Vorlagen überprüft. Diese Aufgabe wird nur ausgeführt, wenn die SettingsTemplateCatalog konfiguriert ist. Der Task " **Automatische Aktualisierung der Vorlage** " führt die ApplySettingsCatalog.exe-Datei aus, die sich im Installationsverzeichnis des UE-V-Agents befindet.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Aufgabenname</th>
<th align="left">Standardauslöser</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>\Microsoft\UE-V\Template Auto Update</p></td>
<td align="left"><p>3:30 Uhr pro Tag</p></td>
</tr>
</tbody>
</table>

 

**Beispiel:** Mit dem folgenden Befehl wird der Agent so konfiguriert, dass der Katalog Speicher für Einstellungs Vorlagen stündlich überprüft wird.

``` syntax
schtasks /change /tn "Microsoft\UE-V\Template Auto Update" /ri 60
```

## Status des Speicherorts für Einstellungen


Die Aufgabe **Speicherorts Status festlegen** führt die folgenden Aktionen aus:

1.  Überprüft, ob die UE-V-Ordner noch mit dem Feature Offlinedateien angeheftet oder registriert sind.

2.  Überprüft, ob der Speicherort für Einstellungen offline oder Online ist.

3.  Erzwingt eine Synchronisierung für das angegebene Intervall anstelle des Standardintervalls für Offlinedateien.

4.  Synchronisiert alle Einstellungs Pakete, die so konfiguriert sind, dass Sie vorab abgerufen werden.

5.  Überprüft, ob sich der Pfad des Active Directory-Basisverzeichnisses geändert hat.

6.  Schreibt die Speicherkonfiguration für aktuelle Einstellungen unter dem folgenden Speicherort

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Aufgabenname</th>
    <th align="left">Standardauslöser</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Status des \Microsoft\UE-V\Settings-Speicherorts</p></td>
    <td align="left"><p>Bei der Anmeldung eines beliebigen Benutzers – nach dem auslösen, wiederholen Sie alle 30 Minuten auf unbestimmte Zeit.</p></td>
    </tr>
    </tbody>
    </table>

     

**Beispiel:** Mit dem folgenden Befehl wird der Agent so konfiguriert, dass die Aktion über stündlich ausgeführt wird.

``` syntax
schtasks /change /tn "\Microsoft\UE-V\Settings Storage Location Status" /ri 60
```

## Verwandte Themen


[Verwalten von UE-V 1.0](administering-ue-v-10.md)

[Vorgänge für UE-V 1.0](operations-for-ue-v-10.md)

 

 





