---
title: Befehlszeilenoptionen für MED-V-Installationsdateien
description: Befehlszeilenoptionen für MED-V-Installationsdateien
author: dansimp
ms.assetid: 7b8cd3e4-1d09-44a0-b690-f85b0d0a6b02
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 39582a592a59a4d0e81ef406edc6a984497275c7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811773"
---
# Befehlszeilenoptionen für MED-V-Installationsdateien


Wenn Sie Microsoft Enterprise Desktop Virtualization (MED-V) 2,0 installieren oder deinstallieren, haben Sie die Möglichkeit, die Installationsdateien an der Eingabeaufforderung auszuführen. In diesem Abschnitt werden verschiedene Optionen beschrieben, die Sie bei der Installation oder Deinstallation von MED-V an der Eingabeaufforderung angeben können.

### Befehlszeilenargumente

Sie können die folgenden Befehlszeilenargumente zusammen mit den jeweiligen MED-V-Installationsdateien verwenden.

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
<th align="left">Installationsdatei</th>
<th align="left">Argument</th>
<th align="left">Akzeptierte Werte</th>
<th align="left">Typ</th>
<th align="left">Beschreibung</th>
<th align="left">Standard</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Host-Agent</p></td>
<td align="left"><p>MEDVDIR</p></td>
<td align="left"><p>&lt;Installationspfad&gt;</p></td>
<td align="left"><p>Installation</p></td>
<td align="left"><p>Installiertes Verzeichnis ändern</p></td>
<td align="left"><p>Die Installation wechselt zu Programme\Microsoft Enterprise Desktop Virtualization.</p></td>
</tr>
<tr class="even">
<td align="left"><p>MED-V-Arbeitsbereichs Paket</p></td>
<td align="left"><p>MEDVDIR</p></td>
<td align="left"><p>&lt;Installationspfad&gt;</p></td>
<td align="left"><p>Installation</p></td>
<td align="left"><p>Installiertes Verzeichnis ändern</p></td>
<td align="left"><p>Die Installation wechselt zu Programme\Microsoft Enterprise Desktop Virtualization.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>MED-V-Arbeitsbereich</p></td>
<td align="left"><p>INSTALLDIR</p></td>
<td align="left"><p>&lt;Installationspfad&gt;</p></td>
<td align="left"><p>Installation</p></td>
<td align="left"><p>Installiertes Verzeichnis ändern</p></td>
<td align="left"><p>Die Installation geht zu ProgramData\Microsoft\Medv\Workspace.</p></td>
</tr>
<tr class="even">
<td align="left"><p>MED-V-Arbeitsbereich</p></td>
<td align="left"><p>VHD überschreiben</p></td>
<td align="left"><p>0 oder 1</p></td>
<td align="left"><p>Installation</p></td>
<td align="left"><p>Fehler bei der Installation, wenn VHD vorhanden ist (0) oder vorhandene VHD überschrieben wird (1).</p></td>
<td align="left"><p>Overwrite tritt nicht auf, und die Installation schlägt fehl, wenn bereits eine virtuelle Festplatte (VHD) vorhanden ist.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>MED-V-Arbeitsbereich</p></td>
<td align="left"><p>SUPPRESSMEDVLAUNCH</p></td>
<td align="left"><p>0 oder 1</p></td>
<td align="left"><p>Installation</p></td>
<td align="left"><p>Starten Sie (0) oder starten Sie (1) med-v nach der Installation von Med-v Workspace nicht.</p></td>
<td align="left"><p>Wenn der Med-v-Arbeitsbereich mit der Benutzeroberfläche (UI) installiert wurde, steuert ein Kontrollkästchen auf der <strong> Seite fertig stellen, </strong> ob Med-v gestartet werden soll.</p></td>
</tr>
<tr class="even">
<td align="left"><p>MED-V-Arbeitsbereich</p></td>
<td align="left"><p>DELETEDIFFDISKS</p></td>
<td align="left"><p>0 oder 1</p></td>
<td align="left"><p>Deinstallation</p></td>
<td align="left"><p>Von MED-V erstellte virtuelle Festplatten beibehalten (0) oder löschen (1)</p></td>
<td align="left"><p>Keine virtuellen Festplatten werden gelöscht.</p></td>
</tr>
</tbody>
</table>

 

### Beispiele für Befehlszeilenargumente

Im folgenden Beispiel wird der vom Med-v Workspace-Paketer erstellte Med-v-Arbeitsbereich installiert. Die Installationsdatei erstellt eine Protokolldatei im temporären Verzeichnis und führt die Installationsdatei im stillen Modus aus, startet aber den MED-V-Host-Agent nicht nach Abschluss. Die Installationsdatei überschreibt alle VHD-Dateien, die von einer vorherigen Installation mit demselben Namen zurückgelassen wurden.

``` syntax
setup.exe /l* %temp%\medv-workspace-install.log /qn SUPPRESSMEDVLAUNCH=1 OVERWRITEVHD=1
```

Im folgenden Beispiel wird der zuvor installierte MED-V-Arbeitsbereich deinstalliert. Die Installationsdatei erstellt eine Protokolldatei im temporären Verzeichnis und führt die Installationsdatei im stillen Modus aus. Die Installationsdatei löscht alle verbleibenden virtuellen Festplattendateien aus dem Dateisystem.

``` syntax
%ProgramData%\Microsoft\Medv\Workspace\uninstall.exe /l* %temp%\medv-workspace-uninstall.log /qn DELETEDIFFDISKS=1
```

## Verwandte Themen


[Bereitstellen der MED-V-Komponenten](deploy-the-med-v-components.md)

[Technische Referenz für MED-V](technical-reference-for-med-v.md)

 

 





