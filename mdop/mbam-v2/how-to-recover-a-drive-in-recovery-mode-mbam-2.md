---
title: So stellen Sie ein Laufwerk im Wiederherstellungsmodus wieder her
description: So stellen Sie ein Laufwerk im Wiederherstellungsmodus wieder her
author: dansimp
ms.assetid: 8b792bc8-b671-4345-9d37-0208db3e5b03
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7d5ce509599d0eb800a71360e3be9d0fa3b33f4f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810927"
---
# So stellen Sie ein Laufwerk im Wiederherstellungsmodus wieder her


Die verschlüsselten Laufwerk Wiederherstellungsfeatures von Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) gewährleisten die Erfassung und Speicherung von Daten und die Verfügbarkeit von Tools für den Zugriff auf ein BitLocker-geschütztes Volume, wenn BitLocker in den Wiederherstellungsmodus wechselt. Ein von BitLocker geschütztes Volume wechselt in den Wiederherstellungsmodus, wenn eine PIN oder ein Kennwort verloren geht oder vergessen wird oder wenn der TPM-Chip (Trusted Module Platform) Änderungen an den BIOS-oder Startdateien eines Computers erkennt.

Gehen Sie wie folgt vor, um auf das Datensystem für die zentralisierte Schlüsselwiederherstellung zuzugreifen, das ein Wiederherstellungskennwort bereitstellen kann, wenn eine Wiederherstellungskennwort-ID und die zugehörige Benutzerkennung angegeben werden

**Wichtig**  
Die Microsoft BitLocker-Verwaltung und-Überwachung verwendet Wiederherstellungsschlüssel zur einmaligen Verwendung, die bei der Verwendung ablaufen. Die einmalige Verwendung eines Wiederherstellungskennworts wird automatisch auf Betriebssystemlaufwerke und Festplatten angewendet. Auf Wechseldatenträgern wird Sie angewendet, wenn das Laufwerk entfernt und dann auf einem Computer, auf dem die Gruppenrichtlinieneinstellungen aktiviert sind, um Wechseldatenträger zu verwalten, erneut eingefügt und wieder freigegeben wird.



**So stellen Sie ein Laufwerk im Wiederherstellungsmodus wieder her**

1.  Öffnen Sie einen Webbrowser, und navigieren Sie zur Websiteverwaltung und Überwachung.

2.  Klicken Sie im Navigationsbereich auf **Laufwerk Wiederherstellung**. Die Webseite "Zugriff auf verschlüsselte Laufwerke wiederherstellen" wird geöffnet.

3.  Geben Sie die Windows-Anmeldedomäne und den Benutzernamen des Benutzers ein, um die Wiederherstellungsinformationen und die ersten acht Ziffern der Wiederherstellungsschlüssel-ID anzuzeigen, um eine Liste der möglichen übereinstimmenden Wiederherstellungsschlüssel oder der gesamten Wiederherstellungsschlüssel-ID zu erhalten, um den genauen Wiederherstellungs

4.  Wählen Sie eine der vordefinierten Optionen aus der Liste **Grund für Laufwerks Sperrung** aus, und klicken Sie dann auf **Absenden**.

    **Hinweis:**  
    Wenn Sie ein MBAM Advanced Helpdesk-Nutzer sind, sind die Benutzerdomänen-und Benutzer-ID-Einträge nicht erforderlich.



~~~
MBAM returns the following:

-   An error message if no matching recovery password is found

-   Multiple possible matches if the user has multiple matching recovery passwords

-   The recovery password and recovery package for the submitted user

    **Note**  
    If you are recovering a damaged drive, the recovery package option provides BitLocker with critical information that it needs to recover the drive.



After the recovery password and recovery package are retrieved, the recovery password is displayed.
~~~

5. Wenn Sie das Kennwort kopieren möchten, klicken Sie auf **Schlüssel kopieren**, und fügen Sie dann das Wiederherstellungskennwort in eine e-Mail-Nachricht ein. Klicken Sie alternativ auf **Speichern** , um das Wiederherstellungskennwort in einer Datei zu speichern.

   Wenn der Benutzer das Wiederherstellungskennwort in das System eingibt oder das Wiederherstellungs Paket verwendet, wird das Laufwerk entsperrt.

## Verwandte Themen


[Verwalten von BitLocker mit MBAM](performing-bitlocker-management-with-mbam-mbam-2.md)









