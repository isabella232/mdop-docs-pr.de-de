---
title: Bearbeiten der Gruppenrichtlinieneinstellungen für MBAM 2.5
description: Bearbeiten der Gruppenrichtlinieneinstellungen für MBAM 2.5
author: dansimp
ms.assetid: a50b6b0c-6818-4419-8447-d0520a533dba
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0f6d180cba6dc721ff7de1607d57f90184303d88
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804346"
---
# Bearbeiten der Gruppenrichtlinieneinstellungen für MBAM 2.5


Zur erfolgreichen Bereitstellung von Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) müssen Sie folgende Aufgaben ausführen:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Aufgabe</th>
<th align="left">Weitere Informationen</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Kopieren Sie die MBAM 2,5-Gruppenrichtlinienvorlagen.</p></td>
<td align="left"><p><a href="copying-the-mbam-25-group-policy-templates.md" data-raw-source="[Copying the MBAM 2.5 Group Policy Templates](copying-the-mbam-25-group-policy-templates.md)">Kopieren die Gruppenrichtlinienvorlagen für MBAM 2.5</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Ermitteln Sie, welche Gruppenrichtlinienobjekte (GPOs) Sie in ihrer MBAM-Implementierung verwenden möchten. Je nach den Anforderungen Ihrer Organisation müssen Sie möglicherweise zusätzliche Gruppenrichtlinieneinstellungen konfigurieren.</p></td>
<td align="left"><p><a href="planning-for-mbam-25-group-policy-requirements.md" data-raw-source="[Planning for MBAM 2.5 Group Policy Requirements](planning-for-mbam-25-group-policy-requirements.md)">Planen von MBAM 2,5-Gruppenrichtlinienanforderungen </a> – enthält Beschreibungen der GPOs</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Festlegen der Gruppenrichtlinieneinstellungen für Ihre Organisation</p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>

 

**Wichtig**  Ändern Sie die Gruppenrichtlinieneinstellungen im **BitLocker Drive Encryption** -Knoten nicht, oder MBAM wird nicht ordnungsgemäß funktionieren. Wenn Sie die Gruppenrichtlinieneinstellungen im MDOP- **MBAM (BitLocker-Verwaltungsknoten)** konfigurieren, konfiguriert MBAM automatisch die **BitLocker-Laufwerk Verschlüsselungs** Einstellungen für Sie.

 

**So bearbeiten Sie die MBAM-Client Gruppenrichtlinieneinstellungen**

1.  Stellen Sie auf einem Computer, auf dem die MBAM-Gruppenrichtlinienvorlagen installiert sind, sicher, dass die MBAM-Dienste aktiviert sind.

2.  Wenn Sie die Gruppenrichtlinien-Verwaltungskonsole (GPMC. msc) oder das Microsoft Advanced Group Policy Management MDOP-Produkt auf einem Computer verwenden, auf dem die MBAM-Gruppenrichtlinienvorlagen installiert sind, wählen Sie **Computer Konfigurations** &gt; **Richtlinien** &gt; **Administrative Vorlagen** &gt; **Windows Components** &gt; **MDOP MBAM (BitLocker-Verwaltung)** aus.

3.  Bearbeiten Sie die Gruppenrichtlinieneinstellungen, die zum Aktivieren von MBAM-Clientdiensten auf Clientcomputern erforderlich sind. Wählen Sie für jede Richtlinie in der folgenden Tabelle **Richtliniengruppe**aus, klicken Sie auf die gewünschte **Richt** Linie, und konfigurieren Sie dann die Einstellungen.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Richtliniengruppe</th>
    <th align="left">Richtlinie</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Clientverwaltung</p></td>
    <td align="left"><p>Konfigurieren von MBAM-Diensten</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Betriebs System Laufwerk</p></td>
    <td align="left"><p>Verschlüsselungseinstellungen für das Betriebssystemlaufwerk</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Wechsellaufwerk</p></td>
    <td align="left"><p>Steuern der Verwendung von BitLocker auf Wechseldatenträgern</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Festes Laufwerk</p></td>
    <td align="left"><p>Steuern der Verwendung von BitLocker auf Festplatten</p></td>
    </tr>
    </tbody>
    </table>

     

## Verwandte Themen


[Planen der Gruppenrichtlinienanforderungen für MBAM 2.5](planning-for-mbam-25-group-policy-requirements.md)

[Kopieren die Gruppenrichtlinienvorlagen für MBAM 2.5](copying-the-mbam-25-group-policy-templates.md)

 
## Sie haben einen Vorschlag für MBAM?
- [Hier](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)können Sie Vorschläge hinzufügen oder abstimmen. 
- Bei MBAM-Problemen verwenden Sie das [MBAM TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).
 





