---
title: So stellen Sie ein Laufwerk im Wiederherstellungsmodus wieder her
description: So stellen Sie ein Laufwerk im Wiederherstellungsmodus wieder her
author: dansimp
ms.assetid: 09d27e4b-57fa-47c7-a004-8b876a49f27e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c1151ffe7453eb8d07d2aa6dcb4c41f6b3efe6de
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804613"
---
# So stellen Sie ein Laufwerk im Wiederherstellungsmodus wieder her


Die Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) enthält verschlüsselte Wiederherstellungsfunktionen. Diese Features gewährleisten die Erfassung und Speicherung von Daten und die Verfügbarkeit von Tools, die für den Zugriff auf ein von BitLocker geschütztes Volume erforderlich sind, wenn BitLocker das Volume in den Wiederherstellungsmodus versetzt. Ein von BitLocker geschütztes Volume wechselt in den Wiederherstellungsmodus, wenn eine PIN oder ein Kennwort verloren geht oder vergessen wird oder wenn der TPM-Chip (Trusted Module Platform) eine Änderung an den BIOS-oder Startdateien des Computers erkennt.

Gehen Sie wie folgt vor, um auf das Datensystem für die zentrale Schlüsselwiederherstellung zuzugreifen, das ein Wiederherstellungskennwort bereitstellen kann, wenn eine Wiederherstellungskennwort-ID und die zugehörige Benutzerkennung angegeben

**Wichtig**  MBAM generiert Wiederherstellungsschlüssel zur einmaligen Verwendung. Unter dieser Einschränkung kann ein Wiederherstellungsschlüssel nur einmal verwendet werden und ist dann nicht mehr gültig. Die einmalige Verwendung eines Wiederherstellungskennworts wird automatisch auf Betriebssystemlaufwerke und Festplatten angewendet. Auf Wechseldatenträgern wird die einmalige Verwendung angewendet, wenn das Laufwerk entfernt und dann auf einem Computer, auf dem die Gruppenrichtlinieneinstellungen aktiviert sind, um Wechseldatenträger zu verwalten, erneut eingefügt und wieder freigegeben wird.

 

**So stellen Sie ein Laufwerk im Wiederherstellungsmodus wieder her**

1.  Öffnen Sie die MBAM-Website.

2.  Klicken Sie im Navigationsbereich auf **Laufwerk Wiederherstellung**. Die Webseite **Wiederherstellen des Zugriffs auf eine verschlüsselte Festplatte** wird geöffnet.

3.  Geben Sie die Windows-Anmeldedomäne des Benutzers und den Benutzernamen sowie die ersten acht Ziffern der Wiederherstellungsschlüssel-ID ein, um eine Liste der möglichen übereinstimmenden Wiederherstellungsschlüssel zu erhalten. Sie können auch die gesamte Wiederherstellungsschlüssel-ID eingeben, um den genauen Wiederherstellungsschlüssel zu erhalten. Wählen Sie eine der vordefinierten Optionen in der Dropdownliste **Grund für Laufwerks Sperrung** aus, und klicken Sie dann auf **Absenden**.

    **Hinweis**  Wenn Sie ein MBAM Advanced Helpdesk-Nutzer sind, sind die Benutzerdomänen-und Benutzer-ID-Einträge nicht erforderlich.

     

4.  MBAM gibt Folgendes zurück:

    1.  Eine Fehlermeldung, wenn kein passendes Wiederherstellungskennwort gefunden wurde

    2.  Mehrere mögliche Übereinstimmungen, wenn der Benutzer über mehrere übereinstimmende Wiederherstellungskennwörter verfügt

    3.  Das Wiederherstellungskennwort und das Wiederherstellungs Paket für den übermittelten Benutzer

        **Hinweis**  Wenn Sie ein beschädigtes Laufwerk wiederherstellen, bietet BitLocker mit der Option "Wiederherstellungs Paket" die wichtigen Informationen, die für den Versuch der Wiederherstellung erforderlich sind.

         

5.  Nachdem das Wiederherstellungskennwort und das Wiederherstellungs Paket abgerufen wurden, wird das Wiederherstellungskennwort angezeigt. Wenn Sie das Kennwort kopieren möchten, klicken Sie auf **Schlüssel kopieren**, und fügen Sie dann das Wiederherstellungskennwort in eine e-Mail oder eine andere Textdatei für den temporären Speicher ein. Wenn Sie das Wiederherstellungskennwort in einer Datei speichern möchten, klicken Sie auf **Speichern**.

6.  Wenn der Benutzer das Wiederherstellungskennwort in das System eingibt oder das Wiederherstellungs Paket verwendet, wird das Laufwerk entsperrt.

## Verwandte Themen


[Verwalten von BitLocker mit MBAM](performing-bitlocker-management-with-mbam.md)

 

 





