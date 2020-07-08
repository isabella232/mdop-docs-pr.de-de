---
title: Neuigkeiten in AGPM 4.0
description: Neuigkeiten in AGPM 4.0
author: dansimp
ms.assetid: 31775f7f-a59c-4e64-a875-0adc9f5bc835
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 82b4445a7d22fb7c1ef4f42d896f11908a22f2f5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808172"
---
# Neuigkeiten in AGPM 4.0


Microsoft Advanced Group Policy Management (AGPM) 4.0 enthält neue Features, mit denen Sie nach Gruppenrichtlinienobjekten (Group Policy Objects, GPOs) suchen, die Liste der angezeigten GPOs filtern, ein GPO in eine andere Gesamtstruktur exportieren und importieren sowie AGPM auf Computern installieren können, auf denen Windows7 und Windows Server2008R2 ausgeführt werden.

## Suchen und Filtern von GPOs


In AGPM 4,0 können Sie die Liste der GPOs nach bestimmten Attributen durchsuchen, um die Liste der angezeigten GPOs zu filtern. So können Sie beispielsweise nach GPOs mit einem bestimmten Namen, Zustand oder Kommentar suchen. Sie können auch nach GPOs suchen, die zuletzt von einem bestimmten Gruppenrichtlinienadministrator oder an einem bestimmten Datum geändert wurden.

Sie können eine komplexe Suchzeichenfolge erstellen, indem Sie das Gruppenrichtlinien *Objekt-Attribut 1: Suchtext 1 GPO-Attribut 2: Suchtext 2...* verwenden, wobei ein GPO-Attribut eine beliebige Spaltenüberschrift in der Liste der GPOs in AGPM ist. Wenn Sie beispielsweise nach allen GPOs mit Namen suchen möchten, einschließlich des Texts "eigenes", der eingecheckt wurde und zuletzt vom Benutzer Editor03 geändert wurde, geben Sie Folgendes in das Suchfeld ein: **Name: eigenes Zustand:****eingecheckt****geändert von: Editor03**. Die Suche gibt partielle Übereinstimmungen zurück, sodass Sie einen Teil eines GPO-namens oder Benutzernamens eingeben und eine Liste aller GPOs anzeigen können, die diesen Text in seinem Namen enthalten.

Darüber hinaus können Sie die gleichen speziellen Begriffe verwenden, die bei der Suche in Windows für die Suche nach GPOs, die an einem bestimmten Datum oder Datumsbereich geändert wurden, verfügbar sind. Ändern Sie beispielsweise **Datum:****lastmonth** oder **Datum ändern:****thisWeek**.

## Exportieren und Importieren von GPOs in unterschiedliche Gesamtstrukturen


Mithilfe von AGPM 4,0 können Sie ein gesteuertes Gruppenrichtlinienobjekt aus einer Domäne in einer Gesamtstruktur in eine Domäne in einer zweiten Gesamtstruktur kopieren. So können Sie beispielsweise ein GPO aus einer Domäne in einer Gesamtstruktur in eine CAB-Datei exportieren, indem Sie AGPM verwenden, diese CAB-Datei auf ein USB-Laufwerk kopieren, das USB-Laufwerk an einen Computer in einer Domäne in einer zweiten Gesamtstruktur anschließen und das Gruppenrichtlinienobjekt in AGPM in einer Domäne in der zweiten Gesamtstruktur importieren. Sie können das Gruppenrichtlinienobjekt entweder als neues gesteuertes Gruppenrichtlinienobjekt importieren oder es importieren, um die Einstellungen eines vorhandenen Gruppenrichtlinienobjekts zu ersetzen, das ausgecheckt ist.

## Unterstützung für Windows Server 2008 R2 und Windows 7


AGPM 4,0 unterstützt Windows Server2008R2 und Windows7 und unterstützt dennoch Windows Server2008 und Windows Vista® mit Service Pack1 (SP1). Es gibt jedoch Einschränkungen in einer gemischten Umgebung, die sowohl das neuere als auch das ältere Betriebssystem enthält, wie in der folgenden Tabelle angegeben.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Betriebssystem, auf dem AGPM Server 4,0 ausgeführt wird</th>
<th align="left">Betriebssystem, auf dem AGPM-Client 4,0 ausgeführt wird</th>
<th align="left">Status der Unterstützung von AGPM 4,0</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows Server2008R2 oder Windows7</p></td>
<td align="left"><p>Windows Server2008R2 oder Windows7</p></td>
<td align="left"><p>Unterstützt</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008R2 oder Windows7</p></td>
<td align="left"><p>Windows Server2008 oder Windows Vista mit SP1</p></td>
<td align="left"><p>Unterstützt, aber Richtlinieneinstellungen oder Einstellungselemente, die nur in Windows Server2008R2 oder Windows7 vorhanden sind, können nicht bearbeitet werden</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2008 oder Windows Vista mit SP1</p></td>
<td align="left"><p>Windows Server2008R2 oder Windows7</p></td>
<td align="left"><p>Nicht unterstützt</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008 oder Windows Vista mit SP1</p></td>
<td align="left"><p>Windows Server2008 oder Windows Vista mit SP1</p></td>
<td align="left"><p>Unterstützt, aber Richtlinieneinstellungen oder Einstellungselemente, die nur in Windows Server2008R2 oder Windows7 vorhanden sind, können nicht gemeldet oder bearbeitet werden</p></td>
</tr>
</tbody>
</table>

 

 

 





