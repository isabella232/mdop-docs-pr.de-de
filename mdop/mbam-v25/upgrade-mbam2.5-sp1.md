---
title: Aktualisieren von MBAM 2,5 auf MBAM 2,5 SP1-Update zur Wartungsversion
author: dansimp
ms.author: ksharma
manager: miaposto
audience: ITPro
ms.topic: article
ms.prod: w10
ms.localizationpriority: Normal
ms.openlocfilehash: 372822e1ec049871c62af9f429290b88bbfac949
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804475"
---
# Upgrade von MBAM 2,5 auf MBAM 2,5 SP1-Update zur Wartungsversion

In diesem Artikel finden Sie Schritt-für-Schritt-Anleitungen zum Upgrade von Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) 2,5 auf MBAM 2,5 Service Pack 1 (SP1) zusammen mit dem [Microsoft Desktop Optimization Pack (MDOP)-Update](https://support.microsoft.com/help/4505175/may-2019-servicing-release-for-microsoft-desktop-optimization-pack) für die Wartung von 2019 in einer eigenständigen Konfiguration.

In diesem Leitfaden wird eine Konfiguration mit zwei Servern verwendet. Bei einem Server handelt es sich um einen Datenbankserver, auf dem Microsoft SQL Server 2016 ausgeführt wird. Dieser Server hostet die MBAM-Datenbanken und-Berichte. Der andere Server ist ein Windows Server 2012 R2-Webserver. Auf diesem Server werden "Verwaltung und Überwachung" und "Self-Service-Portal" gehostet.

## Vorbereiten des Upgrades von MBAM 2,5 SP1

### Kennen Sie die MBAM-Server in Ihrer Umgebung

1. SQL Server-Datenbankmodul: Server, der die MBAM-Datenbanken hostet.
2. SQL Server Reporting Services: Server, der die MBAM-Berichte hostet.
3. Internetinformationsdienste (IIS)-Webservern: Server, auf dem MBAM-Webanwendungen und MBAM-Dienste gehostet werden.
4. Optional Microsoft System Center Configuration Manager-Primärer Standortserver: die MBAM-Konfigurationsanwendung wird auf diesem Server ausgeführt, um MBAM-Berichte mit Configuration Manager zu integrieren. Diese Berichte werden dann mit vorhandenen Configuration Manager-Berichten in der Configuration Manager-Instanz von SQL Server Reporting Services (SSRS) zusammengeführt.

### Identifizieren von Dienstkonten, Gruppen, Servername und Berichts-URL

1. Identifizieren Sie das MBAM-Anwendungspooldienst Konto, das von IIS-Webservern zum Lesen und Schreiben von Daten in MBAM-Datenbanken verwendet wird.
2. Identifizieren Sie die Gruppen, die während der Konfiguration von MBAM Web Features verwendet werden, und die URL des Berichtsweb Diensts.
3. Ermitteln Sie den Namen und den Instanznamen von SQL Server. Schauen Sie sich dieses Video an, um weitere Informationen zu erhalten.

    > [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE3ANP1]

4. Identifizieren Sie das SQL Server Reporting Services-Konto, das zum Lesen von Kompatibilitätsdaten aus der Compliance-und Überwachungsdatenbank verwendet wird. Schauen Sie sich dieses Video an, um weitere Informationen zu erhalten.

    > [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE3ALdZ]

## Upgrade der MBAM-Infrastruktur auf die neueste verfügbare Version

Die Installation oder das Upgrade der MBAM-Server Infrastruktur erfolgt immer in der nachstehend aufgeführten Reihenfolge:

- SQL Server-Datenbankmodul: Datenbanken
- SQL Server Reporting Services: Berichte
- Webserver: Webanwendungen
- SCCM-Server: in SCCM integrierte Berichte (falls zutreffend)
- Clients: MBAM-Agent oder Client Update
- Vorlagen für Gruppenrichtlinien: Aktualisieren Sie die vorhandene Gruppenrichtlinie mit neuen Vorlagen, und aktivieren Sie neue Einstellungen für vorhandene MBAM-Gruppenrichtlinien.

> [!NOTE]
> Wir empfehlen, dass Sie vor dem Ausführen der Upgrades eine vollständige Datenbanksicherung der MBAM-Datenbankenerstellen.

### Aktualisieren des MBAM SQL Server

Schauen Sie sich dieses Video an, um zu erfahren, wie Sie den MBAM SQL Server aktualisieren:

   > [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE3ALew]

### Aktualisieren des MBAM-Webservers

Schauen Sie sich dieses Video an, um zu erfahren, wie Sie den MBAM-Webserver aktualisieren:

   > [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE3ALex]

## Weitere Informationen

Weitere Informationen zu bekannten Problemen in MBAM 2,5 SP1 finden Sie unter [Anmerkungen zu dieser Version von MBAM 2,5 SP1](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/release-notes-for-mbam-25-sp1).
