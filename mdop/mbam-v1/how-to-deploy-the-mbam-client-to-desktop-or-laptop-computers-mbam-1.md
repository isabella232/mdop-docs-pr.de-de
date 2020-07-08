---
title: So stellen Sie den MBAM-Client auf Desktop- oder Laptopcomputern bereit
description: So stellen Sie den MBAM-Client auf Desktop- oder Laptopcomputern bereit
author: dansimp
ms.assetid: f32927a2-4c05-4da8-acca-1108d1dfdb7e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ce4f8597cc182c037983a89efd60c5ef935712ce
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811218"
---
# So stellen Sie den MBAM-Client auf Desktop- oder Laptopcomputern bereit


Der Client für die Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) ermöglicht Administratoren das erzwingen und Überwachen der BitLocker-Laufwerkverschlüsselung auf Computern im Unternehmen. Der MBAM-Client kann in eine Organisation integriert werden, indem der Client mithilfe von Tools wie Active Directory-Domänendiensten oder einem Enterprise-Softwarebereitstellungstool wie MicrosoftSystemCenter2012 ConfigurationManager bereitgestellt wird.

**Hinweis**  Informationen zum Überprüfen der MBAM-Client Systemanforderungen finden Sie unter [unterstützte MBAM 1,0-Konfigurationen](mbam-10-supported-configurations.md).

 

**So stellen Sie den MBAM-Client auf Desktop-oder Laptopcomputern bereit**

1.  Suchen Sie die MBAM-Client Installationsdateien, die mit der MBAM-Software bereitgestellt werden.

2.  Bereitstellen des Windows Installer-Pakets auf Zielcomputern mithilfe von Active Directory-Domänendiensten oder eines Enterprise-Softwarebereitstellungstools wie MicrosoftSystemCenter2012 ConfigurationManager.

    **Hinweis**  Verwenden Sie Gruppenrichtlinien nicht zum Bereitstellen des Windows Installer-Pakets.

     

3.  Konfigurieren Sie die Verteilungseinstellungen oder Gruppenrichtlinien so, dass die MBAM-Client Installationsdatei ausgeführt wird. Nach der erfolgreichen Installation wendet der MBAM-Client die Gruppenrichtlinieneinstellungen an, die von einem Domänencontroller empfangen werden, um BitLocker-Verschlüsselungs-und-Verwaltungsfunktionen zu starten. Weitere Informationen zu den MBAM-Gruppenrichtlinieneinstellungen finden Sie unter [Planen von MBAM 1,0-Gruppenrichtlinienanforderungen](planning-for-mbam-10-group-policy-requirements.md).

    **Wichtig**  Der MBAM-Client startet keine BitLocker-Verschlüsselungs Aktionen, wenn eine Remotedesktopprotokoll-Verbindung aktiv ist. Alle Remotekonsolen Verbindungen müssen geschlossen werden, bevor die BitLocker-Verschlüsselung beginnt.

     

## Verwandte Themen


[Bereitstellen des MBAM 1.0-Clients](deploying-the-mbam-10-client.md)

 

 





