---
title: Anwenden von Hotfixes auf MBAM 2,5 SP1
description: Anwenden von Hotfixes auf MBAM 2,5 SP1
ms.author: ppriya-msft
author: dansimp
ms.assetid: ''
ms.reviewer: ''
manager: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 8/30/2018
ms.openlocfilehash: 71f840ce4d57a0698289128f92b9d760ca14ddfc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810405"
---
# Anwenden von Hotfixes auf MBAM 2,5 SP1
In diesem Thema wird das Verfahren zum Anwenden der Hotfixes für die Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) Server 2,5 SP1 beschrieben.

### Bevor Sie beginnen, laden Sie den neuesten Hotfix für Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) Server 2,5 SP1 herunter.
[Desktop Optimierungspaket](https://www.microsoft.com/download/details.aspx?id=57157)

> [!NOTE]
> Weitere Informationen zu den Hotfix-Versionen finden Sie im [MBAM-Versions Diagramm](https://docs.microsoft.com/archive/blogs/dubaisec/mbam-version-chart).

#### Schritte zum Aktualisieren des MBAM-Servers für die vorhandene MBAM-Umgebung 
1. Entfernen Sie MBAM Server-Feature (Öffnen Sie dazu das MBAM Server-Konfigurations Tool, und wählen Sie dann Features entfernen) aus.
2. Entfernen von MDOP-MBAM aus der Systemsteuerung | Programme und Funktionen.
3. Installieren Sie MBAM 2,5 SP1 RTM-Server Komponenten.
4. Installieren Sie das neueste MBAM 2,5 SP1-Hotfix-Rollup.
5. Konfigurieren Sie MBAM-Features mithilfe von MBAM Server Configurator.

#### Schritte zum Installieren des neuen MBAM 2,5 SP1-Server Hotfixes
Weitere Informationen finden Sie im Dokument für die [Installation von neuen Servern](deploying-the-mbam-25-server-infrastructure.md).
