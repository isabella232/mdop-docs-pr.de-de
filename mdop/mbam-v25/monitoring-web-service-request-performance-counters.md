---
title: Überwachen von Leistungszählern für Webdienstanforderungen
description: Überwachen von Leistungszählern für Webdienstanforderungen
author: dansimp
ms.assetid: bdb812a1-465a-4098-b4c0-cb99890d1b0d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 2db96e3375562b48d289ea5a21dc7e89b800d1ad
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810219"
---
# Überwachen von Leistungszählern für Webdienstanforderungen


Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) stellt Leistungsindikatoren bereit, die die Leistung von Anforderungen aufzeichnen, die an die folgenden Webdienste gesendet werden:

-   **StatusReportingService. svc** – Dienst, der Anforderungen für den Konformitätsstatus erhält

-   **CoreService. svc** – Dienst, der Anforderungen für Schlüssel Wiederherstellungsversuche empfängt

## Von MBAM bereitgestellten Leistungsindikatoren


MBAM stellt die folgenden Leistungsindikatoren für jede der öffentlichen Methoden bereit, die von ihren StatusReportingService-und CoreService-Webdiensten implementiert werden:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Typ des Leistungsindikators</th>
<th align="left">Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Gesamtzahl der Anforderungen</p></td>
<td align="left"><p>Stellt eine Inkrementierung bereit, die beim Starten oder Neustarten des Servers bei Null beginnt.</p>
<p>Bietet eine Gesamtübersicht über die Systemaktivität. Kann mithilfe automatisierter Tools überwacht werden, um die Integrität des Servers zu gewährleisten und zu überprüfen, ob der Zähler kontinuierlich über einen bestimmten Zeitraum inkrementiert wird.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Anforderungen pro Sekunde</p></td>
<td align="left"><p>Gibt den aktuellen Durchsatz des MBAM-Servers an, da er die MBAM-Clientbasis unterstützt.</p>
<p>Ermöglicht Websiteadministratoren Folgendes:</p>
<ul>
<li><p>Berechnen Sie die durchschnittliche Anzahl der Anforderungen pro Sekunde, basierend auf der Anzahl der MBAM-Clients und deren Häufigkeit der Berichterstellung.</p></li>
<li><p>Überprüfen Sie, ob die Anzahl der Anforderungen pro Sekunde in großem Umfang mit der berechneten durchschnittlichen Anzahl von Anforderungen pro Sekunde korreliert. Eine erhebliche Abweichung kann darauf hindeuten, dass der MBAM-Client nicht auf einem Prozentsatz der Clientbasis installiert ist oder dass ein MBAM-Gruppenrichtlinienobjekt nicht erfolgreich bereitgestellt wurde.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>Anforderungsdauer</p></td>
<td align="left"><p>Zeichnet die Dauer von Anforderungen in Millisekunden auf.</p>
<p>Obwohl dieser Leistungsindikator mit der Dauer jeder Anforderung aktualisiert wird, wird er von der Windows-Leistungsüberwachung nur in regelmäßigen Abständen (normalerweise in jeder Sekunde) angezeigt, sodass Sie möglicherweise eine gewisse Variabilität des Werts sehen. Aus diesem Grund sollten Sie die Verwendung des durch den System Monitor angezeigten Mittelwerts in Frage stellen.</p></td>
</tr>
</tbody>
</table>

 

## Ergebnisse und Empfehlungen zu Leistungsindikatoren


Wenn Sie neue MBAM-Clients zu einem MBAM-Server mit Reservekapazität hinzufügen, erwarten Sie, dass die Anzahl der Anfragen pro Sekunde steigt. Dieser Anstieg ist proportional zur Anzahl der neuen Clientcomputer. Die durchschnittliche Anforderungsdauer bleibt relativ statisch. Wenn der Server seine maximale Kapazität erreicht, werden die Anforderungen pro Sekunde gestartet, um sich zu verkleinern, und die durchschnittliche Anforderungsdauer wird länger.

Wenn Sie Bedenken haben, ob Ihre MBAM-Server Ihre Clientbasis unterstützen können, sollten Sie die Bereitstellung von MBAM in Phasen in verschiedenen Sammlungen von Clientcomputern in Betracht gezogen. Wenn Sie MBAM für jede Sammlung von Clientcomputern bereitstellen, empfehlen wir, Snapshots der Leistungsindikatoren zu erstellen, um die relativen Auswirkungen der Bereitstellung auf jede neue Clientsammlung zu erkennen. Wenn sich die Anzahl der Anforderungen pro Sekunde abhebt und die durchschnittliche Anforderungsdauer zunimmt, sollten Sie die MBAM-Server Infrastruktur erweitern, indem Sie eine der folgenden Aktionen ausführen:

-   Verschieben der MBAM-Datenbank auf einen dedizierten Microsoft SQL Server-oder SQL Server-Cluster

-   Lastenausgleichs MBAM auf mehreren IIS-Webservern (Internet Informationsdienste)

-   Bereitstellen von MBAM auf einer leistungsfähigeren Server Hardware

## Anzeigen von Leistungsindikatoren


Das empfohlene Tool für die Anzeige von MBAM-Leistungsindikatoren ist der Windows-System Monitor, der im Lieferumfang von Windows enthalten ist. Wenn Sie Windows PowerShell verwenden, müssen Sie die Leistungsindikatoren nicht aktivieren, bevor Sie Sie anzeigen können, da Sie automatisch vom Windows PowerShell **enable-WebApplication-** Cmdlet registriert werden.

Ausführliche Anweisungen zum Anzeigen von Leistungsindikatoren finden Sie unter [Anzeigen von MBAM-Leistungsindikatoren](https://go.microsoft.com/fwlink/?LinkId=393457).



## Verwandte Themen


[Verwalten von MBAM 2.5](maintaining-mbam-25.md)

 

 


## Sie haben einen Vorschlag für MBAM?
- [Hier](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)können Sie Vorschläge hinzufügen oder abstimmen. 
- Bei MBAM-Problemen verwenden Sie das [MBAM TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).


