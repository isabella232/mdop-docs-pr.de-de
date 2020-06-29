---
title: Konfigurieren der Umgebungsvoraussetzungen
description: Konfigurieren der Umgebungsvoraussetzungen
author: dansimp
ms.assetid: 7379e8e5-1cb2-4b8e-8acc-5c04e26f8c91
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 8d6fc3b81f6dafbe709dd904b9fba6124d2f6b6a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811761"
---
# Konfigurieren der Umgebungsvoraussetzungen


Bevor Sie Microsoft Enterprise Desktop Virtualization (MED-V) 2,0 bereitstellen und ausführen können, müssen Sie sicherstellen, dass Ihre Umgebung die folgenden Mindestvoraussetzungen erfüllt.

**Windows7**

Der Med-v-Host-Agent und der Med-v-Arbeitsbereichs-Packager werden nur in Windows 7 oder höher unterstützt.

**Windows XP SP3**

Der MED-V-Gast-Agent wird nur in Windows XP SP3 unterstützt.

**.NET Framework 3,5 SP1**

Für den Med-v-Host und die Guest-Agents sowie für den Med-v-Arbeitsbereichs-Packager ist Microsoft .NET Framework 3,5 SP1 erforderlich.

**Wichtig**  Sie müssen auch das Update [KB959209](https://go.microsoft.com/fwlink/?LinkId=204950) ( https://go.microsoft.com/fwlink/?LinkId=204950) , das mehrere bekannte Probleme mit der Anwendungskompatibilität behebt, installieren.

 

**Hinweis**  Sie müssen .NET Framework 3,5 SP1 und das Update KB959209 manuell in das Windows Virtual PC-Abbild installieren, das Sie für die Verwendung mit MED-V vorbereiten. Standardmäßig sind jedoch Microsoft .NET Framework 3,5 SP1 und das Update enthalten, wenn Sie Windows 7 auf dem Hostcomputer installieren.

 

**Eine Active Directory-Infrastruktur**

Gruppenrichtlinien stellen die zentralisierte Verwaltung und Konfiguration von Betriebssystemen, Anwendungen und Benutzereinstellungen in einer Active Directory-Umgebung bereit.

## Verwandte Themen


[Konfigurieren der Installationsvoraussetzungen](configure-installation-prerequisites.md)

[High-Level-Architektur](high-level-architecturemedv2.md)

[Von MED 2.0 unterstützte Konfigurationen](med-v-20-supported-configurations.md)

 

 





