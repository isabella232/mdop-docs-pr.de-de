---
title: Hohe Verfügbarkeit von MBAM 1.0
description: Hohe Verfügbarkeit von MBAM 1.0
author: dansimp
ms.assetid: 5869ecf8-1056-4c32-aecb-838a37e05d39
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 1227967d647cbfbc16967b5936066fd73d2412e2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811110"
---
# Hohe Verfügbarkeit von MBAM 1.0


In diesem Thema wird beschrieben, wie Sie eine hoch verfügbare Installation von Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) konfigurieren.

## Szenarien für die Höchstverfügbarkeit für MBAM


Die Microsoft BitLocker-Verwaltung und-Überwachung (MBAM) wurde als fehlertolerant konzipiert. Wenn ein Server nicht mehr zur Verfügung steht, sollten die Benutzer nicht negativ beeinflusst werden. Wenn beispielsweise der MBAM-Agent keine Verbindung mit dem MBAM-Webserver herstellen kann, sollten Benutzer nicht zur Eingabe einer Aktion aufgefordert werden.

Berücksichtigen Sie bei der Planung Ihrer MBAM-Installation die folgenden Bedenken, die sich auf die Verfügbarkeit des MBAM-Diensts auswirken können:

-   Laufwerksverschlüsselung und Wiederherstellungskennwort – wenn ein Wiederherstellungskennwort nicht über einen Treuhandservice verfügt, wird die Verschlüsselung auf dem Clientcomputer nicht gestartet.

-   Upload von Kompatibilitätsstatus Daten – Wenn der Server, auf dem der Kompatibilitätsstatus-Berichtsdienst gehostet wird, nicht verfügbar ist, bleiben die Kompatibilitätsdaten nicht aktuell.

-   Help Desk-Wiederherstellungsschlüssel Zugriff – wenn der Helpdesk nicht auf MBAM-Datenbankinformationen zugreifen kann, können Sie den Benutzern keine Wiederherstellungsschlüssel zur Verfügung stellen.

-   Verfügbarkeit von Berichten – Berichte stehen nicht zur Verfügung, wenn der Server, auf dem die Konformitäts-und Überwachungsberichte gehostet werden, nicht verfügbar ist.

Das Hauptproblem bei der MBAM-Höchstverfügbarkeit ist die Verfügbarkeit der BitLocker-Schlüsselwiederherstellung. Wenn der Helpdesk keine Wiederherstellungsschlüssel bereitstellen kann, können Benutzer, die gesperrt sind, ihre Computer nicht entsperren. Um dieses Problem zu vermeiden, sollten Sie redundante Webserver und Datenbanken implementieren, um eine optimale Verfügbarkeit zu gewährleisten.

Weitere Informationen zur MBAM-Skalierbarkeit und zu einer höheren Verfügbarkeit finden Sie unter [Whitepaper zur MBAM-Skalierbarkeit](https://go.microsoft.com/fwlink/p/?LinkId=229025) ( https://go.microsoft.com/fwlink/p/?LinkId=229025) .

Allgemeine Anleitungen zur Hochverfügbarkeits-Verfügbarkeit für Microsoft SQL Server finden Sie unter [Höchstverfügbarkeit](https://go.microsoft.com/fwlink/p/?LinkId=221504) ( https://go.microsoft.com/fwlink/p/?LinkId=221504) .

Allgemeine Anleitungen zur Verfügbarkeit und Skalierbarkeit für Webserver finden Sie unter [Verfügbarkeit und Skalierbarkeit](https://go.microsoft.com/fwlink/p/?LinkId=221503) ( https://go.microsoft.com/fwlink/p/?LinkId=221503) .

## Verwandte Themen


[Verwalten von MBAM 1.0](maintaining-mbam-10.md)

 

 





