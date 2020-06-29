---
title: So konfigurieren Sie das Verhalten von Verknüpfungen und Dateitypzuordnungen
description: So konfigurieren Sie das Verhalten von Verknüpfungen und Dateitypzuordnungen
author: dansimp
ms.assetid: d6fd1728-4de6-4066-b36b-d4837d593d40
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 84e3e0cdd43cfc26cf56f1b5ac72560b1c702ae6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807296"
---
# So konfigurieren Sie das Verhalten von Verknüpfungen und Dateitypzuordnungen


Die Veröffentlichungsrichtlinie für die Verknüpfungs-und Dateitypzuordnung (FTA) wird von der Veröffentlichungs-XML-Datei definiert und gesteuert, die von einem Veröffentlichungsserver während eines Veröffentlichungs Aktualisierungsvorgangs an Clients gesendet wird. Wenn der Client diese Informationen erhält, werden alle neu veröffentlichten Daten zu Anwendungen wie den Symbolen und Freihandelsabkommen hinzugefügt. Anschließend werden alle veralteten Veröffentlichungsdaten entfernt.

In App-V Version 4,6 wurden zwei Registrierungsschlüsselwerte definiert, damit Administratoren dieses Verhalten steuern können. Standardmäßig werden Tastenkombinationen, die lokal mithilfe der Clientkonsole erstellt werden, nun beibehalten.

## So ändern Sie das Verhalten von Tastenkombinationen und FTA


Für den Registrierungsschlüssel "Clientkonfiguration", "FileTypePolicy" und "ShortcutPolicy", wurden zwei neue DWORD-Registrierungswerte definiert. Diese DWORD-Registrierungswerte sind standardmäßig nicht vorhanden, können aber manuell hinzugefügt werden. Der Registrierungsschlüssel für die Konfiguration befindet sich unter HKEY \ _LOCAL \ _MACHINE \\software\\\ [Wow6432Node\\\] Microsoft\\SoftGrid\\4.5\\Client\\Configuration.

Es gibt vier Richtlinienwerte, die in der folgenden Tabelle definiert sind, und diese gelten für beide Registrierungsschlüsselwerte. Die folgende Liste zeigt die numerischen Werte für die Registrierungseinstellungen und das Verhalten, das auf Dateitypen oder Tastenkombinationen bei einem Veröffentlichungs Aktualisierungsvorgang angewendet wurde.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p>Name</p></td>
<td align="left"><p>Typ</p></td>
<td align="left"><p>Daten (Beispiele)</p></td>
<td align="left"><p>Beschreibung</p></td>
</tr>
<tr class="even">
<td align="left"><p>FileTypePolicy</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Standard = 0x2 (App-V 4,6)</p></td>
<td align="left"><p>(0x0) – "ClientOnly" – entfernen Sie alle vorhandenen Elemente aus derselben Veröffentlichungs Informationsquelle, und behalten Sie nur Elemente bei, die lokal hinzugefügt werden.</p>
<p>(0x1) – "ServerOnly" – entfernen Sie alle veralteten Elemente aus derselben Veröffentlichungs Informationsquelle sowie alle Elemente, die lokal hinzugefügt wurden, und fügen Sie die neuen Elemente hinzu.</p>
<p>(0x2) – "ClientAndServer" – entfernen Sie alle veralteten Elemente aus derselben Veröffentlichungs Informationsquelle, halten Sie die Elemente lokal hinzugefügt, und fügen Sie die neuen Elemente hinzu (Standard, wenn Sie für App-V 4,6 nicht vorhanden sind).</p>
<p>(0x3) – "NoChange" – nehmen Sie keine Änderungen an Dateitypen oder Tastenkombinationen vor.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>ShortcutPolicy</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Standard = 0x2</p></td>
<td align="left"><p>(0x0) – "ClientOnly" – entfernen Sie alle vorhandenen Elemente aus derselben Veröffentlichungs Informationsquelle, und behalten Sie nur lokal hinzugefügte Elemente bei.</p>
<p>(0x1) – "ServerOnly" – entfernen Sie alle veralteten Elemente aus derselben Veröffentlichungs Informationsquelle und alle Elemente, die lokal hinzugefügt wurden, und fügen Sie die neuen Elemente hinzu.</p>
<p>(0x2) – "ClientAndServer" – entfernt alle veralteten Elemente aus derselben Veröffentlichungs Informationsquelle, behält Elemente lokal hinzu und fügt die neuen Elemente hinzu (Standard, wenn nicht vorhanden).</p>
<p>(0x3) – "NoChange" – nehmen Sie keine Änderungen an Dateitypen oder Tastenkombinationen vor.</p></td>
</tr>
</tbody>
</table>

 

**Hinweis**  Die Textwerte beziehen sich auf die Werte für die XML-Attribute in der Veröffentlichungs-XML-Datei.Sie können diese Werte manuell einstellen, wenn Sie eine benutzerdefinierte HTTP-Veröffentlichungslösung implementiert haben.

 

 

 





