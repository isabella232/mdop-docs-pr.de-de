---
title: So konfigurieren Sie die Clientprotokolldatei
description: So konfigurieren Sie die Clientprotokolldatei
author: dansimp
ms.assetid: dd79f8ce-61e2-4dc8-af03-2a353554a1b2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 729089d683c5d102eb7eb45314583023d3362639
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807251"
---
# So konfigurieren Sie die Clientprotokolldatei


Sie können die folgenden Verfahren zum Konfigurieren der Application Virtualization (App-V)-Client Protokolldatei verwenden.

**So ändern Sie den Speicherort der Protokolldatei**

-   Bearbeiten Sie den folgenden Registrierungsschlüsselwert, um den neuen Pfad für die Protokolldatei anzugeben. Nachdem Sie diesen Wert geändert haben, müssen Sie den **sftlist** -Dienst erneut starten. Dieser Speicherort kann auch nach der Installation interaktiv geändert werden.

    HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\softgrid\\4.5\\client\\configuration\\logfilename

**So ändern Sie die Protokoll Berichterstattungs Ebene**

-   Standardmäßig enthalten die in das Protokoll geschriebenen Nachrichtentypen alle Ereignisse des Schweregrads 4 (Information) oder höher. Der Schweregrad wird im folgenden Schlüsselwert gespeichert. Setzen Sie diesen Schlüsselwert auf 5, um die ausführliche Protokollierung zu aktivieren. Verwenden Sie die ausführliche Protokollierung nur für kurze Zeiträume während der Problembehandlung, da Sie eine sehr große Anzahl von Nachrichten generiert und dazu führt, dass das Protokoll schnell gefüllt wird.

    HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\softgrid\\4.5\\client\\configuration\\logminseverity

**So ändern Sie die Protokollgröße**

-   In Application Virtualization (App-V) 4,5 wird die Protokollgröße durch den folgenden Registrierungsschlüsselwert gesteuert. Dieser Wert ist standardmäßig 256MB und definiert die maximale Größe in MB, auf die das Protokoll anwachsen kann, bevor es zurückgesetzt wird.

    HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\softgrid\\4.5\\client\\configuration\\logmaxsize

    **Vorsicht**  Dieser Registrierungsschlüsselwert muss auf einen Wert größer als 0 (null) gesetzt werden, um sicherzustellen, dass die Protokolldatei zurückgesetzt wird.

     

**So ändern Sie die Anzahl von Sicherungskopien**

-   Wenn die Protokolldatei die maximale Größe erreicht, wird ein Reset erzwungen, wenn der nächste Schreibvorgang in das Protokoll erfolgt. Bei einem Reset wird eine neue Protokolldatei erstellt, und die alte Datei wird als Sicherung umbenannt. Mit der folgenden Registrierungseinstellung wird die Anzahl von Sicherungskopien der Protokolldatei gesteuert, die beim Zurücksetzen der Datei aufbewahrt werden. Der Standardwert ist 4.

    HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\softgrid\\4.5\\client\\configuration\\logrollovercount

    Das Format der Namen der Sicherungsprotokolldatei lautet: **sftlog\_YYYYMMDD\_hhmmss-uuu.txt** und basiert auf der Zeit zum Zurücksetzen, in UTC (Universal Coordinated Time). In der folgenden Tabelle sind die beim Erstellen der Dateinamen und deren Beschreibungen verwendeten Symbole aufgeführt.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Symbol</th>
    <th align="left">Beschreibung</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>JJJJ</p></td>
    <td align="left"><p>vierstellige Jahreszahl</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>MM</p></td>
    <td align="left"><p>zweistelliger Monat (01 – 12)</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>DD</p></td>
    <td align="left"><p>zweistelliger Tag des Monats (01 – 31)</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>hh</p></td>
    <td align="left"><p>Stunde (00 – 23)</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>mm</p></td>
    <td align="left"><p>Minuten (00 – 59)</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>ss</p></td>
    <td align="left"><p>Sekunden (00 – 59)</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>uuu</p></td>
    <td align="left"><p>Millisekunden (000 – 999)</p></td>
    </tr>
    </tbody>
    </table>

     

## Verwandte Themen


[So konfigurieren Sie die App-V-Client-Registrierungseinstellungen über die Befehlszeile](how-to-configure-the-app-v-client-registry-settings-by-using-the-command-line.md)

 

 





