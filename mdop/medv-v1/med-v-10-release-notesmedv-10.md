---
title: Versionshinweise für MED-V 1.0
description: Versionshinweise für MED-V 1.0
author: dansimp
ms.assetid: 006a3537-5c5b-43b5-8df8-4bf6ddd3cd2f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 683056f768a3d547828996a9b191d58337c21ad6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811848"
---
# Versionshinweise für MED-V 1.0


## Bekannte Probleme mit MED-V


Dieser Abschnitt enthält die aktuellsten Informationen zu allgemeinen Problemen mit der Microsoft Enterprise Desktop Virtualization (MED-V)-Plattform. Diese Probleme werden in der Produktdokumentation nicht angezeigt und können in einigen Fällen der vorhandenen Produktdokumentation widersprechen. Wenn möglich, werden diese Probleme in späteren Versionen behoben.

### Dateidownloads folgen nicht den webumleitungs Regeln

Dateidownloads folgen nicht den webumleitungs Regeln, die in einer MED-V-Arbeitsbereichs Richtlinie festgesetzt sind.

### Wenn Sie ein von der Konsole veröffentlichtes Anwendungsfenster auf den Vollbildmodus erweitern, wird es nicht mehr angezeigt.

Wenn Sie eine von der Konsole veröffentlichte Anwendung (wie cmd.exe) auf Vollbild in einem im Seamless-Integrationsmodus konfigurierten MED-V-Arbeitsbereich erweitern, kann das Anwendungsfenster verschwinden oder nicht reagieren.

### Wenn Sie im vollständigen Desktopmodus arbeiten, werden die Symbolspeicherorte auf dem Desktop nicht gespeichert.

Wenn Sie im vollständigen Desktopmodus arbeiten, werden die Änderungen manueller Standort Symbole auf dem Desktop nicht zwischen MED-V Workspace-Sitzungen gespeichert.

### Ein lokales Bild und ein Testbild mit demselben Namen können in der gleichen Domäne nicht vorhanden sein.

Wenn ein lokales Bild zur Domäne hinzugefügt wird und der Administrator eine neue Version desselben Bilds mit dem gleichen Computernamen wie ein Testbild erstellt, wenn das Testbild der Domäne Beitritt, schlägt entweder die Aktion für die Join-Domäne fehl, oder es ist erfolgreich, und das lokale Bild wird aus der Domäne entfernt.

### MED-V unterstützt keine Windows Aero-Features

MED-V unterstützt keine Windows Aero-Features (wie Aero Flip 3D).

### Die Verwaltungskonsole kann nur von einem Windows-Benutzer pro Computer verwendet werden.

Die MED-V-Verwaltungskonsole kann nur von Administratoren und dem Windows-Benutzer verwendet werden, der die Verwaltungsanwendung installiert hat.

### Das Med-v Server-Konfigurationsdienstprogramm testet die Microsoft SQL Server-Konnektivität unter dem Benutzerkontext und nicht unter dem Med-v Server-Dienstkontext.

Med-v verwendet den Med-v-Server Dienstkontext, um Berichte aus der Microsoft SQL Server-Berichtsdatenbank zu sammeln. Das MED-V Server-Konfigurationsdienstprogramm überprüft die Datenbank und testet die Datenbankverbindungszeichenfolge. Der Zugriff des MED-V-Server Diensts auf die Datenbank wird nicht überprüft.

 

 





