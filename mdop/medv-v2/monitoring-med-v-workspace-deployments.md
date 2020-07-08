---
title: Überwachen von MED-V Workspace-Bereitstellungen
description: Überwachen von MED-V Workspace-Bereitstellungen
author: dansimp
ms.assetid: 5de0cb06-b8a9-48a5-b8b3-836954295765
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6ec4c7c85326e7945aa3d61b7f96872afe24fe37
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812220"
---
# Überwachen von MED-V Workspace-Bereitstellungen


Mit dem Überwachungsfeature in Microsoft Enterprise Desktop Virtualization (Med-v) 2,0 können Sie Abfragen für einzelne Med-v-Arbeitsbereiche ausführen, um zu ermitteln, ob das erstmalige Setup im gesamten Unternehmen erfolgreich war, nachdem die Med-v-Arbeitsbereiche bereitgestellt wurden. Das Überwachen des Erfolgs der erstmaligen Einrichtung ist wichtig, da sich MED-V erst dann in einem brauchbaren Zustand befindet, wenn die erstmalige Einrichtung erfolgreich abgeschlossen wurde.

Dieser Abschnitt enthält Informationen und Anleitungen, die Ihnen bei der Überwachung des Erfolgs oder des Fehlers bei der erstmaligen Einrichtung helfen.

## So überwachen Sie MED-V-Arbeitsbereichs Bereitstellungen


Das Überwachungsfeature besteht aus einem gekoppelten in-Process-WMI-Anbieter (Windows Management Instrumentation), den Sie mithilfe der WMI-Abfragesprache Abfragen können, um den Status der erstmaligen Einrichtung für alle Endbenutzer in einem MED-V-Arbeitsbereich zu ermitteln.

Der WMI-Anbieter wird mithilfe des WMI-Anbieter Erweiterungs Frameworks von Microsoft .NET Framework 3,5 implementiert. Der WMI-Anbieter wird im Kontext von LocalService ausgeführt und speichert den erstmaligen Setup Status sicher unter \\ProgramData.

Der WMI-Anbieter wird im **root\\microsoft\\medv** -Namespace implementiert und implementiert die Klasse **FTS \ _Status**, die die Methode **SetFtsState**verfügbar macht. MED-V verwendet **SetFtsState** zum Einrichten des erstmaligen Setup Zustands.

Die Klasse enthält die folgenden Eigenschaften.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Eigenschaft</th>
<th align="left">Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Computer</strong></p></td>
<td align="left"><p><strong>Schreibgeschützte </strong> Eigenschaft, die den Namen des virtuellen Gastcomputers enthält, der beim erstmaligen Einrichten bereitgestellt wird. Dieser Schlüssel enthält den Namen, den der Gast beim erstmaligen Setup-Fehler gehabt hätte.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Statuscode</strong></p></td>
<td align="left"><p><strong>Schreibgeschützte </strong> Eigenschaft, die NULL enthält, wenn die erstmalige Einrichtung erfolgreich war. Jeder andere zurückgegebene Wert entspricht der Ereignis-ID des protokollierten Fehlers.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Zeit</strong></p></td>
<td align="left"><p>Die UTC-Zeit, die das erstmalige Einrichten abgeschlossen hat.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Benutzer</strong></p></td>
<td align="left"><p>Der Benutzer, für den die erstmalige Einrichtung ausgeführt wurde.</p></td>
</tr>
</tbody>
</table>

 

Der folgende Code zeigt die MOF-Datei (Managed Object Format), die die **FTS \ _Status** Klasse definiert.

``` syntax
[dynamic: ToInstance, provider("MedvWmi, Version=2.0.258.0, Culture=neutral, PublicKeyToken=14986c3f172d1c2c")]
class FTS_Status
{
[read, key] string User;
[read] string Machine;
[read] sint32 StatusCode;
[read] datetime Time;
[static, implemented] void SetFtsState([in] sint32 statusCode, [in] string machine);
};
```

Da es in erster Linie um die MED-V-Arbeitsbereiche geht, bei denen die erstmalige Einrichtung nicht erfolgreich abgeschlossen wurde, können Sie Ihre Abfrage so schreiben, dass nur die Fehler zurückgegeben werden, die bei der erstmaligen Einrichtung fehlgeschlagen sind, beispielsweise:

``` syntax
Select * from FTS_Status where StatusCode != 0
```

In diesem Fall gibt das Überwachungsfeature eine Liste der MED-V-Arbeitsbereiche zurück, bei denen die erstmalige Einrichtung fehlgeschlagen ist, die Sie verwenden können, um den Fehler durch geeignete Aktionen zu beheben.

## Verwandte Themen


[Überwachen von MED-V-Arbeitsbereichen](monitor-med-v-workspaces.md)

[So überprüfen Sie erstmalige Einstellungen für das Setup](how-to-verify-first-time-setup-settings.md)

 

 





