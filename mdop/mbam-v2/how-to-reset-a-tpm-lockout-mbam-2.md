---
title: So setzen Sie eine TPM-Sperre zurück
description: So setzen Sie eine TPM-Sperre zurück
author: dansimp
ms.assetid: 20719ab2-18ae-4d3b-989a-539341909816
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6453473ec09c2033346c7e464c08dbfdfe046d47
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810924"
---
# So setzen Sie eine TPM-Sperre zurück


Das Feature für die Wiederherstellung verschlüsselter Laufwerke in Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) umfasst sowohl die Erfassung und Speicherung von Daten als auch die Verfügbarkeit für Tools, die für die Verwaltung des Trusted Platform Module (TPM) erforderlich sind. In diesem Thema wird erläutert, wie Sie auf der Website "Verwaltung und Überwachung" auf das System für die zentrale Schlüsselwiederherstellung zugreifen können, das eine TPM-Besitzerkennwort-Datei bereitstellen kann, wenn eine Computer-ID und eine zugeordnete Benutzerkennung bereitgestellt werden.

Eine TPM-Sperrung kann auftreten, wenn ein Benutzer die falsche PIN zu oft eingibt. Gibt an, wie oft ein Benutzer eine falsche PIN eingeben kann, bevor die TPM-Sperren von Hersteller zu Hersteller variieren.

Sie können eine TPM-Sperrung nur zurücksetzen, wenn MBAM das TPM besitzt.

**So setzen Sie eine TPM-Sperrung zurück**

1.  Öffnen Sie einen Webbrowser, und navigieren Sie zur Websiteverwaltung und Überwachung.

2.  Wählen Sie im linken Navigationsbereich **TPM verwalten** aus, um die Seite **TPM verwalten** zu öffnen.

3.  Geben Sie den vollqualifizierten Domänennamen für den Computer und den Computernamen ein, und geben Sie die Windows-Anmeldedomäne des Benutzers und den Benutzernamen des Benutzers ein, um die TPM-Besitzerkennwort-Datei abzurufen.

4.  Wählen Sie aus der Liste **Grund für das Anfordern einer TPM-Besitzerkennwort-Datei** einen Grund für die Anforderung aus, und klicken Sie auf **Absenden**.

    MBAM gibt eine der folgenden Optionen zurück:

    -   Eine Fehlermeldung, wenn keine übereinstimmende TPM-Besitzerkennwort-Datei gefunden wurde

    -   Die TPM-Besitzerkennwort-Datei für den übermittelten Computer

    **Hinweis:**  
    Wenn Sie ein erweiterter Helpdesk-Benutzer sind, sind die Felder Benutzerdomäne und Benutzer-ID nicht erforderlich.



~~~
After the TPM owner password is retrieved, the owner password is displayed.
~~~

5. Wenn Sie das Kennwort in einer TPM-Datei speichern möchten, klicken Sie auf die Schaltfläche **Speichern** .

   Der Benutzer führt die TPM-Verwaltungskonsole aus, wählt die Option **TPM-Sperrung zurücksetzen** aus, und stellt die TPM-Besitzerkennwort-Datei bereit, um die TPM-Sperrung zurückzusetzen.

   **Wichtig**  
   Helpdesk-Administratoren sollten Endbenutzern den TPM-Hashwert oder die TPM-Besitzerkennwort-Datei nicht zuweisen. Die TPM-Informationen werden nicht geändert, daher kann es ein Sicherheitsrisiko darstellen, wenn die Datei an Endbenutzer übergeben wird.



## Verwandte Themen


[Verwalten von BitLocker mit MBAM](performing-bitlocker-management-with-mbam-mbam-2.md)









