---
title: So stellen Sie den MBAM-Client auf Desktop- oder Laptopcomputern bereit
description: So stellen Sie den MBAM-Client auf Desktop- oder Laptopcomputern bereit
author: dansimp
ms.assetid: 56744922-bfdd-48f6-ae01-645ff53b64a8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 49340ae970dafc9d263f5564e7981a402da40f19
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804655"
---
# So stellen Sie den MBAM-Client auf Desktop- oder Laptopcomputern bereit


Der Client für die Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) ermöglicht Administratoren das erzwingen und Überwachen der BitLocker-Laufwerkverschlüsselung auf Computern im Unternehmen. Der BitLocker-Client kann in eine Organisation integriert werden, indem der Client über ein elektronisches Softwareverteilungssystem wie Active Directory-Domänendienste oder MicrosoftSystemCenterConfigurationManager bereitgestellt wird.

**Hinweis**  Informationen zum Überprüfen der Systemanforderungen für die Microsoft BitLocker-Verwaltung und-Überwachung finden Sie unter [unterstützte MBAM 2,0-Konfigurationen](mbam-20-supported-configurations-mbam-2.md).

 

**So stellen Sie den MBAM-Client auf Desktop-oder Laptopcomputern bereit**

1.  Suchen Sie die MBAM-Clientinstallationsdateien, die mit der MBAM-Software bereitgestellt werden.

2.  Verwenden Sie Active Directory-Domänendienste oder ein Enterprise-Softwarebereitstellungstool wie MicrosoftSystemCenterConfigurationManager, um das Windows Installer-Paket auf Zielcomputern bereitzustellen.

3.  Konfigurieren Sie die Verteilungseinstellungen oder Gruppenrichtlinien so, dass die MBAM-Client Installationsdatei ausgeführt wird. Nach der erfolgreichen Installation wendet der MBAM-Client die Gruppenrichtlinieneinstellungen an, die von einem Domänencontroller empfangen werden, um BitLocker-Verschlüsselungs-und-Verwaltungsfunktionen zu starten. Weitere Informationen zu den MBAM-Gruppenrichtlinieneinstellungen finden Sie unter [Planen von MBAM 2,0-Gruppenrichtlinienanforderungen](planning-for-mbam-20-group-policy-requirements-mbam-2.md).

    **Wichtig**  Der MBAM-Client startet keine BitLocker-Verschlüsselungs Aktionen, wenn eine Remotedesktopprotokoll-Verbindung aktiv ist. Alle Remotekonsolen Verbindungen müssen geschlossen werden, bevor die BitLocker-Verschlüsselung beginnt.

     

## Verwandte Themen


[Bereitstellen des MBAM 2.0-Clients](deploying-the-mbam-20-client-mbam-2.md)

 

 





