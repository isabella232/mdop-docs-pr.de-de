---
title: Identifizieren Sie die Anzahl der Instanzen von MED-V
description: Identifizieren Sie die Anzahl der Instanzen von MED-V
author: dansimp
ms.assetid: edea9bdf-a28c-4d24-9298-7bd6536c3a94
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 22f7d54318d2dc489461474e5531c5162d8c087d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810447"
---
# Identifizieren Sie die Anzahl der Instanzen von MED-V


Sie müssen die Anzahl der MED-V-Instanzen ermitteln und den Bereich für jede Instanz definieren, damit Sie die Serverinfrastruktur entwerfen können. Eine MED-V-Instanz enthält Folgendes:

-   Der Med-v-Server und die auf dem Server gespeicherten Med-v-Arbeitsbereiche, einschließlich der Active Directory-Berechtigungen.

-   Eine SQL Server-Datenbank, in der Clientereignisse gespeichert werden. Die Datenbank kann von mehreren MED-V-Instanzen freigegeben werden.

-   Das Bild-Repository für die komprimierten MED-V-Bilder. Das Repository kann von mehreren MED-V-Instanzen freigegeben werden.

-   Die Verwaltungskonsole, die zum Erstellen und Verpacken von Bildern und zum Erstellen von MED-V-Arbeitsbereichen verwendet wird. Die Konsole kann nicht gleichzeitig von mehreren Med-v-Instanzen verwendet werden, kann aber von einem Med-v-Server getrennt und dann mit einem anderen Med-v-Server verbunden werden.

-   Med-v-Clients, die Med-v-Arbeitsbereiche empfangen, und die Autorisierung, Sie vom Server zu verwenden.

Separate Med-v-Instanzen können nicht integriert oder Med-v-Arbeitsbereiche freigegeben werden. Deshalb dezentralisiert jede zusätzliche Instanz die Virtualisierungs-Verwaltung.

## Ermitteln der Anzahl der erforderlichen MED-V-Instanzen


Beginnen Sie mit der Annahme, dass Sie eine MED-V-Instanz verwenden. Nehmen Sie dann die folgenden Bedingungen in Frage, und fügen Sie weitere Instanzen für jede für Ihre Infrastruktur geltende Bedingung hinzu.

-   Anzahl unterstützter Benutzer – jede MED-V-Instanz kann bis zu 5.000 gleichzeitig aktive Clients unterstützen. Gleichzeitig aktiv bedeutet, dass der Client mit dem MED-V-Server Online ist und Umfragen an den Server sendet, um Richtlinien-und Bildaktualisierungen sowie Ereignisse zu erhalten. Wenn Ihre Infrastruktur mehr als 5.000 aktive Benutzer umfassen soll, fügen Sie eine Instanz für alle 5.000-Benutzer hinzu.

-   Benutzer in nicht vertrauenswürdigen Domänen – die Med-v Server Associates Med-v Workspace-Berechtigungen für Active Directory-Benutzer und/oder-Gruppen. Dies erfordert, dass Med-v-Benutzer innerhalb der Vertrauensgrenze des Med-v-Servers vorhanden sind. Hinzufügen einer Med-v-Instanz für jede Gruppe von Med-v-Benutzern, die sich in einer separaten, nicht vertrauenswürdigen Domäne befindet

-   Clients in isolierten Netzwerken – ermitteln Sie, ob sich Clients in isolierten Netzwerken befinden und daher eine separate MED-V-Instanz erforderlich sind. Beispielsweise isolieren Organisationen häufig Lab-Netzwerke aus Produktionsnetzwerken. Fügen Sie für jedes isolierte Netzwerk, das Med-v-Clients enthalten soll, eine Med-v-Instanz hinzu.

-   Organisatorische Anforderungen – für die Organisation kann es erforderlich sein, dass eine Gruppe von Clients aus Sicherheitsgründen von einer separaten MED-V-Instanz verwaltet wird, beispielsweise wenn vertrauliche Anwendungen nur an eine eingeschränkte Anzahl von Benutzern innerhalb einer Domäne übermittelt werden. Beispielsweise kann die lohnabteilung Benutzern aus anderen Abteilungen den Zugriff auf die MED-V-Instanz verweigern, in der die Richtlinie für die Lohnbearbeitung gespeichert ist. Wenn die Organisation darüber hinaus ein verteiltes Verwaltungsmodell verwendet, ist möglicherweise eine separate Med-v-Instanz für jede Unternehmensgruppe erforderlich, die Med-v-Clients hat, damit die Gruppe ihre eigene virtualisierte Umgebung verwalten kann. Fügen Sie für jede einzelne organisatorische Anforderung eine MED-V-Instanz hinzu.

-   Rechtliche Hinweise – nationale Sicherheit, Datenschutz und treuhänderische Gesetze könnten die Trennung bestimmter Daten oder die Verhinderung anderer Daten an Grenzübergängen erforderlich machen. Fügen Sie bei Bedarf weitere MED-V-Instanzen hinzu, um diese Anforderung zu erfüllen.

Nachdem Sie die Anzahl der für Ihre Infrastruktur erforderlichen MED-V-Instanzen sowie die Begründung für jede Instanz ermittelt haben, geben Sie einen Namen für jede Instanz an.

 

 





