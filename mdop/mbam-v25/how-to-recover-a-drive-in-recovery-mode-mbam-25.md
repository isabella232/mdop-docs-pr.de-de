---
title: So stellen Sie ein Laufwerk im Wiederherstellungsmodus wieder her
description: So stellen Sie ein Laufwerk im Wiederherstellungsmodus wieder her
author: dansimp
ms.assetid: e126eaf8-9ae7-40fe-a28e-dbd78d26859e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d15f33f461e60fceeed3acbce3a0c82b02b56f98
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809913"
---
# So stellen Sie ein Laufwerk im Wiederherstellungsmodus wieder her


In diesem Thema wird erläutert, wie Sie die Website "Verwaltung und Überwachung" (auch als "Helpdesk" bezeichnet) verwenden, um ein Wiederherstellungskennwort abzurufen, das den Endbenutzern zur Verfügung steht, wenn Ihr mit BitLocker geschütztes Laufwerk in den Wiederherstellungsmodus wechselt. Laufwerke gehen in den Wiederherstellungsmodus, wenn Benutzer Ihre PIN oder Ihr Kennwort verlieren oder vergessen oder wenn der TPM-Chip (Trusted Module Platform) Änderungen an den BIOS-oder Startdateien eines Computers erkennt.

Verwenden Sie zum Abrufen eines Wiederherstellungskennworts den Bereich **Drive Recovery** der Verwaltungs-und Überwachungs Website. Sie müssen der MBAM Helpdesk-Benutzerrolle oder der MBAM Advanced Helpdesk-Benutzerrolle zugewiesen sein, um auf diesen Bereich der Website zugreifen zu können.

**Hinweis:**  
Sie haben diesen Rollen möglicherweise unterschiedliche Namen gegeben, als Sie Sie erstellt haben. Weitere Informationen finden Sie unter [Planen von MBAM 2,5-Gruppen und-Konten](planning-for-mbam-25-groups-and-accounts.md#bkmk-helpdesk-roles).



**Wichtig**  
Wiederherstellungskennwörter verfallen nach einer einmaligen Verwendung. Auf Betriebssystemlaufwerken und festen Datenlaufwerken wird die Regel für einmalige Verwendung automatisch angewendet. Auf Wechseldatenträgern wird Sie angewendet, wenn das Laufwerk entfernt und dann auf einem Computer, auf dem die Gruppenrichtlinieneinstellungen aktiviert sind, um Wechseldatenträger zu verwalten, erneut eingefügt und wieder freigegeben wird.



**So stellen Sie ein Laufwerk im Wiederherstellungsmodus wieder her**

1.  Öffnen Sie einen Webbrowser, und navigieren Sie zur **Website Verwaltung und Überwachung**.

2.  Wählen Sie im linken Bereich **Drive Recovery** aus, um die Seite **Wiederherstellen des Zugriffs auf eine verschlüsselte Festplatte** zu öffnen.

3.  Geben Sie die Windows-Anmeldedomäne und den Benutzernamen des Endbenutzers ein, um Wiederherstellungsinformationen anzuzeigen.

    **Hinweis:**  
    Wenn Sie sich in der Gruppe erweiterte Helpdesk-Benutzer von MBAM befinden, sind die Felder Benutzerdomäne und Benutzer-ID nicht erforderlich.



4.  Geben Sie die ersten acht Ziffern der Wiederherstellungsschlüssel-ID ein, um eine Liste möglicher übereinstimmender Wiederherstellungsschlüssel anzuzeigen, oder geben Sie die gesamte Wiederherstellungsschlüssel-ID ein, um den genauen Wiederherstellungsschlüssel abzurufen.

5.  Wählen Sie in der Liste **Grund für Laufwerks Sperrung** eine der vordefinierten Optionen aus, und klicken Sie dann auf **Absenden**.

    MBAM gibt Folgendes zurück:

    -   Eine Fehlermeldung, wenn kein passendes Wiederherstellungskennwort gefunden wurde

    -   Mehrere mögliche Übereinstimmungen, wenn der Benutzer über mehrere übereinstimmende Wiederherstellungskennwörter verfügt

    -   Das Wiederherstellungskennwort und das Wiederherstellungs Paket für den übermittelten Benutzer

        **Hinweis:**  
        Wenn Sie ein beschädigtes Laufwerk wiederherstellen, bietet BitLocker mit der Option "Wiederherstellungs Paket" wichtige Informationen, die für die Wiederherstellung des Laufwerks erforderlich sind.



~~~
After the recovery password and recovery package are retrieved, the recovery password is displayed.
~~~

6. Wenn Sie das Kennwort kopieren möchten, klicken Sie auf **Schlüssel kopieren**, und fügen Sie dann das Wiederherstellungskennwort in eine e-Mail-Nachricht ein. Klicken Sie alternativ auf **Speichern** , um das Wiederherstellungskennwort in einer Datei zu speichern.

   Wenn der Benutzer das Wiederherstellungskennwort in das System eingibt oder das Wiederherstellungs Paket verwendet, wird das Laufwerk entsperrt.



## Verwandte Themen


[Durchführen der BitLocker-Verwaltung mit MBAM 2.5](performing-bitlocker-management-with-mbam-25.md)



## Sie haben einen Vorschlag für MBAM?
- [Hier](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)können Sie Vorschläge hinzufügen oder abstimmen. 
- Bei MBAM-Problemen verwenden Sie das [MBAM TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





