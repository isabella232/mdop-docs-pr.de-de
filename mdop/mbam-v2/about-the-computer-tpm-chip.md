---
title: Informationen zum TPM-Chip des Computers
description: Informationen zum TPM-Chip des Computers
author: dansimp
ms.assetid: 6f1cf18c-277a-4932-886d-14202ca8d175
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f6df54dc8085c398bacc508fdbbb79a30b0e4204
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810012"
---
# Informationen zum TPM-Chip des Computers


BitLocker bietet zusätzlichen Schutz, wenn es mit einem TPM-Chip (Trusted Platform Module) verwendet wird. Der TPM-Chip ist eine Hardwarekomponente, die von den Computerherstellern auf vielen neueren Computern installiert wird. Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) verwendet BitLocker zusätzlich zum TPM-Chip, um zusätzlichen Schutz Ihrer Daten zu gewährleisten und sicherzustellen, dass Ihr Computer nicht manipuliert wurde.

## Einrichten Ihres TPMs


Wenn Sie den BitLocker-Laufwerk Verschlüsselungs-Assistenten auf Ihrem Computer starten, überprüft BitLocker nach einem TPM-Chip, wenn Ihre Organisation BitLocker für die Verwendung eines TPM-Chips konfiguriert hat. Wenn BitLocker einen kompatiblen TPM-Chip findet, werden Sie möglicherweise aufgefordert, Ihren Computer neu zu starten, um den TPM-Chip zur Verwendung zu aktivieren. Sobald Ihr Computer neu gestartet wurde, folgen Sie den Anweisungen, um den TPM-Chip im BIOS zu konfigurieren (das BIOS ist eine Pre-Windows-Schicht ihrer Computer Software).

Nachdem BitLocker konfiguriert wurde, können Sie auf zusätzliche Informationen zum TPM-Chip zugreifen, indem Sie das Tool BitLocker-Verschlüsselungsoptionen in der Windows-Systemsteuerung öffnen und dann die **TPM-Verwaltung**auswählen.

**Hinweis**  Sie müssen über Administratorrechte auf dem Computer verfügen, um auf dieses Tool zugreifen zu können.

 

Bei einem TPM-Fehler, einer Änderung im BIOS oder bestimmten Windows-Updates sperrt BitLocker Ihren Computer und fordert Sie auf, sich an Ihren Helpdesk zu wenden, um ihn zu entsperren. Sie müssen den Namen Ihres Computers und die Domäne Ihres Computers angeben. Der Helpdesk kann Ihnen eine Kennwort-Datei zur Verfügung stellen, mit der Sie Ihren Computer entsperren können.

## Behandeln von Problemen mit TPM


Wenn ein TPM-Fehler, eine Änderung im BIOS oder bestimmte Windows-Updates auftreten, sperrt BitLocker Ihren Computer und fordert Sie auf, sich an Ihren Helpdesk zu wenden, um ihn zu entsperren. Sie müssen den Namen Ihres Computers und die Domäne Ihres Computers angeben. Der Helpdesk kann Ihnen eine Kennwortdatei zur Verfügung stellen, die Sie zum Entsperren Ihres Computers verwenden können.

## Verwandte Themen


[Unterstützung für Endbenutzer beim Verwalten von BitLocker](helping-end-users-manage-bitlocker.md)

[Verwenden Ihrer PIN oder Ihres Kennworts](using-your-pin-or-password.md)

 

 





