---
title: Problembehandlung von AGPM-Upgrades
description: Problembehandlung von AGPM-Upgrades
author: dansimp
ms.assetid: 1abbf0c1-fd32-46a8-a3ba-c005f066523d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2089eac51803dca60da51f61ebdb112fbf0bda08
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807431"
---
# Problembehandlung von AGPM-Upgrades

In diesem Abschnitt werden häufig auftretende Probleme aufgeführt, die beim Upgrade des Advanced Group Policy Management (AGPM)-Servers auf eine neuere Version (beispielsweise AGPM 4,0 auf AGPM 4,3) auftreten können. Wenn Sie Probleme diagnostizieren möchten, die hier nicht aufgeführt sind, ist es möglicherweise hilfreich, die [Problembehandlung für AGPM](troubleshooting-agpm-agpm40.md) anzuzeigen oder einem AGPM-Administrator (Vollzugriff) die Protokollierung und Ablaufverfolgung zu verwenden. Weitere Informationen finden Sie unter [Konfigurieren der Protokollierung und Ablaufverfolgung](configure-logging-and-tracing-agpm40.md).

## Welche Probleme haben Sie?

-   [Fehler beim Generieren eines HTML-GPO-Unterschiedsberichts (Fehlercode 80004003)](#bkmk-error-80004003)

### <a href="" id="bkmk-error-80004003"></a>Fehler beim Generieren eines HTML-GPO-Unterschiedsberichts (Fehlercode 80004003)

-   **Ursache**: Sie haben das AGPM-Upgrade-Paket mit einem falschen Konto installiert.

-   **Lösung**: Sie müssen ein AGPM-Administrator sein, um dieses Problem beheben zu können.
    
    -   Stellen Sie sicher, dass Sie den Benutzernamen & Kennwort Ihres **AGPM-Dienstkontos**kennen.

    -   Melden Sie sich auf Ihrem AGPM-Server interaktiv als AGPM-Dienstkonto an.
        
        -   Dies ist wichtig, da die Installation fehlschlägt, wenn Sie ein anderes Konto verwenden.

    -   Beenden Sie den AGPM-Dienst.
    
    -   Installieren Sie den erforderlichen Hotfix.
    
    -   Stellen Sie mit einem AGPM-Client eine Verbindung mit AGPM her, um zu testen, ob Ihre Differenz Berichte nun funktionieren.
    
## Installieren des Hotfix-Pakets 1 für Microsoft Advanced Group Policy Management 4,0 SP3
    
**In diesem Hotfix behobenes Problem**: AGPM kann keine Differenz Berichte generieren, wenn neue Gruppenrichtlinienobjekte (Group Policy Objects, GPOs) gesteuert oder verwaltet werden.

So **erhalten Sie dieses Update**: Installieren Sie die neueste Version des Microsoft-Desktop Optimierungs Pakets ([März 2017-Wartungsversion](https://www.microsoft.com/download/details.aspx?id=54967)). Weitere Informationen finden Sie unter [KB 4014009](https://support.microsoft.com/help/4014009/) .

Genauer gesagt: Sie können auswählen, dass nur die erste Datei in `AGPM4.0SP1_Server_X64_KB4014009.exe` der nach dem Drücken der Schaltfläche herunterladen angezeigten Liste heruntergeladen werden soll.
      
Der Download-Link zum Microsoft-Desktop Optimierungspaket (März 2017-Wartungsversion) finden Sie [hier](https://www.microsoft.com/download/details.aspx?id=54967).
      
      
## Verweis Link
https://support.microsoft.com/help/3127165/hotfix-package-1-for-microsoft-advanced-group-policy-management-4-0-sp
      
