---
title: Verwalten von MBAM 1.0-Funktionen
description: Verwalten von MBAM 1.0-Funktionen
author: dansimp
ms.assetid: dd9a9eff-f1ad-4af3-85d9-c19131a4ad22
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a99ac556227c0f113fb20f3aca32d21c204877b0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808626"
---
# Verwalten von MBAM 1.0-Funktionen


Nachdem Sie alle erforderlichen MBAM-Planung und-Bereitstellung (Microsoft BitLocker-Verwaltung und-Überwachung) abgeschlossen haben, können Sie MBAM konfigurieren und verwenden, um die BitLocker-Unternehmens-Verschlüsselung zu verwalten. Die Informationen in diesem Abschnitt beschreiben die täglichen Aufgaben der MBAM-funktionsvorgänge nach der Installation.

## Verwalten von MBAM-Administrator Rollen


Nachdem das MBAM-Setup für alle Server Features abgeschlossen ist, müssen Administrator Benutzern Zugriff auf diese Server Features gewährt werden. Als bewährte Methode sollten Administratoren, die die MBAM-Server Features verwalten oder verwenden, Active Directory-Sicherheitsgruppen zugewiesen werden, und diese Gruppen sollten der entsprechenden administrativen lokalen Gruppe MBAM hinzugefügt werden.

[So verwalten Sie MBAM-Administratorrollen](how-to-manage-mbam-administrator-roles-mbam-1.md)

## Verwalten der Hardware Kompatibilität


Das MBAM-Hardware Kompatibilitätsfeature kann Ihnen dabei helfen, sicherzustellen, dass nur die von Ihnen als unterstützende BitLocker angegebene Computer Hardware verschlüsselt wird. Wenn dieses Feature aktiviert ist, werden in Bit \ _admmontla nur Computer verschlüsselt, die als kompatibel gekennzeichnet sind.

**Wichtig**  Wenn dieses Feature deaktiviert ist, werden alle Computer, auf denen die MBAM-Richtlinie bereitgestellt wird, verschlüsselt.

 

MBAM kann Informationen über die Marke und das Modell von Clientcomputern sammeln, wenn Sie die Gruppenrichtlinie "Hardware Kompatibilitätsüberprüfung zulassen" bereitstellen. Wenn Sie diese Richtlinie konfigurieren, meldet der MBAM-Agent dem MBAM-Server die Informationen zum Erstellen und modellieren des Computers, wenn der MBAM-Client auf einem Clientcomputer bereitgestellt wird.

[So verwalten Sie Hardwarekompatibilität](how-to-manage-hardware-compatibility-mbam-1.md)

[So verwalten Sie BitLocker-Verschlüsselungsausnahmen für Benutzer](how-to-manage-user-bitlocker-encryption-exemptions-mbam-1.md)

## Verwalten von BitLocker-Verschlüsselungs Ausnahmen


MBAM kann zwei Arten von Ausnahmen von der BitLocker-Verschlüsselung gewähren: Computer Befreiung und Benutzer Befreiung. Die Computer Befreiung wird in der Regel verwendet, wenn ein Unternehmen über Computer verfügt, die nicht verschlüsselt werden müssen, beispielsweise Computer, die in Entwicklungs-oder Testversionen verwendet werden, oder ältere Computer, die BitLocker nicht unterstützen. In einigen Fällen kann die örtliche Gesetzgebung auch verlangen, dass bestimmte Computer nicht verschlüsselt sind. Sie können auch festlegen, dass Benutzer, die Ihre Laufwerke nicht benötigen oder verschlüsselt werden sollen, davon ausgenommen werden.

[So verwalten Sie BitLocker-Verschlüsselungsausnahmen für Computer](how-to-manage-computer-bitlocker-encryption-exemptions.md)

## Verwalten von MBAM-Client-BitLocker-Verschlüsselungsoptionen mithilfe der Systemsteuerung


Wenn Sie über ein Gruppenrichtlinienobjekt (Group Policy Objects, GPO) aktiviert ist, wird unter **System und Sicherheit**ein benutzerdefiniertes MBAM-Control Panel mit dem Namen BitLocker-Verschlüsselungsoptionen zur Verfügung stehen. Dieses angepasste Control Panel ersetzt die standardmäßige Windows BitLocker-Systemsteuerung. Das MBAM Control Panel ermöglicht Ihnen, verschlüsselte Laufwerke (behoben und abnehmbar) zu entsperren, und hilft Ihnen auch bei der Verwaltung Ihrer PIN oder Ihres Kennworts.

[So verwalten Sie BitLocker-Verschlüsselungsoptionen für MBAM-Clients mithilfe der Systemsteuerung](how-to-manage-mbam-client-bitlocker-encryption-options-by-using-the-control-panel-mbam-1.md)

## Weitere Ressourcen für die Verwaltung von MBAM-Features


[Vorgänge für MBAM 1.0](operations-for-mbam-10.md)

 

 





