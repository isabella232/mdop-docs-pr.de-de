---
title: So bearbeiten Sie die GPO-Einstellungen für MBAM 1.0
description: So bearbeiten Sie die GPO-Einstellungen für MBAM 1.0
author: dansimp
ms.assetid: 03d12fbc-4302-43fc-9b38-440607d778a1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 824fbc2fe0d8f2b00c32de177733e4e327cf4d44
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810462"
---
# So bearbeiten Sie die GPO-Einstellungen für MBAM 1.0


Wenn Sie die Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) erfolgreich bereitstellen möchten, müssen Sie zunächst die Gruppenrichtlinien ermitteln, die Sie bei der Implementierung der Microsoft BitLocker-Verwaltung und-Überwachung verwenden werden. Weitere Informationen zu den verschiedenen verfügbaren Richtlinien finden Sie unter [Planen von MBAM 1,0-Gruppenrichtlinienanforderungen](planning-for-mbam-10-group-policy-requirements.md). Nachdem Sie die Richtlinien festgelegt haben, die Sie verwenden möchten, müssen Sie ein oder mehrere Gruppenrichtlinienobjekte, die die MBAM-Richtlinieneinstellungen enthalten, ändern.

In den folgenden Schritten wird beschrieben, wie Sie die Standardeinstellungen für Gruppenrichtlinienobjekte konfigurieren, damit MBAM die BitLocker-Verschlüsselung für die Clientcomputer Ihrer Organisation verwaltet.

**So bearbeiten Sie die Einstellungen für das MBAM-Client-GPO**

1.  Stellen Sie auf einem Computer, auf dem MBAM-Gruppenrichtlinienvorlage installiert ist, sicher, dass MBAM-Dienste aktiviert sind.

2.  Verwenden Sie die Gruppenrichtlinien-Verwaltungskonsole (GPMC. msc) oder das erweiterte MDOP-Produkt für Gruppenrichtlinienverwaltung (AGPM) für diese Aktionen: Wählen Sie **Computer Konfiguration**aus, wählen Sie **Richtlinien**aus, klicken Sie auf **Administrative Vorlagen**, wählen Sie **Windows-Komponenten**aus, und klicken Sie dann auf **MDOP MBAM (BitLocker-Verwaltung)**.

3.  Bearbeiten Sie die Einstellungen für Gruppenrichtlinienobjekte, die zum Aktivieren von MBAM-Clientdiensten auf Clientcomputern erforderlich sind. Wählen Sie für jede Richtlinie in der folgenden Tabelle die Option **Richtliniengruppe**aus, klicken Sie auf die **Richtlinie**, und konfigurieren Sie dann die **Einstellung**.

    Richtliniengruppe

    Richtlinie

    Einstellung

    Clientverwaltung

    Konfigurieren von MBAM-Diensten

    Aktiviert. Legen Sie **MBAM-Wiederherstellungs-und Hardware Dienstendpunkt** , und **Wählen Sie BitLocker-Wiederherstellungsinformationen speichern aus**.

    Setzen Sie den **MBAM-Konformitäts Dienstendpunkt** , und **Geben Sie die Häufigkeit des Statusberichts in (Minuten) ein**.

    Hardware Kompatibilitätsüberprüfung zulassen

    Deaktiviert. Diese Richtlinie ist standardmäßig aktiviert, wird aber für eine grundlegende MBAM-Implementierung nicht benötigt.

    Betriebs System Laufwerk

    Verschlüsselungseinstellungen für das Betriebssystemlaufwerk

    Aktiviert. Legen **Sie SELECT Protector für das Betriebssystemlaufwerk**fest. Dies ist erforderlich, um Betriebssystemlaufwerks Daten auf dem MBAM-Schlüssel Wiederherstellungsserver zu speichern.

    Wechsellaufwerk

    Steuern der Verwendung von BitLocker auf Wechseldatenträgern

    Aktiviert. Diese Vorgehensweise ist erforderlich, wenn MBAM Wechseldatenträger auf dem MBAM-Schlüssel Wiederherstellungsserver speichert.

    Festes Laufwerk

    Steuern der Verwendung von BitLocker auf Festplatten

    Aktiviert. Diese Vorgehensweise ist erforderlich, wenn MBAM Festplatten-Daten auf dem MBAM-Schlüssel Wiederherstellungsserver speichert.

    Legen **Sie fest, wie BitLocker-geschützte Laufwerke wiederhergestellt** und **Daten Wiederherstellungs-Agent zugelassen**werden können.



~~~
**Important**  
Depending on the policies that your organization decides to deploy, you may have to configure additional policies. See [Planning for MBAM 1.0 Group Policy Requirements](planning-for-mbam-10-group-policy-requirements.md) for Group Policy configuration details for all of the available MBAM GPO policy options.
~~~



## Verwandte Themen


[Bereitstellen von Gruppenrichtlinienobjekten für MBAM 1.0](deploying-mbam-10-group-policy-objects.md)









