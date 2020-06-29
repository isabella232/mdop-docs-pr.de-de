---
title: So führen Sie DaRT-Aufgaben mithilfe von PowerShell-Befehlen durch
description: So führen Sie DaRT-Aufgaben mithilfe von PowerShell-Befehlen durch
author: dansimp
ms.assetid: bc788b00-38c7-4f57-a832-916b68264d89
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f8ff87aa09555b93ca04a6ec7fa5dd4ba8504514
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810474"
---
# So führen Sie DaRT-Aufgaben mithilfe von PowerShell-Befehlen durch


Microsoft Diagnostics and Recovery Toolset (Dart) 8,0 bietet die folgenden aufgelisteten Satz von Windows PowerShell-Cmdlets. Administratoren können diese PowerShell-Cmdlets verwenden, um verschiedene Dart 8,0-Serveraufgaben über die Eingabeaufforderung statt über den Dart-Wiederherstellungsbild-Assistenten auszuführen.

## So verwalten Sie Dart mithilfe von PowerShell-Befehlen


Verwenden Sie die hier beschriebenen PowerShell-Cmdlets, um Dart zu verwalten.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Name</th>
<th align="left">Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Kopieren-DartImage</p></td>
<td align="left"><p>Brennt eine ISO auf eine CD, DVD oder ein USB-Laufwerk.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Export-DartImage</p></td>
<td align="left"><p>Ermöglicht die Konvertierung der Quell-WIM-Datei, die ein DART-Bild enthält, in eine ISO-Datei.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Neu – DartConfiguration</p></td>
<td align="left"><p>Erstellt ein DART-Konfigurationsobjekt, das zum Anwenden eines Dart-Toolsets auf ein Windows-Abbild erforderlich ist.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Satz-DartImage</p></td>
<td align="left"><p>Wendet ein DartConfiguration-Objekt auf ein bereitgestelltes Windows-Abbild an. Dies umfasst das Hinzufügen aller Dateien, Konfigurationen und Paketabhängigkeiten.</p></td>
</tr>
</tbody>
</table>

 

## Verwandte Themen


[Verwalten von DaRT 8.0 mithilfe von PowerShell](administering-dart-80-using-powershell-dart-8.md)

 

 





