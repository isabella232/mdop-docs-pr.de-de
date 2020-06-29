---
title: So setzen Sie eine TPM-Sperre zurück
description: So setzen Sie eine TPM-Sperre zurück
author: dansimp
ms.assetid: 91ec6666-1ae2-4e76-9459-ad65c405f639
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: dde77a12e97d050777dac15d4106124ec111b3cd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804589"
---
# So setzen Sie eine TPM-Sperre zurück


Das Feature für die Wiederherstellung verschlüsselter Laufwerke in Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) umfasst sowohl die Erfassung und Speicherung von Daten als auch die Verfügbarkeit für Tools, die für die Verwaltung des Trusted Platform Module (TPM) erforderlich sind. In diesem Thema wird erläutert, wie Sie auf das Datensystem für die zentralisierte Schlüsselwiederherstellung auf der Website "Bit \ _admmon \ _tlanextref Administration" zugreifen. Das Schlüssel Wiederherstellungsdaten System kann eine TPM-Besitzerkennwort-Datei bereitstellen, wenn die Computeridentität und die zugehörige Benutzer-ID bereitgestellt werden.

Eine TPM-Sperrung kann auftreten, wenn ein Benutzer zu oft eine falsche PIN eingibt. Gibt an, wie oft ein Benutzer eine falsche PIN eingeben kann, bevor die TPM-Sperrung auf der Spezifikation des Computerherstellers basiert.

**So setzen Sie eine TPM-Sperrung zurück**

1.  Öffnen Sie die MBAM-Verwaltungswebsite.

2.  Wählen Sie im Navigationsbereich **TPM verwalten**aus. Dadurch wird die Seite **TPM verwalten** geöffnet.

3.  Geben Sie den vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) für den Computer und den Computernamen ein. Geben Sie die Windows-Anmeldedomäne des Benutzers und den Benutzernamen des Benutzers ein. Wählen Sie eine der vordefinierten Optionen im Dropdownmenü " **Grund für das Anfordern der TPM-Besitzer Kennwortdatei** " aus. Klicken Sie auf **Übermitteln**.

4.  MBAM gibt eine der folgenden Optionen zurück:

    -   Eine Fehlermeldung, wenn keine übereinstimmende TPM-Besitzerkennwort-Datei gefunden wurde

    -   Die TPM-Besitzerkennwort-Datei für den übermittelten Computer

    **Hinweis**  Wenn Sie ein erweiterter Helpdesk-Benutzer sind, sind die Felder Benutzerdomäne und Benutzer-ID nicht erforderlich.

     

5.  Beim Abrufen wird das Kennwort des Besitzers angezeigt. Wenn Sie dieses Kennwort in einer TPM-Datei speichern möchten, klicken Sie auf die Schaltfläche **Speichern** .

6.  Der Benutzer führt die TPM-Verwaltungskonsole aus und wählt die TPM- **Sperrungs Option Zurücksetzen** aus, und stellt die TPM-Besitzerkennwort-Datei bereit, um die TPM-Sperrung zurückzusetzen.

## Verwandte Themen


[Verwalten von BitLocker mit MBAM](performing-bitlocker-management-with-mbam.md)

 

 





