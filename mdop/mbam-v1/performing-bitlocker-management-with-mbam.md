---
title: Verwalten von BitLocker mit MBAM
description: Verwalten von BitLocker mit MBAM
author: dansimp
ms.assetid: 2d24390a-87bf-48b3-96a9-3882d6f2a15c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8d0de3711d5b7c3696783a054ee7c7f8220b5356
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811428"
---
# Verwalten von BitLocker mit MBAM


Nachdem Sie die Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) bereitgestellt haben, können Sie MBAM konfigurieren und verwenden, um die BitLocker-Unternehmens-Verschlüsselung zu verwalten. In diesem Abschnitt werden die nach der Installation täglichen BitLocker-Verschlüsselungs Verwaltungsaufgaben beschrieben, die mithilfe von MBAM ausgeführt werden können.

## Zurücksetzen einer TPM-Sperrung mit MBAM


Ein TPM-Microchip (Trusted Platform Module) bietet grundlegende sicherheitsrelevante Funktionen. Diese Funktionen werden in erster Linie durch die Verwendung von Verschlüsselungsschlüsseln erreicht. Das TPM ist in der Regel auf der Hauptplatine eines Computers oder Laptops installiert und kommuniziert mit dem restlichen System mithilfe eines Hardware Busses. Computer, die ein TPM integrieren, können kryptografische Schlüssel erstellen, die nur vom TPM entschlüsselt werden können. Eine TPM-Sperrung kann auftreten, wenn ein Benutzer zu oft eine falsche PIN eingibt. Gibt an, wie oft ein Benutzer eine falsche PIN eingeben kann, bevor die TPM-Sperren von Hersteller zu Hersteller variieren. Mit dem Schlüssel Wiederherstellungsdaten System auf der MBAM-Verwaltungswebsite können Sie eine TPM-Besitzerkennwort-Datei zurücksetzen.

[So setzen Sie eine TPM-Sperre zurück](how-to-reset-a-tpm-lockout-mbam-1.md)

## Wiederherstellen von Laufwerken mit MBAM


Stellen Sie sicher, dass Sie wissen, wie Sie bei einem Hardwarefehler, personellen Änderungen oder anderen Situationen, in denen Verschlüsselungsschlüssel verloren gehen, Datenwiederherstellung von verschlüsselten Laufwerken versuchen. Die verschlüsselten Laufwerk Wiederherstellungsfeatures von MBAM bieten die Erfassung und Speicherung von Daten und die Verfügbarkeit von Tools, die für den Zugriff auf ein von BitLocker geschütztes Volume erforderlich sind, wenn das Volume in den Wiederherstellungsmodus wechselt, verschoben wird oder beschädigt wird.

[So stellen Sie ein Laufwerk im Wiederherstellungsmodus wieder her](how-to-recover-a-drive-in-recovery-mode-mbam-1.md)

[So stellen Sie ein verschobenes Laufwerk wieder her](how-to-recover-a-moved-drive-mbam-1.md)

[So stellen Sie ein beschädigtes Laufwerk wieder her](how-to-recover-a-corrupted-drive-mbam-1.md)

## Ermitteln des BitLocker-Verschlüsselungsstatus von verlorenen Computern mithilfe von MBAM


Wenn Sie MBAM verwenden, können Sie den letzten bekannten BitLocker-Verschlüsselungsstatus von verloren gegangenen oder gestohlenen Computern ermitteln.

[Wie Sie den BitLocker-Verschlüsselung Zustand von einer nicht mehr auffindbar Computern zu ermitteln](how-to-determine-the-bitlocker-encryption-state-of-a-lost-computers-mbam-1.md)

## Weitere Ressourcen zum Durchführen der BitLocker-Verwaltung mit MBAM


[Vorgänge für MBAM 1.0](operations-for-mbam-10.md)

 

 





