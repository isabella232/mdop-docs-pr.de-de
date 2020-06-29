---
title: Verwalten von BitLocker mit MBAM
description: Verwalten von BitLocker mit MBAM
author: dansimp
ms.assetid: 9bfc6c67-f12c-4daa-8f08-5884fb47443c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d261ec4fa789cd331209afe1c2f1858d627209a3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811791"
---
# Verwalten von BitLocker mit MBAM


Nachdem Sie die Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) geplant und dann bereitgestellt haben, können Sie diese zum Verwalten der BitLocker-Unternehmens-Verschlüsselung konfigurieren und verwenden. Die Informationen in diesem Abschnitt beschreiben die täglichen Aufgaben der BitLocker-Verschlüsselungs Verwaltung nach der Installation, die mithilfe der Microsoft BitLocker-Verwaltung und-Überwachung ausgeführt werden.

## Zurücksetzen einer TPM-Sperrung mithilfe von MBAM


Bei einem Trusted Platform Module (TPM) handelt es sich um einen Mikrochip, der grundlegende sicherheitsrelevante Funktionen bereitstellen soll, in erster Linie mit Verschlüsselungsschlüsseln. Das TPM wird normalerweise auf der Hauptplatine eines Computers oder Laptops installiert und kommuniziert mit dem restlichen System mithilfe eines Hardware Busses. Computer, die ein TPM integrieren, können kryptografische Schlüssel erstellen und verschlüsseln, damit Sie nur vom TPM entschlüsselt werden können.

Eine TPM-Sperrung kann auftreten, wenn ein Benutzer die falsche PIN zu oft eingibt. Gibt an, wie oft ein Benutzer eine falsche PIN eingeben kann, bevor die TPM-Sperren von Hersteller zu Hersteller variieren. Sie können MBAM verwenden, um auf das Datensystem für die zentralisierte Schlüsselwiederherstellung auf der Websiteverwaltung und Überwachung zuzugreifen, auf der Sie eine TPM-Besitzerkennwort-Datei abrufen können, wenn Sie eine Computer-ID und eine zugeordnete Benutzerkennung angeben.

[So setzen Sie eine TPM-Sperre zurück](how-to-reset-a-tpm-lockout-mbam-2.md)

## Wiederherstellen von Laufwerken mit MBAM


Bei der Verschlüsselung von Daten insbesondere in einer Unternehmensumgebung sollten Sie berücksichtigen, wie diese Daten bei einem Hardwarefehler, personellen Änderungen oder anderen Situationen, in denen Verschlüsselungsschlüssel verloren gehen können, wiederhergestellt werden können.

Die verschlüsselten Laufwerk Wiederherstellungsfeatures von MBAM stellen sicher, dass Daten erfasst und gespeichert werden können und dass die erforderlichen Tools für den Zugriff auf ein von BitLocker geschütztes Volume verfügbar sind, wenn BitLocker in den Wiederherstellungsmodus wechselt, verschoben wird oder beschädigt wird.

[So stellen Sie ein Laufwerk im Wiederherstellungsmodus wieder her](how-to-recover-a-drive-in-recovery-mode-mbam-2.md)

[So stellen Sie ein verschobenes Laufwerk wieder her](how-to-recover-a-moved-drive-mbam-2.md)

[So stellen Sie ein beschädigtes Laufwerk wieder her](how-to-recover-a-corrupted-drive-mbam-2.md)

## Ermitteln des BitLocker-Verschlüsselungsstatus von verlorenen Computern mithilfe von MBAM


Mithilfe von MBAM können Sie den letzten bekannten BitLocker-Verschlüsselungsstatus von verloren gegangenen oder gestohlenen Computern ermitteln.

[So ermitteln Sie den BitLocker-Verschlüsselungsstatus verloren gegangener Computer](how-to-determine-bitlocker-encryption-state-of-lost-computers-mbam-2.md)

## Verwenden des Self-Service-Portals zum wieder Zugriff auf einen Computer


Wenn Endbenutzer von BitLocker von Windows ausgeschlossen werden, können Sie die Anweisungen in diesem Abschnitt verwenden, um einen BitLocker-Wiederherstellungsschlüssel abzurufen, um wieder Zugriff auf Ihren Computer zu erhalten.

[So verwenden Sie das Self-Service-Portal, um wieder auf einen Computer zugreifen zu können](how-to-use-the-self-service-portal-to-regain-access-to-a-computer.md)

## Weitere Ressourcen zum Durchführen der BitLocker-Verwaltung mit MBAM


[Vorgänge für MBAM 2.0](operations-for-mbam-20-mbam-2.md)

 

 





