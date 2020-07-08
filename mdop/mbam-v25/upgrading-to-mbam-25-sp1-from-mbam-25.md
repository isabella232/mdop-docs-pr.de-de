---
title: Aktualisieren von MBAM 2.5 auf MBAM 2.5 SP1
description: Aktualisieren von MBAM 2.5 auf MBAM 2.5 SP1
author: dansimp
ms.assetid: ''
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 2/16/2018
ms.openlocfilehash: 19da3df0976b51700e0d10c302a31421a88d17e4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804457"
---
# Aktualisieren von MBAM 2.5 auf MBAM 2.5 SP1
In diesem Thema wird beschrieben, wie Sie den Microsoft BitLocker-Verwaltungs-und-Überwachungs Server (MBAM) 2,5 und den MBAM-Client von 2,5 auf MBAM 2,5 SP1 aktualisieren.

### Vorbemerkungen
#### Herunterladen der Service Version vom Mai 2019
[Desktop Optimierungspaket](https://www.microsoft.com/download/details.aspx?id=58345)

#### Überprüfen der Installationsdokumentation
Stellen Sie sicher, dass Sie über eine aktuelle Dokumentation Ihrer MBAM-Umgebung verfügen, einschließlich aller Servernamen, Datenbanknamen, Dienstkonten und deren Kennwörter.

### Upgrade-Schritte
#### Schritte zum Upgrade der MBAM-Datenbank (SQL Server)
1. Verwenden des MBAM-Konfigurators; Entfernen Sie die Rolle "Berichte" aus dem SQL Server oder unabhängig davon, wo die SSRS-Datenbank gehostet wird. Je nach Umgebung kann es sich um denselben Server oder eine separate Person handeln.
  > [!NOTE]
  > Es wird keine Option zum Entfernen der Datenbanken angezeigt. Dies wird erwartet.  
2. Installieren Sie 2,5 SP1 (mit dem MDOP-Microsoft-Desktop Optimierungspaket 2015 auf der Volumen Lizenzierungs-Service Center-Website:  <https://www.microsoft.com/Licensing/servicecenter/default.aspx>
3. Zu diesem Zeitpunkt keine Konfiguration vornehmen 
4. Verwenden des MBAM-Konfigurators; erneutes Hinzufügen der Rolle "Berichte"
5. Verwenden des MBAM-Konfigurators; erneutes Hinzufügen der SQL-Datenbankrolle auf dem SQL Server
6. Am Ende wird eine Warnung angezeigt, dass die DBS bereits vorhanden sind und nicht erstellt wurden, dies wird jedoch erwartet.
7. Durch diesen Vorgang werden die vorhandenen Datenbanken auf die aktuelle Version aktualisiert, die installiert wird.              

#### Schritte zum Upgrade des MBAM-Servers (mit MBAM und IIS)
1. Verwenden des MBAM-Konfigurators; Entfernen der Administrator-und Self-Service-Portale vom IIS-Server
2. Installieren von MBAM 2,5 SP1
3. Zu diesem Zeitpunkt keine Konfiguration vornehmen  
4. Verwenden des MBAM-Konfigurators; erneutes Hinzufügen der Administrator-und Self Service-Portale zum IIS-Server 
5. Öffnen Sie eine Eingabeaufforderung mit erhöhten Rechten, geben Sie **iisreset**ein, und drücken Sie die EINGABETASTE.
 
#### Schritte zum Upgrade der MBAM-Clients/-Endpunkte
1. Deinstallieren des 2,5-Agents aus Clientendpunkten
2. Installieren des 2,5 SP1-Agents auf den Clientendpunkten
3. Pushen des Client Updates für das 2019-Rollup für Mai auf Clients mit dem 2,5 SP1-Agent 
4. Es ist nicht erforderlich, den vorhandenen Client vor der Installation des 2019-Rollups für Mai zu deinstallieren.  
