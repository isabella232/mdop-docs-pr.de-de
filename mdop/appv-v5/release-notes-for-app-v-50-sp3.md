---
title: Versionshinweise für App-V 5.0 SP3
description: Versionshinweise für App-V 5.0 SP3
author: dansimp
ms.assetid: bc4806e0-2aba-4c7b-9ecc-1b2cc54af1d0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5b6d5834e4d0c953365f955922403c1a7a2058b1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804892"
---
# Versionshinweise für App-V 5.0 SP3


Im folgenden sind bekannte Probleme in Microsoft Application Virtualization (App-V) 5,0 SP3 zu finden.

## Server Dateien können nach einer neuen App-V 5,0 SP3-Server Installation nicht gelöscht werden


Wenn Sie den App-v 5,0 SP1-Server deinstallieren und dann den App-v 5,0 SP3-Server installieren, schlägt die Installation fehl, und die falsche Version des Verwaltungsservers ist installiert. Die folgenden Fehler werden angezeigt:

`[0A5C:06F8][2014-09-12T19:08:00]i102: Detected related bundle: {bee44f0f-05be-48e4-81dd-d34a83600b95}, type: Upgrade, scope: PerMachine, version: 5.0.1218.0, operation: MajorUpgrade``[0A5C:06F8][2014-09-12T19:08:00]i000: AppvUX: A previous version of this product is installed; requesting upgrade.``[0A5C:06F8][2014-09-12T19:08:00]i102: Detected related bundle: {e1ca9d65-0ebf-4fd5-98e5-00d6453967a4}, type: Upgrade, scope: PerMachine, version: 5.0.1224.0, operation: MajorUpgrade``[0A5C:06F8][2014-09-12T19:08:00]i000: AppvUX: A previous version of this product is installed; requesting upgrade.`

Das Problem tritt auf, weil die Server Dateien nicht gelöscht werden, wenn Sie App-v 5,0 SP1 deinstallieren, sodass der Installationsvorgang für die APP-v 5,0 SP3 irrtümlicherweise ein Upgrade statt einer neuen Installation durchführt.

**Problemumgehung**: Löschen Sie den folgenden Registrierungsschlüssel, bevor Sie mit der Installation von App-V 5,0 SP3 beginnen:

`HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\Windows\CurrentVersion\Uninstall`

## Abfragen von AD DS können dazu führen, dass einige Anwendungen falsch funktionieren


Wenn Sie aktualisierte Pakete erhalten, indem Sie die Active Directory-Domänendienste nach aktualisierten Gruppenmitgliedschaften Abfragen, kann dies dazu führen, dass einige Anwendungen falsch funktionieren, wenn die Anwendungen vom Zugriffstoken des Benutzers abhängen. Darüber hinaus können häufige Gruppen Mitgliedschafts Abfragen dazu führen, dass der Domänencontroller überlastet wird. Weitere Informationen zu Benutzerzugriffstoken finden Sie unter [Zugriffstoken](https://msdn.microsoft.com/library/windows/desktop/aa374909.aspx).

**Problemumgehung**: warten Sie, bis sich der Benutzer abmeldet und dann wieder anmeldet, bevor Sie eine Abfrage nach aktualisierten Gruppenmitgliedschaften durchführen. Verwenden Sie nicht den Registrierungsschlüssel, der im [Hotfix-Paket 2 für Microsoft Application Virtualization 5,0 Service Pack 1](https://support.microsoft.com/kb/2897087)beschrieben ist, um nach aktualisierten Gruppenmitgliedschaften zu suchen.






## Verwandte Themen


[Informationen zu App-V 5.0 SP3](about-app-v-50-sp3.md)

 

 





