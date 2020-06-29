---
title: Verwalten von MBAM 2.0-Funktionen
description: Verwalten von MBAM 2.0-Funktionen
author: dansimp
ms.assetid: 065e0704-069e-4372-9b86-0b57dd7638dd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 35bb855e185ad8e3fa6880853938074cf6185a0d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809997"
---
# Verwalten von MBAM 2.0-Funktionen


Nachdem Sie alle erforderlichen Planung abgeschlossen und dann die Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) bereitgestellt haben, können Sie Sie konfigurieren und verwenden, um die BitLocker-Verschlüsselung im gesamten Unternehmen zu verwalten die Informationen in diesem Abschnitt beschreiben die nach der Installation ausgeführten Aufgaben in der Microsoft BitLocker-Verwaltungs-und-Überwachungsfunktion.

## Verwalten von MBAM-Administrator Rollen


Nachdem das MBAM-Setup für alle Server Features abgeschlossen ist, müssen Administrator Benutzern Zugriff darauf gewährt werden. Als bewährte Methode sollten Administratoren, die die MBAM-Server Features verwalten oder verwenden, den Active Directory-Domänendienst-Sicherheitsgruppen zugewiesen werden, und diese Gruppen sollten der entsprechenden administrativen lokalen Gruppe MBAM hinzugefügt werden.

[So verwalten Sie MBAM-Administratorrollen](how-to-manage-mbam-administrator-roles-mbam-2.md)

## Verwalten von BitLocker-Verschlüsselungs Ausnahmen


MBAM ermöglicht es Ihnen, bestimmten Benutzern, die Ihre Laufwerke nicht benötigen oder verschlüsseln möchten, Verschlüsselungs Ausnahmen zu gewähren. Die Computer Befreiung wird in der Regel verwendet, wenn ein Unternehmen über Computer verfügt, die nicht verschlüsselt werden müssen, beispielsweise Computer, die in Entwicklungs-oder Testversionen verwendet werden, oder ältere Computer, die BitLocker nicht unterstützen. In einigen Fällen kann die örtliche Gesetzgebung auch verlangen, dass bestimmte Computer nicht verschlüsselt sind.

[So verwalten Sie BitLocker-Verschlüsselungsausnahmen für Benutzer](how-to-manage-user-bitlocker-encryption-exemptions-mbam-2.md)

## Verwalten von MBAM-Client-BitLocker-Verschlüsselungsoptionen mithilfe der Systemsteuerung


MBAM stellt ein benutzerdefiniertes Control Panel mit dem Namen BitLocker-Verschlüsselungsoptionen bereit, das unter **System und Sicherheit**angezeigt wird. Über das MBAM-Control Panel können verschlüsselte fest-und Wechseldatenträger freigegeben und auch Ihre PIN oder Ihr Kennwort verwaltet werden.

**Hinweis**  Dieses angepasste Control Panel ersetzt nicht die standardmäßige Windows BitLocker-Systemsteuerung.

 

[So verwalten Sie BitLocker-Verschlüsselungsoptionen für MBAM-Clients mithilfe der Systemsteuerung](how-to-manage-mbam-client-bitlocker-encryption-options-by-using-the-control-panel-mbam-2.md)

## Weitere Ressourcen für die Verwaltung von MBAM-Features


[Vorgänge für MBAM 2.0](operations-for-mbam-20-mbam-2.md)

 

 





