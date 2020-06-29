---
title: So setzen Sie eine TPM-Sperre zurück
description: So setzen Sie eine TPM-Sperre zurück
author: dansimp
ms.assetid: dd20a728-c52e-48e6-9f6c-1311c71dee74
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f5aea277e80c54fb01d1a6c00b62f0c617d1ad12
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809886"
---
# So setzen Sie eine TPM-Sperre zurück


In diesem Thema wird erläutert, wie Sie die Website "Verwaltung und Überwachung" (auch als "Helpdesk" bezeichnet) verwenden, um eine TPM-Sperrung zurückzusetzen. TPM-Sperrungen können auftreten, wenn ein Endbenutzer die falsche PIN zu oft eingibt. Gibt an, wie oft ein Benutzer eine falsche PIN eingeben kann, bevor die TPM-Sperren von Hersteller zu Hersteller variieren.

Im Bereich " **TPM verwalten** " auf der Website "Verwaltung und Überwachung" können Sie auf das Datensystem für die zentrale Schlüsselwiederherstellung zugreifen, das eine TPM-Besitzerkennwort-Datei bereitstellt, wenn Sie eine Computer-ID und eine zugehörige Benutzer-ID angeben.

Für den Zugriff auf den Bereich TPM Verwalten der Verwaltungs-und Überwachungs Website müssen Sie der Rolle MBAM Helpdesk-Benutzer oder der MBAM Advanced Helpdesk-Benutzerrolle zugewiesen sein. Diese Rollen sind Gruppen, die Administratoren in Active Directory erstellen. Sie können einen beliebigen Namen für diese Gruppen verwenden. Weitere Informationen finden Sie unter [Planen von MBAM 2,5-Gruppen und-Konten](planning-for-mbam-25-groups-and-accounts.md#bkmk-helpdesk-roles).

Informationen zu MBAM und TPM-Besitz finden Sie unter [MBAM 2,5-Sicherheitsüberlegungen](mbam-25-security-considerations.md#bkmk-tpm).

**So setzen Sie eine TPM-Sperrung zurück**

1.  Öffnen Sie einen Webbrowser, und navigieren Sie zur **Website Verwaltung und Überwachung**.

2.  Klicken Sie im linken Bereich auf **TPM verwalten** , um die Seite **TPM verwalten** zu öffnen.

3.  Geben Sie den vollqualifizierten Domänennamen für den Computer und den Computernamen ein.

4.  Geben Sie die Windows-Anmeldedomäne des Endbenutzers und den Benutzernamen ein, um die TPM-Besitzerkennwort-Datei abzurufen.

    **Hinweis**  Wenn Sie sich in der Gruppe erweiterte Helpdesk-Benutzer von MBAM befinden, sind die Felder Benutzerdomäne und Benutzer-ID nicht erforderlich.

     

5.  Wählen Sie aus der Liste **Grund für das Anfordern einer TPM-Besitzerkennwort-Datei** einen Grund für die Anforderung aus, und klicken Sie auf **Absenden**.

    MBAM gibt eine der folgenden Optionen zurück:

    -   Eine Fehlermeldung, wenn keine übereinstimmende TPM-Besitzerkennwort-Datei gefunden wurde

    -   Die TPM-Besitzerkennwort-Datei für den übermittelten Computer

    Nachdem das TPM-Besitzerkennwort abgerufen wurde, wird das Besitzerkennwort angezeigt.

6.  Wenn Sie das Kennwort in einer TPM-Datei speichern möchten, klicken Sie auf die Schaltfläche **Speichern** .

7.  Wählen Sie im Bereich **TPM verwalten** auf der **Website Verwaltung und Überwachung**die Option **TPM-Sperrung zurücksetzen** aus, und geben Sie die TPM-Besitzerkennwort-Datei an.

    Die TPM-Sperrung wird zurückgesetzt, und der Zugriff des Endbenutzers wird wiederhergestellt.

    **Wichtig**  Übergeben Sie die TPM-Hashwerte oder die TPM-Besitzerkennwort-Datei nicht an Endbenutzer. Da sich die TPM-Informationen nicht ändern, stellt die Datei Endbenutzern ein Sicherheitsrisiko dar.

     



## Verwandte Themen


[Durchführen der BitLocker-Verwaltung mit MBAM 2.5](performing-bitlocker-management-with-mbam-25.md)

 

## Sie haben einen Vorschlag für MBAM?
- [Hier](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)können Sie Vorschläge hinzufügen oder abstimmen. 
- Bei MBAM-Problemen verwenden Sie das [MBAM TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





