---
title: So konfigurieren Sie den Client für den unterbrochenen Betriebsmodus
description: So konfigurieren Sie den Client für den unterbrochenen Betriebsmodus
author: dansimp
ms.assetid: 3b48464a-b8b4-494b-93e3-9a6d9bd74652
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1c917d87996a26b330551deb04b1828c31fd3c73
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807259"
---
# So konfigurieren Sie den Client für den unterbrochenen Betriebsmodus


Der Modus für getrennte Vorgänge ermöglicht es dem Application Virtualization (app-v)-Desktop Client oder dem Application Virtualization (app-v)-Client für Remote Desktop Dienste (ehemals Terminal Dienste), Anwendungen auszuführen, die im Dateisystemcache des Clients gespeichert sind, wenn der Client keine Verbindung mit dem App-v-Verwaltungs Server herstellen kann.

**Wichtig**  In einer großen Organisation, in der mehrere Remote Desktop-Sitzungshost Server (ehemals Terminal Server) in einer Farm zur Unterstützung vieler Benutzer verknüpft sind, stellt die Verwendung eines einzelnen App-V-Verwaltungsservers zur Unterstützung der Farm einen einzelnen Fehlerpunkt dar. Wenn Sie eine höhere Verfügbarkeit für die Unterstützung der RDSession-Host Farm bereitstellen möchten, sollten Sie zwei oder mehr App-V-Verwaltungsserver zur Verwendung derselben Datenbank verknüpfen.

 

**So aktivieren Sie den Modus für unterbrochenen Betrieb**

-   Setzen Sie den folgenden Registrierungsschlüsselwert auf "1", um den unterbrochenen Betriebsmodus zu aktivieren:

    HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\softgrid\\4.5\\client\\network\\allowdisconnectedoperation

**So setzen Sie ein Zeitlimit für die Verwendung des getrennten Betriebsmodus**

1.  Setzen Sie den folgenden Registrierungsschlüsselwert auf 1:

    HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\softgrid\\4.5\\client\\network\\limitdisconnectedoperation

2.  Setzen Sie den folgenden Registrierungsschlüsselwert auf die Anzahl der Minuten, die Sie den unterbrochenen Betriebsmodus einschränken möchten. Der gültige Wertebereich ist 1 – 999999. Der Standardwert ist 90 Tage oder 129.600 Minuten.

    HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\softgrid\\4.5\\client\\network\\dotimeoutminutes

**So konfigurieren Sie den Client für Remote Desktop Dienste für den unterbrochenen Betriebsmodus**

1.  Stellen Sie den folgenden Registrierungsschlüsselwert auf 1 ein, um den unterbrochenen Betriebsmodus zu aktivieren:

    HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\softgrid\\4.5\\client\\network\\allowdisconnectedoperation

2.  Setzen Sie den folgenden Registrierungsschlüsselwert auf 0 (null), um die unbegrenzte Verwendung des unterbrochenen Betriebsmodus zu ermöglichen:

    HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\softgrid\\4.5\\client\\network\\limitdisconnectedoperation

3.  Stellen Sie sicher, dass alle Pakete in den Cache geladen sind, um die Leistung zu verbessern.

## Verwandte Themen


[Unterbrochener Betriebsmodus](disconnected-operation-mode.md)

[So konfigurieren Sie die App-V-Client-Registrierungseinstellungen über die Befehlszeile](how-to-configure-the-app-v-client-registry-settings-by-using-the-command-line.md)

 

 





