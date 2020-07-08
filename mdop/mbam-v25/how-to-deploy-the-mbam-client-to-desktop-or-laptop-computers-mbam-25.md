---
title: So stellen Sie den MBAM-Client auf Desktop- oder Laptopcomputern bereit
description: So stellen Sie den MBAM-Client auf Desktop- oder Laptopcomputern bereit
author: dansimp
ms.assetid: 3a7639e0-468e-4496-8be2-ed29b8e07c53
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6b67533a555da4dabec6654ed3f95f91ad8d37bf
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810579"
---
# So stellen Sie den MBAM-Client auf Desktop- oder Laptopcomputern bereit


In diesem Thema wird erläutert, wie der MBAM-Client auf Computern der Endbenutzer bereitgestellt wird. Sie können den MBAM-Client über ein elektronisches Softwareverteilungssystem wie Active Directory-Domänendienste oder MicrosoftSystemCenterConfiguration-Manager bereitstellen.

Informationen zum Bereitstellen des MBAM-Clients als Teil einer Windows-Bereitstellung finden Sie unter [Aktivieren von BitLocker mithilfe von MBAM als Teil einer Windows-Bereitstellung](how-to-enable-bitlocker-by-using-mbam-as-part-of-a-windows-deploymentmbam-25.md).

Bevor Sie die MBAM-Client Bereitstellung starten, überprüfen Sie die [MBAM 2,5-unterstützten Konfigurationen](mbam-25-supported-configurations.md).

**So stellen Sie den MBAM-Client auf Desktop-oder Laptopcomputern bereit**

1.  Suchen Sie die MBAM-Client Installationsdateien, die mit der MBAM-Software bereitgestellt werden.

2.  Verwenden Sie Active Directory-Domänendienste oder ein Enterprise-Softwarebereitstellungstool wie MicrosoftSystemCenterConfiguration-Manager, um das Windows Installer-Paket auf Zielcomputern bereitzustellen.

3.  Konfigurieren Sie die Verteilungseinstellungen oder Gruppenrichtlinieneinstellungen, um die MBAM-Client Installationsdatei auszuführen.

    Nach der erfolgreichen Installation wendet der MBAM-Client die Gruppenrichtlinieneinstellungen an, die von einem Domänencontroller empfangen werden, um die BitLocker-Laufwerkverschlüsselung und-Verwaltungsfunktionen zu starten.

    **Wichtig**  Der MBAM-Client startet keine BitLocker-Laufwerk Verschlüsselungs Aktionen, wenn eine Remotedesktopprotokoll-Verbindung aktiv ist. Alle Remotekonsolen Verbindungen müssen geschlossen sein, und ein Benutzer muss an einer physikalischen Konsolensitzung angemeldet sein, bevor die BitLocker-Laufwerkverschlüsselung beginnt.

     


## Verwandte Themen
[Bereitstellen des MBAM 2.5-Clients](deploying-the-mbam-25-client.md)

[Planen der Clientbereitstellung für MBAM 2.5](planning-for-mbam-25-client-deployment.md)

 

## Sie haben einen Vorschlag für MBAM?
- [Hier](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)können Sie Vorschläge hinzufügen oder abstimmen. 
- Bei MBAM-Problemen verwenden Sie das [MBAM TechNet-Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





