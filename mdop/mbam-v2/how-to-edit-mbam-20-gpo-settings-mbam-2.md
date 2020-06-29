---
title: So bearbeiten Sie GPO-Einstellungen für MBAM 2.0
description: So bearbeiten Sie GPO-Einstellungen für MBAM 2.0
author: dansimp
ms.assetid: f5ffa93d-b4d2-4317-8a1c-7d2be0264fe3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: aaf7c7aab4baba66513edbfa2489fbe53c97dda8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810345"
---
# So bearbeiten Sie GPO-Einstellungen für MBAM 2.0


Zur erfolgreichen Bereitstellung von Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) müssen Sie zunächst die Gruppenrichtlinien ermitteln, die Sie bei der Implementierung der Microsoft BitLocker-Verwaltung und-Überwachung verwenden werden. Weitere Informationen zu den verschiedenen verfügbaren Richtlinien finden Sie unter [Planen von MBAM 2,0-Gruppenrichtlinienanforderungen](planning-for-mbam-20-group-policy-requirements-mbam-2.md) . Nachdem Sie die Richtlinien festgelegt haben, die Sie verwenden möchten, müssen Sie ein oder mehrere Gruppenrichtlinienobjekte ändern, die die Richtlinieneinstellungen für MBAM enthalten.

Mit den folgenden Schritten können Sie die grundlegenden, empfohlenen GPO-Einstellungen so konfigurieren, dass MBAM die BitLocker-Verschlüsselung für die Clientcomputer Ihrer Organisation verwaltet.

**So bearbeiten Sie MBAM-Client-GPO-Einstellungen**

1.  Stellen Sie auf einem Computer, auf dem MBAM-Gruppenrichtlinienvorlage installiert ist, sicher, dass MBAM-Dienste aktiviert sind.

2.  Wenn Sie die Gruppenrichtlinien-Verwaltungskonsole (GPMC. msc) oder das Advanced Group Policy Management (AGPM)-MDOP-Produkt auf einem Computer verwenden, auf dem die MBAM-Gruppenrichtlinienvorlage installiert ist, wählen Sie **Computerkonfiguration**, **Richtlinien**aus, klicken Sie auf **Administrative Vorlagen**, wählen Sie **Windows-Komponenten**aus, und klicken Sie dann auf **MDOP MBAM (BitLocker-Verwaltung)**.

3.  Bearbeiten Sie die Einstellungen für Gruppenrichtlinienobjekte, die zum Aktivieren von MBAM-Clientdiensten auf Clientcomputern erforderlich sind. Wählen Sie für jede Richtlinie in der folgenden Tabelle die Option **Richtliniengruppe**aus, klicken Sie auf die **Richtlinie**, und konfigurieren Sie dann die **Einstellung**:

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Richtliniengruppe</th>
    <th align="left">Richtlinie</th>
    <th align="left">Einstellung</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Clientverwaltung</p></td>
    <td align="left"><p>Konfigurieren von MBAM-Diensten</p></td>
    <td align="left"><p>Aktiviert. Legen <strong> Sie MBAM-Wiederherstellungs-und Hardware Dienstendpunkt </strong> , und <strong> Wählen Sie BitLocker-Wiederherstellungsinformationen speichern aus </strong> . Setzen <strong> Sie den MBAM-Konformitäts Dienstendpunkt </strong> , und geben Sie die Häufigkeit des Statusberichts in (Minuten) ein.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Betriebs System Laufwerk</p></td>
    <td align="left"><p>Verschlüsselungseinstellungen für das Betriebssystemlaufwerk</p></td>
    <td align="left"><p>Aktiviert. Legen <strong> Sie SELECT Protector für das Betriebssystemlaufwerk fest </strong> . Erforderlich, um Betriebssystemlaufwerks Daten auf dem MBAMKey-Wiederherstellungsserver zu speichern.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Wechsellaufwerk</p></td>
    <td align="left"><p>Steuern der Verwendung von BitLocker auf Wechseldatenträgern</p></td>
    <td align="left"><p>Aktiviert. Erforderlich, wenn MBAM Wechseldatenträger-Daten auf dem MBAM-Schlüssel Wiederherstellungsserver speichert.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Festes Laufwerk</p></td>
    <td align="left"><p>Steuern der Verwendung von BitLocker auf Festplatten</p></td>
    <td align="left"><p>Aktiviert. Erforderlich, wenn MBAM Festplatten-Daten auf dem MBAM-Schlüssel Wiederherstellungsserver speichert.</p>
    <p>Legen <strong> Sie fest, wie BitLocker-geschützte Laufwerke wiederhergestellt </strong> und <strong> Daten Wiederherstellungs-Agent zugelassen werden können </strong> .</p></td>
    </tr>
    </tbody>
    </table>



~~~
**Important**  
Depending on the policies that your organization decides to deploy, you may have to configure additional policies. See [Planning for MBAM 2.0 Group Policy Requirements](planning-for-mbam-20-group-policy-requirements-mbam-2.md) for Group Policy configuration details for all of the available MBAM GPO policy options.
~~~



## Verwandte Themen


[Bereitstellen von Gruppenrichtlinienobjekten für MBAM 2.0](deploying-mbam-20-group-policy-objects-mbam-2.md)









