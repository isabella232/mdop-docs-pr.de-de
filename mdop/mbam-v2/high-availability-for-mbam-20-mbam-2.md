---
title: Hohe Verfügbarkeit von MBAM 2.0
description: Hohe Verfügbarkeit von MBAM 2.0
author: dansimp
ms.assetid: 244ee013-9e2a-48d2-b842-4e10594fd74f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6482a099d96aee731f81368b8b787325e592c453
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810729"
---
# Hohe Verfügbarkeit von MBAM 2.0


Dieses Thema enthält grundlegende Informationen zu einer hoch verfügbaren Installation von Microsoft BitLocker-Verwaltung und-Überwachung (MBAM). Szenarien mit hoher Verfügbarkeit werden in dieser Version von MBAM nicht vollständig unterstützt, daher werden Sie hier nicht beschrieben. Es wird empfohlen, Verwandte Blogs und Foren zu durchsuchen, in denen Benutzer beschreiben, wie Sie die Höchstverfügbarkeit für MBAM in ihren Umgebungen erfolgreich konfiguriert haben.

## Szenarien für die Höchstverfügbarkeit für MBAM


Die Microsoft BitLocker-Verwaltung und-Überwachung wurde als fehlertolerant konzipiert. Wenn ein Server nicht mehr zur Verfügung steht, sollten die Benutzer nicht negativ beeinflusst werden. Wenn beispielsweise der MBAM-Agent keine Verbindung mit dem MBAM-Webserver herstellen kann, sollten Benutzer nicht zur Eingabe einer Aktion aufgefordert werden.

Wenn Sie Ihre MBAM-Installation planen, sollten Sie die folgenden Elemente in Frage stellen, die sich auf die Verfügbarkeit des MBAM-Diensts auswirken können:

-   Laufwerksverschlüsselung und Wiederherstellungskennwort – wenn ein Wiederherstellungskennwort nicht über einen Treuhandservice verfügt, wird die Verschlüsselung nicht auf dem Clientcomputer gestartet.

-   Upload von Kompatibilitätsstatus Daten – Wenn der Server, auf dem der Kompatibilitätsstatus-Berichtsdienst gehostet wird, nicht verfügbar ist, bleiben die Kompatibilitätsdaten nicht aktuell.

-   Zugriff auf Helpdesk-Wiederherstellungsschlüssel – wenn der Helpdesk nicht auf Informationen zu MBAM-Datenbanken zugreifen kann, kann der Helpdesk keine Wiederherstellungsschlüssel für Benutzer bereitstellen.

-   Verfügbarkeit von Berichten – wenn der Server, auf dem die Konformitäts-und Überwachungsberichte gehostet werden, nicht verfügbar ist, stehen Berichte nicht zur Verfügung.

## <a href="" id="how-the-mbam-backup-uses-the-volume-shadow-copy-service--vss--"></a>Verwendung des Volumeschattenkopie-Diensts (Volume Shadow Copy Service, VSS) durch die MBAM-Sicherung


Mbam 2.0 bietet einen VSS-Writer (Volume Shadow Copy Service) mit dem Namen Microsoft BitLocker-Verwaltungs-und-Verwaltungs-Writer, der die Sicherung der Compliance-und Überwachungsdatenbank sowie der Wiederherstellungsdatenbank vereinfacht.

Der MBAM-Server Windows Installer registriert den MBAM-VSS-Writer. Jeder Fehler während der VSS-Writer-Registrierung führt dazu, dass die MBAM-Server Installation zurückgesetzt wird. In einer Topologie, in der die Kompatibilitäts-und Überwachungsdatenbank sowie die Wiederherstellungsdatenbank auf unterschiedlichen Servern installiert sind, wird eine separate Instanz von MBAM VSS Writer auf jedem Server registriert. Der MBAM-VSS-Writer ist vom SQL Server VSS-Writer abhängig. Der SQL Server-VSS-Writer wird als Teil der Microsoft SQL Server-Installation registriert. Jede Sicherungstechnologie, die VSS-Writer zum Durchführen einer Sicherung verwendet, kann den MBAM VSS-Writer ermitteln.

## Verwandte Themen


[Verwalten von MBAM 2.0](maintaining-mbam-20-mbam-2.md)

 

 





