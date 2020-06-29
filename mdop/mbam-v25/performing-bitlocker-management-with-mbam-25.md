---
title: Durchführen der BitLocker-Verwaltung mit MBAM 2.5
description: Durchführen der BitLocker-Verwaltung mit MBAM 2.5
author: dansimp
ms.assetid: 068f3ee0-300c-4083-ba18-7065eef997ad
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1a0ee5802f945176914c56659e0ff7e34e93a969
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811497"
---
# Durchführen der BitLocker-Verwaltung mit MBAM 2.5


Nachdem Sie die Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) geplant und dann bereitgestellt haben, können Sie Sie konfigurieren und verwenden, um die BitLocker-Laufwerkverschlüsselung in Ihrem Unternehmen zu verwalten. Die Informationen in diesem Abschnitt beschreiben die nach der Installation täglichen BitLocker-Verschlüsselungs Verwaltungsaufgaben, die mithilfe der Microsoft BitLocker-Verwaltung und-Überwachung ausgeführt werden.

## Zurücksetzen einer TPM-Sperrung


Bei einem Trusted Platform Module (TPM) handelt es sich um einen Mikrochip, der grundlegende sicherheitsrelevante Funktionen bereitstellen soll, in erster Linie mit Verschlüsselungsschlüsseln. Das TPM wird normalerweise auf der Hauptplatine eines Computers installiert, und es kommuniziert mit dem restlichen System mithilfe eines Host-Bus-Adapters. Auf Computern, auf denen ein TPM integriert ist, können Sie kryptografische Schlüssel erstellen und verschlüsseln, sodass Sie nur vom TPM entschlüsselt werden können.

Eine TPM-Sperrung kann auftreten, wenn ein Benutzer die falsche PIN zu oft eingibt. Gibt an, wie oft ein Benutzer eine falsche PIN eingeben kann, bevor die TPM-Sperren je nach Hersteller variieren. Sie können MBAM verwenden, um auf der Website Verwaltung und Überwachung auf das Datensystem für die zentrale Schlüsselwiederherstellung zuzugreifen, in dem Sie eine TPM-Besitzerkennwort-Datei abrufen können, wenn Sie eine Computer-ID und eine zugeordnete Benutzerkennung angeben.

[So setzen Sie eine TPM-Sperre zurück](how-to-reset-a-tpm-lockout-mbam-25.md)

## Wiederherstellen von Laufwerken


Bei der Verschlüsselung von Daten insbesondere in einer Unternehmensumgebung sollten Sie berücksichtigen, wie diese Daten bei einem Hardwarefehler, personellen Änderungen oder anderen Situationen, in denen Verschlüsselungsschlüssel verloren gehen können, wiederhergestellt werden können.

Die verschlüsselten Laufwerk Wiederherstellungsfeatures in MBAM stellen sicher, dass Daten erfasst und gespeichert werden können und dass die erforderlichen Tools für den Zugriff auf ein von BitLocker geschütztes Volume verfügbar sind, wenn BitLocker in den Wiederherstellungsmodus wechselt, verschoben wird oder beschädigt wird.

[So stellen Sie ein Laufwerk im Wiederherstellungsmodus wieder her](how-to-recover-a-drive-in-recovery-mode-mbam-25.md)

[So stellen Sie ein verschobenes Laufwerk wieder her](how-to-recover-a-moved-drive-mbam-25.md)

[So stellen Sie ein beschädigtes Laufwerk wieder her](how-to-recover-a-corrupted-drive-mbam-25.md)

## Ermitteln des BitLocker-Verschlüsselungsstatus von verlorenen Computern


Mithilfe von MBAM können Sie den letzten bekannten BitLocker-Verschlüsselungsstatus von verloren gegangenen oder gestohlenen Computern ermitteln.

[So ermitteln Sie den BitLocker-Verschlüsselungsstatus verloren gegangener Computer](how-to-determine-bitlocker-encryption-state-of-lost-computers-mbam-25.md)

## Verwenden des Self-Service-Portals zum wieder Zugriff auf einen Computer


Wenn Endbenutzer von BitLocker von Windows ausgeschlossen werden, können Sie die Anweisungen in diesem Abschnitt verwenden, um einen BitLocker-Wiederherstellungsschlüssel abzurufen, um wieder Zugriff auf Ihren Computer zu erhalten.

[So verwenden Sie das Self-Service-Portal, um wieder auf einen Computer zugreifen zu können](how-to-use-the-self-service-portal-to-regain-access-to-a-computer-mbam-25.md)



## Verwandte Themen


[Vorgänge für MBAM 2.5](operations-for-mbam-25.md)

 

## Sie haben einen Vorschlag für MBAM?
- [Hier](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)können Sie Vorschläge hinzufügen oder abstimmen. 
- Bei MBAM-Problemen verwenden Sie das [MBAM TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





